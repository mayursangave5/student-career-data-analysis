# Student Placement & Career Success — Data Cleaning

This is Task 1 of my Data Analytics internship at ApexPlanet Software Pvt. Ltd.
The goal was to explore, clean, and prepare a student placement dataset for further analysis.

---

## About the Dataset

The dataset contains information about 25,000 students including their academic performance,
skills, lifestyle habits, and placement outcomes.

- **Rows:** 25,000
- **Columns:** 44
- **Source:** Provided by ApexPlanet as part of the internship program

---

## What I Did

### 1. Explored the Data
- Loaded the CSV file using pandas
- Checked the shape, column names, and data types
- Identified missing values and duplicate rows

### 2. Found These Issues
| Column | Issue | Count |
|--------|-------|-------|
| GitHub_repos | Missing values | 500 |
| mock_interview_score | Missing values | 500 |
| sleep_hours | Missing values | 500 |
| company_type | Missing values | 404 |
| work_mode | Missing values | 404 |
| Duplicates | None found | 0 |

### 3. Cleaned the Data
- Filled missing numeric values using **median** (less affected by outliers)
- Filled missing text values using **mode** (most frequent value)
- Dropped duplicate rows (none were found)

### 4. Feature Engineering
Created a new column called `overall_skill_score` by combining:
- DSA problems solved (30% weight)
- Resume score (20% weight)
- Communication skills (20% weight)
- Aptitude score (20% weight)
- Mock interview score (10% weight)

This gives a single score that represents a student's overall readiness for placement.

---

## Files in This Repo

```
├── data/
│   ├── row data/
│   │   └── student_placement_career_success_dataset.csv   # original dataset
│   └── cleaned_dataset.csv                                # cleaned output
│
├── scripts/
│   └── data_cleaning.py     # main cleaning script
│
├── data_dictionary.csv      # description of all 44 columns
└── README.md                # this file
```

---

## How to Run

1. Clone this repository
```
git clone https://github.com/mayursangave5/student-career-data-analysis/tree/main
```

2. Install required library
```
pip install pandas
```

3. Run the script
```
cd scripts
python data_cleaning.py
```

4. The cleaned file will be saved as `cleaned_dataset.csv`

---

## Tools Used

- Python 3
- Pandas
- Jupyter Notebook (for exploration)

---

## Key Learnings

- Real datasets always have missing values — handling them correctly matters
- Median is better than mean for filling numeric missing values when outliers are present
- Feature engineering helps create more meaningful columns from existing data

---

## Internship Details

- **Company:** ApexPlanet Software Pvt. Ltd.
- **Program:** Data Analytics Internship
- **Task:** Task 1 — Data Immersion & Wrangling
- **Website:** www.apexplanet.in
