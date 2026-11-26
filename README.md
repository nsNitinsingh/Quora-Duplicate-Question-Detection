# Quora Duplicate Question Detection

## 1. Project Overview

This project uses Machine Learning and NLP to identify whether two Quora questions have the same meaning.

For example:

- Question 1: How can I learn Python?
- Question 2: What is the best way to learn Python?

The model predicts whether the two questions are duplicates.

## 2. Dataset

- Dataset: Quora Question Pairs (Kaggle)
- Total question pairs: 404,290
- Target column: `is_duplicate`
- 0 = Not Duplicate
- 1 = Duplicate

## 3. Project Steps

I divided the project into four notebooks:

1. **EDA.ipynb:** Explored the dataset and understood the questions.
2. **bowsimplest.ipynb:** Built a basic model using Bag of Words.
3. **bow_basic_features.ipynb:** Added 7 basic features about the questions.
4. **bow_advanced_features.ipynb:** Added 22 features to improve model performance.

## 4. Features Used

I used two types of features:

- **Bag of Words:** Converts text into numerical values.
- **Feature Engineering:** Extracts information such as word count, common words, question length and text similarity.

## 5. Models Used

- Random Forest
- XGBoost

## 6. Results

| Model | Accuracy |
|---|---:|
| Random Forest (Basic BoW) | 74.23% |
| XGBoost (Basic BoW) | 73.57% |
| Random Forest (Advanced BoW) | **80.40%** |
| XGBoost (Advanced BoW) | 79.79% |

Additional evaluation of Random Forest:

- Precision: 76.19%
- Recall: 67.96%
- F1-score: 71.84%

Random Forest gave the best accuracy among the two advanced models.

## 7. Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- NLTK
- XGBoost
- FuzzyWuzzy

## 8. How to Run

1. Clone the repository.
2. Install the required libraries using `requirements.txt`.
3. Download the dataset from Kaggle.
4. Open Jupyter Notebook.
5. Run the notebooks in the order mentioned in Project Steps.

## 9. Conclusion

This project helped me understand how NLP and Machine Learning can be used to compare questions.

By adding more features to Bag of Words, I improved the Random Forest model's accuracy to 80.40%.
