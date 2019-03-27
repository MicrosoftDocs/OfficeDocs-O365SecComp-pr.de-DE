---
title: Exchange Online Protection im Überblick
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 01/31/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 1270a65f-ddc3-4430-b500-4d3a481efb1e
description: Microsoft Exchange Online Protection (EOP) ist ein cloudbasierter Dienst zum Filtern von E-Mails, mit dem Sie Ihre Organisation vor Spam und Schadsoftware schützen können.
ms.openlocfilehash: c8450d5204635788a044538d701e23f4f77d1e0f
ms.sourcegitcommit: c0d4fe3e43e22353f30034567ade28330266bcf7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2019
ms.locfileid: "30899944"
---
# <a name="exchange-online-protection-overview"></a><span data-ttu-id="4e599-103">Exchange Online Protection im Überblick</span><span class="sxs-lookup"><span data-stu-id="4e599-103">Exchange Online Protection overview</span></span>

<span data-ttu-id="4e599-p101">Microsoft Exchange Online Protection (EOP) ist ein cloudbasierter Dienst zum Filtern von E-Mails, mit dem Sie Ihre Organisation vor Spam und Schadsoftware schützen können. EOP kann die Verwaltung Ihrer Messagingumgebung und viele der beschwerlichen Aufgaben bei der Verwaltung lokaler Hardware und Software vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="4e599-p101">Microsoft Exchange Online Protection (EOP) is a cloud-based email filtering service that helps protect your organization against spam and malware, and includes features to safeguard your organization from messaging-policy violations. EOP can simplify the management of your messaging environment and alleviate many of the burdens that come with maintaining on-premises hardware and software.</span></span>
  
<span data-ttu-id="4e599-106">EOP kann in erster Linie über die folgenden Methoden für den Nachrichtenschutz eingesetzt werden:</span><span class="sxs-lookup"><span data-stu-id="4e599-106">The following are the primary ways you can use EOP for messaging protection:</span></span>
  
- <span data-ttu-id="4e599-107">**In einem eigenständigen Szenario** EOP bietet Cloud-basierten e-Mail-Schutz für Ihre lokale Microsoft Exchange Server 2013-Umgebung, Legacyversionen von Exchange Server oder für andere lokale SMTP-e-Mail-Lösungen.</span><span class="sxs-lookup"><span data-stu-id="4e599-107">**In a standalone scenario** EOP provides cloud-based email protection for your on-premises Microsoft Exchange Server 2013 environment, legacy Exchange Server versions, or for any other on-premises SMTP email solution.</span></span> 
    
- <span data-ttu-id="4e599-108">**Als Bestandteil von Microsoft Exchange Online** EOP schützt standardmäßig cloudgehostete Postfächer von Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4e599-108">**As a part of Microsoft Exchange Online** By default, EOP protects Microsoft Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="4e599-109">**In einer Hybridbereitstellung** kann EOP für den Schutz Ihrer Messagingumgebung und für die Steuerung von E-Mail-Routing konfiguriert werden, wenn Sie sowohl über lokale als auch über Cloud-Postfächer verfügen.</span><span class="sxs-lookup"><span data-stu-id="4e599-109">**In a hybrid deployment** EOP can be configured to protect your messaging environment and control mail routing when you have a mix of on-premises and cloud mailboxes.</span></span> 
    
## <a name="how-eop-works"></a><span data-ttu-id="4e599-110">Funktionsweise von EOP</span><span class="sxs-lookup"><span data-stu-id="4e599-110">How EOP works</span></span>

<span data-ttu-id="4e599-111">Die Funktionsweise von EOP lässt sich am besten an der Verarbeitung eingehender E-Mails veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="4e599-111">To understand how EOP works, it helps to see how it processes incoming email:</span></span>
  
![EOP-e-Mail-Verarbeitung](../media/EOP-email-processing.png)
  
