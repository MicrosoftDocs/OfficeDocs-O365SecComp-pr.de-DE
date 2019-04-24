---
title: Aufbewahren, Löschen und Zerstören von Daten in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Übersicht über die Microsoft-Richtlinien für Office 365 zur Aufbewahrung, Löschung und Vernichtung von Daten.
ms.openlocfilehash: fcae11f10278f1357a68ea3f9a1178da97322775
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262837"
---
# <a name="data-retention-deletion-and-destruction-in-office-365"></a>Aufbewahren, Löschen und Zerstören von Daten in Office 365

Microsoft verfügt über eine Standard Richtlinie für Datenverarbeitung für Office 365, die angibt, wie lange Kundendaten nach dem Löschen aufbewahrt werden. In der Regel gibt es zwei Szenarien, in denen Kundendaten gelöscht werden:

- **AktivEs löschen** – der Mandant hat ein aktives Abonnement, und ein Benutzer löscht Daten, oder die von einem Benutzer bereitgestellten Daten werden vom Administrator gelöscht.
- **PassivEs löschen** – das Mandanten Abonnement endet.

## <a name="data-retention"></a>Datenaufbewahrung

Für jedes dieser Lösch Szenarien zeigt die folgende Tabelle die maximale Datenaufbewahrungsdauer nach Datenkategorie und Klassifizierung:

| Datenkategorie | Datenklassifikation | Beschreibung | Beispiele | AufbewahrungsZeitraum |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Kundendaten | Kunden Inhalt| Direkt von Administratoren und Benutzern bereitgestellte Inhalte <br><br> Hierzu gehören alle Text-, Sound-, Video-, Bilddateien und Software, die in Microsoft-Datencentern erstellt und gespeichert werden, wenn Sie die Dienste in Office 365 verwenden. | Beispiele für die am häufigsten verwendeten Office 365-Anwendungen, die Benutzern das Erstellen von Daten ermöglichen, sind Word, Excel, PowerPoint, Outlook und OneNote. <br><br> Kunden Inhalte enthalten auch kundeneigene/gelieferte Geheimnisse (Kennwörter, Zertifikate, Verschlüsselungsschlüssel, Speicherschlüssel) | **AktivEs Lösch Szenario:** höchstens 30 Tage <br><br> **PassivEs Lösch Szenario:** höchstens 180 Tage |
| Kundendaten | Identifizierbare Informationen für endBenutzer (EUII) | Daten, mit denen der Benutzer eines Microsoft-Diensts identifiziert oder verwendet werden kann. EUII enthält keine Kunden Inhalte | Benutzername oder Anzeigename <br><br> Benutzerprinzipalname (Name @ Domäne) <br><br>  Benutzerspezifische IP-Adressen | **AktivEs Lösch Szenario:** höchstens 180 Tage (nur eine mandantenadministrator-Aktion) <br><br> **PassivEs Lösch Szenario:** höchstens 180 Tage |
| Persönliche Daten <br> (Daten sind nicht in Kundendaten enthalten) | Pseudonyme Bezeichner des endBenutzers (EUPI) | Ein von Microsoft erstellter Bezeichner, der an den Benutzer eines Microsoft-Diensts gebunden ist. Wenn EUPI mit anderen Informationen, wie beispielsweise einer Zuordnungstabelle, kombiniert wird, wird der Endbenutzer identifiziert. <br><br> EUPI enthält keine vom Kunden hochgeladenen oder erstellten Informationen. | Benutzer-GUIDs, PUIDs oder SIDs <br><br> Sitzungs-IDs | **AktivEs Lösch Szenario:** höchstens 30 Tage <br><br> **PassivEs Lösch Szenario:** höchstens 180 Tage |

## <a name="subscription-retention"></a>Abonnement Aufbewahrung

Während der Laufzeit eines aktiven Abonnements kann ein Abonnent jederzeit in Office 365 gespeicherte Kundendaten zugreifen, extrahieren oder löschen. Wenn ein kostenpflichtiges Abonnement beendet oder beendet wird, speichert Microsoft in Office 365 gespeicherte Kundendaten in einem Konto mit eingeschränkten Funktionen 90 Tage lang, damit der Abonnent die Daten extrahieren kann. Nachdem der Aufbewahrungszeitraum für 90 Tage abgelaufen ist, wird das Konto von Microsoft deaktiviert und die Kundendaten gelöscht. Nicht mehr als 180 Tage nach Ablauf oder Beendigung eines Abonnements von Office 365 wird Microsoft das Konto deaktivieren und alle Kundendaten aus dem Konto löschen. Sobald die maximale Aufbewahrungsdauer für Daten abgelaufen ist, werden die Daten kommerziell nicht wiederhergestellt.

Im Fall einer kostenlosen Testversion wird Ihr Konto in den meisten Ländern und Regionen für 30 Tage in einen Kulanz Status versetzt. Während dieses Kulanzzeitraums haben Sie die Option, Office 365 zu erwerben. Wenn Sie sich entscheiden, Office 365 nicht zu kaufen, können Sie entweder Ihre Testversion abbrechen oder den Aktivierungszeitraum ablaufen lassen, und Ihre Test Kontoinformationen und-Daten werden gelöscht.

## <a name="expedited-deletion"></a>Beschleunigter Löschvorgang
Während der Laufzeit eines Abonnements kann ein Teilnehmer jederzeit den Microsoft-Support kontaktieren und eine beschleunigte Abonnement-Aufhebung anfordern. In diesem Prozess werden alle Benutzerdaten, einschließlich Daten in SharePoint Online, Exchange Online, die möglicherweise unterhalten oder in inaktiven Postfächern gespeichert sind, drei Tage nach dem Eintreten des von Microsoft bereitgestellten Sperrcodes durch den Administrator gelöscht. Weitere Informationen zur beschleunigten Deaktivierung finden Sie unter [Cancel Office 365](https://support.office.com/article/Cancel-Office-365-for-business-b1bc0bef-4608-4601-813a-cdd9f746709a).

## <a name="related-links"></a>Links zu verwandten Themen
- [Zerstörung von Daten](office-365-data-destruction.md)
- [Unveränderbarkeit in Office 365](office-365-data-immutability.md)
- [Löschen von Exchange Online-Daten](office-365-exchange-online-data-deletion.md)
- [Löschen von SharePoint Online-Daten](office-365-sharepoint-online-data-deletion.md)
- [Löschen von Skype for Business-Daten](office-365-skype-data-deletion.md)