# DecisionTree
Clustering with Decision Tree and SVM on a MNIST dataset based on python

The dataset used in this project is the MNIST dataset, which contains 70,000 black and white images of the digits 0 to 9, which are distributed evenly across 10 different classes, so that each class represents one of the digits. Each image has dimensions of 28 by 28 pixels, and each pixel has a value between 0 and 255, which indicates its color intensity.

The first phase is Image Filtering. In this phase, a single-channel convolution process and a Sobel filter are applied to the images in the dataset. After applying them, the ready-made hog function is also applied to the images. 

The second phase is Image Centering and PCA. In this phase, the images are first centered, then their dimensions are reduced by PCA. 

The third phase is Decision Tree Hyperparameter Tuning. Grid search is used to improve the performance of the decision tree, and K-fold cross-validation is used to prevent overfitting. 

The fourth phase analyzes the accuracy of the model. Three criteria, Precision, Recall, and F1-Score, are used. The results are also displayed by creating a confusion matrix and visualizing it as a Heatmap. 

In the fifth phase, the pre-pruning technique is used to prevent overfitting.
