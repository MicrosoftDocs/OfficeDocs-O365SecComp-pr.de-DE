---
title: Konfigurieren der Berechtigungsfilterung für die Compliancesuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1adffc35-38e5-4f7d-8495-8e0e8721f377
description: Verwenden Sie Inhaltssuche Berechtigungen Filterung, um ein eDiscovery-Manager nur eine Teilmenge von Postfächern und Websites in Office 365-Organisation durchsuchen können.
ms.openlocfilehash: 2b6968a097e7abe5943a84b9ceb9b6d126057cc2
ms.sourcegitcommit: c166964fe14eec69139a2d3d9c10d2c40ab33f91
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2018
ms.locfileid: "23258623"
---
# <a name="configure-permissions-filtering-for-content-search"></a>Konfigurieren der Berechtigungsfilterung für die Compliancesuche

Suche Berechtigungen filtern, um ein eDiscovery-Manager nur eine Teilmenge von Postfächern und Websites in Office 365-Organisation durchsuchen lassen können. Sie können auch Berechtigungen filtern, um zuzulassen, derselben eDiscovery-Manager nur für Postfach oder Website Inhalte zu suchen, die einem bestimmten Suchkriterium entsprechen. Beispielsweise können Sie einen eDiscovery-Manager nur die Postfächer der Benutzer in einem bestimmten Standort oder jede Abteilung gesucht. Zu diesem Zweck erstellen einen Filter, der einen unterstützten Empfängerfilter verwendet, um einzuschränken, welche Postfächer durchsucht werden können. Sie können auch einen Filter erstellen, der angibt, welche Postfachinhalte durchsucht werden kann. Dies erfolgt durch Erstellen eines Filters, das eine Eigenschaft durchsuchbar verwendet. In ähnlicher Weise können Sie einen eDiscovery-Manager nur bestimmte SharePoint-Websites in Ihrer Organisation zu suchen. Zu diesem Zweck Erstellen eines Filters, das beschränkt, welche Website durchsucht werden kann. Sie können auch einen Filter erstellen, der angibt, welche Websiteinhalte durchsucht werden kann. Dies erfolgt durch Erstellen eines Filters, das eine Websiteeigenschaft durchsuchbar verwendet.

Sie können auch die Suche Berechtigungen Filter zur logische Grenzen ( *Compliance Grenzen*bezeichnet) innerhalb einer Office 365-Organisation zu erstellen, die die Speicherorte für Benutzer Inhalte (wie Postfächer, SharePoint-Websites und OneDrive Konten) steuern, Suche können Sie bestimmte eDiscovery-Manager. Weitere Informationen finden Sie unter [Einrichten von Compliance-Grenzen für eDiscovery Untersuchungen in Office 365](set-up-compliance-boundaries.md).
  
Filtern von Search-Berechtigungen wird durch das Inhaltssuche-Feature in die Office 365-Sicherheit unterstützt &amp; Compliance Center. Diese vier Cmdlets können Sie die konfigurieren und Verwalten von Suchfiltern Permisisons:
  
