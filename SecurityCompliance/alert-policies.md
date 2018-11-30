---
title: Warnen Richtlinien in die Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 8927b8b9-c5bc-45a8-a9f9-96c732e58264
description: Erstellen von alert Richtlinien in die Office 365-Sicherheit &amp; Compliance Center, um potenzielle Bedrohungen, Datenverlust und Problem mit Berechtigungen zu überwachen. Sie können dann anzeigen und Verwalten von Benachrichtigungen, die generiert werden, wenn Benutzer Aktivitäten ausführen, die die Suchkriterien einer Warnung zu.
ms.openlocfilehash: 9aea5660f6a890afb06c5bd04db812d6aeacd17a
ms.sourcegitcommit: 95a3ce0bc5b0f3782fc4ef22a70f5ef1dc879ee3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2018
ms.locfileid: "26988434"
---
# <a name="alert-policies-in-the-office-365-security-amp-compliance-center"></a>Warnen Richtlinien in die Office 365-Sicherheit &amp; Compliance Center

Sie können die neue Richtlinie für die Benachrichtigung und Warnung Dashboard Tools verwenden, in die Office 365-Sicherheit &amp; Compliance Center alert Richtlinien zu erstellen und klicken Sie dann die Warnungen, die generiert werden, wenn Benutzer Aktivitäten ausführen, der die Suchkriterien einer Warnung zu, anzuzeigen. Warnung Richtlinien auf erstellen, und erweitern den Funktionsumfang der Aktivität Benachrichtigungen, mit deren Hilfe Sie die Warnung Richtlinie kategorisieren, wenden Sie die Richtlinie für alle Benutzer in Ihrer Organisation, legen Sie einen Schwellenwert für Wenn eine Warnung ausgelöst wird, und entscheiden, ob e-Mail empfangen Benachrichtigungen. In das Wertpapier ist auch eine Seite **Ansicht Warnungen** &amp; Compliance Center können Sie anzeigen und Filtern von Warnungen, Set eine Warnung Status, mit denen Sie Benachrichtigungen verwalten, und klicken Sie dann auf Schließen informiert, wenn Sie adressiert ist oder das zugrunde liegende Problem behoben haben. Wir haben auch die Art der Ereignisse erweitert, denen Sie Warnungen für erstellen können. Beispielsweise können Sie die Warnung Richtlinien zum Nachverfolgen von Malware-Aktivitäten und Daten erstellen. Schließlich haben wir eine Anzahl von alert Standardrichtlinien enthalten, mit denen Sie überwachen zuweisen Administratorrechte in Exchange Online, Malwareangriffen und ungewöhnliche Ebenen der Datei löschen und externe Freigabe. 
  
> [!NOTE]
> Warnung Richtlinien sind für Organisationen mit einer Office 365 Enterprise oder Office 365 US-Regierung E1/G1, E3/G3 oder E5/G5-Abonnement verfügbar. Einige erweiterte Funktionen ist jedoch nur verfügbar für Organisationen mit einem E5/G5-Abonnement oder für Organisationen, die eine E1/G1 oder E3/G3-Abonnement und ein Office 365-Bedrohungsanalyse oder Office 365 erweiterte Compliance Add-on-Abonnement haben. In diesem Thema wird die Funktionalität, die ein Abonnement E5/G5 oder Add-on erfordert hervorgehoben. Beachten Sie außerdem, dass die Warnung Richtlinien in Office 365 GCC, GCC hohe und DoD US-Regierung Umgebungen zur Verfügung stehen.
  
## <a name="how-alert-policies-work"></a>Wie alert Richtlinien Arbeit

Nachfolgend finden Sie einen schnellen Überblick über wie alert Richtlinien Arbeit und Benachrichtigungen, die Trigger beim Benutzer oder Administrator Aktivität die Bedingungen einer Warnung zu entsprechen.
  
![Übersicht über wie alert Richtlinien Arbeit](media/e02a622d-b429-448b-8107-dd1a4770b4e0.png)
  
1. Ein Administrator in Ihrer Organisation erstellt, konfiguriert und aktiviert eine Warnung Richtlinie mithilfe der Seite **Warnung Richtlinien** in das Wertpapier &amp; Compliance Center. Sie können auch alert Richtlinien erstellen, indem Sie mithilfe des Cmdlets **New-ProtectionAlert** in PowerShell. 
    
