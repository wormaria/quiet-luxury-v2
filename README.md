# When the Economy Turns Grey, So Does Fashion  
### A Machine Learning Analysis of Color Trends and Macroeconomic Conditions — Expanded Edition

<p align="left">
  <img src="https://img.shields.io/badge/Python-3.11-blue?logo=python" />
  <img src="https://img.shields.io/badge/Machine%20Learning-KMeans-orange" />
  <img src="https://img.shields.io/badge/Computer%20Vision-OpenCV-green" />
  <img src="https://img.shields.io/badge/Data-FRED%20API-lightgrey" />
  <img src="https://img.shields.io/badge/Data-Google%20Trends-4285F4" />
  <img src="https://img.shields.io/badge/Status-In%20Progress-yellow" />
</p>

---

## Overview

Fashion is often described as a reflection of economic sentiment — but most evidence remains anecdotal (e.g., the "lipstick effect").

This project takes a **data-driven approach**.

Using **computer vision and unsupervised machine learning**, I analyze **2,400 runway images (2000–2023)** to quantify changes in color intensity and test whether fashion becomes more "neutral" during economic downturns.

This expanded version adds **Google Trends data**, **consumer sentiment**, **quiet luxury market context**, and **luxury peer performance comparisons** to strengthen the original findings.

> **Key Question:**  
> When the economy weakens, does fashion become more muted?

---

## What's New (v2)

This repository extends the [original project](https://github.com/wormaria/when-the-economy-turns-grey-so-does-fashion) with:

| Addition | Description |
|----------|-------------|
| **Google Trends** | Search interest data for "quiet luxury," "neutral fashion," "minimalist fashion," "old money aesthetic," and "capsule wardrobe" (2004–2026) |
| **Consumer Sentiment** | University of Michigan Consumer Sentiment Index (UMCSENT) from FRED |
| **GDP & S&P 500** | Additional macro indicators for richer regression models |
| **Quiet Luxury Market Data** | $137.5B (2024) → $278B (2034) market sizing, +734% demand surge |
| **Luxury Peer Comparison** | Ralph Lauren vs. LVMH vs. Kering indexed revenue performance |
| **Enhanced Regressions** | 4 model specifications including consumer sentiment and lagged indicators |
| **Updated Quarto Report** | New sections on extended economic analysis, quiet luxury context, and Google Trends validation |

---

## Key Results

- 📉 Higher unemployment → **lower color intensity (chroma)**
- ⚫ Recession periods → **more neutral color palettes**
- 📊 Consumer sentiment positively correlates with chroma — when confidence drops, palettes go muted
- 🔍 Google Trends "quiet luxury" interest surged post-2022, coinciding with macro uncertainty
- 👗 Heritage brands (Ralph Lauren, +61%) dramatically outperform trend-driven peers (Kering, −12%) during the quiet luxury shift
- ⏳ Evidence of **lagged response** in fashion trends

---

## Project Structure

```
fashion-trends-recession/
├── WhentheEconomyTurnsGrey.qmd    # Main Quarto report (expanded)
├── references.bib                  # Bibliography (13 sources)
├── styles.css                      # Report styling
├── pyproject.toml                  # Project config
├── requirements.txt                # Python dependencies
├── src/                            # Core modules
│   ├── color_utils.py              # CIELab conversion, chroma computation
│   ├── image_utils.py              # Background removal, pixel sampling
│   └── metrics.py                  # Neutrality metrics (chroma, neutral share)
├── notebooks/                      # Analysis notebooks
│   ├── 01_new_data_sources.ipynb   # Google Trends, FRED, S&P 500, GDP
│   ├── 02_quiet_luxury_context.ipynb # Market sizing, peer comparison, RL thesis
│   └── 03_enhanced_visualizations.ipynb # Correlation analysis, enhanced regressions
├── data/
│   ├── external/                   # Downloaded economic & trends data
│   └── figures/                    # Generated visualizations
└── images/                         # Report images
```

---

## Data Sources

| Source | Description |
|--------|-------------|
| Vogue Runway | 100 images/year (2000–2023) via Internet Archive |
| FRED | U.S. unemployment rates, consumer sentiment, GDP growth, recession indicators |
| Google Trends | Search interest for quiet luxury and neutral fashion terms |
| S&P 500 | Market returns as macro proxy |
| Accio Research | Quiet luxury market sizing |
| McKinsey & Co | State of Fashion 2026 report |

---

## Tech Stack

- **Python 3.11**
- `scikit-learn` – KMeans clustering  
- `OpenCV`, `rembg` – image processing  
- `pandas`, `NumPy` – data manipulation  
- `Matplotlib` – visualization  
- `statsmodels` – OLS regression  
- `pytrends` – Google Trends API  
- FRED API – macroeconomic data  
- Quarto – report rendering

---

## Author

**Maria Workman**  
UNC Chapel Hill — Statistics & Computer Science
