# Voice-based Stress Detection

This project focuses on detecting stress in human speech by classifying audio recordings into **Stressed** and **Not-Stressed** categories using **MFCC feature extraction** and **Random Forest classification**.

[Kaggle Link](https://www.kaggle.com/code/medhavitripathi/voice-based-stress-detection)  
[Link to Dataset](https://www.kaggle.com/datasets/barelydedicated/savee-database)

The dataset contains **audio samples of 7 emotions** spoken by four male English speakers, recorded as part of the **SAVEE (Surrey Audio-Visual Expressed Emotion)** database.

- **Name:** SAVEE Database  
- **Classes:** `Anger`, `Disgust`, `Fear`, `Happiness`, `Neutral`, `Sadness`, `Surprise`  
- **Mapped Labels:** `Stressed`, `Not-Stressed`  
- **Total Samples:** 480 (120 per speaker)  
- **Audio Type:** `.wav` voice recordings with acted emotional speech

---

## Project Structure

- **Audio Feature Extraction**:
  - Loaded audio files using `librosa`
  - Extracted **MFCCs (Mel Frequency Cepstral Coefficients)** as features
  - Computed mean MFCCs per file as fixed-length feature vectors

- **Label Mapping**:
  - Grouped `Anger`, `Disgust`, `Fear`, `Sadness` as **Stressed**
  - Grouped `Neutral`, `Happiness`, `Surprise` as **Not-Stressed**

- **Data Splitting**:
  - Used `train_test_split` to create 80-20 train-test sets

- **Model Training using ML Algorithms**:
  - Random Forest Classifier:
    - 100 estimators with fixed random state
    - Trained to classify stress labels from MFCC features

- **Model Evaluation and Performance Analysis**:
  - Classification Report (Precision, Recall, F1-score)
  - Confusion Matrix for predicted vs actual labels
  - Emotion and stress label distribution graphs for insight

---

## Technologies and Tools

- **Languages**: Python  
- **Libraries**: Librosa, NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn
- **Platform**: Kaggle
