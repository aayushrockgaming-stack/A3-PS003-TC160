# Flow Forge — Federated Traffic-Flow Prediction

**Hackathon:** AIORI Hackathon 3  
**Problem Statement:** PS-003 — Federated Traffic-Flow Prediction with Communication-Cost Evaluation  
**Category:** Smart Cities  
**Team:** Flow Forge

## Team

| Name | Email |
|------|-------|
| Ayush Rastogi | ayushstudy263@gmail.com |
| Purvi Jain | purvijain22jul2006@gmail.com |
| Dr. Atul Srivastava | asrivastava5@lko.amity.edu |

## Intro Video
Complete description of the problem statement 
https://youtu.be/5wjOAO3cRCo
Short description of the problem statement 
https://youtu.be/RWwwxcE9wKE
## Overview

Flow Forge explores federated learning for road-traffic forecasting. It distributes a public traffic dataset across virtual clients that train locally and share model updates with a central server using Federated Averaging (FedAvg), rather than sending raw training data.

The project compares centralized, local-only and federated models, studies IID and non-IID traffic patterns, and evaluates prediction accuracy against communication costs and convergence.

## Approach

- **Dataset:** METR-LA traffic-sensor speed readings for the core benchmark.
- **Forecasting model:** A compact GRU model using historical speed readings to predict future speeds.
- **Clients:** 3–5 simulated clients with IID and non-IID data partitions.
- **Evaluation:** MAE, RMSE, communication bytes per round, cumulative bytes and convergence.
- **Reproducibility:** Experiments across three random seeds with chronological train/validation/test splits.
- **Planned extension:** A separate Pune road-network simulation using SUMO, with simulated data clearly distinguished from the official benchmark.

## Repository Contents

| File | Description |
|------|-------------|
| `Proposed-structure-hackathon.pdf` | Presentation following the AIORI proposed structure |
| `README.md` | Project overview, approach and references |

## Scope and Limitations

The core project uses a public dataset and simulated federated clients. The Pune simulation is an optional extension and does not represent real measured Pune traffic. Communication cost initially counts serialized model-weight payloads, not all real-world network overhead. Federated learning alone does not guarantee formal privacy.

## References

1. McMahan et al., “Communication-Efficient Learning of Deep Networks from Decentralized Data,” AISTATS 2017: https://proceedings.mlr.press/v54/mcmahan17a.html
2. Google Research, “Federated Learning: Collaborative Machine Learning without Centralized Training Data”: https://research.google/blog/federated-learning-collaborative-machine-learning-without-centralized-training-data/
3. SUMO Documentation: https://sumo.dlr.de/docs/
