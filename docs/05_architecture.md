# 3. Architect – Architektur & Informationsbedarf

## 1. Data Need

| Use Case | Datenquelle | Zugang |
|----------|-------------|--------|
| UC1: Studieninfos | FHNW-URLs in Knowledge Base | Extern |
| UC2: Module | Modul_Informationen.pdf + Vorlesungsunterlagen | 🔒 Intern |
| UC3: Fristen | Fristen_und_Termine.pdf | 🔒 Intern |
| UC4: Zulassung | FHNW-URLs in Knowledge Base | Extern |
| UC5: Studienalltag | FHNW-URLs in Knowledge Base | Extern |
| UC6: Karriere | FHNW-URLs in Knowledge Base | Extern |

### Knowledge Base (13 Quellen)

**URLs (11):**
fhnw.ch/de/studium/wirtschaft/bai, bachelor-in-business-artificial-intelligence, modulbeschreibungen.webapps.fhnw.ch, starter-guide-business/dein-semester, studium/wirtschaft/bachelor, plattformen/bai/studium, rund-ums-studium, info-anlaesse-bachelor, internationales/outgoing-studierende, modulgruppe-kuenstliche-intelligenz, flyer-studiengaenge-bsc.pdf

**PDFs (2):**
Modul_Informationen.pdf (intern), Fristen_und_Termine.pdf (intern)

## 2. Channel / UI

**Primär:** Voiceflow Web-Chat Widget (einbettbar, mobile-optimiert, kein Login nötig)

## 3. Framework

**Voiceflow Agentic Framework** mit Claude 4.5 Haiku als LLM. Gewählt wegen: Low-Code, integrierte Knowledge Base, LLM-basierte NLU, Web-Widget mit einem Klick.

## 4. Bot-Architektur

```
┌──────────┐     ┌─────────────────────────────────┐     ┌─────────────────┐
│  Nutzer   │     │      Voiceflow Agent            │     │  Knowledge Base │
│          │────▶│                                 │     │                 │
│          │     │  Global Prompt + Instructions   │     │  11 URLs        │
│          │◀────│         ↓                       │────▶│  2 PDFs (intern)│
└──────────┘     │  ┌───────────────────────────┐  │     └─────────────────┘
                 │  │  Externe Workflows (4)     │  │
  Web-Chat       │  │  Studieninfos             │  │
  Widget         │  │  Zulassung & Bewerbung    │  │
                 │  │  Karriere & Perspektiven  │  │
                 │  │  Studienalltag            │  │
                 │  ├───────────────────────────┤  │
                 │  │  🔒 Zugangscode-Workflow   │  │
                 │  │  Set: zugang = intern     │  │
                 │  ├───────────────────────────┤  │
                 │  │  🔒 Interne Workflows (2)  │  │
                 │  │  Condition → Modul-Info   │  │
                 │  │  Condition → Fristen      │  │
                 │  └───────────────────────────┘  │
                 └─────────────────────────────────┘
```

### Zugangscode-Architektur

```
Externer Nutzer:
[Start] → [4 Buttons: Studieninfos, Zulassung, Karriere, Studienalltag + 🔑 Interner Zugang]
                                                                              ↓
                                                                    [Code eingeben]
                                                                         ↓
                                                              [Set: zugang = intern]
                                                                         ↓
                                                              [2 Buttons: Module, Fristen]

Interne Workflows:
[Start] → [Condition: zugang = intern?]
              ├── IF → [Playbook mit KB-Zugriff]
              └── ELSE → [End: "Zugangscode nötig 🔒"]
```

## Ethische Aspekte

| Aspekt | Massnahme |
|--------|-----------|
| Transparenz | Bot stellt sich klar als KI vor |
| Datenschutz | Zugangscode schützt interne Infos |
| Bias | Neutrale, sachliche Antworten |
| Halluzination | Knowledge Base als primäre Quelle |
| Sicherheit | Bot nennt den Zugangscode nie in Antworten |
