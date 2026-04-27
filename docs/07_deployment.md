# 5. Release & Operate – Deployment & Monitoring

## Deployment

### Umgebungen
| Umgebung | Zweck |
|----------|-------|
| Development | Entwicklung und Testing |
| Production | Finale Version für Endnutzer |

### Widget-Link
🔗 **Laufende Instanz:** *[Link hier einfügen nach Publish]*

## Testing

| # | Testfall | Erwartung | Ergebnis |
|---|---------|-----------|---------|
| 1 | "Hallo" | Begrüssung mit 5 Buttons | *[Screenshot]* |
| 2 | "Wie ist das Studium aufgebaut?" | Antwort (extern) | *[Screenshot]* |
| 3 | "Wie wird Dialogsysteme bewertet?" | Blockiert: Zugangscode nötig 🔒 | *[Screenshot]* |
| 4 | "Was kostet das Studium?" | Antwort (extern) | *[Screenshot]* |
| 5 | "FHNW_BAI2026" | Zugang freigeschaltet 🔓 | *[Screenshot]* |
| 6 | "Wie wird Dialogsysteme bewertet?" | Antwort mit Modulinfos (intern) | *[Screenshot]* |
| 7 | "Wann ist die Prüfung?" | Antwort aus Fristen-PDF (intern) | *[Screenshot]* |
| 8 | "42" | Easter Egg | *[Screenshot]* |
| 9 | "asdfghjkl" | Fallback-Nachricht | *[Screenshot]* |

## Monitoring

### Voiceflow Analytics
| Metrik | Beschreibung |
|--------|-------------|
| Total Chats | Anzahl Gespräche |
| Total Interactions | Anzahl Nachrichten |
| Unique Users | Verschiedene Nutzer |
| Latency | Antwortzeit |

### KPIs
| KPI | Ziel |
|-----|------|
| Containment Rate | > 70% |
| Goal Completion Rate | > 80% |
| Fallback Rate | < 15% |

## Bekannte Limitationen
| Limitation | Mögliche Lösung |
|-----------|----------------|
| Nur Deutsch | Mehrsprachigkeit (Future Work) |
| Zugangscode nicht sicher | Inside-Portal-Authentifizierung |
| Nur Module des 1. Jahres | Weitere PDFs hochladen |
| Knowledge Base Aktualität | Updates beim Semesterwechsel |

## Ausblick
- Skalierung auf alle FHNW-Studiengänge
- Authentifizierung über Inside-Portal
- Mehrsprachigkeit
- Moodle-API-Integration
