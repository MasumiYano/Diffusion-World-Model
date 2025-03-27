# World Models
- Published Date: 27 March 2018
- Category: World Modeling

---

## 📝 Summary of the World Models
The World Models paper intorduces a novel reinforcement learning framework that enables agent to train in a simulated environment from past experience, improving sample efficiecy. 
Instead of relying on direct interacitons with the real environment, the agent learns a compressed
latent representation of the observations using Varial Autoencoder (VAEs) and predicts future states 
and reward swith an MDN-RNN (Mixture Density Network-based Recurrent Neural Network). A simple linear
controller is then trained within this learned "dream world" using evolution strategies (CMA-ES) and 
successfully transferred to the real environment. The paper also run experiments on CarRacing-v0 and
VizDoom to demonstrate the capability of this approach SOTA (by the time of publishment) performance 
while reducing dependence on real-world interacitons. This work laid the foundation for using generative
models in RL and inspierd subsequence advances in model-based RL.

---

## 💻 Breakdown of the implementation
In this breakdown method, we follow the approach introduced by Ha and Schmidhuber (2018)[^1]. 
The 

---

## 🧪 Experiments & Result
The paper runs experiments on CarRacing-

---

## Reference
[^1]: Ha, D., & Schmidhuber, J. (2018). *Recurrent World Models Facilitate Policy Evolution*. In Advances in Neural Information Processing Systems 31 (pp. 2451–2463). Curran Associates, Inc. [https://papers.nips.cc/paper/7512-recurrent-world-models-facilitate-policy-evolution](https://papers.nips.cc/paper/7512-recurrent-world-models-facilitate-policy-evolution)
