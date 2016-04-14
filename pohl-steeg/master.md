Dieser Artikel beschreibt die Entwicklung eines modernen Webauftritts für die Nordrhein-Westfälische Bibliographie (NWBib) im Kontext der historischen Entwicklung dieser Landesbibliographie. Die Aufgaben einer Landesbibliographie bestimmt @Syre2006, S.34 wie folgt:

> Aufgabe einer Regionalbibliographie ist es, die Literatur über eine Region, ihre historischen und aktuellen Teilgebiete, ihre Naturräume und ihre Orte sowie die mit der betreffenden Region verbundenen Persönlichkeiten (verstorbenen wie lebenden) zu verzeichnen. Deckt sich der geographische Berichtsraum einer Regionalbibliographie mit den Grenzen eines Bundeslandes, spricht man von einer Landesbibliographie.

Dies gilt so auch für die Nordrhein-Westfälische Bibliographie, abgekürzt "NWBib". In der Selbstdarstellung auf der Webseite des neuen Webauftritts[^1] heißt es:

> Die Nordrhein-Westfälische Bibliographie (NWBib) verzeichnet die Literatur über das Land Nordrhein-Westfalen, seine Regionen, Orte und Persönlichkeiten, Literatur aus allen Lebens- und Wissensbereichen in Geschichte und Gegenwart.

> Die NWBib ist eine der umfangreichsten Regionalbibliographien Deutschlands. Sie erschließt nicht nur Bücher und Zeitschriften, sondern auch Aufsätze und andere Medien wie etwa Karten, DVDs, Hörbücher und elektronische Publikationen. 

Die NWBib verzeichnet mit Stand März 2016 mehr als 370.000 Literaturnachweise, mehr als 60 Prozent davon sind Aufsätze aus Zeitschriften oder Sammelbänden. Die Arbeit an einem gänzlich neuen NWBib-Webauftritt erstreckt sich von Januar 2014 bis voraussichtlich zum August 2016.

Dieser Beitrag skizziert die historische Entwicklung der NWBib mit Fokus auf die Beziehung der Bibliographie zum World Wide Web (WWW), beschreibt die Voraussetzungen für die Neuentwicklung sowie die Leitlinien des Entwicklungsprozesses und schließt mit Lessons Learned und einem Ausblick auf weitere Entwicklungen. Da die Autoren beide Teil des Software-Entwicklungsteams am hbz sind, wird die Entwicklungsperspektive hier im Vordergrund stehen. Die Perspektive der NWBib-Redaktion ist demgemäß unterrepräsentiert.

### Rechtliche Voraussetzungen und Verantwortlichkeiten

Die "entscheidende Grundlage für die Bearbeitung einer Landesbibliographie" liefert die Wahrnehmung des Pflichtexemplarrechts (@Syre2006, S. 36). Wie in anderen Bundesländern üblich, wird auch die NWBib von jenen Bibliotheken erstellt, die für die Sammlung und Archivierung von Pflichtstücken zuständig sind. Im Unterschied zu anderen Bundesländern ist die Erstellung, die Entwicklung und der Betrieb der Nordrhein-Westfälischen Landesbibliographie sogar im Pflichtexemplargesetz verankert. So heißt es im *Gesetz zur Regelung des Pflichtexemplarrechts in Nordrhein-Westfalen*, §2:

> (1) Die Aufgabe der Sammlung der Pflichtexemplare nehmen die Universitäts- und Landesbibliotheken Bonn, Düsseldorf und Münster gemeinsam wahr. (...)

> (2) Die Bibliotheken erstellen gemeinsam die Nordrhein-Westfälische Bibliographie. Diese verzeichnet und erschließt die Medienwerke mit inhaltlichem Bezug zu Nordrhein-Westfalen unabhängig davon, ob sie innerhalb oder außerhalb Nordrhein-Westfalens verlegt werden.
 
> (3) Das Hochschulbibliothekszentrum des Landes Nordrhein-Westfalen unterstützt die Pflichtexemplarsammlung der Universitäts- und Landesbibliotheken sowie die Herausgabe der Nordrhein-Westfälischen Bibliographie durch die Entwicklung und den Betrieb von technischen Infrastrukturleistungen.

Ähnlich dem Gesetzesinhalt sieht auch die tatsächliche Arbeitsteilung aus. Die Redaktionsstellen an den Universitäts- und Landesbibliotheken Münster und Düsseldorf arbeiten an der Erstellung und Pflege der NWBib, wobei sie von der ULB Bonn unterstützt werden, die sich auf die Erfassung von Monographien beschränkt. Das Hochschulbibliothekszentrum fungiert in erster Linie als technischer Dienstleister für Betrieb und Entwicklung der Erfassungsumgebung und des Webauftritts.[^satzung] Für den Aufbau des neuen NWBib-Webauftritts war dasselbe Team am hbz verantwortlich, das auch den hbz-Linked-Data-Dienstes lobid (Linking Open Bibliographic Data) betreibt. Das lobid-Team besteht aus zwei Entwicklern (Pascal Christoph mit Schwerpunkt auf dem Backend und Fabian Steeg, der vor allem für das Frontend zuständig ist) und einem wissenschaftlichen Bibliothekar (Adrian Pohl), der für Metadatenstandards, Projektmanagement und Kommunikation verantwortlich ist.

### Historie der NWBib

