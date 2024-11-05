![PacManCNN👻](https://github.com/user-attachments/assets/256f3b2d-c499-4e41-93c8-5b5772c89a8a)

This project implements a Deep Convolutional Q-Learning Network (DCQN) to train an AI agent to play the classic Pac-Man game. The agent utilizes reinforcement learning and leverages convolutional neural networks to process visual input and make decisions in real time.

**Table of Contents**
1. Requirements
2. Installation
3. Creating the Architecture of the Neural Network
4. Setting Up the Environment
5. Defining the Agent
6. Training the Agent
7. Visualizing the results
8. Troubleshooting

**Requirements** \
Python 3.10+ \
Libraries

- `OS`: Handle environment variables.
- `random`: Used for implementing epsilon-greedy.
- `numpy`: Stacking arrays and managing state/action values.
- `torch`: Providers tensors similar to numpy but optimized for GPU processing.
- `torch.nn`: Creates the convolutional and fully connected layers of the Q-network.
- `torch.optim`: Optimazation algorithms which update weights of neural networks based on loss calculated.
- `torch.nn.functional`: Contains activation functions and loss functions.
- `collections.deque`: Double-ended queue that handles agent's experiences for replay.
- `torch.utils.data`: Creates data loaders for mini-batch training.
- `gymnasium`: Library used to create and interact with reinforcement learning environments.
- `PIL`: Pillow enables image processing, it handles game frames for processing.
- `torchvision.trandorms`: resizes and normalizes frames to feed into neural network.
- `imageio`: Converts agent's actions into a video for review.
- `IPython.display`: Plays the created video in browser.
- `gym.wrappers.monitoring.video_recorder`: Wrapper for recording the agent's interactions.

*Optional*: Set up environment in Google Colab to save space in hard drive.

**Installation** \
In this section, we install the necessary packages for the project, including Gymnasium, which is used for creating the environment for the game.
![Installation](https://github.com/user-attachments/assets/7489da76-200e-484a-a688-51838eeb6ac6)

Additionally, we import essential Python libraries required for the agent's implementation.
![libraries](https://github.com/user-attachments/assets/8faa24f6-099b-4637-8b0d-4d501af74ee1)

**Creating the Architecture of the Neural Network** \
Define the architecture of the neural network used by the agent. It consists of several convolutional layers followed by fully connected layers to process the game state and predict action values.
![Architecture](https://github.com/user-attachments/assets/a00e23c9-c42b-4bc8-97b3-902d9db79076)

**Setting Up the Environment** \
Here, we initialize the Ms. Pac-Man game environment, retrieves the state shape, state size, and number of possible actions that the agent can take.
![Environment](https://github.com/user-attachments/assets/f85bccc7-7ac6-4eda-85e0-ef72926a8f0a)

Next, we set the hyperparameters for the training process.
![hyperparameters](https://github.com/user-attachments/assets/8364ba6e-2a9f-46ff-970f-02f245262d61)

This function preprocesses the game frames by resizing and normalizing them, making them suitable for input into the neural network.
![ProcessFrames](https://github.com/user-attachments/assets/0be5b282-88d1-45b0-979e-07a33c23bbec)

**Defining the Agent** \
Below we create the agent that interacts with the environment. It contains methods for storing experiences, selecting actions, and learning from past experiences.
![Agent](https://github.com/user-attachments/assets/777c1136-eef2-4c6b-a4c8-e3e544f7d7d2)

Up next, we create an instance of the agent class, providing it with the number of actions available in pacman.
![InstanceAgent](https://github.com/user-attachments/assets/742f739d-fac4-46ef-b4b7-edfa85410ce9)

**Training the Agent** \
This loop trains the agent over a specified number of episodes. It continuously interacts with the environment, collects rewards, and updates its policy based on its experiences.
![TrainingAgent](https://github.com/user-attachments/assets/ca613906-ed2b-42e8-b387-42da754d3bd9)

**Visualizing the Results** \
Finally, we capture the agent's gameplay and save it as a video file, allowing you to visualize the agent's performance in the environment.
![Visualize](https://github.com/user-attachments/assets/b955e72f-3383-478e-aa7e-856345e44e12)

**Troubleshooting**
- Xformers Warning: If xformers is not installed, use pip install xformers to enable memory-efficient attention.
- Deprecation Warnings: Keep libraries updated as some functionalities might be deprecated.
