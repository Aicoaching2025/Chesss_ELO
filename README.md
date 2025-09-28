# ♟️ Chess Tournament Performance Analysis

<div align="center">

![Chess](https://img.shields.io/badge/Game-Chess-black?style=for-the-badge&logo=chess.com)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![Analysis](https://img.shields.io/badge/Analysis-ELO%20Rating-gold?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

**🎯 Analyzing chess tournament performance using ELO-based expected scores**

</div>

---

## 📋 Table of Contents
- [🎯 Project Overview](#-project-overview)
- [📊 Dataset](#-dataset) 
- [🧮 Methodology](#-methodology)
- [🚀 Getting Started](#-getting-started)
- [📈 Key Results](#-key-results)
- [🔧 Requirements](#-requirements)
- [📁 Files](#-files)
- [📚 References](#-references)

---

## 🎯 Project Overview

This project analyzes chess tournament performance by comparing **actual scores** to **ELO-based expected scores**. Using the USCF standard ELO formula, we identify players who significantly over or underperformed relative to their pre-tournament ratings.

### 🎪 What Makes This Analysis Special?
- ✅ **Precise calculations** using individual opponent ratings
- ✅ **USCF standard methodology** for academic rigor  
- ✅ **Comprehensive performance metrics** for all players
- ✅ **Beautiful visualizations** and detailed reporting

---

## 📊 Dataset

The analysis uses tournament data containing:

| Column | Description | Example |
|--------|-------------|---------|
| `Player_Name` | Tournament participant | "GARY HUA" |
| `State` | Player location | "ON", "MI" |
| `Total_Points` | Actual tournament score | 6.0, 5.5 |
| `Pre_Rating` | ELO rating before tournament | 1794, 1553 |
| `Opponent_Ratings` | Semicolon-separated opponent ratings | "1423;1595;1629" |

📈 **Total Players Analyzed:** 63  
🎮 **Games per Player:** 5-7 rounds

---

## 🧮 Methodology

### ELO Expected Score Formula
```
Expected Score = 1 / (1 + 10^((Opponent Rating - Player Rating)/400))
```

**📖 Source:** United States Chess Federation Official Rules of Chess, 7th edition

### 🔄 Analysis Process
1. **Data Cleaning** - Remove invalid entries and parse opponent ratings
2. **Expected Score Calculation** - Apply ELO formula for each game
3. **Performance Analysis** - Compare actual vs expected scores
4. **Ranking** - Identify top over/underperformers

---

## 🚀 Getting Started

### 💻 Installation
```r
# Install required packages
install.packages(c("readr", "dplyr", "stringr", "ggplot2"))

# Load libraries
library(readr)
library(dplyr)
library(stringr)
library(ggplot2)
```

### 🏃‍♂️ Quick Start
```r
# 1. Load the data
source("chess_elo_analysis.R")

# 2. View results
head(performance_summary)

# 3. Generate plots (optional)
# Histogram and scatter plots included in script
```

---

## 📈 Key Results

### 🏆 TOP 5 OVERPERFORMERS

| Rank | Player | Rating | Actual | Expected | Diff |
|------|--------|--------|--------|----------|------|
| 🥇 | **ADITYA BAJAJ** | 1384 | 6.00 | 2.86 | **+3.14** |
| 🥈 | **JACOB ALEXANDER LAVALLEY** | 377 | 3.00 | 0.02 | **+2.98** |
| 🥉 | **AMIYATOSH PWNANANDAM** | 980 | 3.50 | 0.66 | **+2.84** |
| 4️⃣ | **ZACHARY JAMES HOUGHTON** | 1220 | 4.50 | 2.11 | **+2.39** |
| 5️⃣ | **STEFANO LEE** | 1411 | 5.00 | 2.70 | **+2.30** |

### 📉 TOP 5 UNDERPERFORMERS

| Rank | Player | Rating | Actual | Expected | Diff |
|------|--------|--------|--------|----------|------|
| 1️⃣ | **LOREN SCHWIEBERT** | 1745 | 3.50 | 6.01 | **-2.51** |
| 2️⃣ | **GEORGE AVERY JONES** | 1522 | 3.50 | 5.27 | **-1.77** |
| 3️⃣ | **JARED GE** | 1332 | 3.00 | 4.64 | **-1.64** |
| 4️⃣ | **JOSHUA DAVID LEE** | 1438 | 3.50 | 5.09 | **-1.59** |
| 5️⃣ | **CHIEDOZIE OKORIE** | 1602 | 3.50 | 4.73 | **-1.23** |

---

## 🔧 Requirements

### 📦 R Packages
- `readr` - Data import
- `dplyr` - Data manipulation  
- `stringr` - String processing
- `ggplot2` - Visualizations (optional)

### 💾 System Requirements
- R version 4.0+ recommended
- 8MB+ available memory
- CSV file reading capability

---

## 📁 Files

```
📂 Chess-Tournament-Analysis/
├── 📄 chess_elo_analysis.R          # Main analysis script
├── 📊 chess_tournament_results.csv  # Input dataset
├── 📈 chess_performance_analysis.csv # Output results
├── 📖 README.md                     # This file
└── 📋 performance_report.html       # Analysis report
```

---

## 🎨 Visualizations

The analysis includes:

- 📊 **Performance Distribution Histogram** - Shows spread of over/underperformance
- 📈 **Rating vs Performance Scatter Plot** - Reveals rating-performance relationships
- 📋 **Summary Tables** - Detailed player statistics

---

## 🎓 Academic Context

This analysis was conducted as part of a **Masters degree project** investigating:
- ELO rating system accuracy
- Tournament performance prediction
- Statistical analysis of competitive chess
- Rating system evaluation methodologies

---

## 📚 References

1. **United States Chess Federation** - Official Rules of Chess, 7th edition
2. **Elo, Arpad** - The Rating of Chessplayers, Past and Present
3. **FIDE Rating Regulations** - World Chess Federation guidelines

---

## 🤝 Contributing

Contributions welcome! Areas for enhancement:
- Additional rating system comparisons
- Extended statistical analysis
- Interactive visualizations
- Tournament format variations

---

## 📄 License

This project is available under the MIT License. See LICENSE file for details.

---

<div align="center">

**🏁 Analysis Complete | 📊 63 Players Analyzed | ⭐ ELO-Based Methodology**

*Made with ❤️ for chess analytics*

</div>
