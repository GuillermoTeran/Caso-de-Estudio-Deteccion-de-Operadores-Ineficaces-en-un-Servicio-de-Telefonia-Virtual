# 📞 Caso de Estudio: Detección de Operadores Ineficaces en un Servicio de Telefonía Virtual

## 🇪🇸 Español

### Descripción del Proyecto  
La empresa de telefonía virtual **CallMeMaybe** buscaba identificar operadores con bajo rendimiento para optimizar la atención al cliente. Como analista de datos, lideré un proyecto de análisis exploratorio para detectar operadores ineficaces, utilizando múltiples indicadores operativos.

### Objetivos del Proyecto
- Realizar un análisis exploratorio de datos (EDA) para comprender el comportamiento operativo.
- Establecer métricas para identificar ineficiencia operativa.
- Detectar operadores con bajo rendimiento.
- Validar hipótesis mediante pruebas estadísticas.

### Fuentes y Estructura de los Datos

#### 1. `telecom_dataset_us.csv`  
Contiene información de llamadas entrantes, salientes e internas.  
**Variables clave:**  
- `operator_id`, `calls_count`, `is_missed_call`, `call_duration`, `total_call_duration`, `internal`, `direction`

#### 2. `telecom_clients_us.csv`  
Contiene información de clientes.  
**Variables clave:**  
- `user_id`, `tariff_plan`, `date_start`

### Criterios de Ineficiencia Operativa
- Alta proporción de llamadas entrantes perdidas (especialmente externas).
- Tiempo de espera elevado (diferencia entre `total_call_duration` y `call_duration`).
- Baja cantidad de llamadas salientes en operadores cuya función incluye realizarlas.
- Análisis comparativo entre operadores mediante agrupamientos.

### Herramientas Utilizadas
- Python (Pandas, Seaborn, SciPy)
- Jupyter Notebook
- Pruebas estadísticas: prueba t y prueba U de Mann-Whitney
- Visualización: Matplotlib, Seaborn

### Análisis y Resultados
- Se consideraron críticos los operadores con más del **40% de llamadas perdidas**.
- Algunos operadores presentaron un **tiempo de espera promedio > 40%** del tiempo total de llamada.
- Se identificaron operadores asignados a tareas salientes con **tasas muy bajas de llamadas realizadas**.

### Conclusiones y Recomendaciones
- Se elaboró una lista de operadores ineficaces para revisión por Recursos Humanos y Supervisión.
- Se recomendó **reorganizar la asignación de operadores** en función del tráfico de llamadas.
- Se propuso implementar **alertas automáticas** para detectar ineficiencia en tiempo real.

---

# 🧪 Caso de Estudio: Evaluación de una Prueba A/B para un Sistema de Recomendaciones

### Descripción del Proyecto  
Una tienda en línea internacional llevó a cabo una prueba A/B para evaluar un nuevo sistema de recomendaciones. Retomé el análisis tras su abandono por parte del equipo anterior. Mi objetivo fue validar el diseño del experimento y analizar sus resultados.

### Objetivos del Estudio
- Verificar el diseño y la correcta ejecución de la prueba A/B.
- Analizar las conversiones en cada etapa del embudo (`product_page` → `product_card` → `purchase`).
- Determinar si hubo mejoras estadísticamente significativas gracias al nuevo sistema.

### Datos Utilizados

| Dataset                             | Descripción                                 |
|-------------------------------------|---------------------------------------------|
| `final_ab_new_users_upd_us.csv`     | Información de nuevos usuarios              |
| `final_ab_events_upd_us.csv`        | Eventos de interacción de los usuarios      |
| `final_ab_participants_upd_us.csv`  | Participantes y su grupo experimental       |
| `ab_project_marketing_events_us.csv`| Calendario de campañas de marketing         |

### Herramientas Utilizadas
- Python (Pandas, NumPy, SciPy)
- Visualización: Plotly, Seaborn
- Pruebas estadísticas: Z-test para comparación de proporciones
- Validación experimental: revisión de solapamiento de usuarios y distribución de eventos

### Validaciones Previas al Análisis
- Conversión de tipos y manejo de valores nulos.
- Verificación de ausencia de usuarios en ambos grupos.
- Confirmación de que la distribución diaria de eventos fuera similar entre grupos.
- Revisión de eventos de marketing concurrentes.

