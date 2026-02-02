
# AIG 230 – Lab 03

# Text Representation and Statistical Language Models

## Overview
This project explores foundational techniques in Natural Language Processing (NLP) through practical implementations of text representation and statistical language modeling.


## Repository Contents

### 1. `text_representation.ipynb`
This notebook focuses on representing text in vector space and performing similarity-based retrieval.

**Key components:**
- Text preprocessing and tokenization
- TF-IDF vectorization
- Cosine similarity for document retrieval
- Query-based information retrieval
- Model evaluation 

The notebook demonstrates how textual data can be transformed into numerical form and used to retrieve the most relevant documents for a given query.


### 2. `statistical_language_models.ipynb`
This notebook focuses on probabilistic language modeling using n-grams.

**Key components:**
- Unigram, bigram, and trigram language models
- Vocabulary construction with Out-Of-Vocabulary (OOV) handling using `<UNK>`
- Add-k (Laplace) smoothing
- Cross-entropy and perplexity evaluation on a test set
- Backoff strategy:
  - Trigram → Bigram → Unigram
- Simple text generation
- Top-k next-word prediction (e.g., predicting next words for phrases like `"user cannot"`)

The notebook demonstrates how statistical language models estimate word probabilities and how smoothing and backoff improve robustness on sparse data.


## Key NLP Concepts Implemented
- Text preprocessing and tokenization
- TF-IDF representation
- Cosine similarity
- N-gram language models
- Add-k smoothing
- OOV handling
- Cross-entropy
- Perplexity
- Backoff strategies
- Next-word prediction (top-k)


## How to Run
1. Open the notebooks in **Jupyter Notebook** or **VS Code**.
2. Ensure Python is installed.
3. Run the cells sequentially from top to bottom.
4. No external datasets are required — all data is defined within the notebooks.



## Notes on Results
- Due to the relatively small corpus size, some next-word predictions may return fewer than `k` valid candidates when certain tokens (e.g., start tokens) are excluded.
- Higher-order n-gram models (e.g., trigrams) can outperform lower-order models but are more sensitive to data sparsity.
- Changes to the OOV threshold (`min_count`) directly affect perplexity by balancing vocabulary size and unknown word frequency.

