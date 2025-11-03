---
title: KI in Experience Cloud-Anwendungen
description: Erfahren Sie, wie Experience Cloud-Anwendungen generative KI (GenAI), den KI-Assistenten und Agent-basierte KI einsetzen.
source-git-commit: 8c05562121071874002afd6d248f16186616da55
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 3%

---

# KI in Experience Cloud

Willkommen beim umfassenden Handbuch für KI-Funktionen in allen Adobe Experience Cloud-Programmen. In dieser Dokumentation wird beschrieben, wie generative KI-, KI-Assistent- und Adobe-Agenten in Ihre Experience Cloud-Workflows integriert werden, um die Produktivität zu beschleunigen und die Entscheidungsfindung zu verbessern.

## Inhalt dieses Handbuchs

### KI-Assistent

[AI Assistant](./ai-assistant/ai-assistant-ui.md) ist ein interaktives, generatives KI-Tool, das die Produktivität steigert und die Arbeit in Adobe Experience Platform-basierten Anwendungen neu definiert. Anwender können Produktkenntnisse erwerben, Probleme beheben und durch Spracheingabe operative Erkenntnisse gewinnen. Sie können auch den KI-Assistenten verwenden, um auf Adobe Experience Platform-Agenten und andere KI-Funktionen zuzugreifen.

**Wichtigste Funktionen:**

- **Konversationsoberfläche**: Sie können je nach Ihren Workflow-Voreinstellungen zwischen einer Vollbild- und einer Leistenansichtsoberfläche wählen.
- **Erkennungsaufforderungen**: Der KI-Assistent bietet vorkonfigurierte Aufforderungen, die nach Kategorien wie „Lernen“, „Analysieren“ und „Optimieren“ sortiert sind.
- **Kontexteinstellung**: Sie können die Einstellungen für Anwendung, Sandbox und Datenansicht so konfigurieren, dass Antworten empfangen werden, die auf Ihre Anforderungen zugeschnitten sind.
- **Datenvisualisierung**: Das Tool stellt interaktive Diagramme bereit, sodass Sie Einblicke aus Ihren Daten gewinnen können.
- **Reaktionsüberprüfung**: Alle Antworten enthalten Zitate aus Quellen, Erläuterungen zu KI-Argumenten und Mechanismen zur Bereitstellung von Feedback.


### Agent Orchestrator

