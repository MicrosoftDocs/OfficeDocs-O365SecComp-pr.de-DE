---
title: S/MIME für die Nachrichtensignierung und -verschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: S/MIME können Sie e-Mail-Nachrichten verschlüsseln und digital signieren. Bei Verwendung von S/MIME mit einer e-Mail-Nachricht lässt die Personen, die Vergewissern Sie sich, dass sehen in ihren Posteingang die genauen Nachricht, die ersten mit der Absender Schritte die Nachricht empfangen.
ms.openlocfilehash: 3ce95132476417df8949cdc12f2d825047f6b76d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027592"
---
# <a name="smime-for-message-signing-and-encryption"></a>S/MIME für die Nachrichtensignierung und -verschlüsselung

S/MIME (Secure/Multipurpose Internet Mail Extensions) ist eine verbreitete Methode oder präziser ein Protokoll für das Senden von Digital signierte und verschlüsselte Nachrichten. S/MIME können Sie e-Mail-Nachrichten verschlüsseln und digital signieren. Bei Verwendung von S/MIME mit einer e-Mail-Nachricht lässt die Personen, die Vergewissern Sie sich, dass sehen in ihren Posteingang die genauen Nachricht, die ersten mit der Absender Schritte die Nachricht empfangen. Es hilft auch Personen, die an bestimmte werden Nachrichten empfangen, die die Nachricht von bestimmten Absender und nicht von einer Person vorgeben, der Absender stammt. Zu diesem Zweck stellt S/MIME für kryptografische Sicherheitsdienste wie Authentifizierung, Integrität und Nichtabstreitbarkeit Ursprungs (Verwenden von digitalen Signaturen) bereit. Darüber hinaus werden Datenschutz und Sicherheit (mit Verschlüsselung) verbessern elektronischen Messaging. Eine ausführlichere Hintergrundinformationen zu den Verlauf und die Architektur von S/MIME im Kontext von e-Mail finden Sie unter [Grundlegendes zu S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). 
  
