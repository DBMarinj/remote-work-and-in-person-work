# Brief del Proyecto: Análisis de Trabajo Remoto vs. Presencial y Salud Mental

## 1. Pregunta de negocio / análisis
¿Cómo se relacionan las modalidades de trabajo (remoto, híbrido o presencial), la carga laboral y los factores de bienestar (estrés, sueño, actividad física y aislamiento social) con la percepción de productividad y las condiciones de salud mental en la muestra analizada?

## 2. Quién decide
- **Audiencia / tomadores de decisión:** Líderes de Talento Humano (RR. HH.), jefaturas de operación y áreas de bienestar organizacional que evalúan políticas de modalidad laboral y prevención del desgaste.
- **Responsable del análisis:** Analista de datos del proyecto (revisión colaborativa en clase mediante Pull Request).

## 3. Fuente de datos
- Dataset público de análisis exploratorio (*Remote Work and Mental Health*), compuesto por **5,000 registros** y **20 columnas** (7 numéricas enteras y 13 categóricas/texto).

## 4. Alcance (qué SÍ incluye)
- Análisis exploratorio de datos (EDA) sobre las 5,000 filas disponibles.
- Comparación descriptiva entre modalidades de trabajo (`Work_Location`), roles, industrias y regiones frente a carga horaria, reuniones virtuales, estrés, sueño, aislamiento social y cambio de productividad.
- Identificación de valores nulos, categorías y posibles sesgos o anomalías en el archivo.

## 5. Qué NO incluye
- Diagnóstico clínico, asesoría médica individual ni inferencia causal definitiva sobre salud mental.
- Conexión a bases de datos transaccionales en producción ni pipelines de ingesta en tiempo real.
- Datos personales identificables (nombres, correos, documentos o información privada de personas reales).

## 6. Riesgos de calidad de datos
- **Valores faltantes:** `Mental_Health_Condition` tiene 3,804 valores no nulos (1,196 nulos) y `Physical_Activity` tiene 3,371 valores no nulos (1,629 nulos). Hay que aclarar si esos nulos representan ausencia de reporte, categoría no registrada o falta de respuesta.
- **Escalas y categorías sin diccionario oficial:** Columnas numéricas como `Work_Life_Balance_Rating`, `Social_Isolation_Rating` y `Company_Support_for_Remote_Work` requieren verificar su rango exacto (por ejemplo, 1 a 5) y variables como `Productivity_Change` o `Stress_Level` requieren revisar sus etiquetas exactas antes de agrupar.
- **Posibles valores atípicos o inconsistencias:** Revisar rangos lógicos en `Age`, `Hours_Worked_Per_Week`, `Years_of_Experience` y duplicidad o formato de `Employee_ID`.