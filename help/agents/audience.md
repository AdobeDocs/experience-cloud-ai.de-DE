---
title: Audience Agent
description: Erfahren Sie, wie Sie mit der Audience Agent Zielgruppen erstellen, Zielgruppenänderungen anzeigen, doppelte Zielgruppen erkennen und Zielgruppeneinblicke anzeigen können.
source-git-commit: ca3766477459fb13170d176057a3ea9fbb791b29
workflow-type: tm+mt
source-wordcount: '1204'
ht-degree: 2%

---


# Audience Agent

>[!AVAILABILITY]
>
>Die Audience Agent steht allen Kunden zur Verfügung, die Zugriff auf den KI-Assistenten haben. Sie benötigen jedoch die folgenden Berechtigungen, um die Funktionen von Audience Agent vollständig nutzen zu können.
>
>**Segmente anzeigen**: Mit dieser Berechtigung können Sie die Audience Agent verwenden, um Einblicke in die Zielgruppen direkt im KI-Assistenten anzuzeigen.
>
>**Segmente verwalten**: Mit der Berechtigung „Bis“ können Sie die Audience Agent verwenden, um neue Zielgruppen direkt im KI-Assistenten zu erstellen.

Mit der Audience Agent können Sie Einblicke zu Zielgruppen erhalten, einschließlich der Erkennung signifikanter Änderungen der Zielgruppengröße, der Erkennung doppelter Zielgruppen, der Untersuchung Ihres Zielgruppeninventars und des Abrufs der Zielgruppengröße.

>[!SLIDE](audience-agent-overview)

## Unterstützte Anwendungsfälle

Der Audience Agent innerhalb des KI-Assistenten unterstützt die folgenden Anwendungsfälle:

- Unterhalten Sie Ihre Zielgruppe
   - Suchen nach Zielgruppengrößen vorhandener Zielgruppen
   - Auf der Grundlage vollständiger oder teilweiser Attribute mit den folgenden Namen nach Zielgruppen suchen
   - Erkennen doppelter Zielgruppen
   - Entdecken Sie XDM-Felder, mit denen Sie eine Zielgruppe definieren können
- Erkennung signifikanter Änderungen der Zielgruppengröße
   - Auf diese Weise können Sie Zielgruppen finden, die plötzlich gewachsen oder geschrumpft sind, sodass Sie potenzielle Marktveränderungen besser analysieren können
- Erstellung einer Zielgruppe
   - Mit dieser Fähigkeit können Sie eine Zielgruppe basierend auf den angegebenen Attributen und Ereignissen erstellen
   - Darüber hinaus können Sie mit dieser Fähigkeit die potenzielle Größe einer Zielgruppe schätzen, bevor Sie die Zielgruppe erstellen, sodass Sie schnell die effektivste Zielgruppe durchlaufen können, bevor sie aktiviert werden kann

<!-- - Find your audience size and detect significant changes in audience size
  - This lets you find audiences that have suddenly grown or shrunk, letting you better analyze potential market changes
- Detect duplicate audiences
  - This lets you reduce redundancies with your created audiences
- Find audiences based on full or partial attributes named
  - This lets you more easily navigate through your audience inventory
- Discover XDM fields you can use to define an audience
  - This skill lets you more easily identify the right fields to use in your audience based on context and relevance -->

Die Audience Agent unterstützt **derzeit** folgende Funktion nicht:

- Zielbasierte Zielgruppenexploration
   - Durch die zielbasierte Audience-Exploration können Sie relevante Datensätze und Profile ermitteln, die auf ein Geschäftsziel ausgerichtet sind, indem Sie maschinelle Lernmodelle wie Kaufneigung oder Konversionsneigung anwenden.

Darüber hinaus sollten Sie bei der Verwendung von Audience Agent die folgenden Einschränkungen beachten:

- Audience Agent benötigt mindestens 24 Stunden zur Verarbeitung Ihrer Daten
   - Sie können beispielsweise **nicht** eine Abfrage haben, die innerhalb der letzten 24 Stunden nach Daten sucht. Sie müssen mindestens innerhalb der letzten 48 Stunden nachsehen.
- Audience Agent unterstützt nur die folgenden Zielgruppentypen:
   - **Benutzerbasierte** Zielgruppen, die mithilfe der Batch-Segmentierung ausgewertet werden
   - **Account-basierte** Zielgruppen für die folgenden Anwendungsfälle:
      - Konversative Zielgruppenforschung
      - Erkennung doppelter Zielgruppen

