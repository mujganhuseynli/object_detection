# Assistive System for Visually Impaired Users

## Overview

This project implements an assistive system designed to aid visually impaired users. The system leverages deep learning models, real-time computer vision, and various hardware components to provide a comprehensive solution for obstacle detection, path navigation, and voice command processing using [Google's TensorFlow Object Detection API](https://github.com/tensorflow/models/tree/master/research/object_detection) and [OpenCV](http://opencv.org/).

## Features

- **Obstacle Detection and Path Navigation**: Utilizes OpenCV for real-time computer vision processing to detect obstacles and navigate paths.
- **Deep Learning Models**: Implements TensorFlow for developing and deploying deep learning models that enhance the system's accuracy and efficiency.
- **Location Tracking**: Integrates GPS modules to provide precise location tracking, ensuring users can navigate safely and accurately.
- **Sensor Data Management**: Uses Arduino to manage sensor data, improving the system's responsiveness and reliability.
- **Voice Command Processing**: Employs Google Speech-to-Text API to convert voice commands into actions, offering a hands-free experience and increasing accessibility.


## Getting Started
1. `conda env create -f environment.yml`
2. `python object_detection_app.py` / `python object_detection_multithreading.py`
    Optional arguments (default value):
    * Device index of the camera `--source=0`
    * Width of the frames in the video stream `--width=480`
    * Height of the frames in the video stream `--height=360`
    * Number of workers `--num-workers=2`
    * Size of the queue `--queue-size=5`
    * Get video from HLS stream rather than webcam '--stream-input=http://somertmpserver.com/hls/live.m3u8'
    * Send stream to livestreaming server '--stream-output=--stream=http://somertmpserver.com/hls/live.m3u8'

## Tests
```
pytest -vs utils/
```

## Requirements
- [Anaconda / Python 3.5](https://www.continuum.io/downloads)
- [TensorFlow 1.2](https://www.tensorflow.org/)
- [OpenCV 3.0](http://opencv.org/)

