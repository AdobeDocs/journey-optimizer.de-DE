---
solution: Journey Optimizer
product: journey optimizer
title: URL-Parameter verschlüsseln
description: Erfahren Sie, wie Sie sensible URL-Abfrageparameter verschlüsseln, damit personenbezogene Daten nicht im Klartext auf Journey Optimizer-Tracking-Links und Landingpages verfügbar gemacht werden.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
keywords: Verschlüsselung, URL, Tracking, Landingpage, Schlüsselregistrierung, Personalisierung, Sicherheit, Datenschutz, Sandbox
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1348
ht-degree: 1%

---

# URL-Parameter verschlüsseln {#url-parameter-encryption}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie sensible URL-Abfrageparameter verschlüsseln, damit persönlich identifizierbare Informationen nicht im Klartext bereitgestellt werden, einschließlich der Methode zum Erstellen, Drehen und Widerrufen von Schlüsseln in der Sandbox-Schlüsselregistrierung von Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
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

>[!IMPORTANT]
>
>Um auf Schlüssel zuzugreifen und sie zu verwalten, benötigen Sie die Berechtigungen **Schlüsselregistrierung anzeigen** und **Schlüsselregistrierung verwalten**. [Weitere Informationen](../administration/high-low-permissions.md#administration-permissions)

1. Navigieren Sie **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]**.

1. Klicken Sie auf **[!UICONTROL Verwalten]**, um die **[!UICONTROL Schlüsselregistrierung]** zu öffnen.

   ![Abschnitt „Schlüsselregistrierung“ im Menü Administration](assets/encryption-key-registry.png){width="80%"}

1. Erstellen Sie über die entsprechende Schaltfläche nach Bedarf Schlüssel für Ihre Organisation.

   ![Schaltfläche „Schlüssel erstellen“ im Abschnitt „Schlüsselregistrierung“](assets/encryption-create-key.png){width="80%"}

1. Weisen Sie ihnen eine klare Beschriftung oder Kennung zu, auf die Ihre Teams im Personalisierungseditor verweisen können.

   ![Schlüsseldetails im Abschnitt „Schlüsselregistrierung“](assets/encryption-key-details.png){width="80%"}

1. Klicken Sie auf **[!UICONTROL Senden]**, um Ihre Änderungen zu bestätigen.

