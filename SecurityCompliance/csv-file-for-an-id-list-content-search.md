---
title: Vorbereiten einer CSV-Datei für eine Inhaltssuche in der ID-Liste in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Verwenden Sie die Datei results. CSV oder unindexed Items. CSV aus einer vorhandenen Inhaltssuche, um eine ID-Listensuche zu erstellen, die bestimmte e-Mail-Nachrichten zurückgibt. ID-Listen suchen werden normalerweise verwendet, um teilweise indizierte Postfachelemente zurückzugeben.
ms.openlocfilehash: 558a8512ed133995b2cc1d0d8b78fd7f08d11168
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296738"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a>Vorbereiten einer CSV-Datei für eine Inhaltssuche in der ID-Liste in Office 365

Sie können mithilfe einer Liste von Exchange-IDs nach bestimmten e-Mail-Nachrichten und anderen Postfachelementen suchen. Um eine ID-Listensuche (formell als gezielte Suche bezeichnet) zu erstellen, übermitteln Sie eine CSV-Datei (Comma Separated Value), die die zu suchenden Postfachelemente identifiziert. Für diese CSV-Datei verwenden Sie die Datei **results. CSV** oder die unindizierte **Items. CSV** -Datei, die beim Exportieren der Inhalts Suchergebnisse oder beim Exportieren eines Inhalts Suchberichts aus einer vorhandenen Inhaltssuche enthalten sind. Bearbeiten Sie dann eine dieser Dateien, um die zu suchenden Elemente anzugeben, und erstellen Sie dann eine neue ID-Listensuche, und übermitteln Sie die CSV-Datei. 
  
Im folgenden finden Sie eine kurze Übersicht über das Verfahren zum Erstellen einer ID-Listensuche.
  
1. Erstellen Sie eine neue oder geführte Inhaltssuche im Security &amp; Compliance Center, und führen Sie Sie aus.
    
2. Exportieren der Inhalts Suchergebnisse oder Exportieren des Inhalts Suchberichts. Weitere Informationen finden Sie unter:
    
    - [Exportieren von Inhalts Suchergebnissen aus dem Office 365 &amp; Security Compliance Center](export-search-results.md)
    
    - [Exportieren eines Inhaltssuchberichts](export-a-content-search-report.md)
    
