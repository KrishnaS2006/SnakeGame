# Snake Game in C++

A simple and customizable Snake game built in C++. Control the snake, eat food, and avoid walls and your own tail. The game includes difficulty levels, a high score tracker, and customizable snake design (head and body).

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Additional Sections](#additional-sections)
- [Data Structure Analysis](#data-structure-analysis)

## Installation

Follow the instructions below to install and run the Snake Game on your local machine.

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/snake-game.git

2. Install dependencies (if any):

The project does not require additional dependencies. However, you must have a C++ compiler installed (e.g., g++).


3.Compile the game:

On Linux/macOS:
g++ snake_game.cpp -o snake_game

On Windows (using MinGW or other C++ compilers):
g++ snake_game.cpp -o snake_game.exe

4.Run the game:

On Linux/macOS:
./snake_game

On Windows:
snake_game.exe

##Usage
1.How to Play
Customize your Snake: At the start of the game, you will be prompted to choose the character for the snake's head and body.

Head: Enter any character (e.g., @, O, etc.).
Body: Enter any character (e.g., #, *, etc.).

2.Choose the Difficulty: After customizing your snake, you will be prompted to select a difficulty:

Easy (a): Slow game speed.
Medium (b): Moderate game speed.
Hard (c): Fast game speed.


3.Control the Snake:

Use the following keys to move the snake:
W or UP Arrow: Move up
S or DOWN Arrow: Move down
A or LEFT Arrow: Move left
D or RIGHT Arrow: Move right
Press X to quit the game anytime.


4.Game Over:

The game ends if the snake collides with the wall or its own tail.
The final score and high score will be displayed after the game ends.

5.Restart or Exit:

After the game ends, press P to play again or X to exit.

##Contributing
We welcome contributions! If you would like to improve the game or add new features, please follow these steps:

1.Fork the repository.
2.Create a new branch: git checkout -b feature-name.
3.Make your changes.
4.Push your branch: git push origin feature-name.
5.Create a pull request.

##License
This project is licensed under the MIT License.

##Additional Sections
Features
1.Custom Snake Design: Choose the appearance of your snake's head and body.
2.Three Difficulty Levels: Easy, Medium, and Hard.
3.High Score Tracking: Keeps track of the highest score achieved across sessions.
4.Cross-Platform: Works on both Windows and UNIX-based systems (Linux/macOS).

FAQ
1.How do I quit the game?
Press X during gameplay to exit.

2.Can I add more features?
Yes! You can modify the code to add new features like power-ups or multiplayer modes.
Feel free to contribute or open issues if you'd like to add more features or report bugs!


##Data Structure Analysis

Overview
In this Snake game, several data structures are utilized to manage and track the game’s state, including the snake, its movement, food position, and user input. Let's go through the key data structures used in the game and explain how they are organized.

1. Snake Body Representation:
The snake's body is represented using two arrays:

Arrays for X and Y Coordinates:

int tailX[100]: An array storing the X-coordinates of each part of the snake's body (including the head).
int tailY[100]: An array storing the Y-coordinates of each part of the snake's body (including the head).
These arrays represent each segment of the snake’s body, starting from the head at index 0 and extending to the tail.

Array Size and Length:
The snake's length is tracked with the tailLength variable, which defines how many segments (or body parts) the snake currently has.
Initially, the snake starts with a tail length of 3 but increases as the snake eats food.


2. Snake Movement and Direction:
The direction of movement is controlled by an enum type:

enum Direction { STOP = 0, UP, DOWN, LEFT, RIGHT };
This enum allows us to easily represent the direction the snake is moving in (UP, DOWN, LEFT, RIGHT), and STOP is used to initialize the direction when the game starts.


3. Food Position:
The position of the food is tracked by two variables:

int foodX: Stores the X-coordinate of the food.
int foodY: Stores the Y-coordinate of the food.
When the snake eats the food, a new food item is randomly generated at a different position using the spawnFood() function.

4. Game State Management:
Boolean Flags:

bool gameOver: A boolean flag that indicates if the game is over or not.
bool isGameOver(): Returns the game state (whether the game has ended).
Score Management:

int score: Tracks the current score based on the number of food items eaten by the snake.
static int highscore: A static variable that stores the highest score across multiple game sessions.


5. User Input:
To capture the user input (for controlling the snake's movement), the program uses the _kbhit() and _getch() functions. These functions allow non-blocking key input (without waiting for the user to press Enter), ensuring smooth gameplay.

Summary of Data Structure Usage:
Arrays (tailX[], tailY[]): These are used to represent the snake's body segments in both X and Y coordinates. The arrays are large enough to accommodate up to 100 body segments.

Enums (Direction): An enum is used to manage the movement directions and ensure that the snake doesn't reverse into itself.

Variables (foodX, foodY, score, highscore): These variables are used to track game state, the food's position, the score, and the highest score.

This structured approach allows easy management of the game's logic and ensures that the game behaves as expected while providing efficient tracking of the snake's state and food position.


### Explanation of Data Structures:

- **Arrays (`tailX[]`, `tailY[]`)**: The two arrays (`tailX` and `tailY`) are used to store the coordinates of each part of the snake's body. This is necessary for tracking the movement of the snake and checking for collisions.
- **Enum (`Direction`)**: The `Direction` enum makes the code cleaner by using descriptive values (UP, DOWN, LEFT, RIGHT) instead of numeric values. It helps manage the snake's movement in a readable way.
- **Boolean (`gameOver`)**: Used to flag the game state (whether the game is over or not).
- **Score Tracking**: The `score` and `highscore` variables help keep track of the player’s progress.

This section will help users understand how the game’s data is structured and how each piece of information is efficiently handled using appropriate data structures.











