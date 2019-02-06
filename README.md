# Virginia-Tech-Machine-Learning-and-Data-Classifiers-Course
# Assignment 1
## For this problem, we want to propose a model that can predict whether a person makes over $50K/yr based on census data of about 32000 people. The data given for each individual includes 1) Age 2) Workclass 3) Financial weight 4) Education 5) Education-num 6) Marital status 7) Occupation 8) Relationship 9) Race 10) Sex 11) Capital gain 12) Capital loss 13) Hour per week 14) Native country 15) Target

 

## Download link for the CSV file: https://bit.ly/2TmsBQo

## Task assignment 1

### Given the 14 attributes, you are going to predict the Target column. The data occasionally has missing values. Moreover, features might be numerical, ordinal or nominal. You can decide how to take care of data preparation. For example, you might opt to drop any rows with missing data or replace them with a special value. You may assign a number to each nominal feature value, but it would mean an implicit ranking where it is not desired, so you may want to investigate other encodings (hint: one hot encoding). Justify the decisions you make for data preparation.

 

### Analyze the data by plotting the distribution of each feature to get a better understanding of the data. Also extract some statistics for each feature, including min, max, mean, median and standard deviation for numerical features. (optional: illustrate summary statistics with box plots) While correlated features generally do not improve performance, they even tend to make matters worse for linear models and make tuning unstable. Explain why this is the case. Moreover, calculate and plot the correlation matrix of features and identify highly correlated features and prune them. Prior to this, you want to use LabelEncoder preprocessing class in scikit-learn to encode categorical features as numbers.

### Perform data preparation. Take care of missing data and scale feature values if needed.

### Split data into train and test sets, by keeping the last 20% samples of each class for the test dataset.

### Fit scikit-learn’s Logistic Regression model on train samples and predict test dataset.The model parameters can be retrieved by inspecting the coef_ attribute of the fitted model. Try to identify the more important features base on the coefficient values.

### Calculate popular performance metrics, including confusion matrix, accuracy, precision, recall, sensitivity, and specificity.

### Use RidgeCV and LassoCV classes to fit regularized linear models on data. Indicate a proper range for CV and use 10-fold CV to find proper regularization factors. Report the performance metrics and investigate feature importance.

### Test SVM on this dataset. A challenge is that in practice an ideal separating hyperplane may not exist due to a large overlap between input data points from the two classes. 
### Report SVM’s performance metrics with a polynomial kernel and the Gaussian and the sigmoid function kernels.
### Evaluate Random Forest on the dataset. Also, report feature importance implied by fitting the model.
### Draw ROC curves for all these models and compare their performance based on this.

# Assignment 2 Clustering

## Part 1) Color quantization is the process of reducing the number of distinct colors for storage or presentation of an image. This is an old topic and has been studied since the 70s. The intention is usually to have the new image visually similar to the original image as much as possible. While historically it was more motivated for the devices with limited memory capacity, nowadays it is mainly used for GIF and PNG image formats. As you might already know, the GIF images can only support up to 256 distinct colors. PNG images have 24-bit (167 million colors) pallet, but can often be made much smaller in file size without much visual degradation by application of color quantization. Here we are going to investigate how a clustering algorithm, here KMeans, can be used for color quantization.

### Numpy, Pillow (for loading images), Scikit-learn and matplotlib are all you need (and allowed) to use.
### Plot the histogram of the original image. That is a bar chart going from 0 to 255, showing the number of pixels in an image that has that value. Obviously, you would want three histograms for the three channels (Red, Green, Blue).
### Perform color quantization for different values of K.
### Plot the compressed images and their corresponding histogram (or optionally the color pallets; as shown below for The Matrix movie).

assignment-Picture1.png

assignment-Picture2.png

 

### Part 2) Image segmentation is the process of partitioning an image into multiple segments, where every pixel is assigned a label such that pixels with the same label share certain characteristics.  Each of the pixels in a region is similar with respect to some characteristic or computed property, such as color, intensity, or texture. Adjacent regions are significantly different with respect to the same characteristics. In this part, we want to develop an algorithm that helps people with color blindness! Use a clustering algorithm of your choice, such as KMeans, to do this task. To find images to test your algorithm, just search “color blindness test images (Links to an external site.)” in Google Images.

assignment-Picture3.png

 

### Notice that the algorithm can struggle with the RGB representation of images. You might stumble upon cases where your algorithm makes matters worse. The picture below depicts such a case:

 

assignment-Picture4.png

 

### One solution you might consider for this is to transform your images from RGB color space YUB or YCrCb (Links to an external site.). Why do you think this transformation is beneficial?

 

assignment-Picture5.png