[Neue ComplianceSecurityFilter](#new-compliancesecurityfilter)

[Get-ComplianceSecurityFilter](#get-compliancesecurityfilter)

[Set-ComplianceSecurityFilter](#set-compliancesecurityfilter)

[Remove-ComplianceSecurityFilter](#remove-compliancesecurityfilter)

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um die Einhaltung von Bestimmungen Sicherheit Filter-Cmdlets ausführen zu können, müssen Sie Mitglied der Rollengruppe "Organisationsverwaltung" in das Wertpapier sein &amp; Compliance Center. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
- Sie müssen sowohl die Sicherheit Windows PowerShell herstellen &amp; Compliance Center und Ihrer Exchange Online-Organisation auf die Einhaltung von Bestimmungen Sicherheit Filter-Cmdlets verwenden. Dies ist erforderlich, da diese Cmdlets Zugriff auf Eigenschaften von Benutzerpostfächern aus diesem benötigen Grund Sie haben die Verbindung zu Exchange Online. Lesen Sie die Schritte im nächsten Abschnitt. 
    
- Weitere Informationen über Berechtigungsfilter für die Suche finden Sie im Abschnitt [More information](#more-information). 
    
- Filtern von Search-Berechtigungen gilt für inaktive Postfächer, was bedeutet, dass Sie verwenden können, Postfach- und Inhaltsfilter-Postfach einschränken, wer ein inaktives Postfachs suchen können. Finden Sie [Weitere Informationen](#more-information) im Abschnitt zusätzliche Informationen zu Berechtigungen, die Filterung und inaktive Postfächer. 
    
-  Filtern von Search-Berechtigungen können nicht verwendet werden, zu beschränken, die die öffentlichen Ordner im Exchange durchsuchen können. 
    
- Es gibt keine Begrenzung der Anzahl der Berechtigungen Suchfilter, die in einer Organisation erstellt werden können. Suchleistung wird jedoch beeinträchtigt werden, wenn mehr als 100 Suchfilter Berechtigungen vorhanden sind. Um die Anzahl der Suchfilter Berechtigungen in Ihrer Organisation so gering wie möglich zu halten, erstellen Sie Filter, die Regeln in einem einzelnen Filter nach Möglichkeit für Exchange, SharePoint und OneDrive zu kombinieren.
    
## <a name="connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Verbinden mit der Sicherheit &amp; Compliance Center und Exchange Online in einer einzigen remote-PowerShell-Sitzung

1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe von Filename Suffix. ps1. Beispielsweise konnten Sie es in eine Datei namens ConnectEXO CC.ps1 speichern.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem das Skript, das Sie im vorherigen Schritt erstellt haben befindet, und führen Sie das Skript; Zum Beispiel:
    
    ```
    .\ConnectEXO-CC.ps1
    ```
 
Woher wissen Sie, ob dies funktioniert? Nach dem Ausführen des Skripts,-Cmdlets auf die Sicherheit &amp; Compliance Center und Exchange Online in Ihre lokale Windows PowerShell-Sitzung importiert werden. Wenn Sie keine Fehler erhalten, verbunden Sie erfolgreich. Ein schnelles Test ist zum Ausführen eines Wertpapiers &amp; Compliance Center-Cmdlet – beispielsweise **Install-UnifiedCompliancePrerequisite** – und einer Exchange Online-Cmdlets wie **Get-Mailbox**. 
  
Wenn Sie Fehlermeldungen erhalten, überprüfen Sie die folgenden Anforderungen:
  
- Ein häufig auftretendes Problem ist ein falsches Kennwort. Führen Sie die beiden Schritte erneut durch, und achten Sie besonders auf die korrekte Eingabe des Benutzernamens und Kennworts in Schritt 1.
    
- Stellen Sie sicher, dass Ihr Konto über die Berechtigung zum Zugriff auf die Sicherheit hat &amp; Compliance Center. Weitere Informationen hierzu finden Sie unter [Gewähren des Zugriffs auf die Sicherheit &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md).
    
- Um Denial-of-Service (DoS) Angriffe zu verhindern, Sie sind drei offenen remote PowerShell-Verbindungen für die Sicherheit auf beschränkt &amp; Compliance Center.
    
- Windows PowerShell muss zum Ausführen von Skripts konfiguriert werden. Sie müssen diese Einstellung nur einmalig auf Ihrem Computer konfigurieren, und nicht bei jedem Verbindungsaufbau. Um Windows PowerShell für das Ausführen von signierten Skripts zu aktivieren, müssen Sie den folgenden Befehl in einem Windows PowerShell-Fenster mit erhöhten Rechten ausführen (ein Windows PowerShell-Fenster, das Sie durch Auswahl von **Als Administrator ausführen**) geöffnet haben.

    ```
    Set-ExecutionPolicy RemoteSigned
    ```
- Verkehr auf TCP-Port 80 muss zwischen dem lokalen Computer und Office 365 geöffnet sein. Es ist wahrscheinlich geöffnet, aber es ist eine Möglichkeit, wenn Ihre Organisation eine restriktive Internet Access Richtlinie verfügt.
    

  
## <a name="new-compliancesecurityfilter"></a>Neue ComplianceSecurityFilter
<a name="New"> </a>

Die **New-ComplianceSecurityFilter** wird verwendet, um einen neuen Berechtigungen Suchfilter zu erstellen. In der folgenden Tabelle werden die Parameter für dieses Cmdlet beschrieben. Zum Erstellen eines Compliance-Sicherheitsfilter sind alle Parameter erforderlich. 
  
|**Parameter**|**Beschreibung**|
|:-----|:-----|
| _Aktion_ <br/> | _Der Aktionsparameter_ gibt diese Art von Search-Aktion, die auf der Filter angewendet wird. Die möglichen Inhaltssuche Aktionen sind:<br/><br/> **Export** - Filter wird beim Exportieren von Suchergebnissen angewendet.  <br/> **Preview** - Filter wird angewendet, beim Anzeigen der Vorschau der Suchergebnisse.  <br/> **Bereinigen** - Filter wird angewendet, wenn Suchergebnisse zu löschen.  <br/> **Suche** – der Filter wird angewendet, wenn eine Suche ausgeführt.  <br/> **Alle** - der Filter wird auf alle Suche Aktionen angewendet.  <br/> |
| _FilterName_ <br/> |Der _FilterName_ -Parameter gibt den Namen des Filters Berechtigungen. Bei diesem Namen wird einen Filter verwendet, um die Identität bei Verwendung der Cmdlets **Get-ComplianceSecurityFilter**, **Set-ComplianceSecurityFilter,** und **Remove-ComplianceSecurityFilter** .<br/> |
| _Filter_ <br/> | Der _Filter_ -Parameter gibt die Suchkriterien für die Einhaltung von Bestimmungen Sicherheitsfilter. Sie können drei verschiedene Art der Filter erstellen:<br/><br/> **Filtern von Postfach** - diese Art von Filter gibt an, die Postfächer, die die zugewiesene Benutzer (durch den _Benutzer_ -Parameter angegebenen) durchsuchen können. Die Syntax für diese Art von Filter ist **Mailbox_** _MailboxPropertyName_, dabei _MailboxPropertyName_ an ein Postfach-Eigenschaft verwendet, um die Postfächer zu begrenzen, die durchsucht werden können. Beispielsweise das Postfach Filter `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` würde ermöglicht dem Benutzer zugewiesen dieser Filter nur Postfächer suchen mit dem Wert "OttawaUsers" in die CustomAttribute10-Eigenschaft.<br/>  Für die _MailboxPropertyName_ -Eigenschaft kann eine beliebige unterstützte filterbare Empfänger-Eigenschaft verwendet werden. Eine Liste der unterstützten Eigenschaften finden Sie unter [filterbaren Eigenschaften für den Parameter RecipientFilter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/> **Filtern von Inhalt von Postfächern** - diese Art von Filter wird auf den Inhalt angewendet, die durchsucht werden können. Es gibt den Inhalt von Postfächern, die, dem für die zugewiesene Benutzer durchsuchen können. Die Syntax für diese Art von Filter ist **MailboxContent_** _SearchablePropertyName:value_, wobei _SearchablePropertyName_ ein Schlüsselwort Query Language (KQL)-Eigenschaft gibt an, die in einer Inhaltssuche angegeben werden können. Beispielsweise das Postfach Inhaltsfilter `MailboxContent_recipients:contoso.com` ermöglicht dem Benutzer zugewiesen dieser Filter nur die Suche nach Nachrichten, die an Empfänger in der Domäne "contoso.com" gesendet.<br/>  Eine Liste mit Nachrichteneigenschaften durchsucht werden finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md).  <br/><br/> **Filtern von Website- und Website** - befinden sich zwei SharePoint und OneDrive for Business Website bezogenen Filter, die Sie verwenden können, um anzugeben, welche Website oder Websiteinhalte zugewiesene Benutzer suchen können:  <br/><br/> - **Site_** _SearchableSiteProperty_ <br/> - **SiteContent_** _SearchableSiteProperty_ <br/><br/>  Diese beiden Filter sind austauschbar. beispielsweise `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` und `"SiteContent_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` die gleichen Ergebnisse zurückgegeben werden. Zur einfacheren Funktionsweise ein Filters zu identifizieren, Sie können jedoch `Site_` Website bezogenen-Eigenschaften (wie eine Website-URL) angeben und `SiteContent_` an Content-bezogene-Eigenschaften (wie Dokumenttypen. Beispielsweise den Filter `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` ermöglicht dem Benutzer zugewiesen dieser Filter nur die Suche nach Inhalten in der https://contoso.sharepoint.com/sites/doctors Websitesammlung festlegen. Der Filter `"SiteContent_FileExtension -eq 'docx'"` ermöglicht dem Benutzer zugewiesen dieser Filter nur für Word-Dokumente (Word 2007 und später) suchen.<br/><br/>  Eine Liste der Eigenschaften von durchsuchbaren finden Sie unter [Übersicht über durchforstete und verwaltete Eigenschaften in SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Eigenschaften mit **Ja** in markiert die ** Queryable ** Spalte zum Erstellen einer Website oder Inhaltsfilter Website verwendet werden.<br/> <br/> **Wichtig:**  Ein einzelnes Suchfilter kann nur einen Typ des Filters vorhanden sein. Es ist nicht möglich eine Postfach-Filter und einen Filter für die Website enthalten. Es kann nicht auf ähnliche Weise einen Postfach-Filter und Postfach Inhaltsfilter enthalten. Ein Filter kann jedoch eine komplexere Abfrage des gleichen Typs enthalten. Zum Beispiel`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"` <br/><br/> **Wichtig:** Sie müssen einen Suchfilter Berechtigungen explizit hindern Suche Speicherorte für Inhalte in einem bestimmten Office 365-Dienst (beispielsweise verhindern, dass einen Benutzer alle Exchange-Postfach oder einer beliebigen SharePoint-Website suchen) zu erstellen. Anders ausgedrückt, keinen Suchfilter für Berechtigungen, der einem Benutzer ermöglicht, suchen Sie alle SharePoint-Websites in der Organisation erstellen gehindert, Postfächer zu suchen. Damit können SharePoint-Administratoren nur SharePoint-Websites suchen, müssen Sie beispielsweise einen Filter erstellen, der verhindert, dass sie Postfächer zu suchen. Damit Exchange-Administratoren Postfächer nur suchen können, müssen Sie auf ähnliche Weise einen Filter erstellen, der verhindert, dass diese Websites suchen.           |
| _Benutzer_ <br/> |Der _Benutzer_ -Parameter gibt die Benutzer, die dieser Filter angewendet, deren Content-Suche zu erhalten. Identifizieren von Benutzern durch ihren Alias oder die primäre SMTP-Adresse. Sie können mehrere Werte durch Kommas getrennt angeben, oder Sie können den Filter für alle Benutzer mit dem **Alle**Wert zuweisen.<br/> Sie können auch den _Benutzer_ -Parameter zum Angeben eines Wertpapiers &amp; Compliance Center Rollengruppe. Hiermit können Sie eine benutzerdefinierte Rollengruppe zu erstellen, und weisen Sie diese Rolle gruppieren Berechtigungen Suchfilter Nehmen wir beispielsweise an, dass Sie eine benutzerdefinierte Rollengruppe für eDiscovery-Manager für die USA Niederlassung von einem multinationale Unternehmen verfügen. Den Parameter _Benutzer_ können Sie dieser Rollengruppe (mithilfe der Name-Eigenschaft der Rollengruppe) angeben, und klicken Sie dann die Parameter " _Filter_ " verwenden, um nur die Postfächer in den USA zu durchsuchenden erlauben.<br/> Sie können mit diesem Parameter keine Verteilergruppen angeben.  <br/> |
   

## <a name="examples-of-creating-search-permissions-filters"></a>Beispiele für das Erstellen von Suchfiltern Berechtigungen

Nachfolgend finden Sie Beispiele für die Verwendung des **New-ComplianceSecurityFilter**-Cmdlets zum Erstellen eines Berechtigungsfilters für die Suche. 
  
In diesem Beispiel können die Benutzer annb@contoso.com zum Ausführen von Aktionen für alle Inhaltssuche nur für Postfächer in Kanada. Dieser Filter enthält die dreistelligen Ländervorwahl für Kanada ISO 3166-1.

```
New-ComplianceSecurityFilter -FilterName CountryFilter  -Users annb@contoso.com -Filters "Mailbox_CountryCode  -eq '124'" -Action All
```

In diesem Beispiel können die Benutzer „donh“ und „suzanf“ nur die Postfächer durchsuchen, die den Wert „Marketing“ für die Postfacheigenschaft „CustomAttribute1“ aufweisen.

```
New-ComplianceSecurityFilter -FilterName MarketingFilter  -Users donh,suzanf -Filters "Mailbox_CustomAttribute1  -eq 'Marketing'" -Action Search
```
   
In diesem Beispiel können Mitglieder der Rollengruppe „US Discovery Managers“ alle Inhaltssuchvorgänge nur für Postfächer in den USA durchführen. Dieser Filter enthält die dreistellige Landeskennzahl für die USA gemäß ISO 3166-1.
  
```
New-ComplianceSecurityFilter -FilterName USDiscoveryManagers  -Users "US Discovery Managers" -Filters "Mailbox_CountryCode  -eq '840'" -Action All
```

In diesem Beispiel können Mitglieder der eDiscovery-Manager-Rollengruppe nur die Postfächer von Mitgliedern der Verteilergruppe „Ottawa Users“ durchsuchen. 
  
```
$DG = Get-DistributionGroup "Ottawa Users"
```

```
New-ComplianceSecurityFilter -FilterName DGFilter  -Users eDiscoveryManager -Filters "Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'" -Action Search
```
In diesem Beispiel wird verhindert, dass Benutzer Inhalt aus den Postfächern der Mitglieder der Verteilergruppe „Executive Team“ löschen.

```
$DG = Get-DistributionGroup "Executive Team"
```

```
New-ComplianceSecurityFilter -FilterName NoExecutivesPreview  -Users all -Filters "Mailbox_MemberOfGroup -ne '$($DG.DistinguishedName)'" -Action Purge
```
   
In diesem Beispiel wird ermöglicht Mitgliedern der OneDrive eDiscovery-Manager benutzerdefinierte Rollengruppe nur die Suche nach Inhalten in OneDrive for Business-Standorte in der Organisation.

```
New-ComplianceSecurityFilter -FilterName OneDriveOnly  -Users "OneDrive eDiscovery Managers" -Filters "Site_Path -like 'https://contoso-my.sharepoint.com/personal*'" -Action Search
```
   
> [!NOTE]
> Um auf bestimmte Websites suchen Benutzer beschränken möchten, verwenden Sie den Filter `Site_Path`, wie im vorherigen Beispiel gezeigt. Mit `Site_Site` funktionieren nicht. 
  
In diesem Beispiel kann der Benutzer Inhaltssuchvorgänge nur für E-Mail-Nachrichten durchführen, die während des Kalenderjahres 2015 gesendet wurden.

```
New-ComplianceSecurityFilter -FilterName EmailDateRestrictionFilter -Users donh@contoso.com -Filters "MailboxContent_Received -ge '01-01-2015' -and MailboxContent_Received -le '12-31-2015'" -Action All
```
   
Ähnlich wie im vorherigen Beispiel kann der Benutzer in diesem Beispiel die Inhaltssuchvorgänge nur für Dokumente durchführen, die zuletzt im Kalenderjahr 2015 geändert wurden.

```
New-ComplianceSecurityFilter -FilterName DocumentDateRestrictionFilter -Users donh@contoso.com -Filters "SiteContent_LastModifiedTime -ge '01-01-2015' -and SiteContent_LastModifiedTime -le '12-31-2015'" -Action All
```
   
In diesem Beispiel wird verhindert, dass Mitglieder der Rollengruppe "OneDrive-Discovery-Managern" Inhaltssuche Aktionen für jedes Postfach in der Organisation ausgeführt. 

```
New-ComplianceSecurityFilter -FilterName NoEXO -Users "OneDrive Discovery Managers" -Filters "Mailbox_Alias -notlike '*'"  -Action All
```
  
## <a name="get-compliancesecurityfilter"></a>Get-ComplianceSecurityFilter

Das **Get-ComplianceSecurityFilter** wird verwendet, um eine Liste der Berechtigungen Suchfilter zurückzugeben. Verwenden Sie den _FilterName_ -Parameter, um Informationen für einen bestimmten Suchfilter zurückzugeben. 
  
## <a name="set-compliancesecurityfilter"></a>Set-ComplianceSecurityFilter

Das **Set-ComplianceSecurityFilter** wird verwendet, um einen vorhandenen Suchfilter Berechtigungen ändern. Der einzige erforderliche Parameter ist _FilterName_. 
  
|**Parameter**|**Beschreibung**|
|:-----|:-----|
| _Aktion_| _Der Aktionsparameter_ gibt diese Art von Search-Aktion, die auf der Filter angewendet wird. Die möglichen Inhaltssuche Aktionen sind:<br/><br/> **Export** - Filter wird beim Exportieren von Suchergebnissen angewendet.  <br/> **Preview** - Filter wird angewendet, beim Anzeigen der Vorschau der Suchergebnisse.  <br/> **Bereinigen** - Filter wird angewendet, wenn Suchergebnisse zu löschen.  <br/> **Suche** – der Filter wird angewendet, wenn eine Suche ausgeführt.  <br/> **Alle** - der Filter wird auf alle Suche Aktionen angewendet.  <br/> |
| _FilterName_|Der _FilterName_ -Parameter gibt den Namen des Filters Berechtigungen. |
| _Filter_| Der _Filter_ -Parameter gibt die Suchkriterien für die Einhaltung von Bestimmungen Sicherheitsfilter. Sie können zwei unterschiedliche Art der Filter erstellen:<br/><br/>**Filtern von Postfach** - diese Art von Filter gibt an, die Postfächer, die die zugewiesene Benutzer (durch den _Benutzer_ -Parameter angegebenen) durchsuchen können. Die Syntax für diese Art von Filter ist **Mailbox_** _MailboxPropertyName_, dabei _MailboxPropertyName_ an ein Postfach-Eigenschaft verwendet, um die Postfächer zu begrenzen, die durchsucht werden können. Beispielsweise das Postfach Filter `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` würde ermöglicht dem Benutzer zugewiesen dieser Filter nur Postfächer suchen mit dem Wert "OttawaUsers" in die CustomAttribute10-Eigenschaft.  Für die _MailboxPropertyName_ -Eigenschaft kann eine beliebige unterstützte filterbare Empfänger-Eigenschaft verwendet werden. Eine Liste der unterstützten Eigenschaften finden Sie unter [filterbaren Eigenschaften für den Parameter RecipientFilter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/>**Filtern von Inhalt von Postfächern**- diese Art von Filter wird auf den Inhalt angewendet, die durchsucht werden können. Es gibt den Inhalt von Postfächern, die, dem für die zugewiesene Benutzer durchsuchen können. Die Syntax für diese Art von Filter ist **MailboxContent_** _SearchablePropertyName:value_, wobei _SearchablePropertyName_ ein Schlüsselwort Query Language (KQL)-Eigenschaft gibt an, die in einer Inhaltssuche angegeben werden können. Beispielsweise das Postfach Inhaltsfilter `MailboxContent_recipients:contoso.com` ermöglicht dem Benutzer zugewiesen dieser Filter nur die Suche nach Nachrichten, die an Empfänger in der Domäne "contoso.com" gesendet.  Eine Liste mit Nachrichteneigenschaften durchsucht werden finden Sie unter [Stichwortabfragen Content-Suche](keyword-queries-and-search-conditions.md).<br/><br/>**Filtern von Website und Websiteinhalte** Es gibt zwei SharePoint und OneDrive for Business Website bezogenen Filter, die Sie verwenden können, um anzugeben, welche Website oder von Websiteinhalt zugewiesene Benutzer suchen können: <br/><br/>- **Site_** *SearchableSiteProperty* <br/>- **SiteContent**_*SearchableSiteProperty*<br/><br/>Diese beiden Filter sind austauschbar. beispielsweise `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` und `"SiteContent_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` die gleichen Ergebnisse zurückgegeben werden. Zur einfacheren Funktionsweise ein Filters zu identifizieren, Sie können jedoch `Site_` Website bezogenen-Eigenschaften (wie eine Website-URL) angeben und `SiteContent_` an Content-bezogene-Eigenschaften (wie Dokumenttypen. Beispielsweise den Filter `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` ermöglicht dem Benutzer zugewiesen dieser Filter nur die Suche nach Inhalten in der https://contoso.spoppe.com/sites/doctors Websitesammlung festlegen. Der Filter `"SiteContent_FileExtension -eq 'docx'"` ermöglicht dem Benutzer zugewiesen dieser Filter nur für Word-Dokumente (Word 2007 und später) suchen.<br/><br/>Eine Liste der Eigenschaften von durchsuchbaren finden Sie unter [Übersicht über durchforstete und verwaltete Eigenschaften in SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Eigenschaften, mit **Ja** in der Spalte **Einstellung "Queryable"** markiert können zum Erstellen einer Website oder Inhaltsfilter Website verwendet werden.<br/><br/> **Wichtig:** Ein einzelnes Suchfilter kann nur einen Typ des Filters vorhanden sein. Es ist nicht möglich eine Postfach-Filter und einen Filter für die Website enthalten. Es kann nicht auf ähnliche Weise einen Postfach-Filter und Postfach Inhaltsfilter enthalten. Ein Filter kann jedoch eine komplexere Abfrage des gleichen Typs enthalten. Zum Beispiel`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"`          |
| _Benutzer_|Der _Benutzer_ -Parameter gibt die Benutzer, die dieser Filter angewendet, deren Content-Suche zu erhalten. Da es sich um eine mehrwertige Eigenschaft handelt, wird die vorhandene Liste von Benutzern angeben einen Benutzer oder eine Gruppe von Benutzern mit dieser Parameter überschrieben werden. Siehe die folgenden Beispiele für die Syntax für das Hinzufügen und Entfernen von ausgewählten Benutzern.<br/><br/>Sie können auch den _Benutzer_ -Parameter zum Angeben eines Wertpapiers &amp; Compliance Center Rollengruppe. Hiermit können Sie eine benutzerdefinierte Rollengruppe zu erstellen, und weisen Sie diese Rolle gruppieren Berechtigungen Suchfilter Nehmen wir beispielsweise an, dass Sie eine benutzerdefinierte Rollengruppe für eDiscovery-Manager für die USA Niederlassung von einem multinationale Unternehmen verfügen. Den Parameter _Benutzer_ können Sie dieser Rollengruppe (mithilfe der Name-Eigenschaft der Rollengruppe) angeben, und klicken Sie dann die Parameter " _Filter_ " verwenden, um nur die Postfächer in den USA zu durchsuchenden erlauben.<br/><br/>Sie können mit diesem Parameter keine Verteilergruppen angeben. |

## <a name="examples-of-changing-search-permissions-filters"></a>Beispiele zum Ändern der Berechtigungen Suchfilter

Diese Beispiele zeigen, wie Sie die Cmdlets **Get-ComplianceSecurityFilter** und **Set-ComplianceSecurityFilter** zum Hinzufügen oder Entfernen eines Benutzers der vorhandenen Liste von Benutzern, denen der Filter zugeordnet ist. Wenn Sie hinzufügen oder Entfernen von Benutzern aus einen Filter, geben Sie den Benutzer mithilfe der SMTP-Adresse. 
  
In diesem Beispiel wird dem Filter ein Benutzer hinzugefügt.

```
$filterusers = Get-ComplianceSecurityFilter -FilterName OttawaUsersFilter
```
```
$filterusers.users.add("pilarp@contoso.com")
```

```
Set-ComplianceSecurityFilter -FilterName OttawaUsersFilter -Users $filterusers.users
```
   
In diesem Beispiel wird ein Benutzer aus dem Filter entfernt.

```
$filterusers = Get-ComplianceSecurityFilter -FilterName OttawaUsersFilter
```

```
$filterusers.users.remove("annb@contoso.com")
```

```
Set-ComplianceSecurityFilter -FilterName OttawaUsersFilter -Users $filterusers.users
```
  
## <a name="remove-compliancesecurityfilter"></a>Remove-ComplianceSecurityFilter

Die **Remove-ComplianceSecurityFilter** wird verwendet, um ein Suchfilter zu löschen. Verwenden Sie den _FilterName_ -Parameter zum Angeben des Filters, den Sie löschen möchten. 
  
## <a name="more-information"></a>Weitere Informationen

- **Wie führt Suche filtern Arbeit Berechtigungen?** Der Filter Berechtigungen wird zur Suchabfrage hinzugefügt, wenn eine Inhaltssuche ausgeführt wird. Der Filter Berechtigungen ist im Wesentlichen mit der Suchabfrage mithilfe des booleschen Operators **AND** verbunden. Angenommen Sie, dass Sie einen Filter Berechtigungen verfügen, mit der Eintrag Bob, um alle Aktionen für Suchen auf die Postfächer der Mitglieder der Verteilergruppe Mitarbeiter ausführen können. Dann Bob ein Inhaltssuche auf alle Postfächer in der Organisation mit der Suchabfrage ausgeführt wird `sender:jerry@adatum.com`. Da der Filter Berechtigungen und der Suchabfrage durch eine **AND** -Operator logisch kombiniert werden, wird die Suche alle durch jerry@adatum.com an jedes Mitglied der Verteilergruppe Mitarbeiter gesendeten Nachrichten zurück. 
    
- **Was passiert, wenn Sie mehrere Suchfilter Berechtigungen haben?** Mehrere Berechtigungen Filter werden in einer Abfrage Inhaltssuche durch **oder** boolesche Operatoren kombiniert. So werden Ergebnisse zurückgegeben werden, wenn alle Filter true sind. In einer Inhaltssuche werden alle Filter (durch **oder** -Operatoren kombiniert) klicken Sie dann mit der Suchabfrage mit dem **AND** -Operator kombiniert werden. Sehen wir uns im vorherige Beispiel, in dem ein Suchfilter Bob, um nur die Postfächer der Mitglieder der Verteilergruppe Mitarbeiter suchen kann. Klicken Sie dann erstellen wir einen weiteren Filter, die verhindert, dass Bob Phils Postfach ("Mailbox_Alias - Ne 'Phil'") suchen. Und angenommen, dass Phil Mitglied der Gruppe der Mitarbeiter ist auch. Wenn Bob auf alle Postfächer in der Organisation eine Inhaltssuche (aus dem vorherigen Beispiel) ausgeführt wird, werden der Suchergebnisse, obwohl Sie Filter, um zu verhindern, dass Bob Suche Phils Postfach angewendet für das Postfach von Phils zurückgegeben. Dies ist, da der erste Filter, der wodurch Bob, um der Gruppe Mitarbeiter zu suchen, auf true festgelegt ist. Und da Phil ein Mitglied der Gruppe der Mitarbeiter ist, kann Bob Phils Postfach suchen. 
    
- **Führt Suche Berechtigungen filtern Aufwand für inaktive Postfächer?** Ja, können Sie Postfach- und Inhaltsfilter Postfach um zu begrenzen, die inaktiver Postfächer in Ihrer Organisation durchsuchen können. Wie ein normales Postfach muss ein inaktives Postfachs mit der Empfänger-Eigenschaft konfiguriert werden, die zum Erstellen eines Filters Berechtigungen verwendet wird. Falls erforderlich, können Sie den Befehl **Get-Mailbox-InactiveMailboxOnly** verwenden, um die Eigenschaften des inaktiver Postfächer anzuzeigen. Weitere Informationen finden Sie unter [Erstellen und Verwalten inaktiver Postfächer in Office 365](create-and-manage-inactive-mailboxes.md).
    
- **Führt Suche Berechtigungen filtern Arbeit für Öffentliche Ordner?** Nein. Wie bereits erklärt, Suche, die Filterung Berechtigungen verwendet werden können, zu beschränken, die Öffentliche Ordner im Exchange suchen kann. Beispielsweise können nicht Elemente in öffentlichen Ordnern von einem Filter Berechtigungen aus den Suchergebnissen ausgeschlossen werden. 
    
- **Verhindert durch Benutzer alle Speicherorte für Inhalte in einem bestimmten Dienst suchen auch, dass diese Speicherorte für Inhalte in einem anderen Dienst suchen?** Nein. Wie bereits erklärt müssen Sie explizit hindern Speicherorte für Inhalte in einem bestimmten Office 365-Dienst (beispielsweise verhindern, dass einen Benutzer alle Exchange-Postfach oder einer beliebigen SharePoint-Website suchen) suchen Suchfilter Berechtigungen zu erstellen. Anders ausgedrückt, keinen Suchfilter für Berechtigungen, der einem Benutzer ermöglicht, suchen Sie alle SharePoint-Websites in der Organisation erstellen gehindert, Postfächer zu suchen. Damit können SharePoint-Administratoren nur SharePoint-Websites suchen, müssen Sie beispielsweise einen Filter erstellen, der verhindert, dass sie Postfächer zu suchen. Damit Exchange-Administratoren Postfächer nur suchen können, müssen Sie auf ähnliche Weise einen Filter erstellen, der verhindert, dass diese Websites suchen.
