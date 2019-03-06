---
title: Übersicht über die Disposition Reviews
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Wenn Sie eine Bezeichnung erstellen, in der Inhalte in Office 365 aufbewahrt werden, können Sie eine Disposition-Überprüfungen am Ende des Aufbewahrungszeitraums auslösen.
ms.openlocfilehash: a3125ee3f0ae388fce71968f25a68d5ccf3fc652
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410760"
---
# <a name="overview-of-disposition-reviews"></a>Übersicht über die Disposition Reviews

Wenn der Inhalt das Ende seines Aufbewahrungszeitraums erreicht hat, gibt es mehrere Gründe, warum Sie diesen Inhalt überprüfen möchten, um zu entscheiden, ob er sicher gelöscht werden kann ("verworfen"). Beispielsweise müssen Sie Folgendes tun:
  
- UnterBrechen des Löschens ("Disposition") relevanter Inhalte im Fall eines Rechtsstreits oder einer Überwachung.
    
- Entfernen Sie Inhalte aus der Dispositionsliste, um Sie in einem Archiv zu speichern, wenn dieser Inhalt Forschungs-oder Verlaufswerte aufweist.
    
- Weisen Sie dem Inhalt einen anderen Aufbewahrungszeitraum zu, wenn die ursprüngliche Richtlinie eine temporäre oder provisorische Lösung war.
    
- Den Inhalt an Clients zurückgeben oder an eine andere Organisation übertragen.
    
Wenn Sie eine Bezeichnung erstellen, in der Inhalte in Office 365 aufbewahrt werden, können Sie eine Disposition-Überprüfungen am Ende des Aufbewahrungszeitraums auslösen. Bei einer Disposition:
  
- Die Personen, die Sie auswählen, erhalten eine e-Mail-Benachrichtigung, dass Sie Inhalte zur Überarbeitung haben. Diese Prüfer können einzelne Benutzer, Verteiler-oder Sicherheitsgruppen oder Office 365-Gruppen sein. Beachten Sie, dass Benachrichtigungen wöchentlich gesendet werden.
    
- Die Bearbeiter wechseln zur Seite " **Disposition** " im Security &amp; Compliance Center, um den Inhalt zu Überprüfung. 
    
- Für jedes Dokument kann der Prüfer Folgendes tun:
    
  - Anwenden einer anderen Bezeichnung
    
  - Verlängern des Aufbewahrungszeitraums.
    
  - Endgültig löschen.
    
- Prüfer können ausstehende oder historische Dispositionen anzeigen und diese Liste als CSV-Datei exportieren.
    
Beachten Sie, dass für Dispositions Prüfungen ein Office 365 Enterprise E5-Abonnement erforderlich ist.
  
Eine Disposition-Überprüfungen kann Inhalte in Exchange-Postfächern, SharePoint-Websites, OneDrive-Konten und Office 365-Gruppen einbeziehen. Inhalte, die auf eine Disposition-Überprüfungen an diesen Speicherorten warten, werden erst gelöscht, nachdem ein Prüfer die Inhalte endgültig gelöscht hat.
  
