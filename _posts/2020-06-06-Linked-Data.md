---
title: "Linked Data"
date: 2020-06-06
---
Frisch erholt starteten wir am Samstagmorgen früh mit einem Nachtrag zu VuFind und den Kommandos, die unsere Probleme gestern lösen. Danach schlug uns Herr Lohmeier verschiedene Möglichkeiten vor, wie wir auch nach dem Kurs noch Software testen können, respektive in welcher Umgebung, weil Ende Semester ja unsere Virtuellen Maschinen weg sind. 
Damit wir dafür gewappnet sind, zeigte uns Herr Lohmeier live, wie man beim Root-Server [Digitalocean](https://digitalocean.com) zuerst den Server zusammenstellt (man könnte auch einen Standard-fixfertig-Server haben) und dort dann OpenRefine installiert. 

## Linked Data
Als Beispiel für das breite Feld von Linked Data schauten wir Wikidata an. 
Wikidata basiert auf der Software Wikibase. Diese wird von verschiedenen Institutionen genutzt, aktuell prüft gerade die DNB, ob Wikibase auch für die GND genutzt werden kann. 
In einer Gruppenarbeit nuttzen wir OpenRefine und WikiData, um Metadaten anzureichern.  Im vorhin live erstellten Server und frisch installierten OpenRefine haben wir dann zuerst ein neues Projekt angelegt und über eine URL erste Daten eingefügt:

![03-projekt-anlegen](https://user-images.githubusercontent.com/61733461/83939293-28f4d880-a7dc-11ea-81b9-852569d124e5.jpg)

Danach haben wir die Autoren mit Daten angereichert. Da habe ich wohl einen Schritt übersprungen und beim nicht eindeutigen Namen niemanden (respektive alle) ausgewählt:

![04-reconiliation](https://user-images.githubusercontent.com/61733461/83939296-2d20f600-a7dc-11ea-9abe-774798b74cb3.jpg)

![05-ergebnis-reconcialiation](https://user-images.githubusercontent.com/61733461/83939297-2db98c80-a7dc-11ea-9f63-31e40c44c6e9.jpg)

Im nächsten Schritt haben wir die Bilder mit Daten aus Wikidata angereichert:

![06-Daten aus Wikidata angereichert](https://user-images.githubusercontent.com/61733461/83939298-2db98c80-a7dc-11ea-874a-9c9201e0cc06.jpg)

Das ist echt cool, so hat man sogar Bilder, wenn man mit der Maus über die Autoren fährt:

![07-Ergebnis](https://user-images.githubusercontent.com/61733461/83939295-2c885f80-a7dc-11ea-9a98-afb2eb01378e.jpg)

Nach der Übung zeigte uns Herr Lohmeier noch einige Anwendungsbeispiele und Orte, wo man weitere Literatur zur Reconciliation erhält. 

## SPARQL-Abfragen mit dem Wikidata Query Service
Obwohl wir schon ganze zwei Semester mit SPARQL gearbeitet haben, kam in der allerletzten Unterrichtseinheit des gesamten Studiums nocheinmal ein Hinweis, der Gold wert ist: 
**Wenn man mit STR+Leer sucht, dann kriegt man Vorschläge, auch Propertyvorschläge!** Hätte ich das nur schon viel früher erfahren. Ein weiteres Erleuchtungsinput war: Wikidata Query Service bietet einen Abfragehelfer an, mit ganz vielen Beispielsuchen! Das ist ja super-mega-praktisch! Die vergangenen Jahre haben wir jeweils Stunden damit verbraten, die Strukturierten Daten zu durchforschen, nur schon um heruaszufinden welche Properties verwendet werden und wonach wir suchen können... 

Bevor wir zu den Übungen kamen, zeigte uns Herr Lohmeier zur Auflockerungen diesen lustigen [Blogbeitrag](https://blog.wikimedia.de/2016/10/30/10-coole-wikidata-abfragen-die-dir-neue-horizonte-eroeffnen-nummer-7-wird-dich-schockieren/) mit den lustigsten SPARQL-Abfragen. Nummer 7 wird dich schokieren! ;)

Beim Ausprobieren suchte ich nach Nachnamen von Wissenschaftlerinnen. Ausgangslage war dafür eine Beispielabfrage. Dort habe ich zuerst einmal viele Labels entfernt (Geburt, Tod, Geschichte). Um eine überschaubare Liste an Treffern zu erhalten setzte ich ein LIMIT 10. Trotzdem kam die Abfrage nicht zum Abschluss:

![07-abfrage](https://user-images.githubusercontent.com/61733461/83940648-0e276180-a7e6-11ea-9fee-e68ed79ecc12.jpg)

Gut möglich, dass da noch ein Fehler drin ist. Meiner Erfahrung nach braucht es immer ein bis zwei Studnen, bis man richtig im SPARQL und der Datenbank drin ist und selber erfolgreiche Abfragen zu machen. Darum führte ich nochmals die Original-Beispielabfrage durch, die aber ebenfalls zur Zeitüberschreitung führte (mit und ohne LIMIT).

Da es die letzte Stunde ist, sollte doch noch ein bisschen Spass und Erfolg mit dabei sein. Darum machten wir in der Gruppe gemeinsam die Beispiel-Katzen-Abfrage. Die hat auch wunderbar funktioniert:


![01-katzenabfrage](https://user-images.githubusercontent.com/61733461/83940763-c48b4680-a7e6-11ea-9daa-de69e550c16d.jpg)

Von den zahlreichen Ergebnissen, hier einen lustigen Teaser:

![02-Katze ](https://user-images.githubusercontent.com/61733461/83940788-ea185000-a7e6-11ea-95b5-fa04445595e1.jpg)

Zum Schluss stellte uns Herr Lohmeier noch einige weitere Tutorials vor. Diese findet ihr wie immer in seinem [Skript](https://bain.felixlohmeier.de/#/07_linked-data).
