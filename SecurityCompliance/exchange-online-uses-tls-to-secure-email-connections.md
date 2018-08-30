---
title: Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 4cde0cda-3430-4dc0-b489-f2c0736c929f
description: Hier erfahren Sie, wie Exchange Online und Office 365 Transport Layer Security (TLS) und Forward Secrecy (FS) verwenden sichere e-Mail-Kommunikation. Abrufen von Informationen über das von Microsoft für Exchange Online ausgestellte Zertifikat auch.
ms.openlocfilehash: 079a6f574838f5710dbbbcb53726799abfae1d3a
ms.sourcegitcommit: ddfa0ac1f8ef95a78dcc1468241ef29363d56b5b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/30/2018
ms.locfileid: "23520144"
---
# <a name="how-exchange-online-uses-tls-to-secure-email-connections-in-office-365"></a>Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert

Hier erfahren Sie, wie Exchange Online und Office 365 Transport Layer Security (TLS) und Forward Secrecy (FS) verwenden sichere e-Mail-Kommunikation. Enthält Informationen über das Zertifikat von Microsoft für Exchange Online.
  
## <a name="tls-basics-for-office-365-and-exchange-online"></a>Allgemeine Informationen zu TLS für Office 365 und Exchange Online

Transport Layer Security (TLS) und SSL TLS, bevor Sie der Begleitdokumentation werden kryptografische Protokolle, die Kommunikation mithilfe von Sicherheitszertifikate zum Verschlüsseln von einer Verbindungs zwischen Computern über ein Netzwerk zu sichern. TLS hat Vorrang vor dem Secure Sockets Layer (SSL) und wird häufig als SSL 3.1 bezeichnet. Für Exchange Online verwenden wir TLS zum Verschlüsseln von Verbindungen zwischen unsere Exchange-Server und die Verbindungen zwischen unsere Exchange-Server und anderen Servern wie Ihre lokale Exchange-Server oder der Empfänger e-Mail-Servern. Nachdem die Verbindung verschlüsselt ist, werden alle Daten, die über diese Verbindung gesendet über den verschlüsselten Kanal gesendet. Wenn Sie eine Nachricht, die über eine TLS-verschlüsselte Verbindung gesendet wurde weiterleiten, ist nicht jedoch unbedingt die Nachricht verschlüsselt. Dies liegt daran, einfach ausgedrückt, TLS verschlüsseln nicht der Nachricht, nur die Verbindung.
  
Wenn Sie die Nachricht verschlüsseln möchten, müssen Sie eine Verschlüsselungstechnologie verwenden, die den Nachrichteninhalt verschlüsselt, z. B. Office-Nachrichtenverschlüsselung. Unter [Email encryption in Office 365](email-encryption.md) und [Office 365 Message Encryption (OME)](ome.md) erhalten Sie weitere Informationen zu den Verschlüsselungsoptionen für Nachrichten in Office 365. 
  
Wir empfehlen die Verwendung von TLS in Situationen, in dem Sie einen sicheren Kanal Korrespondenz zwischen Office 365 und Ihrer lokalen Organisation oder einer anderen Organisation, beispielsweise von einem Partner einrichten möchten. Exchange Online immer versucht, TLS zunächst mit dem Ihre e-Mails secure jedoch immer dies nicht möglich, wenn die andere Partei keine TLS-Sicherheit bietet. Lassen Sie lesen, um zu ermitteln, wie Sie mithilfe von *Connectors*alle e-Mails an den lokalen Servern oder wichtige Partner sichern können. 
  
## <a name="how-exchange-online-uses-tls-between-exchange-online-customers"></a>Wie Exchange Online TLS bei Exchange Online-Kunden verwendet

Exchange Online-Server verschlüsseln Verbindungen mit anderen Exchange Online-Servern in unseren Datencentern immer mithilfe von TLS 1.2. Wenn Sie E-Mails an einen Empfänger senden, der zu Ihrer Office 365-Organisation gehört, wird diese E-Mail-Nachricht automatisch über eine Verbindung gesendet, die mithilfe von TLS verschlüsselt ist. Darüber hinaus werden alle E-Mail-Nachrichten, die Sie an andere Office 365-Kunden senden, über Verbindungen gesendet, die mithilfe von TLS verschlüsselt und mit Forward Secrecy gesichert werden.
  
## <a name="how-office-365-uses-tls-between-office-365-and-external-trusted-partners"></a>Verwendung von TLS zwischen Office 365 und externen, vertrauenswürdigen Partnern in Office 365

