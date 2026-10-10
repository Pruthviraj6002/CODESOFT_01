# SCT_ML_1 — Movie Genre Classification

**Internship Task 1 | Machine Learning**

## Overview

Build a machine-learning model that predicts a movie's genre from its plot summary. This project uses TF-IDF text features and a Linear Support Vector Classifier (LinearSVC).

## Repository structure

```text
SCT_ML_1/
├── data/
│   └── README.md
├── notebooks/
│   └── movie_genre_classification.ipynb
├── results/
│   └── README.md
├── .gitignore
├── README.md
└── requirements.txt
```

The `artifacts/` folder and result files are generated when you run the notebook.

## Dataset

Download the IMDb Genre Classification Dataset from Kaggle:

**Dataset link:** https://www.kaggle.com/datasets/hijest/genre-classification-dataset-imdb

Put `train_data.txt` inside the `data/` folder. The notebook expects the common dataset layout:

`ID ::: TITLE ::: GENRE ::: DESCRIPTION`

The description is the input text and genre is the target label. Please review the dataset license and terms before redistribution.

## Setup

Python 3.10–3.12 is recommended.

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
jupyter notebook
```

macOS/Linux:

```bash
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Open `notebooks/movie_genre_classification.ipynb` and run all cells.

## Methodology

1. Load and clean the dataset.
2. Explore the genre distribution.
3. Split into training and validation sets.
4. Extract word and character TF-IDF features.
5. Train a LinearSVC classifier.
6. Evaluate using accuracy, precision, recall, F1-score, and a confusion matrix.
7. Save model and evaluation outputs locally.

## Results

The notebook generates actual metrics after training and saves them under `results/`. No accuracy is claimed in advance; use the score from your own run in the internship report.

## Limitations

This baseline predicts one primary genre per movie. Since some movies have multiple genres, a multi-label model would be a useful future improvement.

## Suggested GitHub commit message

```text
Complete Task 01 - Movie Genre Classification
```
