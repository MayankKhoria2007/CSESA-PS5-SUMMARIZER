# 📄 Hybrid Text Summarizer using T5 and TextRank

## 🔍 Project Overview

This project implements a **Hybrid Text Summarization System** that combines:

- **Extractive Summarization** using **TextRank**
- **Abstractive Summarization** using a **T5 Transformer model**

The hybrid approach first selects the most important sentences using TextRank and then generates a fluent abstractive summary using T5.

---

## 🧠 Architecture

Input Text → Preprocessing → TextRank → Top Sentences → T5 → Final Summary

---

## 🚀 Features

- Hybrid summarization (Extractive + Abstractive)
- Uses **T5-Small** transformer
- Lemmatization and text preprocessing
- Sentence ranking with cosine similarity + PageRank
- Evaluation using **ROUGE** and **BERTScore**
- Google Colab compatible

---

## 📂 Repository Structure

├── SUMMARIZERT5HYBRIDWITHTEXTRANK.ipynb  
├── README.md  

---

## 📦 Dependencies

```bash
pip install transformers datasets torch nltk scikit-learn networkx evaluate rouge-score bert-score
```

---

## 📊 Dataset

**BIG PATENT Dataset (subset A)**  
Loaded from Hugging Face:
```python
load_dataset("NortheasternUniversity/big_patent", "a")
```

---

## 🛠️ Model Configuration

- Model: T5-Small
- Max input length: 512
- Max output length: 128
- Learning rate: 2e-4
- Epochs: 4

---

## 🧪 Evaluation Metrics

- ROUGE-1
- ROUGE-2
- ROUGE-L
- BERTScore (Precision, Recall, F1)

---

## ▶️ How to Run

1. Open the notebook in Jupyter or Google Colab
2. Run all cells sequentially
3. Provide input text to generate summaries

---

## ✨ Example

```python
text = "Artificial intelligence is transforming modern applications..."
print(hybrid_summarizer_pipeline(text))
```

---

## 🧑‍💻 Author

**Mayank Khoria**

---

## 📄 License

Academic and educational use only.
