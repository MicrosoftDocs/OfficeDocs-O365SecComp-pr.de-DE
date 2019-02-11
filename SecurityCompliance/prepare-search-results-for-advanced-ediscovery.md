---
title: Vorbereiten der Suchergebnisse für Erweiterte eDiscovery in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportWithZoom
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0b6fac2d-8627-4b05-9df0-03609db6248b
description: Hier erfahren Sie, wie Sie die Ergebnisse einer Inhaltssuche in die Office 365-Sicherheit vorbereiten &amp; Compliance Center zur weiteren Analyse mit dem erweiterten eDiscovery-Tool.
ms.openlocfilehash: c70eec691359170ae67e431f20e3b8ad389443f3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "27280168"
---
# <a name="prepare-search-results-for-office-365-advanced-ediscovery"></a>Vorbereiten der Suchergebnisse für Erweiterte eDiscovery in Office 365

Nach einer Suche, die einem eDiscovery-Fall in die Office 365-Sicherheit zugeordnet ist &amp; Compliance Center erfolgreich ausgeführt wird, können Sie die Suchergebnisse zur weiteren Analyse mit Office 365 erweiterte eDiscovery, dem Sie die große analysieren kann, Vorbereiten unstrukturierte Daten festgelegt und reduzieren die Menge der Daten, die mit einer rechtliche Anfrage relevant sind. Erweiterte eDiscovery-Features gehören:
  
- **Optische zeichenerkennung** - Wenn Sie Suchergebnisse automatisch für erweiterte eDiscovery, optischen zeichenerkennung (OCR) Funktionalität vorbereiten extrahiert den Text von Bildern und dazu gehört das mit den Suchergebnissen, die auf in geladen werden Erweiterte eDiscovery für die Analyse. OCR wird unterstützt für lose Dateien, e-Mail-Anlagen und eingebettete Bilder. Dadurch können Sie die Text-Analysefunktionen der erweiterten eDiscovery (in der Nähe Duplikate, e-Mail-threading, Designs und vorhersehbare codieren) auf den Textinhalt in Bilddateien anwenden. Erweiterte eDiscovery OCR unterstützt die folgenden Formate für Bilddateien:

    - GIF
    - JPEG
    - JPG
    - PNG
    - TIFF
    
- **Erkennung nahezu doppelte** - können Sie die Überprüfung Daten effizienter strukturieren, damit eine Person eine Gruppe von ähnlichen Dokumenten überprüft. Dadurch wird verhindert, dass mehrere Bearbeiter müssen verschiedene Versionen desselben Dokuments anzeigen. 
    
- **Threading-e-Mail** - können Sie die eindeutigen Meldungen in einer e-Mail-Thread identifizieren, damit Sie auf nur die neuen Informationen in jede Nachricht konzentrieren können. In einer e-Mail-Thread enthält die zweite Nachricht die erste Nachricht. Höhere Nachrichten enthalten entsprechend alle vorherigen Nachrichten. E-Mail-threading entfernt die Notwendigkeit, alle Nachrichten in seiner Gesamtheit in einer e-Mail-Thread überprüfen. 
    
- **Designs** - hilft Ihnen wertvolle Erkenntnisse zu Ihren Daten jenseits Suche nur schlüsselwortstatistiken zu erhalten. Designs können Untersuchungen durch verwandte Dokumente gruppieren, damit Sie die Dokumente im Kontext anzeigen können. Wenn Sie Designs verwenden möchten, können Sie die zugehörige Designs für eine Gruppe von Dokumenten anzeigen, alle Überlappung bestimmen und identifizieren Sie Querschnitte von verwandten Daten. 
    
- **Prädiktive codieren** - können Sie die Schulen des Systems für, Sie wonach und ermöglicht es Ihnen zu bestimmen, welche (Informationen, ob etwas relevant oder nicht ist) auf einer kleinen Anzahl von Dokumenten. Erweiterte eDiscovery, Learning (basierend auf Ihrer Anleitung) angewendet wird, wenn alle Dokumente in das DataSet analysieren. Basierend auf dieser Learning, bietet erweiterte eDiscovery Relevanz ranking so Sie entscheiden können, welche Dokumente überprüfen basierend auf welche Dokument am ehesten der Groß-/Kleinschreibung relevant sind. 
    
- **Exportieren von Daten für Applikationen überprüfen** - können Sie Daten aus erweiterte eDiscovery und Office 365 exportieren, nachdem Sie die Analyse abgeschlossen und das DataSet reduziert. Exportpaket enthält eine CSV-Datei, die die Eigenschaften aus der exportierten Inhalte und Analytics Metadaten enthält. Diese Exportpaket kann dann zu einer eDiscovery-Überprüfung-Anwendung importiert werden. 
    
## <a name="before-you-begin"></a>Bevor Sie beginnen:

