---
title: Problembehandlung bei Informationsbarrieren
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/24/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Verwenden Sie diesen Artikel als Leitfaden für die Problembehandlung von Informationsbarrieren.
ms.openlocfilehash: e8750358aaa7788c85f0ab656b30f5b5149d898c
ms.sourcegitcommit: 044003455eb36071806c9f008ac631d54c64dde6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2019
ms.locfileid: "35199512"
---
# <a name="troubleshooting-information-barriers-preview"></a>Problembehandlung bei Informationsbarrieren (Vorschau)

[Informationsbarrieren (Preview)](information-barriers.md) können dazu beitragen, dass Ihre Organisation weiterhin den gesetzlichen Anforderungen und Branchenvorschriften entspricht. Beispielsweise können Sie mit Informationsbarrieren die Kommunikation zwischen bestimmten Benutzergruppen einschränken, um einen Interessenkonflikt oder andere Probleme zu vermeiden. (Weitere Informationen zum Einrichten von Informationsbarrieren finden Sie unter [define Policies for Information Barriers (Preview)](information-barriers-policies.md).)

Für den Fall, dass Personen aufgrund von Informationsbarrieren unerwartete Probleme haben, können Sie einige Schritte zur Lösung dieser Probleme durchführen. Verwenden Sie diesen Artikel als Leitfaden.

