---
solution: Journey Optimizer
product: journey optimizer
title: URLs in E-Mails personalisieren
description: Erfahren Sie mehr über Best Practices und Einschränkungen für die dynamische Generierung von URLs bei gleichzeitiger Gewährleistung der Zuverlässigkeit des Trackings
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: URL, Link, Personalisierung, Tracking, Kodierung, geschweifte Klammern
source-git-commit: 36fad8d6c200118210794249fa12263ae70e5422
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 14%

---

# URLs in E-Mails personalisieren {#url-personalization}

Personalisierte URLs helfen Ihnen bei der Bereitstellung kontextueller Erlebnisse über Ihre [!DNL Journey Optimizer] E-Mail-Nachrichten, z. B. beim Generieren empfängerspezifischer Links oder beim Anhängen dynamischer Parameter.

Je nach den Profilattributen führen sie Empfänger zu bestimmten Seiten einer Website oder zu einer personalisierten Microsite.

## URL personalisieren {#personalize-url}

Gehen Sie wie folgt vor, um eine URL zu personalisieren.

1. Wählen Sie in der E-Mail-Designer ein Inhaltselement aus und [&#x200B; Sie mithilfe der kontextuellen Symbolleiste &#x200B;](message-tracking.md#insert-links)Link einfügen“.

   >[!IMPORTANT]
   >
   >Personalization ist nur für **[!UICONTROL Externer Link]**, **[!UICONTROL Abmelde-]** und **[!DNL Opt-Out]** verfügbar. Stellen Sie sicher, dass Sie einen geeigneten Link-Typ auswählen.

1. Wählen Sie das Personalisierungssymbol aus.

   ![](assets/message-tracking-insert-link-perso.png)

1. Verwenden Sie den Personalisierungseditor, um die Profilattribute hinzuzufügen, mit denen Sie die URL personalisieren möchten.

1. Speichern Sie Ihre Änderungen.

Im Folgenden finden Sie einige Beispiele für personalisierte URLs:

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!NOTE]
>
>Beim Bearbeiten einer personalisierten URL im Personalisierungseditor werden Hilfsfunktionen und die Zielgruppenzugehörigkeit aus Sicherheitsgründen deaktiviert.
>
>Leerzeichen werden in den Personalisierungs-Token, die in URLs verwendet werden, nicht unterstützt.

