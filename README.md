# CTD Python 100 — Code the Dream

**Course:** Python 100 for Data Engineering — Code the Dream (Cohort: Jamaican Boa)
**Status:** ✅ Completed — Week 15 of 15 (Jun 18–24, 2025)

---

## About This Course

Despite the "100" designation, this is a rigorous, advanced Python curriculum spanning **15 weeks** of applied data engineering, analysis, and software development. The course covers the full stack from core Python fundamentals through production-grade data pipelines, SQL databases, web scraping, interactive dashboards, and machine learning capstones — comparable in depth to a graduate-level applied computing course.

**Core Tech Stack:**
`Python 3` · `Pandas` · `NumPy` · `SQLite / sqlite3` · `Matplotlib` · `Seaborn` · `Plotly` · `Dash` · `Streamlit` · `Selenium` · `WebDriver Manager` · `PyTest` · `CSV / JSON` · `Git`

---

## Curriculum Overview

| Week | Topic | Key Skills |
|------|-------|------------|
| 1 | Introduction to Python | Variables, data types, operators, control flow, functions, `*args`/`**kwargs`, error handling with `try/except`, basic debugging with `logging` |
| 2 | Data Structures & File Handling | Lists, tuples, dicts, sets, CSV/text file I/O, `os` module, virtual environments, `map()`, lambdas, `datetime` |
| 3 | Advanced Python | OOP (classes, inheritance, `@property`, `@classmethod`, `@dataclass`), decorators, list comprehensions, generator expressions, closures, `nonlocal` |
| 4 | Intro to Data Engineering | Pandas `Series` and `DataFrame`, loading from CSV/JSON/dict/NumPy, `.loc`/`.iloc`, data cleaning (`fillna`, `dropna`, `to_datetime`, `astype`), `to_csv` |
| 5 | Data Wrangling & Aggregation | `groupby()`, `agg()`, `merge()`, `join()`, `concat()`, column transformations with operators/`map()`/NumPy, `rename`, `sort_values`, `reset_index` |
| 6 | Data Cleaning & Validation I | Pivot tables, `apply()` with `axis=1`, handling missing values, outliers, `drop_duplicates()`, `pd.cut()`, feature engineering, data discretization |
| 7 | Data Cleaning & Validation II | Regular expressions (`re`, `str.replace()`, `str.extract()`, `str.contains()`, `filter()`), label encoding, one-hot encoding (`get_dummies()`), fuzzy matching (`thefuzz`) |
| 8 | Databases & SQL | SQLite schema design (`CREATE TABLE`, primary/foreign keys, constraints), `INSERT`, `SELECT`, `JOIN`, `UPDATE`, `DELETE`, transactions, parameterized queries, `pd.read_sql_query()` |
| 9 | Advanced SQL | Subqueries, complex multi-table `JOIN`s, `GROUP BY`, `HAVING`, aggregation functions (`MIN/MAX/AVG/COUNT`), window functions (`RANK`, `ROW_NUMBER`), `JULIANDAY`, indexing for performance |
| 10 | Web Scraping | Selenium + WebDriver Manager, DOM traversal, CSS selectors, XPath axes (`..`, `following-sibling`), ethical scraping / `robots.txt`, managing requests with `sleep()`, saving to CSV/JSON |
| 11 | Data Visualization I | Matplotlib (line, bar, histogram), Seaborn (heatmaps, pair plots), correlation matrices, `np.random.randn`, customizing axes/titles/legends/color palettes |
| 12 | Data Visualization II | Plotly interactive scatter/line charts, Dash dashboards (`html`, `dcc`, `@app.callback`, `Input`/`Output`), Pandas `DataFrame.plot()`, Streamlit (`st.title`, `st.metric`, `st.plotly_chart`), deploy to Render.com |
| 13 | Kaggle Capstone I | End-to-end data pipeline in Kaggle Notebooks: feature engineering, aggregation, 3+ visualizations, markdown documentation of cleaning and insights |
| 14 | Web Scraping + Dashboard Capstone | Selenium scraping pipeline, CSV → SQLite import, CLI query tool with JOINs, Dash/Streamlit interactive dashboard deployed publicly |
| 15 | Project Completion & Presentations | Final project polish, recorded demo presentation, peer gallery review |

