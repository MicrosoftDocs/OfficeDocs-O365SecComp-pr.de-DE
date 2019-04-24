---
title: Automatisierte Untersuchung und Antwort (AIR) mit Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Erfahren Sie mehr über automatisierte Ermittlungs-und Antwortfunktionen in Office 365 Advanced Threat Protection.
ms.openlocfilehash: 223a28a7f63f101dd5644e433d72a3ddf6e5dc23
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32249866"
---
# <a name="automated-investigation-and-response-air-with-office-365"></a>Automatisierte Untersuchung und Antwort (AIR) mit Office 365

Automatisierte Untersuchung und Antwort (AIR) (demnächst in [Office 365 Threat Investigation and Response Capabilities](office-365-ti.md)) ermöglicht es Ihnen, automatisierte Untersuchungen und Korrekturen zu bekannten Bedrohungen durchzuführen, die es heute gibt. Lesen Sie diesen Artikel, um einen Überblick über die Luft zu erhalten und zu erfahren, wie Sie Ihren Organisationen und Sicherheitsteams helfen können, Bedrohungen effektiver und effizienter zu verringern. 

Weitere Informationen dazu, wann AIR-Funktionen verfügbar sind, finden Sie im [Microsoft 365-Fahrplan](https://www.microsoft.com/microsoft-365/roadmap).

## <a name="alerts"></a>Warnungen

[Warnungen](alert-policies.md#viewing-alerts) stellen Auslöser für Sicherheitsoperationen-Team Workflows für Vorfalls Reaktionen dar. Das Priorisieren des richtigen Warnungs Satzes zur Untersuchung, wobei sichergestellt ist, dass keine Bedrohungen unadressiert sind, ist eine Herausforderung. Wenn Untersuchungen zu Warnungen manuell durchgeführt werden, müssen Sicherheits Betriebsteams Entitäten (z. b. Inhalte, Geräte und Benutzer), die von Bedrohungen bedroht sind, aufspüren und korrelieren. Solche Aufgaben und Workflows sind sehr zeitaufwändig und beinhalten mehrere Tools und Systeme. Mit AIR werden Untersuchungen und Reaktionszeiten zu wichtigen Sicherheits-und Bedrohungs Verwaltungswarnungen automatisiert, die ihre Sicherheitsantwort-Manuskripte automatisch auslösen. 

In der ersten Freigabe von AIR im April 2019 werden Warnungen, die von den Warnungsrichtlinien für einzelne Ereignisse generiert werden, automatisch untersucht. 

1. Es wurde ein potenziell böswilliger URL-Klick erkannt
2. Vom Benutzer als Phishing gemeldete E-Mail *
3. Nach der Lieferung gelöschte e-Mail-Nachrichten mit Schadsoftware *
4. Nach der Lieferung entfernte e-Mail-Nachrichten mit Phishing-URLs *

***Hinweis**: diesen Warnungen wurde in den entsprechenden Warnungsrichtlinien innerhalb des Security _AMP_ Compliance Centers mit deaktivierten e-Mail-Benachrichtigungen eine "Information"-Schweregrad zugewiesen. Diese können über die Warnungsrichtlinien Konfiguration aktiviert werden.

Um Benachrichtigungen anzuzeigen, wählen Sie im Security & Compliance Center **Alerts** > **anzeigen**. Wählen Sie eine Warnung aus, um die Details anzuzeigen, und verwenden Sie dann den Link **untersuchUng anzeigen** , um zur entsprechenden [Untersuchung](#investigation-graph)zu wechseln. Beachten Sie, dass Informationswarnungen standardmäßig in der Warnungsansicht ausgeblendet werden. Um Sie anzuzeigen, müssen Sie die Warnungsfilterung so ändern, dass Sie Informationswarnungen enthält.

Wenn Ihre Organisation ihre Sicherheitswarnungen über ein Warnungsverwaltungssystem, ein Dienst Verwaltungssystem oder ein Informations-und Ereignisverwaltungssystem (Security Information and Event Management, SIEM) verwaltet, können Sie Office 365-Benachrichtigungen über eine e-Mail-Benachrichtigung oder über die [ Office 365-Verwaltungs Aktivitäts-API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). Die Benachrichtigung über Untersuchungen per e-Mail oder API enthält Links für den Zugriff auf die Warnungen im Security & Compliance Center, sodass der zugewiesene Sicherheitsadministrator schnell zu der Untersuchung navigieren kann.

![Warnungen, die auf Untersuchungen verweisen](media/air-alerts-page-details.png) 


## <a name="security-playbooks"></a>Sicherheits Manuskripte

Sicherheits Manuskripte sind Back-End-Richtlinien, die im Mittelpunkt der Automatisierung in Microsoft Threat Protection stehen. Die in AIR bereitgestellten Sicherheits Manuskripte basieren auf allgemeinen Sicherheitsszenarien in der Praxis. Ein Sicherheits Textbuch wird automatisch gestartet, wenn in Ihrer Organisation eine Warnung ausgelöst wird. Sobald die Warnung ausgelöst wird, wird das zugehörige Textbuch automatisch ausgeführt. Das Textbuch führt eine Untersuchung unter Berücksichtigung aller zugehörigen Metadaten durch (einschließlich e-Mail-Nachrichten, Benutzer, betreffs, Absender usw.). Basierend auf den Ergebnissen des Manuskripts empfiehlt AIR eine Reihe von Aktionen, die das Sicherheitsteam Ihrer Organisation ausführen kann, um die Bedrohung zu steuern und zu verringern. 

Die Sicherheits Manuskripte, die Sie mit AIR erhalten, wurden entwickelt, um die häufigsten Bedrohungen zu bewältigen, denen Organisationen heute gegenüberstehen. Sie basieren auf Eingaben aus Sicherheits-und Vorfall Reaktions Teams, einschließlich derer, die dazu beitragen, Microsoft und unsere Kunden zu schützen.

### <a name="security-playbooks-are-rolling-out-in-phases"></a>Sicherheits Manuskripte werden phasenweise ausgeführt

Als Teil von AIR werden Sicherheits Manuskripte phasenweise ausgeführt

- **Phase 1 (April 2019)**: Manuskripte bieten Empfehlungen für Aktionen, die von Sicherheitsadministratoren überprüft und genehmigt werden. 

- **Phase 2 (Post-June 2019)**: Textbuch-Verbesserungen, plus Sicherheitsadministratoren haben die Möglichkeit, Sicherheitshandbuchs so zu konfigurieren, dass einige Aktionen automatisch ohne administrative Interaktion ausgeführt werden.

Phase 1 umfasst die folgenden Manuskripte:
- Vom Benutzer gemeldete Phishing-Nachricht
- Änderung der URL-Click-Entscheidung 
- Nach der Bereitstellung erkannte Schadsoftware (Malware ZAP)
- Phishing-Erkennung nach der Lieferung ZAP (Phishing ZAP)
- Manuelle e-Mail-Untersuchungen (mit Threat Explorer)

Für Phase 2 sind mehrere andere Text Manuskripte geplant.

### <a name="playbooks-include-investigation-and-recommendations"></a>Manuskripte schließen Untersuchungen und Empfehlungen ein

Jedes Textbuch umfasst Folgendes: 
- eine Stamm Ermittlung, 
- Schritte zur Identifizierung und Korrelation anderer potenzieller Bedrohungen und 
- Empfohlene Maßnahmen zur Behebung von Bedrohungen.

Jeder allgemeine Schritt enthält viele unter Schritte, die ausgeführt werden, um eine umfassende, detaillierte und umfassende Antwort auf Bedrohungen bereitzustellen.

## <a name="example-a-user-reported-phish-message-launches-an-investigation-playbook"></a>Beispiel: eine vom Benutzer gemeldete Phishing-Nachricht startet ein Ermittlungs Manuskript

Wenn ein Benutzer in Ihrer Organisation eine e-Mail-Nachricht übermittelt und Microsoft mithilfe des [Berichtsnachrichten-Add-Ins für Outlook oder Outlook Web Access](enable-the-report-message-add-in.md)meldet, wird der Bericht auch an Ihr System gesendet und im Explorer der vom Benutzer gemeldeten Ansicht angezeigt. Diese vom Benutzer berichtete Meldung löst jetzt eine System basierte Informationswarnung aus, die das Ermittlungs Manuskript automatisch startet.

Während der Stamm Untersuchung werden verschiedene Aspekte der e-Mail ausgewertet. Zu diesen zählen:
- Eine Bestimmung darüber, welche Art von Bedrohung es sein könnte;
- Wer hat Sie gesendet?
- Absender der e-Mail (Sendeinfrastruktur)
- Ob andere Instanzen der e-Mail zugestellt oder blockiert wurden;
- Eine Bewertung durch unsere Analysten;
- Gibt an, ob die e-Mail bekannten Kampagnen zugeordnet ist;
- und vieles mehr.

Nach Abschluss der Stamm Prüfung stellt das Textbuch eine Liste der empfohlenen Aktionen für die ursprüngliche e-Mail und die zugehörigen Entitäten bereit.
  
Als nächstes werden mehrere Bedrohungs Ermittlungs-und-Jagd Schritte ausgeführt:

- Ähnliche e-Mails in anderen e-Mail-Clustern werden durchsucht.
- Das Signal wird für andere Plattformen wie [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection)freigegeben.
- Es wird festgelegt, ob Benutzer über böswillige Links in verdächtigen e-Mails geklickt haben.
- Eine Überprüfung erfolgt in Office 365 Exchange Online Protection ([EoP](eop/exchange-online-protection-eop.md)) und Office 365 Advanced Threat Protection ([ATP](office-365-atp.md)), um festzustellen, ob andere ähnliche Nachrichten von Benutzern gemeldet werden.
- Es wird überprüft, ob ein Benutzer kompromittiert wurde. Diese Überprüfung nutzt Signale in [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) und [Azure Active Directory](https://docs.microsoft.com/azure/active-directory)und korreliert alle zugehörigen Anomalien der Benutzeraktivität. 

Während der Jagd Phase werden Risiken und Bedrohungen verschiedenen Jagd Stufen zugeordnet. 

Sanierung ist die letzte Phase des Manuskripts. Während dieser Phase werden korrekturschritte auf der Grundlage der Untersuchungen und der Jagd Phasen durchgeführt. 

## <a name="example-a-security-administrator-triggers-an-investigation-from-threat-explorer"></a>Beispiel: ein Sicherheitsadministrator löst eine Untersuchung vom Bedrohungs-Explorer aus

Zusätzlich zu automatischen Untersuchungen, die durch eine Warnung ausgelöst werden, kann das Sicherheitsteam Ihres Unternehmens eine automatische Überprüfung aus einer Ansicht im [Threat Explorer](use-explorer-in-security-and-compliance.md)auslösen.

Nehmen Sie beispielsweise an, dass Sie im Explorer Daten zu vom Benutzer gemeldeten Nachrichten anzeigen. Sie können ein Element aus der Ergebnisliste auswählen und dann auf **untersuchen**klicken.

![Vom Benutzer gemeldete Nachrichten im Explorer mit Schaltfläche "untersuchen"](media/Explorer-UserReported-Investigate.png)

Nehmen Sie als weiteres Beispiel an, dass Sie Daten zu e-Mail-Nachrichten anzeigen, die als Schadsoftware erkannt wurden, und es werden mehrere e-Mail-Nachrichten als Schadsoftware erkannt. Wählen Sie die Registerkarte **e-Mail** aus, wählen Sie eine oder mehrere e-Mail-Nachrichten aus, und wählen Sie dann im Menü **Aktionen** die Option **untersuchen**aus. 

![Starten einer Untersuchung für Schadsoftware im Explorer](media/Explorer-Malware-Email-ActionsInvestigate.png)

Ähnlich wie von einer Warnung ausgelöste Textdokumente, werden bei automatischen Untersuchungen, die aus einer Ansicht im Explorer ausgelöst werden, eine Stamm Prüfung, Schritte zum Identifizieren und Korrelieren von Bedrohungen sowie Empfohlene Aktionen zur Minderung dieser Bedrohungen ausgeführt.

## <a name="get-started"></a>Erste Schritte

Um auf ihre Untersuchungen zuzugreifen, wechseln Sie als globaler Office 365-Administrator, Sicherheitsadministrator oder Sicherheits Leser zum Security & Compliance[https://protection.office.com](https://protection.office.com)Center (), und melden Sie sich an. Führen Sie dann einen der folgenden Schritte aus:

- Navigieren Sie im linken Navigationsbereich zu **** > Warnungsbenachrichtigungen**anzeigen**, öffnen Sie eine der Untersuchungen zugehörigen Warnungen, und klicken Sie dann unten im Warnungs Flyout auf den Link **Untersuchung anzeigen** . 

    oder

- Navigieren Sie im linken Navigationsbereich zu **Threat Management** > **Investigations**.

    oder

- Besuchen Sie das Threat Management Dashboard (im Security & Compliance Center, navigieren Sie zu **Threat Management** > **Dashboard**).

![AIR-Widgets](media/air-widgets.png)

Ihre AIR-Widgets werden am oberen Rand des [Sicherheits Dashboards](security-dashboard.md)angezeigt. Wählen Sie ein Widget aus, um loszulegen.

Sie können auch direkt über die entsprechenden Warnungen auf eine Untersuchung zugreifen.

### <a name="automated-investigations"></a>Automatisierte Untersuchungen

Auf der Seite automatisierte Untersuchungen werden die Ermittlungen Ihrer Organisation und ihre aktuellen Status angezeigt.

![Haupt Untersuchungs Seite für Luft](media/air-maininvestigationpage.png) 
  
Sie können:
- Navigieren Sie direkt zu einer Untersuchung (Wählen Sie eine **ERMITTLUNGS-ID**aus).
- Anwenden von Filtern Wählen Sie **unter**Untersuchungs, **Zeitspanne**, **Status**oder eine Kombination aus.
- Exportieren Sie die Daten in eine CSV-Datei.

Der Untersuchungsstatus gibt den Fortschritt der Analyse und Aktionen an. Während der Untersuchung ändert sich der Status, um anzugeben, ob Bedrohungen gefunden wurden, und gibt an, ob Aktionen genehmigt wurden. 
- **Start**: die Untersuchung wird in die Warteschlange eingereiht, um bald zu beginnen
- **Running**: die Untersuchung wurde gestartet und führt ihre Analyse aus.
- **Keine Bedrohungen gefunden**: die Untersuchung hat ihre Analyse abgeschlossen, und es wurden keine Bedrohungen gefunden.
- **Beendet vom System**: die Untersuchung wurde nicht geschlossen und ist nach 7 Tagen abgelaufen.
- **AusstehenDe Aktion**: die Untersuchung hat Bedrohungen mit empfohlenen Aktionen gefunden.
- **Gefundene Bedrohungen**: die Untersuchung hat Bedrohungen gefunden, aber die Bedrohungen haben keine Aktionen in Air verfügbar.
- **Behoben**: der Probe wurde beendet und vollständig korrigiert (alle Aktionen wurden genehmigt)
- **Teilweise**korrigiert: die Untersuchung wurde abgeschlossen, und einige der empfohlenen Aktionen wurden genehmigt.
- **Von Benutzer beendet**: ein Administrator hat die Untersuchung beendet
- **Fehlgeschlagen**: während der Untersuchung ist ein Fehler aufgetreten, der eine Schlussfolgerung zu Bedrohungen verhindert hat.
- In die **Warteschlange eingereiht**: die Untersuchung wartet auf Analyse aufgrund von Einschränkungen der System Verarbeitung (zum Schutz der Dienstleistung).
- **Durch Drosselung beendet**: die Untersuchung konnte aufgrund der Untersuchung des Volumens und der System Verarbeitungs Einschränkungen nicht rechtzeitig abgeschlossen werden. Sie können die Untersuchung erneut auslösen, indem Sie die e-Mail-Nachricht im Explorer auswählen und die Aktion untersuchen auswählen.

### <a name="investigation-graph"></a>Untersuchung Graph

Wenn Sie eine bestimmte Untersuchung öffnen, wird die Seite Untersuchungs Graph angezeigt. Auf dieser Seite werden alle Entitäten angezeigt: e-Mail-Nachrichten, Benutzer (und ihre Aktivitäten) und Geräte, die als Teil der ausgelösten Warnung automatisch untersuchtwurden.

![Seite "AIR Investigation Graph"](media/air-investigationgraphpage.png)

Sie können:
- Erhalten Sie einen visuellen Überblick über die aktuelle Untersuchung.
- Zeigt eine Zusammenfassung der Untersuchungsdauer an.
- Wählen Sie einen Knoten in der Visualisierung aus, um Details für diesen Knoten anzuzeigen.
- Wählen Sie oben eine Registerkarte aus, um Details für diese Registerkarte anzuzeigen.

### <a name="alert-investigation"></a>Warnungs Ermittlung

Auf der Registerkarte **Benachrichtigungen** für eine Untersuchung können Sie Warnungen anzeigen, die für die Untersuchung relevant sind. Details sind die Warnung, die die Untersuchung ausgelöst hat, sowie andere Warnungen, wie beispielsweise riskante Anmeldungen, Massendownloads usw., die mit der Untersuchung in Beziehung stehen. Auf dieser Seite kann ein Sicherheitsanalytiker auch zusätzliche Details zu einzelnen Warnungen anzeigen.

![Seite "Luft Warnungen"](media/air-investigationalertspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuelle Auslöse Warnung und alle zugehörigen Warnungen.
- Wählen Sie in der Liste eine Warnung aus, um eine Fly-Out-Seite mit vollständigen Warnungsdetails zu öffnen.

### <a name="email-investigation"></a>E-Mail-Untersuchung

Auf der Registerkarte **e-Mail-Nachricht** für eine Untersuchung werden alle Cluster von e-Mails angezeigt, die im Rahmen der Untersuchung identifiziert wurden. 

Angesichts der schieren Menge an e-Mails, die Benutzer in einer Organisation senden und empfangen, wird der Prozess der 
- Gruppieren von e-Mail-Nachrichten basierend auf ähnlichen Attributen aus einem Nachrichtenkopf, einem Text, einer URL und Anlagen 
- Trennen von böswilligen e-Mails von der guten e-Mail; und 
- Ausführen von Aktionen für böswillige e-Mail-Nachrichten 

kann viele Stunden in Anspruch nehmen. Mit AIR wird dieser Prozess automatisiert, und das Sicherheitsteam des Unternehmens spart Zeit und Aufwand. 

Während des e-Mail-Analyse Schritts können zwei verschiedene Typen von e-Mail-Clustern identifiziert werden: Ähnlichkeits Cluster und Indikator Cluster. 
- Ähnlichkeits Cluster sind e-Mail-Nachrichten, die ähnliche Absender-und Inhaltsattribute enthalten. Diese Cluster werden anhand der ursprünglichen Erkennungsergebnisse auf bösartige Inhalte ausgewertet. E-Mail-Cluster mit ausreichend bösartigen Entdeckungen werden als böswillig eingestuft.
- Indikator Cluster sind e-Mail-Nachrichten, die dieselbe Indikator Entität (Dateihash oder URL) aus der ursprünglichen e-Mail enthalten. Wenn die ursprüngliche Datei/URL-Entität als bösartig identifiziert wird, wendet AIR den Indikator Urteil auf den gesamten Cluster von e-Mail-Nachrichten an, die diese Entität enthalten. Als als Schadsoftware identifizierte Datei bedeutet dies, dass der Cluster von e-Mail-Nachrichten mit dieser Datei als Schadsoftware-e-Mail-Nachrichten behandelt wird.

Das Ziel des Clusterings besteht darin, andere verwandte e-Mail-Nachrichten zu suchen, die von demselben Absender im Rahmen eines Angriffs oder einer Kampagne gesendet werden.

Auf der Registerkarte **e-Mail** -Nachrichten werden auch e-Mail-Elemente angezeigt, die mit der Untersuchung verbunden sind, wie beispielsweise die vom Benutzer gemeldeten e-Mail-Details, die ursprüngliche e-Mail-Nachricht, die e-Mails aufgrund von Schadsoftware/Phishing usw.

Die auf der Registerkarte e-Mail-Adresse angegebene e-Mail-Anzahl stellt derzeit die Gesamtsumme aller auf der Registerkarte **e-Mail** angezeigten e-Mail-Nachrichten dar. Da e-Mail-Nachrichten in mehreren Clustern vorhanden sind, ist die tatsächliche Gesamtanzahl der identifizierten e-Mail-Nachrichten (und von Korrekturaktionen betroffen) die Anzahl der eindeutigen e-Mail-Nachrichten, die in allen Clustern und e-Mails der ursprünglichen Empfänger vorhanden sind. Nachrichten. 

Sowohl Explorer als auch AIR count-e-Mail-Nachrichten pro Empfänger, da sich die Sicherheits Urteile, Aktionen und zugestellten Standorte je nach Empfänger unterscheiden. Daher wird eine ursprüngliche e-Mail, die an drei Benutzer gesendet wird, als insgesamt drei e-Mail-Nachrichten anstelle einer e-Mail gezählt. Hinweis Es kann Fälle geben, in denen eine e-Mail zwei oder mehr Mal gezählt wird, da die e-Mail mehrere Aktionen enthalten kann und es möglicherweise mehrere Kopien der e-Mail gibt, sobald alle Aktionen ausgeführt werden. Beispielsweise kann eine Schadsoftware-e-Mail, die bei der Zustellung erkannt wird, sowohl eine blockierte (isolierte) e-Mail als auch eine ersetzte e-Mail (Bedrohungs Datei wird durch eine Warnungsdatei ersetzt und dann an das Postfach des Benutzers übermittelt) ergeben. Da es buchstäblich zwei Kopien der e-Mail im System gibt, können diese in den Cluster Zählungen gezählt werden. 

Die e-Mail-Anzahl wird zum Zeitpunkt der Untersuchung berechnet, und einige Zählungen werden neu berechnet, wenn Sie unter Such Flyouts (basierend auf einer zugrunde liegenden Abfrage) öffnen. Die für die e-Mail-Cluster auf der Registerkarte e-Mail angezeigten e-Mail-Anzahl und der im Cluster Flyout angezeigte Wert für die e-Mail-Menge werden zum Zeitpunkt der Untersuchung berechnet. Die e-Mail-Anzahl, die unten auf der Registerkarte e-Mail des Cluster-Flyouts angezeigt wird, sowie die Anzahl der im Explorer angezeigten e-Mail-Nachrichten werden nach der anfänglichen Analyse der Untersuchung empfangenen e-Mail-Nachrichten widergespiegelt. Ein e-Mail-Cluster mit einer ursprünglichen Menge von 10 e-Mail-Nachrichten zeigt daher eine e-Mail-Liste mit einer Gesamtanzahl von 15 an, wenn 5 weitere e-Mail-Nachrichten zwischen der Analysephase der Untersuchung eintreffen und der Administrator Wenn beide Anzahlen in verschiedenen Ansichten angezeigt werden, wird die e-Mail-Auswirkung zum Zeitpunkt der Untersuchung und die aktuelle Auswirkung bis zur Ausführung der Korrektur angezeigt.

Betrachten Sie als Beispiel das folgende Szenario. Der erste Cluster von drei e-Mail-Nachrichten wurde als Phishing eingestuft. Es wurde ein weiterer Cluster ähnlicher Nachrichten mit derselben IP-Adresse und einem anderen Betreff gefunden und als bösartig eingestuft, da einige von Ihnen bei der Ersterkennung als Phishing identifiziert wurden. 

![Seite zur Untersuchung der Luft e-Mail](media/air-investigationemailpage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuellen Cluster Ergebnisse und Bedrohungen.
- Klicken Sie auf eine Cluster Entität oder eine Bedrohungsliste, um eine Fly-Out-Seite zu öffnen, auf der die vollständigen Warnungsdetails angezeigt werden.
- Untersuchen Sie den e-Mail-Cluster, indem Sie oben auf der Registerkarte "e-Mail-Cluster Details" auf den Link "in Explorer öffnen" klicken.

![Untersuchung per e-Mail mit Flyout-Details](media/air-investigationemailpageflyoutdetails.png)

* Hinweis: im Zusammenhang mit e-Mails kann eine Bedrohungs Oberfläche für Volumen Anomalien im Rahmen der Untersuchung angezeigt werden. Eine Volume-Anomalie gibt eine Spitze in ähnlichen e-Mail-Nachrichten rund um die Ermittlungsereignis Zeit im Vergleich zu früheren Zeiten an. Diese Spitze im e-Mail-Datenverkehr mit ähnlichen Eigenschaften (beispielsweise Betreff-und Absenderdomäne, Text Ähnlichkeit und Absender-IP) ist typisch für den Beginn von e-Mail-Kampagnen oder-Angriffen. Massen-, Spam-und legitime e-Mail-Kampagnen teilen diese Merkmale jedoch häufig. Volumen Anomalien stellen eine potenzielle Bedrohung dar und können daher im Vergleich zu Schadsoftware oder Phishing-Bedrohungen, die mithilfe von Antiviren-Engines, Detonation oder böswilliger Reputation identifiziert werden, niedriger sein.

### <a name="user-investigation"></a>Benutzer Ermittlung

Auf der Registerkarte **Benutzer** werden alle Benutzer angezeigt, die im Rahmen der Untersuchung identifiziert wurden. Benutzer werden in der Untersuchung angezeigt, wenn ein Ereignis oder ein Hinweis darauf auftritt, dass der Benutzer betroffen oder kompromittiert werden kann.

In der folgenden Abbildung hat AIR beispielsweise Indikatoren für Kompromisse und Anomalien basierend auf einer neuen Posteingangsregel ermittelt, die erstellt wurde. Weitere Details (Evidence) der Untersuchung sind über detaillierte Ansichten auf dieser Registerkarte verfügbar. Indikatoren für Kompromisse und Anomalien können auch Anomalie-Entdeckungen von [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)sein.

![Seite "Luft Ermittlungs Benutzer"](media/air-investigationuserspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die identifizierten Benutzer Ergebnisse und Risiken.
- Wählen Sie einen Benutzer aus, um eine Fly-Out-Seite mit den vollständigen Warnungsdetails zu öffnen.

### <a name="machine-investigation"></a>Computeruntersuchungen

Auf der Registerkarte **Computer** werden alle Computer angezeigt, die im Rahmen der Untersuchung identifiziert wurden. 

![Seite "Luft Untersuchungsgerät"](media/air-investigationmachinepage.png)

Im Rahmen der Untersuchung korreliert AIR e-Mail-Bedrohungen mit Geräten. Eine Untersuchung übergibt beispielsweise einen bösartigen Dateihash an [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) , um zu untersuchen. Dies ermöglicht eine automatisierte Untersuchung der relevanten Computer für Ihre Benutzer, um sicherzustellen, dass Bedrohungen sowohl in der Cloud als auch über ihre Endpunkte adressiert werden. 

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuellen Computer und Bedrohungen.
- Wählen Sie einen Computer aus, um eine Ansicht zu öffnen, die in die zugehörigen [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection) -Untersuchungen im Windows Defender ATP-Sicherheits Center integriert ist.

### <a name="entity-investigation"></a>Entitäts Untersuchung

Auf der Registerkarte **Entitäten** werden alle Entitäten angezeigt, die im Rahmen der Untersuchung identifiziert wurden. 

Hier sehen Sie die untersuchten Entitäten und Details der Entitätstypen, wie e-Mail-Nachrichten, Cluster, IP-Adressen, Benutzer und vieles mehr. Sie können auch sehen, wie viele Entitäten analysiert wurden und welche Bedrohungen jeweils zugeordnet wurden. 

![Seite "AIR Investigation Entities"](media/air-investigationentitiespage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die gefundenen Ermittlungs Entitäten und-Bedrohungen.
- Wählen Sie eine Entität aus, um eine Fly-Out-Seite zu öffnen, die die Details der zugehörigen Entität anzeigt.

![Details zu AIR Investigation Entities](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>Textbuch-Protokoll

Auf der Registerkarte **Protokoll** werden alle Schritte für das Textbuch angezeigt, die während der Untersuchung aufgetreten sind. Das Protokoll erfasst eine vollständige Bestandsaufnahme aller Aktionen, die von Office 365-Funktionen zur automatischen Untersuchung als Teil von AIR ausgeführt wurden. Es bietet eine übersichtliche Ansicht aller Schritte, einschließlich der Aktion selbst, einer Beschreibung und der Dauer des aktuellen vom Anfang bis zum Ende. 

![Seite "AIR Investigation log"](media/air-investigationlogpage.png)

Sie können:
- Sehen Sie sich eine visuelle Übersicht über die Schritte des Manuskripts an.
- Exportieren Sie die Ergebnisse in eine CSV-Datei.
- Filtern Sie die Ansicht.

### <a name="recommended-actions"></a>Empfohlene Aktionen

Auf der Registerkarte **Aktionen** werden alle Text Handlung-Aktionen angezeigt, die nach Abschluss der Untersuchung zur Korrektur empfohlen werden. 

Aktionen erfassen die Schritte, die Microsoft empfiehlt, die Sie am Ende einer Untersuchung ausführen. Sie können Korrekturaktionen durchführen, indem Sie eine oder mehrere Aktionen auswählen. Wenn **** Sie auf Genehmigen klicken, kann die Korrektur beginnen. (Entsprechende Berechtigungen sind erforderlich – die Rolle "suchen und löschen" ist erforderlich, um Aktionen aus Explorer und AIR ausführen zu können). Beispielsweise kann ein Sicherheits Lesegerät Aktionen anzeigen, aber nicht genehmigen. Hinweis: Sie müssen nicht jede Aktion genehmigen. Wenn Sie mit der empfohlenen Aktion nicht einverstanden sind oder Ihre Organisation bestimmte Arten von Aktionen nicht wählt, können Sie entweder die Aktionen **ablehnen** oder einfach ignorieren und keine Aktion ausführen. Durch das genehmigen und/oder ablehnen aller Aktionen wird die Untersuchung vollständig geschlossen, und wenn einige Aktionen nicht abgeschlossen sind, wird der Untersuchungsstatus in den Zustand teilweise korrigiert geändert.

![Seite "AIR Investigations Action"](media/air-investigationactionspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die vom Textbuch empfohlenen Aktionen.
- Wählen Sie eine einzelne Aktion oder mehrere Aktionen aus.
- Genehmigen oder ablehnen von empfohlenen Aktionen mit Kommentaren.
- Exportieren Sie die Ergebnisse in eine CSV-Datei.
- Filtern Sie die Ansicht.

## <a name="how-to-get-air"></a>So erhalten Sie AIR

Derzeit befinden sich Office 365 AIR-Features in der Vorschau. Wenn allgemein verfügbar, werden Office 365 AIR-Features in die folgenden Abonnements aufgenommen:

- Microsoft 365 Enterprise E5
- Office 365 Enterprise E5
- Microsoft Threat Protection
- Office 365 Advanced Threat Protection-Plan 2

Weitere Informationen zur Verfügbarkeit von Funktionen finden Sie in der [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap).
