Coding da Vinci 2017
====================

[Coding da Vinci](https://codingdavinci.de/) ist ein Kulturhackathon. Es geht um offene Daten und aus Kulturinstitutionen. 2017 lag der Fokus auf Berlin.

Die Challenge
-------------

![Tweet](https://raw.githubusercontent.com/tursics/coding-da-vinci-2017/master/docs/twitter-plusha.png)

Helene fragte sich, ob ich es schaffen könnte, alle stadtbezogenen Daten von den beteiligten Kulturinstitutionen miteinander zu verknüpfen. Es geht hier um die örtliche Verknüpfung. Vorraussetzung ist, dass alle Daten (meist Bilder, Fotos, Zeichnungen, Gemälde, ...) über Geocoordinaten verfügen.

Dieses Projekt soll allen Kulturdaten Geopunkte zuweisen. Das Ergebnis soll idealerweise **eine GeoJSON-Datei pro Institution** sein. Am Ende also eine einfache Karte.

Der Hackathon startete am 21. Oktober und geht 6 Wochen.

Die Institutionen
-----------------

**Stadtmuseum Berlin**

- Datensatz: 1000x Berlin
- ca. 1300 Objekte
- Stadtansichten und 'vor den Toren der Stadt'
- Fußgänger- und Vogelperspektive

Goal: Riesige TIFF-Karten (sind allerdings nachzufragen)

---

**FHXB Friedrichshain-Kreuzberg Museum**

- Datensatz: Künstlerkreis Kreuzberger Boheme
- 416 Kunstwerke, u.a. Stadtansichten

Goal: LIDO-XML (falsche Info für Metadata. Sie stehen unter CC-0)

---

**Humboldt-Universität zu Berlin, Institut für Kunst- und Bildgeschichte, Mediathek**

- Datensatz: Historische Glasdiasammlung
- ca. 55.000 Bilder (4.000 bereits verfügbar)
- weltweite Daten, teilweise aus Berlin
- enthalten teilweise Metadaten

Goal: mittelgroße Bilddatei, testweise kml-Ortsdatei (aber nur Städtenamen)

Kontakt: georg.schelbert@hu-berlin.de

---

**Landesdenkmalamt Berlin**

- Datensatz: Denkmalinformationssystem
- ca. 1000 seitiges PDF
- der Datenbankdump ist am Besten
- es gibt eine Denkmalliste in Wikipedia
- es gibt Fotos über 'Wiki loves Monuments'

Goal: Daten werden in einer Doc-Datei gepflegt

Kontakt: juliane.stamm@lda.berlin.de

Recherche:
- [Wikiprojekt](https://de.wikipedia.org/wiki/Wikipedia:WikiProjekt_Listen_der_Kulturdenkmale_in_Berlin)
- [Liste in Wikipedia](https://de.wikipedia.org/wiki/Liste_der_Kulturdenkmale_in_Berlin)
- [Datensatz im Datenportal](https://daten.berlin.de/datensaetze/denkmalliste-des-landes-berlin)
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

**Stiftung Berliner Mauer**

- Datensatz: Mauer-Fotos
- ca. 200 Fotos

Goal: Sind bereits geogetaggt

---

**Berlinische Galerie**

- Datensatz: Berliner Stadtansichten 
- ca. 515 Datensätze mit Fotos aus der Mitte bis Ende des 19. Jahrhunderts

Goal: LIDO-DDB XML

---

**Stadtmuseum Berlin**

- Datensatz: Heinrich Zille - Ein Berliner unter Berlinern
- einige Fotos mit Stadtansichten, viele Personenmotive (insgesamt 2500 Bilder)

---

**Wikidata**

- Basisinfos zu Objekten

Goal: Man könnte unterschiedliche Schreibweisen und Zusatzinfos zu Objekten finden und Querverbindungen



