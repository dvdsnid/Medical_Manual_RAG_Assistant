# Medical Manual RAG Assistant

A Retrieval-Augmented Generation (RAG) project that explores answering medical questions using the Merck Manual as a reference source.

## Project overview

This notebook compares:
- Responses from a base Mistral 7B language model
- Prompt-engineered responses
- RAG responses grounded in retrieved passages from a medical reference
- Different chunking and retrieval configurations
- LLM-as-a-judge evaluation of response quality

The workflow uses LangChain, Chroma, FastEmbed embeddings, PyMuPDF, Hugging Face Hub, and `llama-cpp-python`.

## Important limitations

**This is an educational AI/ML project, not a medical device or clinical decision-support system.**
Generated answers may be incomplete or incorrect. Do not use them to diagnose, treat, or make healthcare decisions. Always consult qualified healthcare professionals and authoritative clinical guidance.

## Requirements

- Python environment compatible with the pinned notebook dependencies
- Several gigabytes of free disk space for the model and vector database
- A GPU is recommended; a compatible CPU setup may also work but can be much slower
- Google Colab with a GPU runtime is the notebook's recommended starting point

## How to run

1. Open `notebooks/Medical_Manual_RAG_Assistant.ipynb` in Google Colab or Jupyter.
2. For Google Colab, select **Runtime → Change runtime type → T4 GPU** if available.
3. Follow the notebook's installation cells and restart the runtime when instructed.
4. Obtain lawful access to the required medical-manual PDF separately. The PDF is not included in this repository.
5. Update the `pdf_path` variable in the notebook's **Loading the Data** section to point to your PDF.
6. Run the notebook cells in order.

Model downloads and vector-database construction can take time and use substantial disk space.

## Repository structure

```text
Medical_Manual_RAG_Assistant/
├── README.md
├── requirements.txt
├── .gitignore
└── notebooks/
    └── Medical_Manual_RAG_Assistant.ipynb
```

## Data and copyright

The notebook references the Merck Manual. The source PDF is intentionally not included. Obtain the document from an authorized source and comply with its applicable terms and copyright restrictions.

## Suggested portfolio summary

Built an educational medical-reference RAG pipeline using Mistral 7B, LangChain, Chroma, and embedding-based retrieval. Compared base-LLM, prompt-engineered, and retrieval-grounded answers, explored chunking/retriever configurations, and evaluated answer relevance and groundedness.
