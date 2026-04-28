<p align="center">
  <img src="StudiBuddy Logo.png" width="200">
</p>

# 🎓 Studi Buddy FHNW

> Ein intelligenter Studienberater-Chatbot für den BSc Business Artificial Intelligence (BAI) an der FHNW, entwickelt im Rahmen des Moduls *Dialogsysteme & Sprachverarbeitung* (FS 2026).

## Team

| Name | Rolle |
|------|-------|
| Helin Koyuncu | Agentaufbau und Präsentation |
| Aurelius Messmer | Definition und Dokumentation |

## Chatbot

🔗 **Laufende Instanz:** (https://creator.voiceflow.com/project/69e64d15fc8dd0daf4d19d14/agent)

## Projektübersicht

**Studi Buddy FHNW** ist ein Chatbot, der sowohl Studieninteressierten (extern) als auch aktuellen Studierenden (intern) des BSc Business Artificial Intelligence an der FHNW Fragen rund um den Studiengang beantwortet.

Der Chatbot unterscheidet zwischen zwei Zugangsstufen:
- **Extern (ohne Code):** Allgemeine Studieninfos, Zulassung & Bewerbung, Karriere & Perspektiven, Studienalltag
- **Intern (mit Zugangscode - nur von der Studiengangleitung Zugriff):** Modul-Informationen und Fristen & Termine — basierend auf echten Unterlagen des 6. Semester. Der restliche Aufbau basiert auf den Modulaufbau in der gesamten Studienzeit.

### Problem

Informationen zum BAI-Studiengang sind über FHNW-Website, Modulbeschreibungen, Moodle, Inside-Portal und PDFs verstreut. Studierende und Interessierte finden Antworten nicht schnell genug.

### Lösung

Ein 24/7 verfügbarer Studienberater-Chatbot mit zwei Zugangsstufen — offen für Interessierte, mit geschütztem Bereich für eingeschriebene Studierende.

## Use Cases

| # | Use Case | Zielgruppe | Zugang |
|---|----------|-----------|--------|
| UC1 | Allgemeine Studieninfos | Beide | Extern |
| UC2 | Modul-Informationen | Studierende | 🔒 Intern |
| UC3 | Fristen & Termine | Studierende | 🔒 Intern |
| UC4 | Zulassung & Bewerbung | Interessierte | Extern |
| UC5 | Studienalltag | Beide | Extern |
| UC6 | Karriere & Perspektiven | Beide | Extern |

## Dokumentation

| Phase | Dokument |
|-------|----------|
| **1. Define** | [Use Cases](docs/01_use_cases.md) |
| **1. Define** | [User Persona](docs/02_user_persona.md) |
| **1. Define** | [Bot Persona](docs/03_bot_persona.md) |
| **2. Design** | [Sample Dialogues](docs/04_sample_dialogues.md) |
| **3. Architect** | [Architektur](docs/05_architecture.md) |
| **4. Build & Train** | [Implementierung](docs/06_build_and_train.md) |
| **5. Release & Operate** | [Deployment & Monitoring](docs/07_deployment.md) |

## Technologie-Stack

- **Framework:** Voiceflow (Agentic Framework)
- **LLM:** Claude 4.5 Haiku
- **Knowledge Base:** über 13+ Quellen (FHNW-URLs + Modul-PDFs + Fristen-PDF)
- **Deployment:** Voiceflow Web-Chat Widget
- **Versionierung:** GitHub

## Repository-Struktur

```
Studi-Buddy-FHNW-ProjektDS/
├── README.md
├── docs/
│   ├── 01_use_cases.md
│   ├── 02_user_persona.md
│   ├── 03_bot_persona.md
│   ├── 04_sample_dialogues.md
│   ├── 05_architecture.md
│   ├── 06_build_and_train.md
│   └── 07_deployment.md
├── assets/
│   └── (Persona-Bilder, Screenshots, Diagramme)
└── voiceflow/
    ├── global_prompt.md
    ├── instructions.md
    ├── playbook_descriptions.md
    └── (studi-buddy.vf Export-Datei)
```

## Ausblick (Future Work)

- Skalierung auf alle FHNW-Studiengänge (z.B. neues Tech-Gebäude am Dreispitz) oder auf BAI Fokus
- Authentifizierung über Inside-Portal für personalisierten Zugang
- Mehrsprachigkeit (Englisch, Französisch)
- Integration mit Moodle-API für Echtzeit-Fristen

---

*FHNW University of Applied Sciences and Arts Northwestern Switzerland – School of Business, Olten*
*Modul: Dialogsysteme & Sprachverarbeitung – Prof. Dr. Andreas Martin & Charuta Pande*
