# Sentiment Analysis of Reviews Using TextBlob

## Overview

This project implements sentiment analysis on customer reviews using the TextBlob library in Python. The primary goal is to analyze textual data from a dataset of reviews and classify their sentiments into categories such as "Very Negative," "Negative," "Neutral," and "Positive." The project also includes visualizations to represent the sentiment distribution through heatmaps.

## Features

- **Sentiment Analysis**: Computes sentiment polarity scores for each review using TextBlob.
- **Data Preprocessing**: Cleans and prepares text data by removing stopwords and unnecessary tokens.
- **Visualization**: Generates heatmaps to visually represent the distribution of sentiment scores across different categories.
- **CSV Input/Output**: Reads from a CSV file containing cleaned reviews and outputs the results back to a new CSV file.

## Requirements

To run this project, you need the following Python libraries:

- `pandas`
- `textblob`
- `seaborn`
- `matplotlib`

You can install these libraries using pip:

```bash
pip install pandas textblob seaborn matplotlib
