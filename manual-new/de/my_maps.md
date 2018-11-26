<!-- WARNING: This file is autogenerated by csv2md.py -->
# Meine Karte


## <a name="sec0"></a>Projekte

Karten können als Projekte geladen und gespeichert werden. Es wird das QGIS Projektformat verwendet, mit Endung _*.qgs_. Projekte werden aus Vorlagen erstellt. Beim Starten der Applikation wird automatisch ein Projekt aus einer Online- oder Offline-Vorlage erstellt, abhängig davon, ob der Rechner am Netz angeschlossen ist.


## <a name="sec1"></a>Datenquellen

Die Hauptdatenquelle ist der **_Geodatenkatalog_**. Beim Programmstart werden nur öffentliche Daten angezeigt. Abhängig vom Benutzer können nach erfolgter Authentifizierung weitere Daten zur Verfügung stehen. Die Authentifizierung erfolgt via Schloss-Symbol in der Geodaten-Toolbar. Nach erfolgreicher Authentifizierung wird der Geodatenkatalog automatisch neu geladen.

Zusätzlich können lokale Vektor- sowie Rasterdaten der Karte hinzugefügt werden, entweder via Symbol in der Geodaten-Toolbar oder per Drag and Drop auf die Karte.


## <a name="sec2"></a>Neue Projekte anlegen und Speichern

Mit den Funktionen **_Neu_**, **_Öffnen_**, **_Speichern_** und **_Speichern als_** können neue Projekte (aus einer Vorlage) erstellt werden, existierende Projekte geöffnet werden und Projekte gespeichert werden.

Gewisse Werkzeuge erzeugen Datensätze, die in Ordner _< projektname > files_ abgelegt werden. Beim austauschen des Projekts sollte dementsprechend dieser Ordner zusammen mit der Projektdatei verteilt werden. Weitere lokale Datensätze die ausgetauscht werden sollten ebenfalls in diesem Verzeichnis abgelegt werden und von dort aus der Karte hinzugefügt werden, ansonsten wird dessen Pfad im Projekt als absoluter Pfad gespeichert, der möglicherweise auf anderen Systemen nicht aufgelöst werden kann.


## <a name="sec3"></a>Projekte öffnen

Gespeicherte Karten (Projekte) können mit der Funktion **_Öffnen_** geladen werden.


## <a name="sec4"></a>Drucken

Die aktuelle Karte kann über die Funktion **_Drucken_** auf den Drucker ausgegeben oder in einer Datei gespeichert werden.

Das Drucken basiert auf Vorlagen. Standardmässig werden Vorlagen für A0 bis A6 sowohl Quer- als Hochformat angeboten, sowie eine Custom Vorlage.


Bei ausgewählter Vorlage wird im Hauptkartenfenster ein blaues halb-transparentes Rechteck angezeigt, welches dem zu druckenden Ausschnitt entspricht. Bei den Vorlagen mit fixem Papierformat kann dieses Rechteck in der Hauptkarte verschoben werden, um den Druckbereich anzupassen. Die Grösse des Ausschnitts wird vom Papierformat und dem im Druckdialog angegebenen Massstab abgeleitet. Bei der _Custom_ Vorlage wird der Ausschnitt zusammen mit dem Massstab im Druckdialog numerisch definiert, und das resultierende Papierformat wird diesen Angaben entsprechend dynamisch berechnet.


Beim Drucken können zusätzliche Elemente, Koordinatengitter, Kartenkartusche, Legende, und Massstabbalken je nach Wunsch ein- oder ausgeblendet werden. Die Position dieser Elemente ist in der Vorlage definiert. 

<img src="../media/image12.png" />

### Druckdialog

+ **Vorlage**: Auswahl der Druckvorlage. Es wird eine Vorschau der Druckausgabe angezeigt.
+ **Titel**: Titel, der auf der Druckausgabe angezeigt wird.
+ **Massstab**: Druckmassstab
+ **Gitter**: Wird der Abschnitt Gitter aufgeklappt, wird im Ausdruck ein Gitternetz hinterlegt.
  + **Koordinatensystem**: Wahl des Gitter-Koordinatensystems
  + **X Intervall**: Abstand der Gitternetzlinien in X-Richtung
  + **Y Intervall**: Abstand der Gitternetzlinien in Y-Richtung
  + **Koordinatenbeschriftungen**: Ein-/Ausschalten der Gitternetzbeschriftungen
+ **Kartenkartusche**: Ein-/Ausschalten der Kartusche
+ **Kartenkartusche anpassen**: Konfiguration der Kartusche
+ **Massstabsbalken**: Ein-/Ausschalten der Masstabsanzeige
+ **Legende**: Ein-/Ausschalten der Legende
+ **Dateiformat**: Auswahl des Formats für die Datei-Export Funktion


### Karten-Kartusche

Im diesem Dialog wird der Inhalt der **_Kartusche_** bestimmt. In den Eingabefeldern ist die Funktion des Textes hinterlegt. Ist die Checkbox **Übung** aktiviert, werden die Angaben zu einer Übung in der Kartusche angezeigt.

Des weiteren kann im Kartuschen-Dialog der Kartuscheninhalt als einzelständige XML Datei importiert und exportiert werden.


### Druckausgabe

+ **Exportieren**: Es wird eine Datei im gewählten Format erstellt.
+ **Drucken**: Über den Druckdialog kann ein eingerichter Drucker ausgewählt und die Ausgabe gestartet werden.
+ **Schliessen**: Der Druckdialog wird geschlossen.
+ **Fortgeschritten**: Aufruf der der erweiterten Layout-Funktionalität 


### Druckvorlagen

Die Druckvorlagen die im Projekt enthalten sind können im Druckzusammenstellungsdialog verwaltet werden, der durch die Schaltfläche rechts vom der Druckvorlageselektion geöffnet werden kann. Dort können einzelne Vorlagen importiert, exportiert sowie aus dem Projekt entfernt werden.

<img src="../media/image12.1.png" />

## <a name="sec5"></a>Karte Kopieren / Karte Speichern

Diese Funktionen erlauben dem Benutzer, den im Hauptfenster sichtbaren Kartenausschnitt in die **_Zwischenablage_** oder in eine Datei zu speichern. Es wird jeweils immer genau der Inhalt des Kartenfenster gespeichert.

Die Funktion **_Karte speichern_** öffnet eine Dateidialog, wo sie den Namen, Pfad und Bildtyp (PNG, JPG und weitere Formate) auswählen. Eine World-Datei, die die Erweiterung PNGW oder JPGW enthält und im selben Ordner gespeichert wird, georeferenziert das Bild.


## <a name="sec6"></a>KML / KMZ Export

Der Karteninhalt kann zudem als KML oder KMZ exportiert werden. Bilder sowie MSS-Symbole der Lagedarstellung werden nur im KMZ Format exportiert.

> Es soll beachtet werden, dass KMZ und KML verlustbehaftete Export-Formate sind, und daher nicht geeignet für den Austausch zwischen KADAS Anwender ist. Dazu sollte das native _*.qgs_ Projektformat verwendet werden.


## <a name="sec7"></a>GPKG Export / Import