Die NWBib ist eine der jüngeren Landesbibliographien Westdeutschlands. Ihre direkten Vorläufer sind die Westfälische Bibliographie, die ab 1954 erstellt wurde und den Zeitraum ab 1945 abdeckt und die Lippische Bibliographie, die ab 1957 erstellt wurde.[^vorlaeufer] Mit der Nordrhein-Westfälischen Bibliographie wurden diese Vorläufer fortgeführt und um die bibliographische Verzeichnung von Literatur über das Rheinland ergänzt. Der erste Band der NWBib (Berichtsjahr 1983) ist 1984 erschienen.

#### EDV-gestützte Druckproduktion

Wie @Schmidt1998 darstellt wurde von Anfang an auf eine EDV-gestützte Produktion gesetzt, auch wenn die Bibliographie zunächst allein als Druckfassung erschien. Dennoch war der Aufwand zur Erstellung einer gedruckten Bibliographie ungleich größer im Vergleich zur heute gängigen Pflege einer Datenbank. Für die ersten zehn Bände beschreibt @Schmidt1998 das Verfahren wie folgt:

> Die Titel wurden jahrgangsweise maschinenschriftlich auf Erfassungsbögen von den beiden Redaktionsstellen an der UB Düsseldorf und der UB Münster ans HBZ gesandt, dort von Datenerfassungskräften maschinenlesbar als EDT-Dateien erfaßt, von einer weiteren Redakteurin korrekturgelesen und schließlich mit dem GID-Programm verarbeitet. Das Endprodukt waren vier Magnetbänder für die jeweils vier Teile einer Druckausgabe, fertig kodiert mit Steuerzeichen für die Weiterverarbeitung auf einer Lichtsetzmaschine. Diese Bänder wurden vom HBZ einem durch Ausschreibung ermittelten Druckhaus übergeben, welches über eine bestimmte Lichtsetzanlage verfügen mußte, um die Satzsteuerzeichen der Magnetbänder richtig lesen zu können. (@Schmidt1998)

Bei der Datenerfassung und -korrektur waren also drei Abteilungen beteiligt, ehe die Daten für den Druck vorbereitet werden konnten. @HallerMuehl2006 nennen drei erhebliche Nachteile dieses Verfahrens: Erstens der doppelte Schreibaufwand bei der Erfassung über Datenerfassungsbögen und der Übertragung in ein maschinenlesbarers Format, zweitens das aufwändige Korrekturverfahren bei der jährlichen Druckaufbereitung und vor allem – drittens – das Fehlen einer Datenbank, was eine Dublettenkontrolle und die kontrollierte Verschlagwortung mittels der Schlagwortnormdatei (SWD) unmöglich machte.

#### Mit LaTeX ins Web

Ab der Herstellung des elften Bandes der NWBib (Jahrgang 1993) hat sich das Verfahren geändert. Der Hauptgrund für die Umstellung des Druckverfahrens war der Anschluss der ULBs Düsseldorf und Münster an den hbz-Verbund Anfang der 1990er Jahre, womit die NWBib als Sub-System der hbz-Verbunddatenbank geführt wurde (**?**). Dies ermöglichte nicht nur das Einsparen von Personalressourcen bei der Druckproduktion, sondern auch die Präsentation der NWBib im WWW.

Die gedruckte Version wurde nun mit der Software *LaTeX* vorbereitet. Dafür wurde aus der für den hbz-Verbundkatalog genutzten Datenbanksoftware *BIS* ein mit TeX-Steuerzeichen versehener Export des jeweiligen NWBib-Jahrgangs generiert (@Schmidt1998). Als Nebenprodukt des neuen Verfahrens konnte auf Basis der LaTeX-Datei mit wenig Aufwand eine HTML-Version der NWBib erstellt werden. Mit Hilfe freier Software und nach Aufbringen einer Personenwoche konnte NWBib-Jahrgang 1993 als erstes WWW-Angebot des hbz 1996 bereitgestellt werden. In @Schmidt1998 heißt es:

> Um das Marketing dieses zusätzlichen Angebotes der Bibliographie auf dem Internet brauchten wir uns ... nicht zu kümmern, das haben die Gesetze des World Wide Web sozusagen über nacht [sic] erledigt. Die NWB-Seiten wurden schon bald von den Suchmaschinen entdeckt, eingelesen und indiziert. So kann ein Benutzer auch über eine Recherche in einer Suchmaschine wie z.B. Alta Vista als Treffer auf eine NWB-Seite geführt werden und dort dann mit den Navigationswerkzeugen weitersuchen.

Zusätzlich zur HTML-Variante der Bibliographie wurde 1996 auch der NWBib-Altbestand in die hbz-Verbunddatenbank eingespielt, so dass die gesamte NWBib über den hbz-OPAC durchsucht werden konnte. Datenbanken können aber nicht durch Suchmaschinen indexiert werden – man bezeichnet derartige Angebote als Teil des "Deep Web" –, weshalb allein das HTML-Angebot die Auffindbarkeit der NWBib über Web-Suchmaschinenen ermöglichte.

Ende der 1990er Jahre wurde das hbz-Verbundsystem auf die Software Aleph von Ex Libris umgestellt. Die NWBib-Redaktion nutzte diese Chance, um die NWBib vollständig in den Verbundkatalog zu integrieren (vgl. @HallerMuehl2006, 314f), was u.a. den Vorteil hatte, dass die Nutzer jetzt auch Besitznachweise für die verzeichneten Titel vorfanden. Laut @HallerMuehl2006, 314 fiel mit "dem Beschluss für eine vollständige Übernahme der Bibliographie in das neue Verbundsystem ... auch die Entscheidung, die Druckausgabe aufzugeben und die Bibliographie nur noch als Datenbank anzubieten." Die letzte Druckausgabe der NWBib erschien 1999 mit Berichtsjahr 1997.