## Eingabeaufforderungen im Beispiel

Die folgenden Beispiele zeigen Beispielaufforderungen und -antworten für die Audience Agent.

### Konversative Zielgruppenforschung

Felder für wohlhabende Käufer anzeigen.

+++ Antwort

![Der KI-Assistent zeigt eine Tabelle mit Feldern an, die für wohlhabende Käufer relevant sind.](./images/audience/affluent-buyers.png)

+++

Welche Zielgruppen wurden in den letzten 30 Tagen in keiner Kampagne aktiviert oder verwendet?

+++ Antwort

![Der KI-Assistent zeigt eine Tabelle mit Zielgruppen an, die in den letzten 30 Tagen nicht aktiviert oder in Kampagnen verwendet wurden.](./images/audience/not-activated.png)

+++

Listet alle Zielgruppen auf, die in den letzten 3 Monaten neuen Zielen zugeordnet wurden.

+++ Antwort

![Der KI-Assistent listet die eine Zielgruppe auf, die in den letzten 3 Monaten einem neuen Ziel zugeordnet wurde.](./images/audience/new-destination.png)

+++

Welche Konto-Zielgruppe hat die größte Zielgruppengröße und wie groß ist diese?

+++ Antwort

![Der KI-Assistent zeigt eine Tabelle mit den größten Konto-Zielgruppen an.](./images/audience/largest-account-audience.png)

+++

### Erkennen doppelter Zielgruppen

Habe ich Zielgruppen mit identischen oder ähnlichen Beschreibungen?

+++ Antwort

![Der KI-Assistent zeigt eine Tabelle an, die die Segmentdefinition und die Namen der Zielgruppen mit denselben Segmentdefinitionen enthält.](./images/audience/similar-descriptions.png)

+++

Identifizieren Sie Zielgruppen, die dieselben Regeln, aber unterschiedliche Namen haben.

+++ Antwort

![Der KI-Assistent zeigt eine Tabelle mit den Namen von Zielgruppen an, die dieselben Zielgruppenregeln verwenden.](./images/audience/same-rules-different-names.png)

+++

Anzeigen aller Zielgruppen mit denselben Regeln, aber unterschiedlichen Aktivierungszielen.

+++ Antwort

![Der KI-Assistent zeigt an, dass es keine doppelten Segmentdefinitionen für verschiedene Ziele gibt.](./images/audience/same-rules-different-destinations.png)

+++

Identifizieren Sie Konto-Zielgruppen, die dieselben Regeln, aber unterschiedliche Namen haben.

+++ Antwort

![Der KI-Assistent zeigt eine Tabelle an, die die Namen und IDs von Konto-Zielgruppen enthält, die dieselben Zielgruppenregeln verwenden.](./images/audience/duplicate-account-audience.png)

+++

### Abrufen der Zielgruppengröße

Wie groß ist meine Audience „Gold-Star Members in California_f153e1“ aktuell?

+++ Antwort

![Der KI-Assistent gibt die aktuelle Größe der Zielgruppe an, nach der gefragt wurde.](./images/audience/current-size.png)

+++

Welches ist mein größtes Publikum?

+++ Antwort

![Der KI-Assistent enthält Informationen zur Zielgruppe mit den meisten Profilen, einschließlich Name und Zielgruppen-ID.](./images/audience/largest-audience.png)

+++

### Erkennung signifikanter Änderungen der Zielgruppengröße

Welche Zielgruppen haben in der letzten Woche um mehr als 20 % zugenommen?

+++ Antwort

![Der KI-Assistent zeigt eine Tabelle mit den Namen aller Zielgruppen an, die mit der Abfrage übereinstimmen. Außerdem werden der prozentuale Anstieg, die aktuelle Zielgruppengröße sowie die frühere Zielgruppengröße angezeigt.](./images/audience/increase-past-week.png)

+++

Welche Zielgruppen sind im letzten Monat um mehr als 10 % kleiner geworden?

+++ Antwort

![Der KI-Assistent zeigt eine Tabelle mit den Namen aller Zielgruppen an, die mit der Abfrage übereinstimmen. Außerdem werden die aktuelle Zielgruppengröße, die frühere Zielgruppengröße sowie das Datum der alten Zielgruppengröße angezeigt.](./images/audience/decrease-month.png)

+++

Welches ist mein am schnellsten wachsendes Publikum?

+++ Antwort

