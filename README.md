# AI-Personal-Trainer

This is a Python script that uses the OpenCV library to read a video file and perform pose detection to count the number of curls performed during a bicep curl exercise. It also displays the percentage of completion of each curl and the current frame rate.

### Dependencies
<ul> OpenCV </ul>
<ul> NumPy </ul>
<ul> PoseModule module (included in the repository) </ul>

### Usage
Clone this repository.
Make sure you have all the dependencies installed.
Put your video file called "curls.mp4" in a subdirectory called "AiTrainer".
Run the script curl_counter.py.

### How it works
The script first imports the necessary libraries, including OpenCV, NumPy, and a custom module called "PoseModule" that contains the pose detection functionality.

Next, the script initializes some variables, including the video capture object, the pose detector object, and variables to keep track of the curl count and the direction of the curl (up or down). The script also initializes a variable to keep track of the previous frame time to calculate the current frame rate.

The main loop of the script reads each frame of the video using the video capture object and resizes it to a standard size of 1280x720. It then uses the pose detector object to find the pose in the image and the positions of various body landmarks, including the left and right arms.

The script then calculates the angle of the right arm at the elbow joint and interpolates this angle to a percentage of completion for the current curl. It also calculates a position for a visual bar that represents the angle and percentage of completion of the curl.

The script then checks whether the percentage of completion is 0 or 100 and updates the curl count and direction accordingly. It also sets the color of the visual bar to green if the percentage of completion is 100, indicating that the curl is complete.

The script then draws the visual bar and the curl count on the image and calculates and displays the current frame rate. Finally, the script displays the image and waits for a key press to exit the program.

Note that the script requires a video file called "curls.mp4" to be present in a subdirectory called "AiTrainer". The script also assumes that the PoseModule.py file is present in the same directory as the script.