2005 wurde auch die HTML-Version der NWBib eingestellt, und es gab nur noch die Möglichkeit einer Recherche über den Web-OPAC, der mittlerweile auf dem Aleph-System von von Ex Libris basierte. Damit verschwand die NWBib aus dem WWW, und die verzeichnete Literatur war nur für die Leute recherchierbar, die von der Existenz der Bibliographie und ihren Möglichkeiten wussten.

#### Der Auftrag zur Modernisierung des Web-Auftritts

Mit dem Aufstieg von Google und Discovery Services in den Bibliotheken wurde die NWbib-Recherche immer weniger zeitgemäßg. Als Reaktion gaben die Landesbibliotheken dem hbz Anfang 2013 den Auftrag, den Webauftritt der NWBib zu überarbeiten. Innerhalb des hbz wurde entschieden, den neuen Webauftritt auf Basis der Programmierschnittstelle (Application Programming Interface, API) des hbz-Linked-Data-Dienstes lobid (Linking Open Bibliographic Data) umzusetzen, die im Herbst 2013 in Produktion gegangen war. Dies sollte u.a. garantieren, dass die NWBib wieder integraler Bestandteil des WWW würde. Anfang 2014 begannen die Entwicklungsarbeiten für den neuen NWBib-Webauftritt.

### Anforderungen an einen modernen Webauftritt

Welche Anforderungen sollte ein moderner Webauftritt erfüllen? @Schnasse2015 hat für einen NWBib-Vortrag beim Bibliothekartag 2015 in Nürnberg eine nützliche Untergliederung von Interessengruppen eines bibliographischen Webauftritts und deren Anforderungen erstellt, an der wir uns hier orientieren.[^4] Es lassen sich vier Interessengruppen unterscheiden:

1. Besucher der NWBib, die nach Literatur recherchieren,
2. Externe Webservices, z.B. Suchmaschinen wie Google, DuckDuckGo oder die Virtuelle Deutsche Landesbibliographie (VDL),
3. die NWBib-Redaktion sowie
4. Web-Entwickler, die auf Basis der NWBib-Daten zusätzliche eigene Anwendungen bauen wollen. 

Im folgenden werden die Anforderungen der verschiedenen Nutzergruppen näher beleuchtet.

#### NWBib-Besucher

Das Ziel von Nutzerinnen und Nutzern einer bibliographischen Rechercheanwendung ist es, Literaturhinweise zu einem bestimmten Thema sowie Hinweise zu Zugriffsmöglichkeiten zu bekommen, im besten Fall mit einem direkten Link zum Volltext. Darüber hinaus erwarten Nutzerinnen und Nutzer im Allgemeinen von einer Webanwendung folgende grundlegende Eigenschaften:

- Verlässlichkeit/Verfügbarkeit
- Übersichtlichkeit
- Intuitive Nutzbarkeit
- Schnelle Ladezeiten

Über diese allgemeinen Anforderungen hinaus, variieren die Anforderungen je nach Nutzungstypus. Eine regelmäßig wiederkehrende Besucherin, die etwa spezielle wissenschaftliche Literatur sucht, wird andere Wünsche und Anforderungen haben als ein Besucher, der über eine Google-Suche direkt auf einen Einzeltreffer gelangt. Letzterer will sich erst einmal auf einfache Weise orientieren, auf was für eine Seite er da gelangt ist und welche Informationen sie ihm bietet. Letztere könnte hingegen Interesse haben, komplexere Recherchefunktionen einzusetzen.
 
Bisher haben wir darauf verzichtet, systematisch herauszufinden, wie zufrieden Endnutzer/innen mit dem NWBib-Webauftritt sind und welche Dinge verbesserungswürdig sind. Im Zuge der kontinuierlichen Weiterentwicklung des Auftritts planen wir Usability-Studien im Jahr 2017.

#### Externe Webservices

Externe Websites lassen sich in verschiedene Typen mit unterschiedlichen Anforderungen an eine Rechercheanwendung untergliedern:

- *Suchmaschinen* crawlen große Mengen von Webseiten und verwerten zunehmend darin angebotene strukturierte Daten.
- Andere möchten die NWBib über eine dokumentierte Schnittstelle abfragen und strukturierte Daten als Antwort bekommen, um die Ergebnisse in ihrem Webauftritt präsentieren. Dazu zählt zum Beispiel die Virtuelle Deutsche Landesbibliographie (VDL).
- Andere wie die *Website der NRW-Landesbibliotheken* möchten die NWBib-Anwendung als Ganzes – inklusive erweiterter Suchmaske und Facettierungsmöglichkeiten – in ihren Webauftritt integrieren.

#### NWBib-Redaktion

Die NWBib-Redaktion bewertet die Funktionalitäten des NWBib-Auftritts in erster Linie vor dem Hintergrund der von ihr erfassten Daten, dem dabei benutzten Regelwerk zur Formalerschließung und den verschiedenen Methoden zur Inhaltserschließung. 

Konkret erwartet die NWBib-Redaktion zum Beispiel folgende Funktionalität:

- Angeboten werden sollte eine erweiterte Suche über verschiedene Felder, die mittels Boolescher Operatoren kombiniert werden können.
- Die Ergebnismenge einer Anfrage soll mit jener in der Aleph-Recherche übereinstimmen, was etwa Methoden wie Stemming o.ä. ausschließt.
- Die Ergebnisliste soll standardmäßig nach Erscheinungsjahr sortiert sein.
- Treffer sollten auf eine Merkliste gesetzt werden können, die exportiert werden kann.

