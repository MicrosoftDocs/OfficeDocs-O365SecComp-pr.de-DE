---
title: Übersicht über inaktive Postfächer in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
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
description: Erfahren Sie mehr über das Aufbewahren von Postfachinhalten für ehemalige Mitarbeiter, indem Sie das Postfach in ein inaktives Postfach umwandeln. Sie können dies tun, indem Sie das Postfach für die Beweissicherung festlegen oder eine Office 365-Aufbewahrungsrichtlinie auf das Postfach anwenden und dann das entsprechende Office 365-Konto entfernen.
ms.openlocfilehash: 19cd2bafc1f4bf0b6aa3b4c0332a3588ace3e5d8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256523"
---
# <a name="overview-of-inactive-mailboxes-in-office-365"></a>Übersicht über inaktive Postfächer in Office 365

Ihre Organisation muss möglicherweise die e-Mails ehemaliger Mitarbeiter beibehalten, nachdem Sie die Organisation verlassen haben. Je nach den Aufbewahrungsanforderungen Ihrer Organisation müssen Sie möglicherweise den Postfachinhalt für einige Monate oder Jahre nach Beendigung der Beschäftigung beibehalten, oder Sie müssen den Postfachinhalt unbegrenzt aufbewahren. Unabhängig davon, wie lange e-Mails aufbewahrt werden müssen, können Sie inaktive Postfächer in Office 365 erstellen, um das Postfach ehemaliger Mitarbeiter beizubehalten. 
  
## <a name="what-are-inactive-mailboxes"></a>Was sind inaktive Postfächer?

Wenn ein Mitarbeiter Ihre Organisation verlässt (oder länger abwesend ist), können Sie dessen Office 365-Konto entfernen. Die Postfachdaten des Mitarbeiters werden 30 Tage lang aufbewahrt, nachdem das Konto entfernt wurde. Während dieses Zeitraums können Sie die Postfachdaten weiterhin wiederherstellen, indem Sie das Löschen des Kontos Aufhebung. Nach 30 Tagen werden die Daten dauerhaft entfernt.
  
Wenn Ihre Organisation jedoch Postfachinhalte für frühere Mitarbeiter aufbewahren muss, können Sie das Postfach in ein inaktives Postfach umwandeln, indem Sie für das Postfach ein Beweissicherungsverfahren festlegen oder eine Office 365-Aufbewahrungsrichtlinie auf das Postfach im Security & Compliance Center anwenden. und dann das entsprechende Office 365-Konto entfernen. Der Inhalt eines inaktiven Postfachs wird für die Dauer des für das Postfach aktivierten Beweissicherungsverfahrens oder des Aufbewahrungszeitraums der Office 365-Aufbewahrungsrichtlinie aufbewahrt, die vor dem Löschen des Postfachs auf dieses angewendet wurde. Sie können das entsprechende Benutzerkonto innerhalb eines Zeitraums von 30 Tagen wiederherstellen. Nach 30 Tagen wird das inaktive Postfach jedoch in Office 365 aufbewahrt, bis die Aufbewahrungsrichtlinie entfernt wurde. 
  
> [!NOTE]
> Wir haben den Stichtag (1. Juli 2017) zum Erstellen von neuem In-Situ-Speicher, um ein Postfach als inaktiv zu markieren, nach hinten verlegt. Ende dieses Jahres oder Anfang des nächsten Jahres können Sie keinen neuen In-Situ-Speicher in Exchange Online mehr erstellen. Es können dann nur noch das Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Vorhandene inaktive Postfächer, die sich im In-Situ-Speicher befinden, werden jedoch weiterhin unterstützt, und Sie können weiterhin die In-Situ-Speicher für inaktive Postfächer verwalten. Dazu zählen das Ändern der Dauer eines In-Situ-Speichers sowie das dauerhafte Löschen eines inaktiven Postfachs durch Entfernen des In-Situ-Speichers. 
 
  
## <a name="inactive-mailboxes-and-office-365-retention-policies"></a>Inaktive Postfächer und Office 365-Aufbewahrungsrichtlinien

Zusätzlich zur Beweissicherung ist die Verwendung des neuen Office 365-Aufbewahrungsrichtlinien Features im Security & Compliance Center eine weitere Möglichkeit, um ein Postfach zu deaktivieren. Um ein Postfach mithilfe einer Aufbewahrungsrichtlinie als inaktiv festzulegen, müssen Sie wie folgt vorgehen: 
  
