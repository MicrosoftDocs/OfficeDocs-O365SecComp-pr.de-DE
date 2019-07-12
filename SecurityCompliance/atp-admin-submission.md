---
title: Übermittlungen von Administratoren in Office 365 ATP
ms.author: brwilcox
author: briwilcox
manager: dansimp
ms.date: 07/09/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Hier erfahren Sie, wie Sie potenziell schädliche Nachrichten, URLs und Dateien an Microsoft übermitteln.
ms.openlocfilehash: 6f7ea63cae4d7cafb0d1386b29d99101d290ef30
ms.sourcegitcommit: 9e2df36b05a2c93ce2629a7a5eda8f44159d114d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2019
ms.locfileid: "35632225"
---
# <a name="admin-submissions-in-office-365-atp"></a>Übermittlungen von Administratoren in Office 365 ATP

Administratoren können jetzt e-Mails senden, indem Sie die Datei-oder Netzwerknachrichten-ID, URLs und Dateien für die Überprüfung durch Microsoft in Office 365 verwenden. Der Abschnitt aktualisierte Übermittlungen enthält weiterhin von Benutzern gemeldete Nachrichten. 

Wenn Sie eine e-Mail übermitteln, erhalten Sie Informationen zu allen Richtlinien, die möglicherweise die eingehenden e-Mails in ihren Mandanten zugelassen haben, sowie über die Untersuchung von URLs und Anlagen in der e-Mail. Richtlinien, die möglicherweise eine e-Mail zugelassen haben, enthalten die Liste sicherer Absender eines einzelnen Benutzers sowie Richtlinien auf Mandantenebene wie ETR-Regeln. 


## <a name="how-to-submit-content"></a>Vorgehensweise zum Übermitteln von Inhalten

Um Inhalte an Microsoft zu übermitteln, klicken Sie auf die Schaltfläche **neue Übermittlung** in der linken oberen Ecke der Seite Übermittlungen. Ein Flyout auf der rechten Seite der Seite wird mit der Option zum Senden einer e-Mail, einer URL oder einer Datei angezeigt. 

### <a name="email"></a>E-Mail
![Beispiel für eine e-Mail-Übermittlung](media/submission-flyout-email.PNG)
1. Um eine e-Mail zu senden, wählen Sie **e-Mail** und geben Sie die e-Mail- **Netzwerknachrichten-ID** an, oder laden Sie die e-Mail-Datei 

2. Geben Sie die Empfänger an, für die Sie die Richtlinienüberprüfung ausführen möchten. Durch die Richtlinienüberprüfung wird ermittelt, ob die e-Mail-Überprüfung aufgrund von Richtlinien auf Benutzer-oder Mandantenebene umgangen wurde. 

3. Geben Sie an, ob die e-Mail-Nachricht blockiert werden sollte. Wenn die e-Mail blockiert wurde, geben Sie an, ob Sie als Spam, Phishing oder Schadsoftware blockiert werden soll. Wenn Sie nicht sicher sind, welche Art Sie haben könnten, verwenden Sie Ihr Bestes Urteil.  

* Wenn der Filter aufgrund von Richtlinien bei der Übermittlung umgangen wurde, werden Informationen zu dieser Richtlinie angezeigt.

* Wenn der Filter aufgrund einer oder mehrerer Richtlinien nicht umgangen wurde, wird die Überprüfung in einigen Minuten abgeschlossen. Sie erhalten zusätzliche Informationen über die Übermittlung, indem Sie auf den Link Status klicken. Dies beinhaltet die Ergebnisse der Richtlinienüberprüfung und das Ergebnis der erneuten Überprüfung. Hinweis Dadurch wird die e-Mail-Nachricht nicht über den Office 365 ATP-voll Filter Stapel erneut ausgeführt, es wird jedoch ein partieller erneuter Scan auf der Grundlage bestimmter Attribute der e-Mail, der URL oder der Datei ausgeführt. 

4. Klicken Sie **** auf die Schaltfläche Absenden.

### <a name="url"></a>URL
![Beispiel für eine e-Mail-Übermittlung](media/submission-url-flyout.png)
1. So übermitteln Sie eine URL wählen Sie **URL** aus dem Flyout aus. Geben Sie die vollständige URL einschließlich des Protokolls (**https://**) ein. 

* Wenn Sie die Option **gefiltert haben ausgewählt haben**, geben Sie an, ob die URL Phishing oder Schadsoftware ist.

2. Klicken Sie **** auf die Schaltfläche Absenden. 


### <a name="file"></a>Datei
![Beispiel für eine e-Mail-Übermittlung](media/submission-file-flyout.PNG)
1. Um eine Datei zu übermitteln, wählen Sie **Datei** aus dem Flyout aus, und laden Sie die Datei hoch, die Sie überprüfen möchten. 

2. Klicken Sie **** auf die Schaltfläche Absenden.


## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection-Plan 2](office-365-ti.md)
  
[Schutz vor Bedrohungen in Office 365](protect-against-threats.md)
  
[Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)
  