So hat die Redaktion zum Ziel, dass die Daten entsprechend den Feldern, Unterscheidungen, Verknüpfungen und Details in den Ausgangsdaten präsentiert werden. Die – teils komplexen – Recherchemöglichkeiten, die die Datenbasis ermöglicht, sollen ausgenutzt werden.

Momentan ist die NWBib-Redaktion jener Stakeholder, der am meisten Einfluss auf den Entwicklungsprozess nehmen konnte.

#### Web-Entwickler

Grundsätzlich versucht das hbz mittels dem lobid-Dienst, offene bibliothekarische Daten so bereitzustellen, dass interessierte Dritte diese innerhalb eigener Anwendungen nutzen können. Damit Entwickler die Daten in eigenen Webanwendungen integrieren können, benötigen sie gut dokumentierte performante und zuverlässige Schnittstellen zu den Daten. Zudem sollten die angebotenen Daten bestenfalls explizit offen lizenziert sein.

### Bibliothekarische Voraussetzungen

Wie bereits erwähnt wird die NWBib als Untermenge des hbz-Verbundkatalogs mit der Software *Aleph* der Firma Ex Libris katalogisiert. Zur Identifizierung von NWBib-Titeln wird ein Sortierzeichen in Feld 078n gesetzt.[^2]

Die Titelerfassung für die NWBib geschieht nach den *Regeln für die alphabetische Katalogisierung in wissenschaftlichen Bibliotheken* (RAK-WB) und seit Beginn dieses Jahres nach *Resource Description and Access* (RDA). Die Inhaltserschließung wird zum einen nach den *Regeln für den Schlagwortkatalog* (RSWK) mithilfe der Gemeinsamen Normdatei (GND) durchgeführt, zum anderen findet eine Klassifizierung statt anhand der NWBib-spezifischen Systematik, die in einen Sachsystematik- und einen Ortssystematikteil[^3] untergliedert ist. Ergänzt wird die NWBib-Ortssystematik zudem durch sogenannte "Gliedernde Schlagwörter", das sind unkontrollierte Einträge von Ortsnamen zur genaueren räumlichen Verortung des Sachbezugs eines Titels. Zudem arbeitet insbesondere die ULB Münster an der Verzeichnung von Schlagwortfolgen, die auch im neuen Webauftritt nutzbar gemacht werden.

### Der Webauftritt

Die Startseite des neuen NWBib-Webauftritts bietet ein Suchfeld für den einfachen Einstieg, eine Beschreibung der NWBib sowie eine Karte für die ortsbasierte Suche, bei der zwischen Kreis- oder Gemeindeebene gewählt werden kann:

![Startseite](img/nwbib-screenshot-startseite.png "Startseite")

Über das Suchfeld und die kartenbasierte Ortsfacette können auf einfache Weise inhaltliche und räumliche Suchkriterien kombiniert werden, hier z.B. wurde die textbasierte Suche nach "braunkohle" durch eine Auswahl in der Karte auf eine Suche von Ressourcen über Braunkohle im rheinischen Braunkohlerevier eingeschränkt:

![Ergebnisliste](img/nwbib-screenshot-ergebnisliste.png "Ergebnisliste")

Weitere Facetten bieten Möglichkeiten zur Einschränkung der Ergebnisse nach inhaltlichen Kriterien, nach Medien- und Publikationstypen, sowie nach Bestand in bestimmten Bibliotheken:

![Facetten](img/nwbib-screenshot-facetten.png "Facetten")

Die Detailansicht eines Treffers bietet über Links Möglichkeiten zum Suchen nach weiteren Treffern desselben Urhebers und derselben inhaltlichen Erschliessung sowie auf einer Karte Details zum Bestand und, wenn verfügbar, Links zum Abfragen der Verfügbarkeit im lokalen Katalog der Bibliotheken:

![Detailansicht](img/nwbib-screenshot-detailansicht.png "Detailansicht")

Neben dieser grundsätzlichen Funktionalität bietet der Auftritt über die Menüleiste eine erweiterte Suche in bestimmten Feldern, eine Themensuche über inhaltserschließende Schlagwortfolgen, Zugriff auf Titel über die Raum- und Sachsystematik, sowie eine Merkliste zum Zusammenstellen und Drucken einer Literaturliste.

### Der Entwicklungsprozess

Die Software für den neuen NWBib-Webauftritt wird schrittweise in stetigem Austausch mit der NWBib-Redaktion entwickelt. Der Entwicklungsprototyp war von Beginn der Entwicklung an offen im Web erreichbar und dient als Referenzpunkt für die Diskussion über offene Anforderungen und bestehende Softwarebugs. An ihm wird kontinuierlich weiterentwickelt (inkrementelle Entwicklung). Für verschiedene Recherchefunktionen sowie teilweise auch für die Einzeltrefferanzeige konnte zudem die Aleph-basierte Version der NWBib als Referenz herangezogen werden.

Zunächst war die Beendigung der Testphase (Beta) des neuen Webauftritts vom Entwicklungsteam für Ende 2014 geplant, weil danach der Hauptentwickler für einige Monate in Elternzeit ging. Der offizielle Launchtermin wurde jedoch mehrmals nach hinten verschoben. Im April 2016 haben die Leitungen der Landesbibliotheken mitgeteilt, dass das Angebot nun beworben werden könne. Eine öffentliche Vorstellung des neuen Auftritts wird Ende August im Rahmen der Feierlichkeiten zu 70 Jahren NRW stattfinden.

