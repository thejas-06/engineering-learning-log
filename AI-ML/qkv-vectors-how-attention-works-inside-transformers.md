# Q, K, V Vectors: How Attention Works Inside Transformers

This note explains the three types of vectors — Query, Key, and Value —
and how they power the attention mechanism in transformer-based models.

---

## Quick recap: what is a vector?
A vector is simply a list of numbers that represents meaning.

Example:
- “cat” → a point in space
- Close to: dog, lion
- Far from: car, rocket

Transformers operate entirely on vectors.

---

## Important insight
Not all vectors in a transformer serve the same purpose.

Inside attention, **each token is converted into three different vectors**:
- Query (Q)
- Key (K)
- Value (V)

Together, this is called **QKV**.

---

## Intuition: the library analogy

### Query (Q) — the question
Query represents **what the current word is looking for**.

Analogy:
- You asking: “Which books are about cats?”

Q asks:
- “What information do I need from other tokens?”

---

### Key (K) — the label
Key represents **what each word offers**.

Analogy:
- Subject tags on books: cats, dogs, history

Keys answer:
- “What is this token about?”

---

### Value (V) — the content
Value contains the **actual information** carried by the token.

Analogy:
- The contents inside the book you finally read

Values answer:
- “What information should I take if this token is relevant?”

---

## How attention works step by step

1. Every token becomes Q, K, and V vectors  
2. Each Query is compared with all Keys  
3. Similarity scores are computed (relevance)  
4. Scores are normalized into attention weights  
5. Weights are applied to Values  
6. A weighted combination of Values becomes the output  

This lets each token pull **only the information it needs**.

---

## Why QKV enables context understanding
Example sentence:

“The cat sat on the mat because it was warm.”

Using QKV:
- “it” generates a Query
- Keys help match “it” to “mat”
- Values transfer the correct meaning

Without QKV, the model would guess randomly.

---

## One-line takeaway
Q, K, and V vectors are how transformers decide *who to listen to*
and *what information to extract*, making true contextual understanding possible.
