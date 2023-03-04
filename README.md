# Dates-vs-Cashews-object-detection
Training YOLOv8 and Faster RCNN models to detect cashews and dates. 

The colab notebook: https://colab.research.google.com/drive/183FmQwelORoIR9h1dtoo1tHU9618Rlv5?usp=sharing


# Assignment description:

1. Take photos of your environment of two or more objects. (at least 100 instances between all objects) 

2. Annotate them on roboflow. 

3. Train a Faster RCNN model using detectron2

4. Train Yolov4/5/6/7/8 (only one of them of choice) in the smallest size

5. Evaluate both models based on mAP and speed and size.

# Solution:

The first problem that I faced during solving this assignment was what objects to detect then I decided to choose dates and cashews and there is a story behind it

## The story:

One day I was watching a movie and I wanted some snacks but I was too lazy to go to the kitchen and get some, so I thought what if there was a robot that can do this for me? life will be much easier. So I decided to bring humanity one step closer to staying in bed while being served by robots and train a model that can detect Dates and Cashews.

## How did I collect the dataset?

I went to the market and bought some dates and cashews then I returned home and took some photos of them in different environments and light conditions.

## How did I annotate the data?

I annotated the data by using a tool called roboflow then I added some preprocessing and augmentations to increase the size of the data:

- Flip: Horizontal
- 90° Rotate: Clockwise, Counter-Clockwise
- Rotation: Between -15° and +15°
- Shear: ±15° Horizontal, ±15° Vertical

# Training a Faster RCNN model:

For training a Faster RCNN model:

- Imported a notebook from the detectron2 GitHub page
- Chose an architecture for the model
- Imported the custom data
- Trained and evaluated the model

# Training a YOLOv8 model:

For training a YOLOv8 model:

- Imported a notebook from roboflow
- Imported the custom data
- Trained and evaluated the model

# Evaluation of the model

Both of the models performed well.

Faster RCNN:

**mAP** = 44.084

**inference time** = 67ms per image

**Size:**: 401Mb

YOLOv8:

**mAP** = 44.6

**inference time** = 23.1ms per image

**parameters:** 11136374 

**Size:** 21.5Mb

As we can see, both of them have very close mAP however, YOLOv8 is much better as it has a lower inference time and a small size.
