---
title: Office 365 ATP sichere Anlagen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/08/2019
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
description: Die sichere Anlagen-Funktion bietet Zeit des klicken Sie auf Überprüfung von e-Mail-Anlagen. Verwenden sichere Anlagen in Ihrer Organisation vor böswilligen Dateien schützen senden oder Empfangen von e-Mail.
ms.openlocfilehash: 45cd3b74b67d7ff8735da7a703ff14c4c517341f
ms.sourcegitcommit: c1c41744c2de89c9e172f817c8f73bb0ada81a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2019
ms.locfileid: "29792230"
---
# <a name="office-365-atp-safe-attachments"></a>Office 365 ATP sichere Anlagen

## <a name="overview-of-office-365-atp-safe-attachments"></a>Übersicht über Office 365 ATP sichere Anlagen

ATP sichere Anlagen (zusammen mit [Sicheren Links ATP](atp-safe-links.md)) ist Teil der [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP). Das Feature ATP sichere Anlagen überprüft, ob e-Mail-Anlagen böswilligen sind und nimmt dann Aktion zum Schutz Ihrer Organisation. Das Feature ATP sichere Anlagen schützt Ihr Unternehmen gemäß den [Richtlinien ATP sichere Anlagen](set-up-atp-safe-attachments-policies.md) , die von Ihrem Office 365 globaler oder Sicherheitsadministratoren festgelegt sind. 
  
ATP Schutz kann auch auf Dateien in SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams, erweitert werden. Finden Sie weitere Informationen finden Sie unter [Office 365 erweiterte Bedrohungsschutz für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md).
       
## <a name="how-it-works"></a>Funktionsweise

Das Feature ATP sichere Anlagen überprüft e-Mail-Anlagen für die Personen in Ihrer Organisation. Wenn eine Richtlinie ATP sichere Anlagen vorhanden ist und eine Person im Rahmen dieser Richtlinie ihre e-Mails in Office 365 anzeigt, ihre e-Mail-Anlagen werden überprüft und entsprechende Aktionen ausgeführt werden, basierend auf Ihren Richtlinien ATP sichere Anlagen. Je nach Ihrer Richtlinien wie definiert sind können Benutzer arbeiten weiterhin, ohne jemals wissen, dass sie schädliche Dateien gesendet wurden.
  
Hier sind zwei Beispiele für sichere Anlagen ATP bei der Arbeit.
  
- **Beispiel 1: E-Mail-Anlage** Nehmen Sie an, dass Kelly eine e-Mail-Nachricht empfängt, die eine Anlage enthält. Ist es nicht eindeutig, Kelly gibt an, ob, dass Anlage sicherer ist oder Malware, die für Kelly Benutzeranmeldeinformationen zu stehlen tatsächlich enthält. In Kelly-Organisation definiert ein Sicherheitsadministrator eine Richtlinie für den sicheren Anlagen ATP binnen weniger Tage zurückliegt. Mit dem Feature ATP sichere Anlagen ist die e-Mail-Anlage geöffnet und in einer virtuellen Umgebung getestet werden, bevor Kelly er empfängt. Wenn die Anlage böswilligen werden bestimmt wird, wird sie automatisch entfernt. Wenn die Anlage sicher ist, wird geöffnet wie erwartet, wenn Kelly darauf klickt. 
    
- **In Beispiel 2: Datei in SharePoint Online** Nehmen Sie an, dass Jean erhalten eine Datei, und es in einer Dokumentbibliothek in SharePoint Online hochgeladen werden. Jean teilt die Verknüpfung mit der Datei mit dem Rest des Teams, nicht wissen, dass die Datei tatsächlich böswilligen ist. Zum Glück [ATP für SharePoint, OneDrive, und Microsoft-Teams,](atp-for-spo-odb-and-teams.md) die bösartige Datei erkennt und blockiert. Einige Tage später, geht Chris zum Öffnen des Dokuments. Chris kann zwar, dass die Datei vorhanden ist sehen, wird "Chris" kann nicht geöffnet oder weitergeben, wodurch die bösartige Datei Chris Computer und andere gehindert. 
    
