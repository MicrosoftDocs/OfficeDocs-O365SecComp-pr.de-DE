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
ms.openlocfilehash: bef9c9e80f4f4c8261e9c44ba201a978937e2841
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296878"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a>HÄUFIG gestellte Fragen zum Importieren von PST-Dateien in Office 365

**Dieser Artikel richtet sich an Administratoren. Möchten Sie PST-Dateien in Ihr eigenes Postfach importieren? Weitere Informationen finden Sie unter [Importieren von e-Mails, Kontakten und Kalendern aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)**|
   
Hier finden Sie einige häufig gestellte Fragen zur Verwendung des Office 365-Import Diensts zum Massenimport von PST-Dateien in Office 365-Postfächer. Weitere Informationen zum Importieren von PST-Dateien finden Sie unter [Übersicht über das Importieren von PST-Dateien in Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84).
  
## <a name="using-network-upload-to-import-pst-files"></a>Verwenden des Netzwerk Uploads zum Importieren von PST-Dateien

Schrittweise Anleitungen finden Sie unter [Verwenden des Netzwerk Uploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md).
  
 **Welche Berechtigungen sind erforderlich, um Importaufträge im Office 365-Import Dienst zu erstellen?**
  
Sie müssen die Rolle "Postfachimport-export" in Exchange Online zuweisen, um PST-Dateien in Office 365-Postfächer zu importieren. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. Sie können die Rolle "Post Fach Import-Export" zur Rollengruppe "Organisationsverwaltung" hinzufügen. Sie können auch eine neue Rollengruppe erstellen, die Export Rolle Post Fach Import zuweisen und sich selbst oder andere Benutzer als Mitglied hinzufügen. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Darüber hinaus muss eine der folgenden Anforderungen erfüllt sein, um &amp; Importaufträge im Office 365 Security Compliance Center zu erstellen:
  
- Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden. Diese Rolle wird standardmäßig den Rollengruppen Organisationsverwaltung und Empfängerverwaltung zugewiesen.
    
    Oder
    
- Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange Online, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die erforderlichen Mindestberechtigungen zum Importieren von PST-Dateien die Rollen Mailbox Import Export und e-Mail-Empfänger der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
 **Wo ist der Netzwerk Upload verfügbar?**
  
Der Netzwerk Upload ist derzeit in den USA, Kanada, Brasilien, Großbritannien, Frankreich, Europa, Indien, Ostasien, Südostasien, Japan, Südkorea und Australien verfügbar. Der Netzwerk Upload steht in Kürze in weiteren Regionen zur Verfügung.
  
 **Wie hoch sind die Preise für den Import von PST-Dateien mithilfe des Netzwerk Uploads?**
  
Die Verwendung des Netzwerk Uploads zum Importieren von PST-Dateien ist kostenlos.
  
Dies hat auch zur Folge, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag im Office 365 Admin Center angezeigt werden. Auch wenn ein Importauftrag möglicherweise noch auf der Seite **Import Data to Office 365** aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **Welche Version des PST-Dateiformats wird für den Import in Office 365 unterstützt?**
  
Es gibt zwei Versionen des PST-Dateiformats: ANSI und Unicode. Es wird empfohlen, Dateien zu importieren, die das Unicode-PST-Dateiformat verwenden. Dateien, die das ANSI-PST-Dateiformat verwenden, beispielsweise für Sprachen, die einen Doppelbyte-Zeichensatz (DBCS) verwenden, können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 4 bei [Verwendung des Netzwerk Uploads zum Importieren der PST-Dateien Ihrer Organisation in Office 365](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file).
  
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
  
## <a name="using-drive-shipping-to-import-pst-files"></a>Verwenden des Laufwerk Versands zum Importieren von PST-Dateien

Schrittweise Anleitungen finden Sie unter [Verwenden des Laufwerk Versands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md).
  
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
  
Nachdem die Festplatte im Microsoft-Datencenter eingegangen ist, dauert es zwischen 7 und 10 Werktage, die PST-Dateien in den Microsoft Azure-Speicherbereich für Ihre Organisation hochzuladen. Die PST-Dateien werden in einen Azure-BLOB-Container mit dem Namen **ingestiondata**hochgeladen. 
  
 **Wie lange dauert es, bis eine PST-Datei in ein Postfach importiert wird?**
  
Nachdem die PST-Dateien in den Azure-Speicherbereich hochgeladen wurden, analysiert Office 365 die Daten in den PST-Dateien (auf sichere und sichere Weise), um das Alter der Elemente und die verschiedenen Nachrichtentypen in den PST-Dateien zu identifizieren. Wenn diese Analyse abgeschlossen ist, haben Sie die Möglichkeit, alle Daten in den PST-Dateien zu importieren oder Filter festzulegen, die Steuern, welche Daten importiert werden. Nachdem Sie den Importauftrag gestartet haben, wird eine PST-Datei mit einer Rate von mindestens 24 GB pro Tag in ein Office 365-Postfach importiert. Wenn diese Rate Ihren Anforderungen nicht entspricht, können Sie andere Methoden zum Importieren von e-Mail-Daten in Office 365 berücksichtigen. Weitere Informationen finden Sie unter [Möglichkeiten zum Migrieren mehrerer e-Mail-Konten zu Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Wenn unterschiedliche PST-Dateien in unterschiedliche Zielpostfächer importiert werden, erfolgt der Importprozess parallel; in anderen Worten, jedes PST/Mailbox-Paar wird gleichzeitig importiert. Wenn mehrere PST-Dateien in dasselbe Postfach importiert werden, werden diese gleichzeitig importiert.
  
 **Nachdem Microsoft meine PST-Dateien in Azure hochgeladen hat, wie lange werden Sie in Azure aufbewahrt, bevor Sie gelöscht werden?**
  
Alle PST-Dateien am Azure-Speicherort für Ihre Organisation (im BLOB-Container mit dem Namen **ingestiondata** ) werden 30 Tage nach dem letzten Importauftrag auf der Seite " **importieren** " im Security &amp; Compliance Center gelöscht. 
  
Dies führt auch dazu, dass nach dem Löschen von PST-Dateien aus dem Azure-Speicherbereich diese nicht mehr in der Liste der Dateien für einen abgeschlossenen Importauftrag &amp; im Security Compliance Center angezeigt werden. Auch wenn auf der Seite " **importieren** " im Security &amp; Compliance Center möglicherweise noch ein Importauftrag aufgeführt wird, ist die Liste der PST-Dateien möglicherweise leer, wenn Sie die Details älterer Importaufträge anzeigen. 
  
 **Welche Version des PST-Dateiformats wird für den Import in Office 365 unterstützt?**
  
Es gibt zwei Versionen des PST-Dateiformats: ANSI und Unicode. Es wird empfohlen, Dateien zu importieren, die das Unicode-PST-Dateiformat verwenden. Dateien, die das ANSI-PST-Dateiformat verwenden, beispielsweise für Sprachen, die einen Doppelbyte-Zeichensatz (DBCS) verwenden, können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 3 unter [Verwenden des Laufwerk Versands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
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
