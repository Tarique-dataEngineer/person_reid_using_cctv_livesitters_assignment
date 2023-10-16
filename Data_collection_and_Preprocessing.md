About Data



I took the dataset from youtube. It's publicly available. The CCTV footage contains people walking on the streets of New York from different views.The duration of this video is about 1:56 seconds. This is the best CCTV footage I found for re-identification our project.

Source Link :- https://www.youtube.com/watch?v=YzcawvDGe4Y&ab_channel=GKorb

The goal of the script is to extract and store individual frames from the video.
Here's a step-by-step explanation:

First, the code imports two libraries: 'cv2,' which is OpenCV for computer vision tasks, and 'os,' which is for managing the operating system (although 'os' is not used in this code).
The script initializes a video_capture object, which is essentially a video player that opens the 'cctv_footage.mp4' video file for reading.
It creates an empty list called 'frames' to store the individual frames from the video.
The code enters a loop, which will continue indefinitely unless a condition is met.
Inside the loop, it attempts to read a frame from the video file using video_capture.read(). This function returns two values: 'ret' (a boolean indicating whether a frame was successfully read) and 'frame' (the actual image frame).
It checks if 'ret' is 'False,' which means that there are no more frames to read in the video. If 'ret' is 'False,' the loop is terminated using the 'break' statement.
If 'ret' is 'True,' indicating that a frame was successfully read, the code appends that frame to the 'frames' list.


Here, RAM is not able to hold this much data so we divert all the cctv_footege to Disk
.
It takes each part of the video, called a frame, and does things like finding objects or people. Then, it saves each frame as a picture on a computer. The pictures are given names like 'frame_0000.jpg' , 'frame_0001.jpg.' and so on. This code does this for all the frames in the video. After it's done, it tells the computer to stop looking at the video. It's like taking pictures from a movie to use later.






Data Preprocessing:

Resizes each video frame to a standard size of 224x224 pixels.
Changes the frame's color format to RGB, which is how we typically see images.
The code converts the frame's data to numbers that computers can easily work with (float32).
Normalizes the pixel values in the frame to a range between -1 and 1, which helps in some computer vision tasks.
The code saves the processed frame as an image file on the computer, just like taking a snapshot.
Repeat these steps for all frames in the video until there are no more frames to process.