2. Ein Benutzer führt eine Aktivität, die die Suchkriterien einer Warnung Richtlinie entspricht. Infizierte e-Mail-Nachrichten an Benutzer in Ihrer Organisation gesendet werden eine Warnung ausgelöst wird im Fall von Malwareangriffe.
    
3. Generiert eine Warnung, die auf der Seite **Ansicht Warnungen** in das Wertpapier angezeigt wird, Office 365 &amp; Compliance Center. Wenn Sie e-Mail-Benachrichtigungen für die Warnung Richtlinie aktiviert sind, sendet Office 365 eine Benachrichtigung an einen Empfänger Liste. 
    
4. Ein Administrator verwaltet Warnungen in das Wertpapier &amp; Compliance Center. Verwalten von Warnungen besteht aus einen Warnungen Status zu überwachen und Verwalten von Untersuchung zuweisen.
    

  
## <a name="alert-policy-settings"></a>Warnung Richtlinieneinstellungen

Eine Warnung Richtlinie besteht aus einem Satz von Regeln und Bedingungen, die der Benutzer oder die Admin-Aktivität, die eine Benachrichtigung für eine Liste der Benutzer generieren, die die Warnung ausgelöst wird, wenn sie die Aktivität ausführen definieren und Schwellenwert, die definiert, wie oft die Aktivität vor auftreten, muss ein n Warnung ist ausgelöst. Sie auch kategorisieren die Richtlinie, und weisen Sie es mit einen Schweregrad. Diese zwei Einstellungen unterstützen Sie beim Verwalten alert-Richtlinien (und der Warnungen, die ausgelöst werden, wenn die Drahtloszugriff abgeglichen werden), da Sie auf diese Einstellungen filtern können, wenn in das Wertpapier Richtlinien verwalten und Anzeigen von Warnungen &amp; Compliance Center. Beispielsweise können Sie Warnungen, die die Suchkriterien aus der gleichen Kategorie, oder Anzeigen von Warnungen mit denselben Schweregrad anzeigen.
  
Wechseln Sie zum Anzeigen und alert Richtlinien erstellen, **Benachrichtigungen** \> **Alert Richtlinien** in das Wertpapier &amp; Compliance Center. 
  
![In das Wertpapier &amp; Complinace-Center auf Benachrichtigungen und dann auf Warnung warnen, Richtlinien zum Anzeigen und Erstellen von Richtlinien](media/09ebd451-8e84-44e1-aefc-63e70bba4d97.png)
  
Eine Warnung Richtlinie umfasst die folgenden Einstellungen und Bedingungen.
  
- **Nachverfolgen der Aktivität der Warnung** : Sie eine Richtlinie zum Nachverfolgen einer Aktivitätsfeeds oder in einigen Fällen ein paar zugehörige Aktivitäten, solche eine Freigabe einer Datei mit einem externen Benutzer durch Freigabe, Zugriffsberechtigungen zuweisen oder erstellen einen anonymen Link erstellen. Wenn ein Benutzer die Aktivität, die von der Richtlinie definierten ausführt, wird eine Warnung ausgelöst basierend auf den entsprechenden schwellenwerteinstellungen.
    
    > [!NOTE]
    > Aktivitäten, die Sie überwachen können, hängt von Ihrer Organisation-Office 365 Enterprise oder Office-365 US-Regierung Plan. Im allgemeinen Aktivitäten im Zusammenhang mit Malware Kampagnen und Phishingangriffen erfordern, ein E5/G5-Abonnement oder eine E1/G1 oder E3/G3-Abonnement mit einem Bedrohungsanalyse Add-on-Abonnement. 
  
- **Aktivität Conditions** - können für die meisten Aktivitäten Sie zusätzliche Bedingungen definieren, die für eine Warnung ausgelöst werden, erfüllt werden müssen. Allgemeine zählt IP-Adressen (so, dass eine Warnung ausgelöst wird, wenn der Benutzer die Aktivität auf einem Computer mit einer bestimmten IP-Adresse oder innerhalb eines IP-Adressbereichs ausführt), ob eine Warnung ausgegeben wird, wenn ein bestimmter Benutzer oder Benutzer diese Aktivität ausführen, und ob die Aktivität erfolgt auf einem bestimmten Dateinamen oder eine URL. Sie können auch eine Bedingung konfigurieren, die eine Warnung ausgelöst wird, wenn die Aktivität von jedem Benutzer in Ihrer Organisation ausgeführt wird. Beachten Sie, dass die verfügbaren Bedingungen für die ausgewählte Aktivität abhängig sind.
    
