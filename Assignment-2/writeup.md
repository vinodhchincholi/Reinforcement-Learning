# Reinforcement Learning Assignment 2
Vinodh Chincholi, MDS202252

## Q1 Gridworld

### Policy Representation (Softmax)
$$ \pi(s, a) = \frac{e^{\sigma \cdot \theta_{s1, s2, a}}}{\sum_{a'} e^{\sigma \cdot \theta_{s1, s2, a'}}} $$

### Hyperparameters
- **σ = 0.1**: Higher values increase exploration but reduce stability.
- **ϵ = 0.001**: Higher values slow learning; lower values increase training time.
- **maxep = 100**: More episodes improve learning but increase computation time.
- **numtrails = 300**: More trials improve learning but increase computation time.
- **γ = 0.9**: Determines reward dependency on previous steps.
- **α = 0.1, β = 0.1, λ = 0.1, vwα = 0.1**: Learning rates for the baseline reinforce algorithm.

## Q2 Cart-Pole

### Policy Representation (Sigmoid)
$$ \pi(s, a) = \frac{1}{1 + e^{-\sum_{t=1}^{4} t_i \cdot s_i}} $$

### Cart-Pole Problem given parameters
- **g = 9.8**: Acceleration due to gravity.
- **mc = 1**: Mass of the cart.
- **mp = 0.1**: Mass of the pole.
- **F = 10**: Initial force.
- **dt = 0.001**: Time interval for derivative approximation.

### Learning Hyperparameters
- **num_episodes = 100**: More episodes improve learning but increase computation time.
- **γ, λ = 0.9**: Reward dependency on previous steps.
- **α, β = 0.1**: Learning rates for faster but possibly inaccurate learning.
- **delta_theta, delta_w = 0.001**: More accurate derivative approximations at the cost of running time.
