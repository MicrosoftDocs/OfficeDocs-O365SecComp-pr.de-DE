---
title: Übersicht über inaktiver Postfächer in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/1/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1fbd74e8-7a60-4157-afe8-fe79f05d2038
description: Informationen Sie zu aufbewahren von Inhalt von Postfächern für frühere Mitarbeiter durch das Postfach in eines inaktiven Postfachs aus-oder einschalten. Hierzu können Sie das Postfach für die Aufbewahrung für eventuelle Rechtsstreitigkeiten Vermarktung oder Anwenden einer Aufbewahrungsrichtlinie für Office 365 auf das Postfach und dann das entsprechende Office 365-Konto zu entfernen.
ms.openlocfilehash: 5b421e32df99a10d13528fe7a75e6a0e8fb54fdc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529522"
---
# <a name="overview-of-inactive-mailboxes-in-office-365"></a>Übersicht über inaktiver Postfächer in Office 365

Möglicherweise müssen Sie die frühere Mitarbeiter e-Mail beibehalten, wenn die Organisation verlassen. Je nach den Anforderungen der Organisation Aufbewahrung müssen Sie möglicherweise Inhalt von Postfächern für einige Monate oder Jahre nach Beschäftigung endet, oder Sie Inhalt von Postfächern auf unbestimmte Zeit aufbewahren müssen möglicherweise beibehalten. Unabhängig davon, wie lange Sie e-Mail beibehalten werden müssen können Sie inaktiver Postfächer in Office 365, die beibehalten werden das Postfach von frühere Mitarbeiter erstellen. 
  
## <a name="what-are-inactive-mailboxes"></a>Was sind inaktive Postfächer?

Wenn ein Mitarbeiter Ihre Organisation verlässt (oder in einer erweiterten Abwesenheit geht), können Sie ihre Office 365-Konto entfernen. Postfachdaten des Mitarbeiters werden beibehalten, 30 Tage nach das Konto entfernt wird. In diesem Zeitraum können Sie die Postfachdaten wiederherstellen, indem das Konto löschen. Nach 30 Tagen werden die Daten dauerhaft entfernt.
  
Aber wenn Ihre Organisation benötigt, die für frühere Mitarbeiter Postfachinhalt beibehalten werden, können Sie das Postfach in eines inaktiven Postfachs aktivieren, indem das Postfach für die Aufbewahrung für eventuelle Rechtsstreitigkeiten Vermarktung oder Anwenden einer Aufbewahrungsrichtlinie für Office 365 auf das Postfach in die Office 365-Sicherheit &amp; Compliance Center und dann das entsprechende Office 365-Konto zu entfernen. Der Inhalt eines inaktiven Postfachs werden beibehalten, für die Dauer des Beweissicherungsverfahrens, der auf das Postfach oder die Aufbewahrungszeit der Office 365 Aufbewahrungsrichtlinie angewendet werden, vor dem Löschen des Postfachs platziert. Sie können das entsprechende Benutzerkonto für einen Zeitraum von 30 Tagen wiederherstellen. Jedoch ist nach 30 Tagen inaktive Postfach in Office 365 beibehalten, bis die Richtlinie halten oder die Aufbewahrung entfernt wird. 
  
**Wichtig:** Wir haben den 1 Juli 2017 Stichtag zum Erstellen von neuen, Compliance-Archive, um ein Postfach deaktivieren, verschoben. Aber weiter unten in diesem Jahr oder frühe nächste Jahr, nicht möglich, neue Compliance-Archive in Exchange Online erstellen. Zu diesem Zeitpunkt können nur Rechtsstreitigkeiten enthält und Office 365 Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Allerdings vorhandenen inaktiver Postfächer, die Compliance-Archiv sind zwar unterstützt, und Sie können auch weiterhin die Compliance-Archive für inaktive Postfächer verwalten. Dazu gehören Ändern der Dauer von einer In-Place Hold und endgültiges Löschen eines inaktiven Postfachs durch Entfernen der In-Place Hold. 
 
  
## <a name="inactive-mailboxes-and-office-365-retention-policies"></a>Inaktive Postfächer und Office 365-Aufbewahrungsrichtlinien

