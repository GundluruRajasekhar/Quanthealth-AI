# QuantHealth AI

Multi-agent, explainable, offline-first preventive healthcare MVP.
(Earlier names: HealthGuard AI, HealthMesh AI, CareFusion AI.)

**Live:** https://gundlururajasekhar.github.io/HealthMesh-AI/

## What it does
- **Agent mesh**: Vitals, Risk, Lifestyle, Medication, Coach and Emergency agents report to a Care Plan agent; run it and watch the messages.
- **Explainable risk score**: every factor shows its percentage contribution.
- **Digital Health Twin 2.0**: what-if sliders (steps, sleep, weight) with 7-day and 30-day forecast.
- **Report analyzer**: paste lab text, get High/Low flags and suggestions.
- **Doctor Copilot**: handoff summary plus FHIR R4 Observation JSON.
- **Emergency intelligence**: stroke, heart attack and diabetic warnings, plus a simulated fall workflow.
- **Validation page**: accuracy, precision, recall, F1, AUC computed live on synthetic profiles.
- **Live Gemini mode (new, optional)**: paste a Gemini API key to get real Gemini answers about your profile or pasted report; sends anonymous numbers only and falls back to the offline coach on failure.
- **Voice coach**: spoken answers about your risk, steps, sleep, medication and BP.

## Run
Open `index.html` in any browser, or deploy the folder to GitHub Pages. No install, no API key.

## Files
`index.html` (app) · `requirements.md` · `readme.md` · `tasks.md`

## Honest limitations
- The default agents are rule-based and run on-device; Gemini is used only when you add a key.
- Gemini mode uses a key in the browser, fine for demos; production should proxy through a backend.
- Wearable sync and hospital alerts are simulated.
- Validation metrics test the scoring engine on synthetic data, not clinical accuracy.
- OCR is replaced by pasted text.

## Roadmap to full marks
Gemini/Azure OpenAI backend for report analysis, Fitbit/Google Fit sync, clinician pilot, real validation dataset, PDF upload.

## Clinical safety notice
QuantHealth AI provides educational insights and risk awareness only. It does not diagnose or treat. Review all outputs with a qualified professional. In an emergency call your local emergency number.
