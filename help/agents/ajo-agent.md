---
title: Übersicht und Benutzerhandbuch zu Journey Agent
description: Eine umfassende Anleitung für Journey Agent, die es den Benutzenden ermöglicht, Marketing-Journey über eine natürliche Sprachschnittstelle in Journey Optimizer zu erstellen, zu analysieren und zu optimieren.
solution: Journey Optimizer
product: journey optimizer
role: Admin,User,Developer,Leader
source-git-commit: 229d349d971ffaba3f2f2fb989e363d96a8d7a70
workflow-type: tm+mt
source-wordcount: '2147'
ht-degree: 18%

---


# Journey Agent: Übersicht und Benutzerhandbuch

## Einführung in Journey Agent in Adobe Journey Optimizer

Journey Agent ermöglicht es Journey Optimizer-Anwendern, Marketing-Journey über eine natürliche Sprachschnittstelle zu erstellen, zu analysieren und zu optimieren. Mit Journey Agent können Marketing-Fachleute Journeys schnell erstellen, Zeitplan- oder Zielgruppenkonflikte erkennen und beheben, die Leistung und Absprungpunkte analysieren und besonders erfolgreiche Journeys identifizieren, um sie in künftigen Kampagnen zu reproduzieren. Es ermöglicht Anwendern, datengesteuerte Entscheidungen zu treffen, die Kundeninteraktion zu verbessern und die Journey-Orchestrierung zu optimieren.

Journey Agent besteht aus zwei Hauptqualifikationen:
- **Journey-Erstellungsagent**: Marketing-Journey über natürliche Sprachaufforderungen erstellen und konfigurieren
- **Journey Analyze Agent**: Analysieren Sie Journey, erkennen Sie Probleme, entdecken Sie Erkenntnisse und optimieren Sie die Kundeninteraktion

## Journey Create Agent: Skill Overview and User Guide

## Überblick

Mit dem Journey Create Agent können Journey Optimizer-Benutzer Marketing-Journey über eine natürliche Sprachschnittstelle erstellen und konfigurieren. Mit Journey Create Agent können Anwender schnell Journey erstellen, indem sie ihre Anforderungen in Gesprächsaufforderungen beschreiben. Der Agent optimiert die Journey-Erstellung, sodass sich Marketing-Experten auf die Strategie und nicht auf die technische Konfiguration konzentrieren können.

>[!AVAILABILITY]
>
>Der Journey Create Agent steht allen Kunden zur Verfügung, die Zugriff auf den KI-Assistenten haben. Sie benötigen jedoch die folgenden Berechtigungen, um die Funktionen von Journey Create Agent vollständig nutzen zu können:
>
>**Journey** verwalten: Mit dieser Berechtigung können Sie neue Journeys direkt im KI-Assistenten erstellen.
>
>**Anzeigen von Journey-Ereignissen, Datenquellen und Aktionen**: Diese Berechtigung stellt sicher, dass der KI-Assistent Journey-Ereignisse und benutzerdefinierte Aktionen durchsuchen kann.
>
>**Segmente anzeigen**: Diese Berechtigung stellt sicher, dass der KI-Assistent beim Erstellen einer Journey nach Zielgruppensegmenten suchen kann.
>
>**Segmente verwalten**: Mit dieser Berechtigung können Sie neue Zielgruppen direkt im KI-Assistenten erstellen.

## Anwendungsfälle

### Häufige Anwendungsfälle für Journey Create Agent

Die Journey Create Agent-Kenntnisse bieten Funktionen, die genutzt werden können, um die Marketing-Ausführung zu beschleunigen:

1. **Ereignisgesteuerte Journey-Erstellung**

   - Erstellen Sie Journey, die basierend auf bestimmten Kundenereignissen aktiviert werden.
   - Entwerfen Sie automatisierte Antworten auf Kundenaktionen in Echtzeit.
   - Erstellen personalisierter Kommunikationsflüsse basierend auf dem Kundenverhalten.

1. **Zielgruppen-orientierte Journey-Erstellung**

   - Erstellen Sie Journey für bestimmte Zielgruppensegmente.
   - Entwerfen Sie mehrstufige Kommunikationssequenzen mit strategischem Timing.

1. **Erstellung von durch Geschäftsereignisse ausgelösten Journey**

   - Erstellen Sie Journey, die basierend auf einem bestimmten Geschäftsereignis aktiviert werden und eine bestimmte Zielgruppe ansprechen (z. B. „Produkt wieder auf Lager“ oder „Spielwertänderung„).
   - Erstellen personalisierter Kommunikationsflüsse basierend auf dem Kundenverhalten.

1. **Erstellung von Journey zur Zielgruppenqualifizierung**

   - Erstellen Sie Journey, die aktiviert werden, wenn Profile in eine Zielgruppensegmentdefinition eintreten oder diese verlassen.
   - Erstellen personalisierter Kommunikationsflüsse basierend auf dem Kundenverhalten.