Neben dem Beweissicherungsverfahren ist das neue Feature der Office 365-Aufbewahrungsrichtlinien im Security &amp; Compliance Center eine weitere Möglichkeit, ein Postfach als inaktiv festzulegen. Um ein Postfach mithilfe einer Aufbewahrungsrichtlinie als inaktiv festzulegen, müssen Sie wie folgt vorgehen: 
  
- Die Richtlinie muss auf Exchange-Postfächer oder Skype for Business-Speicherorte angewendet werden (da Skype-bezogene Inhalte im Postfach des Benutzers gespeichert werden). 
    
- Sie muss so konfiguriert werden, dass Inhalte aufbewahrt oder aufbewahrt und anschließend gelöscht werden. Wenn eine Aufbewahrungsrichtlinie so konfiguriert ist, dass Inhalte lediglich gelöscht werden, wird ein Postfach, auf das die Richtlinie angewendet wurde, beim Löschen des Postfachs nicht inaktiv.
    
- Sie kann abfragebasiert sein, sodass nur Elemente aufbewahrt werden, die einer Suchabfrage entsprechen. 
    
Weitere Informationen zum Konfigurieren von Office 365-Aufbewahrungsrichtlinien finden Sie unter [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md).
  
Bei Verwendung einer Office 365-Aufbewahrungsrichtlinie zum Festlegen eines Postfachs als inaktiv wird die Aufbewahrungsrichtlinie weiterhin von Office 365 auf das inaktive Postfach angewendet. Dies bedeutet Folgendes: Wenn die Aufbewahrungsrichtlinie so konfiguriert ist, das Inhalte aufbewahrt und anschließend gelöscht werden, werden Elemente in den Ordner „Wiederherstellbare Elemente" verschoben, wenn die Aufbewahrungsdauer abläuft, und schließlich aus dem inaktiven Postfach gelöscht. Wenn die Office 365-Aufbewahrungsrichtlinie nicht so konfiguriert ist, das Elemente gelöscht werden, werden Elemente, die vom Benutzer nicht endgültig gelöscht wurden (bevor das Postfach als inaktiv festgelegt wurde), nicht in den „Wiederherstellbare Elemente" verschoben, sondern unbegrenzt aufbewahrt, nachdem das Postfach als inaktiv festgelegt wurde. 
  
Sie können auch eine Office 365-Aufbewahrungsrichtlinie speziell für inaktive Postfächer erstellen. Hier sind einige Gründe dafür und Punkte, die Sie beachten sollten.
  
- Sie können die Aufbewahrungsrichtlinie so konfigurieren, dass Postfachinhalte nur so lange aufbewahrt werden, wie erforderlich ist, um die Anforderungen Ihrer Organisation in Bezug auf ehemalige Mitarbeiter zu erfüllen.
    
- Es ist eine einfache Möglichkeit zum inaktiver Postfächer zu identifizieren, da die Aufbewahrungsrichtlinie auf inaktiver Postfächer nur angewendet wird.
    
- Sie werden möglicherweise von auf einfache Weise die Aufbewahrungsrichtlinie zu identifizieren, die inaktiver Postfächer in Ihrer Organisation zugewiesen ist. Dadurch wird die Aufbewahrungsrichtlinie (oder löschen) bei Bedarf ändern erleichtern. Es wird auch erleichtern endgültig löschen ein inaktives Postfachs, da Sie nur es aus der Richtlinie entfernen können mithilfe der Sicherheits &amp; Compliance Center. Andernfalls müssen Sie mithilfe von Exchange Online PowerShell eines inaktiven Postfachs daraus eine Aufbewahrung für eventuelle Rechtsstreitigkeiten oder verwenden Sie die Sicherheit &amp; Compliance Center PowerShell ein inaktives Postfachs aus einer Organisation geltende Office 365-Aufbewahrungsrichtlinie ausschließen.
    
- Wenn Sie eine Office 365-Aufbewahrungsrichtlinie speziell für inaktive Postfächer erstellen, können Sie der Richtlinie maximal 1.000 Postfächer hinzufügen. In einer sehr großen Organisation müssen Sie möglicherweise mehrere Office 365-Aufbewahrungsrichtlinien für inaktive Postfächer erstellen.
  
