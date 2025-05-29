# Caso de Estudio: Detección de Operadores Ineficaces en un Servicio de Telefonía Virtual
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

