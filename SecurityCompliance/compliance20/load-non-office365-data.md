---
title: Laden von Nicht-Office 365-Daten in einen Prüfdateisatz
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
ms.openlocfilehash: 60775002d5ebec83aacbec350a044b9d6ffeb461
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834959"
---
# <a name="load-non-office-365-data-into-a-review-set"></a>Laden von Nicht-Office 365-Daten in einen Prüfdateisatz

Nicht alle Dokumente, die Sie möglicherweise mit Office 365 Advanced eDiscovery analysieren müssen, Leben in Office 365. Mit der nicht-Office 365-Inhalts Importfunktion in Advanced eDiscovery können Sie Dokumente, die in Office 365 nicht enthalten sind, in einen Übersichts Satz hochladen, sodass Sie mit Advanced eDiscovery analysiert werden. In diesem Verfahren wird gezeigt, wie Sie Ihre nicht-Office 365-Dokumente in Advanced eDiscovery for Analysis einbinden.

>[!Note]
>Advanced eDiscovery erfordert eine Office 365 E3 mit dem Advanced Compliance-Add-on oder ein E5-Abonnement für Ihre Organisation. Wenn Sie diesen Plan nicht haben und die erweiterte eDiscovery testen möchten, können Sie sich für eine Testversion von Office 365 Enterprise E5 registrieren.

## <a name="before-you-begin"></a>Bevor Sie beginnen

Für die Verwendung der in diesem Artikel beschriebenen Funktion zum Hochladen von nicht-Office 365 benötigen Sie Folgendes:

- Ein Office 365-oder Microsoft 365 E5-Abonnement oder ein E3-Abonnement mit dem Advanced Compliance-Add-on-Abonnement.

- Alle Verwalter, deren nicht-Office 365-Inhalte hochgeladen werden, müssen über eine E3-Lizenz mit einer erweiterten Compliance-Add-on-Lizenz verfügen oder über eine E5-Lizenz verfügen.

- Ein vorhandener eDiscovery-Fall.

- Die Depotbank muss dem Fall hinzugefügt werden, bevor Sie die nicht-Office 365-Daten hochladen, die Ihnen zugeordnet sind.

- Alle Dateien, die hochgeladen werden, müssen sich in Ordnern befinden, in denen jeder Ordner einem bestimmten Verwalter zugeordnet ist. Die Namen für diese Ordner müssen das folgende Benennungsformat verwenden: *Alias @ Domain*Name. Der *Alias @ Domain Name* muss der Office 365-Alias und die Domäne des Benutzers sein. Sie können alle *Alias @ Domain Name* -Ordner in einem Stammordner sammeln. Der Stammordner kann nur die *Alias @ Domain Name* -Ordner enthalten; Loose-Dateien sind im Stammordner nicht zulässig.

   Die Ordnerstruktur für die nicht-Office 365-Daten, die Sie hochladen möchten, würde beispielsweise wie folgt aussehen:

   - c:\nonO365\abraham.McMahon@contoso.com
   - c:\nonO365\jewell.Gordon@contoso.com
   - c:\nonO365\staci.Gonzalez@contoso.com

   Dabei sind Abraham.McMahon@contoso.com, Jewell.Gordon@contoso.com und Staci.Gonzalez@contoso.com die SMTP-Adressen der Verwalter in diesem Fall.

   ![Nicht-Office 365 Datenupload-Ordnerstruktur](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- Ein Konto, das entweder ein eDiscovery-Manager oder eDiscovery-Administrator ist

- Microsoft Azure-Speicher Tools, die auf einem Computer installiert sind, der Zugriff auf die nicht-Office 365-Inhaltsordner Struktur hat.

- Installieren Sie AzCopy, was Sie hier tun können:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Hochladen von nicht-Office 365-Inhalten in Advanced eDiscovery

1. Öffnen Sie als eDiscovery-Manager oder eDiscovery-Administrator Advanced eDiscovery, und führen Sie dann den Fall aus, dass die nicht-Office 365-Daten in hochgeladen werden.  Klicken Sie auf die Registerkarte überarbeits **Sätze** , und wählen Sie dann den Übersichts Satz aus, in den Sie die nicht-Office 365-Daten laden möchten.  Wenn Sie noch keinen Übersichts Satz erstellt haben, können Sie dies jetzt tun.  Klicken Sie schließlich auf **Review-Satz verwalten** , und klicken Sie dann auf **Uploads anzeigen** in der Daten Kachel * * nicht-Office 365.

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
   > Wenn der angegebene AzCopy-Befehl fehlschlägt, beziehen Sie sich auf [Problembehandlung AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)

6. Kehren Sie schließlich zur Security & Compliance zurück, und klicken Sie auf die Schaltfläche **Weiter: Process files** .  Dadurch wird die Verarbeitung, die Textextraktion und die Indizierung der hochgeladenen Dateien initiiert.  Sie können den Fortschritt der Verarbeitung hier oder auf der Registerkarte **Aufträge** nachverfolgen.  Sobald der Vorgang abgeschlossen ist, sind die neuen Dateien im Übersichts Satz verfügbar.  Nach Abschluss der Verarbeitung können Sie den Assistenten schließen.

   ![Nicht-Office 365-Import-Prozessdateien](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

