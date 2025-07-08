SPANISH 
# ML_Incidents_Sales_Offices
Proyecto de Machine Learning para predecir incidentes con clientes agresivos en oficinas bancarias.

**ESPAÑOL:**  
El objetivo de este proyecto es desarrollar un modelo de Machine Learning que permita predecir si ocurrirá una incidencia con un cliente agresivo en una oficina bancaria. Esto permitirá a los departamentos de seguridad y operaciones anticiparse a eventos conflictivos y optimizar recursos como personal o medidas preventivas en días u horarios críticos.

## Dataset utilizado 

- **Tipo:** Dataset extraido, modificado y limpiado para cuidar los datos personales, de incidentes en oficinas bancarias.
- **Período:** 2021 a 2025
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

El dataset completo es **privado**, pero se incluye una muestra representativa en la carpeta [`/src/data_sample`] para poder ejecutar el proyecto.

## Solución adoptada / Adopted Solution

Se utiliza un enfoque de aprendizaje supervisado para predecir la variable `incidente_agresivo` utilizando modelos de clasificación.

Se ha desarrollado un modelo de clasificación supervisada para predecir si un incidente podría ser agresivo.  
El cual incluye :

1. Análisis exploratorio de los datos (EDA)
2. Preprocesamiento y codificación de variables
3. Entrenamiento de varios modelos base
4. Evaluación final con métricas como recall, precisión  y matriz de confusión

El modelo final ayuda a detectar patrones de riesgo y puede ser usado para tomar decisiones operativas en oficinas.

Estructura del repositorio

── src/                # El directorio source que debe contener al resto de carpetas
    ├── data_sample/    # Los archivos de datos de muestra utilizados en el proyecto que permitan ejecutar el código
    ├── img/            # Las imágenes que hayas utilizado para tu proyecto
    ├── models/         # Los modelos guardados al ejecutar el código del proyecto en formato pickle o joblib (a elegir)
    ├── notebooks/      # Los notebooks usados para pruebas
    ├── utils/          # Todos los modulos, funciones auxiliares o clases creadas para el desarrollo del proyecto
├── main.ipynb          # El notebook final del proyecto: claro, conciso, y bien estructurado con el paso a paso del proceso
├── presentacion.pdf    # El documento soporte que utilices como apoyo a la exposición de resultados en vídeo
├── README.md           # El fichero README resumen del proyecto
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ENGLISH

 ML_Incidents_Sales_Offices  
Machine Learning project to predict aggressive customer incidents in bank branches.

**ENGLISH:**  
The goal of this project is to develop a Machine Learning model capable of predicting whether an aggressive customer incident will occur in a bank branch. This will allow security and operations departments to anticipate conflictive events and optimize resources such as staff allocation or preventive measures during critical days or hours.

## Dataset used

- **Type:** Dataset extracted, modified, and cleaned to protect personal information related to incidents in bank branches.
- **Period:** 2021 to 2025
- **Size:** 1,187 records
- **Main variables:**
  
  - `fecha_hora`: date and time when the incident was recorded
  - `oficina`: the branch where the incident occurred
  - `aforo`: branch occupancy level (low, medium, high)
  - `turno`: shift (morning or afternoon — morning is until 14:00, and afternoon starts afterward)
  - `agresion_fisica`: 0/1 (0: No, 1: Yes)
  - `agresion_verbal`: 0/1 (0: No, 1: Yes)
  - `llamada_policia`: 0/1 (0: No, 1: Yes)
  - `incidente_agresivo`: target variable (any type of aggression)

The full dataset is **private**, but a representative sample is included in the [`/src/data_sample`] folder to allow project execution.

## Adopted Solution

A supervised learning approach was used to predict the `incidente_agresivo` variable using classification models.

A supervised classification model was developed to predict whether an incident may be aggressive.  
The process includes:

1. Exploratory Data Analysis (EDA)
2. Preprocessing and feature encoding
3. Training several baseline models
4. Final evaluation using metrics such as recall, precision, and confusion matrix

The final model helps detect risk patterns and can be used to support operational decision-making at bank branches.

## Repository Structure

```bash
├── src/                # Source directory containing all code components
│   ├── data_sample/    # Sample dataset files used to run the project
│   ├── img/            # Images and plots used in the project
│   ├── models/         # Trained models saved as pickle or joblib files
│   ├── notebooks/      # Notebooks used for experimentation
│   ├── utils/          # Helper functions, modules, or classes for project development
├── main.ipynb          # Final notebook with the full, well-structured pipeline
├── presentacion.pdf    # Slide deck or visual support used during video presentation
├── README.md           # This README file summarizing the project