## <a name="inactive-mailboxes-and-ediscovery-case-holds"></a>Inaktive Postfächer und eDiscovery-Fallspeicher

Wenn ein Speicherverfahren, das einem eDiscovery-Fall im Security &amp; Compliance Center zugeordnet ist, auf ein Postfach angewendet wird und anschließend das Postfach oder das Office 365-Konto des Benutzers gelöscht wird, wird das Postfach zu einem inaktiven Postfach. Die Verwendung von eDiscovery-Fallspeichern zum Festlegen eines Postfachs als inaktiv wird jedoch nicht empfohlen. Grund hierfür ist, dass eDiscovery-Fälle für bestimmte zeitgebundene Fälle im Zusammenhang mit einem rechtlichen Problem vorgesehen sind. An einem bestimmten Punkt wird ein Rechtsfall wahrscheinlich enden, die dem Fall zugeordneten Speicherverfahren werden entfernt, und der eDiscovery-Fall wird geschlossen. Wenn ein für ein inaktives Postfach festgelegtes Speicherverfahren einem eDiscovery-Fall zugeordnet ist und das Speicherverfahren anschließend aufgehoben oder der eDiscovery-Fall geschlossen (oder gelöscht) wird, wird das inaktive Postfach endgültig gelöscht. Außerdem können Sie keinen zeitbasierten eDiscovery-Fallspeicher erstellen. Dies bedeutet, dass der Inhalt eines inaktiven Postfachs für immer aufbewahrt wird oder bis das Speicherverfahren aufgehoben und das inaktive Postfach gelöscht wird. Daher empfehlen wir die Verwendung eines Beweissicherungsverfahrens oder einer Office 365-Aufbewahrungsrichtlinie für inaktive Postfächer.
  
Weitere Informationen zu eDiscovery-Fälle und Haltebereiche, finden Sie unter [eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](ediscovery-cases.md).
  
## <a name="inactive-mailboxes-and-office-365-labels"></a>Inaktive Postfächer und Office 365-Bezeichnungen

Bezeichnungen in Office 365 unterstützen Sie beim Klassifizieren von E-Mail-Daten in Ihrer Organisation für Governance und beim Erzwingen von Aufbewahrungsregeln auf Basis dieser Klassifikation. Eine Bezeichnung kann entweder manuell von Benutzern oder automatisch von Administratoren auf ein E-Mail-Element angewendet werden, und einem E-Mail-Element kann nur eine Bezeichnung zugewiesen werden. Wenn einem einzelnen E-Mail-Element im Postfach eines Benutzers eine Bezeichnung zugewiesen ist und das Postfach oder das Office 365-Konto des Benutzers gelöscht wird, wird das Postfach zu einem inaktiven Postfach. Ähnlich wie bei eDiscovery-Fallspeichern wird auch die Verwendung von Bezeichnungen nicht empfohlen, um ein Postfach als inaktiv festzulegen. Stattdessen wird empfohlen, ein Beweissicherungsverfahren oder eine Office 365-Aufbewahrungsrichtlinie zu verwenden. Beachten Sie, dass Sie im Fall von Bezeichnungen möglicherweise nicht erkennen, dass eine Bezeichnung auf ein E-Mail-Element angewendet wurde, und dann ein Postfach versehentlich als inaktiv festlegen, wenn Sie das Konto des Benutzers löschen. 
  
Weitere Informationen über Bezeichnungen finden Sie unter [Übersicht über Bezeichnungen](labels.md).
  
## <a name="inactive-mailboxes-and-exchange-mrm-retention-policies"></a>Inaktive Postfächer und Exchange MRM-Aufbewahrungsrichtlinien

