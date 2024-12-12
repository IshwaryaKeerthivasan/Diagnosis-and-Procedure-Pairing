# Diagnosis-Procedure Similarity Prediction using MIMIC-IV
## Project Overview
This project aims to predict the similarity between medical diagnoses and procedures using text-based descriptions. By leveraging the MIMIC-IV clinical dataset, the project uses TF-IDF vectorization and cosine similarity to quantify the relationship between diagnosis descriptions and associated medical procedures. The goal is to enhance clinical decision support systems, enabling better matching of diagnoses to procedures.

## Key Features:
* Data Preprocessing: Involves text extraction from the MIMIC-IV dataset.
* Vectorization: TF-IDF vectorization is used to transform text data into numerical form.
* Similarity Computation: Cosine similarity is used to assess the relationship between diagnoses and procedures.

## Project Phases

### 1. **Data Acquisition**
   - **Dataset**: MIMIC-IV Demo Dataset is used for this project. It contains clinical data with diagnoses and procedure descriptions.
   - **Data Sources**: `d_icd_diagnosis.csv` and `d_icd_procedures.csv`.

### 2. **Data Preprocessing**
   - **Data Cleaning**: Data was sampled and any missing values were handled.
   - **Text Cleaning**: Removal of stop words, special characters, and normalization of text data.

### 3. **Feature Extraction & Vectorization**
   - **TF-IDF Vectorization**: Converts the long textual descriptions of diagnoses and procedures into numerical vectors.
   - **Cosine Similarity**: Measures the cosine similarity between the diagnosis and procedure vectors to find similarities.

### 4. **Model Development**
   - **Siamese Network Architecture**: This project uses a Siamese network model to measure the similarity between diagnoses and procedures. The network consists of twin neural networks that process input pairs and compute a similarity score. It works by calculating the distance between two input embeddings (diagnosis and procedure) in a shared space, allowing the model to predict how similar the two texts are. This architecture is particularly useful for tasks involving similarity or matching, such as in this project.
   - **Evaluation**: The model's performance is evaluated using Validation loss and MAE.

### 5. **Prediction**
   - **Prediction Phase**: After training the model, it is used to predict the similarity score between the diagnosis-procedure pairs. These predictions provide a numerical value that represents how closely related a diagnosis is to a given procedure.
   - **Results**: 
     - The predicted similarity scores ranged from 0.0 (no similarity) to 1.0 (high similarity).
     - In some cases, the model correctly predicted very similar diagnosis-procedure pairs (e.g., a diagnostic code related to pneumonia being matched to an appropriate procedure).
     - The model's ability to predict similarity demonstrates its potential for automated mapping in healthcare settings.

### 6. **Visualization**
   - **Top 5 Most Similar Pairs**: This visualization showcases the most similar diagnoses and procedures based on the highest cosine similarity scores.
   - **Cosine Similarity Distribution**: A histogram showing the distribution of similarity scores between diagnoses and procedures to better understand the overall similarity trend in the data.
   - **Word Cloud**: A word cloud representing the most frequent words from the descriptions of diagnoses and procedures, which gives insight into common terms in the medical domain.


![image](https://github.com/user-attachments/assets/65e5c477-352c-4ad0-9e20-d18af7532f64)
![image](https://github.com/user-attachments/assets/afa158b2-80a6-416b-ac2d-741bfa806a3d)

