# 📝 Sentiment Analysis of Reviews Using TextBlob

## 📖 Overview

This project implements **sentiment analysis** on customer reviews using the **TextBlob** library in Python.  
The goal is to analyze textual data from a dataset of reviews and classify their sentiments into categories like:

✅ Very Negative  
✅ Negative  
✅ Neutral  
✅ Positive  

It also includes visualizations to represent the sentiment distribution using **heatmaps**.

---

## ✨ Features

- **🔍 Sentiment Analysis**: Computes sentiment polarity scores for each review using TextBlob.
- **🧹 Data Preprocessing**: Cleans and prepares text data by removing stopwords and unnecessary tokens.
- **📊 Visualization**: Generates heatmaps to visually display the distribution of sentiment scores across categories.
- **📁 CSV Input/Output**: Reads from a CSV file containing cleaned reviews and writes the sentiment results to a new CSV file.

---

## ⚙️ Requirements

You’ll need the following Python libraries:

- `pandas`  
- `textblob`  
- `seaborn`  
- `matplotlib`

Install them using:

```bash
pip install pandas textblob seaborn matplotlib
```

---

## 📂 Dataset

Prepare a CSV file named (for example):

```
cleaned_reviews.csv
```

with at least one column:

| Review |
|--------|
| The product was excellent and arrived early! |
| Terrible customer service, very disappointed. |

---

## 🚀 Usage

1️⃣ Run the main script:

```bash
python sentiment_analysis.py
```

2️⃣ The script will:

- Read the reviews from the CSV file.
- Calculate sentiment polarity scores.
- Classify each review into a sentiment category.
- Generate visualizations (like heatmaps).
- Write the results to a new CSV file (e.g., `sentiment_results.csv`).

---

## 📊 Sentiment Categories

The polarity scores from TextBlob are mapped as:

| Polarity Score Range   | Category         |
|------------------------|------------------|
| -1.0 to -0.6          | Very Negative    |
| -0.6 to -0.2          | Negative         |
| -0.2 to 0.2          | Neutral          |
| 0.2 to 1.0           | Positive         |

---

## 🛠 Example Code Snippet

```python
from textblob import TextBlob

def get_sentiment_category(polarity):
    if polarity <= -0.6:
        return "Very Negative"
    elif polarity <= -0.2:
        return "Negative"
    elif polarity <= 0.2:
        return "Neutral"
    else:
        return "Positive"

blob = TextBlob("The product was excellent and arrived early!")
polarity = blob.sentiment.polarity
category = get_sentiment_category(polarity)

print(f"Polarity: {polarity}, Category: {category}")
```

---

## 📈 Visualizations

The script uses `seaborn` and `matplotlib` to create heatmaps showing the sentiment distribution across your dataset.

---

## 📜 License

This project is open-source under the MIT License.

---

## 🙏 Acknowledgments

Special thanks to:

- **TextBlob**: For its straightforward and effective sentiment analysis tools.
- **Seaborn** and **Matplotlib**: For making data visualization easy and beautiful.
- **Pandas**: For simplifying data handling.

---

💡 **Feel free to fork this project and customize it for your own review datasets!**
