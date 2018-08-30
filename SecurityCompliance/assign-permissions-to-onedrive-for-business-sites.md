---
title: Zuweisen von eDiscovery-Berechtigungen für OneDrive for Business-Websites
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/27/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: Das eDiscovery Center in SharePoint Online können Sie alle OneDrive for Business-Websites in Ihrer Organisation für bestimmte Schlüsselwörter, vertrauliche Informationen und andere Suchkriterien suchen. Jeder Benutzer in Ihrer Organisation ist der Besitzer der ihre OneDrive for Business-Website, die sich in der Websitesammlung, die mit dem Namen befindet https://domain-my.sharepoint.com. Standardmäßig können ein globaler Office 365-Administrator oder Compliance Manager das eDiscovery Center in SharePoint Online um eine beliebige OneDrive for Business-Websites zu suchen. Zum Suchen einer OneDrive for Business-Website, Administratoren oder Compliance-Manager muss ein Websitesammlungsadministrator für diese OneDrive for Business-Site.
ms.openlocfilehash: 48f84dfe21f0f99913ba2c27123d6c0e1f8bc03f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529473"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a>Zuweisen von eDiscovery-Berechtigungen für OneDrive for Business-Websites

Das eDiscovery Center in SharePoint Online können Sie alle OneDrive for Business-Websites in Ihrer Organisation für bestimmte Schlüsselwörter, vertrauliche Informationen und andere Suchkriterien suchen. Jeder Benutzer in Ihrer Organisation ist der Besitzer der ihre OneDrive for Business-Website, die sich in der Websitesammlung, die mit dem Namen befindet https://domain-my.sharepoint.com. Standardmäßig können ein globaler Office 365-Administrator oder Compliance Manager das eDiscovery Center in SharePoint Online um eine beliebige OneDrive for Business-Websites zu suchen. Zum Suchen einer OneDrive for Business-Website, Administratoren oder Compliance-Manager muss ein Websitesammlungsadministrator für diese OneDrive for Business-Site. 
  
Dieser Artikel führt Sie durch die Schritte zum Manager ein Websitesammlungsadministrator für jede OneDrive for Business-Site ein Administrator oder Compliance in Ihrer Organisation zu erstellen. 
  
