# Data Science Portfolio

Portfolio of the projects I build during my Master's in Smart Data Science at
ENSAI (2026–2027), written as a [Quarto](https://quarto.org) book.

## Contents

| Chapter | Content | Status |
|---|---|---|
| 1 · EDA | Electricity production, consumption and exchanges across French regions (RTE éCO2mix) | Done |
| 2 · Semester 2 | To come | Placeholder |
| 3 · Semester 3 | To come | Placeholder |

## Project structure

```
├── _quarto.yml      # book configuration (title, chapters, output format)
├── _brand.yml       # colours and fonts
├── styles.scss      # extra CSS
├── index.qmd        # home page
├── chapters/        # one .qmd file per chapter
├── references.qmd   # bibliography page
├── references.bib   # citations
├── data_import.R    # downloads and pins the data used in chapter 1
└── uvr.toml         # pinned R environment (uvr)
```

## Reproducing the book

1. Restore the R environment with [uvr](https://github.com/nbafrank/uvr) from
   `uvr.toml` / `uvr.lock` (R version in `.r-version`).
2. Run `data_import.R` once to download the data into `data/` (not versioned).
3. Render the book:

   ```bash
   quarto render            # whole book
   quarto preview           # live preview while editing
   ```

Chapter 1 also needs an internet connection at render time, to load the regional
boundaries used in the maps.
