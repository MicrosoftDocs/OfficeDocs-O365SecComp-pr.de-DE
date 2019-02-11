---
title: Mail Flow Intelligence in Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: Administratoren können sich über die Fehlercodes informieren, die Übermittlung von Nachrichten mithilfe von Connectors in Office 365 (auch bekannt als e-Mail-Fluss Intelligence) zugeordnet sind.
ms.openlocfilehash: 9f27dfd4c265eb62028d68c27764183202692ef4
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327087"
---
# <a name="mail-flow-intelligence-in-office-365"></a>Mail Flow Intelligence in Office 365

In der Regel verwenden Sie eine Verbindung zum Weiterleiten von e-Mail-Nachrichten von Office 365-Organisation an Ihre lokale e-Mail-Umgebung. Sie können auch eine Verbindung zum Weiterleiten von Nachrichten aus Office 365 zu einer Partnerorganisation verwenden. Wenn Office 365 diese Nachrichten über den Connector können nicht übermittelt werden, sind sie Office 365 in der Warteschlange. Office 365 wird weiterhin zum Wiederholen der Übermittlung für jede Nachricht 48 Stunden. Nach 48 Stunden läuft die Nachricht in der Warteschlange, und die Nachricht wird an den ursprünglichen Absender in einen non-Delivery Report (auch bekannt als ein Unzustellbarkeitsbericht oder Springeffekt Nachricht) zurückgegeben.

Office 365 generiert einen Fehler, wenn eine Nachricht mit einem Connector übermittelt werden kann. In diesem Thema werden die häufigsten Fehler und deren Lösung beschrieben. Queuing und Benachrichtigung Fehler für unzustellbare Nachrichten über Connectors ist allgemein, als _e-Mail-Fluss Intelligence_bezeichnet.

## <a name="error-code-450-44312-dns-query-failed"></a>Fehlercode: 450 4.4.312 DNS-Abfragefehler

Dieser Fehler bedeutet normalerweise, Office 365 haben versucht, an den Smarthost verbinden, die in den Connector, aber die DNS-Abfrage zum Suchen von den Smarthost IP-Adressen konnte nicht angegeben ist. Die möglichen Ursachen für diesen Fehler sind:

- Es gibt ein Problem mit dem DNS-Hostingdienst Ihrer Domäne (Partei, die die autoritativen Namensserver für Ihre Domäne verwaltet).

- Ihre Domäne ist vor kurzem abgelaufen. D.h. der MX-Eintrag kann nicht abgerufen werden.

- Der MX-Eintrag Ihrer Domäne hat sich kürzlich geändert, und die Office 365-DNS-Server enthalten weiterhin zuvor zwischengespeicherte DNS-Informationen für Ihre Domäne.

### <a name="how-do-i-fix-error-code-450-44312"></a>Wie behebe ich Fehlercode 450 4.4.312?

- Arbeiten Sie mit Ihrer DNS-Hostingdienst zu identifizieren und beheben Sie das Problem mit der Domäne.

- Wenn der Fehler aus der Partnerorganisation (beispielsweise eine 3. Partei Cloud-Dienstanbieter) ist, wenden Sie sich an Ihren Händler, um das Problem zu beheben.

## <a name="error-code-450-44315-connection-timed-out"></a>Fehlercode: 450 4.4.315 Timeout bei der Verbindung

In der Regel bedeutet dies, dass Office 365 e-Mail auf den Zielserver keine Verbindung herstellen können. Die Fehlerdetails werden das Problem erläutert. Zum Beispiel:

- Ihren lokalen e-Mail-Server ist ausgefallen.

- Es ist ein Fehler in den Einstellungen des intelligenten Hosts des Konnektors vorhanden. Office 365 versucht, ein Verbindung zur falschen IP-Adresse herzustellen.

### <a name="how-do-i-fix-error-code-450-44315"></a>Wie behebe ich Fehlercode 450 4.4.315?

- Erfahren Sie, welches Szenario für Sie gilt, und Korrekturen Sie die erforderlichen. Beispielsweise müssen wenn e-Mail-Fluss ordnungsgemäß arbeitet, und Sie nicht die Connectoreinstellungen geändert haben, überprüfen Sie die lokalen e-Mail-Umgebung, ob der Server ausgefallen ist, oder ob wurden alle Änderungen an die Netzwerkinfrastruktur (z. b Sie haben Internetdienstanbietern, geändert, sodass Sie verschiedene IP-Adressen haben).

- Wenn der Fehler aus der Partnerorganisation (beispielsweise eine 3. Partei Cloud-Dienstanbieter) ist, wenden Sie sich an Ihren Händler, um das Problem zu beheben.

## <a name="error-code-450-44316-connection-refused"></a>Fehlercode: 450 4.4.316 Verbindung abgelehnt

Dieser Fehler bedeutet normalerweise, dass Office 365 einen Fehler aufgetreten ist, bei dem Versuch, mit dem Ziel e-Mail-Server herstellen. Eine mögliche Ursache für diesen Fehler ist, dass die Firewall Verbindungen von Office 365-IP-Adressen blockiert. Oder dieser Fehler möglicherweise entwurfsbedingt Wenn Sie vollständig migriert haben Ihre lokale e-Mail-System zu Office 365, und fahren Sie Ihre lokale e-Mail-Umgebung.

### <a name="how-do-i-fix-error-code-450-44316"></a>Wie behebe ich Fehlercode 450 4.4.316?

- Wenn Sie Postfächer in Ihrer lokalen Umgebung haben, müssen Sie zum Ändern Ihrer Firewalleinstellungen, um Verbindungen von Office 365 IP-Adressen auf TCP-Port 25 mit Ihrem lokalen e-Mail-Servern zu ermöglichen. Eine Übersicht über die Office 365-IP-Adressen finden Sie unter [Office 365-URLs und IP-Adressbereiche](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).

