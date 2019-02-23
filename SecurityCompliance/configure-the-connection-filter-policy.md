---
title: Konfigurieren der Verbindungsfilterrichtlinie
ms.author: tracyp
author: MSFTTracyP
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
ms.collection:
- M365-security-compliance
description: Wenn Sie sicherstellen möchten, dass e-Mails von vertrauenswürdigen Personen nicht blockiert werden, können Sie mithilfe der Verbindungsfilter Richtlinie eine Zulassungsliste mit vertrauenswürdigen IP-Adressen erstellen. Sie können auch eine Liste blockierter Absender erstellen.
ms.openlocfilehash: d7c99f8fb6b9b05efb800804927ccb26f7dd9f40
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216905"
---
# <a name="configure-the-connection-filter-policy"></a>Konfigurieren der Verbindungsfilterrichtlinie
 
Die meisten von uns haben Freunde und Geschäftspartnern, denen wir vertrauen. Es kann ärgerlich sein, E-Mail dieser Absender in Ihrem Junk-E-Mail-Ordner zu finden oder festzustellen, dass sie vom Spamfilter gänzlich blockiert wurden. Wenn Sie sicherstellen möchten, dass von diesen vertrauenswürdigen Absendern gesendete E-Mail nicht blockiert wird, können Sie die Verbindungsfilterrichtlinie zum Erstellen einer Zulassungsliste (bzw. „Liste sicherer Absender") mit vertrauenswürdigen IP-Adressen nutzen. Sie können auch eine Liste blockierter Absender mit IP-Adressen (zumeist von Spammern) erstellen, von denen Sie nie wieder E-Mail-Nachrichten empfangen möchten.
  
 Weitere Antispameinstellungen, die für die gesamte Organisation gelten, finden Sie unter [Sicherstellen, dass eine Nachricht nicht als Spam gekennzeichnet wird](https://go.microsoft.com/fwlink/p/?LinkId=534224) oder [Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zum Verhindern von falsch negativen Ergebnissen](https://go.microsoft.com/fwlink/p/?LinkId=534225). Diese sind hilfreich, wenn Sie über die Steuerung auf Administratorebene verfügen und wenn Sie falsch positive Ergebnisse oder falsch negative Ergebnisse vermeiden möchten.
  
Im folgenden Video wird die Vorgehensweise zur Konfiguration der Verbindungsfilterrichtlinie gezeigt:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

- Geschätzte Zeit zur Durchführung: 15 Minuten
    
- Bevor Sie dieses Verfahren ausführen können, müssen Ihnen Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Antispam" im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Zum Abrufen der IP-Adresse des Absenders, dessen Nachrichten Sie zulassen oder blockieren möchten, können Sie den Internet-Header der Nachricht überprüfen. Suchen Sie den CIP-Header, wie unter [Antispam-Nachrichtenkopfzeilen](anti-spam-message-headers.md)beschrieben. Informationen zum Anzeigen eines Nachrichtenkopfs in verschiedenen e-Mail-Clients finden Sie unter [Message Header Analyzer](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
    
- E-Mails, die von einer IP-Adresse aus der IP-Sperrliste gesendet werden, werden abgelehnt, nicht als Spam gekennzeichnet, und es werden keine weiteren Filter angewendet.
    
- Das folgende Verbindungsfilter Verfahren kann auch über Remote-PowerShell ausgeführt werden. Verwenden Sie das Cmdlet [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) , um Ihre Einstellungen zu überarbeiten, und die [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) , um die Einstellungen für die Verbindungsfilter Richtlinie zu bearbeiten. Informationen dazu, wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online Protection herstellen, finden Sie unter [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). Informationen zur Verwendung von Windows PowerShell zum Herstellen einer Verbindung mit Exchange Online finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>Bearbeiten der Standardrichtlinie für Verbindungsfilter mithilfe der Exchange-Verwaltungskonsole
<a name="sectionSection1"> </a>

Durch Bearbeiten der Verbindungsfilterrichtlinie in der Exchange-Verwaltungskonsole können Sie eine IP-Zulassungs- bzw. -Sperrliste erstellen. Die Einstellungen für die Verbindungsfilterrichtlinie werden nur auf eingehende Nachrichten angewendet.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Verbindungsfilter**, und doppelklicken Sie dann auf die Standardrichtlinie.
    
2. Klicken Sie auf die Menüoption **Verbindungsfilterung**, und erstellen Sie dann die gewünschten Listen: eine IP-Zulassungsliste, eine IP-Sperrliste oder beides. 
    
    Klicken Sie zum Erstellen dieser Listen auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif). Geben Sie im folgenden Dialogfeld die IP-Adressen oder den IP-Adressbereich an, und klicken Sie dann auf **OK**. Wiederholen Sie diesen Vorgang, um weitere Adressen hinzuzufügen. (Sie können IP-Adressen auch bearbeiten oder entfernen, nachdem sie hinzugefügt wurden.)
    
    > [!NOTE]
    >  Wenn Sie beide Listen eine IP-Adresse hinzufügen, werden e-Mails, die von dieser IP-Adresse gesendet werden, zugelassen. 

    Geben Sie IPV4-IP-Adressen im Format nnn. nnn. nnn. nnn an, wobei nnn eine Zahl zwischen 0 und 255 ist. Sie können auch klassenübergreifende CIDR-Bereiche (Inter-Domain Routing) im Format nnn. nnn. nnn. nnn/RR angeben, wobei RR eine Zahl zwischen 24 und 32 ist. Wenn Sie Bereiche außerhalb des Bereichs 24 bis 32 angeben möchten, finden Sie weitere Informationen zum [Konfigurieren von IP-Zulassungslisten](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). 

    Sie können maximal 1273 Einträge angeben, wobei ein Eintrag entweder eine einzelne IP-Adresse oder ein CIDR-Adressfeld mit IP-Adressen von/24 zu/32 ist. > Wenn Sie TLS-verschlüsselte Nachrichten senden, werden IPv6-Adressen und Adressbereiche nicht unterstützt. 
  
3. Aktivieren Sie optional das Kontrollkästchen **sichere Liste aktivieren** , um die fehlenden e-Mails bestimmter bekannter Absender zu verhindern. , Wie? Microsoft abonniert Drittanbieterquellen von vertrauenswürdigen Absendern. Die Verwendung dieser sicheren Liste bedeutet, dass diese vertrauenswürdigen Absender nicht fälschlicherweise als Spam gekennzeichnet werden. Es wird empfohlen, diese Option auszuwählen, da Sie die Anzahl falsch positiver e-Mail-Nachrichten, die als Spam klassifiziert werden, verringern sollte. 
    
4. Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Standardrichtlinieneinstellungen angezeigt.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>Weitere Überlegungen zum Konfigurieren von Listen zugelassener IP-Adressen
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

Folgende Überlegungen sollten Sie anstellen, wenn Sie eine Liste zugelassener IP-Adressen konfigurieren möchten.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>Angeben eines CIDR-Bereichs, der außerhalb des empfohlenen Bereichs liegt

Wenn Sie einen CIDR-IP-Adressbereich von/1 bis/23 angeben möchten, müssen Sie eine e-Mail-Fluss Regel erstellen, die auf dem IP-Adressbereich ausgeführt wird, der das Spam Confidence Level (SCL) zur **Umgehung der Spamfilterung** festlegt (d. h., alle Nachrichten, die innerhalb dieses IP-Adressbereichs empfangen werden, sind wird auf "kein Spam" festgelegt), und es wird keine zusätzliche Filterung vom Dienst ausgeführt). Wenn jedoch eine dieser IP-Adressen in einer der proprietären Sperrlisten von Microsoft oder in einer unserer Sperrlisten von Drittanbietern angezeigt wird, werden diese Nachrichten weiterhin blockiert. Es wird daher dringend empfohlen, den IP-adressumfang von/24 to/32 zu verwenden. 
  
