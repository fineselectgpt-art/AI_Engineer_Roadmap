
# 🚀 00 — Getting Started (Bootcamp Workflow)

This chapter is your “how to learn like an engineer” setup: environment, workflow, and the habits that make you fast and consistent.

---

## 0.1 Your North Star

An AI Engineer is expected to:
- turn messy data into usable training sets
- train models and **prove** they work (metrics + error analysis)
- ship the model as a product feature (API, pipeline, deployment)
- monitor performance + iterate

> ✅ **Outcome mindset:** “I can deliver an ML/AI feature end‑to‑end, reliably.”

---

## 0.2 What To Install

### Required
- **Python 3.10+** (recommend 3.11)
- **Git**
- **VS Code** (or equivalent)
- **Docker Desktop**
- **A browser + a GitHub account**

### Recommended
- **PostgreSQL** (local DB practice)
- **Make** (or just use scripts)
- **Pre‑commit hooks** (keeps code clean)

---

## 0.3 Repo Structure (Use This For Every Project)

```
project/
  data/                 # small samples only; big files ignored
  notebooks/            # exploration + EDA
  src/
    __init__.py
    data.py             # load/clean/feature
    train.py            # training entrypoint
    evaluate.py         # metrics + error analysis
    serve.py            # FastAPI app
  tests/
  artifacts/            # models, reports (gitignored)
  README.md
  requirements.txt
  pyproject.toml (optional)
  .gitignore
```

> ⚠️ **Important:** Don’t commit large datasets. Use links + scripts to fetch them.

---

## 0.4 Daily Study Loop (Bootcamp Pattern)

### 60–90 minutes (minimum day)
1. **Learn** (20–30m): read or watch a focused section  
2. **Build** (30–45m): implement the smallest version of it  
3. **Reflect** (5–10m): write what you learned + what you’ll do next  

### Weekly cadence
- **Mon–Thu:** build + progress
- **Fri:** cleanup + README + tests
- **Sat:** demo + publish + review
- **Sun:** rest or light review

---

## 0.5 How You’ll Track Progress

Create a `learning-log.md` (template in `extras/`) and update it **daily**:

- What did I build today?
- What confused me?
- What will I do tomorrow?
- What result/metric improved?

> ✅ **Deliverable:** 5 logs/week (short is fine). Consistency beats perfection.

---

## 0.6 Quality Bar (Non‑Negotiables)

For every project you ship:
- `README.md` explains **problem, data, approach, results, demo**
- at least **one test** for each important function
- `requirements.txt` or `pyproject.toml` included
- a reproducible run command (`make run`, `python -m ...`, or `docker compose up`)

---

## 0.7 Quick Commands You’ll Use Constantly

```bash
# Create a feature branch
git checkout -b feat/my-change

# Save progress often
git add -A
git commit -m "Add baseline model training script"

# Run tests
pytest -q

# Run a FastAPI service (example)
uvicorn src.serve:app --reload --port 8000
```

---

## 0.8 “Good Enough” Math Rule

You are not training to be a mathematician. You need:
- intuition
- enough math to debug and evaluate
- the ability to explain tradeoffs

If you can answer:
- “What is the metric telling me?”
- “Why did this model improve?”
- “What is overfitting in this case?”
…you’re on track.

---

## Checkpoint

- [ ] Python env created and dependencies installed  
- [ ] GitHub repo created (even for practice)  
- [ ] Docker installed and working  
- [ ] Learning log created
