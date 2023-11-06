# Color Detection Using OpenCV
This simple project demonstrates how to detect a specific color in a live video stream using the OpenCV library in Python. It captures frames from the default camera (usually your webcam), converts them to the HSV color space, and highlights the detected color within the video feed. In this example, we are detecting the color blue, but you can modify the color variable to target different colors.

## Prerequisites
Before running this project, ensure that you have the following installed:

- Python 3.8+
- OpenCV (cv2)
- Pillow (PIL)
- NumPy

You can install these dependencies using pip:
```
pip install opencv-python-headless
pip install pillow
pip install numpy
```

## Getting Started
1. Clone or download the project to your local machine.
2. Open a terminal or command prompt and navigate to the project directory.
3. Run the Python script

```
python color_detection.py
```

## Customizing Color Detection
1. You'll see a window showing the live video feed from your default camera. The script is set to detect the color blue by default. Move objects of the target color in front of the camera to see the color detection in action. Press 'q' to exit the program.
2. To detect a different color, you can change the color variable in the `color_detection.py` file to the BGR (Blue-Green-Red) values of the desired color. Make sure to specify the color in BGR format, as shown in the following line:
   ```
   color = [255, 0, 0]  # Blue in BGR colorspace
   ```
3. You can use online tools or software to find the BGR values for your desired color and update the color variable accordingly.

## Color Detection Algorithm
The core of the color detection algorithm is to convert the captured frame from the camera into the HSV (Hue, Saturation, Value) color space. The `get_limits` function calculates the lower and upper HSV limits based on the provided BGR color. The script then creates a mask to identify pixels within this color range and overlays a green rectangle on the detected area.

## LICENSE
This project is open-source and available under the [MIT License](LICENSE).

Feel free to modify and expand upon this project to suit your specific needs. If you encounter any issues or have suggestions for improvement, please open an issue or submit a pull request on the project's GitHub repository.
