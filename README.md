# Real-time-face-recognition-with-OpenCV-and-face_recognition-library
This code uses face_recognition and OpenCV libraries to recognize faces in a live video from a webcam, and mark them with labels and rectangles. It compares the detected faces with a set of known faces and their names, and plays a beep sound when an unknown face is detected.

# Steps used to solve this problem

1. Load sample images of known faces and encode their facial features using the face_recognition library.
2. Create arrays of the known face encodings and their corresponding names.
3. Start capturing live video frames from the default webcam using OpenCV's VideoCapture object.
4. In each frame, resize the video to a smaller size and convert it to RGB color format.
5. Use the face_recognition library to detect the locations of all faces in the video frame and encode their features.
6. Compare the facial features of each detected face with the known face encodings to determine if it matches any of the known faces.
7. If a match is found, label the face with its corresponding name in the video frame.
8. If an unknown face is detected, play a beep sound and label the face as "Unknown" in the video frame.
9. Display the labeled video frame in a window using OpenCV's imshow function.
10. Continuously repeat steps 3-9 until the user presses the 'q' key to quit.
11. Release the video capture and close the video window when the program exits.

# The process of the code:

1. The program loads pre-trained face encodings of known individuals.
2. The program initializes variables for face locations, encodings, and names.
3. The program initializes a boolean variable to alternate processing frames.
4. The program initializes a video capture object for webcam input.
5. The program continuously captures frames from the video capture object.
6. For every other frame, the program resizes the frame to 1/4 size, converts it from BGR to RGB color, detects faces in the frame, and extracts the face encodings.
7. The program compares the extracted face encodings with the known encodings to determine if any of the detected faces belong to a known individual.
8. The program outputs the names of detected faces and draws rectangles around faces, as well as labels with names, on the frame.
9. The program plays a beep sound and draws a red rectangle around faces of unknown individuals.
10. The program displays the resulting frame with face detections in real-time.
11. The program continues until the user presses the "q" key to quit.
12. The program releases the video capture object and destroys all windows created by OpenCV.
