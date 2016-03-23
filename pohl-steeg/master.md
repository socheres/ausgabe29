Aufgaben einer Landesbibliographie:

 > Zitat

Dies gilt so auch für die Nordrhein-Westfälischen Bibliographie, im folgenden "NWBib" abgekürzt. Auf der Webseite des neuen Webauftritts[^1] heißt es:

> Die Nordrhein-Westfälische Bibliographie (NWBib) verzeichnet die Literatur über das Land Nordrhein-Westfalen, seine Regionen, Orte und Persönlichkeiten, Literatur aus allen Lebens- und Wissensbereichen in Geschichte und Gegenwart.

> Die NWBib ist eine der umfangreichsten Regionalbibliographien Deutschlands. Sie erschließt nicht nur Bücher und Zeitschriften, sondern auch Aufsätze und andere Medien wie etwa Karten, DVDs, Hörbücher und elektronische Publikationen. 

### Organisation

Im Unterschied zu anderen Landesbibliographien sind Erstellung, Entwicklung und Betrieb der Nordrhein-Westfälischen Bibliographie (NWBib) gesetzlich verankert. Im Gesetz zur Regelung des Pflichtexemplarrechts in Nordrhein-Westfalen heißt es in §2:

> (1) Die Aufgabe der Sammlung der Pflichtexemplare nehmen die Universitäts- und Landesbibliotheken Bonn, Düsseldorf und Münster gemeinsam wahr. (...)

> (2) Die Bibliotheken erstellen gemeinsam die Nordrhein-Westfälische Bibliographie. Diese verzeichnet und erschließt die Medienwerke mit inhaltlichem Bezug zu Nordrhein-Westfalen unabhängig davon, ob sie innerhalb oder außerhalb Nordrhein-Westfalens verlegt werden.
 
> (3) Das Hochschulbibliothekszentrum des Landes Nordrhein-Westfalen unterstützt die Pflichtexemplarsammlung der Universitäts- und Landesbibliotheken sowie die Herausgabe der Nordrhein-Westfälischen Bibliographie durch die Entwicklung und den Betrieb von technischen Infrastrukturleistungen.

Ähnlich dem Gesetzesinhalt sieht auch die tatsächliche Arbeitsteilung aus. Die Redaktionen in den Universitäts- und Landesbibliotheken Münster und Düsseldorf arbeiten an der Erstellung und Pflege der NWBib, wobei sie von der ULB Bonn bei der Erfassung von Monographien unterstützt werden. Das Hochschulbibliothekszentrum fungiert in erster Linie als technischer Dienstleister für Betrieb und Entwicklung der Erfassungsumgebung und des Webauftritts.

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



[^1]: https://nwbib.de