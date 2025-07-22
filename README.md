# AlphaZero From Scratch
___

## Project Description 

AlphaZero is an AI project that learns to master Tic Tac Toe and Connect Four entirely from scratch using reinforcement learning. It uses a combination of Monte Carlo Tree Search (MCTS) and a deep neutral network to improve through self play without relying on human gameplay data or predefined strategies. Over time, it becomes better by learning from its own mistakes and updating its policy and value predictions.
This implementation is inspired by DeepMind's AlphaZero but adapted for simpler games to help understand the core concepts behind self learning game AI
___

## Table of Contents 

- [GIF](#GIFs)
- [Logic](#logic)
- [Technologies](#technologies-used)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
___

Below is an example of the trained AlphaZero AI playing Tic Tac Toe against itself.

![tictactoe](https://github.com/user-attachments/assets/5adeb499-7eac-4f96-bd4b-0683ee6d145f)

Below is an example of the trained AlphaZero AI playing Connect Four against itself.

![connectfour](https://github.com/user-attachments/assets/7cf44ff3-79c5-43a5-93c9-b393a886d346)

___

## Logic: Monte Carlo Tree Search (MCTS)

The core of AlphaZero's decision making lies in *Monte Carlo Tree Search (MCTS). 
MCTS is a powerful algorithm that balances **exploration* (trying new moves) and *exploitation* (choosing known good moves) to make decisions in complex games.

Here's how it works in four main steps:

1. *Selection:*  
   Starting at the root, the algorithm selects child nodes based on the best balance of exploitation (win rate) and exploration (uncertainty).

2. *Expansion:*  
   Once it reaches a leaf node that hasn’t been fully explored, it adds one or more child nodes (new moves).

3. *Simulation (Rollout):*  
   From the new node, the game is simulated until the end, typically with random or policy guided moves.

4. *Backpropagation:*  
   The result of the simulation (win/loss) is propagated back through the tree to update the statistics of each visited node.

This process is repeated thousands of times, allowing the model to build a deep understanding of which moves lead to the most favorable outcomes without brute force search.

In AlphaZero, MCTS is further enhanced by a *deep neural network* that predicts:
- The best move (policy)
- The expected outcome (value)

This synergy between search and learning enables AlphaZero to dominate traditional engines.

___

### Technologies 
- *Python* – Core programming language
- *NumPy* – For numerical computations and board representations
- *PyTorch*  – To build and train the neural network
- *Jupyter Notebook* – For development, experimentation, and visualizations
- *Matplotlib* – To visualize training progress and game play
- *Kaggle Notebooks* – Cloud environment used for training and running simulations
___

## Project Architecture

AlphaZero/
│
├── README.md                   📘 Overview of the project 
├── requirements.txt            📦 Python dependencies
├── .gitignore                  🚫 Files to ignore in Git 
│
├── notebooks/                  📓 Jupyter Notebooks organized by purpose
│   ├── 1.TicTacToe.ipynb
│   ├── 2.MCTS.ipynb
│   ├── 3.Model.ipynb
│   ├── 4.AlphaMCTS.ipynb
│   ├── 5.AlphaSelfPlay.ipynb
│   ├── 6.AlphaTrain.ipynb
│   ├── 7.Alphachangesmade.ipynb
│   ├── 8.ConnectFour.ipynb
│   ├── 9.Alphaparallel.ipynb
│   └── 10.AlphaZero(Eval).ipynb
│
├── models/                     🧠 Trained model files
│   ├── model_0.pt
│   ├── model_1.pt
│   ├── model_2.pt
│   ├── model_7_ConnectFour.pt
│   └── ...                   
│
├── images/                     🖼️ Screenshots or visuals for README
│   ├── tictactoe_example.png
│   └── connectfour_example.png
│
├── src/                        💻 Python scripts if you convert notebooks to .py later
│   ├── mcts.py
│   ├── model.py
│   ├── train.py
│   ├── self_play.py
│   └── ... 
│
└── .ipynb_checkpoints/        💻 Backup versions

___

## Contribution 

Contributions are welcome!

If you would like to improve the AlphaZero project whether by optimizing the training loop, enhancing visualizations, or extending the AI to other games feel free to fork this repository and submit a pull request.


___

## Hot Take

**Magnus Carlsen**, a Norwegian chess grandmaster, learned and refined his skills by studying games and strategies influenced by **AlphaZero**.






















