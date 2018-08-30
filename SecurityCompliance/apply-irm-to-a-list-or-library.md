---
title: Zuweisen einer Liste oder Bibliothek (Information Rights Management, IRM)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1
description: (Information Rights Management, IRM) können Sie kontrollieren und Schützen von Dateien, die von Listen oder Bibliotheken heruntergeladen werden.
ms.openlocfilehash: 5a48abf13841716d4dba34311d69ca2e6a5ea422
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529381"
---
# <a name="apply-information-rights-management-irm-to-a-list-or-library"></a>Zuweisen einer Liste oder Bibliothek (Information Rights Management, IRM)

(Information Rights Management, IRM) können Sie kontrollieren und Schützen von Dateien, die von Listen oder Bibliotheken heruntergeladen werden.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Der Azure Rights Management-Dienst (Azure RMS) von Azure Information Protection und die entsprechende lokale Active Directory-Rechteverwaltungsdienste (AD RMS), werden Information Rights Management für Websites unterstützen. Es sind keine separaten oder eine zusätzlichen Installationen erforderlich.
    
- Vor dem Anwenden von IRM auf eine Liste oder Bibliothek müssen sie zuerst von einem Administrator für Ihre Website aktiviert werden.
    
- Zum Anwenden von IRM auf eine Liste oder Bibliothek benötigen Sie Administratorberechtigungen für diese Liste oder Bibliothek.
    
- Wenn Sie SharePoint Online verwenden, können Ihre Benutzer Timeouts für die auftreten, wenn größere IRM-geschützten Dateien herunterladen. In diesem Fall dann Anwenden von IRM-Schutz mithilfe Ihrer Office-Programme, und speichern Sie größere Dateien in einer SharePoint-Dokumentbibliothek, die IRM nicht verwendet.
    
> [!NOTE]
> Wenn Sie SharePoint Server 2013 verwenden, muss ein Serveradministrator IRM-Schutz auf allen Front-End-Webservern für jeden Dateityp installieren, die die Personen in Ihrer Organisation mit IRM schützen möchten. 
  
## <a name="apply-irm-to-a-list-or-library"></a>Anwenden von IRM auf eine Liste oder Bibliothek
<a name="__toc256598179"> </a>

![Einstellungen für die Verwaltung von Informationsrechten](media/1b708102-9c90-42b0-b255-ef0e72d0be88.png)
  
1. Wechseln Sie zu der Liste oder Bibliothek, für die Sie IRM konfigurieren möchten.
    
2. Klicken Sie im Menüband auf klicken Sie die Registerkarte **Bibliothek** , und klicken Sie dann auf **Bibliothekseinstellungen**. (Wenn Sie in einer Liste arbeiten, klicken Sie auf die Registerkarte **Liste** , und klicken Sie dann auf **Listeneinstellungen**).
    
    ![SharePoint-Formularbibliothek Schaltflächen auf Menüband](media/cdf718fa-d792-40fc-8026-00c3b80b9e05.png)
  
3. Klicken Sie unter **Berechtigungen und Verwaltung**klicken Sie auf **Verwaltung von Informationsrechten**. Wenn Sie der Link für die Verwaltung von Informationsrechten nicht angezeigt wird, möglicherweise IRM nicht für Ihre Website aktiviert werden. Wenden Sie sich an Ihren Administrator, um festzustellen, ob es zur Aktivierung von IRM für Ihre Website möglich ist. Der Link für die Verwaltung von Informationsrechten wird für Bildbibliotheken nicht angezeigt.
    
4. Aktivieren Sie das Kontrollkästchen **Berechtigung für Dokumente in dieser Bibliothek beim Herunterladen einschränken** , die Berechtigung eingeschränkten auf Dokumente angewendet, die aus dieser Liste oder Bibliothek heruntergeladen werden, auf der Seite **Information Rights Management Settings** . 
    
5. Geben Sie in das Feld **erstellen einen Titel der Berechtigungsrichtlinie** einen beschreibenden Namen für die Richtlinie, die Sie später verwenden können, um diese Richtlinie von anderen Richtlinien zu unterscheiden. Beispielsweise können Sie **Company Confidential** eingeben, wenn einer Liste oder Bibliothek, die Dokumente des Unternehmens enthält, die vertrauliche sind anwenden eingeschränkten Berechtigung. 
    
