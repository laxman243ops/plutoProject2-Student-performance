# 📄 Principal's Report — Student Performance Analysis
**Pluto Academy Data Analytics Internship | Project 02**
**Prepared by:** [Your Name], Data Analyst
**Prepared for:** School Principal
**Dataset:** 1,000 student records — Students Performance in Exams (Kaggle)

---

## Executive Summary

This report analyses performance data for **1,000 students** across Math, Reading, and Writing examinations. Students whose parents hold higher educational qualifications consistently score better across all subjects, with a 6.2-point Math gap between the lowest and highest parental education levels. Test preparation completion reduces student at-risk rates from **23.7% to 10.1%** — representing the most actionable and high-impact single intervention available to the school in the next academic year.

---

## 5 Key Findings

**Finding 1 — Test Prep Has a Proven, Measurable Impact**

Students who completed the test preparation course scored:
- **+5.6 points** higher in Math
- **+7.4 points** higher in Reading
- **+9.9 points** higher in Writing

Only **358 out of 1,000 students (35.8%)** completed the course — leaving 64.2% of the student body without access to a proven academic advantage.

---

**Finding 2 — Parental Education Consistently Predicts Academic Performance**

| Parental Education | Math | Reading | Writing |
|---|---|---|---|
| some high school | 63.5 | 66.9 | 64.9 |
| high school | 62.1 | 64.7 | 62.4 |
| some college | 67.1 | 69.5 | 68.8 |
| associate's degree | 67.9 | 70.9 | 69.9 |
| bachelor's degree | 69.4 | 73.0 | 73.4 |
| master's degree | 69.7 | 75.4 | 75.7 |

Writing shows the sharpest gap: 62.4 (high school) vs 75.7 (master's degree) — **a 13.3-point difference**. Students from lower parental education backgrounds likely have less academic support at home, not less ability.

---

**Finding 3 — Reading and Writing Skills Are Inseparably Linked (r = 0.955)**

The Pearson correlation between reading and writing scores is **0.955** — near-perfect. A student who struggles in reading will almost certainly struggle in writing too. This allows the school to intervene on both skills simultaneously with a single combined literacy program, maximising efficiency of resources.

---

**Finding 4 — Male Students Underperform in Verbal Subjects**

| Subject | Female Avg | Male Avg | Gap |
|---|---|---|---|
| Math | 63.6 | 68.7 | Male +5.1 |
| Reading | 72.6 | 65.5 | Female +7.1 |
| Writing | 72.5 | 63.3 | Female +9.2 |

Male students lead in Math but fall significantly behind in Reading and Writing — the subjects that most affect overall academic standing and at-risk classification. Male at-risk rate: **20.5%** vs female: **17.2%**.

---

**Finding 5 — Socioeconomic Status is the Strongest At-Risk Predictor**

| Lunch Type | At-Risk Students | Total | At-Risk % |
|---|---|---|---|
| Free / Reduced | 111 | 355 | **31.3%** |
| Standard | 77 | 645 | **11.9%** |

Students on free/reduced lunch are **2.6× more likely** to be at-risk than students on standard lunch. This is the single strongest group-level predictor of academic risk in the dataset — surpassing gender, parental education, and test prep status.

---

## 3 Actionable Recommendations

### Recommendation 1 — Make Test Prep Mandatory for All Students

**The problem:** Only 35.8% of students complete test prep. At-risk rate without test prep: 23.7%. With test prep: 10.1% — a reduction of more than half.

**The action:** Make test preparation compulsory for all enrolled students from next academic year. Offer after-school, weekend, and online sessions to ensure no student misses it due to scheduling conflicts. Track completion rates each term as a key school performance metric alongside exam results.

**Expected impact:** If the remaining 642 students who currently skip test prep all complete it, the school could reduce at-risk students from 188 to approximately 100 — a potential reduction of ~47%.

---

### Recommendation 2 — Launch a Targeted At-Risk Intervention Program

**The problem:** 188 students (18.8%) are currently scoring below 50 in at least one subject. The highest-risk groups are students from 'some high school' parental backgrounds (25.7% at-risk) and students on free/reduced lunch (31.3% at-risk).

**The action:** Identify all 188 at-risk students by name immediately. Assign each one a dedicated faculty mentor. Implement bi-weekly academic check-ins, provide subject-specific support materials, and run a progress tracking dashboard for school leadership. Prioritise outreach to students from the highest-risk demographic groups.

**Expected impact:** Early identification and personalised mentoring has been shown in educational research to reduce dropout risk by 30–40%. Addressing this in the next term prevents these 188 students from falling further behind.

---

### Recommendation 3 — Introduce a Structured Reading & Writing Program for Male Students

**The problem:** Male students score 7.1 points lower in Reading and 9.2 points lower in Writing than female students. Male at-risk rate (20.5%) exceeds female (17.2%). This gap is systemic, not individual.

**The action:** Launch a structured reading enrichment program targeting male students — including book clubs, paired reading sessions, and weekly writing workshops. Integrate these into the regular school schedule rather than as optional extras. Track progress against the current gender baseline each term.

**Expected impact:** Closing even half the reading gap (+3.5 points) would meaningfully reduce male at-risk rates and improve overall school average scores in verbal subjects.

---

## Most Impactful Recommendation

**Recommendation 2 — At-Risk Intervention Program** is the most immediately impactful because it addresses students already at academic risk, right now. While Recommendations 1 and 3 are preventative for future cohorts, Recommendation 2 is corrective and urgent. The data clearly identifies which groups face the highest risk — students from low parental education backgrounds (25.7%) and free/reduced lunch households (31.3%). Assigning mentors and providing structured support to these 188 students has the highest potential return on educational investment, with direct, measurable impact on individual student outcomes in the current academic year.

---

*Pluto Academy Data Analytics Internship 2026 · plutoacademy.in*
