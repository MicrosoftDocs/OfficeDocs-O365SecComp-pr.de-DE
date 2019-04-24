---
title: Technologiesteuerungen in Office 365
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
description: 'Zusammenfassung: eine Übersicht über die Technologie Steuerungsmethoden von Microsoft für Office 365.'
ms.openlocfilehash: a8dcb65880fc729fc067b2f2bcf25c7db76dbca9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262337"
---
# <a name="office-365-technology-controls"></a>Technologiesteuerungen in Office 365 

Microsoft verwendet verschiedene Tools und Technologien, um den Zugriff auf Kundendaten in Exchange Online und SharePoint Online zu steuern, zu verwalten und zu überwachen, einschließlich Lockbox und Kunden Lockbox, mehrstufige Authentifizierung und vieles mehr. Jammern Enterprise verwendet ähnliche Steuerelemente, wie in [jammern Enterprise Access Controls](office-365-yammer-enterprise-access-controls.md)beschrieben.

Office 365-Ingenieure haben keinen Zugriff auf Office 365-Kundendaten, und Sie müssen einen Genehmigungsprozess durchlaufen, der sowohl Microsoft als auch – wenn der Kunde die Kunden-Lockbox-Funktion für Exchange Online und SharePoint Online lizenziert – Kunden Genehmigung, bevor der Zugriff auf Kundendaten für Dienstvorgänge erfolgen kann. Wenn die Genehmigung erteilt wird, werden dienstspezifische Administratorkonten Just-in-Time mit genau genug Zugriff für die Aufgaben, die für die Dienstanforderung erforderlich sind, zur Verfügung gestellt.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox und Kunden-Lockbox
Obwohl es äußerst selten ist, kann ein Kunde eine Unterstützung von Microsoft anfordern, die einem Microsoft-Techniker die Inhalte des Kunden zur Verfügung stellt, um Sie bei einem Problem zu unterstützen. So steuern Sie den Zugriff auf Exchange Online (einschließlich Skype for Business-Daten, die in den Postfächern der Benutzer gespeichert sind (Skype for Business Coverage enthält keine Skype-Besprechungs Übertragungs Aufzeichnungen oder Inhalte, die in Besprechungen von Benutzern hochgeladen werden)) und SharePoint Online ( umfasst OneDrive for Business), Microsoft verwendet ein Zugriffs Steuerungssystem namens Lockbox. Bevor Microsoft Engineer auf Exchange Online-oder SharePoint Online-Systeme oder-Daten zugreifen kann, müssen Sie eine Zugriffsanforderung mit Lockbox übermitteln. Die Verwendung von Lockbox ist für alle erhöhten Zugriff auf Exchange Online oder SharePoint Online erforderlich.

Die Lockbox verarbeitet Anforderungen für Berechtigungen, mit denen Ingenieure Betriebs-und Verwaltungsfunktionen innerhalb des Diensts ausführen können. Ingenieure übermitteln Anfragen über Lockbox, die von einem Vorgesetzten genehmigt werden müssen, bevor der Techniker Zugriff auf Kundendaten erhält. Bei der Genehmigung durch den Manager verfügt der Techniker über einen zeitlich begrenzten und begrenzten Zugriff auf Kundendaten, um am Kundenproblem zu arbeiten.

