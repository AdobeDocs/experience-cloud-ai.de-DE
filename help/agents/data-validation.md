---
title: Validieren Ihrer Daten im KI-Assistenten
description: Erfahren Sie, wie Sie mit der Agent Orchestrator-gestützten Datenvalidierung im KI-Assistenten statistische und semantische Validierungen für Ihre Datensätze durchführen können.
source-git-commit: 97140003d4a03d83260cf42e026c2e068f517a09
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Validieren Ihrer Daten im KI-Assistenten

Sie können den KI-Assistenten verwenden, um die Datenqualität Ihrer Adobe Experience Platform-Datensätze zu überprüfen. Basierend auf Agent Orchestrator kann die Datenvalidierungsfunktion statistische und semantische Validierungen für Datensätze durchführen, Datensatzfelder analysieren, Datenqualitätsprobleme identifizieren und Zusammenfassungen natürlicher Sprachen mit umsetzbaren Einblicken zurückgeben. Dateningenieure, Analysten und Datenverwalter können diese Funktion über den KI-Assistenten nutzen, um schnelle Bewertungen der Datenqualität durchzuführen, ohne SQL-Abfragen zu schreiben oder durch komplexe Schemahierarchien zu navigieren.

Mit der Agent Orchestrator-gestützten Datenvalidierung im KI-Assistenten können Sie:

- Schließen Sie die wesentlichen Lücken sowohl im Onboarding-Prozess als auch in der täglichen Diagnose.
- Reduzieren Sie die manuelle Qualitätssicherung Ihrer Datensätze.
- Verkürzen Sie die Time-to-Value für Ihre Kunden.

Lesen Sie diese Dokumentation, um zu erfahren, wie Sie Ihre Daten im KI-Assistenten validieren können.

>[!NOTE]
>
>Der KI-Assistent ist die Gesprächsoberfläche für diesen Workflow. Agent Orchestrator führt die Logik durch und koordiniert die Validierungsschritte im Hintergrund.

## Anwendungsszenarien

| Anwendungsfall | Beschreibung |
| --- | --- |
| Neue Implementierung | In diesen Szenarien können Sie wichtige Identitäts- und Ereignisfelder überprüfen, um sicherzustellen, dass Formate und Nullraten in Ordnung sind. |
| Verdacht auf Zuordnungsproblem | In diesen Szenarien können Sie ein Feld überprüfen und die wichtigsten Werte und Ungültigkeiten überprüfen, um sicherzustellen, dass es der beabsichtigten Semantik entspricht. |
| Laufende Datenverwaltung | In diesen Szenarien können Sie die Datensatzvalidierung für kritische Datensätze wöchentlich ausführen, um Regressionen frühzeitig zu erkennen. |

## Handbuch für die -Benutzeroberfläche

Verwenden Sie **KI-**) in Adobe CX Enterprise, um Ihre Daten zu validieren. Der KI-Assistent ist die Gesprächsoberfläche, während Agent Orchestrator den Validierungs-Workflow im Hintergrund koordiniert. Die folgenden Schritte folgen den Hauptbildschirmen, die angezeigt werden.

### Validierung starten

![Startseite des KI-Assistenten mit dem Eingabefeld, das eine Anfrage zur Datensatzvalidierung, einen Experience Platform-Umgebungsselektor und eine Sendesteuerung anzeigt.](./images/validation/home.png)

Wählen Sie in der linken Navigationsleiste die Option **[!UICONTROL KI-Assistent]**. Verwenden Sie als Nächstes die Umgebungsauswahl und wählen Sie die Experience Platform-Organisation oder Sandbox aus, in der Ihr Datensatz lebt (z. B. **[!UICONTROL Experience Platform - Prod]**). Geben Sie im Eingabeaufforderungsfeld eine Validierungsanfrage ein (fordern Sie beispielsweise dazu auf, einen Datensatz anhand des Namens zu validieren). Wählen Sie **[!UICONTROL Senden]**, um die Eingabeaufforderung zu senden.

>[!TIP]
>
>Es empfiehlt sich, Ihren Datensatznamen beim Senden einer Abfrage an den KI-Assistenten das Wort „Datensatz“ voranzustellen. Ihre Abfrage sollte beispielsweise lauten: „Validieren des Datensatzes „Elektronik-Beispiel 1000“ anstelle von „Elektronik-Beispiel 1000 validieren“.

