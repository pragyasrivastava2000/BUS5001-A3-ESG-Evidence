
# BUS5001 — Assessment 3: Cloud Platforms and Analytics

**Project:** ESG Automation, LLM-Based Incident Triage and Cloud-Based Technology Evaluation

**Assessment:** BUS5001 — Assessment 3  
**Evidence Repository:** Practical Experiments, Implementation Results and Supporting Documentation

---

## 1. Repository Overview

This repository contains practical implementation evidence, experimental results and supporting documentation for Questions 3 and 4 of BUS5001 Assessment 3.

The assessment explores how cloud-based technologies and language models can support organisational sustainability operations, ESG incident management and academic research workflows.

The repository is organised into two main sections:

- **Q3 — LLM-Based ESG Message Triage**
- **Q4 — Google NotebookLM Evaluation**

Each section contains its own README with the experimental methodology, findings, critical evaluation and supporting evidence.

## 2. Repository Structure

```text
BUS5001-A3-ESG-Evidence/
│
├── README.md
│
├── Q3_LLM_Triage/
│   ├── README.md
│   ├── BUS5001_Q3_ESG_LLM_Triage.ipynb
│   ├── accuracy_summary.csv
│   ├── classification_comparison.csv
│   ├── original_qwen_results.json
│   ├── improved_qwen_results.json
│   ├── json_validation_results.json
│   ├── rule_based_results.json
│   ├── zero_shot_results.json
│   └── HuggingFace_Screenshots/
│
└── Q4_NotebookLM/
    ├── README.md
    └── Q4_NotebookLM_Evaluation_Log.md
```

Additional screenshots and supporting evidence can be added to the relevant folders.

## 3. Q3 — LLM-Based ESG Message Triage

**[View Q3 Experiments and Evidence](Q3_LLM_Triage/README.md)**

### Objective

Evaluate whether an open-source Large Language Model can classify ESG operational incidents and generate structured outputs to support organisational triage and escalation workflows.

### Technologies

- Python
- Google Colab
- Hugging Face
- Qwen/Qwen2.5-1.5B-Instruct
- JSON and CSV

### Experimental Scope

Three synthetic ESG incidents were tested:

| Incident | ESG Category |
|---|---|
| Wastewater discharge | Environmental |
| Worker safety and excessive overtime | Social |
| Undisclosed supplier family relationship | Governance |

### Key Results

| Evaluation | Result |
|---|---|
| Improved four-field classification | 3/3 correct |
| Extended eight-field classification | 2/3 correct |
| Structured output validation | 3/3 successful |
| Classification consistency | 2/3 |

The experiments demonstrated the potential of structured LLM classification while highlighting limitations involving accuracy, consistency and output formatting.

Further details are documented in the Q3 folder.

## 4. Q4 — Google NotebookLM Evaluation

**[View Q4 Experiments and Evidence](Q4_NotebookLM/README.md)**

### Objective

Evaluate the suitability of Google NotebookLM as a cloud-based academic research and learning assistant.

### Academic Scenario

A university student preparing an evidence-based briefing on IFRS S1 and IFRS S2 sustainability disclosure standards.

### Research Sources

- IFRS Foundation — IFRS S1 overview
- IFRS Foundation — IFRS S2 overview

### Experiments

| No. | Feature Evaluated |
|---|---|
| 1 | Source Import |
| 2 | Source-Grounded Question Answering |
| 3 | Academic Summarisation |
| 4 | Cross-Source Comparison |
| 5 | Flashcard Generation |
| 6 | Quiz Generation |
| 7 | Mind Map Generation |

### Key Findings

NotebookLM demonstrated useful capabilities for organising research materials, explaining concepts, preparing summaries and supporting independent revision.

The quiz experiment generated 10 questions, with five selected answers found consistent with the relevant IFRS concepts.

The mind map experiment successfully organised IFRS S1, IFRS S2, the four disclosure areas and the relationship between the standards.

Limitations included source dependence, simplified technical explanations and inconsistent visibility of citations in copied outputs.

Further details are documented in the Q4 folder.

## 5. Evidence and Reproducibility

The repository provides supporting materials for reviewing the experimental processes and findings.

Evidence includes:

- Implementation notebooks
- Test scenarios
- Classification results
- JSON and CSV outputs
- Experimental observations
- Supporting screenshots
- Critical evaluations

Results should be interpreted within the scope of the tests conducted rather than as general performance guarantees.

## 6. Overall Conclusion

The Q3 and Q4 experiments demonstrate different applications of cloud-enabled language technologies.

Q3 explores structured ESG incident classification for organisational operations, while Q4 examines academic research and learning support.

Both investigations highlight the importance of output accuracy, source quality, verification, responsible deployment and human oversight.

---

**BUS5001 — Assessment 3 | Supporting Experimental Evidence**
