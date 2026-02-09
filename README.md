# Predicitve-Analysis-Assignment5
# TOPSIS-Based Evaluation of Pre-trained Text Generation Models

This project implements a **multi-criteria decision-making framework** using **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** to evaluate and rank multiple **pre-trained language models** for **text generation tasks**.

Unlike single-metric evaluations, this approach considers **both generation quality and efficiency**, providing a balanced and interpretable comparison.

---

## 📌 Objectives

- Evaluate multiple pre-trained language models on diverse text generation prompts
- Measure performance using **multiple conflicting criteria**
- Apply **prompt-wise TOPSIS** to identify the best model per prompt
- Apply **overall TOPSIS** to rank models globally
- Visualize results using clear and interpretable plots

---

## 🧠 Models Evaluated

- GPT-2
- DistilGPT-2
- OPT-125M
- GPT-Neo-125M
- DialoGPT-small

All models are evaluated using the same prompts and generation settings for fairness.

---

## 📊 Evaluation Parameters

The following **five criteria** are used for TOPSIS:

| Parameter | Type |
|--------|------|
| BLEU | Benefit (+) |
| ROUGE-L | Benefit (+) |
| METEOR | Benefit (+) |
| Perplexity | Cost (−) |
| Inference Time (seconds) | Cost (−) |

Equal weights are assigned to all criteria (0.2)

---

## 🧪 Dataset

- 25 diverse **completion-style prompts**
- Each prompt includes a **reference continuation**
- Prompts are designed to avoid instruction bias and encourage fair comparison

---

## ⚙️ Methodology

1. Generate text for each `(prompt, model)` pair
2. Compute evaluation metrics at the **prompt level**
3. Apply **TOPSIS per prompt** to identify the best-performing model
4. Aggregate metrics across prompts
5. Apply **overall TOPSIS** to rank models globally
6. Visualize results using scatter and bar plots

---

## 📈 Results

- **Prompt-wise Best Model Plot**: Shows which model performs best for each prompt
- **Overall TOPSIS Ranking**: Ranks models based on balanced quality–efficiency trade-offs

DistilGPT-2 emerged as the top model due to strong efficiency and competitive generation quality.

---

## 🖥️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/ketannehra9/Predicitve-Analysis-Assignment5.git
cd Predicitve-Analysis-Assignment5
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
Open notebook/topsis_llm_evaluation.ipynb in Jupyter or Google Colab and execute all cells.
```


