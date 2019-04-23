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
ms.openlocfilehash: 2ac12cf8c447e3341724d9e853da0f32b7c232fb
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958696"
---
# <a name="load-non-office-365-data-into-a-working-set"></a>Laden von Nicht-Office 365-Daten in einen Arbeitssatz

Nicht alle Dokumente, die Sie möglicherweise mit Office 365 Advanced eDiscovery analysieren müssen, Leben in Office 365. Mit der nicht-Office 365-Inhalts Importfunktion in Advanced eDiscovery können Sie Dokumente, die nicht in Office 365 Leben, in einen Arbeitssatz hochladen, sodass Sie mit Advanced eDiscovery analysiert werden. In diesem Verfahren wird gezeigt, wie Sie Ihre nicht-Office 365-Dokumente in Advanced eDiscovery for Analysis einbinden.

>[!Note]
>Advanced eDiscovery erfordert eine Office 365 E3 mit dem Advanced Compliance-Add-on oder ein E5-Abonnement für Ihre Organisation. Wenn Sie diesen Plan nicht haben und die erweiterte eDiscovery testen möchten, können Sie sich für eine Testversion von Office 365 Enterprise E5 registrieren.

## <a name="before-you-begin"></a>Bevor Sie beginnen
Für die Verwendung der in diesem Verfahren beschriebenen Funktion zum Hochladen von nicht-Office 365-Funktionen ist Folgendes erforderlich:

- Ein Office 365 E3 mit Advanced Compliance-Add-on oder E5-Abonnement.

- Alle Verwalter, deren nicht-Office 365-Inhalte hochgeladen werden, müssen E3 mit Advanced Compliance Add-on oder E5-Lizenzen haben.

- Ein vorhandener eDiscovery-Fall.

- Alle Dateien zum Hochladen in Ordner, in denen ein Ordner pro Depotbank vorhanden ist, und der Name der Ordner in diesem Format *Alias @ Domainname* . *Bei dem Alias @ Domain Name* muss es sich um Benutzer von Office 365 Alias und Domäne handeln. Sie können alle *Alias @ Domain Name* -Ordner in einem Stammordner sammeln. Der Stammordner kann nur die *Alias @ Domain Name* -Ordner enthalten, es dürfen keine losen Dateien im Stammordner vorhanden sein.

   Die Ordnerstruktur für die nicht-Office 365-Daten, die Sie hochladen möchten, sollte ungefähr wie folgt aussehen:

   - c:\nonO365\abraham.mcmahon@contoso.com
   - c:\nonO365\jewell.gordon@contoso.com
   - c:\nonO365\staci.gonzalez@contoso.com

   Dabei sind abraham.mcmahon@contoso.com, jewell.gordon@contoso.com und staci.gonzalez@contoso.com die SMTP-Adressen der Verwalter in diesem Fall.

![Nicht-Office 365 Datenupload-Ordnerstruktur](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- Ein Konto, das entweder ein eDiscovery-Manager oder ein eDiscovery-Administrator ist, Microsoft Azure-Speicher Tools, die auf einem Computer installiert sind, der Zugriff auf die nicht-Office 365-Inhaltsordner Struktur hat.

- Installieren Sie AzCopy, was Sie hier tun können:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Hochladen von nicht-Office 365-Inhalten in Advanced eDiscovery

1. Öffnen Sie als eDiscovery-Manager oder eDiscovery-Administrator Advanced eDiscovery, und führen Sie dann den Fall aus, dass die nicht-Office 365-Daten in hochgeladen werden.  Klicken Sie auf die Registerkarte **Working Sets** , und wählen Sie dann den Arbeitssatz aus, in den Sie die nicht-Office 365-Daten laden möchten.  Wenn Sie noch keine Arbeitsmappe erstellt haben, können Sie dies jetzt tun.  Klicken Sie abschließend auf " **Arbeitsbereiche verwalten** " und dann auf " **Uploads** " im Abschnitt "nicht-Office 365-Daten".

2. Klicken Sie auf die Schaltfläche **Dateien hochladen** , um den nicht-Office 365-Datenimport-Assistenten zu starten.

![Hochladen von Dateien](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. Im ersten Schritt des Assistenten wird ein sicheres Azure-BLOB für die hochzuladenden Dateien vorbereitet.  Klicken Sie nach Abschluss der Vorbereitung auf die Schaltfläche **Weiter: Dateien hochladen** .

![Nicht-Office 365-Import-Prepare](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. Geben Sie im Schritt **Dateien hochladen** den **Pfad zum Speicherort von Dateien**an, in dem sich die nicht von Office 365-Daten, die Sie beim Importieren einplanen, befinden.  Durch Festlegen des korrekten Speicherorts wird sichergestellt, dass der AzCopy-Befehl ordnungsgemäß aktualisiert wird.

> [!NOTE]
> Wenn Sie AzCopy noch nicht installiert haben, können Sie dies hier tun:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. Kopieren Sie den vordefinierten Befehl, indem Sie auf den Link **in die Zwischenablage kopieren** klicken. Starten Sie eine Windows-Eingabeaufforderungen, fügen Sie den Befehl ein, und drücken Sie die EINGABETASTE.  Die Dateien werden für den nächsten Schritt in den Secure Azure BLOB-Speicher hochgeladen.

![Nicht-Office 365 Import-Uploaddateien](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Nicht-Office 365-Import-AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

> [!NOTE]
> Wenn der angegebene AzCopy-Befehl fehlschlägt, finden Sie weitere Informationen unter [Problembehandlung von AzCopy in Advanced eDiscovery (Preview)](troubleshooting-azcopy.md)

6. Kehren Sie schließlich zur Security & Compliance zurück, und klicken Sie auf die Schaltfläche **Weiter: Process files** .  Dadurch wird die Verarbeitung, die Textextraktion und die Indizierung der hochgeladenen Dateien initiiert.  Sie können den Fortschritt der Verarbeitung hier oder auf der Registerkarte **Aufträge** nachverfolgen.  Sobald der Vorgang abgeschlossen ist, sind die neuen Dateien im Arbeitssatz verfügbar.  Nach Abschluss der Verarbeitung können Sie den Assistenten schließen.

![Nicht-Office 365-Import-Prozessdateien](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

