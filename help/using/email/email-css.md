---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen von benutzerdefiniertem CSS zu Ihrem E-Mail-Inhalt
description: Erfahren Sie, wie Sie Ihrem E-Mail-Inhalt direkt in der E-Mail-Designer in Journey Optimizer benutzerdefiniertes CSS hinzufügen.
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: CSS, Editor, Zusammenfassung, E-Mail
source-git-commit: feb3576c230f2fb28ab031f87cc5f99263329b57
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# Hinzufügen von Metadaten zu E-Mail-Inhalten {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="Benutzerdefiniertes CSS hinzufügen"
>abstract="xxx."

Beim Entwerfen Ihrer E-Mails können Sie Ihr eigenes benutzerdefiniertes CSS direkt in der [!DNL Journey Optimizer]E-[-Designer](get-started-email-design.md) hinzufügen.

Was im Textbereich Benutzerdefiniertes CSS hinzufügen erwartet wird, ist eine gültige CSS-Zeichenfolge.

![](assets/email-body-css.png)

Verfügbarkeitsbedingungen

Die Funktion Benutzerdefiniertes CSS hinzufügen ist nur verfügbar, wenn im Editor ein Inhalt definiert ist. Um den Abschnitt Benutzerdefiniertes CSS hinzufügen anzuzeigen, muss der Benutzer Inhalte im Editor hinzufügen. Wenn der/die Benutzende den gesamten Inhalt entfernt, wird der Abschnitt ausgeblendet und das benutzerdefinierte CSS wird nicht angewendet. Wenn der/die Benutzende Inhalte wieder hinzufügt, ist der Abschnitt verfügbar und das benutzerdefinierte CSS wird angewendet.

**Beispiele für ungültige CSS-Eingaben**

Ungültiges CSS kann nicht gespeichert werden. Wenn das CSS ungültig ist, wird ein rotes Popup angezeigt, das anzeigt, dass das CSS nicht gespeichert werden konnte.

`<style>` wird nicht akzeptiert


```
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```


Fehlende Klammer ist ungültig

```
body {
 background: red; 
```
