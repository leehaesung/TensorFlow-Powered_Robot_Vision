# TensorFlow-Powered Vision For Pi-based robot

***

## Introduction

This is a Pi-based robot to implement visual recognition. The TensorFlow-Powered vision(Inception V3) can recognize many objects such as people, car, fruits, and so on. 

* Hardware: Raspberry-Pi2, Sony PS3 Eye Camera
 (Available to use Logitech C270 USB camera)

* Software: TensorFlow(v1.0.1), Jupyter-Notebook

![Structure.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/Structure.png)


## Requirements and Installation

 * TensorFlow (V1.0.1): [How To Install TensorFlow on Raspberry Pi](https://www.instructables.com/id/Google-Tensorflow-on-Rapsberry-Pi/)
 
 * Jupyter-Notebook: [How To Install Jupyter-Notebook on Raspberry Pi](https://www.instructables.com/id/Jupyter-Notebook-on-Raspberry-Pi/)
 
 
## Quick Start
* You should install both TensorFlow(v1.0.1) and Jupyter-Notebook on your Raspberry Pi.
* First, clone the TensorFlow-Powered_Robot_Vision git repository on your Raspberry Pi. This can be accomplished by:
```
cd /home/pi/Documents
git clone https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision.git
```
Next, cd into the newly created directory:
```
cd TensorFlow-Powered_Robot_Vision
``` 
Let's start Jupyter-notebook on cammand window.
```
jupyter-notebook
```
When you implement the jupyter-notebook, the trained data(inception_v3.ckpt) will automatically download there.(/pi/home/Documents/datasets/inception)


## Source Codes

* [TensorFlow-Powered_Robot_Vision.ipynb](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/TensorFlow-Powered_Robot_Vision.ipynb)
* [imagenet_class_names.txt](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/datasets/inception/imagenet_class_names.txt)
* inception_v3.ckpt (When implementing Jupyter notebook)


## Result of Object Recognition (96.25%, EntleBucher)

![RecognitionResult.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/Result_96.25.png)


## Reference
* [Rethinking the Inception Architecture for Computer Vision (Paper)](https://arxiv.org/abs/1512.00567)
* [Image Recognition::Tensorflow.org (Web)](https://www.tensorflow.org/tutorials/image_recognition)
* [Hands-On Machine Learning with Scikit-Learn and TensorFlow (Book)](https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1491962291/ref=sr_1_1?ie=UTF8&qid=1494573194&sr=8-1&keywords=hands+on+machine+learning+with+scikit+learn+and+tensorflow)
* [Train your own image classifier with Inception in TensorFlow (Blog)](https://research.googleblog.com/2016/03/train-your-own-image-classifier-with.html)

