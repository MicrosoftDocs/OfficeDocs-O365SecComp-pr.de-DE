---
title: Laden von Nicht-Office 365-Daten in einen Prüfdateisatz
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 86d858994f95176ea4d415405c4043f7e7c5308e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155007"
---
# <a name="load-non-office-365-data-into-a-review-set"></a>Laden von Nicht-Office 365-Daten in einen Prüfdateisatz

Nicht alle Dokumente, die Sie möglicherweise mit Office 365 Advanced eDiscovery analysieren müssen, werden in Office 365 Live verwendet. Mit der nicht Office 365en Inhalts Importfunktion in Advanced eDiscovery können Sie Dokumente, die nicht in Office 365 Leben, in einen Überprüfungs hochladen, damit diese mit Advanced eDiscovery analysiert werden. In diesem Verfahren erfahren Sie, wie Sie Ihre nicht-Office 365-Dokumente zur Analyse in Advanced eDiscovery integrieren.

>[!Note]
>Advanced eDiscovery erfordert eine Office 365 E3 mit dem Advanced Compliance-Add-on oder ein E5-Abonnement für Ihre Organisation. Wenn Sie diesen Plan nicht haben und Advanced eDiscovery testen möchten, können Sie sich für eine Testversion von Office 365 Enterprise E5 anmelden.

## <a name="before-you-begin"></a>Bevor Sie beginnen

Wenn Sie das Feature "nicht Office 365 hochladen" wie in diesem Artikel beschrieben verwenden, müssen Sie über Folgendes verfügen:

- Ein Office 365-oder Microsoft 365 E5-Abonnement oder ein E3-Abonnement mit dem Add-on-Abonnement für erweiterte Kompatibilität.

- Alle Verwalter, deren nicht Office 365 Inhalt hochgeladen wird, müssen über eine E3-Lizenz mit einer Add-on-Lizenz für Advanced Compliance verfügen oder über eine E5-Lizenz verfügen.

- Ein vorhandener erweiterter eDiscovery-Fall.

- Verwalter müssen dem Fall hinzugefügt werden, bevor Sie die nicht Office 365 Daten hochladen, die Ihnen zugeordnet sind.

- Alle hochzuladenden Dateien müssen sich in Ordnern befinden, in denen jeder Ordner einer bestimmten Depotbank zugeordnet ist. Für die Namen dieser Ordner muss das folgende Benennungsformat verwendet werden: *Alias @ Domain*Name. Der *Alias @ Domain Name* muss der Office 365 Alias und die Domäne des Benutzers sein. Sie können alle Alias- *@ Domain Name* -Ordner in einem Stammordner sammeln. Der Stammordner kann nur die Ordner *Alias @ Domain Name* enthalten; Loose-Dateien sind im Stammordner nicht zulässig.

   Beispielsweise ähnelt die Ordnerstruktur für die nicht Office 365 Daten, die Sie hochladen möchten, etwa wie folgt:

   - c:\nonO365\abraham.McMahon@contoso.com
   - c:\nonO365\jewell.Gordon@contoso.com
   - c:\nonO365\staci.Gonzalez@contoso.com

   Dabei sind Abraham.McMahon@contoso.com, Jewell.Gordon@contoso.com und Staci.Gonzalez@contoso.com die SMTP-Adressen der Verwalter in dem Fall.

   ![Ordnerstruktur für nicht Office 365E Datenuploads](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- Ein Konto, das entweder eDiscovery-Manager oder eDiscovery-Administrator ist

- Microsoft Azure Speicher Tools, die auf einem Computer installiert sind, der Zugriff auf die Struktur nicht Office 365 Inhaltsordner hat.

- Installieren Sie AzCopy, was Sie von hier aus tun können:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Hochladen nicht Office 365er Inhalte in die erweiterte eDiscovery

1. Öffnen Sie als eDiscovery-Manager oder eDiscovery-Administrator Advanced eDiscovery, dann werden die nicht Office 365-Daten hochgeladen.  Klicken Sie auf die Registerkarte Überprüfungs **Sätze** , und wählen Sie dann den Überprüfungs Satz aus, in den Sie die nicht Office 365 Daten laden möchten.  Wenn Sie noch keinen Überprüfungs Sätze erstellt haben, können Sie dies jetzt tun.  Klicken Sie schließlich auf **Überarbeitungs Gruppe verwalten** , und klicken Sie dann auf **Uploads anzeigen** in der * * nicht Office 365 Daten Kachel.

2. Klicken Sie auf die Schaltfläche **Dateien hochladen** , um den nicht Office 365 Datenimport-Assistenten zu starten.

   ![Hochladen von Dateien](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. Im ersten Schritt des Assistenten wird einfach ein sicheres Azure-BLOB für die zu hochzuladenden Dateien vorbereitet.  Nachdem die Vorbereitung abgeschlossen ist, klicken Sie auf die Schaltfläche **Weiter: Dateien hochladen** .

   ![Nicht Office 365 Import – Prepare](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. Geben Sie im Schritt **Upload Files** den **Pfad zum Speicherort der Dateien**an, hier befinden sich die nicht Office 365 Daten, die Sie beim Import planen.  Durch Festlegen des richtigen Speicherorts wird sichergestellt, dass der AzCopy-Befehl ordnungsgemäß aktualisiert wird.

   > [!NOTE]
   > Wenn Sie AzCopy nicht bereits installiert haben, können Sie dies hier tun:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. Kopieren Sie den vordefinierten Befehl, indem Sie auf den Link **in Zwischenablage kopieren** klicken. Starten Sie eine Windows-Eingabeaufforderung, fügen Sie den Befehl ein, und drücken Sie die EINGABETASTE.  Die Dateien werden in den sicheren Azure-BLOB-Speicher für den nächsten Schritt hochgeladen.

   ![Nicht Office 365 Import-Upload-Dateien](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   ![Nicht Office 365 Import – AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > Wenn der angegebene AzCopy-Befehl fehlschlägt, lesen Sie [Troubleshooting AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)

6. Kehren Sie schließlich zur Sicherheit & Compliance zurück, und klicken Sie auf die Schaltfläche **Weiter: Prozessdateien** .  Dadurch wird die Verarbeitung, die Textextraktion und die Indizierung der hochgeladenen Dateien initiiert.  Sie können den Fortschritt der Verarbeitung hier oder auf der Registerkarte **Aufträge** nachverfolgen.  Sobald die neuen Dateien abgeschlossen sind, sind Sie im Überprüfungs verfügbar.  Nachdem die Verarbeitung abgeschlossen ist, können Sie den Assistenten schließen.

   ![Nicht Office 365 Import Prozess-Dateien](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

