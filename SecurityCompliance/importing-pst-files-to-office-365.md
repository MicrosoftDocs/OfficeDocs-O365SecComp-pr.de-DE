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
description: 'Für Administratoren: Informationen zur Verwendung des Import Diensts im Security & Compliance Center für den Massenimport von e-Mail-Daten (PST-Dateien) in Benutzerpostfächern in Exchange Online. Dieses Thema enthält häufig gestellte Fragen und erläutert, wie der PST-Importprozess funktioniert.'
ms.openlocfilehash: 3a7dba3db608eb45347609acef396faf73da483f
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000238"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a>Overview of importing your organization PST files to Office 365

> [!NOTE]
> Dieser Artikel richtet sich an Administratoren. Möchten Sie PST-Dateien in Ihr eigenes Postfach importieren? Weitere Informationen finden Sie unter [Importieren von e-Mails, Kontakten und Kalendern aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)

Sie können den Import Dienst im Security & Compliance Center verwenden, um PST-Dateien schnell in Exchange Online-Postfächer in Ihrer Office 365-Organisation zu importieren. Es gibt zwei Möglichkeiten zum Importieren von PST-Dateien in Office 365:
   
- **Netzwerk Upload** ![Cloud Upload](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) : Hochladen der PST-Dateien über das Netzwerk an einen temporären Azure-Speicherort in der Microsoft-Cloud. Anschließend verwenden Sie den Office 365-Import Dienst, um die PST-Daten in Postfächer in Ihrer Office 365-Organisation zu importieren. 

- **Laufwerk Versand** ![Festplatte](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) : Kopieren Sie die PST-Dateien auf eine mit BitLocker verschlüsselte Festplatte, und senden Sie dann das Laufwerk physisch an Microsoft. Wenn Microsoft die Festplatte empfängt, werden die Daten vom Rechenzentrumsmitarbeiter an einen temporären Azure-Speicherort in der Microsoft-Cloud hochgeladen. Anschließend verwenden Sie den Office 365-Import Dienst, um die Daten in Postfächer in Ihrer Office 365-Organisation zu importieren.

## <a name="step-by-step-instructions"></a>Schrittweise Anleitungen
  
In einem der folgenden Themen finden Sie detaillierte schrittweise Anweisungen zum Massenimportieren der PST-Dateien Ihrer Organisation in Office 365. 
   
