# Verbesserungen von Version 1.0 zu Version 1.1

**Datum:** 15. Oktober 2025

## Übersicht
Dieses Dokument beschreibt die notwendigen Verbesserungen und Änderungen zwischen Version 1.0 und Version 1.1 des Wechselbalg50 Röhrenverstärkers.

---

## 1. Kathoden-Heizung Spannungsdifferenz

### Problem
Die Spannungsdifferenz zwischen Kathode und Heizung darf gemäß Röhrenspezifikation maximal 100V betragen. Bei der aktuellen Schaltung V1.0 besteht die Gefahr, dass die Kathode der Tone-Stack-Vorstufe auf ca. 160V ansteigt, was die zulässige Differenz überschreitet.

### Geplante Maßnahmen

#### 1.1 Überprüfung aller Kathodenspannungen
- [ ] Messung aller Kathodenspannungen im Betrieb
- [ ] Dokumentation der gemessenen Werte
- [ ] Vergleich mit zulässigen Maximalwerten der verwendeten Röhren
- [ ] Besondere Aufmerksamkeit auf Tone-Stack-Vorstufe

#### 1.2 Heater Voltage Elevation (falls erforderlich)
**Bedingung:** Wenn Kathodenspannung > 90V

**Maßnahme:** Heizspannungsanhebung um 75V

- [ ] Implementierung einer Heater Voltage Elevation Schaltung
- [ ] Anhebung der Heizspannung um 75V
- [ ] Neuberechnung der Kathode-Heizung-Differenz
- [ ] Verifizierung: Differenz < 100V
- [ ] Anpassung des Schaltplans (Schematic Update)
- [ ] Update der PCB-Layout falls erforderlich

#### 1.3 Umstellung auf 5V Relais-Steuerung (falls 1.2 implementiert wird)
**Bedingung:** Wenn Heater Voltage Elevation implementiert wird

**Hintergrund:** Durch die Heizspannungsanhebung wird eine separate 5V Versorgung für die Relais-Steuerung erforderlich.

**Maßnahme:** Implementierung 5V Versorgung und Umstellung auf 5V Relais

- [ ] Recherche und Auswahl geeigneter 5V Relais für Kanalumschaltung
- [ ] 5V Wicklung vom Transformator nutzen (falls vorhanden) oder separate Lösung
- [ ] Brückengleichrichter für 5V AC Wicklung
- [ ] LDO Spannungsregler für 5,0V Regulierung (analog zur 12V Versorgung)
- [ ] Schaltplan Update: 5V Versorgungssektion
- [ ] Schaltplan Update: Relais-Ansteuerung auf 5V umstellen
- [ ] PCB Update: 5V Relais Footprints
- [ ] BOM Update: 5V Relais, LDO für 5V, Brückengleichrichter

### Erwartetes Ergebnis
- Kathodenspannung Tone-Stack: ~160V (gemessen)
- Heizspannung (elevated): +75V
- Resultierende Differenz: ~85V ✓ (< 100V Limit)

---

## 2. Thermisches Management / PCB-Layout

### Problem
Die Wärmeentwicklung der Röhren kann zu erhöhten Temperaturen auf der PCB führen, was die Lebensdauer und Zuverlässigkeit der Bauteile beeinträchtigen kann.

### Geplante Maßnahmen

#### 2.1 Temperaturmessung und Analyse
- [ ] Temperaturmessung auf der PCB im Betrieb (verschiedene Lastbedingungen)
- [ ] Identifikation von Hotspots
- [ ] Messung der Bauteiltemperaturen in Röhrennähe
- [ ] Dokumentation der Temperaturen (Idle, Normal, Vollast)
- [ ] Vergleich mit maximalen Betriebstemperaturen der Bauteile

#### 2.2 PCB-Layout Optimierung (falls erforderlich)
**Bedingung:** Wenn Bauteiltemperaturen kritische Werte erreichen

**Maßnahme:** Vergrößerung des Abstands zwischen Röhrensockeln und temperaturkritischen Bauteilen

- [ ] Analyse: Welche Bauteile sind besonders temperaturempfindlich?
- [ ] PCB-Layout Revision: Bauteile weiter von Röhrensockeln positionieren
- [ ] Berücksichtigung thermischer Konvektion (heiße Luft steigt auf)
- [ ] Ggf. Verwendung von Bauteilen mit höherer Temperaturklasse
- [ ] Ggf. zusätzliche Kühlung/Belüftung in Betracht ziehen
- [ ] PCB Update für Version 1.1
- [ ] Prototyp-Test mit Temperaturmessung zur Validierung

### Erwartetes Ergebnis
- Alle Bauteile arbeiten innerhalb ihrer spezifizierten Temperaturbereiche
- Erhöhte Zuverlässigkeit und Lebensdauer
- Reduziertes Risiko von thermisch bedingten Ausfällen

---

## Weitere geplante Verbesserungen
_(Hier können weitere Punkte ergänzt werden)_

---

## Status
- **Version 1.0:** Aktuell in Entwicklung
- **Version 1.1:** Geplant
- **Hauptgrund für Update:** Einhaltung Kathode-Heizung Spannungsdifferenz

