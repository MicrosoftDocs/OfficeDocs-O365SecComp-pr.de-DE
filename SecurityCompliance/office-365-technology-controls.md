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
ms.openlocfilehash: ce2e09ce7db881197d2598c52283ecde7ed46e61
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622435"
---
# <a name="office-365-technology-controls"></a>Technologiesteuerungen in Office 365 

Microsoft verwendet verschiedene Tools und Technologien, um den Zugriff auf Kundendaten in den Onlinediensten zu steuern, zu verwalten und zu überwachen. Diese gelten für Exchange Online, SharePoint Online, Lockbox und Kunden-Lockbox, mehrstufige Authentifizierung und vieles mehr. Jammern verwendet ähnliche Steuerelemente, die in jammern von [Unternehmens Zugriffssteuerungen](office-365-yammer-enterprise-access-controls.md)beschrieben werden.

Office 365 Ingenieure haben keinen ständigen Zugriff auf Office 365 Kundendaten. Ingenieure müssen einen Microsoft-Genehmigungsprozess durchlaufen, bevor der Zugriff auf Kundendaten für Dienstvorgänge erfolgt. Wenn der Kunde das Feature "Kunden-Lockbox" für Exchange Online und SharePoint Online lizenziert, erfordert der Zugriff auf Kundendaten eine Kundengenehmigung. Nach genehmigten dienstspezifischen Administratorkonten werden just-in-Time-Zugriff für Aufgaben, die für die Dienstanforderung erforderlich sind, zur Verfügung gestellt.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox und Kunden-Lockbox

Obgleich selten, kann ein Kunde Unterstützung von Microsoft anfordern, die Kunden Inhalte für einen Microsoft-Techniker verfügbar macht. Um den Zugriff auf Exchange Online zu steuern, verwendet Microsoft ein Zugriffs Steuerungssystem namens Lockbox. Bevor Microsoft Engineer auf Exchange Online-oder SharePoint Online Systeme oder-Daten zugreift, müssen Sie eine Zugriffsanforderung mithilfe von Lockbox übermitteln. Alle Dienstanforderungen für Exchange Online und SharePoint Online werden vom Lockbox-System verarbeitet. Mit Lockbox und Customer Lockbox ist der zugelassene Zugriff auf einen eindeutigen Benutzer zurückzuführen, sodass Ingenieure für die Verarbeitung von Kundendaten verantwortlich sind.

> [!NOTE]
> Exchange Online enthält alle Skype for Business Daten, die in Benutzerpostfächern gespeichert sind. Skype for Business Abdeckung umfasst keine Skype Meeting-Broadcast-Aufzeichnungen oder Inhalte, die von Benutzern in Besprechungen hochgeladen werden. SharePoint Online enthält OneDrive für Unternehmen.

Lockbox verarbeitet Anforderungen für Berechtigungen, die es Ingenieuren ermöglichen, Betriebs-und Verwaltungsfunktionen innerhalb des Diensts auszuführen. Ingenieure senden Anforderungen über Lockbox, und ein Microsoft-Manager muss die Anforderung genehmigen, bevor der Techniker auf Kundendaten zugreifen kann. Nach der Genehmigung des Managers verfügt der Techniker über einen zeitlich begrenzten und Bereichs beschränkten Zugriff auf Kundendaten, um das Problem des Kunden zu bearbeiten.

Kunden-Lockbox für Office 365 hilft Ihnen bei der Erfüllung von Compliance-Verpflichtungen, wenn Sie Verfahren für die explizite Datenzugriffs Autorisierung benötigen. Dies ist eine Voraussetzung für einige Compliance-Standards wie FedRAMP und HIPAA. Kunden-Lockbox fügt Sie in den Lockbox-Genehmigungsprozess ein und bietet Ihnen die Möglichkeit, die Autorisierung von Microsoft-Zugriff auf Ihre Exchange Online zu steuern oder Inhalte für Dienstvorgänge SharePoint Online.

