# README: Deep Q-Network (DQN) for Traffic Light Optimization

## Overview
This repository contains a Jupyter Notebook implementing a Deep Q-Network (DQN) for optimizing traffic light control systems. The goal is to minimize traffic congestion and improve traffic flow by learning an optimal traffic light switching policy.

## Key Features
- **Traffic Light Optimization**: Uses DQN to dynamically adjust traffic light timings based on real-time traffic conditions.
- **Deep Reinforcement Learning**: Implements a DQN for learning optimal policies in a traffic control environment.
- **Replay Buffer**: Stores agent experiences to decorrelate data and improve training stability.
- **Target Network**: Uses a separate target network to stabilize Q-value updates.
- **Exploration Strategy**: Epsilon-greedy approach for balancing exploration and exploitation.

## Workflow
### 1. Setup and Initialization
- **Environment Initialization**: The SUMO (Simulation of Urban Mobility) traffic simulation environment is used to emulate real-world traffic scenarios. SUMO is controlled via the TraCI (Traffic Control Interface) library to enable interaction between the simulation and the reinforcement learning agent.
- **Network Design**: Defines the architecture of the Q-network (neural network) for decision-making.
- **Hyperparameters**: Configures learning rate, discount factor, epsilon parameters, and other settings.

### 2. Training
- **Experience Replay**: Samples random batches from the replay buffer for training the Q-network.
- **Bellman Equation Update**: Updates the Q-values using the Bellman equation based on traffic metrics.
- **Target Network Update**: Periodically synchronizes the target network with the main Q-network.

### 3. Traffic Simulation and Interaction
- **SUMO Simulation**: SUMO simulates realistic traffic scenarios, providing state information such as queue lengths, waiting times, and traffic densities.
- **TraCI Commands**: The TraCI library enables the agent to retrieve state data and set traffic light phases dynamically during training and evaluation.

### 4. Evaluation
- **Performance Metrics**: Evaluates the agent's performance, such as average waiting time, queue length, and throughput.
- **Visualization**: Generates plots for traffic flow trends, reward curves, and policy performance.

### 5. Save and Load
- **Model Checkpointing**: Saves trained models for later use.
- **Replay Buffer Serialization**: Stores the replay buffer to resume training.

## File Structure
- `DQN_update_2.ipynb`: Main notebook containing the DQN implementation for traffic light optimization.
- `README.md`: This file, providing an overview of the project.
- `requirements.txt`: Dependencies for running the notebook.

## Prerequisites
1. **Python 3.8+**
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. **SUMO and TraCI**: Ensure SUMO is installed, and the TraCI library is configured.
4. **Jupyter Notebook**: Ensure Jupyter Notebook is installed and accessible.

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/thisisarjun100905/Optimization-of-traffic-signal-light-system
   ```

## Results and Visualizations
- **Traffic Flow Optimization**: Displays the improvements in traffic flow achieved by the agent during training.
- **Reward Trends**: Shows the cumulative rewards to track learning progress.
- **Policy Execution**: Visualizes the agent's learned traffic light control policy in the simulation environment.

## Future Improvements
- **Dueling DQN**: Enhancing the model by separating state-value and advantage streams.
- **Prioritized Experience Replay**: Sampling experiences with prioritization for improved learning.
- **Multi-intersection Scenarios**: Extending the implementation to handle multiple interconnected intersections.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Author
- **Name**: Arjun
- **Email**: arjunkumar100905@gmail.com
- **Linkedin**: www.linkedin.com/in/arjun-ㅤ-585686236

## Acknowledgments
- SUMO for providing a platform for traffic simulation.
- TraCI for enabling interaction between reinforcement learning agents and SUMO.
- The broader reinforcement learning and traffic optimization community for inspiration and tools.