#### Rollen und Kommunikation

Für die technische Entwicklung des NWBib-Webauftritts ist ein Entwicklungsteam im hbz verantwortlich, das die Anforderungen der NWBib-Redaktion umsetzt. Das Team besteht aus zwei Entwicklern und einem wissenschaftlichen Bibliothekar, der die Rolle eines Product Owners übernimmt und damit vor allem für die Kommunikation zwischen dem Entwicklungsteam und der NWBib-Redaktion verantwortlich ist. Die drei Mitglieder des Entwicklungsteams arbeiten zusammengenommen etwa im Umfang von 1,5 Vollzeitstellen an dem Projekt.

Um die Anforderungen zu definieren, zu priorisieren, umzusetzen und die erfolgreiche Umsetzung abzunehmen, mussten die beteiligten Akteure viel und regelmäßig miteinander kommunizieren. Dies geschah in erster Linie über eine gemeinsame Mailingliste und ein Wiki[^wiki]. Zudem gab es zwei persönliche Treffen im hbz im September 2014 und April 2015.

Zunächst dienten verschiedene von der Redaktion verschickte oder beim gemeinsamen Treffen erstellte Anforderungslisten als Entwicklungvorgaben. Da Fragen der Priorisierung teilweise unklar waren und das Entwicklungsteam einen baldigen Launch des neuen Webauftritts anvisierte, wurden nach etwa einem Jahr Entwicklung im Februar 2015 die verbliebenen Anforderungen durch die NWBib-Redaktion zusammengeführt und priorisiert. So entstand eine strukturierten Übersicht von Anforderungen, die für den Launch des neuen NWBib-Webauftritt unverzichtbar seien.[^prio] Diese Liste diente fortan als Bezugspunkt für die ganze weitere Entwicklung und die Kommunikation zwischen den Projektbeteiligten. Mit der Zeit wurden einige der Anforderungen konkretisiert bzw. in detailliertere Aufgabenpakete aufgeteilt.

Der typische Ablauf zur Umsetzung von Anforderungen sah wie folgt aus:

1. Eine Anforderung oder ein Softwarebug wird von der Redaktion gemeldet.
2. Der Product Owner legt ein oder mehrere Tickets an für die Umsetzung der Anforderung bzw. die Behebung des Bugs.
3. Der Product Owner priorisiert die offenen Tickets gemeinsam mit dem Rest des Entwicklungsteams und weist das Ticket einem Entwickler zu.
4. Der Entwickler arbeitet so lange an der Umsetzung des Tickets, bis er meint, die Anforderungen werden hinreichend erfüllt.
5. Die neue bzw. reparierte Funktionalität und der Code wird durch Mitglieder des Entwicklungsteams begutachtet.
6. Sobald die Begutachtung positiv ist, wird die Anpassung auf dem offen einsehbaren Entwicklungsprototyp produktiv.
7. Ist eine relvante Anzahl von Änderungen produktiv (dies sind meist fünf oder mehr Anpassungen), schickt der Product Owner eine Mail an die gemeinsame NWBib-Mailingliste mit der Bitte um Begutachtung durch die NWBib-Redaktion.
8. Die NWBib-Redaktionsstellen stimmen sich untereinander ab, ob die Anpassungen den Anforderungen genügen. Sodann melden sie das Ergebnis der Abstimmung via Mailingliste an das Entwicklerteam.
9. Ist die Rückmeldung positiv, wird die Entwicklung der Funktionalität als abgeschlossen erklärt, indem die Anforderung im Wiki entsprechend markiert wird. Andernfalls arbeitet das Enticklungsteam an der gewünschten Anpassung und der Prozess setzt wieder bei Punkt 4. ein.

Das Entwicklungsteam arbeitete nicht ausschließlich an der NWBib und die Abstimmung der NWBib-Redaktionsstellen zur Begutachtung des Fortschritts nahm einige Zeit in Anspruch. Zudem fielen alle Teammitglieder in unterschiedlichen Zeiträumen während der Entwicklungszeit wegen Elternzeit aus. Dementsprechend variiert die Länge eines Entwicklungszyklus vom Melden einer Anforderung/eines Bugs bis zur endgültigen Abnahme durch die Redaktion erheblich: Wenn keine Urlaubszeit war und alle Beteiligten da waren, dauerte ein Zyklus zwei bis drei Wochen, in Abwesenheit des Hautentwicklers mehrere Monate.

Neben den Anforderungen der NWBib-Redaktion hat das Entwicklungsteam auch eigene Vorstellungen umgesetzt. So wurden manche Use Cases durch andere Funktionalitäten gelöst als ursprünglich von der Redaktion gefordert. In anderen Fällen setzte das Entwicklungsteam eigene Ideen um – so etwa die Visualisierung von Suchergebnissen oder Bestandsinformationen auf einer Karte. Auch diese Umsetzungen wurden dann der Redaktion zur Begutachtung vorgelegt (Schritt 7).

#### Entwicklungsmethodologie

Die Methodologie zur Entwicklung des NWBib-Auftritts bedient sich bei verschiedenen Ansätzen der agilen Softwarentwicklung (@becketal2001).[^dev] Die Software wird – wie bereits beschrieben – inkrementell in stetigem Austausch mit der NWBib-Redaktion entwickelt. Als Kommunikationswerkzeuge benutzt das Entwicklungsteam vor allem GitHub sowie zusätzlich zur Visualisierung, Priorisierung und Organisation der Aufgaben die GitHub-basierte Kanban-Software *Waffle*.[^waffle] Vom Scrum-Ansatz[^scrum] wird das Stand-up übernommen, ein kurzes tägliches Treffen, bei dem sich die Teammitglieder über ihre erledigten und anstehenden Aufgaben austauschen und aktuelle Probleme benennen. Der Entwicklungsprozess folgt dem GitHub-Flow[^flow].

