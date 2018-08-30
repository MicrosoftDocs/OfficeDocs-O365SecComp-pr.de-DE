---
title: Use mail flow rules to set the spam confidence level (SCL) in messages
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
description: Sie können eine Transportregel erstellen, mit der der SCL-Wert (Spam Confidence Level) einer E-Mail-Nachricht festgelegt wird. Die SCL-Bewertung ist ein Maßstab dafür, wie wahrscheinlich es ist, dass es sich bei einer Nachricht um Spam handelt. Spam sind unverlangt zugesandte (und normalerweise unerwünschte) E-Mail-Nachrichten. Dieser Dienst kann verschiedene Aktionen für eine Nachricht ausführen, die von ihrer SCL-Bewertung abhängen. Sie können z. B. die Spam-Inhaltsfilterung für Nachrichten umgehen, die von Mitarbeitern Ihrer Organisation gesendet werden, weil Sie darauf vertrauen, dass intern gesendete Nachrichten von Kollegen kein Spam sind. Die Verwendung von Transportregeln zur Festlegung des SCL-Wertes einer Nachricht gibt Ihnen bessere Kontrolle über den Umgang mit Spam.
ms.openlocfilehash: 7abd0d1881374b1f2a4bd32ee480445f7683d1b3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002894"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a>Use mail flow rules to set the spam confidence level (SCL) in messages

Sie können eine Transportregel erstellen, mit der der SCL-Wert (Spam Confidence Level) einer E-Mail-Nachricht festgelegt wird. Die SCL-Bewertung ist ein Maßstab dafür, wie wahrscheinlich es ist, dass es sich bei einer Nachricht um Spam handelt. Spam sind unverlangt zugesandte (und normalerweise unerwünschte) E-Mail-Nachrichten. Dieser Dienst kann verschiedene Aktionen für eine Nachricht ausführen, die von ihrer SCL-Bewertung abhängen. Sie können z. B. die Spam-Inhaltsfilterung für Nachrichten umgehen, die von Mitarbeitern Ihrer Organisation gesendet werden, weil Sie darauf vertrauen, dass intern gesendete Nachrichten von Kollegen kein Spam sind. Die Verwendung von Transportregeln zur Festlegung des SCL-Wertes einer Nachricht gibt Ihnen bessere Kontrolle über den Umgang mit Spam. 
  
 **Was sollten Sie wissen, bevor Sie beginnen?**
  
- Geschätzte Zeit bis zum Abschließen dieses Verfahrens: 10 Minuten.
    
- Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "Transportregeln" im [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) oder [Featureberechtigungen in EOP](eop/feature-permissions-in-eop.md). 
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
    
### <a name="to-create-a-transport-rule-that-sets-the-scl-of-a-message"></a>So erstellen Sie eine Transportregel, mit der der SCL-Wert einer Nachricht festgelegt wird

1. Navigieren Sie in der Exchange-Verwaltungskonsole (EAC) zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf **Neu**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und wählen Sie dann **Eine neue Regel erstellen** aus.
    
3. Geben Sie einen Namen für die Regel ein.
    
4. Klicken Sie auf **Weitere Optionen**, und geben Sie anschließend unter **Diese Regel anwenden, wenn** eine Bedingung an, durch die die Aktion ausgelöst wird, die Sie für diese Regel festlegen (in diesem Falle die Festlegung des SCL-Werts).
    
    Sie können z. B. festlegen **Der Absender** \> **ist intern/extern** und anschließend im Dialogfeld **Absenderposition auswählen** auf die Option **Innerhalb meiner Organisation** und auf **OK** klicken.</br>
    ![Absenderstandort auswählen](media/EOP-ETR-SetSCL-1.jpg)
  
5. Wählen Sie unter **Gehen Sie folgendermaßen vor...** die Option **Nachrichteneigenschaften ändern** \> **SCL-Bewertung (Spam Confidence Level) festlegen** aus.
  
6. Wählen sie im Dialogfeld **SCL angeben** einen der folgenden Werte aus, und klicken Sie auf **OK**:
    
  - **Spamfilter umgehen** - Mit dieser Option wird der SCL-Wert auf -1 gesetzt, was bedeutet, dass keine Inhaltsfilterung durchgeführt wird. 
    
  - **0-4** - Wenn Sie den SCL auf einen dieser Werte setzen, wird die Nachricht zur weiteren Verarbeitung an den Inhaltsfilter weitergeleitet. 
    
  - **5, 6** - Wenn Sie den SCL auf einen dieser Werte setzen, wird die Aktion durchgeführt, die in der entsprechenden Inhaltsfilterrichtlinie für **Spam** festgelegt ist. Die Standardaktion ist das Senden der Nachricht an den Junk-E-Mail-Ordner des Empfängers. 
    
  - **7-9** - Wenn Sie den SCL auf einen dieser Werte setzen, wird die Aktion durchgeführt, die in der entsprechenden Inhaltsfilterrichtlinie für **Nachricht mit hoher Spamwahrscheinlichkeit** festgelegt ist. Die Standardaktion ist das Senden der Nachricht an den Junk-E-Mail-Ordner des Empfängers. 
    
    Weitere Informationen zum Konfigurieren Ihrer Inhaltsfilterrichtlinien finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md). Weitere Informationen zu SCL-Werten in diesem Dienst finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).
    
7. Geben Sie zusätzliche Eigenschaften für die Regel an, und wählen Sie **Speichern**.
    
    > [!TIP]
    > Weitere Informationen über die zusätzlichen Eigenschaften, die Sie für diese Regel auswählen oder festlegen können, erhalten Sie unter [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC). 
  
## <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Wenn Sie verifizieren möchten, dass das Verfahren ordnungsgemäß funktioniert, senden Sie eine E-Mail-Nachricht an einen Mitarbeiter in Ihrer Organisation, und prüfen Sie, ob die erwartete Aktion mit der Nachricht durchgeführt wird. Wenn Sie z. B. **den SCL-Wert (Spam Confidence Level)** auf **Spamfilterung umgehen** setzen, sollte die Nachricht an das Postfach des angegebenen Empfängers gesendet werden. Wenn Sie allerdings **den SCL-Wert (Spam Confidence Level)** auf **9** gesetzt haben und die Aktion in der entsprechenden Inhaltsfilterungsrichtlinie für eine **Nachricht mit hoher Spamwahrscheinlichkeit** darin besteht, die Nachricht in den Junk-E-Mail-Ordner zu verschieben, sollte die Nachricht an den Junk-E-Mail-Ordner des angegebenen Empfängers gesendet werden. 
  

