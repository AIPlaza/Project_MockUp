# Flujo de Trabajo: Agente de Instrumentación

## Rol

El `Agente_Instrumentacion` es un agente especializado responsable de diseñar y redactar los instrumentos de recolección de datos según se especifica en el diseño metodológico.

## Entradas

1.  **`Documento_Diseno_Metodologico.md`:** El resultado validado de la Fase 1. El agente utilizará específicamente las siguientes secciones:
    *   `Técnicas e Instrumentos` (para confirmar el tipo de instrumento, ej., Cuestionario).
    *   `Población y Muestra` (para entender a la audiencia objetivo).
    *   Las `Variables` y sus `Dimensiones` que necesitan ser medidas.

## Proceso

1.  **Recibir Entrada:** El `Agente_Orquestador` proporciona el `Documento_Diseno_Metodologico.md`.
2.  **Extraer Especificaciones:** Analiza el documento de entrada para extraer la información clave requerida para el bloque `ESPECIFICACIONES DEL INSTRUMENTO` en la plantilla de prompt (Variable, Dimensiones, Población, etc.).
3.  **Cargar Herramienta:** Accede a la plantilla de prompt en `prompt_template_questionnaire.md`.
4.  **Sintetizar:** Rellena la sección `ESPECIFICACIONES DEL INSTRUMENTO` de la plantilla de prompt con la información extraída.
5.  **Ejecutar Prompt:** Ejecuta el prompt completado para generar el borrador del instrumento.
6.  **Formatear Salida:** Nombra el documento de salida `Borrador_Cuestionario.md`. Asegúrate de que incluya la estructura completa: Encabezado, Instrucciones, Ítems por dimensión y la Tabla de Especificaciones.
7.  **Enviar para Validación:** Pasa el `Borrador_Cuestionario.md` generado de vuelta al `Agente_Orquestador`, que gestionará el proceso de validación como se define en la lista de calidad (juicio de expertos, prueba piloto).

## Salidas

1.  **`Borrador_Cuestionario.md`:** Un borrador completo y bien estructurado del cuestionario, listo para su validación.
2.  **(Post-Validación) `Cuestionario_Final.md`:** La versión final del cuestionario después de incorporar la retroalimentación del proceso de validación.
