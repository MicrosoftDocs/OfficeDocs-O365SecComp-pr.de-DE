---
title: Set up Information Rights Management (IRM) in SharePoint admin center
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 239ce6eb-4e81-42db-bf86-a01362fed65c
description: Erfahren Sie, wie Sie SharePoint Online-IRM über Microsoft Azure Active Directory Rights Management Services (RMS) verwenden, um SharePoint-Listen und Dokumentbibliotheken zu schützen.
ms.openlocfilehash: 6b68135720846a0e74f5b0272dc5f25272381284
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260768"
---
# <a name="set-up-information-rights-management-irm-in-sharepoint-admin-center"></a>Set up Information Rights Management (IRM) in SharePoint admin center

## <a name="introduction"></a>Einführung

In SharePoint Online wird der IRM-Schutz auf Dateien auf Listen-und Bibliotheksebene angewendet. Bevor Ihre Organisation den IRM-Schutz verwenden kann, müssen Sie zunächst die Rechteverwaltung einrichten. IRM verwendet den Azure Rights Management-Dienst von Azure Information Protection, um Nutzungseinschränkungen zu verschlüsseln und zuzuweisen. Einige Office 365-Pläne schließen Azure Rights Management ein, aber nicht alle. Weitere Informationen finden Sie [unter Support für Azure Rights Management durch Office-Anwendungen und-Dienste](https://docs.microsoft.com/azure/information-protection/understand-explore/office-apps-services-support).
  
## <a name="turn-on-irm-service-using-sharepoint-admin-center"></a>Aktivieren des IRM-Diensts mithilfe des SharePoint Admin Center

Bevor Ihre Organisation SharePoint-Listen und-Bibliotheken verwalten kann, müssen Sie zunächst den Rechteverwaltungsdienst für Ihre Organisation aktivieren. Weitere Informationen finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://docs.microsoft.com/information-protection/deploy-use/activate-service). Sie müssen ein Geschäfts-oder Schulkonto verwenden, das über Office 365 globale Administratorrechte verfügt, um den Rechteverwaltungsdienst zu aktivieren. Andernfalls können Sie IRM-Features nicht mit SharePoint Online verwenden.
  
Melden Sie sich nach dem Aktivieren des Rights Management-Diensts im SharePoint Admin Center an, um IRM zu aktivieren.
  
1. Melden Sie sich bei Office 365 als globaler Administrator oder SharePoint-Administrator an.
    
2. Wählen Sie das App- ![Start Symbol in der oberen linken Ecke](media/e5aee650-c566-4100-aaad-4cc2355d909f.png) des App-start Symbols in Office 365 aus, und wählen Sie **Admin** aus, um das Office 365 Admin Center zu öffnen. (If you don't see the Admin tile, you don't have Office 365 administrator permissions in your organization.) 
    
3. Wählen Sie im linken Bereich **Admin Centers** \> **SharePoint**aus.
    
4. Wählen Sie im linken Bereich **Einstellungen**aus.
    
5. Wählen Sie im Abschnitt **Verwaltung von Informationsrechten (IRM)** **den in der Konfiguration angegebenen IRM-Dienst verwenden**aus, und wählen Sie dann **IRM-Einstellungen aktualisieren**aus. Nachdem Sie IRM-Einstellungen aktualisiert haben, können Personen in Ihrer Organisation mit der Verwendung von IRM in Ihren SharePoint-Listen und-Dokumentbibliotheken beginnen. Es kann jedoch bis zu einer Stunde dauern, bis die Optionen in den BibliotheksEinstellungen und den Listeneinstellungen angezeigt werden.
    
## <a name="irm-enable-sharepoint-document-libraries-and-lists"></a>IRM-Aktivieren von SharePoint-Dokumentbibliotheken und-Listen
<a name="__toc220831191"> </a>

Nach dem Aktualisieren der IRM-Einstellungen können Websitebesitzer Ihre SharePoint-Listen und-Dokumentbibliotheken IRM-schützen. Weitere Informationen finden Sie unter [Anwenden der Verwaltung von Informationsrechten auf eine Liste oder Bibliothek](apply-irm-to-a-list-or-library.md).
  
Wenn Websitebesitzer IRM für eine Liste oder Bibliothek aktivieren, können Sie alle unterstützten Dateitypen in dieser Liste oder Bibliothek schützen. Wenn IRM für eine Bibliothek aktiviert ist, gilt die Rechteverwaltung für alle Dateien in dieser Bibliothek. Wenn Sie IRM für eine Liste aktivieren, gilt die Rechteverwaltung nur für Dateien, die an Listenelemente angefügt sind, nicht die eigentlichen Listenelemente.
  
Wenn Benutzer Dateien in einer IRM-fähigen Liste oder Bibliothek herunterladen, werden die Dateien verschlüsselt, sodass nur autorisierte Personen Sie anzeigen können. Jede Datei mit verwalteten Rechten enthält außerdem eine Veröffentlichungslizenz, die den Personen, die die Datei anzeigen, Einschränkungen auferlegt. Zu den typischen Einschränkungen gehört das Erstellen einer schreibgeschützten Datei, das Deaktivieren des Kopierens von Text, das verhindern des Speicherns einer lokalen Kopie und das verhindern, dass Personen die Datei drucken. Client Programme, die IRM-gestützte Dateitypen lesen können, verwenden die Veröffentlichungslizenz innerhalb der Datei mit verwalteten Rechten, um diese Einschränkungen zu erzwingen. So behält eine Datei mit verwalteten Rechten ihren Schutz auch nach dem Herunterladen bei. Informationen zum Aktivieren von IRM für eine Liste oder Bibliothek finden Sie unter [Anwenden der Verwaltung von Informationsrechten auf eine Liste oder Bibliothek](apply-irm-to-a-list-or-library.md).
  
Sie können keine Dokumente in einer IRM-fähigen Bibliothek mithilfe von Office Online erstellen oder bearbeiten. Stattdessen kann eine Person zu einem Zeitpunkt IRM-verschlüsselte Dateien herunterladen und bearbeiten. Verwenden Sie das Einchecken und Auschecken, um die *gemeinsame Dokumenterstellung* oder die Erstellung über mehrere Benutzer hinweg zu verwalten. 
  
Wenn Sie eine PDF-Datei aus einer IRM-geschützten Bibliothek herunterladen, erstellt Office 365 eine geschützte PDF-Datei. Die Dateierweiterung wird nicht geändert, aber die Datei ist geschützt. Zum Anzeigen dieser Datei benötigen Sie den Azure Information Protection-Viewer, den vollständigen Azure Information Protection-Client oder eine andere Anwendung, die das Anzeigen geschützter PDF-Dateien unterstützt. 
  
SharePoint Online unterstützt die Verschlüsselung der folgenden Dateitypen:
  
- PDF
    
- Die 97-2003-Dateiformate für die folgenden Microsoft Office-Programme: Word, Excel und PowerPoint
    
- Die Office Open XML-Formate für die folgenden Microsoft Office-Programme: Word, Excel und PowerPoint
    
- XML Paper Specification (XPS)-Format
    
## <a name="next-steps"></a>Nächste Schritte
<a name="__toc220831191"> </a>

Nachdem Sie IRM für SharePoint Online aktiviert haben, können Sie mit dem Anwenden der Rechteverwaltung auf Listen und Bibliotheken beginnen. Weitere Informationen finden Sie unter [Anwenden der Verwaltung von Informationsrechten auf eine Liste oder Bibliothek](apply-irm-to-a-list-or-library.md).
  
Der neue OneDrive-synchronisierungsclient für Windows unterstützt jetzt das Synchronisieren von IRM-geschützten SharePoint-Dokumentbibliotheken und OneDrive-Speicherorten (solange die IRM-Einstellung für die Bibliothek nicht auf Ablauf von Dokumentzugriffs rechten festgelegt ist). Weitere Informationen oder erste Schritte beim Bereitstellen des neuen Synchronisierungs Clients finden Sie unter [deploy the New OneDrive Sync Client for Windows](https://support.office.com/article/3f3a511c-30c6-404a-98bf-76f95c519668).
  
[Seitenanfang](#introduction)  

