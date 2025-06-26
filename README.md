# COMP0078 — Supervised Learning • Coursework 2  
MSc in Machine Learning, University College London (2024 / 25)

This repository contains all the material submitted for **Coursework 2** of the COMP0078 *Supervised Learning* module.  
It includes:

| Path | Description |
|------|-------------|
| `main.tex`          | LaTeX source of the written report (compiled PDF shows all answers, figures and tables). |
| `images/`           | Auxiliary figures referenced by `main.tex`. |
| `code_supervised_learning_coursework_2.ipynb` | Jupyter notebook implementing every experiment required in the coursework. |
| `dataset.csv`       | Dataset used in all parts of the coursework. |
| `Coursework2_Task.pdf` | The questions of the coursework  |

---

## Quick-start

```bash
# 1. Clone the repo
git clone https://github.com/BenoitCou/UCL-COMP0078-Supervised-Learning-Coursework-2
cd UCL-COMP0078-Supervised-Learning-Coursework-2

# 2. Create & activate a virtual environment  (optional but recommended)
python -m venv .venv

# Install Python dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook code_supervised_learning_coursework_2.ipynb
```

Necessary files for the coursework are available here: http://www0.cs.ucl.ac.uk/staff/M.Herbster/SL/misc/

## Compiling the report
```bash
latexmk -pdf main.tex
```

## Coursework Overview

**Part I – Rademacher complexity (20 % of mark)** 

- **Sub-Gaussian max bound** — proved  
  \( \displaystyle \mathbb{E}[\max_{1\le i\le m} X_i] \;\le\; \tfrac{b-a}{2}\sqrt{2\log m} \)  
  via Hoeffding’s lemma.  
- **Finite-class Rademacher complexity** — chained five lemmas to derive  
  \( \displaystyle \widehat{\mathfrak{R}}_S(H)=O\!\bigl(\sqrt{\tfrac{\log|H|}{n}}\bigr) \)  
  for any finite hypothesis class \(H\).

**Part II – Bayes rule & surrogate losses (40 %)**  

- **Population minimisers** — closed-form \(f^{\*}\) for squared, exponential, logistic and hinge losses.  
- **Bayes decision rule** — recovered \(c^{\*}(x)=\text{sign}\bigl(2\eta(x)-1\bigr)\) with  
  \( \eta(x)=\mathbb{P}(y=1\mid x) \).  
- **Fisher-consistency proofs** — explicit decoding maps \(d(f)\) for each loss.  
- **Comparison inequality** — established  
  \(R(\text{sign}f)-R(\text{sign}f^{\*})\le\sqrt{E(f)-E(f^{\*})}\)  
  through Questions 2.5.1 – 2.5.3.  

**Part III – Kernel perceptron on handwritten digits (40 %)**  

- **Multi-class kernel perceptron** — implemented *one-vs-rest* (OvR) baseline; optional *one-vs-one* (OvO).  
- **Polynomial kernel study**  
  - 20 random 80 / 20 train-test splits, degrees \(d=1\!:\!7\).  
  - Mean ± s.d. train/test errors logged (Q3).  
  - 5-fold CV to select \(d^{\*}\); histogram of chosen degrees (Q4).  
- **Gaussian kernel study** — repeated the same protocol over a log-grid of widths \(c\) (Q7).  
- **Error analysis**  
  - 10 × 10 confusion matrix averaged over 20 runs (Q5).  
  - Visualisation of the five hardest digits with commentary on failure modes (Q6).  
- **OvO vs OvR comparison** — contrasted accuracy and training time (Q8).  

## Marks obtained

*Grade*: 100/100

| Question | Score   | Comments   |
| -------- | ------- | ---------- |
| Q1.1     | 2 / 2   |            |
| Q1.2     | 5 / 5   |            |
| Q1.3     | 3 / 3   |            |
| Q1.4     | 3 / 3   |            |
| Q1.5     | 7 / 7   |            |
| Q2.1     | 4 / 4   |            |
| Q2.2     | 4 / 4   |            |
| Q2.3     | 4 / 4   |            |
| Q2.4     | 4 / 4   |            |
| Q2.5.1   | 8 / 8   |            |
| Q2.5.2   | 8 / 8   |            |
| Q2.5.3   | 8 / 8   |            |
| Q3       | 40 / 40 | Well done! |

   