<span data-ttu-id="4e599-113">Eine eingehende Nachricht durchläuft zunächst die Verbindungsfilterung, die den Ruf des Absenders überprüft und die Nachricht auf Schadsoftware überprüft.</span><span class="sxs-lookup"><span data-stu-id="4e599-113">An incoming message initially passes through connection filtering, which checks the sender's reputation and inspects the message for malware.</span></span> <span data-ttu-id="4e599-114">Die Mehrzahl der Spam-Mails wird an dieser Stelle angehalten und von EOP gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4e599-114">The majority of spam is stopped at this point and deleted by EOP.</span></span> <span data-ttu-id="4e599-115">Nachrichten werden durch die Richtlinienfilterung fortgesetzt, bei der Nachrichten anhand von benutzerdefinierten Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) ausgewertet werden, die Sie aus einer Vorlage erstellen oder erzwingen.</span><span class="sxs-lookup"><span data-stu-id="4e599-115">Messages continue through policy filtering, where messages are evaluated against custom mail flow rules (also known as transport rules) that you create or enforce from a template.</span></span> <span data-ttu-id="4e599-116">Sie können beispielsweise über eine Regel verfügen, die eine Benachrichtigung an einen Vorgesetzten sendet, wenn e-Mails von einem bestimmten Absender eingehen.</span><span class="sxs-lookup"><span data-stu-id="4e599-116">For example, you can have a rule that sends a notification to a manager when mail arrives from a specific sender.</span></span> <span data-ttu-id="4e599-117">(Datenverlust-Vermeidungs Überprüfungen treten auch an diesem Punkt auf, wenn Sie diese Funktion haben; weitere Informationen zur Verfügbarkeit von Funktionen finden Sie in der [Exchange Online Protection-Dienstbeschreibung](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Im nächsten Schritt werden Nachrichten durch Inhaltsfilterung geleitet, bei der Inhalte auf Terminologie oder gemeinsame Eigenschaften für Spam überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="4e599-117">(Data loss prevention checks also occur at this point, if you have that feature; for information about feature availability, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Next, messages pass through content filtering, where content is checked for terminology or properties common to spam.</span></span> <span data-ttu-id="4e599-118">Eine Nachricht, die vom Inhaltsfilter als Spam festgelegt wurde, kann je nach Ihren Einstellungen an den Junk-e-Mail-Ordner eines Benutzers oder an die Quarantäne gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e599-118">A message determined to be spam by the content filter can be sent to a user's Junk Email folder or to the quarantine, among other options, based on your settings.</span></span> <span data-ttu-id="4e599-119">Nachdem eine Nachricht alle diese Schutzebenen erfolgreich übergeben hat, wird Sie an den Empfänger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4e599-119">After a message passes all of these protection layers successfully, it's delivered to the recipient.</span></span>
  
### <a name="eop-datacenters"></a><span data-ttu-id="4e599-120">EOP-Datencenter</span><span class="sxs-lookup"><span data-stu-id="4e599-120">EOP datacenters</span></span>

<span data-ttu-id="4e599-p103">EOP wird in einem weltweiten Rechenzentrennetzwerk ausgeführt, das für eine optimale Verfügbarkeit entworfen wurde. Wenn ein Rechenzentrum ausfällt, werden E-Mails ohne jegliche Dienstunterbrechung automatisch an ein anderes Rechenzentrum weitergeleitet. Die Server in den einzelnen Rechenzentren akzeptieren Nachrichten in Ihrem Namen und trennen Ihre Organisation dadurch vom Internet. So wird die Last Ihrer Server gesenkt. Mit diesem hochverfügbaren Netzwerk kann Microsoft sicherstellen, dass E-Mails rasch an Ihre Organisation übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="4e599-p103">EOP runs on a worldwide network of datacenters that are designed to provide the best availability. For example, if a datacenter becomes unavailable, email messages are automatically routed to another datacenter without any interruption in service. Servers in each datacenter accept messages on your behalf, providing a layer of separation between your organization and the Internet, thereby reducing load on your servers. Through this highly available network, Microsoft can ensure that email reaches your organization in a timely manner.</span></span> 
  
