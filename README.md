# ELS App – Dokumentation

> Einsatzleitsystem für sanitätsdienstliche Großlagen
> Stand: April 2026 | Dashboard-Version: V51

---

## Struktur

```
els-app-dokumentation/
├── aktuell/          # Aktuelle Artefakte (neueste Versionen)
├── archiv/           # Ältere Versionen als Referenz
└── README.md
```

---

## Aktuelle Artefakte

### Dashboard
- `els-dashboard-master-v51.html` – Master-Dashboard mit Checkliste und Statustracking

### Konzept & Spezifikation
- `els-auswertung-und-abschlussbericht-gesamtspezifikation-v1.0.md`
- `els-auswertung-abschlussbericht-konzept-v0.1.md`
- `els-auswertung-kennzahlenkatalog-v1.0.md`
- `els-abschlussbericht-kapitelstruktur-v0.1.md`
- `els-abschlussworkflow-blocker-v0.1.md`
- `els-abschlussbericht-feldkatalog-v0.1.md`
- `els-abschlussbericht-export-und-layout-v0.1.md`

### UX & Screens
- `els-auswertung-abschlussbericht-screens-und-ux-v0.1.md`
- `els-figma-komponenten-briefing-v0.1.md`

### Prompts
- `els-paste-ready-prompts-bolt-v3.md`
- `els-paste-ready-prompts-emergent-v3.md`
- `els-masterprompt-bolt-v0.1.md`
- `els-masterprompt-emergent-v0.1.md`

### Ausführungsstrategien
- `els-ausfuehrungsstrategie-bolt-v1.md`
- `els-ausfuehrungsstrategie-emergent-v1.md`
- `els-ausfuehrungsstrategie-auswertung-abschlussbericht-bolt-v0.1.md`
- `els-ausfuehrungsstrategie-auswertung-abschlussbericht-emergent-v0.1.md`

### Handlungsabläufe & Rollen
- `els-handlungsablauf-app-und-rollen-v0.1.md`

---

## Archiv
Alle älteren Versionen liegen unter `/archiv/` und dienen als Referenz.
Sie werden nicht mehr aktiv gepflegt, aber bewusst nicht gelöscht.

---

## Hinweise
- Produktivsystem-Ziel: arbeitsfähige App, kein Demo-Only-Prototyp
- Demo-Incidents: integrierter Zusatzmodus, klar getrennt vom Produktivbetrieb
- Tools: Bolt.New (funktional/strukturell) + Emergent (visuell/produktnah)
