# Quality Checklist: Data Collection Instrument

## Objective

To ensure the drafted instrument (`Questionnaire_Draft.md`) is valid, reliable, and appropriate for the target population before it is finalized and applied. The validation process involves multiple steps, managed by the `Orchestrator_Agent`.

---

### Step 1: Content Validation (Juicio de Expertos)

**Action:** The `Orchestrator_Agent` must send the `Questionnaire_Draft.md` to 3-5 human experts whose profiles match those defined in the `Methodological_Design_Document.md`. The agent will request them to evaluate the instrument based on the following criteria.

- [ ] **Pertinence:** Do the items actually measure the intended dimension and indicators?
- [ ] **Clarity:** Is the language of each item clear, direct, and unambiguous for the target population?
- [ ] **Coherence:** Is there a logical flow and consistency throughout the instrument?
- [ ] **Adequacy:** Are the instructions, format, and length appropriate for the context in which the instrument will be applied?
- [ ] **Sufficiency:** Are there enough items to cover each dimension adequately? (As per the `DISTRIBUCIÓN ÓPTIMA` in the prompt).

**Outcome:** Collate feedback from experts. If significant changes are required, send the feedback to the `Instrumentation_Agent` to generate a revised draft. Repeat until experts approve.

---

### Step 2: Pilot Test

**Action:** Once content validation is passed, the `Orchestrator_Agent` must coordinate a pilot test as defined in the `Methodological_Design_Document.md`.

- [ ] **Administer Instrument:** Apply the questionnaire to a small, representative sample (5-10 participants) from the target population.
- [ ] **Gather Feedback:**
    - [ ] Collect data on the time taken to complete the instrument.
    - [ ] Interview participants to identify any items that were confusing, ambiguous, or difficult to answer.
- [ ] **Analyze Pilot Data:**
    - [ ] If quantitative, perform a preliminary reliability analysis (e.g., Cronbach's Alpha). The result must meet the predefined criterion (e.g., α ≥ 0.70).

**Outcome:** Based on the feedback and analysis, determine if further revisions are needed. If so, loop back to the `Instrumentation_Agent`.

---

### Step 3: Final Review

- [ ] **Readability & Formatting:** Check for clear, legible font, adequate spacing, and professional presentation.
- [ ] **Accessibility:** If digital, ensure it meets basic accessibility standards.
- [ ] **Cultural Sensitivity:** Final check to ensure no language or examples could be misinterpreted or considered inappropriate by the target population.
- [ ] **Anonymity & Ethics:** Confirm that the header and closing sections correctly state the ethical guarantees (confidentiality, academic use only).

---

### Validation Verdict

- [ ] **Approved for Finalization:** The instrument has successfully passed all validation stages. The `Instrumentation_Agent` can now produce the `Questionnaire_Final.md`.
- [ ] **Rejected:** The instrument has failed a critical validation step and requires significant rework. (Provide detailed feedback from the failed step to the `Orchestrator_Agent`).

**Feedback/Required Revisions:**
(Summary of feedback from experts or pilot test participants)
1.  `...`
2.  `...`
3.  `...`
