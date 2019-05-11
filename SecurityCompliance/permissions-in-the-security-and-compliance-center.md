---
title: Berechtigungen im Office 365 Security & Compliance Center
ms.author: chrisda
author: chrisda
manager: chrisda
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
description: Administratoren können sich über die im Office 365 Security & Compliance Center verfügbaren Berechtigungen informieren.
ms.openlocfilehash: 81b9020260f11700038f7cc266179355dd1a7896
ms.sourcegitcommit: 09fd88272187f82b6e635af83edabea08c2cc49c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2019
ms.locfileid: "33884773"
---
# <a name="permissions-in-the-office-365-security--compliance-center"></a>Berechtigungen im Office 365 Security & Compliance Center

Mit dem Office 365 Security & Compliance Center können Sie Personen, die Compliance-Aufgaben wie Geräteverwaltung, Verhinderung von Datenverlust, eDiscovery, Aufbewahrung usw. ausführen, Berechtigungen erteilen. Diese Personen können nur die Aufgaben ausführen, denen Sie explizit Zugriff gewähren. Für den Zugriff auf das Security & Compliance Center müssen Benutzer ein globaler Office 365-Administrator oder ein Mitglied einer oder mehrerer Sicherheits-& Compliance Center-Rollengruppen sein.
  
Berechtigungen im Security & Compliance Center basieren auf dem Berechtigungsmodell für die rollenbasierte Zugriffssteuerung. Dies ist das gleiche Berechtigungsmodell, das von Exchange verwendet wird, wenn Sie also mit Exchange vertraut sind, wird die Gewährung von Berechtigungen im Security & Compliance Center sehr ähnlich sein. Beachten Sie jedoch, dass die Rollengruppen "Exchange-Rollengruppen" und "Security & Compliance Center" keine Mitgliedschaft oder Berechtigungen freigeben. Zwar verfügen beide über eine Rollengruppe "Organisationsverwaltung", sie sind jedoch nicht identisch. Die erteilten Berechtigungen und die Mitglieder der Rollengruppen sind verschieden. Nachfolgend finden Sie eine Liste der Sicherheits & Compliance Center-Rollengruppen.
  
