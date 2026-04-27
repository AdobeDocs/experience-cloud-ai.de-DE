---
description: Erfahren Sie, wie Sie Daten mit der Data Insights Agent in Customer Journey Analytics visualisieren können
title: Visualisieren von Daten mit der Data Insights Agent in Customer Journey Analytics
role: User, Admin
solution: Customer Journey Analytics
TQID: https://experienceleague.adobe.com/UtKIDlN2x7MOAiHNRRQ8b5OO4fIwzV74r1fnfMwblcQ
product_v2: id: e98b7246-966c-4318-9e95-cad2f7a17dc7
feature_v2: id: b743a5d9-dc51-41ed-8b2f-86a1f8de430fid: c73c4213-d623-4126-81f4-80b42e5e2656id: ce577701-5b9e-4fe4-8fa3-4eedea976da4
subfeature_v2: id: b1f5d324-a668-4e51-a59b-6fc0862d7310id: bc7a5a86-1a70-451f-985c-037b65f091d1id: df7fb1db-aa1b-4314-98ac-59dbfcc3044fid: e44e560d-5e5c-4a5f-9a87-eb8adbb817af
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: dd7883d8eccab3b0f006d55a850248e1c347d7e7
workflow-type: tm+mt
source-wordcount: 2690
ht-degree: 4%

---

# Visualisieren von Daten mit Data Insights Agent

>[!AVAILABILITY]
>
>Data Insights Agent steht berechtigten Kunden für eine begrenzte Zeit zur Verfügung. Der Zugriff auf Data Insights Agent ist bis zum 31. März 2026 verfügbar. Wenn Sie Data Insights Agent über dieses Datum hinaus ohne Unterbrechung weiter verwenden möchten, wenden Sie sich an Ihren Adobe-Kundenbetreuer, um mehr über Lizenzierung und Adobe Experience Platform Agent Orchestrator zu erfahren.

Data Insights Agent, auf das über den [KI-Assistenten](/help/ai-assistant/ai-assistant-ui.md) zugegriffen werden kann, ist ein generativer KI-Konversationsagent, der Fragen zu Ihren Daten schnell und effizient beantwortet. Er erstellt relevante Visualisierungen in Analysis Workspace mithilfe von Komponenten aus Ihrer Datenansicht und Ihren tatsächlichen Daten.

Die Verwendung von Data Insights Agent zur Beantwortung datenorientierter Fragen in Analysis Workspace kann viel Zeit sparen, die Sie andernfalls damit verbringen würden, Visualisierungen in Analysis Workspace manuell zu erstellen und sich mit Ihren Datenansichtskomponenten vertraut zu machen.

![Data Insights Agent im KI-Assistenten](/help/agents/images/cja-agent/cja-ai-asst-da.gif)

## Funktionen innerhalb und außerhalb des Projektumfangs

