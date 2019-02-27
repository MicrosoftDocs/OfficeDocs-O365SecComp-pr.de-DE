---
title: Laden von Nicht-Office 365-Daten in einen Arbeitssatz
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: b177fc292c748f21907621196dc28d6b8fe17959
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296788"
---
# <a name="load-non-office-365-data-into-a-working-set"></a>Laden von Nicht-Office 365-Daten in einen Arbeitssatz

Nicht alle Dokumente, die Sie möglicherweise mit Office 365 Advanced eDiscovery analysieren müssen, Leben in Office 365. Mit der nicht-Office 365-Inhalts Importfunktion in Advanced eDiscovery können Sie Dokumente, die nicht in Office 365 Leben, in einen Arbeitssatz hochladen, sodass Sie mit Advanced eDiscovery analysiert werden. In diesem Verfahren wird gezeigt, wie Sie Ihre nicht-Office 365-Dokumente in Advanced eDiscovery for Analysis einbinden.

>[!Note]
>Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich für eine Testversion von Office 365 Enterprise E5 anmelden.

## <a name="before-you-begin"></a>Bevor Sie beginnen
Für die Verwendung der in diesem Verfahren beschriebenen Funktion zum Hochladen von nicht-Office 365-Funktionen ist Folgendes erforderlich:

- Ein Office 365 E3 mit Advanced Compliance-Add-on oder E5-Abonnement.

- Alle Verwalter, deren nicht-Office 365-Inhalte hochgeladen werden, müssen E3 mit Advanced Compliance Add-on oder E5-Lizenzen haben.

- Ein vorhandener eDiscovery-Fall.

- Alle Dateien zum Hochladen in Ordner, in denen ein Ordner pro Depotbank vorhanden ist, und der Name der Ordner in diesem Format *Alias @ Domainname* . *Bei dem Alias @ Domain Name* muss es sich um Benutzer von Office 365 Alias und Domäne handeln. Sie können alle *Alias @ Domain Name* -Ordner in einem Stammordner sammeln. Der Stammordner kann nur die *Alias @ Domain Name* -Ordner enthalten, es dürfen keine losen Dateien im Stammordner vorhanden sein.

- Ein Konto, das entweder ein eDiscovery-Manager oder ein eDiscovery-Administrator ist, Microsoft Azure-Speicher Tools, die auf einem Computer installiert sind, der Zugriff auf die nicht-Office 365-Inhaltsordner Struktur hat.

- Installieren Sie AzCopy, was Sie hier tun können:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Hochladen von nicht-Office 365-Inhalten in Advanced eDiscovery

1. Öffnen Sie als eDiscovery-Manager oder eDiscovery-Administrator Advanced eDiscovery, und führen Sie dann den Fall aus, dass die nicht-Office 365-Daten in hochgeladen werden.  Klicken Sie auf die Registerkarte **Working Sets** , und wählen Sie dann den Arbeitssatz aus, in den Sie die nicht-Office 365-Daten laden möchten.  Wenn Sie noch keine Arbeitsmappe erstellt haben, können Sie dies jetzt tun.  Klicken Sie abschließend auf Workings- **Set verwalten** und dann auf **Uploads** im nicht-Office 365-Datenabschnitt

2. Klicken Sie auf die Schaltfläche **Dateien hochladen** , um den nicht-Office 365-Datenimport-Assistenten zu starten.

![Hochladen von Dateien](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. Im ersten Schritt des Assistenten wird ein sicheres Azure-BLOB für die hochzuladenden Dateien vorbereitet.  Wenn die Vorbereitung compelted ist, klicken Sie auf die Schaltfläche **Weiter: Dateien hochladen** .

![Nicht-Office 365-Import-Prepare](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. Geben Sie im Schritt **Dateien hochladen** den **Pfad zum Speicherort von Dateien**an, in dem sich die nicht von Office 365-Daten, die Sie beim Importieren einplanen, befinden.  Durch Festlegen des korrekten Speicherorts wird sichergestellt, dass der AzCopy-Befehl ordnungsgemäß aktualisiert wird.

> [!NOTE]
> Wenn Sie AzCopy noch nicht installiert haben, können Sie dies hier tun:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. Kopieren Sie den vordefinierten Befehl, indem Sie auf den Link **in die Zwischenablage kopieren** klicken. Starten Sie eine Windows-Eingabeaufforderungen, fügen Sie den Befehl ein, und drücken Sie die EINGABETASTE.  Die Dateien werden für den nächsten Schritt in den Secure Azure BLOB-Speicher hochgeladen.

![Nicht-Office 365 Import-Uploaddateien](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Nicht-Office 365-Import-AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. Kehren Sie schließlich zur Security & Compliance zurück, und klicken Sie auf die Schaltfläche **Weiter: Process files** .  Dadurch wird die Verarbeitung, die Textextraktion und die Indizierung der hochgeladenen Dateien initiiert.  Sie können den Fortschritt der Verarbeitung hier oder auf der Registerkarte **Aufträge** nachverfolgen.  Sobald der Vorgang abgeschlossen ist, sind die neuen Dateien im Arbeitssatz verfügbar.  Nach Abschluss der Verarbeitung können Sie den Assistenten schließen.

![Nicht-Office 365-Import-Prozessdateien](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

