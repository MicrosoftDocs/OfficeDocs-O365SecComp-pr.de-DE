---
title: Konfigurieren der Berechtigungsfilterung für die Compliancesuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/14/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1adffc35-38e5-4f7d-8495-8e0e8721f377
description: Verwenden Sie Filter für die Inhaltssuche, damit ein eDiscovery-Manager nur eine Teilmenge von Postfächern und Websites in Ihrer Office 365-Organisation durchsuchen kann.
ms.openlocfilehash: ddf474dca814a8e4dc2c8a374b8d74a17d583d27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214645"
---
# <a name="configure-permissions-filtering-for-content-search"></a>Konfigurieren der Berechtigungsfilterung für die Compliancesuche

Sie können die Filterung von Suchberechtigungen verwenden, um einem eDiscovery-Manager nur eine Teilmenge von Postfächern und Websites in Ihrer Office 365-Organisation durchsuchen zu lassen. Sie können auch die Filterung von Berechtigungen verwenden, damit derselbe eDiscovery-Manager nur nach Post Fach-oder Websiteinhalten sucht, die einem bestimmten Suchkriterium entsprechen. Sie können beispielsweise einem eDiscovery-Manager die Suche nach den Postfächern von Benutzern an einem bestimmten Standort oder in einer Abteilung ermöglichen. Hierzu erstellen Sie einen Filter, der einen unterstützten Empfängerfilter verwendet, um zu begrenzen, welche Postfächer durchsucht werden können. Sie können auch einen Filter erstellen, der angibt, welche Postfachinhalte durchsucht werden können. Hierzu erstellen Sie einen Filter, der eine durchsuchbare Nachrichteneigenschaft verwendet. Auf ähnliche Weise können Sie einen eDiscovery-Manager nur bestimmte SharePoint-Websites in Ihrer Organisation durchsuchen lassen. Hierzu erstellen Sie einen Filter, der die Durchsuchung der Website beschränkt. Sie können auch einen Filter erstellen, der angibt, welche Websiteinhalte durchsucht werden können. Hierzu erstellen Sie einen Filter, der eine durchsuchbare Site-Eigenschaft verwendet.

Sie können auch die Filterung von Suchberechtigungen verwenden, um logische Grenzen (sogenannte *Compliance-Grenzen*) innerhalb einer Office 365-Organisation zu erstellen, die die Benutzerinhalts Speicherorte (wie Postfächer, SharePoint-Websites und OneDrive-Konten) steuern, die bestimmte eDiscovery-Manager können suchen. Weitere Informationen finden Sie unter [Einrichten von Konformitäts Grenzen für eDiscovery-Untersuchungen in Office 365](set-up-compliance-boundaries.md).
  
Die Filterung von Suchberechtigungen wird von der Inhaltssuche im Office 365 Security &amp; Compliance Center unterstützt. Mit diesen vier Cmdlets können Sie Such permisisons-Filter konfigurieren und verwalten:
  
