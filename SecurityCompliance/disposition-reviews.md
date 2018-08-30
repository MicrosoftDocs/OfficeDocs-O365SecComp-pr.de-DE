---
title: Übersicht über die Disposition Reviews (engl.)
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d0c6095b-bfee-4906-a2c7-89c2d7f411c1
description: Wenn Sie eine Beschriftung, die Inhalte in Office 365 behält erstellen, können Sie auswählen, Disposition Wiederholung am Ende des Aufbewahrungszeitraums ausgelöst.
ms.openlocfilehash: c0a2933f597c9b314ac4ce2e72de9619fac90082
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013719"
---
# <a name="overview-of-disposition-reviews"></a>Übersicht über die Disposition Reviews (engl.)

Wenn Inhalte am Ende der Aufbewahrungsdauer erreicht, sind verschiedene Gründe, warum Sie möglicherweise überprüfen möchten, dass Inhalte entscheiden, ob sicher gelöscht werden kann ("freigegeben"). Sie können beispielsweise Folgendes ausführen:
  
- Das Löschen ("Disposition") relevante Inhalte im Fall von Rechtsstreitigkeiten oder eine Prüfung anhalten.
    
- Entfernen Sie Inhalt aus der Liste der Disposition von Dokumenten in einem Archiv gespeichert, wenn dieser Inhalte Research oder zurückliegenden Wert hat.
    
- Weisen Sie eine andere Aufbewahrungsdauer den Inhalt, wenn die ursprüngliche Richtlinie einer Lösung temporären oder vorläufigen wurde.
    
- Den Inhalt an Clients zurückgeben oder auf einer anderen Organisation übertragen.
    
Wenn Sie eine Beschriftung, die Inhalte in Office 365 behält erstellen, können Sie auswählen, Disposition Wiederholung am Ende des Aufbewahrungszeitraums ausgelöst. Bei einer Überprüfung Disposition:
  
- Personen, die Sie auswählen, erhalten eine e-Mail-Benachrichtigung, dass sie Inhalte überprüfen aufweisen. Diese Bearbeiter können einzelnen Benutzern, Verteilergruppen oder Sicherheitsgruppen oder Office 365 Gruppen sein. Beachten Sie, dass wöchentlich Benachrichtigungen gesendet werden.
    
- Die Bearbeiter wechseln Sie zur Seite **Disposition von Dokumenten** in das Wertpapier &amp; Compliance Center, um den Inhalt zu überprüfen. 
    
- Für jedes Dokument kann der Prüfer:
    
  - Eine andere Bezeichnung anwenden.
    
  - Erweitern Sie die Aufbewahrungsdauer.
    
  - Dauerhaft löschen.
    
- Prüfer können entweder ausstehende oder zurückliegenden Abschneidedispositionen anzeigen und diese Liste als CSV-Datei zu exportieren.
    
Beachten Sie, Disposition Bewertungen ein Office 365 Enterprise E5 Abonnement benötigen.
  
Disposition Wiederholung kann in Exchange-Postfächern, SharePoint-Websites, OneDrive-Konten und Gruppen für Office 365 enthalten. Eine Disposition Prüfung an diesen Speicherorten Inhalt wird gelöscht, erst nach ein Bearbeiter möchte die Inhalte dauerhaft gelöscht.
  
