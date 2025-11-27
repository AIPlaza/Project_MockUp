# Workflow: Reporting Agent

## Role

The `Reporting_Agent` is a specialized agent responsible for synthesizing the results of the data analysis into a final, actionable report for stakeholders. Its role involves two key tasks: formulating conclusions and developing a strategic action plan.

## Inputs

1.  **`Statistical_Analysis_Report.md`:** The validated output from Phase 3. This is the primary source of information.
2.  **`INFORMACIÓN DEL ESTUDIO` block:** The original study information block from Phase 0, required for referencing the objectives.
3.  **`Methodological_Design_Document.md`:** The output from Phase 1, required for the "Conclusiones Metodológicas" section.

## Process

This is a two-step sequential process.

### Step 1: Formulate Conclusions

1.  **Receive Inputs:** The `Orchestrator_Agent` provides the `Statistical_Analysis_Report.md` and the `INFORMACIÓN DEL ESTUDIO` block.
2.  **Extract Specifications:** Parse the inputs to populate the `INFORMACIÓN PARA CONCLUSIONES` block in the conclusions prompt. This involves identifying objectives, main statistical findings, and key theoretical references used in the analysis report.
3.  **Load Tool 1:** Access the prompt template at `prompt_template_conclusions.md`.
4.  **Execute Prompt 1:** Execute the completed prompt to generate the `Conclusions.md` document.
5.  **Submit for Validation (Internal):** Pass the `Conclusions.md` to the `Orchestrator_Agent` to be checked against the first part of the `quality_checklist.md`.

### Step 2: Develop Action Plan

1.  **Receive Inputs:** The `Orchestrator_Agent` provides the validated `Conclusions.md` and the original context of the study.
2.  **Extract Specifications:** Parse the conclusions and context to populate the `CONTEXTO PARA LAS RECOMENDACIONES` block in the action plan prompt. This involves identifying the main weaknesses and strengths found in the conclusions.
3.  **Load Tool 2:** Access the prompt template at `prompt_template_action_plan.md`.
4.  **Execute Prompt 2:** Execute the completed prompt to generate the `Action_Plan.md` document.
5.  **Submit for Validation (Internal):** Pass the `Action_Plan.md` to the `Orchestrator_Agent` to be checked against the second part of the `quality_checklist.md`.

## Outputs

1.  **`Conclusions.md`:** A document detailing the conclusions of the study, structured by objective, and including emergent and methodological conclusions.
2.  **`Action_Plan.md`:** A strategic and tactical plan with concrete recommendations, timelines, and KPIs to address the findings of the study.
3.  **`Final_Research_Report.md`:** An assembled document, created by the `Orchestrator_Agent`, that combines all key artifacts into a single, cohesive report for the end-user.