Standardmäßig verwendet Exchange Online immer Opportunistische TLS. Dies bedeutet, dass Exchange Online immer zum Verschlüsseln von Verbindungen mit der sicherste Version von TLS zuerst versucht, und klicken Sie dann so arbeitet Sie in der Liste der TLS-Chiffre, bis er eine findet auf dem die beiden Parteien einigen können. Es sei denn, Sie Exchange Online konfiguriert haben, um sicherzustellen, dass Nachrichten an diesen Empfänger nur über eine sichere Verbindung gesendet werden, wird dann standardmäßig die Nachricht unverschlüsselt gesendet, wenn die Empfänger Organisation TLS-Verschlüsselung nicht unterstützen. Opportunistische TLS ist ausreichend für die meisten Unternehmen. Jedoch für Unternehmen, die Compliance-Bestimmungen wie Medical, Bankgeschäfte oder Regierungsbehörden verfügen, können Sie Exchange Online erforderlich ist, oder erzwingen, TLS. Anweisungen finden Sie unter [Configure e-Mail-Fluss mithilfe von Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
Wenn Sie TLS zwischen Ihrer Organisation und einer vertrauenswürdigen Partnerorganisation konfigurieren möchten, können Exchange Online erzwungene TLS Sie vertrauenswürdige Kommunikationskanäle erstellen. Erzwungene TLS erfordert Partnerorganisation zu Exchange Online mit einem Sicherheitszertifikat authentifizieren, um e-Mail-Nachrichten an Sie senden. Ihr Partner müssen eigene Zertifikate verwalten, um diese Schritte durchführen. In Exchange Online verwenden wir Connectors, um Nachrichten zu schützen, die Sie vor nicht autorisiertem Zugriff senden, bevor an den Empfänger e-Mail-Anbieter Ankunft. Informationen zur Verwendung von Connectors zum Konfigurieren von e-Mail-Fluss finden Sie unter [Configure e-Mail-Fluss mithilfe von Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-and-hybrid-exchange-server-deployments"></a>TLS und Exchange Server-Hybridbereitstellungen

Wenn Sie eine hybride Exchange-Bereitstellung verwalten, werden Ihre lokale Exchange Server-Anforderungen zum Authentifizieren zu Office 365 verwendet ein Sicherheitszertifikat, um e-Mails an Empfänger gesendet, deren Postfächer nur in Office 365. Daher müssen Sie eigene Sicherheitszertifikate für den lokalen Exchange-Servern zu verwalten. Sie müssen auch sicher speichern und verwalten diese Serverzertifikate. Weitere Informationen zum Verwalten von Zertifikaten in hybridbereitstellungen finden Sie unter [zertifikatanforderungen für hybridbereitstellungen](https://technet.microsoft.com/library/hh563848%28v=exchg.150%29.aspx).
  
## <a name="how-to-set-up-forced-tls-for-exchange-online-in-office-365"></a>Einrichten von erzwungener TLS für Exchange Online in Office 365

Für Exchange Online-Kunden müssen in der Reihenfolge für die erzwungene TLS funktioniert zum Sichern aller Ihrer gesendete und empfangene e-Mails, die Sie mehrere Connector einrichten, die TLS erforderlich sind. Sie benötigen einen Connector für e-Mail an die Benutzerpostfächer und den anderen Connector für e-Mails, die aus den Benutzerpostfächern gesendet. Erstellen Sie diese Connectors im Exchange Administrationscenter in Office 365. Anweisungen finden Sie unter [Configure e-Mail-Fluss mithilfe von Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-certificate-information-for-exchange-online"></a>TLS-Zertifikatinformationen für Exchange Online

Die Zertifikatinformationen, die von Exchange Online verwendet wird in der folgenden Tabelle beschrieben. Wenn Ihre Geschäftspartner erzwungene TLS auf ihre e-Mail-Server eingerichtet wird, müssen Sie diese Informationen bereitgestellt. Beachten Sie, aus Sicherheitsgründen unsere Zertifikate von Zeit zu Zeit zu ändern. Wir haben, ein Update zu unserer Zertifikat in unseren Rechenzentren zurückgesetzt. Das neue Zertifikat ist gültig 3 September 2018.
  
 **Aktuelle Zertifikatinformationen aus 3 September 2018 ungültig**
  
|**Attribut**|**Wert**|
|:-----|:-----|
|Aussteller des Stammzertifikats der Zertifizierungsstelle  <br/> |Informationen Root CA – R1 <br/> |
|Name des Zertifikats  <br/> |Mail.Protection.Outlook.com  <br/> |
|Organisation  <br/> |Microsoft Corporation  <br/> |
|Organisationseinheit  <br/> |  <br/> |
|Schlüsselstärke des Zertifikats  <br/> |2048  <br/> |
   
 **Gültig bis 3 September 2018 veraltete Zertifikatinformationen**
  
Um einen reibungslosen Übergang zu gewährleisten, wir bietet weiterhin die alte Zertifikatinformationen für den Verweis für eine Weile, Sie sollten jedoch von nun an die aktuelle Zertifikatinformationen verwenden.
  
****

|**Attribut**|**Wert**|
|:-----|:-----|
|Aussteller des Stammzertifikats der Zertifizierungsstelle  <br/> |Baltimore CyberTrust Root  <br/> |
|Name des Zertifikats  <br/> |Mail.Protection.Outlook.com  <br/> |
|Organisation  <br/> |Microsoft Corporation  <br/> |
|Organisationseinheit  <br/> |Microsoft Corporation  <br/> |
|Schlüsselstärke des Zertifikats  <br/> |2048  <br/> |
   
## <a name="prepare-for-the-new-exchange-online-certificate"></a>Vorbereiten Sie für das neue Zertifikat Exchange Online

Das neue Zertifikat wird aus dem vorherigen Zertifikat von Exchange Online verwendeten durch eine andere Zertifizierungsstelle (CA) ausgestellt. Daher müssen Sie möglicherweise einige Aktionen durchführen, um das neue Zertifikat verwenden.

Das neue Zertifikat erfordert eine Verbindung mit der Endpunkte der neuen Zertifizierungsstelle im Rahmen der Überprüfung des Zertifikats. Andernfalls kann dazu führen, dass e-Mail-Fluss beeinträchtigt wird. Wenn Sie Ihre Mail-Server mit Firewalls, mit denen nur die e-Mail-Servern herstellen der Verbindung mit bestimmten Ziele müssen Sie überprüfen schützen, ob Ihre Server das neue Zertifikat zu überprüfen kann. Um zu bestätigen, dass der Server das neue Zertifikat verwenden können, führen Sie diese Schritte aus:

1. Verbinden mit Ihrem lokalen Exchange-Server mithilfe von Windows PowerShell, und führen Sie dann den folgenden Befehl aus:  
  `certutil -URL http://crl.globalsign.com/gsorganizationvalsha2g3.crl`
2. Wählen Sie auf das Fenster, das angezeigt wird, **Abrufen**.
3. Abschluss das Dienstprogramm die Überprüfung nach wird der Status zurückgegeben. Wenn der Status **OK**angezeigt wird, kann das neue Zertifikat von Ihrem e-Mail-Server erfolgreich überprüfen. Wenn dies nicht der Fall ist, müssen Sie feststellen, welche die Verbindungen zu einem Fehler beim verursacht. In den meisten Fällen müssen Sie die Einstellungen einer Firewall zu aktualisieren. Die vollständige Liste der Endpunkte, die erfolgen müssen umfassen:
    - OCSP.GlobalSign.com
     - CRL.GlobalSign.com
     - Secure.GlobalSign.com   

In der Regel erhalten Sie Updates auf Ihre Stammzertifikate automatisch über Windows Update. Jedoch einige Bereitstellungen zusätzlichen Sicherheit erfüllt sein, die verhindert, dass diese Updates automatisch auftritt. Diese gesperrten-Bereitstellungen, in dem Windows Update automatisch Stammzertifikate aktualisieren können, müssen Sie sicherstellen, dass der richtige Stammzertifizierungsstelle installiert ist, indem Sie diese Schritte ausführen:
1.  Verbinden mit Ihrem lokalen Exchange-Server mithilfe von Windows PowerShell, und führen Sie dann den folgenden Befehl aus:  
  `certmgr.msc`
2. Vergewissern Sie sich, dass das neue Zertifikat aufgeführt ist, klicken Sie unter **Vertrauenswürdige Stammzertifizierungsstellen/Zertifikaten**.

## <a name="get-more-information-about-tls-and-office-365"></a>Weitere Informationen zu TLS und Office 365

Eine Liste der unterstützten Verschlüsselungsanbieter-Suites finden Sie unter [Technische Referenz Details über die Verschlüsselung in Office 365](technical-reference-details-about-encryption.md).
  
[Einrichten von Connectors für den sicheren Nachrichtenfluss mit einer Partnerorganisation](https://technet.microsoft.com/library/dn751021%28v=exchg.150%29.aspx)
  
[Connectors mit erweiterter E-Mail-Sicherheit](https://technet.microsoft.com/library/261d92e4-7371-4555-b781-2062b5bb5278.aspx)
  
[Verschlüsselung in Office 365](encryption.md)
  

