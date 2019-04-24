---
title: Verschlüsselung in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: Mit Office 365 werden Ihre Inhalte auf Rest-und Transit Ebene verschlüsselt, wobei die stärkste Verschlüsselung, Protokolle und Technologien zur Verfügung stehen. VerSchaffen Sie sich einen Überblick über die Verschlüsselung in Office 365.
ms.openlocfilehash: 7a73d3d3b24e28f8795ec93ac05dbc383b525906
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256673"
---
# <a name="encryption-in-office-365"></a>Verschlüsselung in Office 365

Die Verschlüsselung ist ein wichtiger Teil der Strategien zum Schutz von Dateien und zum Schutz von Informationen. Lesen Sie diesen Artikel, um einen Überblick über die Verschlüsselung für alle Versionen von Office 365 zu erhalten, und erhalten Sie Hilfe zu Verschlüsselungsaufgaben, vom Einrichten der Verschlüsselung für Ihre Organisation bis zum Kennwortschutz von Office-Dokumenten.
  
- Weitere Informationen zu Zertifikaten und Technologien wie TLS finden Sie unter [technische Referenzdetails zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md).

- Weitere Informationen zum Konfigurieren oder Einrichten der Verschlüsselung für Ihre Organisation finden Sie unter [Einrichten der Verschlüsselung in Office 365 Enterprise](set-up-encryption.md).

## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>Was ist Verschlüsselung und wie funktioniert es in Office 365?

Auf hoher Ebene ist Verschlüsselung der Prozess der Codierung Ihrer Daten (als Klartext bezeichnet) in einen verschlüsselten Text, der von Personen oder Computern nur dann verwendet werden kann, wenn der Chiffretext entschlüsselt wurde. Die entSchlüsselung erfordert einen Verschlüsselungsschlüssel, den nur autorisierte Benutzer haben. Durch die Verschlüsselung wird sichergestellt, dass nur autorisierte Empfänger Ihre Inhalte wie e-Mail-Nachrichten und Dateien entschlüsseln können.
  
Die Verschlüsselung von sich aus verhindert nicht, dass Inhalte wie Dateien, e-Mail-Nachrichten, Kalendereinträge usw. in die falschen Hände gelangen. Die Verschlüsselung ist Teil einer größeren Informationsschutz Strategie für Ihre Organisation. Mithilfe der Verschlüsselung können Sie sicherstellen, dass nur diejenigen, die in der Lage sein sollen, verschlüsselte Daten zu verwenden, in der Lage sind.
  
Sie können mehrere Verschlüsselungsebenen gleichzeitig vorhanden sein. Sie können beispielsweise e-Mail-Nachrichten und auch die Kommunikationskanäle verschlüsseln, über die Ihre e-Mail fließt. Mit Office 365 werden Ihre Daten im Ruhezustand und während der Übertragung verschlüsselt, unter Verwendung mehrerer starker Verschlüsselungsprotokolle und Technologien, die Transport Layer Security/Secure Sockets Layer (TLS/SSL), IPSec (Internet Protocol Security) und erweiterte Verschlüsselung aufweisen. Standard (AES).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Verschlüsselung für Rest-Daten und Daten in der Übertragung

 **Beispiele für Rest-Daten** sind Dateien, die in eine SharePoint-Bibliothek hochgeladen wurden, Project Online-Daten, Dokumente, die in einer Skype for Business-Besprechung hochgeladen wurden, e-Mail-Nachrichten und Anlagen, die in Ordnern in ihrem Office 365 gespeichert sind. Postfächer und Dateien, die in OneDrive for Business hochgeladen werden. 
  
 **Beispiele für Daten in Transit** sind e-Mail-Nachrichten, die gerade zugestellt werden, oder Unterhaltungen, die in einer Onlinebesprechung stattfinden. In Office 365 werden die Daten immer dann übertragen, wenn das Gerät eines Benutzers mit einem Office 365-Server kommuniziert oder wenn ein Office 365-Server mit einem anderen Server kommuniziert. 
  
Mit Office 365 können Sie mehrere Ebenen und Arten der Verschlüsselung zusammenarbeiten, um Ihre Daten zu sichern. Die folgende Tabelle enthält einige Beispiele mit Links zu weiteren Informationen.
  
