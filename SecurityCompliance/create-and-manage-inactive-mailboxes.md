---
title: Erstellen und Verwalten inaktiver Postfächer in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
description: Sie können ein inaktives Postfach in Office 365 erstellen, indem Sie für das Postfach eine Aufbewahrungs-oder Office 365-Richtlinie anwenden und dann das entsprechende Office 365-Benutzerkonto löschen. Elemente in einem inaktiven Postfach werden für die Dauer der Aufbewahrungs-oder Beibehaltungsrichtlinie beibehalten, die vor der Deaktivierung der Sperre angewendet wurde. Wenn Sie ein inaktives Postfach dauerhaft löschen möchten, entfernen Sie einfach die Aufbewahrungsrichtlinie.
ms.openlocfilehash: 8f798873da7d787b54932438e81aebf2dfe85181
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217775"
---
# <a name="create-and-manage-inactive-mailboxes-in-office-365"></a>Erstellen und Verwalten inaktiver Postfächer in Office 365

Office 365 ermöglicht es Ihnen, die Inhalte gelöschter Postfächer beizubehalten. Dieses Feature wird als [inaktive Postfächer](inactive-mailboxes-in-office-365.md)bezeichnet. InAktive Postfächer ermöglichen es Ihnen, die e-Mails ehemaliger Mitarbeiter beizubehalten, nachdem Sie Ihre Organisation verlassen haben. Ein Postfach wird inaktiv, wenn ein Rechtsstreit oder eine Office 365-Aufbewahrungsrichtlinie (im Office 365 &amp; Security Compliance Center) auf das Postfach angewendet wird, bevor das entsprechende Office 365-Benutzerkonto gelöscht wird. Die Inhalte eines inaktiven Postfachs werden für die Dauer des haltebereichs aufbewahrt, der für das Postfach gespeichert wurde, bevor es inaktiv wurde. Auf diese Weise können Administratoren, Compliance Officer und Datensatzverwalter die Inhaltssuche im Security &amp; Compliance Center verwenden, um die Inhalte eines inaktiven Postfachs zu durchsuchen und zu exportieren. InAktive Postfächer können keine e-Mails empfangen und werden nicht im freigegebenen Adressbuch Ihrer Organisation oder in anderen Listen angezeigt.
  
> [!NOTE]
> Wir haben den Stichtag (1. Juli 2017) zum Erstellen von neuem In-Situ-Speicher, um ein Postfach als inaktiv zu markieren, nach hinten verlegt. Ende dieses Jahres oder Anfang des nächsten Jahres können Sie keinen neuen In-Situ-Speicher in Exchange Online mehr erstellen. Es können dann nur noch das Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Vorhandene inaktive Postfächer, die sich im In-Situ-Speicher befinden, werden jedoch weiterhin unterstützt, und Sie können weiterhin die In-Situ-Speicher für inaktive Postfächer verwalten. Dazu zählen das Ändern der Dauer eines In-Situ-Speichers sowie das dauerhafte Löschen eines inaktiven Postfachs durch Entfernen des In-Situ-Speichers. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um ein Postfach als inaktiv festzulegen, muss ihm eine Exchange Online-Plan 2-Lizenz zugewiesen werden, damit für das Postfach vor dem Löschen ein Rechtsstreit oder eine Office 365-Aufbewahrungsrichtlinie angewendet werden kann. Exchange Online-Plan 2-Lizenzen sind Teil eines Office 365 Enterprise E3-und E5-Abonnements. Wenn einem Postfach eine Exchange Online-Plan 1-Lizenz zugewiesen ist (die Teil eines Office 365 Enterprise E1-Abonnements ist), müssen Sie ihm eine separate Exchange Online-Archivierungslizenz zuweisen, damit ein Aufbewahrungs Status auf das Postfach angewendet werden kann, bevor es gelöscht wird. Weitere Informationen finden Sie unter [Exchange Online-Archivierung](https://go.microsoft.com/fwlink/p/?LinkId=286153).
    
- Die dem gelöschten Exchange Online-Postfach zugeordnete Lizenz ist verfügbar, nachdem Sie das entsprechende Office 365-Benutzerkonto gelöscht haben. Sie können dann [Benutzern in Office 365 für Unternehmen Lizenzen zuweisen](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) . 
    
- Wenn vor dem Löschen des Postfachs für dieses kein Beweissicherungsverfahren aktiviert bzw. keine Office 365-Aufbewahrungsrichtlinie auf dieses angewendet wird, werden die Inhalte des Postfachs nicht beibehalten bzw. können diese nicht gefunden werden. Das gelöschte Postfach kann innerhalb von 30 Tagen nach dem Löschen wiederhergestellt werden; wird es nicht innerhalb von 30 Tagen wiederhergestellt, wird das Postfach samt Inhalten unwiderruflich gelöscht.
    
- Weitere Informationen zum Beweissicherungsverfahren finden Sie unter [In-Place Hold and Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=846124). Weitere Informationen zu Office 365-Aufbewahrungsrichtlinien im Security &amp; Compliance Center finden Sie unter [Übersicht über Aufbewahrungsrichtlinien in Office 365](retention-policies.md).
  
## <a name="create-an-inactive-mailbox"></a>Erstellen eines inaktiven Postfachs

Um ein Postfach inaktiv zu halten, müssen zwei Schritte ausgeführt werden: 1) Platzieren des Postfachs in der Rechtsstreitigkeit oder Anwenden einer Office 365-Aufbewahrungsrichtlinie auf diesen, und 2) Löschen des Postfachs oder des entsprechenden Office 365-Benutzerkontos. Nachdem das Postfach inaktiv ist, wird der Inhalt beibehalten, bis die Aufbewahrungsrichtlinie oder-Richtlinie entfernt wurde.
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-an-office-365-retention-policy"></a>Schritt 1: Aktivieren des Beweissicherungsverfahrens für das Postfach oder Anwenden einer Office 365-Aufbewahrungsrichtlinie auf das Postfach

