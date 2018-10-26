---
title: Konfigurieren der Verbindungsfilterrichtlinie
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
description: Um sicherzustellen, dass von Personen, denen, die Sie vertrauen, gesendete e-Mail nicht gesperrt hat, können Sie der verbindungsfilterrichtlinie verwenden, um eine Liste, auch bekannt als eine Liste sicherer Absender verwendet werden, der IP-Adressen zu erstellen, denen Sie vertrauen. Sie können auch eine Liste der blockierten Absender erstellen.
ms.openlocfilehash: 2f8ec3d01de4358d7394c68d0efae9222db08282
ms.sourcegitcommit: a07b91723bae9ecee2cb092bfbc5b208b30b11a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2018
ms.locfileid: "25793560"
---
# <a name="configure-the-connection-filter-policy"></a>Konfigurieren der Verbindungsfilterrichtlinie
 
Die meisten von uns haben Freunde und Geschäftspartnern, denen wir vertrauen. Es kann ärgerlich sein, E-Mail dieser Absender in Ihrem Junk-E-Mail-Ordner zu finden oder festzustellen, dass sie vom Spamfilter gänzlich blockiert wurden. Wenn Sie sicherstellen möchten, dass von diesen vertrauenswürdigen Absendern gesendete E-Mail nicht blockiert wird, können Sie die Verbindungsfilterrichtlinie zum Erstellen einer Zulassungsliste (bzw. „Liste sicherer Absender") mit vertrauenswürdigen IP-Adressen nutzen. Sie können auch eine Liste blockierter Absender mit IP-Adressen (zumeist von Spammern) erstellen, von denen Sie nie wieder E-Mail-Nachrichten empfangen möchten.
  
 Weitere Antispameinstellungen, die für die gesamte Organisation gelten, finden Sie unter [Sicherstellen, dass eine Nachricht nicht als Spam gekennzeichnet wird](https://go.microsoft.com/fwlink/p/?LinkId=534224) oder [Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zum Verhindern von falsch negativen Ergebnissen](https://go.microsoft.com/fwlink/p/?LinkId=534225). Diese sind hilfreich, wenn Sie über die Steuerung auf Administratorebene verfügen und wenn Sie falsch positive Ergebnisse oder falsch negative Ergebnisse vermeiden möchten.
  
Im folgenden Video wird die Vorgehensweise zur Konfiguration der Verbindungsfilterrichtlinie gezeigt:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

- Geschätzte Zeit zur Durchführung: 15 Minuten
    
- Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "AntiSpam" im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Um die IP-Adresse des Absenders abzurufen, deren Nachrichten, die Sie zulassen oder blockieren möchten, können Sie die Internet-Kopfzeile der Nachricht überprüfen. Suchen Sie nach der Kopfzeile CIP gemäß [Anti-Spam Message Headers](anti-spam-message-headers.md). Informationen zum Anzeigen einer Nachrichtenkopfzeile in verschiedenen e-Mail-Clients finden Sie unter [Message Headers Analyzer](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
    
- E-Mails, die von einer IP-Adresse aus der IP-Sperrliste gesendet werden, werden abgelehnt, nicht als Spam gekennzeichnet, und es werden keine weiteren Filter angewendet.
    
- Das folgende Verfahren der Connection Filter kann auch über remote-PowerShell erfolgen. Verwenden Sie das Cmdlet [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) , um Ihre Einstellungen, und das [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) zum Bearbeiten Ihrer filtereinstellungen Richtlinie Verbindung prüfen. Weitere Informationen zu Windows PowerShell verwenden, um die Verbindung mit Exchange Online Protection finden Sie unter [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). So verwenden Sie Windows PowerShell für die Verbindung zu Exchange Online finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>Bearbeiten der Standardrichtlinie für Verbindungsfilter mithilfe der Exchange-Verwaltungskonsole
<a name="sectionSection1"> </a>

Durch Bearbeiten der Verbindungsfilterrichtlinie in der Exchange-Verwaltungskonsole können Sie eine IP-Zulassungs- bzw. -Sperrliste erstellen. Die Einstellungen für die Verbindungsfilterrichtlinie werden nur auf eingehende Nachrichten angewendet.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Verbindungsfilter**, und doppelklicken Sie dann auf die Standardrichtlinie.
    
2. Klicken Sie auf die Menüoption **Verbindungsfilterung**, und erstellen Sie dann die gewünschten Listen: eine IP-Zulassungsliste, eine IP-Sperrliste oder beides. 
    
    Klicken Sie zum Erstellen dieser Listen auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif). Geben Sie im folgenden Dialogfeld die IP-Adressen oder den IP-Adressbereich an, und klicken Sie dann auf **OK**. Wiederholen Sie diesen Vorgang, um weitere Adressen hinzuzufügen. (Sie können IP-Adressen auch bearbeiten oder entfernen, nachdem sie hinzugefügt wurden.)
    
    > [!NOTE]
    >  Wenn Sie eine IP-Adresse beiden Listen hinzufügen, wird von dieser IP-Adresse gesendete e-Mail zulässig ist. 

    Geben Sie IPv4-IP-Adressen an, in dem Format sind, wobei Nnn eine Zahl zwischen 0 und 255 ist. Sie können auch Classless Inter-Domain Routing (CIDR) Bereiche in der Format-nnn.nnn.nnn.nnn/rr angeben, wobei rr eine Zahl von 24 bis 32 ist. Wenn Sie Bereiche außerhalb des Bereichs 24 bis 32 angeben, finden Sie unter [zusätzliche Überlegungen beim Konfigurieren der IP-Zulassungsliste Listen](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). 

    Sie können maximal 1273 Einträge angeben, wobei ein Eintrag einer einzelnen IP-Adresse oder einem CIDR Bereich von IP-Adressen von/24 bis / 32 ist. > Wenn Sie TLS-verschlüsselte Nachrichten senden, werden IPv6-Adressen und -Adressbereiche nicht unterstützt. 
  
3. Wählen Sie optional das Kontrollkästchen **sicheren Liste aktivieren** , um zu verhindern, dass e-Mail-Nachrichten von bestimmten bekannte Absender fehlt. Auf welche Weise? Microsoft abonniert Drittanbieter-Quellen der sicheren Absender enthalten. Mit dieser Liste sicherer bedeutet, dass diese vertrauenswürdige Absender versehentlich als Spam gekennzeichnet werden nicht. Es wird empfohlen, diese Option, da es sollte reduzieren Sie die Anzahl der falsch positive Ergebnisse (unbedenkliche e-Mails, die als Spam klassifiziert ist), die Sie erhalten. 
    
4. Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Standardrichtlinieneinstellungen angezeigt.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>Weitere Überlegungen zum Konfigurieren von Listen zugelassener IP-Adressen
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

Folgende Überlegungen sollten Sie anstellen, wenn Sie eine Liste zugelassener IP-Adressen konfigurieren möchten.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>Angeben eines CIDR-Bereichs, der außerhalb des empfohlenen Bereichs liegt

Um eine CIDR-IP-Adressbereich aus /1 an /23 angeben, müssen Sie erstellen eine e-Mail-Fluss-Regel, die für den IP-Adressbereich ausgeführt wird, die die Spam Confidence Level (SCL) festlegt **Umgehung Spamfilterung** (d. h., alle Nachrichten, die von innerhalb dieser IP-Adressbereich werden Legen Sie auf "nicht spam") und keine zusätzliche Filterung vom Dienst ausgeführt wird). Wenn alle diese IP-Adressen auf angezeigt werden Microsofts proprietäre Block enthält oder auf einem der unsere Drittanbieter-Block enthält, werden diese Nachrichten weiterhin blockiert. Es wird daher dringend empfohlen, für die Verwendung von/24 bis / zu /32 IP-Adressbereich. 
  
Um diese e-Mail-Flussregel zu erstellen, führen Sie die folgenden Schritte aus.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Wählen Sie unter **Diese Regel wird ausgeführt, wenn** die Option **Absender**, und wählen Sie dann **IP-Adresse ist in keinem dieser Bereiche oder stimmt mit keinem Bereich völlig überein**.
    
5. In der **IP-Adressen angeben**, geben Sie den IP-Adressbereich aus, klicken Sie auf **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif), und klicken Sie dann auf **ok**.
    
