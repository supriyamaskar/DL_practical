
---

## 📊 Dataset

- Used a custom paraphrase dataset or **Quora Question Pairs** from Kaggle.
- [Kaggle Link](https://www.kaggle.com/competitions/quora-question-pairs/data)
- The dataset contains sentence pairs (original, paraphrase).

---

## 🏗️ Models Implemented

### 🔹 1. LSTM/GRU without Attention
- Standard encoder-decoder Seq2Seq model.
- Suitable for short sentences but lacks context awareness for long inputs.

### 🔹 2. LSTM/GRU with Bahdanau Attention
- Decoder dynamically focuses on relevant input tokens.
- Improves performance on long and complex sentences.

### 🔹 3. Transformer with Self-Attention
- Implements a minimal Transformer architecture.
- Parallelizable and good at capturing global dependencies.
- Underperformed due to small dataset size.

---

## 📈 Evaluation Metrics

Models were evaluated using:
- **BLEU Score**
- **ROUGE-1, ROUGE-2, ROUGE-L**
- **Inference Time per Sample**

| Model                     | BLEU    | ROUGE-1 | ROUGE-2 | ROUGE-L |
|--------------------------|---------|---------|---------|---------|
| LSTM/GRU (No Attention)   | 0.728   | 0.868   | 0.854   | 0.868   |
| LSTM/GRU (Bahdanau)       | 0.728   | 0.868   | 0.854   | 0.868   |
| Transformer (Self-Attention) | 0.293 | 0.353   | 0.320   | 0.353   |

---

## 📦 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
