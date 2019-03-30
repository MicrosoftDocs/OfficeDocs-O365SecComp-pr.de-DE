---
title: Suchen nach eDiscovery-Aktivitäten im Office 365-Überwachungsprotokoll
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 67cc7f42-a53d-4751-b929-6005c80798f7
description: Erfahren Sie, wie Sie im Office 365-Überwachungsprotokoll nach Ereignissen suchen, die protokolliert werden, wenn Kompatibilitäts Administratoren Inhaltssuche und eDiscovery Case-Aufgaben im Security & Compliance Center ausführen.
ms.openlocfilehash: 4d16fd162cb8d00d940df90dcab3c5856e9e59ee
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000708"
---
# <a name="search-for-ediscovery-activities-in-the-office-365-audit-log"></a>Suchen nach eDiscovery-Aktivitäten im Office 365-Überwachungsprotokoll

Inhaltssuche und eDiscovery-bezogene Aktivitäten, die im Security & Compliance Center oder durch Ausführen der entsprechenden Windows PowerShell-Cmdlets ausgeführt werden, werden im Office 365-Überwachungsprotokoll protokolliert. Ereignisse werden protokolliert, wenn Administratoren oder Compliance-Administratoren (oder alle Benutzer, denen eDiscovery-Berechtigungen zugewiesen sind) die folgenden Aufgaben im Zusammenhang mit Inhaltssuche und eDiscovery im Security & Compliance Center ausführen:
  
- Erstellen und Verwalten von eDiscovery-Fällen
    
- Erstellen, starten und Bearbeiten von Inhalts suchen
    
- Ausführen von Inhalts Suchaktionen wie Vorschau, exportieren und Löschen von Suchergebnissen
    
- Konfigurieren der Filterung von Berechtigungen für die Inhaltssuche
    
- Verwalten der eDiscovery-Administrator Rolle
    
> [!IMPORTANT]
> Die in diesem Artikel beschriebenen Aktivitäten sind nur das Ergebnis von eDiscovery-Aufgaben, die mit dem Security & Compliance Center durchgeführt werden. eDiscovery-Aufgaben, die mit dem in-Place-eDiscovery-Tool in Exchange Online oder dem eDiscovery Center in SharePoint Online ausgeführt wurden, sind nicht enthalten. 
  
Weitere Informationen zum Durchsuchen des Office 365-Überwachungsprotokolls, zu den erforderlichen Berechtigungen und zum Exportieren der Suchergebnisse finden Sie unter [Durchsuchen des Überwachungsprotokolls im Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md).
  
## <a name="how-to-search-for-and-view-ediscovery-activities"></a>Suchen und Anzeigen von eDiscovery-Aktivitäten

Derzeit müssen Sie einige spezifische Schritte ausführen, um eDiscovery-Aktivitäten im Office 365-Überwachungsprotokoll anzuzeigen. Die gehen so:
  
