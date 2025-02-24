---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von E-Mail-Einstellungen
description: Erfahren Sie, wie Sie E-Mail-Einstellungen auf Kanalkonfigurations-Ebene konfigurieren
feature: Email, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Einstellungen, E-Mail, Konfiguration
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: abb837b6af232e23bbbc6a1f1b2607dbc2ee2679
workflow-type: ht
source-wordcount: '1471'
ht-degree: 100%

---

# Konfigurieren von E-Mail-Einstellungen {#email-settings}

Zu Beginn der Erstellung einer E-Mail müssen Sie Konfigurationen für E-Mail-Kanäle einrichten, die alle für Ihre Nachrichten erforderlichen technischen Parameter definieren. [Erfahren Sie, wie Sie Konfigurationen erstellen](../configuration/channel-surfaces.md)

>[!NOTE]
>
>Richten Sie vor der Erstellung einer E-Mail-Konfiguration die Subdomains ein, die Sie zum Senden von E-Mails verwenden, um Ihre Reputation zu wahren und Ihre Zustellbarkeit zu verbessern. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

Legen Sie die E-Mail-Einstellungen im entsprechenden Abschnitt der Kanalkonfiguration fest, wie unten beschrieben.

![](assets/surface-email-settings.png){width="50%" align="left"}

Die E-Mail-Konfiguration wird nach der folgenden Logik für das Senden von Nachrichten übernommen:

* Bei Batch-Journeys gilt dies nicht für Batch-Ausführungen, die bereits begonnen hatten, bevor die Konfiguration der E-Mail-Oberfläche festgelegt wurde. Die Änderungen werden beim nächsten Wiederkehren oder bei der nächsten Neuausführung übernommen.

* Bei Transaktionsnachrichten wird die Änderung sofort für die nächste Mitteilung übernommen (mit einer Verzögerung von bis zu fünf Minuten).

>[!NOTE]
>
>Die aktualisierten E-Mail-Konfigurationseinstellungen werden automatisch in den Journeys oder Kampagnen aufgenommen, in denen die Konfiguration verwendet wird.

## E-Mail-Typ {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definieren des E-Mail-Typs"
>abstract="Typ der E-Mails auswählen, die bei Verwendung dieser Konfiguration gesendet werden sollen: „Marketing“ für Werbenachrichten, für die das Einverständnis der Benutzenden erforderlich ist, oder „Transaktion“ für nicht kommerzielle Nachrichten, die in bestimmten Situationen auch an abgemeldete Profile gesendet werden können."

Wählen Sie im Abschnitt **E-Mail-Typ** die Art der Nachricht für die Konfiguration aus: **[!UICONTROL Marketing]** oder **[!UICONTROL Transaktion]**.

* Wählen Sie **Marketing** für Werbe-E-Mails aus, z. B. für wöchentliche Werbeaktionen eines Einzelhandelsgeschäfts. Diese Nachrichten erfordern die Zustimmung der Person.

* Wählen Sie **Transaktion** für nicht-kommerzielle E-Mails aus, wie z. B. Bestellbestätigungen, Benachrichtigungen beim Zurücksetzen des Passworts oder Versandinformationen. Diese E-Mails können an Profile gesendet werden, die Marketing-Kommunikationen **abgemeldet** haben. Diese Nachrichten können nur in bestimmten Kontexten gesendet werden.

Wenn Sie eine Nachricht erstellen, müssen Sie eine gültige Kanalkonfiguration auswählen, die der für Ihre E-Mail ausgewählten Kategorie entspricht.

## Subdomain {#subdomains}

Wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll.

