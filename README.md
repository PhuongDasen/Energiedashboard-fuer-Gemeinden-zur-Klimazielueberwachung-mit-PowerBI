<p align="center">
  <img src="https://github.com/user-attachments/assets/6336908f-05d6-49f7-96eb-63a5ed766624" width="100%">
</p>
<h1> 📊 Energie-Dashboard</h1>
Data Hackdays | Kanton Bern | 05.2025<br>
Tool: PowerBI<br>

<h2> 📑 Inhaltsverzeichnis <br></h2>
1. [📌 Hintergrund & Überblick]<br>
2. [📂 Datensatzbeschreibung & Datenstruktur]<br>  
3. [🧠 Design-Thinking-Prozess]<br>  
4. [📊 Zentrale Erkenntnisse & Visualisierungen]<br>  
5. [🔎 Abschließende Schlussfolgerung & Empfehlungen]<br>

---
## 📌 Hintergrund und Überblick 

### Ziel:
### 📖 Was ist dieses Projekt?
• Aufbau eines interaktiven Energie-Dashboards auf Basis der EKDP (Energie- und Klimadatenplattform) des Kantons Bern.<br>
•	Ziel: datengetriebene Steuerung und Überwachung der Fortschritte Richtung Klimaneutralität 2050.<br>
•	Visualisierung zentraler KPIs wie Energieträger, Minergie-Standards, Stromproduktion und Bevölkerung auf Gemeindeebene.<br>
### 👤 Für wen ist dieses Projekt?
• Gemeinden<br>
• Politische Entscheidungsträger<br>
• Energieberatende, Ingenieurbüros<br>
• Bevölkerung in Kanton Bern<br>
### ❓ Geschäftsfrage von dem Projekt?
• Welche Energieträger dominieren aktuell in der Gesamtverteilung – und wie groß ist der Anteil erneuerbarer Energiequellen?<br>
• Wie entwickelt sich die Stromproduktion aus erneuerbaren Quellen im Jahresverlauf – und welche Energiequelle liefert welchen Beitrag?<br>
• Welche Gemeinden haben eine hohe Anzahl an Minergie-Gebäuden – und wie korreliert dies mit der Bevölkerungsgröße und dem prozentualen Anteil?<br>
• Wie ist die geografische Verteilung der Energieträger auf Gemeindeebene – und wo bestehen Cluster bestimmter Versorgungsarten?<br>
### 🎯 Projektergebnis: 
•	Bereitstellung eines strategischen Steuerungstools zur Überwachung energie- und klimapolitischer Maßnahmen.<br>
•	Grundlage für datenbasierte Entscheidungen auf kommunaler und kantonaler Ebene.<br>
## 📂 Datensatzbeschreibung & Datenstruktur  

