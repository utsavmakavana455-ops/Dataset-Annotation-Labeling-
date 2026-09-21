
# Dataset Annotation & Labeling 🏷️

## 📌 Overview

This repository contains my learning notes and practical exercises on **Dataset Annotation & Labeling** for AI/LLM evaluation and QA workflows.

The goal was to understand how to apply predefined annotation guidelines consistently, identify user intent, handle multiple labels, and correctly deal with ambiguous or edge-case examples.

---

## 🎯 Learning Objectives

* Understand dataset annotation
* Perform single-label classification
* Perform multi-label annotation
* Identify primary and secondary labels
* Handle edge cases
* Follow annotation guidelines
* Avoid over-labeling and under-labeling
* Improve annotation consistency
* Make evidence-based labeling decisions

---

## 🏷️ Labels Practiced

The exercises used the following intent labels:

* **Billing**
* **Login**
* **Technical**
* **Complaint**
* **Refund**

---

## 🧪 Practice Examples

### Example 1 — Single Label

**Text:**

> I forgot my password and can't access my account.

**Annotation:**
`Login`

---

### Example 2 — Billing

**Text:**

> Why was I charged €20 this month?

**Annotation:**
`Billing`

---

### Example 3 — Multi-Label

**Text:**

> I was charged twice and now I can't log into my account.

**Annotation:**
`Billing + Login`

---

### Example 4 — Technical + Complaint

**Text:**

> Your app is terrible! It crashes every time I try to upload a file.

**Annotation:**
`Technical + Complaint`

---

### Example 5 — Refund

**Text:**

> I want a refund because the product I received was damaged.

**Annotation:**
`Refund`

---

### Example 6 — Edge Case

**Text:**

> I think I was charged twice, but I'm not completely sure. Can you check?

**Annotation:**
`Billing`

**Reason:** The user reports a possible billing issue but does not explicitly express dissatisfaction. Therefore, `Complaint` should not be added based on assumption.

---

### Example 7 — Login + Technical

**Text:**

> I can't remember my password, and the password reset page isn't working.

**Annotation:**
`Login + Technical`

**Reason:**

* `Login` → password/account access problem
* `Technical` → password reset page is not working

---

## 🔍 Important Annotation Principles

### 1. Follow the Guidelines

Labels should be assigned according to predefined rules rather than personal interpretation.

### 2. Don't Infer Extra Labels

Only assign a label when the text provides sufficient evidence.

### 3. Primary vs. Secondary Labels

A single example can contain multiple issues, but each additional label must be supported by the annotation guidelines.

### 4. Handle Edge Cases Carefully

Uncertain wording does not automatically mean that another label should be added.

### 5. Avoid Over-Labeling

Adding labels that are not supported by the text can reduce dataset quality.

### 6. Avoid Under-Labeling

Important issues should not be missed when the text clearly supports multiple labels.

---

## 🔄 Annotation Workflow

```text
Read Text
    ↓
Understand Guidelines
    ↓
Identify Intent
    ↓
Check for Multiple Labels
    ↓
Review Edge Cases
    ↓
Assign Labels
    ↓
Check Consistency
    ↓
Final Annotation
```

---

## 🧠 Key Learning

> **Annotate what the text supports, not what you assume.**

Good annotation requires consistency, attention to detail, and strict application of the defined guidelines.

---

## 🚀 Next Learning Topics

* Annotation Quality Control
* Reviewer Disagreement
* Calibration
* Adjudication
* Inter-Annotator Agreement
* Cohen's Kappa
* AI/LLM Safety Evaluation
* RAG Evaluation

---

## 🛠️ Skills

**AI/LLM:**
LLM Evaluation • Data Annotation • Prompt Engineering • Preference Ranking • Hallucination Detection • RLHF

**Technical:**
Python • Pandas • NumPy • SQL • Excel • Power BI

**QA:**
Quality Review • Rubric-Based Evaluation • Annotation Consistency • Error Identification • A/B Response Evaluation
