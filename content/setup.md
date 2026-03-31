---
layout: default
title: Setup
nav_order: 1
---

# Setup
{: .no_toc }

{:toc}

Complete this page before the hands-on workshops (especially workshops 2 and 3). You will use **Cursor** for AI-assisted coding and **R** to run the examples (ggplot2, tidyverse).

---

## What you need

### **R** (required for 2nd and 3rd workshop)

The examples use R and packages such as **tidyverse** and **ggplot2**. Install R before the workshops:

1. Open **[cloud.r-project.org](https://cloud.r-project.org/)** (CRAN).
2. Choose your operating system (**Download R for Windows** / **Download R for macOS** / **Download R for Linux**).
3. Run the installer and accept the defaults unless your organization requires different options.
4. **Verify:** open R (or a terminal and type `R`) and run:

   ```r
   R.version.string
   ```

You should see a version line (e.g. R version 4.x).

#### **R packages used in the workshops**

After R is installed, install the packages we use for data wrangling and plots. In R, run:

```r
install.packages(c("tidyverse", "readr"))
```

`tidyverse` includes **ggplot2**, **dplyr**, **readr**, and related tools. If installation asks to compile from source and you are unsure, choose a binary/cran build when offered.

---

### **RStudio** (required for 2nd and 3rd workshop)

**RStudio Desktop** is not required for this series. The workshops are built around **Cursor** for prompts and editing; you only need a way to **run R code** (R itself, plus the packages above).

You may still want RStudio if you prefer a separate R console and plots pane:

- Download **[RStudio Desktop](https://posit.co/download/rstudio-desktop/)** (Posit).
- Install it after R is on your machine.

Alternatively, run R in a **terminal inside Cursor**, or use an R extension for your editor if you already use one. Use whichever approach lets you execute the code blocks in the workshop pages.

---

### **Cursor** (required for 2nd and 3rd workshop)

- Free IDE from [cursor.com](https://cursor.com)
- Download and install (free tier should work great for now)
- Chat shortcut: `Cmd+L` (Mac) or `Ctrl+L` (Windows/Linux)

---

### **Data — Palmer Penguins dataset**

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

**Source:** [Palmer Penguins R package](https://allisonhorst.github.io/palmerpenguins/) — learn more about the dataset  

**Artwork:** [Palmer Penguins illustrations](https://allisonhorst.github.io/palmerpenguins/articles/art.html) by [@allison_horst](https://twitter.com/allison_horst)

Save `penguins.csv` in a folder you will use with Cursor (for example a project folder that also contains `data/penguins.csv`, matching the workshop paths).

---

## Quick setup (Cursor)

![Cursor logo](../img/cursor_icon_download.png)

1. Download Cursor from [cursor.com](https://cursor.com)
2. Install and open it
3. Sign in with an account
4. Press `Cmd+L` (Mac) or `Ctrl+L` (Windows/Linux) to open Chat
5. You're ready to start!

---

## Quick start workshops

1. Start with **[Workshop 1: Fundamentals](workshops/01_fundamentals.md)** — about 30 minutes
2. Continue with **[Workshop 2: Data analysis & visualization](workshops/02_data_analysis_visualization.md)** when you're ready
3. Finish with **[Workshop 3: Building with AI](workshops/03_building_with_ai.md)**

Each workshop builds on the previous one, but you can jump around if you want.