- [Verwenden des Netzwerk Uploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md)
- [Verwenden des Laufwerkversands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>Funktionsweise des Importierens von PST-Dateien

Hier sehen Sie eine Abbildung und eine Beschreibung des vollständigen PST-Importvorgangs. Die Abbildung zeigt den primären Workflow und die Unterschiede zwischen dem Netzwerk Upload und den Laufwerk Versandmethoden.
  
![Workflow des PST-Importvorgangs](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **Laden Sie die PST-Importtools und den Schlüssel zum privaten Azure-Speicherort herunter** – der erste Schritt besteht darin, das Tool und die Zugriffstaste herunterzuladen, die zum Hochladen der PST-Dateien verwendet wird, oder Sie auf eine Festplatte zu kopieren. Sie erhalten diese auf der Seite " **importieren** " im Security _AMP_ Compliance Center. Der Schlüssel bietet Ihnen (oder im Fall des Laufwerk Versands) die erforderlichen Berechtigungen zum Hochladen von PST-Dateien an einen privaten und sicheren Azure-Speicherort. Diese Zugriffstaste ist eindeutig für Ihre Organisation und verhindert den unbefugten Zugriff auf Ihre PST-Dateien, nachdem Sie in die Microsoft-Cloud hochgeladen wurden. Beachten Sie, dass das Importieren von PST-Dateien in Office 365 für Ihre Organisation kein separates Azure-Abonnement erfordert. 
    
2. **Hochladen oder Kopieren der PST-Dateien** – der nächste Schritt hängt davon ab, ob Sie den Netzwerk Upload oder den Laufwerk Versand zum Importieren von PST-Dateien verwenden. In beiden Fällen verwenden Sie das Tool und den Secure Storage-Schlüssel, den Sie im vorherigen Schritt abgerufen haben.
    
    - **Netzwerk Upload** Das Tool AzCopy. exe (in Schritt 1 heruntergeladen) wird zum Hochladen und Speichern Ihrer PST-Dateien an einem Azure-Speicherort in der Microsoft-Cloud verwendet. Beachten Sie, dass sich der Azure-Speicherort, an den Sie Ihre PST-Dateien hochladen, im selben regionalen Microsoft-Datencenter befindet, in dem sich Ihre Office 365-Organisation befindet. 
    
      Die PST-Dateien, die Sie in Office 365 importieren möchten, müssen sich in Ihrer Organisation auf einem Dateifreigabe-oder Dateiserver befinden.
    
    - **Laufwerk Versand** Das Tool "Waimportexport. exe (in Schritt 1 heruntergeladen) wird zum Kopieren der PST-Dateien auf die Festplatte verwendet. Dieses Tool verschlüsselt die Festplatte mit BitLocker und kopiert dann das PST auf die Festplatte. Wie bei Netzwerk Upload müssen sich die PST-Dateien, die Sie auf die Festplatte kopieren möchten, auf einem Dateifreigabe-oder Dateiserver in Ihrer Organisation befinden.
    
3. **Erstellen einer PST-Import Zuordnungsdatei** – nachdem die PST-Dateien in den Azure-Speicherort hochgeladen oder auf eine Festplatte kopiert wurden, wird im nächsten Schritt eine CSV-Datei (Comma Separated Value) erstellt, die angibt, in welchen Benutzerpostfächern die PST-Dateien importiert werden sollen (a ND eine PST-Datei kann in das primäre Postfach eines Benutzers oder in sein Archivpostfach importiert werden). Der Office 365-Import Dienst verwendet die Informationen, um die PST-Dateien zu importieren. 
    
4. **Erstellen eines PST-importauftrags** – im nächsten Schritt erstellen Sie auf der Seite " **importieren** " im Security _AMP_ Compliance Center einen PST-Importauftrag und übermitteln die im vorherigen Schritt erstellte PST-Import Zuordnungsdatei. Für Netzwerk Upload (da die PST-Dateien in Azure hochgeladen wurden) analysiert Office 365 die Daten in den PST-Dateien und gibt Ihnen dann die Möglichkeit, Filter festzulegen, die Steuern, welche Daten tatsächlich in die in der PST-Import Zuordnungsdatei angegebenen Postfächer importiert werden. 
    
    Bei Laufwerk Versand werden an dieser Stelle im Prozess einige zusätzliche Schritte ausgeführt.
    
    - Sie senden die Festplatte physisch an ein Microsoft-Datencenter (die Versandadresse des Microsoft-Datencenters wird angezeigt, wenn der Importauftrag erstellt wird).
    
    - Wenn Microsoft die Festplatte empfängt, lädt das Personal des Rechenzentrums die PST-Dateien auf der Festplatte an den Azure-Speicherort für Ihre Organisation hoch. Wie bereits erläutert, werden Ihre PST-Dateien an einen Azure-Speicherort hochgeladen, der sich im selben regionalen Microsoft-Datencenter befindet, in dem sich Ihre Office 365-Organisation befindet.
    
      > [!NOTE]
      > Die PST-Dateien auf der Festplatte werden innerhalb von 7 bis 10 Arbeitstagen nach Azure hochgeladen, nachdem Microsoft die Festplatte erhalten hat. 
  
      Wie beim Netzwerk-Upload analysiert Office 365 dann die Daten in den PST-Dateien und bietet Ihnen die Möglichkeit, Filter festzulegen, die Steuern, welche Daten tatsächlich in die in der PST-Import Zuordnungsdatei angegebenen Postfächer importiert werden.
    
    - Microsoft sendet die Festplatte an Sie zurück. 
    
5. **Filtern der PST-Daten, die in Postfächer importiert** werden – nachdem der Importauftrag erstellt wurde (und nachdem die PST-Dateien von einem Laufwerk Versandauftrag in den Azure-Speicherort hochgeladen wurden), analysiert Office 365 die Daten in den PST-Dateien (sicher und zuverlässig) durch Identifizieren des Alters der Elemente und der verschiedenen Nachrichtentypen, die in den PST-Dateien enthalten sind. Wenn die Analyse abgeschlossen ist und die Daten zum Importieren bereit sind, haben Sie die Möglichkeit, alle in den PST-Dateien enthaltenen Daten zu importieren, oder Sie können die importierten Daten trimmen, indem Sie Filter festlegen, die Steuern, welche Daten importiert werden. 
    
6. **Starten des PST-importauftrags** – nachdem der Importauftrag gestartet wurde, verwendet Office 365 die Informationen in der PST-Import Zuordnungsdatei, um die PST-Dateien aus dem Azure-Speicher Speicherort in Benutzerpostfächer zu importieren. Status Informationen zum Importauftrag (einschließlich Informationen zu jeder importierten PST-Datei) werden auf der Seite **importieren** im Security _AMP_ Compliance Center angezeigt. Wenn der Importauftrag abgeschlossen ist, wird der Status für den Auftrag auf **abgeschlossen**festgelegt.
  
## <a name="why-import-email-data-to-office-365"></a>Gründe für das Importieren von e-Mail-Daten in Office 365

- Das Importieren von PST-Dateien in Benutzerpostfächer ist eine Möglichkeit, die e-Mails Ihrer Organisation zu Office 365 zu migrieren.
    
- Mithilfe der [intelligenten Import](filter-data-when-importing-pst-files.md) Funktion können Sie die Elemente in PST-Dateien filtern, die tatsächlich in die Zielpostfächer importiert werden. Auf diese Weise können Sie die importierten Daten trimmen, indem Sie Filter festlegen, die Steuern, welche Daten importiert werden. 
    
- Durch das Importieren von e-Mail-Daten in Office 365 können Sie die Compliance-Anforderungen Ihrer Organisation erfüllen, indem Sie Folgendes zulassen:
    
  - Aktivieren Sie [Archivpostfächer](enable-archive-mailboxes.md) und [unbegrenzte Archivierung](unlimited-archiving.md) , um Benutzern zusätzlichen Speicherplatz für Postfächer bereitzustellen. 
    
  - Aufbewahrung von Post [](https://go.microsoft.com/fwlink/?linkid=841243) Fächern für das Aufbewahren von Inhalten 
    
  - Verwenden Sie das [Inhaltssuche-Tool](content-search.md) , um nach Postfachinhalten zu suchen. 
    
  - Verwenden von [eDiscovery-Fällen](ediscovery-cases.md) zum Verwalten von rechtlichen Untersuchungen in Ihrer Organisation 
    
  - Verwenden Sie [Aufbewahrungsrichtlinien](retention-policies.md) im Security _AMP_ Compliance Center, um zu steuern, wie lange Postfachinhalte aufbewahrt werden, und dann nach Ablauf des Aufbewahrungszeitraums Inhalte zu löschen. 
    
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
  
Sie müssen die Rolle "Postfachimport-export" in Exchange Online zuweisen, um PST-Dateien in Office 365-Postfächer zu importieren. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Darüber hinaus muss eine der folgenden Anforderungen erfüllt sein, um Importaufträge im Security & Compliance Center zu erstellen:
  
- Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Oder
    
- Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange Online, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die erforderlichen Mindestberechtigungen zum Importieren von PST-Dateien die Rollen Mailbox Import Export und e-Mail-Empfänger der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
 **Wo ist der Netzwerk Upload verfügbar?**
  
Network upload is currently available in the United States, Canada, Brazil, the United Kingdom, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Network upload will be available in more regions soon.
  
 **What is the pricing for importing PST files by using network upload?**
  
Using network upload to import PST files is free.
  
Dies hat auch zur Folge, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag im Microsoft 365 Admin Center angezeigt werden. Auch wenn ein Importauftrag möglicherweise noch auf der Seite **Import Data to Office 365** aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **What version of the PST file format is supported for importing to Office 365?**
  
There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. Dateien, die das ANSI-PST-Dateiformat verwenden, beispielsweise für Sprachen, die einen Doppelbyte-Zeichensatz (DBCS) verwenden, können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 4 bei [Verwendung des Netzwerk Uploads zum Importieren von PST-Dateien in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=823074).
  
Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.
  
 **Nachdem ich meine PST-Dateien in den Azure-Speicherbereich hochgeladen habe, wie lange werden Sie in Azure aufbewahrt, bevor Sie gelöscht werden?**
  
Wenn Sie die Netzwerk-Upload-Methode zum Importieren von PST-Dateien verwenden, laden Sie Sie in einen Azure-BLOB-Container mit dem Namen **ingestiondata**hoch. Wenn auf der Seite " **importieren** " im Security _AMP_ Compliance Center keine Importaufträge ausgeführt werden), werden alle PST-Dateien im **ingestiondata** -Container in Azure 30 Tage nach dem letzten Importauftrag im Sicherheits-& gelöscht. Compliance Center. Dies erfordert auch, dass Sie einen neuen Importauftrag im Security & Compliance Center (beschrieben in Schritt 5 in den Anweisungen zum Netzwerk Upload) innerhalb von 30 Tagen nach dem Hochladen von PST-Dateien in Azure erstellen müssen. 
  
Dies hat auch zur Folge, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag im Security & Compliance Center angezeigt werden. Auch wenn auf der Seite " **importieren** " im Security _AMP_ Compliance Center möglicherweise noch ein Importauftrag aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **Wie lange dauert es, bis eine PST-Datei in ein Postfach importiert wird?**
  
It depends on the capacity of your network, but it typically takes several hours for each terabyte (TB) of data to be uploaded to the Azure storage area for your organization. Nachdem die PST-Dateien in den Azure-Speicherbereich kopiert wurden, wird eine PST-Datei mit einer Rate von mindestens 24 GB pro Tag in ein Office 365-Postfach importiert. Wenn diese Rate Ihren Anforderungen nicht entspricht, können Sie andere Methoden für die Migration von e-Mail-Daten zu Office 365 berücksichtigen. Weitere Informationen finden Sie unter [Methoden zum Migrieren von mehreren E-Mail-Konten zu Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Wenn mehrere PST-Dateien in dasselbe Postfach importiert werden, werden diese gleichzeitig importiert.
  
 **Is there a message size limit when importing PST files?**
  
Ja. Wenn eine PST-Datei ein Postfachelement enthält, das größer als 150 MB ist, wird das Element während des Importvorgangs übersprungen.
  
 **Sind Nachrichteneigenschaften, beispielsweise wenn die Nachricht gesendet oder empfangen wurde, die Liste der Empfänger und andere Eigenschaften, die beim Importieren von PST-Dateien in ein Office 365-Postfach aufbewahrt werden?**
  
Ja. Die ursprünglichen Nachrichten Metadaten werden während des Importvorgangs nicht geändert.
  
 **Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**
  
Yes. You can't import a PST file that has 300 or more levels of nested folders.
  
 **Can I use network upload to import PST files to an inactive mailbox in Office 365?**
  
Yes, this capability is now available. 
  
 **Can I use network upload to import PST files to an online archive mailbox in an Exchange hybrid deployment?**
  
Yes, this capability is now available. 
  
 **Kann ich den Netzwerk Upload zum Importieren von PST-Dateien in öffentliche Ordner in Exchange Online verwenden?**
  
Nein, Sie können PST-Dateien nicht in öffentliche Ordner importieren.
  
### <a name="using-drive-shipping-to-import-pst-files"></a>Verwenden des Laufwerk Versands zum Importieren von PST-Dateien

 **Welche Berechtigungen sind erforderlich, um Importaufträge im Office 365-Import Dienst zu erstellen?**
  
Sie müssen der Postfachimport-export Rolle zugewiesen sein, um PST-Dateien in Office 365-Postfächer zu importieren. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Darüber hinaus muss eine der folgenden Anforderungen erfüllt sein, um Importaufträge im Security & Compliance Center zu erstellen:
  
- Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Oder
    
- Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange Online, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die erforderlichen Mindestberechtigungen zum Importieren von PST-Dateien die Rollen Mailbox Import Export und e-Mail-Empfänger der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
 **Wo ist der Laufwerk Versand verfügbar?**
  
Der Laufwerk Versand ist derzeit in den USA, Kanada, Brasilien, Großbritannien, Europa, Indien, Ostasien, Südostasien, Japan, Südkorea und Australien verfügbar. Drive shipping will be available in more regions soon.
  
 **What commercial licensing agreements support drive shipping?**
  
Laufwerk Versand zum Importieren von PST-Dateien in Office 365 ist über einen Microsoft Enterprise Agreement (EA) verfügbar. Der Laufwerk Versand ist nicht über einen Microsoft-Produkt-und-Dienstvertrag (MPSA) verfügbar.
  
 **Wie hoch sind die Preise für die Verwendung des Laufwerk Versands zum Importieren von PST-Dateien in Office 365?**
  
The cost to use drive shipping to import PST files to Office 365 mailboxes is $2 USD per GB of data. For example, if you ship a hard drive that contains 1,000 GB (1 TB) of PST files, the cost is $2,000 USD. You can work with a partner to pay the import fee. Informationen zum Suchen eines Partners finden Sie unter [Suchen Ihres Office 365-Partners oder](https://go.microsoft.com/fwlink/p/?LinkId=785197)-Händlers.
  
 **What kind of hard drives are supported for drive shipping?**
  
Nur 2,5 Zoll-Solid-State-Laufwerke (SSDs) oder 2,5-oder 3,5-Zoll-SATA II/III-Festplatten werden für die Verwendung mit dem Office 365-Import Dienst unterstützt. You can use hard drives up to 10 TB. Bei Import Aufträgen wird nur das erste Datenvolume auf der Festplatte verarbeitet. The data volume must be formatted with NTFS. Wenn Sie Daten auf eine Festplatte kopieren, können Sie Sie direkt mit einem 2,5-Zoll-SSD oder 2,5-oder 3,5-Zoll-SATA II/III-Stecker anhängen, oder Sie können Sie extern über einen externen 2,5-Zoll-SSD oder 2,5-oder 3,5-Zoll-SATA II/III-USB-Adapter anschließen.
  
> [!IMPORTANT]
> Externe Festplatten, die mit einem integrierten USB-Adapter geliefert werden, werden vom Office 365-Import Dienst nicht unterstützt. Additionally, the disk inside the casing of an external hard drive can't be used. Please don't ship external hard drives. 
  
 **How many hard drives can I ship for a single import job?**
  
You can ship a maximum of 10 hard drives for a single import job.
  
 **After I ship my hard drive, how long does it take to get to the Microsoft data center?**
  
That depends on a few things, such as your proximity to the Microsoft data center and what kind of shipping option you used to ship your hard drive (such as, next-day delivery, two-day delivery, or ground-delivery). With most shippers, you can use the tracking number to track the status of your delivery.
  
 **Wie lange dauert es, bis meine PST-Dateien in Azure hochgeladen werden, nachdem meine Festplatte im Microsoft-Datencenter eingegangen ist?**
  
Nachdem die Festplatte im Microsoft-Datencenter eingegangen ist, dauert es zwischen 7 und 10 Werktage, die PST-Dateien in den Microsoft Azure-Speicherbereich für Ihre Organisation hochzuladen. Die PST `ingestiondata`-Dateien werden in einen Azure-BLOB-Container hochgeladen. 
  
 **Wie lange dauert es, bis eine PST-Datei in ein Postfach importiert wird?**
  
Nachdem die PST-Dateien in den Azure-Speicherbereich hochgeladen wurden, analysiert Office 365 die Daten in den PST-Dateien (auf sichere und sichere Weise), um das Alter der Elemente und die verschiedenen Nachrichtentypen in den PST-Dateien zu identifizieren. Wenn diese Analyse abgeschlossen ist, haben Sie die Möglichkeit, alle Daten in den PST-Dateien zu importieren oder Filter festzulegen, die Steuern, welche Daten importiert werden. Nachdem Sie den Importauftrag gestartet haben, wird eine PST-Datei mit einer Rate von mindestens 24 GB pro Tag in ein Office 365-Postfach importiert. Wenn diese Rate Ihren Anforderungen nicht entspricht, können Sie andere Methoden zum Importieren von e-Mail-Daten in Office 365 berücksichtigen. Weitere Informationen finden Sie unter [Methoden zum Migrieren von mehreren E-Mail-Konten zu Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Wenn mehrere PST-Dateien in dasselbe Postfach importiert werden, werden diese gleichzeitig importiert.
  
 **Nachdem Microsoft meine PST-Dateien in Azure hochgeladen hat, wie lange werden Sie in Azure aufbewahrt, bevor Sie gelöscht werden?**
  
Alle PST-Dateien am Azure-Speicherort für Ihre Organisation (im BLOB-Container `ingestiondata`namens) werden 30 Tage nach dem letzten Importauftrag auf der Seite " **importieren** " im Security & Compliance Center gelöscht. 
  
Dies hat auch zur Folge, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag im Security & Compliance Center angezeigt werden. Auch wenn auf der Seite " **importieren** " im Security _AMP_ Compliance Center möglicherweise noch ein Importauftrag aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **What version of the PST file format is supported for importing to Office 365?**
  
There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. Dateien, die das ANSI-PST-Dateiformat verwenden, beispielsweise für Sprachen, die einen Doppelbyte-Zeichensatz (DBCS) verwenden, können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 3: [Verwenden des Laufwerk Versands zum Importieren Ihrer Organisations-PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.
  
 **Is there a message size limit when importing PST files?**
  
Ja. Wenn eine PST-Datei ein Postfachelement enthält, das größer als 150 MB ist, wird das Element während des Importvorgangs übersprungen.
  
 **Sind Nachrichteneigenschaften, beispielsweise wenn die Nachricht gesendet oder empfangen wurde, die Liste der Empfänger und andere Eigenschaften, die beim Importieren von PST-Dateien in ein Office 365-Postfach aufbewahrt werden?**
  
Ja. Die ursprünglichen Nachrichten Metadaten werden während des Importvorgangs nicht geändert.
  
 **Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**
  
Yes. You can't import a PST file that has 300 or more levels of nested folders.
  
 **Can I use drive shipping to import PST files to an inactive mailbox in Office 365?**
  
Yes, this capability is now available.
  
 **Can I use drive shipping to import PST files to an online archive mailbox in an Exchange hybrid deployment?**
  
Yes, this capability is now available. 
  
 **Kann ich den Laufwerk Versand verwenden, um PST-Dateien in öffentliche Ordner in Exchange Online zu importieren?**
  
Nein, Sie können PST-Dateien nicht in öffentliche Ordner importieren.
  
 **Can Microsoft wipe my hard drive before they ship it back to me?**
  
No, Microsoft can't wipe hard drives before shipping them back to customers. Hard drives are returned to you in the same state they were in when they were received by Microsoft.
  
 **Kann Microsoft meine Festplatte Schreddern, anstatt Sie an mich zurückzustellen?**
  
No, Microsoft can't destroy your hard drive. Hard drives are returned to you in the same state they were in when they were received by Microsoft.
  
 **Welche Kurierdienste werden für den Rückversand unterstützt?**
  
If you're a customer in the United States or Europe, Microsoft uses FedEx to return your hard drive. For all other regions, Microsoft uses DHL.
  
 **Was sind die Versandkosten?**
  
Return shipping costs vary, depending on your proximity to the Microsoft data center that you shipped your hard drive to. Microsoft will bill your FedEx or DHL account to return your hard drive. The cost of return shipping is your responsibility.
  
 **Kann ich einen benutzerdefinierten Kurierversand Dienst verwenden, beispielsweise FedEx Custom Shipping, um meine Festplatte an Microsoft zu senden?**
  
Ja.
  
 **If I have to ship my hard drive to another country, is there anything I need to do?**
  
The hard drive that you ship to Microsoft might have to cross international borders. If this is the case, you're responsible for ensuring that the hard drive and the data it contains are imported and/or exported in accordance with the applicable laws. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the specified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.