- Die Richtlinie muss auf Exchange-Postfächer oder Skype for Business-Speicherorte angewendet werden (da Skype-bezogene Inhalte im Postfach des Benutzers gespeichert werden). 
    
- Es muss so konfiguriert werden, dass Inhalte aufbewahrt oder aufbewahrt und dann gelöscht werden. Wenn eine Aufbewahrungsrichtlinie so konfiguriert ist, dass Inhalte lediglich gelöscht werden, wird ein Postfach, auf das die Richtlinie angewendet wurde, beim Löschen des Postfachs nicht inaktiv.
    
- Sie kann abfragebasiert sein, sodass nur Elemente aufbewahrt werden, die einer Suchabfrage entsprechen. 
    
Weitere Informationen zum Konfigurieren von Office 365-Aufbewahrungsrichtlinien finden Sie unter [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md).
  
Wenn Sie eine Aufbewahrungsrichtlinie für ein inaktives Postfach verwenden, verarbeitet Office 365 weiterhin die Aufbewahrungsrichtlinie für das inaktive Postfach. Dies bedeutet Folgendes: Wenn die Aufbewahrungsrichtlinie so konfiguriert ist, das Inhalte aufbewahrt und anschließend gelöscht werden, werden Elemente in den Ordner „Wiederherstellbare Elemente" verschoben, wenn die Aufbewahrungsdauer abläuft, und schließlich aus dem inaktiven Postfach gelöscht. Wenn die Office 365-Aufbewahrungsrichtlinie nicht so konfiguriert ist, das Elemente gelöscht werden, werden Elemente, die vom Benutzer nicht endgültig gelöscht wurden (bevor das Postfach als inaktiv festgelegt wurde), nicht in den „Wiederherstellbare Elemente" verschoben, sondern unbegrenzt aufbewahrt, nachdem das Postfach als inaktiv festgelegt wurde. 
  
Sie können auch eine Office 365-Aufbewahrungsrichtlinie speziell für inaktive Postfächer erstellen. Hier sind einige Gründe dafür und Punkte, die Sie beachten sollten.
  
- Sie können die Aufbewahrungsrichtlinie so konfigurieren, dass Postfachinhalte nur so lange aufbewahrt werden, wie erforderlich ist, um die Anforderungen Ihrer Organisation in Bezug auf ehemalige Mitarbeiter zu erfüllen.
    
- Es ist eine gute Möglichkeit, inaktive Postfächer zu identifizieren, da die Aufbewahrungsrichtlinie nur auf inaktive Postfächer angewendet wird.
    
- Sie können schnell die Aufbewahrungsrichtlinie identifizieren, die inaktiven Postfächern in Ihrer Organisation zugewiesen ist. Dadurch wird die Änderung der Aufbewahrungs- (oder Lösch-)einstellungen bei Bedarf erleichtert. Außerdem ist es einfacher, ein inaktives Postfach dauerhaft zu löschen, da Sie es einfach mithilfe des Security & Compliance Center aus der Richtlinie entfernen können. Andernfalls müssen Sie Exchange Online PowerShell verwenden, um ein inaktives Postfach zu entfernen oder ein inaktives Postfach mithilfe von Security & Compliance Center PowerShell aus einer organisationsweiten Office 365-Aufbewahrungsrichtlinie auszuschließen.
    
- Wenn Sie eine Office 365-Aufbewahrungsrichtlinie speziell für inaktive Postfächer erstellen, können Sie der Richtlinie maximal 1.000 Postfächer hinzufügen. In einer sehr großen Organisation müssen Sie möglicherweise mehrere Office 365-Aufbewahrungsrichtlinien für inaktive Postfächer erstellen.

