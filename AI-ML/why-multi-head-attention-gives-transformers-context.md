# Why Multi-Head Attention Gives Transformers Context

This note explains what multi-head attention is and why it is essential
for how transformer-based models understand complex input.

---

## The limitation before multi-head attention
A single attention mechanism can focus on only one type of relationship
at a time.

What this causes:
- The model sees limited context
- Important signals compete with each other
- Understanding becomes shallow

Mental analogy:
- Reading with tunnel vision

---

## The core idea behind multi-head attention
Instead of one attention mechanism, transformers use **multiple attention heads**
in parallel.

Each head:
- Looks at the same input
- Learns to focus on different relationships
- Works independently

Mental analogy:
- Multiple experts reading the same sentence,
  each focusing on something different

---

## What each attention head actually does
Every head has its own:
- Query (what it is looking for)
- Key (what it can match against)
- Value (the information it passes forward)

Each head computes:
- Attention scores using dot products between queries and keys
- How much each token should attend to every other token

This happens simultaneously across all heads.

---

## Why multiple heads matter (example)
Sentence:
"Apple released a new iPhone, but it is expensive."

Different heads may focus on:
- Pronoun resolution (“it” refers to iPhone)
- Entity recognition (Apple = company, not fruit)
- Sentiment or contrast (“but” signals a shift)
- Overall semantic meaning

No single head captures all of this alone.

---

## How results are combined
- Outputs from all heads are concatenated
- Passed through a linear layer
- Combined into a unified representation

This merges multiple perspectives into one coherent understanding.

---

## Why this enables strong context understanding
With multi-head attention:
- The model sees syntax, meaning, and relationships at once
- Long-range dependencies become easy to capture
- Context remains consistent across complex inputs

Without it, transformers would miss important connections.

---

## One-line takeaway
Multi-head attention lets transformers look at the same input from multiple
perspectives at the same time.
