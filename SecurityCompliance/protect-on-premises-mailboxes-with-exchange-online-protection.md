---
title: Schützen von lokalen Postfächern mit Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/1/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- GEU150
- GMA150
- GPA150
- MET150
ms.assetid: c5e95951-da67-4ec7-92c5-982abd477e69
description: Auch wenn Sie beabsichtigen, einige oder alle Ihre lokale Postfächer hosten, können Sie weiterhin die Postfächer mit Exchange Online Protection (EOP) schützen. Um Connectors konfigurieren zu können, muss Ihr Konto ein globaler Office 365-Administrator oder ein Exchange-Unternehmensadministrator (der Rollengruppe "Organisationsverwaltung"). Informationen dazu, wie Office 365-Berechtigungen auf Exchange-Berechtigungen beziehen finden Sie unter Zuweisen von Administratorrollen in Office 365 handelt, das von 21Vianet. Wenn alle Ihre Exchange-Postfächer auf Standortbasierte sind, führen Sie diese Schritte zum Einrichten Ihres EOP-Diensts.
ms.openlocfilehash: 4751bb2183e61d292805d1799519644b77b08c2a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530102"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a>Schützen von lokalen Postfächern mit Exchange Online Protection

> [!NOTE]
> Dieser Artikel gilt nur für Office 365 von 21Vianet in China betrieben wird. 
  
Auch wenn Sie beabsichtigen, einige oder alle Ihre lokale Postfächer hosten, können Sie weiterhin die Postfächer mit Exchange Online Protection (EOP) schützen. Um Connectors konfigurieren zu können, muss Ihr Konto ein globaler Office 365-Administrator oder ein Exchange-Unternehmensadministrator (der Rollengruppe "Organisationsverwaltung"). Informationen dazu, wie Office 365-Berechtigungen auf Exchange-Berechtigungen beziehen finden Sie unter [Zuweisen von Administratorrollen in Office 365 handelt, das von 21Vianet](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac). Wenn alle Ihre Exchange-Postfächer auf Standortbasierte sind, führen Sie diese Schritte zum Einrichten Ihres EOP-Diensts. 
  
## <a name="step-1-use-the-office-365-admin-center-to-add-and-verify-your-domain"></a>Schritt 1: Verwenden von Office 365 Admin Center zum Hinzufügen und Überprüfen der Domäne

1. Navigieren Sie im Office 365 Admin Center zu Setup, um dem Dienst Ihre Domäne hinzuzufügen.
    
2.  Führen Sie die Schritte im Portal so DNS-Hostinganbieter die entsprechenden DNS-Datensätze hinzu, um die domäneneigentümerschaft zu überprüfen. 
    
> [!TIP]
> [Hinzufügen einer Domäne und Benutzer zu Office 365 handelt, das von 21Vianet](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) und [Erstellen von DNS-Einträge für Office 365 beim Verwalten Ihrer DNS-Einträge](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) sind hilfreiche Ressourcen, wie Sie mit dem Dienst Ihre Domäne hinzufügen und Konfigurieren von DNS auf. 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a>Schritt 2: Hinzufügen von Empfängern und Konfigurieren des Domänentyps

