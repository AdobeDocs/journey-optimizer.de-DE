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
TQID: https://experienceleague.adobe.com/Fz8Ld7Ga9jq9VNQx1RBoZSH0JonnXhy-0fBv7-zmWsw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 892
ht-degree: 96%

---

# Ausschlussgründe {#exclusion-list}

## Wie Ausschlüsse in Kampagnenberichten gezählt werden

Beachten Sie bei der Anzeige von Kampagnenberichten, dass die Metrik *Ausschlüsse* wie folgt berechnet wird:

**Ausschlüsse = eindeutige Ausschlüsse + doppelte Ausschlussereignisse**

Wenn also ein Profil mehrmals ausgeschlossen wird (z. B. aufgrund mehrerer Ausschlussereignisse für dasselbe Profil), wird jedes Ereignis in der Gesamtzahl der Ausschlüsse gezählt. Daher kann die Summe aus *Zugestellt* und *Ausschlüsse* die ursprüngliche Zielgruppengröße überschreiten. Dieses Verhalten ist normal und entspricht der Art und Weise, wie Ausschlussereignisse im System verfolgt werden.

**Beispiel:**

- Zielgruppe: 94.000 Profile
- Zugestellt: 69.000
- Ausschlüsse: 37.000 (einschließlich doppelter Ausschlussereignisse)
- Insgesamt (Zugestellt + Ausschlüsse): 106.000

Die Gesamtzahl überschreitet die Zielgruppengröße, da doppelte Ausschlussereignisse in der Anzahl der Ausschlüsse enthalten sind.

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
| UnsubscribeLinkNotValid | 050081 | E-Mail | Ein Ausschlussereignis wird generiert, wenn die Betrefflänge von „list-unsubscribe mailTo“ größer als das RFC-Limit von 998 Zeichen ist. |
| InAppNoVariantDefined | 050041 | InApp | Ein Ausschlussereignis wird generiert, wenn für In-App-Nachrichten keine Variante definiert ist. |
| InAppNoMessageFoundForTreatment | 050042 | InApp | Ein Ausschlussereignis wird generiert, wenn das Experiment für die Nachricht aktiviert ist und keine Nachricht für die qualifizierte Abwandlung gefunden wird. |
| PushNoTokenFoundInProfile | 050030 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn das Profil keine Push-Token aufweist. |
| PushNoValidTokenFoundForApps | 050031 | Push-Benachrichtigung | Ein Ausschlussereignis wird generiert, wenn in der Konfiguration kein gültiges Token für die Zielanwendungen gefunden wird. **Wichtig:** Bei Verwendung eines Produktionszertifikats muss das Attribut `pushNotificationDetails.platform` im Benutzerprofil auf `apns` gesetzt werden. Wenn Sie ein Sandbox-Zertifikat verwenden, setzen Sie es auf `apnsSandbox`. Wenn das Plattformattribut und der Zertifikatstyp nicht übereinstimmen, wird dieser Ausschluss ausgelöst. |
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
