# ELS – Paste-Ready Prompts Emergent V3

Stand: April 2026 | Ziel: Hochwertige Produktanmutung + Produktivsystem + Demo-Modus

## Nutzungsregeln
- Schritte 01-09 nacheinander ausfuehren
- Screenwirkung und Informationsarchitektur priorisieren
- Keine Showcase-Optik: echte operative Software-Anmutung
- Demo-Incidents: klar getrennter Modus, nicht Demo-Only

## Schritt 01: Produktbasis & Designsystem
Entwirf eine hochwertige Tablet-/Desktop-App fuer ein sanitaetsdienstliches Einsatzleitsystem. Erstelle ein konsistentes Designsystem: Farbpalette (Primaer, Status: rot/gelb/gruen/grau), Typografie (3 Groessen), Spacing (4px-Raster), Komponenten (Karte, Badge, Chip, Button, Modal, Tabelle). Nutze Emergent-Komponenten-Primitives. Kein Showcase, operative Anmutung.

> **Wichtig:** Alle benoetigen Spezifikations- und Referenzdateien befinden sich im verknuepften GitHub-Repository `DavidStaffe/els-app-dokumentation` (Ordner `/aktuell/`). Lies die dort hinterlegten Dateien (Kennzahlenkatalog, Gesamtspezifikation, Feldkatalog, Kapitelstruktur, Screens-UX, Handlungsablauf) **vor** dem Entwerfen und lege sie als Grundlage fuer saemtliche Design- und Funktionsentscheidungen zugrunde.

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

## Schritt 07: Zusätzliche Anforderung und Produktreife
Es muss eine Rollenauswahl implementiert werden. Die UI und die sichtbaren Screens, Aktionen, Navigationseinträge und Bearbeitungsmöglichkeiten müssen abhängig von der gewählten Rolle dargestellt werden.
Arbeite dabei mit den im Projekt definierten Rollen und leite die Rechte und Sichtbarkeiten aus den vorhandenen Dokumenten ab, insbesondere aus dem Handlungsablauf, der Gesamtspezifikation und dem Abschlussworkflow.
Setze die Rollenauswahl so um, dass:
- beim Einstieg eine Rolle gewählt oder simuliert werden kann,
- die Navigation danach rollenabhängig angezeigt wird,
- relevante Screens und Module je Rolle unterschiedlich sichtbar sind,
- Bearbeitungsrechte, Freigaben, Abschlussprüfung und Berichtsfunktionen je Rolle unterschiedlich verfügbar sind,
- lesende und schreibende Zugriffe klar getrennt sind,
- die Rollendarstellung konsistent durch die gesamte App geführt wird.

Dann pruefe alle Screens: konsistente Designsprache, klare Informationshierarchie, sinnvolle Leer-/Fehlerzustaende. Vermeide Inkonsistenzen zwischen Screens.

## Schritt 08: Demo-Integration
Fuege Demo-Modus ein: Button "Demo-Incident starten" mit realistischen Vordaten. Demo-Badge auf allen Screens. Demo-Daten filtierbar.

## Schritt 09: Auswertungs-Dashboard & Abschluss
Für das Modul „Auswertung & Abschlussbericht“ gilt :
- Das Auswertungs-Dashboard ist als operatives Lagebild zu gestalten, nicht als Analytics-Showcase.
- Der Abschluss-Check muss harte Blocker und weiche Warnungen visuell und funktional klar trennen.
- Die Berichtsvorschau muss A4-orientiert, druckfähig und wie ein echtes Einsatzdokument wirken.
- PDF-Export und Versionen müssen administrativ, vertrauenswürdig und nachvollziehbar gestaltet sein.
- Nachbearbeitung darf nur dokumentarisch erfolgen und den Incident nicht operativ reaktivieren.

Entwirf das Modul "Auswertung & Abschluss" mit professioneller operativer Absicht:
1. Auswertungs-Dashboard: 2-Spalten, dichte aber scannbare KPI-Kacheln, Bloecke A-F
2. Abschluss-Check: starke visuelle Trennung Blocker (rot) vs. Warnungen (gelb), Ampel-Kopf
3. Berichtsvorschau: professionelle A4-Optik, Sidebar-Kapitelnavigation 1-14
4. PDF-Versionen: klare Versionsliste, Freigabe-Status sichtbar
5. Nachbearbeitung: ruhiger Dokumentations-Screen, kein operativer Charakter
