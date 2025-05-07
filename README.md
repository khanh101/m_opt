# m_opt

optimization on manifolds : four years ago, when I was still an undergraduate student in Computer Science, I have no idea how to optimize a function on $S^n$ that is the $n$-sphere on $\mathbb{R}^{n+1}$.

**Problem Statement:** Given a differentiable function $f: \mathbb{R}^n \to \mathbb{R}$, find a point $x \in S^n$ that minimizes $f$. Since $S^n$ is compact and $f$ is continuous, the maxmimal for $f$ exists.

At the time, the only method I knew was *projected gradient descent*, that is from a point $x_i \in S^n$, I can calculate the gradient $\nabla f$ at $x_i$, use *gradient descent*  as follows: 

$$
  \tilde{x}\_{i+1} = x_i - \alpha \nabla f
$$

for some small learning rate $\alpha << 1$. And then project $\tilde{x}\_{i+1}$ back to $S^n$ by scale $\tilde{x}\_{i+1}$ into norm $1$

$$
  x\_{i+1} = \frac{\tilde{x}\_{i+1}}{|| \tilde{x}\_{i+1}||}
$$

However, I could not make any analysis on when the algorithm converges. After two years of wasting my life and two years of masters in math, I learnt manifold theory. Now, optimizing on $S^n$ or any (Riemmanian) manifold $M$ or any submanifold of $\mathbb{R}^n$ is a piece of cake.

I will put into this repo several examples on optimzing on common submanifolds of $\mathbb{R}^n$ like $S^n$, linear subspace, hyperbolic space, etc.