6. Geben Sie im Feld **eine Beschreibung der Berechtigungsrichtlinie hinzufügen** eine Beschreibung, die an Personen angezeigt wird, die verwenden diese Liste oder Bibliothek, die erklärt, wie Dokumente in dieser Liste oder Bibliothek behandelt werden sollen. Beispielsweise können Sie **den Inhalt dieses Dokuments nur mit anderen Mitarbeitern besprechen** eingeben, wenn Sie den Zugriff auf die Informationen in diesen Dokumenten auf interne Mitarbeiter einschränken möchten. 
    
7. Um zusätzliche Einschränkungen auf die Dokumente in dieser Liste oder Bibliothek anzuwenden, klicken Sie auf **Optionen anzeigen**, und eine der folgenden Aktionen aus:
    
|**Gehen Sie zu diesem Zweck wie folgt vor:**|**Führen Sie diese Schritte aus:**|
|:-----|:-----|
|Zulassen von Personen, die zum Drucken von Dokumenten aus dieser Liste oder Bibliothek  <br/> |Aktivieren Sie das Kontrollkästchen **Zulassen Zuschauer zu drucken** .  <br/> |
|Können Personen mit mindestens die Berechtigung anzeigen von Elementen in einem Dokument eingebetteten Code oder Makros ausführen.  <br/> |Aktivieren Sie das Kontrollkästchen **Zulassen Leser von Berichten zum Ausführen von Skripts und Bildschirm Reader auf heruntergeladene Dokumente** .  <br/> Wenn Sie diese Option auswählen, können Benutzer Code, um den Inhalt eines Dokuments zu extrahieren ausführen.           |
|Erfordern Sie, dass Benutzer ihre Anmeldeinformationen in bestimmten Abständen überprüfen.  <br/> Wählen Sie diese Option, wenn Sie den Zugriff auf Inhalte für einen bestimmten Zeitraum einschränken möchten. Wenn Sie diese Option auswählen, läuft Veröffentlichungslizenzen Zugriff auf den Inhalt der Benutzer nach die angegebene Anzahl von Tagen und Personen muss auf dem Server ihre Anmeldeinformationen zu überprüfen, und Laden Sie eine neue Kopie zurück.  <br/> |Wählen Sie aus der **Benutzer müssen ihre Anmeldeinformationen überprüfen mithilfe dieses Intervall (in Tagen)** Kontrollkästchen, und geben Sie dann die Anzahl der Tage, die das Dokument angezeigt werden soll.  <br/> |
| Verhindern Sie, dass Benutzer Dokumente, die IRM nicht, zu dieser Liste oder Bibliothek unterstützen hochladen.  <br/>  Wenn Sie diese Option auswählen, werden Personen nicht Hochladen eines der folgenden Dateitypen:  <br/>  Dateitypen, die keine entsprechenden IRM-Schutz auf allen Front-End-Webserver installiert haben.  <br/>  Dateitypen, die SharePoint Server 2010 Entschlüsselung ist nicht möglich.  <br/>  Dateitypen, die Verwaltung von Informationsrechten in einem anderen Programm sind  <br/> |Aktivieren Sie das Kontrollkästchen **Benutzer Dokumente hochladen, die IRM nicht unterstützen, nicht zulassen** .  <br/> |
|Entfernen Sie eingeschränkte Berechtigungen aus dieser Liste oder Bibliothek an einem bestimmten Datum.  <br/> |Aktivieren Sie das Kontrollkästchen **Einschränken des Zugriffs auf die Bibliothek auf Beenden** , und wählen Sie dann das gewünschte Datum aus.  <br/> |
|Steuerelement das Intervall an, dass die Anmeldeinformationen für die Anwendung zwischengespeichert werden, die zum Öffnen des Dokuments lizenziert ist.  <br/> |Geben Sie in der **Gruppe Schutz und die Anmeldeinformationen Intervall festgelegt**Theinterval zum Zwischenspeichern von Anmeldeinformationen in Tagen ein.  <br/> |
|Ermöglichen Sie Gruppe Schutz, damit Benutzer mit den Mitgliedern dieser Gruppe freigeben können.  <br/> |Wählen Sie **die Gruppe Protection zulassen**, und geben Sie den Namen der Gruppe für die Freigabe.  <br/> |
   
8. Nachdem Sie die gewünschten Optionen ausgewählt haben, klicken Sie auf **OK**.
  
