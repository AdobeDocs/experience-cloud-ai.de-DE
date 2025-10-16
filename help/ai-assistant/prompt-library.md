---
title: Bibliothek mit Eingabeaufforderungen des KI-Assistenten
description: Erfahren Sie mehr über die verschiedenen Arten von Eingabeaufforderungen und Eingabeaufforderungsmustern, die Sie bei der Abfrage des KI-Assistenten verwenden können.
source-git-commit: 4bb6da3fe1abee98446df62c94730274e0931493
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 3%

---

# Bibliothek mit Eingabeaufforderungen des KI-Assistenten

Lesen Sie dieses Handbuch für verschiedene Arten von Eingabeaufforderungen, die Sie im KI-Assistenten verwenden können.

## Audience Agent

Die folgenden Abschnitte enthalten Beispielaufforderungen, die Sie mit der Audience Agent verwenden können, um Ihre Zielgruppen zu untersuchen und zu analysieren. Dazu gehören Möglichkeiten, Zielgruppeneigenschaften zu untersuchen, doppelte Zielgruppen zu erkennen, Zielgruppengrößen abzurufen und signifikante Änderungen der Zielgruppengröße im Laufe der Zeit zu überwachen. Verwenden Sie diese Eingabeaufforderungen, um tiefere Einblicke zu erhalten und die Qualität Ihrer Zielgruppendaten zu erhalten.

### Konversation zur Untersuchung von Zielgruppen

- „Felder für wohlhabende Käufer anzeigen“
- „Welche Zielgruppen wurden in den letzten 30 Tagen in keiner Kampagne aktiviert oder verwendet?“
- „Listen Sie alle Zielgruppen auf, die in den letzten drei Monaten neuen Zielen zugeordnet wurden.“

### Erkennen doppelter Zielgruppen

- „Habe ich Zielgruppen mit identischen oder ähnlichen Beschreibungen?“
- „Identifizieren Sie Zielgruppen, die dieselben Regeln, aber unterschiedliche Namen haben.“
- „Zeigen Sie mir alle Zielgruppen, die dieselben Regeln, aber unterschiedliche Aktivierungsziele haben.“

### Abrufen der Zielgruppengröße

- „Wie groß ist meine Audience derzeit: „Gold-Star Members in California_f153e1“?“
- „Was ist mein größtes Publikum?“

### Erkennung signifikanter Änderungen der Zielgruppengröße

- „Welche Zielgruppen haben in der letzten Woche um mehr als 20 % zugenommen?“
- „Welche Zielgruppen sind im letzten Monat um mehr als 15 % kleiner geworden?“
- „Was ist mein am schnellsten wachsendes Publikum?“

## Data Insights Agent

Die folgenden Beispielaufforderungen können mit dem Data Insights Agent verwendet werden, um Ihre Daten zu analysieren, Trends zu identifizieren und umsetzbare Einblicke zu gewinnen.

### Datenvisualisierung

- „Zeigen Sie mir die Gewinne im September.“
- „Trend der Bestellungen im September.“
- „Umsatz nach Region im September anzeigen.“
- „Umsatzanteil nach Produktkategorie.“
- „Bestellungen nach Wochentag von Januar bis Mai.“
- „Bestellungen nach Geschlecht anzeigen, von März bis Juni.“
- „Was ist der Gewinn für alle SKUs von Februar bis Mai.“
- „Umsatz nach Shop-Name im September.“
- „Was waren meine Top 10 SKUs mit Gewinn im September?“
- „Anteil der Käufe nach Monat des Jahres.“
- „Gesamtgewinn im September.“

## Journey Agent

Die folgenden Beispielaufforderungen können mit der Journey Agent verwendet werden, um Sie bei der Analyse von Journey-Lebenszyklen, der Verwaltung von Journey-Ressourcen, dem Erhalten von Einblicken in Zielgruppen- und Journey-Beziehungen und der Erkennung von Konflikten zwischen Journey zu unterstützen. Verwenden Sie diese Eingabeaufforderungen, um Ihre Journey-Orchestrierung zu optimieren und Probleme effizient zu beheben.

### Fragen zum Journey-Lebenszyklus

- „Wann wurde {JOURNEY_NAME} veröffentlicht?“
- „Wann wurde {JOURNEY_NAME} angehalten?“
- „Alle Journey auflisten, die sich derzeit im Testmodus befinden“

### Fragen zu Journey-Ressourcen

- „Wie viele lebende Journey habe ich?“
- „Geben Sie mir eine Liste aller geplanten wiederkehrenden Journey und ihrer erwarteten Laufzeiten.“

### Erkenntnisse zu Zielgruppen und Journeys

