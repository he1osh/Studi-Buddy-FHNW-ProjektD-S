# 2. Design – Sample Dialogues

## Übersicht

Die Musterdialoge decken alle sechs Use Cases ab und zeigen den Zugangscode-Mechanismus. Basierend auf den Personas Alex (extern) und Sara (intern).

---

## Dialog 1: Externer Nutzer — Studieninfos + Zulassung (UC1 + UC4)

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **BOT** | Hey! 👋 Ich bin Studi Buddy, dein Helfer für alles rund ums BAI-Studium an der FHNW. Was kann ich für dich tun? [Buttons: 📚 Studieninfos, 🎓 Zulassung, 🚀 Karriere, 🏫 Studienalltag, 🔑 Interner Zugang] |
| 2 | **USER** | 📚 Studieninfos |
| 3 | **BOT** | Das BAI-Studium dauert 6 Semester Vollzeit (oder 8 Teilzeit) und umfasst 180 ECTS. Es gibt 5 Modulgruppen: KI, Wirtschaftsinformatik, Wirtschaft, Interdisziplinär und Anwendung & Praxis. Möchtest du wissen, wie du dich bewerben kannst? |
| 4 | **USER** | Brauche ich Programmierkenntnisse? |
| 5 | **BOT** | Nein! Für den BAI-Studiengang brauchst du keine Programmierkenntnisse. Alles wird von Grund auf aufgebaut. Möchtest du auch wissen, was das Studium kostet? |

---

## Dialog 2: Externer Nutzer wird blockiert bei interner Frage

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **USER** | Wie wird das Modul Dialogsysteme bewertet? |
| 2 | **BOT** | Modul-Details sind nur für eingeschriebene BAI-Studierende verfügbar 🔒 Gib deinen Zugangscode ein, um Infos zu Modulinhalten, Dozierenden und Bewertungen zu erhalten. Den Code erhältst du von der Studiengangleitung. |

---

## Dialog 3: Zugangscode eingeben + interne Frage (UC2)

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **USER** | 🔑 Interner Zugang |
| 2 | **BOT** | Bitte gib deinen Zugangscode ein: |
| 3 | **USER** | FHNW_BAI2026 |
| 4 | **BOT** | Zugang freigeschaltet! 🔓 Du hast jetzt Zugriff auf alle Infos — inklusive Module und Fristen. Wie kann ich dir helfen? [Buttons: 📖 Module, 📅 Fristen & Termine] |
| 5 | **USER** | Wie wird Dialogsysteme bewertet? |
| 6 | **BOT** | Das Modul Dialogsysteme & Sprachverarbeitung wird mit einem Projekt (25%) und einer mündlichen Prüfung (75%) bewertet. Dozenten: Prof. Dr. Andreas Martin und Charuta Pande. Möchtest du wissen, wann die Abgabe ist? |

---

## Dialog 4: Falscher Code

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **USER** | 🔑 Interner Zugang |
| 2 | **BOT** | Bitte gib deinen Zugangscode ein: |
| 3 | **USER** | test123 |
| 4 | **BOT** | Der Code stimmt leider nicht 🔒 Bitte versuche es nochmal oder wende dich an das Studierendensekretariat. |

---

## Dialog 5: Fristen & Termine nach Code-Eingabe (UC3)

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **USER** | Wann ist die Prüfungsperiode? |
| 2 | **BOT** | *(Antwortet basierend auf Fristen_und_Termine.pdf aus der Knowledge Base)* |

---

## Dialog 6: Studienalltag — extern verfügbar (UC5)

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **USER** | Kann ich ein Auslandssemester machen? |
| 2 | **BOT** | Ja! Die FHNW hat über 189 Partneruniversitäten weltweit. Das Auslandssemester ist optional und verlängert dein Studium nicht. Es wird über das International Office organisiert. |

---

## Dialog 7: Karriere & Perspektiven (UC6)

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **USER** | Was kann ich nach dem Studium arbeiten? |
| 2 | **BOT** | Mit dem BSc BAI stehen dir viele Wege offen: KI-Projektmanagement, Datenanalyse, Prozessoptimierung, Unternehmensberatung oder eine eigene Gründung 🚀 |

---

## Dialog 8: Easter Egg

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **USER** | 42 |
| 2 | **BOT** | Die Antwort auf alles — aber leider nicht auf deine Prüfungsfragen 😄 |

---

## Dialog 9: Fallback

| # | Sprecher | Nachricht |
|---|----------|-----------|
| 1 | **USER** | asdfghjkl |
| 2 | **BOT** | Hmm, das habe ich nicht ganz verstanden 🤔 Kannst du deine Frage anders formulieren? Ich kann dir bei Studieninfos, Zulassung, Karriere und Studienalltag helfen. Für Module und Fristen brauchst du den internen Zugangscode. |
