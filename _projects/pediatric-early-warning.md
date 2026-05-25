---
layout: page
title: Pediatric Early Warning Score
description: Transformer-based models for predicting clinical deterioration in pediatric patients.
img:
importance: 3
category: social-impact
related_publications: false
---

In collaboration with **Children's Healthcare of Atlanta (CHOA)** and the
**Georgia Tech Pediatric Technology Center**, we develop machine learning systems
for **pediatric early warning** — predicting clinical deterioration before it becomes
life-threatening, enabling timely intervention in hospital settings.

**Problem:** Existing Pediatric Early Warning Scores (PEWS) rely on hand-crafted rules
applied to discrete vital sign thresholds. They miss subtle temporal patterns in
continuous physiological data and generate high false-alarm rates that contribute to
alarm fatigue.

**Our approach:** We apply **transformer-based sequence models** to continuous streams
of physiological signals (heart rate, respiratory rate, SpO₂, blood pressure) from
pediatric patients in CHOA's electronic health records. The model learns to identify
deterioration signatures hours before clinical events, providing interpretable risk
trajectories to clinicians.

**Key directions:**
- Transformer architectures for irregularly-sampled clinical time series
- Calibrated uncertainty quantification for high-stakes clinical decisions
- Integration of structured (vitals) and unstructured (nursing notes) EHR data
- Alarm optimization to balance sensitivity against false-alarm burden
- Prospective evaluation and deployment at CHOA

**Impact:** Improved early warning could reduce preventable PICU admissions and
cardiac arrests in pediatric wards, directly affecting patient outcomes at one of
the largest pediatric healthcare systems in the United States.

*This is an active collaboration. Results forthcoming.*
