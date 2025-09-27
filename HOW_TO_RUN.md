# HOW TO RUN

## Requisitos
Instalar dependencias:
```
pip install -r requirements.txt
```

## Ejecutar en Google Colab
1. Subir `data/processed/cyclistic_trips_clean.snappy.parquet` (si no existe) al panel lateral o montar Google Drive.
2. Abrir `Cyclistic_Bike_Share.ipynb` en Colab y ejecutar celdas en orden.
3. Para regenerar artefactos pesados (clustering, gráficos): setear `RECOMPUTE=True`.

## Resultados
- Visualizaciones en `graphs/`.
- Artefactos analíticos en `data/processed/` (summaries, cluster sample, stat_tests_summary).

## Personalización
- Ajusta los parámetros de KMeans en la sección **Clustering** del notebook.
- Cambia las rutas de salida si deseas otro destino.