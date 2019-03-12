## Welcome to our Group Project website!

### Project 1: Sensor fusion model based on a Bayesian Network


#### Project Description

For this project, our team set out to create a way to fuse the NAO robot's sonar and landmark detection capabilities to determine its orientation in a 20 by 20 inch square, defined by the distance away from the wall it would predominanty face. We sought to accomplish using a sensor fusion technique, based on a Bayesian Network carefully developed over the past few weeks. Currently, have an initial Bayesian Network design for handling the sensor fusion. We have additionally defined random variables that can be observed in our Conditional Probability Tables (CPTs) for each node in the Bayesian Network. These CPTs allow us to input sensor values, from the Nao's Left and Right Sonar sensors along with its Landmark Detection capabilities, to accurately infer its distance from a given wall.

##### Data Collection

Data was collected over 11 independent trials, each containing different orientations regarding the NAO's body and head. The body was either placed straight in front of the Right, Center (straight orientation by the convention of our source code and data), or Left walls, where the position was varied in increments of 2 inches defined by the 20 by 20 inch square, with a 6 inch offset from each wall.

The code for collecting the data from the robot can be found here: https://raw.githubusercontent.com/floridatechcse5694sp19/WallBayesianNetwork/master/csvwriter.py.

Additionally, the sensor data can be found in CSV format here: https://github.com/floridatechcse5694sp19/WallBayesianNetwork/tree/master/sensor_data.

##### Bayesian Network and CPTs for the Sensor Fusion Model

After researching effective techniques of sensor fusion, we found that the ideal sensor fusion model for this project would be a simple, parallel network, where the left and right sonars, along with the landmark detector, would be the sensors, and the distance and orientation would be represented as the centralized fusion node. The generalized representation is presented in chapter 3, page 34 of H.B. Mitchell's Multi-Sensor Data Fusion [1]. 

For each of the sonars, the CPTs were modelled based on a single-variable Normal distribution for each distance away from each wall. The decision for using this distribution was due to the large number of samples collected from each distance coordinate away from the wall (about 700 each from each individual distance coordinates away from the center wall orientation, for example), allowing for the assumption that the Central Limit Theorem would hold. In effect, the probability of a given measurement, given the distance coordinate away from a given wall, is determined through putting it into the probability density function for each distance coordinate per wall orientation. The code for generating the CPTs, along with the CPTs (stored in CPTs.zip) can be found in our repository here: https://github.com/floridatechcse5694sp19/WallBayesianNetwork.

Currently, the sensor fusion process to determine the distance coordinate from the wall can be found here: https://raw.githubusercontent.com/floridatechcse5694sp19/WallBayesianNetwork/master/sensor_fusion.py. 
