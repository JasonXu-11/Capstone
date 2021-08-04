# Capstone -- Deep Learning Drowsiness Detection

## Problem Statement
Drowsiness endanger many drivers during driving. Reminding drivers they need to remain conscious or take a rest is very effective way to avoid car accident. Some car manufactures has developed successful driving monitoring system to detect drivers' drowsiness and alert them for safety.


## Code Requirements
This code is written in [Python3](https://www.python.org/downloads/)

### Project Datasets

| File | Description | Number of Image | Link |
| --- | --- | --- | --- |
| train | trainset contains four folders of pictures (Open-Closed-yawn-no-yawn)| 2467 (Open: 617 ; Closed: 617) |[Link](https://www.kaggle.com/vanvalkenberg/drowsiness-detection-model-tensorflow/data)|
| test | testset contains four folders of pictures (Open-Closed-yawn-no-yawn) | 433 (Open: 109 ; Closed: 109)| [Link](https://www.kaggle.com/vanvalkenberg/drowsiness-detection-model-tensorflow/data)|

### Python Library
1. cv2
2. os
3. matplotlib.pyplot
4. numpy
5. tensorflow.keras
  * preprocessing.image.ImageDataGenerator
  * models.Sequential
  * layers
    * Dense, Dropout, Flatten, Conv2D, MaxPooling2D
6. sklearn.metrics
  * confusion_matrix, plot_confusion_matrix, classification_report
7. seaborn

### Image Selection
| Folder| Description | Number of Image |
| --- | --- | --- |
| Open | image for eye-open | train: 617; test: 109 |
| Closed | image for eye-closed | train: 617; test: 109 |

## Jupyter Notebook

| File | Description |
| --- | --- |
| CNN.ipynb | The process of building CNN model|
| Prediction.ipynb | The example of how to predict any image we have |

## CNN Model
![CNN Model](https://github.com/JasonXu-11/Capstone/blob/main/picture/CNN.png?raw=true)

## Saved model
Run CNN.ipynb with create a saved h5 file contains the cnn model we create.
Use the h5 file and use the following code in Prediction to instantiate the model.

```Python
new_model = tf.keras.models.load_model('../cnn_model_open.h5')
```
