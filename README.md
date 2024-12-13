#Hand Gesture Volume Control using Python
This project demonstrates a hand gesture control system for adjusting the volume of your computer using a webcam, MediaPipe, OpenCV, and PyAutoGUI.

The program detects hand gestures in real-time via webcam and uses the distance between the index finger (Landmark 8) and thumb (Landmark 4) to simulate volume control actions. If the distance is large, the volume increases, and if it's small, the volume decreases.

Requirements
* Python 3.x
* OpenCV
* MediaPipe
* PyAutoGUI
* You can install these dependencies via pip.

##Installation
Clone the repository:
  git clone https://github.com/your-username/hand-gesture-volume-control.git
  cd hand-gesture-volume-control

Install the required packages:
  pip install -r requirements.txt
Or install them individually:
  pip install opencv-python mediapipe pyautogui

##Usage
Connect a webcam to your computer.
Run the Python script:
  python hand_gesture_volume_control.py
The program will open a webcam window where it will detect your hand gestures. The index finger and thumb are used to control the volume:
  -When the distance between the index finger and thumb increases, the volume will increase.
  -When the distance between the index finger and thumb decreases, the volume will decrease.
Press Esc to exit the program.

##How it works
  -Hand Detection: MediaPipe's hand tracking model detects landmarks for your hands.
  -Distance Calculation: The script calculates the distance between the index finger (Landmark 8) and the thumb (Landmark 4).
  -Volume Control: Based on the distance, the program simulates the volumeup or volumedown keypress using PyAutoGUI to control the system's volume.
  Code Walkthrough
  -cv2.VideoCapture(0): Captures video from the webcam.
  -mediapipe.solutions.hands: Used to detect hand landmarks in the webcam frame.
  -pyautogui.press(): Simulates the pressing of volume control keys.

##Troubleshooting
  -No webcam detected: Ensure your webcam is properly connected and accessible.
  -Dependencies issues: Double-check if the required libraries are installed correctly.
  -Volume not working: Make sure your system allows for control through key presses for volume up/down.
