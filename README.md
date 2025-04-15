
# Group_5_CSCN8020_Pacman
Of course! Here's the complete `README.md` content in full — you can copy and paste this directly into your GitHub repository:



# 🎮 MsPacman-v5 Reinforcement Learning using Deep Q-Network (DQN)

This project demonstrates how a Deep Q-Network (DQN) agent can learn to play the **MsPacman** Atari game
using the `ALE/MsPacman-v5`environment from Gymnasium. Implemented using **PyTorch**,
the notebook includes **two experimental setups** to compare training performance.



## 🧠 Project Overview

We used reinforcement learning with DQN to train an agent to play the classic Atari game MsPacman.
The project is designed to run on **Google Colab**, with **Google Drive** used to store checkpoints and models.

### Features
- 🎯 Deep Q-Network (DQN) for learning from pixel inputs
- 🧠 Frame stacking for temporal awareness
- 🧪 Two experimental setups for comparative evaluation
- 📊 Training visualization (reward per episode, moving averages)
- 💾 Model checkpointing to Google Drive


## 📁 File Structure

- `Final_code_with_2_experiments.ipynb` — Main notebook with full DQN training pipeline and two experiments.
- `dqn_checkpoints/` (on Google Drive) — Folder where model checkpoints are stored.



## 🔧 Installation & Setup

### ✅ Install Dependencies

Run this in the first cell of your Google Colab notebook:


!pip install gymnasium[atari] AutoROM
!AutoROM --accept-license


## 🕹️ Environment Details

- **Game**: `ALE/MsPacman-v5`
- **Framework**: Gymnasium
- **Observation Space**: 210×160 RGB frames
- **Action Space**: Discrete with 9 possible actions



## 🧪 Experiments

### 🔁 Experiment 1
- Episodes: `1000`
- Learning Rate: `1e-4`
- Batch Size: `32`
- Gamma (Discount Factor): `0.99`
- Epsilon Decay: `0.998`
- Target Network Update Frequency: `1000` steps

### 🔁 Experiment 2
- Modified hyperparameters (see notebook for detailed configuration)
- Used to evaluate and compare DQN performance under different training conditions


## 🏗️ Model Architecture

The Q-Network is a Convolutional Neural Network (CNN) that takes a stack of 4 preprocessed frames and outputs Q-values for all possible actions.

**Model Summary**:
- **Input**: `(4, 84, 84)` (stacked grayscale frames)
- **Output**: Q-values for each action
- **Layers**:
  - 3 Convolutional Layers with ReLU activation
  - 1 Fully Connected Layer
  - Output Layer for Q-values
- **Loss Function**: Mean Squared Error (MSE)
- **Optimizer**: Adam


## 📉 Results

Performance is evaluated by tracking:
- Reward per episode
- Moving average reward
- Visual improvements in gameplay behavior

Training metrics and learning curves are plotted in the notebook after each experiment.



## 🚀 Future Improvements

Here are some enhancements that can be implemented next:
- 🔁 **Double DQN** to reduce overestimation bias
- 🏆 **Dueling DQN** to separate state-value and advantage
- ⚖️ **Prioritized Experience Replay** for better sampling efficiency
- 📈 **Logging with TensorBoard or W&B** for advanced tracking
- 📼 **Save agent gameplay videos** for performance visualization




## 🤝 Contributors

- **Harika Ravi**
- **Nasr Alani**
- **Paljeet Singh Sambhi**   
- **Priyanka Chitikela**

