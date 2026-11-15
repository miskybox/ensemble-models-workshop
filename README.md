# Ensemble Models: one tree or the whole bench?

Workshop notebook (in Spanish) comparing a single decision tree with ensemble models,
using a football example: **does the home team win?**

Models compared:

- Decision tree (single model, baseline)
- Bagging
- Random Forest
- Gradient Boosting
- Voting (logistic regression + KNN + Random Forest)

The data is **simulated** with a realistic formula, so the demo runs offline.

## Results (test set, 750 matches)

| Model | Train accuracy | Test accuracy |
|---|---|---|
| Gradient Boosting | 81.6 % | 75.7 % |
| Random Forest | 86.7 % | 74.9 % |
| Voting (soft) | 79.5 % | 74.5 % |
| Bagging (100 trees) | 100 % | 72.4 % |
| Decision tree, max_depth=4 | 74.2 % | 71.1 % |
| Decision tree, unlimited | 100 % | 64.9 % |

## How to run

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
```

Open `ensembles_futbol.ipynb` in VS Code (Python + Jupyter extensions), select the `.venv`
kernel and click **Run All**. It also runs in Google Colab.
