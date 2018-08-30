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
ms.openlocfilehash: ff5284eafe01a3887fa69fde2b5bcd023ee391db
ms.sourcegitcommit: 285c58a371e6ab82c40fac3f24530cf3b09d0175
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2018
ms.locfileid: "23002142"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="4cc44-104">Nachrichtenfluss in EOP</span><span class="sxs-lookup"><span data-stu-id="4cc44-104">Mail flow in EOP</span></span>

<span data-ttu-id="4cc44-p102">Als ein Exchange Online Protection (EOP) Kunde werden alle Nachrichten, die an Ihre Organisation gesendet werden, durch EOP geleitet, bevor die Mitarbeiter sie sehen. Ob Sie alle Ihre Postfächer in der Cloud mit Exchange Online hosten oder ob Sie Ihre Postfächer vor Ort hosten (genannt eigenständiges Szenario), haben Sie Optionen für die Art der Weiterleitung von Nachrichten, die zur Bearbeitung EOP durchlaufen, bevor sie an die Postfächer Ihrer Mitarbeiter weitergeleitet werden, um weiterhin die Vorteile Ihrer bestehenden Infrastruktur nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="4cc44-p102">As an Exchange Online Protection (EOP) customer, all messages sent to your organization pass through EOP before your workers see them. Whether you host all of your mailboxes in the cloud with Exchange Online, or you host your mailboxes on premises (called a standalone scenario), perhaps to continue taking advantage of your existing infrastructure, you have options about how to route messages that will pass through EOP for processing before they are routed to your worker inboxes.</span></span>
  
<span data-ttu-id="4cc44-p103">Sie können eine benutzerdefinierte Mail-Weiterleitung konfigurieren, um Ihr Massaging an Ihre Unternehmensanforderung anzupassen. Angenommen, Sie möchten alle ausgehenden Nachrichten durch eine Richtlinienprüfungsvorrichtung leiten.</span><span class="sxs-lookup"><span data-stu-id="4cc44-p103">You may want to configure custom mail routing to conform your messaging to a business requirement. For instance, you can pass all of your outbound mail through a policy-filtering appliance.</span></span> 
  
## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="4cc44-109">Arbeiten mit Nachrichten und Nachrichtenzugangsoptionen</span><span class="sxs-lookup"><span data-stu-id="4cc44-109">Working with messages and message access options</span></span>

<span data-ttu-id="4cc44-p104">EOP bietet viel Flexibilität bezüglich der Weiterleitung Ihrer Nachrichten. In den folgenden Themen werden Schritte im Nachrichtenflussprozess erklärt.</span><span class="sxs-lookup"><span data-stu-id="4cc44-p104">EOP offers a lot of flexibility in how your messages are routed. The following topics explain steps in the mail flow process.</span></span>
  
<span data-ttu-id="4cc44-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Beschreibt die verzeichnisbasierte Edge-Blockierung, die es Ihnen ermöglicht, Nachrichten für ungültige Empfänger am Dienstnetzwerkumkreis abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="4cc44-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span> 
  
<span data-ttu-id="4cc44-113">[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) beschreibt die Verwaltung von Domänen, die mit Ihrem EOP-Dienst verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="4cc44-113">[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) describes how to manage domains that are associated with your EOP service.</span></span> 
  
<span data-ttu-id="4cc44-p105">Wenn Sie Ihrer Organisation Unterdomänen hinzufügen, können Sie auch diese mit dem EOP-Dienst verwalten. Weitere Informationen zu Unterdomänen finden Sie unter [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span><span class="sxs-lookup"><span data-stu-id="4cc44-p105">If you add subdomains to your organization, your EOP service can help you manage these too. Learn more about subdomains at [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span></span>
  
<span data-ttu-id="4cc44-p106">Unter [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) erhalten Sie eine Einführung in Connectors und erfahren, wie diese zum Anpassen von E-Mail-Routing verwendet werden können. Dazu gehören Szenarien zur Gewährleistung sicherer Kommunikation mit einer Partnerorganisation sowie das Einrichten eines Smarthosts.</span><span class="sxs-lookup"><span data-stu-id="4cc44-p106">[Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) introduces connectors and shows how you can use them to customize mail routing. Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span> 
  
<span data-ttu-id="4cc44-p107">Um sicherzustellen, dass junk-e-Mail-ordnungsgemäß an die Junk-e-Mail-Ordner des Benutzers weitergeleitet wird, müssen Sie einige Konfigurationsschritte ausführen. Diese werden in [Stellen Sie sicher, dass Spam an die Junk-e-Mail-Ordner des Benutzers geleitet wird](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)ausführlich beschrieben. Wenn Sie nicht Nachrichten des Benutzers Junk-e-Mail-Ordner verschieben möchten, können Sie eine andere Aktion durch Ihre inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole bearbeiten wählen. Weitere Informationen finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](../configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="4cc44-p107">To ensure that junk email is routed correctly to each user's junk-email folder, you must perform a couple configuration steps. These are detailed in [Ensure that spam is routed to each user's Junk Email folder](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). If you do not want to move messages to each user's junk-email folder, you may choose another action by editing your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](../configure-your-spam-filter-policies.md).</span></span>
  
## <a name="verify-mail-flow"></a><span data-ttu-id="4cc44-122">Überprüfen des Nachrichtenflusses</span><span class="sxs-lookup"><span data-stu-id="4cc44-122">Verify mail flow</span></span>

<span data-ttu-id="4cc44-p108">Weitere Informationen zum Überprüfen des EOP-Setups und der Connectorkonfiguration finden Sie im Abschnitt "Woher wissen Sie, dass diese Aufgabe erfolgreich war?" unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md).</span><span class="sxs-lookup"><span data-stu-id="4cc44-p108">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](set-up-your-eop-service.md).</span></span> 
  
<span data-ttu-id="4cc44-125">[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) liefert Anweisungen, um zu testen, dass Ihr Nachrichtenfluss richtig konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="4cc44-125">[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) provides instructions for testing that your mail flow is set up correctly.</span></span> 
  

