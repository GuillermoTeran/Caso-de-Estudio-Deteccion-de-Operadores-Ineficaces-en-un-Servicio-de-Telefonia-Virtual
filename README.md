# Caso de Estudio: Detección de Operadores Ineficaces en un Servicio de Telefonía Virtual

## ES Español

Descripción del proyecto:

La empresa de telefonía virtual CallMeMaybe buscaba identificar operadores con bajo rendimiento para optimizar la atención al cliente. Como analista de datos, lideré un proyecto de análisis exploratorio para encontrar operadores ineficaces basándome en múltiples indicadores operativos.

## Objetivos del Proyecto
Realizar un análisis exploratorio de datos (EDA) para comprender el comportamiento operativo.

Establecer métricas para determinar la ineficacia operativa.

Identificar operadores con bajo rendimiento.

Validar hipótesis mediante pruebas estadísticas.

## Fuentes y Estructura de Datos
1. telecom_dataset_us.csv

Información sobre llamadas entrantes, salientes e internas.

Variables clave:

operator_id, calls_count, is_missed_call, call_duration, total_call_duration, internal, direction

2. telecom_clients_us.csv

Información de clientes:

user_id, tariff_plan, date_start

## Criterios para Evaluar la Ineficacia
Alta proporción de llamadas entrantes perdidas (especialmente externas).

Tiempo de espera elevado (diferencia entre total_call_duration y call_duration).

Baja cantidad de llamadas salientes, para operadores cuya función incluye realizarlas.

Filtrado y agrupamiento por operador para comparar el rendimiento relativo.

## Herramientas Utilizadas
Python (Pandas, Seaborn, SciPy)

Jupyter Notebook

Análisis de hipótesis: Prueba t y prueba U de Mann-Whitney

Visualización: Matplotlib, Seaborn

## Análisis Exploratorio y Resultados
Operadores con más del 40% de llamadas perdidas fueron considerados críticos.

Se detectó que algunos operadores tenían un promedio de espera > 40% del total de la duración de llamada.

Se identificaron operadores asignados a tareas salientes con una tasa muy baja de llamadas realizadas.

## Conclusiones y Recomendaciones
Se listaron los operadores más ineficaces para revisión por Recursos Humanos y Supervisión.

Se recomendó ajustar la asignación de operadores en función del tráfico de llamadas.

Se propuso desarrollar alertas automáticas para detectar operadores ineficaces en tiempo real.


## Caso de Estudio: Evaluación de una Prueba A/B para un Sistema de Recomendaciones
Descripción del proyecto:

Una tienda en línea internacional realizó una prueba A/B para evaluar un nuevo sistema de recomendaciones. La tarea fue retomada tras ser abandonada por el equipo anterior. Mi objetivo fue validar la calidad del experimento y analizar sus resultados.

## Objetivos del Estudio
Validar el diseño y ejecución de la prueba A/B.

Analizar conversiones en cada etapa del embudo (product_page → product_card → purchase).

Determinar si hubo mejoras significativas en la conversión gracias al nuevo sistema.

## Datos Utilizados
Dataset	Descripción
final_ab_new_users_upd_us.csv	Nuevos usuarios y sus características
final_ab_events_upd_us.csv	Eventos de interacción de los usuarios
final_ab_participants_upd_us.csv	Participantes y su grupo de prueba
ab_project_marketing_events_us.csv	Calendario de campañas de marketing

## Herramientas Utilizadas
Python (Pandas, NumPy, SciPy)

Gráficos: Plotly, Seaborn

Pruebas estadísticas: Z-test para comparación de proporciones

Gestión del experimento: Verificación de superposición de usuarios, distribución de eventos por día

## Validaciones Previas al Análisis
Conversión de tipos y manejo de valores nulos.

Verificación de que no existieran usuarios en ambos grupos.

Confirmación de que la distribución de eventos por día y por usuario fuera similar entre grupos.

Revisión de eventos de marketing concurrentes que pudieran sesgar los resultados.