In den seltenen Fällen, in denen ein Microsoft-Dienst Techniker auf Ihre Daten zugreifen muss, gewähren Sie nur Zugriff auf Daten, die zur Behebung des Problems und für einen begrenzten Zeitraum erforderlich sind. Wenn Sie eine Zugriffsanforderung ablehnen, haben Microsoft-Techniker keinen Zugriff auf Ihre Inhalte und können keine Dienstvorgänge ausführen. Wenn Sie die Anforderung genehmigen, haben Microsoft-Techniker einen begrenzten Just-in-Time-Zugriff auf Ihre Inhalte über überwachte und eingeschränkte Verwaltungsschnittstellen.

Vom Supporttechniker ausgeführte Aktionen werden zu Überwachungszwecken protokolliert und sind über die [Office 365 Verwaltungs Aktivitäts-API](https://msdn.microsoft.com/library/office/dn707383.aspx) und das [Security and Compliance Center](http://protection.office.com/)zugänglich.

>[!NOTE]
> Kunden-Lockbox steht in [Office 365 Enterprise E5](https://products.office.com/business/office-365-enterprise-e5-business-software) als Add-on-Kauf zur Verfügung. Weitere Informationen finden Sie unter [Office 365 Kunden](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)-Lockbox-Anforderungen.

## <a name="just-in-time-access"></a>Just-in-Time-Zugriff

Microsoft verwendet das JIT-Zugriffs Prinzip (Just-in-Time) für Office 365, um Manipulations Risiken und laterale Angriffe durch Anmeldeinformationen zu verringern. JIT entfernt persistenten administrativen Zugriff auf Dienste und ersetzt die Berechtigungen durch die Möglichkeit, diese Rollen bei Bedarf zu erhöhen. Durch das Entfernen von beständigen Zugriffsrechten von Administratoren wird sichergestellt, dass Anmeldeinformationen nur dann verfügbar sind, wenn Sie benötigt werden und das Risiko von Diebstahlschutz

Für das JIT-Zugriffsmodell müssen Ingenieure für einen begrenzten Zeitraum erhöhte Berechtigungen anfordern, um Verwaltungsaufgaben auszuführen. Darüber hinaus verwenden Ingenieure temporäre Konten, die mit maschinell generierten komplexen Kennwörtern erstellt wurden, und erteilt nur die Rollen, die es Ihnen ermöglichen, erforderliche Aufgaben auszuführen. Beispielsweise ist der von Lockbox erteilte administrative Zugriffzeit gebunden, und die Zeitspanne, die der Zugriff gewährt wird, hängt von der angeforderten Rolle ab. Ein Techniker gibt die Zeitdauer an, die der Zugriff in der Anforderung an das Lockbox-System benötigt. Das Lockbox-System lehnt Anforderungen ab, wenn die angeforderte Zeit die maximal zulässige Zeit für die Ansicht überschreitet. Nach Ablauf dieses Zeitraums wird der Administratorzugriff entfernt, und das temporäre Konto läuft ab.

Wenn autorisiert und für den Zugriff genehmigt, erhalten Ingenieure ein einmaliges Administratorkennwort, das vom Autorisierungssystem generiert wird. Jedes Mal, wenn eine Anforderung für erhöhten Zugriff genehmigt wird, werden neue Kennwörter generiert. Das Kennwort wird in ein sicheres Kennwort kopiert, unterscheidet sich von den Anmeldeinformationen des Ingenieurs für die Microsoft-Unternehmensumgebung und ist nur für die genehmigte Sitzung mit erhöhten Zugriffsrechten geeignet.

## <a name="constrained-management-interfaces"></a>Eingeschränkte Verwaltungsschnittstellen

Ingenieure verwenden zwei Verwaltungsschnittstellen, um administrative Aufgaben auszuführen: Remote Desktop über gesicherte Terminal Dienst Gateways (g.t.s.) und Remote-PowerShell. In diesen Verwaltungsschnittstellen stellen Software Richtlinien und Zugriffssteuerungen erhebliche Einschränkungen hinsichtlich der ausgeführten Anwendungen und der verfügbaren Befehle und Cmdlets dar.

Office 365 Server beschränken gleichzeitige Sitzungen auf eine Sitzung pro Dienst-Teamadministrator pro Server. G.t.s. erlauben nur eine einzelne gleichzeitige Sitzung für Benutzer und erlauben nicht mehrere Sitzungen. Mithilfe einer einzelnen Sitzung pro Server können g.t.s. Office 365 Dienst Team Administratoren gleichzeitig eine Verbindung mit mehreren Servern herstellen, damit Administratoren ihre Aufgaben effektiv ausführen können. Dienst Team Administratoren besitzen keine Berechtigungen für das g.t.s. selbst. Die TSG wird nur zum Erzwingen der mehrstufigen Authentifizierung (MFA) und der Verschlüsselungsanforderungen verwendet. Sobald der Dienst Teamadministrator eine Verbindung mit einem bestimmten Server über eine TSG herstellt, erzwingt der jeweilige Server einen Sitzungs Grenzwert von einem pro Administrator.

Nutzungseinschränkungen sowie Verbindungs-und Konfigurationsanforderungen für Office 365 Personal werden durch Active Directory Gruppenrichtlinien festgelegt. Diese Richtlinien umfassen die folgenden Merkmale:

- G.t.s. verwenden nur [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2 validierte Verschlüsselung.
- TSG-Sitzungen werden nach 30 Minuten Inaktivität getrennt.
- TSG-Sitzungen werden nach 24 Stunden automatisch abgemeldet.

Verbindungen zu g.t.s. erfordern auch MFA unter Verwendung einer separaten physischen Smartcard und eines Kontos, das von den Microsoft-Unternehmensanmeldeinformationen des Ingenieurs getrennt ist. Ingenieure erhalten unterschiedliche Smartcards für verschiedene Plattformen und geheime Verwaltungsplattformen stellen eine sichere Speicherung von Anmeldeinformationen sicher. G.t.s. verwenden Sie Active Directory Gruppenrichtlinien, um zu steuern, wer sich an Remoteservern anmelden kann, die Anzahl der zulässigen Sitzungen und Einstellungen für Leerlauftimeouts. Zusätzliche Richtlinien beschränken den Zugriff auf zugelassene Anwendungen und beschränken den Internet Zugriff.

Zusätzlich zum Remotezugriff mit speziell konfigurierten g.t.s. ermöglicht Exchange Online Benutzern mit der Rolle "Dienst Techniker" den Zugriff auf bestimmte administrative Funktionen auf Produktionsservern mithilfe von Remote-PowerShell. Hierzu muss der Benutzer für den schreibgeschützten Zugriff (Debug) auf die Office 365 Produktionsumgebung autorisiert sein. Die Berechtigungseskalation wird auf die gleiche Weise wie für g.t.s. mit dem Lockbox-Prozess aktiviert.

Für den Remotezugriff verfügt jedes Rechenzentrum über eine virtuelle Lastenausgleichs-IP, die als einzelne Zugriffspunkt dient. Die verfügbaren Remote-PowerShell-Cmdlets basieren auf der Berechtigungsstufe, die in dem bei der Authentifizierung erhaltenen Zugriffs Anspruch angegeben ist. Diese Cmdlets bieten die einzige Verwaltungsfunktionalität, auf die Benutzer zugreifen können, die über diese Methode eine Verbindung herstellen. Remote-PowerShell schränkt den Umfang der Befehle ein, die dem Techniker zur Verfügung stehen, und basiert auf der Zugriffsebene, die über den Lockbox-Prozess gewährt wird. Beispielsweise ist in Exchange Online das Get-Mailbox möglicherweise verfügbar, aber das Festlegen von "Postfach" nicht.
