# What Makes AI Agentic and How Agents Work

This note explains what agentic AI really means and how agent-based systems
are structured behind the scenes.

---

## The shift from traditional AI to agentic AI
Traditional AI responds when prompted.

Agentic AI:
- Observes
- Plans
- Acts
- Adapts without constant human input

Mental shortcut:
- Traditional AI waits for you to click
- Agentic AI clicks on its own

---

## Core idea of agentic AI
Agentic AI is not a single model.

It is a **multi-component system** where different parts communicate
in a feedback loop and update internal state over time.

---

## Core components of an agentic AI system

### 1. LLM (Reasoning Brain)
The LLM acts as the core reasoning unit.

What it does:
- Understands goals
- Generates ideas
- Interprets results
- Decides next actions

Example:
- **Chatbot**

---

### 2. Planner
The planner decomposes high-level goals into steps.

Example:
Goal: “Plan a trip”

Planner output:
1. Book flight  
2. Reserve hotel  
3. Create itinerary  

This planning step may itself be driven by the LLM.

---

### 3. Actuator (Tool Executor)
The actuator performs real actions.

What it can do:
- Call APIs
- Access websites
- Read or write files
- Execute scripts
- Click buttons

Important distinction:
- LLM decides *what* to do
- Actuator executes *how* it is done

---

### 4. Memory Module
Stores:
- Past actions
- Results
- Observations
- User preferences

This allows:
- Learning from outcomes
- Avoiding repeated mistakes
- Long-term behavior consistency

---

## How the agent loop works
1. Observe environment or input  
2. Update memory  
3. Plan next steps  
4. Execute actions via tools  
5. Evaluate results  
6. Repeat  

This loop runs continuously.

---

## What makes agents proactive
Agentic systems don’t wait for prompts.

They:
- Monitor conditions
- Detect changes
- Trigger actions automatically

Examples:
- **Google Duplex** booking reservations
- Trading bots monitoring markets 24/7

---

## Why this changes everything
Agentic AI adds:
- Eyes (observation)
- Hands (tools)
- Memory (state)
- Planning (goal decomposition)

Not just intelligence, but **agency**.

---

## One-line takeaway
Agentic AI combines reasoning, planning, memory, and tools to act autonomously
instead of just responding.
