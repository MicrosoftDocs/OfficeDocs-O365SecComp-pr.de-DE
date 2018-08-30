---
title: Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung in Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Um IP-Adressen auf einfache Weise zu ermitteln, die Sie in Office 365 Cloud App-Sicherheit, wie Ihre physischen Büroraums IP-Adressen verwenden, können Sie Gruppen von IP-Adressbereiche einrichten.
ms.openlocfilehash: 76cb9625a46d1f5eceaab696de5dcbb72f4d2b47
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528872"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a><span data-ttu-id="cfda2-103">Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung in Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cfda2-103">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="cfda2-104">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="cfda2-104">****Evaluation** \>**</span></span>|<span data-ttu-id="cfda2-105">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="cfda2-105">****Planning** \>**</span></span>|<span data-ttu-id="cfda2-106">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="cfda2-106">****Deployment** \>**</span></span>|<span data-ttu-id="cfda2-107">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="cfda2-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="cfda2-108">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="cfda2-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="cfda2-109">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="cfda2-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="cfda2-110">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="cfda2-110">You are here!</span></span>  <br/> [<span data-ttu-id="cfda2-111">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="cfda2-111">Next steps</span></span>](#next-steps) <br/> |[<span data-ttu-id="cfda2-112">Starten Sie die Nutzung</span><span class="sxs-lookup"><span data-stu-id="cfda2-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="cfda2-p101">Um IP-Adressen auf einfache Weise zu ermitteln, die Sie in Office 365 Cloud App-Sicherheit, wie Ihre physischen Büroraums IP-Adressen verwenden, können Sie Gruppen von IP-Adressbereiche einrichten. Definieren diese Bereiche können markieren und kategorisiert werden können, und klicken Sie dann können Sie Tags und Kategorien auf anpassen, wie Ihre Aktivität Protokolle und Warnungen angezeigt und untersucht werden.</span><span class="sxs-lookup"><span data-stu-id="cfda2-p101">To easily identify sets of IP addresses that you'll use in Office 365 Cloud App Security, such as your physical office IP addresses, you can set up groups of IP address ranges. Defining these ranges lets you tag and categorize them, and then you can use tags and categories to customize how your activity logs and alerts are displayed and investigated.</span></span>
  
<span data-ttu-id="cfda2-p102">Jede Gruppe von IP-Adressbereichen kann markiert werden mit Tag-Namen, die Sie auswählen, und klicken Sie dann die Tags können kategorisiert werden basierend auf eine Standardliste von IP-Kategorien (beispielsweise Corporate, Administrative, Risky und VPN). Sowohl IPv4 als auch IPv6-Adressen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cfda2-p102">Each group of IP ranges can be tagged with tag names that you choose, and then the tags can be categorized based on a default list of IP categories (such as Corporate, Administrative, Risky, and VPN). Both IPv4 and IPv6 addresses are supported.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cfda2-p103">Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der Verfahren in diesem Artikel werden. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="cfda2-p103">You must be a global administrator or security administrator to perform the procedures in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a><span data-ttu-id="cfda2-119">Einrichten eines IP-Adressbereichs in Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cfda2-119">To set up an IP address range in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="cfda2-p104">Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.)</span><span class="sxs-lookup"><span data-stu-id="cfda2-p104">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="cfda2-122">In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="cfda2-122">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="cfda2-123">Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="cfda2-123">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="cfda2-125">Klicken Sie auf der rechten oberen Ecke der Seite, auf **Einstellungen** \> **IP-Adressbereiche**.</span><span class="sxs-lookup"><span data-stu-id="cfda2-125">On the upper right of the page, click **Settings** \> **IP address ranges**.</span></span>
    
    ![Wählen Sie in Office 365-Cloud-App-Sicherheit Einstellungen für den Einstellungen für Ihr System und Zugriff auf](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)
  
