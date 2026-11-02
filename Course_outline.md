# Course outline

# 1. Reliability and maintainability engineering

Engineering discipline which studies, characterises, analyses, and measures the failure and repair processes affecting systems, with the aim of improving their performance by:

- reducing the probability of failures and/or their consequences (thus reducing the safety risk),
- reducing downtime thus increasing the operational time,
- extending their useful life beyond the initially intended design life.

Provides concepts and criteria for both the **design** and **maintenance** of systems.

# 2. Course structure

The course consists of three main parts: **basic reliability and availability models, failure data analysis, and quality control**. You do not need to understand the details of each part at this stage. However, we would like you to pay particular attention to the following concepts and prerequisites.

## 2.1. Basic reliability and availability models

In this part, you will learn how to model the failure and repair processes of components and systems, and how to characterise their performance in terms of reliability, maintainability, and availability.

A good understanding of basic [calculus](https://www.khanacademy.org/math/calculus-1) and [probability theory](https://www.khanacademy.org/math/statistics-probability) is expected. If you are not comfortable with these topics, we recommend reviewing the relevant material.

A key distinction to understand: **Reliability vs. Availability.**

- **Reliability:** item not failed before $t$ → works continuously before $t$ → <u>survived</u> until time $t$;
- **Availability:** regardless wether this item failed before → <u>may have failed, but been repaired</u> before $t$;
- **Relationship:**
    
    $$
    Availability \ge Reliability.
    $$
    

## 2.2. Analysis of failure data

In this part, you should be able to identify and derive appropriate reliability and maintainability models based on observed data. This requires an understanding of both descriptive and inferential statistics.

## 2.3. Quality control

Quality control is about determining the predictability of a process and its ability to meet customer requirements. Here,

- Predictability → control charts for variables and attributes;
- Process capability → process capability analysis.

# 3. **Quantitative models vs statistical models**

We talk about both quantitative models and statistical models in this course,

- **Quantitative models:**
    - Use numbers to describe, test, and infer relationships or patterns;
    - Including mathematical modelling, optimisation, and computational methods.
- **Statistical models:**
    - Primarily concerned with understanding data and making inferences about populations from samples;
    - Including hypothesis testing, regression, probability theory, and predictive modelling.