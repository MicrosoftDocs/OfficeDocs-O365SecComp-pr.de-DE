---
title: Einrichten von Compliance-Grenzen für eDiscovery Untersuchungen in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/6/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: Verwenden Sie Compliance-Grenzen logische Grenzen innerhalb einer Office 365-Organisation zu erstellen, die die Speicherorte für Benutzer Inhalte steuern, die ein eDiscovery-Manager durchsuchen kann. Compliance-Grenzen Search-Berechtigungen (auch so genannte Kompatibilität Sicherheitsfilter) filtern, um zu steuern, welche Postfächer, die SharePoint-Websites verwenden, und OneDrive-Konten von bestimmten Benutzern durchsucht werden können.
ms.openlocfilehash: 822d228d64d2fd5432db327db98e8d7329c7d939
ms.sourcegitcommit: c166964fe14eec69139a2d3d9c10d2c40ab33f91
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2018
ms.locfileid: "23258633"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a>Einrichten von Compliance-Grenzen für eDiscovery Untersuchungen in Office 365

Compliance-Grenzen erstellen logische Grenzen innerhalb einer Office 365-Organisation, die die Speicherorte für Benutzer Inhalte (wie Postfächer, SharePoint-Websites und OneDrive Konten) steuern, die eDiscovery-Manager durchsuchen können. Darüber hinaus Compliance Grenzen steuern, wer eDiscovery-Fälle verwendet, um die rechtlichen, Personalabteilung oder andere Untersuchungen innerhalb Ihrer Organisation verwalten zugreifen kann. Die Notwendigkeit für Compliance-Grenzen ist häufig erforderlich für Unternehmen mit mehreren Nationen, die über geografische Grenzen und Vorschriften einhalten verfügen und für Behörden, die häufig in unterschiedlichen Behörden unterteilt sind. In Office 365, Compliance Grenzen Hilfe, die Sie erfüllen Inhalt diese Anforderungen beim Ausführen einer suchen und Verwalten von Untersuchungen mit eDiscovery-Fälle.
  
Wir verwenden das Beispiel in der folgenden Abbildung zur Erläuterung der Funktionsweise von Compliance-Grenzen.
  
