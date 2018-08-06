---
title: Einrichten Ihres EOP-Diensts
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d74c6ddf-11b0-43ee-b298-8bb0340895f0
description: In diesem Thema wird erläutert, wie Sie Microsoft Exchange Online Protection (EOP) einrichten. Wenn Sie vom Office 365-Assistenten für Domänen hierher geführt wurden, wechseln Sie zurück zum Office 365-Assistenten für Domänen, wenn Sie Exchange Online Protection nicht verwenden möchten. Wenn Sie weitere Informationen zum Konfigurieren von Connectors suchen, finden Sie diese unter Configure mail flow using connectors in Office 365.
ms.openlocfilehash: f1c65164adcaa17c58ae9c4b4b957c477b9e02f3
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027112"
---
# <a name="set-up-your-eop-service"></a>Einrichten Ihres EOP-Diensts

In diesem Thema wird erläutert, wie Sie Microsoft Exchange Online Protection (EOP) einrichten. Wenn Sie vom Office 365-Assistenten für Domänen hierher geführt wurden, wechseln Sie zurück zum Office 365-Assistenten für Domänen, wenn Sie Exchange Online Protection nicht verwenden möchten. Wenn Sie weitere Informationen zum Konfigurieren von Connectors suchen, finden Sie diese unter [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx).
  
