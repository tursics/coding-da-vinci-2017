Coding da Vinci 2017
====================

[Coding da Vinci](https://codingdavinci.de/) ist ein Kulturhackathon. Es geht um offene Daten und aus Kulturinstitutionen. 2017 lag der Fokus auf Berlin.

Die Challenge
-------------

![Tweet](https://raw.githubusercontent.com/tursics/coding-da-vinci-2017/master/docs/twitter-plusha.png)

Helene fragte sich, ob ich es schaffen könnte, alle stadtbezogenen Daten von den beteiligten Kulturinstitutionen miteinander zu verknüpfen. Es geht hier um die örtliche Verknüpfung. Vorraussetzung ist, dass alle Daten (meist Bilder, Fotos, Zeichnungen, Gemälde, ...) über Geocoordinaten verfügen.

Dieses Projekt soll allen Kulturdaten mit Stadtansichten Geopunkte zuweisen. Das Ergebnis soll idealerweise **eine GeoJSON-Datei pro Institution** sein. Am Ende also eine einfache Karte.

Der Hackathon startete am 21. Oktober und geht 6 Wochen.

Die Institutionen
-----------------

Stand vom 22. Oktober 2017

8 Datenquellen von Institutionen haben Stadtansichten von Berlin
- 1 API hat 48 Treffer für Berlin, 4621 für Deutschland, mit 0 Geopositionen (0%)
- 1 Denkmalliste enthält ca. 34000 Objekte mit 20.401 Geopositionen (60%)
- 1 Datensatz enthält 200 Objekte mit 196 Geopositionen (98%)
- 5 Datensätze enthalten LIDO-Daten mit 5.331 Objekten mit 417 Geopositionen (7,8%)

Museum  | Datensatz | Format | DDB | Objekte | Bilder | Geo-Koordinaten | Metadaten |
--------|-----------|--------|:---:|--------:|-------:|----------------:|-----------|
Humboldt-Universität zu Berlin, Institut für Kunst- und Bildgeschichte  |Historische Glasdiasammlung  |API  |nein  |48  |48  |"Berlin"|[0,1 MByte](http://imeji-mediathek.de/imeji/rest/items?q=q=((bjPdsFEA_f4gqRo0%3Atext%3D%22Berlin%22)))
Landesdenkmalamt Berlin      |Denkmalinformationssystem  |DOC-Datei  |nein  |34000  |0  |0  |[ca. 1000 Seiten](https://daten.berlin.de/datensaetze/denkmalliste-des-landes-berlin)
Stiftung Berliner Mauer      |Mauer-Fotos  |CSV  |nein  |200  |200  |196  |[0,2 MByte](http://www.mauer-fotos.de/site/assets/files/31020587/coding-da-vinci-metadaten.csv)
Stiftung Stadtmuseum Berlin  |1000x Berlin  |LIDO-XML  |ja  |  1169|1290  |0  |[10,8 MByte](http://136.243.4.67/index.php/s/v0UEpnXQcCOOZy3)
Stiftung Stadtmuseum Berlin  |Heinrich Zille - Ein Berliner unter Berlinern  |LIDO-XML  |ja  |2608  |2668  |0  |[26,1 MByte](http://136.243.4.67/index.php/s/rijMXOyuszSxUYH)
Berlinische Galerie          |Heinrich Zille Konvolut  |LIDO-XML  |ja  |624  |624  |0  |[6,1 MByte](http://136.243.4.67/index.php/s/TSoVCI2L4GustL6)
Berlinische Galerie          |Berliner Stadtansichten, Schwartz  |LIDO-XML  |ja  |159  |159  |0  |[1,5 MByte](http://136.243.4.67/index.php/s/bst1wUtBHnJyPuv)
Berlinische Galerie          |Berliner Stadtansichten, Rueckwardt  |LIDO-XML  |ja  |188  |188  |0  |[1,8 MByte](http://136.243.4.67/index.php/s/bst1wUtBHnJyPuv)
Berlinische Galerie          |Berliner Stadtansichten, Panckow  |LIDO-XML  |ja  |166  |166  |0  |[1,5 MByte](http://136.243.4.67/index.php/s/bst1wUtBHnJyPuv)
FHXB Friedrichshain-Kreuzberg Museum  |Künstlerkreis "Kreuzberger Boheme"  |LIDO-XML  |ja  |417  |417  |417  (immer der gleiche Punkt)|[4,1 MByte](http://136.243.4.67/index.php/s/047jsxdCtv9CtYE)

**Stiftung Stadtmuseum Berlin**

- Datensatz: 1000x Berlin
- Stadtansichten und 'vor den Toren der Stadt'
- Fußgänger- und Vogelperspektive
- Riesige TIFF-Karten (sind allerdings nachzufragen)
- [Mediendateien](http://136.243.4.67/index.php/s/dx0RUXWIV1S8MnP)

**FHXB Friedrichshain-Kreuzberg Museum**

- Datensatz: Künstlerkreis "Kreuzberger Boheme"
- Kunstwerke, u.a. Stadtansichten
- [API Dokumentation museum-digital](http://www.museum-digital.de/handbook/?lan=de&q=Ausgabe/APIs)
- Sammlungs-IDs als [Exceltabelle](http://136.243.4.67/index.php/s/2RmwERCaDGv2C8A)

**Stiftung Berliner Mauer**

- Datensatz: Mauer-Fotos
- [Metadaten – Runterscrollen zu Coding da Vinci](http://mauer-fotos.de/info/nutzungshinweise)
- [Fotos](http://www.mauer-fotos.de/)

**Berlinische Galerie**

- Datensatz: Heinrich Zille Konvolut
- Zille als Fotograf
- [Mediendaten](http://136.243.4.67/index.php/s/cHxfZmr1U34hcJK)

**Berlinische Galerie**

- Datensatz: Berliner Stadtansichten 
- Fotos aus der Mitte bis Ende des 19. Jahrhunderts
- [Mediendaten](http://136.243.4.67/index.php/s/ib48ePnU43Dcv4s)

**Stiftung Stadtmuseum Berlin**

- Datensatz: Heinrich Zille - Ein Berliner unter Berlinern
- einige Fotos mit Stadtansichten, viele Personenmotive (insgesamt 2500 Bilder)
- [Mediendateien](http://136.243.4.67/index.php/s/0rlgcVXHqdkq8vS)

**Humboldt-Universität zu Berlin, Institut für Kunst- und Bildgeschichte**

- Datensatz: Historische Glasdiasammlung
- ca. 55.000 Bilder (4.000 bereits verfügbar)
- weltweite Daten, teilweise aus Berlin
- enthalten teilweise Metadaten
- mittelgroße Bilddatei, testweise kml-Ortsdatei (aber nur Städtenamen)
- Kontakt: georg.schelbert@hu-berlin.de
- API: http://imeji-mediathek.de/imeji/rest/items?q=q=((bjPdsFEA_f4gqRo0%3Atext%3D%22Deutschland%22))&size=5000&offset=0
  - "Deutschland" hat 4621 Treffer
  - "Berlin" hat 48 Treffer
- Liste von Wikidata: http://imeji-mediathek.de/imeji/browse?q=%28%284zzImJyVhV_MJ3dV%3Alabel%3D%22%22Wikidata%22%22%29%29
- [API-Dokumentation](https://github.com/imeji-community/imeji/wiki)
- eine [GeoJSON-Datei](https://gist.github.com/schelbertgeorg/ac3e32a0b37230fc2ba90c096d2f0602)
- Hier soll sich eine [Swagger-Doku](https://helloreverb.com/developers/swagger) befinden, die API ist [hier](https://github.com/imeji-community/imeji/wiki) beschrieben

**Landesdenkmalamt Berlin**

- Datensatz: Denkmalinformationssystem
- der Datenbankdump ist am Besten
- es gibt eine Denkmalliste in Wikipedia
- es gibt Fotos über 'Wiki loves Monuments'
- Kontakt: juliane.stamm@lda.berlin.de
- [Metadaten](http://136.243.4.67/index.php/s/flgYzGjdkwi9nOe)
  - Denkmaldatenbank
    - 12150 Objekte
	- Straße + Hausnummer (keine Geodaten)
  - Denkmalliste
    - ca. 34000 Objekte
  - Geodaten
    - 20401 Geopunkte
- [Dokumentation](http://136.243.4.67/index.php/s/OZKvRAFK6BMzdSG/download)
- Denkmalkartierungen über [Web Map Service (WMS)](https://daten.berlin.de/datensaetze/denkmalkarte-berlin-wms) und [ATOM Feed](https://daten.berlin.de/datensaetze/denkmalkarte-berlin-atom)
- [Datensatz im Datenportal](https://daten.berlin.de/datensaetze/denkmalliste-des-landes-berlin)
- [Wikiprojekt](https://de.wikipedia.org/wiki/Wikipedia:WikiProjekt_Listen_der_Kulturdenkmale_in_Berlin)
- [Liste in Wikipedia](https://de.wikipedia.org/wiki/Liste_der_Kulturdenkmale_in_Berlin)
- 1111 Einträge in Wikidata vorhanden
  - 105 keine Geokoordinaten
  - Recherche und [Wikidata Query](https://query.wikidata.org/#%23 Items with Berlin cultural heritage ID%0A%23 Einträge mit Objektdokumentennummer der Berliner Denkmaldatenbank%0A%23defaultView%3AMap%0ASELECT DISTINCT %3Fdenkmal %3FdenkmalLabel %3Fcoordinates WHERE {%0A %3Fdenkmal wdt%3AP2424 %3Fid %3B%0A wdt%3AP625 %3Fcoordinates .%0A SERVICE wikibase%3Alabel { bd%3AserviceParam wikibase%3Alanguage "[AUTO_LANGUAGE]%2Cde%2Cen". }%0A}) von Daniel Mietchen

```
# Items with Berlin cultural heritage ID
# Einträge mit Objektdokumentennummer der Berliner Denkmaldatenbank
#defaultView:Map
SELECT DISTINCT ?denkmal ?denkmalLabel ?coordinates WHERE {
  ?denkmal wdt:P2424 ?id ;
		   wdt:P625 ?coordinates .
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],de,en". }
}
```

![Wikidata](https://raw.githubusercontent.com/tursics/coding-da-vinci-2017/master/docs/denkmalliste-1.png)

---

**Wikidata**

- Basisinfos zu Objekten
- Man könnte unterschiedliche Schreibweisen und Zusatzinfos zu Objekten finden und Querverbindungen


Wissenswertes
-------------

Es gibt bereits tolle Projekte, die ich mir anschauen sollte:
- die allgemeine [Daten-Seite](https://codingdavinci.de/daten/) von Coding da Vinci
- [Historisches Datenmaterial als Karte](https://jochenklar.de/berlin/)
- [LIDO-Spec](http://network.icom.museum/cidoc/working-groups/lido/lido-technical/specification/)
- [LIDO DDB-Preview](https://www.servicestelle-digitalisierung.de/wissenswertes/ddb-preview/)

