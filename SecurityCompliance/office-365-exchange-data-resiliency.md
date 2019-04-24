---
title: Office 365 Exchange-Datensicherheit
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
description: Eine Erläuterung der verschiedenen Aspekte der Ausfallsicherheit von Daten in Exchange Online und Office 365.
ms.openlocfilehash: 9e61efaf95d466fcb268e12317c7feab0701c062
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262757"
---
# <a name="exchange-online-data-resiliency-in-office-365"></a>Exchange Online-Datensicherheit in Office 365

## <a name="introduction"></a>Einführung
Es gibt zwei Arten von Beschädigungen, die sich auf eine Exchange-Datenbank auswirken können: physische Beschädigungen, die in der Regel durch Hardware (insbesondere Speicherhardware) verursacht werden, und logische Beschädigungen, die aufgrund anderer Faktoren auftreten. Im Allgemeinen gibt es zwei Arten von logischen Beschädigungen, die in einer Exchange-Datenbank auftreten können: 
- **Logische Beschädigung der Datenbank** – die Prüfsumme der Datenbankseite stimmt, aber die Daten auf der Seite sind logisch falsch. Dies kann auftreten, wenn das Datenbankmodul (ESE (Extensible Storage Engine)) versucht, eine Datenbankseite zu schreiben, und obwohl das Betriebssystem eine Erfolgsmeldung zurückgibt, die Daten entweder nie auf den Datenträger geschrieben werden oder an der falschen Stelle geschrieben werden. Dies wird als *verlorene Leerung* bezeichnet. ESE enthält zahlreiche Features und Sicherheitsvorkehrungen, die eine physische Beschädigung einer Datenbank und anderer datenverlustszenarien verhindern sollen. Um zu verhindern, dass Verlust von Datenverlusten verloren geht, enthält ESE einen Mechanismus zur Bereinigung von Leerzeichen in der Datenbank zusammen mit einem Feature (Einzelseiten Wiederherstellung), um es zu korrigieren. 
- **Speicher logische Beschädigung** – Daten werden in einer vom Benutzer erwarteten Weise hinzugefügt, gelöscht oder manipuliert. Diese Fälle werden im Allgemeinen durch Anwendungen von Drittanbietern verursacht. Es handelt sich im Allgemeinen nur insofern um eine Beschädigung, als der Benutzer sie als Beschädigung betrachtet. Der Exchange-Speicher betrachtet die Transaktion, die zur logischen Beschädigung geführt hat, als eine Folge gültiger MAPI-Operationen. Die [in-situ-Aufbewahrungs](https://docs.microsoft.com/exchange/security-and-compliance/create-or-remove-in-place-holds) Funktionen in Exchange Online bieten Schutz vor Speicher logischen Beschädigungen (da verhindert wird, dass Inhalte dauerhaft von einem Benutzer oder einer Anwendung gelöscht werden). 

Exchange Online führt während der Protokoll Überprüfung und der Protokollwiedergabe mehrere Konsistenzprüfungen für replizierte Protokolldateien aus. Diese Konsistenzprüfungen verhindern, dass physische Beschädigungen vom System repliziert werden. Beispielsweise gibt es bei der Protokoll Überprüfung eine physikalische Integritätsprüfung, die die Protokolldatei überprüft und überprüft, ob die in der Protokolldatei aufgezeichnete Prüfsumme mit der im Arbeitsspeicher generierten Prüfsumme übereinstimmt. Darüber hinaus wird der Protokoll Dateikopf überprüft, um sicherzustellen, dass die im Protokollheader aufgezeichnete Protokolldatei mit der Protokolldatei übereinstimmt. Während der Protokollwiedergabe wird die Protokolldatei genauer untersucht. Der Datenbankheader enthält beispielsweise auch die Protokollsignatur, die mit der Signatur der Protokolldatei verglichen wird, um sicherzustellen, dass Sie übereinstimmen. 

Schutz vor Beschädigung von Postfachdaten in Exchange Online wird mithilfe von Exchange Native Data Protection, eine Ausfallsicherheit Strategie, die Replikation auf Anwendungsebene über mehrere Server und mehrere Rechenzentren zusammen mit anderen Features zum Schutz vor Verlust von Daten aufgrund von Beschädigungen oder anderen Gründen. Zu diesen Features gehören systemeigene Features, die von Microsoft oder der Exchange Online-Anwendung selbst verwaltet werden, wie beispielsweise:

- [Daten VerfügbarkeitsGruppen](https://docs.microsoft.com/exchange/back-up-email)
- Korrektur für ein einzelnes Bit 
- Online Datenbank-überPrüfung 
- Erkennung verlorener Flush 
- Wiederherstellung einzelner Seiten 
- Postfachreplikationsdienst 
- Protokolldatei Prüfungen 
- Bereitstellung auf einem stabilen Datei System 

Weitere Informationen zu den oben aufgeführten systemeigenen Features erhalten Sie, wenn Sie auf die obigen Hyperlinks klicken, um weitere Informationen und Details zu Elementen ohne Hyperlinks anzuzeigen. Zusätzlich zu diesen systemeigenen Features umfasst Exchange Online auch Daten Resilienz-Features, die Kunden verwalten können, wie zum Beispiel: 
- [Wiederherstellung einzelner Elemente (standardmäßig aktiviert)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [In-Situ-Speicher und Beweissicherungsverfahren](https://docs.microsoft.com/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Aufbewahrungszeit für gelöschte Elemente und automatisch gelöschte Postfächer (beide sind standardmäßig aktiviert)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>DatenbankverfügbarkeitsGruppen 
Jede Postfachdatenbank in Office 365 wird in einer [Database Availability Group (DAG)](https://docs.microsoft.com/exchange/back-up-email) gehostet und in geografisch getrennte Datencenter innerhalb derselben Region repliziert. Die häufigste Konfiguration ist vier Datenbankkopien in vier Rechenzentren; Einige Regionen verfügen jedoch über weniger Rechenzentren (Datenbankenwerden in drei Rechenzentren in Indien und zwei Rechenzentren in Australien und Japan repliziert). In allen Fällen verfügt jedoch jede Postfachdatenbank über vier Kopien, die über mehrere Rechenzentren verteilt sind, wodurch sichergestellt wird, dass die Postfachdaten vor Software-, Hardware-und sogar Rechenzentrums Fehlern geschützt sind. 

Von diesen vier Kopien werden drei davon als hoch verfügbar konfiguriert. Die vierte Kopie ist als verzögerte [Datenbankkopie](https://docs.microsoft.com/Exchange/high-availability/manage-ha/activate-lagged-db-copies)konfiguriert. Die verzögerte Datenbankkopie ist nicht für die Wiederherstellung einzelner Postfächer oder Postfachelemente vorgesehen. Ziel ist die Bereitstellungeines Wiederherstellungsmechanismus für das seltene Ereignis einer systemweiten, katastrophalen logischen Beschädigung. 

Verzögerte Datenbankkopien in Exchange Online werden mit einem siebentägigen Replay-Verzögerungs Zeitpunkt für die Protokolldatei konfiguriert. Darüber hinaus ist der Exchange-Replay-Verzögerungs-Manager aktiviert, um eine dynamische Protokolldatei für verzögerte Kopien bereitzustellen, damit verzögerte Datenbankkopien selbst repariert und das Wachstum der Protokolldatei verwaltet werden kann. Obwohl verzögerte Datenbankkopien in Exchange Online verwendet werden, ist es wichtig zu wissen, dass es sich nicht um eine garantierte Point-in-Time-Sicherung handelt. Verzögerte Datenbankkopien in Exchange Online verfügen über einen Verfügbarkeits Schwellenwert (in der Regel rund 90%), da der Datenträger, der eine verzögerte Kopie enthält, aufgrund eines Datenträgerfehlers verloren geht, und dass die verzögerte Kopie zu einer hoch verfügbaren Kopie (aufgrund der automatischen Wiedergabe) wird. als die Zeiträume, in denen die verzögerte Datenbankkopie die Protokollwiedergabe Warteschlange neu aufbaut. 

## <a name="transport-resilience"></a>Transport Ausfallsicherheit 
Exchange Online umfasst zwei primäre Transport Ausfallsicherheit-Features: Shadow-Redundanz und Sicherheitsnetz. Die Shadow-Redundanz behält eine redundante Kopie einer Nachricht bei der Übertragung bei. Das Sicherheitsnetz speichert eine redundante Kopie einer Nachricht, nachdem die Nachricht erfolgreich zugestellt wurde. 

Bei der Shadow-Redundanz erstellt jeder Exchange Online-Transport Server eine Kopie der einzelnen Nachrichten, die er empfängt, bevor er den erfolgreichen Empfang der Nachricht an den sendenden Server bestätigt. Dadurch werden alle Nachrichten in der Transportpipeline während der Übertragung redundant. Wenn Exchange Online feststellt, dass die ursprüngliche Nachricht während der Übertragung verloren gegangen ist, wird eine redundante Kopie der Nachricht erneut übermittelt. 

Sicherheitsnetz ist eine Transportwarteschlange, die dem Transportdienst auf einem Postfachserver zugeordnet ist. In dieser Warteschlange werden Kopien von Nachrichten gespeichert, die vom Server erfolgreich verarbeitet wurden. Wenn für eine Postfachdatenbank oder einen Serverfehler die Aktivierung einer veralteten Kopie der Postfachdatenbank erforderlich ist, werden Nachrichten in der Sicherheitsnetz Warteschlange automatisch erneut an die neue aktive Kopie der Postfachdatenbank übermittelt. Das Sicherheitsnetz ist ebenfalls redundant, wodurch der Transport nicht als einziger Punkt des Fehlers verhindert wird. Es verwendet das Konzept eines primären Sicherheitsnetzes und ein Shadow-Sicherheitsnetz, wenn das primäre Sicherheitsnetz für mehr als 12 Stunden nicht verfügbar ist, Resubmit-Anforderungen zu Shadow Resubmit-Anforderungen werden und Nachrichten aus dem Shadow-Sicherheitsnetz erneut zugestellt werden.

Die erneute Übermittlung von nachRichten aus dem Sicherheitsnetz wird automatisch von der Active Manager-Komponente des Microsoft Exchange-Replikationsdiensts initiiert, die DAGs und Postfachdatenbankkopien verwaltet. Es sind keine manuellen Aktionen erforderlich, um Nachrichten aus dem Sicherheitsnetz erneut zu übermitteln. 

## <a name="single-bit-correction"></a>Korrektur für ein einzelnes Bit 
ESE enthält einen Mechanismus zum Aufspüren und Auflösen von Single-Bit-CRC-Fehlern (aka Single-Bit-Flips), die das Ergebnis von Hardwarefehlern sind (und als solche physische Beschädigungen darstellen). Wenn diese Fehler auftreten, korrigiert ESE Sie automatisch und protokolliert ein Ereignis im Ereignisprotokoll. 

## <a name="online-database-scanning"></a>Online Datenbank-überPrüfung 
Bei der Online Datenbank-Überprüfung (auch bekannt als *Datenbankprüfsumme*) handelt es sich um den Prozess, bei dem eine ESE eine Datenbankkonsistenzprüfung verwendet, um jede Seite zu lesen und auf die Seite zu prüfen. Der primäre Zweck besteht darin, physische Beschädigungen zu erkennen und Leerräume zu verlieren, die möglicherweise nicht durch transaktionale Vorgänge erkannt werden. Bei der Datenbanküberprüfung werden auch Absturz Vorgänge nach dem Speichern ausgeführt. Speicherplatz kann aufgrund von Abstürzen geleckt werden, und die Online-Datenbanküberprüfung findet und gewinnt verlorenen Speicherplatz. Das System hat die Erwartung, dass jede Datenbank alle sieben Tage vollständig überprüft wird. 

## <a name="lost-flush-detection"></a>Erkennung verlorener Flush 
Ein Verlust Flush tritt auf, wenn ein Datenbankschreibvorgang, bei dem das Datenträgersubsystem/-Betriebssystem als abgeschlossen zurückgegeben wurde, nicht tatsächlich auf den Datenträger geschrieben oder am falschen Speicherort geschrieben wurde. Verloren geGangene Flush-Vorfälle können zu Daten Bank logischen Beschädigungen führen, um zu verhindern, dass verlorene Leerräume zu Datenverlusten führt, enthält ESE einen Mechanismus zur Erkennung verlorener Nachweise. Wenn Datenbankseiten in passive Kopien geschrieben werden, wird eine Prüfung für verlorene Leerräume in der aktiven Kopie durchgeführt. Wenn ein verlorenes Flush erkannt wird, kann ESE den Prozess mithilfe eines Seiten-Patchings reparieren. 

## <a name="single-page-restore"></a>Wiederherstellung einzelner Seiten 
Single Page Restore, Alias *Page Patching*, ist ein automatischer Prozess, bei dem beschädigte Datenbankseiten durch gesunde Kopien von einem gesunden Replikat ersetzt werden. Der Reparaturprozess für eine beschädigte Seite hängt davon ab, ob die Datenbankkopie aktiv oder passiv ist. Wenn eine aktive Datenbankkopie eine beschädigte Seite findet, kann Sie eine Seite aus einem Replikat kopieren, sofern die Seite vollständig auf dem neuesten Stand ist. Dies wird erreicht, indem eine Anforderung für die Seite in den Protokolldatenstrom eingefügt wird, der die Grundlage für die Replikation der Postfachdatenbank ist. Sobald ein Replikat auf die Seitenanforderung trifft, sendet es eine Kopie der Seite an die anfordernde Datenbankkopie. Die Wiederherstellung einzelner Seiten stellt auch einen asynchronen Kommunikationsmechanismus für die aktive zum Anfordern einer Seite aus Replikaten bereit, auch wenn die Replikate derzeit offline sind. 

Bei Beschädigungen in einer passiven Datenbankkopie, einschließlich einer verzögerten Datenbankkopie, da sich diese Kopien immer hinter der aktiven Kopie befinden, ist es immer sicher, eine Seite aus der aktiven Kopie in eine passive Kopie zu kopieren. Eine passive Datenbankkopie ist von Natur aus hoch verfügbar, sodass das Wiedergeben von Protokollen während des Seiten-Patchings angehalten wird, aber der Protokollkopiervorgang wird fortgesetzt. Die passive Datenbankkopie Ruft eine Kopie der beschädigten Seite aus der aktiven Kopie ab, wartet, bis die Protokolldatei, die die maximale erforderliche Protokoll Generierungs Anforderung erfüllt, kopiert und überprüft wird, und dann die beschädigte Seite Patches. Sobald die Seite gepatcht wurde, wird die Protokollwiedergabe fortgesetzt. Der Prozess ist für die verzögerte Datenbankkopie identisch, mit dem Unterschied, dass die verzögerte Datenbank zunächst alle Protokolldateien wiedergibt, die zum Erreichen eines patchable-Status erforderlich sind. 

## <a name="mailbox-replication-service"></a>Postfachreplikationsdienst 
Das Verschieben von Postfächern ist ein wichtiger Teil der Verwaltung eines großen e-Mail-Diensts. Es gibt immer aktualisierte Technologien und Hardware-und Versions-Upgrades, um mit einem stabilen, gedrosselten System zu arbeiten, das es unseren Ingenieuren ermöglicht, diese Aufgabe zu bewältigen, und gleichzeitig die Postfachverschiebungen für Benutzer transparent zu halten (indem Sie sicherstellen, dass Sie online bleiben. während des gesamten Prozesses) ist der Schlüssel und stellt sicher, dass der Prozess ordnungsgemäß skaliert werden, wenn Postfächer größer und größer werden. 

Der Exchange-Postfachreplikationsdienst (MRS) ist für das Verschieben von Postfächern zwischen Datenbanken zuständig. Während der Verschiebung führt MRS eine Konsistenzprüfung für alle Elemente innerhalb des Postfachs durch. Wenn ein Konsistenzproblem gefunden wird, wird MRS entweder das Problem beheben oder die beschädigten Elemente überspringen, wodurch die Beschädigung aus dem Postfach entfernt wird. 

Da MRS eine Komponente von Exchange Online ist, können wir Änderungen am Code vornehmen, um neue Formen der Beschädigung zu beheben, die in der Zukunft erkannt werden. Wenn beispielsweise ein Konsistenzproblem festgestellt wird, das MRS nicht beheben kann, können wir die Beschädigung analysieren, den MRS-Code ändern und die Inkonsistenz korrigieren (wenn wir verstehen, wie). 

## <a name="log-file-checks"></a>Protokolldatei Prüfungen 
Alle Transaktionsprotokolldateien, die von einer Exchange-Datenbank generiert werden, unterliegen verschiedenen Arten von Konsistenzprüfungen. Wenn eine Protokolldatei erstellt wird, ist zunächst ein Bitmuster geschrieben und dann eine Reihe von Protokollschreib Vorgängen ausgeführt. Auf diese Weise kann Exchange Online eine Reihe von Prüfungen durchführen (Verlust von Flush, CRC und anderen Prüfungen), um jede Protokolldatei so zu validieren, wie Sie geschrieben wird, und wieder, wenn Sie repliziert wird. 

## <a name="deployment-on-resilient-file-system"></a>Bereitstellung auf einem stabilen Datei System 
Um zu verhindern, dass Beschädigungen auf Dateisystemebene auftreten, wird Exchange Online auf den systemeigenen ReFS-Partitionen bereitgestellt, um verbesserte Wiederherstellungsfunktionen bereitzustellen. ReFS ist ein Dateisystem in Windows Server 2012 und höher, das auf eine bessere Datenbeschädigung ausgelegt ist und dadurch die Verfügbarkeit und Integrität von Dateien maximiert. Insbesondere führt ReFS zu Verbesserungen in der Art und Weise, wie Metadaten aktualisiert werden, wodurch Daten besser geschützt und Daten beschädigt werden. Außerdem werden Prüfsummen verwendet, um die Integrität von Dateidaten und Metadaten zu überprüfen, um sicherzustellen, dass Datenbeschädigungen leicht gefunden und repariert werden können. 

Exchange Online nutzt mehrere Vorteile von ReFS: 
- Mehr Ausfallsicherheit bei der Datenintegrität führt zu weniger Datenbeschädigungen. Das Verringern der Anzahl von Beschädigungs Vorfällen führt zu weniger unnötigen Daten Bank reseeds. 
- PrüfSumme, die auf Metadaten ausgeführt wird, die eine schnellere und deterministische Entdeckung von Korruptionsfällen ermöglichen, sodass wir Kundendaten Beschädigungen beheben können, bevor graue Fehler auf Daten-Volumes auftreten.
- Entwickelt für eine gute Zusammenarbeit mit extrem großen Datasets – Petabyte und höher – ohne Leistungseinbußen
- Unterstützung für andere Features, die von Exchange Online verwendet werden, beispielsweise BitLocker-Verschlüsselung. 

Exchange Online profitiert auch von anderen ReFS-Features: 
- **Integrity (integrIty Streams)** -ReFS speichert Daten so, dass Sie vor vielen häufig auftretenden Fehlern geschützt werden, die normalerweise zu Datenverlusten führen können. Die Office 365-Suche verwendet IntegritätsDaten Ströme, um die Erkennung von Datenträgerbeschädigungen und Prüfsummen für Dateiinhalte zu erleichtern. Das Feature reduziert außerdem Beschädigungs Vorfälle durch "Torn Writes" (wenn ein Schreibvorgang aufgrund von Stromausfällen usw. nicht abgeschlossen wird). 
- **Verfügbarkeit (Bergungs-)** -ReFS priorisiert die Verfügbarkeit von Daten. Historisch gesehen waren Dateisysteme oft anfällig für Datenbeschädigungen, bei denen das System zur Reparatur offline geschaltet werden muss. Obwohl es selten ist, implementiert ReFS eine Bergungs Funktion, die die beschädigten Daten aus dem Namespace auf einem Live-Volume entfernt und sicherstellt, dass die fehlerhaften Daten nicht beeinträchtigt werden. Durch die Anwendung des Bergungs Features und die Isolierung von Datenbeschädigungen in Exchange Online-Datenbankdatenträgern können wir nicht betroffene Datenbanken zwischen dem Zeitpunkt der Beschädigung und der Reparaturaktion auf einem beschädigten Volume halten. Dadurch wird die Verfügbarkeit von Datenbanken erhöht, die normalerweise von derartigen Datenträgerbeschädigungen betroffen wären. 