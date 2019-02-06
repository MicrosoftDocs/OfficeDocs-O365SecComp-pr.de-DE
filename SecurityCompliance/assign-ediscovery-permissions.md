---
title: Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: Weisen Sie die erforderlichen Berechtigungen für die Sicherheit von eDiscovery-bezogene Aufgaben ausführen &amp; Compliance Center.
ms.openlocfilehash: 95f0ed171c37ec84ca8bb8f00e69ab0318cd31cd
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741158"
---
# <a name="assign-ediscovery-permissions-in-the-office-365-security-amp-compliance-center"></a>Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center

Wenn Sie Benutzer eines der eDiscovery-bezogene Tools in die Office 365-Sicherheit verwenden sollen &amp; Compliance Center, Sie müssen sie die entsprechenden Berechtigungen zugewiesen werden. Die einfachste Möglichkeit hierzu ist, um die Person die entsprechenden Rollengruppe auf der Seite **Berechtigungen** in der Office 365-Sicherheit &amp; Compliance Center. In diesem Thema werden die erforderlichen Berechtigungen für die Sicherheit von eDiscovery-bezogene Aufgaben ausführen &amp; Compliance Center. 
  
Die primäre eDiscovery-bezogene Rollengruppe in Security &amp; Compliance Center **eDiscovery-Manager**aufgerufen wird. Es gibt zwei Untergruppen innerhalb dieser Rollengruppe. 
  
- **eDiscovery-Manager** - eine eDiscovery-Manager kann mithilfe der Inhalte Suchfunktion in das Wertpapier &amp; Compliance Center Speicherorte für Inhalte in der Organisation suchen und suchbezogene Aktionen wie Preview und Exportieren der Suche Ergebnisse. Mitglieder können auch erstellen und Verwalten von eDiscovery-Fälle, hinzufügen und Entfernen von Mitgliedern zu einer Anfrage, Groß-/Kleinschreibung Haltestatus erstellen und Content verknüpft ist, mit der Groß-/Kleinschreibung und Groß-/Kleinschreibung Access-Daten in Office 365 erweiterte eDiscovery-Suche ausgeführt.  Eine eDiscovery-Manager kann nur zugreifen, und verwalten Sie die Fällen, die sie erstellen. Nicht zugreifen oder andere eDiscovery-Manager erstellte Anfragen verwalten. 
    
