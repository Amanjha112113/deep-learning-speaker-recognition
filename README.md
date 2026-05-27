# 🎙️ Deep Learning Speaker Recognition

A beginner-friendly Deep Learning project for speaker recognition using MFCC feature extraction and TensorFlow.

This project identifies whether a voice belongs to:
- `person1`
- `person2`
- `unknown speaker`

The system extracts audio features using **MFCC (Mel Frequency Cepstral Coefficients)** and trains a Deep Neural Network for speaker classification.

---

# 🚀 Features

- Speaker Recognition using Deep Learning
- MFCC Audio Feature Extraction
- Unknown Speaker Detection
- TensorFlow / Keras Neural Network
- Audio Classification Pipeline
- Model Saving & Prediction System
- Beginner-Friendly Implementation

---

# 🧠 Project Workflow

```text
Voice Input
    ↓
MFCC Feature Extraction
    ↓
Deep Neural Network
    ↓
Speaker Prediction
```

---

# 📂 Dataset Used

Dataset:
Speaker Recognition Dataset from Kaggle

Source:
https://www.kaggle.com/datasets/kongaevans/speaker-recognition-dataset

---

# 👥 Classes Used

## Known Speakers
- person1 → Jens_Stoltenberg
- person2 → Benjamin_Netanyau

## Unknown Speakers
- Nelson_Mandela
- Julia_Gillard
- Magaret_Tarcher

The unknown speakers were grouped into a single `unknown` class.

---

# 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- Librosa
- NumPy
- Scikit-learn
- KaggleHub

---

# 🎵 Audio Processing

The project uses:

## MFCC (Mel Frequency Cepstral Coefficients)

MFCCs help convert raw audio into meaningful numerical features representing:
- frequency patterns
- speech characteristics
- vocal information

### Configuration

```python
N_MFCC = 40
MAX_PAD_LEN = 100
SAMPLE_RATE = 16000
```

---

# 🧱 Deep Learning Model Architecture

```text
Input Layer (4000 Features)
        ↓
Dense Layer (256) + ReLU
        ↓
Dropout (0.3)
        ↓
Dense Layer (128) + ReLU
        ↓
Dropout (0.3)
        ↓
Dense Layer (64) + ReLU
        ↓
Output Layer (3 Classes)
```

---

# 📊 Model Summary

| Layer | Output Shape | Parameters |
|---|---|---|
| Dense (256) | (None, 256) | 1,024,256 |
| Dropout | (None, 256) | 0 |
| Dense (128) | (None, 128) | 32,896 |
| Dropout | (None, 128) | 0 |
| Dense (64) | (None, 64) | 8,256 |
| Dense (3) | (None, 3) | 195 |

## Total Parameters
`1,065,603`

---

# 📈 Model Performance

## Test Accuracy

```text
99.40%
```

Example Prediction:

```text
PREDICTION RESULT

Predicted Speaker : person1
Confidence Score  : 1.0
```

---

# ⚠️ Important Notes

The high accuracy is achieved on the selected dataset and controlled audio conditions.

Real-world speaker recognition is significantly harder because of:
- background noise
- microphone differences
- different recording environments
- voice changes
- unseen speakers

This project is designed primarily for:
- learning Deep Learning
- understanding audio preprocessing
- building speaker recognition pipelines

---

# 📦 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/deep-learning-speaker-recognition.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# ▶️ Run The Project

Open the notebook:

```bash
speaker_recognition.ipynb
```

Train the model and test predictions using audio files.

---

# 💾 Model Saving

The trained model is saved using the modern Keras format:

```python
model.save("speaker_recognition_model.keras")
```

---

# 🔮 Future Improvements

Possible future upgrades:
- CNN-based spectrogram models
- Speaker embeddings
- Siamese Networks
- Triplet Loss
- Real-time microphone inference
- Noise robustness
- Transformer-based speech models
- Open-set speaker verification

---

# 📁 Project Structure

```text
deep-learning-speaker-recognition/
│
├── speaker_recognition.ipynb
├── speaker_recognition_model.keras
├── requirements.txt
├── README.md
└── .gitignore
```

---

# 🎯 Learning Outcomes

This project helped in understanding:
- Audio preprocessing
- MFCC extraction
- Deep Learning workflows
- Multi-class classification
- Model training and evaluation
- Speaker recognition fundamentals

---

# 📜 License

This project is for educational and learning purposes.
