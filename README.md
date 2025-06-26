<p align="center">
  <img src="assets/ecommerce-banner.png" alt="E-commerce Sales Banner" width="100%" />
</p>
<h1>Energie-Dashboard</h1>
Data Hackdays in Kanton Bern im 05.2025<br>
Tools: PowerBI
<h1>I. Business Analysis und Anforderungen von Kanton Bern</h1>
<h2>Warum?</h2>
Auf der Energie- und Klimadatenplattform (EKDP) visualisiert der Kanton Bern Erfolge auf dem Weg tur Kimaneutralität bis 2050. Energie- und Kilmadaten können auf Gemeinde- oder Gebäudeebene nach vielfältige Kriteien dargestellt werden. Damit steht mit der Plattform ein wichtiges Instrument zur Verfügung, das für die Förderung, das Monitoring sowie Reporting eingesetzt werden kann.
<h2>Wer?</h2>
Gemiende im Kanton Bern können sich niederschwellig über energierelevante Daten informieren. Aber auch Politisierenden, Energieberatenden, Ingenieurbüros oder der Bevölkerung soll die EKDP spannende Daten aufzeigen.
Das Management sowie die Weiterentwicklung der Plattform wird durch das Amt für Ümwelt und Energie (AUE) des Kantons Bern betreut.
<h2>Was?</h2>
Wir möchten die Nutzung des Dashboards interaktiver gestalten. Interessant wäre z.B die Möglichkeit, Zeitreiben zu visualizieren oder Usern die Erstellung eigener Analysen zu ermöglichen.
Weitere Erwartungen sind:
<ul>
  <li>
    Mögliches neues Energiedashboard mit den vorhandenen Datensätzen.
    Erste Visualisierungen liegen vor.
    Eventuell verwendete zusätzliche Daten sind OGD
    Ideen für Kombination der Daten willkommen
    Lösung soll Ladezeit der EKDP nicht verlängern, um die User-Erfahrung angenehm zu gestalten.
  </li>
</ul>
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






