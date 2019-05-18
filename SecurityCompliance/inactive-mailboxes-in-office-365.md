---
title: Übersicht über inaktive Postfächer in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 1fbd74e8-7a60-4157-afe8-fe79f05d2038
description: In diesem Artikel erfahren Sie, wie Sie Postfachinhalte für frühere Mitarbeiter beibehalten, indem Sie das Postfach in ein inaktives Postfach umwandeln. Sie können dies tun, indem Sie das Postfach in einem Beweissicherungsverfahren platzieren oder eine Office 365-Aufbewahrungsrichtlinie auf das Postfach anwenden und dann das entsprechende Office 365 Konto entfernen.
ms.openlocfilehash: 58bcc888af0d1ae92cf9d86e116fe287e7c2316c
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152717"
---
# <a name="overview-of-inactive-mailboxes-in-office-365"></a>Übersicht über inaktive Postfächer in Office 365

In Ihrer Organisation müssen möglicherweise die e-Mails der ehemaligen Mitarbeiter aufbewahrt werden, nachdem Sie die Organisation verlassen haben. Abhängig von den Aufbewahrungsanforderungen Ihrer Organisation müssen Sie möglicherweise Postfachinhalte für einige Monate oder Jahre nach Beendigung der Arbeit aufbewahren, oder Sie müssen möglicherweise den Postfachinhalt auf unbestimmte Zeit aufbewahren. Unabhängig davon, wie lange Sie e-Mails aufbewahren müssen, können Sie inaktive Postfächer in Office 365 erstellen, um das Postfach ehemaliger Mitarbeiter beizubehalten. 
  
## <a name="what-are-inactive-mailboxes"></a>Was sind inaktive Postfächer?

Wenn ein Mitarbeiter Ihre Organisation verlässt (oder ein längerer Abwesenheits beurlaub), können Sie Ihr Office 365 Konto entfernen. Die Postfachdaten des Mitarbeiters werden 30 Tage lang aufbewahrt, nachdem das Konto entfernt wurde. Während dieses Zeitraums können Sie die Postfachdaten weiterhin wiederherstellen, indem Sie das Löschen des Kontos Aufhebung. Nach 30 Tagen werden die Daten endgültig entfernt.
  
Wenn Ihre Organisation jedoch Postfachinhalte für frühere Mitarbeiter aufbewahren muss, können Sie das Postfach in ein inaktives Postfach umwandeln, indem Sie das Beweissicherungsverfahren für das Postfach aktivieren oder eine Office 365-Aufbewahrungsrichtlinie auf das Postfach im Security & Compliance Center anwenden. und dann das entsprechende Office 365 Konto entfernen. Der Inhalt eines inaktiven Postfachs wird für die Dauer des für das Postfach aktivierten Beweissicherungsverfahrens oder des Aufbewahrungszeitraums der Office 365-Aufbewahrungsrichtlinie aufbewahrt, die vor dem Löschen des Postfachs auf dieses angewendet wurde. Sie können das entsprechende Benutzerkonto innerhalb eines Zeitraums von 30 Tagen wiederherstellen. Nach 30 Tagen wird das inaktive Postfach jedoch in Office 365 aufbewahrt, bis die Aufbewahrungs-oder Aufbewahrungsrichtlinie entfernt wird. 
  
> [!NOTE]
> Wir haben den Stichtag (1. Juli 2017) zum Erstellen von neuem In-Situ-Speicher, um ein Postfach als inaktiv zu markieren, nach hinten verlegt. Ende dieses Jahres oder Anfang des nächsten Jahres können Sie keinen neuen In-Situ-Speicher in Exchange Online mehr erstellen. Es können dann nur noch das Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Vorhandene inaktive Postfächer, die sich im In-Situ-Speicher befinden, werden jedoch weiterhin unterstützt, und Sie können weiterhin die In-Situ-Speicher für inaktive Postfächer verwalten. Dazu zählen das Ändern der Dauer eines In-Situ-Speichers sowie das dauerhafte Löschen eines inaktiven Postfachs durch Entfernen des In-Situ-Speichers. 
 
  
## <a name="inactive-mailboxes-and-office-365-retention-policies"></a>Inaktive Postfächer und Office 365-Aufbewahrungsrichtlinien

Zusätzlich zum Beweissicherungsverfahren ist die Verwendung des neuen Office 365-Aufbewahrungsrichtlinien Features im Security & Compliance Center eine weitere Möglichkeit, ein Postfach inaktiv zu machen. Um ein Postfach mithilfe einer Aufbewahrungsrichtlinie als inaktiv festzulegen, müssen Sie wie folgt vorgehen: 
  
