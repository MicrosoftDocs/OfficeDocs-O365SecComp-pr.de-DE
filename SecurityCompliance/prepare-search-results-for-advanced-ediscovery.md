---
title: Vorbereiten der Suchergebnisse für Erweiterte eDiscovery in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportWithZoom
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0b6fac2d-8627-4b05-9df0-03609db6248b
description: In diesem Artikel erfahren Sie, wie Sie die Ergebnisse einer Inhaltssuche im Office &amp; 365 Security Compliance Center zur weiteren Analyse mit dem erweiterten eDiscovery-Tool vorbereiten.
ms.openlocfilehash: 04de96064f400f8055d0e477bf41ed1c7cb1b35f
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223844"
---
# <a name="prepare-search-results-for-office-365-advanced-ediscovery"></a>Vorbereiten der Suchergebnisse für Erweiterte eDiscovery in Office 365

Nachdem eine Suche, die einem eDiscovery-Fall im Office 365 Security &amp; Compliance Center zugeordnet ist, erfolgreich ausgeführt wurde, können Sie die Suchergebnisse für eine weitere Analyse mit Office 365 Advanced eDiscovery vorbereiten, mit der Sie umfangreiche, unstrukturierte Datensätze und geringere Datenmenge, die für einen Rechtsstreit relevant ist. Zu den erweiterten eDiscovery-Features gehören:
  
- **Optische Zeichenerkennung** : Wenn Sie Suchergebnisse für erweiterte eDiscovery vorbereiten, extrahiert die OCR-Funktionalität (Optical Character Recognition) automatisch Text aus Bildern und enthält die Suchergebnisse, die in Erweiterte eDiscovery für Analyse. OCR wird für lose Dateien, e-Mail-Anlagen und eingebettete Bilder unterstützt. Auf diese Weise können Sie die Textanalyse Funktionen von Advanced eDiscovery (Near-Duplikate, e-Mail-Threading, Designs und Vorhersage Codierung) auf den Textinhalt in Bilddateien anwenden. Advanced eDiscovery OCR unterstützt die folgenden Formate für Bilddateien:

    - GIF
    - JPEG
    - JPG
    - PNG
    - TIFF
    
- **Near-Duplicate Detection** – ermöglicht Ihnen eine effizientere Strukturierung der Datenüberprüfung, sodass eine Gruppe ähnlicher Dokumente von einer Person überprüft wird. Dadurch wird verhindert, dass mehrere Prüfer unterschiedliche Versionen desselben Dokuments anzeigen müssen. 
    
- **E-Mail** -Threading – hilft Ihnen bei der Identifizierung der eindeutigen Nachrichten in einem e-Mail-Thread, sodass Sie sich nur auf die neuen Informationen in jeder Nachricht konzentrieren können. In einem e-Mail-Thread enthält die zweite Nachricht die erste Nachricht. Entsprechend enthalten spätere Nachrichten alle vorherigen Nachrichten. E-Mail-Threading entfernt die Notwendigkeit, alle Nachrichten vollständig in einem e-Mail-Thread zu überarbeiten. 
    
- **Designs** – Sie erhalten wertvolle Einblicke über Ihre Daten über die Statistiken zur Stichwortsuche hinaus. Designs helfen bei der Untersuchung, indem Sie verwandte Dokumente gruppieren, sodass Sie die Dokumente im Kontext betrachten können. Bei der Verwendung von Designs können Sie die zugehörigen Designs für eine Gruppe von Dokumenten anzeigen, Überlappungen festlegen und dann die Querschnitte der zugehörigen Daten identifizieren. 
    
- **Predictive Coding** -ermöglicht es Ihnen, das System für das zu trainieren, wonach Sie suchen, indem Sie Entscheidungen treffen (darüber, ob etwas relevant ist oder nicht) in einer kleinen Gruppe von Dokumenten. Advanced eDiscovery wendet dann dieses Lernen (basierend auf Ihren Anweisungen) an, wenn alle Dokumente im Dataset analysiert werden. Basierend auf diesem Lernprozess bietet Advanced eDiscovery eine Relevanz-Rangfolge, sodass Sie entscheiden können, welche Dokumente auf der Grundlage des Dokuments, das am ehesten für den Fall relevant ist, überprüft werden sollen. 
    
