---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von E-Mail-Einstellungen
description: Erfahren Sie, wie Sie E-Mail-Einstellungen auf Kanaloberflächen-Ebene konfigurieren.
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: Einstellungen, E-Mail, Konfiguration
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: aa71769719dce607e5392c9d8167f3afe3884d5f
workflow-type: tm+mt
source-wordcount: '2340'
ht-degree: 92%

---

# Konfigurieren von E-Mail-Einstellungen {#email-settings}

Zu Beginn der Erstellung einer E-Mail müssen Sie Oberflächen für E-Mail-Kanäle einrichten, die alle für Ihre Nachrichten erforderlichen technischen Parameter definieren. [Erfahren Sie, wie man Oberflächen erstellt](../configuration/channel-surfaces.md)

Legen Sie die E-Mail-Einstellungen im entsprechenden Abschnitt der Kanaloberflächenkonfiguration fest.

![](assets/preset-email-settings.png)

Die Konfiguration der E-Mail-Oberfläche wird nach der folgenden Logik für das Senden von Nachrichten übernommen:

* Bei Batch-Journeys gilt dies nicht für Batch-Ausführungen, die bereits begonnen hatten, bevor die Konfiguration der E-Mail-Oberfläche festgelegt wurde. Die Änderungen werden beim nächsten Intervall oder bei der nächsten Wiederausführung übernommen.

* Bei Transaktionsnachrichten wird die Änderung sofort für die nächste Mitteilung übernommen (mit einer Verzögerung von bis zu fünf Minuten).

>[!NOTE]
>
>Die aktualisierten E-Mail-Oberflächeneinstellungen werden automatisch in den Journeys oder Kampagnen aufgenommen, in denen die Oberfläche verwendet wird.

## E-Mail-Typ {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definieren der E-Mail-Kategorie"
>abstract="Wählen Sie den Typ der E-Mails aus, die bei Verwendung dieser Oberfläche gesendet werden sollen: „Marketing“ für Werbenachrichten, für die das Einverständnis der Benutzenden erforderlich ist, oder „Transaktion“ für nicht kommerzielle Nachrichten, die in bestimmten Situationen auch an abgemeldete Profile gesendet werden können."

Wählen Sie im Abschnitt **E-MAIL-TYP** die Art der Nachricht, die mit der Oberfläche gesendet werden soll: **[!UICONTROL Marketing]** oder **[!UICONTROL Transaktion]**.

* Wählen Sie **Marketing** für Werbe-E-Mails aus, z. B. für wöchentliche Werbeaktionen eines Einzelhandelsgeschäfts. Diese Nachrichten erfordern die Zustimmung der Benutzerin bzw. des Benutzers.

* Wählen Sie **Transaktion** für nicht-kommerzielle E-Mails aus, wie z. B. Bestellbestätigungen, Benachrichtigungen beim Zurücksetzen des Passworts oder Versandinformationen. Diese E-Mails können an Profile gesendet werden, die Marketing-Kommunikationen **storniert** haben. Diese Nachrichten können nur in bestimmten Kontexten gesendet werden.

Wenn Sie eine Nachricht erstellen, müssen Sie eine gültige Kanaloberfläche auswählen, die der für Ihre E-Mail ausgewählten Kategorie entspricht.

## Subdomain- und IP-Pools {#subdomains-and-ip-pools}

Im Abschnitt **Subdomain- und IP-Pools** müssen Sie folgendermaßen vorgehen:

1. Wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

