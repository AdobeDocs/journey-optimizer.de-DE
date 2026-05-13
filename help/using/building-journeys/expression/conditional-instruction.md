---
solution: Journey Optimizer
product: journey optimizer
title: Bedingte Anweisung (if, then, else)
description: Erfahren Sie mehr über die bedingte Anweisung
feature: Journeys
role: Developer
level: Experienced
keywords: erweitert, Bedingung, Aktion, Journey
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cce82f05-fc3c-4af7-85ff-8bba603861a7
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 100%

---

# Bedingte Anweisung (if, then, else) {#conditional-instruction}

Die bedingte Anweisung (if, then, else) wird im erweiterten Editor unterstützt. Sie ermöglicht die Definition komplexerer Ausdrücke. Sie umfasst die folgenden Elemente:

* **[!UICONTROL if]**: die Bedingung, die zuerst ausgewertet werden soll.
* **[!UICONTROL then]**: der auszuwertende Ausdruck, falls das Ergebnis der Auswertung der Bedingung wahr ist.
* **[!UICONTROL else]**: der auszuwertende Ausdruck, falls das Ergebnis der Auswertung der Bedingung falsch ist.

>[!NOTE]
>
>Alle Ausdrücke müssen in Klammern gesetzt werden.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` muss einen booleschen Wert (**boolean**) zurückgeben.

`<expression2>` und `<expression3>` müssen denselben Typ oder kompatible Typen aufweisen. Folgende Signaturen und zurückgegebene Typen werden unterstützt:

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**Verwendung**

Mit der bedingten Anweisung können Sie den Workflow der Journey optimieren, indem Sie die Anzahl der Bedingungsaktivitäten reduzieren. Beispielsweise können Sie innerhalb derselben Aktionsaktivität zwei Alternativen für eine Felddefinition angeben, wobei nur ein Bedingungsausdruck verwendet wird.

Beispiel für eine Aktionsaktivität (für ein Feld, das eine Zeichenfolge als Ergebnis der bedingten Anweisung erwartet):

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
