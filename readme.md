🛢️ Análisis Integral de Producción de Hidrocarburos CNH: Pipeline Multi-Nube e Insights con IA
Este proyecto de Data Engineering implementa un pipeline integral para el análisis de datos abiertos de producción de hidrocarburos de la Comisión Nacional de Hidrocarburos (CNH). Siguiendo una arquitectura Data Lakehouse (Bronze, Silver, Gold), transforma datos crudos en insights accionables y sienta las bases para la aplicación de Machine Learning. Desarrollado inicialmente en un entorno local y diseñado para su despliegue multi-nube (AWS y GCP), este trabajo es una demostración de las capacidades de mi marca Datalquemy para generar valor a partir de datos complejos.

📌 Objetivo
Identificar tendencias y patrones clave en la producción de petróleo y gas en México, destacar el rendimiento de campos y operadores, y construir una base de datos robusta para la aplicación de modelos de Machine Learning.

⚙️ Tecnologías Utilizadas
Lenguajes y Frameworks: Python 3, Pandas, Matplotlib, Seaborn

Procesamiento de Datos: Apache Spark (PySpark) (la lógica del pipeline es adaptable a entornos Spark en la nube)

Almacenamiento de Datos: Formato Parquet, Capas Bronze, Silver, Gold (Data Lakehouse)

Plataformas Cloud (Objetivo de Despliegue): Google Cloud Platform (GCP) - Google Cloud Storage, BigQuery, Vertex AI, Amazon Web Services (AWS) - Amazon S3

Entornos de Desarrollo: Jupyter Notebooks

Control de Versiones: Git, GitHub

🧪 Estructura del Proyecto
El repositorio está organizado siguiendo las etapas de un pipeline de datos, facilitando la comprensión y el seguimiento del flujo de información:


```plaintext
cnh-local-etl-insights/
├── README.md                           # Archivo principal de descripción del proyecto
├── .gitignore                          # Archivo para control de versiones
├── SOURCE/                             # Datos crudos originales (e.g., produccion_original.xlsx)
├── BRONZE/                             # Capa Bronze: Datos crudos estandarizados (e.g., aceite_condensado.csv)
├── SILVER/                             # Capa Silver: Datos limpios y transformados (e.g., aceite_condensado.parquet)
├── GOLD/                               # Capa Gold: Datos agregados y modelados para consumo (e.g., total_anual_petroleo.parquet)
├── NOTEBOOKS/                          # Jupyter Notebooks del pipeline y análisis
│   ├── 01_cnh_raw_data_ingestion.ipynb
│   ├── 02_cnh_silver_layer_transformation.ipynb
│   ├── 03_cnh_gold_layer_aggregation_and_modeling.ipynb
│   └── 04_cnh_production_insights_analysis.ipynb
├── plots/                              # Carpeta para las imágenes de los gráficos (enlazadas en este README)
└── ML/                                 # Futura carpeta para modelos de Machine Learning
```

📊 Principales Hallazgos
Basado en el análisis de los datos de producción de hidrocarburos de la CNH para el periodo 2016-2024, los hallazgos clave incluyen:

1. Tendencias Anuales de Producción Nacional
Declive General de Producción: La producción total anual de petróleo y gas natural en México ha mostrado una tendencia descendente sostenida a lo largo del periodo 2016-2024. Esto sugiere desafíos en la reposición de reservas y en la eficiencia de la extracción a nivel nacional.

Comparativa de Recursos: Ambas producciones (petróleo y gas) siguen patrones de declive similares, sin que una compense la caída de la otra, lo que indica un desafío sistémico.

2. Contribución de Operadores
Hegemonía de PEMEX: PEMEX Exploración y Producción mantiene una dominancia abrumadora en la producción total y promedio diario de petróleo y gas.

Visibilidad de Nuevos Actores (Escala Logarítmica): A pesar del dominio de PEMEX, el uso de escalas logarítmicas permite visualizar y comparar la contribución de otros operadores privados y consorcios, revelando la diversidad (aunque de menor magnitud) en el mercado.

