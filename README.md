# Aplicación de Modelos de Polarizacion

TFG Matemáticas 2024/25

Este notebook procesa y analiza datos de tweets correspondientes a campañas electorales de distintos años (2016, 2020 y 2024). A continuación se explican las principales secciones y funcionalidades del código:

- **Carga y Preprocesado de Datos**:  
  Se importan datasets en formato CSV y se inspeccionan muestras de los datos.

- **Análisis de Usuarios**:  
  Se calcula el número de usuarios únicos por grupo y se determinan intersecciones entre ellos, comprobando usuarios comunes tanto entre partidos como entre años.

- **Construcción del Índice de Intención de Voto**:  
  Se agrupan tweets por usuario para calcular promedios y conteos de etiquetas y, a partir de ello, se construye un índice de intención de voto usando la fórmula:  
  (u_R * m_R - u_D * m_D) / (m_R + m_D)  
  Se obtiene un valor por usuario para cada año y se visualizan los resultados con histogramas.

- **Cálculo de Índices de Polarización**:  
  Se implementan varias funciones para evaluar la polarización a partir de los datos:
  - **Índice de Polarización Gravitatoria (IPG)**: Mide la diferencia normalizada en las opiniones a partir de los centros de gravedad de los valores.
  - **Índice Foster-Wolfson (FW)**: Basado en la desigualdad (Gini) y en la diferencia entre promedios de subgrupos.
  - **Índice de Esteban-Ray (ER)**: Evalúa la polarización considerando la distribución de opiniones negativas, positivas y ceros, con un parámetro ajustable (alpha).
  - **Índice Beta de Polarización**: Un índice original de este trabajo que emplea la entropía de la distribución de las etiquetas de tweets de cada usuario para medir la cohesión interna y la polarización entre grupos.

- **Aplicación a Muestras Reales**:  
  Finalmente, se aplican todos los modelos a las muestras correspondientes a cada año (2016, 2020, 2024) y se imprimen los índices de intención de voto y polarización obtenidos.

Este código proporciona una plataforma completa para analizar la polarización en redes sociales a partir de datos de tweet, combinando análisis estadístico y visualización.
