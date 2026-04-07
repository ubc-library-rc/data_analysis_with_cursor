---
layout: default
title: Setup
nav_order: 1.3
---

# Setup
{: .no_toc }

{:toc}

The concepts we cover are general and apply to many languages and tools. In this series we demonstrate how to code in R using the Cursor Integrated Development Environment (IDE), which provides a simple way to incorporate AI into the coding process. We encourage you to apply what you learn in your own environments.

Complete this page before the hands-on workshops (especially workshops 2 and 3). We will use **Cursor** for AI-assisted coding and **RStudio** to run the examples (ggplot2, tidyverse).

For Python: We also include this exact text for Python and mention why we use the combination of these tools—one ecosystem with Cursor: many learners already use Python; notebooks/scripts in the repo feel natural next to AI chat.

---

## What you need

### Python

**Stack:** Python **3.11 or newer**, plus **pandas** (tables) and **matplotlib** (plots). 

### **Cursor** (required)

- Free IDE from [cursor.com](https://cursor.com)
- Download and install (the free tier is enough for these workshops)
- Chat shortcut: `Cmd+L` (Mac) or `Ctrl+L` (Windows/Linux)

---

### Cursor

![Cursor logo](../img/cursor_icon_download.png)

1. Download **[cursor.com](https://cursor.com)** → choose your OS → install.
2. Open Cursor and **sign in**.
3. Open Chat: **`Cmd+L`** (Mac) or **`Ctrl+L`** (Windows / Linux).

---

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

![Palmer Penguins illustrations](../img/lter_penguins.png)

**[Download dataset (CSV)](../data/penguins.csv)**

**Source:** [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/)  

**Artwork:** [Illustrations](https://allisonhorst.github.io/palmerpenguins/articles/art.html) by [@allison_horst](https://twitter.com/allison_horst)

Put `penguins.csv` in your project so paths match the workshops (e.g. `data/penguins.csv` next to your scripts or notebook).

---

## Quick start workshops

1. **[Workshop 1: Fundamentals](workshops/01_fundamentals.md)** — ~30 min  
2. **[Workshop 2: Data analysis & visualization](workshops/02_data_analysis_visualization.md)**  
3. **[Workshop 3: Building with AI](workshops/03_building_with_ai.md)**

Workshops build on each other, but you can change the order if you prefer.
