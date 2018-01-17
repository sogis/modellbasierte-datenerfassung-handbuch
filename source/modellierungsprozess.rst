Modellierungsprozess
====================

Auf eine strenge Formalisierung des eigentlichen Modellierungsprozesses («Startsitzung», «FIG»  etc.) wird verzichtet. Die Datenmodelle werden durch das AGI gemeinsam mit den Dienststellen erarbeitet. Für den Modellierungsprozess existiert eine Checkliste (``H:\BJSVW\Agi\KGDM\Vorlagen\Checkliste_DM_V6.docx``). Diese ist zu verwenden.

(1) Datenerfassungswunsch in der Dienststelle
---------------------------------------------

*Verantwortung: Dienststelle*

Auslöser kann eine neue Aufgabe sein oder es können ebenfalls alte, bestehende Daten in die modellbasierte Struktur gebracht werden.

(2) Erarbeitung der Modelle
---------------------------

*Verantwortung: AGI und Dienststelle*

Zusammen mit der Dienststelle erarbeitet das AGI die benötigten Datenmodelle (in der Regel ein Erfassungs- und ein Publikationsmodell).

Hilfreich für die Dienststelle kann eine Exceldatei (``H:\BJSVW\Agi\KGDM\Vorlagen\Datenmodell_Grundlage_Vorlage.xlsx``) sein, in die sie in tabellarischer Form ihr «Modell» eintragen (Attributename, -typen etc.) kann. Eventuell lohnt es sich bereits mit Shapefiles ein paar Testdaten zu erfassen.

(3) Review der Modelle
----------------------

*Verantwortung: Dienststelle*

Die Dienststellen müssen zwingend das Modell verstehen und reviewen.

(4) Testen
----------

*Verantwortung: AGI und Dienststelle*

Die Dienststelle muss das Modell in einer Testumgebung zusammen mit einem konfiguriertem QGIS-Projekt testen können. Dieser Schritt ist ungemein wichtig, da jede Anpassung am Modell Aufwand verursacht.

Der GDI ist mittels Ticket (im dazugehörigen Projekt/Auftrag) sämtliche benötigten Informationen zu kommen zu lassen, dh. ili2pg-Befehl und allfällige weitere DDL-Befehle (Permissions etc.). In Zukunft wird nicht mehr der ili2pg-Befehl für das Anlegen der Tabellen ausgeführt, sondern es wird zuerst mit *ili2pg* eine SQL-Datei mit den ``CREATE TABLE`` etc. Befehlen erstellt und anschliessend wird diese ausgeführt. *Ili2pg* muss diesbezüglich aber noch erweitert werden.

Folgende ili2pg-Optionen werden standardmässig verwendet:

* ``--defaultSrsCode 2056``
* ``--strokeArcs``
* ``--createGeomIdx``
* ``--createFkIdx``
* ``--createEnumTabs``
* ``--beautifyEnumDispName``
* ``--createMetaInfo``
* ``--createUnique``
* ``--createFk``
* ``--createNumChecks``

Anmerkung: Für einen kompletten ili2pg-Befehl fehlen in der Auflistung zwingende Optionen (z.B. DB-Host etc.).

Die ``t_ili2db``-Tabelle sind sowohl für Erfassungs- und Publikationsmodelle in der Datenbank (Test und Produktion) **nicht** zu löschen.

(5) Integration in Produktionsumgebung
--------------------------------------

*Verantwortung: AGI*

Das AGI integriert das abgenommen Modell in der Produktionsumgebung. Die QGIS-Projektdatei muss mit den entsprechenden Datenbankparametern angepasst werden. Die Integration erfolgt analog der Integration in die Testumgebung.

Um eine möglichst hohe Datenqualität zu halten, werden die Daten täglich mit einem ili2pg-Befehl exportiert. Dafür wird ein Skript (in Zukunft GRETL-Job) verwendet. Nach der Integration ist das neue Modell in das Skript zu integrieren (zur Zeit durch Noëmi Sturm).

(6) Modelländerungen
--------------------

*Verantwortung: AGI und Dienststelle*

Anforderungen an ein Modell können im Laufe der Zeit ändern. Sogenannte Modelländerungen sind zwar nicht gewünscht aber sie kommen vor. Welche der einzelnen Modellierungsschritte  nochmals durchgeführt werden müssen, hängt von der Änderung selbst ab. Da noch praktisch keine Erfahrungen vorliegen, geht man davon aus, dass das bestehende Schema umbenannt wird und mit dem geänderten Modell ein neues Schema mit dem gleichen Namen erstellt wird. Die alten Daten können mittels GRETL-Job in die neuen Tabellen kopiert umgebaut werden. Ist die Modelländerung abgenommen, kann das alte (umbenannte) Schema gelöscht werden.

Der Modelländerungsprozess hängt sicher auch davon ab, wie wir in Zukunft grundsätzlich Änderungen im AGDI leben wollen und (technisch) können. Time will tell.
