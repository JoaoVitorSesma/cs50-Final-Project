# Colorectal Cancer Survival Prediction

#### Video Demo: [https://www.loom.com/share/cc4e17c8389c4b39a74bc627426e5a3d?sid=0934a1b0-c889-475b-a2e8-7cbe282c1ee2] 

## Description

This project aims to develop a prediction model for the survival of patients with colorectal cancer. The model is trained using a dataset containing clinical and demographic information, with the goal of predicting the likelihood of survival after 3 years. The model was implemented using the **Random Forest Classifier** and was pre-processed to handle missing data and class imbalance.

### Main Features:

- **Data Preparation**: The code starts by importing a dataset containing information about colorectal cancer patients. Pre-processing includes data cleaning, feature selection, and creating new columns like "ULTIDIAG" (time since the last diagnosis) and "PRESENCA_META" (indicating the presence of metastasis).
  
- **Data Transformation**: Categorical variables are converted into a numeric format using techniques such as **One Hot Encoding** for some variables and **Ordinal Encoding** for others. Additionally, numeric data is normalized to ensure that the model performs properly.

- **Modeling**: Using the processed data, a **Random Forest Classifier** was trained to predict survival. The model was adjusted to handle class imbalance using techniques like **undersampling**, **oversampling**, or adjusting class weights.

- **Model Evaluation**: The model was evaluated using metrics such as accuracy, confusion matrix, and ROC curves to compare the model's performance on both training and testing data.

### Implementation Steps:

1. **Loading and Preparing the Data**:
    - Selection of colorectal cancer patients, residents of São Paulo, and confirmed microscopic diagnoses.
    - Creation of new columns like the time since diagnosis and presence of metastasis.

2. **Transformation and Encoding**:
    - Application of **One Hot Encoding** on categorical variables and normalization of numerical data using **MinMaxScaler**.

3. **Model Building and Training**:
    - **Random Forest Classifier** was used to train the prediction model.
    - Adjustments were made to the model to handle class imbalance.

4. **Evaluation**:
    - Model accuracy was calculated, and its effectiveness was tested using confusion matrices and ROC curves.

5. **Prediction on New Data**:
    - The model was used to predict the survival of new patients after completing the same pre-processing steps.

### Technologies Used:

- **Python**: Primary programming language for the project.
- **Libraries**: 
  - **pandas**: For data manipulation.
  - **NumPy**: For numerical calculations.
  - **scikit-learn**: For machine learning modeling, including the Random Forest algorithm.
  - **Plotly**: For interactive visualizations.
  - **Matplotlib/Seaborn**: For static graphs.

## How to Run the Project

1. **Install dependencies**:
    - Clone this repository.
    - Install the necessary libraries using `pip`:
    ```bash
    pip install -r requirements.txt
    ```

2. **Load the dataset**:
    - Ensure the `pacigeral_jun24.csv` data file is available in the `data/` folder.

3. **Run the code**:
    - Execute the Python scripts to prepare the data, train the model, and evaluate its performance.

4. **Make predictions**:
    - After training the model, you can use the trained model to predict the survival of new patients as described in the code.

## Challenges Faced

- **Class Imbalance**: One of the biggest challenges was the class imbalance in the dataset, where most patients survived and fewer patients died. This issue was addressed by applying data balancing techniques like **undersampling**, **oversampling**, and class weight adjustment.

- **Data Pre-processing**: Data preparation was a significant part of the project. Many columns needed to be cleaned and converted into the appropriate format, ensuring the data was ready to feed the machine learning model.

## Results

- **Accuracy** of the model:  75%.
- **ROC Curve**: The model showed good sensitivity and specificity rates on both the training and testing data.

## Conclusion

This project applied machine learning techniques to solve a real-world problem in healthcare. The developed model can be used to predict the survival of patients with colorectal cancer, which can assist doctors and researchers in planning treatment and follow-up strategies for patients.