- Die Richtlinie muss auf Exchange-Postfächer oder Skype for Business-Speicherorte angewendet werden (da Skype-bezogene Inhalte im Postfach des Benutzers gespeichert werden). 
    
- Es muss so konfiguriert werden, dass Inhalte beibehalten oder beibehalten und dann gelöscht werden. Wenn eine Aufbewahrungsrichtlinie so konfiguriert ist, dass Inhalte lediglich gelöscht werden, wird ein Postfach, auf das die Richtlinie angewendet wurde, beim Löschen des Postfachs nicht inaktiv.
    
- Sie kann abfragebasiert sein, sodass nur Elemente aufbewahrt werden, die einer Suchabfrage entsprechen. 
    
Weitere Informationen zum Konfigurieren von Office 365-Aufbewahrungsrichtlinien finden Sie unter [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md).
  
Wenn Sie eine Aufbewahrungsrichtlinie verwenden, um ein inaktives Postfach zu erstellen, werden Office 365 die Aufbewahrungsrichtlinie für das inaktive Postfach weiterverarbeiten. Dies bedeutet Folgendes: Wenn die Aufbewahrungsrichtlinie so konfiguriert ist, das Inhalte aufbewahrt und anschließend gelöscht werden, werden Elemente in den Ordner „Wiederherstellbare Elemente" verschoben, wenn die Aufbewahrungsdauer abläuft, und schließlich aus dem inaktiven Postfach gelöscht. Wenn die Office 365-Aufbewahrungsrichtlinie nicht so konfiguriert ist, das Elemente gelöscht werden, werden Elemente, die vom Benutzer nicht endgültig gelöscht wurden (bevor das Postfach als inaktiv festgelegt wurde), nicht in den „Wiederherstellbare Elemente" verschoben, sondern unbegrenzt aufbewahrt, nachdem das Postfach als inaktiv festgelegt wurde. 
  
Sie können auch eine Office 365-Aufbewahrungsrichtlinie speziell für inaktive Postfächer erstellen. Hier sind einige Gründe dafür und Punkte, die Sie beachten sollten.
  
- Sie können die Aufbewahrungsrichtlinie so konfigurieren, dass Postfachinhalte nur so lange aufbewahrt werden, wie erforderlich ist, um die Anforderungen Ihrer Organisation in Bezug auf ehemalige Mitarbeiter zu erfüllen.
    
- Es ist eine gute Möglichkeit, inaktive Postfächer zu identifizieren, da die Aufbewahrungsrichtlinie nur auf inaktive Postfächer angewendet wird.
    
- Sie können die Aufbewahrungsrichtlinie, die inaktiven Postfächern in Ihrer Organisation zugewiesen ist, schnell identifizieren. Dadurch wird die Änderung der Aufbewahrungs- (oder Lösch-)einstellungen bei Bedarf erleichtert. Außerdem wird es einfacher, ein inaktives Postfach endgültig zu löschen, da Sie es einfach mithilfe des Security & Compliance Center aus der Richtlinie entfernen können. Andernfalls müssen Sie Exchange Online PowerShell verwenden, um ein Beweissicherungsverfahren aus einem inaktiven Postfach zu entfernen oder mithilfe von Security & Compliance Center PowerShell ein inaktives Postfach aus einer organisationsweiten Office 365-Aufbewahrungsrichtlinie auszuschließen.
    
- Wenn Sie eine Office 365-Aufbewahrungsrichtlinie speziell für inaktive Postfächer erstellen, können Sie der Richtlinie maximal 1.000 Postfächer hinzufügen. In einer sehr großen Organisation müssen Sie möglicherweise mehrere Office 365-Aufbewahrungsrichtlinien für inaktive Postfächer erstellen.

