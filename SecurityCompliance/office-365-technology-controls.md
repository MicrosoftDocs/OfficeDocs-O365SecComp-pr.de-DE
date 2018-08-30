---
title: Steuerelemente für Office 365-Technologie
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
description: 'Zusammenfassung: Eine Übersicht über Microsoft Technologie Steuerelement Methoden für Office 365.'
ms.openlocfilehash: 2ef04b558f5fa82075d9aa602b83d437aa4b2ee6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529340"
---
# <a name="office-365-technology-controls"></a>Steuerelemente für Office 365-Technologie 

Microsoft verwendet mehrere Tools und -Technologien zu steuern, verwalten und Überwachen des Zugriffs auf Kundendaten in Exchange Online und SharePoint Online, einschließlich Lockbox und Kunden Lockbox und mehrstufige Authentifizierung. Yammer Enterprise ähnliche Steuerelemente verwendet, wie beschrieben in [Yammer Enterprise zugreifen auf Steuerelemente](office-365-yammer-enterprise-access-controls.md).

Office 365 Ingenieure haben NULL stehende Zugriff auf Office 365-Kundendaten und sie müssen Durchlaufen eines Genehmigungsprozesses, die Microsoft und – falls der Kunde das Kunden Lockbox-Feature für Exchange Online und SharePoint Online lizenziert – enthält Kunden Genehmigung, vor dem Zugriff auf Kundendaten für Dienstvorgänge auftreten kann. Genehmigung erteilt, sind dienstspezifische Administratorkonten bereitgestellten just-in-Time mit der ausreichenden Zugriff auf die Anforderung an den erforderlichen Aufgaben ausführen.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox und Kunden Lockbox
Obwohl es äußerst selten ist, konnte ein Kunde Unterstützung von Microsoft anfordern, die ein Microsoft-Supportmitarbeiter auf Inhalt des Kunden, die sie ein Problem unterstützen verfügbar machen können. Zum Steuern des Zugriffs auf Exchange Online (einschließlich Skype für Geschäftsdaten in die Postfächer der Benutzer (Skype für Business Disposition enthält keine Skype Besprechung übertragen Aufzeichnungen und Besprechungen von Benutzern hochgeladene Inhalte)) und SharePoint Online (die umfasst OneDrive für Unternehmen), Microsoft verwendet eine Access-Verwaltungssystem Lockbox aufgerufen. Bevor alle Microsoft-Supportmitarbeiter alle Exchange Online oder SharePoint Online-Systeme oder Daten zugreifen kann, müssen sie eine Access-Anforderung mit Lockbox senden. Verwendung von Lockbox ist für alle mit erhöhten Rechten Zugriff auf Exchange Online oder SharePoint Online erforderlich.

Lockbox verarbeitet Anforderungen von Berechtigungen, die Ingenieure die Möglichkeit zum Ausführen der Betriebs- und Funktionen innerhalb des Dienstes gewähren. Ingenieure Submit Anforderungen über Lockbox, die von einem Manager vor der Engineer erhalten die Möglichkeit, die Kundendaten zugreifen genehmigt werden müssen. Nach der Genehmigung Manager hat der Engineer zeitlich begrenzte Kampagnen sowie Bereich zeitlich begrenzte Zugriff auf Kundendaten an das Problem des Kunden arbeiten.

