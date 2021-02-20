# INVASE: INstance-wise VAriable SElection using neural networks \[Literature Survey]

#### Authors: Jinsung Yoon, James Jordon, Mihaela van der Schaar
#### Conference: ICLR 2019

**Problem Statement**: Instance-wise feature selection where there can be different number of features selected for each instance.  

**Motivation and Methodology**: Instance-wise feature selection was introduced by the L2X[ref] paper in 2018. It involves finding a subset of features that are most informative for each given example. But, in their methodology, the user had to provide the number of features to be selected as input. This could lead to the problem of over-explanation. So, to mitigate this problem the authors of the INVASE paper take a different approach wherein they try to minimize the KL divergence between the conditional distributions $$Y \vert X$$ and $$Y \vert X_S$$. And, in order to bypass the pain of backprop through sampling, the authors use an actor-critique framework from the RL literature. 

At this point it might not be clear how doing the above solves the issue that we had, but it does and we will see how soon.

**Methodology in detail**:

Let $$\mathcal{X}$$ be a $$d$$-dimensional feature space,

$$
\mathcal{X}=\mathcal{X}_{1} \times \ldots \times \mathcal{X}_{d}
$$

and $$\mathcal{Y}$$ be a discrete label space,

$$
\mathcal{Y}=\{1, \ldots, c\}
$$

Let $$ \mathbf{X}=\left(X_{1}, \ldots, X_{d}\right) \in \mathcal{X} $$ and $$\mathbf{Y} \in \mathcal{Y}$$ be random variables with joint p.m.f.(or p.d.f.) be $$p$$ and marginal p.m.f.(or p.d.f.) be $$p_X$$ and $$p_Y$$ respectively.