3. Liderazgo Anual y Campos Clave
Consistencia en Liderazgo Anual: PEMEX ha sido consistentemente el operador principal en la producción anual de petróleo y gas.

Campos Clave Identificados: Se han identificado los Top 10 campos más productivos de petróleo y gas, puntos críticos para entender la fuente de la producción nacional y para futuras estrategias.

Para un análisis detallado de cada insight y sus visualizaciones, consulta las secciones correspondientes a continuación.

📈 Visualizaciones Clave
Aquí se presentan los gráficos generados, cada uno con su insight correspondiente.

Gráfico 1: Producción Total Anual de Petróleo (2016–2024)
Insight: La producción total anual de petróleo en México muestra una tendencia general a la baja desde 2016, con una posible estabilización o ligera recuperación en los últimos años del periodo analizado (2022-2024). Esto sugiere desafíos en la reposición de reservas o en la eficiencia de la extracción a nivel nacional.

Gráfico 2: Producción Total Anual de Gas Natural sin Nitrógeno (2016–2024)
Insight: Similar al petróleo, la producción total anual de gas natural sin nitrógeno también ha experimentado una disminución sostenida a lo largo del periodo 2016-2024. Esto indica una tendencia general a la baja en la producción de hidrocarburos en México, tanto líquidos como gaseosos.

Gráfico 3: Comparativa Anual de Producción: Petróleo vs Gas (2016–2024)
Insight: Al comparar ambas tendencias, se observa que tanto la producción de petróleo como la de gas natural siguen patrones de declive similares en el periodo. No hay una correlación inversa significativa donde la caída de uno sea compensada por el aumento del otro, lo que refuerza la idea de un desafío sistémico en la producción de hidrocarburos del país.

Gráfico 4: Producción Anual por Recurso (Barras Agrupadas) (2016–2024)
Insight: Este gráfico de barras agrupadas visualiza claramente la magnitud relativa de la producción de petróleo frente al gas en cada año. Confirma la dominancia del petróleo en términos de volumen de energía producida (aunque las unidades son diferentes, la escala visual lo hace evidente) y subraya la tendencia a la baja en ambos recursos a lo largo del tiempo.

Gráfico 5: Promedio Diario de Producción de Petróleo por Operador (Mbd)
Insight: Este gráfico revela la contribución promedio diaria de cada operador a la producción de petróleo. Es fundamental para identificar los operadores más consistentes en el día a día. Se observa que PEMEX Exploración y Producción es, por mucho, el operador dominante en términos de promedio diario, con una brecha significativa respecto a los demás.

Gráfico 6: Promedio Diario de Producción de Gas Natural sin Nitrógeno por Operador (MMpcd)
Insight: De manera análoga al petróleo, PEMEX Exploración y Producción también lidera abrumadoramente la producción promedio diaria de gas natural sin nitrógeno. La distribución de la producción de gas entre los operadores es similar a la del petróleo, con una alta concentración en el operador estatal.

Gráfico 7: Producción Total de Petróleo por Operador (escala logarítmica)
Insight: La aplicación de una escala logarítmica es crucial aquí. Permite visualizar la producción de todos los operadores, incluso aquellos con volúmenes muy pequeños que serían invisibles en una escala lineal. Este gráfico confirma la hegemonía abrumadora de PEMEX en la producción total de petróleo, pero a la vez hace visible y comparable la existencia y contribución de otros operadores privados y consorcios, destacando la diversidad (aunque de menor magnitud) en el mercado.

Gráfico 8: Producción Total de Gas Natural por Operador (escala logarítmica)
Insight: Al igual que con el petróleo, la escala logarítmica en la producción total de gas natural por operador es indispensable. Muestra claramente la vasta diferencia de magnitud entre PEMEX y el resto de los operadores, mientras que simultáneamente permite apreciar las contribuciones y el posicionamiento relativo de los operadores más pequeños en el mercado de gas.

