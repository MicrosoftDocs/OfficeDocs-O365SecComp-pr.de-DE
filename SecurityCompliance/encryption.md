---
title: Verschlüsselung in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
description: Mit Office 365 werden Ihre Inhalte im Ruhezustand und bei der Übertragung, mit der stärksten Verschlüsselung, Protokolle und -Technologien verfügbar verschlüsselt. Rufen Sie eine Übersicht über die Verschlüsselung in Office 365.
ms.openlocfilehash: e5c21cf456f9ccca2393b8985dd47e34745902cf
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529460"
---
# <a name="encryption-in-office-365"></a>Verschlüsselung in Office 365

Verschlüsselung ist ein wichtiger Teil der Strategien für Datei den Schutz und zur Datenschutz. Lesen Sie diesen Artikel, wenn Sie eine Übersicht über die Verschlüsselung für alle Versionen von Office 365 verwendete erhalten möchten, und holen Sie sich Hilfe mit Verschlüsselung-Aufgaben aus der Verschlüsselung für Ihre Organisation zu Office-Dokumenten Kennwortschutz einrichten.
  
- Wenn Sie Informationen zu Zertifikaten und -Technologien wie TLS suchen, finden Sie unter [Technische Referenz Details über die Verschlüsselung in Office 365](technical-reference-details-about-encryption.md).
    
- Wenn Sie Informationen zum Konfigurieren oder Einrichten der Verschlüsselung für Ihre Organisation suchen, finden Sie unter [Einrichten von Verschlüsselung in Office 365 Enterprise](set-up-encryption.md).
    
## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>Was ist Verschlüsselung, und wie funktioniert es in Office 365?

Auf allgemeiner Ebene wird die Verschlüsselung der Vorgang der Codierung der Daten (bezeichnet als nur-Text) in verschlüsselten Text, der durch Benutzer oder Computer verwendet werden kann, solange und der verschlüsselten Text entschlüsselt wird. Entschlüsselung erfordert einen Verschlüsselungsschlüssel, den nur autorisierten Benutzer verfügen. Verschlüsselung wird sichergestellt, dass nur autorisierte Empfänger Ihrer Inhalte, wie e-Mail-Nachrichten und Dateien entschlüsselt werden können.
  
Verschlüsselung von selbst wird nicht verhindert, dass Inhalte, wie Dateien, e-Mail-Nachrichten, Kalendereinträge und usw., in die falschen Hände. Verschlüsselung ist Bestandteil einer größeren Strategie zum Schutz für Ihre Organisation. Mithilfe der Verschlüsselung können Sie sicherstellen, dass nur Benutzer, die verschlüsselte Daten verwenden können soll können.
  
Sie können mehrere Ebenen der Verschlüsselung zur selben Zeit erfüllt sein. Beispielsweise können Sie e-Mail-Nachrichten und auch die Kommunikationskanäle Ihre e-Mails durchläuft verschlüsseln. Mit Office 365 werden Ihre Daten verschlüsselt, im Ruhezustand und bei der Übertragung, verwenden verschiedene starke Verschlüsselungsprotokolle und -Technologien, die Transport Layer Security/Secure Sockets Layer (TLS/SSL), Internet Protocol Security (IPSec) und erweiterte Verschlüsselung enthalten Standard (AES).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Verschlüsselung für Daten im Ruhezustand und Daten während der Übertragung

 **Beispiele für Daten im Ruhezustand** sind Dateien, die auf einer SharePoint-Bibliothek, Project Online-Daten, Dokumente, die in einer Skype für Business Besprechung, e-Mail-Nachrichten und Anlagen, die im Ordner von Office 365 gespeichert sind hochgeladen wurden hochgeladen wurden Postfach- und Dateien zu OneDrive for Business hochgeladen. 
  
 **Beispiele für Daten während der Übertragung** sind e-Mail-Nachrichten, die zurzeit Zustellung oder Unterhaltungen, die stattfinden in einer onlinebesprechung. In Office 365 ist Daten während der Übertragung, wenn das Gerät des Benutzers mit einem Office 365-Server kommuniziert oder wenn ein Office 365-Server mit einem anderen Server kommuniziert. 
  
Mit Office 365 haben Sie mehrere Ebenen und Arten von Verschlüsselung zusammenarbeiten, um Ihre Daten zu schützen. Die folgende Tabelle enthält einige Beispiele für mit Links zu weiteren Informationen.
  
