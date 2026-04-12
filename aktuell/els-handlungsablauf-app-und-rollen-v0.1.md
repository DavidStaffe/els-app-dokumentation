# ELS – Handlungsablauf App & Rollen V0.1

Stand: April 2026

## Allgemeines Ziel der App
Das ELS (Einsatzleitsystem) unterstuetzt sanitaetsdienstliche Einsatzleitung bei Grossveranstaltungen. Es ermoeglicht die strukturierte Erfassung, Steuerung und Dokumentation aller Patienten, Ressourcen, Transporte und Kommunikation waehrend eines Einsatzes. Abschliessend wird ein prueffaehiger Abschlussbericht automatisch generiert.

## Rollen

### Einsatzleiter (EL)
- Startet und beendet Incidents
- Hat Vollzugriff auf alle Module
- Gibt den Abschlussbericht frei
- Startet Demo-Incidents

### Sanitaeter / Helfer
- Erfasst Patienten und Vitalparameter
- Dokumentiert Zeitstempel (Sichtung, Behandlung, Transport)
- Fordert Transporte an
- Meldet Ressourcenkonflikte

### Dokumentar
- Pflegt Nachbearbeitungsfelder
- Bearbeitet Berichtsvorschau
- Exportiert PDF-Versionen

## Handlungsablauf je Kapitel

### Kapitel 1: Incident starten
1. EL oeffnet App, sieht Incident-Liste
2. EL legt neuen Incident an (Name, Typ, Ort, Datum)
3. Optional: Demo-Incident starten (Vordaten)
4. Incident wird im Global-Header als aktiv angezeigt

### Kapitel 2: Patientenerfassung
1. Helfer oeffnet Patientenliste
2. Neuen Patienten anlegen (Kennung auto-generiert)
3. Sichtungsstufe vergeben (S1-S4, farbkodiert)
4. Status setzen (wartend, in Behandlung, transportbereit)
5. Verbleib dokumentieren

### Kapitel 3: Patientendetail & Zeitstempel
1. Helfer oeffnet Patientendetail
2. Sichtungskategorie = Behandlungsstart-Zeitstempel
3. Transportanforderung intern/extern anlegen
4. Fallabschluss-Typ waehlen: RD-Uebergabe / Entlassung / Manuell
5. Zeitstempel werden automatisch gesetzt

### Kapitel 4: Transportsteuerung
1. EL/Helfer oeffnet Transportuebersicht
2. Intern vs. extern getrennt angezeigt
3. Status je Transport: angefordert / zugeteilt / abgeschlossen
4. Ressource zuweisen (Fahrzeug/Personal)
5. Ziel und Zeitstempel dokumentieren

### Kapitel 5: Ressourcen
1. EL oeffnet Ressourcen-Modul
2. Statusmatrix: Fahrzeuge, Personal, Material je Typ
3. Status aendern: verfuegbar / im Einsatz / ausgefallen
4. Konflikte werden automatisch markiert (rot/gelb)

### Kapitel 6: Kommunikation
1. Helfer/EL oeffnet Kommunikations-Modul
2. Meldung erstellen (Typ, Prioritaet, Inhalt)
3. Meldungen priorisiert anzeigen
4. Quittierung durch EL moeglich

### Kapitel 7: Incident abschliessen
1. EL oeffnet Abschluss-Modul
2. Abschluss-Check: Blocker (rot) und Warnungen (gelb) pruefen
3. Alle Blocker behoben -> Freigabe moeglich
4. EL gibt Incident frei

### Kapitel 8: Auswertung & Bericht
1. EL/Dokumentar oeffnet Auswertungs-Dashboard
2. KPI-Kacheln: Patienten, Transport, Ressourcen, Konflikte
3. Berichtsvorschau: 14 Kapitel, A4-Optik
4. PDF exportieren (Druckansicht / Datei)
5. Versionsliste und Freigabe-Status sichtbar

### Kapitel 9: Nachbearbeitung
1. Dokumentar oeffnet Nachbearbeitungs-Screen
2. Freitextfelder ergaenzen
3. Abschlussdokumentation speichern
4. Archivierung des Incidents
