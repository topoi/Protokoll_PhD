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
