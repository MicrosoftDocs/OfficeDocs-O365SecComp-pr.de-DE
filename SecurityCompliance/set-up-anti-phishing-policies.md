---
title: Einrichten von ATP-Antiphishingrichtlinien in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578
description: Schutz vor Phishing, mit umfassendem Schutz als Teil von Office 365 Advanced Threat Protection und grundlegender Schutz in Office 365 Exchange Online Protection, können zum Schutz Ihrer Organisation vor böswilligen Identitätswechsel-basierten Phishing-Angriffen beitragen. und andere Phishing-Angriffe.
ms.openlocfilehash: 94aa4ca6339ee0e0c250e96b9d8a499c83e964f7
ms.sourcegitcommit: 32cb896aef370764ec6e8f8278ebaf16f1c5ff37
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30123966"
---
# <a name="set-up-office-365-atp-anti-phishing-and-anti-phishing-policies"></a>Einrichten von Office 365 ATP-Antiphishing-und-Phishing-Richtlinien

[ATP Anti-Phishing Protection](atp-anti-phishing.md), Teil von [Office 365 Advanced Threat Protection](office-365-atp.md), kann dazu beitragen, Ihre Organisation vor böswilligen Identitätswechsel-basierten Phishing-Angriffen und anderen Phishing-Angriffen zu schützen. Wenn Sie ein Office 365 Enterprise-globaler oder Sicherheitsadministrator sind, können Sie ATP-Phishing-Richtlinien einrichten. 

Phishing-Angriffe kommen in einer Vielzahl von Formularen vor, die auf Commodity-basierten Angriffen oder gezieltem Spear-Phishing oder Walfang basieren. Aufgrund der wachsenden Komplexität ist es für selbst ein geschultes Auge schwierig, einige dieser ausgeklügelten Angriffe zu identifizieren. Glücklicherweise kann Office 365 Advanced Threat Protection helfen. Sie können eine ATP-Richtlinie zum Schutz vor Phishing einrichten, um sicherzustellen, dass Ihre Organisation vor solchen Angriffen geschützt ist.
  
> [!NOTE]
> ATP-Phishing ist nur in Advanced Threat Protection (ATP) verfügbar. ATP ist in Abonnements wie [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht Office 365 ATP enthält, können Sie möglicherweise ATP als Add-on erwerben. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). Stellen Sie sicher, dass Ihre Organisation die neueste Version von Office 365 proPlus unter Windows verwendet, um den Schutz vor Phishing in vollem Umfang zu nutzen. 

Eine Richtlinie zum Schutz vor Phishing ist auch für Office 365 Exchange Online Protection verfügbar, mit einem begrenzten Schutz vor Spoofing, der vor Authentifizierungs-und Täuschungs basierten Angriffen geschützt werden soll.
  
Was ist zu tun:
  
1. Überarbeiten Sie die Voraussetzungen.
    
2. Erfahren Sie mehr über die Anti-Phishing-und ATP-AntiPhishing-Optionen.
    
3. Richten Sie eine Anti-Phishing-Richtlinie oder eine ATP-Richtlinie zum Schutz vor Phishing ein.
    
## <a name="review-the-prerequisites"></a>Überarbeiten der Voraussetzungen

- Um ATP-Richtlinien zu definieren (oder zu bearbeiten), muss Ihnen eine entsprechende Rolle zugewiesen werden. Einige Beispiele werden in der folgenden Tabelle beschrieben: <br>

    |Rolle  |Wo/wie zugewiesen  |
    |---------|---------|
    |Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
    |Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
    |Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
    Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).