> [!CAUTION]
> Wenn Sie eine Aufbewahrungsrichtlinie verwenden, um ein Postfach zu deaktivieren, ändern oder entfernen Sie den Benutzerprinzipalnamen (UPN) für das Postfach nicht, bevor Sie das entsprechende Office 365-Benutzerkonto löschen. Ändern Sie außerdem nicht die primäre SMTP-Adresse (die vom UPN abgeleitet ist), oder entfernen Sie diese e-Mail-Adresse aus der Liste der sekundären SMTP-Adressen, die dem Postfach zugeordnet sind, bevor Sie das Postfach inaktiv machen. Wenn Sie die UPN-oder e-Mail-Adressen (die dem Postfach zugewiesen waren, als die Aufbewahrungsrichtlinie darauf angewendet wurde) ändern und dann das Benutzerkonto löschen, um das Postfach zu deaktivieren, können Sie das inaktive Postfach nicht mehr löschen, wenn Sie i t. Das liegt daran, dass Sie das inaktive Postfach nicht aus der Aufbewahrungsrichtlinie entfernen können, indem Sie einen UPN oder eine e-Mail-Adresse verwenden (um das inaktive Postfach zu identifizieren), die sich von denen unterscheidet, die beim ersten anwenden der Aufbewahrungsrichtlinie auf das Postfach vorhanden waren. Weitere Informationen zum Löschen inaktiver Postfächer finden Sie unter [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md).
  
## <a name="inactive-mailboxes-and-ediscovery-case-holds"></a>Inaktive Postfächer und eDiscovery-Fallspeicher

Wenn ein Haltebereich, der einem eDiscovery-Fall im Security & Compliance Center zugeordnet ist, in einem Postfach gespeichert wird und dann das Postfach oder das Office 365-Konto des Benutzers gelöscht wird, wird das Postfach zu einem inaktiven Postfach. Die Verwendung von eDiscovery-Fallspeichern zum Festlegen eines Postfachs als inaktiv wird jedoch nicht empfohlen. Grund hierfür ist, dass eDiscovery-Fälle für bestimmte zeitgebundene Fälle im Zusammenhang mit einem rechtlichen Problem vorgesehen sind. An einem bestimmten Punkt wird ein Rechtsfall wahrscheinlich enden, die dem Fall zugeordneten Speicherverfahren werden entfernt, und der eDiscovery-Fall wird geschlossen. Wenn ein für ein inaktives Postfach festgelegtes Speicherverfahren einem eDiscovery-Fall zugeordnet ist und das Speicherverfahren anschließend aufgehoben oder der eDiscovery-Fall geschlossen (oder gelöscht) wird, wird das inaktive Postfach endgültig gelöscht. Außerdem können Sie keinen zeitbasierten eDiscovery-Fallspeicher erstellen. Dies bedeutet, dass der Inhalt eines inaktiven Postfachs für immer aufbewahrt wird oder bis das Speicherverfahren aufgehoben und das inaktive Postfach gelöscht wird. Daher empfehlen wir die Verwendung eines Beweissicherungsverfahrens oder einer Office 365-Aufbewahrungsrichtlinie für inaktive Postfächer.
  
Weitere Informationen zu eDiscovery-Fällen und-Haltebereichen finden Sie unter [eDiscovery Cases](ediscovery-cases.md).
  
## <a name="inactive-mailboxes-and-office-365-labels"></a>Inaktive Postfächer und Office 365-Bezeichnungen

Bezeichnungen in Office 365 unterstützen Sie beim Klassifizieren von E-Mail-Daten in Ihrer Organisation für Governance und beim Erzwingen von Aufbewahrungsregeln auf Basis dieser Klassifikation. Eine Bezeichnung kann entweder manuell von Benutzern oder automatisch von Administratoren auf ein E-Mail-Element angewendet werden, und einem E-Mail-Element kann nur eine Bezeichnung zugewiesen werden. Wenn einem einzelnen E-Mail-Element im Postfach eines Benutzers eine Bezeichnung zugewiesen ist und das Postfach oder das Office 365-Konto des Benutzers gelöscht wird, wird das Postfach zu einem inaktiven Postfach. Ähnlich wie bei eDiscovery-Fallspeichern wird auch die Verwendung von Bezeichnungen nicht empfohlen, um ein Postfach als inaktiv festzulegen. Stattdessen wird empfohlen, ein Beweissicherungsverfahren oder eine Office 365-Aufbewahrungsrichtlinie zu verwenden. Beachten Sie, dass Sie im Fall von Bezeichnungen möglicherweise nicht erkennen, dass eine Bezeichnung auf ein E-Mail-Element angewendet wurde, und dann ein Postfach versehentlich als inaktiv festlegen, wenn Sie das Konto des Benutzers löschen. 
  
Weitere Informationen über Bezeichnungen finden Sie unter [Übersicht über Bezeichnungen](labels.md).
  
## <a name="inactive-mailboxes-and-exchange-mrm-retention-policies"></a>Inaktive Postfächer und Exchange MRM-Aufbewahrungsrichtlinien

