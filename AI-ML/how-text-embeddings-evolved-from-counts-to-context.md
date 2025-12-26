# How Text Embeddings Evolved: From Counts to Context

---

## What an embedding actually is
An embedding converts a word (or text) into a vector — a list of numbers
that captures meaning.

Key intuition:
- Similar meanings → vectors closer together
- Dissimilar meanings → vectors far apart

Example:
- "apple" and "banana" → close
- "apple" and "chicken" → far

This idea is called **semantic similarity**.

---

## TF-IDF (Before semantic understanding)
TF-IDF represents text using word frequency statistics.

What it does:
- Counts how important a word is in a document

What it does NOT do:
- Understand meaning

Result:
- "apple" and "banana" are unrelated
- No notion of similarity between words

This was purely statistical, not semantic.

---

## Word2Vec (2013): First meaningful vectors
Word2Vec introduced the idea that:
- Words appearing in similar contexts should have similar vectors

What it learned:
- Semantic relationships
- Analogies like King → Queen

Big limitation:
- One word = one vector
- No context awareness

So:
- "bank" (river bank)
- "bank" (bank robbery)

→ identical embeddings, despite different meanings.

---

## The core problem
Earlier embeddings could not handle **context**.
Meaning changed based on surrounding words, but vectors did not.

---

## Transformers: Context-aware embeddings
Transformers changed how text is processed.

Key shift:
- Tokens are processed together, not one by one
- Meaning depends on the full sentence or document

Result:
- Contextual embeddings
- "bank" now changes meaning based on usage

This made sentence-level and document-level understanding possible and
set the foundation for modern LLMs.

---

This progression explains why embeddings today feel "intelligent" —
they evolved from counting words to understanding context.
