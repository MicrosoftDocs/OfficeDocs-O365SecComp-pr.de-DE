---
title: Office 365 Exchange Online-Daten löschen
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Weiche und der schwerer Daten Löschvorgänge in Exchange Online behandelt werden.
ms.openlocfilehash: 3a17b09e9c21ae309e00bcb0ddc0b51b93478bc1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529302"
---
# <a name="exchange-online-data-deletion-in-office-365"></a>Exchange Online-Daten löschen in Office 365
In Exchange Online, es gibt zwei Arten von Löschvorgängen: Weiche Löschvorgänge und schwer Löschvorgänge. Dies gilt für Postfächer und Elemente in einem Postfach.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Vorläufig gelöschten und schwer gelöschte Postfächer
Ein vorläufig gelöschten Benutzerpostfach ist ein Postfach, das mit Office 365 Administrationscenter oder das Cmdlet Remove-Mailbox gelöscht wurde und wurde noch im Papierkorb Azure Active Directory für weniger als 30 Tage. Ein Postfach kann in einer der folgenden Methoden vorläufig gelöschten werden:
- Das Postfach des Benutzers zugeordnete Azure Active Directory-Benutzerkonto ist vorläufig gelöschten (das Benutzerobjekt ist außerhalb des Gültigkeitsbereichs oder im Container Recycle Bin).
- Das Benutzerpostfach zugeordneten Azure Active Directory-Benutzerkonto wurde Festplatte gelöscht, aber das Exchange Online-Postfach befindet sich unter eine Aufbewahrung für eventuelle Rechtsstreitigkeiten oder eDiscovery halten.
- Des Benutzerpostfachs ein zugeordnetes Azure Active Directory-Benutzerkonto in den letzten 30 Tagen geleert wurde. Das ist die maximale Beibehaltungsdauer Länge Exchange Online wird das Postfach in einem vorläufig gelöschten Status beibehalten, bevor sie endgültig gelöscht und können nicht wiederhergestellt werden kann.

Einer harte gelöscht Benutzerpostfach ist ein Postfach, das in einem der folgenden Arten gelöscht wurde:
- Das Benutzerpostfach wurde vorläufig gelöschten für mehr als 30 Tage, und der zugeordnete Azure Active Directory-Benutzer wurde Festplatte gelöscht. Gesamten Inhalt des Postfachs wie e-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Das Benutzerkonto, das Benutzerpostfach zugeordnet wurde aus dem Azure Active Directory Festplatte gelöscht. Das Benutzerpostfach ist nun vorläufig gelöschten in Exchange Online und für 30 Tage in einem vorläufig gelöschten Status bleibt. In der 30-Tage-Zeitraum in ein neuer Azure Active Directory-Benutzer aus dem ursprünglichen Empfänger Konto mit dem gleichen **ExchangeGuid** oder **ArchiveGuid**synchronisiert ist, und neues Konto für den Exchange Online lizenziert ist, wird in einer harte Löschung von erstellt das ursprüngliche Benutzerpostfach. Gesamten Inhalt des Postfachs wie e-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Ein vorläufig gelöschten Postfach wird mit **Remove-Mailbox-PermanentlyDelete**gelöscht.

Die oben genannten löschen Szenarios wird vorausgesetzt, dass nicht das Postfach des Benutzers in einem der Zustände halten wie Aufbewahrung für eventuelle Rechtsstreitigkeiten oder eDiscovery halten. Wenn eine Art von Haltestatus für das Postfach vorhanden ist, kann nicht das Postfach gelöscht. Für alle e-Mail-Benutzer-Empfängertypen [halten](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) Einstellungen werden ignoriert und haben keinen Einfluss auf die Festplatte Löschvorgänge oder vorläufig Löschvorgänge.

