# NLP-Bag-of-Words-&-TF-IDF


## Overview

This project demonstrates how to preprocess text data using two common Natural Language Processing (NLP) techniques: Bag of Words (BoW) and Term Frequency-Inverse Document Frequency (TF-IDF). Both methods are used to convert text documents into numerical feature vectors that can be used for machine learning models and text analysis.

## Key Concepts

### Bag of Words (BoW)

The Bag of Words model is a simple and widely used method for text representation. It transforms text into a fixed-length vector of word counts, ignoring the order and grammar of words. Here’s a brief overview:

- **Vocabulary Creation**: Build a vocabulary of all unique words in the entire corpus.
- **Vector Representation**: For each document, create a vector where each position represents a word from the vocabulary. The value at each position is the count of the word in the document.

**Advantages**:
- Simple and easy to implement.
- Effective for basic text classification tasks.

**Disadvantages**:
- Ignores word order and context.
- Can lead to large feature vectors with high dimensionality.

### Term Frequency-Inverse Document Frequency (TF-IDF)

TF-IDF is an advanced text representation technique that combines term frequency (TF) and inverse document frequency (IDF) to capture the importance of words in a document relative to a corpus. Here’s how it works:

- **Term Frequency (TF)**: Measures how frequently a term appears in a document. It is calculated as:
  \[
  \text{TF}(t, d) = \frac{\text{Number of times term } t \text{ appears in document } d}{\text{Total number of terms in document } d}
  \]

- **Inverse Document Frequency (IDF)**: Measures how important a term is across all documents. It is calculated as:
  \[
  \text{IDF}(t, D) = \log \left( \frac{\text{Total number of documents } N}{\text{Number of documents containing term } t} \right)
  \]

- **TF-IDF**: Combines TF and IDF to provide a score for each term in each document:
  \[
  \text{TF-IDF}(t, d, D) = \text{TF}(t, d) \times \text{IDF}(t, D)
  \]

**Advantages**:
- Considers both term frequency and the rarity of terms.
- Provides a better representation of important words in documents.

**Disadvantages**:
- More complex than BoW.
- Still ignores word order and context.

## Project Structure

- **`notebooks/`**: Jupyter notebooks demonstrating the usage of BoW and TF-IDF with examples.
- **`README.md`**: This file.

## Requirements

- Python 3.x
- `nltk`
- `scikit-learn`
- `pandas`