### Datensatz-Zusammenfassung und Feldtabelle lesen

![Antwort des KI-Assistenten mit vollständiger Argumentation, einer Validierungszusammenfassung und einer Tabelle mit Feldzusammenfassungen, in der Feldpfade, Typen und gültige Werte aufgelistet sind.](./images/validation/answer.png)

Warten Sie einen Augenblick, bis Agent Orchestrator den Durchlauf abgeschlossen hat (**Reasoning complete**). Wenn die Ausführung abgeschlossen ist, lesen Sie die Zusammenfassung für den Datensatznamen, die Anzahl der validierten Felder und die Stichprobengröße (in der Regel bis zu etwa 1.000 Zeilen).

Verwenden Sie die **[!UICONTROL Feldzusammenfassungen]**, um den Pfad, den Typ und die gültigen Werte jedes Felds (einschließlich des Gültigkeitsindikators) zu überprüfen. Darüber hinaus können Sie, sofern verfügbar, die Tabellen-, Diagramm- oder Dokumentensymbole auf der Karte verwenden, um die Darstellung der Ergebnisse zu ändern.

Wählen Sie **[!UICONTROL Alle Ergebnisse anzeigen]** aus, wenn Sie zusätzliche Spalten oder Zeilen über die erste Ansicht hinaus benötigen.

### Arbeiten in geteilter Ansicht

![Teilansicht mit Validierungsbeschreibung und Statistiken auf der linken Seite und einer erweiterten Diagrammvisualisierung gültiger Werte auf der rechten Seite.](./images/validation/split-screen.png)

Verwenden Sie in der erweiterten Ansicht das Aufspaltungs-Layout: detaillierte Statistiken und Erzählungen auf der einen Seite und das Diagramm auf der anderen Seite.

- Überprüfen Sie auf der Erzählseite die Gültigkeit, unterschiedliche Werte, Nullraten, die höchsten eindeutigen Werte und alle Nachrichten mit ungültigen Werten.
- Verwenden Sie auf der Visualisierungsseite das Diagramm für ein schnelles Lesen gültiger und ungültiger Werte im Beispiel.

Verwenden Sie **[!UICONTROL Verknüpfte Vorschläge]** oder das Eingabeaufforderungsfeld unten, um ein anderes Feld zu validieren, den Datensatz erneut auszuführen oder die Konversation fortzusetzen.

### Verwenden eines entsprechenden Vorschlags für eine Nachverfolgung

![Verwandte Vorschläge Chips über dem Eingabeaufforderungsfeld, wobei ein Vorschlag zur Validierung eines bestimmten Felds im Datensatz ausgewählt wurde.](./images/validation/related-suggestion.png)

Suchen Sie nach einer Antwort **[!UICONTROL Verwandte Vorschläge]** unterhalb der Konversation. Wählen Sie einen Vorschlag aus (z. B. „Bestimmtes Feld im selben Datensatz validieren„), um ihn in das Eingabeaufforderungsfeld zu laden. Passen Sie den Text bei Bedarf an, bestätigen Sie die Umgebung und wählen **[!UICONTROL Senden]**, um die Nachverfolgung auszuführen.

### Validieren auf Feldebene

![Karte mit den Validierungsergebnissen für ein einzelnes Feld in der Diagrammansicht, auf der ein Gültigkeits-Ringdiagramm und die Aktion In erweiterter Ansicht anzeigen angezeigt werden.](./images/validation/single-field.png)

Öffnen Sie eine Karte auf Feldebene **[!UICONTROL Validierungsergebnisse]** (z. B. nach der Validierung eines einzelnen Felds). Verwenden Sie die Steuerelemente „Ansicht“, um zu **Diagramm** (oder einer anderen Ansicht) zu wechseln, wenn Sie anstelle einer Tabelle eine visuelle Zusammenfassung benötigen. In diesem Schritt können Sie optional &quot;**[!UICONTROL &quot; auswählen]** um weitere Informationen zum Feld anzuzeigen.

