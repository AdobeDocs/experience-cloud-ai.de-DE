---
title: Adobe Marketing Agent for Microsoft 365 Copilot
description: Erfahren Sie, wie Sie die Adobe Marketing Agent for Microsoft 365 Copilot verwenden können.
source-git-commit: 5cf5e42c727cd5e48b1b817e150fb9862fc80c82
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# Adobe Marketing Agent für [!DNL Microsoft 365 Copilot]

Adobe Marketing Agent for [!DNL Microsoft 365 Copilot] ist ein KI-gestütztes Tool, das Adobe Experience Platform direkt mit [!DNL Microsoft 365 Copilot] verbindet. Mit diesem Agenten können Sie Fragen in natürlicher Sprache in [!DNL Microsoft 365] Anwendungen wie [!DNL Teams], [!DNL Word], [!DNL Powerpoint] und [!DNL Excel] stellen, um sofort Marketing-Erkenntnisse aus Experience Platform abzurufen, ohne Ihren Workflow zu unterbrechen. Derselbe Agent ist in diesen Apps verfügbar, und Ihr Chat-Verlauf mit der Adobe Marketing Agent wird übernommen. So können Sie z. B. in [!DNL Copilot] in [!DNL Teams] recherchieren und das Gespräch in [!DNL Word] oder [!DNL Powerpoint] fortsetzen, während Sie einen Kampagnenbericht entwerfen oder eine Präsentation überprüfen.

Mit Adobe Marketing Agent for [!DNL Microsoft 365 Copilot] können Marketing-Manager, Analyse- und Insights-Teams und Stakeholder:

- Treffen Sie schnellere, datengesteuerte Marketing-Entscheidungen.
- Weniger Zeitaufwand beim Wechseln zwischen Tools
- Vereinfachen des Zugriffs auf Zielgruppen- und Journey-Einblicke für alle Teams.

## Funktionsweise des Agenten

>[!IMPORTANT]
>
>Adobe Marketing Agent für [!DNL Microsoft 365 Copilot] unterstützt derzeit Experience Platform Operational Insights, Customer Journey Analytics Data Insights, Audience Agent und Journey Agent.

Adobe Marketing Agent for [!DNL Microsoft 365 Copilot] bietet ein integriertes Erlebnis zwischen Experience Platform und [!DNL Microsoft 365]:

- Adobe Marketing Agent wird in [!DNL Microsoft 365 Copilot] als Agent angezeigt, einschließlich in [!DNL Teams], [!DNL Word], [!DNL Powerpoint] und [!DNL Excel].
- Melden Sie sich mit Ihrem Adobe-Konto an und wählen Sie die Datenumgebung (Sandbox, Datenansicht) aus, die Sie verwenden möchten.

### Datenzugriff und Berechtigungen

Die Antworten, die Sie erhalten, spiegeln die **Daten- und Zugriffsebene** wider, die mit Ihrer Adobe-Identität verknüpft ist. Was Sie abfragen und sehen können, ist dasselbe wie das, wozu Sie in Experience Platform und den zugehörigen Lösungen berechtigt sind. Adobe Marketing Agent **erbt** diese Berechtigungen und benötigt **keine** separate Berechtigungseinrichtung für die [!DNL Microsoft 365]. Für die zugrunde liegenden Experience Platform AI Assistant-Funktionen und andere Adobe AI **Agenten sind die Berechtigungsanforderungen** der Verwendung dieser Funktionen in Experience Platform unverändert.

Der Agent verbindet Ihre [!DNL Microsoft 365] mit Experience Platform und den zugehörigen Programmen (Real-Time CDP, Adobe Journey Optimizer und Customer Journey Analytics). Mit dieser Integration können Sie dann den Experience Platform-KI-Assistenten und die Agenten verwenden, um relevante Einblicke direkt zu Ihrer [!DNL Microsoft 365]-Instanz abzurufen. Die in Ihrer [!DNL Microsoft 365]-Instanz zurückgegebenen Antworten werden als Texte, Tabellen und Datenvisualisierungen in konversativer und natürlicher Sprache dargestellt. Darüber hinaus erhalten Sie im selben [!DNL Copilot]-Chat Unterstützung für Folgefragen und Untersuchungen.

## Wichtige Anwendungsfälle und Beispielszenarien

