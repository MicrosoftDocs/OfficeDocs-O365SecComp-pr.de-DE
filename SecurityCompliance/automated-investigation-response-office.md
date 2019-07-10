---
title: Automatische Untersuchung und Reaktion (Air) mit Office 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 06/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Erfahren Sie mehr über die automatisierten Ermittlungs-und Antwortfunktionen in Office 365 Advanced Threat Protection.
ms.openlocfilehash: 3e74fd7a12727880164797f076d254416325713a
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598521"
---
# <a name="automated-investigation-and-response-air-with-office-365"></a>Automatische Untersuchung und Reaktion (Air) mit Office 365

Automatische Untersuchung und Reaktion (Air) (derzeit in der öffentlichen Vorschau als eine von vielen [Office 365 Funktionen zur Ermittlung und Reaktion auf Bedrohungen](office-365-ti.md)) können Sie automatisierte Untersuchungen und Korrekturen an bekannten Bedrohungen durchführen, die heute vorhanden sind. Lesen Sie diesen Artikel, um einen Überblick über Air zu erhalten und um zu erfahren, wie Sie Ihre Organisation und ihre Sicherheitsteams bei der effektiveren und effizienteren Abwehr von Bedrohungen unterstützen können. 

Weitere Informationen zur Verfügbarkeit von Air-Funktionen finden Sie in der [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap).

## <a name="alerts"></a>Warnungen

