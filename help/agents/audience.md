---
title: Audience Agent
description: Erfahren Sie, wie Sie mit der Audience Agent Zielgruppen erstellen, Zielgruppenänderungen anzeigen, doppelte Zielgruppen erkennen und Zielgruppeneinblicke anzeigen können.
source-git-commit: 2c50a4abaf9606e3c7887073053d0cde3ec761e5
workflow-type: tm+mt
source-wordcount: '859'
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

## Unterstützte Anwendungsfälle

Der Audience Agent innerhalb des KI-Assistenten unterstützt die folgenden Anwendungsfälle:

- Unterhalten Sie Ihre Zielgruppe
   - Suchen nach Zielgruppengrößen vorhandener Zielgruppen
   - Auf der Grundlage vollständiger oder teilweiser Attribute mit den folgenden Namen nach Zielgruppen suchen
   - Erkennen doppelter Zielgruppen
   - Entdecken Sie XDM-Felder, mit denen Sie eine Zielgruppe definieren können
- Erkennung signifikanter Änderungen der Zielgruppengröße
   - Auf diese Weise können Sie Zielgruppen finden, die plötzlich gewachsen oder geschrumpft sind, sodass Sie potenzielle Marktveränderungen besser analysieren können

<!-- - Find your audience size and detect significant changes in audience size
  - This lets you find audiences that have suddenly grown or shrunk, letting you better analyze potential market changes
- Detect duplicate audiences
  - This lets you reduce redundancies with your created audiences
- Find audiences based on full or partial attributes named
  - This lets you more easily navigate through your audience inventory
- Discover XDM fields you can use to define an audience
  - This skill lets you more easily identify the right fields to use in your audience based on context and relevance -->

Die Audience Agent unterstützt **derzeit** die folgenden Funktionen nicht:

- Wissensbasierte Zielgruppenerstellung
   - Die wissensbasierte Zielgruppenerstellung erstellt eine Zielgruppe basierend auf den angegebenen Attributen und Ereignissen
   - Darüber hinaus können Sie die potenzielle Größe der Zielgruppe vor der Erstellung der Zielgruppe schätzen. Auf diese Weise können Sie die effektivste Zielgruppe schnell durchlaufen, bevor sie aktiviert werden kann
   - Die Unterstützung für diese Funktion wird in Kürze verfügbar sein
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

## Nächste Schritte

Nach dem Lesen dieses Handbuchs sollten Sie ein besseres Verständnis von Audience Agent und den unterstützten Funktionen haben. Weitere Informationen zu Agenten in Adobe Experience Platform finden Sie in der [Übersicht über Agent Orchestrator](./agent-orchestrator.md).