Kunden-Lockbox für Office 365 helfen Ihnen bei Erfüllung von behördlichen Auflagen, beispielsweise in FedRAMP und HIPAA, wenn Sie Verfahren für die Autorisierung explizite Daten benötigen. Wenn ein Microsoft-Dienst Engineer Zugriff auf Ihre Daten benötigt, gewähren Sie in dem seltenen Fall, dass der Zugriff nur für Daten erforderlich, um dieses Problem zu beheben und für eine begrenzte Zeitspanne. Aktionen, die von der Supporttechniker für Überprüfungszwecken angemeldet sind und über die [Office 365-Verwaltungs-Aktivität API](https://msdn.microsoft.com/library/office/dn707383.aspx) und die [Sicherheit und Compliance Center](http://protection.office.com/)zugegriffen werden. Kunden-Lockbox Kunden in den Genehmigungsprozess Lockbox eingefügt und bietet ihnen die Möglichkeit zum Steuern der Autorisierung von Microsoft Access auf ihren Exchange Online oder SharePoint Online-Inhalte für Vorgänge des Diensts.

>**Hinweis**: Kunden Lockbox in [Office 365 Enterprise E5](https://products.office.com/business/office-365-enterprise-e5-business-software) und als Kauf eines Add-on verfügbar ist, aber manuelle Schritte muss in der Office 365-Verwaltungskonsole unternommen werden (unter Diensteinstellungen | Kunden-Lockbox) zu aktivieren. Weitere Informationen finden Sie unter [Office 365 Lockbox Kundenanfragen](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

Alle Anfragen für Exchange Online und SharePoint Online werden vom System Lockbox behandelt. Mit Kunden-Lockbox alle des Diensts anzuzeigen, das Zugriff auf diese Dienste zu machen, Kundendaten erfordert wird über den Genehmigungsprozess Lockbox, und dann wird der Kunde genehmigen oder Ablehnen der Anforderung danach aktiviert.
 
*Abbildung 1: Kunden Lockbox Workflow*

Wenn die Anforderung durch den Kunden zurückgewiesen wird, der Microsoft-Mitarbeiter haben keinen Zugriff auf Inhalt des Kunden und werden nicht den Dienstvorgang abzuschließen. Wenn die Anforderung vom Kunden genehmigt wird, hat der Microsoft-Mitarbeiter wird Just-in-Time-Zugriff auf der Kunde seinen Inhalt über überwachte und eingeschränkte Verwaltungsschnittstellen begrenzt. Mit Lockbox und Kunden Lockbox erfolgt der Zugriff genehmigter nachverfolgbare auf eine eindeutige Benutzer, Ingenieure verantwortlich für die Handhabung von Kundendaten vornehmen.

## <a name="just-in-time-access"></a>Just-in-Time-Zugriff
Microsoft verwendet das Just-in-Time (JUST-in) Access Prinzip für Office 365 weiter von Anmeldeinformationen Manipulation und seitlichen Angriffe gemindert. JIT entfernt persistenten administrativen Zugriff auf die Dienste und ersetzt diese Berechtigungen durch die Möglichkeit, die in diesen Rollen bei Bedarf zu erhöhen. Entfernen von persistent Rechte von Administratoren wird sichergestellt, dass Anmeldeinformationen verfügbar sind, nur wenn sie benötigt werden, und dem Risiko, dass für das Unternehmen in Fällen von den Diebstahl entfernt.

Das Zugriffsmodell JIT erfordert Ingenieure erhöhte Berechtigungen zum Ausführen von Verwaltungsaufgaben für eine begrenzte anfordern. Darüber hinaus OCEs verwenden temporäre Konten, die mit komplexen Kennwörtern computergenerierte erstellt werden und nur die Rollen, die sie zum Ausführen der erforderlichen Aufgaben können erteilt. Beispielsweise administrativer Zugriff mit Lockbox Zeit gebunden ist, und die Zeitspanne, die der Zugriff gewährt wird, hängt von der Rolle angefordert wird. Ein Techniker gibt die Dauer des Zeit-Zugriff während der Anforderung an das System Lockbox benötigt. Das System Lockbox lehnt Anfragen, in denen die Zeit angefordert die maximal zulässige Zeit für die Erhöhung überschreiten. Nach Ablauf der Anforderung Elevation Verwaltungszugriff entfernt, und das temporäre Konto ist abgelaufen.

Wenn autorisiert und für den Zugriff (beispielsweise Debuggen des Systems) genehmigt, empfangen Ingenieure ein einmaliges administrative Kennwort, das vom Autorisierungssystem jedes Mal generiert wird, die eine Anforderung für den Zugriff mit erhöhten Rechten genehmigt wurde. Das Kennwort in einem sicheren Kennwort vom Techniker kopiert wird, unterscheidet sich von der Techniker Anmeldeinformationen für die Microsoft-Umgebung im Unternehmen und gilt nur für die Sitzung für die Zugriff mit erhöhten Rechten genehmigt wurde.

## <a name="constrained-management-interfaces"></a>Eingeschränkte Verwaltungsschnittstellen
OCEs beiden Verwaltungsschnittstellen für administrative Aufgaben verwenden: Remote Desktop durch gesicherte Terminal Service Gateways (TSGs) und Remote-PowerShell. In diesen Management sind Schnittstellen, die Softwarerichtlinien und Zugreifen auf Steuerelemente, die platzieren erhebliche Einschränkungen für welche Anwendungen ausgeführt werden können und welche Befehle und Cmdlets sind verfügbar. 

Server mit Office 365 einschränken gleichzeitige Sitzungen auf einem Sitzung pro Service-Team-Administrator pro Server. TSGs sind so konfiguriert, dass nur eine einzige gleichzeitige Sitzung für Benutzer zulassen, und lassen sie nicht mehrerer Sitzungen. TSGs ermöglichen Office 365 Team Dienstadministratoren gleichzeitig auf mehreren Servern verbinden mit einer einzigen Sitzung pro Server, damit Administratoren effektiv ihrer Aufgaben ausführen können. Team Dienstadministratoren verfügen keine Berechtigungen auf der TSGs selbst. Der TSG wird nur zum Erzwingen der mehrstufigen Authentifizierung (mehrstufiger Authentifizierung das) und Anforderungen für die Verschlüsselung verwendet. Sobald eine Team Dienstadministrator zu einem bestimmten Server über eine TSG Verbindung wird der angegebenen Server Sitzung maximal eine pro Administrator erzwungen.

Verwendung Einschränkungen und Anforderungen Verbindung und Konfiguration für Office 365-Personal werden von Active Directory-Gruppenrichtlinien festgelegt. Diese Richtlinien umfassen die folgenden Merkmale:
- TSGs sind so konfiguriert, dass nur [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2 überprüften Verschlüsselung verwenden
- TSG Sitzungen sind so konfiguriert, dass nach 30 Minuten Inaktivität trennen
- TSG Sitzungen werden automatisch anmelden deaktiviert nach 24 Stunden konfiguriert

Verbindungen mit TSGs sind ebenfalls mehrstufiger Authentifizierung das Verwenden einer separaten physischen Smartcard und ein Konto, das von der Techniker Microsoft Unternehmensanmeldeinformationen getrennt ist erforderlich. Ingenieure werden verschiedene Smart Karten für verschiedene Plattformen ausgestellt und Secrets Management-Plattformen werden verwendet, um sichere Speicherung von Anmeldeinformationen sicherzustellen. TSGs mithilfe von Gruppenrichtlinien für Active Directory steuern, wer auf Remoteservern, die Anzahl zulässiger Sitzungen und im Leerlauf Timeouteinstellungen anmelden können. Zusätzliche Richtlinien sind direkten Zugriff auf zulässige Applications und Internetzugang einschränken beschränken.

Zusätzlich zu den Remotezugriff mit speziell konfigurierten TSGs ermöglicht Exchange Online Benutzer mit der Rolle Engineer Dienstvorgänge bestimmte administrative Funktionen auf Produktionsservern mit Remote-PowerShell zugreifen. Hierzu muss der Benutzer für den schreibgeschützten (Debug) Zugriff auf die Office 365-produktionsumgebung autorisiert sein. Ausweitung von Berechtigungen ist die gleiche Weise, wie sie für TSGs mithilfe des Prozesses Lockbox aktiviert ist aktiviert.

Für den Remotezugriff ist vorhanden eine Lastenausgleich virtuelle IP-Adresse in jedem Rechenzentrum, das als einen einzigen Zugriffspunkt dient. Die Remote-PowerShell-Cmdlets, die ausgeführt werden können, basieren auf der Berechtigungsstufe, die in den Access Anspruch abgerufen, die während der Authentifizierung identifiziert. Diese Cmdlets sind die nur Verwaltungsfunktionen, die Zugriff auf und von Benutzern, die eine Verbindung mit dieser Methode ausgeführt werden kann. Remote-PowerShell wird zum Einschränken des Bereichs von Befehlen für die Engineer verfügbar, die über den Prozess Lockbox erteilt Zugriffsebene basiert. Beispielsweise in Exchange Online, Get-Mailbox ist möglicherweise verfügbar, jedoch Set-Mailbox nicht würde.
