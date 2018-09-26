---
title: Übersicht über das Importieren von Ihrer Organisation PST-Dateien in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.IngestionHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: 'Für Administratoren: erfahren Sie mehr über die Verwendung des Import-Diensts in die Office 365-Sicherheit &amp; Compliance Center e-Mail (PST-Dateien) auf die Benutzerpostfächer in Exchange Online Massenimport von Daten. Dieses Thema enthält häufig gestellte Fragen und erläutert die Funktionsweise des Importvorgangs PST-Datei.'
ms.openlocfilehash: 2bd58b879d9d4d1ff9d3d2c6c8680a0171d42689
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038018"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a>Übersicht über das Importieren von Ihrer Organisation PST-Dateien in Office 365

> [!NOTE]
> Dieser Artikel ist für Administratoren. Versuchen Sie zum Importieren von PST-Dateien an Ihrem eigenen Postfach? Finden Sie unter [Import e-Mail, Kontakte und Kalender aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)

Sie können mithilfe des Import-Dienstes in die Office 365-Sicherheit &amp; Compliance Center, um schnell-PST Massenimport von Dateien in Exchange Online-Postfächern in Office 365-Organisation. Es gibt zwei Methoden, die Sie PST-Dateien in Office 365 importieren können:
   
- **Netzwerk hochladen** ![Cloud hochladen](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) -PST-Dateien über das Netzwerk an einen temporären Azure Speicherort in der Microsoft-Cloud hochladen. Klicken Sie dann verwenden Sie den Dienst Office 365 importieren, um die PST-Daten auf Postfächer in Office 365-Organisation zu importieren. 

- **Laufwerk des Protokollversands** ![Festplatte](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) – kopieren Sie die PST-Dateien auf einer Festplatte BitLocker verschlüsselt, und klicken Sie dann das Laufwerk an Microsoft physisch liefern. Wenn Microsoft die Festplatte empfängt, hochzuladen Mitarbeiter im Rechenzentrum die Daten in einen temporären Azure Speicherort in der Microsoft-Cloud. Klicken Sie dann verwenden Sie den Dienst Office 365 importieren zum Importieren der Daten auf Postfächer in Office 365-Organisation.

## <a name="step-by-step-instructions"></a>Eine schrittweise Anleitung
  
Finden Sie unter den folgenden Themen ausführlichen, schrittweisen Anweisungen für Massenimport von PST-Dateien Ihres Unternehmens zu Office 365. 
   
