# 🎓 Project 02 — Student Performance Analysis
**Pluto Academy Data Analytics Internship**

---

## 👤 Intern Details

| Field | Details |
|---|---|
| **Name** | Butcha Laxmana Rao |
| **Program** | Pluto Academy — Data Analytics Internship |
| **Project** | Project 02 — Student Performance EDA & Reporting |
| **Dataset** | Students Performance in Exams (Kaggle) |
| **Tools** | Python · Pandas · Matplotlib · Seaborn |

---

## 📊 Dataset

**Source:** [Students Performance in Exams — Kaggle](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)

File used: `StudentsPerformance.csv`

| Property | Value |
|---|---|
| Rows | 1,000 |
| Columns | 8 |
| Missing Values | 0 |
| Duplicates | 0 |

---

## 🧹 Data Exploration & Cleaning

**5-Line Dataset Summary:**

1. **Total students:** 1,000
2. **Gender split:** Female 518 · Male 482
3. **Average scores:** Math 66.1 · Reading 69.2 · Writing 68.1
4. **Parental education levels:** 6 unique categories
5. **Test prep completion:** Completed 358 · None 642

**Cleaning steps performed:**
- Renamed columns for clarity (removed spaces, standardised format)
- Added derived columns: `total_score` and `average_score`
- Confirmed zero null values — no imputation required
- Confirmed zero duplicate rows — no removal needed
- Reordered parental education levels from lowest to highest for analysis

---

## 📈 KPI Summary

| KPI | Value |
|---|---|
| 👨‍🎓 Total Students | **1,000** |
| 📐 Avg Math Score | **66.1 / 100** |
| 📖 Avg Reading Score | **69.2 / 100** |
| ✍️ Avg Writing Score | **68.1 / 100** |
| 📊 Avg Total Score | **203.3 / 300** |
| ⚠️ At-Risk Students | **188 (18.8%)** |
| 🏆 High Performers (250+) | **139 students** |
| 📉 Low Scorers (below 150) | **103 students** |

---

## 🔍 Factor Analysis — 5 Questions Answered

**Q1. Does parental education level affect scores?**

Yes — significantly. Students' math scores improve consistently with higher parental education:

| Parental Education | Math | Reading | Writing | Count |
|---|---|---|---|---|
| some high school | 63.5 | 66.9 | 64.9 | 179 |
| high school | 62.1 | 64.7 | 62.4 | 196 |
| some college | 67.1 | 69.5 | 68.8 | 226 |
| associate's degree | 67.9 | 70.9 | 69.9 | 222 |
| bachelor's degree | 69.4 | 73.0 | 73.4 | 118 |
| master's degree | 69.7 | 75.4 | 75.7 | 59 |

