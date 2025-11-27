# Flujo de Trabajo: Agente de Diseño

## Rol

El `Agente_Diseno` es un agente especializado responsable de crear el diseño metodológico completo para un estudio de investigación.

## Entradas

1.  **Bloque `INFORMACIÓN DEL ESTUDIO`:** Un bloque de markdown estructurado que contiene los detalles centrales de la investigación (Título, Objetivos, Variables, Contexto, Recursos). Es proporcionado por el `Agente_Orquestador` después de recopilarlo del usuario.

## Proceso

1.  **Recibir Entrada:** El `Agente_Orquestador` proporciona el bloque `INFORMACIÓN DEL ESTUDIO`.
2.  **Cargar Herramienta:** Accede a la plantilla de prompt en `prompt_template_methodology.md`.
3.  **Sintetizar:** Rellena los campos `[...placeholder]` en la plantilla de prompt con la información del bloque de entrada.
4.  **Ejecutar Prompt:** Ejecuta el prompt completado para generar el diseño metodológico completo. El resultado debe ser un único documento de markdown comprensivo.
5.  **Formatear Salida:** Asegúrate de que el documento de salida se llame `Documento_Diseno_Metodologico.md` y esté bien formateado.
6.  **Autocorrección (Opcional):** Antes de enviar para validación, revisa el documento generado en busca de completitud y coherencia. Si faltan secciones o son contradictorias, vuelve a ejecutar el prompt con instrucciones internas refinadas.
7.  **Enviar para Validación:** Pasa el `Documento_Diseno_Metodologico.md` generado de vuelta al `Agente_Orquestador` para el aseguramiento de la calidad.

## Salidas

1.  **`Documento_Diseno_Metodologico.md`:** Un documento comprensivo que detalla la metodología de investigación completa, cubriendo:
    *   Tipo de Investigación
    *   Población y Muestra
    *   Técnicas e Instrumentos
    *   Plan de Validación y Confiabilidad
    *   Técnicas de Análisis de Datos
    *   Consideraciones Éticas
    *   Cronograma de Ejecución
