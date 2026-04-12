# ELS – Screens & UX Auswertung & Abschlussbericht V0.1

Stand: April 2026

## Einstieg
Button "Auswertung & Abschluss" auf Incident-Detailseite oder eigenem Tab.

## Screen 1: Auswertungs-Dashboard (Live)
Zweck: Operatives Lagebild des laufenden Incidents
Layout: 2 Spalten (Patienten/Transport links | Ressourcen/Kommunikation/Qualitaet rechts)
Kopf: Incident-Header + Abschlussstatus-Badge
Bloecke: A Patientenlage | B Uebergaben & Prozesszeiten | C Transporte | D Ressourcen | E Kommunikation/Konflikte | F Datenqualitaet
Interaktion: Klick auf Kachel -> gefilterte Listansicht im Fachmodul

## Screen 2: Abschluss-Check
Zweck: Abschlusspruefung mit Blockern und Warnungen
Layout: Kopf (Ampel + Zusammenfassung) | Tabs/Chips (Patient/Transport/Ressourcen/Kommunikation/Bericht) | Listenbereich
Blocker: rot hervorgehoben, Sprunglinks in Fachmodule
Warnungen: gelb, Button "Warnung akzeptieren" mit Pflicht-Begruendungsfeld

## Screen 3: Berichtsvorschau & Druckansicht
Zweck: Vollbild-Vorschau aller 14 Kapitel
Layout: Sidebar Kapitelnavigation (1-14) + A4-orientierter Hauptbereich
Vor Freigabe: Freitextfelder editierbar, Buttons: Abschlusspruefung / Freigabe / Drucken
Nach Freigabe: read-only, nur Drucken + PDF

## Screen 4: PDF-Export & Versionsübersicht
Zweck: Versionsliste + PDF-Download
Inhalt: Tabelle (Version | Datum | Rolle | Freigabestatus | PDF-Link)
Button "PDF erzeugen" (nur nach Freigabe aktiv)
Namensschema: ELS_Abschlussbericht_[ID]_[Datum]_[Version].pdf

## Screen 5: Nachbearbeitung
Zweck: Dokumentarische Korrektur nach Abschluss (nicht operativ)
Hinweisbanner: "Incident ist dokumentarisch, nicht operativ nachbearbeitbar"
Liste offener Nachbearbeitungspunkte
Button "Neue Berichtsversion erzeugen"

## Rollen & Sichtbarkeit
- Alle Rollen: Auswertungs-Dashboard lesend
- Einsatzleitung + Admin: Abschluss starten, freigeben
- Fuehrungsassistenz: Freitexte ergaenzen
- Transportkoordination: Transport-Blocker klaeren