> [!CAUTION]
> Wenn Sie eine Aufbewahrungsrichtlinie verwenden, um ein Postfach inaktiv zu machen, ändern oder entfernen Sie den Benutzerprinzipalnamen (User Principal Name, UPN) für das Postfach nicht, bevor Sie das entsprechende Office 365 Benutzerkonto löschen. Ändern Sie außerdem nicht die primäre SMTP-Adresse (die vom UPN abgeleitet ist), oder entfernen Sie diese e-Mail-Adresse aus der Liste der sekundären SMTP-Adressen, die dem Postfach zugeordnet sind, bevor Sie das Postfach inaktiv machen. Wenn Sie die UPN-oder e-Mail-Adressen ändern (die dem Postfach zugewiesen wurden, als die Aufbewahrungsrichtlinie angewendet wurde), und dann das Benutzerkonto löschen, um das Postfach inaktiv zu machen, können Sie das inaktive Postfach nicht löschen, wenn Sie die i-Funktion nicht mehr beibehalten müssen. t. Das liegt daran, dass Sie das inaktive Postfach nicht mithilfe eines UPN oder einer e-Mail-Adresse (zur Identifizierung des inaktiven Postfachs) aus der Aufbewahrungsrichtlinie entfernen können, die sich von denen unterscheidet, die beim anfänglichen anwenden der Aufbewahrungsrichtlinie auf das Postfach vorhanden waren. Weitere Informationen zum Löschen inaktiver Postfächer finden Sie unter [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md).
  
## <a name="inactive-mailboxes-and-ediscovery-case-holds"></a>Inaktive Postfächer und eDiscovery-Fallspeicher

Wenn ein Haltestatus, der einem eDiscovery-Fall im Security & Compliance Center zugeordnet ist, in einem Postfach gespeichert wird und das Postfach oder das Office 365 Konto des Benutzers gelöscht wird, wird das Postfach zu einem inaktiven Postfach. Die Verwendung von eDiscovery-Fallspeichern zum Festlegen eines Postfachs als inaktiv wird jedoch nicht empfohlen. Grund hierfür ist, dass eDiscovery-Fälle für bestimmte zeitgebundene Fälle im Zusammenhang mit einem rechtlichen Problem vorgesehen sind. An einem bestimmten Punkt wird ein Rechtsfall wahrscheinlich enden, die dem Fall zugeordneten Speicherverfahren werden entfernt, und der eDiscovery-Fall wird geschlossen. Wenn ein für ein inaktives Postfach festgelegtes Speicherverfahren einem eDiscovery-Fall zugeordnet ist und das Speicherverfahren anschließend aufgehoben oder der eDiscovery-Fall geschlossen (oder gelöscht) wird, wird das inaktive Postfach endgültig gelöscht. Außerdem können Sie keinen zeitbasierten eDiscovery-Fallspeicher erstellen. Dies bedeutet, dass der Inhalt eines inaktiven Postfachs für immer aufbewahrt wird oder bis das Speicherverfahren aufgehoben und das inaktive Postfach gelöscht wird. Daher empfehlen wir die Verwendung eines Beweissicherungsverfahrens oder einer Office 365-Aufbewahrungsrichtlinie für inaktive Postfächer.
  
Weitere Informationen zu eDiscovery-Fällen und-Haltestatus finden Sie unter [eDiscovery Cases](ediscovery-cases.md).
  
## <a name="inactive-mailboxes-and-office-365-labels"></a>Inaktive Postfächer und Office 365-Bezeichnungen

Bezeichnungen in Office 365 unterstützen Sie beim Klassifizieren von E-Mail-Daten in Ihrer Organisation für Governance und beim Erzwingen von Aufbewahrungsregeln auf Basis dieser Klassifikation. Eine Bezeichnung kann entweder manuell von Benutzern oder automatisch von Administratoren auf ein E-Mail-Element angewendet werden, und einem E-Mail-Element kann nur eine Bezeichnung zugewiesen werden. Wenn einem einzelnen E-Mail-Element im Postfach eines Benutzers eine Bezeichnung zugewiesen ist und das Postfach oder das Office 365-Konto des Benutzers gelöscht wird, wird das Postfach zu einem inaktiven Postfach. Ähnlich wie bei eDiscovery-Fallspeichern wird auch die Verwendung von Bezeichnungen nicht empfohlen, um ein Postfach als inaktiv festzulegen. Stattdessen wird empfohlen, ein Beweissicherungsverfahren oder eine Office 365-Aufbewahrungsrichtlinie zu verwenden. Beachten Sie, dass Sie im Fall von Bezeichnungen möglicherweise nicht erkennen, dass eine Bezeichnung auf ein E-Mail-Element angewendet wurde, und dann ein Postfach versehentlich als inaktiv festlegen, wenn Sie das Konto des Benutzers löschen. 
  
Weitere Informationen über Bezeichnungen finden Sie unter [Übersicht über Bezeichnungen](labels.md).
  
## <a name="inactive-mailboxes-and-exchange-mrm-retention-policies"></a>Inaktive Postfächer und Exchange MRM-Aufbewahrungsrichtlinien

