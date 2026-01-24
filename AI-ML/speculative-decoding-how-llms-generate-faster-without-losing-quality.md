# Speculative Decoding: How LLMs Generate Faster Without Losing Quality

This note explains speculative decoding — a technique that reduces
LLM latency by combining a small fast model with a large accurate model.

---

## Why latency is still a problem
Large models are powerful but slow.

Even with:
- GPUs
- Quantization
- Optimized kernels

Autoregressive generation still means:
- One token at a time
- High time-to-first-token (TTFT)
- High compute cost at scale

---

## The core idea (simple intuition)
Speculative decoding is like:
- A fast intern drafting text
- A senior expert approving it

The expert doesn’t write everything —
they only verify.

---

## What speculative decoding actually does
Instead of one model doing all the work:

- A **small model** proposes multiple future tokens quickly
- A **large model** verifies those tokens in one pass

If the tokens look good → accept them in bulk  
If not → fall back to normal generation

Accuracy stays high.
Latency drops.

---

## Step-by-step flow

### 1. Drafting
A small, fast model predicts **K future tokens** in advance.

Example:
- Predict next 5–10 tokens at once

---

### 2. Verification
The large model runs a forward pass and checks:
- Do these tokens match my probability distribution?

This is cheaper than full generation.

---

### 3. Acceptance or fallback
- If confidence is high → accept tokens in bulk
- If not → discard and let the large model generate

The system stays correct by design.

---

## Why this reduces latency
- Fewer sequential decoding steps
- Faster time-to-first-token (TTFT)
- Better GPU utilization
- Lower cost per response

Users see responses *almost instantly*.

---

## Important clarification
Speculative decoding:
- Does NOT change the model weights
- Does NOT reduce accuracy
- Works entirely at inference time

It’s a **systems-level optimization**, not a training trick.

---

## One-line takeaway
Speculative decoding makes large models fast by letting
small models draft and big models approve — saving time without sacrificing quality.
