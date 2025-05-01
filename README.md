# Sentiment Analysis of Travel Reviews

This project involves scraping customer reviews from Trustpilot and TripAdvisor, preprocessing the textual data, and performing sentiment analysis using Python's Natural Language Toolkit (NLTK) and the VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analyzer.

## 📌 Project Overview

- **Data Source**: Customer reviews from Trustpilot and TripAdvisor.
- **Objective**: Determine the sentiment (positive, negative, neutral) expressed in travel-related customer reviews.
- **Tools & Libraries**:
  - Python
  - BeautifulSoup (for web scraping)
  - NLTK (Natural Language Toolkit)
  - VADER Sentiment Analyzer
  - Pandas 
## 🛠️ Technologies Used

- **Web Scraping**:
  - `requests`
  - `BeautifulSoup`
- **Text Preprocessing**:
  - Lowercasing
  - Whitespace removal
  - Punctuation removal
  - Special character removal
  - Tokenization
  - Lemmatization
- **Sentiment Analysis**:
  - NLTK's VADER SentimentIntensity Analyzer

## 📂 Project Structure

```

sentiment-analysis/
├── data/
│   ├── trustpilot_reviews.csv
│   └── tripadvisor_reviews.csv
├── notebooks/
│   └── sentiment_analysis.ipynb
├── scripts/
│   ├── scrape_trustpilot.py
│   └── scrape_tripadvisor.py
├── README.md
└── requirements.txt
```


## 🔍 Methodology

1. **Data Collection**:
   - Utilized `requests` and `BeautifulSoup` to scrape customer reviews from Trustpilot and TripAdvisor.
   - Stored the scraped data in CSV format for further processing.
  
---

2. **Data Preprocessing**:
   - Converted all text to lowercase to maintain consistency.
   - Removed extra whitespaces, punctuation, and special characters to clean the text.
   - Tokenized the text into individual words using NLTK's `word_tokenize`.
   - Applied lemmatization using NLTK's `WordNetLemmatizer` to reduce words to their base forms.


---

3. **Sentiment Analysis**:  
   - Used NLTK's `SentimentIntensityAnalyzer` from the VADER lexicon to analyze the sentiment of lemmatized reviews.  
   - Converted each lemmatized list of tokens into a string using a lambda function to ensure compatibility with the analyzer.  
   - Applied the `polarity_scores()` method to extract sentiment scores (`positive`, `negative`, `neutral`) for each review.  
   - Stored the individual sentiment components in new columns for further analysis.  
   - Aggregated sentiment scores across all reviews to determine the overall sentiment of the dataset.  
   - Used a custom function to compare total scores and identify the dominant sentiment, which was **neutral** in this case.

---



## 📊 Results

After analyzing the reviews, the sentiment distribution was Neutral 


## 📚 References

- [NLTK Documentation](https://www.nltk.org/)
- [VADER Sentiment Analysis](https://github.com/cjhutto/vaderSentiment)
- [BeautifulSoup Documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) ([touti-ayoub/Reviews-Sentiment-Analysis-NLTK-VADER - GitHub](https://github.com/touti-ayoub/Reviews-Sentiment-Analysis-NLTK-VADER?utm_source=chatgpt.com), [Sentiment Analysis using NLTK - Sid-Lais Sid-Lais - GitHub](https://github.com/Sid-Lais/Sentiment-Analysis?utm_source=chatgpt.com))

## 📄 License

This project is licensed under the [MIT License](LICENSE).
