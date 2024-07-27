##Author
Eng/Amr Mostafa Omar  
TA at ITCS school , Nile University, Cairo, Egypt  
Date: 20/6/2024

*******==========================================********
   Motor Imagery EEG Signal Analysis for Finger Movement: 
        An Approach to Brain-Computer Interfaces
*******==========================================********

## Motivation and Purpose:
In this study, we aimed to classify finger movements using brain signals captured through EEG. We focused on five distinct classes of finger movements: Thumb, Index, Middle, Ring, and Pinky. Utilizing ML models (Machine Learning),CNN, RNN and hybrid approach CNN +Transformer 


## Features
- **Reduced Channel Count:** Focus on fewer channels to facilitate real-time application without compromising accuracy.
- **Simpler Setup:** Easier and faster to set up, enhancing user convenience.
- **Real-Time Application:** Practical solutions for real-time scenarios using a reduced number of EEG channels.

## Technologies Used
- **Machine Learning Models:** Utilization of various ML models to process and analyze EEG signals.
- **Convolutional Neural Networks (CNN):** For spatial feature extraction from EEG data.
- **Recurrent Neural Networks (RNN):** For temporal feature extraction from EEG data.
- **Hybrid Models:** Combination of CNN and transformer to leverage both spatial and temporal features for improved accuracy.

## Installation Instructions

1. **Mount Google Drive:**
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```
2. **Install PyWavelets:**
    ```bash
    pip install PyWavelets
    ```

## Required Libraries
- `numpy`
- `scipy`
- `scikit-learn`
- `tensorflow`
- `keras`
- `pywt`
- `matplotlib`
- `seaborn`
- `psutil`
- `gc`

=======================
## Usage Instructions
=======================
### Step 1: Load Data
- Load EEG data from .mat files using `scipy.io.loadmat`.
- Concatenate data from multiple subjects.

### Step 2: Preprocess Data
- Apply bandpass filtering using `scipy.signal.butter` and `scipy.signal.filtfilt`.
- Perform Common Average Referencing (CAR).
- Select specific EEG channels.
- Scale data using `RobustScaler` from `sklearn.preprocessing`.

### Step 3: Split Data into Classes
- Assign data to specific classes (Thumb, Index, Middle, Ring, Pinky) and balance classes.

### Step 4: Split Data into Training and Testing Sets 80 : 20
- Split data into training and testing sets using `train_test_split` from `sklearn.model_selection`.

### Step 5: Apply Continuous Wavelet Transform (CWT)
- Apply CWT to the EEG data using `pywt.cwt` with the Morlet mother wavelet.

### Step 6: Train and Evaluate  ML ,CNN, RNN Or hybrid Model
- Train model and evaluate its performance.
- Plot training and validation accuracy and loss.
- Generate confusion matrix and classification report using `sklearn.metrics`.

====================================================================================

Ensure you have access to the dataset and update the paths accordingly in the code. 
https://zenodo.org/records/4316450#.X9MdDrMRWUk

=====================================================================================


