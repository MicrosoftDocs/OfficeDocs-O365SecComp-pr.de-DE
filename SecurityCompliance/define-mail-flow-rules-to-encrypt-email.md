---
title: Definieren von Nachrichtenflussregeln zum Verschlüsseln von E-Mail-Nachrichten in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
ms.collection:
- M365-security-compliance
description: Administratoren können Informationen zum Erstellen von Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) zum Verschlüsseln und Entschlüsseln von Nachrichten mit der Office 365-Nachrichtenverschlüsselung (OM) erlernen.
ms.openlocfilehash: f76abe2d341b9e3677a90d447e70f6091e3a91cc
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276205"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a>Definieren von Nachrichtenflussregeln zum Verschlüsseln von E-Mail-Nachrichten in Office 365

Als globaler Office 365-Administrator können Sie Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) erstellen, um e-Mail-Nachrichten, die Sie senden und empfangen, zu schützen. Sie können Regeln einrichten, um ausgehende e-Mail-Nachrichten zu verschlüsseln und die Verschlüsselung von verschlüsselten Nachrichten aus Ihrer Organisation oder von Antworten auf verschlüsselte Nachrichten von Ihrer Organisation zu entfernen. Sie können die Exchange-Verwaltungskonsole (EAC) oder Exchange Online PowerShell verwenden, um diese Regeln zu erstellen. Zusätzlich zu den allgemeinen Verschlüsselungsregeln können Sie auch einzelne Nachrichten Verschlüsselungsoptionen für Endbenutzer aktivieren oder deaktivieren.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||

Wenn Sie kürzlich von AD RMS zu Azure Information Protection migriert haben, müssen Sie Ihre vorhandenen Nachrichtenfluss Regeln überprüfen, um sicherzustellen, dass Sie weiterhin in ihrer neuen Umgebung funktionieren. Darüber hinaus müssen Sie die vorhandenen Nachrichtenfluss Regeln aktualisieren, wenn Sie die neuen Funktionen von Office 365 Message Encryption (OM) nutzen möchten, die Ihnen über Azure Information Protection zur Verfügung stehen. Andernfalls erhalten Ihre Benutzer weiterhin verschlüsselte e-Mails, die das vorherige HTML-Anlagenformat anstelle der neuen, nahtlosen OM-Umgebung verwenden. Wenn Sie noch nicht eingerichtet haben, finden Sie weitere Informationen unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md) .

Informationen zu den Komponenten, die e-Mail-Flussregeln bilden, und zur Funktionsweise von Nachrichtenfluss Regeln finden Sie unter [Mail Flow Rules (Transport Rules) in Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules). Weitere Informationen zur Funktionsweise von Nachrichtenfluss Regeln mit Azure Information Protection finden Sie unter [Configuring Exchange Online Mail Flow Rules for Azure Information Protection Labels](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules).

