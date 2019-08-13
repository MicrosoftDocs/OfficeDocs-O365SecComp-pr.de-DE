---
title: Einrichten von Compliance-Grenzen für eDiscovery-Untersuchungen in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
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
description: Verwenden Sie Kompatibilitäts Grenzen zum Erstellen von logischen Grenzen in einer Office 365 Organisation, die die Benutzerinhalts Speicherorte steuern, die ein eDiscovery-Manager durchsuchen kann. Compliance-Grenzen verwenden Such Berechtigungs Filterung (auch als Compliance-Sicherheitsfilter bezeichnet), um zu steuern, welche Postfächer, SharePoint-Websites und OneDrive-Konten von bestimmten Benutzern durchsucht werden können.
ms.openlocfilehash: 44c157b8f155755c6a48830231074643a830f498
ms.sourcegitcommit: 226adb6d05015da16138b315dd2f5b937bf4354d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2019
ms.locfileid: "36302424"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a>Einrichten von Compliance-Grenzen für eDiscovery-Untersuchungen in Office 365

Compliance-Grenzen erstellen logische Grenzen in einer Office 365 Organisation, die die Benutzerinhalts Speicherorte (wie Postfächer, SharePoint-Websites und OneDrive-Konten) steuert, die eDiscovery-Manager durchsuchen können. Außerdem steuern Compliance-Grenzen, wer auf eDiscovery-Fälle zugreifen kann, die zur Verwaltung der rechtlichen, personellen oder sonstigen Untersuchungen in Ihrer Organisation verwendet werden. Die Notwendigkeit von Compliance-Grenzen ist häufig für multinationale Unternehmen erforderlich, die geografische und behördliche Bestimmungen respektieren müssen, und für Regierungen, die häufig in verschiedene Agenturen aufgeteilt sind. In Office 365 helfen Compliance-Grenzen bei der Durchführung von Inhalts suchen und der Verwaltung von Untersuchungen mit eDiscovery-Fällen bei der Erfüllung dieser Anforderungen.
  
Wir verwenden das Beispiel in der folgenden Abbildung, um zu erläutern, wie Kompatibilitäts Grenzen funktionieren.
  
