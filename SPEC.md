# Pac-Man Game Specification

## 1. Project Overview

- **Project Name**: Pac-Man
- **Type**: Action maze chase video game
- **Core Functionality**: Player controls Pac-Man through an enclosed maze, eating dots while avoiding ghosts
- **Target Users**: Casual gamers, retro game enthusiasts

## 2. UI/UX Specification

### Layout Structure

- **Canvas Size**: 448px × 496px (19×21 tile grid, 24px per tile)
- **Game Area**: Centered maze with score display above
- **HUD**: Score (top-left), High Score (top-center), Lives (top-right)

### Visual Design

- **Color Palette**:
  - Background: `#000000` (black)
  - Walls: `#1919A6` (blue)
  - Dots: `#FFB8AE` (peach)
  - Energizers: `#FFB8AE` (peach, flashing)
  - Pac-Man: `#FFD700` (gold)
  - Blinky (Red Ghost): `#FF0000`
  - Pinky (Pink Ghost): `#FFB8FF`
  - Inky (Cyan Ghost): `#00FFFF`
  - Clyde (Orange Ghost): `#FFA500`
  - Blue Ghosts: `#2121DE` (blue, vulnerable)
  - Text: `#FFFFFF` (white)

- **Typography**:
  - Font: `"Press Start 2P"` (Google Fonts) or fallback to monospace
  - Score size: 16px
  - Game over text: 24px

### Visual Effects

- Pac-Man mouth animation (opening/closing)
- Ghost eyes movement
- Blue ghost flashing before recovery
- Power pellet flashing animation
- Death animation (Pac-Man shrinks)
- Screen flash on ghost eat

## 3. Functionality Specification

### Core Features

1. **Player Movement**
   - Arrow key controls (Up, Down, Left, Right)
   - Continuous movement in current direction
   - Can only turn at valid intersections
   - Warp tunnels on left/right edges

2. **Ghost AI Personalities**
   - **Blinky (Red)**: Direct chase - always targets Pac-Man's position
   - **Pinky (Pink)**: Ambush - targets 4 tiles ahead of Pac-Man
   - **Inky (Cyan)**: Flanker - targets between Pac-Man and Blinky
   - **Clyde (Orange)**: Conditional - chases when far, flees when close

3. **Game Mechanics**
   - 240 dots per level (70 normal + 4 energizers)
   - Energizer grants 200 points per ghost eaten
   - Ghost point values: 200, 400, 800, 1600 (combo multiplier)
   - 3 lives to start
   - Extra life at 10,000 points

4. **Power Pellet System**
   - 4 large flashing pellets in maze corners
   - Duration starts at 60 seconds, decreases per level
   - Ghosts turn blue and reverse direction
   - Ghosts flash white before returning to normal
   - Eaten ghosts respawn at center box

5. **Level Progression**
   - Fruit appears after eating 70 dots
   - Fruit bonus: 100, 200, 300, 400... (increases per level)
   - Ghost speed increases each level
   - Power pellet duration decreases
   - Level 256 has kill screen bug

### User Interactions

- **Controls**: Arrow keys or WASD
- **Pause**: Press 'P' or 'Escape'
- **Start Game**: Press Space or Enter
- **Restart**: Press Space after game over

### Edge Cases

- Ghost collision during power mode: ghost eaten, eyes return to center
- All dots eaten: next level, reset positions
- All lives lost: game over, show final score
- Ghosts slower in warp tunnels

## 4. Acceptance Criteria

### Visual Checkpoints

- [ ] Maze renders with blue walls on black background
- [ ] Pac-Man displays with yellow color and animated mouth
- [ ] All 4 ghosts display with distinct colors
- [ ] Dots visible throughout maze
- [ ] 4 energizers flash in maze corners
- [ ] Score displays and updates correctly
- [ ] Lives indicator shows remaining lives

### Functional Checkpoints

- [ ] Pac-Man moves smoothly in 4 directions
- [ ] Pac-Man cannot pass through walls
- [ ] Ghosts move autonomously with unique behaviors
- [ ] Eating dots increases score
- [ ] Eating energizer turns ghosts blue
- [ ] Eating blue ghost grants bonus points
- [ ] Ghost collision when not powered = life lost
- [ ] Level advances when all dots eaten
- [ ] Game over when all lives lost

### Performance

- 60 FPS gameplay
- No input lag
- Smooth ghost movement