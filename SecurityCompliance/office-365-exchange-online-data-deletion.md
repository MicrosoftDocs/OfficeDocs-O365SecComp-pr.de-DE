---
title: Office 365 Exchange Online-Datenlöschung
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Wie weiche und harte Datenlöschungen in Exchange Online verarbeitet werden.
ms.openlocfilehash: 977beb41469e0015e22aea6750cfd657d9ee3b39
ms.sourcegitcommit: 1261a37c414111f869df5791548a768d853fda60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2019
ms.locfileid: "31004192"
---
# <a name="exchange-online-data-deletion-in-office-365"></a>Löschen von Exchange Online-Daten in Office 365
In Exchange Online gibt es zwei Arten von Löschungen: weiche Löschvorgänge und harte Löschvorgänge. Dies gilt für Postfächer und Elemente innerhalb eines Postfachs.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Weiche und gelöschte Postfächer
Ein Soft-Deleted-Benutzerpostfach ist ein Postfach, das mit dem Microsoft 365 Admin Center oder dem Cmdlet Remove-Mailbox gelöscht wurde und sich noch weniger als 30 Tage im Azure Active Directory-Papierkorb befindet. Ein Postfach kann auf eine der folgenden Arten als "Soft-Deleted" werden:
- Das zugeordnete Azure Active Directory-Benutzerkonto des Benutzerpostfachs ist Soft-deleted (das Benutzerobjekt befindet sich außerhalb des Bereichs oder im Papierkorb Container).
- Das zugeordnete Azure Active Directory-Benutzerkonto des Benutzerpostfachs wurde schwer gelöscht, aber das Exchange Online-Postfach befindet sich in einem Rechtsstreit oder einer eDiscovery-Aufbewahrung.
- Das zugeordnete Azure Active Directory-Benutzerkonto des Benutzerpostfachs wurde innerhalb der letzten 30 Tage bereinigt; bei der es sich um die maximale Aufbewahrungsdauer handelt, wird das Postfach von Exchange Online vor dem endgültigen Löschen und nicht behebbaren Zustand beibehalten.

Bei einem festgestellten Benutzerpostfach handelt es sich um ein Postfach, das auf eine der folgenden Arten gelöscht wurde:
- Das Benutzerpostfach wurde für mehr als 30 Tage weich gelöscht, und der zugehörige Azure Active Directory-Benutzer wurde schwer gelöscht. Alle Postfachinhalte wie e-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Das mit dem Benutzerpostfach verknüpfte Benutzerkonto wurde aus dem Azure Active Directory schwer gelöscht. Das Benutzerpostfach ist jetzt in Exchange Online deaktiviert und bleibt 30 Tage lang in einem weichen gelöscht. Wenn in einem Zeitraum von 30 Tagen ein neuer Azure Active Directory-Benutzer vom ursprünglichen Empfängerkonto mit demselben **ExchangeGuid** oder **ArchiveGuid**synchronisiert wird und dieses neue Konto für Exchange Online lizenziert wird, führt dies zu einem harten Löschen von das ursprüngliche Benutzerpostfach. Alle Postfachinhalte wie e-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Ein nicht gelöschtes Postfach wird mithilfe von **Remove-Mailbox-PermanentlyDelete**gelöscht.

Bei den obigen Lösch Szenarien wird davon ausgegangen, dass sich das Benutzerpostfach nicht in einem der Aufbewahrungs Status befindet, wie beispielsweise Rechtsstreit oder eDiscovery-Speicher. Wenn ein Aufbewahrungs für das Postfach vorhanden ist, kann das Postfach nicht gelöscht werden. Für alle e-Mail-Benutzer Empfängertypen [](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) werden alle Aufbewahrungseinstellungen ignoriert und haben keine Auswirkungen auf Hard-und Löschvorgänge.

## <a name="soft-deleted-and-hard-deleted-items"></a>Weiche gelöschte und fest gelöschte Elemente
Wenn ein Benutzer ein Postfachelement (beispielsweise eine e-Mail-Nachricht, einen Kontakt, einen Kalendertermin oder eine Aufgabe) löscht, wird das Element in den Ordner "Wiederherstellbare Elemente" und in einen Unterordner mit dem Namen "Löschungen" verschoben. Dies wird als weiche Löschung bezeichnet. Die Aufbewahrungsdauer für gelöschte Elemente im Ordner Löschvorgänge hängt von der Aufbewahrungsdauer für gelöschte Elemente ab, die für das Postfach festgelegt ist. Ein Exchange Online-Postfach hält gelöschte Elemente standardmäßig 14 Tage lang, aber Exchange Online-Administratoren können diese Einstellung ändern, um den Zeitraum auf maximal 30 Tage zu verlängern. (Ausführliche Schritte zum Verlängern des Aufbewahrungszeitraums für gelöschte Elemente für ein Exchange Online-Postfach finden Sie unter [ändern, wie lange dauerhaft gelöschte Elemente für ein Exchange Online-Postfach aufbewahrt werden](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention).) Benutzer können gelöschte Elemente wiederherstellen oder löschen, bevor die Aufbewahrungszeit für ein gelöschtes Element abläuft. Zu diesem Zweck verwenden Sie die Funktion "Gelöschte Elemente wiederherstellen" in Microsoft Outlook oder Outlook im Web.

