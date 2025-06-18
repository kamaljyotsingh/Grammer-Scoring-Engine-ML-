# 🧠 Grammar Scoring Engine 🎤

A lightweight and efficient grammar scoring engine for evaluating spoken English using **speech-to-text** and **natural language processing**. This project was built as part of a Kaggle competition to predict **MOS Likert grammar scores (0 to 5)** based on audio inputs.

---

## 📌 Features

- 🎙️ **Speech-to-text** using [OpenAI Whisper](https://github.com/openai/whisper)
- 🧮 **Grammar analysis** using `nltk` and statistical language rules
- 📊 **Regression model** to predict grammar scores on a continuous scale
- 🎧 Audio recording via `sounddevice` or loading `.wav` files
- ⚡ Simple, fast, and bug-free Python implementation

---

## 🧪 How It Works

1. **Audio Input**: Takes `.wav` audio files as input (or record via microphone).
2. **Transcription**: Converts speech to text using Whisper ASR.
3. **Grammar Processing**: Uses POS tagging, parse trees, and grammar rules to extract features.
4. **Scoring**: Predicts a grammar score from 0 to 5 using a trained model (Linear Regression, XGBoost, etc.).

---

## 🗂️ Project Structure

```
grammar-scoring-engine/
│
├── notebook.ipynb         # Main Jupyter notebook
├── utils.py               # Utility functions
├── model.pkl              # Trained model (if applicable)
├── requirements.txt       # Python dependencies
├── audio_samples/         # Audio test files
├── report.md              # Summary report (for Kaggle)
├── README.md              # You are here
└── .gitignore             # Common ignores
```

---

## 🚀 Getting Started

### 🔧 Prerequisites

- Python 3.8+
- pip

### 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

> Whisper may require additional setup. Visit [Whisper GitHub](https://github.com/openai/whisper) for details.

### ▶️ Run the Notebook

Open and run:

```bash
jupyter notebook notebook.ipynb
```

Or run directly in Python (basic version):

```bash
python main.py
```

---

## 🧠 Model Training (Optional)

You can retrain the grammar scoring model on your dataset:

```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
```

Save model:
```python
import joblib
joblib.dump(model, 'model.pkl')
```

---

## 📈 Example Output

| Audio File       | Transcription               | Predicted Grammar Score |
|------------------|-----------------------------|--------------------------|
| sample_001.wav   | "She go to market."         | 2.0                      |
| sample_002.wav   | "He went to the market."    | 4.7                      |

---

## 📑 Report Summary

This project uses NLP-based features such as:
- Grammatical errors
- Sentence structure complexity
- POS tag frequency
- Fluency metrics from Whisper timestamps

---

## 🧪 Evaluation Metric

The final score is predicted on a **continuous scale from 0 to 5** based on **Mean Squared Error (MSE)**.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss improvements.

---

## 📜 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## ✍️ Author

**Kamal Jyot Singh Anand**  
📧 kamaljyotsingh@gmail.com  
🌐 [LinkedIn](https://www.linkedin.com/in/kamal-jyot-singh-8900b9247/) • [GitHub](https://github.com/kamaljyotsingh)

---

## ⭐ Acknowledgments

- [OpenAI Whisper](https://github.com/openai/whisper)
- [NLTK](https://www.nltk.org/)
- [Scikit-learn](https://scikit-learn.org/)
- Kaggle Grammar Scoring Competition
