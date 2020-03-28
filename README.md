# neural-image-clustering-system

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
3. Run, $ python impl.py
