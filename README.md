# Air Canvas using openCV
# By Hardik Hasani

Have you ever imagined capturing your creative thoughts by merely waving your finger in the air? Introducing an Air Canvas, where you can draw anything simply by moving your hands, using the landmarks on your knuckles as a guide. This virtual drawing tool, a computer vision project, lets you sketch in the air with hand gestures, powered by the robust combination of OpenCV and MediaPipe.

🔧 Tools and Libraries Employed:

Python3, NumPy, OpenCV, MediaPipe

How It Operates:

Video Capture: The script uses OpenCV to capture live video feed from the webcam.
Frame Processing: MediaPipe processes each frame to detect and track hand landmarks.
Landmark Drawing: The identified hand landmarks are rendered on the video frames, forming a virtual canvas for air drawing.
Algorithm Overview:
Start by reading the frames and converting the captured frames to the HSV color space (facilitates easier color detection).
Prepare the canvas frame and add the corresponding ink buttons on it.
Adjust MediaPipe settings to detect only one hand.
Detect landmarks by passing the RGB frame to MediaPipe's hand detector.
Identify the landmarks, locate the forefinger coordinates, and store them in an array for successive frames (arrays store points for drawing on the canvas).
Finally, render the points stored in the array on the frames and the canvas.

Screenshot:

<img src="/airCanvas.jpg" alt="image" width="700" height="500">