> [!NOTE]
> In diesem Thema wird davon ausgegangen, dass lokale Postfächer verwendet werden, die mit EOP geschützt werden sollen - dies wird als eigenständiges Szenario bezeichnet. Wenn Sie mit Exchange Online alle Postfächer in der Cloud hosten möchten, müssen Sie nicht alle hier beschriebenen Schritte ausführen. Rufen Sie [Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286312) auf, um sich anzumelden und Cloudpostfächer zu erwerben. Wenn Sie die Postfächer teils lokal und teils in der Cloud hosten möchten, handelt es sich um ein hybrides Szenario. Für ein solches Szenario sind erweiterte Nachrichtenflusseinstellungen erforderlich. Erläuterungen zu hybridem Nachrichtenfluss sowie Links zu Ressourcen mit den entsprechenden Setupschritten finden Sie unter [Exchange Server 2013 Hybrid Deployments](http://technet.microsoft.com/library/59e32000-4fcf-417f-a491-f1d8f9aeef9b.aspx). 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

- Geschätzte Zeit bis zum Abschließen dieser Aufgabe: 1 Stunde
    
- Wenn Sie Connectors konfigurieren möchten, muss Ihr Konto ein globales Administratorkonto für Office 365 oder ein Exchange-Unternehmensadministratorkonto (Rollengruppe "Organisationsverwaltung") sein. Weitere Informationen dazu, in welcher Beziehung Office 365-Berechtigungen zu Exchange-Berechtigungen stehen, finden Sie unter [Berechtigungen in Office 365](https://go.microsoft.com/fwlink/p/?LinkID=335814).
    
- Wenn Sie sich noch nicht bei EOP registriert haben, rufen Sie [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=282660) auf, und erwerben oder testen Sie den Dienst. 
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="how-do-you-do-this"></a>Wie gehen Sie dazu vor?

### <a name="step-1-use-the-office-365-admin-center-to-add-and-verify-your-domain"></a>Schritt 1: Verwenden von Office 365 Admin Center zum Hinzufügen und Überprüfen der Domäne

1. Navigieren Sie im Office 365 Admin Center zu **Setup**, um dem Dienst Ihre Domäne hinzuzufügen. 
    
    Sie wissen nicht, wo Sie das Office 365 Admin Center finden? Erfahren Sie mehr unter [Informationen zum Office 365-Admin-Center](https://go.microsoft.com/fwlink/p/?LinkId=521888).
    
2. Befolgen Sie die Schritte, um Ihrem DNS-Hostinganbieter die entsprechenden DNS-Datensätze hinzuzufügen, um die Domäneneigentümerschaft zu überprüfen.
    
> [!TIP]
> [Hinzufügen Ihrer Domäne zu Office 365](https://go.microsoft.com/fwlink/p/?LinkId=282303) und [Erstellen von DNS-Einträgen für Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219) sind hilfreiche Ressourcen, auf die Sie zurückgreifen können, wenn Sie dem Dienst Ihre Domäne hinzufügen und DNS konfigurieren. 
  
### <a name="step-2-add-recipients-and-optionally-enable-dbeb"></a>Schritt 2: Hinzufügen von Empfängern und optionales Aktivieren der verzeichnisbasierten Edge-Blockierung (DBEB)

Bevor Sie die Übermittlung Ihrer E-Mails zum und vom EOP-Dienst konfigurieren, empfehlen wir, Ihre Empfänger zum Dienst hinzuzufügen. Es gibt dazu verschiedene Möglichkeiten, die in [Verwalten von E-Mail-Benutzern in EOP](manage-mail-users-in-eop.md) dokumentiert sind. Wenn Sie verzeichnisbasierte Edge-Blockierung (Directory Based Edge Blocking, DBEB) aktivieren möchten, um im Dienst eine Empfängerprüfung zu erzwingen, nachdem Sie Ihre Empfänger hinzugefügt haben, müssen Sie den Domänentyp außerdem auf "Autorisierend" festlegen. Weitere Informationen zur verzeichnisbasierten Edge-Blockierung finden Sie unter [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).
  
### <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Schritt 3: Einrichten des Nachrichtenflusses mithilfe der Exchange-Verwaltungskonsole

Erstellen Sie in der Exchange-Verwaltungskonsole (EAC) Connectors, die den Nachrichtenfluss zwischen EOP und Ihren lokalen E-Mail-Servern ermöglichen. Ausführliche Anweisungen finden Sie unter [Set up connectors to route mail between Office 365 and your own email servers](http://technet.microsoft.com/library/2e93fd60-a5ef-4e64-8e62-2b862b2d1033.aspx).
  
#### <a name="how-do-you-know-this-task-worked"></a>Woher wissen Sie, dass diese Aufgabe erfolgreich war?

Verwenden Sie die Remoteverbindungsuntersuchung, um einen Test auszuführen, bei dem der Nachrichtenfluss zwischen dem Dienst und der Umgebung geprüft wird. Weitere Informationen finden Sie im Abschnitt "Verwenden der Remoteverbindungsuntersuchung zur Prüfung der E-Mail-Zustellung" unter [Testing Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx).
  
### <a name="step-4-allow-inbound-port-25-smtp-access"></a>Schritt 4: Zulassen eingehender SMTP-Verbindungen an Port 25

Nachdem Sie Connectors konfiguriert haben, sollten Sie 72 Stunden warten, bis Ihre DNS-Datensatzaktualisierungen weitergegeben wurden. Schränken Sie anschließend in Ihrer Firewall oder auf Ihren E-Mail-Servern den eingehenden SMTP-Datenverkehr für Port 25 so ein, dass nur E-Mails von EOP-Rechenzentren, genauer gesagt von den unter [Exchange Online Protection-IP-Adressen](exchange-online-protection-ip-addresses.md) aufgeführten IP-Adressen, zugelassen werden. So schützen Sie Ihre lokale Umgebung, indem Sie den Bereich eingehender Nachrichten einschränken, die Sie empfangen können. Wenn Ihr E-Mail-Server Einstellungen aufweist, welche die IP-Adressen steuern, die für E-Mail-Relay eine Verbindung herstellen dürfen, sollten Sie zusätzlich diese Einstellungen aktualisieren.
  
> [!TIP]
> Konfigurieren Sie Einstellungen auf dem SMTP-Server mit einem Verbindungstimeout von 60 Sekunden. Diese Einstellung ist in den meisten Fällen sinnvoll, da sie eine gewisse Verzögerung erlaubt, falls z. B. eine Nachricht mit einem großen Anhang gesendet wird. 
  
### <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Schritt 5: Prüfen Sie in der Shell, dass Spamnachrichten in die jeweiligen Junk-E-Mail-Ordner der Benutzer umgeleitet werden.

Um sicherzustellen, dass Spam (Junk) e-Mail ordnungsgemäß an die Junk-e-Mail-Ordner des Benutzers weitergeleitet wird, müssen Sie ein paar Konfigurationsschritte ausführen. Die Schritte werden in [Stellen Sie sicher, dass Spam an die Junk-e-Mail-Ordner des Benutzers geleitet wird](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)bereitgestellt.
  
Wenn Sie nicht Nachrichten des Benutzers Junk-e-Mail-Ordner verschieben möchten, können Sie eine andere Aktion durch Ihre inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole bearbeiten wählen. Weitere Informationen finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](../configure-your-spam-filter-policies.md).
  
### <a name="step-6-use-the-office-365-admin-center-to-point-your-mx-record-to-eop"></a>Schritt 6: Verwenden von Office 365 Admin Center, um Ihren MX-Eintrag auf EOP zu verweisen

Befolgen Sie die Konfigurationsschritte für Office 365-Domänen, um den MX-Eintrag für die Domäne zu aktualisieren, damit Ihre eingehenden E-Mails über EOP weitergeleitet werden. Stellen Sie sicher, dass Ihr MX-Eintrag direkt auf EOP verweist, damit kein Filterungsdienstrelais eines Drittanbieters eine E-Mail an EOP schreibt. Weitere Informationen finden Sie auch hierzu unter [Erstellen von DNS-Einträgen für Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219).
  
#### <a name="how-do-you-know-this-task-worked"></a>Woher wissen Sie, dass diese Aufgabe erfolgreich war?

Verwenden Sie die Remoteverbindungsuntersuchung, um einen Test auszuführen, der Ihren MX-Eintrag überprüft. Weitere Informationen finden Sie im Abschnitt "Verwenden der Remoteverbindungsuntersuchung zur Prüfung des MX-Eintrags und des ausgehenden Connectors" unter [Testing Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx). 
  
Zu diesem Zeitpunkt haben Sie die Dienstübermittlung für einen ordnungsgemäß konfigurierten Ausgang auf dem lokalen Connector geprüft und sichergestellt, dass Ihr MX-Eintrag auf EOP verwiesen wurde. Sie können nun zusätzlich die folgenden Tests ausführen, um sicherzustellen, dass der Dienst eine E-Mail erfolgreich an Ihre lokale Umgebung versendet hat:
  
- Klicken Sie in der Remoteverbindungsuntersuchung auf die Registerkarte **Office 365**, führen Sie anschließend den **Eingehende SMTP-E-Mail**-Test unter **Internet E-Mail-Tests** aus. 
    
- Senden Sie von einem webbasierten E-Mail-Konto eine E-Mail an einen E-Mail-Empfänger in Ihrer Organisation, dessen Domäne der Domäne entspricht, die Sie dem Dienst hinzugefügt haben. Bestätigen Sie mithilfe von Microsoft Outlook oder einem anderen E-Mail-Client die Zustellung der Nachricht an das lokale Postfach.
    
- Wenn Sie einen Test für ausgehende E-Mails durchführen möchten, können Sie von einem Benutzer in Ihrer Organisation aus eine E-Mail an ein webbasiertes E-Mail-Konto senden und überprüfen, ob die Nachricht übermittelt wurde.
    
> [!TIP]
> Nachdem Sie das Setup abgeschlossen haben, müssen Sie nichts weiter tun, um EOP für das Entfernen von Spam und Malware zu konfigurieren. Spam und Malware werden von EOP automatisch entfernt. Sie können die Einstellungen jedoch in der Exchange-Verwaltungskonsole den jeweiligen Unternehmensanforderungen anpassen. Weitere Informationen finden Sie unter [Anti-Spam and Anti-Malware Protection](http://technet.microsoft.com/library/93c6c227-7442-4293-b64d-ec8f15c928db.aspx). > Es wird empfohlen, nach Bereitstellung des Diensts den Abschnitt [Bewährte Methoden für das Konfigurieren von EOP](best-practices-for-configuring-eop.md) zu lesen, in dem empfohlene Einstellungen und Überlegungen nach der Einrichtung von EOP beschrieben werden. 
  

