Einleitung
==========
Das Modellierungshandbuch dient der Erstellung von kantonalen (minimalen) Geodatenmodellen.
Dabei muss es sich nicht nur um Geodatenmodelle gemäss KGeoIV handeln, sondern im Kontext des
modellbasierten Ansatzes (aka model-driven GDI) sollen diese Modellierungsregeln bewusst auch bei
allen anderen konzeptionellen Datenmodellen angewendet werden.

Die Modellierungsregeln sind minimal gehalten und können im Laufe der Zeit ändern.

Weitere wichtige Informationen zum Modellierungsprozess und zu Formalitäten finden sich im
Dokument «Allgemeine Empfehlungen zur Methodik der Definition ‹minimaler Geodatenmodell›».


Modellierungssprache / Compiler
-------------------------------
+-----------------------------------------+-----------------------------------------+
| Beschreibung                            | Hinweis / Beispiel                      |
+-----------------------------------------+-----------------------------------------+


+--------------+---------------------+
| Beschreibung | Hinweise / Beispiel |
+==============+=====================+
|              |                     |
+--------------+---------------------+
|              |                     |
+--------------+---------------------+
|              |                     |
+--------------+---------------------+

+----------------------------------------------------------------------------------------+---------------------------------------------+
| Beschreibung                                                                           | Hinweise / Beispiel                         |
+----------------------------------------------------------------------------------------+---------------------------------------------+
| Modellierungssprache ist INTERLIS 2.3 gemäss Referenzhandbuch vom 13. April 2006.      |                                             |
+----------------------------------------------------------------------------------------+---------------------------------------------+
| Für die Kontrolle der Datenmodelle wird der INTERLIS-Compiler Version 4.5.22 vom       |                                             |
| 7. April 2016 (oder höher) eingesetzt.                                                 |                                             |
+----------------------------------------------------------------------------------------+---------------------------------------------+
| Die verwendete Compiler-Version ist im Modell-Header anzugeben.                        | ``!! Compiler-Version =„4.5.22-20160407“;`` |
+----------------------------------------------------------------------------------------+---------------------------------------------+
| Der Namensraum für Modelle ist *http://geo.so.ch/models/AMT* wobei das entsprechende   | ``MODEL SO_AV_Nachfuehrungs-``              |
| Amt resp. der Ordner in der Modellablage, in welchem das Modell liegt, angegeben wird. | ``kreise_20160521 (de) AT``                 |
|                                                                                        | ``„http://geo.so.ch/models/AGI“``           |
+----------------------------------------------------------------------------------------+---------------------------------------------+