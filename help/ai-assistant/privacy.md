---
title: Datenschutz, Sicherheit und Governance im KI-Assistenten
description: Erfahren Sie mehr über die Datenschutz-, Sicherheits- und Governance-Praktiken für KI-Assistenten.
source-git-commit: c9909616697ef319a307b5c8a1ee135204347844
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Datenschutz, Sicherheit und Governance im KI-Assistenten

Der KI-Assistent in Adobe Experience Platform ist so konzipiert, dass Datenschutz, Sicherheit und Governance im Vordergrund stehen.

Lesen Sie dieses Dokument, um mehr über die auf das Kundenvertrauen fokussierten Funktionen zu erfahren, die Sie vom KI-Assistenten erwarten können:

* KI Assistant verwendet heute keine personenbezogenen Daten, auch nicht für Trainingszwecke.
* Der KI-Assistent kennt keine Verbraucherdaten.
* Alle vorhandenen [Zugriffssteuerungsrichtlinien](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/home) werden vom KI-Assistenten berücksichtigt.

   * Alle neuen attributbasierten Zugriffssteuerungsrichtlinien werden nach maximal 24 Stunden im KI-Assistenten angezeigt.&ast;

* Die Interaktion mit dem KI-Assistenten muss ausdrücklich erlaubt sein.

   * Sie können Berechtigungen für Experience Platform und Journey Optimizer mithilfe der [Benutzeroberfläche „Berechtigungen“ unterschiedlich ](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/browse) und mit der [Admin Console](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/browse) Berechtigungen für Customer Journey Analytics zuweisen.
   * Die Berechtigungen sind granular und Ihr Sandbox-Administrator kann konfigurieren, welche Ihrer Benutzer bzw. Benutzerinnen verschiedene Fragenkategorien stellen können (Produktkenntnisfragen mit dem KI-Assistenten oder Fragen zu operativen Einblicken).

* Der KI-Assistent ist eine HIPAA-fähige Funktion, wenn sie in Kombination mit Adobe Experience Platform Healthcare Shield verwendet wird.
* Sie können ein Protokoll Ihrer vorherigen Interaktionen mit dem KI-Assistenten mit einer 30-Tage-Aufbewahrungsrichtlinie anzeigen.
* Der KI-Assistent basiert auf Sandbox-spezifischen Daten und der öffentlichen Adobe-Dokumentation, wenn auf Benutzeraufforderungen reagiert wird. Daten werden nicht über Sandboxes hinweg freigegeben.
* Eingabeaufforderungen, die Sie an den KI-Assistenten senden, werden nicht an andere Kunden weitergegeben.

&ast; *Dies bedeutet, dass es beim Hinzufügen neuer Kennzeichnungen zu Feldern und Objekten oder beim Erstellen neuer Richtlinien bis zu 24 Stunden dauert, bis der KI-Assistent diese berücksichtigt. Während dieser 24 Stunden können Benutzer mit neu eingeschränktem Zugriff weiterhin auf diese Felder und Objekte zugreifen.*

