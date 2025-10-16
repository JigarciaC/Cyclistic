# 🚴‍♀️ Cyclistic Bike-Share — Portfolio Project

Proyecto: Análisis comparativo de los patrones de uso de bicicletas entre `miembros anuales` y `ciclistas ocasionales` del sistema Cyclistic (Chicago), una empresa ficticia bike-share (May 2022 — Apr 2023)
* El objetivo es identificar diferencias de uso entre `member` y `casual` para proponer campañas de conversión de casual → member.
Business question & stakeholders

* Pregunta de negocio: ¿De qué manera los ciclistas ocasionales y los miembros anuales usan las bicicletas de Cyclistic de manera diferente?
* Stakeholders: Directora de Marketing, Equipo de Marketing, Equipo Ejecutivo.
* Objetivo final: Generar recomendaciones accionables para convertir casuals a miembros anuales (KPI propuesto: % conversión en 3 meses).


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
├── results_summary.md

```

## Datos y metodología
* El **dataset original** proviene de Divvy/ Motivate (public datasets), compuesto por 12 archivos CSV, históricos, con más de 5 millones de registros. 
* El **dataset procesado** con python y se incluye como `Releases` para su descarga.
* El **análisis** se basó en el esquema **Google DA**
* Se **eliminaron registros** con `started_at` o `ended_at` faltantes o donde `ended_at < started_at` (viajes negativos ó > 24h).
* Se detectaron filas con coordenadas inválidas (`start_lat == 0 & start_lng == 0 o end_lat==0 & end_lng==0`) y se etiquetaron como `“coordenadas inválidas”`.
  * Si station_id está presente, conservar y usar station_id;
  * Si tanto sation_id como coordenadas faltan, entonces eliminar.
* Se **eliminaron registros con NA** en `start_station_name`donde además faltaban filas de `station_id`.
* Se aplicaron estadísticas descriptivas (moda, mediana) y segmentación exploratoria (clustering K-Medias y pruebas estadísticas de diferencia de medianas)

## Hallazgos clave
- `Members`: viajes concentrados en [horas laborables](graphs/heatmap_day_hour_member.png) y [estaciones céntricas](graphs/top10_start_member.png).
- `Casuals`: [picos en fines de semana](graphs/heatmap_day_hour_casual.png) y [zonas turísticas](graphs/top10_start_casual.png).
- Se identificaron [3 clusters de uso](data/processed/cluster_centers.csv) (commuters, recreativos, mixtos) útiles para campañas de conversión.

## Recomendaciones
- Campañas dirigidas (Commuter Convert, Weekend Explorer, Station-targeted trials).
- KPIs sugeridos: % conversión a miembros en 3 meses, ocupación por estación, viajes por usuario.