Sobald ein Schlüssel erstellt wurde, können Marketing-Experten den [URL-Parameterverschlüsselung](functions/helpers.md#url-parameter-encryption-helper)-Helfer im Personalisierungseditor verwenden, um bestimmte Werte zu verschlüsseln, die sie in URL-Abfrageparametern platzieren.

## Verwalten von Schlüsseln {#manage-keys}

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

## Kurzübersicht {#quick-reference}

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

>[!BEGINTABS]

>[!TAB Übersicht]

**TL;DR**

Auf dieser Seite wird erläutert, wie Administratoren Verschlüsselungsschlüssel in der Journey Optimizer-Sandbox-Schlüsselregistrierung erstellen, drehen und widerrufen, sodass Marketer sensible URL-Abfrageparameter verschlüsseln können, sodass personenbezogene Daten nicht im Klartext in Tracking-Links und Landingpages verfügbar sind.

**Intents**

* Erfahren Sie, warum eine Verschlüsselung von URL-Parametern erforderlich ist (vertrauliche Daten und personenbezogene Daten, die in Nur-Text-Abfragezeichenfolgen sichtbar sind)
* Erstellen von Verschlüsselungsschlüsseln in der Sandbox-Schlüsselregistrierung (Administratoraufgabe, für die spezifische Berechtigungen erforderlich sind)
* Schlüssel widerrufen, um ihn für neue Verschlüsselung dauerhaft zu deaktivieren
* Drehen Sie einen Schlüssel, um neues kryptografisches Material bereitzustellen, während die gleiche Kennung beibehalten wird
* Verwenden Sie den `Encrypt` Helper im Personalisierungseditor, um bestimmte Abfrageparameterwerte zu schützen

>[!TAB Glossar]

* **Schlüsselregistrierung**: Ein Repository auf Sandbox-Ebene in Journey Optimizer (Administration > Konfigurationen), in dem Administratoren die vom URL-Parameter-Verschlüsselungshelfer verwendeten Verschlüsselungsschlüssel erstellen und verwalten. *(produktspezifisch)*
* **Encryption Helper (`Encrypt`)**: Eine Hilfsfunktion im Personalisierungseditor, die einen Ausdruckswert zum Rendering verschlüsselt und in URL-Abfrageparametern PII durch Chiffretext ersetzt. *(produktspezifisch)*
* **Widerrufen (Schlüssel)**: Die dauerhafte Deaktivierung eines Schlüssels für eine neue Verschlüsselung. Der Schlüsseleintrag bleibt zur Überprüfung in der Registrierung sichtbar, und ältere Payloads erfordern ihn möglicherweise weiterhin für die Entschlüsselung auf den Systemen des Unternehmens.
* **Drehen (Schlüssel)** Der Vorgang der Bereitstellung von neuem kryptographischem Material für einen Schlüssel unter Beibehaltung der Kennungsstabilität, sodass Kampagnen und Journey, die bereits auf diesen Schlüssel verweisen, nicht aktualisiert werden müssen.
* **PII (Personally Identifiable Information)** Daten, die eine Person identifizieren können - z. B. Profilattribute, Token oder Angebotskennungen - und die bei der Aufnahme in URL-Abfrageparameter geschützt werden müssen.

>[!TAB Terminologie]

* **Kanonischer Name:** URL-Parameterverschlüsselung — Varianten: URL-Verschlüsselung, Abfrageparameter-Verschlüsselung, URL-Parameterverschleierung
* **Synonyme:** „Schlüsselregistrierung“ = „Schlüsselregistrierung“ (UI-Bezeichnung in Administration > Konfigurationen)
* **Nicht verwechseln:** Revoke (Deaktiviert dauerhaft den Schlüssel für neue Verschlüsselung; Eintritt bleibt für Prüfung) ≠ Rotate (ersetzt kryptographisches Material, lässt aber dieselbe Schlüsselkennung für neue Verschlüsselung aktiv)

>[!TAB Leitplanken und Einschränkungen]

* Die URL-Parameterverschlüsselung ist derzeit nur für den E-Mail-Kanal verfügbar.
* Erfordert **View Key Registry**- und **Manage Key Registry**-Berechtigungen für den Zugriff und die Verwaltung von Schlüsseln.
* Die Entschlüsselung liegt in der Verantwortung der Organisation. Journey Optimizer verschlüsselt Werte zum Zeitpunkt des Renderings. Die Website, die App oder die API muss Parameter mit demselben kryptografischen Material und denselben Prozessen entschlüsseln, die vom Unternehmen definiert wurden.
* Zum Verschlüsseln neuer Werte im Personalisierungseditor sollten nur aktive Schlüssel verwendet werden. Gesperrte Schlüssel dürfen nicht für neue Inhalte verwendet werden.
* Widerrufene Schlüssel bleiben zu Prüfzwecken in der Registrierung sichtbar. Sie werden möglicherweise weiterhin von den Systemen des Unternehmens benötigt, um ältere Payloads zu entschlüsseln.

>[!TAB FAQs]

**F: Wer ist für die Entschlüsselung verantwortlich?**

Die Entschlüsselung liegt in der Verantwortung der Organisation. Journey Optimizer verschlüsselt Werte, wenn die Nachricht gerendert wird. Die Website, die App oder die API muss Abfrageparameter mit demselben kryptografischen Material und denselben Prozessen entschlüsseln, die das Unternehmen definiert hat.

**F: Was ist der Unterschied zwischen Revoke und Rotate?**

„Widerrufen“ deaktiviert dauerhaft einen Schlüssel für die neue Verschlüsselung, während der Eintrag in der Registrierung zur Überprüfung sichtbar bleibt (ältere Payloads benötigen möglicherweise weiterhin den Schlüssel zur Entschlüsselung auf den Systemen des Unternehmens). Rotate liefert neues kryptografisches Material für einen Schlüssel, wobei dieselbe Schlüsselkennung beibehalten wird, sodass Kampagnen und Journey, die darauf verweisen, auch weiterhin ohne Updates funktionieren.

**F: Welche Berechtigungen sind erforderlich, um Schlüssel zu verwalten?**

Berechtigungen **View Key Registry** und **Manage Key Registry**.

**F: Welche Kanäle unterstützen die URL-Parameterverschlüsselung?**

Derzeit nur der E-Mail-Kanal.

**F: Kann ein widerrufener Schlüssel für eine neue Verschlüsselung verwendet werden?**

Nein. Nachdem ein Schlüssel widerrufen wurde, sollte der Versuch, ihn im Verschlüsselungs-Helper zu verwenden, zum Zeitpunkt des Renderings fehlschlagen. Verwenden Sie keine widerrufenen Schlüssel für neue Inhalte.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: c594ce24 -->
