---
description: Erfahren Sie, wie Sie Daten mit der Data Insights Agent in Customer Journey Analytics visualisieren können
title: Visualisieren von Daten mit der Data Insights Agent in Customer Journey Analytics
role: User, Admin
solution: Customer Journey Analytics
source-git-commit: 04a73ac0f705cd3a2184fb2f8599aff85b7bb5e5
workflow-type: tm+mt
source-wordcount: '2499'
ht-degree: 5%

---

# Visualisieren von Daten mit Data Insights Agent

>[!AVAILABILITY]
>
>Data Insights Agent steht berechtigten Kunden für eine begrenzte Zeit zur Verfügung. Der Zugriff auf Data Insights Agent ist bis zum 28. Februar 2026 verfügbar. Wenn Sie Data Insights Agent ohne Unterbrechung weiter verwenden möchten, wenden Sie sich an Ihren Adobe-Kundenbetreuer, um mehr über Lizenzierung und Adobe Experience Platform Agent Orchestrator zu erfahren.

Data Insights Agent, auf das über den [KI-Assistenten](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant) in Customer Journey Analytics zugegriffen werden kann, ist ein generativer KI-Konversationsagent, der Fragen zu Ihren Daten schnell und effizient beantwortet. Er erstellt relevante Visualisierungen in Analysis Workspace mithilfe von Komponenten aus Ihrer Datenansicht und unter Verwendung Ihrer tatsächlichen Daten.

Die Verwendung von Data Insights Agent zur Beantwortung datenorientierter Fragen in Analysis Workspace kann unzählige Stunden einsparen, die Sie andernfalls möglicherweise damit verbringen würden, Visualisierungen in Analysis Workspace manuell zu erstellen und sich mit Ihren Datenansichtskomponenten vertraut zu machen.