<span data-ttu-id="4e599-p104">EOP führt einen Lastenausgleich zwischen Rechenzentren aus, jedoch nur innerhalb einer Region. Wenn Sie über eine Bereitstellung in einer bestimmten Region verfügen, werden alle Nachrichten mit dem E-Mail-Routing für diese Region verarbeitet. Die folgende Liste zeigt, wie regionales E-Mail-Routing für die EOP-Datencenter funktioniert:</span><span class="sxs-lookup"><span data-stu-id="4e599-p104">EOP performs load balancing between datacenters but only within a region. If you're provisioned in one region all your messages will be processed using the mail routing for that region. The following list shows the how regional mail routing works for the EOP datacenters:</span></span>
  
    
- <span data-ttu-id="4e599-128">In Europa, dem Nahen Osten und Afrika (EMEA) befinden sich alle Exchange Online-Postfächer in EMEA-Rechenzentren, und alle Nachrichten werden zur EOP-Filterung über EMEA-Rechenzentren geleitet.</span><span class="sxs-lookup"><span data-stu-id="4e599-128">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="4e599-129">In Asien-Pazifik (APAC) befinden sich alle Exchange Online-Postfächer in APAC-Rechenzentren, Nachrichten werden derzeit über APAC-Rechenzentren zur EOP-Filterung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="4e599-129">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, but messages are currently routed through APAC datacenters for EOP filtering.</span></span>

- <span data-ttu-id="4e599-130">In Amerika befinden sich alle Exchange Online-Postfächer in US-Rechenzentren, mit Ausnahme von Südamerika, in dem Datencenter in Brasilien und Chile verwendet werden, und in Kanada, in denen Rechenzentren in Kanada verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e599-130">In the Americas, all Exchange Online mailboxes are located in U.S. datacenters, with the exception of South America where datacenters in Brazil and Chile are used and in Canada where datacenters in Canada are used.</span></span> <span data-ttu-id="4e599-131">Alle e-Mail-Nachrichten, einschließlich Nachrichten für Kunden in Südamerika und Kanada, werden für EOP-Filterung über lokale Datencenter geroutet. quaratined-e-Mails werden im Datencenter gespeichert, in dem sich der Mandant befindet.</span><span class="sxs-lookup"><span data-stu-id="4e599-131">All email messages, including messages for customers in South America and Canada, are routed through local datacenters for EOP filtering; quaratined email is stored in the datacenter where the tenant is located.</span></span>
    
- <span data-ttu-id="4e599-132">In Europa, dem Nahen Osten und Afrika (EMEA) befinden sich alle Exchange Online-Postfächer in EMEA-Rechenzentren, und alle Nachrichten werden zur EOP-Filterung über EMEA-Rechenzentren geleitet.</span><span class="sxs-lookup"><span data-stu-id="4e599-132">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="4e599-133">In Asien-Pazifik (APAC) befinden sich alle Exchange Online-Postfächer in APAC-Rechenzentren, und Nachrichten werden derzeit über APAC-Rechenzentren zur EOP-Filterung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="4e599-133">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, and messages are currently routed through APAC datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="4e599-134">Alle Exchange Online-Postfächer für die Government Community Cloud (GCC) befinden sich in US-Rechenzentren, und alle Nachrichten werden zur EOP-Filterung über US-Rechenzentren geleitet.</span><span class="sxs-lookup"><span data-stu-id="4e599-134">For the Government Community Cloud (GCC), all Exchange Online mailboxes are located in U.S. datacenters and all messages are routed through U.S. datacenters for EOP filtering.</span></span>
    
## <a name="eop-plans-and-features"></a><span data-ttu-id="4e599-135">EOP-Dienste und -Funktionen</span><span class="sxs-lookup"><span data-stu-id="4e599-135">EOP plans and features</span></span>

<span data-ttu-id="4e599-136">Die folgenden EOP-Abonnementpläne sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="4e599-136">The following are the available EOP subscription plans:</span></span>
  
