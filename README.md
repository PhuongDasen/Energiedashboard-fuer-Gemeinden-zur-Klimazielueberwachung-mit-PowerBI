<p align="center">
  <img src="https://github.com/user-attachments/assets/6336908f-05d6-49f7-96eb-63a5ed766624" width="100%">
</p>
<h1> 📊 Energie-Dashboard</h1>
Data Hackdays in Kanton Bern im 05.2025<br>
Tools: PowerBI<br>

<h2> 📑 Table of Contents <br></h2>
1. [📌 Background & Overview]<br>
2. [📂 Dataset Description & Data Structure])<br>  
3. [🧠 Design Thinking Process]<br>  
4. [📊 Key Insights & Visualizations]<br>  
5. [🔎 Final Conclusion & Recommendations]<br>

---
## 📌 Hintergrund und Überblick 

### Objective:
### 📖 Was ist dieses Projekt?
• Aufbau eines interaktiven Energie-Dashboards auf Basis der EKDP (Energie- und Klimadatenplattform) des Kantons Bern.<br>
•	Ziel: datengetriebene Steuerung und Überwachung der Fortschritte Richtung Klimaneutralität 2050.<br>
•	Visualisierung zentraler KPIs wie Energieträger, Minergie-Standards, Stromproduktion und Bevölkerung auf Gemeindeebene.<br>
### 👤 Für wen ist dieses Projekt?
• Gemeinden<br>
• Politische Entscheidungsträger<br>
• Energieberatende, Ingenieurbüros<br>
• Bevölkerung in Kanton Bern<br>
###  ❓Geschäftsfrage von dem Projekt?
• Welche Energieträger dominieren aktuell in der Gesamtverteilung – und wie groß ist der Anteil erneuerbarer Energiequellen?<br>
• Wie entwickelt sich die Stromproduktion aus erneuerbaren Quellen im Jahresverlauf – und welche Energiequelle liefert welchen Beitrag?<br>
• Welche Gemeinden haben eine hohe Anzahl an Minergie-Gebäuden – und wie korreliert dies mit der Bevölkerungsgröße und dem prozentualen Anteil?<br>
• Wie ist die geografische Verteilung der Energieträger auf Gemeindeebene – und wo bestehen Cluster bestimmter Versorgungsarten?<br>
### 🎯Project Outcome: 
•	Bereitstellung eines strategischen Steuerungstools zur Überwachung energie- und klimapolitischer Maßnahmen.<br>
•	Grundlage für datenbasierte Entscheidungen auf kommunaler und kantonaler Ebene.<br>
## 📂 Dataset Description & Data Structure  

### 📌 Data Source  
### 📊 Data Structure & Relationships  

#### 1️⃣ Tables Used:
<details>
  <summary>🔽 Table: city_energy_users (336 Gemeinden mit ihren Energieträger)</summary>
  <br>
  <img src="https://github.com/user-attachments/assets/8f83a71b-a45a-4c36-bea9-39026bc477b6" width="600"/>
</details>
<details>
  <summary>🔽 Table: Geographie Index der Gemeinde (338 Zeilen)</summary>
  <br>
  <img src="https://github.com/user-attachments/assets/5067ff53-e44a-4d6c-8178-601d20e3b74c" width="600"/>
</details>
#### 2️⃣ Table Schema & Data Snapshot  
#### 3️⃣ Data Relationships:  
---

## 🧠 Design Thinking Process  
---

## ⚒️ Main Process
## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview  

#### 1️⃣ Dashboard 1 Preview  
---

## 🔎 Final Conclusion & Recommendations  
👉🏻 Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following:  

📌 Key Takeaways:  
✔️ Recommendation 1  
✔️ Recommendation 2  
✔️ Recommendation 3








<h1>II. Ressourcen - Datenquellen</h1>

