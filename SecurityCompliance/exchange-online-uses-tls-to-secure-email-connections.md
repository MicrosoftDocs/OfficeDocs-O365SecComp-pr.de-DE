---
title: Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: 4cde0cda-3430-4dc0-b489-f2c0736c929f
description: Erfahren Sie, wie Exchange Online und Office 365 Transport Layer Security (TLS) und Forward Geheimhaltung (FS) zur sicheren e-Mail-Kommunikation verwenden. Informieren Sie sich auch über das von Microsoft für Exchange Online ausgestellte Zertifikat.
ms.openlocfilehash: 2621bb325c5bf97baa0a25f1e5eb590339856549
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220495"
---
# <a name="how-exchange-online-uses-tls-to-secure-email-connections-in-office-365"></a>Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert

Erfahren Sie, wie Exchange Online und Office 365 Transport Layer Security (TLS) und Forward Geheimhaltung (FS) zur sicheren e-Mail-Kommunikation verwenden. Enthält außerdem Informationen zu dem Zertifikat, das von Microsoft für Exchange Online ausgestellt wurde.
  
## <a name="tls-basics-for-office-365-and-exchange-online"></a>Allgemeine Informationen zu TLS für Office 365 und Exchange Online

Transport Layer Security (TLS) und SSL, die vor TLS kamen, sind kryptografische Protokolle, die die Kommunikation über ein Netzwerk sichern, indem Sicherheitszertifikate zum Verschlüsseln einer Verbindung zwischen Computern verwendet werden. TLS ersetzt Secure Sockets Layer (SSL) und wird häufig als SSL 3,1 bezeichnet. Für Exchange Online wird TLS zum Verschlüsseln der Verbindungen zwischen unseren Exchange-Servern und den Verbindungen zwischen unseren Exchange-Servern und anderen Servern wie Ihren lokalen Exchange-Servern oder den e-Mail-Servern der Empfänger verwendet. Nachdem die Verbindung verschlüsselt wurde, werden alle Daten, die über diese Verbindung gesendet werden, über den verschlüsselten Kanal gesendet. Wenn Sie jedoch eine Nachricht weiterleiten, die über eine TLS-verschlüsselte Verbindung gesendet wurde, wird diese Nachricht nicht unbedingt verschlüsselt. Dies liegt daran, dass TLS die Nachricht vereinfacht ausgedrückt nicht verschlüsselt, sondern nur die Verbindung.
  
Wenn Sie die Nachricht verschlüsseln möchten, müssen Sie eine Verschlüsselungstechnologie verwenden, die den Nachrichteninhalt verschlüsselt, z. B. Office-Nachrichtenverschlüsselung. Unter [Email encryption in Office 365](email-encryption.md) und [Office 365 Message Encryption (OME)](ome.md) erhalten Sie weitere Informationen zu den Verschlüsselungsoptionen für Nachrichten in Office 365. 
  
Wir empfehlen die Verwendung von TLS in Situationen, in denen Sie einen sicheren Kanal der Korrespondenz zwischen Office 365 und ihrer lokalen Organisation oder einer anderen Organisation wie einem Partner einrichten möchten. Exchange Online versucht immer, TLS zuerst zu verwenden, um Ihre e-Mails zu sichern, kann dies jedoch nicht immer tun, wenn die andere Partei keine TLS-Sicherheit bietet. Lesen Sie weiter, um zu erfahren, wie Sie mithilfe von Connectors alle e-Mails an lokale Server oder wichtige Partner ** sichern können. 
  
## <a name="how-exchange-online-uses-tls-between-exchange-online-customers"></a>Wie Exchange Online TLS bei Exchange Online-Kunden verwendet

Exchange Online-Server verschlüsseln Verbindungen mit anderen Exchange Online-Servern in unseren Datencentern immer mithilfe von TLS 1.2. Wenn Sie E-Mails an einen Empfänger senden, der zu Ihrer Office 365-Organisation gehört, wird diese E-Mail-Nachricht automatisch über eine Verbindung gesendet, die mithilfe von TLS verschlüsselt ist. Darüber hinaus werden alle E-Mail-Nachrichten, die Sie an andere Office 365-Kunden senden, über Verbindungen gesendet, die mithilfe von TLS verschlüsselt und mit Forward Secrecy gesichert werden.
  
## <a name="how-office-365-uses-tls-between-office-365-and-external-trusted-partners"></a>Wie Office 365 TLS zwischen Office 365 und externen, vertrauenswürdigen Partnern verwendet

