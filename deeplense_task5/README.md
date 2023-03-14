# Specific Test V: Exploring Transformers

## Task

Use a vision transformer method of your choice to build a robust and efficient model for binary classification or unsupervised anomaly detection on the provided dataset. In the case of unsupervised anomaly detection, train your model to learn the distribution of the provided strong lensing images with no substructure. Please implement your approach in PyTorch or Keras and discuss your strategy.


## Dataset 

Test 2 dataste is available [here](https://drive.google.com/file/d/16Y1taQoTeUTP5rGpB0tuPZ_S30acvnqr/view?usp=sharing)

A set of simulated strong gravitational lensing images with and without substructure.
The dataset contains images of two classes, `sub`and `no_sub`.

###  Examples: sub
![sub](assets/Class%20-%20sub.png)

###  Examples: no_sub
![no_sub](assets/Class%20-%20no_sub.png)

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

All trained model weights and `model.json` files are available [here](https://drive.google.com/drive/folders/12tS1sQV4oSi5MUdAU9QNgWkxgwGZPZhl?usp=sharing).

| Model Name | AUC | Accuracy |
|------------|-----|----------|
| gcvit_tiny    | 0.9954 | 97.4    |
| swin_s3_tiny_224   | 0.9952 | 96.3  |
| vit_tiny_patch16_224    | 0.9938 | 96.2     |
| convit_tiny | 0.9901| 95.6  |



## Model: gcvit_tiny

### ROC curve and AUC:
![gcvit_tiny-ROC](gcvit_tiny/gcvit_tiny%20-%20ROC.png)
### Loss curve:
![gcvit_tiny-loss](gcvit_tiny/gcvit_tiny%20-%20loss.png)
### Accuracy Curve:
![gcvit_tiny-Accuracy](gcvit_tiny/gcvit_tiny%20-%20Accuracy.png)

## Model: swin_s3_tiny_224

### ROC curve and AUC:
![swin_s3_tiny_224-ROC](swin_s3_tiny_224/swin_s3_tiny_224%20-%20ROC.png)
### Loss curve:
![swin_s3_tiny_224-loss](swin_s3_tiny_224/swin_s3_tiny_224%20-%20loss.png)
### Accuracy Curve:
![swin_s3_tiny_224-Accuracy](swin_s3_tiny_224/swin_s3_tiny_224%20-%20Accuracy.png)

## Model: vit_tiny_patch16_224

### ROC curve and AUC:
![vit_tiny_patch16_224-ROC](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20ROC.png)
### Loss curve:
![vit_tiny_patch16_224-loss](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20loss.png)
### Accuracy Curve:
![vit_tiny_patch16_224-Accuracy](vit_tiny_patch16_224/vit_tiny_patch16_224%20-%20Accuracy.png)


## Model: convit_tiny

### ROC curve and AUC
![convit_tiny-ROC](convit_tiny/convit_tiny%20-%20ROC.png)
### Loss curve
![convit_tiny-loss](convit_tiny/convit_tiny%20-%20loss.png)
### Accuracy Curve
![convit_tiny-Accuracy](convit_tiny/convit_tiny%20-%20Accuracy.png)


# Comments

I have tried 4 different kinds of Transformers to  observe performance. It seels that all the models do well, but `gcvit` is performing best among them. 
While working  on the actual project, we can analyse the difference between these model architectures, and decide which tweaks inside the model leads to better performance.


Further exploration can be done:
* Trying more families of Visual Transformer models.
* Checking the gain in performance while increasing the size of the same model archetwcture.

