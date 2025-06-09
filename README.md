# BreakoutGL - A ModernGL Breakout Game 🕹️

## Description

BreakoutGL is a classic Breakout arcade game implemented in Python. It leverages **ModernGL** for efficient OpenGL rendering and **Pygame** for window creation, event handling, and audio. The project is inspired by tutorials from [LearnOpenGL.com](https://learnopengl.com/) and includes features like multiple levels, power-ups, particle effects, and post-processing shaders.

| Start game | Confuse effect | Chaos effect |
|---|---|---|
|![Breakout demo](README/BreakoutIntro.gif)|![Breakout demo](README/BreakoutConfuse.gif)|![Breakout demo](README/BreakoutChaos.gif)

## Features ✨

* Classic Breakout gameplay mechanics.
* **OpenGL rendering** via ModernGL for hardware acceleration.
* Dynamic **particle effects** for ball movement.
* **Post-processing effects**: Shake, Chaos, and Confuse screen effects.
* **Text rendering** for UI elements (score, lives, messages).
* Multiple **levels** loaded from external `.lvl` files.
* Variety of **Power-ups**:
    * Speed (increases ball speed)
    * Sticky (ball sticks to paddle)
    * Pass-through (ball passes through normal bricks)
    * Pad (increases paddle size)
    * Confuse (visual screen effect)
    * Chaos (visual screen effect)
* **Hard bricks** that reuquires multiple hit to be broken
* **Sound effects** and background music.
* **Resizable game window** with dynamic scaling of game elements.
* Game states: Main Menu, Active Gameplay, and Win Screen.
* Player lives system.
* Embedded GLSL shaders for sprites, particles, text, and post-processing.


## Changelog 📃
* v1.0.1  **Hard bricks** that reuquires multiple hit to be broken



## Dependencies 🛠️

To run BreakoutGL, you'll need Python and the following libraries:

* **pygame:** Used for window management, input events, image/font loading, and audio.
* **moderngl:** A modern Python binding for OpenGL, used for all rendering operations.
* **PyGLM (glm):** A Python implementation of OpenGL Mathematics, used for vector and matrix operations.

---
  
## Installation ⚙️

### From source
1.  **Clone the repository (if you haven't already):**
    ```bash
    git clone https://github.com/g1augusto/breakout 
    cd breakout 
    ```

2.  **Install the dependencies:**
    It's recommended to use a virtual environment.
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    pip install requirements.txt
    ```

### Binaries

In the release section<br>
https://github.com/g1augusto/breakout/releases

---

## How to Run 🚀

Once the dependencies are installed and you are in the project's root directory, execute the main game script:

### From cloned source
```bash
python breakoutgl.py
```

### From compiled binaries
Launch <b>breakout.exe</b> (Windows) or <b>breakout.bin</b> (Linux) 

-----

## Controls 🎮

  * **Left Arrow Key:** Move paddle left.
  * **Right Arrow Key:** Move paddle right.
  * **Spacebar:** Launch the ball from the paddle (when the ball is stuck).
  * **Enter Key:**
      * Start the game from the Main Menu.
      * Proceed to the Main Menu after winning all levels or to retry.

-----

## Project Structure 📂

The game expects certain assets to be present in the same directory as `breakoutgl.py`, or accessible via the paths specified in the code.

```
.
├── breakoutgl.py             # Main game script with embedded shaders
# --- Images / Textures ---
├── awesomeface.png           # Ball texture
├── background.jpg            # Background image
├── block.png                 # Standard brick texture
├── block_solid.png           # Solid brick texture
├── paddle.png                # Paddle texture
├── particle.png              # Particle texture for effects
├── powerup_speed.png         # Speed power-up texture
├── powerup_sticky.png        # Sticky power-up texture
├── powerup_passthrough.png   # Pass-through power-up texture
├── powerup_increase.png      # Pad increase power-up texture
├── powerup_confuse.png       # Confuse effect power-up texture
├── powerup_chaos.png         # Chaos effect power-up texture
├── breakout_window_icon.png  # Window icon
# --- Levels ---
├── one.lvl                   # Level 1 definition file
├── two.lvl                   # Level 2 definition file
├── three.lvl                 # Level 3 definition file
├── four.lvl                  # Level 4 definition file
# --- Audio ---
├── breakout.mp3              # Background music
├── bleep.mp3                 # Sound for breaking a brick
├── solid.wav                 # Sound for hitting a solid brick
├── powerup.wav               # Sound for collecting a power-up
├── bounce.wav                # Sound for ball bouncing off paddle/walls
# --- Fonts ---
├── vastorga.ttf              # Font file for text rendering
└── LICENSE                   # The MIT License file
```

*Level files (`.lvl`) should contain space-separated integers representing brick types, with each line being a row of bricks.*

-----

## Shaders 🎨

The game uses several GLSL shader programs embedded directly within the Python script:

  * **Sprite Shader:** For rendering textured game objects (paddle, ball, bricks, background, power-ups).
  * **Particle Shader:** For rendering and animating particles trailing the ball.
  * **Post-Processing Shader:** For applying full-screen effects like Chaos, Confuse, and Shake.
  * **Text Shader:** For rendering text elements on the screen.

-----

## Acknowledgements 🙏

  * This project's OpenGL concepts and structure are heavily inspired by the invaluable tutorials on [LearnOpenGL.com](https://learnopengl.com/).
  * Uses Pygame, ModernGL, and PyGLM libraries.

-----

## License 📄

This project is licensed under the **MIT License**. See the [LICENSE](https://github.com/g1augusto/breakout?tab=MIT-1-ov-file#MIT-1-ov-file) file for details.

