# FinalTanks – Java 2D Tank Shooter Game (Swing + AWT)

FinalTanks is a 2D tank-shooter game built in Java using Swing, AWT, and Java’s concurrency utilities. It features real-time rendering, keyboard/mouse controls, moving enemies, and physics-based projectile shooting.
This game was built as part of a university assignment and functions as a proof-of-concept demo for 2D game programming, graphics rendering, and event-driven input in Java.



## Features
 ### 🎮 Gameplay

- Player-controlled tank with:

  - Keyboard movement (arrow keys)
  - Mouse-aimed turret rotation
  - Left-click shooting
  - Right-click to switch turret mode
- Enemies with basic AI movement (patrol behavior)
- Collision detection between bullets and enemies
- Game-over state handling
- Real-time FPS-based game loop (fixed update and render rate)

### 🎨 Graphics

- Fully rendered with Swing + AWT (Graphics2D)
- Triple-buffered rendering using BufferStrategy
- Image-based sprites:
  - Tank body
  - Tank gun (two modes)
  - Enemy tank
  - Bullet

### ⚙️ Architecture
- OOP design with dedicated controllers:
- GameState – stores and updates game logic
- GameLoop – main loop (update + render)
- GameFrame – rendering surface and asset loading
- BulletController, EnemyController – entity managers
- Event-driven input system:
  - Custom KeyHandler
  - Custom MouseHandler
### 🚀 Performance
- Custom game loop running at 30 FPS
- ExecutorService (CachedThreadPool) for threaded gameplay
- Minimal input latency (mouse + keyboard)


## 🧠 Concepts Demonstrated

This project showcases several important software-engineering and game-development concepts:

### 🎯 Core Java Skills

- Java SE
- OOP (Encapsulation, Composition, MVC-like game structure)
- Custom event handling (keyboard & mouse)

### 🎨 Graphics & Animation
- Graphics2D rendering
- Rotation transformations
- Image sprite drawing
- Implementing a triple-buffered renderer with BufferStrategy

### 🕹️ Game Development Concepts

- Game loops
- Entity controllers
- Collision detection
- Player input processing
- AI movement patterns
- Angle calculations for aiming (atan, sin, cos)

### ⚙️ Multithreading & Concurrency

- Using ExecutorService for running the game loop
- Thread-safe design for rendering and updating
- Understanding of timing and scheduling (FPS control)

### 📁 Software Design Practices

- Modular structure (controllers, model, rendering separated)
- Sprite resource loading
- Real-time state management

### 📁 Project Structure
```text
src/
 ├── Main.java
 ├── GameFrame.java         # Window + rendering + assets
 ├── GameLoop.java          # Main loop (update/render)
 ├── GameState.java         # Game logic & input state
 ├── Bullet.java
 ├── BulletController.java
 ├── Enemy.java
 ├── EnemyController.java
 ├── ThreadPool.java
 └── Resources/
      └── Images/
           ├── tank.png
           ├── tankGun01.png
           ├── Enemy1.png
           ├── Enemy2.png
           └── ...
```

## How to Run

Install Java 8+
Clone repo
Ensure Resources/Images folder exists in the root directory
Compile and run:
```bash
javac src/*.java
java -cp src Main
```        


## 📚 Project Origin

FinalTanks was originally developed as a university project to explore the fundamentals of 2D game development in Java.
It serves as a proof of concept demonstrating real-time rendering, basic game physics, input handling, and multithreading.
While not intended as a full commercial game, it showcases core software-engineering and game-loop mechanics using Java Swing, AWT, and concurrency utilities.
