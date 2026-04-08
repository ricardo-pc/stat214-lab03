# stat214-lab03

Follow the structure below:

lab3/
├── code/
│   ├── run.sh                        # master script, run everything in order - ONE PERSON SHOULD OWN THIS
│   ├── environment.yaml
│   │
│   ├── preprocessing.py              # PROVIDED — don't touch, just import
│   │
│   ├── embeddings/                   # Each member's scripts
│   │   ├── bow.py
│   │   ├── word2vec.py
│   │   ├── glove.py
│   │   ├── bert_pretrained.py
│   │   └── bert_finetuned.py         # includes LoRA variant
│   │
│   ├── models/                       
│   │   ├── ridge.py                  # training + cross-val logic
│   │   └── evaluation.py             # CC, percentiles, plots
│   │
│   ├── interpretation/               # Lab 3.3
│   │   ├── shap_analysis.py
│   │   └── lime_analysis.py
│   │
│   └── lab3.ipynb                    # final report notebook (or lab3.tex)
│
├── data/                             # GITIGNORE THIS — 20GB files
│   ├── raw/                          # original fMRI + story data, don't touch
│   │   ├── subject1_story1.npy
│   │   └── subject2_story1.npy
│   │
│   └── embeddings/                   # intermediate outputs from embedding scripts
│       # naming: {subject}_{split}_{method}_embeddings.npy
│       # subject: s1, s2
│       # split:   train, test
│       # method:  bow, word2vec, glove, bert, bert_finetuned
│       ├── s1_train_bow_embeddings.npy
│       ├── s1_test_bow_embeddings.npy
│       ├── s2_train_bow_embeddings.npy
│       ├── s2_test_bow_embeddings.npy
│       ├── s1_train_word2vec_embeddings.npy
│       ├── s1_train_glove_embeddings.npy
│       └── ...
│
├── results/
│   ├── models/                       # .pkl files for ridge models (required!)
│   │   # naming: {subject}_{method}_ridge.pkl
│   │   ├── s1_bow_ridge.pkl
│   │   ├── s1_word2vec_ridge.pkl
│   │   └── ...
│   │
│   └── metrics/                      # saved CSVs of CC scores
│       # naming: {subject}_{method}_cc_scores.csv
│       ├── s1_bow_cc_scores.csv
│       ├── s1_word2vec_cc_scores.csv
│       └── ...
│
├── figs/                             # all saved figures
│   # naming: {subject}_{method}_{what}.png
│   ├── s1_bow_cc_distribution.png
│   ├── s1_word2vec_cc_distribution.png
│   └── ...
│
├── documents/                        # Jain & Huth paper, any references
│
├── report/
│   ├── lab3.pdf
│   └── collaboration.txt             # required — who did what
│
└── other/
    └── (scratch notebooks, exploratory work)