### Technologie

Die Implementierung des NWBib-Webauftritts verwendet Java- und Web-Technologie und basiert komplett auf Open-Source-Software.

#### Überblick

Wie oben beschrieben, werden die Daten der NWBib im Bibliothekssystem Aleph katalogisiert. Die Daten werden in einem XML-Format exportiert und mithilfe des Datentransformationstools Matafacture in JSON-LD gewandelt. Diese JSON-Daten werden in Elasticsearch indexiert und über die Lobid-API im Web bereitgestellt. Die NWBib-Webanwendung greift über HTTP auf diese API zu. API und NWBib sind auf Basis des Play-Frameworks implementiert, die NWBib verwendet zusätzlich das HTML/CSS-Framework Bootstrap.

Die folgende Abbildung bietet einen Überblick über diese Komponenten und den Datenfluss aus Aleph in die NWBib:

![Datenfluss](img/data-workflow.svg "Datenfluss")

Java-basierte Ansätze zur Entwicklung von Webanwendungen sind im Bibliothekswesen nach unserem Eindruck relativ selten. Wir wollen daher an dieser Stelle einen kurzen Einblick in die von uns verwendete Technologie und den damit verbundenen Ablauf der Webentwicklung geben. Auf die nur indirekt über die Lobid-API verwendeten Komponenten Metafacture und Elasticsearch gehen wir an dieser Stelle nicht ein.

#### Webentwicklung mit Java

Historisch betrachtet hat Webenwticklung mit Java den Ruf, schwergewichtig und komplex zu sein. Dies liegt vor allem an den Frameworks und Tools, die als Teil der Java-Enterprise-Edition (Java-EE, früher J2EE) zum Einsatz kommen. Applikationsserver und GUI-Frameworks (z.B. Java-Server-Faces, JSF), die als Abstraktionsschicht das Hypertext-Transfer-Protocol (HTTP) vom Entwickler wegkapseln, sind unter bestimmten Umständen für die Entwicklung von Unternehmenssoftware in großen Teams geeignet, für typische Webapplikationen aber häufig nicht optimal.

Hier haben sich leichtgewichtigere Frameworks und Technologien wie PHP und Ruby on Rails etabliert. Diese sind näher an den zugrundeliegenden Web-Technologien wie HTTP und HTML, und erlauben einen schnelleren Entwicklungszyklus: Änderungen im Quellcode werden einfach gespeichert und die Seite im Browser neu geladen. Diese Vorteile dynamischer Sprachen wie PHP, Perl oder Ruby überwiegen gerade in Projekten, die von einem einzigen Entwickler oder einer einzigen Entwicklerin umgesetzt werden deren Nachteile, speziell die höhere Fehleranfälligkeit durch dynamische Typisierung.

Eine statische Typisierung wie in Java hat neben einer höheren Laufzeitperformanz auch für die Arbeit im Team Vorteile: viele Fehler, die durch Änderungen im Quellcode eingeführt werden, werden durch die Typisierung früh erkannt, nämlich nicht erst bei der Verwendung einer bestimmten Funktionalität, z.B. beim Zugriff auf eine bestimmte Seite, sondern schon bei der Kompilierung des Quellcodes, und damit bevor die Seite überhaupt aufgerufen wird. Die Überprüfung kann zudem sehr einfach automatisiert werden, so dass der fehlerhafte Code erst gar nicht ins Code-Repository hochgeladen wird.

#### Webentwicklung mit Play

Das von uns verwendete Play-Framework verbindet die Vorteile der schnellen Entwicklungszyklen und Web-nativen Entwicklung mit der Typsicherheit von Java: bei der Verwendung des Play-Frameworks können wie bei PHP oder Rails nach dem Editieren des Quellcodes die Seiten einfach neu geladen werden. Die nötige Kompilierung erfolgt inkrementell und on-the-fly im Hintergrund. 

Wesentliche Komponenten bei der Webentwicklung mit Play sind Routen, Controller und Templates:

- Routen beschreiben die HTTP-URLs der Anwendung, deren Query-Parameter und den entsprechenden Controller-Aufruf
- Controller werden bei Aufruf der entsprechenden URLs ausgeführt. Sie verarbeiten den ankommenden HTTP-Request und erzeugen eine HTTP-Response, z.B. indem sie ein Template aufrufen
- Templates erzeugen das darzustellende HTML und können dazu beliebige aus den Controllern übergebene Daten verwenden

Alle drei Komponenten werden dabei von Play typsicher verarbeitet. Wird etwa eine Route definiert, bei der z.B. ein `size` Parameter vom Typ `Int` an einen Controller übergeben wird, der einen `String` erwartet, erkennt der Compiler dies bei Start der Anwendung. Ebenso wenn etwa im Template ein Wert als `String` verwendet wird, der aber im Controller als `JsonNode` übergeben wurde. Fehler in Routen, Controllern und Templates werden so früh erkannt, ohne dass dazu erst die betroffene Funktionalität der Anwendung ausgeführt werden muss.

So ermöglicht das Play-Framework moderne Web-Entwicklung nah am HTTP, mit effizienten Entwicklungszyklen, performater Laufzeit und typsicherem Code.