|**Arten von Inhalten**|**VerschlüsselungsTechnologien**|**Ressourcen für weitere Informationen**|
|:-----|:-----|:-----|
|Dateien auf einem Gerät. Dies kann e-Mail-Nachrichten in einem Ordner, Office-Dokumente, die auf einem Computer, Tablet oder Telefon gespeichert sind, oder in der Microsoft-Cloud gespeicherte Daten aufnehmen.  <br/> |BitLocker in Microsoft-Rechenzentren. BitLocker kann auch auf Clientcomputern wie Windows-Computern und Tablets verwendet werden.  <br/> Distributed Key Manager (DKM) in Microsoft-Rechenzentren  <br/> Kundenschlüssel für Office 365  <br/> |[Windows IT Center: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Microsoft Trust Center: Verschlüsselung](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Cloud Security Controls Series: verSchlüsseln von Daten im Ruhezustand](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online](exchange-online-secures-email-secrets.md) <br/> [Kontrolle über Daten in Office 365 mithilfe von Kundenschlüsseln](controlling-your-data-using-customer-key.md) <br/> |
|Dateien während der Übertragung zwischen Benutzern. Dazu können Office-Dokumente oder SharePoint-Listenelemente zwischen Benutzern freigegeben werden.  <br/> |TLS für Dateien während der Übertragung  <br/> |[Datenverschlüsselung in OneDrive for Business und SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Skype for Business Online: Sicherheit und Archivierung](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|E-Mails während der Übertragung zwischen den Empfängern. Hierzu gehören auch e-Mails, die von Exchange Online gehostet werden.  <br/> |Office 365-Nachrichtenverschlüsselung mit Azure Rights Management, S/MIME und TLS für e-Mails während der Übertragung  <br/> |[Office 365-Nachrichtenverschlüsselung (OME)](ome.md) <br/> [E-Mail-Verschlüsselung in Office 365](email-encryption.md) <br/> [Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |

## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>Was geschieht, wenn ich mehr Kontrolle über die Verschlüsselung brauche, um die Sicherheits-und Compliance-Anforderungen zu erfüllen?

Zusätzlich zu den von Microsoft verwalteten Lösungen für Volumen Verschlüsselung, Dateiverschlüsselung und Postfachverschlüsselung in Office 365 können vom Kunden verwaltete Optionen verwendet werden, um strengere Sicherheits-und Compliance-Anforderungen zu erfüllen. Diese Lösungen verwenden Azure Rights Management (Azure RMS) zusammen mit Office 365.
  
Weitere Informationen finden Sie in den folgenden Ressourcen:
  
- [Was ist Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)

- [Aktivieren der Rechteverwaltung im Office 365 Admin Center](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)

- [Set up Information Rights Management (IRM) in SharePoint admin center](set-up-irm-in-sp-admin-center.md)

## <a name="how-do-i"></a>Gewusst wie...

|**So führen Sie diese Aufgabe aus**|**Siehe diese Ressourcen**|
|:-----|:-----|
|Einrichten der Verschlüsselung für meine Organisation  <br/> |[Einrichten der Verschlüsselung in Office 365 Enterprise](set-up-encryption.md) <br/> |
|Anzeigen von Details zu Zertifikaten, Technologien und TLS-Verschlüsselungs Paketen in Office 365  <br/> |[Technische Details zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md) <br/> |
|Arbeiten mit verschlüsselten Nachrichten auf einem mobilen Gerät  <br/> |[Anzeigen von verschlüsselten Nachrichten auf Ihrem Android-Gerät](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [Verschlüsselte Nachrichten auf Ihrem iPhone oder iPad anzeigen](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|VerSchlüsseln eines Dokuments mithilfe des Kennwortschutzes  <br/><br/>  Derzeit wird der Kennwortschutz in Office Online nicht unterstützt. Verwenden Sie Desktop Versionen von Word, Excel und PowerPoint zum Kennwortschutz.           |[Hinzufügen oder Entfernen von Schutz in einem Dokument, einer Arbeitsmappe oder einer Präsentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Wählen Sie einen Abschnitt **Schutz hinzufügen** , und klicken Sie dann **auf verschlüsseln mit Kennwort** )  <br/> |
|Entfernen der Verschlüsselung aus einem Dokument  <br/> |[Hinzufügen oder Entfernen von Schutz in einem Dokument, einer Arbeitsmappe oder einer Präsentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Wählen Sie den Abschnitt **Schutz entfernen** aus, und klicken Sie dann auf **Kennwortverschlüsselung entfernen** ).  <br/> |

## <a name="related-topics"></a>Verwandte Themen

[Planen von Funktionen für Sicherheit und Informationsschutz in Office 365](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[Sicherheit und Compliance in Office 365 for Business-Administratorhilfe](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)
  

