# Pinball Jr

A browser-based pinball game built with Matter.js physics engine, featuring custom graphics and realistic pinball mechanics.

## Features

- **Realistic Physics**: Powered by Matter.js for authentic pinball ball movement and collisions
- **Custom Graphics**: Unique pinball table design with custom artwork and sprites
- **Interactive Gameplay**:
  - 5 bumpers (3 top, 2 bottom) with bounce physics
  - Left and right flippers controlled by keyboard or touch
  - Score tracking with current score and high score
  - Ball launch mechanism
  - Multiple collision zones and obstacles
- **Responsive Controls**:
  - Keyboard: Left/Right arrow keys
  - Touch: Tap buttons for mobile play
  - Mouse drag: God mode for testing

## Technologies

- **Matter.js** - 2D physics engine
- **Matter Attractors** - Plugin for paddle mechanics
- **jQuery** - DOM manipulation
- **HTML5 Canvas** - Game rendering

## Project Structure

```
pinball-jr/
├── index.html          # Main HTML entry point
├── css/
│   └── main.css       # Styles and layout
├── js/
│   └── main.js        # Game logic and physics
└── assets/            # Images and sprites
    ├── JRPINBALLFULLTABLE.jpeg
    ├── IMG_5200.PNG
    ├── IMG_5201.PNG
    ├── BOTON2.png
    └── ballv1.png
```

## Game Elements

### Physics Objects

- **Bumpers**: 5 circular bumpers with 1.5x restitution bounce
- **Flippers**: Left and right paddle mechanisms with attractor physics
- **Walls**: Table boundaries, slingshots, and guide rails
- **Ball**: 14-pixel radius sphere with custom sprite texture

### Scoring

- Hit a bumper: +10 points
- High score automatically tracked

### Constants

- Gravity: 0.80 (simulates tilted table)
- Max Velocity: 50
- Bumper Bounce: 1.5
- Paddle Pull: 0.002

## How to Play

1. Open `index.html` in a web browser
2. The ball launches automatically from the shooter lane
3. Use **Left Arrow** or **Left Button** to activate the left flipper
4. Use **Right Arrow** or **Right Button** to activate the right flipper
5. Keep the ball in play and hit bumpers to score points!

## Controls

| Action        | Keyboard        | Touch/Click  |
| ------------- | --------------- | ------------ |
| Left Flipper  | Left Arrow (←)  | Left Button  |
| Right Flipper | Right Arrow (→) | Right Button |
| God Mode      | Mouse Drag      | -            |

## Development

The game uses a modular structure with separate functions for:

- `init()` - Initialize Matter.js engine and world
- `createStaticBodies()` - Build table elements (bumpers, walls, boundaries)
- `createPaddles()` - Set up flipper mechanisms
- `createPinball()` - Create the ball with sprite texture
- `createEvents()` - Handle collisions and user input
- `launchPinball()` - Reset and launch the ball

## Browser Compatibility

Works in modern browsers that support:

- HTML5 Canvas
- ES6 JavaScript
- Matter.js

## Credits

Built with Matter.js physics engine and custom artwork.