![Data Insights Agent im KI-Assistenten](images/cja-agent//cja-ai-asst-da.gif)

## Funktionen innerhalb und außerhalb des Projektumfangs

| Funktion | Im Umfang | Außerhalb des Geltungsbereichs |
| --- | --- | --- |
| **Visualisierungstypen** | <ul><li>Zeile</li><li>Mehrzeilig</li><li>Freiformtabelle</li><li>Balken</li><li>Ringdiagramm</li><li>Zusammenfassungszahl</li></ul> | <ul><li>Fluss</li><li>Fallout</li><li>Kohortentabelle</li><li>Bereich, Bereich gestapelt</li><li>Balken gestapelt</li><li>Horizontales Säulendiagramm</li><li>Combo</li><li>Histogramm</li><li>Horizontalbalken, Horizontalbalken gestapelt</li><li>Zusammenfassung einer Schlüsselmetrik</li><li>Streuung</li><li>Zusammenfassungsänderung</li><li>Text</li><li>Treemap</li><li>Venn</li><li>Geführte Analyse: Aktives Wachstum, Konversionstrends, Interaktion, Auswirkung auf die erste Verwendung, Häufigkeit, Funnel, Nettowachstum, Auswirkungen auf die Veröffentlichung, Kundenbindung, Zeitleiste, Trends</li></ul> |
| **Workspace-Aktionen und Agentenfunktionen** | <ul><li>Erstellen und Aktualisieren von Visualisierungen<p>Erzeugt eine Freiformtabelle und eine dazugehörige Visualisierung (z. B. Linie, Balken, Ringdiagramm usw.).<p>Beispiel: *Was ist der Gewinn für alle SKUs von Februar bis Mai?*</p></li><li>Stellen von Folgefragen<p>Reagieren Sie auf eine Eingabeaufforderung im Kontext von allen vorherigen Eingabeaufforderungen. Beispiel:</p> <ul><li>Eingabeaufforderung 1: *Trendereignisse ab März.*</li><li>Eingabeaufforderung 2: *Zeigen Sie mir stattdessen die Daten von März bis April*</li></ul> </li><li>Prompterkennung außerhalb des Geltungsbereichs<p>Wenn Sie eine Eingabeaufforderung übermitteln, die außerhalb des Gültigkeitsbereichs liegt, z. B. *Dieses Projekt exportieren*, informiert Data Insights Agent Sie darüber, dass die Frage außerhalb des Gültigkeitsbereichs liegt.</p></li></ul> | <ul><li>Freigeben</li><li>Exportieren</li><li>Download</li><li>Benutzereinstellungen verwalten</li><li>Datenansicht verwalten</li><li>Analytics Dashboards App</li><li>Attribution</li><li>Inline-Zusammenfassung oder -Antwort<p>Data Insights Agent kann in der Chat-Leiste nicht mit einer zusammenfassenden Antwort auf eine Benutzeraufforderung antworten. Beispiele für Eingabeaufforderungen außerhalb des Projektumfangs sind: *Geben Sie mir eine Zusammenfassung der Einblicke aus meiner letzten Eingabeaufforderung* und *Fassen Sie die Highlights aus der Linienvisualisierung zusammen.*</p></li></ul> |
| **Fragen klären** | Wenn Sie eine Frage stellen, die nicht genügend Kontext für eine Antwort von Data Insights Agent hat oder zu generisch ist, antwortet Data Insights Agent mit einer klärenden Frage oder empfohlenen Optionen. <p>Die folgenden klärenden Fragen sind Beispiele für komponentenbezogene Fragen:</p><ul><li>Metrik: *Welche „Umsatz“-Metrik meinten Sie?*</li><li>Dimension: *Auf welche der folgenden „Regionen“ möchten Sie sich konzentrieren?*</li><li>Segment: *Welches „Konto“-Segment wollten Sie anwenden?*</li><li>Datumsbereich: *Mit „letztem Monat“ meinen Sie den letzten vollen Monat oder die letzten 30 Tage?*</li></ul><p>Die folgende klärende Frage ist ein Beispiel für eine Frage im Zusammenhang mit Dimensionselementen:</p> <ul><li>Welchen „Namen des Geschäfts“ meinten Sie? (Beispiel: #5274, #2949 usw.)</li></ul> | Die Klärung von Fragen beschränkt sich auf Komponenten und Dimensionselemente. Data Insights Agent kann Dinge wie Datenansichten, Visualisierungen, Datengranularität, Vergleich und Umfang nicht verdeutlichen. Wenn Klärungsfragen nicht verwendet werden können, verwendet der Agent standardmäßig das, was Sie am wahrscheinlichsten anfordern. Wenn eine unerwartete Visualisierung oder Datengranularität zurückgegeben wird, können Sie eine Folgefrage stellen oder die Visualisierung und Daten anpassen. |
| **Datenverifizierbarkeit und -richtigkeit** | Die Datenverifizierbarkeit und -richtigkeit können durch die Anzeige der generierten Freiformtabelle und Datenvisualisierung bestätigt werden. <p>Wenn Sie Data Insights Agent beispielsweise auffordern, *Bestellungen im letzten Monat* anzugeben, können Sie bestätigen, dass im neu generierten Bedienfeld, in der Datenvisualisierung und in der Freiformtabelle die richtige Metrik („Bestellungen„) und der richtige Datumsbereich („letzter Monat„) ausgewählt wurden. | Data Insights Agent informiert Sie nicht darüber, welche Komponenten oder Visualisierungen hinzugefügt wurden.</p> |
| **Feedback-Mechanismen** | <ul><li>Daumen hoch</li><li>Daumen runter</li><li>Markieren</li></ul> |  |


## Verwalten des Zugriffs auf Data Insights Agent {#manage-access}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-enable-data-insights-data-view"
>title="Für Data Insights Agent aktivieren"
>abstract="Diese Option aktiviert diese Datenansicht für die Verwendung mit Data Insights Agent. Data Insights Agent ist ein auf generativer KI basierender Konversations-Agent, auf den über den KI-Assistenten in Customer Journey Analytics zugegriffen werden kann. Damit können Sie Ihre Daten schnell mit Text-Prompts analysieren. Er erstellt relevante Visualisierungen in Analysis Workspace mithilfe von Komponenten aus Ihrer Datenansicht und unter Verwendung Ihrer tatsächlichen Daten."

<!-- markdownlint-enable MD034 -->

Die folgenden Parameter regeln den Zugriff auf Data Insights Agent in Customer Journey Analytics:

* **Zugriff auf Lösungen**: Data Insights Agent steht allen Customer Journey Analytics-Kunden im Rahmen eines eingeschränkten Zugriffsprogramms bis zum 30. November 2025 zur Verfügung. Sie ist in Adobe Analytics nicht verfügbar.

* **Vertragszugriff**: Wenn Sie Data Insights Agent nicht im KI-Assistenten verwenden können, wenden Sie sich bitte an den Administrator Ihres Unternehmens oder an Ihr Adobe-Accountteam. Bevor Ihr Unternehmen Data Insights Agent verwenden kann, müssen Sie bestimmten rechtlichen Bedingungen im Zusammenhang mit generativer KI zustimmen.

* **Berechtigungen**: Die erforderlichen Berechtigungen müssen in der [!UICONTROL Adobe Admin Console gewährt werden] bevor Benutzerinnen und Benutzer auf Data Insights Agent zugreifen können.

  Um Berechtigungen zu erteilen, muss [Produktprofil-Administrator](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html) in der [!UICONTROL Admin Console die folgenden Schritte ausführen]:

   1. Wählen Sie in **[!UICONTROL Admin Console]** die Registerkarte **[!UICONTROL Produkte]** aus, um die Seite **[!UICONTROL Alle Produkte und Services]** anzuzeigen.
   1. **[!UICONTROL Customer Journey Analytics]**.
   1. Wählen Sie auf **[!UICONTROL Registerkarte]** den Titel des Produktprofils aus, für das Sie Zugriff auf den [!UICONTROL KI-Assistenten: Produktkenntnisse“ ] möchten.
   1. Wählen Sie im jeweiligen Produktprofil die Registerkarte **[!UICONTROL Berechtigungen]** aus.

      ![Registerkarte „Berechtigungen“ in Admin Console](images/cja-agent/ai-assistant-permissions-tab.png)

   1. Wählen Sie in **[!UICONTROL Zeile „Reporting]** Tools“ in der angegebenen Tabelle das Bearbeitungssymbol ![Bearbeiten](images/cja-agent/Edit.svg).
   1. Scrollen Sie zu oder suchen Sie nach **[!UICONTROL KI-Assistent:]** Produktkenntnisse“ und klicken Sie dann auf das Pluszeichen ![AddCircle](images/cja-agent/AddCircle.svg) neben dieser Berechtigung.
   1. Scrollen Sie zu oder suchen Sie nach **[!UICONTROL Data Insights Agent]** und wählen Sie dann das Pluszeichen ![AddCircle](images/cja-agent/AddCircle.svg) neben dieser Berechtigung aus.

      Die Berechtigung **[!UICONTROL KI-Assistent: Produktwissen]** und die Berechtigung **[!UICONTROL Data Insights Agent]** werden der Spalte **[!UICONTROL Enthaltene Berechtigungselemente]** hinzugefügt.

      ![Berechtigung hinzufügen](images/cja-agent/ai-assistant-permissions.png).

   1. Wählen **[!UICONTROL Speichern]**, um die Berechtigungen zu speichern.

  Weitere Informationen zur Zugriffssteuerung finden Sie unter [Zugriffssteuerung](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/access-control#access-control).

* **Zugriff auf Datenansicht**: Datenansichten müssen für Data Insights Agent aktiviert sein.

  >[!IMPORTANT]
  >
  >Beachten Sie beim Aktivieren von Datenansichten Folgendes:
  >* Sie können maximal 50 Datenansichten pro IMS-Organisation aktivieren. Wenn Sie für ein Unternehmen mehr als 50 Datenansichten für alle Produktprofile aktivieren, verwendet die Data Insights Agent die 50 am häufigsten verwendeten Datenansichten.
  >* Die Data Insights Agent kann die enthaltenen Datenansichten an einem Tag referenzieren, an dem Sie sie aktivieren.

  So aktivieren Sie Datenansichten für Data Insights Agent:

   1. Wählen Sie in Customer Journey Analytics **[!UICONTROL Daten-Management]** > **[!UICONTROL Datenansichten]**.
   1. Wählen Sie eine oder mehrere Datenansichten aus, die Sie für Data Insights Agent aktivieren möchten, und wählen Sie dann **[!UICONTROL Für Data Insights Agent aktivieren]**.

      ![Aktivieren von Datenansichten für Data Insights Agent](images/cja-agent/data-view-enable-dia.png)

  So zeigen Sie die Anzahl der Datenansichten an, die für Data Insights Agent in Ihrer IMS-Organisation aktiviert sind:

   1. Wählen Sie in Customer Journey Analytics **[!UICONTROL Daten-Management]** > **[!UICONTROL Datenansichten]**.
   1. Wählen Sie das Informationssymbol oben in der Spalte **[!UICONTROL Data Insights Agent]** aus.

      ![Infosymbol zu Data Insights Agent](images/cja-agent/data-insights-agent-tooltip.png)

## Zugriff auf Data Insights Agent im KI-Assistenten

1. Gehen Sie zu [experience.adobe.com](https://experience.adobe.com/) und melden Sie sich mit Ihrer Adobe ID an.
1. Wählen Sie **Customer Journey Analytics** auf der Experience Cloud-Startseite aus.
1. Wählen Sie **[!UICONTROL Leeres Projekt]** im Banner oben auf der Projektseite aus, um ein neues leeres Projekt zu öffnen.
1. Stellen Sie sicher, dass es sich bei der für das Bedienfeld ausgewählten Datenansicht um eine Datenansicht handelt, die für die Verwendung mit Data Insights Agent aktiviert wurde, wie unter [Verwalten des Zugriffs auf Data Insights Agent in Customer Journey Analytics](#manage-access-to-data-insights-agent-in-customer-journey-analytics) beschrieben.
1. Wählen Sie oben rechts auf der Seite das Chat-Symbol für den KI-Assistenten aus.

   Wenn das Chat-Symbol nicht angezeigt wird, wenden Sie sich an Ihren Administrator, damit er die folgenden Funktionen in der Admin Console aktivieren kann:

   * Reporting-Tools: **[!UICONTROL KI-Assistent: Produktkenntnisse]**
   * Datenansichts-Tools: **[!UICONTROL Data Insights Agent]**

   Weitere Informationen finden Sie unter [Zugriff auf Data Insights Agent in Customer Journey Analytics verwalten](#manage-access-to-data-insights-agent-in-customer-journey-analytics).

   ![KI-Assistenten-Symbol](images/cja-agent/ai-asst-icon.png)

1. Stellen Sie im **[!UICONTROL Fragen zu Customer Journey Analytics]** unten auf der Seite eine Frage zur Datenvisualisierung mit Data Insights Agent.

   Weitere Informationen finden Sie in den folgenden Beispielen.

### Beispiel 1

Nehmen wir beispielsweise an, Sie sind an den Bestellungen interessiert, die Ihr Unternehmen im Juli erhalten hat.

**Eingabeaufforderung:** Geben Sie *„Trend der Bestellungen im Juli“ ein*

![KI-Eingabeaufforderung](images/cja-agent/ai-asst-prompt1.png)

**Antwort:** Data Insights Agent sammelt Einblicke, indem es die Daten in der Datenansicht durchsucht, einschließlich der Metriken und Komponenten. Dadurch wird die Eingabeaufforderung in die richtigen Dimensionen und Metriken innerhalb des Datenbereichs übersetzt.

Wie Sie sehen können, wurden automatisch ein Liniendiagramm und eine Freiformtabelle generiert, um Bestellungen für Juli anzuzeigen.

![Antwort auf Eingabeaufforderung - Liniendiagramm und Freiformtabelle](images/cja-agent/ai-asst-result.png)

### Beispiel 2

Als Nächstes möchten Sie sehen, wie Ihr Umsatz nach Region verglichen wird.

**Prompt:** Geben Sie im Eingabeaufforderungsfenster *„Umsatz nach Region anzeigen“ ein*

**Antwort:** Data Insights Agent versteht, dass Sie mit „Region“ „Kundenregion“ meinen. Es wird ein Balkendiagramm erstellt, das den Umsatz am besten nach Region zeigt:

![Balkendiagramm](images/cja-agent/ai-asst-result2.png)

### Beispiel 3

Als Nächstes möchten Sie nicht nur den Umsatz nach Region verstehen, sondern auch Daten für den Gewinn nach Region anzeigen. Anstatt die vorherige Eingabeaufforderung zu wiederholen, können Sie Data Insights Agent bitten, die neueste Visualisierungs- und Freiformtabelle zu aktualisieren.

**Prompt:** Geben Sie im Eingabeaufforderungsfenster „Gewinn hinzufügen *ein*

**Antwort:** Das **[!UICONTROL Balkendiagramm]** bietet weiterhin die prägnanteste Antwort, aber die Gewinnmetrik wurde als Spalte in der Freiformtabelle hinzugefügt:

![Balkendiagramm](images/cja-agent/ai-asst-result4.png)

### Beispiel 4

Sehen wir uns abschließend den Umsatz nach Produktkategorie an.

**Eingabeaufforderung:** Geben Sie im Eingabeaufforderungsfenster *„Umsatzanteil nach Produktkategorie“ ein*

**Antwort** Auch hier wählt Data Insights Agent die am besten geeignete Visualisierung aus, in diesem Fall die **[!UICONTROL Ringdiagramm]**-Visualisierung, um die Frage zu beantworten.

![Ringdiagramm](images/cja-agent/ai-asst-result3.png)

## Zugriff auf Data Insights Agent über Experience Cloud-Anwendungen hinweg

Adobe Experience Platform Agent Orchestrator ermöglicht den Zugriff auf die Funktionen von Data Insights Agent in mehreren Adobe Experience Cloud-Anwendungen, z. B. Adobe Journey Optimizer und Real-Time CDP.

Agent Orchestrator interpretiert Ihre Anfrage, bestimmt, welche spezialisierten Agenten benötigt werden, und orchestriert sie, um die richtige Antwort zu liefern. Es verfolgt den Kontext über Multi-Turn-Interaktionen hinweg, sodass Sie auf natürliche Weise auf früheren Abfragen aufbauen können.

Weitere Informationen finden Sie unter [Adobe Experience Platform Agent Orchestrator ](/help/agents/agent-orchestrator.md).

## Eingabeaufforderungen zur Beispieldatenvisualisierung

Im Folgenden finden Sie einige Beispiele für häufige Eingabeaufforderungen und die Visualisierungen, die von Data Insights Agent verwendet werden, um auf diese Eingabeaufforderungen zu reagieren.

| Beispiel-Eingabeaufforderung | Erwartete Visualisierung |
| --- | --- |
| Gewinne anzeigen in [Monat] | Zeile<p>Wenn Sie innerhalb eines bestimmten Zeitbereichs nach einem Trend oder einer Metrik fragen, wird standardmäßig eine Linienvisualisierung zurückgegeben. |
| Trend der Bestellungen in [Monat] | Zeile |
| Umsatz nach Region anzeigen in [Monat] | Balken |
| Umsatzanteil nach Produktkategorie | Ringdiagramm |
| Bestellungen nach Wochentag von Januar bis Mai | Balken |
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

Diese Beispiele sollen Ihnen dabei helfen, sich mit der Frage vertraut zu machen, wie bestimmte Wörter oder Strukturen die Ausgabe des Data Insight-Agenten beeinflussen können, um präzisere und wertvollere Einblicke zu ermöglichen. Data Insights Agent verwendet generative KI, sodass Visualisierungen oder ausgewählte Daten über ähnliche Eingabeaufforderungen hinweg leicht variieren können.

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

* **Balancieren Sie die benötigten Komponenten**. Fügen Sie nicht alle Felder Ihrer Datensätze als Metriken oder Dimensionskomponenten zu Ihrer Datenansicht hinzu. Insbesondere die , die Sie mit Sicherheit nicht in Ihrer Analyse verwenden werden. Beschränken Sie sich jedoch nicht ausschließlich auf die Felder, die Sie für Ihre Analyse benötigen. Eine zu eingeschränkte Datenansicht schränkt die Flexibilität Ihrer Analyse und die Data Insights Agent-Funktionen ein.
* **Verwenden Sie immer Anzeigenamen**. Stellen Sie sicher, dass alle Felder, die Sie in Ihrer Datenansicht entweder als Metrik- oder Dimensionskomponente definieren, einen Anzeigenamen für die Komponente aufweisen. Der Prozess des Umbenennens von Feldern mit einem Anzeigenamen ist insbesondere für Felder aus Adobe Analytics-Quell-Connector-Datensätzen relevant. Diese Felder haben häufig nicht benutzerfreundliche, nicht identifizierbare Namen wie `eVar41` oder `prop25`.
* **Verwenden Sie eindeutige Namen**. Unterschiedliche Namen sind besonders relevant, wenn Sie dasselbe Feld sowohl als Metrik- als auch als Dimensionskomponente in Ihrer Datenansicht verwenden. Oder wenn Sie ein Feld in mehreren Komponenten desselben Typs verwenden (z. B. in zwei verschiedenen Metriken), die jeweils unterschiedliche Komponenteneinstellungen aufweisen.
* **Verwenden Sie eine Benennungskonvention für Komponenten**. Sie können eine Komponentennamenskonvention verwenden, um Komponenten zu gruppieren. Beispiel: **[!UICONTROL Bestellungen | Produkt]** und **[!UICONTROL Bestellungen | Kunde]** kann zwischen verschiedenen Bestellmetriken unterscheiden, die möglicherweise in Ihren Daten vorhanden sind.
* **Verwenden des Datenwörterbuchs**. Beschreibung und andere relevante Daten für Komponenten im Datenwörterbuch hinzufügen. Der Data Insight-Agent verwendet derzeit keine Beschreibung und Tags aus dem Datenwörterbuch, könnte dies aber in Zukunft tun.
* **Verwenden Sie genehmigte berechnete Metriken**. Sie müssen sich auf einen Prozess einigen, bei dem nur genehmigte berechnete Metriken als Komponenten in Ihrer Datenansicht verwendet werden, und die Verwendung experimenteller berechneter Metriken vermeiden.
* **Freigeben erforderlicher Segmente**. Stellen Sie sicher, dass Sie Segmente freigeben und Segmente sichtbar machen, die für Data Insights Agent-Eingabeaufforderungen erforderlich sind.
* **Standardisieren von Komponentennamen in Datenansichten**. Wenn Sie dieselben Felder wie eine Komponente in mehreren Datenansichten verwenden, stellen Sie sicher, dass Sie einen einzigen Anzeigenamen und eine einzige Kennung für diese Komponente verwenden. Durch einen einzigen Namen und eine einzige Kennung kann die Data Insights Agent Datenansichten wechseln, ohne den Kontext zu verlieren.

>[!MORELIKETHIS]
>
>[Komponenteneinstellungen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/overview)
>[Datenwörterbuch](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/data-dictionary/data-dictionary-overview)
>[Berechnete Metrik genehmigen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-approving)
>[Segmente freigeben](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/segments/seg-share)
