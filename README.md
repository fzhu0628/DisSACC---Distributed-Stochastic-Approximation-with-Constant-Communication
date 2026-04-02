# Distributed Stochastic Approximation with Constant Communication (DisSACC)
Feng Zhu, Aritra Mitra, Robert W. Heath Jr.  
*IEEE Asilomar Conference on Signals, Systems, and Computers, 2025*

---

## Overview

We study a general **distributed stochastic approximation (SA)** problem with heterogeneous agents, where the goal is to find the root of the average operator across agents.

This setting captures a wide range of applications, including:
- Federated learning
- Multi-agent reinforcement learning (RL)
- Variational inequalities and fixed-point problems

---

## Key Challenges

Existing approaches typically suffer from one or more of the following:

- ❌ Lack of linear speedup in sample complexity  
- ❌ Bias due to heterogeneity across agents  
- ❌ High communication cost  

---

## Our Approach: DisSACC

We propose **DisSACC (Distributed Stochastic Approximation with Constant Communication)**, which is based on a simple but effective idea:

> Instead of performing many noisy local updates, we **aggregate samples locally to construct a refined operator**, and perform fewer, higher-quality updates.

### Key Idea

- Each agent collects multiple samples per round
- Constructs a **variance-reduced operator**
- Performs **one update per round**
- Server aggregates across agents
<img width="882" height="815" alt="image" src="https://github.com/user-attachments/assets/04c7d03b-7c86-4af6-ad2a-12aa6bc5da31" />


---

## Main Results

DisSACC achieves:

- ✅ **Exact convergence** to the global solution  
- ✅ **Linear speedup** in the number of agents (M-fold variance reduction)  
- ✅ **No heterogeneity-induced bias**  
- ✅ **Near-constant communication complexity**: $\tilde{O}(1)$

---

## Why It Matters

This work shows that it is possible to simultaneously achieve:

- statistical efficiency (sample complexity)  
- communication efficiency  
- robustness to heterogeneity  

which are typically conflicting objectives in federated and multi-agent learning systems.

---

## Paper

You can find the paper here:

👉 [PDF](Asilomar25.pdf)

---

## Citation

If you find this work useful, please cite:

```bibtex
@inproceedings{zhu2025dissacc,
  title={Distributed Stochastic Approximation with Constant Communication},
  author={Zhu, Feng and Mitra, Aritra and Heath, Robert W.},
  booktitle={IEEE Asilomar Conference},
  year={2025}
}
