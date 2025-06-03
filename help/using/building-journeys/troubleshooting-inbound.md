---
solution: Journey Optimizer
product: journey optimizer
title: Handbuch zur Fehlerbehebung bei eingehenden Aktionen in Journey
description: Erfahren Sie, wie Sie Probleme im Zusammenhang mit eingehenden Aktionen in Journey Adobe Journey Optimizer debuggen und beheben.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Eingehende Aktionen, Fehlerbehebung, Journey, Debugging, Selbsthilfe, Überprüfen, Fehler
exl-id: 5c56786f-da22-4558-b2ae-01f762175a7f
source-git-commit: 3376b4336fa8bd2691b788995be94f153e9a44bb
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 1%

---

# Fehlerbehebung bei eingehenden Aktionen in Journey {#troubleshooting-inbound-actions}

Eingehende Aktionen wie In-App-, Web- und Code-basierte Erlebnisse sind wichtige Komponenten der [!DNL Journey Optimizer], da sie während des Journey eine personalisierte Interaktion mit Benutzenden ermöglichen. Es kann jedoch zu unerwartetem Verhalten kommen, z. B. fehlende eingehende Inhalte oder die Fortsetzung des Versands nach dem Verlassen des Journey durch ein Profil.

Dieses Handbuch enthält eine schrittweise Anleitung zum Debuggen von Problemen mit eingehenden Aktionen auf einer Journey, damit Sie diese unabhängig identifizieren und beheben können, bevor Sie sich an den Support wenden.

<!--This guide addresses the two most common scenarios with inbound actions in a journey. They are as follows:

* A profile enters the inbound step, but the user does not receive the expected inbound content.
* A user continues to receive inbound content even after the profile exits the journey.
-->

## Voraussetzungen {#prerequisites}

Bevor Sie mit der Fehlerbehebung beginnen können, stellen Sie Folgendes sicher:

