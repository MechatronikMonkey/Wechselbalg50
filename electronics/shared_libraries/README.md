# Gemeinsame Bibliotheken für Wechselbalg50

Dieser Ordner enthält gemeinsame Bibliotheken für die Projekte im Wechselbalg50-Repository.

## Struktur

- `symbols/`: Enthält Symbol-Bibliotheken (.kicad_sym)
- `footprints/`: Enthält Footprint-Bibliotheken (.pretty)
- `3dmodels/`: Enthält 3D-Modelle für die Footprints

## Verwendung

Die Projekte im Repository sind bereits so konfiguriert, dass sie auf diese gemeinsamen Bibliotheken zugreifen.
Die Pfade in den Bibliothekstabellen (`sym-lib-table` und `fp-lib-table`) verwenden den relativen Pfad `${KIPRJMOD}/../shared_libraries/...`.

## Hinzufügen neuer Symbole/Footprints

Wenn du neue Symbole oder Footprints erstellen möchtest, die in mehreren Projekten verwendet werden sollen:

1. Öffne KiCad und den Symbol- oder Footprint-Editor
2. Stelle sicher, dass du auf die gemeinsame Bibliothek als aktive Bibliothek eingestellt hast
3. Erstelle dein neues Symbol/Footprint und speichere es in der gemeinsamen Bibliothek
4. Es wird dann automatisch in allen Projekten verfügbar sein, die auf die gemeinsame Bibliothek verweisen

## 3D-Modelle

Für 3D-Modelle sollte der Pfad in den Footprint-Eigenschaften entsprechend angepasst werden. 
Verwende `${KIPRJMOD}/../shared_libraries/3dmodels/...` anstelle von lokalen Pfaden.