[New-ComplianceSecurityFilter](#new-compliancesecurityfilter)

[Get-ComplianceSecurityFilter](#get-compliancesecurityfilter)

[Set-ComplianceSecurityFilter](#set-compliancesecurityfilter)

[Remove-ComplianceSecurityFilter](#remove-compliancesecurityfilter)

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um die Compliance-Sicherheitsfilter-Cmdlets auszuführen, müssen Sie Mitglied der Rollengruppe "Organisationsverwaltung" im Security &amp; Compliance Center sein. Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
- Sie müssen Windows PowerShell sowohl mit dem Security &amp; Compliance Center als auch mit Ihrer Exchange Online-Organisation verbinden, um die Compliance-Sicherheitsfilter-Cmdlets zu verwenden. Dies ist erforderlich, da diese Cmdlets Zugriff auf Postfacheigenschaften benötigen, weshalb Sie eine Verbindung mit Exchange Online herstellen müssen. Lesen Sie die Schritte im nächsten Abschnitt. 
    
- Weitere Informationen über Berechtigungsfilter für die Suche finden Sie im Abschnitt [More information](#more-information). 
    
- Die Filterung von Suchberechtigungen gilt für inaktive Postfächer, was bedeutet, dass Sie die Post Fach-und Postfachinhalts Filterung verwenden können, um die Suche nach einem inaktiven Postfach zu begrenzen. Weitere Informationen zur Berechtigungs Filterung und zu inaktiven Postfächern finden Sie im Abschnitt [Weitere Informationen](#more-information) . 
    
-  Die Filterung von Suchberechtigungen kann nicht verwendet werden, um zu begrenzen, wer öffentliche Ordner in Exchange durchsuchen kann. 
    
- Es gibt keine Begrenzung für die Anzahl der Filter für Suchberechtigungen, die in einer Organisation erstellt werden können. Die Suchleistung wirkt sich jedoch auf mehr als 100 Such Berechtigungsfilter aus. Um die Anzahl von Such Berechtigungs Filtern in Ihrer Organisation so klein wie möglich zu halten, erstellen Sie Filter, mit denen Regeln für Exchange, SharePoint und OneDrive in einem einzigen Filter kombiniert werden können.
    
## <a name="connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Herstellen einer Verbindung mit &amp; dem Security Compliance Center und Exchange Online in einer einzigen Remote-PowerShell-Sitzung

1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Sie können Sie beispielsweise in einer Datei mit dem Namen ConnectEXO-CC. ps1 speichern.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem sich das Skript befindet, das Sie im vorherigen Schritt erstellt haben, und führen Sie das Skript aus. Zum Beispiel:
    
    ```
    .\ConnectEXO-CC.ps1
    ```
 
Woher wissen Sie, ob dies funktioniert hat? Nachdem Sie das Skript ausgeführt haben, werden Cmdlets vom &amp; Security Compliance Center und von Exchange Online in Ihre lokale Windows PowerShell-Sitzung importiert. Wenn Sie keine Fehler erhalten, haben Sie erfolgreich eine Verbindung hergestellt. Ein kurzer Test ist die Ausführung eines Security &amp; Compliance Center-Cmdlets (beispielsweise **install-UnifiedCompliancePrerequisite** ) und eines Exchange Online-Cmdlets wie **Get-Mailbox**. 
  
Wenn Sie Fehlermeldungen erhalten, überprüfen Sie die folgenden Anforderungen:
  
- Ein häufig auftretendes Problem ist ein falsches Kennwort. Führen Sie die beiden Schritte erneut durch, und achten Sie besonders auf die korrekte Eingabe des Benutzernamens und Kennworts in Schritt 1.
    
- Stellen Sie sicher, dass Ihr Konto über die Berechtigung &amp; für den Zugriff auf das Security Compliance Center verfügt. Weitere Informationen finden Sie unter [Gewähren von Benutzern Zugriff auf &amp; das Security Compliance Center](grant-access-to-the-security-and-compliance-center.md).
    
- Um die Abwehr von DoS-Angriffen (Denial of Service) zu unterstützen, sind Sie auf drei offene Remote- &amp; PowerShell-Verbindungen mit dem Security Compliance Center beschränkt.
    
- Windows PowerShell muss zum Ausführen von Skripts konfiguriert werden. Sie müssen diese Einstellung nur einmalig auf Ihrem Computer konfigurieren, und nicht bei jedem Verbindungsaufbau. Um Windows PowerShell für das Ausführen von signierten Skripts zu aktivieren, müssen Sie den folgenden Befehl in einem Windows PowerShell-Fenster mit erhöhten Rechten ausführen (ein Windows PowerShell-Fenster, das Sie durch Auswahl von **Als Administrator ausführen**) geöffnet haben.

    ```
    Set-ExecutionPolicy RemoteSigned
    ```
- TCP-Portierung 80 Datenverkehr muss zwischen Ihrem lokalen Computer und Office 365 geöffnet sein. Es ist wahrscheinlich geöffnet, aber es ist etwas zu berücksichtigen, wenn Ihre Organisation eine restriktive Richtlinie für den Internet Zugriff hat.
    

  
## <a name="new-compliancesecurityfilter"></a>New-ComplianceSecurityFilter
<a name="New"> </a>

Der **New-ComplianceSecurityFilter** wird zum Erstellen eines neuen Such Berechtigungs Filters verwendet. In der folgenden Tabelle werden die Parameter für dieses Cmdlet beschrieben. Alle Parameter sind erforderlich, um einen Compliance-Sicherheitsfilter zu erstellen. 
  
|**Parameter**|**Beschreibung**|
|:-----|:-----|
| _Aktion_ <br/> | Der Parameter _Action_ gibt den Typ der Suchaktion an, auf die der Filter angewendet wird. Die möglichen Inhalts Suchaktionen sind:<br/><br/> **Export** – der Filter wird beim Exportieren von Suchergebnissen angewendet.  <br/> **Preview** – der Filter wird beim Anzeigen der Vorschau der Suchergebnisse angewendet.  <br/> **Purge** – der Filter wird beim Löschen von Suchergebnissen angewendet.  <br/> **Suche** : der Filter wird beim Durchführen einer Suche angewendet.  <br/> **All** – der Filter wird auf alle Suchaktionen angewendet.  <br/> |
| _FilterName_ <br/> |Der __ Parameter Filtername gibt den Namen des Berechtigungs Filters an. Dieser Name wird verwendet, um einen Filter zu identifizieren, wenn Sie die Cmdlets **Get-ComplianceSecurityFilter**, **Set-ComplianceSecurityFilter** und **Remove-ComplianceSecurityFilter** verwenden.<br/> |
| _Filter_ <br/> | Der Parameter _Filters_ gibt die Suchkriterien für den Compliance-Sicherheitsfilter an. Sie können drei verschiedene Arten von Filtern erstellen:<br/><br/> **Post Fach Filterung** -dieser Filtertyp gibt die Postfächer an, die von den zugewiesenen Benutzern (durch den Parameter _Users_ angegeben) durchsucht werden können. Die Syntax für diesen Filtertyp ist **Mailbox_** _MailboxPropertyName_, wobei _MailboxPropertyName_ eine Postfacheigenschaft angibt, die zum Bereich der zu durchsuchenden Postfächer verwendet wird. Mit dem Post Fach Filter `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` kann der Benutzer beispielsweise nur nach Postfächern mit dem Wert "OttawaUsers" in der CustomAttribute10-Eigenschaft suchen.<br/>  Alle unterstützten filterbaren Empfänger Eigenschaften können für die _MailboxPropertyName_ -Eigenschaft verwendet werden. Eine Liste der unterstützten Eigenschaften finden Sie unter [Filterable Properties for the-RecipientFilter Parameter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/> **Filtern von Postfachinhalten** -dieser Filtertyp wird auf den Inhalt angewendet, der durchsucht werden kann. Es gibt den Postfachinhalt an, nach dem die zugeordneten Benutzer suchen können. Die Syntax für diesen Filtertyp lautet **MailboxContent_** _SearchablePropertyName: Value_, wobei _SearchablePropertyName_ eine KQL-Eigenschaft (Keyword Query Language) angibt, die in einer Inhaltssuche angegeben werden kann. Der Postfachinhalts Filter `MailboxContent_recipients:contoso.com` kann beispielsweise dem Benutzer, der diesen Filter zugewiesen hat, nur nach Nachrichten suchen, die an Empfänger in der contoso.com-Domäne gesendet wurden.<br/>  Eine Liste der durchsuchbaren Nachrichteneigenschaften finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).  <br/><br/> **Website-und Websiteinhalts Filterung** – es gibt zwei SharePoint-und OneDrive für die Website bezogene Filter, die Sie verwenden können, um anzugeben, welche Website-oder Websiteinhalte den zugewiesenen Benutzern durchsucht werden können:  <br/><br/> - **Site_** _SearchableSiteProperty_ <br/> - **SiteContent_** _SearchableSiteProperty_ <br/><br/>  Diese beiden Filter sind austauschbar; zum Beispiel `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` `"SiteContent_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` werden die gleichen Ergebnisse zurückgegeben. Sie können jedoch auch die Verwendung `Site_` von Website bezogenen Eigenschaften (wie eine Website-URL) und `SiteContent_` das Angeben von inhaltsbezogenen Eigenschaften (beispielsweise Dokumenttypen) zur Identifizierung eines Filters unterstützen. Beispielsweise `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` kann der Benutzer mit diesem Filter nur nach Inhalten in der https://contoso.sharepoint.com/sites/doctors Websitesammlung suchen. Mit dem `"SiteContent_FileExtension -eq 'docx'"` Filter kann der Benutzer diesen Filter nur nach Word-Dokumenten (Word 2007 und höher) suchen.<br/><br/>  Eine Liste der durchsuchbaren Websiteeigenschaften finden Sie unter Übersicht über durch [forstete und verwaltete Eigenschaften in SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Eigenschaften, die mit einem **Ja** in der * * Queryable * *-Spalte gekennzeichnet sind, können zum Erstellen eines Website-oder Websiteinhalts Filters verwendet werden.<br/> <br/> **Wichtig:**  Ein einzelner Suchfilter kann nur einen Filtertyp aufweisen. Sie kann keinen Post Fach Filter und keinen Website Filter enthalten. entsprechend kann es keinen Post Fach Filter und einen Postfachinhalts Filter enthalten. Ein Filter kann jedoch eine komplexere Abfrage desselben Typs enthalten. Zum Beispiel`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"` <br/><br/> **Wichtig:** Sie müssen einen Filter für Suchberechtigungen erstellen, um zu verhindern, dass Benutzerinhalts Speicherorte in einem bestimmten Office 365-Dienst durchsuchen (beispielsweise verhindern, dass ein Benutzer ein Exchange-Postfach oder eine SharePoint-Website durchsucht). Anders ausgedrückt: durch das Erstellen eines Filters für Suchberechtigungen, mit dem ein Benutzer alle SharePoint-Websites in der Organisation durchsuchen kann, wird nicht verhindert, dass der Benutzer Postfächer durchsucht. Um beispielsweise SharePoint-Administratoren nur das Durchsuchen von SharePoint-Websites zu gestatten, müssen Sie einen Filter erstellen, der das Durchsuchen von Postfächern verhindert. Um Exchange-Administratoren nur das Durchsuchen von Postfächern zu gestatten, müssen Sie einen Filter erstellen, der die Suche nach Websites verhindert.           |
| _Benutzer_ <br/> |Der Parameter _Users_ gibt die Benutzer an, die diesen Filter auf Ihre Inhaltssuche anwenden. Identifizieren Sie Benutzer anhand Ihres Alias oder ihrer primären SMTP-Adresse. Sie können mehrere Werte durch Kommata getrennt angeben, oder Sie können den Filter allen Benutzern zuweisen, indem Sie den Wert **all**verwenden.<br/> Sie können auch den Parameter _Users_ verwenden, um eine Sicherheits &amp; Kompatibilitäts Center-Rollengruppe anzugeben. Auf diese Weise können Sie eine benutzerdefinierte Rollengruppe erstellen und dieser Rollengruppe dann einen Such Berechtigungsfilter zuweisen. Angenommen, Sie verfügen über eine benutzerdefinierte Rollengruppe für eDiscovery-Manager für die U.S.-Tochter eines multinationalen Unternehmens. Sie können den Parameter _Users_ verwenden, um diese Rollengruppe (mithilfe der Name-Eigenschaft der Rollengruppe) anzugeben, und dann den Parameter _Filter_ verwenden, um zuzulassen, dass nur Postfächer in den USA durchsucht werden.<br/> Sie können mit diesem Parameter keine Verteilergruppen angeben.  <br/> |
   

## <a name="examples-of-creating-search-permissions-filters"></a>Beispiele für das Erstellen von Such Berechtigungs Filtern

Nachfolgend finden Sie Beispiele für die Verwendung des **New-ComplianceSecurityFilter**-Cmdlets zum Erstellen eines Berechtigungsfilters für die Suche. 
  
In diesem Beispiel kann der Benutzer annb@contoso.com alle Aktionen für die Inhaltssuche nur für Postfächer in Kanada durchführen. Dieser Filter enthält den dreistelligen Ländercode für Kanada ab ISO 3166-1.

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
   
In diesem Beispiel können Mitglieder der benutzerdefinierten Rollengruppe "OneDrive eDiscovery Managers" nur nach Inhalten in OneDrive für Geschäftsstandorte in der Organisation suchen.

```
New-ComplianceSecurityFilter -FilterName OneDriveOnly  -Users "OneDrive eDiscovery Managers" -Filters "Site_Path -like 'https://contoso-my.sharepoint.com/personal*'" -Action Search
```
   
> [!NOTE]
> Um Benutzer auf die Suche nach bestimmten Websites zu beschränken, `Site_Path`verwenden Sie den Filter, wie im vorherigen Beispiel gezeigt. Die `Site_Site` Verwendung von funktioniert nicht. 
  
In diesem Beispiel kann der Benutzer Inhaltssuchvorgänge nur für E-Mail-Nachrichten durchführen, die während des Kalenderjahres 2015 gesendet wurden.

```
New-ComplianceSecurityFilter -FilterName EmailDateRestrictionFilter -Users donh@contoso.com -Filters "MailboxContent_Received -ge '01-01-2015' -and MailboxContent_Received -le '12-31-2015'" -Action All
```
   
Ähnlich wie im vorherigen Beispiel kann der Benutzer in diesem Beispiel die Inhaltssuchvorgänge nur für Dokumente durchführen, die zuletzt im Kalenderjahr 2015 geändert wurden.

```
New-ComplianceSecurityFilter -FilterName DocumentDateRestrictionFilter -Users donh@contoso.com -Filters "SiteContent_LastModifiedTime -ge '01-01-2015' -and SiteContent_LastModifiedTime -le '12-31-2015'" -Action All
```
   
In diesem Beispiel wird verhindert, dass Mitglieder der Rollengruppe "OneDrive Discovery Managers" Inhalts Suchaktionen für ein Postfach in der Organisation ausführen. 

```
New-ComplianceSecurityFilter -FilterName NoEXO -Users "OneDrive Discovery Managers" -Filters "Mailbox_Alias -notlike '*'"  -Action All
```
  
## <a name="get-compliancesecurityfilter"></a>Get-ComplianceSecurityFilter

Der **Get-ComplianceSecurityFilter** wird verwendet, um eine Liste der Filter für Suchberechtigungen zurückzugeben. Verwenden Sie den _Filter_ Name-Parameter, um Informationen für einen bestimmten Suchfilter zurückzugeben. 
  
## <a name="set-compliancesecurityfilter"></a>Set-ComplianceSecurityFilter

Die **Set-ComplianceSecurityFilter** wird zum Ändern eines vorhandenen Such Berechtigungs Filters verwendet. Der einzige erforderliche Parameter ist _Filtername_. 
  
|**Parameter**|**Beschreibung**|
|:-----|:-----|
| _Aktion_| Der Parameter _Action_ gibt den Typ der Suchaktion an, auf die der Filter angewendet wird. Die möglichen Inhalts Suchaktionen sind:<br/><br/> **Export** – der Filter wird beim Exportieren von Suchergebnissen angewendet.  <br/> **Preview** – der Filter wird beim Anzeigen der Vorschau der Suchergebnisse angewendet.  <br/> **Purge** – der Filter wird beim Löschen von Suchergebnissen angewendet.  <br/> **Suche** : der Filter wird beim Durchführen einer Suche angewendet.  <br/> **All** – der Filter wird auf alle Suchaktionen angewendet.  <br/> |
| _FilterName_|Der __ Parameter Filtername gibt den Namen des Berechtigungs Filters an. |
| _Filter_| Der Parameter _Filters_ gibt die Suchkriterien für den Compliance-Sicherheitsfilter an. Sie können zwei verschiedene Arten von Filtern erstellen:<br/><br/>**Post Fach Filterung** -dieser Filtertyp gibt die Postfächer an, die von den zugewiesenen Benutzern (durch den Parameter _Users_ angegeben) durchsucht werden können. Die Syntax für diesen Filtertyp ist **Mailbox_** _MailboxPropertyName_, wobei _MailboxPropertyName_ eine Postfacheigenschaft angibt, die zum Bereich der zu durchsuchenden Postfächer verwendet wird. Mit dem Post Fach Filter `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` kann der Benutzer beispielsweise nur nach Postfächern mit dem Wert "OttawaUsers" in der CustomAttribute10-Eigenschaft suchen.  Alle unterstützten filterbaren Empfänger Eigenschaften können für die _MailboxPropertyName_ -Eigenschaft verwendet werden. Eine Liste der unterstützten Eigenschaften finden Sie unter [Filterable Properties for the-RecipientFilter Parameter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/>**Filtern von Postfachinhalten**-dieser Filtertyp wird auf den Inhalt angewendet, der durchsucht werden kann. Es gibt den Postfachinhalt an, nach dem die zugeordneten Benutzer suchen können. Die Syntax für diesen Filtertyp lautet **MailboxContent_** _SearchablePropertyName: Value_, wobei _SearchablePropertyName_ eine KQL-Eigenschaft (Keyword Query Language) angibt, die in einer Inhaltssuche angegeben werden kann. Der Postfachinhalts Filter `MailboxContent_recipients:contoso.com` kann beispielsweise dem Benutzer, der diesen Filter zugewiesen hat, nur nach Nachrichten suchen, die an Empfänger in der contoso.com-Domäne gesendet wurden.  Eine Liste der durchsuchbaren Nachrichteneigenschaften finden Sie unter [Stichwortabfragen für die Inhaltssuche](keyword-queries-and-search-conditions.md).<br/><br/>**Filtern von Website-und Websiteinhalten** Es gibt zwei SharePoint-und OneDrive für Unternehmen-Filter, die Sie verwenden können, um anzugeben, welche Website-oder Websiteinhalte den zugewiesenen Benutzern durchsucht werden können: <br/><br/>- **Site_** *SearchableSiteProperty* <br/>- **SiteContent**_*SearchableSiteProperty*<br/><br/>Diese beiden Filter sind austauschbar; zum Beispiel `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` `"SiteContent_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` werden die gleichen Ergebnisse zurückgegeben. Sie können jedoch auch die Verwendung `Site_` von Website bezogenen Eigenschaften (wie eine Website-URL) und `SiteContent_` das Angeben von inhaltsbezogenen Eigenschaften (beispielsweise Dokumenttypen) zur Identifizierung eines Filters unterstützen. Beispielsweise `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` kann der Benutzer mit diesem Filter nur nach Inhalten in der https://contoso.spoppe.com/sites/doctors Websitesammlung suchen. Mit dem `"SiteContent_FileExtension -eq 'docx'"` Filter kann der Benutzer diesen Filter nur nach Word-Dokumenten (Word 2007 und höher) suchen.<br/><br/>Eine Liste der durchsuchbaren Websiteeigenschaften finden Sie unter Übersicht über durch [forstete und verwaltete Eigenschaften in SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Eigenschaften, die mit einem **Ja** in der Spalte **Queryable** markiert sind, können zum Erstellen eines Website-oder Websiteinhalts Filters verwendet werden.<br/><br/> **Wichtig:** Ein einzelner Suchfilter kann nur einen Filtertyp aufweisen. Sie kann keinen Post Fach Filter und keinen Website Filter enthalten. entsprechend kann es keinen Post Fach Filter und einen Postfachinhalts Filter enthalten. Ein Filter kann jedoch eine komplexere Abfrage desselben Typs enthalten. Zum Beispiel`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"`          |
| _Benutzer_|Der Parameter _Users_ gibt die Benutzer an, die diesen Filter auf Ihre Inhaltssuche anwenden. Da es sich um eine mehrwertige Eigenschaft handelt, wird die vorhandene Benutzerliste überschrieben, wenn ein Benutzer oder eine Gruppe von Benutzern mit diesem Parameter angegeben wird. Die folgenden Beispiele zeigen die Syntax zum Hinzufügen und Entfernen ausgewählter Benutzer.<br/><br/>Sie können auch den Parameter _Users_ verwenden, um eine Sicherheits &amp; Kompatibilitäts Center-Rollengruppe anzugeben. Auf diese Weise können Sie eine benutzerdefinierte Rollengruppe erstellen und dieser Rollengruppe dann einen Such Berechtigungsfilter zuweisen. Angenommen, Sie verfügen über eine benutzerdefinierte Rollengruppe für eDiscovery-Manager für die U.S.-Tochter eines multinationalen Unternehmens. Sie können den Parameter _Users_ verwenden, um diese Rollengruppe (mithilfe der Name-Eigenschaft der Rollengruppe) anzugeben, und dann den Parameter _Filter_ verwenden, um zuzulassen, dass nur Postfächer in den USA durchsucht werden.<br/><br/>Sie können mit diesem Parameter keine Verteilergruppen angeben. |

## <a name="examples-of-changing-search-permissions-filters"></a>Beispiele für das Ändern von Such Berechtigungs Filtern

In diesen Beispielen wird gezeigt, wie Sie mit den Cmdlets **Get-ComplianceSecurityFilter** und **Set-ComplianceSecurityFilter** einen Benutzer der vorhandenen Liste der Benutzer hinzufügen oder daraus entfernen, denen der Filter zugeordnet ist. Wenn Sie Benutzer zu einem Filter hinzufügen oder daraus entfernen, geben Sie den Benutzer mithilfe der zugehörigen SMTP-Adresse an. 
  
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

Der **Remove-ComplianceSecurityFilter** wird zum Löschen eines Suchfilters verwendet. Verwenden Sie den _Filter_ Name-Parameter, um den Filter anzugeben, den Sie löschen möchten. 
  
## <a name="more-information"></a>Weitere Informationen

- **Wie funktioniert die Filterung von Suchberechtigungen?** Der Berechtigungsfilter wird der Suchabfrage hinzugefügt, wenn eine Inhaltssuche ausgeführt wird. Der Berechtigungsfilter ist im Wesentlichen mit der Suchabfrage vom booleschen **und-** Operator verknüpft. Angenommen, Sie verfügen über einen Berechtigungsfilter, mit dem Bob alle Suchaktionen für die Postfächer der Mitglieder der Verteilergruppe "Worker" ausführen kann. Anschließend führt Bob eine Inhaltssuche für alle Postfächer in der Organisation mit der Such `sender:jerry@adatum.com`Abfrage aus. Da der Berechtigungsfilter und die Suchabfrage logisch durch einen **and-** Operator kombiniert werden, gibt die Suche jede Nachricht zurück, die von Jerry@adatum.com an jedes Mitglied der Verteilergruppe "Workers" gesendet wird. 
    
- **Was geschieht, wenn Sie über mehrere Such Berechtigungsfilter verfügen?** In einer Inhalts Suchabfrage werden mehrere Berechtigungsfilter mit **oder** booleschen Operatoren kombiniert. Ergebnisse werden also zurückgegeben, wenn einer der Filter auf true festgelegt ist. In einer Inhaltssuche werden alle Filter (kombiniert mit **oder** -Operatoren) dann mit der Suchabfrage vom **and-** Operator kombiniert. Im vorherigen Beispiel wird mit einem Suchfilter ermöglicht, dass Bob nur die Postfächer der Mitglieder der Verteilergruppe "Workers" durchsucht. Dann erstellen wir einen weiteren Filter, der verhindert, dass Bob Phils Postfach durchsucht ("Mailbox_Alias-ne" Phil "). Und lassen Sie uns auch davon ausgehen, dass Phil ein Mitglied der Gruppe Arbeiter ist. Wenn Bob eine Inhaltssuche (aus dem vorherigen Beispiel) für alle Postfächer in der Organisation ausführt, werden Suchergebnisse für Phils Postfach zurückgegeben, obwohl Sie Filter angewendet haben, um zu verhindern, dass Bob Phils Postfach durchsucht. Der Grund ist, dass der erste Filter, der es Bob ermöglicht, die Arbeitergruppe zu durchsuchen, auf true festgelegt ist. Und da Phil Mitglied der Gruppe Arbeiter ist, kann Bob Phils Postfach durchsuchen. 
    
- **Funktioniert die Filterung von Suchberechtigungen für inaktive Postfächer?** Ja, Sie können Post Fach-und Postfachinhalts Filter verwenden, um zu begrenzen, wer inaktive Postfächer in Ihrer Organisation durchsuchen kann. Wie bei einem regulären Postfach muss ein inaktives Postfach mit der Empfänger Eigenschaft konfiguriert werden, die zum Erstellen eines Berechtigungs Filters verwendet wird. Bei Bedarf können Sie den Befehl **Get-Mailbox-InactiveMailboxOnly** verwenden, um die Eigenschaften von inaktiven Postfächern anzuzeigen. Weitere Informationen finden Sie unter [Erstellen und Verwalten inaktiver Postfächer in Office 365](create-and-manage-inactive-mailboxes.md).
    
- Funktioniert die **Filterung von Suchberechtigungen für Öffentliche Ordner?** Nein. Wie bereits erläutert, kann die Filterung von Suchberechtigungen nicht verwendet werden, um zu begrenzen, wer öffentliche Ordner in Exchange durchsuchen kann. Elemente in öffentlichen Ordner-Speicherorten können beispielsweise nicht aus den Suchergebnissen durch einen Berechtigungsfilter ausgeschlossen werden. 
    
- **Kann ein Benutzer nicht alle inhaltsspeicherorte in einem bestimmten Dienst durchsuchen, um zu verhindern, dass er inhaltsspeicherorte in einem anderen Dienst durchsucht?** Nein. Wie bereits erläutert, müssen Sie einen Filter für die Suchberechtigungen erstellen, um Benutzer daran zu hindern, inhaltsspeicherorte in einem bestimmten Office 365-Dienst zu durchsuchen (beispielsweise um zu verhindern, dass ein Benutzer ein Exchange-Postfach oder eine SharePoint-Website durchsucht). Anders ausgedrückt: durch das Erstellen eines Filters für Suchberechtigungen, mit dem ein Benutzer alle SharePoint-Websites in der Organisation durchsuchen kann, wird nicht verhindert, dass der Benutzer Postfächer durchsucht. Um beispielsweise SharePoint-Administratoren nur das Durchsuchen von SharePoint-Websites zu gestatten, müssen Sie einen Filter erstellen, der das Durchsuchen von Postfächern verhindert. Um Exchange-Administratoren nur das Durchsuchen von Postfächern zu gestatten, müssen Sie einen Filter erstellen, der die Suche nach Websites verhindert.
