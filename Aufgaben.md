- SQL DB: unnötige Spalten entfernen
- PHP Export: Namen der Spalten umbenennen in lesbare Begriffe
- zusätzliche Kategorien für linke Spalte (nur Bilder, nur Memphis etc.) 
- generelles Design anpassen, Logo, Metadaten etc.
- Testversion mit Zenodo verknüpfen, DOI erstellen
- Workflow testen:   
-- aktuelle Version aus SQL exportieren (PHP)  
-- JSON auf Github  
-- Versionierung  
-- kompletten Code auf Annes Github Account
- Bilder auf Github und in Visualisierungsmaske einbinden

- Dating Tabelle und klickbare Bilder für Galerie(?)
Id 1275 da fehlt das Bild, hier der Bildlink: https://images.metmuseum.org/CRDImages/eg/original/LC-67_3_EGDP028267.jpg und der link zum museum: https://www.metmuseum.org/art/collection/search/549236 
- die related objects, bzw. related persons and titles sowie die ### with same name, type usw. in numerischer Reihenfolge, beginnend mit dem Kleinsten ?
ein Vor- und Zurücktaste in der einzelansicht der daten, um einzeln durch die einzelnen datenblätter durchgehen zukönnen
eine ergebnistrefferanzeige (wenn man in der suchmaske zum beispiel nach personen mit einem bestimmten namen suchen will, dass man eine anzeige darüber hat, wieviele daten der gefilterten suche entsprechen
START: 201.09.2019
--> Zu den Einzelansichten: Unter Persons 
1. related object(s) v.l.n.r. Id - Type - Subtype - Provenance - Location - Inventory No
2. related person(s) v.l.n.r. Id - Name - English/name (english) - Gender
3. related title(s) v.l.n.r. Id - title - title (english) - Gender
4. persons with same name v.l.n.r. Id - Name - name (english) - Gender

--> Unter objects
1. related person(s) v.l.n.r. Id - Name - name (english) - Gender
2. objects of the same type v.l.n.r. Id - Type - Subtype - Provenance - Location - Inventory No

--> Unter Titles
1. related person(s) v.l.n.r. Id - Name - name (english) - Gender
2. titles of same name v.l.n.r. Id - title - title (english) - Gender

--> die keys in den Einzelansichten sind derzeit noch z.T. falsch benannt. da steht ja noch name (translit) ich meine das haben wir zu English umbenannt. das müsste dann entsprechend unserer Benennungen angepasst werden. dazu ist mir auch noch was aufgefallen unter titles gibt es den key Translation, der müsste allerdings umbenannt werden, denn es handelt sich ja nicht um eine Übersetzung des titles sondern eine Umschrift in englischer sprache. also wenn es möglich ist den key auch English zu nennen, dann wäre das super. falls das nicht geht weil keys ja nicht gleich heißen dürfen dann würde ich folgenden Schema nehmen

für persons 
english = name (english)

für titles 
translation = title (english) 
ENDE: 21.09.2019

4.11.2019

Abfrage1:  wieviele Personen auf den Objekten für Teti, Unas, Falaise   
Abfrage2:  für alle Grabbesitzer auf allen Friedhöfen (83 Personen), Tomb Owner in tombowner.csv    
10001,Tomb Owner
10035,Tomb Owner
10039,Tomb Owner
10040,Tomb Owner
10042,Tomb Owner
10048,Tomb Owner
10074,Tomb Owner
10076,Tomb Owner
10123,Tomb Owner
10135,Tomb Owner
10150,Tomb Owner
10161,Tomb Owner
10179,Tomb Owner
10187,Tomb Owner
10193,Tomb Owner
10194,Tomb Owner
10212,Tomb Owner
10241,Tomb Owner
10257,Tomb Owner
10267,Tomb Owner
10295,Tomb Owner
10306,Tomb Owner
10307,Tomb Owner
10327,Tomb Owner
10368,Tomb Owner
10385,Tomb Owner
10404,Tomb Owner
10405,Tomb Owner
10415,Tomb Owner
10423,Tomb Owner
10432,Tomb Owner
10434,Tomb Owner
10445,Tomb Owner
10464,Tomb Owner
10466,Tomb Owner
10487,Tomb Owner
10498,Tomb Owner
10510,Tomb Owner
10514,Tomb Owner
10519,Tomb Owner
10530,Tomb Owner
10537,Tomb Owner
10539,Tomb Owner
10547,Tomb Owner
10551,Tomb Owner
10571,Tomb Owner
10587,Tomb Owner
10631,Tomb Owner
10650,Tomb Owner
10662,Tomb Owner
10667,Tomb Owner
10675,Tomb Owner
10676,Tomb Owner
10685,Tomb Owner
10715,Tomb Owner
10752,Tomb Owner
10784,Tomb Owner
10797,Tomb Owner
10800,Tomb Owner
10801,Tomb Owner
10808,Tomb Owner
10815,Tomb Owner
10829,Tomb Owner
10886,Tomb Owner
10895,Tomb Owner
10905,Tomb Owner
10909,Tomb Owner
10933,Tomb Owner
10944,Tomb Owner
10946,Tomb Owner
10952,Tomb Owner
11027,Tomb Owner
11119,Tomb Owner
11187,Tomb Owner
11207,Tomb Owner
11570,Tomb Owner
11584,Tomb Owner
11602,Tomb Owner
11770,Tomb Owner
11876,Tomb Owner
12652,Tomb Owner
12719,Tomb Owner

Update der sql database zur Abgabe der Diss einpflegen 

Tausche Namen 'Memphis Navigator' --> 'Prosopographia Memphitica' und 'A tool designed for database navigation' --> A Prosopographical Database 

Lösche 'Main Menu' Button von Startbildschirm, verwirrt den Besucher, da man davon ausgeht hier zu einem Hauptmenü zu gelangen, 

Tausche 'Project & Help' --> 'Menu'

Tausche 'Instruction' in Seitenreiter --> 'How to use'

Tausche 'Description' im Seitenreiter (Unterpunkt zu 'Networks') --> 'About Network Studies'

Tausche Button 'Main Menu' (drei Striche) innerhalb der Filterlogik zu Homebutton (Haussymbol wie im Browser) --> benennung des hausbuttons dann nicht nötig, weil Haussymbol selbsterklärend ist

Tausche Buttonbeschriftung 'Back to current menu' zu 'Back to search'

Aktuellen Datenstand auf Zenodo hochladen --> Achtung neue DOI

Metadata (siehe upload file in Github) zu 'Project' im Menu

Metadata (citation & access date) zu Einzelansichten hinzufügen

START 21.02.2020 
Ersetze document link in der einzelansicht nach dem folgenden Schema (am bsp. Aaemhotep)

Permalink: https://anneherz.github.io/ProM/detail/singleview_persons.html?ids=2411&name=o#-m-Htp
Citation: 
Anne Herzberg-Beiersdorf, Prosopographia Memphitica,  https://anneherz.github.io/ProM/detail/singleview_persons.html?ids=2411&name=o#-m-Htp
Access Date: 28.02.2020

Ersetze Homebutton durch Home icon im github ordner iconic home (dazu gibt es ein file Unicodes)  
Ersetze vor und zurück pfeile durch pfeil icons im github ordner iconic home  
füge creative commons icons am ende der seite 'project' ein  
Schreibe Prosopographia Memphitica auf startbildschirm nebeneinander nicht untereinander  
Ändere farben der Buttons der dropdowns und show results buttons in rgb 54,100,139 bzw.#36648b bzw. C=61 M=28 Y=0 K=45  
Ändere Farben der Einzelseiten aus dem 'Menu' (Project, How to usw, Networks, Contacts) in rgb 245,245,245 bzw. #f5f5f5 bzw. C=0 M=0 Y=0 K=4  
Als Schriftfont für die Texte hätte ich gerne https://fonts.google.com/specimen/Source+Sans+Pro in light. Schriftgröße: 12 pt bzw. 16 px, Schriftfarbe: rgb 48,48,48 bzw.#303030  
Die Texte (bspw. unter 'About Network Studies') immer im Blocksatz und mit 1,5 pt Zeilenabstand  
Wenn das nicht zuviel Arbeit macht, dann können wir die Schrift gerne für alle Schriften nehmen. Ich würde für den normalen text immer sans source pro light nehmen und für die Überschriften für ich dann sans source pro regular nehmen.
ENDE 21.02.2020

**21.2:**
Wir müssen noch mal die Hierarchie diskutieren. Die Volltextsuche basiert immer auf dem vollen Datensatz und steht über der Dropdown Suche. Würde ich vorschlagen.  

Bei Einzelansicht:    
Citation: Anne Herzberg-Beiersdorf, Prosopographia Memphitica, https://anneherz.github.io/ProM/detail/singleview_persons.html?ids=133&name=o#-mw Access Date: 28.02.2020

muss Komma vor Access Date

Memphis Navigator im Reiter ersetzen  

START 21.02.2020
muss Komma vor Access Date: JA!

Ersetze Text im 'Menu' unter 'About Network Studies' (Formatierungsangaben im Text enthalten) --> pdf in Github hochgeladen

Ersetze Text im 'Menu' unter 'Project' (Formatierungsangaben im Text enthalten) --> pdf in Github hochgeladen

Ändere Hintergrundfarbe der Einzelansicht auf in rgb 245,245,245 bzw. #f5f5f5 bzw. C=0 M=0 Y=0 K=4 und Schriftfarbe in Schriftgröße: 12 pt bzw. 16 px, Schriftfarbe: rgb 48,48,48 bzw.#303030  

Farbe des Menukastens in der Einzelansicht auf Semi-Transparent stellen, wie im Hauptmenu 

Erstelle neuen Reiter im 'Menu' mit dem Namen 'Terms & Conditions of Use' 

Füge Text im 'Menu' unter 'Terms & Conditions of Use' ein (Formatierungsangaben im Text enthalten) --> pdf in github hochgeladen

Texte unter 'Project', 'About Network Studies' und 'Terms und Conditions of Use' nach Möglichkeit über die volle Breite des Bildschirms laufen lassen, sondern einen Abstand/Seitenränder einbauen 