- **Exportieren von Daten für Überprüfungs Anwendungen** – Sie können Daten aus Advanced EDiscovery und Office 365 exportieren, nachdem Sie Ihre Analyse abgeschlossen haben und das DataSet reduziert haben. Das Exportpaket enthält eine CSV-Datei, die die Eigenschaften aus den exportierten Inhalten und Analyse Metadaten enthält. Dieses Exportpaket kann dann in eine eDiscovery-Überprüfungen-Anwendung importiert werden. 
    
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um die Daten eines Benutzers mithilfe von Advanced eDiscovery zu analysieren, muss dem Benutzer (der Depotbank der Daten) eine Office 365 E5-Lizenz zugewiesen werden. Alternativ können Benutzern mit einer Office 365 E1-oder E3-Lizenz eine erweiterte eDiscovery-Standalone-Lizenz zugewiesen werden. Administratoren und Compliance Officer, denen Fälle zugeordnet sind und die erweiterte eDiscovery zur Analyse von Daten verwenden, benötigen keine E5-Lizenz. 
    
- Sie müssen eDiscovery-Manager oder eDiscovery-Administrator im Office 365 Security &amp; Compliance Center sein, um die Suchergebnisse für erweiterte eDiscovery vorzubereiten. Ein eDiscovery-Manager ist Mitglied der Rollengruppe "eDiscovery-Manager". Ein eDiscovery-Administrator ist auch Mitglied der eDiscovery-Manager-Rollengruppe, ihm wurden jedoch zusätzliche eDiscovery-Berechtigungen zugewiesen. Anweisungen zum Zuweisen von eDiscovery-Administrator Berechtigungen finden Sie unter Schritt 1 in [eDiscovery-Fällen im Office 365 Security _AMP_ Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).
    
## <a name="step-1-prepare-search-results-for-advanced-ediscovery"></a>Schritt 1: Vorbereiten der Suchergebnisse für erweiterte eDiscovery

