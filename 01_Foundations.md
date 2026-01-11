
# 🧠 01 — Foundations (Core Concepts & Career Path)

This chapter builds the mental model of **what AI Engineers actually do**, and the foundational skills that make everything else easier: Python, data handling, SQL, math intuition, and evaluation.

---

## 1.1 What AI Engineering Looks Like (In Real Jobs)

### Typical responsibilities
- Convert raw data → training dataset (cleaning, labeling, feature engineering)
- Train models (classic ML + deep learning)
- Compare models fairly (metrics, baselines, ablations)
- Ship models (API service, batch pipeline, or in‑app inference)
- Monitor performance + retrain when data changes

### AI Engineer vs Data Scientist vs MLOps (Quick Map)
| Role | Core focus | Typical output |
|---|---|---|
| Data Scientist | analysis + experimentation | insights + prototypes |
| AI/ML Engineer | shipping models as features | production services + pipelines |
| MLOps Engineer | reliability + automation | CI/CD, monitoring, infra |

> 💡 In small teams, one person often does all three.

---

## 1.2 Skill Pyramid (What To Learn First)

1. **Python + data handling** (NumPy, pandas)  
2. **SQL** (joins, aggregations, window functions)  
3. **ML fundamentals** (train/test, leakage, metrics)  
4. **Deep learning basics** (PyTorch, GPU mindset)  
5. **Deployment + MLOps basics** (FastAPI, Docker, CI/CD)  
6. **LLM apps** (RAG, vector search, evaluation)

---

## 1.3 Math You Actually Use (Practical Level)

### Linear algebra (minimum)
- vectors, matrices, dot products
- how shape errors happen and how to debug them
- gradients as “direction of steepest improvement”

### Probability & statistics (minimum)
- distributions, mean/variance
- correlation vs causation
- confidence intervals (basic intuition)
- Bayes rule (when thinking about false positives/negatives)

### Calculus (minimum)
- derivatives as “slope”
- gradient descent idea
- chain rule intuition (backprop)

> ✅ **Goal:** Enough intuition to understand why training works and why models fail.

---

## 1.4 Python Foundations (Bootcamp Drills)

### What “good” Python means here
- readable code, small functions
- clear variable names
- unit tests for critical logic
- type hints where it helps

### Essential data structures to master
- list/dict/set
- list/dict comprehensions
- generators (for memory‑safe pipelines)
- `dataclasses` for clean structured data

#### Drill: write these from memory
- parse a CSV into dict records
- group records by a key (like `customer_id`)
- compute aggregate metrics
- write a function + a unit test

> ✅ **Deliverable:** `labs/python_drills.py` with at least 10 exercises completed.

---

## 1.5 SQL Foundations (What Employers Expect)

### Core SQL skills
- `SELECT`, `WHERE`, `GROUP BY`, `HAVING`
- joins: `INNER`, `LEFT`
- window functions: `ROW_NUMBER`, `LAG`, `SUM() OVER (...)`
- performance basics: indexes, reading query plans (high level)

### Practice datasets
- sample ecommerce dataset (orders/customers/products)
- public datasets: NYC taxi, IMDb, etc.

> 🧪 **Lab:** Write 20 queries:
> - 10 beginner (filters + group)
> - 5 intermediate (joins)
> - 5 advanced (window functions)

---

## 1.6 ML Fundamentals You Must Know Cold

### The ML loop
1. define problem and metric  
2. collect/clean data  
3. split data properly  
4. train baseline  
5. improve with features + model choices  
6. evaluate and interpret errors  

### Common failure modes
- **data leakage** (accidentally training on future information)
- **target leakage** (feature that directly encodes the answer)
- **distribution shift** (production data differs from training)
- **overfitting** (great train score, weak real performance)

> ⚠️ If you can’t explain leakage, you’ll struggle in interviews.

---

## 1.7 Evaluation: Metrics + Error Analysis (The “Engineer” Part)

### Classification
- Accuracy (often misleading)
- Precision / Recall
- F1
- ROC‑AUC vs PR‑AUC (imbalanced datasets)

### Regression
- MAE, MSE, RMSE
- R² (use carefully)

### Error analysis routine
- look at worst predictions
- segment results (by category, range, etc.)
- identify systematic failures
- propose fixes (data, features, model, thresholding)

> ✅ **Deliverable:** a short `reports/error_analysis.md` for every major project.

---

## 1.8 Ethics, Bias, and Inclusivity (Required)

AI engineers must think about:
- who the model might harm
- what data is missing
- how the metric hides errors for minority groups
- fairness constraints and documentation

**Practical habit:** Always report metrics **by segment** when possible.

> 📌 Include a “Model Limitations” section in every README.

---

## Labs (Hands‑On)

### Lab A — Linear Regression From Scratch
**Goal:** learn the ML loop + gradient descent intuition.

**Tasks**
- generate synthetic data
- implement linear regression with gradient descent
- compare to scikit‑learn results
- plot loss over epochs

**Deliverables**
- `src/train_from_scratch.py`
- `reports/lab_a_results.md`

### Lab B — SQL + pandas pipeline
- query a dataset (or CSV)
- clean with pandas
- compute summary metrics
- export to `reports/summary.csv`

### Lab C — Baseline model + evaluation
- choose a public dataset
- train a baseline model
- create a confusion matrix
- write “next steps” based on errors

---

## Checkpoint

- [ ] I can describe AI Engineer responsibilities clearly  
- [ ] I can write clean Python functions + tests  
- [ ] I can write joins + window functions in SQL  
- [ ] I can explain leakage, overfitting, and distribution shift  
- [ ] I can perform basic error analysis and propose improvements
