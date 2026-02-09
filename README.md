# 🛍️ Retrova
a simple command-line robot controller simulator in python.  
type commands in the terminal to control a robot with rotation-based movement, speed control, and dual grippers.

## Projrect Overview
Retrova is a sustainable thrifting mobile application aimed at reducing over-consumption and promoting circular fashion. The app gives pre-owned clothing a second life by enabling users to buy, swap, and rediscover fashion pieces within a shared community, bridging the gap between past and present styles and transforming vintage items into modern self-expression.

The project emphasizes visual identity, UX/UI design, and brand language, translating the concept of “second life” into color systems, typography, layouts, and interaction flows. It highlights conscious consumption, community exchange, and environmental impact, positioning fashion as an ongoing cycle rather than a disposable trend.

## Requirements
- python 3.6 or higher
- no external dependencies (uses only standard library)

## Project Structure
- robot.py - robot class with movement logic, rotation, grippers, and speed control
- main.py - main control loop and user input handling
- readme.MD - this documentation file

## Commands
commands are case-insensitive.

- F : move forward in the current heading direction
- B : move backward (opposite of current heading)
- N : neutral / stop
- RL : rotate left 90 degrees
- RR : rotate right 90 degrees
- G1 : toggle gripper 1
- G2 : toggle gripper 2
- S<number> : set speed (1-100, e.g., S75)
- Q : quit

## How to Run
```bash
python main.py
```

## How It Works
the robot operates in a 2D grid with a compass heading system:
- heading: The direction the robot is facing (North/East/South/West)
- position: Current coordinates (x, y) on the grid
- forward: Moves in the direction of the current heading
- backward: Moves opposite to the current heading
- rotate: Changes heading by 90° without moving position

## Future Extensions
- make speed actually affect something (movement delay, distance, turn speed)
- add a visual grid display (ASCII art showing robot position)
- add boundaries/obstacles
- save/load robot state
- command history (undo/redo)
- macros (record and replay command sequences)
- add diagonal movement or custom angle rotation
- battery/power system that drains with use
