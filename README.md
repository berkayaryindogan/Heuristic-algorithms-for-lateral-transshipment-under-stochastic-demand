# Lateral Transshipment Optimization in Retail Networks

## Overview
### ---------------------------------------------------------------------------------------------------
This repository contains a senior design project focused on optimizing **lateral transshipment decisions** between retail stores.  
The study is based on **retail stores**, and aims to minimize inventory-related costs by redistributing stock efficiently among stores.

Three optimization models were developed:
1. **Baseline:** No transshipment
2. **Heuristic 1:** Rule-based proportional allocation
3. **Heuristic 2:** Matching-based heuristic optimization

All notebooks and the accompanying report are included.

---

## Repository Structure

| File | Description |
|------|--------------|
| `heuristic1.ipynb` | Implements **Heuristic 1** – proportional rule-based stock redistribution. |
| `heuristic2.ipynb` | Implements **Heuristic 2** – bisection-based optimization with cost evaluation. |
| `no_transshipment.ipynb` | Baseline model with **no transshipment** between stores. |

---

## Problem Description

Retail chains often face unbalanced stock levels due to varying demand across stores:
- High-demand stores face **stockouts**
- Low-demand stores have **excess inventory**
- Both cases increase total system cost

**Lateral transshipment** allows stock transfers between stores to rebalance inventory, improving service levels and minimizing cost.

---

## Methodology

#### Heuristic 1 – Rule-Based Allocation
- Multi-store, multi-day simulation.  
- Each day, stores classified as **senders** or **receivers**.  
- Transfers made proportionally to demand and critical ratios.  
- Allows multiple transshipments per day.  
- Achieves lowest total cost in experiments.

---

#### Heuristic 2 – Matching-Based Optimization
- Only one sender–receiver pair allowed per day.  
- Uses **bisection search** to minimize combined holding, shortage, and transshipment costs.  
- Employs **Monte Carlo simulation** for cost evaluation.  
- Fewer transfers, slightly higher costs than Heuristic 1, but stable.

---

### 3. Baseline Model
No transshipments are allowed.  
Used to measure the cost benefit of applying lateral transshipment.

✅ **Heuristic 1 achieved the best cost and service balance.**


## Key Findings

- **Heuristic 1** offers the best cost–service tradeoff.  
- **Heuristic 2** yields stable results with lower transshipment volume.