Bevor Sie die Übermittlung Ihrer E-Mails zum und vom EOP-Dienst konfigurieren, empfehlen wir, Ihre Empfänger zum Dienst hinzuzufügen. Es gibt dazu verschiedene Möglichkeiten, die in [Verwalten von E-Mail-Benutzern in EOP](https://go.microsoft.com/fwlink/?LinkId=506782) dokumentiert sind. Wenn Sie verzeichnisbasierte Edge-Blockierung (Directory Based Edge Blocking, DBEB) aktivieren möchten, um im Dienst eine Empfängerprüfung zu erzwingen, nachdem Sie Ihre Empfänger hinzugefügt haben, müssen Sie den Domänentyp außerdem auf "Autorisierend" festlegen. Weitere Informationen zur verzeichnisbasierten Edge-Blockierung finden Sie unter [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781).
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Schritt 3: Einrichten des Nachrichtenflusses mithilfe der Exchange-Verwaltungskonsole

Erstellen Sie Connectors in der Exchange-Verwaltungskonsole (EAC), die Nachrichtenübermittlung zwischen EOP und Ihren lokalen e-Mail-Servern zu ermöglichen. Weitere Informationen finden Sie unter [Create erforderliche Connectors grundlegende Nachrichtenflusses über EOP einrichten](https://go.microsoft.com/fwlink/?LinkId=506780).
  
 Woher wissen Sie, dass diese Aufgabe erfolgreich war? 
  
 Verwenden der Remoteverbindungsuntersuchung zum Ausführen von Tests, die e-Mail-Fluss zwischen dem Dienst und der Umgebung überprüft. Weitere Informationen finden Sie im Abschnitt "Verwenden der Remoteverbindungsuntersuchung zum Testen der e-Mail-Übermittlung" unter [Test Mail Flow mit der Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?LinkId=506784).
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a>Schritt 4: Zulassen eingehender SMTP-Verbindungen an Port 25

Nachdem Sie Connectors konfiguriert haben, warten Sie 72 Stunden um Verteilung Ihrer DNS-Datensatz Updates zu ermöglichen. Einschränken des Anschluss daran eingehenden Port 25 SMTP-Datenverkehr auf den Servern Firewall oder der e-Mail-Nachrichten nur aus den Datencentern EOP explizit auf die IP-Adressen zu [URLs und IP-Adressbereiche für Office 365 handelt, das von 21Vianet](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection)aufgeführten akzeptiert werden. Dies schützt Ihre lokale Umgebung durch Beschränken des Bereichs eingehende Nachrichten, die Sie empfangen können. Wenn Sie Einstellungen auf Ihrem e-Mail-Server, die steuern, die IP-Adressen für e-Mail-Weiterleitung eine Verbindung herstellen dürfen verfügen, aktualisieren Sie darüber hinaus auch diese Einstellungen.
  
> [!TIP]
> Konfigurieren Sie Einstellungen auf dem SMTP-Server mit einem Verbindungstimeout von 60 Sekunden. Diese Einstellung ist in den meisten Fällen sinnvoll, da sie eine gewisse Verzögerung erlaubt, falls z. B. eine Nachricht mit einem großen Anhang gesendet wird. 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Schritt 5: Prüfen Sie in der Shell, dass Spamnachrichten in die jeweiligen Junk-E-Mail-Ordner der Benutzer umgeleitet werden.

Um sicherzustellen, dass Spam (Junk) e-Mail ordnungsgemäß an die Junk-e-Mail-Ordner des Benutzers weitergeleitet wird, müssen Sie ein paar Konfigurationsschritte ausführen. Die Schritte werden in [Stellen Sie sicher, dass Spam an die Junk-e-Mail-Ordner des Benutzers geleitet wird](https://go.microsoft.com/fwlink/?LinkId=506804)bereitgestellt. Wenn Sie nicht Nachrichten des Benutzers Junk-e-Mail-Ordner verschieben möchten, können Sie eine andere Aktion durch Ihre inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole bearbeiten wählen. Weitere Informationen finden Sie unter [Configure Content Filter Policies](https://go.microsoft.com/fwlink/?LinkId=506805). 
  
## <a name="step-6-use-the-office-365-admin-center-to-point-your-mx-record-to-eop"></a>Schritt 6: Verwenden von Office 365 Admin Center, um Ihren MX-Eintrag auf EOP zu verweisen

Führen Sie die Schritte zur Konfiguration von Office 365-Domäne, um Ihren MX-Eintrag für Ihre Domäne zu aktualisieren, damit Ihre eingehende e-Mails über EOP fließt. Weitere Informationen können Sie erneut [Erstellen von DNS-Einträgen für Office 365 beim Verwalten Ihrer DNS-Datensätze](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b)verweisen.
  
Woher wissen Sie, dass diese Aufgabe erfolgreich war?
  
 Verwenden der Remoteverbindungsuntersuchung zum Ausführen von Tests, die Ihren MX-Eintrag überprüft. Weitere Informationen finden Sie im Abschnitt "Verwenden den Remote Connectivity Analyzer So testen Sie Ihren MX-Eintrag und ausgehenden Connectors" unter [Test Mail Flow mit der Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?LinkId=506784). 
  
Zu diesem Zeitpunkt haben Sie die Dienstübermittlung für einen ordnungsgemäß konfigurierten Ausgang auf dem lokalen Connector geprüft und sichergestellt, dass Ihr MX-Eintrag auf EOP verwiesen wurde. Sie können nun zusätzlich die folgenden Tests ausführen, um sicherzustellen, dass der Dienst eine E-Mail erfolgreich an Ihre lokale Umgebung versendet hat:
  
- Klicken Sie in der Remoteverbindungsuntersuchung auf die Registerkarte **Office 365**, führen Sie anschließend den **Eingehende SMTP-E-Mail**-Test unter **Internet E-Mail-Tests** aus.
    
- Senden Sie von einem webbasierten E-Mail-Konto eine E-Mail an einen E-Mail-Empfänger in Ihrer Organisation, dessen Domäne der Domäne entspricht, die Sie dem Dienst hinzugefügt haben. Bestätigen Sie mithilfe von Microsoft Outlook oder einem anderen E-Mail-Client die Zustellung der Nachricht an das lokale Postfach.
    
- Wenn Sie einen Test für ausgehende E-Mails durchführen möchten, können Sie von einem Benutzer in Ihrer Organisation aus eine E-Mail an ein webbasiertes E-Mail-Konto senden und überprüfen, ob die Nachricht übermittelt wurde.
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a>Weniger gebräuchlich: eine hybride Setup mit lokale Postfächer und in der Cloud

Wenn Sie Exchange lokale Postfächer verfügen und eine oder mehrere Postfächer in der Cloud in Exchange Online, haben Sie eine *hybride* Setup. In einer Hybrid-Setup Features wie beispielsweise Frei/Gebucht-Informationen zum Freigeben von Kalendern und zur Zusammenarbeit in Ihre lokale e-Mail-routing und cloud-Umgebungen. Ein Hybrid-Setup möglicherweise direkten müssen beim Übergang von Postfächern zu Exchange Online. Eine hybridumgebung ist anders als EOP eigenständige Schutz eingerichtet. 
  
Sie können ein hybridszenario Cloud-basierte e-Mail für den Großteil Ihrer Mitarbeiter nutzen. Dies ist möglich, während Sie auch einige lokale Postfächer hosten; zum Beispiel für die rechtsabteilung. 
  
Ein Hybrid-Setup kann komplex sein, aber es hat viele Vorteile. Weitere Informationen zum Einrichten von hybridszenarien mit Exchange, finden Sie unter [Konfigurieren von Exchange-hybridbereitstellungsfunktionen mit Office 365 handelt, das von 21Vianet](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d).
  