> [!IMPORTANT]
> Um die in diesem Artikel beschriebenen Aufgaben ausführen zu können, muss Ihnen eine entsprechende Rolle zugewiesen sein, beispielsweise eine der folgenden:<br/>-Microsoft 365 Enterprise-Global-Administrator<br/>-Office 365 globaler Administrator<br/>-Compliance-Administrator<br/>-IB-Compliance-Management (Dies ist eine neue Rolle!)<p>Weitere Informationen zu den Voraussetzungen für Informationsbarrieren finden Sie unter Prerequisites [(for Information Barrier Policies)](information-barriers-policies.md#prerequisites).<p>Stellen Sie sicher, dass Sie [eine Verbindung mit Office 365 Security #a0 Compliance Center PowerShell herstellen](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

## <a name="issue-communications-are-allowed-between-users-who-should-be-blocked-in-microsoft-teams"></a>Problem: Kommunikationen zwischen Benutzern, die in Microsoft Teams blockiert werden sollten, sind zulässig.

In diesem Fall sind zwar Informationsbarrieren definiert, aktiv und angewendet, aber Personen, die nicht miteinander kommunizieren sollten, können sich irgendwie in Microsoft Teams befinden.

### <a name="what-to-do"></a>Nächste Schritte

Stellen Sie sicher, dass die fraglichen Benutzer in einer Informations Sperrrichtlinie enthalten sind. 

1. Verwenden Sie das Cmdlet **Get-InformationBarrierRecipientStatus** mit Identitäts Parametern.

    Syntax`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` 

    Sie können einen beliebigen Wert verwenden, der jeden Benutzer eindeutig identifiziert, beispielsweise Name, Alias, Distinguished Name, kanonischer Domänenname, e-Mail-Adresse oder GUID. 

    Beispiel: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` 

    In diesem Beispiel wird auf zwei Benutzerkonten in Office 365 verwiesen: *meganb* für *Megan*und *alexw* für *Alex*. 
    
    > [!TIP]
    > Sie können dieses Cmdlet auch für einen einzelnen Benutzer verwenden:`Get-InformationBarrierRecipientStatus -Identity <value>`
    
2. Überprüfen Sie die Ergebnisse. Das Cmdlet **Get-InformationBarrierRecipientStatus** gibt Informationen zu Benutzern zurück, beispielsweise Attributwerte und alle Richtlinien für Informationsbarrieren, die angewendet werden. 

    Überprüfen Sie die Ergebnisse, und führen Sie dann die nächsten Schritte aus, wie in der folgenden Tabelle beschrieben:
    
    |Ergebnisse  |Nächste Schritte  |
    |---------|---------|
    |Für die ausgewählten Benutzer werden keine Segmente aufgeführt.     |Führen Sie einen der folgenden Schritte aus:<br/>– Zuweisen von Benutzern zu einem vorhandenen Segment durch Bearbeiten der Benutzerprofile in Azure Active Directory. (Weitere Informationen finden Sie unter [Konfigurieren von Benutzerkontoeigenschaften mit Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).)<br/>-Definieren eines Segments mithilfe eines [unterstützten Attributs für Informationsbarrieren](information-barriers-attributes.md). Definieren Sie dann entweder [eine neue Richtlinie](information-barriers-policies.md#part-2-define-information-barrier-policies) , oder [Bearbeiten Sie eine vorhandene Richtlinie](information-barriers-edit-segments-policies.md.md#edit-a-policy) , um dieses Segment einzubeziehen.  |
    |Segmente werden aufgelistet, aber diesen Segmenten werden keine Richtlinien für Informationsbarrieren zugewiesen.     |Führen Sie einen der folgenden Schritte aus:<br/>- [Definieren einer neuen Informations Sperrrichtlinie](information-barriers-policies.md#part-2-define-information-barrier-policies) für jedes betreffende Segment<br/>- [Bearbeiten einer vorhandenen Richtlinie für Informationsbarrieren](information-barriers-edit-segments-policies.md.md#edit-a-policy) , um Sie dem richtigen Segment zuzuweisen         |
    |Segmente werden aufgelistet, und jede Richtlinie enthält eine Informations Barriere.     |-Führen Sie `Get-InformationBarrierPolicy` das Cmdlet aus, um sicherzustellen, dass Richtlinien für Informationsbarrieren aktiv sind.<br/>-Führen Sie `Get-InformationBarrierPoliciesApplicationStatus` das Cmdlet aus, um zu bestätigen, dass die Richtlinien angewendet werden<br/>-Ausführen des `Start-InformationBarrierPoliciesApplication` Cmdlets zum Anwenden aller Active Information Barrier-Richtlinien          |
    

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a>Problem: Personen werden unerwartet für die Kommunikation in Microsoft Teams blockiert 

In diesem Fall melden Personen unerwartete Probleme, die mit anderen in Microsoft Teams kommunizieren. Beispiele:
- Ein Benutzer kann keinen anderen Benutzer in Microsoft Teams finden.
- Ein Benutzer kann keinen anderen Benutzer in Microsoft Teams auswählen.
- Ein Benutzer kann einen anderen Benutzer sehen, aber er kann keine Nachrichten an diesen anderen Benutzer in Microsoft Teams auswählen oder senden.
- Ein Benutzer kann einen anderen Benutzer anzeigen und auswählen, jedoch nicht mit diesem Benutzer in Microsoft Teams kommunizieren.

### <a name="what-to-do"></a>Nächste Schritte

Bestimmen Sie, ob die Benutzer von einer Informations Sperrrichtlinie betroffen sind.

1. Verwenden Sie das Cmdlet **Get-InformationBarrierRecipientStatus** mit dem Parameter Identity. 

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

    Überprüfen Sie die Details für das Segment. Bearbeiten Sie bei Bedarf [ein Segment](information-barriers-edit-segments-policies.md.md#edit-a-segment), und verwenden Sie dann das `Start-InformationBarrierPoliciesApplication` Cmdlet erneut.

    Wenn Sie weiterhin Probleme mit ihrer Richtlinie zu Informationsbarrieren haben, wenden Sie sich an den Support.
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a>Problem: der Anwendungsprozess für Informationsbarrieren dauert zu lange.

Nach dem Ausführen des Cmdlets **Start-InformationBarrierPoliciesApplication** dauert es sehr lange, bis der Vorgang abgeschlossen ist.

### <a name="what-to-do"></a>Nächste Schritte

Beachten Sie, dass beim Ausführen des Cmdlets für die Richtlinienanwendung für alle Konten in Ihrer Organisation Richtlinien für Informationsbarrieren angewendet (oder entfernt) werden, Benutzer nach Benutzer. Wenn Sie viele Benutzer haben, dauert es eine Weile, bis Sie verarbeitet werden. (Als allgemeine Richtlinie dauert es etwa eine Stunde, 5.000-Benutzerkonten zu verarbeiten.)

1. Verwenden Sie das Cmdlet **Get-InformationBarrierPoliciesApplicationStatus** , um den Status der neuesten Richtlinienanwendung zu überprüfen.

    Syntax`Get-InformationBarrierPoliciesApplicationStatus`

    (Zum Anzeigen des Status für *alle* Richtlinien Anwendungen für Informationsbarrieren verwenden Sie dieses Cmdlet:<br/>
    `Get-InformationBarrierPoliciesApplicationStatus -All $true`)

    Dadurch werden Informationen darüber angezeigt, ob die Richtlinienanwendung abgeschlossen, ein Fehler aufgetreten ist oder ausgeführt wird..

2. Führen Sie je nach den Ergebnissen des vorherigen Schritts einen der folgenden Schritte aus:
  
    |Status  |Nächster Schritt  |
    |---------|---------|
    |**Nicht gestartet**     |Wenn es mehr als 45 Minuten seit dem **Start-InformationBarrierPoliciesApplication-** Cmdlet ausgeführt wurde, überprüfen Sie Ihr Überwachungsprotokoll, um zu sehen, ob es Fehler in Richtlinien Definitionen gibt, oder aus einem anderen Grund, warum die Anwendung noch nicht gestartet wurde. |
    |**Fehlgeschlagen**     |Wenn die Anwendung fehlgeschlagen ist, überprüfen Sie Ihr Überwachungsprotokoll. Überprüfen Sie auch ihre Segmente und Richtlinien. Sind alle Benutzer mehr als einem Segment zugeordnet? Sind Segmente mit mehr als einem poliicy zugeordnet? Bearbeiten Sie gegebenenfalls [Segmente](information-barriers-edit-segments-policies.md.md#edit-a-segment) und/oder [Bearbeiten Sie Richtlinien](information-barriers-edit-segments-policies.md.md#edit-a-policy), und führen Sie dann das Cmdlet **Start-InformationBarrierPoliciesApplication** erneut aus.  |
    |**In Bearbeitung**     |Wenn die Anwendung noch ausgeführt wird, lassen Sie mehr Zeit für ihre Ausführung zu. Wenn es sich um mehrere Tage handelt, erfassen Sie die Überwachungsprotokolle, und wenden Sie sich an den Support. |

## <a name="related-topics"></a>Verwandte Themen

[Definieren von Richtlinien für Informationsbarrieren in Microsoft Teams (Vorschau)](information-barriers-policies.md)

[Informationsbarrieren (Vorschau)](information-barriers.md)



