# EfficientNet
The presented code herein implements the algorithm outlined in the article titled "Automated Diagnosis of Pneumonia from Classification of Chest X-Ray Images using EfficientNet," with a specific focus on the following key aspects:

EfficientNet Architecture:
EfficientNet stands as a family of convolutional neural networks (CNNs) meticulously crafted to achieve superior performance while optimizing computational resources. Its architecture rests on a compound scaling methodology, uniformly adjusting dimensions of depth, width, and resolution through a set of predetermined scaling coefficients. This approach ensures EfficientNet strikes a harmonious balance between network accuracy and computational efficiency, thereby surpassing many existing CNN models across diverse benchmarking scenarios.

The variant of EfficientNet utilized in this investigation, typically denoted from EfficientNet-B0 to EfficientNet-B7, offers a spectrum of sizes and complexities. Each iteration progressively enhances both size and accuracy, with EfficientNet-B0 representing the smallest and most resource-efficient option. In selecting the appropriate variant for this study, due consideration was given to dataset scale and available computational resources.

Methodology:

Data Collection and Preprocessing:
The dataset encompasses chest X-ray images sourced from multiple clinical and experimental sources, thus introducing variability in image quality and characteristics. Initial preprocessing stages comprised:
Exploratory Data Analysis (EDA): A comprehensive analysis aimed at understanding fundamental dataset attributes and distribution patterns.
Data Cleaning: Rigorous removal of noise and extraneous data to enhance model training efficacy.
Class Imbalance Mitigation: Employing strategies such as oversampling minority classes or undersampling majority classes to ensure equitable class distribution.
Data Augmentation: Application of techniques to artificially expand the dataset by generating modified image versions through transformations like rotation, flipping, and scaling.
Transfer Learning and Fine-Tuning:
Transfer learning entails harnessing a pre-trained model on a large dataset and customizing it for the specific task of pneumonia detection. This process entails:
Model Selection: Opting for EfficientNet due to its established performance and computational efficiency.
Initial Training: Utilizing the EfficientNet model pre-trained on the ImageNet dataset as the initial starting point.
Fine-Tuning: Making necessary adjustments to the pre-trained model to align it with the chest X-ray dataset. This entails freezing the initial layers of the network to preserve learned features while training the latter layers on the new dataset to adapt to pneumonia-specific features.
Model Evaluation:
The performance of the EfficientNet model underwent comprehensive evaluation utilizing various metrics, including:
Accuracy: Reflecting the proportion of correctly identified pneumonia cases relative to the total cases.
Area Under the Curve (AUC): Quantifying the model's ability to discriminate between positive and negative cases.
Precision, Recall, and F1 Score: Offering nuanced insights into the model's precision, recall, and overall balance between the two through the harmonic mean of precision and recall (F1 score).
The ensuing results are delineated as follows:

![image](https://github.com/fmirzadeh99/EfficientNet/assets/169579231/59ca16c2-a535-46d1-ad1e-94e2faeef8c3)

![image](https://github.com/fmirzadeh99/EfficientNet/assets/169579231/312ed42c-85f5-4632-8b2b-df98ec8ab2c9)

![image](https://github.com/fmirzadeh99/EfficientNet/assets/169579231/0baee230-bb32-42a7-94b3-a7b449096570)
