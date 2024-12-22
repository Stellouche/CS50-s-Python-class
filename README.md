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
  
# Knights and Knaves AI Project

## Description
This project solves logical puzzles inspired by Raymond Smullyan's "Knights and Knaves." Each character in the puzzles is either a knight, who always tells the truth, or a knave, who always lies. The goal is to determine whether each character is a knight or a knave based on their statements.

The solution is implemented using propositional logic, where an AI uses model-checking to deduce the truth about each character.

## How to Use

### Prerequisites
- Python 3.8 or later

### Running the Program
1. Clone the repository to your local machine or download the zip file.
2. Navigate to the project directory.
3. Run the following command:
   ```bash
   python puzzle.py
   ```

### Output
The program will evaluate each puzzle and print the status of each character (whether they are a knight or a knave). For example:
```plaintext
Puzzle 0
    A is a Knave
Puzzle 1
    A is a Knave
    B is a Knight
Puzzle 2
    A is a Knight
    B is a Knave
Puzzle 3
    A is a Knight
    B is a Knave
    C is a Knight
```

## Puzzles Solved

### Puzzle 0
- **Setup**: A says, "I am both a knight and a knave."
- **Logic**: This statement is inherently contradictory, so A must be a knave.

### Puzzle 1
- **Setup**: A says, "We are both knaves." B says nothing.
- **Logic**: If A were a knight, their statement would contradict the rules of the puzzle. Therefore, A is a knave, and B must be a knight.

### Puzzle 2
- **Setup**: 
  - A says, "We are the same kind."
  - B says, "We are of different kinds."
- **Logic**: The statements are mutually exclusive. If A is a knight, their statement is true, and B is also a knight. Otherwise, A is a knave, and B is a knight.

### Puzzle 3
- **Setup**:
  - A says either "I am a knight" or "I am a knave," but you don't know which.
  - B says, "A said 'I am a knave.'"
  - B says, "C is a knave."
  - C says, "A is a knight."
- **Logic**: The statements interact to determine that A is a knight, B is a knave, and C is a knight.

## Implementation Details
- **Propositional Logic**: Statements are represented as logical formulas using classes like `And`, `Or`, `Not`, `Implication`, and `Biconditional`.
- **Model Checking**: The program uses a model-checking algorithm to evaluate whether the knowledge base entails the query.
- **Logic.py**: Contains the implementation of propositional logic and the model-checking algorithm.
- **Puzzle.py**: Defines the puzzles and their corresponding knowledge bases.

## Notes
- The AI deduces solutions based on logical consistency; it does not "guess."
- You can extend the project by adding more puzzles with new characters and statements.

# Minesweeper AI Project

## Description
This project implements an AI to play Minesweeper using logical inference. The AI uses a knowledge-based approach to infer the location of mines and make safe moves, aiming to win the game by marking all mines correctly.

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
2. Navigate to the project directory.
3. Run the following command to start the game:
   ```bash
   python runner.py
   ```

### Playing the Game
- The game board consists of a grid of cells, some of which contain hidden mines.
- Left-click a cell to reveal it.
- Right-click a cell to flag it as a mine.
- Use the "AI Move" button to let the AI make a move based on its knowledge base.
- Use the "Reset" button to restart the game.

## Features
- **Knowledge Representation**: The AI uses logical sentences to represent knowledge about the Minesweeper board.
- **Inference**:
  - Marks cells as safe or mines based on knowledge.
  - Infers new sentences by combining existing knowledge.
  - Simplifies knowledge by removing known cells.
- **Decision Making**:
  - Chooses safe moves when available.
  - Makes random moves if no safe moves are known.

## Core Classes and Methods

### `Sentence` Class
- **`known_mines`**: Identifies cells that are certainly mines.
- **`known_safes`**: Identifies cells that are certainly safe.
- **`mark_mine(cell)`**: Updates the sentence when a cell is confirmed as a mine.
- **`mark_safe(cell)`**: Updates the sentence when a cell is confirmed as safe.

### `MinesweeperAI` Class
- **`add_knowledge(cell, count)`**:
  - Marks a cell as safe.
  - Adds a new sentence to the knowledge base based on the cell’s neighbors and mine count.
  - Updates knowledge to deduce new safe cells and mines.
- **`make_safe_move()`**: Returns a cell known to be safe.
- **`make_random_move()`**: Chooses a random cell that is not yet known to be a mine or already clicked.
- **`update_knowledge()`**: Simplifies and infers new sentences from the knowledge base.

## Example Output
When running `runner.py`, the game will display the Minesweeper board, and the AI will make logical moves. Example scenarios:
- If a safe move is available:
  ```plaintext
  AI making safe move.
  ```
- If no safe moves are known:
  ```plaintext
  No known safe moves, AI making random move.
  ```

## Notes
- The AI may still lose if it must guess randomly.
- The project demonstrates the use of logical inference in a game environment.
# PageRank AI Project

## Description
This project implements the PageRank algorithm, which ranks web pages by importance. The algorithm computes the probability that a random surfer ends up on each page, either by following links from the current page or by jumping to a random page in the corpus.

