---
title: Einrichten von Richtlinien für Office 365 ATP sichere Anlagen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
description: Definieren Sie sichere Anlagen Richtlinien zum Schutz Ihrer Organisation aus schädliche Dateien in e-Mail.
ms.openlocfilehash: c5c18e3e8300a5cb8eabb8a099d6757a09170ff7
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014877"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a>Einrichten von Richtlinien für Office 365 ATP sichere Anlagen

Benutzer regelmäßig senden, empfangen und Freigeben von Anlagen, wie Dokumente, Kalkulationstabellen, Präsentationen und vieles mehr. Es ist nicht immer leicht zu erkennen, ob eine Anlage sicherer oder böswilliges ist einfach anhand einer e-Mail-Nachricht. Und die letzte gewünschte ist eine bösartige Anlage abzurufenden über, einem Chaos für Ihre Organisation. Zum Glück kann [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP) helfen. Sie können Richtlinien [ATP sichere Anlagen](atp-safe-attachments.md) einrichten, um sicherzustellen, dass Ihre Organisation vor Angriffen durch unsichere e-Mail-Anlagen geschützt ist. 
  
## <a name="what-to-do"></a>Nächste Schritte 
  
1. [Überprüfen Sie die erforderlichen Komponenten](#review-the-prerequisites)
    
2. [Richten Sie eine Richtlinie ATP sichere Anlagen](#set-up-an-atp-safe-attachments-policy)
    
3. [Erfahren Sie mehr über Richtlinienoptionen ATP sichere Anlagen](#learn-about-atp-safe-attachments-policy-options)
    
## <a name="step-1-review-the-prerequisites"></a>Schritt 1: Überprüfen der erforderlichen Komponenten

- Stellen Sie sicher, dass Ihre Organisation [Office 365 erweiterte Schutz](office-365-atp.md)verfügt.
    
- Stellen Sie sicher, dass Sie die erforderlichen verfügen [Berechtigungen für die Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
- [Informieren Sie sich über Richtlinienoptionen ATP sichere Anlagen](#learn-about-atp-safe-attachments-policy-options) (in diesem Artikel). Einige Optionen, wie die Optionen Monitor oder ersetzen können dazu führen eine geringfügige Verzögerung von e-Mails während Anlagen überprüft werden. Nachricht verzögert zu vermeiden, erwägen Sie [Dynamische Übermittlung und Anzeigen der Vorschau](dynamic-delivery-and-previewing.md).
    
- Können Sie bis zu 30 Minuten für die neue oder aktualisierte Richtlinie in allen Office 365-Rechenzentren verteilen.
    
## <a name="step-2-set-up-or-edit-an-atp-safe-attachments-policy"></a>Schritt 2: Einrichten eine Richtlinie für den sicheren Anlagen ATP (oder bearbeiten)
  
1. Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. In der Office 365-Sicherheit &amp; Compliance Center, wählen Sie im linken Navigationsbereich unter **Threat Management** **Policy** \> **Sichere Anlagen**.
    
3. Wenn Sie **für SharePoint, OneDrive, und Microsoft-Teams, ATP einschalten**angezeigt wird, wird empfohlen, dass Sie diese Option auswählen. Dadurch können [Office 365 erweiterte Bedrohungsschutz für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md) für die Office 365-Umgebung. 
    
4. Wählen Sie **neu** (die neue Schaltfläche ähnelt ein Pluszeichen ( **+**)) zum erstmaligen Erstellen der Richtlinie.
    
5. Geben Sie Name, Beschreibung und Einstellungen für die Richtlinie ein.<br/><br/>**Beispiel:** Um eine Richtlinie namens "keine Verzögerungen" eingerichtet, die alle Nachrichten sofort übermittelt und Anlagen dann überwacht werden, nachdem sie überprüft haben, können Sie die folgenden Einstellungen angeben: 
    
      - Geben Sie im Feld **Name** keine verzögert.
    
      - Geben Sie im Feld **Beschreibung** eine Beschreibung wie sofort bietet Nachrichten und Anlagen überwacht nach der Überprüfung.
    
      - Wählen Sie im Abschnitt Antwort **Dynamische Übermittlung** . ([Erfahren Sie mehr über dynamische Übermittlung und sichere Anlagen ATP Vorschau](dynamic-delivery-and-previewing.md)).
    
      - Wählen Sie die Option zum Umleiten aktivieren, und geben Sie die e-Mail-Adresse des Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheit Analyst, die bösartige Anlagen untersuchen, klicken Sie im Abschnitt **Anlage umleiten** . 
    
      - **Angewendet auf** Sie im Abschnitt wählen Sie **die Domäne des Empfängers ist**, und wählen Sie dann Ihre Domäne aus. Wählen Sie **Hinzufügen**, und wählen Sie dann auf **OK**.
    
6. Klicken Sie auf **Save**.
    
Verwenden Sie nach Möglichkeit mehrere sichere Anlagen ATP-Richtlinien für Ihre Organisation. Diese Richtlinien werden in der Reihenfolge angewendet werden, die sie auf der Seite **ATP sichere Anlagen** aufgeführt werden. Nachdem eine Richtlinie definiert oder bearbeitet wurde, können Sie mindestens 30 Minuten für die Richtlinien in der gesamten Microsoft-Rechenzentren wirksam wird. 
  
## <a name="step-3-learn-about-atp-safe-attachments-policy-options"></a>Schritt 3: Informationen Sie zu Richtlinienoptionen ATP sichere Anlagen

Wie Sie Ihre Richtlinien ATP sichere Anlagen eingerichtet haben, wählen Sie ein Gerät viele Optionen, einschließlich Monitor, blockieren, ersetzen, dynamische Übermittlung und So weiter. Für den Fall, dass Sie wissen möchten, wie Sie, diese Optionen vorgehen, die in der folgenden Tabelle werden alle zusammengefasst und ihre Auswirkung.
  
|**Option**|**Effekt**|**Wird verwendet, wenn Sie möchten:**|
|:-----|:-----|:-----|
|**Off** <br/> |Anlagen für Malware überprüft nicht  <br/> Nachrichtenübermittlung werden nicht verzögert.  <br/> |Deaktivieren Sie Überprüfung für interne Absender, Scanner, Faxe oder Smarthosts, die nur ordnungsgemäßen Anlagen senden  <br/> Verhindern, dass unnötige Verzögerungen bei der internen e-Mail-Routings  <br/> **Diese Option ist nicht für die meisten Benutzer empfohlen. Sie können Sie deaktivieren ATP sichere Anlagen scannen für eine kleine Gruppe von internen Absendern.**           |
|**Monitor** <br/> |Übermittelt Nachrichten mit Anlagen, und klicken Sie dann verfolgt was passiert, mit erkannte Schadsoftware  <br/> |Finden Sie unter erkannte Schadsoftware in Ihrer Organisation, auf dem wechselt  <br/> |
|**Blockieren** <br/> |Verhindert, dass Nachrichten mit Anlagen aus fortfahren erkannte Schadsoftware  <br/> Sendet Nachrichten mit erkannte Schadsoftware in [Quarantäne in Office 365](manage-quarantined-messages-and-files.md) , in dem ein Sicherheitsadministrator oder Analyst überprüfen und release (diese Nachrichten oder löschen kann)  <br/> Zukünftige Nachrichten und Anlagen blockiert automatisch  <br/> |Schützen der Organisation wiederholte Angriffe mit der gleichen Malware Anlagen  <br/> |
|**Ersetzen** <br/> |Entfernt Anlagen Schadsoftware erkannt  <br/> Benachrichtigt Empfänger, dass Anlagen entfernt wurden  <br/> Sendet Nachrichten mit erkannte Schadsoftware in [Quarantäne in Office 365](manage-quarantined-messages-and-files.md) , in dem ein Sicherheitsadministrator oder Analyst überprüfen und release (diese Nachrichten oder löschen kann)  <br/> |Auslösen der Sichtbarkeit an Empfänger, dass Anlagen aufgrund gefundene Malware entfernt wurden  <br/> |
|**Dynamische Übermittlung** <br/> |Übermittelt Nachrichten sofort  <br/> Anlagen ersetzt mit einer Platzhalterdatei, bis Überprüfung abgeschlossen ist, und klicken Sie dann die Anlagen überwacht, wenn keine Schadsoftware ermittelt wird  <br/> Enthält als Anlage Vorschau von Funktionen für die meisten PDF-Dateien und Office-Dateien während der Überprüfung  <br/> Sendet Nachrichten mit erkannte Schadsoftware in Quarantäne, in dem ein Sicherheitsadministrator oder Analyst überprüfen und release (diese Nachrichten oder löschen kann)  <br/> [Erfahren Sie mehr über dynamische Übermittlung und sichere Anlagen ATP Vorschau](dynamic-delivery-and-previewing.md) <br/> |Vermeiden Sie Nachricht Verzögerungen beim Schützen der Empfänger schädliche Dateien  <br/> Aktivieren von Empfängern für die Vorschau von Anlagen im abgesicherten Modus während Überprüfung durchgeführt wird  <br/> |
|**Aktivieren Sie die Umleitung** <br/> |Gilt, wenn die Option überwachen, blockieren oder Ersetzen ausgewählt wird  <br/> Sendet Anlagen an eine angegebene e-Mail-Adresse, in dem können Sicherheitsadministratoren oder Analysten untersuchen  <br/> |Aktivieren der Sicherheitsadministratoren und Analysten verdächtige Anlagen überprüfen  <br/> |
   
## <a name="next-steps"></a>Nächste Schritte

Nachdem Ihre ATP sichere Anlagen Richtlinien vorhanden sind, können Sie sehen, wie für Ihre Organisation ATP funktionsfähig ist, indem Sie Berichte anzeigen. Finden Sie in den folgenden Ressourcen, um mehr zu erfahren:
- [Anzeigen von Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)
- [Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center](use-explorer-in-security-and-compliance.md)
 