- **Wenn die Warnung ausgelöst wird** - eine Einstellung, die definiert, wie oft eine Aktivität auftreten kann, bevor eine Warnung ausgegeben wird, können konfiguriert werden. Dadurch können Sie eine Richtlinie einrichten, um eine Benachrichtigung erzeugt wird jedes Mal, wenn eine Aktivität einen bestimmten Schwellenwert überschritten wird, oder wenn das Vorkommen der Aktivität, den die Benachrichtigung nachverfolgten ungewöhnlich, dass unser Unternehmen wird die Drahtloszugriff übereinstimmt. 
    
    ![Konfigurieren von wie Warnungen ausgelöst werden, basierend auf die Aktivität tritt, einen Schwellenwert oder ungewöhnliche Aktivitäten für Ihre Organisation](media/97ee1ed2-e7a9-47a2-a980-5f9f63872c65.png)
  
    Wenn Sie die Einstellung basierend auf ungewöhnliche Aktivitäten auswählen, stellt Office 365 ein Baselinewert, der die normale Häufigkeit für die ausgewählte Aktivität definiert, her; bis zu sieben Tage zu dieser Baseline festgelegt werden, während die Warnungen generiert werden, wird nicht benötigt. Nachdem die Grundlinie hergestellt wurde, wird eine Warnung ausgelöst werden, wenn die Häufigkeit der Aktivität erheblich durch die Warnung Richtlinie nachverfolgt den Baselinewert überschreitet. Legen Sie für die Überwachung im Zusammenhang Aktivitäten (beispielsweise Dateien und Ordner Aktivitäten) Sie Grundwerte basierend auf einem einzelnen Benutzer oder für alle Benutzer in Ihrer Organisation; bei Aktivitäten im Zusammenhang mit Schadsoftware können Sie einen Basisplan basierend auf einer einzelnen Malware-Familie, einen einzelnen Empfänger oder alle Nachrichten in Ihrer Organisation herstellen.
    
    > [!NOTE]
    > Die Möglichkeit, konfigurieren Sie Richtlinien basierend auf einem Schwellenwert oder basierend auf ungewöhnliche Aktivitäten Warnung erfordert ein Abonnement E5/G5 oder eine E1/G1 oder E3/G3-Abonnement mit einer Bedrohungsanalyse oder erweiterte Compliance Add-on-Abonnement. Organisationen mit einem Abonnement E1/G1 und E3/G3 können nur eine Warnung Richtlinie erstellen, in dem eine Benachrichtigung jedes Mal ausgelöst wird, das eine Aktivität auftritt. 
  
- **Warnung Kategorie** -, das Ihnen bei nachverfolgen und Verwalten von Benachrichtigungen generiert durch eine Richtlinie können Sie eine der folgenden Kategorien auf eine Richtlinie zuweisen.
    
  - Datengovernance
    
  - Verhinderung von Datenverlust

  - Nachrichtenübermittlung
    
  - Berechtigungen
    
  - Bedrohungsverwaltung
    
  - Sonstige
    
    Tritt auf eine Aktivität, die die Bedingungen der alert-Richtlinie entspricht, wird die Benachrichtigung, die generiert wird mit der Kategorie, die in dieser Einstellung festgelegten markiert. Hiermit können Sie nachverfolgen und Verwalten von Warnungen, die die Kategorie der Einstellung auf der Seite **Ansicht Warnungen** in das Wertpapier haben &amp; Compliance Center, da Sie können sortieren und Filter Benachrichtigungen basierend auf Kategorie. 
    
