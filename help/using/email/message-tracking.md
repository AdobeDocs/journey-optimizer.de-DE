---
solution: Journey Optimizer
product: journey optimizer
title: Verfolgen von Nachrichten
description: Erfahren Sie, wie Sie Links hinzufügen und gesendete Nachrichten verfolgen können.
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: Links, Tracking, Überwachen, E-Mail
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 288e3418b7152410166ddb9e520997933f1f589c
workflow-type: tm+mt
source-wordcount: '1380'
ht-degree: 95%

---

# Hinzufügen von Links und Verfolgen von Nachrichten {#tracking}

Verwenden Sie [!DNL Journey Optimizer], um Links zu Ihrem Inhalt hinzuzufügen und die gesendeten Nachrichten zu verfolgen und so das Verhalten Ihrer Empfängerinnen und Empfänger zu überwachen.

>[!NOTE]
>
>Wenn in Ihrem Inhalt Links enthalten sind, laufen sie **25 Monate** nach dem Versand der Nachricht ab, mit Ausnahme von Links zu einer Mirror-Seite, die nach **90 Tagen** ablaufen. Nach Ablauf dieser Dauer sind die Links nicht mehr verfügbar.

## Aktivieren von Tracking {#enable-tracking}

Sie können das Tracking einer E-Mail-Nachricht aktivieren, indem Sie die Optionen **[!UICONTROL E-Mail-Öffnungen]** und/oder **[!UICONTROL Klick in E-Mail]** markieren, wenn Sie Ihre Nachricht in einer Journey oder Kampagne erstellen, wie auf den Registerkarten unten dargestellt.

>[!BEGINTABS]

>[!TAB Aktivieren des Trackings in einer Journey]

![](assets/message-tracking-journey.png)

>[!TAB Aktivieren des Trackings in einer Kampagne]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>Beide Optionen sind standardmäßig aktiviert.

Wenn diese Optionen aktiviert sind, verfolgen Sie das Verhalten der Empfangenden Ihrer Nachrichten:

* Die Metrik **[!UICONTROL E-Mail-Öffnungen]** überprüft, wie viele Nachrichten geöffnet wurden.
* Die Metrik **[!UICONTROL Klick in E-Mail]** berechnet die Anzahl der Klicks auf Links in einer E-Mail.

## Links einfügen {#insert-links}

