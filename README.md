# 🚴‍♀️ Cyclistic Bike-Share — Portfolio Project

## Proyecto: 
  Análisis comparativo de los patrones de uso de bicicletas entre `miembros anuales` y `ciclistas ocasionales` del sistema Cyclistic (Chicago), una empresa ficticia bike-share (May 2022 — Apr 2023)
## Objetivo:
  Identificar diferencias de uso entre `member` y `casual` para proponer campañas de conversión de casual → member.

## Business question & stakeholders
* Pregunta de negocio: ¿De qué manera los ciclistas ocasionales y los miembros anuales usan las bicicletas de Cyclistic de manera diferente?
* Stakeholders: Directora de Marketing, Equipo de Marketing, Equipo Ejecutivo.


## Incluye
```
├─ data/ processed/ # OBJETOS: csv pequeños, logs, snapshots, parquet
│ ├─ cyclistic_trips_clean.snappy.parquet # fuente 
│ ├─ cyclistic_trips_clean_imputed_v2_tagged.parquet
│ ├─ cyclistic_trips_station_backed.snappy.parquet
│ ├─ imputation_log_v2.csv
│ ├─ imputation_validation_rows.csv
│ ├─ audit_validation_summary.csv
│ └─ first_rows.csv / sample_100.csv / station_coord_lookup.csv
├─ graphs/ 
├─ Cyclistic_Bike_Share.ipynb/ # report_and_results
├─ dictionary_variables.md
├── .gitignore
├─ README.md
├─ HOW_TO_RUN.md
└─ requirements.txt

```
## Resumen ejecutivo
Analizamos el comportamiento de uso de Cyclistic (bicicletas compartidas de Chicago) para entender **cómo difieren los ciclistas ocasionales y los miembros anuales**, con foco en diseñar tácticas de marketing para convertir ocasionales en miembros.

**Hallazgos clave**
- Dataset combinado (12 meses): **≈ 5.85M** viajes (raw), proviene de Divvy/ Motivate (public datasets) 
- Dataset limpio / station-backed sample usado en reportes: **n ≈ 49,344** (ejemplo de muestra con estaciones asignadas).
- El **análisis** se basó en el esquema **Google DA**
- Proporción en la muestra: **Miembros ≈ 30,601 (≈62%) ; Ocasionales ≈ 18,742 (≈38%)**.  
- Duración media/mediana:
  - Mediana (member): **≈ 8.666 min**  
  - Mediana (casual): **≈ 12.5 min**  
  - Mann-Whitney U: **U ≈ 3,290,524,717.0 p = 0.00 ** (diferencia significativa).
- Asociación entre `rideable_type` y `member_casual`: **chi2 ≈ 306676,679, p = 0.000**.
- Segmentación (KMeans) identificó clusters interpretables (commuters, after-work, leisure), cuyos centros están en `data/processed/cluster_centers.csv`.

## Hallazgos visuales
- `Members`: viajes concentrados en [horas laborables](graphs/heatmap_day_hour_member.png) y [estaciones céntricas](graphs/top10_start_member.png).
- `Casuals`: [picos en fines de semana](graphs/heatmap_day_hour_casual.png) y [zonas turísticas](graphs/top10_start_casual.png).
- Se identificaron [3 clusters de uso](data/processed/cluster_centers.csv) (commuters, recreativos, mixtos) útiles para campañas de conversión.

## Recomendaciones (resumen)
- **Commuter Convert:** campañas dirigidas a ocasionales con patrones de hora punta (trial/membresía reducida); KPI: % conversión en 3 meses.  
- **Weekend Explorer:** targeting a ocasionales con picos fines de semana y alta duración; oferta: trial fines de semana.  
- **Station-targeted trials:** campañas geolocalizadas en estaciones con alta densidad de ocasionales.

