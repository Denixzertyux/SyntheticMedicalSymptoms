# Synthetic Medical Symptoms Classification

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A machine learning project that analyzes synthetic medical symptoms data and builds a classification model to predict medical diagnoses based on patient symptoms, vital signs, and laboratory values.

## 📋 Overview

This project performs comprehensive exploratory data analysis (EDA) on a synthetic medical symptoms dataset and implements a Random Forest classifier to predict medical diagnoses. The model uses various features including patient demographics, symptoms, vital signs, and laboratory test results to classify patients into different diagnostic categories.

## 🎯 Objectives

- Perform exploratory data analysis on medical symptoms data
- Visualize data distributions, correlations, and patterns
- Build a machine learning model to predict medical diagnoses
- Evaluate model performance using various metrics
- Identify important features for diagnosis prediction

## 📊 Dataset

The dataset (`synthetic_medical_symptoms_dataset.csv`) contains **3,000 patient records** with the following information:

### Features

**Demographics:**
- `age`: Patient age
- `gender`: Patient gender (Male/Female)

**Symptoms (0-3 severity scale):**
- `fever`: Fever severity
- `cough`: Cough severity
- `fatigue`: Fatigue level
- `headache`: Headache severity
- `muscle_pain`: Muscle pain level
- `nausea`: Nausea severity
- `vomiting`: Vomiting severity
- `diarrhea`: Diarrhea severity
- `skin_rash`: Skin rash presence/severity
- `loss_smell`: Loss of smell severity
- `loss_taste`: Loss of taste severity

**Vital Signs:**
- `systolic_bp`: Systolic blood pressure (mmHg)
- `diastolic_bp`: Diastolic blood pressure (mmHg)
- `heart_rate`: Heart rate (bpm)
- `temperature_c`: Body temperature (°C)
- `oxygen_saturation`: Blood oxygen saturation (%)

**Laboratory Values:**
- `wbc_count`: White blood cell count (×10³/µL)
- `hemoglobin`: Hemoglobin level (g/dL)
- `platelet_count`: Platelet count (×10³/µL)
- `crp_level`: C-reactive protein level (mg/L)
- `glucose_level`: Blood glucose level (mg/dL)

**Target Variable:**
- `diagnosis`: Medical diagnosis (COVID-19, Influenza, Dengue, Malaria, Pneumonia)

## 🛠️ Requirements

- Python 3.7 or higher
- Jupyter Notebook or JupyterLab

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Denixzertyux/SyntheticMedicalSymptoms.git
   cd SyntheticMedicalSymptoms
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   
   # On Windows:
   venv\Scripts\activate
   
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## 📁 Project Structure

```
SyntheticMedicalSymptoms/
│
├── synthetic_medical_symptoms_dataset.csv  # Dataset file (3,000 patient records)
├── medical_symptoms_analysis.ipynb          # Jupyter notebook with complete analysis
├── requirements.txt                         # Python package dependencies
├── LICENSE                                  # MIT License
├── .gitignore                               # Git ignore file
└── README.md                                # Project documentation
```

## 🚀 Getting Started

### Running the Analysis

1. **Start Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

2. **Open the analysis notebook:**
   - Navigate to `medical_symptoms_analysis.ipynb` in the Jupyter interface
   - Or directly open it:
     ```bash
     jupyter notebook medical_symptoms_analysis.ipynb
     ```

3. **Run the cells sequentially:**
   - **Cell 0**: Import required libraries and set up environment
   - **Cell 1**: Load the dataset
   - **Cell 2**: Data preprocessing and cleaning
   - **Cell 3**: Exploratory data analysis with visualizations
   - **Cell 4**: Model building and evaluation

## 📈 Analysis Workflow

### 1. Data Loading and Preprocessing
- Loads the CSV dataset
- Converts numeric columns to appropriate data types
- Handles missing values (if any)
- Final dataset shape: 3,000 rows × 24 columns

### 2. Exploratory Data Analysis
The notebook generates several visualizations:

- **Histograms**: Distribution of all numeric features
- **Count Plot**: Distribution of diagnoses
- **Correlation Heatmap**: Relationships between numeric features
- **Pair Plot**: Pairwise relationships for key features
- **Box Plot**: Age distribution across different diagnoses

### 3. Model Building
- **Algorithm**: Random Forest Classifier
- **Features**: All numeric features (excluding gender and diagnosis)
- **Train/Test Split**: 80/20 with stratification
- **Hyperparameters**: 
  - `n_estimators`: 100
  - `random_state`: 42

### 4. Model Evaluation
The model evaluation includes:

- **Accuracy Score**: Overall classification accuracy
- **Confusion Matrix**: Visual representation of classification performance
- **Feature Importance**: Permutation importance analysis to identify key predictors
- **ROC Curve**: Receiver Operating Characteristic curve for model performance

## 📊 Model Performance

The Random Forest classifier achieves an **accuracy of approximately 24.17%** on the test set. Note that this is a multi-class classification problem with 5 diagnostic categories, so performance should be evaluated in context of:
- Class distribution balance
- Baseline accuracy (random guess: ~20% for 5 classes)
- Confusion matrix patterns
- Feature importance insights

## 🔍 Key Insights

The analysis provides insights into:
- Feature distributions and their relationships
- Which symptoms and vital signs are most predictive
- Patterns in diagnosis distribution
- Correlations between different medical measurements

## ⚠️ Important Notes

1. **Synthetic Data**: This dataset is synthetic and should not be used for real medical decision-making.

2. **Model Limitations**: 
   - The model is trained on synthetic data
   - Performance metrics are for demonstration purposes only
   - Not suitable for clinical use

3. **Data Privacy**: This is synthetic data, so no real patient information is included.

## 🔮 Future Improvements

Potential enhancements to the project:
- Hyperparameter tuning for better model performance
- Feature engineering and selection
- Cross-validation for more robust evaluation
- Additional classification algorithms (SVM, XGBoost, Neural Networks)
- Class imbalance handling techniques
- Multi-class ROC curves for all diagnoses
- Model interpretation using SHAP values

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/Denixzertyux/SyntheticMedicalSymptoms/issues).

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Thanks to the open-source community for the excellent libraries used in this project
- Synthetic dataset created for educational purposes

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

---

**⚠️ Disclaimer**: This project uses synthetic data and is intended for educational and research purposes only. It should **NOT** be used for actual medical diagnosis or treatment decisions. Always consult with qualified healthcare professionals for medical advice.

