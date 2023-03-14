# DEEPLENSE Tasks for GSOC'23 - by Sawradip

Hello and welcome to my GitHub repository that contains pre-requisite tasks for Deeplense project under [ML4SCI](https://ml4sci.org/) at Google Summer of Code 2023.

## About Me

I'm a Sawradip Saha, currently a Mechanical Engineering undergraduate student at Bangladesh University of  Engineering & Technology.I have a strong passion for Deep Learning and have been working on several projects in this field, including IEEE Video and Image Processing  Cup (Champion at 2021 and 2nd Runners up at 2022). I'm been working about 3 years in the field of Deep Learning based Computer Vision and primarily work using Pytorch (also familiar with Keras).

As someone with a deep interest in astronomy, I have studied the phenomenon of gravitational lensing extensively. I am familiar with the theoretical concepts behind it as well as the practical applications in observational astronomy. This background has prepared me well for the DeepLense project, and I am excited to contribute my expertise to the team.

## How to Evaluate models



`Step 1`: Pretrained weights and `model.json` files for all the tasks are available  [here](https://drive.google.com/drive/folders/1CsK2pvhiGBTdQaFJLR_aE3EjoCOAtoc3?usp=sharing).  Download the corresponding  files for the model you want to eavaluate.

`Step 2`: Open the notebook, initial  2-3  cells of every notebooks are for downloading and extracting data in a specific folder(`test_n`) in the nottebook directory. Skip these if you already data, and change the data folder path in appropriate places..

`Step 3`: Run the notebook from top upto  defining the `Trainer `class. No need to run the training block.

`Step 4`:  Skip the `Training` cell, and move to `Evaluation` cell.Replace the `model_name`, `json_path` and `weight_path` in the next cell. Now, run the next cells, and  it will plot the Evaluation metrics as   well as training curves for corresponding model.

## My Contibutions:

* I have created a very flexible training and testing pipeline, that uses [pytorch Timm](https://github.com/huggingface/pytorch-image-models)  as backend. So, we can test hundreds of computer-vision model.

* Clean and minimal training metrics logging in `model.json` file.

* Easy saving, loding  model as well as resuming training.

* The pipeline is easily extensible with any Loss function and optimizers, can be  used for  classification, regression as well as object  detection(yet to extend).

* Provided multi-model ablation study for each task, and organized plots of various training parameters.

* Can run the notbooks in Google Colab or any environment. Data downloading and other setups are done in notebook.


## Tasks Summary
### Common Test I: [Multi-Class Classification](deeplense_task1) (Common)

`Task`: Build a model for classifying the images into lenses using PyTorch or Keras. Pick the most appropriate approach and discuss your strategy.

| Model Name | AUC | Accuracy |
|------------|-----|----------|
| rersnet18    | 0.9924 | 0.85    |
| resnet26    | 0.5528 | 0.75     |
| efficientnet_b0 | 0.9704| 0.90  |
| convit_tiny   | 0.8826 | 0.1618  |

The notebook can be  also used with Google Colab:
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sawradip/deeplense_tasks_23/blob/main/deeplense_task1/Task1_updated.ipynb)

### Specific Test II: [Lens Finding](deeplense_task2)

*Those interested in the Lens Finding Project should complete Test II.*

`Task`: Build a model for classifying the images into lenses using PyTorch or Keras. Pick the most appropriate approach and discuss your strategy.

| Model Name | AUC | Accuracy |
|------------|-----|----------|
| convit_tiny   | 0.9114 | 83.00  |
| vit_tiny_patch16_224    | 0.8973 | 81.61     |
| rersnet18    | 0.8604 | 80.55    |
| efficientnetv2_s | 0.5677| 68.05  |

The notebook can be  also used with Google Colab:
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sawradip/deeplense_tasks_23/blob/main/deeplense_task2/Task2_updated.ipynb)

### Specific Test III: [Learning Mass of Dark Matter Halo](deeplense_task3)

*Those interested in the Regression Project should complete Test III.*\
*Those interested in Extending the DeepLense Pipeline should complete Test III.*

`Task`: Using the provided dataset implement a regression algorithm to learn the mapping between lensing images and the lensing dark matter halo mass. You can use the machine learning algorithm of your choice.  Please implement your approach in PyTorch or Keras and discuss your strategy.

| Model Name | MSE | Normalized RMSE |
|------------|-----|----------|
| resnet18    | 5.87e-05 | 0.1618     |
| resnet26    | 8.39e-05 | 0.201     |
| convnext_pico    | 2.14e-04| 0.352     |

The notebook can be  also used with Google Colab: 
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sawradip/deeplense_tasks_23/blob/main/deeplense_task3/Task3_updated.ipynb)


### Specific Test V: [Exploring Transformers](deeplense_task5)

*Those interested in the Transformer Project should complete Test V.*

`Task`: Use a vision transformer method of your choice to build a robust and efficient model for binary classification or unsupervised anomaly detection on the provided dataset. In the case of unsupervised anomaly detection, train your model to learn the distribution of the provided strong lensing images with no substructure. Please implement your approach in PyTorch or Keras and discuss your strategy.

| Model Name | AUC | Accuracy |
|------------|-----|----------|
| gcvit_tiny    | 0.9954 | 97.4    |
| swin_s3_tiny_224   | 0.9952 | 96.3  |
| vit_tiny_patch16_224    | 0.9938 | 96.2     |
| convit_tiny | 0.9901| 95.6  |

The notebook can be  also used with Google Colab:
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sawradip/deeplense_tasks_23/blob/main/deeplense_task5/Task5_updated.ipynb)






