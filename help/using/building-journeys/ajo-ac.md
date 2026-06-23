---
solution: Journey Optimizer
product: journey optimizer
title: Senden einer Nachricht mit Campaign v7/v8
description: Erfahren Sie, wie Sie mit Campaign v7/v8 eine Nachricht senden.
feature: Journeys, Integrations, Custom Actions, Use Cases
topic: Administration
role: Admin, Developer, User
level: Intermediate, Experienced
keywords: Journey, Nachricht, Kampagne, Integration
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/btOUMO8tgvwLD7kjVdgpj6I6QXRrj1iTD3P8AUrqJFM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: d08afb72-92f6-4856-88e3-11ec34313c2f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1025
ht-degree: 39%

---

# Senden einer Nachricht mit Campaign v7/v8 {#campaign-v7-v8-use-case}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine E-Mail von einer Journey mithilfe der Integration mit Adobe Campaign v7 und v8 senden, einschließlich der Erstellung der Transaktionsvorlage, des Ereignisses und der Aktion.

>[!ENDSHADEBOX]

In diesem Anwendungsbeispiel werden alle Schritte erläutert, die zum Senden einer E-Mail mithilfe der Integration mit [!DNL Adobe Campaign] v7 und [!DNL Adobe Campaign] v8 erforderlich sind.

>[!NOTE]
>
>Um diese Integration verwenden zu können, benötigen Sie Campaign v7/v8 Build 9125 oder höher.

Erstellen Sie zunächst eine Transaktions-E-Mail-Vorlage in Campaign. Erstellen Sie anschließend in Journey Optimizer das Ereignis, die Aktion und die Journey.

Weiterführende Informationen zur Campaign-Integration finden Sie auf diesen Seiten:

* [Erstellen einer Campaign-Aktion](../action/acc-action.md)
* [Verwenden der Aktion in einer Journey](../building-journeys/using-adobe-campaign-v7-v8.md).

**[!DNL Adobe Campaign]**

Die Campaign-Instanz muss für diese Integration bereitgestellt werden. Die Funktion für Transaktionsnachrichten muss konfiguriert sein.

1. Melden Sie sich bei Ihrer Campaign-Kontrollinstanz an.

1. Wählen Sie unter **Administration** > **Platform** > **Aufzählungen** die Aufzählung **Ereignistyp** (eventType) aus. Erstellen Sie einen neuen Ereignistyp (in unserem Beispiel „Journey-Ereignis“). Verwenden Sie später beim Schreiben der JSON-Datei den internen Name des Ereignistyps.

   ![Konfigurieren eines Ereignisses in [!DNL Adobe Journey Optimizer] mit Schema- und Feldauswahl](assets/accintegration-uc-1.png)

1. Trennen Sie die Verbindung zur Instanz und stellen Sie sie erneut her, damit die Erstellung wirksam wird.

1. Erstellen Sie unter **Message Center** > **Transaktionsnachrichten-Vorlagen** eine neue E-Mail-Vorlage basierend auf dem zuvor erstellten Ereignistyp.

   ![Ereigniskonfiguration mit Einstellungen für Namespace und Profilkennungen](assets/accintegration-uc-2.png)

1. Gestalten Sie Ihre Vorlage. In diesem Beispiel wird eine Personalisierung auf den Vornamen und die Bestellnummer des Profils angewendet. Der Vorname befindet sich in der [!DNL Adobe Experience Platform] Datenquelle und die Bestellnummer ist ein Feld aus dem Journey Optimizer-Ereignis. Stellen Sie sicher, dass Sie die richtigen Feldnamen in Campaign verwenden.

   ![Vorschau der Ereignis-Payload mit JSON-Struktur mit Profil- und Ereignisdaten](assets/accintegration-uc-3.png)

1. Veröffentlichen Sie Ihre Transaktionsnachrichtenvorlage.

   ![Schaltfläche „Ereigniskopie“ zum Kopieren der Payload-ID für die API-Integration](assets/accintegration-uc-4.png)

1. Die JSON-Payload muss entsprechend der Vorlage geschrieben werden.

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* Beim Kanal geben Sie „E-Mail“ ein.
* Verwenden Sie für eventType den internen Namen des zuvor erstellten Ereignistyps.
* Die E-Mail-Adresse ist eine Variable, sodass Sie ein beliebiges Label eingeben können.
* Unter ctx sind die Personalisierungsfelder auch Variablen.

**Journey Optimizer**

1. Erstellen Sie ein Ereignis. Schließen Sie das Feld „purchaseOrderNumber“ ein.

   ![Konfigurationsbildschirm für benutzerdefinierte Aktionen für die [!DNL Adobe Campaign] Classic-Integration](assets/accintegration-uc-5.png)

1. Erstellen Sie eine Aktion in Journey Optimizer, die der Kampagnenvorlage entspricht. Wählen **in der Dropdown** Liste „Aktionstyp“ **[!DNL Adobe Campaign]Classic**.

   ![Auswahl des Aktionstyps mit [!DNL Adobe Campaign] Option Classic](assets/accintegration-uc-6.png)

1. Klicken Sie auf das Feld **Payload** und fügen Sie die zuvor erstellte JSON-Datei ein.

   ![Dropdown-Liste zur Auswahl des Campaign-Kontos für die Integration von Aktionen](assets/accintegration-uc-7.png)