- **Schweregrad einer Warnung** - ähnelt der Warnung Kategorie weisen Sie ein Severity-Attribut ( **Niedrig**, **Mittel**oder **Hoch**) alert Richtlinien. Wie der Kategorie "Warnung" tritt eine Aktivität, die die Warnung Richtlinie ein, die Bedingungen erfüllt ist die Benachrichtigung, die generiert wird mit denselben Schweregrad markiert, die für die Warnung Richtlinie festgelegt ist. In diesem Fall können Sie zum Nachverfolgen und Verwalten von Warnungen, die dieselbe Schweregrad Einstellung auf der Seite **Warnungen anzeigen** verfügen. Beispielsweise können Sie die Liste der Warnungen filtern, sodass nur Benachrichtigungen mit einem **hohen** Schweregrad angezeigt werden. 
    
    > [!TIP]
    > Berücksichtigen Sie beim Einrichten einer Warnungen Richtlinie Aktivitäten, die stark negative Folgen, wie die Erkennung von Schadsoftware nach der Übermittlung an Benutzer führen können eine höhere Priorität zuweisen, sensible oder vertrauliche Daten anzeigen, Freigeben von Daten mit externen Benutzern, oder andere Aktivitäten, die Daten Verlust oder Security Threats führen können. Dies kann Ihnen Priorisieren von Warnungen und Aktionen, die Sie untersuchen und Beheben der zugrunde liegenden Ursachen durchführen. 
  
- **E-Mail-Benachrichtigungen** – Sie können einrichten die Richtlinie so, dass e-Mail-Benachrichtigungen gesendet (oder werden nicht gesendet) zu einer Liste von Benutzern, wenn eine Warnung ausgegeben wird. Sie können auch einen tägliche Benachrichtigung Grenzwert festlegen, sobald die maximale Anzahl der Benachrichtigungen erreicht ist, keine weitere Benachrichtigung für die Warnung während dieses Tages gesendet werden. In zusätzliche können, um e-Mail-Benachrichtigungen, Sie oder andere Administratoren Benachrichtigungen anzeigen, die durch eine Richtlinie auf der Seite **Ansicht Warnungen** ausgelöst werden. E-Mail-Benachrichtigungen für alert Richtlinien einer bestimmten Kategorie in Betracht, oder eine höhere Schweregrad Einstellung über verfügen. 
  
## <a name="default-alert-policies"></a>Warnung Standardrichtlinien

Office 365 bietet integrierte alert Richtlinien, mit denen Exchange Admin Berechtigungen Missbrauch, Malware-Aktivitäten und Daten Governance Risiken zu identifizieren. Auf der Seite **Warnung Richtlinien** der Namen dieser integrierten Richtlinien sind fett dargestellt und der Richtlinientyp als **System**definiert ist. Diese Richtlinien sind standardmäßig aktiviert. Sie können diese Richtlinien deaktivieren (oder danach wieder an), eine Liste von Empfängern zum Senden von e-Mail-Benachrichtigungen einrichten und Festlegen eines Zeitlimits für tägliche Benachrichtigung. Die anderen Einstellungen für diese Richtlinien können nicht bearbeitet werden.
  
In der folgenden Tabelle enthält und beschreibt die verfügbaren alert Standardrichtlinien und gibt an, die Office 365 Enterprise und Office-365 US-Regierung Pläne für jeden erforderlich. Beachten Sie, dass einige alert Standardrichtlinien verfügbar sind, wenn Ihre Organisation das entsprechende Add-on-Abonnement neben ein Abonnement/G1 E1 oder E3/G3 verfügt. 
  
