---
title: Create organization-wide safe sender or blocked sender lists in Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/8/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150s
ms.assetid: 9721b46d-cbea-4121-be51-542395e6fd21
description: Wenn Sie möchten, um sich zu vergewissern, dass Sie Nachrichten von einem bestimmten Absender, empfangen, da Sie sie und ihre Nachrichten vertrauen, können Sie Anpassen Ihrer Liste in einer Richtlinie Spam-Filter in der Exchange-Verwaltungskonsole zu ermöglichen.
ms.openlocfilehash: a90679fc900ca5695904898af3627fc1900a8545
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003164"
---
# <a name="create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365"></a>Create organization-wide safe sender or blocked sender lists in Office 365
  
Wenn Sie möchten, um sich zu vergewissern, dass Sie Nachrichten von einem bestimmten Absender, empfangen, da Sie sie und ihre Nachrichten vertrauen, können Sie Anpassen Ihrer Zulassungsliste in einer Richtlinie Spam-Filter in der Exchange-Verwaltungskonsole (EAC) unter **Schutz** \> **Spam-Filter**. Weitere Informationen hierzu unter [Ihrer Spam-Filter-Richtlinien konfigurieren](configure-your-spam-filter-policies.md). Eine weitere Option wäre eine Exchange-Transportregel erstellen, dass den Spam-Filter funktioniert wie in der Domäne oder benutzerbasierten Liste zulassen. Sie können Nachrichten von einer bestimmten Domäne oder eines Benutzers auf ähnliche Weise zu blockieren.
  
Eine Transportregel würde in dieser Situation hilfreich sein, wenn Sie zum Filtern von komplexen Kriterien wie Nachrichtenkopfzeilen oder die Namen von Anlagen überprüfen müssen, oder wenn Sie komplexe Aktionen wie hinzufügen einen Haftungsausschluss auf die Nachricht oder einen bestimmten Zeitraum anwenden hinzufügen möchten, auf dem die Rul e ist aktiv. Es ist jedoch die bevorzugte Methode, um sicherzustellen, dass e-Mails von einem bestimmten Absender oder Domäne den Spamfilter umgehen diese Richtlinie Ihrer Spam-Filter hinzufügen. Erste Schritte mit dies in der Exchange-Verwaltungskonsole zu **Schutz** zugreifen, indem \> **Spam-Filter**. Weitere Informationen finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](configure-your-spam-filter-policies.md).
  
> [!TIP]
> Eine Liste domänenbasierte in einer Transportregel nicht so sicher wie eine Liste mit IP-Adresse, da Domänen manipuliert werden können. Darüber hinaus ist die IP-Adresse des Absenders in einer Sperrliste, es weiterhin blockiert werden, auch wenn für die Domäne filtern oder Benutzer wird umgangen wird. Dies ist, da eine Transportregel auf eine Domäne oder einen Benutzer globale IP-Sperrliste nicht außer Kraft setzt. Es wird empfohlen, eine Liste mit IP-Adresse in den meisten Fällen verwenden. Um eine Liste mit IP-Adresse zu erstellen, können Sie die Liste zugelassener IP-Adressen oder IP-Sperrliste im Verbindungsfilter verwenden. Alle Nachrichten von dieser IP-Adressen werden vom Inhaltsfilter nicht überprüft. Anweisungen zum Konfigurieren der verbindungsfilterrichtlinie IP-Adressen hinzugefügt, zu der Liste zugelassener IP-Adressen oder IP-Sperrliste finden Sie unter [Konfigurieren der verbindungsfilterrichtlinie](configure-the-connection-filter-policy.md). 
  
