# QuantHealth AI – Requirements

Live app: https://gundlururajasekhar.github.io/HealthMesh-AI/
Stage: MVP. Single-file, offline-first, privacy-first.

## Functional requirements
| ID | Requirement | Where |
|----|-------------|-------|
| FR-1 | Collect age, BP, glucose, weight, height, steps, sleep, adherence; save locally | Overview |
| FR-2 | Risk score 0-100 from a transparent rule engine | Overview |
| FR-3 | Explainable AI: percentage contribution per factor (BP, activity, sleep, glucose, BMI, age) | Overview |
| FR-4 | Six agents (Vitals, Risk, Lifestyle, Medication, Coach, Emergency) plus Care Plan; visible collaboration log | Overview |
| FR-5 | Personal care plan, daily coach summary, recovery score | Overview |
| FR-6 | Digital Health Twin what-if simulator (steps, sleep, weight) | Health Twin |
| FR-7 | 7-day and 30-day risk forecast chart | Health Twin |
| FR-8 | Report analyzer: parse pasted lab text, flag High/Low, suggest actions | Reports |
| FR-9 | Doctor Copilot: 30-second handoff and FHIR R4 Observation bundle | Doctor Copilot |
| FR-10 | Emergency checks for stroke, heart attack, diabetic emergency | Emergency |
| FR-11 | Simulated fall workflow (agent, caregiver, hospital, location) | Emergency |
| FR-12 | Validation dashboard: accuracy, precision, recall, F1, AUC on synthetic data | Validation |
| FR-13 | Voice coach: speech output and, where supported, speech input | Voice Coach |
| FR-15 | Optional live Gemini mode: user-supplied key, anonymous metrics only, session-only key, offline fallback on error | Gemini AI |
| FR-14 | Clinical safety notice always visible | Footer |

## Non-functional requirements
- Works with no network, no API key, no backend. Gemini mode is opt-in.
- Data stays in the browser (localStorage); nothing is transmitted.
- Responsive from 360 px, keyboard focusable, light and dark themes, reduced-motion respected.
- Loads as one HTML file under 50 KB.

## Out of scope (MVP)
Server-side LLM proxy, live wearable sync, real alerts, clinical validation, diagnosis.

## Acceptance
1. Changing any input updates risk, breakdown, plan, twin, doctor summary immediately.
2. Breakdown percentages total 100.
3. Sample report flags HbA1c, LDL, total cholesterol and fasting glucose as High.
4. Selecting a FAST symptom shows a stroke warning.
