---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen eines Google TXT-Eintrags zu einer Subdomain
description: Erfahren Sie, wie Sie einen Google TXT-Eintrag zu einer Subdomain hinzufügen
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Google, TXT, Eintrag, Gmail, Zustellbarkeit
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
TQID: https://experienceleague.adobe.com/FCUB2NeETecjNGYnVhkpkYtEZqgX6y-czXinn2t3J84
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 100%

---

# Hinzufügen eines Google TXT-Eintrags zu einer Subdomain {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="TXT-Einträge von Google"
>abstract="Für einen erfolgreichen Versand von E-Mails an Gmail-Adressen können Subdomains spezielle TXT-Einträge der Website-Überprüfung von Google hinzugefügt werden, um ihre Verifizierung sicherzustellen."

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Für optimale Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen ermöglicht es Ihnen [!DNL Journey Optimizer], Ihren Subdomains spezielle TXT-Einträge der Website-Überprüfung von Google hinzuzufügen, um ihre Verifizierung sicherzustellen.

>[!CAUTION]
>
> Dieser Vorgang kann nur ausgeführt werden, wenn eine Subdomain den Status **[!UICONTROL Erfolg]** aufweist. Weiterführende Informationen zum Status von Subdomains finden Sie in [diesem Abschnitt](delegate-subdomain.md#access-delegated-subdomains).

## Hinzufügen eines Google TXT-Eintrags {#add-google-txt-record}

Gehen Sie wie folgt vor, um Ihrer Subdomain einen Google TXT-Eintrag hinzuzufügen:

1. Öffnen Sie die Subdomain über das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** > **[!UICONTROL Subdomains]**.

1. Geben Sie im Abschnitt **[!UICONTROL Google TXT-Eintrag]** den Verifizierungs-Code ein, der in [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> generiert wurde. Klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![](assets/subdomain-google-txt.png)

1. Nachdem der TXT-Eintrag hinzugefügt wurde, muss er von Google verifiziert werden. Gehen Sie dazu zu [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> und starten Sie den Verifizierungsvorgang.

## Aktualisieren eines Google TXT-Eintrags {#update-google-txt-record}

Gehen Sie wie folgt vor, um einen vorhandenen Google TXT-Eintrag zu aktualisieren:

1. Öffnen Sie die Subdomain über das Menü **[!UICONTROL Subdomains]**.

1. Löschen Sie den vorhandenen Wert im Feld **[!UICONTROL Google TXT-Eintrag]** und klicken Sie auf **[!UICONTROL Speichern]**. Dieser Schritt ersetzt den vorherigen Wert des Google TXT-Eintrags durch eine leere Zeichenfolge.

1. Öffnen Sie nun dieselbe Subdomain erneut und geben Sie den neuen Verifizierungs-Code ein.

1. Klicken Sie erneut auf **[!UICONTROL Speichern]**.

1. Prüfen Sie den aktualisierten Eintrag über [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}.
