# NLP_cw1: Classifying Patronising and Condescending Language

## Overview
This repository contains the code and resources for classifying patronising and condescending language (PCL) using natural language processing (NLP) techniques. The project leverages the *Don't Patronize Me!* dataset to train and evaluate models capable of identifying subtle PCL in text. The project aims to classify PCL using a language model, with a focus on improving performance beyond a baseline RoBERTa model. The report details the exploration of the dataset, experimentation with various techniques, and analysis of model performance.

## Authors
- **Megan Howard**: [mh2919@ic.ac.uk](mailto:mh2919@ic.ac.uk)
- **Benedict Newton-Ingham**: [bn120@ic.ac.uk](mailto:bn120@ic.ac.uk)
- **Anjali Ramesh**: [ar4323@ic.ac.uk](mailto:ar4323@ic.ac.uk)


## Dataset
The *Don't Patronize Me!* dataset is used, which includes text annotated for PCL. The dataset is imbalanced, with only 9.5% of entries labeled as patronising. Features include:
- Keywords
- Country of origin
- Binary PCL labels

## Methodology

### Model Setup
- **Model Used**: RoBERTaForSequenceClassification  
- **Preprocessing**: Minimal, to preserve context and nuance.  
- **Data Augmentation**: Upsampling of minority class using backtranslation and synonym replacement.  
- **Loss Function**: Weighted cross-entropy to address class imbalance.

### Improvements
- Data preprocessing and augmentation strategies were tested to balance the dataset.
- Keywords and country labels were appended to text to provide additional context.
- Hyperparameter tuning was conducted to optimise model performance.

### Baseline Comparison
Baseline models included:
- Logistic Regression
- TF-IDF
- Bag of Words  

The improved RoBERTa model outperformed these baselines, particularly in handling the minority class.

## Results
- The final model achieved a significant improvement in F1 score over baseline models.
- The model performed best on texts with clear PCL characteristics but struggled with more nuanced cases.
- Longer texts provided more context, improving model performance, though extremely long texts led to inconsistent results.

## Future Work
Recommendations include:
- Further experimentation with data augmentation techniques.
- Exploring additional model architectures to improve classification of nuanced PCL.

## References
- Pérèz et al., 2020. "*Don’t Patronize Me! An Annotated Dataset with Patronizing and Condescending Language towards Vulnerable Communities.*"
- Zampieri et al., 2019. "*SemEval-2019 Task 6: Identifying and Categorizing Offensive Language in Social Media (OffensEval).*"

---
