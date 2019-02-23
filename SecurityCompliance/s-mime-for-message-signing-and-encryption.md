---
title: S/MIME für die Nachrichtensignierung und-Verschlüsselung in Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: Mit S/MIME können Sie e-Mails verschlüsseln und digital signieren. Wenn Sie S/MIME mit einer e-Mail-Nachricht verwenden, hilft es den Personen, die diese Nachricht erhalten, sicher zu sein, dass das, was Sie in Ihrem Posteingang sehen, die genaue Nachricht ist, die mit dem Absender gestartet wurde.
ms.openlocfilehash: 41a84d5332092748f9a8cc8fe4936c39e5fd2012
ms.sourcegitcommit: 06d6e63225f912d0f3c6bb836c61eb11c1dbe97a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "30206508"
---
# <a name="smime-for-message-signing-and-encryption"></a>S/MIME für die Nachrichtensignierung und -verschlüsselung

S/MIME (Secure/Multipurpose Internet Mail Extensions) ist eine weithin akzeptierte Methode oder genauer gesagt ein Protokoll zum Senden von digital signierten und verschlüsselten Nachrichten. Mit S/MIME können Sie e-Mails verschlüsseln und digital signieren. Wenn Sie S/MIME mit einer e-Mail-Nachricht verwenden, hilft es den Personen, die diese Nachricht erhalten, sicher zu sein, dass das, was Sie in Ihrem Posteingang sehen, die genaue Nachricht ist, die mit dem Absender gestartet wurde. Außerdem können Benutzer, die Nachrichten empfangen, sicher sein, dass die Nachricht vom Absender stammt und nicht von einer Person, die vorgibt, der Absender zu sein. Zu diesem Zweck stellt S/MIME kryptografische Sicherheitsdienste wie Authentifizierung, Nachrichtenintegrität und nicht Ablehnung des Ursprungs (mithilfe digitaler Signaturen) bereit. Darüber hinaus wird die Datensicherheit (mit Verschlüsselung) für elektronisches Messaging verbessert. Einen umfassenderen Hintergrund zur Geschichte und Architektur von S/MIME im Kontext von e-Mails finden Sie unter Understanding [s/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). 
  
