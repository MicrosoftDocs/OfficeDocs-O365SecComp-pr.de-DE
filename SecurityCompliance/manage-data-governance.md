---
title: Verwalten von Daten Steuerung in Office 365
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 5/9/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 48064107-fed2-4db0-9e5c-aa5ddd5ccb09
description: Wenn Sie nicht, wird der Daten Governance alles über die Sicherheit für Ihre Daten um, wenn Sie es benötigen und erste entfernt. Mit Daten Governance in Office 365 können Sie den vollständige Content-Lebenszyklus verwalten, importieren und Speichern von Daten zu Beginn, bis zum Erstellen von Richtlinien, die beibehalten werden und dann endgültig löschen von Inhalt am Ende.
ms.openlocfilehash: ca3443c3b90a067bf171ddf89be604d262a7b9a4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529969"
---
# <a name="manage-data-governance-in-office-365"></a>Verwalten von Daten Steuerung in Office 365

Wenn Sie nicht, wird der Daten Governance alles über die Sicherheit für Ihre Daten um, wenn Sie es benötigen und erste entfernt. Mit Daten Governance in Office 365 können Sie den vollständige Content-Lebenszyklus verwalten, importieren und Speichern von Daten zu Beginn, bis zum Erstellen von Richtlinien, die beibehalten werden und dann endgültig löschen von Inhalt am Ende.
  
## <a name="import"></a>Importieren

Einige Ihrer Daten möglicherweise an Orten außerhalb der Cloud, wie der lokale Server oder in der Drittanbieter-apps gespeichert werden. Der Import-Dienst erleichtert Ihnen, Ihre messaging, SharePoint und OneDrive für Geschäftsdaten in Office 365, entweder durch Hochladen direkt über das Netzwerk oder ein verschlüsseltes Laufwerk für uns shipping aufzurufen. Sie können auch das intelligenten Importfeature im Import-Dienst zum Filtern der Elemente in PST-Dateien, die tatsächlich auf die Postfächer Ziel importiert. 
  
- [Übersicht über das Importieren von PST-Dateien in Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84)
    
- [Verwenden des Netzwerkuploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md)
    
- [Verwenden des Laufwerkversands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- [Verwenden Sie das PST-Auflistung-Tool zu suchen, kopieren und Löschen von PST-Dateien in Ihrer Organisation](find-copy-and-delete-pst-files-in-your-organization.md)
    
- [Filtern von Daten beim Importieren von PST-Dateien in Office 365](filter-data-when-importing-pst-files.md)
    
- [Hochladen lokaler Inhalte in SharePoint Online mithilfe von PowerShell-Cmdlets](https://support.office.com/article/555049c6-15ef-45a6-9a1f-a1ef673b867c)
    
## <a name="govern-i-store-data"></a>Steuern von I: Speichern von Daten

Nachdem Sie Daten importieren, müssen Sie möglicherweise Ihren Speicher erhöhen. Das Feature für unbegrenzte Archivierung in Office 365 (gewählte erweiterbares Archivierung) bietet eine unbegrenzte Zeitspanne Speicher in archivpostfächer.
  
- [Aktivieren von archivpostfächern in die Office 365-Sicherheit &amp; Compliance Center](enable-archive-mailboxes.md)

- [Übersicht über die uneingeschränkte Archivierung in Office 365](unlimited-archiving.md)
    
- [Aktivieren Sie die uneingeschränkte Archivierung in Office 365](enable-unlimited-archiving.md)
    

    
## <a name="govern-ii-create-policies-and-labels-to-retain-content"></a>Steuern II: Erstellen von Richtlinien und Beschriftungen, die Inhalt beibehalten werden.

Eine Aufbewahrungsrichtlinie hilft Ihnen, proaktiv durch sicherstellen, dass Sie, solange sich aber nicht mehr erforderlich ist als die Inhalte beibehält mit rechtlichen Vorschriften und internen Richtlinien entsprechen. Eine einzelne Aufbewahrungsrichtlinie kann die gesamte Organisation umfassen. Darüber hinaus können Sie Etiketten ein Dateiplans implementieren, durch die Klassifizierung der Daten in Ihrer Organisation für die Steuerung, und klicken Sie dann Durchsetzung Aufbewahrungsregeln basierend auf Klassifikation.
  
- [Übersicht über die Aufbewahrungsrichtlinien](retention-policies.md)
    
- [Übersicht über Etiketten](labels.md)
    
- [Massen erstellen und Veröffentlichen von Etiketten mithilfe von PowerShell](https://support.office.com/article/8986701b-ffa1-46ec-8fd0-8f7e81d5b25f.aspx)
    
- [Übersicht über die Disposition Reviews (engl.)](disposition-reviews.md)
    
- [Übersicht über die ereignisgesteuerte Aufbewahrung](event-driven-retention.md)
    
## <a name="govern-iii-retain-the-email-of-former-employees"></a>III steuern bei: Behalten Sie die e-Mail-Adresse des frühere Mitarbeiter

Wenn eine Person die Organisation verlässt, können Sie ihre e-Mails durch Erstellen eines inaktiven Postfachs beibehalten. Ein Postfach wird inaktiv, wenn eine Aufbewahrung für eventuelle Rechtsstreitigkeiten Aufbewahrungsrichtlinie für Office 365, oder andere Art von Haltestatus angewendet wird, und klicken Sie dann das entsprechende Office 365-Benutzerkonto wird gelöscht. Elemente in eines inaktiven Postfachs werden für die Dauer der Richtlinie halten oder die Aufbewahrung weitergeführt, die für das Postfach getätigt wurde, bevor sie als inaktiv festgelegt wurde.
  
- [Übersicht über inaktiver Postfächer in Office 365](inactive-mailboxes-in-office-365.md)
    
- [Erstellen Sie und verwalten Sie inaktiver Postfächer in Office 365](create-and-manage-inactive-mailboxes.md)

- [Ändern Sie die Dauer halten eines inaktiven Postfachs in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)
  
- [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md)
 
- [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md)

- [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)

## <a name="monitor"></a>Überwachen

Überwachung können Sie Richtlinien definieren, die e-Mail- und 3rd Party Communications in Ihrer Organisation erfassen, damit diese von internen oder externen Prüfern überprüft werden können. Bearbeiter können dann klassifizieren diese Communications, stellen Sie sicher, dass sie mit Ihrer Organisation Richtlinien kompatibel sind und fragwürdige Material ausweiten, falls erforderlich.
  
Sie können auch die Steuerung Datenberichte und die Bezeichnung Aktivität Explorer überwachen, dass Ihre Etiketten wie gewünscht auf Inhalte angewendet werden.
  
- [Konfigurieren von Richtlinien für Ihre Organisation Überwachung](configure-supervision-policies.md)
    
- [Überwachung Berichte](supervision-reports.md)
    
- [Label-Aktivität für Dokumente anzeigen](view-label-activity-for-documents.md)
    
- [Anzeigen der Daten Governance-Berichte](view-the-data-governance-reports.md)
    
## <a name="more-information"></a>Weitere Informationen

- [Sehen Sie sich Videos des Teams für Microsoft Data Governance](https://go.microsoft.com/fwlink/?linkid=867039)
    
- [Sehen Sie sich einen Überblick über die Steuerung von Daten in Office 365](https://go.microsoft.com/fwlink/?linkid=852644)
    
- [Office 365-Sicherheit &amp; Compliance Center-Cmdlets](https://go.microsoft.com/fwlink/?linkid=852310)
    