Wenn eine Exchange-Aufbewahrungsrichtlinie (Messaging Records Management oder MRM, Feature in Exchange Online) auf das Postfach angewendet wurde, als es inaktiv wurde, werden alle Löschrichtlinien (die Aufbewahrungstags, die mit einer Aufbewahrungsaktion für das **Löschen** konfiguriert sind) weiterhin für das inaktive Postfach verarbeitet werden. Mit einer Löschrichtlinie markierte Elemente werden demnach in den Ordner „Wiederherstellbare Elemente" verschoben, wenn der Aufbewahrungszeitraum abläuft. Diese Elemente werden aus dem inaktiven Postfach gelöscht, wenn die Aufbewahrungsdauer abläuft. Wenn keine Aufbewahrungsdauer für das inaktive Postfach angegeben wurde, werden Elemente im Ordner „Wiederherstellbare Elemente" unbegrenzt aufbewahrt. 
  
Umgekehrt werden Archivrichtlinien (hierbei handelt es sich um Aufbewahrungstags, für die die Aufbewahrungsaktion **MoveToArchive** konfiguriert ist) ignoriert, die in der einem inaktiven Postfach zugewiesenen Aufbewahrungsrichtlinie enthalten sind. Elemente in einem inaktiven Postfach, die mit einer Archivrichtlinie markiert sind, verbleiben demnach im primären Postfach, wenn der Aufbewahrungszeitraum abläuft. Sie werden nicht in das Archivpostfach oder in den Ordner „Wiederherstellbare Elemente" im Archivpostfach verschoben. Sie werden unbegrenzt aufbewahrt. 
  
## <a name="creating-an-inactive-mailbox"></a>Erstellen eines inaktiven Postfachs

Um ein Postfach als inaktiv festzulegen, muss dem Postfach eine Exchange Online-Lizenz (Plan 2) zugewiesen sein, sodass ein Beweissicherungsverfahren oder eine Office 365-Aufbewahrungsrichtlinie auf das Postfach angewendet werden kann, bevor es gelöscht wird. Nachdem das Postfach gelöscht wurde, kann die ihm zugeordnete Exchange Online-Lizenz einem neuen Benutzer zugewiesen werden. Für inaktive Postfächer sind keine laufenden Lizenzen erforderlich.
  
Die folgende Tabelle enthält eine Übersicht über das Verfahren, mit dem ein inaktives Postfach in verschiedenen Aufbewahrungsszenarios erstellt wird. Weitere Informationen finden Sie unter [Verwalten inaktiver Postfächer in Office 365](create-and-manage-inactive-mailboxes.md).
  
|**Ziel**|**Vorgehensweise**|**Ergebnis**|
|:-----|:-----|:-----|
|Aufbewahren des Postfachinhalts für unbegrenzte Zeit, nachdem ein Mitarbeiter die Organisation verlassen hat  <br/> | Aktivieren Sie das Beweissicherungsverfahren für das Postfach, oder wenden Sie eine Office 365-Aufbewahrungsrichtlinie auf das Postfach an.  <br/>  Geben Sie keine Aufbewahrungsdauer für das Beweissicherungsverfahren an, bzw. konfigurieren Sie die Office 365-Aufbewahrungsrichtlinie nicht für das Löschen von Elementen; alternativ können Sie eine Aufbewahrungsrichtlinie verwenden, die Elemente unbegrenzt aufbewahrt.  <br/>  Sie entfernen das Office 365-Konto des Benutzers.  <br/> |Alle Inhalte im inaktiven Postfach, einschließlich der Elemente im Ordner "Wiederherstellbare Elemente", werden unbegrenzt aufbewahrt.  <br/> |
|Aufbewahren des Postfachinhalts für einen bestimmten Zeitraum nach dem Ausscheiden des Mitarbeiters und anschließendes Löschen  <br/> | Wenden Sie eine Office 365-Aufbewahrungsrichtlinie auf das Postfach an.  <br/>  Konfigurieren Sie die Aufbewahrungsrichtlinie so, dass Elemente beibehalten und dann gelöscht werden, wenn der Aufbewahrungszeitraum abgelaufen ist.  <br/>  Sie entfernen das Office 365-Konto des Benutzers.  <br/> |Wenn der Aufbewahrungszeitraum für ein Postfachelement abläuft, wird das Element in den Ordner "Wiederherstellbare Elemente" verschoben und dann endgültig aus dem inaktiven Postfach gelöscht, wenn der Aufbewahrungszeitraum für gelöschte Elemente (für Exchange-Postfächer) abläuft. Die Aufbewahrungsdauer der Office 365-Aufbewahrungsrichtlinie kann basierend auf dem ursprünglichen Datum konfiguriert werden, an dem ein Postfachelement empfangen oder erstellt oder zuletzt geändert wurde.  <br/> |
   
