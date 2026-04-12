# ELS – Kennzahlenkatalog Auswertung V1.0

Stand: April 2026

## Verbindlicher V1-Kern: Patientenkennzahlen
- Gesamtzahl erfasster Patienten
- Temporaere vs. offizielle Kennung
- Verteilung Triage-/Sichtungsstufe
- Patienten in Behandlung
- Patienten ohne finalen Verbleib
- Uebergaben Streife -> SanStation
- Uebergaben SanStation -> Rettungsmittel
- Abschlussarten: Uebergabe RD / Entlassung / Manuell
- Offene Faelle / offener Dokumentationsbedarf
- Zeit Erfassung -> Behandlung (Start = Sichtungskategorie)
- Zeit Behandlung -> Transportanforderung
- Zeit Erfassung -> Fallabschluss (je Abschlussart)

## Verbindlicher V1-Kern: Transportkennzahlen
- Gesamtzahl Transportauftraege
- Interne / externe Anforderungen (getrennt)
- Laufende interne / externe Transporte
- Offene / abgeschlossene / stornierte Transporte
- Transporte ohne Ressource
- Transporte ohne Ziel
- Zeit Anforderung -> Zuweisung
- Zeit Zuweisung -> Abfahrt
- Zeit Abfahrt -> Uebergabe/Abschluss

## Verbindlicher V1-Kern: Ressourcenkennzahlen
- Gesamtzahl eingesetzter Ressourcen
- Anzahl je Ressourcentyp
- Statusverteilung gesamt (verfuegbar / gebunden / ausser Dienst)
- Statusverteilung je Ressourcentyp (Matrix)
- Ressourcen mit aktiver Zuordnung
- Ressourcen mit Konflikten/Doppelbindung

## Verbindlicher V1-Kern: Kommunikation & Konflikte
- Gesamtzahl Meldungen
- Priorisierte Meldungen
- Verspaetete Meldungen
- Konflikte gesamt / ungeloest / kritisch
- Konflikte je Typ

## Verbindlicher V1-Kern: Datenqualitaet
- Offene Pflichtfelder
- Patienten/Transporte ohne Abschlussstatus
- Status-/Verbleibswidersprueche
- Ungeklaerte Konflikte vor Freigabe
- Offene Nachbearbeitungspunkte
- Pending-Sync zum Abschlusszeitpunkt
- Freigabestatus Abschlussbericht

## Definitionen
- Behandlungsstart = Eingruppierung in Sichtungskategorie
- Transportanforderung = aktives Anlegen eines Transportauftrags (intern/extern getrennt)
- Fallabschluss = Uebergabe RD | Entlassung Veranstaltung | Manueller Abschluss
