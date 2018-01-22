## Exoplanet Hunting in Deep Space
The data describe the change in flux (light intensity) of several thousand stars. Each star has a binary label of 2 or 1. 2 indicated that that the star is confirmed to have at least one exoplanet in orbit; some observations are in fact multi-planet systems.

As you can imagine, planets themselves do not emit light, but the stars that they orbit do. If said star is watched over several months or years, there may be a regular 'dimming' of the flux (the light intensity). This is evidence that there may be an orbiting body around the star; such a star could be considered to be a 'candidate' system. Further study of our candidate system, for example by a satellite that captures light at a different wavelength, could solidify the belief that the candidate can in fact be 'confirmed'.

DATASET = https://www.kaggle.com/keplersmachines/kepler-labelled-time-series-data

## Description
- LABEL -> 2 is an exoplanet star and 1 is a non-exoplanet-star.
- FLUX1-FLUX3197 -> the light intensity recorded for each star, at a different point in time.

**Trainset:**

- 5087 rows or observations.
- 3198 columns or features.
- Column 1 is the label vector. Columns 2 - 3198 are the flux values over time.
- 37 confirmed exoplanet-stars and 5050 non-exoplanet-stars.

**Testset:**

- 570 rows or observations.
- 3198 columns or features.
- Column 1 is the label vector. Columns 2 - 3198 are the flux values over time.
- 5 confirmed exoplanet-stars and 565 non-exoplanet-stars.

## Algorithm (3-layered NN):
**Steps:**
- Get the train and test data.
- Normalize the data.
- Define the neural network structure i.e. get the no. of nodes of each layer.
- Randomly initialize the weights and parameters of all the layers (0.01).
- Forward propagation.
- Compute cost function.
- Backward propagation.
- Update the weights and baises (Gradient descent).
- Model() for combining forward_prop,compute_grap,backward_prop,update_weh.
- Predict the values for train and test set using updated weights.
- Calculate the accuracy on Train and test set.

### Defining Neural network structure:
This would consist of 3 layers (excluding input layer) i.e 2-hidden layer and 1-output layer. Each ***hidden layer***=**12 nodes** and ***output layer*** = **1 node**. Hidden layers will use **tanh()** as activation function and output layer will use **sigmoid()**