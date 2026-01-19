# Computer Vision Hand Gesture Projects (OpenCV + MediaPipe)

This repository contains **two real-time hand-gesture based Python projects** using **OpenCV + MediaPipe**:

1. **Air Canvas** – Draw in the air using your index finger  
2. **AI Rock Paper Scissors** – Play Rock Paper Scissors against AI using hand gestures

---

## IMPORTANT: Python Version Requirement

✅ Use **Python 3.12 or 3.13**  
❌ Do **NOT** use **Python 3.14** (it may give compiler/module installation errors)

Recommended:
- Python **3.12.x**
- Python **3.13.x**

---

## Projects Included

### 1) Air Canvas 🎨
Draw on the screen by moving your finger in the air.

**Features**
- Draw using **Index Finger**
- Select color using **Index + Middle Finger**
- Palette Colors:
  - Purple
  - Blue
  - Green
  - Yellow
  - Eraser (Black)
- Keyboard controls:
  - `C` → Clear canvas
  - `Q` → Quit

---

### 2) AI Rock Paper Scissors ✊✋✌
Play Rock Paper Scissors against an AI using hand gestures.

**Features**
- Real-time gesture detection
- AI chooses randomly
- Scoreboard (Player vs AI)
- Timer delay between rounds
- Keyboard control:
  - `Q` → Quit

---

## Requirements

### Hardware
- A working **webcam / laptop camera**

### Python Modules Used
Both projects require:

- `opencv-python`
- `mediapipe`
- `numpy`

Rock Paper Scissors also uses built-in modules:
- `random`
- `time`

---

## Installation & Setup

### 1) Clone the Repository
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
2) Create a Virtual Environment (Recommended)
Windows
bash
Copy code
python -m venv .venv
.venv\Scripts\activate
Mac/Linux
bash
Copy code
python3 -m venv .venv
source .venv/bin/activate
3) Install Required Packages
bash
Copy code
pip install opencv-python mediapipe numpy
(Optional but recommended)

bash
Copy code
pip install --upgrade pip
Run the Projects
▶ Run Air Canvas
bash
Copy code
python air_canvas.py
How to use

Index finger up → Draw

Index + Middle finger up → Select color

Move your finger to the top palette area to change color

Press:

C to clear

Q to quit

▶ Run AI Rock Paper Scissors
bash
Copy code
python rps_ai.py
How to play
Show your hand in front of the camera:

Gesture	Fingers	Move
Fist	All down	ROCK
Open Palm	All up	PAPER
Index + Middle up	2 fingers	SCISSORS

Press Q to quit.

How It Works (Short Explanation)
Air Canvas Working
Captures webcam frames using OpenCV.

Detects hand landmarks using MediaPipe Hands.

Tracks the index finger tip position.

Two modes:

Selection Mode (Index + Middle up): choose color from palette

Draw Mode (Only Index up): draw line on canvas

Canvas is merged with the live camera feed.

Rock Paper Scissors Working
Captures webcam frames.

Detects hand landmarks.

Counts which fingers are up.

Converts gesture into ROCK/PAPER/SCISSORS.

AI chooses randomly.

Winner is decided and score updates.

A short timer starts before the next round.

File Structure
bash
Copy code
.
├── air_canvas.py
├── rps_ai.py
└── README.md
Common Errors & Fixes
Webcam not opening
Close apps using the camera (Zoom/Meet/etc.)

Try changing camera index in code:

python
Copy code
cap = cv2.VideoCapture(1)
mediapipe / opencv install error
Use Python 3.12 or 3.13

Upgrade pip:

bash
Copy code
pip install --upgrade pip
Author
Created by Vaiksy

If you like this project, give it a ⭐ on GitHub!
