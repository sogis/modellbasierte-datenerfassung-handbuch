Modelldokumentation und -Ablage
===============================

Dokumentation
-------------

In der Regel genügt eine Dokumentation im Modell selbst (Bemerkungen zu Topics, Klassen und Attributen). Bei grösseren Modellen und/oder z.B. im Rahmen von Erfassungsrichtlinien ist eine Dokumentation des Modelles in einem zusätzlichen Dokument notwendig. 

Diese Bemerkungen zu Topics, Klasssen und Attributen werden beim Anlegen der Tabellen in der Datenbank übernommen und als Kommentar zu Tabellen und Attributen geführt. Zum jetzigen Zeitpunkt (Januar 2018) werden leider noch die Umlaute falsch gemappt.

Zusätzlich zu den INTERLIS-Objekten muss das Schema in der Datenbank kommentiert werden und falls immer möglich mit Auskunftspersonen (E-Mail-Adressen) hinterlegt werden, z.B.:: 

    Dieses Schema wird für die Erfassung der Hoheitsgrenzen verwendet. Fragen: noemi.sturm@bd.so.ch, stefan.ziegler@bd.so.ch.


Ablage
------

Die definitiven und abgenommenen Datenmodelle (``*.ili``) werden in der `INTERLIS-Modellablage <http://geo.so.ch/models/>`_ des Kantons Solothurn publiziert. Ist das Datenmodell publiziert, darf es ohne Änderung des Modellnamens inhaltlich nicht verändert werden (redaktionelle Änderungen sind denkbar). Die Modelle werden in der privaten Zone auf das Filesystem kopiert und jede Nacht in die globale Zone ("Internet") gespiegelt. Das Betriebshandbuch zur INTERLIS-Modellablage findet sich hier: ``H:\BJSVW\Agi\GDI\Betrieb\Interlis_Modellablage\Betriebs-_und_Nachfuehrungshandbuch_Interlis-Modellablage``.

Durch die Publikation in einer Modellablage und der Verknüpfung der verschiedenen Modellablagen untereinander, finden die eingesetzten Werkzeuge (meistens) ohne weiteres Zutun sämtliche INTERLIS-Modelle, die im eigenen Modell importiert werden. 

Die UML-Datei wird ebenfalls in der Modellablage abgelegt. Die UML-Datei ist der Master. Es dürfen keine Änderungen nur in der INTERLIS-Modelldatei vorgenommen werden. 


Weitere Unterlagen
------------------

Weitere Unterlagen im Rahmen der Modellierung sind im Projekte-Ordner abzulegen.
