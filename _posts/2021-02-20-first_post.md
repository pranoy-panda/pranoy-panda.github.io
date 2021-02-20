# INVASE: INstance-wise VAriable SElection using neural networks \[Literature Survey]

#### Authors: Jinsung Yoon, James Jordon, Mihaela van der Schaar
#### Conference: ICLR 2019

**Problem Statement**: Instance-wise feature selection where there can be different number of features selected for each instance.  

**Motivation and Methodology**: Instance-wise feature selection was introduced by the L2X[ref] paper in 2018. It involves finding a subset of features that are most informative for each given example. But, in their methodology, the user had to provide the number of features to be selected as input. This could lead to the problem of over-explanation. So, to mitigate this problem the authors of the INVASE paper take a different approach wherein they try to minimize the KL divergence between the conditional distributions $$Y \vert X$$ and $$Y \vert X_S$$. And, in order to bypass the pain of backprop through sampling, the authors use an actor-critique framework from the RL literature. 

At this point it might not be clear how doing the above solves the issue that we had, but it does and we will see how soon.

**Methodology in detail**:

