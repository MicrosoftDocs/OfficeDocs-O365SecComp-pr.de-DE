---
title: Erstellen einer Dokumentlöschrichtlinie
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- SPO160
ms.assetid: 41b2ed73-eb8d-4429-945e-a8197894585a
description: Organisationen müssen häufig Dokumente aufgrund von Konformitäts-, rechtlicher und anderer Bestimmungen für einen bestimmten Zeitraum aufbewahren. Wenn Dokumente aber länger als nötig aufbewahrt werden, kann dies für die Organisation rechtliche Folgen haben.
ms.openlocfilehash: 115e4d7df93d81e7ee5a860f20a00d9cb175f927
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013999"
---
# <a name="create-a-document-deletion-policy"></a>Erstellen einer Dokumentlöschrichtlinie

> [!IMPORTANT]
> Vorwärts verschoben, es wird empfohlen, dass Sie eine Aufbewahrungsrichtlinie oder in das Wertpapier erstellt Etiketten verwenden &amp; Compliance Center anstelle einer dokumentlöschrichtlinie. Dokumentlöschrichtlinien werden weiterhin parallel zu Aufbewahrungsrichtlinien funktionieren, aber wenn Sie müssen beibehalten oder Löschen von Inhalt an einer beliebigen Stelle in Office 365, es wird empfohlen, dass Sie eine Aufbewahrungsrichtlinie zu verwenden. Weitere Informationen finden Sie unter [Verwendung einer Aufbewahrungsrichtlinie anstelle dieser Features](retention-policies.md#use-a-retention-policy-instead-of-these-features). 
  
Organisationen müssen häufig Dokumente aufgrund von Konformitäts-, rechtlicher und anderer Bestimmungen für einen bestimmten Zeitraum aufbewahren. Wenn Dokumente aber länger als nötig aufbewahrt werden, kann dies für die Organisation rechtliche Folgen haben.
  
Sie können mit einer dokumentlöschrichtlinie proaktiv Risiko reduzieren, durch das Löschen von Dokumenten in einer Website nach einem bestimmten Zeitraum – beispielsweise Dokumente löschen in der Benutzer OneDrive for Business-Websites fünf Jahre nach die Dokumente erstellt wurden. 
  
Nach dem Erstellen einer Dokumentlöschrichtlinie können Sie sie einer Vorlage für Websitesammlung zuweisen, damit die Richtlinie für alle Websitesammlungen, die aus dieser Vorlage erstellt werden, verfügbar ist. Sie können außerdem einer bestimmten Websitesammlung eine Richtlinie zuweisen, die alle Richtlinien, die der Vorlage für diese Websitesammlung möglicherweise schon zugewiesen wurden, außer Kraft setzt.
  
![Startseite von Document Deletion Policy Center](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="policy-templates"></a>Richtlinienvorlagen

Sie können eine Dokumentlöschrichtlinie von Grund auf neu erstellen oder eine unserer Beispielrichtlinien verwenden. Im Compliance Policy Center finden Sie Beispielrichtlinien, die Sie entweder sofort verwenden oder als Ausgangsbasis verwenden und umbenennen oder ändern können.
  
![Beispiel von Dokumentlöschrichtlinien](media/IP-Sample-deletion-policies.png)
  
## <a name="examples-of-how-to-use-document-deletion-policies"></a>Beispiele

Eine Websitesammlung oder einer Vorlage für Websitesammlung kann eine weitere Richtlinien zugewiesen, und jeweils die Richtlinien kann eine oder mehrere Regeln verwendet. Allerdings kann nur eine Richtlinie, die pro Website aktiv ist, und kann nur eine Löschregel, die zu einem beliebigen Zeitpunkt für die Bibliotheken, die innerhalb der Website aktiv ist.
  
![Diagramm der Beziehungen zwischen Richtlinien](media/IP-Two-policies-four-rules.png)
  
Außerdem können Sie eine Richtlinie als obligatorisch oder Standard und eine Löschregel als Standardregel auswählen: 
  
- **Obligatorische Richtlinie** Wenn eine Richtlinie als obligatorisch gekennzeichnet ist, kann nur eine Richtlinie zur Websitesammlung oder Vorlage zugewiesen werden. Die Richtlinie als Standard markiert werden muss und auf alle Websites angewendet wird. Websitebesitzer können nicht aus der Richtlinie aufheben.
    
- **Standardrichtlinie** Wenn eine Richtlinie als Standard festgelegt wird, ist die Richtlinie auf allen Websites, die sie zugewiesen wurde keine Aktion erforderlich Websitebesitzer automatisch aktiv.
    
- **Standardregel** Wenn eine Löschregel als Standard festgelegt wird, wird sie automatisch auf alle Bibliotheken auf den Websites angewendet, die die Richtlinie verwenden.
    
Die folgenden Beispiele erläutern, wann Sie möglicherweise eine obligatorische Richtlinie oder Standardrichtlinien und -regeln verwenden sollten.
  
### <a name="example-1-apply-a-single-policy-with-a-single-rule-to-a-site-collection-template"></a>Beispiel 1: Anwenden einer einzelnen Richtlinie mit einer einzelnen Regel auf eine Vorlage für Websitesammlung

Angenommen, Sie möchten eine Dokumentlöschrichtlinie für eine vielfältige Reihe von unstrukturierten Inhalten erzwingen, z. B. alle Websites von OneDrive for Business oder alle Teamwebsites. Wenn Sie sicherstellen möchten, dass eine einzelne Dokumentlöschrichtlinie auf allen Websites aktiv ist, die von einer Vorlage für Websitesammlung erstellt wurde, können Sie wie folgt vorgehen:
  
1. Erstellen Sie eine einzelne Richtlinie mit einer einzelnen Standardlöschregel.
    
2. Legen Sie die Richtlinie als obligatorisch und Standard fest.
    
3. Weisen Sie die Richtlinie einer Vorlage für Websitesammlung zu.
    
In diesem Beispiel wird die Standardlöschregel auf alle Bibliotheken in allen Websitesammlungen angewendet, die aufgrund der Vorlage erstellt wurden, und die Websitebesitzer können die Richtlinie nicht abwählen. Dies ist die einfachste Möglichkeit, um eine Dokumentlöschrichtlinie umfassend und strikt zu erzwingen.
  
![Diagramm einer einzelnen obligatorischen Richtlinie](media/IP-Example-1-doc-deletion-policies.png)
  
### <a name="example-2-apply-a-single-policy-with-several-rules-to-a-site-collection-template"></a>Beispiel 2: Anwenden einer einzelnen Richtlinie mit mehreren Regeln auf eine Vorlage für Websitesammlung

Websitebesitzer wissen oft am besten, welche Art von Inhalten ihre Website enthält, sodass Sie Websitebesitzern die Auswahl der für ihre Website am besten geeigneten Löschregel ermöglichen können. Sie können auch zulassen, dass Websitebesitzer die Richtlinie ganz abwählen.
  
Auch dann können Sie die Richtlinien noch zentral erstellen und verwalten. Sie können auch eine Richtlinie und Regel als den Standard auswählen, sodass eine Richtlinie so lange aktiv ist, bis der Websitebesitzer eine andere auswählt oder die Richtlinie abwählt. Wenn Sie Websitebesitzern diese Flexibilität bieten möchten, können Sie wie folgt vorgehen:
  
1. Erstellen Sie eine einzelne Richtlinie mit mehreren Löschregeln, und legen Sie eine Regel als den Standard fest.
    
2. Legen Sie die Richtlinie als die Standardrichtlinie fest.
    
3. Weisen Sie die Richtlinie einer Vorlage für Websitesammlung zu.
    
Websitebesitzer können eine der alternativen Löschregeln auswählen, die Richtlinie abwählen oder nichts unternehmen und die Standardrichtlinie und -regel übernehmen.
  
![Diagramm einer Richtlinie mit vielen Regeln](media/IP-Example-2-doc-deletion-policies.png)
  
### <a name="example-3-apply-several-policies-with-one-or-more-rules-to-a-site-collection"></a>Beispiel 3: Anwenden mehrerer Richtlinien mit mindestens einer Regel auf eine Websitesammlung

In diesem Beispiel haben Websitebesitzer die höchste Flexibilität, weil sie aus mehreren Richtlinien auswählen und nach der Auswahl einer Richtlinie oft aus mehreren Regeln auswählen können. Eine Richtlinie und eine Regel sind als der Standard festgelegt, sodass eine Richtlinie so lange aktiv ist, bis der Websitebesitzer eine andere auswählt oder die Richtlinie abwählt. Beachten Sie Folgendes: Wenn Sie keine Richtlinie und Regel als Standard festlegen, sind auf der Website keine Richtlinien oder Regeln für die Dokumentbibliotheken aktiv, bis der Websitebesitzer eine Aktion durchführt, um sie auszuwählen und anzuwenden.
  
Im Unterschied zu den vorherigen beiden Beispielen werden diese Richtlinien einer bestimmten Websitesammlung zugewiesen, nicht der Vorlage für Websitesammlung. Die Richtlinien können also gezielter für den Inhalt in einer bestimmten Websitesammlung angepasst werden.
  
Richtlinien und Regeln werden vererbt. Websitebesitzer können für ihre Website eine Richtlinie und Regel auswählen, und alle Unterwebsites erben die Richtlinie von der übergeordneten Website. Ein Besitzer einer Unterwebsite kann aber die Vererbung aufheben, indem er eine andere Richtlinie und Regel auswählt, die wiederum für alle Unterwebsites gilt, bis die Vererbung wieder aufgehoben wird.
  
Um dieses Szenario einzurichten, können Sie wie folgt vorgehen:
  
1. Erstellen Sie mehrere Richtlinien, die jeweils mindestens eine Regel enthalten.
    
2. Legen Sie eine Richtlinie und Regel als den Standard fest.
    
3. Weisen Sie die Richtlinien einer bestimmten Websitesammlung zu.
    
Außerdem werden die Richtlinien und Regeln für eine bestimmte Websitesammlung angepasst, bei der die Websitebesitzer die Vererbung aufheben können, indem sie die Richtlinie und Regel auswählen, die sich am besten für ihre Website eignet.
  
![Diagramm mit vielen Richtlinien und Regeln](media/IP-Example-3-doc-deletion-policies.png)
  
## <a name="create-a-document-deletion-policy"></a>Erstellen einer Dokumentlöschrichtlinie

1. In der Office-365Security &amp; Compliance Center, navigieren Sie zu **Verwaltung der Daten** \> **Aufbewahrung**. Klicken Sie unter **Löschen**klicken Sie auf **dokumentlöschrichtlinien für SharePoint Online und OneDrive für Unternehmen verwalten**. Die Löschung Richtlinie Dokumentcenter wird in einer neuen Registerkarte Browser geöffnet.
    
    Beim ersten Sie über die Sicherheit navigieren &amp; Compliance Center an das Dokumentcenter der Löschvorgang Richtlinie, das Richtlinie Center automatisch für Sie erstellt. Alternativ können Sie das Richtlinie Center, [Erstellen der Websitesammlung](http://go.microsoft.com/fwlink/p/?LinkID=404342) und **Compliance Richtlinie Center** auf der Registerkarte **Enterprise** manuell erstellen. 
    
2. Wählen Sie **Löschrichtlinien**aus.
    
    ![Option "Löschrichtlinien"](media/IP-Deletion-Policies-option.png)
  
3. Wählen Sie **Neues Element** aus.
    
4. Geben Sie einen Namen und eine Beschreibung für die Richtlinie ein. Websitebesitzer wählen eine Richtlinie möglicherweise aufgrund ihres Namens und ihrer Beschreibung aus. Geben Sie daher ausreichende Informationen an, damit sie die richtige Richtlinie auswählen können.
    
5. Um eine Regel zu erstellen, wählen Sie **Neu** aus.
    
6. Geben Sie einen Namen ein, und wählen Sie die folgenden Optionen aus:
    
  - Wählen Sie aus, ob die Regel dauerhaft löschen von Dokumenten oder in den Papierkorb zu löschen. Der Papierkorb stellt ein Sicherheitsnetz endgültigen, bevor ein Element aus einer Website dauerhaft gelöscht wird. Weitere Informationen zu den Papierkorb finden Sie unter [den Papierkorb leeren oder Wiederherstellen die Dateien](http://go.microsoft.com/fwlink/p/?LinkID=404348).
    
  - Wählen Sie aus, ob das Löschdatum ab dem Datum der Dokumenterstellung oder der letzten Dokumentänderung berechnet werden soll.
    
  - Geben Sie die Anzahl der Tage, Monate oder Jahre als Zeitraum ein, nach dem das Dokument gelöscht werden soll.
    
  - Wählen Sie, ob die Regel eine Standardregel ist. Die erste Regel, die Sie erstellen, wird automatisch als die Standardregel festgelegt. Eine Standardregel wird automatisch auf alle Bibliotheken auf den Websites angewendet, die die Richtlinie verwenden.
    
![Seite "Neue Löschregel"](media/IP-New-deletion-rule.png)
  
7. Klicken Sie auf **Speichern**.
    
8. Erstellen Sie zusätzliche Regeln, wenn Sie zulassen möchten, dass Websitebesitzer andere Regeln auswählen und auf ihre Website anwenden können. Falls vorhanden wird die Standardregel angewendet, wenn der Websitebesitzer keine Aktion durchführt.
    
9. Um eine Regel von einer Richtlinie zu entfernen, wählen Sie die Regel aus, klicken Sie auf **Löschen**, und klicken Sie dann auf **OK**.
    
    > [!NOTE]
    > Wenn Sie eine Regel löschen und die Richtlinie kein Standardregel enthält, wird keine Regel wird für diese Richtlinie aktiviert werden – also keine Dokumente werden gelöscht. 
  
![Meldung zum Bestäntigen des Entfernens einer Regel für eine Richtlinie](media/IP-Remove-rule-from-policy-message.png)
  
## <a name="assign-the-document-deletion-policy-to-a-site-collection-template"></a>Zuweisen der Dokumentlöschrichtlinie zu einer Vorlage für Websitesammlung

Durch das Zuweisen einer Richtlinie zu einer Vorlage für Websitesammlung machen Sie die Richtlinie für alle Websitesammlungen verfügbar, die aufgrund dieser Vorlage erstellt werden, einschließlich bereits vorhandener und künftiger Websitesammlungen.
  
Es ist wichtig zu verstehen, dass den Zeitraum an, die für ein Dokument angegeben Löschung die Zeit bedeutet seit das Dokument wurde erstellt oder geändert werden, nicht die Zeit, da die Richtlinie zugewiesen wurde. Wenn Sie die Richtlinie zum ersten Mal zuweisen, werden alle Dokumente in der Website ausgewertet, und wenn sie die Kriterien erfüllen, gelöscht werden. Dies gilt für alle vorhandenen Dokumente, nicht nur neue Dokumente erstellt wurden, da die Richtlinie zugewiesen wurde.
  
1. In das Wertpapier &amp; Compliance Center, navigieren Sie zu **Verwaltung der Daten** \> **Aufbewahrung**. Klicken Sie unter **Löschen**klicken Sie auf **dokumentlöschrichtlinien für SharePoint Online und OneDrive für Unternehmen verwalten**. Die Löschung Richtlinie Dokumentcenter wird in einer neuen Registerkarte Browser geöffnet.
    
2. Wählen Sie **Richtlinienzuweisungen für Vorlagen**.
    
    ![Option "Richtlinienzuweisungen für Vorlagen"](media/IP-Policy-Assignments-for-Templates-option.png)
  
3. Wählen Sie **Neues Element** aus.
    
4. Führen Sie einen der folgenden Schritte aus:
    
  - Um die Richtlinie einer Vorlage für Websitesammlung wie die Teamwebsitevorlage zuzuweisen, wählen Sie **Vorlage für Websitesammlung zuweisen** aus, und wählen Sie die Vorlage für Websitesammlung.
    
  - Um Benutzern ein Drive für Unternehmen die Richtlinie zuzuweisen, wählen Sie in der **OneDrive for Business-Vorlage zuweisen**, unten hervorgehobene.
    
    > [!NOTE]
    > Wenn Sie eine Richtlinie zu einer Vorlage für Websitesammlung zuweisen, wird die Richtlinie für bereits vorhandene Websitesammlungen, die aufgrund dieser Vorlage erstellt wurden, und für künftige Websitesammlungen verfügbar gemacht. 
  
![Seite "Vorlage wählen" mit der Option "OneDrive"](media/IP-Choose-a-template.png)
  
5. Klicken Sie auf **Speichern**.
    
    > [!NOTE]
    > Jede Vorlage kann nur ein Satz von Richtlinien zugewiesen haben. Wenn Sie eine Fehlermeldung ausgegeben sehen, dass diese Vorlage bereits Richtlinien zugewiesen ist, wählen Sie **Abbrechen** \> im linken Navigationsbereich **auf Websitesammlung zuweisen** \> wählen Sie eine Websitesammlung anzeigen und verwalten den Satz von Richtlinien, die bereits sind zugewiesen. 
  
6. Wählen Sie **Zugewiesene Richtlinien verwalten**, wählen Sie die Richtlinien, die Sie zuweisen möchten, und wählen Sie dann, ob eine Richtlinie die Standardrichtlinie ist. Wenn Sie eine Standardrichtlinie festlegen, haben alle Websites zugewiesen, die Richtlinie automatisch die Richtlinie active keine Aktion Websitebesitzer erforderlich.
    
    ![Seite "Richtlinien hinzufügen und verwalten"](media/IP-Add-and-manage-policies-page.png)
  
7. Klicken Sie auf **Speichern**.
    
8. Wenn Sie die Richtlinie auf allen Websites erzwingen möchten, ohne zuzulassen, dass Websitebesitzer sie abwählen können, wählen Sie **Richtlinie als obligatorisch kennzeichnen** aus. Wenn Sie eine Richtlinie als obligatorisch kennzeichnen, kann einer Vorlage für Websitesammlung nur diese einzelne Richtlinie zugewiesen werden. Die Richtlinie muss außerdem als Standard gekennzeichnet werden.
    
    Wenn diese Option ausgegraut ist, wählen Sie **Zugewiesene Richtlinien verwalten** aus, und stellen Sie sicher, dass mindestens eine Richtlinie zugewiesen und als Standard festgelegt ist. 
    
9. Klicken Sie auf **Speichern**.
    
## <a name="assign-the-document-deletion-policy-to-a-site-collection"></a>Zuweisen der Dokumentlöschrichtlinie zu einer Websitesammlung

Durch das Zuweisen einer Richtlinie zu einer bestimmten Websitesammlung machen Sie die Richtlinie nur für diese Websitesammlung verfügbar. Sie können also Richtlinien näher an den Inhalt in der Websitesammlung anpassen. Außerdem setzen Richtlinien, die einer bestimmten Websitesammlung zugewiesen werden, alle Richtlinien, die der Vorlage für diese Websitesammlung zugewiesen sind, außer Kraft. Zum Beispiel setzt eine Richtlinie, die der (aus der Teamwebsitevorlage erstellten) Websitesammlung Vertriebsabteilung zugewiesen ist, alle Richtlinien außer Kraft, die der Teamwebsitevorlage zugewiesen sind.
  
Es ist wichtig zu verstehen, dass den Zeitraum an, die für ein Dokument angegeben Löschung die Zeit bedeutet seit das Dokument wurde erstellt oder geändert werden, nicht die Zeit, da die Richtlinie zugewiesen wurde. Wenn Sie die Richtlinie zum ersten Mal zuweisen, werden alle Dokumente in der Website ausgewertet, und wenn sie die Kriterien erfüllen, gelöscht werden. Dies gilt für alle vorhandenen Dokumente, nicht nur neue Dokumente erstellt wurden, da die Richtlinie zugewiesen wurde.
  
1. In das Wertpapier &amp; Compliance Center, navigieren Sie zu **Verwaltung der Daten** \> **Aufbewahrung**. Wählen Sie unter **Löschen** **dokumentlöschrichtlinien für SharePoint Online und OneDrive für Unternehmen verwalten**. Die Löschung Richtlinie Dokumentcenter wird in einer neuen Registerkarte Browser geöffnet.
    
2. Wählen Sie **Richtlinienzuweisungen für Websitesammlungen**.
    
    ![Option "Richtlinienzuweisungen für Websitesammlungen"](media/IP-Policy-Assignments-for-Site-Collections-option.png)
  
3. Wählen Sie **Neues Element** aus.
    
4. Wählen Sie **eine Websitesammlung auswählen**. Suchen nach Name oder URL der Websitesammlung, wählen Sie die Websitesammlung aus, und klicken Sie auf **Speichern**.
    
    > [!NOTE]
    > Jede Websitesammlung kann nur ein Satz von Richtlinien zugewiesen haben. Wenn eine Fehlermeldung ausgegeben, dass diese Websitesammlung bereits Richtlinien zugewiesen hat angezeigt wird, wählen Sie **Abbrechen** \> **Websitesammlung zuweisen** und wählen Sie eine Websitesammlung anzeigen und verwalten den Satz von Richtlinien, die bereits zugewiesen sind. 
  
![Seite "Websitesammlung auswählen"](media/IP-Choose-a-site-collection-page.png)
  
5. Wählen Sie **Zugewiesene Richtlinien verwalten**, wählen Sie die Richtlinien, die Sie zuweisen möchten, und wählen Sie dann, ob eine Richtlinie die Standardrichtlinie ist. Wenn Sie eine Standardrichtlinie festlegen, haben alle Websites zugewiesen, die Richtlinie automatisch die Richtlinie active keine Aktion Websitebesitzer erforderlich.
    
    ![Seite "Richtlinien hinzufügen und verwalten"](media/IP-Add-and-manage-policies-page.png)
  
6. Klicken Sie auf **Speichern**.
    
7. Wenn Sie die Richtlinie auf allen Websites erzwingen möchten, ohne zuzulassen, dass Websitebesitzer sie abwählen können, wählen Sie **Richtlinie als obligatorisch kennzeichnen** aus. Wenn Sie eine Richtlinie als obligatorisch kennzeichnen, kann einer Websitesammlung nur diese einzelne Richtlinie zugewiesen werden. Die Richtlinie muss außerdem als Standard gekennzeichnet werden.
    
    Wenn diese Option ausgegraut ist, wählen Sie **Zugewiesene Richtlinien verwalten** aus, und stellen Sie sicher, dass mindestens eine Richtlinie zugewiesen und als Standard festgelegt ist. 
    
8. Klicken Sie auf **Speichern**.
    
## <a name="delete-a-policy-assignment"></a>Löschen einer Richtlinienzuweisung

Wenn Sie eine Zuweisung löschen, werden die zugewiesenen Richtlinien nicht mehr auf die Websites in der Websitesammlung oder Vorlage für Websitesammlung angewendet.
  
1. In das Wertpapier &amp; Compliance Center, navigieren Sie zu **Verwaltung der Daten** \> **Aufbewahrung**. Wählen Sie unter **Löschen** **dokumentlöschrichtlinien für SharePoint Online und OneDrive für Unternehmen verwalten**. Die Löschung Richtlinie Dokumentcenter wird in einer neuen Registerkarte Browser geöffnet.
    
2. Wählen Sie entweder **Richtlinienzuweisungen für Vorlagen ** oder **Richtlinienzuweisungen für Websitesammlungen**.
    
3. Wählen Sie das zuweisungselement aus, und klicken Sie auf **Element löschen**.
    
    ![Befehl "Element löschen" für Richtlinienzuweisung](media/IP-Delete-policy-assignment.png)
  
## <a name="delete-a-policy"></a>Löschen einer Richtlinie

Eine Richtlinie, die verwendet wird, kann nicht gelöscht werden. Bevor Sie eine Richtlinie löschen können, müssen Sie zuerst alle Zuordnungen für Websitesammlungen und Vorlagen, die die Richtlinie einbeziehen löschen – finden Sie im vorherigen Abschnitt.
  
1. In das Wertpapier &amp; Compliance Center \> wählen Sie **datenverwaltung** \> **Aufbewahrung** im linken Navigationsbereich \> unter **Löschen** \> **Verwalten Dokument löschen von Richtlinien für SharePoint Online und OneDrive für Unternehmen**. Die Löschung Richtlinie Dokumentcenter wird in einer neuen Registerkarte Browser geöffnet.
    
2. Wählen Sie ** Löschrichtlinien **.
    
    ![Option "Löschrichtlinien"](media/IP-Deletion-Policies-option.png)
  
3. Wählen Sie die Richtlinie aus.
    
4. Klicken Sie im Menüband \> Registerkarte **Elemente** \> **Richtlinie entfernen**.
    
    ![Schaltfläche "Richtlinie entfernen" auf Menüband](media/IP-Remove-Policy-button-on-Ribbon.png)
  
5. Wenn die Richtlinie verwendet wird, werden Sie gefragt, ob Sie möchten die Richtlinie aus allen Websitesammlungen zu entfernen, auf dem sie verwendet wird. Wenn Sie sicher sind, wählen Sie **OK**.
    
    ![Bestätigungsmeldung für "Richtlinie löschen"](media/IP-Delete-policy-confirmation.png)
  
## <a name="see-also"></a>Siehe auch

[Übersicht über Dokumentlöschrichtlinien](document-deletion-policies.md)

[Anwenden oder Entfernen einer Dokumentlöschrichtlinie für eine Website](apply-or-remove-a-document-deletion-policy-for-a-site.md)
 

