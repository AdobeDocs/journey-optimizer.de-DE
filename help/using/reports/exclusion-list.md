---
solution: Journey Optimizer
product: journey optimizer
title: Ausschlussliste
description: Erfahren Sie mehr über Ausschlüsse, die beim Versand auftreten
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: 853e87cdd69a3fc180dcb1aa38b4b67f27977939
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 83%

---

# Ausschlussgründe {#exclusion-list}

## Wie Ausschlüsse in Kampagnenberichten gezählt werden

Beachten Sie bei der Anzeige von Kampagnenberichten, dass *Metrik* Ausschlüsse“ wie folgt berechnet wird:

**Ausschlüsse = eindeutige Ausschlüsse + doppelte Ausschlussereignisse**

Wenn also ein Profil mehrmals ausgeschlossen wird (z. B. aufgrund mehrerer Ausschlussereignisse für dasselbe Profil), wird jedes Ereignis in der Gesamtzahl der Ausschlüsse gezählt. Daher kann die Summe aus *Zugestellt* und *Ausschlüssen* die ursprüngliche Zielgruppengröße überschreiten. Dieses Verhalten ist zu erwarten und spiegelt die Art und Weise wider, wie Ausschlussereignisse im System verfolgt werden.

**Beispiel:**

- Zielgruppe: 94.000 Profile
- Veröffentlicht: 69.000
- Ausschlüsse: 37.000 (einschließlich doppelter Ausschlussereignisse)
- Insgesamt (geliefert + Ausschlüsse): 106.000

Die Gesamtzahl überschreitet die Zielgruppe, da doppelte Ausschlussereignisse in der Anzahl der Ausschlüsse enthalten sind.

Weitere Informationen zu den spezifischen Ausschlussgründen finden Sie in der folgenden Tabelle.

## Liste der Ausschlussgründe

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
