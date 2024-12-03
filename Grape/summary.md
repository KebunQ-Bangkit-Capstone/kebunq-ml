# Summary of Grape Model (Best Model)

## Dataset
The dataset used is a combination of datasets from [Grape Dataset](https://www.kaggle.com/datasets/khalil18/grape-dataset)

The dataset used in this model can be accessed at [Grape zip](https://drive.google.com/drive/folders/1GUiqstRU-dbCwnZWGd-8W67BBTuz4lNg?usp=sharing)

## Prepocessing Steps
### 1. Pixel Normalization
Converting the pixel values of the image to a floating-point representation and dividing them by 255.0
### 2. Resize 
Resizes the image to a new width and height of 224 pixels each
### 3. Balancing dataset
Create a balanced dataset by selecting a specific number of images from each class and copying them to a new directory

The result of preprocessing data is as follows 

<img src="-" width="600px">

## Split Dataset
Divide the dataset into three parts: train, validation, and test with composition 
Train : 80%, Validation: 10%, and Test : 10%

## Build Model
This model uses a sequential model with a Conv2D layer followed by MaxPooling2D, flatten, dropout, and dense. The model was used to classify images with 4 different classes namely non potato, potato early blight, potato healthy, potato late blight.
A summary of the model can be seen in this image 

<img src="" width="600px">

To train and evaluate the model, callbacks are defined : earlystopping and modelcheckpoint. The model is then compiled using Adam's optimizer, loss function categorical crossentropy, and metric accuracy. With 50 epochs, the results of model training can be seen in the following figure

<img src="" width="600px">

On the validation generator, obtained
test loss: 0.009127928875386715 and test accuracy: 0.9975000023841858
<img src="" width="600px">

While on the test generator, obtained
test loss: 0.03554805368185043 and test accuracy: 0.9775000214576721
<img src="" width="600px">

Overall, the model has good performance on test data and validation data. Low loss values and high accuracy indicate that the model is able to classify both data sets well. The difference between loss and accuracy in the test data and validation data is very small, which indicates that the model is not overfitting to the training data and can generalize well to data not used in training

## Plotting Accuracy and Loss of Training and Validation

<img src="" width="600px">


## Confusion Matrix
The confusion matrix generated using test data looks like the following image

<img src="" width="600px">

It can be seen that the model classifies not potato class correctly. While in the potato early blight class, there are 2 times the model error classifying to potato late blight. There is 5 time model error classifying potato late blight as potato healthy. And there is 2 time model error classifying potato early blight and potato healthy as potato late blight

## Classification Report 

<img src="" width="600px">
     
## Testing Images
Testing is done by uploading images. With some sample images, the results show that the model has classified 3 images according to existing classes

<img src="" height="600px">

## Saving Model
The model is saved in .h5 form and can be directly downloaded using the available code 