- [Gebäude- und Wohnungsregister GWR](https://opendata.swiss/de/dataset/eidg-gebaude-und-wohnungsregister-energie-warmequelle-heizung)  
  ◦ [Doku Datendownload](https://www.housing-stat.ch/de/madd/public.html) 
  ◦ [Doku Attribute](https://www.housing-stat.ch/de/docs/index.html), insbesondere die [Code-Liste](https://www.housing-stat.ch/files/Codeliste_Publikation_20240411.xlsx)

- [Elektrizitätsproduktionsanlagen](https://opendata.swiss/de/dataset/elektrizitatsproduktionsanlagen)
  ◦ [Dokumentation Datenmodell](https://www.bfe.admin.ch/bfe/de/home/versorgung/digitalisierung-und-geoinformation/geoinformation/geodaten/produktionsanlagen/elektrizitaetsproduktionsanlagen.html)

- [Minergiegebäude](https://opendata.swiss/de/dataset/anzahl-minergie-gebaude-in-gemeinden)

- [Ausgenutztes PV-Potential in Gemeinden](https://opendata.swiss/de/dataset/energie-reporter)  
  ◦ [Dokumentation Methodik](https://energiereporter.energyapps.ch/methodology#heading-solarstrom)

- [Thermische Netze Schweiz](https://opendata.swiss/de/dataset/thermische-netze-nahwarme-fernwarme-fernkalte)  
  ◦ [Dokumentation Datenmodell](https://www.bfe.admin.ch/bfe/de/home/versorgung/digitalisierung-und-geoinformation/geoinformation/geodaten/thermische-netze/thermische-netze.html)
- [Nachhaltiges Potenzial verholzter Biomasse](https://opendata.swiss/de/dataset/nachhaltiges-potenzial-der-verholzten-biomassenressourcen-fur-bioenergie-in-der-schweiz-auf-gem), [Nachhaltiges Potenzial nicht verholzter Biomasse](https://opendata.swiss/de/dataset/nachhaltiges-potenzial-der-nicht-verholzten-biomassenressourcen-fur-bioenergie-in-der-schweiz-a)

- [Gemeinden Kanton Bern](https://opendata.swiss/de/dataset/historisiertes-gemeindeverzeichnis-der-schweiz), oder direkt via  
  [Excel-Tabelle mit aktuellem Gemeindestand](https://www.agvchapp.bfs.admin.ch/de) → `Gemeindestand.xlsx`

- Weitere Open Government Data (OGD) dürfen verwendet werden, siehe z. B.  
  [Geoprodukte des Kanton Bern](https://www.agi.dij.be.ch/de/start/geoportal/geodaten/geodaten-zum-download/geoprodukte-zum-download.html), oder [opendata.swiss](https://opendata.swiss/)

## Weitere Infos
Hintergrundinformationen zum Zweck der EKDP sind auf der [Themenseite des Kantons](https://www.weu.be.ch/de/start/themen/energie/energiedatenplattform.html) verfügbar.

<h1>III. Brainstorming</h1>
<img width="750" alt="Screenshot 2025-05-19 at 10 31 01" src="https://github.com/user-attachments/assets/fdf0b61e-92d1-4c62-ba71-a9d2abcad596" />
<img width="750" alt="Screenshot 2025-05-19 at 10 30 26" src="https://github.com/user-attachments/assets/56e464db-f40e-483a-9fdc-3bf3d11499e5" />
<img width="750" alt="Screenshot 2025-05-19 at 10 30 19" src="https://github.com/user-attachments/assets/21ab95f0-4a72-45a5-aecb-764e0e2c5ca3" />

<h1>IV. Visualisierung</h1>
<img width="3500" alt="Screenshot 2025-05-26 at 18 06 16" src="https://github.com/user-attachments/assets/4f6ddb94-8916-4016-9af9-9e7ce8fedb15" />

<h1>V. Insights</h1>
1️⃣ Tiefere Analyse der Energiequellen
<ul>
<li>🔥 Dominanz fossiler Energieträger: Heizöl (39.22 %) und Gas (11.54 %) machen über 50 % des Mix aus – hohe Abhängigkeit von nicht-erneuerbaren Quellen.</li>
<li>💧 Geringe Nutzung von Fernwärme (4.01 %) und Wasserenergie (0.33 %) – Potenzial für urbane Infrastruktur und Förderprogramme.</li>
<li>⚠️ Kategorie „Keine“ (5.78 %) als Warnsignal – Datenerhebungsprobleme oder fehlende Meldepflicht können Qualität der Analyse beeinträchtigen.</li>
</ul>
2️⃣ Gemeindevergleiche und Minergie-Kontext
<ul>
<li>🏘️ Kleinere Gemeinden mit hohem Minergie-Prozentsatz – Potenzial als Best-Practice-Beispiele.</li>
<li>🏙️ Stadt Bern mit hoher Gesamtenergieproduktion, aber moderatem Wert pro Kopf – zeigt Herausforderungen bei Effizienz in großen Städten.</li>
<li>📊 Viele Gemeinden im unteren Bereich bei Minergie und Prozentanteil – gezielte Unterstützung notwendig.</li>
</ul>
3️⃣ Handlungsempfehlungen für Energieplanung
<ul>
<li>✅ Förderprogramme für Gemeinden mit niedriger Minergie-Quote starten.
<li>⚙️ Einheitliche Datenerfassung und Klassifikation für Energieträger etablieren – besonders für „Keine“ und „Weitere“.
</ul>






