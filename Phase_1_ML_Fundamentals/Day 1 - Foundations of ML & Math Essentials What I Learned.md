# Day 1 - Foundations of ML & Math Essentials: What I Learned

Nov 13, 2026 Himanshu Choyal

## Core idea: supervised learning

Supervised learning learns a mapping from inputs (features) to known answers (labels).

We hold data back for validation and testing, so the score reflects unseen seasons, not memorised ones.

## Math: mean, variance and standard deviation

- **Mean:** the average yield, in t/ha.
- **Variance:** how far yields spread from the mean, on average, squared.
- **Standard deviation:** the square root of variance, so it is in the same units as yield.

I reported yield as mean ± standard deviation.

## Colab exercise: 80/20 split in pure NumPy

- Dataset: Kaggle, Crop Yield Prediction (crop yield vs rainfall).
- Shuffled row indices with a seeded generator (`default_rng(0)`), then cut at 80%.
- Computed the training-set mean, variance and standard deviation of yield.
- Runtime: free CPU is enough.

Notebook: \[paste your Colab link here\]

## Watch out

If I predict future seasons, I should split by year instead of shuffling blindly. Shuffling lets the model see later seasons during training, which inflates the score.

## Sources

- Dataset: Kaggle, "Crop Yield Prediction" - "yeild_df.csv" [https://www.kaggle.com/datasets/patelris/crop-yield-prediction-dataset?resource=download&select=yield_df.csv]
- Colab notebook: [https://colab.research.google.com/drive/1nCG2hJ_UamR8SJRIoBtVQSns97U1D_wE?usp=sharing]
