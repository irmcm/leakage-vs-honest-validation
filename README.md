# Leakage vs honest validation

A short study on what happens to a regression score when the data is split
correctly instead of randomly.

## The question

The UCI Parkinson's Telemonitoring dataset contains around 200 voice
recordings from each of 42 patients, and the task is to predict a clinical
severity score from voice measures. Because recordings are repeated per
patient, a random split places the same patient on both sides of the split.
The model can then recognise the patient rather than the condition.

The intended use of such a model is a patient it has never heard before.
This repo compares three evaluation setups to see how much of the reported
performance survives that requirement.

## Setups compared

1. **Random K-Fold** — rows split randomly, patients appear in both folds
2. **GroupKFold by patient** — no patient appears in both train and test
3. **GroupKFold with feature selection inside the CV loop** — selection
   repeated within each fold instead of once on the full dataset

## Results

_to be filled_

## Reproducing

Open the notebook in Colab, or install `requirements.txt` and run it locally.
The dataset is downloaded automatically.

## Author

İrem Nur Ceylan — MSc Computer Engineering, Ege University