Gráfico 9: Top 10 Operadores de Petróleo por Producción Acumulada
Insight: Este gráfico se enfoca en los 10 operadores más importantes por producción acumulada de petróleo. Si PEMEX fue excluido (o si su barra es tan grande que aún domina), este gráfico permite analizar la jerarquía y la concentración de la producción entre los principales actores más allá del gigante estatal. Es útil para identificar a los "siguientes en la línea" en términos de impacto en la producción nacional.

Gráfico 10: Top 1 Operador por Año – Petróleo (Mbd)
Insight: Este gráfico de barras apiladas (o agrupadas por año) muestra quién ha sido el operador principal en la producción de petróleo en cada año. Si PEMEX es consistentemente el "Top 1", este gráfico lo reafirma. Si hay otros operadores que han logrado ser el "Top 1" en algún año (aunque sea con menor volumen), esto indicaría cambios en el liderazgo o la emergencia de nuevos actores dominantes en periodos específicos.

Gráfico 11: Top 1 Operador por Año – Gas sin Nitrógeno (MMpcd)
Insight: De forma análoga al petróleo, este gráfico revela el liderazgo anual en la producción de gas natural. Si PEMEX mantiene su posición como "Top 1" en todos los años, subraya su rol central en la producción de gas. Cualquier cambio o aparición de otro operador en esta posición sería un hallazgo significativo.

Gráfico 12: Top 10 Campos por Producción Acumulada de Petróleo (Mbd)
Insight: Este gráfico es crucial para identificar las "joyas de la corona" de la producción petrolera mexicana. Muestra los 10 campos individuales que más han contribuido a la producción acumulada de petróleo. Los nombres de estos campos son de alto valor estratégico, y un análisis más profundo de cada uno (como la funcionalidad de IA que planeamos) sería fundamental.

Gráfico 13: Top 10 Campos por Producción Acumulada de Gas Natural sin Nitrógeno (MMpcd)
Insight: Similar al gráfico de campos de petróleo, este visualiza los 10 campos más productivos en términos de gas natural. Es esencial para comprender las fuentes primarias de gas del país y para cualquier estrategia de desarrollo o inversión en este recurso.

🤖 Siguientes Pasos con Machine Learning
Como siguiente fase, el proyecto integrará capacidades de Machine Learning para:

Predicción de Series de Tiempo: Pronosticar la producción futura de petróleo y gas a nivel nacional y por operadores/campos clave.

Detección de Anomalías: Identificar desviaciones inesperadas en los patrones de producción que puedan indicar problemas operativos o de datos.

Generación de Contexto con IA: Desarrollar una funcionalidad para obtener resúmenes contextuales de campos/operadores utilizando la API de Gemini.

🚀 Visión de Datalquemy
Este proyecto es una iniciativa clave de Datalquemy, mi empresa digital enfocada en transformar datos en valor estratégico. Como CEO de Datalquemy, mi visión es construir soluciones de datos innovadoras y escalables, aprovechando la Inteligencia Artificial para optimizar procesos y generar insights profundos.

📥 Dataset
Los datos utilizados en este proyecto son de acceso público, descargados directamente desde la CNH - Datos Abiertos.

Los datasets procesados se encuentran en este mismo repositorio, organizados por capas (Bronze, Silver, Gold).

⚙️ Cómo Ejecutar el Proyecto Localmente
Para replicar y explorar este proyecto en tu entorno local:

Clona este repositorio: git clone https://github.com/Datalquemy/cnh-local-etl-insights.git

Instala dependencias: Asegúrate de tener Python 3.x y las librerías necesarias (pandas, matplotlib, seaborn, pyarrow). Puedes instalarlas con:

pip install pandas matplotlib seaborn pyarrow

Navega a la carpeta NOTEBOOKS/:

cd cnh-local-etl-insights/NOTEBOOKS

Abre los notebooks en Jupyter Lab/Notebook y ejecútalos en orden numérico (01_cnh_raw_data_ingestion.ipynb, 02_cnh_silver_layer_transformation.ipynb, 03_cnh_gold_layer_aggregation_and_modeling.ipynb, 04_cnh_production_insights_analysis.ipynb).

Nota: Este proyecto está diseñado para su futura migración y despliegue en entornos multi-nube (GCP y AWS).

