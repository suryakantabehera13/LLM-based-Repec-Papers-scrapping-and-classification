#### RePEc Papers Classifier: 

This notebook extracts research papers from the RePEc Ideas website, processes the metadata, and classifies whether a paper is relevant to economics using hybrid approaches (keyword filtering, embeddings, and transformers).

### Setup Instructions
1. Open the Notebook in Google Colab
Upload or open Repec_Papers_data.ipynb in Google Colab.

2. Install Dependencies

# Run the following cell to install required libraries:

!pip install -q requests beautifulsoup4 pandas tqdm sentence-transformers transformers

3. Environment Requirements

- Python 3.8+

- Google Colab with internet access (for downloading models and accessing RePEc site)

- Compatible with CPU runtime, GPU not required.

### How to Run the Script
1. Start from the top and run all cells sequentially.

2. The script performs the following:

- Scrapes papers from the RePEc Ideas site.

- Extracts metadata (title, abstract, authors, links).

- Applies:

       -- Keyword-based filtering

       -- Embedding-based similarity (Sentence-BERT)

       -- Zero-shot classification (HuggingFace Transformers)

### Output
- Extracted paper metadata containing columns like title, author, abstract, keywords, links, download links, page number etc.

- Filtered list of economics-relevant papers printed in the output cells.

- Scores and reasoning (based on model) shown for each classification method.

### Tips
- Can change the keyword list or model for better accuracy.

- Use of HuggingFace token (optional) for faster model downloads.