- Sie werden wahrscheinlich mehrere Phishing-Richtlinien für Ihre Organisation einrichten. Office 365 erzwingt diese Richtlinien in der Reihenfolge, in der Sie auf der **Seite Anti-Phishing** und **ATP-** Antiphishingseiten im Security &amp; Compliance Center aufgeführt sind. Nachdem Sie Ihre [Richtlinienoptionen](#learn-about-atp-anti-phishing-policy-options)überprüft haben, sollten Sie sich etwas Zeit nehmen, um zu bestimmen, wie viele Richtlinien Sie benötigen und welche Priorität es hat. 
    
- Planen Sie die Einrichtung ihrer ersten Anti-Phishing-Richtlinie ungefähr 5-15 Minuten.
    
- Erlauben Sie bis zu 30 Minuten, bis Ihre neue oder aktualisierte Richtlinie auf alle Office 365-Rechenzentren verteilt ist.
    
## <a name="set-up-an-anti-phishing-or-atp-anti-phishing-policy"></a>Einrichten einer Anti-Phishing-oder ATP-AntiPhishing-Richtlinie

Jede Organisation in Office 365 hat eine standardmäßige Anti-Phishing-Richtlinie, die für alle Benutzer gilt. Sie können mehrere benutzerdefinierte Anti-Phishing-Richtlinien erstellen, die Sie für bestimmte Benutzer, Gruppen oder Domänen innerhalb Ihrer Organisation einrichten können. Die von Ihnen erstellten benutzerdefinierten Richtlinien haben Vorrang vor der Standardrichtlinie. Sie können Richtlinien zum Schutz vor Phishing im Office 365 Security &amp; Compliance Center hinzufügen, bearbeiten und löschen.
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an. 
    
2. Wählen Sie im Office 365 &amp; Security Compliance Center im linken Navigationsbereich unter Bedrohungs **Verwaltung**die Option **Richtlinie**aus.
    
3. Wählen Sie auf der Seite **Richtlinie** **Anti-Phishing** oder **ATP-Phishing**aus.
    
4. Führen Sie auf der Seite **Anti-Phishing** -oder **ATP-AntiPhishing** einen der folgenden Schritte aus: 
    
    - Um eine neue Richtlinie hinzuzufügen, wählen Sie **+ Erstellen**.
    - Wenn Sie eine vorhandene Richtlinie bearbeiten möchten, wählen Sie den Richtliniennamen aus der auf der Seite **Anti-Phishing** angezeigten Liste aus. (Alternativ können Sie die **Standardrichtlinie** oberhalb der Liste auswählen.) Klicken Sie auf der angezeigten Seite auf **Richtlinie bearbeiten**.  
    
5. Geben Sie den Namen, die Beschreibung und die Einstellungen für die Richtlinie an. Weitere Informationen finden Sie unter Informationen [zu Optionen für die ATP-AntiPhishing-Richtlinie](#learn-about-atp-anti-phishing-policy-options) . 
    
6. Nachdem Sie Ihre Einstellungen überprüft haben, wählen Sie **Diese Richtlinie erstellen** (oder **Speichern**). 
    
## <a name="learn-about-atp-anti-phishing-policy-options"></a>Informationen zu Optionen für die ATP-AntiPhishing-Richtlinie

Beim Einrichten oder Bearbeiten Ihrer ATP-Richtlinie zum Schutz vor Phishing können Sie aus verschiedenen Optionen auswählen, die den anspruchsvollsten und umfassendsten, wie in der folgenden Tabelle beschrieben, bieten.
  
|**Diese Einstellung**|**Funktion**|**Verwenden Sie, wenn Sie Folgendes möchten:**|
|:-----|:-----|:-----|
|**Hinzufügen von Benutzern zu schützen** <br/> |Definiert, welche e-Mail-Adressen von der Richtlinie geschützt werden. Sie können bis zu 60 interne und externe Adressen, die Sie vor Identitätswechsel schützen möchten, hinzufügen.  <br/> |Wenn Sie sicherstellen möchten, dass e-Mails von außerhalb Ihrer Organisation kein Identitätswechsel eines der Benutzer in der Liste der Benutzer sind, die Sie schützen. Beispiele für Benutzer, die Sie schützen möchten, sind hochrangige Führungskräfte, Unternehmer, externe Vorstandsmitglieder usw.<br/> Diese Liste der geschützten Benutzer unterscheidet sich von der Liste der Personen, auf die die Richtlinie angewendet wird, oder besser gesagt, für die die Richtlinie erzwungen wird. Sie definieren die Liste gilt für im Abschnitt **angewendet auf** der Richtlinienoptionen.<br/> Wenn Sie beispielsweise als zu `Mary Smith <marys@contoso.com>` schützender Benutzer hinzufügen, wenden Sie die Richtlinie auf die Gruppe "alle Benutzer" an. Dadurch wird sichergestellt, dass eine e-Mail-Nachricht, die als Identitätswechsel an einen Benutzer in der Gruppe "alle Benutzer" gesendet wurde, von der Richtlinie verarbeitet wird.<br/> |
|**Hinzufügen von Domänen zum Schutz** <br/> |Ermöglicht Ihnen die Auswahl der Domänen, die vor Identitätswechsel geschützt werden sollen. Sie können angeben, dass die Richtlinie alle benutzerdefinierten Domänen, eine durch trennzeichengetrennte Liste von Domänen oder eine Kombination aus beiden enthält. Wenn Sie **automatisch Domänen einbeziehen, die ich**besitze, und Sie später eine Domäne zu ihrer Office 365-Organisation hinzufügen, wird diese Richtlinie zum Schutz vor Phishing für die neue Domäne eingerichtet.<br/> |Immer dann, wenn Sie sicherstellen möchten, dass e-Mail-Nachrichten von außerhalb Ihrer Organisation kein Identitätswechsel einer der Domänen sind, die in Ihrer Liste der überprüften Domänen oder einer Partnerdomäne definiert sind.  <br/> |
|**Aktionen auswählen** <br/> |Wählen Sie die auszuführende Aktion aus, wenn Office 365 einen Identitätswechsel Versuch für die Benutzer und Domänen erkennt, die Sie der Richtlinie hinzugefügt haben. Sie können unterschiedliche Aktionen für Benutzer und Domänen in derselben Anti-Phishing-Richtlinie auswählen. Diese Aktionen gelten für alle eingehenden e-Mails, die von Office 365 als Identität eines Benutzerkontos oder einer Domäne identifiziert wurden, das unter dem Schutz dieser Anti-Phishing-Richtlinie steht.<br/> **Quarantäne Nachricht** E-Mails werden an Office 365 Quarantine gesendet. Wenn Sie diese Option auswählen, wird die e-Mail nicht an den ursprünglichen Empfänger gesendet.<br/> **Umleiten der Nachricht an eine andere e-Mail-Adresse** E-Mails werden an die von Ihnen angegebene e-Mail-Adresse gesendet. Sie können mehrere e-Mail-Adressen angeben. Wenn Sie diese Option auswählen, wird die e-Mail nicht an den ursprünglichen Empfänger gesendet.<br/> **Nachricht in den Junk-e-Mail-Ordner der Empfänger verschieben** E-Mails werden an den Junk-e-Mail-Ordner der Empfänger gesendet. Wenn Sie diese Option auswählen, wird die e-Mail weiterhin an den ursprünglichen Empfänger gesendet, aber nicht im Posteingang des Empfängers.<br/> **Zustellung der Nachricht und Hinzufügen weiterer Adressen zur Bcc-Zeile** E-Mails werden an den ursprünglichen Empfänger übermittelt. Darüber hinaus werden die von Ihnen identifizierten Benutzer der Bcc-Zeile der Nachricht hinzugefügt, bevor Sie zugestellt wird. Wenn Sie diese Option auswählen, wird die e-Mail weiterhin an den Posteingang des ursprünglichen Empfängers gesendet.<br/> Keine **Aktion anwenden** Die E-Mail wird an den Posteingang des ursprünglichen Empfängers übermittelt. Für die e-Mail-Nachricht werden keine weiteren Aktionen ausgeführt.<br/> **Schützen von Phishing-Tipps** Ermöglicht Phishing-Sicherheitstipps in e-Mails.  <br/> |Wenn Sie eine Aktion für Nachrichten ausführen möchten, die von Office 365 als Identitätswechsel eines Benutzers oder einer Domäne gemäß der Definition in der Richtlinie festgelegt wurden.  <br/> |
|**Aktivieren von Postfach-Intelligence** <br/> |Aktiviert oder deaktiviert Postfach-Intelligence für diese Richtlinie. Sie können nur Postfach-Intelligence für Cloud-basierte Konten aktivieren, also Konten, deren Postfach vollständig in Office 365 gehostet wird.  <br/> |Wenn Sie die Identitätswechsel Ergebnisse für Benutzer auf der Grundlage der einzelnen Absender Zuordnung der einzelnen Benutzer erhöhen möchten. Mailbox Intelligence basiert auf den Personen, von denen Sie e-Mails senden und empfangen. Diese Intelligenz ermöglicht es Office 365, die Identitätswechsel Richtlinie auf Benutzerebene anzupassen, um falsch positive Ergebnisse besser behandeln zu können.  <br/> |
|**Hinzufügen vertrauenswürdiger Absender und Domänen** <br/> |Definiert e-Mail-Adressen und Domänen, die von dieser Richtlinie nicht als Identitätswechsel betrachtet werden. Nachrichten von den Absender-e-Mail-Adressen und Domänen, die Sie als vertrauenswürdige Absender und Domänen hinzufügen, werden nie als Identitätswechsel Angriff klassifiziert. Daher werden die Aktionen und Einstellungen in dieser Richtlinie nicht auf Nachrichten von diesen Absendern und Domänen angewendet.  <br/> |Wenn Benutzer mit Domänen oder Benutzern interagieren, die den Identitätswechsel auslösen, aber als sicher gelten. Wenn ein Partner beispielsweise den gleichen/ähnlichen Anzeigenamen oder Domänennamen hat wie ein in der Liste definierter Benutzer.  <br/> |
|**Angewendet auf** <br/> |Definiert die Empfänger, deren eingehende e-Mail-Nachrichten den Regeln der Richtlinie unterliegen. Sie können Bedingungen und Ausnahmen für die Empfänger erstellen, die der Richtlinie zugeordnet sind.  <br/> Sie können beispielsweise eine globale Richtlinie für Ihre Organisation erstellen, indem Sie die Regel auf alle Empfänger in Ihrer Domäne anwenden.  <br/> Sie können auch Ausnahmeregeln erstellen, beispielsweise eine Regel, die keine e-Mail-Nachrichten für eine bestimmte Empfängergruppe überprüft.  <br/> |Jede Richtlinie muss einer Reihe von Benutzern zugeordnet werden, beispielsweise Benutzern in einer bestimmten Gruppe oder Domäne.  <br/> |
|**Erweiterte Phishing-Schwellenwerte** <br/> |Definiert die Ebene der Einstellungen für die Behandlung von Phishing-Nachrichten.  <br/> **Standard** E-Mails, die als Phishing vermutet werden, werden auf die Standardweise behandelt.  <br/> **Aggressiv** E-Mails, die als Phishing verdächtigt werden, mit hohem oder sehr hohem Vertrauensgrad werden vom System auf die gleiche Art und Weise gehandhabt.  <br/> **Aggressiver** E-Mails, die als Phishing mit einem mittleren, hohen oder sehr hohem Vertrauensgrad vermutet werden, werden auf die gleiche Weise vom System behandelt.  <br/> **Aggressivste** E-Mail-Nachweise, die mit einem niedrigen, mittleren, hohen oder sehr hohem Vertrauensgrad als Phishing vermutet werden, werden auf die gleiche Weise vom System gehandhabt.  <br/> |Wenn Sie bei der Behandlung von potenziell Phishing-Nachrichten in Office 365 aggressiver sein möchten. Beispielsweise haben Nachrichten mit einer sehr hohen Wahrscheinlichkeit des Phishing-Angriffs die aggressivsten Aktionen, während Nachrichten mit niedriger Wahrscheinlichkeit weniger aggressive Aktionen ausführen. Diese Einstellung wirkt sich auch auf andere Teile des Filtersystems aus, die Signale zusammenfassen. Die Möglichkeit, gute Nachrichten zu bewegen, erhöht sich, wenn die Ebene der Einstellungen zunimmt.  <br/>|
   
## <a name="learn-about-anti-phishing-policy-options"></a>Informationen zu Optionen für die Anti-Phishing-Richtlinie 

Wenn Sie Ihr AntiPhishing einrichten oder bearbeiten, können Sie wie in der folgenden Tabelle beschrieben verschiedene Optionen auswählen: 

|**Diese Einstellung**|**Funktion**|**Verwenden Sie, wenn Sie Folgendes möchten:**|
|:-----|:-----|:-----|
|**Angewendet auf** <br/> |Definiert die Empfänger, deren eingehende e-Mail-Nachrichten den Regeln der Richtlinie unterliegen. Sie können Bedingungen und Ausnahmen für die Empfänger erstellen, die der Richtlinie zugeordnet sind.  <br/> Sie können beispielsweise eine globale Richtlinie für Ihre Organisation erstellen, indem Sie die Regel auf alle Empfänger in Ihrer Domäne anwenden.  <br/> Sie können auch Ausnahmeregeln erstellen, beispielsweise eine Regel, die keine e-Mail-Nachrichten für eine bestimmte Empfängergruppe überprüft.  <br/> |Jede Richtlinie muss einer Reihe von Benutzern zugeordnet werden, beispielsweise Benutzern in einer bestimmten Gruppe oder Domäne.  <br/> | 
|**Aktionen auswählen** <br/> |Wählen Sie die Aktion aus, die ausgeführt werden soll, wenn Office 365 einen "Intra-org"-oder "External-org"-Spoofing-Versuch für Ihre Benutzer erkennt. Diese Aktionen gelten für alle eingehenden e-Mails, die von Office 365 als Spoofing-Versuch für Benutzer identifiziert wurden, die unter dem Schutz dieser Anti-Phishing-Richtlinie stehen.<br/> **Quarantäne Nachricht** E-Mails werden an Office 365 Quarantine gesendet. Wenn Sie diese Option auswählen, wird die e-Mail nicht an den ursprünglichen Empfänger gesendet.<br/> **Nachricht in den Junk-e-Mail-Ordner der Empfänger verschieben** E-Mails werden an den Junk-e-Mail-Ordner der Empfänger gesendet. Wenn Sie diese Option auswählen, wird die e-Mail weiterhin an den ursprünglichen Empfänger gesendet, aber nicht im Posteingang des Empfängers.<br/> Keine **Aktion anwenden** Die E-Mail wird an den Posteingang des ursprünglichen Empfängers übermittelt. Für die e-Mail-Nachricht werden keine weiteren Aktionen ausgeführt.<br/> |Wenn Sie eine Aktion für Nachrichten ausführen möchten, die von Office 365 als Spoofing-Versuch interner oder externer Domänen gemäß der Definition in der Richtlinie festgelegt wurden.  <br/>|

Nachdem Ihre Organisation Anti-Phishing-Richtlinien oder ATP-AntiPhishing-Richtlinien eingerichtet hat, können Sie sehen, wie der Dienst funktioniert, indem Sie [Berichte zu Advanced Threat Protection anzeigen](view-reports-for-atp.md).
  
## <a name="example-anti-phishing-policy-to-protect-a-user-and-a-domain"></a>Beispiel: Anti-Phishing-Richtlinie zum Schutz von Benutzern und Domänen

In diesem Beispiel wird eine Richtlinie mit dem Namen "Domain and CEO" eingerichtet, die sowohl Benutzer-als auch Domänen Schutz vor Identitätswechsel bereitstellt und dann die Richtlinie auf alle `contoso.com`e-Mails anwendet, die von Benutzern innerhalb der Domäne empfangen werden. Der Sicherheitsadministrator hat festgestellt, dass die Richtlinie diese geschäftlichen Anforderungen erfüllen muss:
  
- Die Richtlinie muss Schutz für das e-Mail-Konto des CEO und die gesamte Domäne bieten.
    
- Nachrichten, die als Identitätswechsel für das Benutzerkonto des CEO festgelegt wurden, müssen an die e-Mail-Adresse des Sicherheitsadministrators umgeleitet werden.
    
- Nachrichten, die als Identitätswechsel Versuche für die Domäne bestimmt sind, sind geringer und sollten zur späteren Überprüfungen isoliert werden.
    
Der Sicherheitsadministrator bei Contoso kann Werte wie den folgenden verwenden, um eine Anti-Phishing-Richtlinie zu erstellen, die diese Anforderungen erfüllt.
  
|||
|:-----|:-----|
|**Einstellung oder Option** <br/> |**Beispiel** <br/> |
|Name  <br/> |Domäne und CEO  <br/> |
|Description  <br/> |Stellen Sie sicher, dass der CEO und unsere Domäne nicht angenommen werden.  <br/> |
|Hinzufügen von Benutzern zu schützen  <br/> |Die e-Mail-Adresse des CEO mindestens.  <br/> |
|Hinzufügen von Domänen zum Schutz  <br/> |Die Organisationsdomäne, die das Office des CEO enthält.  <br/> |
|Aktionen auswählen  <br/> |Wenn e-Mails von einem imitierten Benutzer gesendet werden: Wählen Sie **Nachricht an eine andere e-Mail-Adresse umleiten** aus, und geben Sie dann die e `securityadmin@contoso.com`-Mail-Adresse des Sicherheitsadministrators ein, beispielsweise.  <br/> Wenn e-Mails von einer angenommenen Domäne gesendet werden: Wählen Sie **Quarantäne Nachricht**aus.  <br/> |
|Postfach-Intelligence  <br/> |Standardmäßig wird die Post Fach Intelligenz ausgewählt, wenn Sie eine neue Richtlinie zum Schutz vor Phishing erstellen. BeLassen Sie **** diese Einstellung für optimale Ergebnisse.<br/> |
|Hinzufügen vertrauenswürdiger Absender und Domänen  <br/> |Definieren Sie für dieses Beispiel keine Außerkraftsetzungen.  <br/> |
|Angewendet auf  <br/> |Wählen Sie **die Empfängerdomäne ist**aus. Wählen Sie unter **einer der folgenden**Option **auswählen**aus. Wählen Sie **+ Hinzufügen**aus. Aktivieren Sie das Kontrollkästchen neben dem Namen der Domäne, beispielsweise `contoso.com`in der Liste, und wählen Sie dann **Hinzufügen**aus. Wählen Sie **Fertig**aus.<br/> |
   
## <a name="delete-an-anti-phishing-or-atp-anti-phishing-policy"></a>Löschen einer Anti-Phishing-oder ATP-AntiPhishing-Richtlinie

Sie können benutzerdefinierte Richtlinien, die Sie mithilfe des Security &amp; Compliance Center erstellt haben, löschen. Sie können die Standardrichtlinie für Ihre Organisation nicht löschen. Wir empfehlen die Verwendung des &amp; Security Compliance Center, um Ihre ATP-Richtlinien zu überarbeiten oder zu bearbeiten.
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an. 
    
2. Wählen Sie im linken Navigationsbereich unter **Bedrohungs Verwaltung**die Option **Richtlinie**aus.
    
3. Wählen Sie auf der Seite **Richtlinie** **Anti-Phishing** oder **ATP-Phishing**aus.
    
4. Wählen Sie auf der Seite **Anti-Phishing** -oder **ATP-Phishing** den Richtliniennamen aus der Liste aus.

5. Klicken Sie auf der angezeigten Seite auf **Richtlinie löschen**. Sie können bis zu 30 Minuten dauern, bis Ihre Änderungen auf alle Office 365-Rechenzentren verteilt sind.
    

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie die Richtlinien für den Phishingschutz eingerichtet haben, können Sie sehen, wie Ihre Bedrohungsschutz Funktionen für Ihre Organisation funktionieren, indem Sie Berichte anzeigen. Weitere Informationen finden Sie in den folgenden Ressourcen:
- [Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md) oder [Anzeigen von e-Mail-Sicherheitsberichten](view-email-security-reports.md)
- [Verwenden des Explorers (auch als Bedrohungs-Explorer bezeichnet)](use-explorer-in-security-and-compliance.md)

Bleiben Sie auf dem neuesten Stand der neuen Features für ATP. Besuchen Sie die [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) , und erfahren Sie mehr über [neue Features, die ATP hinzugefügt werden](office-365-atp.md#new-features-in-office-365-atp).
 