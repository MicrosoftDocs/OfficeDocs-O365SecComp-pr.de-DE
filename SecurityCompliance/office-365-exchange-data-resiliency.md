---
title: Office 365 Exchange Datenflexibilität
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
description: Eine Erklärung der verschiedenen Aspekte der datenflexibilität in Exchange Online und Office 365.
ms.openlocfilehash: 8d0448a95f010b766faf852a374513a1c2da61fa
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529345"
---
# <a name="exchange-online-data-resiliency-in-office-365"></a>Exchange Online Datenflexibilität in Office 365

## <a name="introduction"></a>Einführung
Es gibt zwei Arten der Beschädigung, die eine Exchange-Datenbank beeinflussen: physische Beschädigung, was in der Regel (in bestimmten, Speicherhardware) Hardwareprobleme zurückzuführen ist, und logische Beschädigung, das eintritt, aufgrund von anderen Faktoren. Im Allgemeinen stehen zwei Arten von logischen Beschädigung, die innerhalb einer Exchange-Datenbank auftreten können: 
- **Logische Datenbankfehler** - Datenbank Seite Prüfsumme übereinstimmt, aber die Daten auf der Seite ist logisch falsch. Dies auftreten kann, wenn die Datenbank-Engine (die Extensible Storage Engine (ESE)) versucht, eine Datenbankseite geschrieben und, obwohl das Betriebssystem eine Erfolgsmeldung zurückgegeben, die Daten ist entweder nicht auf den Datenträger geschrieben oder in der falschen Stelle geschrieben. Dies wird als eine *flush verloren*bezeichnet. ESE enthält zahlreiche Features und Sicherheitsmaßnahmen, die entworfen wurden, um physische Beschädigung einer Datenbank und andere Datenverlust Szenarien zu verhindern. Um zu verhindern, dass verloren leert Datenverlust, enthält ESE einen Erkennungsmechanismus verloren flush-in der Datenbank sowie eine Funktion (einseitige wiederherstellen) korrigieren. 
- **Logische Beschädigung Store** - Daten wird hinzugefügt, gelöscht oder in eine Möglichkeit, das der Benutzer nicht geändert. Dieser Fälle werden in der Regel durch drittanbieteranwendungen verursacht. Es ist in der Regel nur eine Beschädigung insofern, als der Benutzer als eine Beschädigung anzeigt. Exchange-Speicher berücksichtigt die Transaktion, die logische Beschädigung, um eine Reihe von Operationen, gültige MAPI werden erstellt. Die [Compliance-Archiv](https://docs.microsoft.com/exchange/security-and-compliance/create-or-remove-in-place-holds) -Funktionen in Exchange Online bietet Schutz vor Store logische Beschädigung (, da es Inhalt verhindert, dass endgültig gelöscht werden, von einem Benutzer oder einer Anwendung). 

Exchange Online ausführt mehrere konsistenzprüfungen für replizierte Protokolldateien während der Prüfung der Protokolldateien und Protokollwiedergabe. Diese konsistenzprüfungen zu verhindern, dass physische Beschädigung aus, die vom System repliziert. Während der Überprüfung der Protokolldatei wird beispielsweise eine physische integritätsprüfung überprüft die Protokolldatei und überprüft, dass die in der Protokolldatei aufgezeichnete Prüfsumme im Arbeitsspeicher generierte Prüfsumme übereinstimmt. Darüber hinaus wird in der Kopfzeile untersucht, um sicherzustellen, dass die Signatur der Log-Datei in der Kopfzeile des Protokolls aufgezeichnet, die der Protokolldatei übereinstimmt. Während der Wiedergabe des Transaktionsprotokolls der Deklaration der Protokolldatei weitere Prüfung. Beispielsweise enthält Kopfzeile der Datenbank auch die Log-Signatur, das mit der Protokolldatei Signatur, um sicherzustellen, dass sie übereinstimmen verglichen wird. 

Schutz gegen Beschädigung Postfachdaten in Exchange Online erfolgt mithilfe von Exchange Native Data Protection einer Strategie für die ausfallsicherheit, die auf Anwendungsebene Replikation auf mehreren Servern und mehreren Rechenzentren zusammen mit anderen nutzt Features, die Daten zu schützen aufgrund einer Beschädigung oder aus anderen Gründen verloren gehen. Dazu zählen systemeigene Funktionen, die von Microsoft oder der Exchange Online-Anwendung selbst, wie etwa verwaltet werden:

- [Daten-Verfügbarkeitsgruppen](https://docs.microsoft.com/exchange/back-up-email)
- Einzelnes Bit Korrektur 
- Überprüfen von Online-Datenbank 
- Flush Erkennung verloren 
- Einzelne Seite wiederherstellen 
- Mailbox Replication Service 
- Melden Sie sich eine Überprüfung auf Dateiebene 
- Bereitstellung auf Resilient File System 

Weitere Informationen zu den oben aufgeführten systemeigenen Funktionen klicken Sie auf die oben genannten Hyperlinks und finden Sie weiter unten für Weitere Informationen und Details auf Elemente ohne Hyperlinks. Zusätzlich zu diesen systemeigenen Funktionen enthält Exchange Online auch Daten Resiliency Features, die Kunden, wie etwa verwalten können: 
- [(Standardmäßig aktiviert) Wiederherstellung einzelner Elemente](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [In-Situ-Speicher und Beweissicherungsverfahren](https://docs.microsoft.com/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Gelöschte Aufbewahrung von Elementen und Soft-Deleted Postfächer (beide standardmäßig aktiviert)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Database Availability Groups 
Jede Postfachdatenbank in Office 365 wird in einer [Database Availability Group (DAG)](https://docs.microsoft.com/exchange/back-up-email) gehostet und in geografisch getrennte Rechenzentren innerhalb desselben Bereichs repliziert. Die am häufigsten verwendete Konfiguration ist vier Datenbankkopien in vier Rechenzentren. Einige Regionen müssen jedoch weniger Rechenzentren (Datenbanken werden auf drei Rechenzentren in Indien und zwei Rechenzentren in Australien und Japan repliziert). Jedoch in allen Fällen jede Postfachdatenbank gibt es vier Kopien, die für mehrere Rechenzentren, um sicherzustellen, dass die Postfachdaten von Software, Hardware und sogar Datacenter mit Fehlern geschützt ist verteilt werden. 

Nicht genügend diese vier Kopien sind drei davon als hochverfügbare konfiguriert. Die vierte Kopie wird als eine [verzögerte Datenbankkopie](https://docs.microsoft.com/Exchange/high-availability/manage-ha/activate-lagged-db-copies)konfiguriert. Die verzögerte Datenbankkopie ist nicht für einzelne postfachwiederherstellung oder Element postfachwiederherstellung vorgesehen. Ihr Zweck ist einen Recovery-Mechanismus für das Ereignis seltenen systemweiten, nach einem schwerwiegenden Fehler logische Beschädigung bereitstellen. 

Verzögerte Datenbankkopien in Exchange Online sind mit einer sieben Tagen Datei-wiedergabeverzögerung konfiguriert. Darüber hinaus ist Exchange Replay Lag-Manager anzugebende dynamische Protokoll Datei die Wiedergabe für verzögerte Kopien für die verzögerte Datenbankkopien automatische Reparatur und verwalten Wachstum der Datei zulassen aktiviert. Obwohl Datenbank verzögerte Kopien in Exchange Online verwendet werden, ist es wichtig zu verstehen, sind sie nicht garantiert Zeitpunkt-Sicherung. Verzögerte Datenbankkopien in Exchange Online haben Verfügbarkeit Schwellenwert in der Regel etwa 90 % aufgrund der Zeiträume, in dem der Datenträger, auf eine verzögerte Kopie durch Datenträgerfehler, die verzögerte Kopie eine hochverfügbare immer verloren ist (aufgrund von Automatische Wiedergabe), auch kopieren der Wiedergabewarteschlange Warteschlange als die Zeiträume, in dem die verzögerte Datenbankkopie Protokoll erneut erstellt wird. 

## <a name="transport-resilience"></a>Transport von Standorten 
Exchange Online umfasst zwei primäre Transport von Standorten Features: Shadow-Redundanz und Sicherheitsnetz. Shadow-Redundanz hält eine redundante Kopie einer Nachricht, während sie während der Übertragung ist. Sicherheitsnetz hält eine redundante Kopie einer Nachricht, nachdem die Nachricht erfolgreich zugestellt wird. 

Mit Shadow-Redundanz wird jeder Exchange Online-Transport-Server eine Kopie der einzelnen Nachrichten, die er erhält, bevor es Elementarten erfolgreich empfangen der Nachricht an den absenderserver. Dadurch wird alle Nachrichten in der Transportpipeline unterwegs redundant. Exchange Online fest, dass die ursprüngliche Nachricht während der Übertragung verloren wurde, wird eine redundante Kopie der Nachricht erneut zugestellt. 

Sicherheitsnetz ist eine Transport-Warteschlange, die den Transportdienst auf einem Postfachserver zugeordnet ist. Diese Warteschlange Kopien der Nachrichten, die vom Server erfolgreich verarbeitet wurden. Wenn ein Postfach Datenbank- oder Fehler eine veraltete Kopie der Postfachdatenbank aktivieren erfordert, werden Nachrichten in der Warteschlange Sicherheitsnetz automatisch auf die neue aktive Kopie der Postfachdatenbank erneut übermittelt. Sicherheitsnetz ist auch redundant, sodass nicht Transport als eine einzelne Fehlerquelle. Es verwendet das Konzept der primären Sicherheitsnetz und ein Schatten Sicherheitsnetz in dem, wenn der primäre Sicherheitsnetz für mehr als 12 Stunden nicht verfügbar ist, erneut zu übermitteln Anfragen werden Schatten zur erneuten Übermittlung Anforderungen, und Nachrichten aus den Schatten Safety Net erneut übermittelt werden.

Das erneute senden Nachrichten aus Safety Net werden automatisch von der Komponente Active Manager von der Microsoft Exchange-Replikationsdienst, die DAGs und Postfach verwaltet initiiert Datenbankkopien. Keine manuellen Aktionen sind erforderlich, um Nachrichten aus Safety Net erneut zu übermitteln. 

## <a name="single-bit-correction"></a>Einzelnes Bit Korrektur 
ESE enthält einen Mechanismus zum Erkennen und lösen Sie Einzel-Bit-CRC-Fehler (auch bekannt als kippt Einzel-Bit), die das Ergebnis der Hardwarefehler sind (und als solche sie physische Beschädigung darstellen). Wenn diese Fehler auftreten, wird ESE automatisch korrigiert diese und im Ereignisprotokoll ein Ereignis protokolliert. 

## <a name="online-database-scanning"></a>Überprüfen von Online-Datenbank 
Online-Datenbank (auch bekannt als *Datenbank Prüfsumme*) Scannen bezeichnet den Vorgang, in dem eine ESE eine Datenbank konsistenzüberprüfung auf jeder Seite lesen und überprüfen Sie für eine Beschädigung der Seite zu. Der primäre Zweck ist zum Erkennen von physische Beschädigung und verlorenen geleert, die nicht vom transaktionale Vorgänge erkannt erste werden können. Überprüfung der Datenbank führt auch nach der Store Absturz Vorgänge. Leerzeichen kann aufgrund von Abstürzen verloren werden, und online-Datenbank untersucht gesucht und verlorenen Speicherplatz wiederhergestellt. Das System wird unter der Annahme so konzipiert, dass alle sieben Tage vollständig in jeder Datenbank überprüft wird. 

## <a name="lost-flush-detection"></a>Flush Erkennung verloren 
Eine Bereinigung verlorene tritt auf, wenn ein Schreibvorgang für Datenbank, die dem Subsystem Datenträger/Betriebssystem zurückgegeben wird, als abgeschlossen nicht tatsächlich in geschrieben wurden auf dem Datenträger oder in den falschen Speicherort geschrieben wurde. Flush Vorfälle verloren können Ergebnis in logischen datenbankbeschädigung, also so verhindern Sie, dass verloren leert resultierenden Daten verloren gehen, ESE enthält einen verlorenen flush Erkennungsmechanismus. Wie Datenbankseiten in passiven Kopien geschrieben werden, erfolgt eine Überprüfung für verloren leert in der aktiven Kopie. Wenn eine Bereinigung verlorene erkannt wird, kann ESE den Prozess, indem eine Seite patchingprozess reparieren. 

## <a name="single-page-restore"></a>Einzelne Seite wiederherstellen 
Einseitige wiederherstellen, auch bekannt als *Patchen*, läuft automatisch ab, in dem beschädigt Datenbankseiten durch fehlerfreie Kopien aus einer fehlerfreien Replikat ersetzt werden. Der Reparatur für eine beschädigte Seite hängt davon ab, ob die Datenbankkopie aktiv oder Passiv ist. Wenn eine Kopie der aktiven Datenbank eine beschädigte Seite stößt, können sie eine Seite eines seiner Replikate kopieren, sofern die Seite, kopiert vollständig auf dem neuesten Stand ist. Dies wird durch die Protokollstream, der Grundlage für die Postfach-Datenbankreplikation ist eine Anforderung für die Seite Inbetriebnahme erreicht. Sobald ein Replikat der angeforderte Seite erkannt wird durch Senden einer Kopie der Seite an den anfordernden Datenbankkopie reagiert. Einseitige Wiederherstellen bietet auch einen asynchronen Kommunikationsmechanismus für das aktive zum Anfordern einer Seite von Replikate, selbst wenn die Replikate momentan offline sind. 

Im Falle einer Beschädigung in eine passive Datenbankkopie einschließlich eine verzögerte Datenbankkopie, da diese Kopien immer hinter die aktive Kopie sind, es ist sicherer, eine beliebige Seite aus der aktiven Kopie in eine passive Kopie zu kopieren. Eine passive Datenbankkopie ist grundsätzlich hochverfügbare, damit während der Seite patchingprozess Wiedergabe von Protokolldateien angehalten wird, aber weiterhin kopieren. Die passive Datenbankkopie Ruft eine Kopie der beschädigten Seite aus der aktiven Kopie, wartet, bis die Protokolldatei die maximale erforderlichen Protokolldateien Generation Anforderung erfüllt wird kopiert und geprüft und klicken Sie dann die beschädigte Seite patches. Nachdem die Seite gepatcht wurde, werden die Protokollwiedergabe fortgesetzt. Der Prozess ist für die verzögerte Datenbankkopie identisch, außer dass die verzögerte Datenbank zunächst alle Protokolldateien, die erforderlich sind gibt, um einen patchable Zustand zu erreichen sind. 

## <a name="mailbox-replication-service"></a>Mailbox Replication Service 
Verschieben von Postfächern ist ein wichtiger Teil der Verwaltung umfangreicher-e-Mail-Dienst. Es sind immer aktualisierte Technologien und Hardware- und Version Upgrades für den Umgang mit, damit eine robuste, dass gedrosselt System, unsere Ingenieure in Arbeit und das Postfach weiterhin durchführen können, verschoben transparent für Benutzer (indem sichergestellt wird, dass sie online bleiben über den gesamten Prozess) ist Schlüssel und es wird sichergestellt, dass der Prozess wird ordnungsgemäß skaliert, wie Postfächer je mehr erhalten möchten. 

Gruppenrichtlinien-Verwaltungskonsole (Exchange Postfach Replication Service, MRS) ist verantwortlich für das Verschieben von Postfächern zwischen Datenbanken. Während des Verschiebens führt MRS eine konsistenzprüfung für alle Elemente innerhalb des Postfachs an. Wenn ein Problem Konsistenz gefunden wird, wird MRS wird entweder das Problem zu beheben oder beschädigte Elemente, überspringen, wodurch Beschädigung aus dem Postfach entfernt. 

Da MRS eine Komponente von Exchange Online ist, können wir in ihrem Code Adresse neuer Formulare der Beschädigung ändern, die in der Zukunft erkannt werden. Beispielsweise wenn wir ein Problem Konsistenz, die MRS nicht beheben kann erkennen, wir können Beschädigung zu analysieren, ändern Sie den Code MRS und korrigieren Sie die Inkonsistenz (Wenn wir wissen, wie Sie). 

## <a name="log-file-checks"></a>Melden Sie sich eine Überprüfung auf Dateiebene 
Alle Transaktionsprotokolldateien von einer Exchange-Datenbank generierte unterzogen werden mehrere konsistenzprüfungen. Wenn eine Protokolldatei erstellt wird, ist die erstes fertig ein Bitmuster wird geschrieben, und klicken Sie dann eine Reihe von Schreibvorgängen durchgeführt wird. Auf diese Weise können Exchange Online zum Ausführen einer Reihe von überprüft, ob (verloren Flush, CRC und andere überprüft), um jeder Protokolldatei zu überprüfen, wie er geschrieben wurde, und klicken Sie erneut, während sie repliziert werden. 

## <a name="deployment-on-resilient-file-system"></a>Bereitstellung auf Resilient File System 
Um eine Beschädigung auftritt auf Dateiebene System zu verhindern, ist Exchange Online auf Partitionen anzugebende verbesserte Wiederherstellungsfunktionen ausfallsichere File System (ReFS) bereitgestellt wird. ReFS ist ein Dateisystem in Windows Server 2012 und höher, das vor Beschädigung der Daten und Maximierung der Verfügbarkeit und Integrität ausfallsicherer werden soll. Insbesondere bringt ReFS Verbesserungen in die Möglichkeit, Metadaten wird aktualisiert, die bietet einen besseren Schutz für Daten und verringert die Daten beschädigt sind. Verwendet auch Prüfsumme zum Überprüfen der Integrität von Daten und Metadaten, eine Beschädigung der Daten zu gewährleisten, dass einfach gefunden und repariert. 

Exchange Online nutzt mehrere ReFS Vorteile: 
- Weitere Resiliency Datenintegrität bedeutet weniger Daten Beschädigung Vorfälle. Reduzieren der Anzahl der Beschädigung Vorfälle bedeutet weniger Datenbank unnötig Seeding nützlich. 
- Auf Metadaten Aktivieren der Erkennung von beschädigt sind schneller und mehr deterministisch, da wir So korrigieren Sie Kundendaten mit Prüfsumme Beschädigung, bevor auf Inhaltsdaten graue Fehler auftreten.
- Sehr große Datenmengen gut entwickelt – Kostenfaktor und größere – ohne Auswirkung auf die Leistung
- Unterstützung für andere Features von Exchange Online, wie BitLocker-Verschlüsselung verwendet. 

Exchange Online bietet auch von anderen Features ReFS Vorteile: 
- **Integrität (Integrität Datenströme)** - ReFS speichert die Daten in eine Möglichkeit, die es viele häufige Fehler schützt, die normalerweise von Datenverlusten führen können. Office 365-Suche verwendet Integrität Datenströme frühe Datenträger Beschädigung Erkennung und Prüfsumme der Inhalt der Datei zu unterstützen. Das Feature wird auch eine Beschädigung Vorfälle aufgrund von "Zerrissenes schreibt" (wenn ein Schreibvorgang nicht abgeschlossen wurde aufgrund von Stromausfall usw..) reduziert. 
- **Verfügbarkeit (Restwert)** – ReFS priorisiert die Verfügbarkeit der Daten. In der Vergangenheit wurden Dateisysteme häufig anfällig für eine Beschädigung der Daten, die zur Reparatur offline geschaltet werden das System benötigen. Obwohl seltenen, wenn eine Beschädigung auftritt, retten ReFS implementiert ein Feature, das beschädigten Daten aus dem Namespace auf einem live Volume entfernt und wird sichergestellt, dass eine gute Daten durch nicht repariert werden beschädigte Daten nicht beeinträchtigt werden. Das Feature Restwert anwenden und Isolieren von Beschädigung der Daten zu Exchange Online-Datenbank-Volumes bedeutet, dass wir nicht betroffenen Datenbanken auf einen beschädigten Datenträger fehlerfrei zwischen dem Zeitpunkt der Beschädigung und Reparieren Aktion weiter können. Dadurch wird die Verfügbarkeit von Datenbanken, die normalerweise durch eine solche Datenträger Beschädigung Probleme beeinträchtigt werden würde erhöht. 