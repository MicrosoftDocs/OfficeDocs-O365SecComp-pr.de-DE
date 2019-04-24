---
title: Anwenden der Verwaltung von Informationsrechten (IRM) auf eine Liste oder Bibliothek
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1
ms.collection:
- M365-security-compliance
description: Sie können die Verwaltung von Informationsrechten (Information Rights Management, IRM) verwenden, um Dateien zu steuern und zu schützen, die aus Listen oder Bibliotheken heruntergeladen werden.
ms.openlocfilehash: ae07136cf128f167695f667cc8a149492287f498
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32244026"
---
# <a name="apply-information-rights-management-irm-to-a-list-or-library"></a>Anwenden der Verwaltung von Informationsrechten (IRM) auf eine Liste oder Bibliothek

Sie können die Verwaltung von Informationsrechten (Information Rights Management, IRM) verwenden, um Dateien zu steuern und zu schützen, die aus Listen oder Bibliotheken heruntergeladen werden.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Der Azure Rights Management Service (Azure RMS) von Azure Information Protection und die lokalen äquivalenten Active Directory-RechteverwaltungsDienste (AD RMS) unterstützen die Verwaltung von Informationsrechten für Websites. Es sind keine separaten oder zusätzlichen Installationen erforderlich.
    
- Bevor Sie IRM auf eine Liste oder Bibliothek anwenden, muss Sie zunächst von einem Administrator für Ihre Website aktiviert werden.
    
- Zum Anwenden von IRM auf eine Liste oder Bibliothek benötigen Sie Administratorberechtigungen für diese Liste oder Bibliothek.
    
- Wenn Sie SharePoint Online verwenden, können Benutzer Timeouts beim Herunterladen größerer IRM-geschützter Dateien erfahren. In diesem Fall wenden Sie den IRM-Schutz mithilfe Ihrer Office-Programme an, und speichern Sie größere Dateien in einer SharePoint-Bibliothek, die IRM nicht verwendet.
    
> [!NOTE]
> Wenn Sie SharePoint Server 2013 verwenden, muss ein Server Administrator auf allen Front-End-Webservern für jeden Dateityp, den die Personen in Ihrer Organisation mithilfe von IRM schützen möchten, die Schutzkomponenten installieren. 
  
## <a name="apply-irm-to-a-list-or-library"></a>Anwenden von IRM auf eine Liste oder Bibliothek
<a name="__toc256598179"> </a>

![Einstellungen für die Verwaltung von Informationsrechten](media/1b708102-9c90-42b0-b255-ef0e72d0be88.png)
  
1. Wechseln Sie zu der Liste oder Bibliothek, für die Sie IRM konfigurieren möchten.
    
2. Klicken Sie auf dem Menüband auf die Registerkarte **Bibliothek** , und klicken Sie dann auf **Bibliothekseinstellungen**. (Wenn Sie in einer Liste arbeiten, klicken Sie auf die Registerkarte **Liste** , und klicken Sie dann auf **Listeneinstellungen**).
    
    ![Schaltflächen für die SharePoint-BibliotheksEinstellungen im Menüband](media/cdf718fa-d792-40fc-8026-00c3b80b9e05.png)
  
3. Klicken Sie unter **Berechtigungen und Verwaltung**auf **Verwaltung von Informationsrechten**. Wenn der Link Information Rights Management nicht angezeigt wird, ist IRM möglicherweise nicht für Ihre Website aktiviert. Wenden Sie sich an den Server Administrator, um zu prüfen, ob IRM für Ihre Website aktiviert werden kann. Der Link zur Verwaltung von Informationsrechten wird nicht für Bildbibliotheken angezeigt.
    
4. Aktivieren Sie auf der Seite Einstellungen für die **Verwaltung von Informationsrechten** das Kontrollkästchen **Berechtigungen für Dokumente in dieser Bibliothek beim Herunterladen einschränken** , um eingeschränkte Berechtigungen für Dokumente anzuwenden, die aus dieser Liste oder Bibliothek heruntergeladen werden. 
    
5. Geben Sie im Feld **Titel der Berechtigungsrichtlinie erstellen** einen beschreibenden Namen für die Richtlinie ein, die Sie später verwenden können, um diese Richtlinie von anderen Richtlinien zu unterscheiden. Sie können beispielsweise " **Company Confidential** " eingeben, wenn Sie eine eingeschränkte Berechtigung für eine Liste oder Bibliothek anwenden, die vertrauliche Unternehmensdokumente enthalten soll. 
    
