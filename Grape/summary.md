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

![Screenshot 2024-12-03 221450](https://github.com/user-attachments/assets/06192028-7d18-4c7c-938d-3d87fa0a9775)

## Split Dataset
Divide the dataset into three parts: train, validation, and test with composition 
Train : 80%, Validation: 10%, and Test : 10%

## Build Model
This model uses a sequential model with a Conv2D layer followed by MaxPooling2D, flatten, dropout, and dense. The model was used to classify images with 4 different classes namely Black Rot, Esca (Black Measles), Healthy, Leaf Blight.
A summary of the model can be seen in this image 

![Screenshot 2024-12-03 221831](https://github.com/user-attachments/assets/bf0cae32-0ee5-4e48-a105-da01958c07c0)

To train and evaluate the model, callbacks are defined : earlystopping and modelcheckpoint. The model is then compiled using Adam's optimizer, loss function categorical crossentropy, and metric accuracy. With 50 epochs, the results of model training can be seen in the following figure

![Screenshot 2024-12-03 221856](https://github.com/user-attachments/assets/e5046433-e926-4365-bf08-a3a7076eae9f)

On the validation generator, obtained
test loss: 0.02407589554786682 and test accuracy: 0.9926035404205322

![Screenshot 2024-12-03 222024](https://github.com/user-attachments/assets/39549340-71b0-40c7-8028-101368ff91f9)

While on the test generator, obtained
test loss: 0.07771185785531998 and test accuracy: 0.979411780834198

![Screenshot 2024-12-03 222058](https://github.com/user-attachments/assets/94870b97-7381-4e59-9660-79e927505314)

Overall, the model has good performance on test data and validation data. Low loss values and high accuracy indicate that the model is able to classify both data sets well. The difference between loss and accuracy in the test data and validation data is very small, which indicates that the model is not overfitting to the training data and can generalize well to data not used in training

## Plotting Accuracy and Loss of Training and Validation
![download (1)](https://github.com/user-attachments/assets/f82f3d31-7969-4b73-a796-f7c779845dbb)
![download (2)](https://github.com/user-attachments/assets/319f0f7e-1911-4d14-b423-83588d622bdd)


## Confusion Matrix
The confusion matrix generated using test data looks like the following image

![download (3)](https://github.com/user-attachments/assets/a00d4d95-beed-4c0c-a84a-3790e8dde53a)

The confusion matrix above shows the performance of the classification model for detecting 4 classes: Black Rot, Esca (Black Measles), Healthy, and Leaf Blight.

The main diagonal shows the correct predictions:
- Black Rot: 166 samples were correctly detected.
- Esca (Black Measles): 170 samples were correctly detected.
- Healthy: 160 samples were correctly detected.
- Leaf Blight: 170 samples were correctly detected.

The off-diagonal shows the incorrect predictions:
- Example: 3 Black Rot samples were incorrectly predicted as Esca (Black Measles), and 8 Healthy samples were incorrectly predicted as Leaf Blight.

This matrix shows that the model has high accuracy, with small errors in some classes.

## Classification Report 

![Screenshot 2024-12-03 222301](https://github.com/user-attachments/assets/99636e83-ad1e-45a7-94c0-e957897b2d68)

     
## Testing Images
Testing is done by uploading images. With some sample images, the results show that the model has classified images according to existing classes

![Screenshot 2024-12-03 222421](https://github.com/user-attachments/assets/7b0d10c5-69e8-471a-a91b-a214ddeefeb0)

## Saving Model
The model is saved in .h5 form and can be directly downloaded using the available code 
