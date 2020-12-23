# OpenCV-Virtual-Gesture-Keyboard
A very simple gesture virtual keyboard using Python and OpenCV. It based on yellow paper that is worn on finger and the ideaof click is based on when the paper moves towards the camera its area increases and when it goes away, the area decreases which is detected by the camera. The position of the click determines the key press that is to be simulated.

# Requirements
1. PyAutoGui<br>
2. OpenCV 3<br>

# Usage
First run the range-detector.py to set the range for the mask for colour segmentation. The easiest way to use it is to put the yellow paper in front of the camera and then slowly increasing the lower parameters(H_MIN, V_MIN, S_MIN) one by one and then slowly decreasing the upper parameters (H_MAX, V_MAX, S_MAX). When the adjusting has been done you will find that only the yellow paper will have a corresponding white patch and rest of the image will be dark. Then run the virtual_keyboard.py file.

    python3 range-detector.py -f HSV -w
    python3 virtual_keyboard.py
