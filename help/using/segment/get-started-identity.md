---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Identitäten in Journey Optimizer
description: Erfahren Sie, wie Sie Identitäten in Adobe Journey Optimizer verwalten.
feature: Profiles
role: User
level: Beginner
exl-id: 90e892e9-33c2-4da5-be1d-496b42572897
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Erste Schritte mit Identitäten {#identities-gs}

Eine Identität sind Daten, die für eine Entität eindeutig sind, normalerweise für eine einzelne Person. Eine Identität wie z. B. eine Anmelde-ID, eine ECID oder eine Treueprogramm-ID wird als bekannte Identität bezeichnet.

Persönlich identifizierbare Informationen (PII) wie E-Mail-Adresse und Telefonnummer dienen zur direkten Identifizierung eines Kunden. Daher werden personenbezogene Daten verwendet, um die verschiedenen Identitäten eines Kunden systemübergreifend abzugleichen.

In [!DNL Adobe Journey Optimizer], **Identitäten** Verbraucher geräteübergreifend und kanalübergreifend zu verknüpfen, ergibt sich daraus ein [Identitätsdiagramm](#id-graph). Das verknüpfte Identitätsdiagramm wird verwendet, um Erlebnisse basierend auf Interaktionen über all Ihre geschäftlichen Touchpoints hinweg zu personalisieren.

![](assets/identities-home.png)

Weitere Informationen **Identity Service** in [diese Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html){target=&quot;_blank&quot;}.

## Identitäts-Namespaces {#identity-namespaces}

**Identitäts-Namespaces** sind eine Komponente von Identity Service , die als Indikatoren für den Kontext dient, auf den sich eine Identität bezieht. Sie unterscheiden beispielsweise den Wert von `name@email.com` als E-Mail-Adresse oder `443522` als numerische CRM-ID. Die Arbeit mit Identitäts-Namespaces setzt ein Verständnis der verschiedenen beteiligten Adobe Experience Platform-Dienste voraus. Bevor Sie mit Namespaces arbeiten, lesen Sie bitte die Dokumentation für die folgenden Dienste:

Weitere Informationen **Identitäts-Namespaces** in [diese Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}.

## Identitätsdiagramm{#id-graph}

Die **Identitätsdiagramm** ist eine Zusammenstellung der Beziehungen zwischen verschiedenen Identitäten für einen bestimmten Kunden und bietet Ihnen eine visuelle Darstellung, wie Ihr Kunde über verschiedene Kanäle mit Ihrer Marke interagiert. Alle Diagramme zur Kundenidentität werden vom Adobe Experience Platform Identity Service als Reaktion auf Kundenaktivitäten nahezu in Echtzeit verwaltet und aktualisiert.

Der Identitätsdiagramm-Viewer in [!DNL Adobe Journey Optimizer] Die Benutzeroberfläche ermöglicht es Ihnen, zu visualisieren und besser zu verstehen, welche Kundenidentitäten zusammengeführt werden und auf welche Weise. Mit dem Viewer können Sie verschiedene Teile des Diagramms ziehen und damit komplexe Identitätsbeziehungen untersuchen, effizienter debuggen und von erhöhter Transparenz bei der Verwendung von Informationen profitieren.

Weitere Informationen **Identitätsdiagramm** in [diese Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}.
