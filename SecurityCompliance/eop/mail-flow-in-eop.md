---
title: Nachrichtenfluss in EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/13/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
description: Als ein Exchange Online Protection (EOP) Kunde werden alle Nachrichten, die an Ihre Organisation gesendet werden, durch EOP geleitet, bevor die Mitarbeiter sie sehen. Ob Sie alle Ihre Postfächer in der Cloud mit Exchange Online hosten oder ob Sie Ihre Postfächer vor Ort hosten (genannt eigenständiges Szenario), haben Sie Optionen für die Art der Weiterleitung von Nachrichten, die zur Bearbeitung EOP durchlaufen, bevor sie an die Postfächer Ihrer Mitarbeiter weitergeleitet werden, um weiterhin die Vorteile Ihrer bestehenden Infrastruktur nutzen zu können.
ms.openlocfilehash: b223efc62ff875ed345ce27a17263b3876829999
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255893"
---
# <a name="mail-flow-in-eop"></a>Nachrichtenfluss in EOP

Als ein Exchange Online Protection (EOP) Kunde werden alle Nachrichten, die an Ihre Organisation gesendet werden, durch EOP geleitet, bevor die Mitarbeiter sie sehen. Ob Sie alle Ihre Postfächer in der Cloud mit Exchange Online hosten oder ob Sie Ihre Postfächer vor Ort hosten (genannt eigenständiges Szenario), haben Sie Optionen für die Art der Weiterleitung von Nachrichten, die zur Bearbeitung EOP durchlaufen, bevor sie an die Postfächer Ihrer Mitarbeiter weitergeleitet werden, um weiterhin die Vorteile Ihrer bestehenden Infrastruktur nutzen zu können.
  
Sie können eine benutzerdefinierte Mail-Weiterleitung konfigurieren, um Ihr Massaging an Ihre Unternehmensanforderung anzupassen. Angenommen, Sie möchten alle ausgehenden Nachrichten durch eine Richtlinienprüfungsvorrichtung leiten. 
  
## <a name="working-with-messages-and-message-access-options"></a>Arbeiten mit Nachrichten und Nachrichtenzugangsoptionen

EOP bietet viel Flexibilität bezüglich der Weiterleitung Ihrer Nachrichten. In den folgenden Themen werden Schritte im Nachrichtenflussprozess erklärt.
  
[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Beschreibt die verzeichnisbasierte Edge-Blockierung, die es Ihnen ermöglicht, Nachrichten für ungültige Empfänger am Dienstnetzwerkumkreis abzulehnen. 
  
[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) beschreibt die Verwaltung von Domänen, die mit Ihrem EOP-Dienst verbunden sind. 
  
Wenn Sie Ihrer Organisation Unterdomänen hinzufügen, können Sie auch diese mit dem EOP-Dienst verwalten. Weitere Informationen zu Unterdomänen finden Sie unter [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).
  
Unter [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) erhalten Sie eine Einführung in Connectors und erfahren, wie diese zum Anpassen von E-Mail-Routing verwendet werden können. Dazu gehören Szenarien zur Gewährleistung sicherer Kommunikation mit einer Partnerorganisation sowie das Einrichten eines Smarthosts. 
  
Sie müssen eine Reihe von Konfigurationsschritten ausführen, um wirklich sicherzustellen, dass Junk-E-Mail in die Junk-E-Mail-Ordner der Benutzer umgeleitet werden. Diese werden ausführlich unter [sicherstellen, dass Spam an die Junk-e-Mail-Ordner der einzelnen Benutzer weitergeleitet wird](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). Wenn die Nachrichten nicht in die Junk-E-Mail-Ordner der Benutzer verschoben werden sollen, können Sie eine andere Aktion auswählen, indem Sie die standardmäßige Inhaltsfilterrichtlinie im Exchange Admin Center bearbeiten. Weitere Informationen finden Sie unter [Konfigurieren von Spamfilterrichtlinien](../configure-your-spam-filter-policies.md).
  
## <a name="verify-mail-flow"></a>Überprüfen des Nachrichtenflusses

Weitere Informationen zum Überprüfen des EOP-Setups und der Connectorkonfiguration finden Sie im Abschnitt "Woher wissen Sie, dass diese Aufgabe erfolgreich war?" unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md). 
  
[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) liefert Anweisungen, um zu testen, dass Ihr Nachrichtenfluss richtig konfiguriert ist. 
  

