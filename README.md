# EEG Seizure Detection using Machine Learning

This project implements a machine learning approach to detect seizures from electroencephalography (EEG) signals. The pipeline includes preprocessing, feature extraction, and classification using Support Vector Machines (SVM) and Random Forest algorithms.

## Project Overview

Epilepsy is a neurological disorder affecting approximately 50 million people worldwide. Automatic seizure detection from EEG signals can assist medical professionals in diagnosis and treatment planning. This project demonstrates how machine learning can be applied to this important medical challenge.

## Pipeline Components

1. **Data Loading and Exploration**
   - Loads EEG data from seizure and non-seizure recordings
   - Visualizes sample data to understand signal characteristics

2. **Preprocessing**
   - Applies bandpass filtering (0.5-40 Hz) to remove noise while preserving relevant brain wave patterns
   - Focuses on Delta, Theta, Alpha, Beta, and Gamma frequency bands

3. **Feature Extraction**
   - Time-domain features: mean, standard deviation, max, min, range, skewness, kurtosis
   - Frequency-domain features: power in different EEG rhythms (Delta, Theta, Alpha, Beta, Gamma)
   - Resonance frequency (frequency with maximum power)

4. **Classification**
   - Data split: 70% training, 30% testing
   - Standardization of features
   - Two classifiers: Support Vector Machine (SVM) and Random Forest
   - Performance evaluation using accuracy, precision, recall, F1-score, and confusion matrices

## Results

Our evaluation shows that the Random Forest classifier outperforms the SVM model:

**Random Forest Results**:
- Accuracy: 94.59%
- Precision: 97.87%
- Recall: 90.20%
- F1 Score: 93.88%

**SVM Results**:
- Accuracy: 91.44% 
- Precision: 98.82%
- Recall: 82.35%
- F1 Score: 89.84%

The higher recall of the Random Forest model is particularly important in medical applications, as it means fewer seizures are missed (false negatives).

## Visualizations

This project includes visualizations for:
- EEG signal comparison between seizure and non-seizure patterns
- Effect of preprocessing (bandpass filtering)
- Frequency domain analysis
- Feature distributions
- Model performance comparisons

## Dependencies

- Python 3.x
- NumPy
- Pandas
- SciPy
- Scikit-learn
- Matplotlib
- Seaborn

## Usage

1. Prepare your data in CSV format with EEG channels as columns
2. Update the paths in the code to point to your data folders
3. Run the main function to execute the full pipeline
