
# Q3 — LLM-Based ESG Message Triage

## 1. Overview

This folder contains the implementation and experimental evidence for **Question 3 of BUS5001 Assessment 3**.

The project investigates how a **Large Language Model (LLM)** can classify Environmental, Social and Governance (ESG) incident reports and produce structured outputs to support incident triage.

## 2. Implementation Environment

| Component | Technology |
|---|---|
| Platform | Google Colab |
| Programming Language | Python |
| LLM | Qwen/Qwen2.5-1.5B-Instruct |
| Hardware | NVIDIA T4 GPU |
| Input Data | Three synthetic ESG incident reports |
| Output Formats | JSON and CSV |

**Note:** All test incidents were synthetic. No real organisational or personal incident data was used.

## 3. Test Scenarios

| Incident ID | Incident Description | Expected ESG Category |
|---|---|---|
| ESG001 | Wastewater discharge incident | Environmental |
| ESG002 | Worker safety and excessive overtime concerns | Social |
| ESG003 | Undisclosed family relationship involving a supplier | Governance |

## 4. Experimental Approach

The practical investigation included:

1. Preparing synthetic ESG incident reports.
2. Testing rule-based classification.
3. Testing zero-shot LLM classification.
4. Evaluating original Qwen-generated responses.
5. Improving prompts to produce structured classifications.
6. Testing extended eight-field outputs.
7. Validating JSON formatting.
8. Evaluating classification consistency.
9. Exporting results into JSON and CSV files.

## 5. Key Experimental Findings

### 5.1 Improved Prompt Performance

The improved four-field Qwen prompt correctly classified **3 out of 3 incidents** into their expected ESG categories.

### 5.2 Extended Output Performance

The extended eight-field output correctly classified **2 out of 3 incidents**.

**Observed error:** Incident ESG002, involving worker safety and excessive overtime, was incorrectly classified as Environmental rather than Social.

### 5.3 JSON Validation

The structured-output validation succeeded for **3 out of 3 tested outputs**.

However, some raw responses contained Markdown code fences around JSON, requiring preprocessing before machine-readable use.

### 5.4 Classification Consistency

Classification consistency was observed in **2 out of 3 tested cases**.

This demonstrates that valid output formatting does not necessarily guarantee accurate or consistent ESG classification.

## 6. Evidence Files

The repository contains the experimental notebook, generated results, comparison files and supporting screenshots.

### Google Colab Notebook

- `BUS5001_Q3_ESG_LLM_Triage.ipynb`

### CSV Results

- `accuracy_summary.csv`
- `classification_comparison.csv`

### JSON Results

- `original_qwen_results.json`
- `improved_qwen_results.json`
- `json_validation_results.json`
- `rule_based_results.json`
- `zero_shot_results.json`

### Screenshots

- `HuggingFace_Screenshots/`

## 7. Critical Evaluation

### Strengths

- Demonstrated the feasibility of LLM-assisted ESG incident classification.
- Improved classification performance through prompt refinement.
- Produced structured outputs suitable for further processing.
- Enabled comparison between different classification approaches.

### Limitations

- Only three synthetic incidents were tested.
- Results cannot establish real-world classification accuracy.
- The model misclassified one incident in the extended-output experiment.
- Output consistency was imperfect.
- Raw JSON sometimes required formatting cleanup.
- Human verification would be required for practical deployment.

## 8. Conclusion

The experiment demonstrated that **prompt engineering can improve the quality of LLM-generated ESG classifications**.

However, classification errors, inconsistent outputs and the limited test dataset highlight the need for further evaluation before applying the approach to real-world ESG incident management.

## 9. Academic Integrity

AI-generated classifications were treated as experimental outputs rather than authoritative decisions.

The outputs were evaluated against predefined incident categories, and observed errors were retained to support transparent reporting.

