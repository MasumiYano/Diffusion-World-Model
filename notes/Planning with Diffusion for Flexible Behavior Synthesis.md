# Planning with Diffusion for Flexible Behavior Synthesis
- Published Date: 20 May 2022
- Category: Diffusion Planner

---

## 📝 Summary of the World Models

This paper proposes Diffuser, a novel framework for trajectory optimization in reinforcement learning that integrates diffusion probabilistic models into the planning process. Traditional model-based RL separates dynamics modeling from planning, which can lead to adversarial trajectories and poor long-horizon performance. Diffuser instead learns a generative model of entire trajectories using a denoising diffusion process. This model allows planning to be treated as sampling with guidance, using classifier gradients or inpainting for goal conditioning. The approach supports long-horizon, sparse-reward planning, multi-task generalization, and flexible test-time behavior synthesis. By tying model learning and planning together, Diffuser significantly outperforms prior offline RL methods on benchmarks like Maze2D, block stacking, and D4RL locomotion, while offering elegant properties like temporal compositionality and variable-length planning horizons.

---

## 💡Key Contribution
- Trajectory-level Diffusion Model:
    - Proposes a trajectory-level denoising diffusion probabilistic model that generates entire state-action sequences concurrently instead of autoregressively.

- Unified Planning and Sampling:
    - Planning is reframed as conditional sampling from the generative model, aligning model learning directly with planning needs

- Flexible Conditioning:
    - Uses classifier-guided sampling where the return function gradient influences trajectory generation.
    - Implements image inpainting-style constraints to satisfy goal-reaching conditions.

- Test-Time Compositionality
    - Able to combine unseen tasks during inference by adding reward gradients
    Supports variable-length plans due to fully convolutional architecture

---

## 💻 Breakdown of the implementation
Coming soon...

---

## 🧪 Experiments & Result

### Benchmarks:
- Maze2D (Fu et al., 2020): Sparse-reward navigatio tasks [^1]
- Multi2D: Multi-task version with randomized goals.
- Block Stacking: Test-time flexible planning (conditional/unconditional/rearrangement).
- D4RL Locomotion: Standard offline RL benchmark with varying data quality. 

### Baselines:
- Model-Free: **CQL**[^2], **IQL**[^3], **BCQ**[^4]
- Return-Conditioning: **Decision Transformer (DT)** [^5]
- Model-Based: **Trajectory Transformer (TT)**[^6], **MOPO**[^7], **MORel**[^8], **MBOP**[^9]
- Traditional Planning: **MPPI**[^10]

### Results
**Maze2D and Multi2D Performance (Long-Horizon Planning)**:
![result maze](../figures/Diffuser_Maze2D_Result.png)

**Block Stacking Performance (Test-time Flexibility)**:
![result stacking](../figures/Diffuser_Stacking.png)

**Offline RL (D4RL Locomotion)**:
![result dr4l](../figures/Diffuser_D4RL.png)

---

## Reference
[^1]: Fu J., Kumar, A., et al., (2020). *D4RL: Datasets for deep data-driven reinforcement learning*. arXiv preprint at *arXiv:2004.072.07219* 2020
[^2]: Kumar, A., Zhou, A. et al., (2020). *Conservative Q-learning for offline reinforcement learnin*. NeurIPS 2020.
[^3]: Kostriv, I., Nair, A., et al., (2022). *Offline reinforcement learning with implicit Q-learing* ICLR 2022
[^4]: Fujimoto , S., Meger, D., et al., (2019) *Off-policy deep reinforcement learning without exploration* ICML 2019
[^5]: Chen, L., Lu, K., et al., (2021), *Decision Transformer: Reinforcement learning via sequence modeling* NeurIPS 2021
[^6]: Janner, M., Li, Q., et al., (2021) *Offline reinforcement learning as one big sequence modeling problem* NeurIPS 2021
[^7]: Yu, T., Thomas, G., et al., (2020) *MOPO: Model-based offline policy optimization* NeurIPS 20220
[^8]: Kidambi, R., Rajeswaran A., (2020) *MOReL: Model-based offline reinforcement learning* NeurIPS 2020
[^9]: Argenson, A., Dulac-Arnold, G (2021) *Model-based offline planning* ICLR 2021
[^10]: Williams, G., Aldrich, A., et al., (2015) *Model predictive path integral control using covariance variable importance sampling* arXiv preprint at arXiv:1509.01149 2015
