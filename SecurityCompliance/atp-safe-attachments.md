---
title: Office 365 ATP Safe Attachments
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/08/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
description: Mit der Funktion "sichere Anlagen" können Sie e-Mail-Anhänge per Mausklick überprüfen. Verwenden Sie sichere Anlagen, um Ihre Organisation vor schädlichen Dateien zu schützen, die Personen in e-Mails senden oder empfangen.
ms.openlocfilehash: 9e0a53acb55e4fcb81c071f3decaccde3b45c96a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215185"
---
# <a name="office-365-atp-safe-attachments"></a>Office 365 ATP Safe Attachments

## <a name="overview-of-office-365-atp-safe-attachments"></a>Übersicht über Office 365 ATP Safe Attachments

ATP Safe Attachments (zusammen mit [ATP Safe Links](atp-safe-links.md)) ist Teil von [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP). Das Feature ATP Safe Attachments prüft, ob e-Mail-Anlagen bösartig sind, und führt dann Maßnahmen zum Schutz Ihrer Organisation aus. Das Feature für sichere Anlagen in ATP schützt Ihre Organisation gemäß den [Richtlinien für ATP Safe Attachments](set-up-atp-safe-attachments-policies.md) , die von ihren Office 365-globalen oder Sicherheitsadministratoren festgelegt werden. 
  
Der ATP-Schutz kann auch auf Dateien in SharePoint Online, OneDrive for Business und Microsoft Teams ausgedehnt werden. Weitere Informationen finden Sie unter [Office 365 Advanced Threat Protection for SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md).
       
## <a name="how-it-works"></a>Funktionsweise

Das Feature für sichere Anlagen für ATP prüft e-Mail-Anlagen für Personen in Ihrer Organisation. Wenn eine ATP-Richtlinie für sichere Anlagen vorhanden ist und eine Person, die von dieser Richtlinie erfasst wird, Ihre e-Mails in Office 365 anzeigt, werden Ihre e-Mail-Anhänge überprüft, und es werden entsprechende Aktionen basierend auf Ihren Richtlinien für ATP-sichere Anlagen ausgeführt. Je nachdem, wie Ihre Richtlinien definiert werden, können die Benutzer weiterhin arbeiten, ohne jemals zu wissen, dass Sie bösartige Dateien gesendet haben.
  
Hier sind zwei Beispiele für sichere ATP-Anlagen am Arbeitsplatz.
  
- **Beispiel 1: e-Mail-Anlage** Angenommen, Lee erhält eine e-Mail-Nachricht mit einer Anlage. Es ist für Lee nicht offensichtlich, ob diese Anlage sicher ist oder tatsächlich Schadsoftware enthält, mit der Schutz Benutzeranmeldeinformationen gestohlen werden sollen. In der Organisation von Lee hat ein Sicherheitsadministrator vor wenigen Tagen eine ATP-Richtlinie für sichere Anlagen definiert. Mit dem Feature ATP Safe Attachments wird die e-Mail-Anlage in einer virtuellen Umgebung geöffnet und getestet, bevor Sie von Lee empfangen wird. Wenn die Anlage als bösartig festgelegt wird, wird Sie automatisch entfernt. Wenn die Anlage sicher ist, wird Sie wie erwartet geöffnet, wenn Lee darauf klickt. 
    
- **Beispiel 2: Datei in SharePoint Online** Angenommen, Jean hat eine Datei erhalten und Sie in eine Bibliothek in SharePoint Online hochgeladen. Jean teilt den Link zur Datei mit dem Rest des Teams, ohne zu wissen, dass die Datei tatsächlich bösartig ist. Glücklicherweise erkennt [ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md) die bösartige Datei und blockiert Sie. Ein paar Tage später geht Chris zum Öffnen des Dokuments. Chris kann zwar sehen, dass die Datei vorhanden ist, aber Chris kann Sie nicht öffnen oder freigeben, wodurch Chriss Computer und andere Personen aus der Schadsoftware verhindert werden. 
    
