---
title: Methode zur KonformitätsBewertung
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft Compliance Manager ist ein kostenloses Workflow basiertes Risiko Bewertungstool im Microsoft Service Trust-Portal. Mit Compliance-Manager können Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachverfolgen, zuweisen und überprüfen.
ms.openlocfilehash: 120aede52d67375f60145412f5d210509ac57581
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473091"
---
# <a name="compliance-score-methodology-preview"></a>Methode zur KonformitätsBewertung (Vorschau)

> [!NOTE]
> Die Compliance-Bewertung drückt kein absolutes Maß für die Einhaltung eines bestimmten Standards oder einer bestimmten Vorschrift in der Organisation aus. Sie drückt vielmehr den Umfang aus, in dem Sie Steuerelemente einsetzen, durch die die Risiken für persönliche Daten und den Datenschutz reduziert werden können. Kein Dienst kann garantieren, dass Sie einen Standard oder eine Vorschrift einhalten. Die Compliance-Bewertung sollte in keinster Weise als eine Garantie verstanden werden.

Das Compliance-Manager-Dashboard zeigt eine Gesamt Konformitätsbewertung für Bewertungen in jeder Bewertungs Kachel an. Dies ist die Gesamtwertung für die Bewertung und die Akkumulation von Punkten, die für die einzelnen implementierten und getesteten Steuerelemente in der Bewertung erhalten wurden. Für eine neue Bewertung hat der Kompatibilitäts Faktor einen anfänglichen Wert für die enthaltenen von Microsoft verwalteten Steuerelemente, die von unabhängigen Drittanbietern getestet wurden. Compliance-Bewertung kann bei der Priorisierung der Bewertungen und Steuerelemente helfen, um Ihre allgemeine Compliance-Position zu verbessern.

Die angezeigten Werte für die KonformitätsBewertung für das Steuerelement werden *in vollem* Umfang auf den Gesamtwert der Konformitätsbewertung bei einem Durchlauf/fehlschlagen angewendet. Entweder wird das Steuerelement implementiert und übergibt den nachfolgenden Bewertungstest oder nicht. Es gibt keine Teilgutschrift für eine Teilimplementierung. Zugewiesene Punkte werden dem Kompatibilitäts Faktor hinzugefügt, wenn das Steuerelement Folgendes hat:

- **Implementierungs Status** Equals **implementiert** oder **alternative Implementierung** und,
- **Test Ergebnis** Equals **übergeben**.

## <a name="compliance-score"></a>Konformitätsbewertung
  
Im Compliance-Manager werden die Baseline-Bewertungen von der Steuerungsebene zur Aktionselement Ebene verschoben. Scores basieren auf dem Zweck (Kriminal-, präventiv-oder Korrektiv) und der Erzwingung des Aktionselements.

Aktionselemente werden Steuerelementen zugeordnet, und wenn ein Steuerelement mehreren Aktionselementen zugeordnet wird, ist die Summe der Ergebnisse des Aktionselements das Ergebnis des Steuerelements. Die Summe der Steuerelement Bewertung für alle Steuerelemente in einer bestimmten Bewertung ist die Bewertungs Bewertung. Die durchschnittliche Bewertung aller Bewertungen in einer Gruppe ist die Konformitätsbewertung für diese Gruppe.
  
### <a name="mandatory-or-discretionary-controls"></a>Obligatorische oder diskretionäre Steuerelemente
  
 **Obligatorische Steuerelemente** sind Steuerelemente, die weder absichtlich noch versehentlich umgangen werden können. Ein Beispiel für ein gängiges obligatorisches Steuerelement ist eine zentral verwaltete Kennwortrichtlinie, die Anforderungen für Kennwortlänge,-Komplexität und-Ablauf festlegt. Benutzer müssen diese Anforderungen erfüllen, um auf das System zuzugreifen.
  
 **Diskretionäre Steuerelemente** basieren auf Benutzern, um Richtlinien zu verstehen und entsprechend zu handeln. Beispielsweise ist eine Richtlinie, die Benutzer dazu verpflichtet, Ihren Computer zu sperren, wenn Sie Sie verlassen, ein diskretionäres Steuerelement, da Sie vom Benutzer abhängig ist.
  
