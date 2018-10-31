---
title: E-Mail-Verschlüsselung in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
description: Vergleichen Sie die Optionen zur Verschlüsselung in Office 365, einschließlich Office Message Encryption (OME), S/MIME, (Information Rights Management, IRM) und Informationen zu Transport Layer Security (TLS).
ms.openlocfilehash: c9c83283cab09ac81ab2856aec53fe8682ec45b8
ms.sourcegitcommit: c05076501dfe118e575998ecfc08ad69d13c8abc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25853080"
---
# <a name="email-encryption-in-office-365"></a>E-Mail-Verschlüsselung in Office 365

In diesem Artikel vergleicht Optionen zur Verschlüsselung in Office 365, einschließlich Office Message Encryption (OME), S/MIME, (Information Rights Management, IRM) und führt Transport Layer Security (TLS).
  
Office 365 bietet mehrere Optionen können Sie Ihre geschäftlichen Anforderungen für e-Mail-Sicherheit. Dieser Artikel enthält Informationen zu drei Methoden zum Verschlüsseln von e-Mail in Office 365. Wenn Sie weitere Informationen zu allen Sicherheitsfeatures in Office 365 erfahren möchten, besuchen Sie das [Office 365-Trust Center](http://go.microsoft.com/fwlink/p/?LinkID=282470). In diesem Artikel werden die drei Typen der Verschlüsselung für Office 365-Administratoren zur sicheren e-Mail in Office 365 verfügbar eingeführt:
  
- Office-Nachrichtenverschlüsselung (Office Message Encryption, OME)
    
- Secure/Multipurpose Internet Mail Extensions (S/MIME)
    
- Information Rights Management (IRM).
    
## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a>Was ist E-Mail-Verschlüsselung, und wie wird sie in Office 365 verwendet?

Verschlüsselung ist der Prozess, mit dem Informationen codiert ist, damit nur autorisierter Empfänger decodieren und die Informationen nutzen kann. Office 365 verwendet eine Verschlüsselung auf zwei Arten: im Dienst und als Steuerelement Customer. In den Dienst wird die Verschlüsselung in Office 365 standardmäßig verwendet. Sie müssen nicht vornehmen. Office 365 wird beispielsweise Transport Layer Security (TLS) verschlüsselt die Verbindung oder Sitzung zwischen zwei Servern verwendet. 
  
Hier wird die Funktionsweise von e-Mail-Verschlüsselung in der Regel:
  
- Eine Nachricht wird verschlüsselt oder von nur-Text in darstellbare verschlüsselten, auf dem Computer des Senders oder von einem zentralen Server umgewandelt wird, während die Nachricht während der Übertragung ist.
    
- Die Nachricht verbleibt in verschlüsselten Text, während sie während der Übertragung ist, um es geschützt, gelesen, für den Fall, dass die Nachricht abgefangen wird.
    
- Nachdem die Nachricht vom Empfänger empfangen wurde, wird sie mit einer der folgenden zwei Methoden wieder in lesbaren Nur-Text umgewandelt:
    
  - Dem Computer des Empfängers verwendet einen Schlüssel zum Entschlüsseln der Nachricht oder
    
  - Ein zentraler Server entschlüsselt die Nachricht im Auftrag des Empfängers nach Überprüfung der Identität des Empfängers.
    
Weitere Informationen wie Office 365-Kommunikation zwischen Servern sichert verwendet wie zwischen Organisationen in Office 365 oder zwischen Office 365 und einen vertrauenswürdigen Geschäftspartner außerhalb von Office 365, finden Sie unter [wie Exchange Online TLS, um sichere e-Mail Verbindungen in Office 365](exchange-online-uses-tls-to-secure-email-connections.md).
  
In diesem Video wird eine Einführung in die [Verschlüsselung in Office 365](https://www.youtube.com/watch?v=KmfxCd5ublI).
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Vergleichen der in Office 365 verfügbaren E-Mail-Verschlüsselungsoptionen

||        ![Konzeptionelle Grafik, die OME beschreibt.](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)                 |        ![Konzeptionelle Grafik, die IRM beschreibt.](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)                 |        ![Konzeptionelle Grafik, die SMIME beschreibt.](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)                |
|:-----|:-----|:-----|:-----|
|Was ist das?  <br/> |Office 365-Nachrichtenverschlüsselung (Office Message Encryption, OME) ist ein Dienst, der auf Azure Rights Management (Azure RMS) aufbaut und mit dem Sie verschlüsselte E-Mails an Personen innerhalb oder außerhalb Ihrer Organisation senden können, unabhängig von der E-Mail-Zieladresse (Gmail, Yahoo! Mail, Outlook.com usw.).  <br/> Als Administrator können Sie Transportregeln einrichten, die die Bedingungen für die Verschlüsselung definieren. Wenn ein Benutzer eine Nachricht sendet, die mit einer Regel übereinstimmt, wird die Verschlüsselung automatisch angewendet.  <br/> Zum Anzeigen von verschlüsselter Nachrichten Empfänger können entweder eine einmalige Kennung, melden Sie sich mit einem Microsoft-Konto oder melden Sie sich mit einem Arbeit erhalten möchten, oder Schule mit Office 365-Konto. Empfänger können verschlüsselte Antworten auch senden. Sie benötigen kein Office 365-Abonnement zu verschlüsselte Nachrichten senden oder verschlüsselte Antworten.  <br/> |IRM ist eine Verschlüsselungslösung, die auch Nutzungseinschränkungen auf E-Mail-Nachrichten anwendet. Mit dieser Lösung können Sie verhindern, dass vertrauliche Informationen von nicht autorisierten Personen gedruckt, weitergeleitet oder kopiert werden.  <br/> IRM-Funktionen in Office 365 verwenden Azure Rights Management (Azure RMS). 
  <br/> |S/MIME ist eine Verschlüsselung zertifikatbasierte-Lösung, mit dem Sie sowohl verschlüsseln eine Nachricht digital signieren. Die Verschlüsselung von Nachrichten wird sichergestellt, dass nur der beabsichtigte Empfänger öffnen und die Nachricht lesen kann. Die digitale Signatur kann den Empfänger die Identität des Absenders zu überprüfen.  <br/> Digitale Signaturen und Nachrichtenverschlüsselung werden durch Verwendung eindeutiger digitaler Zertifikate ermöglicht, die die Schlüssel für das Überprüfen von digitalen Signaturen und das Verschlüsseln oder Entschlüsseln von Nachrichten enthalten.  <br/> Verwendung von S/MIME, benötigen Sie öffentliche Schlüssel für jeden Empfänger auf Datei. Empfänger müssen ihre eigenen privaten Schlüssel verwalten die dauerhaft gesichert werden müssen. Wenn der private Schlüssel des Empfängers gefährdet sind, muss der Empfänger zum Abrufen eines neuen privaten Schlüssels und öffentlichen Schlüssel an alle Absender potenzielle verteilen.  <br/> |
|Vorhandene Funktionen  <br/> | OME:  <br/>  Verschlüsselt Nachrichten, die an interne oder externe Empfänger gesendet werden.  <br/>  Ermöglicht Benutzern das Senden verschlüsselter Nachrichten an beliebige E-Mail-Adressen, einschließlich Outlook.com, Yahoo! Mail und Gmail.  <br/>  Ermöglicht es Ihnen, als Administrator, zu die anzeigeportal entsprechend Ihrer Organisation Marke e-Mail anpassen.  <br/>  Microsoft sicher verwaltet und speichert die Schlüssel, damit Sie auf nicht.  <br/>  Es ist keine spezielle clientseitige Software erforderlich, sofern die verschlüsselte Nachricht (als HTML-Anlage gesendet) in einem Browser geöffnet werden kann.  <br/> | IRM:  <br/>  Verwendet Verschlüsselung und Nutzungsbeschränkungen, um Online- und Offlineschutz für E-Mail-Nachrichten und Anlagen bereitzustellen.  <br/>  Gibt Ihnen als Administrator die Möglichkeit, Transportregeln oder Outlook-Schutzregeln einzurichten, um IRM automatisch auf ausgewählte Nachrichten anzuwenden.  <br/>  Ermöglicht Benutzern das manuelle Anwenden von Vorlagen in Outlook oder Outlook Web App.  <br/> |In S/MIME erfolgt die Absenderauthentifizierung durch digitale Signaturen, und die Vertraulichkeit von Nachrichten wird durch Verschlüsselung sichergestellt.  <br/> |
|Nicht vorhandene Funktionen  <br/> |OME kann nicht Sie Usage Einschränkungen auf Nachrichten anwenden. Angenommen, können sie Sie um durch weiterleiten oder Drucken eine verschlüsselte Nachricht einen Empfänger zu beenden.  <br/> |Einige Anwendungen möglicherweise IRM-e-Mails nicht auf allen Geräten unterstützt. Weitere Informationen zu diesen und anderen Produkten, die IRM für e-Mail zu unterstützen, finden Sie unter [Client Gerätefunktionen](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).<br/> |S/MIME zulässig verschlüsselte Nachrichten für Schadsoftware, Spam oder Richtlinien erzwungen wird nicht ist.  <br/> |
|Empfehlungen und Beispielszenarien  <br/> | Es wird empfohlen, OME verwenden, wenn Sie vertrauliche Geschäftsdaten an Personen außerhalb Ihrer Organisation senden möchten, ob sie Verbraucher oder andere Unternehmen sind. Zum Beispiel:  <br/>  Ein Bankangestellter sendet Kreditkartenabrechnungen an Kunden  <br/>  Senden von Patientendaten zu einem Patienten ein Arzt office  <br/>  Ein Anwalt sendet vertrauliche Rechtsinformationen an einen anderen Anwalt.  <br/> | Die Verwendung von IRM wird empfohlen, wenn Sie Nutzungseinschränkungen und Verschlüsselung anwenden möchten. Beispiel:  <br/>  Ein Manager sendet vertrauliche Informationen an ihr Team über ein neues Produkt gilt die Option "Nicht weiterleiten".  <br/>  Eine Führungskraft muss ein Angebot für ein anderes Unternehmen freigeben, das eine Anlage von einem Partner enthält, der Office 365 verwendet, und sowohl die E-Mail als auch die Anlage müssen geschützt werden.  <br/> | Es wird empfohlen, mit S/MIME, wenn Ihre Organisation oder des Empfängers Organisation true Peer-zu-Peer-Verschlüsselung erforderlich ist.  <br/>  S/MIME wird am häufigsten in den folgenden Szenarien verwendet:  <br/>  Kommunikation zwischen Behörden  <br/>  Kommunikation zwischen einem Unternehmen und einer Behörde  <br/> |
   
## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a>Welche Verschlüsselungsoptionen sind für mein Office 365-Abonnement verfügbar?

Informationen zu e-Mail-Verschlüsselungsoptionen für Ihre Office 365-Abonnements finden Sie in der [Exchange Online-dienstbeschreibung](https://technet.microsoft.com/en-us/library/exchange-online-service-description.aspx). Hier finden Sie Informationen zu den folgenden Verschlüsselungsfeatures:
  
- Azure RMS, einschließlich IRM-Funktionen und OME
    
- S/MIME
    
- TLS
    
- Verschlüsselung von Daten im Ruhezustand (über BitLocker)
    
## <a name="what-about-encryption-for-data-at-rest"></a>Wissenswertes zur Verschlüsselung von Daten im Ruhezustand

"Daten im Ruhezustand" bezieht sich auf Daten, die während der Übertragung aktiv ist. In Office 365 werden die e-Mail-Daten im Ruhezustand mit BitLocker Drive Encryption verschlüsselt. BitLocker verschlüsselt die Festplatten in Office 365-Rechenzentren verbesserten Schutz vor nicht autorisiertem Zugriff bereitstellen. Finden Sie weitere Informationen finden Sie unter [BitLocker Overview](https://go.microsoft.com/fwlink/p/?LinkId=394737).
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a>Weitere Informationen zu E-Mail-Verschlüsselungsoptionen in Office 365

Weitere Informationen zu den in diesem Artikel vorgestellten E-Mail-Verschlüsselungsoptionen sowie zu TLS finden Sie in den folgenden Artikeln:
  
 **OME**
  
[Office 365-Nachrichtenverschlüsselung (OME)](ome.md)
  
 **IRM**
  
[Verwaltung von Informationsrechten in Exchange Online](https://technet.microsoft.com/en-us/library/jj983436%28v=exchg.150%29.aspx)
  
[Was ist Azure Rights Management?](https://technet.microsoft.com/library/jj585026)
  
 **S/MIME**
  
[S/MIME für die Nachrichtensignierung und -verschlüsselung](https://technet.microsoft.com/library/dn626158)
  
[Grundlegendes zu S/MIME](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[Grundlegendes zu öffentlichen Schlüsseln](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
 **TLS**
  
[Konfigurieren der benutzerdefinierten Nachrichtenübermittlung mithilfe von Connectors in Office 365](https://technet.microsoft.com/en-us/library/jj723138%28v=exchg.150%29.aspx)
  

