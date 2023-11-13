#### Probabilistic mapping algorithms
Probabilistic mapping 不知道翻译为什么合适，按照我的理解，这是用来解决“建图”这一问题所提出的算法，因此在这里翻译为概率建图。类似的翻译是SLAM（simultaneous localization and mapping），Probabilistic mapping应该是SLAM的一个子类。
概率建图算法要解决的问题是：给定测量集合 $Z^t=\{z^t, z^{t-1}, ..., z^1\}$ 求出在地图空间 $\mathbf{m}$ 上的某种后验概率分布 $p(\mathbf{m}|Z^t)$ 。但是在现实世界中，空间是连续的、无限维度的，对于计算机来说无法求解。这时候就可以把空间离散化成为一个个的网格（gird），求解网格格点上的概率分布。对于每一个格点的分布，如果仍是连续分布，则仍然难以处理，这时候OG（Occupation Grid）就可以排上用场了。在OG建图里，空间被离散化为网格点，每个网格点上的概率分布是一个二元概率分布 $\mu_c\in\{0,1\}$ 。假设空间被分割为 $C$ 个网格点，OG建图所需要考虑的整个地图空间的复杂度降低至 $2^C$。但是这仍然是个指数级的问题，当网格点个数成千上万时，仍然无法求解。 在OG的基础上，可以进一步提出很多算法来解决这一问题，比如基于**贝叶斯推理（[[Bayesian inference]]）**、d-s证据理论（[[Dempster-Shafer evidence theory]]）、模糊集理论（[[Fuzzy set theory]]）。