- **Administratoren eDiscovery** - eine eDiscovery-Administrator ist Mitglied der Rollengruppe eDiscovery-Manager und kann führen Sie die gleichen Inhaltssuche auch die Groß-/Kleinschreibung verwaltungsbezogenen Aufgaben, die eine eDiscovery-Manager ausführen können. Darüber hinaus können eine eDiscovery-Administrator: 
    
  - Zugriff auf alle Anfragen, die auf der Seite **eDiscovery-Fälle** , in das Wertpapier aufgelisteten &amp; Compliance Center. 

  - Groß-/Kleinschreibung Zugriff auf Daten in erweiterten eDiscovery für alle Fall in der Organisation.
    
  - eDiscovery-Fälle verwalten, nachdem sie sich selbst als Fallmitglied hinzugefügt haben.
  
  Gründe, warum Sie die eDiscovery-Administratoren in Ihrer Organisation sollten, finden Sie unter im Abschnitt [Weitere Informationen](#more-information) . 

> [!NOTE]
> Um eine erweiterte eDiscovery mit Benutzerdaten zu analysieren, muss der Benutzer (der Verwaltungsberechtigte der Daten) eine Lizenz für Office 365 E5 zugewiesen werden. Alternativ können der Benutzer mit einer Lizenz für Office 365 E1 oder E3 eine erweiterte eDiscovery eigenständige Lizenz zugewiesen werden. Administratoren und Compliance Officer, die zugewiesenen Fällen und erweiterte eDiscovery verwenden, um Daten zu analysieren erforderlich keine E5-Lizenz.  
  
## <a name="before-you-begin"></a>Bevor Sie beginnen:

- Sie müssen ein Mitglied der Rollengruppe "Organisationsverwaltung" (oder die Verwaltungsrolle Rolle zugewiesen werden) zum Zuweisen von Berechtigungen in das Wertpapier eDiscovery &amp; Compliance Center.
    
- Können Sie das Cmdlet [Add-RoleGroupMember](https://technet.microsoft.com/en-us/library/dd638207%28v=exchg.160%29.aspx) in Security &amp; Compliance Center PowerShell So fügen Sie eine e-Mail-aktivierte Sicherheitsgruppe als Mitglied der Untergruppe eDiscovery-Manager in der Gruppe von eDiscovery-Manager-Rolle hinzu. Allerdings kann nicht die Untergruppe der eDiscovery-Administratoren eine e-Mail-aktivierte Sicherheitsgruppe hinzugefügt werden. Finden Sie [Weitere Informationen](#more-information) im Abschnitt Weitere Informationen. 
    
## <a name="assign-ediscovery-permissions-in-the-security-amp-compliance-center"></a>Zuweisen von Berechtigungen in das Wertpapier eDiscovery &amp; Compliance Center

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Berechtigungen**, und klicken Sie dann auf das Kontrollkästchen neben **eDiscovery-Manager**.
    
4. Führen Sie auf der Seite flyoutmenü **eDiscovery-Manager** die folgenden basierend auf den eDiscovery-Berechtigungen, die Sie zuweisen möchten. 
    
  - **So machen einem Benutzer eine eDiscovery-Manager** Neben den **eDiscovery-Manager**klicken Sie auf **Bearbeiten**. Klicken Sie unter **Selected eDiscovery-Manager**, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Hinzufügen**. Wählen Sie die (oder Benutzer) Sie verwenden möchten, fügen Sie als ein eDiscovery-Manager, und klicken Sie dann auf **Hinzufügen**. Wenn Sie die Benutzer hinzugefügt haben, klicken Sie auf **Fertig**. Klicken Sie dann auf der Seite flyoutmenü **Bearbeiten wählen Sie eDiscovery-Manager** klicken Sie auf **Speichern** , um die Änderungen an der eDiscovery-Manager die Mitgliedschaft zu speichern. 
    
  - **So machen einem Benutzer zu eine eDiscovery-Administrator** Klicken Sie neben **eDiscovery-Administrator**auf **Bearbeiten**. Klicken Sie unter **Selected eDiscovery Administratoren**, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Hinzufügen**. Wählen Sie die (oder Benutzer) Sie verwenden möchten, fügen Sie als einer eDiscovery-Administrator, und klicken Sie dann auf **Hinzufügen**. Wenn Sie die Benutzer hinzugefügt haben, klicken Sie auf **Fertig**. Klicken Sie dann auf der Seite **Wählen Sie bearbeiten eDiscovery Administrator** flyoutmenü klicken Sie auf **Speichern** , um die Änderungen zu speichern, um die Mitgliedschaft in der Administratorgruppe eDiscovery. 
    
> [!NOTE]
> Sie können auch das Cmdlet **Add-eDiscoveryCaseAdmin** verwenden, um einem Benutzer einer eDiscovery-Administrator. Allerdings muss der Benutzer die Groß-/Kleinschreibung Verwaltungsrolle zugewiesen werden, bevor Sie dieses Cmdlet verwenden können, um sie zu eine eDiscovery-Administrator machen. Weitere Informationen finden Sie unter [Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217). 
  
Auf der Seite **Berechtigungen** in das Wertpapier &amp; Compliance Center, Sie können auch Benutzer zuweisen eDiscovery-bezogene Berechtigungen Rollengruppen Compliance-Administrator, Organization Management und Reviewer hinzu. Eine Beschreibung der eDiscovery-bezogene RBAC-Rollen, jede dieser Rollengruppen zugewiesen sind finden Sie im Abschnitt [RBAC-Rollen im Zusammenhang mit eDiscovery](#rbac-roles-related-to-ediscovery) . 

## <a name="rbac-roles-related-to-ediscovery"></a>RBAC-Rollen, die im Zusammenhang mit der eDiscovery

In der folgenden Tabelle sind die eDiscovery-bezogene RBAC-Rollen in der & Security Compliance Center, und gibt an, die integrierte Rollengruppen, die jede Rolle standardmäßig zugewiesen wird. 
    
|**Rolle**|**Compliance-Administrator**|**eDiscovery-Manager &-Administrator**|**Organisationsverwaltung**|**Reviewer**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|Fall-Verwaltung <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Compliance-Suche <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Exportieren <br/> | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Aufbewahrung <br/>  |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Vorschau <br/>  | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Prüfung  <br/>  | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |
|RMS-Entschlüsselung <br/>  ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |||
|Suchen und löschen <br/> | <br/> | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | 
||||
  
In den folgenden Abschnitten werden die verschiedenen eDiscovery-bezogene RBAC-Rollen in der obigen Tabelle aufgeführt.

### <a name="case-management"></a>Fall-Verwaltung

Diese Rolle kann Benutzer erstellen, bearbeiten, löschen und Steuerung des Zugriffs auf eDiscovery-Fälle, in der & Security Compliance Center. Weitere Informationen finden Sie unter [Verwalten von eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](manage-ediscovery-cases.md). Wie bereits erklärt wird ein Benutzer muss die Groß-/Kleinschreibung Verwaltungsrolle zugewiesen sein bevor Sie mit dem Cmdlet **Add-eDiscoveryCaseAdmin** verwenden können, um sie zu eine eDiscovery-Administrator machen. 

### <a name="compliance-search"></a>Compliance-Suche

Diese Rolle ermöglicht Benutzern das Ausführen des Content-Suche in der & Security Compliance Center zum Suchen von Postfächern und öffentlichen Ordnern, SharePoint Online-Websites, OneDrive for Business-Websites Skype für Business Unterhaltungen, Office 365-Gruppen und Microsoft-Teams. Diese Rolle ermöglicht einem Benutzer erhalten eine Schätzung der Suchergebnisse und Exportieren von Berichten zu erstellen, jedoch zusätzliche Rollen sind erforderlich, damit Inhaltssuche Aktionen wie Vorschau, exportieren oder Löschen von Suchergebnissen zu initiieren.

Beachten Sie, dass Benutzer der Rolle Compliance Suche jedoch nicht die Preview-Rolle kann die Ergebnisse einer Suche Vorschau anzeigen, in dem die Preview-Aktion durch einen Benutzer initiiert wurde, die die Preview-Rolle zugewiesen hat. Der Benutzer ohne die Preview-Rolle kann eine Vorschau anzeigen Ergebnisse für bis zu zwei Wochen, nachdem die ursprünglichen Vorschau-Aktion erstellt wurde.

In ähnlicher Weise Benutzern zugewiesen, die Compliance-Suchrolle jedoch nicht den Export-Rolle die Ergebnisse einer Suche herunterladen kann, in dem die Export-Aktion durch einen Benutzer initiiert hat, die die Export-Rolle zugewiesen hat. Der Benutzer ohne die Export-Rolle kann die Ergebnisse einer Suche für bis zu zwei Wochen nach dem Erstellen der anfänglichen Aktion herunterladen. Nach Ausführung dieses nicht sie möglich die Ergebnisse herunterladen, es sei denn, ein Benutzer mit der Rolle Export den Export wird neu gestartet.

Weitere Informationen finden Sie unter [Content-Suche in Office 365](content-search.md). 

### <a name="export"></a>Exportieren

Die Rolle kann Benutzer die Ergebnisse einer Inhaltssuche auf einen lokalen Computer exportiert. Darüber hinaus können sie die Suchergebnisse für die Analyse in erweiterten eDiscovery vorzubereiten. 

Weitere Informationen zum Exportieren von Suchergebnissen finden Sie unter [Suchergebnisse aus der Sicherheit in Office 365 Compliance Center & exportieren](export-search-results.md).

### <a name="hold"></a>Aufbewahrung

Diese Rolle kann Benutzer Inhalte versehen Sie Postfächer, Öffentliche Ordner, Websites, Skype für Business-Unterhaltungen, und halten Sie Office 365-Gruppen auf. Wenn Inhalte in der Warteschleife ist, Besitzer von Inhalten werden kann, ändern oder löschen den ursprünglichen Inhalt, aber der Inhalt wird beibehalten, bis die Sperre entfernt wurde oder die Dauer halten abgelaufen ist. 

Weitere Informationen zu Haltebereichen finden Sie unter:

- [eDiscovery-Fälle, in der Office 365-Sicherheit & Compliance Center](ediscovery-cases.md) 
- [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md)

### <a name="preview"></a>Vorschau

Diese Rolle ermöglicht Benutzern das Anzeigen einer Liste von Elementen, die von einem Inhaltssuche zurückgegeben wurden. Außerdem werden zu öffnen und Anzeigen von jedes Element aus der Liste aus, um seinen Inhalt anzuzeigen.

### <a name="review"></a>Prüfung 

Diese Rolle ermöglicht Benutzern, die Groß-/Kleinschreibung Daten in Office 365 erweiterte eDiscovery zugreifen. Der primäre Zweck der dieser Rolle ist erhalten Benutzer Zugriff auf Erweiterte eDiscovery. Benutzer, die dieser Rolle zugewiesen sind können finden und öffnen Sie die Liste auf der Seite eDiscovery-Fälle in den & Security Compliance Center, die sie Mitglieder sind. Nachdem der Benutzer eine Anfrage in den & Security Compliance Center zugreift, kann er **Schalter, mit dem erweiterten eDiscovery** Zugriff und zum Analysieren der Groß-/Kleinschreibung Daten in erweiterten eDiscovery klicken. Diese Rolle ermöglicht nicht es dem Benutzer, um die Ergebnisse einer Inhaltssuche Vorschau anzeigen, die die Groß-/Kleinschreibung zugeordnet ist oder andere Inhaltssuche oder Fallmanagement Aufgaben auszuführen.

### <a name="rms-decrypt"></a>RMS-Entschlüsselung

Dieser Rolle können Benutzer entschlüsseln RMS-verschlüsselten e-Mail-Nachrichten beim Exportieren in erweiterten eDiscovery Ergebnisse oder vorbereiten Suchergebnisse für die Analyse suchen. Weitere Informationen zu entschlüsseln Suchergebnisse während des Exports, finden Sie unter [Suchergebnisse aus der Sicherheit in Office 365 Compliance Center & exportieren](export-search-results.md).

### <a name="search-and-purge"></a>Suchen und löschen

Diese Rolle ermöglicht Benutzern das Bulk Entfernen von Daten, die die Kriterien der ein Inhaltssuche entsprechen. Weitere Informationen finden Sie unter [Suchen und Löschen von e-Mail-Nachrichten in Office 365-Organisation](search-for-and-delete-messages-in-your-organization.md). 


## <a name="more-information"></a>Weitere Informationen

- **Gründe für das Erstellen einer eDiscovery-Administrator?** Wie bereits erläutert, eine eDiscovery, den Administrator Mitglied der Gruppe der eDiscovery-Manager-Rolle ist, anzeigen und alle eDiscovery-Fälle in Ihrer Organisation zugreifen kann. Diese Möglichkeit zum Zugriff auf die eDiscovery-Fälle hat zwei wichtige Funktionen: 
    
  - Wenn eine Person, die das einzige Mitglied einer eDiscovery-Fall ist Ihre Organisation verlässt, kann niemand (einschließlich Mitglieder der Rollengruppe "Organisationsverwaltung" oder ein anderes Mitglied der Rollengruppe eDiscovery-Manager), eDiscovery-Fall zugreifen, da der Mitglied sind nicht der Fall. In diesem Fall würde keine Möglichkeit, den Zugriff auf die Groß-/Kleinschreibung vorhanden sein. Da eine eDiscovery-Administrator alle eDiscovery-Fälle, in der Organisation zugreifen kann, können sie die Groß-/Kleinschreibung in das Wertpapier anzeigen, aber &amp; Compliance Center und Hinzufügen von sich selbst oder einem anderen eDiscovery-Manager als Mitglied der Groß-/Kleinschreibung.
    
  - Da eine eDiscovery-Administrator kann anzeigen und Zugriff auf alle eDiscovery-Fälle, können sie überwachen und allen Fällen überwachen und Compliance-Suchvorgänge verknüpft. Dies hilft um Missbrauch des Compliance Suchvorgänge oder eDiscovery-Fälle zu verhindern. Und da eDiscovery Administratoren möglicherweise vertraulichen Informationen in den Ergebnissen einer Compliance-Suche zugreifen kann, sollten Sie die Anzahl der Personen, die eDiscovery-Administratoren sind beschränken.
    
    Darüber hinaus eDiscovery Administratoren in das Wertpapier &amp; Compliance Center werden automatisch als Administratoren in erweiterten eDiscovery hinzugefügt. Dies bedeutet, dass eine Person einer eDiscovery-Administrator zum Ausführen von Verwaltungsaufgaben in erweiterten eDiscovery, wie Einrichten von Benutzern, Erstellen von Fällen und Importieren von Daten in einer Anfrage sein muss.
    
- **Kann ich eine Gruppe als Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier hinzufügen &amp; Compliance Center?** Wie bereits erläutert, Sie können eine e-Mail-aktivierte Sicherheitsgruppe als Mitglied der Untergruppe eDiscovery-Manager in der eDiscovery-Manager-Rollengruppe hinzufügen, indem Sie mithilfe des Cmdlets **Add-RoleGroupMember** in Security &amp; Compliance Center PowerShell. Beispielsweise können Sie den folgenden Befehl zum Hinzufügen einer e-Mail-aktivierte Sicherheitsgruppe Gruppe eDiscovery-Manager-Rolle ausführen. 
    
  ```
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Beachten Sie, dass ein Exchange-Verteilergruppen oder eine Office 365-Gruppe werden nicht unterstützt. Sie müssen eine e-Mail-aktivierte Sicherheitsgruppe, die Sie mithilfe der in Exchange Online PowerShell erstellen können verwenden die ` New-DistributionGroup -Type Security ` Befehl. Sie können eine e-Mail-aktivierte Sicherheitsgruppe erstellen (und Hinzufügen von Mitgliedern) in der Exchange-Verwaltungskonsole oder im Office 365 Administrationscenter. Beachten Sie, dass es bis zu 60 Minuten dauern kann nach der Erstellung für eine neue e-Mail-aktivierte Sicherheitsgruppe für die eDiscovery-Manager-Rollengruppe hinzufügen verfügbar sein. 
    
    Auch wie bereits erwähnt, können Sie eine e-Mail-aktivierte Sicherheitsgruppe eine eDiscovery-Administrator mithilfe des **Add-eDiscoveryCaseAdmin** -Cmdlets in Security group vornehmen &amp; Compliance Center PowerShell. Sie können nur einzelne Benutzer als eDiscovery-Administratoren hinzufügen. 
    
    Beachten Sie, dass Sie als Mitglied der Fall auch eine e-Mail-aktivierte Sicherheitsgruppe hinzufügen können.
