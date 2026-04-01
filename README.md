# Mapping the Soul's Journey: A Text Analysis of the Egyptian Book of the Dead

**Authors:** Clare McGarvey & Sude Boz  
**Course:** Text Mining — MUCSS 25/26  

---

## Overview

This project applies computational text mining to the *Egyptian Book of the Dead*, a collection of Ancient Egyptian funerary spells, hymns and prayers designed to guide the deceased through the afterlife. The edition analysed is the 1904 English translation by P. Le Page Renouf and Édouard Naville, sourced from Project Gutenberg (ID: 69566).

The central question is whether the text has a measurable internal structure — whether the vocabulary and emotional register shift meaningfully as the soul progresses through the four theological sections established during the Saïte Period (26th Dynasty).

---

## Techniques Used

- **TF-IDF** — to identify the vocabulary most distinctive to each of the four theological sections, confirming whether the text follows the canonical Saïte ordering
- **NRC Sentiment Analysis** — to map the emotional arc of the text across sections, using the eight-emotion NRC lexicon
- **Zipf's Law** — to verify that this 3,000-year-old ritual text follows the same statistical regularities as natural language

---

## Key Findings

- The vocabulary shifts distinctly across the four sections, from ceremonial reunification language (Section I) through mythological conflict (Section II), spatial and procedural imagery (Section III), to architectural and devotional language at final vindication (Section IV).
- Trust is the dominant emotion across the entire text — more prevalent than fear — consistent with the book's function as a reassuring guide rather than a document of dread.
- Trust and fear move in near-perfect opposition across sections: fear peaks in Section II (the Osiris myth), while trust peaks in Section IV (final vindication). The two techniques are mutually reinforcing.
- Despite its age and archaic language, the text conforms to Zipf's law.

---

## Repository Structure
```
├── BozSude_McGarveyClare_TMFinalAssignment.qmd   # Main analysis notebook
├── BozSude_McGarveyClare_TMFinalAssignment.html  # Rendered output
├── pg69566-images.epub                           # Source text (Project Gutenberg)
└── README.md
```

---

## Requirements

The analysis is written in R and requires the following packages:
```r
install.packages(c("tidytext", "stringr", "dplyr", "epubr", 
                   "ggplot2", "textdata", "tidyr"))
```

To reproduce the analysis, place `pg69566-images.epub` in the same directory as the `.qmd` file and render with Quarto.

The epub can be downloaded directly from Project Gutenberg:  
https://www.gutenberg.org/ebooks/69566

---

## Source

The Egyptian Book of the Dead (P. Le Page Renouf & E. Naville, Trans.). (2022). Project Gutenberg. (Original work published 1904). https://www.gutenberg.org/ebooks/69566
