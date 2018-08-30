---
title: Verhindern Sie, dass e-Mail als Spam in Office 365 und Exchange Online Protection markiert wird
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 74aaade0-efc0-46ac-b949-f2d1d59256fa
description: Tipps für Office 365-Administratoren, die verhindern, dass eine gute e-Mail als Spam isoliert werden als falsch positiv Unzustellbarkeitsberichte markiert. Anpassen von einer von Listen sicherer Adressen und andere Optionen, um zu verhindern, dass eine gute e-Mail als Spam gekennzeichnet.
ms.openlocfilehash: 42b27d237592e95e6d175ab335959bc82269c0f7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528937"
---
# <a name="prevent-email-from-being-marked-as-spam-in-office-365-and-exchange-online-protection"></a>Verhindern Sie, dass e-Mail als Spam in Office 365 und Exchange Online Protection markiert wird

Exchange Online oder Exchange Online Protection (EOP) Administratoren mit Anmeldeinformationen für den entsprechenden Zugriff können folgendermaßen verwenden, um sicherzustellen, dass eine e-Mail-Nachricht über den Dienst auf Reisen als Spam gekennzeichnet ist nicht.
  
Es kann sehr gut, legitime e-Mail unter Quarantäne gestellte e-Mails oder blockiert werden, als spam und in einem Quarantäneordner Zielseite haben ärgerlich sein. Sie können eine Liste sicherer Absender oder eine e-Mail-Flussregel umgehen der Spamfilterung und verhindern, dass eine gute e-Mail-Nachrichten als Junk-e-Mail markiert. Wenn eine Nachricht durch den Spamfilter falsch als Spam markiert ist, wird dies als falsch positives Ergebnis bezeichnet. Der Office 365-Spam-Filter außerdem einige Optionen, die Endbenutzer anpassen können, um falsch positive Ergebnisse zu verhindern.
  
Wenn Sie Hilfe mit falsch negativen e-Mail-Nachrichten suchen d. h., Spam Ruft eine Meldung ab, die über Wenn es sollte nicht, die Tipps in [e-Mail-Nachrichten mit dem Office 365-Spam-Filter auf false negative Probleme zu verhindern, dass spam blockieren](block-email-spam-to-prevent-false-negatives.md)Auschecken.
  
## <a name="eop-only-customers-use-directory-synchronization"></a>Nur EOP-Kunden: verzeichnissynchronisierung

EOP ist ein Cloud-basierte e-Mail-filterdiensts, die Ihre Organisation vor Spam und Malware geschützt. Wenn Sie Postfächer in Office 365 verfügen, werden sie automatisch von EOP geschützt, da er Teil des Diensts ist. 
  