>[!NOTE]
>
>Um die Kontrolle über die E-Mail-Einstellungen zu verbessern, können Sie dynamische Subdomains definieren. [Weitere Informationen](../email/surface-personalization.md#dynamic-subdomains)

Um die Reputation Ihrer Domain zu wahren, den IP-Warming-Prozess zu beschleunigen und die Zustellbarkeit zu verbessern, delegieren Sie Ihre sendenden Subdomains an Adobe. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

## Details des IP-Pools {#ip-pools}

Wählen Sie den IP-Pool aus, der mit der Konfiguration verknüpft werden soll. [Weitere Informationen](../configuration/ip-pools.md)

![](assets/surface-subdomain-ip-pool.png){width="50%" align="left"}

Sie können nicht mit der Erstellung der Konfiguration fortfahren, während sich der ausgewählte IP-Pool in [Bearbeitung](../configuration/ip-pools.md#edit-ip-pool) befindet (Status **[!UICONTROL Verarbeitung läuft]**) und noch nie mit der ausgewählten Subdomain verknüpft wurde. In diesem Fall wird weiterhin die älteste Version der IP-Pool-/Subdomain-Zuordnung verwendet. Wenn dies der Fall ist, speichern Sie die Konfiguration als Entwurf und versuchen Sie es erneut, sobald der IP-Pool den Status **[!UICONTROL Erfolg]** erreicht hat.

>[!NOTE]
>
>Für Nicht-Produktionsumgebungen erstellt Adobe keine nativen Test-Subdomains und gewährt auch keinen Zugriff auf einen freigegebenen Versand-IP-Pool. Sie müssen [Ihre eigenen Subdomains delegieren](../configuration/delegate-subdomain.md) und die IPs des Ihrem Unternehmen zugewiesenen Pools verwenden.

Nachdem ein IP-Pool ausgewählt wurde, sind PTR-Informationen zu sehen, wenn Sie den Mauszeiger über die IP-Adressen bewegen, die unter der Dropdown-Liste „IP-Pool“ angezeigt werden. [Weitere Informationen zu PTR-Einträgen](../configuration/ptr-records.md)

>[!NOTE]
>
>Wenn kein PTR-Eintrag konfiguriert ist, wenden Sie sich an den Adobe-Support.

## Abmelden von der Liste {#list-unsubscribe}

Bei der Auswahl einer Subdomain aus der Liste wird die Option **[!UICONTROL Abmelden von der Liste aktivieren]** angezeigt. Diese ist standardmäßig aktiviert.

Dadurch können Sie eine URL zum Abmelden mit einem Klick in die E-Mail-Kopfzeile einfügen. [Weitere Informationen](list-unsubscribe.md)

## Header-Parameter {#email-header}

Geben Sie im Abschnitt **[!UICONTROL Header-Parameter]** die Absendernamen und E-Mail-Adressen ein, die mit dem Typ der mit dieser Konfiguration gesendeten E-Mails verknüpft sind. [Weitere Informationen](header-parameters.md)

## BCC-E-Mail-Adresse {#bcc-email}

Sie können eine identische Kopie (oder Blindkopie) von E-Mails senden, die von [!DNL Journey Optimizer] an einen BCC-Posteingang gesendet wurden, in dem sie für Compliance- oder Archivierungszwecke gespeichert werden.

Aktivieren Sie dazu auf der Ebene der Kanalkonfiguration die optionale Funktion **[!UICONTROL BCC-E-Mail]**. [Weitere Informationen](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

Darüber hinaus ist bei der Definition der **[!UICONTROL BCC-E-Mail]**-Adresse sicherzustellen, dass eine Subdomain mit einer gültigen MX-Eintragskonfiguration verwendet wird. Andernfalls schlägt die Verarbeitung der E-Mail-Konfiguration fehl.

Wenn beim Senden der E-Mail-Konfiguration ein Fehler auftritt, bedeutet dies, dass der MX-Eintrag nicht für die Subdomain der eingegebenen Adresse konfiguriert ist. Sie können die Administrierenden kontaktieren, um den entsprechenden MX-Eintrag zu konfigurieren, oder eine andere Adresse mit einer gültigen MX-Eintragskonfiguration verwenden.

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

Wenn diese Option aktiviert ist, kann eine Kundin bzw. ein Kunde zwar Ihre Marketing-E-Mail als Spam gekennzeichnet haben, wird jedoch Ihre Transaktionsnachrichten unter Verwendung der aktuellen Konfiguration empfangen können. Achten Sie immer darauf, Opt-out-Voreinstellungen gemäß den Best Practices für die Zustellbarkeit zu verwalten.

## Testadressenliste {#seed-list}

>[!CONTEXTUALHELP]
>id="ajo_surface_seed_list"
>title="Testadressenliste hinzufügen"
>abstract="Gewünschte Testadressenliste auswählen, um den Zielgruppen automatisch bestimmte interne Adressen zu hinzuzufügen. Diese Testadressen werden zum Ausführungszeitpunkt des Versands hinzugefügt und erhalten für Sicherheitszwecke eine exakte Kopie der Nachricht."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html?lang=de#use-seed-list" text="Was sind Testadressenlisten?"

Eine Testadressenliste in [!DNL Journey Optimizer] ermöglicht es Ihnen, automatisch bestimmte E-Mail-Testadressen in Ihre Sendungen einzuschließen. [Weitere Informationen](../configuration/seed-lists.md)

>[!CAUTION]
>
>Diese Funktion ist derzeit nur für den E-Mail-Kanal verfügbar.

Wählen Sie die Liste, die für Sie relevant ist, im Abschnitt **[!UICONTROL Testadressenliste]** aus. In [diesem Abschnitt](../configuration/seed-lists.md#create-seed-list) erfahren Sie, wie Sie eine Testadressenliste erstellen.

![](../configuration/assets/seed-list-surface.png){width="80%"}

>[!NOTE]
>
>Es kann jeweils nur eine Testadressenliste ausgewählt werden.

Wenn die aktuelle Konfiguration in einer Kampagne oder einer Journey verwendet wird, werden zum Zeitpunkt der Versandausführung die E-Mail-Adressen in der ausgewählten Testadressenliste einbezogen, d. h. sie erhalten zu Sicherheitszwecken eine Kopie des Versands.

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

Sie können **[!UICONTROL URL-Tracking-Parameter]** verwenden, um die Effektivität Ihrer Marketing-Maßnahmen kanalübergreifend zu messen. [Weitere Informationen](url-tracking.md)

## Ausführungsadresse {#execution-address}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="Überschreiben der zu verwendenden Standard-Ausführungsadresse"
>abstract="Wenn mehrere E-Mail-Adressen in der Datenbank vorhanden sind (privat, beruflich usw.), können Sie auswählen, welche Adresse für den Versand Vorrang haben soll. Die primäre Adresse wird auf Sandbox-Ebene definiert, aber hier können Sie die Standardeinstellung für diese spezifische E-Mail-Konfiguration überschreiben."

Wenn Sie ein Profil als Ziel auswählen, stehen in der Datenbank möglicherweise mehrere E-Mail-Adressen zur Verfügung (private, berufliche E-Mail-Adresse usw.).

In diesem Fall verwendet [!DNL Journey Optimizer] die in den **[!UICONTROL Ausführungsfeldern]** auf Sandbox-Ebene angegebene Adresse, um zu bestimmen, welche E-Mail-Adresse vom Profildienst vorrangig verwendet werden soll. [Weitere Informationen](../configuration/primary-email-addresses.md)

>[!NOTE]
>
>Um die standardmäßig verwendeten Felder zu überprüfen, rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL Ausführungsfelder]** auf.

Dieses standardmäßige Ausführungsfeld kann jedoch auf der Konfigurationsebene des E-Mail-Kanals geändert werden. Diese Einstellung kann dann auf bestimmte Kampagnen oder Journeys angewendet werden.

Bearbeiten Sie dazu das Feld **[!UICONTROL Versandadresse]** und wählen Sie ein Element aus der Liste der verfügbaren XDM-Felder vom Typ E-Mail aus.

![](assets/email-config-delivery-address.png)

Das Ausführungsfeld wird aktualisiert und dann als primäre Adresse verwendet. Dies überschreibt die allgemeine Einstellung auf Sandbox-Ebene.
