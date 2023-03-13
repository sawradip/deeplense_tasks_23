# Common Test I: Multi-Class Classification

## Task

Build a model for classifying the images into lenses using PyTorch or Keras. Pick the most appropriate approach and discuss your strategy.


## Dataset 

Test 1 dataset is available [here](https://drive.google.com/file/d/1B_UZtU4W65ZViTJsLeFfvK-xXCYUhw2A/view)

The Dataset consists of three classes, strong lensing images with no substructure(`no`), subhalo(`sphere`) substructure, and vortex(`vort`) substructure. The images have been normalized using min-max normalization, but you are free to use any normalization or data augmentation methods to improve your results.

###  Example of 'no'
![Example of class no](assets/Class%20-%20no.png)

###  Example of 'sphere'
![Example of class sphere](assets/Class%20-%20sphere.png)

###  Example of 'vort'
![Example of class vort](assets/Class%20-%20vort.png)

## Evaluation Metrics

`ROC curve (Receiver Operating Characteristic curve)`: 
The ROC curve is a graphical plot that shows the performance of a classification model by comparing the trade-off between its true positive rate and false positive rate. It is commonly used to evaluate and compare the performance of different models.


`AUC score (Area Under the ROC Curve)`:
The AUC score (Area Under the ROC Curve) is a scalar metric that summarizes the performance of a binary classification model over all possible classification thresholds. It measures the ability of the model to distinguish between positive and negative classes, with higher values indicating better performance.

## Training Parameters

`Loss`: Cross Entropy

`Optimizer`: Adam

`Learning Rate`: 1e-6 (No scheduler)

`Early Stopping`: On Accuracy(Patience = 5)

# Models: Weights and Summary

All trained model weights and `model.json` files are available here

## Model: resnet18


### ROC curve and AUC
![rersnet18-ROC](resnet18/resnet18%20-%20ROC.png)

### Loss curve
![rersnet18-Loss](resnet18/resnet18%20-%20loss.png)

### Accuracy Curve
![resnet18-Accuracy](resnet18/resnet18%20-%20Accuracy.png)


## Model: resnet26

### ROC curve and AUC
![resnet26-ROC](resnet26/resnet26%20-%20ROC.png)

### Loss curve
![resnet26-Loss](resnet26/resnet26%20-%20loss.png)

### Accuracy Curve
![resnet26-Accuracy](resnet26/resnet26%20-%20Accuracy.png)



## Model: efficientnet_b0

### ROC curve and AUC
![efficientnet_b0-ROC](efficientnet_b0/efficientnet_b0%20-%20ROC.png)

### Loss curve
![efficientnet_b0-Loss](efficientnet_b0/efficientnet_b0%20-%20loss.png)

### Accuracy Curve
![efficientnet_b0-Accuracy](efficientnet_b0/efficientnet_b0%20-%20Accuracy.png)



## Model: convit_tiny

[[Best Weights]()] [[model.json]()]

### ROC curve and AUC
![convit_tiny-ROC](convit_tiny/convit_tiny%20-%20ROC.png)
### Loss curve
![convit_tiny-Loss](convit_tiny/convit_tiny%20-%20loss.png)
### Accuracy Curve
![convit_tiny-Accuracy](convit_tiny/convit_tiny%20-%20Accuracy.png)


# Comments

I have tried models from  different families. While we compare between `resnet18` and `resnet26`, it is clear that increasing the model size often leads to worse results.

While looking at plots of `convit_tiny`, we see that the performance was in the rising trend, and we would have gotten much better results if early stopping had a higher value of patience.

Further exploration can be done:
* Elaborate hyperparameter search
* Training with higher patience of Early Stopping
* Training with different architectures


