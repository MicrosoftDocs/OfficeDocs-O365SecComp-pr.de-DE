---
title: Exportieren eines Inhaltssuchberichts
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Anstelle von Export von tatsächlichen Ergebnissen einer Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center, können Sie nur einen Bericht der Suchergebnisse exportieren. Der Bericht enthält eine Zusammenfassung der Ergebnisse der und ein Dokument mit ausführlichen Informationen über jedes Element, das exportiert werden würde.
ms.openlocfilehash: db6ba2dd58befa782dc3a5968e0034bccfa46855
ms.sourcegitcommit: ea625737c4be14927f69aa71d4fbd7d7d94d9334
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2019
ms.locfileid: "27544126"
---
# <a name="export-a-content-search-report"></a>Exportieren eines Inhaltssuchberichts

Anstelle von exportieren die vollständige Unterstützung der Suche von Suchergebnissen aus einer Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center (und aus einer Inhaltssuche, die einem eDiscovery-Fall zugeordnet ist), können Sie dieselben Berichte, die nur exportieren generiert werden, wenn Sie Exportieren von Suchergebnissen.
  
Beim Exportieren eines Berichts wird es in einen Ordner heruntergeladen, die den gleichen Namen wie die Inhaltssuche hat, aber, die mit *_ReportsOnly* angehängt ist. Beispielsweise wird die Inhaltssuche *ContosoCase0815* genannt, wird Sie dann der Bericht in einen Ordner namens *ContosoCase0815_ReportsOnly* heruntergeladen. Eine Liste von Dokumenten, die im Bericht enthalten sind, finden Sie unter [Was ist im Bericht enthalten](#whats-included-in-the-report).

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um einen Bericht Inhaltssuche zu exportieren, müssen Sie die Verwaltungsrolle Compliance-Suche in der Office 365-Sicherheit zugewiesen werden &amp; Compliance Center. Integrierte eDiscovery-Manager und Organization Management Rollengruppen wird diese Rolle zugewiesen. Es ist nicht in der Standardeinstellung der Rollengruppe "Organisationsverwaltung" zugewiesen. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
    
- Wenn Sie einen Bericht exportieren, werden die Daten vorübergehend in einem eindeutigen Windows Azure-Speicher-Bereich in der Microsoft-Cloud gespeichert, bevor sie sich an Ihren lokalen Computer heruntergeladen wird. Achten Sie darauf Ihrer Organisation kann an den Endpunkt in Azure, ist eine Verbindung herstellen ** \*. blob.core.windows.net** (der Platzhalter stellt einen eindeutigen Bezeichner für Ihren Export). Suche Ergebnisse werden die Daten aus dem Bereich der Azure-Speicher gelöscht zwei Wochen, nachdem er erstellt wurde. 
    
- Der Computer, den Sie zum Exportieren der Suchergebnisse verwenden, muss die folgenden Voraussetzungen erfüllen:


    
  - 32- oder 64-Bit-Versionen von Windows 7 und höher
    
  - Microsoft .NET Framework 4.7
    
  - Einen unterstützten Browser:
    
    - Microsoft Edge
    
      oder
    
    - Microsoft Internet Explorer 10 und höhere Versionen
    
    **Hinweis:** Microsoft herstellen nicht Drittanbieter-Erweiterungen oder Add-ons für ClickOnce-Anwendungen. Exportieren von Suchergebnissen mithilfe von einem nicht unterstützten Browser mit Drittanbieter-Erweiterungen oder Add-ons wird nicht unterstützt. 

- Wenn die geschätzte Gesamtgröße der von einem Inhaltssuche zurückgegebenen Ergebnisse 20 übersteigt&nbsp;TB, Exportieren des Berichts schlägt fehl. Versuchen Sie zum erfolgreichen Exportieren des Berichts, den Bereich einzuschränken, und führen Sie die Suche erneut aus, damit die geschätzte Größe der Ergebnisse kleiner als 20 ist&nbsp;TB.

- Exportieren von Inhaltssuche Berichten zählt gegen die maximale Anzahl von Exporten ausgeführt zum gleichen Zeitpunkt und die maximale Anzahl von Exporten, die ein einzelner Benutzer ausgeführt werden kann. Weitere Informationen zu den Export Grenzwerten finden Sie unter [Exportieren von Inhalt von Suchergebnissen aus der Office 365-Sicherheit und Compliance Center](export-search-results.md#export-limits).

## <a name="generate-and-download-a-content-search-report"></a>Generieren und Herunterladen eines Berichts für die Inhaltssuche

Die Schritte zum Generieren und zum Herunterladen eines Berichts Inhaltssuche sind sehr ähnlich tatsächlich Suchergebnisse exportieren.
  
## <a name="step-1-generate-the-report-for-export"></a>Schritt 1: Generieren Sie den Bericht für den export

Der erste Schritt besteht darin, den Bericht vorzubereiten, für den Download auf Ihrem Computer exportieren. Cloud-Wenn Sie den Bericht, den Bericht, Dokumente in einen Bereich Azure-Speicher in der Microsoft hochgeladen werden.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
4. Wählen Sie auf der Seite **Inhaltssuche** eine Suche ein. 
    
5. Klicken Sie im Detailbereich unter **Bericht auf einen Computer exportieren**auf **Bericht generieren**.
    
    > [!NOTE]
    > Wenn die Ergebnisse für eine Suche älter als 7 Tage sind, werden Sie aufgefordert, um die Suchergebnisse zu aktualisieren. In diesem Fall Abbrechen Sie den Export, klicken Sie im Detailbereich für die ausgewählte Suche auf **Update-Suchergebnisse** und starten Sie den Berichtsexport erneut, nachdem die Ergebnisse aktualisiert werden. 
  
6. Wählen Sie auf der Seite **Exportieren eines Berichts** unter **diese Einträge aus der Suche einschließen**eine der folgenden Optionen aus:
    
    - Nur indizierte Elemente exportieren
    
    - Indizierte und nicht indizierte Elemente exportieren
    
    - Nur nicht indizierte Elemente exportieren
    
    Weitere Informationen zu nicht indizierten Elementen finden Sie unter [teilweise indizierte Elemente in Inhaltssuche](partially-indexed-items-in-content-search.md).
    
7. Verhindern Sie, dass die Suchstatistik für alle Versionen von SharePoint-Dokumenten enthält. Diese Option ist nur dann, wenn die Inhaltsquellen der Suche umfasst SharePoint oder OneDrive for Business-Websites.
    
8. Klicken Sie auf **Bericht generieren**.
    
    Der Bericht der Suchergebnisse vorbereitet wird für das Herunterladen, was bedeutet, dass die Berichtsdokumente in den Bereich der Azure-Speicher in der Cloud Microsoft hochgeladen werden soll. Wenn der Bericht zum Download bereit ist, wird der **Bericht herunterladen** Link im Detailbereich unter **Bericht auf einen Computer exportieren** angezeigt. 
    
> [!NOTE]
> Sie können auch einen Bericht für ein Inhaltssuche exportieren, die einem eDiscovery-Fall zugeordnet ist. Wechseln Sie zu diesem Zweck zu **Suche &amp; Untersuchung** \> **eDiscovery**, wählen Sie eine Anfrage aus, und klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Klicken Sie auf der Seite **sucht** , wählen Sie eine Suche aus, und klicken Sie dann auf **Exportieren** ![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Exportieren eines Berichts**. 
  
## <a name="step-2-download-the-report"></a>Schritt 2: Herunterladen des Berichts

Im nächste Schritt wird um den Bericht aus dem Bereich der Azure-Speicher auf dem lokalen Computer herunterzuladen.
  
1. Klicken Sie im Detailbereich für die Suche, dass Sie den Bericht für, unter **Exportieren Bericht auf einen Computer**generiert auf **Bericht herunterladen**.
    
    Die Downloadseite **Bericht** wird angezeigt und enthält die folgenden Informationen zu den Bericht bis zum an Ihrem Computer heruntergeladen werden. 
    
    - Die Anzahl der Elemente, die heruntergeladen werden.
    
    - Die geschätzte Gesamtgröße der Elemente, die heruntergeladen werden.
    
    - Ob indiziert oder nicht-indizierten exportiert werden. Nicht indizierte Elemente sind Elemente, die ein bekanntes Format haben, werden verschlüsselt oder aus anderen Gründen indiziert wurden nicht.
    
    - Unabhängig davon, ob Versionen von SharePoint-Dokumente heruntergeladen werden.
    
    - Der Status des Exportvorgangs Bericht. Sie können beginnen, den Bericht herunterladen, auch wenn die Vorbereitung des Berichts nicht abgeschlossen ist.
    
2. Klicken Sie unter **Schlüssel exportieren**auf **in die Zwischenablage kopieren**. Sie verwenden dieser Schlüssel in Schritt 5, um den Bericht herunterzuladen.
    
    > [!IMPORTANT]
    > Da jeder kann installieren und das eDiscovery-Export-Tool starten und dann dieser Schlüssel verwenden, um den Bericht Suche herunterzuladen, müssen Sie unbedingt müssen Sie Vorsichtsmaßnahmen gegen dieser Schlüssel schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen zu schützen. 
  
3. Klicken Sie auf **Bericht herunterladen**.
    
4. Wenn Sie aufgefordert werden, installieren Sie **MicrosoftOffice 365 eDiscovery-Exporttool**, klicken Sie auf **Installieren**.
    
5. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 2 kopiert haben, in das entsprechende Feld ein.
    
6. Klicken Sie auf **Durchsuchen** , um den Speicherort angeben, in dem Sie den Bericht herunterladen möchten. 
    
7. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Die **eDiscovery-Exporttool** zeigt Statusinformationen über den Exportvorgang, einschließlich eine Schätzung der Anzahl (und Größe) der verbleibenden Elemente heruntergeladen werden. Wenn der Exportvorgang abgeschlossen ist, können Sie die Dateien in den Speicherort zugreifen, in dem sie heruntergeladen wurden. 
    
> [!NOTE]
> Sie können den Bericht für ein Inhaltssuche herunterladen, die einem eDiscovery-Fall zugeordnet ist. Wechseln Sie zu diesem Zweck zu **Suche &amp; Untersuchung** \> **eDiscovery**, wählen Sie eine Anfrage aus, und klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Klicken Sie auf der Seite **exportiert** wählen Sie einen Bericht exportieren, und klicken Sie dann im Detailbereich auf **Bericht herunterladen** . 
  
## <a name="whats-included-in-the-report"></a>Was ist in den Bericht einbezogen.

Wenn Sie generieren und eines Berichts zu den Ergebnissen einer Inhaltssuche exportieren, sind die folgenden Dokumente heruntergeladen werden:
  
- **Zusammenfassung exportieren** - eine Excel-Dokument, das eine Zusammenfassung des Exports enthält. Hierzu zählen Informationen wie die Anzahl der Inhaltsquellen, die durchsucht wurden, die Anzahl der Suchergebnisse aus jeder Inhaltsspeicherort, die geschätzte Anzahl der Elemente, die tatsächliche Anzahl von Elementen, die exportiert werden würde und der geschätzten und der tatsächlichen Größe der Elemente würde exportiert werden. 
    
    > [!NOTE]
    > Wenn Sie beim Exportieren des Berichts nicht indizierter Elemente einschließen, werden die Anzahl der nicht-indizierten Elemente in die Gesamtzahl der geschätzten Suchergebnisse und die Gesamtzahl der heruntergeladenen Suchergebnisse (Wenn Sie waren so exportieren Sie die Suchergebnisse), die in aufgeführt sind die Exportieren Sie Zusammenfassungsbericht. Anders ausgedrückt, entspricht die Gesamtanzahl der Elemente, die heruntergeladen werden würde die Gesamtzahl der erwarteten Ergebnisse und die Gesamtzahl der nicht-indizierten Elementen. 
  
- **Manifest** - eine Manifestdatei (im XML-Format), das Informationen über jedes Element in den Suchergebnissen enthalten enthält. 
    
- **Ergebnisse** - eine Excel-Dokument, das eine Zeile mit Informationen zu den einzelnen indizierten Elementen enthält, die mit den Suchergebnissen exportiert werden würde. Für e-Mails die, das Ergebnis-Protokoll enthält Informationen zu jeder Nachricht, einschließlich: 
    
  - Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).
    
  - Das Datum, an dem die Nachricht gesendet oder empfangen wurde.
    
  - Die Betreffzeile der Nachricht.
    
  - Absender und Empfänger der Nachricht.
    
    Für Dokumente aus SharePoint und OneDrive for Business-Websites, das Ergebnisse-Protokoll enthält Informationen über jedes Dokument einschließlich:
    
  - Die URL für das Dokument.
    
  - Die URL für die Websitesammlung, in dem das Dokument gespeichert ist.
    
  - Das Datum, das das Dokument zuletzt geändert wurde.
    
  - Der Name des Dokuments (der in der Spalte Betreff im Protokoll Ergebnis befindet).
    
    > [!NOTE]
    > Die Anzahl der Zeilen in **der Ergebnisbericht** sollte die Gesamtzahl der Suchergebnisse entsprechen, die minus der Gesamtanzahl der Elemente aufgeführt, die im Bericht **Nicht indizierten Elementen** gedownloadet werden sollen. 
  
- **Nicht-indizierten Elementen** - eine Excel-Dokument, das Informationen über alle nicht-indizierten Elemente enthält, die in den Suchergebnissen enthalten sein wird. Wenn Sie beim Erstellen des Berichts der Suchergebnisse nicht indizierter Elemente einschließen, in diesem Bericht wird weiterhin heruntergeladen werden, aber leer.
