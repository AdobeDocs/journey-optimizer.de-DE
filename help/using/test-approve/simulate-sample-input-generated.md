---
solution: Journey Optimizer
product: journey optimizer
title: Automatische Generierung von Inhaltsvarianten (Beta)
description: Erfahren Sie, wie Sie mithilfe einer KI-basierten Simulation automatisch Inhaltsvarianten generieren.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Private Beta" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: 53d8fbb28e8516e4ee79f556a335b2d084af42e7
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---


# Automatische Generierung von Inhaltsvarianten (Beta){#auto-generate-variants}

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **privaten Betaversion** und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.

[!DNL Journey Optimizer] führt eine KI-basierte Simulation ein, mit der automatisch mehrere Varianten generiert werden können, um Ihren Inhalt zu testen. Diese Funktion reduziert die Notwendigkeit, Varianten manuell zu erstellen, was die Validierung der Personalisierungslogik in komplexen Vorlagen erleichtert.

Beim Rendern von Inhalten für die Simulation oder das Proofing analysiert das System Ihre Inhalte und identifiziert alle Personalisierungs-Token und Verzweigungsregeln. Es ersetzt Personalisierungs-Token durch aussagekräftige Werte, die eine nahezu realistische Vorschau des endgültigen Inhalts bieten.

Stellen Sie sich eine E-Mail-Vorlage für Finanzdienstleistungen mit Verzweigungslogik vor, die auf **Investorentyp**, **Altersgruppe**, **Familienstand**, **Steuer-ID-** und **Ort** basiert. Ohne Variantengenerierung müssten Sie Dutzende von Varianten manuell erstellen, um alle Pfade zu validieren. Mit automatisch generierten Varianten erzeugt das System repräsentative Varianten, die diese Bedingungen automatisch abdecken.  Jede generierte Variante wird im Vorschaubereich gerendert und zeigt genau an, welche Blöcke und Bedingungen angewendet werden.

## Inhaltsvarianten generieren

Gehen Sie wie folgt vor, um Varianten für Ihren Inhalt zu generieren und eine Vorschau anzuzeigen:

1. Öffnen Sie Ihren Inhalt und wählen Sie **[!UICONTROL Inhalt simulieren]** / **[!UICONTROL Inhaltsvarianten simulieren]**.

   ![](assets/simulate-sample.png)

2. Klicken Sie auf die **[!UICONTROL Generieren]**-Schaltfläche.

   ![](assets/simulate-generate-variant.png)

3. [!DNL Journey Optimizer] generiert basierend auf erkannten Attributen automatisch Varianten.

4. Überprüfen Sie die Liste der generierten Varianten im linken Bereich und wählen Sie eine Variante aus, um ihr personalisiertes Rendering im Vorschaubereich anzuzeigen.

>[!NOTE]
>
>Diese Funktion funktioniert auf die gleiche Weise wie die standardmäßige Funktion „Inhaltsvarianten simulieren“. Weitere Informationen zu Inhaltsvariantensimulationen und den zugehörigen Leitplanken und Einschränkungen finden Sie in diesem Abschnitt: [Inhaltsvarianten simulieren](../test-approve/simulate-sample-input.md)
