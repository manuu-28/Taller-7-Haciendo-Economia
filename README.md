# Taller 7

## Equipo consultor

| Integrante        | Rol                                               |
|-------------------|---------------------------------------------------|
| David Suárez      | Líder del proyecto y enlace con el fondo          |
| Manuela Vergara   | Especialista en datos y reproducibilidad          |
| Santiago Cortés   | Analista cuantitativo                             |
| Ariana Garzón     | Especialista en visualización y comunicación      |

## Descripción del proyecto

Este proyecto simula una consultoría financiera para un fondo de inversión internacional. El objetivo central es evaluar la evolución, el desempeño acumulado y el perfil de riesgo-retorno de **tres sectores de la economía global** durante el decenio 2015–2025, analizando en particular el impacto estocástico y estructural asociado al periodo pre y post COVID-19.

Para esto, se construyen tres índices financieros transparentes basados en universos de 10 acciones por sector, evaluando la sensibilidad de los resultados según distintas reglas de ponderación (volumen transaccionado inicial vs. precio inicial). A través de un análisis cuantitativo documentado y reproducible en Excel (con soporte opcional en Power BI y conexión a terminales Bloomberg), se entregan métricas de dispersión, análisis de distribuciones de retornos, intervalos de confianza al 95% e interpretaciones clave para la toma de decisiones estratégicas de inversión.

## Contribuciones

### 1. Líder del proyecto y enlace con el fondo — David Suárez

- Definió las preguntas del fondo y la estructura del informe.
- Redactó la recomendación de inversión (priorizar Tecnología, mantener Salud bajo observación, evitar Energía)
- Revisó la consistencia entre las cifras de las tablas y las conclusiones.

### 2. Especialista en datos y reproducibilidad — Manuela Vergara

- Descargó precios de cierre (`PX_LAST`) y volúmenes (`PX_VOLUME`) diarios 2015–2025 de 30 acciones con la conexión Excel–Bloomberg. 
- Documentó tickers, empresas, industrias, fuente y parámetros, y creó nombres definidos para actualizar todo desde un solo lugar. 
- Construyó el indicador de día hábil, que detecta los festivos rellenados por Bloomberg para que no contaminen los retornos.

### 3. Analista cuantitativo — Santiago Cortés

- Calculó los pesos por volumen, por precio y por valor transado de enero 2015, con verificación de que suman 1.
- Calculó los retornos aritméticos diarios por acción y los retornos ponderados de los índices; construyó los índices base 100 y las caídas desde el máximo. 
- Calculó número de observaciones, promedio, desviación estándar e intervalos de confianza al 95% con `CONFIDENCE.T`, más las pruebas de diferencia de medias (Welch) y de varianzas (F).
- 
### 4. Especialista en visualización y comunicación — Ariana Garzón

- Diseñó los diagramas de cajas y bigotes con valores atípicos, construidos con fórmulas y actualizables. 
- Construyó los histogramas con curva normal de referencia y los gráficos de líneas base 100 en escala lineal y logarítmica. 
- Preparó los gráficos de barras 2015 vs 2025 con intervalos de confianza y el guion de la presentación de 5 minutos. 

## Estructura del repositorio
RawData/ -> Datos sin editar

Excel/ -> Excel resuelto

Resultados/ -> Gráficos generados 
