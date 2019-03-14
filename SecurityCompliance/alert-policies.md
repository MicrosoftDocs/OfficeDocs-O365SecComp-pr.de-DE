---
title: Warnungsrichtlinien im Office 365 Security &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: 8927b8b9-c5bc-45a8-a9f9-96c732e58264
description: Erstellen Sie im Office 365 Security &amp; Compliance Center Warnungsrichtlinien, um potenzielle Bedrohungen, Datenverluste und Berechtigungen zu überwachen. Dann können Sie die Warnungen anzeigen und verwalten, die generiert werden, wenn Benutzeraktivitäten ausführen, die den Bedingungen einer Warnungs Richtlinie entsprechen.
ms.openlocfilehash: 639cd893b39505b002cbe8a72cde6f3c9f9643fa
ms.sourcegitcommit: 8b36bf7949f1769f1418d740293637d60e403f87
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30339453"
---
# <a name="alert-policies-in-the-office-365-security-amp-compliance-center"></a>Warnungsrichtlinien im Office 365 Security &amp; Compliance Center

Sie können die neuen Warnungsrichtlinien-und Warnungs-Dashboard-Tools im Office 365 &amp; Security Compliance Center verwenden, um Warnungsrichtlinien zu erstellen und dann die Warnungen anzuzeigen, die generiert werden, wenn Benutzeraktivitäten ausführen, die den Bedingungen einer Warnungs Richtlinie entsprechen. Warnungsrichtlinien bauen auf und erweitern die Funktionalität von Aktivitäts Warnungen, indem Sie die Warnungs Richtlinie kategorisieren, die Richtlinie auf alle Benutzer in Ihrer Organisation anwenden, einen Schwellenwert für den Zeitpunkt festlegen, zu dem eine Warnung ausgelöst wird, und entscheiden, ob Sie e-Mails empfangen möchten. Benachrichtigungen. Es gibt auch eine Seite **Benachrichtigungen anzeigen** im Security &amp; Compliance Center, in der Sie Warnungen anzeigen und Filtern können, einen Warnungsstatus für die Verwaltung von Warnungen festlegen und dann Warnungen schließen, nachdem Sie den zugrunde liegenden Vorfall adressiert oder gelöst haben. Außerdem haben wir den Typ von Ereignissen erweitert, für die Sie Warnungen erstellen können. Sie können beispielsweise Warnungsrichtlinien erstellen, um Malwareaktivitäten und Datenverlust Vorfälle nachzuverfolgen. Schließlich haben wir auch eine Reihe von standardmäßigen Warnungsrichtlinien hinzugefügt, die Ihnen dabei helfen, die Zuweisung von Administratorrechten in Exchange Online, Malwareangriffen und ungewöhnlichen Ebenen von Dateilöschungen und externer Freigabe zu überwachen. 
  
> [!NOTE]
> Warnungsrichtlinien sind für Organisationen mit einem Office 365 Enterprise-oder Office 365 US Government E1/G1, E3/G3 oder E5/G5-Abonnement verfügbar. Einige erweiterte Funktionen sind jedoch nur für Organisationen mit einem E5/G5-Abonnement oder für Organisationen mit einem E1/G1-oder E3/G3-Abonnement und einem Office 365 Threat Intelligence-oder Office 365 Advanced Compliance-Add-on-Abonnement verfügbar. Die Funktionalität, die ein E5/G5-oder Add-on-Abonnement erfordert, wird in diesem Thema hervorgehoben. Beachten Sie, dass Warnungsrichtlinien in Office 365 GCC, GCC High und DoD US Government Environments verfügbar sind.
  
## <a name="how-alert-policies-work"></a>FunktionsWeise von Warnungsrichtlinien

Hier finden Sie eine kurze Übersicht über die Funktionsweise von Warnungsrichtlinien und die Warnungen, die ausgelöst werden, wenn die Benutzer-oder Administrator Aktivität den Bedingungen einer Warnungs Richtlinie entspricht.
  
![Übersicht über die Funktionsweise von Warnungsrichtlinien](media/e02a622d-b429-448b-8107-dd1a4770b4e0.png)
  
1. Ein Administrator in Ihrer Organisation erstellt, konfiguriert und aktiviert eine Warnungs Richtlinie mithilfe der Seite **Warnungsrichtlinien** im Security _AMP_ Compliance Center. Sie können auch Warnungsrichtlinien erstellen, indem Sie das Cmdlet **New-protectionalert können** in PowerShell verwenden. Zum Erstellen von Warnungsrichtlinien müssen Sie die Rolle "Organisationskonfiguration" oder "Benachrichtigungen verwalten" im Security & Compliance Center besitzen.
    
2. Ein Benutzer führt eine Aktivität aus, die den Bedingungen einer Warnungs Richtlinie entspricht. Bei Malwareangriffen werden infizierte e-Mail-Nachrichten, die an Benutzer in Ihrer Organisation gesendet werden, eine Warnung auslösen.
    
