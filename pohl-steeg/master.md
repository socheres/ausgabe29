Aufgaben einer Landesbibliographie:

 > Zitat

Dies gilt so auch für die Nordrhein-Westfälischen Bibliographie, im folgenden "NWBib" abgekürzt. Auf der Webseite des neuen Webauftritts[^1] heißt es:

> Die Nordrhein-Westfälische Bibliographie (NWBib) verzeichnet die Literatur über das Land Nordrhein-Westfalen, seine Regionen, Orte und Persönlichkeiten, Literatur aus allen Lebens- und Wissensbereichen in Geschichte und Gegenwart.

> Die NWBib ist eine der umfangreichsten Regionalbibliographien Deutschlands. Sie erschließt nicht nur Bücher und Zeitschriften, sondern auch Aufsätze und andere Medien wie etwa Karten, DVDs, Hörbücher und elektronische Publikationen. 

Die NWBib verzeichnet mit Stand März 2016 mehr als 370.000 Literaturnachweise, mehr als 60 Prozent davon sind Aufsätze aus Zeitschriften oder Sammelbänden.

### Organisation

Im Unterschied zu anderen Landesbibliographien sind Erstellung, Entwicklung und Betrieb der Nordrhein-Westfälischen Bibliographie (NWBib) gesetzlich verankert. Im Gesetz zur Regelung des Pflichtexemplarrechts in Nordrhein-Westfalen heißt es in §2:

> (1) Die Aufgabe der Sammlung der Pflichtexemplare nehmen die Universitäts- und Landesbibliotheken Bonn, Düsseldorf und Münster gemeinsam wahr. (...)

> (2) Die Bibliotheken erstellen gemeinsam die Nordrhein-Westfälische Bibliographie. Diese verzeichnet und erschließt die Medienwerke mit inhaltlichem Bezug zu Nordrhein-Westfalen unabhängig davon, ob sie innerhalb oder außerhalb Nordrhein-Westfalens verlegt werden.
 
> (3) Das Hochschulbibliothekszentrum des Landes Nordrhein-Westfalen unterstützt die Pflichtexemplarsammlung der Universitäts- und Landesbibliotheken sowie die Herausgabe der Nordrhein-Westfälischen Bibliographie durch die Entwicklung und den Betrieb von technischen Infrastrukturleistungen.

Ähnlich dem Gesetzesinhalt sieht auch die tatsächliche Arbeitsteilung aus. Die Redaktionen in den Universitäts- und Landesbibliotheken Münster und Düsseldorf arbeiten an der Erstellung und Pflege der NWBib, wobei sie von der ULB Bonn unterstützt werden, die sich auf die Erfassung von Monographien beschränkt. Das Hochschulbibliothekszentrum fungiert in erster Linie als technischer Dienstleister für Betrieb und Entwicklung der Erfassungsumgebung und des Webauftritts.

### Historie

Die NWBib ist eine der jüngeren Landesbibliographien Westdeutschlands. Ihre Vorläufer sind die Westfälische Bibliographie, die 1954 an den Start ging und den Zeitraum ab 1945 abdeckt und die Lippische Bibliographie, die ab 1957 erstellt wurde. Mit der Nordrhein-Westfälischen Bibliographie wurden diese Vorläufer fortgeführt und um die bibliographische Verzeichnung von Literatur über das Rheinland ergänzt.

Wie Schmidt, 1998 darstellt wurde von Anfang an auf eine EDV-gestützte Produktion gesetzt, auch wenn die Bibliographie zunächst allein als Druckfassung erschien. Im Vergleich zur heute gängigen Pflege einer Datenbank war der Aufwand zur Erstellung einer gedruckten Bibliographie ungleich größer. Für die ersten zehn Bände beschreibt Schmidt, 1998 das Verfahren wie folgt:

> Die Titel wurden jahrgangsweise maschinenschriftlich auf Erfassungsbögen von den beiden Redaktionsstellen an der UB Düsseldorf und der UB Münster ans HBZ gesandt, dort von Datenerfassungskräften maschinenlesbar als EDT-Dateien erfaßt, von einer weiteren Redakteurin korrekturgelesen und schließlich mit dem GID-Programm verarbeitet. Das Endprodukt waren vier Magnetbänder für die jeweils vier Teile einer Druckausgabe, fertig kodiert mit Steuerzeichen für die Weiterverarbeitung auf einer Lichtsetzmaschine. Diese Bänder wurden vom HBZ einem durch Ausschreibung ermittelten Druckhaus übergeben, welches über eine bestimmte Lichtsetzanlage verfügen mußte, um die Satzsteuerzeichen der Magnetbänder richtig lesen zu können. (Schmidt, 1998)

Ab dem elften Band wurde zur Herstellung eines Bandes der Landesbibligraphie anders verfahren. Der Hauptgrund für die Umstellung des Druckverfahrens war Anfang der 1990er Jahre stattgefundene Anschluss der ULBs Düsseldorf und Münster an den hbz-Verbund. Seitdem existiert die NWBib als eine Untermenge der hbz-Verbunddaten.

- Druckfassung bis Ende 1990er
- Online-Fassung als Nebenprodukt einer effizienteren Druckproduktion mit Latex
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

### Ausblick

- Einbindung der Vorläuferbibliographien in die Recherche

### Literatur

Schmidt, Ronald Michael (1998): *Die Nordrhein-Westfälische Bibliographie Online*. In: Bibliographische Datenbanken im Internet: DFG-Kolloquium vom 4. bis 5. Dezember 1997 an der Herzogin Anna Amalia Bibliothek. URL (Internet Archive): http://web.archive.org/web/20000310115644/http://www.weimar-klassik.de/kolloquien/e5i_224d.html

[^1]: https://nwbib.de