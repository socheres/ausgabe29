### Organisation

- Redaktionen: ULBs Münster und Düsseldorf
- Unterstützung ULB Bonn
- Technik: hbz

### Historie

- Druckfassung bis Ende 1990er
- Online-Fassung als Nebenprodukt einer effizienteren Durkcproduktion mit Latex
- Datenbank im Deep Web (seit 2005 komplett)
- Auftrag zur Modernisierung: 22.03.2013

### Voraussetzungen / Bibliothekarisches

- Katalogisierung nach RAK-WB, neuerdings RDA
- Inhaltserschließung mit RSWK/GND, zwei speziellen NWBib-Klassifikationen + Gliedernde Schlagwörter (GSW)
  - In Münster: Schlagwortfolgen
- NWBib ist Teil des hbz-Verbundkatalogs => Aleph


### Methodologie

- Inkrementelle Entwicklung
- offener Prototyp
- Rollen/Stakeholder: Projektteam (Entwickler, Projektmanager/Product Owner/Produktmanager) + Kunden (Redaktionen in Düsseldorf und Münster + Bonn)
  - Endnutzer bisher nicht einbezogen
- Kommunikation zwischen Entwicklungsteam und Kunden/Redaktion: Mailingliste, Wiki + zwei persönliche Treffen als Hauptkanäle
- Kommunikation innerhalb des Entwicklungsteams: GitHub, Waffle, Chat, Daily Standups (keine Sprints)

### Technologie

Free Software Java-Tooling:
- lobid-API (Metafacture, elasticsearch, Play)
- für das NWBib-Frontend: Play & Bootstrap 

### Planung und Fortschritt

- zunächst Fertigstellung bis Ende 2014 geplant.
- zweimal verlängert

### Herausforderungen
 
#### Daten und Recherche
 
 - Körperschaftssuche
 - Schlagwortfolgen
 - GND: Ansetzungs- und Verweisungsformen
 - GSW
 - Gleiche Treffer bei gleicher Anfrage: DB vs. Suchmaschine
 - Existierende Java-JSON-LD-Tools nicht dazu geeignet, in ES gut nutzbares JSON-LD zu generieren => API 2.0 als Ergebnis

#### Zusammenarbeit

- Inkrementelles, transparentes offenes Arbeiten noch nicht verinnerlicht
- Präsentation unfertiger Produkte, die in Arbeit sind, ist schwierig
 

#### Endnutzereinbindung

### Lessons Learned

