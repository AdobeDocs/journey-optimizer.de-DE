---
solution: Journey Optimizer
product: journey optimizer
title: URL-Parameter verschlüsseln
description: Erfahren Sie, wie Sie sensible URL-Abfrageparameter verschlüsseln, damit personenbezogene Daten nicht im Klartext auf Journey Optimizer-Tracking-Links und Landingpages verfügbar gemacht werden.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
keywords: Verschlüsselung, URL, Tracking, Landingpage, Schlüsselregistrierung, Personalisierung, Sicherheit, Datenschutz, Sandbox
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
source-git-commit: 5c8d615b5f6b2c2cb80a21c59f3ea5f12325e6fd
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 4%

---

# URL-Parameter verschlüsseln {#url-parameter-encryption}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.
>
>Diese Funktion ist derzeit nur für den E-Mail-Kanal verfügbar.

## Warum URL-Parameterverschlüsselung verwenden? {#why-url-parameter-encryption}

Personalisierte Tracking-Links und Landingpage-URLs enthalten oft Profilattribute, Kennungen, Token oder andere Werte in der Abfragezeichenfolge. Diese Parameter sind in der Regel als Nur-Text in der E-Mail oder SMS sichtbar und bleiben lesbar, wenn jemand den Link kopiert, freigibt oder Lesezeichen hinzufügt. Dies kann ein Sicherheits- und Datenschutzrisiko darstellen, wenn die Werte personenbezogene Daten (PII) oder andere sensible Daten enthalten können, die sie schützen müssen.

[!DNL Journey Optimizer] bietet einen Verschlüsselungs-Helper im Personalisierungseditor, mit dem Sie jeden Ausdruckswert zum Rendern verschlüsseln können (z. B. ein Profilattribut, ein Token oder eine Zeichenfolge, die Sie aus mehreren Feldern erstellt haben). Die Verschlüsselung erfordert immer einen Schlüssel aus der Registrierung Ihres Unternehmens.

Sie verschlüsseln nur die ausgewählten Abfrageparameter mithilfe von Schlüsseln, die Administratoren in einer Registrierung auf Sandbox-Ebene verwalten, sodass vertrauliche Werte nicht im Klartext offen gelegt werden, wenn der Link freigegeben oder überprüft wird.

### Funktionsweise {#how-it-works}

