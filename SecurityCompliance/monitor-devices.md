---
title: Überwachen von Geräten in Microsoft 365 Security
description: Beschreibt, wie Sie Ihre Geräte sicher, auf dem neuesten Stand halten und potenzielle Bedrohungen in Ihrer Organisation erkennen können.
keywords: Sicherheit, Schadsoftware, Microsoft 365, M365, Sicherheitscenter, Überwachung, Bericht, Geräte
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: fea3f35e0fca3ccc8148d93b7a535c98dd2d32b9
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000528"
---
# <a name="monitor-devices-in-microsoft-365-security"></a><span data-ttu-id="c97fe-104">Überwachen von Geräten in Microsoft 365 Security</span><span class="sxs-lookup"><span data-stu-id="c97fe-104">Monitor devices in Microsoft 365 security</span></span>

<span data-ttu-id="c97fe-105">Halten Sie Ihre Geräte sicher, auf dem neuesten Stand und stellen Sie potenzielle Bedrohungen im Microsoft 365 Security Center vor.</span><span class="sxs-lookup"><span data-stu-id="c97fe-105">Keep your devices secure, up-to-date, and spot potential threats in the Microsoft 365 security center.</span></span>

## <a name="view-device-alerts"></a><span data-ttu-id="c97fe-106">Anzeigen von Geräte Warnungen</span><span class="sxs-lookup"><span data-stu-id="c97fe-106">View device alerts</span></span>

<span data-ttu-id="c97fe-107">Informieren Sie sich über aktuelle Warnungen zu Verstößen und anderen Bedrohungen auf Ihren Geräten von Windows Defender ATP (verfügbar mit einer E5-Lizenz).</span><span class="sxs-lookup"><span data-stu-id="c97fe-107">Get up-to-date alerts about breach activity and other threats on your devices from Windows Defender ATP (available with an E5 license).</span></span> <span data-ttu-id="c97fe-108">Microsoft 365 Security Center verfügt über mehrere Karten, mit denen Sie diese Warnungen in Abhängigkeit von Ihrem bevorzugten Workflow effektiv überwachen können.</span><span class="sxs-lookup"><span data-stu-id="c97fe-108">Microsoft 365 security center has several cards that allow you to effectively monitor these alerts at a high-level, depending on your preferred workflow.</span></span>

### <a name="monitor-high-impact-alerts"></a><span data-ttu-id="c97fe-109">Überwachen von Warnungen mit hoher Auswirkung</span><span class="sxs-lookup"><span data-stu-id="c97fe-109">Monitor high-impact alerts</span></span>

<span data-ttu-id="c97fe-110">Jede Windows Defender-ATP-Warnung weist einen entsprechenden Schweregrad auf – hoch, Mittel, niedrig oder Informationswert –, der die potenziellen Auswirkungen auf Ihr Netzwerk angibt, wenn Sie unbeaufsichtigt bleiben.</span><span class="sxs-lookup"><span data-stu-id="c97fe-110">Each Windows Defender ATP alert has a corresponding severity—high, medium, low, or informational—that indicates its potential impact to your network if left unattended.</span></span>  

<span data-ttu-id="c97fe-111">Verwenden Sie die **Geräte Warnungs schwere** Karte, um sich gezielt auf schwerwiegende Warnungen zu konzentrieren, die möglicherweise sofort beantwortet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-111">Use the **Device alert severity** card to focus specifically on alerts that are more severe and might require immediate response.</span></span> <span data-ttu-id="c97fe-112">Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-112">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

