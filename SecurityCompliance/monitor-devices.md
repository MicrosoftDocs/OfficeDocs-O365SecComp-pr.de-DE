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
search.appverid: met150
ms.openlocfilehash: 2984231caba574b8fa47b725ab77227f6ab5ae56
ms.sourcegitcommit: 468a7c72df3206333d7d633dd7ce1f210dc1ef3a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2019
ms.locfileid: "33302739"
---
# <a name="monitor-devices-in-microsoft-365-security"></a><span data-ttu-id="a0da8-104">Überwachen von Geräten in Microsoft 365 Security</span><span class="sxs-lookup"><span data-stu-id="a0da8-104">Monitor devices in Microsoft 365 security</span></span>

<span data-ttu-id="a0da8-105">Halten Sie Ihre Geräte sicher, auf dem neuesten Stand und stellen Sie potenzielle Bedrohungen im Microsoft 365 Security Center vor.</span><span class="sxs-lookup"><span data-stu-id="a0da8-105">Keep your devices secure, up-to-date, and spot potential threats in the Microsoft 365 security center.</span></span>

## <a name="view-device-alerts"></a><span data-ttu-id="a0da8-106">Anzeigen von Geräte Warnungen</span><span class="sxs-lookup"><span data-stu-id="a0da8-106">View device alerts</span></span>

<span data-ttu-id="a0da8-107">Informieren Sie sich über aktuelle Warnungen zu Verstößen und anderen Bedrohungen auf Ihren Geräten von Windows Defender ATP (verfügbar mit einer E5-Lizenz).</span><span class="sxs-lookup"><span data-stu-id="a0da8-107">Get up-to-date alerts about breach activity and other threats on your devices from Windows Defender ATP (available with an E5 license).</span></span> <span data-ttu-id="a0da8-108">Microsoft 365 Security Center überwacht diese Warnungen effektiv über Ihren bevorzugten Workflow auf hoher Ebene.</span><span class="sxs-lookup"><span data-stu-id="a0da8-108">Microsoft 365 security center effectively monitors these alerts at a high level using your preferred workflow.</span></span>

### <a name="monitor-high-impact-alerts"></a><span data-ttu-id="a0da8-109">Überwachen von Warnungen mit hoher Auswirkung</span><span class="sxs-lookup"><span data-stu-id="a0da8-109">Monitor high-impact alerts</span></span>

<span data-ttu-id="a0da8-110">Jede Windows Defender-ATP-Warnung weist einen entsprechenden Schweregrad auf – hoch, Mittel, niedrig oder Informationswert –, der die potenziellen Auswirkungen auf Ihr Netzwerk angibt, wenn Sie unbeaufsichtigt bleiben.</span><span class="sxs-lookup"><span data-stu-id="a0da8-110">Each Windows Defender ATP alert has a corresponding severity—high, medium, low, or informational—that indicates its potential impact to your network if left unattended.</span></span>  

<span data-ttu-id="a0da8-111">Verwenden Sie die **Geräte Warnungs schwere** Karte, um sich gezielt auf schwerwiegende Warnungen zu konzentrieren, die möglicherweise sofort beantwortet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-111">Use the **Device alert severity** card to focus specifically on alerts that are more severe and might require immediate response.</span></span> <span data-ttu-id="a0da8-112">Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-112">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