Finden Sie [Weitere Informationen](#more-information) im Abschnitt Tipps zur Verwendung des Skripts in diesem Artikel, einschließlich Überarbeitung des Skripts in Schritt 3, um einen Benutzer als Websitesammlungsadministrator aus OneDrive for Business-Websites zu entfernen. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Installieren Sie die SharePoint Online-Verwaltungsshell. Weitere Informationen finden Sie unter [Einrichten der Windows PowerShell-Umgebung für die SharePoint Online-Verwaltungsshell ](https://go.microsoft.com/fwlink/p/?LinkID=286318).
    
- Führen Sie das Skript in Schritt 3 jedes Mal alle OneDrive for Business-Websites in Ihrer Organisation einen Benutzer als Administrator einer Websitesammlung zugewiesen werden soll. 
    
    > [!IMPORTANT]
    > Ein Administrator oder Compliance Manager, ein Websitesammlungsadministrator für OneDrive for Business-Websites können Benutzer OneDrive for Business-Dokumentbibliotheken zu öffnen und die gleichen als Besitzer Aufgaben ist. Es ist wichtig, steuern und überwachen, die eDiscovery-Berechtigungen zu OneDrive for Business-Websites in Ihrer Organisation zugewiesen wurde. 
  
- Das in diesem Artikel beschriebene Beispielskript wird unter keinem standard Support-Programm von Microsoft oder der Dienst nicht unterstützt. Das Beispielskript wird wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt alle konkludente Garantien einschließlich, aber nicht beschränkt auf konkludente Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck. Das gesamte Risiko aus der Verwendung oder der Leistung der Beispielskript und der Dokumentation liegt bei Ihnen. In keinem Fall muss Microsoft, seine Autoren oder jeder anderen Beteiligten in die Erstellung, die Produktion oder die Bereitstellung des Skripts für Schäden jeglicher Art (einschließlich, aber nicht beschränkt auf Schäden für den Verlust von Gewinn Business, Business Unterbrechung, Verlust von Unternehmensinformationen, Folge- oder) aus der Verwendung des oder der Fehler beim das Beispielskript oder Dokumentation verwenden haftbar gemacht werden, auch wenn Microsoft die Möglichkeit solcher Schäden hingewiesen wurde.
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a>Schritt 1: Sammeln Sie eine Liste aller onedrive for Business-Websites

Der erste Schritt ist zum Erstellen einer Liste aller onedrive for Business-Websites in Ihrer Organisation. Anweisungen finden Sie unter [Erstellen einer Liste der OneDrive Positionen in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Dieses Skript in diesem Artikel erstellt eine Textdatei, die eine Liste aller OneDrive-Websites enthält. Das Skript, das Sie in Schritt 3 ausführen, weist einen angegebenen Benutzer als Administrator einer Websitesammlung zu jedem OneDrive for Business-Website aufgeführt, die in der Textdatei, die in diesem Schritt erstellt wird. Der folgende Text enthält ein Beispiel, wie die Liste der Websites in dieser Datei formatiert werden soll. Sie können bei Bedarf Websites aus dieser Datei entfernen.

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a>Schritt 2: SharePoint Online-Verwaltungsshell Herstellen einer Verbindung mit Ihrer Organisation

1. Öffnen Sie auf Ihrem lokalen Computer die SharePoint Online-Verwaltungsshell, und führen Sie den folgenden Befehl aus:

    ```
    $credentials = Get-Credential
    ```

2. Geben Sie im Dialogfeld **Bei Windows PowerShell anmelden** den Benutzernamen und das Kennwort für Ihr globales Office 365-Administratorkonto an, und klicken Sie dann auf **OK**.
    
3. Führen Sie den folgenden Befehl aus, um eine Verbindung zwischen der Shell und Ihrem SharePoint Online-Unternehmen herzustellen:
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. Um zu prüfen, ob Sie mit Ihrer SharePoint Online-Organisation verbunden sind, führen Sie den folgenden Befehl aus, um eine Liste aller Websites in Ihrer Organisation abzurufen:
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a>Schritt 3: Zuweisen eines Benutzers als Websitesammlungsadministrator für OneDrive for Business-Websites

Im nächste Schritt wird das Ausführen eines Skripts, das einen angegebenen Benutzer als Websitesammlungsadministrator in jeder OneDrive for Business-Standort in Ihrer Organisation zuweist. Dieses Skript nutzt die Liste der OneDrive for Business-Websites, die Sie in Schritt 1 erstellt haben. Wie bereits erwähnt müssen Sie dieses Skript jedes Mal ausführen, die Sie einen Benutzer als Administrator einer Websitesammlung zu OneDrive for Business-Websites zuweisen möchten.
  
1. Speichern Sie den folgenden Text in einer Textdatei. Sie können als Dateinamen beispielsweise "OD4BAssignSCA.txt" wählen.

    ```
    # Start logging, so if this script fails, you can look at the last successful change,
    # remove any OneDrive for Business paths that worked it from the input file, and then rerun the script.

    Start-Transcript

    # URL for your organization's SPO admin service

    $AdminURI = "https://<your organization name>-admin.sharepoint.com"

    # User account for an Office 365 global admin in your organization

    $AdminAccount = "<global admin account>"

    # Compliance manager to be made site collection admin on each MySite

    $eDiscoveryUser = "<eDiscovery user account>"

    # URL for your tenant's MySite domain

    $MySitePrefix = "https://<your organization name>-my.sharepoint.com"

    # Where should we read the list of MySites?
    # This file should contain partial MySite paths formatted as follows, one per line; for example
    # /personal/junminh_contoso_onmicrosoft_com/

    $MySiteListFile = 'C:\Users\<youralias>\Desktop\ListOfMysites.txt'

    # Begin by connecting to the service
    Connect-SPOService -Url $AdminURI -Credential $AdminAccount

    # Make a reader for our list of MySites

    $reader = [System.IO.File]::OpenText($MySiteListFile)

    try {
      for(;;) {

    # Read a line
          $line = $reader.ReadLine()
    # Stop if it doesn't exist
          if ($line -eq $null) { break }

    # Turn the line into a complete SharePoint site path by merging $MySitePrefix
    # Formatted like this: "https://contoso-my.sharepoint.com"
    # ...with each partial MySite path in the file, formatted like this:
    # "/personal/junminh_contoso_onmicrosoft_com/"

          $fullsitepath = "$MySitePrefix$line"

    Write-Host "Operating on $fullsitepath "

    # We need to remove the last "/" to work around an issue.
    # "/personal/junminh_contoso_onmicrosoft_com/"
    # becomes "/personal/junminh_contoso_onmicrosoft_com"

    $fullsitepath = $fullsitepath.trimend("/")

    # Make the specified eDiscovery user a site collection admin on the OneDrive for Business site
    Write-Host "Making $eDiscoveryUser a Site Collection Admin"
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
      }
    }
    finally {
      $reader.Close()
    }
    Write-Host "Done!"
    Stop-Transcript
    Write-Host "Log written."
    ```

2. Bearbeiten Sie die folgenden Variablen am Anfang der Skriptdatei, und verwenden Sie die Informationen, die für die Organisation spezifisch sind. In den folgenden Beispielen wird davon ausgegangen, dass der Domänennamen Ihrer Organisation contoso.onmicrosoft.com ist. Achten Sie darauf, um die Werte für die Variablen mit doppelte Anführungszeichen umgeben ("").
    
    - **$AdminURI** - Dies gibt den URI für die SharePoint Online-Verwaltungsdienst, beispielsweise `"https://contoso-admin.sharepoint.com"`.
    
    - **$AdminAccount** - Hiermit wird ein globales Administratorkonto in Office 365-Organisation, beispielsweise `"admin@contoso.onmicrosoft.com"`.
    
    - **$eDiscoveryUser** - Hiermit wird das Benutzerkonto ein Administrator oder Compliance-Manager, beispielsweise als Websitesammlungsadministrator für jede OneDrive for Business-Website in Ihrer Organisation zugewiesen werden `"annb@contoso.onmicrosoft.com"`.
    
      > [!NOTE]
      > Ändern Sie das Benutzerkonto, das durch die Variable **$eDiscoveryUser** angegeben und erneut führen Sie des Skripts einen anderen Benutzer als Administrator einer Websitesammlung, um der OneDrive for Business-Websites zuzuweisen, die durch die Variable **$MySiteListFile** angegeben sind aus. 
  
    - **$MySitePrefix** Dies gibt die URL für die MySite Domäne Ihrer Organisation an. Dies ist die Domäne, die alle die OneDrive for Business-Websites in Ihrer Organisation, beispielsweise enthält `"https://contoso-my.sharepoint.com"`.
    
    - **$MySiteListFile** Dies gibt den vollständigen Pfad der Textdatei, die Sie in Schritt 1 erstellt haben. Diese Datei enthält eine Liste von OneDrive für Websites mit Geschäftsdaten in Ihrer Organisation, beispielsweise `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Achten Sie darauf, um den Wert für diese Variable mit einfache Anführungszeichen umgeben (""). Beachten Sie, dass Sie den Speicherort angeben müssen, dass Sie in Schritt 1 zu Textdatei gespeichert.
    
3. Speichern Sie die Textdatei als PowerShell-Datei, indem Sie die Dateinamenerweiterung in ".ps1" ändern. Speichern Sie beispielsweise die Datei "OD4BAssignSCA.txt" als "OD4BAssignSCA.ps1".
    
4. Wechseln Sie in der SharePoint Online-Verwaltungsshell zum Ordner mit dem im vorherigen PowerShell-Schritt erstellten Skript, und führen Sie es aus. Beispiel:
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    Sie werden aufgefordert, das Kennwort für das Administratorkonto einzugeben, die Sie in das Skript angegeben. Wenn das Skript die Nachricht erfolgreich ausgeführt wird `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` wird für jede OneDrive for Business-Website, die in der Eingabedatei durch **$MySiteListFile**angegebenen aufgeführt wird angezeigt.

## <a name="more-information"></a>Weitere Informationen

- Das Skript, das Sie in Schritt 3 ausgeführt haben verwendet das **Set-SPOUser** -Cmdlet, um den angegebenen Benutzer als Administrator einer Websitesammlung zu jeder OneDrive for Business zuweisen, die in der Datei angegeben durch die Variable **$MySiteListFile** aufgeführt wird. Wenn Sie eine große Organisation mit Hunderttausenden von Benutzern verfügen, berücksichtigen Sie Folgendes ein, um das Zuweisen von eDiscovery-Berechtigungen verwalten zu vereinfachen. 
    
  - Bearbeiten Sie die Datei, die Sie in Schritt 1 erstellt haben, die die Liste der OneDrive for Business-Websites enthält, sodass sie nur die Sites enthält, für die Benutzer sind, die aktive juristische Anfragen beteiligt sind.
    
  - Zuweisen von Berechtigungen zu nicht mehr als 2.500 OneDrive for Business-Websites pro Tag. Nehmen wir beispielsweise an, mit denen Sie 10.000 OneDrive for Business-Websites in Ihrer Organisation. Sie können die Liste in Schritt 1 zum Erfassen aller Websites erstellen. Diese Datei können Sie dann die vier Dateien erstellt, die jeweils 2.500 Benutzer enthalten. Klicken Sie auf den ersten Tag führen Sie das Skript in Schritt 3, um die zuerst 2.500 OneDrive for Business-Websites Berechtigungen zuzuweisen. Am zweiten Tag klicken Sie führen Sie das Skript für die nächsten 2.500 OneDrive for Business-Websites, und so weiter.
    
- Notieren Sie sich die OneDrive for Business-Websites, die zugewiesen wurden, eDiscovery-Berechtigungen und der Benutzer, der als Administrator der Websitesammlung zugewiesen ist. Nach dem Zuweisen von Berechtigungen können Sie beispielsweise die Textdatei mit der Liste der OneDrive for Business-Websites zu speichern und fügen Sie eine Zeile hinzu, die den Benutzer identifiziert, die als Administrator der Websitesammlung zugewiesen ist.
    
- Benutzer können die Liste der Site Collection Administratoren für ihre OneDrive for Business-Website anzeigen. Da Benutzer Websitesammlungsadministrator für ihre eigenen OneDrive for Business-Website sind, können sie Websitesammlungsadministratoren entfernen. Berücksichtigen Sie Folgendes ein, um zu mindern das Risiko von Benutzern, entfernen den Benutzer, der eDiscovery-Berechtigungen für Websites mit Geschäftsdaten zu OneDrive zugewiesen ist.
    
  - Teilen Sie den Benutzern, dass für eDiscovery und Compliance, Compliance-beauftragte als Administrator einer Websitesammlung zu OneDrive für Websites mit Geschäftsdaten in Ihrer Organisation zugewiesen wurde.
    
  - Führen Sie das Skript erneut in Schritt 3, falls erforderlich, um einen Benutzer als Administrator der Websitesammlung für OneDrive for Business-Websites neu zuzuweisen.
    
- Sie können auch das Skript, das Sie in Schritt 3 ausgeführt haben, um einen Benutzer als Administrator der Websitesammlung aus OneDrive for Business-Websites zu entfernen. Wenn einen Benutzer als Administrator einer Websitesammlung entfernen möchten, müssen Sie aus den folgenden Befehl (gegen Ende des Skripts) zu ändern: 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    in:
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    Sie können auch die folgende Zeile im Skript wie folgt ändern. Von:

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    in:
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    Nachdem Sie diese Änderungen vorgenommen haben, speichern Sie das Skript mit einem anderen Namen, beispielsweise OD4BRemoveSCA.ps1, und ihn verwenden Sie, um einen Benutzer als Administrator einer Websitesammlung aus einer Gruppe von OneDrive for Business-Websites zu entfernen.
