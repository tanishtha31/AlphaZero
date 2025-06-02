# AlphaZero From Scratch



![tictactoe](https://github.com/user-attachments/assets/5adeb499-7eac-4f96-bd4b-0683ee6d145f)

![connectfour](https://github.com/user-attachments/assets/7cf44ff3-79c5-43a5-93c9-b393a886d346)



___


**AlphaZero** is a game-playing algorithm that uses artificial intelligence and machine learning techniques to learn how to play board games at a suerhuman level.

___

## Logic: Monte Carlo Tree Search (MCTS)

The core of AlphaZero's decision-making lies in *Monte Carlo Tree Search (MCTS). MCTS is a powerful algorithm that balances **exploration* (trying new moves) and *exploitation* (choosing known good moves) to make decisions in complex games.

Here's how it works in four main steps:

1. *Selection:*  
   Starting at the root, the algorithm selects child nodes based on the best balance of exploitation (win rate) and exploration (uncertainty).

2. *Expansion:*  
   Once it reaches a leaf node that hasn’t been fully explored, it adds one or more child nodes (new moves).

3. *Simulation (Rollout):*  
   From the new node, the game is simulated until the end, typically with random or policy-guided moves.

4. *Backpropagation:*  
   The result of the simulation (win/loss) is propagated back through the tree to update the statistics of each visited node.

This process is repeated thousands of times, allowing the model to build a deep understanding of which moves lead to the most favorable outcomes — without brute-force search.

In AlphaZero, MCTS is further enhanced by a *deep neural network* that predicts:
- The best move (policy)
- The expected outcome (value)

This synergy between search and learning enables AlphaZero to dominate traditional engines.

___

### Tech Stack 
- *Python* – Core programming language
- *NumPy* – For numerical computations and board representations
- *PyTorch*  – To build and train the neural network
- *Jupyter Notebook* – For development, experimentation, and visualizations
- *Matplotlib* – To visualize training progress and game play
- *Kaggle Notebooks* – Cloud environment used for training and running simulations
  
___

## Hot Take

**Magnus Carlsen**, a Norwegian chess grandmaster, learned and refined his skills by studying games and strategies influenced by **AlphaZero**.






















