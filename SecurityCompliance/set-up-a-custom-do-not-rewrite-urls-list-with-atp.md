---
title: Einrichten einer benutzerdefinierten do-not-Rewrite-URLs-Liste mit Office 365 ATP-sicheren Links
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
ms.collection:
- M365-security-compliance
description: Wenn Sie Ihre ATP-Richtlinien für sichere Links einrichten, können Sie eine do-not-Rewrite-Liste mit URLs hinzufügen, um einigen Personen in Ihrer Organisation das Besuchen von Websites zu ermöglichen, die Sie in Ihre Liste aufnehmen.
ms.openlocfilehash: 006dab44054f9cb707bb13d158588ab6606fab5c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264452"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>Einrichten einer benutzerdefinierten do-not-Rewrite-URLs-Liste mit Office 365 ATP-sicheren Links

> [!IMPORTANT]
> Dieser Artikel richtet sich an Geschäftskunden. Wenn Sie ein Benutzer sind, der nach Informationen zu sicheren Links in Outlook sucht, lesen Sie den Thema [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Mit [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) kann Ihre Organisation über eine [benutzerdefinierte Blockierte URL](set-up-a-custom-blocked-urls-list-wtih-atp.md)verfügen, sodass Sie beim Klicken auf Webadressen (URLs) in e-Mail-Nachrichten oder bestimmten Office-Dokumenten daran gehindert werden, zu diesen URLs zu wechseln. Ihre Organisation kann auch benutzerdefinierte "nicht umschreiben"-Listen für bestimmte Gruppen in Ihrer Organisation haben. Eine Liste "nicht umschreiben" ermöglicht es einigen Personen, URLs zu besuchen, die sonst durch [ATP-sichere Links in Office 365](atp-safe-links.md)blockiert werden. 
  
In diesem Artikel wird beschrieben, wie Sie eine Liste von URLs angeben, die von der Überprüfung von ATP Safe Links ausgeschlossen werden, sowie einige wichtige Punkte, die Sie beachten sollten.

## <a name="set-up-a-do-not-rewrite-list"></a>Einrichten einer "nicht umschreiben"-Liste

ATP Safe Links Protection verwendet mehrere Listen, einschließlich der Liste blockierter URLs Ihrer Organisation und der Listen "nicht umschreiben" für Ausnahmen. Wenn Sie über die erforderlichen Berechtigungen verfügen, können Sie Ihre benutzerdefinierten Listen "nicht umschreiben" einrichten. Sie können dies tun, wenn Sie Richtlinien für sichere Links hinzufügen oder bearbeiten, die für bestimmte Empfänger in Ihrer Organisation gelten. 

Um ATP-Richtlinien zu bearbeiten (oder zu definieren), müssen Sie eine der in der folgenden Tabelle beschriebenen Rollen besitzen:

|Rolle  |Wo/wie zugewiesen  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).

### <a name="to-view-or-edit-a-custom-do-not-rewrite-urls-list"></a>So können Sie eine benutzerdefinierte URL-Liste "nicht umschreiben" anzeigen oder bearbeiten
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an. 
    
2. Klicken Sie im linken Navigationsbereich unter **sichere Links**für die **Richtlinie** \> zur **Gefahren Verwaltung** \> .
    
3. Klicken Sie im Abschnitt **Richtlinien für bestimmte Empfänger** auf **neu** (die Schaltfläche neu ähnelt einem Pluszeichen ( **+**)), um eine neue Richtlinie zu erstellen. (Alternativ können Sie eine vorhandene Richtlinie bearbeiten.)<br/>![Wählen Sie neu aus, um eine Richtlinie zu sicheren Links für bestimmte e-Mail-Empfänger hinzuzufügen](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. Geben Sie einen Namen und eine Beschreibung für die Richtlinie an.
    
5. Aktivieren Sie im Abschnitt keine **Umschreibung der folgenden URLs** das Feld **gültige URL eingeben** , und geben Sie dann eine URL ein, und wählen Sie dann das Pluszeichen (+) aus. 
    
6. Wählen Sie im Abschnitt **angewendet** am **den Empfänger ist Mitglied von aus**, und wählen Sie dann die Gruppe (n) aus, die Sie in Ihre Richtlinie aufnehmen möchten. Klicken Sie auf **Hinzufügen**und dann auf **OK**.
    
7. Wenn Sie mit dem Hinzufügen von URLs fertig sind, wählen Sie in der unteren rechten Ecke des Bildschirms **Speichern**aus.
    
> [!NOTE]
> Stellen Sie sicher, dass Sie die benutzerdefinierte Liste der blockierten URLs Ihrer Organisation überprüfen. Weitere Informationen finden Sie unter [Einrichten einer benutzerdefinierten Liste blockiertEr URLs mit sicheren ATP-Links](set-up-a-custom-blocked-urls-list-wtih-atp.md). 
  
## <a name="important-points-to-keep-in-mind"></a>Wichtige Punkte, die Sie beachten sollten

- Alle URLs, die Sie in der Liste "nicht umschreiben" angeben, werden für die von Ihnen angegebenen Empfänger von der Überprüfung von ATP Safe Links ausgeschlossen.
 
- Wenn Sie eine "nicht umschreiben"-Liste für eine ATP-Richtlinie für sichere Links angeben, können Sie bis zu drei Platzhalter\*Sternchen () verwenden. Platzhalter (\*) werden für Einträge wie `contoso.com`, die nicht explizit Präfixe oder Unterdomänen wie `http://` oder `https://`enthalten. Dies bedeutet, dass ein Eintrag wie `contoso.com` `*contoso.com*` bei der Liste "nicht umschreiben" ähnlich ist.

- Wenn Sie bereits über eine Liste von URLs in der Liste "nicht umschreiben" verfügen, vergewissern Sie sich, dass Sie diese Liste überprüfen und gegebenenfalls Platzhalter hinzufügen. Wenn Ihre vorhandene Liste beispielsweise einen Eintrag wie `http://contoso.com/a` enthält und Sie Unterpfade wie `http://contoso.com/a/b` in Ihre Richtlinie aufnehmen möchten, fügen Sie Ihrem Eintrag einen Platzhalter hinzu, damit er aussieht `http://contoso.com/a*`.
    
- Fügen Sie keinen Schrägstrich (/) in die URLs ein, die Sie in der Liste "nicht umschreiben" angeben. Geben `contoso.com`Sie beispielsweise anstatt in `contoso.com/` Ihre Liste "nicht umschreiben" eingeben ein.
    
In der folgenden Tabelle werden Beispiele für die Eingabe und die Auswirkungen dieser Einträge aufgeführt.
    
|**Beispieleintrag**|**Funktionsweise**|
|:-----|:-----|
|`*contoso.com*`  <br/> |Ermöglicht es bestimmten Empfängern, eine Domäne, Unterdomänen und Pfade zu besuchen, Beispiels `http://www.contoso.com`Weise `https://www.contoso.com` `https://maps.contoso.com`,, oder`http://www.contoso.com/a`  <br/> |
|`http://contoso.com/a`  <br/> |Ermöglicht es bestimmten Empfängern, eine Website `http://contoso.com/a`wie zu besuchen, jedoch keine Unterpfade wie`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Ermöglicht es bestimmten Empfängern, eine Website `http://contoso.com/a` wie und Unterpfade wie`http://contoso.com/a/b`  <br/> |
   
 