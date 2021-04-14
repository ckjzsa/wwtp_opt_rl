# Optimization of operation parameters towards sustainable WWTP based on deep reinforcement learning

## 1. Project Introduction
This study used a novel technique, Multi-Agent Deep Reinforcement Learning (MADRL), to optimize dissolved oxygen (DO) and dosage in a hypothetical WWTP. The reward function is specially designed as LCA-based form to achieve sustainability optimization. Four scenarios: baseline, LCA-oriented, cost-oriented and effluent-oriented are considered.

## 2. Learning
The MADDPG learning process mainly follows the original paper and is introduced in this section. 
Different from the original paper, Gaussian noise $\mathcal{N}$ rather than Ornstein-Uhlenbeck process is used for exploration.
Hyperparameters of MADDPG are fine tuned, before training, $10,000$ sample data are acquired by Monte Carlo sampling, actions are sampled from uniform distribution. 
The value of DO ranges from 0 to 5 $mg/L$, and chemical dosage ranges from 0 to 800 $kg/d$. The first training is implemented under LCA scenario, with the SRT as
15 days. For other scenarios, transfer learning is applied to narrow down required data size by freezing part of the network. 

## 3. Result
The result shows thatoptimization based on LCA has lower environmental impacts compared to baseline scenario, as cost, energy consumption and greenhouse gas emissions reduce to 0.890 CNY/m$^3$-ww, 0.530 kWh/m$^3$-ww, 2.491 kg CO$_2$-eq/m$^3$-ww respectively. The cost-oriented control strategy exhibits comparable overall performance to the LCA-driven strategy since it sacrifices environmental benefits but has lower cost as 0.873 CNY/m$^3$-ww. 

## 4. Paper
[Paper](https://arxiv.org/pdf/2008.10417.pdf) 

### Cite the paper as follows:

    @inproceedings{Chena2020OptimizationOO,
    title={Optimization of operation parameters towards sustainable WWTP based on deep reinforcement learning},
    author={Kehua Chen and Hongcheng Wang and Borja Valverde Perezc and Luca Vezzaro and A. Wang},
    year={2020}
    }

