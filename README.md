# Snake Game

This is a classic Snake Game implemented in C++, where the player controls a snake to eat food and grow longer. The game includes features like customizable difficulty levels, a scoreboard for tracking the highest scores, and intuitive console-based gameplay.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Compiling for Different Operating Systems](#compiling-for-different-operating-systems)
- [Contributing](#contributing)
- [License](#license)
- [Data Structure Analysis](#data-structure-analysis)
- [Features](#features)
- [Badges](#badges)
- [Screenshots](#screenshots)
- [Conclusion](#conclusion)

## Installation

To get started with the Snake Game, follow these steps:

### 1. Clone the Repository:
```bash
git clone https://github.com/yourusername/snake-game.git

2. Navigate to the Project Directory:
cd snake-game

3. Install a C++ Compiler:
Ensure you have a C++ compiler installed. On most systems, g++ is the default C++ compiler.

Usage
Once you've compiled the game, you can start playing the game via the terminal/command prompt.

Start the Game: Once the game is compiled, you can run the executable.
Controls: Use W, A, S, and D to move the snake. Press X to quit the game.
Difficulty: Choose between Easy, Medium, or Hard difficulty levels.
Score: Your score will increase as you eat food, and the snake grows longer. The high score will be displayed at the end of each game session.
Compiling for Different Operating Systems
For Windows:
Install MinGW (for GCC): You can download and install MinGW from here.
Compile the Code: Open the Command Prompt in your project directory and run:
bash
Copy
Edit
g++ -o snake_game main.cpp
Run the Game:

snake_game.exe
For macOS and Linux:
Install g++:
macOS: Use Homebrew to install GCC:

brew install gcc
Linux: Install g++ using the following command:
sudo apt install g++
Compile the Code:
bash
Copy
Edit
g++ -o snake_game main.cpp
Run the Game:
bash
Copy
Edit
./snake_game
Contributing
We welcome contributions! Here's how you can get involved:

Fork the repository.
Create a new branch:
bash
Copy
Edit
git checkout -b feature-name
Make your changes.
Commit your changes:

git commit -m "Added a new feature"
Push your branch:
bash
Copy
Edit
git push origin feature-name
Create a pull request.
We appreciate your contributions!

License
This project is licensed under the MIT License.

Data Structure Analysis
Data Structures Used:
Arrays:

tailX[] and tailY[]: Arrays are used to store the x and y coordinates of each segment of the snake’s body. As the snake grows, new body segments are added to these arrays, tracking the position of each segment.
These arrays are dynamically updated every time the snake moves to a new position.
Enum:

Direction Enum: The direction of the snake is managed using an enumeration to ensure clarity and type safety. The enum contains values for each of the four possible directions: UP, DOWN, LEFT, RIGHT, and STOP (which is used when the game ends).
This makes it easy to check the direction and prevent the snake from moving in the opposite direction.
Static Variables:

highscore: This static variable tracks the highest score achieved in the game. It is updated each time the player finishes a game.
score: Tracks the current score of the game, which increments as the snake eats food and grows in size.
Primitives:

x and y: These variables track the position of the snake’s head.
gameOver: A flag that indicates whether the game is over. It is set to true when the snake collides with the wall or itself.
Object Structure:
The game logic revolves around the snake's movement, and the key objects involved are:
The Snake: Represented by the coordinates stored in arrays (tailX[], tailY[]) and controlled by the Direction enum.
Food: Randomly placed on the game grid, and when the snake eats it, the score increases and the snake grows longer.
Game Over Condition: If the snake's head collides with the boundaries of the game area or its own body, the game ends.
Game Loop:
Movement: The game updates the position of the snake based on the direction. If a segment of the snake collides with another segment or the wall, the game ends.
Growth: As the snake eats food, a new segment is added to the snake’s body, and the game continues until the snake dies.
Features
Customizable Snake Design: Choose different characters for the snake’s head and body.
Difficulty Levels: Adjust the speed of the snake for an easy, medium, or hard challenge.
Score Tracking: Keep track of your current score and the highest score achieved.
Console-based Gameplay: Play the game directly in the terminal or command prompt.













 



