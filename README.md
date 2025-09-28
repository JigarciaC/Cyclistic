# 🚴‍♀️ Cyclistic Bike-Share — Portfolio Project

Este repositorio contiene un análisis comparativo de los patrones de uso de bicicletas entre usuarios `member` y `casual` del sistema Cyclistic (Chicago), una empresa ficticia bike-share.  
El objetivo del negocio es diseñar estrategias de marketing que permitan convertir `ciclistas ocasionales` en `miembros anuales`, ya que éstos son más rentable, con base en los datos de viajes de doce meses (may 2022 - abr 2023).
El analisis se centró en conocer: ¿De qué manera los `ciclistas ocasionales` y los `miembros anuales`usan las bicicletas de Cyclistic de manera diferente?. 
Incluye notebook, visualizaciones y objetos de procesamientos y calidad (resúmenes). 


## Estructura
```
├── Cyclistic_Bike_Share.ipynb
├── results_summary.md
├── README.md
├── HOW_TO_RUN.md
├── requirements.txt
├── .gitignore
├── graphs/
└── data/processed/
```

## Hallazgos clave
- `Members`: viajes concentrados en horas laborables y estaciones céntricas.
- `Casuals`: picos en fines de semana y zonas turísticas.
- Se identificaron 3 clusters de uso (commuters, recreativos, mixtos) útiles para campañas de conversión.

## Recomendaciones
- Campañas dirigidas (Commuter Convert, Weekend Explorer, Station-targeted trials).
- KPIs sugeridos: % conversión a miembros en 3 meses, ocupación por estación, viajes por usuario.

## Nota sobre datos
El dataset original proviene de Divvy/ Motivate (public datasets). 
El dataset procesado se incluye como `Releases` para su descarga.
