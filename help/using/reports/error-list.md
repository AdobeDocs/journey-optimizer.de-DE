---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerliste
description: Erfahren Sie mehr über Fehler beim Versand
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: deaa72f235a64dd2cb9bfbafef3574fdb025a026
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 9%

---

# Liste der Fehlerursachen {#error-list}

| Ausschlussgrund | Fehler-Code | Kanal | Erklärung |
|-|-|-|-|
| RuntimeDispatchError | 050301 | Alle Kanäle | Generisches Ausschlussereignis für einen Laufzeitaussendefehler. |
| RuntimeRenderingError | 050302 | Alle Kanäle | Generisches Ausschlussereignis für Fehler beim Rendern der Laufzeit. |
| NamespaceErrorForExperimentation | 050017 | Alle Kanäle | Ein Ausschlussereignis wird generiert, wenn sich der Namespace in Experiment vom Namespace des Profils unterscheidet. |
| ExperimentationHoldoutExclusion | 050018 | Alle Kanäle | Dieses Ausschlussereignis wird generiert, wenn die qualifizierte Behandlung für ein Experiment &quot;Holdout&quot;lautet. |
| ExcludedForControlRules | 050002 | Alle Kanäle | Dieses Ausschlussereignis wird generiert, wenn der Versand der aktuellen Nachricht zu einem Verstoß gegen die Kontrollregeln führt, z. B. die zulässige Anzahl von E-Mails in einem Monat. |
| DirectMailNoVariantDefined | 050062 | DirectMail | Ein Ausschlussereignis wird generiert, wenn in der Briefpost-Variante nicht definiert ist. |
| DirectMailNoMessageFoundForTreatment | 050061 | DirectMail | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Behandlung gefunden wird. |
| EmailNoConsent | 050101 | E-Mail | Ein Ausschlussereignis wird generiert, wenn der Benutzer sich vom Erhalt von Marketing-E-Mails abgemeldet hat. |
| Unterdrückt | 050107 | E-Mail | Ausschluss aufgrund eines der Gründe der Unterdrückung. |
| EmailSuppressed | 050102 | E-Mail | Wenn die Ziel-E-Mail unterdrückt wird, wird ein Ausschlussereignis generiert. |
| DomainSuppressed | 050105 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Domäne der E-Mail-Zielgruppe unterdrückt wird. |
| NotAllowed | 050108 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Zulassungsliste aktiviert ist und die E-Mail-Zielgruppe aus der Zulassungsliste ausgeschlossen wird. |
| EmailNotAllowed | 050103 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Zulassungsliste aktiviert ist und die E-Mail-Zielgruppe aus der Zulassungsliste ausgeschlossen wird. |
| DomainNotAllowed | 050106 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Zulassungsliste aktiviert ist und die Domain der E-Mail-Zielgruppe von der Zulassungsliste ausgeschlossen wird. |
| EmailNoSubscriberIdFoundInProfile | 050025 | E-Mail | Ein Ausschlussereignis wird generiert, wenn subscriberId im Profil einer Abonnenten-E-Mail nicht gefunden wird. |
| EmailNoAddressFoundInProfile | 050020 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die E-Mail-Adresse nicht in der Ausführungsadresse gefunden wird. |
| EmailNoAddressDefinedInPreset | 050021 | E-Mail | Ein Ausschlussereignis wird erzeugt, wenn die Ausführungsadresse nicht an der Oberfläche definiert ist. |
| EmailNoVariantDefined | 050026 | E-Mail | Wenn in der E-Mail-Nachricht keine Variante definiert ist, wird ein Ausschlussereignis generiert. |
| EmailNoMessageFoundForTreatment | 050027 | E-Mail | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Behandlung gefunden wird. |
| EmailMalformedAddress | 050024 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die E-Mail eine fehlerhafte Adresse enthält. |
| InAppNoVariantDefined | 050041 | InApp | Wenn für In-App-Nachrichten keine Variante definiert ist, wird ein Ausschlussereignis generiert. |
| InAppNoMessageFoundForTreatment | 050042 | InApp | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Behandlung gefunden wird. |
| PushNoTokenFoundInProfile | 050030 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn das Profil keine Push-Token aufweist. |
| PushNoValidTokenFoundForApps | 050031 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn kein gültiges Token für die Targeting-Apps auf der Oberfläche gefunden wird. |
| PushMalformedProfile | 050034 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn pushNotificationDetails im Profil fehlerhaft ist. |
| PushNoConsent | 050111 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn der Benutzer sich von Marketing-Push-Benachrichtigungen abgemeldet hat. |
| PushNoApplicationDefinedInPreset | 050033 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn die Oberfläche keine Zielanwendung enthält. |
| PushNoVariantDefined | 050035 | Push-Benachrichtigung | Wenn keine Variante definiert ist, wird ein Ausschlussereignis generiert. |
| PushNoMessageFoundForTreatment | 050036 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Behandlung gefunden wird. |
| SMSNoConsent | 050104 | SMS | Ein Ausschlussereignis wird generiert, wenn der Benutzer sich von der Marketing-SMS abgemeldet hat. |
| SMSFromNumberNotDefinedInPreset | 050152 | SMS | Ein Ausschlussereignis wird generiert, wenn &quot;FromNumber&quot;nicht in der Oberfläche definiert ist. |
| SMSNoToNumberDefinedInProfile | 050153 | SMS | Ein Ausschlussereignis wird generiert, wenn &quot;ToNumber&quot;nicht auf der Oberfläche definiert ist. |
| SMSNoVariantDefined | 050154 | SMS | Wenn keine Variante definiert ist, wird ein Ausschlussereignis generiert. |
| SMSNoMessageFoundForTreatment | 050155 | SMS | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Behandlung gefunden wird. |
| WebNoVariantDefined | 050041 | Web | Wenn für eine Webnachricht keine Variante definiert ist, wird ein Ausschlussereignis generiert. |
| WebNoMessageFoundForTreatment | 050042 | Web | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Behandlung gefunden wird. |
