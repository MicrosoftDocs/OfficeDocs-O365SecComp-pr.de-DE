---
title: Exportieren eines Berichts für die Inhaltssuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Anstatt die tatsächlichen Ergebnisse einer Inhaltssuche im Security & Compliance Center in Office 365 zu exportieren, können Sie einfach einen Suchergebnisbericht exportieren. Der Bericht enthält eine Zusammenfassung der Suchergebnisse und ein Dokument mit detaillierten Informationen zu jedem Element, das exportiert würde.
ms.openlocfilehash: 57c8a9be5c53998570f6ff15a49df69e27745e26
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958726"
---
# <a name="export-a-content-search-report"></a>Exportieren eines Berichts für die Inhaltssuche

Anstatt den vollständigen Satz von Suchergebnissen aus einer Inhaltssuche im Security & Compliance Center (und aus einer Inhaltssuche, die mit einem eDiscovery-Fall verknüpft ist) zu exportieren, können Sie die gleichen Berichte exportieren, die beim Exportieren der Suche generiert werden. Ergebnisse.
  
Wenn Sie einen Bericht exportieren, wird er in einen Ordner heruntergeladen, der den gleichen Namen wie die Inhaltssuche hat, aber mit *_ReportsOnly* angefügt wird. Wenn die Inhaltssuche beispielsweise " *ContosoCase0815* " heißt, wird der Bericht in einen Ordner mit dem Namen *ContosoCase0815_ReportsOnly* heruntergeladen. Eine Liste der Dokumente, die im Bericht enthalten sind, finden Sie unter [What es included in the Report](#whats-included-in-the-report).

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um einen Bericht über Inhaltssuche zu exportieren, muss Ihnen die Rolle Compliance Search Management im Security & Compliance Center zugewiesen werden. Diese Rolle wird den integrierten eDiscovery-Manager-und Organisations Verwaltungsrollengruppen zugewiesen. Sie wird der Rollengruppe Organisationsverwaltung nicht standardmäßig zugewiesen. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen](assign-ediscovery-permissions.md).
    
- Beim Exportieren eines Berichts werden die Daten vorübergehend in einem eindeutigen Windows Azure-Speicherbereich in der Microsoft-Cloud gespeichert, bevor Sie auf Ihren lokalen Computer heruntergeladen werden. stellen sie sicher, dass ihre organisation eine verbindung mit dem endpunkt in Azure herstellen kann, nämlich ** \*. blob.core.windows.net** (der platzhalter stellt einen eindeutigen bezeichner für den export dar). Die Suchergebnis Daten werden zwei Wochen nach der Erstellung aus dem Azure-Speicherbereich gelöscht. 
    
- Der Computer, den Sie zum Exportieren der Suchergebnisse verwenden, muss die folgenden Voraussetzungen erfüllen:
    
  - 32- oder 64-Bit-Versionen von Windows 7 und höher
    
  - Microsoft .NET Framework 4,7
    
  - Einen unterstützten Browser:
    
    - Microsoft Edge
    
      oder
    
    - Microsoft Internet Explorer 10 und höhere Versionen
    
    **Hinweis:** Microsoft stellt keine Drittanbietererweiterungen oder Add-ons für ClickOnce-Anwendungen her. Das Exportieren von Suchergebnissen mithilfe eines nicht unterstützten Browsers mit Drittanbietererweiterungen oder Add-ons wird nicht unterstützt. 

- Wenn die geschätzte Gesamtgröße der von einer Inhaltssuche zurückgegebenen Ergebnisse 20&nbsp;TB überschreitet, tritt beim Exportieren des Berichts ein Fehler auf. Um den Bericht erfolgreich zu exportieren, versuchen Sie, den Bereich einzugrenzen und die Suche erneut auszuführen, damit die geschätzte Größe der Ergebnisse weniger&nbsp;als 20 TB beträgt.