![Berechtigungsseite im Office 365 Security & Compliance Center](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>Beziehung zwischen Mitgliedern, Rollen und Rollengruppen

Eine **Rolle** gewährt Berechtigungen zum Ausführen einer Reihe von Aufgaben. Beispielsweise berechtigt die Rolle "Fallmanagement" Personen zum Arbeiten mit eDiscovery-Fällen.
  
Eine **Rollengruppe** ist eine Gruppe von Rollen, mit deren Hilfe Personen Ihre Aufgaben im Security & Compliance Center erledigen können. die Rollengruppe "Compliance-Administrator" enthält beispielsweise die Rollen für die Fallverwaltung, die Inhaltssuche und die Organisationskonfiguration (plus andere), da jemand, der ein Kompatibilitäts-admin ist, die Berechtigungen für diese Aufgaben benötigt, um seine Aufgabe auszuführen.
  
Das Security & Compliance Center enthält Standardrollengruppen für die am häufigsten verwendeten Aufgaben und Funktionen, denen Sie Personen zuweisen müssen. Es wird empfohlen, den Standardrollengruppen einfach einzelne Benutzer als **Mitglieder** hinzuzufügen.
  
![Diagramm mit der Beziehung von Rollengruppen zu Rollen und Elementen](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
Sie können die vorhandenen Rollengruppen bearbeiten oder löschen, aber dies wird nicht empfohlen. Anstatt eine standardmäßige Rollengruppe zu bearbeiten, können Sie sie kopieren, ändern und dann unter einem anderen Namen speichern.
  
## <a name="permissions-needed-to-use-features-in-the-security--compliance-center"></a>Erforderliche Berechtigungen für die Verwendung von Features im Security & Compliance Center

In der folgenden Tabelle sind die Standardrollengruppen aufgeführt, die im Security & Compliance Center verfügbar sind, und die Rollen, die den Rollengruppen standardmäßig zugewiesen sind. Wenn Sie einem Benutzerberechtigungen zum Ausführen einer Konformitäts Aufgabe erteilen möchten, fügen Sie diese der entsprechenden Sicherheits-&-Compliance Center-Rollengruppe hinzu.
  
Durch das Verwalten von Berechtigungen im Security & Compliance Center erhalten Benutzer nur Zugriff auf die Compliance-Funktionen, die im Security & Compliance Center selbst zur Verfügung stehen. Wenn Sie anderen Compliance-Funktionen, die nicht im Security & Compliance Center, wie Exchange-Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet), Berechtigungen erteilen möchten, müssen Sie die Exchange-Verwaltungskonsole verwenden.
  
Informationen zum Gewähren des Zugriffs auf das Security & Compliance Center finden Sie unter Erteilen des [Benutzerzugriffs auf das Office 365 Compliance Admin Center](grant-access-to-the-security-and-compliance-center.md).
  
|**Rollengruppe**|**Beschreibung**|**Zugewiesene Standardrollen**|
|:-----|:-----|:-----|
|**Compliance-Administrator** <sup>1</sup>|Mitglieder können Einstellungen für Geräteverwaltung, Verhinderung von Datenverlust, Berichte und Archivierung verwalten.|Fallverwaltung <br/><br/> Complianceadministrator <br/><br/> Compliance-Suche <br/><br/> DLP-Compliance-Verwaltung <br/><br/> Geräteverwaltung <br/><br/> Disposition-Verwaltung <br/><br/> Situ <br/><br/> IB-Compliance-Management <br/><br/> 
            Benachrichtigungen verwalten <br/><br/> Organisationskonfiguration <br/><br/> RecordManagement <br/><br/> Aufbewahrungsverwaltung <br/><br/> Überwachungsprotokolle für die Anzeige <br/><br/> Aufbewahrungsverwaltung (nur anzeigen) <br/><br/> Management der DLP-Konformitätsverwaltung <br/><br/> Nur-anzeigen-Geräteverwaltung <br/><br/> View-Only IB Compliance Management <br/><br/> Benachrichtigungen verwalten <br/><br/> Schreibgeschützte Empfänger <br/><br/> Datensatzverwaltung mit Schreibschutz|
|**Compliance-Daten Administrator**|Mitglieder können Einstellungen für Geräteverwaltung, Datenschutz, Verhinderung von Datenverlust, Berichte und Archivierung verwalten.|Complianceadministrator <br/><br/> Compliance-Suche <br/><br/> DLP-Compliance-Verwaltung <br/><br/> Geräteverwaltung <br/><br/> Disposition-Verwaltung <br/><br/> IB-Compliance-Management <br/><br/> 
            Benachrichtigungen verwalten <br/><br/> Organisationskonfiguration <br/><br/> RecordManagement <br/><br/> Aufbewahrungsverwaltung <br/><br/> Vertraulichkeits Bezeichnung-Administrator <br/><br/> Überwachungsprotokolle für die Anzeige <br/><br/> Management der DLP-Konformitätsverwaltung <br/><br/> Nur-anzeigen-Geräteverwaltung <br/><br/> View-Only IB Compliance Management <br/><br/> Benachrichtigungen verwalten <br/><br/> Schreibgeschützte Empfänger <br/><br/> Datensatzverwaltung mit Schreibschutz <br/><br/> Aufbewahrungsverwaltung (nur anzeigen)|
|**Daten Prüfer**|Mitglieder können Suchvorgänge für Postfächer, SharePoint-Websites und OneDrive-Konten durchführen.|Kommunikation <br/><br/> Compliance-Suche <br/><br/> Custodian <br/><br/> Daten Ermittlungsverwaltung <br/><br/> Exportieren<br/><br/> Vorschau <br/><br/> RMS-Entschlüsselung <br/><br/> Überprüfung|
|**eDiscovery-Manager**|Mitglieder können Suchvorgänge durchführen und Postfächer, SharePoint Online-Websites und OneDrive for Business-Orte im In-Situ-Speicher platzieren. Mitglieder können auch eDiscovery-Fälle erstellen und verwalten, einem Fall Mitglieder hinzufügen und daraus entfernen, mit einem Fall verknüpfte Inhalts Suchvorgänge erstellen und bearbeiten sowie Falldaten in Office 365 Advanced eDiscovery abrufen. <br/><br/> Ein eDiscovery-Administrator ist Mitglied der Rollengruppe "eDiscovery-Manager", der zusätzliche Berechtigungen zugewiesen wurden. Zusätzlich zu den Aufgaben, die ein eDiscovery-Manager ausführen kann, kann ein eDiscovery-Administrator Folgendes tun: <br/>• Anzeigen aller eDiscovery-Fälle in der Organisation. <br/>• Verwalten Sie alle eDiscovery-Fälle, nachdem Sie sich selbst als Mitglied der Anfrage hinzugefügt haben. <br/><br/> Der Hauptunterschied zwischen einem eDiscovery-Manager und einem eDiscovery-Administrator besteht darin, dass ein eDiscovery-Administrator auf alle Fälle zugreifen kann, die auf der Seite **eDiscovery-Fälle** im Security & Compliance Center aufgeführt sind. Ein eDiscovery-Manager kann nur auf die von ihm erstellten Fälle oder Fälle zugreifen, in denen er Mitglied ist. Weitere Informationen zum Erstellen eines eDiscovery-Administrators für einen Benutzer finden Sie unter [assign eDiscovery Permissions in the Office 365 Security & Compliance Center](assign-ediscovery-permissions.md).|Fallverwaltung <br/><br/> Kommunikation <br/><br/> Compliance-Suche <br/><br/> Custodian <br/><br/> Exportieren <br/><br/> Situ <br/><br/> Vorschau <br/><br/> RMS-Entschlüsselung <br/><br/> Überprüfung|
|**Mailflow-Administrator**|Mitglieder können im Security & Compliance Center Nachrichtenfluss-Einblicke und Berichte überwachen und anzeigen. Globale Administratoren können dieser Gruppe normale Benutzer hinzufügen, aber wenn der Benutzer kein Mitglied der Exchange-Verwaltungsgruppe ist, hat der Benutzer keinen Zugriff auf Aufgaben im Zusammenhang mit Exchange-Verwaltung.|Schreibgeschützte Empfänger|
|**Organisationsverwaltung** <sup>1</sup>|Mitglieder können Berechtigungen für den Zugriff auf Funktionen im Security & Compliance Center Steuern und auch Einstellungen für die Geräteverwaltung, die Verhinderung von Datenverlust, Berichte und die Aufbewahrung verwalten. <br/><br/> Beachten Sie, dass der Benutzer ein Exchange-Administrator sein muss, damit ein Benutzer, der kein globaler Administrator ist, die Liste der von MDM für Office 365 verwalteten Geräte anzeigen und Aktionen auf diesen Geräten ausführen kann, beispielsweise das Zurückziehen eines Geräts von MDM für Office 365. <br/><br/> Office 365 globale Administratoren werden automatisch als Mitglieder dieser Rollengruppe hinzugefügt.|Überwachungsprotokolle <br/><br/> Fallverwaltung <br/><br/> Complianceadministrator <br/><br/> Compliance-Suche <br/><br/> DLP-Compliance-Verwaltung <br/><br/> Geräteverwaltung <br/><br/> Disposition-Verwaltung <br/><br/> Situ <br/><br/> IB-Compliance-Management <br/><br/> 
            Benachrichtigungen verwalten <br/><br/> Organisationskonfiguration <br/><br/> RecordManagement <br/><br/> Aufbewahrungsverwaltung <br/><br/> Rollenverwaltung <br/><br/> Suchen und löschen <br/><br/> Sicherheitsadministrator <br/><br/> Sicherheits Leser <br/><br/> Vertraulichkeits Bezeichnung-Administrator <br/><br/> Ansicht "Dienstsicherheit" <br/><br/> Überwachungsprotokolle für die Anzeige <br/><br/> Management der DLP-Konformitätsverwaltung <br/><br/> Nur-anzeigen-Geräteverwaltung <br/><br/> View-Only IB Compliance Management <br/><br/> Benachrichtigungen verwalten <br/><br/> Schreibgeschützte Empfänger <br/><br/> Datensatzverwaltung mit Schreibschutz <br/><br/> Aufbewahrungsverwaltung (nur anzeigen)|
|**Datensatzverwaltung**|Mitglieder können Datensatzinhalte verwalten und freigeben.|Überwachungsprotokolle <br/><br/> RecordManagement <br/><br/> Aufbewahrungsverwaltung|
|**Reviewer**|Mitglieder können nur die Liste der Fälle auf der Seite eDiscovery-Fälle im Security & Compliance Center anzeigen. Sie können keine eDiscovery-Fälle erstellen, öffnen oder verwalten. Der primäre Zweck dieser Rollengruppe besteht darin, Mitgliedern das Anzeigen und Zugreifen auf Falldaten in Advanced eDiscovery zu ermöglichen. <br/><br/> Diese Rollengruppe verfügt über die restriktivsten Berechtigungen in Bezug auf eDiscovery.|Überprüfung|
|**Sicherheits Administrator**|Mitglieder dieser Rollengruppe können dienstübergreifende Administratoren sowie externe Partnergruppen und Microsoft-Support sein. Dieser Gruppe werden standardmäßig keine Rollen zugewiesen. Sie ist jedoch Mitglied der Rolle "Sicherheitsadministratoren" in Azure Active Directory und erbt die Funktionen dieser Rolle. Um Berechtigungen zentral zu verwalten, nehmen Sie Änderungen an dieser Rolle im Azure Active Directory Admin Center vor – Weitere Informationen finden Sie unter [Administrator Rollen Berechtigungen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). <br/><br/> Wenn Sie diese Rollengruppe im Security & Compliance Center bearbeiten, gelten diese Änderungen nur für das Security & Compliance Center und keine anderen Dienste, während Änderungen im Azure Active Directory Admin Center alle Dienste betreffen. <br/><br/> Alle schreibgeschützten Berechtigungen der Rolle "Sicherheits Leser" sowie eine Reihe zusätzlicher administrativer Berechtigungen für dieselben Dienste: Azure Information Protection, Identity Protection Center, privilegierte Identitätsverwaltung, Überwachen des Office 365-Diensts Integrität und Office 365 Security & Compliance Center.|Überwachungsprotokolle <br/><br/> DLP-Compliance-Verwaltung <br/><br/> Geräteverwaltung <br/><br/> IB-Compliance-Management <br/><br/> 
            Benachrichtigungen verwalten <br/><br/> Sicherheitsadministrator <br/><br/> Vertraulichkeits Bezeichnung-Administrator <br/><br/> Überwachungsprotokolle für die Anzeige <br/><br/> Management der DLP-Konformitätsverwaltung <br/><br/> Nur-anzeigen-Geräteverwaltung <br/><br/> View-Only IB Compliance Management <br/><br/> Benachrichtigungen verwalten|
|**Sicherheits Operator**|Mitglieder können Sicherheitswarnungen verwalten und auch Berichte und Einstellungen von Sicherheitsfunktionen anzeigen.|Compliance-Suche <br/><br/> 
            Benachrichtigungen verwalten <br/><br/> Sicherheits Leser <br/><br/> Überwachungsprotokolle für die Anzeige <br/><br/> Management der DLP-Konformitätsverwaltung <br/><br/> Nur-anzeigen-Geräteverwaltung <br/><br/> View-Only IB Compliance Management <br/><br/> Benachrichtigungen verwalten|
|**Sicherheits Leser**|Mitglieder verfügen über Lesezugriff auf eine Reihe von Sicherheitsfunktionen von Identity Protection Center, privilegierte Identitätsverwaltung, Überwachung der Office 365-Dienst Integrität und Office 365 Security & Compliance Center. <br/><br/> Die Mitgliedschaft in dieser Rollengruppe wird über die Dienste hinweg synchronisiert und zentral verwaltet. Mitglieder dieser Rollengruppe können dienstübergreifende Administratoren sowie externe Partnergruppen und Microsoft-Support sein. Dieser Gruppe werden standardmäßig keine Rollen zugewiesen. Sie ist jedoch Mitglied der Rolle "Sicherheits Leser" in Azure Active Directory und erbt die Funktionen dieser Rolle. Um Berechtigungen zentral zu verwalten, nehmen Sie Änderungen an dieser Rolle im Azure Active Directory Admin Center vor – Weitere Informationen finden Sie unter [Administrator Rollen Berechtigungen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Wenn Sie diese Rollengruppe im Security & Compliance Center bearbeiten, gelten diese Änderungen nur für das Security & Compliance Center und keine anderen Dienste, während Änderungen im Azure Active Directory Admin Center alle Dienste betreffen.|Sicherheits Leser <br/><br/> Management der DLP-Konformitätsverwaltung <br/><br/> Nur-anzeigen-Geräteverwaltung <br/><br/> View-Only IB Compliance Management <br/><br/> Benachrichtigungen verwalten|
|**Dienstüberprüfungsbenutzer**|Mitglieder können im Office 365 Security & Compliance Center auf den Abschnitt "Dienst Assurance" zugreifen. Service Assurance stellt Berichte und Dokumente bereit, in denen die Sicherheitsmethoden von Microsoft für Kundendaten beschrieben werden, die in Office 365 gespeichert sind. Darüber hinaus werden unabhängige Drittanbieter-Überwachungsberichte in Office 365 bereitgestellt. Weitere Informationen finden Sie unter [Service Assurance im Office 365 Security & Compliance Center](http://go.microsoft.com/fwlink/p/?LinkID=717765).|Ansicht "Dienstsicherheit"|
|**Aufsichtsüberprüfung**|Mitglieder können die Richtlinien erstellen und verwalten, die definieren, welche Kommunikation in einer Organisation einer Überprüfung unterliegt. Weitere Informationen finden Sie unter [configure Supervisory Review Policies for your organization](configure-supervision-policies.md).|Supervisory Review-Administrator|

> [!NOTE]
> <sup>1</sup> Diese Rollengruppe weist Mitgliedern nicht die Berechtigungen zu, die zum Durchsuchen des Office 365-Überwachungsprotokolls erforderlich sind, oder zum Verwenden von Berichten, die Exchange-Daten wie die DLP-oder ATP-Berichte beinhaltet. Zum Durchsuchen des Überwachungsprotokolls oder zum Anzeigen aller Berichte muss einem Benutzer in Exchange Online Berechtigungen zugewiesen werden. Dies liegt daran, dass das zugrunde liegende Cmdlet zum Durchsuchen des Überwachungsprotokolls ein Exchange Online-Cmdlet ist. Office 365 globale Administratoren können das Überwachungsprotokoll durchsuchen und alle Berichte anzeigen, da diese automatisch als Mitglieder der Rollengruppe "Organisationsverwaltung" in Exchange Online hinzugefügt werden. Weitere Informationen finden Sie unter [Durchsuchen des Überwachungsprotokolls im Office 365 Security & Compliance Center](https://go.microsoft.com/fwlink/p/?LinkID=708432).
  
## <a name="roles-in-the-security--compliance-center"></a>Rollen im Security & Compliance Center

In der folgenden Tabelle sind die verfügbaren Rollen und Rollengruppen aufgeführt, denen Sie standardmäßig zugewiesen sind.

Beachten Sie, dass die folgenden Rollen nicht standardmäßig der Rollengruppe "Organisationsverwaltung" zugewiesen sind:

- Kommunikation

- Custodian

- Daten Ermittlungsverwaltung

- Exportieren

- Vorschau

- Überprüfung

- RMS-Entschlüsselung

- Supervisory Review-Administrator

|**Rolle**|**Beschreibung**|**Standardrollengruppen Zuweisungen**|
|:-----|:-----|:-----|
|**Überwachungsprotokolle**|Aktivieren und konfigurieren Sie die Überwachung für die Office 365-Organisation, zeigen Sie die Überwachungsberichte der Organisation an, und exportieren Sie diese Berichte in eine Datei.|Organisationsverwaltung <br/><br/> Datensatzverwaltung <br/><br/> Sicherheitsadministrator|
|**Fallverwaltung**|Erstellen, bearbeiten, löschen und Steuern des Zugriffs auf eDiscovery-Fälle.|Complianceadministrator <br/><br/> eDiscovery-Manager <br/><br/> Organisationsverwaltung|
|**Daten Prüfer**|Führen Sie Suchvorgänge für Postfächer, SharePoint Online-Websites und OneDrive für Geschäftsstandorte durch.|Exportieren <br/><br/> RMS-Entschlüsselung <br/><br/> Custodian <br/><br/> Kommunikation <br/><br/> Überprüfung <br/><br/> Vorschau <br/><br/> Compliance-Suche <br/><br/> Daten Ermittlungsverwaltung|
|**Kommunikation**|Erstellen, bearbeiten, löschen und Steuern des Zugriffs auf die Kommunikation.|eDiscovery-Manager|
|**Complianceadministrator**|Anzeigen und Bearbeiten von Einstellungen und Berichten für Kompatibilitätsfeatures.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung|
|**Compliance-Suche**|Führen Sie Suchvorgänge in Postfächern durch und erhalten Sie eine Schätzung der Ergebnisse.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> eDiscovery-Manager <br/><br/> Organisationsverwaltung <br/><br/> Sicherheits Operator|
|**Custodian**|Erstellen, bearbeiten, löschen und Steuern des Zugriffs auf Verwalter.|eDiscovery-Manager|
|**Daten Ermittlungsverwaltung**|Erstellen, bearbeiten, löschen und Steuern des Zugriffs auf Daten Untersuchungen.|Daten Prüfer|
|**Geräteverwaltung**|Anzeigen und Bearbeiten von Einstellungen und Berichten für Geräteverwaltungsfunktionen.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator|
|**Disposition-Verwaltung**|Steuern Sie die Berechtigungen für den Zugriff auf die manuelle Disposition im Security & Compliance Center.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung|
|**DLP-Compliance-Verwaltung**|Anzeigen und Bearbeiten von Einstellungen und Berichten für DLP-Richtlinien (Data Loss Prevention).|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator|
|**Export**|Exportieren von Post Fach-und Websiteinhalten, die von Suchvorgängen zurückgegeben werden.|eDiscovery-Manager|
|**Situ**|Platzieren Sie Inhalte in Postfächern, Websites und öffentlichen Ordnern in der Warteschleife. In der Warteschleife wird eine Kopie des Inhalts an einem sicheren Speicherort gespeichert. Inhaltsbesitzer können weiterhin den ursprünglichen Inhalt ändern oder löschen.|Complianceadministrator <br/><br/> eDiscovery-Manager <br/><br/> Organisationsverwaltung|
|**IB-Compliance-Management**|Informationen zu Richtlinien anzeigen, erstellen, entfernen, ändern und testen.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator|
|**
            Benachrichtigungen verwalten**|Anzeigen und Bearbeiten von Einstellungen und Berichten für Warnungen.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator <br/><br/> Sicherheits Operator|
|**Organisationskonfiguration**|Ausführen, anzeigen und Exportieren von Überwachungsberichten und Verwalten von Kompatibilitätsrichtlinien für DLP, Geräte und Archivierung.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung|
|**Preview**|Zeigen Sie eine Liste der Elemente an, die von der Inhaltssuche zurückgegeben werden, und öffnen Sie jedes Element in der Liste, um den Inhalt anzuzeigen.|eDiscovery-Manager|
|**RecordManagement**|Anzeigen und Bearbeiten der Konfiguration und Berichte für die Daten Satz Verwaltungsfunktion.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Datensatzverwaltung|
|**Aufbewahrungsverwaltung**|Verwalten von Aufbewahrungsrichtlinien|Datensatzverwaltung <br/><br/> Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung|
|**Überprüfung**|Verwenden Sie Office 365 Advanced eDiscovery, um Dokumente nachzuverfolgen, zu markieren, zu analysieren und zu testen, die Ihnen zugewiesen sind.|eDiscovery-Manager <br/><br/> Reviewer|
|**RMS-Entschlüsselung**|Entschlüsseln von RMS-geschützten Inhalten beim Exportieren von Suchergebnissen|eDiscovery-Manager|
|**Rollenverwaltung**|Verwalten der Rollengruppenmitgliedschaft und erstellen oder Löschen von benutzerdefinierten Rollengruppen.|Organisationsverwaltung|
|**Suchen und löschen**|Ermöglicht Benutzern das Massen Entfernen von Daten, die den Kriterien einer Inhaltssuche entsprechen.|Organisationsverwaltung|
|**Sicherheits Administrator**|Anzeigen und Bearbeiten der Konfiguration und Berichte für Sicherheitsfunktionen.|Organisationsverwaltung <br/><br/> Sicherheitsadministrator|
|**Sicherheits Leser**|Zeigen Sie die Konfiguration und Berichte für Sicherheitsfunktionen an.|Organisationsverwaltung <br/><br/> Sicherheits Operator <br/><br/> Sicherheits Leser|
|**Vertraulichkeits Bezeichnung-Administrator**|Anzeigen, erstellen, ändern und Entfernen von Vertraulichkeits Beschriftungen.|Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator|
|**Ansicht "Dienstsicherheit"**|Laden Sie die verfügbaren Dokumente aus dem Abschnitt Service Assurance herunter. Zu den Inhalten gehören unabhängige Überwachungs-, Konformitäts-und Vertrauens bezogene Anleitungen für die Verwendung von Office 365-Features zur Verwaltung von Compliance-und Sicherheitsrisiken.|Dienstüberprüfungsbenutzer <br/><br/> Organisationsverwaltung|
|**Supervisory Review-Administrator**|Verwalten Sie Aufsichts Übersichts Richtlinien, einschließlich der zu überprüfenden Kommunikation und der Benutzer, die die Überprüfungen durchführen sollen.|Aufsichtsüberprüfung|
|**Überwachungsprotokolle für die Anzeige**|Anzeigen und Exportieren von Überwachungsberichten. Da diese Berichte vertrauliche Informationen enthalten können, sollten Sie diese Rolle nur Personen zuweisen, die explizit diese Informationen anzeigen müssen.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator <br/><br/> Sicherheits Operator|
|**Nur-anzeigen-Geräteverwaltung**|Zeigen Sie die Konfiguration und Berichte für das Feature Geräteverwaltung an.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator <br/><br/> Sicherheits Operator <br/><br/> Sicherheits Leser|
|**Management der DLP-Konformitätsverwaltung**|Anzeigen der Einstellungen und Berichte für DLP-Richtlinien (Data Loss Prevention).|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator <br/><br/> Sicherheits Operator <br/><br/> Sicherheits Leser|
|**View-Only IB Compliance Management**|Anzeigen der Konfiguration und Berichte für das Feature "Informationsbarrieren".|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Sicherheitsadministrator <br/><br/> Sicherheits Operator <br/><br/> Sicherheits Leser|
|**Benachrichtigungen verwalten**|Zeigen Sie die Konfiguration und Berichte für das Feature zum Verwalten von Benachrichtigungen an.|Sicherheitsadministrator <br/><br/> Sicherheits Operator <br/><br/> Sicherheits Leser <br/><br/> Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung|
|**Schreibgeschützte Empfänger**|Informationen zu Benutzern und Gruppen anzeigen.|Mailflow-Administrator <br/><br/> Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung|
|**Datensatzverwaltung mit Schreibschutz**|Zeigen Sie die Konfiguration und Berichte für die Daten Satz Verwaltungsfunktion an.|Complianceadministrator <br/><br/> Compliance-Daten Administrator <br/><br/> Organisationsverwaltung|
|**Aufbewahrungsverwaltung (nur anzeigen)**|Zeigen Sie die Konfiguration und Berichte für die Aufbewahrungs Verwaltungsfunktion an.|Compliance-Daten Administrator <br/><br/> Organisationsverwaltung <br/><br/> Complianceadministrator|
