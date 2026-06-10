# MOVIE-SENTIBOT: NLP-Based Solution for Movie Review Sentiment Analysis

## Overview
MOVIE-SENTIBOT is an NLP-based machine learning project designed to analyze movie reviews and classify them as positive or negative. This project is developed as part of the IT2011 Group Assignment for Artificial Intelligence and Machine Learning at the Sri Lanka Institute of Information Technology (SLIIT). The focus of Progress Review I is on data cleaning, preprocessing, and Exploratory Data Analysis (EDA), with each team member handling a specific preprocessing technique. The project uses the IMDB Dataset of 50K Movie Reviews for binary sentiment classification.

The system allows users to submit a movie review, which is then processed through a preprocessing pipeline and classified using machine learning models. The goal is to achieve high accuracy in sentiment detection, aiding users in understanding review polarity.

## Team Members
- IT24100209: Data Cleaning (Text Cleaning)
- IT24100095: Stop Words Removal
- IT24100163: Stemming
- IT24100068: N-grams Extraction
- IT24100109: lowercasing
- IT24100156: Encoding Categorical Variables

Group Work: Handling Missing Data (shared by all members).

## Dataset
- **Source**: [IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)
- **Description**: 50,000 movie reviews labeled as positive or negative (25,000 each). Columns: `review` (text) and `sentiment` (categorical: positive/negative).
- **Usage**: The dataset is used for training and testing the sentiment classification model. It is loaded as `IMDB Dataset.csv`.
- **Additional Info**: From http://ai.stanford.edu/~amaas/data/sentiment/. No missing values typically, but handled for completeness.

## Preprocessing Pipeline
The preprocessing pipeline is a collaborative effort, integrating individual contributions into a logical flow. It processes the raw text reviews to prepare them for modeling. The pipeline demonstrates proper integration, logical flow, and collaboration, with clearly commented and organized code.


- **Handling Missing Data (Group Work):- Check for nulls and drop rows if any. Justification: Ensures dataset completeness for accurate sentiment analysis. EDA: Bar plot of missing values per column (typically zero in IMDB dataset).

- **Data Cleaning (IT24100209):- Remove HTML tags, punctuation, and convert to lowercase. Justification: Reviews contain noise like `<br>` tags. EDA: Histograms of word counts before/after + difference plot.

- **Stop Words Removal (IT24100095):- Eliminate common words (e.g., 'the', 'is'). Justification: Reduces noise in text data. EDA: Sample text comparison before/after + word count difference histogram.

- **Stemming (IT24100163):- Reduce words to roots (e.g., 'running' → 'run'). Justification: Groups similar words for better sentiment detection. EDA: Sample text comparison before/after + word count difference histogram.

- **N-grams Extraction (IT24100068):- Extract unigrams and bigrams. Justification: Captures context like 'not good'. EDA: Bar plots of top unigrams before and top bigrams after.

- **Lowercasing (IT24100109):- Converts all text to lowercase. Justification: Ensures uniformity, reduces vocabulary size. EDA: Uppercase presence before/after + sample comparison.

- **Encoding Categorical Variables (IT24100156):- Label encode 'sentiment' (positive/negative → 1/0). Justification: Models require numeric labels. EDA: Count plots of sentiment distribution before/after encoding.

### Group Requirement 
- A combined preprocessing pipeline script (`group_pipeline.py` or `.ipynb`) integrates all individual work.
- Demonstrates logical flow: Missing Handling → Data Cleaning → Stop Words Removal → Stemming → N-grams Extraction → Spell Checking → Encoding.
- Output: A cleaned, preprocessed CSV ready for modeling.

## Installation and Setup
### Requirements
- Python 3.8+
- Libraries: pandas, scikit-learn, nltk, textblob, matplotlib, seaborn
- Install via: `pip install pandas scikit-learn nltk textblob matplotlib seaborn`

### Dataset Setup
1. Download the IMDB Dataset from the link above.
2. Place `IMDB Dataset.csv` in the project root.

### Running the Pipeline
1. Run `Missing_Data_Handling.ipynb` to handle missing values.
2. Run each member's notebook sequentially for preprocessing.
3. Run `group_pipeline.py` or `.ipynb` for the integrated pipeline.
4. Output files are saved in `processed_data/` folder.