1. Ändern Sie für die E-Mail-Adresse und die beiden Personalisierungsfelder **Konstante** in **Variable**.

   ![Konfiguration der Aktions-Payload mit Feldzuordnung für die Campaign-Integration](assets/accintegration-uc-8.png)

1. Erstellen Sie nun eine neue Journey und beginnen Sie mit dem zuvor erstellten Ereignis.

   ![Journey-Arbeitsfläche mit konfiguriertem Ereignis und konfigurierter Campaign-Aktion](assets/accintegration-uc-9.png)

1. Fügen Sie die Aktion hinzu und ordnen Sie jedes Feld dem richtigen Feld in Journey Optimizer zu.

   ![Zuordnung von Aktionsparametern mit dem Ausdruckseditor für dynamische Werte](assets/accintegration-uc-10.png)

1. Testen Sie Ihre Journey.

   ![Vollständiger Journey-Fluss mit Ausführung von Ereignis-Trigger und Campaign-Aktion](assets/accintegration-uc-11.png)

1. Sie können Ihre Journey jetzt veröffentlichen.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite finden Sie eine schrittweise Anleitung zum Senden einer Transaktions-E-Mail von Adobe Journey Optimizer mithilfe der Integration mit Adobe Campaign v7/v8. Hier werden die Erstellung von Kampagnenvorlagen, die Konfiguration von Ereignissen und Aktionen und das Journey-Design behandelt.

**intents:**
* Konfigurieren einer Transaktions-E-Mail-Vorlage in Adobe Campaign v7/v8 zur Verwendung mit Journey Optimizer
* Erstellen eines Ereignisses in Journey Optimizer, das benutzerdefinierte Felder wie eine Bestellnummer enthält
* Erstellen und Konfigurieren einer Campaign Classic-Aktion in Journey Optimizer mit einer JSON-Payload
* Zuordnen von Journey-Ereignisfeldern zu Campaign-Personalisierungsvariablen in der Aktionskonfiguration
* Erstellen und veröffentlichen Sie eine Journey, die eine Transaktions-E-Mail in Campaign Trigger

**Glossar:**
* **Transaktionsnachrichten**: Eine Campaign-Funktion, die ausgelöste E-Mails in Echtzeit sendet, die auf Ereignissen basieren. Muss konfiguriert werden, bevor diese Integration verwendet werden kann *(produktspezifisch)*
* **Ereignistyp (eventType)** Ein in Campaign definierter Auflistungswert, der den Typ des Transaktionsereignisses identifiziert; sein interner Name wird in der JSON-Payload-*referenziert (produktspezifisch)*
* **Campaign Classic-Aktion**: Ein Journey Optimizer-Aktionstyp, der eine Verbindung zu Adobe Campaign v7/v8 herstellt, um Transaktionsnachrichten zu senden *(produktspezifisch)*
* **Payload-Feld**: Die JSON-Struktur, die in eine Journey Optimizer-Aktion eingefügt wird und die an Campaign gesendeten Datenfelder definiert *(produktspezifisch)*

**Leitplanken:**
* Campaign v7/v8 Build 9125 oder höher ist für diese Integration erforderlich
* Die Transaktionsnachrichten-Funktion muss vor der Verwendung in der Campaign-Instanz konfiguriert werden
* Nachdem Sie einen neuen Ereignistyp in Campaign erstellt haben, müssen Sie die Verbindung zur Instanz trennen und erneut herstellen, damit sie wirksam wird
* Personalization-Feldwerte, die in der Aktion als „Konstante“ festgelegt sind, müssen in „Variable“ geändert werden, um eine dynamische Population zur Laufzeit zu ermöglichen

**Terminologie:**
* Kanonischer Name: Adobe Campaign v7/v8 — Akronym: ACC — Varianten: Campaign Classic, Campaign v7, Campaign v8
* Synonyme: „eventType“ = „Interner Name des Ereignistyps“
* Verwechseln Sie nicht: &quot;Campaign Classic-Aktion“ ≠ „benutzerdefinierte Aktion“ (Campaign Classic-Aktion ist ein bestimmter integrierter Aktionstyp für die ACC-Integration)

**FAQ:**
* **F: Welche Campaign-Version ist für diese Integration erforderlich?** — Campaign v7/v8 Build 9125 oder höher ist erforderlich.
* **F: Was muss in Campaign konfiguriert werden, bevor Sie beginnen?** — Die Transaktionsnachrichten-Funktion muss konfiguriert und eine Transaktions-E-Mail-Vorlage muss auf Grundlage des Ereignistyps erstellt werden.
* **F: Wie mache ich Personalisierungsfelder im Journey Optimizer-Modus dynamisch?** — Ändern Sie in der Konfiguration der Aktions-Payload die Feldkonfiguration für Felder, die zur Laufzeit ausgefüllt werden, von „konstant“ in „variabel“.
* **F: Woher kommen in diesem Anwendungsfall die Personalisierungsdaten für den Vornamen?** - Der Vorname stammt aus der Adobe Experience Platform-Datenquelle, während die Bestellnummer von der Journey Optimizer-Ereignis-Payload stammt.
* **F: Wie kann ich die Journey Optimizer-Aktion mit der Kampagnenvorlage verbinden?** — Wählen Sie als Aktionstyp &quot;Adobe Campaign Classic&quot; aus und fügen Sie dann die JSON-Payload ein, die der Struktur der Transaktionsnachrichten-Vorlage entspricht.

+++
