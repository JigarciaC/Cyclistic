# Results summary — Cyclistic Bike-Share

_Auto-generado: 2025-09-27T09:59:27.573709 UTC_

## 1. Resumen general
- Filas analizadas: **5858517**
- Miembros: **3500469**
- Ocasionales: **2358048**

## 2. Duración de viajes (ride_length)
- Mediana (member): **8.666666666666666 min**
- Mediana (casual): **12.516666666666667 min**
- Diferencia de medianas (member - casual): **-3.8500000000000014 min**
- Mann-Whitney U: **3727446996.5**, p = **0.0**
- Tamaño del efecto (Cohen's d aprox): **-0.07475062203611703**

**Evidencia visual:**
- Histograma (log y): graphs/dist_ride_length_logy.png

## 3. Rideable type vs member/casual
- Chi2 = **306676.67948989075**, p = **0.0**, dof = **2**
- Tabla de contingencia: ver datos en `data/processed`.

## 4. Segmentación (Clustering)
- Centros de cluster (extracto):

|   cluster |   ride_length_min |   hour_of_day |   distance_km |
|----------:|------------------:|--------------:|--------------:|
|         0 |           9.38526 |        8.9354 |       1.54951 |
|         1 |           9.97839 |       17.7004 |       1.53874 |
|         2 |          36.057   |       14.6167 |       4.88916 |

- Artefacto completo: `data/processed/cluster_centers.csv`
- Muestra etiquetada: `data/processed/cluster_sample_with_labels.csv.gz`

## 5. Heatmaps y top-stations
- heatmap_day_hour_member.png: `graphs/heatmap_day_hour_member.png`
- heatmap_day_hour_casual.png: `graphs/heatmap_day_hour_casual.png`
- top10_start_member.png: `graphs/top10_start_member.png`
- top10_start_casual.png: `graphs/top10_start_casual.png`
- trips_by_member_type.png: `graphs/trips_by_member_type.png`


## 6. Small previews (first / last / sample)
### First rows (primeras 5 filas)
| ride_id          | rideable_type   | started_at          | ended_at            | start_station_name                | start_station_id   | end_station_name            | end_station_id   |   start_lat |   start_lng |   end_lat |   end_lng | member_casual   |   ride_length_s |   ride_length_min | date       |   hour_of_day | day_of_week   | month   | is_weekend   | coords_start_invalid   | coords_end_invalid   |   distance_km | long_trip_flag   |
|:-----------------|:----------------|:--------------------|:--------------------|:----------------------------------|:-------------------|:----------------------------|:-----------------|------------:|------------:|----------:|----------:|:----------------|----------------:|------------------:|:-----------|--------------:|:--------------|:--------|:-------------|:-----------------------|:---------------------|--------------:|:-----------------|
| EC2DE40644C6B0F4 | classic_bike    | 2022-05-23 23:06:58 | 2022-05-23 23:40:19 | Wabash Ave & Grand Ave            | TA1307000117       | Halsted St & Roscoe St      | TA1309000025     |     41.8915 |    -87.6268 |   41.9437 |  -87.6489 | member          |            2001 |          33.35    | 2022-05-23 |            23 | Monday        | May     | False        | False                  | False                |      6.08823  | False            |
| 1C31AD03897EE385 | classic_bike    | 2022-05-11 08:53:28 | 2022-05-11 09:31:22 | DuSable Lake Shore Dr & Monroe St | 13300              | Field Blvd & South Water St | 15534            |     41.881  |    -87.6167 |   41.8863 |  -87.6175 | member          |            2274 |          37.9     | 2022-05-11 |             8 | Wednesday     | May     | False        | False                  | False                |      0.60287  | False            |
| 1542FBEC830415CF | classic_bike    | 2022-05-26 18:36:28 | 2022-05-26 18:58:18 | Clinton St & Madison St           | TA1305000032       | Wood St & Milwaukee Ave     | 13221            |     41.8822 |    -87.6411 |   41.9077 |  -87.6726 | member          |            1310 |          21.8333  | 2022-05-26 |            18 | Thursday      | May     | False        | False                  | False                |      3.84407  | False            |
| 6FF59852924528F8 | classic_bike    | 2022-05-10 07:30:07 | 2022-05-10 07:38:49 | Clinton St & Madison St           | TA1305000032       | Clark St & Randolph St      | TA1305000030     |     41.8822 |    -87.6411 |   41.8846 |  -87.6319 | member          |             522 |           8.7     | 2022-05-10 |             7 | Tuesday       | May     | False        | False                  | False                |      0.802763 | False            |
| 483C52CAAE12E3AC | classic_bike    | 2022-05-10 17:31:56 | 2022-05-10 17:36:57 | Clinton St & Madison St           | TA1305000032       | Morgan St & Lake St         | TA1306000015     |     41.8822 |    -87.6411 |   41.8858 |  -87.651  | member          |             301 |           5.01667 | 2022-05-10 |            17 | Tuesday       | May     | False        | False                  | False                |      0.913438 | False            |

### Last rows (últimas 5 filas)
| ride_id          | rideable_type   | started_at          | ended_at            | start_station_name         | start_station_id   | end_station_name          | end_station_id   |   start_lat |   start_lng |   end_lat |   end_lng | member_casual   |   ride_length_s |   ride_length_min | date       |   hour_of_day | day_of_week   | month   | is_weekend   | coords_start_invalid   | coords_end_invalid   |   distance_km | long_trip_flag   |
|:-----------------|:----------------|:--------------------|:--------------------|:---------------------------|:-------------------|:--------------------------|:-----------------|------------:|------------:|----------:|----------:|:----------------|----------------:|------------------:|:-----------|--------------:|:--------------|:--------|:-------------|:-----------------------|:---------------------|--------------:|:-----------------|
| 5A98F86A573AAB2C | electric_bike   | 2023-04-24 07:27:02 | 2023-04-24 07:58:22 | Richmond St & Diversey Ave | 15645              | Clark St & Ida B Wells Dr | TA1305000009     |     41.932  |    -87.7013 |   41.8759 |  -87.6306 | member          |            1880 |           31.3333 | 2023-04-24 |             7 | Monday        | April   | False        | False                  | False                |      8.54819  | False            |
| 92B02F2FBDC1FB9F | classic_bike    | 2023-04-12 08:16:48 | 2023-04-12 08:40:08 | Michigan Ave & Lake St     | TA1305000011       | May St & Taylor St        | 13160            |     41.886  |    -87.6244 |   41.8695 |  -87.6555 | member          |            1400 |           23.3333 | 2023-04-12 |             8 | Wednesday     | April   | False        | False                  | False                |      3.16344  | False            |
| 119A6C53607EAA4A | electric_bike   | 2023-04-28 07:24:54 | 2023-04-28 07:53:44 | Richmond St & Diversey Ave | 15645              | Clark St & Ida B Wells Dr | TA1305000009     |     41.9319 |    -87.7013 |   41.8759 |  -87.6306 | member          |            1730 |           28.8333 | 2023-04-28 |             7 | Friday        | April   | False        | False                  | False                |      8.54051  | False            |
| 9BCF1E8BA027EAFA | electric_bike   | 2023-04-21 07:15:06 | 2023-04-21 07:41:45 | Richmond St & Diversey Ave | 15645              | Clark St & Ida B Wells Dr | TA1305000009     |     41.9319 |    -87.7013 |   41.8759 |  -87.6306 | member          |            1599 |           26.65   | 2023-04-21 |             7 | Friday        | April   | False        | False                  | False                |      8.54334  | False            |
| A17D800CE963661A | classic_bike    | 2023-04-11 15:46:42 | 2023-04-11 15:50:03 | Michigan Ave & Lake St     | TA1305000011       | Clark St & Randolph St    | TA1305000030     |     41.886  |    -87.6244 |   41.8846 |  -87.6319 | member          |             201 |            3.35   | 2023-04-11 |            15 | Tuesday       | April   | False        | False                  | False                |      0.640698 | False            |

### Sample (5 filas desde sample_100.csv)
| ride_id          | rideable_type   | started_at          | ended_at            | start_station_name                     | start_station_id   | end_station_name        | end_station_id   |   start_lat |   start_lng |   end_lat |   end_lng | member_casual   |   ride_length_s |   ride_length_min | date       |   hour_of_day | day_of_week   | month     | is_weekend   | coords_start_invalid   | coords_end_invalid   |   distance_km | long_trip_flag   |
|:-----------------|:----------------|:--------------------|:--------------------|:---------------------------------------|:-------------------|:------------------------|:-----------------|------------:|------------:|----------:|----------:|:----------------|----------------:|------------------:|:-----------|--------------:|:--------------|:----------|:-------------|:-----------------------|:---------------------|--------------:|:-----------------|
| 5F7C8E8F46276038 | classic_bike    | 2022-09-13 17:42:48 | 2022-09-13 17:45:56 | Emerald Ave & 31st St                  | TA1309000055       | Morgan St & 31st St     | TA1308000046     |     41.8382 |    -87.6451 |   41.8378 |  -87.6511 | member          |             188 |           3.13333 | 2022-09-13 |            17 | Tuesday       | September | False        | False                  | False                |      0.498783 | False            |
| D462AAF20F82B5A8 | classic_bike    | 2022-10-01 09:11:21 | 2022-10-01 09:24:47 | DuSable Lake Shore Dr & Wellington Ave | TA1307000041       | Clark St & Lincoln Ave  | 13179            |     41.9367 |    -87.6368 |   41.9157 |  -87.6346 | casual          |             806 |          13.4333  | 2022-10-01 |             9 | Saturday      | October   | True         | False                  | False                |      2.3423   | False            |
| A997793203B2C3C6 | electric_bike   | 2022-05-28 18:20:31 | 2022-05-28 19:08:07 | Blue Island Ave & 18th St              | 13135              | nan                     | nan              |     41.8575 |    -87.6617 |   41.89   |  -87.61   | member          |            2856 |          47.6     | 2022-05-28 |            18 | Saturday      | May       | True         | False                  | False                |      5.60634  | False            |
| DA2CB45AE21F0361 | electric_bike   | 2022-05-12 06:42:00 | 2022-05-12 06:44:07 | Michigan Ave & Washington St           | 13001              | Dearborn St & Monroe St | TA1305000006     |     41.8839 |    -87.6235 |   41.8813 |  -87.6295 | member          |             127 |           2.11667 | 2022-05-12 |             6 | Thursday      | May       | False        | False                  | False                |      0.580395 | False            |
| FE47F8AA2D03FFA2 | electric_bike   | 2022-10-28 22:14:09 | 2022-10-28 22:18:33 | nan                                    | nan                | nan                     | nan              |     41.84   |    -87.73   |   41.84   |  -87.73   | casual          |             264 |           4.4     | 2022-10-28 |            22 | Friday        | October   | False        | False                  | False                |      0        | False            |

## 7. Recomendaciones operativas (resumen)
- **Commuter Convert:** segmentar ocasionales con patrones punta (ver heatmap + cluster centers). KPI: % conversión a miembro en 3 meses.
- **Weekend Explorer:** trials en fines de semana para usuarios con ride_length mayor.
- **Station-targeted trials:** usar estaciones en top10_start_casual.png para campañas localizadas.

## 8. Objetos / dónde inspeccionar
- `data/processed/stat_tests_summary.json`  — resultados estadísticos (JSON)
- `data/processed/first_rows.csv`, `last_rows.csv`, `sample_100.csv` — previews
- `graphs/` — imágenes (.png)

---
