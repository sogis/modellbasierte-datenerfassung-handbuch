Modelltypen
===========

INTERLIS-Modelle werden für verschiedene Zwecke eingesetzt. Entsprechend muss dies beim Modellieren berücksichtigt werden. Nicht in jedem Fall werden oder müssen sowohl ein Erfassungs- und eine Publikationsmodell geschrieben werden.

Erfassungsmodell
----------------
Erfassungsmodelle dienen der Erfassung und Nachführung von Daten in der Datenbank. Als Werkzeug zur Bewirtschaftung der Daten wird *QGIS* eingesetzt. Der Fokus bei der Modellierung liegt auf den Verzicht von Redundanzen, d.h. die Modelle sind normalisiert. So werden z.B. zwischen den einzelnen Klassen Beziehungen modelliert und Aufzähltypen modelliert um allfällige Redundanzen zu vermeiden. Im Zusammenspiel mit *QGIS* entsteht somit eine «generische» Erfassungsfachschale.

Publikationsmodell
------------------
Aufgrund der Normalisierung eignen sich Daten im Erfassungsmodell nicht für die Publikation in einem Web GIS oder als «einfacher» Layer in *QGIS*. Die für den Benutzer wichtigen Informationen sind in einem Erfassungsmodell oftmals auf verschiedene Klassen resp. Datenbanktabellen verteilt. Für die reine Darstellung und das einfache Abfragen von Informationen ist ein simpleres Modell – das Publikationsmodell – zu erarbeiten. Hauptmerkmal eines Publikationsmodelles ist der Verzicht auf Beziehungen zwischen den Klassen und dass der Inhalt zu jedem Zeitpunkt und automatisiert aus dem Erfassungsmodell und weiteren vorhandener Daten ableitbar ist.

Für eine allfällige Datenabgabe kann sowohl das Erfassungs- und Publikationsmodell zweckdienlich sein.

Validierungsmodell
------------------
Das Validierungsmodell dient zur Definition von zusätzlichen Prüfungen mit der Software *ilivalidator*. In diesem Modell müssen zuerst Views erstellt werden. In diesen Views können mit Constraints die zusätzlichen Prüfungen definiert werden. Ein Beispiel findet sich `hier <http://geo.so.ch/models/ARP/SO_Nutzungsplanung_20171118_Validierung_20171120.ili>`_.

Weitergehende Informationen zu den Modelltypen gibt es in der  `Präsentation <https://intraso.rootso.org/verwaltung/bau-und-justiz/amt-fuer-geoinformation/dokumente-und-grundlagen/veranstaltungen-workshops/>`_  des AGI vom 29. August 2017 zum Thema «Arbeiten mit einem Datenmodell».