3. Bearbeiten Sie die Datei **results. CSV** oder die unindizierten **Elemente. CSV** , und identifizieren Sie die bestimmten Postfachelemente, die Sie in die ID-Listensuche einbeziehen möchten. Weitere Informationen finden Sie in den [Anweisungen](#prepare-the-csv-file-for-an-id-list-search) zum Vorbereiten einer CSV-Datei für eine ID-Listensuche. 
    
4. Erstellen Sie eine neue ID-Listensuche (siehe die [Anweisungen](#create-an-id-list-search)), und übermitteln Sie die von Ihnen VORBEREITETE CSV-Datei. Die Suchabfrage, die erstellt wird, sucht nur nach den in der CSV-Datei ausgewählten Elementen.
    
> [!NOTE]
> ID-Listen suchen werden nur für Postfachelemente unterstützt. Sie können nicht in einer ID-Listensuche nach SharePoint-und OneDrive-Dokumenten suchen. 
  
 **Gründe für das Erstellen einer ID-Listensuche** Wenn Sie nicht ermitteln können, ob ein Element auf eine eDiscovery-Anforderung basierend auf den Metadaten in den Dateien " **results.** CSV" oder "unindiziered **Items. CSV** " reagiert, verwenden Sie eine ID-Listensuche, um dieses Element zu suchen, in der Vorschau anzuzeigen und es dann zu exportieren, um zu ermitteln, ob es reagiert auf den Fall, den Sie untersuchen. ID-Listen suchen werden normalerweise verwendet, um nach einem bestimmten Satz von nicht indizierten Elementen zu suchen und diesen zurückzugeben. 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a>Vorbereiten der CSV-Datei für eine ID-Listensuche

Nachdem Sie die Suchergebnisse oder den Bericht für eine Inhaltssuche exportiert haben, können Sie die folgenden Schritte ausführen, um die CSV-Datei für eine ID-Listensuche vorzubereiten. Diese CSV-Datei identifiziert jedes Element in der ID-Listensuche.
  
Beachten Sie, dass Sie eine CSV-Datei aus einer Suche mit SharePoint-Websites und OneDrive-Konten verwenden können, aber Sie können *nur* Postfachelemente für eine ID-Listensuche auswählen. Wenn Sie ein Dokument in SharePoint oder OneDrive auswählen, schlägt die Überprüfung der CSV-Datei fehl, wenn Sie eine ID-Listensuche erstellen. 
  
1. Öffnen Sie die Datei **results. CSV** oder unindexed **Items. CSV** in Excel. 
    
2. Fügt eine neue Spalte und einen Namen **** ein. Es spielt keine Rolle, wo Sie die Spalte einfügen. Zur Vereinfachung empfiehlt es sich, es Links von der ersten Spalte einzufügen.
    
3. Geben Sie in der **ausgewählten** Spalte **Ja** in der Zelle ein, die dem Element entspricht, nach dem Sie suchen möchten. Wiederholen Sie diesen Schritt für jedes Element, nach dem Sie suchen möchten. 
    
    > [!IMPORTANT]
    > Wenn Sie die CSV-Datei in Excel öffnen, wird das Datenformat für die **Dokument-ID-** Spalte in **Allgemein**geändert. Dadurch wird die Dokument-ID für ein Element in wissenschaftlicher Schreibweise angezeigt. Die Dokument-ID "481037338205" wird beispielsweise als "4.81037 E + 11" angezeigt, wenn Sie die nächsten Schritte ausführen müssen, um das Datenformat der **Dokument-ID-** Spalte in **Number** zu ändern, um das richtige Format für die Dokument-ID wiederherzustellen. Wenn Sie dies nicht tun, schlägt die ID-Listensuche, die die CSV-Datei verwendet, fehl. 
  
4. Klicken Sie mit der rechten Maustaste auf die gesamte **Dokument-ID** -Spalte, und wählen Sie **Zellen formatieren**aus.
    
5. Klicken Sie im Feld **Kategorie** auf **Zahl**.
    
6. Ändern Sie die Anzahl der Dezimalstellen in **0**, und klicken Sie dann auf **OK** , um die Änderungen zu speichern. Beachten Sie, dass die Werte in der Spalte Dokument-ID in Zahlen geändert werden. 
    
    Nachfolgend finden Sie ein Beispiel für eine CSV-Datei, die für die Inhaltssuche einer ID-Liste eingereicht werden kann.
    
    ![Beispiel einer CSV-Datei für eine gezielte Inhaltssuche](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. Speichern Sie die CSV-Datei **** , oder speichern Sie die Datei mit einem anderen Dateinamen speichern unter. In beiden Fällen müssen Sie die Datei im CSV-Format speichern. 
  
## <a name="create-an-id-list-search"></a>Erstellen einer ID-Listensuche

Im nächsten Schritt erstellen Sie eine neue ID-Listeninhalts Suche und übermitteln die CSV-Datei, die Sie im vorherigen Schritt vorbereitet haben.
  
> [!IMPORTANT]
> Sie sollten eine ID-Listensuche nicht mehr als 2 Tage nach dem Export der Ergebnisse oder Berichte aus einer Inhaltssuche erstellen. Wenn die Suchergebnisse oder der Bericht vor mehr als zwei Tagen exportiert wurden, sollten Sie die Suchergebnisse oder den Bericht erneut exportieren, um aktualisierte CSV-Dateien zu generieren. Anschließend können Sie eine der aktualisierten CSV-Dateien vorbereiten und diese verwenden, um eine ID-Listensuche zu erstellen. 
  
1. Navigieren Sie im &amp; Security Compliance Center zu Such **Suche &amp; ** \> - **Inhaltssuche**.
    
2. Klicken Sie auf der Seite **Suchen** auf den Pfeil neben ![Symbol](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **neue Suche**hinzufügen, und klicken Sie dann auf **nach ID-Liste suchen**.
    
    ![Klicken Sie in der Dropdownliste neue Suche auf nach ID-Liste suchen.](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. Geben Sie im Flyout **Suche nach ID-Liste** die Suche an (und beschreiben Sie Sie optional), und klicken Sie dann auf **Durchsuchen** , und wählen Sie die CSV-Datei aus, die Sie im vorherigen Schritt vorbereitet haben. 
    
    Office 365 versucht, die CSV-Datei zu überprüfen. Wenn die Überprüfung nicht erfolgreich ist, wird eine Fehlermeldung angezeigt, die Ihnen bei der Behandlung der Validierungsfehler helfen kann. Die CSV-Datei muss erfolgreich validiert werden, um eine ID-Listensuche zu erstellen.
    
4. Nachdem die CSV-Datei erfolgreich überprüft wurde, klicken Sie auf **Suchen** , um die ID-Listensuche zu erstellen. 
    
    NachFolgend finden Sie ein Beispiel für die geschätzten Suchergebnisse und die Abfrage, die für eine ID-Listensuche generiert wird.
    
    ![Suchabfrage für eine gezielte Inhaltssuche im Detailbereich](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    Beachten Sie, dass die Anzahl der geschätzten Elemente, die in der Statistik für die ID-Suche angezeigt werden, mit der Anzahl der Elemente übereinstimmen sollte, die Sie in der CSV-Datei ausgewählt haben.
    
5. Vorschau oder Exportieren der Elemente, die von der ID-Listensuche zurückgegeben werden.
    
> [!NOTE]
> Wenn Sie ein Postfach nach dem Erstellen einer ID-Listensuche verschieben, gibt die Abfrage für die Suche nicht die angegebenen Elemente zurück. Der Grund dafür ist, dass die **Document** -Eigenschaft für Postfachelemente geändert wird, wenn ein Postfach verschoben wird. In den seltenen Fällen, in denen ein Postfach verschoben wird, nachdem Sie eine ID-Listensuche erstellt haben, sollten Sie eine neue Inhaltssuche erstellen (oder die Suchergebnisse für die vorhandene Inhaltssuche aktualisieren) und dann die Suchergebnisse oder den Bericht exportieren, um aktualisierte CSV-Dateien zu generieren, die verwendet werden können.  , um eine neue ID-Listensuche zu erstellen. 
