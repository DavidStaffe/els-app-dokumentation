# ELS – Abschlussworkflow & Blockerlogik V0.1

Stand: April 2026

## Workflow-Kette
1. Abschluss starten
2. Automatische Pruefung ausfuehren
3. Ergebnis in Blocker / Warnungen trennen
4. Offene Punkte anzeigen
5. Berichtsvorschau erzeugen
6. Freitexte ergaenzen
7. Bericht freigeben
8. Incident in Abschlusszustand ueberführen

## Harte Blocker (sperren Freigabe)
- Patienten ohne finalen Verbleib
- Patienten ohne gueltiges Abschlussereignis
- Offene externe Transporte
- Aktive Doppelbindung von Ressourcen
- Ungeloeste kritische Konflikte
- Fachlich relevante Pending-Sync-Ereignisse
- Fehlende Pflichtkapitel des Berichts

## Weiche Warnungen (muessen bestaetigt werden)
- Offener Dokumentationsbedarf
- Manuelle Abschluesse
- Verspaetete Meldungen
- Auffaellige Statusverteilung je Ressourcentyp
- Stornierte Transporte
- Offene Nachbearbeitungspunkte ohne Blockerstatus

## Abschlusszustaende
- operativ aktiv
- Abschlusspruefung laeuft
- blockiert
- freigabebereit mit Warnungen
- freigegeben
- dokumentarisch abgeschlossen
- nachbearbeitbar

## Rollen im Abschlussprozess
- Einsatzleitung: startet Abschluss, gibt frei
- Fuehrungsassistenz/Funk-Doku: ergaenzt Freitexte
- Transportkoordination: klaert Transport-Blocker
- Admin: kann Nachbearbeitung freischalten