- Das Exportieren von Inhalts Suchberichten gilt für die maximale Anzahl von Exporten, die gleichzeitig ausgeführt werden, und die maximale Anzahl von Exporten, die ein einzelner Benutzer ausführen kann. Weitere Informationen zu Export Grenzwerten finden Sie unter [Exportieren von Inhalts Suchergebnissen](export-search-results.md#export-limits).

## <a name="generate-and-download-a-content-search-report"></a>Generieren und Herunterladen eines Inhalts Suchberichts

Die Schritte zum Generieren und Herunterladen eines Inhalts Suchberichts ähneln dem tatsächlichen Exportieren der Suchergebnisse.
  
## <a name="step-1-generate-the-report-for-export"></a>Schritt 1: Generieren des Berichts für den Export

Der erste Schritt besteht darin, den Bericht für das Herunterladen auf Ihren Computer vorzubereiten, der exportiert wird. Beim Bericht werden die Berichtsdokumente in einen Azure-Speicherbereich in der Microsoft-Cloud hochgeladen.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security & Compliance Centers auf **Suche** \> **Inhaltssuche**.
    
4. Wählen Sie auf der Seite **Inhaltssuche** eine Suche aus. 
    
5. Klicken Sie im Detailbereich unter **Bericht auf einem Computer exportieren**auf **Bericht generieren**.
    
    > [!NOTE]
    > Wenn die Suchergebnisse älter als 7 Tage sind, werden Sie aufgefordert, die Suchergebnisse zu aktualisieren. Wenn dies der Fall ist, brechen Sie den Export ab, klicken Sie im Detailbereich für die ausgewählte Suche auf **Suchergebnisse aktualisieren** , und starten Sie dann den Berichtsexport erneut, nachdem die Ergebnisse aktualisiert wurden. 
  
6. Wählen Sie auf der Seite **Bericht exportieren** unter **diese Elemente aus der Suche einbeziehen**eine der folgenden Optionen aus:
    
    - Nur indizierte Elemente exportieren
    
    - Indizierte und nicht indizierte Elemente exportieren
    
    - Nur nicht indizierte Elemente exportieren
    
    Weitere Informationen zu nicht indizierten Elementen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche](partially-indexed-items-in-content-search.md).
    
7. Wählen Sie aus, dass Suchstatistiken für alle Versionen von SharePoint-Dokumenten eingeschlossen werden sollen. Diese Option wird nur angezeigt, wenn die Inhaltsquellen der Suche SharePoint oder OneDrive for Business-Websites enthalten.
    
8. Klicken Sie auf **Bericht generieren**.
    
    Der Suchergebnisbericht wird zum Herunterladen vorbereitet, was bedeutet, dass die Berichtsdokumente in den Azure-Speicherbereich in der Microsoft-Cloud hochgeladen werden. Wenn der Bericht zum Herunterladen bereit ist, wird der Link zum **herunterladen** des Berichts unter **Bericht auf einem Computer exportieren** im Detailbereich angezeigt. 
    
