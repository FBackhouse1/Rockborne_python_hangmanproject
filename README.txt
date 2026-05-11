# Hangman Project

A simple command-line Hangman game written in Python. The game lets the user choose a word category, randomly selects a hidden word, and asks the user to guess letters until they either reveal the full word or run out of lives.

## Project Overview

This project was built as part of a Python programming assignment. It demonstrates core beginner Python concepts including:

- Variables and global session tracking
- Dictionaries and lists
- Functions
- Loops and conditional statements
- User input validation
- Random word selection
- Basic game logic

## Features

- Category-based word selection
- Three available categories:
  - Animals
  - Geography
  - Coding
- Random word selection using Python's `random` module
- Five lives per game
- Repeated-guess detection
- Hidden-word display using underscores
- Session statistics showing wins, games played, and win rate
- A loop safety counter to help prevent infinite gameplay loops

## Files

```text
Hangman_project.ipynb    # Main Jupyter Notebook containing the game code
README.md               # Project documentation
```

## How to Run

### Option 1: Run in Jupyter Notebook

1. Open `Hangman_project.ipynb` in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.
2. Run the cells from top to bottom.
3. When prompted, select a category by entering its number.
4. Guess one letter at a time until you win or lose.

### Option 2: Run as a Python Script

You can copy the code from the notebook into a `.py` file, for example:

```text
hangman.py
```

Then run:

```bash
python hangman.py
```


## Main Functions

### `get_user_category()`

Displays the category menu and repeatedly asks the user to choose a valid category number.

### `initialize_word(category_name)`

Selects a random word from the chosen category and creates:

- A list version of the hidden word
- A visual list of underscores
- The original word as a string

### `play_hangman()`

Runs the main game loop. It manages user guesses, checks whether guesses are correct, updates the visual display, subtracts lives for incorrect guesses, detects wins and losses, and updates session statistics.

## Example Gameplay

```text
--- SELECT A CATEGORY ---
1. Animals
2. Geography
3. Coding

Enter number (1-3): 3
_ _ _ _ _ _
Please enter a letter: p
p _ _ _ _ _
Please enter a letter: z
p _ _ _ _ _
Incorrect. Minus one life. Remaining lives = 4
```

## Requirements

The project only uses Python's built-in libraries.

```python
import random
```

No external packages are required.

## Possible Improvements

Future improvements could include:

- Stronger input validation using `guess.isalpha()`
- Option to replay without rerunning the notebook
- Difficulty levels
- More word categories
- ASCII art for the Hangman figure
- Saving scores between sessions
- Converting the notebook into a standalone Python script

## Author

Fenner Backhouse
