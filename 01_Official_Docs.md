
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