| Funktion | Im Umfang | Außerhalb des Geltungsbereichs |
| --- | --- | --- |
| **Visualisierungstypen** | <ul><li>Zeile</li><li>Mehrzeilig</li><li>Freiformtabelle</li><li>Balken</li><li>Ringdiagramm</li><li>Zusammenfassungszahl</li></ul> | <ul><li>Fluss</li><li>Fallout</li><li>Kohortentabelle</li><li>Bereich, Bereich gestapelt</li><li>Bar Stacked</li><li>Horizontales Säulendiagramm</li><li>Combo</li><li>Histogramm</li><li>Horizontal Bar, Horizontal Bar Stacked</li><li>Key Metric Summary</li><li>Streuung</li><li>Summary Change</li><li>Text</li><li>Treemap</li><li>Venn</li><li>Guided analysis: Active growth, Conversion trends, Engagement, First use impact, Frequency, Funnel, Net growth, Release impact, Retention, Timeline, Trends</li></ul> |
| **Workspace actions and agent capabilities** | <ul><li>Build and update visualizations<p>Generates a freeform table and associated visualization (such as a line, bar, donut, and so forth).</p><p>For example, *What is the profit across SKUs from February to May?*</p></li><li>Ask follow-up questions<p>Respond to a prompt in the context from any prior prompts. Beispiel:</p> <ul><li>Prompt 1: *Trend events from March.*</li><li>Prompt 2: *Show me the data from March to April instead*</li></ul> </li><li>Out-of-scope prompt detection<p>If you submit a prompt that is out of scope, such as *Export this project*, Data Insights Agent responds by informing you that the question is out of scope.</p></li></ul> | <ul><li>Freigeben</li><li>Exportieren</li><li>Herunterladen</li><li>Manage user preferences</li><li>Manage data view</li><li>Analytics Dashboards app</li><li>Attribution</li><li>In-line summary or response<p>Data Insights Agent cannot respond in-line in the chat rail with a summary answer of a user prompt. Examples of out-of-scope prompts are, *Give me a summary of the insights from my last prompt* and *Summarize the highlights from the line visualization.*</p></li></ul> |
| **Clarifying questions** | If you ask a question that does not have enough context for Data Insights Agent to answer, or is too generic, Data Insights Agent responds with a clarifying question or suggested options. <p>The following clarifying questions are examples of component-related questions:</p><ul><li>Metric: *Which &quot;revenue&quot; metric did you mean?*</li><li>Dimension: *Auf welche der folgenden „Regionen“ möchten Sie sich konzentrieren?*</li><li>Segment: *Welches „Konto“-Segment wollten Sie anwenden?*</li><li>Datumsbereich: *Mit „letztem Monat“ meinen Sie den letzten vollen Monat oder die letzten 30 Tage?*</li></ul><p>Die folgende klärende Frage ist ein Beispiel für eine Frage im Zusammenhang mit Dimensionselementen:</p> <ul><li>Welchen „Namen des Geschäfts“ meinten Sie? (Beispiel: #5274, #2949 usw.)</li></ul> | Die Klärung von Fragen beschränkt sich auf Komponenten und Dimensionselemente. Data Insights Agent kann Dinge wie Datenansichten, Visualisierungen, Datengranularität, Vergleich und Umfang nicht verdeutlichen. Wenn Klärungsfragen nicht verwendet werden können, verwendet der Agent standardmäßig das, was Sie am wahrscheinlichsten anfordern. Wenn eine unerwartete Visualisierung oder Datengranularität zurückgegeben wird, können Sie eine Folgefrage stellen oder die Visualisierung und Daten anpassen. |
| **Datenverifizierbarkeit und -richtigkeit** | Die Datenverifizierbarkeit und -richtigkeit können durch die Anzeige der generierten Freiformtabelle und Datenvisualisierung bestätigt werden. <p>Wenn Sie Data Insights Agent beispielsweise auffordern, *Bestellungen im letzten Monat* anzugeben, können Sie bestätigen, dass im neu generierten Bedienfeld, in der Datenvisualisierung und in der Freiformtabelle die richtige Metrik („Bestellungen„) und der richtige Datumsbereich („letzter Monat„) ausgewählt wurden.</p> | Data Insights Agent informiert Sie nicht darüber, welche Komponenten oder Visualisierungen hinzugefügt wurden. |
| **Feedback-Mechanismen** | <ul><li>Daumen hoch</li><li>Daumen runter</li><li>Markieren</li></ul> |  |


## Verwalten des Zugriffs auf Data Insights Agent {#manage-access}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-enable-data-insights-data-view"
>title="Für Data Insights Agent aktivieren"
>abstract="Diese Option aktiviert diese Datenansicht für die Verwendung mit Data Insights Agent. Data Insights Agent ist ein auf generativer KI basierender Konversations-Agent, auf den über den KI-Assistenten in Customer Journey Analytics zugegriffen werden kann. Damit können Sie Ihre Daten schnell mit Text-Prompts analysieren. Er erstellt relevante Visualisierungen in Analysis Workspace mithilfe von Komponenten aus Ihrer Datenansicht und unter Verwendung Ihrer tatsächlichen Daten."

<!-- markdownlint-enable MD034 -->

Die folgenden Parameter regeln den Zugriff auf Data Insights Agent in Customer Journey Analytics:

* **Zugriff auf Lösungen**: Data Insights Agent steht berechtigten Kundinnen und Kunden für eine begrenzte Zeit zur Verfügung. Der Zugriff auf Data Insights Agent ist bis zum 28. Februar 2026 verfügbar. Sie ist in Adobe Analytics nicht verfügbar.

* **Vertragszugriff**: Wenn Sie Data Insights Agent nicht im KI-Assistenten verwenden können, wenden Sie sich bitte an den Administrator Ihres Unternehmens oder an Ihr Adobe-Accountteam. Bevor Ihr Unternehmen Data Insights Agent verwenden kann, müssen Sie bestimmten rechtlichen Bedingungen im Zusammenhang mit generativer KI zustimmen.

* **Berechtigungen**: Die erforderlichen Berechtigungen müssen in der [!UICONTROL Adobe Admin Console gewährt werden] bevor Benutzerinnen und Benutzer auf Data Insights Agent zugreifen können.

  Um Berechtigungen zu erteilen, muss [Produktprofil-Administrator](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html) in der [!UICONTROL Admin Console die folgenden Schritte ausführen]:
   1. In the **[!UICONTROL Admin Console]**, select the **[!UICONTROL Products]** tab to view the **[!UICONTROL All products and services]** page.
   1. Select **[!UICONTROL Customer Journey Analytics]**.
   1. On the **[!UICONTROL Product Profiles]** tab, select the title of the product profile for which you want to provide access to [!UICONTROL AI Assistant: Product Knowledge].
   1. In the specific product profile, select the **[!UICONTROL Permissions]** tab.

      ![Permissions tab in Admin Console](/help/agents/images/cja-agent/ai-assistant-permissions-tab.png)

   1. In the **[!UICONTROL Reporting Tools]** row in the provided table, select the edit icon ![Edit](/help/agents/images/cja-agent/Edit.svg).
   1. Scroll to or search for **[!UICONTROL AI Assistant: Product Knowledge]**, then select the plus icon ![AddCircle](/help/agents/images/cja-agent/AddCircle.svg) next to this permission.
   1. Scroll to or search for **[!UICONTROL Data Insights Agent]**, then select the plus icon ![AddCircle](/help/agents/images/cja-agent/AddCircle.svg) next to this permission.

      The **[!UICONTROL AI Assistant: Product Knowledge]** permission and the **[!UICONTROL Data Insights Agent]** permission are added to the **[!UICONTROL Included permission items]** column.

      ![Add permission](/help/agents/images/cja-agent/ai-assistant-permissions.png).

   1. Select **[!UICONTROL Save]** to save the permissions.

  For additional information about access control, see [Access control](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/access-control#access-control).

* **Data view access**: Data views must be enabled for Data Insights Agent.

  >[!IMPORTANT]
  >
  >Consider the following when enabling data views:
  >* You can enable a maximum of 50 data views per IMS organization. If you enable more than 50 data views across all product profiles for a given organization, the Data Insights Agent will use the 50 most-used data views.
  >  You can use the [info on the Data Insights Agent column in Data views](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/manage-dataviews#manage-data-views) to view the number of data views that are enabled for Data Insights Agent in your IMS organization.
  >* The Data Insights Agent can reference the included data views sometime during the same day that you enable them.

  To enable data views for Data Insights Agent:

   1. In Customer Journey Analytics, select **[!UICONTROL Data Management]** > **[!UICONTROL Data views]**.

   1. Select one or more data views that you want to enable for Data Insights Agent, then select **[!UICONTROL Enable for Data Insights Agent]**.

      ![Enable data views for Data Insights Agent](/help/agents/images/cja-agent/data-view-enable-dia.png)

      For more information about enabling data views for Data Insights Agent, see the [AI Settings for a data view](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview#ai-settings/help/data-views/create-dataview.md #ai-settings).

  To view the number of data views that are enabled for Data Insights Agent in your IMS organization:

   1. In Customer Journey Analytics, select **[!UICONTROL Data Management]** > **[!UICONTROL Data views]**.

   1. Wählen Sie das Informationssymbol oben in der Spalte **[!UICONTROL Data Insights Agent]** aus.

      ![Infosymbol zu Data Insights Agent](/help/agents/images/cja-agent/data-insights-agent-tooltip.png)


## Zugriff auf Data Insights Agent im KI-Assistenten

1. Gehen Sie zu [experience.adobe.com](https://experience.adobe.com/) und melden Sie sich mit Ihrer Adobe ID an.

2. Wählen Sie **Customer Journey Analytics** auf der Experience Cloud-Startseite aus.

3. Wählen Sie **[!UICONTROL Leeres Projekt]** im Banner oben auf der Projektseite aus, um ein neues leeres Projekt zu öffnen.

4. Stellen Sie sicher, dass es sich bei der für das Bedienfeld ausgewählten Datenansicht um eine Datenansicht handelt, die für die Verwendung mit Data Insights Agent aktiviert wurde, wie unter [Verwalten des Zugriffs auf Data Insights Agent in Customer Journey Analytics](#manage-access-to-data-insights-agent-in-customer-journey-analytics) beschrieben.

5. Wählen Sie oben rechts auf der Seite das Chat-Symbol für den KI-Assistenten aus.

   Wenn das Chat-Symbol nicht angezeigt wird, wenden Sie sich an Ihren Administrator, damit er die folgenden Funktionen in der Admin Console aktivieren kann:

   * Reporting-Tools: **[!UICONTROL KI-Assistent: Produktkenntnisse]**

   * Datenansichts-Tools: **[!UICONTROL Data Insights Agent]**

   Weitere Informationen finden Sie unter [Zugriff auf Data Insights Agent in Customer Journey Analytics verwalten](#manage-access-to-data-insights-agent-in-customer-journey-analytics).

   ![KI-Assistenten-Symbol](/help/agents/images/cja-agent/ai-asst-icon.png)

6. Stellen Sie im **[!UICONTROL Fragen zu Customer Journey Analytics]** unten auf der Seite eine Frage zur Datenvisualisierung mit Data Insights Agent.

   Weitere Informationen finden Sie in den folgenden Beispielen.

### Beispiel 1

Nehmen wir beispielsweise an, Sie sind an den Bestellungen interessiert, die Ihr Unternehmen im Juli erhalten hat.

**Eingabeaufforderung:** Geben Sie *„Trend der Bestellungen im Juli“ ein*

![KI-Eingabeaufforderung](/help/agents/images/cja-agent/ai-asst-prompt1.png)

**Antwort:** Data Insights Agent sammelt Einblicke, indem es die Daten in der Datenansicht durchsucht, einschließlich der Metriken und Komponenten. Dadurch wird die Eingabeaufforderung in die richtigen Dimensionen und Metriken innerhalb des Datenbereichs übersetzt.

Wie Sie sehen können, wurden automatisch ein Liniendiagramm und eine Freiformtabelle generiert, um Bestellungen für Juli anzuzeigen.

![Antwort auf Eingabeaufforderung - Liniendiagramm und Freiformtabelle](/help/agents/images/cja-agent/ai-asst-result.png)

### Beispiel 2

Als Nächstes möchten Sie sehen, wie Ihr Umsatz nach Region verglichen wird.

**Prompt:** Geben Sie im Eingabeaufforderungsfenster *„Umsatz nach Region anzeigen“ ein*

**Antwort:** Data Insights Agent versteht, dass Sie mit „Region“ „Kundenregion“ meinen. It produces a bar chart that best shows revenue by region:

![Bar chart](/help/agents/images/cja-agent/ai-asst-result2.png)

### Beispiel 3

Next, in addition to understanding revenue by region, you also want to see data for profit by region. Instead of repeating the previous prompt, you can ask Data Insights Agent to update the most recent visualization and freeform table.

**Prompt:** In the prompt window, type *&quot;Add profit.&quot;*

**Response:** The **[!UICONTROL Bar]** chart still provides the most concise answer, but the profit metric has been added as a column in the freeform table:

![Bar chart](/help/agents/images/cja-agent/ai-asst-result4.png)

### Beispiel 4

Finally, let&#39;s look at the revenue by product category.

**Prompt:** In the prompt window, enter *&quot;Proportion of revenue by product category.&quot;*

**Response:** Again, Data Insights Agent picks the most appropriate visualization, in this case the **[!UICONTROL Donut]** visualization, to answer the question.

![Ringdiagramm](/help/agents/images/cja-agent/ai-asst-result3.png)

## Access Data Insights Agent across Experience Cloud applications

Adobe Experience Platform Agent Orchestrator allows you to access the functionality of Data Insights Agent in multiple Adobe Experience Cloud applications, such as Adobe Journey Optimizer and Real-Time CDP.

Agent Orchestrator interprets your request, determines which specialized agents are needed, and orchestrates them to deliver the right response. It keeps track of context across multi-turn interactions, so you can build on prior queries naturally.

For more information, see [Adobe Experience Platform Agent Orchestrator](https://business.adobe.com/products/experience-platform/agent-orchestrator.html).

## Example data visualization prompts

The following are some examples of common prompts and the visualizations used by Data Insights Agent to respond to those prompts.

| Beispiel-Eingabeaufforderung | Expected visualization |
| --- | --- |
| Show me profits in [Month] | Zeile<p>Asking for a trend or metric within a certain time range by default returns a line visualization. |
| Trend orders in [Month] | Zeile |
| Show revenue by region in [Month] | Balken |
| Share of revenue by product category | Ringdiagramm |
| Orders by day of week, from January to May | Balken |
| Bestellungen nach Geschlecht anzeigen, von März bis Juni | Balken |
| Wie hoch ist der Gewinn aller SKUs von Februar bis Mai? | Balken |
| Umsatz nach Filialname in [Monat] | Balken |
| Was waren meine Top 10 SKUs nach Gewinn in [Monat]? | Balken |
| Anteil der Käufe nach Monat des Jahres | Ringdiagramm |
| Gesamtgewinn in [Monat] | Zusammenfassungszahl<p>Wenn Sie über einen bestimmten Zeitraum nach der „Gesamtsumme“ einer Metrik fragen, sollte eine Visualisierung der Zusammenfassungszahl zurückgegeben werden. |


## Best Practices bei der Eingabeaufforderung

Data Insights Agent verarbeitet den Kontext, der von jeder Benutzeraufforderung bereitgestellt wird, und versucht, mit der am besten geeigneten Visualisierung und den am besten geeigneten Komponenten in einer Freiformtabelle intelligent zu reagieren.

Die Antworten können je nach den in der Eingabeaufforderung verwendeten spezifischen Wörtern und Ausdrücken variieren, und leichte Sprachänderungen können zu unterschiedlichen Ergebnissen führen.

Um die besten Ergebnisse zu erzielen, beachten Sie die folgenden Richtlinien:

* **Spezifisch:** Sie genaue Begriffe ein, um die Antwort einzugrenzen. Es folgt ein Beispiel für eine bestimmte Eingabeaufforderung: „Umsatz des letzten Monats in Kalifornien“

* **Klare Metriken, Dimensionen und Segmente verwenden:** Durch das Hinzufügen spezifischer Metriken (z. B. „Umsatz„), Dimensionen (z. B. „Website-Name„), Segmente (z. B. &quot;iPhone-Benutzer„) und Datumsbereiche (z. B. „Letzte drei Monate„) kann Data Insights Agent sich auf die richtigen Daten konzentrieren.

* **Direkte Fragen stellen:** Das direkte Formulieren von Fragen erleichtert Data Insights Agent die Bereitstellung klarer, relevanter Erkenntnisse. Im Folgenden finden Sie ein Beispiel für eine direkte Frage in einer Eingabeaufforderung: „Wie hoch ist der durchschnittliche Umsatz nach Produktkategorie in diesem Jahr?“

Sehen Sie sich die folgende Tabelle mit Beispielbegriffen und -ausdrücken an, die Sie in Eingabeaufforderungen mit Data Insights Agent verwenden können, zusammen mit den Antworttypen, die Sie erwarten können.

Diese Beispiele sollen Ihnen dabei helfen, sich damit vertraut zu machen, wie bestimmte Wörter oder Strukturen die Ausgabe der Data Insights Agent beeinflussen können, und so präzisere und wertvollere Einblicke gewährleisten. Data Insights Agent verwendet generative KI, sodass Visualisierungen oder ausgewählte Daten über ähnliche Eingabeaufforderungen hinweg leicht variieren können.

| Gewünschtes Ergebnis | Beispielbegriffe und Ausdrücke |
| --- | --- |
| Visualisierung der Zusammenfassungszahl | <ul><li>Gesamt</li></ul> |
| Vergleichen von Komponenten | <ul><li>Vergleichen</li><li>VS</li><li>Kontrast</li><li>Week-to-Week</li><li>Monat-zu-Monat</li><li>Quartalsvergleich</li><li>Year-over-Year</li></ul> |
| Ringvisualisierung | <ul><li>Verhältnis</li><li>Anteil von</li><li>Verteilung</li><li>Prozentsatz</li><li>Beitrag</li><li>Anteil</li><li>Teile</li></ul> |
| Linienvisualisierung | <ul><li>Trend</li><li>[Metrik] in [Zeitbereich]</li></ul> |
| Balkenvisualisierung | <ul><li>[Metrik] von [Dimension]</li></ul> |

<!--

## Beta testing expectations and requested feedback

After posing each question, carefully review the assistant's provided answer. It's crucial to evaluate the generated visualizations comprehensively before providing feedback. 

Consider the following when evaluating a response from Data Insights Agent: 

* Chat rail response or template: Evaluate the textual response provided. Is the response appropriate given the context of your prompt? 

* Visualization/chart: Evaluate the visualization. Is it the appropriate or expected visualization for your question, or would you have expected a different visualization?  

* Freeform table: Evaluate the freeform table. Is the freeform table data correct? Is it breaking down data where requested? Are the applied segments those that you requested or expected? 

* Error Message / Out-of-Scope: If a generic error message is given stating the question is out of scope, provide feedback on whether you think the out-of-scope message is appropriate, given your prompt. Was your prompt actually in scope? 

**For every response, give a thumbs up or thumbs down, based on the response.**

Following the thumbs up or thumbs down selection, please make a selection for the relevant multi-select feedback boxes. If you want to provide additional feedback, add notes in the open text box.

## Questions and Contact

* Send questions and feedback in the Beta Slack channel: #data-insights-agent-in-cja-beta

-->


## Best Practices für die Konfiguration

Im Folgenden finden Sie Best Practices für Ihre Customer Journey Analytics-Konfiguration (Datenansicht, berechnete Metriken, Segmente usw.), um sicherzustellen, dass die Data Insights Agent die richtigen Komponenten finden und sauberere Antworten zurückgeben kann, ohne Sie nach zusätzlichen Informationen fragen zu müssen.

* **Balancieren Sie die benötigten Komponenten**. Fügen Sie nicht alle Felder Ihrer Datensätze als Metriken oder Dimensionskomponenten zu Ihrer Datenansicht hinzu, insbesondere nicht die, die Sie bei Ihrer Analyse nicht erwarten. Beschränken Sie sich jedoch nicht ausschließlich auf die Felder, die Sie für Ihre Analyse benötigen. Eine zu eingeschränkte Datenansicht schränkt die Flexibilität Ihrer Analyse und die Data Insights Agent-Funktionen ein.
* **Verwenden Sie immer Anzeigenamen**. Stellen Sie sicher, dass alle Felder, die Sie in Ihrer Datenansicht entweder als Metrik- oder Dimensionskomponente definieren, einen Anzeigenamen für die Komponente aufweisen. Der Prozess des Umbenennens von Feldern mit einem Anzeigenamen ist insbesondere für Felder aus Adobe Analytics-Quell-Connector-Datensätzen relevant. Diese Felder haben häufig nicht benutzerfreundliche, nicht identifizierbare Namen wie `eVar41` oder `prop25`.
* **Verwenden Sie eindeutige Namen**. Unterschiedliche Namen sind besonders relevant, wenn Sie dasselbe Feld sowohl als Metrik- als auch als Dimensionskomponente in Ihrer Datenansicht verwenden. Oder wenn Sie ein Feld in mehreren Komponenten desselben Typs verwenden (z. B. in zwei verschiedenen Metriken), die jeweils unterschiedliche Komponenteneinstellungen aufweisen.
* **Verwenden Sie eine Benennungskonvention für Komponenten**. Sie können eine Komponentennamenskonvention verwenden, um Komponenten zu gruppieren. Beispielsweise können **[!UICONTROL Bestellungen | Produkt]** und **[!UICONTROL Bestellungen | Kunde]** zwischen verschiedenen Bestellmetriken unterscheiden, die möglicherweise in Ihren Daten vorhanden sind.
* **Verwenden des Datenwörterbuchs**. Fügen Sie Beschreibungen und andere relevante Daten für Komponenten im Datenwörterbuch hinzu. Der Data Insights Agent verwendet derzeit keine Beschreibung und Tags aus dem Datenwörterbuch, könnte aber in Zukunft verwendet werden.
* **Verwenden Sie genehmigte berechnete Metriken**. Sie müssen sich auf einen Prozess einigen, bei dem nur genehmigte berechnete Metriken als Komponenten in Ihrer Datenansicht verwendet werden, und die Verwendung experimenteller berechneter Metriken vermeiden.
* **Freigeben erforderlicher Segmente**. Stellen Sie sicher, dass Sie Segmente freigeben und Segmente sichtbar machen, die für Data Insights Agent-Eingabeaufforderungen erforderlich sind.
* **Standardisieren von Komponentennamen in Datenansichten**. Wenn Sie dieselben Felder wie eine Komponente in mehreren Datenansichten verwenden, stellen Sie sicher, dass Sie einen einzigen Anzeigenamen und eine einzige Kennung für diese Komponente verwenden. Durch einen einzigen Namen und eine einzige Kennung kann die Data Insights Agent Datenansichten wechseln, ohne den Kontext zu verlieren.


>[!MORELIKETHIS]
>
>[Komponenteneinstellungen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/overview)
>[Datenwörterbuch](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/data-dictionary/data-dictionary-overview)
>[Berechnete Metrik genehmigen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-approving)
>[Segmente freigeben](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/segments/seg-share)
