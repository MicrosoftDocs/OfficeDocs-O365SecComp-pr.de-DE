---
title: Schützen von lokalen Postfächern mit Exchange Online Protection
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/1/2017
ms.audience: ITPro
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
description: Auch wenn Sie planen, einige oder alle Postfächer lokal zu hosten, können Sie die Postfächer weiterhin mit Exchange Online Protection (EOP) schützen. Zum Konfigurieren von Connectors muss es sich bei Ihrem Konto um einen globalen Administrator von Office 365 oder um einen Exchange-Unternehmens Administrator (die Rollengruppe Organisationsverwaltung) handeln. Informationen zur Beziehung zwischen Office 365-Berechtigungen und Exchange-Berechtigungen finden Sie unter Zuweisen von Administratorrollen in Office 365, betrieben von 21Vianet. Wenn alle Ihre Exchange-Postfächer lokal sind, führen Sie die folgenden Schritte aus, um den EOP-Dienst einzurichten.
ms.openlocfilehash: 40fb5471a084cf245d9aef7f7b2b88effb5c4a83
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276035"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a>Schützen von lokalen Postfächern mit Exchange Online Protection

> [!NOTE]
> Dieser Artikel bezieht sich nur auf Office 365, betrieben von 21Vianet in China. 
  
Auch wenn Sie planen, einige oder alle Postfächer lokal zu hosten, können Sie die Postfächer weiterhin mit Exchange Online Protection (EOP) schützen. Zum Konfigurieren von Connectors muss es sich bei Ihrem Konto um einen globalen Administrator von Office 365 oder um einen Exchange-Unternehmens Administrator (die Rollengruppe Organisationsverwaltung) handeln. Informationen zur Beziehung zwischen Office 365-Berechtigungen und Exchange-Berechtigungen finden Sie unter [Zuweisen von Administratorrollen in office 365, betrieben von 21Vianet](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac). Wenn alle Ihre Exchange-Postfächer lokal sind, führen Sie die folgenden Schritte aus, um den EOP-Dienst einzurichten. 
  
## <a name="step-1-use-the-office-365-admin-center-to-add-and-verify-your-domain"></a>Schritt 1: Verwenden von Office 365 Admin Center zum Hinzufügen und Überprüfen der Domäne

1. Navigieren Sie im Office 365 Admin Center zu Setup, um dem Dienst Ihre Domäne hinzuzufügen.
    
2.  Führen Sie die Schritte im Portal aus, um die entsprechenden DNS-Einträge zu Ihrem DNS-Hostinganbieter hinzuzufügen, um den Domänenbesitz zu überprüfen. 
    
> [!TIP]
> [Hinzufügen Ihrer Domäne und Benutzer zu office 365 betrieben von 21Vianet](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) und [Erstellen von DNS-Einträgen für Office 365 Wenn Sie Ihre DNS-Einträge verwalten](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) , sind hilfreiche Ressourcen zum verweisen, wenn Sie Ihre Domäne zum Dienst hinzufügen und DNS konfigurieren. 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a>Schritt 2: Hinzufügen von Empfängern und Konfigurieren des Domänentyps

