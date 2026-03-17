---
layout: default
title: Data Analysis & Visualization
nav_order: 2
---

# 2. Data Analysis & Visualization

Create charts and plots with AI using ggplot2.

**Duration:** 30 min | **Tools:** Cursor, R, ggplot2

---

## What You'll Learn

- Build 2 quick visualizations using AI prompts
- Understand what ggplot2 code looks like
- Know when to use which chart type

---

## Setup (2 minutes)

```r
library(tidyverse)

penguins <- read_csv("data/penguins.csv") |> drop_na()

species_colors <- c(Adelie = "#4878d0", Chinstrap = "#ee854a", Gentoo = "#6acc65")
```

---

## Chart 1: Bar Plot (Species Count)

**Cursor prompt:**
> "Create a bar chart showing how many penguins are in each species. Use the species_colors palette. Add count labels on top of each bar."

```r
penguins |>
  count(species) |>
  ggplot(aes(x = species, y = n, fill = species)) +
  geom_col(width = 0.6, show.legend = FALSE) +
  geom_text(aes(label = n), vjust = -0.4, fontface = "bold") +
  scale_fill_manual(values = species_colors) +
  labs(title = "Penguin Count by Species", x = NULL, y = "Count") +
  theme_minimal()
```

---

## Chart 2: Scatter Plot (Bill vs. Flipper Length)

**Cursor prompt:**
> "Create a scatter plot with bill length on x-axis and flipper length on y-axis. Color by species using species_colors. Add title and axis labels."

```r
penguins |>
  ggplot(aes(x = bill_length_mm, y = flipper_length_mm, color = species)) +
  geom_point(alpha = 0.7, size = 2) +
  scale_color_manual(values = species_colors) +
  labs(
    title = "Bill Length vs. Flipper Length",
    x = "Bill Length (mm)",
    y = "Flipper Length (mm)",
    color = "Species"
  ) +
  theme_minimal()
```

---

## Your Turn (10 minutes)

Pick one and use Cursor Chat to build it:

**Option 1:** Box plot of body mass by species  
**Option 2:** Histogram of flipper length with overlays by species  
**Option 3:** Simple table showing average measurements per species

**Tip:** Open Chat (`Cmd+L`), paste one of these, and let Cursor write the code:
```
"Create a [chart type] showing [what data]. Use species_colors. Add title and labels."
```

---

## Key Takeaways

- Use **bar charts** for counts across categories
- Use **scatter plots** to see relationships between two measurements
- Use **box plots** to compare distributions
- Always **specify colors, titles, and labels** in your prompts

---

## Resources

- [ggplot2 reference](https://ggplot2.tidyverse.org/reference/)
- [Common chart types](https://www.r-graph-gallery.com/)

---

**Previous:** [1. Fundamentals](1_fundamentals.md)  
**Next:** [3. Building with AI](3_building_with_ai.md)
