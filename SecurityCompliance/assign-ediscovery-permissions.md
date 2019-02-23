---
title: Zuweisen von eDiscovery-Berechtigungen im Office 365 &amp; Security Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: Weisen Sie die erforderlichen Berechtigungen zum Ausführen von eDiscovery-bezogenen Aufgaben mithilfe &amp; des Security Compliance Centers zu.
ms.openlocfilehash: c4dcbf51282aa2887fd7d5032eb8587b5e9d56d7
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223274"
---
# <a name="assign-ediscovery-permissions-in-the-office-365-security-amp-compliance-center"></a>Zuweisen von eDiscovery-Berechtigungen im Office 365 &amp; Security Compliance Center

Wenn Sie möchten, dass Benutzer eines der eDiscovery-bezogenen Tools im Office 365 Security &amp; Compliance Center verwenden, müssen Sie Ihnen die entsprechenden Berechtigungen zuweisen. Am einfachsten können Sie dies tun, indem Sie die Person die entsprechende Rollengruppe auf der Seite **Berechtigungen** im Office 365 Security &amp; Compliance Center hinzufügen. In diesem Thema werden die Berechtigungen beschrieben, die zum Ausführen von eDiscovery-bezogenen &amp; Aufgaben mithilfe des Security Compliance Centers erforderlich sind. 
  
Die primäre eDiscovery-bezogene Rollengruppe im Security &amp; Compliance Center heißt **eDiscovery Manager**. Innerhalb dieser Rollengruppe gibt es zwei Untergruppen. 
  
- **eDiscovery** -Manager – ein eDiscovery-Vorgesetzten kann das Inhaltssuche- &amp; Tool im Security Compliance Center verwenden, um inhaltsspeicherorte in der Organisation zu durchsuchen, und verschiedene suchbezogene Aktionen wie Vorschau-und Export Suche ausführen. Ergebnisse. Mitglieder können auch eDiscovery-Fälle erstellen und verwalten, hinzufügen und Entfernen von Mitgliedern zu einem Fall, erstellen Fall Haltestatus, und führen Sie mit einem Fall verknüpfte Inhaltssuche und Access Case Data in Office 365 Advanced eDiscovery.  EDiscovery-Manager können nur auf die von Ihnen erstellten Fälle zugreifen und diese verwalten. Sie können nicht auf Fälle zugreifen oder diese verwalten, die von anderen eDiscovery-Managern erstellt wurden. 
    
