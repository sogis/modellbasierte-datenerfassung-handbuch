Modellierungsregeln
===================

Modellierungssprache / Compiler
-------------------------------

*#101*: Modellierungssprache ist INTERLIS 2.3 gemäss Referenzhandbuch vom 13. April 2006.

*#102*: Für die Kontrolle der Datenmodelle wird der INTERLIS-Compiler Version 4.5.22 vom 7. April 2016 (oder höher) eingesetzt.

*#103*: Die verwendete Compiler-Version ist im Modell-Header anzugeben.

*#104*: Der Namensraum für Modelle ist http://geo.so.ch/models/AMT wobei das entsprechende Amt angegeben wird.


Modellname / Version / Formatierung
-----------------------------------

*#201*: Die Benennung von Modell- und UML- Dateien erfolgt nach folgendem Schema:

  kk_ds_n*_v*.ili/.uml

  kk: Kantonskürzel (``SO``)

  ds: Amt / Dienststelle (``AV``)

  n*: Sprechender Name des Modells (``Nachfuehrungskreise``)

  v*: Version des Modells im Format JJJJMMTT (``20160407``)

  Für den Dateinamen des Validierungsmodells wird dem Dateinamen des zu validierenden Modelles «_Validierung_JJJJMMMTT» angehängt.


*#202*: Die Benennung von Modellen erfolgt nach folgendem Schema:

  kk_n*_v*

  kk: Kantonskürzel (``SO``)

  ds: Amt / Dienststelle (``AV``)

  n*: Sprechender Name des Modells (``Nachfuehrungskreise``)

  v*: Version des Modells im Format JJJJMMTT (``20160407``)

  Der Modellnamen des Validierungsmodelles wird analog der Regel für Dateinamen gewählt.


*#203*: Die ID der Geobasisdatensätze muss im Header der Modelldatei eingetragen werden. Kantonale minimale Geodatenmodell gemäss KgeoIV erhalten die offizielle ID gemäss Anhang. Die übrigen Modelle erhalten keine ID. ``!!@ kGeoiV_ID = „SO-1004“;``

*#204*: Die Metaattribute ``File``, ``Title``, ``shortDescription``, ``Issuer`` und ``technicalContact`` sind im Header der Modelldatei zu erfassen.

*#205*: Die Änderungshistorie wird im Header der Modelldatei dokumentiert.

*#206*: Für die Formatierung der Modelldateien dürfen keine Tabulatoren verwendet werden.

*#207*: In Kommentaren müssen Umlaute verwendet werden. Dies führt noch zu Problemen beim Import in die Datenbank. Dieses Verhalten wird aber 2018 korrigiert.

*#208*: Im Header der Modelldatei muss der Modelltyp angegeben werden («Erfassungsmodell», «Publikationsmodell», «Validierungsmodell»). Wird neben dem Erfassungsmodell ein zusätzliches Publikationsmodell erstellt, erhält dieses im Dateinamen und im Modellnamen vor dem Datum den Zusatz „Publikation“.

*#209*: Die Version (= Datum) des Modelles ist anzugeben. ``VERSION "2017-01-19"``

*#210*: Jedes Attribut muss mit einem Kommentar versehen werden, welcher das Attribut sinnvoll beschreibt.

Namenskonvention
----------------

*#301*: Alle Modellelemente (Modellnamen, Topics, Klassen, Attribute etc.) werden ausschliesslich auf Deutsch bezeichnet.

*#302*: Namen von Topics, Klassen und Assoziationen sollte nicht länger als 29 Zeichen sein.

*#303*: Attributnamen einer Klasse sollten nicht länger als 29 Zeichen sein.

*#304*: Topic-Namen: Gross- und Kleinschrift mit Underscore als Trennzeichen. Plural.

*#305*: Klassen-Namen: Gross- und Kleinschrift mit Underscore als Trennzeichen. Singular.

*#306*: Attribut-Namen: Gross- und Kleinschrift mit Underscore als Trennzeichen. Singular.

*#307*: Die Verwendung von reservierten Namen ist nicht erlaubt.

Modellstruktur
--------------

*#401*: Es müssen die Geometrietypen aus dem CHBase-Modell ``GeometryCHLV95_V1`` verwendet werden.

*#402*: Für Kantonskürzel muss ``CHCantonCode`` aus dem CHBase-Modell ``CHAdminCodes_V1`` verwendet werden

*#403*: BFS-Nummern sind als Wertebereich 0 .. 9999 zu definieren.

Einschränkungen zum Gebrauch von INTERLIS 2.3
---------------------------------------------

*#501*: Es dürfen nur zweiwertige (binäre) Beziehungen (ASSOCIATION) deklariert werden.

*#502*: Views dürfen nicht nur in Validierungsmodellen verwendet werden.

*#503*: Für ``TEXT`` muss immer eine konkrete Länge angegeben werden.

*#504*: Externe Objektkataloge und Codelisten dürfen nicht verwendet werden.

Konsistenzbedingungen
---------------------

*#601*: Die Kardinalitäten von Rollen muss erfasst werden.

*#602*: UNIQUE-Bedingungen müssen erfasst werden.

Darstellungsmodell
------------------

*#701*: Textpositionen werden nur definiert, wenn diese schwer aus den Daten berechnet werden können oder spezielle Anforderungen an die Darstellung bestehen.

Entwurfsmuster
--------------

*#801*: Als OID wird ``INTERLIS.UUIDOID`` verwendet.

*#802*: Allgemeiner Grundsatz: Es wird nur die IST- Situation beschrieben.

*#803*: Für Labelorientierungen etc. wird die Einheit ``Units.Angle_Degree`` verwendet.