[Warnungen](alert-policies.md#viewing-alerts) stellen Auslöser für Sicherheitsvorgänge-Team Workflows für die Vorfall Antwort dar. Priorisieren des richtigen Warnungs Satzes für die Untersuchung, wobei sichergestellt wird, dass keine Bedrohungen unbehandelt sind, ist eine Herausforderung. Wenn Untersuchungen zu Warnungen manuell durchgeführt werden, müssen Sicherheits Betriebsteams Entitäten (beispielsweise Inhalte, Geräte und Benutzer), die von Bedrohungen bedroht sind, jagen und korrelieren. Solche Aufgaben und Workflows sind sehr zeitaufwendig und umfassen mehrere Tools und Systeme. Mit Air werden Untersuchungen und Antworten in wichtige Warnungen zur Sicherheits-und Bedrohungs Verwaltung automatisiert, die ihre Sicherheitsantwort-Textbuch automatisch auslösen. 

In der ersten Version von Air im April 2019 werden Warnungen, die von folgenden Warnungsrichtlinien für einzelne Ereignisse generiert werden, automatisch untersucht. 

1. Ein potenziell böswilliger URL-Klick wurde erkannt.
2. Vom Benutzer als Phishing gemeldete e-Mail *
3. E-Mail-Nachrichten mit Schadsoftware nach der Zustellung entfernt *
4. E-Mail-Nachrichten mit gelöschten Phishing-URLs nach der Zustellung *

> [!NOTE]
> Diesen Warnungen wurde in den jeweiligen Warnungsrichtlinien innerhalb des Security #a0 Compliance Centers mit e-Mail-Benachrichtigungen ein "Informations"-Schweregrad zugewiesen. Diese können über die Warnungsrichtlinien Konfiguration aktiviert werden.

Um Warnungen anzuzeigen, wählen Sie **** > im Security #a0 Compliance Center Benachrichtigungen**anzeigen Warnungen**aus. Wählen Sie eine Warnung aus, um die Details anzuzeigen, und verwenden Sie dann den Link **Untersuchung anzeigen** , um zur entsprechenden [Untersuchung](#investigation-graph)zu gelangen. Beachten Sie, dass Informationswarnungen standardmäßig in der Warnungsansicht ausgeblendet werden. Um diese anzuzeigen, müssen Sie die Warnungsfilterung so ändern, dass Informationswarnungen hinzugefügt werden.

Wenn Ihre Organisation ihre Sicherheitswarnungen über ein Warnungsverwaltungssystem, ein Dienst Verwaltungssystem oder ein System für die Verwaltung von Sicherheitsinformationen und Ereignissen verwaltet, können Sie Office 365 Benachrichtigungen entweder per e-Mail-Benachrichtigung oder über den [ Office 365-Verwaltungs Aktivitäts-API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). Die Untersuchung von Benachrichtigungs Benachrichtigungen per e-Mail oder API enthält Links für den Zugriff auf die Warnungen im Security #a0 Compliance Center, sodass der zugewiesene Sicherheitsadministrator schnell zu der Untersuchung navigieren kann.

![Warnungen, die mit Untersuchungen verknüpft sind](media/air-alerts-page-details.png) 


## <a name="security-playbooks"></a>Sicherheits-Manuskripte

Sicherheits-Textbuch sind Back-End-Richtlinien, die im Mittelpunkt der Automatisierung in Microsoft Threat Protection stehen. Die in Air bereitgestellten Sicherheits-Textbuch basieren auf gängigen realen Sicherheitsszenarien. Ein Sicherheits Textbuch wird automatisch gestartet, wenn in Ihrer Organisation eine Warnung ausgelöst wird. Sobald die Warnung ausgelöst wird, wird das zugehörige Textbuch automatisch ausgeführt. Im Textbuch wird eine Untersuchung durchgeführt, wobei alle zugehörigen Metadaten (einschließlich e-Mail-Nachrichten, Benutzer, Subjekte, Absender usw.) untersucht werden. Basierend auf den Ergebnissen des Textbuch empfiehlt Air eine Reihe von Aktionen, die das Sicherheitsteam Ihres Unternehmens ausführen kann, um die Bedrohung zu steuern und zu mindern. 

Die Sicherheits-Textbuch-Dokumente, die Sie mit Air erhalten, wurden entwickelt, um die häufigsten Bedrohungen zu bewältigen, denen Organisationen heute ausgesetzt sind. Sie basieren auf Eingaben aus Sicherheits-und Vorfall Reaktions Teams, einschließlich derer, die Microsoft-und Kunden Ressourcen schützen.

### <a name="security-playbooks-are-rolling-out-in-phases"></a>Sicherheits-Textbuch-Rollen in Phasen

Im Rahmen von Air werden Sicherheits-Textbuch in Phasen ausgerollt.

- **Phase 1 (April 2019)**: Textbuch enthält Empfehlungen für Aktionen, die Sicherheitsadministratoren überprüfen und genehmigen. In Phase 1 werden die folgenden Textbuch-Texttypen enthalten:
    - Vom Benutzer gemeldete Phishing-Nachricht
    - Änderung des URL-Klick Urteils 
    - Erkannte Schadsoftware nach der Zustellung (Malware zap)
    - Phishing-Erkennung nach der Zustellung zap (Phishing zap)
    - Manuelle e-Mail-Untersuchungen (mit Threat Explorer)

- **Phase 2 (zweite Hälfte von 2019)**: mehrere neue Textbuch-und Textbuch-Verbesserungen sowie die Option für Sicherheitsadministratoren zum Konfigurieren von Sicherheits-Textbuch zum automatischen Ausführen bestimmter Aktionen ohne administrative Interaktion. 

### <a name="playbooks-include-investigation-and-recommendations"></a>Manuskripte umfassen Untersuchungen und Empfehlungen

Jedes Textbuch umfasst Folgendes: 
- eine Stamm Untersuchung, 
- Schritte zum Identifizieren und korrelieren anderer potenzieller Bedrohungen und 
- Empfohlene Aktionen zur Behebung von Bedrohungen.

Jeder allgemeine Schritt umfasst viele unter Schritte, die ausgeführt werden, um eine Tiefe, detaillierte und erschöpfende Antwort auf Bedrohungen bereitzustellen.

## <a name="example-a-user-reported-phish-message-launches-an-investigation-playbook"></a>Beispiel: eine von einem Benutzer gemeldete Phishing-Nachricht startet eine Untersuchung des Manuskripts

Wenn ein Benutzer in Ihrer Organisation eine e-Mail-Nachricht übermittelt und an Microsoft mithilfe des [Berichtsnachrichten-Add-Ins für Outlook oder Outlook Web Access](enable-the-report-message-add-in.md)meldet, wird der Bericht auch an Ihr System gesendet und im Explorer in der vom Benutzer gemeldeten Ansicht angezeigt. Diese vom Benutzer gemeldete Nachricht löst jetzt eine System basierte Informationswarnung aus, die das unter suchbuch automatisch startet.

Während der Stamm Untersuchungsphase werden verschiedene Aspekte der e-Mail bewertet. Zu diesen zählen:
- Eine Bestimmung darüber, welche Art von Bedrohung es sein könnte;
- Absender
- Woher die e-Mail gesendet wurde (sendende Infrastruktur);
- Gibt an, ob andere Instanzen der e-Mail zugestellt oder blockiert wurden;
- Eine Bewertung durch unsere Analysten;
- Gibt an, ob die e-Mail bekannten Kampagnen zugeordnet ist;
- und vieles mehr.

Nachdem die Stamm Untersuchung abgeschlossen ist, enthält das Textbuch eine Liste der empfohlenen Aktionen, die für die ursprünglichen e-Mail-Objekte und zugehörigen Entitäten übernommen werden sollen.
  
Im nächsten Schritt werden mehrere Schritte zur Ermittlung und Jagd von Bedrohungen ausgeführt:

- Ähnliche e-Mail-Nachrichten in anderen e-Mail-Cluster werden durchsucht.
- Das Signal wird für andere Plattformen wie [Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)freigegeben.
- Es wird festgestellt, ob Benutzer in verdächtigen e-Mail-Nachrichten auf böswillige Links geklickt haben.
- Eine Überprüfung erfolgt über Office 365 Exchange Online Protection ([EoP](eop/exchange-online-protection-eop.md)) und Office 365 Advanced Threat Protection ([ATP](office-365-atp.md)), um zu sehen, ob andere ähnliche Nachrichten von Benutzern gemeldet werden.
- Eine Überprüfung wird durchgeführt, um festzustellen, ob ein Benutzer kompromittiert wurde. Bei dieser Überprüfung werden Signale in der [Microsoft Cloud-App-Sicherheit](https://docs.microsoft.com/cloud-app-security) und in der [Azure-Active Directory](https://docs.microsoft.com/azure/active-directory)verwendet, sodass alle zugehörigen Anomalien der Benutzeraktivität korreliert werden. 

Während der Jagd Phase werden Risiken und Bedrohungen verschiedenen Jagd Schritten zugeordnet. 

Die Korrektur ist die letzte Phase des Textbuch. In dieser Phase werden korrekturschritte basierend auf den Ermittlungs-und Jagd Phasen durchgeführt. 

## <a name="example-a-security-administrator-triggers-an-investigation-from-threat-explorer"></a>Beispiel: ein Sicherheitsadministrator löst eine Untersuchung mit Threat Explorer aus.

Zusätzlich zu den automatischen Untersuchungen, die durch eine Warnung ausgelöst werden, kann das Sicherheits Betriebsteam Ihrer Organisation eine automatische Untersuchung aus einer Ansicht in [Threat Explorer](use-explorer-in-security-and-compliance.md)auslösen.

Nehmen wir beispielsweise an, dass Sie Daten im Explorer zu vom Benutzer gemeldeten Nachrichten anzeigen. Sie können ein Element in der Ergebnisliste auswählen und dann auf über **prüfen**klicken.

![Vom Benutzer gemeldete Nachrichten im Explorer mit Schaltfläche "Recherchieren"](media/Explorer-UserReported-Investigate.png)

Nehmen Sie als weiteres Beispiel an, dass Sie Daten zu e-Mail-Nachrichten anzeigen, die als Schadsoftware erkannt wurden, und dass mehrere e-Mail-Nachrichten als Schadsoftware erkannt werden. Sie können die Registerkarte **e-Mail** auswählen, eine oder mehrere e-Mail-Nachrichten auswählen und dann im Menü **Aktionen** die Option **untersuchen**auswählen. 

![Starten einer Untersuchung für Schadsoftware im Explorer](media/Explorer-Malware-Email-ActionsInvestigate.png)

Ähnlich wie Textbuch, die durch eine Warnung ausgelöst werden, umfassen automatische Untersuchungen, die aus einer Ansicht im Explorer ausgelöst werden, eine Stamm Ermittlung, Schritte zum Identifizieren und Korrelieren von Bedrohungen sowie Empfohlene Aktionen zur Minderung dieser Bedrohungen.

## <a name="get-started"></a>Erste Schritte

Um auf ihre Untersuchungen zuzugreifen, wechseln Sie als globaler Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser zum Security #a0 Compliance[https://protection.office.com](https://protection.office.com)Center (), und melden Sie sich an. Führen Sie dann einen der folgenden Schritte aus:

- Navigieren Sie in der linken Navigationsleiste zu **Benachrichtigungen** > Warnungen**anzeigen**, öffnen Sie eine der untersuchten Warnungen, und klicken Sie dann unten im Warnungs Flyout auf den Link **Untersuchung anzeigen** . 

    oder

- Navigieren Sie in der linken Navigationsleiste zu **Threat Management** > **Investigations**.

    oder

- Besuchen Sie das Threat Management-Dashboard (im Security #a0 Compliance Center finden Sie unter **Threat Management** > **Dashboard**).

![Air-Widgets](media/air-widgets.png)

Ihre Air-Widgets werden am oberen Rand des [Sicherheits Dashboards](security-dashboard.md)angezeigt. Wählen Sie ein Widget aus, um loszulegen.

Sie können auch direkt über die zugehörigen Benachrichtigungen auf eine Untersuchung zugreifen.

### <a name="automated-investigations"></a>Automatisierte Untersuchungen

Die Seite Automatische Untersuchungen zeigt die Ermittlungen Ihrer Organisation und ihre aktuellen Status.

![Haupt Untersuchungs Seite für Air](media/air-maininvestigationpage.png) 
  
Sie können:
- Navigieren Sie direkt zu einer Untersuchung (Wählen Sie eine **Ermittlungs-ID**aus).
- Anwenden von Filtern. Wählen Sie **** zwischen Ermittlungstyp, **Zeitbereich**, **Status**oder einer Kombination aus diesen aus.
- Exportieren Sie die Daten in eine CSV-Datei.

Der unter Suchstatus gibt den Fortschritt der Analyse und der Aktionen an. Beim Ausführen der Untersuchung ändert sich der Status, um anzugeben, ob Bedrohungen gefunden wurden, und gibt an, ob Aktionen genehmigt wurden. 
- **Start**: die Untersuchung wird in Kürze in die Warteschlange eingereiht.
- **Running**: die Untersuchung wurde gestartet und führt die Analyse
- **Keine Bedrohungen gefunden**: die Untersuchung hat die Analyse abgeschlossen, und es wurden keine Bedrohungen gefunden.
- **Beendet durch System**: die Untersuchung wurde nicht geschlossen und ist nach 7 Tagen abgelaufen.
- **Ausstehende Aktion**: die Untersuchung hat Bedrohungen mit empfohlenen Aktionen gefunden
- **Gefundene Bedrohungen**: die Untersuchung hat Bedrohungen festgestellt, aber für die Bedrohungen sind keine Aktionen in Air verfügbar.
- **Behoben**: das Probe wurde fertig gestellt und wurde vollständig korrigiert (alle Aktionen wurden genehmigt)
- **Teilweise behoben**: die Untersuchung wurde abgeschlossen, und einige der empfohlenen Aktionen wurden genehmigt.
- **Durch den Benutzer beendet**: ein Administrator hat die Untersuchung beendet
- **** Fehler: während der Untersuchung ist ein Fehler aufgetreten, der verhindert, dass er eine Schlussfolgerung zu Bedrohungen erreicht.
- In der **Warteschlange durch Drosselung**: die Untersuchung wartet aufgrund von Einschränkungen der System Verarbeitung auf die Analyse (zum Schutz der Dienstleistung)
- **Durch Drosselung beendet**: die Untersuchung konnte aufgrund der Untersuchung von Volumen-und System Verarbeitungs Einschränkungen nicht rechtzeitig abgeschlossen werden. Sie können die Untersuchung erneut auslösen, indem Sie die e-Mail im Explorer auswählen und die Aktion untersuchen auswählen.

### <a name="investigation-graph"></a>Unter Such Diagramm

Wenn Sie eine bestimmte Untersuchung öffnen, wird die Seite "Ermittlungs Diagramm" angezeigt. Auf dieser Seite werden alle unterschiedlichen Entitäten angezeigt: e-Mail-Nachrichten, Benutzer (und deren Aktivitäten) und Geräte, die automatisch als Teil der ausgelösten Warnung untersuchtwurden.

![Seite "Luft Untersuchungs Diagramm"](media/air-investigationgraphpage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuelle Untersuchung.
- Hier wird eine Zusammenfassung der Untersuchungsdauer angezeigt.
- Wählen Sie einen Knoten in der Visualisierung aus, um Details zu diesem Knoten anzuzeigen.
- Wählen Sie eine Registerkarte oben aus, um Details für diese Registerkarte anzuzeigen.

### <a name="alert-investigation"></a>Warnungs Ermittlung

Auf der Registerkarte **Benachrichtigungen** für eine Untersuchung können Sie Warnungen anzeigen, die für die Untersuchung relevant sind. Details umfassen die Warnung, die die Untersuchung ausgelöst hat, und andere Warnungen, wie etwa riskante Anmeldungen, Massendownloads usw., die mit der Untersuchung korreliert sind. Auf dieser Seite kann ein Sicherheitsanalytiker auch weitere Details zu einzelnen Benachrichtigungen anzeigen.

![Seite "Luft Warnungen"](media/air-investigationalertspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuelle Auslöse Warnung und alle zugeordneten Warnungen.
- Wählen Sie eine Warnung in der Liste aus, um eine Ausklappseite zu öffnen, auf der vollständige Warnungsdetails angezeigt werden.

### <a name="email-investigation"></a>E-Mail-Untersuchung

Auf der Registerkarte **e-Mail** für eine Untersuchung können Sie alle Cluster von e-Mails sehen, die im Rahmen der Untersuchung identifiziert wurden. 

Angesichts der schieren Menge an e-Mails, die Benutzer in einer Organisation senden und empfangen, wird der Prozess der 
- Gruppieren von e-Mail-Nachrichten basierend auf ähnlichen Attributen aus einer Nachrichtenkopfzeile, einem Textkörper, einer URL und Anlagen; 
- Trennen von böswilligen e-Mails von der guten e-Mail-Nachricht und 
- Ausführen von Aktionen in böswilligen e-Mail-Nachrichten 

kann viele Stunden dauern. Dieses Verfahren wird von Air jetzt automatisiert, sodass Zeit und Aufwand für das Sicherheitsteam Ihres Unternehmens gespart werden. 

Während des e-Mail-Analyse Schritts können zwei verschiedene Arten von e-Mail-Clustern identifiziert werden: Ähnlichkeits Cluster und Indikator Cluster. 
- Ähnlichkeits Cluster sind e-Mail-Nachrichten, die ähnliche Absender-und Inhaltsattribute enthalten. Diese Cluster werden basierend auf den ursprünglichen Entdeckungs Ergebnissen auf schädliche Inhalte ausgewertet. E-Mail-Cluster mit ausreichenden bösartigen Erkennungen werden als böswillig betrachtet.
- Indikator Cluster sind e-Mail-Nachrichten, die die gleiche Indikator Entität (Datei Hash oder URL) aus der ursprünglichen e-Mail enthalten. Wenn die ursprüngliche Datei/URL-Entität als bösartig identifiziert wird, wendet Air das Indikator Urteil auf den gesamten Cluster von e-Mail-Nachrichten an, die diese Entität enthalten. Da eine als Schadsoftware bezeichnete Datei bedeutet, dass der Cluster von e-Mail-Nachrichten mit dieser Datei als Schadsoftware-e-Mail-Nachrichten behandelt wird.

Das Ziel des Clusterings besteht darin, andere verwandte e-Mail-Nachrichten zu finden, die von demselben Absender als Teil eines Angriffs oder einer Kampagne gesendet werden.

Auf der Registerkarte **e-Mail** werden auch e-Mail-Elemente im Zusammenhang mit der Untersuchung angezeigt, beispielsweise die e-Mail-Details des Benutzers, die gemeldeten e-Mails, die e-Mail-Nachricht (en), die aufgrund von Schadsoftware/Phishing zapped wurden.

Die auf der Registerkarte e-Mail angegebene e-Mail-Anzahl stellt derzeit die Gesamtsumme aller e-Mail-Nachrichten dar, die auf der Registerkarte **e-Mail** angezeigt werden. Da e-Mail-Nachrichten in mehreren Clustern vorhanden sind, ist die tatsächliche Gesamtanzahl der identifizierten e-Mail-Nachrichten (und von Korrekturaktionen betroffen) die Anzahl der eindeutigen e-Mail-Nachrichten, die in allen Clustern und den e-Mail-Adressen der ursprünglichen Empfänger vorhanden sind. Nachrichten. 

Sowohl Explorer als auch Air count-e-Mails pro Empfänger, da sich die Sicherheits Urteile, Aktionen und Übermittlungsorte pro Empfänger unterscheiden. Eine ursprüngliche e-Mail-Nachricht, die an drei Benutzer gesendet wird, wird daher als insgesamt drei e-Mail-Nachrichten anstelle von einer e-Mail gezählt. Hinweis Es kann Fälle geben, in denen eine e-Mail zwei oder mehr Mal gezählt wird, da die e-Mail möglicherweise mehrere Aktionen enthält und mehrere Kopien der e-Mail vorhanden sein können, sobald alle Aktionen ausgeführt werden. Beispielsweise kann eine Malware-e-Mail, die bei der Zustellung erkannt wird, sowohl eine blockierte (isolierte) e-Mail-Nachricht als auch eine ersetzte e-Mail verursachen (Bedrohungs Datei wurde durch eine Warn Datei ersetzt und dann an das Postfach des Benutzers gesendet). Da es buchstäblich zwei Kopien der e-Mail im System gibt, können diese beide in Cluster Zählungen gezählt werden. 

E-Mail-Anzahlen werden zum Zeitpunkt der Untersuchung berechnet, und einige Zahlen werden neu berechnet, wenn Sie Ermittlungs Flyouts (basierend auf einer zugrunde liegenden Abfrage) öffnen. Die e-Mail-Anzahl, die für die e-Mail-Cluster auf der Registerkarte e-Mail angezeigt wird, und der Wert für die e-Mail-Menge, die im Cluster Flyout angezeigt wird, werden zum Die e-Mail-Anzahl, die am unteren Rand der Registerkarte e-Mail im Cluster Flyout angezeigt wird, sowie die Anzahl der im Explorer angezeigten e-Mail-Nachrichten spiegeln e-Mail-Nachrichten wider, die nach der anfänglichen Analyse der Untersuchung empfangen wurden. So würde ein e-Mail-Cluster, der eine ursprüngliche Menge von 10 e-Mail-Nachrichten anzeigt, eine e-Mail-Listen Summe von 15 anzeigen, wenn 5 weitere e-Mail-Nachrichten zwischen der Ermittlungs Analysephase und dem Zeitpunkt, zu dem der Administrator Das anzeigen beider Zähler in unterschiedlichen Ansichten wird durchgeführt, um die e-Mail-Auswirkungen zum Zeitpunkt der Untersuchung und die aktuellen Auswirkungen bis zur Ausführung der Wiederherstellung anzugeben.

Als Beispiel wird das folgende Szenario betrachtet. Der erste Cluster von drei e-Mail-Nachrichten wurde als Phishing betrachtet. Ein weiterer Cluster ähnlicher Nachrichten mit derselben IP und demselben Betreff wurde gefunden und als bösartig eingestuft, da einige von Ihnen während der anfänglichen Erkennung als Phishing identifiziert wurden. 

![Seite für die Untersuchung von Air e-Mail](media/air-investigationemailpage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuellen Clustering-Ergebnisse und Bedrohungen, die gefunden wurden.
- Klicken Sie auf eine Cluster Entität oder eine Bedrohungsliste, um eine Ausklappseite zu öffnen, auf der die vollständigen Warnungsdetails angezeigt werden.
- Untersuchen Sie den e-Mail-Cluster weiter, indem Sie oben auf der Registerkarte "e-Mail-Cluster Details" auf den Link "in Explorer öffnen" klicken.

![Air Investigation e-Mail mit Flyout-Details](media/air-investigationemailpageflyoutdetails.png)

* Hinweis: im Rahmen der Untersuchung wird im Kontext der e-Mail möglicherweise eine Bedrohungs Fläche für Volumen Anomalien angezeigt. Eine Volumen Anomalie gibt eine Spitze in ähnlichen e-Mail-Nachrichten um die Ermittlungsereignis Zeit im Vergleich zu früheren Zeitrahmen an. Diese Spitze im e-Mail-Datenverkehr mit ähnlichen Merkmalen (z. b. Betreff-und Absenderdomäne, Text Ähnlichkeit und Absender-IP) ist typisch für den Start von e-Mail-Kampagnen oder-Angriffen. Massen-, Spam-und legitime e-Mail-Kampagnen teilen diese Merkmale jedoch häufig. Volumen Anomalien stellen eine potenzielle Bedrohung dar und können dementsprechend im Vergleich zu Malware-oder Phishing-Bedrohungen, die mit Antiviren-Engines, Detonation oder böswilliger Reputation identifiziert werden, eine geringere schwere aufweisen.

### <a name="user-investigation"></a>Benutzer Ermittlung

Auf der Registerkarte **Benutzer** werden alle Benutzer angezeigt, die als Teil der Untersuchung identifiziert wurden. Benutzer werden in der Untersuchung angezeigt, wenn ein Ereignis oder ein Hinweis darauf besteht, dass der Benutzer möglicherweise betroffen oder kompromittiert wurde.

In der folgenden Abbildung zeigt Air beispielsweise Indikatoren für Kompromisse und Anomalien basierend auf einer neuen Posteingangsregel, die erstellt wurde. Weitere Details (Beweise) der Untersuchung stehen über detaillierte Ansichten auf dieser Registerkarte zur Verfügung. Indikatoren für Kompromisse und Anomalien können auch anomale Erkennungen von [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)umfassen.

![Seite "Air Investigation Users"](media/air-investigationuserspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über identifizierte Benutzer Ergebnisse und gefundene Risiken.
- Wählen Sie einen Benutzer aus, um eine Ausklappseite zu öffnen, auf der die vollständigen Warnungsdetails angezeigt werden.

### <a name="machine-investigation"></a>Maschinelle Untersuchung

Auf der Registerkarte " **Computer** " werden alle Computer angezeigt, die als Teil der Untersuchung identifiziert wurden. 

![Seite "Air Investigation Machine"](media/air-investigationmachinepage.png)

Im Rahmen der Untersuchung korreliert Air e-Mail-Bedrohungen mit Geräten. Beispielsweise übergibt eine Untersuchung einen bösartigen Datei Hash an [Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection
) , um zu untersuchen. Dies ermöglicht eine automatisierte Untersuchung relevanter Computer für Ihre Benutzer, um sicherzustellen, dass Bedrohungen sowohl in der Cloud als auch in ihren Endpunkten behandelt werden. 

Sie können:
- Erhalten Sie eine visuelle Übersicht über die gefundenen aktuellen Computer und Bedrohungen.
- Wählen Sie einen Computer aus, um eine Ansicht zu öffnen, die in den entsprechenden [Microsoft Defender-ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations) -Untersuchungen im Sicherheits Center von Microsoft Defender angezeigt wird.

### <a name="entity-investigation"></a>Untersuchung von Entitäten

Auf der Registerkarte **Entitäten** werden alle Entitäten angezeigt, die als Teil der Untersuchung identifiziert wurden. 

Hier sehen Sie die untersuchten Entitäten und Details der Entitätstypen wie e-Mail-Nachrichten, Cluster, IP-Adressen, Benutzer und vieles mehr. Sie können auch sehen, wie viele Entitäten analysiert wurden, und die Bedrohungen, die jedem zugeordnet wurden. 

![Seite "Air Investigation Entities"](media/air-investigationentitiespage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die gefundenen Ermittlungs Entitäten und-Bedrohungen.
- Wählen Sie eine Entität aus, um eine Ausklappseite zu öffnen, auf der die zugehörigen Entitäts Details angezeigt werden.

![Details zu Air Investigation Entities](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>Manuskript Protokoll

Auf der Registerkarte **Protokoll** werden alle Schritte im Textbuch angezeigt, die während der Untersuchung aufgetreten sind. Im Protokoll wird ein vollständiger bestand aller Aktionen erfasst, die von Office 365 automatischen Ermittlungsfunktionen als Teil von Air abgeschlossen wurden. Es bietet eine klare Sicht auf alle Schritte, einschließlich der Aktion selbst, eine Beschreibung und die Dauer des tatsächlichen von Anfang bis Ende. 

![Seite "Air Investigation log"](media/air-investigationlogpage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die ausgeführten Schritte im Textbuch.
- Exportieren Sie die Ergebnisse in eine CSV-Datei.
- Filtern Sie die Ansicht.

### <a name="recommended-actions"></a>Empfohlene Aktionen

Auf der Registerkarte **Aktionen** werden alle Textbuch-Aktionen angezeigt, die nach Abschluss der Untersuchung zur Korrektur empfohlen werden. 

Durch Aktionen werden die Schritte erfasst, die Microsoft am Ende einer Untersuchung empfiehlt. Sie können hier Korrekturaktionen durch Auswählen einer oder mehrerer Aktionen durchführen. Durch **** klicken auf genehmigen kann die Wiederherstellung beginnen. (Entsprechende Berechtigungen sind erforderlich – die Funktion "suchen und löschen" ist erforderlich, um Aktionen aus Explorer und Air auszuführen). Beispielsweise kann ein Sicherheits Leser Aktionen anzeigen, aber nicht genehmigen. Hinweis: Sie müssen nicht jede Aktion genehmigen. Wenn Sie mit der empfohlenen Aktion nicht einverstanden sind oder Ihre Organisation keine bestimmten Arten von Aktionen ausgewählt hat, können Sie entweder die Aktionen **ablehnen** oder einfach ignorieren und keine Aktionen ausführen. Durch das genehmigen und/oder ablehnen aller Aktionen wird die Untersuchung vollständig beendet, während einige unvollständige Aktionen dazu führen, dass der unter Suchstatus in einen teilweise korrigierten Zustand wechselt.

![Seite "Luft Ermittlungsaktionen"](media/air-investigationactionspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die empfohlenen Aktionen im Textbuch.
- Wählen Sie eine einzelne Aktion oder mehrere Aktionen aus.
- Genehmigen oder ablehnen von empfohlenen Aktionen mit Kommentaren.
- Exportieren Sie die Ergebnisse in eine CSV-Datei.
- Filtern Sie die Ansicht.

## <a name="how-to-get-air"></a>So erhalten Sie Luft

Derzeit befinden sich Office 365 Air-Features in der Vorschau. Wenn allgemein verfügbar ist, werden Office 365 Air-Features in den folgenden Abonnements enthalten sein:

- Microsoft 365 Enterprise E5
- Office 365 Enterprise E5
- Microsoft Threat Protection
- Office 365 Advanced Threat Protection-Plan 2

Weitere Informationen zur Verfügbarkeit von Features finden Sie in der [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap).