> [!IMPORTANT]
> Bei Hybriden Exchange-Umgebungen können lokale Benutzer verschlüsselte e-Mails nur über OM senden, wenn e-Mails über Exchange Online weitergeleitet werden. Um om in einer hybriden Exchange-Umgebung zu konfigurieren, müssen Sie zunächst [Hybrid mit dem Assistenten für die Hybrid Konfiguration konfigurieren](https://docs.microsoft.com/Exchange/exchange-hybrid) und anschließend [Mail für den Fluss von Ihrem e-Mail-server zu Office 365 konfigurieren](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365). Nachdem Sie e-Mail-Nachrichten für den Fluss über Office 365 konfiguriert haben, können Sie mithilfe dieser Anleitung Nachrichtenfluss Regeln für OM konfigurieren.

## <a name="create-mail-flow-rules-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>Erstellen von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten mit den neuen OM-Funktionen

Mithilfe der Exchange-verwaltungsKONSOLE können Sie e-Mail-Flussregeln zum Auslösen der Nachrichtenverschlüsselung mit den neuen OM-Funktionen definieren.

### <a name="use-the-eac-to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities"></a>Erstellen einer Regel zum Verschlüsseln von e-Mail-Nachrichten mit den neuen OM-Funktionen mithilfe der Exchange-verwaltungsKONSOLE

1. Melden Sie sich in einem Webbrowser bei einem Arbeits-oder Schulkonto, dem globale Administratorberechtigungen erteilt wurden, bei [Office 365 an](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Wählen Sie die Kachel **Admin** aus.

3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.

4. Wechseln Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** , und wählen Sie **Neues** ![neues Symbol](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Erstellen**aus. Weitere Informationen zur Verwendung der EAC finden Sie unter [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Geben Sie unter **Name**einen Namen für die Regel ein, beispielsWeise Verschlüsseln von e-mails für DrToniRamos@hotmail.com.

6. Wählen Sie unter **Diese Regel anwenden, wenn** eine Bedingung aus, und geben Sie ggf. einen Wert ein. Geben Sie beispielsweise Folgendes ein, um Nachrichten an "DrToniRamos@hotmail.com" zu verschlüsseln:

   1. Wählen Sie unter **Diese Regel anwenden, wenn****the recipient is** (Der Empfänger ist) aus.

   2. Wählen Sie in der Kontaktliste einen vorhandenen Namen aus, oder geben Sie im Feld **Namen prüfen** eine neue E-Mail-Adresse ein.

      - Um einen vorhandenen Namen auszuwählen, wählen Sie ihn in der Liste aus, und klicken Sie dann auf **OK**.

      - Geben Sie eine e-Mail-Adresse in das Feld **Namen überprüfen** ein, und wählen Sie dann **** **Namen** \> überprüfen aus, um einen neuen Namen einzugeben.

7. Klicken Sie zum Hinzufügen weiterer Bedingungen auf **Weitere Optionen** , und wählen Sie dann **Bedingung hinzufügen** aus, und wählen Sie in der Liste aus.

   Wenn Sie beispielsweise die Regel nur anwenden möchten, wenn sich der Empfänger außerhalb Ihrer Organisation befindet, wählen Sie **Bedingung hinzufügen** aus, und wählen Sie dann **den Empfänger ist extern/intern** \> **außerhalb der Organisation** \> **** aus.

8. Wenn Sie die Verschlüsselung mithilfe der neuen OM-Funktionen aktivieren möchten, wählen Sie nach **folgend**die Option **Nachrichtensicherheit ändern** aus, und wählen Sie dann **Office 365 Nachrichtenverschlüsselung und Rechte Schutz anwenden**aus. Wählen Sie in der Liste eine RMS-Vorlage aus, klicken Sie auf **Speichern**und dann auf **OK**.
  
  Die Liste der Vorlagen enthält alle Standardvorlagen und-Optionen sowie alle benutzerdefinierten Vorlagen, die Sie für Office 365 erstellt haben. Wenn die Liste leer ist, stellen Sie sicher, dass Sie die Office 365-Nachrichtenverschlüsselung mit den neuen Funktionen eingerichtet haben, wie unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md)beschrieben. Informationen zu den Standardvorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen zur Option " **nicht weiterleiten** " finden Sie unter [do not Forward Option for Emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Informationen zur Option **nur** verschlüsseln finden Sie unter [Encrypt only Option for Emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

  Wenn Sie eine andere Aktion angeben möchten, können Sie **Aktion hinzufügen** auswählen.

### <a name="use-the-eac-to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities"></a>Verwenden der Exchange-verwaltungsKONSOLE zum Aktualisieren einer vorhandenen e-Mail-Fluss Regel zur Verwendung der neuen OM-Funktionen

1. Melden Sie sich in einem Webbrowser bei einem Arbeits-oder Schulkonto, dem globale Administratorberechtigungen erteilt wurden, bei [Office 365 an](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Wählen Sie die Kachel **Admin** aus.

3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.

4. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.

5. Wählen Sie in der Liste der Nachrichtenfluss Regeln die Regel aus, die Sie ändern möchten, um die neuen OM-Funktionen **** ![zu verwenden,](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)und wählen Sie dann Bearbeitungssymbol bearbeiten aus.

6. Wenn Sie die Verschlüsselung mithilfe der neuen OM-Funktionen aktivieren möchten, wählen Sie nach **folgend**die Option **Nachrichtensicherheit ändern** und dann auf **Office 365 Nachrichtenverschlüsselung und Rechte Schutz anwenden**aus. Wählen Sie in der Liste eine RMS-Vorlage aus, klicken Sie auf **Speichern** und dann auf **OK**.

   Die Liste der Vorlagen enthält alle Standardvorlagen und-Optionen sowie alle benutzerdefinierten Vorlagen, die Sie für Office 365 erstellt haben. Wenn die Liste leer ist, stellen Sie sicher, dass Sie die Office 365-Nachrichtenverschlüsselung mit den neuen Funktionen eingerichtet haben, wie unter [Einrichten der neuen office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren](set-up-new-message-encryption-capabilities.md). Informationen zu den Standardvorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen zur Option " **nicht weiterleiten** " finden Sie unter [do not Forward Option for Emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Informationen zur Option **nur** verschlüsseln finden Sie unter [Encrypt only Option for Emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

   Wenn Sie eine andere Aktion angeben möchten, können Sie **Aktion hinzufügen** auswählen.

7. Entfernen Sie in der **folgenden** Liste alle Aktionen, die zum **Ändern der Nachrichtensicherheit** \> zugewiesen sind, **wenden Sie die frühere Version von OM**an.

8. Klicken Sie auf **Save**.

## <a name="create-mail-flow-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>Erstellen von Nachrichtenübermittlungs Regeln für die Office 365-Nachrichtenverschlüsselung ohne die neuen Funktionen

Wenn Sie Ihre Office 365-Organisation noch nicht in die neuen OM-Funktionen verschoben haben, können Sie mithilfe dieser Aufgaben Nachrichtenfluss Regeln definieren, um Nachrichten für Ihre Organisation zu verschlüsseln. Microsoft empfiehlt, einen Plan für die Umstellung auf die neuen Funktionen von OM zu erstellen, sobald es für Ihre Organisation sinnvoll ist. Anweisungen hierzu finden Sie unter [Einrichten neuer Office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren](set-up-new-message-encryption-capabilities.md).

### <a name="use-the-eac-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a>Erstellen einer Nachrichtenfluss Regel zum Verschlüsseln von e-Mail-Nachrichten ohne die neuen OM-Funktionen mithilfe der Exchange-verwaltungsKONSOLE

1. Melden Sie sich in einem Webbrowser bei einem Arbeits-oder Schulkonto, dem globale Administratorberechtigungen erteilt wurden, bei [Office 365 an](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Wählen Sie die Kachel **Admin** aus.

3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.

4. Wechseln Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** , und wählen Sie **Neues** ![neues Symbol](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Erstellen**aus. Weitere Informationen zur Verwendung der EAC finden Sie unter [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Geben Sie unter **Name**einen Namen für die Regel ein, beispielsWeise Verschlüsseln von e-mails für DrToniRamos@hotmail.com.

6. Wählen Sie unter **Diese Regel anwenden, wenn** eine Bedingung aus, und geben Sie ggf. einen Wert ein. Geben Sie beispielsweise Folgendes ein, um Nachrichten an "DrToniRamos@hotmail.com" zu verschlüsseln:

   1. Wählen Sie unter **Diese Regel anwenden, wenn****the recipient is** (Der Empfänger ist) aus.

   2. Wählen Sie in der Kontaktliste einen vorhandenen Namen aus, oder geben Sie im Feld **Namen prüfen** eine neue E-Mail-Adresse ein.

      - Um einen vorhandenen Namen auszuwählen, wählen Sie ihn in der Liste aus, und klicken Sie dann auf **OK**.

      - Geben Sie eine e-Mail-Adresse in das Feld **Namen überprüfen** ein, und wählen Sie dann **** **Namen** \> überprüfen aus, um einen neuen Namen einzugeben.

7. Klicken Sie zum Hinzufügen weiterer Bedingungen auf **Weitere Optionen** , und wählen Sie dann **Bedingung hinzufügen** aus, und wählen Sie in der Liste aus.

   Wenn Sie beispielsweise die Regel nur anwenden möchten, wenn sich der Empfänger außerhalb Ihrer Organisation befindet, wählen Sie **Bedingung hinzufügen** aus, und wählen Sie dann **den Empfänger ist extern/intern** \> **außerhalb der Organisation** \> **** aus.

8. Um die Verschlüsselung zu aktivieren, ohne die neuen Funktionen von OM zu verwenden, wählen Sie im **folgenden ausführen**die Option **Nachrichtensicherheit** \> **Anwenden der vorherigen Version von OM**ändern aus, und wählen Sie dann **Speichern**aus.

  Wenn Sie eine Fehlermeldung erhalten, dass die IRM-Lizenzierung nicht aktiviert ist, haben Sie noch keine OM für Ihre Organisation eingerichtet. Wenn Sie jetzt OM einrichten möchten, müssen Sie es einrichten, um die neuen OM-Funktionen zu verwenden. Weitere Informationen finden Sie unter [Einrichten neuer Office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren](set-up-new-message-encryption-capabilities.md). Microsoft unterstützt nicht mehr das Einrichten neuer Bereitstellungen von OM ohne die neuen Funktionen.

  Wenn Sie eine andere Aktion angeben möchten, können Sie **Aktion hinzufügen** auswählen.

### <a name="use-exchange-online-powershell-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities"></a>Verwenden von Exchange Online PowerShell zum Erstellen einer e-Mail-Fluss Regel zum Verschlüsseln von e-Mail-Nachrichten ohne die neuen OM-Funktionen

1. Stellen Sie eine Verbindung mit Exchange Online PowerShell her. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

2. Erstellen Sie mithilfe des Cmdlets **New-TransportRule** eine Regel, und legen Sie `$true`den Parameter _ApplyOME_ auf fest.

   In diesem Beispiel müssen alle an DrToniRamos@hotmail.com gesendeten e-Mail-Nachrichten verschlüsselt werden.

   ```powershell
   New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
   ```

   **Hinweise**:

   - Der eindeutige Name der neuen Regel lautet "Verschlüsselungs Regel für Dr. Toni Ramos".

   - Der Parameter _SentTo_ gibt die Nachrichtenempfänger an (identifiziert durch den Namen, die e-Mail-Adresse, den Distinguished Name usw.). In diesem Beispiel wird der Empfänger durch die e-Mail-Adresse "DrToniRamos@hotmail.com" identifiziert.

   - Der Parameter _SentToScope_ gibt den Speicherort der Nachrichtenempfänger an. In diesem Beispiel befindet sich das Postfach des Empfängers in Hotmail und ist nicht Teil der Office 365-Organisation, daher wird `NotInOrganization` der Wert verwendet.

   Detaillierte Informationen zur Syntax und den Parametern finden Sie unter [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).

### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Entfernen der Verschlüsselung von e-Mail-Antworten ohne die neuen OM-Funktionen

Wenn Ihre e-Mail-Benutzer verschlüsselte Nachrichten senden, können Empfänger dieser Nachrichten mit verschlüsselten Antworten Antworten. Sie können Nachrichtenfluss Regeln erstellen, um die Verschlüsselung aus Antworten automatisch zu entfernen, sodass sich e-Mail-Benutzer in Ihrer Organisation nicht beim Verschlüsselungs Portal anmelden müssen, um Sie anzuzeigen. Sie können die Exchange-verwaltungsKONSOLE oder Windows PowerShell-Cmdlets verwenden, um diese Regeln zu definieren. Wenn Sie die neuen OM-Funktionen noch nicht verwenden, können Sie nur Nachrichten entschlüsseln, die in Ihrer Organisation oder Nachrichten gesendet werden, die Antworten auf Nachrichten aus Ihrer Organisation senden. Sie können keine verschlüsselten Nachrichten entschlüsseln, die von außerhalb Ihrer Organisation stammen.

#### <a name="use-the-eac-to-create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Erstellen einer Regel zum Entfernen der Verschlüsselung aus e-Mail-Antworten ohne die neuen OM-Funktionen mithilfe der Exchange-verwaltungsKONSOLE

1. Melden Sie sich in einem Webbrowser bei einem Arbeits-oder Schulkonto, dem Administratorberechtigungen erteilt wurden, bei [Office 365 an](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Wählen Sie die Kachel **Admin** aus.

3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.

4. Wechseln Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** , und wählen Sie **Neues** ![neues Symbol](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Erstellen**aus. Weitere Informationen zur Verwendung der EAC finden Sie unter [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Geben Sie unter **Name**einen Namen für die Regel ein, beispielsweise Verschlüsselung von eingehenden e-Mails entfernen.

6. Wählen Sie unter **diese Regel anwenden, wenn** die Bedingungen auswählen, unter denen die Verschlüsselung aus Nachrichten entfernt werden soll, wie **der Empfänger sich** \> **innerhalb der Organisation**befindet.

7. Wählen Sie unter **folgende Aktion**die Option **Nachrichtensicherheit** \> **Entfernen der vorherigen Version von OM**aus.

8. Wählen Sie **Speichern** aus.

#### <a name="use-exchange-online-powershell-to-create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Verwenden von Exchange Online PowerShell zum Erstellen einer Regel zum Entfernen der Verschlüsselung aus e-Mail-Antworten ohne die neuen OM-Funktionen

1. Stellen Sie eine Verbindung mit Exchange Online PowerShell her. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

2. Erstellen Sie mithilfe des Cmdlets **New-TransportRule** eine Regel, und legen Sie `$true`den Parameter _RemoveOME_ auf fest.

   In diesem Beispiel wird die Verschlüsselung aller e-Mails, die an Empfänger in der Office 365-Organisation gesendet wurden, entfernt.

   ```powershell
   New-TransportRule -Name "Remove encryption from incoming mail" -SentToScope "InOrganization" -RemoveOME $true
   ```

   **Hinweise**:

   - Der eindeutige Name der neuen Regel lautet "Entfernen der Verschlüsselung von eingehenden e-Mails".

   - Der Parameter _SentToScope_ gibt den Speicherort der Nachrichtenempfänger an. In diesem Beispiel wird der Value `InOrganization` -Wert verwendet, der angibt:

     - Der Empfänger ist ein Postfach, ein e-Mail-Benutzer, eine Gruppe oder ein e-Mail-aktivierter Öffentlicher Ordner in Ihrer Organisation.

       oder

     - Die e-Mail-Adresse des Empfängers befindet sich in einer akzeptierten Domäne, die als autorisierende Domäne oder als interne Relay-Domäne in Ihrer Organisation konfiguriert ist, _und_ die Nachricht wurde über eine authentifizierte Verbindung gesendet oder empfangen.

Detaillierte Informationen zur Syntax und den Parametern finden Sie unter [New-TransportRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/New-TransportRule).

## <a name="related-topics"></a>Verwandte Themen

[Verschlüsselung in Office 365](encryption.md)

[Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md)

[Hinzufügen von Branding zu verschlüsselten Nachrichten](add-your-organization-brand-to-encrypted-messages.md)

[Nachrichtenflussregeln (Transportregeln) in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=506707)

[Nachrichtenflussregeln (Transportregeln) in Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=506708)