![DisPositions Seite](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a>Einrichten der Disposition-Überprüfungen durch Erstellen einer Bezeichnung

Dies ist der grundlegende Workflow für das Einrichten einer Disposition-Überprüfungen. Beachten Sie, dass dieser Fluss eine Beschriftung anzeigt, die veröffentlicht und dann von einem Benutzer manuell angewendet wird. Alternativ kann eine Bezeichnung, die eine Dispositions Überprüfung auslöst, automatisch auf Inhalte angewendet werden.
  
![Diagramm mit dem Ablauf der Funktionsweise der Disposition](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
Eine Dispositions Überprüfung ist eine Option, wenn Sie eine Bezeichnung in Office 365 erstellen. Beachten Sie, dass diese Option nicht in einer Aufbewahrungsrichtlinie, sondern nur in einer Bezeichnung mit Aufbewahrungseinstellungen verfügbar ist.
  
Weitere Informationen über Bezeichnungen finden Sie unter [Übersicht über Bezeichnungen](labels.md).
  
![Aufbewahrungseinstellungen für eine Bezeichnung](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>Freigeben von Inhalten

Wenn ein Prüfer per e-Mail benachrichtigt wird, dass der Inhalt bereit ist, zu überprüfen, können Sie die Seite " **Disposition** " im &amp; Security Compliance Center aufrufen und ein oder mehrere Elemente auswählen. Der Prüfer kann dann Folgendes tun: 
  
- Anwenden einer anderen Bezeichnung
    
- Verlängern Sie den Aufbewahrungszeitraum.
    
- Das Element endgültig löschen.
    
Ein Prüfer kann den Link verwenden, um das Dokument an seinem ursprünglichen Speicherort anzuzeigen, wenn der Prüfer über Berechtigungen für diesen Speicherort verfügt. Während einer Disposition-Überprüfungen werden die Inhalte nie vom ursprünglichen Speicherort verschoben, und Sie werden nie gelöscht, bis sich der Prüfer dazu entscheidet.
  
Beachten Sie, dass die e-Mail-Benachrichtigungen wöchentlich automatisch an die Bearbeiter gesendet werden. Wenn der Inhalt das Ende seines Aufbewahrungszeitraums erreicht hat, kann es daher bis zu sieben Tage dauern, bis die Bearbeiter die e-Mail-Benachrichtigung erhalten haben, dass Inhalte auf Ihre Disposition warten.
  
Beachten Sie, dass alle Dispositionsaktionen überwacht werden. Um dies sicherzustellen, müssen Sie die Überwachung mindestens einen Tag vor der ersten Dispositionsaktion aktivieren – Weitere Informationen finden Sie unter [Durchsuchen des Überwachungsprotokolls im Office 365 &amp; Security Compliance Center](search-the-audit-log-in-security-and-compliance.md). 
  
![DisPositions Optionen für ein Dokument](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a>Berechtigungen für die Disposition

Um Zugriff auf die disPositions Seite zu erhalten, müssen die Bearbeiter Mitglieder der Rolle " **dispositionverwaltung** " und " **View-Only** " sein. **** Es wird empfohlen, eine neue Rollengruppe mit dem Namen disPositions Prüfer zu erstellen, diese beiden Rollen dieser Rollengruppe hinzuzufügen und dann der Rollengruppe Mitglieder hinzuzufügen. 
  
Weitere Informationen finden Sie unter [Gewähren von Benutzern Zugriff auf das Office 365 &amp; Security Compliance Center](grant-access-to-the-security-and-compliance-center.md)
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>Dauer bis zum endgültigen Löschen des verworfenen Inhalts

Inhalte, die auf eine Disposition-Überprüfungen warten, werden erst gelöscht, nachdem ein Prüfer den Inhalt endgültig gelöscht hat. Wenn der Prüfer diese Option auswählt, wird der Inhalt der SharePoint-Website oder des OneDrive-Kontos für den in diesem Abschnitt beschriebenen Standard Bereinigungsprozess zugelassen: [Funktionsweise einer Aufbewahrungsrichtlinie mit Inhalten](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Dies führt dazu, dass:
  
- Inhalte in einer Dokumentbibliothek werden **innerhalb von 7 Tagen** nach der Disposition in den endgültigen Papierkorb verschoben und anschließend **93 Tage** danach endgültig gelöscht. Der Papierkorb wird nicht durch die Suche indiziert, und daher stehen die Inhalte für einen eDiscovery-Speicher nicht zur Verfügung. 
    
- Inhalte in der Bibliothek zur Aufbewahrungsdauer werden **innerhalb von 7 Tagen** nach der Disposition dauerhaft gelöscht. 
    
## <a name="view-pending-and-completed-dispositions"></a>Ausstehende und abgeschlossene Dispositionen anzeigen

Auf der Seite " **Disposition** " des &amp; Security Compliance Centers können Sie ausstehende und abgeschlossene Dispositionen anzeigen: 
  
- **** Ausstehende Dispositionen haben das Ende des Aufbewahrungszeitraums erreicht und erfordern eine Disposition-Überprüfungen. Entscheiden Sie nach der Überprüfung der einzelnen Elemente, ob Sie eine andere Bezeichnung zuweisen möchten, verlängern Sie die Aufbewahrungsdauer, oder löschen Sie sie endgültig. 
    
- **Abgeschlossene** Dispositionen wurden während einer Disposition-Überprüfung zum Löschen genehmigt und sind jetzt permanent gelöscht. Elemente, auf die eine andere Bezeichnung angewendet wurde oder deren Beibehaltungsdauer im Rahmen einer Überprüfungen verlängert wurde, werden hier nicht angezeigt. 
    
### <a name="filter-the-disposition-views"></a>Filtern der Dispositions Ansichten

Sie können diese Ansichten nach Beschriftung oder Zeitspanne filtern. Bei ausstehenden Dispositionen basiert der Zeitintervall auf dem Ablaufdatum. Bei historischen Dispositionen basiert der Zeitintervall auf dem Löschdatum.
  
![Filter Optionen auf der Seite "Disposition"](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a>Exportieren der Dispositionselemente

Darüber hinaus können Sie die Elemente in einer der beiden Ansichten als CSV-Datei exportieren, die Sie in Excel öffnen können.
  
![Exportierte Dispositionsdaten in Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

