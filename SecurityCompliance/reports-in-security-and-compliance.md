---
title: Berichte im Security & Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: 'Verwenden Sie das Security & Compliance Center, um verschiedene Berichte für Ihre SharePoint Online-und Exchange Online-Organisation sowie Azure Active Directory-Berichte zu erhalten.  '
ms.openlocfilehash: b902ce8e44e20fdb9e5fc22189ca07b6168be329
ms.sourcegitcommit: 6c9340e4eb221bf81472ff3f1ae25ae21aaf5297
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2019
ms.locfileid: "31813916"
---
# <a name="reports-in-the-security--compliance-center"></a>Berichte im Security & Compliance Center

Auf der Seite **Berichte anzeigen** im Security _AMP_ Compliance Center können Sie schnell auf Überwachungsberichte für Ihre SharePoint Online-und Exchange Online-Organisationen zugreifen. Sie können auf der Seite **Berichte anzeigen** auch auf Azure Active Directory (AD)-Benutzeranmelde Berichte, Benutzer Aktivitätsberichte und das Azure AD-Überwachungsprotokoll zugreifen. Dies liegt daran, dass Ihr bezahltes Office 365-Abonnement ein kostenloses Abonnement für Microsoft Azure enthält. Wenn Sie versuchen, auf diese Azure-Berichte zuzugreifen, müssen Sie einen einmaligen Registrierungsvorgang ausführen. 
  
> [!TIP]
> Weitere Berichte zu Aktivitäten in Ihrer Office 365-Organisation finden Sie unter [Aktivitätsberichte im Microsoft 365 Admin Center](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263). 
  
 **Bevor Sie beginnen:**
  
Sie benötigen die folgenden Berechtigungen zum Anzeigen von Berichten im Security & Compliance Center.
  
- Sie müssen der Sicherheits Lese Rolle in der Exchange-Verwaltungskonsole (EAC) zugewiesen sein, um Berichte im Security & Compliance Center anzuzeigen. Diese Rolle wird standardmäßig den Rollengruppen "Organisationsverwaltung" und "Sicherheits Leser" in der Exchange-Verwaltungskonsole zugewiesen.
    
- Sie müssen im Security & Compliance Center über die Verwaltungsrolle "View-Only DLP Compliance Management" verfügen, um DLP-Berichte im Security & Compliance Center anzuzeigen. Diese Rolle wird standardmäßig den Rollengruppen "Compliance-Administrator", "Organisationsverwaltung", "Sicherheitsadministrator" und "Sicherheits Leser" im Security & Compliance Center zugewiesen.

- Darüber hinaus müssen Sie die Rolle "nur anzeigen" in der Exchange-verwaltungsKONSOLE besitzen, um DLP-Berichte in der Exchange-verwaltungsKONSOLE anzuzeigen. Diese Rolle wird standardmäßig den Rollengruppen "Compliance Management", "Organization Management" und "View-Only Organization Management" in der Exchange-verwaltungsKONSOLE zugewiesen.
  
 **So öffnen Sie die Seite Berichte anzeigen im Security & Compliance Center:**
  
1. Wechseln Sie zu [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports).
    
2. Melden Sie sich bei Office 365 mit den Anmeldeinformationen für ein Benutzerkonto in Ihrer Office 365-Organisation an.
    
Auf der Seite **Berichte anzeigen** können Sie die folgenden Arten von Berichten anzeigen: 
  
