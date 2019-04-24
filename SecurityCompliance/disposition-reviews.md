---
title: Übersicht über die Disposition Reviews
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Wenn Sie eine Aufbewahrungs Bezeichnung erstellen, die Inhalte in Microsoft 365 speichert, können Sie eine Disposition-Überprüfungen am Ende des Aufbewahrungszeitraums auslösen.
ms.openlocfilehash: 1828f4055e9048260db7d16df8ad87db36438211
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257328"
---
# <a name="overview-of-disposition-reviews"></a>Übersicht über die Disposition Reviews

Wenn der Inhalt das Ende seines Aufbewahrungszeitraums erreicht hat, gibt es mehrere Gründe, warum Sie diesen Inhalt überprüfen möchten, um zu entscheiden, ob er sicher gelöscht werden kann ("verworfen"). Beispielsweise müssen Sie Folgendes tun:
  
- UnterBrechen des Löschens ("Disposition") relevanter Inhalte im Fall eines Rechtsstreits oder einer Überwachung.
    
- Entfernen Sie Inhalte aus der Dispositionsliste, um Sie in einem Archiv zu speichern, wenn dieser Inhalt Forschungs-oder Verlaufswerte aufweist.
    
- Weisen Sie dem Inhalt einen anderen Aufbewahrungszeitraum zu, wenn die ursprüngliche Richtlinie eine temporäre oder provisorische Lösung war.
    
- Den Inhalt an Clients zurückgeben oder an eine andere Organisation übertragen.
    
Wenn Sie im Microsoft 365 Compliance Center, im Microsoft 365 Security Center oder im Office 365 Security & Compliance Center eine Aufbewahrungs Bezeichnung erstellen, können Sie eine Disposition Überprüfung am Ende des Aufbewahrungszeitraums auslösen. Bei einer Disposition:
  
- Die Personen, die Sie auswählen, erhalten eine e-Mail-Benachrichtigung, dass Sie Inhalte zur Überarbeitung haben. Diese Prüfer können einzelne Benutzer, Verteiler-oder Sicherheitsgruppen oder Office 365-Gruppen sein. Beachten Sie, dass Benachrichtigungen wöchentlich gesendet werden.
    
- Die Bearbeiter wechseln zur Seite " **Disposition** " im Security &amp; Compliance Center, um den Inhalt zu Überprüfung. Die Bearbeiter können sehen, wie viele Elemente für jede Aufbewahrungs Bezeichnung auf die Disposition warten, und dann eine Aufbewahrungs Bezeichnung auswählen, um alle Inhalte mit dieser Bezeichnung anzuzeigen.
    
- Der Prüfer kann für jedes Dokument oder jede e-Mail Folgendes tun:
    
  - Anwenden einer anderen Aufbewahrungs Bezeichnung.
    
  - Verlängern des Aufbewahrungszeitraums.
    
  - Endgültig löschen.
    
- Prüfer können ausstehende oder abgeschlossene Dispositionen anzeigen und diese Liste als CSV-Datei exportieren.

> [!NOTE]
> Für disPositions Prüfungen ist ein Office 365 Enterprise E5-Abonnement erforderlich.
  
Eine Disposition-Überprüfungen kann Inhalte in Exchange-Postfächern, SharePoint-Websites, OneDrive-Konten und Office 365-Gruppen einbeziehen. Inhalte, die auf eine Disposition-Überprüfungen an diesen Speicherorten warten, werden erst gelöscht, nachdem ein Prüfer die Inhalte endgültig gelöscht hat.
  
![Seite "Dispositions" im Security and Compliance Center](media/Retention_Dispositions_v2_page.png)

## <a name="setting-up-the-disposition-review-by-creating-a-retention-label"></a>Einrichten der Disposition-Überprüfungen durch Erstellen einer Aufbewahrungs Bezeichnung

Dies ist der grundlegende Workflow für das Einrichten einer Disposition-Überprüfungen. Beachten Sie, dass in diesem Ablauf eine Aufbewahrungs Bezeichnung veröffentlicht und dann manuell von einem Benutzer angewendet wird. Alternativ kann eine Aufbewahrungs Bezeichnung, die eine Dispositions Überprüfung auslöst, automatisch auf Inhalte angewendet werden.
  