Durch Aktivieren des Beweissicherungsverfahrens für ein Postfach oder Anwenden einer Office 365-Aufbewahrungsrichtlinie auf das Postfach werden alle Inhalte des Postfachs beibehalten, bevor es gelöscht wird. Bei beiden Verfahren bleiben sämtliche Postfachinhalte einschließlich gelöschter Elemente und Originalversionen geänderter Elemente erhalten. Gelöschte und geänderte Elemente verbleiben für einen bestimmten Zeitraum im inaktiven Postfach oder solange, bis das inaktive Postfach endgültig gelöscht wird, indem die Archivierung deaktiviert wird oder die auf das inaktive Postfach angewendete Aufbewahrungsrichtlinie entfernt wird.
  
Wenn bereits eine Archivierung für ein Postfach aktiviert ist oder wenn bereits eine Office 365-Aufbewahrungsrichtlinie darauf angewendet wurde, müssen Sie lediglich das entsprechende Office 365-Benutzerkonto löschen, wie in Schritt 2 erläutert.
  
Eine Schritt-für-Schritt-Anleitung zur Aktivierung des Beweissicherungsverfahrens für ein Postfach oder zur Anwendung einer Office 365-Aufbewahrungsrichtlinie finden Sie unter:
  
- [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [Übersicht über Aufbewahrungsrichtlinien in Office 365](retention-policies.md)
    
> [!NOTE]
> Für Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien können Sie das Postfach unbegrenzt lang oder zeitlich begrenzt archivieren. Bei einer dauerhaften Aufbewahrung werden die Inhalte des inaktiven Postfachs dauerhaft oder so lange beibehalten, bis die Aufbewahrung aufgehoben oder ihre Dauer geändert wird. Nachdem die Aufbewahrung beendet oder die Aufbewahrungsrichtlinie deaktiviert wurde (vorausgesetzt, das Postfach wurde vor mehr als 30 Tagen gelöscht), wird das inaktive Postfach für das endgültige Löschen markiert, und die Inhalte des Postfachs werden nicht aufbewahrt und können nicht gefunden werden. Bei einer zeitbasierten Aufbewahrung oder einer Office 365-Aufbewahrungsrichtlinie legen Sie die Dauer der Aufbewahrung fest. Diese Dauer wird pro Element festgelegt und wird von dem Datum ab berechnet, an dem ein Postfachelement empfangen oder erstellt wurde. Nachdem die Archivierung für ein Postfachelement abgelaufen ist und sich dieses Element im Ordner „Wiederherstellbare Elemente" im inaktiven Postfach befindet, wird das Element dauerhaft aus dem inaktiven Postfach gelöscht, nachdem die Aufbewahrungsdauer für das gelöschte Element abgelaufen ist. 
  
### <a name="step-2-delete-the-mailbox"></a>Schritt 2: Löschen des Postfachs

Nachdem das Postfach gehalten oder eine Office 365-Aufbewahrungsrichtlinie darauf angewendet wurde, besteht der nächste Schritt im Löschen des Postfachs. Die beste Möglichkeit zum Löschen eines Postfachs besteht darin, das entsprechende Office 365-Benutzerkonto im Office 365 Admin Center zu löschen. Informationen zum Löschen von Office 365-Benutzerkonten finden Sie unter [Löschen eines Benutzers aus Ihrer Organisation](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e).
  
> [!NOTE]
> Sie können das Postfach auch mithilfe des Cmdlets **Remove-Mailbox** in Exchange Online PowerShell löschen. Weitere Informationen finden Sie unter [Löschen oder Wiederherstellen von Benutzerpostfächern in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856287). 
  

## <a name="view-a-list-of-inactive-mailboxes"></a>Anzeigen einer Liste von inaktiven Postfächern


So zeigen Sie eine Liste der inaktiven Postfächer in Ihrer Organisation an
  
1. Wechseln Sie [https://protection.office.com/](https://protection.office.com/) zu, und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in ihrer Office 365-Organisation an. 
    
2. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Data Governance** \> * * Retention * *.
    
3. Klicken Sie auf der Seite **Aufbewahrung** auf **Weitere**![Ellipsen in](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif)der Navigationsleiste, und klicken Sie dann auf inaktive **Postfächer**.
    
    ![Klicken Sie auf der Seite Aufbewahrung auf mehr und dann auf inAktive Postfächer, um eine Liste der inaktiven Postfächer anzuzeigen.](media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    Die Seite inAktive **Postfächer** wird angezeigt. Hinweis Die Gesamtzahl der inaktiven Postfächer in Ihrer Organisation wird angezeigt. 
    
    ![Eine Liste aller inaktiven Postfächer in Ihrer Organisation wird angezeigt.](media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
Alternativ können Sie den folgenden Befehl in Exchange Online PowerShell ausführen, um die Liste der inaktiven Postfächer anzuzeigen.

```
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

Sie können auf ![Export Search results Icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Export** klicken, um eine CSV-Datei anzuzeigen oder herunterzuladen, die zusätzliche Informationen zu den inaktiven Postfächern in Ihrer Organisation enthält. 
  
Sie können den folgenden Befehl auch ausführen, um die Liste der inaktiven Postfächer und anderer Informationen in eine CSV-Datei zu exportieren. In diesem Beispiel wird die CSV-Datei im aktuellen Verzeichnis erstellt.

```
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```
   
> [!NOTE]
> Möglicherweise hat ein inaktives Postfach dieselbe SMTP-Adresse wie ein aktives Benutzerpostfach. In diesem Fall kann der Wert der **distinguishedName** -oder **ExchangeGuid** -Eigenschaft verwendet werden, um ein inaktives Postfach eindeutig zu identifizieren. 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a>Durchsuchen und Exportieren der Inhalte eines inaktiven Postfachs

Sie können auf die Inhalte des inaktiven Postfachs zugreifen, indem Sie das Tool für &amp; die Inhaltssuche im Security Compliance Center verwenden. Wenn Sie ein inaktives Postfach durchsuchen, können Sie eine Stichwort Suchabfrage erstellen, um nach bestimmten Elementen zu suchen, oder Sie können den gesamten Inhalt des inaktiven Postfachs zurückgeben. Sie können eine Vorschau der Suchergebnisse anzeigen oder die Suchergebnisse in eine Outlook-Datendatei (PST) oder als einzelne e-Mail-Nachrichten exportieren. Schrittweise Verfahren zum Durchsuchen von Postfächern und Exportieren von Suchergebnissen finden Sie in den folgenden Themen:
  
- [Inhaltssuche in Office 365](content-search.md)
    
- [Exportieren von Inhalts Suchergebnissen aus dem Office 365 &amp; Security Compliance Center](export-search-results.md)
    
Im folgenden finden Sie einige Punkte, die Sie beachten sollten, wenn Sie inaktive Postfächer durchsuchen.
  
- Wenn eine Inhaltssuche ein Benutzerpostfach enthält und das Postfach dann inaktiv ist, wird die Inhaltssuche weiterhin das inaktive Postfach durchsuchen, wenn Sie die Suche erneut ausführen, nachdem Sie inaktiv wurde.
    
- In einigen Fällen kann ein Benutzer über ein aktives Postfach und ein inaktives Postfach mit derselben SMTP-Adresse verfügen. In diesem Fall wird nur das bestimmte Postfach, das Sie als Speicherort für eine Inhaltssuche auswählen, durchsucht. Anders ausgedrückt: Wenn Sie ein Benutzerpostfach zu einer Suche hinzufügen, können Sie nicht davon ausgehen, dass sowohl Ihre aktiven als auch die inaktiven Postfächer durchsucht werden. nur das Postfach, das Sie der Suche explizit hinzufügen, wird durchsucht.
    
- Es wird dringend empfohlen, ein aktives Postfach und ein inaktives Postfach mit derselben SMTP-Adresse zu vermeiden. Wenn Sie die SMTP-Adresse, die derzeit einem inaktiven Postfach zugewiesen ist, wieder verwenden müssen, sollten Sie das inaktive Postfach wiederherstellen oder den Inhalt eines inaktiven Postfachs in einem aktiven Postfach (oder im Archiv eines aktiven Postfachs) wiederherstellen und dann den inaktives Postfach.
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a>Ändern der Aufbewahrungsdauer für ein inaktives Postfach

Nachdem ein Postfach deaktiviert wurde, können Sie die Dauer des haltebereichs oder die auf das inaktive Postfach angewendete Office 365-Aufbewahrungsrichtlinie ändern. Schrittweise Anleitungen finden Sie unter [Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
  
## <a name="recover-an-inactive-mailbox"></a>Wiederherstellen eines inaktiven Postfachs

Wenn ein ehemaliger Mitarbeiter an Ihre Organisation zurückkommt oder ein neuer Mitarbeiter zur Übernahme der Aufgaben des abberufenen Mitarbeiters angeheuert wird, können Sie die Inhalte des inaktiven Postfachs wiederherstellen. Wenn Sie ein inaktives Postfach wiederherstellen, wird das Postfach in ein neues Postfach konvertiert, die Inhalte und die Ordnerstruktur des inaktiven Postfachs werden beibehalten, und das Postfach ist mit einem neuen Benutzerkonto verknüpft. Nach der Wiederherstellung ist das inaktive Postfach nicht mehr vorhanden. Schrittweise Verfahren und weitere Informationen zu den Vorgängen beim Wiederherstellen eines inaktiven Postfachs finden Sie unter [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md).
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a>Wiederherstellen des Inhalts eines inaktiven Postfachs in einem anderen Postfach

Wenn ein anderer Mitarbeiter die Aufgaben eines ehemaligen Mitarbeiters übernimmt oder eine andere Person Zugriff auf die Inhalte des inaktiven Postfachs benötigt, können Sie den Inhalt des inaktiven Postfachs in einem vorhandenen Postfach wiederherstellen (oder zusammenführen). Wenn Sie ein inaktives Postfach wiederherstellen, wird der Inhalt in ein anderes Postfach kopiert. Das inaktive Postfach wird beibehalten und bleibt ein inaktives Postfach. Das inaktive Postfach kann weiterhin mithilfe von eDiscovery durchsucht werden, der Inhalt kann in einem anderen Postfach wiederhergestellt oder zu einem späteren Zeitpunkt wiederhergestellt oder gelöscht werden. Schrittweise Anleitungen finden Sie unter [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md).
  
## <a name="delete-an-inactive-mailbox"></a>Löschen eines inaktiven Postfachs

Wenn Sie den Inhalt eines inaktiven Postfachs nicht mehr aufbewahren müssen, können Sie das inaktive Postfach dauerhaft löschen, indem Sie die Aufbewahrungsrichtlinie für das inaktive Postfach entfernen oder die Office 365-Richtlinie entfernen. Wenn das Postfach vor mehr als 30 Tagen gelöscht wurde, wird das Postfach für eine dauerhafte Löschung gekennzeichnet, nachdem Sie den Haltestatus entfernt haben, und das Postfach kann nicht wiederhergestellt werden. Wenn das Postfach innerhalb der letzten 30 Tage gelöscht wurde, können Sie das Postfach nach dem Entfernen der halte-oder Aufbewahrungsrichtlinie wiederherstellen. Eine schrittweise Anleitung zum Entfernen eines haltebereichs oder einer Office 365-Aufbewahrungsrichtlinie zum endgültigen Löschen eines inaktiven Postfachs finden Sie unter [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md).