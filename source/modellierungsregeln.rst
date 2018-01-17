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

  kk_ds_n*_[Publikation|Validierung]_v*.ili/.uml

  kk: Kantonskürzel (``SO``)

  ds: Kürzel Amt / Dienststelle (``AV``)

  n*: Sprechender Name des Modells (``Nachfuehrungskreise``)

  v*: Version des Modells im Format JJJJMMTT (``20160407``)

  Für den Dateinamen des Validierungsmodells wird dem Dateinamen des zu validierenden Modelles «Validierung» hinzugefügt und für den Dateinamen des Publikationsmodells «Publikation».


*#202*: Die Benennung von Modellen erfolgt nach folgendem Schema:

  kk_ds_n*_v*

  kk: Kantonskürzel (``SO``)

  ds: Kürzel Amt / Dienststelle (``AV``)

  n*: Sprechender Name des Modells (``Nachfuehrungskreise``)

  v*: Version des Modells im Format JJJJMMTT (``20160407``)

  Der Modellnamen des Validierungsmodelles und des Publikationsmodells wird analog der Regel für Dateinamen gewählt.


*#203*: Die ID der Geobasisdatensätze muss im Header der Modelldatei eingetragen werden. Kantonale minimale Geodatenmodell gemäss KgeoIV erhalten die offizielle ID gemäss Anhang. Die übrigen Modelle erhalten keine ID. ``!!@ kGeoiV_ID = „SO-1004“;``

*#204*: Die Metaattribute ``File``, ``Title``, ``shortDescription``, ``Issuer`` und ``technicalContact`` sind im Header der Modelldatei zu erfassen.

*#205*: Die Änderungshistorie wird im Header der Modelldatei dokumentiert.

*#206*: Für die Formatierung der Modelldateien dürfen keine Tabulatoren verwendet werden.

*#207*: In Kommentaren sollen Umlaute verwendet werden. Dies führt momentan aber noch zu Problemen beim Import in die Datenbank (temporäre Lösung: keine Umlaute verwenden). Dieses Verhalten soll aber 2018 korrigiert werden.

*#208*: Im Header der Modelldatei muss der Modelltyp angegeben werden («Erfassungsmodell», «Publikationsmodell», «Validierungsmodell»). 

*#209*: Die Version (= Datum) des Modelles ist (via UML-Editor) anzugeben. ``VERSION "2017-01-19"``

*#210*: Jedes Attribut muss mit einem Kommentar versehen werden, welcher das Attribut sinnvoll beschreibt.

Namenskonvention
----------------

*#301*: Alle Modellelemente (Modellnamen, Topics, Klassen, Attribute etc.) werden ausschliesslich auf Deutsch bezeichnet.

*#302*: Namen von Topics, Klassen, Assoziationen und Attributen sollte nicht länger als 29 Zeichen sein.

*#303*: Topic-Namen: Gross- und Kleinschrift mit Underscore als Trennzeichen. Plural.

*#304*: Klassen-Namen: Gross- und Kleinschrift mit Underscore als Trennzeichen. Singular.

*#305*: Attribut-Namen: Gross- und Kleinschrift mit Underscore als Trennzeichen. Singular.

*#306*: Die Verwendung von reservierten Namen ist nicht erlaubt.

Modellstruktur
--------------

*#401*: Es müssen die Geometrietypen aus dem CHBase-Modell ``GeometryCHLV95_V1`` verwendet werden.

*#402*: Für Kantonskürzel muss ``CHCantonCode`` aus dem CHBase-Modell ``CHAdminCodes_V1`` verwendet werden

*#403*: BFS-Nummern sind als Wertebereich 0 .. 9999 zu definieren.

Einschränkungen zum Gebrauch von INTERLIS 2.3
---------------------------------------------

*#501*: Es dürfen nur zweiwertige (binäre) Beziehungen (ASSOCIATION) deklariert werden. Was heisst das??????

*#502*: Views dürfen nur in Validierungsmodellen verwendet werden.

*#503*: Für ``TEXT`` muss immer eine konkrete Länge angegeben werden.

*#504*: Externe Objektkataloge und Codelisten dürfen nicht verwendet werden.

Konsistenzbedingungen
---------------------

*#601*: Die Kardinalitäten von Rollen muss erfasst werden.

*#602*: UNIQUE-Bedingungen müssen erfasst werden.

*#603*: Als OID wird ``INTERLIS.UUIDOID`` verwendet.

Darstellungsmodell Eigenes Modell??? Taucht vorher nirgends auf.
------------------

*#701*: Textpositionen werden nur definiert, wenn diese schwer aus den Daten berechnet werden können oder spezielle Anforderungen an die Darstellung bestehen.

*#702*: Für Labelorientierungen etc. wird die Einheit ``Units.Angle_Degree`` verwendet.

Allgemeines
--------------

*#801*: Allgemeiner Grundsatz: Es wird nur die IST-Situation beschrieben. Also weder Archivierung noch Historisierung respektive die dafür benötigten Attribute.



Beispielheader
--------------

::

  INTERLIS 2.3; 
  !!============================================================================== 
  !!@ File = "SO_AV_Nachfuehrungskreise_20160521.ili"; 
  !!@ Title = "AV-Nachführungskreise"; 
  !!@ shortDescription = "Nachführungskreise der amtlichen Vermessung im Kanton Solothurn"; 
  !!@ Issuer = "http://www.agi.so.ch"; 
  !!@ technicalContact = "mailto:agi@bd.so.ch"; 
  !!@ furtherInformation = "http://models.geo.so.ch/AGI/SO_AV_Nachfuehrungskreise_2016_05_21.pdf"; 
  !!@ kGeoiV_ID = "SO-1004"; 
  !!  Erfassungsmodell;
  !!  Compiler-Version = "4.5.22-20160407"; 
  !!------------------------------------------------------------------------------ 
  !! Version    | wer | Änderung 
  !!------------------------------------------------------------------------------ 
  !! 2016-02-11 | P1  | Erstfassung 
  !! 2016-05-21 | P2  | Finalisierung und Abschluss 
  !!============================================================================== 
  MODEL SO_AV_Nachfuehrungskreise_20160521(de) 
    AT "http://geo.so.ch/models/AGI" 
    VERSION "2016-05-21" = 

  END SO_AV_Nachfuehrungskreise_20160521.
