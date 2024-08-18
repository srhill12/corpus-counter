
# Reuters Text Analysis

This project is focused on analyzing a collection of Reuters articles categorized under "grain." The analysis involves preprocessing the text data to generate insights on the most common words and bigrams (pairs of adjacent words) in the corpus. The project makes use of the Natural Language Toolkit (NLTK) and pandas for text processing and data manipulation.

## Project Structure

- **Main Script**: The main script imports the necessary libraries, processes the text data, and generates insights.
- **Functions**:
  - `process_text(article)`: Preprocesses a given text article by removing stopwords, non-alphabetic characters, tokenizing the text, lemmatizing words, and filtering out stopwords.
  - `word_counter(corpus)`: Counts and returns the top ten most common words in a given corpus of text.
  - `bigram_counter(corpus)`: Counts and returns the top ten most common bigrams in a given corpus of text.

## Requirements

- **Python 3.x**
- **NLTK**: The Natural Language Toolkit is required for text processing. Install it using pip:
  ```bash
  pip install nltk
  ```
- **pandas**: For data manipulation and analysis. Install it using pip:
  ```bash
  pip install pandas
  ```

## Setup

Before running the script, ensure that you have the required NLTK data packages. The script will download them if they are not already installed:

```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
```

## Usage

1. **Preprocess Text**: The `process_text` function cleans and processes the text from the Reuters articles, including tokenizing and lemmatizing the words.

2. **Word Frequency Analysis**:
   - Use the `word_counter` function to identify the most common words in the corpus.
   - The function returns a pandas DataFrame with the top ten words and their respective counts.

3. **Bigram Frequency Analysis**:
   - Use the `bigram_counter` function to identify the most common bigrams in the corpus.
   - The function returns a pandas DataFrame with the top ten bigrams and their respective counts.

## Example

```python
# Instantiate the lemmatizer
lemma = WordNetLemmatizer()

# List the articles about grains
ids = reuters.fileids(categories='grain')
corpus = [reuters.raw(i) for i in ids]

# Analyze the corpus
word_counts = word_counter(corpus)
print(word_counts)

bigram_counts = bigram_counter(corpus)
print(bigram_counts)
```

## Output

- **Word Frequency**:
  - The `word_counter` function outputs a DataFrame with the most common words, such as "said," "tonne," and "mln," along with their respective counts.
  
- **Bigram Frequency**:
  - The `bigram_counter` function outputs a DataFrame with the most common bigrams, such as ("mln", "tonne"), ("us", "agriculture"), and ("soviet", "union"), along with their respective counts.

## Conclusion

This project provides a simple yet powerful way to preprocess and analyze textual data using NLTK. The functions included allow for quick insights into word and bigram frequencies within a corpus, making it useful for natural language processing (NLP) tasks and text analysis.
```
