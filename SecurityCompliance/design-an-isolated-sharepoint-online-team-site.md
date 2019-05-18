---
title: Entwerfen einer isolierten SharePoint Online-Teamwebsite
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: 'Zusammenfassung: Lernen Sie die Schritte zum Entwerfen von isolierten SharePoint Online-Teamwebsites kennen.'
ms.openlocfilehash: 04634052354de47a09aa3b13e2c82d97be22f4d2
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150317"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a>Entwerfen einer isolierten SharePoint Online-Teamwebsite

 **Zusammenfassung:** Lernen Sie die Schritte zum Entwerfen von isolierten SharePoint Online-Teamwebsites kennen.
  
In diesem Artikel werden die wichtigsten Entwurfsentscheidungen erläutert, die Sie vor der Erstellung einer isolierten SharePoint Online-Teamwebsite treffen müssen.
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a>Phase 1: Ermitteln der SharePoint-Gruppen und Berechtigungsstufen

Jede SharePoint Online-Teamwebsite wird standardmäßig mit den folgenden SharePoint-Gruppen erstellt:
  
- \<Website name>-Mitglieder
    
- \<Website name> Besucher
    
- \<Website name> Besitzer
    
Diese Gruppen unterscheiden sich von Office 365- und Azure Active Directory (AD)-Gruppen und bilden die Grundlage zum Zuweisen von Berechtigungen für die Ressourcen der Website.
  
Der Satz von spezifischen Berechtigungen, der bestimmt, welche Aktionen ein Mitglied einer SharePoint-Gruppe auf einer Website ausführen kann, ist eine Berechtigungsstufe. Für eine SharePoint Online-Teamwebsite gibt es standardmäßig drei Berechtigungsstufen: Bearbeitungszugriff, Lesezugriff und Vollzugriff. In der folgenden Tabelle ist die standardmäßige Korrelation von SharePoint-Gruppen und zugewiesenen Berechtigungsstufen dargestellt:
  
|**SharePoint-Gruppe**|**Berechtigungsstufe**|
|:-----|:-----|
|\<Website name>-Mitglieder  <br/> |Bearbeiten  <br/> |
|\<Website name> Besucher  <br/> |Lesen  <br/> |
|\<Website name> Besitzer  <br/> |Vollzugriff  <br/> |
   
 **Bewährte Methode:** Sie können weitere SharePoint-Gruppen und Berechtigungsstufen erstellen. Allerdings wird empfohlen, die SharePoint-Standardgruppen und die Berechtigungsstufen für die isolierte SharePoint Online-Website zu verwenden.
  
Hier sind die standardmäßigen SharePoint-Gruppen und Berechtigungsstufen.
  
