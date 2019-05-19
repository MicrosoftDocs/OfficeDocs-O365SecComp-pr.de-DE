---
title: Verschlüsselung in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
audience: Admin
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
description: Mit Office 365 werden Ihre Inhalte im Ruhezustand und in der Übertragung verschlüsselt, wobei die stärkste Verschlüsselung, die verfügbaren Protokolle und Technologien verwendet werden. Erhalten Sie eine Übersicht über die Verschlüsselung in Office 365.
ms.openlocfilehash: 3cd72b3caf26c18ca6836490bc3cd48c2977863b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154717"
---
# <a name="encryption-in-office-365"></a>Verschlüsselung in Office 365

Die Verschlüsselung ist ein wichtiger Bestandteil ihrer Strategien für Dateischutz und Informationsschutz. Lesen Sie diesen Artikel, um eine Übersicht über die Verschlüsselung zu erhalten, die für alle Versionen von Office 365 verwendet wird, und erhalten Sie Hilfe bei Verschlüsselungsaufgaben, von der Einrichtung der Verschlüsselung für Ihre Organisation bis zum Kennwortschutz für Office-Dokumente.
  
- Wenn Sie nach Informationen zu Zertifikaten und Technologien wie TLS suchen, lesen Sie [technische Referenzdetails zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md).

- Wenn Sie nach Informationen zum Konfigurieren oder Einrichten der Verschlüsselung für Ihre Organisation suchen, finden Sie weitere Informationen unter [Einrichten der Verschlüsselung in Office 365 Enterprise](set-up-encryption.md).

## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>Was ist Verschlüsselung und wie funktioniert Sie in Office 365?

Bei der Verschlüsselung handelt es sich um den Prozess der Codierung Ihrer Daten (als Klartext bezeichnet) in einen verschlüsselten Text, der von Personen oder Computern nur dann verwendet werden kann, wenn der Text verschlüsselt wird. Für die Entschlüsselung ist ein Verschlüsselungsschlüssel erforderlich, den nur autorisierte Benutzer besitzen. Durch die Verschlüsselung wird sichergestellt, dass nur autorisierte Empfänger Ihre Inhalte wie e-Mail-Nachrichten und Dateien entschlüsseln können.
  
Durch die Verschlüsselung selbst wird nicht verhindert, dass Inhalte wie Dateien, e-Mail-Nachrichten, Kalendereinträge und so weiter in die falschen Hände gelangen. Die Verschlüsselung ist Teil einer umfassenderen Informationsschutz Strategie für Ihre Organisation. Mithilfe der Verschlüsselung können Sie sicherstellen, dass nur diejenigen, die in der Lage sind, verschlüsselte Daten zu verwenden, in der Lage sind.
  
Sie können mehrere Verschlüsselungsebenen gleichzeitig einsetzen. Beispielsweise können Sie e-Mail-Nachrichten und auch die Kommunikationskanäle verschlüsseln, über die Ihre e-Mails fließt. Mit Office 365 werden Ihre Daten im Ruhezustand und in der Übertragung verschlüsselt, wobei mehrere starke Verschlüsselungsprotokolle und Technologien verwendet werden, die Transport Layer Security/Secure Sockets Layer (TLS/SSL), Internet Protocol Security (IPSec) und erweiterte Verschlüsselung umfassen. Standard (AES).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Verschlüsselung von Daten im Ruhezustand und Daten während der Übertragung

 **Beispiele für Daten im Ruhezustand** sind Dateien, die in eine SharePoint-Bibliothek hochgeladen wurden, Project Online Daten, Dokumente, die in einer Skype for Business Besprechung hochgeladen wurden, e-Mail-Nachrichten und Anlagen, die in Ordnern in Ihrem Office 365 gespeichert sind. das Postfach und die Dateien, die in OneDrive für Unternehmen hochgeladen wurden. 
  
 **Beispiele für Daten in Transit** sind e-Mail-Nachrichten, die gerade zugestellt werden, oder Unterhaltungen, die in einer Onlinebesprechung stattfinden. In Office 365 werden Daten immer dann übertragen, wenn das Gerät eines Benutzers mit einem Office 365-Server kommuniziert oder wenn ein Office 365 Server mit einem anderen Server kommuniziert. 
  