Wenn eine Aufbewahrungsrichtlinie Exchange (Messaging Records Management oder MRM, Funktion in Exchange Online) auf Postfach angewendet wurde, wenn sie als inaktiv festgelegt wurde, werden alle Löschrichtlinien (die aufbewahrungstags mit eine Aufbewahrungsaktion **Löschen** konfiguriert sind) weiterhin für inaktives Postfach verarbeitet werden. Dies bedeutet, dass Elemente, die mit einer Richtlinie löschen markiert sind in Ordner "wiederherstellbare Elemente" verschoben werden sollen, wenn der Aufbewahrungszeitraum abgelaufen ist. Diese Elemente werden vom inaktives Postfach gelöscht, die Warteschleife Dauer abgelaufen. Wenn eine Warteschleife Dauer für inaktives Postfach nicht angegeben ist, werden Elemente im Ordner Elemente wiederherstellen auf unbestimmte Zeit beibehalten. 
  
Umgekehrt werden Archivrichtlinien (hierbei handelt es sich um Aufbewahrungstags, für die die Aufbewahrungsaktion **MoveToArchive** konfiguriert ist) ignoriert, die in der einem inaktiven Postfach zugewiesenen Aufbewahrungsrichtlinie enthalten sind. Elemente in einem inaktiven Postfach, die mit einer Archivrichtlinie markiert sind, verbleiben demnach im primären Postfach, wenn der Aufbewahrungszeitraum abläuft. Sie werden nicht in das Archivpostfach oder in den Ordner „Wiederherstellbare Elemente" im Archivpostfach verschoben. Sie werden unbegrenzt aufbewahrt. 
  
## <a name="creating-an-inactive-mailbox"></a>Erstellen eines inaktiven Postfachs

Damit ein Postfach inaktiv ist, muss es eine Lizenz Exchange Online (Plan 2) zugewiesen werden, damit eine Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Office 365 Aufbewahrungsrichtlinie auf das Postfach angewendet werden kann, bevor es gelöscht wird. Nach dem Löschen des Postfachs werden an, einen neuen Benutzer zugewiesen die Exchange Online-Lizenz, die es zugeordnet wurde. Inaktive Postfächer erfordern keine laufende Lizenzen.
  
In der folgenden Tabelle werden den Vorgang der Bereitstellung eines inaktiven Postfachs für unterschiedliche Aufbewahrungsrichtlinien Szenarien zusammengefasst. Weitere Informationen finden Sie unter [Verwalten inaktiver Postfächer in Office 365](create-and-manage-inactive-mailboxes.md).
  
|**Ziel**|**Vorgehensweise**|**Ergebnis**|
|:-----|:-----|:-----|
|Aufbewahren des Postfachinhalts für unbegrenzte Zeit, nachdem ein Mitarbeiter die Organisation verlassen hat  <br/> | Aktivieren Sie das Beweissicherungsverfahren für das Postfach, oder wenden Sie eine Office 365-Aufbewahrungsrichtlinie auf das Postfach an.  <br/>  Geben Sie keine Aufbewahrungsdauer für das Beweissicherungsverfahren an, bzw. konfigurieren Sie die Office 365-Aufbewahrungsrichtlinie nicht für das Löschen von Elementen; alternativ können Sie eine Aufbewahrungsrichtlinie verwenden, die Elemente unbegrenzt aufbewahrt.  <br/>  Sie entfernen das Office 365-Konto des Benutzers.  <br/> |Alle Inhalte der inaktiven Postfachs, einschließlich der Elemente in den Ordner wiederherstellbare Elemente wird auf unbestimmte Zeit beibehalten.  <br/> |
|Aufbewahren des Postfachinhalts für einen bestimmten Zeitraum nach dem Ausscheiden des Mitarbeiters und anschließendes Löschen  <br/> | Anwenden einer Aufbewahrungsrichtlinie für Office 365 an das Postfach an.  <br/>  Konfigurieren Sie die Aufbewahrungsrichtlinie um beibehalten, und klicken Sie dann Elemente löschen, wenn der Aufbewahrungszeitraum abgelaufen ist.  <br/>  Sie entfernen das Office 365-Konto des Benutzers.  <br/> |Nach Ablauf der Aufbewahrungszeitraum für ein Postfach-Element das Element wird in den Ordner wiederherstellbare Elemente verschoben, und anschließend dauerhaft gelöscht (gelöscht) aus dem inaktiven Postfach nach Ablauf der Aufbewahrungszeit (für Exchange-Postfächer). Die Aufbewahrungsdauer der Office 365 Aufbewahrungsrichtlinie kann konfiguriert werden, basierend auf dem ursprünglichen Datum, das ein Element Postfach empfangen oder erstellt wurde, oder es wurde der letzten Änderung.  <br/> |
   