![Schwerekarte für Geräte Warnungen](./media/security-docs/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a><span data-ttu-id="a0da8-114">Informationen zu Quellen von Warnungen</span><span class="sxs-lookup"><span data-stu-id="a0da8-114">Understand sources of alerts</span></span>

<span data-ttu-id="a0da8-115">Windows Defender ATP nutzt Daten aus einer Vielzahl von Sicherheitssensoren und Intelligence-Quellen, um Warnungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a0da8-115">Windows Defender ATP leverages data from a broad range of security sensors and intelligence sources to generate alerts.</span></span> <span data-ttu-id="a0da8-116">Sie können beispielsweise Erkennungsinformationen von Windows Defender Antivirus und Antischadsoftware von Drittanbietern sowie ihre eigenen benutzerdefinierten Bedrohungs Nachrichten verwenden, die über die Webdienst-API bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0da8-116">For example, it can use detection information from Windows Defender Antivirus and third-party antimalware, as well as your own custom threat intelligence provided through the web service API.</span></span>

<span data-ttu-id="a0da8-117">Die Karte zur **Erkennung von Geräte Warnungen** zeigt die Verteilung der Warnungen nach Quelle.</span><span class="sxs-lookup"><span data-stu-id="a0da8-117">The **Device alert detection** sources card shows the distribution of alerts by source.</span></span> <span data-ttu-id="a0da8-118">Diese Karte kann Ihnen dabei helfen, Aktivitäten im Zusammenhang mit bestimmten Quellen, insbesondere ihren benutzerdefinierten Quellen nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-118">This card can help you track activity related to certain sources, particularly your custom sources.</span></span> <span data-ttu-id="a0da8-119">Sie können sich auch auf Warnungen konzentrieren, die von Sensoren stammen, die nicht so konfiguriert sind, dass Sie bösartige Aktivitäten oder Komponenten automatisch blockieren.</span><span class="sxs-lookup"><span data-stu-id="a0da8-119">You can also use this to focus on alerts coming from sensors that are not configured to automatically block malicious activity or components.</span></span>

![Geräte Warnungs-Erkennungsquellen Karte](./media/security-docs/device-alert-detection-sources.png)

<span data-ttu-id="a0da8-121">Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-121">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a><span data-ttu-id="a0da8-122">GrundLegendes zu den Arten von Bedrohungen, die Warnungen auslösen</span><span class="sxs-lookup"><span data-stu-id="a0da8-122">Understand the types of threats that trigger alerts</span></span>

<span data-ttu-id="a0da8-123">Windows Defender ATP sortiert jede Warnung in einer Kategorie, die eine bestimmte Stufe in der Angriffs Kette oder eine Art von Bedrohungs Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0da8-123">Windows Defender ATP sorts each alert into a category representing a certain stage in the attack chain or a type of threat component.</span></span> <span data-ttu-id="a0da8-124">Die erkannte Bedrohungsaktivität kann beispielsweise in "Lateral Movement" kategorisiert werden, um anzugeben, dass die Aktivität versucht hat, andere Geräte im Netzwerk zu erreichen, und die Wahrscheinlichkeit aufgetreten ist, nachdem Angreifer eine erste Stütze erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="a0da8-124">For example, detected threat activity might be categorized into “lateral movement” to indicate that the activity involved an attempt to reach other devices on the network and has likely occurred after attackers have gained an initial foothold.</span></span> <span data-ttu-id="a0da8-125">Wenn eine Bedrohungs Komponente erkannt wird, kann Sie entweder als "Schadsoftware" oder genauer als "Ransomware", "Diebstahl von Anmeldeinformationen" oder anderen Arten von böswilliger oder unerwünschter Software klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a0da8-125">When detected, a threat component might either be classified broadly as “malware” or more specifically as “ransomware”, “credential stealing” or other types of malicious or unwanted software.</span></span>

<span data-ttu-id="a0da8-126">Die Karte für die **Geräte Bedrohungskategorien** zeigt die Verteilung von Warnungen in diese Kategorien an.</span><span class="sxs-lookup"><span data-stu-id="a0da8-126">The **Device threat categories** card shows the distribution of alerts into these categories.</span></span> <span data-ttu-id="a0da8-127">Sie können diese Informationen verwenden, um die Bedrohungsaktivität zu identifizieren, wie beispielsweise Versuche zum Diebstahl von Anmeldeinformationen, die sich im Vergleich zu den versuchen bei Social Engineering zum Beispiel erheblich auswirken können.</span><span class="sxs-lookup"><span data-stu-id="a0da8-127">You can use this information to identify threat activity, such as attempts at credential theft, which can have more significant impact compared to attempts at social engineering, for example.</span></span> <span data-ttu-id="a0da8-128">Sie können dies auch verwenden, um potenziell zerstörerische Bedrohungen wie Ransomware zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-128">You can also use this to monitor for potentially destructive threats like ransomware.</span></span>

![Karte für Geräte Bedrohungskategorien](./media/security-docs/device-threat-categories.png)

### <a name="monitor-active-alerts"></a><span data-ttu-id="a0da8-130">Überwachen aktiver Warnungen</span><span class="sxs-lookup"><span data-stu-id="a0da8-130">Monitor active alerts</span></span>

<span data-ttu-id="a0da8-131">Die **Geräte Warnungsstatus** Karte gibt die Anzahl der Warnungen an, die nicht aufgelöst wurden und möglicherweise Aufmerksamkeit erfordern.</span><span class="sxs-lookup"><span data-stu-id="a0da8-131">The **Device alert status** card indicates the number of alerts that have not been resolved and might require attention.</span></span> <span data-ttu-id="a0da8-132">Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-132">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

![Geräte Warnungsstatus Karte](./media/security-docs/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a><span data-ttu-id="a0da8-134">Überwachen der Klassifizierung aufgelöster Warnungen</span><span class="sxs-lookup"><span data-stu-id="a0da8-134">Monitor classification of resolved alerts</span></span>

<span data-ttu-id="a0da8-135">Wenn Sie eine Windows Defender-ATP-Warnung auflösen, können Ihre Sicherheitsmitarbeiter angeben, ob eine Warnung wie folgt überprüft wurde:</span><span class="sxs-lookup"><span data-stu-id="a0da8-135">When resolving a Window Defender ATP alert, your security staff can specify whether an alert has been verified as:</span></span>

* <span data-ttu-id="a0da8-136">Eine echte Warnung, die tatsächliche Verletzungs Aktivität oder Bedrohungs Komponenten identifiziert</span><span class="sxs-lookup"><span data-stu-id="a0da8-136">A true alert that identifies actual breach activity or threat components</span></span>
* <span data-ttu-id="a0da8-137">Falsche Warnung, die normale Aktivität falsch erkannt hat</span><span class="sxs-lookup"><span data-stu-id="a0da8-137">A false alert that has incorrectly detected normal activity</span></span>

<span data-ttu-id="a0da8-138">Auf der **Device Alert** -Klassifikations Karte wird angezeigt, ob Ihre aufgelöste Warnungen als wahr oder falsch eingestuft wurden.</span><span class="sxs-lookup"><span data-stu-id="a0da8-138">The **Device alert classification** card shows whether your resolved alerts have been classified as true or false alerts.</span></span> <span data-ttu-id="a0da8-139">Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-139">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

<span data-ttu-id="a0da8-140">Hinweis: in einigen Fällen sind Klassifizierungsinformationen für bestimmte Warnungen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0da8-140">Note: In some cases, classification information is unavailable for certain alerts.</span></span>

![Geräte Warnungs-Klassifikations Karte](./media/security-docs/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a><span data-ttu-id="a0da8-142">Überwachen der Ermittlung aufgelöster Warnungen</span><span class="sxs-lookup"><span data-stu-id="a0da8-142">Monitor determination of resolved alerts</span></span>

<span data-ttu-id="a0da8-143">Zusätzlich zur Klassifizierung, ob eine Warnung während der Auflösung true oder false ist, können Ihre Sicherheitsmitarbeiter eine Bestimmung bereitstellen, die angibt, welche Art von normaler oder bösartiger Aktivität während der Überprüfung der Warnung gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a0da8-143">In addition to classifying whether an alert is true or false during resolution, your security staff can provide a determination, indicating the type of normal or malicious activity that was found while validating the alert.</span></span>

<span data-ttu-id="a0da8-144">Auf der **Geräte Warnungs Findungs** Karte wird die für jede Warnung vorgesehene Bestimmung angezeigt, insbesondere:</span><span class="sxs-lookup"><span data-stu-id="a0da8-144">The **Device alert determination** card shows the determination provided for each alert, specifically:</span></span>

* <span data-ttu-id="a0da8-145">**Apt** – Advanced persistent Threat, die darauf hinweist, dass die erkannte Aktivität oder Bedrohungs Komponente Teil einer ausgeklügelten Verletzung ist, die dazu dient, im betroffenen Netzwerk Fuß zu fassen</span><span class="sxs-lookup"><span data-stu-id="a0da8-145">**APT** – advanced persistent threat, indicating that the detected activity or threat component is part of a sophisticated breach designed to gain a foothold in the affected network</span></span>  
* <span data-ttu-id="a0da8-146">**Schadsoftware** – Schadsoftware oder Code</span><span class="sxs-lookup"><span data-stu-id="a0da8-146">**Malware** – malicious file or code</span></span>
* <span data-ttu-id="a0da8-147">**Sicherheitspersonal** – normale Aktivitäten des Sicherheitspersonals</span><span class="sxs-lookup"><span data-stu-id="a0da8-147">**Security personnel** – normal activity performed by security staff</span></span>
* <span data-ttu-id="a0da8-148">**Sicherheitstests** – Aktivitäten oder Komponenten zur Simulation von tatsächlichen Bedrohungen und erwarteten Sicherheitssensoren und Warnungen generieren</span><span class="sxs-lookup"><span data-stu-id="a0da8-148">**Security testing** – activity or components designed to simulate actual threats and expected to trigger security sensors and generate alerts</span></span>
* <span data-ttu-id="a0da8-149">**Unerwünschte Software** – apps und andere Software, die nicht als bösartig gelten, aber sonst gegen Richtlinien oder akzeptable Nutzungsstandards verstoßen</span><span class="sxs-lookup"><span data-stu-id="a0da8-149">**Unwanted software** – apps and other software that are not considered malicious, but otherwise violate policy or acceptable use standards</span></span>
* <span data-ttu-id="a0da8-150">**Andere** – jede andere Bestimmung, die nicht unter die angegebenen Typen fällt</span><span class="sxs-lookup"><span data-stu-id="a0da8-150">**Others** – any other determination that does not fall under the provided types</span></span>

<span data-ttu-id="a0da8-151">Von dieser Karte aus können Sie weitere Informationen im Windows Defender Security Center anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-151">From this card, you can view more information in Windows Defender security center.</span></span>

![Geräte Warnungs Findungs Karte](./media/security-docs/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a><span data-ttu-id="a0da8-153">Verstehen der gefährdeten Geräte</span><span class="sxs-lookup"><span data-stu-id="a0da8-153">Understand which devices are at risk</span></span>

<span data-ttu-id="a0da8-154">**Geräteschutz** zeigt die Risikostufe für Geräte an.</span><span class="sxs-lookup"><span data-stu-id="a0da8-154">**Device protection** shows the risk level for devices.</span></span> <span data-ttu-id="a0da8-155">Die Risikostufe basiert auf Faktoren wie Typ und Schweregrad der Warnungen auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="a0da8-155">The risk level is based on factors such as the type and severity of alerts on the device.</span></span>

![Geräteschutz Karte](./media/security-docs/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a><span data-ttu-id="a0da8-157">Überwachen und melden des Status von InTune-verwalteten Geräten</span><span class="sxs-lookup"><span data-stu-id="a0da8-157">Monitor and report status of Intune-managed devices</span></span>

<span data-ttu-id="a0da8-158">Die folgenden Überwachungen und Berichte enthalten Daten von Geräten, die in InTune registriert sind.</span><span class="sxs-lookup"><span data-stu-id="a0da8-158">The following monitoring and reports contain data from devices enrolled in Intune.</span></span> <span data-ttu-id="a0da8-159">Daten von nicht registrierten Geräten sind nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="a0da8-159">Data from unenrolled devices is not included.</span></span> <span data-ttu-id="a0da8-160">Nur globale Administratoren können diese Karten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-160">Only Global Administrators can view these cards.</span></span>

<span data-ttu-id="a0da8-161">InTune-Daten für registrierte Geräte umfassen:</span><span class="sxs-lookup"><span data-stu-id="a0da8-161">Intune enrolled device data includes:</span></span>

* <span data-ttu-id="a0da8-162">Geräte Konformität</span><span class="sxs-lookup"><span data-stu-id="a0da8-162">Device compliance</span></span>
* <span data-ttu-id="a0da8-163">Geräte mit aktiver Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="a0da8-163">Devices with active malware</span></span>
* <span data-ttu-id="a0da8-164">Arten von Schadsoftware auf Geräten</span><span class="sxs-lookup"><span data-stu-id="a0da8-164">Types of malware on devices</span></span>
* <span data-ttu-id="a0da8-165">Schadsoftware auf Geräten</span><span class="sxs-lookup"><span data-stu-id="a0da8-165">Malware on devices</span></span>
* <span data-ttu-id="a0da8-166">Geräte mit Schadsoftware-Entdeckungen</span><span class="sxs-lookup"><span data-stu-id="a0da8-166">Devices with malware detections</span></span>
* <span data-ttu-id="a0da8-167">Benutzer mit Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="a0da8-167">Users with malware detections</span></span>

### <a name="monitor-device-compliance"></a><span data-ttu-id="a0da8-168">Überwachen der Geräte Konformität</span><span class="sxs-lookup"><span data-stu-id="a0da8-168">Monitor device compliance</span></span>

<span data-ttu-id="a0da8-169">**Device Compliance** zeigt, wie viele Geräte, die in InTune registriert sind, Konfigurationsrichtlinien einhalten.</span><span class="sxs-lookup"><span data-stu-id="a0da8-169">**Device compliance** shows how many devices that are enrolled in Intune comply with configuration policies.</span></span>

![Geräte Konformitäts Karte](./media/security-docs/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a><span data-ttu-id="a0da8-171">Erkennen von Geräten mit Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="a0da8-171">Discover devices with malware detections</span></span>

<span data-ttu-id="a0da8-172">**Geräte-Malware** -Entdeckungen bieten die Anzahl von InTune-Geräten, die aufgrund ausstehender Aktionen nicht vollständig aufgelöst wurden – ein Neustart, eine vollständige Überprüfung oder manuelle Benutzeraktionen – oder wenn die Behebungsaktion nicht erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a0da8-172">**Device malware detections** provides the number of Intune enrolled devices with malware that have not been fully resolved due to pending actions—a restart, a full scan or manual user actions—or if the remediation action did not complete successfully.</span></span>

![Geräte-Malware-Erkennungskarte](./media/security-docs/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a><span data-ttu-id="a0da8-174">GrundLegendes zu den festgestellten Arten</span><span class="sxs-lookup"><span data-stu-id="a0da8-174">Understand the types of malware detected</span></span>

<span data-ttu-id="a0da8-175">**Arten von Schadsoftware auf Geräten** zeigt verschiedene Arten von Schadsoftware, die auf Geräten erkannt wurden, die in InTune registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="a0da8-175">**Types of malware on devices** shows different kinds of malware that have been detected on devices enrolled in Intune.</span></span> <span data-ttu-id="a0da8-176">Sie können jeden Typ im Microsoft 365 Security Center untersuchen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-176">You can investigate each type in Microsoft 365 security center.</span></span>

![Arten von Schadsoftware auf der Geräte Karte](./media/security-docs/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a><span data-ttu-id="a0da8-178">Verstehen der auf Ihren Geräten festgestellten spezifischen Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="a0da8-178">Understand the specific malware detected on your devices</span></span>

<span data-ttu-id="a0da8-179">**Schadsoftware auf Geräten** enthält eine Liste der auf Ihren Geräten erkannten spezifischen Schadsoftware.</span><span class="sxs-lookup"><span data-stu-id="a0da8-179">**Malware on devices** provides a list of the specific malware detected on your devices.</span></span>

![Schadsoftware auf Geräte Karte](./media/security-docs/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a><span data-ttu-id="a0da8-181">Verstehen der Geräte, die die meisten Schadsoftware aufweisen</span><span class="sxs-lookup"><span data-stu-id="a0da8-181">Understand which devices have the most malware</span></span>

<span data-ttu-id="a0da8-182">**Geräte mit Schadsoftware** -Entdeckungen zeigen, welche Geräte die meisten Malware-Entdeckungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-182">**Devices with malware detections** shows which devices have the most malware detections.</span></span> <span data-ttu-id="a0da8-183">In Microsoft 365 Security Center können Sie untersuchen, ob Schadsoftware aktiv ist, wer das Gerät verwendet, und den Verwaltungsstatus in InTune.</span><span class="sxs-lookup"><span data-stu-id="a0da8-183">In Microsoft 365 security center, you can investigate whether malware is active, who uses the device, and its management status in Intune.</span></span>

![Geräte mit Schadsoftware-Erkennungskarte](./media/security-docs/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a><span data-ttu-id="a0da8-185">Verstehen der Benutzer, die über Geräte mit der meisten Schadsoftware verfügen</span><span class="sxs-lookup"><span data-stu-id="a0da8-185">Understand which users have devices with the most malware</span></span>

<span data-ttu-id="a0da8-186">**Benutzer mit Schadsoftware** -Entdeckungen zeigen Benutzer mit Geräten, die die meisten Malware-Entdeckungen hatten.</span><span class="sxs-lookup"><span data-stu-id="a0da8-186">**Users with malware detections** shows users with devices that had the most malware detections.</span></span> <span data-ttu-id="a0da8-187">In Microsoft 365 Security Center können Sie sehen, wie viele Geräte jedem Benutzer zugewiesen sind, sowie weitere Informationen zu jedem Gerät und zu dem Typ der Schadsoftware.</span><span class="sxs-lookup"><span data-stu-id="a0da8-187">In Microsoft 365 security center, you can see how many devices are assigned to each user and more information about each device and the type of malware.</span></span>

![Benutzer mit Schadsoftware-Erkennungskarte](./media/security-docs/users-with-malware-detections.png)

## <a name="monitor-and-manage-asr-rule-deployment-and-detections"></a><span data-ttu-id="a0da8-189">Überwachen und Verwalten der Bereitstellung und Erkennung von ASR-Regeln</span><span class="sxs-lookup"><span data-stu-id="a0da8-189">Monitor and manage ASR rule deployment and detections</span></span>

<span data-ttu-id="a0da8-190">Mithilfe von Regeln zur anGriffs [Flächen Reduzierung (ASR)](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) können Sie verhindern, dass Aktionen und apps, die in der Regel von Exploit-suchen verwendet werden, Computer infizieren.</span><span class="sxs-lookup"><span data-stu-id="a0da8-190">[Attack Surface Reduction (ASR) rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) help prevent actions and apps that are typically used by exploit-seeking malware to infect machines.</span></span> <span data-ttu-id="a0da8-191">Diese Regeln steuern, wann und wie ausführbare Dateien ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="a0da8-191">These rules control when and how executables can run.</span></span> <span data-ttu-id="a0da8-192">Sie können beispielsweise verhindern, dass JavaScript oder VBScript eine heruntergeladene ausführbare Datei startet, Win32-API-Aufrufe von Office-Makros blockiert oder Prozesse blockiert, die von USB-Laufwerken ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0da8-192">For example, you can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, or block processes that run from USB drives.</span></span>

![Karte für anGriffsflächen Reduzierung](./media/security-docs/attack-surface-reduction-rules.png)

<span data-ttu-id="a0da8-194">Die **Regelkarte Angriffsflächen Reduzierung** bietet eine Übersicht über die Bereitstellung von Regeln auf Ihren Geräten.</span><span class="sxs-lookup"><span data-stu-id="a0da8-194">The **Attack surface reduction rules** card provides an overview of the deployment of rules across your devices.</span></span>

<span data-ttu-id="a0da8-195">Auf der oberen Leiste der Karte wird die Gesamtzahl der Geräte angezeigt, die sich in den folgenden Bereitstellungsmodi befinden:</span><span class="sxs-lookup"><span data-stu-id="a0da8-195">The top bar on the card shows the total number of devices that are in the following deployment modes:</span></span>

* <span data-ttu-id="a0da8-196">**Blockierungs Modus** – Geräte mit mindestens einer Regel, die zum Blockieren der erkannten Aktivität konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="a0da8-196">**Block mode** – devices with at least one rule configured to block detected activity</span></span>
* <span data-ttu-id="a0da8-197">**Überwachungsmodus** – Geräte, für die keine Regeln festgelegt wurden, um erkannte Aktivitäten zu blockieren, aber mindestens eine Regel zum Überwachen erkannter Aktivitäten festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="a0da8-197">**Audit mode** – devices with no rules set to block detected activity, but has at least one rule set to audit detected activity</span></span>  
* <span data-ttu-id="a0da8-198">**Off** – Geräte, für die alle ASR-Regeln deaktiviert sind</span><span class="sxs-lookup"><span data-stu-id="a0da8-198">**Off** – devices with all ASR rules turned off</span></span>

<span data-ttu-id="a0da8-199">Im unteren Teil dieser Karte werden Einstellungen nach Regel über Ihre Geräte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0da8-199">The lower part of this card shows settings by rule across your devices.</span></span> <span data-ttu-id="a0da8-200">Jeder Balken gibt die Anzahl der Geräte an, die zum Blockieren oder Überwachen der Erkennung oder zur vollständigen Deaktivierung der Regel aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="a0da8-200">Each bar indicates the number of devices that are set to block or audit detection or have the rule completely turned off.</span></span>

### <a name="view-asr-detections"></a><span data-ttu-id="a0da8-201">Anzeigen von ASR-Erkennungen</span><span class="sxs-lookup"><span data-stu-id="a0da8-201">View ASR detections</span></span>

<span data-ttu-id="a0da8-202">Wenn Sie detaillierte Informationen zu ASR-Regel Erkennungen in Ihrem Netzwerk anzeigen möchten, wählen Sie auf der Karte für die anGriffs **Flächen Reduzierungs Regeln** **Ansichts Erkennungen** aus.</span><span class="sxs-lookup"><span data-stu-id="a0da8-202">To view detailed information about ASR rule detections in your network, select **View detections** on the **Attack surface reduction rules** card.</span></span> <span data-ttu-id="a0da8-203">Die \*\*\*\* Registerkarte "Entdeckungen" auf der Seite "detaillierter Bericht" wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a0da8-203">The **Detections** tab in the detailed report page will open.</span></span>

![Registerkarte "Entdeckungen"](./media/security-docs/detections-tab.png)

<span data-ttu-id="a0da8-205">Das Diagramm am oberen Rand der Seite zeigt Entdeckungen im Zeitverlauf, die entweder blockiert oder überwacht wurden.</span><span class="sxs-lookup"><span data-stu-id="a0da8-205">The chart at the top of the page shows detections over time stacking detections that were either blocked or audited.</span></span> <span data-ttu-id="a0da8-206">In der Tabelle unten sind die neuesten Entdeckungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0da8-206">The table at the bottom lists the most recent detections.</span></span> <span data-ttu-id="a0da8-207">Verwenden Sie die folgenden Informationen in der Tabelle, um die Art der Entdeckungen zu verstehen:</span><span class="sxs-lookup"><span data-stu-id="a0da8-207">Use the following information on the table to understand the nature of the detections:</span></span>

* <span data-ttu-id="a0da8-208">**Erkannte Datei** – die Datei, in der Regel ein Skript oder ein Dokument, deren Inhalt die mutmaßliche Angriffs Aktivität ausgelöst hat</span><span class="sxs-lookup"><span data-stu-id="a0da8-208">**Detected file** – the file, typically a script or a document, whose contents triggered the suspected attack activity</span></span>
* <span data-ttu-id="a0da8-209">**Regel** – Name zur Beschreibung der Angriffsaktivitäten, die von der Regel erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-209">**Rule** – name describing the attack activities the rule is designed to catch.</span></span> <span data-ttu-id="a0da8-210">Informationen zu vorhandenen ASR-Regeln</span><span class="sxs-lookup"><span data-stu-id="a0da8-210">Read about existing ASR rules</span></span>
* <span data-ttu-id="a0da8-211">**Quell-App** – die Anwendung, die Inhalte geladen oder ausgeführt hat, die die mutmaßliche Angriffs Aktivität auslösen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-211">**Source app** – the application that loaded or executed content triggering the suspected attack activity.</span></span> <span data-ttu-id="a0da8-212">Dabei kann es sich um eine legitime Anwendung wie Webbrowser, eine Office-Anwendung oder ein System Tool wie PowerShell handeln.</span><span class="sxs-lookup"><span data-stu-id="a0da8-212">This could be a legitimate application, such as web browser, an Office application, or a system tool like PowerShell</span></span>
* <span data-ttu-id="a0da8-213">**Publisher** – der Anbieter, der die Quell-App veröffentlicht hat</span><span class="sxs-lookup"><span data-stu-id="a0da8-213">**Publisher** – the vendor that released the source app</span></span>

### <a name="review-device-asr-rule-settings"></a><span data-ttu-id="a0da8-214">Überprüfungen der Einstellungen für die Geräte ASR-Regel</span><span class="sxs-lookup"><span data-stu-id="a0da8-214">Review device ASR rule settings</span></span>

<span data-ttu-id="a0da8-215">Wechseln Sie auf der Seite Regeln für die anGriffs **Flächen Reduzierung** auf die Registerkarte **Konfiguration** , um die Regeleinstellungen für einzelne Geräte zu überarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a0da8-215">In the **Attack surface reduction rules** report page, go to the **Configuration** tab to review rule settings for individual devices.</span></span> <span data-ttu-id="a0da8-216">Wählen Sie ein Gerät aus, um detaillierte Informationen dazu abzurufen, ob sich jede Regel im Blockmodus, im Überwachungsmodus oder vollständig deaktiviert befindet.</span><span class="sxs-lookup"><span data-stu-id="a0da8-216">Select a device to get detailed information about whether each rule is in block mode, audit mode, or turned off entirely.</span></span>

![Registerkarte "Konfiguration"](./media/security-docs/configuration-tab.png)

<span data-ttu-id="a0da8-218">Microsoft InTune bietet Verwaltungsfunktionen für Ihre ASR-Regeln.</span><span class="sxs-lookup"><span data-stu-id="a0da8-218">Microsoft Intune provides management functionality for your ASR rules.</span></span> <span data-ttu-id="a0da8-219">Wenn Sie Ihre Einstellungen aktualisieren möchten, wählen Sie unter **Geräte konfigurieren** auf der Registerkarte **Erste Schritte** , um Geräteverwaltung auf InTune zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-219">If you want to update your settings, select **Get started** under **Configure devices** in the tab to open device management on Intune.</span></span>

### <a name="exclude-files-from-asr-rules"></a><span data-ttu-id="a0da8-220">Ausschließen von Dateien aus ASR-Regeln</span><span class="sxs-lookup"><span data-stu-id="a0da8-220">Exclude files from ASR rules</span></span>

<span data-ttu-id="a0da8-221">Microsoft 365 Security Center sammelt die Namen der [Dateien, die Sie möglicherweise](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr#add-exclusions-for-a-false-positive) nach Angriffs Oberflächen Reduzierungs Regeln ausschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="a0da8-221">Microsoft 365 security center collects the names of the [files you might want to exclude](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr#add-exclusions-for-a-false-positive) from detections by attack surface reduction rules.</span></span> <span data-ttu-id="a0da8-222">Durch das Ausschließen von Dateien können Sie falsch positive Erkennungsergebnisse verringern und die Regeln zur Angriffsflächen Reduzierung im Blockmodus sicherer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-222">By excluding files, you can reduce false positive detections and more confidently deploy attack surface reduction rules in block mode.</span></span>

<span data-ttu-id="a0da8-223">Die Ausschlüsse werden auf Microsoft InTune verwaltet, aber Microsoft 365 Security Center stellt ein Analyse Tool bereit, mit dem Sie die Dateien besser verstehen können.</span><span class="sxs-lookup"><span data-stu-id="a0da8-223">The exclusions are managed on Microsoft Intune, but Microsoft 365 security center provides an analysis tool to help you understand the files.</span></span> <span data-ttu-id="a0da8-224">Um Dateien für den Ausschluss zu sammeln, wechseln Sie zur Registerkarte **Ausschlüsse hinzufügen** auf der Seite Bericht zur Angriffs **Flächen Reduzierung** .</span><span class="sxs-lookup"><span data-stu-id="a0da8-224">To start collecting files for exclusion, go to the **Add exclusions** tab in the **Attack surface reduction rules** report page.</span></span>

>[!NOTE]  
><span data-ttu-id="a0da8-225">Das Tool analysiert Entdeckungen nach allen Regeln zur Angriffs Oberflächen Einschränkung, aber [nur einige Regeln unterstützen Ausschlüsse](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="a0da8-225">The tool analyzes detections by all attack surface reduction rules, but [only some rules support exclusions](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard#attack-surface-reduction-rules).</span></span>

![Registerkarte "Ausschlüsse hinzufügen"](./media/security-docs/add-exclusions-tab.png)

<span data-ttu-id="a0da8-227">In der Tabelle sind alle Dateinamen aufgeführt, die von den Regeln zur Angriffs Oberflächenreduzierung erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="a0da8-227">The table lists all the file names detected by your attack surface reduction rules.</span></span> <span data-ttu-id="a0da8-228">Sie können Dateien auswählen, um die Auswirkungen der Ausklammerung zu über sehen:</span><span class="sxs-lookup"><span data-stu-id="a0da8-228">You can select files to review the impact of excluding them:</span></span>

* <span data-ttu-id="a0da8-229">Wie viele wenige Entdeckungen</span><span class="sxs-lookup"><span data-stu-id="a0da8-229">How many fewer detections</span></span>
* <span data-ttu-id="a0da8-230">Wie viele weniger Geräte die Entdeckungen melden</span><span class="sxs-lookup"><span data-stu-id="a0da8-230">How many fewer devices report the detections</span></span>

<span data-ttu-id="a0da8-231">Wenn Sie eine Liste der ausgewählten Dateien mit den vollständigen Pfaden für den Ausschluss abrufen möchten, wählen Sie **Ausschluss Pfade abrufen**aus.</span><span class="sxs-lookup"><span data-stu-id="a0da8-231">To get a list of the selected files with their full paths for exclusion, select **Get exclusion paths**.</span></span>

<span data-ttu-id="a0da8-232">Protokolle für die ASR-Regel **Block Anmeldeinformationen, die vom Windows Local Security Authority Subsystem (Lsass. exe) gestohlen** werden, erfassen die Quell-app " **LSASS. exe**", eine normale System Datei, als erkannte Datei.</span><span class="sxs-lookup"><span data-stu-id="a0da8-232">Logs for the ASR rule **Block credential stealing from the Windows local security authority subsystem (lsass.exe)** capture the source app **lsass.exe**, a normal system file, as the detected file.</span></span> <span data-ttu-id="a0da8-233">Daher enthält die generierte Liste der Ausschluss Pfade diese Datei.</span><span class="sxs-lookup"><span data-stu-id="a0da8-233">As a result, the generated list of exclusion paths will include this file.</span></span> <span data-ttu-id="a0da8-234">Um die Datei auszuschließen, die diese Regel anstelle von " **LSASS. exe**" ausgelöst hat, verwenden Sie den Pfad zur Quell-APP anstelle der erkannten Datei.</span><span class="sxs-lookup"><span data-stu-id="a0da8-234">To exclude the file that triggered this rule instead of **lsass.exe**, use the path to the source app instead of the detected file.</span></span>

<span data-ttu-id="a0da8-235">Um die Quell-APP zu finden, führen Sie die folgende [erweiterte Suchabfrage](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/advanced-hunting-windows-defender-advanced-threat-protection) für diese bestimmte Regel aus (identifiziert durch Regel-ID 9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2):</span><span class="sxs-lookup"><span data-stu-id="a0da8-235">To locate the source app, run the following [advanced hunting query](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/advanced-hunting-windows-defender-advanced-threat-protection) for this specific rule (identified by rule ID 9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2):</span></span> 

```MiscEvents
| where EventTime > ago(7d)
| where ActionType startswith "Asr"
| where AdditionalFields contains "9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2"
| project InitiatingProcessFolderPath, InitiatingProcessFileName
```

#### <a name="check-files-for-exclusion"></a><span data-ttu-id="a0da8-236">Dateien auf Ausschluss überprüfen</span><span class="sxs-lookup"><span data-stu-id="a0da8-236">Check files for exclusion</span></span>
<span data-ttu-id="a0da8-237">Bevor Sie eine Datei aus der automatischen sprachERKENNUNG ausschließen, sollten Sie die Datei überprüfen, um zu ermitteln, ob Sie tatsächlich nicht bösartig ist.</span><span class="sxs-lookup"><span data-stu-id="a0da8-237">Before excluding a file from ASR, we recommend that you inspect the file to determine if it is indeed not malicious.</span></span>

<span data-ttu-id="a0da8-238">Verwenden Sie die [Seite Dateiinformationen](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/investigate-files-windows-defender-advanced-threat-protection) im Windows Defender-Sicherheits Center, um eine Datei zu überarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a0da8-238">To review a file, use the [file information page](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/investigate-files-windows-defender-advanced-threat-protection) on Windows Defender Security Center.</span></span> <span data-ttu-id="a0da8-239">Die Seite enthält Informationen zur Prävalenz sowie das virusTotal Antivirus-Erkennungs Verhältnis.</span><span class="sxs-lookup"><span data-stu-id="a0da8-239">The page provides prevalence information as well as the VirusTotal antivirus detection ratio.</span></span> <span data-ttu-id="a0da8-240">Sie können die Seite auch zum übermitteln der Datei zur tiefen Analyse verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0da8-240">You can also use the page to submit the file for deep analysis.</span></span>

<span data-ttu-id="a0da8-241">Um eine erkannte Datei im Windows Defender-Sicherheits Center zu suchen, suchen Sie mithilfe der folgenden Advanced Hunting-Abfrage nach allen ASR-Erkennungen:</span><span class="sxs-lookup"><span data-stu-id="a0da8-241">To locate a detected file in Windows Defender Security Center, search for all ASR detections using the following advanced hunting query:</span></span>

```MiscEvents
| where EventTime > ago(7d)
| where ActionType startswith "Asr"
| project FolderPath, FileName, SHA1, InitiatingProcessFolderPath, InitiatingProcessFileName, InitiatingProcessSHA1
```

<span data-ttu-id="a0da8-242">Verwenden Sie den **SHA1** -oder **InitiatingProcessSHA1** in den Ergebnissen, um die Datei mithilfe der universellen Suchleiste im Windows Defender-Sicherheits Center zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a0da8-242">Use the **SHA1** or the **InitiatingProcessSHA1** in the results to search for the file using the universal search bar in Windows Defender Security Center.</span></span>
