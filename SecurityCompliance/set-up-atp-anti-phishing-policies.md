---
title: Einrichten von Richtlinien für Office 365 ATP Anti-phishing
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578
description: ATP Phishing-Schutz, die Teil von Office 365 erweiterte Threat Protection kann Ihre Organisation vor böswilligen Identitätswechsel-basierte Phishingangriffe und andere Phishingangriffen schützen. Wenn Sie ein Office 365 Enterprise-global oder Sicherheitsadministrator sind, können Sie ATP Anti-Phishing Richtlinien einrichten. Phishing Angriffe kommen in einer Vielzahl von Formularen von Waren-basierte Angriffe auf zielgerichteten Spear Phishing oder Whaling. Mit der wachsenden Komplexität ist es schwierig, auch eine geschult Auge um einige dieser komplexen Angriffe zu identifizieren. Zum Glück kann Office 365 erweiterte Threat Protection helfen. Sie können eine ATP Anti-Phishing-Richtlinie einrichten, um sicherzustellen, dass Ihre Organisation vor solchen Angriffen geschützt ist.
ms.openlocfilehash: 73bcc148f3bd4f0700020c147cfa9cbb2734bc34
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529768"
---
# <a name="set-up-office-365-atp-anti-phishing-policies"></a>Einrichten von Richtlinien für Office 365 ATP Anti-phishing

[ATP Phishing - Schutz](atp-anti-phishing.md) , Bestandteil des [Office 365 erweiterte Schutz](office-365-atp.md), können Ihrer Organisation vor böswilligen Identitätswechsel-basierte Phishingangriffe und andere Phishingangriffen schützen. Wenn Sie ein Office 365 Enterprise-global oder Sicherheitsadministrator sind, können Sie ATP Anti-Phishing Richtlinien einrichten. Phishing Angriffe kommen in einer Vielzahl von Formularen von Waren-basierte Angriffe auf zielgerichteten Spear Phishing oder Whaling. Mit der wachsenden Komplexität ist es schwierig, auch eine geschult Auge um einige dieser komplexen Angriffe zu identifizieren. Zum Glück kann Office 365 erweiterte Threat Protection helfen. Sie können eine ATP Anti-Phishing-Richtlinie einrichten, um sicherzustellen, dass Ihre Organisation vor solchen Angriffen geschützt ist.
  