Als Administrator können Sie S/MIME-basierte Sicherheit für Ihre Organisation aktivieren, wenn Sie Postfächer in Exchange 2013 SP1 oder Exchange Online, ein Teil von Office 365 verfügen. Verwenden Sie die Anweisungen in den Themen verknüpft hier zusammen mit der Exchange-Verwaltungsshell zum Einrichten von S/MIME. Verwendung von S/MIME in unterstützten Versionen von Outlook oder ActiveSync mit Exchange 2013 SP1 oder Exchange Online müssen die Benutzer in Ihrer Organisation signieren und Verschlüsseln von Zwecken ausgestellte Zertifikate und Daten für Ihre lokale Active Directory veröffentlicht haben. -Domänendienst (AD DS). Ihrer AD DS muss auf den Computern an einem physischen Standort, den Sie steuern und nicht auf einer remote-Funktion oder cloudbasierten Dienst irgendwo im Internet befinden. Weitere Informationen zu AD DS finden Sie unter [Active Directory-Domänendienste](https://go.microsoft.com/fwlink/?LinkID=394064).
  
## <a name="supported-scenarios-and-technical-considerations"></a>Unterstützte Szenarien und technische Aspekte
<a name="sectionSection0"> </a>

Wenn in Ihrer Organisation Exchange 2013 SP1 oder Exchange Online verwendet wird, können Sie S/MIME funktioniert mit jeder der folgenden Endpunkte einrichten: 
  
- Outlook 2010
    
- Outlook 2013
    
- Outlook Web App
    
- Exchange ActiveSync (EAS)
    
Die Schritte für die Einrichtung von S/MIME für die verschiedenen Endpunkte unterscheiden sich je nach Endpunkt leicht. In der Regel müssen Sie die folgenden Aktionen ausführen:
  
- Installieren einer Windows-basierten Zertifizierungsstelle, und richten Sie eine public Key-Infrastruktur zum Ausstellen von S/MIME-Zertifikaten. Zertifikate, die von Anbietern von Drittanbieter-Zertifikat ausgestellt wurden, werden ebenfalls unterstützt. Weitere Informationen hierzu finden Sie unter [Active Directory Zertifikat Services (Übersicht)](https://technet.microsoft.com/library/hh831740.aspx).
    
- Veröffentlichen des Benutzerzertifikats in einem lokalen AD DS-Konto in den Attributen "UserSMIMECertificate" und/oder "UserCertificate".
    
- Synchronisieren Sie die Benutzerzertifikate aus AD DS zu Azure Active Directory für Exchange Online-Organisationen mit einer entsprechenden Version der DirSync. Dieser Zertifikate werden dann von Azure Active Directory mit Exchange Online Directory synchronisiert erhalten möchten, und es werden beim Verschlüsseln einer Nachricht an einen Empfänger verwendet.
    
- Einrichten einer virtuellen Zertifikatauflistung zum Validieren von S/MIME. Diese Informationen verwendet OWA beim Validieren der Signatur einer E-Mail und Sicherstellen, dass sie von einem vertrauenswürdigen Zertifikat signiert wurde.
    
- Einrichten des Outlook- oder EAS-Endpunkts für die Verwendung von S/MIME. 
    
## <a name="setup-smime-with-outlook-web-app"></a>Einrichten von S/MIME mit Outlook Web App
<a name="sectionSection1"> </a>

Einrichten von S/MIME für Exchange 2013 SP1 oder Exchange Online mit Outlook Web App umfasst die folgenden wichtigen Schritte:
  
1. [Konfigurieren von S/MIME-Einstellungen für Outlook Web App](configure-s-mime-settings-for-outlook-web-app.md)
    
2. [Einrichten einer virtuellen Zertifikatauflistung für die Überprüfung von S/MIME](set-up-virtual-certificate-collection-to-validate-s-mime.md)
    
3. [Synchronisierung von Benutzerzertifikaten nach Office 365 für S/MIME](sync-user-certificates-to-office-365-for-s-mime.md) Dieser Schritt gilt nur für Exchange Online. 
    
## <a name="related-message-encryption-technologies"></a>Zugehörige Nachrichten-Verschlüsselungstechnologien
<a name="sectionSection2"> </a>

Nachrichtensicherheit wichtiger wird, müssen die Administratoren den Prinzipien und Konzepte von secure messaging vertraut machen. Diese Kenntnisse ist besonders wichtig, aufgrund der wachsenden verschiedener Protection-Technologien, wie S/MIME, die verfügbar sind. Weitere Informationen zum S/MIME und deren Funktionsweise im Kontext von e-Mails finden Sie unter [Grundlegendes zu S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). Eine Reihe von verschlüsselungstechnologien arbeiten zusammen, um Schutz für Nachrichten an Rest- und in während der Übertragung zu bieten. S/MIME können gleichzeitig mit der folgenden Technologien arbeiten, jedoch nicht abhängig sind:
  
> **Transport Layer Security (TLS)** verschlüsselt den Tunnel oder die Route zwischen E-Mail-Servern, um ein Ausspionieren oder Ausspähen zu verhindern. 
    
> **Secure Sockets Layer (SSL)** verschlüsselt die Verbindung zwischen E-Mail-Clients und Office 365-Servern. 
    
> **BitLocker** verschlüsselt die Daten auf einer Festplatte in einem Datacenter, so dass wenn jemand unbefugt Zugang verschaffen, sie dennoch nicht lesen können. 
    
### <a name="smime-compared-with-office-365-message-encryption"></a>S/MIME-im Vergleich zur Office 365-Nachrichtenverschlüsselung

S/MIME erfordert eine Zertifikat und Veröffentlichung Infrastruktur, die häufig in B2B- und B2C Situationen verwendet wird. Der Benutzer steuert die kryptografischen Schlüssel in S/MIME und kann auswählen, ob sie für jede Nachricht verwenden, die sie senden. E-Mail-Programme wie Outlook suchen Sie einen vertrauenswürdigen Stammzertifizierungsstellen-Zertifikat Autorität Speicherort für digitale Signaturen und Überprüfung der Signatur ausführen. Office 365 Message Encryption ist ein richtlinienbasierte Verschlüsselungsdienst, der vom Administrator und nicht für einen einzelnen Benutzer zum Verschlüsseln von Nachrichten an alle Personen innerhalb oder außerhalb der Organisation konfiguriert werden kann. Es ist ein Onlinedienst, der basiert auf Azure Rights Management (RMS) und basiert nicht auf eine public Key-Infrastruktur. Office 365-Nachrichtenverschlüsselung bietet auch zusätzliche Funktionen, wie etwa die Möglichkeit zum Anpassen der e-Mail-Nachrichten mit der Organisation Marke. Weitere Informationen zu Office 365 Message Encryption finden Sie unter [Office 365 Message Encryption](https://go.microsoft.com/fwlink/?LinkID=392525).
  
## <a name="more-information"></a>Weitere Informationen
<a name="sectionSection3"> </a>

[Outlook Web App](http://technet.microsoft.com/library/3814b665-01e8-4881-9a44-163f14789ee4.aspx)
  
[Secure Mail (2000)](https://technet.microsoft.com/en-us/library/cc962043.aspx)
  