## <a name="soft-deleted-and-hard-deleted-items"></a>Vorläufig gelöschten und schwer gelöschte Elemente
Wenn ein Benutzer ein Postfach-Element (beispielsweise eine e-Mail-Nachricht, einen Kontakt, eines Kalendertermins oder eine Aufgabe) löscht, wird das Element in den Ordner wiederherstellbare Elemente, und klicken Sie in einem Unterordner mit dem Namen Löschvorgänge verschoben. Dies wird als soft Löschvorgang bezeichnet. Wie lange gelöschte Elemente werden in der Löschvorgang Ordner hängt die Aufbewahrungszeit für gelöschte Elemente, die für das Postfach festgelegt wird gespeichert. Exchange Online-Postfach behält gelöschte Elemente für 14 Tage standardmäßig, aber Exchange Online-Administratoren können diese Einstellung erhöhen den Zeitraum bis maximal 30 Tage zu ändern. (Ausführliche Schritte zum Erhöhen der Aufbewahrungszeit für ein Exchange Online-Postfach, finden Sie unter [ändern wie lange dauerhaft gelöscht Elemente für ein Exchange Online-Postfach geführt werden](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention).) Benutzer können wiederherstellen oder löschen, Gelöschte Objekte vor Ablauf die Aufbewahrungszeit für ein gelöschtes Element. Dazu verwenden sie das Feature gelöschte Elemente wiederherstellen in Microsoft Outlook oder Outlook im Web.

Wenn ein Benutzer mit dem Feature gelöschte Elemente wiederherstellen in Outlook oder Outlook im Web ein gelöschtes Element löscht, wird diese als Löschen einer harte bezeichnet. In Exchange Online ist Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn ein neues Postfach erstellt wird, damit ein Administrator kann weiterhin schwer gelöschte Elemente [Wiederherstellen](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/recover-deleted-messages) vor Ablauf die Aufbewahrungszeit für gelöschte. Auch wenn eine Nachricht von einem Benutzer oder Prozess geändert wird, werden Kopien des ursprünglichen Elements auch beibehalten, wenn Wiederherstellung einzelner Elemente aktiviert ist.

## <a name="page-zeroing"></a>Unwiderrufliches Löschen
*Zeroing* ist ein Sicherheitsmechanismus, der Nullen oder ein binäres Muster über gelöschten Daten schreibt, sodass die gelöschten Daten schwieriger wiederhergestellt werden. In Exchange Online Postfachdatenbanken *Seiten* als die Maßeinheit Speicher, und Implementieren einer überschreiben genanntes *Unwiderrufliches Löschen*. Unwiderrufliches Löschen ist standardmäßig aktiviert und kann nicht deaktiviert werden, von Kunden oder von Microsoft. Seite unwiderruflichen Vorgänge werden in die Transaktionsprotokolldateien aufgezeichnet, sodass alle Kopien einer bestimmten Datenbank Seite-auf ähnliche Weise unwiderruflich gelöscht werden. Unwiderrufliches Löschen einer Seite auf eine Kopie der aktiven Datenbank bewirkt, dass die Seite auf passiven Kopien der Datenbank unwiderruflich gelöscht abrufen.

Unwiderrufliches Löschen ein binäres Muster über Festplatte gelöschte Datensätze geschrieben. Das Muster Unwiderrufliches speziell für Extensible Storage Engine (ESE) (der Name der internen Datenbank-Engine verwendete Vorgänge von Servern in Exchange Online) ist, und es ist für laufzeitvorgänge im Vergleich zu Hintergrund datenbankwartungsvorgänge unterschiedlich. (Datenbankwartung im Hintergrund ist ein Prozess, der kontinuierlich Prüfsumme und Überprüfungen jeder Datenbank. Ihre primäre Funktion besteht darin Prüfsumme Datenbankseiten, aber es behandelt auch Speicherplatz bereinigen und unwiderrufliches Löschen der Datensätze und Seiten, die nicht aufgrund einer Store Absturz gelöscht wurden.)

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


### <a name="page-zeroing-process"></a>Unwiderrufliches Löschen der Seite-Prozess
Der Prozess für Unwiderrufliches hängt das Szenario löschen. Die folgende Tabelle beschreibt die Datenbank löschen-Szenarien und beim Auftreten von Seite unwiderruflichen Funktionen.

