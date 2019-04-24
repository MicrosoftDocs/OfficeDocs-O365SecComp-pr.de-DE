---
title: DSGVO für lokale Dateifreigaben
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Erfahren Sie, wie Sie mit DSGVO-Anforderungen bei lokalen Windows Server-Dateifreigaben umgehen.
ms.openlocfilehash: 14af73a2ff2a162f2f3e621c2efeb5d9050c069a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255223"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a><span data-ttu-id="76393-103">DSGVO für lokale Windows Server-Dateifreigaben</span><span class="sxs-lookup"><span data-stu-id="76393-103">GDPR for on-premises Windows Server file shares</span></span>

<span data-ttu-id="76393-104">Folgende grundlegende Vorgehensweise wird für Dateifreigaben empfohlen:</span><span class="sxs-lookup"><span data-stu-id="76393-104">The basic recommended approach for file shares is:</span></span>

-   <span data-ttu-id="76393-105">Verwenden Sie Azure Information Protection, um vertrauliche Daten zu beschriften.</span><span class="sxs-lookup"><span data-stu-id="76393-105">Use Azure Information Protection to label sensitive data.</span></span>

-   <span data-ttu-id="76393-106">Verwenden Sie den Azure Information Protection-Scanner, um Daten zu finden.</span><span class="sxs-lookup"><span data-stu-id="76393-106">Use Azure Information Protection scanner to find data.</span></span>

<span data-ttu-id="76393-107">Die empfohlene Vorgehensweise für  Dateifreigaben umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="76393-107">The recommended approach for files shares includes these steps:</span></span>

1.  <span data-ttu-id="76393-108">**Installieren und konfigurieren Sie den Azure Information Protection-Scanner.**</span><span class="sxs-lookup"><span data-stu-id="76393-108">**Install and configure Azure Information Protection scanner.**</span></span>

    -   <span data-ttu-id="76393-109">Entscheiden Sie, welche vertraulichen Datentypen Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="76393-109">Decide which sensitive data types to use.</span></span>

    -   <span data-ttu-id="76393-110">Geben Sie die lokalen Ordner und Netzwerkfreigaben an, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="76393-110">Specify local folders and network shares to use.</span></span>

2.  <span data-ttu-id="76393-111">**Führen Sie einen Suchzyklus durch.**</span><span class="sxs-lookup"><span data-stu-id="76393-111">**Complete a discovery cycle.**</span></span>

    -   <span data-ttu-id="76393-112">Führen Sie den Scanner im Suchmodus aus und überprüfen Sie die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="76393-112">Run the scanner in discovery mode and validate the findings.</span></span>

    -   <span data-ttu-id="76393-113">Falls erforderlich, optimieren Sie die Bedingungen und vertraulichen Datentypen.</span><span class="sxs-lookup"><span data-stu-id="76393-113">If needed, optimize the conditions and sensitive information types.</span></span>

    -   <span data-ttu-id="76393-114">Bewerten Sie die erwarteten Auswirkungen einer automatischen Anwendung von Beschriftungen.</span><span class="sxs-lookup"><span data-stu-id="76393-114">Assess the expected impact of automatically applying labels.</span></span>

3.  <span data-ttu-id="76393-115">**Führen Sie den Azure Information Protection-Scanner aus, um Beschriftungen für berechtigende Dokumente anzuwenden**.</span><span class="sxs-lookup"><span data-stu-id="76393-115">**Run the Azure Information Protection scanner to apply labels to qualifying documents**.</span></span>

4.  <span data-ttu-id="76393-116">**Zum Schutz:**</span><span class="sxs-lookup"><span data-stu-id="76393-116">**For protection:**</span></span>

    -   <span data-ttu-id="76393-117">Konfigurieren Sie Regeln zum Schutz vor Datenverlust in Exchange, um Dokumente mit der gewünschten Beschriftung zu schützen.</span><span class="sxs-lookup"><span data-stu-id="76393-117">Configure Exchange data loss prevention rules to protect documents with the desired label.</span></span>

    -   <span data-ttu-id="76393-118">Beschränken Sie mithilfe von Berechtigungen, wer auf Dateien zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="76393-118">Be sure to use permissions to limit who can access files.</span></span>

5.  <span data-ttu-id="76393-119">**Integrieren Sie zur Überwachung Windows Server-Protokolle mit einem SIEM-Tool.**</span><span class="sxs-lookup"><span data-stu-id="76393-119">**For monitoring, integrate Windows Server logs with a SIEM tool.**</span></span>

    -   <span data-ttu-id="76393-p101">Verwenden Sie den Azure Information Protection-Scanner, um personenbezogene Daten für Anfragen von betroffenen Personen zu finden. Sie können auch eine SharePoint Server-Suche konfigurieren, um Dateifreigaben zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="76393-p101">To find personal data for data subject requests, use Azure Information Protection scanner. You can also configure SharePoint Server search to crawl file shares.</span></span>

<span data-ttu-id="76393-122">Weitere Informationen über die Verwendung des Azure Information Protection-Scanners zum Suchen und Beschriften von personenbezogenen Daten finden Sie im Microsoft GDPR Data Discovery Toolkit unter [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>).</span><span class="sxs-lookup"><span data-stu-id="76393-122">For more information on using Azure Information Protection scanner to find and label personal data, see the Microsoft GDPR Data Discovery Toolkit at [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>).</span></span>

<span data-ttu-id="76393-p102">Informationen über die Konfiguration des Scanners für Bedingungen und die Verwendung der vertraulichen Datentypen für die Verhinderung von Datenverlust in Office 365 finden Sie unter [So konfigurieren Sie Bedingungen für die automatische und empfohlene Klassifizierung von Azure Information Protection](https://docs.microsoft.com/de-DE/information-protection/deploy-use/configure-policy-classification). Beachten Sie, dass neue vertrauliche Datentypen in Office 365 nicht sofort für die Verwendung mit dem Scanner zur Verfügung stehen und dass benutzerdefinierte vertrauliche Datentypen nicht mit dem Scanner verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="76393-p102">For information on configuring the scanner for conditions and using the Office 365 data loss prevention (DLP) sensitive information types, see [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/de-DE/information-protection/deploy-use/configure-policy-classification). Note that new Office 365 sensitive information types will not be immediately available to use with the scanner and custom sensitive information types cannot be used with the scanner.</span></span>
