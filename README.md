# Regularized Xception for Facial Expression Recognition with Extra Training Data and Step Decay Learning Rate

Despite extensive research on facial expression recognition, achieving the highest level of accuracy remains challenging. The objective of this study is to enhance the accuracy of current models by adjusting the structure, the data used, and the training procedure. The incorporation of regularization into the Xception architecture, the augmentation of training data, and the utilization of step decay learning rate together address and surpass current constraints. A substantial improvement in accuracy is demonstrated by the assessment conducted on the FER2013 dataset, achieving a remarkable 94.34%. This study introduces potential avenues for enhancing facial expression recognition systems, specifically targeting the requirement for increased accuracy within this domain.

![Proposed Method try](https://github.com/elangarka/Regularized-Xception-FER-Extra-Training-Data-Step-Decay-Learning-Rate/assets/157675554/c42c96b7-fcb6-428c-abd8-1805bc09f192)


## DATASET
**Download Dataset**

[![Dataset ](https://img.shields.io/badge/Dataset-Google_Drive-green)](https://drive.google.com/file/d/1PtU6vkjFvOJh32A3mIxkLO9x0xvhBdKQ/view?usp=sharing)

This dataset is a combination of three datasets namely FER2013, CK+, and Extended & Augmented Google FER (without "contempt" class). Here are the details of the contents of the datasets to be used.

| Dataset | Usage     | Amount of Data                |
| :-------- | :------- | :------------------------- |
| FER2013(TrainingData) [![KaggleFER2013 ](https://img.shields.io/badge/FER2013-Kaggle-blue)](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data) | `Training Data` | 28.709 |
| CK+ [![KaggleCK+ ](https://img.shields.io/badge/CKPLUS-Kaggle-blue)](https://www.kaggle.com/datasets/shawon10/ckplus)| `Training Data` | 981  |
| Extended & Augmented Google FER (without "contempt" class )[![KaggleEXT ](https://img.shields.io/badge/Ext_Google_FER-Kaggle-blue)](https://www.kaggle.com/datasets/prajwalsood/google-fer-image-format) | `Training Data` | 38.191 |
| FER2013(PublicTest) [![KaggleFER2013 ](https://img.shields.io/badge/FER2013-Kaggle-blue)](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data) | `Validation Data` | 3.589 |
| FER2013(PrivateTest) [![KaggleFER2013 ](https://img.shields.io/badge/FER2013-Kaggle-blue)](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data) | `Test Data` | 3.589  |

## MODEL
**Download Model**

[![Dataset ](https://img.shields.io/badge/Model-Google_Drive-green)](https://drive.google.com/file/d/1TrmA0WkO7hPC4EV12Tt9jO9axn_4toJi/view?usp=sharing)

Xception is composed of three sections: the entry flow, the middle flow, and the exit flow. The Entry Flow component, which constitutes the initial segment of Xception, is tasked with the processing of the incoming image. The Middle Flow section serves as the central component of the Xception network and consists of a sequence of profound convolutional blocks. Nevertheless, the design in this study was altered by incorporating a layer dropout in the middle flow section, along with applying L2 regularization to the exit flow section. The purpose of this change was to mitigate overfitting in the model outcome.

![arsitektur xception modif](https://github.com/elangarka/Regularized-Xception-FER-Extra-Training-Data-Step-Decay-Learning-Rate/assets/157675554/ee6c504d-c7c4-458a-b0ef-d651c1f2a526)

## TRAINING

- Download Dataset
- Open Regularized Xception_FER_ExtraTrainingData_StepDecay.ipynb [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elangarka/Regularized-Xception-FER-Extra-Training-Data-Step-Decay-Learning-Rate/blob/main/Regularized_Xception_FER_ExtraTrainingData_StepDecay.ipynb)

- Upload the dataset to google colab
- Customize the model output (.h5) file name as desired *(Default : bestXceptionPlusData.h5)*
- Run the program
- Download the model (.h5)

*Notes: Please copy the colab files to your drive, thanks!*
## EVALUATE

- Open Evaluate Model.ipynb [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elangarka/Regularized-Xception-FER-Extra-Training-Data-Step-Decay-Learning-Rate/blob/main/Evaluate_Model.ipynb)
- Upload model (.h5) and dataset to google colab
- Run the program

*Notes: Please copy the colab files to your drive, thanks!*
## RESULT

The research results show that the model achieved a training accuracy of 96.5%, a validation accuracy of 94.73%, and a test accuracy of 94.3%. In addition, each class achieves a f1-score value of > 90%, indicating a high level of balance between precision and recall for the findings in each class.

**Accuracy and loss graph from third training:**
![Screenshot 2023-10-30 180649](https://github.com/elangarka/Regularized-Xception-FER-Extra-Training-Data-Step-Decay-Learning-Rate/assets/157675554/6a1d54aa-d1db-40f9-bcd6-4810ce528745)

**Confusion matrix and classification report model:**
![Screenshot 2023-11-01 155131](https://github.com/elangarka/Regularized-Xception-FER-Extra-Training-Data-Step-Decay-Learning-Rate/assets/157675554/b532860d-5659-4f61-ac68-045f11302ca9)
![Screenshot 2023-11-01 155144](https://github.com/elangarka/Regularized-Xception-FER-Extra-Training-Data-Step-Decay-Learning-Rate/assets/157675554/32d19722-2aa0-4322-9456-53f54944374b)

**Test loss and test accuracy model:**
![Screenshot 2023-11-01 155157](https://github.com/elangarka/Regularized-Xception-FER-Extra-Training-Data-Step-Decay-Learning-Rate/assets/157675554/adde14e2-c58d-4168-a105-87e60181d293)


## REFERENCES

- I. J. Goodfellow et al., “Challenges in Representation Learning: A report on three machine learning contests,” Jul. 2013, [Online]. Available: http://arxiv.org/abs/1307.0414
- F. Chollet, “Xception: Deep Learning with Depthwise Separable Convolutions,” Proceedings of the IEEE conference on computer vision and pattern recognition, 2017.





