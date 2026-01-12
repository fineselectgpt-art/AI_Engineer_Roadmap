# 📘 Python Data Handling Bootcamp Guide (Combined)

> This file is a single-file version of the multi-chapter mini-ebook.

# 📘 Python Data Handling Bootcamp Guide (NumPy + pandas)
**Mini-ebook (Markdown + PDF)**

This mini-ebook packages a curated, high-signal set of learning resources for:
- **NumPy** (arrays, shapes, vectorization, broadcasting)
- **pandas** (DataFrames, IO, cleaning, joins, reshaping)

It also includes a **bootcamp-style practice plan** so you can turn resources into skills.

---

## Contents

- `README.md` (this file)
- `01_Official_Docs.md`
- `02_YouTube_Playlists.md`
- `03_Packt_Books_And_Video.md`
- `04_Coursera_And_Udemy.md`
- `05_Other_Top_Resources.md`
- `06_Practice_Checklist.md`
- `07_Best_Of_Learning_Stack.md`

PDF:
- `pdf/Python_Data_Handling_Bootcamp_Guide.pdf`

---

## How to use (recommended)

1. Follow **01_Official_Docs.md** first (fast + correct).
2. Use **YouTube** for repetition while coding.
3. Do the **Practice Checklist** (this is what makes it stick).
4. When stuck, use the “Other resources” section for targeted help.

---

