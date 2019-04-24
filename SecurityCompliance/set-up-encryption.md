---
title: Einrichten von Verschlüsselung in Office 365 Enterprise
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/2/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e86fc991-0161-4f01-9c1c-d25e87733d06
description: Bei Office 365 sind einige Verschlüsselungsfunktionen standardmäßig aktiviert. andere Funktionen können so konfiguriert werden, dass bestimmte Compliance-oder gesetzliche Anforderungen erfüllt werden.
ms.openlocfilehash: 1bc4ceb7762c96f55c03f89e7c448f9e4073063e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260793"
---
# <a name="set-up-encryption-in-office-365-enterprise"></a>Einrichten von Verschlüsselung in Office 365 Enterprise

Die Verschlüsselung kann verhindern, dass Ihre Inhalte von nicht autorisierten Benutzern gelesen werden. Da die [Verschlüsselung in Office 365](encryption.md) mit verschiedenen Technologien und Methoden durchgeführt werden kann, gibt es keinen einzigen Ort, an dem Sie die Verschlüsselung aktivieren oder einrichten. Dieser Artikel enthält Informationen zu verschiedenen Methoden zum Einrichten oder Konfigurieren der Verschlüsselung im Rahmen ihrer Strategie zum Schutz von Informationen.
  
> [!TIP]
> Weitere technische Details zur Verschlüsselung finden Sie unter [technische Referenzdetails zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md).
  
Mit Office 365 stehen standardmäßig mehrere Verschlüsselungsfunktionen zur Verfügung. Zusätzliche Verschlüsselungsfunktionen können so konfiguriert werden, dass bestimmte Compliance-oder gesetzliche Anforderungen erfüllt werden. In der folgenden Tabelle werden verschiedene Verschlüsselungsmethoden für verschiedene Szenarien beschrieben.
  
|**Szenario**|**VerschlüsselungsMethoden**|
|:-----|:-----|
|Dateien werden auf Windows-Computern gespeichert  <br/> |Die Verschlüsselung auf Computerebene kann mithilfe von BitLocker auf Windows-Geräten ausgeführt werden. Als Unternehmensadministrator oder IT-Experte können Sie dies mithilfe des Microsoft Deployment Toolkit (MDT) einrichten. Weitere Informationen finden Sie unter [Einrichten von MDT für BitLocker](https://go.microsoft.com/fwlink/?linkid=849282).  <br/> |
|Dateien werden auf mobilen Geräten gespeichert  <br/> |Einige Arten von mobilen Geräten verschlüsseln Dateien, die standardmäßig auf diesen Geräten gespeichert werden. Mit den [Funktionen der integrierten Verwaltung mobiler Geräte für office 365](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0)können Sie Richtlinien festlegen, die festlegen, ob mobilen Geräten der Zugriff auf Daten in Office 365 ermöglicht werden soll. Sie können beispielsweise eine Richtlinie festlegen, mit der nur Geräte, die Inhalt verschlüsseln, auf Office 365-Daten zugreifen können. Weitere Informationen finden Sie unter [Erstellen und Bereitstellen von Gerätesicherheitsrichtlinien](https://support.office.com/article/d310f556-8bfb-497b-9bd7-fe3c36ea2fd6).  <br/> Eine zusätzliche Kontrolle darüber, wie mobile Geräte mit Office 365 interagieren, können Sie [Microsoft InTune](https://aka.ms/qzln04)hinzufügen. Weitere Informationen finden Sie unter [Choose zwischen MDM für Office 365 und Microsoft InTune](https://support.office.com/article/c93d9ab9-efb2-4349-9b93-30c30562ee22).  <br/> |
|Sie benötigen die Kontrolle über die Verschlüsselungsschlüssel, die zum Verschlüsseln Ihrer Daten in Microsoft-Rechenzentren verwendet werden.  <br/> | Als Office 365-Administrator können Sie die Verschlüsselungsschlüssel Ihrer Organisation steuern und dann Office 365 so konfigurieren, dass Sie zum Verschlüsseln Ihrer Daten in den Datencentern von Microsoft verwendet werden.  <br/> [Kontrolle über Daten in Office 365 mithilfe von Kundenschlüsseln](controlling-your-data-using-customer-key.md) <br/> [Kundenschlüssel für Office 365 – häufig gestellte Fragen](service-encryption-with-customer-key-faq.md) <br/> |
|Personen kommunizieren per e-Mail (Exchange Online)  <br/> | Als Exchange Online-Administrator haben Sie mehrere Optionen zum Konfigurieren der e-Mail-Verschlüsselung. Zu diesen zählen:  <br/>  Verwenden der [Office 365-Nachrichtenverschlüsselung (OM)](set-up-new-message-encryption-capabilities.md) mit Azure Rights Management (Azure RMS), damit Personen verschlüsselte Nachrichten innerhalb oder außerhalb Ihrer Organisation senden können  <br/>  Verwenden [von S/MIME für die Nachrichtensignierung und-Verschlüsselung](https://aka.ms/c6dozg) zum Verschlüsseln und digitalen Signieren von e-Mail-Nachrichten  <br/>  Verwenden von TLS zum [Einrichten von Connectors für den sicheren e-Mail-Fluss mit einer anderen Organisation](https://aka.ms/hs809p) <br/>  Weitere Informationen finden Sie unter [e-Mail-Verschlüsselung in Office 365](https://aka.ms/hic3f7).  <br/> |
|Zugriff auf Dateien über Teamwebsites oder Dokumentbibliotheken (OneDrive for Business oder SharePoint Online)  <br/> |Wenn Benutzer mit Dateien arbeiten, die in OneDrive for Business oder SharePoint Online gespeichert sind, werden TLS-Verbindungen verwendet. Dies ist in Office 365 automatisch integriert. Siehe [Datenverschlüsselung in OneDrive for Business und SharePoint Online](https://go.microsoft.com/fwlink/?linkid=526379).  <br/> |
|Dateien werden in Onlinebesprechungen und Chat Unterhaltungen freigegeben (Skype for Business Online)  <br/> |Wenn Benutzer mit Skype for Business Online-Dateien arbeiten, wird TLS für die Verbindung verwendet. Dies ist in Office 365 automatisch integriert. Siehe [Sicherheit und Archivierung (Skype for Business Online)](https://aka.ms/nuq4ws).  <br/> |

## <a name="additional-information"></a>Weitere Informationen

Weitere Informationen zu Lösungen zum Schutz von Dateien, die Verschlüsselungsoptionen aufweisen, finden Sie unter [File Protection Solutions in Office 365](https://www.microsoft.com/en-us/download/details.aspx?id=55523).