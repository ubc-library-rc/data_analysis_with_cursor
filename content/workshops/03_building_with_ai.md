---
layout: default
title: 3. Building with AI
parent: Workshops
nav_order: 3
---

# 3. Building with AI: Build a Real Analysis in 30 Minutes

Put it all together: load data, clean it, summarize it, plot it.

**Duration:** 30 min | **Tools:** Cursor, Python (pandas, matplotlib)

---

## What You'll Learn

- How to use Cursor Chat to write real analysis code
- Build a complete workflow from data → summary → visualization
- Quick debugging tips when things go wrong

---

## Cursor Shortcuts

| Shortcut | What It Does |
|----------|-------------|
| `Cmd+L` | Open Chat (ask questions, get code) |
| `Cmd+I` | Open Composer (generate full sections) |
| `Cmd+K` | Inline edit (fix selected code) |

---

## The Project: Quick Penguin Report

Create a new **Jupyter notebook** (`.ipynb`) for this project. This format works great in Cursor **and** Google Colab, so your code outputs appear just like a report.

Build your workflow step by step below using Cursor Chat to generate and refine analysis code (see steps below).

---

### Step 1: Load & Inspect (5 minutes)

**Chat prompt:**
```
Load data/penguins.csv with pandas. Show: how many rows,
column names, and missing values per column.
```

**Expected output:**
```python
import pandas as pd

penguins = pd.read_csv("data/penguins.csv")
print("Rows:", len(penguins))
print(penguins.columns.tolist())
print(penguins.isna().sum())
```

---

### Step 2: Clean Data (5 minutes)

**Chat prompt:**
```
Remove rows with missing values. Show how many rows we had
before and after.
```

**Expected output:**
```python
penguins_clean = penguins.dropna()
print("Before:", len(penguins), "| After:", len(penguins_clean))
```

---

### Step 3: Summary Statistics (5 minutes)

**Chat prompt:**
```
Group by species and show: count, average bill length,
average body mass. Round averages to 1 decimal place.
```

**Expected output:**
```python
summary = (
    penguins_clean.groupby("species")
    .agg(
        n=("bill_length_mm", "count"),
        avg_bill=("bill_length_mm", lambda s: round(s.mean(), 1)),
        avg_mass=("body_mass_g", lambda s: round(s.mean(), 1)),
    )
)
print(summary)
```

---

### Step 4: One Visualization (10 minutes)

**Chat prompt:**
```
Scatter plot: bill length (x-axis) vs flipper length (y-axis).
Color by species. Add title and axis labels. Use matplotlib.
```

**Expected output:**
```python
import matplotlib.pyplot as plt

species_colors = {
    "Adelie": "#4878d0",
    "Chinstrap": "#ee854a",
    "Gentoo": "#6acc65",
}

fig, ax = plt.subplots(figsize=(6, 4))
for sp in ["Adelie", "Chinstrap", "Gentoo"]:
    sub = penguins_clean[penguins_clean["species"] == sp]
    ax.scatter(
        sub["bill_length_mm"],
        sub["flipper_length_mm"],
        c=species_colors[sp],
        label=sp,
        alpha=0.7,
        s=20,
    )

ax.set_title("Penguin Measurements")
ax.set_xlabel("Bill Length (mm)")
ax.set_ylabel("Flipper Length (mm)")
ax.legend(title="Species")
plt.show()
```

---

## If Something Goes Wrong

**Error in your code?**
1. Copy the full error message
2. Open Chat (`Cmd+L`)
3. Paste: `I'm getting this error: [paste error]. Here's my code: [paste code]. What does it mean?`

**Plot doesn't look right?**
1. Select the plot code
2. Press `Cmd+K`
3. Type: `Make this plot [describe what you want]`

---

## Next Steps

Pick one to extend your analysis:
- Add a second plot (box plot of body mass by species)
- Calculate correlation between bill length and flipper length
- Compare just two species instead of all three
- Save your results to a CSV file

---

## Key Takeaways

1. **Start simple** — load, clean, summarize, plot
2. **Use Chat for guidance** — don't try to memorize pandas or matplotlib syntax
3. **Test after each step** — catch mistakes early
4. **Iterate** — your first version won't be perfect, and that's OK

---

## Resources

- [Cursor docs](https://docs.cursor.com)
- [pandas documentation](https://pandas.pydata.org/docs/)
- [Matplotlib documentation](https://matplotlib.org/stable/index.html)

---

**Previous:** [2. Data Analysis & Visualization](02_data_analysis_visualization.md)

---

Congratulations! You now know how to use AI tools to do real data analysis.