> [!NOTE]
> ATP Anti-Phishing ist nur verfügbar, erweiterte Threat Protection, mit Office 365 Enterprise E5 verfügbar. Wenn in Ihrer Organisation ein weiteres Abonnement von Office 365 Enterprise verwendet wird, kann der erweiterte Schutz als Add-on erworben werden. (Als ein globaler Administrator, in der Office 365-Verwaltungskonsole, wählen Sie **Abrechnung** \> **Hinzufügen Abonnements**.) Weitere Informationen zu den Optionen zum Plan finden Sie unter [Vergleich alle Office 365 für Unternehmen plant](https://go.microsoft.com/fwlink/?linkid=844053). Stellen Sie sicher, dass Ihre Organisation die neueste Version von Office 365 ProPlus von Windows verwenden, ATP Phishing-Schutz vollständig zu nutzen. 
  
Was ist zu tun:
  
1. [Überprüfen Sie die erforderlichen Komponenten](set-up-atp-anti-phishing-policies.md#phishprereq)
    
2. [Erfahren Sie mehr über ATP Anti-Phishing Richtlinienoptionen](set-up-atp-anti-phishing-policies.md#phishpolicyoptions)
    
3. [Richten Sie eine ATP Anti-Phishing-Richtlinie](set-up-atp-anti-phishing-policies.md#addphishpolicy)
    
## <a name="review-the-prerequisites"></a>Überprüfen Sie die erforderlichen Komponenten

- Stellen Sie sicher, dass Sie Mitglied der Gruppe der **Administratoren im Unternehmen** oder **Sicherheit-Admins** Rolle sind. 
    
- [Informieren Sie sich über ATP Anti-Phishing Richtlinienoptionen](set-up-atp-anti-phishing-policies.md#phishpolicyoptions) (in diesem Artikel). 
    
- Sie werden möglicherweise mehrere ATP Anti-Phishing-Richtlinien für Ihre Organisation einrichten. Office 365 setzt diese Richtlinien in der Reihenfolge, die sie auf der Seite **ATP Anti-Phishing** in das Wertpapier aufgeführt sind &amp; Compliance Center. Nachdem Sie die Richtlinienoptionen überprüft haben, führen Sie etwas Zeit, um zu bestimmen, wie viele Richtlinien, die Sie benötigen und die Priorität für die einzelnen. 
    
- Planen Sie etwa 5-15 Minuten verbringen zum Einrichten Ihrer ersten ATP Anti-Phishing-Richtlinie.
    
- Können Sie bis zu 30 Minuten für die neue oder aktualisierte Richtlinie in allen Office 365-Rechenzentren verteilen.
    
## <a name="set-up-an-atp-anti-phishing-policy"></a>Richten Sie eine ATP Anti-Phishing-Richtlinie
<a name="addphishpolicy"> </a>

Sie hinzufügen, bearbeiten und Löschen von ATP Anti-Phishing-Richtlinien in der Office 365-Sicherheit &amp; Compliance Center.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. In der Office 365-Sicherheit &amp; Compliance Center, wählen Sie im linken Navigationsbereich unter **Threat Management** **Policy**.
    
3. Wählen Sie auf der Seite **Richtlinie** **ATP Anti-Phishing**aus.
    
4. Führen Sie auf der Seite **Anti-Phishing** eine der folgenden Aktionen aus: 
    
  - Zum Hinzufügen eine neue Richtlinie wählen Sie **+ Erstellen**.
    
  - Um eine vorhandene Richtlinie zu bearbeiten, wählen Sie den Namen der Richtlinie aus der Liste auf der Seite **Anti-Phishing** angezeigt. Wählen Sie auf der angezeigten Seite **Richtlinie bearbeiten**.
    
    Ein Assistent wird gestartet, die Sie schrittweise durch die Anti-Phishing-Richtlinie definieren.
    
5. Geben Sie Name, Beschreibung und Einstellungen für die Richtlinie ein. Einzelheiten finden Sie unter [erfahren Sie mehr über ATP Anti-Phishing Richtlinienoptionen](set-up-atp-anti-phishing-policies.md#phishpolicyoptions) . 
    
6. Einmal Sie Ihre Einstellungen überprüft haben, wählen Sie **diese Richtlinie erstellen** oder **Speichern** nach Bedarf. 
    
## <a name="learn-about-atp-anti-phishing-policy-options"></a>Erfahren Sie mehr über ATP Anti-Phishing Richtlinienoptionen
<a name="phishpolicyoptions"> </a>

Als Sie einrichten oder Bearbeiten Ihrer ATP Anti-Phishing-Richtlinien können Sie mehrere Optionen auswählen wie in der folgenden Tabelle beschrieben:
  
|**Diese Einstellung**|**Funktion**|**Wird verwendet, wenn Sie möchten:**|
|:-----|:-----|:-----|
|**Hinzufügen von Benutzern zu schützen** <br/> |Definiert, welche e-Mail-Adressen durch die Richtlinie geschützt werden. Sie können bis zu 20 interne und externe Adressen hinzufügen, die Sie Identitätswechsel schützen möchten.  <br/> |Wenn Sie sicherstellen, dass e-Mails von außerhalb Ihrer Organisation einen Identitätswechsel eines der Benutzer in der Liste der Benutzer ist nicht geschützten möchten. Beispiele für Benutzer aus, die Sie möglicherweise schützen möchten sind allgemeine Führungskräfte, geschäftlichen Besitzer, externe Vorstandsmitglieder usw..<br/> Diese Liste mit Benutzern von geschützten unterscheidet sich von der Liste der Personen, für die die Richtlinie, oder vielmehr gilt, für die die Richtlinie erzwungen wird. Definieren Sie die Liste im Abschnitt **für** die Richtlinienoptionen betrifft.<br/> Angenommen, Sie Mary Smith hinzufügen \<marys@contoso.com\> als Benutzer zu schützen, wenden Sie die Richtlinie für die Gruppe "alle Benutzer". Dadurch wird sichergestellt, dass eine e-Mail-Nachrichten, die scheinbar impersonate "Mary Smith" gesendet, um einen Benutzer in der Gruppe "Alle Benutzer" durch die Richtlinie auf ausgeführt würde.<br/> |
|**Hinzufügen von Domänen zu schützenden Komponenten** <br/> |Ermöglicht Ihnen, welche Domänen sollen Identitätswechsel zu schützen. Sie können angeben, dass die Richtlinie alle Ihre benutzerdefinierten Domänen, eine durch Trennzeichen getrennte Liste der Domänen oder eine Kombination aus beidem enthält. Wenn Sie **automatisch umfassen Domänen, die ich besitzen**, und Sie später einer Domäne zu Office 365-Organisation hinzufügen, wird diese Anti-Phishing-Richtlinie für die neue Domäne sein.<br/> |Wenn Sie möchten sicherstellen, dass e-Mails von außerhalb Ihrer Organisation einen Identitätswechsel eines Domänen in Ihrer Liste der überprüften Domänen oder von einer Partnerdomäne definiert ist nicht.  <br/> |
|**Wählen Sie Aktionen** <br/> |Wählen Sie die Aktion an, die beim Office 365 erkennt Versuch Identitätswechsel für den Benutzer und Domänen, die Sie die Richtlinie hinzugefügt. Sie können unterschiedliche Aktionen für Benutzer und Domänen in der gleichen Anti-Phishing-Richtlinie auswählen. Diese Aktionen gelten für alle eingehenden e-Mails, der als annehmen der Identität eines Benutzerkontos von Office 365 identifiziert wurde oder Domäne, unter dem diese Richtlinie Anti-Phishing-Schutz ist.<br/> **In Quarantäne verschobene Nachricht** E-Mails werden in Office 365 Quarantäne versendet. Wenn Sie diese Option auswählen, wird die e-Mail nicht an den ursprünglichen Empfänger gesendet.<br/> **Umleiten der Nachricht an eine andere e-Mail-Adresse** E-Mail wird an die e-Mail-Adresse gesendet, die Sie angeben. Sie können mehrere e-Mail-Adressen angeben. Wenn Sie diese Option auswählen, wird die e-Mail nicht an den ursprünglichen Empfänger gesendet.<br/> **Verschieben der Nachricht an die Empfänger Junk-e-Mail-Ordner** E-Mail wird an die Empfänger Junk-e-Mail-Ordner gesendet. Wenn Sie diese Option auswählen, die e-Mail wird weiterhin an den ursprünglichen Empfänger gesendet, aber wird nicht in den Posteingang des Empfängers platziert.<br/> **Die Nachricht zu übermitteln und andere Adressen der Bcc-Zeile hinzufügen** E-Mails werden an den ursprünglichen Empfänger übermittelt. Darüber hinaus werden der Benutzer, die Sie identifizieren hinzugefügt werden die Bcc-Zeile der Nachricht vor der Lieferung ist. Wenn Sie diese Option auswählen, wird die e-Mail noch an den ursprünglichen Posteingang des Empfängers gesendet.<br/> **Gelten nicht für alle Aktionen** E-Mail wird an den ursprünglichen Posteingang des Empfängers übermittelt werden. Klicken Sie auf der e-Mail-Nachricht wird keine andere Aktion ausgeführt werden.<br/> **Schalten Sie Phishing-Schutz-Tipps** Anti-Phishing Safety Tipps in e-Mail-aktiviert.  <br/> |Wenn Sie eine Aktion auf Nachrichten angewendet werden, die Office 365 festgestellt, dass ein Identitätswechsel eines Benutzers oder einer Domäne als der in der Richtlinie definierten möchten.  <br/> |
|**Postfach Intelligence aktivieren** <br/> |Aktiviert oder deaktiviert Postfachs Intelligence für diese Richtlinie. Sie können nur Postfach Intelligence für cloudbasierten Konten, d. h., Konten aktivieren, deren Postfach vollständig in Office 365 gehostet wird.  <br/> |Wenn Sie Identitätswechsel Ergebnisse für Benutzer, die basierend auf den einzelnen Absender Wegweiser für jeden Benutzer verbessern möchten. Postfach Intelligence basiert auf Personen senden und Empfangen von e-Mails aus. Diese Intelligence ermöglicht Office 365 ein, um die Richtlinie Identitätswechsel auf der Benutzerebene anpassen, um besser falsch positive Ergebnisse zu behandeln.  <br/> |
|**Hinzufügen von vertrauenswürdigen Absender und Domänen** <br/> |Definiert, e-Mail-Adressen und Domänen, die durch diese Richtlinie nicht Identitätswechsel berücksichtigt werden. Nachrichten von den Absender e-Mail-Adressen und Domänen, die Sie als vertrauenswürdige Absender hinzufügen und Domänen werden nicht als Angriff Identitätswechsel-basierte jemals klassifiziert werden. Daher wird nicht die Aktionen und Einstellungen in dieser Richtlinie auf Nachrichten aus diesen Absender und Domänen angewendet werden.  <br/> |Wenn Benutzer interagieren mit Domänen oder Benutzern, die Identitätswechsel auslösen, jedoch werden als sicher angesehen. Beispielsweise wenn ein Partner angezeigt gleichen/ähnliche oder Domänennamen als Benutzer in der Liste definiert.  <br/> |
|**Angewendet auf** <br/> |Definiert die Empfänger, deren eingehende e-Mail-Nachrichten können die Regeln der Richtlinie werden. Sie können die Bedingungen und Ausnahmen für die Empfänger der Richtlinie zugeordnet erstellen.  <br/> Beispielsweise können Sie eine globale Richtlinie für Ihre Organisation erstellen, indem Sie die Regel an alle Empfänger in Ihrer Domäne anwenden.  <br/> Sie können auch Regeln, wie eine Regel erstellen, die keine e-Mail-Nachrichten für eine bestimmte Gruppe von Empfängern überprüft wird.  <br/> |Jede Richtlinie muss eine Gruppe von Benutzern, beispielsweise Benutzer in einer bestimmten Gruppe oder Domäne zugeordnet werden.  <br/> |
   
Nach ATP Anti-Phishing Richtlinien der Organisation eingerichtet hat, können Sie sehen, wie der Dienst durch [Anzeigen von Berichten für erweiterte Threat Protection](view-reports-for-atp.md)funktionsfähig ist.
  
## <a name="example-anti-phishing-policy-to-protect-a-user-and-a-domain"></a>Beispiel: Anti-Phishing-Richtlinie zum Schutz von einem Benutzer und einer Domäne
<a name="phishpolicyoptions"> </a>

In diesem Beispiel richtet eine Richtlinie namens "Domäne und CEO", die enthält Benutzer und Domäne Schutz vor Identitätswechsel und anschließend die Richtlinie auf alle e-Mails, die vom Benutzer in der Domäne "contoso.com" angewendet. Der Sicherheitsadministrator hat festgestellt, dass die Richtlinie dieser geschäftlichen Anforderungen erfüllt sein müssen:
  
- Die Richtlinie für den Schutz für des CEO muss e-Mail-Konto und die gesamte Domäne.
    
- Nachrichten, die zum Identitätswechsel Zugriffsversuche gegen die CEO Benutzerkonto werden bestimmt werden müssen, zu der Sicherheitsadministrator e-Mail-Adresse weitergeleitet werden.
    
- Nachrichten, die Identitätswechsel Versuche für die Domäne sind weniger dringende sind und für die spätere Verwendung isoliert werden sollten.
    
Der Sicherheitsadministrator bei Contoso können Werte wie folgt, um eine Anti-Phishing-Richtlinie zu erstellen, die diese Anforderungen erfüllt.
  
|||
|:-----|:-----|
|**Option oder Einstellung** <br/> |**Beispiel** <br/> |
|Name  <br/> |Domäne und CEO  <br/> |
|Beschreibung  <br/> |Stellen Sie sicher, dass CEO und unsere Domäne nicht imitiert werden.  <br/> |
|Hinzufügen von Benutzern zu schützen  <br/> |E-Mail-Adresse mindestens die CEO.  <br/> |
|Hinzufügen von Domänen zu schützenden Komponenten  <br/> |Die Organisationseinheit Domäne, die im Büro des CEO enthält.  <br/> |
|Wählen Sie Aktionen  <br/> |Wenn Sie e-Mails von einem angenommener Benutzer gesendet wird: Wählen Sie **Umleiten der Nachricht an eine andere e-Mail-Adresse** , und geben Sie die e-Mail-Adresse des Sicherheitsadministrators, beispielsweise securityadmin@contoso.com.  <br/> Wenn Sie e-Mails von einer angenommener Domäne gesendet wird: Wählen Sie **in Quarantäne verschobene Nachricht**.  <br/> |
|Postfach intelligence  <br/> |Postfach Intelligence ist standardmäßig aktiviert, bei der Erstellung einer neuen Anti-Phishing-Richtlinie. Lassen Sie diese Einstellung **für** die besten Ergebnisse erzielen.<br/> |
|Hinzufügen von vertrauenswürdigen Absender und Domänen  <br/> |In diesem Beispiel definieren Sie eine beliebige überschreibt.  <br/> |
|Angewendet auf  <br/> |Wählen Sie **die Domäne des Empfängers ist**. Wählen Sie unter **diese** **auswählen**. Wählen Sie **+ Hinzufügen**. Aktivieren Sie das Kontrollkästchen neben dem Namen der Domäne, z. B. "contoso.com" in der Liste und dann auf **Hinzufügen**. Wählen Sie **Fertig**.<br/> |
   
## <a name="delete-an-atp-anti-phishing-policy"></a>Löschen einer ATP Anti-Phishing-Richtlinie
<a name="phishpolicyoptions"> </a>

Sie können hinzufügen und Bearbeiten von Richtlinien in das Wertpapier &amp; Compliance Center. Es wird empfohlen, die Sicherheit &amp; Compliance Center zu überprüfen oder eine beliebige ATP Richtlinie bearbeiten.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Wählen Sie im linken Navigationsbereich, klicken Sie unter **Threat Management** **Richtlinie**aus.
    
3. Wählen Sie auf der Seite **Richtlinie** **ATP Anti-Phishing**aus.
    
4. Wählen Sie auf der Seite **Anti-Phishing** den Namen der Richtlinie aus der Liste auf der Seite **Anti-Phishing** angezeigt. Wählen Sie auf der angezeigten Seite **Richtlinie zu löschen**. Können Sie bis zu 30 Minuten, damit die Änderungen in allen Office 365-Rechenzentren verteilen.
    
## <a name="related-topics"></a>Verwandte Themen
<a name="phishpolicyoptions"> </a>

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Phishing-Schutz in Office 365](anti-phishing-protection.md)
  
[ATP Anti-Phishing-Funktionen in Office 365](atp-anti-phishing.md)
  
[ATP sichere Links in Office 365](atp-safe-links.md)
  
[Einrichten von ATP sichere Links Richtlinien in Office 365](set-up-atp-safe-links-policies.md)
  
[ATP sichere Anlagen in Office 365](atp-safe-attachments.md)
  
[Einrichten von Richtlinien für ATP sichere Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)
  
[Anzeigen der Berichte zu Advanced Threat Protection](view-reports-for-atp.md)
  

