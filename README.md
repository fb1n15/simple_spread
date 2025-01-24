# Simple_spread

## MARL environment

The `simple_spread_v3` environment is part of the Multi-Agent Particle Environments (MPE) within the PettingZoo library, designed for multi-agent reinforcement learning research. In this environment, multiple agents aim to cover all landmarks while avoiding collisions. Agents receive a global reward based on their proximity to the nearest landmark and are penalized for collisions with other agents. The environment supports both discrete and continuous action spaces, controlled by the `continuous_actions` parameter. When set to `True`, agents can select continuous movement velocities in each of the four cardinal directions, allowing for more nuanced control compared to discrete actions. ([PettingZoo Documentation](https://pettingzoo.farama.org/environments/mpe/simple_spread/?utm_source=chatgpt.com))

Continuous action spaces in reinforcement learning allow agents to select actions from a continuous range, enabling more precise and flexible decision-making. This is particularly beneficial in tasks requiring fine motor control or where actions are not naturally discrete. However, learning optimal policies in continuous action spaces can be more challenging due to the infinite range of possible actions, necessitating specialized algorithms like Deep Deterministic Policy Gradient (DDPG) or Proximal Policy Optimization (PPO) to effectively navigate and learn within these spaces. ([SpringerLink](https://link.springer.com/chapter/10.1007/978-3-642-27645-3_7?utm_source=chatgpt.com)) 

## Files in the repository

**1. `pyproject.toml`**

- **Purpose**: This file serves as the configuration for Poetry, a Python dependency management tool. It defines project metadata, dependencies, and build settings.

- **Significance**: By utilizing `pyproject.toml`, you streamline package management, ensuring consistent environments across different setups.

**2. `simple_speaker_listener.ipynb`**

- **Focus**: This Jupyter Notebook explores reinforcement learning (RL) using the Proximal Policy Optimization (PPO) algorithm.

- **Details**:
  - **Proximal Policy Optimization (PPO)**: A policy gradient method in RL that alternates between sampling data through interaction with the environment and optimizing a surrogate objective function using stochastic gradient ascent. PPO is known for its simplicity and efficiency in training RL agents. ([arXiv](https://arxiv.org/abs/1707.06347?utm_source=chatgpt.com))

**3. `simple_spread_env_with_RWs.ipynb`**

- **Focus**: This notebook delves into reinforcement learning using the PPO algorithm, enhanced by a reward machine that encourages adherence to a specified norm.

- **Details**:
  - **Reward Machines**: These are finite state machines used to represent reward functions in RL. They expose the structure of reward functions, allowing agents to exploit this structure for more efficient learning. By incorporating reward machines, the agent can decompose tasks and apply automated reward shaping, leading to improved learning efficiency. ([arXiv](https://arxiv.org/abs/2010.03950?utm_source=chatgpt.com))

Collectively, these components indicate a project centered on advanced reinforcement learning techniques, emphasizing the integration of structured reward representations to enhance agent performance. 
