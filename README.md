# Object-Detection-Using-Yolo-and-OpenCV-

## What is Yolo exactly?
YOLO (You Only Look Once) is a method / way to do object detection. It is the algorithm/strategy behind how the code is going to detect objects in the image.

The official implementation of this idea is available through DarkNet(neural net implementation from the ground up in 'C' from the author). It is available on github for people to use.

Earlier detection frameworks, looked at different parts of the image multiple times at different scales and repurposed image classification technique to detect objects. This approach is slow and inefficient.

YOLO takes entirely different approach. It looks at the entire image only once and goes through the network once and detects objects. Hence the name. It is very fast. That’s the reason it has got so popular.

Lets see how YOLO detects the objects in a given image.

First, it divides the image into a 13×13 grid of cells. The size of these 169 cells vary depending on the size of the input. For a 416×416 input size that we used in our experiments, the cell size was 32×32. Each cell is then responsible for predicting a number of boxes in the image.

For each bounding box, the network also predicts the confidence that the bounding box actually encloses an object, and the probability of the enclosed object being a particular class.

Most of these bounding boxes are eliminated because their confidence is low or because they are enclosing the same object as another bounding box with very high confidence score. This technique is called non-maximum suppression.

The authors of YOLOv3, Joseph Redmon and Ali Farhadi, have made YOLOv3 faster and more accurate than their previous work YOLOv2. YOLOv3 handles multiple scales better. They have also improved the network by making it bigger and taking it towards residual networks by adding shortcut connections.

## What is Open CV

OpenCV (Open source computer vision) is a library of programming functions mainly aimed at real-time computer vision. Originally developed by Intel, it was later supported by Willow Garage then Itseez (which was later acquired by Intel). The library is cross-platform and free for use under the open-source BSD license.

### What it can do:

1. Read and Write Images.
2. Detection of faces and its features.
3. Detection of shapes like Circle,rectangle etc in a image. E.g Detection of coin in images.
4. Text recognition in images. e.g Reading Number Plates
5. Modifying image quality and colors e.g Instagram, CamScanner.
6. Developing Augmented reality apps.

and many more...

### Which Language it supports:

1. C++
2. Android SDK
3. Java
4. Python
5. C (Not recommended)

### Some Advantages of using OpenCV:
1. Simple to learn,lots of tutorial available.
2. Works with almost all the famous languages.
3. Free to use.

## Why use OpenCV for Yolo?

Here are a few reasons you may want to use OpenCV for YOLO.

1. Easy integration with an OpenCV application: If your application already uses OpenCV and you simply want to use YOLOv3, you don’t have to worry about compiling and building the extra Darknet code.
2. OpenCV CPU version is 9x faster: OpenCV’s CPU implementation of the DNN module is astonishingly fast. For example, Darknet when used with OpenMP takes about 2 seconds on a CPU for inference on a single image. In contrast, OpenCV’s implementation runs in a mere 0.22 seconds! Check out table below.
3. Python support: Darknet is written in C, and it does not officially support Python. In contrast, OpenCV does. There are python ports available for Darknet though.

## Problem Statement:
  Create an object detection code that will use yolo framework to detect the objects from the image. Firstly, on running the script, camera of the laptop will capture a picture and save it after which it will perform object detection on it and will show the image with detected object into a rectangle with detected name and save it using the detection date and time along with total number of detections in it.
