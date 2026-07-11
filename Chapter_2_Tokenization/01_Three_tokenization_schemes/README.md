# Project 1 — Three tokenization schemes

**Chapter 2 · Tokenization** · pp. 20–27

## Goal
Compare three ways to turn text into integers — **character-based**, **word-based**, and GPT-2's statistical **BPE** tokenizer — on a sample sentence, and see how they trade off vocabulary size, information density, and reversibility.

## Key techniques
- Build character/word vocabs with list comprehensions, `set`, `sorted`, and dict look-up tables (manual encode/decode)
- Load GPT-2's tokenizer via Hugging Face `AutoTokenizer.from_pretrained('gpt2')` — `.encode()`, `.decode()`, `.vocab_size`
- Visualize token sequences and compare total vs. unique token counts across the three schemes