Mit Office 365 können Sie mehrere Ebenen und Verschlüsselungsarten zusammenarbeiten, um Ihre Daten zu schützen. Die folgende Tabelle enthält einige Beispiele mit Links zu zusätzlichen Informationen.
  
|**Arten von Inhalten**|**Verschlüsselungstechnologien**|**Ressourcen für weitere Informationen**|
|:-----|:-----|:-----|
|Dateien auf einem Gerät. Dies kann e-Mail-Nachrichten enthalten, die in einem Ordner gespeichert sind, auf einem Computer, einem Tablet oder einem Telefon gespeicherte Office-Dokumente oder in der Microsoft-Cloud gespeicherte Daten.  <br/> |BitLocker in Microsoft-Datencentern. BitLocker kann auch auf Clientcomputern verwendet werden, wie Windows-Computer und Tablets  <br/> Distributed Key Manager (DKM) in Microsoft-Rechenzentren  <br/> Kundenschlüssel für Office 365  <br/> |[Windows-IT-Center: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Microsoft Trust Center: Verschlüsselung](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Cloud Security Controls Series: Verschlüsseln von Daten im Ruhezustand](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online](exchange-online-secures-email-secrets.md) <br/> [Kontrolle über Daten in Office 365 mithilfe von Kundenschlüsseln](controlling-your-data-using-customer-key.md) <br/> |
|Dateien während der Übertragung zwischen Benutzern. Dies kann Office-Dokumente oder SharePoint-Listenelemente sein, die von Benutzern gemeinsam verwendet werden.  <br/> |TLS für Dateien während der Übertragung  <br/> |[Datenverschlüsselung in OneDrive for Business und SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Skype for Business Online: Sicherheit und Archivierung](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|E-Mails während der Übertragung zwischen Empfängern. Hierzu gehören auch von Exchange Online gehostete e-Mails.  <br/> |Office 365 Nachrichtenverschlüsselung mit Azure Rights Management, S/MIME und TLS für e-Mails bei der Übertragung  <br/> |[Office 365-Nachrichtenverschlüsselung (OME)](ome.md) <br/> [E-Mail-Verschlüsselung in Office 365](email-encryption.md) <br/> [Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |

## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>Was ist, wenn ich mehr Kontrolle über die Verschlüsselung brauche, um Sicherheits-und Compliance-Anforderungen zu erfüllen?

Zusätzlich zu den von Microsoft verwalteten Lösungen von Volumen Verschlüsselung, Dateiverschlüsselung und Postfachverschlüsselung in Office 365 können Kunden verwaltete Optionen verwendet werden, um strengere Sicherheits-und Compliance-Anforderungen zu erfüllen. Solche Lösungen verwenden Azure Rights Management (Azure RMS) zusammen mit Office 365.
  
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
|Verschlüsseln eines Dokuments mithilfe des Kennwortschutzes  <br/><br/>  Derzeit wird der Kennwortschutz in Office Online nicht unterstützt. Verwenden Sie Desktop Versionen von Word, Excel und PowerPoint für den Kennwortschutz.           |[Hinzufügen oder Entfernen von Schutz in Ihrem Dokument, in einer Arbeitsmappe oder in einer Präsentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Wählen Sie einen Abschnitt **Schutz hinzufügen** aus, und sehen Sie dann verschlüsseln **mit Kennwort** )  <br/> |
|Entfernen der Verschlüsselung aus einem Dokument  <br/> |[Hinzufügen oder Entfernen von Schutz in Ihrem Dokument, in einer Arbeitsmappe oder in einer Präsentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Wählen Sie einen Abschnitt zum **Entfernen des Schutzes** aus, und entfernen Sie dann die **Kennwortverschlüsselung** )  <br/> |

## <a name="related-topics"></a>Verwandte Themen

[Planen der Office 365 Funktionen für Sicherheits-und Informationsschutz](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[Sicherheit und Compliance in Office 365 für Unternehmen – Administratorhilfe](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)