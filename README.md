# Automated-Liver-Tumor-Detection

In this project, a computer-aided diagnosis (CAD) system  is provided for Abdominal CT Liver Images.

![cad-gui](https://user-images.githubusercontent.com/91828519/139037040-f2650624-1b8d-4184-a90d-671fcd384f64.png)


This implementation comprises of four main phases: 
* liver segmentation
* lesion candidate segmentation
* feature extraction from each candidate lesion
* liver disease classification

Flowchart The proposed method is as follows

![flowchart-en](https://user-images.githubusercontent.com/91828519/139037802-b1386a82-4907-44ef-9a77-9a394ddb41bb.png)


### Preprocessing
In the preprocessing stage, the histogram thresholding method is used to highlight the liver tissue.

<img width="639" alt="4-1" src="https://user-images.githubusercontent.com/91828519/139037197-3192d085-1773-4eaa-9a66-830ae730b6e1.png">

### 1.liver segmentation
To liver segmentation, used the levelset method. This step is done in two parts; The first part uses an initial mask to find the area of the liver and finally morphological operations are used to improve the border of the liver image.

<img width="595" alt="4-3" src="https://user-images.githubusercontent.com/91828519/139037304-20d23e1d-f25c-4294-b2cb-6bd7e88dbe79.png">


### 2.lesion candidate segmentation
Fast fuzzy c-means (FFCM) clustering is used for lesion candidates extraction.

<img width="552" alt="4-4" src="https://user-images.githubusercontent.com/91828519/139037506-7f065fad-1a81-456d-af80-91e0e330350e.png">

### 3.feature extraction
In the third phase after extraction of lesion from the liver, variety of features are extracted from each candidate. These features describe the tissue properties and shape of the lesion and include: area, median, mean, skewness, standad deviation, kurtosis and haralick.

### 4.liver disease classification
Finally, these features are used in a classification stage using a support vector machine.
  