Wenn ein Benutzer ein gelöschtes Element mithilfe des Features "Gelöschte Elemente wiederherstellen" in Outlook oder Outlook im Web löscht, wird dies als harte Löschung bezeichnet. In Exchange Online ist die Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn ein neues Postfach erstellt wird, sodass ein Administrator die festgestellten Elemente [Wiederherstellen](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/recover-deleted-messages) kann, bevor der Aufbewahrungszeitraum für gelöschte Elemente abgelaufen ist. Zudem werden Kopien des ursprünglichen Elements, wenn die Wiederherstellung einzelner Elemente aktiviert ist, beibehalten, sofern die Nachricht durch einen Benutzer oder Prozess geändert wird.

## <a name="page-zeroing"></a>Unwiderrufliches Löschen
** Bei Nullen handelt es sich um einen Sicherheitsmechanismus, der Nullen oder ein binäres Muster über gelöschte Daten schreibt, sodass die Wiederherstellung der gelöschten Daten schwieriger ist. In Exchange Online verwenden Postfachdatenbanken *Seiten* als Speichereinheit und implementieren einen überschreibenden Prozess, der mit dem Namen *Page Zeroing*ausgeführt wird. Das unwiderrufliche Löschen von Seiten ist standardmäßig aktiviert und kann nicht von Kunden oder von Microsoft deaktiviert werden. Die Vorgänge für die Seiten rücknullen werden in den Transaktionsprotokolldateien aufgezeichnet, sodass alle Kopien einer bestimmten Datenbank auf ähnliche Weise auf die Seite gesetzt werden. Wenn Sie eine Seite in einer aktiven Datenbankkopie aufNullieren, wird die Seite für passive Kopien der Datenbank auf NULL gesetzt.

Bei der Nullung von Seiten wird ein binäres Muster über fest gelöschte Datensätze geschrieben. Das Muster für die Seiten NULL ist spezifisch für ESE-Vorgänge (Extensible Storage Engine) (der Name des internen Datenbankmoduls, das von Servern in Exchange Online verwendet wird), und es unterscheidet sich für Laufzeitvorgänge im Vergleich zu Daten Bank Wartungsvorgängen. (Die Hintergrunddaten Bank Wartung ist ein Prozess, bei dem die einzelnen Datenbanken kontinuierlich überprüft und gescannt werden. Die primäre Funktion besteht darin, Datenbankseiten zu überprüfende, aber es behandelt auch das Bereinigen von Speicherplatz und das Löschen von Datensätzen und Seiten, die aufgrund eines Speicher Absturzes nicht gelöscht wurden.)

In der folgenden Tabelle sind die Füllmuster zusammengestellt, die für die speziellen Laufzeitvorgänge verwendet werden.

| ESE-Laufzeitvorgang   | Füllmuster |
|--------------------------|--------------|
| Ersetzen                  | R            |
| Datensatz/Long-Wert löschen | D            |
| Freigegebener Seitenspeicherplatz         | H            |


In der folgenden Tabelle sind die Füllmuster zusammengestellt, die den speziellen Vorgängen entsprechen, die bei der Hintergrundwartung einer ESE-Datenbank ausgeführt werden.

| Hintergrundwartungsvorgang für ESE-Datenbank | Füllmuster |
|-----------------------------------------------|--------------|
| Datensatz löschen                                 | D            |
| Long-Wert löschen                             | L            |
| Freigegebener Seitenspeicherplatz einer teilweise verwendeten Seite       | Z            |
| Freigegebener Seitenspeicherplatz einer nicht verwendeten Seite               | U            |


### <a name="page-zeroing-process"></a>Prozess zum Löschen von Seiten
Das Verfahren für das Löschen von Seiten hängt vom Lösch Szenario ab. In der folgenden Tabelle ist für verschiedene Datenbanklöschszenarien erläutert, wann Funktionen zum unwiderruflichen Löschen ausgeführt werden.

