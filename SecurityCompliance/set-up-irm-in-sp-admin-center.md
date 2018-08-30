---
title: Festlegen von Information Rights Management (IRM) im SharePoint Administrationscenter
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 239ce6eb-4e81-42db-bf86-a01362fed65c
description: Hier erfahren Sie, wie Sie SharePoint Online IRM über Microsoft Azure Active Directory Rights Management Services (RMS) zum Schutz von SharePoint-Listen und Dokumentbibliotheken.
ms.openlocfilehash: dea8c71ce67207b3c40a1f934f90e63740f70f29
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529453"
---
# <a name="set-up-information-rights-management-irm-in-sharepoint-admin-center"></a>Festlegen von Information Rights Management (IRM) im SharePoint Administrationscenter

In SharePoint Online ist IRM-Schutz auf Dateien auf der Listen- und Bibliotheksdaten angewendet. Bevor Ihre Organisation IRM-Schutz verwenden kann, müssen Sie zuerst Verwaltung von Informationsrechten einrichten. IRM nutzt die Azure Rights Management Service von Azure Information Protection verschlüsseln und Zuweisen von Usage Einschränkungen. Einige Office 365-Pläne enthalten Azure Rights Management, jedoch nicht alle. Weitere Informationen finden lesen Sie, [wie Office-Programme und Dienste Azure Rights Management unterstützen](https://docs.microsoft.com/azure/information-protection/understand-explore/office-apps-services-support).
  
## <a name="turn-on-irm-service-using-sharepoint-admin-center"></a>Aktivieren der IRM-Dienst mithilfe von SharePoint Administrationscenter

Vor Ihrer Organisation können IRM-Schutz von SharePoint-Listen und Bibliotheken, müssen Sie zuerst den Verwaltung von Informationsrechten-Dienst für Ihre Organisation aktivieren. Um Hier erfahren, wie finden Sie unter [Aktivieren von Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/activate-service). Sie müssen ein Konto arbeiten oder Schule verwenden, die Office 365 globaler Administrator-Berechtigungen zum Aktivieren des Verwaltung von Informationsrechten-Diensts verfügt. Andernfalls wird nicht Sie IRM-Funktionen mit SharePoint Online verwenden können.
  
Nach der Aktivierung des Verwaltung von Informationsrechten-Diensts, melden sich bei der SharePoint-Verwaltungskonsole zum Aktivieren von IRM.
  
1. Melden Sie sich bei Office 365 als globaler Administrator oder SharePoint-Administrator an.
    
2. Wählen Sie das App-Startfeldsymbol ![App-Startfeldsymbol in Office 365](media/e5aee650-c566-4100-aaad-4cc2355d909f.png) in der oberen linken Ecke, und wählen Sie **Admin**, um das Office 365 Admin Center zu öffnen. (Wenn die Administratorkachel nicht angezeigt wird, besitzen Sie keine Office 365-Administratorberechtigungen in Ihrer Organisation.) 
    
3. Wählen Sie im linken Bereich **Admin zentriert** \> **SharePoint**.
    
4. Wählen Sie im linken Bereich **Einstellungen**aus.
    
5. Klicken Sie im Abschnitt **(Information Rights Management, IRM)** wählen Sie aus, **Verwenden Sie den IRM-Dienst in Ihrer Konfiguration festgelegt**, und dann **Aktualisieren IRM-Einstellungen**. Nachdem Sie IRM-Einstellungen aktualisieren, können Personen in Ihrer Organisation mithilfe von IRM in ihre SharePoint-Listen und Dokumentbibliotheken beginnen. Allerdings können die Optionen dazu zu einer Stunde dauern, bis in der Bibliothek und Listeneinstellungen angezeigt werden.
    
## <a name="irm-enable-sharepoint-document-libraries-and-lists"></a>IRM-Enable SharePoint-Dokumentbibliotheken und Listen
<a name="__toc220831191"> </a>

Nach der Aktualisierung von IRM-Einstellungen, die Websitebesitzer können IRM-Schutz ihrer SharePoint-Listen und Dokumentbibliotheken. Weitere Informationen finden Sie unter [Information Rights Management zu einer Liste oder Bibliothek anwenden](apply-irm-to-a-list-or-library.md).
  
Wenn die Websitebesitzer IRM für eine Liste oder Bibliothek aktivieren, können sie alle unterstützten Dateitypen in dieser Liste oder Bibliothek schützen. Wenn IRM für eine Dokumentbibliothek aktiviert ist, gilt die Verwaltung von Informationsrechten für alle Dateien in dieser Bibliothek. Bei Aktivierung von IRM für eine Liste Betrifft die Verwaltung von Informationsrechten nur Dateien, die Listenelemente, nicht die tatsächliche Listenelemente angefügt sind.
  
Wenn Benutzer Dateien in einer IRM-fähigen Liste oder Bibliothek herunterladen, werden die Dateien verschlüsselt, so dass nur autorisierte Personen angezeigt werden können. Jede Datei mit verwalteten rechten enthält außerdem eine Veröffentlichungslizenz, die erfordert Einschränkungen auf die Personen, die die Datei anzeigen. Typische Einschränkungen enthalten eine Datei schreibgeschützt, deaktivieren das Kopieren von Text, die verhindern, dass Personen aus eine lokale Kopie gespeichert und verhindert, dass Personen die Datei drucken zu machen. Clientprogramme, die IRM-unterstützten Dateitypen lesen können verwenden der Veröffentlichungslizenz innerhalb der Datei mit verwalteten rechten zum Erzwingen von dieser Beschränkungen. Dies ist wie eine Datei mit verwalteten rechten seinen Schutz behält auch nach dem sie heruntergeladen wird. Zum Aktivieren von IRM für eine Liste oder Bibliothek finden Sie unter [Information Rights Management zu einer Liste oder Bibliothek anwenden](apply-irm-to-a-list-or-library.md).
  
Erstellen oder Bearbeiten von Dokumenten in einer IRM-fähigen Bibliothek mit Office Online. Stattdessen kann von einer Person zu einem Zeitpunkt herunterladen und Bearbeiten von IRM-verschlüsselten Dateien. Verwenden Sie ein- und Auschecken zum Verwalten von *gemeinsamen dokumenterstellung* oder authoring auf mehrere Benutzer. 
  
Wenn Sie eine PDF-Datei aus einer IRM-geschützten-Bibliothek herunterladen, erstellt Office 365 geschützte PDF-Datei. Die Erweiterung der Datei wird nicht geändert, aber die Datei ist geschützt. Zum Anzeigen dieser Datei benötigen Sie Azure Information Protection-Viewer, der vollständige Azure Information Protection-Client oder einer anderen Anwendung, die Wiedergabe unterstützt geschützte PDF-Dateien. 
  
SharePoint Online unterstützt die Verschlüsselung der folgenden Dateitypen:
  
- PDF
    
- Die 97-2003-Dateiformate für die folgenden Microsoft Office-Programme: Word, Excel und PowerPoint
    
- Office Open XML-Formaten für die folgenden Microsoft Office-Programme: Word, Excel und PowerPoint
    
- Das Format der XML Paper Specification (XPS)
    
## <a name="next-steps"></a>Nächste Schritte
<a name="__toc220831191"> </a>

Wenn Sie IRM für SharePoint Online aktiviert haben, können Sie die Verwaltung von Informationsrechten auf Listen und Bibliotheken anwenden starten. Informationen finden Sie unter [Information Rights Management zu einer Liste oder Bibliothek anwenden](apply-irm-to-a-list-or-library.md).
  
Die neue OneDrive-Synchronisierungsclient für Windows unterstützt jetzt synchronisieren von IRM-geschützten SharePoint-Dokumentbibliotheken und OneDrive Speicherorte (sofern nicht die IRM-Einstellung für die Bibliothek an, die ablaufen Dokument durch den Zugriffsrechte festgelegt). Weitere Informationen oder die ersten Schritte beim Bereitstellen des neuen Sync-Clients finden Sie unter [Bereitstellen der neuen OneDrive-Synchronisierungsclient für Windows](https://support.office.com/article/3f3a511c-30c6-404a-98bf-76f95c519668).
  
[Seitenanfang](set-up-irm-in-sp-admin-center.md#__top)
  