- Wenn keine weiteren Nachrichten an Ihre lokale Umgebung übermittelt werden sollen, klicken Sie in der Warnung auf **Jetzt korrigieren**, damit Office 365 die Nachrichten mit ungültigen Empfängern sofort ablehnen kann. Dadurch wird das Risiko verringert, dass das Kontingent für ungültige Empfänger Ihrer Organisation überschritten wird, wodurch die normale Nachrichtenübermittlung beeinträchtigt werden könnte. Alternativ können Sie das Problem mit den folgenden Anweisungen manuell beheben:

  - Deaktivieren Sie in der [Exchange-Verwaltungskonsole (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365 oder löschen Sie den Connector, der e-Mail von Office 365 mit der lokalen e-Mail-Umgebung übermittelt:

    1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Connectors**.

    2. Wählen Sie die Verbindung mit dem Wert **von** **Office 365** und **den Wert **Ihrer Organisation e-Mail-Server** ** , und führen Sie einen der folgenden Schritte aus:

       - Löschen Sie den Connector, indem Sie auf **Löschen** ![Symbol "entfernen"](media/adf01106-cc79-475c-8673-065371c1897b.gif)

       - Deaktivieren Sie den Connector durch Klicken auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) , und **schalten Sie ihn**deaktivieren.

  - Ändern Sie die akzeptierte Domäne in Office 365, die Ihre lokalen e-Mail-Umgebung von **Internes Relay** **authoritative**zugeordnet ist. Anweisungen finden Sie unter [Manage akzeptierte Domänen im Exchange, Online](https://go.microsoft.com/fwlink/p/?linkid=785428).

  **Hinweis**: in der Regel diese Änderungen werden zwischen 30 Minuten und einer Stunde wirksam wird. Nach einer Stunde stellen Sie sicher, dass die Fehlermeldung nicht mehr angezeigt.

- Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a>Fehlercode: 450 4.4.317 Fehler beim Herstellen der Verbindung mit Remote-Server

Dieser Fehler bedeutet normalerweise, Office 365 mit dem Ziel e-Mail-Server verbunden, aber der Server mit einem sofortige Fehler geantwortet, oder die Verbindung Anforderungen nicht erfüllen. Die Fehlerdetails werden das Problem erläutert. Zum Beispiel:

- Ziel e-Mail Serverantwort mit einer Fehlermeldung "Dienst nicht verfügbar" gibt den Server an kann keine Kommunikation mit Office 365 verwalten.

- Der Connector wird so konfiguriert, dass TLS erforderlich, aber der Ziel-e-Mail-Server unterstützt TLS nicht.

### <a name="how-do-i-fix-error-code-450-44317"></a>Wie behebe ich Fehlercode 450 4.4.317?

- Überprüfen Sie die TLS-Einstellungen und die Zertifikate auf Ihren lokalen e-Mail-Servern und die TLS-Einstellungen für den Connector ein.

- Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a>Fehlercode: 450 4.4.318 Verbindung wurde plötzlich geschlossen

Dieser Fehler bedeutet normalerweise, dass Office 365 ist haben Probleme bei Kommunikation mit Ihrer lokalen e-Mail-Umgebung, damit die Verbindung unterbrochen wurde. Die möglichen Ursachen für diesen Fehler sind:

- Ihre Firewall verwendet SMTP-Paketprüfungsregeln, und diese Regeln funktionieren nicht ordnungsgemäß.

- Ihren lokalen e-Mail-Server ist nicht arbeiten ordnungsgemäß (z. B., Dienst hängt, Abstürze oder geringe Systemressourcen), welcher den Server zu Timeouts verursacht, und schließen Sie die Verbindung zu Office 365.

- Es treten Netzwerkprobleme zwischen Ihrer lokalen Umgebung und Office 365 auf.

### <a name="how-do-i-fix-error-code-450-44318"></a>Wie behebe ich Fehlercode 450 4.4.318?

- Erfahren Sie, welches Szenario für Sie gilt, und nehmen Sie die erforderlichen Korrekturen vor.

- Wenn das Problem durch Netzwerkprobleme zwischen Ihrer lokalen Umgebung und Office 365 verursacht wird, wenden Sie sich an Ihr Netzwerkteam, um das Problem zu beheben.

- Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.

## <a name="error-code-450-47320-certificate-validation-failed"></a>Fehlercode: 450 4.7.320 Zertifikatüberprüfungsfehler

Dieser Fehler bedeutet normalerweise, dass Office 365-Fehler beim Versuch, die das Zertifikat des Zielservers e-Mails zu überprüfen. Die Fehlerdetails werden den Fehler erläutert. Zum Beispiel:

- Zertifikat abgelaufen

- Konflikt mit dem Zertifikatantragsteller

- Zertifikat ist nicht mehr gültig

### <a name="how-do-i-fix-error-code-450-47320"></a>Wie behebe ich Fehlercode 450 4.7.320?

- Beheben das Zertifikat oder die Einstellungen für den Connector, damit Nachrichten in Office 365 in der Warteschlange geliefert werden können.

- Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.

## <a name="other-error-codes"></a>Andere Fehlercodes

Office 365 ist Probleme übermitteln von Nachrichten an Ihre lokale oder partner-e-Mail-Server. Verwenden Sie die Informationen **Zielserver** Fehler, um das Problem in Ihrer Umgebung zu überprüfen, oder ändern Sie den Connector aus, wenn ein Konfigurationsfehler. 

Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.
