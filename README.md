# Grammar-scoring-Engine
Google Colab link: https://colab.research.google.com/drive/1QIlDj7GQ7mXpmPfDj0sCmBFqs6MQnTNw?usp=sharing

✅ Project Summary:

-  Developed a Grammar Scoring Engine using audio features.
- Feature extraction included MFCCs, Zero Crossing Rate, Spectral Centroid, and more.
- Used RandomForestRegressor with Hyperparameter Tuning.
- Final evaluation on validation set gave:
    - RMSE: 0.9796
    - R^2 Score: 0.1693
    - Pearson Correlation: 0.4212
- Visualizations showed important features and performance insights.
- Final submission file generated and ready!

Future Improvements:
- Try advanced models like XGBoost or Deep Learning models.
- Use data augmentation for audio.
- Extract advanced linguistic features (optional).

Here's a **well-structured and detailed `README.md` file** explicitly tailored for your uploaded Colab notebook and the project description you shared:

---

## 📘 README.md

# 🎓 Grammar Scoring Engine for Spoken English

This project aims to build a Grammar Scoring Engine that evaluates short spoken English audio clips (45–60 seconds) and predicts a continuous score between 0 and 5** based on grammar quality. The model is trained using a labeled dataset of human-scored audio files and evaluated based on Pearson correlation.

---

## 📂 Dataset Overview

The dataset consists of the following components:

### 🎧 Audio Files
- `audios_train/`: 444 training audio samples in `.wav` format.
- `audios_test/`: 195 testing audio samples (used for inference).

### 📄 CSV Files
- `train.csv`: Contains `file_name` and the corresponding grammar score (labels).
- `test.csv`: Contains `file_name` for test samples with dummy labels.
- `sample_submission.csv`: Format required for test predictions.

---

## 📊 Grammar Scoring Rubric

| Score | Description |
|-------|-------------|
| **1** | Severe grammar issues, broken sentence structures |
| **2** | Frequent grammatical mistakes with limited structures |
| **3** | Some grammatical control, but regular syntax errors |
| **4** | Strong grammar, with few minor errors |
| **5** | Excellent grammar, confident use of complex structures |

---

## 🛠️ Project Structure

| Cell No. | Section |
|----------|---------|
| **1–5** | Import libraries and check hardware availability |
| **6–8** | Dataset loading and basic exploration |
| **9–14** | Audio visualizations – waveform, spectrograms, MFCC |
| **15–20** | Feature extraction using MFCC |
| **21–25** | Data preparation and train-test split |
| **26–29** | Model architecture using PyTorch |
| **30** | Training loss visualization |
| **31–33** | Model evaluation using Pearson correlation |
| **34+** | Prediction on test data and sample submission generation |

---

## 🧪 Model Details

- **Framework**: PyTorch
- **Features Used**: MFCCs extracted via `librosa`
- **Model**: Simple Feedforward Neural Network with fully connected layers
- **Loss Function**: Mean Squared Error Loss (MSE)
- **Evaluation Metric**: Pearson Correlation Coefficient

---

## 📈 Evaluation

- The model is evaluated using **Pearson correlation** between predicted scores and actual scores on the validation set.
- The final inference is done on the provided `audios_test/` data, and a CSV is generated in the correct submission format.

---

## 📌 Instructions to Run

1. **Mount Google Drive in Colab**  
   Ensure the dataset is placed under `MyDrive/GrammarScoring/`.

2. **Verify Paths in Code**  
   Update paths in the notebook to:
   ```python
   base_path = '/content/drive/MyDrive/GrammarScoring'
   train_audio_folder = f'{base_path}/audios_train'
   test_audio_folder = f'{base_path}/audios_test'
   ```

3. **Run Cells Sequentially**  
   Execute cells from top to bottom. Ensure MFCC extraction, model training, and evaluation completed successfully.

4. **Generate Submission File**  
   Once test predictions are ready, export them using the format in `sample_submission.csv`.

---

## 📊 Visualizations

- **Waveform and Spectrograms** of audio clips help understand the signal behavior.
- **MFCC Heatmaps** highlight key frequency features used for modeling.
- **Loss Curves** track training progression.
- **Pearson Correlation Visualization** for performance understanding.

---

## 📝 Future Enhancements

- Integrate pre-trained audio models (e.g., Wav2Vec2).
- Use attention mechanisms or RNNs for sequential modeling.
- Incorporate linguistic features (POS tags, grammar parsers) via speech-to-text.
- Hyperparameter tuning & model ensembling for better accuracy.

---

## 👨‍💻 Contributors

- **Your Name** – Model development, analysis, and visualization.

---

## 📜 License

This project is part of a Machine Learning competition and is intended for educational use.

---

Let me know if you'd like a Markdown file copy, or if you want your name/email/GitHub added under contributors!
