---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei benutzerdefinierten Aktionen
description: Informationen zur Fehlerbehebung bei einer benutzerdefinierten Aktion
badge: label="Eingeschränkte Verfügbarkeit"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Aktion, Drittanbieter, benutzerdefiniert, Journeys, API
source-git-commit: d6501c8cc7e3293bd6a057d8e74654bced7dae75
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 3%

---


# Fehlerbehebung bei benutzerdefinierten Aktionen {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.
>

Sie können Ihre benutzerdefinierten Aktionen testen, indem Sie API-Aufrufe aus dem Abschnitt Administration der Benutzeroberfläche von Journey Optimizer senden. Mit dieser Funktion können Sie Fehler bei benutzerdefinierten Aktionen beheben, bevor oder nachdem diese auf einer Journey verwendet werden.

Verwenden Sie als Administrator die Funktion **[!UICONTROL Testanfrage senden]** um Ihre benutzerdefinierten Aktionskonfigurationen zu validieren, indem Sie echte API-Aufrufe direkt von Adobe Journey Optimizer aus durchführen. Mit dieser Funktion wird sichergestellt, dass Anfragestruktur, Kopfzeilen, Authentifizierung und Payload korrekt formatiert sind, bevor sie auf einer Journey verwendet werden.

![](assets/send-test-request.png){width="70%" align="left"}

Mit dieser Funktion wird der Test- und Validierungsprozess optimiert, sodass benutzerdefinierte Aktionen in Live-Journey ordnungsgemäß funktionieren.

## Voraussetzungen {#troubleshoot-custom-action-prereq}

Um die Funktion **[!UICONTROL Testanfrage senden]** verwenden zu können, muss **benutzerdefinierte Aktion** mit einer URL, Kopfzeilen und Authentifizierungseinstellungen vorkonfiguriert werden.

Damit Admins diese Funktion verwenden können, sind die folgenden Berechtigungen erforderlich:

* Benutzer müssen über die Berechtigung **[!DNL Manage journeys events, data sources and actions]** verfügen.
* Diese Berechtigung ist in der Rolle *Journey-Administratoren* enthalten.
* Die Berechtigung **[!DNL View journeys events]** allein reicht nicht aus.

Weitere Informationen zu Journey-Berechtigungen finden Sie [ (diesem Abschnitt](../administration/high-low-permissions.md#journey-capability).

## Verwendung der Funktion „Testanfrage senden“ {#troubleshoot-custom-action-use}

Gehen Sie wie folgt vor, um eine benutzerdefinierte Aktion zu testen:

1. Navigieren Sie zum Konfigurationsbildschirm **Aktionen** und wählen Sie eine benutzerdefinierte Aktion aus.
1. Klicken Sie auf die **[!UICONTROL Testanfrage senden]** Schaltfläche unten im Bildschirm für die Aktionskonfiguration.
   ![Schaltfläche „Testanfrage senden“ im Bereich „Aktionskonfiguration“](assets/test-request.png){width="70%" align="left"}
1. Im Popup-Fenster können Sie Anforderungsparameter angeben:

   * Wenn die **benutzerdefinierte Aktionsmethode GET** ist, ist keine Payload erforderlich.
   * Wenn die **benutzerdefinierte Aktionsmethode POST“ ist** müssen Sie eine JSON-Payload angeben.

     >[!NOTE]
     >
     >Adobe Journey Optimizer löst einen Fehler aus, wenn die Struktur dieser JSON falsch ist, aber nicht, wenn keine Übereinstimmung mit einem Datentyp vorliegt. Beispielsweise gibt es keinen Fehler, wenn ein ganzzahliger Parameter für eine Zeichenfolge verwendet wird.

   * Wenn die Authentifizierung definiert ist, werden Sie aufgefordert, Authentifizierungsdetails einzugeben.

1. Klicken Sie **Senden** um die Anfrage auszuführen.
1. Die Antwort der API, einschließlich Kopfzeilen und Status-Codes, wird in der Benutzeroberfläche angezeigt.

## Authentifizierungsverarbeitung {#troubleshoot-custom-action-auth}

Wenn eine benutzerdefinierte Aktion eine Authentifizierung enthält, verlangt Adobe Journey Optimizer, dass der Benutzer Authentifizierungsdetails für jede Testanfrage eingibt:

* **Einfache Authentifizierung:** Der Benutzer muss das *Kennwort“*.
* **API-Schlüsselauthentifizierung:** Der Benutzer muss den API-Schlüssel (*)*.
* **Benutzerdefinierte Authentifizierung:** Der Benutzer muss die Authentifizierungsparameter in der Anfrage (bodyParam *angeben*. In diesem Fall werden zwei Abschnitte hinzugefügt: **Authentifizierungsanfrage** und **Authentifizierungsantwort**.

## Wesentliche Vorteile {#troubleshoot-custom-action-benefits}

Als Journey Optimizer-Administrator können Sie auch externe Tools (z. B. Postman) verwenden, um Ihre benutzerdefinierten Aktionen zu testen. Die wichtigsten Vorteile der produktinternen Fehlerbehebungsfunktion im Vergleich zu einem externen Test sind unten aufgeführt:

* Die Testanfrage wird von **AJO Journey** ausgeführt, was bedeutet:

   * Die exakte Anfragestruktur (einschließlich Adobe Journey Optimizer-spezifischer Kopfzeilen) wird verwendet.
   * Die Quell-IP und -Kopfzeilen stimmen mit denen überein, die in Live-Journey verwendet werden.

* Die Funktion **[!UICONTROL Testanfrage senden]** kann zur Fehlerbehebung (**-Journey-**) verwendet werden, da die benutzerdefinierte Aktion bereits bereitgestellt ist.

* Durch diese produktinterne Testfunktion entfällt die Notwendigkeit, Konfigurationsdetails manuell zwischen Tools zu kopieren, wodurch das Fehlerrisiko reduziert wird.

## Fehlerbehebung {#troubleshoot-custom-action-check}

Wenn die Anfrage fehlschlägt, können Sie Folgendes überprüfen:

* Die im Test eingegebenen Authentifizierungsdaten.
* Die Anfragemethode (GET vs. POST) und die entsprechende Payload.
* Der API-Endpunkt und die Header, die in der benutzerdefinierten Aktion definiert sind.
* Verwenden Sie die Antwortdaten, um potenzielle Fehlkonfigurationen zu identifizieren.

