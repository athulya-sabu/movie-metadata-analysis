# 🎬 Movie Metadata Analysis

## 📌 Project Overview
This project analyzes a **movie metadata dataset** to uncover insights into genres, budgets, revenues, IMDb ratings, and other attributes.  
The goal is to identify factors that influence a movie’s success and highlight trends across **decades, directors, and countries**.

---

## 🛠 Tools Used
- **Microsoft Excel** → Initial cleaning & preprocessing  
- **Microsoft Power BI** → Data modeling, dashboards & visualization  

---

## 🎯 Dataset
**Source:** Sample Movie Metadata  

**Key Columns:**
- 🎥 `movie_title` – Name of the movie  
- 🎬 `director_name` – Director of the movie  
- 🏷️ `genres` – Genre(s) of the movie  
- 💰 `budget` – Production budget (USD)  
- 🌍 `gross` – Worldwide gross revenue (USD)  
- ⭐ `imdb_score` – IMDb rating (1–10 scale)  
- 📅 `year` – Release year  
- 🗣️ `language` – Language of the movie  
- 🇨🇺 `country` – Country of production  
- ⏱️ `duration` – Duration in minutes  
- 🔖 `rating` – MPAA rating (PG, R, etc.)  

---

## 🔄 Workflow

### 1. Data Collection & Import
- Imported raw movie dataset into Power BI.

### 2. Data Cleaning & Transformation (Power Query)
- Removed nulls, duplicates & irrelevant columns  
- Standardized text fields (e.g., trimmed spaces, split multiple genres)  
- Converted data types (`budget/gross` → numeric, `year` → date hierarchy)  
- Built a **MovieGenres bridge table** for multi-genre handling  

### 3. Data Modeling (Star Schema)
- **Fact Table:** Movies (budget, gross, IMDb, duration, etc.)  
- **Dimension Tables:** Genres, Directors, Countries, Languages, Dates  
- **Relationships:**
  - Movies → MovieGenres → Genres  
  - Movies → Directors  
  - Movies → Countries  
  - Movies → Languages  
  - Movies[Year] → Date[Year]  

### 4. Measures & KPIs (DAX)
- **Profit** = Gross – Budget  
- **ROI** = (Profit / Budget) × 100  
- Average Duration & IMDb Rating  
- Profitability grouped by Budget Categories (Low, Medium, High)  

### 5. Visualization & Dashboards
- 📊 Profitability by budget, ROI, IMDb score trends  
- 🎭 Genre analysis (profitability, ROI, frequency)  
- ⏳ Duration analysis across decades  
- 🌍 Country-wise production & ROI  
- 👨‍💼 Director analysis (top directors & IMDb scores)  
- 🧾 KPI cards for Total Profit, Avg ROI, Top Genre, Top Director  

---

## 🔑 Key Insights

### 🎥 Movie Trends & Ratings
- Movie releases grew rapidly after the 1970s, peaking ~2010  
- Most movies are rated **R (39.9%)**, followed by PG-13 (28.9%)  
- English dominates (~13k movies), other languages have low representation  

### 👨‍💼 Directors & Production
- **Spielberg, Eastwood, Scorsese** = most prolific directors  
- High IMDb averages: **John Blanchard (9.5)**, **Sadyk Sher-Niyaz (8.7)**  

### 💰 Budget, Duration & Profitability
- **Low & Medium budgets** far more profitable than High budgets  
- Standard-duration movies = most common (~80%)  
- High-budget standard-duration = **biggest losses (~ -83B total)**  

### 🎟️ Box Office Performance
- Top-grossing: **Lion King (1994), Avatar (2009), Jurassic World (2015)**  
- ROI varies widely → *Inside Out (103%)* vs *Lion King (839%)*  

### ⭐ IMDb & Audience Ratings
- Average IMDb = **6.45**  
- Most films cluster between **5–7** rating  
- Quality trend has declined → Avg IMDb dropped from **8.0 (1930s)** to **6.3 (2010s)**  

### 🎭 Genre Analysis
- **Comedy, Adventure, Thriller, Family** = most profitable  
- ROI leaders: **Game-Show (1516%)**, **Film-Noir (410%)**  

### 🌍 Country & ROI
- USA dominates production volume  
- Smaller industries outperform in ROI → **Kenya (323%)**, **UAE (39%)**  

---