5. <span data-ttu-id="cfda2-127">Klicken Sie auf die Schaltfläche neu, die ein Pluszeichen (+) ähnelt ( **+**).</span><span class="sxs-lookup"><span data-stu-id="cfda2-127">Click the new button, which resembles a plus sign ( **+**).</span></span>
    
6. <span data-ttu-id="cfda2-128">Geben Sie im Fenster **neuen IP-Adressbereich** die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="cfda2-128">In the **New IP address range** window, specify the following values:</span></span> 
    
|<span data-ttu-id="cfda2-129">**Webfeld- oder**</span><span class="sxs-lookup"><span data-stu-id="cfda2-129">**Field or list**</span></span>|<span data-ttu-id="cfda2-130">**Nächste Schritte**</span><span class="sxs-lookup"><span data-stu-id="cfda2-130">**What to do**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cfda2-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="cfda2-131">**Name**</span></span> <br/> |<span data-ttu-id="cfda2-p105">Verwenden Sie dieses Feld zum Verwalten von IP-Adressbereich und Einstellungen. (Dieser Wert in Aktivitäten Protokolle werden nicht angezeigt werden.)</span><span class="sxs-lookup"><span data-stu-id="cfda2-p105">Use this field to manage your IP address range and settings. (You won't see this value in activities logs.)</span></span>  <br/> |
|<span data-ttu-id="cfda2-134">**IP-Adressbereiche**</span><span class="sxs-lookup"><span data-stu-id="cfda2-134">**IP address ranges**</span></span> <br/> |<span data-ttu-id="cfda2-p106">Geben Sie einen Bereich, mithilfe der Netzwerk-Präfix-Notation (auch bekannt als CIDR-Notation). 192.168.1.0/27 umfasst beispielsweise den Wertebereich 192.168.1.0 bis 192.168.1.31 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="cfda2-p106">Specify a range, using network prefix notation (also known as CIDR notation). For example, 192.168.1.0/27 includes the range of values 192.168.1.0 through 192.168.1.31 (inclusive).</span></span>  <br/> |
|<span data-ttu-id="cfda2-137">**Speicherort** und den **Internetdienstanbieter registriert**</span><span class="sxs-lookup"><span data-stu-id="cfda2-137">**Location** and **Registered ISP**</span></span> <br/> |<span data-ttu-id="cfda2-p107">Geben Sie den Speicherort und den Internetdienstanbieter (ISP) für den IP-Adressbereich ein. Dies überschreibt für die Adressen definierten öffentlichen Felder die kann bei Fällen hilfreich sein, wie eine IP-Adresse ist, gilt als öffentlich in Irland, jedoch ist tatsächlich in den USA</span><span class="sxs-lookup"><span data-stu-id="cfda2-p107">Specify the location and Internet Service Provider (ISP) for the IP address range. This overrides the public fields defined for the addresses, which is helpful for cases, such as an IP address is that is considered publicly to be in Ireland but is actually in the U.S.</span></span>  <br/> |
|<span data-ttu-id="cfda2-140">**Tags**</span><span class="sxs-lookup"><span data-stu-id="cfda2-140">**Tags**</span></span> <br/> |<span data-ttu-id="cfda2-p108">Verwenden Sie Tags zum Benennen von Ihren Gruppen von IP-Adressen. (Im Gegensatz zu Sie im Feld Name wird Tags in Aktivitätsprotokolle angezeigt.) Geben Sie ein Wort oder Ausdruck, die Sie für ein Tag verwenden möchten. Sie können beliebig viele Tags, wie Sie für jede IP-Adressbereich hinzufügen. Und wenn Sie bereits ein Tag eingerichtet haben, und Sie diese IP-Adressbereich hinzufügen möchten, wählen Sie ihn aus der Liste der aktuellen Tags, die angezeigt werden, wie Sie mit der Eingabe beginnen.</span><span class="sxs-lookup"><span data-stu-id="cfda2-p108">Use tags to name your groups of IP addresses. (Unlike the Name field, you will see Tags in activity logs.) Type a word or phrase that you want to use for a tag. You can add as many tags as you like for each IP address range. And if you've already set up a tag and you want to add this IP address range to it, choose it from the list of current tags that appear as you start typing.</span></span>  <br/> |
|<span data-ttu-id="cfda2-145">**Kategorie**</span><span class="sxs-lookup"><span data-stu-id="cfda2-145">**Category**</span></span> <br/> | <span data-ttu-id="cfda2-p109">Zuweisen von Kategorien zu Ihrer Kategorien zu erleichtern, Aktivitäten zu erkennen, die von bestimmten IP-Adressen stammen. Wählen Sie die folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="cfda2-p109">Assign categories to your tags to make it easier to recognize activities that come from certain IP addresses. Choose from the following options:  </span></span><br/> <span data-ttu-id="cfda2-148">**Administrative** Alle IP-Adressen Ihrer Admins.</span><span class="sxs-lookup"><span data-stu-id="cfda2-148">**Administrative** All of the IP addresses of your admins.</span></span>  <br/> <span data-ttu-id="cfda2-149">**Cloud-Anbieter** Die IP-Adresse Ihres Proxys in der Cloud.</span><span class="sxs-lookup"><span data-stu-id="cfda2-149">**Cloud provider** The IP address of your proxy in the cloud.</span></span>  <br/> <span data-ttu-id="cfda2-150">**Im Unternehmen** Alle IP-Adressen in Ihrem internen Netzwerk, Ihren Zweigstellen und Ihre wechselnden Arbeitsplätzen Wi-Fi-Adressen.</span><span class="sxs-lookup"><span data-stu-id="cfda2-150">**Corporate** All of the IP addresses in your internal network, your branch offices, and your Wi-Fi roaming addresses.</span></span>  <br/> <span data-ttu-id="cfda2-p110">**Riskant.** IP-Adressen, die Sie berücksichtigen riskant sein wie verdächtigen IP-Adressen in der Vergangenheit IP-Adressen in Ihrer Mitbewerber Netzwerken gesehen haben und so weiter. Standardmäßig enthält die Kategorien riskant zwei IP-Tags: **anonyme Proxy** und **Tor**</span><span class="sxs-lookup"><span data-stu-id="cfda2-p110">**Risky** Any IP addresses that you consider to be risky, such as suspicious IP addresses you've seen in the past, IP addresses in your competitors' networks, and so on. By default, the Risky categories includes two IP tags: **Anonymous proxy** and **Tor**</span></span> <br/> <span data-ttu-id="cfda2-153">**VPN** IP-Adressen, die Ihre Mitarbeiter remote verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfda2-153">**VPN** Any IP addresses that your remote workers use.</span></span>  <br/> |
   
7. <span data-ttu-id="cfda2-154">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="cfda2-154">Choose **Save**.</span></span>
    
<span data-ttu-id="cfda2-155">Lassen Sie nach dem Einrichten Ihrer IP-Adressbereiche, beachten Sie, dass diese Änderungen nur zukünftige Ereignisse betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="cfda2-155">After you set up your IP address ranges, keep in mind that only future events are affected by these changes.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="cfda2-156">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="cfda2-156">Next steps</span></span>

- [<span data-ttu-id="cfda2-157">Aktivität Richtlinien und Warnungen</span><span class="sxs-lookup"><span data-stu-id="cfda2-157">Activity policies and alerts</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="cfda2-158">Anomalie Erkennungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="cfda2-158">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="cfda2-159">Integrieren von Ihrem Server SIEM</span><span class="sxs-lookup"><span data-stu-id="cfda2-159">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="cfda2-160">Lesen Sie und führen Sie einer Aktion Warnungen in Office 365-Cloud-App-Sicherheit aus</span><span class="sxs-lookup"><span data-stu-id="cfda2-160">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    

