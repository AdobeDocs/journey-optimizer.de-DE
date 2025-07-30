---
solution: Journey Optimizer
product: journey optimizer
title: Bearbeiten des Inhalts einer Kampagne, die durch API ausgelöst wird
description: Informationen zum Bearbeiten des Inhalts einer Kampagne, die durch API ausgelöst wird.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
exl-id: b7f12c65-c1af-4c49-b126-c13a51940a43
source-git-commit: 45c95d5682b35c8afb161b75c88942c010b36d1c
workflow-type: ht
source-wordcount: '385'
ht-degree: 100%

---

# Bearbeiten des Inhalts einer Kampagne, die durch API ausgelöst wird {#api-content}

Um den Nachrichteninhalt zu konfigurieren, navigieren Sie zur Registerkarte **[!UICONTROL Inhalt]** oder klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**.

![](assets/campaign-content.png)

## Entwerfen des Inhalts {#design}

Der Prozess der Inhaltserstellung hängt vom ausgewählten Kanal ab. Auf den folgenden Seiten erfahren Sie, wie Sie Ihren Nachrichteninhalt erstellen:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="E-Mail" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>E-Mail</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="Push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>Push-Benachrichtigung</strong></a></div></td>
</tr></table>

## Personalisieren von Inhalten mit kontextuellen Daten {#contextual}

Sie können zusätzliche Daten zur Personalisierung Ihrer Nachricht an die API-Payload übergeben.

In diesem Beispiel möchten Kunden ihr Kennwort zurücksetzen. Sie senden ihnen deshalb zum Zurücksetzen des Kennworts eine URL, die in einem Drittanbieter-Tool generiert wird. Bei von einer API ausgelösten Kampagnen können Sie diese generierte URL in die API-Payload übergeben und in der Kampagne in die Nachricht einfügen.

Dazu müssen Sie sie an die API-Payload übergeben und mithilfe des Personalisierungseditors in Ihre Nachricht einfügen.  Verwenden Sie die Syntax `{{context.<contextualAttribute>}}`, wobei `<contextualAttribute>` mit dem Namen der Variablen in Ihrer API-Payload übereinstimmen muss, die die zu übergebenden Daten enthält.

Beachten Sie, dass im Menü in der linken Leiste derzeit kein kontextuelles Attribut verfügbar ist. Attribute müssen direkt in Ihren Personalisierungsausdruck eingegeben werden, ohne dass eine Überprüfung durch [!DNL Journey Optimizer] durchgeführt wird.

![](assets/api-triggered-context.png)

**Unbedingt lesen**

* Die in die Anfrage übergebenen Kontextattribute dürfen 200 KB nicht überschreiten und sind stets vom Typ „Zeichenfolge“.
* Die Syntax `context.system` ist auf die interne Nutzung bei Adobe beschränkt und sollte nicht zur Weitergabe von kontextuellen Attributen verwendet werden.
* Im Gegensatz zu profilaktivierten Ereignissen werden die in der REST-API übergebenen kontextuellen Daten für die einmalige Kommunikation verwendet und nicht im Profil gespeichert. Das Profil wird nur mit den Namespace-Details erstellt, falls es nicht vorhanden ist.
* Die Verwendung einer großen Zahl oder umfangreicher kontextueller Daten in Ihren Inhalten kann die Performance beeinträchtigen.

## Testen und Überprüfen Ihres Inhalts

Nachdem der Inhalt definiert ist, verwenden Sie die Schaltfläche **[!UICONTROL Inhalt simulieren]**, um eine Vorschau anzuzeigen und den Inhalt mit Testprofilen oder Beispieleingabedaten zu testen, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Informationen zum Anzeigen von Inhalten in der Vorschau und Testen von Inhalten](../content-management/preview-test.md). Klicken Sie auf den Linkspfeil, um zum Bildschirm der Kampagnenerstellung zurückzukehren.

![](assets/create-campaign-design.png)

## Nächste Schritte {#next}

Sobald die Konfiguration und der Inhalt Ihrer Kampagne fertiggestellt sind, können Sie die Zielgruppe der Kampagne definieren. [Weitere Informationen](api-triggered-campaign-audience.md)
