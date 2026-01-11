
# 🛠️ 02 — Tools & Frameworks (The AI Engineer Toolbelt)

This chapter turns the “AI stack” into a **practical map**: what tools exist, when you use them, and how they connect in real projects.

---

## 2.1 Core Python Data Stack

### Must‑know libraries
- **NumPy** — fast numeric arrays, shapes, vector operations
- **pandas** — tabular data manipulation and joins
- **matplotlib** — plotting fundamentals (keep it simple)
- **scikit‑learn** — classical ML models + pipelines

> 💡 **Tip:** scikit‑learn’s `Pipeline` + `ColumnTransformer` is the fastest path to clean, reproducible ML.

---

## 2.2 Classic ML Framework: scikit‑learn

### What you should be able to do
- build baselines fast (`LogisticRegression`, `RandomForest`, and gradient boosting if you add it)
- use `train_test_split` correctly (or time‑based splits)
- cross‑validation (`GridSearchCV`, `RandomizedSearchCV`)
- calibration, thresholds, and imbalanced classification strategies

#### Minimal baseline template
```python
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report
from sklearn.linear_model import LogisticRegression

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

model = LogisticRegression(max_iter=200)
model.fit(X_train, y_train)

pred = model.predict(X_test)
print(classification_report(y_test, pred))
```

---

## 2.3 Deep Learning: PyTorch (Recommended First)

### Why PyTorch
- Pythonic, flexible, widely used in research + production
- easier debugging for beginners

### What to master
- tensors + shapes
- `Dataset` / `DataLoader`
- training loop (forward → loss → backward → step)
- saving/loading models
- GPU basics (moving tensors to device)

> ✅ **Deliverable:** Build a small classifier in PyTorch and explain the training loop in plain language.

---

## 2.4 TensorFlow / Keras (Good To Know)

You don’t need both PyTorch and TensorFlow to start.  
However, knowing Keras makes it easier to:
- read existing codebases
- use certain enterprise stacks
- ship simple models quickly

**Bootcamp rule:** Choose one as your “primary,” but be able to read the other.

---

## 2.5 LLMs: Hugging Face + RAG Tooling

### Core concepts
- tokenization
- embeddings
- fine‑tuning vs prompting
- retrieval‑augmented generation (RAG)
- evaluation (hallucinations, groundedness)

### Practical tools
- **transformers** — models + pipelines
- **datasets** — dataset loading/versioning
- **sentence-transformers** — strong embedding baselines
- **FAISS** — local vector search
- optional hosted vector DBs (Pinecone, Weaviate, Milvus)

> ⚠️ **Pitfall:** A “chatbot” demo without retrieval often fails because it can’t ground answers in your data.

---

## 2.6 APIs and Serving: FastAPI

Most AI features get delivered behind a service.

### You should be able to
- define request/response schemas (pydantic)
- load a model artifact and run inference
- handle errors and return useful messages
- add basic logging

#### Mini FastAPI inference example
```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

class Input(BaseModel):
    text: str

@app.post("/predict")
def predict(inp: Input):
    # model inference goes here
    return {"label": "positive", "score": 0.91}
```

---

## 2.7 Docker (Reproducibility + Deployment)

### Why Docker matters
- “works on my machine” stops being a problem
- deployments become repeatable
- you can pin versions cleanly

### Minimum Docker skills
- write a `Dockerfile`
- build and run images
- expose ports
- manage environment variables

> ✅ **Deliverable:** Dockerize one of your APIs and run it locally.

---

## 2.8 CI/CD: GitHub Actions (Minimum Setup)

### What to automate
- run tests on every push
- lint/format checks (optional)
- build docker image (optional)
- deploy (later)

> ✅ Even a basic workflow that runs `pytest` is a big signal to employers.

---

## 2.9 Experiment Tracking & Reproducibility

### Tools (choose one)
- **MLflow** (open‑source, widely used)
- **Weights & Biases** (excellent UX)

### What to log
- model version
- data version
- hyperparameters
- metrics
- evaluation plots

> 🧠 The goal is to answer: “What changed, and why did metrics move?”

---

## 2.10 Data/Model Versioning

- **Git** for code
- **DVC** for datasets + model artifacts (optional but strong)
- keep “artifact” files out of git unless tiny

---

## 2.11 Cloud (Where This Usually Lands)

### Core concepts
- compute (CPU vs GPU)
- storage (object storage, blobs)
- managed ML services vs DIY

### Common choices
- AWS (SageMaker, EC2, S3)
- GCP (Vertex AI, Compute Engine, GCS)
- Azure (Azure ML, VMs, Blob Storage)

> 💡 **Bootcamp advice:** Learn one cloud deeply; understand the others at a surface level.

---

## 2.12 Orchestration (When Projects Grow)

- **Airflow** or **Prefect** for scheduled workflows
- “pipelines” for ETL → training → evaluation → deployment

You don’t need orchestration for tiny projects — but you should know why it exists.

---

## Labs

### Lab A — scikit‑learn Pipeline
- build preprocessing + model in one pipeline
- cross‑validate and report metrics
- save the fitted pipeline artifact

### Lab B — FastAPI + model artifact
- load saved model
- expose `/predict`
- add request validation

### Lab C — RAG mini prototype
- ingest 20–50 documents
- embed + store in FAISS
- retrieve top‑k context
- generate answer from retrieved context
- include “sources” in the response

---

## Checkpoint

- [ ] I can explain when to use scikit‑learn vs deep learning  
- [ ] I can build a FastAPI service around a model  
- [ ] I can Dockerize the service  
- [ ] I can use embeddings + vector search for a basic RAG app  
- [ ] I understand what experiment tracking is and why it matters
