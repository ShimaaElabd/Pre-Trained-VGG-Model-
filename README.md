# Pre-Trained-VGG-Model

Using The Pre-Trained VGG Model to Classify Objects in Photographs:-
(Develop a Simple Photo Classifier)

1. Get a Sample Image:
First, we need an image we can classify.
2. Load the VGG Model:
Load the weights for the VGG-16 model
3. Load and Prepare Image:
Next, we can load the image as pixel data and prepare it to be presented to the network. Keras provides some tools to help with this step.
First, we can use the load_img() function to load the image and resize it to the required size of 224×224 pixels.
Next, we can convert the pixels to a NumPy array so that we can work with it in Keras. We can use the img_to_array() function for this.
The network expects one or more images as input; that means the input array will need to be 4-dimensional: samples, rows, columns, and channels.
We only have one sample (one image). We can reshape the array by calling reshape() and adding the extra dimension.
Next, the image pixels need to be prepared in the same way as the ImageNet training data was prepared.
4. Make a Prediction
We can call the predict() function on the model in order to get a prediction of the probability of the image belonging to each of the 1000 known object types.
5. Interpret Prediction
Keras provides a function to interpret the probabilities called decode_predictions().
It can return a list of classes and their probabilities in case you would like to present the top 3 objects that may be in the photo. I will just report the first most likely object.
