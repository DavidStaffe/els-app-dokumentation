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


## Schritt 10: Einsatzabschnitte

Erweitere den Incident-Kontext um ein Einsatzabschnitt-Modul. Einsatzabschnitte sind benannte Teilbereiche eines Incidents (z.B. "Abschnitt Nord", "BHP", "Zelt A") denen Ressourcen zugeordnet werden können.

Datenmodell:
- id, incident_id, name (Freitext), farbe (Farbkodierung zur visuellen Trennung), beschreibung (optional), erstellt_um (Zeitstempel), aktiv (boolean)
- Ressourcen-Zuweisung: jede Ressource kann genau einem Abschnitt zugeordnet sein (oder keinem)

Anlegen & Bearbeiten:
- Bei Incident-Erstellung: optionaler Schritt "Einsatzabschnitte anlegen" im Setup-Wizard (überspringbar)
- Im laufenden Incident: Modul erreichbar über Hauptnavigation oder aus Ressourcen-Übersicht
- Aktionen je Abschnitt: umbenennen, Farbe ändern, deaktivieren (kein Löschen bei laufendem Incident), Ressourcen zuweisen/entfernen

UI-Screen "Einsatzabschnitte":
- Kachelansicht: jeder Abschnitt als farbige Kachel mit Name, Anzahl zugewiesener Ressourcen, Status-Überblick der Ressourcen (Ampel: alle verfügbar / teilweise im Einsatz / kritisch)
- Button "+ Abschnitt anlegen" prominent
- Klick auf Kachel: Detailansicht mit vollständiger Ressourcenliste des Abschnitts, Ressourcen-Status je Zeile, direkte Zuweisung/Entfernung weiterer Ressourcen
- In der Ressourcen-Statusmatrix (Schritt 06): neue Spalte "Abschnitt" mit Farbpunkt und Name
- Ressource ohne Abschnitt-Zuweisung erscheint in Kategorie "Nicht zugewiesen" (grau)

Integration Abschluss-Check:
- Warnung wenn Ressourcen ohne Abschnitt-Zuweisung vorhanden (> 20% der Ressourcen)
- KPI im Auswertungs-Dashboard: Anzahl Abschnitte, Ressourcenverteilung je Abschnitt

## Schritt 11: UHS – Unterabschnitt Behandlungsplatz (Betten)

Erweitere das Modul um einen Unterabschnittstyp "UHS / Behandlungsplatz" mit verwaltbaren Behandlungsbetten. Betten sind benannte Plätze (z.B. "Bett 1", "Liege 3", "Schockraum") an denen Patienten platziert und von dort weiter behandelt werden können.

Datenmodell Behandlungsbett:
- id, incident_id, abschnitt_id (optional: Bett kann einem Einsatzabschnitt angehören), name (Freitext), typ: ENUM [Liegend | Sitzend | Schockraum | Beobachtung | Sonstiges], status: ENUM [Frei | Belegt | Gesperrt], patient_id (FK, nullable), belegt_seit (Zeitstempel, automatisch bei Zuweisung), erstellt_um

Anlegen & Bearbeiten:
- Bei Incident-Erstellung: optionaler Schritt "Behandlungsplätze konfigurieren" im Setup-Wizard (überspringbar) – Schnellerfassung: Anzahl eingeben + Typ â€” Auto-Benennung (Bett 1, Bett 2 ...)
- Im laufenden Incident: Betten hinzufügen, umbenennen, Typ ändern, sperren. Kein Löschen belegter Betten
- Bestehende Betten können einem Einsatzabschnitt zugeordnet werden

UI-Screen "Behandlungsplätze":
- Rasteransicht: jedes Bett als Kachel, farbkodiert nach Status (Frei: grün / Belegt: rot / Gesperrt: grau)
- Belegte Kachel: zeigt Patienten-Kennung, Sichtungsstufe-Badge (S1-S4 farbig), Zeit seit Belegung
- Freie Kachel: Button "Patient zuweisen" öffnet Modal mit Patientenliste (filtert auf: Status = wartend/behandelbar, noch kein Bett zugewiesen)
- Belegte Kachel: Buttons "Patient-Detail", "Transport anfordern", "Bett freigeben"
- Bett-Typ-Icon je Kachel (Liege, Stuhl, Stern für Schockraum)
- Filter-Chips: Alle / Frei / Belegt / Gesperrt / Nach Abschnitt
- Button "+ Bett anlegen" und "Schnell-Setup" (Anzahl + Typ)

Patient-Kontext:
- Im Patientendetail (Schritt 04): neues Feld "Bett-Zuweisung" – zeigt aktuelles Bett, Bett ändern/freigeben möglich
- Ein Patient kann nur einem Bett gleichzeitig zugewiesen sein
- Bei Transport-Abschluss: Bett wird automatisch freigegeben

Integration Abschluss-Check:
- Blocker: Patienten mit Status aktiv ohne Bett-Zuweisung UND ohne Transport (unklärer Verbleib)
- Warnung: Betten im Status Gesperrt über gesamte Incident-Dauer (nie genutzt)
- KPI im Auswertungs-Dashboard Block A: durchschnittliche Bett-Belegungsdauer, maximale Gleichzeitigkeit, Bett-Auslastung gesamt

## Schritt 12: Integration Einsatzabschnitte + UHS in Gesamtapp

Verbinde die neuen Module (Schritt 10 + 11) nahtlos mit der bestehenden App-Architektur.

Incident Setup-Wizard – erweiterter Ablauf:
1. Incident-Grunddaten (Name, Typ, Ort, Datum)
2. Einsatzabschnitte anlegen (optional, überspringbar) – Kacheln direkt im Wizard
3. Behandlungsplätze konfigurieren (optional, überspringbar) – Schnell-Setup pro Abschnitt
4. Ressourcen importieren/anlegen (bereits vorhanden, Abschnitt-Zuweisung jetzt möglich)
5. Zusammenfassung + Incident starten

Hauptnavigation:
- Neue Nav-Einträge: "Abschnitte" und "Behandlungsplätze" sichtbar für Rollen EL und Sanitäter
- Dokumentar: nur Lesezugriff

Lagebildschirm (falls vorhanden) oder Ressourcen-Übersicht:
- Gruppierung der Ressourcen-Matrix nach Einsatzabschnitt mit farbiger Trennlinie
- Bett-Status-Zusammenfassung je Abschnitt als Kompakt-Widget

Patientenfluss komplett:
Patient angelegt → Bett zuweisen (aus Behandlungsplätze oder Patientendetail) → Behandlung → Transport anfordern → Transport abschließen → Bett automatisch freigegeben

Demo-Incident (Schritt 08 ergänzen):
- Demo-Daten enthalten: 2 Einsatzabschnitte, 6 Behandlungsbetten (4 belegt, 2 frei), realistische Patientenzuweisung auf Betten

Abschluss-Checkliste (Schritt 09 ergänzen):
- Blocker: Patienten aktiv ohne Bett und ohne Transport
- Warnung: Abschnitte ohne zugewiesene Ressourcen
- Warnung: Betten gesperrt (nie genutzt)
- KPI-Block A ergänzen: Bett-Auslastung %, max. Gleichzeitigkeit, Ø Belegungsdauer
- KPI-Block C ergänzen: Ressourcen je Abschnitt, Abschnitt-Übersicht im Bericht Kapitel 4

Pruefen: Konsistenz zwischen allen Screens sicherstellen – kein Screen zeigt veraltete Zustände. Bett-Status und Abschnitt-Zuweisung müssen überall reaktiv aktualisiert werden (kein manuelles Reload).
