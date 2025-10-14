---
title: Adobe Experience Platform Agent Orchestrator
description: Erfahren Sie mehr über Adobe Experience Platform Agent Orchestrator.
source-git-commit: 352ba791195eca7f68e6d317e0f2449d6ededeb2
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 2%

---

# Adobe Experience Platform Agent Orchestrator

Adobe Experience Platform Agent Orchestrator ist die neue agentische Schicht in Adobe Experience Platform. Experience Platform Agent Orchestrator wurde entwickelt, um die umfangreichen Daten und das Kundenwissen von Experience Platform zu nutzen. unterstützt die Intelligenz und das Denken der speziell entwickelten Adobe Experience Platform-Experten und ermöglicht es ihnen, komplexe Entscheidungsfindungs- und Problemlösungsaufgaben schnell und skaliert auszuführen - alles unter menschlicher Aufsicht. Wenn Sie Fragen stellen oder Hilfe über eine natürliche Sprache in einer Gesprächsoberfläche wie dem KI-Assistenten anfordern, ruft Agent Orchestrator automatisch spezialisierte Agenten auf, um die richtigen Antworten zu erhalten. Agent Orchestrator speichert Ihren Gesprächsverlauf, sodass Sie auf natürliche Weise auf früheren Fragen aufbauen können, ohne den Kontext zu wiederholen, und kombiniert Einblicke aus mehreren Agenten, um Ihnen klare, einheitliche Antworten zu bieten.

Sie können komplexe End-to-End-Workflows über eine intuitive Gesprächsoberfläche abschließen, ohne wissen zu müssen, welche Agenten hinter den Kulissen arbeiten. Das System versteht Ihre Ziele, erstellt schrittweise Pläne und passt seinen Ansatz nach Bedarf auf der Grundlage Ihres Feedbacks an. In Ihrem Gespräch im KI-Assistenten können Sie das Agent Orchestrator-Begründungsfeld erkunden, um den schrittweisen Denkprozess zu sehen und besser zu verstehen, wie Ihre Anfragen verarbeitet werden.

Lesen Sie dieses Dokument, um mehr über Agent Orchestrator zu erfahren.

## Komponenten von Agent Orchestrator {#components}

Agent Orchestrator besteht aus mehreren Schlüsselkomponenten, darunter die KI-Assistenten-Gesprächsoberfläche, eine Argumentations-Engine für Entscheidungsfindung und Planung, spezialisierte Adobe Experience Platform-Agenten und eine Wissensdatenbank, die Zugriff auf relevante Informationen bietet.

![Die Marketing-Architektur von Agent Orchestrator.](./images/agent-orchestrator/agentic-architecture.png)

### Konversationsschnittstelle des KI-Assistenten {#ai-assistant}

KI-Assistent ist ein intelligentes, in natürlicher Sprache geführtes Gesprächserlebnis, das es Anwendern von Experience Cloud-fähigen Programmen ermöglicht, GenAI- und AgentAI-Funktionen zu nutzen, deren Umfang von den von Kunden lizenzierten Experience Cloud-Programmen abhängt. Um den Zugriff zu entsperren, lesen Sie [Handbuch zum Zugriff auf den KI-Assistenten](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/access).

Weitere Informationen finden Sie im [Handbuch zur Benutzeroberfläche des KI-Assistenten](../ai-assistant/ai-assistant-ui.md).

### Begründungs-Engine {#reasoning-engine}

Die Reasoning-Engine interpretiert Ihre Ziele basierend auf Ihren natürlichen Sprachaufforderungen, überprüft alle Grenzen oder Anforderungen und erstellt schrittweise Pläne, um Ihnen beim Erreichen Ihrer Ziele zu helfen. Im Gegensatz zu einfachen Frage-und-Antwort-Systemen kann sie ihre Pläne anpassen, wenn sich die Dinge ändern, und zurückgehen und bei Bedarf andere Ansätze ausprobieren. Die von ihr erstellten Pläne werden Ihnen in der Benutzeroberfläche des KI-Assistenten angezeigt, damit Sie den Prozess sehen und verfolgen sowie bei Bedarf eingreifen können.

### Adobe Experience Platform-Agenten {#agents}

Adobe Experience Platform-Agenten sind eine speziell entwickelte Gruppierung von KI-Agenten, die in der Lage sind, gängige Aufträge über Kundenerlebnis-Domains hinweg bereitzustellen. Nachfolgend finden Sie eine Liste der Adobe Experience Platform-Agenten, die derzeit in Experience Cloud-Programmen verfügbar sind:

