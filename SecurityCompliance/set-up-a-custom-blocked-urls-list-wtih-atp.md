---
title: Richten Sie eine benutzerdefinierte blockierte URLs Liste mit sicheren Links zu Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 12/11/2018
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Hier erfahren Sie, wie Sie eine Liste der blockierten URLs für Ihre Organisation mit Office 365 erweiterte Threat Protection einrichten. Blockierte URLs werden auf e-Mail-Nachrichten und Office-Dokumenten gemäß Ihrer ATP sichere Links Richtlinien angewendet.
ms.openlocfilehash: 25f01b767726ebf02d5da5d18444fa0428f144ac
ms.sourcegitcommit: 031781d0eecf33baabcd03ea53546d41076062b4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2018
ms.locfileid: "27240528"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Richten Sie eine benutzerdefinierte blockierte URLs Liste mit sicheren Links zu Office 365 ATP

Mit [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP) kann Ihre Organisation eine benutzerdefinierte Liste von Website-Adressen (URLs verwendet) haben, die blockiert werden. Wenn eine URL blockiert wird, Personen, die Links zu den blockierten URL klicken Sie auf einer [Seite Warnung](atp-safe-links-warning-pages.md) wird aufgerufen, die in der folgenden Abbildung ähneln: 
  
![Diese Website wird blockiert.](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
Die Liste der blockierte URLs von Office 365-Security-Team Ihrer Organisation definiert ist, und dieser Liste gilt für alle Benutzer in der Organisation, die von sicheren Links zu Office 365 ATP Richtlinien abgedeckt wird. 
  
Lesen Sie diesen Artikel erfahren, wie Ihre Organisation benutzerdefinierte blockierte URLs Liste für [ATP sichere Links in Office 365](atp-safe-links.md)einrichten.
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>Zeigen Sie an oder bearbeiten Sie eine benutzerdefinierte Liste der blockierten URLs

[ATP sichere Links in Office 365](atp-safe-links.md) verwendet mehrere Listen, einschließlich Ihrer Organisation benutzerdefinierte blockierte URLs Liste. Wenn Sie die erforderlichen Berechtigungen verfügen, können Sie benutzerdefinierte Liste in Ihrer Organisation einrichten. Zu diesem Zweck Ihrer Organisation Standardrichtlinie sichere Links bearbeiten.
  
1. Wechseln Sie zu [https://security.microsoft.com](https://security.microsoft.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Wählen Sie im linken Navigationsbereich, klicken Sie unter **Threat Management** **Policy** \> **Sichere Links**.
    
3. Klicken Sie im Abschnitt **Richtlinien, die für die gesamte Organisation gelten,** **Standard**wählen Sie aus, und wählen Sie dann auf **Bearbeiten** (die Schaltfläche Bearbeiten hat einen Stift).<br/>![Klicken Sie auf Bearbeiten, um die Standardrichtlinie für sichere Links Protection bearbeiten](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)<br/>Dadurch können Sie Ihrer Liste der blockierten URLs anzuzeigen. Zunächst verfügen Sie möglicherweise keine hier aufgeführten URLs.<br/>![Liste der URLs in der Standardrichtlinie für sichere Links blockiert](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. Feld **Geben Sie eine gültige URL** auswählen, geben Sie eine URL ein, und wählen Sie dann auf das Pluszeichen (**+**). 

5. Wenn Sie das Hinzufügen von URLs in der unteren rechten Ecke des Bildschirms abgeschlossen haben, wählen Sie **Speichern**.
    
## <a name="a-few-things-to-keep-in-mind"></a>Einige Dinge im Hinterkopf behalten

Während Sie URLs zur Kontaktliste hinzufügen, sollten beachten Sie die folgenden Punkte: 

- Schließen Sie keinen Schrägstrich ( **/**) am Ende der URL. Beispielsweise statt `http://www.contoso.com/`, geben Sie `http://www.contoso.com`.
    
- Sie können eine Domäne-only-URL angeben (wie `contoso.com` oder `tailspintoys.com`). Dies wird blockiert, Klicks für jede URL, die die Domäne enthält.

- Sie können eine Unterdomäne angeben (wie `toys.contoso.com*`) ohne zu eine vollständige Domäne blockieren (wie `contoso.com`). Dadurch Block klickt auf einen beliebigen URL, die die Unterdomäne enthält, aber es nicht blockieren Klicks auf eine URL, die die vollständige Domäne enthält.  
    
- Sie können bis zu drei Platzhalter Sternchen einschließen (\*) pro URL. Die folgende Tabelle enthält einige Beispiele für die Eingabe und Einfluss auf diese Einträge haben.
    
|**Beispieleintrag**|**Sinn und Zweck**|
|:-----|:-----|
|`contoso.com`oder`*contoso.com*`  <br/> |Blockiert die Domäne, untergeordnete Domänen und Pfade, wie `https://www.contoso.com`, `http://sub.contoso.com`, und`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |Eine Website blockiert `http://contoso.com/a` aber keine zusätzliche Pfade`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Eine Website blockiert `http://contoso.com/a` und wie Sie zusätzliche Pfade`http://contoso.com/a/b`  <br/> |
|`http://toys.contoso.com*`  <br/> |Blöcke eine Unterdomäne (in diesem Fall "Toys"), aber zulassen Klicks zu anderen Domänen-URLs (wie `http://contoso.com` oder `http://home.contoso.com`).  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a>Gewusst wie: Definieren von Ausnahmen für bestimmte Benutzer in einer Organisation

Bestimmte Gruppen können URLs anzuzeigen, die für andere Benutzer blockiert werden soll, können Sie eine sichere Links ATP Richtlinie angeben, die für bestimmte Empfänger gilt. Finden Sie unter [Einrichten einer benutzerdefinierten "nicht rewrite" URLs Liste verwenden ATP sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
  