|**Warnung Standardrichtlinie**|**Beschreibung**|**Office 365 Enterprise-Abonnement**|
|:-----|:-----|:-----|
|**Erstellung der Regel Weiterleitung-Umleitung** <br/> |Generiert eine Warnung, wenn eine Person in Ihrer Organisation eine Posteingangsregel für ihr Postfach wird erstellt, die weiterleitet oder leitet Nachrichten an ein anderes e-Mail-Konto. Diese Richtlinie verfolgt nur Posteingangsregeln, die mit Outlook Web App oder Exchange Online PowerShell erstellt werden. Diese Richtlinie hat eine Einstellung für **niedriger** Schweregrad. Weitere Informationen zum Posteingangsregeln zum Weiterleiten und Umleiten von e-Mail in Outlook Web App verwenden finden Sie unter [Verwenden von Regeln in Outlook Web App zum automatischen Weiterleiten von Nachrichten an ein anderes Konto](https://support.office.com/article/1433e3a0-7fb0-4999-b536-50e05cb67fed).<br/> |/ G1 E1, E3/G3 oder E5/G5  <br/> |
|**eDiscovery-Suche gestartet oder zu exportierenden** <br/> |Generiert eine Warnung, wenn ein Benutzer das Tool für die Inhaltssuche im Compliance Center & Sicherheit verwendet. Eine Warnung wird ausgelöst, wenn die folgenden Inhaltssuche Aktivitäten ausgeführt werden:<br/><br/>• Eine Inhaltssuche wird gestartet.<br/>•, Die die Ergebnisse einer Inhaltssuche exportiert werden<br/>• Ein Inhaltssuche-Bericht wird exportiert.<br/><br/>Benachrichtigungen werden auch trigged, wenn die vorherige Inhaltssuche Aktivitäten im Zusammenhang mit einem eDiscovery-Fall ausgeführt werden. Diese Richtlinie hat eine Einstellung für **mittlerer** Schweregrad. Weitere Informationen zu Aktivitäten Inhaltssuche finden Sie unter [Suchen für eDiscovery-Aktivitäten in der Office 365 in das Überwachungsprotokoll](search-for-ediscovery-activities-in-the-audit-log.md#ediscovery-activities).<br/> |/ G1 E1, E3/G3 oder E5/G5  <br/> |
|**Erhöhung von Exchange Admin-Berechtigungen** <br/> |Generiert eine Warnung, wenn jemand Administratorberechtigungen in Ihrer Exchange Online-Organisation zugewiesen wird; beispielsweise wenn ein Benutzer der Organisation Verwaltungsrolle hinzugefügt wird adminisratorrollengruppe in Exchange Online. Diese Richtlinie hat eine Einstellung für **niedriger** Schweregrad.<br/> |/ G1 E1, E3/G3 oder E5/G5  <br/> |
|**Verzögert Nachrichten** <br/> |Generiert eine Warnung, wenn Office 365 e-Mail-Nachrichten an Ihre lokale Organisation oder einem Partner Servern übermittelt werden kann nicht mit einem Connector. Wenn dies der Fall sein, wird die Nachricht in Office 365 in der Warteschlange. Diese Warnung wird ausgelöst, wenn 2.000 Nachrichten oder mehr, die für mehr als eine Stunde zurückgestellt wurden vorhanden sind. Diese Richtlinie hat eine Einstellung für die **hohe** Schweregrad.<br/> |/ G1 E1, E3/G3 oder E5/G5  <br/> |
|**Nach der Übermittlung erkannt Malware Kampagne** <br/> |Generiert eine Warnung, wenn eine ungewöhnlich große Anzahl von Nachrichten mit Schadsoftware an Postfächer in Ihrer Organisation übermittelt werden. Wenn dieses Ereignis eintritt, entfernt Office 365 die infizierten Nachrichten aus Exchange Online-Postfächer. Diese Richtlinie hat eine Einstellung für die **hohe** Schweregrad.<br/> |Add-on-Abonnement E5/G5 oder Office 365 Bedrohungsanalyse  <br/> |
|**Malware Kampagne erkannt und blockiert** <br/> |Generiert eine Warnung, wenn jemand versucht hat, um eine ungewöhnlich große Anzahl von e-Mail-Nachrichten mit einem bestimmten Typ von Schadsoftware für Benutzer in Ihrer Organisation zu senden. Wenn dieses Ereignis auftritt, sind die infizierten Nachrichten von Office 365 blockiert und nicht auf Postfächer übermittelt. Diese Richtlinie hat eine Einstellung für **niedriger** Schweregrad.<br/> |Add-on-Abonnement E5/G5 oder Office 365 Bedrohungsanalyse  <br/> |
|**Malware Kampagne in SharePoint und OneDrive erkannt** <br/> |Generiert eine Warnung, wenn eine ungewöhnlich große Menge von Schadsoftware oder Viren in Dateien im SharePoint-Websites oder OneDrive-Konten in Ihrer Organisation erkannt werden. Diese Richtlinie hat eine Einstellung für die **hohe** Schweregrad.<br/> |Add-on-Abonnement E5/G5 oder Office 365 Bedrohungsanalyse  <br/> |
|**Ungewöhnliche externe Datei Benutzeraktivität** <br/> |Generiert eine Warnung, wenn eine in der Regel große Anzahl von Aktivitäten auf Dateien in SharePoint oder OneDrive von Benutzern außerhalb Ihrer Organisation ausgeführt werden. Dazu gehören Aktivitäten wie der Zugriff auf Dateien, Herunterladen von Dateien und Löschen von Dateien. Diese Richtlinie hat eine Einstellung für die **hohe** Schweregrad.<br/> |E5/G5 oder Office 365 Bedrohungsanalyse oder erweiterte Compliance Add-on-Abonnement  <br/> |
|**Ungewöhnliche Volumen der externen Dateifreigabe** <br/> |Generiert eine Warnung, wenn eine in der Regel große Anzahl von Dateien in SharePoint oder OneDrive mit Benutzern außerhalb Ihres Unternehmens gemeinsam genutzt werden. Diese Richtlinie hat eine Einstellung für **mittlerer** Schweregrad.<br/> |E5/G5 oder Office 365 Bedrohungsanalyse oder erweiterte Compliance Add-on-Abonnement  <br/> |
|**Ungewöhnliche Volumen der Datei löschen** <br/> |Generiert eine Warnung, wenn eine ungewöhnlich große Anzahl von Dateien in SharePoint oder OneDrive in einem kurzen Zeitraum gelöscht werden. Diese Richtlinie hat eine Einstellung für **mittlerer** Schweregrad.<br/> |E5/G5 oder Office 365 Bedrohungsanalyse oder erweiterte Compliance Add-on-Abonnement  <br/> |
|**Ungewöhnlicher Anstieg der e-Mail als Phishing gemeldet** <br/> |Generiert eine Warnung, wenn eine erhebliche Steigerung der Anzahl von Personen in Ihrer Organisation verwenden des Berichtnachricht-add-Ins in Outlook auf Berichtnachrichten als Phishing Mail vorhanden ist. Diese Richtlinie hat eine Einstellung für die **hohe** Schweregrad. Weitere Informationen zu diesem Add-in finden Sie unter [Verwenden des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).<br/> |Add-on-Abonnement E5/G5 oder Office 365 Bedrohungsanalyse  <br/> |
   
Beachten Sie, dass der von einigen der integrierten Richtlinien überwacht ungewöhnliche Aktivitäten auf demselben Prozess basiert, wie Warnschwellenwert festlegen, die weiter oben beschrieben wurde. Office 365 richtet einen geplante-Wert, der die normale Häufigkeit für die Aktivität "normalen" definiert. Benachrichtigungen werden dann ausgelöst, wenn die Häufigkeit der Aktivitäten, die durch die integrierten alert Richtlinie erheblich nachverfolgt der Baselinewert überschreitet.
 
## <a name="viewing-alerts"></a>Anzeigen von Warnungen

Wenn eine Aktivität von Benutzern in Ihrer Organisation entsprechen die Einstellungen einer Warnung Richtlinie, wird eine Warnung generiert und auf der Seite **Ansicht Warnungen** in das Wertpapier angezeigt &amp; Compliance Center. Abhängig von den Einstellungen einer Warnung Richtlinie wird eine e-Mail-Benachrichtigung auch eine Liste der angegebenen Benutzer gesendet, wenn eine Warnung ausgegeben wird. Für jede Warnung zeigt das Dashboard auf der Seite **Ansicht Warnungen** den Namen des die entsprechende Richtlinie Warnung, Schweregrad und Kategorie für die Benachrichtigung (definiert in der Warnung Richtlinie) und die Anzahl der, wie oft, die eine Aktivität aufgetreten ist, die die Benachrichtigung wird geführt hat generiert. Dieser Wert basiert auf den Schwellenwert für die Einstellung der alert-Richtlinie. Das Dashboard zeigt auch den Status für jede Warnung. Finden Sie weitere Informationen zur Verwendung der Status-Eigenschaft zum Verwalten von Warnungen im Abschnitt [Verwalten von Benachrichtigungen](#managing-alerts) . 
  
Wechseln Sie zum Anzeigen von Warnungen **Benachrichtigungen** \> **Ansicht Warnungen** in das Wertpapier &amp; Compliance Center. 
  
![In das Wertpapier &amp; Complinace Center, klicken Sie auf Benachrichtigungen und dann auf Ansicht Benachrichtigungen, um Warnungen anzuzeigen](media/ec5ea59b-bf61-459f-8b65-970ab4bb8bcc.png)
  
Die folgenden Filter können Sie eine Teilmenge der alle Benachrichtigungen auf der Seite **Ansicht Warnungen** anzeigen. 
  
- **Status** – dies angezeigt, die einen bestimmten Status zugewiesen sind Filtern verwenden; die Standardstatus ist **aktiv**. Sie oder andere Administratoren können den Statuswert ändern.
    
- **Gruppenrichtlinien** - Benachrichtigungen angezeigt, die die Einstellung der eine oder mehrere alert Richtlinien entsprechen diesen Filter verwenden. Oder Sie können nur alle Warnungen für alle Richtlinien für die Warnung anzeigen.
    
- **Zeitbereich** - diesen Filter verwenden, um Warnungen anzuzeigen, die innerhalb eines bestimmten Datums und der Zeitbereich generiert wurden.
    
- **Schweregrad** - diesen Filter verwenden, um Warnungen anzuzeigen, die einen bestimmten Schweregrad zugewiesen sind.
    
- **Kategorie** - Verwendung dieser Filter aus eine oder mehrere Kategorien angezeigt.

- **Source** - Verwendung dieser Filter zum Anzeigen von Warnungen alert Richtlinien in der Sicherheit & Compliance Center oder Warnungen ausgelöst, indem Office 365 Cloud App-Sicherheitsrichtlinien oder beides ausgelöst. Weitere Informationen zu Office 365-Cloud-App-Sicherheit Warnungen finden Sie im Abschnitt [Anzeigen Cloud App Sicherheitshinweise](#viewing-cloud-app-security-alerts) .

  
## <a name="managing-alerts"></a>Verwalten von Warnungen

Nachdem die Warnungen generiert und auf der Seite **Ansicht Warnungen** in das Wertpapier angezeigt wurden &amp; Compliance Center, Sie können untersuchen, untersuchen und beheben Sie diese. Hier sind einige Aufgaben, die Sie ausführen können, um Benachrichtigungen zu verwalten. 
  
- **Weisen Sie einen Status, um Benachrichtigungen** - können Sie einen der folgenden Status Benachrichtigungen zuweisen: **aktiven** (Standardwert), **Investigating**, **gelöst**oder **Dismissed**. Anschließend können Sie auf diese Einstellung, um Warnungen angezeigt werden, mit der statuseinstellung der gleiche filtern. Diese statuseinstellung kann den Prozess der Verwaltung von Benachrichtigungen verfolgen.
    
- **Anzeigen von Warnungsdetails** - Sie können eine Warnung anzeigen eine Seite flyoutmenü mit ausführlichen Informationen über die Benachrichtigung klicken. Ausführliche Informationen, die entsprechende Benachrichtigung Richtlinie hängt, aber es in der Regel enthält die folgenden: Domänennamen für den tatsächlichen Vorgang, der die Warnung (beispielsweise ein Cmdlet), eine Beschreibung der Aktivität, die die Benachrichtigung, den Benutzer (oder die Liste der Benutzer) ausgelöst die durch die Warnung ausgelöst wurde, und den Namen (und den Link zur) der entsprechenden Richtlinie warnen.
    
  - Der Name der tatsächlichen Operation, die Warnung an, wie ein Cmdlet oder eine Audit Log-Operation ausgelöst.
    
  - Eine Beschreibung der Aktivität, die die Warnung ausgelöst wurde.
    
  - Der Benutzer, der die Warnung ausgelöst; Dies ist nur für die Warnung Richtlinien, die zum Nachverfolgen von einem einzelnen Benutzer oder eine einzelne Aktivität eingerichtet sind.
    
  - Wie oft die Aktivität durch die Warnung nachverfolgt wurde ausgeführt. Beachten Sie, dass diese Nummer möglicherweise nicht übereinstimmt, tatsächliche Anzahl von verwandten Benachrichtigungen auf der Seite Ansicht Benachrichtigungen aufgelistet werden, da möglicherweise zusätzliche Warnungen ausgelöst wurde.
    
  - Eine Verknüpfung zu einer Aktivitätenliste, die für jede Aktivität, die ausgeführt wird, wurde ein Element enthält, die die Warnung ausgelöst. Jeder Eintrag in dieser Liste gibt an, wann der Aktivität, des Namens des tatsächlichen-Vorgang (beispielsweise "FileDeleted") und der Benutzer, der ausgeführt werden, die Aktivität, die das Objekt (wie eine Datei, einem eDiscovery-Fall oder ein Postfach), dem für die Aktivität ausgeführt wurde und die IP-Adresse die Adresse des Computers des Benutzers. Für Schadsoftware weiterführende Benachrichtigungen, diese enthält Links zu einer e-Mail-Liste.
    
  - Der Name (und Link zur) der entsprechenden alert Richtlinie.
    
- **Unterdrücken e-Mail-Benachrichtigungen** - können Sie deaktivieren (oder unterdrücken) e-Mail-Benachrichtigungen auf der Seite flyoutmenü für eine Benachrichtigung. Wenn Sie e-Mail-Benachrichtigungen unterdrücken, Office 365 wird nicht Benachrichtigung senden, wenn Aktivitäten oder Ereignisse, die die Bedingungen entsprechen die Warnung Richtlinie. Jedoch weiterhin Benachrichtigungen Trigger sein, wenn die Aktivitäten von Benutzern der alert-Richtlinie entsprechen. Sie können e-Mail-Benachrichtigungen deaktivieren, durch die Warnung Richtlinie bearbeiten.
    
- **Beheben von Benachrichtigungen** - Sie können eine Warnung markieren, wie in der Dropdown-Seite für eine Warnung aufgelöst (die den Status der Warnung in **gelöst**festgelegt). Sofern Sie den Filter ändern, werden nicht aufgelöste Benachrichtigungen auf der Seite **Ansicht Warnungen** angezeigt. 
    
## <a name="viewing-cloud-app-security-alerts"></a>Anzeigen von Warnungen Cloud App-Sicherheit
  
Warnungen, die von Office 365 Cloud App-Sicherheitsrichtlinien ausgelöst werden, werden jetzt im Compliance Center & Sicherheit auf der Seite **Ansicht Warnungen** angezeigt. Dazu gehören, die Aktivität Richtlinien ausgelöst werden Benachrichtigungen und Warnungen, die von Anomalie Erkennungsrichtlinien in Office 365-Cloud-App-Sicherheit ausgelöst werden. Dies bedeutet, dass Sie alle Warnungen im Compliance Center & Sicherheit anzeigen können. Beachten Sie, dass Office 365-Cloud-App-Sicherheit nur für Organisationen mit einem Office 365 Enterprise E5 oder Office 365 US-Regierung G5-Abonnement verfügbar ist. Weitere Informationen finden Sie unter [Overview of Office 365 Cloud App-Security](office-365-cas-overview.md).

Darüber hinaus beziehen sich Organisationen, in denen Microsoft Cloud App-Sicherheit als Teil eines Enterprise-Mobilität + Sicherheit E5 Abonnement oder als eigenständigen Dienst kann auch Ansicht Cloud App-Sicherheit Warnungen, die auf Office 365-apps und Diensten in das Wertpapier & Compliance Center.

Wenn nur Cloud App Sicherheitshinweise im Compliance Center & Sicherheit anzeigen möchten, verwenden Sie den Filter für die **Datenquelle** , und wählen Sie **Cloud App-Sicherheit**.

![Verwenden des Quelle Filters, um nur Cloud App-Sicherheit Warnungen angezeigt werden](media/FilterCASAlerts.png)

Ähnlich wie eine Warnung ausgelöst, indem eine Benachrichtigung Sicherheit und Compliance Center-Richtlinie, können Sie eine Cloud App-Sicherheitshinweis um ein Dropdown-Seite mit Details über die Warnung anzuzeigen klicken. Die Benachrichtigung enthält einen Link, um die Details anzeigen und Verwalten der Benachrichtigung in der Cloud App-Sicherheit Portal- und einen Link zu der entsprechenden Cloud App Codezugriffssicherheits-Richtlinie, die die Warnung ausgelöst. Finden Sie unter [Überprüfen und entsprechende Maßnahmen Warnungen in Office 365-Cloud-App-Sicherheit](review-office-365-cas-alerts.md).

![Warnungsdetails enthalten Links zu den Portal Cloud App-Sicherheit](media/CASAlertDetail.png)

> [!IMPORTANT]
> Ändern des Status einer Warnung Cloud App-Sicherheit im Compliance Center & Sicherheit wird nicht den Status Lösung für dieselbe Warnung im Portal Cloud App-Sicherheit zu aktualisieren. Wenn Sie den Status der Warnung im Compliance Center & Sicherheit als **gelöst** markieren, wird der Status der Warnung in der Cloud App-Sicherheit Portal unverändert. Beheben oder schließen eine Cloud App-Sicherheitshinweis, die Benachrichtigung in der Cloud App-Sicherheit-Portal verwalten.