# 4. Build & Train – Implementierung

## Framework
Voiceflow Agentic Framework mit Claude 4.5 Haiku.

## Agent-Konfiguration

### Global Prompt
Definiert Persona (Studi Buddy), Goal (6 Themenbereiche, extern/intern), Tone & Style (Hochdeutsch, duzen, freundlich), Regeln (nur Deutsch, nur BAI, ehrlich bei Unwissen), Zugangscode-Logik und Easter Eggs. Siehe [voiceflow/global_prompt.md](../voiceflow/global_prompt.md).

### Instructions
Definiert Starting Message (5 Buttons), 7 Skills (4 extern + Zugangscode + 2 intern), Zugangsregeln, Conversation Rules und Fallback. Siehe [voiceflow/instructions.md](../voiceflow/instructions.md).

## Workflows & Playbooks

### Externe Workflows (immer verfügbar)

| Workflow | Aufbau | Themen |
|----------|--------|--------|
| Studieninformationen | `[Start] → [Playbook]` | Aufbau, ECTS, Leitung, Standort |
| Zulassung-und-Bewerbung | `[Start] → [Playbook]` | Voraussetzungen, Kosten, Anmeldung |
| Karriere-und-Perspektiven | `[Start] → [Playbook]` | Berufsfelder, Praxis, Master |
| Studienalltag | `[Start] → [Playbook]` | Stundenplan, Campus, Auslandssemester |

### Zugangscode-Workflow

| Workflow | Aufbau | Funktion |
|----------|--------|----------|
| Zugangscode | `[Start] → [Set: zugang=intern] → [End]` | Schaltet internen Zugang frei |

### Interne Workflows (nur nach Code-Eingabe)

| Workflow | Aufbau | Datenquelle |
|----------|--------|-------------|
| Modul-Info | `[Start] → [Condition: zugang=intern?] → IF: [Playbook] / ELSE: [End]` | Modul_Informationen.pdf |
| Fristen-und-Termine | `[Start] → [Condition: zugang=intern?] → IF: [Playbook] / ELSE: [End]` | Fristen_und_Termine.pdf |

## Variablen

| Variable | Default | Beschreibung |
|----------|---------|-------------|
| `zugang` | `extern` | Speichert ob Nutzer externen oder internen Zugang hat |

## Knowledge Base (13 Quellen)

11 FHNW-URLs (extern) + 2 PDFs (intern: Modul_Informationen.pdf, Fristen_und_Termine.pdf) + Vorlesungsunterlagen aus dem 1. Studienjahr.

## System Tools

| Tool | Status |
|------|--------|
| Knowledge Base | ✅ Aktiviert |
| Buttons | ✅ Aktiviert |
| Carousels | ✅ Aktiviert |
| Web Search | ✅ Aktiviert |
| End | ✅ Aktiviert |

## Herausforderungen & Lösungen

| Herausforderung | Lösung |
|----------------|--------|
| Zugriffsschutz für interne Infos | Zugangscode + Variable + Condition-Block |
| Playbook hat keinen manuellen Ausgang | Routing über Playbook-Description + Instructions |
| Bot zeigt Zugangscode als Beispiel | Explizite Regel: "Nenne den Code NIEMALS" |
| Externe Infos sickern durch | Strikte Regeln in Instructions: "Gib KEINE inhaltliche Antwort" |