**Hinweis:** Wenn eine Aufbewahrung für eventuelle Rechtsstreitigkeiten für ein Postfach bereits platziert wird oder wenn es bereits eine Aufbewahrungsrichtlinie für Office 365 angewendet wird, dann müssen Sie nur das entsprechende Office 365-Benutzerkonto zum Erstellen eines inaktiven Postfachs löschen. 
  
## <a name="managing-inactive-mailboxes"></a>Verwalten inaktiver Postfächer

Nachdem Sie ein Postfach als inaktiv festgelegt haben, können Sie verschiedene Verwaltungsaufgaben für inaktive Postfächer ausführen.
  
- **Ändern Sie die Dauer halten eines inaktiven Postfachs** Nachdem ein Postfach inaktive vorgenommen wurde, können Sie die Warteschleife Dauer der Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Office 365 Aufbewahrungsrichtlinie auf inaktives Postfach angewendet ändern. Eine schrittweise Anleitung finden Sie unter [Ändern der Dauer halten eines inaktiven Postfachs in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
    
- **Wiederherstellen ein inaktives Postfachs** Wenn einem früheren Mitarbeiter (oder einem Mitarbeiter auf Urlaub) für Ihre Organisation zurückgibt, oder wenn ein neuer Mitarbeiter eingestellt ist, die auf die Verantwortlichkeiten des Mitarbeiters ehemalige angewendet werden, können Sie den Inhalt des inaktiven Postfachs wiederherstellen. Beim Wiederherstellen eines inaktiven Postfachs, das Postfach wird in ein neues Postfach konvertiert, den Inhalt und die Ordnerstruktur des inaktiven Postfachs werden beibehalten, und das Postfach mit ein neues Benutzerkonto verknüpft ist. Nachdem es wiederhergestellt wird, ist das inaktive Postfach nicht mehr vorhanden. Schrittweise Verfahren und Informationen, was geschieht, wenn Sie ein inaktives Postfachs Wiederherstellen finden Sie unter [Wiederherstellen ein inaktives Postfachs in Office 365](recover-an-inactive-mailbox.md).
    
- **Wiederherstellen ein inaktives Postfachs** Wenn eine andere Mitarbeiter auf den Verantwortungsbereich einem früheren Mitarbeiter dauert oder eine andere Person Zugriff auf den Inhalt der inaktives Postfach benötigt, können Sie wiederherstellen (den Inhalt des inaktiven Postfachs auf ein vorhandenes Postfach oder Zusammenführen). Beim Wiederherstellen eines inaktiven Postfachs wird der Inhalt auf anderes Postfach kopiert. Inaktive Postfach wird beibehalten, und eines inaktiven Postfachs bleibt. Inaktive Postfach kann weiterhin durchsucht werden von eDiscovery-Tools, dessen Inhalt an ein anderes Postfach wiederhergestellt werden können und es wiederhergestellt oder zu einem späteren Zeitpunkt gelöscht werden kann. Schrittweise Anweisungen finden Sie unter [Wiederherstellen ein inaktives Postfachs in Office 365](restore-an-inactive-mailbox.md).
    
- **Löschen eines inaktiven Postfachs** Wenn Sie nicht mehr benötigen, die den Inhalt eines inaktiven Postfachs beibehalten werden, können Sie sie dauerhaft löschen, entfernen Sie alle Haltestatus oder Office 365-Aufbewahrungsrichtlinien inaktives Postfach angewendet. Wenn ein Postfach inaktive mehr als 30 Tage hergestellt wurde vor versehen für endgültig, nachdem Sie die Sperre aufheben. Wenn das Postfach in den letzten 30 Tagen inaktiv hergestellt wurde, können Sie diese active machen, erneut nach dem Entfernen der Richtlinie halten oder die Aufbewahrung. Schrittweise Anweisungen finden Sie unter [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md).