Wenn eine Exchange-Aufbewahrungsrichtlinie (die Messaging-Datensatzverwaltung oder das MRM-Feature in Exchange Online) auf das Postfach angewendet wurde, als es inaktiv wurde, werden alle Löschrichtlinien (die mit einer **Lösch** Aufbewahrungsaktion konfiguriert sind) gelöscht. Weiterverarbeitung für das inaktive Postfach. Mit einer Löschrichtlinie markierte Elemente werden demnach in den Ordner „Wiederherstellbare Elemente" verschoben, wenn der Aufbewahrungszeitraum abläuft. Diese Elemente werden aus dem inaktiven Postfach gelöscht, wenn die Aufbewahrungsdauer abläuft. Wenn keine Aufbewahrungsdauer für das inaktive Postfach angegeben wurde, werden Elemente im Ordner „Wiederherstellbare Elemente" unbegrenzt aufbewahrt. 
  
Umgekehrt werden Archivrichtlinien (hierbei handelt es sich um Aufbewahrungstags, für die die Aufbewahrungsaktion **MoveToArchive** konfiguriert ist) ignoriert, die in der einem inaktiven Postfach zugewiesenen Aufbewahrungsrichtlinie enthalten sind. Elemente in einem inaktiven Postfach, die mit einer Archivrichtlinie markiert sind, verbleiben demnach im primären Postfach, wenn der Aufbewahrungszeitraum abläuft. Sie werden nicht in das Archivpostfach oder in den Ordner „Wiederherstellbare Elemente" im Archivpostfach verschoben. Sie werden unbegrenzt aufbewahrt. 
  
## <a name="creating-an-inactive-mailbox"></a>Erstellen eines inaktiven Postfachs

Um ein Postfach als inaktiv festzulegen, muss dem Postfach eine Exchange Online-Lizenz (Plan 2) zugewiesen sein, sodass ein Beweissicherungsverfahren oder eine Office 365-Aufbewahrungsrichtlinie auf das Postfach angewendet werden kann, bevor es gelöscht wird. Nachdem das Postfach gelöscht wurde, ist die ihm zugeordnete Exchange Online Lizenz verfügbar, die einem neuen Benutzer zugewiesen werden kann. Für inaktive Postfächer sind keine laufenden Lizenzen erforderlich.
  
Die folgende Tabelle enthält eine Übersicht über das Verfahren, mit dem ein inaktives Postfach in verschiedenen Aufbewahrungsszenarios erstellt wird. Weitere Informationen finden Sie unter [Verwalten inaktiver Postfächer in Office 365](create-and-manage-inactive-mailboxes.md).
  
|**Ziel**|**Vorgehensweise**|**Ergebnis**|
|:-----|:-----|:-----|
|Aufbewahren des Postfachinhalts für unbegrenzte Zeit, nachdem ein Mitarbeiter die Organisation verlassen hat  <br/> | Aktivieren Sie das Beweissicherungsverfahren für das Postfach, oder wenden Sie eine Office 365-Aufbewahrungsrichtlinie auf das Postfach an.  <br/>  Geben Sie keine Aufbewahrungsdauer für das Beweissicherungsverfahren an, bzw. konfigurieren Sie die Office 365-Aufbewahrungsrichtlinie nicht für das Löschen von Elementen; alternativ können Sie eine Aufbewahrungsrichtlinie verwenden, die Elemente unbegrenzt aufbewahrt.  <br/>  Sie entfernen das Office 365-Konto des Benutzers.  <br/> |Der gesamte Inhalt des inaktiven Postfachs, einschließlich der Elemente im Ordner "Wiederherstellbare Elemente", wird unbegrenzt aufbewahrt.  <br/> |
|Aufbewahren des Postfachinhalts für einen bestimmten Zeitraum nach dem Ausscheiden des Mitarbeiters und anschließendes Löschen  <br/> | Wenden Sie eine Office 365-Aufbewahrungsrichtlinie auf das Postfach an.  <br/>  Konfigurieren Sie die Aufbewahrungsrichtlinie so, dass Elemente beibehalten und dann gelöscht werden, wenn der Aufbewahrungszeitraum abgelaufen ist.  <br/>  Sie entfernen das Office 365-Konto des Benutzers.  <br/> |Wenn der Aufbewahrungszeitraum für ein Postfachelement abläuft, wird das Element in den Ordner "Wiederherstellbare Elemente" verschoben und dann endgültig aus dem inaktiven Postfach gelöscht, wenn der Aufbewahrungszeitraum für gelöschte Elemente (für Exchange-Postfächer) abgelaufen ist. Der Aufbewahrungszeitraum der Office 365-Aufbewahrungsrichtlinie kann basierend auf dem ursprünglichen Datum, an dem ein Postfachelement empfangen oder erstellt wurde, oder nach der letzten Änderung konfiguriert werden.  <br/> |
   
