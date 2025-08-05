# 🌐 Hinglish to English Translator using LLMs

This project implements a translation pipeline that converts code-mixed **Hinglish** (Hindi-English) sentences into fluent, grammatically correct English using transformer-based **Large Language Models (LLMs)**.

> 🧠 Built during internship at CDSAML (Centre for Data Science and Applied Machine Learning), PES University.

---
hinglish-translator-llm/
├── README.md
├── hinglish_to_english.ipynb
├── dataset/                (optional: if you have a sample)
│   └── sample_data.csv
├── requirements.txt        (optional: for dependencies)
└── results/
    └── bleu_score_log.txt  (optional: performance metrics)


## 📌 Overview

- Fine-tuned [mBART](https://huggingface.co/facebook/mbart-large-50-many-to-many-mmt) model using **Hugging Face Transformers**.
- Trained on a custom Hinglish-English dataset.
- Achieved **BLEU score** improvement from `25.6 ➝ 31.62`.

---

## 🛠️ Tech Stack

- Python
- Hugging Face Transformers
- Google Colab (GPU-enabled)
- Pandas, NumPy, NLTK (for preprocessing)
- BLEU Scoring for evaluation

---

## 🔄 Workflow

1. **Data Preprocessing**  
   Tokenization, noise removal, and alignment of Hinglish-English pairs.

2. **Model Fine-tuning**  
   Used mBART on Hugging Face with pre-trained weights.

3. **Evaluation**  
   Measured BLEU scores to evaluate translation accuracy.

---

## 📊 Results

| Metric        | Baseline | Final  |
|---------------|----------|--------|
| BLEU Score    | 25.6     | 31.62  |

> ⚡ Significant improvement after fine-tuning on domain-specific data.

---

```bash
pip install transformers datasets nltk
python hinglish_to_english.py