## Quick install (local)

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -U pip
pip install numpy pandas matplotlib jupyter
```

---

## Print-friendly PDF

Open: `pdf/Python_Data_Handling_Bootcamp_Guide.pdf`

---

# 01 - Official Docs (High-signal, always current)

These are the most reliable references for **correctness** and **best practices**.

---

## NumPy

### NumPy Quickstart
**Best for:** arrays, shapes, axis, vectorization (the mental model you must have)
- Link: https://numpy.org/doc/stable/user/quickstart.html

**Bootcamp task**
- Read once.
- Then recreate these from memory:
  - Create arrays (1D/2D)
  - Reshape
  - Slice
  - `axis=0` vs `axis=1`
  - `sum`, `mean`, `argmax` along an axis

---

### NumPy: Absolute basics for beginners
**Best for:** the "hello world" of ndarray, indexing, and common operations
- Link: https://numpy.org/doc/stable/user/absolute_beginners.html

**Bootcamp task**
- Write a 30-line script that:
  - loads a CSV with `numpy.genfromtxt`
  - computes mean, std
  - normalizes the data
  - prints top-5 rows

---

### NumPy User Guide
**Best for:** deeper fundamentals and patterns you keep returning to
- Link: https://numpy.org/doc/stable/user/

**Suggested sequence inside the user guide**
1. Array creation
2. Indexing
3. Broadcasting
4. Copies vs views
5. Universal functions (ufuncs)

---

### NumPy Learn Hub
**Best for:** curated educational resources vetted by the community
- Link: https://numpy.org/learn/

---

## pandas

### pandas Getting Started
**Best for:** how pandas thinks (tables, indexing, common workflows)
- Link: https://pandas.pydata.org/docs/getting_started/index.html

---

### Getting started tutorials
**Best for:** DataFrame basics, IO, cleaning, joins, reshaping, time series
- Link: https://pandas.pydata.org/docs/getting_started/intro_tutorials/

**Bootcamp task**
- Complete the tutorials and turn each tutorial into a small notebook:
  - `01_read_write.ipynb`
  - `02_select_filter.ipynb`
  - `03_missing_values.ipynb`
  - `04_joins.ipynb`
  - `05_reshape.ipynb`
  - `06_timeseries.ipynb`

---

### 10 minutes to pandas
**Best for:** a fast overview you can repeat weekly
- Link: https://pandas.pydata.org/docs/user_guide/10min.html

**Bootcamp rule**
- Re-run the examples weekly until they feel boring.

---

### pandas Community Tutorials
**Best for:** vetted external tutorials and workshops from the community
- Link: https://pandas.pydata.org/pandas-docs/stable/tutorials.html

---

## If you do nothing else

**NumPy Quickstart -> pandas Getting Started -> pandas 10 Minutes**

That is enough to start building real projects.

---

# 02 - YouTube (Free + very practical)

Use YouTube for repetition while you code. Watch a small segment, then implement it immediately.

---

## pandas (highly recommended)

### Corey Schafer - Pandas Tutorials (playlist)
- Playlist: https://www.youtube.com/playlist?list=PL-osiE80TeTsWmV9i9c58mdDCSskIFdDS
- Channel:  https://www.youtube.com/channel/UCCezIgC97PvUuR4_gbFUs5g

**How to use it (bootcamp style)**
- Create a folder `pandas_labs/`
- After each video, implement one small lab:
  - a CSV load + quick EDA
  - a filter + groupby
  - a join between two tables
  - a pivot table
  - time series resampling

**Minimum output**
- 8 labs total, each in its own notebook or script.

---

## NumPy (full beginner course + extras)

### freeCodeCamp channel (lots of full courses)
- Channel: https://www.youtube.com/@freecodecamp

### freeCodeCamp NumPy learning article (with video context)
- Article: https://www.freecodecamp.org/news/numpy-python-tutorial/

**Bootcamp drill (must-do)**
- Rebuild common operations without looking:
  - vectorized math (no loops)
  - boolean masking
  - `reshape`, `transpose`
  - broadcasting example (add a column vector to a matrix)

---

## How to watch YouTube without wasting time

Use this loop:

1. Watch 5-10 minutes
2. Pause
3. Code 15-30 minutes
4. Write a 3-bullet recap

If you can’t code it, you don’t know it yet.

---

# 03 - Packt Publishing (Books + Video Courses)

Packt is useful when you want a structured walk-through with a practical angle.

---

## Packt book (NumPy + pandas)

### Hands-On Data Analysis with NumPy and pandas
- Packt page: https://www.packtpub.com/en-us/product/hands-on-data-analysis-with-numpy-and-pandas-9781789534245

**Bootcamp use**
- Don’t "read it like a novel."
- Treat it like a lab manual:
  - reproduce code
  - change variables
  - write a short summary after each chapter

**Output requirement**
- A repo called `hands_on_numpy_pandas_notes/` with:
  - chapter notebooks
  - a README describing what you learned

---

## Packt video course

### Unpacking NumPy and Pandas (video)
- Packt page: https://www.packtpub.com/en-us/product/unpacking-numpy-and-pandas-9781787121195

**Bootcamp use**
- If you learn better by watching than reading, use this as your primary.
- Still produce labs after each module.

---

## Packt content via Coursera

Packt content sometimes appears on Coursera as standalone courses.
Example:
- Data Processing and Exploration with NumPy & Pandas: https://www.coursera.org/learn/packt-data-processing-and-exploration-with-numpy-and-pandas-2b8vp

---

# 04 - Coursera Plus and Udemy

Use these when you want a structured class feel and guided practice.

---

## Coursera Plus (structured + certificates)

### Guided Project (fast win)
**Python for Data Analysis: Pandas & NumPy**
- Link: https://www.coursera.org/projects/python-for-data-analysis-numpy

**Bootcamp use**
- Do it in one sitting.
- Then recreate the same steps on a different dataset (no copy/paste).

### Browse pandas on Coursera
- Catalog: https://www.coursera.org/courses?query=python+pandas

**How to pick**
- Choose courses that include:
  - exercises
  - mini projects
  - real datasets

---

## Udemy (practice-heavy)

### Python Data Analysis: NumPy & Pandas Masterclass
- Course page: https://www.udemy.com/course/python-pandas/

### Udemy Pandas topic page
- Browse: https://www.udemy.com/topic/pandas/

**Udemy quality filter**
- Look for:
  - recently updated
  - high rating with high review count
  - downloadable datasets
  - exercises or projects

---

# 05 - Other Top Resources (Skill-building)

These are excellent when you want fast practice or a different explanation.

---

## Kaggle Learn (short lessons + exercises)

### Kaggle Learn: Pandas
- Link: https://www.kaggle.com/learn/pandas

Kaggle is great because it forces you to practice, not just watch.

---

## DataCamp (guided practice)

### Data Manipulation with pandas
- Link: https://www.datacamp.com/courses/data-manipulation-with-pandas

### Joining Data with pandas
- Link: https://www.datacamp.com/courses/joining-data-with-pandas

### Writing Efficient Code with pandas
- Link: https://www.datacamp.com/courses/writing-efficient-code-with-pandas

### DataCamp pandas tutorial (reference-style)
- Link: https://www.datacamp.com/tutorial/pandas

---

## edX (university/industry-style)

### Learn pandas hub
- Link: https://www.edx.org/learn/pandas

### Pragmatic AI Labs: Python and Pandas for Data Engineering
- Link: https://www.edx.org/learn/data-engineering/pragmatic-ai-labs-python-and-pandas-for-data-engineering

---

## Real Python (excellent explanations)

### NumPy tutorial
- Link: https://realpython.com/numpy-tutorial/

### NumPy resources hub
- Link: https://realpython.com/tutorials/numpy/

### pandas DataFrame guide
- Link: https://realpython.com/pandas-dataframe/

### Explore a dataset with pandas
- Link: https://realpython.com/pandas-python-explore-dataset/

---

# 06 - Practice Checklist (AI-engineer-ready data handling)

This is the part that transforms "I watched it" into "I can do it."

---

## A. Read / Write (IO)
- [ ] Read CSV
- [ ] Read JSON
- [ ] Read Excel (optional)
- [ ] Write CSV
- [ ] Write Parquet (recommended for analytics workflows)
- [ ] Validate schema (column names + dtypes)

**Coding drill**
```python
import pandas as pd

