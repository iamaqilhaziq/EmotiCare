# EmotiCare AI-Assisted Emotional Analysis Workflow

## Overview

EmotiCare incorporates an AI-assisted emotional analysis workflow to analyse journal text and identify emotional information that can support appropriate digital intervention.

The current workflow combines sentiment analysis, text feature extraction, machine-learning emotion classification, and intervention determination.

---

## High-Level Workflow

```text
Journal Input
      │
      ▼
Input Validation
      │
      ▼
Sentiment Analysis
      │
      ▼
TF-IDF Feature Extraction
      │
      ▼
Logistic Regression
      │
      ▼
Emotion Classification
      │
      ▼
Intervention Determination
      │
      ▼
Analysis Result
```

---

## 1. Journal Input

The emotional analysis process begins with journal text submitted through the EmotiCare journaling feature.

The journal entry provides textual information for the emotional analysis process.

---

## 2. Input Validation

The submitted journal information is validated before emotional analysis is performed.

Only valid input proceeds through the analysis workflow.

---

## 3. Sentiment Analysis

### VADER

VADER is used as part of the sentiment analysis process.

The sentiment analysis provides information about the sentiment expressed within the journal text.

This information contributes to the broader emotional analysis and intervention process.

---

## 4. Text Feature Extraction

### TF-IDF

TF-IDF is used to convert journal text into numerical features that can be processed by the machine-learning classification model.

At a high level:

```text
Journal Text
      │
      ▼
Text Processing
      │
      ▼
TF-IDF
      │
      ▼
Numerical Features
```

---

## 5. Emotion Classification

### Logistic Regression

The numerical features produced through TF-IDF are processed using a Logistic Regression classifier.

The classifier identifies an emotional category associated with the analysed text.

---

## 6. Intervention Determination

Following emotional analysis, EmotiCare determines an appropriate intervention type.

At a conceptual level:

```text
Emotional Analysis Result
          │
          ▼
Determine Intervention
          │
     ┌────┼──────────────┐
     │    │              │
     ▼    ▼              ▼
 Normal  Guided       Higher-Risk
Support  Support       Support
```

The intervention process allows the platform to respond differently according to the emotional information identified during analysis.

---

## 7. Analysis Output

The analysis process can produce information including:

- Sentiment information
- Detected emotional category
- Intervention type

The relevant output is then used by the EmotiCare platform as part of its emotional-support workflow.

---

## Complete Conceptual Process

```text
BEGIN

    RECEIVE journal text

    VALIDATE journal text

    IF journal text is valid THEN

        PERFORM sentiment analysis

        EXTRACT text features using TF-IDF

        CLASSIFY emotion using Logistic Regression

        DETERMINE intervention type

        STORE relevant analysis result

        RETURN emotional analysis result

    ELSE

        STOP analysis process

    END IF

END
```

---

## Current AI/ML Approach

The current EmotiCare AI-assisted emotional analysis workflow incorporates:

| Function | Approach |
|---|---|
| Sentiment Analysis | VADER |
| Feature Extraction | TF-IDF |
| Emotion Classification | Logistic Regression |
| Output | Emotion and intervention information |

---

## Human-Centered Principle

AI-assisted analysis in EmotiCare is intended to support the broader emotional-care process.

The system follows the principle:

> **Technology that supports people, not replaces people.**

Human support remains an important component of the overall emotional-care approach.

---

> **Note:** This document presents the conceptual AI workflow. Production model files, source code, model parameters, API configurations, security configurations, and other proprietary implementation details are intentionally excluded.