6. Geben Sie im Feld **Beschreibung einer Berechtigungsrichtlinie hinzufügen** eine Beschreibung ein, die Personen angezeigt wird, die diese Liste oder Bibliothek verwenden, um zu erläutern, wie Sie die Dokumente in dieser Liste oder Bibliothek behandeln sollen. Sie können beispielsweise **den Inhalt dieses Dokuments nur mit anderen Mitarbeitern besprechen** eingeben, wenn Sie den Zugriff auf die Informationen in diesen Dokumenten auf interne Mitarbeiter beschränken möchten. 
    
7. Wenn Sie zusätzliche Einschränkungen für die Dokumente in dieser Liste oder Bibliothek anwenden möchten, klicken Sie auf **Optionen anzeigen**, und führen Sie einen der folgenden Schritte aus:
    
|**Gehen Sie hierfür folgendermaßen vor:**|**Tun Sie Folgendes:**|
|:-----|:-----|
|Zulassen, dass Benutzer Dokumente aus dieser Liste oder Bibliothek drucken  <br/> |Aktivieren Sie das Kontrollkästchen **Viewer drucken zulassen** .  <br/> |
|Personen mit mindestens der View Items-Berechtigung erlauben, eingebetteten Code oder Makros in einem Dokument auszuführen.  <br/> |Aktivieren Sie das Kontrollkästchen zum **Ausführen von Skripts und Bildschirmleseprogrammen für heruntergeladene Dokumente zulassen** .  <br/> Wenn Sie diese Option auswählen, können Benutzercode ausführen, um den Inhalt eines Dokuments zu extrahieren.           |
|Verlangen, dass Personen Ihre Anmeldeinformationen in bestimmten Intervallen überprüfen.  <br/> Wählen Sie diese Option aus, wenn Sie den Zugriff auf Inhalte auf einen bestimmten Zeitraum einschränken möchten. Wenn Sie diese Option auswählen, laufen die Veröffentlichungslizenzen für die Personen, die für den Zugriff auf den Inhalt gelten, nach der angegebenen Anzahl von Tagen ab, und Personen müssen zum Server zurückkehren, um Ihre Anmeldeinformationen zu überprüfen und eine neue Kopie herunterzuladen.  <br/> |Aktivieren Sie das Kontrollkästchen **Benutzer müssen Ihre Anmeldeinformationen mit diesem Intervall (Tage) überprüfen** , und geben Sie dann die Anzahl der Tage an, für die das Dokument angezeigt werden soll.  <br/> |
| Verhindern, dass Personen Dokumente hochladen, die IRM nicht unterstützen, in dieser Liste oder Bibliothek.  <br/>  Wenn Sie diese Option auswählen, können die Benutzer keine der folgenden Dateitypen hochladen:  <br/>  Dateitypen, die auf allen Front-End-Webservern nicht über entsprechende IRM-Schutzkomponenten verfügen.  <br/>  Dateitypen, die von SharePoint Server 2010 nicht entschlüsselt werden können.  <br/>  Dateitypen, die in einem anderen Programm IRM-geschützt sind  <br/> |Aktivieren Sie das Kontrollkästchen **Benutzer dürfen keine Dokumente hochladen, die IRM nicht unterstützen** .  <br/> |
|Entfernen Sie eingeschränkte Berechtigungen aus dieser Liste oder Bibliothek zu einem bestimmten Datum.  <br/> |Aktivieren Sie das Kontrollkästchen **Zugriff auf die Bibliothek beschränken** auf, und wählen Sie dann das gewünschte Datum aus.  <br/> |
|Steuern des Intervalls, in dem die Anmeldeinformationen für das Programm, das zum Öffnen des Dokuments lizenziert ist, zwischengespeichert werden.  <br/> |Geben Sie im Feld **Gruppen Schutz und Anmeldeinformationen festlegen**in der Anzahl von Tagen theinterval für das Zwischenspeichern von Anmeldeinformationen ein.  <br/> |
|Gruppen Schutz zulassen, sodass Benutzer für Mitglieder derselben Gruppe freigeben können.  <br/> |Wählen Sie **Gruppen Schutz zulassen**aus, und geben Sie den Namen der Gruppe für die Freigabe ein.  <br/> |
   
8. Nachdem Sie die gewünschten Optionen ausgewählt haben, klicken Sie auf **OK**.
  
