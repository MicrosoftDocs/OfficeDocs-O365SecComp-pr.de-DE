---
title: Einrichten einer benutzerdefinierten Liste blockierter URLs mit Office 365 ATP-sicheren Links
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
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
ms.collection: M365-security-compliance
description: Erfahren Sie, wie Sie mithilfe von Office 365 Advanced Threat Protection eine Liste blockierter URLs für Ihre Organisation einrichten. Die blockierten URLs gelten für e-Mail-Nachrichten und Office-Dokumente gemäß ihren Richtlinien für ATP Safe Links.
ms.openlocfilehash: ad9c613221b94e61022b11541ee068e35e47cc70
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213025"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Einrichten einer benutzerdefinierten Liste blockierter URLs mit Office 365 ATP-sicheren Links

> [!IMPORTANT]
> Dieser Artikel richtet sich an Geschäftskunden. Wenn Sie ein Benutzer sind, der nach Informationen zu sicheren Links in Outlook sucht, lesen Sie den Thema [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Mit [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) kann Ihre Organisation über eine benutzerdefinierte Liste von Websiteadressen (URLs) verfügen, die blockiert werden. Wenn eine URL blockiert wird, werden Personen, die auf Links zu der blockierten URL klicken, zu einer [Warnungsseite](atp-safe-links-warning-pages.md) weitergeleitet, die der folgenden Abbildung ähnelt: 
  
![Diese Website ist blockiert](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
Die Liste Blockierte URLs wird vom Office 365-Sicherheitsteam Ihrer Organisation definiert, und diese Liste gilt für alle in der Organisation, die von Office 365 ATP Safe Links-Richtlinien abgedeckt werden. 
  
In diesem Artikel erfahren Sie, wie Sie die Liste der benutzerdefinierten blockierten URLs für [ATP-sichere Links in Office 365](atp-safe-links.md)einrichten.
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>Anzeigen oder Bearbeiten einer benutzerdefinierten Liste blockierter URLs

[ATP-sichere Links in Office 365](atp-safe-links.md) verwenden mehrere Listen, einschließlich der benutzerdefinierten Liste blockierter URLs Ihrer Organisation. Wenn Sie über die erforderlichen Berechtigungen verfügen, können Sie die benutzerdefinierte Liste Ihrer Organisation einrichten. Hierzu bearbeiten Sie die Standardrichtlinie für sichere Links in Ihrer Organisation.

Um ATP-Richtlinien zu bearbeiten (oder zu definieren), müssen Sie eine der in der folgenden Tabelle beschriebenen Rollen besitzen: 

|Rolle  |Wo/wie zugewiesen  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a>So können Sie eine benutzerdefinierte Liste blockierter URLs anzeigen oder bearbeiten
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an. 
    
2. Wählen Sie im linken Navigationsbereich unter **Bedrohungs Verwaltung**die Option **Richtlinie** \> für **sichere Links**aus.
    
3. Wählen Sie in den **Richtlinien für den Abschnitt gesamte Organisation** die Option **Standard**aus, und klicken Sie dann auf **Bearbeiten** (die Schaltfläche Bearbeiten ähnelt einem Bleistift).<br/>![Klicken Sie auf Bearbeiten, um die Standardrichtlinie für den Schutz sicherer Links zu bearbeiten.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)<br/>Auf diese Weise können Sie die Liste der blockierten URLs anzeigen. Am Anfang haben Sie möglicherweise keine URLs aufgelistet.<br/>![Liste blockierter URLs in der Standardrichtlinie für sichere Links](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. Aktivieren Sie das Kontrollkästchen **gültige URL eingeben** , geben Sie eine URL ein, und klicken Sie dann**+** auf das Pluszeichen (). 

5. Wenn Sie mit dem Hinzufügen von URLs fertig sind, wählen Sie in der unteren rechten Ecke des Bildschirms **Speichern**aus.
    
## <a name="a-few-things-to-keep-in-mind"></a>Einige Dinge, die Sie beachten sollten

Beachten Sie beim Hinzufügen von URLs zu Ihrer Liste die folgenden Punkte: 

- Fügen Sie am Ende der URL keinen **/** Schrägstrich () ein. Geben Sie beispielsweise statt Eingabe `http://www.contoso.com/`ein ein `http://www.contoso.com`.
    
- Sie können eine nur-Domäne-URL angeben ( `contoso.com` wie `tailspintoys.com`oder). Dadurch werden Klicks auf alle URLs blockiert, die die Domäne enthalten.

- Sie können eine Unterdomäne (like `toys.contoso.com*`) angeben, ohne eine vollständige Domäne zu `contoso.com`blockieren (like). Dadurch wird das Klicken auf eine beliebige URL blockiert, die die Unterdomäne enthält, es werden jedoch keine Klicks auf eine URL blockiert, die die vollständige Domäne enthält.  
    
- Sie können bis zu drei Platzhalter Sternchen (\*) pro URL hinzufügen. In der folgenden Tabelle sind einige Beispiele für die Eingabe und die Auswirkungen dieser Einträge aufgeführt.
    
|**Beispieleintrag**|**Funktionsweise**|
|:-----|:-----|
|`contoso.com`oder`*contoso.com*`  <br/> |Blockiert die Domäne, Unterdomänen und Pfade, wie `https://www.contoso.com` `http://sub.contoso.com`, und`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |Blockiert eine Website `http://contoso.com/a` , jedoch keine zusätzlichen Unterpfade wie`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Blockiert eine Website `http://contoso.com/a` und weitere Unterpfade wie`http://contoso.com/a/b`  <br/> |
|`http://toys.contoso.com*`  <br/> |Blockiert eine Unterdomäne (in diesem Fall "Toys"), ermöglicht jedoch das Klicken auf andere Domänen- `http://contoso.com` URLs `http://home.contoso.com`(wie oder).  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a>Definieren von Ausnahmen für bestimmte Benutzer in einer Organisation

Wenn Sie möchten, dass bestimmte Gruppen URLs anzeigen können, die möglicherweise für andere blockiert werden, können Sie eine ATP-Richtlinie für sichere Links angeben, die für bestimmte Empfänger gilt. Weitere Informationen finden Sie unter [Einrichten einer benutzerdefinierten "nicht umschreiben"-URL-Liste mit ATP-sicheren Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
  

