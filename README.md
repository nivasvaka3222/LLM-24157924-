# Seychelles IMF Financial Stability Analysis

A Jupyter Notebook project analysing **Seychelles** using **IMF Country Report No. 23/402 (December 2023)**, a Staff Report covering the EFF/RSF programme reviews.

## What the project does

- Extracts and cleans text from an 80-page IMF report; creates 130 overlapping text chunks.
- Builds semantic embeddings with **all-MiniLM-L6-v2** and searches them using **FAISS**.
- Uses **GPT-4o-mini** and **GPT-4o** via **OpenRouter** for summaries, financial-indicator extraction, grounded Q&A and evaluation.
- Produces four charts covering risk themes, GDP trends, indicator comparisons and review outcomes.

## Run locally

1. Place `Seychelles_Financial_Stability.ipynb` and `Seychelles_IMF_Country_Report_2023.pdf` in the same project folder.
2. Install the Python dependencies listed in the notebook.
3. Create a `.env` file in the project folder:
   ```env
   OPENROUTER_API_KEY=your_key_here
   ```
4. Open the notebook in Jupyter and run its cells in order. Results are written to the notebook's output folders.

**Never commit `.env` or API credentials to GitHub.** API requests may incur OpenRouter charges. CPU execution is supported.

## Notes

LLM-generated values and evaluations can be incomplete or incorrect, particularly for PDF tables. Verify economic figures against the original IMF report; `-1.0` indicates an unavailable extracted value, not an economic measurement.

**Source:** [IMF Country Report No. 23/402](https://www.elibrary.imf.org/view/journals/002/2023/402/002.2023.issue-402-en.xml).