1. **Bedingte Journey-Flüsse**

   - Erstellen Sie Entscheidungszweige basierend auf Kundenattributen.
   - Entwerfen Sie Split-Pfade, die sich an die Kundenpräferenzen anpassen.

Für jeden dieser Anwendungsfälle übersetzt der Agent Anforderungen an natürliche Sprachen in strukturierte Journey-Konfigurationen.

## In Umfang und außerhalb des Umfangs Kenntnisse

### **Im Umfang**

Die folgenden Funktionen werden vom Journey Create Agent unterstützt:

- **Erstellung von Journey in natürlicher Sprache**: Ermöglicht Benutzern, den Journey-Fluss in einer Konversationssprache zu beschreiben.
- **Ereignisbasierte und zielgruppenbasierte Journey**: Unterstützt sowohl Trigger-basierte als auch geplante Journey-Typen sowie die Qualifizierung von Geschäftsereignissen und Zielgruppen.
- **Bedingte Logik**: Verarbeitet Entscheidungsaufteilungen und Verzweigungen basierend auf Kundenattributen.
- **Multi-Channel-Messaging**: Unterstützt Push-Benachrichtigungen, E-Mail- und SMS-Kanäle.
- **Journey-Planung**: Konfiguriert Startdaten und -zeiten für geplante Journeys.

### **Außerhalb des Bereichs**

Die folgenden Möglichkeiten werden derzeit nicht unterstützt:

- **Erweiterte Journey-**
- **Echtzeit-Journey-Änderungen**
- **Cross-Journey-Orchestrierung**
- **A/B-Testkonfiguration**
- **Komplexe Datenumwandlungen**
- **Erstellung von Inhaltsnachrichten**

## Eingabeaufforderungen im Beispiel

### Häufige Eingabeaufforderungen für die Journey-Erstellung

Im Folgenden finden Sie Beispiele für wertvolle Eingabeaufforderungen, die Benutzende zum Erstellen von Journey verwenden können.

### Ereignisgesteuerte Journey-Eingabeaufforderungen

**Besuch speichern Journey:**

„Erstellen Sie eine Journey, die gestartet wird, wenn ein Benutzer meinen Speicherort eingibt. Senden Sie eine Push-Benachrichtigung, um Benutzer im Store willkommen zu heißen. Warten Sie 2 Tage und überprüfen Sie, ob der Benutzer über eine gültige E-Mail-Adresse verfügt. Wenn der Benutzer über eine gültige E-Mail-Adresse verfügt, senden Sie eine E-Mail-Umfrage, um ihn nach seinem Store-Erlebnis zu fragen. Wenn der Benutzer keine gültige E-Mail-Adresse hat, senden Sie eine Push-Benachrichtigung, um ihn zur Registrierung aufzufordern.“

**Nach dem Kauf Journey:**

„Erstellen Sie eine Journey, die startet, wenn ein Kunde einen Online-Kauf tätigt. Senden Sie eine Push-Benachrichtigung, um sich für den Kauf zu bedanken. Überprüfen Sie anschließend, ob es sich um Mitglieder des Treueprogramms handelt. Wenn der Benutzer Mitglied des Treueprämien-Programms ist, senden Sie eine zweite Push-Benachrichtigung mit einem Rabattcode von 10 %. Wenn der Benutzer kein Mitglied des Treueprämien-Programms ist, senden Sie eine Push-Benachrichtigung, mit der er aufgefordert wird, sich für das Treueprogramm anzumelden. Warten Sie zwei Tage und senden Sie eine Follow-up-Push-Benachrichtigung mit einer Umfrage zu ihrem Kauferlebnis.“

**Ereignisbasierte Promotion:**

„Erstellen Sie eine Journey, die ausgelöst wird, wenn der Spielstand 50 erreicht. Senden Sie eine SMS-Nachricht an Mitglieder des Treueprämien-Teams, in der sie darauf hingewiesen werden, dass sie für ein kostenloses Stück Pizza vom Partner-Sponsor infrage kommen.“

### Zielgruppen-orientierte Journey-Eingabeaufforderungen

**Saisonkampagne:**

„Ich möchte eine Journey erstellen, die sich an ein Publikum von Tageswanderern richtet. Ich möchte eine E-Mail senden, die diese Zielgruppe auf meinen bevorstehenden Weihnachtsverkauf hinweist, der eine Vielzahl von Wander-Essentials enthält. Warten Sie 3 Tage nach dem Versand der ersten E-Mail und senden Sie eine zweite E-Mail, die einen 15%-Coupon mit kostenlosem Versand enthält. Warten Sie 1 Woche und senden Sie dann eine dritte E-Mail-Nachricht, um unsere neue Schlafsack- und Zeltkollektion zu zeigen. Planen Sie den Start der Journey am 20.12.20.“

