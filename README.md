
# BUS5001 Assessment 3 — ESG Automation and Responsible AI

## Project Overview

This repository contains practical implementation evidence, experimental outputs, screenshots, and supporting documentation for BUS5001 Assessment 3.

The assessment explores cloud-based sustainability automation, conversational AI, and responsible use of large language models.

The repository contains evidence for three practical components:

- **Q1:** EcoAssist sustainability incident reporting chatbot
- **Q3:** LLM-based ESG operational message triage
- **Q4:** NotebookLM for academic ESG research

**Q2**, the 2024 Snowflake cloud security incident analysis, is presented in the written assessment report.

## Repository Navigation

### Q1 — EcoAssist Chatbot

EcoAssist is a sustainability incident reporting chatbot developed using Google Dialogflow CX.

It supports five incident categories and demonstrates intent recognition, custom entities, parameter collection, conditional routing, critical escalation, report review, correction, and human handoff.

- [Q1 Implementation Screenshots](EcoAssist_Q1_Evidence/01_Implementation_Screenshots)
- [Q1 Chatbot Test Screenshots](EcoAssist_Q1_Evidence/02_Chatbot_Test_Screenshots)
- [Q1 Project Documentation](EcoAssist_Q1_Evidence/README.md)

Fifteen simulator scenarios (T01–T15) were executed, including critical incident escalation and error recovery.

### Q3 — LLM-Based ESG Message Triage

A Google Colab prototype using Qwen/Qwen2.5-1.5B-Instruct to classify three synthetic ESG operational messages.

The experiments compare basic, improved four-field, and eight-field prompts with rule-based and zero-shot classification baselines.

#### Key Results

| Experiment | Category accuracy |
|---|---|
| Basic Qwen prompt | 2/3 |
| Improved four-field Qwen prompt | 3/3 |
| Eight-field Qwen prompt | 2/3 |
| Keyword rule-based baseline | 3/3 |
| BART zero-shot baseline | 2/3 |

Additional findings:

- **Category–team consistency:** 2/3 for the eight-field outputs.
- **Raw JSON validity:** 0/3 due to Markdown code fences.
- **JSON schema validity after removing fences:** 3/3.
- The experiments use only three synthetic messages, so the results are illustrative rather than representative of production accuracy.

See the Q3 experiment files and README for supporting evidence.

### Q4 — NotebookLM ESG Research Assistant

NotebookLM was evaluated as a source-grounded research assistant using IFRS S1 and IFRS S2 overview pages from the IFRS Foundation.

Seven experiments were completed:

| Experiment | Feature evaluated |
|---|---|
| E01 | Source import |
| E02 | Source-grounded question answering |
| E03 | Academic summarisation |
| E04 | Cross-source comparison |
| E05 | Flashcards |
| E06 | Quiz generation |
| E07 | Mind mapping |

The evaluation considers accuracy, usefulness, citation verification, and limitations of source-grounded AI.

- [Q4 NotebookLM Evidence](Q4_NotebookLM)

## Evidence and Reproducibility

The repository provides screenshots, experimental outputs, and documentation supporting the assessment findings.

Q1 demonstrates a working Dialogflow CX conversational prototype, but does not implement live ticket creation or staff notifications.

Q3 uses synthetic messages and a small experimental sample. Its results should not be interpreted as production-level performance.

Q4 uses IFRS Foundation overview pages rather than the complete technical standards, so technical conclusions require verification against the original standards.

## Assessment Information

**Unit:** BUS5001  
**Assessment:** Assessment 3  
**Topic:** Cloud Platforms, ESG Automation and Responsible AI

The written report contains the complete analysis, evaluation, references, and recommendations. The Q1 executive demonstration video is provided separately through the report.
