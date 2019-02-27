---
title: Overview of importing your organization PST files to Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.IngestionHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: 'Für Administratoren: Informationen zur Verwendung des Import Diensts im Office 365 Security &amp; Compliance Center für den Massenimport von e-Mail-Daten (PST-Dateien) in Benutzerpostfächern in Exchange Online. Dieses Thema enthält häufig gestellte Fragen und erläutert, wie der PST-Importprozess funktioniert.'
ms.openlocfilehash: 89aa1a351d0a9bcc70819f4b2657d04adc7599e2
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296778"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a>Overview of importing your organization PST files to Office 365

> [!NOTE]
> Dieser Artikel richtet sich an Administratoren. Versuchen Sie, PST-Dateien in Ihr eigenes Postfach zu importieren? Weitere Informationen finden Sie unter [Importieren von e-Mails, Kontakten und Kalendern aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)

Sie können den Import Dienst im Office 365 Security &amp; Compliance Center verwenden, um PST-Dateien schnell in Exchange Online-Postfächer in ihrer Office 365-Organisation zu importieren. Es gibt zwei Möglichkeiten zum Importieren von PST-Dateien in Office 365:
   
- **Netzwerk Upload** ![Cloud Upload](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) : Hochladen der PST-Dateien über das Netzwerk an einen temporären Azure-Speicherort in der Microsoft-Cloud. Anschließend verwenden Sie den Office 365-Import Dienst, um die PST-Daten in Postfächer in Ihrer Office 365-Organisation zu importieren. 

- **Laufwerk Versand** ![Festplatte](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) : Kopieren Sie die PST-Dateien auf eine mit BitLocker verschlüsselte Festplatte, und senden Sie dann das Laufwerk physisch an Microsoft. Wenn Microsoft die Festplatte empfängt, werden die Daten vom Rechenzentrumsmitarbeiter an einen temporären Azure-Speicherort in der Microsoft-Cloud hochgeladen. Anschließend verwenden Sie den Office 365-Import Dienst, um die Daten in Postfächer in Ihrer Office 365-Organisation zu importieren.

## <a name="step-by-step-instructions"></a>Schrittweise Anleitungen
  
In einem der folgenden Themen finden Sie detaillierte schrittweise Anweisungen zum Massenimportieren der PST-Dateien Ihrer Organisation in Office 365. 
   
