---
title: Berechtigungen im Office 365 Security &amp; Compliance Center
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.AdminRoleGroups
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
description: Mit dem Office 365 &amp; Security Compliance Center können Sie Personen, die Compliance-Aufgaben wie Geräteverwaltung, Verhinderung von Datenverlust, eDiscovery, Aufbewahrung usw. ausführen, Berechtigungen erteilen. Diese Personen können nur die Aufgaben ausführen, denen Sie explizit Zugriff gewähren. Für den Zugriff auf &amp; das Security Compliance Center müssen Benutzer ein globaler Office 365-Administrator oder ein Mitglied einer oder mehrerer Rollengruppen &amp; des Security Compliance Centers sein.
ms.openlocfilehash: eba77fd6edcf41bac5eeebae3637707c2c5a7246
ms.sourcegitcommit: 799a958fcac643f62dfac6fa04020f2f4758635c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30997081"
---
# <a name="permissions-in-the-office-365-security-amp-compliance-center"></a>Berechtigungen im Office 365 Security &amp; Compliance Center

Mit dem Office 365 &amp; Security Compliance Center können Sie Personen, die Compliance-Aufgaben wie Geräteverwaltung, Verhinderung von Datenverlust, eDiscovery, Aufbewahrung usw. ausführen, Berechtigungen erteilen. Diese Personen können nur die Aufgaben ausführen, denen Sie explizit Zugriff gewähren. Für den Zugriff auf &amp; das Security Compliance Center müssen Benutzer ein globaler Office 365-Administrator oder ein Mitglied einer oder mehrerer Rollengruppen &amp; des Security Compliance Centers sein.
  
Berechtigungen im Security &amp; Compliance Center basieren auf dem Berechtigungsmodell für die rollenbasierte Zugriffssteuerung. Dies ist das gleiche Berechtigungsmodell, das von Exchange verwendet wird, wenn Sie also mit Exchange vertraut sind, ist das Gewähren von &amp; Berechtigungen im Security Compliance Center sehr ähnlich. Beachten Sie jedoch, dass Exchange-Rollengruppen und Sicherheits &amp; Kompatibilitäts Center-Rollengruppen keine Mitgliedschaft oder Berechtigungen gemeinsam nutzen. Zwar verfügen beide über eine Rollengruppe "Organisationsverwaltung", sie sind jedoch nicht identisch. Die erteilten Berechtigungen und die Mitglieder der Rollengruppen sind verschieden. Nachfolgend finden Sie eine Liste &amp; der Rollengruppen Security Compliance Center.
  
