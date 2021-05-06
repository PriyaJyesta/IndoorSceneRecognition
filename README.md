# IndoorSceneRecognition
### INTRODUCTION: 
Indoor scene recognition is a challenging open problem in high level vision. Most scene recognition models that work well for outdoor scenes perform poorly in the indoor domain. The main difficulty is that while some indoor scenes (e.g., corridors) can be well characterized by global spatial properties, others (e.g., bookstores) are better characterized by the objects they contain. More generally, to address the indoor scenes recognition problem we need a model that can exploit local and global discriminative information.
For instance, for a robot operating in indoors it is helpful to be aware whether it is in a kitchen, a hallway or a bedroom. It's approaches attempt to classify the scene based on 2D images. And, also it can be used for applications which can help visually impaired people to identify the scene and help them navigate. From Application point of view, it is useful for content based image reterival.

### AIM: 
The aim of the project is to build an Indoor scene recognition model using CNN network to detect the indoor scenes from the available dataset.

### DATASET:
The Dataset has 67 categories like bedroom, kitchen, garage, game room, airport, salon etc. and each category has at least 100 images and 15,687 RGB images totally. The size of the data is 2GB. 
All these images are in jpg format.  All of 67 categories of indoor scene image will be used to train the models.
Source : http://web.mit.edu/torralba/www/indoor.html  

### PLANNED FRAMEWORK:
Overall framework of the indoor scene classification method will be based on CNN feature. There will be two parts in the framework. The first part is to generate scene category features by CNN feature extraction and process. The second step is to match CNN feature vector of the test scene image with the scene category features by a new feature matching algorithm to generate scores of different scenes. The largest score indicates the result of scene classification.

### ResNet
A residual network (ResNet), is an artificial neural network that helps to build deeper neural network by utilizing skip connections or shortcuts to jump over some layers. It's skipping helps build deeper network layers without falling into the problem of vanishing gradients. 
There are different versions of ResNet, including ResNet-18, ResNet-34, ResNet-50, and so on. The numbers denote layers, although the architecture is the same. I have used the 18 layer ResNet18 in this project.
ResNet Blocks
There are two main types of blocks used in ResNet:
Identity Block: When the input and output activation dimensions are the same. 
Convolution Block: When the input and output activation dimensions are different from each other.
*TRANSFER LEARNING WITH PYTORCH*
The main aim of transfer learning (TL) is to implement a model quickly. To solve the current problem, instead of creating a DNN (dense neural network) from scratch, the model will transfer the features it has learned from the different dataset that has performed the same task. This transaction is also known as knowledge transfer.

Implementation and Results from ResNet
Added a fully-connected layer for classification, specifying the classes and number of features and also tunned the parameters.

The model has an accuracy of 78%, and it predicts the scenes correctly.

