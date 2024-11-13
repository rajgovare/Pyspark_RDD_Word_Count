---

# PySpark Word Count

## Overview
This project demonstrates how to create an RDD (Resilient Distributed Dataset) using PySpark, apply transformations to 
count the occurrences of each word in a text dataset, and perform actions to collect and print the results. 
The example uses a list of text strings and performs word count operations using PySpark functionalities.

## Methodology
1. **Data Initialization**: 
   - A sample dataset is defined as a list of sentences.
   - This dataset is parallelized into an RDD.
2. **Transformations**:
   - The sentences are split into words using the `flatMap()` transformation.
   - Each word is then mapped to a key-value pair of the form `(word, 1)` using the `map()` transformation.
   - The word counts are aggregated using the `reduceByKey()` transformation to sum up the occurrences of each word.
3. **Actions**:
   - The `collect()` action retrieves the word count results.
   - The results are printed to the console.

## Requirements
- Python 3.x
- PySpark

To install PySpark, use the following command:
```bash
!pip install PySpark
```

## Results
The program successfully processes the provided text dataset and counts the occurrences of each word. 
It identifies that the word **"hello"** appears the most frequently with a total of **5 occurrences**.
Meanwhile, words like **"world," "spark," "RDD," "pySpark,"** and **"Raj"** each appear only **once** in the dataset. 

---