Wählen Sie **[!UICONTROL In erweiterter Ansicht anzeigen]**, um eine größere, detailliertere Ansicht der Feldüberprüfung zu öffnen.

![Erweiterte Ansicht mit detaillierten Validierungsstatistiken auf Feldebene und Diagrammvisualisierung.](./images/validation/expanded-view.png)

In der erweiterten Ansicht können Sie eine Auflistung des gesamten Felds anzeigen, die auf einer Stichprobe von bis zu 1000 Datensätzen für das jeweilige Feld basiert. Mit dieser Funktion können Sie Informationen zu gültigen, eindeutigen und Nullwerten abrufen.

## Funktionsweise der Validierung

Wenn Sie eine Validierung im KI-Assistenten starten, analysiert Agent Orchestrator eine repräsentative Stichprobe Ihres Datensatzes, in der Regel die letzten ~1.000 Zeilen, anstatt den gesamten Datensatzverlauf zu verarbeiten. Der Prozess ist streng schreibgeschützt und stellt sicher, dass Ihre Daten, Schemata und Zuordnungen unverändert bleiben. Die Validierungsergebnisse sind konsistent, unabhängig davon, wie Ihre Daten in Experience Platform eintreten, ob durch Quellen, Streaming, Datei-Uploads, Datenvorbereitung oder andere Erfassungsmethoden. Die Ergebnisse dienen als indikative Prüfungen, damit Sie schnell Datenqualitätsmuster oder potenzielle Probleme identifizieren können, sodass Sie bei Bedarf weitere Maßnahmen ergreifen können (z. B. mithilfe des Abfrage-Service). Dieser Agent Orchestrator-gestützte Ansatz ermöglicht schnelle Bewertungen, ohne die Datenaufnahme zu unterbrechen oder die Produktionsarbeitslasten zu beeinträchtigen.

## Validierungsergebnisse

Für jedes validierte Feld zeigt der KI-Assistent die vom Validierungs-Workflow generierten Ergebnisse an, darunter:

**Basisstatistiken**

- Gesamtzahl der für die Stichprobe verwendeten Zeilen
- nullCount (und optional % null)
- uniqueCount (falls verfügbar)
- Wichtigste eindeutige Werte (z. B. Top 10) und ihre Häufigkeiten

**Semantische Validierung**

- Liste der **vermutlich ungültigen Werte**
- Für jeden ungültigen Wert eine **Erklärung** (z. B. „Kein gültiges E-Mail-Format“, „Zeitstempel außerhalb des erwarteten Bereichs„)

**Zusammenfassung natürlicher Sprache**

- Eine kurze Zusammenfassung der Feldqualität
- Empfohlene nächste Aktionen, z. B. „Zuordnung für Feld X überprüfen“, „Feld Y aufgrund hoher Nullrate ignorieren“ oder „Validierung für E-Mail-Format verschärfen“.

| Aspekt | Musterausgabe |
| --- | --- |
| Vollständigkeit | `nullCount = 9,532 (95.3%)` |
| Einzigartigkeit | `uniqueCount = 3` |
| Top-Werte | `"True" (255), "False" (243)` |
| Ausgangswerte | `"abc@, reason: "not a valid email address"` |

## Validierungstypen

Es gibt zwei Hauptvalidierungstypen, die Sie mit dem KI-Assistenten durchführen können:

- **Feldüberprüfung**: Überprüfen eines bestimmten Felds in einem Datensatz.
- **Datensatzvalidierung**: Validieren von bis zu fünf (5) Feldern in einem Datensatz.

>[!BEGINTABS]

>[!TAB Feldüberprüfung]

Verwenden Sie die Feldvalidierung im KI-Assistenten, um ein bestimmtes Feld in einem bestimmten Datensatz zu validieren. Diese Validierungsfertigkeit bietet Folgendes:

- Null-Anzahl und Anzahl eindeutiger Werte.
- Die wichtigsten eindeutigen Werte und ihre entsprechenden Häufigkeiten.
- KI-unterstützte semantische Validierung (die Möglichkeit, ungültige Werte basierend auf den verfügbaren Metadaten und den tatsächlichen Werten der Daten zu erkennen).

Zu den Beispielaufforderungen für die Feldüberprüfung gehören:

