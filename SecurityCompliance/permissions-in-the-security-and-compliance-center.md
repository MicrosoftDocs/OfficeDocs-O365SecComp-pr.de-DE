---
title: Berechtigungen im Office 365 Security &amp; Compliance Center
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AdminRoleGroups
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d10608af-7934-490a-818e-e68f17d0e9c1
description: Die Office 365-Sicherheit &amp; Compliance Center können Sie Personen Berechtigungen erteilen, die Einhaltung von Bestimmungen wie Gerätemanagement, Verhinderung von Datenverlust, eDiscovery, Aufbewahrung und So weiter Aufgaben. Diese Personen können nur die Aufgaben ausführen, denen Sie explizit ihnen Zugriff zu gewähren. Greifen Sie auf die Sicherheit &amp; Compliance Center, Benutzer müssen ein globaler Office 365-Administrator oder ein Mitglied der Sicherheit für eine oder mehrere sein &amp; Rollengruppen Compliance Center.
ms.openlocfilehash: ef281ca7cda706ff78fbf1a5584674cdf41e9025
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741058"
---
# <a name="permissions-in-the-office-365-security-amp-compliance-center"></a>Berechtigungen im Office 365 Security &amp; Compliance Center

Die Office 365-Sicherheit &amp; Compliance Center können Sie Personen Berechtigungen erteilen, die Einhaltung von Bestimmungen wie Gerätemanagement, Verhinderung von Datenverlust, eDiscovery, Aufbewahrung und So weiter Aufgaben. Diese Personen können nur die Aufgaben ausführen, denen Sie explizit ihnen Zugriff zu gewähren. Greifen Sie auf die Sicherheit &amp; Compliance Center, Benutzer müssen ein globaler Office 365-Administrator oder ein Mitglied der Sicherheit für eine oder mehrere sein &amp; Rollengruppen Compliance Center.
  
Berechtigungen in das Wertpapier &amp; Compliance Center basieren auf das Berechtigungsmodell Rolle basierend Access Control (RBAC). Dies ist das Modell der gleichen Berechtigungen, die von Exchange verwendet wird also wenn Sie Exchange vertraut, Erteilen von Berechtigungen in das Wertpapier &amp; Compliance Center werden sehr ähnlich. Es ist wichtig, die Exchange-Serverrolle jedoch beachten Gruppen und-Sicherheit &amp; Compliance Center Rollengruppen nicht freigeben, Mitgliedschaft oder Berechtigungen. Zwar sowohl eine Rollengruppe "Organisationsverwaltung" haben, sind auch identisch. Der erteilten Berechtigungen und die Mitglieder der Rollengruppen, unterscheiden. Es wird eine Liste der Sicherheit &amp; Compliance Center Rollengruppen unten.
  
