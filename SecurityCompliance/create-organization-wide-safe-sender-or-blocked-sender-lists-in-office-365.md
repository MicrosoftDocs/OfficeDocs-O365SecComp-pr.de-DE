---
title: Erstellen von organisationsweiten Listen sicherer Absender oder blockierter Absender in Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/8/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150s
ms.assetid: 9721b46d-cbea-4121-be51-542395e6fd21
description: Wenn Sie sicherstellen möchten, dass Sie e-Mails von einem bestimmten Absender erhalten, weil Sie Ihnen und ihren Nachrichten Vertrauen, können Sie Ihre Zulassungsliste in einer Spamfilter Richtlinie im Exchange Admin Center anpassen.
ms.openlocfilehash: 765660ba8c0c9ab384368a0f0c4cd194e4ff2bc6
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693274"
---
# <a name="create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365"></a>Erstellen von organisationsweiten Listen sicherer Absender oder blockierter Absender in Office 365
  
Wenn Sie sicherstellen möchten, dass Sie e-Mails von einem bestimmten Absender erhalten, weil Sie Ihnen und ihren Nachrichten Vertrauen, können Sie Ihre Zulassungsliste in einer Spamfilter Richtlinie im Exchange Admin Center (EAC) unter **Schutz** \> - **Spamfilter**anpassen. Weitere Informationen finden Sie unter [configure your Spamfilter Policies](configure-your-spam-filter-policies.md). Eine weitere Option wäre das Erstellen einer Exchange-Nachrichtenfluss Regel (auch als Transportregel bezeichnet), die wie die Domänen-oder benutzerbasierte Zulassungsliste im Spamfilter funktioniert. Sie können Nachrichten, die von einer bestimmten Domäne oder einem Benutzer gesendet werden, auch auf ähnliche Weise blockieren.
  
Eine e-Mail-Fluss Regel wäre in dieser Situation hilfreich, wenn Sie nach komplexen Kriterien wie dem Überprüfen von Nachrichtenkopfzeilen oder den Namen von Anlagenfiltern möchten, oder wenn Sie komplexe Aktionen wie Hinzufügen eines Haftungsausschlusses zur Nachricht oder Anwenden eines Zeitraums, in dem die Regel e ist aktiv. Die bevorzugte Methode, um sicherzustellen, dass e-Mails von einem bestimmten Absender oder einer Domäne Ihren Spamfilter umgehen, besteht jedoch darin, Sie Ihrer Spamfilter Richtlinie hinzuzufügen. Erste Schritte mit diesem in der Exchange-Verwaltungskonsole, indem Sie auf **Schutz** \> - **Spam Filter**. Weitere Informationen finden Sie unter [configure your Spamfilter Policies](configure-your-spam-filter-policies.md).
  
> [!TIP]
> Eine domänenbasierte Liste in einer e-Mail-Fluss Regel ist nicht so sicher wie eine IP-Adress basierte Liste, da Domänen gefälscht werden können. Wenn Sich die IP-Adresse des Absenders außerdem in einer Sperrliste befindet, wird sie auch dann blockiert, wenn die Filterung nach der Domäne oder dem Benutzer umgangen wird. Der Grund ist, dass eine e-Mail-Fluss Regel für eine Domäne oder einen Benutzer die globale IP-Sperrliste nicht außer Kraft setzt. In den meisten Fällen wird empfohlen, eine auf IP-Adressen basierende Liste zu verwenden. Wenn Sie eine auf IP-Adressen basierende Liste erstellen möchten, können Sie die IP-Zulassungsliste oder die IP-Sperrliste im Verbindungsfilter verwenden. Nachrichten, die von diesen IP-Adressen gesendet werden, werden nicht vom Inhaltsfilter überprüft. Anweisungen zum Konfigurieren der Verbindungsfilterrichtlinie durch Hinzufügen von IP-Adressen zur IP-Zulassungsliste oder zur IP-Sperrliste finden Sie unter [Konfigurieren der Verbindungsfilterrichtlinie](configure-the-connection-filter-policy.md). 
  
