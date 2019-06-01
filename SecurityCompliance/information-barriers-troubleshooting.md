---
title: Problembehandlung bei Informationsbarrieren
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Verwenden Sie diesen Artikel als Leitfaden für die Problembehandlung von Informationsbarrieren.
ms.openlocfilehash: b37585469ec8bb299b7976f8a330f4c6b29e3f95
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668301"
---
# <a name="troubleshooting-information-barriers-preview"></a>Problembehandlung bei Informationsbarrieren (Vorschau)

Informationsbarrieren können dazu beitragen, dass Ihre Organisation weiterhin den gesetzlichen Bestimmungen und Branchenvorschriften entspricht. Beispielsweise können Sie mit Informationsbarrieren die Kommunikation zwischen bestimmten Benutzergruppen einschränken, um einen Interessenkonflikt oder andere Probleme zu vermeiden. Weitere Informationen finden Sie unter [Information Barriers (Preview)](information-barriers.md).

Dieser Artikel enthält Anleitungen, die Sie verwenden können, um Antworten auf Fragen zu erhalten oder Probleme zu beheben, die mit Informationsbarrieren auftreten können.  

## <a name="before-you-begin"></a>Bevor Sie beginnen...

Um die in diesem Artikel beschriebenen Aufgaben ausführen zu können, muss Ihnen eine entsprechende Rolle zugewiesen sein, beispielsweise eine der folgenden:
- Microsoft 365 Enterprise-Global-Administrator
- Office 365 globaler Administrator
- Complianceadministrator
- IB-Konformitätsverwaltung (Dies ist eine neue Rolle!)

Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Berechtigungen im Office 365 Security #a0 Compliance Center](permissions-in-the-security-and-compliance-center.md).

