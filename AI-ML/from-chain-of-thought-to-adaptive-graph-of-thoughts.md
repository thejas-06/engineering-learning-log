# From Chain of Thought to Adaptive Graph of Thoughts (AGOT)

This note explains why linear reasoning (Chain of Thought) is limited
and how Adaptive Graph of Thoughts enables more human-like problem solving.

---

## Chain of Thought (CoT): the linear approach
Chain of Thought reasoning forces the model to:
- Think step by step
- Follow one straight reasoning path
- Reach a final answer linearly

This works well for:
- Math problems
- Simple logic
- Clearly defined tasks

But real-world problems aren’t linear.

---

## Why linear reasoning breaks down
In real problem-solving, humans:
- Explore multiple ideas
- Abandon bad paths
- Revisit earlier assumptions
- Combine partial insights

Linear CoT:
- Commits too early
- Can’t easily backtrack
- Misses alternative solutions

---

## The core idea behind AGOT
Adaptive Graph of Thoughts treats reasoning as a **graph**, not a line.

How it works:
- Each idea becomes a node
- Relationships become edges
- Multiple reasoning paths are explored in parallel

Reasoning becomes flexible, not forced.

---

## How exploration is controlled
A controller algorithm manages the graph.

Its role:
- Decide which paths to expand
- Prune weak or redundant ideas
- Merge promising branches
- Allocate compute to the best directions

The LLM itself stays the same.
Only the **inference-time orchestration** changes.

---

## Mental model
Think of a team solving a hard problem on a whiteboard:
- Ideas are written down
- Bad ones are erased
- Good ones are connected
- Multiple perspectives evolve together

AGOT turns this into a machine process.

---

## Why this matters for complex domains
AGOT shines when problems have competing objectives.

Example: drug discovery
- One branch explores new molecules
- Another checks toxicity
- Another evaluates manufacturing cost

Instead of competing, these paths:
- Coexist
- Exchange information
- Merge into a balanced solution

---

## What actually changed (important)
AGOT does NOT require:
- Bigger models
- New training
- More parameters

It changes:
- How reasoning paths are generated
- How they are evaluated
- How they are combined

This is a systems-level improvement.

---

## One-line takeaway
Chain of Thought thinks in a straight line; Adaptive Graph of Thoughts
thinks like a team — exploring, pruning, and synthesizing ideas dynamically.
