---
title: Mail Flow Intelligence in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/27/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: 'Normalerweise verwenden Sie eine Verbindung zum Weiterleiten von Nachrichten aus Office 365-Organisation für Ihre lokale messaging-Umgebung. Sie können auch eine Verbindung zum Weiterleiten von Nachrichten aus Office 365 zu einer Partnerorganisation verwenden. Wenn Office 365 diese Nachrichten über den Connector können nicht übermittelt werden, sind sie Office 365 in der Warteschlange. '
ms.openlocfilehash: 4effbb783d6ba8f3b33d0aed446e031193d2f2a3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002720"
---
# <a name="mail-flow-intelligence-in-office-365"></a>Mail Flow Intelligence in Office 365
  
In der Regel verwenden Sie einen Konnektor zum Weiterleiten von Nachrichten aus Ihrer Office 365-Organisation in Ihre lokale Nachrichtenumgebung. Sie können auch einen Konnektor verwenden, um Nachrichten von Office 365 zu einer Partnerorganisation weiterzuleiten. Wenn Office 365 diese Nachrichten nicht über den Konnektor senden kann, werden sie in die Office 365-Warteschlange gestellt. Office 365 versucht 48 Stunden, die Nachrichten zu senden. Nach 48 Stunden läuft die Nachricht in der Warteschlange ab, und die Nachricht wird an den ursprünglichen Absender in einem Unzustellbarkeitsbericht zurückgegeben (auch bekannt als NDR oder Unzustellbarkeitsnachricht).
  
Office 365 generiert einen Fehler, wenn eine Nachricht nicht mithilfe eines Konnektors gesendet werden kann. In diesem Thema werden die am häufigsten auftretenden Fehler und die dazugehörigen Lösungen beschrieben. Warteschlangen- und Benachrichtigungsfehler für unzustellbare Nachrichten, die über Konnektoren gesendet werden, sind als intelligente Nachrichtenübermittlung bekannt.
  
 **Inhalt**
  
