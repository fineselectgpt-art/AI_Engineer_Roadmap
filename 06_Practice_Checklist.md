
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