---

## Repository Structure

```
ctd-python-101/
├── assignments/
│   ├── assignment1/        # Python operators, control flow, Pig Latin, Hangman, calculator (PyTest)
│   ├── assignment2/        # File I/O, CSV handling, dicts, sets, os module, datetime, custom modules
│   └── assignment3/        # Decorators, list comprehensions, closures, OOP, Tic-Tac-Toe
├── database-work/
│   ├── sqlcommand.py       # Interactive CLI for SQL queries against lesson.db
│   ├── load_db.py          # Populates lesson.db from CSV (employees, customers, orders, products)
│   ├── create_lesson_db.py # Schema + seed data scripts
│   ├── employee_results.py # SQL → Pandas: revenue per employee via multi-table JOIN
│   ├── cumulative.py       # Cumulative revenue line chart from SQL data
│   ├── myapp.py            # Dash app: GDP per capita dashboard (gapminder, deployed Render.com)
│   └── wind.py             # Plotly interactive scatter: wind strength vs frequency by direction
├── streamlit-projects/
│   ├── app.py              # Streamlit component explorer (text, inputs, layout, sidebar)
│   ├── dashboard_app.py    # Streamlit product dashboard with Plotly bar chart + metrics
│   └── streamlit_app.py    # Full Streamlit deployment-ready app
├── ames-housing-price-prediction/
│   ├── code/               # Notebooks: data reprocessing, model tuning, Kaggle submissions
│   ├── data/               # Train/test CSVs + cleaned datasets
│   └── images/             # Feature heatmaps, regression plots, distribution charts
├── baseball-capstone/      # ← Final Capstone (see below)
│   ├── 1.Web_Scraping/     # Selenium scraper: National League historical stats
│   ├── 2.National_League/  # Raw scraped CSV output
│   ├── 3.National_League_Cleaned/ # Cleaned datasets post-processing
│   ├── 3.1.Parsing/        # Parsing and reshaping raw scrape output
│   ├── 4.Further_clean_and_EDA/   # EDA notebooks: distributions, correlations, outliers
│   ├── 5.Streamlit/        # Interactive Streamlit dashboard (deployed, presented to peers)
│   ├── create_nl_db.py     # Imports CSVs into SQLite with schema and FK constraints
│   └── README.md           # Capstone-specific documentation
└── requirements.txt
```

---

## Baseball Capstone — Final Project

The capstone demonstrates a **production-style end-to-end data engineering pipeline** applied to Major League Baseball history.

**Pipeline stages:**
1. **Web Scraping** — Selenium + WebDriver Manager scrapes historical National League statistics year-by-year, handling pagination, missing tags, and dynamic page content
2. **Parsing & Cleaning** — Raw HTML-extracted data parsed, reshaped, and cleaned using Pandas: type conversion, deduplication, null handling, outlier detection, and string standardization
3. **EDA** — Exploratory analysis with Matplotlib/Seaborn: distributions, correlation heatmaps, player/team trend analysis across eras
4. **Database** — Cleaned CSVs imported into SQLite via `create_nl_db.py` with proper schema, primary/foreign key constraints, and JOIN-ready table relationships
5. **Dashboard** — Interactive Streamlit app (`5.Streamlit/`) with dynamic charts, dropdown filters, heatmaps, and player/team performance comparisons across seasons

**Presented live to peers via Streamlit on Jun 18–24, 2025.**

---

## Note on Course Depth

Python 100 is the foundational tier in Code the Dream's curriculum, but "foundational" refers to prerequisites — not complexity. The course progresses from Python syntax to regex, OOP, SQL window functions, Selenium scraping, Plotly dashboards, and a multi-stage ML capstone over 15 weeks of weekly graded assignments. All assignments were submitted via GitHub pull requests with code review, mirroring industry development workflows.
