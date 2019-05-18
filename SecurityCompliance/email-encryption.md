---
title: E-Mail-Verschlüsselung in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
ms.collection:
- M365-security-compliance
description: Vergleichen Sie Verschlüsselungsoptionen in Office 365 einschließlich Office-Nachrichtenverschlüsselung (OM), S/MIME, Information Rights Management (IRM) und erfahren Sie mehr über TLS (Transport Layer Security).
ms.openlocfilehash: 4a39bee76346bb46a53ab752d2fac31316c0258f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154787"
---
# <a name="email-encryption-in-office-365"></a>E-Mail-Verschlüsselung in Office 365

In diesem Artikel werden Verschlüsselungsoptionen in Office 365, einschließlich Office-Nachrichtenverschlüsselung (OM), S/MIME, Information Rights Management (IRM), und Einführung in Transport Layer Security (TLS), verglichen.
  
Office 365 bietet mehrere Verschlüsselungsoptionen, die Ihnen dabei helfen, Ihre geschäftlichen Anforderungen für E-Mail-Sicherheit zu erfüllen. In diesem Artikel werden drei Methoden zum Verschlüsseln von e-Mails in Office 365 vorgestellt. Wenn Sie mehr über alle Sicherheitsfeatures in Office 365 erfahren möchten, besuchen Sie das [Office 365 Trust Center](http://go.microsoft.com/fwlink/p/?LinkID=282470). In diesem Artikel werden die drei Verschlüsselungstypen vorgestellt, die für Office 365 Administratoren zur Verfügung stehen, um e-Mails in Office 365 zu schützen:
  
- Office-Nachrichtenverschlüsselung (Office Message Encryption, OME)
    
- Secure/Multipurpose Internet Mail Extensions (S/MIME)
    
- Information Rights Management (IRM).
    
## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a>Was ist E-Mail-Verschlüsselung, und wie wird sie in Office 365 verwendet?

Verschlüsselung ist der Vorgang, bei dem Informationen so codiert werden, dass nur ein autorisierter Empfänger die Informationen decodieren und nutzen kann. Office 365 verwendet Verschlüsselung auf zweierlei Weise: im Dienst und als Kunden Steuerelement. Im Dienst wird die Verschlüsselung standardmäßig in Office 365 verwendet; Sie müssen nichts konfigurieren. Beispielsweise verwendet Office 365 Transport Layer Security (TLS), um die Verbindung oder Sitzung zwischen zwei Servern zu verschlüsseln. 
  
So funktioniert die e-Mail-Verschlüsselung normalerweise:
  
- Eine Nachricht wird verschlüsselt oder aus nur-Text in unlesbaren verschlüsselten Text, entweder auf dem Computer des Absenders oder von einem zentralen Server transformiert, während sich die Nachricht in der Übertragung befindet.
    
- Die Nachricht verbleibt während der Übertragung in verschlüsselter Reihenfolge, um Sie vor dem Lesen zu schützen, falls die Nachricht abgefangen wird.
    
- Nachdem die Nachricht vom Empfänger empfangen wurde, wird sie mit einer der folgenden zwei Methoden wieder in lesbaren Nur-Text umgewandelt:
    
  - Der Computer des Empfängers verwendet einen Schlüssel, um die Nachricht zu entschlüsseln, oder
    
  - Ein zentraler Server entschlüsselt die Nachricht im Namen des Empfängers, nachdem die Identität des Empfängers überprüft wurde.
    
Weitere Informationen darüber, wie Office 365 die Kommunikation zwischen Servern, beispielsweise zwischen Organisationen innerhalb Office 365 oder zwischen Office 365 und einem vertrauenswürdigen Geschäftspartner außerhalb von Office 365 sichert, finden Sie unter [how Exchange Online uses TLS to Secure Email Verbindungen in Office 365](exchange-online-uses-tls-to-secure-email-connections.md).
  
Sehen Sie sich dieses Video für eine Einführung in die [Verschlüsselung in Office 365](https://www.youtube.com/watch?v=KmfxCd5ublI)an.
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Vergleichen der in Office 365 verfügbaren E-Mail-Verschlüsselungsoptionen

||![Konzeptuelles Kunstwerk, das OM beschreibt](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)|![Konzeptuelles Kunstwerk, das IRM beschreibt](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)|![Konzeptuelles Kunstwerk, das SMIME beschreibt](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)|
|:-----|:-----|:-----|:-----|
|Was ist das?|Office 365-Nachrichtenverschlüsselung (Office Message Encryption, OME) ist ein Dienst, der auf Azure Rights Management (Azure RMS) aufbaut und mit dem Sie verschlüsselte E-Mails an Personen innerhalb oder außerhalb Ihrer Organisation senden können, unabhängig von der E-Mail-Zieladresse (Gmail, Yahoo! Mail, Outlook.com usw.).  <br/> Als Administrator können Sie Transportregeln einrichten, die die Bedingungen für die Verschlüsselung definieren. Wenn ein Benutzer eine Nachricht sendet, die mit einer Regel übereinstimmt, wird die Verschlüsselung automatisch angewendet.  <br/> Zum Anzeigen verschlüsselter Nachrichten können Empfänger entweder eine einmalige Kennung abrufen, sich mit einem Microsoft-Konto anmelden oder sich mit einem Geschäfts- oder Schulkonto anmelden, das Office 365 zugeordnet ist. Empfänger können auch verschlüsselte Antworten senden. Sie benötigen kein Office 365-Abonnement, um verschlüsselte Nachrichten anzuzeigen oder verschlüsselte Antworten zu senden.|IRM ist eine Verschlüsselungslösung, die auch Nutzungseinschränkungen auf E-Mail-Nachrichten anwendet. Mit dieser Lösung können Sie verhindern, dass vertrauliche Informationen von nicht autorisierten Personen gedruckt, weitergeleitet oder kopiert werden.  <br/> IRM-Funktionen in Office 365 verwenden Azure Rights Management (Azure RMS).|S/MIME ist eine zertifikatbasierte Verschlüsselungslösung, mit der Sie Nachrichten sowohl verschlüsseln als auch digital signieren können. Durch die Nachrichtenverschlüsselung kann sichergestellt werden, dass nur der vorgesehene Empfänger die Nachricht öffnen und lesen kann. Mithilfe einer digitalen Signatur kann den Empfänger die Identität des Absenders überprüfen.  <br/> Digitale Signaturen und Nachrichtenverschlüsselung werden durch Verwendung eindeutiger digitaler Zertifikate ermöglicht, die die Schlüssel für das Überprüfen von digitalen Signaturen und das Verschlüsseln oder Entschlüsseln von Nachrichten enthalten.  <br/> Um S/MIME verwenden zu können, müssen Sie über gespeicherte öffentliche Schlüssel für jeden Empfänger verfügen. Empfänger müssen ihre eigenen privaten Schlüssel verwalten, die dauerhaft gesichert sein müssen. Wenn die privaten Schlüssel eines Empfängers gefährdet sind, muss der Empfänger einen neuen privaten Schlüssel abrufen und öffentliche Schlüssel an alle potenziellen Absender weiterverteilen.|
|Vorhandene Funktionen|Ome  <br/>  Verschlüsselt Nachrichten, die an interne oder externe Empfänger gesendet werden.  <br/>  Ermöglicht Benutzern das Senden verschlüsselter Nachrichten an beliebige E-Mail-Adressen, einschließlich Outlook.com, Yahoo! Mail und Gmail.  <br/>  Ermöglicht es Ihnen als Administrator, das e-Mail-Anzeige Portal so anzupassen, dass es die Marke Ihrer Organisation widerspiegelt.  <br/>  Die Schlüssel werden von Microsoft sicher verwaltet und gespeichert, daher müssen Sie dies nicht tun.  <br/>  Es ist keine spezielle clientseitige Software erforderlich, sofern die verschlüsselte Nachricht (als HTML-Anlage gesendet) in einem Browser geöffnet werden kann.|IRM  <br/>  Verwendet Verschlüsselung und Nutzungsbeschränkungen, um Online- und Offlineschutz für E-Mail-Nachrichten und Anlagen bereitzustellen.  <br/>  Gibt Ihnen als Administrator die Möglichkeit, Transportregeln oder Outlook-Schutzregeln einzurichten, um IRM automatisch auf ausgewählte Nachrichten anzuwenden.  <br/>  Ermöglicht Benutzern das manuelle Anwenden von Vorlagen in Outlook oder Outlook im Internet (früher bekannt als Outlook Web App).|In S/MIME erfolgt die Absenderauthentifizierung durch digitale Signaturen, und die Vertraulichkeit von Nachrichten wird durch Verschlüsselung sichergestellt.|
|Nicht vorhandene Funktionen|Mit OM können Sie keine Nutzungseinschränkungen auf Nachrichten anwenden. Sie können ihn beispielsweise nicht verwenden, um zu verhindern, dass ein Empfänger eine verschlüsselte Nachricht weiterleitet oder druckt.|Einige Anwendungen unterstützen IRM-E-Mails möglicherweise nicht auf allen Geräten. Weitere Informationen zu diesen und anderen Produkten, die IRM-e-Mails unterstützen, finden Sie unter [Client-Gerätefunktionen](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).|S/MIME lässt nicht zu, dass verschlüsselte Nachrichten auf Schadsoftware, Spam oder Richtlinien überprüft werden.|
|Empfehlungen und Beispielszenarien|Wir empfehlen die Verwendung von OM, wenn Sie vertrauliche Geschäftsinformationen an Personen außerhalb Ihrer Organisation senden möchten, unabhängig davon, ob es sich um Verbraucher oder andere Unternehmen handelt. Beispiel:  <br/>  Ein Bankangestellter sendet Kreditkartenabrechnungen an Kunden.  <br/>  Das Büro eines Arztes, der medizinische Aufzeichnungen an einen Patienten sendet  <br/>  Ein Anwalt sendet vertrauliche Rechtsinformationen an einen anderen Anwalt.|Die Verwendung von IRM wird empfohlen, wenn Sie Nutzungseinschränkungen und Verschlüsselung anwenden möchten. Beispiel:  <br/>  Ein Manager, der vertrauliche Details zu einem neuen Produkt an das Team sendet, wendet die Option "nicht weiterleiten" an.  <br/>  Eine Führungskraft muss ein Angebot für ein anderes Unternehmen freigeben, das eine Anlage von einem Partner enthält, der Office 365 verwendet, und sowohl die E-Mail als auch die Anlage müssen geschützt werden.|Wir empfehlen die Verwendung von S/MIME, wenn entweder Ihre Organisation oder die Organisation des Empfängers echte Peer-to-Peer-Verschlüsselung erfordert.  <br/>  S/MIME wird am häufigsten in den folgenden Szenarien verwendet:  <br/>  Kommunikation zwischen Behörden  <br/>  Kommunikation zwischen einem Unternehmen und einer Behörde|
   
## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a>Welche Verschlüsselungsoptionen sind für mein Office 365-Abonnement verfügbar?

Informationen zu e-Mail-Verschlüsselungsoptionen für Ihr Office 365-Abonnement finden Sie in der [Exchange Online-Dienstbeschreibung](https://technet.microsoft.com/en-us/library/exchange-online-service-description.aspx). Hier finden Sie Informationen zu den folgenden Verschlüsselungsfeatures:
  
- Azure RMS, einschließlich IRM-Funktionen und OME
    
- S/MIME
    
- TLS
    
- Verschlüsselung von Daten im Ruhezustand (über BitLocker)
    
## <a name="what-about-encryption-for-data-at-rest"></a>Wissenswertes zur Verschlüsselung von Daten im Ruhezustand

"Daten im Ruhezustand" bezieht sich auf Daten, die nicht aktiv unterwegs sind. In Office 365 werden E-Mail-Daten im Ruhezustand mit der BitLocker-Laufwerkverschlüsselung verschlüsselt. BitLocker verschlüsselt die Festplatten in Office 365-Datencentern, um verbesserten Schutz vor nicht autorisiertem Zugriff bereitzustellen. Weitere Informationen finden Sie unter [Übersicht über BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=394737).
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a>Weitere Informationen zu E-Mail-Verschlüsselungsoptionen in Office 365

Weitere Informationen zu den in diesem Artikel vorgestellten E-Mail-Verschlüsselungsoptionen sowie zu TLS finden Sie in den folgenden Artikeln:
  
 **Ome**
  
[Office 365-Nachrichtenverschlüsselung (OME)](ome.md)
  
 **IRM**
  
[Verwaltung von Informationsrechten in Exchange Online](https://technet.microsoft.com/en-us/library/jj983436%28v=exchg.150%29.aspx)
  
[Was ist Azure Rights Management?](https://technet.microsoft.com/library/jj585026)
  
 **S/MIME**
  
[S/MIME für die Nachrichtensignierung und -verschlüsselung](https://technet.microsoft.com/library/dn626158)
  
[Grundlegendes zu S/MIME](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[Grundlegendes zur Kryptografie mit öffentlichen Schlüsseln](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
 **TLS**
  
[Konfigurieren benutzerdefinierter e-Mail-Fluss mithilfe von Connectors in Office 365](https://technet.microsoft.com/en-us/library/jj723138%28v=exchg.150%29.aspx)
  

