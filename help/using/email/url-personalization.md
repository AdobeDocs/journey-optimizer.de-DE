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
source-git-commit: daf07abd855079aeedf77708575a92d1ce13f66d
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 24%

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


<!--
## Best practices and guardrails {#best-practices}

To keep links valid, clickable, and trackable, follow the best practices and guardrails below.

### Braces for dynamic URLs {#use-braces}

When inserting a URL that contains personalization, use three curly braces (`{{{ ... }}}`) for the dynamic portion of the URL. This prevents escaping from altering special characters (for example `/` and `+`) and helps avoid broken URLs, incorrect redirects, or tracking issues.

Here is an example:

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>Using raw output (`{{{ ... }}}`) means the value is inserted as-is. Only use it with values you trust and that are intended to be URL-safe (for example, values you generate or validate upstream).

### Correct URL tracking {#enable-url-tracking}

* When using personalization to generate the URL, ensure the resolved value starts with `http`/`https` for every recipient. Otherwise, tracking may not be applied and the link may not behave as expected.

* Do not use dynamic logic such as `let`, `each`, or `if` statements directly in the personalization editor's URL field. These are disabled for security reasons.

* If your scenario involves complex logic to generate personalized URLs, avoid placing that logic directly in the personalization editor's URL field. Instead:
    * Add the necessary logic and statements in the HTML content above or near the URL field.
    * Generate and store personalized attributes separately, then reference them in your email content.

### URL encoding and length {#encoding}

* URI syntax rules ([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) apply to all URLs in your email content. However, personalized URLs are more likely to surface encoding issues because recipient-specific values can introduce reserved characters (for example in query parameters). Therefore, ensure your dynamic values are URL-encoded (especially spaces, `&`, `#`, `%`, and `+`) and avoid using `+` for query values.

* Very long URLs can be truncated or rejected by browsers, mail clients, or downstream systems. For example, mirror page URLs can grow significantly when runtime personalization is heavy. Keep personalized payloads small and avoid embedding large objects into URLs.

### Recommended validation steps {#validation}

Before activating a journey or campaign, follow the recommendations below:

* Send a [proof](../content-management/proofs.md) and click links to confirm the resolved URL starts with `http`/`https` and keeps the expected structure.
* If tracking parameters are appended, confirm the final URL includes them (either via configuration-level URL tracking or per-link tracking parameters).
-->
