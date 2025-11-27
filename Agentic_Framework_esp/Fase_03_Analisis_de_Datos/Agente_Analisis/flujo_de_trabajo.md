# Flujo de Trabajo: Agente de Análisis

## Rol

El `Agente_Analisis` es un agente especializado responsable de realizar un análisis estadístico completo de los datos de la investigación.

## Entradas

1.  **`DATOS RECOLECTADOS`:** Un archivo estructurado (ej. CSV, tabla de Markdown) que contiene los datos crudos recopilados de la aplicación del `Cuestionario_Final.md`. El formato debe ser una matriz de respuestas o una tabla de frecuencias como se ejemplifica en la plantilla de prompt.
2.  **Documentos de Contexto:**
    *   `Documento_Diseno_Metodologico.md`: Para entender las variables, dimensiones y el contexto general de la investigación.
    *   `Cuestionario_Final.md`: Para obtener la redacción exacta de los ítems para el informe.

## Proceso

1.  **Recibir Entrada:** El `Agente_Orquestador` proporciona el archivo de datos crudos y los documentos de contexto.
2.  **Extraer Especificaciones:** Analiza los documentos de contexto para extraer la información requerida para el bloque `INFORMACIÓN DEL ESTUDIO` en la plantilla de prompt (Variable, Dimensiones, Tamaño de la Muestra, etc.).
3.  **Cargar Herramienta:** Accede a la plantilla de prompt en `prompt_template_analysis.md`.
4.  **Sintetizar:**
    *   Rellena el bloque `INFORMACIÓN DEL ESTUDIO`.
    *   Inserta los datos crudos en la sección `DATOS RECOLECTADOS` del prompt.
5.  **Ejecutar Prompt:** Ejecuta el prompt completado para generar el análisis estadístico completo.
6.  **Formatear Salida:** Nombra el documento de salida `Reporte_Analisis_Estadistico.md`. Asegúrate de que siga la estructura del informe final definida en el prompt, desde "I. INTRODUCCIÓN AL ANÁLISIS" hasta "VIII. CONCLUSIONES PRELIMINARES".
7.  **Enviar para Validación:** Pasa el `Reporte_Analisis_Estadistico.md` generado de vuelta al `Agente_Orquestador` para el aseguramiento de la calidad.

## Salidas

1.  **`Reporte_Analisis_Estadistico.md`:** Un documento comprensivo que detalla el análisis estadístico completo, incluyendo:
    *   Análisis por Ítem, Dimensión y Variable.
    *   Visualizaciones de datos recomendadas.
    *   Análisis cruzado (si aplica).
    *   Estadísticas descriptivas.
    *   Hallazgos escritos triangulados con el marco teórico.
    *   Una lista de conclusiones preliminares, fortalezas y debilidades.