| Datenbanklöschszenario | ESE-Vorgang und -Zeitrahmen für unwiderrufliches Löschen von Datenbankdaten |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Das Element läuft basierend auf dem Aufbewahrungszeitraum für gelöschte Elemente ab. | Ein asynchroner Thread schreibt ein binäres Muster über die gelöschten Daten. Diese Aktion wird innerhalb von Millisekunden nach dem Datensatzlöschvorgang ausgeführt. Wenn der Informationsspeicherprozess abstürzt, während das asynchrone unwiderrufliche Löschen noch nicht erledigt ist (oder das Bereinigen des Versionsspeichers wegen dessen Vergrößerung abgebrochen wurde), wird das unwiderrufliche Löschen ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |
| Szenario anzeigen: Ablauf von Elementen aus Outlook/Outlook in der Webordneransicht (beispielsweise Unterhaltungsansicht) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |
| Postfach verschieben/Postfach löschen: Quellpostfach gelöscht (Ablauf des gelöschten Postfachs) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Postfachdatentypen ohne unwiderrufliches Löschen
Die folgenden Post Fach Datentypen enthalten keine Bestimmungen für das unwiderrufliche Löschen von Seiten:
- **Transaktionsprotokolle der Postfachdatenbank** -wenn Transaktionsprotokolle im Rahmen normaler Vorgänge gelöscht werden, gibt es keinen Prozess, um die Blöcke im Dateisystem, die die gelöschten Protokolldateien gespeichert haben, auf NULL zu setzen. Es ist wahrscheinlich, dass das Dateisystem diesen freien Speicherplatz für neu erstellte Protokolle schnell wieder verwendet, aber es gibt keine Garantie dafür.
- **Inhaltsindex-Katalogdateien** – Exchange Online verwendet Search Foundation (auch bekannt als fast) für die Such Indizierungsfunktionalität. Der Suchindexkatalog besteht aus mehreren Dutzend Dateien, die auf demselben Volume wie die Postfachdatenbankdatei gespeichert sind. Wenn eine Nachricht aus der Postfachdatenbank gelöscht wird, wird der zugehörige Inhalt im Suchkatalog nicht sofort gelöscht. Das Löschen von Inhalten tritt auf, wenn die Such Foundation eine Shadow-(oder Master-Zusammenführung) vieler kleiner Katalogdateien in einer einzelnen größeren Datei ausführt. Nach Abschluss des Master Zusammenführungsvorgangs werden die kleineren Katalogdateien gelöscht. Die Blöcke, die die gelöschten Katalogdateien gespeichert haben, können nicht zurückgesetzt werden.

## <a name="continuous-replication"></a>Fortlaufende Replikation
Bei der fortlaufenden Replikation (auch Protokollversand und-Wiedergabe genannt) handelt es sich um Technologie in Exchange Online, die Kopien jeder Postfachdatenbank erstellt und verwaltet, um hohe Verfügbarkeit, Ausfallsicherheit von Standorten und Notfallwiederherstellung zu gewährleisten. Die fortlaufende Replikation nutzt die Unterstützung der Exchange Server-Datenbankabsturz Wiederherstellung, um Technologie bereitzustellen, die eine asynchrone Aktualisierung einer oder mehrerer Kopien einer Postfachdatenbank ermöglicht. Jeder Postfachserver zeichnet Datenbankaktualisierungen für eine aktive Datenbank (beispielsweise e-Mail-Aktivität der Benutzer) als Protokolldatensätze in einem sequenziellen Satz von 1 MB-Transaktionsprotokolldateien auf. Dieser Satz von Dateien wird als Protokolldatenstrom bezeichnet. Bei der fortlaufenden Replikation wird der Protokolldatenstrom auch verwendet, um eine oder mehrere Kopien einer Datenbank asynchron zu aktualisieren. Dies wird erreicht, indem die Protokolle an einen Speicherort übertragen werden, der eine passive Kopie der aktiven Datenbank enthält, und diese dann in der passiven Datenbankkopie wiedergegeben wird. Wenn alle Protokolle aus der aktiven Datenbank für eine passive Kopie der Datenbank wiedergegeben werden, sind die beiden Datenbanken äquivalent, und durch diesen Vorgang wird jede physische Änderung an einer aktiven Datenbank auf alle passiven Kopien dieser Datenbank repliziert.

Jeder Löschvorgang aus einer Postfachdatenbank, unabhängig davon, ob es sich um ein Postfachelement oder ein vollständiges Postfach handelt, und ob es sich um eine Soft-Delete-oder eine Hard-Delete-Aktion handelt, stellt eine physikalische Änderung der aktiven Datenbank Das unwiderrufliche Löschen von Seiten umfasst auch physische Änderungen an der aktiven Datenbank. Diese Änderungen werden in die Protokolldateien über einen Prozess namens fortlaufende Replikation geschrieben, und wenn diese Protokolldateien für passive Kopien der Datenbank wiedergegeben werden, werden dieselben physischen Änderungen an diesen passiven Datenbanken vorgenommen.