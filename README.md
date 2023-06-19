# Car Counter Repository

This repository contains code for counting cars in a video using object detection and tracking techniques. The code is written in Python and utilizes various libraries and tools.

## Setup and Dependencies

To run the code in this repository, you need to set up the following dependencies:

1. Python: Make sure you have Python installed on your system.
2. OpenCV: Install the OpenCV library for image and video processing.
   - Use the command `pip install opencv-python-headless` to install OpenCV.
3. Google Colab: Mount Google Drive to access the necessary files.
   - Use the following commands to mount Google Drive:
     ```
     from google.colab import drive
     drive.mount('/content/drive/')
     ```
4. Ultralytics: Install the Ultralytics library for object detection.
   - Use the command `!pip install ultralytics==8.0.28` to install Ultralytics.
5. cvzone: Install the cvzone library for additional computer vision utilities.
   - Use the command `!pip install cvzone` to install cvzone.
6. FilterPy: Install the FilterPy library for object tracking.
   - Use the command `!pip install filterpy==1.4.5` to install FilterPy.
7. scikit-image: Install the scikit-image library for image processing.
   - Use the command `!pip install scikit-image` to install scikit-image.
8. lap: Install the lap library for solving linear assignment problems.
   - Use the command `!pip install lap==0.4.0` to install lap.

## Usage

1. Clone the repository and navigate to the project directory.
```
git clone https://github.com/jakubpiwowarski/car_counter.git
cd car-counter
```
2. Download the necessary files, such as the YOLO model and the video file, and place them in the appropriate directories.
- YOLO model:
  - Store the YOLO model file at `/content/drive/MyDrive/101 - Object Detection /Pliki z kursu/yolov8n.pt`.
- Video file:
  - Store the video file at `/content/drive/MyDrive/101 - Object Detection /Pliki z kursu/Videos/cars.mp4`.
3. Run the main script to start counting cars in the video.
```
python car_counter.py
```
4. The script will display the processed video with bounding boxes around cars and car count information.

## Description

The main script, `car_counter.py`, performs the following steps:

1. Sets up the necessary dependencies and imports libraries.
2. Mounts Google Drive to access the required files.
3. Loads the YOLO model for object detection.
4. Defines the class names for detection.
5. Loads the mask image for the region of interest.
6. Initializes the object tracker.
7. Opens the video file for processing.
8. Processes each frame of the video:
- Applies the mask to the frame.
- Performs object detection using the YOLO model.
- Filters the detections to include only cars, trucks, buses, and motorbikes with confidence above a certain threshold.
- Updates the object tracker with the filtered detections.
- Draws bounding boxes around the tracked objects.
- Displays the processed frame with car count information.
9. Exits when the video processing is complete.

## Results

The script utilizes object detection and tracking techniques to count the number of cars in a video. The processed video is displayed with bounding boxes around the cars and the car count information. The script also draws a line indicating a specific region of interest.

## License

This project is licensed under the MIT License.

## Acknowledgments

This project is inspired by the "Project 1 - Car Counter" from the "101 - Object Detection" course.

Please note that this README file assumes the repository structure and file locations based on the provided code. Adjustments may be needed if the structure or file locations differ.
