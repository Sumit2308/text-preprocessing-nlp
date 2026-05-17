# Text Preprocessing Pipeline — NLP Assignment 2

A complete NLP pipeline that collects, cleans, and converts 
Wikipedia-style text into ML-ready format using TF-IDF vectorization.

## Problem
Build an end-to-end text preprocessing pipeline across 4 categories:
- Artificial Intelligence
- Space Exploration  
- Human Biology
- Famous Scientists

## Dataset
- 60 articles total — 15 per category
- Collected from Wikipedia content
- Saved as `raw_dataset.csv`

## Pipeline Steps

| Step | Task | Tool |
|---|---|---|
| 1 | Remove HTML tags | BeautifulSoup |
| 2 | Remove citations [1],[23] | Regex |
| 3 | Remove punctuation | Regex |
| 4 | Lowercase conversion | Python str |
| 5 | Remove extra spaces | Regex |
| 6 | Tokenization | NLTK word_tokenize |
| 7 | Stopword removal | NLTK stopwords |
| 8 | Lemmatization | WordNetLemmatizer |
| 9 | TF-IDF Vectorization | sklearn TfidfVectorizer |

## Key Results
- **60 articles** processed across 4 categories
- Lemmatization chosen over Stemming — produces real dictionary words
- TF-IDF clearly separated categories with domain-specific keywords
- Top words per category made intuitive sense:
  - AI → model, learning, network
  - Space → satellite, orbit, apollo
  - Biology → cell, dna, genome
  - Scientists → quantum, physic, turing

## Files
| File | Description |
|---|---|
| `raw_dataset.csv` | Original scraped text + labels |
| `cleaned_dataset.csv` | After HTML, citation, punctuation removal |
| `final_dataset.csv` | After tokenization, stopword removal, lemmatization |
| `notebook.ipynb` | Full pipeline with explanations |

## Tech Stack
`Python` `NLTK` `BeautifulSoup` `scikit-learn` `pandas` `matplotlib`
