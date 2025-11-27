# Workflow: Instrumentation Agent

## Role

The `Instrumentation_Agent` is a specialized agent responsible for designing and drafting the data collection instruments as specified in the methodological design.

## Inputs

1.  **`Methodological_Design_Document.md`:** The validated output from Phase 1. The agent will specifically use the following sections:
    *   `Técnicas e Instrumentos` (to confirm the instrument type, e.g., Cuestionario).
    *   `Población y Muestra` (to understand the target audience).
    *   The `Variables` and their `Dimensiones` which need to be measured.

## Process

1.  **Receive Input:** The `Orchestrator_Agent` provides the `Methodological_Design_Document.md`.
2.  **Extract Specifications:** Parse the input document to extract the key information required for the `ESPECIFICACIONES DEL INSTRUMENTO` block in the prompt template (Variable, Dimensiones, Población, etc.).
3.  **Load Tool:** Access the prompt template at `prompt_template_questionnaire.md`.
4.  **Synthesize:** Populate the `ESPECIFICACIONES DEL INSTRUMENTO` section of the prompt template with the extracted information.
5.  **Execute Prompt:** Execute the completed prompt to generate the draft instrument.
6.  **Format Output:** Name the output document `Questionnaire_Draft.md`. Ensure it includes the full structure: Header, Instructions, Items per dimension, and the Specification Table.
7.  **Submit for Validation:** Pass the generated `Questionnaire_Draft.md` back to the `Orchestrator_Agent`, which will manage the validation process as defined in the quality checklist (expert judgment, pilot testing).

## Outputs

1.  **`Questionnaire_Draft.md`:** A comprehensive, well-structured draft of the questionnaire, ready for validation.
2.  **(Post-Validation) `Questionnaire_Final.md`:** The final version of the questionnaire after incorporating feedback from the validation process.