- Überprüfen Sie das E-Mail-Feld im Datensatz Customers_2024 .
- Überprüfen Sie den Feldstatus für den Datensatz customer_events_2024.
- Überprüfen Sie das Feld person.address.city für den Kundendatensatz.

>[!TAB Datensatzvalidierung]

Verwenden Sie die Datensatzvalidierung im KI-Assistenten, um ganze Datensätze zu validieren, wobei die Gesamtqualität und die wichtigsten Probleme zusammengefasst werden. Sie können diese Felder zwar explizit bereitstellen, Agent Orchestrator kann aber auch den Datensatz analysieren und automatisch die relevantesten Felder ermitteln. Diese Fähigkeit bietet denselben Typ von Informationen wie die Feldüberprüfung, jedoch über mehrere Zielfelder hinweg. Sie können bis zu fünf Felder in einem Datensatz überprüfen.

Zu den Beispielaufforderungen für die Datensatzvalidierung gehören:

- Validieren des Kundendaten-Datensatzes 2024.
- Validieren Sie die Felder E-Mail, Telefon für Kunden_2024.
- Zusammenfassen von firstName, lastName, BirthDate für Kundendaten.
- Datensatz zusammenfassen 693012a4b8c98b09cea350bc.

>[!ENDTABS]

## Von der Datenvalidierung durchgeführte Prüfungen

Für jedes Feld und jeden Datensatz werden die folgenden Validierungstypen durchgeführt:

- **Vollständigkeitsprüfungen**: Null/fehlende Zählungen und Prozentsätze.
- **Verteilungsprüfungen**: Beste eindeutige Werte und ihre Verteilungen, Erkennung hoher Kardinalität.
- **Semantische Prüfungen vs. Schema**: Verwendet den XDM-Feldnamen, den Typ und die Beschreibung, um daraus abzuleiten, wie „gültig“ aussieht, und kennzeichnet dann Anomalien.
- **Datentypabhängige Prüfungen** (falls zutreffend):
   - E-Mail: Plausibilität von Format und Domain
   - Telefon: Formatbereitschaft (z. B. E.164)
   - Datumsangaben/Zeitstempel: Grundlegende Formatsicherheit (z. B. ISO-8601)
- **Identitätsbezogene Prüfungen** (künftig/erweitert): Eindeutigkeit von potenziellen Identitätsfeldern oder zusammengesetzten Schlüsseln.

Diese Prüfungen kombinieren deterministische Statistiken mit LLM-unterstützter semantischer Validierung, um Werte zu erkennen, die „falsch aussehen“, selbst wenn sie technisch mit dem Schema übereinstimmen.

## Einschränkungen

Bevor Sie Ihre Daten validieren, sollten Sie einige wichtige Einschränkungen beachten. Diese Einschränkungen sollen ein Gleichgewicht zwischen Leistung und Funktionalität herstellen und dabei helfen, Erwartungen für die erwarteten Analysetypen und Erkenntnisse zu definieren.

- **Nur Sampling**: Die Validierung arbeitet an einer Stichprobe des Datensatzes (in der Regel die letzten ~1.000 Zeilen), anstatt den gesamten Datensatz zu verarbeiten. Vollständige Datensatz-Scans sind nicht verfügbar.
- **Maximale Feldanzahl**: Bei der Validierung eines Datensatzes analysiert der Agent bis zu fünf Felder pro Anfrage. Sie können diese Felder angeben oder zulassen, dass der Agent sie automatisch auswählt.
- **probabilistische Semantik**: Die Erkennung ungültiger Werte beruht zum Teil auf LLM-basierter Inferenz, bei der gelegentlich subtile Fehler oder Markierungsgrenzwerte übersehen werden können.
- **Schreibgeschützter Vorgang**: Der Agent nimmt keine Änderungen an Ihren Daten oder ihrem Schema vor. Es bietet Einblicke und hebt potenzielle Probleme hervor, führt jedoch keine automatischen Korrekturen durch.

Wenn Ihre Validierungsanforderungen erschöpfender sind oder die Anwendung komplexer Geschäftslogik erfordern, sollten Sie die im KI-Assistenten angezeigten Ergebnisse um zusätzliche Tools wie Abfrage-Service- oder Datenvorbereitungs-Validierungen ergänzen.
