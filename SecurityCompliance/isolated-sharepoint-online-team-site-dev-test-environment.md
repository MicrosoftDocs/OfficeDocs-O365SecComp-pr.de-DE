---
title: Isolierte SharePoint Online-Teamwebsite in Ihrer Office 365-Entwicklungs-/Testumgebung
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: d1795031-beef-49ea-a6fc-5da5450d320d
description: 'Zusammenfassung: Konfigurieren einer SharePoint Online-Teamwebsite, die vom Rest der Organisation in Ihrer Office 365-Entwicklungs-/Testumgebung isoliert ist.'
ms.openlocfilehash: 0aa5e6e47344134b1e103fb287f627afd2808af6
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345817"
---
# <a name="isolated-sharepoint-online-team-site-devtest-environment"></a>Isolierte SharePoint Online-Teamwebsite in Ihrer Office 365-Entwicklungs-/Testumgebung

 **Zusammenfassung:** Konfigurieren einer SharePoint Online-Teamwebsite, die vom Rest der Organisation in Ihrer Office 365-Entwicklungs-/Testumgebung isoliert ist.
  
SharePoint Online-Teamwebsites in Office 365 sind Orte für die Zusammenarbeit unter Verwendung einer gemeinsamen Dokumentbibliothek, eines OneNote-Notizbuchs und anderer Dienste. In vielen Fällen sind ein umfangreicher Zugriff sowie eine ausgedehnte Zusammenarbeit über Abteilungen oder Organisationen hinweg hilfreich. In einigen Fällen ist es jedoch empfehlenswert, den Zugriff und die Berechtigungen für die Zusammenarbeit in einer kleinen Personengruppe genau zu steuern.
  
Der Zugriff auf SharePoint Online-Teamwebsites und die Aktionen, die Benutzer ausführen können, werden durch SharePoint-Gruppen und Berechtigungsstufen gesteuert. SharePoint Online-Websites haben standardmäßig drei Zugriffsebenen:
  
- **Mitglieder**, die Ressourcen auf dieser Website anzeigen, erstellen und ändern können.
    
- **Besitzer**, die über eine vollständige Kontrolle über die Website verfügen, einschließlich der Fähigkeit, Berechtigungen zu ändern.
    
- **Besucher**, die Ressourcen auf der Website nur anzeigen können.
    
In diesem Artikel werden Sie durch die Konfiguration einer isolierten SharePoint Online-Teamwebsite für ein geheimes Forschungsprojekt mit dem Namen „ProjectX“ geführt. Die Zugriffsanforderungen sehen folgendermaßen aus:
  
- Nur Mitglieder des Projekts können auf die Website und deren Inhalte (Dokumente, OneNote-Notizbuch, Seiten) über SharePoint-Berechtigungsstufen zum Bearbeiten und Anzeigen zugreifen, die über die Gruppenmitgliedschaft gesteuert werden.
    
- Nur der Ersteller der Website und die Mitglieder einer Administratorengruppe für die Website können die Websiteverwaltung durchführen, die das Ändern von Berechtigungen auf Websiteebene umfasst.
    
Das Einrichten einer isolierten SharePoint Online-Teamwebsite in Ihrer Office 365-Entwicklungs-/Testumgebung umfasst drei Phasen:
  
1. Erstellen der Office 365-Entwicklungs-/Testumgebung
    
2. Erstellen der Benutzer und Gruppen für ProjectX.
    
3. Erstellen einer neuen SharePoint Online-Teamwebsite für ProjectX und Isolieren der Website.
    
