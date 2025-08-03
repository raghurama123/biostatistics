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

  ul {
    list-style-type: disc;
  }

  ul li::marker {
    color: #94231b;
  }

  ul ul {
    list-style-type: circle;
  }

  ul ul li::marker {
    color: #94231b;
  }
---

# Module 1: Introduction to Biostatistics and Data Description

---

<small>

## What is Biostatistics?
Biostatistics deals with the application of statistical methods to biological problems.  
**Biostatistics = Statistics for Biology**

In physics or chemistry:  
- Variation is mostly due to **experimental error**. Recall the definition of _variance_ and _standard deviation_. 
- Averaging over repeated measurements on the **same sample** eliminates variance.

In biology:  
- We study **naturally varying populations** (organisms, cells, patients, etc.).  
- This **biological variation** is a meaningful phenomenon and not an error.  
- We must go **beyond repeated measurements** to understand:  
  - Genetic differences  
  - Environmental effects  
  - _Random_ biological processes

> _Biostatistics helps us to do statistics while accounting for biological variation._

</small>

---

<small>

## Classification of Data in Biostatistics

| **Aspect**     | **Categories**                                                 | **Examples**                            |
|----------------|----------------------------------------------------------------|-----------------------------------------|
| **Data Structure**  | Cross-sectional<br>Time series<br>Longitudinal                 | One-time survey<br>Heart rate over 24 hrs<br>Glucose levels at multiple visits |
| **Data Type**  | Numerical<br>Categorical                                       | Height, Temperature<br>Blood group      |
| **Data Scale**      | Ratio / Interval (Numerical)<br>Ordinal / Nominal (Categorical)| Temperature (°C), Weight<br>DAFOR scale, Genotype |

> _Note: Data structure appears first because it reflects **how** the data was collected before analyzing what type of data was recorded or how it was measured._

</small>

---
<small>

## Data Structures 

- **Cross-sectional data**
  - Data collected **at a single time point**; Multiple subjects, one measurement per variable
  - No tracking over time
  - *Example:* Blood pressure of 100 patients measured today

- **Time series data**
  - Repeated measurements of **a single subject or system** over **time**
  - Focus is on **temporal trends, patterns, fluctuations**
  - Time is a key variable
  - *Example:* Heart rate of a patient measured every hour for 24 hours

- **Longitudinal data (Combines cross-sectional and time series elements)**
  - Repeated measurements of **multiple subjects** over time
  - Tracks **within-subject changes** and **between-subject variation**
  - *Example:* Glucose levels of 50 patients measured weekly for 3 months

</small>

---

<small>

## Types and Scales of Data

Based on types and scales, biological data (or variables) can be broadly classified into:

- **Numerical (Quantitative) data**:  These are numeric values that can be measured or counted on **interval** or **ratio** scales.

  - **Interval scale**: Numeric scale with equal spacing but **no true zero**  
    *Example: Temperature in °C (40°C is not twice as hot as 20°C)*

  - **Ratio scale**: Numeric scale with a **true zero** point  
    *Example: Height of a plant (40 cm is twice as tall as 20 cm)*

- **Categorical (Qualitative) data**:  These are non-numeric and describe categories or groups measured using **nominal** or **ordinal** scales.

  - **Nominal scale**: Categories without any intrinsic order  
    *Example: Blood group, species name*

  - **Ordinal scale**: Categories with a meaningful order, but unequal spacing between categories  
    *Example: Abundance of a plant species as Dominant, Abundant, Frequent, Occasional, Rare (DAFOR)*

</small>

---

<small>

## Numerical (Quantitative) Data

Quantitative data are **numeric values** that can be **measured** or **counted**.

They allow arithmetic operations and are of two types:
- **Discrete**: Countable whole numbers (e.g., number of leaves)
- **Continuous**: Measurable quantities that can take any real value within a range (e.g., weight, height)

Quantitative data are measured on:
- **Interval scale**
- **Ratio scale**

**Examples:**
- Plant height (in cm)
- Body temperature (in °C)
- Enzyme activity levels


</small>

---

<small>

## Interval Scale

Numerical values with **equal intervals**, but **no true zero**.

**Properties:**
- **Addition and subtraction make sense**  
  - Example: The difference between 40°C and 30°C (10°C) is the same as between 20°C and 10°C — both represent a 10-degree change in temperature.