Sie können die Ergebnisse einer Suche vorbereiten, die einem eDiscovery-Fall zugeordnet ist. Wenn Sie Suchergebnisse für erweiterte eDiscovery vorbereiten, werden die Daten hochgeladen und vorübergehend in einem eindeutigen Windows Azure-Speicherbereich in der Microsoft-Cloud gespeichert. An dieser Stelle extrahiert die OCR-Funktionalität Text aus Bildern in den Suchergebnissen. In [Schritt 2](#step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery)werden dieser Text und die anderen Suchergebnis Daten in den Fall in Advanced eDiscovery geladen.
  
1. Klicken Sie im Security &amp; Compliance Center auf **Suche &amp; Untersuchung** \> **eDiscovery**, um die Liste der Fälle in Ihrem Unternehmen anzuzeigen. 
    
2. Klicken Sie neben dem Fall, dass Sie Suchergebnisse für die Analyse in Advanced eDiscovery vorbereiten möchten, auf **Öffnen** . 
    
3. Klicken Sie auf der **Start** Seite für den Fall auf **Suchen**, und wählen Sie dann die Suche aus.
    
4. Klicken Sie im Detailbereich unter **Ergebnisse mit erweiterter EDiscovery analysieren**auf **Ergebnisse für Analyse vorbereiten**.
    
    > [!NOTE]
    > Wenn die Suchergebnisse älter als 7 Tage sind, werden Sie aufgefordert, die Suchergebnisse zu aktualisieren. 
  
5. Gehen Sie auf der Seite **Ergebnisse für Analyse vorbereiten** folgendermaßen vor:  
    
    - Wählen Sie die Vorbereitung von indizierten Elementen, indizierten und nicht indizierten Elementen oder nur nicht indizierten Elementen für die Analyse in Advanced eDiscovery aus.
    
    - Legen Sie fest, ob alle Versionen von Dokumenten in SharePoint eingeschlossen werden sollen, die den Suchkriterien entsprechen. Diese Option wird nur angezeigt, wenn die Inhaltsquellen für die Suche Websites enthalten.
    
    - Geben Sie an, ob eine Benachrichtigung an eine Person gesendet oder kopiert werden soll, wenn der Vorbereitungsvorgang abgeschlossen ist und die Daten in Advanced eDiscovery verarbeitet werden können.
    
6. Klicken Sie auf **Vorbereiten**.
    
    Die Suchergebnisse werden für die Analyse mit Advanced eDiscovery vorbereitet.
    
7. Klicken Sie im Detailbereich auf **Vorbereitungsstatus überprüfen** , um Informationen zum Vorbereitungsvorgang anzuzeigen. Wenn der Vorbereitungsvorgang abgeschlossen ist, können Sie den Fall in Advanced eDiscovery aufrufen, um die Daten für die Analyse zu verarbeiten. 
    
## <a name="step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery"></a>Schritt 2: Hinzufügen der Suchergebnis Daten zum Fall in Advanced eDiscovery
<a name="step2"> </a>

Wenn die Vorbereitung abgeschlossen ist, gehen Sie als nächster Schritt zu Advanced eDiscovery und laden die Suchergebnis Daten (die in einen Azure-Speicherbereich in der Microsoft-Cloud hochgeladen wurden) in den Fall in Advanced eDiscovery. Wie bereits erläutert, müssen Sie für den Zugriff auf Advanced eDiscovery ein eDiscovery-Administrator im Security &amp; Compliance Center oder ein Administrator in Advanced eDiscovery sein.
  
> [!NOTE]
> Die Zeit, die die Daten aus dem Security &amp; Compliance Center zum Hinzufügen zu einem Fall in Advanced eDiscovery benötigt werden, variiert je nach der Größe der Ergebnisse der eDiscovery-Suche. 
  
1. Klicken Sie im Security &amp; Compliance Center auf **Suche &amp; Untersuchung** \> **eDiscovery**, um die Liste der Fälle in Ihrem Unternehmen anzuzeigen. 
    
2. Klicken Sie neben dem Fall, in den Sie Daten laden möchten, in Advanced eDiscovery auf **Öffnen** . 
    
3. Klicken Sie auf der Seite **Start** für den Fall auf **Advanced eDiscovery**. 
    
    ![Klicken Sie auf zu Advanced eDiscovery wechseln, um den Fall in Advanced eDiscovery zu öffnen.](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    Die Statusleiste **Verbinden mit Advanced eDiscovery** wird angezeigt. Wenn Sie mit Advanced eDiscovery verbunden sind, wird auf der Setup Seite für den Fall eine Liste der Container angezeigt. 
    
    ![Die Groß-/Kleinschreibung wird in Advanced eDiscovery angezeigt.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Diese Container stellen die Suchergebnisse dar, die Sie in Schritt 1 für die Analyse in Advanced eDiscovery vorbereitet haben. Beachten Sie, dass der Name des Containers den gleichen Namen wie die Suche im Fall im Security &amp; Compliance Center hat. Die Container in der Liste sind diejenigen, die Sie vorbereitet haben. Wenn ein anderer Benutzer Suchergebnisse für Advanced eDiscovery vorbereitet hat, werden die entsprechenden Container nicht in die Liste aufgenommen. 
    
4. Wenn Sie die Suchergebnis Daten aus einem Container in den Fall in Advanced eDiscovery laden möchten, wählen Sie einen Container aus, und klicken Sie dann auf **verarbeiten**.
    
## <a name="next-steps"></a>Nächste Schritte

Nachdem einem Fall die Ergebnisse einer eDiscovery-Suche hinzugefügt wurden, besteht der nächste Schritt darin, die erweiterten eDiscovery-Tools zu verwenden, um die Daten zu analysieren und den Inhalt zu identifizieren, der auf einen bestimmten Rechtsfall reagiert. Informationen zur Verwendung von Advanced eDiscovery finden Sie unter [Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md).
  
## <a name="more-information"></a>Weitere Informationen

Alle RMS-verschlüsselten e-Mail-Nachrichten, die in den Suchergebnissen enthalten sind, werden entschlüsselt, wenn Sie Sie für die Analyse in Advanced eDiscovery vorbereiten. Diese Entschlüsselungsfunktion ist standardmäßig für Mitglieder der eDiscovery-Manager-Rollengruppe aktiviert. Der Grund ist, dass die Verwaltungsrolle "RMS Decrypt" dieser Rollengruppe zugewiesen ist. Beachten Sie beim Entschlüsseln von e-Mail-Nachrichten Folgendes:
  
- Derzeit enthält diese Entschlüsselungsfunktion keine verschlüsselten Inhalte aus SharePoint-und OneDrive für Business-Websites. Nur RMS-verschlüsselte e-Mail-Nachrichten werden entschlüsselt, wenn Sie Sie exportieren.
    
- Wenn eine RMS-verschlüsselte e-Mail-Nachricht eine Anlage hat (beispielsweise ein Dokument oder eine andere e-Mail-Nachricht), die ebenfalls verschlüsselt ist, wird nur die e-Mail-Nachricht der obersten Ebene entschlüsselt.
    
- Wenn Sie verhindern möchten, dass eine Person RMS-verschlüsselte Nachrichten entschlüsselt, wenn Sie Suchergebnisse für die Analyse in Advanced eDiscovery vorbereiten, müssen Sie eine benutzerdefinierte Rollengruppe erstellen (indem Sie die integrierte eDiscovery-Manager-Rollengruppe kopieren) und dann den RMS-Server entfernen. EntSchlüsseln der Verwaltungsrolle aus der benutzerdefinierten Rollengruppe. Fügen Sie dann die Person, die Sie nicht möchten, Nachrichten als Mitglied der benutzerdefinierten Rollengruppe zu entschlüsseln.