![Disposition-Seite](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a>Einrichten der Disposition überprüfen, indem Sie eine Beschriftung erstellen

Dies ist der grundlegende Workflow für das Einrichten einer Disposition überprüfen. Beachten Sie, dass diesem Datenstrom eine Beschriftung zeigt, veröffentlicht, und klicken Sie dann manuell von einem Benutzer zugewiesen. auch kann eine Beschriftung, die eine Überprüfung Disposition ausgelöst wird automatisch auf Inhalte angewendet wird.
  
![Diagramm mit der Funktionsweise der Disposition Ablauf](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
Disposition Wiederholung ist eine Option aus, wenn Sie eine Beschriftung in Office 365 erstellen. Beachten Sie, dass diese Option nicht in einer Aufbewahrungsrichtlinie jedoch nur in einem Bezeichnungsfeld mit Einstellungen für die Aufbewahrung verfügbar ist.
  
Weitere Informationen zu Etiketten finden Sie unter [Übersicht über die Beschriftungen](labels.md).
  
![Einstellungen für eine Beschriftung für die Aufbewahrung](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>Verwerfen von Inhalten

Wenn ein Bearbeiter per e-Mail benachrichtigt wird, dass Inhalte bereit, um zu prüfen, können sie wechseln Sie zur Seite **Disposition von Dokumenten** in das Wertpapier &amp; Compliance Center, und wählen Sie einen oder mehrere Elemente. Der Prüfer können Sie: 
  
- Eine andere Bezeichnung anwenden.
    
- Erweitern Sie die Aufbewahrungsdauer.
    
- Löschen Sie das Element endgültig.
    
Ein Prüfer können den Link Sie das Dokument am ursprünglichen Speicherort, anzeigen, wenn der Prüfer Berechtigungen für diesen Speicherort verfügt. Während der Überprüfung Disposition der Inhalt wird nie vom ursprünglichen Speicherort verschoben, und es wird nie gelöscht, bis der Prüfer dazu auswählt.
  
Beachten Sie, dass an Prüfer wöchentlich automatisch die e-Mail-Benachrichtigungen gesendet werden. Aus diesem Grund wenn Inhalte am Ende der Aufbewahrungsdauer erreicht, dauern bis zu sieben Tage für Bearbeiter an die e-Mail-Benachrichtigung, dass Inhalte Disposition wartet.
  
Beachten Sie außerdem, dass alle Dispositionsaktionen überwacht werden. Zu diesem Zweck müssen Sie mindestens einen Tag vor der ersten Dispositionsaktion - Weitere Informationen zu Überwachung einzuschalten, finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md). 
  
![Disposition Optionen für ein Dokument](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a>Berechtigungen für die disposition

Wenn Sie Zugriff auf die Seite **Disposition** erhalten möchten, müssen Bearbeiter Mitglieder von der **Disposition** Verwaltungsrolle und der Rolle für **Überwachungsprotokolle Kontaktobjekts** sein. Erstellen einer neuen Rollengruppe Disposition Bearbeiter aufgerufen, dieser Rollengruppe dieser beiden Rollen hinzugefügt und dann Hinzufügen von Mitgliedern der Rollengruppe empfohlen. 
  
Weitere Informationen finden Sie unter [Gewähren des Zugriffs auf die Office 365-Sicherheit &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md)
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>Wie lange dauert die verworfene Inhalte dauerhaft gelöscht wird

Inhalte, die eine Disposition Prüfung wird gelöscht, erst nach ein Bearbeiter möchte die Inhalte dauerhaft gelöscht. Wenn der Prüfer diese Option wählt, wird der Inhalt in der SharePoint-Website oder das OneDrive-Konto für den standard-Cleanup-Prozess in diesem Abschnitt beschriebenen Kandidaten: [Funktionsweise eine Aufbewahrungsrichtlinie mit Inhalten](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Dies bedeutet, dass:
  
- Inhalte in einer Dokumentbibliothek werden in der ersten Stufe Papierkorb **in 7 Tage** der Disposition verschoben, und klicken Sie dann endgültig gelöscht **93 Tage** nach Ausführung dieses. Der Papierkorb ist nicht von der Suche indiziert und seinen Inhalt sind daher nicht zu einem Haltestatus eDiscovery verfügbar. 
    
- Inhalt in der Beibehaltung halten Bibliothek dauerhaft sein wird gelöscht **in 7 Tage** der Disposition. 
    
## <a name="view-pending-and-completed-dispositions"></a>Ansicht ausstehenden und abgeschlossenen Abschneidedispositionen

Auf der Seite **Disposition** der Sicherheit &amp; Compliance Center, Sie können ausstehende und abgeschlossene Abschneidedispositionen anzeigen: 
  
- **Ausstehende** Abschneidedispositionen am Ende der Aufbewahrungszeitraum erreicht haben und Disposition Wiederholung erfordern. Überprüfen Sie jedes Element, entscheiden Sie, ob Sie eine andere Bezeichnung zuweisen, zur Erweiterung der Aufbewahrungszeitraum oder dauerhaft löschen möchten. 
    
- **Completed** Abschneidedispositionen zum Löschen während der Überprüfung Disposition genehmigt wurden und sind nun gerade dauerhaft gelöscht. Elemente, die wurde für eine andere Bezeichnung angewendet oder der Aufbewahrungszeitraum erweitert als Teil einer Überprüfung hier nicht angezeigt wird. 
    
### <a name="filter-the-disposition-views"></a>Filtern der Disposition Ansichten

Sie können diese Ansichten nach Bezeichnung oder den Zeitraum filtern. Für ausstehende Abschneidedispositionen, der Zeitbereich des Ablaufdatums basiert auf. Für zurückliegenden Abschneidedispositionen der Zeitbereich das Löschdatum basiert.
  
![Filteroptionen auf Disposition-Seite](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a>Exportieren der Disposition Elemente

Darüber hinaus können Sie die Elemente in einer Ansicht als CSV-Datei exportieren, die Sie in Excel öffnen können.
  
![Disposition exportierten Daten in Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

