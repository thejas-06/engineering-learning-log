# Mamba

## The inefficiency before this
Transformer-based chat models reread the entire conversation history
for every new prompt.

Mental analogy:
- Re-reading a whole book to remember the last page.

---

## Why that inefficiency mattered
As conversations grew longer:
- Latency increased
- Compute costs exploded
- Real-time interaction became harder

The model did not remember — it recomputed.

---

## What changed with Mamba
Mamba maintains a running internal state that updates continuously
instead of reprocessing the full sequence.

The model remembers as it goes.

---

## Why this fix is important
- Long conversations stay fast
- Long time-series become practical
- Pattern detection across years of data becomes efficient

This enables real-time, long-context AI systems.

---

## One-line takeaway
Mamba replaces repeated recomputation with persistent memory.
