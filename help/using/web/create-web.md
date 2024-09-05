---
title: Erstellen von Web-Erlebnissen
description: Erfahren Sie, wie Sie in Journey Optimizer eine Web-Seite erstellen und ihren Inhalt bearbeiten
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 100%

---

# Erstellen von Web-Erlebnissen {#create-web}

[!DNL Journey Optimizer] ermöglicht es Ihnen, das Web-Erlebnis, das Sie Ihren Kunden über eingehende Web-Kampagnen bereitstellen, zu personalisieren.

>[!CAUTION]
>
>Derzeit können Sie Web-Erlebnisse in [!DNL Journey Optimizer] nur mithilfe von **Kampagnen** erstellen. 

[In diesem Video erfahren Sie, wie Sie eine Web-Kampagne verfassen](#video)

## Erstellen einer Web-Kampagne {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definieren einer Web-Konfiguration"
>abstract="Eine Web-Konfiguration kann einer einzelnen Seiten-URL oder mehreren Seiten entsprechen, sodass inhaltliche Änderungen auf einer oder mehreren Web-Seiten vorgenommen werden können."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Erstellen einer Regel zum Seitenabgleich"
>abstract="Eine Regel zum Seitenabgleich macht es möglich, mehrere URLs, die derselben Regel entsprechen, als Ziel auszuwählen. Dies ist zum Beispiel praktisch, wenn die Änderungen an einem Hero-Banner auf einer ganzen Website angewendet oder oben ein Bild hinzugefügt werden soll, das auf allen Produktseiten einer Website angezeigt wird."

Gehen Sie wie folgt vor, um mit der Erstellung Ihres Web-Erlebnisses durch eine Kampagne zu beginnen.

>[!NOTE]
>
>Wenn Sie zum ersten Mal ein Web-Erlebnis erstellen, stellen Sie sicher, dass Sie die in [diesem Abschnitt](web-prerequisites.md) beschriebenen Voraussetzungen befolgen.

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.[Weitere Informationen](../campaigns/create-campaign.md)


1. Wählen Sie den Typ der Kampagne aus, die Sie ausführen möchten.

   * **Geplant – Marketing**: die Kampagne wird sofort oder an einem bestimmten Datum ausgeführt. Geplante Kampagnen dienen dem Versand von Marketing-Nachrichten. Sie werden über die Benutzeroberfläche konfiguriert und ausgeführt.

   * **API-ausgelöst – Marketing/Transaktion**: die Kampagne wird mithilfe eines API-Aufrufs ausgeführt.  API-ausgelöste Kampagnen zielen auf den Versand von Nachrichten des Typs „Marketing“ oder „Transaktion“ ab. Beim Typ „Transaktion“ handelt es sich um Nachrichten, die nach einer von einem Kontakt durchgeführten Aktion verschickt werden: Zurücksetzen des Passworts und Verlassen des Warenkorbs.

1. Führen Sie die Schritte zur Erstellung einer Web-Kampagne aus, z. B. die Kampagneneigenschaften, [Zielgruppe](../audience/about-audiences.md) und [Zeitplan](../campaigns/create-campaign.md#schedule).

1. Wählen Sie die Aktion **[!UICONTROL Web]**.

1. Wählen Sie eine Konfiguration aus oder erstellen Sie eine neue Konfiguration. [Weitere Informationen zur Web-Konfiguration](web-configuration.md).

   ![](assets/web-campaign-steps.png)

Weitere Informationen zur Konfiguration Ihrer Kampagne finden Sie auf [dieser Seite](../campaigns/get-started-with-campaigns.md).

## Testen der Web-Kampagne {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Vorschau des Web-Erlebnisses"
>abstract="Betrachten Sie in einer Simulation, wie Ihr Web-Erlebnis aussehen wird."

Sobald Sie mit dem Web-Designer [das Web-Erlebnis erstellt haben](edit-web-content.md), können Sie mithilfe der Testprofile eine Vorschau der geänderten Web-Seiten anzeigen. Wenn Sie personalisierte Inhalte eingefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie diese Inhalte angezeigt werden.

Klicken Sie dazu entweder im Bildschirm zur Inhaltsbearbeitung einer Web-Kampagne oder im Web-Designer auf **[!UICONTROL Inhalt simulieren]** und fügen Sie dann ein Testprofil hinzu, um Ihre Web-Seite mithilfe der Testprofildaten zu überprüfen.

![](assets/web-designer-preview.png)

Sie können sie auch im Standard-Browser öffnen oder die Test-URL kopieren, um sie in einen beliebigen Browser einzufügen. Auf diese Weise können Sie den Link für Ihr Team und Ihre Interessensgruppen freigeben, damit sie in der Lage sind, das neue Web-Erlebnis in einem beliebigen Browser in der Vorschau zu betrachten, bevor die Kampagne live geschaltet wird.

>[!NOTE]
>
>Beim Kopieren der Test-URL ist der angezeigte Inhalt derjenige, der für das Testprofil personalisiert wurde, das zum Zeitpunkt der Erstellung der Inhaltsimulation in [!DNL Journey Optimizer] verwendet wurde.

Detaillierte Informationen zur Auswahl von Testprofilen und zur Vorschau Ihres Inhalts finden Sie im Abschnitt [Content-Management](../content-management/preview-test.md).

## Aktivieren der Web-Kampagne {#activate-web-campaign}

Nachdem Sie Ihre [Web-Kampagneneinstellungen](#configure-web-campaign) festgelegt und Ihren Inhalt wie gewünscht mit dem [Web-Designer](edit-web-content.md#work-with-web-designer) bearbeitet haben, können Sie Ihre Web-Kampagne überprüfen und aktivieren. Führen Sie dazu folgende Schritte durch.

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. Wählen Sie in Ihrer Web-Kampagne die Option **[!UICONTROL Zur Aktivierung überprüfen]** aus.

1. Überprüfen und bearbeiten Sie bei Bedarf Inhalt, Eigenschaften, Konfiguration, Zielgruppe und Zeitplan.

1. Wählen Sie **[!UICONTROL Aktivieren]** aus.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Nachdem Sie auf **[!UICONTROL Aktivieren]** geklickt haben, kann es bis zu 15 Minuten dauern, bis Web-Kampagnenänderungen auf Ihrer Website live sind.

Ihre Web-Kampagne geht in den **[!UICONTROL Live]**-Status über und ist nun für die ausgewählte Zielgruppe sichtbar. Jeder Empfänger Ihrer Kampagne kann die Änderungen sehen, die Sie Ihrer Website mithilfe des Web-Designers von [!DNL Journey Optimizer] hinzugefügt haben.

>[!NOTE]
>
>Wenn Sie einen Zeitplan für Ihre Web-Kampagne definiert haben, hat sie den Status **[!UICONTROL Geplant]**, bis das Startdatum und die Startzeit erreicht werden.
>
>Wenn Sie eine Web-Kampagne aktivieren, die sich auf dieselben Seiten auswirkt wie eine andere bereits aktive Kampagne, werden alle Änderungen auf Ihre Web-Seiten angewendet.

Weitere Informationen zur Aktivierung von Kampagnen finden Sie in [diesem Abschnitt](../campaigns/review-activate-campaign.md).

## Stoppen einer Web-Kampagne {#stop-web-campaign}

Wenn eine Web-Kampagne live ist, können Sie sie stoppen, um zu verhindern, dass Ihre Änderungen für Ihre Zielgruppe sichtbar werden. Führen Sie dazu folgende Schritte durch.

1. Wählen Sie eine Live-Kampagne aus der Liste aus.

1. Wählen Sie im oberen Menü **[!UICONTROL Kampagne stoppen]** aus.

   ![](assets/web-campaign-stop.png)

1. Die hinzugefügten Änderungen sind dann für die von Ihnen definierte Zielgruppe nicht mehr sichtbar.

>[!NOTE]
>
>Nachdem eine Web-Kampagne gestoppt wurde, kann sie nicht mehr bearbeitet oder wieder aktiviert werden. Sie können sie nur duplizieren und dann die duplizierte Kampagne aktivieren.

## Anleitungsvideo{#video}

Im folgenden Video erfahren Sie, wie Sie eine Web-Kampagne erstellen, ihre Eigenschaften konfigurieren, sie überprüfen und veröffentlichen.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)