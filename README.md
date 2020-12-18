# Improving-Breast-cancer-detection-using-Ultrasound-and-Mammogram-images

Breast Cancer is the second most leading cause of death among women worldwide.
There is always a need of advancement when it comes to medical imaging. Early detection of cancer followed by the proper treatment can reduce the risk of deaths.
Machine Learning can help medical professionals to diagnose the disease with more accuracy. 
Providing medical science with ML tools for diagnosing and treating cancer can reduce physician errors and financial losses. 
Where deep learning or neural networks is one of the techniques which can be used for breast cancer detection. 
Deep Learning techniques such as Data Augmentation and Transfer Learning are applied on Mammogram and Ultrasound images to improve breast cancer detection. 

In this project we aimed to improve breast cancer detection from Ultrasound and Mammogram images.

Data preprocessing
We took Ultrasound and Mammogram images with Normal and Malignant labels creating a binary classification problem. We took normal and malignant images as features and their masks as labels. 
We apply standardization and normalization before training the deep learning model.

U-net is a convolutional neural network that was developed for the task of segmenting regions of interest mostly for biomedical images. 
This architecture was modified to use for fewer training images and to get more precise segmentations. 

With small datasets a simple convolutional neural network performs very poorly. 
As collection of large data sets with high quality is extremely hard in biomedical applications, strategies such as Data augmentation is very useful which generates several additional images by image rotation, shift, rescale. 
Data augmentation is implemented with transfer learning. Transfer learning is a machine learning method in which first a model is trained on a source task which is like the target task. 
Source and target models have feature and classification layers
First, we train our baseline U-net model using source dataset and consider this as a source model. 
In the source model the initial layers are feature layers and the last layer is the classification layer.
After training the source model we separated the feature layers and freeze the weight update of the feature layer and then transferred that as input to the target model, which we trained using the target dataset.

We had fit our Transfer Learning model to run for 150 epochs. The graphs and the predicted images depicted an improvement in the detection. 
