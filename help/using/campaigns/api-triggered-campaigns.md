---
solution: Journey Optimizer
product: journey optimizer
title: Auslösen von Kampagnen mit APIs
description: Auslösen von Kampagnen mit Journey Optimizer-APIs
topic: Content Management
role: Developer, Admin
level: Intermediate, Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 11c1945f8e7f7ca74a2c9ca33ff85fea77bcf5db
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 77%

---

# Auslösen von Kampagnen mit APIs {#trigger-campaigns}

## Über von einer API ausgelöste Kampagnen {#about}

Mit [!DNL Journey Optimizer] können Sie Kampagnen erstellen und diese dann in einem externen System über eine [Interactive Message Execution REST-API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) auslösen. Auf diese Weise können Sie verschiedene Marketing- und Transaktionsnachrichten abdecken, wie z. B. Kennwortrücksätze, OTP-Token usw.

Dazu müssen Sie zunächst in Journey Optimizer eine von einer API ausgelöste Kampagne erstellen und deren Ausführung dann über einen API-Aufruf starten.

Für von einer API ausgelöste Kampagnen stehen die Kanäle E-Mail, SMS und Push-Benachrichtigungen zur Verfügung.

## Erstellen einer von einer API ausgelösten Kampagne {#create}

### Konfigurieren und Aktivieren der Kampagne {#create-activate}

Gehen Sie wie folgt vor, um eine API-gesteuerte Kampagne zu erstellen. Detaillierte Informationen zum Erstellen einer Kampagne finden Sie in [diesem Abschnitt](create-campaign.md).

1. Erstellen Sie eine neue Kampagne vom Typ **[!UICONTROL API-ausgelöst]**.

1. Wählen Sie die **[!UICONTROL Marketing]** oder **[!UICONTROL Transactional]** je nach dem zu sendenden Kommunikationstyp.

1. Wählen Sie einen der unterstützten Kanäle und die zugehörige Kanaloberfläche für den Nachrichtenversand aus und klicken Sie auf **[!UICONTROL Erstellen]**.

   ![](assets/api-triggered-type.png)

   >[!NOTE]
   >
   >Derzeit wird die schnelle Bereitstellung für Kampagnen, die von der Push-Benachrichtigungs-API ausgelöst werden, nicht unterstützt.