Informationen zu weiteren Verwaltungsaufgaben in Bezug auf Transportregeln finden Sie unter [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
## <a name="use-the-eac-to-customize-a-block-or-allow-list-to-prevent-or-receive-email-from-a-domain-or-user"></a>Verwenden der Exchange-Verwaltungskonsole, damit die Liste, um zu verhindern, dass oder Empfangen von e-Mails von einer Domäne oder eines Benutzers oder einen Block anpassen

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Spam-Filter**. 
    
2. Führen Sie auf der Seite **Allgemein** eine der folgenden Aktionen aus: 
    
  - Doppelklicken Sie auf die Standardrichtlinie oder eine vorhandene Richtlinie, um die Bearbeitung zu starten.
    
  - Klicken Sie auf **neu** , um eine neue Richtlinie für den benutzerdefinierten Spam-Filter zu erstellen, die Benutzern, Gruppen und Domänen in Ihrer Organisation angewendet werden können. 
    
3. Auf der Seite **Listen ermöglichen** können Sie angeben, Einträge, wie Absender oder Domänen, die immer in den Posteingang übermittelt werden können. E-Mail-Nachrichten von dieser Einträge wird von den Spam-Filter nicht verarbeitet. Die folgenden Schritte aus: 
    
  - Fügen Sie vertrauenswürdige Absender an den Absender Liste zulassen. Klicken Sie auf **Hinzufügen**, und fügen Sie im Dialogfeld Auswahl die Absenderadressen, die Sie zulassen möchten. Sie können mehrere Einträge mit einem Semikolon oder eine neue Zeile zu trennen. Klicken Sie auf Ok, um die Seite **Zulassen Listen** zurückzukehren. 
    
  - Fügen Sie vertrauenswürdige Domänen auf die Domäne Liste zulassen. Klicken Sie auf **Hinzufügen**, und fügen Sie im Dialogfeld Auswahl der Domänen, die Sie zulassen möchten. Sie können mehrere Einträge mit einem Semikolon oder eine neue Zeile zu trennen. Klicken Sie auf Ok, um die Seite **Zulassen Listen** zurückzukehren. 
    
    > [!CAUTION]
    > Wenn Sie Domänen auf oberster Ebene zulassen, ist es wahrscheinlich, dass unerwünschte E-Mails an einen Posteingang übermittelt werden. 
  
4. Auf der Seite **Sperrlisten** können Sie Einträge, wie z. B. Absender oder Domänen, angeben, die immer als Spam markiert werden. Der Dienst wendet die konfigurierte Spamaktion bei hoher Vertrauenswürdigkeit auf E-Mails an, die diesen Einträgen entsprechen. 
    
  - Fügen Sie der Absendersperrliste unerwünschte Absender hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Absenderadressen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **OK**, um zur Seite **Sperrlisten** zurückzukehren. 
    
  - Fügen Sie der Domänensperrliste unerwünschte Domänen hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Domänen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **OK**, um zur Seite **Sperrlisten** zurückzukehren. 
    
    > [!CAUTION]
    > Wenn Sie Domänen auf oberster Ebene blockieren, ist es wahrscheinlich, dass E-Mails, die Sie erhalten möchten, als Spam markiert werden. 
  
## <a name="what-do-you-need-to-know-before-you-begin-creating-a-transport-rule"></a>Wobei benötigen Sie wissen, bevor Sie mit dem Erstellen einer Transportregel beginnen?
    
- Sie müssen nicht erstellen eine Transportregel zum Umgehen der Spamfilterung oder e-Mail als Spam für einen Absender oder eine Domäne markieren. Verwenden Sie den Exchange Online Protection-Block und ermöglichen Sie Listen in einer Spam-Richtlinie anstelle von Transportregel zu, wenn Sie einfach blockieren oder Zulassen eines bestimmten Absender oder einer Domäne und etwaige zusätzlichen Auflagen nicht anfügen möchten. Weitere Informationen hierzu unter [Ihrer Spam-Filter-Richtlinien konfigurieren](configure-your-spam-filter-policies.md).
    
- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Transportregeln" im Thema [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx). 
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.
    
> [!TIP]
> Liegt ein Problem vor? Erhalten Sie in der Exchange-Foren. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542)oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-the-eac-to-create-a-transport-rule-to-bypass-spam-filtering-for-a-domain-or-user"></a>Verwenden der Exchange-Verwaltungskonsole zum Erstellen einer Transportregel umgehen der Spamfilterung für eine Domäne oder einen Benutzer

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**. Wählen Sie **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann die **Umgehung Spam-Filter**.
    
