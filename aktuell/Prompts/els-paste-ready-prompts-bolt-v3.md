# ELS – Paste-Ready Prompts Bolt.New V3

Stand: April 2026 | Ziel: Produktivsystem + integrierter Demo-Modus

## Nutzungsregeln
- Schritte 01-09 nacheinander ausfuehren
- Bestehende Komponenten wiederverwenden
- Kein Komplett-Umbau bei Folgeschritten
- Demo-Incidents = sauber getrennter Modus, kein Demo-Only-System

## Schritt 01: UI-Grundsystem
Erstelle eine produktionsnahe PWA/Tablet-App fuer ein sanitaetsdienstliches Einsatzleitsystem (ELS). Tech-Stack: React + TypeScript + Tailwind. Richte ein sauberes Routing-System ein mit Placeholder-Seiten fuer: Dashboard, Incidents, Patienten, Transport, Ressourcen, Kommunikation, Konflikte, Auswertung. Verwende eine wiederverwendbare Komponentenbibliothek (Cards, Buttons, Badges, Tables, Modals). Nutze lokalen State/Context fuer Mock-Daten. Keine externe DB noetig.

## Schritt 02: Einstieg & Incident-Kontext
Erweitere die App um einen funktionalen Incident-Auswahlscreen. Zeige eine Liste aktiver Incidents (Mock-Daten: Name, Typ, Beginn, Status). Klick auf Incident setzt den aktiven Incident-Kontext fuer alle nachfolgenden Screens. Zeige den aktiven Incident-Namen im Global-Header. Trenne Demo-Incidents klar von produktiven (Badge: DEMO vs. PRODUKTIV).

## Schritt 03: Patientenkern Teil 1
Baue den Patientenlisten-Screen fuer den aktiven Incident. Felder: Kennung (temp/offiziell), Sichtungsstufe, Status, Verbleib, Uebergabe-Info. Filter: Sichtungsstufe, Status, Verbleib. Neue Patienten anlegen mit Pflichtfeldern: Kennung, Sichtungsstufe, Status.

## Schritt 04: Patientenkern Teil 2
Erweitere den Patientendetail-Screen. Zeige: Zeitstempel Erfassung, Sichtungskategorie (= Behandlungsstart), Transportanforderung (intern/extern), Fallabschluss (Typ: RD/Entlassung/Manuell). Berechne und zeige: Zeit Erfassung->Behandlung, Zeit Behandlung->Transportanforderung, Zeit Erfassung->Fallabschluss.

## Schritt 05: Transportmodul
Baue Transportuebersicht und Transportdetail. Trenne intern/extern klar. Felder: Transportauftrag-ID, Typ, Patient, Ressource, Ziel, Status, Zeitstempel Anforderung/Zuweisung/Abfahrt/Abschluss. Filter: Typ, Status, ohne Ressource, ohne Ziel.

## Schritt 06: Kommunikation, Ressourcen & Konflikte
Baue drei getrennte Screens: Ressourcen (Typ, Status, Zuordnung, Doppelbindung), Kommunikation (Meldungen, Prioritaet, Zeitstempel), Konflikte (Typ, Schwere, Status, Aufloesung).

## Schritt 07: Produktreife & Konsistenz
Pruefe alle Screens auf: einheitliche Komponenten, konsistente Navigation, korrekte Filterlogik, Fehlerzustaende (keine Daten, Ladefehler). Stelle sicher, dass alle Pflichtfelder validiert werden.

## Schritt 08: Demo-Integration
Fuege einen Demo-Modus ein: Button "Demo-Incident erstellen" legt einen vorausgefuellten Incident mit realistischen Mock-Daten an (Patienten, Transporte, Ressourcen, Konflikte). Demo-Incidents tragen ein sichtbares DEMO-Badge auf allen Screens. Demo-Daten sind filterbar/separat anzeigbar.

## Schritt 09: Auswertung & Abschluss
Baue das Modul "Auswertung & Abschluss" mit 5 Screens:
1. Auswertungs-Dashboard: 2-Spalten-Layout, Bloecke A-F (Patient/Transport/Ressourcen/Kommunikation/Konflikte/Qualitaet), KPI-Kacheln, Sprunglinks
2. Abschluss-Check: Ampel-Header, Tabs (Patient/Transport/Ressourcen/Kommunikation/Bericht), Blocker (rot) + Warnungen (gelb) + Akzeptieren-Button
3. Berichtsvorschau: Vollbild A4-Layout, Sidebar Kap. 1-14, editierbare Freitexte vor Freigabe, Buttons Freigabe/Drucken
4. PDF-Versionen: Tabelle (Version/Datum/Rolle/Status/Download), Button PDF erzeugen
5. Nachbearbeitung: Hinweisbanner, offene Punkte, neue Version erzeugen
