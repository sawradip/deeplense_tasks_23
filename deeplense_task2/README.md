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

All trained model weights and `model.json` files are available [here](https://drive.google.com/drive/folders/10s6qrFXgs_4UHfN0Grh3XgWXEAGwOjac?usp=sharing).

| Model Name | AUC | Accuracy |
|------------|-----|----------|
| convit_tiny   | 0.9114 | 83.00  |
| vit_tiny_patch16_224    | 0.8973 | 81.61     |
| rersnet18    | 0.8604 | 80.55    |
| efficientnetv2_s | 0.5677| 68.05  |



## Model: convnext_pico

### ROC curve and AUC:
![convnext_pico-ROC](convnext_pico/convnext_pico%20-%20ROC.png)
### Loss curve:
![convnext_pico-loss](convnext_pico/convnext_pico%20-%20loss.png)
### Accuracy Curve:
![convnext_pico-Accuracy](convnext_pico/convnext_pico%20-%20Accuracy.png)


## Model: vit_tiny_patch16_224

### ROC curve and AUC:
![vit_tiny_patch16_224-ROC](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20ROC.png)
### Loss curve:
![vit_tiny_patch16_224-loss](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20loss.png)
### Accuracy Curve:
![vit_tiny_patch16_224-Accuracy](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20Accuracy.png)


## Model: resnet18

### ROC curve and AUC
![resnet18-ROC](resnet18/resnet18%20-%20ROC.png)
### Loss curve
![resnet18-loss](resnet18/resnet18%20-%20loss.png)
### Accuracy Curve
![resnet18-Accuracy](resnet18/resnet18%20-%20Accuracy.png)


## Model: efficientnetv2_s

### ROC curve and AUC
![efficientnetv2_s-ROC](efficientnetv2_s/efficientnetv2_s%20-%20ROC.png)
### Loss curve
![efficientnetv2_s-loss](efficientnetv2_s/efficientnetv2_s%20-%20loss.png)
### Accuracy Curve
![efficientnetv2_s-Accuracy](efficientnetv2_s/efficientnetv2_s%20-%20Accuracy.png)


# Comments

We see that, `convnext_pico` have performed bestamong the models. But it has achieved a AUC  score of 0.9114. The second best one is `ViT` models that achieves 0.8973. So, it can be said that these types of models, specifically Transformer architectures might work betteron this dataset.

From the highest achieved accuracy, we can come to a decision that thisdataset is comparatively hasrder to classify, and there is a lot room for improvement.


Further exploration can be done:
* Add an image brightness term to the Loss function, that might  have direct relation  with the  result.
* Experiment with LR Scheduler.







