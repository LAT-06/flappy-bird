# Flappy Bird Clone

A simple Flappy Bird clone built with Python and Pygame.

## Description

This project is a classic Flappy Bird implementation featuring:
- Procedurally generated pipes.
- Realistic bird physics (gravity and lift).
- Collision detection with pipes and ground.
- Sound effects for flapping and hitting obstacles.
- Start screen and automatic restart.

## Prerequisites

Before running the game, ensure you have Python installed on your system. You will also need the `pygame` library.

### Installation

1. Clone the repository (or download the files).
2. Install the required dependencies using pip:

```bash
pip install -r requirements.txt
```

## How to Run

### Locally

Navigate to the project directory and run the following command:

```bash
python flappy.py
```

### Using Docker

To run the game inside a Docker container (requires an X11 server on the host):

1. **Build the image**:
   ```bash
   docker build -t flappybird .
   ```

2. **Run the container**:
   ```bash
   xhost +local:docker # Allow local connections to X server
   docker run -it --rm \
     -e DISPLAY=$DISPLAY \
     -v /tmp/.X11-unix:/tmp/.X11-unix \
     flappybird
   ```

## Controls

- **Spacebar** or **Up Arrow**: Flap the bird's wings to stay in the air.
- **Close Window**: Exit the game.

## Assets

- Sprites and audio are located in the `assets/` directory.
- Backgrounds, bird animations, and UI elements are handled via Pygame's sprite module.