Befolgen Sie die [Best Practices und Leitplanken](#best-practices) unten, um ein zuverlässiges Rendering und Tracking zu gewährleisten.

## Vollständige/Basis-URL personalisieren {#personalize-complete-base-url}

Journey Optimizer unterstützt auch die Personalisierung **gesamten** URL oder der **Basis-Domain** einer URL, z. B.:

```html
<a href="{{profile.social.link}}" />
<a href="{{profile.social.baseUrl}}/profile" />
<a href="https://{{profile.social.baseUrl}}/profile" />
```

>[!IMPORTANT]
>
>Um die vollständige oder Basis-URL-Personalisierung zu aktivieren, wenden Sie sich an Adobe und geben Sie Ihre Liste der zulässigen Domains an. Dies ist erforderlich, um unsichere Weiterleitungen zu verhindern.

## URL-Tracking-Parameter personalisieren {#personalize-url-tracking-parameters}

[URL-Tracking](url-tracking.md) wird auf der Ebene der Kanalkonfiguration verwaltet und gilt für alle URLs, die im Nachrichteninhalt enthalten sind. Sie können auch URL-Tracking-Parameter für einen einzelnen Link in der E-Mail-Designer personalisieren. Auf diese Weise können Sie einen empfängerspezifischen Parameter an einen einzelnen Link anhängen (z. B. um eine Kennung an Ihre Web-Analyse-Tools zu übergeben).

Wählen Sie dazu [Link einfügen](message-tracking.md#insert-links), klicken Sie auf das Personalisierungssymbol, fügen Sie den URL-Tracking-Parameter hinzu und wählen Sie im Personalisierungseditor [&#x200B; gewünschte Profilattribut &#x200B;](../personalization/personalization-build-expressions.md).

![](assets/message-tracking-perso-parameter.png)

Wiederholen Sie die obigen Schritte für jeden Link, dem Sie diesen Tracking-Parameter hinzufügen möchten.

Wenn die E-Mail gesendet wird, wird dieser Parameter jetzt automatisch an das Ende der URL angehängt. Sie können diesen Parameter dann in Web-Analyse-Tools oder in Leistungsberichten erfassen.

>[!NOTE]
>
>Um die endgültige URL zu überprüfen, können Sie einen [Testversand durchführen](../content-management/proofs.md) und auf den Link im E-Mail-Inhalt klicken, sobald Sie die als Testversand vorgesehene Nachricht erhalten haben. Die URL sollte den Tracking-Parameter anzeigen. Beispiel: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>

## Best Practices und Leitplanken {#best-practices}

Um Links gültig, anklickbar und verfolgbar zu halten, befolgen Sie die folgenden Best Practices und Leitplanken.

### Geschweifte Klammern für dynamische URLs {#use-braces}

Verwenden Sie beim Einfügen einer URL, die Personalisierung enthält, drei geschweifte Klammern (`{{{ ... }}}`) für den dynamischen Teil der URL. Dadurch wird verhindert, dass Sonderzeichen (z. B. `/` und `+`) durch Escape-Zeichen geändert werden, und es werden fehlerhafte URLs, falsche Umleitungen oder Tracking-Probleme vermieden.

Siehe folgendes Beispiel:

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>Die Verwendung der Rohausgabe (`{{{ ... }}}`) bedeutet, dass der Wert unverändert eingefügt wird. Verwenden Sie sie nur mit Werten, denen Sie vertrauen und die URL-sicher sein sollen (z. B. Werte, die Sie Upstream generieren oder validieren).

### URL-Tracking korrigieren {#enable-url-tracking}

* Wenn Sie die URL mithilfe der Personalisierung generieren, stellen Sie sicher, dass der aufgelöste Wert für jede Empfängerin und jeden Empfänger mit `http`/`https` beginnt. Andernfalls wird das Tracking möglicherweise nicht angewendet und der Link verhält sich möglicherweise nicht wie erwartet.

* Verwenden Sie keine dynamische Logik wie `let`, `each` oder `if` Anweisungen direkt im URL-Feld des Personalisierungseditors. Diese sind aus Sicherheitsgründen deaktiviert.

* Wenn Ihr Szenario eine komplexe Logik zum Generieren personalisierter URLs umfasst, vermeiden Sie es, diese Logik direkt im URL-Feld des Personalisierungseditors zu platzieren. Stattdessen:
   * Fügen Sie die erforderliche Logik und die Anweisungen im HTML-Inhalt über oder in der Nähe des URL-Felds hinzu.
   * Personalisierte Attribute separat generieren und speichern und dann in Ihrem E-Mail-Inhalt darauf verweisen.

### URL-Codierung und -Länge {#encoding}

* URI-Syntaxregeln ([RFC 3986-Standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) gelten für alle URLs in Ihrem E-Mail-Inhalt. Bei personalisierten URLs treten jedoch mit höherer Wahrscheinlichkeit Kodierungsprobleme auf, da empfängerspezifische Werte reservierte Zeichen einführen können (z. B. in Abfrageparametern). Stellen Sie daher sicher, dass Ihre dynamischen Werte URL-kodiert sind (insbesondere Leerzeichen, `&`, `#`, `%` und `+`), und vermeiden Sie die Verwendung von `+` für Abfragewerte.

* Sehr lange URLs können von Browsern, Mail-Clients oder nachgelagerten Systemen abgeschnitten oder abgelehnt werden. Beispielsweise können die URLs von Mirrorseiten bei starker Laufzeitpersonalisierung erheblich zunehmen. Halten Sie personalisierte Payloads klein und vermeiden Sie das Einbetten großer Objekte in URLs.

### Empfohlene Validierungsschritte {#validation}

Bevor Sie eine Journey oder Kampagne aktivieren, befolgen Sie die folgenden Empfehlungen:

* Senden Sie einen [Testversand](../content-management/proofs.md) und klicken Sie auf Links, um zu bestätigen, dass die aufgelöste URL mit `http`/`https` beginnt und die erwartete Struktur beibehält.
* Wenn Tracking-Parameter angehängt werden, bestätigen Sie, dass die endgültige URL sie enthält (entweder über URL-Tracking auf Konfigurationsebene oder über Tracking-Parameter pro Link).

