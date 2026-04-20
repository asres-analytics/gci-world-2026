# Week 02 — Efficient Data Manipulation with NumPy 📊⚡

Program: **GCI World 2026 (Global Consumer Intelligence)**  
Lab: **Matsuo-Iwasawa Laboratory, University of Tokyo**  
Session: **Lecture 2 (April Session)**  

---

## 🎯 Objective

The objective of Week 02 was to transition from **basic Python programming** to **efficient, data-centric computing** using **NumPy**.

Instead of working with simple variables and loops, I focused on learning how numerical and tabular data is handled at scale, how performance improves through vectorization, and how NumPy enables fast computations that are essential for data science, machine learning, and AI workflows.

---

## 📘 What I Learned

### 🔹 Introduction to NumPy

NumPy (Numerical Python) is a core Python library designed for **fast numerical and scientific computing**. It provides efficient data structures and operations that replace slow, loop-based Python logic.

I learned that NumPy is foundational to almost every data science tool, including:
- Pandas  
- Machine learning libraries  
- Scientific computing frameworks  

The key motivation for NumPy is **performance**. Unlike Python lists, NumPy arrays store data in **continuous memory**, allowing faster access and optimized CPU-level operations.

---

### 🔹 NumPy Arrays (`ndarray`)

The central data structure in NumPy is the **ndarray**.

The **`ndarray` (N-dimensional array)** is the core data structure in NumPy.

 
 ### Important properties:
- Arrays store **homogeneous data** (single data type)
- Support **1D and multi-dimensional structures**
- Enable efficient mathematical operations
- Represent data in vector and matrix form

This required shifting from list-based thinking to **array-based thinking**.

---

### 🔹 Vectorization & Universal Functions

One of the most important concepts this week was **vectorization**.

NumPy replaces explicit Python loops with vectorized operations powered by universal functions (`ufuncs`). These operations apply element‑by‑element at C‑level speed.
Benefits observed:

- Cleaner and more readable code
- Significant speed improvements
- Fewer logical errors


Instead of writing loops:

```python
for i in range(len(a)):
    a[i] = a[i] * 2 
```

## We use NumPy vectorized operations:
```python
  a = a * 2
```
---
## 🔹 Broadcasting
**Broadcasting** allows NumPy to automatically align array shapes during operations without copying data.
I learned:

- Scalar‑to‑array operations
- Shape compatibility rules
- Common causes of broadcasting errors
- This explained how NumPy performs flexible operations while remaining memory‑efficient.

---
## 🔍 Indexing and Data Selection
### 🔹 Indexing & Slicing
I practiced:

- Zero‑based and negative indexing
- Slicing using `start` : `end` : `step`
- Periodic extraction (e.g., weekly sampling from time‑series data)
Important insight: slicing operations are `views`, not copies.
### 🔹 Boolean & Advanced Indexing
Boolean indexing was a key tool for real‑world data cleaning:

- Filtering values using conditions
- Removing missing or invalid observations
- Combining conditions using logical operators

Advanced indexing enabled extraction of non‑consecutive elements and custom sub‑matrices.

---

## 📐 Working with 2D Arrays
### 🔹 Two‑Dimensional Data
2D NumPy arrays were used to represent tabular datasets where:

- Rows correspond to observations
- Columns correspond to features

All mathematical operations apply `element‑wise` unless matrix multiplication is explicitly used.

### 🔹 Axis & Aggregation
I learned that:

- `axis=0` performs column‑wise operations
- `axis=1` performs row‑wise operations

**Aggregation functions** such as 
-  **mean**, 
- **min**, 
- **max**, 
- **sum**, and
- **std** were used to summarize datasets correctly.

## 🔹 Reshaping

Using reshape() and -1 helped me understand how NumPy manages dimensions without changing underlying data.
---


## 📊 Dataset & Hands‑On Practice
I worked with the **NOAA Global Historical Climatology Network (GHCN)** sample dataset, provided as the file:

dataset/`GHCND_sample_csv.csv`
From this dataset, I focused on the following numerical columns:

- **TMAX** — maximum temperature (in tenths of °C)
- **TMIN** — minimum temperature (in tenths of °C)
- **PRCP** — precipitation (in tenths of mm)

Using this dataset, I practiced:

Loading numeric columns with np.loadtxt()

- Unit conversion using vectorized operations
- Daily temperature range computation
- Handling missing precipitation values (encoded as large constants such as 9999)
- Statistical aggregation across time periods using axis‑based operations

The full hands‑on analysis using this dataset is provided in the following notebook:

- notebooks/`numpy_weather_analysis.ipynb`

---


## 🛠️ What I Practiced

- Vectorized arithmetic and transformations
- Indexing, slicing, and boolean masking
- Axis‑based aggregation on 2D arrays
- Reshaping and stacking arrays
- Introductory linear algebra operations (transpose, dot product, matrix multiplication)

--- 


## ⚠️ Challenges Faced

- Understanding broadcasting rules and shape compatibility
- Correct use of the `axis` parameter
- Distinguishing slicing vs advanced indexing

These required experimentation and visualization to fully grasp how NumPy operates internally.



## 📚 References

- GeeksforGeeks. [NumPy ndarray (n-dimensional array)](https://www.geeksforgeeks.org/numpy/numpy-ndarray/)