Die Überprüfung von ATP Safe Attachments erfolgt in derselben Region, in der sich Ihre Office 365-Daten befinden. Weitere Informationen zur Geografie des Rechenzentrums finden Sie unter [wo befinden sich Ihre Daten?](https://products.office.com/where-is-your-data-located?geo=All) 

ATP-Richtlinien für sichere Anlagen können auf bestimmte Personen oder Gruppen in Ihrer Organisation oder auf Ihre gesamte Domäne angewendet werden. Darüber hinaus können ATP-Richtlinien für sichere Anlagen für die Verwendung von Platzhalter Anlagen konfiguriert werden, während tatsächliche Anlagen gescannt werden. Weitere Informationen finden Sie unter **[Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)**. 
  
## <a name="how-to-get-atp-safe-attachments"></a>So erhalten Sie ATP Safe Attachments

Stellen Sie zunächst sicher, dass Ihr Abonnement [Advanced Threat Protection](office-365-atp.md)enthält. ATP ist in Abonnements wie [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht Office 365 ATP enthält, können Sie möglicherweise ATP als Add-on erwerben. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

Stellen Sie als nächstes sicher, dass Ihre ATP-Richtlinien für sichere Anlagen definiert sind. (Siehe [Einrichten von Office 365 ATP Safe Attachments Policies](set-up-atp-safe-attachments-policies.md)) ATP Safe Attachments-Features sind aktiv, wenn:
  
- Die Richtlinien für ATP-sichere Anlagen sind eingerichtet. (Siehe [Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md).)
    
- Benutzer haben sich mit Ihrem Geschäfts-oder Schulkonto bei Office 365 angemeldet. (Siehe [Anmelden bei Office oder office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)

Um ATP-Richtlinien zu definieren (oder zu bearbeiten), muss Ihnen eine entsprechende Rolle zugewiesen werden. Einige Beispiele werden in der folgenden Tabelle beschrieben:

|Rolle  |Wo/wie zugewiesen  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>Wie Sie wissen, ob ATP Safe Attachments Protection vorhanden ist

Nachdem Sie [Ihre ATP-Richtlinien für sichere Anlagen definiert (oder überprüft)](set-up-atp-safe-attachments-policies.md)haben, können Sie mithilfe von [Berichten zu Advanced Threat Protection](view-reports-for-atp.md)eine gute Möglichkeit sehen, wie der Dienst funktioniert.
  
In der folgenden Tabelle werden einige Beispielszenarien beschrieben. In allen diesen Fällen wird davon ausgegangen, dass die Organisation über ein Office 365-Abonnement verfügt, in dem Advanced Threat Protection enthalten ist.
  
|**Beispielszenario**|**Gilt in diesem Fall ATP Safe Attachments Protection?**|
|:-----|:-----|
|Pat es Organisation verfügt über Office 365 Enterprise E5, aber es wurden noch keine Richtlinien für sichere ATP-Anlagen definiert.  <br/> |Nein. Obwohl das Feature verfügbar ist, muss mindestens eine ATP-Richtlinie für sichere Anlagen definiert werden, damit der Schutz von ATP-Anlagen sicher ist.  <br/> |
|Lee ist ein Mitarbeiter in der Vertriebsabteilung bei Contoso. Lees Organisation verfügt über eine Richtlinie für sichere ATP-Anlagen, die nur für Mitarbeiter von Finance gilt.  <br/> |Nein. In diesem Fall würden Finanzmitarbeiter über ATP Safe Attachments Protection verfügen, aber andere Mitarbeiter, einschließlich der Vertriebsabteilung, würden erst dann eine Richtlinie definieren, die diese Gruppen enthält.  <br/> |
|Gestern richtete ein Office 365-Administrator bei der Organisation von Jean eine ATP-Richtlinie für sichere Anlagen ein, die für alle Mitarbeiter gilt. Heute hat Jean eine e-Mail-Nachricht erhalten, die eine Anlage enthält.  <br/> |Ja. In diesem Beispiel verfügt Jean über eine Lizenz für Advanced Threat Protection, und eine Richtlinie zu sicheren ATP-Anlagen, die Jean enthält, wurde definiert. In der Regel dauert es ungefähr 30 Minuten, bis eine neue Richtlinie über Rechenzentren hinweg wirksam wird. Da in diesem Fall ein Tag vergangen ist, sollte die Richtlinie wirksam sein.  <br/> |
|Chris es Organisation verfügt über Office 365 Enterprise E5 mit den Richtlinien für sichere ATP-Anlagen für alle Benutzer in der Organisation. Chris erhält eine e-Mail mit einer Anlage und leitet die Nachricht an andere Personen weiter, die sich außerhalb der Organisation befinden.  <br/> |ATP Safe Attachments Protection ist für Nachrichten vorhanden, die Chris empfängt. Wenn in den Organisationen des Empfängers auch ATP-Richtlinien für sichere Anlagen vorhanden sind, wird die Nachricht, dass Chris Forwards für diese Richtlinien gilt, wenn die weitergeleitete Nachricht eingeht.  <br/> |
|In Jamies Organisation sind ATP-Richtlinien für sichere Anlagen vorhanden, und [ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md) wurde aktiviert. Jamie geht davon aus, dass jede Datei in SharePoint Online gescannt wurde und sicher geöffnet oder heruntergeladen werden kann.<br/> |Der sichere ATP-Anlagenschutz ist gemäß den definierten Richtlinien vorhanden. Dies bedeutet jedoch nicht, dass jede einzelne Datei in SharePoint Online, OneDrive for Business oder Microsoft Teams gescannt wird. (Weitere Informationen finden Sie unter [ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md).)<br/> |
   
## <a name="submitting-files-for-malware-analysis"></a>Übermitteln von Dateien für die Malware Analyse

- Wenn Sie eine Datei erhalten, die von Microsoft analysiert werden soll, besuchen Sie [Datei für die Malware Analyse einreichen](https://aka.ms/wdsi/submit).

- Wenn Sie eine e-Mail-Nachricht (mit oder ohne Anlage) erhalten, die Sie zur Analyse an Microsoft übermitteln möchten, verwenden Sie das [Add-in Berichtnachricht](enable-the-report-message-add-in.md).
  
