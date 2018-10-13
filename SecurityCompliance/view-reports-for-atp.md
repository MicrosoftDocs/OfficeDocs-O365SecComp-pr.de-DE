---
title: Anzeigen von Berichten für Office 365 erweiterte Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
description: Informationen zum Suchen und Verwenden von Berichten für Office 365 erweiterte Threat Protection in das Wertpapier &amp; Compliance Center.
ms.openlocfilehash: 1a0ecb9a6722deb50a491a15f720481a5bb7b0a4
ms.sourcegitcommit: e0c6f99d5514d8da8a70d9bd3616d1a1c0851254
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2018
ms.locfileid: "25552333"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a>Anzeigen von Berichten für Office 365 erweiterte Threat Protection

Wenn Ihre Organisation [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP verfügt), und Sie über die [erforderlichen Berechtigungen](#what-permissions-are-needed-to-view-these-reports)verfügen, können verschiedene ATP-Berichte in das Wertpapier &amp; Compliance Center. (Gehe zu **Berichten** \> **Dashboard**.)
  
![Die Sicherheit &amp; Compliance Center-Dashboard kann Ihnen finden Sie unter, in dem erweiterte Schutz funktionsfähig ist](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
ATP Berichte umfassen [Threat Protection Statusbericht](#threat-protection-status-report), den [Bericht ATP Dateitypen](#atp-file-types-report)und [ATP Nachricht Disposition Bericht](#atp-message-disposition-report). In diesem Artikel wird beschrieben, die ATP-Berichte und enthält Links zu [zusätzlichen Berichte anzeigen](#additional-reports-to-view).
  
## <a name="threat-protection-status-report"></a>Threat Protection Statusbericht

Der **Schutzstatus Bedrohung** -Bericht ist eine einzelne Ansicht, die Informationen zu böswilligen Content und bösartige e-Mails erkannt und blockiert von [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) und [Office 365 ATP](office-365-atp.md)zusammenführt. Der Bericht bietet eine aggregierte Anzahl von eindeutigen e-Mail-Nachrichten mit schädlichem Inhalt (Dateien oder Website-Adressen (URLs)), die vom antischadsoftwaremodul, [0-Stunden automatisch löschen (ZAP)](zero-hour-auto-purge.md)und ATP Features wie [ATP sichere Links](atp-safe-links.md), [ATP Safe blockiert Anlagen](atp-safe-attachments.md), und [ATP Anti-Phishing-Funktionen](atp-anti-phishing.md).

> [!NOTE]
> Ein Bericht Bedrohung Schutzstatus steht Kunden mit [Office 365 ATP](office-365-atp.md) oder [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); Allerdings werden die Informationen, die im Bericht Schutzstatus Bedrohung für ATP-Kunden angezeigt wird wahrscheinlich andere Daten als was EOP-Kunden finden Sie unter möglicherweise enthalten. Beispielsweise wird der Schutzstatus Bedrohung Bericht für ATP-Kunden Informationen zu [schädliche Dateien in SharePoint Online, OneDrive, oder Microsoft-Teams erkannt](atp-for-spo-odb-and-teams.md)enthalten. Diese Angaben ist ATP, so dass Kunden EOP jedoch nicht ATP diese Details in ihre Threat Protection Statusbericht nicht angezeigt werden.
  
Zum Anzeigen des Threat Protection Statusberichts in die Sicherheit &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **Bedrohung Schutzstatus**.
  
![ATP Threat Protection-Statusbericht](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
Um den detaillierten Status für einen Tag erhalten möchten, bewegen Sie den Mauszeiger über dem Diagramm.
  
![ATP Bedrohung Schutzstatus Daten für einen Tag](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
Der Threat Protection Statusbericht zeigt standardmäßig Daten für die letzten sieben Tage. Sie können jedoch **Filter** auswählen und ändern den Datumsbereich zum Anzeigen von Daten für bis zu 90 Tage. 
  
![ATP Bedrohung Schutzstatus Filter](media/4f703369-642b-402b-9758-b9c828283410.png)
  
Klicken Sie im Menü **Ansichtsdaten nach** können auch ändern, welche Informationen im Bericht angezeigt wird. 
  
![Anzeigen von Optionen für ATP Threat Protection-Statusbericht](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a>Dateitypen ATP-Bericht

Der Bericht **ATP Dateitypen** enthält den Typ der Dateien von [ATP sichere Anlagen](atp-safe-attachments.md)als böswilligen entdeckt.
  
So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **ATP Dateitypen**.
  
![Dateitypen ATP-Bericht](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
Wenn Sie über einen bestimmten Tag bewegen, sehen Sie die Aufgliederung der Typen von böswilligen Dateien, die vom [ATP sichere Anlagen](atp-safe-attachments.md) erkannt wurden und [Anti-Spam- &amp; antischadsoftwareschutz in Office 365](anti-spam-and-anti-malware-protection.md).
  
![Dateitypen ATP Report-Daten für einen Tag](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a>ATP Nachricht Disposition Bericht

Der Bericht **ATP Nachricht Disposition** zeigt die Aktionen, die für e-Mail-Nachrichten erstellt wurden, die mit schädlichem Inhalt erkannt wurden. 
  
So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **ATP Nachricht Disposition**.
  
![ATP Nachricht Dispositionsbericht](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
Wenn Sie über eine Leiste im Diagramm bewegen, können Sie sehen, welche Aktionen für ermittelte-e-Mail für diesen Tag ausgeführt wurden.
  
![ATP Nachricht Disposition Report-Daten für einen Tag](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a>Weitere Berichte anzeigen

Zusätzlich zu den in diesem Artikel beschriebenen ATP-Berichten stehen verschiedene andere Berichte, wie in der folgenden Tabelle beschrieben:


|Berichtstyp  |Weitere Informationen  |
|---------|---------|
|**E-Mail-Sicherheitsberichte**wie etwa eine häufigste Absender und Empfänger Bericht, einen Bericht Spoofing Mail und einen Bericht Spamerkennungen. | [Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center](view-email-security-reports.md)        |
|**Explorer** (auch als Bedrohung Explorer bezeichnet wird, ist dies in [Office 365 Bedrohungsanalyse](office-365-ti.md)enthalten)     | [Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center](use-explorer-in-security-and-compliance.md)        |
|**EOP und ATP Ergebnisse** (Dies ist einen benutzerdefinierten Bericht, den Sie mithilfe von PowerShell generieren). Dieser Bericht enthält Informationen, wie Domäne, Datum, Ereignistyp, Richtung, Aktion und Anzahl der Nachrichten an.  | [Get-MailTrafficATPReport-Cmdlet-Referenz](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|**EOP und ATP erkannte** (Dies ist einen benutzerdefinierten Bericht, den Sie mithilfe von PowerShell generieren). Dieser Bericht enthält Details zu schädliche Dateien oder URLs, Phishing-Versuche, Identitätswechsel und andere potenziellen Bedrohungen in e-Mail- oder Dateien.   | [Get-MailDetailATPReport-Cmdlet-Referenz](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a>Welche Berechtigungen sind erforderlich, damit die ATP-Berichte anzeigen?

Um anzuzeigen, und die in diesem Artikel beschriebenen Berichte verwenden, benötigen Sie eine entsprechende Rolle zugewiesen sind, in das Wertpapier &amp; Compliance Center und in der Exchange-Verwaltungskonsole.
  
|**Rollengruppe**|**Wobei zugewiesen**|**Weitere Informationen**|
|:-----|:-----|:-----|
| Eine der folgenden Varianten:  <br/><br/>--Organisationsverwaltung  <br/>--Sicherheitsadministrator  <br/>– Leser Sicherheit  <br/> |Security &amp; Compliance Center  <br/> |[Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md) <br/> |
| Eine der folgenden Varianten:  <br/><br/>--Organisationsverwaltung  <br/>– Organisationsverwaltung nur Ansicht  <br/>--Kontaktobjekts Empfänger-Rolle  <br/>--Verwaltung der Richtlinientreue  <br/> |Exchange Admin Center  <br/> |[Featureberechtigungen in Exchange Online](https://technet.microsoft.com/library/jj200673%28v=exchg.150%29.aspx) <br/> |
   
## <a name="what-if-the-reports-arent-showing-data"></a>Was passiert, wenn nicht die Berichte Daten angezeigt?

Wenn Sie Daten in Ihren ATP-Berichten nicht angezeigt werden, überprüfen Sie, dass Ihre Richtlinien ordnungsgemäß eingerichtet wurden. Ihrer Organisation benötigen [ATP sichere Links](set-up-atp-safe-links-policies.md) und [sichere Anlagen ATP Richtlinien](set-up-atp-safe-attachments-policies.md) definiert, in der Reihenfolge für den Schutz von ATP vorhanden sein. Außerdem finden Sie unter [Anti-Spam and Anti-Malware Protection in Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Verwandte Themen

[Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Erstellen Sie einen Zeitplan für einen Bericht in das Wertpapier &amp; Compliance Center](create-a-schedule-for-a-report.md)
  
[Einrichten von, und Laden Sie einen benutzerdefinierten Bericht in das Wertpapier &amp; Compliance Center](set-up-and-download-a-custom-report.md)
  

