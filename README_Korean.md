# 라즈베리파이기반 TensorFlow 사물인식 로봇

***

* TensorFlow Version: 1.0.1
* [English version](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/README.md)

## 소개

이것은 시각 인식([Inception V3](https://research.googleblog.com/2016/03/train-your-own-image-classifier-with.html))을 구현하는 라즈베리파이 기반 로봇 입니다. 텐서플로우를 이용한 컴퓨터 비전은 사람, 자동차, 버스, 과일 등과 같은 많은 물체를 인식 할 수 있습니다. 

* 하드웨어 : Raspberry-Pi2, Sony PS3 Eye USB 카메라
 
   (소니 PS3 Eye USB 카메라 대신에 로직텍 C270 USB 카메라와 당신의 라즈베리파이를 함께 사용할 수 있습니다.)

* 소프트웨어 : 파이썬 텐서플로우 라이브러리(v1.0.1), 주피터 노트북

![Structure.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/Structure.png)


## 나의 동기
 저는 라즈베리파이의 텐서플로우를 이용해서 이미지 인식성능 대해 정말 궁금하였습니다. 또한 주피터노트북은 빠른 프로토타입으로 즉석으로 코드를 작성하는 데 매우 편리합니다. 따라서 이미지 분류의 오류율 측면에서 Inception V3 (3.46 %)는 인간 (5.1 %)보다 우수하지만 라즈베리 파이의 처리 속도는 노트북과 비교할 때 매우 느립니다.  

([차트: 제프리 딘의 키노트 @구글 브레인](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44921.pdf)). 
 
 ![Chart_IR.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/Chart_ImageRecognition.png)


* Inception-v3 구조

![InceptionV3.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/InceptionV3.png)


## 요구사항 및 설치

 * USB 카메라드라이이버 설치하기
 ```
 sudo apt-get install fswebcam
 ```
 
 * USB 카메라 테스트하기
 ```
 fswebcam test.jpg
 ```

 * 텐서플로우 (버전1.0.1): [라즈베리파이에서 텐서플로우 설치방법](https://www.instructables.com/id/Google-Tensorflow-on-Rapsberry-Pi/)
 
 * 주피터노트북: [라즈베리파이에서 주피터 설치방법](https://www.instructables.com/id/Jupyter-Notebook-on-Raspberry-Pi/)
 
 
## 시작방법
* 당신의 라즈베리파이에 텐서플로우(v1.0.1)와 주피터노트북을 함께 설치해야합니다.
* 먼저 라즈베리파이에서 TensorFlow-Powered_Robot_Vision git 저장소를 복제합니다. 이것은 다음과 같이 수행 할 수 있습니다.
```
cd /home/pi/Documents
git clone https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision.git
```
다음으로 새로 생성 된 디렉토리에 cd 명령합니다.
```
cd TensorFlow-Powered_Robot_Vision
``` 
아래와 같이 커맨드 창에서 주피터노트북을 구동해봅시다.
```
jupyter-notebook
```
주피터노트북을 구동할때 미리 훈련된 데이터(inception_v3.ckpt)가 자동으로 다운로드됩니다. (저장장소: / pi / home / Documents / datasets / inception)


## 소스 코드

* [TensorFlow-Powered_Robot_Vision.ipynb](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/TensorFlow-Powered_Robot_Vision.ipynb)
* [imagenet_class_names.txt](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/datasets/inception/imagenet_class_names.txt)
* inception_v3.ckpt (주피터노트북 사용할때 자동으로 다운로드됩니다.)


## 객체 인식 결과 (96.25 %, EntleBucher종 스위스 알프스산 개)

* 와우! 이미지인식결과 굉장하네요 !!

![RecognitionResult.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/Result_96.25.png)


## 참고자료
* [Rethinking the Inception Architecture for Computer Vision (Paper)](https://arxiv.org/abs/1512.00567)
* [Image Recognition::Tensorflow.org (Web)](https://www.tensorflow.org/tutorials/image_recognition)
* [Hands-On Machine Learning with Scikit-Learn and TensorFlow (Book)](https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1491962291/ref=sr_1_1?ie=UTF8&qid=1494573194&sr=8-1&keywords=hands+on+machine+learning+with+scikit+learn+and+tensorflow)
* [Train your own image classifier with Inception in TensorFlow (Blog)](https://research.googleblog.com/2016/03/train-your-own-image-classifier-with.html)
* ["Large-Scale Deep Learning for Building Intelligent Computer Systems," a Keynote Presentation from Google](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44921.pdf)