![Der KI-Assistent gibt den Namen der am schnellsten wachsenden Zielgruppe sowie die aktuelle Größe und den Prozentsatz des Wachstums an.](./images/audience/fastest-growing.png)

+++

### Erstellen einer Zielgruppe

Wenn Sie mit Audience Agent eine Zielgruppe erstellen, führt Sie der KI-Assistent durch einen Plan. Sie können beispielsweise anfordern, „eine Zielgruppe aus Personen zu erstellen, die in Kalifornien leben“. Der KI-Assistent listet dann den Plan auf, den er zur Erstellung der Zielgruppe durchführen wird.

+++ Antwort

![Der KI-Assistent zeigt den Plan zur Erstellung einer Zielgruppe an.](./images/audience/audience-create-plan.png)

+++

Dieser Plan umfasst drei Schritte:

1. [Identifizieren von Zielgruppeneigenschaften](#identify)
2. [Zielgruppengröße schätzen](#estimate)
3. [Erstellen und Beibehalten einer neuen Zielgruppe](#create)

#### Identifizieren von Zielgruppeneigenschaften {#identify}

![Schritt 1 des Plans zur Identifizierung der Merkmale der Zielgruppe.](./images/audience/plan-step-1.png){align="center" width="80%"}

Nachdem Sie den Plan akzeptiert haben, erfasst der KI-Assistent die Eigenschaften der Zielgruppe basierend auf Ihrer ersten Abfrage.

+++ Antwort

![Die Zielgruppendefinition, die auf der Benutzerabfrage basiert.](./images/audience/audience-create-definition.png)

Für diese Abfrage generiert der KI-Assistent den entsprechenden Profile Query Language (PQL), der nach Personen sucht, die in Kalifornien leben. In diesem Anwendungsfall würde die PQL-Abfrage wie folgt aussehen:

```sql
homeAddress.state.equals("California", false)
```

Weiterführende Informationen zu PQL finden Sie in der Übersicht zu [PQL](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/pql/overview).

+++

Wenn die Zielgruppendefinition des KI-Assistenten korrekt ist, können Sie sie genehmigen und mit dem nächsten Schritt fortfahren.

#### Zielgruppengröße schätzen {#estimate}

![Schritt 2 des Plans zur Schätzung der Größe der potenziellen Zielgruppe.](./images/audience/plan-step-2.png){align="center" width="80%"}

Nach Genehmigung der identifizierten Zielgruppeneigenschaften schätzt der KI-Assistent die Größe der potenziellen Zielgruppe und die Details der Zielgruppendefinition.

+++ Antwort

![Die Beispielschätzung für die potenzielle Zielgruppe wird angezeigt. Die geschätzte Größe und die Segmentdefinition werden angezeigt.](./images/audience/audience-create-estimate.png)

+++

Wenn die geschätzte Größe korrekt aussieht, können Sie sie genehmigen und mit dem nächsten Schritt fortfahren.

#### Neue Zielgruppe erstellen und beibehalten {#create}

![Schritt 3 des Plans, der die Erstellung der Zielgruppe abschließt.](./images/audience/plan-step-3.png){align="center" width="80%"}

Wenn die Eigenschaften und die Zielgruppengröße korrekt aussehen, können Sie die Erstellung der Zielgruppe genehmigen oder ablehnen.

+++ Antwort

Zunächst können Sie die vorgeschlagene Zielgruppe über das bereitgestellte Datenraster überprüfen.

![Der Überprüfungsbildschirm wird angezeigt.](./images/audience/audience-create-review.png)

Wenn die Zielgruppe korrekt dargestellt wird, können Sie den Vorschlag akzeptieren, indem Sie auf **[!UICONTROL Erstellen]** klicken, um die Erstellung der Zielgruppe abzuschließen.

![Das vollständige Angebot für die Zielgruppe wird angezeigt.](./images/audience/audience-create-proposal.png)

+++

Die Zielgruppe wird jetzt erstellt.

![Der Zielgruppenvorschlag wurde akzeptiert und die Zielgruppe wurde erstellt.](./images/audience/audience-finish-create.png){align="center" width="80%"}

## Nächste Schritte

Nach dem Lesen dieses Handbuchs sollten Sie ein besseres Verständnis von Audience Agent und den unterstützten Funktionen haben. Weitere Informationen zu Agenten in Adobe Experience Platform finden Sie in der [Übersicht über Agent Orchestrator](./agent-orchestrator.md).

