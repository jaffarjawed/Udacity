# Dog_Breed_Classifier
# Project Overview
<p>
  Welcome to the dog classifier project. This project uses Convolutional Neural Networks(CNNs). In this project, I build a pipeline to process a real-world, user-supplied images.Given an image of a dog, your algorithm will identify an estimate of the canine's breed. If supplied an image of a human, the code will identify the resembling dog breed
</p>

![doggy](https://user-images.githubusercontent.com/23507650/80122607-647c7000-85ab-11ea-8cee-f640fade2858.jpg)


# Instructions
1. Clone the repository and navigate to the downloaded folder.
!git clone https://github.com/jaffarjawed/Dog_Breed_Classifier.git

# Download dataset
1. Download the <a href = 'https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip'>Dog Dataset</a><br/>
1. Download the <a href = 'https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip'>Human Dataset</a><br/>

# Requirements
1. Tensorflow<br />
2. Keras<br />
3. Sklearn<br />
4. OpenCV<br />
5. PIL<br />


# CNN Structures (Building a model on my own)
(conv1): Conv2D(32, (3, 3), input_shape = (224, 224, 3),activation = 'relu'))<br />
activation: relu<br />
(pool): MaxPooling2D(pool_size = (2, 2)))<br />
activation: relu<br />
(conv2): Conv2D(64, (3, 3), activation = 'relu'))<br />
activation: relu<br />
(pool): MaxPooling2D(pool_size = (2, 2)))<br />
(conv3): Conv2D(128, (3, 3), activation = 'relu'))<br />
(pool): MaxPooling2D(pool_size = (2, 2)))<br />
(conv3): Conv2D(256, (3, 3), activation = 'relu'))<br />
(fc2): Linear(in_features=500, out_features=133, bias=True)

# Summary
There are several state of the arts model we tried. First I gave to shot to OpenCv but it fails when we don't have forward facing faces.
Then I tried convolutional Neural Network from scratch with above parameters.It gave an accuracy of 9% which is too low. At last i tried two state of the arts pre-trained model VGG16 and Xception. VGG16 gave an accuracy of 43% where as Xception gave an accuracy of 81.9% of validation dataset with 20 epochs and about 30 sec of training on GPU.