Weitere Verwaltungsaufgaben im Zusammenhang mit Nachrichtenfluss Regeln finden Sie unter [Mail Flow Rules (Transport Rules) in Exchange Online](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
## <a name="use-the-eac-to-customize-a-block-or-allow-list-to-prevent-or-receive-email-from-a-domain-or-user"></a>Verwenden der Exchange-verwaltungsKONSOLE zum Anpassen eines Blocks oder einer Zulassungsliste zum verhindern oder empfangen von e-Mails von einer Domäne oder einem Benutzer

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> - **Spam Filter**. 
    
2. Führen Sie auf der Seite **Allgemein** eine der folgenden Aktionen aus: 
    
  - Doppelklicken Sie auf die Standardrichtlinie oder eine vorhandene Richtlinie, um Sie zu bearbeiten.
    
  - Klicken Sie auf **neu** , um eine neue benutzerdefinierte Spamfilter Richtlinie zu erstellen, die auf Benutzer, Gruppen und Domänen in Ihrer Organisation angewendet werden kann. 
    
3. Auf der Seite **Zulassungslisten** können Sie Einträge angeben, z. B. Absender oder Domänen, die immer an den Posteingang übermittelt werden. E-Mails von diesen Einträgen werden nicht vom Spamfilter verarbeitet. Gehen Sie wie folgt vor: 
    
  - Fügen Sie der Zulassungsliste für Absender vertrauenswürdige Absender hinzu. Klicken Sie auf **Hinzufügen**, und fügen Sie dann im Dialogfeldauswahl die Absenderadressen hinzu, die Sie zulassen möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf „OK“, um zur Seite **Zulassungslisten** zurückzukehren. 
    
  - Fügen Sie der Zulassungsliste für Domänen vertrauenswürdige Domänen hinzu. Klicken Sie auf **Hinzufügen**, und fügen Sie dann im Dialogfeldauswahl die Domänen hinzu, die Sie zulassen möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf „OK“, um zur Seite **Zulassungslisten** zurückzukehren. 
    
    > [!CAUTION]
    > Wenn Sie Domänen auf oberster Ebene zulassen, ist es wahrscheinlich, dass unerwünschte E-Mails an einen Posteingang übermittelt werden. 
  
4. Auf der Seite **Sperrlisten** können Sie Einträge, wie z. B. Absender oder Domänen, angeben, die immer als Spam markiert werden. Der Dienst wendet die konfigurierte Spamaktion bei hoher Vertrauenswürdigkeit auf E-Mails an, die diesen Einträgen entsprechen. 
    
  - Fügen Sie der Absendersperrliste unerwünschte Absender hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Absenderadressen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **OK**, um zur Seite **Sperrlisten** zurückzukehren. 
    
  - Fügen Sie der Domänensperrliste unerwünschte Domänen hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Domänen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **OK**, um zur Seite **Sperrlisten** zurückzukehren. 
    
    > [!CAUTION]
    > Wenn Sie Domänen auf oberster Ebene blockieren, ist es wahrscheinlich, dass E-Mails, die Sie erhalten möchten, als Spam markiert werden. 
  
## <a name="what-do-you-need-to-know-before-you-begin-creating-a-mail-flow-rule"></a>Was müssen Sie wissen, bevor Sie mit dem Erstellen einer e-Mail-Fluss Regel beginnen?
    
- Sie müssen keine Nachrichtenfluss Regel erstellen, um die Spamfilterung zu umgehen oder e-Mails als Spam für einen Absender oder eine Domäne zu markieren. Verwenden Sie die Exchange Online Protection-Blockierungs-und Zulassungslisten in einer Spam Richtlinie anstelle dieser Nachrichtenfluss Regel, wenn Sie nur einen bestimmten Absender oder eine Domäne blockieren oder zulassen möchten und keine zusätzlichen Bedingungen anfügen. Weitere Informationen finden Sie unter [configure your Spamfilter Policies](configure-your-spam-filter-policies.md).
    
- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Nachrichtenfluss Regeln" im Thema [Messaging Policy and Compliance Permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) . 
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen im Exchange Admin Center**.
    
> [!TIP]
> Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Sie finden die Foren unter folgenden Links: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder[Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-bypass-spam-filtering-for-a-domain-or-user"></a>Erstellen einer e-Mail-Fluss Regel zum Umgehen der Spamfilterung für eine Domäne oder einen Benutzer mithilfe der Exchange-verwaltungsKONSOLE

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**. Wählen **** ![Sie Add Add](media/ITPro-EAC-AddIcon.gif) Icon aus, und wählen Sie dann **Spamfilterung umgehen**aus.
    
2. Benennen Sie die Regel. Wählen Sie unter **Diese Regel anwenden, wenn** die Option **Der Absender** und dann eine der folgenden Bedingungen aus: 
    
  - If you want to specify a domain, choose **domain is**. Geben Sie im Dialogfeld **Domäne angeben** die Domäne des Absenders ein, den Sie als sicher festlegen möchten, beispielsweise contoso.com. **Hinzufügen** ![Symbol](media/ITPro-EAC-AddIcon.gif) hinzufügen, um es in die Liste der Ausdrücke zu verschieben. Repeat this step if you want to add additional domains, and click **OK** when you are finished. 
    
  - Wenn Sie einen Benutzer angeben möchten, klicken Sie auf **ist diese Person**. Fügen Sie im Dialogfeld **Mitglieder hinzufügen** den Benutzer aus der Liste hinzu, geben Sie den Benutzernamen ein, und klicken Sie auf **Namen überprüfen**. Wiederholen Sie diesen Schritt ggf. für weitere Benutzer, und klicken Sie zum Abschluss auf **OK**. 
    
3. Aktivieren Sie das Kontrollkästchen **Keine weiteren Regeln anwenden**, um sicherzustellen, dass keine andere Regel die Umgehungsaktion umkehren kann. 
    
4. Wählen Sie für **Absenderadresse in Nachricht** die Option **Kopfzeile oder Umschlag** aus.
    
5. Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen.
    
6. Wählen Sie **Speichern** aus, um die Regel zu speichern. 
    
Nachdem Sie die Regel erstellt und erzwungen haben, wird die Spamfilterung für die angegebene Domäne oder den angegebenen Benutzer umgangen.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-that-blocks-messages-sent-from-a-domain-or-user"></a>Erstellen einer Nachrichtenfluss Regel, die Nachrichten blockiert, die von einer Domäne oder einem Benutzer gesendet werden, mithilfe der Exchange-verwaltungsKONSOLE

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**. Wählen **** ![Sie Add Add](media/ITPro-EAC-AddIcon.gif) Icon aus, und wählen Sie dann **neue Regel erstellen**aus.
    
2. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**. 
    
3. Wählen Sie unter **Diese Regel anwenden, wenn** die Option **Der Absender** und dann eine der folgenden Bedingungen aus: 
    
  - If you want to specify a domain, choose **domain is**. In the Specify domain dialog box, enter the sender domain from which you want to block messages, such as contoso.com. Klicken Sie auf Symbol](media/ITPro-EAC-AddIcon.gif) hinzufügen, um es in die Liste der Ausdrücke zu verschieben. **** ![ Repeat this step if you want to add additional domains, and click **OK** when you are finished. 
    
  - Wenn Sie einen Benutzer angeben möchten, klicken Sie auf **ist diese Person**. Fügen Sie im Dialogfeld **Mitglieder hinzufügen** den Benutzer aus der Liste hinzu, geben Sie den Benutzernamen ein, und klicken Sie auf **Namen überprüfen**. Wiederholen Sie diesen Schritt ggf. für weitere Benutzer, und klicken Sie zum Abschluss auf **OK**. 
    
4. Wählen Sie unter **Gehen Sie folgendermaßen vor** die Option **Nachricht blockieren** aus, und klicken Sie dann auf eine der anderen Optionen wie **Nachricht ohne Benachrichtigung anderer Benutzer löschen**.
    
5. Klicken Sie auf **Weitere Optionen**, und wählen Sie dann für **Absenderadresse in Nachricht** die Option **Kopfzeile oder Umschlag** aus.
    
6. Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen. Es wird empfohlen, die Regel eine Zeit lang zu testen, bevor Sie sie in Ihrer Organisation erzwingen.
    
7. Wählen Sie **Speichern** aus, um die Regel zu speichern. 
    
Nachdem Sie die Regel erstellt und erzwungen haben, werden alle von der von Ihnen angegebenen Domäne oder dem von Ihnen angegebenen Benutzer gesendeten Nachrichten blockiert.
  
## <a name="see-also"></a>Siehe auch

[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  
[Konfigurieren von Nachrichtenflussregeln zum Konfigurieren der Massen-E-Mail-Filterung](use-transport-rules-to-configure-bulk-email-filtering.md)