![Schwerekarte für Geräte Warnungen](./media/security-docs/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a><span data-ttu-id="c97fe-114">Informationen zu Quellen von Warnungen</span><span class="sxs-lookup"><span data-stu-id="c97fe-114">Understand sources of alerts</span></span>

<span data-ttu-id="c97fe-115">Windows Defender ATP nutzt Daten aus einer Vielzahl von Sicherheitssensoren und Intelligence-Quellen, um Warnungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c97fe-115">Windows Defender ATP leverages data from a broad range of security sensors and intelligence sources to generate alerts.</span></span> <span data-ttu-id="c97fe-116">Sie können beispielsweise Erkennungsinformationen von Windows Defender Antivirus und Antischadsoftware von Drittanbietern sowie ihre eigenen benutzerdefinierten Bedrohungs Nachrichten verwenden, die über die Webdienst-API bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c97fe-116">For example, it can use detection information from Windows Defender Antivirus and third-party antimalware, as well as your own custom threat intelligence provided through the web service API.</span></span>

<span data-ttu-id="c97fe-117">Die Karte zur **Erkennung von Geräte Warnungen** zeigt die Verteilung der Warnungen nach Quelle.</span><span class="sxs-lookup"><span data-stu-id="c97fe-117">The **Device alert detection** sources card shows the distribution of alerts by source.</span></span> <span data-ttu-id="c97fe-118">Diese Karte kann Ihnen dabei helfen, Aktivitäten im Zusammenhang mit bestimmten Quellen, insbesondere ihren benutzerdefinierten Quellen nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-118">This card can help you track activity related to certain sources, particularly your custom sources.</span></span> <span data-ttu-id="c97fe-119">Sie können sich auch auf Warnungen konzentrieren, die von Sensoren stammen, die nicht so konfiguriert sind, dass Sie bösartige Aktivitäten oder Komponenten automatisch blockieren.</span><span class="sxs-lookup"><span data-stu-id="c97fe-119">You can also use this to focus on alerts coming from sensors that are not configured to automatically block malicious activity or components.</span></span>

![Geräte Warnungs-Erkennungsquellen Karte](./media/security-docs/device-alert-detection-sources.png)

<span data-ttu-id="c97fe-121">Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-121">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a><span data-ttu-id="c97fe-122">GrundLegendes zu den Arten von Bedrohungen, die Warnungen auslösen</span><span class="sxs-lookup"><span data-stu-id="c97fe-122">Understand the types of threats that trigger alerts</span></span>

<span data-ttu-id="c97fe-123">Windows Defender ATP sortiert jede Warnung in einer Kategorie, die eine bestimmte Stufe in der Angriffs Kette oder eine Art von Bedrohungs Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="c97fe-123">Windows Defender ATP sorts each alert into a category representing a certain stage in the attack chain or a type of threat component.</span></span> <span data-ttu-id="c97fe-124">Die erkannte Bedrohungsaktivität kann beispielsweise in "Lateral Movement" kategorisiert werden, um anzugeben, dass die Aktivität versucht hat, andere Geräte im Netzwerk zu erreichen, und die Wahrscheinlichkeit aufgetreten ist, nachdem Angreifer eine erste Stütze erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="c97fe-124">For example, detected threat activity might be categorized into “lateral movement” to indicate that the activity involved an attempt to reach other devices on the network and has likely occurred after attackers have gained an initial foothold.</span></span> <span data-ttu-id="c97fe-125">Wenn eine Bedrohungs Komponente erkannt wird, kann Sie entweder als "Schadsoftware" oder genauer als "Ransomware", "Diebstahl von Anmeldeinformationen" oder anderen Arten von böswilliger oder unerwünschter Software klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c97fe-125">When detected, a threat component might either be classified broadly as “malware” or more specifically as “ransomware”, “credential stealing” or other types of malicious or unwanted software.</span></span>

<span data-ttu-id="c97fe-126">Die Karte für die **Geräte Bedrohungskategorien** zeigt die Verteilung von Warnungen in diese Kategorien an.</span><span class="sxs-lookup"><span data-stu-id="c97fe-126">The **Device threat categories** card shows the distribution of alerts into these categories.</span></span> <span data-ttu-id="c97fe-127">Sie können diese Informationen verwenden, um die Bedrohungsaktivität zu identifizieren, wie beispielsweise Versuche zum Diebstahl von Anmeldeinformationen, die sich im Vergleich zu den versuchen bei Social Engineering zum Beispiel erheblich auswirken können.</span><span class="sxs-lookup"><span data-stu-id="c97fe-127">You can use this information to identify threat activity, such as attempts at credential theft, which can have more significant impact compared to attempts at social engineering, for example.</span></span> <span data-ttu-id="c97fe-128">Sie können dies auch verwenden, um potenziell zerstörerische Bedrohungen wie Ransomware zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-128">You can also use this to monitor for potentially destructive threats like ransomware.</span></span>

![Karte für Geräte Bedrohungskategorien](./media/security-docs/device-threat-categories.png)

### <a name="monitor-active-alerts"></a><span data-ttu-id="c97fe-130">Überwachen aktiver Warnungen</span><span class="sxs-lookup"><span data-stu-id="c97fe-130">Monitor active alerts</span></span>

<span data-ttu-id="c97fe-131">Die **Geräte Warnungsstatus** Karte gibt die Anzahl der Warnungen an, die nicht aufgelöst wurden und möglicherweise Aufmerksamkeit erfordern.</span><span class="sxs-lookup"><span data-stu-id="c97fe-131">The **Device alert status** card indicates the number of alerts that have not been resolved and might require attention.</span></span> <span data-ttu-id="c97fe-132">Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-132">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

![Geräte Warnungsstatus Karte](./media/security-docs/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a><span data-ttu-id="c97fe-134">Überwachen der Klassifizierung aufgelöster Warnungen</span><span class="sxs-lookup"><span data-stu-id="c97fe-134">Monitor classification of resolved alerts</span></span>

<span data-ttu-id="c97fe-135">Wenn Sie eine Windows Defender-ATP-Warnung auflösen, können Ihre Sicherheitsmitarbeiter angeben, ob eine Warnung wie folgt überprüft wurde:</span><span class="sxs-lookup"><span data-stu-id="c97fe-135">When resolving a Window Defender ATP alert, your security staff can specify whether an alert has been verified as:</span></span>

* <span data-ttu-id="c97fe-136">Eine echte Warnung, die tatsächliche Verletzungs Aktivität oder Bedrohungs Komponenten identifiziert</span><span class="sxs-lookup"><span data-stu-id="c97fe-136">A true alert that identifies actual breach activity or threat components</span></span>
* <span data-ttu-id="c97fe-137">Falsche Warnung, die normale Aktivität falsch erkannt hat</span><span class="sxs-lookup"><span data-stu-id="c97fe-137">A false alert that has incorrectly detected normal activity</span></span>

<span data-ttu-id="c97fe-138">Auf der **Device Alert** -Klassifikations Karte wird angezeigt, ob Ihre aufgelöste Warnungen als wahr oder falsch eingestuft wurden.</span><span class="sxs-lookup"><span data-stu-id="c97fe-138">The **Device alert classification** card shows whether your resolved alerts have been classified as true or false alerts.</span></span> <span data-ttu-id="c97fe-139">Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-139">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

<span data-ttu-id="c97fe-140">Hinweis: in einigen Fällen sind Klassifizierungsinformationen für bestimmte Warnungen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c97fe-140">Note: In some cases, classification information is unavailable for certain alerts.</span></span>

![Geräte Warnungs-Klassifikations Karte](./media/security-docs/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a><span data-ttu-id="c97fe-142">Überwachen der Ermittlung aufgelöster Warnungen</span><span class="sxs-lookup"><span data-stu-id="c97fe-142">Monitor determination of resolved alerts</span></span>

<span data-ttu-id="c97fe-143">Zusätzlich zur Klassifizierung, ob eine Warnung während der Auflösung true oder false ist, können Ihre Sicherheitsmitarbeiter eine Bestimmung bereitstellen, die angibt, welche Art von normaler oder bösartiger Aktivität während der Überprüfung der Warnung gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c97fe-143">In addition to classifying whether an alert is true or false during resolution, your security staff can provide a determination, indicating the type of normal or malicious activity that was found while validating the alert.</span></span>

<span data-ttu-id="c97fe-144">Auf der **Geräte Warnungs Findungs** Karte wird die für jede Warnung vorgesehene Bestimmung angezeigt, insbesondere:</span><span class="sxs-lookup"><span data-stu-id="c97fe-144">The **Device alert determination** card shows the determination provided for each alert, specifically:</span></span>

* <span data-ttu-id="c97fe-145">**Apt** – Advanced persistent Threat, die darauf hinweist, dass die erkannte Aktivität oder Bedrohungs Komponente Teil einer ausgeklügelten Verletzung ist, die dazu dient, im betroffenen Netzwerk Fuß zu fassen</span><span class="sxs-lookup"><span data-stu-id="c97fe-145">**APT** – advanced persistent threat, indicating that the detected activity or threat component is part of a sophisticated breach designed to gain a foothold in the affected network</span></span>  
* <span data-ttu-id="c97fe-146">**Schadsoftware** – Schadsoftware oder Code</span><span class="sxs-lookup"><span data-stu-id="c97fe-146">**Malware** – malicious file or code</span></span>
* <span data-ttu-id="c97fe-147">**Sicherheitspersonal** – normale Aktivitäten des Sicherheitspersonals</span><span class="sxs-lookup"><span data-stu-id="c97fe-147">**Security personnel** – normal activity performed by security staff</span></span>
* <span data-ttu-id="c97fe-148">**Sicherheitstests** – Aktivitäten oder Komponenten zur Simulation von tatsächlichen Bedrohungen und erwarteten Sicherheitssensoren und Warnungen generieren</span><span class="sxs-lookup"><span data-stu-id="c97fe-148">**Security testing** – activity or components designed to simulate actual threats and expected to trigger security sensors and generate alerts</span></span>
* <span data-ttu-id="c97fe-149">**Unerwünschte Software** – apps und andere Software, die nicht als bösartig gelten, aber sonst gegen Richtlinien oder akzeptable Nutzungsstandards verstoßen</span><span class="sxs-lookup"><span data-stu-id="c97fe-149">**Unwanted software** – apps and other software that are not considered malicious, but otherwise violate policy or acceptable use standards</span></span>
* <span data-ttu-id="c97fe-150">**Andere** – jede andere Bestimmung, die nicht unter die angegebenen Typen fällt</span><span class="sxs-lookup"><span data-stu-id="c97fe-150">**Others** – any other determination that does not fall under the provided types</span></span>

<span data-ttu-id="c97fe-151">Von dieser Karte aus können Sie weitere Informationen im Windows Defender Security Center anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-151">From this card, you can view more information in Windows Defender security center.</span></span>

![Geräte Warnungs Findungs Karte](./media/security-docs/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a><span data-ttu-id="c97fe-153">Verstehen der gefährdeten Geräte</span><span class="sxs-lookup"><span data-stu-id="c97fe-153">Understand which devices are at risk</span></span>

<span data-ttu-id="c97fe-154">**Geräteschutz** zeigt die Risikostufe für Geräte an.</span><span class="sxs-lookup"><span data-stu-id="c97fe-154">**Device protection** shows the risk level for devices.</span></span> <span data-ttu-id="c97fe-155">Die Risikostufe basiert auf Faktoren wie Typ und Schweregrad der Warnungen auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="c97fe-155">The risk level is based on factors such as the type and severity of alerts on the device.</span></span>

![Geräteschutz Karte](./media/security-docs/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a><span data-ttu-id="c97fe-157">Überwachen und melden des Status von InTune-verwalteten Geräten</span><span class="sxs-lookup"><span data-stu-id="c97fe-157">Monitor and report status of Intune-managed devices</span></span>

<span data-ttu-id="c97fe-158">Die folgenden Überwachungen und Berichte enthalten Daten von Geräten, die in InTune registriert sind.</span><span class="sxs-lookup"><span data-stu-id="c97fe-158">The following monitoring and reports contain data from devices enrolled in Intune.</span></span> <span data-ttu-id="c97fe-159">Daten von nicht registrierten Geräten sind nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="c97fe-159">Data from unenrolled devices is not included.</span></span> <span data-ttu-id="c97fe-160">Nur globale Administratoren können diese Karten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-160">Only Global Administrators can view these cards.</span></span>

<span data-ttu-id="c97fe-161">InTune-Daten für registrierte Geräte umfassen:</span><span class="sxs-lookup"><span data-stu-id="c97fe-161">Intune enrolled device data includes:</span></span>

* <span data-ttu-id="c97fe-162">Geräte Konformität</span><span class="sxs-lookup"><span data-stu-id="c97fe-162">Device compliance</span></span>
* <span data-ttu-id="c97fe-163">Geräte mit aktiver Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="c97fe-163">Devices with active malware</span></span>
* <span data-ttu-id="c97fe-164">Arten von Schadsoftware auf Geräten</span><span class="sxs-lookup"><span data-stu-id="c97fe-164">Types of malware on devices</span></span>
* <span data-ttu-id="c97fe-165">Schadsoftware auf Geräten</span><span class="sxs-lookup"><span data-stu-id="c97fe-165">Malware on devices</span></span>
* <span data-ttu-id="c97fe-166">Geräte mit Schadsoftware-Entdeckungen</span><span class="sxs-lookup"><span data-stu-id="c97fe-166">Devices with malware detections</span></span>
* <span data-ttu-id="c97fe-167">Benutzer mit Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="c97fe-167">Users with malware detections</span></span>

### <a name="monitor-device-compliance"></a><span data-ttu-id="c97fe-168">Überwachen der Geräte Konformität</span><span class="sxs-lookup"><span data-stu-id="c97fe-168">Monitor device compliance</span></span>

<span data-ttu-id="c97fe-169">**Device Compliance** zeigt, wie viele Geräte, die in InTune registriert sind, Konfigurationsrichtlinien einhalten.</span><span class="sxs-lookup"><span data-stu-id="c97fe-169">**Device compliance** shows how many devices that are enrolled in Intune comply with configuration policies.</span></span>

![Geräte Konformitäts Karte](./media/security-docs/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a><span data-ttu-id="c97fe-171">Erkennen von Geräten mit Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="c97fe-171">Discover devices with malware detections</span></span>

<span data-ttu-id="c97fe-172">**Geräte-Malware** -Entdeckungen bieten die Anzahl von InTune-Geräten, die aufgrund ausstehender Aktionen nicht vollständig aufgelöst wurden – ein Neustart, eine vollständige Überprüfung oder manuelle Benutzeraktionen – oder wenn die Behebungsaktion nicht erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c97fe-172">**Device malware detections** provides the number of Intune enrolled devices with malware that have not been fully resolved due to pending actions—a restart, a full scan or manual user actions—or if the remediation action did not complete successfully.</span></span>

![Geräte-Malware-Erkennungskarte](./media/security-docs/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a><span data-ttu-id="c97fe-174">GrundLegendes zu den festgestellten Arten</span><span class="sxs-lookup"><span data-stu-id="c97fe-174">Understand the types of malware detected</span></span>

<span data-ttu-id="c97fe-175">**Arten von Schadsoftware auf Geräten** zeigt verschiedene Arten von Schadsoftware, die auf Geräten erkannt wurden, die in InTune registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="c97fe-175">**Types of malware on devices** shows different kinds of malware that have been detected on devices enrolled in Intune.</span></span> <span data-ttu-id="c97fe-176">Sie können jeden Typ im Microsoft 365 Security Center untersuchen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-176">You can investigate each type in Microsoft 365 security center.</span></span>

![Arten von Schadsoftware auf der Geräte Karte](./media/security-docs/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a><span data-ttu-id="c97fe-178">Verstehen der auf Ihren Geräten festgestellten spezifischen Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="c97fe-178">Understand the specific malware detected on your devices</span></span>

<span data-ttu-id="c97fe-179">**Schadsoftware auf Geräten** enthält eine Liste der auf Ihren Geräten erkannten spezifischen Schadsoftware.</span><span class="sxs-lookup"><span data-stu-id="c97fe-179">**Malware on devices** provides a list of the specific malware detected on your devices.</span></span>

![Schadsoftware auf Geräte Karte](./media/security-docs/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a><span data-ttu-id="c97fe-181">Verstehen der Geräte, die die meisten Schadsoftware aufweisen</span><span class="sxs-lookup"><span data-stu-id="c97fe-181">Understand which devices have the most malware</span></span>

<span data-ttu-id="c97fe-182">**Geräte mit Schadsoftware** -Entdeckungen zeigen, welche Geräte die meisten Malware-Entdeckungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-182">**Devices with malware detections** shows which devices have the most malware detections.</span></span> <span data-ttu-id="c97fe-183">In Microsoft 365 Security Center können Sie untersuchen, ob Schadsoftware aktiv ist, wer das Gerät verwendet, und den Verwaltungsstatus in InTune.</span><span class="sxs-lookup"><span data-stu-id="c97fe-183">In Microsoft 365 security center, you can investigate whether malware is active, who uses the device, and its management status in Intune.</span></span>

![Geräte mit Schadsoftware-Erkennungskarte](./media/security-docs/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a><span data-ttu-id="c97fe-185">Verstehen der Benutzer, die über Geräte mit der meisten Schadsoftware verfügen</span><span class="sxs-lookup"><span data-stu-id="c97fe-185">Understand which users have devices with the most malware</span></span>

<span data-ttu-id="c97fe-186">**Benutzer mit Schadsoftware** -Entdeckungen zeigen Benutzer mit Geräten, die die meisten Malware-Entdeckungen hatten.</span><span class="sxs-lookup"><span data-stu-id="c97fe-186">**Users with malware detections** shows users with devices that had the most malware detections.</span></span> <span data-ttu-id="c97fe-187">In Microsoft 365 Security Center können Sie sehen, wie viele Geräte jedem Benutzer zugewiesen sind, sowie weitere Informationen zu jedem Gerät und zu dem Typ der Schadsoftware.</span><span class="sxs-lookup"><span data-stu-id="c97fe-187">In Microsoft 365 security center, you can see how many devices are assigned to each user and more information about each device and the type of malware.</span></span>

![Benutzer mit Schadsoftware-Erkennungskarte](./media/security-docs/users-with-malware-detections.png)

## <a name="monitor-and-manage-asr-rule-deployment-and-detections"></a><span data-ttu-id="c97fe-189">Überwachen und Verwalten der Bereitstellung und Erkennung von ASR-Regeln</span><span class="sxs-lookup"><span data-stu-id="c97fe-189">Monitor and manage ASR rule deployment and detections</span></span>

<span data-ttu-id="c97fe-190">Mithilfe von Regeln zur anGriffs [Flächen Reduzierung (ASR)](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) können Sie verhindern, dass Aktionen und apps, die in der Regel von Exploit-suchen verwendet werden, Computer infizieren.</span><span class="sxs-lookup"><span data-stu-id="c97fe-190">[Attack Surface Reduction (ASR) rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) help prevent actions and apps that are typically used by exploit-seeking malware to infect machines.</span></span> <span data-ttu-id="c97fe-191">Diese Regeln steuern, wann und wie ausführbare Dateien ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c97fe-191">These rules control when and how executables can run.</span></span> <span data-ttu-id="c97fe-192">Sie können beispielsweise verhindern, dass JavaScript oder VBScript eine heruntergeladene ausführbare Datei startet, Win32-API-Aufrufe von Office-Makros blockiert oder Prozesse blockiert, die von USB-Laufwerken ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c97fe-192">For example, you can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, or block processes that run from USB drives.</span></span>

![Karte für anGriffsflächen Reduzierung](./media/security-docs/attack-surface-reduction-rules.png)

<span data-ttu-id="c97fe-194">Die **Regelkarte Angriffsflächen Reduzierung** bietet eine Übersicht über die Bereitstellung von Regeln auf Ihren Geräten.</span><span class="sxs-lookup"><span data-stu-id="c97fe-194">The **Attack surface reduction rules** card provides an overview of the deployment of rules across your devices.</span></span>

<span data-ttu-id="c97fe-195">Auf der oberen Leiste der Karte wird die Gesamtzahl der Geräte angezeigt, die sich in den folgenden Bereitstellungsmodi befinden:</span><span class="sxs-lookup"><span data-stu-id="c97fe-195">The top bar on the card shows the total number of devices that are in the following deployment modes:</span></span>

* <span data-ttu-id="c97fe-196">**Blockierungs Modus** – Geräte mit mindestens einer Regel, die zum Blockieren der erkannten Aktivität konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="c97fe-196">**Block mode** – devices with at least one rule configured to block detected activity</span></span>
* <span data-ttu-id="c97fe-197">**Überwachungsmodus** – Geräte, für die keine Regeln festgelegt wurden, um erkannte Aktivitäten zu blockieren, aber mindestens eine Regel zum Überwachen erkannter Aktivitäten festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="c97fe-197">**Audit mode** – devices with no rules set to block detected activity, but has at least one rule set to audit detected activity</span></span>  
* <span data-ttu-id="c97fe-198">**Off** – Geräte, für die alle ASR-Regeln deaktiviert sind</span><span class="sxs-lookup"><span data-stu-id="c97fe-198">**Off** – devices with all ASR rules turned off</span></span>

<span data-ttu-id="c97fe-199">Im unteren Teil dieser Karte werden Einstellungen nach Regel über Ihre Geräte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c97fe-199">The lower part of this card shows settings by rule across your devices.</span></span> <span data-ttu-id="c97fe-200">Jeder Balken gibt die Anzahl der Geräte an, die zum Blockieren oder Überwachen der Erkennung oder zur vollständigen Deaktivierung der Regel aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c97fe-200">Each bar indicates the number of devices that are set to block or audit detection or have the rule completely turned off.</span></span>

### <a name="view-asr-detections"></a><span data-ttu-id="c97fe-201">Anzeigen von ASR-Erkennungen</span><span class="sxs-lookup"><span data-stu-id="c97fe-201">View ASR detections</span></span>

<span data-ttu-id="c97fe-202">Wenn Sie detaillierte Informationen zu ASR-Regel Erkennungen in Ihrem Netzwerk anzeigen möchten, wählen Sie auf der Karte für die anGriffs **Flächen Reduzierungs Regeln** **Ansichts Erkennungen** aus.</span><span class="sxs-lookup"><span data-stu-id="c97fe-202">To view detailed information about ASR rule detections in your network, select **View detections** on the **Attack surface reduction rules** card.</span></span> <span data-ttu-id="c97fe-203">Die \*\*\*\* Registerkarte "Entdeckungen" auf der Seite "detaillierter Bericht" wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c97fe-203">The **Detections** tab in the detailed report page will open.</span></span>

![Registerkarte "Entdeckungen"](./media/security-docs/detections-tab.png)

<span data-ttu-id="c97fe-205">Das Diagramm am oberen Rand der Seite zeigt Entdeckungen im Zeitverlauf, die entweder blockiert oder überwacht wurden.</span><span class="sxs-lookup"><span data-stu-id="c97fe-205">The chart at the top of the page shows detections over time stacking detections that were either blocked or audited.</span></span> <span data-ttu-id="c97fe-206">In der Tabelle unten sind die neuesten Entdeckungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c97fe-206">The table at the bottom lists the most recent detections.</span></span> <span data-ttu-id="c97fe-207">Verwenden Sie die folgenden Informationen in der Tabelle, um die Art der Entdeckungen zu verstehen:</span><span class="sxs-lookup"><span data-stu-id="c97fe-207">Use the following information on the table to understand the nature of the detections:</span></span>

* <span data-ttu-id="c97fe-208">**Erkannte Datei** – die Datei, in der Regel ein Skript oder ein Dokument, deren Inhalt die mutmaßliche Angriffs Aktivität ausgelöst hat</span><span class="sxs-lookup"><span data-stu-id="c97fe-208">**Detected file** – the file, typically a script or a document, whose contents triggered the suspected attack activity</span></span>
* <span data-ttu-id="c97fe-209">**Regel** – Name zur Beschreibung der Angriffsaktivitäten, die von der Regel erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-209">**Rule** – name describing the attack activities the rule is designed to catch.</span></span> <span data-ttu-id="c97fe-210">Informationen zu vorhandenen ASR-Regeln</span><span class="sxs-lookup"><span data-stu-id="c97fe-210">Read about existing ASR rules</span></span>
* <span data-ttu-id="c97fe-211">**Quell-App** – die Anwendung, die Inhalte geladen oder ausgeführt hat, die die mutmaßliche Angriffs Aktivität auslösen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-211">**Source app** – the application that loaded or executed content triggering the suspected attack activity.</span></span> <span data-ttu-id="c97fe-212">Dabei kann es sich um eine legitime Anwendung wie Webbrowser, eine Office-Anwendung oder ein System Tool wie PowerShell handeln.</span><span class="sxs-lookup"><span data-stu-id="c97fe-212">This could be a legitimate application, such as web browser, an Office application, or a system tool like PowerShell</span></span>
* <span data-ttu-id="c97fe-213">**Publisher** – der Anbieter, der die Quell-App veröffentlicht hat</span><span class="sxs-lookup"><span data-stu-id="c97fe-213">**Publisher** – the vendor that released the source app</span></span>

### <a name="review-device-asr-rule-settings"></a><span data-ttu-id="c97fe-214">Überprüfungen der Einstellungen für die Geräte ASR-Regel</span><span class="sxs-lookup"><span data-stu-id="c97fe-214">Review device ASR rule settings</span></span>

<span data-ttu-id="c97fe-215">Wechseln Sie auf der Seite Regeln für die anGriffs **Flächen Reduzierung** auf die Registerkarte **Konfiguration** , um die Regeleinstellungen für einzelne Geräte zu überarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c97fe-215">In the **Attack surface reduction rules** report page, go to the **Configuration** tab to review rule settings for individual devices.</span></span> <span data-ttu-id="c97fe-216">Wählen Sie ein Gerät aus, um detaillierte Informationen dazu abzurufen, ob sich jede Regel im Blockmodus, im Überwachungsmodus oder vollständig deaktiviert befindet.</span><span class="sxs-lookup"><span data-stu-id="c97fe-216">Select a device to get detailed information about whether each rule is in block mode, audit mode, or turned off entirely.</span></span>

![Registerkarte "Konfiguration"](./media/security-docs/configuration-tab.png)

<span data-ttu-id="c97fe-218">Microsoft InTune bietet Verwaltungsfunktionen für Ihre ASR-Regeln.</span><span class="sxs-lookup"><span data-stu-id="c97fe-218">Microsoft Intune provides management functionality for your ASR rules.</span></span> <span data-ttu-id="c97fe-219">Wenn Sie Ihre Einstellungen aktualisieren möchten, wählen Sie unter **Geräte konfigurieren** auf der Registerkarte **Erste Schritte** , um Geräteverwaltung auf InTune zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-219">If you want to update your settings, select **Get started** under **Configure devices** in the tab to open device management on Intune.</span></span>

### <a name="exclude-files-from-asr-rules"></a><span data-ttu-id="c97fe-220">Ausschließen von Dateien aus ASR-Regeln</span><span class="sxs-lookup"><span data-stu-id="c97fe-220">Exclude files from ASR rules</span></span>

<span data-ttu-id="c97fe-221">Durch das Ausschließen von Dateien von Entdeckungen können Sie unerwünschte falsch positive Entdeckungen verhindern und die Regeln zur Angriffsflächen Reduzierung im Blockmodus sicherer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-221">By excluding files from detections, you can prevent unwanted false positive detections and more confidently deploy attack surface reduction rules in block mode.</span></span>

<span data-ttu-id="c97fe-222">Während Datei Ausschlüsse für Angriffsflächen Reduzierungs Regeln auf Microsoft InTune verwaltet werden, stellt das Microsoft 365 Security Center ein Analyse Tool bereit, mit dem Sie die Dateien verstehen können, die Entdeckungen auslösen.</span><span class="sxs-lookup"><span data-stu-id="c97fe-222">While file exclusions for attack surface reduction rules are managed on Microsoft Intune, Microsoft 365 security center provides an analysis tool to help you understand the files that are triggering detections.</span></span> <span data-ttu-id="c97fe-223">Außerdem werden die Namen der Dateien, die Sie möglicherweise ausschließen möchten, erfasst.</span><span class="sxs-lookup"><span data-stu-id="c97fe-223">It also helps collect the names of the files you might want to exclude.</span></span>

<span data-ttu-id="c97fe-224">Wechseln Sie zur Registerkarte **Ausschlüsse hinzufügen** auf der Seite Bericht zur Angriffs **Flächen Reduzierung** , um die Analyse von Entdeckungen und das Sammeln von Dateien zu starten.</span><span class="sxs-lookup"><span data-stu-id="c97fe-224">To start analyzing detections and collecting files for exclusion, go to the **Add exclusions** tab in the **Attack surface reduction rules** report page.</span></span>

![Registerkarte "Ausschlüsse hinzufügen"](./media/security-docs/add-exclusions-tab.png)

<span data-ttu-id="c97fe-226">In der Tabelle sind alle Dateinamen aufgeführt, die von den Regeln zur Angriffs Oberflächenreduzierung erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="c97fe-226">The table lists all the file names detected by your attack surface reduction rules.</span></span> <span data-ttu-id="c97fe-227">Nachdem Sie eine oder mehrere Dateien ausgewählt haben, können Sie die Auswirkungen des Hinzufügens dieser Dateien zu ihren Ausnahmen überarbeiten:</span><span class="sxs-lookup"><span data-stu-id="c97fe-227">Once you select a file or multiple files, you can review the impact of adding those files to your exceptions:</span></span>

* <span data-ttu-id="c97fe-228">Die Verringerung der Gesamtanzahl von Entdeckungen</span><span class="sxs-lookup"><span data-stu-id="c97fe-228">The reduction in the total number of detections</span></span>
* <span data-ttu-id="c97fe-229">Die Verringerung der Gesamtzahl der von den Entdeckungen betroffenen Geräte</span><span class="sxs-lookup"><span data-stu-id="c97fe-229">The reduction in the total number of devices affected by the detections</span></span>

<span data-ttu-id="c97fe-230">Wenn Sie eine Liste der ausgewählten Dateien mit den vollständigen Pfaden für den Ausschluss abrufen möchten, wählen Sie **Ausschluss Pfade abrufen**aus.</span><span class="sxs-lookup"><span data-stu-id="c97fe-230">To get a list of the selected files with their full paths for exclusion, select **Get exclusion paths**.</span></span>

<span data-ttu-id="c97fe-231">Weitere Informationen zu Ausschlüssen und ausführlichen Anweisungen zum Hinzufügen finden Sie unter [Problembehandlung bei Angriffs Oberflächenreduzierung](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr).</span><span class="sxs-lookup"><span data-stu-id="c97fe-231">For more information about exclusions and detailed instructions about how to add them, read [troubleshoot attack surface reduction rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr).</span></span>
