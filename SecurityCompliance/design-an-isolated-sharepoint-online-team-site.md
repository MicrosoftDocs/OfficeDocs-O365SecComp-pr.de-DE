---
title: Entwerfen einer isolierten SharePoint Online-Teamwebsite
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: 'Zusammenfassung: Lernen Sie die Schritte zum Entwerfen von isolierten SharePoint Online-Teamwebsites kennen.'
ms.openlocfilehash: bd36044eb16b9f6ee3ee9bbb444fe8f4efe2fd63
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345807"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a>Entwerfen einer isolierten SharePoint Online-Teamwebsite

 **Zusammenfassung:** Lernen Sie die Schritte zum Entwerfen von isolierten SharePoint Online-Teamwebsites kennen.
  
In diesem Artikel werden die wichtigsten Entwurfsentscheidungen erläutert, die Sie vor der Erstellung einer isolierten SharePoint Online-Teamwebsite treffen müssen.
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a>Phase 1: Ermitteln der SharePoint-Gruppen und Berechtigungsstufen

Jede SharePoint Online-Teamwebsite wird standardmäßig mit den folgenden SharePoint-Gruppen erstellt:
  
- \<Websitename > Mitglieder
    
- \<Websitename > Besucher
    
- \<Websitename > Besitzer
    
Diese Gruppen unterscheiden sich von Office 365- und Azure Active Directory (AD)-Gruppen und bilden die Grundlage zum Zuweisen von Berechtigungen für die Ressourcen der Website.
  
Der Satz von spezifischen Berechtigungen, der bestimmt, welche Aktionen ein Mitglied einer SharePoint-Gruppe auf einer Website ausführen kann, ist eine Berechtigungsstufe. Für eine SharePoint Online-Teamwebsite gibt es standardmäßig drei Berechtigungsstufen: Bearbeitungszugriff, Lesezugriff und Vollzugriff. In der folgenden Tabelle ist die standardmäßige Korrelation von SharePoint-Gruppen und zugewiesenen Berechtigungsstufen dargestellt:
  
|**SharePoint-Gruppe**|**Berechtigungsstufe**|
|:-----|:-----|
|\<Websitename > Mitglieder  <br/> |Bearbeiten  <br/> |
|\<Websitename > Besucher  <br/> |Überwachungsdaten  <br/> |
|\<Websitename > Besitzer  <br/> |Vollzugriff  <br/> |
   
 **Bewährte Methode:** Sie können weitere SharePoint-Gruppen und Berechtigungsstufen erstellen. Allerdings wird empfohlen, die SharePoint-Standardgruppen und die Berechtigungsstufen für die isolierte SharePoint Online-Website zu verwenden.
  
Hier sind die SharePoint-Gruppen und Berechtigungsstufen.
  
