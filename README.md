# 🟨 Real-Time Yellow Object Tracking Using OpenCV

[![OpenCV](https://img.shields.io/badge/OpenCV-5.0+-orange)](https://opencv.org/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue)](https://python.org)

This project tracks **yellow-colored objects** in real-time using your webcam. It detects yellow hues in HSV color space and follows them as they move, drawing a dynamic green bounding box that updates with the object's motion.

![Yellow Object Detection](./Demo.gif)

---

## 🛠️ Tech Stack

- **Python 3.8+**
- **OpenCV** - for video capture and color processing
- **NumPy** - for numerical operations
- **Pillow (PIL)** - for bounding box calculations

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- Webcam
- Basic Python environment set up

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/yellow-object-tracking.git
   cd yellow-object-tracking
   ```
2. Install dependencies:
    ```bash
    pip install opencv-python numpy pillow
    ```
3. Run the program:
    ```bash
    python main.py
    ```
4. Interaction
    - Hold a yellow object in front of your webcam
    - Move the object to see real-time tracking
    - Press Q to quit the application

---

## 🧠 How It Works

1. Captures frames from your webcam (`cv2.VideoCapture`).
2. Converts frames from BGR to HSV color space.
3. Applies a mask to isolate yellow pixels using dynamic thresholds.
4. Uses Pillow to calculate the bounding box around the detected yellow area.
5. Continuously updates and **tracks the yellow object** as it moves in the frame.

---

## 📁 File Structure

```plaintext
.
├── main.py          # Main script that captures webcam input and tracks yellow objects
├── util.py          # Helper module to compute HSV limits for a given BGR color
├── Demo.gif   # Gif of tracking in action
└── README.md        # This file