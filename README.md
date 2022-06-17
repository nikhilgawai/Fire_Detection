# Fire_Detection

Fire and smoke detection system which will detect objects based on whether it is fire and smoke

## Aim and Objectives

### Aim
To create a real-time video fire and smoke detection system which will detect objects based on whether it is fire and smoke for indoor outdoor  and environment.

### Objectives
➢ The main objective of the project is to create a program which can be either run on Jetson nano or any pc with YOLOv5 installed and start detecting using the camera module on the device.

➢ Using appropriate datasets for recognizing and interpreting data using machine learning.

➢ To show on the optical view finder of  the camera  module whether objects are Fire and smoke.

### Abstract

➢ An object is classified based on whether it is  fire and smoke is detected by the live feed from the system’s camera.

➢ We have completed this project on jetson nano which is a very small computational device.

➢ A lot of research is being conducted in the field of Computer Vision and Machine Learning (ML), where machines are trained to identify various objects from one another. Machine Learning provides various techniques through which various objects can be detected.

➢ One such technique is to use YOLOv5 with Roboflow model, which generates a small size trained model and makes ML integration easier.

➢Fire can be considered an unfortunate phenomenon that can cause catastrophic damage to property and environment. It can also pose an immense threat to human safety and lives, especially when this hazard gets out of control. When fire breaks out, especially in an open space, it often remains undetected by the conventional smoke sensor-based detection systems until it reaches a severe stage.

➢ Therefore, skillfully designed video based smoke and fire detection systems, using surveillance cameras in open space environments, can be the key to providing early warning signals. These systems utilise videos obtained from surveillance cameras and subsequently process. them to detect either fire and smoke or the initiation of a fire. 

### Introduction
➢ This project is based on a fire and smoke detection model with modifications. 
We are going to implement this project with Machine Learning and this project can be even run on jetson nano which we have done.

➢ This project can also be used to gather information about what category of fire and smoke does the object comes in.

➢ The objects can even be further classified into fire and smoke based on the image annotation we give in roboflow.

➢ Fire and smoke detection sometimes becomes difficult as certain mixed together and gets harder for the model to detect. However, training in Roboflow has allowed us to crop images and also change the contrast of certain images to match the time of day for better recognition by the model.

➢ Neural networks and machine learning have been used for these tasks and have obtained good results.

➢ Machine learning algorithms have proven to be very useful in pattern recognition and classification, and hence can be used for fire and smoke detection as well.

➢Fire is one of the leading hazards endangering human life, the economy, and the environment  Due to the rapid increase in fire accidents, every building or passenger vehicle for public transportation is equipped with fire protection and fire prevention systems. These systems consist mainly of point-type thermal and smoke detectors that need to be installed in proximity of the fire; otherwise, they may easily fail without detecting the fire. In addition, these devices must be properly installed and positioned as they can be damaged during the fire itself

➢Video-based fire detection is currently a standard technology due to image processing, computer vision, and Artifcial Intelligence. These systems have remarkable potential advantages over traditional methods, such as a fast response and wide detection areas.
Literature Review

➢Fire detection is crucial for safeguarding human life and property. Conventional techniques for fire detection rely on smoke and other by-products of fire for detection. They detect the presence of particles generated by smoke and fire by ionization. This has its own limitations because many factors cannot be assessed such as origin of fire, intensity, direction of smoke propagation, size of  fire, growth rate of fire etc.

➢ Another major drawback of conventional systems is that it can only cover small areas because the sensors should be in close  proximity to the fire for detection. To get over such limitations video fire detection systems are used.

➢ With the advent of computer vision and image processing, vision based fire detection techniques are widely used in recent times. This technique provides numerous advantages over the conventional system such as quicker response and wider coverage area. Many algorithms are available for fire and smoke detection. These algorithms use convolution neural networks which give way better accuracy in detection than the conventional methods of detection.

➢Deep learning algorithms can learn the useful features for fire and smoke detection from a video source. 
Convolutional neural networks are a branch of deep learning that can extract topological properties from an image.

➢ In our approach we use convolutional neural networks to train the system for intelligently detecting fire.  This is done by training the system on a very diverse dataset of fire,smoke and non-fire images. This can successfully improve the
accuracy of detection. This method will improve the accuracy of detection than the existing vision based models.

### Jetson Nano Compatibility

➢ The power of modern AI is now available for makers, learners, and embedded developers everywhere.

➢ NVIDIA® Jetson Nano™ Developer Kit is a small,  powerful computer that lets you run multiple neural networks in parallel for applications like image classification,  object detection,  segmentation,  and  speech processing. All in an easy-to-use platform that runs in as little as 5 watts.