> [!NOTE]
> Sie können einen Bericht auch für eine Inhaltssuche exportieren, die mit einem eDiscovery-Fall verknüpft ist. Wechseln Sie dazu zu **eDiscovery** \> **eDiscovery**, wählen Sie einen Fall aus, und klicken Sie auf Bearbeitungs](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)Symbol **Bearbeiten** ![. Wählen Sie auf der Seite Such **Vorgänge** eine Suche aus, und **** ![klicken Sie dann auf Export](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> Suchergebnis Symbol exportieren, um **einen Bericht zu exportieren**. 
  
## <a name="step-2-download-the-report"></a>Schritt 2: Herunterladen des Berichts

Im nächsten Schritt wird der Bericht aus dem Azure-Speicherbereich auf Ihren lokalen Computer heruntergeladen.
  
1. Klicken Sie im Detailbereich für die Suche, für die Sie den Bericht erstellt haben, unter **Bericht auf Computer exportieren**auf **Bericht herunterladen**.
    
    Die Seite zum **herunterladen des Berichts** wird angezeigt und enthält die folgenden Informationen zum Bericht, bis Sie auf Ihren Computer heruntergeladen werden können. 
    
    - Die Anzahl der Elemente, die heruntergeladen werden.
    
    - Die geschätzte Gesamtgröße der Elemente, die heruntergeladen werden.
    
    - Ob indiziert oder nicht indiziert wird exportiert. Nicht indizierte Elemente sind Elemente, die ein erkanntes Format aufweisen, verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden.
    
    - Gibt an, ob Versionen von SharePoint-Dokumenten heruntergeladen werden.
    
    - Der Status des Berichtsexport Vorgangs. Sie können den Download des Berichts auch dann starten, wenn die Vorbereitung des Berichts nicht abgeschlossen ist.
    
2. Klicken Sie unter **Schlüssel exportieren** auf **In Zwischenablage kopieren**. Sie verwenden diesen Schlüssel in Schritt 5, um den Bericht herunterzuladen.
    
    > [!IMPORTANT]
    > Da jeder das eDiscovery-Export Tool installieren und starten und dann diesen Schlüssel zum Herunterladen des Suchberichts verwenden kann, müssen Sie Vorkehrungen treffen, um diesen Schlüssel genau so zu schützen, als würden Sie Kennwörter oder andere sicherheitsrelevante Informationen schützen. 
  
3. Klicken Sie auf **Bericht herunterladen**.
    
4. Wenn Sie aufgefordert werden, das **microsoft office 365 eDiscovery-Export Tool**zu installieren, klicken Sie auf **Installieren**.
    
5. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 2 kopiert haben, in das entsprechende Feld ein.
    
6. Klicken Sie auf **Durchsuchen** , um den Speicherort für den Bericht anzugeben. 
    
7. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Das **eDiscovery-Export Tool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und der Größe) der verbleibenden zu ladenden Elemente. Nach Abschluss des Exportvorgangs können Sie auf die Dateien am Speicherort zugreifen, an dem Sie heruntergeladen wurden. 
    
> [!NOTE]
> Sie können den Bericht für eine Inhaltssuche herunterladen, die einem eDiscovery-Fall zugeordnet ist. Wechseln Sie dazu zu **eDiscovery** \> **eDiscovery**, wählen Sie einen Fall aus, und klicken Sie auf Bearbeitungs](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)Symbol **Bearbeiten** ![. Wählen Sie **** auf der Seite Exports einen Berichtsexport aus, und klicken Sie dann im Detailbereich auf **Bericht herunterladen** . 
  
## <a name="whats-included-in-the-report"></a>Inhalt des Berichts

Wenn Sie einen Bericht zu den Ergebnissen einer Inhaltssuche generieren und exportieren, werden die folgenden Dokumente heruntergeladen:
  
- **Export Zusammenfassung** – ein Excel-Dokument, das eine Zusammenfassung des Exports enthält. Hierzu gehören Informationen wie die Anzahl der durchsuchten Inhaltsquellen, die Anzahl der Suchergebnisse von jedem Inhaltsspeicherort, die geschätzte Anzahl von Elementen, die tatsächliche Anzahl von Elementen, die exportiert werden sollen, sowie die geschätzte und tatsächliche Größe von Elementen. , die exportiert werden würden. 
    
    > [!NOTE]
    > Wenn Sie beim Exportieren des Berichts nicht indizierte Elemente einschließen, ist die Anzahl der nicht indizierten Elemente in der Gesamtzahl der geschätzten Suchergebnisse und in der Gesamtzahl der heruntergeladenen Suchergebnisse enthalten (wenn Sie die Suchergebnisse exportieren), die im Zusammenfassungsbericht exportieren. Anders ausgedrückt: die Gesamtzahl der heruntergeladenen Elemente entspricht der Gesamtzahl der geschätzten Ergebnisse und der Gesamtanzahl der nicht indizierten Elemente. 
  
- **Manifest** – eine Manifestdatei (im XML-Format), die Informationen zu jedem in den Suchergebnissen enthaltenen Element enthält. 
    
- **Results** – ein Excel-Dokument, das eine Zeile mit Informationen zu jedem indizierten Element enthält, das mit den Suchergebnissen exportiert würde. Für e-Mails enthält das Ergebnisprotokoll Informationen zu den einzelnen Nachrichten, einschließlich: 
    
  - Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).
    
  - Das Datum, an dem die Nachricht gesendet oder empfangen wurde.
    
  - Die Betreffzeile der Nachricht.
    
  - Absender und Empfänger der Nachricht.
    
    Für Dokumente aus SharePoint und OneDrive for Business-Websites enthält das Ergebnisprotokoll Informationen zu jedem Dokument, einschließlich:
    
  - Die URL für das Dokument.
    
  - Die URL für die Websitesammlung, in der sich das Dokument befindet.
    
  - Das Datum, an dem das Dokument zuletzt geändert wurde.
    
  - Der Name des Dokuments (das sich in der Spalte Betreff im Ergebnisprotokoll befindet).
    
    > [!NOTE]
    > Die Anzahl der Zeilen im **Ergebnis** Bericht sollte der Gesamtzahl der gedownloadeten Suchergebnisse minus der Gesamtanzahl der im Bericht "nicht **indizierte Elemente** " aufgeführten Elemente entsprechen. 
  
- Nicht **indizierte Elemente** – ein Excel-Dokument mit Informationen zu nicht indizierten Elementen, die in die Suchergebnisse eingeschlossen werden würden. Wenn Sie beim Generieren des Suchergebnis Berichts keine nicht indizierten Elemente hinzufügen, wird dieser Bericht weiterhin heruntergeladen, ist aber leer.
