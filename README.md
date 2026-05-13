# VisionCanvas
An interactive 'Air Canvas' built with OpenCV and NumPy that allows users to draw in mid-air using color tracking and contour detection.../


## How it Works

1. **Color Segmentation:** Converts the camera feed to **HSV space** to isolate the marker's color using user-defined trackbars.
2. **Object Tracking:** Uses `cv2.findContours` and `cv2.minEnclosingCircle` to locate the marker's tip.
3. **Point Mapping:** The center coordinates of the marker are stored in `deques` to maintain a smooth drawing history.
4. **Virtual UI:** The screen is divided into regions that act as buttons for "Clear All" or switching between **Blue, Green, Red, and Yellow** ink.
   
---- 

## Features

* **Multi-Color Support:** Switch between 4 distinct colors seamlessly.
* **Live Calibration:** On-the-fly HSV adjustment to work with any colored object.
* **Dual Display:** View your drawing on both the live camera feed and a clean white canvas.
