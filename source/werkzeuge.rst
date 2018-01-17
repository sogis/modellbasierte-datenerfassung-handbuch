Werkzeuge
=========

Für die verschiedenen Modellierungsprozesse stehen passende Werkzeuge zur Verfügung.

UML/INTERLIS-Editor
-------------------

Der `UML/INTERLIS-Editor <http://umleditor.org/>`_ dient der Modellierung von INTERLIS-Modellen mittels UML-Diagrammen. Er benötigt Java und kann lokal installiert und verwendet werden. Die Lernkurve ist relativ steil und die Bedienung gewöhnungsbedürftig. Mit dem Verständnis von INTERLIS als Modellierungssprache wächst auch die Verständnis für die Bedienung des *UML/INTERLIS-Editors*.

ili2c
-----

Mittels `INTERLIS-Compiler <https://sourceforge.net/projects/umleditor/files/ili2c/>`_ kann das INTERLIS-Modell syntaktisch geprüft werden. Die Software ist bereits im *UML/INTERLIS-Editor* eingebaut und muss nicht zwingend separat installiert werden.

ili2pg
------

`Ili2pg <http://www.eisenhutinformatik.ch/interlis/ili2pg/>`_ erstellt aufgrund eines INTERLIS-Modelles ein Schema mit leeren Tabellen in einer PostgreSQL/PostGIS-Datenbank. Es kann auch INTERLIS-Transferdateien importieren oder aus einer Datenbank Daten in eine Transferdatei exportieren.

Es wird Version XXXXXX (TODO) verwendet.

Mit `ili2gpkg` und `ili2fgdb` stehen Derivate für GeoPackage und FileGeodatabase zur Verfügung.

ilivalidator
------------

Dank des `ilivalidators <https://github.com/claeis/ilivalidator>`_ kann eine INTERLIS-Transferdatei auf ihre Modellkonformität geprüft werden. Die Software ist ebenfalls in *ili2pg* eingebaut und ist standardmässig aktiviert und muss mit ``--disableValidation`` ausgeschaltet werden.

QGIS-Projektgenerator
---------------------

Das QGIS-Plugin «QGIS-Projektgenerator» (QGIS 3 only) erstellt anhand eines INTERLIS-Modelles resp. der in der Datenbank angelegten Tabellen automatisch ein QGIS-Projekt mit bereits vorkonfigurierten und verknüpften Formularen. Für grössere Modelle wird man in Zukunft sicher darauf aufbauen können. Oliver Jeker war Mitglied der Arbeitsgruppe und Sandra Curiger hat bereits erste Tests durchgeführt.