- Um eine erweiterte eDiscovery mit Benutzerdaten zu analysieren, muss der Benutzer (der Verwaltungsberechtigte der Daten) eine Lizenz für Office 365 E5 zugewiesen werden. Alternativ können der Benutzer mit einer Lizenz für Office 365 E1 oder E3 eine erweiterte eDiscovery eigenständige Lizenz zugewiesen werden. Administratoren und Compliance Officer, die zugewiesenen Fällen und erweiterte eDiscovery verwenden, um Daten zu analysieren erforderlich keine E5-Lizenz. 
    
- Sie müssen ein eDiscovery-Manager oder einer eDiscovery-Administrator in der Office 365-Sicherheit &amp; Compliance Center, um die Suchergebnisse für erweiterte eDiscovery vorbereiten. Eine eDiscovery-Manager ist Mitglied der Rollengruppe eDiscovery-Manager. Eine eDiscovery Administrator ist auch Mitglied der Gruppe der eDiscovery-Manager-Rolle, jedoch zusätzliche eDiscovery Berechtigungen zugewiesen wurde. Anweisungen zum Zuweisen von eDiscovery-Administrator-Berechtigungen finden Sie unter Schritt 1 in [eDiscovery-Fälle, in der Office 365-Sicherheit & Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).
    
## <a name="step-1-prepare-search-results-for-advanced-ediscovery"></a>Schritt 1: Vorbereiten der Suchergebnisse für erweiterte eDiscovery

