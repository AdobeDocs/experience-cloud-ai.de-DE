---
title: Data Engineering Agent
description: Erfahren Sie, wie Sie die Data Engineering Agent verwenden können.
hide: true
hidefromtoc: true
source-git-commit: 12c61f88b358fc8c357ec4fa373493d6b70d5a06
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 2%

---

# Data Engineering Agent

&lt;!— DIES IST EIN ENTWURF —>

Data Engineering Agent ist ein Agent Orchestrator-gestützter KI-basierter Copilot für Daten-Teams in Adobe Experience Platform. Der Agent ist für die Bewältigung der großen Last im gesamten End-to-End-Datenlebenszyklus konzipiert: Datenmodellierung, Onboarding, SQL-Datenvorbereitung, Governance und Lebenszyklus-Management. Mit dem Data Engineering Agent können Ingenieure und Architekten schneller arbeiten, da die Datenqualität steigt und die manuellen Arbeitsschritte geringer sind.

Data Engineering Agent ist in Kompetenzen unterteilt, die Sie zur Optimierung Ihrer Workflows nutzen können.

| DATA ENGINEERING AGENT SKILL | Beschreibung |
| --- | --- |
| Daten-Onboarding | <strong>Daten-Onboarding</strong> unterstützt Batch-Quellen wie S3, Marketo und Data Landing Zone (DLZ). Zu den Funktionen gehören: <ul><li>Herstellen einer Verbindung zu verschiedenen Datenquellen, einschließlich S3, Data Landing Zone, Marketo und mehr.</li><li>Profilerstellung von Quelldaten (z. B. eindeutige Werte, NULL, Duplikate und grundlegende Qualitätsmetriken).</li><li>Ausrichten von Quellfeldern sowohl an XDM-Standardfeldgruppen als auch an benutzerdefinierten Feldern.</li><li>Vorschlagen und Erstellen von Datenaufnahme-Datenflüssen (z. B. Verschieben von Daten aus S3 oder Marketo in RTCDP-/CJA-Datensätze).</li></ul> |
| Automatisierte Datenqualität und semantische Anreicherung | <ul><li>Führt umfassende Bewertungen der Datenqualität durch, einschließlich der Identifizierung von Anomalien und der Meldung gültiger/ungültiger Anzahl von Datensätzen.</li><li>empfiehlt Verbesserungen der Datenqualität, z. B. Typnormalisierung, Währungsformatierung und ID-Deduplizierung.</li><li>Wendet die semantische Anreicherung auf Schemata an, die auf Daten-Sampling und intelligenter Erkennung von Benennungsmustern basieren.</li><li>Ersucht Benutzende um Bestätigung für vorgeschlagene Anreicherungen, um sicherzustellen, dass abgeschlossene und genehmigte Datenänderungen vorgenommen werden.</li></ul> |
| Data Distiller | |
| Datenerfassung | |
| Datenvalidierung | |

Mit Data Engineering Agent können Sie Folgendes sicherstellen:

- **Schnelleres Onboarding**: Verkürzen Sie den Zeitaufwand von Wochen der manuellen Schemazuordnung und Pipeline-Einrichtung auf Stunden geführter, konversativer Konfiguration.
- **Höhere Datenqualität**: Weniger ungültige Datensätze und Produktionsvorfälle aufgrund von integrierter Datenqualitätsanalyse und semantischen Prüfungen.
- **Verbesserte Governance und Compliance**: Governance-Richtlinien werden zur Entwurfszeit angehängt (Bezeichnungen, TTL, Identitätsverarbeitung) und nicht als nachträglicher Einblick.
- **Produktivere Daten-Teams**: Die Arbeit mit sich wiederholenden SQL/Datenflüssen wird automatisiert, sodass sich die Ingenieure auf die hochwertige Gestaltung und Optimierung konzentrieren.
- **Umfassenderer Self-Service**: Nicht-Experten-Stakeholder können gängige Datenvorbereitungsaufgaben mit Leitplanken sicher selbst bereitstellen.