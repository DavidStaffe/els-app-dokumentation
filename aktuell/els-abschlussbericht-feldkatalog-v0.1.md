# ELS – Feldkatalog Abschlussbericht V0.1

Stand: April 2026

## Feldattribute
Jedes Feld hat: Feld-ID | Kapitelzuordnung | Pflicht/optional | automatisch/manuell/gemischt | Datenquelle | Sichtbarkeit je Rolle | Blockerrelevanz | Exportrelevanz

## Kap. 01 Berichtskopf
- Incident-Name: auto-Pflicht
- Incident-ID: auto-Pflicht
- Incident-Typ: auto-Pflicht
- Beginn/Ende/Dauer: auto-Pflicht
- Berichtsversion: auto-Pflicht
- Erzeugungszeitpunkt: auto-Pflicht
- Freigabestatus: auto-Pflicht

## Kap. 02 Lagekurzbeschreibung
- Automatische Kurzinfo (Typ, Dauer, Patienten): auto-Pflicht
- Freitext Lagekurzbeschreibung: manuell-Pflicht (max. 500 Zeichen)

## Kap. 03-12 Kennzahlenkapitel
- Alle Kennzahlen gemaess V1-Kern: auto-Pflicht
- Fehlende Werte: als 'nicht verfuegbar' markiert
- Keine manuellen Eingaben in Kennzahlenkapiteln

## Kap. 13 Besondere Vorkommnisse
- Freitext: manuell-optional (max. 1000 Zeichen)

## Kap. 14 Abschluss & Freigabe
- Freigabedatum/-zeit: auto-Pflicht
- Freigebende Rolle: auto-Pflicht
- Freigabekommentar: manuell-optional (max. 300 Zeichen)

## Freitextregeln V1
- Freitext nur in Kap. 02, 13, 14
- Keine freien Ergaenzungen in Kennzahlenkapiteln
- Vor Freigabe editierbar fuer berechtigte Rollen
- Nach Freigabe read-only
