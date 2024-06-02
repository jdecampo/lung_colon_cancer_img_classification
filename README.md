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

## Main Project Reference:

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
