---
title: Einrichten von Compliance-Grenzen für eDiscovery-Untersuchungen in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: Verwenden Sie Konformitäts Grenzen, um logische Grenzen innerhalb einer Office 365-Organisation zu erstellen, die die Benutzerinhalts Speicherorte steuern, die ein eDiscovery-Manager durchsuchen kann. Konformitäts Grenzen verwenden Sie die Filterung von Suchberechtigungen (auch als Compliance-Sicherheitsfilter bezeichnet), um zu steuern, welche Postfächer, SharePoint-Websites und OneDrive-Konten von bestimmten Benutzern durchsucht werden können.
ms.openlocfilehash: b23c6d0c96874fb7e6205de6bf8a7f4eb00e4254
ms.sourcegitcommit: 691370682825a7601bd4b77d0a8c4b51ed15682f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "31014024"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a>Einrichten von Compliance-Grenzen für eDiscovery-Untersuchungen in Office 365

Konformitäts Grenzen erstellen logische Grenzen innerhalb einer Office 365-Organisation, die die Benutzerinhalts Speicherorte (wie Postfächer, SharePoint-Websites und OneDrive-Konten) steuern, die von eDiscovery-Managern durchsucht werden können. Darüber hinaus steuern Compliance-Grenzen, wer auf eDiscovery-Fälle zugreifen kann, die zum Verwalten der rechtlichen, personellen Ressourcen oder sonstigen Untersuchungen in Ihrer Organisation verwendet werden. Die Notwendigkeit von Compliance-Grenzen ist häufig für Multi-Nations-Unternehmen erforderlich, die geographische Anforderungen und Vorschriften respektieren müssen, und für Regierungen, die häufig in verschiedene Agenturen unterteilt sind. In Office 365 können Sie diese Anforderungen bei der Durchführung von Inhalts suchen und bei der Verwaltung von Untersuchungen mit eDiscovery-Fällen erfüllen.
  
Anhand des Beispiels in der folgenden Abbildung wird erläutert, wie die Konformitäts Grenzen funktionieren.
  
