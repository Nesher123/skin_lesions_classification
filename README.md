# Skin Lesions Classification: An Efficient MultiClass Skin Cancer Classification Using Transfer Learning

### 📌 Abstract

Skin cancer is the most common cancer in the world, constituting one-third of cancer cases.
Benign skin cancers are not fatal and can be cured with proper medication.
But it is not the same as malignant skin cancers.
In the case of malignant melanoma, in its peak stage, the maximum life expectancy is less than or equal to 5 years.
But, it can be cured if detected in the early stages.
Though there are numerous clinical procedures, the accuracy of diagnosis falls between 49% to 81% and is time-consuming.
So, dermatoscopy has been brought into the picture. It helped increase the accuracy of diagnosis but could not demolish
the error-prone behavior. A quick and less error-prone solution is needed to diagnose this majorly growing skin cancer.
This project deals with the usage of deep learning in skin lesion classification. In this project, an automated model
for skin lesion classification using dermoscopic images is developed with CNN (Convolution Neural Networks) as a
training model. Convolution neural networks are known for capturing the features of an image. So, they are preferred in
analyzing medical images to find the characteristics that drive the model toward success.
This work has the potential to assist dermatology specialists in decision-making at critical stages.

### 🗃️ Dataset

A public dataset from the International Skin Imaging Collaboration (ISCI) archive was obtained for this work known as
HAM10000. It is quite a large dataset that consists of 10015 samples of multi-source dermatoscopic images of common
pigmented skin lesions.
Get the data [here](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T).

### 📝 Results

The table below presents the results of the skin lesions classification using different models, color spaces,
augmentations, and localization strategies.

| #  | File Name                              | Link                                                         | Accuracy | Precision | Recall | F1   |
|----|----------------------------------------|--------------------------------------------------------------|----------|-----------|--------|------|
| 1  | Exploratory Data Analysis              | [**Notebook**](EDA.ipynb)                                    | -        | -         | -      | -    |
| 2  | ResNet50 (RGB, aug)                    | [**Notebook**](model_ResNet50_rgb_aug.ipynb)                 | 0.89     | 0.77      | 0.81   | 0.79 |
| 3  | ResNet50 (grayscale, aug)              | [**Notebook**](model_ResNet50_gray_aug.ipynb)                | 0.81     | 0.63      | 0.74   | 0.67 |
| 4  | ResNet50 (RGB, NO aug)                 | [**Notebook**](model_ResNet50_rgb_no_aug.ipynb)              | 0.87     | 0.77      | 0.78   | 0.76 |
| 5  | ResNet50 (RGB, aug, "lower extremity") | [**Notebook**](model_ResNet50_rgb_aug_lower_extremity.ipynb) | 0.88     | 0.80      | 0.79   | 0.79 |
| 6  | ResNet50 (RGB, aug, mel vs nv)         | [**Notebook**](model_ResNet50_rgb_aug_mel_nv.ipynb)          | 0.95     | 0.90      | 0.89   | 0.89 |
| 7  | ResNet50 (RGB, aug, mel vs bkl)        | [**Notebook**](model_ResNet50_rgb_aug_mel_bkl.ipynb)         | 0.86     | 0.86      | 0.86   | 0.86 |
| 8  | ResNet50 (RGB, aug, akiec vs bcc)      | [**Notebook**](model_ResNet50_rgb_aug_akiec_bcc.ipynb)       | 0.88     | 0.89      | 0.86   | 0.87 |
| 9  | Xception (RGB, aug)                    | [**Notebook**](model_Xception_rgb_aug.ipynb)                 | 0.87     | 0.75      | 0.82   | 0.78 |
| 10 | Xception (grayscale, aug)              | [**Notebook**](model_Xception_gray_aug.ipynb)                | 0.80     | 0.61      | 0.71   | 0.66 |
| 11 | InceptionResNetV2 (RGB, aug)           | [**Notebook**](model_InceptionResNetV2_rgb_aug.ipynb)        | 0.85     | 0.74      | 0.78   | 0.76 |
| 12 | InceptionResNetV2 (grayscale, aug)     | [**Notebook**](model_InceptionResNetV2_gray_aug.ipynb)       | 0.83     | 0.67      | 0.73   | 0.70 |
| 13 | VGG19 (RGB, aug)                       | [**Notebook**](model_Vgg19_rgb_aug.ipynb)                    | 0.73     | 0.57      | 0.69   | 0.61 |
| 14 | VGG19 (grayscale, aug)                 | [**Notebook**](model_Vgg19_gray_aug.ipynb)                   | 0.11     | 0.02      | 0.14   | 0.03 |
| 15 | Ensemble Predictions                   | [**Notebook**](ensemble_predictions.ipynb)                   | -        | -         | -      | -    |
| 16 | Mix-Model                              | [**Notebook**](mix_model.ipynb)                              | 0.89     | 0.78      | 0.85   | 0.81 |

### 📁 Project Structure

```
├───data
│   ├───HAM10000.zip (both parts form source combined into a single zip file)
│   ├───HAM10000_metadata.csv (metadata file from source)
│   ├───test_image_gen_class_indices.csv (class indices file created on notebook run)
│   ├───test_image_gen_classes.csv (ground truth classes for each image image in test set. created on notebook run)
│   │
│   ├───history
│       └───all models' history from training
│   ├───predictions
│       └───all models' predictions after training
│   └───models
│       └───all already-trained models hdf5 files (weights for loading afer building the model instead of training)
│
├───all notebooks from table above
└───README.md
```

### 📞 Contact Me

If you have any questions or comments about this project, please feel free to contact me by email:
[**here**](mailto:Nesher123@gmail.com)
