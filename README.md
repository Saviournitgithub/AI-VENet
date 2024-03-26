# AI-VENet

# METHODOLOGY

The AI-VENet framework proposed for breast cancer classification using BUS images. The proposed architecture consist of four stages: i) Pre-Processing, ii) Feature Extraction, iii) Oversampling and iv) Classification. In the preprocessing stage data augmentation and denoising is performed where BM3D filter is used for denoising. In the feature extraction stage attention based deep features and handcrafted features are extracted where newly devloped Hybrid Attention Module (HAM) is utilized for attention based deep feature extraction. Whereas HOG is used for handcrfated features. In next step Borderline SMOTE is used to create synthetic data samples. Finally, a weighted voting technique is employed for classification, where SVM, XT, and LGBM serve as base classifiers, and the weights of these base classifiers are determined using the Hill Climbing (HC) optimization algorithm. The architecture of AI-VENet is provided below.


![Weighted_Voting_final(mask) (5)](https://github.com/Saviournitgithub/AI-VENet/assets/164878062/bb7d9b72-8889-4258-9a8b-c085cca5f918)


# STEPS:

Step 1: Read images from the directory.

Step 2: Extract features using attention based ResNet50 and HOG. (To extract features using attention based ResNet50, first train the attention model with the secondary BUS (Breast Ultrasound) dataset and extract features from the primary BUS dataset using trained attention based ResNet50 model)

Step3: Concatinate the attention based deep features and HOG features.

Step 4: Apply  Borderline SMOTE (Graplical representaion of before and after applying BSMOTE is given below)
![smote (2)](https://github.com/Saviournitgithub/AI-VENet/assets/164878062/9b7fa753-c0ef-40fa-8096-763c9850a514)

Step5: Classification using weighted voting ensemble classifier (The weights of the base classifier are determined using the HC algorithm. The initial parameters and output are provided below:)

![TABLE_PAPER](https://github.com/Saviournitgithub/AI-VENet/assets/164878062/b6945089-5a27-4673-9fc5-3bb1b7f18b2b)

The flow diagram of the HC algorithm is provided below:



![Hill_climbing (2)](https://github.com/Saviournitgithub/AI-VENet/assets/164878062/f7a11fb4-73a5-4e34-a5c4-42f0e7d9881b)


# Data Availability

# BUSI:
https://scholar.cu.edu.eg/?q=afahmy/pages/dataset

DOI: https://doi.org/10.1016/j.dib.2019.104863

# UDIAT:
http://www2.docm.mmu.ac.uk/STAFF/m.yap/dataset.php
