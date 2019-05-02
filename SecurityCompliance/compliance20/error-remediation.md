---
title: Beheben von Fehlern beim Verarbeiten von Daten
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
ms.openlocfilehash: d54f5ffa5a2dd253a478a758ac0616025a79f118
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2019
ms.locfileid: "33516493"
---
# <a name="error-remediation-when-processing-data"></a>Beheben von Fehlern beim Verarbeiten von Daten

Fehlerkorrektur ermöglicht eDiscovery-Administratoren die Möglichkeit, Daten Probleme zu beheben, die verhindern, dass erweiterte eDiscovery die Inhalte ordnungsgemäß verarbeitet. Dateien, die kennwortgeschützt sind, können beispielsweise nicht verarbeitet werden, da die Dateien gesperrt oder verschlüsselt sind. Mithilfe von Fehlerkorrekturen können eDiscovery-Administratoren Dateien mit solchen Fehlern herunterladen, den Kennwortschutz entfernen und die korrigierten Dateien hochladen.

Verwenden Sie den folgenden Workflow, um Dateien mit Fehlern in erweiterten eDiscovery-Fällen zu beheben.

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a>Erstellen einer Fehlerbehebungssitzung zum Beheben von Dateien mit Verarbeitungsfehlern

>[!NOTE]
>Wenn der Fehlerkorrektur-Assistent während des folgenden Verfahrens jederzeit geschlossen ist, können Sie auf der Registerkarte **Verarbeitung** zur Fehlerbehebungssitzung zurückkehren, indem Sie im Dropdownmenü **Ansicht** die Option **Fehler** Korrekturen auswählen.

1. Wählen Sie auf der Registerkarte **Verarbeitung** in einem erweiterten eDiscovery-Fall im Dropdownmenü **Ansicht** die Option **Fehler** aus.

2. Wählen Sie die Fehler aus, die Sie korrigieren möchten, indem Sie auf das Optionsfeld neben dem Fehlertyp oder-Dateityp klicken.  Im folgenden Beispiel besprechen wir eine kennwortgeschützte Datei.

3. Klicken Sie auf **+ neue Fehlerkorrektur**.

    ![Fehlerkorrektur](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    Die Fehlerbehebungssitzung beginnt mit einer Vorbereitungsphase, in der die fehlerhaften Dateien zu einem sicheren Azure-Speicherort verschoben und heruntergeladen werden.

    ![Vorbereiten der Fehlerkorrektur](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. Klicken Sie nach Abschluss der Vorbereitung auf **Weiter: Dateien herunterladen** , um den Download fortzusetzen.

    ![Dateien herunterladen](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. Zum Herunterladen von Dateien geben Sie den **Zielpfad zum Herunterladen**an. Hierbei handelt es sich um einen Pfad auf dem lokalen Computer, auf dem die Datei heruntergeladen werden soll.  Der Standardpfad,%USERPROFILE%\Downloads\errors, verweist auf den Downloadordner des angemeldeten Benutzers. Dies kann bei Bedarf geändert werden.

    >[!NOTE]
    >Es wird empfohlen, einen lokalen Dateipfad anstelle eines Remotenetzwerk Pfads für eine optimale Leistung zu verwenden.

    > [!NOTE]
    > Wenn Sie AzCopy nicht installiert haben, können Sie es von hier aus installieren:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

6. Kopieren Sie den vordefinierten Befehl **, indem Sie auf in Zwischenablage kopieren**klicken. Starten Sie eine Windows-Eingabeaufforderungen, fügen Sie den Befehl ein, und drücken Sie dann die **Eingabe**Taste.  

    Die Dateien werden heruntergeladen.

    ![Vorbereiten der Fehlerkorrektur](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > Wenn der angegebene AzCopy-Befehl fehlschlägt, finden Sie weitere Informationen unter [Problembehandlung bei AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)

7. Nachdem Sie die Dateien heruntergeladen haben, können Sie Sie mit einem geeigneten Tool beheben. Für kennwortgeschützte Dateien gibt es eine Reihe von Kenn Wort Knack Werkzeugen, die Sie verwenden können. Wenn Sie die Kennwörter für die Dateien kennen, können Sie Sie öffnen und den Kennwortschutz entfernen.
    > [!NOTE]
    > Es ist wichtig, dass Sie die Verzeichnisstruktur und die Dateinamen der bereinigten Dateien im Takt behalten.  Alle in den heruntergeladenen Dateien und Ordnern verwendeten Benennungskonventionen ermöglichen es, die remdiated-Dateien dem Original zuzuordnen.

8. Kehren Sie nun zu Advanced eDiscovery zurück, und klicken Sie auf **Weiter: Dateien hochladen**.  Dadurch gelangen Sie zum nächsten Schritt, in dem Sie jetzt die Dateien hochladen können.

    ![Hochladen von Dateien](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. Spezifizieren Sie den Speicherort der wiederherzustellenden Dateien im Textfeld **Pfad zum Speicherort der Dateien** , und klicken Sie dann auf **in clibpboard kopieren**.

10. Fügen Sie den Befehl in eine Windows-Eingabeaufforderungen ein, und drücken **Sie die Eingabe** Taste, um die Dateien hochzuladen.

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. Kehren Sie schließlich zu Advanced eDiscovery zurück, und klicken Sie auf **Weiter: Process files**.

12. Nach Abschluss der Verarbeitung.  Sie können zum Übersichts Satz zurückkehren und die korrigierte Datei anzeigen.

## <a name="what-happens-when-files-are-remediated"></a>Was geschieht, wenn Dateien korrigiert werden

Bei hochgeladenen Dateien werden die ursprünglichen Metadaten mit Ausnahme der folgenden Felder beibehalten: 

- DocumentExtractedUrl
- ExtractedTextSize
- HasText
- IsErrorRemediate
- IsParentExtractedUrl
- ItemExtractedUrl
- Lade-Nr.
- ProcessingErrorMessage
- ProcessingStatus
- Text
- WordCount
- WorkingsetId

Eine Definition aller Dokument Metadatenfelder in Advanced eDiscovery finden Sie unter [Document Metadata fields](document-metadata-fields.md).