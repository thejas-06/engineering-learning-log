# How Prompts Steer LLM Behavior and Knowledge

This note explains how models like **ChatGPT**
understand prompts and why structured prompting produces better results.

---

## What happens when I type a prompt
Transformer-based models use attention to weigh every word in the input.

What this means:
- Different words activate different internal knowledge paths
- Adding details changes *which* concepts become active

Example:
- "Explain quantum physics"
- vs
- "Explain quantum physics like I'm 5, using ice cream analogies"

Both trigger different internal reasoning routes.

---

## Mental model: knowledge routing
The model already contains vast knowledge.

Your prompt:
- Does not add new knowledge
- Selects *which knowledge path* to use

Better prompts help the model “settle” into the right reasoning pathway.

---


## The structured prompt formula
A reliable prompt structure is:

**Role + Context + Task + Constraints + Format**

---

## Example (to remember)
Role:
- “You are a senior Python developer”

Context:
- “I’m building a web scraper”

Task:
- “Write a pagination function”

Constraints:
- “Use BeautifulSoup and include error handling”

Format:
- “Output only the code”

This structure narrows the reasoning space and activates relevant expertise.

---

## Why examples make it even stronger
Adding 2–3 examples (few-shot prompting):
- Gives the model a concrete pattern
- Guides tone, structure, and expectations
- Requires no retraining

The model uses attention to match examples with the new task.

---

## Key insight
The model already “knows” how to do many things.

Prompting is not teaching — it is **unlocking**.

---

## One-line takeaway
Good prompts guide attention; bad prompts leave the model guessing.