![Berechtigungen in der Office 365-Sicherheit Seite &amp; Compliance Center](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>Beziehung zwischen Mitgliedern, Rollen und Rollengruppen

Eine **Rolle** gewährt Berechtigungen zum Ausführen einer Reihe von Aufgaben. Beispielsweise berechtigt die Rolle "Fallmanagement" Personen zum Arbeiten mit eDiscovery-Fällen. 
  
Eine **Rollengruppe** ist ein Satz von Rollen, mit der Personen, die über die Sicherheit ihrer Tätigkeit ausführen &amp; Compliance Center; der Rolle Compliance-Administratorgruppe umfasst beispielsweise die Rollen für Fallmanagement, Inhaltssuche, und Organisationskonfiguration (sowie andere Personen), da einer Person, die ein Compliance-Admin ist die Berechtigungen für diese Vorgänge für ihre Arbeit benötigen. 
  
Die Sicherheit &amp; Compliance Center umfasst Rolle Standardgruppen für die häufigsten Aufgaben und Funktionen, die Sie benötigen, um Personen zuzuweisen. Es wird empfohlen, einfach Hinzufügen einzelner Benutzer als **Mitglieder** der Rolle Standardgruppen. 
  
![Diagramm mit dem Verhältnis von Rollengruppen zu Rollen und Elementen](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
Bearbeiten oder Löschen von vorhandenen Rollengruppen können, jedoch nicht empfohlen. Anstatt zur Bearbeitung einer Rollengruppe Standard, können Sie kopieren, ändern und dann mit einem anderen Namen speichern.
  
## <a name="permissions-needed-to-use-features-in-the-security-amp-compliance-center"></a>Verwenden von Features in das Wertpapier benötigten Berechtigungen &amp; Compliance Center

Die folgende Tabelle enthält die Rolle Standardgruppen, die in das Wertpapier verfügbar sind &amp; Compliance Center. Um einem Benutzer das Ausführen einer Aufgabe Compliance gewähren, diese hinzufügen die entsprechenden Sicherheitsfunktionen &amp; Compliance Center Rollengruppe.
  
Verwalten von Berechtigungen in das Wertpapier &amp; Compliance Center nur ermöglicht Benutzern den Zugriff auf die Compliance-Features, die innerhalb der Sicherheit verfügbar sind &amp; Compliance Center selbst. Wenn Sie möchten andere Kompatibilitätsfeatures Berechtigungen erteilen, die nicht in das Wertpapier sind &amp; Compliance Center, wie Exchange-Transportregeln, müssen Sie die Exchange-Verwaltungskonsole zu verwenden.
  
Zum Erteilen Zugriff für die Sicherheit finden Sie unter &amp; Compliance Center, Auschecken [gewähren Sie Benutzerzugriff auf Office 365 Compliance-Verwaltungskonsole](grant-access-to-the-security-and-compliance-center.md).
  
|**Rollengruppe**|**Beschreibung**|
|:-----|:-----|
|**Compliance-Administrator** <sup>1</sup> <br/> |Mitglieder können Einstellungen für die Verwaltung von Geräten, Verhinderung von Datenverlust, Berichte und permanentes verwalten.  <br/> |
|**eDiscovery-Manager** <br/> | Mitglieder können Suchvorgänge ausführen und Place-Haltebereiche auf Postfächer, SharePoint Online-Websites und OneDrive for Business-Speicherorte. Mitglieder können auch erstellen und Verwalten von eDiscovery-Fälle, hinzufügen und Entfernen von Mitgliedern zu einer Anfrage, erstellen und bearbeiten Content-Suche eine Groß-/Kleinschreibung und Groß-/Kleinschreibung Access-Daten in Office 365 erweiterte eDiscovery zugeordnet.<br/><br/>Eine eDiscovery Administrator ist Mitglied der Gruppe der eDiscovery-Manager-Rolle, die zusätzliche Berechtigungen zugewiesen wurden. Zusätzlich zu den Aufgaben, die eine eDiscovery-Manager ausführen können, können eine eDiscovery-Administrator:<br/><br/>  • Anzeigen aller eDiscovery-Fälle, in der Organisation.  <br/>  • Alle eDiscovery-Fall verwaltet werden, nachdem sie sich als Mitglied der Groß-/Kleinschreibung hinzufügen.  <br/><br/>Der Hauptunterschied zwischen einer eDiscovery-Manager und eine eDiscovery-Administrator ist eine eDiscovery-Administrator festgelegte allen Fällen zugreifen zu kann, die auf der Seite **eDiscovery-Fälle** , in das Wertpapier aufgelistet sind &amp; Compliance Center. Ein eDiscovery-Manager kann nur zugreifen, die Fall den von die Ihnen erstellten oder, denen sie Mitglied sind.  Weitere Informationen zum Aktivieren eines Benutzers einer eDiscovery-Administrator, finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).<br/>           |
|**Organisationsverwaltung** <sup>1</sup> <br/> |Mitglieder können Berechtigungen für den Zugriff auf Features in das Wertpapier steuern &amp; Compliance Center, und auch Verwalten von Einstellungen für die Verwaltung von Geräten, Verhinderung von Datenverlust, Berichte und permanentes.  <br/> Beachten Sie, dass in der Reihenfolge für einen Benutzer, der kein globaler Administrator angemeldet, finden in der Liste der Geräte, die von MDM für Office 365 verwaltet wird und Ausführen von Aktionen für diese Geräte, beispielsweise Abschließen eines Geräts von MDM für Office 365, muss der Benutzer ein Exchange-Administrator sein.  <br/> Office 365 globale Administratoren werden automatisch als Mitglieder dieser Rollengruppe hinzugefügt.           |
|**Datensatzverwaltung** <br/> |Mitglieder können verwalten und dispose Datensatz Inhalte.  <br/> |
|**Reviewer** <br/> |Mitglieder können nur anzeigen die Liste der Anfragen auf der Seite eDiscovery-Fälle, in das Wertpapier &amp; Compliance Center. Sie können nicht erstellen, öffnen oder einen eDiscovery-Fall verwalten. Der primäre Zweck der dieser Rollengruppe wird zum Anzeigen und Zugriff Mitglieder können Daten in erweiterten eDiscovery case.  <br/> Diese Rollengruppe verfügt über die restriktivsten Berechtigungen in Bezug auf eDiscovery.  <br/> |
|**Sicherheitsadministrator** <br/> |Mitglieder dieser Rollengruppe können Cross-Service-Administratoren als auch externe Partnergruppen und Microsoft Support enthalten. Standardmäßig kann dieser Gruppe keine Rollen zugewiesen werden. Allerdings werden werden ein Mitglied der Rolle Sicherheitsadministratoren in Azure Active Directory und die Funktionen dieser Rolle erbt. Zum zentral verwalten von Berechtigungen, vornehmen von Änderungen an dieser Rolle in der Verwaltungskonsole von Azure Active Directory - Weitere Informationen finden Sie unter [Rolle Administratorberechtigungen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Wenn Sie dieser Rollengruppe in der & Security Compliance Center bearbeiten, gelten diese Änderungen nur für die Sicherheit & Compliance Center und nicht in einer anderen Diensten, Änderungen in der Verwaltungskonsole von Azure Active Directory nicht alle Dienste beeinträchtigen.<br/> Alle nur-Lese-Berechtigungen der Sicherheitsrolle Reader sowie eine Anzahl von zusätzlichen administrativen Berechtigungen für dieselben Dienste: Azure Information Protection, Identity Protection Center, privilegierten Identity Management, Monitor Office 365-Dienst Integrität und Sicherheit in Office 365 &amp; Compliance Center.  <br/> |
|**Sicherheit-Reader** <br/> |Mitglieder haben schreibgeschützten Zugriff auf eine Anzahl von Sicherheitsfeatures von Identity Protection Center, privilegierten Identity Management, Monitor Office 365-Dienststatus und Sicherheit in Office 365 &amp; Compliance Center.  <br/> Die Mitgliedschaft in dieser Rollengruppe ist zwischen Diensten synchronisiert und zentral verwaltet. Mitglieder dieser Rollengruppe können Cross-Service-Administratoren als auch externe Partnergruppen und Microsoft Support enthalten. Standardmäßig kann dieser Gruppe keine Rollen zugewiesen werden. Allerdings werden werden ein Mitglied der Rolle Sicherheitsadministratoren in Azure Active Directory und die Funktionen dieser Rolle erbt. Zum zentral verwalten von Berechtigungen, vornehmen von Änderungen an dieser Rolle in der Verwaltungskonsole von Azure Active Directory - Weitere Informationen finden Sie unter [Rolle Administratorberechtigungen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Wenn Sie dieser Rollengruppe in der & Security Compliance Center bearbeiten, gelten diese Änderungen nur für die Sicherheit & Compliance Center und nicht in einer anderen Diensten, Änderungen in der Verwaltungskonsole von Azure Active Directory nicht alle Dienste beeinträchtigen.<br/> |
|**Dienstüberprüfungsbenutzer** <br/> |Mitglieder können den Service Assurance Abschnitt in der Office 365-Sicherheit zugreifen &amp; Compliance Center. Service Assurance bietet Berichte und Dokumente, die Microsoft Sicherheitsmaßnahmen für Kundendaten beschreiben, die in Office 365 gespeichert ist. Es bietet auch, dass unabhängigen Drittanbieter-Prüfung auf Office 365-Berichte. Weitere Informationen finden Sie unter [Service Assurance in die Office 365-Sicherheit &amp; Compliance Center](http://go.microsoft.com/fwlink/p/?LinkID=717765).<br/> |
|**Generelle überprüfen** <br/> |Mitglieder können erstellen und verwalten Sie die Richtlinien, die dem definieren Communications unterliegen Überprüfung in einer Organisation. Weitere Informationen finden Sie unter [Configure generelle Richtlinien für Ihre Organisation überprüfen](configure-supervision-policies.md).<br/> |
   
> [!NOTE]
> <sup>1</sup> dieser Rollengruppe nicht Mitglieder weisen Sie die Berechtigungen erforderlich, um das Office 365-Überwachungsprotokoll zu suchen oder Berichte, die Sie verwenden, die Exchange-Daten, wie die DLP oder ATP Berichte enthalten kann. Um das Überwachungsprotokoll durchsuchen oder alle Berichte anzeigen möchten, muss ein Benutzer in Exchange Online Berechtigungen zugewiesen werden. Dies ist, da das zugrunde liegende-Cmdlet verwendet, um das Überwachungsprotokoll durchsuchen Exchange Online-Cmdlet ist. Office 365 globale Administratoren können das Überwachungsprotokoll zu suchen und alle Berichte anzeigen, da sie automatisch als Mitglieder der Rollengruppe Organisationsverwaltung in Exchange Online hinzugefügt haben. Weitere Informationen finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](https://go.microsoft.com/fwlink/p/?LinkID=708432). 
  

