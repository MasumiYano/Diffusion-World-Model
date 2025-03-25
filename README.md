# 🌍Diffusion World Models in Reinforcement Learning (RL) - Survey 

![Image of Timeline](figures/timeline_draft_1.png)

This repository is a comprehensive resource hub for ongoing survey on **Diffusion Models in World Modeling for RL**. It includes:

- 📄 A collection of key papers that introduced or advanced the field.
- 📎 Summaries and implementation notes for each work.
- 🧠 Planned code implementation of representative algorithms (e.g., IRIS, DWM, DIAMOND, DreamerV3, etc).
- 🕰️ A timeline mapping the evolution of DWM research
- 🧪 Experimental and architectural insights aimed at bridging theoretical understanding with practical implementation

---

## Motivation
Diffusion models have recently emerged as powerful tools not only in generative modeling but also in the realm of reinforcement learning. As an alternative to traditional dynamics modeling (approaches (e.g., RNNs, Transformers), diffusion-based world models offer:

- Better visual fidelity in imagined rollouts
- Long-horizon and multimodal future prediction
- Reduced compounding errors from autoregressive rollouts
- Robust planning in offline and online RL settings. 

This survey investigates the intersection of **diffusion modeling** and **world models** in RL, focusing on (MAYBE): 
- Architecture design
- Model training strategies 
- Planning & decision-making capabilities
- Sample efficiency and rollouts fidelity.

--- 

## 📚 Included Papers

The repository includes PDFs and sumaries of major works, such as:

- **[World Models (Ha & Schmidhuber, 2018)]**
- **[IRIS: Transformers as Sample-Efficient World Models]**
- **[Diffusion World Models (ICLR 2024)]**
- **[DIAMOND: Diffusion as Environment Dreams]**
- **[DreamerV3: Mastering Diverse Domains]**

... and more

Each paper will be accompanies by:
- A brief symmary 
- Key contributions
- Implementation notes (architecture, training schedule, planning interface).
- Model-based RL setting and evaluation protocol.

---

## [MAYBE] Code Implementation

We aim to reproduce (or minimally implement) the core ideas from the following works:
- List 

---

# 🛠️ Repository Structure
```bash
📁 papers/             # PDFs and summaries
📁 notes/              # Annotated breakdowns of methods
📁 implementations/    # Code implementations (MAYBE)
📁 figures/            # Diagrams & timelines
📄 README.md
```

---

## 🤝 Contributing
This project is under active development. Feel free to open issues or pull requests if you:
- Found a mistake in a summary
- Want to contribute code
- Have implementation suggestions

---

## 📜 Citation

Coming soon 

---

## 📬 Contact

If you're working in this space and want to collaborate or discuss insights, feel free to reach out!

E-mail: masumi76@uw.edu
