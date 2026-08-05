# Project 3 — Pandas frequency tables of token lengths

**Chapter 2 · Tokenization** · pp. 31–34

## Goal
Measure how long GPT-2 tokens are, in characters, and study the distribution of those lengths — first for a single paragraph, then across the 10 Project Gutenberg books — using pandas frequency tables (`value_counts`) and seaborn plots.

## Key techniques
- Decode individual tokens back to text with `tokenizer.decode` and measure length with `len`
- Build a `pandas.DataFrame` and count category frequencies with `Series.value_counts` (raw and `normalize=True`)
- Bar plot of a frequency table with `seaborn.barplot`
- Overlay normalized distributions across books with `seaborn.scatterplot` on a log x-axis