- „Welche Zielgruppen werden in mehr als X Journey verwendet?“
- „Listen Sie alle Journey auf, die die {AUDIENCE_NAME} Zielgruppe verwenden.“

### Prompts zur Konfliktanalyse

Nutzen Sie diese Prompts, um mögliche Konflikte zwischen Journeys zu analysieren, einschließlich Überschneidungen bei der Zeitplanung und der Zielgruppe:

+++Zur Listenansicht auswählen

- „Können Sie eine umfassende Konfliktanalyse für unsere Journey-{JOURNEY_NAME} mit Konflikttyp-Informationen (Planung/Zielgruppe) mit Live-/laufenden Journey-Nachrichten durchführen?“
- „Bitte planen Sie eine Konfliktanalyse für Journey-{JOURNEY_NAME} mit Informationen zum Konflikttyp.“
- „Führen Sie eine Analyse zur Zielgruppenüberschneidung für das Journey von {JOURNEY_NAME} mit Informationen zum Konflikttyp durch.“
- „Gibt es Planungskonflikte für Journey {JOURNEY_NAME}?“
- „Konflikte bei Zielgruppenüberschneidungen für Journey {JOURNEY_NAME} anzeigen“
- „Analysieren Sie alle Konflikte für das Journey {JOURNEY_NAME} mit anderen Live-Journey.“
- „Was sind die aktuellen Konflikte bei Journey {JOURNEY_NAME}?“
- „Überprüfen, ob Journey {JOURNEY_NAME} Zielgruppenkonflikte mit anderen Journey aufweist.“
- „Prüfen Sie, ob Planungskonflikte beim Journey-{JOURNEY_NAME} vorliegen.“
- „Ich möchte mehr über alle Journey-Konflikte für {JOURNEY_NAME} erfahren.“
- „Stehen Live-Journey in Konflikt mit {JOURNEY_NAME} nach Zeitplan oder Zielgruppe?“
- „Identifizieren Sie Konflikttypen für Journey-{JOURNEY_NAME} im Vergleich zu laufenden Journey.“
- „Überschneidende Zielgruppen für Journey {JOURNEY_NAME} und andere Journey anzeigen.“
- „Überschneidungen bei der Planung zwischen Journey-{JOURNEY_NAME} und Live-Journey hervorheben.“
- „Steht die Ausführung von Journey {JOURNEY_NAME} im Konflikt mit anderen Journey?“
- „Bitte Konflikte für {JOURNEY_NAME} erkennen und auflisten.“
- „Melden Sie alle Konflikttypen für Journey {JOURNEY_NAME}.“
- „Geben Sie mir eine Konfliktaufschlüsselung (Planung und Zielgruppe) für {JOURNEY_NAME}.“
- „Gibt es {JOURNEY_NAME} Konflikte, die sich auf die Leistung auswirken können?“
- „Gibt es aktive Konflikte, die {JOURNEY_NAME} betreffen?“
- &quot;Journey auflisten, die mit {JOURNEY_NAME} in Konflikt stehen, nach Zeitplan oder Zielgruppe.“
- „Hat Journey {JOURNEY_NAME} Konflikte ausgelöst?“
- „Finden Sie potenzielle Zielgruppenkonflikte für Journey {JOURNEY_NAME}.“
- „Analysieren des Konfliktrisikos für Journey {JOURNEY_NAME}.“
- „Bereitstellung von Konfliktdiagnosen für {JOURNEY_NAME}.“

+++

## Produktsupport-Agent

Der Product Support Agent hilft Ihnen bei der Fehlerbehebung, der Erstellung von Support-Fällen und der Verfolgung des Status Ihrer Support-Tickets. Verwenden Sie die folgenden Beispielaufforderungen, um Hilfe zu erhalten.

### Hilfe zur Fehlerbehebung

- „Warum unterscheidet sich die Anzahl meiner Profile im Lizenznutzungs-Dashboard und auf der Experience Platform-Startseite?“
- „Was sind die Gründe dafür, dass eine Journey nicht ausgelöst wird?“
- „Wie erstellt Adobe Experience Platform Echtzeit-Erlebnisse?“
- „Wie werden Warnhinweise in Adobe Experience Platform konfiguriert und verwendet?“
- „Was ist die Beschränkung für Batch-Segmentierungsaufträge in Adobe Experience Platform Activation?“
- „Was ist die Grenze für den durchschnittlichen Profilreichhaltigkeit in Adobe Experience Platform Activation?“

### Erstellung von Support-Fällen

- „Erstellen Sie ein Support-Ticket.“
- „Können Sie mir beim Erstellen eines Support-Tickets helfen?“

### Fallfortschritt verfolgen

- „Was ist das Neueste zu meinem Fall E-12345?“
- „Was ist das Update für Ticket E-67890?“

