---
title: Häufig gestellte Fragen zum Importieren von PST-Dateien in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 2fe71b05-f5a2-4182-ade7-4dc5cabdfd51
description: 'Häufig gestellte Fragen für Administratoren zur Verwendung von Office 365 importieren-Dienst zum Erstellen vorhanden ist, wird Ihre von PST-Dateien in Office 365-Postfächer zu importieren. '
ms.openlocfilehash: 35080106f92b38e944ba31f74d5564e65ba1f752
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530129"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a>Häufig gestellte Fragen zum Importieren von PST-Dateien in Office 365

**Dieser Artikel ist für Administratoren. Möchten Sie die PST-Dateien in Ihrem Postfach importieren? Finden Sie unter [Import e-Mail, Kontakte und Kalender aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)**|
   
Hier sind einige häufig gestellten Fragen zur Verwendung von Office 365 importieren-Dienst zum Massenimport-PST-Dateien in Office 365-Postfächer. Weitere Informationen zum Importieren von PST-Dateien finden Sie unter [Übersicht über das Importieren von PST-Dateien zu Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84).
  
## <a name="using-network-upload-to-import-pst-files"></a>Importieren von PST-Dateien mithilfe von Netzwerk-upload

Eine schrittweise Anleitung finden Sie unter [Verwendung Netzwerk zum Importieren von PST-Dateien zu Office 365 hochladen](use-network-upload-to-import-pst-files.md).
  
 **Welche Berechtigungen sind zum Erstellen von Importaufträge in der Office 365-Dienst importieren erforderlich?**
  
Sie müssen die Rolle Postfach importieren exportieren in Exchange Online zum Importieren von PST-Dateien in Office 365-Postfächer zugewiesen werden. Standardmäßig ist nicht dieser Rolle alle Rollengruppe in Exchange Online zugewiesen. Sie können die Rollengruppe "Organisationsverwaltung" Postfach Import/Export-Rolle hinzufügen. Oder Sie können eine neuen Rollengruppe erstellen, weisen Sie die Rolle Postfach Import/Export, und fügen Sie selbst oder andere Benutzer als Mitglied. Weitere Informationen finden Sie unter "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" in [Manage Role Gruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)Abschnitte.
  
Darüber hinaus Import erstellen Aufträge in der Office 365-Sicherheit &amp; Compliance Center, eine der folgenden muss true sein:
  
- Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zugewiesen werden. Standardmäßig wird diese Rolle der Organization Management und Recipient Management Rollen Gruppen zugewiesen.
    
    oder -
    
- Sie müssen ein globaler Administrator in Office 365-Organisation sein.
    
> [!TIP]
> Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange-Online, die speziell für das Importieren von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die Mindestebene von Berechtigungen, die zum Importieren von PST-Dateien erforderlich sind der neuen Rollengruppe die Rollen Postfach importieren exportieren und E-Mail-Empfänger, und fügen Sie Mitglieder. 
  
 **Wo ist die Netzwerk-Upload verfügbar?**
  
Netzwerk-Upload ist in den USA, Kanada, Brasilien, die Großbritannien, Europa, Indien, Ostasien, Südost Asien, Japan, Republik Korea und Australien derzeit verfügbar. Netzwerk-Upload Kürze Weitere Regionen verfügbar.
  
 **Was ist der Preisgestaltung für den Import von PST-Dateien mithilfe von Netzwerk-Upload?**
  
Netzwerk-Upload zum Importieren von PST-Dateien mit ist kostenlos.
  
Dies bedeutet auch, dass nach der PST-Dateien aus dem Bereich der Azure-Speicher gelöscht werden, sie nicht mehr in der Liste der Dateien für einen Auftrag abgeschlossene Import im Office 365 Administrationscenter angezeigt werden. Obwohl ein Importauftrag weiterhin auf der Seite **Importieren von Daten zu Office 365** aufgeführt sind, möglicherweise die Liste der PST-Dateien leer, wenn Sie die Details der älteren Importaufträge anzeigen. 
  
 **Welche Version von PST-Dateiformat unterstützt wird, für das Importieren in Office 365?**
  
Es gibt zwei Versionen des Dateiformats PST: ANSI und Unicode. Es wird empfohlen, Importieren von Dateien, die das Unicode-PST-Dateiformat verwenden. Jedoch Dateien, die das Dateiformat ANSI PST wie für Sprachen verwenden, die ein Double-Byte-Zeichen verwenden (DBCS) Sie können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 4 in [Verwendung Netzwerk hochladen, um Ihre Organisation PST-Dateien nach Office 365 zu importieren](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file).
  
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
  
## <a name="using-drive-shipping-to-import-pst-files"></a>Importieren von PST-Dateien mithilfe von Laufwerk des Protokollversands