Führen Sie die folgenden Schritte aus, um diese e-Mail-Fluss Regel zu erstellen.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Wählen Sie unter **Diese Regel wird ausgeführt, wenn** die Option **Absender**, und wählen Sie dann **IP-Adresse ist in keinem dieser Bereiche oder stimmt mit keinem Bereich völlig überein**.
    
5. Geben Sie in die IP- **Adressen angeben**den IP-Adressbereiche an, klicken](media/ITPro-EAC-AddIcon.gif)Sie auf Add-Symbol **Hinzufügen** ![, und klicken Sie dann auf **OK**.
    
6. Legen Sie unter **Gehen Sie folgendermaßen vor:** die Aktion fest, indem Sie erst **Nachrichteneigenschaften ändern** wählen und dann die **SCL-Bewertung (Spam Confidence Level) festlegen**. Wählen Sie im Feld **SCL angeben** die Option **Spamfilter umgehen**, und klicken Sie auf **OK**.
    
7. Wenn Sie möchten, können Sie eine Auswahl treffen, um die Regel zu überwachen, die Regel zu testen, die Regel während eines bestimmten Zeitraums zu aktivieren und andere Optionen auszuwählen. Es wird empfohlen, die Regel für einen Zeitraum zu testen, bevor Sie Sie erzwingen. Die [Verfahren für Nachrichtenfluss Regeln in Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) enthalten weitere Informationen zu diesen Auswahlmöglichkeiten. 
    
8. Klicken Sie auf **Speichern** , um die Regel zu speichern. Die Regel wird in der Liste der Regeln angezeigt. 
    
Nachdem Sie die Regel erstellt und erzwungen haben, umgeht der Dienst die Spamfilterung für den angegebenen IP-Adressbereiche.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>Bereichsfestlegung für Ausnahmen von einer Liste der zugelassenen IP-Adressen einer bestimmten Domäne

Sie sollten die IP-Adresse (oder IP-Adressbereiche) für alle Ihre Domänen, die Sie als sicher einschätzen, der Liste der zugelassenen IP-Adressen hinzufügen. Wenn Sie jedoch nicht wünschen, dass der Eintrag in dieser IP-Adressliste für alle Domänen gilt, erstellen Sie eine Transportregel, von der bestimmte Domänen ausgenommen sind. 
  
Nehmen wir an, Sie haben drei Domänen: ContosoA.com, ContosoB.com und ContosoC.com. Sie wollen die IP-Adresse (zur Vereinfachung verwenden wir 1.2.3.4) hinzufügen und die Filterung nur für die Domäne ContosoB.com überspringen. Dazu müssten Sie eine IP-Zulassungsliste für 1.2.3.4 erstellen, mit der die SCL-Bewertung (Spam Confidence Level) für alle Domänen auf -1 gesetzt wird (was bedeutet, dass sie als "Kein Spam" klassifiziert wird). Sie können dann eine Transportregel erstellen, mit der die SCL-Bewertung für alle Domänen außer ContosoB.com auf 0 gesetzt wird. Das bewirkt, dass die Nachricht für alle Domänen, die der IP-Adresse zugeordnet sind, erneut überprüft wird - mit Ausnahme von ContosoB.com, weil diese Domäne als Ausnahme in der Regel definiert ist. ContosoB.com hat weiterhin eine SCL-Bewertung von -1, was das Überspringen der Filterung bedeutet, während ContosoA.com und ContosoC.com SCL-Bewertungen von 0 haben, was bedeutet, dass sie durch den Inhaltsfilter erneut überprüft werden.
  
Führen Sie dazu die folgenden Schritte aus:
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Wählen Sie unter **Diese Regel wird ausgeführt, wenn** die Option **Absender**, und wählen Sie dann **IP-Adresse ist in keinem dieser Bereiche oder stimmt mit keinem Bereich völlig überein**.
    
5. Geben Sie im Feld IP- **Adressen angeben** die IP-Adresse oder den IP-Adressbereiche an, die Sie in die **** ![IP-Zulassungs](media/ITPro-EAC-AddIcon.gif)Liste eingegeben haben, klicken Sie auf Hinzufügen, und klicken Sie dann auf **OK**.
    
6. Legen Sie unter **Gehen Sie folgendermaßen vor:** die Aktion fest, indem Sie erst **Nachrichteneigenschaften ändern** wählen und dann die **SCL-Bewertung (Spam Confidence Level) festlegen**. Wählen Sie im Feld **SCL angeben** die Option **0**, und klicken Sie auf **OK**.
    
7. Klicken Sie unter **Außer wenn** auf **Ausnahme hinzufügen**, und wählen Sie erst **Absender** und dann **Domäne ist**. 
    
8. Geben Sie im Feld **Domäne angeben** die Domäne ein, für die Sie die Spamfilterung umgehen möchten, beispielsweise **contosob.com**. Klicken Sie auf Symbol](media/ITPro-EAC-AddIcon.gif) hinzufügen, um es in die Liste der Ausdrücke zu verschieben. **** ![ Wiederholen Sie diesen Schritt, wenn Sie zusätzliche Domänen als Ausnahmen hinzufügen möchten, und klicken Sie auf **OK** , wenn Sie fertig sind. 
    
9. Wenn Sie möchten, können Sie eine Auswahl treffen, um die Regel zu überwachen, die Regel zu testen, die Regel während eines bestimmten Zeitraums zu aktivieren und andere Optionen auszuwählen. Es wird empfohlen, die Regel für einen Zeitraum zu testen, bevor Sie Sie erzwingen. Die [Verfahren für Nachrichtenfluss Regeln in Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) enthalten weitere Informationen zu diesen Auswahlmöglichkeiten. 
    
10. Klicken Sie auf **Speichern** , um die Regel zu speichern. Die Regel wird in der Liste der Regeln angezeigt. 
    
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
  

