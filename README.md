# 🚴‍♀️ Cyclistic Bike-Share — Portfolio Project

Este repositorio contiene un análisis comparativo entre usuarios `member` y `casual` del sistema Cyclistic (Chicago).
Incluye notebook, visualizaciones y artefactos de calidad (resúmenes). El dataset procesado se incluye como release para su descarga.

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
- Members: viajes concentrados en horas laborables y estaciones céntricas.
- Casuals: picos en fines de semana y zonas turísticas.
- Se identificaron 3 clusters de uso (commuters, recreativos, mixtos) útiles para campañas de conversión.

## Recomendaciones
- Campañas dirigidas (Commuter Convert, Weekend Explorer, Station-targeted trials).
- KPIs sugeridos: % conversión a miembros en 3 meses, ocupación por estación, viajes por usuario.

## Nota sobre datos
El dataset original proviene de Divvy/ Motivate (public datasets). No subir CSV grandes al repo: usar releases, Git LFS o almacenar en cloud.