| Anwendungsfall | Beschreibung |
| --- | --- |
| Abrufen von operativen Einblicken für Zielgruppen und Kunden-Journey | Mit der Adobe Marketing Agent können Sie mühelos operative Einblicke in Ihre Zielgruppen und Kunden-Journey abrufen. Sie können ermitteln, welche Zielgruppen am stärksten oder am stärksten interagieren, sodass Sie priorisieren können, wo Sie Ihre Bemühungen konzentrieren müssen. Sie können sehen, welche Kunden-Journey derzeit aktiv sind, und erfahren, wie sie abschneiden, sodass Sie Optimierungsmöglichkeiten erkennen können. Mit dem Agenten können Sie auch verfolgen, wie Ihre verschiedenen Segmente im Laufe der Zeit wachsen oder schrumpfen, sodass Sie auf Änderungen in Ihrer Zielgruppendynamik reagieren können, wenn sie auftreten. |
| Verwenden der Datenvisualisierung zur besseren Analyse von Journey und Kampagnen von Kunden | Sie können die Journey-Performance und die Abbrüche überprüfen, die Kampagnenleistung im Zeitverlauf vergleichen und verstehen, welche Touchpoints für Konversionen verantwortlich sind. Darüber hinaus können Sie visuelle Berichte zur Kampagnenleistung generieren und diese über Kanäle, Regionen oder über verschiedene Zeiträume hinweg vergleichen. Sie können auch Trends untersuchen, ohne Abfragen oder Dashboards manuell erstellen zu müssen. |
| Zusammenarbeit und Entscheidungsfindung fördern | Verwenden Sie empfohlene Eingabeaufforderungen, um Zielgruppen, Kampagnen und Web-Traffic zu untersuchen. Nutzen Sie die Vorteile einer Benutzeroberfläche in natürlicher Sprache, um sich leichter mit den Konzepten von Experience Platform und Customer Journey Analytics vertraut zu machen. Darüber hinaus können Sie bei Planungssitzungen Einblicke in [!DNL Teams] Kanäle oder Chats austauschen. Sie können die Adobe Marketing Agent auch verwenden, um Ad-hoc-Fragen in Echtzeit zu beantworten und gleichzeitig Pläne oder Decks zu überprüfen, sodass Sie den Stakeholdern die gleichen Metriken und Definitionen bieten können. |

## Voraussetzungen

Bevor Sie Adobe Marketing Agent für [!DNL Microsoft 365 Copilot] verwenden können, müssen Sie zunächst sicherstellen, dass Folgendes vorhanden ist:

- [!DNL Microsoft 365] mit [!DNL Microsoft Teams] oder [!DNL Microsoft Copilot Chat].
- Experience Platform und/oder mindestens eines der folgenden: Real-Time CDP, Adobe Journey Optimizer und/oder Customer Journey Analytics.
- Berechtigung für die Experience Platform Agent Orchestrator und Agenten.
- Zugriff auf das Adobe Experience Cloud-Konto Ihres Unternehmens (Anmeldung und Produktberechtigungen) für die verwendeten Lösungen und Daten. Wenn Sie keinen Zugriff auf Adobe haben, wenden Sie sich an Ihren Adobe-Administrator.

## Aktivieren des Agenten für Ihre Organisation {#enable-the-agent-for-your-organization}

Endbenutzer können die Adobe Marketing Agent erst verwenden, nachdem sie in Ihrem [!DNL Microsoft 365]-Mandanten zur Verfügung gestellt wurde. **Arbeiten Sie mit Ihrem [!DNL Microsoft 365] Copilot-Administrator** oder einem entsprechenden Administrator für Copilot-Agenten in Ihrer Organisation) zusammen, um den Zugriff zu aktivieren und den Agenten nach Bedarf Ihrer Organisation zuzuweisen.

Typische Ergebnisse nach der Admin-Einrichtung sind:

- Sie können **[!DNL Agent Store]** in [!DNL Teams] öffnen, **[!DNL Adobe Marketing Agent]** in Ihrer Agentenliste finden und **[!DNL Add]** auswählen, um sie an Ihre Copilot-Agenten anzuhängen.
- Alternativ kann Ihr Copilot-Administrator den **auch für alle Personen in Ihrer Organisation oder für bestimmte Gruppen** veröffentlichen), sodass Benutzer ihn nicht einzeln hinzufügen müssen.

Informationen zu Administratorschritten und Richtlinienoptionen im [!DNL Microsoft 365] Admin Center finden Sie unter [Verwalten von Agenten für Microsoft 365-Kopilot](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/manage) in der Microsoft-Dokumentation.

## Erste Schritte