| Agent | Details | Unterstützte Anwendungen |
| --- | --- | --- |
| [Audience Agent](audience.md) | Mit Audience Agent können Sie Einblicke zu Zielgruppen erhalten, einschließlich der Erkennung signifikanter Änderungen der Zielgruppengröße, der Erkennung doppelter Zielgruppen, der Untersuchung Ihres Zielgruppeninventars und des Abrufs der Zielgruppengröße. | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | Data Insights Agent, auf das über den KI-Assistenten in Customer Journey Analytics zugegriffen werden kann, ist ein generativer KI-Konversationsagent, der Fragen zu Ihren Daten schnell und effizient beantwortet. Er erstellt relevante Visualisierungen in Analysis Workspace mithilfe von Komponenten aus Ihrer Datenansicht und unter Verwendung Ihrer tatsächlichen Daten. | Customer Journey Analytics |
| [Experimentationsagent](./agent-experiment.md) | Experimentationsagent hilft Teams, schneller zu lernen, indem sie Experimentergebnisse analysieren, Auswirkungen vorhersagen und neue Experimente vorschlagen. Es zentralisiert frühere und aktive Experimente, sodass Sie auf dem aufbauen können, was Sie bereits gelernt haben, Lücken erkennen und Prioritäten setzen können, was als Nächstes getestet werden soll. | Adobe Journey Optimizer Experimentation Accelerator |
| [Journey Agent](./ajo-agent-analyze.md) | Mit Journey Agent können Adobe Journey Optimizer-Benutzer Journey-Dateien über eine natürliche Sprachschnittstelle erstellen, analysieren und optimieren. Mit Journey Agent können Sie schnell Journey erstellen, Zeitplan- oder Zielgruppenkonflikte erkennen und lösen, Leistungs- und Abfallpunkte analysieren und leistungsstarke Journey ermitteln, die für zukünftige Kampagnen repliziert werden können. Dies hilft Ihnen bei datengesteuerten Entscheidungen, verbessert die Kundeninteraktion und optimiert die Journey-Orchestrierung. | Adobe Journey Optimizer |
| [Produktsupport-Agent](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/new-features/customer-support) | Der Produktsupport-Agent ist eine Selbstbedienungs-Debugging- und Fehlerbehebungsfunktion, mit der Sie Fehler in Adobe Experience Platform-Funktionen und -Anwendungen beheben können, ohne Ihre Workflows verlassen zu müssen. Support-Administratoren können Support-Tickets mit Kontext aus Ihren KI-Assistenten-Interaktionen erstellen und Sie können Ticket-Aktualisierungen über den KI-Assistenten überprüfen. | <ul><li>Adobe Experience Platform</li><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li><li>Adobe Journey Optimizer B2B edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

Weitere Informationen zur Verfügbarkeit von Agenten in Experience Cloud-Programmen finden Sie in der Dokumentation [Agent-KI in Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/features/agentic-ai).

### Knowledgebase {#knowledge-base}

Die Wissensdatenbank bietet Agenten sicheren Zugriff auf Customer Business Intelligence durch strukturierte und unstrukturierte Datenquellen, einschließlich Adobe-Produktdokumentation, Kundenmetadaten zu Geschäftsobjekten und Analysedaten.

## Zugriff {#access}

KI-Assistentenanfragen werden mit den Adobe Identity Management Services authentifiziert. Berechtigungen werden von der Adobe Experience Platform-Zugriffssteuerung und der Customer Journey Analytics-Zugriffssteuerung erzwungen.

Um Zugriff auf die Konversationsoberfläche des KI-Assistenten zu erhalten und einen oder mehrere Experience Platform-Agenten zu verwenden, muss Ihnen Ihr Adobe-Administrator die entsprechenden Berechtigungen in der Benutzeroberfläche „Berechtigungen“ oder in der Adobe Admin Console gewähren:

* **Real-Time CDP** und **Adobe Journey Optimizer**: Ihr Administrator muss Ihnen die Berechtigung **KI-Assistenten aktivieren** erteilen, um Ihnen den Zugriff auf den KI-Assistenten zu ermöglichen. Ihr Administrator muss Ihnen auch die Berechtigungen **Betriebseinblicke anzeigen** erteilen, damit Sie im KI-Assistenten Fragen zu Betriebseinblicken stellen können. Beide Berechtigungen werden vom Administrator in der Benutzeroberfläche „Berechtigungen“ festgelegt.

* **Customer Journey Analytics**: Ihr Administrator muss Ihnen die Berechtigung für den Zugriff auf den KI-Assistenten über die [Customer Journey Analytics-Zugriffssteuerung](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/access-control) erteilen. Auf diese Weise können Sie Fragen zu Produktwissen und Dateneinblicken stellen.

>[!NOTE]
>
>Operative Insights-Fragen sind für Customer Journey Analytics nicht verfügbar. Daher werden keine zusätzlichen Berechtigungen angewendet.

* **Adobe Experience Manager**: Ihr Administrator muss Ihnen über die [Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html) die Berechtigung für den Zugriff auf den KI-Assistenten erteilen.

