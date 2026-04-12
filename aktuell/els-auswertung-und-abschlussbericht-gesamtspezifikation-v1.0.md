# ELS – Gesamtspezifikation Auswertung & Abschlussbericht V1.0

Stand: April 2026

## Zielbild
Produktionsnahes Modul zur automatisierten Auswertung und Abschlussberichterstellung fuer sanitaetsdienstliche Grosslagen-Incidents.

## Enthaltene Teilspezifikationen

### 1. Kennzahlenkatalog V1.0
- Patientenkennzahlen (inkl. Dauern und Uebergaben)
- Transportkennzahlen (intern/extern getrennt)
- Ressourcenkennzahlen (inkl. Statusverteilung je Ressourcentyp)
- Kommunikation & Konflikte
- Datenqualitaet

### 2. Definitionen
- Behandlungsstart = Eingruppierung in Sichtungskategorie
- Transportanforderung = aktives Anlegen eines Transportauftrags (intern/extern getrennt)
- Fallabschluss = je nach Verbleib:
  - Uebergabe Rettungsdienst
  - Entlassung in Veranstaltung
  - Manueller Abschluss

### 3. Kapitelstruktur Abschlussbericht (14 Kapitel)
01 Berichtskopf | 02 Lagekurzbeschreibung | 03 Zeitverlauf
04 Patientenuebersicht | 05 Uebergaben & Fallabschluesse
06 Patientenprozesszeiten | 07 Transportuebersicht
08 Transportprozesszeiten | 09 Ressourcenuebersicht
10 Kommunikation | 11 Konflikte | 12 Datenqualitaet
13 Besondere Vorkommnisse | 14 Abschluss & Freigabe

### 4. Abschlussworkflow
- Harte Blocker (sperren Freigabe)
- Weiche Warnungen (muessen bestaetigt werden)
- Abschlusszustaende: operativ aktiv / Pruefung laeuft / blockiert / freigabebereit / freigegeben / dokumentarisch abgeschlossen / nachbearbeitbar

### 5. Feldkatalog
- Auto-Pflicht / Auto-Optional / Manuell-Pflicht / Manuell-Optional je Kapitel
- Freitextregeln: nur Lagekurzbeschreibung, Besonderheiten, Freigabe

### 6. Export & Layout
- Druckansicht (Vorschau, vor/nach Freigabe)
- PDF-Export (versioniert, nach Freigabe)
- Gemeinsame Vorlage fuer beide Ausgabewege
- Format: A4 Hochformat
- Namensschema PDF: ELS_Abschlussbericht_[Incident-ID]_[Datum]_[Version].pdf

## Abhaengigkeiten
- Patientenmodul (Erfassung, Status, Verbleib)
- Transportmodul (Auftraege, Ressourcenzuordnung)
- Ressourcenmodul (Typ, Status, Konflikte)
- Kommunikationsmodul (Meldungen, Prioritaeten)
- Konfliktmodul (Typen, Status, Aufloesung)
