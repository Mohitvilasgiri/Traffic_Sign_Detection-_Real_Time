# Traffic_Sign_Detection-_Real_Time

Introduction:
The automotive industry is one of the largest industries in the world. In 2019, ninety-two million motor vehicles were produced in the world, with the United States itself producing over 2.5 million automobiles.With the world moving towards self-driving vehicles, more than 80 companies are testing over 1400 of them in the United States alone. It was forecasted that there would be more than 10 million self-driving cars on road by 2020. This prediction was quite exciting but quite clearly, did not happen. There are numerous reasons behind it.

In today’s world as the number of vehicles is increasing so are the road accidents and according to reports, India is on 1st spot in the greatest number of accidents in a country. This is caused due to many reasons such as poor enforcement of laws, carelessness, etc. One of the reasons is that people don’t recognize or follow 
traffic signboards. So, we have made a traffic sign recognizer which can inform the driver of the vehicle about the traffic sign coming ahead and to follow it. but the main issue is safety. 

Self-driving cars need to identify all the details on the road with extreme precision and accuracy including traffic signs not just for the passenger, but fellow pedestrians as well. We began by studying the dataset at hand. Data pre-processing was done to make the data ready to be used.
Convolutional neural networks are a part of deep learning and are extensively used in image recognition. 
These convolutional neural networks consist of several layers. First, a Conv2D layer is used for feature 
extraction with the help of filters. A number of filters are generally in the power of 2 like 32, 64, or 128. An 
activation function is used in this layer. Generally ReLU(Rectified Linear Unit) activation function is used. 
ReLU function is defined as maximum (0, x).

The max-pooling pooling layer which is used reduce the dimensions of the image. This is done to reduce the 
computation power required for processing the third he image. Third is dropout layer. This dropout layer is 
used to prevent overfitting and to reduce the complexity of the model. In this layer some neurons are 
removed randomly.The combination of first 3 layers is called feature learning phase. These 3 layers are used 
multiple times to improve the training.

The flatten layer which converts the 2-D data into a long 1-D vector of features for a fully 
connected layer that can be fed into the neural network.The last layer is the dense layer which is  Traffic Sign Detection and Recognition System 
SVPCET, Nagpurused as an output layer. The last layer has number of nodes same as the number of classes. The last 
dense layer uses SoftMax activation function. SoftMax function gives the probability value (between 0 and 1) so that the model can predict which class has the highest probability
