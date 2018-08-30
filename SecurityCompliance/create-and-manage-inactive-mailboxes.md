---
title: Erstellen Sie und verwalten Sie inaktiver Postfächer in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
description: Sie können ein inaktives Postfachs in Office 365 erstellen, Anwenden einer Warteschleife oder Office 365 Aufbewahrungsrichtlinie auf das Postfach und das entsprechende Office 365-Benutzerkonto löschen. Elemente in eines inaktiven Postfachs bleiben für die Dauer der Richtlinie halten oder die Aufbewahrung, die darauf angewendet wurde, bevor sie als inaktiv festgelegt wurde. Zum Löschen eines inaktiven Postfachs nur entfernen Sie die Warteschleife oder Aufbewahrung Richtlinie.
ms.openlocfilehash: ed0af9077222d9151dc41010bca10590769118b1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529225"
---
# <a name="create-and-manage-inactive-mailboxes-in-office-365"></a>Erstellen Sie und verwalten Sie inaktiver Postfächer in Office 365

Office 365 ermöglicht es Ihnen, den Inhalt der gelöschte Postfächer zu behalten. Dieses Feature heißt [inaktiver Postfächer](inactive-mailboxes-in-office-365.md). Inaktive Postfächer können Sie frühere Mitarbeiter e-Mail beibehalten, wenn die Organisation verlassen. Ein Postfach wird inaktiv, wenn ein Beweissicherungsverfahren oder eine Aufbewahrungsrichtlinie für Office 365 (erstellt in der Office 365-Sicherheit &amp; Compliance Center) auf das Postfach angewendet wird, bevor das entsprechende Office 365-Benutzerkonto gelöscht wird. Der Inhalt eines inaktiven Postfachs werden für die Dauer des Haltestatus weitergeführt, die für das Postfach getätigt wurde, bevor sie als inaktiv festgelegt wurde. Dies ermöglicht Administratoren, Compliance Officer und Datensätze Inhaltssuche in das Wertpapier erachten &amp; Compliance Center zum Suchen und Exportieren des Inhalts eines inaktiven Postfachs. Inaktive Postfächer e-Mail nicht empfangen werden und sind nicht in anderen Listen oder freigegebenen Adressbuch Ihrer Organisation angezeigt.
  