- [Verwenden des Netzwerkuploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md)
- [Verwenden des Laufwerkversands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>Funktionsweise der Import von PST-Dateien

Nachfolgend finden Sie eine Abbildung und eine Beschreibung des vollständigen PST Importvorgangs. Die Abbildung veranschaulicht den primären Workflow und hebt die Unterschiede zwischen der Netzwerk-hochladen und Laufwerk ausgeliefert Methoden.
  
![Workflow der Importvorgang PST-Datei](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **Download der PST-Datei importieren, Tools und auf private Schlüssel Azure Speicherort** - der erste Schritt besteht darin, den Tool und Access Schlüssel verwendet, um die PST-Dateien hochladen oder auf einer Festplatte kopieren herunterladen. Sie erhalten diese auf der Seite **Importieren** , in die Office 365-Sicherheit &amp; Compliance Center. Der Schlüssel bietet Sie (oder Microsoft Mitarbeiter im Rechenzentrum im Fall von Laufwerk des Protokollversands) mit den erforderlichen Berechtigungen zum Hochladen von PST-Dateien an einen Speicherort für die private und sichere Azure-Speicher. Diese Tastenkombination ist in Ihrer Organisation eindeutig und verhindert nicht autorisierten Zugriff auf Ihre PST-Dateien nach dem Upload in die Microsoft-Cloud. Beachten Sie, dass das Importieren von PST-Dateien in Office 365 nicht Ihrer Organisation zu ein separates Azure-Abonnement verfügen muss. 
    
2. **Hochladen oder Kopie der PST-Dateien** – im nächsten Schritt hängt gibt an, ob Sie Netzwerk hochladen oder Laufwerk des Protokollversands verwendeten PST-Dateien zu importieren. In beiden Fällen verwenden Sie das Tool und die sicherer Speicher-Schlüssel, den Sie im vorherigen Schritt abgerufen.
    
    - **Netzwerk hochladen** Das AzCopy.exe-Tool (in Schritt 1 heruntergeladen haben) Dient zum Hochladen und PST-Dateien an einem Speicherort Azure-Speicher in der Microsoft-Cloud speichern. Beachten Sie, dass im selben Rechenzentrum für regionale Microsoft Azure Speicherort, dem Sie Ihrer PST-Dateien zum Hochladen befindet, auf dem Office 365-Organisation befindet. 
    
      Wenn sie hochladen möchten, müssen die PST-Dateien, die Sie zu Office 365 importieren möchten in einer Dateifreigabe oder Dateiserver in Ihrer Organisation befinden.
    
    - **Laufwerk des Protokollversands** Das WAImportExport.exe-Tool (in Schritt 1 heruntergeladen haben) wird verwendet, um Ihre PST-Dateien auf der Festplatte kopiert. Dieses Tool die Festplatte mit BitLocker verschlüsselt und dann wird die PST-Dateien auf die Festplatte kopiert. Wie Netzwerk hochladen haben die PST-Dateien, die auf der Festplatte kopiert werden soll, in einer Dateifreigabe oder Dateiserver in Ihrer Organisation befinden.
    
3. **Erstellen eine PST-Datei importieren Zuordnungsdatei** - nach die PST-Dateien in der Azure Speicherort hochgeladen oder in einer Festplatte kopiert wurden, im nächsten Schritt wird eine Datei mit durch Kommas getrennten Werten (CSV) zu erstellen, der angibt, welche Benutzer Postfächer die PST-Dateien zu importiert werden sollen (a Nd eine PST-Datei kann zum primären Postfach eines Benutzers oder ihrer Archivpostfach importiert werden). Importieren von Office 365-Dienst verwendet die Informationen zum Importieren der PST-Dateien. 
    
4. **Erstellen einer PST-Datei importieren Job** - der nächste Schritt besteht darin, erstellen Sie einen Auftrag für Import von PST-Datei auf der Seite **Importieren** in das Wertpapier &amp; Compliance Center, und übermitteln Sie die PST-Datei importieren Zuordnungsdatei im vorherigen Schritt erstellt haben. Für den Upload Netzwerk (, da die PST-Dateien in Azure hochgeladen wurden) Office 365 analysiert die Daten in die PST-Dateien und dann haben Sie Gelegenheit Filter festlegen, die steuern, welche Daten, auf die Postfächer in die Datei zur Zuordnung von PST-Datei importieren angegebenen importierten Ruft ab. 
    
    Für den Versand Laufwerk finden einige zusätzliche Vorgänge an diesem Punkt im Prozess.
    
    - Physisch liefern Ihnen die Festplatte in einem Microsoft-Rechenzentrum (die Adresse für das Microsoft-Rechenzentrum wird angezeigt, wenn Sie der Importauftrag erstellt wird)
    
    - Wenn Microsoft die Festplatte empfängt, Mitarbeiter im Rechenzentrum PST-Dateien auf der Festplatte auf den Speicherort der Azure-Speicher für Ihre Organisation hochgeladen werden. Wie bereits erklärt werden Ihre PST-Dateien an einem Speicherort von Azure-Speicher, der sich im selben regionale Microsoft-Rechenzentrum befindet hochgeladen, wo sich Office 365-Organisation befindet.
    
      > [!NOTE]
      > Die PST-Dateien auf der Festplatte gespeichert werden innerhalb von 7 bis 10 Arbeitstagen nach Microsoft die Festplatte erhält in Azure hochgeladen. 
  
      Wie der Netzwerk-Ladevorgang Office 365 dann analysiert die Daten in die PST-Dateien und bietet Ihnen eine Möglichkeit, Filter zu setzen, die steuern, welche Daten, auf die Postfächer in der PST-Datei importzuordnung angegebenen importierten Ruft ab.
    
    - Microsoft liefert die Festplatte für Sie. 
    
5. **Filtern die PST-Daten, die auf Postfächer importiert werden sollen** : Nachdem Sie der Importauftrag erstellt wird (und die PST-Dateien aus einem Laufwerk des Protokollversands Auftrag für den Azure Speicherort hochgeladen werden) analysiert Office 365, die Daten in die PST-Dateien (sicher und sichere) durch Identifizieren das Alter der Elemente und die verschiedenen Nachrichtentypen in PST-Dateien enthalten. Wenn die Analyse abgeschlossen ist, und die Daten zum Importieren bereit sind, Sie haben die Möglichkeit, alle Daten in die PST-Dateien importieren oder können Sie die Daten, die importiert wird durch Festlegen von Filtern, die steuern, welche Daten importierten ruft zuschneiden. 
    
6. **Starten Sie den Auftrag für Import von PST** - nach der Importauftrag gestartet wird, verwendet Office 365 die Informationen in die Datei zur Zuordnung von PST-Datei importieren zum Importieren der PST-Dateien aus dem Azure IE-Speicherort für Benutzerpostfächer. Statusinformationen über den Importauftrag (einschließlich Informationen zu jeder zu importierenden PST-Datei) wird angezeigt, auf der Seite **Importieren** in das Wertpapier &amp; Compliance Center. Wenn der Auftrag für Import abgeschlossen ist, wird der Status für den Auftrag auf **Complete**festgelegt.
  
## <a name="why-import-email-data-to-office-365"></a>Warum Importieren von e-Mail-Daten in Office 365?

- Importieren von PST-Dateien auf die Benutzerpostfächer ist eine Möglichkeit zum Migrieren von e-Mail von Ihrer Organisation zu Office 365.
    
- Das [Intelligente](filter-data-when-importing-pst-files.md) Importfeature können zum Filtern der Elemente in PST-Dateien, die tatsächlich auf die Postfächer Ziel importiert. Hiermit können Sie die Daten zuschneiden, die importiert wird, indem Sie Filter festlegen, kontrollieren, welche Daten importiert. 
    
- Importieren von e-Mail-Daten in Office 365 schützt Adresse kompatibilitätsanforderungen Ihrer Organisation, mit deren Hilfe Sie:
    
  - Aktivieren Sie [archivpostfächer](enable-archive-mailboxes.md) und [unbegrenzte Archivierung](unlimited-archiving.md) , um Benutzern zusätzliche Postfach Speicherplatz zu erteilen. 
    
  - Platzieren Sie Postfächer [Aufbewahrung für eventuelle Rechtsstreitigkeiten](https://go.microsoft.com/fwlink/?linkid=841243) , die Inhalt beibehalten werden. 
    
  - Verwenden Sie die [Inhalte Such-Tool](content-search.md) zum Suchen nach Inhalt von Postfächern. 
    
  - Verwenden von [eDiscovery-Fälle](ediscovery-cases.md) des Umgangs mit Ihrer Organisation rechtliche Ermittlungen 
    
  - Verwenden von [Aufbewahrungsrichtlinien](retention-policies.md) in das Wertpapier &amp; Compliance Center zu steuern, wie lange Postfachinhalt beibehalten wird, und klicken Sie dann löschen nach der Aufbewahrungszeitraum abgelaufen ist. 
    
- Importieren von Daten in Office 365 trägt zum Schutz vor Datenverlust. E-Mail-Daten, die in Office 365 importiert werden, erbt die Funktionen für hohe Verfügbarkeit von Exchange Online.
    
- E-Mail-Daten in Office 365 ist von allen Geräten für Benutzer verfügbar, da sie in der Cloud gespeichert ist.
    
## <a name="importing-sharepoint-data-to-office-365"></a>Importieren von SharePoint-Daten in Office 365

Sie können auch Dateien und Dokumenten auf SharePoint-Websites und OneDrive-Konten in Office 365-Organisation importieren. Weitere Informationen finden Sie in der [lokalen Inhalte zu SharePoint Online mithilfe von PowerShell-Cmdlets hochladen](https://docs.microsoft.com/sharepointmigration/upload-on-premises-content-to-sharepoint-online-using-powershell-cmdlets).


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a>Häufig gestellte Fragen zum Importieren von PST-Dateien in Office 365
  
Hier sind einige häufig gestellten Fragen zur Verwendung des Office 365 importieren-Diensts zum Massenimport-PST-Dateien in Office 365-Postfächer. 
  
- [Importieren von PST-Dateien mithilfe von Netzwerk-upload](#using-network-upload-to-import-pst-files)
  
- [Importieren von PST-Dateien mithilfe von Laufwerk des Protokollversands](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a>Importieren von PST-Dateien mithilfe von Netzwerk-upload

 **Welche Berechtigungen sind zum Erstellen von Importaufträge in der Office 365-Dienst importieren erforderlich?**
  
Sie müssen die Rolle Postfach importieren exportieren in Exchange Online zum Importieren von PST-Dateien in Office 365-Postfächer zugewiesen werden. Standardmäßig ist nicht dieser Rolle alle Rollengruppe in Exchange Online zugewiesen. Sie können die Rollengruppe "Organisationsverwaltung" Postfach Import/Export-Rolle hinzufügen. Oder Sie können eine neuen Rollengruppe erstellen, weisen Sie die Rolle Postfach Import/Export, und fügen Sie selbst oder andere Benutzer als Mitglied. Weitere Informationen finden Sie unter "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" in [Manage Role Gruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)Abschnitte.
  
Darüber hinaus Import erstellen Aufträge in der Office 365-Sicherheit &amp; Compliance Center, eine der folgenden muss true sein:
  
- Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zugewiesen werden. Standardmäßig wird diese Rolle der Organization Management und Recipient Management Rollen Gruppen zugewiesen.
    
    Oder
    
- Sie müssen ein globaler Administrator in Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange-Online, die speziell für das Importieren von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die Mindestebene von Berechtigungen, die zum Importieren von PST-Dateien erforderlich sind der neuen Rollengruppe die Rollen Postfach importieren exportieren und E-Mail-Empfänger, und fügen Sie Mitglieder. 
  
 **Wo ist die Netzwerk-Upload verfügbar?**
  
Netzwerk-Upload ist in den USA, Kanada, Brasilien, die Großbritannien, Europa, Indien, Ostasien, Südost Asien, Japan, Republik Korea und Australien derzeit verfügbar. Netzwerk-Upload Kürze Weitere Regionen verfügbar.
  
 **Was ist der Preisgestaltung für den Import von PST-Dateien mithilfe von Netzwerk-Upload?**
  
Netzwerk-Upload zum Importieren von PST-Dateien mit ist kostenlos.
  
Dies bedeutet auch, dass nach der PST-Dateien aus dem Bereich der Azure-Speicher gelöscht werden, sie nicht mehr in der Liste der Dateien für einen Auftrag abgeschlossene Import im Office 365 Administrationscenter angezeigt werden. Obwohl ein Importauftrag weiterhin auf der Seite **Importieren von Daten zu Office 365** aufgeführt sind, möglicherweise die Liste der PST-Dateien leer, wenn Sie die Details der älteren Importaufträge anzeigen. 
  
 **Welche Version von PST-Dateiformat unterstützt wird, für das Importieren in Office 365?**
  
Es gibt zwei Versionen des Dateiformats PST: ANSI und Unicode. Es wird empfohlen, Importieren von Dateien, die das Unicode-PST-Dateiformat verwenden. Jedoch Dateien, die das Dateiformat ANSI PST wie für Sprachen verwenden, die ein Double-Byte-Zeichen verwenden (DBCS) Sie können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 4 in [Verwendung Netzwerk zum Importieren von PST-Dateien zu Office 365 hochladen](https://go.microsoft.com/fwlink/p/?LinkId=823074).
  
Darüber hinaus können PST-Dateien in Outlook 2007 und höhere Versionen zu Office 365 importiert werden.
  
 **Nachdem ich meine PST-Dateien in den Bereich der Azure-Speicher hochgeladen haben, wie lange bleiben sie in Azure, bevor sie gelöscht werden?**
  
Wenn Sie die Netzwerk-Upload-Methode zum Importieren von PST-Dateien verwenden, wird diese mit einem Azure Blob-Container mit dem Namen **Ingestiondata**hochladen. Wenn es keine Importaufträge in Arbeit auf der Seite **Importieren** in das Wertpapier sind &amp; Compliance Center), und klicken Sie dann alle PST-Dateien im Container **Ingestiondata** in Azure 30 Tage nach der neueste Importauftrag, in das Wertpapier &amp;Compliance Center. Die auch bedeutet, dass Sie zum Erstellen eines neuen Importauftrags in das Wertpapier &amp; Compliance Center (in Schritt 5 in die Netzwerk-Upload-Anweisungen beschrieben) innerhalb von 30 Tagen Hochladen von PST-Dateien in Azure. 
  
Dies bedeutet auch, dass nach der PST-Dateien aus dem Bereich der Azure-Speicher gelöscht werden, sie nicht mehr in der Liste der Dateien für einen Auftrag abgeschlossene Import in das Wertpapier angezeigt werden &amp; Compliance Center. Obwohl ein Importauftrag weiterhin auf der Seite **Importieren** in das Wertpapier aufgeführt werden möglicherweise &amp; Compliance Center, die Liste der PST-Dateien möglicherweise leer sein, wenn Sie die Details der älteren Importaufträge anzeigen. 
  
 **Wie lange dauert es eine PST-Datei an ein Postfach importieren?**
  
Es hängt von der Kapazität des Netzwerks, aber er wird in der Regel mehrere Stunden für jede Terabyte (TB) von Daten in den Bereich der Azure-Speicher für Ihre Organisation hochgeladen werden. Nachdem die PST-Dateien in den Bereich der Azure-Speicher kopiert wurden, wird eine PST-Datei in ein Office 365-Postfach mit einer Rate von mindestens 24 GB pro Tag importiert. Wenn diese Rate nicht Ihren Anforderungen entsprechen, sollten Sie andere Methoden zum Migrieren von e-Mail-Daten zu Office 365. Weitere Informationen finden Sie unter [Möglichkeiten, um mehrere e-Mail-Konten zu Office 365 zu migrieren](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Wenn unterschiedliche PST-Dateien auf anderes Ziel Postfächer importiert werden, tritt der Importvorgang parallel. Anders ausgedrückt, wird jedes Paar PST-Postfach gleichzeitig importiert. Dienstanbieter entscheidet auch, wenn mehrere PST-Dateien in demselben Postfach importiert werden, werden sie gleichzeitig importiert werden.
  
 **Gibt es eine Nachrichtengröße beim Import von PST-Dateien?**
  
Ja. Wenn eine PST-Datei ein Postfach-Element, der als 150 MB überschreitet enthält, wird das Element während des Importvorgangs übersprungen.
  
 **Werden Nachrichteneigenschaften, beispielsweise, wenn die Nachricht gesendet wurde, oder erhalten haben, wird die Liste der Empfänger und andere Eigenschaften, die beim Import von PST-Dateien in ein Office 365-Postfach werden beibehalten?**
  
Ja. Die Nachrichtenmetadaten der ursprünglichen wird während des Importvorgangs nicht geändert.
  
 **Gibt es eine Beschränkung für die Anzahl der Ebenen in einer Ordnerhierarchie für eine PST-Datei, die ich an ein Postfach importieren möchten?**
  
Ja. Sie können keine PST-Datei importieren, die 300 oder mehr Ebenen geschachtelte Ordner verfügt.
  
 **Kann ich Netzwerk Upload zum Importieren von PST-Dateien in eines inaktiven Postfachs in Office 365 verwenden?**
  
Ja, diese Funktion ist jetzt verfügbar.
  
 **Kann ich Netzwerk Upload zum Importieren von PST-Dateien in einer hybridbereitstellung von Exchange online-Archiv-Postfach verwenden?**
  
Ja, diese Funktion ist jetzt verfügbar.
  
 **Kann ich Netzwerk Upload zum Importieren von PST-Dateien auf Öffentliche Ordner in Exchange Online verwenden?**
  
Sie können keine Nein, PST-Dateien auf Öffentliche Ordner importieren.
  
### <a name="using-drive-shipping-to-import-pst-files"></a>Importieren von PST-Dateien mithilfe von Laufwerk des Protokollversands

 **Welche Berechtigungen sind zum Erstellen von Importaufträge in der Office 365-Dienst importieren erforderlich?**
  
Sie müssen die Rolle des Postfachs exportieren importieren zum Importieren von PST-Dateien in Office 365-Postfächer zugewiesen werden. Standardmäßig ist nicht dieser Rolle alle Rollengruppe in Exchange Online zugewiesen. Sie können die Rollengruppe "Organisationsverwaltung" Postfach Import/Export-Rolle hinzufügen. Oder Sie können eine neuen Rollengruppe erstellen, weisen Sie die Rolle Postfach Import/Export, und fügen Sie selbst oder andere Benutzer als Mitglied. Weitere Informationen finden Sie unter "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" in [Manage Role Gruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)Abschnitte.
  
Darüber hinaus Import erstellen Aufträge in der Office 365-Sicherheit &amp; Compliance Center, eine der folgenden muss true sein:
  
- Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zugewiesen werden. Standardmäßig wird diese Rolle der Organization Management und Recipient Management Rollen Gruppen zugewiesen.
    
    Oder
    
- Sie müssen ein globaler Administrator in Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange-Online, die speziell für das Importieren von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die Mindestebene von Berechtigungen, die zum Importieren von PST-Dateien erforderlich sind der neuen Rollengruppe die Rollen Postfach importieren exportieren und E-Mail-Empfänger, und fügen Sie Mitglieder. 
  
 **Protokollversand Laufwerk ist, auf dem verfügbaren?**
  
Laufwerk des Protokollversands ist in den USA, Kanada, Brasilien, die Großbritannien, Europa, Indien, Ostasien, Südost Asien, Japan, Republik Korea und Australien derzeit verfügbar. Laufwerk des Protokollversands Kürze in mehrere Bereiche verfügbar.
  
 **Welche kommerziellen Lizenzverträge Laufwerk des Protokollversands unterstützt?**
  
Zum Importieren von PST-Dateien in Office 365 shipping Laufwerk ist über Microsoft Enterprise Agreement (EA) verfügbar. Laufwerk des Protokollversands nicht über eine Microsoft Products and Services Vereinbarung (MPSA) zur Verfügung.
  
 **Was ist der Preisgestaltung für die Verwendung von Laufwerk ausgeliefert zum Importieren von PST-Dateien in Office 365?**
  
Die Kosten für die Laufwerk des Protokollversands zum Importieren von PST-Dateien in Office 365-Postfächer verwenden ist 2 US-Dollar pro GB Daten. Wenn Sie eine Festplatte, die 1.000 GB (1 TB) PST-Dateien enthält liefern, ist die Kosten beispielsweise 2.000 US-Dollar. Sie können mit einem Partner die Import-Gebühr Zahlen arbeiten. Informationen zum Suchen nach einem Partner finden Sie unter [finden Ihrer Office 365-Partner oder Händler](https://go.microsoft.com/fwlink/p/?LinkId=785197).
  
 **Welche Art von Festplatten für Laufwerk des Protokollversands unterstützt werden?**
  
Nur 2,5 Zoll Solid-State-Laufwerke (SSDs) oder 2.5 oder 3,5 Zoll SATA II/III interne Festplatten für die Verwendung mit dem Import von Office 365-Dienst unterstützt werden. Festplatten können bis zu 10 TB. Für Projekte importieren wird nur die erste Datenvolumen auf der Festplatte verarbeitet werden. Das Datenvolume muss mit NTFS formatiert werden. Beim Kopieren von Daten auf einer Festplatte, verknüpfen Sie ihn direkt mit einem 2,5 Zoll SSD 2.5 oder 3.5 Zoll SATA II/III Connector oder können Sie es extern mit externen 2,5 Zoll SSD oder 2.5 oder 3,5 Zoll SATA II/III USB-Adapter anfügen.
  
> [!IMPORTANT]
> Externe Festplatten, die mit einer integrierten USB-Adapter geliefert werden vom Office 365-Import-Dienst nicht unterstützt. Darüber hinaus kann nicht innerhalb der Groß-/Kleinschreibung von einer externen Festplatte Datenträger verwendet werden. Bitte versenden Sie nicht externe Festplatten. 
  
 **Wie viele Festplatten kann ich für einen einzelnen Importauftrag ausgeliefert?**
  
Sie können maximal 10 Festplatten für einen einzelnen Importauftrag liefern.
  
 **Nachdem ich meine Festplatte liefern, wie lange dauert es, um die Microsoft-Rechenzentrum abzurufen?**
  
Dies hängt von ein paar Dinge, wie Ihre in der Nähe der Microsoft-Rechenzentrum und welche Art von Versandoption, die Sie auf die Festplatte (z. B. am nächsten Übermittlung, zwei Tage Übermittlung oder Grund-Delivery) liefern verwendet. Mit den meisten Versandfirmen können Sie die laufende Nummer zum Nachverfolgen des Status von Ihrer Bereitstellung.
  
 **Nach der Festplatte auf die Microsoft-Rechenzentrum eingehen, wie lange dauert es so meine PST-Dateien in Azure hoch?**
  
Nachdem die Festplatte in der Microsoft-Rechenzentrum empfangen wurde, dauert es zwischen 7 bis 10 Arbeitstage in Bereich für die Microsoft Azure-Speicherung für Ihre Organisation die PST-Dateien hochladen. Die PST-Dateien werden in Azure BLOB-Container mit dem Namen hochgeladen werden `ingestiondata`. 
  
 **Wie lange dauert es eine PST-Datei an ein Postfach importieren?**
  
Nachdem die PST-Dateien in den Bereich der Azure-Speicher hochgeladen werden, analysiert Office 365 die Daten in PST-Dateien (auf sichere Weise), um das Alter der Elemente und die verschiedenen Nachrichtentypen in PST-Dateien enthalten zu ermitteln. Wenn diese Analyse abgeschlossen ist, müssen Sie die Option aus, um alle Daten in die PST-Dateien zu importieren oder Set Filter an, die steuern, welche Daten importierten dient zum Abrufen. Nachdem Sie den Importauftrag gestartet haben, wird eine PST-Datei in ein Office 365-Postfach mit einer Rate von mindestens 24 GB pro Tag importiert. Wenn diese Rate nicht Ihren Anforderungen entsprechen, sollten Sie andere Methoden zum Importieren von e-Mail-Daten in Office 365. Weitere Informationen finden Sie unter [Möglichkeiten, um mehrere e-Mail-Konten zu Office 365 zu migrieren](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Wenn unterschiedliche PST-Dateien auf anderes Ziel Postfächer importiert werden, tritt der Importvorgang parallel. Anders ausgedrückt, wird jedes Paar PST-Postfach gleichzeitig importiert. Dienstanbieter entscheidet auch, wenn mehrere PST-Dateien in demselben Postfach importiert werden, werden sie gleichzeitig importiert werden.
  
 **Nachdem Microsoft Meine PST-Dateien in Azure hochgeladen, wie lange bleiben sie in Azure, bevor sie gelöscht werden?**
  
Alle PST-Dateien in den Speicherort der Azure-Speicher für Ihre Organisation (in Blob-Container mit dem Namen `ingestiondata`), 30 Tage nach der neueste Importauftrag auf der Seite **Importieren** in das Wertpapier erstellt wurde, werden gelöscht &amp; Compliance Center. 
  
Dies bedeutet auch, dass nach der PST-Dateien aus dem Bereich der Azure-Speicher gelöscht werden, sie nicht mehr in der Liste der Dateien für einen Auftrag abgeschlossene Import in das Wertpapier angezeigt werden &amp; Compliance Center. Obwohl ein Importauftrag weiterhin auf der Seite **Importieren** in das Wertpapier aufgeführt werden möglicherweise &amp; Compliance Center, die Liste der PST-Dateien möglicherweise leer sein, wenn Sie die Details der älteren Importaufträge anzeigen. 
  
 **Welche Version von PST-Dateiformat unterstützt wird, für das Importieren in Office 365?**
  
Es gibt zwei Versionen des Dateiformats PST: ANSI und Unicode. Es wird empfohlen, Importieren von Dateien, die das Unicode-PST-Dateiformat verwenden. Jedoch Dateien, die das Dateiformat ANSI PST wie für Sprachen verwenden, die ein Double-Byte-Zeichen verwenden (DBCS) Sie können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 3 in [verwenden, um Ihre Organisation PST-Dateien zu Office 365 importieren ausgeliefert Laufwerk](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
Darüber hinaus können PST-Dateien in Outlook 2007 und höhere Versionen zu Office 365 importiert werden.
  
 **Gibt es eine Nachrichtengröße beim Import von PST-Dateien?**
  
Ja. Wenn eine PST-Datei ein Postfach-Element, der als 150 MB überschreitet enthält, wird das Element während des Importvorgangs übersprungen.
  
 **Werden Nachrichteneigenschaften, beispielsweise, wenn die Nachricht gesendet wurde, oder erhalten haben, wird die Liste der Empfänger und andere Eigenschaften, die beim Import von PST-Dateien in ein Office 365-Postfach werden beibehalten?**
  
Ja. Die Nachrichtenmetadaten der ursprünglichen wird während des Importvorgangs nicht geändert.
  
 **Gibt es eine Beschränkung für die Anzahl der Ebenen in einer Ordnerhierarchie für eine PST-Datei, die ich an ein Postfach importieren möchten?**
  
Ja. Sie können keine PST-Datei importieren, die 300 oder mehr Ebenen geschachtelte Ordner verfügt.
  
 **Kann ich Laufwerk des Protokollversands zum Importieren von PST-Dateien in eines inaktiven Postfachs in Office 365 verwenden?**
  
Ja, diese Funktion ist jetzt verfügbar.
  
 **Kann ich Laufwerk des Protokollversands zum Importieren von PST-Dateien in einer hybridbereitstellung von Exchange online-Archiv-Postfach verwenden?**
  
Ja, diese Funktion ist jetzt verfügbar.
  
 **Kann ich Laufwerk des Protokollversands zum Importieren von PST-Dateien auf Öffentliche Ordner in Exchange Online verwenden?**
  
Sie können keine Nein, PST-Dateien auf Öffentliche Ordner importieren.
  
 **Kann Microsoft meine Festplatte Wischen, bevor sie es an mich liefern?**
  
Nein, kann nicht Microsoft Festplatten vor der Lieferung an den Kunden Wischen. Festplatten werden an Sie in dem Zustand zurückgegeben, die, denen Sie in waren, wenn sie von Microsoft empfangen wurden.
  
 **Werden Microsoft kann meine Festplatte anstelle der Lieferung an mich vernichtet?**
  
Nein, nicht Microsoft Festplatte löschen kann. Festplatten werden an Sie in dem Zustand zurückgegeben, die, denen Sie in waren, wenn sie von Microsoft empfangen wurden.
  
 **Welche Courier-Dienste für die Rückgabe des Protokollversands unterstützt werden?**
  
Wenn Sie einen Kunden in den Vereinigten Staaten oder Europa sind, wird Microsoft FedEx Festplatte zurückgegeben. Microsoft verwendet für alle Regionen DHL.
  
 **Was sind die Rückgabeparameter Versandkosten?**
  
Rückgabewerte Versandkosten, hängt von Ihrer Nähe zum Microsoft-Rechenzentrum ab, die Sie auf die Festplatte geliefert. Microsoft wird Ihr Konto FedEx oder DHL zurückzugebenden Festplatte in Rechnung gestellt. Der Rückgabewert Versandkosten liegt in Ihrer Verantwortung.
  
 **Kann ich einen benutzerdefinierten Courier Dienst wie FedEx benutzerdefinierte Versand des Protokollversands für meine Festplatte an Microsoft zu liefern verwenden?**
  
Ja.
  
 **Wenn ich meine Festplatte in ein anderes Land liefern müssen, gibt es etwas, das muss ich jetzt ausführen?**
  
Die Festplatte, die Sie an Microsoft zu liefern möglicherweise internationale Rahmen schneidet. Wenn dies der Fall ist, können Sie sicherstellen, dass die Festplatte und die darin enthaltenen Daten importiert und/oder gemäß der Gesetze exportiert werden. Überprüfen Sie vor der Lieferung einer Festplatte, mit der Berater, um sicherzustellen, dass das Laufwerk und die Daten an die angegebene Microsoft-Rechenzentrum gesetzlich geliefert werden können. Dadurch wird sichergestellt, dass er Microsoft in kurzer Zeit erreicht.