> [!TIP]
> Klicken Sie [hier](http://aka.ms/catlgstack), um eine visuelle Darstellung aller Artikel im Stapel der Testumgebungsanleitungen in der Microsoft Cloud zu erhalten.
  
## <a name="phase-1-build-out-your-lightweight-or-simulated-enterprise-office-365-devtest-environment"></a>Phase 1: Erstellen einer einfachen oder simulierten Office 365-Unternehmensentwicklungs-/-testumgebung

Wenn Sie lediglich auf einfache Weise eine isolierte SharePoint Online-Teamwebsite mit den Mindestanforderungen erstellen möchten, befolgen Sie die Anweisungen in den Phasen 2 und 3 unter [Office 365-Entwicklungs-/Testumgebung](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).
  
Wenn Sie eine isolierte SharePoint Online-Teamwebsite in einer simulierten Unternehmenskonfiguration erstellen möchten, befolgen Sie die Anweisungen unter [DirSync für die Office 365-Entwicklungs-/Testumgebung](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment).
  
> [!NOTE]
> Für das Erstellen einer isolierten SharePoint Online-Website ist keine simulierte Unternehmensentwicklungs-/-testumgebung erforderlich, die ein simuliertes Intranet, das mit dem Internet verbunden ist, und die Verzeichnissynchronisierung für eine Windows Server Active Directory-Gesamtstruktur umfasst. Dies wird hier als Option bereitgestellt, damit Sie eine isolierte SharePoint Online-Website testen und damit in einer Umgebung, die eine typische Organisation darstellt, experimentieren können. 
  
## <a name="phase-2-create-user-accounts-and-access-groups"></a>Phase 2: Erstellen von Benutzerkonten und Zugriffsgruppen

Befolgen Sie die Anweisungen unter [Verbinden mit Office 365 PowerShell](https://technet.microsoft.com/library/dn975125.aspx), um eine Verbindung zu Ihrem Office 365-Testabonnement über Ihr globales Administratorkonto von folgender Stelle aus herzustellen:
  
- Ihrem Computer aus (für die einfache Office 365-Entwicklungs-/Testunternehmensumgebung).
    
- Dem virtuellen Computer CLIENT1 aus (für die simulierte Office 365-Entwicklungs-/Testumgebung).
    
Führen Sie die folgenden Befehle aus dem Microsoft Azure Active Directory-Modul für Windows PowerShell aus, um die neuen Zugriffsgruppen für die SharePoint Online-Teamwebsite für ProjectX zu erstellen:
  
```
$groupName="ProjectX-Members"
$groupDesc="People allowed to collaborate for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Admins"
$groupDesc="People allowed to administer SharePoint for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Viewers"
$groupDesc="People allowed to view the SharePoint resources for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
```

> [!TIP]
> Klicken Sie [hier](https://gallery.technet.microsoft.com/PowerShell-commands-for-an-b2608df1), um eine Textdatei herunterzuladen, die alle PowerShell-Befehle in diesem Artikel enthält.
  
Geben Sie den Namen Ihrer Organisation (z. B. „contosotoycompany“) und den zweistelligen Ländercode für Ihren Standort ein. Führen Sie dann über die Eingabeaufforderung des Windows Azure Active Directory-Moduls für Windows PowerShell die folgenden Befehle aus:
  
```
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$licAssignment= $orgName + ":ENTERPRISEPREMIUM"
$userName= "designer@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Designer" -FirstName Lead -LastName Designer -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

Notieren Sie aus der **New-MsolUser** -Befehlsanzeige das Kennwort, das für das Lead Designer-Konto generiert wurde, und bewahren Sie es an einem sicheren Ort auf.
  
Führen Sie über die „Windows Azure Active Directory-Modul für Windows PowerShell“-Eingabeaufforderung die folgenden Befehle aus:
  
```
$userName= "researcher@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Researcher" -FirstName Lead -LastName Researcher -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

Notieren Sie aus der **New-MsolUser** -Befehlsanzeige das Kennwort, das für das Lead Researcher-Konto generiert wurde, und bewahren Sie es an einem sicheren Ort auf.
  
Führen Sie über die „Windows Azure Active Directory-Modul für Windows PowerShell“-Eingabeaufforderung die folgenden Befehle aus:
  
```
$userName= "devvp@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Development VP" -FirstName Development -LastName VP -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

Notieren Sie aus der **New-MsolUser** -Befehlsanzeige das Kennwort, das für das Development VP-Konto generiert wurde, und bewahren Sie es an einem sicheren Ort auf.
  
Führen Sie als Nächstes die folgenden PowerShell-Befehle aus dem Microsoft Azure Active Directory-Modul für Windows PowerShell aus, um die neuen Konten zu den neuen Zugriffsgruppen hinzuzufügen:
  
```
$grpName="ProjectX-Members"
$userUPN="designer@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$userUPN="researcher@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Admins"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userCredential.UserName }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Viewers"
$userUPN="devvp@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
```

Ergebnisse:
  
- Die Zugriffsgruppe „ProjectX-Members“ enthält die Benutzerkonten „Lead Designer“ und „Lead Researcher“.
    
- Die Zugriffsgruppe „ProjectX-Admins“ enthält das globale Administratorkonto für das Testabonnement.
    
- Die Zugriffsgruppe „ProjectX-Viewers“ enthält das Benutzerkonto „Development VP“.
    
Abbildung 1 zeigt die Zugriffsgruppen und ihre Mitgliedschaft.
  
**Abbildung 1**

![Die Office 365-Gruppen und deren Mitgliedschaft für eine isolierte SharePoint Online-Gruppenwebsite](media/5b7373b9-2a80-4880-afe5-63ffb17237e6.png)
  
## <a name="phase-3-create-a-new-projectx-sharepoint-online-team-site-and-isolate-it"></a>Phase 3: Erstellen einer neuen SharePoint Online-Teamwebsite für ProjectX und Isolieren der Website

Führen Sie folgende Schritte aus, um eine SharePoint Online-Teamwebsite für ProjectX zu erstellen:
  
1. Mithilfe eines Browsers entweder auf den lokalen Computer (einfache Konfiguration) oder auf CLIENT1 (simulierten Enterprise-Konfiguration), melden Sie sich bei Office 365-Portal ([https://portal.office.com](https://portal.office.com)) mit Ihrer globalen Administratorkonto an.
    
2. Klicken Sie in der Liste von Kacheln auf **SharePoint**.
    
3. Klicken Sie auf der neuen SharePoint-Registerkarte in Ihrem Browser auf **+ Website erstellen**.
    
4. Geben Sie unter **Name der Teamwebsite** den Namen **ProjectX** ein. Wählen Sie in den **Datenschutzeinstellungen** die Option **Privat - nur Mitglieder können auf diese Website zugreifen** aus.
    
5. Geben Sie unter **Beschreibung der Teamwebsite** den Text **SharePoint-Website für ProjectX** ein, und klicken Sie dann auf **Weiter**.
    
6. Klicken Sie im Bereich **Wer soll hinzugefügt werden**? auf **Fertig stellen**.
    
7. Klicken Sie auf der neuen Registerkarte **ProjectX-Home** in Ihrem Browser auf der Symbolleiste auf das Symbol „Einstellungen", und klicken Sie dann auf **Websiteberechtigungen**.
    
8. Klicken Sie im Bereich **Websiteberechtigungen** auf **Erweiterte Berechtigungseinstellungen**.
    
9. Klicken Sie auf der neuen Registerkarte **Berechtigungen: ProjectX** in Ihrem Browser auf **Einstellungen für Zugriffsrechteanforderungen**.
    
10. Deaktivieren Sie im Dialogfeld **Einstellungen für Zugriffsrechteanforderungen** die Optionen **Mitgliedern das Freigeben der Website sowie einzelner Dateien und Ordner erlauben** und **Zugriffsanforderungen zulassen** (sodass alle drei Kontrollkästchen deaktiviert sind), und klicken Sie dann auf **OK**.
    
11. Klicken Sie in der Liste auf **ProjectX-Members**.
    
12. Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.
    
13. Geben Sie im Dialogfeld **Freigeben** **ProjectX-Members** ein, wählen Sie die Option aus, und klicken Sie dann auf **Freigeben**.
    
14. Klicken Sie auf die Schaltfläche „Zurück“ in Ihrem Browser.
    
15. Klicken Sie in der Liste auf **ProjectX-Owners**.
    
16. Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.
    
17. Geben Sie im Dialogfeld **Freigeben** **ProjectX-Admins** ein, wählen Sie die Option aus, und klicken Sie dann auf **Freigeben**.
    
18. Klicken Sie auf die Schaltfläche „Zurück“ in Ihrem Browser.
    
19. Klicken Sie in der Liste auf **ProjectX-Visitors**.
    
20. Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.
    
21. Geben Sie im Dialogfeld **Freigeben** **ProjectX-Viewers** ein, wählen Sie die Option aus, und klicken Sie dann auf **Freigeben**.
    
22. Schließen Sie die Registerkarte **Benutzer und Gruppen** in Ihrem Browser, klicken Sie auf die Registerkarte **ProjectX-Home** in Ihrem Browser, und schließen Sie dann den Bereich **Websiteberechtigungen**.
    
Ergebnisse der Konfiguration von Berechtigungen:
  
- Die SharePoint-Gruppe „ProjectX Members“ enthält nur die Zugriffsgruppe „ProjectX-Members“ (die nur die Benutzerkonten „Lead Designer“ und „Lead Researcher“ enthält) und die Gruppe „ProjectX“ (die nur das Benutzerkonto des globalen Administrators enthält).
    
- Die SharePoint-Gruppe „ProjectX Owners“ enthält nur die Zugriffsgruppe „ProjectX-Admins“ (die nur das Benutzerkonto des globalen Administrators enthält).
    
- Die SharePoint-Gruppe „ProjectX Visitors“ enthält nur die Zugriffsgruppe „ProjectX-Viewers“ (die nur das Benutzerkonto „Development VP“ enthält).
    
- Mitglieder können keine Berechtigungen auf Websiteebene ändern (dies kann nur von Mitgliedern der Gruppe „ProjectX-Admins“ ausgeführt werden).
    
- Andere Benutzerkonten können nicht auf die Website oder ihre Ressourcen zugreifen oder Zugriff auf die Website anfordern.
    
In Abbildung 2 sind die SharePoint-Gruppen und ihre Mitgliedschaft dargestellt.
  
**Abbildung 2**

![Die SharePoint Online-Gruppen und deren Mitgliedschaft für eine isolierte SharePoint Online-Gruppenwebsite](media/595abff4-64f9-49de-a37a-c70c6856936b.png)
  
Nachfolgend wird der Zugriff unter Verwendung des Lead Designer-Benutzerkontos veranschaulicht:
  
1. Klicken Sie auf die Registerkarte **ProjectX-Home** in Ihrem Browser, und klicken Sie dann auf die Registerkarte **Microsoft Office Home** im Browser.
    
2. Klicken Sie auf den Namen des globalen Administrators, und klicken Sie dann auf **Abmelden**.
    
3. Melden Sie sich bei Office 365-Portal ([https://portal.office.com](https://portal.office.com)) mit den Designer führen Kontonamen und das zugehörige Kennwort.
    
4. Klicken Sie in der Liste von Kacheln auf **SharePoint**.
    
5. Geben Sie auf der neuen Registerkarte **SharePoint** in Ihrem Browser **ProjectX** in das Suchfeld ein, aktivieren Sie die Suche, und klicken Sie dann auf die Teamwebsite **ProjectX**. Für die ProjectX-Teamwebsite sollte nun eine neue Registerkarte im Browser angezeigt werden.
    
6. Klicken Sie auf das Symbol „Einstellungen". Beachten Sie, dass keine Option für **Websiteberechtigungen** vorhanden ist. Dies ist richtig, da nur die Mitglieder der Gruppe „ProjectX-Admins" Berechtigungen für die Website ändern können.
    
7. Öffnen Sie Editor oder einen anderen Text-Editor Ihrer Wahl.
    
8. Kopieren Sie die URL der ProjectX-Teamwebsite, und fügen Sie sie in einer neuen Zeile in Editor oder in Ihrem Text-Editor ein.
    
9. Klicken Sie auf der neuen Registerkarte **ProjectX-Home** im Browser auf **Dokumente**.
    
10. Kopieren Sie die URL des ProjectX-Dokumentordners, und fügen Sie sie in einer neuen Zeile in Editor oder in Ihrem Text-Editor ein.
    
11. Klicken Sie auf der neuen Registerkarte **ProjectX-Dokumente** im Browser auf **Neu > Word-Dokument**.
    
12. Geben Sie auf der Seite **Word Online** etwas Text ein, warten Sie, bis der Status **Gespeichert** lautet, klicken Sie auf die Schaltfläche „Zurück" in Ihrem Browser, und aktualisieren Sie dann die Seite. Im Ordner **Dokumente** sollte nun ein neues Dokument **Document.docx** angezeigt werden.
    
13. Klicken Sie auf die Auslassungspunkte für das Dokument **Document.docx**, und klicken Sie dann auf **Link abrufen**.
    
14. Kopieren Sie die URL in das Dialogfeld **„Document.docx" freigeben**, und fügen Sie sie in einer neuen Zeile in Editor oder in Ihrem Text-Editor ein, und schließen Sie dann das Dialogfeld **„Document.docx"**.
    
15. Schließen Sie die Registerkarten **ProjectX-Dokumente** und **SharePoint** in Ihrem Browser, und klicken Sie dann auf die Registerkarte **Microsoft Office Home** im Browser.
    
16. Klicken Sie auf den Namen **Lead Designer**, und klicken Sie dann auf **Abmelden**.
    
Nachfolgend wird der Zugriff unter Verwendung des Development VP-Benutzerkontos veranschaulicht:
  
1. Melden Sie sich bei Office 365-Portal ([https://portal.office.com](https://portal.office.com)) mit der Entwicklung VP Kontoname und das zugehörige Kennwort.
    
2. Klicken Sie in der Liste von Kacheln auf **SharePoint**.
    
3. Geben Sie auf der neuen Registerkarte **SharePoint** in Ihrem Browser **ProjectX** in das Suchfeld ein, aktivieren Sie die Suche, und klicken Sie dann auf die Teamwebsite **ProjectX**. Für die ProjectX-Teamwebsite sollte nun eine neue Registerkarte im Browser angezeigt werden.
    
4. Klicken Sie auf **Dokumente**, und klicken Sie dann auf die Datei **Document.docx**.
    
5. Versuchen Sie, auf der Registerkarte **Document.docx** in Ihrem Browser den Text zu ändern. Es sollte eine Meldung angezeigt werden, die besagt, dass **dieses Dokument schreibgeschützt ist**. Dies wird erwartet, da das Development VP-Benutzerkonto nur über Anzeigeberechtigungen für die Website verfügt.
    
6. Schließen Sie die Registerkarten **Document.docx**, **ProjectX-Dokumente** und **SharePoint** in Ihrem Browser.
    
7. Klicken Sie auf der Registerkarte **Microsoft Office Home** auf den Namen **Development VP**, und klicken Sie dann auf **Abmelden**.
    
Nachfolgend wird der Zugriff mit einem Benutzerkonto ohne Berechtigungen veranschaulicht:
  
1. Melden Sie sich bei Office 365-Portal ([https://portal.office.com](https://portal.office.com)) mit den Kontonamen des Benutzers 3 und das zugehörige Kennwort.
    
2. Klicken Sie in der Liste von Kacheln auf **SharePoint**.
    
3. Geben Sie auf der Registerkarte **SharePoint** in Ihrem Browser **ProjectX** im Suchfeld ein, aktivieren Sie dann die Suche. Es sollte die Meldung **Leider gibt es hierzu keine Suchergebnisse** angezeigt werden.
    
4. Kopieren Sie aus der geöffneten Instanz von Editor oder Ihres Text-Editors die URL für die ProjectX-Website in die Adressleiste Ihres Browsers, und drücken Sie die **EINGABETASTE**. Die Seite **Zugriff verweigert** sollte angezeigt werden.
    
5. Kopieren Sie aus Editor oder aus Ihrem Text-Editor die URL für den ProjectX-Dokumenteordner in die Adressleiste Ihres Browsers, und drücken Sie die **EINGABETASTE**. Die Seite **Zugriff verweigert** sollte angezeigt werden.
    
6. Kopieren Sie aus Editor oder aus Ihrem Text-Editor die URL für die Datei „Documents.docx" in die Adressleiste Ihres Browsers, und drücken Sie die **EINGABETASTE**. Die Seite **Zugriff verweigert** sollte angezeigt werden.
    
7. Schließen Sie die Registerkarte **SharePoint** in Ihrem Browser, klicken Sie auf die Registerkarte **Microsoft Office Home**, klicken Sie auf den Namen **Benutzer 3**, und klicken Sie dann auf **Abmelden**.
    
Sie können nun weiter mit der isolierten SharePoint Online-Website experimentieren.
  
## <a name="next-step"></a>Nächster Schritt

Wenn Sie eine isolierte SharePoint Online-Teamwebsite in der Produktion bereitstellen möchten, lesen Sie die schrittweisen Überlegungen zum Entwurf unter [Entwerfen einer isolierten SharePoint Online-Teamwebsite](design-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Siehe auch

[Isolierte SharePoint Online-Teamwebsites](isolated-sharepoint-online-team-sites.md)
  
[Testumgebungsanleitungen (TLGs) zur Cloudakzeptanz](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[Basiskonfiguration der Entwicklungs-/Testumgebung](https://docs.microsoft.com/office365/enterprise/base-configuration-dev-test-environment)
  
[Office 365-Entwicklungs-/Testumgebung](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)
  
[Cloudakzeptanz und Hybridlösungen](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