**Hinweis:** Wenn bereits ein Beweissicherungsverfahren für ein Postfach erteilt wurde oder wenn bereits eine Office 365 Aufbewahrungsrichtlinie angewendet wurde, müssen Sie lediglich das entsprechende Office 365 Benutzerkonto löschen, um ein inaktives Postfach zu erstellen. 
  
## <a name="managing-inactive-mailboxes"></a>Verwalten inaktiver Postfächer

Nachdem Sie ein Postfach als inaktiv festgelegt haben, können Sie verschiedene Verwaltungsaufgaben für inaktive Postfächer ausführen.
  
- **Ändern der Aufbewahrungsdauer für ein inaktives Postfach** Nachdem ein Postfach als inaktiv festgelegt wurde, können Sie die Aufbewahrungsdauer des Beweissicherungsverfahrens oder der auf das inaktive Postfach angewendeten Office 365-Aufbewahrungsrichtlinie ändern. Eine schrittweise Anleitung finden Sie unter [Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).

  > [!NOTE]
  > Andere Aufbewahrungsrichtlinien können nicht auf ein inaktives Postfach angewendet werden. Sie können nur die Aufbewahrungsdauer einer vorhandenen Aufbewahrungsrichtlinie ändern, die auf das inaktive Postfach angewendet wird.
    
- **Wiederherstellen eines inaktiven Postfachs** Wenn ein ehemaliger (oder für längere Zeit freigestellter) Mitarbeiter in Ihre Organisation zurückkehrt oder ein neuer Mitarbeiter eingestellt wird, der die Zuständigkeiten des ehemaligen Mitarbeiters übernimmt, können Sie den Inhalt des inaktiven Postfachs wiederherstellen. Wenn Sie ein inaktives Postfach wiederherstellen, wird das Postfach in ein neues Postfach umgewandelt, wobei Inhalt und Ordnerstruktur des inaktiven Postfachs beibehalten werden und das Postfach mit einem neuen Benutzerkonto verknüpft wird. Nach der Wiederherstellung ist das inaktive Postfach nicht mehr vorhanden. Schritt-für-Schritt-Verfahren und Informationen dazu, was geschieht, wenn Sie ein inaktives Postfach wiederherstellen, finden Sie unter [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md).
    
- **Wiederherstellen eines** inaktiven Postfachs Wenn ein anderer Mitarbeiter die Aufgaben eines ehemaligen Mitarbeiters übernimmt oder eine andere Person Zugriff auf die Inhalte des inaktiven Postfachs benötigt, können Sie den Inhalt des inaktiven Postfachs in einem vorhandenen Postfach wiederherstellen (oder zusammenführen). Wenn Sie ein inaktives Postfach wiederherstellen, werden die Inhalte in ein anderes Postfach kopiert. Das inaktive Postfach wird beibehalten und bleibt ein inaktives Postfach. Das inaktive Postfach kann weiterhin mithilfe von eDiscovery-Tools durchsucht werden, dessen Inhalt kann in einem anderen Postfach wiederhergestellt werden, und es kann zu einem späteren Zeitpunkt wiederhergestellt oder gelöscht werden. Eine schrittweise Anleitung finden Sie unter [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md).
    
- **Löschen eines** inaktiven Postfachs Wenn Sie den Inhalt eines inaktiven Postfachs nicht mehr aufbewahren müssen, können Sie ihn dauerhaft löschen, indem Sie alle Haltestatus oder Office 365 auf das inaktives Postfach angewendeten Aufbewahrungsrichtlinien entfernen. Wenn ein Postfach vor mehr als 30 Tagen inaktiv gemacht wurde, wird es für die dauerhafte Löschung markiert, nachdem Sie den Haltebereich entfernt haben. Wenn das Postfach innerhalb der letzten 30 Tage inaktiv gemacht wurde, können Sie es erneut aktivieren, nachdem Sie die Aufbewahrungs-oder Aufbewahrungsrichtlinie entfernt haben. Eine schrittweise Anleitung finden Sie unter [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md).