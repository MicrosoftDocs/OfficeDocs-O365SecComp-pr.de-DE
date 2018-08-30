---
title: Verwaltung von Informationsrechten in Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/13/2017
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2c956776-0016-4be6-b4cd-133a237f4a9e
description: Häufig werden vertrauliche Informationen wie Finanzdaten, Verträge, vertrauliche Produktinformationen, Verkaufsberichte und -prognosen oder Patienten-, Kunden- und Mitarbeiterdaten per E-Mail ausgetauscht. Postfächer können daher zu Repositories großer Mengen potenziell vertraulicher Informationen werden, und Informationsverluste können eine ernstzunehmende Bedrohung für die Organisation darstellen.
ms.openlocfilehash: 5036fe359215de1c2674d7efabbb283c78418a19
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002566"
---
# <a name="information-rights-management-in-exchange-online"></a>Verwaltung von Informationsrechten in Exchange Online

Häufig werden vertrauliche Informationen wie Finanzdaten, Verträge, vertrauliche Produktinformationen, Verkaufsberichte und -prognosen oder Patienten-, Kunden- und Mitarbeiterdaten per E-Mail ausgetauscht. Postfächer können daher zu Repositories großer Mengen potenziell vertraulicher Informationen werden, und Informationsverluste können eine ernstzunehmende Bedrohung für die Organisation darstellen.
  
Um Informationsverluste zu verhindern, enthält Exchange Online eine IRM-Funktion (Verwaltung von Informationsrechten), die Online- und Offlineschutz für E-Mails und Anlagen bereitstellt. IRM-Schutz kann von Benutzern in Microsoft Outlook oder Outlook im Web und zudem von Administratoren mithilfe von Transportschutzregeln oder Outlook-Schutzregeln angewendet werden. Mithilfe von IRM können Sie und Ihre Benutzer steuern, wer auf vertrauliche Daten in einer E-Mail zugreifen und E-Mails weiterleiten, drucken oder kopieren kann.
  
## <a name="changes-to-how-irm-works-with-office-365-message-encryption-ome-and-azure-active-directory"></a>Änderungen an der Funktionsweise von IRM mit Office 365-Nachrichtenverschlüsselung (OME) und Azure Active Directory

Ab September 2017: Wenn Sie die neuen Funktionen von Office 365-Nachrichtenverschlüsselung für Ihre Organisation einrichten, richten Sie auch IRM für die Verwendung mit Azure Rights Management (Azure RMS) ein. Sie richten IRM nicht mehr separat mit Azure RMS ein. Stattdessen arbeiten OME und Rights Management nahtlos zusammen. Ausführliche Informationen über die neuen Funktionen finden Sie in den [Häufig gestellten Fragen zur Office 365-Nachrichtenverschlüsselung](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e). Wenn Sie die neuen OME-Funktionen in Ihrer Organisation verwenden möchten, finden Sie unter [Einrichten von neuen Funktionen für die Office 365-Nachrichtenverschlüsselung, die auf Azure Information Protection aufbauen](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e) weitere Informationen dazu.
  
## <a name="how-irm-works-with-exchange-online-and-active-directory-rights-management-services"></a>Funktionsweise von IRM in Exchange Online und Active Directory Rights Management Services

Für IRM in Exchange Online werden die lokalen Active Directory-Rechteverwaltungsdienste (AD RMS) verwendet, eine Informationsschutztechnologie in Windows Server 2008 und höher. IRM-Schutz wird auf E-Mails angewendet, indem eine AD RMS-Berechtigungsrichtlinienvorlage auf eine E-Mail angewendet wird. Rechte werden der Nachricht selbst zugeordnet, sodass der Schutz sowohl online und offline als auch innerhalb und außerhalb der Firewall der Organisation stattfindet.
  
Benutzer können eine Vorlage auf eine E-Mail anwenden, um zu steuern, welche Berechtigungen Empfänger für die E-Mail erhalten. Aktionen wie das Extrahieren von Informationen aus einer Nachricht, Weiterleiten, Speichern oder Drucken einer Nachricht können durch Anwenden einer AD RMS-Rechterichtlinie auf die Nachricht gesteuert werden.
  
Sie können IRM für die Verwendung eines AD RMS-Servers mit Windows Server 2008 oder höher konfigurieren. Dieser AD RMS-Server wird zum Verwalten der AD RMS-Rechterichtlinienvorlagen für die cloudbasierte Organisation verwendet. Der AD RMS-Server wird von Outlook auch verwendet, um Benutzern das Anwenden von IRM-Schutz auf die von ihnen gesendeten Nachrichten zu ermöglichen. Weitere Informationen finden Sie unter [Configure IRM to use an on-premises AD RMS server](configure-irm-to-use-an-on-premises-ad-rms-server.md). 
  
Nach der Aktivierung kann IRM-Schutz auf Nachrichten wie folgt angewendet werden:
  
- **Benutzer können eine Vorlage manuell mit Outlook und Outlook im Web anwenden** Benutzer können eine AD RMS-Rechterichtlinienvorlage auf eine E-Mail-Nachricht anwenden, indem sie die Vorlage aus der Liste **Berechtigungen festlegen** auswählen. Wenn Benutzer eine IRM-geschützte Nachricht senden, erhalten alle an die Nachricht angefügten Dateien in einem unterstützten Format den gleichen IRM-Schutz wie die Nachricht. IRM-Schutz wird auf Dateien aus Microsoft Office Word, Excel und PowerPoint sowie XPS-Dateien und angefügte E-Mails angewendet. 
    
- **Administratoren können mithilfe von Transportregeln automatisch IRM-Schutz auf Outlook und Outlook im Web anwenden** Sie können Transportregeln erstellen, um IRM-Schutz für Nachrichten bereitzustellen. Konfigurieren Sie die Transportschutzregelaktion, um eine AD RMS-Rechterichtlinienvorlage auf Nachrichten anzuwenden, die die Regelbedingung erfüllen. Nach dem Aktivieren von IRM sind die AD RMS-Rechterichtlinienvorlagen zur Verwendung mit der Transportschutzregelaktion **Rechteschutz auf Nachricht anwenden mit** verfügbar.
    
- **Administratoren können Outlook-Schutzregeln erstellen.** Durch Outlook-Schutzregeln wird basierend auf Nachrichtenbedingungen wie der Abteilung des Absenders, dem Empfänger und dem Empfängerbereich (innerhalb oder außerhalb der Organisation) automatisch IRM-Schutz auf Nachrichten in Outlook 2010 angewendet (nicht in Outlook im Web). Weitere Informationen finden Sie unter [Create an Outlook Protection Rule](http://technet.microsoft.com/library/da64750d-faaf-44de-ad8c-888eba7fbdbf.aspx).
    

