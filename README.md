
# NLP Vector Space Foundations – Lab Workshop

## Overview
This lab walks through the development of a foundational NLP pipeline from scratch. It introduces core vector space concepts and demonstrates how to implement a document search system using custom preprocessing and vectorization.

---

## Team Members
- **Fasalu Rahman Kottaparambu** – 8991782  
- **Srinu Babu Rai** – 8994032  
- **Christo Pananjickal Baby** – 8989796

---

## Objective
To build a fully functional NLP pipeline capable of:
- Text preprocessing (tokenization, stopword removal, stemming)
- Creating various vector representations (binary, TF, TF-IDF)
- Constructing a positional index
- Handling phrase queries
- Computing document similarity via cosine distance


##  Core Steps in the Pipeline

### 1. **Custom Text Preprocessing**
- Lowercasing
- Regex-based tokenization
- Stopword removal
- Suffix-based stemming (manual)

### 2. **Document Loading**
- Reads all `.txt` files from a specified folder

### 3. **Vector Representations**
- **Binary Term-Document Matrix**: Tracks presence/absence of words
- **Term Frequency Matrix (TF)**: Raw word counts
- **TF-IDF Matrix**: Highlights important words across documents

### 4. **Positional Indexing**
- Records exact word positions within each document
- Enables precise phrase searches

### 5. **Cosine Similarity**
- Measures semantic similarity between documents using TF-IDF vectors

---

## 🔎 Sample Outputs (from test queries)
```python
# Sample Results:
print("\nTerm-Document (learn):\n", incidence_df.get("learn", "Not Found"))
print("\nTerm-Frequency (deep):\n", tf_df.get("deep", "Not Found"))
print("\nTF-IDF (machin):\n", tfidf_df.get("machin", "Not Found"))
print("\nPositional Index (model):\n", positional_index.get("model", "Not Found"))
print("\nPhrase Query ('deep learn'):\n", phrase_query("deep learn", preprocessed_docs, filenames))
print("\nCosine Similarity (first document):\n", cosine_sim_df.iloc[0])
```

---

## Talking Points
1. Built-in Positional Index for Phrase Matching : A custom positional index maps each word to its positions across documents, allowing for precise phrase queries and simulating real search engine logic.
2. Semantic Search with Cosine Similarity: Cosine similarity is used on TF-IDF vectors to rank document similarity, demonstrating how modern NLP systems perform semantic comparison and relevance scoring.
3. Vectors can be used to identify the relations between vetcor points in vector space. 


## Final Thoughts
This lab provides a complete, minimal yet powerful introduction to building a vector space model. It's an ideal foundation for expanding into search engines, chatbots, or recommendation systems.

> "Understanding how machines process language begins by teaching them how to read—and this lab is their first lesson."
