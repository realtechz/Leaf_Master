# Leaf-Disease-Classifier

* Leaf Disease Classifier classifies disease based on image processing techniques for automated vision system used at agricultural field. 

* The classifier is trained on the dataset found at
   * https://www.kaggle.com/emmarex/plantdisease
   * https://github.com/spMohanty/PlantVillage-Dataset
* You can find model weights here:
   * Model with weights : https://drive.google.com/file/d/1al0dZHeRtE0EqdEBbSaUQbTLUdEPKqJb/view?usp=sharing
   * Only weights : https://drive.google.com/file/d/1al0dZHeRtE0EqdEBbSaUQbTLUdEPKqJb/view?usp=sharing 

# Deep Dive into Concepts
- [Disease Classifier](##DiseaseClassifier)
- [How To Train](##HowToTrain)
- [Run Model](##RunModel)

## Disease Classifier

The whole disease classification process is divided into 2 stages as in 

- 8 CNN classifiers are trained to identify the diseases of each of the 8 plant classes.  The result from stage 2 is used to call the classifier that has been trained to classify the different diseases for that plant. If there are none, the leaf would be classified as 'Healthy'.

<img src="./images/subClasses.png" width="800" height="400">

- All the above CNN's are trained on a Deep Residual Network- ResNet-50 Architecture using "Transfer Learning" from the ImageNet weights.

[//]: # (<img src="./images/resnetACC.png" width="400" height="200">)

- Frameworks used : Keras


# How-To-Train:
- Every leaf has its own model so you can train them sperately and test them.
- there is a main classifier model which will take time to train.
- quick tip delete the model from the model folder to train.

## Run Model
- Download weights from links given
- place them in a folder Best_model and Best_weights
- To run and setup the model, you’ll need at least OpenCV 3.4.2.
- Every thing is in one file show just run all cells
