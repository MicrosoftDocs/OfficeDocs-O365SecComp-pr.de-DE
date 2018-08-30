---
title: Berichte in Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/1/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: 'Verwenden Sie die Office 365-Sicherheit &amp; Compliance Center verschiedene Berichte für Ihre Exchange Online und SharePoint Online-Organisation abgerufen, plus Azure Active Directory-Berichte.  '
ms.openlocfilehash: 0b633583e14a18c7cf579d10462cf41714397812
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528931"
---
# <a name="reports-in-the-office-365-security-amp-compliance-center"></a>Berichte in Office 365-Sicherheit &amp; Compliance Center

Sie können die Seite **Berichte anzeigen** in der Office 365-Sicherheit &amp; Compliance Center schnellen Zugriff auf Überwachungsberichte für Ihre Exchange Online und SharePoint Online-Organisationen. Sie können auch auf Azure Active Directory (AD)-Anmeldung Benutzerberichte, Benutzeraktivität meldet, und der Azure AD-Überwachungsprotokolle melden Sie sich von der Seite **Berichte anzeigen** . Dies ist, da Ihres kostenpflichtigen Office 365-Abonnements in Microsoft Azure ein kostenloses Abonnement enthält. Beim ersten, die Sie versuchen, diese Azure Berichte, zugreifen müssen Sie eine einmalige Registrierungsvorgangs. 
  
> [!TIP]
> Weitere Berichte über die Aktivität in Office 365-Organisation finden Sie unter [Berichte im Office 365 Administrationscenter](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263). 
  
 **Bevor Sie beginnen**
  
Sie benötigen die folgenden Berechtigungen zum Anzeigen von Berichten in das Wertpapier &amp; Compliance Center.
  
- Sie müssen die Sicherheit Reader-Rolle in der Exchange-Verwaltungskonsole (EAC) anzeigen von Berichten in das Wertpapier zugewiesen werden &amp; Compliance Center. Standardmäßig wird diese Rolle Rollengruppen Organization Management und Sicherheit Reader in der Exchange-Verwaltungskonsole zugewiesen.
    
- Sie müssen die Rolle des DLP Compliance Management in das Wertpapier zugewiesen werden &amp; Compliance Center zum Anzeigen von DLP-Berichte (und DLP-Richtlinien) in die Sicherheit &amp; Compliance Center. Standardmäßig ist dieser Rolle zugewiesen, die Compliance-Administrator, Organization Management und Sicherheitsadministrator Rollengruppen in das Wertpapier &amp; Compliance Center.
    
Darüber hinaus müssen Sie die Verhinderung von Datenverlust Rolle in der Exchange-Verwaltungskonsole zum Anzeigen von DLP-Berichte (und DLP-Richtlinien) zugewiesen werden in der Exchange-Verwaltungskonsole. Standardmäßig wird diese Rolle Rollengruppen Compliance Management und Organization Management in der Exchange-Verwaltungskonsole zugewiesen.
  
 **So öffnen Sie die Seite "Berichte anzeigen" in die Sicherheit &amp; Compliance Center:**
  
1. Wechseln Sie zu [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports).
    
2. Melden Sie sich bei Office 365 mit den Anmeldeinformationen für ein Benutzerkonto in Office 365-Organisation.
    
Klicken Sie auf der Seite **Berichte anzeigen** können Sie die folgenden Berichtstypen anzeigen: 
  
