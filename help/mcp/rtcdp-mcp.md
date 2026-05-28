---
solution: Real-Time Customer Data Platform
title: Real-Time CDP MCP (Beta)
description: Erfahren Sie, wie Sie Adobe Real-Time CDP mithilfe des MCP-Servers mit MCP-Clients verbinden.
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: b2c93fd31bb72ebaf79aaa07aab68d39e63dc9b5
workflow-type: tm+mt
source-wordcount: '2634'
ht-degree: 2%

---

# Real-Time CDP MCP (Beta) {#rtcdp-mcp}

Sie können die Adobe Real-Time CDP-MCP-Integration verwenden, um Zielgruppen, Ziele und den Aktivierungsstatus mit einfachen Eingabeaufforderungen abzufragen - ohne API-Aufrufe zu schreiben oder durch Produktbildschirme zu navigieren. Diese Integration dient sowohl Kunden von Adobe Real-Time CDP als auch von Adobe Real-Time CDP B2B edition und bietet eine Möglichkeit, unterstützte Real-Time CDP-Daten und -Workflows von MCP-kompatiblen Clients aus zu untersuchen. Lesen Sie dieses Handbuch, um zu erfahren, wie die Integration funktioniert, was Sie damit tun können und wie Sie beginnen.

>[!AVAILABILITY]
>
>Real-Time CDP MCP befindet sich in Beta. Die Funktion und die Dokumentation können sich ändern. Der Real-Time CDP-MCP-Server wird als **Remote-HTTP-Transport-Server** verteilt, den Benutzerinnen und Benutzer in unterstützten MCP-Clients und App-Plattformen installieren und konfigurieren (z. B. [!DNL Claude], [!DNL ChatGPT], [!DNL Claude Code], [!DNL Codex], [!DNL Cursor] oder [!DNL VS Code]). Die Authentifizierung erfolgt über einen **browserbasierten Anmeldefluss** - Wenn Ihr Client zum ersten Mal eine Verbindung zum Server herstellt, wird Ihr Standardbrowser geöffnet, damit Sie sich mit Ihren Adobe-Anmeldeinformationen anmelden und den Zugriff autorisieren können. Wenden Sie sich an den Adobe-Support, um auf dieses Beta-Programm zuzugreifen.

## Beta, Sicherheit und rechtliche Hinweise {#mcp-notices}

**Hinweis zur Beta-Dokumentation:** Diese Dokumentation behandelt eine Beta-Funktion und stellt keine endgültige Dokumentation dar. Der hier beschriebene Inhalt bezieht sich auf eine Beta-Version und kann sich vor der allgemeinen Verfügbarkeit ändern. Adobe übernimmt keine Gewähr für die Vollständigkeit oder Richtigkeit dieser Dokumentation.

Durch die Verwendung des Adobe Real-Time CDP MCP Servers (Beta) (“Beta„) erkennen Sie hiermit an, dass der Beta **„wie besehen“ und ohne Gewährleistung jeglicher Art bereitgestellt wird**. Adobe ist nicht verpflichtet, die Beta zu pflegen, zu korrigieren, zu aktualisieren, zu ändern oder anderweitig zu unterstützen. Es wird empfohlen, Vorsicht walten zu lassen und sich nicht auf die ordnungsgemäße Funktionsweise oder Leistung solcher Beta und/oder Begleitmaterialien zu verlassen. Die Beta-Version wird als vertrauliche Information von Adobe betrachtet. Jedes „Feedback“ (Informationen zur Beta-Version, einschließlich, aber nicht beschränkt auf Probleme oder Mängel, auf die Sie bei der Verwendung der Beta-Version stoßen, Vorschläge, Verbesserungen und Empfehlungen), das Sie Adobe übermitteln, wird hiermit an Adobe übertragen, einschließlich aller Rechte, Titel und Interessen an diesem Feedback.

