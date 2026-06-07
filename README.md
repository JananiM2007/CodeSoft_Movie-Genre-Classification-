# Movie Genre Classification using Machine Learning

## Project Overview

This project develops a Machine Learning model that predicts the genre of a movie based on its title and plot summary. Natural Language Processing (NLP) techniques are used to transform textual data into numerical features, which are then used to train a classification model.

## Objectives

- Perform text preprocessing and cleaning on movie plot descriptions.
- Extract textual features using TF-IDF Vectorization.
- Train a machine learning model to classify movie genres.
- Evaluate model performance using standard classification metrics.
- Analyze important features contributing to genre prediction.

## Dataset

The dataset contains:

- Movie ID
- Movie Title
- Genre Label
- Movie Plot Summary

The dataset includes 27 genres such as Drama, Documentary, Comedy, Horror, Thriller, Action, Romance, Sci-Fi, Family, Adventure, Animation, Crime, Mystery, Fantasy, Western, Music, Musical, Sport, Talk-Show, Reality-TV, Biography, History, News, War, Game-Show, Adult, and Short.

## Data Preprocessing

The following preprocessing steps were applied:

- Converted text to lowercase
- Removed URLs
- Removed special characters and punctuation
- Removed numerical values
- Removed stop words
- Combined movie titles and plot descriptions
- Normalized textual content

## Feature Engineering

### Word-Level TF-IDF

- Unigrams, Bigrams, and Trigrams
- Maximum feature selection
- Sublinear TF scaling

### Character-Level TF-IDF

- Character n-grams (3–5)
- Captures sub-word patterns and textual structure

### Feature Combination

- Combined word-level and character-level TF-IDF features
- Improved representation of movie descriptions and titles

## Model Used

### Linear Support Vector Classifier (Linear SVC)

Model configuration:

- TF-IDF Feature Representation
- Balanced Class Weights
- Hyperparameter Optimization

## Model Evaluation

Evaluation metrics used:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report

### Results

| Model | Accuracy |
|---------|----------|
| Linear SVC | 58.5% |

The dataset contains 27 genres with significant class imbalance and overlapping genre characteristics, making the classification task challenging. The model successfully learned genre-specific patterns from movie plot summaries and titles.

## Feature Analysis

Examples of important keywords learned by the model:

| Genre | Top Features |
|---------|-------------|
| Horror | vampire, demon, zombie, haunted |
| Sci-Fi | alien, planet, future, space |
| Western | sheriff, outlaw, ranch |
| Music | concert, band, album |
| Thriller | murder, hacker, disappearance |

These features indicate that the model effectively captures genre-related vocabulary for classification.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- TF-IDF Vectorization
- Support Vector Machine (SVM)

## Project Structure

Movie-Genre-Classification/

├── train_data.txt

├── test_data.txt

├── test_data_solution.txt

├── Movie_Genre_Classification.ipynb

├── README.md

└── requirements.txt

## Future Improvements

- Fine-tune transformer-based models such as BERT
- Apply advanced feature selection techniques
- Address class imbalance using resampling methods
- Explore deep learning approaches for improved performance

## Conclusion

This project demonstrates the application of Natural Language Processing and Machine Learning techniques for multi-class movie genre classification. By combining TF-IDF feature extraction with a Linear SVM classifier, the model effectively learns genre-specific patterns from textual movie descriptions and titles.