![Compliance-Grenzen bestehen aus Berechtigungen Suchfilter, dass Steuern des Zugriffs auf Behörden und Administratorrolle, Steuern des Zugriffs auf eDisocovery Fällen Gruppen](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
In diesem Beispiel wird die Contoso LTD einer Office 365-Organisation, die aus zwei Niederlassungen, Fourth Coffee und Coho Winery besteht. Das Unternehmen benötigt, eDiscovery-Manager und Prüfer nur die Exchange-Postfächer, OneDrive-Konten und SharePoint-Websites in ihrer Behörde durchsuchen können. Darüber hinaus eDiscovery-Manager und Prüfer können nur sehen, eDiscovery-Fälle, in der in ihrer Behörde und können nur auf zugreifen die Fälle, in denen sie Mitglied sind. Hier ist wie Grenzen Compliance diese Anforderungen erfüllen.
  
- Die Search-Berechtigungen Filterfunktionalität in Inhalten Suchsteuerelemente die Speicherorte für Inhalte, die eDiscovery-Manager und Prüfer suchen können. Dies bedeutet, dass die eDiscovery-Manager und Prüfer in Fourth Coffee Behörde nur Speicherorte für Inhalte in das Fourth Coffee Subsidiary suchen können. Diese Beschränkung gilt für die Niederlassung Coho Winery.
    
    Die Rolle des Projektmanagers steuern, wer die eDiscovery-Fälle in die Office 365-Sicherheit finden Sie unter kann &amp; Compliance Center. Dies bedeutet, dass die eDiscovery-Manager und Prüfer nur die eDiscovery-Fälle, in deren Agency sehen können.
    
- Außerdem steuern Rollengruppen, die Mitglieder zu einem eDiscovery-Fall zuweisen können. Dies bedeutet, dass die eDiscovery-Manager und Prüfer nur Mitglieder Fällen zuweisen können, die sie selbst Mitglied sind.
    
Hier wird der Prozess zum Einrichten von Compliance-Grenzen:
  
[Schritt 1: Identifizieren einer Benutzerattribut, um Ihre Behörden definieren](#step-1-identify-a-user-attribute-to-define-your-agencies)

[Schritt 2: Datei eine Anforderung mit Microsoft Support für die Synchronisierung von Benutzer-Attribut auf OneDrive-Konten](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[Schritt 3: Erstellen einer Rollengruppe für jede Behörde](#step-3-create-a-role-group-for-each-agency)

[Schritt 4: Erstellen Sie einen Suchfilter Berechtigungen, um die Grenze für die Einhaltung von Bestimmungen erzwingen](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[Schritt 5: Erstellen Sie einen eDiscovery-Fall für ein Intra-Agency Untersuchungen](#step-5-create-an-ediscovery-case-for-an-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a>Schritt 1: Identifizieren einer Benutzerattribut, um Ihre Behörden definieren

Der erste Schritt besteht, wählen Sie ein Azure Active Directory-Attribut verwenden, die Ihre Behörden definiert werden. Zum Erstellen des Berechtigungen Suchfilters, der eine eDiscovery-Grenzwerte Manager, um nur die Speicherorte für Inhalte von Benutzern zu suchen, die einen bestimmten Wert für dieses Attribut zugewiesen sind, wird dieses Attribut verwendet werden. Beispielsweise angenommen, dass Contoso entscheidet, verwenden Sie das Attribut **Abteilung** . Der Wert für dieses Attribut für Benutzer in der Niederlassung Fourth Coffee wäre `FourthCoffee` und der Wert für Benutzer in Coho Winery Niederlassung wäre `CohoWinery`. In Schritt 4: Verwenden Sie dies `attribute:value` Paar (beispielsweise *Abteilung: FourthCoffee* ) an den Benutzer beschränken content-Standorte, die eDiscovery-Manager durchsuchen können. 
  
Es folgt eine Liste von Azure Active Directory-Benutzer-Attribute, die Sie für Compliance-Grenzen verwenden können:
  
- Company
    
- CountryCode
    
- CustomAttribute1 - CustomAttribute15
    
- Abteilung
    
- Büro
    
Weitere Benutzerattribute besonders für Exchange-Postfächer verfügbar sind, sind die oben aufgeführten Attribute die einzigen, die derzeit von OneDrive unterstützt werden.
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a>Schritt 2: Datei eine Anforderung mit Microsoft Support für die Synchronisierung von Benutzer-Attribut auf OneDrive-Konten

Im nächste Schritt wird an der Datei einer Anforderung mit Microsoft-Supportmitarbeiter zum Synchronisieren von Azure Active Directory-Attribut, das Sie in Schritt 1 für alle OneDrive-Konten in Ihrer Organisation ausgewählt haben. Nachdem diese Synchronisierung wird das Attribut (und dessen Wert), die Sie in Schritt 1 ausgewählt haben werden in SharePoint mit dem Namen einer ausgeblendeten verwalteten Eigenschaft zugeordnet `ComplianceAttribute`. Verwenden Sie dieses Attribut für OneDrive in Schritt 4 den Suchfilter Berechtigungen zu erstellen.
  
Enthalten Sie die folgenden Informationen an, wenn die Anforderung an den Support von Microsoft zu übermitteln:
  
- Der Standard-Domänenname des Office 365-Organisation
    
- Der Name des Azure Active Directory-Attributs (aus Schritt 1)
    
- Die folgenden Titel oder die Beschreibung des Zwecks der Anforderung Unterstützung: "OneDrive for Business Synchronisierung mit Azure Active Directory für Compliance Sicherheitsfilter aktivieren". Dadurch wird die Anforderung an den Office 365 eDiscovery engineering Team weitergeleitet, die die Anforderung implementiert.
    
Nachdem die engineering Änderung erfolgt ist und das Attribut wird mit OneDrive synchronisiert, senden Microsoft Support Sie eine geschätzte Bereitstellungsdatum und die Buildnummer an, der in die Änderung erfolgt ist. Beachten Sie, dass der Bereitstellungsprozess in der Regel 4 bis 6 Wochen nach der Supportanfrage zu übermitteln.
  
 **Wichtig:** Sie können Schritt 3 bis 5 Schritt abschließen, bevor die Änderung bereitgestellt wird. Aber Content-Suche ausgeführt werden nicht zurück Dokumente aus OneDrive-Websites im Suchfilter Berechtigungen bis angegeben wird, nachdem die Änderung bereitgestellt wird. 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a>Schritt 3: Erstellen einer Rollengruppe für jede Behörde

Im nächsten Schritt wird zum Erstellen von Rollengruppen in die Office 365-Sicherheit &amp; Compliance Center, die mit Ihrer Behörden ausgerichtet werden. Es wird empfohlen, dass Sie eine neuen Rollengruppe durch Kopieren der integrierten eDiscovery-Manager-Gruppe, die entsprechenden Member hinzufügen und Entfernen von Rollen, die möglicherweise nicht anwendbar auf Ihre Bedürfnisse erstellen. Weitere Informationen zu Rollen im Zusammenhang mit eDiscovery, finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
  
Wenn Rollengruppen erstellen möchten, wechseln Sie zur Seite **Berechtigungen** in das Wertpapier &amp; Compliance Center und erstellen eine Rollengruppe für jedes Team in jeder Agency, die Grenzen Compliance und eDiscovery-Fälle verwenden, um Untersuchungen zu verwalten. 
  
Contoso Compliance-Grenzen Szenario verwenden, vier Rollengruppen erstellt werden müssen und die entsprechenden Member jeweils hinzugefügt.
  
- Fourth Coffee eDiscovery-Manager
    
- Fourth Coffee Prüfer
    
- Coho Winery eDiscovery-Manager
    
- Coho Winery Prüfer
    

  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a>Schritt 4: Erstellen Sie einen Suchfilter Berechtigungen, um die Grenze für die Einhaltung von Bestimmungen erzwingen
<a name="step4"> </a>

Nachdem Sie Rollengruppen für jede Behörde erstellt haben, im nächste Schritt besteht darin, die Berechtigungen Suchfilter erstellen, die jede Rollengruppe zu seiner bestimmte Agency zuordnen und definiert die Compliance-Begrenzung selbst. Sie müssen eine Berechtigungen Suchfilter für jede Behörde erstellen. Weitere Informationen zu Sicherheit Berechtigungen Filter erstellen finden Sie unter [Konfigurieren von Berechtigungen für Inhaltssuche Filtern](permissions-filtering-for-content-search.md).
  
Dies ist die Syntax, die zum Erstellen eines Suchfilters-Berechtigungen für die Einhaltung von Bestimmungen Grenzen verwendet verwendet wird.

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<Compliance attribute from Step 1>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq <AttributeValue>' -or Site_Path -like <SharePointURL> *'" -Action <Action >
```
  
Hier ist eine Beschreibung der einzelnen Parameter in den Befehl ein:
  
-  `FilterName`-Gibt den Namen des Filters. Verwenden Sie einen Namen, die beschreibt, oder der Behörde, die Filtern identifiziert wird in verwendet werden. 
    
-  `Users`-Gibt an, die Benutzer oder Gruppen, die dieser Filter angewendet, die den Inhaltssuche-Aktionen, die sie ausführen möchten. Für Compliance-Grenzen gibt dieser Parameter die Rollengruppen (die in Schritt 3 erstellte) in der Behörde, den Sie für den Filter erstellen. Beachten Sie, dass dies ein Parameter mit mehreren Werten ist, damit Sie einen oder mehrere Rollengruppen, durch Kommas getrennt angeben können. 
    
-  `Filters`-Gibt die Suchkriterien für den Filter an. Für die Einhaltung von Bestimmungen Grenzen definieren Sie die folgenden Filter. Jeweils gilt für einen Benutzer Inhaltsspeicherort. 
    
  -  `Mailbox`-Gibt an, die Postfächer, die in die Rollengruppen definiert die `Users` Parameter suchen kann. Für Compliance-Grenzen *ComplianceAttribute* die gleichen Attribute, die Sie in Schritt 1 identifiziert und *AttributeValue* gibt Behörde. Dieser Filter ermöglicht Mitgliedern der Rollengruppe nur die Postfächer in einer bestimmten Agency durchsuchen; beispielsweise `"Mailbox_Department -eq 'FourthCoffee'"` . 
    
  -  `Site`-Gibt an, die OneDrive-Konten, die in die Rollengruppen definiert die `Users` Parameter suchen kann. Verwenden Sie die Zeichenfolge für den Filter OneDrive `ComplianceAttribute`; Dies wird ordnen Sie die gleichen, die Sie in Schritt 1 identifiziert wird, die mit OneDrive Konten aufgrund der Support-Anforderung, die Sie in Schritt2 übermittelt synchronisiert;  *AttributeValue* gibt Behörde an. Dieser Filter ermöglicht Mitgliedern der Rollengruppe die Konten OneDrive nur in einer bestimmten Agency durchsuchen; beispielsweise `"Site_ComplianceAttribute -eq 'FourthCoffee'"`.
    
  -  `Site_Path`-Gibt an, die SharePoint-Websites, die in die Rollengruppen definiert die `Users` Parameter suchen kann. Die *SharePointURL* gibt die Websites in der Behörde, die Mitglieder der Rollengruppe suchen können. Zum Beispiel`Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`
    
-  `Action`-Gibt den Typ des Compliance Search-Aktion, die auf der Filter angewendet wird. Beispielsweise `-Action Search` den Filter würde nur angewendet werden, wenn Mitglieder der Rollengruppen in definiert die `Users` Parameter wird eine Inhaltssuche ausgeführt. In diesem Fall würde nicht der Filter angewendet werden, wenn Suchergebnisse exportieren. Verwenden Sie für Compliance-Grenzen `-Action All` damit alle Aktionen für Suchen der Filter angewendet wird. 
    
    Eine Liste der Aktionen Inhaltssuche finden Sie im Abschnitt "New-ComplianceSecurityFilter" [Konfigurieren von Berechtigungen für Inhaltssuche Filtern](permissions-filtering-for-content-search.md#new-compliancesecurityfilter).
    
Es folgen Beispiele für die beiden Berechtigungen Suchfilter, die zur Unterstützung der Contoso-Szenario für die Einhaltung von Bestimmungen Grenzen erstellt werden.
  
 **Fourth Coffee**

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 **Coho Winery**

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-an-intra-agency-investigations"></a>Schritt 5: Erstellen Sie einen eDiscovery-Fall für ein Intra-Agency Untersuchungen

Der letzte Schritt ist die Erstellung einen neuen eDiscovery-Fall in das Wertpapier &amp; Compliance Center, und fügen Sie die Rollengruppe –, die Sie in Schritt 3 erstellte – als Mitglied der Groß-/Kleinschreibung. Dies führt zu zwei wesentliche Merkmale der Verwendung von Compliance-Grenzen:
  
- Nur Mitglieder der Rollengruppe die Groß-/Kleinschreibung hinzugefügt können werden, finden Sie unter und Zugreifen auf die Groß-/Kleinschreibung in das Wertpapier &amp; Compliance Center. Angenommen, wenn die Rollengruppe Fourth Coffee Prüfer des einzigen Elements der Fall ist, möglich nicht dann Mitglieder der Gruppe von Fourth Coffee eDiscovery-Manager-Rolle (oder eine beliebige andere Rollengruppe) finden Sie unter oder Zugriff auf die Groß-/Kleinschreibung.
    
- Wenn ein Mitglied der Rollengruppe zugewiesen sind, in eine Anfrage eine zugeordneten Suche dem der Groß-/Kleinschreibung ausgeführt wird, werden sie nur die Speicherorte für Inhalte innerhalb ihrer Behörde suchen (definiert durch den Suchfilter für Berechtigungen, die Sie in Schritt 4 erstellt haben.)


So erstellen Sie einen neuen Fall und Mitglieder zuweisen:
    
1. Wechseln Sie zu der Seite **eDiscovery** in das Wertpapier &amp; Compliance Center, und erstellen Sie eine neue Anfrage. 
    
2. Klicken Sie in der Liste der eDiscovery-Fälle auf den Namen der die Anfrage, die Sie gerade erstellt haben.
    
3. Klicken Sie auf der Seite **Verwalten in diesem Fall** flyoutmenü unter **des Umgangs mit Rollengruppen** ![Symbol hinzufügen](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **Hinzufügen**.
    
    ![Hinzufügen einer Rollengruppe als Mitglied einer eDiscovery-Fall](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. Wählen Sie in der Liste mit Rollengruppen eine der Rollengruppen, die Sie in Schritt 3 erstellt haben, und klicken Sie auf **Hinzufügen**.
    
5. Klicken Sie auf **Speichern** , auf die flyoutmenü **in diesem Fall verwalten** , um die Änderung zu speichern. 

## <a name="compliance-boundary-limitations"></a>Compliance-Grenze Einschränkungen

Beachten Sie die folgenden Einschränkungen beim Verwalten von eDiscovery-Fälle und Untersuchungen, mit denen der Compliance-Grenzen.
  
- Beim Erstellen und Ausführen einer Suche Inhalte, können Sie die Speicherorte für Inhalte auswählen, die sich außerhalb Ihrer Behörde befinden. Aufgrund der Suchfilter Berechtigungen werden nicht-Inhalten in diese Standorte in den Suchergebnissen enthalten sein.
    
- Compliance-Grenzen nicht auf Haltebereiche in eDiscovery-Fälle angewendet. Dies bedeutet, dass einen Benutzer ein eDiscovery-Manager in eine Stelle in einer anderen Behörde in der Warteschleife platziert werden kann. Die Grenze für die Einhaltung von Bestimmungen wird jedoch erzwungen werden, wenn der eDiscovery-Manager des Benutzers die Speicherorte für Inhalte durchsucht, die in die Warteschleife gestellt wurde. Bedeutet dies, dass der eDiscovery-Manager wird nicht sein können Suche Speicherorte für Inhalte des Benutzers, halten, obwohl er auf den Benutzer platzieren konnte.
    
    Halten Sie darüber hinaus, dass nur Statistiken für Speicherorte für Inhalte in Behörde gelten.
    
- Suchfilter Berechtigungen sind nicht auf Öffentliche Ordner von Exchange angewendet.

## <a name="searching-and-exporting-sharepoint-content-in-multi-geo-environments"></a>Suchen und Exportieren von SharePoint-Inhalten in Umgebungen mit mehreren geografisch

Suchfilter Berechtigungen können auch steuern, in denen Weiterleitung von Inhalten für den Export und SharePoint-Websites und OneDrive-Konten in einer [Umgebung mit SharePoint Multi-Geo](https://go.microsoft.com/fwlink/?linkid=860840)durchsucht welche Rechenzentren werden können:
  
- Exportieren von Suchergebnissen aus einem bestimmten-Rechenzentrum. Dies bedeutet, dass Sie angeben können, dass der Speicherort, dass die Suche im Rechenzentrum, die Ergebnisse aus exportiert werden.
    
- Leiten Sie Suchvorgänge in SharePoint-Websites und OneDrive-Konten in einem Rechenzentrum Satelliten. Dies bedeutet, dass Sie den Speicherort des Data Center angeben können dem Suchvorgänge ausgeführt wird.
    
Verwenden Sie **den Bereichsparameter** für **Neu ComplianceSecurityFilter** oder **Set-ComplianceSecurityFilter** -Cmdlets zum Erstellen oder ändern, welche der Export über weitergeleitet werden, Datacenter.
  
|**Übergebener Wert**|**Zentrale Rechenzentrum**|
|:-----|:-----|
|NAM  <br/> |Nordamerika (tatsächlichen Daten, die Ressourcen in den USA sind)  <br/> |
|EUR  <br/> |Europa  <br/> |
|APC  <br/> |Asien-Pazifik  <br/> |
|CAN <br/> |Kanada
   
In ähnlicher Weise können Sie die folgenden Werte für die **Region** Parameterwerte welche Rechenzentrum steuern, die Content-Suche in ausgeführt wird, bei der Suche von SharePoint und OneDrive-Speicherorte. Beachten Sie, dass welche Rechenzentrum auch in der folgenden Tabelle sind Exporte über weitergeleitet werden. 
  
|**Übergebener Wert**|**Routing Speicherorte für den Export im Rechenzentrum**|
|:-----|:-----|
|NAM  <br/> |US  <br/> |
|EUR  <br/> |Europa  <br/> |
|APC  <br/> |Asien-Pazifik  <br/> |
|CAN  <br/> |US  <br/> |
|AUS  <br/> |Asien-Pazifik  <br/> |
|KOR  <br/> |Die Organisation Standard-Rechenzentrum  <br/> |
|GBR  <br/> |Europa  <br/> |
|JPN  <br/> |Asien-Pazifik  <br/> |
|IND  <br/> |Asien-Pazifik  <br/> |
|LAM  <br/> |US  <br/> |
   
 **Hinweis:** Wenn Sie den Bereichsparameter für ein Suchfilter Berechtigungen nicht angeben, werden Suchergebnisse vom nächsten Rechenzentrum exportiert. 
  
Es folgen Beispiele für die Verwendung der **-Region** Parameter beim Erstellen von Suchfiltern der Berechtigung für Compliance-Grenzen. Hierbei wird davon ausgegangen, dass das Fourth Coffee Subsidiary sich in Nordamerika befindet und Europa Coho Winery wird. 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
Behalten Sie Folgendes beachten Sie beim Durchsuchen und Exportieren von SharePoint und OneDrive in Umgebungen mit mehreren geografisch Content.
  
- Der Parameter **Region** steuern nicht Suchvorgänge in Exchange-Postfächern. Alle Rechenzentren werden durchsucht werden, wenn Sie Postfächer suchen. Verwenden Sie zum Einschränken von der Exchange-Postfächer durchsucht werden können, des **Filter** -Parameters beim Erstellen oder Ändern eines Suchfilters Berechtigungen. 
    
- Wenn es für ein eDiscovery-Suche über mehrere SharePoint-Regionen Manager erforderlich ist, müssen Sie ein anderen Benutzerkontos für diese eDiscovery-Manager, der verwendet werden kann im Suchfilter Berechtigungen an die alternative Region erstellen, in dem die SharePoint-Websites oder OneDrive Konten befinden.
    
- Bei der Suche nach Inhalten in SharePoint und OneDrive weist **der Bereichsparameter** Suchvorgänge nach entweder im Hauptfenster oder Satelliten-Speicherort, in dem der eDiscovery-Manager eDiscovery Untersuchungen durchführen wird. Wenn ein eDiscovery-Manager SharePoint und OneDrive Websites außerhalb der Region, die in den Suchfilter Berechtigungen angegeben ist sucht, werden keine Suchergebnisse zurückgegeben werden soll. 
    
- Beim Exportieren von Suchergebnissen wird Inhalt aus allen Speicherorte für Inhalte (einschließlich Exchange, Skype für Business, SharePoint, OneDrive und andere Office 365-Dienste, die Sie mithilfe der Suchfunktion von Inhalten suchen können) hochgeladen werden, an die Position der Azure-Speicher in der Rechenzentrum, das durch den Parameter **Region** angegeben ist. Dadurch Organisationen innerhalb Compliance bleiben, indem nicht zulassen Inhalte über gesteuerte Grenzen hinweg exportiert werden sollen. Wenn keine Region im Suchfilter Berechtigungen angegeben wird, wird der Inhalt in der Organisation als Standard Bereich hochgeladen. 
    
- Sie können einen vorhandenen Suchfilter Berechtigungen zum Hinzufügen oder ändern den Bereich mithilfe des folgenden Befehls bearbeiten:

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

 **Wer können erstellen und Verwalten von Berechtigungen Suchfilter (mit Set-ComplianceSecurityFilter-Cmdlets und New-ComplianceSecurityFilter)?**
  
Zum Erstellen, anzeigen und ändern Sie Suchfilter Berechtigungen haben, müssen Sie ein Mitglied der Rollengruppe "Organisationsverwaltung" in das Wertpapier sein &amp; Compliance Center.
  
 **Wenn ein eDiscovery-Manager für mehr als eine Rollengruppe, die mehrere Behörden umfasst zugewiesen ist, wie Suchen sie für Inhalte in eine Stelle oder anderen?**
  
Der eDiscovery-Manager kann Parameter ihre Suchabfrage hinzufügen, die einer bestimmten Stelle für die Suche einschränken. Beispielsweise wenn eine Organisation die **CustomAttribute10** -Eigenschaft, um die Unterscheidung von Behörden angegeben, sie können fügen Sie die folgenden an ihre Suchabfrage Postfächern und OneDrive-Konten in einer bestimmten Agency durchsuchen: `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`.
  
 **Was passiert, wenn der Wert des Attributs, das verwendet wird, wie das Compliance-Attribut im Suchfilter Berechtigungen geändert wird?**
  
Es dauert bis zu drei Tage für ein Suchfilter Berechtigungen, die Einhaltung von Bestimmungen Grenze zu erzwingen, wenn der Wert des Attributs, das im Filter verwendet wird, geändert wird. Beispielsweise im Contoso-Szenario angenommen, dass ein Benutzer in der Behörde Fourth Coffee Coho Winery Behörde übertragen wird. Daher wird der Wert des Attributs **Abteilung** für das Benutzerobjekt aus *FourthCoffee* in *CohoWinery* geändert. In diesem Fall erhalten Fourth Coffee eDiscovery und Anleger Suchergebnisse für diesen Benutzer für um drei Tage nach das Attribut geändert wird. In ähnlicher Weise dauert bis zu drei Tage vor Coho Winery eDiscovery-Manager und Prüfer erhalten Suchergebnisse für den Benutzer. 
  
 **Kann ein eDiscovery-Manager die Inhalte von zwei separaten Grenzen anzeigen?**
  
Ja. Dies kann durch Hinzufügen des Benutzers zu Rollengruppen, die Sichtbarkeit auf beide Behörden erfolgen.
  
 **Führen Sie Berechtigungen Filter Arbeit für eDiscovery Groß-/Kleinschreibung Haltestatus, Office 365-Aufbewahrungsrichtlinien oder DLP suchen?**
  
Nein, nicht zu diesem Zeitpunkt
  
 **Wenn ich eine Region für die Steuerung angeben, wobei Inhalt exportiert, jedoch nicht mir einer SharePoint-Organisation in diesem Bereich, kann ich noch SharePoint suchen?**
  
Wenn die Region gemäß den Suchfilter Berechtigungen in Ihrer Organisation nicht vorhanden ist, wird die standardmäßige Region gesucht werden soll.
  
 **Was ist die maximale Anzahl der Berechtigungen Suchfilter, die in einer Organisation erstellt werden können?**
  
Es gibt keine Begrenzung der Anzahl der Berechtigungen Suchfilter, die in einer Organisation erstellt werden können. Suchleistung wird jedoch beeinträchtigt werden, wenn mehr als 100 Suchfilter Berechtigungen vorhanden sind. Um die Anzahl der Suchfilter Berechtigungen in Ihrer Organisation so gering wie möglich zu halten, erstellen Sie Filter, die Regeln für Exchange, SharePoint und OneDrive in einer einzelnen Berechtigungen Suchfilter möglichst zu kombinieren.
