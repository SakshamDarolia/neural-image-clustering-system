# neural-image-clustering-system
It takes images as input and then assigns them to a cluster based on the probability of each class in an image(extracted using a softmax layer at the end of network). For this an ensemble model of 3 ResNet50s(trained myself) is deployed at backend.

Here I've tried a new supervised way for clustering which is faster and in some cases more accurate than K-means because of the use of a trained model at backend. But as of now this project only works for 4 classes namely building, person, weapon and vehicle.

The only downside of supervised clustering is that you have to have a trained model(which will later be used for clustering) prior to the whole clustering process, whereas in K-means training happens on the fly i.e. the model stars with zero experience and learns from the images in real-time while clustering them one by one, eventually getting better. I'm working to overcome that downside of supervised clustering, so that even a few images would be sufficient for the model to learn the pattern thoroughly.

## Requirements:
1. PyQt5 (comes pre-installed in Ubuntu)
2. PyTorch 1.1+

## Prerequisites:
1. Create a folder named 'add_new' under ./clustering_sys code
2. Create a folder named 'ensemble_model' under ./clustering_sys code/dl_models
3. Create two folders 'level1' and 'level2' under ./clustering_sys code/dl_models/ensemble_model
4. Download the .pth(trained model) files from the link provided and place them in their respective folders:
   1. level1:
   - https://drive.google.com/open?id=1mo1jPRIjFLGWKc89ptShU4juakd5i2-1
   - https://drive.google.com/open?id=1aNr-PApeLLahk47mKnDLOGC1QJAOxMR3
   2. level2:
   - https://drive.google.com/open?id=1dB-6amHZ1ceb21_X-MbOTyerH5xJ2b5s
5. Check out the addresses of files provided in code in files under ./clustering_sys ui and change them according to your environment.
6. If you are using PyTorch GPU, please read the comments provided in impl.py located under ./clustering_sys ui

## How to use:
1. Open a terminal at ./clustering_sys ui
2. Activate the environment in which PyTorch is installed. (Skip this if you've PyTorch installed on base)
3. Compile and execute 'impl.py' using, $ python impl.py

file:///home/evil_overlord/Walls/00d4148cf10e821c-mercedes-benz-g63-amg-black-hd-wallpapers.jpg
