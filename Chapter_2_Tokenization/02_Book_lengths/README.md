# Project 2 — Book lengths in characters, words, and tokens

**Chapter 2 · Tokenization** · pp. 28–30

## Goal
Import 10 out-of-copyright books from Project Gutenberg and compare their lengths measured three ways — **characters**, **words**, and **GPT-2 tokens** — for both total and unique counts, then examine how those measures relate across books.

## Key techniques
- Download book text over HTTP with the `requests` library (`requests.get(url).text`)
- Count characters (`len`), words (`.split()`), and GPT-2 tokens (`tokenizer.encode`)
- Print a formatted comparison table across books
- Scatter-plot total vs. unique counts and quantify the relationship with `np.corrcoef`
- Spot and investigate an outlier book
