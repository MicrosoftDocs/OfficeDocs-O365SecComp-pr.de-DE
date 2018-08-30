---
title: Suchen Sie nach eDiscovery-Aktivitäten im Überwachungsprotokoll Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 67cc7f42-a53d-4751-b929-6005c80798f7
description: Erfahren Sie, wie das Überwachungsprotokoll Office 365 für Ereignisse zu suchen, die protokolliert werden, wenn Administratoren Compliance Inhaltssuche und eDiscovery Groß-/Kleinschreibung in das Wertpapier Aufgaben &amp; Compliance Center.
ms.openlocfilehash: 24bd629f5576fe042e59d5cbbdecf01b3fd59cf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529555"
---
# <a name="search-for-ediscovery-activities-in-the-office-365-audit-log"></a>Suchen Sie nach eDiscovery-Aktivitäten im Überwachungsprotokoll Office 365

Content-Suche und eDiscovery-bezogene Aktivitäten, die in Office 365-Sicherheit ausgeführt werden &amp; Compliance Center oder durch Ausführen der entsprechenden Windows PowerShell-Cmdlets im Überwachungsprotokoll Office 365 angemeldet sind. Ereignisse protokolliert, wenn Administratoren oder Compliance-Administratoren (oder jedes Benutzers, der eDiscovery-zugewiesenen Berechtigungen wird) den folgenden Inhaltssuche und Aufgaben im Zusammenhang mit eDiscovery in die Office 365-Sicherheit ausführen &amp; Compliance Center:
  
- Erstellen und Verwalten von eDiscovery-Fällen
    
- Erstellen, starten und Bearbeiten von Content-Suche
    
- Ausführen Inhaltssuche Aktionen, beispielsweise das Anzeigen einer Vorschau, führt zu ausführenden und Löschen von Suche
    
- Konfigurieren von Berechtigungen für die Inhaltssuche filtern
    
- Verwalten von eDiscovery-Administratorrolle
    
> [!IMPORTANT]
> In diesem Artikel beschriebenen Aktivitäten sind das Ergebnis der eDiscovery-Aufgaben mithilfe der Sicherheits &amp; Compliance Center. eDiscovery-Aufgaben, die mithilfe des Compliance-eDiscovery-Tools in Exchange Online oder das eDiscovery Center in SharePoint Online ausgeführt wurden, werden nicht berücksichtigt. 
  
Weitere Informationen zur Suche des Office 365-Überwachungsprotokolls die Berechtigungen, die erforderlich sind, und Exportieren von Suchergebnissen finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).
  
## <a name="how-to-search-for-and-view-ediscovery-activities"></a>Suchen nach und eDiscovery-Aktivitäten anzeigen

Aktuell, müssen Sie einige bestimmte Aufgaben zum Anzeigen von eDiscovery-Aktivitäten in das Überwachungsprotokoll Office 365. Hier ist wie.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.
    
3. Klicken Sie im linken Bereich auf **Suche &amp; Untersuchung**, und klicken Sie auf **Audit Log suchen**.
    
4. Klicken Sie in der Dropdownliste **Aktivitäten** unter **eDiscovery Aktivitäten**, auf eine oder mehrere Aktivitäten zu suchenden. Oder Sie können auf **eDiscovery Aktivitäten** aus, die für alle Aktivitäten im Zusammenhang mit eDiscovery suchen. 
    
    > [!NOTE]
    > Die Aktivitäten Dropdown Liste enthält auch eine Gruppe von Aktivitäten, die mit dem Namen **eDiscovery-Cmdlet Aktivitäten** , mit denen Datensätze aus dem Überwachungsprotokoll Cmdlet zurückgegeben wird. 
  
5.  Wählen Sie einen Datum und Uhrzeit Bereich eDiscovery Ereignisse angezeigt, die innerhalb dieses Zeitraums aufgetreten sind. 
    
6. Wählen Sie im Feld **Benutzer** einen oder mehrere Benutzer Anzeige von Suchergebnissen für ein. Lassen Sie dieses Feld leer, Zurückgeben von Einträgen für alle Benutzer. 
    
7. Klicken Sie auf **Suche** zum Ausführen der Suche mit den Suchkriterien. 
    
8. Nachdem die Suchergebnisse angezeigt werden, können Sie **Filterergebnisse** filtern oder sortieren die resultierende Aktivitätsdatensätze klicken. Leider können Sie filtern explizit Ausschließen bestimmter Aktivitäten. 
    