**Hinweis:** Wenn für ein Postfach bereits eine Aufbewahrungspflicht gilt oder wenn bereits eine Office 365-Speicherrichtlinie darauf angewendet wurde, müssen Sie lediglich das entsprechende Office 365-Benutzerkonto löschen, um ein inaktives Postfach zu erstellen. 
  
## <a name="managing-inactive-mailboxes"></a>Verwalten inaktiver Postfächer

Nachdem Sie ein Postfach als inaktiv festgelegt haben, können Sie verschiedene Verwaltungsaufgaben für inaktive Postfächer ausführen.
  
- **Ändern der Aufbewahrungsdauer für ein inaktives Postfach** Nachdem ein Postfach als inaktiv festgelegt wurde, können Sie die Aufbewahrungsdauer des Beweissicherungsverfahrens oder der auf das inaktive Postfach angewendeten Office 365-Aufbewahrungsrichtlinie ändern. Schrittweise Anleitungen finden Sie unter [Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).

  > [!NOTE]
  > Sie können keine anderen Aufbewahrungsrichtlinien auf ein inaktives Postfach anwenden. Sie können nur die Aufbewahrungsdauer einer vorhandenen Aufbewahrungsrichtlinie ändern, die auf das inaktive Postfach angewendet wird.
    
- **Wiederherstellen eines inaktiven Postfachs** Wenn ein ehemaliger (oder für längere Zeit freigestellter) Mitarbeiter in Ihre Organisation zurückkehrt oder ein neuer Mitarbeiter eingestellt wird, der die Zuständigkeiten des ehemaligen Mitarbeiters übernimmt, können Sie den Inhalt des inaktiven Postfachs wiederherstellen. Wenn Sie ein inaktives Postfach wiederherstellen, wird das Postfach in ein neues Postfach umgewandelt, wobei Inhalt und Ordnerstruktur des inaktiven Postfachs beibehalten werden und das Postfach mit einem neuen Benutzerkonto verknüpft wird. Nach der Wiederherstellung ist das inaktive Postfach nicht mehr vorhanden. Schrittweise Anleitungen und Informationen dazu, was passiert, wenn Sie ein inaktives Postfach wiederherstellen, finden Sie unter [recover an Inactive Mailbox in Office 365](recover-an-inactive-mailbox.md).
    
- **Wiederherstellen eines** inaktiven Postfachs Wenn ein anderer Mitarbeiter die Aufgaben eines ehemaligen Mitarbeiters übernimmt oder eine andere Person Zugriff auf die Inhalte des inaktiven Postfachs benötigt, können Sie den Inhalt des inaktiven Postfachs in einem vorhandenen Postfach wiederherstellen (oder zusammenführen). Wenn Sie ein inaktives Postfach wiederherstellen, wird der Inhalt in ein anderes Postfach kopiert. Das inaktive Postfach wird beibehalten und bleibt ein inaktives Postfach. Das inaktive Postfach kann weiterhin mithilfe von eDiscovery-Tools durchsucht werden, dessen Inhalt in einem anderen Postfach wiederhergestellt und zu einem späteren Zeitpunkt wiederhergestellt oder gelöscht werden kann. Schrittweise Anleitungen finden Sie unter [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md).
    
- **Löschen eines** inaktiven Postfachs Wenn Sie den Inhalt eines inaktiven Postfachs nicht mehr beibehalten müssen, können Sie es dauerhaft löschen, indem Sie alle Haltestatus oder Office 365-Aufbewahrungsrichtlinien entfernen, die auf das inaktive Postfach angewendet werden. Wenn ein Postfach vor mehr als 30 Tagen inaktiv wurde, wird es nach dem Entfernen des Haltestatus dauerhaft gelöscht. Wenn das Postfach innerhalb der letzten 30 Tage inaktiv wurde, können Sie es wieder aktivieren, nachdem Sie die Aufbewahrungs-oder Beibehaltungsrichtlinie entfernt haben. Schrittweise Anleitungen finden Sie unter [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md).