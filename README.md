# stat214-lab03

## Folder Structure

```
lab3/
├── code/
│   ├── run.sh               # master script - ONE PERSON OWNS THIS
│   ├── environment.yaml
│   ├── preprocessing.py     # PROVIDED — do not modify
│   ├── embeddings/
│   │   ├── bow.py
│   │   ├── word2vec.py
│   │   ├── glove.py
│   │   ├── bert_pretrained.py
│   │   └── bert_finetuned.py
│   ├── models/
│   │   ├── ridge.py
│   │   └── evaluation.py
│   ├── interpretation/
│   │   ├── shap_analysis.py
│   │   └── lime_analysis.py
│   └── lab3.ipynb
├── data/                    # GITIGNORED — do not commit
│   ├── raw/
│   └── embeddings/
├── results/
│   ├── models/
│   └── metrics/
├── figs/
├── documents/
├── report/
│   ├── lab3.pdf
│   └── collaboration.txt
└── other/
```

## Naming Conventions

| Type | Pattern | Example |
|------|---------|---------|
| Embeddings | `{subject}_{split}_{method}_embeddings.npy` | `s1_train_bow_embeddings.npy` |
| Models | `{subject}_{method}_ridge.pkl` | `s1_bow_ridge.pkl` |
| Metrics | `{subject}_{method}_cc_scores.csv` | `s1_bow_cc_scores.csv` |
| Figures | `{subject}_{method}_{what}.png` | `s1_bow_cc_distribution.png` |

**Subjects:** `s1`, `s2` — **Splits:** `train`, `test` — **Methods:** `bow`, `word2vec`, `glove`, `bert`, `bert_finetuned`
