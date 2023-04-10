﻿# # Melanoma Skin Cancer Detection Group Project
Group project headed by Rahul , Veer and Nikhit to identify Melanoma (Skin Cancer) using Convolutional Neural Network (CNN)

from a dataset of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC)

# ## Table of Contents
\* [General Info]

Melanoma is the deadliest and most aggressive form of skin cancer; it is estimated that 7,650 deaths will be attributed to melanoma in the year 2022. However, if Melanoma is caught in an early stage, the 5-year survival rate is about 99%. Therefore, the early detection of Melanoma, before metastasis, is critical for patient survival.

\* [Technologies Used]

TensorFlow , Keras , Numpy , Pandas

# ## General Information
Problem statement: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

Actinic keratosis

Basal cell carcinoma

Dermatofibroma

Melanoma

Nevus

Pigmented benign keratosis

Seborrheic keratosis

Squamous cell carcinoma

Vascular lesion

### # Sample image from Dataset
![](Aspose.Words.fc2a3008-965d-4ee9-bb19-ce199e84f8c7.001.png)

# CNN Architecture Design
To classify skin cancer using skin lesions images. To achieve higher accuracy and results on the classification task, I have built custom CNN model.

- Rescalling Layer - To rescale an input in the [0, 255] range to be in the [0, 1] range.
- Convolutional Layer – Convolutional operation processed on the layer. A convolution converts all the pixels in its receptive field into a single value. 
- Pooling Layer - Pooling layers used to reduce the dimensions of feature maps. Hence, it reduces the number of parameters required to learn and computation performed in the network. The pooling layer summarizes the features present in a region of the feature map generated by a convolution layer.
- Dropout Layer – Is mainly included to prevent overfitting. The Dropout layer randomly sets input units to 0 with a frequency of rate at each step during training time.
- Flatten Layer - converting the data into a 1-D array for input into the next layer. We flatten the output of the convolutional layers to create a single long feature vector and in turn is connected to the final model called a fully-connected layer.
- Activation Function(ReLU) - The rectified linear activation function or ReLU in short is a piecewise linear function that will output the input directly if it is positive, otherwise, it will output zero. The rectified linear activation function overcomes the vanishing gradient problem, allowing models to learn faster and perform better.
- Activation Function(Softmax) - Softmax function is used as the activation function in the output layer of neural network models that predict a multinomial probability distribution. Advantage of using Softmax is the output probabilities range. The range will 0 to 1, and the sum of all the probabilities will be equal to one.
# Model Architecture
![](Aspose.Words.fc2a3008-965d-4ee9-bb19-ce199e84f8c7.002.png)
# Model Evaluation
![](Aspose.Words.fc2a3008-965d-4ee9-bb19-ce199e84f8c7.003.png)
# Observations:
- The training accuracy seems to be nearly **~92%**.
- The validation accuracy is nearly **~80%**.
- Though the model accuracy has improved, the **class rebalance** has helped **treat the overfitting to some extent**.
- Much better models could be built or tried out using **more epochs and more layers**.