![Compliance-Grenzen bestehen aus Such Berechtigungs filtern, die den Zugriff auf Agenturen und Administratorrollengruppen steuern, mit denen der Zugriff auf eDiscovery-Fälle gesteuert wird](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
In diesem Beispiel ist Contoso Ltd eine Office 365 Organisation, die aus zwei Niederlassungen, Fourth Coffee und dem Weingut Winery besteht. Das Unternehmen erfordert, dass eDiscovery-Manager und Ermittler nur die Exchange-Postfächer, OneDrive-Konten und SharePoint-Websites in Ihrer Agentur durchsuchen können. Außerdem können eDiscovery-Manager und Ermittler nur eDiscovery-Fälle in Ihrer Agentur anzeigen, und Sie können nur auf die Fälle zugreifen, in denen Sie Mitglied sind. Hier erfahren Sie, wie Compliance-Grenzen diese Anforderungen erfüllen.
  
- Die Suchberechtigungen-Filterfunktion in der Inhaltssuche steuert die inhaltsspeicherorte, die eDiscovery-Manager und-Prüfer durchsuchen können. Dies bedeutet, dass eDiscovery-Manager und Ermittler in der vierten Coffee Agency nur inhaltsspeicherorte in der vierten Coffee-Niederlassung durchsuchen können. Die gleiche Einschränkung gilt für die Weingut-Tochter.
    
    Rollengruppen steuern, wer die eDiscovery-Fälle im Security #a0 Compliance Center anzeigen kann. Dies bedeutet, dass eDiscovery-Manager und Ermittler nur die eDiscovery-Fälle in Ihrer Agentur anzeigen können.
    
- Rollengruppen steuern außerdem, wer einem eDiscovery-Fall Mitglieder zuweisen kann. Dies bedeutet, dass eDiscovery-Manager und Ermittler nur Mitglieder für Fälle zuweisen können, in denen Sie selbst Mitglied sind.
    
Hier ist der Prozess zum Einrichten von Kompatibilitäts Grenzen:
  
[Schritt 1: Identifizieren eines Benutzer Attributs zur Definition ihrer Agenturen](#step-1-identify-a-user-attribute-to-define-your-agencies)

[Schritt 2: Datei eine Anforderung mit dem Microsoft-Support, um das Benutzerattribut mit OneDrive-Konten zu synchronisieren](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[Schritt 3: Erstellen einer Rollengruppe für jede Agentur](#step-3-create-a-role-group-for-each-agency)

[Schritt 4: Erstellen eines Such Berechtigungs Filters zum Erzwingen der Konformitäts Grenze](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[Schritt 5: Erstellen eines eDiscovery-Falls für eine Intra-Agency-Untersuchung](#step-5-create-an-ediscovery-case-for-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a>Schritt 1: Identifizieren eines Benutzer Attributs zur Definition ihrer Agenturen

Der erste Schritt besteht darin, ein zu verwendender Azure Active Directory-Attribut auszuwählen, mit dem Ihre Agenturen definiert werden. Dieses Attribut wird verwendet, um den Such Berechtigungsfilter zu erstellen, mit dem ein eDiscovery-Manager so eingeschränkt wird, dass nur die inhaltsspeicherorte von Benutzern durchsucht werden, denen ein bestimmter Wert für dieses Attribut zugewiesen ist. Angenommen, Contoso entscheidet, das **Department** -Attribut zu verwenden. Der Wert für dieses Attribut für Benutzer in der vierten Coffee `FourthCoffee` -Tochtergesellschaft wäre und der Wert für die Benutzer in der Weingut-Tochter `CohoWinery`Gesellschaft. In Schritt 4 verwenden Sie dieses `attribute:value` Paar (beispielsweise *Department: fourthcoffee*), um die Benutzerinhalts Speicherorte zu begrenzen, die eDiscovery-Manager durchsuchen können. 
  
Im folgenden finden Sie eine Liste der Azure Active Directory Benutzerattribute, die Sie für Kompatibilitäts Grenzen verwenden können:
  
- Company
    
- CustomAttribute1 – CustomAttribute15
    
- Abteilung
    
- Büro

- C (zweistelliger Landes Code)
    
Obwohl mehr Benutzerattribute verfügbar sind, insbesondere für Exchange-Postfächer, sind die oben aufgeführten Attribute die einzigen, die derzeit von OneDrive unterstützt werden.
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a>Schritt 2: Datei eine Anforderung mit dem Microsoft-Support, um das Benutzerattribut mit OneDrive-Konten zu synchronisieren

Im nächsten Schritt wird eine Anforderung mit dem Microsoft-Support gespeichert, um das Azure Active Directory-Attribut zu synchronisieren, das Sie in Schritt 1 für alle OneDrive-Konten in Ihrer Organisation ausgewählt haben. Nach dieser Synchronisierung wird das Attribut (und sein Wert), das Sie in Schritt 1 ausgewählt haben, einer ausgeblendeten verwalteten Eigenschaft in SharePoint namens `ComplianceAttribute`zugeordnet. Sie verwenden dieses Attribut, um den Such Berechtigungsfilter für OneDrive in Schritt 4 zu erstellen.
  
Schließen Sie die folgenden Informationen ein, wenn Sie die Anforderung an den Microsoft-Support übermitteln:
  
- Der Standarddomänenname Ihrer Office 365 Organisation
    
- Der Name des Azure Active Directory-Attributs (aus Schritt 1)
    
- Der folgende Titel oder die Beschreibung des Zwecks der Supportanforderung: "aktivieren Sie OneDrive für Unternehmen Synchronisierung mit Azure Active Directory für Compliance-Sicherheitsfilter". Dadurch wird die Anforderung an das Office 365 eDiscovery-Entwicklungsteam weitergeleitet, das die Anforderung implementiert.
    
Nachdem die technische Änderung vorgenommen wurde und das Attribut mit OneDrive synchronisiert wurde, sendet der Microsoft-Support Ihnen die Buildnummer, in der die Änderung vorgenommen wurde, und ein geschätztes Bereitstellungsdatum. Der Bereitstellungsprozess dauert in der Regel 4 bis 6 Wochen, nachdem Sie die Supportanfrage gesendet haben.
  
 **Wichtig:** Sie können Schritt 3 bis Schritt 5 abschließen, bevor die Änderung bereitgestellt wird. Durch die Ausführung von Inhalts suchen werden jedoch keine Dokumente von OneDrive-Websites zurückgegeben, die im Such Berechtigungsfilter angegeben sind, bis die Änderung bereitgestellt wurde. 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a>Schritt 3: Erstellen einer Rollengruppe für jede Agentur

Der nächste Schritt besteht darin, die Rollengruppen im Security #a0 Compliance Center zu erstellen, das mit ihren Agenturen in Einklang steht. Es wird empfohlen, eine Rollengruppe zu erstellen, indem Sie die integrierte eDiscovery-Manager-Gruppe kopieren, die entsprechenden Mitglieder hinzufügen und Rollen entfernen, die möglicherweise nicht auf Ihre Anforderungen zutreffen. Weitere Informationen zu eDiscovery-bezogenen Rollen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office 365 Security #a0 Compliance Center](assign-ediscovery-permissions.md).
  
Zum Erstellen der Rollengruppen wechseln Sie zur Seite **Berechtigungen** im Security #a0 Compliance Center, und erstellen Sie eine Rollengruppe für jedes Team in jeder Agentur, die Compliance-Grenzen und eDiscovery-Fälle zum Verwalten von Untersuchungen verwenden wird. 
  
Im Szenario Contoso-Konformitäts Grenzen müssen vier Rollengruppen erstellt werden, denen jeweils die entsprechenden Mitglieder hinzugefügt werden.
  
- Vierter Kaffee eDiscovery-Manager
    
- Vierter Kaffee Ermittler
    
- EDiscovery-Manager für Weingut
    
- Weingut Forscher
  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a>Schritt 4: Erstellen eines Such Berechtigungs Filters zum Erzwingen der Konformitäts Grenze

Nachdem Sie für jede Agentur Rollengruppen erstellt haben, besteht der nächste Schritt darin, die Such Berechtigungsfilter zu erstellen, die jede Rollengruppe ihrer spezifischen Agentur zuordnen und die Konformitäts Grenze selbst definiert. Sie müssen für jede Agentur einen Such Berechtigungsfilter erstellen. Weitere Informationen zum Erstellen von Sicherheits Berechtigungs Filtern finden Sie unter [Konfigurieren der Berechtigungs Filterung für die Inhaltssuche](permissions-filtering-for-content-search.md).
  
Hier ist die Syntax, die verwendet wird, um einen Such Berechtigungsfilter zu erstellen, der für Kompatibilitäts Grenzen verwendet wird.

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<ComplianceAttribute>  -eq '<AttributeVale> '", "Site_<ComplianceAttribute>  -eq '<AttributeValue>' -or Site_Path -like '<SharePointURL>*'" -Action <Action >
```
  
Im folgenden finden Sie eine Beschreibung der einzelnen Parameter im Befehl:
  
-  `FilterName`: Gibt den Namen des Filters an. Verwenden Sie einen Namen, der die Agentur beschreibt oder identifiziert, in der der Filter verwendet wird. 
    
-  `Users`: Gibt die Benutzer oder Gruppen an, die diesen Filter auf die durchgeführten Inhalts Suchaktionen anwenden. Für Kompatibilitäts Grenzen gibt dieser Parameter die Rollengruppen (die Sie in Schritt 3 erstellt haben) in der Agentur an, für die Sie den Filter erstellen. Hinweis Hierbei handelt es sich um einen mehrwertigen Parameter, mit dem Sie eine oder mehrere Rollengruppen, getrennt durch Kommas, einbinden können. 
    
-  `Filters`: Gibt die Suchkriterien für den Filter an. Für die Konformitäts Grenzen definieren Sie die folgenden Filter. Jeder wird auf einen Inhaltsspeicherort angewendet. 
    
    -  `Mailbox`: Gibt die Postfächer an, die die im `Users` Parameter definierten Rollengruppen durchsuchen können. Für Kompatibilitäts Grenzen ist *complianceattribute* das gleiche Attribut, das Sie in Schritt 1 identifiziert haben, und *Attribut* Wert gibt die Agentur an. Mit diesem Filter können Mitglieder der Rollengruppe nur die Postfächer in einer bestimmten Agentur durchsuchen. Beispiel: `"Mailbox_Department -eq 'FourthCoffee'"`. 
    
    -  `Site`: Gibt die OneDrive-Konten an, die die im `Users` Parameter definierten Rollengruppen durchsuchen können. Verwenden Sie für den OneDrive-Filter die tatsächliche `ComplianceAttribute`Zeichenfolge. Dies entspricht dem Attribut, das Sie in Schritt 1 identifiziert haben und das mit OneDrive-Konten als Ergebnis der in Schritt 2 übermittelten Supportanforderung synchronisiert wird.  *Attributvalue* gibt die Agentur an. Mit diesem Filter können Mitglieder der Rollengruppe nur die OneDrive-Konten in einer bestimmten Agentur durchsuchen. Beispiel: `"Site_ComplianceAttribute -eq 'FourthCoffee'"`.
    
    -  `Site_Path`: Gibt die SharePoint-Websites an, die die im `Users` Parameter definierten Rollengruppen durchsuchen können. Das *SharePointURL* gibt die Websites in der Agentur an, die Mitglieder der Rollengruppe durchsuchen können. Beachten Sie Beispiels `"Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"` Weise, `Site` dass `Site_Path` die und-Filter durch einen **-oder-** Operator verbunden sind.
    
     > [!NOTE]
     > Die Syntax für den `Filters` Parameter enthält eine *Filterliste*. Eine Filterliste ist ein Filter, der einen Post Fach Filter und einen Website Filter enthält, der durch ein Komma getrennt ist. Beachten Sie im vorherigen Beispiel, dass durch ein Komma **Mailbox_ComplianceAttribute** und **Site_ComplianceAttribute**getrennt werden `-Filters "Mailbox_<ComplianceAttribute>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq '<AttributeValue>' -or Site_Path -like '<SharePointURL>*'"`:. Wenn dieser Filter während der Ausführung einer Inhaltssuche verarbeitet wird, werden zwei Such Berechtigungsfilter aus der Liste Filter erstellt: ein Post Fach Filter und ein Website Filter. Eine Alternative zur Verwendung einer Filterliste besteht darin, zwei separate Such Berechtigungsfilter für jede Agentur zu erstellen: einen Such Berechtigungsfilter für das Postfachattribut und einen Filter für die Website Attribute. In beiden Fällen sind die Ergebnisse identisch. Die Verwendung einer Filterliste oder das Erstellen separater Such Berechtigungsfilter ist eine Frage der Präferenz.

-  `Action`: Gibt die Art der Konformitäts Suchaktion an, auf die der Filter angewendet wird. Beispielsweise würde `-Action Search` der Filter nur angewendet, wenn Mitglieder der Rollengruppe, die im `Users` Parameter definiert sind, eine Inhaltssuche ausführen. In diesem Fall würde der Filter beim Exportieren von Suchergebnissen nicht angewendet. Verwenden Sie `-Action All` für Kompatibilitäts Grenzen den Filter, damit dieser auf alle Suchaktionen angewendet wird. 
    
    Eine Liste der Inhalts Suchaktionen finden Sie im Abschnitt "New-ComplianceSecurityFilter" unter Konfigurieren der [Berechtigungs Filterung für die Inhaltssuche](permissions-filtering-for-content-search.md#new-compliancesecurityfilter).

Im folgenden sind Beispiele für die beiden Such Berechtigungsfilter aufgeführt, die zur Unterstützung des Szenarios "Contoso-Konformitäts Grenzen" erstellt würden. Beide Beispiele enthalten eine Liste mit Trennzeichen getrennten filtern, in der die Post Fach-und Website Filter im gleichen Such Berechtigungsfilter enthalten sind und durch ein Komma getrennt werden.
  
 **Vierter Kaffee**

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 **Weingut Winery**

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-intra-agency-investigations"></a>Schritt 5: Erstellen eines eDiscovery-Falls für Intra-Agency-Untersuchungen

Der letzte Schritt besteht darin, einen eDiscovery-Fall im Security #a0 Compliance Center zu erstellen und dann die Rollengruppe hinzuzufügen, die Sie in Schritt 3 als Mitglied der Anfrage erstellt haben. Dies führt zu zwei wichtigen Merkmalen der Verwendung von Kompatibilitäts Grenzen:
  
- Nur Mitglieder der Rollengruppe, die dem Fall hinzugefügt werden, können den Fall im Security #a0 Compliance Center anzeigen und darauf zugreifen. Wenn beispielsweise die Fourth Coffee Investigators-Rollengruppe das einzige Mitglied eines Falles ist, können Mitglieder der vierten Coffee-eDiscovery-Manager-Rollengruppe (oder Mitglieder einer anderen Rollengruppe) den Fall nicht sehen oder auf diese zugreifen.
    
- Wenn ein Mitglied der Rollengruppe, das einem Fall zugewiesen ist, eine mit dem Fall verknüpfte Suche ausführt, können die inhaltsspeicherorte in Ihrer Agentur nur durchsucht werden (Dies ist durch den Such Berechtigungsfilter definiert, den Sie in Schritt 4 erstellt haben).


So erstellen Sie eine Anfrage und weisen Mitglieder zu:
    
1. Wechseln Sie zur Seite **eDiscovery** im Security #a0 Compliance Center, und erstellen Sie einen Fall. 
    
2. Klicken Sie in der Liste der eDiscovery-Fälle auf den Namen des von Ihnen erstellten Falls.
    
3. Klicken Sie auf der Seite **diesen Fall Flyout verwalten** unter **Rollengruppen verwalten**auf ![Symbol](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **hinzu**fügen.
    
    ![Hinzufügen einer Rollengruppe als Mitglied eines eDiscovery-Falls](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. Wählen Sie in der Liste der Rollengruppen eine der Rollengruppen aus, die Sie in Schritt 3 erstellt haben, und klicken Sie auf **Hinzufügen**.
    
5. Klicken Sie im Flyout **dieses Fall verwalten** auf **Speichern** , um die Änderung zu speichern. 

## <a name="compliance-boundary-limitations"></a>Einschränkungen bei der Konformitäts Begrenzung

Beachten Sie beim Verwalten von eDiscovery-Fällen und Untersuchungen zur Verwendung von Compliance-Grenzen die folgenden Einschränkungen.
  
- Beim Erstellen und Durchführen einer Inhaltssuche können Sie inhaltsspeicherorte auswählen, die sich außerhalb Ihrer Agentur befinden. Aufgrund des Such Berechtigungs Filters werden Inhalte dieser Speicherorte jedoch nicht in die Suchergebnisse einbezogen.
    
- Compliance-Grenzen gelten nicht für Aufbewahrungen in eDiscovery-Fällen. Das bedeutet, dass ein eDiscovery-Manager in einer Agentur einen Benutzer in einer anderen Agentur in der Warteschleife platzieren kann. Die Konformitäts Grenze wird jedoch erzwungen, wenn der eDiscovery-Manager die inhaltsspeicherorte des Benutzers durchsucht, der in der Warteschleife gespeichert wurde. Das bedeutet, dass der eDiscovery-Manager nicht in der Lage ist, die inhaltsspeicherorte des Benutzers zu durchsuchen, obwohl er den Benutzer in der Warteschleife platzieren konnte.
    
    Darüber hinaus gelten die Aufbewahrungs Statistiken nur für inhaltsspeicherorte in der Agentur.
    
- Such Berechtigungsfilter werden nicht auf öffentliche Exchange-Ordner angewendet.

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a>Suchen und Exportieren von Inhalten in Multi-Geo-Umgebungen

Mit Such Berechtigungs filtern können Sie auch steuern, wohin Inhalte für den Export weitergeleitet werden und welches Rechenzentrum beim Durchsuchen von Inhaltsspeicherorten in einer [SharePoint-Multi-Geo-Umgebung](https://go.microsoft.com/fwlink/?linkid=860840)durchsucht werden kann.
  
- **Exportieren von Suchergebnissen:** Sie können die Suchergebnisse aus Exchange-Postfächern, SharePoint-Websites und OneDrive-Konten aus einem bestimmten Datencenter exportieren. Dies bedeutet, dass Sie den Speicherort des Rechenzentrums angeben können, aus dem Suchergebnisse exportiert werden.

    Verwenden Sie den Parameter **Region** für **New-ComplianceSecurityFilter** oder **ComplianceSecurityFilter** Cmdlets, um zu erstellen oder zu ändern, durch welche Datencenter der Export weitergeleitet wird.
  
    |**Übergebener Wert**|**Speicherort des Datencenters**|
    |:-----|:-----|
    |NAM  <br/> |Nordamerika (Rechenzentren befinden sich in den USA)  <br/> |
    |EUR  <br/> |Europa  <br/> |
    |APC  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |CAN <br/> |Kanada|
    |||
    
- **Routen von Inhalts suchen:** Sie können die Inhaltssuche von SharePoint-Websites und OneDrive-Konten an ein Satellitendaten Center weiterleiten. Dies bedeutet, dass Sie den Speicherort des Rechenzentrums angeben können, in dem Suchvorgänge ausgeführt werden.
    
    Verwenden Sie die folgenden Werte für die **Region** -Parameterwerte, um zu steuern, in welchem Datencenter die Inhaltssuche ausgeführt wird, wenn Sie SharePoint-Websites und OneDrive-Speicherorte durchsuchen. 
  
    |**Übergebener Wert**|**Rechenzentrums-Routing Speicherorte für SharePoint**|
    |:-----|:-----|
    |NAM  <br/> |Uns  <br/> |
    |EUR  <br/> |Europa  <br/> |
    |APC  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |CAN  <br/> |Uns  <br/> |
    |AUS  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |KOR  <br/> |Das standardmäßige Rechenzentrum der Organisation  <br/> |
    |GBR  <br/> |Europa  <br/> |
    |JPN  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |IND  <br/> |Asiatisch-pazifischer Raum  <br/> |
    |Lam  <br/> |Uns  <br/> |
    |||

   Wenn Sie den Parameter **Region** nicht für einen Such Berechtigungsfilter angeben, wird die standardmäßige SharePoint-Region der Organisation durchsucht, dann werden Suchergebnisse in das nächstgelegene Datencenter exportiert.

> [!TIP]
> Zur Vereinfachung des Konzepts steuert der **Region** -Parameter das Rechenzentrum, das zum Suchen von Inhalten in SharePoint und OneDrive verwendet wird. Dies gilt nicht für die Suche nach Inhalten in Exchange, da Exchange-Inhalts suchen nicht an den geografischen Standort von Rechenzentren gebunden sind. Außerdem kann der gleiche **Regions** Parameterwert auch das Rechenzentrum diktieren, durch das die Exporte weitergeleitet werden. Dies ist häufig erforderlich, um die Verlagerung von Daten über geografische Grenzen hinweg zu steuern.<br/><br/>Wenn Sie Advanced eDiscovery verwenden, ist die Suche nach Inhalten in SharePoint und OneDrive nicht an den geografischen Standort von Rechenzentren gebunden. Weitere Informationen zu Advanced eDiscovery finden Sie unter [Übersicht über die erweiterte eDiscovery-Lösung in Microsoft 365](compliance20/overview-ediscovery-20.md).

Im folgenden finden Sie Beispiele für die Verwendung des **Region** -Parameters beim Erstellen von Such Berechtigungs Filtern nach Kompatibilitäts Grenzen. Dabei wird davon ausgegangen, dass sich die Fourth Coffee-Tochtergesellschaft in Nordamerika befindet und dass sich die Weinkellerei in Europa befindet. 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
Beachten Sie beim Suchen und Exportieren von Inhalten in Multi-Geo-Umgebungen die folgenden Aspekte.
  
- Der **Region** -Parameter steuert keine Suche von Exchange-Postfächern. Alle Rechenzentren werden durchsucht, wenn Sie Postfächer durchsuchen. Wenn Sie den Bereich, in dem Exchange-Postfächer durchsucht werden können, einschränken möchten, verwenden Sie den Parameter **Filters** beim Erstellen oder Ändern eines Such Berechtigungs Filters. 
    
- Wenn es für einen eDiscovery-Manager erforderlich ist, in mehreren SharePoint-Regionen zu suchen, müssen Sie für diesen eDiscovery-Manager ein anderes Benutzerkonto erstellen, das im Such Berechtigungsfilter verwendet werden kann, um die Alternative Region anzugeben, in der die SharePoint Standorte oder OneDrive-Konten befinden sich.
    
- Bei der Suche nach Inhalten in SharePoint und OneDrive leitet der Parameter **Region** die Suche entweder an den Haupt-oder Satelliten Speicherort, an dem der eDiscovery-Manager eDiscovery-Untersuchungen durchführt. Wenn ein eDiscovery-Manager SharePoint-und OneDrive-Websites außerhalb der Region durchsucht, die im Such Berechtigungsfilter angegeben ist, werden keine Suchergebnisse zurückgegeben. 
    
- Beim Exportieren von Suchergebnissen werden Inhalte aus allen Inhaltsspeicherorten (einschließlich Exchange, Skype for Business, SharePoint, OneDrive und anderen Office 365 Diensten, die Sie mithilfe des Inhalts Such Tools suchen können) in den Azure-Speicherort hochgeladen, in das Rechenzentrum, das durch den **Region** -Parameter angegeben wird. Auf diese Weise können Organisationen innerhalb der Compliance-Richtlinien bleiben, da Inhalte nicht über kontrollierte Grenzen hinweg exportiert werden können. Wenn im Such Berechtigungsfilter kein Bereich angegeben ist, wird der Inhalt in den Standardbereich der Organisation hochgeladen. 
    
- Sie können einen vorhandenen Such Berechtigungsfilter bearbeiten, um den Bereich hinzuzufügen oder zu ändern, indem Sie den folgenden Befehl ausführen:

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

 **Wer kann Such Berechtigungsfilter erstellen und verwalten (mithilfe von New-ComplianceSecurityFilter-und ComplianceSecurityFilter-Cmdlets)?**
  
Zum Erstellen, anzeigen und Ändern von Such Berechtigungs filtern müssen Sie Mitglied der Rollengruppe "Organisationsverwaltung" im Security #a0 Compliance Center sein.
  
 **Wenn ein eDiscovery-Manager mehreren Rollengruppen zugewiesen ist, die sich über mehrere Agenturen erstrecken, suchen Sie nach Inhalten in einer oder einer Agentur?**
  
Der eDiscovery-Manager kann der Suchabfrage Parameter hinzufügen, mit denen die Suche auf eine bestimmte Agentur beschränkt wird. Wenn beispielsweise eine Organisation die **CustomAttribute10** -Eigenschaft für die Unterscheidung von Agenturen angegeben hat, können Sie die folgenden Informationen an Ihre Suchabfrage anfügen, um Postfächer und OneDrive-Konten `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`in einer bestimmten Agentur zu suchen:.
  
 **Was geschieht, wenn der Wert des Attributs, das als Kompatibilitätsattribut in einem Such Berechtigungsfilter verwendet wird, geändert wird?**
  
Es dauert bis zu drei Tage, bis ein Such Berechtigungsfilter zum Erzwingen der Konformitäts Grenze verwendet wird, wenn der Wert des im Filter verwendeten Attributs geändert wird. Beispielsweise wird im Contoso-Szenario angenommen, dass ein Benutzer in der Fourth Coffee-Agentur an die Weingut-Agentur von Winery übergeben wird. Daher wird der Wert des **Department** -Attributs für das User-Objekt von *fourthcoffee* in *cohowinery*geändert. In dieser Situation erhalten vierter Kaffee eDiscovery und Investoren Suchergebnisse für diesen Benutzer für drei Tage nach dem Ändern des Attributs. In ähnlicher Weise dauert es bis zu drei Tage, bis die Weingut eDiscovery-Manager und Ermittler Suchergebnisse für den Benutzer erhalten. 
  
 **Kann ein eDiscovery-Manager Inhalte aus zwei separaten Kompatibilitäts Grenzen anzeigen?**
  
Ja. Dies kann durch Hinzufügen des Benutzers zu Rollengruppen erfolgen, die für beide Agenturen sichtbar sind.
  
 **Funktionieren Such Berechtigungsfilter für eDiscovery Case Holds, Office 365-Aufbewahrungsrichtlinien oder DLP?**
  
Nein, diesmal nicht.
  
 **Wenn ich einen Bereich zum Steuern der Inhaltsangabe, aber keine SharePoint-Organisation in dieser Region habe, kann ich dennoch SharePoint durchsuchen?**
  
Wenn der im Such Berechtigungsfilter angegebene Bereich nicht in Ihrer Organisation vorhanden ist, wird der Standardbereich durchsucht.
  
 **Wie hoch ist die maximale Anzahl von Such Berechtigungs filtern, die in einer Organisation erstellt werden können?**
  
Es gibt keine Beschränkung für die Anzahl der Such Berechtigungsfilter, die in einer Organisation erstellt werden können. Die Suchleistung wird jedoch beeinträchtigt, wenn mehr als 100 Such Berechtigungsfilter vorhanden sind. Um die Anzahl der Such Berechtigungsfilter in Ihrer Organisation so klein wie möglich zu halten, erstellen Sie Filter, die Regeln für Exchange, SharePoint und OneDrive in einem einzigen Such Berechtigungsfilter kombinieren, wenn möglich.