**Math score gap (some high school → master's): +6.2 points**

---

**Q2. Do students who complete test prep score higher?**

Yes — across all three subjects:

| Test Prep | Math | Reading | Writing | Students |
|---|---|---|---|---|
| Completed | 69.7 | 73.9 | 74.4 | 358 |
| None | 64.1 | 66.5 | 64.5 | 642 |

**Improvement from test prep: +5.6 Math · +7.4 Reading · +9.9 Writing points**

---

**Q3. What is the correlation between reading, writing, and math scores?**

| | Math | Reading | Writing |
|---|---|---|---|
| Math | 1.000 | 0.818 | 0.803 |
| Reading | 0.818 | 1.000 | 0.955 |
| Writing | 0.803 | 0.955 | 1.000 |

- **Reading ↔ Writing: 0.955** (very strong — near-perfect)
- **Math ↔ Reading: 0.818** (strong)
- **Math ↔ Writing: 0.803** (strong)

Students who excel in one subject tend to perform well across all three.

---

**Q4. Which gender performs better in which subject?**

| Gender | Math | Reading | Writing | Count |
|---|---|---|---|---|
| Female | 63.6 | 72.6 | 72.5 | 518 |
| Male | 68.7 | 65.5 | 63.3 | 482 |

- **Math:** Male leads by +5.1 points
- **Reading:** Female leads by +7.1 points
- **Writing:** Female leads by +9.2 points

---

**Q5. What is the distribution of total scores?**

| Statistic | Value |
|---|---|
| Mean | 203.3 |
| Median | 205.0 |
| Std Dev | 42.8 |
| Min | 27 |
| Max | 300 |
| 25th Percentile | 175 |
| 75th Percentile | 233 |
| High performers (250+) | 139 students |
| Low scorers (below 150) | 103 students |

---

## 📉 Visualisations

| # | Chart Type | What It Shows |
|---|---|---|
| Chart 1 | Box Plot (3 panels) | Score distribution by parental education level |
| Chart 2 | Grouped Bar | Test prep completed vs not — Math, Reading, Writing |
| Chart 3 | Correlation Heatmap | Pearson r between all 3 subjects |
| Chart 4 | Grouped Bar | Gender vs subject performance comparison |
| Chart 5 | Histogram | Total score distribution with mean, median, at-risk line |
| Chart 6 | Scatter Plot | Reading vs Math scores coloured by gender + trend line |
| At-Risk | Bar Chart | At-risk % by parental education level |

All charts include titles, axis labels, and legends.

---

## ⚠️ At-Risk Student Segmentation

**Definition:** A student is classified as **at-risk** if they score **below 50 in any one subject**.

| Group | At-Risk Count | Total | At-Risk % |
|---|---|---|---|
| **Overall** | **188** | **1,000** | **18.8%** |

**By Parental Education:**

| Parental Education | At-Risk | Total | At-Risk % |
|---|---|---|---|
| some high school | 46 | 179 | **25.7%** 🔴 |
| high school | 49 | 196 | **25.0%** 🔴 |
| some college | 38 | 226 | 16.8% 🟠 |
| associate's degree | 33 | 222 | 14.9% 🟠 |
| bachelor's degree | 16 | 118 | 13.6% 🟢 |
| master's degree | 6 | 59 | **10.2%** 🟢 |

**By Gender:**

| Gender | At-Risk | Total | At-Risk % |
|---|---|---|---|
| Male | 99 | 482 | 20.5% |
| Female | 89 | 518 | 17.2% |

**By Test Prep:**

| Test Prep | At-Risk | Total | At-Risk % |
|---|---|---|---|
| None | 152 | 642 | **23.7%** |
| Completed | 36 | 358 | **10.1%** |

**By Lunch (Socioeconomic Indicator):**

| Lunch Type | At-Risk | Total | At-Risk % |
|---|---|---|---|
| Free/Reduced | 111 | 355 | **31.3%** |
| Standard | 77 | 645 | **11.9%** |

**Key Finding:** Students on free/reduced lunch are 2.6× more likely to be at-risk than those on standard lunch — the strongest single predictor of academic risk in this dataset.

---

## 📄 Principal's Report

### Executive Summary

This report analyses performance data for 1,000 students across Math, Reading, and Writing exams. Students whose parents hold higher qualifications consistently score better across all subjects, with a 6.2-point Math gap between the lowest and highest education levels. Test preparation completion reduces at-risk rates from 23.7% to 10.1% — the most actionable single intervention available to the school.

### 5 Key Findings

**Finding 1 — Test Prep Works (+5.6 to +9.9 Points Across Subjects)**
Students who completed the test preparation course scored 5.6 points higher in Math, 7.4 points higher in Reading, and 9.9 points higher in Writing than those who did not. Only 358 of 1,000 students (35.8%) completed the course — leaving 64.2% without a proven academic advantage.

**Finding 2 — Parental Education is a Consistent Predictor**
Math scores rise steadily from 62.1 (high school parents) to 69.7 (master's degree parents). Writing shows the sharpest gap: 62.4 vs 75.7 — a 13.3-point difference. Students from lower parental education backgrounds are not less capable, but they likely have less academic support at home.

**Finding 3 — Reading and Writing are Inseparably Linked (r = 0.955)**
Reading and writing scores are almost perfectly correlated. A student who struggles in one verbal subject will almost certainly struggle in both. This allows the school to identify and intervene on both issues simultaneously with a single reading/writing support program.

**Finding 4 — Male Students are Disproportionately At-Risk**
Male students have a 20.5% at-risk rate vs 17.2% for females. Males lead in Math (+5.1 pts) but fall significantly behind in Reading (−7.1 pts) and Writing (−9.2 pts) — subjects that contribute to overall academic standing and risk classification.

**Finding 5 — Socioeconomic Status is the Strongest At-Risk Predictor**
Students on free/reduced lunch have a 31.3% at-risk rate — 2.6× higher than students on standard lunch (11.9%). This is the single strongest group-level predictor of academic risk in the dataset, surpassing gender, parental education, and test prep completion.

### 3 Actionable Recommendations

**Recommendation 1 — Make Test Prep Mandatory for All Students**
Test prep reduces at-risk rates from 23.7% to 10.1% — more than halving academic risk. Currently only 358/1,000 students complete it. The school should make test preparation compulsory for all students, offer after-school sessions for those who miss classes, and track completion rates each term as a key performance metric.

**Recommendation 2 — Launch a Targeted At-Risk Intervention Program**
All 188 at-risk students should be identified immediately and assigned a faculty mentor. Bi-weekly academic check-ins, subject-specific support materials, and progress tracking should be introduced. Priority should be given to students with parents from 'some high school' or 'high school' backgrounds (25.7% and 25.0% at-risk rates), and to those on free/reduced lunch (31.3% at-risk rate).

**Recommendation 3 — Introduce Reading & Writing Support for Male Students**
The 7.1-point reading gap and 9.2-point writing gap between male and female students signals a systemic issue, not individual underperformance. The school should launch a structured reading enrichment program — book clubs, paired reading, writing workshops — specifically targeting male students in Grades where this gap first emerges. Progress should be tracked against the current gender baseline.

---

## 🔍 Most Impactful Recommendation

Recommendation 2 — the At-Risk Intervention Program — is the most impactful because it directly addresses the 188 students already at academic risk right now. While Recommendations 1 and 3 are preventative, this one is corrective and urgent. The data shows that without intervention, students from lower parental education backgrounds and free/reduced lunch households face dramatically higher failure rates. Identifying them by name, assigning mentors, and providing structured support has the highest potential return on educational investment — and the longest-lasting impact on individual student outcomes.

---

## 🚀 How to Run

```bash
pip install pandas matplotlib seaborn numpy
python project02_student.py
```

Or open in [Google Colab](https://colab.research.google.com) — the script includes an automatic file upload prompt.

---

## 📁 Output Files Generated

```
project02_outputs/
├── chart1_parental_education_boxplot.png
├── chart2_test_prep_comparison.png
├── chart3_correlation_heatmap.png
├── chart4_gender_subject.png
├── chart5_total_score_histogram.png
├── chart6_scatter_reading_math.png
└── at_risk_segmentation.png
```
<img width="1166" height="473" alt="image" src="https://github.com/user-attachments/assets/6ff0c894-57bf-495b-9a28-42723011c320" />
<img width="1307" height="707" alt="image" src="https://github.com/user-attachments/assets/e328a7e3-21b4-4b2b-a413-86ebf4a771f4" />
<img width="821" height="669" alt="image" src="https://github.com/user-attachments/assets/d39f5433-f92e-45f2-8ea9-6149e06d6c20" />
<img width="1188" height="707" alt="image" src="https://github.com/user-attachments/assets/7ade2874-4202-460a-b24c-03f133eee5f1" />
<img width="1427" height="707" alt="image" src="https://github.com/user-attachments/assets/2c488971-97bd-4507-8edc-0b1e6b62da62" />
<img width="1067" height="827" alt="image" src="https://github.com/user-attachments/assets/8e920f17-b941-4e3a-adbc-4246616330ef" />

---

*Pluto Academy Data Analytics Internship 2026 · plutoacademy.in*
