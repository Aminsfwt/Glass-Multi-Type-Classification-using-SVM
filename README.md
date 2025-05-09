# Glass Identification Using SVM

This repository contains a machine learning project that identifies different types of glass based on their chemical composition using Support Vector Machines (SVM). 
The project demonstrates data preprocessing, model training, hyperparameter tuning with GridSearchCV, and model evaluation through metrics, classification reports, and (optionally) visualizations.

## Repository Structure

```
 Glass Identification/
    ├── glass.csv                # Dataset containing glass sample measurements and target variable ('Type')
    ├── MultiClass_SVM.py        # Main script for data preprocessing, training the SVM model, tuning hyperparameters, and evaluating the model
```

## Overview

- **Data Preprocessing:**  
  - Reads the `glass.csv` dataset and shuffles the data.
  - Splits the data into features (`X`) and target (`y`).
  - Standardizes the features using `StandardScaler`.

- **Model Training:**  
  - Trains an SVM model using an RBF kernel.
  - Displays the accuracy of the baseline model on the test set.

- **Hyperparameter Tuning:**  
  - Uses `GridSearchCV` over a parameter grid (varying `C`, `gamma`, and `kernel`) to find the best SVM configuration.
  - Applies a balanced class weight in order to manage any class imbalances.
  - Evaluates the tuned model with accuracy and prints a classification report.

- **Feature Importance (Optional):**  
  - Measures feature importance using permutation importance on the best model.
  
- **Visualizations (Optional):**  
  - The script includes commented-out code for plotting a confusion matrix and feature scatter plots.

## Requirements

- Python 3.x
- Pandas
- NumPy
- scikit-learn
- seaborn
- matplotlib

Install the requirements using pip:

```bash
pip install pandas numpy scikit-learn seaborn matplotlib
```

## How to Run

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/your-repository-name.git
   ```

2. **Navigate to the Project Folder:**

   ```bash
   cd your-repository-name/Applied ML/Glass Identification
   ```

3. **Run the Main Script:**

   Execute the script to train and evaluate the SVM model:

   ```bash
   python MultiClass_SVM.py
   ```

   The script will automatically:
   - Standardize the features,
   - Split the dataset into training and test sets,
   - Train an SVM model (baseline),
   - Tune hyperparameters using GridSearchCV,
   - Print the best parameters, accuracy, and classification report,
   - (Optionally) provide feature importance and visualizations.

## Customization

- **Hyperparameter Grid:**  
  You can modify the parameter values in `MultiClass_SVM.py` under the `param_grid` dictionary to experiment with different configurations.

- **Visualizations:**  
  Uncomment the plotting sections if you would like to view the confusion matrix or feature scatter plots.