>[!WARNING]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration. Die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen in einer Sandbox-Umgebung vor der produktiven Verwendung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Was ist das Modell-Kontextprotokoll? {#mcp-overview}

Marketing-, Daten- und Kundenerlebnis-Teams verlassen sich zunehmend auf Chat-basierte Anwendungen und Entwickler-Tools - wie Anthropic Claude, OpenAI ChatGPT, Cursor und Microsoft Copilot Studio -, um ihre tägliche Arbeit zu optimieren. Diese Anwendungen unterstützen das **Model Context Protocol (MCP)**, einen offenen Standard, der es Anwendungen ermöglicht, Backend-Tools auf einheitliche Weise für große Sprachmodelle (LLMs) verfügbar zu machen.

Real-Time CDP bietet jetzt einen MCP-Server, der Zielgruppen-, Ziel- und Aktivierungsvorgänge direkt in jeder MCP-kompatiblen Anwendung aufzeigt. Mit der Real-Time CDP MCP-Integration können verschiedene Benutzertypen um dieselben Segmentierungs- und Aktivierungsdaten zusammenarbeiten, ohne Abfragen an den Adobe Experience Platform REST-APIs zu schreiben oder durch mehrere Bildschirme der Benutzeroberfläche zu navigieren. Kunden können ihre Absichten im Gespräch beschreiben und das LLM die entsprechenden MCP-Tools aufrufen lassen.

## Wichtigste Funktionen {#mcp-capabilities}

Der Real-Time CDP MCP-Server ist **schreibgeschützte Überwachungs** und Triage-Oberfläche. Es stellt APIs für das Abrufen von Zielgruppen, Zielen, Quellen, Identität und Profilauflösung als Klarsprachenantworten innerhalb Ihres KI-Assistenten bereit - ohne Abfragen zu schreiben oder durch Produktbildschirme zu navigieren. Es können keine Daten über den MCP-Server erstellt, geändert oder gelöscht werden.

>[!IMPORTANT]
>
>Alle Tools in der aktuellen Beta **schreibgeschützt**. Schreibvorgänge - einschließlich Erstellen, Aktivieren, Aktualisieren oder Löschen von Zielgruppen, Zielen oder Datenflüssen - werden nicht unterstützt.

Die Beta-Version umfasst die folgenden 18 Tools:

| Tool | Beschreibung |
| --- | --- |
| `search_audiences` | Audiences auflisten und nach Namen, Entitätstyp, Lebenszyklusstatus, Identity-Namespace oder Herkunft suchen. |
| `preview_audience_membership` | Schätzen Sie die Größe eines PQL- oder SDD-Segmentausdrucks, bevor Sie ihn als Zielgruppe speichern. |
| `inspect_audience_evaluation_jobs` | Rufen Sie Datensätze zu Segmentauswertungsaufträgen ab, um zu diagnostizieren, warum eine Batch-Zielgruppe nicht aktualisiert wird, oder um den letzten Auswertungsverlauf zu bestätigen. |
| `inspect_audience_export_jobs` | Rufen Sie Audience-Exportauftragsdatensätze ab, um abgeschlossene Exporte zu bestätigen oder Fehlerdetails aufzudecken. |
| `search_destination_connectors` | Auflisten der in der Plattform verfügbaren Ziel-Connector-Typen (z. B. [!DNL Amazon S3], [!DNL Google Ads], [!DNL Salesforce] CRM). |
| `search_destination_accounts` | Auflisten authentifizierter Zielkonten - konfigurierte Instanzen eines Ziel-Connector-Typs. |
| `search_destination_input_connections` | Rufen Sie die Experience Platform-seitige Eingabe eines Zielflusses ab - die Zielgruppe oder den Datensatz, die bzw. der exportiert wird. |
| `search_destination_output_connections` | Rufen Sie den externen Endpunkt eines Zielflusses ab - Zielpfad, Dateiformat und Versandkonfiguration. |
| `search_destination_flows` | Auflisten und Überprüfen der konfigurierten Zielaktivierungsflüsse, einschließlich ihres Status, ihrer Zuordnungen und ihres Zeitplans. |
| `inspect_flow_runs` | Abrufen des Ausführungsverlaufs für Quell- und Zielflüsse - Status, Timing, Anzahl der Einträge und Fehlerdetails pro Ausführung. |
| `search_source_connectors` | Auflisten der in der Plattform verfügbaren Quell-Connector-Typen. |
| `search_source_accounts` | Auflisten authentifizierter Quellkonten - konfigurierte Instanzen eines Quell-Connector-Typs. |
| `search_source_input_connections` | Rufen Sie die Datenauswahlschicht eines Quellflusses ab - was von einem Konto abgerufen wird. |
| `search_source_output_connections` | Rufen Sie das Experience Platform-Datensatzziel eines Quellflusses ab, in dem aufgenommene Daten landen. |
| `search_source_flows` | Auflisten und Überprüfen der konfigurierten Quell-Aufnahme-Pipelines, einschließlich ihres Status, ihrer Zuordnungen und ihres Zeitplans. |
| `search_identity_namespaces` | Auflisten von Identitäts-Namespace-Definitionen in Ihrer Sandbox - sowohl standardmäßige als auch benutzerdefinierte Namespaces von Adobe. |
| `search_merge_policies` | Listen Sie Zusammenführungsrichtlinien-Datensätze auf, die steuern, wie Echtzeit-Kundenprofile aus Profilfragmenten zusammengestellt werden. |
| `search_organizations` | Listen Sie die Adobe-Organisationen auf, auf die der authentifizierte Benutzer zugreifen kann. |

## Anwendungsszenarien {#mcp-use-cases}

Der Real-Time CDP MCP-Server wurde für **Überwachung und Triage** entwickelt. Da der Server mit IDs statt mit Namen arbeitet, beginnt ein typischer Workflow mit einer Liste - Bitten Sie Claude, Ihnen zu zeigen, was verfügbar ist, wählen Sie das gewünschte Element aus und stellen Sie dann anhand der zurückgegebenen ID Folgefragen.

| Ziel | Beispiel-Eingabeaufforderung |
| --- | --- |
| **Audiences auflisten** | „Listen Sie meine Zielgruppen in der `prod` Sandbox auf.“ |
| **Untersuchen einer bestimmten Zielgruppe** | „Zeigen Sie mir die Details und den Lebenszyklusstatus für die Zielgruppen-ID `abc123`.“ |
| **Diagnostizieren eines Auswertungsfehlers** | „Zeigen Sie mir die neuesten Auswertungsaufträge, und markieren Sie etwaige Fehler.“ |
| **Exportvorgang überprüfen** | „Listen Sie die letzten Audience-Exportaufträge auf und zeigen Sie mir den Status der einzelnen Aufträge an.“ |
| **Schätzen der Zielgruppengröße** | „Schätzen Sie die Größe dieses PQL-Ausdrucks, bevor ich ihn speichern: `homeAddress.country = 'US'`.“ |
| **Auflisten der Connector-Typen für Ziele** | „Welche Ziel-Connector-Typen sind in meiner Sandbox verfügbar?“ |
| **Auflisten der konfigurierten Zielkonten** | „Listen Sie meine Zielkonten und deren Verbindungsstatus auf.“ |
| **Auflisten der Zielflüsse** | „Listen Sie meine Zielaktivierungsflüsse auf und zeigen Sie an, welche aktiviert oder deaktiviert sind.“ |
| **Überprüfen eines Zielflusses** | „Zeigen Sie mir die vollständige Konfiguration für die Ziel-Fluss-ID `xyz789`.“ |
| **Zustand des Zielkontos überprüfen** | „Listen Sie meine Zielkonten auf und markieren Sie alle , die sich in einem Fehlerstatus befinden.“ |
| **Überwachen der letzten Aktivierungsläufe** | „Fluss anzeigen läuft in den letzten 24 Stunden und kennzeichnet Fehler.“ |
| **Untersuchen eines fehlgeschlagenen Durchgangs** | „Anzeigen des Ausführungsverlaufs für Fluss-ID `xyz789` und Zusammenfassung etwaiger Fehler“ |
| **Quellflüsse auflisten** | „Auflisten der Aufnahme-Flüsse meiner Quelle und Anzeigen ihres aktuellen Status.“ |
| **Prüfen eines Quellflusses** | „Zeigen Sie mir die Konfiguration für die Quell-Fluss-ID `src456` - was wird aufgenommen und wo wird es landen?“ |
| **Überprüfen des Ausführungszustands der Aufnahme** | „Aktuelle Ausführungsverläufe für Quellfluss-ID-`src456` und Markierungsfehler anzeigen“ |
| **Identitäts-Namespaces auflisten** | „Welche Identity-Namespaces werden in meiner Sandbox konfiguriert?“ |
| **Zusammenführungsrichtlinien auflisten** | „Listen Sie meine Zusammenführungsrichtlinien auf und zeigen Sie an, welche die Standardeinstellung ist.“ |
| **Organisations-ID suchen** | „Listen Sie die Adobe-Organisationen auf, auf die ich Zugriff habe.“ |

## Zugriff und Aktivierung {#mcp-access}

>[!AVAILABILITY]
>
>Der Real-Time CDP MCP-Server befindet sich in Beta und ist nicht für die Selbstbedienungsregistrierung offen. Der Zugriff erfolgt nur auf Einladung und erfordert, dass Ihre Adobe-Organisation explizit ausgewählt wird, bevor Sie eine Verbindung herstellen können.

So fordern Sie Zugriff an:

1. Wenden Sie sich an Ihren Adobe-Kundenbetreuer (Customer Success Manager, Technical Account Manager oder Account Executive) und bekunden Sie Ihr Interesse am Real-Time CDP MCP Beta-Programm.
2. Der Adobe-Support koordiniert sich mit dem Produkt-Team, um die Eignung zu bewerten und Ihre Organisations-ID zu aktivieren.
3. Nach der Aktivierung bestätigt der Adobe-Support den Zugriff und stellt zusätzliches Onboarding-Material zur Verfügung.

>[!NOTE]
>
>Nur Organisationen, die explizit aktiviert wurden, können eine Verbindung zum Real-Time CDP MCP-Server herstellen. Der Versuch, vor der Aktivierung eine Verbindung herzustellen, führt zu einem Authentifizierungsfehler.

## Voraussetzungen {#mcp-prerequisites}

Stellen Sie vor dem Verbinden des Real-Time CDP-MCP-Servers mit dem MCP-Client Folgendes sicher:

* Sie besitzen eine aktive Real-Time CDP-Lizenz.
* Ihre Adobe-Organisation wurde von Ihrem Adobe-Support-Mitarbeiter für das Beta-Programm aktiviert (siehe [Zugriff und Aktivierung](#mcp-access)).
* Sie haben Zugriff auf einen unterstützten MCP-Client wie [!DNL Claude], [!DNL ChatGPT], [!DNL Claude Code], [!DNL Codex], [!DNL Cursor] oder [!DNL VS Code].
* Sie haben Ihre Organisations-ID und den Namen der Sandbox, die Sie abfragen möchten.
* Sie verfügen in Adobe Experience Platform über die erforderlichen Berechtigungen zum Anzeigen von Zielgruppen, Zielen und Flow Service-Entitäten.

## Real-Time CDP MCP-Server verbinden {#mcp-connect}

Der Real-Time CDP MCP-Server-Endpunkt ist:

```
https://rtcdp-mcp.adobe.io/mcp
```

Der Server verwendet einen **Remote-HTTP (Streamable HTTP**-Transport) mit einem **browserbasierten Adobe-Anmeldefluss**. In jedem Client ist das Setup-Muster gleich:

1. Fügen Sie die Server-URL hinzu: `https://rtcdp-mcp.adobe.io/mcp`
2. Speichern oder aktivieren Sie die Verbindung.
3. Schließen Sie die **Browser-basierte Adobe-Anmeldung** ab, wenn der Client zum ersten Mal ein Tool aufruft.
4. Geben Sie `imsOrgId` und `sandboxName` zu Beginn jeder Sitzung an.

### Allgemeine JSON-Konfiguration {#mcp-connect-json}

Für Clients, die eine JSON-basierte MCP-Server-Konfiguration akzeptieren - wie Claude Desktop (`claude_desktop_config.json`), VS Code oder jeder Client, der eine `mcp.json`-Datei liest - verwenden Sie eines der folgenden Formate, je nachdem, ob Ihr Client natives Remote-HTTP unterstützt oder eine lokale Bridge benötigt:

**Über `mcp-remote` Bridge (Claude Desktop und andere Clients, die eine lokale Bridge benötigen)**

```json
{
  "mcpServers": {
    "rtcdp": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://rtcdp-mcp.adobe.io/mcp"
      ]
    }
  }
}
```

**Natives Remote-HTTP (Clients, die es direkt unterstützen)**

```json
{
  "mcpServers": {
    "rtcdp": {
      "url": "https://rtcdp-mcp.adobe.io/mcp",
      "transport": "http"
    }
  }
}
```

>[!NOTE]
>
>In der Konfiguration sind keine API-Schlüssel, Bearer-Token oder zusätzlichen Header erforderlich. Die Authentifizierung wird bei der ersten Verwendung vollständig über den Browser-basierten Adobe-Anmeldefluss durchgeführt.

### Installieren in benutzeroberflächenbasierten Clients {#mcp-connect-ui}

#### Claude

Fügen Sie für `claude.ai` und Claude Desktop den Real-Time CDP-MCP-Server als **benutzerdefinierten Connector)** der Server-URL-`https://rtcdp-mcp.adobe.io/mcp` hinzu.

* **Individuelle Pläne** - Navigieren Sie in Claude zu **Anpassen → Connectoren**, wählen Sie **Connector hinzufügen** aus und geben Sie die Server-URL ein.
* **Team- und Unternehmenspläne** - Ein Arbeitsbereich **Verantwortlicher** oder **Primärer Verantwortlicher** fügt den Connector unter **Organisationseinstellungen → Connectoren** hinzu. Nach dem Hinzufügen aktiviert jeder Benutzer sie in seinen eigenen Claude-Einstellungen.

Nachdem der Connector hinzugefügt wurde, aktivieren Sie ihn in einer Konversation und schließen Sie die Adobe-Browser-Anmeldung bei der ersten Verwendung ab. Claude erkennt den Adobe-Autorisierungsserver automatisch - es ist keine Client-ID oder kein Client-Geheimnis erforderlich.

#### ChatGPT

Fügen Sie [!DNL ChatGPT] den Real-Time CDP-MCP-Server als **benutzerdefinierten Connector“**:

1. Navigieren Sie zu **Einstellungen → Connectoren** (oder **Einstellungen → Apps und Connectoren** je nach Plan).
2. Wählen Sie **Connector hinzufügen** aus und geben Sie `https://rtcdp-mcp.adobe.io/mcp` als Server-URL ein.
3. Speichern Sie den Connector. Abhängig von Ihrem [!DNL ChatGPT] kann dieser Schritt die Genehmigung **Entwicklermodus** oder des Arbeitsbereich-Administrators erfordern.
4. Sobald der Connector aktiviert ist, authentifizieren Sie sich über die Adobe-Browser-Anmeldung, wenn Sie bei der ersten Verwendung dazu aufgefordert werden.

#### Cursor

Fügen Sie in Cursor den Real-Time CDP MCP-Server als Remote-MCP-Server hinzu:

1. Öffnen Sie **Einstellungen → MCP**.
2. Wählen Sie **Neuen Server hinzufügen** aus und geben Sie `https://rtcdp-mcp.adobe.io/mcp` als Server-URL ein.
3. Wählen Sie **Verbinden** aus, um den Trigger für die Browser-basierte Adobe-Anmeldung zu erstellen und sich zu authentifizieren.

Sobald die Verbindung hergestellt ist, sind die Real-Time CDP-Tools im Cursor-Composer- und Agenten-Modus verfügbar.

#### Andere benutzeroberflächenbasierte Clients

Fügen Sie für Clients wie VS Code oder andere Desktop- und Web-Anwendungen mit Remote-MCP-Unterstützung den Real-Time CDP MCP-Server als **Remote-HTTP**-Server mit `https://rtcdp-mcp.adobe.io/mcp` hinzu. Wenn der Client optionale Kopfzeilen oder Bearer-Token unterstützt, lassen Sie diese leer - die Authentifizierung wird bei der ersten Verwendung über den browserbasierten Adobe-Anmeldefluss durchgeführt.

### Installation in technischen Clients {#mcp-connect-technical}

#### Claude Code

Fügen Sie den Server vom Terminal aus hinzu:

```bash
claude mcp add --transport http rtcdp https://rtcdp-mcp.adobe.io/mcp
```

Starten Sie dann Claude Code und führen Sie Folgendes aus:

```text
/mcp
```

Wählen Sie den `rtcdp` aus und schließen Sie den Anmeldevorgang für Adobe in Ihrem Browser ab. Wenn Sie den Server bereits in `claude.ai` hinzugefügt haben, wird er möglicherweise automatisch im Claude-Code angezeigt, wenn beide bei demselben Konto angemeldet sind.

#### Codex

Fügen Sie den Server vom Terminal aus hinzu:

```bash
codex mcp add rtcdp --url https://rtcdp-mcp.adobe.io/mcp
```

Server authentifizieren:

```bash
codex mcp login rtcdp
```

Überprüfen Sie die Konfiguration:

```bash
codex mcp list
```

Sie können den Server auch direkt zu `~/.codex/config.toml` hinzufügen:

```toml
[mcp_servers.rtcdp]
url = "https://rtcdp-mcp.adobe.io/mcp"
```

### Erforderliche Anfrageparameter {#mcp-connect-params}

Jeder Tool-Aufruf erfordert zwei Parameter, die die Anfrage an Ihren Adobe Experience Platform-Mandanten ausrichten:

* `imsOrgId` - Ihre Organisations-ID, die der `x-gw-ims-org-id`-Kopfzeile bei nachgelagerten Experience Platform-API-Aufrufen zugeordnet ist.
* `sandboxName` - Der Experience Platform-Sandbox-Name, der der `x-sandbox-name`-Kopfzeile zugeordnet ist.

Stellen Sie diese zu Beginn jeder Sitzung bereit. Beispiel:

> „Verwenden Sie `1234ABCD@AdobeOrg` und Sandbox-`prod` für diese Sitzung.“

Wenn Sie Ihre Organisations-ID nicht kennen, bitten Sie Ihren KI-Assistenten, `search_organizations` anzurufen. Er gibt jede Organisation zurück, auf die Ihre Adobe-Anmeldeinformationen zugreifen können.

## Bekannte Einschränkungen (Beta) {#mcp-limitations}

Die folgenden Einschränkungen gelten für die aktuelle Beta-Version des [!DNL Adobe Real-Time CDP] MCP-Servers:

| Einschränkung | Beschreibung | Problemumgehung |
| --- | --- | --- |
| **Schreibgeschützte Oberfläche** | Der MCP-Server stellt nur APIs zum Abrufen bereit. Zielgruppen, Ziele oder Datenflüsse können nicht erstellt, aktualisiert, aktiviert oder gelöscht werden. | Verwenden Sie die Real-Time CDP-Benutzeroberfläche oder die Experience Platform-REST-APIs für Schreibvorgänge. |
| **Keine Interaktions- oder Versandmetriken** | Der MCP-Server gibt keine nachgelagerten Versandstatistiken, Interaktions- oder Konversionsmetriken von Zielplattformen zurück. | Verwenden Sie die eigenen Berichte der Zielplattform, Customer Journey Analytics MCP oder Adobe Analytics MCP für Interaktions- und Konversionsdaten. |
| **Segmentabfrage muss extern erstellt werden** | `Preview Audience Membership` erfordert einen gültigen PQL- oder SDD-Ausdruck als Eingabe. Der MCP-Server erstellt die Abfrage nicht für Sie. | Erstellen Sie den PQL/SDD-Ausdruck in der Segment Builder-Benutzeroberfläche oder über die Segmentierungs-Service-API und fügen Sie ihn dann in die MCP-Eingabeaufforderung ein. |
| **Paginierung über Fortsetzungs-Token** | Listen-Tools geben paginierte Ergebnisse zurück. Für eine vollständige Auflistung über sehr große Sandboxes müssen `continuationToken` verkettet werden. | Engen Sie Abfragen mithilfe von Filtern (Name, Status, Verbindungsspezifikation, Zeitraum) ein, anstatt die vollständige Liste aufzuzählen. |
| **Die Filterung des Aktivierungsdurchgangs ist nur zeitbasiert** | `Inspect Activation Runs` unterstützt das Filtern nach Status und Abschlusszeitstempel (Epoche ms UTC), jedoch nicht direkt nach Fehlertyp oder Zielplattform. | Filtern Sie nach `flowId` ersten (von `List Configured Destinations` abgerufenen) Durchläufen zum Bereich, der für ein bestimmtes Ziel bestimmt ist. |
| **Organisations-ID erforderlich beim Sitzungsstart** | Jeder Tool-Aufruf (außer `search_organizations`) erfordert `imsOrgId` und `sandboxName` als explizite Parameter. Wenn diese nicht angegeben werden, schlagen Tool-Aufrufe fehl. | Teilen Sie Ihrem KI-Assistenten am Anfang jeder Sitzung mit: „Verwenden Sie `<YOUR_ORG_ID>` und Sandbox-`<SANDBOX_NAME>` für diese Sitzung.“ Wenn Sie Ihre Organisations-ID nicht kennen, rufen Sie zuerst `search_organizations` auf. Es werden die Organisationen zurückgegeben, auf die Ihre Anmeldeinformationen zugreifen können. |

## Häufig gestellte Fragen {#mcp-faq}

+++Welche MCP-Clients werden unterstützt?

Der Real-Time CDP MCP-Server funktioniert mit jedem Client, der Remote-MCP-Server oder benutzerdefinierte Connectoren unterstützt - einschließlich [!DNL Claude], [!DNL ChatGPT], [!DNL Claude Code], [!DNL Codex], [!DNL Cursor] und [!DNL VS Code]. Der Einrichtungsfluss hängt vom Client ab: Benutzeroberflächenbasierte Clients fügen den Server normalerweise über ein Einstellungen- oder Connectoren-Bedienfeld hinzu, während technische Clients wie Claude Code und Codex ihn über die Befehlszeile oder Konfigurationsdateien hinzufügen können.
+++

+++Wie erhalte ich Zugriff?

Der Zugriff erfolgt nur auf Einladung während der Beta. Wenden Sie sich an Ihren Adobe-Kundenbetreuer (Customer Success Manager, Technical Account Manager oder Account Executive), um eine Registrierung anzufordern. Der Adobe-Support koordiniert sich mit dem Produkt-Team, um Ihr Unternehmen zu unterstützen. Weitere Informationen [&#x200B; Sie unter &#x200B;](#mcp-access) und Aktivierung .
+++

+++Wie funktioniert die Authentifizierung?

Die Authentifizierung erfolgt über eine **Browser-basierte Anmeldung**. Wenn Ihr MCP-Client zum ersten Mal ein Tool aufruft, wird Ihr Standardbrowser auf einer Adobe-Anmeldeseite geöffnet. Nachdem Sie sich authentifiziert und den Client autorisiert haben, wird die Sitzung eingerichtet und die nachfolgenden Tool-Aufrufe verwenden sie erneut. In Ihrer Client-Konfiguration müssen keine API-Schlüssel oder langlebigen Anmeldedaten gespeichert werden.
+++

+++Auf welche Real-Time CDP-Objekte kann ich über MCP zugreifen?

Sie können auf Zielgruppen, Zieltypen, konfigurierte Zielkonten, Zieldatenflüsse, Quell- und Zielverbindungen und den Ausführungsverlauf der Aktivierung zugreifen. Vorgänge sind schreibgeschützt (APIs abrufen); Schreibvorgänge werden in der aktuellen Version nicht unterstützt.
+++

+++Benötige ich Entwicklerzugriff, um den Real-Time CDP MCP-Server zu verwenden?

Nein. Der MCP-Server ist sowohl für Marketing- als auch für technische Personas konzipiert. Marketing-Experten können mit ihr über natürliche Spracheingaben in jedem unterstützten MCP-Client interagieren, während Dateningenieure und Entwickler sie in Entwickler-Tools verwenden können, die MCP unterstützen.
+++