6. Legen Sie unter **Gehen Sie folgendermaßen vor:** die Aktion fest, indem Sie erst **Nachrichteneigenschaften ändern** wählen und dann die **SCL-Bewertung (Spam Confidence Level) festlegen**. Wählen Sie im Feld **SCL angeben** die Option **Spamfilter umgehen**, und klicken Sie auf **OK**.
    
7. Wenn Sie möchten, können Sie, Auswahl der Überwachungsregel, testen Sie die Regel, aktivieren die Regel während eines bestimmten Zeitraums und andere Auswahl. Es wird empfohlen, testen die Regel für einen bestimmten Zeitraum, bevor Sie es erzwingen. [Regeln für die Verfahren für die Nachrichtenübermittlung in Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) enthält weitere Informationen zu diesen Auswahlmöglichkeiten. 
    
8. Klicken Sie auf **Speichern** , um die Regel zu speichern. Die Regel in der Liste der Regeln wird angezeigt. 
    
Nachdem Sie erstellen und der Regel erzwingen, umgeht der Dienst Spamfilterung für den IP-Adressbereich, den Sie angegeben haben.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>Bereichsfestlegung für Ausnahmen von einer Liste der zugelassenen IP-Adressen einer bestimmten Domäne

Sie sollten die IP-Adresse (oder IP-Adressbereiche) für alle Ihre Domänen, die Sie als sicher einschätzen, der Liste der zugelassenen IP-Adressen hinzufügen. Wenn Sie jedoch nicht wünschen, dass der Eintrag in dieser IP-Adressliste für alle Domänen gilt, erstellen Sie eine Transportregel, von der bestimmte Domänen ausgenommen sind. 
  