![Die standardmäßigen SharePoint-Gruppen und -Berechtigungsstufen für eine SharePoint Online-Website.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a>Phase 2: Zuweisen von Berechtigungen zu Benutzern mit Zugriffsgruppen

Sie können Benutzern Berechtigungen zuweisen, indem Sie ihr Benutzerkonto oder eine Office 365- oder Azure AD-Gruppe, in der das Benutzerkonto Mitglied ist, zu den SharePoint-Gruppen hinzufügen. Nach dem Hinzufügen wird den Office 365-Benutzerkonten entweder direkt oder indirekt über die Mitgliedschaft in einer Office 365- oder Azure AD-Gruppe die Berechtigungsstufe zugewiesen, die der SharePoint-Gruppe zugeordnet ist.
  
Am Beispiel der SharePoint-Standardgruppen bedeutet dies:
  
- Mitglieder der ** \<Websitename > Mitglieder** SharePoint-Gruppe, die Benutzerkonten und Gruppen enthalten können, sind **die Berechtigungsstufen** zugewiesen
    
- Mitglieder der ** \<Websitename > Besucher** SharePoint-Gruppe, die Benutzerkonten und Gruppen enthalten können, werden die Berechtigungsstufe **Lesen** zugewiesen
    
- Mitglieder der ** \<Websitename > Besitzer** SharePoint-Gruppe, die Benutzerkonten und Gruppen enthalten können, werden die Berechtigungsstufe **Vollzugriff** zugewiesen
    
 **Bewährte Methode:** Obwohl Sie Berechtigungen über einzelne Benutzerkonten verwalten können, empfehlen wir stattdessen die Verwendung einer einzelnen Azure AD-Gruppe, die als Zugriffsgruppe bezeichnet wird. Dadurch wird die Verwaltung von Berechtigungen über Mitgliedschaft in der Zugriffsgruppe anstelle der Verwaltung der Liste von Benutzerkonten für jede SharePoint-Gruppe erleichtert.
  
Azure AD-Gruppen für Office 365 unterscheiden sich von Office 365-Gruppen. Azure AD-Gruppen werden im Office Admin Center mit dem **Typ****Sicherheit** angezeigt und haben keine E-Mail-Adresse. Azure AD-Gruppen können verwaltet werden in:
  
- Windows Server Active Directory (AD)
    
    Hierbei handelt es sich um Gruppen, die in Ihrer lokalen Windows Server AD-Infrastruktur erstellt und mit Ihrem Office 365-Abonnement synchronisiert wurden. Im Office Admin Center haben diese Gruppen den **Status****Mit Active Directory synchronisiert**.
    
- Office 365
    
    Hierbei handelt es sich um Gruppen, die mit dem Office Admin Center, dem Azure-Portal oder Microsoft PowerShell erstellt wurden. Im Office Admin Center haben diese Gruppen den **Status****Cloud**.
    
 **Bewährte Methode:** Wenn Sie Windows Server AD lokal verwenden und mit Ihrem Office 365-Abonnement synchronisieren, führen Sie die Benutzer- und Gruppenverwaltung mit Windows Server AD durch.
  
Für isolierte SharePoint Online-Teamwebsites sieht die empfohlene Gruppenstruktur wie folgt aus:
  
|**SharePoint-Gruppe**|**Azure AD-basierte Zugriffsgruppe**|**Berechtigungsstufe**|
|:-----|:-----|:-----|
|\<Websitename > Mitglieder  <br/> |\<Websitename > Mitglieder  <br/> |Bearbeiten  <br/> |
|\<Websitename > Besucher  <br/> |\<Websitename > Leser von Berichten  <br/> |Überwachungsdaten  <br/> |
|\<Websitename > Besitzer  <br/> |\<Websitename > Admins  <br/> |Vollzugriff  <br/> |
   
 **Bewährte Methode:** Sie können zwar sowohl Office 365- als auch Azure AD-Gruppen als Mitglieder von SharePoint-Gruppen verwenden, wir empfehlen jedoch die Verwendung von Azure AD-Gruppen. Azure AD-Gruppen, die über Windows Server AD oder Office 365 verwaltet werden, bieten Ihnen größere Flexibilität bei der Verwendung geschachtelter Gruppen zum Zuweisen von Berechtigungen.
  
Hier sind die standardmäßige SharePoint-Gruppen für die Verwendung von Azure AD-based Access Gruppen konfiguriert.
  
![Verwenden von Access Gruppen als Mitglieder von Standardgruppen SharePoint Online-Website.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
Beachten Sie beim Entwerfen der drei Zugriffsgruppen die folgenden Punkte:
  
- Sollte nur einige Elemente in der ** \<Websitename > Admins** Zugriffsgruppe, für eine kleine Anzahl von SharePoint Online-Administratoren, die Teamwebsite verwaltet werden.
    
- Die meisten der Websitemitglieder einer sind der ** \<Websitename > Mitglieder** oder ** \<Websitename > Viewer** Zugriff auf Gruppen. Da Websitemitglieder in der ** \<Websitename > Mitglieder** Zugriffsgruppe haben die Möglichkeit, löschen oder Ändern von Ressourcen in der Website, überlegen Sie sich die Mitgliedschaft. Wenn in unsicheren, das Websitemitglied hinzufügen die ** \<Websitename > Viewer** Zugriffsgruppe.
    
Hier ist ein Beispiel für die SharePoint-Gruppen und Access-Gruppen für eine isolierte Website mit dem Namen ProjektX.
  
![Ein Beispiel für die Verwendung von Zugriffsgruppen für eine SharePoint Online-Website mit dem Namen „ProjectX“.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a>Phase 3: Verwenden von geschachtelten Azure AD-Gruppen

Für ein Projekt, das auf eine kleine Anzahl von Personen beschränkt ist, ist es in den meisten Fällen ausreichend, den SharePoint-Gruppen der Website eine einzelne Ebene von Azure AD-basierten Zugriffsgruppen hinzuzufügen. Wenn jedoch eine große Anzahl von Personen vorhanden ist und diese Personen bereits Mitglied in bestehenden Azure AD-Gruppen sind, können Sie SharePoint-Berechtigungen einfacher mithilfe geschachtelter Gruppen zuweisen, d. h. Gruppen, die andere Gruppen als Mitglieder enthalten.
  
Beispiel: Sie möchten eine isolierte SharePoint Online-Teamwebsite für die Zusammenarbeit zwischen den Leitern der Abteilungen Vertrieb, Marketing, Technik, Recht und Support erstellen, und diese Abteilungen haben bereits eigene Gruppen mit Benutzerkonten der Führungskräfte als Mitgliedern. Anstatt eine neue Gruppe für die neuen Websitemitglieder zu erstellen und alle einzelnen Benutzerkonten der Führungskräfte hinzuzufügen, fügen Sie die vorhandenen Führungskräftegruppen für die einzelnen Abteilung zur neuen Gruppe hinzu.
  
  Wenn ein Office 365-Abonnement von mehreren Organisationen gemeinsam genutzt wird, kann eine einzelne Gruppenmitgliedschaftsebene für eine isolierte Website für eine Organisation aufgrund der schieren Anzahl von Benutzerkonten schwierig zu verwalten sein. In diesem Fall können Sie zum Verwalten der Berechtigungen geschachtelte Azure AD-Gruppen für jede Organisation verwenden, die die Gruppen innerhalb der Organisationen enthalten.
  
So verwenden Sie geschachtelte Azure AD-Gruppen:
  
1. Identifizieren oder erstellen Sie die Azure AD-Gruppen, die Benutzerkonten enthalten sollen, und fügen Sie die entsprechenden Benutzerkonten als Mitglieder hinzu.
    
2. Erstellen Sie die Azure AD-basierte Containerzugriffsgruppe, die die anderen Azure AD-Gruppen enthalten soll, und fügen Sie die Gruppen als Mitglieder hinzu.
    
3.   Um die entsprechende Zugriffsebene für die Containerzugriffsgruppe festzulegen, identifizieren Sie die SharePoint-Gruppe und die entsprechende Berechtigungsstufe.
    
> [!NOTE]
> Sie können keine geschachtelten Office 365-Gruppen verwenden. 
  
Es folgt ein Beispiel für geschachtelte Azure AD-Gruppen für die Mitgliedergruppe Access ProjektX.
  
![Ein Beispiel für geschachtelte Zugriffsgruppen für die Mitglieder der Zugriffsgruppe auf der ProjektX-Website.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
Da alle Benutzerkonten in der Research, Engineering und Project leads Teams Websitemitglieder werden sollen, ist es einfacher, ihren Azure Active Directory-Gruppen zur Gruppe Zugriff ProjektX Mitglieder hinzufügen möchten.
  
## <a name="next-step"></a>Nächster Schritt

Wenn Sie eine isolierte Website in der Produktion erstellen und konfigurieren möchten, finden Sie entsprechende Informationen unter [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Weitere Artikel

[Isolierte SharePoint Online-Teamwebsites](isolated-sharepoint-online-team-sites.md)
  
[Verwalten einer isolierten SharePoint Online-Teamwebsite](manage-an-isolated-sharepoint-online-team-site.md)

[Bereitstellen einer isolierten SharePoint Online-Teamwebsite](deploy-an-isolated-sharepoint-online-team-site.md)