1. Wählen Sie den IP-Pool aus, der mit der Oberfläche verknüpft werden soll. [Weitere Informationen](../configuration/ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

Sie können nicht mit der Erstellung der Oberfläche fortfahren, während sich der ausgewählte IP-Pool [in Bearbeitung](../configuration/ip-pools.md#edit-ip-pool) befindet (Status **[!UICONTROL Verarbeitung läuft]**) und noch nie mit der ausgewählten Subdomain verknüpft wurde. In diesem Fall wird weiterhin die älteste Version der IP-Pool-/Subdomain-Zuordnung verwendet. Um dies zu vermeiden, speichern Sie die Oberfläche als Entwurf und versuchen Sie es erneut, sobald der IP-Pool den Status **[!UICONTROL Erfolgreich abgeschlossen]** erreicht hat.

>[!NOTE]
>
>Für Nicht-Produktionsumgebungen erstellt Adobe keine nativen Test-Subdomains und gewährt auch keinen Zugriff auf einen freigegebenen Versand-IP-Pool. Sie müssen [Ihre eigenen Subdomains zuweisen](../configuration/delegate-subdomain.md) und die IPs des Ihrem Unternehmen zugewiesenen Pools verwenden.

Nachdem ein IP-Pool ausgewählt wurde, sind PTR-Informationen zu sehen, wenn Sie den Mauszeiger über die IP-Adressen bewegen, die unter der Dropdown-Liste „IP-Pool“ angezeigt werden. [Weitere Informationen zu PTR-Einträgen](../configuration/ptr-records.md)

![](assets/email-surface-ptr-record.png)

>[!NOTE]
>
>Wenn kein PTR-Eintrag konfiguriert ist, wenden Sie sich an den Adobe-Support.

## List-Unsubscribe {#list-unsubscribe}

Bei [der Auswahl einer Subdomain](#subdomains-and-ip-pools) aus der Liste wird die Option zur **[!UICONTROL Aktivierung der Abmeldung von der Liste]** angezeigt.

![](assets/preset-list-unsubscribe.png)

Standardmäßig ist diese Option aktiviert.

Wenn Sie diese Option aktiviert lassen, wird automatisch ein Abmelde-Link in die E-Mail-Kopfzeile eingefügt, z. B.:

![](assets/preset-list-unsubscribe-header.png)

Wenn Sie diese Option deaktivieren, wird in der E-Mail-Kopfzeile kein Abmelde-Link angezeigt.

Der Abmelde-Link besteht aus zwei Elementen:

* Einer **Abmelde-E-Mail-Adresse**, an die alle Abmeldeanfragen gesendet werden.

  Bei [!DNL Journey Optimizer] ist die Abmelde-E-Mail-Adresse die standardmäßig in der Kanaloberfläche angezeigte Adresse **[!UICONTROL Mailto (unsubscribe)]** und basiert auf der [ausgewählten Subdomain](#subdomains-and-ip-pools).

  ![](assets/preset-list-unsubscribe-mailto.png)

* Die **Abmelde-URL** ist die URL der Landingpage, auf die der Benutzer gelangt, wenn er sich abgemeldet hat.

  Wenn Sie einen [Ein-Klick-Opt-out-Link](../privacy/opt-out.md#one-click-opt-out) zu einer Nachricht hinzufügen, die mit dieser Oberfläche erstellt wurde, ist die Abmelde-URL die für den Ein-Klick-Opt-out-Link definierte URL.

  ![](assets/preset-list-unsubscribe-opt-out-url.png)

  >[!NOTE]
  >
  >Wenn Sie in Ihrem Nachrichteninhalt keinen Ein-Klick-Opt-out-Link hinzufügen, wird dem Benutzer keine Landingpage angezeigt.

Weitere Informationen zum Hinzufügen eines Kopfzeilen-Abmelde-Links zu Ihren Nachrichten finden Sie in [diesem Abschnitt](../privacy/opt-out.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Kopfzeilenparameter {#email-header}

Geben Sie im Abschnitt **[!UICONTROL Kopfzeilenparameter]** die Absendernamen und E-Mail-Adressen ein, die mit dem Typ der mit dieser Oberfläche gesendeten E-Mails verknüpft sind.

* **[!UICONTROL Absendername]**: Der Name des Absenders, wie z. B. der Name der Marke.

* **[!UICONTROL Absender-E-Mail]**: Die E-Mail-Adresse, die für die Kommunikation verwendet werden soll.

* **[!UICONTROL Antwort an (Name)]**: Der Name, der verwendet wird, wenn der Empfänger in seiner E-Mail-Client-Software auf den Button **Antworten** klickt.

* **[!UICONTROL Antwort an (E-Mail)]**: Die E-Mail-Adresse, die verwendet wird, wenn der Empfänger in seiner E-Mail-Client-Software auf den Button **Antworten** klickt. [Weitere Informationen](#reply-to-email)

* **[!UICONTROL E-Mail-Fehler]**: An dieser Adresse werden alle Fehlermeldungen empfangen, die von ISPs nach mehreren Tagen der E-Mail-Zustellung erzeugt wurden (asynchrone Bounces). Die Abwesenheitsbenachrichtigungen und die Anfechtungsantworten werden ebenfalls an diese Adresse gesendet.

  >[!NOTE]
  >
  >Wenn Sie die Abwesenheitsbenachrichtigungen erhalten und die Antworten auf eine bestimmte E-Mail-Adresse herausfordern möchten, die nicht an Adobe delegiert ist, müssen Sie eine [Weiterleitungsprozess](#forward-email). Vergewissern Sie sich in diesem Fall, dass Sie über eine manuelle oder automatisierte Lösung verfügen, mit der die in diesen Posteingang eingehenden E-Mails verarbeitet werden können.


>[!CAUTION]
>
>Die **[!UICONTROL Absender-E-Mail-Adresse]** und **[!UICONTROL Fehler-E-Mail]**-Adressen müssen die aktuell ausgewählte [delegierte Subdomain](../configuration/about-subdomain-delegation.md) verwenden. Wenn die delegierte Subdomain beispielsweise *marketing.luma.com* lautet, kann *contact@marketing.luma.com* und *error@marketing.luma.com* verwendet werden. 

![](assets/preset-header.png)

>[!NOTE]
>
>Adressen müssen mit einem Buchstaben (A-Z) beginnen und dürfen nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

### Antwort auf E-Mail {#reply-to-email}

Bei der Definition der **[!UICONTROL Antwort an (E-Mail)]**-Adresse kann eine beliebige E-Mail-Adresse angegeben werden, vorausgesetzt es handelt sich um eine gültige Adresse in einem korrekten Format und ohne Tippfehler.

Der Posteingang, der für Antworten verwendet wird, erhält alle Antwort-E-Mails mit Ausnahme von Abwesenheitsbenachrichtigungen und Anfechtungsantworten, die auf der **[!UICONTROL Fehler-Email]** Adresse.

Bitte die nachstehenden Empfehlungen befolgen, um eine ordnungsgemäße Antwortverwaltung sicherzustellen:

* Bitte sicherstellen, dass der dedizierte Posteingang über genügend Aufnahmekapazität verfügt, um alle Antwort-E-Mails zu empfangen, die über die E-Mail-Oberfläche gesendet werden. Wenn der Posteingang Bounce-Nachrichten zurückgibt, werden manche Antworten von den Kunden möglicherweise nicht empfangen.

* Die Antworten müssen unter Berücksichtigung der Datenschutz- und Compliance-Verpflichtungen verarbeitet werden, da sie personenbezogene Daten (PII) enthalten können.

* Bitte im Posteingang für Antworten keine Nachrichten als Spam markieren, da sich das auf alle anderen an diese Adresse gesendeten Antworten auswirken würde.

Darüber hinaus ist bei der Definition der **[!UICONTROL Antwortadresse (E-Mail)]** sicherzustellen, dass eine Subdomain mit einer gültigen MX-Eintragskonfiguration verwendet wird. Andernfalls schlägt die Verarbeitung der E-Mail-Oberfläche fehl.

Wenn beim Senden der E-Mail-Oberfläche ein Fehler auftritt, bedeutet dies, dass der MX-Datensatz nicht für die Subdomain der eingegebenen Adresse konfiguriert ist. Sie können die Administrierenden kontaktieren, um den entsprechenden MX-Eintrag zu konfigurieren, oder eine andere Adresse mit einer gültigen MX-Eintragskonfiguration verwenden.

>[!NOTE]
>
>Wenn die Subdomain der eingegebenen Adresse eine Domain ist, die Adobe [komplett delegiert](../configuration/delegate-subdomain.md#full-subdomain-delegation) wurde, kontaktieren Sie die Adobe-Kundenbetreuung.

### Weiterleiten von E-Mails {#forward-email}

Alle E-Mails, die von [!DNL Journey Optimizer] Wenden Sie sich für die zugewiesene Subdomain an die Adobe-Kundenunterstützung.

>[!NOTE]
>
>Wenn die für die **[!UICONTROL Antwort an (E-Mail)]** -Adresse nicht an Adobe delegiert wird, kann die Weiterleitung für diese Adresse nicht funktionieren.

Sie müssen Folgendes bereitstellen:

* Die E-Mail-Weiterleitungsadresse Ihrer Wahl. Beachten Sie, dass die E-Mail-Adress-Domain für Weiterleitungen nicht mit einer an Adobe delegierten Subdomain übereinstimmen darf.
* Ihren Sandbox-Namen.
* Der Oberflächenname oder die Subdomain, für die die Weiterleitungs-E-Mail-Adresse verwendet wird.
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel surface level.-->

>[!NOTE]
>
>Pro Subdomain kann nur eine Weiterleitungs-E-Mail-Adresse verwendet werden. Wenn mehrere Oberflächen dieselbe Subdomain verwenden, muss daher für alle dieselbe Weiterleitungs-E-Mail-Adresse verwendet werden.

Die Weiterleitungs-E-Mail-Adresse wird von Adobe eingerichtet. Dies kann 3 bis 4 Tage dauern.

Nach Abschluss des Vorgangs werden alle Nachrichten auf der **[!UICONTROL Antwort an (E-Mail)]** und **[!UICONTROL Fehler-Email]** Die Adressen werden an die von Ihnen angegebene E-Mail-Adresse weitergeleitet.

## BCC-E-Mail-Adresse {#bcc-email}

Sie können eine identische Kopie (oder Blindkopie) von E-Mails senden, die von [!DNL Journey Optimizer] an einen BCC-Posteingang gesendet wurden, in dem sie für Compliance- oder Archivierungszwecke gespeichert werden.

Aktivieren Sie dazu auf der Ebene der Kanaloberfläche die optionale Funktion **[!UICONTROL BCC-E-Mail]**. [Weitere Informationen](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

Darüber hinaus ist bei der Definition der **[!UICONTROL BCC-E-Mail]**-Adresse sicherzustellen, dass eine Subdomain mit einer gültigen MX-Eintragskonfiguration verwendet wird. Andernfalls schlägt die Verarbeitung der E-Mail-Oberfläche fehl.

Wenn beim Senden der E-Mail-Oberfläche ein Fehler auftritt, bedeutet dies, dass der MX-Datensatz nicht für die Subdomain der eingegebenen Adresse konfiguriert ist. Sie können die Administrierenden kontaktieren, um den entsprechenden MX-Eintrag zu konfigurieren, oder eine andere Adresse mit einer gültigen MX-Eintragskonfiguration verwenden.

## Senden an unterdrückte E-Mail-Adressen {#send-to-suppressed-email-addresses}

>[!CONTEXTUALHELP]
>id="ajo_surface_suppressed_addresses"
>title="Überschreiben der Unterdrückungslistenpriorität"
>abstract="Sie können Transaktionsnachrichten auch dann an Profile senden, wenn deren E-Mail-Adressen aufgrund von Spam-Beschwerden auf der Adobe Journey Optimizer-Unterdrückungsliste stehen. Standardmäßig ist diese Option deaktiviert."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html?lang=de" text="Verwalten der Unterdrückungsliste"

>[!IMPORTANT]
>
>Diese Option ist nur verfügbar, wenn Sie den E-Mail-Typ **[!UICONTROL Transaktion]** ausgewählt haben. [Weitere Informationen](#email-type)

In [!DNL Journey Optimizer] werden alle E-Mail-Adressen, die als Hardbounces, Softbounces und Spam-Beschwerden gekennzeichnet sind, automatisch in der [Unterdrückungsliste](../configuration/manage-suppression-list.md) gesammelt und vom Versand in einer Journey oder Kampagne ausgeschlossen.

Sie können jedoch entscheiden, Nachrichten des Typs **Transaktion** an Profile zu senden, auch wenn ihre E-Mail-Adressen aufgrund von Spam-Beschwerden einer Benutzerin oder eines Benutzers auf der Unterdrückungsliste stehen.

Tatsächlich erhalten Transaktionsnachrichten im Allgemeinen nützliche und erwartete Informationen wie eine Bestellbestätigung oder eine Benachrichtigung zur Passwortzurücksetzung. Selbst wenn eine Ihrer Marketing-Nachrichten als Spam gemeldet wurde, möchten Sie in den meisten Fällen, dass Ihre Kunden diese Art nicht kommerzieller E-Mails erhalten.

Um E-Mail-Adressen, die aufgrund von Spam-Beschwerden unterdrückt wurden, in Ihre Zielgruppe für Transaktionsnachrichten aufzunehmen, wählen Sie die entsprechende Option aus dem Abschnitt **[!UICONTROL An unterdrückte E-Mail-Adressen senden]** aus.

![](assets/preset-suppressed-email-addresses.png)

>[!NOTE]
>
>Standardmäßig ist diese Option deaktiviert.

Als Best Practice für die Zustellbarkeit ist diese Option standardmäßig deaktiviert, um sicherzustellen, dass Ihre Kundinnen und Kunden, die sich abgemeldet haben, nicht kontaktiert werden. Sie können diese Standardoption jedoch ändern, sodass Sie dann Transaktionsnachrichten an Ihre Kundinnen und Kunden senden können.

Wenn diese Option aktiviert ist, kann eine Kundin bzw. ein Kunde zwar Ihre Marketing-E-Mail als Spam gekennzeichnet haben, wird jedoch Ihre Transaktionsnachrichten unter Verwendung der aktuellen Oberfläche empfangen können. Achten Sie immer darauf, Opt-out-Voreinstellungen gemäß den Best Practices für die Zustellbarkeit zu verwalten.

## Testadressenliste {#seed-list}

>[!CONTEXTUALHELP]
>id="ajo_surface_seed_list"
>title="Testadressenliste hinzufügen"
>abstract="Wählen Sie die Testadressenliste Ihrer Wahl aus, um automatisch bestimmte interne Adressen zu Ihren Zielgruppen hinzuzufügen. Diese Testadressen werden zum Ausführungszeitpunkt des Versands hinzugefügt und erhalten für Sicherheitszwecke eine exakte Kopie der Nachricht."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html?lang=de#use-seed-list" text="Was sind Testadressenlisten?"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html?lang=de#create-seed-list" text="Erstellen einer Testadressenliste"


Eine Testadressenliste in [!DNL Journey Optimizer] ermöglicht es Ihnen, automatisch bestimmte E-Mail-Testadressen in Ihre Sendungen einzuschließen. [Weitere Informationen](../configuration/seed-lists.md)

>[!CAUTION]
>
>Diese Funktion ist derzeit nur für den E-Mail-Kanal verfügbar.

Wählen Sie die Liste, die für Sie relevant ist, im Abschnitt **[!UICONTROL Testadressenliste]** aus. In [diesem Abschnitt](../configuration/seed-lists.md#create-seed-list) erfahren Sie, wie Sie eine Testadressenliste erstellen.

![](../configuration/assets/seed-list-surface.png)

>[!NOTE]
>
>Es kann jeweils nur eine Testadressenliste ausgewählt werden.

Wenn die aktuelle Oberfläche in einer Kampagne oder einer Journey verwendet wird, werden zum Zeitpunkt der Versandausführung die E-Mail-Adressen in der ausgewählten Testadressenliste einbezogen, d. h. sie erhalten zu Sicherheitszwecken eine Kopie des Versands.

In [diesem Abschnitt](../configuration/seed-lists.md#use-seed-list) erfahren Sie, wie Sie eine Testadressenliste in einer Kampagne oder einer Journey verwenden.

## E-Mail-Wiederholungsparameter {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Anpassen des Wiederholungszeitraumes"
>abstract="Wiederholungen werden 3,5 Tage lang (84 Stunden) durchgeführt, wenn ein E-Mail-Versand aufgrund eines temporären Softbounce-Fehlers fehlschlägt. Sie können diesen standardmäßigen Wiederholungszeitraum an Ihre Anforderungen anpassen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html?lang=de" text="Über weitere Zustellversuche"

Sie können die **E-Mail-Wiederholungsparameter** konfigurieren.

![](assets/preset-retry-parameters.png)

Standardmäßig ist der [Zeitraum für weitere Zustellversuche](../configuration/retries.md#retry-duration) auf 84 Stunden festgelegt. Sie können diese Einstellung jedoch an Ihre Anforderungen anpassen.

Sie müssen einen ganzzahligen Wert (in Stunden oder Minuten) innerhalb des folgenden Bereichs eingeben:

* Für E-Mails vom Typ Marketing beträgt der Mindestzeitraum für weitere Zustellversuche 6 Stunden.
* Für E-Mails vom Typ Transaktion beträgt der Mindestzeitraum für weitere Zustellversuche 10 Minuten.
* Für beide E-Mail-Typen beträgt der maximale Zeitraum für weitere Zustellversuche 84 Stunden (d. h. 5.040 Minuten).

Weitere Informationen zu weiteren Zustellversuchen finden Sie in [diesem Abschnitt](../configuration/retries.md).

## URL-Tracking {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Definieren der URL-Tracking-Parameter"
>abstract="Verwenden Sie diesen Abschnitt, um Tracking-Parameter automatisch an die im E-Mail-Inhalt vorhandenen URLs anzuhängen. Diese Funktion ist optional."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Vorschau der URL-Tracking-Parameter"
>abstract="Überprüfen Sie, wie Tracking-Parameter an die in Ihrem E-Mail-Inhalt vorhandenen URLs angehängt werden."

Sie können **[!UICONTROL URL-Tracking-Parameter]** verwenden, um die Effektivität Ihrer Marketing-Maßnahmen kanalübergreifend zu messen. Diese Funktion ist optional.

Die in diesem Abschnitt definierten Parameter werden an das Ende der URLs angehängt, die im Inhalt Ihrer E-Mail-Nachricht enthalten sind. Anschließend können Sie diese Parameter in Web-Analyse-Tools wie Adobe Analytics oder Google Analytics erfassen und verschiedene Leistungsberichte erstellen.

Sie können mithilfe der Schaltfläche **[!UICONTROL Neuen Parameter hinzufügen]** bis zu 10 Tracking-Parameter hinzufügen.

![](assets/preset-url-tracking.png)

Um einen URL-Tracking-Parameter zu konfigurieren, können Sie die gewünschten Werte direkt in die Felder **[!UICONTROL Name]** und **[!UICONTROL Wert]** eingeben.

Mithilfe des [Ausdruckseditors](../personalization/personalization-build-expressions.md) können Sie auch jedes **[!UICONTROL Werte]**-Feld bearbeiten. Klicken Sie auf das Bearbeitungssymbol, um den Editor zu öffnen. Dort können Sie die gewünschten Kontexteigenschaften und/oder den Text direkt bearbeiten.

![](assets/preset-url-tracking-editor.png)

Die folgenden vordefinierten Werte sind über den Ausdruckseditor verfügbar:

* **Quellaktion-ID**: ID der E-Mail-Aktion, die der Journey oder Kampagne hinzugefügt wurde.

* **Name der Quellaktion**: Name der E-Mail-Aktion, die der Journey oder Kampagne hinzugefügt wurde.

* **Quell-ID**: ID der Journey oder Kampagne, mit der die E-Mail gesendet wurde.

* **Quellname**: Name der Journey oder Kampagne, mit der die E-Mail gesendet wurde.

* **Quellversions-ID**: ID der Journey- oder Kampagnenversion, mit der die E-Mail gesendet wurde.

* **Angebots-ID**: ID des in der E-Mail verwendeten Angebots.

>[!NOTE]
>
>Sie können die Eingabe von Textwerten und die Verwendung von kontextuellen Attributen im Ausdruckseditor kombinieren. Jedes **[!UICONTROL Wert]**-Feld kann eine Anzahl von Zeichen bis zu einer Größe von 5 KB enthalten.

<!--You can drag and drop the parameters to reorder them.-->

Im Folgenden finden Sie Beispiele für URLs, die mit Adobe Analytics und Google Analytics kompatibel sind.

* Mit Adobe Analytics kompatible URL: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Mit Google Analytics kompatible URL: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

Sie können die resultierende Tracking-URL dynamisch in der Vorschau anzeigen. Jedes Mal, wenn Sie einen Parameter hinzufügen, bearbeiten oder entfernen, wird die Vorschau automatisch aktualisiert.

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>Sie können auch dynamische, personalisierte Tracking-Parameter zu den Links im E-Mail-Inhalt hinzufügen. Auf Oberflächenebene ist dies jedoch nicht möglich. Diesen Schritt müssen Sie bei der Erstellung Ihrer Nachricht mit dem E-Mail-Designer durchführen. [Weitere Informationen](message-tracking.md#url-tracking)
