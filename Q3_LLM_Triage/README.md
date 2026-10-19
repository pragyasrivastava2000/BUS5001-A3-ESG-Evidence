
# Q3 — LLM-Based ESG Message Triage

**Subject:** BUS5001 — Cloud Platforms and Analytics  
**Assessment:** Assessment 3, Question 3  
**Technology:** Python, Google Colab, Hugging Face, Qwen LLM  
**Focus:** ESG Incident Classification and Operational Triage

---

## 1. Project Overview

This project investigates the feasibility of using a Large Language Model (LLM) to classify and triage Environmental, Social and Governance (ESG) operational incidents.

The proposed workflow aims to support organisations in processing incoming incident reports by identifying issue categories, assessing urgency, determining follow-up requirements and recommending appropriate escalation pathways.

The prototype was developed and tested using Python in Google Colab, with an open-source language model and three synthetic ESG incident scenarios.

The evaluation focuses on classification accuracy, prompt effectiveness, structured JSON output, consistency and operational limitations.

## 2. Objectives

The main objectives were to:

1. Develop and evaluate prompts for structured ESG incident classification.
2. Test an open-source LLM using realistic synthetic incident reports.
3. Compare LLM classifications against baseline approaches.
4. Assess JSON output quality and classification consistency.
5. Identify hallucination, bias, privacy and escalation risks.
6. Consider the feasibility of integrating the workflow into a cloud-based operational system.

## 3. Implementation Environment

| Component | Implementation |
|---|---|
| Development Platform | Google Colab |
| Programming Language | Python |
| LLM | Qwen/Qwen2.5-1.5B-Instruct |
| Model Ecosystem | Hugging Face |
| Runtime Hardware | NVIDIA T4 GPU |
| Input Data | Three synthetic ESG incident reports |
| Output Formats | JSON and CSV |
| Evaluation Methods | Baseline comparison, classification accuracy, JSON validation and consistency testing |

## 4. Test Dataset

Three synthetic ESG incidents were used to represent different operational reporting scenarios.

| Incident ID | Scenario | Expected Category |
|---|---|---|
| ESG001 | Wastewater discharge incident | Environmental |
| ESG002 | Worker safety and excessive overtime concerns | Social |
| ESG003 | Undisclosed family relationship involving a supplier | Governance |

These examples were selected to test the model across environmental, workplace and governance-related reporting situations.

The dataset was intentionally small for prototype evaluation and does not represent a comprehensive real-world benchmark.

## 5. Experimental Methodology

### 5.1 Baseline Classification

Baseline classification approaches were tested to provide a reference for evaluating the LLM.

The baseline results were compared with the model-generated classifications to identify differences and potential errors.

### 5.2 Initial LLM Testing

The Qwen model was tested using the synthetic ESG incidents.

Initial responses were examined for:

- Correct identification of ESG categories.
- Ability to interpret incident context.
- Structured output quality.
- Compliance with requested response formats.

### 5.3 Prompt Refinement

The prompt was refined to improve classification clarity and output structure.

An improved four-field classification format was tested before extending the output to additional operational fields.

### 5.4 Extended Structured Output

An eight-field output format was tested to examine the model's ability to provide more detailed operational triage information.

The intended fields were:

1. `issue_category`
2. `urgency`
3. `sentiment`
4. `followup_required`
5. `recommended_team`
6. `escalation_reason`
7. `data_sensitivity_risk`
8. `brief_summary`

### 5.5 JSON Validation and Consistency

The experiments also examined whether the model produced valid machine-readable outputs and whether classifications remained consistent.

Some raw responses included Markdown code fences around JSON, requiring additional cleaning before parsing.

## 6. Experimental Results

