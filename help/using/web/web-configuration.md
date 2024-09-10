---
title: Konfiguration von Web-Kanälen
description: Erstellen einer Web-Kanalkonfiguration
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 2161baf0-38b7-4397-bffe-083929e8033a
source-git-commit: 37e60e5d7c0ad164cde67015b72341e1f4eda6a9
workflow-type: ht
source-wordcount: '855'
ht-degree: 100%

---

# Erstellen einer Web-Kanalkonfiguration {#web-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="Regel zum Seitenabgleich"
>abstract="Erstellen Sie eine Regel zum Seitenabgleich, um eine Gruppe von URLs, die dieselben Kriterien aufweisen, effizient zu verwalten und als Ziel festzulegen. Mit dieser Regel können Sie mehrere URLs unter einer Richtlinie zusammenfassen, wodurch die Anwendung konsistenter Einstellungen und Aktionen auf diesen Seiten vereinfacht wird."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="Standard-Authoring- und Vorschau-URL"
>abstract="Dieses Feld stellt sicher, dass die von der Regel generierten oder abgeglichenen Seiten über eine bestimmte URL verfügen, die sowohl für die effektive Erstellung als auch Vorschau von Inhalten erforderlich ist."

Eine Web-Konfiguration ist eine Web-Eigenschaft, die durch eine URL identifiziert wird, über die die Inhalte bereitgestellt werden. Sie kann einer einzelnen Seiten-URL oder mehreren Seiten entsprechen, sodass Sie Änderungen auf einer oder mehreren Web-Seiten vornehmen können.

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL Kanalkonfigurationen]** auf, und klicken Sie dann auf **[!UICONTROL Kanalkonfiguration erstellen]**.

   ![](assets/web_config_1.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Konfiguration an.

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Um der Konfiguration benutzerdefinierte oder grundlegende Datennutzungskennzeichnungen zuzuweisen, können Sie **[!UICONTROL Zugriff verwalten]** auswählen. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Wählen Sie den **Web**-Kanal aus.

   ![](assets/web_config_2.png)

1. Wählen Sie eine **[!UICONTROL Marketing-Aktion]** aus, um Einverständnisrichtlinien mit den Nachrichten zu verknüpfen, die diese Konfiguration verwenden. Es werden alle mit dieser Marketing-Aktion verknüpften Einverständnisrichtlinien genutzt, um die Voreinstellungen Ihrer Kundinnen und Kunden zu respektieren. [Weitere Informationen](../action/consent.md#surface-marketing-actions)

1. Wenn Sie die Änderungen nur auf eine einzelne Seite anwenden möchten, können Sie eine **[!UICONTROL Seiten-URL]** eingeben.

1. Sie können aber auch eine **[!UICONTROL Matching-Regel für Seiten]** festlegen, um mehrere URLs als Ziel auszuwählen, die derselben Regel entsprechen. Dies ist zum Beispiel sinnvoll, wenn Sie die Änderungen auf ein Hero-Banner auf einer ganzen Website anwenden oder oben ein Bild hinzufügen möchten, das auf allen Produktseiten einer Web-Site angezeigt wird.

   Wählen Sie dazu **[!UICONTROL Regel zum Seitenabgleich]** aus.

1. Definieren Sie Ihre Kriterien für die Felder **[!UICONTROL Domain]** und **[!UICONTROL Seite]**.

   Wenn Sie beispielsweise Elemente bearbeiten möchten, die auf allen Damenproduktseiten Ihrer Luma-Website angezeigt werden, wählen Sie **[!UICONTROL Domain]** > **[!UICONTROL Beginnt mit]** > `luma` und **[!UICONTROL Seite]** > **[!UICONTROL Enthält]** > `women`.

   ![](assets/web_config_3.png)

1. Wenn Sie eine **[!UICONTROL Regel zum Seitenabgleich]** erstellt haben, müssen Sie die **Standard**-Authoring- und Vorschau-URL eingeben. Dieser Schritt stellt sicher, dass die von der Regel generierten oder abgeglichenen Seiten über eine bestimmte URL für die Erstellung und Vorschau von Inhalten verfügen. Weitere Informationen zur Regel zum Seitenabgleich finden Sie im [folgenden Abschnitt](#web-page-matching-rule).

1. Speichern Sie Ihre Änderungen.

Sie können Ihre Konfiguration jetzt beim Verwenden des Web-Kanals in Kampagnen oder Journeys auswählen.

## Regel zum Seitenabgleich {#web-page-matching-rule}

Beim Erstellen einer Regel, die mehrere Seiten abgleicht, sodass Sie dieselben Inhaltsänderungen auf mehreren Seiten gleichzeitig anwenden können, können Sie verschiedene Operatoren in den Abschnitten **Domain** und **Pfad** verwenden, um die gewünschte Regel zu erstellen. Sehen Sie sich die unten aufgeführten, verfügbaren Operatoren an.

Verfügbare Operatoren zum Erstellen von Regeln zum Seitenabgleich:

* **Domain**

  | Operator  | Beschreibung  | Beispiele  |
  |---|---|---|
  | Gleich  | Exakte Übereinstimmung mit der Domain.  |
  | Beginnt mit  | Gleicht alle Domains (einschließlich Subdomains) ab, die mit der eingegebenen Zeichenfolge beginnen.  | Beispiel: „Beginnt mit: dev“-> gleicht alle Domains und Subdomains ab, die mit „dev“ beginnen, wie: dev.example.com, dev.products.example.com, developer.example.com  |
  | Endet mit  | Gleicht alle Domains ab (einschließlich Subdomains), die mit der eingegebenen Zeichenfolge enden.   | Beispiel: „Endet mit: example.com“-> gleicht alle Domains und Subdomains ab, die mit „example.com“ enden, wie: stage.example.com, prod.example.com, myexample.com  |
  | Platzhalterabgleich  | Mit dem Operator „Platzhalterabgleich“ können Benutzende einen Platzhalterabgleich in der Mitte der Zeichenfolge definieren, z. B. „dev.*.example.com“. Die Validierungsregeln bestehen darin, dass der Wert einen und nur einen Platzhalter (Sternchen) enthalten darf, wenn der Operator „Platzhalterabgleich“ ist.  | Beispiel: „Platzhalterabgleich: dev.*.example.com“ -> gleicht Domains wie: dev.products.example.com, dev.mytest.products.example.com und dev.blog.example.com ab.  |
  | Beliebige  | Gleicht alle Domains ab: nützlich beim Domain-übergreifenden Testen eines bestimmten Pfads  |


* **Pfad**

<table>
    <thead>
    <tr>
        <th><strong>Operator</th>
        <th><strong>Beschreibung</th>
        <th><strong>Beispiele</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>Gleich</td>
        <td>Exakte Übereinstimmung mit dem Pfad. </td>
        <td></td>
    </tr>
    <tr>
        <td>Beginnt mit</td>
        <td>Gleicht alle Pfade (einschließlich Nebenpfaden) ab, die mit der eingegebenen Zeichenfolge beginnen.</td>
        <td></td>
    </tr>
    <tr>
        <td>Endet mit</td>
        <td>Gleicht alle Pfade (einschließlich Nebenpfaden) ab, die mit der eingegebenen Zeichenfolge enden.</td>
        <td></td>
    </tr>
    <tr>
        <td>Beliebig</td>
        <td>Gleicht alle Pfade ab: nützlich beim Targeting aller Pfade unter einer oder mehreren Domains.</td>
        <td></td>
    </tr>
    <tr>
        <td>Platzhalterabgleich</td>
        <td>Mit dem Operator „Platzhalterabgleich“ können Benutzende einen internen Platzhalterabgleich im Pfad definieren, z. B. „/products/*/detail“.  Das Platzhalterzeichen * in der Komponente Pfad ** gleicht alle Zeichenfolgen ab, bis das erste /-Zeichen gefunden wird.  /*/ gleicht alle Zeichenfolgen ab (einschließlich Nebenpfaden) </td>
        <td>Beispiel: „Wildcard matching: /products/*/detail“, gleicht alle Pfade ab, wie: <ul><li>example.com/products/yoga/detail</li><li>example.com/products/surf/detail</li><li>example.com/products/tennis/detail</li><li>example.com/products/yoga/pants/detail</li></ul>Beispiel: „Matches: /prod*/detail, stimmt mit allen Pfaden überein, wie: <ul><li>example.com/products/detail</li><li>example.com/production/detail</li></ul>Gleicht keine Pfade ab wie: <ul><li>example.com/products/yoga/detail</li></ul></td>
    </tr>
    <tr>
        <td>Enthält</td>
        <td>„Enthält“ wird in einen Platzhalter wie „mystring“ übersetzt und gleicht alle Pfade ab, die diese Zeichenfolge enthalten.</td>
        <td>Beispiel: „Contains: product“ gleicht alle Pfade ab, die das Zeichenfolgenprodukt enthalten, z. B.: <ul><li>example.com/products</li><li>example.com/yoga/perfproduct</li><li>example.com/surf/productdescription</li><li>example.com/home/product/page</li></ul></td>
    </tr>
    </tbody>
</table>

Wenn Ihr Anwendungsfall nicht mit einer Regel modelliert werden kann, können Sie mehrere Seitenregeln hinzufügen und die Operatoren „Oder“ oder „Ausschließen“ verwenden. „Ausschließen“ ist nützlich, wenn eine der Seiten, die mit der definierten Regel übereinstimmen, nicht als Ziel ausgewählt werden sollte, z. B. alle „example.com“-Seiten, die „product“ enthalten, mit Ausnahme der folgenden Seite: `https://example.com/blogs/productinfo`.