1. Richten Sie eine **Assurance**-Sitzung ein. Weitere Informationen hierzu finden Sie in der Dokumentation zu [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

1. Navigieren Sie zu der Journey mit der eingehenden Aktion, um den Journey-Namen und die Versions-ID abzurufen.

   >[!NOTE]
   >
   >Die Journey-Versions-ID befindet sich in der URL nach &quot;Journey/&quot; (z. B.: *86232fb1-2932-4036-8198-55dfec606fd7*).

   ![](assets/troubleshoot-inbound-retrieve-journey-id.png)

1. Klicken Sie auf die eingehende Aktion, um deren Details anzuzeigen. Titel und ID der eingehenden Aktion abrufen.

   ![](assets/troubleshoot-inbound-retrieve-action-id.png)

1. Rufen Sie den Namespace und die ID des Profils ab, um Probleme im Profil zu identifizieren. Je nach Ihrer Konfiguration kann der Namespace beispielsweise ECID, E-Mail oder Kunden-ID sein. Wie Sie ein Profil suchen, erfahren Sie in der Dokumentation zu [Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/profile/ui/user-guide#browse-identity){target="_blank"}.

## Szenario 1: Der Benutzer hat den eingehenden Inhalt nicht erhalten {#scenario-1}

In diesem Szenario hat ein Profil die eingehende Aktion auf der Journey eingegeben, aber selbst nach 30 Minuten wird der entsprechende eingehende Inhalt auf dem Gerät/Client beim Setup-Trigger-Schritt nicht angezeigt.


### Vorab-Prüfungen {#pre-checks}

1. **Eingehender Journey-Datensatz ist für die Profilaufnahme aktiviert**

   Die eingehende Aktion verwendet den **Journey Inbound**-Datensatz für die Profilaktualisierungen während der Ausführung. Stellen Sie sicher, dass der Datensatz für Profile in der aktuellen Sandbox aktiviert ist. [Weitere Informationen zu Datensätzen](../data/get-started-datasets.md)

2. **in Platform-Identitäten definierte Identität &#39;Joai&#39;**

   Die eingehende Aktion verwendet den **joai**-Namespace im `segmentMembership`, um das Profil für den eingehenden Schritt zu aktivieren. Stellen Sie sicher, dass dies in Platform-Identitäten für die Sandbox definiert wurde. Weitere Informationen zu [Experience Platform Identity Service](https://experienceleague.adobe.com/de/docs/experience-platform/identity/home){target="_blank"}

### Debugging-Schritte {#debugging-steps}

Das folgende Diagramm zeigt die Abfolge der Debugging-Schritte, die Sie ausführen können:

![](assets/troubleshoot-inbound-scenario-1-steps.png){width="70%" align="center"}

### Schritt 1: Überprüfen, ob das Gerät/der Client den Inhalt von Edge Network erhält {#step-1}

Überprüfen Sie zunächst, ob das Gerät/der Client den erwarteten Inhalt erhält.

>[!BEGINTABS]

>[!TAB In-App-Kanal]

1. Wechseln Sie zur Sitzung [Assurance](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"} und wählen Sie im linken Bereich den **In-App-Nachrichten** aus.

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Nachrichten auf Gerät **[!UICONTROL auf die Dropdown-Liste]** Nachrichten“.

   ![](assets/troubleshoot-inbound-assurance-in-app.png){width="80%"}

1. Suchen Sie nach einer Nachricht mit dem Namen der Journey gefolgt von &quot;- In-App-Nachricht“. Falls vorhanden, bedeutet dies, dass die In-App-Nachricht auf dem Gerät/Client vorhanden ist und das Problem möglicherweise mit dem In-App-Trigger zusammenhängt.

1. Wenn die Nachricht nicht gefunden wurde, wurde die In-App-Nachricht nicht vom Gerät/Client empfangen. <!--Go to the [next step](#step-2) for further debugging.-->

>[!TAB Web-Kanal]

Besuchen Sie die Seite und überprüfen Sie die Registerkarte „Netzwerk“ oder überprüfen Sie die Edge-Antwort-Payload im Abschnitt **[!UICONTROL Edge Delivery]** der Sitzung [Assurance](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

>[!TAB Code-basierter Erlebniskanal]

Führen Sie mit der API von [Adobe eine cURL](https://developer.adobe.com/data-collection-apis/docs/api/)Anfrage durch und überprüfen Sie die Edge-Antwort-Payload im Abschnitt **[!UICONTROL Edge Delivery]** der Sitzung [Assurance](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

>[!ENDTABS]

### Schritt 2: Überprüfen, ob die Edge Network den Inhalt zurückgibt {#step-2}

In diesem Schritt wird sichergestellt, dass die Edge Network den erwarteten eingehenden Inhalt zurückgibt, der auf dem Gerät/Client gerendert werden soll.

Wenn ein Profil in eine eingehende Aktion auf einer Journey eintritt, wird es automatisch in ein spezielles Zielgruppensegment (im **joai**-Namespace) qualifiziert, das der eingehenden Journey-Aktion entspricht.

Wenn ein Client eine Anfrage an die Edge Network für ein bestimmtes Profil und eine bestimmte Oberfläche sendet, ist das Profil nur dann für den Empfang von Inhalten für die eingehenden Journey-Aktionen qualifiziert, die auf diese Oberfläche abzielen, wenn das Profil derzeit Mitglied des entsprechenden Segments **joai** ist.

Gehen Sie wie folgt vor, um das Verhalten von Edge Network zu debuggen.

1. Öffnen Sie die Ansicht **[!UICONTROL Edge Delivery]** in der Assurance-Sitzung. Diese Ansicht enthält Informationen über die Ausführung der eingehenden Aktion auf dem Edge Network-Server. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.

1. Überprüfen Sie, ob die Edge-Aktivität, die der eingehenden Aktion entspricht, in den Abschnitten **[!UICONTROL Qualifizierte Aktivitäten]** oder **[!UICONTROL Nicht qualifizierte Aktivitäten]** aufgeführt ist.

   ![](assets/troubleshoot-inbound-edge-delivery.png)

   * Wenn sich im **Qualifizierte Aktivitäten** das Profil für die eingehende Journey-Aktion qualifiziert hat, sollte der Inhalt zurückgegeben werden.
   * Wenn im Abschnitt **Nicht qualifizierte Aktivitäten** das Profil nicht für die eingehende Journey-Aktion qualifiziert war. Weitere Informationen finden Sie unter den Ausschlussgründen .
   * Wenn in **keinem Abschnitt** entweder ein Problem mit der Veröffentlichung der eingehenden Journey-Aktion in der Edge Network aufgetreten ist oder der angeforderte Oberflächen-URI nicht mit den Kanalkonfigurationseinstellungen für die eingehende Aktion übereinstimmt.

   >[!NOTE]
   >
   >Um Ihre Edge-Aktivität in der **Assurance**-Sitzung zu finden, suchen Sie nach der Aktivität, bei der **[!UICONTROL audienceNamespace]** **joai** lautet und die **[!UICONTROL audienceSegmentId]** &lt;*JourneyVersionID*>_&lt;*JourneyActionID*> lautet (Beispiel: *86232FB1-2932-4036-8198-55DFEC606FD7_708F718D-8503-4427-AD8D-8E28979B554C*).

   ![](assets/troubleshoot-inbound-edge-delivery-unqualified.png){width="70%"}

1. Wenn sich Ihre Aktivität im Abschnitt **[!UICONTROL Nicht qualifizierte Aktivitäten]** befindet und der Ausschlussgrund &quot;*Segment ist nicht aktiv“* ist, bedeutet dies, dass der Edge Network-Bereitstellungs-Server das Profil nicht für Teil des entsprechenden Zielgruppensegments **joai** hält.

   Sie können überprüfen, ob das **joai**-Segment in der Profilansicht des Edge Network-Versand-Servers vorhanden ist, indem Sie das **segmentsMap**-Element des Profilabschnitts öffnen und nach dem Vorhandensein der **joai**-Segment-ID suchen.

1. Wenn der Edge Network-Versandserver das Profil nicht als im entsprechenden **joai**-Segment ansieht, fahren Sie mit dem nächsten Schritt fort.<!--use the Platform Profile viewer UI to check if the expected **joai** segment is in a realized state in the Edge profile. Learn more in the [Experience Platform Profile UI documentation](https://experienceleague.adobe.com/de/docs/experience-platform/profile/ui/user-guide){target="_blank"}-->

### Schritt 3: Überprüfen, ob die Zielgruppenzugehörigkeit für „joai“ auf die Edge Network übertragen wurde {#step-3}

In diesem Schritt wird überprüft, ob das Edge-Profil korrekt aktualisiert wurde, als das Profil in die eingehende Journey-Aktion eintrat, und das Profil für das entsprechende **joai**-Segment qualifiziert wurde.

Wenn ein Profil in ein **joai**-Segment qualifiziert wird, wird das Profil zunächst im Hub aktualisiert und dann die Segmentzugehörigkeit an das Edge-Profil projiziert, damit es vom Edge Network-Bereitstellungsserver verwendet werden kann.

>[!NOTE]
>
>Die Übertragung vom Hub zu Edge kann bis zu 15-30 Minuten ab dem Zeitpunkt dauern, zu dem das Profil im Hub aktualisiert wird.

Edge Gehen Sie wie folgt vor, um im `segmentMembership` des **-Profils** Segment „joai zu überprüfen.

1. Navigieren Sie zum Menü **[!UICONTROL Kunde]** > **[!UICONTROL Profile]** im linken [!DNL Journey Optimizer] Navigationsbereich und navigieren Sie mithilfe des Namespace und der ID zum Profil. Weitere Informationen zu [Echtzeit-Kundenprofilen](../audience/get-started-profiles.md)

1. Wählen Sie die **[!UICONTROL Attribute]** und dann die Ansicht **[!UICONTROL Edge]** aus.

1. Klicken Sie **[!UICONTROL JSON anzeigen]**, um die JSON-Ansicht für das Profil zu öffnen.

   ![](assets/troubleshoot-inbound-profile-view-json.png){width="80%"}

1. Wechseln Sie zum `segmentMembership` Attribut und überprüfen Sie, ob die Segment-ID &lt;*JourneyVersionID>*_&lt;*JourneyActionID*> im Namespace **Joai** vorhanden ist und ob sie im **[!UICONTROL realized]**<!--or existing?--> ist.

   ![](assets/troubleshoot-inbound-profile-json-realized.png){width="90%"}

   * Wenn vorhanden, wurde **Segment &quot;**&quot;, das der eingehenden Journey-Aktion entspricht, korrekt an das Edge-Profil übertragen.

   * Wenn das Profil nicht in der Profilansicht des Edge Network-Versand-Servers angezeigt wird, kann ein Problem damit auftreten, wie der Versand-Server das Edge-Profil lädt.

1. Wenn die **joai**-Segment-ID nicht vorhanden ist oder sich im Status **[!UICONTROL beendet]** befindet, bedeutet dies, dass sie (noch) nicht an Edge weitergegeben wurde.

   Warten Sie 15 bis 30 Minuten, bis die `segmentMembership` Werte vom Hub an den Edge übertragen werden. Wenn noch nicht vorhanden, mit dem nächsten Schritt fortfahren.

<!--The next step is to check whether the audience segment is present in the profile on the Hub.-->

### Schritt 4: Überprüfen, ob im Profil im Hub die Zielgruppenzugehörigkeit „joai“ vorhanden ist. {#step-4}

In diesem Schritt wird überprüft, ob das Hub-Profil korrekt aktualisiert wurde, als das Profil in die eingehende Journey-Aktion eintrat, und das Profil für das entsprechende **joai**-Segment qualifiziert wurde.

>[!NOTE]
>
>Die Aufnahme der **joai**-Segmentzugehörigkeit in das Hub-Profil kann bis zu 15-30 Minuten ab dem Zeitpunkt dauern, zu dem das Profil in die eingehende Journey-Aktion eingetreten ist.

Gehen Sie wie folgt vor, um im `segmentMembership` des Hub **Profils nach dem Vorhandensein** Segments „joai zu suchen.

1. Navigieren Sie zum Menü **[!UICONTROL Kunde]** > **[!UICONTROL Profile]** im linken [!DNL Journey Optimizer] Navigationsbereich und navigieren Sie mithilfe des Namespace und der ID zum Profil. Weitere Informationen zu [Echtzeit-Kundenprofilen](../audience/get-started-profiles.md)

1. Wählen Sie die Registerkarte **[!UICONTROL Attribute]** und dann die Ansicht **[!UICONTROL Hub]** aus.

1. Klicken Sie **[!UICONTROL JSON anzeigen]**, um die JSON-Ansicht für das Profil zu öffnen.

1. Navigieren Sie zum **[!UICONTROL segmentMembership]**-Attribut und überprüfen Sie, ob die Segment-ID &lt;*JourneyVersionID>*_&lt;*JourneyActionID*> im Namespace **joai** vorhanden ist und ob sie in **[!UICONTROL realized]** <!--or existing?--> ist.

   * Wenn vorhanden, wurde **Segment &quot;**&quot;, das der eingehenden Journey-Aktion entspricht, korrekt in das Hub-Profil aufgenommen.

   * Wenn nach mindestens 30 Minuten nicht im Edge-Profil gefunden wird, kann ein Problem mit dem Edge-Projektionssystem vorliegen.

1. Wenn die **joai**-Segment-ID nicht vorhanden ist oder sich im **[!UICONTROL exited]**-Status befindet, bedeutet dies, dass das Profil beim Eintritt in die entsprechende eingehende Journey-Aktion (noch) nicht korrekt **dem speziellen joai**-Zielgruppensegment qualifiziert wurde.

   Warten Sie 15 bis 30 Minuten, bis die `segmentMembership` Werte in das Profil im Hub aufgenommen wurden. Wenn noch nicht vorhanden, mit dem nächsten Schritt fortfahren.

### Schritt 5: Wenn der Client/das Gerät immer noch nicht den erwarteten Inhalt erhält {#step-5}

Wenn Sie alle oben genannten Schritte durchlaufen haben und nach 30 bis 60 Minuten Wartezeit, bis die Segmentzugehörigkeit an Edge Network weitergegeben wird, das erwartete Verhalten nicht sehen, wenden Sie sich an die Adobe-Kundenunterstützung oder Ihren Adobe-Support-Mitarbeiter.

Fügen Sie so viele Details wie möglich aus den Debugging-Schritten hinzu, z. B.:

* der Schritt, in dem das unerwartete Verhalten angezeigt wird;
* die Journey-Versions-ID;
* die Journey-Aktions-ID;
* vollständige Assurance-Verfolgung;
* die JSON-Ansicht des Edge-Profils
* die JSON-Ansicht des Hub-Profils
* usw.

## Szenario 2: Der Benutzer erhält weiterhin den eingehenden Inhalt {#scenario-2}

Dieses Szenario ist das Gegenteil von [Szenario 1](#scenario-1): Das Profil hat die Journey verlassen, aber der Benutzer erhält weiterhin den eingehenden Inhalt.

Wenn ein Profil jedoch eine Journey verlässt, sollte es sich nicht mehr für die Zielgruppensegmente **joai** qualifizieren, die den eingehenden Aktionen auf der Journey entsprechen.

Führen Sie dieselben Debugging-Schritte wie für [Szenario 1](#debugging-steps) durch, um zu überprüfen, ob das Hub-Profil, das Edge-Profil und der Edge Network-Bereitstellungs-Server den Segmentzugehörigkeitsstatus des entsprechenden **joai**-Segments korrekt widerspiegeln und ob der Client den eingehenden Inhalt nicht mehr erhält.

<!--

## Reference Section {#reference-section}

- [Assurance Setup Guide](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/tutorials/using-assurance)
- [Adobe Experience Platform Documentation](https://experienceleague.adobe.com/docs/experience-platform/home.html)
- [Streaming Ingestion APIs Troubleshooting](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=de)

-->