Wenn das [Tracking aktiviert ist](#enable-tracking), werden alle im Nachrichteninhalt enthaltenen Links nachverfolgt.

>[!NOTE]
>
>Links aus Fragmenten, die in einer E-Mail verwendet werden, werden ebenfalls nachverfolgt. [Erfahren Sie mehr über Fragmente](../content-management/fragments.md)

Gehen Sie wie folgt vor, um Links in Ihren E-Mail-Inhalt einzufügen:

1. Wählen Sie ein Element (Text oder Bild) aus und klicken Sie in der kontextuellen Symbolleiste auf **[!UICONTROL Link einfügen]**.

   ![](assets/message-tracking-insert-link.png)

1. Wählen Sie den gewünschten Link-Typ aus.

   * Wählen Sie **[!UICONTROL Externer Link]** aus, um einen Link auf eine externe URL einzufügen.

   * Wählen Sie **[!UICONTROL Landingpage]** aus, um einen Link zu einer Landingpage einzufügen. [Weitere Informationen](../landing-pages/get-started-lp.md)

   * Wählen Sie **[!UICONTROL Opt-out mit einem Klick]** aus, um einen Link einzufügen, über den die Benutzenden Ihre Nachrichten schnell kündigen können, ohne den Kündigungsvorgang bestätigen zu müssen. [Weitere Informationen](email-opt-out.md#one-click-opt-out).

   * Wählen Sie **[!UICONTROL Externes Opt-in/Anmeldung]** aus, um einen Link für das Akzeptieren des Erhalts von Nachrichten von Ihrer Marke einzufügen.

   * Wählen Sie **[!UICONTROL Externes Opt-out/Abmeldung]** aus, um einen Link einzufügen, über den man sich vom Erhalt von Nachrichten Ihrer Marke abmelden kann. Weitere Informationen zur Opt-out-Verwaltung finden Sie in [diesem Abschnitt](email-opt-out.md#email-opt-out).

   * Wählen Sie **[!UICONTROL Mirror-Seite]** aus, um der Mirror-Seite der E-Mail einen Link hinzuzufügen. [Weitere Informationen](#mirror-page)

1. Geben Sie die gewünschte URL in das entsprechende Feld ein oder wählen Sie eine Landingpage aus und definieren Sie die Link-Einstellungen und -Stile. [Weitere Informationen](#adjust-links)

   >[!NOTE]
   >
   >Zum Interpretieren von URLs hält sich [!DNL Journey Optimizer] an die URI-Syntax ([RFC 3986-Standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}), sodass einige internationale Sonderzeichen in URLs unterbunden werden. Wenn beim Test- oder E-Mail-Versand ein Fehler im Zusammenhang mit einer URL zurückgegeben wird, die zu Ihrem Inhalt hinzugefügt wurde, können Sie für die Zeichenfolge eine URL-Codierung durchführen und so das Problem umgehen.

1. Sie können Ihre Links personalisieren. [Weitere Informationen](../personalization/personalization-build-expressions.md)

1. Speichern Sie Ihre Änderungen.

1. Sobald der Link erstellt ist, können Sie ihn in den Bereichen **[!UICONTROL Einstellungen]** und **[!UICONTROL Stile]** auf der rechten Seite noch ändern.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>E-Mail-Nachrichten vom Typ Marketing müssen einen [Ausschluss-Link](../privacy/opt-out.md#opt-out-decision-management) enthalten, der für Transaktionsnachrichten nicht erforderlich ist. Die Nachrichtenkategorie (**[!UICONTROL Marketing]** oder **[!UICONTROL Transaktion]**) wird beim Erstellen der Nachricht in der [Kanalkonfiguration](email-settings.md#email-type) definiert.

Nach dem Versand der Nachricht beträgt die Gültigkeitsdauer für einen Link **25 Monate**. Nach dieser Dauer ist der Link nicht mehr verfügbar.

>[!CAUTION]
>
>Wenn sowohl **label** als auch **URL** einer Schaltfläche in einem Fragment bearbeitbar gemacht werden können, wird in Tracking-Berichten die URL anstelle der Schaltflächenbeschriftung angezeigt. Das Feld `_experience.customerJourneyManagement.messageInteraction.label` im Tracking-Datensatz protokolliert den URL-Wert.

## Link zu einer Mirror-Seite {#mirror-page}

Die Mirror-Seite ist eine Online-Version Ihrer E-Mail. Beim E-Mail-Marketing empfiehlt es sich, einen Link zur Mirror-Seite hinzuzufügen. Benutzerinnen und Benutzer können die Mirrorseite einer E-Mail aufrufen, etwa wenn bei der Anzeige in ihrem Posteingang Rendering-Probleme auftreten oder Bilder beschädigt sind. Es wird außerdem empfohlen, aus Gründen der Barrierefreiheit oder um zum Social Sharing zu ermutigen, eine Online-Version bereitzustellen.

Die von Adobe Journey Optimizer generierte Mirror-Seite enthält alle Personalisierungsdaten.

Um Ihrer E-Mail einen Link zu einer Mirror-Seite hinzuzufügen, fügen Sie [einen Link](#insert-links) ein und wählen Sie **[!UICONTROL Mirror-Seite]** als Link-Typ aus.

![](assets/message-tracking-mirror-page.png)

Die Mirror-Seite wird automatisch erstellt. Wenn die Empfänger nach dem Versand der E-Mail auf den Mirror-Seiten-Link klicken, wird der Inhalt der E-Mail in ihrem Standard-Webbrowser angezeigt.

Die Gültigkeitsdauer für eine Mirror-Seite beträgt **90 Tage**. Nach dieser Verzögerung ist die Mirror-Seite nicht mehr verfügbar.

>[!CAUTION]
>
>* Links zu Mirrorseiten werden automatisch generiert und können nicht bearbeitet werden. Sie enthalten alle verschlüsselten personalisierten Daten, die zum Rendern der ursprünglichen E-Mail erforderlich sind. Daher kann die Verwendung personalisierter Attribute mit großen Werten zu langen Mirror-Seiten-URLs führen, was verhindert, dass der Link in Webbrowsern mit einer maximalen URL-Länge funktioniert.
>
>* Beim Erstellen von E-Mails, die stark von der Laufzeitpersonalisierung abhängen (z. B. `#each`-Schleifen, verschachtelte Objekte, große Payload-Daten), können die URLs der Mirror-Seite übermäßig groß werden, insbesondere in durch API ausgelösten Kampagnen, die umfangreiche kontextuelle Daten aus Payloads verwenden. Dies kann HTTP-Fehler (404, 422, 502) in Browsern oder Mail-Clients verursachen. Adobe empfiehlt, die Breite und Tiefe dynamischer Felder zu begrenzen, die Abhängigkeit von komplexen Fragmenten zu reduzieren und Personalisierungsstrukturen zu vereinfachen, um Link-Fehler zu vermeiden.
>
>* Im [Testversand](../content-management/proofs.md) an die Testprofile ist der Link zur Mirror-Seite nicht aktiv. Er wird erst in den endgültigen Nachrichten aktiv.

## Anpassen von Link-Erscheinungsbild und Ziel {#adjust-links}

Sie Anpassungen Ihrer Links vornehmen, in dem Sie sie z. B. unterstreichen, ihre Farbe ändern oder ihr Ziel auswählen.  Diese Änderungen werden in den Bereichen **[!UICONTROL Einstellungen]** und **[!UICONTROL Stile]** im rechten Abschnitt des Inhaltseditors festgelegt.

### Target {#link-target}

Mit dem Attribut **Ziel** lässt sich steuern, wo eine verknüpfte Seite geöffnet wird. Durch Hinzufügen des Attributs „Ziel“ in einem Anker-Tag kann angegeben werden, ob der Link auf einer neuen Registerkarte, auf derselben Registerkarte oder in einem anderen Frame geöffnet werden soll.

Gehen Sie wie folgt vor, um das Ziel eines Links zu definieren:

1. Wählen Sie in einer **[!UICONTROL Text]**-Komponente, in die ein Link eingefügt ist, Ihren Link aus.

1. Wählen Sie auf der Registerkarte **[!UICONTROL Einstellungen]** im Dropdown-Menü **[!UICONTROL Ziel]** aus, wo der Link geöffnet wird. Nachfolgend sind mögliche Werte aufgeführt:

   * **[!UICONTROL None]**: öffnet den Link in demselben Frame, in dem er angeklickt wurde (Standardwert).
   * **[!UICONTROL Blank]**: öffnet den Link in einem neuen Fenster oder auf einer neuen Registerkarte.
   * **[!UICONTROL Self]**: öffnet den Link in demselben Frame, in dem er angeklickt wurde.
   * **[!UICONTROL Parent]**: öffnet den Link im übergeordneten Frame.
   * **[!UICONTROL Top]**: öffnet den Link im gesamten Fenster.

   ![](assets/link_2.png)

1. Speichern Sie Ihre Änderungen.


### Unterstreichen eines Links {#link-underline}

Markieren Sie die Option **[!UICONTROL Link unterstreichen]**, damit das Label Ihres Links unterstrichen wird.

![](assets/link_1.png)

### Farbe des Links {#link-color}

Um die Farbe Ihres Links zu ändern, klicken Sie auf **[!UICONTROL Link-Farbe]** auf der Registerkarte **[!UICONTROL Stile]**.

![](assets/link_3.png)


## Tracking verwalten {#manage-tracking}

Mit [E-Mail-Designer](content-from-scratch.md) können Sie die verfolgten URLs verwalten, z. B. den Tracking-Typ für jeden Link bearbeiten.

1. Klicken Sie auf das Symbol **[!UICONTROL Links]** im linken Bereich, um die Liste aller URLs Ihres Inhalts, die verfolgt werden sollen, anzuzeigen.

   Diese Liste bietet einen guten Überblick und ermöglicht das Auffinden aller im E-Mail-Inhalt vorhandenen URLs.

1. Um einen Link zu bearbeiten, wählen Sie das entsprechende Stiftsymbol aus.

1. Sie können den **[!UICONTROL Tracking-Typ]** bei Bedarf ändern:

   ![](assets/message-tracking-edit-a-link.png)

   Für jede verfolgte URL können Sie einen der folgenden Tracking-Modi festlegen:

   * **[!UICONTROL Verfolgt]**: Aktiviert das Tracking dieser URL.
   * **[!UICONTROL Opt-out]**: Diese URL wird als Opt-out- oder Abmelde-URL behandelt.
   * **[!UICONTROL Mirrorseite]**: Diese URL wird als Mirror-Seite behandelt.
   * **[!UICONTROL Nie]**: Das Tracking dieser URL wird nie aktiviert.

Reporting zu Öffnungen und Klicks ist im [Live-Bericht](../reports/live-report.md) und im [Customer Journey Analytics-Bericht](../reports/report-gs-cja.md) verfügbar.

## Personalisieren des URL-Trackings {#url-tracking}

Das [URL-Tracking](email-settings.md#url-tracking) wird auf Konfigurationsebene verwaltet und gilt für alle im Nachrichteninhalt vorhandenen URLs.

Sie können im E-Mail-Designer auch einzelne URLs personalisieren. Gehen Sie wie folgt vor, um einem Link in Ihrem Inhalt personalisierte URL-Tracking-Parameter hinzuzufügen.

1. Wählen Sie einen Link aus und klicken Sie in der kontextbezogenen Symbolleiste auf **[!UICONTROL Link einfügen]**.

1. Wählen Sie das Personalisierungssymbol aus. Das Personalisierungssymbol ist nur für folgende Arten von Links verfügbar: **externer Link**, **Abmelde-Link** und **Ausschluss-Link**.

   ![](assets/message-tracking-insert-link-perso.png)

1. Fügen Sie den URL-Tracking-Parameter hinzu und wählen Sie im [Personalisierungseditor](../personalization/personalization-build-expressions.md) das gewünschte Profilattribut aus.

   ![](assets/message-tracking-perso-parameter.png)

1. Speichern Sie Ihre Änderungen.

1. Wiederholen Sie die obigen Schritte für jeden Link, dem Sie diesen Tracking-Parameter hinzufügen möchten.

Wenn die E-Mail gesendet wird, wird dieser Parameter nun automatisch an das Ende der URL angehängt. Sie können diesen Parameter dann in Web-Analyse-Tools oder in Leistungsberichten erfassen.

>[!NOTE]
>
>Um die endgültige URL zu überprüfen, können Sie einen [Testversand durchführen](../content-management/proofs.md) und auf den Link im E-Mail-Inhalt klicken, sobald Sie die als Testversand vorgesehene Nachricht erhalten haben. Die URL sollte den Tracking-Parameter anzeigen. Im obigen Beispiel lautet die endgültige URL: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>
