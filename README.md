# 👁️ Basic Communication for Paralyzed

**Basic Communication for Paralyzed** is an assistive system using eye movement detection to help non-verbal individuals express basic needs. Built for Raspberry Pi, it tracks eye movements (up, down, left, right) and speaks predefined commands via a connected speaker—enabling simple communication based on gaze direction.

---

## 🔍 Features

- **Eye Movement Detection**: Captures eye position via webcam using OpenCV and facial landmark detection.
- **Direction-to-Command Mapping**: Maps gaze directions (up/down/left/right) to specific voice commands (e.g., “Can you bring water?”).
- **Audio Output**: Uses Raspberry Pi’s audio output (speaker or buzzer) to speak or alert based on gaze.
- **Minimal Interface**: Focuses on simplicity—no buttons or additional interfaces required.

---

## ⚙️ How It Works

1. **Eye Tracking** (`utils.py`, `Main.py`)
   - Detects face and eyes using OpenCV.
   - Determines eye position (left/right/up/down) via landmark ratios.
2. **Command Execution** (`Main.py`)
   - When eyes move in a direction, triggers a corresponding voice/audio command (e.g., `Water.mp3`, `Food.mp3`).
3. **Audio Playback**
   - Plays pre-recorded audio files based on the detected direction.

---

## 🧰 Tech Stack

- **Language**: Python
- **Vision**: OpenCV (face and eye landmarks)
- **Audio**: `pygame` or `os` audio playback
- **Hardware**: Raspberry Pi with webcam + speaker

---

## 🚀 Getting Started

### 📦 Prerequisites

- Raspberry Pi (any model with camera support)
- USB or Pi Camera + speaker/buzzer connected
- Python 3.x

### 🔧 Installation

      ```bash
      git clone https://github.com/Rishikarpe/Basic-communication-for-paralysed.git
      cd Basic-communication-for-paralysed
      pip install opencv-python numpy pygame

##  Usage
    
    ```bash
    python Main.py

- The webcam feed will open in a window.
- Move your eyes in a direction (up/down/left/right).
- The system will play the corresponding audio command.

## Use Cases
- Assisting individuals with quadriplegia or ALS to communicate basic needs
- Low-cost alternative to screen-based AAC systems
- Basis for expanding into Morse-code blinking or full gaze-tracking communication

