---
title: Schützen von lokalen Postfächern mit Exchange Online Schutz
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/1/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- GEU150
- GMA150
- GPA150
- MET150
ms.assetid: c5e95951-da67-4ec7-92c5-982abd477e69
ms.collection:
- M365-security-compliance
description: Selbst wenn Sie planen, einige oder alle ihre Postfächer lokal zu hosten, können Sie die Postfächer dennoch mit Exchange Online Schutz schützen (EoP). Wenn Sie Connectors konfigurieren möchten, muss Ihr Konto ein globales Administratorkonto für Office 365 oder ein Exchange-Unternehmensadministratorkonto (Rollengruppe "Organisationsverwaltung") sein. Informationen dazu, wie sich Office 365 Berechtigungen auf Exchange-Berechtigungen beziehen, finden Sie unter Zuweisen von Administratorrollen in Office 365 betrieben von 21Vianet. Wenn alle Exchange-Postfächer lokal sind, führen Sie die folgenden Schritte aus, um den EoP-Dienst einzurichten.
ms.openlocfilehash: 20fa94a356823e624fcb42dc493d555cec3fe523
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156937"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a>Schützen von lokalen Postfächern mit Exchange Online Schutz

> [!NOTE]
> Dieser Artikel bezieht sich nur auf Office 365, die von 21Vianet in China betrieben werden. 
  
Selbst wenn Sie planen, einige oder alle ihre Postfächer lokal zu hosten, können Sie die Postfächer dennoch mit Exchange Online Schutz schützen (EoP). Wenn Sie Connectors konfigurieren möchten, muss Ihr Konto ein globales Administratorkonto für Office 365 oder ein Exchange-Unternehmensadministratorkonto (Rollengruppe "Organisationsverwaltung") sein. Informationen dazu, wie sich Office 365 Berechtigungen auf Exchange-Berechtigungen beziehen, finden Sie unter [Zuweisen von Administratorrollen in Office 365 betrieben von 21Vianet](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac). Wenn alle Exchange-Postfächer lokal sind, führen Sie die folgenden Schritte aus, um den EoP-Dienst einzurichten. 
  
## <a name="step-1-use-the-microsoft-365-admin-center-to-add-and-verify-your-domain"></a>Schritt 1: Verwenden des Microsoft 365 Admin Center zum Hinzufügen und Überprüfen Ihrer Domäne

1. Navigieren Sie im Microsoft 365 Admin Center zu Setup, um Ihre Domäne dem Dienst hinzuzufügen.
    
2.  Führen Sie die Schritte im Portal aus, um dem DNS-Hosting-Anbieter die entsprechenden DNS-Einträge hinzuzufügen, um den Domänenbesitz zu überprüfen. 
    
> [!TIP]
> [Fügen Sie Ihre Domäne und Benutzer Office 365 betrieben von 21Vianet hinzu](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) , und [Erstellen Sie DNS-Einträge für Office 365 beim Verwalten Ihrer DNS-Einträge](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) sind hilfreiche Ressourcen, die Sie beim Hinzufügen Ihrer Domäne zum Dienst und beim Konfigurieren von DNS referenzieren. 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a>Schritt 2: Hinzufügen von Empfängern und Konfigurieren des Domänentyps