Nehmen wir an, Sie haben drei Domänen: ContosoA.com, ContosoB.com und ContosoC.com. Sie wollen die IP-Adresse (zur Vereinfachung verwenden wir 1.2.3.4) hinzufügen und die Filterung nur für die Domäne ContosoB.com überspringen. Dazu müssten Sie eine IP-Zulassungsliste für 1.2.3.4 erstellen, mit der die SCL-Bewertung (Spam Confidence Level) für alle Domänen auf -1 gesetzt wird (was bedeutet, dass sie als "Kein Spam" klassifiziert wird). Sie können dann eine Transportregel erstellen, mit der die SCL-Bewertung für alle Domänen außer ContosoB.com auf 0 gesetzt wird. Das bewirkt, dass die Nachricht für alle Domänen, die der IP-Adresse zugeordnet sind, erneut überprüft wird - mit Ausnahme von ContosoB.com, weil diese Domäne als Ausnahme in der Regel definiert ist. ContosoB.com hat weiterhin eine SCL-Bewertung von -1, was das Überspringen der Filterung bedeutet, während ContosoA.com und ContosoC.com SCL-Bewertungen von 0 haben, was bedeutet, dass sie durch den Inhaltsfilter erneut überprüft werden.
  
Führen Sie dazu die folgenden Schritte aus:
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Wählen Sie unter **Diese Regel wird ausgeführt, wenn** die Option **Absender**, und wählen Sie dann **IP-Adresse ist in keinem dieser Bereiche oder stimmt mit keinem Bereich völlig überein**.
    
5. Geben Sie im Feld **IP-Adressen angeben** , die IP-Adresse oder die IP-Adressbereich, die Sie in der IP-Zulassungsliste eingegeben haben, klicken Sie auf **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif), und klicken Sie dann auf **ok**.
    
6. Legen Sie unter **Gehen Sie folgendermaßen vor:** die Aktion fest, indem Sie erst **Nachrichteneigenschaften ändern** wählen und dann die **SCL-Bewertung (Spam Confidence Level) festlegen**. Wählen Sie im Feld **SCL angeben** die Option **0**, und klicken Sie auf **OK**.
    
7. Klicken Sie unter **Außer wenn** auf **Ausnahme hinzufügen**, und wählen Sie erst **Absender** und dann **Domäne ist**. 
    
8. Geben Sie in das Feld **Geben Sie die Domäne** der Domäne für die umgehen der Spamfilterung wie **contosob.com**werden soll. Klicken Sie auf **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) in der Liste der Ausdrücke zu verschieben. Wiederholen Sie diesen Schritt, wenn Sie verwenden möchten, fügen Sie zusätzliche Domänen als Ausnahmen, und klicken Sie auf **ok** , wenn Sie fertig sind. 
    
9. Wenn Sie möchten, können Sie, Auswahl der Überwachungsregel, testen Sie die Regel, aktivieren die Regel während eines bestimmten Zeitraums und andere Auswahl. Es wird empfohlen, testen die Regel für einen bestimmten Zeitraum, bevor Sie es erzwingen. [Regeln für die Verfahren für die Nachrichtenübermittlung in Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) enthält weitere Informationen zu diesen Auswahlmöglichkeiten. 
    
10. Klicken Sie auf **Speichern** , um die Regel zu speichern. Die Regel in der Liste der Regeln wird angezeigt. 
    
Nach Erstellen und Erzwingen der Regel wird der Spamfilter für die von Ihnen angegebene IP-Adresse bzw. IP-Adressbereich nur für die von Ihnen eingegebene Domänenausnahme umgangen.
  
## <a name="new-to-office-365"></a>Neu bei Office 365?
<a name="sectionSection3"> </a>

||
|:-----|
|![Das Kurzsymbol für LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Neu bei Office 365?**         Entdecken Sie die kostenlosen Videokurse für **Office 365 admins and IT pros**, präsentiert von LinkedIn Learning. |
   
## <a name="for-more-information"></a>Weitere Informationen
<a name="sectionSection4"> </a>

[Listen sicherer und blockierter Absender in Exchange Online](safe-sender-and-blocked-sender-lists-faq.md)
  
[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  
[Konfigurieren der Richtlinie für ausgehende Spamnachrichten](configure-the-outbound-spam-policy.md)
  
[So können Sie dazu beitragen, dass eine Nachricht nicht als Spam gekennzeichnet wird](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

