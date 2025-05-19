# 🎲 CITS4407 Assignment 2  
## *“Board Games”*  

---

### 📋 Overview
Welcome to the **Board Games Dataset Analysis** project, part of the CITS4407 Open Source Tools and Scripting course.  
This project demonstrates data cleaning, empty cell detection, and exploratory data analysis on board game datasets.

---

### 👤 Author Details  
- **Name:** Raghava Mahidhar Akella 
- **Student ID:** 24654725  
- **Date:** 19 May 2025  
- **Course:** CITS4407 – Open Source Tools and Scripting  

---

### 📂 Project Contents

| Script Name   | Description                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| `empty_cells` | Counts empty cells per column in a delimited file, handling whitespace and non-ASCII chars.  |
| `preprocess`  | Cleans raw `;`-delimited dataset, converts to TSV, fixes line endings, decimals, fills IDs.  |
| `analysis`   | Answers research questions: popular mechanics/domains & Pearson correlations on cleaned data. |
| `README.md`  | This documentation file.                                                                      |

---

### ⚙️ System Requirements & Dependencies  
- Unix-like environment (Linux/macOS/WSL)  
- Bash shell (`/usr/bin/env bash`)  
- Unix tools: `awk`, `sed`, `tr`, `tail`, `head`  
- **No external dependencies or libraries needed!**

---

### 🚀 Quick Start Guide

1. **Make scripts executable:**  
   ```bash
   chmod +x empty_cells preprocess analysis
   ```
2. **Run empty cell counter:**  
   ```bash
   ./empty_cells bgg_dataset.txt ";"
   ```
3. **Preprocess raw data:**  
   ```bash
   ./preprocess bgg_dataset.txt > cleaned_bgg_dataset.tsv
   ```
4. **Analyze cleaned dataset:**  
   ```bash
   ./analysis cleaned_bgg_dataset.tsv
   ```

---

### 🧪 Testing & Edge Cases

#### empty_cells  
- Detects and reports error for empty files  
- Handles header-only files gracefully  
- Counts whitespace-only cells as empty  
- Counts blank lines as empty cells in every column  
- Validates delimiter correctness  
- Removes non-ASCII chars prior to counting  

#### preprocess  
- Fills missing IDs sequentially  
- Maintains commas inside mechanics/domains  
- Normalizes mixed line endings to Unix format  
- Converts comma decimals to dot decimals  
- Changes semicolons to tabs for TSV output  
- Cleanses non-ASCII characters  

#### analysis  
- Skips rows missing mechanics or domains for counts  
- Calculates Pearson correlations for:  
  - Year published vs average rating  
  - Complexity vs average rating  

---