- **eDiscovery-Administratoren** – ein eDiscovery-Administrator ist Mitglied der rollenGruppe "eDiscovery-Manager" und kann dieselben Aufgaben wie Inhaltssuche und Fallverwaltung ausführen, die ein eDiscovery-Manager ausführen kann. Darüber hinaus kann ein eDiscovery-Administrator: 
    
  - Zugriff auf alle Fälle, die auf der Seite **eDiscovery-Fälle** im Security &amp; Compliance Center aufgeführt sind. 

  - Zugriffs Fall Daten in Advanced eDiscovery für jeden Fall in der Organisation.
    
  - eDiscovery-Fälle verwalten, nachdem sie sich selbst als Fallmitglied hinzugefügt haben.
  
  Im Abschnitt [Weitere Informationen](#more-information) finden Sie Gründe, warum Sie EDiscovery-Administratoren in Ihrer Organisation wünschen. 

> [!NOTE]
> Um die Daten eines Benutzers mithilfe von Advanced eDiscovery zu analysieren, muss dem Benutzer (der Depotbank der Daten) eine Office 365 E5-Lizenz zugewiesen werden. Alternativ können Benutzern mit einer Office 365 E1-oder E3-Lizenz eine erweiterte eDiscovery-Standalone-Lizenz zugewiesen werden. Administratoren und Compliance Officer, denen Fälle zugeordnet sind und die erweiterte eDiscovery zur Analyse von Daten verwenden, benötigen keine E5-Lizenz.  
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen Mitglied der Rollengruppe "Organisationsverwaltung" sein (oder der Rolle "Rollenverwaltung" zugewiesen sein), um eDiscovery-Berechtigungen im &amp; Security Compliance Center zuzuweisen.
    
- Mithilfe des [Add-RoleGroupMember-](https://technet.microsoft.com/en-us/library/dd638207%28v=exchg.160%29.aspx) Cmdlets in Security &amp; Compliance Center PowerShell können Sie eine e-Mail-aktivierte Sicherheitsgruppe als Mitglied der Untergruppe "eDiscovery-Manager" in der Rollengruppe "eDiscovery-Manager" hinzufügen. Sie können jedoch keine e-Mail-aktivierte Sicherheitsgruppe zur Untergruppe eDiscovery-Administratoren hinzufügen. Weitere Informationen finden Sie im Abschnitt [More Information](#more-information) . 
    
## <a name="assign-ediscovery-permissions-in-the-security-amp-compliance-center"></a>Zuweisen von eDiscovery-Berechtigungen im &amp; Security Compliance Center

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Berechtigungen**, und klicken Sie dann auf das Kontrollkästchen neben **eDiscovery-Manager**.
    
4. Führen Sie auf der Seite " **eDiscovery Manager-** Flyout" eine der folgenden Aktionen basierend auf den eDiscovery-Berechtigungen aus, die Sie zuweisen möchten. 
    
  - **So machen Sie einen EDiscovery-Manager für einen Benutzer** Klicken Sie neben **EDiscovery-Manager**auf **Bearbeiten**. Klicken Sie unter **ausgewählte eDiscovery-Manager**auf **Bearbeiten**und dann ![auf Symbol](media/ITPro-EAC-AddIcon.gif) **hinzu**fügen. Wählen Sie den Benutzer (oder die Benutzer) aus, den Sie als eDiscovery-Manager hinzufügen möchten, und klicken Sie dann auf **Hinzufügen**. Wenn Sie mit dem Hinzufügen von Benutzern fertig sind, klicken Sie auf **Fertig**. Klicken Sie dann auf der Seite **Bearbeiten Wählen Sie eDiscovery-Manager-** Flyout aus auf **Speichern** , um die Änderungen an der eDiscovery Manager-Mitgliedschaft zu speichern. 
    
  - **So machen Sie einen eDiscovery-Administrator für einen Benutzer** Klicken Sie neben **eDiscovery-Administrator**auf **Bearbeiten**. Klicken Sie unter **ausgewählte eDiscovery-Administratoren**auf **Bearbeiten**und dann ![auf Symbol](media/ITPro-EAC-AddIcon.gif) **hinzu**fügen. Wählen Sie den Benutzer (oder die Benutzer) aus, den Sie als eDiscovery-Administrator hinzufügen möchten, und klicken Sie dann auf **Hinzufügen**. Wenn Sie mit dem Hinzufügen von Benutzern fertig sind, klicken Sie auf **Fertig**. Klicken Sie dann auf der Seite zum **Bearbeiten von eDiscovery-Administratoren auswählen** auf **Speichern** , um die Änderungen an der eDiscovery-Administrator-Mitgliedschaft zu speichern. 
    
> [!NOTE]
> Sie können auch das Cmdlet **Add-eDiscoveryCaseAdmin** verwenden, um einen Benutzer zu einem EDiscovery-Administrator zu machen. Dem Benutzer muss jedoch die Fall Verwaltungsrolle zugewiesen werden, bevor Sie dieses Cmdlet verwenden können, um Sie zu einem eDiscovery-Administrator zu machen. Weitere Informationen finden Sie unter [Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217). 
  
Auf der Seite **Berechtigungen** im Security &amp; Compliance Center können Sie auch Benutzer mit eDiscovery-bezogenen Berechtigungen zuweisen, indem Sie Sie den Rollengruppen Compliance-Administrator, Organisationsverwaltung und Prüfer hinzufügen. Eine Beschreibung der eDiscovery-bezogenen RBAC-Rollen, die den einzelnen Rollengruppen zugewiesen sind, finden Sie im Abschnitt [RBAC-Rollen im Zusammenhang mit eDiscovery](#rbac-roles-related-to-ediscovery) . 

## <a name="rbac-roles-related-to-ediscovery"></a>RBAC-Rollen im Zusammenhang mit eDiscovery

In der folgenden Tabelle sind die eDiscovery-bezogenen RBAC-Rollen im Security & Compliance Center aufgeführt, und es werden die integrierten Rollengruppen angezeigt, denen standardmäßig jede Rolle zugewiesen ist. 
    
|**Rolle**|**Compliance-Administrator**|**eDiscovery-Manager &-Administrator**|**Organisationsverwaltung**|**Reviewer**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|Fallverwaltung <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Compliance-Suche <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Exportieren <br/> | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Aufbewahrung <br/>  |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Vorschau <br/>  | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Prüfung  <br/>  | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |
|RMS-entSchlüsselung <br/>  ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |||
|Suchen und löschen <br/> | <br/> | <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | 
||||
  
In den folgenden Abschnitten werden alle eDiscovery-bezogenen RBAC-Rollen beschrieben, die in der obigen Tabelle aufgeführt sind.

### <a name="case-management"></a>Fallverwaltung

Diese Rolle ermöglicht Benutzern das Erstellen, bearbeiten, löschen und Steuern des Zugriffs auf eDiscovery-Fälle im Security & Compliance Center. Weitere Informationen finden Sie unter [Verwalten von eDiscovery-Fällen im Office 365 &amp; Security Compliance Center](manage-ediscovery-cases.md). Wie bereits erläutert, muss einem Benutzer die Rolle "Fallverwaltung" zugewiesen werden, bevor Sie das **Add-eDiscoveryCaseAdmin-** Cmdlet verwenden können, um Sie zu einem EDiscovery-Administrator zu machen. 

### <a name="compliance-search"></a>Compliance-Suche

Diese Rolle ermöglicht Benutzern das Ausführen des Inhalts Suchtool im Security & Compliance Center zum Durchsuchen von Postfächern und öffentlichen Ordnern, SharePoint Online-Websites, OneDrive for Business-Websites, Skype for Business-Unterhaltungen, Office 365-Gruppen und Microsoft Teams. Diese Rolle ermöglicht es einem Benutzer, eine Schätzung der Suchergebnisse zu erhalten und Export Berichte zu erstellen, aber zusätzliche Rollen sind erforderlich, um Inhalts Suchaktionen wie die Vorschau, den Export oder das Löschen von Suchergebnissen zu initiieren.

Beachten Sie, dass Benutzer, denen die Konformitäts Such Rolle zugewiesen wurde, aber nicht über die Rolle "Vorschau" verfügen, eine Vorschau der Ergebnisse einer Suche haben, in der die Vorschau Aktion von einem Benutzer initiiert wurde, dem die Rolle "Vorschau" zugewiesen wurde. Der Benutzer ohne die Vorschau Rolle kann Ergebnisse für bis zu 2 Wochen nach der Erstellung der ersten Vorschau Aktion anzeigen.

Entsprechend können Benutzer, denen die Konformitäts Such Rolle zugewiesen wurde, aber nicht über die Export Rolle verfügen, die Ergebnisse einer Suche herunterladen, in der die Exportaktion von einem Benutzer initiiert wurde, dem die Export Rolle zugewiesen wurde. Der Benutzer ohne die Export Rolle kann die Ergebnisse einer Suche nach der Erstellung der anfänglichen Exportaktion bis zu 2 Wochen lang herunterladen. Danach können die Ergebnisse nicht heruntergeladen werden, es sei denn, jemand mit der Export Rolle startet den Export erneut.

Weitere Informationen finden Sie unter [Inhaltssuche in Office 365](content-search.md). 

### <a name="export"></a>Exportieren

Die Rolle ermöglicht Benutzern das Exportieren der Ergebnisse einer Inhaltssuche auf einen lokalen Computer. Außerdem können Sie Suchergebnisse für die Analyse in Advanced eDiscovery vorbereiten. 

Weitere Informationen zum Exportieren von Suchergebnissen finden Sie unter [Exportieren von Suchergebnissen aus dem Office 365 Security _AMP_ Compliance Center](export-search-results.md).

### <a name="hold"></a>Aufbewahrung

Mit dieser Rolle können Benutzer Inhalte in Postfächern, öffentlichen Ordnern, Websites, Skype for Business-Unterhaltungen und Office 365-Gruppen platzieren. Wenn der Inhalt in der Warteschleife gespeichert ist, können Inhaltsbesitzer weiterhin den ursprünglichen Inhalt ändern oder löschen, der Inhalt bleibt jedoch erhalten, bis der Aufbewahrungszeitraum entfernt oder die Aufbewahrungsdauer abgelaufen ist. 

Weitere Informationen zu Haltebereichen finden Sie unter:

- [eDiscovery-Fälle im Office 365 Security & Compliance Center](ediscovery-cases.md) 
- [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md)

### <a name="preview"></a>Vorschau

Diese Rolle ermöglicht Benutzern das Anzeigen einer Liste von Elementen, die von einer Inhaltssuche zurückgegeben wurden. Außerdem können Sie jedes Element in der Liste öffnen und anzeigen, um dessen Inhalt anzuzeigen.

### <a name="review"></a>Prüfung 

Diese Rolle ermöglicht Benutzern den Zugriff auf Falldaten in Office 365 Advanced eDiscovery. Der Hauptzweckdieser Rolle besteht darin, Benutzern Zugriff auf Erweiterte eDiscovery zu gewähren. Benutzer, die dieser Rolle zugewiesen sind, können die Liste der Fälle auf der eDiscovery-Seite im Security & Compliance Center sehen und öffnen, von denen Sie Mitglieder sind. Nachdem der Benutzer auf einen Fall im Security & Compliance Center zugegriffen hat, kann er auf **zu Advanced eDiscovery wechseln** , um auf die Falldaten in Advanced eDiscovery zuzugreifen und diese zu analysieren. Diese Rolle ermöglicht es dem Benutzer nicht, eine Vorschau der Ergebnisse einer Inhaltssuche anzuzeigen, die mit dem Fall verknüpft ist, oder um andere Inhaltssuche oder Fall Verwaltungsaufgaben durchzuführen.

### <a name="rms-decrypt"></a>RMS-entSchlüsselung

Mit dieser Rolle können Benutzer RMS-verschlüsselte e-Mail-Nachrichten beim Exportieren von Suchergebnissen oder beim Vorbereiten der Suchergebnisse für die Analyse in Advanced eDiscovery entschlüsseln. Weitere Informationen zum Entschlüsseln von Suchergebnissen während des Exports finden Sie unter [Exportieren von Suchergebnissen aus dem Office 365 Security _AMP_ Compliance Center](export-search-results.md).

### <a name="search-and-purge"></a>Suchen und löschen

Diese Rolle ermöglicht Benutzern die Massen Entfernung von Daten, die den Kriterien einer Inhaltssuche entsprechen. Weitere Informationen finden Sie unter [Suchen und Löschen von e-Mail-Nachrichten in Ihrer Office 365-Organisation](search-for-and-delete-messages-in-your-organization.md). 


## <a name="more-information"></a>Weitere Informationen

- **Gründe für die Erstellung eines eDiscovery** -Administrators Wie bereits erläutert, ist ein eDiscovery-Administrator Mitglied der eDiscovery-Manager-Rollengruppe, die alle eDiscovery-Fälle in Ihrer Organisation anzeigen und darauf zugreifen kann. Diese Möglichkeit für den Zugriff auf alle eDiscovery-Fälle hat zwei wichtige Zwecke: 
    
  - Wenn eine Person, die das einzige Mitglied eines eDiscovery-Falles ist, Ihre Organisation verlässt, kann niemand (einschließlich der Mitglieder der Rollengruppe "Organisationsverwaltung" oder ein anderes Mitglied der eDiscovery-Manager-Rollengruppe) auf diesen eDiscovery-Fall zugreifen, da er kein Mitglied ist. eines Falls. In dieser Situation gäbe es keine Möglichkeit, auf die Daten in dem Fall zuzugreifen. Da ein eDiscovery-Administrator jedoch auf alle eDiscovery-Fälle in der Organisation zugreifen kann, können Sie den Fall im &amp; Security Compliance Center anzeigen und sich selbst oder einen anderen eDiscovery-Manager als Mitglied der Anfrage hinzufügen.
    
  - Da ein eDiscovery-Administrator alle eDiscovery-Fälle anzeigen und darauf zugreifen kann, können Sie alle Fälle und zugehörige Compliance-Suchvorgänge überwachen und überwachen. Dadurch kann verhindert werden, dass Kompatibilitäts-und eDiscovery-Fälle missbraucht werden. Und da eDiscovery-Administratoren in den Ergebnissen einer Compliance-Suche auf potenziell vertrauliche Informationen zugreifen können, sollten Sie die Anzahl der eDiscovery-Administratoren begrenzen.
    
    Außerdem werden eDiscovery-Administratoren im Security &amp; Compliance Center automatisch als Administratoren in Advanced eDiscovery hinzugefügt. Das kann bedeuten, dass eine Person ein eDiscovery-Administrator sein muss, um administrative Aufgaben in Advanced eDiscovery ausführen zu können, wie das Einrichten von Benutzern, das Erstellen von Fällen und das Importieren von Daten in einen Fall.
    
- **Kann ich eine Gruppe als Mitglied der eDiscovery-Manager-Rollengruppe im Security &amp; Compliance Center hinzufügen?** Wie bereits erläutert, können Sie eine e-Mail-aktivierte Sicherheitsgruppe als Mitglied der Untergruppe eDiscovery-Manager in der Rollengruppe eDiscovery Manager mithilfe des **Add-RoleGroupMember-** Cmdlets &amp; in Security Compliance Center PowerShell hinzufügen. Sie können beispielsweise den folgenden Befehl ausführen, um eine e-Mail-aktivierte Sicherheitsgruppe zur eDiscovery-Manager-Rollengruppe hinzuzufügen. 
    
  ```
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Beachten Sie, dass eine Exchange-Verteilergruppe oder eine Office 365-Gruppe nicht unterstützt wird. Sie müssen eine e-Mail-aktivierte Sicherheitsgruppe verwenden, die Sie mithilfe des ` New-DistributionGroup -Type Security ` Befehls in Exchange Online PowerShell erstellen können. Sie können auch eine e-Mail-aktivierte Sicherheitsgruppe (und Mitglieder hinzufügen) in der Exchange-Verwaltungskonsole oder im Office 365 Admin Center erstellen. Beachten Sie, dass es möglicherweise bis zu 60 Minuten nach dem Erstellen für eine neue e-Mail-aktivierte Sicherheit verfügbar ist, die der Rollengruppe "eDiscovery-Manager" hinzugefügt werden kann. 
    
    Außerdem können Sie eine e-Mail-aktivierte Sicherheitsgruppe nicht als eDiscovery-Administrator festlegen, indem Sie das Cmdlet **Add-eDiscoveryCaseAdmin** in Security &amp; Compliance Center PowerShell verwenden. Sie können nur einzelne Benutzer als eDiscovery-Administratoren hinzufügen. 
    
    Beachten Sie, dass Sie eine e-Mail-aktivierte Sicherheitsgruppe auch nicht als Mitglied einer Anfrage hinzufügen können.
