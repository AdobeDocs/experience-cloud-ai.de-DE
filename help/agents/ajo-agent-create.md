---
title: Journey Create Agent SKILL Overview
description: Erfahren Sie, wie Sie mit der Journey Agent Create-Fertigkeit Marketing-Journey über natürliche Spracheingaben in Journey Optimizer erstellen können.
solution: Journey Optimizer
product: journey optimizer
role: Admin,User,Developer
source-git-commit: 037d9864f72610f745b336acf0cf1192b7f21aa0
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---


# Journey Create Agent: Skill Overview and User Guide

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

