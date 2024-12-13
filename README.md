# KebunQ-ML
## 📋 Project Overview
KebunQ is a mobile application designed to assist home gardeners in Indonesia by identifying diseases in grape, tomato, and cucumber plants. Using image recognition technology, KebunQ simplifies the diagnosis process and provides educational content on disease prevention and treatment.

This project addresses the challenges faced by gardeners in identifying plant diseases, offering a solution that promotes sustainable gardening practices and a sense of community among gardening enthusiasts.

## 📊 Model Details
The AI-powered model leverages Convolutional Neural Networks (CNN) for image recognition, trained on a curated dataset of diseased and healthy plants.

Model Highlights:
Framework: TensorFlow <br>
Dataset Size: ~8,000 labeled images <br>
Accuracy: 92-97% (average across classes) <br>
Input Format: JPEG, JPG, PNG <br>
Output: Disease classification and treatment recommendations <br>

Our Dataset: [Dataset](https://drive.google.com/drive/folders/1ROh6v3-WBDmtzjOfKJ15Is-fIlGPtwYj?usp=sharing)

## 📈 Results

### Cucumber's Accuracy

![acctomato](https://github.com/user-attachments/assets/1793df44-c8e5-467d-83a9-4c4981af3ae2)

### Grape's Accuracy

![Screenshot 2024-12-13 133812](https://github.com/user-attachments/assets/51639d13-baf6-4adc-b80c-276500947437)

### Tomato's Accuracy

![eecee](https://github.com/user-attachments/assets/51abe2d4-9672-4c31-9edd-f6a39b017e8a)

## 🛠️ How to Use

### 1. Clone the repository
Clone this github repository or download zip and extract it
```bash
git clone https://github.com/KebunQ-Bangkit-Capstone/kebunq-ml.git
cd KebunQ
```

### 2. Open the ipynb file
Open the ipynb file contained in each folder using Local / Google Colaboraty

### 3. Download the Dataset
Download the Dataset [Here](https://drive.google.com/drive/folders/1ROh6v3-WBDmtzjOfKJ15Is-fIlGPtwYj?usp=sharing)

### 4. Check and Update Dataset Path
Ensure the dataset path in the notebook matches the location of the dataset in your Google Drive.

### 5. Run the Notebook and Save the Model
The model will be trained using the dataset and once the process complete, model will saved as an .h5 file format.
