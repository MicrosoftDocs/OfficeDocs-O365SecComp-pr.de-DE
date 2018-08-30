---
title: Verwenden von Transportregeln zum Konfigurieren von Massen-e-Mail-Filterung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: Sie können den unternehmensweiten Inhaltsfilter für Spam und Massen-E-Mails über die Standardrichtlinien für die Spam-Inhaltsfilterung festlegen. Informationen zum Festlegen der Richtlinien für die Inhaltsfilterung finden Sie unter Konfigurieren von Spamfilterrichtlinien und Set-HostedContentFilterPolicy.
ms.openlocfilehash: 8fa4ba619b55ae12207f36b7625acfaa9838e696
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002476"
---
# <a name="use-transport-rules-to-configure-bulk-email-filtering"></a>Verwenden von Transportregeln zum Konfigurieren von Massen-e-Mail-Filterung

Sie können den unternehmensweiten Inhaltsfilter für Spam und Massen-E-Mails über die Standardrichtlinien für die Spam-Inhaltsfilterung festlegen. Informationen zum Festlegen der Richtlinien für die Inhaltsfilterung finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) und [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx). 
  
Wenn Sie weitere Optionen zum Filtern von Massennachrichten haben möchten, können Sie Exchange-Transportregeln erstellen, um nach Textmustern oder Ausdrücken zu suchen, die häufig in Massen-E-Mails vorkommen. Alle Nachrichten, die diese Merkmale enthalten, werden als Spam markiert. Mithilfe dieser Regeln können Sie die Menge an unterwünschten Massen-E-Mails verringern, die Ihre Organisation empfängt.
  
> [!NOTE]
> Es wird empfohlen, vor der in diesem Thema dokumentierten Erstellung von Transportregeln zuerst [Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?](what-s-the-difference-between-junk-email-and-bulk-email.md) und [BCL-Werte (Bulk Complaint Level)](bulk-complaint-level-values.md) zu lesen. 
  
> [!NOTE]
> Durch die folgenden Verfahren wird eine Nachricht für Ihre gesamte Organisation als Spam markiert. Sie können jedoch eine andere Bedingung hinzufügen, damit diese Regeln nur für bestimmte Empfänger in Ihrer Organisation gelten. Auf diese Weise können die aggressiven Filtereinstellungen für Massen-E-Mails nur für einige wenige Benutzer gelten, die verstärkt anvisiert werden, während der Rest Ihrer Benutzer (die zumeist die Massen-E-Mails erhalten, für die sie sich registriert haben) nicht betroffen sind. 
  
### <a name="create-an-exchange-transport-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a>Erstellen einer Exchange-Transportregel zum Filtern von Massen-E-Mails basierend auf Textmustern

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Geben Sie einen Namen für die Regel ein.
    
4. Klicken Sie auf **Weitere Optionen**. Aktivieren Sie unter **Diese Regel anwenden, wenn,** die Option **Betreff oder Nachrichtentext** \> **Betreff oder Nachrichtentext entspricht diesen Textmustern**.
    
5. Geben Sie im Dialogfeld **Wörter oder Ausdrücke angeben** die folgenden häufig in Massen-E-Mails vorkommenden regulären Ausdrücke nacheinander ein, und klicken Sie auf **OK**, sobald Sie fertig sind: 
    
  - Wenn Sie den Inhalt dieser E-Mail nicht anzeigen können\,
    
  - \\>(sicher )?melden Sie sich ab( hier)?\\</a\\>
    
  - Wenn Sie keine weitere Kommunikation dieser Art mehr erhalten möchten\,
    
  - \\<img height\="?1"? width\="?1"? src\=.?http\://
    
  - So beenden Sie die empfangen von \s+e-mails\:http\ -e-Mails\:http\://
    
  - Um \w+ (E\-?Brief|E?-?Mail|Newsletter) abzubestellen
    
  - keine \w+ E-Mail (mehr )?(gesendet bekommen möchten|erhalten möchten)
    
  - Wenn Sie den Inhalt dieser E-Mail nicht anzeigen können\, klicken Sie hier
    
  - Um sicherzustellen, dass (Ihre täglichen Geschäfte | unsere e-?mails)\, hinzufügen
    
  - Wenn Sie diese E-Mails nicht mehr erhalten möchten
    
  - um Ihre (Abonnementeinstellungen zu ändern|Einstellungen zu ändern oder sich abzumelden)
    
  - klicken Sie (hier zum|auf) Abmelden
    
    **Hinweise**:
    
  - Die obige Liste keine vollständige Reihe von regulären Ausdrücken in Massen-e-Mails. Weitere können je nach Bedarf hinzugefügt oder entfernt werden. Es ist jedoch einen guten Ausgangspunkt.
    
  - Die Suche nach Wörtern oder Textmustern im Betreff oder anderen Kopffelder in der Nachricht tritt auf, *nachdem* die Nachricht aus der MIME-Content-Übertragung Codierung zum Übertragen der binären Nachricht zwischen SMTP-Server in ASCII-Text verwendete Methode decodiert wurden. Sie können Bedingungen oder Ausnahmen für die Suche (in der Regel Base64)-codierten Werte der Betreff oder anderen Kopffelder in Nachrichten. 
    
6. Wählen Sie unter **Gehen Sie folgendermaßen vor...** die Option **Nachrichteneigenschaften ändern** \> **SCL-Bewertung (Spam Confidence Level) festlegen** aus.
    
