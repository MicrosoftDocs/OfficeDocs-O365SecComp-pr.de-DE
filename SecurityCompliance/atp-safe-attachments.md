---
title: Office 365 ATP sichere Anlagen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 11/08/2018
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
description: Die sichere Anlagen-Funktion bietet Zeit des klicken Sie auf Überprüfung von e-Mail-Anlagen. Verwenden sichere Anlagen in Ihrer Organisation vor böswilligen Dateien schützen senden oder Empfangen von e-Mail.
ms.openlocfilehash: e09c9abec7485408f102fa6c20d14b91d9c2bf36
ms.sourcegitcommit: 147768bbe44c8c98c02fa29ae9d882cee4ec2d6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2018
ms.locfileid: "26238437"
---
# <a name="office-365-atp-safe-attachments"></a>Office 365 ATP sichere Anlagen

## <a name="overview-of-office-365-atp-safe-attachments"></a>Übersicht über Office 365 ATP sichere Anlagen

ATP sichere Anlagen (zusammen mit [Sicheren Links ATP](atp-safe-links.md)) ist Teil der [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP). Das Feature ATP sichere Anlagen überprüft, ob e-Mail-Anlagen böswilligen sind und nimmt dann Aktion zum Schutz Ihrer Organisation. Das Feature ATP sichere Anlagen schützt Ihr Unternehmen gemäß den [Richtlinien ATP sichere Anlagen](set-up-atp-safe-attachments-policies.md) , die von Ihrem Office 365 globaler oder Sicherheitsadministratoren festgelegt sind. 
  
ATP Protection wurde vor kurzem in Dateien in SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams, erweitert. Finden Sie weitere Informationen finden Sie unter [Office 365 erweiterte Bedrohungsschutz für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md).
       
## <a name="how-it-works"></a>Funktionsweise

Das Feature ATP sichere Anlagen überprüft e-Mail-Anlagen für die Personen in Ihrer Organisation. Wenn eine Richtlinie ATP sichere Anlagen vorhanden ist und eine Person im Rahmen dieser Richtlinie ihre e-Mails in Office 365 anzeigt, ihre e-Mail-Anlagen werden überprüft und entsprechende Aktionen ausgeführt werden, basierend auf Ihren Richtlinien ATP sichere Anlagen. Je nach Ihrer Richtlinien wie definiert sind können Benutzer arbeiten weiterhin, ohne jemals wissen, dass sie schädliche Dateien gesendet wurden.
  
Hier sind zwei Beispiele für sichere Anlagen ATP bei der Arbeit.
  
- **Beispiel 1: E-Mail-Anlage** Nehmen Sie an, dass Kelly eine e-Mail-Nachricht empfängt, die eine Anlage enthält. Ist es nicht eindeutig, Kelly gibt an, ob, dass Anlage sicherer ist oder Malware, die für Kelly Benutzeranmeldeinformationen zu stehlen tatsächlich enthält. In Kelly-Organisation definiert ein Sicherheitsadministrator eine Richtlinie für den sicheren Anlagen ATP binnen weniger Tage zurückliegt. Mit dem Feature ATP sichere Anlagen ist die e-Mail-Anlage geöffnet und in einer virtuellen Umgebung getestet werden, bevor Kelly er empfängt. Wenn die Anlage böswilligen werden bestimmt wird, wird sie automatisch entfernt. Wenn die Anlage sicher ist, wird geöffnet wie erwartet, wenn Kelly darauf klickt. 
    
- **In Beispiel 2: Datei in SharePoint Online** Nehmen Sie an, dass Jean erhalten eine Datei, und es in einer Dokumentbibliothek in SharePoint Online hochgeladen werden. Jean teilt die Verknüpfung mit der Datei mit dem Rest des Teams, nicht wissen, dass die Datei tatsächlich böswilligen ist. Zum Glück [ATP für SharePoint, OneDrive, und Microsoft-Teams,](atp-for-spo-odb-and-teams.md) die bösartige Datei erkennt und blockiert. Einige Tage später, geht Chris zum Öffnen des Dokuments. Chris kann zwar, dass die Datei vorhanden ist sehen, wird "Chris" kann nicht geöffnet oder weitergeben, wodurch die bösartige Datei Chris Computer und andere gehindert. 
    
Sichere Anlagen ATP Richtlinien können auf bestimmte Benutzer oder Gruppen in Ihrer Organisation oder an Ihre gesamte Domäne angewendet werden. Weitere Informationen finden Sie finden Sie unter **[Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)**. 
  
## <a name="how-to-get-atp-safe-attachments"></a>Wie ATP sichere Anlagen abrufen

Das Feature ATP sichere Anlagen ist Teil der [Erweiterte Schutz](office-365-atp.md), die in Microsoft 365 Enterprise und Office 365 Enterprise E5 Microsoft 365 Business enthalten ist. 
  
Das Feature ATP sichere Anlagen gültig, wenn:
  
- Sichere Anlagen ATP Richtlinien sind eingerichtet. (Siehe [sichere Anlagen ATP Richtlinien in Office 365 einrichten](set-up-atp-safe-attachments-policies.md).)
    
- Benutzer haben in Office 365 mit ihrer Arbeit oder Schule Konto angemeldet. (Siehe [Office oder Office 365 anmelden](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)
    
## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>Wie Sie feststellen, ob die sichere Anlagen ATP Schutz vorhanden ist

 In der Reihenfolge für den Schutz von ATP sichere Anlagen vorhanden sein muss [ATP sichere Anlagen Richtlinien](set-up-atp-safe-attachments-policies.md) definiert werden. 
  
[Anzeigen von Berichten für erweiterte Schutz](view-reports-for-atp.md)ist eine gute Möglichkeit, finden Sie unter wie der Dienst funktioniert wird.
  
Darüber hinaus werden in der folgenden Tabelle einige Beispielszenarien beschrieben. In allen Fällen wird davon ausgegangen, dass die Organisation über Office 365 Enterprise E5, verfügt der erweiterte Schutz enthält.
  
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
  
