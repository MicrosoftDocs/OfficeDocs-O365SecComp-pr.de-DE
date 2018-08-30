---
title: Null-Stunden automatisch löschen - Schutz vor Spam und malware
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: Null-Stunden automatisch löschen (ZAP) ist eine e-Mail-Schutz-Funktion, die Nachrichten mit Spam oder Schadsoftware erkannt, die bereits an die Posteingänge der Benutzer gesendet wurden, und klicken Sie dann den schädlichem Inhalt unschädlichen rendert. Wie ZAP dies funktioniert, hängt von den Typ des schädlichem Inhalt erkannt.
ms.openlocfilehash: dc8901dc7c1db5b323ccbeee610647b8a302fcb3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529055"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Null-Stunden automatisch löschen - Schutz vor Spam und malware

Null-Stunden automatisch löschen (ZAP) ist eine e-Mail-Schutz-Funktion, die Nachrichten mit Spam oder Schadsoftware erkannt, die bereits an die Posteingänge der Benutzer gesendet wurden, und klicken Sie dann den schädlichem Inhalt unschädlichen rendert. Wie ZAP dies funktioniert, hängt von den Typ des schädlichem Inhalt erkannt.
  
ZAP ist mit Exchange Online Protection, die mit einem beliebigen Office 365-Abonnement enthalten ist, die Exchange Online-Postfächer enthält standardmäßig verfügbar.
  
## <a name="how-does-zap-work"></a>Wie funktioniert ZAP?

Office 365 aktualisiert Anti-Spam-Modul- und Malware-Signaturen in Echtzeit auf täglicher Basis. Jedoch könnte die Benutzer weiterhin bösartige Nachrichten an ihre Posteingänge für eine Vielzahl von Gründe, wenn der Inhalt weaponized wurde zu einem Zeitpunkt, nachdem es zuerst an Benutzer übermittelt wurde erhalten. Entfernen von Adressen dies durch die Überwachung ständig mit Office 365 Spam und Malware Signaturen, aktualisiert können und daher suchen und Entfernen zuvor bereitgestellte Nachrichten bereits im Posteingang. Für e-Mail-Nachrichten, die bereits als Spam erkannt wurde, verschiebt ZAP ungelesene Nachrichten an die Junk-e-Mail-Ordner des Benutzers. Für neu erkannte Schadsoftware entfernt ZAP Anlagen aus der e-Mail-Nachricht, unabhängig davon, ob die e-Mail-Nachricht gelesen wurde. Umgekehrt gilt für Nachrichten, die fälschlicherweise als bösartige klassifiziert wurden.
  
Die ZAP-Aktion ist nahtlos, für den Postfachbenutzer, kann er nicht informiert wird, dass die e-Mail-Nachricht verschoben wurde.
  