## <a name="what-is-information-rights-management"></a>Was ist die Verwaltung von Informationsrechten?
<a name="__toc256598175"> </a>

(Information Rights Management, IRM) können Sie die Aktionen zu beschränken, die Benutzer für Dateien ausführen können, die von Listen oder Bibliotheken heruntergeladen wurden. IRM verschlüsselt die heruntergeladenen Dateien und schränkt die Benutzer und Programme, die diese Dateien entschlüsseln zulässig sind. IRM kann auch die Rechte der Benutzer beschränken, die zum Lesen von Dateien, damit sie wie das Drucken von Kopien der Dateien Aktionen oder das Kopieren von Text daraus können nicht zulässig sind.
  
IRM können für Listen oder Bibliotheken Sie um die Verbreitung von vertrauliche Inhalte zu begrenzen. Wenn Sie eine Dokumentbibliothek zum Freigeben von Informationen zu anstehenden Produkten mit ausgewählten marketing Vertretern erstellen, können Sie beispielsweise IRM verwenden, um zu verhindern, dass diese Personen freigeben dieser Inhalte für andere Mitarbeiter im Unternehmen.
  
Klicken Sie auf eine Website wenden Sie IRM nicht auf eine gesamte Liste oder Bibliothek, sondern in einzelne Dateien. Dies vereinfacht die eine einheitliche Schutzstufe für einen ganzen Satz von Dokumenten oder Dateien sicherzustellen. IRM kann daher Ihrer Organisation zum Erzwingen von Unternehmensrichtlinien, die die Verwendung und die Verbreitung von vertraulichen oder proprietären Informationen steuern helfen.
  
> [!NOTE]
> Die Informationen auf dieser Seite zur Verwaltung von Informationsrechten ersetzt alle Microsoft SharePoint Server 2013 und SharePoint Server 2016 Begriff Lizenzverträge Begriffe, die "Information Rights Management" verweisen. 
  
### <a name="how-irm-can-help-protect-content"></a>Wie IRM schützen kann Inhalte
<a name="__toc256598176"> </a>

Verwaltung von Informationsrechten kann eingeschränkten Inhalte wie folgt schützen:
  
- Wird verhindert, dass einen autorisierten Benutzer kopieren, ändern, drucken, Faxen, oder kopieren und Einfügen von Inhalt für unerlaubte Verwendung
    
- Wird verhindert, dass einen autorisierten Benutzer den Inhalt mithilfe des Druck-Features in Microsoft Windows kopieren
    
- Wird verhindert, dass einen nicht autorisierten Benutzer den Inhalt anzeigen, wenn sie per E-mail gesendet wird, nachdem er vom Server heruntergeladen wurde
    
- Schränkt den Zugriff auf einen angegebenen Zeitraum, nach dem Benutzer ihre Anmeldeinformationen bestätigen müssen, und den Inhalt erneut herunterladen von Inhalten
    
- Erzwingen von Unternehmensrichtlinien, die die Verwendung und die Verbreitung von Inhalten innerhalb Ihrer Organisation steuern können
    
### <a name="how-irm-cannot-help-protect-content"></a>Wie IRM kann nicht zum Schutz des Inhalts
<a name="__toc256598177"> </a>

IRM schützen nicht eingeschränkten Inhalte aus den folgenden:
  
- Löschung, Diebstahl, Aufzeichnung oder Übertragung durch bösartige Programme wie trojanischen Pferden, Tastatureingabe und bestimmte Arten von spyware
    
- Verlust oder Beschädigung aufgrund der Aktionen von Computerviren
    
- Manuelles Kopieren oder Abschreiben von Inhalten aus der Anzeige auf dem Bildschirm
    
- Digitale oder konventionelle Fotos von Inhalten, die auf dem Bildschirm angezeigt wird
    
- Kopieren mithilfe von Drittanbieter-Bildschirmaufnahme Programme
    
- Kopieren von Inhaltsmetadaten (Spaltenwerte) durch die Verwendung von Drittanbieter-Bildschirmaufnahme Programme oder kopieren und einfügen
    