Standardmäßig verwendet Exchange Online immer opportunistisches TLS. Dies führt dazu, dass Exchange Online immer versucht, Verbindungen zunächst mit der sichersten Version von TLS zu verschlüsseln, und dann in der Liste der TLS-Verschlüsselungsverfahren nach unten arbeitet, bis es einen findet, auf dem sich beide Parteien einigen können. Wenn Sie Exchange Online nicht so konfiguriert haben, dass Nachrichten an diesen Empfänger nur über sichere Verbindungen gesendet werden, wird die Nachricht standardmäßig unverschlüsselt gesendet, wenn die Empfängerorganisation keine TLS-Verschlüsselung unterstützt. Opportunistic TLS ist für die meisten Unternehmen ausreichend. Für Unternehmen, die über Compliance-Anforderungen wie Mediziner, Banken oder Behörden verfügen, können Sie Exchange Online jedoch so konfigurieren, dass TLS erforderlich oder erzwungen wird. Anweisungen finden Sie unter [Configure Mail Flow using Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
Wenn Sie TLS zwischen Ihrer Organisation und einer vertrauenswürdigen Partnerorganisation konfigurieren, kann Exchange Online erzwungene TLS zum Erstellen vertrauenswürdiger Kommunikationskanäle verwenden. Erzwungenes TLS erfordert, dass sich Ihre Partnerorganisation bei Exchange Online mit einem Sicherheitszertifikat authentifiziert, um e-Mails an Sie zu senden. Ihr Partner muss dafür eigene Zertifikate verwalten. In Exchange Online verwenden wir Connectors, um Nachrichten zu schützen, die Sie vor dem e-Mail-Anbieter des Empfängers von einem nicht autorisierten Zugriff senden. Informationen zur Verwendung von Connectors zum Konfigurieren des Nachrichtenflusses finden Sie unter [Configure Mail Flow using Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-and-hybrid-exchange-server-deployments"></a>TLS und Exchange Server-Hybridbereitstellungen

Wenn Sie eine hybride Exchange-Bereitstellung verwalten, muss sich der lokale Exchange-Server bei Office 365 mithilfe eines Sicherheitszertifikats authentifizieren, um e-Mails an Empfänger zu senden, deren Postfächer sich nur in Office 365 befinden. Daher müssen Sie Ihre eigenen Sicherheitszertifikate für Ihre lokalen Exchange-Server verwalten. Sie müssen diese Serverzertifikate auch sicher speichern und verwalten. Weitere Informationen zum Verwalten von Zertifikaten in hybridbereitstellungen finden Sie unter [Certificate Requirements for Hybrid Deployments](https://technet.microsoft.com/library/hh563848%28v=exchg.150%29.aspx).
  
## <a name="how-to-set-up-forced-tls-for-exchange-online-in-office-365"></a>Einrichten von erzwungener TLS für Exchange Online in Office 365

Für Exchange Online-Kunden müssen Sie mehr als einen Connector einrichten, der TLS benötigt, damit erzwungenes TLS alle gesendeten und empfangenen e-Mails sichert. Sie benötigen einen Connector für e-Mails, die an Ihre Benutzerpostfächer gesendet werden, und einen weiteren Connector für e-Mails, die von ihren Benutzerpostfächern gesendet werden. Erstellen Sie diese Connectors im Exchange Admin Center in Office 365. Anweisungen finden Sie unter [Configure Mail Flow using Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-certificate-information-for-exchange-online"></a>TLS-Zertifikatinformationen für Exchange Online

Die von Exchange Online verwendeten Zertifikatinformationen werden in der folgenden Tabelle beschrieben. Wenn Ihr Geschäftspartner erzwungenes TLS auf dem e-Mail-Server eingerichtet hat, müssen Sie diese Informationen für Sie bereitstellen. Beachten Sie, dass sich unsere Zertifikate aus Sicherheitsgründen von Zeit zu Zeit ändern. Wir haben ein Update für unser Zertifikat in unseren Rechenzentren eingeführt. Das neue Zertifikat ist gültig vom 3. September 2018.
  
 **Aktuelle Zertifikatinformationen gültig vom 3. September 2018**
  
|**Attribut**|**Wert**|
|:-----|:-----|
|Aussteller des Stammzertifikats der Zertifizierungsstelle  <br/> |GlobalSign-StammzertifizierungsSTELLE – R1 <br/> |
|Name des Zertifikats  <br/> |Mail.Protection.Outlook.com  <br/> |
|Organisation  <br/> |Microsoft Corporation  <br/> |
|Organisationseinheit  <br/> |  <br/> |
|Schlüsselstärke des Zertifikats  <br/> |2048  <br/> |
   
 **VerAltete Zertifikatinformationen gültig bis 3. September 2018**
  
Um einen reibungslosen Übergang zu gewährleisten, werden wir weiterhin die alten Zertifikatinformationen für Ihre Referenz bereitstellen, jedoch sollten Sie die aktuellen Zertifikatinformationen jetzt verwenden.
  
****

|**Attribut**|**Wert**|
|:-----|:-----|
|Aussteller des Stammzertifikats der Zertifizierungsstelle  <br/> |Baltimore CyberTrust Root  <br/> |
|Name des Zertifikats  <br/> |Mail.Protection.Outlook.com  <br/> |
|Organisation  <br/> |Microsoft Corporation  <br/> |
|Organisationseinheit  <br/> |Microsoft Corporation  <br/> |
|Schlüsselstärke des Zertifikats  <br/> |2048  <br/> |
   
## <a name="prepare-for-the-new-exchange-online-certificate"></a>Vorbereiten des neuen Exchange Online-Zertifikats

Das neue Zertifikat wird von einer anderen Zertifizierungsstelle (Certification Authority, CA) aus dem vorherigen von Exchange Online verwendeten Zertifikat ausgestellt. Daher müssen Sie möglicherweise einige Aktionen ausführen, um das neue Zertifikat zu verwenden.

Das neue Zertifikat erfordert die Verbindung mit den Endpunkten der neuen ZERTIFIZIERUNGsSTELLE im Rahmen der Validierung des Zertifikats. Andernfalls kann sich der Nachrichtenfluss negativ auswirken. Wenn Sie Ihre e-Mail-Server mit Firewalls schützen, die es den e-Mail-Servern erlauben, sich mit bestimmten Zielen zu verbinden, müssen Sie überprüfen, ob Ihr Server das neue Zertifikat überprüfen kann. Führen Sie die folgenden Schritte aus, um zu bestätigen, dass Ihr Server das neue Zertifikat verwenden kann:

1. Stellen Sie mithilfe von Windows PowerShell eine Verbindung mit Ihrem lokalen Exchange-Server her, und führen Sie dann den folgenden Befehl aus:  
  `certutil -URL http://crl.globalsign.com/gsorganizationvalsha2g3.crl`
2. Wählen Sie im daraufhin angezeigten Fenster **Abrufen**aus.
3. Wenn das Dienstprogramm seine Prüfung abgeschlossen hat, gibt es einen Status zurück. Wenn der Status **OK**angezeigt wird, kann Ihr e-Mail-Server das neue Zertifikat erfolgreich validieren. Wenn dies nicht der Fall ist, müssen Sie bestimmen, was die Ursache für die Verbindungen ist. Wahrscheinlich müssen Sie die Einstellungen einer Firewall aktualisieren. Die vollständige Liste der Endpunkte, auf die zugegriffen werden muss, sind:
    - OCSP.GlobalSign.com
     - CRL.GlobalSign.com
     - Secure.GlobalSign.com   

NormalerWeise erhalten Sie Updates für Ihre Stammzertifikate automatisch über Windows Update. Einige Bereitstellungen haben jedoch eine zusätzliche Sicherheit, die verhindert, dass diese Aktualisierungen automatisch stattfinden. In diesen gesperrten Bereitstellungen, bei denen Windows Update nicht automatisch Stammzertifikate aktualisieren kann, müssen Sie sicherstellen, dass das richtige Zertifikat der stammzertifizierungsSTELLE installiert wird, indem Sie die folgenden Schritte ausführen:
1.  Stellen Sie mithilfe von Windows PowerShell eine Verbindung mit Ihrem lokalen Exchange-Server her, und führen Sie dann den folgenden Befehl aus:  
  `certmgr.msc`
2. Bestätigen Sie unter **Vertrauenswürdige Stammzertifizierungsstelle/Zertifikate**, dass das neue Zertifikat aufgeführt wird.

## <a name="get-more-information-about-tls-and-office-365"></a>Weitere Informationen zu TLS und Office 365

Eine Liste der unterstützten Verschlüsselungssammlungen finden Sie unter [technische Referenzdetails zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md).
  
[Einrichten von Connectors für den sicheren Nachrichtenfluss mit einer Partnerorganisation](https://technet.microsoft.com/library/dn751021%28v=exchg.150%29.aspx)
  
[Connectors mit erweiterter E-Mail-Sicherheit](https://technet.microsoft.com/library/261d92e4-7371-4555-b781-2062b5bb5278.aspx)
  
[Verschlüsselung in Office 365](encryption.md)
  