Kunden-Lockbox für Office 365 kann Ihnen helfen, Compliance-Verpflichtungen zu erfüllen, wie Sie in FedRAMP und HIPAA gefunden werden, wenn Sie Verfahren für die explizite Datenzugriffs Autorisierung benötigen. In den seltenen Fällen, in denen ein Microsoft-Dienst Techniker Zugriff auf Ihre Daten benötigt, gewähren Sie diesen Zugriff nur auf Daten, die zur Lösung des Problems und für einen begrenzten Zeitraum erforderlich sind. Vom Supporttechniker ausgeführte Aktionen werden zu Überwachungszwecken protokolliert und können über die [Office 365 Management Activity API](https://msdn.microsoft.com/library/office/dn707383.aspx) und das [Security and Compliance Center](http://protection.office.com/)aufgerufen werden. Kunden-Lockbox fügt den Kunden in den Lockbox-Genehmigungsprozess ein und bietet Ihnen die Möglichkeit, die Autorisierung von Microsoft Access zu Ihren Exchange Online-oder SharePoint Online-Inhalten für Dienstvorgänge zu steuern.

>**Hinweis**: Kunden-Lockbox ist in [Office 365 Enterprise E5](https://products.office.com/business/office-365-enterprise-e5-business-software) und als Add-on-Kauf verfügbar, aber manuelle maßnahmen müssen im Microsoft 365 Admin Center (unter Diensteinstellungen | Kunden-Lockbox), um Sie zu aktivieren. Weitere Informationen finden Sie unter [Office 365-Kunden](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)-lockBox-Anfragen.

Alle Dienstanforderungen für Exchange Online und SharePoint Online werden vom Lockbox-System verarbeitet. Und mit der Kunden-Lockbox wird jeder Dienstvorgang, der den Zugriff auf diese Dienste erfordert, mit der Exposition gegenüber Kundendaten durch den Lockbox-Genehmigungsprozess durchlaufen und dann dem Kunden ermöglicht, die Anforderung anschließend zu genehmigen oder abzulehnen.
 
*Abbildung 1: Kunden-Lockbox-Workflow*

Wenn die Anforderung vom Kunden abgelehnt wird, hat der Microsoft-Techniker keinen Zugriff auf die Inhalte des Kunden und kann den Dienstvorgang nicht abschließen. Wenn die Anforderung vom Kunden genehmigt wurde, hat der Microsoft-Techniker über überwachte und eingeschränkte Verwaltungsschnittstellen nur begrenzten Zugriff auf die Inhalte des Kunden. Sowohl mit Lockbox als auch mit der Kunden-Lockbox können alle genehmigten Zugriffe auf einen eindeutigen Benutzer zurückgeführt werden, wodurch Ingenieure für Ihre Kundendaten verantwortlich sind.

## <a name="just-in-time-access"></a>Just-in-Time-Zugriff
Microsoft verwendet das JIT-Zugriffs Prinzip (Just-in-Time) für Office 365, um das Risiko von Manipulationen von Anmeldeinformationen und lateralen Angriffen weiter zu verringern. JIT entfernt den beständigen administrativen Zugriff auf Dienste und ersetzt diese Ansprüche durch die Möglichkeit, diese Rollen bei Bedarf zu erhöhen. Das Entfernen beständiger Rechte von Administratoren stellt sicher, dass Anmeldeinformationen nur dann zur Verfügung stehen, wenn Sie benötigt werden, und entfernt das Risiko für das Unternehmen bei Diebstahl von Anmeldeinformationen.

Das JIT-Zugriffsmodell erfordert, dass Ingenieure erweiterte Rechte für einen begrenzten Zeitraum anfordern, um Verwaltungsaufgaben auszuführen. Darüber hinaus verwenden OCEs temporäre Konten, die mit vom computergenerierten komplexen Kennwörtern erstellt werden und nur die Rollen erhalten, mit denen Sie die erforderlichen Aufgaben ausführen können. Beispielsweise ist der von Lockbox erteilte administrative Zugriffzeit gebunden, und die Zeitdauer, die der Zugriff gewährt wird, hängt von der angeforderten Rolle ab. Ein Techniker gibt die Zeitdauer an, die während der Anforderung an das Lockbox-System benötigt wird. Das Lockbox-System lehnt Anforderungen ab, bei denen die angeforderte Zeit die maximal zulässige Zeit für die Ansicht überschreitet. Nach Ablauf der Ansichts Anforderung wird der Administratorzugriff entfernt, und das temporäre Konto ist abgelaufen.

Wenn für den Zugriff autorisiert und genehmigt (beispielsweise zum Debuggen eines Systems), erhalten Techniker ein einmaliges Verwaltungskennwort, das vom Autorisierungssystem generiert wird, wenn eine Anforderung für erhöhten Zugriff genehmigt wird. Dieses Kennwort wird vom Techniker in eine Kennwortsicherheit kopiert, ist von den Anmeldeinformationen des Ingenieurs für die Microsoft-Unternehmensumgebung getrennt und eignet sich nur für die Sitzung, für die der erweiterte Zugriff genehmigt wurde.

## <a name="constrained-management-interfaces"></a>Eingeschränkte Verwaltungsschnittstellen
OCEs verwenden zwei Verwaltungsschnittstellen, um Verwaltungsaufgaben auszuführen: Remote Desktop über gesicherte Terminal Service Gateways (G.t.s.) und Remote-PowerShell. Innerhalb dieser Verwaltungsschnittstellen gibt es Software Richtlinien und Zugriffssteuerungen, die erhebliche Einschränkungen bei der Ausführung von Anwendungen und den verfügbaren Befehlen und Cmdlets bieten. 

Office 365-Serverschränken gleichzeitige Sitzungen auf einen Teamadministrator pro Server ein. G.t.s. sind so konfiguriert, dass Sie nur eine einzelne gleichzeitige Sitzung für Benutzer zulassen und nicht mehrere Sitzungen zulassen. G.t.s. ermöglichen Office 365-Dienst Team Administratoren die gleichzeitige Verbindung mit mehreren Servern, wobei eine einzelne Sitzung pro Server verwendet wird, damit Administratoren ihre Aufgaben effektiv ausführen können. Dienst Team Administratoren haben keine Berechtigungen für die G.t.s. selbst. Die TSG wird nur verwendet, um die mehrstufige Authentifizierung (MFA) und Verschlüsselungsanforderungen zu erzwingen. Sobald der Dienst Teamadministrator eine Verbindung mit einem bestimmten Server über eine TSG herstellt, erzwingt der jeweilige Server eine Sitzungs Grenze pro Administrator.

Nutzungseinschränkungen und Verbindungs-und Konfigurationsanforderungen für Office 365-Mitarbeiter werden durch Active Directory-Gruppenrichtlinien festgelegt. Zu diesen Richtlinien gehört Folgendes:
- G.t.s. sind so konfiguriert, dass nur [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2-validierte Verschlüsselung verwendet wird
- TSG-Sitzungen sind so konfiguriert, dass Sie nach 30 Minuten der Inaktivität getrennt werden
- TSG-Sitzungen sind so konfiguriert, dass Sie nach 24 Stunden automatisch abgemeldet werden.

Verbindungen mit G.t.s. erfordern auch MFA mit einer separaten physischen Smartcard und einem Konto, das von den Microsoft-Unternehmensanmeldeinformationen des Entwicklers getrennt ist. Ingenieuren werden verschiedene Smartcards für verschiedene Plattformen und geheime Verwaltungsplattformen für die sichere Speicherung von Anmeldeinformationen erteilt. G.t.s. verwenden Active Directory-Gruppenrichtlinien, um zu steuern, wer sich bei Remoteservern anmelden kann, die Anzahl der zulässigen Sitzungen und die Einstellungen für Leerlauftimeouts. Weitere Richtlinien sind vorhanden, um den Zugriff auf zulässige Anwendungen zu begrenzen und den Internet Zugriff zu beschränken.

Zusätzlich zum Remotezugriff mithilfe von speziell konfigurierten G.t.s. ermöglicht Exchange Online Benutzern mit der Rolle "Service Engineer" den Zugriff auf bestimmte Verwaltungsfunktionen auf Produktionsservern mithilfe von Remote-PowerShell. Hierzu muss der Benutzer für schreibgeschützten Zugriff (Debug) auf die Office 365-Produktionsumgebung autorisiert sein. Die Berechtigungseskalation wird auf die gleiche Weise aktiviert, wie Sie für G.t.s. mit dem Lockbox-Prozess aktiviert ist.

Für den Remotezugriff gibt es in jedem Rechenzentrum eine virtuelle IP mit Lastenausgleich, die als einzelner Zugriffspunkt dient. Die Remote-PowerShell-Cmdlets, die ausgeführt werden können, basieren auf der Berechtigungsstufe, die in dem während der Authentifizierung erhaltenen Zugriffs Anspruchs identifiziert wurde. Diese Cmdlets sind die einzigen Verwaltungsfunktionen, auf die von Benutzern, die mit dieser Methode eine Verbindung herstellen, zugegriffen und ausgeführt werden kann. Remote-PowerShell wird verwendet, um den Umfang der verfügbaren Befehle für den Techniker einzuschränken, der auf der Zugriffsebene basiert, die über den Lockbox-Prozess gewährt wird. In Exchange Online kann beispielsweise Get-Mailbox verfügbar sein, aber Set-Mailbox nicht.