[Adobe Experience Platform Agent Orchestrator &#x200B;](./agents/agent-orchestrator.md) ist die neue Agentenschicht in Adobe Experience Platform. Experience Platform Agent Orchestrator wurde entwickelt, um die umfangreichen Daten und das Kundenwissen der Plattform zu nutzen. Es unterstützt die Intelligenz und das Denken der speziell entwickelten Adobe Experience Platform-Experten und ermöglicht es ihnen, komplexe Entscheidungsfindungs- und Problemlösungsaufgaben schnell und skaliert auszuführen - alles unter menschlicher Aufsicht. Wenn Sie Fragen stellen oder Hilfe über eine natürliche Sprache in einer Gesprächsoberfläche wie dem KI-Assistenten anfordern, ruft Agent Orchestrator automatisch spezialisierte Agenten auf, um die richtigen Antworten zu erhalten. Agent Orchestrator speichert Ihren Gesprächsverlauf, sodass Sie auf natürliche Weise auf früheren Fragen aufbauen können, ohne den Kontext zu wiederholen, und kombiniert Einblicke aus mehreren Agenten, um Ihnen klare, einheitliche Antworten zu bieten.

**Kernkomponenten:**

- **Reasoning Engine**: Erstellt schrittweise Pläne und passt Ansätze nach Bedarf an
- **Spezialagenten**: Speziell entwickelte Agenten für bestimmte Aufgaben und Domains
- **Wissensdatenbank**: Sicherer Zugriff auf Business Intelligence und Dokumentation

### Spezialagenten

#### Audience Agent

Die Audience Agent bietet Einblicke in Zielgruppen, darunter:

- Erkennen signifikanter Änderungen der Zielgruppengröße.
- Identifizieren doppelter Zielgruppen.
- Durchsuchen des Zielgruppeninventars.
- Abrufen der Zielgruppengrößen.

Weitere Informationen finden Sie in der Dokumentation [&#x200B; &#x200B;](./agents/audience.md)Audience Agent .

#### Data Insights Agent

Verfügbar in Customer Journey Analytics, der Data Insights Agent:

- Beantwortet Fragen zu Ihren Daten in natürlicher Sprache.
- Erstellt relevante Visualisierungen in Analysis Workspace.
- Verwendet Komponenten aus Ihrer Datenansicht und tatsächliche Daten.

#### Journey Analyze Agent

Der Journey Analyze Agent ermöglicht Adobe Journey Optimizer-Benutzenden Folgendes:

- Analysieren und optimieren Sie Journey mit natürlicher Sprache.
- Konflikte mit Zeitplänen oder Zielgruppen erkennen und lösen.
- Analyse der Performance und der Abfallpunkte.

Weitere Informationen finden Sie in der [Journey Analyze Agent](./agents/ajo-agent-analyze.md)Dokumentation.

#### Produktsupport-Agent

Verwenden Sie den Produktsupport-Agenten für das Self-Service-Debugging und die Fehlerbehebung:

- Fehlerbehebung bei Adobe Experience Platform-Funktionen, ohne Workflows zu verlassen.
- Erstellen Sie Support-Tickets mit Kontext aus KI-Assistenten-Interaktionen.
- Überprüfen Sie Ticketaktualisierungen über den KI-Assistenten.

Weitere Informationen finden [&#x200B; in der &#x200B;](./agents/product-support.md) zum Product Support Agent .

## Erste Schritte

### Zugriffsanforderungen

Um den KI-Assistenten und die Experience Platform-Agenten zu verwenden, muss Ihr Adobe-Administrator die entsprechenden Berechtigungen einrichten:

- Um den KI-Assistenten in Real-Time CDP und Adobe Journey Optimizer zu verwenden, benötigen Sie die Berechtigung „KI-Assistenten aktivieren“ sowie die Berechtigung „Betriebliche Einblicke anzeigen“, um auf betriebliche Fragen zuzugreifen.
- Der Zugriff auf den KI-Assistenten in Customer Journey Analytics wird über die Customer Journey Analytics-Zugriffssteuerung verwaltet, mit der Sie sowohl Fragen zum Produktwissen als auch zu den Dateneinblicken stellen können.
- Für Adobe Experience Manager können Sie über die in der Adobe Admin Console festgelegten Berechtigungen auf den KI-Assistenten zugreifen.

### Datenschutz und Sicherheit

Der KI-Assistent wurde mit Datenschutz, Sicherheit und Governance im Vordergrund erstellt:

- Für Schulungen werden keine personenbezogenen Daten verwendet.
- Alle vorhandenen Zugriffssteuerungsrichtlinien werden berücksichtigt.
- HIPAA-fähig bei Verwendung mit Adobe Experience Platform Healthcare Shield.
- 30-tägige Aufbewahrungsrichtlinie für Interaktionsprotokolle.
- Sandbox-spezifische Datenisolierung.

## Best Practices

Um Ihr KI-Assistenzerlebnis optimal zu nutzen, befolgen Sie die folgenden Best Practices:

- **Seien Sie spezifisch** in Ihren Eingabeaufforderungen, um gezielte und relevante Einblicke vom KI-Assistenten zu erhalten.
- **Überprüfen Sie** Antworten, indem Sie die Zitate der Quelle und die vom KI-Assistenten bereitgestellten Begründungen durchgehen.
- **Verwenden Sie die**, um sicherzustellen, dass für Ihre Fragen die relevantesten Datenquellen verwendet werden.
- **Feedback geben**, um die Leistung und Genauigkeit des KI-Assistenten im Laufe der Zeit zu verbessern.
- **Kombinieren Sie** Erkenntnisse aus mehreren Agenten, um eine umfassendere und abgerundetere Analyse zu erzielen.

## Rechtliche Erwägungen

Bei der Verwendung des KI-Assistenten ist es wichtig, sich der wichtigsten rechtlichen und praktischen Überlegungen bewusst zu sein. Derzeit unterstützt der KI-Assistent Antworten nur auf Englisch. Überprüfen Sie die bereitgestellten Informationen immer sorgfältig, da Sprachmodelle gelegentlich Fehler machen können. Nutzen Sie die in den Antworten enthaltenen Schritte und Erläuterungen, um die Antworten, die Sie erhalten, besser zu verstehen. Wenn Sie auf Probleme oder Ungenauigkeiten stoßen, senden Sie bitte Feedback, um den KI-Assistenten im Laufe der Zeit zu verbessern.
