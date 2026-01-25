# Sparse Attention vs Flash Attention: How LLMs Handle Long Context Efficiently

This note explains what happens when prompts become very long
and how sparse attention and flash attention solve different parts of the problem.

---

## The core problem: long prompts
Transformers use **all-to-all attention**.

This means:
- Every token compares with every other token
- Compute and memory grow quadratically (O(n²))

With long documents (PDFs, legal text, codebases),
this becomes slow and extremely expensive.

---

## Why naive attention is wasteful
Example:
- A 500-page contract

Do we really need:
- Every word on page 1
- Compared with every word on page 500?

No.

Most relationships are local or thematic.

---

## Sparse Attention: compute less by focusing smarter
Sparse attention changes **who attends to whom**.

Key idea:
- Tokens only attend to *relevant* tokens
- Skip unnecessary comparisons

Common patterns:
- Local windows
- Block or chunk attention
- Global tokens (headers, summaries)

Result:
- Far fewer attention operations
- Massive compute savings
- Context preserved where it matters

Mental model:
- Only cross-reference related sections in a document

---

## Flash Attention: same attention, faster math
Flash attention does **not change attention patterns**.

Instead, it optimizes:
- Memory access
- GPU utilization
- Kernel execution order

Problem with standard attention:
- Constant memory transfers between GPU and RAM
- Bottlenecks dominate runtime

Flash attention:
- Reorders computation
- Keeps data in GPU memory
- Computes attention in fused steps

Mental model:
- Take all ingredients out once
- Cook efficiently without running back and forth

---

## Key difference (important)
- Sparse attention → *reduces what you compute*
- Flash attention → *computes the same thing faster*

They solve different bottlenecks.

---

## Why modern LLMs need both
Models like **GPT-4**
support extremely long contexts (100K+ tokens) because:

- Sparse attention controls quadratic explosion
- Flash attention makes GPU execution efficient

Together:
- Long documents become affordable
- Latency stays reasonable
- Costs don’t explode

---

## One-line takeaway
Sparse attention reduces *how much* attention you compute;
flash attention reduces *how fast* you compute it.
