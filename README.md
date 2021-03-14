[Machine Learning] Support Vector Machine Classifier To Identify Handwritten
Digits

## Introduction

- The goal of this project is to use SVM Classifier to train a simple system for
    the recognition of handwritten digits and for that MNIST dataset of
    handwritten digits is used for testing and training the system which
    contains 60k images that are sorted as one vector each with their labels.
- There are 7 parts of this projects which has different objectives but finding
    the accuracy is the main goal of the whole system, and there will be
    different size of train data and different size of testing data each time to
    see how the SVM Classifier works and what kind of accuracy it will gain.

## Project methodology, equations and implementations

Python Packages Used: -

- Idx2numpy
- Numpy
- Matplotlib
- Pandas
- Sklearn
- Tabulate

Methodology and Implementations: -

- First of all I have used idx2numpy package to read the "train-images.idx3-
    ubyte" and "train-labels.idx1-ubyte" files as a NumPy array.
- After converting the training images from 3d to 2d as most of the
    classification algorithms works better on 2d arrays and the images file
    contains the (60000,28,28) means 60000 of 28*28 size images. So I have
    converted that into (60000, 784).
- The next step is to initialize the classifier, in our case we are implementing
    the SVM classifier with C value of 20.


- In part 1 we took first 1000 images and its labels as the training dataset and
    from 2000 to 2100, 100 images as testing dataset. And we find the accuracy
    and the confusion matrix.


- In part 2 we take first 10000 images and its label as the training set and
    20000 – 20100, 100 images as a testing dataset. And calculated the
    accuracy and construct a confusion matrix.

- In part 3, we took 10000 images and labels as training dataset and 20000-
    21000, 1000 images and labels as the testing dataset and build the
    confusion matrix and also find the accuracy.

- In part 5, we took first 10000 images and labels as a training set and 20000-
    2 1000, 1000 images as a testing dataset but here we implemented different
    kernel for the SVM which is polynomial and find the accuracy.


- In part 6, we took binary images of different threshold values of 0, 75, 150,
    225 and converted the whole dataset into the binary images with the
    thresholding and tested the classifier on each of them and get the
    comparison table.


- In part 6, Created a comparison table for all the accuracies of each part.

```

│ │ Part │ Accuracy │
╞════╪════════╡
│ 0 │ Part 1 │ 0.91 │
├────┼────────────┤
│ 1 │ Part 2 │ 0.97 │
├────┼────────────┤
│ 2 │ Part 3 │ 0.962 │
├────┼────────────┤
│ 3 │ Part 5 │ 0.952 │
├────┼────────────┤
│ 4 │ TH Val 0 │ 0.956 │
├────┼────────────┤
│ 5 │ TH Val 75 │ 0.953 │
├────┼────────────┤
│ 6 │ TH Val 150 │ 0.947 │
├────┼────────────┤
│ 7 │ TH Val 215 │ 0.93 │

```

# Conclusion

- As from comparison table, it is obvious that part 2’s accuracy is best, and
    the reason is that it took larger dataset and test it on the smaller size. It
    means the larger the data, better the classifier. (Does not mean every time
    because it sometimes overfit).
- From Threshold Values, it is clearly seen that threshold value > 0 is the best
    one because it is already a 28*28 size image which is also a black and white
    image, not every time it will give the best accuracy but, in our dataset, it
    gives so that is best for us.
- As comparing the best accuracy of threshold images and best accuracy of
    normal image datasets, which has the same test and train dataset, we got
    0.006 difference, but I think threshold images will get the better accuracy
    for a greater number of images, so I think for digit recognition with this kind
    of dataset and images, converting it to binary images is a good idea.


**References: -**

**https://pypi.org/project/idx2numpy/**

**https://scikit-learn.org/stable/**

**https://pypi.org/project/tabulate/**


