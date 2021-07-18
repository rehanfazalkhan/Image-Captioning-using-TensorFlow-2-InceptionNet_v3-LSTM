# Image-Captioning-using-TensorFlow-2-InceptionNet_v3-LSTM
                    IMAGE CAPTIONING APPLICATION 

             (Visual Attention , Resnet-50 , Tensorflow 2)


An Image Captioning application takes an image as input and produces a short textual summary describing the content of the photo.


For our application, we start with image files as input and extract their essential features in a compact encoded representation. We will input these to a Sequence Decoder, consisting of several LSTM layers, which will decode the encoded image and predict a sequence of words that describes the photo.



Image Captioning Dataset :

We will use the MS-COCO dataset, preprocess it and take a subset of images using ResNet-51, train an encoder-decoder model, and generate captions on new images using the trained model.

Image files : In “MS-COCO - 2014 Train images “ This folder contains approx 81k images
Captions : In “Train/Val annotation folder” contain approx 415k captions and each image has 5 captions .


Training data pipeline:
We will build the pipeline for our deep learning architecture in two phases.


For the first phase, we use transfer learning to pre-process the raw images with a pre-trained CNN-based network. This takes the images as input and produces the encoded image vectors that capture the essential features of the image. We do not need to train this network further.
We then input these encoded image features, rather than the raw images themselves, to our Image Caption model. We also pass in the target captions corresponding to each encoded image. The model decodes the image features and learns to predict captions that match the target captions.

 Dataset:
Using coco dataset, needs lot of computational power and also time. It's hard to train on Coco dataset as it has 80k images and for each images 5 annotations thats aprox 415k annotations . And also the implementation is hard as there will be some biases in the network. 

And for fliker 8, it requires less computational power. If we are using fliker 8k it's has image 8k image and for annotations 5 per image aprox 41k annotations and we can train our model easily with resNet 18 or inception V3 .

Why Flickr8k dataset…?
It is small in size. So, the model can be trained easily on low-end laptops/desktops...
Data is properly labelled. For each image 5 captions are provided.
The dataset is available for free.

resNet-18 vs. resNet-34
So this graph is a comparison between ResNet-34 and ResNet-18, I think it is best to use ResNet-34 first because it’s 