Nachdem Ihr Unternehmen den Agenten aktiviert hat (siehe [Aktivieren des Agenten für Ihr Unternehmen](#enable-the-agent-for-your-organization)), navigieren Sie in der Anwendung Ihrer Wahl zu [!DNL Microsoft 365 Copilot] und wählen Sie **[!DNL All Agents]** über die linke Navigation aus.

![Linker Navigationsbereich des Microsoft 365 Copilot mit allen ausgewählten Agenten.](../agents/images/ama/all-agents.png)

Suchen Sie die Karte für [!DNL Adobe Marketing Agent] oder suchen Sie in der Suchleiste manuell nach dem Agenten. Sobald Sie den Agenten haben, wählen Sie die Karte aus.

![Adobe Marketing Agent-Karte oder Suchergebnis in der Agentengalerie.](../agents/images/ama/select-ama.png)

Verwenden Sie das Popup-Fenster, um mehr über den Agenten zu erfahren. Wenn Sie fertig sind, wählen Sie **[!DNL Add]** aus.

![Popup mit Adobe Marketing Agent-Details mit hervorgehobener Schaltfläche „Hinzufügen“.](../agents/images/ama/add-ama.png)

Das [!DNL Microsoft 365 Copilot]-Dashboard wird nun mit dem [!DNL Adobe Marketing Agent]-Branding auf der Hauptseite aktualisiert.

![Startseite von Microsoft 365 Copilot, auf der Adobe Marketing Agent im Haupt-Dashboard angezeigt wird.](../agents/images/ama/home.png)

### Anmelden und Kontext festlegen

Fordern Sie als Nächstes den Agenten auf, sich anzumelden, und führen Sie die folgenden Schritte aus, die zur Authentifizierung Ihres Kontos erforderlich sind. In diesem Schritt müssen Sie einen numerischen Code kopieren, den der Agent zurückgibt, und sich dann bei Ihrem Adobe-Unternehmen anmelden. Wenn Sie die Anmeldung nicht abschließen können oder keinen Zugriff auf Adobe-Lösungen für Ihr Unternehmen haben, wenden Sie sich an Ihren **Adobe-Administrator**.

![Anmeldung bei Adobe mit einem zu kopierenden numerischen Code und Anweisungen zur Authentifizierung bei Ihrer Adobe-Organisation.](../agents/images/ama/sign-in.png)

Verwenden Sie bei Erfolg den Kontextsetter, um die Dokumentationsquelle, Sandbox und Datenansicht festzulegen, die Sie für Ihre Abfragen verwenden werden.

![Benutzeroberfläche „Kontextsetter“ zum Auswählen der Dokumentationsquelle, Sandbox und Datenansicht für Abfragen.](../agents/images/ama/context.png)

### Verwenden des Agenten zum Abrufen operativer Erkenntnisse

Sobald Sie angemeldet sind, können Sie die auf der Hauptseite bereitgestellten Eingabeaufforderungen verwenden, um zu beginnen. Sie können auch eine Starteraufforderung nutzen, die sich auf die Analyse von Marketing-Audiences, die Überprüfung der Kampagnenleistung und die Überwachung der Kampagnen-Journey erstreckt. Wählen Sie beispielsweise **[!DNL Review campaign performance]** und dann **[!DNL Analyze engagement - Show web visitors for top 10 products last week]** aus.

![Starteraufforderungen auf der Agenten-Startseite, einschließlich der Optionen Kampagnenleistung überprüfen und Interaktion analysieren.](../agents/images/ama/starter-guide.png)

Warten Sie einige Augenblicke, bis der Agent berechnet hat, und dann antwortet der Agent mit einer visualisierten Darstellung Ihrer Daten. Sie können das dargestellte Balkendiagramm verwenden oder **[!DNL View data]** auswählen, um die Daten in Tabellen anzuzeigen.

![Agentenantwort mit einem Balkendiagramm, das Web-Besucher für die wichtigsten Produkte visualisiert, und Option „Daten anzeigen“.](../agents/images/ama/response.png)

![Dieselben Einblicke werden als Datentabelle angezeigt, nachdem Sie auf „Daten anzeigen“ geklickt haben.](../agents/images/ama/tables.png)

Sie können weitere Nachforschungen anstellen, indem Sie Folgefragen auswählen, die der Agent empfiehlt. Alternativ können Sie auch verschiedene Starter-Eingabeaufforderungen drehen und ausprobieren, die Informationsquellen überprüfen, auf die der Agent verwiesen hat, oder Feedback mithilfe des Feedback-Mechanismus geben.

![Vorgeschlagene Folgefragen unter der Antwort des Agenten für weitere Untersuchungen.](../agents/images/ama/follow-up.png)

Weitere Informationen zu den Funktionen der Benutzeroberfläche des KI-Assistenten finden Sie im Handbuch unter [Verwenden des KI-Assistenten](../ai-assistant/ai-assistant-ui.md).

## Sicherheit, Datenschutz und verantwortungsvolle KI

**Datenverarbeitung und Governance**

Adobe Marketing Agent stützt sich auf dieselben Kontrollen und dieselbe Governance wie Experience Platform und [!DNL Microsoft 365]. Ihre Organisation behält das Eigentum und die Kontrolle über ihre Daten. Die über den Agenten zurückgegebenen Insights beziehen sich auf die Adobe-Berechtigungen und Datenberechtigungen jedes Benutzers. Es wird kein zusätzliches Berechtigungsmodell für die [!DNL Microsoft 365] eingeführt, das über das hinausgeht, was bereits in Experience Platform und den zugehörigen Adobe AI-Agenten gilt.

**Verantwortungsvolle KI-Nutzung**

Der Agent soll schreibgeschützte Einblicke zurückgeben und ändert Ihre Kundendaten in Experience Platform nicht. Sie sollten alle generierten Zusammenfassungen und Analysen überprüfen, bevor Sie sie für geschäftliche Entscheidungen verwenden.

**Unterstützte Sprachen und Umfang**

Die erste Version ist als englischsprachige Version verfügbar. Die Funktionen sind auf schreibgeschützte Einblicke beschränkt. Der Agent erstellt oder aktualisiert keine Marketing-Assets oder -Konfigurationen.

## Anhang

Weitere Informationen zu Adobe Marketing Agent für [!DNL Microsoft 365 Copilot] finden Sie im Folgenden.

### Adobe Marketing Agent [!DNL Microsoft 365 Copilot]-Administratorschritte

Um Agenten von einem externen Anbieter (Drittanbieterfirmen oder dem Microsoft Commercial Marketplace) einzurichten, müssen Sie zunächst sicherstellen, dass Ihre Mandanteneinstellungen externe Apps zulassen, und sie dann über den Abschnitt Integrierte Apps oder Agenten des Admin Centers verwalten.

#### Aktivieren externer Agenten in Mandanteneinstellungen

Bevor Sie externe Agenten bereitstellen können, muss die Richtlinie Ihrer Organisation diese zulassen.

- Melden Sie sich beim [Microsoft 365 Admin Center](https://admin.microsoft.com/) an.
- Navigieren Sie **Agenten** > **Einstellungen** > **Benutzerzugriff**.
- Stellen **unter „Zulässige Agententypen** sicher, **Zulassen von Apps und Agenten, die von externen Herausgebern erstellt wurden** ausgewählt ist.

>[!IMPORTANT]
>
>Wenn diese Einstellung deaktiviert ist, werden für Ihre Benutzerinnen und Benutzer keine externen Agenten im [Agentenspeicher](https://devblogs.microsoft.com/microsoft365dev/introducing-the-agent-store-build-publish-and-discover-agents-in-microsoft-365-copilot/) angezeigt.

#### Ermitteln und Genehmigen des Agenten

Normalerweise finden Sie externe Agenten im [[!DNL Microsoft Commercial Marketplace]](https://appsource.microsoft.com/).

- **Vom Marketplace**: Suchen Sie den gewünschten Agenten und wählen Sie **Jetzt abrufen**. Dadurch werden Sie oft zurück zur Seite „Integrierte Apps **Ihres Admin Centers**.
- **Berechtigungen überprüfen**: Wählen Sie in der Liste [Integrierte ](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide)&quot; den externen Agenten aus.
- Überprüfen Sie die **Daten und Tools** und **Sicherheit und**), um zu sehen, auf welche Daten der externe Anbieter zugreifen wird.
- Wählen Sie **Genehmigen** oder **Aktivieren** aus, um es in das Inventar Ihrer Organisation zu verschieben.

#### Für bestimmte Benutzer bereitstellen

Nach der Genehmigung können Sie genau steuern, wer den Agenten in der Seitenleiste des Copiloten sehen kann.

- Navigieren [[!DNL Microsoft 365]  im ](https://admin.microsoft.com/) zu **Agenten** > **Alle Agenten**.
- Wählen Sie den externen Agenten aus der Liste aus.
- Wählen **Bereitstellen** (oder **Zuweisung bearbeiten**) aus.
- Wählen Sie **Spezifische Benutzer/Gruppen** und suchen Sie nach den Einzelpersonen oder [!DNL Entra ID] Gruppen, die es haben sollen.
- Wählen Sie **Bereitstellung beenden** aus. Dadurch wird der Agent an diese Benutzer weitergeleitet, damit er automatisch in der Copilot-Oberfläche angezeigt wird.

#### Updates verwalten

Externe Anbieter aktualisieren ihre Agenten häufig. Befolgen Sie die folgenden Best Practices, um diese Aktualisierungen zu verwalten:

- Überprüfen Sie die [[!DNL Agent Registry]](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-registry?view=o365-worldwide) regelmäßig.
- Wenn für eine Aktualisierung neue Berechtigungen erforderlich sind, kann der Agent den Status &quot;**Update“**.
- Sie müssen Updates **genehmigen** bevor die neue Version für die zugewiesenen Benutzer bereitgestellt wird.