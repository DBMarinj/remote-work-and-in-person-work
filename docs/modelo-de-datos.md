# Modelo de Datos del Dataset

Este proyecto trabaja sobre **un archivo tabular (dataset)** con **5,000 filas** y **20 columnas**, no sobre una base de datos normalizada con múltiples tablas. A nivel lógico, las columnas se agrupan por temática para facilitar su lectura y análisis.

## Diccionario de columnas

| # | Columna | Tipo en pandas | Significado en el dataset | Agrupación temática |
|---|---|---|---|---|
| 0 | `Employee_ID` | `object` | Identificador alfanumérico del registro/empleado en el dataset. | Identificación |
| 1 | `Age` | `int64` | Edad del trabajador en años. | Perfil demográfico |
| 2 | `Gender` | `object` | Género reportado en el registro. | Perfil demográfico |
| 3 | `Region` | `object` | Región geográfica asociada al registro. | Perfil demográfico |
| 4 | `Job_Role` | `object` | Rol o cargo desempeñado. | Contexto laboral |
| 5 | `Industry` | `object` | Sector o industria del trabajador. | Contexto laboral |
| 6 | `Years_of_Experience` | `int64` | Años de experiencia laboral acumulada. | Contexto laboral |
| 7 | `Work_Location` | `object` | Modalidad de trabajo (ej. remoto, híbrido, presencial). | Dinámica y carga laboral |
| 8 | `Hours_Worked_Per_Week` | `int64` | Horas trabajadas por semana. | Dinámica y carga laboral |
| 9 | `Number_of_Virtual_Meetings` | `int64` | Cantidad de reuniones virtuales registradas. | Dinámica y carga laboral |
| 10 | `Company_Support_for_Remote_Work` | `int64` | Calificación numérica del soporte empresarial para trabajo remoto. | Dinámica y carga laboral |
| 11 | `Satisfaction_with_Remote_Work` | `object` | Nivel o estado de satisfacción con el trabajo remoto. | Dinámica y carga laboral |
| 12 | `Productivity_Change` | `object` | Cambio percibido o reportado en la productividad. | Desempeño y bienestar |
| 13 | `Work_Life_Balance_Rating` | `int64` | Calificación numérica del balance vida-trabajo. | Desempeño y bienestar |
| 14 | `Stress_Level` | `object` | Nivel de estrés reportado. | Salud y bienestar |
| 15 | `Mental_Health_Condition` | `object` | Condición de salud mental registrada (3,804 no nulos; 1,196 nulos). | Salud y bienestar |
| 16 | `Access_to_Mental_Health_Resources` | `object` | Disponibilidad o acceso a recursos de salud mental. | Salud y bienestar |
| 17 | `Physical_Activity` | `object` | Hábito o nivel de actividad física (3,371 no nulos; 1,629 nulos). | Hábitos y estilo de vida |
| 18 | `Sleep_Quality` | `object` | Calidad del sueño reportada. | Hábitos y estilo de vida |
| 19 | `Social_Isolation_Rating` | `int64` | Calificación numérica del nivel de aislamiento social. | Hábitos y estilo de vida |

## Relación entre elementos del dataset
- **Granularidad:** Cada fila representa **un registro individual** (identificado por `Employee_ID`) dentro del mismo archivo plano.
- **Relaciones internas:** Al tratarse de un único dataset tabular y no de tablas separadas por claves foráneas, todas las variables describen atributos del mismo registro. Para el análisis se relacionan cruzando `Work_Location`, `Hours_Worked_Per_Week` y `Number_of_Virtual_Meetings` frente a variables de resultado o bienestar (`Productivity_Change`, `Stress_Level`, `Mental_Health_Condition`, `Sleep_Quality`, `Social_Isolation_Rating`), segmentadas por `Job_Role`, `Industry` o `Region`.