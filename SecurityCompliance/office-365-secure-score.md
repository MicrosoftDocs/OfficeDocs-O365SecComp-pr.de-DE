---
title: Office 365 Secure Score
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/25/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Haben Sie sich je gefragt, wie sicher Ihre Organisation wirklich in Office 365 ist? Sichere Faktor ist hier helfen. Sichere Faktor Sicherheit Ihrer Organisation basierend auf Ihren regulären Aktivitäten und Sicherheitseinstellungen in Office 365 analysiert und weist eine Bewertung.
ms.openlocfilehash: bc0379e40b09e63e5fded1b1a289d40c306def91
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559088"
---
# <a name="office-365-secure-score"></a>Office 365 Secure Score

**Zusammenfassung** Haben Sie sich je gefragt, wie sicher Ihre Organisation wirklich in Office 365 ist? Sichere Faktor ist hier helfen. Sichere Faktor Sicherheit Ihrer Organisation basierend auf Ihren regulären Aktivitäten und Sicherheitseinstellungen in Office 365 analysiert und weist eine Bewertung. Lesen Sie diesen Artikel, um einen Überblick über Secure Score und wie Sie es verwenden können.
  
## <a name="how-to-get-to-secure-score"></a>Wie Sie Secure integritätsbewertung abrufen

Wenn Ihre Organisation verfügt ein Abonnement, die [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/)oder Office 365 Business Premium enthält und Sie über die [erforderlichen Berechtigungen](#required-permissions)verfügen, können Sie Ihrer Organisation sichere Score Vorsichtsmaßnahmen anzeigen. [https://securescore.office.com](https://securescore.office.com). 

Alternativ können Sie die Sicherheit & Compliance Center besuchen ([https://protection.office.com](https://protection.office.com)), in der Sie ein Secure Score-Widget finden, die Sie mit Ihr aktuelles Ergebnis bereitstellt.

![Sichere Score widget](media/SecureScoreWidget-o365.png)

Das Widget enthält einen Link zum Dashboard Score sichern.

![Sichere Score-dashboard](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a>Funktionsweise

Sichere Score bestimmt, welche Office 365-Dienste (beispielsweise OneDrive, SharePoint und Exchange) dann verwendeten verglichen Ihrer Einstellungen und die Aktivitäten aus, die einen Basisplan von Microsoft hergestellt wird. Sie erhalten einen Faktor basierend auf wie gut ausgerichtet mit bewährten Methoden für die Sicherheit Ihrer Organisation ist. Sie erhalten auch Empfehlungen zu den erforderlichen Schritten, die Sie ergreifen können, um Ihr Unternehmen zu verbessern. 
  
![Aktionen Warteschlange im Office 365 Secure Score-tool](media/SecureScore-ActionsToTake.png)
  
Sichere Score berechnet Ihr Ergebnis basierend auf den Diensten, die Sie erworben haben. Angenommen, wenn Sie nur einen Exchange Online-Plan erworben haben, werden nicht Sie für SharePoint Online-Sicherheitsfeatures bewertet werden. Die als Nenner für die Bewertung ist die Summe der alle Baselines für die Steuerelemente, die für die Produkte gelten, die Sie erworben haben. Der Zähler ist die Summe aller Steuerelemente, für die Sie abgeschlossen, oder teilweise abgeschlossen, die Aktionen für das jeweilige Steuerelement zu erfüllen.

Erweitern Sie eine Aktion, um zu erfahren, welche Schritte an, die Gefahren, die geschützt werden müssen Sie aus, und zeigt, wie viele Ihre Punktzahl erhöht wird, nachdem Sie die Empfehlung.
  
![Erweiterte Aktion im Office 365 Secure Score-tool](media/SecureScore-DetailedActionToTake.png)
  
Um die Auswirkungen von Ihren Aktionen auf Sicherheit Ihrer Organisation anzuzeigen, wählen Sie die Registerkarte **Score Analyzer** , und überprüfen Sie den Verlauf. 
  
![Faktor Analyzer Registerkarte des Office 365 Secure Score-Tools](media/SecureScore-ScoreAnalyzer-7days.png)
  
Unter dem Diagramm sehen Sie eine Liste der Faktoren und Aktionen nach Kategorie. 
  
![Diagramm auf der Score Analyzer Registerkarte zeigt einen Datenpunkt ausgewählt](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
Aktionen, die als **[Nicht bewertet]** sind gekennzeichnet sind, die Sie für Ihre Organisation ausführen können, aber, da sie nicht sichere Score verbunden sind, werden sie nicht bewertet.  

Klicken Sie auf der Seite **Score Analyzer** auf einen Datenpunkt für einen bestimmten Tag, und klicken Sie dann einen Bildlauf nach unten zu finden, die für diesen Tag zu erfahren, welche Aktionen abgeschlossenen und unvollständigen geändert. Die Bewertung wird einmal pro Tag (etwa 1:00 Uhr PST) berechnet. Wenn Sie eine Änderung an einer gemessene Aktion vornehmen, wird die Bewertung den nächsten Tag automatisch aktualisiert. Es dauert bis zu 48 Stunden für eine Änderung in Ihr Ergebnis übernommen werden.

Sichere Score ist nicht express eine absolute Maßeinheit des wie wahrscheinlich generiertes abgerufen werden sollen. Dieser drückt des Umfang an dem Features eingeführt haben, die das Risiko wird generiertes versetzt werden können. Kein Dienst kann sicherstellen, dass Sie nicht verletzt werden, und die Bewertung Secure nicht als keinerlei Garantie interpretiert werden soll.
 
## <a name="how-secure-score-helps"></a>Schutzmechanismen in Secure Score

Mit Secure Faktor können Sie verbessern Sicherheitsstatus Ihrer Organisation mithilfe der integrierten Sicherheitsfeatures in Office 365 (von denen Sie bereits erworben haben aber möglicherweise nicht bekannt). Weitere Informationen zu diesen Features kann ermöglichen Ihnen Gewissheit, dass Sie die richtigen Maßnahmen für Ihre Organisation vor Angriffen zu schützen einnehmen.
  
Aber nicht einfach Probieren Sie es. Kunden, die mithilfe von Secure Score haben ihre Score fünfmaliges mehr als Kunden zu erhöhen, die sie nutzen sind nicht sichtbar. (Die Anhebung der dem Faktor entspricht mit den Sicherheitsfunktionen in ihren Organisationen verwendet wird.)
  
> [!NOTE]
> Sichere Score ist nicht express eine absolute Maßeinheit des wie wahrscheinlich generiertes abgerufen werden sollen. Dieser drückt des Umfang an dem Steuerelemente eingeführt haben die generiertes wird das Risiko offset können. Kein Dienst kann sicherstellen, dass Sie nicht verletzt werden, und Secure Score nicht als keinerlei Garantie interpretiert werden soll. 
  
## <a name="required-permissions"></a>Erforderliche Berechtigungen

Zum Anzeigen und verwenden Sie das Dashboard Score Secure, müssen Sie eine der folgenden Rollen in Azure Active Directory zugewiesen werden:
- Globaler Administrator
- Abrechnungsadministrator
- Benutzeradministrator
- Kennwort-Administrator
- Sicherheitsadministrator
- Sicherheit-Reader
- Exchange-Administrator
- SharePoint-Administrator

 Benutzer, die Admin-Rolle zugewiesen sind nicht auf Secure Score zugreifen.

## <a name="related-topics"></a>Verwandte Themen

[Übersicht über die Sicherheit-dashboard](security-dashboard.md)

[Welches Abonnement habe ich?](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)