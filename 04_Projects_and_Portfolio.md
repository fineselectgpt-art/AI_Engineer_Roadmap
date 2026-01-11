
# 💼 04 — Projects & Portfolio (Ship Real Things)

This chapter defines your portfolio as **product‑style projects**. Each project includes:
- requirements
- suggested datasets
- architecture
- evaluation expectations
- README checklist
- stretch goals

---

## Portfolio Strategy (What Recruiters Want)

Aim for **3 strong projects** rather than 10 unfinished ones:
1. Classic ML project (clean evaluation + pipeline)
2. Deep Learning project (PyTorch, training loop, GPU mindset)
3. LLM/RAG project (retrieval + grounded responses)
+ optional deployed “capstone” that combines everything

> ✅ Each project should answer: “What business/user problem does this solve?”

---

## Project 1 — LLM Chatbot + Vector Search (RAG)

### Goal
Build a chatbot that answers questions **from your own knowledge base** (docs, PDFs, notes), with sources shown.

### Core features
- ingest documents → chunk → embed
- store embeddings in **FAISS**
- retrieve top‑k relevant chunks
- generate response with an LLM prompt that includes retrieved context
- return **sources** (document + chunk IDs)

### Suggested datasets
- your own notes (course notes, manuals)
- public documentation (small subset)
- FAQs from a domain you know (automotive, music production, etc.)

### Architecture (simple)
```
Docs -> Chunk -> Embeddings -> Vector Index
User Q -> Embed Q -> Retrieve top-k -> Prompt -> LLM -> Answer + Sources
```

### Evaluation
- 20 test questions
- measure: groundedness (did it cite relevant sources?), hallucinations (did it invent?)
- log failures and improvements

### Stretch goals
- add re‑ranking
- add conversation memory (with limits)
- add simple UI (Streamlit or React + API)

> ✅ **Deliverable:** Hosted demo + README + evaluation notes.

---

## Project 2 — Real‑Time Dashboard With Predictive Insights

### Goal
Create a small analytics dashboard that also predicts something useful.

Examples:
- predict equipment failure risk (classification)
- forecast demand (time series)
- predict customer churn (classification)

### Core features
- scheduled data refresh
- model training script
- API endpoint for predictions
- dashboard that displays predictions + confidence

### Tech suggestions
- pandas + scikit‑learn
- FastAPI
- Postgres (optional)
- Streamlit (fast UI) or lightweight web UI

### Evaluation expectations
- baseline model + improved model
- error analysis by segment

---

## Project 3 — AI Image Classification API

### Goal
Train a classifier and expose it via an API.

### Core features
- dataset loader
- training loop in PyTorch
- model checkpointing
- `/predict` endpoint that returns label + confidence
- dockerized service

### Datasets
- CIFAR‑10 (starter)
- Food‑101 (more realistic)
- a small custom dataset (advanced)

### Stretch goals
- add Grad‑CAM visualization
- add batch inference endpoint

---

## Supporting Mini‑Projects (Confidence Builders)

### Mini 1 — Titanic Predictor (Classic)
- focus on feature engineering + leakage avoidance

### Mini 2 — Sentiment Classifier
- baseline with TF‑IDF + logistic regression
- then upgrade to a transformer model (optional)

### Mini 3 — House Price Regression
- focus on bias/variance and robust evaluation

---

## README Checklist (Use Template)

Your README must include:
- problem statement + user value
- dataset description
- approach (baseline → improvements)
- metrics + plots
- error analysis (what failed + why)
- how to run (local + docker)
- demo link (or gif/screenshots)
- limitations + next steps

Template in: `templates/Project_README_Template.md`

---

## Rubric (How You’ll Be Graded)

| Category | Passing | Strong |
|---|---|---|
| Problem framing | clear goal + metric | strong user story + constraints |
| Code quality | clean modules, runs | tests + typing + lint |
| Evaluation | correct metrics | segmented analysis + ablations |
| Deployment | runs locally | docker + hosted demo |
| Communication | readable README | diagrams + experiment notes |

> ✅ If you can hit “Strong” on two projects, you’re competitive.

---

## Capstone Option (Optional but Powerful)

Combine:
- ingestion + ETL
- model training + tracking
- FastAPI service
- UI demo
- deployment + monitoring

This becomes your “I can ship end‑to‑end systems” proof.

---

## Checkpoint

- [ ] I have at least 3 project repos planned with timelines  
- [ ] Each project has a baseline + improvement plan  
- [ ] Each project has an evaluation plan (metrics + test questions)  
- [ ] I have a consistent README format across repos
