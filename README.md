# 2017-2MachineLearningProject

# Using Convolution Neural Network to classify distracting driver's posture.
----------------------------------------------------------------------------
# Abstract
----------------------------------------------------------------------------
Distracted driving habit is the biggest problem around the world. It causes many accidents and human disasters. To solve this problems, in this paper, I used the Kaggle dataset for “distracted driver” posture images with more distraction features than safe driving features. So I used machine learning method to identify driver’s posture while driving. Driver’s image has 10 classes which are drinking picture, texting posture, talking on the phone posture etc. My system used a supervised learning with general Convolutional Neural Networks (CNNs) and Softmax classification to classify this images into 10 classes. In this paper, this system shows 12% classification accuracy method. 

# DataSet
----------------------------------------------------------------------------
Kaggle,
The data structure is as follows. The image of the total of 22424 driver’s driving is the 10 classifications. Image size is 640 * 480 pixels jpeg file. There are about approximately 2100 images according to each class. Each classes represent safe driving, texting with right-hand, talking on the phone with right-hand, texting with left-hand, talking on the phone with left-hand, operating the radio, drinking, reaching behind, hair and makeup, talking to passenger. Drivers are 100 persons.

# Data Preprocess & Training
----------------------------------------------------------------------------
+ •	I cut all  640 X 480 pixel  22424 images to 480 X 480 pixel images and resized to 192 X 192 pixel images. (Data Preprocessing)
+ •	I made 5 training network layers consisted of 3X3 8 filters, convolution layer, relu function, 2X2 kernel size max pooling and drop out(keep probability = 80%). Each training network layer, number of filter increases twice. Initialized number is 8.
+ •	I made 2 fully connected layers used classify images to their label. I used Adam Optimizer to minimize cost and softmax cross entropy to check costs. Accuracy function is comparing label’s argumax value and machine’s calculated arguma value.
+ •	In training settings, learning rate is 0.01, data batch size is 100, 10 training epochs which means how many times to train all data.

# Result
----------------------------------------------------------------------------
+ •	I tested this model so many times but its result shows that its classification accuracy is 10% ~ 12%.