| Datenbanklöschszenario | ESE-Vorgang und -Zeitrahmen für unwiderrufliches Löschen von Datenbankdaten |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Element läuft basierend auf die Aufbewahrungszeit für gelöschte Elemente ab. | Ein asynchroner Thread schreibt ein binäres Muster über die gelöschten Daten. Diese Aktion wird innerhalb von Millisekunden nach dem Datensatzlöschvorgang ausgeführt. Wenn der Informationsspeicherprozess abstürzt, während das asynchrone unwiderrufliche Löschen noch nicht erledigt ist (oder das Bereinigen des Versionsspeichers wegen dessen Vergrößerung abgebrochen wurde), wird das unwiderrufliche Löschen ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |
| Szenario für Ansicht: Ablauf von Elementen aus Outlook/Outlook auf dem Web-Ordneransicht (beispielsweise Unterhaltungsansicht) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |
| Verschieben/löschen Postfach Szenario: Das Quellpostfach gelöscht (Ablauf des gelöschten Postfachs) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Postfachdatentypen ohne unwiderrufliches Löschen
Die folgenden postfachdatentypen keine Regelungen für Unwiderrufliches Löschen:
- **Transaktionsprotokolle einer Postfachdatenbank** - wenn Transaktionsprotokolle als Teil des normalen Betriebs gelöscht werden, es werden keine Blöcke im Dateisystem 0 (null), die die gelöschten Log-Dateien gespeichert. Es ist wahrscheinlich, dass im Dateisystem schnell erneut, freien Speicherplatz für die neu erstellten Protokolle verwenden, aber es ist nicht gewährleistet, dass dies der Fall sein wird.
- **Inhaltsindex-Katalogdateien** - Exchange Online verwendet Search Foundation (auch bekannt als FAST) für die Suche Indizierung Funktionalität. Suchkatalog Index besteht aus mehreren Dutzend Dateien auf dem gleichen Volume wie die Postfach-Datenbankdatei gespeichert. Wenn eine Nachricht aus der Postfachdatenbank Festplatte gelöscht wird, ist nicht der zugeordnete Inhalt in der Suchkatalog sofort gelöscht. Content Löschvorgang tritt auf, wenn Search Foundation hat einen Schatten (oder hauptzusammenführung) von viele kleine Katalogdateien in in einer einzelnen Datei größer. Nach Abschluss der hauptzusammenführung werden die kleineren Katalogdateien gelöscht. Es werden keine Blöcke NULL, die gelöschten Katalogdateien gespeichert.

## <a name="continuous-replication"></a>Fortlaufende Replikation
Fortlaufende Replikation (auch bekannt als Protokollversand und Replay) ist-Technologie im Exchange-Online, die erstellt und verwaltet von Datenbankkopien jedes Postfach für hohe Verfügbarkeit und ausfallsicherheit von Standorten Disaster Recovery bereitzustellen. Fortlaufende Replikation nutzt Exchange Server-Datenbank Absturz Wiederherstellung Support für die Technologie bereitstellen ausführt, asynchrone Aktualisierung der einen oder mehrere Kopien der Postfachdatenbank an. Jeder Postfachserver zeichnet Datenbank Aktualisierungen in einer aktiven Datenbank (beispielsweise Benutzeraktivität e-Mail) als Protokolleinträge in eine sequenzielle Reihe von Transaktionsprotokolldateien 1 MB. Diese Gruppe von Dateien ist als die Protokollstream bezeichnet. Fortlaufende Replikation wird der Protokollstream auch asynchron eine oder mehrere Kopien einer Datenbank zu aktualisieren. Dies geschieht durch übertragen die Protokolle an einen Speicherort, enthält eine passive Kopie der aktiven Datenbank und klicken Sie dann in die passive Datenbankkopie Wiedergeben dieser. Wenn alle Protokolle aus der aktiven Datenbank gegen eine passive Kopie der Datenbank wiedergegeben werden, klicken Sie dann die beiden Datenbanken sind gleichwertig und durch diesen Vorgang ist, dass jede physische Änderung an einer aktiven Datenbank auf alle passiven Kopien der Datenbank repliziert wird.

Alle löschen aus einer Postfachdatenbank darstellt, ob ein Element Postfach oder ein gesamtes Postfach und, ob ein Soft-Delete oder einer harte-Delete, eine physische Änderung auf die aktive Datenbank. Unwiderrufliches Löschen auch umfasst physische Änderungen auf die aktive Datenbank vornehmen. Diese Änderungen in die fortlaufende Replikation so genannten Protokolldateien geschrieben werden, und die Protokolldateien gegen passiven Kopien der Datenbank wiedergegeben werden, werden die gleichen physischen Änderungen auf diese passiven Datenbanken vorgenommen.