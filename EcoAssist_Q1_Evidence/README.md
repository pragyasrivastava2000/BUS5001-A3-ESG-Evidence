
# Q1 — EcoAssist: ESG Sustainability Incident Reporting Chatbot

## Project Overview

EcoAssist is a sustainability incident reporting chatbot developed using **Google Dialogflow CX** for **BUS5001 Assessment 3 — Question 1**.

The chatbot helps employees report sustainability-related incidents through a structured conversation. It demonstrates natural language recognition, parameter collection, conditional routing, critical incident escalation, report review, correction, and human handoff.

## 1. Supported Incident Categories

EcoAssist supports five incident categories:

1. Water Leak
2. Energy Waste
3. Waste Contamination
4. Hazardous Spill
5. Accessibility Barrier

## 2. Technical Implementation

| Component | Implementation |
|---|---|
| Platform | Google Dialogflow CX |
| Cloud region | Australia (Sydney) |
| Language | English |
| Custom entities | 6 |
| Custom intents | 7 |
| Required parameters | `incident_type`, `campus_location`, `severity_level` |
| Critical escalation | Conditional routing with `priority = URGENT` |
| Report confirmation | Review Report page |
| Error handling | Fallback prompts and human handoff |
| Cancellation and restart | Session parameter clearing |

### Key Functionalities

- **Natural language recognition:** Identifies reporting requests using custom intents and annotated training phrases.
- **Structured information collection:** Captures incident type, campus location, and severity.
- **Slot filling:** Requests only missing information.
- **Critical escalation:** Identifies critical incidents and displays immediate safety guidance.
- **Report review:** Allows users to confirm or correct information before submission.
- **Fallback handling:** Provides clarification prompts and human handoff after repeated unsuccessful inputs.
- **Cancellation and restart:** Clears session parameters to prevent information from carrying into a new report.

## 3. Implementation Screenshots

**[View All Implementation Screenshots](https://github.com/pragyasrivastava2000/BUS5001-A3-ESG-Evidence/tree/main/EcoAssist_Q1_Evidence/01_Implementation_Screenshots)**

These screenshots document the backend configuration of EcoAssist in Dialogflow CX.

| Screenshot | Description |
|---|---|
| D01 | Complete conversation flow canvas |
| D02a–D02b | Custom entities and incident type values |
| D03 | Configured intents |
| D04a–D04b | Training phrases and parameter extraction |
| D05 | Report Details page |
| D06a–D06b | Required parameters and reprompt handlers |
| D07a–D07b | Critical condition and URGENT priority preset |
| D08 | Report Details conditional routes |
| D09a–D09b | Start Page routes and event handlers |
| D10 | Apply Changes routes |
| D11a–D11b | Review summary and confirmation routes |
| D12 | Cancellation parameter presets |

## 4. Chatbot Testing Screenshots

**[View All Chatbot Test Screenshots](https://github.com/pragyasrivastava2000/BUS5001-A3-ESG-Evidence/tree/main/EcoAssist_Q1_Evidence/02_Chatbot_Test_Screenshots)**

Fifteen simulator scenarios (T01–T15) were executed to evaluate the chatbot's functionality.

| Test ID | Test scenario |
|---|---|
| T01 | Greeting and initial interaction |
| T02 | Step-by-step incident reporting |
| T03 | Single-message information collection |
| T04 | Missing-field prompts |
| T05 | Critical hazardous spill escalation |
| T06 | Critical severity synonym recognition |
| T07 | Single-field report correction |
| T08 | Multiple-field report correction |
| T09 | Mid-conversation correction |
| T10 | Fallback and clarification |
| T11 | Repeated invalid input and human handoff |
| T12 | Human handoff request |
| T13 | Additional conversation recovery testing |
| T14 | Report cancellation |
| T15 | Report restart |

### Critical Incident Demonstration — T05

The T05 scenario demonstrates a hazardous chemical spill reported in the Library.

The chatbot:

1. Recognises the hazardous spill category and location.
2. Requests the missing severity level.
3. Recognises critical severity.
4. Activates the urgent escalation pathway.
5. Displays immediate safety guidance.
6. Assigns `priority = URGENT`.
7. Presents the report summary for confirmation.
8. Completes the prototype submission flow.

The T05 screenshots are also included in the assessment report as **Figures 4a and 4b**.

## 5. Testing and Evaluation

The chatbot was evaluated for:

- Correct intent recognition
- Accurate entity and parameter extraction
- Appropriate conditional routing
- Critical incident escalation
- Report confirmation and correction
- Fallback recovery and human handoff
- Cancellation and restart behaviour

Testing identified issues with certain user phrases, route configuration, safety messaging, and confirmation recognition. These were addressed through iterative configuration and retesting.

## 6. Implementation Limitations

EcoAssist is a **functional conversational prototype**, not a production incident management system.

The current implementation:

- Does not create real service tickets.
- Does not send live notifications to facilities staff.
- Does not integrate with a production ESG dashboard.
- Has not been fully evaluated for multilingual or voice-based interaction.

Future integration with ticketing systems, notifications, and ESG reporting dashboards could support operational deployment.

## 7. Assessment Evidence

This folder contains supporting evidence for **BUS5001 Assessment 3 — Question 1**.

The written assessment report provides the design rationale, ethical considerations, testing analysis, and recommendations.

The executive demonstration video is submitted separately through the assessment report.
