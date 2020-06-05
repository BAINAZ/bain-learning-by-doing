---
title: "Metadaten & Schnittstellen"
date: 2020-06-05
---

Gestartet haben wir wie immer mit einem Ausblick auf den Tag un einem Rückblick zu einzelnen offenen Fragen der letzten Session.
Danach ging es los mit:

##OpenRefine
![00_open refine](https://user-images.githubusercontent.com/61733461/83861997-a0196680-a721-11ea-9c7b-ba790e1a2983.jpg)
*Bildquelle: https://openrefine.org/*

Dazu hatten wir bereits im Vorbereitungsauftrag die [Library Carpentry Lesson zu OpenRefine](https://librarycarpentry.org/lc-open-refine/).
Im Unterricht wurden dann nochmals die verschiedenen Stärken angeschaut, aber natürlich auch ein zwei Punkte, wo OpenRefine nicht so gut geeignet ist:
* OpenRefine unterstützt verschiedene Informationswissenschafts
* Es ist besonders geeignet für tabellarische Daten (Komma oder Tab-separierte Daten oder Daten mit wirkliche festen Spaltenbreiten)
* Bequem ist, dass OpenRefine auch einfaches XML oder JSON verarbeiten & modellieren kann
* Bei komplexen XML ist es dann aber mühsam und erfordert viel Zusatzaufwand. Darum ist es dafür nicht zu empfehlen.
* OpenRefine kann in Kombination mit MarcEdit für MARC21 verwendet werden (zu MarcEdit hatten wir auch ein [Vorbereitungs-Library-Carpentry-Tutorial](https://librarycarpentry.org/lc-marcedit/01-introduction/index.html))

Mit OpenRefine kann man bei grossen Datenlieferungen die Daten erstmal durchschauen. So kann man einschätzen, wie einheitlich die Daten schon sind. Laut Felix Lohmeier brauchen auch von den besten Datenpaketen mindestens 20% der Daten eine Überarbeitung. Weil der Abgleich mit Normdaten (z.B. mit der GND oder VIAF) sehr beliebt ist, wird der Bereich im Moment auch stark weiterentwickelt.
Wenn man mit OpenRefine arbeiten möchte, sollte man sich bewusst sein, dass es auf das Arbeiten in Desktop-Umgebung konzipiert ist.


	##XSLT Corsswalks mit MarcEdit

Bei den Crosswalks geht es um die Konvertierung von einem Metadatenstandard in einen anderen, z.B. MARC21 zu Dbulin Core
Das Problem dabei ist, dass MARC21 sehr viele Felder hat, mehr als andere Standards. Darum lässt sich das nicht 1:1 übertragbar. Dann müssen schlussendlich trotzdem wieder Menschen überlegen, welches Feld das für die Umwandlung genommen wird. Es gibt aus diesne Gründen halt häufig kleine Verluste.

Die Umwandlung selber passiert über XSLT:
XSL ist die Sprache, das T steht für Transformation. Grundsätzlich ist es einfach eine spezielle Programmiersprache des W3C für die Umwandlung.

In der Gruppe haben wir auf dem Bildschirm von Erica gemeinsam eine MARC21-Datei in eine JSON-Datei umgewandelt. Das sah so aus:

![02-Marc-Tool-Rückmeldung](https://user-images.githubusercontent.com/61733461/83886839-e97cac80-a747-11ea-8ca2-8ebf82102eb9.jpg)
![03-Marc-Tool-json-ergebnis](https://user-images.githubusercontent.com/61733461/83886841-ea154300-a747-11ea-8e6a-3843ff97cf9f.jpg)
![01Marc-tools](https://user-images.githubusercontent.com/61733461/83886842-ea154300-a747-11ea-9290-b64bc44223da.jpg)

Die haben wir die Datei überprüft und das JSON schein valide zu sein. Ob es denn auch vollständig ist, das ist eine andere Sache…
Auf der einen Seite sind die Konvertierungen also sehr praktisch, "Trotzdem kann man der Übertragung nicht blind vertrauen, so einfach ist das leider nicht.", schloss Herr Lohmeier das Kapitel.

## Austauschprotokolle für Metadaten (OAI-PMH, SRU)
Search/Retrieve via URL, kurz SRU, und Open Archives Initiative Protocol for Metadata Harvesting, kurz OAI-PMH, sind zwei Beispiele für Übertragungsprotokolle im Bibliotheks- und Archivbereich.
Wieder in unserer Gruppe lasen wir uns kurz in SRU ein und testeten danach live im Swissbib mit SRU-Funktion:
http://sru.swissbib.ch/

Nachdem wir erst einmal durch Probieren herausgefunden haben, dass wir mit dem Bibliothekscode (E27 für FH Graubündenbibliothek) suchen mussten, konnten wir die folgende Frage absetzen:

![04-SRU-Swissbib](https://user-images.githubusercontent.com/61733461/83887134-4d9f7080-a748-11ea-869e-0d4ac3df8320.jpg)
Das führte zum Ergebnis von 1146 Treffer im XML-Format:
![05- Ergebnisse](https://user-images.githubusercontent.com/61733461/83887157-585a0580-a748-11ea-8a30-4cf600a1f0e5.jpg)
Wenn man sich die Ergebnisse im Dublin Core ausgeben lässt, verbessert sich meiner Meinung nach die Lesbarkeit enorm:

![06_Ergebnis-dc](https://user-images.githubusercontent.com/61733461/83887195-6576f480-a748-11ea-8e16-2c9d7b15c786.jpg)

Zur Lösung der Aufgabe zu OAI-PMH mit Swissbib sind wir dann leider nicht mehr gekommen. Die fanden wir alle schwieriger, weil sie nicht so schöne vorgefertigte Schablonen hatte sondern über Sprachkommandos funktioniert. Herr Lohmeier hat uns dann die Auflösung gezeigt, gerne kannst du das im SKRIPT!!! nachlesen. Mein Fazit: Verwende doch lieber SRU, es ist viel einfacher.

Nach einer kurzen Pause stellte uns Herr Lohmeier noch weitere Tools zur Metadatentransformation vor. Zur BOLD"Nutzung von JSON-APIs" zeigte er uns auch noch zwei Beispiele. Beide Themen könnt ihr auch im Skript (LINK) nachlesen.

Vor dem Mittag gab es noch eine kurze Repetition zu Solr, zu welchem wir ebenfalls ein [Tutorial](https://lucene.apache.org/solr/guide/8_5/solr-tutorial.html) im Voraus erhalten haben. Solr ist sehr weit verbreitet und wird auf den meisten Seiten zur Volltextsuche verwendet. Eine Stärke von Solr ist, dass es sehr viele Dateiformate importieren und die Metadaten dazu auslesen kann.
Für Solr wurde extra die Disscovery-Lösung VuFind entwickelt.Anmerkung am Rande: auch das teure Primo von Ex Libris basiert auf Solr…

Am Nachmittag gings dann weiter mit VuFind. Auch das wird ständig weiterentwickelt  und ist ziemlich verbreitet. Darum haben wir uns das auch auf unsere Virtuellen Maschinen installiert. Weil das nicht ganz einfach ist, hat uns Herr Lohmeier das zuerst live gezeigt und ist mit uns [die Installationsanleitung](https://vufind.org/wiki/installation:ubuntu) durchgegangen.
Auf dies Punkte hat er uns hingewiesen, die findest du wie immer im SKRIPT!!!! zum Nachlesen. Danach waren wir dran und installierten das Programm bei uns, wie immer über Bash. Auch wenn wir vorgewarnt waren, dass eine Fehlermeldung kommt, erschrak ich trotzdem als sie erschien. Aber zum Glück gehört das zur Installation dazu. Was im Vergleich zu den letzten Sitzungen bei der Installation geholfen hat, ist meine neue stabile Internetverbindung. Eigentlich klar, aber darauf sollte man schon achten, wenn man so was öfters tun möchte. Vor allem wenn man gleichzeitig noch Unterricht streamt….
Weil wir MariaDB anstatt MySQL auf unserem Ubuntu-Server haben, mussten wir noch ein neues Passwort vergeben. (Das liegt daran, dass die Installation nicht auf MariaDB ausgelegt war.)
Die Installation brauchte trotz Anleitung einiges an Zeit. Immer wieder tauchte der eine oder andere Fehler...

![07-0-vufind](https://user-images.githubusercontent.com/61733461/83887297-8ccdc180-a748-11ea-8b3d-ec614708f02c.jpg)
![07-a-vufind einrichten](https://user-images.githubusercontent.com/61733461/83887310-90614880-a748-11ea-94d7-3631f74010ce.jpg)
![07-b-vufind installiert](https://user-images.githubusercontent.com/61733461/83887317-91927580-a748-11ea-8970-be63f7efaede.jpg)
![07-c-vufind](https://user-images.githubusercontent.com/61733461/83887327-9525fc80-a748-11ea-8935-df38a8901457.jpg)

...bis endlich alles im grünen Bereich war:
![08-alles grün](https://user-images.githubusercontent.com/61733461/83887383-a5d67280-a748-11ea-94d0-44efb52c3531.gif)

Danach arbeiteten wir in Gruppen an einem [Tutorial](https://felixlohmeier.gitbooks.io/vufind-tutorial-de/content/04_Installation_Testimport.html)
Leider gab es in unserer (auf 2 Personen geschrumpfte Gruppe) Probleme beim ersten Kapitel, dem Datenimport. Wir konnten zwar die Daten finden, speichern, bearbeiten und auch wieder hochladen. Aber im VuFind kamen die Daten nie an:(

![09-no result-crying](https://user-images.githubusercontent.com/61733461/83887520-d8806b00-a748-11ea-97b8-bc05558634fc.gif)

Wenn man das Tutorial durchstöbert, findet man auch viele ScreenShots und kann sich auch ohne Paralleldurchführung ein sehr gutes Bild von VuFind machen. Unsere Mini-Gruppe kam zum Schluss, dass VuFind ganz patent ist.

So ging schlussendlich ein intensiver Tag zu Ende. 
