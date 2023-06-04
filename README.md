# Practice for 5511 GAN : Monet Painting


*June 2023*


### **Problem Statement**

The objective of this project is to build a GAN that generates 7,000 to 10,000 Monet-style images.



### **Data Source:**

https://www.kaggle.com/c/gan-getting-started/data


The data set includes 7363 files in 4 folders, and the details of each folder is as below:

* monet_jpg - 300 Monet paintings sized 256x256 in JPEG format
* monet_tfrec - 5 TFRecord files (300 Monet paintings sized 256x256 in TFRecord format)
* photo_jpg - 7038 photos sized 256x256 in JPEG format
* photo_tfrec - 20 TFRecord files (7038 photos sized 256x256 in TFRecord format)


### **Methodology**

A GAN will be built for this project. It will be consists of two neural networks: a generator model and a discriminator model.
Two models will work against each other, with the generator trying to trick the discriminator, and the discriminator trying to accurately classify the real vs. generated images.

And finally generate 7,000 to 10,000 Monet-style images with the model built.

By completing this project, we hope to enhance our knowledge of GAN and its applicability in real-world scenarios.

### **Detail steps** 


**1. Exploratory Data Analysis (EDA)** 

Firstly we will explore and visualize the data to understand the structure and distribution of the data.  

**2. Model Training & Evaluation**

Next, we will build GAN with training data set and check the performance on photo dataset. 
Different parameters in downsample() will be tried. 

1. Initialize the random weights for the convolutional layer: initializer = tf.random_normal_initializer(0., 0.02)
2. Enlarge the stdev to 0.2:  initializer = tf.random_normal_initializer(0., 0.2)
3. Change convolutional layer to separable convolutional layer: layers.Conv2D -->  layers.SeparableConv2D

**3. Conclusions**

Finally, we will summarize the results and see what can be improved in the future. 
