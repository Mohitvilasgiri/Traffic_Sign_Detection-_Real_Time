# Traffic_Sign_Detection-_Real_Time

## Introduction:
The automotive industry is one of the largest industries in the world. In 2019, ninety-two million motor vehicles were produced in the world, with the United States itself producing over 2.5 million automobiles.With the world moving towards self-driving vehicles, more than 80 companies are testing over 1400 of them in the United States alone. It was forecasted that there would be more than 10 million self-driving cars on road by 2020. This prediction was quite exciting but quite clearly, did not happen. There are numerous reasons behind it.

In today’s world as the number of vehicles is increasing so are the road accidents and according to reports, India is on 1st spot in the greatest number of accidents in a country. This is caused due to many reasons such as poor enforcement of laws, carelessness, etc. One of the reasons is that people don’t recognize or follow 
traffic signboards. So, we have made a traffic sign recognizer which can inform the driver of the vehicle about the traffic sign coming ahead and to follow it. but the main issue is safety. 

Self-driving cars need to identify all the details on the road with extreme precision and accuracy including traffic signs not just for the passenger, but fellow pedestrians as well. We began by studying the dataset at hand. Data pre-processing was done to make the data ready to be used.convolutional neural networks are a part of deep learning and are extensively used in image recognition. These convolutional neural networks consist of several layers. First, a Conv2D layer is used for feature extraction with the help of filters. A number of filters are generally in the power of 2 like 32, 64, or 128. An activation function is used in this layer. Generally ReLU(Rectified Linear Unit) activation function is used.ReLU function is defined as maximum (0, x).

The max-pooling pooling layer which is used reduce the dimensions of the image. This is done to reduce the computation power required for processing the third he image. Third is dropout layer. This dropout layer is used to prevent overfitting and to reduce the complexity of the model. In this layer some neurons are removed randomly.The combination of first 3 layers is called feature learning phase. These 3 layers are used multiple times to improve the training.

The flatten layer which converts the 2-D data into a long 1-D vector of features for a fully connected layer that can be fed into the neural network.The last layer is the dense layer which is used as an output layer. The last layer has number of nodes same as the number of classes. The last dense layer uses SoftMax activation function. SoftMax function gives the probability value (between 0 and 1) so that the model can predict which class has the highest probability.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Literature Survey

Extensive research has been done in the area of recognition and classification of traffic and road signs. The authors proposed a Convolutional Neural Network and Support Vector Machines (CNN-SVM) method for traffic signs recognition and classification. The coloring used in this method is YCbCr color space which is input to the convolutional neural network to divide the color channels and extracting some special characteristics. 
Their proposed method achieved a 98.6% accuracy for traffic signs recognition and classification. In another model the authors developed a new dataset consisting of 100,000 images and also proposed a traffic sign detection and classification method based on a robust end-to-end CNN. The method achieved 84% accuracy. 
The authors analyzed the spatial transformers and stochastic optimization methods for deep neural network for traffic sign recognition. They finalized this with a proposed system that achieved 99.71% accuracy. 

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Implementation:
In this Project we create Traffic sign Detection Model. Using Traffic sign Detection Model, we can inform 
the driver of the vehicle about the traffic sign coming ahead. 
Project Setup 
The dataset is plot into training, test and validation sets, with the following characteristics: 
           • Images are 32 (width) x 32 (height) x 3 (RGB color channels) 
           • Training set is composed of 34799 images 
           • Validation set is composed of 4410 images 
           • Test set is composed of 12630 images 
           • There are 43 classes (e.g., Speed Limit 20km/h, No entry, bumpy road, etc.) Moreover, we 
              will be using Python 3.7 with TensorFlow to write our code. 
        
### Pre-Processing :

        1) Input the image.
        2) Image Resizing:- One of the limitations of the CNN model is that they cannot be trained on a different
        dimension of images. So, it is mandatory to have same dimension images in the dataset. 
        We’ll check the dimension of all the images of the dataset so that we can process the images into having 
        similar dimensions(32*32*3).
        3) Image Grayscale: We convert our 3 Channel images into a single grayscale image.  
        4) Image Equalization: - It standardize the lighting in a image. 
        5) Image Normalization: - To Normalized Value between 0 and 1 instead of 0 to 255.
        
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------### Model Architecture:

For building the we will use sequential model from keras library. Then we will add the layers to make convolutional neural network. In the first 2 Conv2D layers we have used 32 filters and the kernel size is (5,5). In the MaxPool2D layer we have kept pool size (2,2) which means it will select the maximum value of every 
2 x 2 area of the image. By doing this dimension of the image will reduce by factor of 2. In dropout layer we have kept dropout rate = 0.25 that means 25% of neurons are removed randomly. We apply these 3 layers again with some change in parameters. Then we apply flatten layer to convert 2-D data to 1-D vector. This layer is followed by dense layer, dropout layer and dense layer again. The last dense layer outputs 43 nodes as the traffic signs are divided into 43 categories in our dataset. This layer uses the SoftMax activation function which gives probability value and predicts which of the 43 options has the highest probability.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------### Apply the model and plot the graphs for accuracy and loss:
We will compile the model and apply it using fit function. The batch size will be 32. Then we will plot the graphs for accuracy and loss. We got accuracy of 98.5%.
![image](https://user-images.githubusercontent.com/66352630/126447117-996d3b14-fec8-4201-a664-9360aab979f4.png)




