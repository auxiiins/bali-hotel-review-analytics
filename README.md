# Bali Hotel Review Analytics

An end-to-end Natural Language Processing (NLP) project that transforms over 3,000 TripAdvisor hotel reviews from Bali into structured business insights using transformer models and linguistic analysis techniques.

---

## Project Overview

Online hotel reviews contain valuable customer feedback, but they are unstructured and difficult to analyze at scale.  
This project builds an NLP pipeline to extract:

- **Sentiment (emotion classification)**
- **Aspect-level insights (e.g., staff, cleanliness, room, location)**
- **Concise summaries of long reviews**

The goal is to convert raw text into actionable insights for hotel management and business decision-making.

---

## Pipeline Architecture
    Raw Reviews
        ↓
    Text Preprocessing
        ↓
    Sentiment Analysis (DeBERTaV3)
        ↓
    Aspect Extraction (POS Tagging)
        ↓   
    Summarization (BART)
        ↓
    Structured Insights


---

## Methods & Models

### Sentiment Analysis — DeBERTaV3
A transformer-based model used to classify the emotional tone of each review.

- Model: DeBERTaV3
- Task: Text classification
- Output: Positive / Negative / Mixed sentiment

Why DeBERTaV3?
- Strong contextual understanding
- Improved attention mechanisms compared to BERT

---

### Aspect Extraction — POS Tagging
Parts-of-Speech tagging is used to identify important features mentioned in reviews such as:

- Staff
- Room
- Cleanliness
- Location
- Facilities

Each aspect is linked to sentiment for granular analysis.

---

### Review Summarization - BART
BART (Bidirectional and Auto-Regressive Transformers) is used to generate concise summaries of long reviews.

- Model: BART
- Task: Abstractive summarization
- Output: Human-readable review summaries

---

## 📊 Example Output

### Input Review:
> "The staff were incredibly friendly, but the room was not very clean and had a bad smell."

### Output:

**Sentiment:**
- Mixed

**Aspect-Level Sentiment:**
- staff → Positive  
- room → Negative  
- cleanliness → Negative  

**Summary:**
> Friendly staff, but the room cleanliness was poor.

---

## Tech Stack
- Python
- Hugging Face Transformers
- PyTorch
- DeBERTaV3
- BART
- NLTK / SpaCy (POS tagging)
- Pandas, NumPy

---

## 📁 Project Structure
    ├── Bali_Hotel_Review_Analytics.ipynb # Main notebook
    ├── data/ # Sample dataset 
    ├── outputs/ # Generated predictions & summaries
    ├── requirements.txt # Dependencies
    └── README.md



---

## 🚀 How to Run

1. Clone the repository
```bash
git clone https://github.com/your-username/bali-hotel-review-analytics.git
cd bali-hotel-review-analytics
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Open notebook
```bash
jupyter notebook
```
