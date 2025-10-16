---
title: Journey Analyze Agent SKILL Overview and User Guide
description: Umfassender Leitfaden zur Analysefunktion in Journey Agent, die Benutzende dabei unterstützt, Marketing-Journeys zu analysieren, Probleme zu erkennen, Erkenntnisse zu gewinnen und Kundeninteraktionen zu optimieren.
solution: Journey Optimizer
product: journey optimizer
role: Admin,User,Developer,Leader
source-git-commit: 26b579471b591d3c436f4275d07303d297e0fbf8
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 38%

---


# Journey Analyze Agent: Kompetenzübersicht und Benutzerhandbuch

## Überblick

Journey Agent ermöglicht es Journey Optimizer-Anwendern, Journey mithilfe einer natürlichen Sprachschnittstelle zu analysieren und zu optimieren. Mit Journey Agent können Anwendende Zeitplankonflikte und/oder Zielgruppenkonflikte schnell identifizieren und lösen, Punkte der Benutzerkündigung in einer Journey erkennen und Einblicke oder Empfehlungen liefern. Er unterstützt Marketing-Fachleute dabei, datengestützte Entscheidungen zu treffen, die Kundeninteraktion zu verbessern und die Journey-Orchestrierung zu optimieren.

Erfahren Sie mehr und entdecken Sie den Agenten auf einen Blick in dieser [Übersicht](https://experienceleague.adobe.com/de/slides/journey-agent-overview).

>[!AVAILABILITY]
>
>Die Journey Agent steht allen Kunden zur Verfügung, die Zugriff auf den KI-Assistenten haben. Sie benötigen jedoch die folgenden Berechtigungen, um die Funktionen von Journey Agent vollständig nutzen zu können:
>
>**Journey anzeigen**: Mit dieser Berechtigung können Sie Einblicke in die Journey direkt im KI-Assistenten anzeigen.
>
>**Journey verwalten**: Mit der Berechtigung „Bis“ können Sie neue Journeys direkt im KI-Assistenten erstellen.
>
>**Segmente anzeigen**: Mit dieser Berechtigung können Sie Einblicke in die Zielgruppen direkt im KI-Assistenten anzeigen.
>
>**Segmente verwalten**: Mit der Berechtigung „Bis“ können Sie neue Zielgruppen direkt im KI-Assistenten erstellen.

![Beispiel für AJO Agent](./images/ajo-agent/ajo-agent-sample.png)

## Anwendungsfälle

### Wichtige Anwendungsfälle für die Analysefunktion von Journey Agent

Die Analysefunktion von Journey Agent bietet vielfältige Möglichkeiten zur Optimierung von Marketing-Maßnahmen:

1. **Journey-Fallout-Analyse**

   - Erfahren Sie, wo und warum Kundinnen und Kunden während einer Journey abspringen.
   - Erkennen Sie Muster im Kundenverhalten, die zu einem Rückgang der Interaktion führen.
   - Nutzen Sie diese Erkenntnisse, um das Journey-Design zu verfeinern und die Kundenbindung zu verbessern.

1. **Analyse der Zielgruppenüberschneidung in Journeys**

   - Analysieren Sie Zielgruppenüberschneidungen über mehrere Journeys hinweg.
   - Vermeiden Sie Zielgruppenermüdung, die durch übermäßiges Targeting verursacht wird.
   - Optimieren Sie die Segmentierung, um eine ausgewogene Interaktion sicherzustellen.

1. **Analyse von Zeitplanüberschneidungen in Journeys**

   - Erkennen Sie Überschneidungen in den Zeitplänen von Journeys, die sich an dieselbe Zielgruppe richten.
   - Vermeiden Sie übermäßige Kommunikation und verbessern Sie die Effizienz Ihrer Zeitplanung.
   - Maximieren Sie die Wirkung auf Ihre Zielgruppe, indem Sie sicherstellen, dass die Journeys zu optimalen Zeiten geschaltet werden.

1. **Betriebliche Erkenntnisse**

   - Prompt-basierte Journey-Einblicke - Erhalten Sie operative Einblicke über Journey, d. h. „Zeige mir alle Live-Journey&quot;.

Bei jeder dieser Analysen erkennt der Agent nicht nur Probleme, sondern gibt auch **umsetzbare Empfehlungen zur Lösung dieser Probleme**.


## Leistungsumfang

### **Unterstützte Funktionen**

Die folgenden Möglichkeiten werden von der Analysefunktion von Journey Agent unterstützt:

- **Reaktive Abfragen**: Mit dieser Funktion können Benutzende gezielte Fragen zur Leistung der Journey, zur Nutzung durch die Zielgruppe und zu Zeitplankonflikten stellen.
- **Integration mit anderen Agents**: Zusammenarbeit mit Audience Agent und Data Insights Agent für eine tiefergehende Analyse.
- **Struktur der Agent-**: Argumentation (Erläuterung der Logik), Zusammenfassung der Analyse (Hervorhebung der Schlüsselpunkte), Problemdetails (Beschreibung des Problems) und Empfehlung (Vorschlag der nächsten Schritte).

### **Nicht unterstützte Funktionen**

Die folgenden Möglichkeiten werden derzeit nicht unterstützt:

- **Automatisierte Erstellung von Journeys**
- **Echtzeit-Anomalieerkennung**
- **Kanalüberschneidungen**
- **Analyse des Journey-Eintritts**
- **Analyse technischer Probleme**
- **Analyse der Kontaktermüdung**

## Beispiel-Prompts

### Allgemeine Prompts für die Journey-Analyse

Im Folgenden finden Sie Beispiele für praktische Prompts, die Benutzende verwenden können, um ihre Journeys zu erkunden, zu überwachen und Fehler zu beheben.

### Fragen zum Journey-Lebenszyklus

- „Wann wurde [Journey-Name] veröffentlicht?“
- „Wann wurde [Journey-Name] angehalten?“
- „Alle Journey auflisten, die sich derzeit im Testmodus befinden“

### Fragen zu Journey-Ressourcen

- „Wie viele lebende Journey habe ich?“
- „Geben Sie mir eine Liste aller geplanten wiederkehrenden Journey und ihrer erwarteten Laufzeiten.“

### Erkenntnisse zu Zielgruppen und Journeys

- „Welche Zielgruppen werden in mehr als X Journey verwendet?“
- „Listen Sie alle Journey mit der [Zielgruppenname] Zielgruppe auf.“

### Fallout-Analyse

- „Ich möchte den Fallout nach Knoten für das Journey der Kampagne vom 4. Juli analysieren.“
- „Führen Sie eine Fallout-Analyse für das Journey der Kampagne vom 4. Juli durch.“
- „Was bedeutet Profilverlust im Verlauf des Journey der Kampagne vom 4. Juli?“
- „Anzeigen, wo Benutzer in der Journey der Kampagne vom 4. Juli abbrechen.“

### Prompts zur Konfliktanalyse

Nutzen Sie diese Prompts, um mögliche Konflikte zwischen Journeys zu analysieren, einschließlich Überschneidungen bei der Zeitplanung und der Zielgruppe:

- „Können Sie eine umfassende Konfliktanalyse für unsere Journey [Journey-Name] mit Informationen zum Konflikttyp (Planung/Zielgruppe) mit Live-/laufenden Journey-Dateien durchführen?“
- „Bitte planen Sie eine Konfliktanalyse für Journey [Journey-Name] mit Informationen zum Konflikttyp.“
- „Führen Sie eine Analyse zur Zielgruppenüberschneidung für das Journey von [Journey-] mit Informationen zum Konflikttyp durch.“
- „Gibt es Planungskonflikte für Journey [Journey-Name]?“
- „Konflikte bei Zielgruppenüberschneidungen für Journey [Journey-Name anzeigen]&quot;
- „Analysieren Sie alle Konflikte für das Journey [Journey-Name] mit anderen Live-Journey.“
- „Was sind die aktuellen Konflikte beim Journey [Journey-Name]?“
- „Überprüfen, ob der Journey [Journey-Name] Zielgruppenkonflikte mit anderen Journey aufweist.“
- „Prüfen Sie, ob Planungskonflikte beim Journey [Journey-Name] vorliegen.“
- „Ich möchte mehr über alle Journey-Konflikte für [Journey-Name] erfahren.“
- „Kollidieren Live-Journey mit [Journey-Name] nach Zeitplan oder Zielgruppe?“
- „Identifizieren Sie Konflikttypen für Journey [Journey-Name] im Vergleich zu laufenden Journey.“
- „Überschneidende Zielgruppen für das Journey von [Journey-Name] und anderen Journey anzeigen.“
- „Zeitplanüberschneidungen zwischen Journey [Journey-Name] und Live-Journey hervorheben.“
- „Steht die Ausführung von Journey [Journey]Name&rbrace; im Konflikt mit einer anderen Journey?“
- „Bitte Konflikte für [Journey-Name&rbrace; erkennen und ].“
- „Melden Sie alle Konflikttypen für das Journey [Journey-Name].“
- „Geben Sie mir eine Konfliktaufschlüsselung (Planung und Zielgruppe) für [Journey-Name].“
- „Gibt es für [Journey-] Konflikte, die sich auf die Leistung auswirken können?“
- „Gibt es aktive Konflikte, die sich auf [Journey-Name] auswirken?“
- &quot;Journey auflisten, die mit [Journey-Name] in Konflikt stehen, nach Zeitplan oder Zielgruppe.“
- „Hat Journey [Journey-Name] Konflikte ausgelöst?“
- „Finden Sie potenzielle Zielgruppenkonflikte für Journey [Journey-Name].“
- „Analysieren des Konfliktrisikos für Journey [Journey-Name].“
- „Stellen Sie eine Konfliktdiagnose für [Journey-Name] bereit.“

## Best Practices

### Best Practices für das Prompting

Um die Effektivität der Analysefunktion von Journey Agent zu maximieren, sollten Sie diese Best Practices befolgen:

1. **Seien Sie präzise**: Verwenden Sie klare und prägnante Prompts, um zielgerichtete Erkenntnisse zu erhalten. Anstatt beispielsweise zu fragen: „Was sind meine Journey?“, geben Sie „Alle im letzten Monat erstellten Journey auflisten“ an.
1. **Kombinieren Sie Erkenntnisse**: Integrieren Sie Erkenntnisse aus Audience Agent und Data Insights Agent, um eine ganzheitliche Sicht auf die Leistung der Journey zu erhalten.
1. **Iterative Verfeinerung**: Nutzen Sie Analysen zu Abbrüchen und Überschneidungen, um das Journey-Design und die Zeitplanung iterativ zu verfeinern.

### Best Practices beim Setup

- **Definieren Sie klare Ziele**: Legen Sie vor der Analyse von Journeys klare Ziele fest (z. B. Verbesserung der Kundenbindung, Steigerung der Konversionsrate).
- **Überwachen Sie regelmäßig**: Planen Sie regelmäßige Überprüfungen der Journey-Leistung, um Trends und Anomalien zu erkennen.
- **Optimieren Sie die Segmentierung**: Stellen Sie sicher, dass die Zielgruppensegmentierung ausgewogen ist, um Ermüdungserscheinungen zu vermeiden und Interaktionen zu maximieren.

