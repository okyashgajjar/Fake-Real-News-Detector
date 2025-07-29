# 📰 Fake-Real News Detector

A machine learning-powered web application that analyzes news articles and predicts whether they are REAL or FAKE. Built with Streamlit, the app allows you to enter news content manually or upload files in PDF, DOCX, PPTX, or TXT format for instant analysis.

---

## 🚀 Features

- **Manual News Input:** Enter a news title and content directly into the app.
- **File Upload Support:** Upload news articles as PDF, Word (DOCX), PowerPoint (PPTX), or plain TXT files.
- **Intelligent Preprocessing:** The app automatically extracts and cleans text from various document types.
- **State-of-the-art Model:** Utilizes a `RidgeClassifier` trained on a labeled dataset of real and fake news.
- **Fast & User-Friendly:** Simple, clean Streamlit interface for quick analysis.
- **Clear Prediction Results:** Get instant feedback on whether the news appears REAL or FAKE.
- **Open Source:** Easily customizable for your own datasets or use cases.

---

## 🛠️ How It Works

1. **Text Preprocessing:** The news content is cleaned (lowercased, punctuation removed, etc.).
2. **Text Vectorization:** The cleaned text is converted into numerical features using a pre-trained TF-IDF vectorizer.
3. **Prediction:** The loaded RidgeClassifier model predicts if the news is REAL (1) or FAKE (0).
4. **Result Display:** The app shows the result with clear messaging and allows you to inspect the analyzed text.

---

## 🏗️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/OkYashGajjar/Fake-Real-News-Detector.git
cd Fake-Real-News-Detector
```

### 2. Install dependencies

It is recommended to use a virtual environment.

```bash
pip install -r requirements.txt
```

**Main dependencies:**
- streamlit
- scikit-learn
- pandas
- numpy
- python-docx
- python-pptx
- PyMuPDF (fitz)

### 3. Download Model Files

Make sure the following files are present in your project directory:

- `News_Predictor_model_RidgeClassifier_.pkl` (the trained model)
- `tfid_Text_vectorizer.pkl` (the fitted TF-IDF vectorizer)

> **Note:** If you want to retrain the model, all training code is available in `fake_real_predictor.ipynb`.

### 4. Run the App

```bash
streamlit run app.py
```

---

## 🖥️ Usage

1. Open the Streamlit app in your browser (it will usually auto-open).
2. Select your input method in the sidebar:
    - **Manual Input**: Type or paste the news title and content.
    - **Upload File**: Upload a news article in PDF, DOCX, PPTX, or TXT format.
3. Click the **Detect** button.
4. View the prediction and inspect the analyzed text if desired.

---

## 📂 File Structure

```
Fake-Real-News-Detector/
├── app.py                         # Main Streamlit app
├── fake_real_predictor.ipynb      # Model training and analysis notebook
├── News_Predictor_model_RidgeClassifier_.pkl  # Trained model
├── tfid_Text_vectorizer.pkl       # TF-IDF vectorizer for text
├── requirements.txt               # Python dependencies
├── README.md                      # This file
└── ...                            # Additional files (data, etc.)
```

---

## 🧠 Model Details

- **Algorithm:** RidgeClassifier
- **Vectorizer:** TfidfVectorizer (max_features=20000, English stopwords)
- **Training Data:** Combination of labeled real and fake news datasets, with preprocessing and cleaning steps (see notebook for details).
- **Accuracy:** Test accuracy ~99.3% (see `fake_real_predictor.ipynb` for metrics and confusion matrix).

---

## ⚠️ Disclaimer

- This model is trained on a specific dataset and may not generalize perfectly to all types of news or all topics.
- It is intended for educational and research purposes only. Always verify news from trusted sources.

---

## 📈 Example

### Manual Input

```
Title: "NASA Confirms Discovery of a New Earth-Like Planet"
Content: "In a historic announcement, NASA revealed the discovery of an exoplanet with Earth-like characteristics..."
```

Output:  
✅ This news appears to be REAL.

---

## 🤝 Contributing

Pull requests and suggestions are welcome!  
Feel free to fork the repository and submit improvements.

---

## 📄 License

This project is licensed under the MIT License.

## ✉️ Author

Made with ❤️ by [OkYashGajjar](https://github.com/OkYashGajjar)

---
