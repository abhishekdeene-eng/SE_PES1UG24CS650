# Software Engineering Lab 4 – Vibe Coding

## Fruit Ninja – Python/Pygame

**Student:** Abhishek  
**SRN:** PES1UG24CS650  
**Course:** Software Engineering Lab 4  
**Project:** Fruit Ninja  
**Technologies:** Python, Pygame, Git, GitHub

---

## 1. Project Overview

This project is a Fruit Ninja–style game developed using Python and Pygame as part of Software Engineering Lab 4 – Vibe Coding.

The original starter project was enhanced through four tasks to improve gameplay, user experience, and functionality.

### Tasks Implemented

1. Improve fast-swipe collision detection.
2. Implement a Game Over screen.
3. Add replay functionality and difficulty levels.
4. Add sound effects for gameplay events.

Each task was developed and tested as part of the project workflow.

---

## 2. Objectives

- Improve fruit slicing during fast mouse movements.
- Display a Game Over screen when the round ends.
- Show the final score and replay instructions.
- Provide Easy, Medium, and Hard difficulty levels.
- Allow players to start a new round without restarting the application.
- Add sound effects for fruit slicing and bomb collisions.
- Practise debugging, iterative development, and version control using Git and GitHub.

---

## 3. Technologies Used

- **Programming Language:** Python
- **Game Framework:** Pygame
- **Version Control:** Git
- **Repository Hosting:** GitHub
- **Code Editor:** Visual Studio Code

---

## 4. Tasks Implemented

### Task 1 – Fast-Swipe Collision Detection

**Objective:** Improve collision detection so that fruit is less likely to be missed during fast mouse swipes.

**Implementation:**

- Checks the line segment between the previous and current mouse positions.
- Samples intermediate points along the swipe.
- Checks the sampled points against fruit hitboxes.
- Uses the existing fruit-slicing logic when a collision is detected.

**Result:** Fast mouse movements can detect fruit collisions more reliably.

**Git commit message:** `Fix fast-swipe collision detection`

### Task 2 – Game Over Screen

**Objective:** Display a clear Game Over screen when the player loses.

**Implementation:**

- Displays a Game Over title.
- Adds a translucent overlay over the game screen.
- Displays the final score.
- Shows instructions for selecting a difficulty and replaying.

**Result:** Players receive clear feedback when a round ends and can see how to start another round.

**Git commit message:** `Add Game Over screen`

### Task 3 – Replay and Difficulty Levels

**Objective:** Allow players to replay the game and choose different difficulty levels.

**Implementation:**

Three difficulty levels are available:

| Difficulty | Spawn Interval | Speed Scale | Bomb Probability |
|---|---:|---:|---:|
| Easy | 70 | 0.8 | 8% |
| Medium | 55 | 1.0 | 15% |
| Hard | 40 | 1.2 | 25% |

The Game Over screen supports the following keyboard controls:

- **E** – Start a new Easy round.
- **M** – Start a new Medium round.
- **H** – Start a new Hard round.

The reset functionality clears the previous round's fruits and swipe trail, resets the score and lives, and applies the selected difficulty.

**Result:** Players can replay the game with different difficulty settings without restarting the application.

**Git commit message:** `Add replay and difficulty levels`

### Task 4 – Sound Effects

**Objective:** Add audio feedback for important gameplay events without requiring separate external sound files.

**Implementation:**

- Generates sound effects in memory using Python and Pygame.
- Plays a higher-pitched sound when fruit is sliced.
- Plays a lower-pitched sound when a bomb is hit.
- Reuses the bomb sound when the player loses all lives.
- Handles sound initialization errors so that unavailable audio does not unnecessarily stop the game.

The sound setup and playback logic are implemented in `game/game_engine.py`.

**Result:** The game provides audio feedback for fruit slicing, bomb collisions, and losing all lives.

**Git commit message:** `Add sound effects`

---

## 5. Final Features

The completed project includes:

- Improved fast-swipe collision detection.
- Fruit slicing and bomb collision handling.
- Game Over screen with final score.
- Replay functionality.
- Easy, Medium, and Hard difficulty levels.
- Difficulty-dependent spawning, speed, and bomb probability.
- Generated sound effects for gameplay events.
- Git version control for tracking development changes.

---

## 6. Project Structure

```text
41_fruit-ninja/
├── game/
│   ├── game_engine.py
│   └── fruit.py
├── .gitignore
├── main.py
├── requirements.txt
├── README.md
├── before.mp4
├── After.mp4
└── Fruit_Ninja_Code_Change_Chat_History.pdf
```

The `game` directory contains the game engine and fruit-related logic. The `main.py` file launches the game, while `requirements.txt` lists the required Python dependencies.

The repository may contain additional files as part of the starter project.

---

## 7. How to Run the Project

### Step 1 – Clone the Repository

```bash
git clone https://github.com/SETAPESU26/41_fruit-ninja.git
```

Alternatively, download the repository and open the project folder in Visual Studio Code.

### Step 2 – Open the Project Directory

```bash
cd 41_fruit-ninja
```

### Step 3 – Install Dependencies

```bash
pip install -r requirements.txt
```

If Pygame is not included in the installed dependencies, install it using:

```bash
pip install pygame
```

### Step 4 – Run the Game

```bash
python main.py
```

---

## 8. Testing

The following features should be verified during testing:

- **Collision detection:** Test slow and fast mouse swipes across fruit.
- **Game Over screen:** Verify that the screen appears after a bomb collision or when all lives are lost.
- **Final score:** Confirm that the final score is displayed.
- **Replay:** Test starting a new round using E, M, and H.
- **Difficulty levels:** Verify that Easy, Medium, and Hard use their respective settings.
- **Sound effects:** Test the sounds for fruit slicing, bomb collisions, and losing all lives.
- **Integration:** Verify that the features work together.

---

## 9. Before and After Demonstration

### Before Implementation

The original project is demonstrated in `before.mp4`.

### After Implementation

The updated project is demonstrated in `After.mp4`.

These videos are included in the repository for comparison between the starter version and the enhanced game.

---

## 10. Git Version Control

Git was used to track the implementation of the four tasks. The changes were organised into separate commits.

| Task | Commit Message |
|---|---|
| Task 1 | `Fix fast-swipe collision detection` |
| Task 2 | `Add Game Over screen` |
| Task 3 | `Add replay and difficulty levels` |
| Task 4 | `Add sound effects` |

The project and its submission files are maintained in the personal GitHub repository.

---

## 11. Development Workflow

1. Start with the provided Fruit Ninja project.
2. Improve fast-swipe collision detection.
3. Test the collision changes and commit them.
4. Implement the Game Over screen.
5. Test the end-of-round behaviour and commit the changes.
6. Add replay and difficulty selection.
7. Test the difficulty settings and reset behaviour.
8. Add sound effects and test audio playback.
9. Perform final integration testing.
10. Maintain the project files and documentation in GitHub.

---

## 12. Lab 4 Deliverables

The repository contains the project files and supporting submission materials:

1. Updated Fruit Ninja source code.
2. Before implementation video.
3. After implementation video.
4. Vibe Coding prompt documentation.
5. Code-change chat history PDF.
6. Git commits for the implemented tasks.

---

## 13. Conclusion

The Fruit Ninja project was enhanced through four Vibe Coding tasks: improving fast-swipe collision detection, implementing a Game Over screen, adding replay and difficulty selection, and introducing sound effects.

These improvements make the game more responsive and engaging while providing an opportunity to practise Python programming, debugging, testing, and Git-based version control.

**Software Engineering Lab 4 – Vibe Coding: Fruit Ninja**
