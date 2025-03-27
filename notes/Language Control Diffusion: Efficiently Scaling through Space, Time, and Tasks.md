# Language Control Diffusion: Efficiently Scaling through Space, Time, and Tasks
- Published Date: 27 Oct 2022
- Category: Diffusion Planning

---
## 📝 Summary of the World Models
The paper introduces a hierarchical framework for language-conditioned reinforcement learning (RL) that 
leverages diffusion models as high-level planners to generate long-horizon action plans in a low-dimensional
latent space. By conditioning the diffusion model on the natural language instructions and decoupling planning from execution,
the proposed framework can generalize to a tasks efficiently scale across spatial (high-dimensional visual inputs),
temporal (long-horizon tasks), and task (diverse instructions) axes. The high-level diffusion model outputs subsamples latent goals,
which are then executed by a pre-trained, goal-conditioned low-level policy (LLP). This resuces computational cost and improving 
inference speed using DDIM sampling and temporal abstraction.

---
## 💡Key Contribution
- Using natural transfer model (T5-XXL) to encode the natural language instructions
- Utilize temporal U-Net and perform 1D convolutions across the time dimension of the latent plan
- Use diffusion model to generate long-horizon action plans in a low-dimensional latent space

---
## 💻 Breakdown of the implementation

---
## 🧪 Experiments & Result

### Benchmarks:
- CALVIN: Benchmarks for language conditioned policy learning [^1]
- CLEVR-Robot [^2]

### Baselines:
- SPIL (Skill Prior Imitation Learning) [^3]
- HULC [^4]
- MCIL [^5]

### Results

---
## Reference
