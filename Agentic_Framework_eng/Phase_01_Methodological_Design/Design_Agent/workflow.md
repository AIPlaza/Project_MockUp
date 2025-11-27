# Workflow: Design Agent

## Role

The `Design_Agent` is a specialized agent responsible for creating the complete methodological design for a research study.

## Inputs

1.  **`INFORMACIÓN DEL ESTUDIO` Block:** A structured markdown block containing the core details of the research (Title, Objectives, Variables, Context, Resources). This is provided by the `Orchestrator_Agent` after gathering it from the user.

## Process

1.  **Receive Input:** The `Orchestrator_Agent` provides the `INFORMACIÓN DEL ESTUDIO` block.
2.  **Load Tool:** Access the prompt template at `prompt_template_methodology.md`.
3.  **Synthesize:** Populate the `[...placeholder]` fields in the prompt template with the information from the input block.
4.  **Execute Prompt:** Execute the completed prompt to generate the full methodological design. The output should be a single, comprehensive markdown document.
5.  **Format Output:** Ensure the output document is named `Methodological_Design_Document.md` and is well-formatted.
6.  **Self-Correction (Optional):** Before submitting for validation, review the generated document for completeness and coherence. If sections are missing or contradictory, re-run the prompt with refined internal instructions.
7.  **Submit for Validation:** Pass the generated `Methodological_Design_Document.md` back to the `Orchestrator_Agent` for quality assurance.

## Outputs

1.  **`Methodological_Design_Document.md`:** A comprehensive document detailing the full research methodology, covering:
    *   Type of Research
    *   Population and Sample
    *   Techniques and Instruments
    *   Validation and Reliability Plan
    *   Data Analysis Techniques
    *   Ethical Considerations
    *   Execution Timeline
