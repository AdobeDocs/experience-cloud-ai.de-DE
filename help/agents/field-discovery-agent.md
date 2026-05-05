---
title: Field Discovery Agent
description: Suchen, Auswerten und Auswählen von XDM-Feldern in Adobe Experience Platform mithilfe der natürlichen Sprache im KI-Assistenten, mit Rangergebnissen, Beispielwerten und Nutzungskontext für Segmentierungs-, Abfrage- und Daten-Workflows.
keywords: Felderkennung, XDM, KI-Assistent, Experience Platform-Agenten, Entitätsverknüpfung, Felderempfehlungen, Zielgruppenerstellung, Segmentierung
solution: Experience Platform
role: User, Admin, Developer
source-git-commit: b4d8c83cca73a19e1fe229c8cec03caee16bcd8c
workflow-type: tm+mt
source-wordcount: '3525'
ht-degree: 1%

---

# Field Discovery Agent

Beim Erstellen von Zielgruppen oder Onboarding-Daten in Adobe Experience Platform ist es oft erforderlich, Schemas manuell zu durchsuchen oder im Voraus genau zu wissen, wie ein Feld benannt wird, um das richtige XDM-Feld für ein Geschäftskonzept zu identifizieren. Verschiedene Felder können dasselbe Konzept unter verschiedenen Namen darstellen, z. B. Bundesland, Region und Ort, und die Auswahl des falschen führt zu Fehlern in nachgelagerten Workflows.

Der Field Discovery Agent ist ein KI-gestützter Agent in Adobe Experience Platform, mit dem Sie XDM-Felder mithilfe von Abfragen in natürlicher Sprache im KI-Assistenten suchen, auswerten und auswählen können. Sie beschreiben, wonach Sie suchen, in einfacher Sprache - ein Geschäftskonzept, ein Workflow-Ziel oder ein bestimmter Feldname - und der Agent gibt Rangfolgenfeldempfehlungen mit unterstützendem Kontext zurück.

Der Felderkennungs-Agent wird im KI-Assistenten automatisch im Hintergrund aufgerufen, wenn andere Experience Platform-Agenten Feld- oder Entitätsverweise auflösen müssen. In diesen Fällen arbeitet sie im Hintergrund, um die Genauigkeit des Agenten, mit dem Sie arbeiten, zu verbessern. Wenn Sie die Felderkennung für Ihre eigene Arbeit benötigen, schreiben Sie eine explizite Eingabeaufforderung zur Feldsuche im KI-Assistenten. Der Field Discovery Agent zeigt nur Feldinformationen an. Schemas, Datensätze oder Zielgruppen werden nicht geändert, und die vorhandenen Zugriffssteuerungen und der Sandbox-Kontext werden berücksichtigt.

## Verwendungszeitpunkt {#when-to-use-this}

Verwenden Sie den Felderkennungsagenten explizit im KI-Assistenten, wenn Sie Rangfolgenfeldempfehlungen, Beispielwerte und den Nutzungskontext für eine Zuordnung, Segmentierung oder Abfrage benötigen. Sie wird implizit verwendet, wenn ein anderer Experience Platform-Agent sie im Hintergrund aufruft, um Feld- oder Entitätsverweise aufzulösen. In diesen Fällen bleiben Sie im Workflow dieses Agenten und geben keine separate Eingabeaufforderung zur Feldsuche aus.

## Voraussetzungen {#prerequisites}

Um den Field Discovery Agent zu verwenden, benötigen Sie Folgendes:

- Zugriff auf Adobe Experience Platform und den KI-Assistenten
- Die richtige Organisation und Sandbox
- Zugriff auf die Schemata und Datensätze, die Sie abfragen möchten

Eine grundlegende Vertrautheit mit XDM-Schemata und der Verwendung von Feldern in Segmentierungs- oder Daten-Workflows kann Ihnen dabei helfen, die Ergebnisse effektiver zu interpretieren. Weitere Informationen finden Sie unter [XDM-Übersicht](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/home) und [Dokumentation zum Schema-Editor](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/tutorials/create-schema-ui).

