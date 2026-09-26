# Employee Training Effectiveness Dashboard – Power BI

## 📊 Project Overview

This project is an interactive **Power BI dashboard** designed to analyze employee training effectiveness and help understand whether training programs are improving employee performance.

The dashboard focuses on training completion, score improvement, employee satisfaction, training costs, and program performance.

---

## 🎯 Objectives

- Measure the effectiveness of employee training programs.
- Track employee completion and drop-off rates.
- Analyze improvement in scores before and after training.
- Monitor employee satisfaction with training programs.
- Analyze training costs and spending.
- Compare training performance across departments, regions, and programs.
- Provide useful insights for Learning & Development decisions.

---

## 📁 Dataset Overview

The dataset contains **5,000 employee training records** and **10 columns**.

### Dataset Columns

| Column | Description |
|---|---|
| EmployeeID | Unique employee identifier |
| Department | Employee department |
| Region | Employee region |
| TrainingProgram | Training course attended |
| EnrollmentDate | Date of training enrollment |
| CompletionStatus | Completed, In Progress, or Dropped |
| PreTrainingScore | Score before training |
| PostTrainingScore | Score after training |
| TrainingCost_INR | Training cost per employee |
| SatisfactionRating | Employee satisfaction rating from 1–5 |

The dataset covers training activity across **8 departments, 5 regions, and 10 training programs** over the 2024–2025 period.

---

## 🛠️ Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Excel / XLSX
- Data Visualization
- Data Cleaning & Transformation

---

## 🔄 Data Preparation

The data was prepared in Power Query by:

- Importing the training dataset.
- Correcting data types.
- Handling blank values in post-training scores.
- Preparing date and numerical fields.
- Preparing the dataset for Power BI analysis.

---

## 🧮 Calculated Columns

The dashboard uses calculated columns including:

- **Score Improvement**
- **Enrollment Month**
- **Outcome Flag**
- **Cost Bucket**

### Score Improvement

```DAX
Score Improvement =
IF(
    ISBLANK('Training'[PostTrainingScore]),
    BLANK(),
    'Training'[PostTrainingScore] - 'Training'[PreTrainingScore]
)