**Wertschätzung der Treue:**

„Erstellen Sie eine Treueprogramm-Wertungs-Journey für SUV-Besitzer, einschließlich einer Dankes-Push-Benachrichtigung mit einem kostenlosen Autowaschangebot und einer Folge-Push-Benachrichtigung, wenn die erste Benachrichtigung nicht innerhalb eines Tages interagiert wird.“

### Eingabeaufforderungen mit offenem Ende

Für Benutzer, die ohne eine bestimmte Journey beginnen:

- „Ich möchte eine Journey erstellen“
- „Helfen Sie mir, eine Journey zu erstellen“
- „Create me a Journey&quot;

Der Agent stellt Anleitungen und Beispiele bereit, um Sie bei der Definition Ihrer Journey-Anforderungen zu unterstützen.

## Best Practices

### Best Practices bei der Eingabeaufforderung

Um die Effektivität von Journey Create Agent zu maximieren, befolgen Sie die folgenden Best Practices:

1. **Spezifisch**: Geben Sie eindeutige Details zu Ihren Journey-Zielen, Ihrer Zielgruppe und den gewünschten Aktionen an. Beinhalten Informationen über Kanäle, Timing und Bedingungen.
1. **Zeitvorgabe angeben**: Geben Sie eindeutig an, wann die Wartezeiten zwischen Aktionen sein sollen und wann die Journey gestartet werden soll.
1. **Bedingungen definieren**: Bei Verwendung der bedingten Logik müssen Sie die Kriterien für jeden Verzweigungspfad erläutern.
1. **Kanäle einschließen**: Geben Sie an, welche Kommunikationskanäle Sie verwenden möchten (Push, E-Mail, SMS).
1. **Erwähnung Planung**: Geben Sie für geplante Journey das gewünschte Startdatum und die gewünschte Startzeit an.
1. **Benutzerdefinierte Aktionen**: Wenn Sie benutzerdefinierte Aktionen in Ihrem Workflow verwenden, müssen Sie angeben, dass Sie eine benutzerdefinierte Aktion zusammen mit dem genauen Namen der benutzerdefinierten Aktion verwenden. Beispiel:
Wenn ein(e) Benutzende(r) meinen Store-Speicherort betritt, senden Sie eine Willkommensnachricht mit der benutzerdefinierten Aktion „ExternalPush“. Warten Sie 2 Tage und senden Sie dann eine Folgenachricht mit benutzerdefinierter Aktion ExternalEmail mit einer Umfrage zu ihrem Besuch.
1. **Ausdrücke überprüfen** Überprüfen und validieren Sie alle Ausdrücke, die von Journey Agent erstellt werden, um sicherzustellen, dass die richtigen Felder und Werte verwendet werden.

### Best Practices für die Einrichtung

- **Definieren Sie klare Ziele** Bevor Sie Journey erstellen, definieren Sie klare Ziele (Verbesserung der Kundenbindung, Förderung von Konversionen, Steigerung der Interaktion).
- **Zielgruppen vorbereiten**: Stellen Sie sicher, dass Ihre Zielgruppen bereits erstellt und ordnungsgemäß segmentiert sind.
- **Planen des Nachrichteninhalts**: Lassen Sie Ihre Messaging-Strategie vor der Erstellung von Journey definieren.
- **Kundenerlebnis berücksichtigen**: Entwerfen Sie Journey-Flüsse, die Kundenpräferenzen berücksichtigen und Überkommunikation vermeiden.

## Journey Analyze Agent: Kompetenzübersicht und Benutzerhandbuch

## Überblick

Journey Agent ermöglicht es Journey Optimizer-Anwendern, Journey mithilfe einer natürlichen Sprachschnittstelle zu analysieren und zu optimieren. Mit Journey Agent können Anwendende Zeitplankonflikte und/oder Zielgruppenkonflikte schnell identifizieren und lösen, Punkte der Benutzerkündigung in einer Journey erkennen und Einblicke oder Empfehlungen liefern. Er unterstützt Marketing-Fachleute dabei, datengestützte Entscheidungen zu treffen, die Kundeninteraktion zu verbessern und die Journey-Orchestrierung zu optimieren.

Erfahren Sie mehr und entdecken Sie den Agenten auf einen Blick in dieser [Übersicht](https://experienceleague.adobe.com/en/slides/journey-agent-overview).

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
- „Steht die Ausführung von Journey [Journey]Name} im Konflikt mit einer anderen Journey?“
- „Bitte Konflikte für [Journey-Name} erkennen und ].“
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

## Folien und Präsentation

>[!NOTE]
>
>Folien und Präsentationsmaterialien für Journey Agent werden hier zur Verfügung stehen. Bitte schauen Sie bald wieder vorbei, um Updates zu erhalten.