- [Überwachungsberichte in EOP](#auditing-reports)
- [Überprüfungsbericht generelle](#supervisory-review-report)
- [Berichte zur Verhinderung von Datenverlust](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>Überwachungsberichte

Die folgende Tabelle beschreibt die Berichte im Abschnitt **Überwachung** auf der Seite " **Berichte anzeigen** " in das Wertpapier &amp; Compliance Center. 
  
|**Bericht**|**Beschreibung**|
|:-----|:-----|
|**Die Überwachungsprotokollbericht Office 365** <br/> |Sie können das Office 365-Überwachungsprotokoll für Benutzer- und Admin-Aktivität in Office 365-Organisation suchen. Der Bericht enthält Einträge Benutzer- und Admin-Aktivität in Exchange Online, SharePoint Online, OneDrive für Unternehmen und Azure Active Directory, der den Verzeichnisdienst für Office 365 ist. Weitere Informationen finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).<br/> |
|**Azure AD-Berichte** <br/> |Um für ungewöhnliche oder verdächtigen-Anmeldung Aktivität in Office 365-Organisation zu suchen, können-Anmeldung und die Aktivitäten Berichte in Microsoft Azure. Sie können auch Ereignisse im Überwachungsprotokoll Azure AD anzeigen. Klicken Sie zum Anzeigen von Berichten in Azure einfach auf **Berichte anzeigen Azure AD**. Weitere Informationen finden Sie unter:<br/><br/>[Verwenden Sie Ihr kostenloses Azure Active Directory-Abonnement in Office 365](use-your-free-azure-ad-subscription-in-office-365.md). <br/> [Ihre Verwendung Berichte anzeigen](http://go.microsoft.com/fwlink/p/?LinkId=506902).  <br/> |
|**Exchange-Überwachungsberichte** <br/> | Die Überprüfungsfunktionen können in Office 365 zum Nachverfolgen von Änderungen an der Exchange Online-Konfiguration von den Administratoren Ihrer Organisation. Änderungen an Ihrer Exchange Online-Organisation von einem Administrator der Microsoft Data Center oder von einem delegierten Administrator werden ebenfalls protokolliert. Für Exchange Online, Administrator-Überwachungsprotokolleinträge-Protokollierung ist standardmäßig aktiviert, so Sie nichts Unternehmen, um es zu aktivieren müssen. Exchange Online bietet auch postfachüberwachungsprotokollierung Sie den Zugriff auf Postfächer durch eine andere Person als der Postfachbesitzer verfolgen können. Sie müssen Aktivieren der postfachüberwachungsprotokollierung für jedes Postfach, die nicht-Besitzer Access nachverfolgen möchten.<br/>  Postfachüberwachungsprotokollierung für Admin und Postfach, können Sie Überwachungsberichte zum Anzeigen der Überwachungsprotokolleinträgen ausgeführt werden. Sie können auch Postfach- und Admin Überwachungsprotokolle exportieren, die an Sie innerhalb von 24 Stunden in einer XML-Datei gesendet werden, die e-Mail-Nachricht angefügt ist.<br/><br/>Weitere Informationen zum Exportieren von Überwachungsprotokollen finden Sie unter:  <br/><br/> [Exportieren von Postfachüberwachungsprotokollen](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [Zeigen Sie an und exportieren Sie des Datencenter-administratorüberwachungsprotokolls](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [Durchsuchen der rollengruppenänderungen oder Administrator Überwachungsprotokolle](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Exchange-Überwachungsberichte](http://go.microsoft.com/fwlink/p/?LinkID=395232).  <br/> |
   
## <a name="supervisory-review-report"></a>Überprüfungsbericht generelle

Mit dem Überprüfungsbericht generelle sehen Sie den Status aller generelle Überprüfung Richtlinien in Ihrer Organisation. Weitere Informationen finden Sie unter [Configure generelle Richtlinien für Ihre Organisation überprüfen](configure-supervision-policies.md).
  
## <a name="data-loss-prevention-reports"></a>Berichte zur Verhinderung von Datenverlust

Verhinderung von Datenverlust (DLP)-Berichte enthalten Informationen zu DLP-Richtlinien und Regeln, die auf Inhalte angewendet wurden vertrauliche Daten in Office 365-Organisation enthalten. Sie können auch den Bericht zum Anzeigen von Informationen zu DLP-Aktionen, die auf Ihrer DLP-Richtlinien und Regeln basierten konfigurieren. Weitere Informationen finden Sie unter [Anzeigen des Berichts für die Verhinderung von Datenverlust](view-the-dlp-reports.md).
