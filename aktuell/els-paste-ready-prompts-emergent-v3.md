# ELS – Paste-Ready Prompts Emergent V3

Stand: April 2026 | Ziel: Hochwertige Produktanmutung + Produktivsystem + Demo-Modus

## Nutzungsregeln
- Schritte 01-09 nacheinander ausfuehren
- Screenwirkung und Informationsarchitektur priorisieren
- Keine Showcase-Optik: echte operative Software-Anmutung
- Demo-Incidents: klar getrennter Modus, nicht Demo-Only

## Schritt 01: Produktbasis & Designsystem
Entwirf eine hochwertige Tablet-/Desktop-App fuer ein sanitaetsdienstliches Einsatzleitsystem. Erstelle ein konsistentes Designsystem: Farbpalette (Primaer, Status: rot/gelb/gruen/grau), Typografie (3 Groessen), Spacing (4px-Raster), Komponenten (Karte, Badge, Chip, Button, Modal, Tabelle). Nutze Emergent-Komponenten-Primitives. Kein Showcase, operative Anmutung.

## Schritt 02: Einstieg & Incident-Auswahl
Entwirf den Einstiegsscreen mit Incident-Liste. Zeige Incident-Name, Typ, Dauer, Status als uebersichtliche Karten. Aktiver Incident ist im Global-Header sichtbar. Demo-Incidents haben ein klar sichtbares DEMO-Badge. Nutze das Designsystem aus Schritt 01.

## Schritt 03: Patientenliste
Entwirf die Patientenliste fuer einen aktiven Incident. Fokus: schnelle Scanbarkeit. Zeige Kennung, Sichtungsstufe (farbkodiert), Status, Verbleib. Filter als Chips. Neue Patienten anlegen. Verbinde mit Incident-Kontext.

## Schritt 04: Patientendetail
Entwirf den Patientendetail-Screen. Zeige Zeitstempel-Erfassung, Sichtungskategorie (=Behandlungsstart), Transportanforderung (intern/extern), Fallabschluss-Typ. Dauerkennzahlen kompakt sichtbar.

## Schritt 05: Transportuebersicht
Entwirf Transportuebersicht mit klarer intern/extern-Trennung. Zeige Status, Ressource, Ziel, Zeitstempel. Visuell klar: offene vs. abgeschlossene Transporte, fehlende Ressourcen.

## Schritt 06: Ressourcen, Kommunikation & Konflikte
Entwirf drei getrennte Module. Ressourcen: Statusmatrix je Typ, klar lesbar. Kommunikation: Meldungen priorisiert. Konflikte: rot/gelb farbkodiert nach Schwere.

## Schritt 07: Produktreife
Pruefe alle Screens: konsistente Designsprache, klare Informationshierarchie, sinnvolle Leer-/Fehlerzustaende. Vermeide Inkonsistenzen zwischen Screens.

## Schritt 08: Demo-Integration
Fuege Demo-Modus ein: Button "Demo-Incident starten" mit realistischen Vordaten. Demo-Badge auf allen Screens. Demo-Daten filtierbar.

## Schritt 09: Auswertungs-Dashboard & Abschluss
Entwirf das Modul "Auswertung & Abschluss" mit professioneller operativer Anmutung:
1. Auswertungs-Dashboard: 2-Spalten, dichte aber scannbare KPI-Kacheln, Bloecke A-F
2. Abschluss-Check: starke visuelle Trennung Blocker (rot) vs. Warnungen (gelb), Ampel-Kopf
3. Berichtsvorschau: professionelle A4-Optik, Sidebar-Kapitelnavigation 1-14
4. PDF-Versionen: klare Versionsliste, Freigabe-Status sichtbar
5. Nachbearbeitung: ruhiger Dokumentations-Screen, kein operativer Charakter
