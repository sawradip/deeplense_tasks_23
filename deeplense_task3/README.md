# Specific Test III: Learning Mass of Dark Matter Halo 

## Task

Using the provided dataset implement a regression algorithm to learn the mapping between lensing images and the lensing dark matter halo mass. You can use the machine learning algorithm of your choice.  Please implement your approach in PyTorch or Keras and discuss your strategy.


## Dataset 

Test 3 dataste is available [here](https://drive.google.com/file/d/1hu472ALwGPBcTCXSAM0VoCWmTktg9j-j/view)


The data set consists of strong lensing images for cold dark matter with subhalo substructure. For each lensing image the corresponding fraction of mass in dark matter substructure is provided.

###  Examples: Dark Halo Mass
![Dark Halo Mass](assets/Dark%20Matter%20Halo%20mass.png)


## Evaluation Metrics

`MSE (Mean Square Error)`: 
It is a commonly used loss function in deep learning that measures the average squared difference between the predicted and actual values. It is differentiable and convex, making it suitable for optimization through gradient descent-based algorithms.

## Training Parameters

`Loss`: Mean Square Error

`Optimizer`:Adam

`Lreaning Rate`: 1e-6

`Early Stopping`: On MSE(Patience=5)


# Models: Weights and Summary

All trained model weights and `model.json` files are available here

| Model Name | MSE | Normalized RMSE |
|------------|-----|----------|
| resnet18    | 5.87e-05 | 0.1618     |
| resnet26    | 8.39e-05 | 0.201     |
| convnext_pico    | 2.14e-04| 0.352     |

## Model: resnet18

### Mean Square Error curve:
![resnet18-MSE](resnet18/resnet18%20-%20MSE.png)

### Normalized Root Mean Square Curve:
![resnet18-NRMSE](resnet18/resnet18%20-%20NRMSE.png)


## Model: resnet26

### Mean Square Error curve:
![resnet26-MSE](resnet26/resnet26%20-%20MSE.png)

### Normalized Root Mean Square Curve:
![resnet26-NRMSE](resnet26/resnet26%20-%20NRMSE.png)


## Model: convnext_pico

### Mean Square Error curve:
![convnext_pico-MSE](convnext_pico/convnext_pico%20-%20MSE.png)

### Normalized Root Mean Square Curve:
![convnext_pico-NRMSE](convnext_pico/convnext_pico%20-%20NRMSE.png)


# Comments

Though we get best performance with `resnet18` , the training curves show  that losses were at decreasing trend, thus longer training with higher patience willlead to better results.

Further exploration can be done:
* Adding some part to the loss function related to pixel brightness, or number of pixels over a certian treshold value, as existance of a larger Halo mass, would lead to larger  gravitational lensing. It should improve the performance.
* Elaborate hyperparameter search
* Training with higher patience of Early Stopping
* Training with different architectures