![Die SharePoint-Standardgruppen und-Berechtigungsstufen für eine SharePoint Online Website.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a>Phase 2: Zuweisen von Berechtigungen zu Benutzern mit Zugriffsgruppen

Sie können Benutzern Berechtigungen zuweisen, indem Sie ihr Benutzerkonto oder eine Office 365- oder Azure AD-Gruppe, in der das Benutzerkonto Mitglied ist, zu den SharePoint-Gruppen hinzufügen. Nach dem Hinzufügen wird den Office 365-Benutzerkonten entweder direkt oder indirekt über die Mitgliedschaft in einer Office 365- oder Azure AD-Gruppe die Berechtigungsstufe zugewiesen, die der SharePoint-Gruppe zugeordnet ist.
  
Am Beispiel der SharePoint-Standardgruppen bedeutet dies:
  
- Mitglieder der SharePoint-Gruppe Mitglieder der ** \<Website name>** , die sowohl Benutzerkonten als auch Gruppen enthalten kann, werden mit der Berechtigungsstufe **Bearbeiten** versehen.
    
- Mitglieder der SharePoint-Gruppe " ** \<Site name> Visitors** ", die sowohl Benutzerkonten als auch Gruppen enthalten kann, werden mit der Berechtigungsstufe " **Lesen** " versehen.
    
- Mitglieder der SharePoint-Gruppe " ** \<Website name> Besitzer** ", die sowohl Benutzerkonten als auch Gruppen enthalten kann, werden mit der Berechtigungsstufe " **Vollzugriff** " versehen.
    
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
|\<Website name>-Mitglieder  <br/> |\<Website name>-Mitglieder  <br/> |Bearbeiten  <br/> |
|\<Website name> Besucher  <br/> |\<Website name> Viewer  <br/> |Lesen  <br/> |
|\<Website name> Besitzer  <br/> |\<Website-name>-Administratoren  <br/> |Vollzugriff  <br/> |
   
 **Bewährte Methode:** Sie können zwar sowohl Office 365- als auch Azure AD-Gruppen als Mitglieder von SharePoint-Gruppen verwenden, wir empfehlen jedoch die Verwendung von Azure AD-Gruppen. Azure AD-Gruppen, die über Windows Server AD oder Office 365 verwaltet werden, bieten Ihnen größere Flexibilität bei der Verwendung geschachtelter Gruppen zum Zuweisen von Berechtigungen.
  
Im folgenden finden Sie die standardmäßigen SharePoint-Gruppen, die für die Verwendung von Azure AD basierten Zugriffsgruppen konfiguriert sind.
  
![Verwenden von Zugriffsgruppen als Mitglieder von Standard SharePoint Online Websitegruppen.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
Beachten Sie beim Entwerfen der drei Zugriffsgruppen die folgenden Punkte:
  
- Es sollte nur einige wenige Mitglieder in der ** \<** Zugriffsgruppe "Website-name>-Administrators" geben, die einer kleinen Anzahl von SharePoint Online Administratoren entsprechen, die die Teamwebsite verwalten.
    
- Die meisten ihrer Websitemitglieder befinden sich im ** \<Website name> Mitglieder** oder ** \<Website name> Viewer** -Zugriffsgruppen. Da Websitemitglieder in der Zugriffsgruppe ** \<Mitglieder der Website name>** die Möglichkeit haben, Ressourcen auf der Website zu löschen oder zu ändern, sollten Sie die Mitgliedschaft sorgfältig prüfen. Wenn Sie Zweifel haben, fügen Sie das Website Mitglied der Zugriffsgruppe der ** \<Website name> Viewer** hinzu.
    
Im folgenden finden Sie ein Beispiel für die SharePoint-Gruppen und Zugriffsgruppen für eine isolierte Website mit dem Namen ProjectX.
  
![Ein Beispiel für die Verwendung von Zugriffsgruppen für eine SharePoint Online Website mit dem Namen ProjectX.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
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
  
Im folgenden finden Sie ein Beispiel für geschachtelte Azure Ad Gruppen für die ProjectX-Mitglieder Zugriffsgruppe.
  
![Ein Beispiel für die Verwendung von geschachtelten Zugriffsgruppen für die Mitglieder Zugriffsgruppe für die ProjectX-Website.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
Da alle Benutzerkonten in den Teams für Forschung, Entwicklung und Projektleitung als Websitemitglieder dienen sollen, ist es einfacher, ihre Azure Ad Gruppen zur Zugriffsgruppe ProjectX-Mitglieder hinzuzufügen.
  
## <a name="next-step"></a>Nächster Schritt

Wenn Sie eine isolierte Website in der Produktion erstellen und konfigurieren möchten, finden Sie entsprechende Informationen unter [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Siehe auch

[Isolierte SharePoint Online-Teamwebsites](isolated-sharepoint-online-team-sites.md)
  
[Verwalten einer isolierten SharePoint Online-Teamwebsite](manage-an-isolated-sharepoint-online-team-site.md)

[Bereitstellen einer isolierten SharePoint Online-Teamwebsite](deploy-an-isolated-sharepoint-online-team-site.md)



