---
title: Was ist EoP
ms.author: tracyp
author: msfttracyp
ms.reviewer: andypunt
manager: dansimp
ms.date: 02/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 393b0050-7c7e-49e6-a03d-b1e09fe4de9e
description: Dieses Einführungsdokument hilft Ihnen, Exchange Online Schutz (EoP) und einige wichtige Terminologie zu verstehen. Dies gilt für Office 365 Kunden, die Exchange Online in der Cloud gehosteten Postfächern und EOP-eigenständigen Kunden schützen, die lokale Postfächer wie Exchange Server 2016 schützen.
ms.openlocfilehash: b0d3aac6e2c7e70ce298309d2053a7d6bb5920c1
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599461"
---
## <a name="what-is-exchange-online-protection-eop"></a>Was ist Exchange Online Schutz (EoP)

Exchange Online Protection (EoP) ist ein Cloud-basierter e-Mail-Filterdienst, der Ihre Organisation vor Spam und Schadsoftware schützen kann. Wenn Sie über Postfächer in Office 365 verfügen, werden diese automatisch von EoP geschützt, da Sie Teil des Diensts sind. Dies umfasst Organisationen mit Postfächern sowohl in Office 365 als auch lokal, was gemeinhin als Hybrid Szenario bezeichnet wird. EoP Standalone steht auch Kunden zur Verfügung, die keine Postfächer in der Cloud haben, aber ihre lokalen Postfächer schützen möchten. 

EoP versucht, Junk zu filtern, sodass Ihr Posteingang die Inhalte frei hält, die Benutzer nicht sehen möchten. Normalerweise werden Junk-e-Mails an den Junk-e-Mail-Ordner zugestellt. Einige Benutzer möchten sicherstellen, dass die Filterung das tut, was Sie möchten, damit der Junk-e-Mail-Ordner eine einfache Möglichkeit für Benutzer ist, sich selbst zu überprüfen.  

> [!TIP]
> Es ist eine gute Sache, wenn Junk-oder anderweitig ungültige e-Mails automatisch in den Junk-e-Mail-Ordner eingeht. Der Dienst tut, was erforderlich ist, basierend auf dem Status des Standard-oder benutzerdefinierten Administratoreinstellungen. In anderen Worten: Benutzer sollten sich keine Gedanken darüber machen, wie viele Spamnachrichten im Junk-e-Mail-Ordner angezeigt werden. Wenn Administratoren alle Junk-e-Mails aus dem Blickfeld ziehen möchten, sollte die Quarantäne konfiguriert werden. Weitere Informationen finden Sie unter [Quarantäne-e-Mail-Nachrichten in Office 365](../quarantine-email-messages.md) Artikel.

## <a name="important-terms"></a>Wichtige Begriffe

**Eingehend:** Nachrichten, die in Office 365 kommen.

**Outbound:** Nachrichten, die Office 365 ausgehen.

**Intern:** Nachrichten, die von einer Person innerhalb der Organisation an eine Person innerhalb der Organisation gesendet werden. Dies umfasst Kunden, die sich in Hybrid Szenarien befinden, und ein Postfach könnte lokal sein, und das andere Postfach befindet sich in der Cloud.

**Falsch negativ (FN):** Spam und andere Junk-e-Mails, die fälschlicherweise in den Posteingang gesendet werden.

**Falsch positiv (FP):** Legitime Nachrichten, die fälschlicherweise als Spam gekennzeichnet und in den Junk-e-Mail-Ordner oder in die Quarantäne verschoben werden.

**Spam, auch als unerwünschte e-Mail bezeichnet:** Dies erfolgt in Form von kommerzieller Werbung, Kettenbriefen, politischen Mailings usw. Hierbei handelt es sich um e-Mails, die Benutzer nicht für und von Spammern registrieren, die versuchen, Produkte anzufordern oder Betrugsversuche zu begehen.

**Phishing:** Bei Phishing handelt es sich um eine spezielle Art von Spam, die Sie dazu verleiten soll, persönliche Informationen zum Zwecke des Identitätsdiebstahls oder-Betrugs zu geben. Dieser Nachrichtentyp enthält normalerweise einen böswilligen Link oder eine Anlage, jedoch nicht immer.

**Spoof:** Spoofing ist, wenn Spammer die From-Kopfzeile fälschen, sodass Nachrichten von einer Person oder einem anderen als der tatsächlichen Quelle stammen. Dies kann Spam sein, wird aber am häufigsten für Phishing-Benutzer verwendet.

**Identitätswechsel:** Diese Art von Spam ist auch eine Möglichkeit, die Absenderadresse zu fälschen, aber Sie erfolgt durch Ändern eines Teils des Namens oder der Domäne, sodass Sie wie die reale Quelle aussieht. Beispiel: Bi11@micr0s0ft.com, wobei das "l" in Bill tatsächlich die Zahl "11" und das "o" in Microsoft wurde durch die Zahl Null ersetzt.

**Bulk:** Massen-e-Mails werden normalerweise von Benutzern angefordert, wenn auch indirekt, wenn Unternehmen Informationen an andere Unternehmen verkaufen. Es ist üblich, dass sich Benutzer absichtlich für Massen-e-Mails (d. h. Briefsendungen) registrieren, aber später vergessen und denken, dass es sich um Spam handelt. Massen-e-Mails werden zu Spam, wenn Massen-e-Mail-Nachrichten mehr senden als Benutzer registrieren und die Reklamations Stufe zu hoch wird.