➢ Hence due to ease of process as well as reduced cost of implementation we have used Jetson nano for model detection and training.
➢ NVIDIA JetPack SDK is the most comprehensive solution for building end-to-end accelerated AI applications. All Jetson modules and developer kits are 
supported by JetPack SDK.

➢ In our model we have used JetPack version 4.6 which is the latest production release and supports all Jetson modules.

### Proposed System
    
    1. Study basics of machine learning and image recognition.
    
    2. Start with implementation

➢ Front-end development

➢ Back-end development

3. Testing, analysing and improvising the model. An application using python and Roboflow and its machine learning libraries will be using machine learning to identify whether objects are fire and smoke.

4. Use datasets to interpret the object and suggest whether the object is fire and smoke.

### Methodology
The Fire and smoke detection system is a program that focuses on implementing real time Fire and smoke detection.
It is a prototype of a new product that comprises of the main module: Fire and smoke detection and then showing on view finder whether the object is Fire and smoke or not.

Fire and Smoke Detection Module

This Module is divided into two parts:

1] Fire and Smoke detection

➢ Ability to detect the location of object in any input image or frame. The output is the bounding box coordinates on the detected object.

➢ For this task, initially the Dataset library Kaggle was considered. But integrating it was a complex task so then we just downloaded the images from gettyimages.ae and google images and made our own dataset.

➢ This Datasets identifies object in a Bitmap graphic object and returns the bounding box image with annotation of object present in a given image.

2] Classification Detection

➢ Classification of the object based on whether it is fire and smoke or not.

➢ Hence YOLOv5 which is a model library from roboflow for image classification and vision was used.

➢ There are other models as well but YOLOv5 is smaller and generally easier to use in production. Given it is natively implemented in PyTorch (rather than Darknet), modifying the architecture and exporting and deployment to many environments is straightforward.

➢ YOLOv5 was used to train and test our model for various classes like Fire and smoke. We trained it for 149 epochs and achieved an accuracy of approximately 91%.

### Jetson Nano 2GB Developer Kit.





![IMG_20220125_115121](https://user-images.githubusercontent.com/100038142/170922938-5e7dd2ca-f4c2-4e2c-b7f9-fa35e331702b.jpg)







### Setup

## Installation

### Initial Setup

Remove unwanted Applications.
```bash
sudo apt-get remove --purge libreoffice*
sudo apt-get remove --purge thunderbird*
```
### Create Swap file

```bash
sudo fallocate -l 10.0G /swapfile1
sudo chmod 600 /swapfile1
sudo mkswap /swapfile1
sudo vim /etc/fstab
```
```bash
#################add line###########
/swapfile1 swap swap defaults 0 0
```
### Cuda Configuration

```bash
vim ~/.bashrc
```
```bash
#############add line #############
export PATH=/usr/local/cuda/bin${PATH:+:${PATH}}
export
LD_LIBRARY_PATh=/usr/local/cuda/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_P
ATH}}
export LD_PRELOAD=/usr/lib/aarch64-linux-gnu/libgomp.so.1
```
```bash
source ~/.bashrc
```
### Update a System
```bash
sudo apt-get update && sudo apt-get upgrade
```
################pip-21.3.1 setuptools-59.6.0 wheel-0.37.1#############################

```bash 
sudo apt install curl
```
``` bash 
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```
``` bash
sudo python3 get-pip.py
```
```bash
sudo apt-get install libopenblas-base libopenmpi-dev
```

```bash
vim ~/.bashrc
```

```bash
sudo pip3 install pillow
```
```bash
curl -LO https://nvidia.box.com/shared/static/p57jwntv436lfrd78inwl7iml6p13fzh.whl
```
```bash
mv p57jwntv436lfrd78inwl7iml6p13fzh.whl torch-1.8.0-cp36-cp36m-linux_aarch64.whl
```
```bash
sudo pip3 install torch-1.8.0-cp36-cp36m-linux_aarch64.whl
```
```bash
sudo python3 -c "import torch; print(torch.cuda.is_available())"
```
### Installation of torchvision.

```bash
git clone --branch v0.9.1 https://github.com/pytorch/vision torchvision
cd torchvision/
sudo python3 setup.py install
```
### Clone yolov5 Repositories and make it Compatible with Jetson Nano.

```bash
cd
git clone https://github.com/ultralytics/yolov5.git
cd yolov5/
```

``` bash
sudo pip3 install numpy==1.19.4
history
##################### comment torch,PyYAML and torchvision in requirement.txt##################################
sudo pip3 install --ignore-installed PyYAML>=5.3.1
sudo pip3 install -r requirements.txt
sudo python3 detect.py
sudo python3 detect.py --weights yolov5s.pt --source 0
```

## Fire Dataset Training
### We used Google Colab And Roboflow

train your model on colab and download the weights and pass them into yolov5 folder
link of project


## Running Fire Detection Model
source '0' for webcam

```bash
!python detect.py --weights best.pt --img 416 --conf 0.1 --source 0
```

### Demo



https://user-images.githubusercontent.com/100038142/170931878-8c774d97-9a97-4dee-97f1-e809b61d4e58.mp4





### Advantages

➢ Video-based fire detection is currently a standard technology due to image processing, computer vision, and Artificial Intelligence. These systems have remarkable potential advantages over traditional methods, such as a fast response and wide detection areas.

➢The development of new camera-based solutions improves the robustness and reliability of fire and smoke detection by filling the gap of previous systems. Cameras and closed-circuit television (CCTV) systems are already installed for surveillance purposes in most human environments, such as city streets, industry, public transportation. The existing infrastructure includes hundreds of video cameras, a communication network, possible processing units, and monitor screens in a control room. Their utilization would allow a reduction in purchase and installation cost as there is no need for additional products.

➢Deep learning techniques have the advantage of extracting the features automatically, making this process more effective and dramatically improving the state-of-the-art in Image Classification and object detection methods

➢ It can then convey to the person who present in control room  if it needs to be completely automated 

➢ When completely automated no user input is required and therefore works with absolute efficiency and speed.

➢ It can work around the clock and therefore becomes more cost efficient.

### Application

➢Detects object class like fire and smoke in a given image frame or view finder using a camera module.

➢ Can be used in various places.

➢ Can be used as a refrence for other ai models based on fire and smoke  detection.

### Future Scope
➢ As we know technology is marching towards automation, so this project is one of the step towards automation.

➢ Thus, for more accurate results it needs to be trained for more images, and for a greater number of epochs.

➢ Fire and smoke segregation will become a necessity in the future due to rise in population and hence our model will be of great help to tackle the 
situation in an efficient way.

➢  In future our model which can be trained and modified with just the addition of images can be very useful.

### Conclusion
➢ In this project our model is trying to detect objects and then showing it on view finder, live as what their class is as whether they are  Fire and smoke or not as we have specified in Roboflow.

➢Using smart cameras you can identify various suspicious incidents such as collisions, medical emergencies, and fires. Of such, fire is the most dangerous abnormal occurrence, because failure to control it at an early stage can lead to huge disasters, leading to human, ecological and economic losses. Inspired by the great potential of CNNs, we can detect fire from images or videos at an early stage.

➢Considering the fair fire detection accuracy of the CNN model, it can be of assistance to disaster management teams in managing fire disasters on time, thus preventing huge losses.

### Refrences

1] Roboflow :- https://roboflow.com/

