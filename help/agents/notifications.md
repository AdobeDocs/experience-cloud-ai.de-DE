---
title: Benachrichtigungsagent
description: Erfahren Sie, wie Sie mit dem Benachrichtigungsagenten im KI-Assistenten Ihre Adobe CX Enterprise-Benachrichtigungen in natürlicher Sprache zusammenfassen, interpretieren und bearbeiten können.
source-git-commit: d4254ada196055b869e6392b6d8cc2d4a037c4ad
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---

# Benachrichtigungsagent

Der Benachrichtigungsagent fügt eine dialogorientierte KI-Ebene in [KI-](../ai-assistant/ai-assistant-ui.md)) hinzu, mit der Sie Ihre Benachrichtigungen mithilfe natürlicher Sprache zusammenfassen, interpretieren und bearbeiten können, wodurch ein passiver Feed in einen aktiven Assistenten umgewandelt wird. Anstatt eine lange Liste zu scannen, können Sie in einem einzigen Austausch von „Ich habe 47 Benachrichtigungen“ zu „2 brauche meine Genehmigung bis Freitag, 3 Datensätze haben Konflikte, der Rest ist FYI“ wechseln.

## Was der Benachrichtigungsagent tun kann

Der Benachrichtigungs-Agent unterstützt die folgenden Funktionen:

| Funktionen | Beschreibung |
| --- | --- |
| **Zusammenfassung und Einblicke zu Benachrichtigungen** | Verschaffen Sie sich einen kurzen Überblick über Ihre Benachrichtigungen, unterscheiden Sie klar zwischen denen, die Maßnahmen erfordern, und denen, die nur informativer Natur sind, und verstehen Sie sowohl den Zweck einer Benachrichtigung als auch den Grund, warum Sie sie erhalten haben. |
| **Operative Aktionen** | Sie können Benachrichtigungen direkt über die Konversation bearbeiten, als gelesen markieren, Erinnerungen einblenden oder Erinnerungen für einzelne oder gruppierte Benachrichtigungen festlegen. |
| **Voreinstellungen und Einstellungen** | Aktivieren oder Deaktivieren von Benachrichtigungskanälen (E-Mail, Slack, In-App) pro Lösung und Kategorie, ohne Navigieren in den Einstellungen. |
| **Navigation und Deep-Linking** | Über Deep-Links von einer Benachrichtigung direkt in den relevanten Produktbereich springen. |
| **Collaboration und Freigabe** | Geben Sie Benachrichtigungen frei oder senden Sie Ankündigungen an Empfänger innerhalb derselben Organisation. |

## Auf Benachrichtigungsagent zugreifen

Sie können wie folgt auf den Benachrichtigungsagenten zugreifen:

- **Aus KI-Assistent**: Öffnen Sie den KI-Assistenten und geben Sie eine Benachrichtigungs-Eingabeaufforderung ein.
- **Aus der Eingabeaufforderungsbibliothek**: Wählen Sie eine Eingabeaufforderung aus, die Ihren Anforderungen entspricht.

## Eingabeaufforderungen im Beispiel

In den folgenden Abschnitten finden Sie Beispiele für Eingabeaufforderungen, die Sie mit dem Benachrichtigungsagenten verwenden können.

### Zusammenfassungen und Erkenntnisse

- „Zusammenfassen meiner letzten Benachrichtigungen.“
- „Welche meiner Benachrichtigungen benötigen meine Aktion im Vergleich zu meiner bisherigen Vorgehensweise?“

### Aktionen

- „Markieren Sie alle nicht verwertbaren Benachrichtigungen als gelesen.“
- „Erinnere mich in einer Stunde an die {NOTIFICATION_OF_INTEREST}-Benachrichtigung.“

### Einstellungen

- „Aktivieren von Slack-Benachrichtigungen für Journey Optimizer.“
- „Meine tägliche Zusammenfassung auf wöchentlich umstellen.“

### Zusammenarbeit

- „Diese Benachrichtigung für {EMAIL_ADDRESS_OF_USER_IN_YOUR_ORG} freigeben.“

## Best Practices

Beachten Sie bei der Verwendung des Benachrichtigungsagenten die folgenden Tipps:

- **Spezifisch** - Benennen Sie die App, die Benachrichtigung, die Benachrichtigungskategorie und den Kanal klar, damit der Agent auf die beabsichtigte Zielgruppe reagieren kann.
- **Kettenaufforderungen** - Sie können nach einer Zusammenfassung fragen, den Fokus auf eine bestimmte Benachrichtigung legen und dann eine Aktion ausführen, und das alles in einem einzigen Gespräch.
- **Antwort auf klärende Fragen** - Wenn der Agent um eine Bestätigung über die App, den Kanal oder die Benachrichtigung bittet, müssen Sie darauf antworten, damit die Änderungen korrekt angewendet werden.
