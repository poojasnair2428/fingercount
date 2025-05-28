# ✋ Finger Count (OpenCV + MediaPipe)

This is my **first OpenCV project**, where I built a simple real-time **finger counting application** using OpenCV and MediaPipe. The program captures video from a webcam, detects one hand, and counts the number of fingers raised.

## 🚀 Features

* Real-time hand tracking using **MediaPipe**
* Finger count detection for up to 5 fingers
* Overlay of finger count on the webcam feed
* Press `'q'` to quit the app

## 🛠 Technologies Used

* Python 🐍
* OpenCV 🎥
* MediaPipe 🖐️

## 📦 Installation

1. Clone the repository or copy the code:

   ```bash
   git clone https://github.com/your-username/finger-count.git
   cd finger-count
   ```

2. Install the required libraries:

   ```bash
   pip install opencv-python mediapipe
   ```

3. Run the script:

   ```bash
   python finger_count.py
   ```

## 📸 How It Works

* MediaPipe detects 21 landmarks on the hand.
* The script compares landmark positions to determine if each finger is "up" or "down".
* The thumb is detected using horizontal (x) coordinates.
* Other fingers are detected using vertical (y) coordinates.

## 📷 Screenshot

![Finger Count Demo]("C:\Users\hp\OneDrive\Pictures\Screenshots\u.png")

> Replace with an actual screenshot of your app if available.

## 🧠 Logic Summary

| Finger | Logic                           |
| ------ | ------------------------------- |
| Thumb  | `lmlist[4][1] < lmlist[2][1]`   |
| Index  | `lmlist[8][2] < lmlist[6][2]`   |
| Middle | `lmlist[12][2] < lmlist[10][2]` |
| Ring   | `lmlist[16][2] < lmlist[14][2]` |
| Pinky  | `lmlist[20][2] < lmlist[18][2]` |

## 🙋‍♀️ Why I Built This

This is my **first OpenCV project**, and I wanted to explore the basics of computer vision and hand tracking. It was a great way to get hands-on with MediaPipe and understand coordinate systems in vision application.
