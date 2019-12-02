# Emotion Filter

This is a machine learning project that takes a facial picture as input and gives an emotion as output. Simply put, it's a face
classifier.

## Getting Started

Before you can get the project up and running one needs to follow procedures to get the projects up and running.
It is preferred that the user is running Ubuntu and has Anaconda or MiniConda Distribution installed.

```
Required Packages

1)Python 2.7
2)Cuda 10 (If running on GPU)
3)Pytorch
4)torchvision
5)Sklearn
6)PIL
7)Numpy
```

### Installing

If one has Anaconda or Miniconda installed it is technically easier to reproduce the results. Simply run the following commands
to install the necessary packages and create a seperate environment for our tests.

```
conda create -n EmotionFilter python=2.7 anaconda

conda activate EmotionFilter

conda install pytorch==0.4.0 torchvision==0.2.0 cuda100 -c pytorch  (cuda90 if CUDA9, cuda80 if CUDA8 etc)
```

## Training from Scratch

To train the model from scratch one needs to follow the following operations.

### Copying dataset from drive

Go to
```
https://drive.google.com/open?id=1K9ayDIoNWmfMteLAf7QtphFkhrgPc4a1
```
& copy the data folder to the Emotion Folder directory. It contains the data.h5 which is warped version of the fer2013.csv
which will be used for the pytorch dataloader.

### Training
Make sure your environment is active.
```
conda activate EmotionFilter
```

The following command will train the model for 250 epochs. 
``` trainVGG.py ```

The weights will be saved in following folder
``` FER2013_VGG19```

If anyone wants to continue their training from their previous weights, they can simply run the following commands.
``` trainVGG.py --resume ```

## Accuracy & other plots

One can follow the following operations after they have some weights from the model. This can be done by training the model
and achieveing the weights or one can simply copy the weights folder from the google drive link given above
named ```FER2013_VGG19``` into the ```EmotionFilter``` of their directory.

### Plotting the Confusion Matrix

Run 
```plot_fer2013_confusion_matrix_VGG19.py```

The confusion matrix will generate in the weights folder.