Schrittweise Anweisungen finden Sie unter [Verwenden Sie zum Importieren von PST-Dateien zu Office 365 shipping Laufwerk](use-drive-shipping-to-import-pst-files-to-office-365.md).
  
 **Welche Berechtigungen sind zum Erstellen von Importaufträge in der Office 365-Dienst importieren erforderlich?**
  
Sie müssen die Rolle des Postfachs exportieren importieren zum Importieren von PST-Dateien in Office 365-Postfächer zugewiesen werden. Standardmäßig ist nicht dieser Rolle alle Rollengruppe in Exchange Online zugewiesen. Sie können die Rollengruppe "Organisationsverwaltung" Postfach Import/Export-Rolle hinzufügen. Oder Sie können eine neuen Rollengruppe erstellen, weisen Sie die Rolle Postfach Import/Export, und fügen Sie selbst oder andere Benutzer als Mitglied. Weitere Informationen finden Sie unter "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" in [Manage Role Gruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)Abschnitte.
  
Darüber hinaus Import erstellen Aufträge in der Office 365-Sicherheit &amp; Compliance Center, eine der folgenden muss true sein:
  
- Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zugewiesen werden. Standardmäßig wird diese Rolle der Organization Management und Recipient Management Rollen Gruppen zugewiesen.
    
    oder -
    
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
  
Nachdem die Festplatte in der Microsoft-Rechenzentrum empfangen wurde, dauert es zwischen 7 bis 10 Arbeitstage in Bereich für die Microsoft Azure-Speicherung für Ihre Organisation die PST-Dateien hochladen. Die PST-Dateien werden in Azure BLOB-Container mit dem Namen **Ingestiondata**hochgeladen werden. 
  
 **Wie lange dauert es eine PST-Datei an ein Postfach importieren?**
  
Nachdem die PST-Dateien in den Bereich der Azure-Speicher hochgeladen werden, analysiert Office 365 die Daten in PST-Dateien (auf sichere Weise), um das Alter der Elemente und die verschiedenen Nachrichtentypen in PST-Dateien enthalten zu ermitteln. Wenn diese Analyse abgeschlossen ist, müssen Sie die Option aus, um alle Daten in die PST-Dateien zu importieren oder Set Filter an, die steuern, welche Daten importierten dient zum Abrufen. Nachdem Sie den Importauftrag gestartet haben, wird eine PST-Datei in ein Office 365-Postfach mit einer Rate von mindestens 24 GB pro Tag importiert. Wenn diese Rate nicht Ihren Anforderungen entsprechen, sollten Sie andere Methoden zum Importieren von e-Mail-Daten in Office 365. Weitere Informationen finden Sie unter [Möglichkeiten, um mehrere e-Mail-Konten zu Office 365 zu migrieren](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Wenn unterschiedliche PST-Dateien auf anderes Ziel Postfächer importiert werden, tritt der Importvorgang parallel. Anders ausgedrückt, wird jedes Paar PST-Postfach gleichzeitig importiert. Dienstanbieter entscheidet auch, wenn mehrere PST-Dateien in demselben Postfach importiert werden, werden sie gleichzeitig importiert werden.
  
 **Nachdem Microsoft Meine PST-Dateien in Azure hochgeladen, wie lange bleiben sie in Azure, bevor sie gelöscht werden?**
  
Alle PST-Dateien in den Speicherort der Azure-Speicher für Ihre Organisation (in BLOB-Container mit dem Namen **Ingestiondata** ), werden nach der neueste Importauftrag erstellt wurde, auf der Seite **Importieren** in das Wertpapier 30 Tage gelöscht &amp; Compliance Center. 
  
Dies bedeutet auch, dass nach der PST-Dateien aus dem Bereich der Azure-Speicher gelöscht werden, sie nicht mehr in der Liste der Dateien für einen Auftrag abgeschlossene Import in das Wertpapier angezeigt werden &amp; Compliance Center. Obwohl ein Importauftrag weiterhin auf der Seite **Importieren** in das Wertpapier aufgeführt werden möglicherweise &amp; Compliance Center, die Liste der PST-Dateien möglicherweise leer sein, wenn Sie die Details der älteren Importaufträge anzeigen. 
  
 **Welche Version von PST-Dateiformat unterstützt wird, für das Importieren in Office 365?**
  
Es gibt zwei Versionen des Dateiformats PST: ANSI und Unicode. Es wird empfohlen, Importieren von Dateien, die das Unicode-PST-Dateiformat verwenden. Jedoch Dateien, die das Dateiformat ANSI PST wie für Sprachen verwenden, die ein Double-Byte-Zeichen verwenden (DBCS) Sie können auch in Office 365 importiert werden. Weitere Informationen zum Importieren von ANSI-PST-Dateien finden Sie unter Schritt 3 in [Verwenden Sie zum Importieren von PST-Dateien zu Office 365 shipping Laufwerk](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
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
