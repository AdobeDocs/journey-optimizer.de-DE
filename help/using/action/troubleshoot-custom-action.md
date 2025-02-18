---
solution: Journey Optimizer
product: journey optimizer
title: Testen einer benutzerdefinierten Aktion
description: Informationen zur Fehlerbehebung bei einer benutzerdefinierten Aktion
badge: label="Eingeschränkte Verfügbarkeit"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Aktion, Drittanbieter, benutzerdefiniert, Journeys, API
source-git-commit: 5ce76bd61a61e1ed5e896f8da224fc20fba74b53
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 3%

---


# Fehlerbehebung bei benutzerdefinierten Aktionen {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.
>

## Übersicht

Mit **Funktion „Testanfrage senden** können Admins ihre benutzerdefinierten Aktionskonfigurationen überprüfen, indem sie echte API-Aufrufe direkt aus Adobe Journey Optimizer (AJO) durchführen. Mit dieser Funktion wird sichergestellt, dass Anfragestruktur, Kopfzeilen, Authentifizierung und Payload korrekt formatiert sind, bevor sie auf einer Journey verwendet werden.

![](assets/send-test-request.png){width="70%" align="left"}

## Voraussetzungen

- **Administratorzugriff erforderlich:**
   - Benutzende müssen über die Berechtigung **Verwalten von Journey-Ereignissen, Datenquellen und Aktionen“** verfügen.
   - Diese Berechtigung ist in der Rolle *Journey-Administratoren* enthalten.
   - Die Berechtigung **Journey-Ereignisse anzeigen…** allein reicht nicht aus.
- Eine **benutzerdefinierte Aktion** muss mit einer URL, Kopfzeilen und Authentifizierungseinstellungen vorkonfiguriert werden.

## Verwenden der Funktion „Testanfrage senden“

1. Navigieren Sie zum Konfigurationsbildschirm **Benutzerdefinierte Aktionen** .
1. Klicken Sie auf die Schaltfläche **Testanfrage senden**.
1. Ein Popup-Fenster wird angezeigt, in dem Sie Anforderungsparameter angeben können:
   - Wenn die **benutzerdefinierte Aktionsmethode GET** ist, ist keine Payload erforderlich.
   - Wenn die **benutzerdefinierte Aktionsmethode POST“ ist** müssen Sie eine JSON-Payload angeben.

     >[!NOTE]
     >
     >AJO löst einen Fehler aus, wenn die Struktur dieser JSON falsch ist, aber nicht, wenn sie nicht mit einem Datentyp übereinstimmt. Beispielsweise gibt es keinen Fehler, wenn ein ganzzahliger Parameter für eine Zeichenfolge verwendet wird.

   - Wenn die Authentifizierung definiert ist, werden Sie aufgefordert, Authentifizierungsdetails einzugeben.

1. Klicken Sie **Senden** um die Anfrage auszuführen.
1. Die Antwort der API, einschließlich Kopfzeilen und Status-Codes, wird in der Benutzeroberfläche angezeigt.

## Authentifizierungsverarbeitung

Wenn eine benutzerdefinierte Aktion die Authentifizierung enthält, verlangt AJO von den Benutzenden, dass sie Authentifizierungsdetails für jede Testanfrage eingeben:

- **Einfache Authentifizierung:** Der Benutzer muss das *Kennwort“*.
- **API-Schlüsselauthentifizierung:** Der Benutzer muss den API-Schlüssel (*)*.
- **Benutzerdefinierte Authentifizierung:** Der Benutzer muss die Authentifizierungsparameter in der Anfrage (bodyParam *angeben*. In diesem Fall werden zwei Abschnitte hinzugefügt: **Authentifizierungsanfrage** und **Authentifizierungsantwort**.

## Hauptunterschiede zu externen Test-Tools (z. B. Postman)

- Die Testanfrage wird von **AJO Journey** ausgeführt, was bedeutet:
   - Die exakte Anfragestruktur (einschließlich AJO-spezifischer Header) wird verwendet.
   - Die Quell-IP und -Kopfzeilen stimmen mit denen überein, die in Live-Journey verwendet werden.
- Kann zur Fehlerbehebung bei **Live-Journey** verwendet werden, bei denen die benutzerdefinierte Aktion bereits bereitgestellt ist.
- Vermeidet die Notwendigkeit, Konfigurationsdetails manuell zwischen Tools zu kopieren, wodurch das Fehlerrisiko reduziert wird.

## Fehlerbehebung

- Wenn die Anfrage fehlschlägt, überprüfen Sie:
   - Die im Test eingegebenen Authentifizierungsdaten.
   - Die Anfragemethode (GET vs. POST) und die entsprechende Payload.
   - Der API-Endpunkt und die Header, die in der benutzerdefinierten Aktion definiert sind.
- Verwenden Sie die Antwortdaten, um potenzielle Fehlkonfigurationen zu identifizieren.

Diese Funktion optimiert den Test- und Validierungsprozess und stellt sicher, dass benutzerdefinierte Aktionen in Live AJO-Journey ordnungsgemäß funktionieren.

