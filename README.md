# Pre-Seizure Classification Using CNN

This project applies deep learning techniques to classify **preictal (pre-seizure)** and **interictal (non-seizure)** EEG signals. A Convolutional Neural Network (CNN) model is used to detect patterns in short EEG segments and predict the likelihood of an impending epileptic seizure.
## 📚 Dataset: CHB-MIT Scalp EEG

This project uses the [CHB-MIT Scalp EEG Database](https://physionet.org/content/chbmit/1.0.0/), a well-known public dataset from PhysioNet. It contains long-term EEG recordings from pediatric epilepsy patients.

### Dataset Details
- Source: PhysioNet
- Format: `.edf` files
- Patients: 23 subjects with recorded seizure and non-seizure segments
- Sampling rate: 256 Hz

### How to Use
1. Visit the dataset: https://physionet.org/content/chbmit/1.0.0/
2. Download relevant patient `.edf` files (or use Python to do this automatically).
3. Organize your dataset as follows:
/dataset/
├── interictal/
│ ├── patient01_segment1.npy
│ ├── ...
└── preictal/
├── patient01_segment1.npy
├── ...

## 📁 Dataset
- EEG data is divided into:
  - `5s Preictal` segments (just before a seizure)
  - `5s Interictal` segments (normal periods)
- Data is expected to be placed in a `/dataset` folder.
- Originally prepared for seizure prediction across **multiple patients**.

## 🧠 Model
- A CNN model built using **TensorFlow/Keras**
- Takes EEG segments as input
- Trained to distinguish between preictal and interictal states

## 🔄 Workflow
1. Data preparation and labeling
2. Train-test split
3. CNN model design and training
4. Evaluation with metrics like accuracy, precision, recall
5. Visualizations and interpretation

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- TensorFlow
- NumPy
- Matplotlib
- Jupyter Notebook

### Run the Notebook
Clone the repo and open the notebook:

```bash
git clone https://github.com/your-username/preseizure-classification-cnn.git
cd preseizure-classification-cnn
jupyter notebook PreSeizureClassificationUsingCNN_Allpatient.ipynb