## <a name="what-is-information-rights-management"></a>Was ist Verwaltung von Informationsrechten?
<a name="__toc256598175"> </a>

Mit der Verwaltung von Informationsrechten (IRM) können Sie die Aktionen einschränken, die Benutzer auf Dateien übernehmen dürfen, die aus Listen oder Bibliotheken heruntergeladen wurden. IRM verschlüsselt die heruntergeladenen Dateien und beschränkt die Gruppe von Benutzern und Programmen, von denen diese Dateien entschlüsselt werden dürfen. IRM kann auch die Rechte der Benutzer, die Dateien lesen dürfen, so einschränken, dass sie keine Aktionen wie das Drucken von Kopien der Dateien oder das Kopieren von Text aus ihnen ausführen können.
  
Sie können IRM in Listen oder Bibliotheken verwenden, um die Verbreitung von vertraulichen Inhalten einzuschränken. Wenn Sie beispielsweise eine Dokumentbibliothek erstellen, um Informationen zu bevorstehenden Produkten mit ausgewählten Marketing Vertretern gemeinsam zu verwenden, können Sie mithilfe von IRM verhindern, dass diese Personen diese Inhalte für andere Mitarbeiter im Unternehmen freigeben.
  
Auf einer Website wenden Sie IRM auf eine gesamte Liste oder Bibliothek und nicht auf einzelne Dateien an. Dadurch wird es einfacher, einen konsistenten Schutzgrad für eine ganze Gruppe von Dokumenten oder Dateien sicherzustellen. IRM kann daher Ihre Organisation bei der Durchsetzung von Unternehmensrichtlinien unterstützen, die die Verwendung und Weitergabe vertraulicher oder proprietärer Informationen steuern.
  
> [!NOTE]
> Die Informationen auf dieser Seite zur Verwaltung von Informationsrechten ersetzen alle Ausdrücke, die in allen Microsoft SharePoint Server 2013-und SharePoint Server 2016-Lizenz Begriffs Vereinbarungen auf "Information Rights Management" verweisen. 
  
### <a name="how-irm-can-help-protect-content"></a>Wie IRM zum Schutz von Inhalten beitragen kann
<a name="__toc256598176"> </a>

IRM unterstützt den Schutz eingeschränkter Inhalte auf folgende Weise:
  
- Verhindert, dass ein autorisierter Betrachter das Kopieren, ändern, drucken, Faxen oder kopieren und Einfügen des Inhalts zur nicht autorisierten Verwendung ermöglicht
    
- Verhindert, dass ein autorisierter Viewer den Inhalt mithilfe der Druck Bildschirm Funktion in Microsoft Windows kopiert
    
- Verhindert, dass ein nicht autorisierter Betrachter den Inhalt anzeigt, wenn er per e-Mail gesendet wird, nachdem er vom Server heruntergeladen wurde.
    
- Schränkt den Zugriff auf Inhalte auf einen bestimmten Zeitraum ein, nach dem Benutzer ihre Anmeldeinformationen bestätigen und erneut herunterladen müssen.
    
- Unterstützt die Durchsetzung von Unternehmensrichtlinien, die die Verwendung und Verbreitung von Inhalten in Ihrer Organisation steuern
    
### <a name="how-irm-cannot-help-protect-content"></a>Wie IRM nicht zum Schutz von Inhalten beitragen kann
<a name="__toc256598177"> </a>

IRM kann eingeschränkte Inhalte nicht aus folgenden Bereichen schützen:
  
- Löschung, Diebstahl, Erfassung oder Übertragung durch bösartige Programme wie Trojanische Pferde, keyloggers und bestimmte Arten von Spyware
    
- Verlust oder Beschädigung aufgrund der Aktionen von Computerviren
    
- Manuelles Kopieren oder erneutes Eingeben von Inhalten aus der Anzeige auf einem Bildschirm
    
- Digitale oder Film Fotografie von Inhalten, die auf einem Bildschirm angezeigt werden
    
- Kopieren durch die Verwendung von Drittanbieter-Bildschirmaufnahmeprogrammen
    
- Kopieren von Inhaltsmetadaten (Spaltenwerte) durch die Verwendung von Bildschirmaufnahmeprogrammen eines Drittanbieters oder durch Kopieren und Einfügen
    
