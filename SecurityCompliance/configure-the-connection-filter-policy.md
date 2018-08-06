---
title: Konfigurieren der Verbindungsfilterrichtlinie
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
description: Um sicherzustellen, dass von Personen, denen, die Sie vertrauen, gesendete e-Mail nicht gesperrt hat, können Sie der verbindungsfilterrichtlinie verwenden, um eine Liste, auch bekannt als eine Liste sicherer Absender verwendet werden, der IP-Adressen zu erstellen, denen Sie vertrauen. Sie können auch eine Liste der blockierten Absender erstellen.
ms.openlocfilehash: d106e55779c6246b77018fef3ab9d58fa759d99e
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027602"
---
# <a name="configure-the-connection-filter-policy"></a>Konfigurieren der Verbindungsfilterrichtlinie
 
Die meisten von uns haben Freunde und Geschäftspartnern, denen wir vertrauen. Es kann ärgerlich sein, E-Mail dieser Absender in Ihrem Junk-E-Mail-Ordner zu finden oder festzustellen, dass sie vom Spamfilter gänzlich blockiert wurden. Wenn Sie sicherstellen möchten, dass von diesen vertrauenswürdigen Absendern gesendete E-Mail nicht blockiert wird, können Sie die Verbindungsfilterrichtlinie zum Erstellen einer Zulassungsliste (bzw. „Liste sicherer Absender") mit vertrauenswürdigen IP-Adressen nutzen. Sie können auch eine Liste blockierter Absender mit IP-Adressen (zumeist von Spammern) erstellen, von denen Sie nie wieder E-Mail-Nachrichten empfangen möchten.
  
 Weitere Antispameinstellungen, die für die gesamte Organisation gelten, finden Sie unter [Sicherstellen, dass eine Nachricht nicht als Spam gekennzeichnet wird](https://go.microsoft.com/fwlink/p/?LinkId=534224) oder [Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zum Verhindern von falsch negativen Ergebnissen](https://go.microsoft.com/fwlink/p/?LinkId=534225). Diese sind hilfreich, wenn Sie über die Steuerung auf Administratorebene verfügen und wenn Sie falsch positive Ergebnisse oder falsch negative Ergebnisse vermeiden möchten.
  
Im folgenden Video wird die Vorgehensweise zur Konfiguration der Verbindungsfilterrichtlinie gezeigt:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 15 Minuten
    
- Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "AntiSpam" im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Um die IP-Adresse des Absenders zu ermitteln, dessen Nachrichten Sie zulassen oder blockieren möchten, können Sie die Internetkopfzeile der Nachricht prüfen. Suchen Sie, wie in [Antispam-Nachrichtenkopfzeilen](anti-spam-message-headers.md) beschrieben, nach der CIP-Kopfzeile. Informationen dazu, wie Sie einen Nachrichtenkopf in verschiedenen E-Mail-Clients anzeigen, finden Sie unter [Message Header Analyzer](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
    
- E-Mails, die von einer IP-Adresse aus der IP-Sperrliste gesendet werden, werden abgelehnt, nicht als Spam gekennzeichnet, und es werden keine weiteren Filter angewendet.
    
- Das folgende Verfahren der Connection Filter kann auch über remote-PowerShell erfolgen. Verwenden Sie das Cmdlet [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) , um Ihre Einstellungen, und das [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) zum Bearbeiten Ihrer filtereinstellungen Richtlinie Verbindung prüfen. Weitere Informationen zu Windows PowerShell verwenden, um die Verbindung mit Exchange Online Protection finden Sie unter [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). So verwenden Sie Windows PowerShell für die Verbindung zu Exchange Online finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>Bearbeiten der Standardrichtlinie für Verbindungsfilter mithilfe der Exchange-Verwaltungskonsole
<a name="sectionSection1"> </a>

Durch Bearbeiten der Verbindungsfilterrichtlinie in der Exchange-Verwaltungskonsole können Sie eine IP-Zulassungs- bzw. -Sperrliste erstellen. Die Einstellungen für die Verbindungsfilterrichtlinie werden nur auf eingehende Nachrichten angewendet.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Verbindungsfilter**, und doppelklicken Sie dann auf die Standardrichtlinie.
    
2. Klicken Sie auf die Menüoption **Verbindungsfilterung**, und erstellen Sie dann die gewünschten Listen: eine IP-Zulassungsliste, eine IP-Sperrliste oder beides. 
    
    Klicken Sie zum Erstellen dieser Listen auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Geben Sie im folgenden Dialogfeld die IP-Adressen oder den IP-Adressbereich an, und klicken Sie dann auf **OK**. Wiederholen Sie diesen Vorgang, um weitere Adressen hinzuzufügen. (Sie können IP-Adressen auch bearbeiten oder entfernen, nachdem sie hinzugefügt wurden.)
    
    > [!NOTE]
    >  Wenn Sie eine IP-Adresse beiden Listen hinzufügen, wird von dieser gesendete E-Mail zugelassen. >  IPV4-IP-Adressen müssen im Format nnn.nnn.nnn.nnn angegeben werden, wobei nnn eine Zahl von 0 bis 255 ist. Sie können auch CIDR-Bereiche (Classless Inter-Domain Routing) im Format nnn.nnn.nnn.nnn/rr angeben, wobei rr eine Zahl von 24 bis 32 ist. Informationen zum Angeben von Bereichen außerhalb des Bereichs von 24 bis 32 finden Sie unter [Weitere Überlegungen zum Konfigurieren von Listen zugelassener IP-Adressen](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). >  Sie können maximal 1273 Einträge angeben, wobei ein Eintrag einer einzelnen IP-Adresse oder einem CIDR-Bereich von IP-Adressen von /24 bis /32 entspricht. >  Wenn Sie TLS-verschlüsselte Nachrichten senden, werden IPv6-Adressen und -Adressbereiche nicht unterstützt. 
  
3. Aktivieren Sie optional das Kontrollkästchen **Liste sicherer Adressen aktivieren**, um zu verhindern, dass Sie E-Mail von bestimmten bekannten Absendern verpassen. Wie? Microsoft hat verschiedene Quellen von Drittanbietern mit vertrauenswürdigen Absendern abonniert. Mithilfe dieser sicheren Liste sorgen Sie dafür, dass diese vertrauenswürdigen Absender nicht versehentlich als Spammer gekennzeichnet werden. Es wird empfohlen, diese Option auszuwählen, da dadurch die Anzahl falsch positiver Ergebnisse (also unbedenklicher E-Mails, die als Spam klassifiziert werden), die Sie erhalten, reduziert werden sollte. 
    
4. Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Standardrichtlinieneinstellungen angezeigt.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>Weitere Überlegungen zum Konfigurieren von Listen zugelassener IP-Adressen
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

Folgende Überlegungen sollten Sie anstellen, wenn Sie eine Liste zugelassener IP-Adressen konfigurieren möchten.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>Angeben eines CIDR-Bereichs, der außerhalb des empfohlenen Bereichs liegt

Wenn Sie einen CIDR-Bereich zwischen /1 und /23 für einen IP-Adressbereich angeben, müssen Sie eine Transportregel aufstellen, die für den IP-Adressbereich gilt, der den Spamwahrscheinlichkeitswert (SCL) mit **Spamfilter umgehen** festlegt (das heißt, alle Nachrichten, die innerhalb dieses IP-Adressbereichs empfangen werden, werden als Nicht-Spam klassifiziert, und der Dienst nimmt keine zusätzliche Filterung vor). Falls eine dieser IP-Adressen jedoch in einer der proprietären Sperrlisten von Microsoft oder eines Drittanbieters auftaucht, werden diese Nachrichten weiterhin gesperrt. Daher wird unbedingt empfohlen, dass Sie den IP-Adressbereich zwischen /32 und /24 verwenden. 
  
Führen Sie die folgenden Schritte aus, um eine Transportregel zu erstellen.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Wählen Sie unter **Diese Regel wird ausgeführt, wenn** die Option **Absender**, und wählen Sie dann **IP-Adresse ist in keinem dieser Bereiche oder stimmt mit keinem Bereich völlig überein**.
    
5. Geben Sie im **Eingabefeld für IP-Adressen** den IP-Adressbereich ein, und klicken Sie erst auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png) und dann auf **OK**.
    
6. Legen Sie unter **Gehen Sie folgendermaßen vor:** die Aktion fest, indem Sie erst **Nachrichteneigenschaften ändern** wählen und dann die **SCL-Bewertung (Spam Confidence Level) festlegen**. Wählen Sie im Feld **SCL angeben** die Option **Spamfilter umgehen**, und klicken Sie auf **OK**.
    
7. Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen. Wir empfehlen, die Regel über eine bestimmte Zeit zu testen, bevor Sie sie erzwingen. Weitere Informationen zu diesen Optionen finden Sie unter [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx). 
    
8. Klicken Sie auf die Schaltfläche **Speichern**, um die Regel zu speichern. Sie wird in der Liste der Regeln angezeigt. 
    
Nach Erstellen und Erzwingen der Regel wird der Spamfilter für den von Ihnen angegebenen IP-Adressbereich umgangen.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>Bereichsfestlegung für Ausnahmen von einer Liste der zugelassenen IP-Adressen einer bestimmten Domäne

Sie sollten die IP-Adresse (oder IP-Adressbereiche) für alle Ihre Domänen, die Sie als sicher einschätzen, der Liste der zugelassenen IP-Adressen hinzufügen. Wenn Sie jedoch nicht wünschen, dass der Eintrag in dieser IP-Adressliste für alle Domänen gilt, erstellen Sie eine Transportregel, von der bestimmte Domänen ausgenommen sind. 
  
Nehmen wir an, Sie haben drei Domänen: ContosoA.com, ContosoB.com und ContosoC.com. Sie wollen die IP-Adresse (zur Vereinfachung verwenden wir 1.2.3.4) hinzufügen und die Filterung nur für die Domäne ContosoB.com überspringen. Dazu müssten Sie eine IP-Zulassungsliste für 1.2.3.4 erstellen, mit der die SCL-Bewertung (Spam Confidence Level) für alle Domänen auf -1 gesetzt wird (was bedeutet, dass sie als "Kein Spam" klassifiziert wird). Sie können dann eine Transportregel erstellen, mit der die SCL-Bewertung für alle Domänen außer ContosoB.com auf 0 gesetzt wird. Das bewirkt, dass die Nachricht für alle Domänen, die der IP-Adresse zugeordnet sind, erneut überprüft wird - mit Ausnahme von ContosoB.com, weil diese Domäne als Ausnahme in der Regel definiert ist. ContosoB.com hat weiterhin eine SCL-Bewertung von -1, was das Überspringen der Filterung bedeutet, während ContosoA.com und ContosoC.com SCL-Bewertungen von 0 haben, was bedeutet, dass sie durch den Inhaltsfilter erneut überprüft werden.
  
Führen Sie dazu die folgenden Schritte aus:
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Wählen Sie unter **Diese Regel wird ausgeführt, wenn** die Option **Absender**, und wählen Sie dann **IP-Adresse ist in keinem dieser Bereiche oder stimmt mit keinem Bereich völlig überein**.
    
5. Geben Sie im **Eingabefeld für IP-Adressen** die IP-Adresse oder den IP-Adressbereich ein, die bzw. den Sie in der Liste der zugelassenen IP-Adresse angegeben haben, und klicken Sie erst auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png) und dann auf **OK**.
    
6. Legen Sie unter **Gehen Sie folgendermaßen vor:** die Aktion fest, indem Sie erst **Nachrichteneigenschaften ändern** wählen und dann die **SCL-Bewertung (Spam Confidence Level) festlegen**. Wählen Sie im Feld **SCL angeben** die Option **0**, und klicken Sie auf **OK**.
    
7. Klicken Sie unter **Außer wenn** auf **Ausnahme hinzufügen**, und wählen Sie erst **Absender** und dann **Domäne ist**. 
    
8. Geben Sie im Feld **Domäne angeben** diejenige Domäne ein, für die der Spamfilter umgangen werden soll, beispielsweise **contosob.com**. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png), um sie in die Liste der Ausdrücke zu verschieben. Wiederholen Sie diesen Schritt, falls Sie zusätzliche Domänen als Ausnahmen hinzufügen möchten, und klicken Sie abschließend auf **OK**. 
    
9. Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen. Wir empfehlen, die Regel über eine bestimmte Zeit zu testen, bevor Sie sie erzwingen. Weitere Informationen zu diesen Optionen finden Sie unter [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx). 
    
10. Klicken Sie auf die Schaltfläche **Speichern**, um die Regel zu speichern. Sie wird in der Liste der Regeln angezeigt. 
    
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
  