Als Administrator können Sie die S/MIME-basierte Sicherheit für Ihre Organisation aktivieren, wenn Sie über Postfächer in Exchange 2013 SP1 oder Exchange Online, einem Teil von Office 365, verfügen. Verwenden Sie die Anweisungen in den hier verknüpften Themen zusammen mit der Exchange-Verwaltungsshell, um S/MIME einzurichten. Um S/MIME in unterstützten Versionen von Outlook oder ActiveSync mit Exchange 2013 SP1 oder Exchange Online verwenden zu können, müssen die Benutzer in Ihrer Organisation über Zertifikate verfügen, die zum Signieren und verschlüsseln und für die in Ihrem lokalen Active Directory veröffentlichten Daten ausgestellt wurden. Domänendienst (AD DS). Ihre AD DS muss sich auf Computern an einem physischen Standort befinden, den Sie steuern und nicht an einem Remotestandort oder einem cloudbasierten Dienst im Internet. Weitere Informationen zu AD DS finden Sie unter [Active Directory Domain Services](https://go.microsoft.com/fwlink/?LinkID=394064).
  
## <a name="supported-scenarios-and-technical-considerations"></a>Unterstützte Szenarien und technische Aspekte
<a name="sectionSection0"> </a>

Sie können S/MIME für alle der folgenden Endpunkte einrichten: 
  
- Outlook 2010 oder höher
    
- Outlook im Web (früher Outlook Web App)
    
- Exchange ActiveSync (EAS)
    
Die Schritte für die Einrichtung von S/MIME für die verschiedenen Endpunkte unterscheiden sich je nach Endpunkt leicht. In der Regel müssen Sie die folgenden Aktionen ausführen:
  
- Installieren Sie eine Windows-basierte ZertifizierungsStelle, und richten Sie eine Public Key-Infrastruktur zum Ausgeben von S/MIME-Zertifikaten ein. Zertifikate von Drittanbieter-Zertifikatanbietern werden ebenfalls unterstützt. Weitere Informationen finden Sie unter [Active Directory Certificate Services Overview](https://technet.microsoft.com/library/hh831740.aspx).
    
- Veröffentlichen des Benutzerzertifikats in einem lokalen AD DS-Konto in den Attributen "UserSMIMECertificate" und/oder "UserCertificate".
    
- Synchronisieren Sie für Exchange Online-Organisationen die Benutzerzertifikate mithilfe einer geeigneten dirSync-Version von AD DS zu Azure Active Directory. Diese Zertifikate werden dann von Azure Active Directory in das Exchange Online-Verzeichnis synchronisiert und beim Verschlüsseln einer Nachricht an einen Empfänger verwendet.
    
- Richten Sie eine virtuelle Zertifikat Sammlung ein, um S/MIME zu überprüfen. Diese Informationen werden von Outlook im Web (früher als Outlook im Web bezeichnet) verwendet, wenn Sie die Signatur einer e-Mail überprüfen und sicherstellen, dass Sie von einem vertrauenswürdigen Zertifikat signiert wurde.
    
- Richten Sie den Outlook- oder EAS-Endpunkt für die Verwendung von S/MIME ein. 
    
## <a name="setup-smime-with-outlook-on-the-web"></a>Einrichten von S/MIME mit Outlook im Web
<a name="sectionSection1"> </a>

Das Einrichten von S/MIME für Exchange Online mit Outlook im Web umfasst die folgenden wichtigen Schritte:
  
1. [Configure S/MIME settings for Outlook on the web](configure-s-mime-settings-for-outlook-web-app.md)
    
2. [Einrichten einer virtuellen Zertifikatauflistung für die Überprüfung von S/MIME](set-up-virtual-certificate-collection-to-validate-s-mime.md)
    
3. [Synchronisieren von Benutzerzertifikaten mit Office 365 für S/MIME](sync-user-certificates-to-office-365-for-s-mime.md) Dieser Schritt gilt nur für Exchange Online. 
    
## <a name="related-message-encryption-technologies"></a>Zugehörige Nachrichten-Verschlüsselungstechnologien
<a name="sectionSection2"> </a>

Da die Nachrichtensicherheit immer wichtiger wird, müssen Administratoren die Grundsätze und Konzepte von Secure Messaging verstehen. Dieses Verständnis ist besonders wichtig aufgrund der wachsenden Vielfalt von schutzbezogenen Technologien, wie S/MIME, die verfügbar sind. Weitere Informationen zu S/MIME und zur Funktionsweise im Kontext von e-Mails finden Sie unter [understandIng s/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). Es werden verschiedene Verschlüsselungstechnologien zusammen verwendet, um den Schutz von Nachrichten auf Rest-und Transit Daten zu gewährleisten. S/MIME kann gleichzeitig mit den folgenden Technologien arbeiten, ist aber nicht davon abhängig:
  
> **Transport Layer Security (TLS)** verschlüsselt den Tunnel oder die Route zwischen E-Mail-Servern, um ein Ausspionieren oder Ausspähen zu verhindern. 
    
> **Secure Sockets Layer (SSL)** verschlüsselt die Verbindung zwischen E-Mail-Clients und Office 365-Servern. 
    
> **BitLocker** verschlüsselt die Daten auf einer Festplatte in einem Rechenzentrum, sodass Benutzer, die nicht autorisierten Zugriff erhalten, Sie nicht lesen können. 
    
### <a name="smime-compared-with-office-365-message-encryption"></a>S/MIME-im Vergleich zur Office 365-Nachrichtenverschlüsselung

S/MIME erfordert eine Zertifikat-und Veröffentlichungs Infrastruktur, die häufig in Business-to-Business-und Business-to-Consumer-Situationen verwendet wird. Der Benutzer steuert die kryptografischen Schlüssel in S/MIME und kann auswählen, ob Sie für jede gesendete Nachricht verwendet werden sollen. E-Mail-Programme wie Outlook suchen einen vertrauenswürdigen Speicherort der Stammzertifizierungsstelle für die digitale Signierung und Überprüfung der Signatur. Office 365 Nachrichtenverschlüsselung ist ein Policy-basierter Verschlüsselungsdienst, der von einem Administrator konfiguriert werden kann, und nicht von einem einzelnen Benutzer, um e-Mails zu verschlüsseln, die an Personen innerhalb oder außerhalb der Organisation gesendet werden. Es handelt sich um einen Onlinedienst, der auf Azure Rights Management (RMS) basiert und nicht auf einer Public Key-Infrastruktur beruht. Die Nachrichtenverschlüsselung in Office 365 bietet außerdem zusätzliche Funktionen wie die Möglichkeit zum Anpassen der e-Mail mit der Marke der Organisation. Weitere Informationen zur Nachrichtenverschlüsselung von Office 365 finden Sie unter [office 365-Nachrichtenverschlüsselung](https://go.microsoft.com/fwlink/?LinkID=392525).
  
## <a name="more-information"></a>Weitere Informationen
<a name="sectionSection3"> </a>

[Outlook im Web](http://technet.microsoft.com/library/3814b665-01e8-4881-9a44-163f14789ee4.aspx)
  
[Secure Mail (2000)](https://technet.microsoft.com/en-us/library/cc962043.aspx)
  

