---
layout: default
title: 1. Fundamentals
parent: Workshops
nav_order: 1
---

# 1. Fundamentals of AI-Assisted Coding

Learn how LLMs work and write better prompts.

**Duration:** 30 min

---

## Learning objectives

By the end of this workshop, you will know:

- How LLMs work and why tokens matter
- The prompt formula: context + task + constraints + format
- How to write focused, specific prompts that work
- Why conversation history affects your results

---

## Key Idea: Why Tokens & Context Matter for Learning with AI

Before we can get the most out of AI-assisted coding, it's important to understand how the underlying models work. LLMs, like the ones powering coding assistants, process everything as tokens (short pieces of words or characters—not full words). Even more crucially, these models consider **the entire conversation history** when generating each new response.

**Why does this matter for you as a learner?**  
- Every message—including previous questions—affects the AI's answers.
- Long or unfocused prompts can quickly use up tokens (the model’s memory), making responses less clear or even cutting off your conversation.
- Learning to write precise, clear prompts helps you get more relevant support, improves the quality of help you receive, and mirrors good communication with real collaborators.

### See It in Action: Explore Your Prompt's Token Breakdown

Understanding how many tokens your prompt uses is a practical way to see this in action—and helps you develop stronger prompts. Try pasting your questions into the tool below to measure and refine your prompts for clarity and efficiency.

**🔗 [Open Tiktokenizer in new tab](https://tiktokenizer.vercel.app/)**

> - "10 facts about penguin demographics and behaviors. What makes penguins so fascinating..."
<<<<<<< HEAD
=======

>>>>>>> 973c656204b510c988438e7fb3c10aa61ea6d807


---

## The Prompt Formula

When asking AI to help with data, a clear prompt gives better results. A simple structure you can use is:

```
Context: What data do you have?
Task: What do you want to do?
Constraints: Any details or tools to use?
Format: How should the answer look?
```

You can remember it as: **Context + Task + Constraints + Format**

Let's look at two ways to ask for help:

**Bad (vague):**
> "Tell me about my penguin data."

**Better (simple and clear):**
> "I have a CSV file with penguin data. How many columns does it have? Show me the column names as a list."

**Why the better prompt works:**  
- It tells the AI what data you're working with (context)  
- States what you want to know (task)  
- Asks for a specific output (format)

You can build on this as you get more comfortable. For example, you might add a tool or a more specific task:

> "I have `penguins.csv`. Using pandas, show me the average flipper length for each species as a table."

Start simple! 
- Being specific helps, but you don’t need complex instructions
- e.g. "How would you ask a person over the phone who has not seen your file?"

---

## Quick Try-Out: What Would YOU Ask?

Let's make this interactive!  
Imagine you have a file called `data/penguins.csv` with penguin data.

### Which prompt would you be most interested in trying?

Select one option:

- [ ] **A**: Load `data/penguins.csv` with pandas and show me the first 5 rows and column names.
- [ ] **B**: I have `data/penguins.csv` with penguin measurements. Use pandas to group by species and count how many in each. Show as a table.
- [ ] **C**: Plot a histogram of flipper length for each species in `data/penguins.csv` using matplotlib.
- [ ] **D**: Find any missing values in the `penguins.csv` data and tell me which columns have them.

### Data — Palmer Penguins dataset

Preview of the data we'll work with:

| species | island | bill_length_mm | bill_depth_mm | flipper_length_mm | body_mass_g | sex | year |
|---------|--------|----------------|---------------|-------------------|-------------|-----|------|
| Adelie | Torgersen | 39.1 | 18.7 | 181 | 3750 | male | 2007 |
| Adelie | Torgersen | 39.5 | 17.4 | 186 | 3800 | female | 2007 |
| Adelie | Torgersen | 40.3 | 18.0 | 195 | 3250 | female | 2007 |
| Chinstrap | Dream | 46.5 | 17.9 | 192 | 3500 | female | 2007 |
| Gentoo | Biscoe | 46.1 | 13.2 | 211 | 4500 | female | 2007 |

**344 rows × 8 columns**

**[Download dataset (CSV)](../data/penguins.csv)**

**Source:** [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/)  

**Artwork:** [Illustrations](https://allisonhorst.github.io/palmerpenguins/articles/art.html) by [@allison_horst](https://twitter.com/allison_horst)


What about these promts them less effective?  

- “what’s in the file”
- “analyze this”
- “find errors”
- “run pandas”
- “missing values??”


Notice how these are vague or missing context. As you practice, try to avoid these and be clear about what you want!


---

## Key Takeaways

1. **Be specific** — the more detail, the better
2. **Be concise** — don't ramble
3. **State your format** — say exactly what output you want (table, plot, list, etc.)
4. **Tools matter** — when you want code, say which language or libraries you have in mind (e.g. pandas)—you can still practice the wording without installing anything

---

## Resources

- [Cursor docs](https://docs.cursor.com)
- [Palmer Penguins dataset](https://allisonhorst.github.io/palmerpenguins/)

---

**Next:** [2. Data Analysis & Visualization](02_data_analysis_visualization.md)