Anweisungen zum Aktivieren des Zugriffs auf den KI-Assistenten und zum Gewähren der erforderlichen Berechtigungen finden Sie im [Agent Orchestrator-Zugriffshandbuch](./agent-orchestrator.md#access).

## Funktionen des Field Discovery Agents {#field-discovery-agent-functions}

Der Field Discovery Agent verarbeitet Ihre Abfrage und gibt abhängig von Ihrer Absicht einen von drei Ausgabetypen zurück. Diese Funktionen spiegeln wider, wie der Agent Ihre Abfrage interpretiert; Sie wählen sie nicht aus. Der Agent bestimmt den entsprechenden Antworttyp automatisch anhand Ihrer Beschreibung.

| Funktion | Beschreibung | Erwartete Ausgabe |
| --- | --- | --- |
| **Identifikation** | kennzeichnet XDM-Felder, die semantisch einem Geschäftskonzept oder -attribut entsprechen, das Sie in natürlicher Sprache beschreiben. | Eine Rangliste von möglichen Feldern mit Links zu Relevanzkennzeichnungen, Feldpfaden und Nutzungskontexten. |
| **Empfehlung** | empfiehlt XDM-Felder basierend auf einem von Ihnen beschriebenen Workflow-Ziel oder Anwendungsfall, z. B. Erstellen eines Zielgruppensegments oder Modellieren eines Verhaltensattributs. | Eine priorisierte Liste von Feldern, die für das angegebene Ziel relevant sind, mit jeweils relevantem Kontext. |
| **Anreicherung** | Gibt einen detaillierten Kontext für ein bestimmtes Feld zurück, einschließlich Beispielwerten, Schemaspeicherort und der Stelle, an der das Feld über Datensätze, Zielgruppen und Ziele hinweg verwendet wird. | Felddetails, einschließlich Beispielwerte, Schemapfad, verknüpfte Datensätze und Zielgruppen- oder Zielverwendung. |

## Funktionsweise des Field Discovery Agent {#how-field-discovery-agent-works}

Auf allgemeiner Ebene interpretiert der Agent Ihre Absicht, durchsucht Ihre verfügbaren Daten und ordnet die Ergebnisse nach Relevanz. Die Formulierung Ihrer Abfrage wirkt sich direkt auf jedes Stadium aus, was sich wiederum auf die Qualität der Ergebnisse auswirkt.

Wenn Sie eine Abfrage im KI-Assistenten senden, verarbeitet der Field Discovery Agent Ihre Anfrage in drei Schritten:

| Staging | Beschreibung |
|------|-------------|
| **Intent-Interpretation** | Der Agent liest Ihre Eingabe in natürlicher Sprache und identifiziert das zugrunde liegende Konzept oder Ziel. Beispielsweise wird eine Abfrage über „Personen in Kalifornien“ als geografische Attributanfrage interpretiert und nicht als wörtliche Zeichenfolgenübereinstimmung. Der Agent ordnet Ihre Formulierungen semantisch äquivalenten Konzepten zu, die unter verschiedenen Namen in Ihren Schemata erscheinen können. |
| **Suchbereich** | Der Agent durchsucht die XDM-Schemata, Datensätze und Feldmetadaten, die in Ihrer aktuellen IMS-Organisation und Sandbox verfügbar sind. Dabei werden Feldnamen, Anzeigenamen, Beschreibungen und Nutzungsverknüpfungen berücksichtigt, um Kandidaten zu finden, die Ihrer Absicht entsprechen. |
| **Rangfolge** | Der Agent ordnet die Ergebnisse nach semantischer Relevanz - wie genau ein Feld mit Ihrer angegebenen Absicht übereinstimmt - ergänzt durch Signale wie Metadaten-Vollständigkeit und Feldnutzung in Ihrem gesamten Daten-Ökosystem. Felder mit beschreibenden Namen, ausgefüllten Metadaten und bestätigter Verwendung in aktiven Datensätzen haben einen höheren Rang als Felder, die nur in einer Schemadefinition vorhanden sind. Der Agent legt die den einzelnen Signalen zugeordneten spezifischen Gewichte nicht offen. |

## Wissenswertes zu Ergebnissen {#understand-your-results}

Der Field Discovery Agent gibt für jede Abfrage einen strukturierten Ergebnissatz zurück. Wenn Sie die Komponenten eines Ergebnisses verstehen, können Sie mögliche Felder auswerten und mit Konfidenz darauf reagieren, ohne dass Sie zusätzliche Versuche und Fehler machen müssen.

Felder als einsatzbereit behandeln, wenn ihre Bezeichnung **[!UICONTROL Relevanz]** &quot;**[!UICONTROL Relevanz“]**, ihre Beispielwerte mit den erwarteten Daten (falls verfügbar) übereinstimmen und ihre **[!UICONTROL Nutzungskontexte]** an der geplanten Verwendung ausgerichtet sind. Wenn die Ergebnisse nur **[!UICONTROL mäßig relevant]** oder **[!UICONTROL relevant]**, die Beispielwerte nicht Ihren Erwartungen entsprechen oder der Nutzungskontext begrenzt ist, verfeinern Sie Ihre Abfrage und überprüfen Sie einen neuen Ergebnissatz, bevor Sie fortfahren.

### Relevanzkennzeichnungen

Der Felderkennungs-Agent weist jedem Feldergebnis in der Spalte **[!UICONTROL Relevanz]** des Bedienfelds **[!UICONTROL Identifizierte Felder]** einen Relevanztitel zu, der angibt, wie genau das Feld mit Ihrer Abfrage übereinstimmt.

- **[!UICONTROL Höchste Relevanz]** - Das Feld entspricht basierend auf seinem Namen, den Metadaten und den Nutzungssignalen deutlich Ihrem angegebenen Konzept. Bestätigen Sie den Feldpfad und überprüfen Sie die Beispielwerte, um sicherzustellen, dass er die erwarteten Daten enthält.
- **[!UICONTROL Mäßig relevant]** - Das Feld weist eine teilweise semantische Überschneidung mit Ihrer Abfrage auf, kann sich jedoch in Umfang, Datentyp oder Spezifität unterscheiden. Überprüfen Sie die Beispielwerte und den Nutzungskontext, um festzustellen, ob er Ihren Anforderungen entspricht, bevor Sie ihn auswählen.
- **[!UICONTROL Relevant]** - Das Feld stimmt teilweise mit Ihrer Abfrage überein. Sie kann semantische Überschneidungen aufweisen, sich aber in Umfang, Spezifität oder Datentyp unterscheiden. Überprüfen Sie die Beispielwerte und den Nutzungskontext, bevor Sie entscheiden, ob Sie sie verwenden möchten.

Wenn alle Ergebnisse eher als **[!UICONTROL mäßig relevant]** oder **[!UICONTROL relevant]** und nicht **[!UICONTROL hoch relevant]** gekennzeichnet sind, ist Ihre Abfrage möglicherweise zu breit angelegt oder verwendet eine Terminologie, die nicht mit Ihren Schema-Metadaten übereinstimmt. Verfeinern Sie Ihre Eingabeaufforderung mit spezifischeren Sprach- oder Domain-Begriffen, die widerspiegeln, wie Ihre Felder benannt sind.

### Beispielwerte

Neben jedem Feldvorschlag zeigt der Felderkennungs-Agent Beispielwerte an, die aus den Felddaten in Ihrer Sandbox abgerufen wurden. Mit Beispielwerten können Sie vor der Auswahl überprüfen, ob ein Feld den erwarteten Datentyp enthält.

>[!IMPORTANT]
>
>Beispielwerte können personenbezogene Daten enthalten. Geben Sie sie nicht außerhalb sicherer interner Workflows frei.

Beispielwerte sind nur für Felder innerhalb Ihrer Datensatzzugriffsberechtigungen sichtbar. Informationen zu Data Governance und Nutzungsbeschränkungen in Experience Platform finden Sie unter [Data Governance - Übersicht](https://experienceleague.adobe.com/de/docs/experience-platform/data-governance/home).

Wenn für ein Feld keine Beispielwerte angezeigt werden, kann das Feld in der aktuellen Sandbox leer sein oder Ihre Berechtigungen umfassen möglicherweise nicht den Zugriff auf den zugrunde liegenden Datensatz. Felder mit hoher Kardinalität (z. B. Kennungs- oder UUID-Felder) geben möglicherweise auch keine repräsentativen Beispielwerte zurück. Die Beispielwerte werden aggregiert und sind frequenzbasiert und nicht auf einzelne Profile zurückzuführen.

### Nutzungskontext

Jedes Feldergebnis enthält einen Nutzungskontext, der anzeigt, wo das Feld in Ihrem gesamten Daten-Ökosystem angezeigt wird:

**Zielgruppe → Datensatz → Ziel → Schema**

Ein Feld, das in einer veröffentlichten Zielgruppe verwendet wird, in einem aktiven Datensatz angezeigt wird, einem Live-Ziel zugeordnet wird und in einem Schema definiert ist, das eine reale Nutzung in Ihrer Umgebung gezeigt hat. Dadurch werden Felder, auf die aktiv zurückgegriffen wird, von Feldern unterschieden, die nur in einer Schemadefinition vorhanden sind, aber in der Praxis nicht verwendet wurden. Verwenden Sie dieses Signal zusammen mit der Relevanzbeschriftung und den Beispielwerten, um eine fundiertere Feldauswahl zu erzielen.

### Ergebnisse im KI-Assistenten

Der Felderkennungsagent gibt Ergebnisse in einem Bedienfeld **[!UICONTROL Felder identifiziert]** innerhalb der Antwort des KI-Assistenten zurück. Das Bedienfeld zeigt eine Tabelle mit drei Spalten an:

- **[!UICONTROL Feldname]** - Der XDM-Pfad des Kandidatenfelds.
- **[!UICONTROL Relevanz]** — Die dem Feld zugewiesene Relevanzkennzeichnung (**[!UICONTROL Sehr relevant]**, **[!UICONTROL Mäßig relevant]** oder **[!UICONTROL Relevant]**)
- **[!UICONTROL Nutzungskontexte]** - Links, die zeigen, wo das Feld in Ihrem gesamten Daten-Ökosystem angezeigt wird. Wählen Sie **[!UICONTROL Audience]**, **[!UICONTROL Datensatz]**, **[!UICONTROL Ziel]** oder **[!UICONTROL Schema]** aus, um einen Seitenbereich zu öffnen, der anzeigt, wo das Feld verwendet wird.

![Das Bedienfeld „Identifizierte Felder“ im KI-Assistenten, das Kandidatenfelderzeilen mit Relevanzkennzeichnungen und Links zu Nutzungskontexten anzeigt.](./images/field-discovery/fields-identified-panel-in-chat.png)

Ein **[!UICONTROL Ergebnisse erläutert]** wird unterhalb der Tabelle **[!UICONTROL Felder]** angezeigt und bietet zusätzlichen Kontext auf Feldebene, einschließlich Erläuterungen und unterstützenden Details für jedes Ergebnis. Eine Anleitung zum Navigieren in der Benutzeroberfläche des KI-Assistenten finden Sie im [Handbuch zur Benutzeroberfläche des KI-Assistenten](../ai-assistant/ai-assistant-ui.md).

## Verwenden des Felderkennungsagenten {#use-field-discovery-agent}

Die Interaktion mit dem Field Discovery Agent erfolgt über den KI-Assistenten in natürlicher Sprache. Der Agent erfordert eine klare Absichtserklärung. Eine vage oder zu kurze Abfrage liefert Ergebnisse von geringerer Qualität oder ruft den Felderkennungsagenten möglicherweise überhaupt nicht auf.

Für eine explizite Felderkennung führen Sie diesen Workflow aus: Identifizieren Sie das Attribut- oder Zuordnungsproblem, senden Sie eine Feldsuchabfrage, überprüfen Sie die Rang-Ergebnisse und den Nutzungskontext im Bedienfeld **[!UICONTROL Identifizierte Felder]**, wählen Sie den **[!UICONTROL Feldname]**-Pfad aus, der zu Ihrer Absicht passt, und wenden Sie diesen XDM-Pfad in Segment Builder, Query Service oder einem anderen Workflow an.

So verwenden Sie den Felderkennungsagenten:

1. Navigieren Sie von **[!UICONTROL aktivierten Experience Platform]** Anwendung zum KI-Assistenten. Der **[!UICONTROL KI-Assistent]**-Arbeitsbereich wird angezeigt.
2. Geben Sie Ihre Absicht explizit im Eingabefeld an. Beschreiben Sie das gesuchte Konzept, Ziel oder Feldmerkmal. Beispiel: *„Felder im Zusammenhang mit dem Kunden-E-Mail-Opt-out-Status suchen.“*
3. Überprüfen Sie die Ergebnisse der Rangfolge im Bedienfeld **[!UICONTROL Identifizierte Felder]**. Jede Zeile enthält eine Relevanzbeschriftung und einen XDM-Feldpfad in der Spalte **[!UICONTROL Feldname]**.
4. Wählen Sie **[!UICONTROL Audience]**, **[!UICONTROL Dataset]**, **[!UICONTROL Destination]** oder **[!UICONTROL schema]** in der Spalte **[!UICONTROL Usage Contexts]** aus, um einen Seitenbereich zu öffnen, in dem das Feld verwendet wird. Weitere Informationen zu Kontext auf Feldebene finden Sie im Abschnitt **[!UICONTROL Ergebnisse]** Erklärung) unter der Ergebnistabelle.

   ![Seitenbereich im KI-Assistenten, der Nutzungskontexte für ein ausgewähltes Feld anzeigt, einschließlich Zielgruppen-, Datensatz-, Ziel- und Schemaverknüpfungen.](./images/field-discovery/fields-identified-panel-expanded.png)

5. Verwenden Sie den **[!UICONTROL Feldname]**-Pfad je nach Anwendungsfall in nachgelagerten Tools wie Segment Builder, Abfrage-Service oder Datenaufnahme-Workflows. Der Field Discovery Agent stellt die Feldreferenz bereit, fügt sie jedoch nicht in andere Tools ein.

Wählen Sie bei Bedarf das Dropdown-**[!UICONTROL „Reasoning complete]** über der Antwort aus, um zu bestätigen, dass der Field Discovery Agent Ihre Anfrage verarbeitet hat. Das Dropdown-Menü enthält Argumentationsdetails, die angeben, welcher Agent aufgerufen wurde.

>[!NOTE]
>
>Wenn im Begründungsbereich kein Field Discovery Agent angezeigt wird, enthält Ihre Abfrage möglicherweise keine eindeutige Felderkennungsabsicht. Stellen Sie Ihre Abfrage mit der expliziten Feldsuchsprache erneut her und senden Sie sie erneut. Siehe [Fehlerbehebung](#troubleshooting) für häufige Aufrufprobleme.

Eine Anleitung zur Benutzeroberfläche des KI-Assistenten finden Sie im [Handbuch zur Benutzeroberfläche des KI-Assistenten](../ai-assistant/ai-assistant-ui.md).

## Unterstützte Anwendungsfälle {#supported-use-cases}

In den folgenden Abschnitten werden die drei Funktionen des Field Discovery Agents mit repräsentativen Szenarien und Beispielaufforderungen beschrieben. Zu den Ergebnissen gehören Relevanzkennzeichnungen und Nutzungskontext, die bei der Bewertung von Feldern hilfreich sind. Informationen zur Interpretation der Ergebnisse finden [&#x200B; unter „Wissenswertes zu Ergebnissen](#understand-your-results). Der Felderkennungs-Agent gibt nur Feldinformationen zurück: Er erstellt keine Zielgruppen, führt keine Abfragen aus und überträgt keine Daten in andere Tools. Nachdem Sie ein Feld identifiziert haben, lesen Sie seinen XDM-Pfad aus der Spalte **[!UICONTROL Feldname]** und verwenden Sie ihn in Ihrem nachgelagerten Workflow.

### Identifizieren von Feldern für ein Geschäftskonzept

Wenn Sie ein bestimmtes Datenkonzept oder -attribut beschreiben, gibt der Felderkennungsagent eine Rangliste von Feldern zurück, die semantisch Ihrer Beschreibung entsprechen.

> „Welche Felder repräsentieren den Bundesstaat oder die Provinz eines Kunden?“
> „Suchen Sie Felder, die sich auf das Kauftransaktionsdatum beziehen.“
> „Welche Felder enthalten Informationen zum E-Mail-Marketing-Einverständnis?“

Die Antwort listet mögliche Felder mit ihrer Relevanzbezeichnung und dem XDM-Pfad im Bedienfeld **[!UICONTROL Felder identifiziert]** auf. Die mit **[!UICONTROL Sehr relevant]** gekennzeichneten Felder entsprechen am ehesten Ihrem angegebenen Konzept. Wenn die obersten Ergebnisse eher als **[!UICONTROL mäßig relevant]** oder **[!UICONTROL relevant]** und nicht **[!UICONTROL hoch relevant]** gekennzeichnet sind, verfeinern Sie Ihre Abfrage mithilfe einer spezifischeren Terminologie oder eines Kontexts auf Feldebene.

### Abrufen von Feldempfehlungen für einen Anwendungsfall

Wenn Sie ein Workflow-Ziel oder einen Anwendungsfall beschreiben - z. B. das Erstellen eines Segments, das Onboarding eines Datensatzes oder das Vorbereiten einer Abfrage - empfiehlt der Felderkennungs-Agent Felder, die an diesem Ziel ausgerichtet sind und nach Relevanz priorisiert sind.

> „Ich möchte eine Audience mit hochwertigen Kunden aufbauen. Welche Felder sollte ich verwenden?“
> „Empfehlen Sie Felder zur Modellierung der Kaufneigung.“
> „Welche Felder sollte ich beim Onboarding eines Einzelhandelstransaktionsdatensatzes einbeziehen?“

Die Antwort gibt eine priorisierte Liste von Feldern mit Relevanzkontext zurück. Überprüfen Sie den Nutzungskontext für jedes empfohlene Feld, um sicherzustellen, dass es aktiv in Ihrer Umgebung verwendet wird.

### Feldkontext anreichern

Wenn Sie ein bestimmtes Feld nach Name oder Pfad fragen, gibt der Felderkennungs-Agent einen detaillierten Kontext für dieses Feld zurück, einschließlich Beispielwerten, Schemaspeicherort und Verwendung in Datensätzen, Zielgruppen und Zielen.

> „Erzähl mir mehr über die `person.name.lastName`.“
> „Welche Beispielwerte gibt es für `homeAddress.stateProvince`?“
> „Wo wird das Feld in meinen Datensätzen und Audiences verwendet`commerce.purchases.value`&quot;

Die Antwort gibt die Beispielwerte des Felds, den Speicherort des Schemas, die zugehörigen Datensätze und alle Zielgruppen oder Ziele zurück, in denen das Feld angezeigt wird. Überprüfen Sie diesen Kontext, um zu bestätigen, dass das Feld die erwarteten Daten enthält.

## Im Umfang und außerhalb des Bereichs {#in-scope-and-out-of-scope}

In diesem Abschnitt wird zusammengefasst, was der Field Discovery Agent tun kann und was nicht. Detaillierte Aufgabenanleitungen finden Sie unter [Unterstützte Anwendungsfälle](#supported-use-cases). Informationen zu Plattformeinschränkungen finden Sie unter [Leitplanken und Einschränkungen](#guardrails-and-limitations).

### Im Umfang

In der folgenden Liste werden die Aufgaben beschrieben, die der Field Discovery Agent ausführen kann. Anhand dieser Aufgabe können Sie prüfen, ob der Agent Ihrer Anforderung nachkommen kann, bevor Sie sich in Ihrem Workflow darauf verlassen.

- Identifizieren von XDM-Feldern, die einem Geschäftskonzept oder einer Beschreibung natürlicher Sprache entsprechen.
- Empfohlene Felder für ein angegebenes Workflow-Ziel oder einen angegebenen Anwendungsfall.
- Anreichern eines bestimmten Felds mit Beispielwerten, Schemaspeicherort und Nutzungskontext.
- Nach semantischer Relevanz sortierte Ergebnisse, die als „hochrelevant“, „mäßig relevant“ oder „relevant“ gekennzeichnet sind.
- Aufdecken von Beispielwerten innerhalb Ihrer autorisierten Datensatzberechtigungen.

### Außerhalb des Geltungsbereichs

In der folgenden Liste werden Aktionen beschrieben, die der Field Discovery Agent nicht ausführt. Verwenden Sie die Liste, um zu vermeiden, dass der Agent für Aufgaben außerhalb seines Bereichs erforderlich ist.

- Ändern von Schemata, Datensätzen, Feldern oder Zielgruppen.
- Erstellen oder veröffentlichen Sie Zielgruppen oder Segmente.
- Führen Sie Abfragen aus oder aktivieren Sie Daten für Ziele.
- Zugriff auf Felder oder Datensätze außerhalb Ihrer autorisierten Berechtigungen.
- Offenlegung interner Einbettungslogik, Vektordatenbankarchitektur oder Entitätsverknüpfungs-Implementierungsdetails.
- Garantie eines bestimmten Zeitfensters für Wissensdatenbankaktualisierungen nach Schema- oder Datensatzänderungen.

## Leitlinien und Einschränkungen {#guardrails-and-limitations}

Diese Leitplanken sind wichtig, da der Field Discovery Agent innerhalb von Beschränkungen auf Plattformebene arbeitet, die die Verfügbarkeit und Qualität der Ergebnisse beeinflussen. Verwenden Sie sie, um fehlende, verzögerte oder unvollständige Ergebnisse zu interpretieren und unerwartete Lücken mit realistischen Erwartungen zu beheben.

### Knowledgebase

Der Field Discovery Agent basiert auf einer Wissensdatenbank, die regelmäßig mit Schemas und Metadaten aus Ihrer Experience Platform-Umgebung aktualisiert wird. Die Ergebnisse spiegeln den Status der Wissensdatenbank zum Zeitpunkt Ihrer Abfrage wider - nicht den Echtzeitstatus Ihrer Schemas. Außerdem kann es zu einer Verzögerung zwischen der Datenaufnahme und dem Zeitpunkt kommen, zu dem sie im Agenten angezeigt wird.

Neue Schemata, Felder oder Datensätze, die Ihrer Umgebung hinzugefügt wurden, werden möglicherweise nicht sofort in den Ergebnissen des Field Discovery Agent angezeigt. Es kann einige Zeit dauern, bis die Ergebnisse die jüngsten Änderungen widerspiegeln.

>[!NOTE]
>
>Das Aktualisierungsintervall für die Wissensdatenbank kann sich ändern. Wenn ein kürzlich hinzugefügtes Feld nicht in den Ergebnissen angezeigt wird, warten Sie, bis die Wissensdatenbank aktualisiert wurde, und senden Sie dann Ihre Abfrage erneut.

### Qualität und Abdeckung von Metadaten

Die Ergebnisqualität hängt von der Qualität und Vollständigkeit der Feldmetadaten in Ihrer Experience Platform-Umgebung ab. Der Agent verwendet Feldnamen, Anzeigenamen, Beschreibungen und Nutzungsverknüpfungen, um die Ergebnisse zu reihen. Felder mit unzureichenden oder fehlenden Metadaten werden möglicherweise nicht in den Ergebnissen angezeigt oder rangieren möglicherweise niedriger als erwartet.

Wenn Sie Zugriff auf die Schemabearbeitung haben, können Sie die Ergebnisqualität verbessern, indem Sie:

- Verwenden klarer, beschreibender Anzeigenamen für Felder in Ihren Schemata.
- Hinzufügen von Feldbeschreibungen, sofern möglich.
- Verknüpfen von Feldern mit aktiven Datensätzen, anstatt sie als schreibgeschützte Schemadefinitionen zu belassen.

Anleitungen für die Bearbeitung von Anzeigenamen und Beschreibungen von Feldern im Schema-Editor finden Sie unter [Erstellen und Bearbeiten von Schemas in der Benutzeroberfläche](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/ui/resources/schemas).

Wenn Sie keinen Zugriff auf die Schemabearbeitung haben und die Ergebnisse durchgängig schlecht sind, wenden Sie sich an Ihren Experience Platform-Administrator oder Ihr Data Engineering-Team, um die Feldmetadaten für die Schemata zu überprüfen, mit denen Sie arbeiten.

### Zugriffs- und PII-Einschränkungen

Der Field Discovery Agent berücksichtigt alle vorhandenen Experience Platform-Zugriffssteuerungen und arbeitet innerhalb Ihres aktuellen Sandbox-Kontexts. Sie erhalten nur Ergebnisse für Felder in Schemata und Datensätzen, auf die Sie zugreifen dürfen.

Beispielwerte werden von denselben Berechtigungen auf Datensatzebene gesteuert. Felder in profilaktivierten Datensätzen mit PII-Einschränkungen geben Beispielwerte nur zurück, wenn Sie über den erforderlichen Zugriff verfügen. Siehe [Beispielwerte](#sample-values) für die Handhabung. Der Field Discovery Agent umgeht keine Sicherheitseinstellungen auf Feldebene oder profilaktivierte Zugriffsbeschränkungen.

## Best Practices {#best-practices}

Verwenden Sie die folgenden Anleitungen, um genaue, verwertbare Ergebnisse vom Field Discovery Agent zu erhalten.

- **Geben Sie nicht nur den Feldtyp an, sondern das Konzept** Eine Eingabeaufforderung wie „Nach einem Bundesland suchen“ liefert schlechtere Ergebnisse als „Nach dem Feld suchen, das den US-Bundesstaat einer Kundin oder eines Kunden für die geografische Segmentierung enthält“. Durch die Spezifität erhält der Agent ein stärkeres Signal, das mit Ihren Metadaten abgeglichen werden kann. Warum [&#x200B; wichtig ist, erfahren Sie &#x200B;](#how-field-discovery-agent-works) „Funktionsweise des Field Discovery Agent“.
- **Verwenden Sie die Terminologie, die Ihren Schemadateien entspricht.** Wenn Ihre Schemata den Begriff „Transaktion“ anstelle von „Kauf“ verwenden, verwenden Sie in Ihren Eingabeaufforderungen „Transaktion“. Der Agent gleicht tatsächliche Feldnamen und Beschreibungen ab, nicht nur allgemeine Konzepte.
- **Felder vor dem Commit überprüfen.** Nachdem Sie mögliche Felder gefunden haben, fragen Sie nach einem bestimmten Feld anhand des Namens oder Pfads, um dessen Beispielwerte und den Nutzungskontext zu überprüfen, bevor Sie es in einem Segment oder einer Abfrage verwenden. Dadurch verringert sich das Risiko, das falsche Feld auszuwählen.
- **Iterieren Sie, wenn die Ergebnisse eher mäßig relevant oder relevant als hoch relevant sind.** Formulieren Sie Ihre Abfrage mit einer anderen Terminologie oder fügen Sie mehr Kontext zu Ihrem Anwendungsfall hinzu. Eine zweite, spezifischere Abfrage taucht oft als bessere Kandidaten auf.
- **Den Bereichskontext in die Eingabeaufforderungen einbeziehen.** Schließen Sie bei der geobasierten Segmentierung die Zielregion ein. Schließen Sie bei zeitbasierten Abfragen das Zeitattribut ein. Je mehr Kontext Sie angeben, desto zielgerichteter ist das Ergebnis-Ranking.

## Beispiel-Eingabeaufforderungen {#example-prompts}

Verwenden Sie diesen Abschnitt als Bibliothek mit einer Eingabeaufforderung als Schnellverweis. Wenn Sie mit dem Field Discovery Agent noch nicht vertraut sind, lesen Sie zunächst [Best Practices](#best-practices) und [Unterstützte Anwendungsfälle](#supported-use-cases) um zu verstehen, wann und warum jede Funktion gilt.

### Eingabeaufforderungen zur Identifizierung

Verwenden Sie diese Eingabeaufforderungen, wenn Sie das benötigte Datenkonzept kennen, aber nicht wissen, welches Feld es enthält.

> „Welches Feld enthält den Bundesstaat oder die Region eines Kunden?“
> „Felder zum E-Mail-Abonnementstatus finden.“
> „Welches Feld enthält das Datum des ersten Kaufs eines Kunden?“
> „Identifizieren Sie Felder, die den Kundenlebenszeitwert darstellen.“
> „Welche Felder in meinem Profilschema beziehen sich auf die Mitgliedschaft im Treueprogramm?“

### Eingabeaufforderungen zur Empfehlung

Verwenden Sie diese Eingabeaufforderungen, wenn Sie einen Workflow starten und Anleitungen benötigen, welche Felder für ein bestimmtes Ziel eingeschlossen werden sollen.

> „Welche Felder sollte ich verwenden, um eine Zielgruppe für die erneute Interaktion zu erstellen?“
> „Empfehlungsfelder für eine Zielgruppe, die sich an Kunden richten, die seit 90 Tagen keinen Kauf getätigt haben.“
> „Welche Felder sind am nützlichsten für die Modellierung des Abwanderungsrisikos?“
> „Vorschläge für Felder, die ich bei der Erstellung einer geografischen Segmentierung einbeziehen sollte.“
> „Ich baue ein Modell mit einer Kaufneigung auf. Mit welchen Feldern soll ich beginnen?“

### Eingabeaufforderungen zur Anreicherung

Verwenden Sie diese Eingabeaufforderungen, wenn Sie ein Kandidatenfeld haben und es überprüfen möchten, bevor Sie es in einem Segment, einer Abfrage oder einer Zuordnung verwenden.

> „Erzähl mir mehr über `homeAddress.stateProvince`.“
> „Beispielwerte für `commerce.purchases.value` anzeigen.“
> „Wo wird `person.name.lastName` in meinen Datensätzen und Audiences verwendet?“
> „Welche Datensätze enthalten die `web.webPageDetails.URL`?“
> „Ist `segmentMembership` aktiven Zielen zugeordnet?“

## Fehlerbehebung {#troubleshooting}

Verwenden Sie diesen Abschnitt, wenn Ergebnisse fehlen oder unerwartet auftreten oder wenn Sie sich nicht sicher sind, ob der Field Discovery Agent Ihre Anfrage verarbeitet hat.

- **Ein kürzlich hinzugefügtes Feld wird nicht in den Ergebnissen angezeigt.** Die Wissensdatenbank spiegelt möglicherweise noch nicht das neue Schema oder Feld wider. Warten Sie einige Zeit, bis die Wissensdatenbank aktualisiert wurde, nachdem Sie Schemata oder Felder zu Ihrer Umgebung hinzugefügt haben, und senden Sie dann Ihre Abfrage erneut. Siehe [Wissensdatenbank](#knowledge-base).

- **Alle Ergebnisse sind eher als mäßig relevant oder relevant und nicht als hoch relevant gekennzeichnet.** Ihre Abfrage ist möglicherweise zu umfangreich oder die verwendete Terminologie stimmt möglicherweise nicht mit Ihren Feldmetadaten überein. Verfeinern Sie Ihre Eingabeaufforderung mit einer spezifischeren Sprache oder spezifischeren Begriffen, die mit der Art und Weise übereinstimmen, wie Ihre Felder in Ihren Schemata benannt sind. Siehe [Best Practices](#best-practices).

- **Der Felderkennungs-Agent wurde nicht aufgerufen.** Sie haben eine Abfrage im KI-Assistenten gesendet, aber im Bedienfeld **[!UICONTROL Begründung abgeschlossen]** wird kein Felderkennungsagent angegeben. Ihre Abfrage enthält möglicherweise keine eindeutige Felderkennungsabsicht. Stellen Sie Ihre Abfrage explizit neu dar - z. B. „Suchen Sie das Feld, das den Kunden-E-Mail-Opt-out-Status enthält“ - und senden Sie sie erneut. Siehe [Verwenden des Field Discovery Agent](#use-field-discovery-agent).

- **Beispielwerte werden für ein Feld nicht angezeigt.** Das Feld kann in der aktuellen Sandbox leer sein, Ihre Berechtigungen können keinen Zugriff auf den zugrunde liegenden Datensatz enthalten oder das Feld kann eine hohe Kardinalität aufweisen (z. B. ein ID-Feld), für das keine Beispielwerte angezeigt werden. Bestätigen Sie Ihre Zugriffsberechtigungen für den Datensatz und stellen Sie sicher, dass das Feld mit Daten gefüllt wird. Siehe [Zugriffs- und PII-Beschränkungen](#access-and-pii-constraints).

- **Die Ergebnisse enthalten Felder aus Schemata, die Sie nicht erwartet haben.** Der Field Discovery Agent durchsucht alle Schemas und Datensätze in der aktuellen Sandbox, auf die mit Ihren Berechtigungen zugegriffen werden kann. Wenn unerwartete Ergebnisse auftreten, bestätigen Sie Ihren aktiven Sandbox-Kontext im KI-Assistenten und überprüfen Sie, welche Schemas und Datensätze für Ihre Rolle zugänglich sind.

Um zu überprüfen, welcher Agent Ihre Anfrage verarbeitet hat, lesen Sie Schritt 6 in [Verwenden des Field Discovery Agent](#use-field-discovery-agent).