9. Um Details zu einer Aktivität anzeigen möchten, klicken Sie auf den Datensatz in der Liste der Suchergebnisse. 
    
    **Details** Ausfliegen Seite wird angezeigt, die die detaillierten Eigenschaften aus dem Ereignisdatensatz enthält. Um weitere Details anzuzeigen, klicken Sie auf **Weitere Informationen**. Eine Beschreibung dieser Eigenschaften finden Sie im Abschnitt [Detailangaben zu den Eigenschaften für eDiscovery-Aktivitäten](#detailed-properties-for-ediscovery-activities) . 

  
## <a name="ediscovery-activities"></a>eDiscovery-Aktivitäten

Die folgende Tabelle beschreibt die Inhaltssuche und eDiscovery-bezogene Aktivitäten, die protokolliert werden, wenn ein Administrator oder Benutzer eine eDiscovery-bezogene Aktivität führt mithilfe der Sicherheits &amp; Compliance Center oder durch Ausführen des entsprechenden Cmdlets Remote-PowerShell, die Sicherheit Ihrer Organisation verbunden ist &amp; Compliance Center. 
  
> [!NOTE]
> In diesem Abschnitt beschriebenen eDiscovery Aktivitäten bieten ähnliche Informationen wie die eDiscovery-Cmdlet-Aktivitäten im nächsten Abschnitt beschrieben. Es wird empfohlen, dass Sie verwenden die eDiscovery-Aktivitäten, die in diesem Abschnitt beschrieben werden, da sie in den Suchergebnissen für Audit Log innerhalb von 30 Minuten angezeigt werden. Es dauert bis zu 24 Stunden für den eDiscovery Cmdlet Aktivitäten aus, die in Audit Log-Suchergebnissen angezeigt werden. 
  
|**Anzeigename**|**Operation**|**Entsprechende cmdlet**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|Element zu eDiscovery-Fall hinzugefügt  <br/> |CaseMemberAdded  <br/> |Hinzufügen von ComplianceCaseMember  <br/> |Ein Benutzer wurde als Mitglied einer eDiscovery-Fall hinzugefügt. Als Mitglied der Fall kann ein Benutzer verschiedene Aufgaben im Zusammenhang mit Groß-/Kleinschreibung je nachdem, ob sie die erforderlichen Berechtigungen zugewiesen wurden, ausführen.  <br/> |
|Geänderte Inhaltssuche  <br/> |SearchUpdated  <br/> |Set-ComplianceSearch  <br/> |Eine vorhandene Inhalte Suche wurde geändert. Hinzufügen oder Entfernen von Speicherorte für Inhalte oder bearbeiten die Suchabfrage, können Änderungen enthalten.  <br/> |
|Mitgliedschaft in der Administratorgruppe geänderten eDiscovery  <br/> |CaseAdminUpdated  <br/> |Update-eDiscoveryCaseAdmin  <br/> |Die Liste der eDiscovery-Administratoren in Ihrer Organisation wurde geändert. Diese Aktivität wird protokolliert, wenn die Liste der eDiscovery-Administratoren mit einer Gruppe von neuen Benutzern ersetzt wird. Wenn ein einzelner Benutzer hinzugefügt oder entfernt wird, wird der Vorgang CaseAdminAdded protokolliert.  <br/> |
|Geänderte eDiscovery-Fall  <br/> |CaseUpdated  <br/> |Set-ComplianceCase  <br/> |EDiscovery-Fall wurde geändert. Änderungen enthalten Schließen einer offenen Anfrage oder eine geschlossene Anfrage erneut öffnen.  <br/> |
|Groß-/Kleinschreibung geänderten eDiscovery-Mitgliedschaft  <br/> |CaseMemberUpdated  <br/> |Update-ComplianceCaseMember  <br/> |Liste der Mitglieder einer eDiscovery-Fall wurde geändert. Wenn alle Mitglieder einer Gruppe von neuen Benutzern ersetzt werden, wird diese Aktivität protokolliert. Wenn ein einzelnes Element hinzugefügt oder entfernt wird, wird die CaseMemberAdded oder CaseMemberRemoved Vorgang protokolliert.  <br/> |
|Suchfilter Berechtigungen geändert  <br/> |SearchPermissionUpdated  <br/> |Set-ComplianceSecurityFilter  <br/> |Suchfilter Berechtigungen wurde geändert.  <br/> |
|Geänderte Suchabfrage für eDiscovery Groß-/Kleinschreibung Haltestatus  <br/> |HoldUpdated  <br/> |Set-CaseHoldRule  <br/> |Eine abfragebasierte Aufbewahrung, eDiscovery-Fall zugeordnet wurde geändert. Mögliche Änderungen gehören das Bearbeiten der Abfrage, oder halten Sie Datumsbereich für eine Abfrage basiert.  <br/> |
|Inhaltssuche Preview Element heruntergeladen  <br/> |PreviewItemDownloaded  <br/> |Nicht zutreffend  <br/> |Ein Benutzer heruntergeladen ein Element auf ihrem lokalen Computer (durch Klicken auf den Link **herunterladen Originalelement** ) beim Anzeigen einer Vorschau der Suchergebnisse.  <br/> |
|Inhaltssuche Preview Element aufgelistet.  <br/> |PreviewItemListed  <br/> |Nicht zutreffend  <br/> |Ein Benutzer geklickt **Vorschau der Suchergebnisse** zum Anzeigen der Vorschau Suchergebnisseite, der bis zu 1000 Elemente aus den Ergebnissen einer Inhaltssuche aufgeführt sind.  <br/> |
|Inhaltssuche Preview Element angezeigt.  <br/> |PreviewItemRendered  <br/> |Nicht zutreffend  <br/> |Ein eDiscovery-Manager angezeigt ein Elements durch Klicken auf beim Anzeigen der Vorschau der Suchergebnisse.  <br/> |
|Erstellte Inhaltssuche  <br/> |SearchCreated  <br/> |New-ComplianceSearch  <br/> |Eine neue Inhaltssuche erstellt wurde.  <br/> |
|Erstellte eDiscovery-administrator  <br/> |CaseAdminAdded  <br/> |Hinzufügen von eDiscoveryCaseAdmin  <br/> |Ein Benutzer wurde als einer eDiscovery-Administrator in der Organisation hinzugefügt.  <br/> |
|Erstellte eDiscovery-Fall  <br/> |CaseAdded  <br/> |Neue ComplianceCase  <br/> |EDiscovery-Fall erstellt wurde. Wenn eine Anfrage erstellt wurde, müssen Sie nur einen Namen zu geben. Andere Case-bezogene Aufgaben wie das Hinzufügen von Mitgliedern, Haltestatus erstellen und Erstellen von Suchen in zusätzliche Ereignisse protokolliert wird die Groß-/Kleinschreibung Ergebnis zugeordnet.  <br/> |
|Suchfilter Berechtigungen erstellt  <br/> |SearchPermissionCreated  <br/> |Neue ComplianceSecurityFilter  <br/> |Suchfilter Berechtigungen erstellt wurde.  <br/> |
|Erstellte Suchabfrage für eDiscovery Groß-/Kleinschreibung Haltestatus  <br/> |HoldCreated  <br/> |Neue CaseHoldRule  <br/> |Eine abfragebasierte Aufbewahrung, eDiscovery-Fall zugeordnet wurde erstellt.  <br/> |
|Gelöschte Inhaltssuche  <br/> |SearchRemoved  <br/> |Remove-ComplianceSearch  <br/> |Eine vorhandene Inhaltssuche wurde gelöscht.  <br/> |
|Gelöschte eDiscovery-administrator  <br/> |CaseAdminRemoved  <br/> |Remove-eDiscoveryCaseAdmin  <br/> |Eine eDiscovery-Administrator wurde aus Ihrer Organisation gelöscht.  <br/> |
|Gelöschte eDiscovery-Fall  <br/> |CaseRemoved  <br/> |Remove-ComplianceCase  <br/> |EDiscovery-Fall wurde gelöscht. Beachten Sie, dass eine Sperre die Groß-/Kleinschreibung zugeordnet, entfernt werden soll, bevor die Groß-/Kleinschreibung gelöscht werden kann.  <br/> |
|Gelöschte Berechtigungen Suchfilter  <br/> |SearchPermissionRemoved  <br/> |Remove-ComplianceSecurityFilter  <br/> |Suchfilter Berechtigungen wurde gelöscht.  <br/> |
|Gelöschte Suchabfrage für eDiscovery Groß-/Kleinschreibung Haltestatus  <br/> |HoldRemoved  <br/> |Remove-CaseHoldRule  <br/> |Eine abfragebasierte Aufbewahrung, eDiscovery-Fall zugeordnet wurde gelöscht. Entfernen der Abfrage aus dem Haltestatus ist häufig das Ergebnis des Löschens von eines Haltestatus. Wenn einem Haltestatus oder eine Abfrage Haltestatus gelöscht werden, werden die Speicherorte für Inhalte, die in der Warteschleife waren freigegeben.  <br/> |
|Heruntergeladenen Export von Inhaltssuche  <br/> |SearchResultDownloaded  <br/> |Nicht zutreffend  <br/> |Ein Benutzer heruntergeladen die Ergebnisse einer Suche Content auf ihrem lokalen Computer. Beachten Sie, dass eine Aktivität **gestartet Exportieren der Inhaltssuche** initiiert werden, bevor die Suchergebnisse heruntergeladen werden können.<br/> |
|Als Vorschau angezeigte Ergebnisse der Inhaltssuche  <br/> |SearchPreviewed  <br/> |Nicht zutreffend  <br/> |Ein Benutzer eine Vorschau der Ergebnisse einer Suche Content.  <br/> |
|Zeitfenster Ergebnisse der Inhaltssuche  <br/> |SearchResultsPurged  <br/> |New-ComplianceSearchAction  <br/> |Ein Benutzer gelöscht die Ergebnisse einer Inhaltssuche durch Ausführen der **New-ComplianceSearchAction-bereinigen** Befehl.  <br/> |
|Entfernte Analyse der Inhaltssuche  <br/> |RemovedSearchResultsSentToZoom  <br/> |Remove-ComplianceSearchAction  <br/> |Eine Inhaltssuche vorbereiten Aktion (zum Vorbereiten der Suchergebnisse für Office 365 erweiterte eDiscovery) wurde gelöscht. Wenn die Aktion zur Vorbereitung auf weniger als zwei Wochen war, wurden die Suchergebnisse, die für erweiterte eDiscovery vorbereitet wurden aus dem Bereich der Microsoft Azure-Speicher gelöscht. Wenn die Aktion Vorbereitung älter als zwei Wochen wurde, gibt dieses Ereignis, dass nur die entsprechende Aktion Vorbereitung gelöscht wurde.  <br/> |
|Entfernte Export von Inhaltssuche  <br/> |RemovedSearchExported  <br/> |Remove-ComplianceSearchAction  <br/> |Eine Inhaltssuche Export-Aktion wurde gelöscht. Wenn die Export-Aktion weniger als zwei Wochen war, wurden die Suchergebnisse, die für die Microsoft Azure Storage Area hochgeladen wurden gelöscht. Wenn die Export-Aktion älter als zwei Wochen wurde, gibt dieses Ereignis, dass nur die entsprechende Aktion Export gelöscht wurde.  <br/> |
|Entfernte Member von eDiscovery-Fall  <br/> |CaseMemberRemoved  <br/> |Remove-ComplianceCaseMember  <br/> |Ein Benutzer wurde als Mitglied einer eDiscovery-Fall entfernt.  <br/> |
|Entfernt Vorschau der Ergebnisse von Inhaltssuche  <br/> |RemovedSearchPreviewed  <br/> |Remove-ComplianceSearchAction  <br/> |Eine Inhaltssuche Preview Aktion wurde gelöscht.  <br/> |
|Entfernte Purge-Aktion für die Inhaltssuche  <br/> |RemovedSearchResultsPurged  <br/> |Remove-ComplianceSearchAction  <br/> |Bei der Aktion ein Inhaltssuche wurde gelöscht.  <br/> |
|Entfernt Suchbericht  <br/> |SearchReportRemoved  <br/> |Remove-ComplianceSearchAction  <br/> |Eine Inhaltssuche exportieren Bericht, dass Aktion gelöscht wurde.  <br/> |
|Schritte Analyse der Inhaltssuche  <br/> |SearchResultsSentToZoom  <br/> |New-ComplianceSearchAction  <br/> |Die Ergebnisse einer Inhaltssuche wurden für die Analyse in erweiterten eDiscovery vorbereitet.  <br/> |
|Schritte Inhaltssuche  <br/> |SearchStarted  <br/> |Start-ComplianceSearch  <br/> |Eine Inhaltssuche wurde gestartet. Beim Erstellen oder Ändern einer Inhaltssuche mithilfe der Sicherheits &amp; Compliance Center GUI, für die Suche wird automatisch gestartet. Wenn Sie erstellen oder ändern eine Suche mithilfe des **New-ComplianceSearch** oder **Set-ComplianceSearch** -Cmdlet, müssen Sie das Cmdlet **Start-ComplianceSearch** zum Starten der Suche auszuführen.<br/> |
|Schritte beim Export von Inhaltssuche  <br/> |SearchExported  <br/> |New-ComplianceSearchAction  <br/> |Ein Benutzer exportiert die Ergebnisse einer Suche Content.  <br/> |
|Schritte beim Exportbericht  <br/> |SearchReport  <br/> |New-ComplianceSearchAction  <br/> |Ein Benutzer exportiert einen Inhaltssuche-Bericht.  <br/> |
|Beendet die Inhaltssuche  <br/> |SearchStopped  <br/> |Stop-ComplianceSearch  <br/> |Ein Benutzer hat eine Inhaltssuche beendet.  <br/> |
  
## <a name="ediscovery-cmdlet-activities"></a>eDiscovery-Cmdlet Aktivitäten

Die folgende Tabelle enthält die Cmdlet-Überwachungsprotokolldatensätze, die protokolliert werden, wenn ein Administrator oder Benutzer eine eDiscovery-bezogene Aktivität führt mithilfe der Sicherheits &amp; Compliance Center oder durch Ausführen des entsprechenden Cmdlets in remote-PowerShell, die den verbunden mit Sicherheit Ihrer Organisation &amp; Compliance Center. Beachten Sie, dass die detaillierte Informationen in den Protokolleintrag Audit für die in dieser Tabelle aufgeführten Cmdlets Aktivitäten und die eDiscovery-Aktivitäten, die im vorherigen Abschnitt beschrieben ist. 
  
Wie bereits zuvor erwähnt dauert bis zu 24 Stunden für eDiscovery Cmdlet Aktivitäten aus, die in den Suchergebnissen für Audit Log angezeigt werden.
  
> [!TIP]
> Die Cmdlets in der Spalte **Vorgang** in der folgenden Tabelle sind zum entsprechenden Cmdlet Hilfethema auf TechNet-Website verknüpft. Wechseln Sie zum Cmdlet Hilfethema eine Beschreibung der verfügbaren Parameter für jedes-Cmdlet. Der Parameter und der Wert des Parameters, die mit einem-Cmdlet verwendet wurden sind in der Überwachungsprotokolleintrag für jede eDiscovery-Cmdlet-Aktivität enthalten, die angemeldet ist. 
  
|**Anzeigename**|**Vorgang (Cmdlet)**|**Beschreibung**|
|:-----|:-----|:-----|
|Erstellte Haltestatus in eDiscovery-Fall  <br/> |[Neue CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823813) <br/> |Ein Haltestatus wurde für einen eDiscovery-Fall erstellt. Ein Haltestatus kann mit oder ohne Angabe einer Inhaltsquelle erstellt werden. Inhaltsquellen angegeben, werden sie in der Überwachungsprotokolleintrag identifiziert werden.  <br/> |
|Gelöschte halten von eDiscovery-Fall  <br/> |[Remove-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823814) <br/> |Ein Haltestatus, der einem eDiscovery-Fall zugeordnet ist, wurde gelöscht. Löschen von einem Haltestatus gibt alle die Speicherorte für Inhalte aus dem Haltestatus frei. Löschen den Haltestatus auch führt zu löschen der Groß-/Kleinschreibung Hold-Regeln, die dem Haltebereich zugeordnet (siehe **Remove-CaseHoldRule** unten).<br/> |
|Geänderte Haltestatus in eDiscovery-Fall  <br/> |[Set-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823815) <br/> |Ein Haltestatus, der ein eDiscovery zugeordnet ist, wurde geändert. Mögliche Änderungen enthalten, hinzufügen oder Entfernen von Speicherorte für Inhalte oder ausschalten (deaktivieren) den Haltebereich.  <br/> |
|Erstellte Suchabfrage für eDiscovery Groß-/Kleinschreibung Haltestatus  <br/> |[Neue CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823816) <br/> |Eine abfragebasierte Aufbewahrung, eDiscovery-Fall zugeordnet wurde erstellt.  <br/> |
|Gelöschte Suchabfrage für eDiscovery Groß-/Kleinschreibung Haltestatus  <br/> |[Remove-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823820) <br/> |Eine abfragebasierte Aufbewahrung, eDiscovery-Fall zugeordnet wurde gelöscht. Entfernen der Abfrage aus dem Haltestatus ist häufig das Ergebnis des Löschens von eines Haltestatus. Wenn einem Haltestatus oder eine Abfrage Haltestatus gelöscht werden, werden die Speicherorte für Inhalte, die in der Warteschleife waren freigegeben.  <br/> |
|Geänderte Suchabfrage für eDiscovery Groß-/Kleinschreibung Haltestatus  <br/> |[Set-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823819) <br/> |Eine abfragebasierte Aufbewahrung, eDiscovery-Fall zugeordnet wurde geändert. Mögliche Änderungen gehören das Bearbeiten der Abfrage, oder halten Sie Datumsbereich für eine Abfrage basiert.  <br/> |
|Erstellte eDiscovery-Fall  <br/> |[Neue ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823842) <br/> |EDiscovery-Fall erstellt wurde. Wenn eine Anfrage erstellt wurde, müssen Sie nur einen Namen zu geben. Andere Case-bezogene Aufgaben wie das Hinzufügen von Mitgliedern, Haltestatus erstellen und Erstellen von Suchen in zusätzliche Ereignisse protokolliert wird die Groß-/Kleinschreibung Ergebnis zugeordnet.  <br/> |
|Gelöschte eDiscovery-Fall  <br/> |[Remove-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823844) <br/> |EDiscovery-Fall wurde gelöscht. Beachten Sie, dass eine Sperre die Groß-/Kleinschreibung zugeordnet, entfernt werden soll, bevor die Groß-/Kleinschreibung gelöscht werden kann.  <br/> |
|Geänderte eDiscovery-Fall  <br/> |[Set-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823846) <br/> |EDiscovery-Fall wurde geändert. Änderungen enthalten Schließen einer offenen Anfrage oder eine geschlossene Anfrage erneut öffnen.  <br/> |
|Element zu eDiscovery-Fall hinzugefügt  <br/> |[Hinzufügen von ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823848) <br/> |Ein Benutzer wurde als Mitglied einer eDiscovery-Fall hinzugefügt. Als Mitglied der Fall kann ein Benutzer verschiedene Aufgaben im Zusammenhang mit Groß-/Kleinschreibung je nachdem, ob sie die erforderlichen Berechtigungen zugewiesen wurden, ausführen.  <br/> |
|Entfernte Member von eDiscovery-Fall  <br/> |[Remove-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823849) <br/> |Ein Benutzer wurde als Mitglied einer eDiscovery-Fall entfernt.  <br/> |
|Groß-/Kleinschreibung geänderten eDiscovery-Mitgliedschaft  <br/> |[Update-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823850) <br/> |Liste der Mitglieder einer eDiscovery-Fall wurde geändert. Wenn alle Mitglieder einer Gruppe von neuen Benutzern ersetzt werden, wird diese Aktivität protokolliert. Wenn ein einzelnes Element hinzugefügt oder entfernt wird, wird der Vorgang **Hinzufügen ComplianceCaseMember** oder **Remove-ComplianceCaseMember** protokolliert.<br/> |
|Erstellte Inhaltssuche  <br/> |[New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935) <br/> |Eine neue Inhaltssuche erstellt wurde.  <br/> |
|Gelöschte Inhaltssuche  <br/> |[Remove-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517936) <br/> |Eine vorhandene Inhaltssuche wurde gelöscht.  <br/> |
|Geänderte Inhaltssuche  <br/> |[Set-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517937) <br/> |Eine vorhandene Inhalte Suche wurde geändert. Hinzufügen oder Entfernen von Speicherorte für Inhalte, die durchsucht werden und bearbeiten die Suchabfrage, können Änderungen enthalten.  <br/> |
|Schritte Inhaltssuche  <br/> |[Start-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517938) <br/> |Eine Inhaltssuche wurde gestartet. Beim Erstellen oder Ändern einer Inhaltssuche mithilfe der Sicherheits &amp; Compliance Center GUI, für die Suche wird automatisch gestartet. Wenn Sie erstellen oder ändern eine Suche mithilfe des **New-ComplianceSearch** oder **Set-ComplianceSearch** -Cmdlet, müssen Sie das Cmdlet **Start-ComplianceSearch** zum Starten der Suche auszuführen.<br/> |
|Beendet die Inhaltssuche  <br/> |[Stop-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517939) <br/> |Eine Inhaltssuche, der ausgeführt wurde, wurde beendet.  <br/> |
|Inhaltssuche-Aktion erstellt  <br/> |[New-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=527971) <br/> |Eine Inhaltssuche-Aktion erstellt wurde. Inhaltssuche zählen Vorschau der Suchergebnisse, Suchergebnisse exportieren, Vorbereiten der Suchergebnisse für die Analyse in Office 365 erweiterte eDiscovery und Elemente, die die Suchkriterien ein Inhaltssuche endgültig gelöscht werden.  <br/> |
|Gelöschte Inhaltssuche-Aktion  <br/> |[Remove-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=824027) <br/> |Eine Aktion Inhaltssuche wurde gelöscht.  <br/> |
|Suchfilter Berechtigungen erstellt  <br/> |[Neue ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617542) <br/> |Suchfilter Berechtigungen erstellt wurde.  <br/> |
|Gelöschte Berechtigungen Suchfilter  <br/> |[Remove-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617543) <br/> |Suchfilter Berechtigungen wurde gelöscht.  <br/> |
|Suchfilter Berechtigungen geändert  <br/> |[Set-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617544) <br/> |Suchfilter Berechtigungen wurde geändert.  <br/> |
|Erstellte eDiscovery-administrator  <br/> |[Hinzufügen von eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=798217) <br/> |Ein Benutzer wurde als einer eDiscovery-Administrator in Ihrer Organisation hinzugefügt.  <br/> |
|Gelöschte eDiscovery-administrator  <br/> |[Remove-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823945) <br/> |Eine eDiscovery-Administrator wurde aus Ihrer Organisation gelöscht.  <br/> |
|Mitgliedschaft in der Administratorgruppe geänderten eDiscovery  <br/> |[Update-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823946) <br/> |Die Liste der eDiscovery-Administratoren in Ihrer Organisation wurde geändert. Diese Aktivität wird protokolliert, wenn die Liste der eDiscovery-Administratoren mit einer Gruppe von neuen Benutzern ersetzt wird. Wenn ein einzelner Benutzer hinzugefügt oder entfernt wird, wird der Vorgang **Hinzufügen eDiscoveryCaseAdmin** oder **Remove-eDiscoveryCaseAdmin** protokolliert.<br/> |
   
## <a name="detailed-properties-for-ediscovery-activities"></a>Detailangaben zu den Eigenschaften für eDiscovery-Aktivitäten

Die folgende Tabelle beschreibt die Eigenschaften, die eingebunden werden, wenn Sie **Weitere Informationen** auf der Seite **Details** für eine eDiscovery-Aktivität in den Suchergebnissen aufgeführt. Diese Eigenschaften sind auch in der CSV-Datei enthalten, wenn Sie die Ergebnisse der Audit Log exportieren. Beachten Sie, dass ein Audit Log-Eintrag für eine eDiscovery-Aktivität für jede unten aufgeführten detaillierte Eigenschaft wird nicht. 
  
> [!TIP]
> Wenn Sie die Suchergebnisse exportieren, enthält die CSV-Datei eine Spalte mit dem Namen **Detail**, das detaillierten Eigenschaften beschrieben, die in der folgenden Tabelle in eine mehrwertige Eigenschaft enthält. Sie können die Abfrage Power-Funktion in Excel verwenden, mehrere Spalten in dieser Spalte aufgeteilt werden, damit jede Eigenschaft eine eigenen Spalte verwendet werden. Dadurch können Sie sortieren und Filtern für ein oder mehrere dieser Eigenschaften. Weitere Informationen finden Sie im Abschnitt "Die Suchergebnisse in eine Datei exportieren" bei der [Suche der Überwachungsprotokolle melden Sie sich bei der Office 365-Sicherheit und Compliance Center ](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file). 
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|Fall  <br/> |Die Identität (GUID) des eDiscovery-Fall, die erstellt, geändert oder gelöscht wurde.  <br/> |
|ClientApplication  <br/> |eDiscovery-Cmdlet Aktivitäten verwendet einen Wert von **EMC** für diese Eigenschaft. Dies gibt an, die Aktivität ausgeführt wurde, mithilfe der Sicherheits &amp; Compliance Center GUI oder das Cmdlet in PowerShell ausführen.<br/> |
|ClientIP  <br/> |Die IP-Adresse des Geräts, das verwendet wurde, wenn die Aktivität protokolliert wurde. Die IP-Adresse wird in ein IPv4 oder IPv6-Adressformat angezeigt.  <br/> |
|ClientRequestId  <br/> | Diese Eigenschaft ist für eDiscovery-Aktivitäten in der Regel leer.  <br/> |
|CmdletVersion  <br/> |Die Buildnummer für die Version der Sicherheit &amp; in Ihrer Organisation ausgeführten Compliance Center.  <br/> |
|CreationTime  <br/> |Das Datum und die Uhrzeit in koordinierter Weltzeit (UTC), wenn die eDiscovery-Aktivität abgeschlossen wurde.  <br/> |
|EffectiveOrganization  <br/> |Der Name der die Office 365-Organisation.  <br/> |
|ExchangeLocations  <br/> |Exchange Online-Postfächer, die in einer Inhaltssuche enthalten oder gebracht werden in einem eDiscovery-Fall halten.  <br/> |
|Ausschlüsse  <br/> |Postfach oder einer Website Standorte, die von einem Inhaltssuche oder einem Haltestatus in einem eDiscovery-Fall ausgeschlossen werden.  <br/> |
|ExtendedProperties  <br/> |Zusätzliche Eigenschaften aus einem Inhalt suchen, eine Aktion Inhaltssuche oder halten Sie in einem eDiscovery-Fall, wie die Objekt-GUID und der entsprechenden Cmdlet und Cmdlet-Parameter, die verwendet wurden, wenn die Aktivität ausgeführt wurde.  <br/> |
|Id  <br/> |Die ID des Berichts-Eintrags. Die ID identifiziert eindeutig die Überwachungsprotokolleintrag.  <br/> |
|NonPIIParameters  <br/> |Eine Liste der Parameter (ohne Werte), die mit dem Cmdlet in der Eigenschaft Vorgang identifiziert verwendet wurden. In dieser Eigenschaft aufgeführten Parameter sind die gleichen, die in der Parameters-Eigenschaft aufgeführt.  <br/> |
|ObjectId  <br/> |Die GUID oder den Namen des Objekts (beispielsweise eine Inhaltssuche oder einem eDiscovery-Fall), das erstellt wurde, geändert oder gelöscht, indem Sie die Aktivität, die in die Operation-Eigenschaft aufgelistet. Dieses Objekt wird auch in der Spalte Element in den Suchergebnissen für Audit Log identifiziert.  <br/> |
|ObjectType  <br/> |Die Art der eDiscovery-Objekt, das der Benutzer erstellt, gelöscht oder geändert. Beispiel einer Aktion Inhaltssuche (Preview, exportieren oder löschen), einem eDiscovery-Fall oder eine Inhaltssuche.  <br/> |
|Vorgang  <br/> |Der Name des Vorgangs, der die Aktivität eDiscovery entspricht, die durchgeführt wurden.  <br/> |
|Organisations-ID an  <br/> |Die GUID für Office 365-Organisation.  <br/> |
|Parameter  <br/> |Der Name und Wert für die Parameter, die mit dem entsprechenden Cmdlet verwendet wurden.  <br/> |
|PublicFolderLocations  <br/> |Halten Sie die Speicherorte für Öffentliche Ordner in Exchange-Online, die in einer Inhaltssuche enthalten oder gebracht werden in einem eDiscovery-Fall.  <br/> |
|Abfrage  <br/> |Die Suchabfrage die Aktivität, wie eine Inhaltssuche oder eine abfragebasierte Aufbewahrung zugeordnet.  <br/> |
|RecordType  <br/> |Der Typ des Vorgangs durch den Eintrag angegeben. Der Wert von **18** gibt ein Ereignis im Zusammenhang mit einer Aktivität im Abschnitt [eDiscovery-Cmdlet Aktivitäten](#ediscovery-cmdlet-activities) aufgelistet. Der Wert **24** gibt an, ein Ereignis im Zusammenhang mit einer Aktivität im Abschnitt [Suchen nach und Anzeigen von Aktivitäten eDiscovery](#how-to-search-for-and-view-ediscovery-activities) aufgeführt.<br/> |
|ResultStatus  <br/> |Gibt an, ob die Aktion (in der Operation-Eigenschaft angegeben) erfolgreich war.  <br/> |
|SecurityComplianceCenterEventType  <br/> |Gibt an, dass die Aktivität eines Wertpapiers wurde &amp; Compliance Center-Ereignis. Alle eDiscovery-Aktivitäten müssen einen Wert von **0** für diese Eigenschaft.<br/> |
|SharepointLocations  <br/> |SharePoint Online-Websites, die in einer Inhaltssuche enthalten oder gebracht werden in einem eDiscovery-Fall halten.  <br/> |
|StartTime  <br/> |Das Datum und die Uhrzeit in koordinierter Weltzeit (UTC), wenn die eDiscovery-Aktivität gestartet wurde.  <br/> |
|Benutzer-ID  <br/> |Der Benutzer, der die Aktivität (in der Operation-Eigenschaft angegeben) ausgeführt wird, die den Datensatz protokolliert geführt hat. Beachten Sie, dass Einträge für eDiscovery-Aktivitäten von Systemkonten (beispielsweise NT-Autorität\System) auch im Überwachungsprotokoll enthalten sind.  <br/> |
|UserKey  <br/> |Eine alternative ID für den Benutzer in der UserId-Eigenschaft identifiziert. Für eDiscovery-Aktivitäten ist der Wert für diese Eigenschaft in der Regel die UserId-Eigenschaft identisch.  <br/> |
|UserServicePlan  <br/> |Das Office 365-Abonnement Ihrer Organisation verwendeten. Diese Eigenschaft ist für eDiscovery-Aktivitäten in der Regel leer.  <br/> |
|UserType  <br/> |Der Typ des Benutzers, der der Vorgang ausgeführt wird. Die folgenden Werte geben den Benutzer.  <br/> 0 ein regelmäßiger Benutzer. 2 ein Administrator in Office 365-Organisation. 3 als Microsoft Datacenter-Administrator oder Datacenter Systemkonto berücksichtigt. 4 als Systemkonto berücksichtigt. 5 eine Anwendung. 6 einen Dienstprinzipal. |
|Version  <br/> |Gibt die Versionsnummer der Aktivität (identifiziert durch die Operation-Eigenschaft), die angemeldet ist.  <br/> |
|Arbeitslast  <br/> |Der Office 365-Dienst, in die Aktivität aufgetreten ist. Für eDiscovery-Aktivitäten ist der Wert **SecurityComplianceCenter**.<br/> |
