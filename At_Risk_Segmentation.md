# ⚠️ At-Risk Student Segmentation
**Pluto Academy Data Analytics Internship | Project 02**

---

## Definition

> A student is classified as **at-risk** if they score **below 50 in ANY one subject** (Math, Reading, or Writing).

This threshold was chosen because a score below 50 in any subject indicates the student is likely to fail that subject if not given additional support. It provides an early warning system before the student reaches critical failure.

---

## Overall At-Risk Summary

| | Count | Percentage |
|---|---|---|
| **Total Students** | 1,000 | 100% |
| **At-Risk Students** | **188** | **18.8%** |
| Safe Students | 812 | 81.2% |

**188 out of every 1,000 students are currently at academic risk.**

---

## Breakdown by Parental Education

| Parental Education | At-Risk | Total | At-Risk % | Risk Level |
|---|---|---|---|---|
| some high school | 46 | 179 | **25.7%** | 🔴 High |
| high school | 49 | 196 | **25.0%** | 🔴 High |
| some college | 38 | 226 | 16.8% | 🟠 Medium |
| associate's degree | 33 | 222 | 14.9% | 🟠 Medium |
| bachelor's degree | 16 | 118 | 13.6% | 🟢 Low |
| master's degree | 6 | 59 | **10.2%** | 🟢 Low |

**Key Insight:** Students whose parents have only completed high school or some high school have more than **2.5× the at-risk rate** of students whose parents hold a master's degree (25% vs 10.2%). This gap reflects the reduced home academic support available to students from lower parental education backgrounds.

---

## Breakdown by Gender

| Gender | At-Risk | Total | At-Risk % |
|---|---|---|---|
| Male | 99 | 482 | **20.5%** |
| Female | 89 | 518 | 17.2% |

Male students are **1.2× more likely** to be at-risk than female students, driven primarily by their significantly lower Reading (−7.1 pts) and Writing (−9.2 pts) average scores compared to females.

---

## Breakdown by Test Prep Completion

| Test Prep | At-Risk | Total | At-Risk % |
|---|---|---|---|
| None | 152 | 642 | **23.7%** |
| Completed | 36 | 358 | **10.1%** |

This is the most actionable finding in the segmentation. Completing test prep **more than halves** the probability of being at-risk — from 23.7% to 10.1%. Of the 188 at-risk students, **152 (80.9%)** did not complete test prep.

---

## Breakdown by Lunch Type (Socioeconomic Indicator)

| Lunch Type | At-Risk | Total | At-Risk % |
|---|---|---|---|
| Free / Reduced | 111 | 355 | **31.3%** |
| Standard | 77 | 645 | **11.9%** |

Students on free/reduced lunch are **2.6× more likely** to be at-risk. This is the strongest single predictor of at-risk status in the entire dataset — stronger than gender, parental education, or test prep completion. Free/reduced lunch status serves as a proxy for socioeconomic disadvantage, which reduces access to academic resources, tutoring, and a stable home study environment.

---

## Why These Groups Are At Higher Risk

| Risk Factor | Root Cause | Evidence |
|---|---|---|
| Low parental education | Less academic support at home | 25.7% at-risk vs 10.2% |
| No test prep | Missing structured exam preparation | 23.7% at-risk vs 10.1% |
| Free/reduced lunch | Socioeconomic disadvantage | 31.3% at-risk vs 11.9% |
| Male gender | Verbal subject underperformance | 20.5% at-risk vs 17.2% |

---

## Recommendation

Immediately identify all **188 at-risk students** and cross-reference against these four risk factors. Students who fall into **two or more high-risk categories** (e.g. free/reduced lunch + no test prep + low parental education) should be considered **critical priority** for the intervention program and assigned mentors in the first week of the next term.

---

*Pluto Academy Data Analytics Internship 2026 · plutoacademy.in*
