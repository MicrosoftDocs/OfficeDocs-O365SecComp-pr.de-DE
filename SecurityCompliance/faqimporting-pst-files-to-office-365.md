---
title: HÄUFIG gestellte Fragen zum Importieren von PST-Dateien in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 2fe71b05-f5a2-4182-ade7-4dc5cabdfd51
description: 'Häufig gestellte Fragen für Administratoren zur Verwendung des Office 365-Import Diensts zum Importieren Ihrer Organizaiton-PST-Dateien in Office 365-Postfächer. '
ms.openlocfilehash: 69767353a574336351b01fdc42a9c6117c5c31ed
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255433"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a>HÄUFIG gestellte Fragen zum Importieren von PST-Dateien in Office 365

**Dieser Artikel richtet sich an Administratoren. Möchten Sie PST-Dateien in Ihr eigenes Postfach importieren? Weitere Informationen finden Sie unter [Importieren von e-Mails, Kontakten und Kalendern aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)**|
   
Hier finden Sie einige häufig gestellte Fragen zur Verwendung des Office 365-Import Diensts zum Massenimport von PST-Dateien in Office 365-Postfächer. Weitere Informationen zum Importieren von PST-Dateien finden Sie unter [Übersicht über das Importieren von PST-Dateien in Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84).
  
## <a name="using-network-upload-to-import-pst-files"></a>Verwenden des Netzwerk Uploads zum Importieren von PST-Dateien

Schrittweise Anleitungen finden Sie unter [Verwenden des Netzwerk Uploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md).
  
 **Welche Berechtigungen sind erforderlich, um Importaufträge im Office 365-Import Dienst zu erstellen?**
  
Sie müssen die Rolle "Postfachimport-export" in Exchange Online zuweisen, um PST-Dateien in Office 365-Postfächer zu importieren. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Darüber hinaus muss eine der folgenden Anforderungen erfüllt sein, um Importaufträge im Security & Compliance Center zu erstellen:
  
- Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Oder
    
- Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange Online, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die erforderlichen Mindestberechtigungen zum Importieren von PST-Dateien die Rollen Mailbox Import Export und e-Mail-Empfänger der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
 **Wo ist der Netzwerk Upload verfügbar?**
  
Der Netzwerk Upload ist derzeit in den USA, Kanada, Brasilien, Großbritannien, Frankreich, Europa, Indien, Ostasien, Südostasien, Japan, Südkorea und Australien verfügbar. Network upload will be available in more regions soon.
  
 **What is the pricing for importing PST files by using network upload?**
  
Using network upload to import PST files is free.
  
Dies hat auch zur Folge, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag im Microsoft 365 Admin Center angezeigt werden. Auch wenn ein Importauftrag möglicherweise noch auf der Seite **Import Data to Office 365** aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **What version of the PST file format is supported for importing to Office 365?**
  
There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. Dateien, die das ANSI-PST-Dateiformat verwenden, beispielsweise für Sprachen, die einen Doppelbyte-Zeichensatz (DBCS) verwenden, können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 4 bei [Verwendung des Netzwerk Uploads zum Importieren der PST-Dateien Ihrer Organisation in Office 365](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file).
  
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
  
## <a name="using-drive-shipping-to-import-pst-files"></a>Verwenden des Laufwerk Versands zum Importieren von PST-Dateien

Schrittweise Anleitungen finden Sie unter [Verwenden des Laufwerk Versands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md).
  
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
  
Nachdem die Festplatte im Microsoft-Datencenter eingegangen ist, dauert es zwischen 7 und 10 Werktage, die PST-Dateien in den Microsoft Azure-Speicherbereich für Ihre Organisation hochzuladen. Die PST-Dateien werden in einen Azure-BLOB-Container mit dem Namen **ingestiondata**hochgeladen. 
  
 **Wie lange dauert es, bis eine PST-Datei in ein Postfach importiert wird?**
  
Nachdem die PST-Dateien in den Azure-Speicherbereich hochgeladen wurden, analysiert Office 365 die Daten in den PST-Dateien (auf sichere und sichere Weise), um das Alter der Elemente und die verschiedenen Nachrichtentypen in den PST-Dateien zu identifizieren. Wenn diese Analyse abgeschlossen ist, haben Sie die Möglichkeit, alle Daten in den PST-Dateien zu importieren oder Filter festzulegen, die Steuern, welche Daten importiert werden. Nachdem Sie den Importauftrag gestartet haben, wird eine PST-Datei mit einer Rate von mindestens 24 GB pro Tag in ein Office 365-Postfach importiert. Wenn diese Rate Ihren Anforderungen nicht entspricht, können Sie andere Methoden zum Importieren von e-Mail-Daten in Office 365 berücksichtigen. Weitere Informationen finden Sie unter [Methoden zum Migrieren von mehreren E-Mail-Konten zu Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Wenn mehrere PST-Dateien in dasselbe Postfach importiert werden, werden diese gleichzeitig importiert.
  
 **Nachdem Microsoft meine PST-Dateien in Azure hochgeladen hat, wie lange werden Sie in Azure aufbewahrt, bevor Sie gelöscht werden?**
  
Alle PST-Dateien am Azure-Speicherort für Ihre Organisation (im BLOB-Container mit dem Namen **ingestiondata** ) werden 30 Tage nach dem letzten Importauftrag auf der Seite " **importieren** " im Security & Compliance Center gelöscht. 
  
Dies hat auch zur Folge, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag im Security & Compliance Center angezeigt werden. Auch wenn auf der Seite " **importieren** " im Security _AMP_ Compliance Center möglicherweise noch ein Importauftrag aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **What version of the PST file format is supported for importing to Office 365?**
  
There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. Dateien, die das ANSI-PST-Dateiformat verwenden, beispielsweise für Sprachen, die einen Doppelbyte-Zeichensatz (DBCS) verwenden, können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 3 unter [Verwenden des Laufwerk Versands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
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
