## Introduction
This work implements the algorithm presented in the paper titled "Automated Diagnosis of Pneumonia from Classification of Chest X-Ray Images using EfficientNet," with regard to application according to the EfficientNet architecture in pneumonia diagnosis using chest X-ray images.

## Data Ingestion and Preprocessing
This dataset contains chest X-ray images from multiple clinical and experimental sources. Thus, variability in characteristics or image qualities has been added. The first preprocessing steps were as follows:
Exploratory Data Analysis (EDA): Conducted to understand the dataset's basic attributes and distribution patterns.
Data Cleaning: This is done in order to get rid of noise and extraneous data, thus increasing the efficiency of the training model.
Class imbalance mitigation: This was attained via oversampling of the minority classes or undersampling of the majority.
Data Augmentation: Synthetic augmentation of dataset through variations in images by means of operations like rotation, flipping, and scaling.

![image](https://github.com/user-attachments/assets/041dd37a-0af5-4070-9d89-cbb505a28f25)
|:-:|
|An image of one of the dataset samples with PNEUMONIA

!![image](https://github.com/user-attachments/assets/f6e56c7b-e6c5-4753-b5b8-ec2ea474e76d)
|:-:|
|Augmented data

## Hyperparameters and Training
For the purpose of this study, a family of CNNs called EfficientNet was chosen; it is designed to achieve an optimal balance between network accuracy and computational efficiency. Variant EfficientNet-B0 was chosen as the use case in view of the dataset size and availability of computational resources. The training involved:
Model selection: EfficientNet was selected for its established performance and computational efficiency.

![image](https://github.com/user-attachments/assets/0bc40425-fcd3-47e9-bb8b-a801708b386e)
|:-:|
|EfficientNet Architecture

Initial Training: The top EfficientNet trained on ImageNet served as the initialization.
Tuning: In this process, changes in the pre-trained model were fitted on the chest X-ray dataset. The concept of transfer learning here included freezing the first layer, which had preserved learned features, while latter layers were required to train further towards adaptation for features specific to the newly provided dataset of pneumonia.


## Evaluation Metrics and Results
The different metrics for which the performance was evaluated of the EfficientNet model were:

Accuracy: This is the measure of how correct pneumonia identification is for the proportion of cases against the total number.

AUC: This quantifies a model's performance in classifying positive versus negative cases.

Precision, Recall, F1 Score: All of these provide nuanced insight into a model's performance, where precision indicates the correctness of the positive predictions, recall reflects the model's ability to identify all positive cases, and the F1 score provides a balance between precision and recall.

## Results
The EfficientNet model demonstrated very high accuracy and strong performance in all evaluation metrics. The literature has proven the efficiency of this architecture in diagnosing pneumonia from chest X-ray images. In details:
Accuracy: 0.85666 

![image](https://github.com/user-attachments/assets/24da41f0-0706-4fdc-a4d4-9726b126de5d)
|:-:|
|Confusion Matrix

![image](https://github.com/user-attachments/assets/a06995e9-9300-44f6-9b84-da017ac2e550)
|:-:|
|ROC curve

Precision: 0.96

Recall: 0.83

F1 Score: 0.89

These results show that the model has highly efficient performance in classifying the presence of pneumonia on chest radiographs, hence validating EfficientNet for medical image classification tasks.
