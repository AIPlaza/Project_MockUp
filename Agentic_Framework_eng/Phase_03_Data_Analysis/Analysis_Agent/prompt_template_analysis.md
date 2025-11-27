## 📊 PROMPT: Análisis Estadístico de Datos

```
Actúa como un estadístico experto. Analiza los siguientes datos de mi
investigación y genera un informe completo:

┌─────────────────────────────────────────────────────────────┐
│ INFORMACIÓN DEL ESTUDIO                                      │
├─────────────────────────────────────────────────────────────┤
│ Variable analizada: [Nombre]                                │
│ Dimensiones: [Lista]                                        │
│ Instrumento: [Tipo]                                         │
│ Escala utilizada: [Descripción]                             │
│ Tamaño de muestra (n): [Número]                            │
└─────────────────────────────────────────────────────────────┘

📊 DATOS RECOLECTADOS:

[Pegar aquí la matriz de datos o tabla de frecuencias]

Ejemplo de formato:

| Ítem | S | CS | N | Total |
|------|---|----|----|-------|
| 1    | 12| 8  | 5  | 25    |
| 2    | 15| 7  | 3  | 25    |
| ...  |   |    |    |       |

🔍 ANÁLISIS REQUERIDO:

1. 📋 ANÁLISIS POR ÍTEM
   
   Para cada ítem, calcula:
   
   ┌──────────────────────────────────────────────────────┐
   │ ÍTEM #1: [Texto del ítem]                           │
   ├──────────────────────────────────────────────────────┤
   │                                                       │
   │ Frecuencias absolutas:                               │
   │ • Siempre (S): [n] respuestas                       │
   │ • Casi Siempre (CS): [n] respuestas                 │
   │ • Nunca (N): [n] respuestas                         │
   │                                                       │
   │ Frecuencias relativas:                               │
   │ • Siempre: [%]                                      │
   │ • Casi Siempre: [%]                                 │
   │ • Nunca: [%]                                        │
   │                                                       │
   │ Moda: [Categoría más frecuente]                    │
   │                                                       │
   │ Interpretación:                                      │
   │ [Análisis en lenguaje natural de lo que significa   │
   │ esta distribución de respuestas]                    │
   │                                                       │
   │ Gráfico recomendado: [Barras/Pastel]               │
   └──────────────────────────────────────────────────────┘

2. 📊 ANÁLISIS POR DIMENSIÓN
   
   Agrupa los ítems por dimensión y calcula:
   
   ╔═══════════════════════════════════════════════════════╗
   ║ DIMENSIÓN: [Nombre]                                   ║
   ║ Ítems incluidos: [Lista de números de ítems]         ║
   ╠═══════════════════════════════════════════════════════╣
   ║                                                       ║
   ║ Tabla resumen:                                        ║
   ║                                                       ║
   ║ | Ítem | S | CS | N | Tendencia |                   ║
   ║ |------|---|----|----|-----------|                   ║
   ║ | X    | % | %  | %  | [Alta/    |                   ║
   ║ |      |   |    |    |  Media/   |                   ║
   ║ |      |   |    |    |  Baja]    |                   ║
   ║                                                       ║
   ║ Promedio de la dimensión:                            ║
   ║ • % en categoría positiva (S + CS)                   ║
   ║ • % en categoría negativa (N)                        ║
   ║                                                       ║
   ║ Interpretación general de la dimensión:              ║
   ║ [Análisis integrado de todos los ítems de esta      ║
   ║ dimensión, identificando fortalezas y debilidades]  ║
   ║                                                       ║
   ║ Ítems críticos (con mayor % en "Nunca"):            ║
   ║ • Ítem #X: [descripción]                            ║
   ║ • Ítem #Y: [descripción]                            ║
   ║                                                       ║
   ╚═══════════════════════════════════════════════════════╝

3. 🎯 ANÁLISIS POR VARIABLE
   
   Integra todas las dimensiones:
   
   ┌────────────────────────────────────────────────────────┐
   │ VARIABLE: [Nombre completo]                            │
   ├────────────────────────────────────────────────────────┤
   │                                                         │
   │ Resumen por dimensiones:                               │
   │                                                         │
   │ | Dimensión | Items | S% | CS% | N% | Valoración |    │
   │ |-----------|-------|----|----|----|-----------   │    │
   │ | Dim 1     | 1-6   |    |    |    | [Alta/...]   │    │
   │ | Dim 2     | 7-12  |    |    |    | [Alta/...]   │    │
   │                                                         │
   │ Promedio general de la variable:                       │
   │ • Positivo (S + CS): [%]                              │
   │ • Negativo (N): [%]                                   │
   │                                                         │
   │ Dimensión más fuerte: [Nombre y justificación]        │
   │ Dimensión más débil: [Nombre y justificación]         │
   │                                                         │
   │ INTERPRETACIÓN GENERAL:                                │
   │ [Análisis comprehensivo del estado de esta variable   │
   │ en la organización, basado en todos los datos         │
   │ recolectados. Relaciona con el marco teórico.]        │
   │                                                         │
   │ HALLAZGOS PRINCIPALES:                                 │
   │ 1. [Hallazgo 1]                                       │
   │ 2. [Hallazgo 2]                                       │
   │ 3. [Hallazgo 3]                                       │
   │                                                         │
   │ ÁREAS DE MEJORA IDENTIFICADAS:                        │
   │ • [Área 1 con base en los ítems con mayores          │
   │   porcentajes en "Nunca"]                            │
   │ • [Área 2]                                            │
   │                                                         │
   └────────────────────────────────────────────────────────┘

4. 📈 VISUALIZACIONES RECOMENDADAS
   
   Genera especificaciones para:
   
   A) GRÁFICO DE BARRAS POR DIMENSIÓN
   ```
   Eje X: Dimensiones (Dim1, Dim2, Dim3...)
   Eje Y: Porcentaje (0-100%)
   Barras apiladas con:
   • Verde: Siempre
   • Amarillo: Casi Siempre
   • Rojo: Nunca
   
   Título: "Distribución de respuestas por dimensión"
   ```
   
   B) GRÁFICO DE TORTA/PASTEL GENERAL
   ```
   Segmentos:
   • Siempre: [%] (Verde)
   • Casi Siempre: [%] (Amarillo)
   • Nunca: [%] (Rojo)
   
   Título: "Percepción general sobre [Variable]"
   ```
   
   C) DIAGRAMA DE PARETO (80-20)
   ```
   Identifica el 20% de ítems que concentran el 80%
   de respuestas negativas ("Nunca")
   
   Esto permite priorizar acciones de mejora
   ```

5. 🔍 ANÁLISIS CRUZADO (si aplica)
   
   Relaciona variables demográficas con respuestas:
   
   | Dimensión | Grupo A | Grupo B | Diferencia | Sig. |
   |-----------|---------|---------|------------|------|
   | Dim 1     | X%      | Y%      | ±Z%        | Sí/No|
   
   Ejemplos:
   • Por antigüedad en la empresa
   • Por nivel educativo
   • Por área de trabajo
   • Por género (si es relevante éticamente)

6. 📊 ESTADÍSTICA DESCRIPTIVA AVANZADA
   
   Si usaste escala Likert 5 puntos (1-5), calcula:
   
   ┌──────────────────────────────────────────────┐
   │ Media aritmética (μ): [valor]               │
   │ Mediana (Me): [valor]                        │
   │ Moda (Mo): [valor]                           │
   │ Desviación estándar (σ): [valor]            │
   │ Varianza (σ²): [valor]                       │
   │ Coeficiente de variación (CV): [%]          │
   └──────────────────────────────────────────────┘
   
   Interpretación de la desviación estándar:
   • σ < 1: Alta homogeneidad en respuestas
   • σ ≈ 1-2: Dispersión moderada
   • σ > 2: Alta heterogeneidad

7. 📝 REDACCIÓN DE HALLAZGOS
   
   Redacta en prosa académica cada hallazgo:
   
   "En relación a la dimensión [nombre], se observó que
   el [X%] de los participantes indicó [categoría de respuesta],
   lo cual según [Autor, año] sugiere que [interpretación teórica].
   Este resultado concuerda/contrasta con lo encontrado por
   [antecedente], quien reportó [dato].
   
   Los ítems con mayor porcentaje negativo fueron el #X
   ([tema]) con [%] y el #Y ([tema]) con [%], lo que evidencia
   la necesidad de [acción recomendada]."

8. 🔗 TRIANGULACIÓN CON MARCO TEÓrico
   
   Para cada dimensión, relaciona los hallazgos con:
   
   ┌──────────────────────────────────

   ────────────┐
   │ Dimensión: [nombre]                          │
   │ Resultado: [resumen estadístico]             │
   │                                               │
   │ Según [Autor, año]: "[cita]"                 │
   │                                               │
   │ Análisis: El resultado obtenido              │
   │ concuerda/contrasta con lo planteado por    │
   │ el autor porque [explicación].               │
   │                                               │
   │ Implicaciones: Este hallazgo sugiere que    │
   │ la organización [interpretación práctica].  │
   └──────────────────────────────────────────────┘

💡 FORMATO FINAL DEL INFORME:

Presenta el análisis siguiendo esta estructura:

I. INTRODUCCIÓN AL ANÁLISIS
II. CARACTERIZACIÓN DE LA MUESTRA
III. ANÁLISIS POR VARIABLE E INDICADOR
    A. Variable 1: [nombre]
       ├── Dimensión 1.1
       ├── Dimensión 1.2
       └── Síntesis de la variable
    B. Variable 2: [nombre]
       └── [similar]
IV. ANÁLISIS INTEGRADO
V. PRINCIPALES HALLAZGOS
VI. FORTALEZAS IDENTIFICADAS
VII. DEBILIDADES IDENTIFICADAS
VIII. CONCLUSIONES PRELIMINARES
```