1. Wechseln Sie zu [https://compliance.microsoft.com](https://compliance.microsoft.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich auf **Suchen**, und klicken Sie dann auf **Überwachungsprotokoll Suche**.
    
4. Klicken Sie in der Dropdownliste **Aktivitäten** unter **eDiscovery-Aktivitäten**auf eine oder mehrere Aktivitäten, nach denen gesucht werden soll. Sie können auch auf **eDiscovery-Aktivitäten** klicken, um nach allen eDiscovery-bezogenen Aktivitäten zu suchen. 
    
    > [!NOTE]
    > Die Dropdownliste Aktivitäten enthält auch eine Gruppe von Aktivitäten namens EDiscovery- **Cmdlet-Aktivitäten** , die Datensätze aus dem Cmdlet-Überwachungsprotokoll zurückgeben. 
  
5.  Wählen Sie einen Datums-und Uhrzeitbereich aus, um eDiscovery-Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten sind. 
    
6. Wählen Sie im Feld **Benutzer** einen oder mehrere Benutzer aus, für die Suchergebnisse angezeigt werden sollen. Lassen Sie dieses Feld leer, um Einträge für alle Benutzer zurückzugeben. 
    
7. Klicken Sie auf **Suchen** , um die Suche mit Ihren Suchkriterien auszuführen. 
    
8. Nachdem die Suchergebnisse angezeigt wurden, können Sie auf **Ergebnisse filtern** klicken, um die resultierenden Aktivitätsdatensätze zu filtern oder zu sortieren. Sie können die Filterung nicht verwenden, um bestimmte Aktivitäten explizit auszuschließen. 
    
9. Zum Anzeigen von Details zu einer Aktivität klicken Sie in der Liste der Suchergebnisse auf den Aktivitätsdatensatz. 
    
    Es wird eine Seite mit **Details** fliegen angezeigt, die die detaillierten Eigenschaften aus dem Ereignisdatensatz enthält. Klicken Sie auf **Weitere Informationen**, um zusätzliche Details anzuzeigen. Eine Beschreibung dieser Eigenschaften finden Sie im Abschnitt [detaillierte Eigenschaften für eDiscovery-Aktivitäten](#detailed-properties-for-ediscovery-activities) . 

  
## <a name="ediscovery-activities"></a>eDiscovery-Aktivitäten

In der folgenden Tabelle werden die Inhaltssuche und eDiscovery-bezogenen Aktivitäten beschrieben, die protokolliert werden, wenn ein Administrator oder ein Benutzer mithilfe des Security & Compliance Centers oder durch Ausführen des entsprechenden Cmdlets eine eDiscovery-bezogene Aktivität ausführt. Remote-PowerShell, die mit dem Security & Compliance Center Ihrer Organisation verbunden ist. 
  
> [!NOTE]
> Die in diesem Abschnitt beschriebenen eDiscovery-Aktivitäten enthalten ähnliche Informationen zu den im nächsten Abschnitt beschriebenen eDiscovery-Cmdlet-Aktivitäten. Es wird empfohlen, die in diesem Abschnitt beschriebenen eDiscovery-Aktivitäten zu verwenden, da Sie innerhalb von 30 Minuten in den Suchergebnissen des Überwachungsprotokolls angezeigt werden. Es dauert bis zu 24 Stunden, bis die eDiscovery-Cmdlet-Aktivitäten in den Überwachungsprotokoll-Suchergebnissen angezeigt werden. 
  
|**Anzeigename**|**Vorgang**|**Entsprechendes Cmdlet**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|Mitglied zu eDiscovery-Fall HinzugeFügt  <br/> |CaseMemberAdded  <br/> |Add-ComplianceCaseMember  <br/> |Ein Benutzer wurde als Mitglied eines eDiscovery-Falls hinzugefügt. Als Mitglied eines Falls kann ein Benutzer verschiedene fallbezogene Aufgaben ausführen, je nachdem, ob ihm die erforderlichen Berechtigungen zugewiesen wurden.  <br/> |
|Geänderte Inhaltssuche  <br/> |SearchUpdated  <br/> |Set-ComplianceSearch  <br/> |Eine vorhandene Inhaltssuche wurde geändert. Zu den Änderungen gehört das Hinzufügen oder Entfernen von Inhaltsspeicherorten oder das Bearbeiten der Suchabfrage.  <br/> |
|Geänderte eDiscovery-Administrator Mitgliedschaft  <br/> |CaseAdminUpdated  <br/> |Update-eDiscoveryCaseAdmin  <br/> |Die Liste der eDiscovery-Administratoren in Ihrer Organisation wurde geändert. Diese Aktivität wird protokolliert, wenn die Liste der eDiscovery-Administratoren durch eine Gruppe neuer Benutzer ersetzt wird. Wenn ein einzelner Benutzer hinzugefügt oder entfernt wird, wird der CaseAdminAdded-Vorgang protokolliert.  <br/> |
|Geänderter eDiscovery-Fall  <br/> |CaseUpdated  <br/> |Set-ComplianceCase  <br/> |Ein eDiscovery-Fall wurde geändert. Zu den Änderungen gehört das Schließen eines geöffneten Falls oder das erneute Öffnen eines geschlossenen Falls.  <br/> |
|Geänderte eDiscovery-Fall Mitgliedschaft  <br/> |CaseMemberUpdated  <br/> |Update-ComplianceCaseMember  <br/> |Die Mitgliedschaftsliste eines eDiscovery-Falls wurde geändert. Diese Aktivität wird protokolliert, wenn alle Mitglieder durch eine Gruppe neuer Benutzer ersetzt werden. Wenn ein einzelnes Element hinzugefügt oder entfernt wird, wird CaseMemberAdded-oder CaseMemberRemoved-Vorgang protokolliert.  <br/> |
|Filter für geänderte Suchberechtigungen  <br/> |SearchPermissionUpdated  <br/> |Set-ComplianceSecurityFilter  <br/> |Ein Filter für Suchberechtigungen wurde geändert.  <br/> |
|Geänderte Suchabfrage für eDiscovery Case Hold  <br/> |HoldUpdated  <br/> |Set-CaseHoldRule  <br/> |Eine abfragebasierte Aufbewahrung, die einem eDiscovery-Fall zugeordnet ist, wurde geändert. Zu den möglichen Änderungen gehört das Bearbeiten der Abfrage oder des Datumsbereichs für eine abfragebasierte Aufbewahrung.  <br/> |
|Inhaltssuche-Vorschau Element heruntergeladen  <br/> |PreviewItemDownloaded  <br/> |Nicht zutreffend  <br/> |Ein Benutzer hat ein Element auf seinen lokalen Computer heruntergeladen (durch Klicken auf den Link zum **herunterladen des ursprünglichen Elements** ), wenn die Vorschau der Suchergebnisse angezeigt wird.  <br/> |
|Element der Inhaltssuche (Vorschau)  <br/> |PreviewItemListed  <br/> |Nicht zutreffend  <br/> |Ein Benutzer hat auf **Vorschau der Such** Ergebnisse geklickt, um die Seite Vorschau der Suchergebnisse anzuzeigen, in der bis zu 1000 Elemente aus den Ergebnissen einer Inhaltssuche aufgelistet werden.  <br/> |
|Vorschau Element der Inhaltssuche angezeigt  <br/> |PreviewItemRendered  <br/> |Nicht zutreffend  <br/> |Ein eDiscovery-Manager hat ein Element durch Klicken bei der Vorschau der Suchergebnisse angezeigt.  <br/> |
|Erstellte Inhaltssuche  <br/> |SearchCreated  <br/> |New-ComplianceSearch  <br/> |Es wurde eine neue Inhaltssuche erstellt.  <br/> |
|Erstellter eDiscovery-Administrator  <br/> |CaseAdminAdded  <br/> |Add-eDiscoveryCaseAdmin  <br/> |Ein Benutzer wurde als eDiscovery-Administrator in der Organisation hinzugefügt.  <br/> |
|Erstellter eDiscovery-Fall  <br/> |CaseAdded  <br/> |New-ComplianceCase  <br/> |Ein eDiscovery-Fall wurde erstellt. Wenn ein Fall erstellt wird, müssen Sie ihm nur einen Namen geben. Weitere fallbezogene Aufgaben wie das Hinzufügen von Elementen, das Erstellen von Haltebereichen und das Erstellen von Inhalts suchen, die mit dem Fall verbunden sind, führen dazu, dass zusätzliche Ereignisse protokolliert werden.  <br/> |
|Filter für erstellte Suchberechtigungen  <br/> |SearchPermissionCreated  <br/> |New-ComplianceSecurityFilter  <br/> |Ein Filter für Suchberechtigungen wurde erstellt.  <br/> |
|Erstellte Suchabfrage für eDiscovery Case Hold  <br/> |HoldCreated  <br/> |New-CaseHoldRule  <br/> |Es wurde eine abfragebasierte Aufbewahrungszeit erstellt, die einem eDiscovery-Fall zugeordnet ist.  <br/> |
|Gelöschte Inhaltssuche  <br/> |SearchRemoved  <br/> |Remove-ComplianceSearch  <br/> |Eine vorhandene Inhaltssuche wurde gelöscht.  <br/> |
|Gelöschter eDiscovery-Administrator  <br/> |CaseAdminRemoved  <br/> |Remove-eDiscoveryCaseAdmin  <br/> |Ein eDiscovery-Administrator wurde aus Ihrer Organisation gelöscht.  <br/> |
|Gelöschter eDiscovery-Fall  <br/> |CaseRemoved  <br/> |Remove-ComplianceCase  <br/> |Ein eDiscovery-Fall wurde gelöscht. Beachten Sie, dass jeder mit der Anfrage verknüpfte Aufbewahrungsbereich entfernt werden muss, bevor der Fall gelöscht werden kann.  <br/> |
|Filter für gelöschte Suchberechtigungen  <br/> |SearchPermissionRemoved  <br/> |Remove-ComplianceSecurityFilter  <br/> |Ein Filter für Suchberechtigungen wurde gelöscht.  <br/> |
|Gelöschte Suchabfrage für eDiscovery Case Hold  <br/> |HoldRemoved  <br/> |Remove-CaseHoldRule  <br/> |Ein abfragebasierter Speicher, der einem eDiscovery-Fall zugeordnet ist, wurde gelöscht. Das Entfernen der Abfrage aus dem Haltebereich ist häufig das Ergebnis des Löschens eines haltebereichs. Wenn ein Hold-oder eine Hold-Abfrage gelöscht wird, werden die in der Warteschleife befindlichen inhaltsspeicherorte freigegeben.  <br/> |
|HeruntergeLadener Export der Inhaltssuche  <br/> |SearchExportDownloaded  <br/> |Nicht zutreffend  <br/> |Ein Benutzer hat die Ergebnisse einer Inhaltssuche auf den lokalen Computer heruntergeladen. Beachten Sie, dass ein **gestarteter Export der Inhaltssuche** initiiert werden muss, bevor Suchergebnisse heruntergeladen werden können.  <br/> |
|Vorschau der Ergebnisse der Inhaltssuche  <br/> |SearchPreviewed  <br/> |Nicht zutreffend  <br/> |Ein Benutzer hat eine Vorschau der Ergebnisse einer Inhaltssuche angezeigt.  <br/> |
|Bereinigte Ergebnisse der Inhaltssuche  <br/> |SearchResultsPurged  <br/> |New-ComplianceSearchAction  <br/> |Ein Benutzer hat die Ergebnisse einer Inhaltssuche gelöscht, indem er den Befehl **New-ComplianceSearchAction-Purge** ausführt.  <br/> |
|Analyse der Inhaltssuche entfernt  <br/> |RemovedSearchResultsSentToZoom  <br/> |Remove-ComplianceSearchAction  <br/> |Eine Inhaltssuche Prepare-Aktion (zur Vorbereitung der Suchergebnisse für Office 365 Advanced eDiscovery) wurde gelöscht. Wenn die Vorbereitungs Aktion weniger als zwei Wochen alt war, wurden die Suchergebnisse, die für Advanced eDiscovery vorbereitet wurden, aus dem Microsoft Azure-Speicherbereich gelöscht. Wenn die Vorbereitungs Aktion älter als 2 Wochen war, gibt dieses Ereignis an, dass nur die entsprechende Vorbereitungs Aktion gelöscht wurde.  <br/> |
|Export der Inhaltssuche entfernt  <br/> |RemovedSearchExported  <br/> |Remove-ComplianceSearchAction  <br/> |Eine Exportaktion für Inhaltssuche wurde gelöscht. Wenn die Exportaktion weniger als zwei Wochen alt war, wurden die Suchergebnisse, die in den Microsoft Azure-Speicherbereich hochgeladen wurden, gelöscht. Wenn die Exportaktion älter als 2 Wochen war, gibt dieses Ereignis an, dass nur die entsprechende Exportaktion gelöscht wurde.  <br/> |
|Entferntes Element aus eDiscovery-Fall  <br/> |CaseMemberRemoved  <br/> |Remove-ComplianceCaseMember  <br/> |Ein Benutzer wurde als Mitglied eines eDiscovery-Falls entfernt.  <br/> |
|Vorschau Ergebnisse der Inhaltssuche entfernt  <br/> |RemovedSearchPreviewed  <br/> |Remove-ComplianceSearchAction  <br/> |Eine Vorschau Aktion der Inhaltssuche wurde gelöscht.  <br/> |
|Entfernen der Aufräumaktion für die Inhaltssuche  <br/> |RemovedSearchResultsPurged  <br/> |Remove-ComplianceSearchAction  <br/> |Eine Inhaltssuche-Löschaktion wurde gelöscht.  <br/> |
|Suchbericht entfernt  <br/> |SearchReportRemoved  <br/> |Remove-ComplianceSearchAction  <br/> |Die Aktion Exportbericht für Inhaltssuche wurde gelöscht.  <br/> |
|Analyse der Inhaltssuche gestartet  <br/> |SearchResultsSentToZoom  <br/> |New-ComplianceSearchAction  <br/> |Die Ergebnisse einer Inhaltssuche wurden für die Analyse in Advanced eDiscovery vorbereitet.  <br/> |
|Inhaltssuche gestartet  <br/> |SearchStarted  <br/> |Start-ComplianceSearch  <br/> |Eine Inhaltssuche wurde gestartet. Wenn Sie eine Inhaltssuche mithilfe der Benutzeroberfläche Security & Compliance Center erstellen oder ändern, wird die Suche automatisch gestartet. Wenn Sie eine Suche mithilfe des Cmdlets **New-ComplianceSearch** oder **Set-ComplianceSearch** erstellen oder ändern, müssen Sie das Cmdlet **Start-ComplianceSearch** ausführen, um die Suche zu starten.  <br/> |
|Export der Inhaltssuche gestartet  <br/> |SearchExported  <br/> |New-ComplianceSearchAction  <br/> |Ein Benutzer hat die Ergebnisse einer Inhaltssuche exportiert.  <br/> |
|Exportbericht gestartet  <br/> |SearchReport  <br/> |New-ComplianceSearchAction  <br/> |Ein Benutzer hat einen Inhalts Suchbericht exportiert.  <br/> |
|Angehaltene Inhaltssuche  <br/> |SearchStopped  <br/> |Stop-ComplianceSearch  <br/> |Ein Benutzer hat eine Inhaltssuche angehalten.  <br/> |
  
## <a name="ediscovery-cmdlet-activities"></a>eDiscovery-Cmdlet-Aktivitäten

In der folgenden Tabelle sind die Cmdlet-Überwachungsprotokolldatensätze aufgeführt, die protokolliert werden, wenn ein Administrator oder ein Benutzer eine eDiscovery-bezogene Aktivität mithilfe des Security & Compliance Centers oder durch Ausführen des entsprechenden Cmdlets in der verbundenen Remote-PowerShell ausführt. im Security & Compliance Center Ihrer Organisation. Beachten Sie, dass die detaillierten Informationen im Überwachungsprotokoll für die in dieser Tabelle aufgeführten Cmdlet-Aktivitäten und die im vorherigen Abschnitt beschriebenen eDiscovery-Aktivitäten unterschiedlich sind. 
  
Wie bereits erwähnt, dauert es bis zu 24 Stunden, bis die eDiscovery-Cmdlet-Aktivitäten in den Suchergebnissen des Überwachungsprotokolls angezeigt werden.
  
> [!TIP]
> Die Cmdlets in der Spalte **Vorgang** in der folgenden Tabelle sind mit dem entsprechenden Cmdlet-Hilfethema auf TechNet verknüpft. Eine Beschreibung der verfügbaren Parameter für die einzelnen Cmdlets finden Sie im Hilfethema zum Cmdlet. Der Parameter und der Parameterwert, die mit einem Cmdlet verwendet wurden, sind im Überwachungsprotokolleintrag für jede zu protokollierende eDiscovery-Cmdlet-Aktivität enthalten. 
  
|**Anzeigename**|**Operation (Cmdlet)**|**Beschreibung**|
|:-----|:-----|:-----|
|Erstellter Speicher im eDiscovery-Fall  <br/> |[New-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823813) <br/> |Für einen eDiscovery-Fall wurde ein Speicher erstellt. Ein Haltebereich kann mit oder ohne Angabe einer Inhaltsquelle erstellt werden. Wenn Inhaltsquellen angegeben werden, werden Sie im Überwachungsprotokolleintrag identifiziert.  <br/> |
|Aufbewahrungszeit aus eDiscovery-Fall gelöscht  <br/> |[Remove-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823814) <br/> |Ein mit einem eDiscovery-Fall verknüpfter Speicher wurde gelöscht. Durch das Löschen eines Haltestatus werden alle inhaltsspeicherorte aus dem Haltebereich freigegeben. Durch das Löschen des haltebereichs werden auch die mit dem Haltebereich verknüpften Case Hold-Regeln gelöscht (siehe **Remove-CaseHoldRule** unten).  <br/> |
|Haltestatus in eDiscovery-Fall geändert  <br/> |[Set-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823815) <br/> |Ein mit einer eDiscovery verknüpfter Haltebereich wurde geändert. Zu den möglichen Änderungen gehört das Hinzufügen oder Entfernen von Inhaltsspeicherorten oder das Deaktivieren des haltebereichs.  <br/> |
|Erstellte Suchabfrage für eDiscovery Case Hold  <br/> |[New-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823816) <br/> |Es wurde eine abfragebasierte Aufbewahrungszeit erstellt, die einem eDiscovery-Fall zugeordnet ist.  <br/> |
|Gelöschte Suchabfrage für eDiscovery Case Hold  <br/> |[Remove-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823820) <br/> |Ein abfragebasierter Speicher, der einem eDiscovery-Fall zugeordnet ist, wurde gelöscht. Das Entfernen der Abfrage aus dem Haltebereich ist häufig das Ergebnis des Löschens eines haltebereichs. Wenn ein Hold-oder eine Hold-Abfrage gelöscht wird, werden die in der Warteschleife befindlichen inhaltsspeicherorte freigegeben.  <br/> |
|Geänderte Suchabfrage für eDiscovery Case Hold  <br/> |[Set-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823819) <br/> |Eine abfragebasierte Aufbewahrung, die einem eDiscovery-Fall zugeordnet ist, wurde geändert. Zu den möglichen Änderungen gehört das Bearbeiten der Abfrage oder des Datumsbereichs für eine abfragebasierte Aufbewahrung.  <br/> |
|Erstellter eDiscovery-Fall  <br/> |[New-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823842) <br/> |Ein eDiscovery-Fall wurde erstellt. Wenn ein Fall erstellt wird, müssen Sie ihm nur einen Namen geben. Weitere fallbezogene Aufgaben wie das Hinzufügen von Elementen, das Erstellen von Haltebereichen und das Erstellen von Inhalts suchen, die mit dem Fall verbunden sind, führen dazu, dass zusätzliche Ereignisse protokolliert werden.  <br/> |
|Gelöschter eDiscovery-Fall  <br/> |[Remove-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823844) <br/> |Ein eDiscovery-Fall wurde gelöscht. Beachten Sie, dass jeder mit der Anfrage verknüpfte Aufbewahrungsbereich entfernt werden muss, bevor der Fall gelöscht werden kann.  <br/> |
|Geänderter eDiscovery-Fall  <br/> |[Set-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823846) <br/> |Ein eDiscovery-Fall wurde geändert. Zu den Änderungen gehört das Schließen eines geöffneten Falls oder das erneute Öffnen eines geschlossenen Falls.  <br/> |
|Mitglied zu eDiscovery-Fall HinzugeFügt  <br/> |[Add-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823848) <br/> |Ein Benutzer wurde als Mitglied eines eDiscovery-Falls hinzugefügt. Als Mitglied eines Falls kann ein Benutzer verschiedene fallbezogene Aufgaben ausführen, je nachdem, ob ihm die erforderlichen Berechtigungen zugewiesen wurden.  <br/> |
|Entferntes Element aus eDiscovery-Fall  <br/> |[Remove-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823849) <br/> |Ein Benutzer wurde als Mitglied eines eDiscovery-Falls entfernt.  <br/> |
|Geänderte eDiscovery-Fall Mitgliedschaft  <br/> |[Update-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823850) <br/> |Die Mitgliedschaftsliste eines eDiscovery-Falls wurde geändert. Diese Aktivität wird protokolliert, wenn alle Mitglieder durch eine Gruppe neuer Benutzer ersetzt werden. Wenn ein einzelnes Element hinzugefügt oder entfernt wird, wird der Vorgang **Add-ComplianceCaseMember** oder **Remove-ComplianceCaseMember** protokolliert.  <br/> |
|Erstellte Inhaltssuche  <br/> |[New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935) <br/> |Es wurde eine neue Inhaltssuche erstellt.  <br/> |
|Gelöschte Inhaltssuche  <br/> |[Remove-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517936) <br/> |Eine vorhandene Inhaltssuche wurde gelöscht.  <br/> |
|Geänderte Inhaltssuche  <br/> |[Set-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517937) <br/> |Eine vorhandene Inhaltssuche wurde geändert. Zu den Änderungen zählen das Hinzufügen oder Entfernen von Inhaltsspeicherorten, die durchsucht werden, und das Bearbeiten der Suchabfrage.  <br/> |
|Inhaltssuche gestartet  <br/> |[Start-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517938) <br/> |Eine Inhaltssuche wurde gestartet. Wenn Sie eine Inhaltssuche mithilfe der Benutzeroberfläche Security & Compliance Center erstellen oder ändern, wird die Suche automatisch gestartet. Wenn Sie eine Suche mithilfe des Cmdlets **New-ComplianceSearch** oder **Set-ComplianceSearch** erstellen oder ändern, müssen Sie das Cmdlet **Start-ComplianceSearch** ausführen, um die Suche zu starten.  <br/> |
|Angehaltene Inhaltssuche  <br/> |[Stop-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517939) <br/> |Eine Inhaltssuche wurde beendet.  <br/> |
|Erstellte Inhalts Suchaktion  <br/> |[New-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=527971) <br/> |Eine Inhalts Suchaktion wurde erstellt. Zu den Aktionen für die Inhaltssuche gehört das Anzeigen einer Vorschau der Suchergebnisse, das Exportieren der Suchergebnisse, das Vorbereiten der Suchergebnisse für die Analyse in Office 365 Advanced eDiscovery und das dauerhafte Löschen von Elementen, die den Suchkriterien einer Inhaltssuche entsprechen.  <br/> |
|Gelöschte Inhaltssuche (Aktion)  <br/> |[Remove-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=824027) <br/> |Eine Inhalts Suchaktion wurde gelöscht.  <br/> |
|Filter für erstellte Suchberechtigungen  <br/> |[New-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617542) <br/> |Ein Filter für Suchberechtigungen wurde erstellt.  <br/> |
|Filter für gelöschte Suchberechtigungen  <br/> |[Remove-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617543) <br/> |Ein Filter für Suchberechtigungen wurde gelöscht.  <br/> |
|Filter für geänderte Suchberechtigungen  <br/> |[Set-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617544) <br/> |Ein Filter für Suchberechtigungen wurde geändert.  <br/> |
|Erstellter eDiscovery-Administrator  <br/> |[Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=798217) <br/> |Ein Benutzer wurde als eDiscovery-Administrator in Ihrer Organisation hinzugefügt.  <br/> |
|Gelöschter eDiscovery-Administrator  <br/> |[Remove-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823945) <br/> |Ein eDiscovery-Administrator wurde aus Ihrer Organisation gelöscht.  <br/> |
|Geänderte eDiscovery-Administrator Mitgliedschaft  <br/> |[Update-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823946) <br/> |Die Liste der eDiscovery-Administratoren in Ihrer Organisation wurde geändert. Diese Aktivität wird protokolliert, wenn die Liste der eDiscovery-Administratoren durch eine Gruppe neuer Benutzer ersetzt wird. Wenn ein einzelner Benutzer hinzugefügt oder entfernt wird, wird der Vorgang **Add-eDiscoveryCaseAdmin** oder **Remove-eDiscoveryCaseAdmin** protokolliert.  <br/> |
   
## <a name="detailed-properties-for-ediscovery-activities"></a>Detaillierte Eigenschaften für eDiscovery-Aktivitäten

In der folgenden Tabelle werden die Eigenschaften beschrieben, die enthalten sind, wenn Sie auf der Seite **Details** auf **Weitere Informationen** für eine eDiscovery-Aktivität klicken, die in den Suchergebnissen aufgeführt ist. Diese Eigenschaften sind auch in der CSV-Datei enthalten, wenn Sie die Suchergebnisse des Überwachungsprotokolls exportieren. Beachten Sie, dass ein Überwachungsprotokolleintrag für eine eDiscovery-Aktivität nicht alle unten aufgeführten detaillierten Eigenschaften enthalten kann. 
  
> [!TIP]
> Wenn Sie die Suchergebnisse exportieren, enthält die CSV-Datei eine Spalte mit dem Namen **Detail**, die die in der folgenden Tabelle beschriebenen detaillierten Eigenschaften in einer mehrwertigen Eigenschaft enthält. Sie können die Power Query-Funktion in Excel verwenden, um diese Spalte in mehrere Spalten aufzuteilen, sodass jede Eigenschaft eine eigene Spalte hat. Auf diese Weise können Sie eine oder mehrere dieser Eigenschaften sortieren und filtern. Weitere Informationen finden Sie im Abschnitt "Exportieren der Suchergebnisse in eine Datei" unter [Durchsuchen des Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file). 
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|Fall  <br/> |Die Identität (GUID) des eDiscovery-Falls, die erstellt, geändert oder gelöscht wurde.  <br/> |
|ClientApplication  <br/> |eDiscovery-Cmdlet-Aktivitäten weisen für diese Eigenschaft den Wert **EMC** auf. Dies weist darauf hin, dass die Aktivität mithilfe der GUI Security & Compliance Center oder Ausführen des Cmdlets in PowerShell ausgeführt wurde.  <br/> |
|ClientIP  <br/> |Die IP-Adresse des Geräts, das verwendet wurde, als die Aktivität protokolliert wurde. Die IP-Adresse wird im Adressformat IPv4 oder IPv6 angezeigt.  <br/> |
|ClientRequestId  <br/> | Für eDiscovery-Aktivitäten ist diese Eigenschaft normalerweise leer.  <br/> |
|CmdletVersion  <br/> |Die Buildnummer für die Version des Security & Compliance Center, die in Ihrer Organisation läuft.  <br/> |
|CreationTime  <br/> |Datum und Uhrzeit in koordinierter weltZeit (UTC), als die eDiscovery-Aktivität abgeschlossen wurde.  <br/> |
|EffectiveOrganization  <br/> |Der Name der Office 365-Organisation.  <br/> |
|ExchangeLocations  <br/> |Die Exchange Online-Postfächer, die in einer Inhaltssuche enthalten sind oder in einem eDiscovery-Fall aufbewahrt werden.  <br/> |
|Ausschlüsse  <br/> |Postfach-oder Websitespeicher Orte, die von einer Inhaltssuche oder einem Haltebereich in einem eDiscovery-Fall ausgeschlossen werden.  <br/> |
|ExtendedProperties  <br/> |Zusätzliche Eigenschaften aus einer Inhaltssuche, einer Inhalts Suchaktion oder in einem eDiscovery-Fall, beispielsweise die Objekt-GUID und die entsprechenden Cmdlet-und Cmdlet-Parameter, die beim Ausführen der Aktivität verwendet wurden.  <br/> |
|Id  <br/> |Die ID des Berichts Eintrags. Die ID identifiziert den Überwachungsprotokolleintrag eindeutig.  <br/> |
|NonPIIParameters  <br/> |Eine Liste der Parameter (ohne Werte), die mit dem in der Operation-Eigenschaft angegebenen Cmdlet verwendet wurden. Die in dieser Eigenschaft aufgeführten Parameter sind identisch mit den in der Parameters-Eigenschaft aufgeführten Parametern.  <br/> |
|ObjectId  <br/> |Die GUID oder der Name des Objekts (beispielsweise eine Inhaltssuche oder ein eDiscovery-Fall), die von der in der Operation-Eigenschaft aufgeführten Aktivität erstellt, geändert oder gelöscht wurden. Dieses Objekt wird auch in der Spalte Element in den Suchergebnissen des Überwachungsprotokolls identifiziert.  <br/> |
|ObjectType  <br/> |Der Typ des eDiscovery-Objekts, das der Benutzer erstellt, gelöscht oder geändert hat; beispielsweise eine Inhalts Suchaktion (Vorschau, Export oder Bereinigung), einen eDiscovery-Fall oder eine Inhaltssuche.  <br/> |
|Vorgang  <br/> |Der Name des Vorgangs, der der ausgeführten eDiscovery-Aktivität entspricht.  <br/> |
|OrganizationId  <br/> |Die GUID für Ihre Office 365-Organisation.  <br/> |
|Parameter  <br/> |Der Name und der Wert für die Parameter, die mit dem entsprechenden Cmdlet verwendet wurden.  <br/> |
|PublicFolderLocations  <br/> |Die Speicherorte für Öffentliche Ordner in Exchange Online, die in einer Inhaltssuche enthalten sind oder in einem eDiscovery-Fall gespeichert werden.  <br/> |
|Abfrage  <br/> |Die der Aktivität zugeordnete Suchabfrage, beispielsweise eine Inhaltssuche oder eine abfragebasierte Aufbewahrung.  <br/> |
|RecordType  <br/> |Der vom Datensatz angegebene Vorgangstyp. Der Wert **18** gibt ein Ereignis im Zusammenhang mit einer Aktivität an, die im Abschnitt [Aktivitäten des eDiscovery](#ediscovery-cmdlet-activities) -Cmdlets aufgeführt ist. Der Wert **24** gibt ein Ereignis im Zusammenhang mit einer im Abschnitt Vorgehens [Weise suchen und Anzeigen von eDiscovery-Aktivitäten](#how-to-search-for-and-view-ediscovery-activities) aufgeführten Aktivität an.  <br/> |
|ResultStatus  <br/> |Gibt an, ob die Aktion (in der Eigenschaft "Operation" angegeben) erfolgreich war oder nicht.  <br/> |
|SecurityComplianceCenterEventType  <br/> |Gibt an, dass die Aktivität ein Security & Compliance Center-Ereignis war. Alle eDiscovery-Aktivitäten haben den Wert **0** für diese Eigenschaft.  <br/> |
|SharepointLocations  <br/> |Die SharePoint Online-Websites, die in einer Inhaltssuche enthalten sind oder in einem eDiscovery-Fall aufbewahrt werden.  <br/> |
|StartTime  <br/> |Das Datum und die Uhrzeit in koordinierter weltZeit (UTC), als die eDiscovery-Aktivität gestartet wurde.  <br/> |
|UserId  <br/> |Der Benutzer, der die Aktivität (angegeben in der Eigenschaft "Operation") ausgeführt hat, die dazu geführt hat, dass der Datensatz protokolliert wird. Beachten Sie, dass Datensätze für eDiscovery-Aktivitäten, die von Systemkonten ausgeführt werden (beispielsweise NT AUTHORITY\SYSTEM), ebenfalls im Überwachungsprotokoll enthalten sind.  <br/> |
|UserKey  <br/> |Eine alternative ID für den in der UserId-Eigenschaft identifizierten Benutzer. Bei eDiscovery-Aktivitäten ist der Wert für diese Eigenschaft in der Regel dieselbe wie die UserId-Eigenschaft.  <br/> |
|UserServicePlan  <br/> |Das Office 365-Abonnement, das von Ihrer Organisation verwendet wird. Für eDiscovery-Aktivitäten ist diese Eigenschaft normalerweise leer.  <br/> |
|UserType  <br/> |Der Typ des Benutzers, der den Vorgang ausgeführt hat. Die folgenden Werte geben den Benutzertyp an.  <br/> 0 ein regulärer Benutzer. 2 ein Administrator in Ihrer Office 365-Organisation. 3 ein Microsoft-Datencenter-Administrator-oder Datacenter-Systemkonto. 4 ein Systemkonto. 5 eine Anwendung. 6 ein Dienstprinzipal. |
|Version  <br/> |Gibt die Versionsnummer der Aktivität an (identifiziert durch die Eigenschaft "Operation"), die protokolliert wird.  <br/> |
|Arbeitslast  <br/> |Der Office 365-Dienst, in dem die Aktivität aufgetreten ist. Für eDiscovery-Aktivitäten lautet der Wert **SecurityComplianceCenter**.  <br/> |