- <span data-ttu-id="4e599-137">**EOP als eigenständige Lösung** Hier schützt EOP Ihre lokalen Postfächer.</span><span class="sxs-lookup"><span data-stu-id="4e599-137">**EOP standalone** Where EOP protects your on-premises mailboxes.</span></span> 
    
- <span data-ttu-id="4e599-138">**EOP-Funktionen in Exchange Online** Hier schützt EOP Ihre cloudgehosteten Exchange Online-Postfächer.</span><span class="sxs-lookup"><span data-stu-id="4e599-138">**EOP features in Exchange Online** Where EOP protects your Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="4e599-139">**Exchange Enterprise CAL mit Diensten** Hier schützt EOP Ihre lokalen Postfächer wie EOP als eigenständige Lösung. Außerdem sind DLP-Funktionen (Data Loss Prevention, Verhinderung von Datenverlust) und eine Berichterstellung mithilfe von Webdiensten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4e599-139">**Exchange Enterprise CAL with Services** Where EOP protects your on-premises mailboxes, like EOP standalone, and includes data loss prevention (DLP) and reporting using web services.</span></span> 
    
<span data-ttu-id="4e599-140">Weitere Informationen zu Anforderungen, wichtigen Grenzwerten und Verfügbarkeit von Funktionen in allen EOP-Abonnementplänen finden Sie in der [Exchange Online Protection-Dienstbeschreibung](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span><span class="sxs-lookup"><span data-stu-id="4e599-140">For information about requirements, important limits, and feature availability across all EOP subscription plans, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span></span>
  
## <a name="setting-up-eop"></a><span data-ttu-id="4e599-141">Einrichten von EOP</span><span class="sxs-lookup"><span data-stu-id="4e599-141">Setting up EOP</span></span>

<span data-ttu-id="4e599-p106">EOP-Bereitstellungen können einfach sein. Dies gilt insbesondere für kleine Organisationen mit einer Handvoll Regeln für die Richtlinientreue. Verfügen Sie jedoch über eine große Organisation mit mehreren Domänen, benutzerdefinierten Richtlinienregeln oder Hybridnachrichtenübermittlung, kann die Einrichtung einen höheren Planungs- und Zeitaufwand erfordern.</span><span class="sxs-lookup"><span data-stu-id="4e599-p106">Setting up EOP can be simple, especially in the case of a small organization with a handful of compliance rules. However, if you have a large organization with multiple domains, custom compliance rules, or hybrid mail flow, set up can take more planning and time.</span></span>
  
<span data-ttu-id="4e599-144">Sollten Sie bereits EOP erworben haben, können Sie mit den Hinweisen unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md) sicherstellen, dass Sie alle für die Konfiguration von EOP zum Schutz Ihrer Nachrichtenumgebung erforderlichen Schritte ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="4e599-144">If you've already purchased EOP, see [Set up your EOP service](set-up-your-eop-service.md) to ensure that you complete all the steps necessary to configure EOP to protect your messaging environment.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="4e599-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4e599-145">For more information</span></span>

[<span data-ttu-id="4e599-146">EOP-Features</span><span class="sxs-lookup"><span data-stu-id="4e599-146">EOP features</span></span>](eop-features.md)
  
[<span data-ttu-id="4e599-147">EOP – Allgemeine häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="4e599-147">EOP general FAQ</span></span>](eop-general-faq.md)
  
[<span data-ttu-id="4e599-148">Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="4e599-148">EOP queued, deferred, and bounced messages FAQ</span></span>](eop-queued-deferred-and-bounced-messages-faq.md)
  
[<span data-ttu-id="4e599-149">Häufig gestellte Fragen zur delegierten Verwaltung</span><span class="sxs-lookup"><span data-stu-id="4e599-149">Delegated administration FAQ</span></span>](delegated-administration-faq.md)
  
[<span data-ttu-id="4e599-150">Verschieben von Domänen und Einstellungen zwischen EOP-Organisationen</span><span class="sxs-lookup"><span data-stu-id="4e599-150">Move domains and settings from one EOP organization to another EOP organization</span></span>](move-domains-and-settings-from-one-eop-organization-to-another-eop-organization.md)
  