### Resultados del Análisis
- El grupo B mostró una mejora del **12% en la tasa de visitas a la página de producto**.
- Las tasas de clics en `product_card` y de `purchase` también mejoraron, aunque solo la primera alcanzó **significancia estadística**.
- Se observó una **mayor retención en el grupo B**, pero se recomendó un período adicional de observación.

### Conclusiones y Recomendaciones
- El nuevo sistema de recomendaciones **mejora la atracción inicial del usuario**.
- Se recomienda **optimizar el embudo de compras** para mejorar la conversión en etapas posteriores.
- La prueba A/B fue válida, aunque sería ideal usar una **muestra mayor** para confirmar efectos en las compras.

---

## 🇺🇸 English

# 📞 Case Study: Detection of Inefficient Operators in a Virtual Phone Service

### Project Description  
The virtual phone company **CallMeMaybe** aimed to identify underperforming operators to improve customer service. As a data analyst, I led an exploratory data analysis (EDA) project to detect inefficiency based on multiple performance indicators.

### Project Objectives
- Conduct EDA to understand operational behavior.
- Define metrics to evaluate operator inefficiency.
- Identify underperforming operators.
- Validate hypotheses through statistical tests.

### Data Sources and Structure

#### 1. `telecom_dataset_us.csv`  
Includes data on incoming, outgoing, and internal calls.  
**Key variables:**  
- `operator_id`, `calls_count`, `is_missed_call`, `call_duration`, `total_call_duration`, `internal`, `direction`

#### 2. `telecom_clients_us.csv`  
Includes customer data.  
**Key variables:**  
- `user_id`, `tariff_plan`, `date_start`

### Inefficiency Evaluation Criteria
- High proportion of missed incoming calls (especially external).
- High waiting time (difference between `total_call_duration` and `call_duration`).
- Low number of outgoing calls by operators responsible for them.
- Operator-level comparisons through filtering and grouping.

### Tools Used
- Python (Pandas, Seaborn, SciPy)
- Jupyter Notebook
- Statistical tests: t-test and Mann-Whitney U test
- Visualization: Matplotlib, Seaborn

### Exploratory Analysis and Results
- Operators with **over 40% missed calls** were flagged as critical.
- Some operators had **average waiting times exceeding 40%** of total call duration.
- Outbound operators with very **low outgoing call activity** were identified.

### Conclusions and Recommendations
- Inefficient operators were listed for **review by HR and Supervisors**.
- It was recommended to **adjust assignments based on call traffic**.
- Development of **real-time alerts** was proposed to flag inefficiencies automatically.

---

# 🧪 Case Study: A/B Test Evaluation for a Recommendation System

### Project Description  
An international e-commerce company conducted an A/B test to evaluate a new recommendation engine. I resumed the analysis after it was left incomplete by the previous team. My goal was to validate the experimental design and analyze the outcome.

### Study Objectives
- Validate the A/B test design and execution.
- Analyze conversions at each funnel stage (`product_page` → `product_card` → `purchase`).
- Determine if the new system significantly improved performance.

### Datasets Used

| Dataset                             | Description                                |
|-------------------------------------|--------------------------------------------|
| `final_ab_new_users_upd_us.csv`     | New users and their attributes              |
| `final_ab_events_upd_us.csv`        | User interaction events                     |
| `final_ab_participants_upd_us.csv`  | Participants and their assigned group       |
| `ab_project_marketing_events_us.csv`| Marketing campaign calendar                 |

### Tools Used
- Python (Pandas, NumPy, SciPy)
- Visualization: Plotly, Seaborn
- Statistical testing: Z-test for proportions
- Experiment management: user overlap and event distribution checks

### Pre-Analysis Validations
- Data type conversions and missing value handling.
- Ensured users appeared in only one group.
- Confirmed similar daily event distribution across groups.
- Reviewed concurrent marketing campaigns to avoid bias.

### Analysis Results
- Group B showed a **12% improvement in product page visit rates**.
- Conversion rates for `product_card` and `purchase` also improved, though only the first reached **statistical significance**.
- **Higher user retention** was observed in Group B, but longer observation was advised for purchase validation.

### Conclusions and Recommendations
- The new recommendation engine **increases initial user engagement**.
- Recommend iterating on the **purchase funnel** to improve later-stage conversions.
- The test was valid; a **larger sample size** is suggested to confirm purchasing impact.