### Herausforderungen & Lessons Learned
 
 Im Laufe des Projekts sind die Beteiligten einigen Herausforderungen begegnet, und das lobid-Team hat eine Menge gelernt. Im folgenden werden einige Herausforderungen und Lessons Learned aus Sicht des Entwicklungsteams erläutert.
 
#### Daten und Recherche
 
 Die NWBib basiert auf der lobid-API, die unter anderem Zugriff auf die hbz-Verbundkatalogdaten sowie die Daten des deutschen ISIL-Verzeichnisses ermöglicht. Für die Bereitstellung der Schnittstelle werden die Quelldaten, die in einem Aleph-XML-Exportformat (hbz-Verbunddaten) sowie Pica+-XML (ISIL-Daten) vorliegen, nach RDF/Linked Data überführt. Die Transformation von bibliothekarischen MAB-/MARC-basierten Daten in eine für Entwickler leicht zu nutzende Datenstruktur ist alles andere als trivial. Auch wenn für die Bereitstellung der lobid-API bereits eine Menge Vorarbeiten stattgefunden hatten, mussten im Zuge der Entwicklung des neuen NWBib-Webauftritts einige Herausforderungen auf Datenebene gemeistert werden, um die gewünschten Funktionalitäten anbieten zu können.

*JSON-LD und Elasticsearch*: Ein grundlegendes Problem mit dem JSON-LD, das in die Elasticsearch-Suchmaschine indexiert wird, war schon seit Anfang 2014 bekannt. Die verwendeten existierenden Java-JSON-LD-Tools bieten beschränkte Möglichkeiten zur Überführung von N-Triples in JSON-LD, so dass das resultierende JSON-LD nicht die optimale Struktur aufweist. Es hat keine geschachtelte Baumstruktur, sondern ein flache Struktur, so dass sich viele Möglichkeiten der Suchmaschine nicht nutzen lassen. Als Ergebnis wurde im Mai 2014 die Planung für eine Version 2.0 der lobid-API begonnen. Die Generierung eines für Elasticsearch optimierten JSON-LD ist eines der Hauptziele.

*Körperschaftssuche*: Die NWBib-Redaktion besteht auf einer Suchmöglichkeit bibliographischer Ressourcen auf Basis von beteiligten Körperschaften. Da bei der bisherigen Datenmodellierung ein solcher Anwendungsfall nicht berücksichtigt wurde, waren einige temporäre Anpassungen möglich, um eine Körperschaftssuche anbieten zu können. Für die erwähnte komplette Neuüberarbeitung der Datenstrukturen (lobid-API 2.0) wurde schließlich beschlossen, eine grundlegende Unterscheidung von Körperschaften und Personen auf Feldebene umzusetzen, damit eine Körperschaftssuche einfach umsetzbar ist.
 
*Schlagwortfolgen*: Wie oben bereits erwähnt sind eine Menge der NWBib-Titel mit einer oder mehreren Schlagwortfolgen versehen. Generell ist die Abbildung von Reihenfolgen in RDF umständlich und wurde bisher auch nicht umgesetzt. Um Schlagwortfolgen anzeigen zu können wurde im Laufe des Projekts eine temporäre Lösung gewählt, in der Schlagwortfolgen als Ganzes in einem extra Feld gespeichert werden. Mit der API 2.0 wird sich das ändern und Schlagwörtern – wie auch Autoren – werden in einer geordneten Liste in der richtigen Reihenfolge gespeichert werden.

*RDA-Umstellung*: Wie bei der Katalogisierung und wie in allen anderen bibliothekarischen Rechercheumgebungen auch, mussten mit der Umstellung auf die neuen Katalogisierungsregeln *RDA* einige Anpassungen an der Transformation der Daten aus dem Verbundkatalog nach RDF vorgenommen werden. Die wichtigsten Anpassungen sind bereits umsetzt, einige stehen aber noch aus.
 
*Filterung nach Publikations- und Medientypen*: Für die NWBib wurde eine Facettierung nach "Publikationstyp" und "Medientyp" umgesetzt. Die Katalogisierung nach RAK-WB hat sich als sehr ungünstige Basis herausgestellt zum Aufbau einer nützlichen Facettierung. Auf Basis von Vorarbeiten für die DigiBib wurde eine brauchbare Lösung erreicht.[^typfacette] Im Hinblick auf den Medientyp sind die neuen RDA-Katalogisierungsregeln zu begrüßen, die eine in sich schlüssige Unterscheidung und Erfassung von Inhaltstyp, Medientyp und Datenträgertyp (IMD) vorgeben.[^imd]
 
*Gliedernde Schlagwörter*: Als fortwährendes und bis heute nich gelöstes Problem erwiesen sich die von der NWBib-Redaktion so genannten "Gliedernden Schlagwörter" (GSW). Diese sind der groben Ortsklassifikation beigeordnet und geben einen konkreten Ort, auf den sich der Inhalt eines Titel bezieht. Dabei kann es sich um Angabe eines Orts (z.B. "Köln") oder eines Ortsteils (z.B. "Köln-Ehrenfeld") handeln. Diese Schlagwörter sind nicht normiert, so dass es für denselben Ort verschiedene Schreibweisen geben kann. Schon früh gab es den Wunsch, die GSW in die normierte Systematik zu integrieren und im Zuge dessen verschiedene Schreibweisen zu eliminieren. Eine vernünftige und zukunftssichere Lösung ist allerdings nur unter Anpassung der Quelldaten in der Aleph-Verbunddatenbank machbar und sollte mit einer Änderung der Katalogisierungspraxis einhergehen. Da sich hier keine einfache Lösung anbietet, wurde die Umsetzung auf die Zeit nach dem offiziellen Launch der NWBib vertagt. Aus Sicht des Entwicklungsteams sollte es Ziel sein, die Ortssystematik um Orte und Ortsteile zu erweitern bzw. bestehende Ortsdatenbanken wie GeoNames oder Wikidata zu nutzen, um eine kontrolierte Erfasung zu gewährleisten.
 
