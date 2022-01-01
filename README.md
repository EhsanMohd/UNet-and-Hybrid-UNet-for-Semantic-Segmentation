# UNet-and-Hybrid-UNet-for-Semantic-Segmentation
UNet and Hybrid UNet for Semantic Segmentation on CityScapes dataset with dice score as metric. 

First of all, as with any Python file or IPython notebook, all the required libraries are imported. The libraries imported include os to handle file paths, numpy for numerical processing, pandas for data manipulation, Pytorch for creating and training the model and matplotlib & seaborn for visualizations. 

Next the file paths for the dataset are fetched and paths for logging directory and weight directory are created. 

A class called Generator is created to transform the training data as it loads based on various parameters such as batch size, scaling factor, and data augmentation approaches. The class has a function to augment the training data and a function to generate a training batch. 
Some images with their masks from the training dataset are displayed to gain an understanding of what the images hold. 

Next the UNet model is created as a class with objects of other classes as its components. After that a UNet model is created as an object of the UNet class.
Adam optimizer with binary cross entropy loss function was used for training the model. A function for training is defined, using which the model is trained on 10 epochs with a batch size of 32 images. 

Using the validation dataset, some predictions are made on the trained model and the results and displayed and compared with the ground truth images. 
 
 
Libraries used:
1. numpy 
2. os
3. seaborn 
4. matplotlib 
5. pandas 
6. tqdm 
7. pytorch 
8. torchvision 
9. cv2
10. random

The motivation for the project:
To check whether there is an improvement in the performance of the UNet segmentation model with a slight change in its structure. 

The files in the repository with a small description of each:
Readme -> the file you are reading right now
UNet.ipynb -> holds code for creation, training and testing of the UNet model for cityscapes dataset 
Hybrid_UNet.ipynb -> holds code for creation, training and testing of the Hybrid UNet model for cityscapes dataset 
Licence -> MIT licence 

Download the dataset from https://www.kaggle.com/dansbecker/cityscapes-image-pairs and extract and use the corresponding paths in the code for the code to run successfully. 

Summary of the results of the analysis:
The dice score co-efficient which is a measure of accuracy in the task of semantic segmentation shows improvement when we used the Hybrid model. The dice score of the plain UNet model was 0.4549 when compared with the Hybrid UNet model for which it is 0.4588. Comparing them with the benchmark (0.77) both the models have low values due to the smaller number of epochs and extremely small size of the dataset. 

Necessary acknowledgments:None 
