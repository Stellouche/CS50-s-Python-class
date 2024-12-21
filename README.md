# CS50-s-Python-class
CS50’s Introduction to Artificial Intelligence with Python

# Degrees Project

## Description
The Degrees Project is an implementation of a search algorithm to determine the "degrees of separation" between two actors in the Hollywood film industry. Inspired by the "Six Degrees of Kevin Bacon" game, this program finds the shortest path of connections between two actors based on movies they have starred in together.

## How to Use
1. Clone the repository to your local machine.
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

