# MONAI-Model-Analysis-for-Diesesed-Brain-Image-Classification-
The notebook contains code adapted from MONAI to classify images of healthy and diseased brain's in grayscale. The notebook uses three different classification models and compares the results.
# Overview 
Within this Mini-Project adapted code was used to compare classification results from three different models. A SENet model, an EfficientNetBN model, and a DenseNet121 model.
# Procedure 
The majority of this code was adapted from the MONAI tutorial. In this tutorial, the necessary libraries are imported alongside the data. The data must be uniform to get accurate results, this involved making sure they are all the same size with the same amount of objects in them, in this case, each image has four smaller mages of brain and they are all in grayscale. The data was then split into Train, Test, and Validation sets. A transformer was created and applied to the models. Models themselves needed to be created. The three chosen were a SENet model, an EfficientNetBN model, and a DenseNet121 model. Each has slightly different inputs but the important ones that were specific to the images themselves were the following.
* spatial_dims = 2, each image is 2 dimensional 
* in_channels = 4, 4 different classifications need to be made per image
* out_channels or num_classes = 2, the possible classifications, in this case, tumor or no tumor for the brain image.
Models were then trained and the loss and best value metric was computed after 10 total epochs on each model. A loss curve was created and the final step was producing a confusion matrix of the results for display.

# Results 
* DenseNet: Loss: 0.3853, best val metric: 0.9845 at epoch 7. 93% accurate on Healthy, 92% accurate on Tumour.
* EfficientNet: Loss: 0.6555, best val metric: 0.6649 at epoch 8. 69% accurate on Healthy, 71% accurate on Tumour.
* SENet: Loss: 0.4422, best val metric: 0.9536 at epoch 10. 99% accurate on Healthy, 90% accurate on Tumour.
