# ELS – Kapitelstruktur Abschlussbericht V0.1

Stand: April 2026

## 14 Pflichtkapitel (alle V1-Pflicht)

01. Berichtskopf (auto-Pflicht: Incident-Name, ID, Typ, Beginn, Ende, Dauer, Version, Erzeugungszeitpunkt, Freigabestatus)
02. Lagekurzbeschreibung (auto + Freitext-Pflicht)
03. Zeitlicher Verlauf (auto: Meilensteine des Incidents)
04. Patientenuebersicht (auto: V1-Kern Patientenkennzahlen)
05. Uebergaben & Fallabschluesse (auto: Uebergabekette + Abschlussarten)
06. Patientenprozesszeiten (auto: Dauerkennzahlen)
07. Transportuebersicht (auto: V1-Kern Transportkennzahlen)
08. Transportprozesszeiten (auto: Dauerkennzahlen intern/extern)
09. Ressourcenuebersicht (auto: V1-Kern Ressourcen + Statusmatrix)
10. Kommunikation (auto: Meldungen, priorisiert, verspaetet)
11. Konflikte (auto: gesamt, ungeloest, kritisch, je Typ)
12. Datenqualitaet (auto: offene Felder, Widersprueche, Pending-Sync)
13. Besondere Vorkommnisse (Freitext-Optional)
14. Abschluss & Freigabe (auto + Freitext-Optional, Freigabeinfo)

## Regeln
- Kennzahlen- und Freitextbereiche klar trennen
- Intern/extern bei Transporten immer getrennt
- Warn-/Qualitaetskapitel optisch hervorheben
- Bericht ueberwiegend automatisch erzeugt
- Freitext nur: Kap. 02, 13, 14
