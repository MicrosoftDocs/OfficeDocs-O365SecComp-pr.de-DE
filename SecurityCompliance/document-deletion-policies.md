---
title: Übersicht über Dokumentlöschrichtlinien
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/12/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- SPO160
ms.assetid: 55e8d858-f278-482b-a198-2e62d6a2e6e5
description: Ihre Organisation Fällen müssen Sie für eine bestimmte Zeitspanne aufgrund von Kompatibilitäts-, rechtliche, Dokumente oder andere geschäftlichen Anforderungen beibehalten werden. Wenn Ihre Organisation Dokumente länger als erforderlich gespeichert sind, erstellen Sie unnötige rechtliche Risiken. Sie können mit einer dokumentlöschrichtlinie proaktiv Risiko reduzieren, durch das Löschen von Dokumenten in einer Website nach einem bestimmten Zeitraum – beispielsweise Dokumente löschen in der Benutzer OneDrive for Business-Websites fünf Jahre nach die Dokumente erstellt wurden.
ms.openlocfilehash: 495dd781c56e25e884d47f72a7e48410ea340208
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013659"
---
# <a name="overview-of-document-deletion-policies"></a>Übersicht über Dokumentlöschrichtlinien

> [!IMPORTANT]
> Vorwärts verschoben, es wird empfohlen, dass Sie eine Aufbewahrungsrichtlinie oder in das Wertpapier erstellt Etiketten verwenden &amp; Compliance Center anstelle einer dokumentlöschrichtlinie. Dokumentlöschrichtlinien werden weiterhin parallel zu Aufbewahrungsrichtlinien funktionieren, aber wenn Sie müssen beibehalten oder Löschen von Inhalt an einer beliebigen Stelle in Office 365, es wird empfohlen, dass Sie eine Aufbewahrungsrichtlinie zu verwenden. Weitere Informationen finden Sie unter [Verwendung einer Aufbewahrungsrichtlinie anstelle dieser Features](retention-policies.md#use-a-retention-policy-instead-of-these-features).
  
Ihre Organisation Fällen müssen Sie für eine bestimmte Zeitspanne aufgrund von Kompatibilitäts-, rechtliche, Dokumente oder andere geschäftlichen Anforderungen beibehalten werden. Wenn Ihre Organisation Dokumente länger als erforderlich gespeichert sind, erstellen Sie unnötige rechtliche Risiken. Sie können mit einer dokumentlöschrichtlinie proaktiv Risiko reduzieren, durch das Löschen von Dokumenten in einer Website nach einem bestimmten Zeitraum – beispielsweise Dokumente löschen in der Benutzer OneDrive for Business-Websites fünf Jahre nach die Dokumente erstellt wurden.
  
Dokumentlöschrichtlinien werden leistungsfähige noch flexibler – Sie können beispielsweise:
  
- Erlauben Sie Websitebesitzern, die von Ihnen erstellten und verwalteten Richtlinien auszuwählen. Sie können Websitebesitzern auch erlauben, eine Richtlinie abzuwählen, falls sie für ihre Inhalte nicht geeignet sein sollte.
    
- Erzwingen Sie eine einzelne obligatorische Richtlinie auf allen Websites in einer Websitesammlung, wie z. B. OneDrive for Business-Websites, oder erzwingen Sie eine Richtlinie auf allen Websitesammlungen, die aus einer bestimmten Vorlage für Websitesammlung, z. B. die Teamwebsitevorlage, erstellt wurde.
    
- Stellen Sie eine Standardrichtlinie mit einer Standardregel bereit, die automatisch angewendet wird, ohne dass die Websitebesitzer eine Aktion durchführen müssen.
    
- Erstellen Sie eine Richtlinie mit mehreren Löschregeln, aus denen ein Websitebesitzer wählen kann.
    
Sie erstellen und Verwalten von dokumentlöschrichtlinien mithilfe der Löschvorgang Richtlinie Dokumentcenter, die finden Sie unter **Beibehaltung** in die Office 365-Sicherheit &amp; Compliance Center. Alternativ können Sie das Richtlinie Center manuell durch [Erstellen der Websitesammlung](https://go.microsoft.com/fwlink/p/?LinkID=404342) , und wählen **Compliance Richtlinie Center** auf die Registerkarte **Unternehmen** erstellen. Jeder Mandant kann nur ein Dokument löschen Richtlinie Center, und es werden automatisch erstellt werden, wenn Sie über die Sicherheit starten &amp; Compliance Center. 
  
![Startseite von Document Deletion Policy Center](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="when-to-use-document-deletion-policies"></a>Zeitpunkt für die Verwendung von Dokumentlöschrichtlinien

Zusätzlich zu Dokumentlöschrichtlinien enthält Office 365 die folgenden Aufbewahrungsrichtlinien für Websiteinhalte:
  
- [Datensatzverwaltung](https://go.microsoft.com/fwlink/p/?LinkID=404250)
    
- [Informationsverwaltungsrichtlinien für Inhaltstypen, Listen und Bibliotheken](https://go.microsoft.com/fwlink/p/?LinkID=404239)
    
- [Websiterichtlinien](https://go.microsoft.com/fwlink/p/?LinkID=404242)
    
Die einzelnen Richtlinientypen eignen sich am besten für einen bestimmten Website- oder Datentyp. Angenommen, Ihre Organisation hat eine hochgradig strukturierte Website, die Inhaltstypen verwendet, wie z. B. eine Finanzwebsite für Verträge oder eine Wissensdatenbank für Artikel. In diesem Fall können Sie Inhaltstyprichtlinien verwenden. Oder angenommen, Ihre Organisation muss rechtliche Dokumente aufbewahren. In diesem Fall könnten Sie Inhaltstypen und ein Datenarchiv verwenden, um einen Dateiplan zu implementieren.
  
Dokumentlöschrichtlinien ersetzen nicht Records Management oder Informationen Informationsverwaltungsrichtlinien, Sie die am besten mit strukturierten Daten und Inhaltstypen. In diesem Fall sollten Sie dokumentlöschrichtlinien verwenden, wenn Sie die automatische Löschung unstrukturierte Daten wie OneDrive for Business-Websites und Teamwebsites Allgemein verwalten müssen.
  
![Diagramm der Aufbewahrungsrichtlinien für Websiteinhalte](media/IP-Retention-policies-for-site-content.png)
  
Wenn Sie eine Dokumentlöschrichtlinie auf eine Website anwenden, die bereits Inhaltstyprichtlinien oder Informationsverwaltungsrichtlinien für eine Liste oder Bibliothek verwendet, werden diese Richtlinien ignoriert, solange die Dokumentlöschrichtlinie aktiv ist. Das heißt, für eine Website dürfen nur Richtlinien verwendet werden, die für strukturierten oder unstrukturierten Inhalt bestimmt sind, aber nicht beides. Weitere Informationen dazu, wie Dokumentlöschrichtlinien andere Richtlinien außer Kraft setzen, finden Sie unter [Apply or remove a document deletion policy for a site](apply-or-remove-a-document-deletion-policy-for-a-site.md).
  
Im Unterschied zu anderen Richtlinien eignen sich Dokumentlöschrichtlinien nur für Dokumentbibliotheken, nicht Listen.
  
## <a name="deletion-policies-and-rules"></a>Löschrichtlinien und -regeln

Eine Dokumentlöschrichtlinie enthält mindestens eine Löschregel, die Folgendes festlegt:
  
- Zeitraum bis zum Löschen.
    
- Legt fest, ob das Löschdatum ab dem Zeitpunkt der Erstellung oder der letzten Änderung des Dokuments berechnet werden soll.
    
- Legt fest, ob das Dokument permanent oder in den Papierkorb gelöscht werden soll.
    
Wenn eine Richtlinie mehr als eine Regel enthält, können Websitebesitzer die Regel auswählen, die sich am besten für ihren Inhalt eignet.
  
![Seite "Neue Löschregel"](media/IP-New-deletion-rule.png)
  
## <a name="policies-and-assignments"></a>Richtlinien und Zuweisungen

Nachdem Sie eine dokumentlöschrichtlinie erstellt haben, können Sie ihn auf eine Vorlage für Websitesammlung zuweisen – beispielsweise Sie können eine Richtlinie zuweisen die OneDrive for Business-Vorlage, damit sie jedes Benutzers OneDrive Website enthält. Wenn Sie eine Richtlinie einer Vorlage für Websitesammlung zuweisen, gilt dies für alle Websitesammlungen, die bereits erstellt aus der Vorlage, zusätzlich zur alle Websitesammlungen in der Zukunft aus dieser Vorlage erstellt.
  
![Seite "Vorlage wählen" mit der Option "OneDrive"](media/IP-Choose-a-template.png)
  
Sie können außerdem einer bestimmten Websitesammlung eine Richtlinie zuweisen. Dadurch werden alle Richtlinien, die dieser Vorlage für Websitesammlung bereits zugewiesen wurden, außer Kraft gesetzt. Sie können zum Beispiel der Teamwebsitevorlage Richtlinien zuweisen, sie dann aber außer Kraft setzen, indem Sie einen anderen Satz von Richtlinien auf eine bestimmte Websitesammlung anwenden, die aus dieser Vorlage erstellt wurde.
  
### <a name="one-mandatory-policy-or-several-policies-to-choose-from"></a>Eine obligatorische Richtlinie oder mehrere Methoden zur Auswahl

Beim Zuweisen einer Richtlinie können Sie sie als obligatorisch festlegen, sodass nur diese Richtlinie zugewiesen werden kann und auf alle Websites in der Websitesammlung angewendet wird. Websitebesitzer können eine obligatorische Richtlinie nicht abwählen, d. h. Dokumente auf der Website sind auf jeden Fall von der Löschrichtlinie betroffen.
  
Statt eine einzelne Richtlinie als obligatorisch zu kennzeichnen, können Sie einer Websitesammlung auch mehrere Richtlinien zuweisen. Dadurch kann jeder Websitebesitzer die Richtlinie, die auf die Website angewendet werden soll, auswählen oder ganz abwählen. Sie können zum Beispiel eine Richtlinie für allgemeine Geschäftsdokumente und eine für finanzielle Dokumente erstellen, die einen anderen Aufbewahrungszeitplan haben. Ein Websitebesitzer weiß oft am besten, welchen Inhalt die Website enthält und welche Dokumentlöschrichtlinie angewendet werden soll. Auf jede Website kann immer nur eine Richtlinie angewendet werden.
  
### <a name="one-rule-or-several-rules-to-choose-from"></a>Eine Regel oder mehrere Regeln zur Auswahl

Jede Richtlinie kann wiederum viele Regeln enthalten – beispielsweise möglicherweise eine Löschung Richtlinie für allgemeine Geschäftsdokumente zwei Regeln:
  
- Dokumente, bei denen es nicht basierend auf Vorschriften oder laufender Geschäftsprozesse aufzubewahren sollte nicht mehr als ein Jahr nach Erstellung aufbewahrt werden.
    
- Dokumente, die für aktive fortlaufende Geschäftsprozesse und länger als ein Jahr benötigt werden, sollten nicht länger als drei Jahre nach ihrer Erstellung aufbewahrt werden.
    
Websitebesitzer kann bestimmen, dass ihre Website allgemeine Business enthält Dokumente, wählen Sie diese Richtlinie löschen aus, und wählen Sie dann die entsprechende Regel aus der Richtlinie. Sie können nur eine Regel auswählen, aus der Richtlinie, die derzeit auf der Website (also nicht von einer Richtlinie) angewendet wird, und die Regel gilt für alle Dokumentbibliotheken in der Website.
  
## <a name="the-relationship-of-site-collections-policies-and-rules"></a>Beziehung zwischen Websitesammlungen, Richtlinien und Regeln

Die grundlegende Beziehung ist:
  
Eine Websitesammlung oder einer Vorlage für Websitesammlung kann eine oder mehrere Richtlinien zugewiesen haben, und jeweils die Richtlinien kann eine oder mehrere Regeln verwendet. Allerdings kann nur eine Richtlinie, die pro Website aktiv ist, und kann nur eine Löschregel, die zu einem beliebigen Zeitpunkt für die Bibliotheken, die innerhalb der Website aktiv ist.
  
![Diagramm der Beziehungen zwischen Richtlinien](media/IP-Two-policies-four-rules.png)
  
## <a name="document-deletion-policies-are-inherited"></a>Dokumentlöschrichtlinien werden vererbt.

So wie Berechtigungen, Navigation und viele andere Websitefunktionen werden auch Dokumentlöschrichtlinien vererbt. Websitebesitzer können für ihre Website eine Richtlinie und Regel auswählen, und alle Unterwebsites erben die Richtlinie von der übergeordneten Website. Ein Besitzer einer Unterwebsite kann die Vererbung aufheben, indem er eine andere Richtlinien- und Regelkombination auswählt, und diese Richtlinie gilt dann für alle Unterwebsites, bis die Vererbung wieder aufgehoben wird.
  
## <a name="assigning-document-deletion-policies-for-the-first-time"></a>Erstmaliges Zuweisen von Dokumentlöschrichtlinien

Es ist wichtig zu verstehen, dass den Zeitraum an, die für ein Dokument angegeben Löschung die Zeit bedeutet seit das Dokument wurde erstellt oder geändert werden, nicht die Zeit, da die Richtlinie zugewiesen wurde. Beispielsweise können Sie erstellen eine dokumentlöschrichtlinie, die Dokumente löscht dauerhaft zwei Jahre, nachdem sie erstellt wurden, und weisen Sie die Richtlinie einer Vorlage für Websitesammlung aus der mehrere Websitesammlungen vier oder fünf Jahren erstellt wurden. In diesem Fall ist es wahrscheinlich, dass die vorhandene Websitesammlungen viele Dokumente enthalten, die bereits älter als die zwei Jahre durch die Löschung-Richtlinie angegeben sind – das bedeutet viel Inhalt bald nach dem Zuweisen der dokumentlöschrichtlinie für das erste gelöscht wird Zeit.
  
Wenn Sie die Richtlinie zum ersten Mal zuweisen, werden alle Dokumente auf der Website ausgewertet und, falls sie die Kriterien erfüllen, gelöscht. Dies trifft auf alle vorhandenen Dokumente zu, nicht nur auf neue Dokumente, die seit der Zuweisung der Richtlinie erstellt wurden. Denken Sie auch daran, dass der Zeitraum das Alter eines Dokuments darstellt, nicht den Zeitraum ab der erstmaligen Zuweisung der Richtlinie.
  
Daher sollten Sie vor dem erstmaligen Zuweisen einer Richtlinie zu einer Website zunächst das Alter des vorhandenen Inhalts und die möglichen Auswirkungen der Richtlinie auf diesen vorhandenen Inhalt bedenken. Sie können außerdem vor dem Zuweisen die Websitebesitzer über die neue Richtlinie informieren, um ihnen Zeit zur Auswertung der möglichen Auswirkungen zu geben.
  
## <a name="time-lag-for-propagating-policies"></a>Zeitverzögerung für die Verbreitung von Richtlinien

Nachdem Sie einer Websitesammlung Richtlinien zugewiesen haben, können Websitebesitzer über den Link **Dokumentlöschrichtlinien** auf der Seite **Websiteeinstellungen** die für die Website verfügbaren Richtlinien anzeigen und anwenden. 
  
Der Link **Dokumentlöschrichtlinien** wird nicht angezeigt, es sei denn, für die Websitesammlung Richtlinien zugewiesen wurden. Darüber hinaus der Link wird nicht angezeigt, unmittelbar nachdem Richtlinien, zu der Website zugewiesen sind – dauert bis zu 24 Stunden aus, wenn die Richtlinien zugewiesen sind, wenn der Link **Dokumentlöschrichtlinien** angezeigt wird. 
  
## <a name="permissions"></a>Berechtigungen

Mitglieder Ihres Kompatibilitätsteams, die das Document Deletion Policy Center verwenden, benötigen Berechtigungen für das Policy Center und die Websitesammlungen, auf die die Richtlinien angewendet werden sollen. Wir empfehlen, dass Sie wie folgt vorgehen:
  
1. Erstellen Sie eine Sicherheitsgruppe, die alle Benutzer der der Löschvorgang Richtlinie Dokumentcenter enthält – wahrscheinlich Compliance richtlinienverwaltung Team. Weitere Informationen finden Sie unter [Manage Mail-Enabled-Sicherheitsgruppen](https://go.microsoft.com/fwlink/p/?LinkID=404345) . 
    
2. Im Dokument löschen Richtlinie Center Websitesammlung Besitzerberechtigungen der Sicherheitsgruppe zuweisen. Weitere Informationen finden Sie unter [Berechtigungen für Administratoren von Websitesammlungen](https://go.microsoft.com/fwlink/p/?LinkID=404346) . 
    
3. Weisen Sie in jeder Websitesammlung, der Sie Dokumentlöschrichtlinien zuweisen müssen, Websitesammlungs-Besitzerberechtigungen zu der Sicherheitsgruppe zu.
    
## <a name="how-document-deletion-policies-work-with-hold-policies"></a>Funktionsweise von Dokumentlöschrichtlinien und Aufbewahrungsrichtlinien

Eine Aufbewahrungsrichtlinie stellt sicher, dass alle Inhalte für einen bestimmten Zeitraum archiviert werden, während eine Dokumentlöschrichtlinie sicherstellt, dass alle Inhalte nach einem bestimmten Zeitraum gelöscht werden.
  
Wenn Sie Dokumente für einen bestimmten Zeitraum aufbewahren müssen, verwenden Sie eine Aufbewahrungsrichtlinie gemeinsam mit einer Löschrichtlinie. Sie könnten zum Beispiel Dokumente nach ihrer letzten Änderung drei Jahre lang aufbewahren und dann eine Löschrichtlinie festlegen, um sie drei Jahre nach ihrer letzten Änderung zu löschen.
  
Beachten Sie, dass eine Löschrichtlinie eine Aufbewahrungsrichtlinie nicht außer Kraft setzen kann. Wenn eine Website archiviert und ein Dokument aufgrund einer Dokumentlöschrichtlinie gelöscht wird, dann wird das Dokument im permanenten Dokumentarchiv aufbewahrt, so als ob es manuell gelöscht worden sei.
  
## <a name="see-also"></a>Siehe auch

[Anwenden oder Entfernen einer Dokumentlöschrichtlinie für eine Website](apply-or-remove-a-document-deletion-policy-for-a-site.md)

[Erstellen einer Dokumentlöschrichtlinie](create-a-document-deletion-policy.md)