[Anwenden von Information Rights Management auf eine Liste oder Bibliothek](https://support.office.com/article/6714cfe3-ef39-43b0-bb65-a887726bb63c)
  
## <a name="how-irm-works-for-lists-and-libraries"></a>FunktionsWeise von IRM für Listen und Bibliotheken
<a name="__toc256598178"> </a>

Der IRM-Schutz wird auf Dateien auf der Listen-oder Bibliotheksebene angewendet. Wenn IRM für eine Bibliothek aktiviert ist, gilt die Rechteverwaltung für alle Dateien in dieser Bibliothek. Wenn IRM für eine Liste aktiviert ist, gilt die Rechteverwaltung nur für Dateien, die an Listenelemente angefügt sind, nicht die eigentlichen Listenelemente.
  
Wenn Benutzer Dateien in einer IRM-fähigen Liste oder Bibliothek herunterladen, werden die Dateien verschlüsselt, sodass nur autorisierte Personen Sie anzeigen können. Jede Datei mit verwalteten Rechten enthält außerdem eine Veröffentlichungslizenz, die den Personen, die die Datei anzeigen, Einschränkungen auferlegt. Zu den typischen Einschränkungen gehört das Erstellen einer schreibgeschützten Datei, das Deaktivieren des Kopierens von Text, das verhindern des Speicherns einer lokalen Kopie und das verhindern, dass Personen die Datei drucken. Client Programme, die IRM-gestützte Dateitypen lesen können, verwenden die Veröffentlichungslizenz innerhalb der Datei mit verwalteten Rechten, um diese Einschränkungen zu erzwingen. So behält eine Datei mit verwalteten Rechten ihren Schutz auch nach dem Herunterladen vom Server.
  
Die Einschränkungen, die beim Herunterladen aus einer Liste oder Bibliothek auf eine Datei angewendet werden, basieren auf den Berechtigungen des jeweiligen Benutzers für die Website, die die Datei enthält. In der folgenden Tabelle wird erläutert, wie die Berechtigungen für Websites IRM-Berechtigungen entsprechen.
  
|**Berechtigungen**|**IRM-Berechtigungen**|
|:-----|:-----|
|Berechtigungen verwalten, Website verwalten  <br/> |**Vollzugriff** (wie vom Clientprogramm definiert): diese Berechtigung ermöglicht es einem Benutzer im Allgemeinen, Berechtigungen für Inhalte mit verwalteten Rechten zu lesen, zu bearbeiten, zu kopieren, zu speichern und zu ändern.  <br/> |
|Bearbeiten von Elementen, Verwalten von Listen, hinzufügen und Anpassen von Seiten  <br/> |**Bearbeiten**, **Kopieren**und **Speichern**: ein Benutzer kann eine Datei nur drucken, wenn das Kontrollkästchen **Benutzern das Drucken von Dokumenten erlauben** auf der Seite Einstellungen für die Verwaltung von Informationsrechten für die Liste oder Bibliothek aktiviert ist.  <br/> |
|
            Elemente anzeigen  <br/> |**Lesen**: ein Benutzer kann das Dokument lesen, aber seinen Inhalt nicht kopieren oder ändern. Ein Benutzer kann nur drucken, wenn das Kontrollkästchen **Benutzer können Dokumente drucken** aktiviert ist, auf der Seite Einstellungen für die Verwaltung von Informationsrechten für die Liste oder Bibliothek.  <br/> |
|Andere  <br/> |Keine anderen Berechtigungen entsprechen den IRM-Berechtigungen direkt.  <br/> |
   
Wenn Sie IRM für eine Liste oder Bibliothek in SharePoint Server 2013 aktivieren, können Sie nur Dateitypen in dieser Liste oder Bibliothek schützen, für die eine Schutzkomponente auf allen Front-End-Webservern installiert ist. Ein Protector ist ein Programm, das die Verschlüsselung und Entschlüsselung von Dateien mit verwalteten Rechten eines bestimmten Dateiformats steuert. SharePoint enthält Schutzfolien für die folgenden Dateitypen:
  
- Microsoft Office InfoPath-Formulare
    
- Die 97-2003-Dateiformate für die folgenden Microsoft Office-Programme: Word, Excel und PowerPoint
    
- Die Office Open XML-Formate für die folgenden Microsoft Office-Programme: Word, Excel und PowerPoint
    
- XML Paper Specification (XPS)-Format
    
Wenn in Ihrer Organisation zusätzlich zu den oben aufgeführten die IRM zum Schutz anderer Dateitypen verwendet werden soll, muss der Server Administrator die Schutzkomponenten für diese zusätzlichen Dateiformate installieren.
  