### 📌 Datenquellen:   
- Quelle: Data von Kanton Bern (https://www.ekdp.apps.be.ch/home)
- Grösse: 40'393 Zeilen und 10 Säulen
- Format: .csv
### 📊 Datenstruktur und Datenbeziehungen  

#### 1️⃣ Verwendete Tabellen:
Es gibt 9 Tabellen im Datensatz.
#### 2️⃣ Tabellenschema & Datenübersicht
<details>
  <summary>🔽 Tabelle 1: city_energy_users (336 Gemeinden mit ihren Energieträger)</summary>
  <br>
  <img src="https://github.com/user-attachments/assets/8f83a71b-a45a-4c36-bea9-39026bc477b6" width="600"/>
</details>
<details>
  <summary>🔽 Tabelle 2: Geographie Index der Gemeinde (338 Zeilen)</summary>
  <br>
  <img src="https://github.com/user-attachments/assets/5067ff53-e44a-4d6c-8178-601d20e3b74c" width="600"/>
</details>
<details>
  <summary>🔽 Tabelle 3: Erneuerbare Energie Produktion (40'393 Zeilen und 10 Säulen)</summary>
  <br>
  <img src="https://github.com/user-attachments/assets/4ad25ceb-1f6b-4c49-87bf-669e8c9ac05b" width="600"/>
</details>

#### 3️⃣ Datenbeziehungen:  
<img src="https://github.com/user-attachments/assets/3d208ab8-104a-4c40-aea2-88597b8c748a" alt="Data Modelling" width="600" /><br>
---

## 🧠  Ideensammlung
<p><strong>Analysiere die Geschäftsfragen, um alle möglichen Kennzahlen und Lösungen zu definieren</strong></p>
<img width="750" src="https://github.com/user-attachments/assets/fdf0b61e-92d1-4c62-ba71-a9d2abcad596"/>
<p><strong>Schnittstellenreferenz und Entwurfslayout</strong></p>
<img width="750" alt="Screenshot 2025-05-19 at 10 30 26" src="https://github.com/user-attachments/assets/56e464db-f40e-483a-9fdc-3bf3d11499e5" />
<p><strong>Aktuelle Schnittstellenstatusanalyse</strong></p>
<img width="750" alt="Screenshot 2025-05-19 at 10 30 19" src="https://github.com/user-attachments/assets/21ab95f0-4a72-45a5-aecb-764e0e2c5ca3" />
 <br>
---

## ⚒️ Hauptprozess <br> 
1️⃣ Datenbereinigung und -vorverarbeitung <br> 
Daten des Kantons Bern wurden im System bereinigt und aufbereitet. <br>

2️⃣ Explorative Datenanalyse (EDA) <br>
- Verständnis der Struktur und Inhalte der Datensätze zu Energie, Bevölkerung und Minergie.<br>
- Untersuchung der Verteilung der Energieträger (z. B. Holz, Elektrizität, Fernwärme) in den Gemeinden.<br>
- Analyse der Beziehung zwischen Minergie-Anzahl, Minergie-Prozentsatz und Bevölkerung pro Gemeinde.<br>
- Aggregation der erneuerbaren Stromproduktion (Wasser, Solar, Wind, Biomasse, Abfall) nach Jahr zur Erkennung von Trends.<br>
- Vergleich der Top-Gemeinden mit dem höchsten Energieverbrauch oder der höchsten Minergie-Zahl.<br>
- Aufdecken von Auffälligkeiten oder interessanten Mustern zur Unterstützung der Dashboard-Gestaltung.<br>

3️⃣ SQL/ Python Analyse 
## 1. Gesamtanzahl der Energieträger

```python
energy_distribution = (
    energy_by_label['Energieträger_Label']
    .value_counts()
    .reset_index()
    .rename(columns={'index': 'Energieträger_Label', 'Energieträger_Label': 'Anzahl'})
)
energy_distribution['Prozentual'] = round(
    (energy_distribution['Anzahl'] / energy_distribution['Anzahl'].sum()) * 100, 2)
display(energy_distribution.head())
```

&nbsp;

| Energieträger_Label | Anzahl | Prozentual |
|---------------------|--------|------------|
| Holz                | 335    | 10.97      |
| Heizöl              | 334    | 10.94      |
| Elektrizität        | 331    | 10.84      |
| Weitere             | 331    | 10.84      |
| Keine               | 330    | 10.81      |

🎯 **Ergebnisanalyse:**  
Holz, Heizöl und Elektrizität sind die drei am häufigsten verwendeten Energieträger, wobei jeder rund 11 % der Gesamtanzahl ausmacht.

## 2. Gesamt-Minergie, Bevölkerung und Minergie-Prozentsatz

```python
minergie_scatter = minergie_data[['Gemeindename', 'Minergie', 'Minergie_percentual']]
display(minergie_scatter.head())
```

&nbsp;

| Gemeindename | Minergie | Minergie_percentual |
|--------------|----------|----------------------|
| Aadorf       | 37       | 0.32                 |
| Aarau        | 409      | 2.53                 |
| Aarberg      | 48       | 1.12                 |
| Aarburg      | 31       | 0.57                 |
| Aarwangen    | 53       | 0.89                 |

🎯 **Ergebnisanalyse:**  
Aarau hat mit 409 die meisten Minergie-Gebäude, was 2,53 % der Gesamtbevölkerung entspricht – deutlich höher als andere Gemeinden.

## 3. Produktion erneuerbarer Elektrizität pro Jahr

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

&nbsp;

| Jahr | Biomasse | Solar     | Abfall   | Wasser      | Wind     |
|------|----------|-----------|----------|-------------|----------|
| 2022 | 3108580  | 11190311  | 2466235  | 103047218   | 463221   |
| 2023 | 12261186 | 50255514  | 9802144  | 485151896   | 2046467  |
| 2024 | 3975583  | 19596145  | 3215339  | 172992561   | 601489   |

🎯 **Ergebnisanalyse:**  
Die Wasserenergie macht den größten Anteil aus und zeigt 2023 einen starken Produktionsanstieg auf über 485 Mio. kWh.

## 4. Top Gemeinden nach Minergie und Energieverbrauch

```python
energy_sum = (
    energy_by_label.groupby('GGDENAME')['Anzahl']
    .sum().reset_index().rename(columns={'GGDENAME': 'Gemeindename', 'Anzahl': 'Total_Energy'})
)
top_gemeinden = pd.merge(minergie_data, energy_sum, on='Gemeindename', how='left')
display(top_gemeinden.head())
```

&nbsp;

| Gemeindename | Energieträger | BfsNumber | Minergie | Minergie_percentual | Total_Energy |
|--------------|----------------|-----------|----------|----------------------|---------------|
| Aadorf       | Elektrizität    | 4561      | 37       | 0.32                 | 3             |
| Aarau        | Gas             | 4001      | 409      | 2.53                 | 7             |
| Aarberg      | Holz            | 304       | 48       | 1.12                 | 6             |
| Aarburg      | Elektrizität    | 4101      | 31       | 0.57                 | 4             |
| Aarwangen    | Heizöl          | 331       | 53       | 0.89                 | 5             |

🎯 **Ergebnisanalyse:**  
Gemeinden wie Aarau vereinen hohe Minergie-Zahlen mit vergleichsweise moderatem Energieverbrauch (z. B. 7 Einträge in Total_Energy).

## 5. Vergleich: Gesamte Stromproduktion vs. Pro-Kopf-Produktion

```python
total_vs_capita = {
    'Total_Per_Capita_Production': production_data['renelec_production_mwh_per_year_per_capita'].sum(),
    'Total_Production': production_data['renelec_production_mwh_per_year'].sum()
}
display(pd.DataFrame([total_vs_capita]))
```

&nbsp;

| Total_Per_Capita_Production | Total_Production |
|-----------------------------|------------------|
| 786193.39                   | 880173937        |

🎯 **Ergebnisanalyse:**  
Die Gesamtproduktion beträgt über 880 Mio. kWh, während die Pro-Kopf-Produktion nur 786 Tsd. kWh beträgt – ein Hinweis auf regionale Produktionsungleichheit.
<br>

## 📊 Zentrale Erkenntnisse & Visualisierungen 

### 🔍 Dashboard Vorschau  
<img width="3500" alt="Screenshot 2025-05-26 at 18 06 16" src="https://github.com/user-attachments/assets/4f6ddb94-8916-4016-9af9-9e7ce8fedb15" />

📊 Hauptbeobachtungen  
- 🛢️ Heizöl ist mit 39.22 % der am häufigsten genutzte Energieträger, gefolgt von 🌲 Holz (16.36 %) und 🔥 Gas (11.54 %).  
- ⚡ Die jährliche Stromproduktion schwankt erheblich, mit einem Spitzenwert über 4 M im Dezember 2023.
---

## 🔎 Abschließende Schlussfolgerung & Empfehlungen 

📌 Zentrale Erkenntnisse:

✔️ Fokussierung auf leistungsstarke Lieferanten:
Konzentrieren Sie den Einkauf auf Lieferanten mit hoher Lieferzuverlässigkeit und gutem Kosten-Leistungs-Verhältnis.
Maßnahme: Einführung einer Auswahlrichtlinie für Lieferanten basierend auf der Termintreue und dem Kosten-Effizienz-Index.

✔️ Verbesserung leistungsschwacher Bereiche:
Identifizieren Sie Lieferanten oder Gemeinden mit geringer Energieeffizienz oder hohen Ausschussquoten.
Maßnahme: Start eines Lieferanten-Entwicklungsprogramms mit klaren KPIs und vierteljährlichen Bewertungen.

✔️ Optimierung der Ressourcennutzung basierend auf Nutzungstrends:
Passen Sie Investitionen in Infrastruktur (z. B. erneuerbare Energien, Logistik) an saisonale oder regionale Verbrauchstrends an.
Maßnahme: Entwicklung eines dynamischen Ressourcenplanungsmodells auf Basis der Dashboard-Daten.






