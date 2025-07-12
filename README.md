```bash
# Proyecto de Machine Learning: Predicción de Incidentes en Oficinas Bancarias

## Problema que se quiere resolver

El objetivo de este proyecto es desarrollar un modelo de Machine Learning capaz de predecir si en una oficina bancaria ocurrirá un incidente con un cliente agresivo (verbal o físico). Esto permitirá a los equipos de seguridad anticipar escenarios conflictivos y asignar recursos como vigilantes, refuerzos o medidas disuasorias de forma más eficaz.

## Dataset empleado

El dataset utilizado es de caracter privado, combina datos de bases de datos (Herramienta de Ticketing desarrollada para almacenaje de datos) reales, se limpió el fichero antes de la extracción eliminando datos personales como Nombre, Apellido, Testigos, DNIs, NIE, CIF y cualquier elemento de caracter personal, para no comprometer información confidencial.

- **Tamaño total:** 1.696 registros
- **Variable target:** `agresion_fisica_verbal`  (1 = Sí, 0 = No)

### Columnas del dataset

```dataset
columnas_dataset = [
    "id_incidente",                # ID único asignado a cada incidente ticket dentro de la petición.
    "fecha_incidente",             # Fecha en la que ocurrió el incidente.
    "hora_incidente",              # Hora aproximada en la que ocurrió el incidente.
    "id_oficina",                  # Identificador único de cada oficina bancaria.
    "ciudad_oficina",              # Ciudad donde se ubica la oficina.
    "llamada_fcs",                 # 1 = Sí, 0 = No. Si se realizó llamada a las Fuerzas y Cuerpos de Seguridad.
    "dia_mes",                     # Día del mes en el que ocurrió el incidente (1 a 31).
    "aforo_alto",                  # 1 = Sí, 0 = No. Indica si había un alto aforo en el momento del incidente.
    "ocupacion_categoria",        # Categoría percibida de ocupación de la oficina ('bajo', 'medio', 'alto').
    "franja_horaria",             # Franja del día en que ocurrió el incidente ('manana' o 'tarde').
    "servicio_vigilante",         # 1 = Sí, 0 = No. Si la oficina contaba con vigilante ese día.
    "ccaa_videoportero",          # 1 = Sí, 0 = No. Si se usó control de acceso con videoportero.
    "fraude_detectado",           # Número de operaciones canceladas por posible fraude ese día.
    "seguimiento_procedimiento_seg",  # 1 = Sí, 0 = No. Si se siguieron procedimientos de seguridad/mitigación.
]
```
Este dataset es **privado**, pero se incluye una muestra **pública** en el directorio `/src/data_sample/` para fines de evaluación.

## Solución adoptada

Se ha implementado un flujo completo de machine learning:

1. **Preprocesamiento** de datos y análisis exploratorio.
2. **Ingeniería de variables** para codificar categorías y escalar valores.
3. **Entrenamiento** de modelos base como Regresión Logística y Random Forest.
4. **Ajuste de hiperparámetros** mediante validación cruzada.
5. **Evaluación final** con métricas como recall y matriz de confusión.
6. **Exportación del modelo** entrenado en formato `.joblib`.

## Estructura de directorios

```
ML_Incidents_Sales_Offices
├── README.md
├── main.ipynb
├── src/
│   ├── data_sample/
│   │   └── sample_dataset.csv
│   ├── models/
│   │   └── modelo_final.joblib
│   └── figures/
│       └── grafico_evaluacion.png
└── docs/
    └── presentacion_proyecto.pdf
```

**Notas:**

- El notebook `main.ipynb` contiene todo el flujo desde carga de datos hasta evaluación y exportación.
- El directorio `src/data_sample` incluye un subset del dataset original.
- `src/models` contiene el modelo exportado.
- `docs` contiene la presentación final en PDF.

---

# Predicting Customer Incidents in Bank Branches (ENGLISH VERSION)

##  Problem Statement

The goal of this project is to develop a Machine Learning model to predict whether an incident involving an aggressive customer (verbal or physical) will occur in a bank branch. This prediction helps security and operations teams to better anticipate conflicts and allocate resources more effectively.

## Dataset Used

The data set used is of a private nature, it combines data real databases (Ticketing Tool developed for data storage data base). The file was cleaned before extraction by eliminating personal data such as Name, Surname, Witnesses, DNIs, NIE, CIF and any element of a personal nature, to mantain secure the confidential information.

- **Total size:** 1,696 records
- **Target variable:** `agresion_fisica_verbal`  (1 = Yes, 0 = No)

### Dataset columns
```dataset
columnas_dataset = [
    "id_incidente",                # Unique ID assigned to each incident ticket within the request.
    "fecha_incidente",             # Date on which the incident occurred.
    "hora_incidente",              # Approximate time when the incident occurred.
    "id_oficina",                  # Unique identifier for each bank branch.
    "ciudad_oficina",              # City where the branch is located.
    "llamada_fcs",                 # 1 = Yes, 0 = No. Whether law enforcement was called.
    "dia_mes",                     # Day of the month when the incident occurred (1 to 31).
    "aforo_alto",                  # 1 = Yes, 0 = No. Indicates if there was high occupancy at the time.
    "ocupacion_categoria",        # Perceived occupancy category of the branch ('low', 'medium', 'high').
    "franja_horaria",             # Time slot of the day when the incident occurred ('morning' or 'afternoon').
    "servicio_vigilante",         # 1 = Yes, 0 = No. Whether the branch had a security guard that day.
    "ccaa_videoportero",          # 1 = Yes, 0 = No. Whether access control via video intercom was used.
    "fraude_detectado",           # Number of operations canceled due to suspected fraud that day.
    "seguimiento_procedimiento_seg",  # 1 = Yes, 0 = No. Whether security/mitigation procedures were followed.
]
```

The dataset is **private**, but a **public sample** is included in `/src/data_sample/` for evaluation purposes.

##  Adopted Solution

A full machine learning pipeline was implemented:

1. **Data preprocessing** and exploratory data analysis.
2. **Feature engineering** to encode categories and scale values.
3. **Training** of baseline models such as Logistic Regression and Random Forest.
4. **Hyperparameter tuning** via cross-validation.
5. **Final evaluation** using metrics like recall and confusion matrix.
6. **Model export** in `.joblib` format.

## Repository Structure

```structure
ML_Incidents_Sales_Offices
├── README.md
├── main.ipynb
├── src/
│   ├── data_sample/
│   │   └── sample_dataset.csv
│   ├── models/
│   │   └── modelo_final.joblib
│   └── figures/
│       └── grafico_evaluacion.png
└── docs/
    └── presentacion_proyecto.pdf
```

**Notes:**

- The `main.ipynb` notebook contains the full pipeline from data loading to model evaluation and export.
- The `src/data_sample` directory includes a subset of the original dataset.
- `src/models` contains the exported model.
- `docs` contains the final presentation in PDF format.