> [!NOTE]
> Wir haben den Stichtag (1. Juli 2017) zum Erstellen von neuem In-Situ-Speicher, um ein Postfach als inaktiv zu markieren, nach hinten verlegt. Ende dieses Jahres oder Anfang des nächsten Jahres können Sie keinen neuen In-Situ-Speicher in Exchange Online mehr erstellen. Es können dann nur noch das Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Vorhandene inaktive Postfächer, die sich im In-Situ-Speicher befinden, werden jedoch weiterhin unterstützt, und Sie können weiterhin die In-Situ-Speicher für inaktive Postfächer verwalten. Dazu zählen das Ändern der Dauer eines In-Situ-Speichers sowie das dauerhafte Löschen eines inaktiven Postfachs durch Entfernen des In-Situ-Speichers. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Damit ein Postfach inaktiv ist, muss es eine Lizenz für Exchange Online – Plan 2 zugewiesen werden, damit eine Aufbewahrung für eventuelle Rechtsstreitigkeiten oder eine Aufbewahrungsrichtlinie für Office 365 an das Postfach angewendet werden kann, bevor es gelöscht wird. Exchange Online – Plan 2 Lizenzen sind Teil einer Office 365 Enterprise E3 und E5-Abonnements. Wenn ein Postfach eine Lizenz für Exchange Online – Plan 1 zugeordnet ist (die Teil eines Office 365 Enterprise E1-Abonnements ist), müssten Sie es eine separate Lizenz Exchange Online-Archivierung zuweisen, sodass ein Haltestatus an das Postfach angewendet werden kann, bevor es gelöscht wird. Weitere Informationen finden Sie unter [Exchange Online-Archivierung](https://go.microsoft.com/fwlink/p/?LinkId=286153).
    
- Die Lizenz der gelöschten Exchange Online-Postfach zugeordnet sind nach dem Löschen des entsprechenden Benutzerkontos für Office 365 verfügbar. Anschließend können Sie [Lizenzen für Benutzer in Office 365 für Unternehmen zuweisen](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) an einen anderen Benutzer. 
    
- Wenn vor dem Löschen des Postfachs für dieses kein Beweissicherungsverfahren aktiviert bzw. keine Office 365-Aufbewahrungsrichtlinie auf dieses angewendet wird, werden die Inhalte des Postfachs nicht beibehalten bzw. können diese nicht gefunden werden. Das gelöschte Postfach kann innerhalb von 30 Tagen nach dem Löschen wiederhergestellt werden; wird es nicht innerhalb von 30 Tagen wiederhergestellt, wird das Postfach samt Inhalten unwiderruflich gelöscht.
    
- Weitere Informationen zum Beweissicherungsverfahren finden Sie unter [In-Place Hold and Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=846124). Weitere Informationen zu Office 365-Aufbewahrungsrichtlinien im Security &amp; Compliance Center finden Sie unter [Übersicht über Aufbewahrungsrichtlinien in Office 365](retention-policies.md).
  
## <a name="create-an-inactive-mailbox"></a>Erstellen eines inaktiven Postfachs

Ein Postfach inaktiv machen umfasst zwei Schritte: (1) platzieren das Postfach für Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Anwenden einer Aufbewahrungsrichtlinie für Office 365 hinzu und (2) Löschen des Postfachs oder ein entsprechendes Benutzerkonto für Office 365. Nachdem das Postfach nicht aktiv ist, werden dessen Inhalt beibehalten, bis die Warteschleife oder Aufbewahrung Richtlinie entfernt wird.
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-an-office-365-retention-policy"></a>Schritt 1: Aktivieren des Beweissicherungsverfahrens für das Postfach oder Anwenden einer Office 365-Aufbewahrungsrichtlinie auf das Postfach

Durch Aktivieren des Beweissicherungsverfahrens für ein Postfach oder Anwenden einer Office 365-Aufbewahrungsrichtlinie auf das Postfach werden alle Inhalte des Postfachs beibehalten, bevor es gelöscht wird. Bei beiden Verfahren bleiben sämtliche Postfachinhalte einschließlich gelöschter Elemente und Originalversionen geänderter Elemente erhalten. Gelöschte und geänderte Elemente verbleiben für einen bestimmten Zeitraum im inaktiven Postfach oder solange, bis das inaktive Postfach endgültig gelöscht wird, indem die Archivierung deaktiviert wird oder die auf das inaktive Postfach angewendete Aufbewahrungsrichtlinie entfernt wird.
  
Wenn bereits eine Archivierung für ein Postfach aktiviert ist oder wenn bereits eine Office 365-Aufbewahrungsrichtlinie darauf angewendet wurde, müssen Sie lediglich das entsprechende Office 365-Benutzerkonto löschen, wie in Schritt 2 erläutert.
  
Eine Schritt-für-Schritt-Anleitung zur Aktivierung des Beweissicherungsverfahrens für ein Postfach oder zur Anwendung einer Office 365-Aufbewahrungsrichtlinie finden Sie unter:
  
- [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [Übersicht über Aufbewahrungsrichtlinien in Office 365](retention-policies.md)
    
> [!NOTE]
> Für Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien können Sie das Postfach unbegrenzt lang oder zeitlich begrenzt archivieren. Bei einer dauerhaften Aufbewahrung werden die Inhalte des inaktiven Postfachs dauerhaft oder so lange beibehalten, bis die Aufbewahrung aufgehoben oder ihre Dauer geändert wird. Nachdem die Aufbewahrung beendet oder die Aufbewahrungsrichtlinie deaktiviert wurde (vorausgesetzt, das Postfach wurde vor mehr als 30 Tagen gelöscht), wird das inaktive Postfach für das endgültige Löschen markiert, und die Inhalte des Postfachs werden nicht aufbewahrt und können nicht gefunden werden. Bei einer zeitbasierten Aufbewahrung oder einer Office 365-Aufbewahrungsrichtlinie legen Sie die Dauer der Aufbewahrung fest. Diese Dauer wird pro Element festgelegt und wird von dem Datum ab berechnet, an dem ein Postfachelement empfangen oder erstellt wurde. Nachdem die Archivierung für ein Postfachelement abgelaufen ist und sich dieses Element im Ordner „Wiederherstellbare Elemente" im inaktiven Postfach befindet, wird das Element dauerhaft aus dem inaktiven Postfach gelöscht, nachdem die Aufbewahrungsdauer für das gelöschte Element abgelaufen ist. 
  
### <a name="step-2-delete-the-mailbox"></a>Schritt 2: Löschen des Postfachs

Nachdem das Postfach in der Warteschleife platziert wird, oder eine Office 365-Aufbewahrungsrichtlinie angewendet wird, besteht der nächste Schritt das Postfach löschen. Die beste Möglichkeit zum Löschen eines Postfachs ist das entsprechende Office 365-Benutzerkonto in Office 365 Administrationscenter zu löschen. Informationen zum Löschen von Office 365-Benutzerkonten finden Sie unter [Löschen eines Benutzers aus Ihrer Organisation](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e).
  
> [!NOTE]
> Sie können auch das Postfach mithilfe des Cmdlets **Remove-Mailbox** in Exchange Online PowerShell löschen. Weitere Informationen finden Sie unter [Löschen oder Wiederherstellen von Benutzerpostfächern in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856287). 
  

## <a name="view-a-list-of-inactive-mailboxes"></a>Anzeigen einer Liste von inaktive Postfächer


Um eine Liste der inaktiver Postfächer in Ihrer Organisation anzuzeigen:
  
1. Wechseln Sie zu [https://protection.office.com/](https://protection.office.com/) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> ** Aufbewahrung **.
    
3. Klicken Sie auf der Seite **Aufbewahrung** **Weitere**![Navigationsleiste Ellipsen](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif), und klicken Sie dann auf **inaktiver Postfächer**.
    
    ![Klicken Sie auf der Seite Aufbewahrung klicken Sie auf Weitere, und klicken Sie dann auf inaktiver Postfächer zum Anzeigen einer Liste mit inaktive Postfächer](media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    Die Seite **inaktiver Postfächer** wird angezeigt. Beachten Sie, dass die Gesamtzahl der inaktiver Postfächer in Ihrer Organisation angezeigt wird. 
    
    ![Eine Liste aller inaktiver Postfächer in Ihrer Organisation wird angezeigt.](media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
Alternativ können Sie den folgenden Befehl in Exchange führen Online PowerShell, um die Liste der inaktiver Postfächer anzuzeigen.

```
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

Sie können klicken ![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Exportieren** , anzeigen oder Herunterladen einer CSV-Datei, die zusätzliche Informationen über die inaktiver Postfächer in Ihrer Organisation enthält. 
  
Sie können auch den folgenden Befehl aus, um die Liste der inaktiver Postfächer und andere Informationen in einer CSV-Datei zu exportieren ausführen. In diesem Beispiel wird die CSV-Datei im aktuellen Verzeichnis erstellt.

```
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```
   
> [!NOTE]
> Es ist möglich, dass ein inaktives Postfachs dieselbe SMTP-Adresse als aktive Benutzerpostfach möglicherweise. In diesem Fall kann der Wert der Eigenschaft **DistinguishedName** oder **ExchangeGuid** zur eindeutigen Identifizierung ein inaktives Postfachs verwendet werden. 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a>Durchsuchen und Exportieren der Inhalte eines inaktiven Postfachs

Sie können den Inhalt des inaktiven Postfachs zugreifen, indem Sie mit dem Tool für die Inhaltssuche in die Sicherheit &amp; Compliance Center. Beim Durchsuchen eines inaktiven Postfachs können Sie eine Keyword Search-Abfrage zum Suchen nach bestimmten Objekten erstellen oder Sie können den gesamten Inhalt des inaktiven Postfachs zurückgeben. Sie können eine Vorschau der Suchergebnisse oder exportieren die Suchergebnisse in eine Datei Outlook-Daten (PST) oder als einzelne e-Mail-Nachrichten. Eine schrittweise Anleitung für Postfächer durchsuchen und Exportieren von Suchergebnissen finden Sie unter den folgenden Themen:
  
- [Content-Suche in Office 365](content-search.md)
    
- [Exportieren von Suchergebnissen aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md)
    
Hier sind einige Dinge im Hinterkopf behalten, inaktiver Postfächer zu suchen.
  
- Wenn eine Inhaltssuche ein Benutzerpostfach enthält und das Postfach dann inaktiv erfolgt, wird die Inhaltssuche weiterhin inaktive Postfach suchen, wenn die Suche erneut ausführen, nachdem es deaktiviert wurde.
    
- In einigen Fällen kann ein Benutzer einer aktiven Postfach- und eines inaktiven Postfachs, die der gleichen SMTP-Adresse verfügen. In diesem Fall wird nur das spezifische Postfach, das Sie als Speicherort für ein Inhaltssuche auswählen gesucht werden soll. Anders ausgedrückt, wenn Sie dem Postfach eines Benutzers zu einer Suche hinzufügen, nicht davon ausgehen, dass ihre aktive und inaktive Postfächer durchsucht werden; Es wird nur das Postfach, das Sie für die Suche explizit hinzu gesucht werden soll.
    
- Es wird dringend empfohlen, dass Sie vermeiden, dass eine aktive Postfach- und inaktiven Postfachs mit der gleichen SMTP-Adresse. Wenn Sie müssen die SMTP-Adresse wiederverwenden, die aktuell eines inaktiven Postfachs zugewiesen ist, wird empfohlen, das inaktive Postfach wiederherstellen oder des Inhalts eines inaktiven Postfachs zu einem aktiven Postfach (oder das Archiv eines aktiven Postfachs wiederherstellen), und Sie löschen die Inaktives Postfach.
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a>Ändern der Aufbewahrungsdauer für ein inaktives Postfach

Nachdem ein Postfach inaktive vorgenommen wurde, können Sie die Dauer der Haltebereich oder der Office 365-Aufbewahrungsrichtlinie inaktives Postfach angewendet ändern. Eine schrittweise Anleitung finden Sie unter [Ändern der Dauer halten eines inaktiven Postfachs in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
  
## <a name="recover-an-inactive-mailbox"></a>Wiederherstellen eines inaktiven Postfachs

Wenn ein früheren Mitarbeiter für Ihre Organisation zurückgibt, oder wenn ein neuer Mitarbeiter eingestellt wird, die auf die Verantwortlichkeiten des Mitarbeiters departed angewendet werden, können Sie den Inhalt des inaktiven Postfachs wiederherstellen. Beim Wiederherstellen eines inaktiven Postfachs, das Postfach wird in ein neues Postfach konvertiert, den Inhalt und die Ordnerstruktur des inaktiven Postfachs werden beibehalten, und das Postfach mit ein neues Benutzerkonto verknüpft ist. Nachdem es wiederhergestellt wird, ist das inaktive Postfach nicht mehr vorhanden. Schrittweise Verfahren und Weitere Informationen zu geschieht, wenn Sie ein inaktives Postfachs wiederherstellen, finden Sie unter [Wiederherstellen ein inaktives Postfachs in Office 365](recover-an-inactive-mailbox.md).
  
[Verwalten inaktiver Postfächer](create-and-manage-inactive-mailboxes.md#manageinactivemailboxes)
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a>Wiederherstellen des Inhalts eines inaktiven Postfachs in einem anderen Postfach

Wenn eine andere Mitarbeiter auf den Verantwortungsbereich einem früheren Mitarbeiter dauert oder eine andere Person Zugriff auf den Inhalt der inaktives Postfach benötigt, können Sie wiederherstellen (den Inhalt des inaktiven Postfachs auf ein vorhandenes Postfach oder Zusammenführen). Beim Wiederherstellen eines inaktiven Postfachs wird der Inhalt auf anderes Postfach kopiert. Inaktive Postfach wird beibehalten, und eines inaktiven Postfachs bleibt. Inaktive Postfach kann weiterhin mit dem eDiscovery gesucht werden, dessen Inhalt an ein anderes Postfach wiederhergestellt werden können oder es wiederhergestellt oder zu einem späteren Zeitpunkt gelöscht werden kann. Schrittweise Anweisungen finden Sie unter [Wiederherstellen ein inaktives Postfachs in Office 365](restore-an-inactive-mailbox.md).
  
## <a name="delete-an-inactive-mailbox"></a>Löschen eines inaktiven Postfachs

Wenn Sie nicht mehr benötigen, die den Inhalt eines inaktiven Postfachs beibehalten werden, können Sie dauerhaft inaktive Postfach löschen, indem dem Haltebereich oder Entfernen der Office 365-Aufbewahrungsrichtlinie inaktives Postfach angewendet. Wenn das Postfach vor mehr als 30 Tage gelöscht wurde, wird das Postfach für endgültig markiert, nachdem Sie den Haltestatus entfernen und das Postfach wird nicht wiederhergestellt werden. Wenn das Postfach in den letzten 30 Tagen gelöscht wurde, können Sie das Postfach nach dem Entfernen der Richtlinie halten oder die Aufbewahrung wiederherstellen. Eine schrittweise Anleitung zum Entfernen von einem Haltestatus oder eine Office 365 Aufbewahrungsrichtlinie endgültig löschen ein inaktives Postfachs finden Sie unter [Löschen ein inaktives Postfachs in Office 365](delete-an-inactive-mailbox.md).