![Seite "Berechtigungen" im Office 365 &amp; Security Compliance Center](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>Beziehung zwischen Mitgliedern, Rollen und Rollengruppen

Eine **Rolle** gewährt Berechtigungen zum Ausführen einer Reihe von Aufgaben. Beispielsweise berechtigt die Rolle "Fallmanagement" Personen zum Arbeiten mit eDiscovery-Fällen. 
  
Eine **Rollengruppe** ist eine Gruppe von Rollen, mit deren Hilfe Personen Ihre Aufgaben im Security &amp; Compliance Center ausführen können. die Rollengruppe "Compliance-Administrator" enthält beispielsweise die Rollen für die Fallverwaltung, die Inhaltssuche und die Organisationskonfiguration (plus andere), da jemand, der ein Kompatibilitäts-admin ist, die Berechtigungen für diese Aufgaben benötigt, um seine Aufgabe auszuführen. 
  
Das Security &amp; Compliance Center enthält Standardrollengruppen für die am häufigsten verwendeten Aufgaben und Funktionen, denen Sie Personen zuweisen müssen. Es wird empfohlen, den Standardrollengruppen einfach einzelne Benutzer als **Mitglieder** hinzuzufügen. 
  
![Diagramm mit der Beziehung von Rollengruppen zu Rollen und Elementen](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
Sie können die vorhandenen Rollengruppen bearbeiten oder löschen, aber dies wird nicht empfohlen. Anstatt eine standardmäßige Rollengruppe zu bearbeiten, können Sie sie kopieren, ändern und dann unter einem anderen Namen speichern.
  
## <a name="permissions-needed-to-use-features-in-the-security-amp-compliance-center"></a>Erforderliche Berechtigungen für die Verwendung von Features im &amp; Security Compliance Center

In der folgenden Tabelle sind die Standardrollengruppen aufgeführt, die im Security &amp; Compliance Center verfügbar sind. Wenn Sie einem Benutzerberechtigungen zum Ausführen einer Konformitäts Aufgabe erteilen möchten, fügen Sie diese der &amp; entsprechenden Sicherheits Kompatibilitäts Center-Rollengruppe hinzu.
  
Durch das Verwalten von Berechtigungen &amp; im Security Compliance Center erhalten Benutzer nur Zugriff auf die Compliance-Funktionen, die im &amp; Security Compliance Center selbst zur Verfügung stehen. Wenn Sie anderen Kompatibilitätsfeatures, die sich nicht im Security &amp; Compliance Center befinden, wie Exchange-Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet), Berechtigungen erteilen möchten, müssen Sie die Exchange-Verwaltungskonsole verwenden.
  
Informationen zum Gewähren des Zugriffs auf das Security &amp; Compliance Center finden Sie unter [Benutzern zugriff auf Office 365 Compliance Admin Center](grant-access-to-the-security-and-compliance-center.md)erteilen.
  
|**Rollengruppe**|**Beschreibung**|
|:-----|:-----|
|**Compliance-Administrator** <sup>1</sup> <br/> |Mitglieder können Einstellungen für Geräteverwaltung, Verhinderung von Datenverlust, Berichte und Archivierung verwalten.  <br/> |
|**Compliance-Daten Administrator** <br/> |Mitglieder können Einstellungen für Geräteverwaltung, Datenschutz, Verhinderung von Datenverlust, Berichte und Archivierung verwalten.  <br/> |
|**eDiscovery-Manager** <br/> | Mitglieder können Suchvorgänge durchführen und Postfächer, SharePoint Online-Websites und OneDrive for Business-Orte im In-Situ-Speicher platzieren. Mitglieder können auch eDiscovery-Fälle erstellen und verwalten, einem Fall Mitglieder hinzufügen und daraus entfernen, mit einem Fall verknüpfte Inhalts suchVorgänge erstellen und bearbeiten sowie Falldaten in Office 365 Advanced eDiscovery abrufen. <br/><br/>Ein eDiscovery-Administrator ist Mitglied der Rollengruppe "eDiscovery-Manager", der zusätzliche Berechtigungen zugewiesen wurden. Zusätzlich zu den Aufgaben, die ein eDiscovery-Manager ausführen kann, kann ein eDiscovery-Administrator Folgendes tun:  <br/><br/>  • Anzeigen aller eDiscovery-Fälle in der Organisation.  <br/>  • Verwalten Sie alle eDiscovery-Fälle, nachdem Sie sich selbst als Mitglied der Anfrage hinzugefügt haben.  <br/><br/>Der Hauptunterschied zwischen einem eDiscovery-Manager und einem eDiscovery-Administrator besteht darin, dass ein eDiscovery-Admininstrator auf alle Fälle zugreifen kann, die auf der Seite &amp; eDiscovery- **Fälle** im Security Compliance Center aufgeführt sind. Ein eDiscovery-Manager kann nur auf die von ihm erstellten Fälle oder Fälle zugreifen, in denen er Mitglied ist.  Weitere Informationen zum Erstellen eines eDiscovery-Administrators für einen Benutzer finden Sie unter [assign eDiscovery Permissions in &amp; the Office 365 Security Compliance Center](assign-ediscovery-permissions.md). <br/> |
|**MailFlow-Administrator** <br/> |Mitglieder können Nachrichtenfluss-Einblicke und Berichte im Security & Compliance Center überwachen und anzeigen. Globale Administratoren können dieser Gruppe normale Benutzer hinzufügen, aber wenn der Benutzer kein Mitglied der Exchange-Verwaltungsgruppe ist, hat der Benutzer keinen Zugriff auf Aufgaben im Zusammenhang mit Exchange-Verwaltung.  <br/> |
|**Organisationsverwaltung** <sup>1</sup> <br/> |Mitglieder können Berechtigungen für den Zugriff auf Features im Security &amp; Compliance Center Steuern und auch Einstellungen für die Geräteverwaltung, die Verhinderung von Datenverlust, Berichte und die Aufbewahrung verwalten.  <br/> Beachten Sie, dass der Benutzer ein Exchange-Administrator sein muss, damit ein Benutzer, der kein globaler Administrator ist, die Liste der von MDM für Office 365 verwalteten Geräte anzeigen und Aktionen auf diesen Geräten ausführen kann, beispielsweise das Zurückziehen eines Geräts von MDM für Office 365.  <br/> Office 365 globale Administratoren werden automatisch als Mitglieder dieser Rollengruppe hinzugefügt.           |
|**Datensatzverwaltung** <br/> |Mitglieder können Datensatzinhalte verwalten und freigeben.  <br/> |
|**Reviewer** <br/> |Mitglieder können nur die Liste der Fälle auf der Seite eDiscovery-Fälle im Security &amp; Compliance Center anzeigen. Sie können keine eDiscovery-Fälle erstellen, öffnen oder verwalten. Der primäre Zweck dieser Rollengruppe besteht darin, Mitgliedern das Anzeigen und Zugreifen auf Falldaten in Advanced eDiscovery zu ermöglichen.  <br/> Diese Rollengruppe verfügt über die restriktivsten Berechtigungen in Bezug auf eDiscovery.  <br/> |
|**Sicherheitsadministrator** <br/> |Mitglieder dieser Rollengruppe können dienstübergreifende Administratoren sowie externe Partnergruppen und Microsoft-Support sein. Dieser Gruppe werden standardmäßig keine Rollen zugewiesen. Sie ist jedoch Mitglied der Rolle "Sicherheitsadministratoren" in Azure Active Directory und erbt die Funktionen dieser Rolle. Um Berechtigungen zentral zu verwalten, nehmen Sie Änderungen an dieser Rolle im Azure Active Directory Admin Center vor – Weitere Informationen finden Sie unter [Administrator Rollen Berechtigungen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Wenn Sie diese Rollengruppe im Security & Compliance Center bearbeiten, gelten diese Änderungen nur für das Security & Compliance Center und keine anderen Dienste, während Änderungen im Azure Active Directory Admin Center alle Dienste betreffen.<br/> Alle schreibgeschützten Berechtigungen der Rolle "Sicherheits Leser" sowie eine Reihe zusätzlicher administrativer Berechtigungen für dieselben Dienste: Azure Information Protection, Identity Protection Center, privilegierte Identitätsverwaltung, Überwachen des Office 365-Diensts Integrität und Office 365 Security &amp; Compliance Center.  <br/> |
|**Sicherheits Operator** <br/> |Mitglieder können Sicherheitswarnungen verwalten und auch Berichte und Einstellungen von Sicherheitsfunktionen anzeigen. <br/> |
|**Sicherheits Leser** <br/> |Mitglieder verfügen über Lesezugriff auf eine Reihe von Sicherheitsfunktionen von Identity Protection Center, privilegierte Identitätsverwaltung, Überwachung der Office 365-Dienst Integrität und Office 365 Security &amp; Compliance Center.  <br/> Die Mitgliedschaft in dieser Rollengruppe wird über die Dienste hinweg synchronisiert und zentral verwaltet. Mitglieder dieser Rollengruppe können dienstübergreifende Administratoren sowie externe Partnergruppen und Microsoft-Support sein. Dieser Gruppe werden standardmäßig keine Rollen zugewiesen. Sie ist jedoch Mitglied der Rolle "Sicherheits Leser" in Azure Active Directory und erbt die Funktionen dieser Rolle. Um Berechtigungen zentral zu verwalten, nehmen Sie Änderungen an dieser Rolle im Azure Active Directory Admin Center vor – Weitere Informationen finden Sie unter [Administrator Rollen Berechtigungen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Wenn Sie diese Rollengruppe im Security & Compliance Center bearbeiten, gelten diese Änderungen nur für das Security & Compliance Center und keine anderen Dienste, während Änderungen im Azure Active Directory Admin Center alle Dienste betreffen.<br/> |
|**Dienstüberprüfungsbenutzer** <br/> |Mitglieder können im Office 365 Security &amp; Compliance Center auf den Abschnitt "Dienst Assurance" zugreifen. Service Assurance stellt Berichte und Dokumente bereit, in denen die Sicherheitsmethoden von Microsoft für Kundendaten beschrieben werden, die in Office 365 gespeichert sind. Darüber hinaus werden unabhängige Drittanbieter-Überwachungsberichte in Office 365 bereitgestellt. Weitere Informationen finden Sie unter [Service Assurance im Office 365 Security &amp; Compliance Center](http://go.microsoft.com/fwlink/p/?LinkID=717765).  <br/> |
|**Aufsichtsüberprüfung** <br/> |Mitglieder können die Richtlinien erstellen und verwalten, die definieren, welche Kommunikation in einer Organisation einer Überprüfung unterliegt. Weitere Informationen finden Sie unter [configure Supervisory Review Policies for your organization](configure-supervision-policies.md).  <br/> |
   
> [!NOTE]
> <sup>1</sup> diese Rollengruppe weist Mitgliedern nicht die Berechtigungen zu, die zum Durchsuchen des Office 365-Überwachungsprotokolls erforderlich sind, oder zum Verwenden von Berichten, die Exchange-Daten wie die DLP-oder ATP-Berichte beinhaltet. Zum Durchsuchen des Überwachungsprotokolls oder zum Anzeigen aller Berichte muss einem Benutzer in Exchange Online Berechtigungen zugewiesen werden. Dies liegt daran, dass das zugrunde liegende Cmdlet zum Durchsuchen des Überwachungsprotokolls ein Exchange Online-Cmdlet ist. Office 365 globale Administratoren können das Überwachungsprotokoll durchsuchen und alle Berichte anzeigen, da diese automatisch als Mitglieder der Rollengruppe "Organisationsverwaltung" in Exchange Online hinzugefügt werden. Weitere Informationen finden Sie unter [Durchsuchen des Überwachungsprotokolls im Office 365 Security &amp; Compliance Center](https://go.microsoft.com/fwlink/p/?LinkID=708432). 
  
## <a name="mapping-of-role-groups-to-assigned-roles"></a>Zuordnen von Rollengruppen zu zugewiesenen Rollen

Standardmäßig sind Rollengruppen eine Reihe von Rollen zugewiesen. In dieser Tabelle werden die Rollen angezeigt, die jeder Rollengruppe zugewiesen sind.

|**Rollengruppe**|**Zugewiesene Rollen**|
|:-----|:-----|
|**Complianceadministrator** <br/> |AufbewahrungsVerwaltung (nur anzeigen) <br/>
            Benachrichtigungen verwalten <br/>Benachrichtigungen verwalten <br/>Nur-anzeigen-Geräteverwaltung <br/>Organisationskonfiguration <br/>DLP-Compliance-Verwaltung <br/>View-Only IB Compliance Management <br/>Disposition-Verwaltung <br/>Management der DLP-KonformitätsVerwaltung <br/>RecordManagement <br/>IB-Compliance-Management <br/>Überwachungsprotokolle für die Anzeige <br/>Complianceadministrator <br/>Geräteverwaltung <br/>Compliance-Suche <br/>Fallverwaltung <br/>AufbewahrungsVerwaltung <br/>Datensatzverwaltung mit Schreibschutz <br/>Schreibgeschützte Empfänger <br/>Situ <br/> |
|**Compliance-Daten Administrator** <br/> |AufbewahrungsVerwaltung (nur anzeigen) <br/>
            Benachrichtigungen verwalten <br/>Vertraulichkeits Bezeichnung-Administrator <br/>Benachrichtigungen verwalten <br/>Nur-anzeigen-Geräteverwaltung <br/>Organisationskonfiguration <br/>DLP-Compliance-Verwaltung <br/>View-Only IB Compliance Management <br/>Disposition-Verwaltung <br/>Management der DLP-KonformitätsVerwaltung <br/>RecordManagement <br/>IB-Compliance-Management <br/>Überwachungsprotokolle für die Anzeige <br/>Complianceadministrator <br/>Geräteverwaltung <br/>Compliance-Suche <br/>AufbewahrungsVerwaltung <br/>Datensatzverwaltung mit Schreibschutz <br/>Schreibgeschützte Empfänger<br/> |
|**eDiscovery-Manager** <br/> |Exportieren <br/>RMS-entSchlüsselung <br/>Custodian <br/>Kommunikation <br/>Überprüfung <br/>Vorschau <br/>Compliance-Suche <br/>Fallverwaltung <br/>Situ <br/> |
|**MailFlow-Administrator** <br/> |Schreibgeschützte Empfänger <br/>  |
|**Organisationsverwaltung** <br/> |AufbewahrungsVerwaltung (nur anzeigen) <br/>
            Benachrichtigungen verwalten <br/>Rollenverwaltung <br/>Vertraulichkeits Bezeichnung-Administrator <br/>Benachrichtigungen verwalten <br/>Nur-anzeigen-Geräteverwaltung <br/>Organisationskonfiguration <br/>DLP-Compliance-Verwaltung <br/>View-Only IB Compliance Management <br/>Disposition-Verwaltung <br/>Management der DLP-KonformitätsVerwaltung <br/>RecordManagement <br/>Überwachungsprotokolle <br/>IB-Compliance-Management <br/>Sicherheits Leser <br/>Sicherheitsadministrator <br/>Ansicht "Dienstsicherheit" <br/>Suchen und löschen <br/>Überwachungsprotokolle für die Anzeige <br/>Complianceadministrator <br/>Geräteverwaltung <br/>Compliance-Suche <br/>Fallverwaltung <br/>AufbewahrungsVerwaltung <br/>Datensatzverwaltung mit Schreibschutz <br/>Schreibgeschützte Empfänger <br/>Situ <br/> |
|**Datensatzverwaltung** <br/> |RecordManagement <br/>Überwachungsprotokolle <br/>AufbewahrungsVerwaltung <br/> |
|**Reviewer** <br/> |Überprüfung <br/> |
|**Sicherheitsadministrator** <br/> |
            Benachrichtigungen verwalten <br/>Vertraulichkeits Bezeichnung-Administrator <br/>Benachrichtigungen verwalten <br/>Nur-anzeigen-Geräteverwaltung <br/>DLP-Compliance-Verwaltung <br/>View-Only IB Compliance Management <br/>Management der DLP-KonformitätsVerwaltung <br/>Überwachungsprotokolle <br/>IB-Compliance-Management <br/>Sicherheitsadministrator <br/>Überwachungsprotokolle für die Anzeige <br/>Geräteverwaltung <br/> |
|**Sicherheits Operator** <br/> |
            Benachrichtigungen verwalten <br/>Benachrichtigungen verwalten <br/>Nur-anzeigen-Geräteverwaltung <br/>View-Only IB Compliance Management <br/>Management der DLP-KonformitätsVerwaltung <br/>Sicherheits Leser <br/>Überwachungsprotokolle für die Anzeige <br/>Compliance-Suche <br/> |
|**Sicherheits Leser** <br/> |Benachrichtigungen verwalten <br/>Nur-anzeigen-Geräteverwaltung <br/>View-Only IB Compliance Management <br/>Management der DLP-KonformitätsVerwaltung <br/>Sicherheits Leser <br/> |
|**Dienstüberprüfungsbenutzer** <br/> |Ansicht "Dienstsicherheit" <br/> |
|**Aufsichtsüberprüfung** <br/> |Supervisory Review-Administrator <br/> |
