# FloodEngine™ 3.4 - Avancerat översvämnings- och erosionsverktyg

## Installation

1. Ladda ner den bifogade zip-filen (`FloodEngine.zip`)
2. Öppna QGIS och gå till **Plugins > Hantera och installera plugins...**
3. Välj fliken **Installera från ZIP**
4. Klicka på knappen **Bläddra...** och välj den nedladdade zip-filen
5. Klicka på **Installera plugin**
6. Efter installationen kommer FloodEngine-ikonen att synas i QGIS verktygsfält

## Funktioner

FloodEngine 3.4 innehåller följande huvudfunktioner:

### GUI & Användarupplevelse
- Basic/Advanced toggle för enkel eller avancerad användning
- Mörkt läge (antracitgrått) för bättre visualisering
- Fet stil för FloodEngine™ i gränssnittet
- Slider för vattennivå med valfri höjd (0-20m)
- Slider för inbränningsdjup med textruta
- Konsekvent visuell design genom hela verktyget

### Modellfunktioner
- Översvämningsyta (polygon) beräknas från DEM + bathymetri + vattennivå
- Inbränning av vattendrag med anpassad sänkning längs linje
- Erosionsriskmodell med koppling till jordartstyp
- Flödespilar (vektorlager) med färg baserad på flödeshastighet
- Streamlines som alternativ till pilar (togglingbar)
- Hydraulisk tröghet och volymbevarande logik

### Indata
- Stöd för .tif och .asc för DEM
- Stöd för .csv bathymetri (valbara kolumner)
- Stöd för .shp jordarter
- Val av vattendrag för inbränning (.shp)

### Utdata
- Översvämningsyta som polygonlager (.shp eller .gpkg)
- Flödespilar/streamlines som vektorlager
- Erosionszoner som polygonlager
- Valbar loggfil (output till .txt)

## Användning

### Basic Mode
1. Välj DEM-fil (.tif eller .asc)
2. Lägg till bathymetridata (.csv) om tillgängligt
3. Ange vattennivå (m)
4. Klicka på "Kör modell"

### Advanced Mode
1. Välj DEM-fil (.tif eller .asc)
2. Lägg till bathymetridata (.csv) om tillgängligt
3. Ange vattennivå (m)
4. Välj jordartskarta (.shp) om erosionsberäkning önskas
5. Aktivera inbränning och välj vattendrag (.shp) om önskat
6. Justera inbränningsdjup med slidern
7. Välj utdataoptioner (erosion, flödespilar, streamlines, loggfil)
8. Klicka på "Kör modell"

## Resultat

Efter modellkörning kommer följande lager att laddas i QGIS:

1. **Översvämningsyta** - Polygon som visar översvämmade områden
2. **Flödespilar** - Vektorer som visar flödesriktning och hastighet (om valt)
3. **Streamlines** - Alternativ till flödespilar som visar flödesvägar (om valt)
4. **Erosionsrisk** - Polygon som visar områden med risk för erosion (om valt)

Resultaten sparas också i en separat mapp, namngiven efter datum/tid, vilket möjliggör enkel delning och återanvändning.

## Teknisk information

FloodEngine använder följande algoritmer och metoder:

- **Översvämningsberäkning**: Baseras på en förenklad "bathtub"-modell med djupinformation
- **Inbränning**: Sänker höjdmodellen längs vattendrag för att säkerställa rätt flödesvägar
- **Erosionsmodell**: Kombinerar lutning, jordart och flödeshastighet för riskbedömning
- **Flödesberäkning**: Baseras på höjdgradient för att beräkna riktning och hastighet

## Krav

- QGIS 3.0 eller senare
- Python 3.6 eller senare
- GDAL/OGR-bibliotek (installeras med QGIS)

## Support

För frågor eller support, kontakta FloodEngine-teamet på floodengine@example.com

---

© 2025 FloodEngine Team
