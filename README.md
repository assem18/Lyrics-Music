# Lyrics Music: Hybrid Music Retrieval System

## Overview

Lyrics2Music is an intelligent music retrieval system that identifies songs from partial lyrics entered as text or spoken through a microphone.

The system combines traditional Information Retrieval techniques with modern Transformer-based semantic search to achieve both high efficiency and high accuracy.

Instead of searching the entire collection using a deep neural model, the system first retrieves candidate songs using BM25 and then performs semantic re-ranking using Sentence-BERT.

---

## Features

* Text-based lyrics search
* Voice-based lyrics search using Whisper
* BM25 candidate retrieval
* Sentence-BERT semantic re-ranking
* Hybrid retrieval architecture
* SerpAPI integration for external song links
* Interactive user interface using ipywidgets
* Fast and scalable search pipeline

---

## System Architecture

User Input (Text or Audio)

↓

Whisper Speech Recognition

↓

BM25 Candidate Retrieval

↓

Top-N Candidate Songs

↓

Sentence-BERT Semantic Re-ranking

↓

Best Matching Song

↓

SerpAPI Song Links

---

## Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Rank-BM25
* Sentence-Transformers
* Sentence-BERT
* Faster-Whisper
* SerpAPI
* Jupyter Notebook
* Google Colab
* ipywidgets

---

## Dataset

The project uses a lyrics collection containing songs from:

* Drake
* Billie Eilish
* Maroon 5

Each song contains:

* Artist
* Song Title
* Album
* Lyrics
* Metadata

---

## Retrieval Pipeline

### Stage 1: Candidate Retrieval

The user query is processed and submitted to a BM25 retrieval model.

BM25 efficiently retrieves the most relevant candidate songs from the collection.

### Stage 2: Semantic Re-ranking

The original query and candidate songs are encoded using Sentence-BERT embeddings.

Cosine Similarity is used to measure semantic similarity and re-rank the candidates.

### Stage 3: External Song Information

The highest-ranked song is passed to SerpAPI to retrieve external music links and additional information.

---

## Example Query

Input:

don't be cautious don't be kind you committed I'm your crime

Output:

Artist: Billie Eilish

Song: COPYCAT

Similarity Score: 0.95+

---

## Installation

```bash
pip install rank_bm25
pip install sentence-transformers
pip install faster-whisper
pip install google-search-results
pip install ipywidgets
```

## Run

Open the notebook and execute all cells.

Choose:

* Text Input
* Audio Input

Then click Search.

---

## Future Improvements

* Spotify API integration
* Album cover retrieval
* Music preview playback
* Larger music datasets
* Multilingual lyrics retrieval
* Fine-tuned retrieval models

---

## Author

Assem Aldurini

Computer Science Student

Zewail City of Science and Technology