[Verwaltung von Informationsrechten auf eine Liste oder Bibliothek anwenden](https://support.office.com/article/6714cfe3-ef39-43b0-bb65-a887726bb63c)
  
## <a name="how-irm-works-for-lists-and-libraries"></a>Funktionsweise von IRM für Listen und Bibliotheken
<a name="__toc256598178"> </a>

IRM-Schutz wird auf Dateien auf die Liste oder Bibliotheksebene angewendet. Wenn IRM für eine Dokumentbibliothek aktiviert ist, gilt die Verwaltung von Informationsrechten für alle Dateien in dieser Bibliothek. Wenn IRM für eine Liste aktiviert ist, gilt die Verwaltung von Informationsrechten nur für Dateien, die Listenelemente, nicht die tatsächliche Listenelemente angefügt sind.
  
Wenn Benutzer Dateien in einer IRM-fähigen Liste oder Bibliothek herunterladen, werden die Dateien verschlüsselt, so dass nur autorisierte Personen angezeigt werden können. Jede Datei mit verwalteten rechten enthält außerdem eine Veröffentlichungslizenz, die erfordert Einschränkungen auf die Personen, die die Datei anzeigen. Typische Einschränkungen enthalten eine Datei schreibgeschützt, deaktivieren das Kopieren von Text, die verhindern, dass Personen aus eine lokale Kopie gespeichert und verhindert, dass Personen die Datei drucken zu machen. Clientprogramme, die IRM-unterstützten Dateitypen lesen können verwenden der Veröffentlichungslizenz innerhalb der Datei mit verwalteten rechten zum Erzwingen von dieser Beschränkungen. Dies ist wie eine Datei mit verwalteten rechten seinen Schutz behält auch nach dem Download vom Server.
  
Die Arten von Einschränkungen, die in eine Datei angewendet werden, wenn sie von einer Liste oder Bibliothek heruntergeladen wird basieren auf den einzelnen Benutzer Berechtigungen auf der Website, die die Datei enthält. In der folgenden Tabelle wird erläutert, wie Berechtigungen für Websites die IRM-Berechtigungen entsprechen.
  
|**Berechtigungen**|**IRM-Berechtigungen**|
|:-----|:-----|
|Berechtigungen verwalten, Website verwalten  <br/> |**Vollzugriff** (gemäß Definition durch das Clientprogramm): mit dieser Berechtigung können in der Regel ein Benutzers zu lesen, bearbeiten, kopieren, speichern und Ändern der Berechtigungen für Inhalte mit verwalteten rechten.  <br/> |
|Elemente bearbeiten, Listen verwalten, Seiten hinzufügen und anpassen  <br/> |**Bearbeiten**, **Kopieren**und **Speichern**: Benutzer kann eine Datei drucken, nur, wenn das Kontrollkästchen **Benutzern erlauben, Drucken von Dokumenten** auf der Seite Information Rights Management Settings für die Liste oder Bibliothek ausgewählt ist.  <br/> |
|
            Elemente anzeigen  <br/> |**Lesen**: ein Benutzer Lesen des Dokuments, aber nicht kopieren oder seinen Inhalt ändern kann. Nur, wenn das Kontrollkästchen **Benutzern erlauben, Drucken von Dokumenten** auf der Seite Information Rights Management Settings für die Liste oder Bibliothek ausgewählt ist, kann ein Benutzer drucken.<br/> |
|Andere  <br/> |Keine sonstigen Berechtigungen entsprechen direkt IRM-Berechtigungen.  <br/> |
   
Wenn Sie IRM für eine Liste oder Dokumentbibliothek in SharePoint Server 2013 aktivieren, können Sie nur schützen Dateitypen in dieser Liste oder Bibliothek, für die ein IRM-Schutz auf allen Front-End-Webservern installiert ist. Ein IRM-Schutz ist ein Programm, das die Ver- und Entschlüsselung von Dateien mit verwalteten rechten eines bestimmten Dateiformats steuert. SharePoint enthält Schutzvorrichtungen für die folgenden Dateitypen:
  
- Microsoft Office InfoPath-Formularen
    
- Die 97-2003-Dateiformate für die folgenden Microsoft Office-Programme: Word, Excel und PowerPoint
    
- Office Open XML-Formaten für die folgenden Microsoft Office-Programme: Word, Excel und PowerPoint
    
- Das Format der XML Paper Specification (XPS)
    
Wenn Ihre Organisation plant, IRM zum Schutz von anderen Dateitypen zusätzlich zu den oben aufgelisteten verwenden, muss der Serveradministrator Schutzvorrichtungen für diese zusätzlichen Dateiformate installieren.
  