![Diagramm mit dem Ablauf der Funktionsweise der Disposition](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
Eine Dispositions Überprüfung ist eine Option, wenn Sie eine Aufbewahrungs Bezeichnung in Office 365 erstellen. Beachten Sie, dass diese Option nicht in einer Aufbewahrungsrichtlinie verfügbar ist, sondern nur in einer Aufbewahrungs Bezeichnung, die so konfiguriert ist, dass Inhalte aufbewahrt werden.
  
Weitere Informationen zu Aufbewahrungs Bezeichnungen finden Sie unter [Übersicht über Aufbewahrungs Beschriftungen](labels.md).
  
![Aufbewahrungseinstellungen für eine Bezeichnung](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>Freigeben von Inhalten

Wenn ein Prüfer per e-Mail benachrichtigt wird, dass der Inhalt bereit ist, zu überprüfen, können Sie die Seite " **Disposition** " im &amp; Security Compliance Center aufrufen. Die Bearbeiter können sehen, wie viele Elemente für jede Aufbewahrungs Bezeichnung auf die Disposition warten, und dann eine Aufbewahrungs Bezeichnung auswählen, um alle Inhalte mit dieser Bezeichnung anzuzeigen.

Nachdem Sie eine Aufbewahrungs Bezeichnung ausgewählt haben, werden auf der nächsten Seite alle ausstehenden Dispositionen für diese Bezeichnung angezeigt.

![DisPositions Optionen](media/Retention_Disposition_options_v2.png)

Der Prüfer kann dann Folgendes tun: 
  
- Anwenden einer anderen Aufbewahrungs Bezeichnung.
    
- Verlängern Sie den Aufbewahrungszeitraum.
    
- Das Element endgültig löschen.

Beachten Sie, dass ein Prüfer mehrere Elemente auswählen und gleichzeitig freigeben kann.
    
Ein Prüfer kann den Link auch verwenden, um das Dokument an seinem ursprünglichen Speicherort anzuzeigen, wenn der Prüfer über Berechtigungen für diesen Speicherort verfügt. Während einer Disposition-Überprüfungen werden die Inhalte nie vom ursprünglichen Speicherort verschoben, und Sie werden nie gelöscht, bis sich der Prüfer dazu entscheidet.
  
Beachten Sie, dass die e-Mail-Benachrichtigungen wöchentlich automatisch an die Bearbeiter gesendet werden. Wenn der Inhalt das Ende seines Aufbewahrungszeitraums erreicht hat, kann es daher bis zu sieben Tage dauern, bis die Bearbeiter die e-Mail-Benachrichtigung erhalten haben, dass Inhalte auf Ihre Disposition warten.
  
Beachten Sie, dass alle Dispositionsaktionen überwacht werden. Um dies sicherzustellen, müssen Sie die Überwachung mindestens einen Tag vor der ersten Dispositionsaktion aktivieren – Weitere Informationen finden Sie unter [Durchsuchen des Überwachungsprotokolls im Office 365 &amp; Security Compliance Center](search-the-audit-log-in-security-and-compliance.md). 
  
## <a name="permissions-for-disposition"></a>Berechtigungen für die Disposition

Um Zugriff auf die disPositions Seite zu erhalten, müssen die Bearbeiter Mitglieder der Rolle " **dispositionverwaltung** " und " **View-Only** " sein. **** Es wird empfohlen, eine neue Rollengruppe mit dem Namen disPositions Prüfer zu erstellen, diese beiden Rollen dieser Rollengruppe hinzuzufügen und dann der Rollengruppe Mitglieder hinzuzufügen. 
  
Weitere Informationen finden Sie unter [Gewähren von Benutzern Zugriff auf das Office 365 &amp; Security Compliance Center](grant-access-to-the-security-and-compliance-center.md)
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>Dauer bis zum endgültigen Löschen des verworfenen Inhalts

Inhalte, die auf eine Disposition-Überprüfungen warten, werden erst gelöscht, nachdem ein Prüfer den Inhalt endgültig gelöscht hat. Wenn der Prüfer diese Option auswählt, wird der Inhalt der SharePoint-Website oder des OneDrive-Kontos für den in diesem Abschnitt beschriebenen Standard Bereinigungsprozess zugelassen: [Funktionsweise einer Aufbewahrungsrichtlinie mit Inhalten](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Dies führt dazu, dass:
  
- Inhalte in einer Dokumentbibliothek werden **innerhalb von 7 Tagen** nach der Disposition in den endgültigen Papierkorb verschoben und anschließend **93 Tage** danach endgültig gelöscht. Der Papierkorb wird nicht durch die Suche indiziert, und daher stehen die Inhalte für einen eDiscovery-Speicher nicht zur Verfügung.

- Inhalte in der Bibliothek zur Aufbewahrungsdauer werden **innerhalb von 7 Tagen** nach der Disposition dauerhaft gelöscht.

- Elemente in einem Exchange-Postfach werden innerhalb von **14 Tagen** nach der Disposition dauerhaft gelöscht. (Beachten Sie, dass 14 Tage die Standardeinstellung sind, Sie können jedoch bis zu 30 Tage lang konfiguriert werden.)
    
## <a name="view-pending-dispositions-and-disposed-items"></a>Anzeigen ausstehender Dispositionen und verworfener Elemente

Auf der Seite ausStehende **Disposition** können Sie ausstehende und abgeschlossene Dispositionen für eine bestimmte Aufbewahrungs Bezeichnung anzeigen: 
  
- Die **ausstehende Disposition** zeigt Elemente an, die das Ende ihrer Aufbewahrungsdauer erreicht haben und eine Disposition-Überprüfungen erfordern. Entscheiden Sie nach der Überprüfung der einzelnen Elemente, ob Sie eine andere Aufbewahrungs Bezeichnung anwenden möchten, verlängern Sie die Aufbewahrungsdauer, oder löschen Sie sie endgültig. Sie können mehrere Elemente auswählen.
    
- Auf der Registerkarte " **Disposed Items** " werden Dispositionen angezeigt, die während einer Disposition-Überprüfung zum Löschen genehmigt wurden und jetzt permanent gelöscht werden. Elemente, auf die eine andere Aufbewahrungs Bezeichnung angewendet wurde oder deren Beibehaltungsdauer im Rahmen einer Überprüfungen verlängert wurde, werden hier nicht angezeigt.

![DisPositions Registerkarten](media/Retention_Disposition_tabs.png)
    
### <a name="filter-the-disposition-views"></a>Filtern der Dispositions Ansichten

Sie können diese Ansichten nach Beibehaltungs Bezeichnung oder Zeitspanne filtern. Bei ausstehenden Dispositionen basiert der Zeitintervall auf dem Ablaufdatum. Für verworfene Elemente basiert der Zeitintervall auf dem Löschdatum.
  
![Optionen für den disPositions Filter](media/Retention_filter_options.png)

### <a name="export-the-disposition-items"></a>Exportieren der Dispositionselemente

Darüber hinaus können Sie die Elemente in einer der beiden Ansichten als CSV-Datei exportieren, die Sie in Excel öffnen können.
  
![Exportierte Dispositionsdaten in Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

