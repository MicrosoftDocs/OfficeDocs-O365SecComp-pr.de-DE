---
title: Konfigurieren der Richtlinie für ausgehende Spamnachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/10/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
description: Die Filterung ausgehender Spamnachrichten ist immer aktiviert, wenn Sie den Dienst für das Senden ausgehender E-Mails verwenden und dadurch Organisationen, die den Dienst nutzen, und ihre jeweiligen Empfänger schützen.
ms.openlocfilehash: b6185cfded28613cb5a512882aefb1a99db158db
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002410"
---
# <a name="configure-the-outbound-spam-policy"></a>Konfigurieren der Richtlinie für ausgehende Spamnachrichten

Die Filterung ausgehender Spamnachrichten ist immer aktiviert, wenn Sie den Dienst für das Senden ausgehender E-Mails verwenden und dadurch Organisationen, die den Dienst nutzen, und ihre jeweiligen Empfänger schützen. Ebenso wie die Filterung eingehender Nachrichten besteht die Filterung ausgehender Nachrichten aus einer Verbindungsfilterung und einer Inhaltsfilterung, wobei die Einstellungen für den ausgehenden Filter nicht konfiguriert werden können. Wenn eine ausgehende Nachricht als Spam identifiziert wird, wird sie durch den Pool für besonders riskante Zustellungen geleitet, der die Wahrscheinlichkeit reduziert, dass der normale Pool für ausgehende IP-Adressen einer Sperrliste hinzugefügt wird. Falls ein Kunde auch weiterhin ausgehende Spamnachrichten über den Dienst sendet, wird er für das Senden von Nachrichten gesperrt. Die Filterung ausgehender Spamnachrichten kann zwar nicht deaktiviert oder geändert werden, aber Sie können verschiedene unternehmensweite Spameinstellungen über die Standardrichtlinie für ausgehende Spamnachrichten konfigurieren. 
  
Das folgende Video zeigt, wie die Richtlinie für ausgehende Spamnachrichten konfiguriert wird:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
  
Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter der "Anti-Spam-Eintrag im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.
  
Das folgende Verfahren kann auch über remote-PowerShell erfolgen. Verwenden Sie das Cmdlet [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) , um Ihre Einstellungen, und das [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) zum Bearbeiten Ihrer Einstellungen für ausgehende Spamnachrichten Richtlinie zu prüfen. Weitere Informationen zu Windows PowerShell verwenden, um die Verbindung mit Exchange Online Protection finden Sie unter [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). So verwenden Sie Windows PowerShell für die Verbindung zu Exchange Online finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a>Bearbeiten der Standardrichtlinie für ausgehende Spamnachrichten mithilfe der Exchange-Verwaltungskonsole
<a name="sectionSection1"> </a>

Verwenden Sie das folgende Verfahren, um die Standardrichtlinie für ausgehende Spamnachrichten zu bearbeiten:
  
### <a name="to-configure-the-default-outbound-spam-policy"></a>So konfigurieren Sie die Standardrichtlinie für ausgehende Spamnachrichten

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Ausgehende Spamnachrichten**, und doppelklicken Sie dann auf die Standardrichtlinie.
    
2. Wählen Sie die Menüoption **Einstellungen für ausgehenden Spam** aus. 
    
3. Aktivieren Sie folgende Kontrollkästchen für ausgehende Nachrichten, und geben Sie dann eine oder mehrere zugehörige E-Mail-Adressen in dem nebenstehenden Eingabefeld ein (es kann sich dabei um Verteilerlisten handelt, wenn diese gültige SMTP-Ziele ergeben):
    
1. **Eine Kopie aller verdächtigen ausgehenden E-Mails an folgende E-Mail-Adressen senden**. Dabei handelt es sich um Nachrichten, die vom Filter als Spam markiert wurden (unabhängig von der SCL-Bewertung). Sie werden vom Filter nicht zurückgewiesen, sondern durch den Pool für besonders riskante Zustellungen geleitet. Trennen Sie mehrere Adressen durch ein Semikolon. Beachten Sie, dass die angegebenen Empfänger die Nachrichten als "Bcc" (Blind Carbon Copy, nicht sichtbare Kopie) erhalten (in den Feldern "Von" und "An" sind der ursprüngliche Sender und Empfänger angegeben).
    
2. **Senden Sie eine Benachrichtigung an die folgende E-Mail-Adresse, wenn ein Absender für das Senden ausgehender Spamnachrichten blockiert wird**. Trennen Sie mehrere Adressen durch ein Semikolon.
    
    Wenn eine auffällige Menge an Spamnachrichten von einem bestimmten Benutzer stammt, wird dieser Benutzer für das Senden von E-Mails gesperrt. Der Administrator der Domäne, der in dieser Einstellung angegeben ist, wird darüber informiert, dass ausgehende Nachrichten für diesen Benutzer blockiert werden. Ein Beispiel für diese Benachrichtigung finden Sie unter [Beispielbenachrichtigung, wenn ein Absender aufgrund des Versendens von ausgehendem Spam blockiert wird](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Informationen zur erneuten Aktivierung finden Sie unter [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).
    
4. Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Standardrichtlinieneinstellungen angezeigt.
    
## <a name="for-more-information"></a>Weitere Informationen
<a name="sectionSection2"> </a>

[Pool für besonders riskante Zustellungen für ausgehende Nachrichten](high-risk-delivery-pool-for-outbound-messages.md)
  
[Anti-Spam-Schutz – häufig gestellte Fragen](anti-spam-protection-faq.md)
  

