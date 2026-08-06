# Project 4 — Token lengths in characters and bytes

**Chapter 2 · Tokenization** · pp. 35–39

## Goal
Compare how long every GPT-2 token is when measured in **characters** versus **UTF-8 bytes**, across the whole 50,257-token vocabulary. Most tokens are plain ASCII (1 byte per character, so the two measures match), but tokens containing accented letters, non-Latin scripts, or emoji take multiple bytes per character — and those mismatches are what this project hunts down and visualizes.

## Key techniques
- Encode a string to UTF-8 and count its bytes with `len(s.encode("utf-8"))`
- Loop the full vocabulary via `tokenizer.decode([i])` and `tokenizer.vocab_size`
- Build a 2-D character-vs-byte frequency matrix and colour points by log frequency
- Find mismatched tokens with a boolean mask (`chars != bytes`) and `np.where`
- Compare length distributions with `np.unique(..., return_counts=True)`
