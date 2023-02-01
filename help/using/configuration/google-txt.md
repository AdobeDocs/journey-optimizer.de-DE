---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen eines Google TXT-Eintrags zu einer Subdomain
description: Erfahren Sie, wie Sie einen Google TXT-Eintrag zu einer Subdomain hinzufügen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: Subdomain, Google, TXT, Eintrag, Gmail, Zustellbarkeit
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: ht
source-wordcount: '214'
ht-degree: 100%

---

# Hinzufügen eines Google TXT-Eintrags zu einer Subdomain {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="TXT-Einträge von Google"
>abstract="Für einen erfolgreichen Versand von E-Mails an Gmail-Adressen können Sie Ihren Subdomains spezielle TXT-Einträge der Website-Überprüfung von Google hinzuzufügen, um ihre Verifizierung sicherzustellen."

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Für optimale Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen ermöglicht es Ihnen [!DNL Journey Optimizer], Ihren Subdomains spezielle TXT-Einträge der Website-Überprüfung von Google hinzuzufügen, um ihre Verifizierung sicherzustellen.

>[!CAUTION]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomain den Status **[!UICONTROL Erfolg]** aufweist. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](about-subdomain-delegation.md#access-delegated-subdomains).

Gehen Sie wie folgt vor, um Ihrer Subdomain einen Google TXT-Eintrag hinzuzufügen:

1. Öffnen Sie die Subdomain über das Menü **[!UICONTROL Kanäle]** / **[!UICONTROL Subdomains]** .

1. Geben Sie im Abschnitt **[!UICONTROL Google TXT-Eintrag]** den Verifizierungs-Code ein, der in [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> generiert wurde. Klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![](assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, muss er von Google verifiziert werden. Gehen Sie dazu zu [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> und starten Sie den Verifizierungsvorgang.
