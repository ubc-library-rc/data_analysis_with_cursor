---
layout: default
title: Building with AI
nav_order: 3
---

# 3. Building with AI: Build a Real Analysis in 30 Minutes

Put it all together: load data, clean it, summarize it, plot it.

**Duration:** 30 min | **Tools:** Cursor, R, RStudio or R Markdown

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

Create a new `.R` file and use Cursor Chat to build these 4 steps:

---

### Step 1: Load & Inspect (5 minutes)

**Chat prompt:**
```
Load data/penguins.csv with readr. Show: how many rows, 
column names, and any missing values per column.
```

**Expected output:**
```r
library(tidyverse)
penguins <- read_csv("data/penguins.csv")
cat("Rows:", nrow(penguins), "\n")
names(penguins)
penguins |> summarise(across(everything(), ~ sum(is.na(.))))
```

---

### Step 2: Clean Data (5 minutes)

**Chat prompt:**
```
Remove rows with missing values. Show how many rows we had 
before and after.
```

**Expected output:**
```r
penguins_clean <- penguins |> drop_na()
cat("Before:", nrow(penguins), "| After:", nrow(penguins_clean), "\n")
```

---

### Step 3: Summary Statistics (5 minutes)

**Chat prompt:**
```
Group by species and show: count, average bill length, 
average body mass. Round to 1 decimal place.
```

**Expected output:**
```r
penguins_clean |>
  group_by(species) |>
  summarise(
    n = n(),
    avg_bill = round(mean(bill_length_mm), 1),
    avg_mass = round(mean(body_mass_g), 1)
  )
```

---

### Step 4: One Visualization (10 minutes)

**Chat prompt:**
```
Scatter plot: bill length (x-axis) vs flipper length (y-axis).
Color by species. Add title and axis labels. Use minimal theme.
```

**Expected output:**
```r
penguins_clean |>
  ggplot(aes(x = bill_length_mm, y = flipper_length_mm, color = species)) +
  geom_point(alpha = 0.7, size = 2) +
  labs(
    title = "Penguin Measurements",
    x = "Bill Length (mm)",
    y = "Flipper Length (mm)"
  ) +
  theme_minimal()
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
2. **Use Chat for guidance** — don't try to memorize R syntax
3. **Test after each step** — catch mistakes early
4. **Iterate** — your first version won't be perfect, and that's OK

---

## Resources

- [Cursor docs](https://docs.cursor.com)
- [R for Data Science](https://r4ds.hadley.nz)
- [ggplot2 examples](https://ggplot2.tidyverse.org/reference/)

---

**Previous:** [2. Data Analysis & Visualization](2_data_analysis_visualization.md)

---

Congratulations! You now know how to use AI tools to do real data analysis.
