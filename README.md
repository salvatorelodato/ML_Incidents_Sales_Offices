# ML_Incidents_Sales_Offices
Proyecto de Machine Learning para predecir incidentes con clientes agresivos en oficinas bancarias.

El objetivo de este proyecto es desarrollar un modelo de Machine Learning que permita predecir la probabilidad de que ocurra una incidencia con un cliente agresivo en una oficina bancaria. Esta información permitiría a las áreas de seguridad, recursos humanos y operaciones anticiparse a eventos conflictivos y optimizar recursos como personal de seguridad o medidas preventivas en horarios o días críticos.


**ESPAÑOL:**  
El objetivo de este proyecto es desarrollar un modelo de Machine Learning que permita predecir si ocurrirá una incidencia con un cliente agresivo en una oficina bancaria. Esto permitirá a los departamentos de seguridad y operaciones anticiparse a eventos conflictivos y optimizar recursos como personal o medidas preventivas en días u horarios críticos.

**ENGLISH:**  
The goal of this project is to build a Machine Learning model capable of predicting whether an aggressive customer incident will occur at a bank branch. This will allow security and operations teams to anticipate risk situations and optimize staff and preventive measures during critical days and hours.

---

## Dataset utilizado / Dataset Used

- **Tipo:** Dataset extraido, modificado y limpiado para cuidar los datos personales, de incidentes en oficinas bancarias.
- **Período:** 2022 a 2025
- **Tamaño:** 1187 registros
- **Variables principales:**
  - `fecha_hora`: fecha y hora del incidente registrado
  - `oficina`: sucursal donde ocurrió
  - `aforo`: ocupación de la oficina (bajo, medio, alto)
  - `turno`: mañana o tarde (se considera el periodo hasta las 14:00 mañana y en adelante tarde)
  - `agresion_fisica`: 0/1 (0:No, 1:Si)
  - `agresion_verbal`: 0/1 (0:No, 1:Si)
  - `llamada_policia`: 0/1  (0:No, 1:Si)
  - `incidente_agresivo`: variable objetivo (target) (Se considera cualquier agresion)



## Solución adoptada / Adopted Solution

Se utiliza un enfoque de aprendizaje supervisado para predecir la variable `incidente_agresivo` utilizando modelos de clasificación. El flujo de trabajo incluye:


---