3. Office 365 generiert eine Warnung, die auf der Seite **Warnungen anzeigen** im Security &amp; Compliance Center angezeigt wird. Wenn e-Mail-Benachrichtigungen für die Warnungs Richtlinie aktiviert sind, sendet Office 365 auch eine Benachrichtigung an eine Listen Empfänger. Die Warnungen, die einem Administrator oder anderen Benutzern auf der Seite **Warnungen anzeigen** angezeigt werden können, werden durch die dem Benutzer zugewiesenen Rollen bestimmt. Weitere Informationen finden Sie im Abschnitt [RBAC-Berechtigungen, die zum Anzeigen von Warnungen erforderlich](#rbac-permissions-required-to-view-alerts) sind.
    
4. Ein Administrator verwaltet Warnungen im Security &amp; Compliance Center. Die Verwaltung von Warnungen besteht in der Zuweisung eines Warnungsstatus zur Unterstützung der Nachverfolgung und Verwaltung von Untersuchungen.
    
## <a name="alert-policy-settings"></a>Warnungsrichtlinien Einstellungen

Eine Warnungs Richtlinie besteht aus einer Reihe von Regeln und Bedingungen, die die Benutzer-oder Administrator Aktivität definieren, die eine Warnung generiert, eine Liste der Benutzer, die die Warnung auslösen, wenn Sie die Aktivität ausführen, und der Schwellenwert, der definiert, wie oft die Aktivität ausgeführt werden muss, bevor ein n Warnung wird ausgelöst. Außerdem kategorisieren Sie die Richtlinie und weisen ihr einen Schweregrad zu. Diese beiden Einstellungen unterstützen Sie bei der Verwaltung von Warnungsrichtlinien (und den Warnungen, die ausgelöst werden, wenn die Richtlinienbedingungen abgeglichen werden), da Sie diese Einstellungen beim Verwalten von Richtlinien &amp; und Anzeigen von Warnungen im Security Compliance Center filtern können. Sie können beispielsweise Warnungen anzeigen, die den Bedingungen derselben Kategorie entsprechen, oder Warnungen mit demselben Schweregrad anzeigen.
  
Um Warnungsrichtlinien anzuzeigen und zu erstellen, wechseln **** \> Sie zu Warnungs **Richtlinien** im Security &amp; Compliance Center. 
  
![Klicken Sie im &amp; Security Complinace Center auf Warnungen, und klicken Sie dann auf Warnungsrichtlinien, um Warnungsrichtlinien anzuzeigen und zu erstellen.](media/09ebd451-8e84-44e1-aefc-63e70bba4d97.png)
  
Eine Warnungs Richtlinie besteht aus den folgenden Einstellungen und Bedingungen.
  
- **Aktivität, die die Warnung verfolgt** – Sie erstellen eine Richtlinie, um eine Aktivität nachzuverfolgen, oder in einigen Fällen ein paar verwandte Aktivitäten, wie beispielsweise das Freigeben einer Datei für einen externen Benutzer, indem Sie Sie freigeben, Zugriffsberechtigungen zuweisen oder einen anonymen Link erstellen. Wenn ein Benutzer die durch die Richtlinie definierte Aktivität ausführt, wird eine Warnung basierend auf den Warnungsschwellenwert Einstellungen ausgelöst.
    
    > [!NOTE]
    > Die Aktivitäten, die Sie verfolgen können, hängen vom Office 365 Enterprise-oder Office 365 US Government-Plan Ihrer Organisation ab. Im Allgemeinen erfordern Aktivitäten im Zusammenhang mit Schadsoftware-Kampagnen und Phishing-Angriffen ein E5/G5-Abonnement oder ein E1/G1-oder E3/G3-Abonnement mit einem Add-on-Abonnement für Threat Intelligence. 
  
- **Aktivitätsbedingungen** – für die meisten Aktivitäten können Sie zusätzliche Bedingungen definieren, die erfüllt sein müssen, damit eine Warnung ausgelöst wird. Häufige Bedingungen sind IP-Adressen (sodass eine Warnung ausgelöst wird, wenn der Benutzer die Aktivität auf einem Computer mit einer bestimmten IP-Adresse oder innerhalb eines IP-Adressbereiches ausführt), ob eine Warnung ausgelöst wird, wenn ein bestimmter Benutzer oder Benutzer diese Aktivität durchführen, und ob die Aktivität wird für einen bestimmten Dateinamen oder eine bestimmte URL ausgeführt. Sie können auch eine Bedingung konfigurieren, die eine Warnung auslöst, wenn die Aktivität von einem beliebigen Benutzer in Ihrer Organisation ausgeführt wird. Beachten Sie, dass die verfügbaren Bedingungen von der ausgewählten Aktivität abhängig sind.
    
- **Wenn die Warnung ausgelöst wird** , können Sie eine Einstellung konfigurieren, die definiert, wie oft eine Aktivität auftreten kann, bevor eine Warnung ausgelöst wird. Auf diese Weise können Sie eine Richtlinie einrichten, mit der eine Warnung generiert wird, wenn eine Aktivität mit den Richtlinienbedingungen übereinstimmt, wenn ein bestimmter Schwellenwert überschritten wird oder wenn das Auftreten der Aktivität, die von der Warnung überwacht wird, für unsere Organisation ungewöhnlich ist. 
    
    ![Konfigurieren, wie Warnungen ausgelöst werden, basierend auf dem Zeitpunkt der Aktivität, einem Schwellenwert oder einer ungewöhnlichen Aktivität für Ihre Organisation](media/97ee1ed2-e7a9-47a2-a980-5f9f63872c65.png)
  
    Wenn Sie die Einstellung basierend auf ungewöhnlichen Aktivitäten auswählen, richtet Office 365 einen Basis Plan Wert ein, der die normale Häufigkeit für die ausgewählte Aktivität definiert. Es dauert bis zu 7 Tage, bis diese Baseline erstellt wird, während der Warnungen nicht generiert werden. Nachdem die Baseline festgelegt wurde, wird eine Warnung ausgelöst, wenn die Häufigkeit der von der Warnungs Richtlinie nachverfolgten Aktivität den geplanten Wert erheblich überschreitet. Für Überwachungsbezogene Aktivitäten (wie Datei-und Ordner Aktivitäten) können Sie eine Baseline basierend auf einem einzelnen Benutzer oder basierend auf allen Benutzern in Ihrer Organisation einrichten. bei Aktivitäten mit Schadsoftware können Sie eine Baseline basierend auf einer einzelnen Schadsoftware-Familie, einem einzelnen Empfänger oder allen Nachrichten in Ihrer Organisation einrichten.
    
    > [!NOTE]
    > Die Möglichkeit zum Konfigurieren von Warnungsrichtlinien basierend auf einem Schwellenwert oder basierend auf ungewöhnlichen Aktivitäten erfordert ein E5/G5-Abonnement oder ein E1/G1-oder E3/G3-Abonnement mit einem Add-on-Abonnement für Threat Intelligence oder Advanced Compliance. Organisationen mit einem E1/G1-und E3/G3-Abonnement können nur eine Warnungs Richtlinie erstellen, bei der bei jeder Aktivität eine Warnung ausgelöst wird. 
  
- **Warnungskategorie** : Sie können einer Richtlinie eine der folgenden Kategorien zuweisen, um die von einer Richtlinie generierten Warnungen zu verfolgen und zu verwalten.
    
  - Datengovernance
    
  - Verhinderung von Datenverlust

  - Nachrichtenübermittlung
    
  - Berechtigungen
    
  - Bedrohungsverwaltung
    
  - Sonstige
    
  Wenn eine Aktivität auftritt, die den Bedingungen der Warnungs Richtlinie entspricht, wird die generierte Warnung mit der in dieser Einstellung definierten Kategorie gekennzeichnet. Auf diese Weise können Sie Benachrichtigungen nachverfolgen und verwalten, die dieselbe Kategorieeinstellungen auf der Seite **Benachrichtigungen anzeigen** im Security _AMP_ Compliance Center aufweisen, da Sie Warnungen basierend auf der Kategorie sortieren und Filtern können. 
    
- **Warnungsschweregrad** – ähnlich wie bei der Warnungskategorie weisen Sie Warnungsrichtlinien ein Severity-Attribut ( **niedrig**, **Mittel**oder **hoch**) zu. Wie bei der Warnungskategorie wird bei einer Aktivität, die mit den Bedingungen der Warnungs Richtlinie übereinstimmt, die generierte Warnung mit dem gleichen Schweregrad gekennzeichnet, der für die Warnungs Richtlinie festgelegt ist. Auf diese Weise können Sie auch Warnungen mit der gleichen Schweregrad Einstellung auf der Seite **Warnungen anzeigen** verfolgen und verwalten. Sie können beispielsweise die Liste der Warnungen filtern, sodass nur Warnungen mit einem **hohen** Schweregrad angezeigt werden. 
    
    > [!TIP]
    > Erwägen Sie beim Einrichten einer Warnungs Richtlinie das Zuweisen eines höheren Schweregrads zu Aktivitäten, die zu schwerwiegenden nachteiligen Folgen führen können, beispielsweise die Erkennung von Schadsoftware nach der Bereitstellung an Benutzer, die Anzeige vertraulicher oder klassifizierter Daten, die Freigabe von Daten für externe Benutzer. oder andere Aktivitäten, die zu Datenverlust oder Sicherheitsbedrohungen führen können. Dies kann Ihnen bei der Priorisierung von Warnungen und den Aktionen helfen, die Sie ausführen, um die zugrunde liegenden Ursachen zu ermitteln und zu beheben. 
  
- **E-Mail-Benachrichtigungen** – Sie können die Richtlinie so einrichten, dass e-Mail-Benachrichtigungen an eine Liste von Benutzern gesendet werden (oder nicht gesendet werden), wenn eine Warnung ausgelöst wird. Sie können auch einen täglichen Benachrichtigungs Grenzwert festlegen, sodass nach Erreichen der maximalen Anzahl von Benachrichtigungen an diesem Tag keine weiteren Benachrichtigungen mehr für die Warnung gesendet werden. Zusätzlich zu e-Mail-Benachrichtigungen können Sie oder andere Administratoren die Warnungen anzeigen, die von einer Richtlinie auf der Seite **Warnungen anzeigen** ausgelöst werden. Erwägen Sie, e-Mail-Benachrichtigungen für Warnungsrichtlinien einer bestimmten Kategorie zu aktivieren oder die Einstellung für einen höheren Schweregrad festzulegen. 
  
## <a name="default-alert-policies"></a>Standard Warnungsrichtlinien

Office 365 bietet integrierte Warnungsrichtlinien, mit denen die Exchange-Administratorberechtigungen für Missbrauch, Schadsoftware und Datensteuerung identifiziert werden können. Auf der Seite **Warnungsrichtlinien** werden die Namen dieser integrierten Richtlinien fett formatiert, und der Richtlinientyp ist als **System**definiert. Diese Richtlinien sind standardmäßig aktiviert. Sie können diese Richtlinien deaktivieren (oder wieder aktivieren), eine Liste von Empfängern zum Senden von e-Mail-Benachrichtigungen einrichten und eine Tägliche Benachrichtigungsgrenze festlegen. Die anderen Einstellungen für diese Richtlinien können nicht bearbeitet werden.
  
In der folgenden Tabelle werden die verfügbaren Standard Warnungsrichtlinien und die Kategorie aufgeführt, der jede Richtlinie zugewiesen ist. Beachten Sie, dass diese Kategorie verwendet wird, um zu bestimmen, welche Warnungen ein Benutzer auf der Seite Warnungen anzeigen anzeigen kann. Weitere Informationen finden Sie im Abschnitt [RBAC-Berechtigungen, die zum Anzeigen von Warnungen erforderlich](#rbac-permissions-required-to-view-alerts) sind.  

Die Tabelle gibt außerdem an, welche Office 365 Enterprise-und Office 365 US Government-Pläne für jeden erforderlich sind. Beachten Sie, dass einige standardmäßige Warnungsrichtlinien verfügbar sind, wenn Ihre Organisation zusätzlich zu einem E1/G1-oder E3/G3-Abonnement über das entsprechende Add-on-Abonnement verfügt. 
  
|**Standard Warnungs Richtlinie**|**Beschreibung**|**Category**|**Office 365 Enterprise-Abonnement**|
|:-----|:-----|:-----|:-----|
|**Erstellung der Weiterleitungs-/Umleitungsregel** <br/> |Generiert eine Warnung, wenn in Ihrer Organisation eine Posteingangsregel für Ihr Postfach erstellt wird, die Nachrichten an ein anderes e-Mail-Konto weiterleitet oder umleitet. Diese Richtlinie verfolgt nur Posteingangsregeln, die mit Outlook im Web (früher als Outlook Web App bezeichnet) oder mit Exchange Online PowerShell erstellt werden. Diese Richtlinie hat eine **niedrige** Dringlichkeits Einstellung. Weitere Informationen mithilfe von Posteingangsregeln zum Weiterleiten und Umleiten von e-Mails in Outlook im Web finden Sie unter [Verwenden von Regeln in Outlook im Web zum automatischen Weiterleiten von Nachrichten an ein anderes Konto](https://support.office.com/article/1433e3a0-7fb0-4999-b536-50e05cb67fed).  <br/> |Bedrohungsverwaltung <br/> |E1/G1, E3/G3 oder E5/G5  <br/> |
|**eDiscovery-Suche gestartet oder exportiert** <br/> |Generiert eine Warnung, wenn ein Benutzer das Tool für die Inhaltssuche im Security & Compliance Center verwendet. Wenn die folgenden Inhalts Suchaktivitäten ausgeführt werden, wird eine Warnung ausgelöst: <br/><br/>• Eine Inhaltssuche wird gestartet<br/>• Die Ergebnisse einer Inhaltssuche werden exportiert<br/>• Ein Bericht über Inhaltssuche wird exportiert<br/><br/>Benachrichtigungen werden auch dann trigged, wenn die vorherigen Inhalts Suchaktivitäten in Verbindung mit einem eDiscovery-Fall durchgeführt werden. Diese Richtlinie hat eine Einstellung für **mittlere** Schweregrade. Weitere Informationen zu Inhalts Suchaktivitäten finden Sie unter [Suchen nach eDiscovery-Aktivitäten im Office 365-Überwachungsprotokoll](search-for-ediscovery-activities-in-the-audit-log.md#ediscovery-activities). <br/> |Bedrohungsverwaltung<br/> |E1/G1, E3/G3 oder E5/G5  <br/> |
|**Erweiterung des Exchange-Administrator Privilegs** <br/> |Generiert eine Warnung, wenn einer Person in Ihrer Exchange Online-Organisation Administratorberechtigungen zugewiesen werden. Wenn beispielsweise ein Benutzer zur Rollengruppe "Organisationsverwaltung" in Exchange Online hinzugefügt wird. Diese Richtlinie hat eine **niedrige** Dringlichkeits Einstellung.  <br/> |Berechtigungen <br/> |E1/G1, E3/G3 oder E5/G5  <br/> |
|**Nachrichten wurden verzögert** <br/> |Generiert eine Warnung, wenn Office 365 keine e-Mail-Nachrichten an Ihre lokale Organisation oder an Partnerserver über einen Connector übermitteln kann. Wenn dies der Fall ist, wird die Nachricht in der Warteschlange in Office 365. Diese Warnung wird ausgelöst, wenn es 2.000 oder mehr Nachrichten gibt, die länger als eine Stunde in der Warteschlange stehen. Diese Richtlinie hat eine Einstellung für **hohen** Schweregrad.  <br/> |Nachrichtenübermittlung<br/> |E1/G1, E3/G3 oder E5/G5  <br/> |
|**Nach der Übertragung erkannte Schadsoftware-Kampagne** <br/> |Generiert eine Warnung, wenn eine ungewöhnlich viele Nachrichten mit Schadsoftware an Postfächer in Ihrer Organisation übermittelt werden. Wenn dieses Ereignis auftritt, entfernt Office 365 die infizierten Nachrichten aus Exchange Online-Postfächern. Diese Richtlinie hat eine Einstellung für **hohen** Schweregrad.  <br/> |Bedrohungsverwaltung<br/> |E5/G5 oder Office 365 Threat Intelligence-Add-on-Abonnement  <br/> |
|**Malware Kampagne erkannt und blockiert** <br/> |Generiert eine Warnung, wenn jemand versucht hat, eine ungewöhnlich hohe Anzahl von e-Mail-Nachrichten zu senden, die einen bestimmten Typ von Schadsoftware an Benutzer in Ihrer Organisation enthalten. Wenn dieses Ereignis auftritt, werden die infizierten Nachrichten von Office 365 blockiert und nicht an Postfächer zugestellt. Diese Richtlinie hat eine **niedrige** Dringlichkeits Einstellung.  <br/> |Bedrohungsverwaltung<br/> |E5/G5 oder Office 365 Threat Intelligence-Add-on-Abonnement  <br/> |
|**In SharePoint und OneDrive erkannte Malware Kampagne** <br/> |Generiert eine Warnung, wenn in Dateien, die in SharePoint-Websites oder OneDrive-Konten in Ihrer Organisation gespeichert sind, eine ungewöhnlich große Anzahl von Schadsoftware oder Viren erkannt wird. Diese Richtlinie hat eine Einstellung für **hohen** Schweregrad.  <br/> |Bedrohungsverwaltung<br/> |E5/G5 oder Office 365 Threat Intelligence-Add-on-Abonnement  <br/> |
|**Ungewöhnliche externe Benutzerdatei Aktivität** <br/> |Generiert eine Warnung, wenn eine normalerweise hohe Anzahl von Aktivitäten für Dateien in SharePoint oder OneDrive von Benutzern außerhalb Ihrer Organisation ausgeführt wird. Hierzu gehören Aktivitäten wie der Zugriff auf Dateien, das Herunterladen von Dateien und das Löschen von Dateien. Diese Richtlinie hat eine Einstellung für **hohen** Schweregrad.  <br/> |Datengovernance<br/> |E5/G5 oder Office 365 Threat Intelligence oder Advanced Compliance-Add-on-Abonnement  <br/> |
|**Ungewöhnliche Menge an externer Dateifreigabe** <br/> |Generiert eine Warnung, wenn eine normalerweise hohe Anzahl von Dateien in SharePoint oder OneDrive für Benutzer außerhalb Ihrer Organisation freigegeben wird. Diese Richtlinie hat eine Einstellung für **mittlere** Schweregrade.  <br/> |Datengovernance<br/> |E5/G5 oder Office 365 Threat Intelligence oder Advanced Compliance-Add-on-Abonnement  <br/> |
|**UnGewöhnlicher Umfang des Löschens von Dateien** <br/> |Generiert eine Warnung, wenn eine ungewöhnlich viele Dateien in SharePoint oder OneDrive innerhalb eines kurzen Zeitrahmens gelöscht werden. Diese Richtlinie hat eine Einstellung für **mittlere** Schweregrade.  <br/> |Datengovernance <br/> |E5/G5 oder Office 365 Threat Intelligence oder Advanced Compliance-Add-on-Abonnement  <br/> |
|**Ungewöhnliche Vergrößerung der als Phishing gemeldeten e-Mails** <br/> |Generiert eine Warnung, wenn die Anzahl der Personen in Ihrer Organisation, die das Berichtnachrichten-Add-in in Outlook verwenden, die Nachrichten als Phishing-e-Mail melden. Diese Richtlinie hat eine Einstellung für **hohen** Schweregrad. Weitere Informationen zu diesem Add-in finden Sie unter [Verwenden des Berichtnachrichten-Add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).  <br/> |Bedrohungsverwaltung<br/> |E5/G5 oder Office 365 Threat Intelligence-Add-on-Abonnement  <br/> |
|**Benutzer darf keine e-Mails senden** <br/> |Generiert eine Warnung, wenn in Ihrer Organisation keine ausgehenden e-Mails mehr gesendet werden. Dies führt normalerweise zu einem kompromittierten Konto, und der Benutzer wird auf der Seite " **eingeschränkte Benutzer** " im Security _AMP_ Compliance Center aufgeführt. (Um auf diese Seite zuzugreifen, wechseln Sie zu **Threat Management _GT_ Review _GT_ restrictEd users**). Diese Richtlinie hat eine Einstellung für **hohen** Schweregrad. Weitere Informationen zu eingeschränkten Benutzern finden Sie unter [Entfernen eines Benutzers, einer Domäne oder einer IP-Adresse aus einer Sperrliste nach dem Senden von Spam-e-Mails](https://docs.microsoft.com/office365/securitycompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email).  <br/> |Bedrohungsverwaltung<br/> |E1/G1, E3/G3 oder E5/G5  <br/> |
|||||
   
Beachten Sie, dass die ungewöhnliche Aktivität, die von einigen der integrierten Richtlinien überwacht wird, auf dem gleichen Prozess wie die zuvor beschriebene Einstellung für den Warnungsschwellenwert basiert. Office 365 legt einen Basis Wert fest, der die normale Häufigkeit für "übliche" Aktivität definiert. Warnungen werden dann ausgelöst, wenn die Häufigkeit der Aktivitäten, die von der integrierten Warnungs Richtlinie verfolgt werden, den geplanten Wert erheblich überschreitet.
 
## <a name="viewing-alerts"></a>Anzeigen von Warnungen

Wenn eine von Benutzern in Ihrer Organisation durchgeführte Aktivität mit den Einstellungen einer Warnungs Richtlinie übereinstimmt, wird eine Warnung generiert und auf der Seite **Warnungen anzeigen** im Security &amp; Compliance Center angezeigt. Abhängig von den Einstellungen einer Warnungs Richtlinie wird eine e-Mail-Benachrichtigung auch an eine Liste der angegebenen Benutzer gesendet, wenn eine Warnung ausgelöst wird. Für jede Warnung werden im Dashboard auf der Seite **Warnungen anzeigen** der Name der entsprechenden Warnungs Richtlinie, der Schweregrad und die Kategorie für die Warnung (in der Warnungs Richtlinie definiert) und die Häufigkeit, mit der eine Aktivität aufgetreten ist, angezeigt, die dazu führte, dass die Warnung generiert Dieser Wert basiert auf der Einstellung der Schwellenwerte für die Warnungs Richtlinie. Im Dashboard wird auch der Status für jede Warnung angezeigt. Weitere Informationen zur Verwendung der Status-Eigenschaft zum Verwalten von Warnungen finden Sie im Abschnitt [Managing Alerts](#managing-alerts) . 
  
Um Warnungen anzuzeigen, wechseln Sie **** \> **** zu Warnungen im Security &amp; Compliance Center. 
  
![Klicken Sie im &amp; Security Complinace Center auf Warnungen, und klicken Sie dann auf Warnungen anzeigen, um Warnungen anzuzeigen.](media/ec5ea59b-bf61-459f-8b65-970ab4bb8bcc.png)
  
Sie können die folgenden Filter verwenden, um eine Teilmenge aller Warnungen auf der Seite **Benachrichtigungen anzeigen** anzuzeigen. 
  
- **Status** -verwenden Sie diesen Filter, um Warnungen anzuzeigen, denen ein bestimmter Status zugewiesen wurde. der Standardstatus ist **aktiv**. Sie oder andere Administratoren können den Statuswert ändern.
    
- **Richtlinie** – verwenden Sie diesen Filter, um Warnungen anzuzeigen, die mit der Einstellung einer oder mehrerer Warnungsrichtlinien übereinstimmen. Sie können auch nur alle Warnungen für alle Warnungsrichtlinien anzeigen.
    
- **Zeitbereich** – verwenden Sie diesen Filter, um Warnungen anzuzeigen, die innerhalb eines bestimmten Datums-und Uhrzeitbereichs generiert wurden.
    
- **Schweregrad** -verwenden Sie diesen Filter, um Warnungen anzuzeigen, denen ein bestimmter Schweregrad zugewiesen wurde.
    
- **Category** – verwenden Sie diesen Filter, um Warnungen aus einer oder mehreren Warnungs Kategorien anzuzeigen.

- **Source** -verwenden Sie diesen Filter, um Warnungen anzuzeigen, die durch Warnungsrichtlinien im Security _AMP_ Compliance Center ausgelöst wurden, oder Warnungen, die von sicherheitsRichtlinien für Office 365 Cloud App ausgelöst werden, oder beides. Weitere Informationen zu Sicherheitswarnungen in Office 365 Cloud App finden Sie im Abschnitt ["Anzeigen von Sicherheitswarnungen](#viewing-cloud-app-security-alerts) in der Cloud-app".

## <a name="rbac-permissions-required-to-view-alerts"></a>Erforderliche RBAC-Berechtigungen zum Anzeigen von Warnungen

> [!NOTE]
> Die in diesem Abschnitt beschriebenen Funktionen werden ab dem 20. Februar 2019 für Organisationen bereitgestellt, die bis Ende März 2019 weltweit abgeschlossen werden.

Die den Benutzern in Ihrer Organisation zugewiesenen rollenbasierte Zugriffssteuerung (Role Bases Access Control, RBAC) bestimmt, welche Warnungen ein Benutzer auf der Seite **Warnungen anzeigen** sehen kann. Wie wird das erreicht? Die den Benutzern zugewiesenen Verwaltungsrollen (basierend auf Ihrer Mitgliedschaft in Rollengruppen im Security & Compliance Center) bestimmen, welche Warnungs Kategorien ein Benutzer auf der Seite **Warnungen anzeigen** sehen kann. Im Folgenden finden Sie einige Beispiele:

- Mitglieder der Rollengruppe "Datensatzverwaltung" können nur die Warnungen anzeigen, die von Warnungsrichtlinien generiert werden, denen die Kategorie " **Datensteuerung** " zugewiesen ist.

- Mitglieder der Rollengruppe "Compliance-Administrator" können keine Warnungen anzeigen, die von Warnungsrichtlinien generiert wurden, denen die Kategorie " **Bedrohungs Verwaltung** " zugewiesen ist. 

- Mitglieder der eDiscovery-Manager-Rollengruppe können keine Warnungen anzeigen, da keine der zugewiesenen Rollen die Berechtigung zum Anzeigen von Warnungen aus einer Warnungskategorie bereitstellt.

Mit diesem Entwurf (basierend auf RBAC-Berechtigungen) können Sie festlegen, welche Warnungen von Benutzern in bestimmten Auftrags Rollen in Ihrer Organisation angezeigt (und verwaltet) werden können. 

In der folgenden Tabelle sind die Rollen aufgeführt, die zum Anzeigen von Warnungen aus den 6 verschiedenen Warnungs Kategorien erforderlich sind. Die erste Spalte in der Tabelle enthält alle Rollen im Security & Compliance Center.  Ein Häkchen zeigt an, dass ein Benutzer, dem diese Rolle zugewiesen ist, Warnungen aus der entsprechenden Warnungskategorie in der obersten Zeile anzeigen kann.

Informationen zu der Kategorie, der eine Standard Benachrichtigungsrichtlinie zugewiesen ist, finden Sie in der Tabelle im Abschnitt [standardmäßige Warnungsrichtlinien](#default-alert-policies) .

|<br/>|Datengovernance|Verhinderung von Datenverlust|Nachrichtenübermittlung|Berechtigungen|Bedrohungsverwaltung|Sonstige | 
|:---------|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|
|Überwachungsprotokolle <br/> |         ||         |         |         |         |
|Fallverwaltung <br/>|         |         |         |         |         |         |
|Complianceadministrator<br/>|![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Compliance-Suche<br/>|         |         |         |         |         |         |
|Geräteverwaltung<br/>|         |         |         |         |         |         |
|Disposition-Verwaltung<br/>|         |         |         |         |         |         |
|DLP-Compliance-Verwaltung<br/>|         |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |
|Exportieren<br/>|         |         |         |         |         |         |
|Situ<br/>|         |         |         |         |         |         |
|
            Benachrichtigungen verwalten<br/>|         |         |         |         |         |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Organisationskonfiguration|         |         |         |         |         |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Vorschau <br/>|         |         |         |         |         |         |
|Datensatzverwaltung <br/>|![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|AufbewahrungsVerwaltung <br/>| ![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Überprüfung <br/>|         |         |         |         |         |         |
|RMS-entSchlüsselung<br/>|         |         |         |         |         |         |
|Rollenverwaltung<br/>|         |         |         |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |
|Suchen und löschen<br/>|         |         |         |         |         |         |
|Sicherheitsadministrator<br/>||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| | ![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Sicherheits Leser<br/>|         |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| | ![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)
|Ansicht "Dienstsicherheit"<br/>|         |         |         |         |         |         |
|Supervisory Review-Administrator<br/>|         |         |         |         |         |         |
|Überwachungsprotokolle für die Anzeige<br/>|         |         |         |         |         |         |
|Nur-anzeigen-Geräteverwaltung<br/>|         |         |         |         |         |         |
|Management der DLP-KonformitätsVerwaltung<br/>|         |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |
|Benachrichtigungen verwalten<br/>|         |         |         |         |         |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Schreibgeschützte Empfänger<br/>|         |         |  ![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       |         ||         |
|Datensatzverwaltung mit Schreibschutz<br/>|![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|AufbewahrungsVerwaltung (nur anzeigen)<br/>|![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|         |         |         |         |         |         |

**Tipp:** Führen Sie die folgenden Befehle in Security & Compliance Center PowerShell aus, um die Rollen anzuzeigen, die den einzelnen Standardrollengruppen zugewiesen sind: 

```
$RoleGroups = Get-RoleGroup

$RoleGroups | foreach {Write-Output -InputObject `r`n,$_.Name,"-----------------------"; Get-RoleGroup $_.Identity | Select-Object -ExpandProperty Roles}
```
Sie können auch die Rollen anzeigen, die einer Rollengruppe im Security & Compliance Center zugewiesen sind. Wechseln Sie zur Seite **Berechtigungen** , und klicken Sie auf eine Rollengruppe. Die zugewiesenen Rollen werden auf der Flyout-Seite aufgeführt.


## <a name="managing-alerts"></a>Verwalten von Warnungen

Nachdem Warnungen generiert und auf der Seite **Warnungen anzeigen** im Security &amp; Compliance Center angezeigt wurden, können Sie Sie selektieren, untersuchen und beheben. Hier sind einige Aufgaben, die Sie zum Verwalten von Warnungen ausführen können. 
  
- **Status zu Warnungen zuweisen** – Sie können Alerts einen der folgenden Status zuweisen: **aktiv** (standardWert), unter **Suchen**, **aufgelöst**oder **geschlossen**. Anschließend können Sie nach dieser Einstellung filtern, um Warnungen mit derselben Statuseinstellung anzuzeigen. Diese Statuseinstellung kann helfen, den Prozess der Verwaltung von Warnungen nachzuverfolgen.
    
- **Warnungsdetails anzeigen** -Sie können auf eine Warnung klicken, um eine Flyout-Seite mit Details zur Warnung anzuzeigen. Die detaillierten Informationen hängen von der entsprechenden Warnungs Richtlinie ab, aber Sie beinhaltet in der Regel Folgendes: Name des tatsächlichen Vorgangs, der die Warnung ausgelöst hat (beispielsweise ein Cmdlet), eine Beschreibung der Aktivität, die die Warnung ausgelöst hat, der Benutzer (oder die Liste der Benutzer) Wer die Warnung ausgelöst hat, und den Namen (und Link zu) der entsprechenden Warnungs Richtlinie.
    
  - Der Name des tatsächlichen Vorgangs, der die Warnung ausgelöst hat, beispielsweise ein Cmdlet oder ein Überwachungsprotokoll Vorgang.
    
  - Eine Beschreibung der Aktivität, die die Warnung ausgelöst hat.
    
  - Der Benutzer, der die Warnung ausgelöst hat; Dies ist nur für Warnungsrichtlinien enthalten, die zum Nachverfolgen eines einzelnen Benutzers oder einer einzelnen Aktivität eingerichtet sind.
    
  - Die Häufigkeit, mit der die von der Warnung verfolgte Aktivität ausgeführt wurde. Beachten Sie, dass diese Anzahl möglicherweise nicht mit der tatsächlichen Anzahl verwandter Warnungen übereinstimmt, die auf der Seite Warnungen anzeigen aufgeführt sind, da möglicherweise zusätzliche Warnungen ausgelöst wurden.
    
  - Ein Link zu einer Aktivitätsliste, die ein Element für jede ausgeführte Aktivität enthält, die die Warnung ausgelöst hat. Jeder Eintrag in dieser Liste identifiziert, wann die Aktivität aufgetreten ist, der Name des tatsächlichen Vorgangs (wie "fileDeleted") und der Benutzer, der die Aktivität ausgeführt hat, das Objekt (wie eine Datei, ein eDiscovery-Fall oder ein Postfach), für das die Aktivität ausgeführt wurde, und die IP die Adresse des Computer des Benutzers. Für Malware bezogene Warnungen wird dieser Link zu einer Nachrichtenliste angezeigt.
    
  - Der Name (und Link zu) der entsprechenden Warnungs Richtlinie.
    
- **E-Mail-Benachrichtigungen unterdrücken** – Sie können e-Mail-Benachrichtigungen aus der Flyout-Seite für eine Warnung deaktivieren (oder ausblenden). Wenn Sie e-Mail-Benachrichtigungen unterdrücken, sendet Office 365 keine Benachrichtigungen, wenn Aktivitäten oder Ereignisse mit den Bedingungen der Warnungs Richtlinie übereinstimmen. Warnungen werden jedoch weiterhin ausgelöst, wenn die von Benutzern ausgeführten Aktivitäten mit den Bedingungen der Warnungs Richtlinie übereinstimmen. Sie können e-Mail-Benachrichtigungen auch deaktivieren, indem Sie die Warnungs Richtlinie bearbeiten.
    
- **Auflösen von Warnungen** : Sie können eine Warnung als aufgelöst auf der Flyout-Seite für eine Warnung markieren (wodurch der Status der Warnung auf " **aufgelöst**" festgelegt wird). Wenn Sie den Filter nicht ändern, werden aufgelöste Warnungen nicht auf der Seite **Warnungen anzeigen** angezeigt. 
    
## <a name="viewing-cloud-app-security-alerts"></a>Anzeigen von Sicherheitswarnungen in der Cloud-App
  
Warnungen, die von Office 365 Cloud App-Sicherheitsrichtlinien ausgelöst werden, werden jetzt im Security & Compliance Center auf der Seite **Warnungen anzeigen** angezeigt. Hierzu gehören Warnungen, die durch Aktivitätsrichtlinien und Warnungen ausgelöst werden, die durch Anomalie-Erkennungsrichtlinien in Office 365 Cloud App Security ausgelöst werden. Dies führt dazu, dass Sie alle Benachrichtigungen im Security & Compliance Center anzeigen können. Beachten Sie, dass Office 365 Cloud App Security nur für Organisationen mit einem Office 365 Enterprise E5-oder Office 365 US Government G5-Abonnement verfügbar ist. Weitere Informationen finden Sie unter [Overview of Office 365 Cloud App Security](office-365-cas-overview.md).

Darüber hinaus können Organisationen mit Microsoft Cloud App Security im Rahmen eines Enterprise Mobility + Security E5-Abonnements oder als eigenständiger Dienst auch Cloud-App-Sicherheitswarnungen im Zusammenhang mit Office 365-apps und-Diensten im Sicherheits & anzeigen. Compliance Center.

Um nur Sicherheitswarnungen zur Cloud-App im Security & Compliance Center anzuzeigen, verwenden Sie den **Quell** Filter, und wählen Sie **Cloud App Security**aus.

![Verwenden des Quell Filters zum Anzeigen von Sicherheitswarnungen in der Cloud-App](media/FilterCASAlerts.png)

Ähnlich wie bei einer Warnung, die durch eine Warnungs Richtlinie für das Security & Compliance Center ausgelöst wurde, können Sie auf eine Sicherheitswarnung der Cloud-App klicken, um eine Flyout-Seite mit Details zur Warnung anzuzeigen. Die Warnung enthält einen Link zum Anzeigen der Details und zum Verwalten der Warnung im Sicherheitsportal der Cloud-App sowie einen Link zur entsprechenden Sicherheitsrichtlinie für Cloud-apps, die die Warnung ausgelöst hat. Weitere Informationen finden Sie unter [Review and Take Action on Alerts in Office 365 Cloud App Security](review-office-365-cas-alerts.md).

![Warnungsdetails enthalten Links zum Cloud-App-Sicherheitsportal](media/CASAlertDetail.png)

> [!IMPORTANT]
> Durch das Ändern des Status einer Sicherheitswarnung der Cloud-App im Security & Compliance Center wird der Auflösungsstatus für dieselbe Warnung im Sicherheitsportal der Cloud-APP nicht aktualisiert. Wenn Sie beispielsweise den Status der Warnung im Security & Compliance Center als **aufgelöst** markieren, wird der Status der Warnung im Sicherheitsportal der Cloud-APP nicht geändert. Um eine Cloud-App-Sicherheitswarnung zu beheben oder zu schließen, verwalten Sie die Warnung im Cloud-App-Sicherheitsportal.
