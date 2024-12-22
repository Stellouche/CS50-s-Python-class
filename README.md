# CS50-s-Python-class
CS50’s Introduction to Artificial Intelligence with Python

# Degrees Project

## Description
The Degrees Project is an implementation of a search algorithm to determine the "degrees of separation" between two actors in the Hollywood film industry. Inspired by the "Six Degrees of Kevin Bacon" game, this program finds the shortest path of connections between two actors based on movies they have starred in together.

## How to Use
1. Clone the repository to your local machine or download the Degrees.zip.
2. Ensure you have Python 3.12 or later installed.
3. Navigate to the project directory.
4. Run the following command to execute the program:
   ```bash
   python degrees.py [directory]
   ```
   - Replace `[directory]` with either `small` or `large`, depending on the dataset you want to use.

5. When prompted, enter the names of two actors to find their degrees of separation.

Example:
```bash
$ python degrees.py small
Loading data...
Data loaded.
Name: Emma Watson
Name: Jennifer Lawrence
3 degrees of separation.
1: Emma Watson and Brendan Gleeson starred in Harry Potter and the Order of the Phoenix
2: Brendan Gleeson and Michael Fassbender starred in Trespass Against Us
3: Michael Fassbender and Jennifer Lawrence starred in X-Men: First Class
```
## Conclusion
The Degrees Project provides a concrete result by identifying the shortest chain of connections between two actors through shared movies. This result demonstrates how interconnected the film industry is and how search algorithms efficiently uncover these paths, providing valuable insights into relationships within the dataset.
# Tic-Tac-Toe AI Project

## Description
This project implements an optimal AI player for the game Tic-Tac-Toe using the Minimax algorithm. The AI is designed to make the best possible moves at every stage of the game. You can play against the AI via a graphical interface powered by Pygame.

## How to Use

### Prerequisites
- Python 3.8 or later
- Pygame library

Install the required dependencies by running:
```bash
pip install -r requirements.txt
```

### Running the Game
1. Clone the repository to your local machine or download the zip file.
2. Navigate to the project directory and install the requirement.txt.
3. Run the following command to start the game:
   ```bash
   python runner.py
   ```

### Playing the Game
- When the game starts, choose whether to play as `X` or `O`.
- The game alternates turns between the player and the AI.
- The AI is designed to play optimally, ensuring that it never loses when both players play perfectly.

## Features
- Fully implemented Minimax algorithm for optimal AI decision-making.
- Graphical interface built with Pygame for an interactive gaming experience.
- Handles all game scenarios, including ties, wins, and valid/invalid moves.

## Core Functions
- **`player(board)`**: Determines which player’s turn it is.
- **`actions(board)`**: Returns all possible moves on the board.
- **`result(board, action)`**: Generates a new board state after a move.
- **`winner(board)`**: Determines if there is a winner.
- **`terminal(board)`**: Checks if the game is over.
- **`utility(board)`**: Assigns a utility value to the board (1, -1, or 0).
- **`minimax(board)`**: Computes the optimal move for the current player.

## Notes
- The AI cannot be beaten if it plays optimally.
- If both players play perfectly, the game will always end in a tie.