ATP sichere Anlagen scannen akzeptiert platzieren im selben Bereich, in dem sich Ihre Office 365-Daten befinden. Weitere Informationen zum Data Center Geografie, finden Sie unter [, wo wird Ihre Daten befinden?](https://products.office.com/where-is-your-data-located?geo=All) 

Sichere Anlagen ATP Richtlinien können auf bestimmte Benutzer oder Gruppen in Ihrer Organisation oder an Ihre gesamte Domäne angewendet werden. Darüber hinaus können ATP sichere Anlagen Richtlinien konfiguriert werden, um Platzhalter für Anlagen verwenden, während der tatsächliche Anlagen gescannt werden. Weitere Informationen finden Sie finden Sie unter **[Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)**. 
  
## <a name="how-to-get-atp-safe-attachments"></a>Wie ATP sichere Anlagen abrufen

Stellen Sie zunächst sicher, dass Ihr Abonnement [Erweiterte Threat Protection](office-365-atp.md)umfasst. ATP ist in Abonnements, wie beispielsweise [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement, die nicht in Office 365 ATP enthalten ist umfasst, können Sie potenziell ATP als Add-on erwerben. Weitere Informationen finden Sie unter [Erweiterte Threat Protection von Office 365-Pläne und zu Preisen](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 erweiterte Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

Im nächsten Schritt stellen Sie sicher, dass alle Richtlinien ATP sichere Anlagen definiert sind. (Siehe [Einrichten von Richtlinien für Office 365 ATP sichere Anlagen](set-up-atp-safe-attachments-policies.md)) Sichere Anlagen ATP Features sind in den aktiv:
  
- Sichere Anlagen ATP Richtlinien sind eingerichtet. (Siehe [sichere Anlagen ATP Richtlinien in Office 365 einrichten](set-up-atp-safe-attachments-policies.md).)
    
- Benutzer haben in Office 365 mit ihrer Arbeit oder Schule Konto angemeldet. (Siehe [Office oder Office 365 anmelden](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)

Um ATP Richtlinien definieren (oder bearbeiten), müssen Sie eine der in der folgenden Tabelle beschriebenen Rollen zugewiesen werden:

|Rolle  |WHERE/wie zugewiesen.  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die zum Erwerben von Office 365 angemeldet ist ein globaler Administrator in der Standardeinstellung. (Siehe [zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) , um mehr zu erfahren.)         |
|Sicherheitsadministrator |Azure Active Directory-Verwaltungskonsole ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Verwaltung von Exchange Online-Organisation |Exchange-Verwaltungskonsole ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>Wie Sie feststellen, ob die sichere Anlagen ATP Schutz vorhanden ist

Nachdem Sie [Ihre ATP sichere Anlagen Richtlinien definiert (oder überprüft)](set-up-atp-safe-attachments-policies.md)haben, ist eine gute Möglichkeit, finden Sie unter wie der Dienst funktioniert durch [Anzeigen von Berichten für erweiterte Threat Protection](view-reports-for-atp.md).
  
In der folgenden Tabelle werden einige Beispielszenarien beschrieben. In allen Fällen wird davon ausgegangen, dass die Organisation über ein Office 365-Abonnement verfügt, der erweiterte Schutz enthält.
  
|**Beispielszenario**|**In diesem Fall wird ATP sichere Anlagen Protection werden angewendet?**|
|:-----|:-----|
|Pats Organisation hat Office 365 Enterprise E5, aber niemand verfügt über alle Richtlinien noch für sichere Anlagen ATP definiert.  <br/> |Nein. Obwohl das Feature verfügbar ist, muss mindestens eine sichere Anlagen ATP-Richtlinie in der Reihenfolge für den Schutz von ATP sichere Anlagen vorhanden sein definiert werden.  <br/> |
|Kelly ist ein Mitarbeiter der Abteilung "sales" bei Contoso. Kelly Organisation hat eine sichere Anlagen ATP-Richtlinie vorhanden, die nur für Mitarbeiter der Finanzabteilung gelten.  <br/> |Nein. In diesem Fall Mitarbeiter der Finanzabteilung müssten ATP sichere Anlagen Schutz, während andere Mitarbeiter, die IT-Abteilung, einschließlich würde, nicht bis Richtlinien, die diese Gruppen enthalten definiert sind.  <br/> |
|Ein Office 365-Administrator bei Jeans Organisation eingerichtet gestern, eine sichere Anlagen ATP-Richtlinie, die für alle Mitarbeiter gilt. Jean empfangen heute, eine e-Mail-Nachricht, die eine Anlage enthält.  <br/> |Ja. In diesem Beispiel Jean verfügt über eine Lizenz für erweiterte Threat Protection und eine sichere Anlagen ATP-Richtlinie, die Jean enthält definiert wurde. In der Regel nimmt etwa 30 Minuten für eine neue Richtlinie wirksam in Rechenzentren; Da in diesem Fall ein Tag verstrichen ist, sollte die Richtlinie aktiviert sein.  <br/> |
|Chris Organisation sind Office 365 Enterprise E5 mit ATP sichere Anlagen Richtlinien für alle Benutzer in der Organisation. Chris erhält eine e-Mail-Nachricht, die eine Anlage enthält, und leitet die Nachricht an andere Personen, die sich außerhalb der Organisation befinden.  <br/> |Sichere Anlagen ATP Schutz ist für Nachrichten, die Chris empfängt. Wenn der Empfänger Organisationen auch ATP sichere Anlagen Richtlinien erstellt wurden, klicken Sie dann wäre die Nachricht, die Chris weiterleitet können diese Richtlinien beim Eintreffen der weitergeleiteten Nachricht.  <br/> |
|Fraus Organisation ATP sichere Anlagen Richtlinien direkt, und eingeschaltet [ATP für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md) . Frau wird davon ausgegangen, dass jede Datei in SharePoint Online überprüft worden ist und sicher öffnen oder herunterladen.<br/> |Sichere Anlagen ATP Schutz ist direkten gemäß den Richtlinien, die definiert sind. Dies bedeutet jedoch nicht, dass jede einzelne Datei in SharePoint Online, OneDrive for Business oder Microsoft-Teams, überprüft wird. (Weitere Informationen finden Sie finden Sie unter [ATP für SharePoint, OneDrive, und Microsoft-Teams,](atp-for-spo-odb-and-teams.md).)<br/> |
   
## <a name="submitting-files-for-malware-analysis"></a>Senden von Dateien für die Analyse der malware

- Wenn Sie eine Datei, die Sie Microsoft zur Analyse stellen möchten erhalten, besuchen Sie [senden eine Datei für die Schadsoftware Analyse](https://aka.ms/wdsi/submit).

- Wenn Sie eine e-Mail-Nachricht (mit oder ohne Anlagen), die Sie für die Analyse an Microsoft senden möchten erhalten, verwenden Sie das [Bericht-add-in](enable-the-report-message-add-in.md).
  