Bevor Sie die Übermittlung Ihrer E-Mails zum und vom EOP-Dienst konfigurieren, empfehlen wir, Ihre Empfänger zum Dienst hinzuzufügen. Es gibt dazu verschiedene Möglichkeiten, die in [Verwalten von E-Mail-Benutzern in EOP](https://go.microsoft.com/fwlink/?LinkId=506782) dokumentiert sind. Wenn Sie verzeichnisbasierte Edge-Blockierung (Directory Based Edge Blocking, DBEB) aktivieren möchten, um im Dienst eine Empfängerprüfung zu erzwingen, nachdem Sie Ihre Empfänger hinzugefügt haben, müssen Sie den Domänentyp außerdem auf "Autorisierend" festlegen. Weitere Informationen zur verzeichnisbasierten Edge-Blockierung finden Sie unter [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781).
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Schritt 3: Einrichten des Nachrichtenflusses mithilfe der Exchange-Verwaltungskonsole

Erstellen Sie in der Exchange-Verwaltungskonsole (EAC) Connectors, die den Nachrichtenfluss zwischen EOP und Ihren lokalen E-Mail-Servern ermöglichen. Ausführliche Anweisungen finden Sie unter [Create required Connectors to Setup Basic Email Flow Through EoP](https://go.microsoft.com/fwlink/?LinkId=506780).
  
 Woher wissen Sie, dass diese Aufgabe erfolgreich war? 
  
 Verwenden Sie die Remoteverbindungsuntersuchung, um einen Test auszuführen, bei dem der Nachrichtenfluss zwischen dem Dienst und der Umgebung geprüft wird. Weitere Informationen finden Sie im Abschnitt "Verwenden der Remote Verbindungs Untersuchung zum Testen der e-Mail-Zustellung" unter [Testen der Nachrichtenübermittlung mit der Remote Verbindungsanalyse](https://go.microsoft.com/fwlink/?LinkId=506784).
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a>Schritt 4: Zulassen eingehender SMTP-Verbindungen an Port 25

Nachdem Sie Connectors konfiguriert haben, sollten Sie 72 Stunden warten, bis Ihre DNS-Datensatzaktualisierungen weitergegeben wurden. Auf diese Weise können Sie den eingehenden Port-25-SMTP-Datenverkehr auf Ihrer Firewall oder Ihren e-Mail-Servern so einschränken, dass e-Mails nur von den EoP-Rechenzentren akzeptiert werden, insbesondere von den IP-Adressen, die unter [URLs und IP-Adressbereichen für Office 365 betrieben von 21Vianet](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection)aufgeführt werden. So schützen Sie Ihre lokale Umgebung, indem Sie den Bereich eingehender Nachrichten einschränken, die Sie empfangen können. Wenn Ihr E-Mail-Server Einstellungen aufweist, welche die IP-Adressen steuern, die für E-Mail-Relay eine Verbindung herstellen dürfen, sollten Sie zusätzlich diese Einstellungen aktualisieren.
  
> [!TIP]
> Konfigurieren Sie Einstellungen auf dem SMTP-Server mit einem Verbindungstimeout von 60 Sekunden. Diese Einstellung ist in den meisten Fällen sinnvoll, da sie eine gewisse Verzögerung erlaubt, falls z. B. eine Nachricht mit einem großen Anhang gesendet wird. 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Schritt 5: Prüfen Sie in der Shell, dass Spamnachrichten in die jeweiligen Junk-E-Mail-Ordner der Benutzer umgeleitet werden.

Sie müssen eine Reihe von Konfigurationsschritten ausführen, um wirklich sicherzustellen, dass Junk-E-Mail (Spam) in die Junk-E-Mail-Ordner der Benutzer umgeleitet werden. Die Schritte werden bereitgestellt [, um sicherzustellen, dass Spam an die Junk-e-Mail-Ordner der einzelnen Benutzer weitergeleitet wird](https://go.microsoft.com/fwlink/?LinkId=506804). Wenn die Nachrichten nicht in die Junk-E-Mail-Ordner der Benutzer verschoben werden sollen, können Sie eine andere Aktion auswählen, indem Sie die standardmäßige Inhaltsfilterrichtlinie im Exchange Admin Center bearbeiten. Weitere Informationen finden Sie unter [Configure Content Filter Policies](https://go.microsoft.com/fwlink/?LinkId=506805). 
  
## <a name="step-6-use-the-microsoft-365-admin-center-to-point-your-mx-record-to-eop"></a>Schritt 6: Verwenden des Microsoft 365 Admin Center zum Verweisen Ihres MX-Eintrags auf EoP

Befolgen Sie die Konfigurationsschritte für Office 365-Domänen, um den MX-Eintrag für die Domäne zu aktualisieren, damit Ihre eingehenden E-Mails über EOP weitergeleitet werden. Weitere Informationen finden Sie erneut [Erstellen von DNS-Einträgen für Office 365, wenn Sie Ihre DNS-Einträge verwalten](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b).
  
Woher wissen Sie, dass diese Aufgabe erfolgreich war?
  
 Verwenden Sie die Remoteverbindungsuntersuchung, um einen Test auszuführen, der Ihren MX-Eintrag überprüft. Weitere Informationen finden Sie unter "Verwenden der Remote Verbindungs Untersuchung zum Testen des MX-Eintrags und des ausgehenden Connectors" im Abschnitt " [Testen der Nachrichtenübermittlung mit der Remote Verbindungsanalyse](https://go.microsoft.com/fwlink/?LinkId=506784)". 
  
Zu diesem Zeitpunkt haben Sie die Dienstübermittlung für einen ordnungsgemäß konfigurierten Ausgang auf dem lokalen Connector geprüft und sichergestellt, dass Ihr MX-Eintrag auf EOP verwiesen wurde. Sie können nun zusätzlich die folgenden Tests ausführen, um sicherzustellen, dass der Dienst eine E-Mail erfolgreich an Ihre lokale Umgebung versendet hat:
  
- Klicken Sie in der Remoteverbindungsuntersuchung auf die Registerkarte **Office 365**, führen Sie anschließend den **Eingehende SMTP-E-Mail**-Test unter **Internet E-Mail-Tests** aus.
    
- Senden Sie von einem webbasierten E-Mail-Konto eine E-Mail an einen E-Mail-Empfänger in Ihrer Organisation, dessen Domäne der Domäne entspricht, die Sie dem Dienst hinzugefügt haben. Bestätigen Sie mithilfe von Microsoft Outlook oder einem anderen E-Mail-Client die Zustellung der Nachricht an das lokale Postfach.
    
- Wenn Sie einen Test für ausgehende E-Mails durchführen möchten, können Sie von einem Benutzer in Ihrer Organisation aus eine E-Mail an ein webbasiertes E-Mail-Konto senden und überprüfen, ob die Nachricht übermittelt wurde.
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a>Seltener: ein Hybrid-Setup mit lokalen und in der Cloud bereitgestellten Postfächern

Wenn Sie lokale Exchange-Postfächer und mindestens ein Postfach in der Cloud in Exchange Online haben, haben Sie ein *hybrides* Setup. In einem hybriden Setup arbeiten Features wie frei/gebucht-Kalenderfreigabe und e-Mail-Routing in Ihren lokalen und Cloud-Umgebungen zusammen. Möglicherweise haben Sie ein hybrides Setup eingerichtet, während Sie Postfächer zu Exchange Online wechseln. Eine Hybridumgebung ist anders als EoP eigenständiger Schutz eingerichtet. 
  
Sie können ein Hybrid Szenario auswählen, um Cloud-basierte e-Mails für die meisten ihrer Mitarbeiter zu nutzen. Sie können dies tun, während Sie auch einige Postfächer lokal hosten; beispielsweise für Ihre Rechtsabteilung. 
  
Ein hybrides Setup kann komplex sein, bietet aber viele Vorteile. Weitere Informationen zum Einrichten von Hybrid Szenarien mit Exchange finden Sie unter [Konfigurieren von Exchange-Hybrid Bereitstellungsfeatures mit Office 365 betrieben von 21Vianet](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d).
  

