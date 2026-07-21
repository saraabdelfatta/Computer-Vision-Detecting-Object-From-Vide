# Object Detection from Video Using YOLOv8

This project is a simple computer vision application that detects objects in a video using the YOLOv8 model.

The main script is in `code2.py`, and it uses:
- OpenCV for video processing
- Ultralytics YOLOv8 for object detection
- A pre-trained model file: `yolov8s.pt`

## Project Goal

The goal of this project is to load a video, detect objects frame by frame, draw bounding boxes around the detected objects, and display the results.

## Files in the Project

- `code2.py` — Python script for running object detection on a video
- `yolov8s.pt` — YOLOv8 small pre-trained model weights
- `55849-504238895.mp4` — sample input video

## Requirements

Before running the project, install the required packages:

```bash
pip install opencv-python ultralytics
```

If you are using Google Colab, also make sure the notebook environment supports the YOLOv8 workflow.

## How It Works

1. The video is opened using OpenCV.
2. Each frame is passed to the YOLOv8 model.
3. Detected objects are filtered by confidence score.
4. Bounding boxes and labels are drawn on the frame.
5. The processed video frame is displayed.

## Run the Project

### Option 1: Google Colab

Use the same code in a Colab notebook and make sure the video path is available in the environment.

### Option 2: Local Python Environment

Update the code so the video path points to your local video file, then run:

```bash
python code2.py
```

## Notes

- The current script was originally written for a Colab environment.
- If you run it locally, you may need to replace the Colab display function with a normal OpenCV window display.
- You can adjust the detection confidence threshold by changing the value in the script.

## Example Output

The output will show:
- Bounding boxes around detected objects
- The name of the detected class
- Confidence score for each object

## Future Improvements

You can extend this project by:
- detecting objects in multiple videos
- saving the processed video to a new file
- adding counting or tracking of objects
- building a web or GUI version

## License

This project is for educational and experimental use.