1. Geben Sie einen Titel und eine Beschreibung für die Kampagne an und klicken Sie dann auf **[!UICONTROL Inhalt bearbeiten]**, um die zu sendende Nachricht zu konfigurieren.

   >[!NOTE]
   >
   >Sie können an die API-Payload zusätzliche Daten zur Nachrichtenpersonalisierung übergeben. [Weitere Informationen](#contextual)
   >
   >Die Verwendung einer großen Zahl oder umfangreicher kontextuelle Daten in Ihren Inhalten kann die Leistung beeinträchtigen.

1. Im **[!UICONTROL Zielgruppe]** Geben Sie den Namespace an, der zur Identifizierung der Kontakte verwendet werden soll.

   * Wenn Sie eine **transactional**-Typ Kampagne, müssen die Zielgruppenprofile im API-Aufruf definiert werden. Die Option **[!UICONTROL Erstellen neuer Profile]** ermöglicht es Ihnen, automatisch Profile zu erstellen, die nicht in der Datenbank vorhanden sind. [Erfahren Sie mehr über die Erstellung von Profilen bei der Kampagnenausführung](#profile-creation)

   * Für **Marketing**-type campaigns, klicken Sie auf die **[!UICONTROL Zielgruppe]** zur Auswahl der Zielgruppe.

1. Konfigurieren Sie das Start- und Enddatum der Kampagne.

   Wenn Sie ein bestimmtes Start- und/oder Enddatum für eine Kampagne konfigurieren, wird diese nicht außerhalb dieses Zeitraums ausgeführt und API-Aufrufe schlagen fehl, wenn eine Kampagne durch APIs ausgelöst wird.

1. Klicken Sie auf **[!UICONTROL Zum Aktivieren überprüfen]**, um sicherzustellen, dass Ihre Kampagne korrekt konfiguriert ist, und aktivieren Sie sie.

Sie können die Kampagne jetzt über die APIs ausführen. [Weitere Informationen](#execute)

### Ausführen der Kampagne {#execute}

Nachdem Ihre Kampagne aktiviert wurde, müssen Sie die generierte Beispiel-cURL-Anfrage abrufen und in der API verwenden, um Ihre Payload zu erstellen und die Kampagne auszulösen.

1. Öffnen Sie die Kampagne und kopieren Sie dann die Beispielanfrage aus dem Abschnitt **[!UICONTROL cURL-Anfrage]**.

   ![](assets/api-triggered-curl.png)

1. Verwenden Sie diese cURL-Anfrage in den APIs, um Ihre Payload zu erstellen und die Kampagne auszulösen. Weitere Informationen finden Sie in der [Dokumentation zur API für die Ausführung interaktiver Nachrichten](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

   Beispiele für API-Aufrufe finden Sie auch in [diese Seite](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Beachten Sie, dass, wenn Sie bei der Erstellung der Kampagne ein bestimmtes Start- und/oder Enddatum konfiguriert haben, die Kampagne außerhalb dieses Zeitraums nicht ausgeführt wird und API-Aufrufe fehlschlagen.

## Verwenden von kontextuellen Attributen in von einer API ausgelösten Kampagnen {#contextual}

Bei von einer API ausgelösten Kampagnen können Sie zusätzliche Daten in die API-Payload übertragen und innerhalb der Kampagne nutzen, um Ihre Nachricht zu personalisieren.

In diesem Beispiel möchten Kunden ihr Kennwort zurücksetzen. Sie senden ihnen deshalb zum Zurücksetzen des Kennworts eine URL, die in einem Drittanbieter-Tool generiert wird. Bei von einer API ausgelösten Kampagnen können Sie diese generierte URL in die API-Payload übergeben und in der Kampagne in die Nachricht einfügen.

>[!NOTE]
>
>Im Gegensatz zu profilaktivierten Ereignissen werden die in der REST-API übergebenen kontextuellen Daten für die einmalige Kommunikation verwendet und nicht im Profil gespeichert. Das Profil wird nur mit den Namespace-Details erstellt, falls es nicht vorhanden ist.

Um diese Daten in Ihren Kampagnen verwenden zu können, müssen Sie sie an die API-Payload übergeben und mithilfe des Ausdruckseditors zu Ihrer Nachricht hinzufügen. Verwenden Sie dazu die Syntax `{{context.<contextualAttribute>}}`, wobei `<contextualAttribute>` mit dem Namen der Variablen in Ihrer API-Payload, die die zu übergebenden Daten enthält, übereinstimmen muss.

Die Syntax `{{context.<contextualAttribute>}}` ist nur einem Zeichenfolgen-Datentyp zugeordnet.

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>Die in die Anfrage übergebenen Kontextattribute dürfen 50 KB nicht überschreiten und sind stets vom Typ Zeichenfolge abhängig.
>
>Die Syntax `context.system` ist auf die interne Nutzung bei Adobe beschränkt und sollte nicht zur Weitergabe von kontextuellen Attributen verwendet werden.

Beachten Sie, dass im Menü in der linken Leiste derzeit kein kontextuelles Attribut verfügbar ist. Attribute müssen direkt in Ihren Personalisierungsausdruck eingegeben werden, ohne dass eine Überprüfung durch [!DNL Journey Optimizer] durchgeführt wird.

## Profilerstellung bei der Kampagnenausführung {#profile-creation}

In einigen Fällen müssen Sie möglicherweise Transaktionsnachrichten an Profile senden, die nicht im System sind. Wenn zum Beispiel ein unbekannter Benutzer versucht, sein Kennwort auf Ihrer Website zurückzusetzen.

Wenn ein Profil nicht in der Datenbank vorhanden ist, erlaubt Journey Optimizer Ihnen, es automatisch bei der Ausführung der Kampagne zu erstellen, um das Senden der Nachricht an dieses Profil zu ermöglichen.

>[!IMPORTANT]
>
>Bei Transaktionsnachrichten ist diese Funktion verfügbar für **Profilerstellung mit sehr geringem Volumen** in einem Anwendungsfall für den Versand von Transaktionsnachrichten mit großem Volumen, wobei ein Großteil der Profile bereits in der Plattform vorhanden ist.

Um die Profilerstellung bei der Kampagnenausführung zu aktivieren, schalten Sie die Option **[!UICONTROL Neue Profile erstellen]** im Abschnitt **[!UICONTROL Audience]** ein. Wenn diese Option deaktiviert ist, werden unbekannte Profile für jeden Versand zurückgewiesen und der API-Aufruf schlägt fehl.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>Unbekannte Profile werden im **Profil-Datensatz von AJO Interactive Messaging** erstellt, und zwar in drei Standard-Namespaces (E-Mail, Telefon und ECID) für jeden ausgehenden Kanal (E-Mail, SMS und Push).
