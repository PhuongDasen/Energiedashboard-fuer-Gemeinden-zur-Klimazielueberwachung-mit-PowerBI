
# 📊 Exploratory Data Analysis: Swiss Energy Dashboard

This analysis explores various aspects of energy usage and production across Swiss municipalities.

---

## 1. Total Anzahl von Energieträger (Donut Chart oben links)

```python
energy_distribution = (
    energy_by_label['Energieträger_Label']
    .value_counts()
    .reset_index()
    .rename(columns={'index': 'Energieträger_Label', 'Energieträger_Label': 'Anzahl'})
)
energy_distribution['Prozentual'] = round((energy_distribution['Anzahl'] / energy_distribution['Anzahl'].sum()) * 100, 2)
display(energy_distribution.head())
```

| Energieträger_Label | Anzahl | Prozentual |
|---------------------|--------|------------|
| Energieträger_Label   |   Anzahl |   Prozentual |
|:----------------------|---------:|-------------:|
| Holz                  |      335 |        10.97 |
| Heizöl                |      334 |        10.94 |
| Elektrizität          |      331 |        10.84 |
| Weitere               |      331 |        10.84 |
| Keine                 |      330 |        10.81 |

---

## 2. Total Minergie, Population und Minergie_percentual (Scatter Plot)

```python
minergie_scatter = minergie_data[['Gemeindename', 'Minergie', 'Minergie_percentual']]
display(minergie_scatter.head())
```

| Gemeindename   |   Minergie |   Minergie_percentual |
|:---------------|-----------:|----------------------:|
| Aarberg        |         12 |              1.26984  |
| Aarwangen      |          9 |              0.715421 |
| Adelboden      |          5 |              0.267094 |
| Aefligen       |          2 |              0.569801 |
| Aegerten       |          0 |              0        |

---

## 3. Renelektrizität Produktion per Jahr (Chart oben rechts)

```python
production_data['Jahr'] = pd.to_datetime(production_data['renelec_production_date_from']).dt.year
prod_per_year = production_data.groupby('Jahr').agg({
    'renelec_production_biomass_mwh_per_year': 'sum',
    'renelec_production_solar_mwh_per_year': 'sum',
    'renelec_production_waste_mwh_per_year': 'sum',
    'renelec_production_water_mwh_per_year': 'sum',
    'renelec_production_wind_mwh_per_year': 'sum'
}).reset_index()
display(prod_per_year.head())
```

|   Jahr |    Biomasse |       Solar |      Abfall |      Wasser |             Wind |
|-------:|------------:|------------:|------------:|------------:|-----------------:|
|   2022 | 3.10858e+06 | 1.11903e+07 | 2.46624e+06 | 1.03047e+08 | 463221           |
|   2023 | 1.22612e+07 | 5.02555e+07 | 9.80214e+06 | 4.85152e+08 |      2.04647e+06 |
|   2024 | 3.97558e+06 | 1.95961e+07 | 3.21534e+06 | 1.72993e+08 | 601489           |

---

## 4. Top Gemeinden nach Minergie, Energieverbrauch

```python
energy_sum = (
    energy_by_label.groupby('GGDENAME')['Anzahl']
    .sum().reset_index().rename(columns={'GGDENAME': 'Gemeindename', 'Anzahl': 'Total_Energy'})
)
top_gemeinden = pd.merge(minergie_data, energy_sum, on='Gemeindename', how='left')
display(top_gemeinden.head())
```

| Gemeindename   |   Minergie |   Minergie_percentual |   Total_Energy |
|:---------------|-----------:|----------------------:|---------------:|
| Aarberg        |         12 |              1.26984  |            945 |
| Aarwangen      |          9 |              0.715421 |           1258 |
| Adelboden      |          5 |              0.267094 |           1872 |
| Aefligen       |          2 |              0.569801 |            351 |
| Aegerten       |          0 |              0        |            559 |

---

## 5. Vergleich: Total Electricity Production vs. per capita

```python
total_vs_capita = {
    'Total_Per_Capita_Production': production_data['renelec_production_mwh_per_year_per_capita'].sum(),
    'Total_Production': production_data['renelec_production_mwh_per_year'].sum()
}
display(pd.DataFrame([total_vs_capita]))
```

|   Total_Per_Capita_Production |   Total_Production |
|------------------------------:|-------------------:|
|                        786193 |        8.80174e+08 |

---
