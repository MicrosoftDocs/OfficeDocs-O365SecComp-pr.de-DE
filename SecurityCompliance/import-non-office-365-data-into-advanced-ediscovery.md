---
title: Importieren von Inhalten, die nicht aus Office 365 stammen, für die Advanced eDiscovery-Analyse
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: VorGehensWeise zum Importieren von Inhalten, die nicht in O365 gespeichert sind, in einem Azure-BLOB, damit es mit AeD analysiert werden kann
ms.openlocfilehash: 1019fa2e2429aeff8bd20bc3dfb266ab5fb25eaf
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217065"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a>Importieren von Inhalten, die nicht aus Office 365 stammen, für die Advanced eDiscovery-Analyse

Nicht alle Dokumente, die Sie möglicherweise mit Office 365 Advanced eDiscovery analysieren müssen, Leben in Office 365. Mit der nicht-Office 365-Inhalts Importfunktion in Advanced eDiscovery können Sie Dokumente hochladen, die nicht in Office 365 (außer PST-Dateien) enthalten sind, in einen mit dem Azure-Speicher BLOB verknüpften Fall und diese mit Advanced eDiscovery analysieren. In diesem Verfahren wird gezeigt, wie Sie Ihre nicht-Office 365-Dokumente in Advanced eDiscovery for Analysis einbinden.
  
> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
> [!NOTE]
> Sie können ein Office 365 Advanced eDiscovery Data Storage-Add-on-Abonnement für Ihre nicht-Office 365-Inhalte erwerben. Diese ist exklusiv für Inhalte verfügbar, die mit Advanced eDiscovery analysiert werden sollen. Führen Sie die Schritte in [kaufen oder bearbeiten und Add-on für office 365 for Business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) aus, und erwerben Sie das erweiterte Office 365-eDiscovery-Speicher-Add-on. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

Für die Verwendung der in diesem Verfahren beschriebenen Funktion zum Hochladen von nicht-Office 365-Funktionen ist Folgendes erforderlich:
  
- Ein Office 365 E3 mit Advanced Compliance-Add-on oder E5-Abonnement
    
- Alle Verwalter, deren nicht-Office 365-Inhalte hochgeladen werden, müssen E3 mit Advanced Compliance-Add-on oder E5-Lizenzen haben.
    
- Ein vorhandener eDiscovery-Fall
    
- Alle Dateien zum Hochladen in Ordner, in denen ein Ordner pro Depotbank vorhanden ist, und der Name der Ordner in diesem Format *Alias @ Domainname* . *Bei dem Alias @ Domain Name* muss es sich um Benutzer von Office 365 Alias und Domäne handeln. Sie können alle *Alias @ Domain Name* -Ordner in einem Stammordner sammeln. Der Stammordner kann nur die *Alias @ Domain Name* -Ordner enthalten, es dürfen keine losen Dateien im Stammordner vorhanden sein. 
    
- Ein Konto, das entweder ein eDiscovery-Manager oder eDiscovery-Administrator ist
    
- [Microsoft Azure-Speicher Tools](https://aka.ms/downloadazcopy) , die auf einem Computer installiert sind, der Zugriff auf die nicht-Office 365-Inhaltsordner Struktur hat. 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Hochladen von nicht-Office 365-Inhalten in Advanced eDiscovery

1. Öffnen Sie **eDiscovery**als eDiscovery-Manager oder eDiscovery-Administrator, und öffnen Sie den Fall, dass die nicht-Office 365-Daten hochgeladen werden. Wenn Sie einen Fall erstellen müssen, finden Sie weitere Informationen unter [Verwalten von eDiscovery-Fällen &amp; im Office 365 Security Compliance Center](manage-ediscovery-cases.md) .
    
2. Klicken Sie auf **zu Advanced EDiscovery wechseln** .
    
3. Wählen **** Sie unter Quelltyp die Option **nicht-Office 365-Daten**aus.
    
4. Klicken Sie auf **Container hinzufügen**. Benennen Sie den Container, und fügen Sie eine Beschreibung hinzu.
    
5. Wählen Sie den neu hinzugefügten Container aus der Container Liste aus, und kopieren Sie die URL, die im Bereich Container Details angezeigt wird, und schließen Sie dann den Bereich
    
6. Öffnen Sie eine Eingabeaufforderungen als Administrator, und ändern Sie das Verzeichnis in den Ordner, in dem Sie AzCopy installiert haben.
    
7. Erstellen Sie die AzCopy-Befehlszeile, um die Dateien wie folgt hochzuladen:
    
    AzCopy/Source: " *Vollständiger Pfad zum Stammordner auf dem lokalen Computer* "/dest: "die *Container-URL bis zu dem, aber nicht mit dem?* "/DestSAS: " *Rest der Container-URL aus der? bis zum Ende* "/s 
    
    Verwenden Sie beispielsweise die folgenden Werte: 
    
  - Stammordner – C:\Collected-Daten 
    
  - Container-URL https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp-; SR =&amp;c Si = NonOfficeData15%&amp;7C0 SIG = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA% 3D
    
    die Syntax der AzCopy-Befehlszeile lautet:
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    Weitere Informationen zur Azcopy-Syntax finden Sie unter über [tragen von Daten mit dem Azcopy unter Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) . 
    
    > [!IMPORTANT]
    > Es muss ein Stammordner pro Benutzer vorhanden sein, und der Ordnername muss im *Alias @ Domainname* -Format vorliegen. 
  
8. Wechseln Sie nach dem Hochladen der Ordner zurück zu Advanced eDiscovery. Der Inhalt in den hochgeladenen Ordnern kann jetzt in Advanced eDiscovery verarbeitet werden. Wählen Sie den Container aus, und klicken Sie auf die Schaltfläche verarbeiten. Weitere Informationen zur erweiterten eDiscovery-Verarbeitung finden Sie unter [Ausführen des Process-Moduls und Laden von Daten in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
    
    > [!IMPORTANT]
    > Sobald der Container erfolgreich in Advanced eDiscovery verarbeitet wurde, können Sie dem SAS-Speicher in Azure keine neuen Inhalte mehr hinzufügen. Wenn Sie zusätzliche Inhalte sammeln und Sie dem Fall für die erweiterte eDiscovery-Analyse hinzufügen möchten, müssen Sie einen neuen **nicht-Office 365-Daten** Container erstellen und dieses Verfahren wiederholen. 
  
    > [!NOTE]
    > Wenn der Container *aufgrund von Ordner Benennungs Problemen nicht erfolgreich verarbeitet* wird und Sie dann die Probleme beheben, müssen Sie mit den Verfahren in diesem Artikel weiterhin einen neuen Container erstellen und erneut verbinden und erneut hochladen. 
  

