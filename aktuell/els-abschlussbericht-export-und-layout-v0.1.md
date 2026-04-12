# ELS – Export & Layout Abschlussbericht V0.1

Stand: April 2026

## Ausgabewege
- Druckansicht (in-App, Vorschau vor/nach Freigabe, Druckdialog)
- PDF-Export (versioniert, nach Freigabe, archivierungsfaehig)

## Gemeinsame Layoutregeln
- Format: A4 Hochformat
- Kapitelreihenfolge: 01-14 (identisch in beiden Ausgaben)
- Klare Kapitelueberschriften
- Kennzahlen- und Freitextbereiche visuell getrennt
- Warn-/Qualitaetskapitel hervorgehoben
- Intern/extern bei Transporten immer getrennt dargestellt
- Statusmatrix Ressourcen je Typ sichtbar

## Druckansicht
- Aufruf: Button in Berichtsvorschau
- Verfuegbar: vor und nach Freigabe
- Zweck: Sichtpruefung, interner Gebrauch, Sofortausdruck
- Freitextfelder: editierbar vor Freigabe, read-only danach

## PDF-Export
- Aufruf: nach Freigabe aus Versionsliste
- Versioniert (erhoeht sich bei Nachbearbeitung)
- Traegt Freigabestatus sichtbar
- Namensschema: ELS_Abschlussbericht_[Incident-ID]_[Datum]_[Version].pdf
- Zweck: Ablage, Versand, Nachverfolgung, Archiv

## Technische Leitlinie
- Beide Ausgaben aus derselben Berichtsvorlage
- Keine doppelte fachliche Pflege zweier Versionen
- Unterschiede nur in: Layout-Rendering, Metadaten, Finalisierungslogik