Listen, [e-Mail-Flussregeln](https://go.microsoft.com/fwlink/p/?LinkId=722755)und Endbenutzer Regeln zulassen oder zusätzliche Filter haben Vorrang vor ZAP.
  
 **Inhalt dieses Artikels:**
  
> [Legen Sie die Richtlinie für Spam-filter](zero-hour-auto-purge.md#BK_SetSpam)
    
> [Überprüfen Sie, ob ZAP Ihrer Nachricht verschoben.](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [ZAP deaktivieren](zero-hour-auto-purge.md#BK_Posh)
    
> [Häufig gestellte Fragen](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a>Arbeiten mit ZAP

ZAP ist standardmäßig aktiviert, aber Sie müssen sicherstellen, dass eine Reihe von Bedingungen erfüllt sind:
  
- Richtlinie für Spam-Filter wird auf die [Nachricht in Junk-e-Mail-Ordner verschieben](zero-hour-auto-purge.md#BK_SetSpam)festgelegt.
    
    Sie können auch eine neue Richtlinie des Spam-Filter erstellen, die nur für eine Gruppe von Benutzern angewendet wird, wenn Sie nicht möchten, dass alle Postfächer von ZAP überwachten sein.
    
- Des Benutzers [Optionen \> Junk-e-Mail-](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).
    
Wenn Sie [überprüfen, ob ZAP Ihre Nachricht verschoben](zero-hour-auto-purge.md#BK_DidZAPMove)möchten, können Sie das Exchange Online Tool für die nachrichtenablaufverfolgung.
  
Administratoren können auch [Deaktivieren ZAP](zero-hour-auto-purge.md#BK_Posh) mithilfe von PowerShell. 
  
 **Richtlinie für Spam-Filter festlegen**
  
1. Melden Sie sich bei der [Where zur Anmeldung bei Office 365 für Unternehmen](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) , und wählen Sie **Protection** \> **Spam-Filter**. 
    
    ![In der Exchange-Verwaltungskonsole "Schutz" und dann Spam-filter](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. Wählen Sie die Filterrichtlinie, die Sie anpassen möchten, oder wählen Sie **Hinzufügen**![Symbol hinzufügen](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) einen neuen Anwendungspool erstellen. 
    
    In der vorherigen Screenshot ist die Richtlinie namens "Default", aber wenn Sie zusätzliche Spam Filterrichtlinien erstellen Sie können Geben sie einen anderen Namen. Sie können nur eine begrenzte Auswahl von Benutzern auch die Richtlinie zuweisen.
    
3. Klicken Sie im Richtlinienfenster wählen Sie **Spam und Massen-Aktionen**, und stellen Sie sicher, dass **Spam** **Verschieben**der Nachricht an die Junk-e-Mail-Ordner festgelegt ist. 
    
    Wenn Sie **Speichern** zu diesem Zeitpunkt auswählen, gilt die Richtlinie zu Ihrem Office 365-Mandanten. 
    
    ![Festlegen von Spam und Massen-Aktionen Mpve der Nachricht an die Junk-e-Mail-Ordner](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. Wenn Sie eine neue Richtlinie erstellt und die Richtlinie nur einen Satz von Benutzer gelten sollen, Scroll **Angewendet auf** Abschnitt Filter im Fenster Richtlinie und in den Menüsteuerelementen im wählen Sie die **Empfänger**, **Domäne**oder **Gruppenmitgliedschaften** Sie Möchten Sie die Richtlinie angewendet werden soll. Sie können auch zusätzliche Bedingungen und Ausnahmen festlegen. 
    
    ![Wählen Sie im Abschnitt angewendet auf die Empfänger](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    Wählen Sie die Richtlinie auf die ausgewählten Benutzer anwenden **zu speichern** . 
    
 **Um festzustellen, ob ZAP Ihrer Nachricht verschoben.**
  
- [Feststellen und beheben Probleme bei der e-Mail-Übermittlung als ein Office 365 für Unternehmen Admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) können Sie ermitteln, ob die Nachricht vom ZAP verschoben wurde: 
    
    Suchen Sie nach dem Text "null-Stunden automatisch löschen (ZAP)" in Ihre Trace-Details, um eine Nachricht zu identifizieren, die vom ZAP verschoben wurde.
    
 **So deaktivieren Sie ZAP**
  
- Wenn Sie deaktivieren möchten für Ihre Office 365-Mandanten entfernen, oder eine Gruppe von Benutzern, verwenden Sie den **ZapEnabled** -Parameter des [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), ein EOP-Cmdlet.
    
    Im folgenden Beispiel wird ZAP für eine inhaltsfilterrichtlinie namens "Test" deaktiviert.
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a>Häufig gestellte Fragen
<a name="BK_FAQ"> </a>

 **Was passiert, wenn eine legitime Nachricht in den Junk-e-Mailordner verschoben wird?**
  
Befolgen Sie den normalen reporting-Prozess für falsch positive ein. Der einzige Grund für die Nachricht aus dem Posteingang in den Junk-e-Mailordner verschoben werden wird, da der Dienst festgestellt hat, dass die Nachricht Spam war wäre oder böswilliges.
  
 **Was geschieht, wenn ich Office 365 Quarantäne anstelle der Junk-e-Mailordner verwenden?**
  
ZAP nicht Sie Nachrichten in Quarantäne aus dem Posteingang zu diesem Zeitpunkt verschieben.
  
 **Was geschieht, wenn ich eine benutzerdefinierte e-Mail-Flussregel haben (blockieren / Regel zulassen)?**
  
Regelanzahl durch Administratoren (e-Mail-Flussregeln) oder blockieren und zulassen Regeln haben Vorrang vor. Solche Nachrichten werden von der Funktion Kriterien ausgeschlossen.
  
## <a name="related-topics"></a>Verwandte Themen
<a name="BK_FAQ"> </a>

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](block-email-spam-to-prevent-false-negatives.md)
  

