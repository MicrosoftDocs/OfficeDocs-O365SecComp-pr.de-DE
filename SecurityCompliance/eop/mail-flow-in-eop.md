---
title: Nachrichtenfluss in EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/13/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
description: Als ein Exchange Online Protection (EOP) Kunde werden alle Nachrichten, die an Ihre Organisation gesendet werden, durch EOP geleitet, bevor die Mitarbeiter sie sehen. Ob Sie alle Ihre Postfächer in der Cloud mit Exchange Online hosten oder ob Sie Ihre Postfächer vor Ort hosten (genannt eigenständiges Szenario), haben Sie Optionen für die Art der Weiterleitung von Nachrichten, die zur Bearbeitung EOP durchlaufen, bevor sie an die Postfächer Ihrer Mitarbeiter weitergeleitet werden, um weiterhin die Vorteile Ihrer bestehenden Infrastruktur nutzen zu können.
ms.openlocfilehash: d35e6f2fdbe7bb991ebf3d766fadae34638831ef
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027342"
---
# <a name="mail-flow-in-eop"></a>Nachrichtenfluss in EOP

Als ein Exchange Online Protection (EOP) Kunde werden alle Nachrichten, die an Ihre Organisation gesendet werden, durch EOP geleitet, bevor die Mitarbeiter sie sehen. Ob Sie alle Ihre Postfächer in der Cloud mit Exchange Online hosten oder ob Sie Ihre Postfächer vor Ort hosten (genannt eigenständiges Szenario), haben Sie Optionen für die Art der Weiterleitung von Nachrichten, die zur Bearbeitung EOP durchlaufen, bevor sie an die Postfächer Ihrer Mitarbeiter weitergeleitet werden, um weiterhin die Vorteile Ihrer bestehenden Infrastruktur nutzen zu können.
  
Sie können eine benutzerdefinierte Mail-Weiterleitung konfigurieren, um Ihr Massaging an Ihre Unternehmensanforderung anzupassen. Angenommen, Sie möchten alle ausgehenden Nachrichten durch eine Richtlinienprüfungsvorrichtung leiten. 
  
## <a name="working-with-messages-and-message-access-options"></a>Arbeiten mit Nachrichten und Nachrichtenzugangsoptionen

EOP bietet viel Flexibilität bezüglich der Weiterleitung Ihrer Nachrichten. In den folgenden Themen werden Schritte im Nachrichtenflussprozess erklärt.
  
[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Beschreibt die verzeichnisbasierte Edge-Blockierung, die es Ihnen ermöglicht, Nachrichten für ungültige Empfänger am Dienstnetzwerkumkreis abzulehnen. 
  
[View or Edit Managed Domains in EOP](http://technet.microsoft.com/library/69523bec-07ee-46f9-ae08-40437e39b87c.aspx) beschreibt die Verwaltung von Domänen, die mit Ihrem EOP-Dienst verbunden sind. 
  
Wenn Sie Ihrer Organisation Unterdomänen hinzufügen, können Sie auch diese mit dem EOP-Dienst verwalten. Weitere Informationen zu Unterdomänen finden Sie unter [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).
  
Unter [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) erhalten Sie eine Einführung in Connectors und erfahren, wie diese zum Anpassen von E-Mail-Routing verwendet werden können. Dazu gehören Szenarien zur Gewährleistung sicherer Kommunikation mit einer Partnerorganisation sowie das Einrichten eines Smarthosts. 
  
Um sicherzustellen, dass junk-e-Mail-ordnungsgemäß an die Junk-e-Mail-Ordner des Benutzers weitergeleitet wird, müssen Sie einige Konfigurationsschritte ausführen. Diese werden in [Stellen Sie sicher, dass Spam an die Junk-e-Mail-Ordner des Benutzers geleitet wird](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)ausführlich beschrieben. Wenn Sie nicht Nachrichten des Benutzers Junk-e-Mail-Ordner verschieben möchten, können Sie eine andere Aktion durch Ihre inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole bearbeiten wählen. Weitere Informationen finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](../configure-your-spam-filter-policies.md).
  
## <a name="verify-mail-flow"></a>Überprüfen des Nachrichtenflusses

Weitere Informationen zum Überprüfen des EOP-Setups und der Connectorkonfiguration finden Sie im Abschnitt "Woher wissen Sie, dass diese Aufgabe erfolgreich war?" unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md). 
  
[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) liefert Anweisungen, um zu testen, dass Ihr Nachrichtenfluss richtig konfiguriert ist. 
  

