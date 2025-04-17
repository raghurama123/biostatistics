---
marp: true
title: Introduction to Biostatistics
theme: default
paginate: true
footer: '[Go to main page](https://raghurama123.github.io/biostatistics/)'
style: |
  section {
    font-size: 1.5em;
    line-height: 1.5;
  }
  h1{
    color: #94231b;
  }
  h2{
    color: #94231b;
  }
  h3 {
    color: #004080;
  }
  footer {
    font-size: 0.5em;
    color: #1b6794;
  }
---

# Module 1: Introduction to Biostatistics and Data Description

---

<small>

## What is Biostatistics?
Biostatistics deals with the application of statistical methods to biological problems.  
**Biostatistics = Statistics for Biology**

In physics or chemistry:  
- Variation is mostly due to **experimental error**. 
- Averaging over repeated measurements on the **same sample** eliminates variance.

In biology:  
- We study **naturally varying populations** (organisms, cells, patients).  
- This **biological variation** is a meaningful phenomenon—not error.  
- We must go **beyond repeated measurements** to understand:  
  - Genetic differences  
  - Environmental effects  
  - _Random_ biological processes

> Biostatistics helps us to do statistics while accounting for biological variation—not eliminate it.

</small>

---

<small>

## Types of Biological Data

Biological data (or variables) can be broadly classified into:

- **Categorical or Qualitative data**:  These are non-numeric and describe categories or groups.  
  They are measured using **nominal** or **ordinal** scales.

  - **Nominal scale**: Categories without any intrinsic order  
    *Example: blood group, species name*

  - **Ordinal scale**: Categories with a meaningful order, but unequal spacing between categories  
    *Example: Abundance of a plant species as Dominant, Abundant, Frequent, Occasional, Rare (DAFOR)*

- **Numerical or Quantitative data**:  These are numeric values that can be measured or counted.  
  They are measured on **interval** or **ratio** scales.

  - **Interval scale**: Numeric scale with equal spacing but **no true zero**  
    *Example: Temperature in °C (40°C is not twice as hot as 20°C)*

  - **Ratio scale**: Numeric scale with a **true zero** point  
    *Example: Height of a plant (40 cm is twice as tall as 20 cm)*

</small>

---


