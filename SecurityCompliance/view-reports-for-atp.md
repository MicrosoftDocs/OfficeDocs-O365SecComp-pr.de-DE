---
title: Anzeigen von Berichten für Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection:
- M365-security-compliance
description: Informationen zum Suchen und Verwenden von Berichten für Office 365 Advanced Threat Protection im Security &amp; Compliance Center.
ms.openlocfilehash: c2c1e1134d72bc8c786e0dd783d22adcebeed79b
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/25/2019
ms.locfileid: "30242107"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a>Anzeigen von Berichten für Office 365 Advanced Threat Protection

Wenn Ihre Organisation [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) besitzt und Sie über die [erforderlichen Berechtigungen](#what-permissions-are-needed-to-view-these-reports)verfügen, können Sie im Security &amp; Compliance Center mehrere ATP-Berichte verwenden. (Wechseln Sie zum **Dashboard** **Berichte** \> .)
  
![Mit dem &amp; Security Compliance Center-Dashboard können Sie erkennen, wo Advanced Threat Protection funktioniert.](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Zu den ATP-Berichten gehören der Bericht über den [Status von Bedrohungsschutz](#threat-protection-status-report), der [Bericht ATP-Dateitypen](#atp-file-types-report)und der Bericht zur Verteilung der ATP-nach [richten](#atp-message-disposition-report). Dieser Artikel beschreibt die ATP-Berichte und enthält Links zu [weiteren Berichten, die Sie anzeigen können](#additional-reports-to-view).
  
## <a name="threat-protection-status-report"></a>Status Bericht zum BedrohungsSchutz

Der **Status** Bericht zu Bedrohungen ist eine einzelne Ansicht, in der Informationen zu böswilligen Inhalten und bösartigen e-Mails zusammengeführt werden, die von [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) und [Office 365 ATP](office-365-atp.md)erkannt und blockiert wurden. Der Bericht bietet eine aggregierte Anzahl von eindeutigen e-Mail-Nachrichten mit bösartigen Inhalten (Dateien oder Websiteadressen (URLs)), die vom Antischadsoftware-Modul blockiert wurden, [Zero-Hour Auto Purge (zap)](zero-hour-auto-purge.md)und ATP-Funktionen wie ATP- [sichere Links](atp-safe-links.md), [ATP-Safe ](atp-safe-attachments.md)Und [ATP-Phishing-Funktionen](atp-anti-phishing.md).

> [!NOTE]
> Ein Bericht über den BedrohungsSchutz steht Kunden zur Verfügung, die entweder [Office 365 ATP](office-365-atp.md) oder [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP) haben; die Informationen, die im Status Bericht zur Gefahrenabwehr für ATP-Kunden angezeigt werden, enthalten jedoch wahrscheinlich unterschiedliche Daten als die EOP-Kunden. Beispielsweise enthält der Status Bericht über Bedrohungen für ATP-Kundeninformationen zu [schädlichen Dateien, die in SharePoint Online, OneDrive oder Microsoft Teams erkannt](atp-for-spo-odb-and-teams.md)wurden. Diese Informationen sind spezifisch für ATP, sodass Kunden, die über EOP, jedoch nicht über ATP verfügen, diese Details nicht in Ihrem Status Bericht über den BedrohungsSchutz sehen.
  
Zum Anzeigen des Statusberichts zum Bedrohungsschutz wechseln Sie im [Security &amp; Compliance Center](https://protection.office.com)zu **Status des Threat Protection**- **Dashboards** \> für **Berichte** \> .
  
![Status Bericht zum ATP-BedrohungsSchutz](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
Wenn Sie einen detaillierten Status für einen Tag erhalten möchten, bewegen Sie den Mauszeiger über das Diagramm.
  
![Status Daten für den ATP-BedrohungsSchutz für einen Tag](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
Standardmäßig werden im Bericht über den Status des BedrohungsSchutzes Daten für die letzten sieben Tage angezeigt. Sie können jedoch **Filter** auswählen und den Datums Umfang ändern, um Daten für bis zu 90 Tage anzuzeigen. 
  
![Status Filter für ATP-BedrohungsSchutz](media/4f703369-642b-402b-9758-b9c828283410.png)
  
Sie können auch das Menü **Daten anzeigen** , um zu ändern, welche Informationen im Bericht angezeigt werden. 
  
![Anzeigeoptionen für den Status Bericht zum ATP-BedrohungsSchutz](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a>Bericht "ATP-Dateitypen"

Der Bericht **ATP-Dateitypen** zeigt Ihnen den Typ der Dateien an, die von [ATP Safe Attachments](atp-safe-attachments.md)als bösartig erkannt wurden.
  
Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu **Berichte** \> **-Dashboard** \> - **ATP-Dateitypen**.
  
![Bericht "ATP-Dateitypen"](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
Wenn Sie den Mauszeiger über einen bestimmten Tag bewegen, sehen Sie die Aufschlüsselung der Arten von bösartigen Dateien, die durch [ATP Safe Attachments](atp-safe-attachments.md) und [Anti-Spam &amp; Anti-Malware Protection in Office 365](anti-spam-and-anti-malware-protection.md)erkannt wurden.
  
![ATP-Dateitypen Berichtsdaten für einen Tag](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a>Bericht zur ATP-Nachrichten Disposition

Der Bericht zur Bereitstellung von ATP-Nachrichten zeigt Ihnen die Aktionen an, die für e-Mail- **Nachricht** ausgeführt wurden, die als bösartige Inhalte erkannt wurden. 
  
Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu **Berichte** \> **-Dashboard** \> **ATP Message Disposition**.
  
![Bericht zur ATP-Nachrichten Disposition](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
Wenn Sie auf einen Balken im Diagramm zeigen, können Sie sehen, welche Aktionen für erkannte e-Mails für diesen Tag ausgeführt wurden.
  
![ATP-Nachrichten Disposition-Berichtsdaten für einen Tag](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a>Zusätzliche Berichte zum Anzeigen

Zusätzlich zu den in diesem Artikel beschriebenen ATP-Berichten stehen mehrere weitere Berichte zur Verfügung, wie in der folgenden Tabelle beschrieben:

|Berichtstyp  |Weitere Informationen  |
|---------|---------|
|**E-Mail-Sicherheitsberichte**, wie beispielsweise ein Bericht über Top-Absender und-Empfänger, ein spoof-e-Mail-Bericht und ein Spam Erkennungs Bericht. | [Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center](view-email-security-reports.md)        |
|**Explorer** (auch als Bedrohungs-Explorer bezeichnet, ist dies in [Office 365 Threat Intelligence](office-365-ti.md)enthalten)     | [Verwenden des Explorers im Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md)        |
|**EoP und ATP-Ergebnisse** (Hierbei handelt es sich um einen benutzerdefinierten Bericht, den Sie mithilfe von PowerShell generieren). Dieser Bericht enthält Informationen wie Domäne, Datum, Ereignistyp, Richtung, Aktion und Nachrichtenanzahl.  | [Get-MailTrafficATPReport-Cmdlet-Referenz](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|**EoP und ATP-Ermittlungen** (Hierbei handelt es sich um einen benutzerdefinierten Bericht, den Sie mithilfe von PowerShell generieren). Dieser Bericht enthält Details zu schädlichen Dateien oder URLs, Phishing-versuchen, Identitätswechsel und anderen potenziellen Bedrohungen in e-Mails oder Dateien.   | [Get-MailDetailATPReport-Cmdlet-Referenz](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a>Welche Berechtigungen sind erforderlich, um die ATP-Berichte anzuzeigen?

Um die in diesem Artikel beschriebenen Berichte anzuzeigen und zu verwenden, **müssen Sie eine entsprechende Rolle sowohl für das Security &amp; Compliance Center als auch für das Exchange Admin Center zugewiesen haben**.

- Für das Security &amp; Compliance Center muss eine der folgenden Rollen zugewiesen sein:
    - Organisationsverwaltung
    - Sicherheits Administrator (kann im Azure Active Directory Admin Center[https://aad.portal.azure.com](https://aad.portal.azure.com)zugewiesen werden)
    - Sicherheits Leser

- Für Exchange Online müssen Sie über eine der folgenden Rollen verfügen, die entweder in der Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() oder mit PowerShell-Cmdlets zugewiesen sind (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Organisationsverwaltung
    - Organisationsverwaltung mit Leserechten
    - Rolle „Empfänger mit Leserechten“
    - Verwaltung der Richtlinientreue

Weitere Informationen finden Sie in den folgenden Ressourcen:

- [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Featureberechtigungen in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a>Was geschieht, wenn die Berichte keine Daten anzeigen?

Wenn in ihren ATP-Berichten keine Daten angezeigt werden, überprüfen Sie, ob Ihre Richtlinien ordnungsgemäß eingerichtet sind. Ihre Organisation muss über [ATP Safe Links Policies](set-up-atp-safe-links-policies.md) und [ATP Safe Attachments-Richtlinien](set-up-atp-safe-attachments-policies.md) verfügen, die für den ATP-Schutz definiert sind. Weitere Informationen finden Sie unter [Anti-Spam and Anti-Malware Protection in Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Verwandte Themen

[Berichte und Einblicke im Office 365 &amp; Security Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Erstellen eines Zeitplans für einen Bericht im &amp; Security Compliance Center](create-a-schedule-for-a-report.md)
  
[Einrichten und Herunterladen eines benutzerdefinierten Berichts im Security &amp; Compliance Center](set-up-and-download-a-custom-report.md)
  