2] Datasets or images used: https://www.gettyimages.in/search/2/image?family=creative&phrase=fire%20and%20smoke&sort=mostpopular&mediatype=photography

3] Google images

### References

[1]  Lucas-Borja M.E., González-Romero J., Plaza-     Álvarez P.A., Sagra J., Gómez M.E., Moya D., Heras J., et al.
The impact of straw mulching and salvage logging on post-fire runoff and soil erosion generation under mediterranean climate conditions
Sci. Total Environ., 654 (2019), pp. 441-451, 10.1016/j.scitotenv.2018.11.161
ArticleDownload PDFView Record in ScopusGoogle Scholar

[2] Lucas-Borja M.E., Hedo J., Cerdá A., Candel-Pérez D., Viñegla B.
Unravelling the importance of forest age stand and forest structure driving microbiological soil properties, enzymatic activities and soil nutrients content in mediterranean spanish black pine (pinus nigra ar. ssp. salzmannii) forest
Sci. Total Environ., 562 (2016), pp. 145-154, 10.1016/j.scitotenv.2016.03.160
ArticleDownload PDFView Record in ScopusGoogle Scholar
             
[3] Pan Y., Birdsey R.A., Phillips O.L., Jackson R.B.
The structure, distribution, and biomass of the world’s forests
Annu. Rev. Ecol. Evol. Syst., 44 (2013), pp. 593-622, 10.1146/annurev-ecolsys-110512-135914
 View PDF
View Record in ScopusGoogle Scholar
             
[4] Martinez-de Dios J.R., Arrue B.C., Ollero A., Merino L., Gómez-Rodríguez F.
Computer vision techniques for forest fire perception
Image Vis. Comput., 26 (4) (2008), pp. 550-562, 10.1016/j.imavis.2007.07.002
ArticleDownload PDFView Record in ScopusGoogle Scholar

[5]Harrison M.E., Page S.E., Limin S.H.
The global impact of Indonesian forest fires
Biologist, 56 (3) (2009), pp. 156-163
https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.709.6831&rep=rep1&type=pdf
View Record in ScopusGoogle Scholar