Sie können die Ergebnisse einer Suche vorbereiten, die einem eDiscovery-Fall zugeordnet ist. Wenn Sie die Suchergebnisse für erweiterte eDiscovery vorbereiten, die Daten hochgeladen und vorübergehend in einem eindeutigen Windows Azure-Speicher-Bereich in der Microsoft-Cloud gespeichert. Zu diesem Zeitpunkt ist die OCR Funktionalität von Bildern in den Suchergebnissen Text extrahiert. In [Schritt2](#step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery), der Text und die anderen Suche Ergebnisdaten in zu der erweiterten eDiscovery-Fall geladen.
  
1. Klicken Sie im Security &amp; Compliance Center auf **Suche &amp; Untersuchung** \> **eDiscovery**, um die Liste der Fälle in Ihrem Unternehmen anzuzeigen. 
    
2. Klicken Sie neben die Groß-/Kleinschreibung, die Sie Suchergebnisse für die Analyse in erweiterten eDiscovery vorbereiten möchten **Öffnen** . 
    
3. Klicken Sie auf **der Homepage für den Fall** auf **Suchen**, und wählen Sie dann Suche aus.
    
4. Klicken Sie im Detailbereich unter **Analyze Ergebnisse mit erweiterten eDiscovery**auf **Prepare-Ergebnisse für die Analyse**.
    
    > [!NOTE]
    > Wenn die Suchergebnisse älter als 7 Tage sind, werden Sie aufgefordert, die Suchergebnisse zu aktualisieren. 
  
5. Gehen Sie auf der Seite **Ergebnisse für Analyse vorbereiten** folgendermaßen vor:  
    
    - Verhindern Sie, dass indizierte Elemente, indiziert und nicht-indizierten Elemente oder nur nicht-indizierten Elemente für die Analyse in erweiterten eDiscovery vorzubereiten.
    
    - Wählen Sie, ob alle Versionen von Dokumenten in SharePoint, die die Suchkriterien erfüllen gefunden werden sollen. Diese Option ist nur dann, wenn die Inhaltsquellen für die Suche umfasst Websites.
    
    - Geben Sie an, ob eine Benachrichtigung gesendet (oder kopiert) an eine Person aus, wenn die Vorbereitung abgeschlossen ist und die Daten ist bereit, die im erweiterten eDiscovery verarbeitet werden soll.
    
6. Klicken Sie auf **Vorbereiten**.
    
    Die Suchergebnisse sind für die Analyse mit erweiterten eDiscovery vorbereitet.
    
7. Klicken Sie im Detailbereich auf **Überprüfen Vorbereitung Status** zum Anzeigen von Informationen über den Prozess zur Vorbereitung. Wenn die Vorbereitung abgeschlossen ist, navigieren Sie zu der Groß-/Kleinschreibung im erweiterten eDiscovery zum Verarbeiten der Daten für die Analyse. 
    
## <a name="step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery"></a>Schritt 2: Hinzufügen der Suchdaten Ergebnisse zu der erweiterten eDiscovery-Fall
<a name="step2"> </a>

Wenn die Vorbereitung abgeschlossen ist, besteht der nächste Schritt Erweiterte eDiscovery und Laden Sie die Suche Ergebnisse-Daten (die in einen Bereich Azure-Speicher in der Microsoft-Cloud hochgeladen wurden), zu der erweiterten eDiscovery-Fall. Wie bereits erläutert, um erweiterte eDiscovery zuzugreifen, Sie eine eDiscovery-Administrator in das Wertpapier sein müssen &amp; Compliance Center oder ein Administrator in erweiterten eDiscovery.
  
> [!NOTE]
> Den Zeitaufwand für die Daten aus der Sicherheit &amp; Compliance Center hinzufügen zu einer erweiterten eDiscovery-Fall verfügbar variiert je nach der Größe der Ergebnisse aus der eDiscovery-Suche. 
  
1. Klicken Sie im Security &amp; Compliance Center auf **Suche &amp; Untersuchung** \> **eDiscovery**, um die Liste der Fälle in Ihrem Unternehmen anzuzeigen. 
    
2. Klicken Sie neben die Groß-/Kleinschreibung, die Sie Daten in in erweiterten eDiscovery laden möchten **Öffnen** . 
    
3. Klicken Sie auf der Seite **Start** für den Fall auf **Advanced eDiscovery**. 
    
    ![Klicken Sie auf Wechseln zu erweiterten eDiscovery So öffnen Sie die Groß-/Kleinschreibung in erweiterten eDiscovery](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    **Herstellen einer Verbindung mit erweiterten eDiscovery** Statusanzeige wird angezeigt. Wenn Sie erweiterte eDiscovery verbunden sind, wird eine Liste der Container auf der Setupseite für die Groß-/Kleinschreibung angezeigt. 
    
    ![Die Groß-/Kleinschreibung wird in erweiterten eDiscovery angezeigt.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Diese Container darstellen der Suchergebnisse, die Sie für die Analyse in erweiterten eDiscovery in Schritt 1 vorbereitet haben. Beachten Sie, dass der Name des Containers den gleichen Namen wie die Suche in der Groß-/Kleinschreibung in das Wertpapier hat &amp; Compliance Center. Der Container in der Liste sind diejenigen aus, denen Sie vorbereitet haben. Wenn ein anderer Benutzer die Suchergebnisse für die erweiterte eDiscovery vorbereitet, wird nicht die entsprechenden Container in der Liste enthalten. 
    
4. Um die Suche Ergebnisdaten aus einem Container in der Anfrage in erweiterten eDiscovery zu laden, wählen Sie einen Container, und klicken Sie dann auf **Prozess**.
    
## <a name="next-steps"></a>Nächste Schritte

Nachdem die Ergebnisse einer eDiscovery Search hinzugefügt wurden Fall im nächsten Schritt wird die Verwendung der erweiterten eDiscovery-Tools zum Analysieren der Daten und identifizieren den Inhalt, der mit einer bestimmten rechtliche Anfrage reagiert. Informationen zur Verwendung von erweiterten eDiscovery finden Sie unter [Office 365 erweiterte eDiscovery](office-365-advanced-ediscovery.md).
  
## <a name="more-information"></a>Weitere Informationen

RMS-verschlüsselten e-Mail-Nachrichten, die in den Suchergebnissen enthalten sind werden bei der Vorbereitung für die Analyse in erweiterten eDiscovery entschlüsselt. Diese Funktion Entschlüsselung ist standardmäßig für Mitglieder der Gruppe der eDiscovery-Manager-Rolle aktiviert. Dies ist, da die Verwaltungsrolle RMS Entschlüsseln dieser Rollengruppe zugewiesen ist. Beachten Sie die folgenden Punkte berücksichtigen zu entschlüsseln von e-Mail-Nachrichten:
  
- Diese Funktion Entschlüsselung umfasst derzeit nicht verschlüsselte Inhalte aus SharePoint und OneDrive for Business-Websites. Nur RMS-verschlüsselten e-Mail-Nachrichten werden entschlüsselt werden, wenn Sie sie exportieren.
    
- Wenn eine RMS-verschlüsselten e-Mail-Nachricht eine Anlage (beispielsweise ein Dokument oder eine andere e-Mail-Nachricht), die auch verschlüsselt ist enthält, wird nur die obersten Ebene e-Mail-Nachricht entschlüsselt.
    
- Wenn Sie verhindern, dass eine Person Entschlüsseln von RMS-verschlüsselten Nachrichten, bei der Vorbereitung der Suchergebnisse für die Analyse in erweiterten eDiscovery müssen, müssen Sie zum Erstellen einer benutzerdefinierten Rollengruppe (durch Kopieren der integrierten eDiscovery Rollengruppe Manager), und entfernen Sie den RMS Entschlüsseln Sie Verwaltungsrolle aus die benutzerdefinierte Rollengruppe. Fügen Sie die Person, die Sie nicht als Mitglied der Gruppe benutzerdefinierte Rolle Nachrichten entschlüsseln möchten.