7. Legen Sie im Dialogfeld **SCL angeben** den SCL auf **5**, **6** oder **9** fest, und klicken Sie auf **OK**.
    
    Wenn der SCL auf 5 oder 6 festgelegt wird, wird die **Spam**-Aktion ausgeführt, und wenn der SCL auf 9 festgelegt wird, wird die Aktion **Nachricht mit hoher Spamwahrscheinlichkeit** ausgeführt, wie in der Inhaltsfilterrichtlinie konfiguriert. Der Dienst führt die in der Inhaltsfilterrichtlinie festgelegte Aktion aus. Die Standardaktion ist, die Nachricht an den Junk-E-Mail-Ordner der Empfänger zuzustellen. Es können allerdings, wie in [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) beschrieben, andere Aktionen konfiguriert werden.
    
    > [!NOTE]
    > Wenn die konfigurierte Aktion die Verschiebung der Nachrichten in das Quarantänefach ist, statt sie an den Junk-E-Mail-Ordner des Empfänger zu senden, wird die Nachricht aufgrund einer Übereinstimmung mit einer Transportregel an die Administrator-Quarantäne gesendet und steht nicht in der Endbenutzer-Spam-Quarantäne oder über Endbenutzer-Spam-Benachrichtigungen zur Verfügung, 
  
    Weitere Informationen zu SCL-Werten im Dienst finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).
    
8. Speichern Sie die Regel.
    
### <a name="create-an-exchange-transport-rule-to-filter-bulk-email-messages-based-on-phrases"></a>Erstellen einer Exchange-Transportregel zum Filtern von Massen-E-Mails basierend auf Ausdrücken

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Geben Sie einen Namen für die Regel ein.
    
4. Klicken Sie auf **Weitere Optionen**. Wählen Sie unter **diese Regel anwenden, wenn** **der Betreff oder Nachrichtentext** \> **Betreff oder Nachrichtentext enthält eines dieser Wörter**.
    
5. Geben Sie im Dialogfeld **Wörter oder Ausdrücke angeben** die folgenden häufig in Massen-E-Mails vorkommenden Ausdrücke nacheinander ein, und klicken Sie auf **OK**, sobald Sie fertig sind: 
    
  - zum Ändern Ihrer Einstellungen oder Abmelden
    
  - Ändern Sie Ihre E-Mail-Einstellungen, oder melden Sie sich ab
    
  - Dies ist eine Werbe-E-Mail
    
  - Sie erhalten diese E-Mail, da Sie ein Abonnement angefordert haben
    
  - klicken Sie hier, um sich abzumelden
    
  - Sie haben diese E-Mail erhalten, da Sie sich dafür angemeldet haben
    
  - Wenn Sie unseren E-Mail-Newsletter nicht mehr erhalten möchten
    
  - melden Sie sich von diesem Newsletter ab
    
  - Wenn Sie Probleme haben, diese E-Mail anzuzeigen
    
  - Dies ist eine Werbeanzeige
    
  - möchten Sie sich abmelden oder Ihre Adresse ändern
    
  - Diese E-Mail als Webseite anzeigen
    
  - Sie erhalten diese E-Mail, da Sie sich dafür angemeldet haben
    
    **Hinweis**: erneut, diese Liste ist eine umfassende Gruppe von Ausdrücke in Massen-e-Mails; nicht Weitere können je nach Bedarf hinzugefügt oder entfernt werden. Es ist jedoch einen guten Ausgangspunkt.
    
6. Wählen Sie unter **Gehen Sie folgendermaßen vor...** die Option **Nachrichteneigenschaften ändern** \> **SCL-Bewertung (Spam Confidence Level) festlegen** aus.
    
7. Legen Sie im Dialogfeld **SCL angeben** den SCL auf **5**, **6** oder **9** fest, und klicken Sie auf **OK**.
    
    Wenn der SCL auf 5 oder 6 festgelegt wird, wird die **Spam**-Aktion ausgeführt, und wenn der SCL auf 9 festgelegt wird, wird die Aktion **Nachricht mit hoher Spamwahrscheinlichkeit** ausgeführt, wie in der Inhaltsfilterrichtlinie konfiguriert. Der Dienst führt die in der Inhaltsfilterrichtlinie festgelegte Aktion aus. Die Standardaktion ist, die Nachricht an den Junk-E-Mail-Ordner der Empfänger zuzustellen. Es können allerdings, wie in [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) beschrieben, andere Aktionen konfiguriert werden.
    
    > [!NOTE]
    > Wenn die konfigurierte Aktion die Verschiebung der Nachrichten in das Quarantänefach ist, statt sie an den Junk-E-Mail-Ordner des Empfänger zu senden, wird die Nachricht aufgrund einer Übereinstimmung mit einer Transportregel an die Administrator-Quarantäne gesendet und steht nicht in der Endbenutzer-Spam-Quarantäne oder über Endbenutzer-Spam-Benachrichtigungen zur Verfügung, 
  
    Weitere Informationen zu SCL-Werten im Dienst finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).
    
8. Speichern Sie die Regel.
    
## <a name="for-more-information"></a>Weitere Informationen

[Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?](what-s-the-difference-between-junk-email-and-bulk-email.md)
  
[BCL-Werte (Bulk Complaint Level)](bulk-complaint-level-values.md)
  
[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  
[Erweiterte spamfilterungsoptionen](advanced-spam-filtering-asf-options.md)
  

