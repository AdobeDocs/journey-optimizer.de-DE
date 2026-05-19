---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden und Konfigurieren von Deeplinks in E-Mail- und SMS-Nachrichten
description: Erfahren Sie, wie Sie E-Mail- und SMS-Inhalten Deeplinks hinzufügen und wie Sie die Deeplink-Handhabung in iOS- und Android-Apps implementieren.
feature: Email, SMS
topic: Content Management
role: User, Developer
level: Intermediate
keywords: Deeplink, Deep-Link, universelle Links, App-Links, E-Mail, SMS
source-git-commit: 3d3218e24074ffb8ec36f1ec14ff8a6c45950d90
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 1%

---


# Verwenden und Konfigurieren von Deeplinks in E-Mails und SMS {#deeplinks}

Mit Deeplinks können Sie Empfänger von einer E-Mail oder SMS-Nachricht zu einem bestimmten Bildschirm oder Inhalt in Ihrer Mobile App weiterleiten. Dadurch können Benutzer direkt zum gewünschten In-App-Erlebnis gelangen, ohne sie über einen Webbrowser oder einen App Store weiterzuleiten, sodass der Journey relevant und markenintern bleibt.

Wenn Ihre Empfänger auf den Deeplink klicken, werden sie direkt zum gewünschten In-App-Inhalt weitergeleitet - **vorausgesetzt, Sie haben Folgendes abgeschlossen**:

