# Object-Localization-with-TensorFlow
This project focuses on predicting the correct class of an emoji and identifying its accurate location through bounding box coordinates. The images used in training and testing are synthetically generated using the emojis from OpenMoji.
<br><br>
Coursera Guided Project: [Object Localization with TensorFlow](https://www.coursera.org/projects/object-localization-tensorflow) 
<br>
All emojis are designed by [OpenMoji](https://openmoji.org/) – the open-source emoji and icon project. License: CC BY-SA 4.0

![openmoji-750x421](https://github.com/user-attachments/assets/5200a7ea-5c0c-4888-9606-da09cd6cfd09)

## Key Steps
### Create Samples
Create a synthetic image (144 x 144) by randomly selecting an emoji (72 x 72) and placing it randomly on the white background.

### Plot Bounding boxes
Given (x, y) coordinates, plot the bounding box surrounding the emoji.

### Generate data
Generate a batch of images and labels of the given batch size.

### Metrics
Intersection over union (IOU) is considered for a given pair of actual and predicted bounding box coordinates to assess the accuracy of the bounding box coordinates prediction.

### Training
Used a custom learning rate scheduler that divides the current learning rate by 5 at each fifth epoch that is capped at the minimum of 3e-7.

### Testing
Create a set of validation samples using the data generator after each epoch and test the model that has been trained so far.
> Achieved a final IOU score of 0.407 and a classification accuracy of 1.0 for the classes.
