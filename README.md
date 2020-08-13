# COVID-19 and Pneumonia Diagnosis

## Project [ COVID-19 and Pneumonia Diagnosis ]
  - https://www.kaggle.com/c/deep-learning-competition-cs-2020

## Dataset
The dataset is organized into 2 folders (train and test) and contains subfolders for the train category (COVID-19 and Pneumonia/Normal).
There are 5,266 X-Ray training images, 1,341 Normal X-Ray and 3,925 (COVID-19 and Pneumonia) images.

[Dataset in Kaggle!](https://www.kaggle.com/c/deep-learning-competition-cs-2020/data)

## Data Preparation and PreProcessing:
   • Convert to gray image
   • Histogram Equalization
   • resize shape to ( 128, 128 )
   • Reshape to (128, 128, 1) “Add dimension at axis = -1”
   • Min-Max Normalization
   • Split Training data to 90% training and 10% validation

## Data Augmentation :
   • Randomly rotate some training images by 30 degrees
   • Randomly Zoom by 20% some training images
   • Randomly shift images horizontally by 10% of the width
   • Randomly shift images vertically by 10% of the height Once our model is ready, we fit the training dataset.

## Models 'trails':
    Start with VGG19 model then change/reduce layers to score a validation accuracy up to 98.
    Best Model: ![model](/images/model.png)


## Optimizer → Adam with learning rate 2e-4
## Loss function → binary cross entropy
## Evaluation metrics → accuracy
## Total parameters → 949,313


## leaderboard kaggle:
  1. Public testset ![model](/images/public_res.png)
  2. Private testset ![model](/images/private_res.png)
