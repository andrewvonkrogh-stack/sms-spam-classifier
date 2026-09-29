# SMS Spam Classifier

A Python machine-learning project that classifies text messages as spam or legitimate (“ham”), with an emphasis on avoiding false positives: legitimate messages incorrectly flagged as spam.

## Current progress

- Explored 5,574 labeled messages.
- Checked for missing values and conflicting labels.
- Removed 403 exact duplicate message texts, leaving 5,171 unique messages.
- Split the cleaned data into training, validation, and test sets.
- Trained a TF-IDF and logistic regression classifier.
- Investigated the model’s false positives.

## Validation results

| Outcome | Messages |
|---|---:|
| Legitimate messages correctly kept | 902 |
| Legitimate messages incorrectly flagged | 2 |
| Spam correctly caught | 89 |
| Spam missed | 41 |

The model achieved 97.8% spam precision and 68.5% spam recall on the validation set. It rarely flagged legitimate messages, but missed nearly one-third of the spam.

These are preliminary validation results. The final test set has not been evaluated.

## How to run

1. Download the [UCI SMS Spam Collection](https://archive.ics.uci.edu/dataset/228/sms+spam+collection).
2. Extract `SMSSpamCollection` into a `data` folder beside `exploration.ipynb`.
3. Open `exploration.ipynb` in VS Code with the Python and Jupyter extensions.
4. Select a Python environment and run the notebook cells from top to bottom. The first code cell installs pandas and scikit-learn.

## Limitations and next steps

This project uses a historical SMS dataset, so its results may not reflect modern messages. Removing exact duplicates does not eliminate near-duplicate messages.

Next steps include exploring the tradeoff between catching spam and protecting legitimate messages, then evaluating the chosen approach on the held-out test set.

## Dataset credit

Almeida, T. & Hidalgo, J. (2011). *SMS Spam Collection*. UCI Machine Learning Repository. https://doi.org/10.24432/C5CC84

Dataset licensed under CC BY 4.0.