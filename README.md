## Image-Captioning
This program is used to create captions for the images that we are feeding to it. It is trained as a Encoder and Decoder program which takes in image tensor as input and passes it on to the decoder along with the descriptions given to it to train. Later the weights of the trained network will be used to predict the image with no captions. The approach is not definitive process, we thought to consider the best steps in the methods that are available first and then we started with the simple approach to build a vision and language network to encode the image, decode the descriptions using RNN.


############ Please run the code in the sequential manner one after another ############