|**Arten von Inhalten**|**Verschlüsselungstechnologien**|**Weitere Ressourcen**|
|:-----|:-----|:-----|
|Die Dateien auf einem Gerät. Dies kann e-Mail-Nachrichten gespeichert, die in einem Ordner, Office-Dokumente auf einem Computer, Tablet oder Telefon gespeichert oder in die Microsoft-Cloud gespeicherten Daten umfassen.  <br/> |BitLocker in Microsoft-Rechenzentren. BitLocker kann auch auf Clientcomputern wie Windows-Computern und Tablet-PCs verwendet werden  <br/> Verteilte Schlüssel Manager (DKM) in Microsoft-Rechenzentren  <br/> Kundenschlüssel für Office 365  <br/> |[Windows IT Center: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Microsoft Trust Center: Verschlüsselung](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Cloud-Sicherheit steuert Series: Verschlüsseln von Daten im Ruhezustand](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online](exchange-online-secures-email-secrets.md) <br/> [Kontrolle über Ihre Daten in Office 365 mit Kunden-Taste](controlling-your-data-using-customer-key.md) <br/> |
|Dateien während der Übertragung zwischen Benutzern. Dies kann Office-Dokumente oder SharePoint-Listenelementen zwischen Benutzern shared enthalten.  <br/> |TLS für Dateien während der Übertragung  <br/> |[Datenverschlüsselung in OneDrive for Business und SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Skype für Unternehmen Online: Sicherheit und Archivierung](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|E-Mail während der Übertragung zwischen Empfängern. Dazu gehören e-Mail von Exchange Online gehostet.  <br/> |Office 365 Message Encryption mit Azure Rights Management, S/MIME und TLS für e-Mail während der Übertragung  <br/> |[Office 365-Nachrichtenverschlüsselung (OME)](ome.md) <br/> [E-Mail-Verschlüsselung in Office 365](email-encryption.md) <br/> [Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |
   
## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>Was passiert, wenn ich mehr benötigen Verschlüsselung Sicherheit und Richtlinientreue Anforderungen erfüllt steuern?

Zusätzlich zu Microsoft-Mitarbeiter Lösungen Volumeverschlüsselung, Verschlüsselung und Postfach Verschlüsselung in Office 365 können Kunden verwaltete Optionen strengere Sicherheits- und Compliance-Anforderungen erfüllt verwendet werden. Eine solche Lösungen mithilfe von Azure Rights Management (Azure RMS) zusammen mit Office 365.
  
Finden Sie in den folgenden Ressourcen, um mehr zu erfahren:
  
- [Was ist Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
    
- [Aktivieren der Verwaltung von Informationsrechten in Office 365 Administrationscenter](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)
    
- [Festlegen von Information Rights Management (IRM) im SharePoint Administrationscenter](set-up-irm-in-sp-admin-center.md)
    
## <a name="how-do-i"></a>Gewusst wie...

|**Für diese Aufgabe**|**Diese Ressourcen**|
|:-----|:-----|
|Einrichten von Verschlüsselung für meine Organisation  <br/> |[Einrichten von Verschlüsselung in Office 365 Enterprise.](set-up-encryption.md) <br/> |
|Anzeigen von Details zu Zertifikaten, Technologien und TLS-Verschlüsselungssammlungen in Office 365  <br/> |[Technische Details zu Verschlüsselung in Office 365](technical-reference-details-about-encryption.md) <br/> |
|Arbeiten Sie mit verschlüsselten Nachrichten auf einem mobilen Gerät  <br/> |[Anzeigen von verschlüsselten Nachrichten auf dem Android-Gerät](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [Anzeigen von verschlüsselten Nachrichten auf dem iPhone oder iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|Verschlüsseln Sie ein Dokument mit einem Kennwort  <br/></br>  Kennwortschutz wird in Office Online derzeit nicht unterstützt. Verwenden Sie für den Kennwortschutz desktop Versionen von Word, Excel und PowerPoint.           |[Hinzufügen oder Entfernen des Schutzes in Ihr Dokument, eine Arbeitsmappe oder eine Präsentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Wählen Sie einen **Add Protection** -Abschnitt, um zu sehen **mit Kennwort verschlüsseln** )  <br/> |
|Entfernen der Verschlüsselung aus einem Dokument  <br/> |[Hinzufügen oder Entfernen des Schutzes in Ihr Dokument, eine Arbeitsmappe oder eine Präsentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Wählen Sie einen Abschnitt **Entfernen Sie den Schutz** und dann finden Sie unter **Entfernen-kennwortverschlüsselungsmethode** )  <br/> |
   
## <a name="related-topics"></a>Verwandte Themen

[Planen von Office 365 und Sicherheitsinformationen Schutzfunktionen](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[Sicherheit und Einhaltung von Vorschriften in Office 365 für Unternehmen - Admin-Hilfe](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)
  

