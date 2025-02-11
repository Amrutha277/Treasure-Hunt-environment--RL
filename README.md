This project implements and optimizes a Treasure Hunt Reinforcement Learning (RL) Grid Environment using SARSA, Q-Learning, and N-Step Double Q-Learning algorithms. The environment is structured as a Markov Decision Process (MDP) where an agent must navigate a grid-based map to maximize rewards while avoiding obstacles. The project focuses on algorithm optimization and hyperparameter tuning to achieve the highest test accuracy.
1. Custom RL Grid Environment
  Grid-Based Navigation: The agent moves within an N x N grid to locate treasure.
  Obstacle & Trap Placement: The environment includes randomized obstacles and traps to introduce stochasticity.
  Custom Reward Function:
  +10 for reaching the treasure.
  -5 for stepping on a trap.
  -1 per step to promote efficiency.
  State Representation: Each state is a coordinate pair (x, y).
2. Implemented RL Algorithms
  A. SARSA (State-Action-Reward-State-Action)
    On-policy RL method, updating Q-values based on the agent’s actual experience.
    Uses epsilon-greedy exploration to balance exploration & exploitation.
    Handles stochastic environments more robustly than Q-learning.
  B. Q-Learning
    Off-policy learning, updating Q-values based on the best possible action in the next state.
    Uses Bellman equation for future reward estimation.
    Generally learns faster than SARSA, but may struggle with environment variability.
  C. N-Step Double Q-Learning
    Extends Q-Learning by using two Q-tables to reduce overestimation bias.
    Uses multi-step returns (n-step updates) for improved learning efficiency.
    More stable convergence compared to one-step Q-learning.
3. Optimization & Performance Enhancements
  Adaptive Epsilon Decay: Dynamically adjusts exploration-exploitation tradeoff.
  Reward Shaping: Introduces intermediary rewards to guide agent learning.
  Hyperparameter Tuning: Grid search on:
  Learning Rate (α): {0.1, 0.01, 0.001}
  Discount Factor (γ): {0.8, 0.9, 0.99}
  Epsilon Decay Strategies
  N-Step Values: {1, 2, 3, 4, 5}
  Policy Benchmarking: Performance comparisons across different RL methods.
4. Model Evaluation & Visualizations
  Reward Progression Graphs: Track total rewards per episode.
  Epsilon Decay Curve: Monitors exploration reduction over time.
  Q-Value Heatmaps: Shows learned Q-values for different states.
  Trajectory Visualization: Displays agent movements on the grid.