![Konformitäts Grenzen bestehen aus Such Berechtigungs filtern, die den Zugriff auf Agenturen und Administratorrollengruppen steuern, die den Zugriff auf eDisocovery-Fälle steuern.](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
In diesem Beispiel ist contoso LTD eine Office 365-Organisation, die aus zwei Niederlassungen, Fourth Coffee und Weinkellerei besteht. Das Unternehmen erfordert, dass eDiscovery-Manger und-Prüfer nur die Exchange-Postfächer, OneDrive-Konten und SharePoint-Websites in Ihrer Agentur durchsuchen können. Darüber hinaus können eDiscovery-Manager und-Prüfer nur eDiscovery-Fälle in der Agentur anzeigen, und Sie können nur auf die Fälle zugreifen, in denen Sie Mitglied sind. Hier erfahren Sie, wie Compliance-Grenzen diese Anforderungen erfüllen.
  
- Die Funktion zum Filtern von Suchberechtigungen in der Inhaltssuche steuert die inhaltsspeicherorte, die eDiscovery-Manager und-Prüfer durchsuchen können. Dies führt dazu, dass eDiscovery-Manager und-Prüfer in der vierten Kaffee Agentur nur inhaltsspeicherorte in der Fourth Coffee-Niederlassung durchsuchen können. Die gleiche Einschränkung gilt für die Weinkellerei-Tochtergesellschaft.
    
    Rollengruppen steuern, wer die eDiscovery-Fälle im Security & Compliance Center anzeigen kann. Dies führt dazu, dass eDiscovery-Manager und-Prüfer nur die eDiscovery-Fälle in Ihrer Agentur sehen können.
    
- Rollengruppen steuern außerdem, wer einem eDiscovery-Fall Mitglieder zuweisen kann. Dies führt dazu, dass eDiscovery-Manager und-Prüfer nur dann Mitglieder zuweisen können, wenn Sie selbst Mitglied sind.
    
Hier finden Sie den Prozess zum Einrichten von Konformitäts Grenzen:
  
[Schritt 1: Identifizieren eines Benutzer Attributs zum Definieren Ihrer Agenturen](#step-1-identify-a-user-attribute-to-define-your-agencies)

[Schritt 2: Datei eine Anforderung mit Microsoft-Support, um das Benutzerattribut mit OneDrive-Konten zu synchronisieren](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[Schritt 3: Erstellen einer Rollengruppe für jede Agentur](#step-3-create-a-role-group-for-each-agency)

[Schritt 4: Erstellen eines Filters für Suchberechtigungen zum Erzwingen der Konformitäts Grenze](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[Schritt 5: Erstellen eines eDiscovery-Falls für interne Untersuchungen](#step-5-create-an-ediscovery-case-for-an-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a>Schritt 1: Identifizieren eines Benutzer Attributs zum Definieren Ihrer Agenturen

Der erste Schritt besteht darin, ein Azure Active Directory-Attribut zu verwenden, das Ihre Agenturen definiert. Dieses Attribut wird verwendet, um den Such Berechtigungsfilter zu erstellen, der einen eDiscovery-Manager so beschränkt, dass nur die inhaltsspeicherorte der Benutzer durchsucht werden, denen ein bestimmter Wert für dieses Attribut zugewiesen wurde. Nehmen wir beispielsweise an, Contoso beschließt, das **Department** -Attribut zu verwenden. Der Wert für dieses Attribut für Benutzer in der Fourth Coffee `FourthCoffee` -Tochtergesellschaft wäre und der Wert für Benutzer in Weinkellerei-Tochterunternehmen `CohoWinery`wäre. In Schritt 4 verwenden Sie dieses `attribute:value` Paar (beispielsweise *Department: fourthcoffee* ), um die Benutzerinhalts Speicherorte einzuschränken, die eDiscovery-Manager durchsuchen können. 
  
Im folgenden finden Sie eine Liste der Azure Active Directory-Benutzerattribute, die Sie für Konformitäts Grenzen verwenden können:
  
- Company
    
- CustomAttribute1-CustomAttribute15
    
- Abteilung
    
- Büro

- C (zwei Länder Code)
    
Obwohl mehr Benutzerattribute verfügbar sind, insbesondere für Exchange-Postfächer, sind die oben aufgeführten Attribute die einzigen, die derzeit von OneDrive unterstützt werden.
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a>Schritt 2: Datei eine Anforderung mit Microsoft-Support, um das Benutzerattribut mit OneDrive-Konten zu synchronisieren

Der nächste Schritt besteht darin, eine Anforderung beim Microsoft-Support zu stellen, um das Azure Active Directory-Attribut zu synchronisieren, das Sie in Schritt 1 für alle OneDrive-Konten in Ihrer Organisation ausgewählt haben. Nach dieser Synchronisierung wird das Attribut (und sein Wert), den Sie in Schritt 1 ausgewählt haben, einer ausgeblendeten verwalteten Eigenschaft in SharePoint zugeordnet `ComplianceAttribute`. Sie verwenden dieses Attribut, um den Filter für Suchberechtigungen für OneDrive in Schritt 4 zu erstellen.
  
Schließen Sie die folgenden Informationen ein, wenn Sie die Anforderung an den Microsoft-Support übermitteln:
  
- Der Standarddomänenname Ihrer Office 365-Organisation
    
- Der Name des Azure Active Directory-Attributs (aus Schritt 1)
    
- Der folgende Titel oder eine Beschreibung des Zwecks der Supportanfrage: "Aktivieren der OneDrive for Business-Synchronisierung mit Azure Active Directory für Compliance-Sicherheitsfilter". Dadurch wird die Anforderung an das Office 365 eDiscovery Engineering-Team weitergeleitet, das die Anforderung implementiert.
    
Nachdem die technische Änderung vorgenommen wurde und das Attribut mit OneDrive synchronisiert wurde, sendet Ihnen der Microsoft-Support die Buildnummer, an der die Änderung vorgenommen wurde, und einen geschätzten Bereitstellungstermin. Beachten Sie, dass der Bereitstellungsprozess in der Regel 4-6 Wochen dauert, nachdem Sie die Supportanfrage übermittelt haben.
  
 **Wichtig:** Sie können Schritt 3 bis Schritt 5 abschließen, bevor die Änderung bereitgestellt wird. Durch die Ausführung von Inhalts suchen werden jedoch erst nach der Bereitstellung der Änderung Dokumente von OneDrive-Websites zurückgegeben, die im Filter für Suchberechtigungen angegeben sind. 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a>Schritt 3: Erstellen einer Rollengruppe für jede Agentur

Im nächsten Schritt werden die Rollengruppen im Security & Compliance Center erstellt, das an Ihre Agenturen ausgerichtet wird. Es wird empfohlen, eine neue Rollengruppe zu erstellen, indem Sie die integrierte eDiscovery-Manager-Gruppe kopieren, die entsprechenden Mitglieder hinzufügen und Rollen entfernen, die möglicherweise nicht Ihren Anforderungen entsprechen. Weitere Informationen zu eDiscovery-bezogenen Rollen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office 365 Security _AMP_ Compliance Center](assign-ediscovery-permissions.md).
  
Um die Rollengruppen zu erstellen, wechseln Sie zur Seite **Berechtigungen** im Security _AMP_ Compliance Center, und erstellen Sie eine Rollengruppe für jedes Team in jeder Agentur, die Konformitäts Grenzen und eDiscovery-Fälle zum Verwalten von Untersuchungen verwendet. 
  
Unter Verwendung des Contoso-Konformitäts Grenzen-Szenarios müssen vier Rollengruppen erstellt und den jeweiligen Mitgliedern hinzugefügt werden.
  
- Vierter Kaffee eDiscovery-Manager
    
- Vierte Kaffee erMittler
    
- Weinkellerei-eDiscovery-Manager
    
- Weinkellerei-unterSucher
    

  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a>Schritt 4: Erstellen eines Filters für Suchberechtigungen zum Erzwingen der Konformitäts Grenze

Nachdem Sie Rollengruppen für jede Agentur erstellt haben, besteht der nächste Schritt darin, die Such Berechtigungsfilter zu erstellen, die jede Rollengruppe ihrer jeweiligen Agentur zuordnen und die Konformitäts Grenze selbst definieren. Sie müssen für jede Agentur einen Filter für Suchberechtigungen erstellen. Weitere Informationen zum Erstellen von Sicherheits Berechtigungs Filtern finden Sie unter [configure Permissions Filtering for Content Search](permissions-filtering-for-content-search.md).
  
Hier ist die Syntax, die zum Erstellen eines Filters für die Einhaltung von Konformitäts Grenzen verwendet wird.

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<Compliance attribute from Step 1>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq <AttributeValue>' -or Site_Path -like <SharePointURL> *'" -Action <Action >
```
  
Im folgenden finden Sie eine Beschreibung der einzelnen Parameter im Befehl:
  
-  `FilterName`-Gibt den Namen des Filters an. Verwenden Sie einen Namen, der die Agentur beschreibt oder identifiziert, in der der Filter verwendet wird. 
    
-  `Users`– Gibt die Benutzer oder Gruppen an, die diesen Filter auf die ausgeführten Inhalts Suchaktionen anwenden. Für Konformitäts Grenzen gibt dieser Parameter die Rollengruppen (die Sie in Schritt 3 erstellt haben) in der Agentur an, für die Sie den Filter erstellen. Hinweis Hierbei handelt es sich um einen mehrwertigen Parameter, sodass Sie eine oder mehrere Rollengruppen mit Kommas voneinander trennen können. 
    
-  `Filters`-Gibt die Suchkriterien für den Filter an. Für die Konformitäts Grenzen definieren Sie die folgenden Filter. Jedes gilt für einen Benutzer-Inhaltsspeicherort. 
    
  -  `Mailbox`– Gibt die Postfächer an, die die im `Users` Parameter definierten Rollengruppen durchsuchen können. Für Konformitäts Grenzen ** ist complianceattribute das gleiche Attribut, das Sie in Schritt 1 identifiziert haben, und *Attribut* Wert gibt die Agentur an. Dieser Filter ermöglicht es Mitgliedern der Rollengruppe, nur die Postfächer in einer bestimmten Agentur zu durchsuchen. Beispiel: `"Mailbox_Department -eq 'FourthCoffee'"` . 
    
  -  `Site`– Gibt die OneDrive-Konten an, die die im `Users` Parameter definierten Rollengruppen durchsuchen können. Verwenden Sie für den OneDrive-Filter die tatsächliche `ComplianceAttribute`Zeichenfolge; Dies entspricht dem Attribut, das Sie in Schritt 1 identifiziert haben und das aufgrund der von Ihnen in Schritt 2 übermittelten Supportanforderungen mit OneDrive-Konten synchronisiert wird.  *Attributvalue* gibt die Agentur an. Dieser Filter ermöglicht es Mitgliedern der Rollengruppe, nur die OneDrive-Konten in einer bestimmten Agentur zu durchsuchen. Beispiel: `"Site_ComplianceAttribute -eq 'FourthCoffee'"`.
    
  -  `Site_Path`– Gibt die SharePoint-Websites an, die die im `Users` Parameter definierten Rollengruppen durchsuchen können. Der *SharePointURL* gibt die Websites in der Agentur an, die Mitglieder der Rollengruppe durchsuchen können; Zum Beispiel`"Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`
    
-  `Action`-Gibt den Typ der Compliance-Suchaktion an, auf die der Filter angewendet wird. Beispielsweise würde `-Action Search` den Filter nur anwenden, wenn Mitglieder der im `Users` Parameter definierten Rollengruppen eine Inhaltssuche ausführen. In diesem Fall würde der Filter beim Exportieren von Suchergebnissen nicht angewendet. Verwenden Sie `-Action All` für Compliance-Grenzen den Filter, der auf alle Suchaktionen angewendet wird. 
    
    Eine Liste der Inhalts Suchaktionen finden Sie im Abschnitt "New-ComplianceSecurityFilter" unter [configure Permissions Filtering for Content Search](permissions-filtering-for-content-search.md#new-compliancesecurityfilter).
    
Im folgenden finden Sie Beispiele für die beiden Filter für Suchberechtigungen, die für die Unterstützung des Contoso-Konformitäts Grenzen-Szenarios erstellt würden.
  
 **Vierter Kaffee**

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 **Weinkellerei**

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-an-intra-agency-investigations"></a>Schritt 5: Erstellen eines eDiscovery-Falls für interne Untersuchungen

Der letzte Schritt besteht darin, einen neuen eDiscovery-Fall im Security & Compliance Center zu erstellen und dann die Rollengruppe, die Sie in Schritt 3 erstellt haben, als Mitglied der Groß-/Kleinschreibung hinzuzufügen. Dies führt zu zwei wichtigen Merkmalen der Verwendung von Konformitäts Grenzen:
  
- Nur Mitglieder der Rollengruppe, die dem Fall hinzugefügt wurden, können den Fall im Security & Compliance Center sehen und darauf zugreifen. Wenn beispielsweise die Rollengruppe "Fourth Coffee Investigators" das einzige Mitglied eines Falls ist, können Mitglieder der Gruppe "vierte Kaffee-eDiscovery-Manager" (oder Mitglieder einer anderen Rollengruppe) den Fall nicht anzeigen oder darauf zugreifen.
    
- Wenn ein Mitglied der Rollengruppe, die einem Fall zugewiesen ist, eine Suche ausführt, die dem Fall zugeordnet ist, können Sie nur die inhaltsspeicherorte innerhalb Ihrer Agentur Durchsuchen (Dies wird durch den Filter für Suchberechtigungen definiert, den Sie in Schritt 4 erstellt haben).


So erstellen Sie eine neue Groß-/Kleinschreibung und weisen Mitglieder zu:
    
1. Wechseln Sie zur **eDiscovery** -Seite im Security _AMP_ Compliance Center, und erstellen Sie einen neuen Fall. 
    
2. Klicken Sie in der Liste der eDiscovery-Fälle auf den Namen der soeben erstellten Groß-/Kleinschreibung.
    
3. Klicken Sie auf der Seite **dieses Fall Flyout verwalten** unter **Mange role groups**auf ![Add Icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **Add**.
    
    ![Hinzufügen einer Rollengruppe als Mitglied eines eDiscovery-Falls](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. Wählen Sie in der Liste der Rollengruppen eine der Rollengruppen aus, die Sie in Schritt 3 erstellt haben, und klicken Sie auf **Hinzufügen**.
    
5. Klicken Sie im Flyout **dieses Fall verwalten** auf **Speichern** , um die Änderung zu speichern. 

## <a name="compliance-boundary-limitations"></a>Einschränkungen der Compliance-Grenze

Beachten Sie beim Verwalten von eDiscovery-Fällen und Untersuchungen, die Konformitäts Grenzen verwenden, die folgenden Einschränkungen.
  
- Beim Erstellen und Durchführen einer Inhaltssuche können Sie inhaltsspeicherorte außerhalb Ihrer Agentur auswählen. Aufgrund des Filters "Suchberechtigungen" werden die Inhalte allerdings nicht in die Suchergebnisse eingeschlossen.
    
- Konformitäts Grenzen gelten nicht für haltebereiche in eDiscovery-Fällen. Das besagt, dass ein eDiscovery-Manager in einer Agentur einen Benutzer in einer anderen Agentur halten kann. Die Kompatibilitäts Grenze wird jedoch erzwungen, wenn der eDiscovery-Manager die inhaltsspeicherorte des Benutzers durchsucht, der in der Warteschleife gespeichert wurde. Das kann bedeuten, dass der eDiscovery-Manager nicht in der Lage ist, die inhaltsspeicherorte des Benutzers zu durchsuchen, obwohl er in der Lage ist, den Benutzer zu halten.
    
    Darüber hinaus gilt die Aufbewahrungs Statistik nur für inhaltsspeicherorte in der Agentur.
    
- Filter für Suchberechtigungen werden nicht auf öffentliche Exchange-Ordner angewendet.

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a>Suchen und Exportieren von Inhalten in Multi-Geo-Umgebungen

Mit den Such Berechtigungs filtern können Sie auch steuern, wohin der Inhalt für den Export weitergeleitet wird und welches Rechenzentrum beim Durchsuchen von Inhaltsspeicherorten in einer [Multi-Geo-Umgebung für SharePoint](https://go.microsoft.com/fwlink/?linkid=860840)durchsucht werden kann.
  
- **Suchergebnisse exportieren** – Sie können die Suchergebnisse aus Exchange-Postfächern, SharePoint-Websites und OneDrive-Konten aus einem bestimmten Datencenter exportieren. Dies führt dazu, dass Sie den Speicherort des Datencenters angeben, aus dem Suchergebnisse exportiert werden.

    Verwenden Sie den Parameter **Region** für die Cmdlets **New-ComplianceSecurityFilter** oder **Set-ComplianceSecurityFilter** , um das Datencenter zu erstellen oder zu ändern, über das der Export weitergeleitet wird.
  
    |**Übergebener Wert**|**Datencenter-Speicherort**|
    |:-----|:-----|
    |NAM  <br/> |Nordamerika (tatsächliche Rechenzentren befinden sich in den USA)  <br/> |
    |EUR  <br/> |Europa  <br/> |
    |APC  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |CAN <br/> |Kanada
    
- **Routen von Inhalts suchen** – Sie können die Inhaltssuche von SharePoint-Websites und OneDrive-Konten zu einem Satellitendaten Center weiterleiten. Sie können also den Speicherort des Datencenters angeben, an dem die Suche ausgeführt wird.
    
    Verwenden Sie die folgenden Werte für die **Region** -Parameterwerte, um zu steuern, welches Datencenter beim Durchsuchen von SharePoint-Websites und OneDrive-Speicherorten in der Inhaltssuche ausgeführt wird. Beachten Sie, dass in der folgenden Tabelle gezeigt wird, welche Datencenter-Exporte weitergeleitet werden. 
  
    |**Übergebener Wert**|**Datencenter-Routing Speicherorte für den Export**|
    |:-----|:-----|
    |NAM  <br/> |UNS  <br/> |
    |EUR  <br/> |Europa  <br/> |
    |APC  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |CAN  <br/> |UNS  <br/> |
    |AUS  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |KOR  <br/> |Das Standarddaten Center der Organisation  <br/> |
    |GBR  <br/> |Europa  <br/> |
    |JPN  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |IND  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |LAM  <br/> |UNS  <br/> |
   
> [!NOTE]
> Wenn Sie den Parameter **Region** für einen Filter für Suchberechtigungen nicht angeben, wird die SharePoint-Standardregion Organisationen durchsucht, und die Suchergebnisse werden in das nächstgelegene Datencenter exportiert. 
  
Im folgenden finden Sie Beispiele für die Verwendung des **Region** -Parameters beim Erstellen von Such Berechtigungs Filtern für Konformitäts Grenzen. Dabei wird davon ausgegangen, dass sich die Fourth Coffee-Tochtergesellschaft in Nordamerika befindet und dass es sich um Weinkellerei in Europa handelt. 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
Beachten Sie beim Durchsuchen und Exportieren von Inhalten in Multi-Geo-Umgebungen Folgendes.
  
- Der Parameter **Region** steuert die Suche von Exchange-Postfächern nicht. Alle Rechenzentren werden durchsucht, wenn Sie Postfächer durchsuchen. Zum Einschränken des Bereichs, in dem Exchange-Postfächer durchsucht werden können, verwenden Sie den **Filters** -Parameter beim Erstellen oder Ändern eines Such Berechtigungs Filters. 
    
- Wenn ein eDiscovery-Manager für die Suche in mehreren SharePoint-Regionen erforderlich ist, müssen Sie ein anderes Benutzerkonto für diesen eDiscovery-Manager erstellen, der im Filter für Suchberechtigungen verwendet werden kann, um die Alternative Region anzugeben, in der die SharePoint-Websites oder OneDrive-Konten befinden sich.
    
- Bei der Suche nach Inhalten in SharePoint und OneDrive leitet der Parameter **Region** die Suche entweder auf den Haupt-oder den Satellitenstandort, an dem der eDiscovery-Manager eDiscovery-Untersuchungen durchführen wird. Wenn ein eDiscovery-Manager SharePoint-und OneDrive-Websites außerhalb der Region durchsucht, die im Filter "Suchberechtigungen" angegeben ist, werden keine Suchergebnisse zurückgegeben. 
    
- Beim Exportieren von Suchergebnissen werden Inhalte aus allen Inhaltsspeicherorten (einschließlich Exchange, Skype for Business, SharePoint, OneDrive und anderen Office 365-Diensten, die Sie mithilfe des Inhalts Suchtools durchsuchen können) an den Azure-Speicherort in der Rechenzentrum, das durch den Parameter **Region** angegeben wird. Dadurch können Organisationen innerhalb der Compliance bleiben, indem Sie nicht zulassen, dass Inhalte über kontrollierte Rahmen exportiert werden. Wenn im Filter Berechtigungen für die Suche keine Region angegeben ist, wird der Inhalt in die Standardregion der Organisation hochgeladen. 
    
- Sie können einen vorhandenen Filter für Suchberechtigungen bearbeiten, um den Bereich hinzuzufügen oder zu ändern, indem Sie den folgenden Befehl ausführen:

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

 **Wer kann Such Berechtigungsfilter erstellen und verwalten (mithilfe von New-ComplianceSecurityFilter und Set-ComplianceSecurityFilter-Cmdlets)?**
  
Zum Erstellen, anzeigen und Ändern von Such Berechtigungs filtern müssen Sie Mitglied der Rollengruppe "Organisationsverwaltung" im Security & Compliance Center sein.
  
 **Wenn ein eDiscovery-Manager mehreren Rollengruppen zugewiesen ist, die mehrere Organisationen umfassen, wie Suchen Sie nach Inhalten in einer Agentur oder in der anderen?**
  
Der eDiscovery-Manager kann seiner Suchabfrage Parameter hinzufügen, die die Suche auf eine bestimmte Agentur einschränken. Wenn eine Organisation beispielsweise die **CustomAttribute10** -Eigenschaft zum unterscheiden von Agenturen angegeben hat, können Sie die folgenden Punkte an Ihre Suchabfrage anfügen, um Postfächer und OneDrive-Konten in `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`einer bestimmten Agentur zu suchen:.
  
 **Was geschieht, wenn der Wert des Attributs, das als Kompatibilitätsattribut in einem Filter für Suchberechtigungen verwendet wird, geändert wird?**
  
Es dauert bis zu 3 Tage, bis ein Such Berechtigungsfilter die Konformitäts Grenze erzwungen hat, wenn der Wert des Attributs, das im Filter verwendet wird, geändert wird. Im Contoso-Szenario wird beispielsweise angenommen, dass ein Benutzer in der vierten Kaffee Agentur an die Weinkellerei Agentur Winery übertragen wird. Daher wird der Wert des **Department** -Attributs für das User-Objekt von *fourthcoffee* in *cohowinery* geändert. In dieser Situation erhalten Fourth Coffee eDiscovery und Investoren Suchergebnisse für diesen Benutzer nach drei Tagen nach dem Ändern des Attributs. Auf ähnliche Weise wird es bis zu 3 Tage dauern, bis das Weingut eDiscovery-Manager und-Prüfer die Suchergebnisse für den Benutzer erhalten. 
  
 **Kann ein eDiscovery-Manager Inhalte aus zwei separaten Kompatibilitäts Grenzen anzeigen?**
  
Ja. Hierzu können Sie den Benutzerrollen Gruppen hinzufügen, die für beide Agenturen sichtbar sind.
  
 **Funktionieren Such Berechtigungsfilter für eDiscovery Case Holds, Office 365-Aufbewahrungsrichtlinien oder DLP?**
  
Nein, nicht zu diesem Zeitpunkt
  
 **Wenn ich eine Region angeben, um zu steuern, wo der Inhalt exportiert wird, aber ich habe keine SharePoint-Organisation in dieser Region, kann ich trotzdem SharePoint durchsuchen?**
  
Wenn der im Filter "Search Permissions" angegebene Bereich nicht in Ihrer Organisation vorhanden ist, wird der Standardbereich durchsucht.
  
 **Wie hoch ist die maximale Anzahl von Such Berechtigungs filtern, die in einer Organisation erstellt werden können?**
  
Es gibt keine Begrenzung für die Anzahl der Filter für Suchberechtigungen, die in einer Organisation erstellt werden können. Die Suchleistung wirkt sich jedoch auf mehr als 100 Such Berechtigungsfilter aus. Um die Anzahl von Such Berechtigungs Filtern in Ihrer Organisation so klein wie möglich zu halten, erstellen Sie Filter, mit denen Regeln für Exchange, SharePoint und OneDrive in einem einzigen Filter für Suchberechtigungen kombiniert werden, wann immer möglich.