df = pd.read_csv("data.csv")
assert set(["id", "date", "value"]).issubset(df.columns)
df["date"] = pd.to_datetime(df["date"], errors="coerce")
```

---

## B. Cleaning
- [ ] missing values: `isna`, `fillna`, `dropna`
- [ ] type casting: `astype`, `to_numeric`, `to_datetime`
- [ ] strings: `str.lower`, `str.strip`, regex replace
- [ ] duplicates: `drop_duplicates`

**Coding drill**
```python
df["price"] = pd.to_numeric(df["price"], errors="coerce")
df = df.drop_duplicates(subset=["id", "date"])
df["name"] = df["name"].str.strip().str.lower()
```

---

## C. Joins (merging tables)
- [ ] `merge` with `left`, `inner`
- [ ] validate merge keys
- [ ] handle one-to-many vs many-to-many
- [ ] dedupe keys before merging

**Coding drill**
```python
orders = orders.merge(customers, on="customer_id", how="left", validate="many_to_one")
```

---

## D. Groupby (features + analytics)
- [ ] aggregations: `sum`, `mean`, `count`, `nunique`
- [ ] custom features per group
- [ ] sorting + ranking within group

**Coding drill**
```python
features = (
    df.groupby("customer_id")
      .agg(total_spend=("amount", "sum"),
           orders=("order_id", "nunique"),
           avg_spend=("amount", "mean"))
      .reset_index()
)
```

---

## E. Reshaping (pivot/melt)
- [ ] `pivot_table`
- [ ] `melt` to long format

---

## F. Time series
- [ ] `to_datetime`
- [ ] `set_index` with datetime
- [ ] resample (`D`, `W`, `M`)
- [ ] rolling windows

---

## G. Performance (professional habits)
- [ ] prefer vectorization over loops
- [ ] avoid slow `.apply()` when possible
- [ ] use categorical dtype for low-cardinality strings

**Coding drill**
```python
df["city"] = df["city"].astype("category")
df["ratio"] = df["a"] / df["b"]   # vectorized
```

---

## Weekly mini-project (recommended)

Pick a dataset and deliver:
- `notebook.ipynb` (EDA + cleaning)
- `src/transform.py` (reusable transformation)
- `README.md` (what you did + what you found)

Repeat weekly for 4 weeks.

---

# 07 - Best-of Learning Stack (Minimal switching)

If you want a clean plan:

---

## Step 1: Official docs (fast + correct)
- NumPy Quickstart: https://numpy.org/doc/stable/user/quickstart.html
- pandas Getting Started: https://pandas.pydata.org/docs/getting_started/index.html
- 10 Minutes to pandas: https://pandas.pydata.org/docs/user_guide/10min.html

---

## Step 2: YouTube repetition while coding
- Corey Schafer pandas playlist: https://www.youtube.com/playlist?list=PL-osiE80TeTsWmV9i9c58mdDCSskIFdDS

---

## Step 3: Exercises
- Kaggle Learn Pandas: https://www.kaggle.com/learn/pandas

---

## Step 4: Skill polish
- DataCamp Joining Data with pandas: https://www.datacamp.com/courses/joining-data-with-pandas
- DataCamp Writing Efficient Code with pandas: https://www.datacamp.com/courses/writing-efficient-code-with-pandas

---

## Step 5: Book depth (optional)
- Packt Hands-On Data Analysis with NumPy and pandas: https://www.packtpub.com/en-us/product/hands-on-data-analysis-with-numpy-and-pandas-9781789534245

---

## Bootcamp pacing (suggested)
- Week 1: docs + 6 drills
- Week 2: joins + groupby + reshaping
- Week 3: time series + performance
- Week 4: mini-project (cleaning + features + report)
