---
title: Error Remediation beim Verarbeiten von Daten
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
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607832"
---
# <a name="error-remediation-when-processing-data"></a>Error Remediation beim Verarbeiten von Daten

Error Remediation kann eDiscovery-Administratoren die Möglichkeit zum Beheben von Problemen mit der die verhindern, dass die erweiterte eDiscovery (Preview) ordnungsgemäß verarbeiten des Inhalts. Dateien, die ein Kennwort geschützt sind können beispielsweise verarbeitet werden, da die Dateien gesperrt oder verschlüsselt werden. Error Remediation verwenden, können eDiscovery-Administratoren Downloaddateien mit derartige Fehler, Entfernen des Kennwortschutzes und die für gewartete Dateien hochladen.

Verwenden Sie den folgenden Workflow zum Warten von Dateien mit Fehlern in Fällen erweiterte eDiscovery (Preview).

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a>Erstellen eine Error Remediation Sitzung zum Warten von Dateien mit der Verarbeitung von Fehlern

>[!NOTE]
>Wenn der der Fehler Remediation-Assistent geschlossen ist, können Sie jederzeit während des folgenden Verfahrens, können Sie zurückgeben der Error Remediation-Sitzung auf der Registerkarte **Verarbeitung** **Fehler Bereinigungsstatus** in das Dropdownmenü **Ansicht** auswählen.

1. Wählen Sie auf der Registerkarte **Verarbeitung** in einem erweiterten eDiscovery (Preview)-Fall **Fehler** in das Dropdownmenü **Ansicht** aus.

2. Wählen Sie die Fehler, den, die Sie durch Klicken auf das Optionsfeld neben den Fehlertyp oder der Dateityp warten möchten.  Im folgenden Beispiel haben wir eine kennwortgeschützte Datei Korrigieren von.

3. Klicken Sie auf **+ Neues Error Remediation**.

    ![Error remediation](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    Die Fehler Remediation-Sitzung wird gestartet, beginnend mit einer Vorbereitung Phase, in der das Dateifehler an einem sicheren Speicherort Azure verschoben heruntergeladen werden.

    ![Vorbereiten der Error remediation](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. Nachdem die Vorbereitung abgeschlossen ist, klicken Sie auf **Weiter: Downloaddateien** Download fortsetzen.

    ![Herunterladen von Dateien](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. Informationen zum Herunterladen von Dateien anzugeben Sie den **Zielpfad für den Download**. Hierbei handelt es sich um einen Pfad auf dem lokalen Computer, auf dem die Datei heruntergeladen werden soll.  Der Standardpfad % USERPROFILE%\Downloads\errors, verweist auf des angemeldeten Benutzers Downloads Ordner; Dies kann bei Bedarf geändert werden.

    >[!NOTE]
    >Es wird empfohlen, dass Sie einen lokalen Pfad anstelle einer remote Netzwerkpfad für eine optimale Leistung verwenden.

    > [!NOTE]
    > Wenn Sie AzCopy nicht installiert haben, können Sie es dort installieren:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

6. Kopieren Sie den vordefinierten Befehl durch Klicken auf **in die Zwischenablage kopieren**. Starten einer Windows-Eingabeaufforderung, fügen Sie den Befehl ein, und drücken Sie die **EINGABETASTE**.  

    Die Dateien werden heruntergeladen.

    ![Vorbereiten der Error remediation](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > Wenn Sie Probleme mit diesem Befehl ausgeführt haben, finden Sie unter https://go.microsoft.com/fwlink/?linkid=2038117 Tipps zur Problembehandlung.

7. Nach dem Herunterladen der Dateien, können Sie diese mit einem geeigneten Tool warten. Für kennwortgeschützte Dateien schützen stehen Ihnen eine Reihe von Kennwörtern Tools, die Sie verwenden können. Wenn Sie die Kennwörter für die Dateien kennen, können Sie öffnen und den Kennwortschutz entfernen.
    > [!NOTE]
    > IT ist wichtig, dass Sie die Directory-Struktur und den Dateinamen der Dateien für gewartete intakt beibehalten.  Alle Namenskonventionen verwendet wird, in den heruntergeladenen Dateien und Ordner ermöglichen, ordnen Sie die Dateien Remdiated wieder in den ursprünglichen.

8. Nun, erweiterte eDiscovery (Preview) zurück, und klicken Sie auf **Weiter: Hochladen von Dateien**.  Dies wird mit dem nächsten Schritt verschieben, können Sie jetzt die Dateien hochladen.

    ![Hochladen von Dateien](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. Geben Sie den Speicherort der Dateien in das Textfeld **Pfad zum Speicherort der Dateien** für gewartete klicken Sie dann auf **in Clibpboard kopieren**.

10. Fügen Sie den Befehl in einer Windows-Eingabeaufforderung, und drücken Sie die **EINGABETASTE** , um die Dateien hochladen.

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. Schließlich erweiterte eDiscovery (Preview) zurück, und klicken Sie auf **Weiter: Dateien verarbeiten**.

12. Wenn die Verarbeitung abgeschlossen ist.  Sie können die Arbeitsseiten zurück, und finden Sie in der Datei für gewartete.

## <a name="what-happens-when-files-are-remediated"></a>Was geschieht, wenn Dateien behoben wurden

Wenn für gewartete Dateien hochgeladen werden, wird die ursprüngliche Metadaten mit Ausnahme der folgenden Felder beibehalten: 

- DocumentExtractedUrl
- ExtractedTextSize
- HasText
- IsErrorRemediate
- IsParentExtractedUrl
- ItemExtractedUrl
- LoadId
- ProcessingErrorMessage
- Verarbeitungsstatusname
- Text
- WordCount
- WorkingsetId

Eine Definition aller Dokument Metadaten-Felder in erweiterten eDiscovery (Preview) finden Sie unter [Metadatenfelder Dokument](document-metadata-fields.md).