# Flujo de Trabajo: Agente de Reportes

## Rol

El `Agente_Reportes` es un agente especializado responsable de sintetizar los resultados del análisis de datos en un informe final y accionable para los interesados. Su rol implica dos tareas clave: formular conclusiones y desarrollar un plan de acción estratégico.

## Entradas

1.  **`Reporte_Analisis_Estadistico.md`:** El resultado validado de la Fase 3. Esta es la fuente principal de información.
2.  **Bloque `INFORMACIÓN DEL ESTUDIO`:** El bloque de información original del estudio de la Fase 0, necesario para hacer referencia a los objetivos.
3.  **`Documento_Diseno_Metodologico.md`:** El resultado de la Fase 1, necesario para la sección de "Conclusiones Metodológicas".

## Proceso

Este es un proceso secuencial de dos pasos.

### Paso 1: Formular Conclusiones

1.  **Recibir Entradas:** El `Agente_Orquestador` proporciona el `Reporte_Analisis_Estadistico.md` y el bloque `INFORMACIÓN DEL ESTUDIO`.
2.  **Extraer Especificaciones:** Analiza las entradas para rellenar el bloque `INFORMACIÓN PARA CONCLUSIONES` en el prompt de conclusiones. Esto implica identificar objetivos, principales hallazgos estadísticos y referencias teóricas clave utilizadas en el informe de análisis.
3.  **Cargar Herramienta 1:** Accede a la plantilla de prompt en `prompt_template_conclusions.md`.
4.  **Ejecutar Prompt 1:** Ejecuta el prompt completado para generar el documento `Conclusiones.md`.
5.  **Enviar para Validación (Interna):** Pasa el `Conclusiones.md` al `Agente_Orquestador` para que sea verificado contra la primera parte de la `lista_de_calidad.md`.

### Paso 2: Desarrollar Plan de Acción

1.  **Recibir Entradas:** El `Agente_Orquestador` proporciona el `Conclusiones.md` validado y el contexto original del estudio.
2.  **Extraer Especificaciones:** Analiza las conclusiones y el contexto para rellenar el bloque `CONTEXTO PARA LAS RECOMENDACIONES` en el prompt del plan de acción. Esto implica identificar las principales debilidades y fortalezas encontradas en las conclusiones.
3.  **Cargar Herramienta 2:** Accede a la plantilla de prompt en `prompt_template_action_plan.md`.
4.  **Ejecutar Prompt 2:** Ejecuta el prompt completado para generar el documento `Plan_de_Accion.md`.
5.  **Enviar para Validación (Interna):** Pasa el `Plan_de_Accion.md` al `Agente_Orquestador` para que sea verificado contra la segunda parte de la `lista_de_calidad.md`.

## Salidas

1.  **`Conclusiones.md`:** Un documento que detalla las conclusiones del estudio, estructurado por objetivo, e incluyendo conclusiones emergentes y metodológicas.
2.  **`Plan_de_Accion.md`:** Un plan estratégico y táctico con recomendaciones concretas, cronogramas e indicadores clave de rendimiento (KPIs) para abordar los hallazgos del estudio.
3.  **`Reporte_Final_Investigacion.md`:** Un documento ensamblado, creado by el `Agente_Orquestador`, que combina todos los artefactos clave en un único informe cohesivo para el usuario final.