* die [Konfigurationsschritte](#configuration) in Journey Optimizer;

* Die [Implementierung von Mobile ](#mobile-implementation)) für iOS und Android in Ihrer Mobile App.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer] unterstützt Deeplinking für iOS und Android mithilfe von getrackten URLs (`/ee/v1/mclick/*`), um Kompatibilität und Klick-Tracking sicherzustellen.

## Erstellen von Deeplinks {#authoring}

### E-Mail {#authoring-email}

Für E-Mail-Nachrichten haben Sie zwei Möglichkeiten, einen Deeplink einzufügen:

* **E-Mail an Designer**: Stellen Sie sicher[ dass das Linktracking aktiviert ](message-tracking.md#enable-tracking). Wählen Sie das Element aus, das Sie verknüpfen möchten (Text, Schaltfläche oder Bild), klicken Sie **[!UICONTROL Link einfügen]** in der kontextuellen Symbolleiste und wählen Sie **[!UICONTROL Deeplink]** aus, um Ihre Deeplink-URL einzugeben. [Weitere Informationen zum Einfügen von Links](message-tracking.md#insert-links)

* **Personalization-Editor (Code)**: Fügen Sie den Deeplink mithilfe des folgenden Snippets direkt in HTML ein:

  ```html
  <a class="arc-link" data-nl-type="DEEPLINK" href="<<deeplink_url>>" id="acr-link-7821368" style="text-decoration:underline;" target="_blank" data-tracking-type="DEEPLINK">Click Here</a>
  ```

  Ersetzen Sie `<<deeplink_url>>` durch Ihre tatsächliche Deeplink-URL und verwenden Sie eine eindeutige `id` für jeden Block, um Konflikte zu vermeiden.

### SMS {#authoring-sms}

Für SMS werden Deeplinks mit der Hilfsfunktion **URL** im Personalisierungseditor erstellt. Weitere Informationen zum Hinzufügen von Links zu SMS-Inhalten finden Sie [ diesem Abschnitt](../sms/create-sms.md#sms-content).

Verwenden Sie die folgende Syntax, um Deeplinks in SMS-Inhalte einzufügen:

```
{{url originalUrl='<<url>>' type='DEEPLINK' action='CLICK'}}
```

Ersetzen Sie `<<url>>` durch Ihre tatsächliche Deeplink-URL.

## Konfiguration in Journey Optimizer {#configuration}

Um Deeplinks in E-Mails und SMS für Ihre Mobile Apps verwenden zu können, führen Sie die folgenden Konfigurationsschritte aus.

>[!NOTE]
>
>Dieser Abschnitt gilt für die Verwendung **universellen Links (iOS)** und **App-Links (Android)** (HTTPS-basierte Deeplinks).

1. Delegieren Sie in Journey Optimizer die Subdomain, für die die Deeplinking-Funktion aktiviert ist. [Weitere Informationen](../configuration/delegate-subdomain.md)

1. Hosten Sie die AASA-Datei für iOS und die assetLinks.json-Datei für Android in Ihrer Subdomain. Wenden Sie sich mit den folgenden Informationen an die ](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"}-Kundenunterstützung von [Adobe oder Ihren Adobe-Support-Mitarbeiter:

   * **Für iOS (AASA)**:
      * Delegierte Subdomain
      * App-Bundle-ID
   * **Für Android (assetLinks.json)**:
      * Delegierte Subdomain
      * App-Bundle-ID
      * SHA-256-Zertifikat-Fingerabdruck

>[!IMPORTANT]
>
>Deeplinking über die Adobe-Infrastruktur gilt, wenn das Linktracking für Ihre Nachricht in den E[Mail-Tracking-Einstellungen ](message-tracking.md#enable-tracking) im Abschnitt **[!UICONTROL Aktionstracking]** für SMS-Kampagnen aktiviert ist. Getrackte Deeplink-Klicks verwenden URLs unter `/ee/v1/mclick/*`, die von Adobe gehostet und aufgelöst werden.
>
>Bei **nicht getrackten** Links wird die URL nicht über Adobe-Systeme neu geschrieben. Sie müssen universelle Links oder App-Links auf Ihren eigenen Domains und beim Hosting konfigurieren, damit diese Links Ihre App wie vorgesehen öffnen.

## Mobile-App-Implementierung {#mobile-implementation}

In diesem Abschnitt wird erläutert, wie Sie mobile Deeplinks mit [!DNL Adobe Journey Optimizer] implementieren, sodass in einem typischen **HTTPS**-Setup (universelle Links und App-Links) eine einzelne URL:

* einen bestimmten Bildschirm in der App öffnen, wenn die App installiert ist, oder
* Öffnen Sie Ihre Website als Fallback, wenn die App nicht installiert ist.

Wenn das Linktracking für Ihre Nachricht aktiviert ist, verfolgt [!DNL Journey Optimizer] diese Klicks weiterhin, bezieht sie in das Reporting ein und kann sie in [Inhaltsexperimenten“ verwenden](../content-management/content-experiment.md) wenn Sie sie für die Nachricht ausführen.

In diesem Abschnitt finden Sie allgemeine Implementierungsmuster für Deeplinks. Die genaue Einrichtung hängt von Ihrer App-Architektur und dem Routing-Framework ab.

### iOS (Universelle Links) {#ios-implementation}

1. Wählen Sie in Xcode Ihr Ziel über **[!UICONTROL Signing &amp; Capabilities]** > **[!UICONTROL + Capability]** > **[!UICONTROL Associated Domains]** aus.
1. Fügen Sie Einträge für Ihre delegierten Subdomains hinzu, z. B.:

   ```text
   applinks:www.mybusiness.com
   applinks:data.email.mybusiness.com
   ```

1. Verarbeiten Sie universelle Links in der App und rufen Sie den ursprünglichen Link aus der Antwortkopfzeile ab.

   +++ Beispiel: iOS 13+ mit Szenen

   ```swift
   class SceneDelegate: UIResponder, UIWindowSceneDelegate {
   
       func scene(_ scene: UIScene,
                 continue userActivity: NSUserActivity) {
           guard userActivity.activityType == NSUserActivityTypeBrowsingWeb,
                 let incomingURL = userActivity.webpageURL else {
               return
           }
   
           handleUniversalLink(url: incomingURL)
       }
   
       private func handleUniversalLink(url: URL) {
           // Only handle AJO tracked mobile clicks
           guard url.host == "data.email.mybusiness.com",
                 url.path.hasPrefix("/ee/v1/mclick") else {
               // Could also handle direct www.mybusiness.com links here
               return
           }
   
           resolveTrackedUrlAndRoute(url)
       }
   
       private func resolveTrackedUrlAndRoute(_ trackedUrl: URL) {
           var request = URLRequest(url: trackedUrl)
           request.httpMethod = "GET"
   
           URLSession.shared.dataTask(with: request) { _, response, error in
               guard error == nil,
                     let httpResponse = response as? HTTPURLResponse,
                     let locationValue = httpResponse.allHeaderFields["Location"] as? String,
                     let finalUrl = URL(string: locationValue) else {
                   return
               }
   
               DispatchQueue.main.async {
                   self.routeToDestination(finalUrl)
               }
           }.resume()
       }
   
       private func routeToDestination(_ url: URL) {
           // Example: map URL paths to screens
           // https://www.mybusiness.com/dashboard/offers/coupons
           // → OffersViewController for Coupons
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>Die App muss eine **GET** für die `mclick`-URL durchführen und die **`Location`**-Kopfzeile lesen und dann basierend auf der **endgültigen**-URL weiterleiten.
>
>Öffnen Sie nicht einfach die `mclick` URL in Safari. Das widerspricht dem Zweck des Deeplinkings.

### Android (App-Links) {#android-implementation}

1. Fügen Sie den Intent-Filter für App-Links in Ihrer Android-App hinzu.

   ```xml
   <activity
       android:name=".DeepLinkActivity"
       android:exported="true">
   
       <intent-filter android:autoVerify="true">
           <action android:name="android.intent.action.VIEW" />
           <category android:name="android.intent.category.DEFAULT" />
           <category android:name="android.intent.category.BROWSABLE" />
   
           <data
               android:scheme="https"
               android:host="data.email.mybusiness.com"
               android:pathPrefix="/ee/v1/mclick" />
       </intent-filter>
   
   </activity>
   ```

1. Implementieren Sie den Deep-Link-Handler.

   +++ In Kotlin:

   ```kotlin
   class DeepLinkActivity : AppCompatActivity() {
   
       override fun onCreate(savedInstanceState: Bundle?) {
           super.onCreate(savedInstanceState)
   
           val trackedUri = intent?.data
           if (trackedUri == null ||
               trackedUri.host != "data.email.mybusiness.com" ||
               !trackedUri.path.orEmpty().startsWith("/ee/v1/mclick")) {
               finish()
               return
           }
   
           resolveTrackedUrlAndRoute(trackedUri)
       }
   
       private fun resolveTrackedUrlAndRoute(trackedUri: Uri) {
           lifecycleScope.launch(Dispatchers.IO) {
               try {
                   val finalUrl = followRedirect(trackedUri.toString())
                   withContext(Dispatchers.Main) {
                       routeToDestination(finalUrl)
                       finish()
                   }
               } catch (e: Exception) {
                   // Optionally log error, fallback to browser
                   finish()
               }
           }
       }
   
       private fun followRedirect(trackedUrl: String): Uri {
           val client = OkHttpClient.Builder()
               .followRedirects(false) // We want to read Location ourselves
               .build()
   
           val request = Request.Builder()
               .url(trackedUrl)
               .get()
               .build()
   
           client.newCall(request).execute().use { response ->
               val location = response.header("Location")
                   ?: throw IllegalStateException("Missing Location header")
               return Uri.parse(location)
           }
       }
   
       private fun routeToDestination(finalUri: Uri) {
           // Example: interpret https://www.mybusiness.com/dashboard/offers/coupons
           // and open the correct Activity / Fragment
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>Wie iOS muss die App die `mclick`-URL aufrufen und die **`Location`**-Kopfzeile verwenden, um das endgültige Ziel zu bestimmen.
>
>Verwenden Sie `followRedirects(false)`, damit Sie die Umleitungshandhabung steuern und Analysen bei Bedarf genau protokollieren können.
>
>Die Routing-Logik ist App-spezifisch. Definieren Sie eine klare Zuordnung von URLs zu Bildschirmen.

## Empfohlene Verfahren {#deeplink-best-practices}

* **Stabile Pfade verwenden**: Routen bevorzugen, die gegenüber Änderungen der App-Benutzeroberfläche robust sind (z. B. `/account/orders` statt `/tab/3/view/2`).
* **Konto für getrackte Pfade**: Wenn das Linktracking aktiviert ist, kann der geklickte Link getrackte Pfadmuster verwenden (z. B. `/ee/v1/mclick/`). Stellen Sie sicher, dass Ihr Router die endgültige URL analysieren kann, nachdem der getrackte Link aufgelöst wurde.
* **Parameter vorhersehbar halten**: Definieren eines konsistenten Parameterschemas (z. B. `?orderId=12345`).
* **Vermeiden Sie vertrauliche Daten in URLs**: Fügen Sie keine Geheimnisse oder persönlichen Daten direkt in die Deeplink-URL ein.
* **Deeplink testen**: Führen Sie einen Testversand durch und klicken Sie auf dem Gerät, auf dem die App installiert ist, auf den Deeplink.
* **Auf echten Geräten validieren**: Universal Links und das Verhalten bei der Auflösung getrackter Links sind zuverlässiger bei der Validierung auf physischen Geräten als auf Simulatoren.
* **App-seitiges Routing validieren**: Wenn der Deeplink nicht den erwarteten Bildschirm öffnet, validieren Sie das App-seitige Routing und das URL-Format (Host/Pfad/Abfrage und URL-Codierung).
* **Beachten Sie die App-Initialisierung**: Das Verhalten von App-Links/universellen Links ist am zuverlässigsten, nachdem die App mindestens einmal installiert und geöffnet wurde.

## Fehlerbehebung und häufig gestellte Fragen {#troubleshooting-faq}

+++ Die App wird nicht geöffnet, wenn ich auf den Deeplink tippe.

* Stellen Sie sicher, dass die URL den Host- und Pfadmustern entspricht, für die Ihre App registriert ist, einschließlich getrackter Klickpfade, wenn das Linktracking aktiviert ist (z. B. Pfade unter `/ee/v1/mclick/`).
* Bestätigen Sie bei universellen Links von iOS und Links zur Android-App, dass die Domain-Zuordnung (AASA/`assetlinks.json`) korrekt konfiguriert und erreichbar ist.
* Testen auf einem realen Gerät (Simulatoren/Emulatoren können sich für die Link-Zuordnung anders verhalten).

+++

+++ Die App wird geöffnet, navigiert jedoch nicht zum erwarteten Bildschirm.

* Bestätigen Sie, dass der App-seitige Router den URL-Pfad/die Abfrage korrekt analysiert.
* URL-Kodierung überprüfen: reservierte Zeichen sollten URL-kodiert sein.
* Überprüfen Sie, ob Parameternamen und -werte mit den Erwartungen des Routers übereinstimmen.

+++

+++ Was passiert, wenn die App nicht installiert ist?

* Wenn dieselbe HTTPS-URL von Ihrer Website bereitgestellt werden kann, kann der Link eine Web-Seite als Ausweichlösung öffnen, wenn die App nicht installiert ist (konfigurieren Sie Ihr Web-Ziel und das Routing entsprechend).

+++

+++ Wie binde ich Sonderzeichen sicher in Parameter ein?

URL-kodierte Abfrageparameterwerte. Dadurch werden Bereitstellungs- und Rendering-Probleme reduziert und Parsing-Fehler in der App vermieden.

+++

+++ Wie sollten wir End-to-End testen?

* Erstellen Sie einen Korrekturabzug mit einem Deeplink und klicken Sie darauf auf iOS- und Android-Geräten (installierte und nicht installierte Szenarien).
* Validieren:
   * Der endgültige Wert der E-Mail- oder SMS-Relation (Host/Pfad/Abfrage)
   * Die Verknüpfung auf Betriebssystemebene (bei Verwendung von universellen Links/App-Links)
   * Das In-App-Routing-Ergebnis

+++

+++ Ich habe eine App, aber verschiedene Subdomains für die Organisation. Sollte ich für jede Subdomain die Erstellung von AASA und assetLinks.json anfordern?

Ja. Wenn Sie Deeplinking für jede delegierte Subdomain wünschen, fordern Sie die AASA- und `assetlinks.json`-Konfiguration für jede Subdomain an, die die Funktion unterstützen soll.

+++

+++ Sollte die von mir konfigurierte URL ein Deeplinking-Format verwenden (z. B. `appname://path`)?

Sie können ein benutzerdefiniertes URL-Schema verwenden (z. B. `appname://path`), der empfohlene Ansatz ist jedoch ein universeller Link oder ein App-Link (`https://`), der dem HTTPS-basierten Setup in den Konfigurationsabschnitten und den Implementierungsabschnitten auf dieser Seite entspricht.

+++

+++ Sind UTM-Parameter für die URL in der Mobile App für Analysen verfügbar?

Ja. UTM-Parameter, die Sie in [!DNL Journey Optimizer] konfigurieren, sind in der endgültigen URL enthalten, die im `Location`-Header zurückgegeben wird, wenn Ihre App eine GET auf der `mclick` URL durchführt, sodass Sie sie für In-App-Analysen verwenden können.

+++

+++ Was ist das Benutzererlebnis für `/ee/v1/click/` URLs?

Der Link wird im Standard-Webbrowser des Geräts geöffnet (Standard-Klick-Tracking-Verhalten) und nicht wie ein App-Deep-Link durch den auf dieser Seite beschriebenen `mclick`-Fluss gehandhabt.

+++