- **Ratios do not make sense**  
  - Example: 40°C is not "twice as hot" as 20°C because 0°C does not represent the absence of temperature (it's not a true zero).

**Examples:**
- Temperature in Celsius or Fahrenheit
- IQ scores (in psychological studies)


</small>

---

<small>

## Ratio Scale

Numerical values with **equal intervals** and a **true zero point**  
(Zero means the **absence** of the quantity being measured).

**Properties:**
- All arithmetic operations are valid: addition, subtraction, multiplication, division
- **Ratios are meaningful**  
  - Example: A plant that is 40 cm tall is **twice as tall** as one that is 20 cm.  
  - Example: A mouse that weighs 30 g is **1.5× heavier** than one that weighs 20 g.

**Examples:**
- Weight of a mouse
- Height of a plant
- Concentration of glucose in blood
- Cell count in a sample


</small>

---


<small>

## Categorical (Qualitative) Data

Non-numeric data used to label categories or groups.

Measured using:
- **Nominal scale**
- **Ordinal scale**

**Examples:**
- Blood types (A, B, AB, O)
- Species name (*Arabidopsis*, *Zea mays*)
- Eye color

</small>

---

<small>

## Nominal Scale

Categories with **no intrinsic order**.  
They are **labels** used for naming or classification.

**Operations allowed:**  
- **Counting**: How many samples belong to each category  
  - Example: 12 samples are labeled as "neuron", 8 as "glial"  
- **Mode**: Identify the most frequent category  
  - Example: The most common blood group is "O"

**Not allowed:**  
- **Averaging or ranking**  
  - Example: You cannot compute an "average species"  
  - Sorting genotypes alphabetically doesn't imply biological order

**Examples:**
- Genotype (AA, Aa, aa)
- Cell type (neuron, glial, epithelial)
- Blood group (A, B, AB, O)


</small>

---

<small>

## Ordinal Scale

Categories with a **meaningful order**, but **unequal spacing** between levels.

**Operations allowed:**  
- **Ranking**: You can sort or order the categories  
  - Example: "Severe" disease is ranked higher than "Mild"
- **Median**: You can find the middle-ranked value in ordered data

**Not allowed:**  
- **Arithmetic operations**  
  - Example: You can’t say "Moderate" is the average of "Mild" and "Severe"  
  - The difference between "Abundant" and "Frequent" is not equal to the difference between "Frequent" and "Occasional"

**Examples:**
- **DAFOR scale**: Dominant > Abundant > Frequent > Occasional > Rare
- **Disease severity**: Mild < Moderate < Severe
- **Tumor grading**: Grade I, II, III, IV (increasing severity)



</small>

---

<small>

## Data Representation

Data can be _represented_ in two main forms:

- **Long Form Representation for the Raw Data**  
  - Collected as-is from observations or experiments
  - Typically stored in **tables** with rows = observations, columns = variables
  - Both **categorical** and **numerical** are presented as tables in raw form

- **Compact Form Representation to Summarize the Raw Data**  
  - Useful for **description, visualization, and comparison**
  - Particular compact form depends on whether the variable is **categorical** or **numerical**


</small>

---

<small>

## Long Form: Tables

Raw data is often recorded in tabular form:

| Sample ID | Species     | Height (cm) | Abundance |
|-----------|-------------|-------------|-----------|
| S1        | Arabidopsis | 14.5        | Frequent  |
| S2        | Arabidopsis | 16.2        | Abundant  |
| S3        | Zea mays    | 120.3       | Dominant  |

This format is:
- Used for **data entry and storage**
- Directly imported into statistical tools (Excel, R, Python/pandas)
- The basis for further analysis and summarization

</small>

---

<small>

## Compact Form: Categorical Data

Categorical variables are summarized using **frequency tables**.

**Example: Abundance levels**

| Category   | Frequency |
|------------|-----------|
| Rare       | 2         |
| Occasional | 5         |
| Frequent   | 10        |
| Abundant   | 7         |
| Dominant   | 1         |

Can be visualized as:
- **Bar plots**
- **Pie charts**

</small>

---

<small>

## Compact Form: Numerical Data

Numerical data are summarized using **descriptive statistics**:

- **Measures of central tendency**:
  - Mean, Median, Mode

- **Measures of spread**:
  - Range, Variance, Standard Deviation, IQR

**Example: Plant Height (cm)**  
- Mean = 42.3  
- Median = 38.5  
- SD = 12.1

Can be visualized as:
- Histograms
- Boxplots

</small>