Wenn Sie einen nur EOP-Kunden sind, d. h., die EOP-Diensts für die Verwendung mit Ihrem lokalen Exchange-Server abonnieren, sollten Sie benutzereinstellungen mit dem Dienst mithilfe von verzeichnissynchronisierung synchronisieren. Dadurch wird sichergestellt, dass Ihre sichere Absender, die Listen von EOP eingehalten werden. Weitere Informationen finden Sie unter "verzeichnissynchronisierung zum Verwalten von e-Mail-Benutzer" in [Manage Mail Users in EOP](https://go.microsoft.com/fwlink/?LinkId=534098).
  
## <a name="prevent-false-positive-email-by-using-the-connection-filters-ip-allow-list"></a>Verhindern, dass falsch positive e-Mail mithilfe der Verbindungs des Filters IP-Zulassungsliste

Wenn Sie feststellen, dass e-Mail des Absenders wird immer auf die Junk-e-Ordner in Ihrer Organisation verschoben, können Sie die IP-Adresse der e-Mail-Adresse des Absenders in der Verbindungsfilter-IP-Adresse hinzufügen Zulassungsliste. Normalerweise wird dies verhindert, dass false positive Antworten für diesen Absender für alle Empfänger in Ihrer Organisation. Die Ausnahme ist, wenn ein Benutzer die Option ermöglicht "listet nur sichere: nur Nachrichten von Personen und Domänen in Ihrer Liste sicherer Absender oder die Liste sicherer Empfänger übermittelt werden an Ihren Posteingang" in Outlook und der Absender zur Liste sicherer Absender werden nicht hinzugefügt. Informationen zum Überschreiben dieser Option finden Sie unter [Problembehandlung: eine Nachricht endet im Ordner Junk, obwohl EOP die Nachricht als nicht-Spam markiert](prevent-email-from-being-marked-as-spam-0.md#TroubleshootingJunkEOPNonSpam).
  
 **Eine IP-Adresse hinzu, die Verbindung des Filters-IP-Zulassungsliste**
  
1. Abrufen der Kopfzeile auf eine Nachricht vom Absender, den Sie zulassen möchten. Sie können Ihre e-Mail-Client wie Outlook oder Outlook im Web dazu gemäß [Nachricht Kopfzeile Analyzer](https://go.microsoft.com/fwlink/p/?LinkId=306583).
    
2. Suchen Sie manuell für die IP-Adresse der CIP Kategorie in der Kopfzeile X-Forefront-Antispam-Report oder mithilfe der Registerkarte **Nachricht Analyzer** von [Remote Connectivity Analyzer](https://testconnectivity.microsoft.com/?tabid=mha)folgen.
    
3. Hinzufügen die IP-Adresse die IP-Adresse Zulassungsliste durch die Schritte unter "Verwenden der Exchange-Verwaltungskonsole zum Bearbeiten der Standardrichtlinie für Verbindungsfilter" unter [Konfigurieren der verbindungsfilterrichtlinie](https://go.microsoft.com/fwlink/?LinkId=534132).
    
## <a name="prevent-false-positive-email-by-configuring-spam-filter-policies"></a>Verhindern Sie falsch positive e-Mail, indem Sie Konfigurieren von Richtlinien für Spam-filter

Durch die Schritte in [Ihrer Spam-Filter-Richtlinien konfigurieren](https://go.microsoft.com/fwlink/?LinkID=534136)können Sie eine Liste zugelassener Domänen oder einzelne e-Mail-Adressen hinzufügen.
  
## <a name="review-your-advanced-spam-filter-policies"></a>Überprüfen Sie Ihre erweiterte Spam-Filter-Richtlinien

Wenn Sie besondere Einschränkungen in einer Spam-Filter-Richtlinie, beispielsweise eingerichtet haben, wenn Sie eine gesamte Domäne blockiert haben, sollten Sie überprüfen, um zu überprüfen, ob sie falsch positive Ergebnisse verursachen können. Finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](https://go.microsoft.com/fwlink/?LinkId=534136), und deaktivieren Sie zusätzliche [Optionen für erweiterte Spamfilterung](https://go.microsoft.com/fwlink/?LinkId=534137) , die Nachrichten als Spam gekennzeichnet werden verursachen könnten. 
  
## <a name="help-your-end-users-create-a-safe-sender-list-to-prevent-good-email-from-being-marked-as-spam"></a>Erstellen einer Liste sicherer Absender, um zu verhindern, dass eine gute e-Mail als Spam markiert wird Endbenutzer-Hilfe
<a name="BKMK_email-user-help-safelist"> </a>

Weisen Sie die Benutzer an-Adressen von Absendern hinzuzufügen, die sie zu ihrer Liste sicherer Absender in [Outlook](https://go.microsoft.com/fwlink/p/?LinkId=270065) oder [Outlook im Web](https://go.microsoft.com/fwlink/p/?LinkId=294862)vertrauen. Wählen Sie in Outlook im Web Einstieg **Einstellungen**![ConfigureAPowerBIAnalysisServicesConnector_settingsIcon](media/24bd5467-c8d2-4936-9c37-a179bd0e21ec.png) \> **Optionen** \> **Blockieren oder Zulassen von**. Das folgende Diagramm zeigt ein Beispiel für etwas zu einer Liste sicherer Absender hinzufügen.
  
![Einen sicheren Absender hinzufügen in Outlook Web App](media/8de6b24e-429e-4e8f-8ce8-53ba659cbfcb.png)
  
EOP berücksichtigt Ihrer Benutzer sichere Absender und Empfänger, aber nicht sichere Domänen. Dies gilt unabhängig davon, ob die Domäne hinzugefügt, über die Outlook im Web oder in Outlook hinzugefügt und mit der Verzeichnissynchronisierung synchronisiert.
  
## <a name="troubleshooting-a-message-ends-up-in-the-junk-folder-even-though-eop-marked-the-message-as-non-spam"></a>Problembehandlung: Eine Nachricht endet im Ordner Junk, obwohl EOP die Nachricht als nicht-Spam markiert
<a name="TroubleshootingJunkEOPNonSpam"> </a>

Wenn Ihre Benutzer die Option in Outlook für aktiviert haben "listet nur sichere: nur Nachrichten von Personen und Domänen in Ihrer Liste sicherer Absender oder die Liste sicherer Empfänger übermittelt werden an Ihren Posteingang", fahren Sie alle e-Mail-Nachrichten in den Junk-e-Ordner für ein Absender wird, sofern der Absender in der EMP ist Liste mit sicheren Absendern des Pient. Dies geschieht unabhängig davon, ob EOP eine Nachricht als nicht-Spam markiert oder wenn Sie eine Regel in EOP eingerichtet haben, um eine Nachricht als nicht-Spam markieren.
  
Sie können die Option nur sichere Absender für Ihre Benutzer Outlook deaktivieren, indem Sie wie im folgenden beschrieben [Outlook: richtlinieneinstellung Deaktivieren der Junk-e-Mail-Benutzeroberfläche und Filtern von Mechanismus](https://support.microsoft.com/en-us/kb/2180568).
  
Wenn Sie die Nachricht in Outlook im Web anzeigen, wird ein gelbes Safety Tipp, der angibt, dass die Nachricht im Ordner Junk, da der Absender nicht in der Liste der sicheren Absender des Empfängers ist vorhanden sein.
  
Wenn Sie die Kopfzeile einer Nachricht betrachten, kann es unter anderem Stempel sfv (zugelassene IP-Adressen oder ETR zulassen) oder SFV:NSPM (nicht-Spam), jedoch die Nachricht ist noch in den Ordner des Benutzers Junk-e-abgelegt. Es gibt nichts in der Kopfzeile der Nachricht, die angibt, dass der Benutzer "Nur sichere Absender" aktiviert hat. In diesem Fall, da die Option "Nur sichere Absender" Festlegen von Benutzern in Outlook die EOP-Einstellung überschreibt. 
  
 **So überprüfen Sie wird warum ein sicherer Absender eine Nachricht als nicht-Spam in der Kopfzeile der Nachricht, aber dennoch enden in den Ordner des Benutzers Junk gekennzeichnet**
  
1. Herstellen einer Verbindung mit Exchange Online PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). 
    
2. Führen Sie den folgenden Befehl zum Anzeigen von den Einstellungen des Benutzers junk-e-Mail-Konfiguration aus:
    
  ```
  Get-MailboxJunkEmailConfiguration example@contoso.com | fl TrustedListsOnly,ContactsTrusted,TrustedSendersAndDomains
  ```

    Wenn TrustedListsOnly auf True festgelegt ist, bedeutet dies, dass diese Einstellung aktiviert ist. Wenn ContactsTrusted auf True festgelegt ist, bedeutet dies, dass der Benutzer, Kontakte und sichere Absender vertraut. Die TrustedSendersAndDomains wird der Inhalt der Liste sicherer Absender des Benutzers aufgelistet.
    
## <a name="still-need-help"></a>Benötigen Sie weitere Hilfe?
<a name="TroubleshootingJunkEOPNonSpam"> </a>

[![Erhalten von Hilfe in den Communityforen von Office 365](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Administratoren: Anmelden und Serviceanfrage erstellen](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Administratoren: Support kontaktieren](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  
## <a name="see-also"></a>Siehe auch
<a name="TroubleshootingJunkEOPNonSpam"> </a>

[Übersicht über den Junk-e-Mail-Filter](https://support.office.com/article/5AE3EA8E-CF41-4FA0-B02A-3B96E21DE089)
  
[Blockieren Sie oder zulassen Sie (junk-e-Mail-Einstellungen)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](block-email-spam-to-prevent-false-negatives.md)

