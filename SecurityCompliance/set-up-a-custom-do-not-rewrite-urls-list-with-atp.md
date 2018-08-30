---
title: Richten Sie eine benutzerdefinierte-nicht-zum Umschreiben von Adressen URLs-Liste mit sicheren Links zu Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
description: Beim Einrichten Ihrer ATP sichere Links Richtlinien können Sie eine Not Rewrite einschließen ' Liste der URLs zum Aktivieren von einigen Personen in Ihrer Organisation Websites besuchen, die Sie in der Liste enthalten.
ms.openlocfilehash: 780b4e5d194ad89acf12b052c81f8af21234eea3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529217"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>Richten Sie eine benutzerdefinierte-nicht-zum Umschreiben von Adressen URLs-Liste mit sicheren Links zu Office 365 ATP

Mit [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP) kann Ihrer Organisation eine [benutzerdefinierte blockierte URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md)so, dass beim Klicken Sie auf Personen Web-Adressen (URLs) in e-Mail-Nachrichten oder bestimmte Office-Dokumente, sie werden daran gehindert unterschiedlich sein und sollte diesen URLs. Ihrer Organisation kann auch benutzerdefinierte "nicht rewrite" Listen für bestimmte Gruppen in Ihrer Organisation haben. Eine Liste "nicht rewrite" kann einige Personen URLs zu besuchen, die andernfalls [ATP sichere](atp-safe-links.md)Links in Office 365 blockiert sind. 
  
In diesem Artikel wird beschrieben, wie eine Liste der URLs an, die von sicheren Links ATP untersucht, und einige wichtige Punkte zu bedenken ausgeschlossen werden.
    
## <a name="important-points-to-keep-in-mind"></a>Wichtige Punkte zu bedenken

- Alle URLs, die Sie in der Liste "nicht rewrite" angeben, werden von ATP sichere Links Scan für die Empfänger die Angabe ausgeschlossen.
    
- Wenn Sie eine Liste "nicht rewrite" für eine sichere Links ATP Richtlinie angeben, können Sie bis zu drei Platzhalter Sternchen einschließen (\*). Platzhalter (\*) wird angenommen, dass für Einträge wie `contoso.com`, die nicht explizit einschließen Präfixe oder Unterdomänen, wie `http://` oder `https://`. Dies bedeutet, dass einen Eintrag wie `contoso.com` ähnelt `\*contoso.com\*` für die Liste "nicht rewrite".
    
    Die folgende Tabelle Listen Beispiele für die Eingabe und Einfluss auf diese Einträge haben.
    
|**Beispieleintrag**|**Sinn und Zweck**|
|:-----|:-----|
|`\*contoso.com\*`  <br/> |Können bestimmte Empfänger eine Domäne, untergeordnete Domänen und Pfade, z. B. Besuchen `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, oder`http://www.contoso.com/a`  <br/> |
|`http://contoso.com/a`  <br/> |Können bestimmte Empfänger eine Website wie `http://contoso.com/a`, aber nicht Pfade`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a\*`  <br/> |Können bestimmte Empfänger eine Website wie `http://contoso.com/a` und Pfade wie`http://contoso.com/a/b`  <br/> |
   
- Wenn Sie bereits eine Liste mit URLs in der Liste "nicht rewrite" verfügen, stellen Sie sicher, überprüfen Sie die Liste und Hinzufügen von Platzhaltern nach Bedarf. Beispielsweise, wenn Ihre vorhandene Liste hat ein Eintrag wie `http://contoso.com/a` und Pfade wie sollen `http://contoso.com/a/b` fügen Sie einen Platzhalter in der Richtlinie den Eintrag, sodass es aussieht `http://contoso.com/a\*`.
    
- Schließen Sie einen Schrägstrich (/) nicht in den URLs, die Sie in der Liste "nicht rewrite" angeben. Beispielsweise geben, sondern `contoso.com/` Geben Sie in der Liste "nicht rewrite" `contoso.com`.
    
## <a name="set-up-a-do-not-rewrite-list-for-specific-groups"></a>Richten Sie eine Liste "nicht rewrite" für bestimmte Gruppen

Sichere Links ATP Protection verwendet mehrere Listen, einschließlich der Liste der blockierten URLs Ihrer Organisation und den Listen "nicht rewrite" für Ausnahmen. Wenn Sie die erforderlichen Berechtigungen verfügen, können Sie Ihre benutzerdefinierte Listen "nicht rewrite" einrichten. Hierzu beim Hinzufügen oder Bearbeiten von Richtlinien für sichere Links, die für bestimmte Empfänger in Ihrer Organisation gelten. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Im Navigationsbereich unter **Threat Management** \> **Richtlinie** \> **Sichere Links**.
    
3. Wählen Sie im Abschnitt **Richtlinien, die auf bestimmte Empfänger anzuwenden** , **New** (neue Schaltfläche ähnelt ein Pluszeichen ( **+**)) zum Erstellen einer neuen Richtlinie. (Alternativ können Sie eine vorhandene Richtlinie bearbeiten.)
    
    ![Wählen Sie neu aus, um eine sichere Links Richtlinie für bestimmte e-Mail-Empfänger hinzufügen](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. Geben Sie einen Namen und eine Beschreibung für die Richtlinie ein.
    
5. Klicken Sie im Abschnitt **Schreiben Sie die folgenden URLs nicht** wählen Sie das Feld **Geben Sie eine gültige URL** und geben Sie eine URL ein, und wählen Sie dann auf das Pluszeichen (+). 
    
6. **Angewendet auf** Sie im Abschnitt wählen Sie **der Empfänger ist Mitglied von**, und wählen Sie dann die Kontaktgruppen, die in der Richtlinie enthalten sein sollen. Wählen Sie **Hinzufügen**, und wählen Sie dann auf **OK**.
    
7. Wenn Sie das Hinzufügen von URLs in der unteren rechten Ecke des Bildschirms abgeschlossen haben, wählen Sie **Speichern**.
    
> [!NOTE]
> Stellen Sie sicher, dass Sie die benutzerdefinierte Liste der blockierten URLs Ihrer Organisation überprüfen. Finden Sie unter [Einrichten einer benutzerdefinierten blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md). 
  
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[ATP sichere Links in Office 365](atp-safe-links.md)
  
[Einrichten von sicheren Links ATP Richtlinien in Office 365](set-up-atp-safe-links-policies.md)
  
[Richten Sie eine benutzerdefinierte blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md)

[Anzeigen von Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)

[Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  