### <a name="preventative-detective-or-corrective-controls"></a>Vorbeugende, präventive oder korrigierende Steuerelemente
  
 **Vorbeugende Steuerelemente** sind Steuerelemente, die bestimmte Risiken verhindern. Beispielsweise ist der Schutz von Informationen in Rest mithilfe der Verschlüsselung eine vorbeugende Kontrolle gegen Angriffe, Verstöße. Die Trennung von Zöllen ist eine vorbeugende Kontrolle, um Interessenkonflikte zu bewältigen und Betrugsfälle zu schützen.
  
 Bei den Kontroll **Mechanismen** handelt es sich um Steuerelemente, die Systeme aktiv überwachen, um unregelmäßige Bedingungen oder Verhaltensweisen zu identifizieren, die Risiken darstellen oder die dazu verwendet werden können, Intrusionen zu erkennen oder festzustellen, ob eine Verletzung aufgetreten ist Überwachung der System Zugriffsüberwachung und privilegierter Verwaltungsaktionen sind Arten von Überwachungs Kontrollen. Audits zur Einhaltung von Vorschriften sind eine Art von Kontrollverfahren, mit denen Prozessprobleme ermittelt werden.
  
**Korrekturhilfen** sind Steuerelemente, die versuchen, die nachteiligen Auswirkungen eines Sicherheitsvorfalls auf ein Minimum zu begrenzen, Korrekturmaßnahmen zu ergreifen, um die sofortige Wirkung zu verringern und den Schaden nach Möglichkeit umzukehren. Die Reaktion auf die Datenschutz Vorfälle ist eine Korrekturmaßnahme zur Begrenzung der Beschädigung und Wiederherstellung von Systemen nach einer Verletzung.
  
Jedem Steuerelement ist im Compliance-Manager ein Wert zugewiesen, der auf dem risikobasiert, das er darstellt:

|**Type**|**Zugewiesene Bewertung**|
|:-----|:-----|
| Vorbeugend erforderlich | 27 |
| Vorbeugende diskretionäre | 9 |
| Detektei obligatorisch | 3 |
| ErMessensfreiheit | 1 |
| Korrektiv erforderlich | 3 |
| Korrigierbarer erMessensSpielraum | 1 |
  
## <a name="action-item-workflow"></a>Aktionselement-Workflow

Hier ist der grundlegende Workflow für ein typisches Aktionselement:
  
1. Der Compliance-, Risk-, Privacy-und/oder Data Protection Officer einer Organisation weist jemand in der Organisation eine Aufgabe zu, um ein Steuerelement zu implementieren. Diese Person könnte folgende sein:

    - Ein Geschäftsrichtlinien Besitzer.
    - Eine IT-Implementierung.
    - Eine andere Person in der Organisation, die für die Durchführung der Aufgabe zuständig ist.

2. Diese Person führt die für die Implementierung des Steuerelements erforderlichen Aufgaben aus, lädt den Nachweis der Implementierung in Compliance-Manager hoch und markiert das an das Aktionselement gebundene Steuerelement wie implementiert. Sobald diese Aufgaben abgeschlossen sind, weisen Sie das Aktionselement einem Gutachter zur Validierung zu.

    Assessoren können folgende sein:

    - Interne Prüfer, die die Validierung von Steuerelementen in einer Organisation durchführen.
    - Externe Prüfer, die die Compliance überprüfen, verifizieren und zertifizieren, wie die unabhängigen Drittanbieter Organisationen, die die Microsoft Cloud-Dienste überwachen.

3. Der Prüfer validiert das Steuerelement und untersucht den Beweis und kennzeichnet das Steuerelement als beurteilt und die Ergebnisse der Bewertung.

Sobald alle Steuerelemente, die einer Bewertung zugeordnet sind, ausgewertet werden, ist die Bewertung abgeschlossen.