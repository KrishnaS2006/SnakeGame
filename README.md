##Snake Game
A console-based Snake Game where players control a snake that grows longer as it eats food while avoiding walls and its own tail. The game allows customization of the snake's appearance and supports different difficulty levels, making it fun and challenging. The game also tracks scores and high scores.

Table of Contents
Installation
Usage
Contributing
License
Data Structure Analysis


##Installation
To get the Snake Game up and running on your local machine, follow these steps:

1. Clone the Repository:
git clone https://github.com/yourusername/snake-game.git


2. Compile and Run the Code:
Since this project is written in C++, you will need a C++ compiler to compile and run the code.


g++ -o snake_game main.cpp
./snake_game
Ensure that you have a C++ compiler like g++ installed on your system.

##Usage
Once you've compiled the code, follow these steps to run the game:

After running the program, you'll be prompted to design your snake by choosing characters for the head and body.
Then, you'll select a difficulty level (Easy, Medium, or Hard).
The game uses the following controls:
W: Move Up
S: Move Down
A: Move Left
D: Move Right
X: Quit the game
When the game ends, the final score and high score will be displayed. You can choose to play again by pressing 'p' or exit by pressing 'x'.

##Contributing
We encourage contributions to make this game even better. Here’s how you can contribute:

Fork the repository.
Create a new branch: git checkout -b feature-name.
Make your changes.
Commit your changes: git commit -m 'Add new feature'.
Push to your branch: git push origin feature-name.
Create a pull request.
We welcome improvements, bug fixes, and new features!

##License
This project is licensed under the MIT License.

##Data Structure Analysis
Overview of Data Structures Used
The Snake Game utilizes a combination of arrays, enums, and simple data types to manage the state of the game and implement its logic.

##Data Structures:
Arrays:

tailX[] and tailY[]: These arrays are used to store the x and y coordinates of the snake's tail (body). These arrays are updated every time the snake moves, helping track the body segments and allowing collision detection with the body.
Example: tailX[i] and tailY[i] represent the position of the i-th segment of the snake's body.
The size of these arrays is fixed at 100, meaning the snake can grow up to 100 body segments.
Enum:

Direction: An enum used to represent the possible movement directions of the snake. It has values STOP, UP, DOWN, LEFT, and RIGHT. This enum is crucial for controlling snake movement and preventing invalid directions (e.g., preventing the snake from moving in the opposite direction).
Example: Direction dir = UP; sets the direction of the snake to "up".
Static Variable:

highscore: A static variable used to track the highest score achieved across game sessions. This allows the game to display the high score at the end of each session.
Simple Integer and Boolean Variables:

score: Keeps track of the current score.
gameOver: A boolean flag used to indicate whether the game has ended.
tailLength: Tracks the length of the snake's body.
x and y: Represent the current coordinates of the snake’s head.
foodX and foodY: Coordinates of the food item in the game.
These variables are essential for game logic, such as checking collisions and updating the game state.
How Data Structures Are Used



Movement: The snake moves based on the direction specified by the Direction enum. The snake’s movement is updated in the logic() method, where the position of the head and the body are adjusted, and the body segments are shifted to follow the head’s movement.

Tail Tracking: The tailX[] and tailY[] arrays store the positions of the tail segments. Every time the snake moves, the tail segments move one step forward, and the head position is updated based on user input.

Food Spawning: The spawnFood() function places food randomly on the grid, ensuring it doesn't spawn on the snake's body. This is done by checking if the random food coordinates coincide with any segment of the snake's tail.

Collision Detection: The game checks for collisions with walls or the snake's own body. If the snake's head coordinates (x, y) match the food coordinates (foodX, foodY), the score is increased, and the snake’s length is extended. If the snake's head collides with its body or the wall, the game ends.

Game State: The game’s state is represented using simple flags like gameOver, which is checked in the game loop. If the game ends (either due to wall collision or body collision), the game stops and the final score is displayed.

Object-Oriented Structure
The main game logic is encapsulated within the SnakeGame class. The SnakeGame object holds all of the game’s state and behavior, including:


Initialization: The resetGame() method initializes the game state.
Movement and Logic: The input() and logic() methods handle user input and game state updates.
Drawing: The draw() method is responsible for rendering the game state to the console, displaying the snake, food, and score.
Game Loop: The main loop of the game repeatedly calls the input(), logic(), and draw() methods until the game ends.



Summary of Data Structures
Arrays (tailX[], tailY[]): These arrays are used to store the positions of the snake's tail and are crucial for movement and collision detection.
Enum (Direction): Provides an easy way to represent movement directions and avoid invalid moves.
Static Variable (highscore): Tracks the highest score across sessions.
Integer and Boolean Variables: Used to track game state (e.g., score, gameOver flag, and snake size).
Class Encapsulation: The SnakeGame class encapsulates all of the game logic, making the code modular and easy to maintain.
This Snake Game is a fun and interactive project that leverages simple data structures and object-oriented principles to create an engaging user experience. Contributions are welcome, and feel free to customize and improve the game further!








 



