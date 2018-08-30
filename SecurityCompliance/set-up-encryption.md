---
title: Einrichten von Verschlüsselung in Office 365 Enterprise.
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/2/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e86fc991-0161-4f01-9c1c-d25e87733d06
description: Mit Office 365 sind einige Verschlüsselungsfunktionen standardmäßig aktiviert; andere Funktionen können konfiguriert werden, um bestimmte Compliance oder rechtlichen Anforderungen erfüllen.
ms.openlocfilehash: 80deced80283ac36d82ac15cee9af6d390c4749a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529200"
---
# <a name="set-up-encryption-in-office-365-enterprise"></a>Einrichten von Verschlüsselung in Office 365 Enterprise.

Verschlüsselung kann verhindern, dass Ihre Inhalte, die durch nicht autorisierte Benutzer gelesen werden. Da [Verschlüsselung in Office 365](encryption.md) erfolgen kann mithilfe verschiedener Technologien und Methoden eine zentrale Stelle, wo Sie aktivieren oder Einrichten von Verschlüsselung, nicht vorhanden ist. Dieser Artikel enthält Informationen zu verschiedenen Methoden, die können Sie festlegen oder konfigurieren Sie die Verschlüsselung als Teil Ihrer Strategie zum Schutz. 
  
> [!TIP]
> Wenn Sie ausführliche technische Informationen zur Verschlüsselung suchen, finden Sie unter [Technische Referenz Details über die Verschlüsselung in Office 365](technical-reference-details-about-encryption.md). 
  
Mit Office 365 sind mehrere Verschlüsselungsfunktionen standardmäßig verfügbar. Zusätzliche Verschlüsselungsfunktionen können konfiguriert werden, um bestimmte Compliance oder rechtlichen Anforderungen erfüllen. In der folgenden Tabelle werden verschiedene Verschlüsselungsmethoden für verschiedene Szenarien beschrieben.
  
|**Szenario**|**Verschlüsselungsmethoden**|
|:-----|:-----|
|Dateien werden auf Computern mit Windows gespeichert.  <br/> |Verschlüsselung auf Computerebene erfolgen BitLocker auf Windows-Geräten verwenden. Als Unternehmensadministrator oder IT-Spezialisten können Sie dies mit dem Microsoft Deployment Toolkit (MDT) festlegen. Finden Sie unter [Einrichten von MDT für BitLocker](https://go.microsoft.com/fwlink/?linkid=849282).<br/> |
|Dateien werden auf mobilen Geräten gespeichert.  <br/> |Einige Arten von mobilen Geräten Verschlüsseln von Dateien, die in der Standardeinstellung für diese Geräte gespeichert sind. Mit den [Funktionen von integrierten Verwaltung mobiler Geräte für Office 365](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0)können Sie Richtlinien festlegen, die bestimmen, ob mobile Geräte Zugriff auf Daten in Office 365 dürfen. Beispielsweise können Sie eine Richtlinie festlegen, die nur, die Inhalte ermöglicht für Office 365 für den Datenzugriff zu verschlüsseln. Finden Sie unter [Erstellen und Bereitstellen von Sicherheitsrichtlinien für Geräte](https://support.office.com/article/d310f556-8bfb-497b-9bd7-fe3c36ea2fd6).<br/> Mit Office 365 für zusätzliche Kontrolle über von mobilen Geräten interagieren, können Sie das Hinzufügen von [Microsoft Intune](https://aka.ms/qzln04)betrachten. Finden Sie unter [entscheiden, ob MDM für Office 365 und Microsoft Intune](https://support.office.com/article/c93d9ab9-efb2-4349-9b93-30c30562ee22).<br/> |
|Sie benötigen die Kontrolle über die Verschlüsselungsschlüssel zum Verschlüsseln von Daten in Microsoft Rechenzentren  <br/> | Als Office 365-Administrator können Sie steuern Ihres Unternehmens Verschlüsselungsschlüssel und Office 365, um ihre Verwendung zum Verschlüsseln von Ihrer Daten im Ruhezustand in Microsoft Rechenzentren konfigurieren.  <br/> [Kontrolle über Ihre Daten in Office 365 mit Kunden-Taste](controlling-your-data-using-customer-key.md) <br/> [Kunden-Keys für Office 365 – häufig gestellte Fragen](service-encryption-with-customer-key-faq.md) <br/> |
|Personen kommunizieren per e-Mail (Exchange Online)  <br/> | Als Exchange Online-Administrator haben Sie mehrere Optionen zum Konfigurieren der e-Mail-Verschlüsselung. Dazu zählen folgende:<br/>  Verwenden von [Office 365-nachrichtenverschlüsselung (OME)](set-up-new-message-encryption-capabilities.md) mit Azure-Rechteverwaltung (RMS Azure) zum ermöglichen des Personen zum Senden verschlüsselter Nachrichten innerhalb oder außerhalb Ihrer Organisation  <br/>  Verwenden von [S/MIME für die nachrichtensignierung und-Verschlüsselung](https://aka.ms/c6dozg) zum Verschlüsseln und digitales Signieren von e-Mail-Nachrichten  <br/>  Verwendung von TLS zum [Einrichten von Connectors für die sichere Nachrichtenübermittlung mit einer anderen Organisation](https://aka.ms/hs809p) <br/>  Finden Sie unter [e-Mail-Verschlüsselung in Office 365](https://aka.ms/hic3f7).  <br/> |
|Dateien werden von Teamwebsites oder Dokumentbibliotheken (OneDrive for Business oder SharePoint Online) zugegriffen werden.  <br/> |Wenn Personen mit OneDrive for Business oder SharePoint Online gespeicherte Dateien arbeiten, werden die TLS-Verbindungen verwendet. Dadurch wird automatisch in Office 365 integriert. Finden Sie unter [Data Encryption in OneDrive für Unternehmen und SharePoint Online](https://go.microsoft.com/fwlink/?linkid=526379).<br/> |
|Dateien werden in onlinebesprechungen und Sofortnachrichtenunterhaltungen (Skype für Business Online) freigegeben.  <br/> |Wenn Personen mit Dateien mithilfe von Skype für Business Online arbeiten, ist TLS für die Verbindung verwendet. Dadurch wird automatisch in Office 365 integriert. Finden Sie unter [Security and Archiving (Skype für Online Business)](https://aka.ms/nuq4ws).<br/> |
   
## <a name="additional-information"></a>Weitere Informationen

Weitere Informationen zu Lösungen zum Schutz, die Optionen zur Verschlüsselung enthalten, finden Sie unter [Datei Protection Solutions in Office 365](https://www.microsoft.com/en-us/download/details.aspx?id=55523).
  

