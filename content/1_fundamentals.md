---
layout: default
title: Fundamentals of AI-Assisted Coding
nav_order: 1
---

# 1. Fundamentals of AI-Assisted Coding

Learn how LLMs work and write better prompts.

**Duration:** 30 min | **Tools:** Cursor, R

---

## What You'll Learn

- Why **tokens** matter in AI prompts
- How to write prompts that get better results
- The "prompt formula" for asking AI to help with data

---

## Key Idea: Tokens & Context

Models don't see words — they see tokens (roughly 0.75 words each). More importantly, every time you send a message, the model receives **your entire conversation history**, not just your latest message.

**This means:** Keep prompts short and specific. Rambling wastes tokens and confuses the AI.

---

## The Prompt Formula

Good prompts have 4 parts:

```
"I have [data]. I want to [task]. Use [constraints]. Show [format]."
```

**Example:**
> "I have `data/penguins.csv` with 344 penguins and 7 columns. Load it with readr and group by species to show average bill length and body mass. Use dplyr. Show as a tibble rounded to 1 decimal."

**Bad (vague):**
> "Tell me about my data."

**Why the good version works:** It tells the AI *what* data, *what* analysis, *what* tools, and *what* output format.

---

## Quick Try-Out

Open Cursor Chat (`Cmd+L`) and try one of these prompts:

```
"Load `data/penguins.csv` with readr and show me the first 5 rows and column names."
```

OR

```
"I have `data/penguins.csv` with penguin measurements. Group by species and count how many in each. Show as a table."
```

---

## Key Takeaways

1. **Be specific** — the more detail, the better
2. **Be concise** — don't ramble
3. **State your format** — say exactly what output you want (table, plot, list, etc.)
4. **Tools matter** — mention which R packages to use (dplyr, ggplot2, etc.)

---

## Resources

- [Cursor docs](https://docs.cursor.com)
- [Palmer Penguins dataset](https://allisonhorst.github.io/palmerpenguins/)

---

**Next:** [2. Data Analysis & Visualization](2_data_analysis_visualization.md)
