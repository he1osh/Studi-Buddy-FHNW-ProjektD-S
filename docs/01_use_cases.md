# 1. Define – Use Cases

## Übersicht

Der Studi Buddy FHNW bedient zwei Zielgruppen: externe Studieninteressierte und interne (aktuelle) Studierende. Interne Inhalte (Module, Fristen) sind durch einen Zugangscode geschützt. Insgesamt werden sechs Use Cases abgedeckt.

---

## Externe Use Cases (ohne Code verfügbar)

### UC1: Allgemeine Studienprogramm-Informationen
| Aspekt | Beschreibung |
|--------|-------------|
| **Zielgruppe** | Extern + Intern |
| **Ziel** | Schnelle Antworten zu Studienaufbau, ECTS, Standort, Studienleitung |

**Typische Fragen:** "Wie ist das BAI-Studium aufgebaut?", "Wie viele ECTS brauche ich?", "Wer leitet den Studiengang?"

### UC4: Zulassung & Bewerbung
| Aspekt | Beschreibung |
|--------|-------------|
| **Zielgruppe** | Extern |
| **Ziel** | Alle Fragen zur Bewerbung und Zulassung klären |

**Typische Fragen:** "Brauche ich Programmierkenntnisse?", "Was kostet das Studium?", "Kann ich mit einer Gymnasialmatura studieren?"

### UC5: Studienalltag & Organisation
| Aspekt | Beschreibung |
|--------|-------------|
| **Zielgruppe** | Extern + Intern |
| **Ziel** | Schnelle Antworten zu Stundenplan, Campus, Auslandssemester, Stipendien |

**Typische Fragen:** "Wo ist der Campus?", "Kann ich ein Auslandssemester machen?", "Gibt es Stipendien?"

### UC6: Karriere & Perspektiven
| Aspekt | Beschreibung |
|--------|-------------|
| **Zielgruppe** | Extern + Intern |
| **Ziel** | Motivation und klare Infos zu Karrierewegen und Praxisbezug |

**Typische Fragen:** "Was kann ich nach dem Studium arbeiten?", "Gibt es Praxisprojekte?"

---

## Interne Use Cases (nur mit Zugangscode)

### UC2: Modul-spezifische Informationen 🔒
| Aspekt | Beschreibung |
|--------|-------------|
| **Zielgruppe** | Intern (aktuelle Studierende) |
| **Zugang** | Nur nach Eingabe des Zugangscodes |
| **Datenquelle** | Modul_Informationen.pdf + Vorlesungsunterlagen in der Knowledge Base |
| **Ziel** | Detailinformationen zu einzelnen Modulen des 1. Studienjahres |

**Typische Fragen:** "Was lerne ich in Dialogsysteme?", "Wer unterrichtet Statistik?", "Wie wird das Modul bewertet?"

### UC3: Fristen und Termine 🔒
| Aspekt | Beschreibung |
|--------|-------------|
| **Zielgruppe** | Intern (aktuelle Studierende) |
| **Zugang** | Nur nach Eingabe des Zugangscodes |
| **Datenquelle** | Fristen_und_Termine.pdf in der Knowledge Base |
| **Ziel** | Schneller Zugriff auf Prüfungstermine und Abgabefristen |

**Typische Fragen:** "Wann ist die Prüfungsperiode?", "Wann muss ich die Projektarbeit abgeben?"

---

## Zugangscode-Konzept

Externe Nutzer sehen beim Start 5 Buttons (4 externe Themen + "🔑 Interner Zugang"). Nach Eingabe des korrekten Zugangscodes werden die internen Themen (📖 Module, 📅 Fristen) freigeschaltet.

Dieses Konzept ermöglicht es der Studiengangleitung, den Zugangscode an eingeschriebene Studierende zu verteilen, während Interessierte trotzdem alle relevanten Infos zur Studienorientierung erhalten.

---

## Abgrenzung (Out of Scope)

Der Chatbot beantwortet **nicht:** individuelle Noten, Fragen zu anderen Studiengängen, administrative Prozesse (Anmeldung/Exmatrikulation), persönliche Beratung.
