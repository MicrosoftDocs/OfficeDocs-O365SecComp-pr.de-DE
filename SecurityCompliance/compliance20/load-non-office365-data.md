---
title: Laden von Nicht-Office 365-Daten in einen Arbeitssatz
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 1dad52075303450673e7f48b87e2952e35629a5e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706086"
---
# <a name="load-non-office-365-data-into-a-working-set"></a>Laden von Nicht-Office 365-Daten in einen Arbeitssatz

Nicht alle Dokumente, die Sie möglicherweise zur Analyse mit Office 365 erweiterte eDiscovery werden in Office 365 live. Importieren Sie mit dem Inhalt nicht Office 365-Feature in erweiterten eDiscovery Sie Dokumente hochladen können, die in Office 365 in einer Arbeitssatz live nicht, damit diese mit erweiterten eDiscovery analysiert werden. Dieses Verfahren wird veranschaulicht, wie Sie Ihre nicht - Office 365-Dokumente in erweiterten eDiscovery für die Analyse bringen.

>[!Note]
>Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich für eine Testversion von Office 365 Enterprise E5 anmelden.

## <a name="before-you-begin"></a>Bevor Sie beginnen:
Verwendung des Upload nicht Office 365-Features, wie in diesem Verfahren beschrieben muss vorhanden sein:

- Ein Office 365 E3 mit erweiterte Compliance Add-on oder E5 Abonnement.

- Alle Verwalter, dessen Inhalt nicht - Office 365 hochgeladen werden soll, müssen E3 mit erweiterte Compliance Add-on oder E5 Lizenzen verfügen.

- Eine vorhandene eDiscovery-Fall.

- Alle zum Hochladen von Dateien in den Ordner, in dem ein Ordner pro Verwaltungsberechtigter vorhanden ist und die Ordner Name befindet sich in diesem Format *Alias@DomainName,* gesammelt werden. Die *alias@domainname* müssen Office 365-Benutzeralias und die Domäne sein. Sie können alle *alias@domainname* Ordner in einem Stammordner zusammenfassen. Stammordner kann nur die *alias@domainname* Ordner enthalten, es muss keine losen Dateien im Stammordner gespeichert.

- Ein Konto, das entweder ein eDiscovery-Manager oder eDiscovery Microsoft Azure Storage Administratortools auf einem Computer mit Zugriff auf die Struktur des nicht - Office 365 Content-Ordner installiert ist.

- Installieren Sie AzCopy, was hier möglich:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Hochladen Sie nicht - Office 365-Inhalte in erweiterten eDiscovery

1. Öffnen Sie als ein eDiscovery-Manager oder eine eDiscovery-Administrator erweiterte eDiscovery, und klicken Sie dann auf die Groß-/Kleinschreibung, der die Daten nicht - Office 365 zu hochgeladen werden soll.  Klicken Sie auf der Registerkarte **legt arbeiten** , und wählen Sie dann des Arbeitssatzes, die, dem Sie die Daten nicht-Office 365 zu laden möchten.  Wenn Sie nicht bereits ein Arbeitssatz erstellt haben, können Sie dies jetzt tun.  Klicken Sie abschließend auf **Verwalten Funktionsweise festgelegt** und dann **Uploads anzeigen** im Datenabschnitt nicht Office 365

2. Klicken Sie auf die Schaltfläche **Dateien hochladen** , um den nicht-Office 365-Assistenten zu starten.

![Hochladen von Dateien](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. Der erste Schritt im Assistenten bereitet einfach einen sicheren Azure Blob für die Dateien hochgeladen werden.  Nach der Vorbereitung Compelted ist, klicken Sie auf die **Weiter: Hochladen von Dateien** Schaltfläche.

![Nicht-Office 365 importieren – vorbereiten](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. **Hochladen von Dateien** im Schritt geben Sie den **Pfad zum Speicherort der Dateien**, ist dies, in die nicht-Office 365-Daten, die Sie zum Importieren von planen gespeichert ist.  Festlegen des richtigen Speicherorts wird der AzCopy Befehl ordnungsgemäß aktualisiert wird sichergestellt.

> [!NOTE]
> Wenn Sie AzCopy noch nicht installiert haben, können Sie hier dazu:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. Kopieren Sie den vordefinierten Befehl durch Klicken auf den Link **in die Zwischenablage kopieren** . Starten einer Windows-Eingabeaufforderung, fügen Sie den Befehl ein, und drücken Sie die EINGABETASTE.  Die Dateien werden in der sicheren Azure BLOB-Speicher für den nächsten Schritt hochgeladen werden.

![Importieren von nicht-Office 365 - Hochladen von Dateien](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importieren von nicht-Office 365 - AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. Schließlich zum der & Security Compliance zurückzukehren, und klicken Sie auf die **Weiter: Dateien verarbeiten** Schaltfläche.  Dies wird initiiert Verarbeitung Extraktion von Text und Indizieren der hochgeladenen Dateien.  Sie können den Fortschritt der Verarbeitung hier oder auf der Registerkarte **Aufträge** verfolgen.  Sobald abgeschlossen ist, werden die neuen Dateien in den Arbeitsseiten verfügbar sein.  Nach Abschluss der Verarbeitung können Sie den Assistenten schließen.

![Importieren von nicht-Office 365 - Dateien](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