## Resultados del Análisis
Se encontró una mejora del 12% en la tasa de visitas a la página del producto en el grupo B.

Las tasas de product_card y purchase también mejoraron, pero solo alcanzaron significancia estadística en la primera etapa (product_page).

El grupo B mostró una mayor retención, pero se recomendó más tiempo de observación para validar compras.

## Conclusiones y Recomendaciones
El nuevo sistema de recomendaciones mejora la atracción inicial del usuario.

Se recomienda iterar sobre el embudo de compras para mejorar conversión en las etapas posteriores.

La prueba A/B fue válida, aunque se sugiere una muestra más grande para confirmar efectos en compras.


# Case Study: Detection of Inefficient Operators in a Virtual Telephone Service

## US English

Project description:

The virtual telephone company CallMeMaybe sought to identify underperforming operators to optimize customer service. As a data analyst, I led an exploratory analysis project to find ineffective operators based on multiple operational indicators.

## Project Objectives
Conduct exploratory data analysis (EDA) to understand operational behavior.

Establish metrics to determine operational inefficiency.

Identify underperforming operators.

Validate hypotheses through statistical testing.

## Data Sources and Structure
1. telecom_dataset_us.csv

Information about incoming, outgoing, and internal calls.

Key variables:

operator_id, calls_count, is_missed_call, call_duration, total_call_duration, internal, direction

2. telecom_clients_us.csv

Customer information:

user_id, tariff_plan, date_start

## Criteria for Evaluating Inefficiency
A high proportion of missed incoming calls (especially external).

High waiting time (difference between total_call_duration and call_duration).

A low number of outgoing calls for operators whose job includes making them.

Filtering and grouping by the operator to compare relative performance.

## Tools Used
Python (Pandas, Seaborn, SciPy)

Jupyter Notebook

Hypothesis testing: t-test and Mann-Whitney U test

Visualization: Matplotlib, Seaborn

## Exploratory Analysis and Results
Operators with more than 40% of missed calls were considered critical.

It was detected that some operators had an average wait time of> 40% of the total call duration.

Operators assigned to outgoing tasks with a very low rate of calls made were identified.

## Conclusions and Recommendations
The most inefficient operators were listed for review by Human Resources and Supervision.

It was recommended that operator assignments be adjusted based on call traffic.

It was proposed that automatic alerts be developed to detect inefficient operators in real-time.


## Case Study: Evaluation of an A/B Test for a Recommendation System
Project description:

An international online store conducted an A/B test to evaluate a new recommendation system. The task was resumed after being abandoned by the previous team. My goal was to validate the quality of the experiment and analyze its results.

## Study Objectives
Validate the design and execution of the A/B test.

Analyze conversions at each stage of the funnel (product_page → product_card → purchase).

Determine whether there were significant improvements in conversion thanks to the new system.

## Data Used
Dataset    Description
final_ab_new_users_upd_us.csv    New users and their characteristics
final_ab_events_upd_us.csv    User interaction events
final_ab_participants_upd_us.csv    Participants and their test group
ab_project_marketing_events_us.csv    Marketing campaign calendar

## Tools Used
Python (Pandas, NumPy, SciPy)

Graphics: Plotly, Seaborn

Statistical tests: Z-test for comparison of proportions

Experiment management: Verification of user overlap, distribution of events by day

## Pre-Analysis Validations
Type conversion and handling of null values.

Verification that there were no users in both groups.

Confirmation that the distribution of events per day and user was similar between groups.

Review of concurrent marketing events that could skew the results.

## Analysis Results
A 12% improvement in the product page visit rate was found in group B.

The product_card and purchase rates also improved, but only reached statistical significance in the first stage (product_page).

Group B showed higher retention, but more observation time was recommended to validate purchases.

## Conclusions and Recommendations
The new recommendation system improves initial user engagement.

It is recommended to iterate on the purchase funnel to improve conversion in later stages.

The A/B test was valid, although a larger sample size is suggested to confirm the effects on purchases.






