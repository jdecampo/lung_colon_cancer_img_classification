# Lung Colon cancer histopathological imgages Classification - Project Overview
Lung and Colon cancer histopathological image classification utilizing DeepL (CNN, Transfer Learning) as part of Deep Learning course assignment.
- The assignment goal was to evaluate how the application of various deep learning techniques, particularly computer vision approaches like Convolutional Neural Networks (CNN) and Transfer Learning, influences the accuracy of predictions in detecting and diagnosing lung and colon cancer, using the Lung and Colon Cancer Histopathological Image Dataset.
- The outcome of this project should be a potential solution that can further support Healthcare specialists (Oncologists) for the diagnosis and study of cancer (Model Accuracy 97%), based on Histopathological imaging.

## Dataset Description
The dataset comprises 25,000 colour images, evenly distributed across 5 distinct histological categories:

**(0)** **Colon Benign Tissue:** non-cancerous cells and structures within the colon.

**(1)** **Colon Adenocarcinoma:** is the most common type of colon cancer, it originates from the glandular cells of the colon, which are responsible for producing mucus and other fluids.

**(2)** **Lung Benign Tissue:** includes the normal structures of the lungs that are involved in breathing but are not affected by cancerous changes.

**(3)** **Lung Squamous Cell Carcinoma:** is a type of NSCLC and is more frequently associated with smoking. It typically occur in the central part of the lungs near the main airways.

**(4)** **Lung Adenocarcinoma:** is the most common type of non-small cell lung cancer (NSCLC) seen in the USA.

## Project Reference(s):

- **Dataset original Article:** Borkowski AA, Bui MM, Thomas LB, Wilson CP, DeLand LA, Mastorides SM. Lung and Colon Cancer Histopathological Image Dataset (LC25000). arXiv:1912.12142v1 [eess.IV], 2019 [arXiv:1912.12142v1](https://arxiv.org/abs/1912.12142v1)
- [Histological category descriptions](https://www.ncbi.nlm.nih.gov/)
- Snippets of code, derived from existing solutions, have been annotated and included as inline comments.





Project Organization
------------

    ├── LICENSE
    ├── README.md          <- High-level README for developers using this project.
    ├── code               <- Jupyter Notebook with scripts to perform EDA, train models 
    │   │   │                 and make predictions.
    ├── data
    │   ├── curated        <- Curated Image datasets divided into features and target variable.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │   └── model_trained  <- Trained models.   
    │
    └── report            <- Generated analysis as PDF, PNG.


## EDA

To gain a better understanding of the problem, display a subset of the histopathological images: ![image](https://github.com/jdecampo/lung_colon_cancer_img_classification/blob/main/report/eda_lung_colon_cancer_images.png)

Plot the distribution for each category present in the dataset: ![image](https://github.com/jdecampo/lung_colon_cancer_img_classification/blob/main/report/eda_class_distribution.png)

## Methodology Pipeline:

![image](https://github.com/jdecampo/lung_colon_cancer_img_classification/blob/main/report/lung_colon_methodology_pipeline.png)

## Model Performance: 

- The best model has been selected based on test **Accuracy** score (TP+TN / TP+TN+FP+FN). 
- Model performance per histological categories are assessed based on **Precision** (TP/TP+FP) for categories **(0)**, **(2)** as we want to mitigate the impact of wrongly diagnosing patients with cancer as healthy.
- Whereas **Recall** score (TP/TP+FN) is used for **(1)**, **(3)**, **(4)**, to prevent the risk of falsely diagnosing a patient to be healthy while having cancer. Additionally, the **ROC-AUC** score was utilized to monitor the model's performance per category, ensuring effectiveness beyond chance.
- Given the sensitive nature of the use case, it is highly recommended that healthcare specialists personally review all patient results. The outcomes derived from the support solution should be evaluated in mainly ~40% of the cases to ensure thorough oversight and accuracy. The current model is designed to streamline the process for the remaining 60% of cases, allowing healthcare professionals to concentrate their efforts on more complex scenarios. This approach ensures that resources are optimally allocated, enhancing overall efficiency and effectiveness in patient care.

**Base CNN model:** Accuracy: 74%

**Enhanced CNN model:** Accuracy: 97%

**Transfer Learning (VGG16) model:** Accuracy: 97%. ROC-AUC 1 for each category.

Selected best model since it matches the performance of the Enhanced model while utilizing a less resource-intensive network. This efficiency showcases the benefits of transfer learning, highlighting its ability to maintain high accuracy without the need for extensive computational resources.


## Error Analysis: 

Based on the results obtained, when employing the Transfer model, healthcare specialists should pay particular attention to the histological categories of Lung Squamous Cell Carcinoma and Lung Adenocarcinoma. 
This caution is advised because the current model has shown a tendency to misclassify these two diagnoses as shown in **Confusion Matrix**:

![image](https://github.com/jdecampo/lung_colon_cancer_img_classification/blob/main/report/transfer_model_confusion_matrix.png)

    