| Evaluation | Observed Result | Interpretation |
|---|---|---|
| Improved four-field classification | 3/3 correct | All three incidents matched their expected ESG categories |
| Extended eight-field classification | 2/3 correct | ESG002 was incorrectly classified as Environmental |
| Structured output validation | 3/3 successful | Tested outputs passed validation after the applicable processing |
| Classification consistency | 2/3 | Classification behaviour was not fully consistent |
| Export validation | Passed | Generated results were successfully exported into JSON and CSV formats |

**Important:** These results describe performance on the three selected synthetic incidents only. They should not be interpreted as general model accuracy.

### 6.1 Correct Classification Example

The improved four-field prompt correctly classified ESG001 as an Environmental incident, ESG002 as a Social incident and ESG003 as a Governance incident.

### 6.2 Misclassification Example

During extended eight-field testing, ESG002 was incorrectly classified as Environmental instead of Social.

This error illustrates that requesting more detailed output can introduce classification inconsistencies, even when the model produces a structured response.

### 6.3 Output Formatting

Some raw model responses included Markdown code fences around JSON.

This highlighted the need for output preprocessing, schema validation and error handling before integrating LLM responses into automated workflows.

## 7. Critical Evaluation

### 7.1 Strengths

- The model demonstrated the ability to interpret different ESG incident scenarios.
- Prompt refinement improved classification results in the selected tests.
- Structured outputs could support downstream operational processing.
- Baseline comparison provided a reference for evaluating model behaviour.
- JSON and CSV exports supported further analysis and documentation.

### 7.2 Limitations

- Only three synthetic incidents were evaluated.
- The model produced an incorrect ESG classification in extended-output testing.
- Classification consistency was imperfect.
- Valid JSON formatting did not guarantee correct classification.
- The small dataset did not permit meaningful conclusions about generalisation or demographic bias.
- The prototype was not connected to a live enterprise incident management system.

### 7.3 Operational Risks

**Hallucination:** The model may generate unsupported incident details or escalation recommendations.

**Misclassification:** Incorrect categories or urgency assessments may delay appropriate action.

**Data Protection:** Real incident reports may contain confidential employee, supplier or organisational information.

**Human Oversight:** High-risk incidents should be reviewed by authorised personnel rather than automatically actioned.

**Reliability:** Production use would require larger test datasets, monitoring, validation and defined escalation rules.

## 8. Proposed Azure Cloud Architecture

A potential cloud implementation could use the following components:

| Azure Component | Proposed Role |
|---|---|
| Azure Logic Apps | Receive and orchestrate incoming incident messages |
| Azure Functions | Validate inputs and process model outputs |
| Azure Machine Learning | Host and manage an appropriate classification model |
| Azure Blob Storage | Store approved incident records and outputs |
| Azure Monitor | Monitor workflow execution and operational errors |
| Microsoft Entra ID | Support identity and access management |
| Azure Key Vault | Secure application secrets and credentials |

### Conceptual Workflow

`Incident Submission → Logic Apps → Azure Functions → LLM Classification → JSON Validation → Risk-Based Human Review → Approved Storage or Escalation`

This architecture is a **proposed design**, not a deployed Azure implementation.

## 9. Repository Evidence

The Q3 evidence includes the experimental notebook and generated outputs.

### Notebook

- `BUS5001_Q3_ESG_LLM_Triage.ipynb`

### Result Files

- `accuracy_summary.csv`
- `classification_comparison.csv`
- `original_qwen_results.json`
- `improved_qwen_results.json`
- `json_validation_results.json`
- `rule_based_results.json`
- `zero_shot_results.json`

Supporting screenshots and additional experimental evidence are maintained alongside the implementation files.

## 10. Conclusion

The prototype demonstrated that an open-source LLM can support structured ESG incident classification under controlled experimental conditions.

Prompt refinement improved classification performance in the selected tests. However, the extended-output misclassification, inconsistent responses and formatting issues demonstrated important reliability limitations.

The approach is suitable for further controlled testing but is not sufficiently validated for autonomous production use.

A practical deployment would require expanded testing, schema enforcement, privacy controls, monitoring and human oversight for sensitive or high-priority incidents.