- [Fehlercode: 450 4.4.312 DNS-Abfragefehler](mail-flow-intelligence-in-office-365.md#ErrorCode44312)
    
- [Fehlercode: 450 4.4.315 Timeout bei der Verbindung](mail-flow-intelligence-in-office-365.md#ErrorCode44315)
    
- [Fehlercode: 450 4.4.316 Verbindung abgelehnt](mail-flow-intelligence-in-office-365.md#ErrorCode44316)
    
- [Fehlercode: 450 4.4.317 Fehler beim Herstellen der Verbindung mit Remote-Server](mail-flow-intelligence-in-office-365.md#ErrorCode44317)
    
- [Fehlercode: 450 4.4.318 Verbindung wurde plötzlich geschlossen](mail-flow-intelligence-in-office-365.md#ErrorCode44318)
    
- [Fehlercode: 450 4.7.320 Zertifikatüberprüfungsfehler](mail-flow-intelligence-in-office-365.md#ErrorCode47320)
    
## <a name="error-code-450-44312-dns-query-failed"></a>Fehlercode: 450 4.4.312 DNS-Abfragefehler

Dieser Fehler bedeutet in der Regel, dass Office 365 versucht hat, eine Verbindung zum intelligenten Host herzustellen, der im Konnektor angegeben ist, aber die DNS-Abfrage zum Ermitteln der IP-Adressen des intelligenten Hosts ist fehlgeschlagen. Mögliche Ursachen für diesen Fehler sind:
  
- Es gibt ein Problem mit dem DNS-Hostingdienst Ihrer Domäne (Partei, die die autoritativen Namensserver für Ihre Domäne verwaltet).
    
- Ihre Domäne ist vor kurzem abgelaufen. D.h. der MX-Eintrag kann nicht abgerufen werden.
    
- Der MX-Eintrag Ihrer Domäne hat sich kürzlich geändert, und die Office 365-DNS-Server enthalten weiterhin zuvor zwischengespeicherte DNS-Informationen für Ihre Domäne.
    
Sie müssen das DNS-Problem beheben, indem Sie mit Ihrem DNS-Hostingdienst arbeiten.
  
Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.
  
## <a name="error-code-450-44315-connection-timed-out"></a>Fehlercode: 450 4.4.315 Timeout bei der Verbindung

Dies bedeutet normalerweise, dass Office 365 keine Verbindung mit dem Ziel-Messagingserver herstellen kann. Die Fehlerdetails erläutern das Problem. Beispiel:
  
- Ihr lokaler Messagingserver ist ausgefallen.
    
- Es ist ein Fehler in den Einstellungen des intelligenten Hosts des Konnektors vorhanden. Office 365 versucht, ein Verbindung zur falschen IP-Adresse herzustellen.
    
Erfahren Sie, welches Szenario für Sie gilt, und nehmen Sie die erforderlichen Korrekturen vor. Wenn beispielsweise der Nachrichtenfluss korrekt funktioniert hat und Sie die Konnektoreinstellungen nicht geändert haben, müssen Sie in Ihrer lokalen Messagingumgebung prüfen, ob der Server ausgefallen ist oder ob Änderungen an Ihrer Netzwerkinfrastruktur vorgenommen wurden (beispielsweise Änderung der Internet-Dienstanbieter, sodass sie jetzt eine andere IP-Adresse haben).
  
Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.
  
## <a name="error-code-450-44316-connection-refused"></a>Fehlercode: 450 4.4.316 Verbindung abgelehnt

Dieser Fehler bedeutet normalerweise, dass Office 365 einen Fehler beim Versuch festgestellt hat, eine Verbindung mit dem Ziel-Messagingserver herzustellen. Eine mögliche Ursache für diesen Fehler ist, dass Ihre Firewall Verbindungen von Office 365-IP-Adressen blockiert. Dieser Fehler ist möglicherweise beabsichtigt, wenn Sie Ihr lokales Messaging-System vollständig zu Office 365 migriert haben und die lokale Messaging-Umgebung herunterfahren.
  
- Wenn Ihre lokale Umgebung Postfächer aufweist, müssen Sie Ihre Firewalleinstellungen ändern, um Verbindungen von Office 365-IP-Adressen auf TCP-Port 25 zu Ihren lokalen Messagingservern zuzulassen. Eine Liste der Office 365-IP-Adressen finden Sie unter [Office 365-URLs und -IP-Adressbereiche](https://go.microsoft.com/fwlink/p/?linkid=228887).
    
- Wenn keine weiteren Nachrichten an Ihre lokale Umgebung übermittelt werden sollen, klicken Sie in der Warnung auf **Jetzt korrigieren**, damit Office 365 die Nachrichten mit ungültigen Empfängern sofort ablehnen kann. Dadurch wird das Risiko verringert, dass das Kontingent für ungültige Empfänger Ihrer Organisation überschritten wird, wodurch die normale Nachrichtenübermittlung beeinträchtigt werden könnte. Alternativ können Sie das Problem mit den folgenden Anweisungen manuell beheben: 
    
  - Deaktivieren oder Löschen der Verbindung von Office 365 mit der lokalen Umgebung: Office 365 Administrationscenter \> **Admin zentriert** \> **Exchange** \> **E-Mail-Fluss** \> **Connectors** \> wählen Sie die Verbindung mit dem Wert **von** **Office 365** und die **zu** **Ihrer Organisation e-Mail-Server**-Wert. Löschen Sie den Connector, indem Sie auf **Löschen**![Löschsymbol](media/ITPro-EAC-DeleteIcon.gif), oder deaktivieren Sie den Connector durch Klicken auf **Bearbeiten** ![Bearbeitungssymbol](media/ITPro-EAC-EditIcon.gif) , und **schalten Sie ihn**deaktivieren.
    
  - Ändern Sie die akzeptierte Domäne in Office 365, die Ihrer lokalen Nachrichtenumgebung zugeordnet ist, von **Internes Relay** in **Autorisierend**. Anweisungen finden Sie unter [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).
    
    **Hinweis**: in der Regel diese Änderungen werden zwischen 30 Minuten und einer Stunde wirksam wird. Nach einer Stunde stellen Sie sicher, dass die Fehlermeldung nicht mehr angezeigt.
    
Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.
  
## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a>Fehlercode: 450 4.4.317 Fehler beim Herstellen der Verbindung mit Remote-Server

Dieser Fehler bedeutet normalerweise, dass Office 365 mit dem Ziel-Messagingserver verbunden ist, aber der Server mit einem sofortigen Fehler geantwortet hat oder nicht die Verbindungsanforderungen erfüllt. Die Fehlerdetails erläutern das Problem. Beispiel:
  
- Der Ziel-Messagingserver hat mit dem Fehler „Dienst nicht verfügbar" geantwortet. Dies bedeutet, dass der Server nicht mit Office 365 kommunizieren kann.
    
- Der Konnektor erfordert gemäß Konfiguration TLS, aber der Ziel-Messagingserver unterstützt TLS nicht.
    
Überprüfen Sie die TLS-Einstellungen und Zertifikate auf Ihren lokalen Messagingservern und die TLS-Einstellungen auf dem Konnektor.
  
Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.
  
## <a name="error-code-450-44318-connection-was-closed-abruptly"></a>Fehlercode: 450 4.4.318 Verbindung wurde plötzlich geschlossen

Dieser Fehler bedeutet normalerweise, dass Office 365 Probleme hat, mit Ihrer lokalen Messagingumgebung zu kommunizieren, sodass die Verbindung getrennt wurde. Mögliche Ursachen für diesen Fehler sind:
  
- Ihre Firewall verwendet SMTP-Paketprüfungsregeln, und diese Regeln funktionieren nicht ordnungsgemäß.
    
- Ihr lokaler Messagingserver funktioniert nicht korrekt (Beispiele: Dienst hängt, Dienst stürzt ab oder geringe Systemressourcen), was zu einem Server-Timeout und zum Schließen der Verbindung mit Office 365 führt.
    
- Es treten Netzwerkprobleme zwischen Ihrer lokalen Umgebung und Office 365 auf. Wenn das Problem weiterhin besteht, wenden Sie sich zur Behebung des Problems an Ihr Netzwerkteam.
    
Erfahren Sie, welches Szenario für Sie gilt, und nehmen Sie die erforderlichen Korrekturen vor.
  
Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.
  
## <a name="error-code-450-47320-certificate-validation-failed"></a>Fehlercode: 450 4.7.320 Zertifikatüberprüfungsfehler

Dieser Fehler bedeutet normalerweise, dass Office 365 beim Versuch, das Zertifikat des Ziel-Messagingservers zu überprüfen, einen Fehler festgestellt hat. Die Fehlerdetails erläutern den Fehler. Beispiel:
  
- Zertifikat abgelaufen
    
- Konflikt mit dem Zertifikatantragsteller
    
- Zertifikat ist nicht mehr gültig
    
Aktualisieren Sie das Zertifikat oder den Konnektor, sodass Nachrichten in der Warteschlange in Office 365 gesendet werden können.
  
Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.
  
## <a name="other-error-codes"></a>Andere Fehlercodes

Office 365 hat Probleme beim Senden von Nachrichten an Ihren lokalen Messagingserver oder Partner-Messagingserver. Verwenden Sie die Informationen zum **Zielserver** im Fehler, um das Problem in Ihrer Umgebung zu untersuchen, oder ändern Sie den Konnektor bei einem Konfigurationsfehler. 
  
Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.
  