Bevor Sie die Übermittlung Ihrer E-Mails zum und vom EOP-Dienst konfigurieren, empfehlen wir, Ihre Empfänger zum Dienst hinzuzufügen. Es gibt dazu verschiedene Möglichkeiten, die in [Verwalten von E-Mail-Benutzern in EOP](https://go.microsoft.com/fwlink/?LinkId=506782) dokumentiert sind. Wenn Sie verzeichnisbasierte Edge-Blockierung (Directory Based Edge Blocking, DBEB) aktivieren möchten, um im Dienst eine Empfängerprüfung zu erzwingen, nachdem Sie Ihre Empfänger hinzugefügt haben, müssen Sie den Domänentyp außerdem auf "Autorisierend" festlegen. Weitere Informationen zur verzeichnisbasierten Edge-Blockierung finden Sie unter [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781).
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Schritt 3: Einrichten des Nachrichtenflusses mithilfe der Exchange-Verwaltungskonsole

Erstellen Sie Connectors im Exchange Admin Center (EAC), die den Nachrichtenfluss zwischen EOP und Ihren lokalen e-Mail-Servern aktivieren. Ausführliche Anweisungen finden Sie unter [Create required Connectors to Set Up Basic Email Flow Through EoP](https://go.microsoft.com/fwlink/?LinkId=506780).
  
 Woher wissen Sie, dass diese Aufgabe erfolgreich war? 
  
 Verwenden Sie die Remote Verbindungs Untersuchung, um einen Test auszuführen, der den Nachrichtenfluss zwischen dem Dienst und ihrer Umgebung überprüft. Weitere Informationen finden Sie im Abschnitt "Verwenden der Remote Verbindungs Untersuchung zum Testen der e-Mail-Übermittlung" unter [Test Mail Flow with the Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?LinkId=506784).
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a>Schritt 4: Zulassen eingehender SMTP-Verbindungen an Port 25

Warten Sie nach dem Konfigurieren von Connectors 72 Stunden, um die Weitergabe von DNS-Eintrags Updates zu ermöglichen. Nachfolgend beschränken Sie den eingehenden Anschluss-25-SMTP-Datenverkehr auf Ihren Firewall-oder e-Mail-Servern so, dass er e-Mails nur aus den EOP-Rechenzentren akzeptiert, insbesondere aus den IP-Adressen, die unter [URLs und IP-Adressbereiche für Office 365 unter 21Vianet betrieben](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection)werden. Dadurch wird Ihre lokale Umgebung geschützt, indem der Umfang eingehender Nachrichten eingeschränkt wird, die Sie empfangen können. Wenn Sie außerdem Einstellungen auf Ihrem e-Mail-Server haben, die die IP-Adressen Steuern, die für e-Mail-Relay zugelassen werden dürfen, aktualisieren Sie diese Einstellungen ebenfalls.
  
> [!TIP]
> Konfigurieren Sie Einstellungen auf dem SMTP-Server mit einem Verbindungstimeout von 60 Sekunden. Diese Einstellung ist in den meisten Fällen sinnvoll, da sie eine gewisse Verzögerung erlaubt, falls z. B. eine Nachricht mit einem großen Anhang gesendet wird. 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Schritt 5: Prüfen Sie in der Shell, dass Spamnachrichten in die jeweiligen Junk-E-Mail-Ordner der Benutzer umgeleitet werden.

Um sicherzustellen, dass Spam (Junk)-e-Mails ordnungsgemäß an den Junk-e-Mail-Ordner der einzelnen Benutzer weitergeleitet werden, müssen Sie einige Konfigurationsschritte ausführen. Mit den Schritten [wird sichergestellt, dass Spam an die Junk-e-Mail-Ordner der einzelnen Benutzer weitergeleitet wird](https://go.microsoft.com/fwlink/?LinkId=506804). Wenn Sie keine Nachrichten in den Junk-e-Mail-Ordner der einzelnen Benutzer verschieben möchten, können Sie eine andere Aktion auswählen, indem Sie Ihre Inhaltsfilter Richtlinien im Exchange Admin Center bearbeiten. Weitere Informationen finden Sie unter [configure Content Filter Policies](https://go.microsoft.com/fwlink/?LinkId=506805). 
  
## <a name="step-6-use-the-office-365-admin-center-to-point-your-mx-record-to-eop"></a>Schritt 6: Verwenden von Office 365 Admin Center, um Ihren MX-Eintrag auf EOP zu verweisen

Führen Sie die Office 365-Domänen Konfigurationsschritte aus, um Ihren MX-Eintrag für Ihre Domäne zu aktualisieren, damit Ihre eingehenden e-Mails über EOP fließen. Weitere Informationen finden Sie erneut unter [Erstellen von DNS-Einträgen für Office 365, wenn Sie Ihre DNS-Einträge verwalten](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b).
  
Woher wissen Sie, dass diese Aufgabe erfolgreich war?
  
 Verwenden Sie die Remote Verbindungs Untersuchung, um einen Test auszuführen, der Ihren MX-Eintrag überprüft. Weitere Informationen finden Sie im Abschnitt "Verwenden der Remote Verbindungs Untersuchung zum Testen des MX-Eintrags und des ausgehenden Connectors" unter [Testen des Nachrichtenflusses mit der Remote Verbindungs Untersuchung](https://go.microsoft.com/fwlink/?LinkId=506784). 
  
Zu diesem Zeitpunkt haben Sie die Dienstübermittlung für einen ordnungsgemäß konfigurierten Ausgang auf dem lokalen Connector geprüft und sichergestellt, dass Ihr MX-Eintrag auf EOP verwiesen wurde. Sie können nun zusätzlich die folgenden Tests ausführen, um sicherzustellen, dass der Dienst eine E-Mail erfolgreich an Ihre lokale Umgebung versendet hat:
  
- Klicken Sie in der Remoteverbindungsuntersuchung auf die Registerkarte **Office 365**, führen Sie anschließend den **Eingehende SMTP-E-Mail**-Test unter **Internet E-Mail-Tests** aus.
    
- Senden Sie von einem webbasierten E-Mail-Konto eine E-Mail an einen E-Mail-Empfänger in Ihrer Organisation, dessen Domäne der Domäne entspricht, die Sie dem Dienst hinzugefügt haben. Bestätigen Sie mithilfe von Microsoft Outlook oder einem anderen E-Mail-Client die Zustellung der Nachricht an das lokale Postfach.
    
- Wenn Sie einen Test für ausgehende E-Mails durchführen möchten, können Sie von einem Benutzer in Ihrer Organisation aus eine E-Mail an ein webbasiertes E-Mail-Konto senden und überprüfen, ob die Nachricht übermittelt wurde.
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a>Seltener: Hybrid Einrichtung mit Postfächern in der lokalen und in der Cloud

Wenn Sie Exchange-Postfächer lokal und ein oder mehrere Postfächer in der Cloud in Exchange Online haben, verfügen Sie über eine *Hybrid* Einrichtung. In einer Hybrid Einrichtung arbeiten Features wie frei/gebucht-Kalenderfreigabe-und e-Mail-Routing in Ihren lokalen und Cloud-Umgebungen zusammen. Möglicherweise verfügen Sie über ein Hybrid Setup, während Sie Postfächer zu Exchange Online umstellen. Eine Hybridumgebung ist anders als EOP Standalone-Schutz eingerichtet. 
  
Sie können ein Hybrid Szenario auswählen, um die Vorteile von Cloud-basierten e-Mails für die meisten ihrer Mitarbeiter zu nutzen. Sie können dies tun, während auch einige Postfächer lokal gehostet werden; zum Beispiel für Ihre Rechtsabteilung. 
  
Eine Hybrid Einrichtung kann komplex sein, bietet aber viele Vorteile. Weitere Informationen zum Einrichten von Hybrid Szenarien mit Exchange finden Sie unter [Configuring Exchange Hybrid Deployment Features with Office 365 operated by 21Vianet](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d).
  

