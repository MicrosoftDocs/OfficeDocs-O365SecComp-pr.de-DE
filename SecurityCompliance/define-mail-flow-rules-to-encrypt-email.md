---
title: Definieren von e-Mail-Flussregeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
description: Als globaler Office 365-Administrator können Sie Mail Flow Regeln zum Aktivieren von Office 365 Message Encryption (OME) erstellen. Sie können alle ausgehenden e-Mail-Nachrichten verschlüsseln und Entfernen der Verschlüsselung aus interne Nachrichten oder Antworten auf verschlüsselte Nachrichten, die von Ihrer Organisation gesendet.
ms.openlocfilehash: 06668f29e69c885adb8c67d723efe42b4a4aa166
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529114"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a>Definieren von e-Mail-Flussregeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365

Als globaler Office 365-Administrator können Sie e-Mail-Flussregeln, auch bekannt als Transportregeln, zum Schutz von e-Mail-Nachrichten senden und empfangen erstellen. Sie können Regeln zum Verschlüsseln von ausgehenden e-Mail-Nachrichten und Entfernen der Verschlüsselung von verschlüsselten Nachrichten, die von innerhalb Ihrer Organisation oder von Antworten auf verschlüsselte Nachrichten aus Ihrer Organisation einrichten. Der Exchange-Verwaltungskonsole (EAC) oder Windows PowerShell-Cmdlets für Exchange Online können Sie um diese Regeln zu erstellen. Zusätzlich zu den allgemeinen verschlüsselungsregeln können Sie auch auswählen, aktivieren oder Deaktivieren der einzelnen Nachricht Kennwortverschlüsselungsoptionen für Endbenutzer.
  
Wenn Sie kürzlich von AD RMS in Azure Information Protection migriert, müssen Sie überprüfen Ihrer vorhandenen e-Mail-Flussregeln, um sicherzustellen, dass sie auch weiterhin in der neuen Umgebung funktionieren. Wenn Sie die neuen Office 365 Message Encryption (OME)-Funktionen Ihnen über Azure Information Protection nutzen möchten, müssen Sie darüber hinaus Ihre vorhandenen e-Mail-Flussregeln zu aktualisieren. Andernfalls erhalten Ihre Benutzer weiterhin verschlüsselten e-Mail-Nachrichten, die das vorherige HTML-Anlagenformat anstelle der neuen, nahtlosen OME-Umgebung verwendet wird. Wenn Sie OME noch eingerichtet haben, finden Sie unter [Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf der Basis Azure Information Protection](set-up-new-message-encryption-capabilities.md) Informationen. 
  
Informationen zu den Komponenten, aus denen e-Mail-Flussregeln und wie e-Mail-Fluss-Regeln funktionieren, finden Sie unter [E-Mail-Flussregeln (Transportregeln) in Exchange Online](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx). Weitere Informationen zur Funktionsweise von e-Mail-Flussregeln mit Azure Information Protection finden Sie unter [Konfigurieren von Exchange Online e-Mail-Flussregeln für Azure Information Protection Etiketten](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules).
  
## <a name="create-a-mail-flow-rule-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>Erstellen einer e-Mail-Flussregel zum Verschlüsseln von e-Mail-Nachrichten mit den neuen OME-Funktionen

Sie können e-Mail-Flussregeln zum Auslösen von Verschlüsselung von Nachrichten mit den neuen Funktionen von OME mithilfe der Exchange-Verwaltungskonsole definieren.
  
### <a name="to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities-by-using-the-eac"></a>Erstellen eine Regel zum Verschlüsseln von e-Mail-Nachrichten mit den neuen Funktionen von OME mithilfe der Exchange-Verwaltungskonsole

1. In einem Webbrowser unter Verwendung eines Kontos arbeiten oder Schule, die [Anmeldung an Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)globaler Administrator-Berechtigungen erteilt wurden.
    
2. Wählen Sie die Kachel " **Admin** ". 
    
3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.
    
4. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** \> ![New Icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) ( **neu**) \> **neue Regel erstellen**. Weitere Informationen zum Verwenden der Exchange-Verwaltungskonsole finden Sie unter [Exchange-Verwaltungskonsole in Exchange Online](https://technet.microsoft.com/library/jj200743%28v=exchg.150%29.aspx).
    
5. Geben Sie im Feld **Name**einen Namen für die Regel, z. B. e-Mails für DrToniRamos@hotmail.com verschlüsseln.
    
6. Wählen Sie unter **Diese Regel anwenden, wenn** eine Bedingung aus, und geben Sie ggf. einen Wert ein. Geben Sie beispielsweise Folgendes ein, um Nachrichten an "DrToniRamos@hotmail.com" zu verschlüsseln: 
    
    1. Wählen Sie unter **Diese Regel anwenden, wenn****the recipient is** (Der Empfänger ist) aus.
    
    2. Wählen Sie in der Kontaktliste einen vorhandenen Namen aus, oder geben Sie im Feld **Namen prüfen** eine neue E-Mail-Adresse ein. 
    
        Um einen vorhandenen Namen auszuwählen, wählen Sie ihn in der Liste aus, und klicken Sie dann auf **OK**.
    
        Geben Sie einen neuen Namen ein, geben Sie im Feld **Namen prüfen** eine e-Mail-Adresse, und wählen Sie dann auf **Namen überprüfen** \> **OK**.
    
7. Um weitere Bedingungen hinzuzufügen, wählen Sie **Weitere Optionen** und wählen Sie **Bedingung hinzufügen,** und wählen Sie aus der Liste aus. 
    
    Beispielsweise, um die Regel gelten nur, wenn der Empfänger außerhalb Ihrer Organisation befindet, wählen Sie **Bedingung hinzufügen** und die wählen Sie dann aus **der Empfänger ist extern/interne** \> **außerhalb der Organisation** \> **OK**.
    
8. Zum Aktivieren der Verschlüsselung mithilfe der neuen OME-Funktionen aus, **die folgenden Schritte aus**, wählen Sie **nachrichtensicherheit ändern** , und wählen Sie dann **Office 365-Nachrichtenverschlüsselung anwenden und Schutzrechte**. Wählen Sie eine RMS-Vorlage aus der Liste aus, wählen Sie **Speichern**, und wählen Sie dann auf **OK**.
    
    Die Liste der Vorlagen enthält alle Standardvorlagen und Optionen sowie die von denen Ihnen für erstellten benutzerdefinierten Vorlagen von Office 365 verwenden. Wenn die Liste leer ist, stellen Sie sicher, dass Sie Office 365 Message Encryption mit den neuen Funktionen eingerichtet haben wie unter [Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf den oberen Bereich des Azure Information Protection](set-up-new-message-encryption-capabilities.md)beschrieben. Informationen zu den standardmäßigen Vorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen über die Option **Nicht weiterleiten** finden Sie unter [nicht weiterleiten Option-e-Mails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Informationen über die Option **nur zu verschlüsseln** finden Sie unter [Verschlüsseln nur die Option-e-Mails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).
    
    Sie können **Aktion hinzufügen** auswählen, wenn Sie eine andere Aktion angeben möchten. 
    
### <a name="to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities-by-using-the-eac"></a>So aktualisieren Sie eine vorhandene e-Mail-Flussregel, um die neuen Funktionen von OME mithilfe der Exchange-Verwaltungskonsole

1. In einem Webbrowser unter Verwendung eines Kontos arbeiten oder Schule, die [Anmeldung an Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)globaler Administrator-Berechtigungen erteilt wurden.
    
2. Wählen Sie die Kachel " **Admin** ". 
    
3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.
    
4. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
5. Wählen Sie in der Liste der e-Mail-Flussregeln, die Regel zu ändern, um die neuen OME-Funktionen verwenden, und wählen Sie dann ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) ( **Bearbeiten**).
    
6. Zum Aktivieren der Verschlüsselung mithilfe der neuen OME-Funktionen aus, **die folgenden Schritte aus**, wählen Sie **nachrichtensicherheit ändern** , und wählen Sie dann **Office 365-Nachrichtenverschlüsselung anwenden und Schutzrechte**. Wählen Sie eine RMS-Vorlage aus der Liste aus, wählen Sie **Speichern** , und wählen Sie dann auf **OK**.
    
    Die Liste der Vorlagen enthält alle Standardvorlagen und Optionen sowie die von denen Ihnen für erstellten benutzerdefinierten Vorlagen von Office 365 verwenden. Wenn die Liste leer ist, stellen Sie sicher, dass Sie Office 365 Message Encryption mit den neuen Funktionen eingerichtet haben wie unter [Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf den oberen Bereich des Azure Information Protection](set-up-new-message-encryption-capabilities.md)beschrieben. Informationen zu den standardmäßigen Vorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen über die Option **Nicht weiterleiten** finden Sie unter [nicht weiterleiten Option-e-Mails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Informationen über die Option **nur zu verschlüsseln** finden Sie unter [Verschlüsseln nur die Option-e-Mails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).
    
    Sie können **Aktion hinzufügen** auswählen, wenn Sie eine andere Aktion angeben möchten. 
    
7. Entfernen Sie aus der Liste **gehen** alle Aktionen, die zum **Ändern der nachrichtensicherheit** zugewiesen sind \> **übernehmen die vorherige Version des OME**.
    
8. Wählen Sie **Speichern**.
    
## <a name="creating-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>Erstellen von Regeln für Office 365 Message Encryption ohne die neuen Funktionen

Wenn Sie noch nicht Office 365-Organisation auf die neuen Funktionen der OME bewegt wurden, verwenden Sie diese Aufgaben Mail Flow Regeln zum Verschlüsseln von Nachrichten für Ihre Organisation definiert. Microsoft empfiehlt, stellen Sie einen Plan für die in der neuen OME-Funktionen zu verschieben, wie es für Ihre Organisation angemessen ist. Anweisungen finden Sie unter [Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf der Basis Azure Information Protection](set-up-new-message-encryption-capabilities.md).
  
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-the-eac"></a>Erstellen eine Regel zum Verschlüsseln von e-Mail-Nachrichten, ohne die neuen Funktionen von OME mithilfe der Exchange-Verwaltungskonsole

1. In einem Webbrowser unter Verwendung eines Kontos arbeiten oder Schule, die [Anmeldung an Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)globaler Administrator-Berechtigungen erteilt wurden.
    
2. Wählen Sie die Kachel " **Admin** ". 
    
3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.
    
4. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** \> **+** ( **neu**) \> **neue Regel erstellen**. Weitere Informationen zum Verwenden der Exchange-Verwaltungskonsole finden Sie unter [Exchange-Verwaltungskonsole in Exchange Online](https://technet.microsoft.com/library/jj200743%28v=exchg.150%29.aspx).
    
5. Geben Sie im Feld **Name**einen Namen für die Regel, z. B. e-Mails für DrToniRamos@hotmail.com verschlüsseln.
    
6. Wählen Sie unter **Diese Regel anwenden, wenn** eine Bedingung aus, und geben Sie ggf. einen Wert ein. Geben Sie beispielsweise Folgendes ein, um Nachrichten an "DrToniRamos@hotmail.com" zu verschlüsseln: 
    
1. Wählen Sie unter **Diese Regel anwenden, wenn****the recipient is** (Der Empfänger ist) aus.
    
2. Wählen Sie in der Kontaktliste einen vorhandenen Namen aus, oder geben Sie im Feld **Namen prüfen** eine neue E-Mail-Adresse ein. 
    
    Um einen vorhandenen Namen auszuwählen, wählen Sie ihn in der Liste aus, und klicken Sie dann auf **OK**.
    
    Geben Sie einen neuen Namen ein, geben Sie im Feld **Namen prüfen** eine e-Mail-Adresse, und wählen Sie dann auf **Namen überprüfen** \> **OK**.
    
7. Um weitere Bedingungen hinzuzufügen, wählen Sie **Weitere Optionen** und wählen Sie dann die **Bedingung hinzufügen** aus, und wählen Sie aus der Liste aus. 
    
    Beispielsweise, um die Regel gelten nur, wenn der Empfänger außerhalb Ihrer Organisation befindet, wählen Sie **Bedingung hinzufügen** und die wählen Sie dann aus **der Empfänger ist extern/interne** \> **außerhalb der Organisation** \> **OK**.
    
8. Wählen Sie zum Aktivieren der Verschlüsselung ohne Verwendung der neuen OME-Funktionen in **die folgenden Aktionen ausführen** **Ändern nachrichtensicherheit** \> **übernehmen die vorherige Version des OME**, und wählen Sie dann auf **Speichern**.
    
    Wenn Sie eine, die IRM-Lizenzierung nicht aktiviert Fehlermeldung, und klicken Sie dann noch nicht eingerichtet werden OME für Ihre Organisation noch. Wenn Sie OME jetzt einrichten möchten, müssen Sie es einrichten, zum Verwenden der neuen OME-Funktionen. Informationen finden Sie unter [Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf der Basis Azure Information Protection](set-up-new-message-encryption-capabilities.md). Einrichten von neuen Bereitstellungen von OME ohne die neuen Funktionen wird von Microsoft nicht mehr unterstützt.
    
    Sie können **Aktion hinzufügen** auswählen, wenn Sie eine andere Aktion angeben möchten. 
    
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-windows-powershell-for-exchange-online"></a>Erstellen eine Regel zum Verschlüsseln von e-Mail-Nachrichten, ohne die neuen Funktionen von OME mithilfe von Windows PowerShell für Exchange Online

1. Verwenden von Windows PowerShell auf dem lokalen Computer eine remote-PowerShell-Sitzung zu Exchange Online zu erstellen. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).
    
2. Definieren Sie eine Regel mit dem Cmdlet **New-TransportRule** , und das **ApplyOME** -Attribut auf **true**festgelegt.
    
    Beispielsweise um erfordern, dass alle e-Mail-Nachrichten, die an DrToniRamos@hotmail.com adressiert sind verschlüsselt werden müssen, geben Sie Folgendes ein:
    
     ```
     New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
     ```

    In diesem Beispiel:
    
  - Der Name der neuen Regel ist "Verschlüsseln Regel für Dr Toni Ramos".
    
  - Der Parameter **SentTo -** gibt eine Bedingung, die für Empfänger in e-Mail-Nachrichten aussieht. Sie können einen beliebigen Wert verwenden, der den Empfänger an, wie eine e-Mail-Adresse, Name, definierten Namen (DN) usw. eindeutig identifiziert. In diesem Beispiel wird der Empfänger durch die e-Mail-Adresse "DrToniRamos@hotmail.com" identifiziert. 
    
  - Der **SentToScope -** Parameter gibt eine Bedingung, die für den Speicherort der Empfänger aussieht. In diesem Beispiel wird das Postfach des Empfängers befindet sich in Hotmail und ist nicht Bestandteil der Office 365-Organisation, sodass der Wert "NotInOrganization" verwendet wird. 
    
    Weitere Informationen über die Bedingungen, dass Sie auf e-Mail-Flussregeln mit diesem Cmdlet festlegen können finden Sie unter [New-TransportRule](https://technet.microsoft.com/en-us/library/bb125138%28v=exchg.160%29.aspx).
    
### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Entfernen der Verschlüsselung aus e-Mail-Antworten verschlüsselt werden, ohne die neuen OME-Funktionen

Wenn Ihre e-Mail-Benutzer verschlüsselte Nachrichten senden, können Empfänger dieser Nachrichten mit verschlüsselten Antworten reagieren. Sie können Mail Flow Regeln erstellen Verschlüsselung automatisch aus Antworten zu entfernen, so dass e-Mail-Benutzer in Ihrer Organisation keine Verschlüsselung-Portal anmelden, um sie anzuzeigen. Die Exchange-Verwaltungskonsole oder Windows PowerShell-Cmdlets können Sie diese Regeln zu definieren. Wenn Sie noch nicht die neuen OME-Funktionen verwenden, können Sie nur Nachrichten entschlüsseln, die entweder aus gesendet, in Ihrer Organisation oder Antworten auf Nachrichten, die von innerhalb Ihrer Organisation gesendet werden. Verschlüsselte Nachrichten, die von außerhalb der Organisation stammen nicht entschlüsselt werden.
  
#### <a name="to-create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-the-eac"></a>Erstellen eine Regel zum Entfernen der Verschlüsselung aus e-Mail-Antworten verschlüsselt ohne die neuen Funktionen von OME mithilfe der Exchange-Verwaltungskonsole
<a name="DecryptruleEACNoNewOME"> </a>

1. In einem Webbrowser unter Verwendung eines Kontos arbeiten oder Schule, die [Anmeldung an Office 365](https://support.office.com/article/Sign-in-to-Office-or-Office-365-b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)Administratorberechtigungen erteilt wurden.
    
2. Wählen Sie die Kachel " **Admin** ". 
    
3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.
    
4. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** \> **+** ( **neu**) \> **neue Regel erstellen**. Weitere Informationen zum Verwenden der Exchange-Verwaltungskonsole finden Sie unter [Exchange-Verwaltungskonsole in Exchange Online](https://technet.microsoft.com/en-us/library/jj200743%28v=exchg.150%29.aspx).
    
5. Geben Sie im Feld **Name**einen Namen für die Regel, z. B. Entfernen der Verschlüsselung von eingehender e-Mail.
    
6. Wählen Sie in **diese Regel anwenden, wenn** die Bedingungen, auf dem Verschlüsselung aus Nachrichten wie **der Empfänger befindet** entfernt werden sollten \> **innerhalb der Organisation**.
    
7. Wählen Sie in **der folgenden Schritte aus**, **Ändern nachrichtensicherheit** \> **die vorherige Version des OME zu entfernen**.
    
8. Klicken Sie auf **Speichern**.
    
#### <a name="to-create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-windows-powershell-for-exchange-online"></a>Erstellen eine Regel zum Entfernen der Verschlüsselung aus e-Mail-Antworten verschlüsselt ohne die neuen Funktionen von OME mithilfe von Windows PowerShell für Exchange Online
<a name="DecryptrulePShellNoNewOME"> </a>

1. Verwenden von Windows PowerShell auf dem lokalen Computer eine remote-PowerShell-Sitzung zu Exchange Online zu erstellen. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).
    
2. Definieren Sie eine Regel mit dem Cmdlet **New-TransportRule** , und das **RemoveOME** -Attribut auf **true**festgelegt.
    
    Angenommen, um die Verschlüsselung von Nachrichten an Empfänger in Office 365-Organisation zu entfernen, geben Sie Folgendes ein:
    
     ```
     New-TransportRule - Name "Remove encryption from incoming mail"     -SentToScope "InOrganization" -RemoveOME $true
     ```

    In diesem Beispiel:
    
  - Der Name der neuen Regel ist "Remove-Verschlüsselung von eingehende e-Mail".
    
  - Der **SentToScope -** Parameter gibt eine Bedingung, die für den Speicherort der Empfänger aussieht. In diesem Beispiel wird der Wert "InOrganization" verwendet, die angibt: 
    
  - Der Empfänger ist ein Postfach, e-Mail-Benutzer, Gruppe oder e-Mail-aktivierte Öffentliche Ordner in Ihrer Organisation oder
    
  - Die E-Mail-Adresse des Empfängers befindet sich in einer akzeptierten Domäne, die als autorisierende Domäne oder interne Relaydomäne konfiguriert ist, und die Nachricht wurde über eine authentifizierte Verbindung gesendet oder empfangen.
    
    Weitere Informationen über die Bedingungen, dass Sie auf e-Mail-Flussregeln mit diesem Cmdlet festlegen können finden Sie unter [New-TransportRule](https://technet.microsoft.com/en-us/library/bb125138%28v=exchg.160%29.aspx).
    
## <a name="related-topics"></a>Verwandte Themen

[Verschlüsselung in Office 365](encryption.md)
  
[Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf der Basis Azure Information Protection](set-up-new-message-encryption-capabilities.md)
  
[Hinzufügen von Branding zu verschlüsselten Nachrichten](add-your-organization-brand-to-encrypted-messages.md)
  
[Nachrichtenflussregeln (Transportregeln) in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=506707)
  
[Nachrichtenflussregeln (Transportregeln) in Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=506708)
  