Two methods are used to calculate PageRank:
1. **Sampling Method**: Simulates a random surfer visiting pages.
2. **Iterative Method**: Uses a mathematical formula to iteratively compute PageRank until convergence.

## How to Use

### Prerequisites
- Python 3.8 or later

### Running the Program
1. Clone the repository to your local machine or download the zip file.
2. Ensure the corpus of web pages (HTML files) is organized in a directory.
3. Run the following command:
   ```bash
   python pagerank.py corpus_directory
   ```
   Replace `corpus_directory` with the path to the directory containing the web pages.

### Output
The program will compute and display the PageRank results using both the sampling and iterative methods. Example output:
```plaintext
PageRank Results from Sampling (n = 10000)
  1.html: 0.2223
  2.html: 0.4303
  3.html: 0.2145
  4.html: 0.1329
PageRank Results from Iteration
  1.html: 0.2202
  2.html: 0.4289
  3.html: 0.2202
  4.html: 0.1307
```

## Features
- **Random Surfer Model**: Simulates random page visits based on the damping factor.
- **Iterative Formula**: Computes PageRank until convergence, ensuring stable results.
- Handles pages with no outgoing links by distributing the probability evenly across all pages.

## Core Functions

### `transition_model`
- **Input**: Corpus, current page, damping factor.
- **Output**: A probability distribution over which page to visit next.
- Handles cases where a page has no outgoing links by treating it as linking to all pages.

### `sample_pagerank`
- **Input**: Corpus, damping factor, number of samples.
- **Output**: Estimated PageRank values for each page based on sampling.
- Simulates a random surfer by repeatedly applying the transition model.

### `iterate_pagerank`
- **Input**: Corpus, damping factor.
- **Output**: PageRank values for each page based on iterative computation.
- Repeatedly updates PageRank values until they converge within a threshold of 0.001.

## Notes
- The damping factor (default: 0.85) balances between following links and jumping to random pages.
- Results from both methods should closely align for the same corpus.
- The PageRank values for all pages sum to 1.

## Example Corpus
If the directory contains the following pages:
- `1.html` links to `2.html` and `3.html`
- `2.html` links to `3.html`
- `3.html` links to `1.html` and `4.html`
- `4.html` has no outgoing links

The program will analyze these links to compute the importance of each page.

# Heredity AI Project

## Description
This project implements a Bayesian Network to analyze genetic inheritance and assess the likelihood that a person possesses a specific genetic trait. The model uses probabilistic reasoning to infer distributions over the number of gene copies and whether a trait is expressed for each individual in a dataset.

## How to Use

### Prerequisites
- Python 3.8 or later

### Running the Program
1. Clone the repository to your local machine or download the zip file.
2. Prepare or select a dataset in CSV format that specifies individuals, their parents, and observed traits.
3. Run the program with the following command:
   ```bash
   python heredity.py data/family0.csv
   ```
   Replace `data/family0.csv` with the path to your dataset.

### Output
The program calculates and displays the probabilities for each individual:
- The likelihood of having 0, 1, or 2 copies of the gene.
- The likelihood of exhibiting the trait (True/False).

Example:
```plaintext
Harry:
  Gene:
    2: 0.0092
    1: 0.4557
    0: 0.5351
  Trait:
    True: 0.2665
    False: 0.7335
James:
  Gene:
    2: 0.1976
    1: 0.5106
    0: 0.2918
  Trait:
    True: 1.0000
    False: 0.0000
```

## Features
- **Bayesian Network**: Models genetic inheritance with conditional probabilities.
- **Joint Probability**:
  - Computes the likelihood of a specific configuration of genes and traits.
- **Updating Probabilities**:
  - Adjusts the probability distributions for each individual using new joint probabilities.
- **Normalization**:
  - Ensures all probability distributions sum to 1.

## Core Functions

### `joint_probability`
- **Input**: Dataset, gene sets, and observed traits.
- **Output**: The joint probability of the specified genetic and trait configuration.
- **Details**:
  - Accounts for inheritance probabilities based on parents' genes.
  - Incorporates mutation probabilities and trait likelihoods.

### `update`
- **Input**: Probabilities dictionary, gene sets, trait sets, and joint probability.
- **Output**: Updates the probabilities dictionary.
- **Details**:
  - Adds the joint probability to the gene and trait distributions for each individual.

### `normalize`
- **Input**: Probabilities dictionary.
- **Output**: Normalized probabilities.
- **Details**:
  - Adjusts probabilities so that distributions sum to 1, maintaining relative proportions.

## Dataset Format
The CSV file should have the following columns:
- **name**: Name of the individual.
- **mother**: Name of the individual’s mother (or blank if unknown).
- **father**: Name of the individual’s father (or blank if unknown).
- **trait**: `1` if the trait is present, `0` if absent, or blank if unknown.

Example:
```csv
name,mother,father,trait
Harry,Lily,James,
James,,,1
Lily,,,0
```

## Notes
- The algorithm models gene inheritance probabilities based on parental genes and mutation rates.
- The program handles missing trait data by considering all possibilities and normalizing results.