Weitere Informationen zu den Voraussetzungen für Informationsbarrieren finden Sie unter Prerequisites [(for Information Barrier Policies)](information-barriers-policies.md#prerequisites).

Stellen Sie außerdem sicher, dass Sie [eine Verbindung mit Office 365 Security #a0 Compliance Center PowerShell herstellen](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a>Problem: Personen werden unerwartet für die Kommunikation in Microsoft Teams blockiert 

In diesem Fall melden Personen unerwartete Probleme, die in Microsoft Teams miteinander kommunizieren. Beispiele:
- Ein Benutzer kann keinen anderen Benutzer in Microsoft Teams finden oder mit ihm kommunizieren.
- Ein Benutzer kann einen anderen Benutzer in Microsoft Teams nicht anzeigen oder auswählen.
- Ein Benutzer kann Nachrichten an einen anderen Benutzer in Microsoft Teams anzeigen, aber nicht senden.

### <a name="what-to-do"></a>Nächste Schritte

1. Bestimmen Sie, ob die Benutzer von einer Informations Sperrrichtlinie betroffen sind. Verwenden Sie dazu das Cmdlet **Get-InformationBarrierRecipientStatus** mit dem Parameter Identity. 

    Die Syntax lautet`Get-InformationBarrierRecipientStatus -Identity`

    Sie können jeden Identitätswert verwenden, der jeden Empfänger eindeutig identifiziert, beispielsweise Name, Alias, DN (Distinguished Name), kanonischer DN, e-Mail-Adresse oder GUID.

    Beispiel: `Get-InformationBarrierRecipientStatus -Identity meganb`

    In diesem Beispiel wird ein Alias (*meganb*) für den Parameter Identity verwendet. Dieses Cmdlet gibt Informationen zurück, die angeben, ob der Benutzer von einer Richtlinie für Informationsbarrieren betroffen ist. (Suchen Sie nach * ExoPolicyId \<: GUID>.)

    Wenn die Benutzer nicht in Richtlinien für Informationsbarrieren enthalten sind, wenden Sie sich an den Support. Führen Sie andernfalls die nächste Aktion aus.

2. Finden Sie heraus, welche Segmente in einer Informations Sperrrichtlinie enthalten sind. Verwenden Sie dazu das `Get-InformationBarrierPolicy` Cmdlet mit dem Parameter Identity. Verwenden Sie Details wie die Richtlinien-GUID (ExoPolicyId), die Sie während des vorherigen Schritts erhalten haben, als Identitätswert.

    Beispiel: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`

    In diesem Beispiel werden detaillierte Informationen zur Richtlinie mit Informationsbarrieren abgerufen, die ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*enthält.
    
    Suchen Sie nach dem Ausführen des Cmdlets in den Ergebnissen nach **AssignedSegment**-, **SegmentsAllowed**-und **SegmentsBlocked** -Werten.

    Beispiel: nach dem Ausführen `Get-InformationBarrierPolicy` des Cmdlets haben wir in der Ergebnisliste Folgendes gesehen:

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    In diesem Fall können wir sehen, dass eine Informations Barriere-Richtlinie Personen betrifft, die sich in den Segmenten Vertrieb und Forschung befinden. In diesem Fall werden Personen im Vertrieb daran gehindert, mit Personen in der Forschung zu kommunizieren. Wenn dies richtig erscheint, funktionieren Informationsbarrieren wie erwartet. Wenn dies nicht der Fall ist, fahren Sie mit dem nächsten Schritt fort.

4. Stellen Sie sicher, dass ihre Segmente ordnungsgemäß definiert sind. Verwenden Sie dazu das `Get-OrganizationSegment` Cmdlet, und überprüfen Sie die Ergebnisliste. 

    Um Details für ein bestimmtes Segment anzuzeigen, verwenden Sie `Get-OrganizationSegment` das-Cmdlet mit einem Identity-Parameter. 

    Beispiel: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`

    In diesem Beispiel werden Informationen zu dem Segment abgerufen, das über GUID- *c96e0837-C232-4a8a-841e-ef45787d8fcd*verfügt.

    Überprüfen Sie die Details für das Segment. Bearbeiten Sie bei Bedarf [ein Segment](information-barriers-policies.md#edit-a-segment), und verwenden Sie dann das `Start-InformationBarrierPoliciesApplication` Cmdlet erneut.

    Wenn Sie weiterhin Probleme mit ihrer Richtlinie zu Informationsbarrieren haben, wenden Sie sich an den Support.
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a>Problem: der Anwendungsprozess für Informationsbarrieren dauert zu lange.

Nach dem Ausführen des Cmdlets **Start-InformationBarrierPoliciesApplication** dauert es sehr lange, bis der Vorgang abgeschlossen ist.

### <a name="what-to-do"></a>Nächste Schritte

1. Beachten Sie, dass beim Ausführen des Cmdlets für die Richtlinienanwendung für alle Konten in Ihrer Organisation Richtlinien für Informationsbarrieren angewendet (oder entfernt) werden, Benutzer nach Benutzer. Wenn Sie viele Benutzer haben, dauert es eine Weile, bis Sie verarbeitet werden. (Als allgemeine Richtlinie dauert es etwa eine Stunde, 5.000-Benutzerkonten zu verarbeiten.) 

2. Verwenden Sie das Cmdlet **Get-InformationBarrierPoliciesApplicationStatus** , um den Status zu überprüfen.

    Syntax`Get-InformationBarrierPoliciesApplicationStatus`

    Verwenden Sie zum Anzeigen des Status für alle Richtlinien Anwendungen für Informationsbarrieren`Get-InformationBarrierPoliciesApplicationStatus -All $true`

    Dadurch werden Informationen darüber angezeigt, ob die Richtlinienanwendung abgeschlossen, ein Fehler aufgetreten ist oder ausgeführt wird..

3. Führen Sie je nach den Ergebnissen von Schritt 2 einen der folgenden Schritte aus:

    - Wenn die Anwendung nicht gestartet wurde und seit der Ausführung des **Start-InformationBarrierPoliciesApplication-** Cmdlets mehr als 45 Minuten dauern, überprüfen Sie Ihr Überwachungsprotokoll, um zu ermitteln, ob Fehler in Richtlinien Definitionen vorliegen, oder aus einem anderen Grund, warum die die Anwendung wurde nicht gestartet.

    - Wenn die Anwendung fehlgeschlagen ist, überprüfen Sie Ihre Segmente und Richtlinien. Bearbeiten Sie gegebenenfalls [Segmente](information-barriers-policies.md#edit-a-segment) und/oder [Bearbeiten Sie Richtlinien](information-barriers-policies.md#edit-a-policy), und führen Sie dann das Cmdlet **Start-InformationBarrierPoliciesApplication** erneut aus.

    - Wenn die Anwendung noch ausgeführt wird, lassen Sie mehr Zeit für ihre Ausführung zu. Wenn es sich um mehrere Tage handelt, wenden Sie sich an den Support.

## <a name="related-topics"></a>Verwandte Themen

[Definieren von Richtlinien für Informationsbarrieren in Microsoft Teams (Vorschau)](information-barriers-policies.md)

[Informationsbarrieren (Vorschau)](information-barriers.md)



