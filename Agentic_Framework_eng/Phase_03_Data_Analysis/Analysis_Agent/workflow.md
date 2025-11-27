# Workflow: Analysis Agent

## Role

The `Analysis_Agent` is a specialized agent responsible for conducting a complete statistical analysis of the research data.

## Inputs

1.  **`DATOS RECOLECTADOS`:** A structured file (e.g., CSV, Markdown table) containing the raw data collected from the application of the `Questionnaire_Final.md`. The format should be a matrix of responses or a frequency table as exemplified in the prompt template.
2.  **Contextual Documents:**
    *   `Methodological_Design_Document.md`: To understand the variables, dimensions, and overall research context.
    *   `Questionnaire_Final.md`: To get the exact wording of the items for the report.

## Process

1.  **Receive Input:** The `Orchestrator_Agent` provides the raw data file and the contextual documents.
2.  **Extract Specifications:** Parse the contextual documents to extract the information required for the `INFORMACIÓN DEL ESTUDIO` block in the prompt template (Variable, Dimensiones, Sample Size, etc.).
3.  **Load Tool:** Access the prompt template at `prompt_template_analysis.md`.
4.  **Synthesize:**
    *   Populate the `INFORMACIÓN DEL ESTUDIO` block.
    *   Insert the raw data into the `DATOS RECOLECTADOS` section of the prompt.
5.  **Execute Prompt:** Execute the completed prompt to generate the full statistical analysis.
6.  **Format Output:** Name the output document `Statistical_Analysis_Report.md`. Ensure it follows the final report structure defined in the prompt, from "I. INTRODUCCIÓN AL ANÁLISIS" to "VIII. CONCLUSIONES PRELIMINARES".
7.  **Submit for Validation:** Pass the generated `Statistical_Analysis_Report.md` back to the `Orchestrator_Agent` for quality assurance.

## Outputs

1.  **`Statistical_Analysis_Report.md`:** A comprehensive document detailing the full statistical analysis, including:
    *   Analysis by Item, Dimension, and Variable.
    *   Recommended data visualizations.
    *   Cross-analysis (if applicable).
    *   Descriptive statistics.
    *   Written findings triangulated with the theoretical framework.
    *   A list of preliminary conclusions, strengths, and weaknesses.
