---
title: Erstellen eines benutzerdefinierten Kanals
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer mithilfe des Channel Builders einen benutzerdefinierten Kanal erstellen und konfigurieren.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '1555'
ht-degree: 1%

---


# Einrichten eines benutzerdefinierten Kanals {#create-custom-channel}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_settings"
>title="Über benutzerdefinierte Kanäle"
>abstract="Mit einem benutzerdefinierten Kanal kann Adobe Journey Optimizer über Ihren eigenen API-Endpunkt personalisierte Nachrichten an ein externes System senden. Definieren Sie die allgemeinen Eigenschaften, den Endpunkt, die Authentifizierung und die Payload und testen und aktivieren Sie dann Ihren neuen benutzerdefinierten Kanal. Anschließend können Sie sie beim Erstellen einer Kanalkonfiguration verwenden, damit Marketing-Experten sie in Journey und Kampagnen verwenden können."
>additional-url="" text="Erste Schritte mit benutzerdefinierten Kanälen"

<!--Contextual help final location TBC (here or in Settings subsection-->

Um einen benutzerdefinierten Kanal in -Kampagnen und -Journey verwenden zu können, muss zunächst ein Administrator den Kanal erstellen. Dazu gehört die Definition des Endpunkts, der Authentifizierung, der Drosselungsrichtlinie und der Payload-Struktur der Nachricht.

Der **Channel Builder**-Abschnitt ist die zentrale Schnittstelle zum Definieren neuer benutzerdefinierter Kanäle. <!--It is accessible to users with the **[!UICONTROL Administrator]** role. -->Damit können Sie benutzerdefinierte Kanäle erstellen und konfigurieren, aber auch API-Anmeldeinformationen verwalten und Subdomains delegieren.

>[!IMPORTANT]
>
>Um auf den Channel Builder zugreifen, benutzerdefinierte Kanäle erstellen und verwalten zu können, benötigen Sie die Berechtigungen **Benutzerdefinierte Kanäle anzeigen** und **Benutzerdefinierte Kanäle verwalten** . <!--[Learn more](../administration/high-low-permissions.md)--> Erfahren Sie in ([&#x200B; Abschnitt), wie Sie Berechtigungen &#x200B;](../administration/permissions.md).

## Zugreifen auf und Verwalten von benutzerdefinierten Kanälen {#access-channel-builder}

Gehen Sie wie folgt vor, um auf **Channel Builder** zuzugreifen und Ihre benutzerdefinierten Kanäle zu verwalten.

1. Navigieren Sie **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** in der linken Navigationsleiste.

1. Wählen **[!UICONTROL Benutzerdefinierte Kanäle]** im Abschnitt **[!UICONTROL Channel Builder]** aus.

   ![Benutzerdefinierter Kanalbestand](assets/custom_channels_inventory.png){width="70%"}

1. Das Inventar listet alle benutzerdefinierten Kanäle in Ihrer Sandbox auf, einschließlich ihres aktuellen Status und des Authentifizierungstyps, der zum Herstellen einer Verbindung mit dem externen Endpunkt verwendet wird.

1. Sie können die benutzerdefinierten Kanäle nach Status (**Entwurf**, **Aktiv** oder **Archiviert**) filtern, von wem sie erstellt wurden, und nach Namen suchen.

1. Um einen Kanal zu bearbeiten, klicken Sie im Inventar auf seinen Namen, nehmen Sie die Änderungen vor und speichern Sie. Für aktive Kanäle können nur bestimmte Felder bearbeitet werden ([&#x200B; Informationen](#test-activate).

   >[!CAUTION]
   >
   >Die Änderung der Drosselungs- oder Wiederholungseinstellungen für einen aktiven Kanal wird sofort für alle laufenden und zukünftigen Ausführungen wirksam.

1. Um einen Kanal zu archivieren, öffnen Sie ihn im Inventar und klicken Sie auf **[!UICONTROL Archivieren]**.

   Wenn Sie einen aktiven Kanal archivieren, wird er aus allen Auswahl-Dropdown-Menüs entfernt - Kampagnenaktionsselektor, Journey-Aktionspalette, orchestrierte Kampagnenkanalliste, Kanalkonfigurationen und Inhaltsvorlagen. Bestehende Journey und Kampagnen, die den -Kanal bereits verwenden, funktionieren weiterhin normal.

## Erstellen eines benutzerdefinierten Kanals {#create-channel}

Gehen Sie wie folgt vor, um einen neuen benutzerdefinierten Kanal zu erstellen.

1. Klicken Sie auf **[!UICONTROL Benutzerdefinierten Kanal erstellen]**, um das Formular zur Kanalerstellung zu öffnen. Definieren Sie zunächst die allgemeinen Einstellungen für Ihren benutzerdefinierten Kanal.

   ![Allgemeine Einstellungen](assets/custom_channel_properties.png){width="70%"}

1. Geben Sie **[!UICONTROL Abschnitt]** einen **[!UICONTROL Namen]** für Ihren benutzerdefinierten Kanal ein. Dieser Name wird auf der Journey-Arbeitsfläche, in der Auswahl der Kampagnenaktion und in der Liste der Kanäle für orchestrierte Kampagnen angezeigt.

   >[!NOTE]
   >
   >Der Name muss eindeutig sein, mit einem Buchstaben (A-Z) beginnen, nur alphanumerische Zeichen oder Sonderzeichen ( _, ., -) enthalten und sollte mehr als 1 Zeichen lang sein.

1. Sie können ein Symbol aus der standardmäßigen Symbolbibliothek auswählen oder eine SVG-Datei auf Ihrem Computer auswählen.

   >[!NOTE]
   >
   >Die Datei darf nicht größer als 150 KB sein.

   Dieses Symbol wird neben dem Kanalnamen auf der Journey-Arbeitsfläche angezeigt. Wenn kein Symbol hochgeladen wird, wird das Standardsymbol verwendet.

1. Geben Sie eine optionale **[!UICONTROL Beschreibung]** ein.

<!--
1. Optionally, assign **[!UICONTROL Access labels]** to restrict access to this channel based on data usage policies. Learn more
-->

## Festlegen der Endpunktkonfiguration {#endpoint-configuration}

Sie müssen den Endpunkt konfigurieren. Dies ist die HTTP-URL Ihres externen Messaging-Systems. [!DNL Journey Optimizer] sendet eine POST-Anfrage mit der personalisierten Payload an diesen Endpunkt, wenn sich ein Profil in einer Kampagne oder auf einer Journey qualifiziert.

![Endpunktkonfiguration](assets/custom_channel_endpoint_configuration.png){width="70%"}

1. Geben **[!UICONTROL im Abschnitt „Endpunktkonfiguration]** den Host **[!UICONTROL URL]** Ihres externen Messaging-Systems ein.

   <!--The HTTP method to is currently set to **POST**.-->

   >[!IMPORTANT]
   >Ihr externes Messaging-System muss einen HTTPS-Endpunkt bereitstellen, den [!DNL Journey Optimizer] über HTTP POST aufrufen können. Der Endpunkt muss:
   >
   >* Akzeptieren Sie das von Ihrem Kanal definierte Payload-Format (JSON).
   >* Unterstützt eine der Authentifizierungsmethoden, die im Channel Builder verfügbar sind. [Weitere Informationen](#authentication-settings)
   >* Gibt eine HTTP 2xx-Antwort zurück, um den erfolgreichen Empfang der Anfrage zu bestätigen.

1. Fügen Sie **[!UICONTROL Kopfzeilen]** nach Bedarf hinzu. Header sind Schlüssel-Wert-Paare, die auf HTTP-Anfrageebene übertragen werden. Sie werden zusammen mit jeder Anfrage an Ihren Endpunkt gesendet und normalerweise für Authentifizierungs-Token, Inhaltstypspezifikationen oder andere Metadaten verwendet, die von Ihrem externen System benötigt werden.

   <!--At minimum, `Content-Type` and `Charset` are available as default headers.-->

   ![Headers-Konfiguration](assets/custom_channel_endpoint_headers.png)

   Für jede Kopfzeile können Sie festlegen, ob ihr Wert wie folgt lautet:

   * **[!UICONTROL Konstante]** - Ein statischer Wert, der einmal festgelegt und in jeder Anfrage enthalten ist. Sie können beispielsweise den `Content-Type` mit dem Wert `application/json` oder den `Charset` mit dem Wert `UTF-8` definieren.
   * **[!UICONTROL Variable]** - Wenn hier ein Standardwert eingegeben wird, wird er verwendet, es sei denn, er wird in der Kanalkonfiguration überschrieben. Sie können beispielsweise eine Variable für die Benutzer-ID definieren, die zur Laufzeit aufgelöst wird. [Weitere Informationen](custom-channel-configuration.md) <!--From Custom actions section: For these parameters, you can define where to get this information (example: events, data sources), pass values manually or use the advanced expression editor for advanced use cases. Advanced uses cases can be data manipulation and other function usage. Refer to this [page](expression/expressionadvanced.md).-->

1. Fügen Sie optional **[!UICONTROL Abfrageparameter“]** demselben Konstanten-/Variablenmuster hinzu. Abfrageparameter werden zur Versandzeit an die Endpunkt-URL angehängt. Konstante Parameter werden immer mit demselben Wert hinzugefügt. Variablenparameter werden zum Sendezeitpunkt aufgelöst, z. B. um eine Benutzerkennung aus dem Profil zu übergeben.

   ![Abfrageparameter](assets/custom_channel_endpoint_query_param.png){width="70%"}

1. Definieren Sie **[!UICONTROL Abschnitt]** Richtlinienkonfiguration“, wie [!DNL Journey Optimizer] mit Anfragedurchsatz und -fehlern umgeht. Dies ist wichtig, um sicherzustellen, dass Ihr externes System das Anfragevolumen verarbeiten kann, und um eine Überlastung zu vermeiden.

   ![Richtlinienkonfiguration](assets/custom_channel_endpoint_policy_config.png)

   * **[!UICONTROL Drosselung aktivieren]** - Standardmäßig deaktiviert. Legen Sie die maximale Anzahl von Anfragen pro Sekunde fest (Standard: **5.000c**). Sobald das Limit erreicht ist, werden Anfragen in die Warteschlange gestellt und so bald wie möglich gesendet.
   * **[!UICONTROL Wiederholen aktivieren]** - Standardmäßig aktiviert. Legen Sie die maximale Wiederholungsanzahl (Standard: **3)** konfigurierbaren Bereich: 0-10) für fehlgeschlagene Anfragen fest. Dadurch wird verhindert, dass der Endpunkt während vorübergehender Fehler überlastet wird.
   * **[!UICONTROL Zeitüberschreitung]** - Standard: **5.000 Millisekunden**. Legen Sie die maximale Zeit fest, die auf eine Antwort des Endpunkts gewartet werden soll, bevor die Anfrage als fehlgeschlagen eingestuft wird.
     <!--* **[!UICONTROL Enable cache]** – Disabled by default. Set the caching duration (default TTL: **600 seconds**). After the TTL (Time To Live) expires, the next request is sent to the endpoint. Caching is useful for endpoints that return the same response for identical requests, reducing load and improving performance.-->

## Authentifizierungseinstellungen {#authentication-settings}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_authentication"
>title="Authentifizierungstyp definieren"
>abstract="Die Authentifizierung stellt sicher, dass nur autorisierte Anfragen an Ihr externes Messaging-System gesendet werden. Sie können aus verschiedenen Authentifizierungsmethoden auswählen, einschließlich API-Schlüssel, Standardauthentifizierung und OAuth 2.0. Nach der Aktivierung generiert Adobe Journey Optimizer automatisch einen ersten Satz von API-Anmeldeinformationen für den Kanal, der im Inventar der API-Anmeldeinformationen verwaltet werden kann. Selbst wenn Sie die Anmeldeinformationen später ändern können, müssen Sie hier die Authentifizierungsdetails angeben, um die Verbindung zu Ihrem Endpunkt zu testen, bevor Sie den Kanal aktivieren."
>additional-url="" text="Weitere Informationen zu API-Anmeldeinformationen"

Wählen Sie **[!UICONTROL „Authentifizierungstyp]** aus, den Sie für diesen Kanal verwenden müssen. Die verfügbaren Optionen hängen von den Authentifizierungsmethoden ab, die von Ihrem externen Messaging-System unterstützt werden.

![Authentifizierungstyp](assets/custom_channel_authentication_type.png){width="70%"}

Geben Sie die Authentifizierungsdetails an, wie von Ihrem Endpunkt benötigt.

* **[!UICONTROL Keine]** - Die Anfrage wird ohne Anmeldeinformationen gesendet.
* **[!UICONTROL API-Schlüssel]** - Geben Sie den Schlüsselnamen, den Wert und den Speicherort (Abfrageparameter oder Kopfzeile) an.
* **[!UICONTROL Einfache Authentifizierung]** - Geben Sie einen Benutzernamen und ein Kennwort ein.
* **[!UICONTROL OAuth 2.0]** - Konfigurieren der Payload für die OAuth 2.0-Authentifizierung.
  <!--* **[!UICONTROL Custom]** – Define the authentication configuration using a JSON payload.-->

Wenn es sich bei dem Authentifizierungstyp um einen anderen **als &quot;**&quot; handelt, generiert [!DNL Journey Optimizer] automatisch einen ersten Satz von API-Anmeldeinformationen für diesen Kanal, wenn er aktiviert wird. Sie können diese Anmeldeinformationen ändern und neue im Inventar der API-Anmeldeinformationen erstellen. [Weitere Informationen](custom-channel-api-credentials.md) <!--TBC-->

Die Authentifizierungsdetails sind jedoch hier erforderlich, um die Verbindung zu Ihrem Endpunkt zu testen, bevor Sie den Kanal aktivieren. Zur **[!UICONTROL der Authentifizierungseinstellungen]** die Schaltfläche „Verbindung testen“ verfügbar. [Weitere Informationen](#test-activate)

## Payload-Konfiguration {#payload-configuration}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_payload_config"
>title="Feld für Kanalkonfiguration aktivieren"
>abstract="Wenn diese Option aktiviert ist, werden die Felder in dieser Spalte in der Kanalkonfiguration angezeigt, sodass Admins für jede Konfiguration unterschiedliche Werte festlegen können (z. B. eine andere Absender-ID pro Marke oder Region). Dies eignet sich für Felder, die je nach Kampagnenkontext oder Journey variieren können, z. B. Absenderinformationen oder Nachrichtenvorlagen."
>additional-url="" text="Konfigurieren dynamischer Parameter in der Konfiguration benutzerdefinierter Kanäle"

<!--Create a page on Custom channel config to explain how to use the payload in a channel configuration.-->

Die Payload wird an den Endpunkt gesendet, wenn sich ein Profil in einer Kampagne oder auf einer Journey qualifiziert.

Definieren Sie in der Payload-Konfiguration die Struktur der Nachrichten-Payload und die Felder, die Marketing-Experten erstellen und personalisieren können.

1. Klicken Sie **[!UICONTROL Payload definieren]** und wählen Sie aus, wie die Payload definiert werden soll:

   * **[!UICONTROL Beispiel-JSON-Payload einfügen]** - Fügen Sie ein repräsentatives JSON-Objekt ein und leitet [!DNL Journey Optimizer] automatisch ein Schema daraus ab.
   * **[!UICONTROL JSON-Schema importieren]** (in Kürze verfügbar) - Laden Sie eine vollständige JSON-Schemadatei hoch.

     >[!AVAILABILITY]
     >
     >Diese Funktion ist noch nicht verfügbar. Sie wird in einer zukünftigen Version hinzugefügt.

1. Nachdem das Schema generiert wurde, zeigt [!DNL Journey Optimizer] alle erkannten Felder in einer Formularansicht an.

   ![](assets/custom_channel_payload_configuration.png)

1. Konfigurieren Sie für jedes Feld die folgenden Einstellungen:

   | Einstellung | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Standardwert]** | Optional. Wird verwendet, wenn beim Authoring kein personalisierter Wert angegeben wird. |
   | **[!UICONTROL Typ]** | Schreibgeschützt, von der Payload abgeleitet. Unterstützte Typen: `string`, `integer`, `decimal`, `boolean`, `dateTime`, `dateTimeOnly`, `dateOnly`, `listObject`, `listString`, `listInteger`, `listDecimal`, `listBoolean`, `listDateTime`, `listDateTimeOnly`, `listDateOnly`. |
   | **[!UICONTROL Erforderlich]** | Wenn diese Option aktiviert ist, muss das Feld einen Wert enthalten, wenn der Kanal in einer Kampagne oder auf einer Journey verwendet wird. Fehlende Pflichtfelder : Trigger eines Validierungsfehlers, der die Aktivierung verhindert. |
   | **[!UICONTROL Kanalkonfiguration]** | Wenn diese Option aktiviert ist, wird das Feld in der Kanalkonfiguration angezeigt, sodass Admins für jede Konfiguration unterschiedliche Werte festlegen können (z. B. eine andere Absender-ID pro Marke oder Region). [Weitere Informationen](custom-channel-configuration.md) |

   Verschachtelte Felder werden mit Punktnotation dargestellt (z. B. `image.id`)<!--TBC-->

## Testen und Aktivieren {#test-activate}

Während sich der Kanal im Status **[!UICONTROL Entwurf]** befindet, verwenden Sie die Schaltfläche **[!UICONTROL Verbindung testen]** am oberen Bildschirmrand, um eine Testanfrage an Ihren Endpunkt zu senden und die End-to-End-Verbindung zu validieren.

![Schaltfläche „Verbindung testen“](assets/custom_channel_test_connection.png){width="70%"}

Überprüfen Sie die Protokolle Ihres externen Systems, um sicherzustellen, dass die Anfrage mit der erwarteten Authentifizierung und Payload empfangen wurde.

Nach erfolgreichem Test können Sie den Kanal speichern oder aktivieren.

* Klicken Sie **[!UICONTROL Als Entwurf speichern]**, um Ihren Fortschritt zu speichern, ohne den Kanal verfügbar zu machen.
* Klicken Sie **[!UICONTROL Aktivieren]**, um den Kanal für die Verwendung in Kanalkonfigurationen, Kampagnen und Journey verfügbar zu machen.

>[!IMPORTANT]
>
>Nachdem ein Kanal aktiviert wurde, können nur die folgenden Felder bearbeitet werden: Name, Beschreibung, Symbol, Einschränkungen und Konfiguration wiederholen. Endpunkt-URL, Kopfzeilen, Abfrageparameter, Authentifizierung und Payload-Struktur sind gesperrt.<!--TBC-->

<!--TBC: An activated channel can be **archived** (hidden from all selection drop-downs while existing journeys and campaigns continue to function), but it cannot be **deleted**. Deletion is only possible while the channel is in **[!UICONTROL Draft]** status.TBC-->

## Nächste Schritte {#next-steps}

Ihr benutzerdefinierter Kanal wird jetzt erstellt. Schließen Sie die Konfiguration ab, indem Sie die verbleibenden Schritte ausführen:

* [Einrichten von API-Anmeldeinformationen](custom-channel-api-credentials.md) (wenn der Kanal die Authentifizierung verwendet)
* [Subdomain delegieren](custom-channel-subdomains.md) (optional - für Linktracking erforderlich)
* [Erstellen einer Kanalkonfiguration](custom-channel-configuration.md)
