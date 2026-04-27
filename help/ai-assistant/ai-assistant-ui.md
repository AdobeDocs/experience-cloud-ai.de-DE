---
title: Handbuch zur Benutzeroberfläche des KI-Assistenten
description: Erfahren Sie, wie Sie in der Benutzeroberfläche auf den KI-Assistenten zugreifen und ihn nutzen können.
TQID: https://experienceleague.adobe.com/MWhVCqUFt5Qze4mQp-G85OF81Mk1OL4xY8Jygm-B4PI
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: dd7883d8eccab3b0f006d55a850248e1c347d7e7
workflow-type: tm+mt
source-wordcount: 2162
ht-degree: 3%

---

# KI-Assistent

>[!IMPORTANT]
>
>Dieses Dokument gilt für KI-Assistenten (der nächsten Generation). Informationen zum KI-Assistenten (veraltet) finden Sie im [Handbuch zur Benutzeroberfläche des KI-Assistenten](https://experienceleague.adobe.com/de/docs/experience-platform/ai-assistant/home) in der Dokumentation zu Adobe Experience Platform.

In der folgenden Tabelle finden Sie einen Vergleich von KI-Assistent (veraltet) und KI-Assistent (nächste Generation):

| Merkmalsbereich | KI-Assistent (veraltet) | KI-Assistent (nächste Generation) |
| --- | --- | --- |
| Benutzererlebnis | Der KI-Assistent (veraltet) ist nur in einem Bereich der rechten Leiste verfügbar. | Der KI-Assistent (der nächsten Generation) ist sowohl im Bereich der rechten Leiste als auch im immersiven Vollbilderlebnis verfügbar. |
| Funktionsumfang | Sie können den KI-Assistenten (frühere Version) sowohl für Produktkenntnisse als auch für betriebliche Einblicke verwenden. | Sie können den KI-Assistenten (der nächsten Generation) für Produktkenntnisse, operative Einblicke sowie erweiterte agentische Fähigkeiten und die Ausführung mehrstufiger Aufgaben verwenden. |
| Architektur von Platform | Der KI-Assistent (veraltet) wurde nicht auf dem Agent Orchestrator-Stack erstellt. | Der KI-Assistent (der nächsten Generation) wird von [Adobe Experience Platform Agent Orchestrator &#x200B;](https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator) unterstützt und ermöglicht Erweiterbarkeit und erweiterte Koordinierung über Funktionen hinweg. |
| Anwendungsbereich | Der KI-Assistent (veraltet) ist eine anwendungsspezifische Implementierung. | Sie können den KI-Assistenten (der nächsten Generation) für ein einheitliches KI-Assistentenerlebnis in allen Adobe Experience Cloud-Programmen verwenden. |
| Zugriffs- und Berechtigungsmodell | Auf einzelne Produktgrenzen abgestimmtes Zugriffsmodell für die Anwendung. | Alle Benutzer erhalten Zugriff auf den KI-Assistenten (der nächsten Generation) und die zugehörigen Experience Platform-Agenten. **Hinweis**: <ul><li>**Adobe Experience Manager**: Ihr Administrator muss Ihnen über die [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html) die Berechtigung für den Zugriff auf den KI-Assistenten (der nächsten Generation) erteilen.</li><li>**Customer Journey Analytics**: Ihr Administrator muss Ihnen die Berechtigung für den Zugriff auf den KI-Assistenten über die [Customer Journey Analytics-Zugriffssteuerung](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/access-control?lang=en) erteilen. Auf diese Weise können Sie Fragen zu Produktwissen und Dateneinblicken stellen. |

AI Assistant ist ein interaktives, generatives KI-Tool, das die Produktivität steigert und die Arbeit in Adobe Experience Platform-basierten Anwendungen neu definiert. Sie können den KI-Assistenten verwenden, um auf Adobe Experience Platform-Agenten und andere KI-Funktionen zuzugreifen.

Lesen Sie dieses Handbuch, um zu erfahren, wie Sie den KI-Assistenten verwenden können.

![Die Benutzeroberfläche des KI-Assistenten im Vollbildmodus.](./images/ai-assistant/blank-home.png)

>[!SLIDE](agent-orchestrator-ui)

## Zugriff auf den KI-Assistenten

Es gibt mehrere Möglichkeiten, auf den KI-Assistenten zuzugreifen.

Wählen Sie auf der Experience Cloud-Startseite **[!UICONTROL KI-Assistent]** aus der linken Navigationsleiste, um die Vollbildansicht des KI-Assistenten zu öffnen.

+++Zum Anzeigen auswählen

![Die Experience Cloud-Startseite mit dem ausgewählten Symbol für den KI-Assistenten im linken Navigationsbereich.](./images/ai-assistant/from-experience-cloud.png)

+++

Sie können den KI-Assistenten auch über die Startseiten von Experience Cloud-Programmen wie Experience Platform, Adobe Journey Optimizer und Customer Journey Analytics starten. Navigieren Sie zu Ihrer Produkt-Startseite und wählen Sie dann in der oberen **das Symbol** KI-Assistent“ aus, um das Chat-Bedienfeld des KI-Assistenten in der rechten Leiste zu starten.

+++Zum Anzeigen auswählen

![Die Produkt-Startseite mit dem im linken Navigationsbereich ausgewählten Symbol „KI-Assistent“.](./images/ai-assistant/from-product.png)

+++

## Navigieren in der Benutzeroberfläche des KI-Assistenten

In diesem Abschnitt erfahren Sie, wie Sie in der Benutzeroberfläche des KI-Assistenten navigieren können.

### Vollbildansicht

Die Benutzeroberfläche des KI-Assistenten umfasst mehrere wichtige Elemente, die Ihnen bei der effektiven Interaktion helfen:

1. **[!UICONTROL Unterhaltungen]**: Wählen Sie das Symbol **[!UICONTROL Unterhaltungen]** aus, um eine neue Unterhaltung zu beginnen und auf aktuelle Unterhaltungen aus Ihrem Verlauf zuzugreifen. Weitere Informationen finden Sie im Abschnitt zu [Konversationen](#conversations).
2. **Eingabefeld**: Wählen Sie das Eingabefeld aus, um Fragen und Eingabeaufforderungen für den KI-Assistenten einzugeben. Weitere Informationen finden Sie im Abschnitt zu [Eingabefunktionen](#input-features).
3. **Daten und Objekt automatisch vervollständigen**: - Wählen Sie das Pluszeichen, um Daten- und Objektvorschläge zu verwenden und die automatische Vervollständigung durchzuführen. Wenn ausgewählt, können Sie ein Popup-Fenster verwenden, um vorgeschlagene Entitäten auszuwählen. Weitere Informationen finden Sie im Abschnitt zu [automatische Vervollständigung von Daten und Objekten](#autocomplete).
4. **Kontexteinstellung**: Wählen Sie das Symbol Kontexteinstellung aus, um Informationsquellen für den KI-Assistenten zu konfigurieren. Sie können dieses Tool verwenden, um die Anwendung, Sandbox und Datenansicht zu konfigurieren, auf die der KI-Assistent verweist, um Ihre Abfrage zu beantworten. Weitere Informationen finden Sie im Abschnitt zu [Kontexteinstellungen](#context-setting).
5. **Discovery**: Wählen Sie **[!UICONTROL Lernen]**, **[!UICONTROL Analysieren]** und **[!UICONTROL Optimieren]**, um Beispielabfragen anzuzeigen, mit denen Sie beginnen können. Weitere Informationen finden Sie im Abschnitt zu [Entdeckungsaufforderungen](#discoverability-prompts).

![Der KI-Assistent im Vollbildmodus.](./images/ai-assistant/ui-home.png)

### Leistenansicht

Die Leistenansicht bietet schnellen Zugriff auf Chat, Erkennungsaufforderungen, Aktualisierungen, Unterhaltungen und Benutzeroberflächen-Steuerelemente in einem kompakten Bedienfeld.

1. **[!UICONTROL Chat]**: Wählen Sie **[!UICONTROL Chat]** in der Kopfzeile aus, um zu Ihrer Konversation zurückzukehren, falls Sie sie verlassen haben, um auf verschiedene Elemente in der Benutzeroberfläche zuzugreifen.
1. **[!UICONTROL Discovery]**: Wählen Sie **[!UICONTROL Discovery]** aus, um eine Liste der Eingabeaufforderungen des KI-Assistenten nach Kategorie geordnet anzuzeigen. Sie können diese vorkonfigurierten Eingabeaufforderungen verwenden, um Ihren Chat zu füllen. Darüber hinaus können Sie die vorgeschlagenen Eingabeaufforderungen an Ihren jeweiligen Anwendungsfall anpassen.
1. **[!UICONTROL Neue Funktionen]** Wählen Sie **[!UICONTROL Neue Funktionen]** aus, um eine Liste der neuesten Aktualisierungen anzuzeigen, die für den KI-Assistenten verfügbar sind.
1. **[!UICONTROL Unterhaltungen]**: Wählen Sie das Symbol **[!UICONTROL Unterhaltungen]** aus, um eine neue Unterhaltung zu beginnen und auf aktuelle Unterhaltungen aus Ihrem Verlauf zuzugreifen. Weitere Informationen finden Sie im Abschnitt zu [Konversationen](#conversations).
1. **Vollbildansicht**: Wählen Sie das Symbol **[!UICONTROL Vollbildansicht]** aus, um Ihre Benutzeroberfläche des KI-Assistenten von der rechten Leiste in den Vollbildmodus zu ändern.
1. **Automatische Vervollständigung von Daten und Objekten**: Wählen Sie das Pluszeichen, um Daten- und Objektvorschläge zu verwenden und die automatische Vervollständigung durchzuführen. Wenn ausgewählt, können Sie ein Popup-Fenster verwenden, um vorgeschlagene Entitäten auszuwählen. Weitere Informationen finden Sie im Abschnitt zu [automatische Vervollständigung von Daten und Objekten](#autocomplete).
1. **Kontexteinstellung**: Wählen Sie das Symbol Kontexteinstellung aus, um Informationsquellen für den KI-Assistenten zu konfigurieren. Sie können dieses Tool verwenden, um die Anwendung, Sandbox und Datenansicht zu konfigurieren, auf die der KI-Assistent verweist, um Ihre Abfrage zu beantworten. Weitere Informationen finden Sie im Abschnitt zu [Kontexteinstellungen](#context-setting).

![Der KI-Assistent in der Leistenansicht](./images/ai-assistant/rail-mode.png)

## Handbuch zur Benutzeroberfläche des KI-Assistenten

Dieser Abschnitt bietet einen Überblick über die wichtigsten Funktionen und Navigationsoptionen in der Benutzeroberfläche des KI-Assistenten. Es wird erläutert, wie auf den KI-Assistenten zugegriffen wird, das Layout und die Steuerelemente sowohl in der Vollbild- als auch in der Leistenansicht beschrieben werden und es werden wichtige Tools wie Unterhaltungen, Eingabefunktionen, automatische Vervollständigung, Kontexteinstellungen und Erkennungsaufforderungen vorgestellt. Die folgenden Abschnitte enthalten detaillierte Anleitungen zur Verwendung dieser Funktionen, um mit dem KI-Assistenten zu interagieren und Ihre Erfahrung optimal zu nutzen.

### Erkennungsaufforderungen {#discovery-prompts}

You can use AI Assistant&#39;s discovery feature to view a list of the general subjects, grouped into entities, that AI Assistant supports. Discovery prompts are different depending on your starting point.

>[!BEGINTABS]

>[!TAB Use discovery from the full screen view]

From the full screen view, discovery prompts are grouped into three categories: **[!UICONTROL Learn]**, **[!UICONTROL Analyze]**, and **[!UICONTROL Optimize]**.

To use discovery prompts to advance product knowledge, select **[!UICONTROL Learn]** and then select a prompt from the dropdown window that appears.

![The discovery prompt selection from the full screen view.](./images/ai-assistant/inputs/discover.png)

>[!TAB Use discover from the rail view]

Select **[!UICONTROL Discovery]** from the rail view to access an extensive list of discovery prompts that you can use to get started and populate your chat with AI Assistant.

![The discovery panel from the rail view.](./images/ai-assistant/inputs/discover-rail.png)

>[!ENDTABS]

Select a prompt to populate the input box. From here, you can edit the prompt to fit your particular use case. When ready, select the send icon on the right to submit your query.

![The discover prompt in the input box.](./images/ai-assistant/inputs/question-input.png)

## Interacting with responses

### Check for reasoning process {#reasoning}

AI Assistant then queries its knowledge base and computes an answer. After a few moments, AI Assistant returns an answer, including options to dive deeper into its reasoning process, related suggestions, information sources, and feedback tools.

To better understand the underlying reasoning process, select **[!UICONTROL Reasoning complete]**.

![The AI Assistant response.](./images/ai-assistant/inputs/answer.png)

The *[!UICONTROL Reasoning complete]* window expands to display a summary of your request and details on how the response was crafted.

![The expanded reasoning panel in an AI Assistant response.](./images/ai-assistant/inputs/reasoning-complete.png)

### Use related suggestions

Next, navigate down to the bottom of the response and select **[!UICONTROL Related suggestions]** to receive a list of prompts relating to your initial query. You can use these prompts to further continue your conversation with AI Assistant.

![The related suggestions window in AI Assistant.](./images/ai-assistant/inputs/related-suggestions.png)

### Quellen anzeigen

Um die Antwort des KI-Assistenten zu überprüfen, wählen Sie **[!UICONTROL Quellen]** aus, um eine Liste der Informationsquellen anzuzeigen, auf die der KI-Assistent bei der Berechnung seiner Antwort verwiesen hat.

![Die Liste der Quellen, auf die vom KI-Assistenten verwiesen wird.](./images/ai-assistant/inputs/sources.png)

### Feedback geben

Mithilfe der mit der Antwort bereitgestellten Optionen können Sie Feedback zu Ihren Erfahrungen mit dem KI-Assistenten geben.

Um Feedback zu geben, wählen Sie entweder Daumen hoch oder Daumen runter aus, nachdem Sie eine Antwort vom KI-Assistenten erhalten haben, und geben Sie dann Ihr Feedback in das bereitgestellte Textfeld ein.

![Die Symbole „Daumen hoch“ und „Daumen runter“ im KI-Assistenten.](./images/ai-assistant/inputs/feedback.png)

>[!BEGINTABS]

>[!TAB Daumen hoch]

Wählen Sie **[!UICONTROL Daumen hoch]**, um positives Feedback zu geben. Sie können optional aus einer Liste mit positivem Feedback auswählen oder das Eingabefeld verwenden, um Ihr eigenes spezifisches Feedback einzugeben.

+++Zum Anzeigen auswählen

![Das Feedback-Fenster mit dem Daumen nach oben.](./images/ai-assistant/inputs/thumbs-up.png)

Sie können auch **[!UICONTROL Detailliertes Feedback]** auswählen, um Ihr Feedback weiter auszuarbeiten. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Absenden]**..

![Das detaillierte Feedback-Fenster für Daumen hoch.](./images/ai-assistant/inputs/thumbs-up-detailed.png)

+++

>[!TAB Daumen runter]

Wählen Sie **[!UICONTROL Daumen runter]** um konstruktives Feedback zu geben. Sie können optional aus einer Liste mit konstruktivem Feedback auswählen oder das Eingabefeld verwenden, um Ihr eigenes spezifisches Feedback einzugeben.

+++Zum Anzeigen auswählen

![Das Feedback-Fenster mit den Daumen nach unten.](./images/ai-assistant/inputs/thumbs-down.png)

Ebenso können Sie auch **[!UICONTROL Detailliertes Feedback]** auswählen, um Ihr Feedback weiter auszuarbeiten. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Absenden]**..

![Das detaillierte Feedback-Fenster für die Daumen nach unten.](./images/ai-assistant/inputs/thumbs-down-detailed.png)

+++

>[!ENDTABS]

### Verwenden der Funktion „Aufspaltungsansicht“

Wenn die Antwort des KI-Assistenten ein Bild enthält, können Sie das Pfadsymbol auswählen, um einen Aufspaltungsmodus zu starten. Auf diese Weise können Sie die gesamte Antwort des KI-Assistenten mit dem kontextuellen Bild, das auf der rechten Seite angezeigt wird, lesen.

![Der Aufspaltungsmodus im KI-Assistenten.](./images/ai-assistant/inputs/split-view.png)

### Unterhaltungen

Sie können das Bedienfeld *[!UICONTROL Alle Konversationen]* verwenden, um Konversationen mit dem KI-Assistenten zurückzusetzen und erneut aufzurufen. Wählen Sie das Symbol **[!UICONTROL Konversationen]** aus, um das Fenster *[!UICONTROL Alle Konversationen]* anzuzeigen.

![Das Fenster „Konversationen“ im KI-Assistenten.](./images/ai-assistant/conversations/select-conversations.png)

To revisit a previous conversation, select the conversation topic from the list provided.

![The list of previous conversations recorded on AI Assistant.](./images/ai-assistant/conversations/revisit-conversation.png)

To start a new conversation, select **[!UICONTROL New conversation]**.

![The &quot;new conversation&quot; option selected.](./images/ai-assistant/conversations/new-conversation.png)

### Context setting {#context-setting}

Use the context setting feature of AI Assistant to configure the **application**, **sandbox**, and **dataview** that AI Assistant references to answer your query. To access context setting, select the **[!UICONTROL Context setting]** icon from the input box.

![The context setting icon selected.](./images/ai-assistant/inputs/context-selection.png)

The *[!UICONTROL Answer from...]* pop-up window appears. Use this window to configure the information sources that you want to use and then select **[!UICONTROL Set context]**.

| Information source | Beschreibung | Beispiele |
| --- | --- | --- |
| App | The Experience Cloud application that your query pertains to. | Experience Platform, Journey Optimizer, Customer Journey Analytics, etc. |
| Sandbox | The sandbox that contains the dataset(s) or information that your query pertains to. | Prod (VA7), Dev. |
| Dataview | When you&#39;re using AI Assistant with Customer Journey Analytics, the dataview setting helps the Data Insights Agent understand: <ul><li>Which datasets to query</li><li>What data components are available</li><li>How to structure responses about your data</li><li>Which visualizations to create in Analysis Workspace</li></ul> | |

![The &quot;Answer from&quot; panel where information sources can be configured.](./images/ai-assistant/inputs/answer-from.png)

### Data and object autocomplete

You can use the autocomplete function to receive a list of data objects that exist in your sandbox. Um die automatische Vervollständigung zu verwenden, geben Sie in Ihrer Abfrage das Pluszeichen (+) ein. Alternativ können Sie auch das Pluszeichen (+) unten im Texteingabefeld auswählen. Es wird ein Fenster mit einer Liste empfohlener Datenobjekte aus Ihrer Sandbox angezeigt.

![Die Schaltfläche zur automatischen Vervollständigung von Daten und Objekt wurde ausgewählt.](./images/ai-assistant/autocomplete/autocomplete.png)

### Überprüfen von Antworten

Es gibt eine Reihe von Möglichkeiten, Antworten des KI-Assistenten zu überprüfen. Wählen Sie **[!UICONTROL Abfragebegriff, der mit Objekten]** wurde) aus, um eine Zusammenfassung der Begriffe in Ihrer Abfrage anzuzeigen, die mit bestimmten Objekten in Ihrer Organisation abgeglichen wurden.

![Die Abfragebegriffe entsprechen Ihrer Antwort.](./images/ai-assistant/autocomplete/query-terms.png)

Wählen Sie **[!UICONTROL Hier habe ich die Ergebnisse erhalten]** um eine detaillierte, schrittweise Erklärung zu erhalten, wie der KI-Assistent zu seiner Antwort gelangt ist. Darüber hinaus können Sie auch die SQL-Abfrage anzeigen, die zur Beantwortung Ihrer Frage ausgeführt wurde. Diese Abfrage ist schreibgeschützt und wird für die Verwendung im Abfrage-Service nicht unterstützt.

![Die SQL-Verifizierungs-Tools im KI-Assistenten.](./images/ai-assistant/autocomplete/verifications.png)

### Konfigurieren der Datenvisualisierung

Sie können die Datenvisualisierungsfunktionen des KI-Assistenten verwenden, um Ihre Daten besser zu verstehen. Sie können auch den Diagrammtyp angeben, den Sie in Ihrer Abfrage verwenden möchten. Senden Sie beispielsweise eine Abfrage mit folgendem Inhalt: **Nach Produktname für letzten Monat (Balken) Gewinn anzeigen“**, um ein Balkendiagramm für den Gewinn im letzten Monat zu erhalten, sortiert nach Produktname.

![Ein Balkendiagramm wird im KI-Assistenten angezeigt](./images/ai-assistant/visualization/graph.png)

Wählen Sie anschließend **[!UICONTROL Eigenschaften]**, um den Diagrammtyp zu ändern und Werte für Ihre X- und Y-Achse zu konfigurieren.

Der KI-Assistent unterstützt verschiedene Diagrammtypen für die Datenvisualisierung. Sie können mit allen Diagrammtypen interagieren, indem Sie den Mauszeiger über die Daten bewegen.

>[!BEGINTABS]

>[!TAB Line]

Um ein Liniendiagramm anzuzeigen, wählen Sie **[!UICONTROL Eigenschaften]** und anschließend **[!UICONTROL Linie]** aus.

![Ein Liniendiagramm im KI-Assistenten.](./images/ai-assistant/visualization/line.png)

>[!TAB Bereich]

Um ein Flächendiagramm anzuzeigen, wählen Sie **[!UICONTROL Eigenschaften]** und dann **[!UICONTROL Bereich]** aus.

![Ein Flächendiagramm im KI-Assistenten.](./images/ai-assistant/visualization/area.png)

>[!TAB Streuung]

Um ein Streudiagramm anzuzeigen, wählen Sie **[!UICONTROL Eigenschaften]** und dann **[!UICONTROL Streudiagramm]** aus.

![Ein Streudiagramm im KI-Assistenten.](./images/ai-assistant/visualization/scatter.png)

>[!TAB Ringdiagramm]

Um ein Ringdiagramm anzuzeigen, wählen Sie **[!UICONTROL Eigenschaften]** und dann **[!UICONTROL Ringdiagramm]** aus.

![Ein Ringdiagramm im KI-Assistenten.](./images/ai-assistant/visualization/donut.png)

>[!ENDTABS]
