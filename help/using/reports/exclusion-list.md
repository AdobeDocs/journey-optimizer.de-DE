---
solution: Journey Optimizer
product: journey optimizer
title: Ausschlussliste
description: Weitere Informationen zu Ausschlüssen beim Versand
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 100%

---

# Ausschlussgründe {#exclusion-list}

| Ausschlussgrund | Fehler-Code | Kanal | Erklärung |
|-|-|-|-|
| RuntimeDispatchError | 050301 | Alle Kanäle | Generisches Ausschlussereignis für Laufzeitfehler beim Senden. |
| RuntimeRenderingError | 050302 | Alle Kanäle | Generisches Ausschlussereignis für Laufzeitfehler beim Rendering. |
| NamespaceErrorForExperimentation | 050017 | Alle Kanäle | Ein Ausschlussereignis wird generiert, wenn sich der Namespace im Experiment vom Namespace des Profils unterscheidet. |
| ExperimentationHoldoutExclusion | 050018 | Alle Kanäle | Dieses Ausschlussereignis wird generiert, wenn die qualifizierte Abwandlung eines Experiments „Holdout“ lautet. |
| ExcludedForControlRules | 050002 | Alle Kanäle | Dieses Ausschlussereignis wird generiert, wenn der Versand der aktuellen Nachricht gegen die Kontrollregeln verstößt, z. B. die zulässige Anzahl von E-Mails in einem Monat. |
| DirectMailNoVariantDefined | 050062 | DirectMail | Ein Ausschlussereignis wird generiert, wenn die Variante in der Briefpost nicht definiert ist. |
| DirectMailNoMessageFoundForTreatment | 050061 | DirectMail | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Abwandlung gefunden wird. |
| EmailNoConsent | 050101 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Person sich vom Empfangen von Marketing-E-Mails abgemeldet hat. |
| Unterdrückt | 050107 | E-Mail | Ausschluss aufgrund eines der Unterdrückungsgründe. |
| EmailSuppressed | 050102 | E-Mail | Ein Ausschlussereignis wird erzeugt, wenn die Ziel-E-Mail unterdrückt wird. |
| DomainSuppressed | 050105 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Domain der angeschriebenen E-Mail-Adresse unterdrückt ist. |
| NotAllowed | 050108 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Zulassungsliste aktiviert ist und die angeschriebene E-Mail-Adresse aus der Zulassungsliste ausgeschlossen ist. |
| EmailNotAllowed | 050103 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Zulassungsliste aktiviert ist und die angeschriebene E-Mail-Adresse aus der Zulassungsliste ausgeschlossen ist. |
| DomainNotAllowed | 050106 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Zulassungsliste aktiviert ist und die Domain der angeschriebenen E-Mail-Adresse von der Zulassungsliste ausgeschlossen ist. |
| EmailNoSubscriberIdFoundInProfile | 050025 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Abonnenten-ID im Profil einer Abonnement-E-Mail nicht gefunden wird. |
| EmailNoAddressFoundInProfile | 050020 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die E-Mail-Adresse in der Ausführungsadresse nicht gefunden wird. |
| EmailNoAddressDefinedInPreset | 050021 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Ausführungsadresse nicht in der Konfiguration definiert ist. |
| EmailNoVariantDefined | 050026 | E-Mail | Ein Ausschlussereignis wird generiert, wenn in der E-Mail-Nachricht keine Variante definiert ist. |
| EmailNoMessageFoundForTreatment | 050027 | E-Mail | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Abwandlung gefunden wird. |
| EmailMalformedAddress | 050024 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die E-Mail eine fehlerhafte Adresse enthält. |
| InAppNoVariantDefined | 050041 | InApp | Ein Ausschlussereignis wird generiert, wenn für In-App-Nachrichten keine Variante definiert ist. |
| InAppNoMessageFoundForTreatment | 050042 | InApp | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Abwandlung gefunden wird. |
| PushNoTokenFoundInProfile | 050030 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn das Profil keine Push-Token aufweist. |
| PushNoValidTokenFoundForApps | 050031 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn in der Konfiguration kein gültiges Token für die Zielanwendungen gefunden wird. |
| PushMalformedProfile | 050034 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn pushNotificationDetails im Profil fehlerhaft ist. |
| PushNoConsent | 050111 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn die Person sich von Marketing-Push-Benachrichtigungen abgemeldet hat. |
| PushNoApplicationDefinedInPreset | 050033 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn die Konfiguration keine Zielanwendung enthält. |
| PushNoVariantDefined | 050035 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn keine Variante definiert ist. |
| PushNoMessageFoundForTreatment | 050036 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Abwandlung gefunden wird. |
| SMSNoConsent | 050104 | SMS | Ein Ausschlussereignis wird generiert, wenn sich der Benutzer von Marketing-SMS abgemeldet hat. |
| SMSFromNumberNotDefinedInPreset | 050152 | SMS | Ein Ausschlussereignis wird generiert, wenn „FromNumber“ nicht in der Konfiguration definiert ist. |
| SMSNoToNumberDefinedInProfile | 050153 | SMS | Ein Ausschlussereignis wird generiert, wenn „ToNumber“ nicht in der Konfiguration definiert ist. |
| SMSNoVariantDefined | 050154 | SMS | Ein Ausschlussereignis wird generiert, wenn keine Variante definiert ist. |
| SMSNoMessageFoundForTreatment | 050155 | SMS | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Abwandlung gefunden wird. |
| WebNoVariantDefined | 050041 | Web | Ein Ausschlussereignis wird generiert, wenn für eine Web-Nachricht keine Variante definiert ist. |
| WebNoMessageFoundForTreatment | 050042 | Web | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Abwandlung gefunden wird. |
