# YOLOv5 Cone Detection for Formula Student
This repository contains a YOLOv5 model fine-tuned to detect colored cones for the Formula Student Driverless competition. The model is trained on the FSOCO dataset and is optimized for real-time performance.

**Model Performance Examples**

Here is a quick look at how the model performs on sample test images.

**Original vs. Prediction**
| Original | Prediction |
|---|---|
| inference_examples/BME_00044.jpg | inference_examples/BME_00044_prediction.jpg |
| inference_examples/BME_00063.jpg | inference_examples/BME_00063_prediction.jpg |

**Getting Started**

Follow these instructions to set up the project and run the model on your local machine.

**Prerequisites**

Python 3.8 or later

Pip and a virtual environment (recommended)

**Installation**

Clone the repository:
```
git clone https://github.com/Sushant1703/Formula-Student-Cone-Detector.git
cd Formula-Student-Cone-Detector/yolov5/
```

**Create and activate a virtual environment:**

For Mac/Linux
```
python3 -m venv venv
source venv/bin/activate 
```

For Windows
```
python -m venv venv
.\venv\Scripts\activate
```

Install the required dependencies: ( ensure your cd is 
```
pip install -r requirements.txt
```

**Usage**

You can use the included detect.py script to run inference on your own images, videos, or a live camera feed.

**Run on an Image**
```
python detect.py --weights weights/best.pt --source path/to/your/image.jpg
```

**Run on a Video**
```
python detect.py --weights weights/best.pt --source path/to/your/video.mp4
```

The output, with bounding boxes drawn on the media, will be saved automatically in the runs/detect/ directory.

**Training Details**

Base Model: YOLOv5s

Dataset: FSOCO (Formula Student Objects in Context)

**Classes:**

1) yellow_cone

2) blue_cone

3) orange_cone

4) large_orange_cone

5) unknown_cone

**The analysis and training process can be reviewed in the Jupyter Notebook located in the /analysis folder.**
