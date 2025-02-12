# SnakeGame 🐍

A fun, console-based **Snake** game implemented in **C++**! In this game, control a snake that eats food to grow longer and avoid crashing into walls or its own tail. It features multiple difficulty levels and high score tracking.

## Table of Contents 📚

- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Badges](#badges)
- [Data Structure Analysis](#data-structure-analysis)

## Installation 🛠️

### Prerequisites
- A **C++ compiler** (e.g., GCC or Clang)
- **Windows** (for using `_kbhit()` and `_getch()`)
- **Linux/macOS** (alternative key input handling may be required)

### Clone the Repository:
```bash
git clone https://github.com/yourusername/SnakeGame.git
cd SnakeGame

Compile and Run the Game
For Windows:
You can compile the program using MinGW or MSVC:

1.Using MinGW (GCC for Windows):
g++ -o SnakeGame SnakeGame.cpp

Then, run the game:
SnakeGame.exe

2.Using Visual Studio:

Open the project in Visual Studio and build the solution.
Run the SnakeGame.exe from the output directory.

3.For Linux/macOS:
Using GCC:
g++ -o SnakeGame SnakeGame.cpp

Run the game:
clang++ -o SnakeGame SnakeGame.cpp

Then, run:
./SnakeGame

Running the Game
After compiling, you can run the game and enjoy playing!

##Usage 🎮
Game Controls:
W: Move Up
S: Move Down
A: Move Left
D: Move Right
X: Quit the game

Difficulty Levels:
1) Easy
2) Medium
3) Hard
Choose your difficulty at the start, and control the snake to grow longer as you eat the food (denoted by F). The goal is to avoid crashing into walls or your own tail!

Scoring:
You earn 10 points each time the snake eats food.
The game ends if the snake hits the wall or its tail.
The high score is updated whenever you beat your previous best.

Game Over:
When the game ends, you’ll be shown your final score and the high score. You can press R to restart the game or X to exit.

##Contributing 🛠️
We welcome contributions to enhance the game! Follow these steps to contribute:

Fork the repository.
Clone your fork to your local machine.
Create a new branch:
git checkout -b feature-name

Make your changes, test them, and commit them.

Push your changes:
git push origin feature-name

Create a pull request for review.
Feel free to suggest new features or improvements.

##License 📄
This project is licensed under the MIT License. You are free to use, modify, and distribute the code.

##Data Structure Analysis 📊

Key Data Structures:

1.Arrays for Snake's Tail:

tailX[] and tailY[] store the X and Y coordinates of the snake's body segments. These arrays are updated each time the snake moves, and they allow the game to track the snake's body as it grows.

2.Enum for Direction:

The Direction enum represents the four possible directions the snake can move: UP, DOWN, LEFT, and RIGHT. The game uses this enum to control movement.

3.Game State Variables:

x and y: Coordinates of the snake's head.
foodX and foodY: Coordinates of the food item on the grid.
score: The player's current score.
highScore: The highest score achieved.
tailLength: Length of the snake, starting at 3 and increasing when the snake eats food.

4.Game Logic:

The game loop continually updates the snake’s position, checks for collisions (with walls or the snake’s own body), and updates the score. The use of arrays and enums ensures efficient tracking of the snake’s body and direction, while the game state variables allow easy modification and retrieval of the game status.

5.Recursive Food Spawning:

The spawnFood() function ensures that the food does not appear on the snake's body by checking each segment of the snake's tail. If food spawns on the snake, it is relocated.






