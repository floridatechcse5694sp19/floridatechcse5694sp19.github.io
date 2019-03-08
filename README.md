## Welcome to our Group Project website!

### Project 1: Sensor fusion model based on a Bayesian Network


#### Project Description

For this project, our team set out to create a way to fuse the NAO robot's sonar and landmark detection capabilities to determine its orientation in a 20 by 20 inch square, defined by the distance away from the wall it would predominanty face. We sought to accomplish using a sensor fusion technique, based on a Bayesian Network carefully developed over the past few weeks. Currently, have an initial Bayesian Network design for handling the sensor fusion. We have additionally defined random variables that can be observed in our Conditional Probability Tables (CPTs) for each node in the Bayesian Network. These CPTs allow us to input sensor values, from the Nao's Left and Right Sonar sensors along with its Landmark Detection capabilities, to accurately infer its distance from a given wall.

##### Data Collection

Data was collected over 11 independent trials, each containing different orientations regarding the NAO's body and head. The body was either placed straight in front of the Right, Center (straight orientation by the convention of our source code and data), or Left walls, where the position was varied in increments of 2 inches defined by the 20 by 20 inch square, with a 6 inch offset from each wall.



The code for collecting the data from the robot can be found here: https://raw.githubusercontent.com/floridatechcse5694sp19/WallBayesianNetwork/master/csvwriter.py .
