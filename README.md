## Image-Captioning
This program is created to generate captions for the images that we are feeding to it. It is trained as a Encoder and Decoder program which takes in image tensor as input and passes it on to the decoder along with the descriptions given to it to train. Later the weights of the trained network will be used to predict the image with no captions. The approach is not a definitive process, I thought to consider the best steps in the methods that are available first and then I started with the simple approach to build a vision and language network to encode the image, decode the descriptions using RNN. The exact steps are explained below


######### Please run the code in the sequential manner one after another ##########

* Cleaning and preprocessing the train_test_descriptions
* Image transform defined with the resizing the images, transforming them to tensors normalizing them for all the pixel values 
* Building the vocabulary from the descriptions given 
* Using FreqDist function to find out the frequencies of the words in the dataset
* Removing the words with less than 5 counts 
* Generating distinct numbers for the vocabulary created above
* Finding out the maximum length of the description in the dataset. 
* FormiVC the main vocabulary vc by zipping the numbers generated and vocabulary 
* Adding + 2 to consider the <start> and <end> tag also for the max length
* Loading the image from the directory please give the respective directory 
* Load the images in the variabl imgg 
* Data loader class for the loading images and captions data 
* Encoder Class with resnet 18 model to make it simpler to run 
* Decoder class to decode the captions and generate captions
* Initiating the loader and loading the data
* Initiating the Encoder, embed size, hidden size, loss criterion and optimizer
* Train function to train the data given
* Function to run the train function through the epochs mentioned
* Test Fucntion to generate the image capitons

  
