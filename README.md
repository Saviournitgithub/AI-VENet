# AI-VENet

# METHODOLOGY

The AI-VENet framework proposed for breast cancer classification using BUS images. The proposed architecture consist of four stages: i) Pre-Processing, ii) Feature Extraction, iii) Oversampling and iv) Classification. In the preprocessing stage data augemnetation and denoising is performed where BM3D filter is used for dnoising. In the feature extraction stage attention based deep features and handcrafted features are extracted whre newly devloped Hybrid Attention Module (HAM) is utilized for attention based deep feature extraction. Whereas HOG is used for handcrfated features. In next step Borderline SMOTE is used to create synthic data samples.Finally weighted voting technique is used for classification whrere, SVM, XT and LGMB are used as base classifier and the weights of the base classifier is determined using Hill Climbing optimation algorithm. The archetecture of the AI-VENet is given below.


![Weighted_Voting_final(mask) (4)](https://github.com/Saviournitgithub/AI-VENet/assets/164878062/138cfa96-6f35-4954-aab3-91ca58d94712)




# Steps:

Step1: Read images from the directory.

step2: Extract features using attention based ResNet50 and HOG. (To extract features using attention based ResNet50, first train the attention model with the secondary BUS dataset and extract features from the primary BUS dataset using trained attention based ResNet50 model)

Step3: Concatinate the attention based deep features and HOG features.

step4: Apply  Borderline SMOTE (Graplical representtaion of before and after applying BSMOTE is given below)
![smote (2)](https://github.com/Saviournitgithub/AI-VENet/assets/164878062/9b7fa753-c0ef-40fa-8096-763c9850a514)

Step5: Classifiaction using weighted voting ensemble classifier (The weights of the base classifier determined using HC algorithm. The initial parameters and o/p is given below)

![TABLE_PAPER](https://github.com/Saviournitgithub/AI-VENet/assets/164878062/b6945089-5a27-4673-9fc5-3bb1b7f18b2b)

The flow diagram of HC algorithm given below



![Hill_climbing (2)](https://github.com/Saviournitgithub/AI-VENet/assets/164878062/f7a11fb4-73a5-4e34-a5c4-42f0e7d9881b)


# Data Availability

# BUSI:
https://scholar.cu.edu.eg/?q=afahmy/pages/dataset

DOI: https://doi.org/10.1016/j.dib.2019.104863

# UDIAT:
http://www2.docm.mmu.ac.uk/STAFF/m.yap/dataset.php