- [Verwenden des Netzwerkuploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md)
- [Verwenden des Laufwerkversands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>Funktionsweise des Importierens von PST-Dateien

Hier sehen Sie eine Abbildung und eine Beschreibung des vollständigen PST-Importvorgangs. Die Abbildung zeigt den primären Workflow und die Unterschiede zwischen dem Netzwerk Upload und den Laufwerk Versandmethoden.
  
![Workflow des PST-Importvorgangs](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **Laden Sie die PST-Importtools und den Schlüssel zum privaten Azure-Speicherort herunter** – der erste Schritt besteht darin, das Tool und die Zugriffstaste herunterzuladen, die zum Hochladen der PST-Dateien verwendet wird, oder Sie auf eine Festplatte zu kopieren. Sie erhalten diese auf der Seite " **importieren** " im Office 365 &amp; Security Compliance Center. Der Schlüssel bietet Ihnen (oder im Fall des Laufwerk Versands) die erforderlichen Berechtigungen zum Hochladen von PST-Dateien an einen privaten und sicheren Azure-Speicherort. Diese Zugriffstaste ist eindeutig für Ihre Organisation und verhindert den unbefugten Zugriff auf Ihre PST-Dateien, nachdem Sie in die Microsoft-Cloud hochgeladen wurden. Beachten Sie, dass das Importieren von PST-Dateien in Office 365 für Ihre Organisation kein separates Azure-Abonnement erfordert. 
    
2. **Hochladen oder Kopieren der PST-Dateien** – der nächste Schritt hängt davon ab, ob Sie den Netzwerk Upload oder den Laufwerk Versand zum Importieren von PST-Dateien verwenden. In beiden Fällen verwenden Sie das Tool und den Secure Storage-Schlüssel, den Sie im vorherigen Schritt abgerufen haben.
    
    - **Netzwerk Upload** Das Tool AzCopy. exe (in Schritt 1 heruntergeladen) wird zum Hochladen und Speichern Ihrer PST-Dateien an einem Azure-Speicherort in der Microsoft-Cloud verwendet. Beachten Sie, dass sich der Azure-Speicherort, an den Sie Ihre PST-Dateien hochladen, im selben regionalen Microsoft-Datencenter befindet, in dem sich Ihre Office 365-Organisation befindet. 
    
      Die PST-Dateien, die Sie in Office 365 importieren möchten, müssen sich in Ihrer Organisation auf einem Dateifreigabe-oder Dateiserver befinden.
    
    - **Laufwerk Versand** Das Tool "Waimportexport. exe (in Schritt 1 heruntergeladen) wird zum Kopieren der PST-Dateien auf die Festplatte verwendet. Dieses Tool verschlüsselt die Festplatte mit BitLocker und kopiert dann das PST auf die Festplatte. Wie bei Netzwerk Upload müssen sich die PST-Dateien, die Sie auf die Festplatte kopieren möchten, auf einem Dateifreigabe-oder Dateiserver in Ihrer Organisation befinden.
    
3. **Erstellen einer PST-Import Zuordnungsdatei** – nachdem die PST-Dateien in den Azure-Speicherort hochgeladen oder auf eine Festplatte kopiert wurden, wird im nächsten Schritt eine CSV-Datei (Comma Separated Value) erstellt, die angibt, in welchen Benutzerpostfächern die PST-Dateien importiert werden sollen (a ND eine PST-Datei kann in das primäre Postfach eines Benutzers oder in sein Archivpostfach importiert werden). Der Office 365-Import Dienst verwendet die Informationen, um die PST-Dateien zu importieren. 
    
4. **Erstellen eines PST-importauftrags** – im nächsten Schritt erstellen Sie auf der Seite " **importieren** " im Security &amp; Compliance Center einen PST-Importauftrag und übermitteln die im vorherigen Schritt erstellte PST-Import Zuordnungsdatei. Für Netzwerk Upload (da die PST-Dateien in Azure hochgeladen wurden) analysiert Office 365 die Daten in den PST-Dateien und gibt Ihnen dann die Möglichkeit, Filter festzulegen, die Steuern, welche Daten tatsächlich in die in der PST-Import Zuordnungsdatei angegebenen Postfächer importiert werden. 
    
    Bei Laufwerk Versand werden an dieser Stelle im Prozess einige zusätzliche Schritte ausgeführt.
    
    - Sie senden die Festplatte physisch an ein Microsoft-Datencenter (die Versandadresse des Microsoft-Datencenters wird angezeigt, wenn der Importauftrag erstellt wird).
    
    - Wenn Microsoft die Festplatte empfängt, lädt das Personal des Rechenzentrums die PST-Dateien auf der Festplatte an den Azure-Speicherort für Ihre Organisation hoch. Wie bereits erläutert, werden Ihre PST-Dateien an einen Azure-Speicherort hochgeladen, der sich im selben regionalen Microsoft-Datencenter befindet, in dem sich Ihre Office 365-Organisation befindet.
    
      > [!NOTE]
      > Die PST-Dateien auf der Festplatte werden innerhalb von 7 bis 10 Arbeitstagen nach Azure hochgeladen, nachdem Microsoft die Festplatte erhalten hat. 
  
      Wie beim Netzwerk-Upload analysiert Office 365 dann die Daten in den PST-Dateien und bietet Ihnen die Möglichkeit, Filter festzulegen, die Steuern, welche Daten tatsächlich in die in der PST-Import Zuordnungsdatei angegebenen Postfächer importiert werden.
    
    - Microsoft sendet die Festplatte an Sie zurück. 
    
5. **Filtern der PST-Daten, die in Postfächer importiert** werden – nachdem der Importauftrag erstellt wurde (und nachdem die PST-Dateien von einem Laufwerk Versandauftrag in den Azure-Speicherort hochgeladen wurden), analysiert Office 365 die Daten in den PST-Dateien (sicher und zuverlässig) durch Identifizieren des Alters der Elemente und der verschiedenen Nachrichtentypen, die in den PST-Dateien enthalten sind. Wenn die Analyse abgeschlossen ist und die Daten zum Importieren bereit sind, haben Sie die Möglichkeit, alle in den PST-Dateien enthaltenen Daten zu importieren, oder Sie können die importierten Daten trimmen, indem Sie Filter festlegen, die Steuern, welche Daten importiert werden. 
    
6. **Starten des PST-importauftrags** – nachdem der Importauftrag gestartet wurde, verwendet Office 365 die Informationen in der PST-Import Zuordnungsdatei, um die PST-Dateien aus dem Azure-Speicher Speicherort in Benutzerpostfächer zu importieren. Status Informationen zum Importauftrag (einschließlich Informationen zu jeder importierten PST-Datei) werden auf der Seite " **importieren** " im Security &amp; Compliance Center angezeigt. Wenn der Importauftrag abgeschlossen ist, wird der Status für den Auftrag auf **abgeschlossen**festgelegt.
  
## <a name="why-import-email-data-to-office-365"></a>Gründe für das Importieren von e-Mail-Daten in Office 365

- Das Importieren von PST-Dateien in Benutzerpostfächer ist eine Möglichkeit, die e-Mails Ihrer Organisation zu Office 365 zu migrieren.
    
- Mithilfe der [intelligenten Import](filter-data-when-importing-pst-files.md) Funktion können Sie die Elemente in PST-Dateien filtern, die tatsächlich in die Zielpostfächer importiert werden. Auf diese Weise können Sie die importierten Daten trimmen, indem Sie Filter festlegen, die Steuern, welche Daten importiert werden. 
    
- Durch das Importieren von e-Mail-Daten in Office 365 können Sie die Compliance-Anforderungen Ihrer Organisation erfüllen, indem Sie Folgendes zulassen:
    
  - Aktivieren Sie [Archivpostfächer](enable-archive-mailboxes.md) und [unbegrenzte Archivierung](unlimited-archiving.md) , um Benutzern zusätzlichen Speicherplatz für Postfächer bereitzustellen. 
    
  - Aufbewahrung von Post [](https://go.microsoft.com/fwlink/?linkid=841243) Fächern für das Aufbewahren von Inhalten 
    
  - Verwenden Sie das [Inhaltssuche-Tool](content-search.md) , um nach Postfachinhalten zu suchen. 
    
  - Verwenden von [eDiscovery-Fällen](ediscovery-cases.md) zum Verwalten von rechtlichen Untersuchungen in Ihrer Organisation 
    
  - Verwenden Sie [Aufbewahrungsrichtlinien](retention-policies.md) im &amp; Security Compliance Center, um zu steuern, wie lange Postfachinhalte aufbewahrt werden, und löschen Sie dann nach Ablauf des Aufbewahrungszeitraums Inhalte. 
    
- Das Importieren von Daten in Office 365 schützt vor Datenverlust. E-Mail-Daten, die in Office 365 importiert werden, erben die Hochverfügbarkeitsfeatures von Exchange Online.
    
- E-Mail-Daten in Office 365 sind für Benutzer auf allen Geräten verfügbar, da Sie in der Cloud gespeichert sind.
    
## <a name="importing-sharepoint-data-to-office-365"></a>Importieren von SharePoint-Daten in Office 365

Sie können auch Dateien und Dokumente in SharePoint-Websites und OneDrive-Konten in Ihrer Office 365-Organisation importieren. Weitere Informationen finden Sie in den folgenden Artikeln:

- [Migration zu SharePoint Online](https://docs.microsoft.com/sharepointmigration/migrate-to-sharepoint-online)

- [Einführung in das SharePoint-Migrationstool](https://docs.microsoft.com/sharepointmigration/introducing-the-sharepoint-migration-tool)

- [Migrieren zu SharePoint Online mithilfe von PowerShell](https://docs.microsoft.com/sharepointmigration/overview-spmt-ps-cmdlets)

- [Migrieren Ihrer Dateifreigabe Inhalte zu SharePoint Online mithilfe des Azure-Datenfelds](https://docs.microsoft.com/sharepointmigration/how-to-migrate-file-share-content-to-spo-using-azuredatabox)


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a>Häufig gestellte Fragen zum Importieren von PST-Dateien in Office 365
  
Hier finden Sie einige häufig gestellte Fragen zur Verwendung des Office 365-Import Diensts zum Massenimport von PST-Dateien in Office 365-Postfächer. 
  
- [Verwenden des Netzwerk Uploads zum Importieren von PST-Dateien](#using-network-upload-to-import-pst-files)
  
- [Verwenden des Laufwerk Versands zum Importieren von PST-Dateien](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a>Verwenden des Netzwerk Uploads zum Importieren von PST-Dateien

 **Welche Berechtigungen sind erforderlich, um Importaufträge im Office 365-Import Dienst zu erstellen?**
  
Sie müssen die Rolle "Postfachimport-export" in Exchange Online zuweisen, um PST-Dateien in Office 365-Postfächer zu importieren. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. Sie können die Rolle "Post Fach Import-Export" zur Rollengruppe "Organisationsverwaltung" hinzufügen. Sie können auch eine neue Rollengruppe erstellen, die Export Rolle Post Fach Import zuweisen und sich selbst oder andere Benutzer als Mitglied hinzufügen. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Darüber hinaus muss eine der folgenden Anforderungen erfüllt sein, um &amp; Importaufträge im Office 365 Security Compliance Center zu erstellen:
  
- Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden. Diese Rolle wird standardmäßig den Rollengruppen Organisationsverwaltung und Empfängerverwaltung zugewiesen.
    
    Oder
    
- Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange Online, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die erforderlichen Mindestberechtigungen zum Importieren von PST-Dateien die Rollen Mailbox Import Export und e-Mail-Empfänger der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
 **Wo ist der Netzwerk Upload verfügbar?**
  
Der Netzwerk Upload ist derzeit in den USA, Kanada, Brasilien, Großbritannien, Europa, Indien, Ostasien, Südostasien, Japan, Südkorea und Australien verfügbar. Der Netzwerk Upload steht in Kürze in weiteren Regionen zur Verfügung.
  
 **Wie hoch sind die Preise für den Import von PST-Dateien mithilfe des Netzwerk Uploads?**
  
Die Verwendung des Netzwerk Uploads zum Importieren von PST-Dateien ist kostenlos.
  
Dies hat auch zur Folge, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag im Office 365 Admin Center angezeigt werden. Auch wenn ein Importauftrag möglicherweise noch auf der Seite **Import Data to Office 365** aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **Welche Version des PST-Dateiformats wird für den Import in Office 365 unterstützt?**
  
Es gibt zwei Versionen des PST-Dateiformats: ANSI und Unicode. Es wird empfohlen, Dateien zu importieren, die das Unicode-PST-Dateiformat verwenden. Dateien, die das ANSI-PST-Dateiformat verwenden, beispielsweise für Sprachen, die einen Doppelbyte-Zeichensatz (DBCS) verwenden, können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 4 bei [Verwendung des Netzwerk Uploads zum Importieren von PST-Dateien in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=823074).
  
Darüber hinaus können PST-Dateien aus Outlook 2007 und neueren Versionen in Office 365 importiert werden.
  
 **Nachdem ich meine PST-Dateien in den Azure-Speicherbereich hochgeladen habe, wie lange werden Sie in Azure aufbewahrt, bevor Sie gelöscht werden?**
  
Wenn Sie die Netzwerk-Upload-Methode zum Importieren von PST-Dateien verwenden, laden Sie Sie in einen Azure-BLOB-Container mit dem Namen **ingestiondata**hoch. Wenn auf der Seite " **importieren** " im Security &amp; Compliance Center keine Importaufträge ausgeführt werden), werden alle PST-Dateien im **ingestiondata** -Container in Azure 30 Tage nach der Erstellung des letzten importauftrags im Security &amp;Compliance Center. Dies erfordert auch, dass Sie einen neuen Importauftrag im Security &amp; Compliance Center (beschrieben in Schritt 5 in den Anweisungen zum Netzwerk Upload) innerhalb von 30 Tagen nach dem Hochladen von PST-Dateien in Azure erstellen müssen. 
  
Dies führt auch dazu, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag &amp; im Security Compliance Center angezeigt werden. Auch wenn auf der Seite " **importieren** " im Security &amp; Compliance Center möglicherweise noch ein Importauftrag aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **Wie lange dauert es, bis eine PST-Datei in ein Postfach importiert wird?**
  
Es hängt von der Kapazität Ihres Netzwerks ab, es dauert jedoch in der Regel mehrere Stunden, bis jedes Terabyte (TB) an Daten in den Azure-Speicherbereich für Ihre Organisation hochgeladen wird. Nachdem die PST-Dateien in den Azure-Speicherbereich kopiert wurden, wird eine PST-Datei mit einer Rate von mindestens 24 GB pro Tag in ein Office 365-Postfach importiert. Wenn diese Rate Ihren Anforderungen nicht entspricht, können Sie andere Methoden für die Migration von e-Mail-Daten zu Office 365 berücksichtigen. Weitere Informationen finden Sie unter [Möglichkeiten zum Migrieren mehrerer e-Mail-Konten zu Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Wenn unterschiedliche PST-Dateien in unterschiedliche Zielpostfächer importiert werden, erfolgt der Importprozess parallel; in anderen Worten, jedes PST/Mailbox-Paar wird gleichzeitig importiert. Wenn mehrere PST-Dateien in dasselbe Postfach importiert werden, werden diese gleichzeitig importiert.
  
 **Gibt es einen Grenzwert für die Nachrichtengröße beim Importieren von PST-Dateien?**
  
Ja. Wenn eine PST-Datei ein Postfachelement enthält, das größer als 150 MB ist, wird das Element während des Importvorgangs übersprungen.
  
 **Sind Nachrichteneigenschaften, beispielsweise wenn die Nachricht gesendet oder empfangen wurde, die Liste der Empfänger und andere Eigenschaften, die beim Importieren von PST-Dateien in ein Office 365-Postfach aufbewahrt werden?**
  
Ja. Die ursprünglichen Nachrichten Metadaten werden während des Importvorgangs nicht geändert.
  
 **Gibt es eine Grenze für die Anzahl der Ebenen in einer Ordnerhierarchie für eine PST-Datei, die in ein Postfach importiert werden soll?**
  
Ja. Sie können keine PST-Datei mit 300 oder mehr Ebenen von geschachtelten Ordnern importieren.
  
 **Kann ich den Netzwerk Upload verwenden, um PST-Dateien in ein inaktives Postfach in Office 365 zu importieren?**
  
Ja, diese Funktion ist jetzt verfügbar.
  
 **Kann ich den Netzwerk Upload zum Importieren von PST-Dateien in ein Onlinearchivpostfach in einer Exchange-hybridbereitstellung verwenden?**
  
Ja, diese Funktion ist jetzt verfügbar.
  
 **Kann ich den Netzwerk Upload zum Importieren von PST-Dateien in öffentliche Ordner in Exchange Online verwenden?**
  
Nein, Sie können PST-Dateien nicht in öffentliche Ordner importieren.
  
### <a name="using-drive-shipping-to-import-pst-files"></a>Verwenden des Laufwerk Versands zum Importieren von PST-Dateien

 **Welche Berechtigungen sind erforderlich, um Importaufträge im Office 365-Import Dienst zu erstellen?**
  
Sie müssen der Postfachimport-export Rolle zugewiesen sein, um PST-Dateien in Office 365-Postfächer zu importieren. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. Sie können die Rolle "Post Fach Import-Export" zur Rollengruppe "Organisationsverwaltung" hinzufügen. Sie können auch eine neue Rollengruppe erstellen, die Export Rolle Post Fach Import zuweisen und sich selbst oder andere Benutzer als Mitglied hinzufügen. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Darüber hinaus muss eine der folgenden Anforderungen erfüllt sein, um &amp; Importaufträge im Office 365 Security Compliance Center zu erstellen:
  
- Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden. Diese Rolle wird standardmäßig den Rollengruppen Organisationsverwaltung und Empfängerverwaltung zugewiesen.
    
    Oder
    
- Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange Online, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die erforderlichen Mindestberechtigungen zum Importieren von PST-Dateien die Rollen Mailbox Import Export und e-Mail-Empfänger der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
 **Wo ist der Laufwerk Versand verfügbar?**
  
Der Laufwerk Versand ist derzeit in den USA, Kanada, Brasilien, Großbritannien, Europa, Indien, Ostasien, Südostasien, Japan, Südkorea und Australien verfügbar. Der Laufwerk Versand wird in Kürze mehr Regionen verfügbar sein.
  
 **Welche kommerziellen Lizenzvereinbarungen unterstützen den Laufwerk Versand?**
  
Laufwerk Versand zum Importieren von PST-Dateien in Office 365 ist über einen Microsoft Enterprise Agreement (EA) verfügbar. Der Laufwerk Versand ist nicht über einen Microsoft-Produkt-und-Dienstvertrag (MPSA) verfügbar.
  
 **Wie hoch sind die Preise für die Verwendung des Laufwerk Versands zum Importieren von PST-Dateien in Office 365?**
  
Die Kosten für die Verwendung des Laufwerk Versands zum Importieren von PST-Dateien in Office 365-Postfächern sind $2 USD pro GB Daten. Wenn Sie beispielsweise eine Festplatte mit 1.000 GB (1 TB) von PST-Dateien versenden, sind die Kosten $2.000 USD. Sie können mit einem Partner zusammenarbeiten, um die Import Gebühr zu bezahlen. Informationen zum Suchen eines Partners finden Sie unter [Suchen Ihres Office 365-Partners oder](https://go.microsoft.com/fwlink/p/?LinkId=785197)-Händlers.
  
 **Welche Art von Festplatten werden für den Laufwerk Versand unterstützt?**
  
Nur 2,5 Zoll-Solid-State-Laufwerke (SSDs) oder 2,5-oder 3,5-Zoll-SATA II/III-Festplatten werden für die Verwendung mit dem Office 365-Import Dienst unterstützt. Sie können Festplatten mit bis zu 10 TB verwenden. Bei Import Aufträgen wird nur das erste Datenvolume auf der Festplatte verarbeitet. Das Datenvolume muss mit NTFS formatiert sein. Wenn Sie Daten auf eine Festplatte kopieren, können Sie Sie direkt mit einem 2,5-Zoll-SSD oder 2,5-oder 3,5-Zoll-SATA II/III-Stecker anhängen, oder Sie können Sie extern über einen externen 2,5-Zoll-SSD oder 2,5-oder 3,5-Zoll-SATA II/III-USB-Adapter anschließen.
  
> [!IMPORTANT]
> Externe Festplatten, die mit einem integrierten USB-Adapter geliefert werden, werden vom Office 365-Import Dienst nicht unterstützt. Darüber hinaus kann der Datenträger innerhalb des Gehäuses einer externen Festplatte nicht verwendet werden. Senden Sie keine externen Festplatten. 
  
 **Wie viele Festplatten kann ich für einen einzelnen Importauftrag liefern?**
  
Sie können maximal 10 Festplatten für einen einzelnen Importauftrag versenden.
  
 **Wie lange dauert es, bis Sie nach dem Versand meiner Festplatte zum Microsoft-Datencenter gelangen?**
  
Dies hängt von einigen Faktoren ab, beispielsweise von der Nähe zum Microsoft-Datencenter und von der Art der Versandoption, die Sie zum Versenden der Festplatte verwendet haben (beispielsweise Zustellung am nächsten Tag, Zustellung von zwei Tagen oder Boden Zustellung). Bei den meisten Versendern können Sie die Verfolgungsnummer verwenden, um den Status ihrer Zustellung nachzuverfolgen.
  
 **Wie lange dauert es, bis meine PST-Dateien in Azure hochgeladen werden, nachdem meine Festplatte im Microsoft-Datencenter eingegangen ist?**
  
Nachdem die Festplatte im Microsoft-Datencenter eingegangen ist, dauert es zwischen 7 und 10 Werktage, die PST-Dateien in den Microsoft Azure-Speicherbereich für Ihre Organisation hochzuladen. Die PST `ingestiondata`-Dateien werden in einen Azure-BLOB-Container hochgeladen. 
  
 **Wie lange dauert es, bis eine PST-Datei in ein Postfach importiert wird?**
  
Nachdem die PST-Dateien in den Azure-Speicherbereich hochgeladen wurden, analysiert Office 365 die Daten in den PST-Dateien (auf sichere und sichere Weise), um das Alter der Elemente und die verschiedenen Nachrichtentypen in den PST-Dateien zu identifizieren. Wenn diese Analyse abgeschlossen ist, haben Sie die Möglichkeit, alle Daten in den PST-Dateien zu importieren oder Filter festzulegen, die Steuern, welche Daten importiert werden. Nachdem Sie den Importauftrag gestartet haben, wird eine PST-Datei mit einer Rate von mindestens 24 GB pro Tag in ein Office 365-Postfach importiert. Wenn diese Rate Ihren Anforderungen nicht entspricht, können Sie andere Methoden zum Importieren von e-Mail-Daten in Office 365 berücksichtigen. Weitere Informationen finden Sie unter [Möglichkeiten zum Migrieren mehrerer e-Mail-Konten zu Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Wenn unterschiedliche PST-Dateien in unterschiedliche Zielpostfächer importiert werden, erfolgt der Importprozess parallel; in anderen Worten, jedes PST/Mailbox-Paar wird gleichzeitig importiert. Wenn mehrere PST-Dateien in dasselbe Postfach importiert werden, werden diese gleichzeitig importiert.
  
 **Nachdem Microsoft meine PST-Dateien in Azure hochgeladen hat, wie lange werden Sie in Azure aufbewahrt, bevor Sie gelöscht werden?**
  
Alle PST-Dateien am Azure-Speicherort für Ihre Organisation (im BLOB-Container `ingestiondata`mit dem Namen) werden 30 Tage nach dem letzten Importauftrag auf der Seite " **importieren** " im Security &amp; Compliance Center gelöscht. 
  
Dies führt auch dazu, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag &amp; im Security Compliance Center angezeigt werden. Auch wenn auf der Seite " **importieren** " im Security &amp; Compliance Center möglicherweise noch ein Importauftrag aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **Welche Version des PST-Dateiformats wird für den Import in Office 365 unterstützt?**
  
Es gibt zwei Versionen des PST-Dateiformats: ANSI und Unicode. Es wird empfohlen, Dateien zu importieren, die das Unicode-PST-Dateiformat verwenden. Dateien, die das ANSI-PST-Dateiformat verwenden, beispielsweise für Sprachen, die einen Doppelbyte-Zeichensatz (DBCS) verwenden, können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 3: [Verwenden des Laufwerk Versands zum Importieren Ihrer Organisations-PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
Darüber hinaus können PST-Dateien aus Outlook 2007 und neueren Versionen in Office 365 importiert werden.
  
 **Gibt es einen Grenzwert für die Nachrichtengröße beim Importieren von PST-Dateien?**
  
Ja. Wenn eine PST-Datei ein Postfachelement enthält, das größer als 150 MB ist, wird das Element während des Importvorgangs übersprungen.
  
 **Sind Nachrichteneigenschaften, beispielsweise wenn die Nachricht gesendet oder empfangen wurde, die Liste der Empfänger und andere Eigenschaften, die beim Importieren von PST-Dateien in ein Office 365-Postfach aufbewahrt werden?**
  
Ja. Die ursprünglichen Nachrichten Metadaten werden während des Importvorgangs nicht geändert.
  
 **Gibt es eine Grenze für die Anzahl der Ebenen in einer Ordnerhierarchie für eine PST-Datei, die in ein Postfach importiert werden soll?**
  
Ja. Sie können keine PST-Datei mit 300 oder mehr Ebenen von geschachtelten Ordnern importieren.
  
 **Kann ich den Laufwerk Versand verwenden, um PST-Dateien in ein inaktives Postfach in Office 365 zu importieren?**
  
Ja, diese Funktion ist jetzt verfügbar.
  
 **Kann ich den Laufwerk Versand verwenden, um PST-Dateien in ein Onlinearchivpostfach in einer Exchange-hybridbereitstellung zu importieren?**
  
Ja, diese Funktion ist jetzt verfügbar.
  
 **Kann ich den Laufwerk Versand verwenden, um PST-Dateien in öffentliche Ordner in Exchange Online zu importieren?**
  
Nein, Sie können PST-Dateien nicht in öffentliche Ordner importieren.
  
 **Kann Microsoft meine Festplatte löschen, bevor Sie Sie an mich zurückschickt?**
  
Nein, Microsoft kann keine Festplatten löschen, bevor Sie an Kunden zurückgeliefert werden. Festplatten werden in demselben Zustand an Sie zurückgegeben, in dem Sie von Microsoft empfangen wurden.
  
 **Kann Microsoft meine Festplatte Schreddern, anstatt Sie an mich zurückzustellen?**
  
Nein, Microsoft kann die Festplatte nicht zerstören. Festplatten werden in demselben Zustand an Sie zurückgegeben, in dem Sie von Microsoft empfangen wurden.
  
 **Welche Kurierdienste werden für den Rückversand unterstützt?**
  
Wenn Sie ein Kunde in den USA oder Europa sind, verwendet Microsoft FedEx, um Ihre Festplatte zurückzugeben. Für alle anderen Regionen verwendet Microsoft DHL.
  
 **Was sind die Versandkosten?**
  
Die Versandkosten variieren je nach der Nähe des Microsoft-Datencenters, auf das Sie Ihre Festplatte versandt haben. Microsoft berechnet Ihr FedEx-oder DHL-Konto, um Ihre Festplatte zurückzugeben. Die Kosten für den Versand sind in ihrer Verantwortung.
  
 **Kann ich einen benutzerdefinierten Kurierversand Dienst verwenden, beispielsweise FedEx Custom Shipping, um meine Festplatte an Microsoft zu senden?**
  
Ja.
  
 **Muss ich meine Festplatte an ein anderes Land senden, muss ich irgendetwas tun?**
  
Die Festplatte, die Sie an Microsoft senden, muss möglicherweise internationale Grenzen überschreiten. In diesem Fall müssen Sie sicherstellen, dass die Festplatte und die darin enthaltenen Daten in Übereinstimmung mit den anwendbaren Gesetzen importiert und/oder exportiert werden. Bevor Sie eine Festplatte versenden, erkundigen Sie sich bei ihren Beratern, ob Laufwerk und Daten rechtlich an das angegebene Microsoft-Datencenter geliefert werden können. Dadurch wird sichergestellt, dass Microsoft rechtzeitig erreicht wird.
