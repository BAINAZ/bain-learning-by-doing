---
title: "Spaces: Archivespace & DSpace"
date: 2020-04-14
---
Heute starteten wir nach einem kurzen Rückblick auf die letzte Veranstaltung zu Koha mit einer Auffrischung der Metadatenstandards [ISAD(G)](https://de.wikipedia.org/wiki/ISAD(G)) und [EAD](https://de.wikipedia.org/wiki/Encoded_Archival_Description).
In Kleingruppen untersuchten wir zwei bestehende Archivfindmittel, um in die Archivdenkweise einzutauchen. Danach ging es mit ArchivesSpace los.

## ArchivesSpace

ArchivesSpace ist ein OpenSource Programm, das aus zwei Vorläuferprogrammen fusiniert wurde. Es gibt einen [Verein](https://archivesspace.org/member-area/thank-you-for-becoming-a-member), mit dessen Mitgliederbeiträgen 5 Vollzeitstellen geschaffen wurden, welche ArchivesSpace warten und weiterentwickeln. Dadurch ist es ziemlich hochwertig und wird weltweit genutzt:

![as_weltkarte](https://user-images.githubusercontent.com/61733461/80275798-ebccff00-86e3-11ea-912f-f701f90a2165.jpg)

Wir installierten das Programm wieder auf unsere Virtuellen Computer. Das braucht nur wenige Zeilen Code, hat bei mir aber nicht auf Anhib geklappt. Herr Lohmeier hat mir aber geholfen, das Störprogramm im Hintergrund zu "killen", danach hat es zum Glück funktioniert.
In einem ersten Schritt haben wir dann ein Testrepositorium erstellt:

![as_repository](https://user-images.githubusercontent.com/61733461/81039698-0a808200-8eaa-11ea-8a2a-b0916395b7ea.jpg)

Danach haben wir darin einen Eintrag in der Gruppe gemacht. Nachträglich habe ich noch einen Collection-Beitrag erstellt. Das Formular dafür ist sehr einfach, hier ein Ausschnitt davon:

![as_formular](https://user-images.githubusercontent.com/61733461/81039787-33a11280-8eaa-11ea-8031-0206f6e4b81e.jpg)

Sobald das gespeichert ist, kann man auf dem 81er Port das Repositorium aufrufen....

![as_suche](https://user-images.githubusercontent.com/61733461/81039978-a5795c00-8eaa-11ea-8ef2-d05eb5c4f767.jpg)

.... und nach den Einträgen suchen...

![as_resultat](https://user-images.githubusercontent.com/61733461/81041092-37826400-8ead-11ea-86eb-42c33e7b5095.jpg)

... und den Treffer auch anschauen:

![as_treffer](https://user-images.githubusercontent.com/61733461/81041116-4701ad00-8ead-11ea-8af1-aa0e79cd7309.jpg)

Nach der Mittagspause schauten wir uns den Import und Export in ArchivesSapce an. Leider hatte ich den ganzen Tag Probleme mit dem Internet. Es war, als ob mein PC in den 90er Jahren wäre: Kaum Internet, jeder Klick beansprucht den Computer total. Zum Glück funktionierten die Übertragungen des Unterrichts und der Gruppe. Dank *Alfredo* und *mimbulus* konnte ich trotzdem an den Übungen teilhaben. So merkten wir, dass beim MARCXML-Datenexport nicht alle Daten exportiert wurden:
“Level of Description”, “Language of Description” und “Script of Description” fehlten.

Der Import funktionierte ganz gut, nachdem wir erst einmal gecheckt hatten, dass wir die Raw-XML Datei aus den EAD-Beispieldaten kopieren, in einem Texteditor einfügen, speichern und erst jetzt hochladen mussten. Das dauert einfach eine gefühlte Ewigkeit (auch bei den Kolleginnen und Kollegen mit voll laufendem Internet).

Nach einer kurzen Streifung des Marktüberlicks ([Access to Memory (Atom)](https://www.accesstomemory.org), [scope.Archiv](http://www.scope.ch) & [CMISTAR](https://www.cmiag.ch/cmistar)) ging es kurz um die Unterschiede zwischen Bibliotheks- und Archivsystemen. Da ist das Hauptproblem: Unterschiedliche Ziele der Software führt zu unterschiedlichen Inhalten und Ausprägungen, was wiederum zu Problemen beim Austausch führt).

## DSpace
Dspace ist eine Repository-Software. Bevor wir die installierten, gab es einen kleine Exkurs zu Open Access und Open Data. Durch die Betrachtung von verschiedenen Statistiken und Webseiten zeigt uns Herr Lohmeier, das Dspace sehr weit verbreitet ist.
Dspace konnten wir über eine Demo-Version online nutzen, ohne dass man das Programm gleich installieren mussten. Das ist ziemlich cool und halt mega einfach zum Bedienen. Im nu hat man dann eine Community und innerhalb der Community eine Collection angelegt. Dank Bild-Einfüg-Option war das auch richtig spassig!
Das sieht dann zum Beispiel so aus:

![ds_collection und community](https://user-images.githubusercontent.com/61733461/81041734-d2c80900-8eae-11ea-995a-c84749711c11.jpg)

In dieser Collection konnten wir dann einen eigenen Beitrag in unsere Sammlung hochladen:

![ds_Eintrag_vollanasicht](https://user-images.githubusercontent.com/61733461/81041789-ff7c2080-8eae-11ea-8706-6725ce2db2da.jpg)

Zum Tagesabschluss zeigte uns Herr Lohmeier noch kurz einige weiterführende Infos zu DSpace und danach einen kleinen Marktüberblick zu verschiedenen Repositorien. Das alles und viel mehr kannst du in seinem [Skript](https://bain.felixlohmeier.de/#/04_repository-software-fuer-publikationen-und-forschungsdaten) nachlesen.
Das wars von mir - Bis zum nächsten Eintrag!
