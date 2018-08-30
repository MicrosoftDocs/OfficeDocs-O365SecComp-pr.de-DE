---
title: Importieren von Inhalten für die erweiterte eDiscovery Analyse nicht - Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Wie BLOB-Schritten zum Importieren von Inhalt, die nicht in einer Azure in O365 gespeichert ist, damit es mit AeD analysiert werden kann
ms.openlocfilehash: ab6c7ac76a159603a34719aa8edb51de3a4fabbb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530115"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a>Importieren von Inhalten für die erweiterte eDiscovery Analyse nicht - Office 365

Nicht alle Dokumente, die Sie möglicherweise zur Analyse mit Office 365 erweiterte eDiscovery werden in Office 365 live. Importieren Sie mit dem Inhalt nicht Office 365-Feature in erweiterten eDiscovery Sie Dokumente hochladen können, die nicht in Office 365 (mit Ausnahme von PST-Dateien) in ein Blob Groß-/Kleinschreibung verknüpfte Azure Storage live und mit erweiterten eDiscovery zu analysieren. Dieses Verfahren wird veranschaulicht, wie Sie Ihre nicht - Office 365-Dokumente in erweiterten eDiscovery für die Analyse bringen.
  
> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
> [!NOTE]
> Sie können für Ihre nicht - Office 365-Inhalte ein Office 365 erweiterte eDiscovery Daten Speicher Add-on-Abonnement erwerben. Dies ist für Inhalte, die mit erweiterten eDiscovery analysiert werden ausschließlich zur Verfügung. Führen Sie die Schritte in [erwerben oder bearbeiten und Add-on für Office 365 für Unternehmen](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) und erwerben Sie das Office 365 erweiterte eDiscovery Speicher Add-on. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

Verwendung des Upload nicht Office 365-Features, wie in diesem Verfahren beschrieben muss vorhanden sein:
  
- Ein Office 365 E3 mit erweiterte Compliance Add-on oder E5 Abonnement
    
- Alle Verwalter, dessen Inhalt nicht - Office 365 hochgeladen werden, müssen mit erweiterte Compliance Add-on oder E5 Lizenzen E3 verfügen.
    
- Eine vorhandene eDiscovery-Fall
    
- Alle zum Hochladen von Dateien in den Ordner, in dem ein Ordner pro Verwaltungsberechtigter vorhanden ist und die Ordner Name befindet sich in diesem Format *Alias@DomainName,* gesammelt werden. Die *alias@domainname* müssen Office 365-Benutzeralias und die Domäne sein. Sie können alle *alias@domainname* Ordner in einem Stammordner zusammenfassen. Stammordner kann nur die *alias@domainname* Ordner enthalten, es muss keine losen Dateien im Stammordner 
    
- Ein Konto, das entweder eine eDiscovery-Manager oder eine eDiscovery-Administrator ist
    
- [Microsoft Azure-Speicher-Tools](https://aka.ms/downloadazcopy) auf einem Computer mit Zugriff auf die Struktur des nicht - Office 365 Content-Ordner installiert. 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Hochladen Sie nicht - Office 365-Inhalte in erweiterten eDiscovery

1. Als eDiscovery-Manager oder eDiscovery-Administrator öffnen Sie **eDiscovery**, und öffnen Sie die Groß-/Kleinschreibung, der die Daten nicht - Office 365 zu hochgeladen werden soll. Wenn Sie eine Anfrage erstellen müssen, finden Sie unter [Verwalten von eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](manage-ediscovery-cases.md)
    
2. Klicken Sie auf **Wechseln zu erweiterten eDiscovery**
    
3. Wählen Sie unter **Typ der Datenquelle** **nicht Office 365-Daten**.
    
4. Klicken Sie auf **Add Container**. Nennen Sie den Container, und fügen Sie eine Beschreibung hinzu.
    
5. Wählen Sie den neu hinzugefügten Container aus der Containerliste, und kopieren Sie die URL, die im Detailbereich Container angezeigt wird, und schließen Sie den Bereich
    
6. Öffnen Sie ein Eingabeaufforderungsfenster als Administrator, und wechseln Sie zum Verzeichnis zum Ordner, in dem Sie AzCopy installiert haben.
    
7. Erstellen Sie die Befehlszeile AzCopy zum Hochladen von Dateien wie folgt:
    
    AzCopy/Source: " *vollständigen Pfad zum Stammordner auf lokalen Computer* " / dest: " *Container URLs bis, aber nicht einschließlich der?* " /DestSAS: " *Rest der Container-Url aus der? zum Ende* "/ S. 
    
    Beispielsweise mithilfe der folgenden Werte: 
    
  - Stammordner - C:\Collected Daten 
    
  - Container-Url - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;Si NonOfficeData15 = %7 C 0&amp;Sig = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA % 3D
    
    die Befehlszeilensyntax AzCopy wäre:
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    Weitere Informationen zu Azcopy Syntax finden Sie unter, [Übertragen von Daten mit der AzCopy auf Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) . 
    
    > [!IMPORTANT]
    > Es muss ein Stammordner pro Benutzer und der Name des Ordners muss im Format *alias@domainname* . 
  
8. Nachdem die Ordner hochladen haben, wechseln Sie wieder zur erweiterten eDiscovery. Der Inhalt in den Ordnern, die Sie hochgeladen haben kann jetzt im erweiterten eDiscovery verarbeitet werden. Wählen Sie den Container, und klicken Sie auf die Schaltfläche Prozess. Weitere Informationen zu erweiterten eDiscovery Verarbeitung finden Sie unter, [Führen Sie das Modul Prozess und Laden von Daten in Office 365 erweiterte eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
    
    > [!IMPORTANT]
    > Nachdem Sie der Container in der erweiterten eDiscovery erfolgreich verarbeitet wird, werden Sie nicht mehr, neuen Inhalt hinzuzufügen, um die SAS-Speicher in Azure sein. Wenn Sie zusätzliche Inhalte sammeln und Sie es die Groß-/Kleinschreibung für die erweiterte eDiscovery-Analyse hinzufügen möchten, müssen Sie einen neuen Container **nicht Office 365-Daten** erstellen und wiederholen Sie dieses Verfahren. 
  
    > [!NOTE]
    > Wenn der Container *verarbeitet nicht erfolgreich aufgrund Ordner naming Probleme* und Sie dann die Probleme beheben, müssen Sie zum Erstellen einer neuen Container und die Verbindung wiederherstellen und hochladen, erneut mit den Verfahren in diesem Artikel. 
  

