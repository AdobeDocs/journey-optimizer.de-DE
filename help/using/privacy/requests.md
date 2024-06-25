---
solution: Journey Optimizer
product: journey optimizer
title: Datenschutzanfragen
description: Erfahren Sie mehr über Datenschutzanfragen und den Privacy Service.
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: 41717213cb75185476f054bd076e67f942be0f1c
workflow-type: ht
source-wordcount: '457'
ht-degree: 100%

---

# Datenschutzanfragen {#track-changes}

Der **Privacy Service** von Adobe Experience Platform stellt eine RESTful-API und eine Benutzeroberfläche bereit, mit der Sie Anfragen zu Kundendaten verwalten können. Mit Privacy Service können Sie Anfragen zum Zugreifen auf und Löschen von personenbezogene(n) Kundendaten aus Adobe Experience Cloud-Programmen stellen, was die automatische Einhaltung gesetzlicher und unternehmensinterner Datenschutzbestimmungen erleichtert.

Datenschutzanfragen können über das Menü **[!UICONTROL Anfragen]** erstellt und verwaltet werden.

![](assets/requests.png)

Weitere Informationen zu Privacy Service und zum Erstellen und Verwalten von Datenschutzanfragen finden Sie in der Adobe Experience Platform-Dokumentation:

* [Übersicht über den Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de)
* [Verwalten von Datenschutzaufträgen in der Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de)



## Verwalten einzelner Datenschutzanfragen, die Sie an Adobe Journey Optimizer senden können {#data-privacy-requests}

Sie können individuelle Anfragen zum Zugriff auf und zum Löschen von Verbraucherdaten aus Adobe Journey Optimizer auf zwei Arten senden:

* Über die **Privacy Service-Benutzeroberfläche**. Informationen finden Sie in der Dokumentation [hier](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/ui/user-guide#_blank).
* Über das **Privacy Service-API**. Informationen finden Sie in der Dokumentation [hier](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank) und in den API-Informationen [hier](https://developer.adobe.com/experience-platform-apis/#_blank).

Der Privacy Service unterstützt zwei Arten von Anfragen: **Datenzugriff** und **Datenlöschung**.

>[!NOTE]
>
>In diesem Handbuch wird nur beschrieben, wie Sie Datenschutzanfragen für Adobe Journey Optimizer stellen. Wenn Sie auch Datenschutzanfragen für den Platform-Data-Lake planen, lesen Sie dieses [Handbuch](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/privacy) zusätzlich zu diesem Tutorial. Informationen zum Echtzeit-Kundenprofil finden Sie in diesem [Handbuch](https://experienceleague.adobe.com/de/docs/experience-platform/profile/privacy). Informationen zum Identity Service finden Sie in diesem [Handbuch](https://experienceleague.adobe.com/de/docs/experience-platform/identity/privacy). Bei Anfragen zum Löschen und für den Zugriff müssen Sie diese einzelnen Systeme aufrufen, um sicherzustellen, dass die Anfragen von jedem einzelnen System bearbeitet werden. Durch eine Datenschutzanfrage an Adobe Journey Optimizer werden die Daten nicht aus all diesen Systemen entfernt.

Für **Anfragen für den Zugriff** geben Sie „Adobe Journey Optimizer“ über die Benutzeroberfläche an (oder „CJM“ als Produkt-Code im API).

Für **Anfragen zum Löschen** müssen Sie zusätzlich zur Anfrage „Adobe Journey Optimizer“ auch Anfragen zum Löschen an drei vorgelagerte Services senden, um zu verhindern, dass Journey Optimizer die gelöschten Daten wieder aufnimmt. Wenn diese vorgelagerten Services nicht angegeben werden, bleibt die Anfrage „Adobe Journey Optimizer“ im Verarbeitungsstatus, bis Anfragen zum Löschen für die vorgelagerten Services erstellt werden.

Bei den drei vorgelagerten Services handelt es sich um:

* Profile (Produkt-Code: „profileService“)
* AEP Data Lake (Produkt-Code: „AdobeCloudPlatform“)
* Identity (Produkt-Code: „identity“)

## Erstellen von Anfragen für den Zugriff und zum Löschen

### Voraussetzungen

Um Anfragen für den Zugriff auf und zum Löschen von Daten in Adobe Journey Optimizer zu stellen, ist Folgendes erforderlich:

* eine IMS-Organisations-ID
* eine Identitätskennung der Person, auf die Sie reagieren möchten, und die entsprechenden Namespaces. Weitere Informationen zu Identity-Namespaces in Adobe Journey Optimizer und Experience Platform finden Sie im Abschnitt [Übersicht zu Identity-Namespace](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces).

### Erforderliche Feldwerte in Adobe Journey Optimizer für API-Anfragen

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your IMS Org ID Value>

"users":
    "action": either access or delete

    "userIDs":
        "namespace": e.g. email, aaid, ecid, etc.
        "type": standard
        "value": <Data Subject's Identity Identifier>

"include":
    CJM (which is the Adobe product code for Adobe Journey Optimizer)
    profileService (product code for Profile)
    AdobeCloudPlatform (product code for AEP Data Lake)
    identity (product code for Identity)

"regulation":
    gdpr, ccpa, pdpa, lgpd_bra, or nzpa_nzl (which is the privacy regulation that applies to the request)
```


### Beispiel für eine DSGVO-Zugriffsanfrage:

Über die Benutzeroberfläche:

![](assets/accessrequest.png)

Über das API:

```json
// JSON Request
{
   "companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"745F37C35E4B776E0A49421B@AdobeOrg"
      }
   ],
   "users":[
      {
         "action":[
            "access"
         ],
         "userIDs":[
            {
               "namespace":"ecid",
               "value":"38400000-8cf0-11bd-b23e-10b96e40000d",
               "type":"standard"
            },
            {
               "namespace":"email",
               "value":"johndoe4@gmail.com",
               "type":"standard"
            }
         ]
      }
   ],
   "include":[
      "CJM"
   ],
   "regulation":"gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "access"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

### Beispiel für eine DSGVO-Anfrage zum Löschen:

Über die Benutzeroberfläche:

![](assets/deleterequest.png)

Über das API:

```json
// JSON Request
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "745F37C35E4B776E0A49421B@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
          "delete"
      ],
      "userIDs": [
        {
          "namespace": "ecid",
          "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
          "type": "standard"
        },
                {
          "namespace": "email",
          "value": "johndoe4@gmail.com",
          "type": "standard"
        }
      ]
    }
  ],
  "include": [
    "CJM", "profileService", "AdobeCloudPlatform", "identity"
  ],
  "regulation": "gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "delete"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```