*Aleph-Datenbanksuche als Vorbild*: Die NWbib-Redaktion hat bei der Begutachtung des Entwicklungsprototypen stets die Aleph-basierte NWBib-Recherche zum Maßstab genommen. Die Forderung war, dass bei gleicher Suchanfrage auch die gleiche Anzahl von Treffern ergeben sollte. Da eine Suchmaschine anders funktioniert als die relationale Datenbank des hbz-Vernundkatalogs, mussten hier einige Anpassungen vorgenommen werden. So musste etwa die Volltextsuche über alle Felder auf bestimmte Felder eingeschränkt werden, damit die Anzahl der Treffer bei einer freien Suche mit der Aleph-Suche übereinstimmte. Zur Lösung des Schiller-Räuber-Problems (@wikipedia2016) wurde allerdings von dieser Vorgabe abgewichen. Somit können nun auch die Bände eines mehrbändigen Werks durch eine Kombination von Autorenname und Titel in der NWBib gefunden werden.
Auch in Bezug auf die Sortierung der Suchergebnisse gab es Uneinigkeiten. Während das lobid-Team die Möglichkeiten der Suchmaschine ausnutzen und standardmäßig die Suchergebnisse mit einer Relevanzsortierung anbieten wollte, bestand die NWBib-Redaktion auf der Sortierung nach Veröffentlichungsdatum als Default-Einstellung.

#### Zusammenarbeit

*Agile Entwicklung* als Herausforderung: Inkrementelles, transparentes offenes Arbeiten noch nicht verinnerlicht. Präsentation unfertiger Produkte, die in Arbeit sind, ist schwierig
*Englisch als Ticketing-Sprache* nicht unbedingt die beste Wahl

#### Endnutzereinbindung

Wurde vom lobid-Team mehrmals angesprochen: Wer sind die Stakholder/Nutzergruppen? Worauf sollte man mit Blick auf die Endnutzer bei der Entwicklugn achten?
Usability wurde bisher nicht getestet. Für 2017 angedacht.

### Ausblick

- API 2.0 und alle Vorteile, die das mit sich bringt
- Einbindung der Vorläuferbibliographien in die Recherche
- hbz-Katalog auf Basis der NWBib-Entwicklung
- Usability-Studien
- Export für Literaturverwaltungssysteme; @zumsteinstoehr2015

### Literatur

* @becketal2001
* @HallerMuehl2006
* @Pichler2009
* @Schmidt1998
* @Schnasse2015
* @Syre2006
* @wikipedia2016

[^1]: [https://nwbib.de](https://nwbib.de)
[^2]: Eigentlich ein System basierend auf dem MARC-Standard, wurde Aleph für den deutschsprachigen Raum angepasst, um mit MAB verwendet werden zu können.
[^vorlaeufer]: Für eine umfassendere Darstellung der NWBib-Vorläufer siehe @HallerMuehl2006, 305ff.
[^3]: Siehe [http://nwbib.de/classification?t=Sachsystematik](http://nwbib.de/classification?t=Sachsystematik) und [http://nwbib.de/classification?t=Raumsystematik](http://nwbib.de/classification?t=Raumsystematik).
[^4]: Siehe @Schnasse2015, Folie 5.
[^wiki]: Siehe [https://wiki1.hbz-nrw.de/x/mYyW](https://wiki1.hbz-nrw.de/x/mYyW).
[^prio]: Siehe [https://wiki1.hbz-nrw.de/x/CoCDAw](https://wiki1.hbz-nrw.de/x/CoCDAw).
[^dev]: Für eine detaillierte Beschreibung des Entwicklungsprozesses im lobid-Team (allerdings in Englisch) siehe http://hbz.github.io/#dev-process. [https://hbz.github.io/#dev-process](https://hbz.github.io/#dev-process).
[^waffle]: Siehe das gemeinsame Waffle-Board für alle Projekte des lobid-Teams: https://waffle.io/hbz/lobid
[^scrum]: Siehe etwa @Pichler2009.
[^flow]: Siehe [https://guides.github.com/introduction/flow/](https://guides.github.com/introduction/flow/) sowie die Dokumentation des lobid-Entwicklungsprozesses: [http://hbz.github.io/#dev-process](http://hbz.github.io/#dev-process).
[^satzung]: Die "technische Organisation und Präsentation der Nordrhein-Westfälischen Bibliographie" ist auch in der Satzung des Hochulbibliothekszentrums explizit genannt, s. https://www.hbz-nrw.de/ueberuns/satzung/ (§2, Abs. 3 a, Punkt 7).
[^typfacette]: Siehe [https://wiki1.hbz-nrw.de/display/SEM/Facetten+ueber+hbz01-Daten](https://wiki1.hbz-nrw.de/display/SEM/Facetten+ueber+hbz01-Daten).
[^imd]: Vgl. die Folien  der AG RDA zum Thema: [https://wiki.dnb.de/download/attachments/105260204/Modul_2_04_IMD.pptx](https://wiki.dnb.de/download/attachments/105260204/Modul_2_04_IMD.pptx).