- [Überwachungsberichte](#auditing-reports)
- [Bericht über die aufsichtsüberprüfung](#supervisory-review-report)
- [Berichte zur Verhinderung von Datenverlust](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>Überwachungsberichte

In der folgenden Tabelle werden die Berichte im Abschnitt **Überwachung** auf der Seite **Berichte anzeigen** im Security & Compliance Center beschrieben. 
  
|**Bericht**|**Beschreibung**|
|:-----|:-----|
|**Office 365-Überwachungsprotokollbericht** <br/> |Sie können das Office 365-Überwachungsprotokoll nach Benutzer-und Administratoraktivitäten in Ihrer Office 365-Organisation durchsuchen. Der Bericht enthält Einträge Benutzer-und Administratoraktivitäten in Exchange Online, SharePoint Online, OneDrive for Business und Azure Active Directory, bei dem es sich um den Verzeichnisdienst für Office 365 handelt. Weitere Informationen finden Sie unter [Durchsuchen des Überwachungsprotokolls im Office 365](search-the-audit-log-in-security-and-compliance.md).  <br/> |
|**Azure AD-Berichte** <br/> |Um ungewöhnliche oder verdächtige Anmeldeaktivitäten in Ihrer Office 365-Organisation zu suchen, können Sie Anmelde-und Aktivitätsberichte in Microsoft Azure verwenden. Sie können auch Ereignisse im Azure AD-Überwachungsprotokoll anzeigen. Klicken Sie zum Anzeigen von Berichten in Azure einfach auf **Azure AD-Berichte anzeigen**. Weitere Informationen finden Sie unter: <br/><br/>[Verwenden Sie Ihr freies Azure Active Directory-Abonnement in Office 365](use-your-free-azure-ad-subscription-in-office-365.md). <br/> [Zeigen Sie Ihre Access-und Nutzungsberichte](http://go.microsoft.com/fwlink/p/?LinkId=506902)an.  <br/> |
|**Exchange-Überwachungsberichte** <br/> | Mithilfe der Überwachungsfunktionen in Office 365 können Sie Änderungen an Ihrer Exchange Online-Konfiguration nachverfolgen, die von den Administratoren Ihrer Organisation vorgenommen wurden. Änderungen, die von einem Microsoft-Datencenter Administrator oder einem Delegierten Administrator an Ihrer Exchange Online-Organisation vorgenommen wurden, werden ebenfalls protokolliert. Für Exchange Online ist die Administrator-Überwachungsprotokollierung standardmäßig aktiviert, sodass Sie nichts tun müssen, um Sie zu aktivieren. Exchange Online bietet außerdem die postfachüberwachungsprotokollierung, mit der Sie den Zugriff auf Postfächer von anderen Benutzern als dem Postfachbesitzer nachverfolgen können. Die Postfachüberwachungsprotokollierung muss für jedes Postfach aktiviert werden, für das Sie den Zugriff durch Nicht-Besitzer nachverfolgen möchten.  <br/>  Sowohl für die Administrator-als auch für die postfachüberwachungsprotokollierung können Sie Überwachungsberichte ausführen, um die Überwachungsprotokolleinträge anzuzeigen. Sie können auch Postfach-und Administratorüberwachungsprotokolle exportieren, die innerhalb von 24 Stunden in einer XML-Datei an Sie gesendet werden, die an eine e-Mail-Nachricht angefügt ist. <br/><br/>Weitere Informationen zum Exportieren von Überwachungsprotokollen finden Sie unter:  <br/><br/> [Exportieren von Postfachüberwachungsprotokollen](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [Anzeigen und Exportieren des Überwachungsprotokolls des Datencenter-Administrators](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [Durchsuchen der Rollengruppenänderungen oder Administratorüberwachungsprotokolle](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Exchange-Überwachungsberichte](http://go.microsoft.com/fwlink/p/?LinkID=395232).  <br/> |
   
## <a name="supervisory-review-report"></a>Bericht über die aufsichtsüberprüfung

Mit dem Bericht über die aufsichtsüberprüfung können Sie den Status aller Aufsichtsrichtlinien in Ihrer Organisation anzeigen. Weitere Informationen finden Sie unter [configure Supervisory Review Policies for your organization](configure-supervision-policies.md).
  
## <a name="data-loss-prevention-reports"></a>Berichte zur Verhinderung von Datenverlust

Data Loss Prevention (DLP)-Berichte enthalten Informationen zu den DLP-Richtlinien und-Regeln, die auf Inhalte mit vertraulichen Daten in Ihrer Office 365-Organisation angewendet wurden. Sie können diese Berichte auch so konfigurieren, dass sie Informationen über DLP-Aktionen anzeigen, die auf Ihren DLP-Richtlinien und -Regeln basieren. Weitere Informationen finden Sie unter [Anzeigen des Berichts zur Verhinderung von Datenverlust](view-the-dlp-reports.md).
