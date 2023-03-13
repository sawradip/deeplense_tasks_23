# Specific Test II: Lens Finding

## Task

Build a model for classifying the images into lenses using PyTorch or Keras. Pick the most appropriate approach and discuss your strategy.


## Dataset 

Test 2 dataste is available [here](https://drive.google.com/file/d/1eXmbZqUfpqhI-MWz2xkpK0dXQ4FttGQf/view?usp=sharing)


The dataset contains images of two classes, `with` and `without` gravitational lenses.

###  Examples: with Gravitational  Lense
![with_lens](assets/Class%20-%20with_lens.png)

###  Examples: without Gravitational  Lense
![without_lens](assets/Class%20-%20without_lens.png)


## Evaluation Metrics

`ROC curve (Receiver Operating Characteristic curve)`: 
The ROC curve is a graphical plot that shows the performance of a classification model by comparing the trade-off between its true positive rate and false positive rate. It is commonly used to evaluate and compare the performance of different models.


`AUC score (Area Under the ROC Curve)`:
The AUC score (Area Under the ROC Curve) is a scalar metric that summarizes the performance of a binary classification model over all possible classification thresholds. It measures the ability of the model to distinguish between positive and negative classes, with higher values indicating better performance.

## Training Parameters

`Loss`: Mean Square Error

`Optimizer`:Adam

`Lreaning Rate`: 1e-6

`Early Stopping`: On Accuracy(Patience=5)


# Models: Weights and Summary

All trained model weights and `model.json` files are available here

## Model: resnet18

### ROC curve and AUC
![resnet18-ROC](resnet18/resnet18%20-%20ROC.png)
### Loss curve
![resnet18-loss](resnet18/resnet18%20-%20loss.png)
### Accuracy Curve
![resnet18-Accuracy](resnet18/resnet18%20-%20Accuracy.png)


## Model: vit_tiny_patch16_224

### ROC curve and AUC
![vit_tiny_patch16_224-ROC](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20ROC.png)
### Loss curve
![vit_tiny_patch16_224](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20loss.png)
### Accuracy Curve
![vit_tiny_patch16_224](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20Accuracy.png)


## Model: vit_tiny_patch16_224

### ROC curve and AUC
![vit_tiny_patch16_224-ROC](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20ROC.png)
### Loss curve
![vit_tiny_patch16_224](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20loss.png)
### Accuracy Curve
![vit_tiny_patch16_224](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20Accuracy.png)








