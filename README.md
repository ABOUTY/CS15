# CS15
https://hackmd.io/@Fall2024-CS15/HJ5yLrAs0
## Functionality
Overview
Pacman is played on a 23 x 23 grid organized into a maze. The user controls Pacman’s direction of movement with the keyboard (see Controlling Pacman for more details). The goal is to eat all of the white dots while avoiding the four ghosts (Blinky, Pinky, Inky, and Clyde) who chase after Pacman.

## Initial Setup
Your board should be initially set up as shown in the image below with: Pacman in his starting square, one ghost outside of the ghost pen, and the rest of the ghosts inside the ghost pen. There are also dots and energizers on the board. Each wall, dot, energizer, ghost, and Pacman himself are initially positioned in a single square in the 23x23 grid.

You must also keep track of Pacman’s score and remaining lives. This information should be clearly visible on the screen at all times. Pacman will start with 3 lives and 0 points. The game should also have a quit button. Please note that the countdown in the demo until the game starts is extra-credit and is not mandatory.

## Initial State of the Board
Gameplay
If Pacman collides with any of the ghosts, he should lose one life. Additionally, the ghosts should be returned to the pen, and Pacman’s location should be reset to the original starting location. If Pacman collides with a dot or energizer, the dot or energizer should disappear from the board, and the game score should be updated accordingly. Finally, every time an energizer is eaten, the ghosts should be set to frightened mode (read about this below) for a short time.

## Ghosts
When in Scatter or Chase Mode, the ghosts move according to a breadth-first-search algorithm, which is outlined in the Ghost Behavior section. In these modes, when Pacman collides with a ghost, the game resets and he loses a life.

In Frightened Mode, the ghosts’ behavior changes and Pacman is able to eat them. The ghosts should all simultaneously change their color to blue when frightened mode begins and revert to their original colors when frightened mode ends. They don’t need to blink like they do in the demo, but they must change color to blue. When a ghost is eaten, it disappears and reappears in the ghost pen. The ghost pen periodically releases ghosts to the free square just above the pen.

## Scoring
Whenever Pacman eats a dot, energizer, or ghost, the game score should be updated as follows:

Dot: +10 points
Energizer: +100 points
Ghost: +200 points
Winning and Losing
The game ends either when all of the dots and energizers are eaten or when Pacman loses all of his lives. When the game ends, the ghosts and Pacman should all stop moving, and keyboard input should be disabled.


![image](https://github.com/user-attachments/assets/a4b32b00-9acf-49cc-9bd6-97659e6afe2a)