* **Administratoren** verwenden die Schlüsselregistrierung, um [Schlüssel zu erstellen](#create-keys) und [Schlüssel zu verwalten](#manage-keys) in Übereinstimmung mit den Sicherheitsrichtlinien Ihrer Organisation.
* **Marketingexperten** Fügen Sie den `Encrypt` Helper in den Personalisierungseditor ein und übergeben Sie den zu schützenden Wert sowie eine aktive Schlüsselkennung aus der Registrierung. Syntax und Optionen finden Sie [diesem Abschnitt](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>Die Entschlüsselung liegt in der Verantwortung Ihres Unternehmens. [!DNL Journey Optimizer] verschlüsselt Werte beim Rendern der Nachricht. Ihre Website, Ihr Programm oder Ihre API muss Parameter mit demselben kryptografischen Material und denselben Prozessen entschlüsseln, die Sie definieren - im Einklang mit Ihrem Sicherheitsmodell.

### Beispiel

Eine Landingpage-URL verwendet möglicherweise einen Abfrageparameter wie `token`, dessen Wert ein Zeichenfolgen-Token ist (z. B. eine JSON-Payload mit Angebots- oder Profilkennungen). Ohne Verschlüsselung ist dieses Zeichenfolgen-Token als einfacher Text im Link sichtbar. Wenn dieser Wert mit dem Verschlüsselungs-Helper umschlossen wird, wird die sensible Payload durch Chiffretext in der URL ersetzt, während der Rest des Links unverändert bleibt.

## Schlüssel erstellen {#create-keys}

Bevor Sie den URL-Parameter-Verschlüsselungs-Helper verwenden können, müssen Sie einen Schlüssel erstellen. Gehen Sie dazu wie folgt vor.

>[!NOTE]
>
>Derzeit gibt es keine spezifischen Berechtigungen zum Zugreifen auf und Verwalten von Schlüsseln. Rollen, die Zugriff auf den Abschnitt **[!UICONTROL Konfigurationen]** unter **[!UICONTROL Administration]** gewähren, gewähren auch Zugriff auf die Schlüsselregistrierung. Spezifische Berechtigungen sind jedoch für eine zukünftige Version geplant.

<!--
>[!IMPORTANT]
>
>To access and manage keys, you you must have the **View Key Registry** and **Manage Key Registry** permissions granted. [Learn more](../administration/high-low-permissions.md)
-->

1. Navigieren Sie **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]**.

1. Klicken Sie auf **[!UICONTROL Verwalten]**, um die **[!UICONTROL Schlüsselregistrierung]** zu öffnen.

   ![Abschnitt „Schlüsselregistrierung“ im Menü Administration](assets/encryption-key-registry.png){width="80%"}

1. Erstellen Sie über die entsprechende Schaltfläche nach Bedarf Schlüssel für Ihre Organisation.

   ![Schaltfläche „Schlüssel erstellen“ im Abschnitt „Schlüsselregistrierung“](assets/encryption-create-key.png){width="80%"}

1. Weisen Sie ihnen eine klare Beschriftung oder Kennung zu, auf die Ihre Teams im Personalisierungseditor verweisen können.

   ![Schlüsseldetails im Abschnitt „Schlüsselregistrierung“](assets/encryption-key-details.png){width="80%"}

1. Klicken Sie auf **[!UICONTROL Senden]**, um Ihre Änderungen zu bestätigen.

Sobald ein Schlüssel erstellt wurde, können Marketing-Experten den [URL-Parameterverschlüsselung](functions/helpers.md#url-parameter-encryption-helper)-Helfer im Personalisierungseditor verwenden, um bestimmte Werte zu verschlüsseln, die sie in URL-Abfrageparametern platzieren.

## Schlüssel verwalten {#manage-keys}

Gehen Sie wie folgt vor, um Schlüssel zu verwalten.

1. Rufen Sie die **[!UICONTROL Schlüsselregistrierung“]**. Sie können alle für die aktuelle Sandbox erstellten Schlüssel in einer Listenansicht anzeigen.

   ![Listenansicht der Schlüsselregistrierung](assets/encryption-key-registry-list.png){width="100%"}

1. Klicken Sie auf einen Schlüssel mit dem Status **[!UICONTROL Aktiv]**, um die Schlüsseldetails zu öffnen.

   ![Details zum aktiven Schlüssel](assets/encryption-key-active-details.png){width="80%"}

1. Klicken Sie auf **[!UICONTROL Widerrufen]**, um den Schlüssel für die neue Verschlüsselung dauerhaft zu deaktivieren.

   Sobald ein Schlüssel widerrufen wurde, sollte der Versuch, ihn im Helper zu verwenden, zum Zeitpunkt des Renderings fehlschlagen. Gesperrte Einträge bleiben für die Prüfung sichtbar. Ihre Teams benötigen möglicherweise weiterhin das entsprechende Material, um ältere Payloads auf Ihren eigenen Systemen zu entschlüsseln.

1. Klicken Sie auf **[!UICONTROL Drehen]**, um neues Schlüsselmaterial bereitzustellen und gleichzeitig eine stabile Schlüsselkennung beizubehalten, auf die Ihre Journey und Kampagnen bereits verweisen.

   Das frühere Material wird mit dem Status „widerrufen“ und einem entsprechenden Grund (z. B. einem Rotationszeitstempel) in der Registrierung beibehalten, und eine neue Zeile oder Version spiegelt den aktiven Schlüssel wider.

   >[!NOTE]
   >
   >Es sollten nur aktive Schlüssel ausgewählt werden, um neue Werte im Personalisierungseditor zu verschlüsseln. Verwenden Sie keine widerrufenen Schlüssel für neue Inhalte.