2. Benennen Sie die Regel. Wählen Sie unter **Diese Regel anwenden, wenn** die Option **Der Absender** und dann eine der folgenden Bedingungen aus: 
    
  - Wenn Sie eine Domäne angeben möchten, wählen Sie die **Domäne ist**. Geben Sie die Domäne des Absenders, den Sie als sicherer, beispielsweise "contoso.com" festlegen möchten, klicken Sie im Dialogfeld **Domäne angeben** . **Fügen Sie hinzu** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) in der Liste der Ausdrücke zu verschieben. Wiederholen Sie diesen Schritt, wenn Sie möchten zusätzliche Domänen hinzufügen, und klicken Sie auf **OK** , wenn Sie fertig sind. 
    
  - Wenn Sie einen Benutzer angeben möchten, klicken Sie auf **ist diese Person**. Fügen Sie im Dialogfeld **Mitglieder hinzufügen** den Benutzer aus der Liste hinzu, geben Sie den Benutzernamen ein, und klicken Sie auf **Namen überprüfen**. Wiederholen Sie diesen Schritt ggf. für weitere Benutzer, und klicken Sie zum Abschluss auf **OK**. 
    
3. Aktivieren Sie das Kontrollkästchen **Keine weiteren Regeln anwenden**, um sicherzustellen, dass keine andere Regel die Umgehungsaktion umkehren kann. 
    
4. Wählen Sie für **Absenderadresse in Nachricht** die Option **Kopfzeile oder Umschlag** aus.
    
5. Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen. Es wird empfohlen, die Regel eine Zeit lang zu testen, bevor Sie sie in Ihrer Organisation erzwingen. Weitere Informationen zu diesen Einstellungen finden Sie unter [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx).
    
6. Wählen Sie **Speichern** aus, um die Regel zu speichern. 
    
Nachdem Sie die Regel erstellt und erzwungen haben, wird die Spamfilterung für die angegebene Domäne oder den angegebenen Benutzer umgangen.
  
## <a name="use-the-eac-to-create-a-transport-rule-that-blocks-messages-sent-from-a-domain-or-user"></a>Verwenden der Exchange-Verwaltungskonsole eine Transportregel erstellen, die von einer Domäne oder Benutzer gesendete Nachrichten blockiert

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**. Wählen Sie **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann auf **neue Regel erstellen**.
    
2. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**. 
    
3. Wählen Sie unter **Diese Regel anwenden, wenn** die Option **Der Absender** und dann eine der folgenden Bedingungen aus: 
    
  - Wenn Sie eine Domäne angeben möchten, wählen Sie die **Domäne ist**. Geben Sie im Dialogfeld Domäne angeben die Domäne des Absenders, von der Sie Nachrichten, beispielsweise "contoso.com" blockieren möchten. Klicken Sie auf **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) in der Liste der Ausdrücke zu verschieben. Wiederholen Sie diesen Schritt, wenn Sie möchten zusätzliche Domänen hinzufügen, und klicken Sie auf **OK** , wenn Sie fertig sind. 
    
  - Wenn Sie einen Benutzer angeben möchten, klicken Sie auf **ist diese Person**. Fügen Sie im Dialogfeld **Mitglieder hinzufügen** den Benutzer aus der Liste hinzu, geben Sie den Benutzernamen ein, und klicken Sie auf **Namen überprüfen**. Wiederholen Sie diesen Schritt ggf. für weitere Benutzer, und klicken Sie zum Abschluss auf **OK**. 
    
4. Wählen Sie unter **Gehen Sie folgendermaßen vor** die Option **Nachricht blockieren** aus, und klicken Sie dann auf eine der anderen Optionen wie **Nachricht ohne Benachrichtigung anderer Benutzer löschen**.
    
5. Klicken Sie auf **Weitere Optionen**, und wählen Sie dann für **Absenderadresse in Nachricht** die Option **Kopfzeile oder Umschlag** aus.
    
6. Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen. Es wird empfohlen, die Regel eine Zeit lang zu testen, bevor Sie sie in Ihrer Organisation erzwingen. Weitere Informationen zu diesen Einstellungen finden Sie unter [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx).
    
7. Wählen Sie **Speichern** aus, um die Regel zu speichern. 
    
Nachdem Sie die Regel erstellt und erzwungen haben, werden alle von der von Ihnen angegebenen Domäne oder dem von Ihnen angegebenen Benutzer gesendeten Nachrichten blockiert.
  
## <a name="see-also"></a>Siehe auch

[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  
[Verwenden von Transportregeln zum Konfigurieren von Massen-e-Mail-Filterung](use-transport-rules-to-configure-bulk-email-filtering.md)

