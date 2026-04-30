# Pac-Man

A classic arcade-style maze chase game built with vanilla JavaScript.

## Gameplay

- **Objective**: Eat all dots in the maze while avoiding ghosts
- **Controls**: Arrow keys or WASD to move
- **Power Pellets**: Eat the flashing energizers to turn ghosts blue and eat them for bonus points
- **Lives**: Start with 3 lives, earn extra life at 10,000 points

## Ghost Personalities

| Ghost | Color | Behavior |
|-------|-------|----------|
| Blinky | Red | Directly chases Pac-Man |
| Pinky | Pink | Ambushes from ahead |
| Inky | Cyan | Flanks from unpredictable angles |
| Clyde | Orange | Chases when far, flees when close |

## How to Play

1. Open `app/index.html` in a web browser
2. Press **SPACE** to start
3. Use **Arrow Keys** or **WASD** to control Pac-Man
4. Press **P** or **Escape** to pause

## Features

- Authentic maze layout
- 4 unique ghost AI behaviors
- Score tracking with high score persistence
- Level progression with increasing difficulty
- Power pellet system with ghost eating
- Fruit bonus items

## Tech Stack

- HTML5 Canvas
- Vanilla JavaScript
- No external dependencies

## License

MIT License