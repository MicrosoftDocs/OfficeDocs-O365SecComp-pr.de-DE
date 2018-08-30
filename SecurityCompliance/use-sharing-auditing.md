---
title: Verwenden Sie die Freigabe der Überwachung in das Überwachungsprotokoll Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Die Freigabe ist eine Aktivität in SharePoint Online und OneDrive für Unternehmen. Administratoren können nun Freigabe Überwachung in der Office 365-Überwachungsprotokoll um zu bestimmen, wie gemeinsame Nutzung in ihrer Organisation verwendet wird. '
ms.openlocfilehash: 511f8b0e61d450659d78177d5b87fac9ee636cd4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529561"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Verwenden Sie die Freigabe der Überwachung in das Überwachungsprotokoll Office 365

Die Freigabe ist eine Aktivität in SharePoint Online und OneDrive für Unternehmen, und es in Office 365-Organisationen weit verbreitet ist. Administratoren können nun Freigabe Überwachung in der Office 365-Überwachungsprotokoll um zu bestimmen, wie gemeinsame Nutzung in ihrer Organisation verwendet wird. 
  
## <a name="the-sharepoint-sharing-schema"></a>Das Freigeben von SharePoint-schema

Anwendungsfreigabe-Ereignisse (außer Freigaberichtlinie und Freigabe link Ereignisse) unterscheiden sich von Datei und Ordner-bezogenen Ereignisse in eine primäre Möglichkeit: ein Benutzer ist einer Aktion, die auf einen anderen Benutzer einige auswirkt. Beispielsweise erhalten Benutzer A Benutzer B Zugriff auf eine Datei. In diesem Beispiel Benutzer A ist der *Benutzer fungiert* und Benutzer B den *Zielbenutzer*. In der SharePoint-Datei Schema wirkt sich auf die handelnden Aktion des Benutzers nur die Datei selbst. Wenn Benutzer A öffnet eine Datei, die nur im Ereignis **FileAccessed** erforderlichen Informationen der handelnden Benutzer hat. Um diesen Unterschied zu beheben, ist es ein separates Schema, *Freigeben von SharePoint-Schema*, das Weitere Informationen zum Freigeben von Ereignissen erfasst wird aufgerufen. Dadurch wird sichergestellt, dass Administratoren über einen besseren Einblick in die, die eine Ressource freigegeben und der Benutzer die Ressource freigegeben wurde. 
  
Das Schema für die Freigabe bietet zwei weitere Felder im Zusammenhang mit der Freigabe von Ereignissen in das Überwachungsprotokoll geschrieben: 
  
- **TargetUserOrGroupName** - speichert die UPN oder den Namen des Zielbenutzers oder der Gruppe, dass eine Ressource für (im vorherigen Beispiel Benutzer B) freigegeben wurde. 
    
- **TargetUserOrGroupType** - bestimmt, ob der Zielbenutzer oder die Gruppe ein Mitglied, Gast, Gruppe oder Partner ist. 
    
Diese beiden Felder, zusätzlich zu anderen Eigenschaften aus der Office 365 audit Log Schema wie Benutzer-, Vorgang und Datum umfassende über *welche* Benutzer shared *welche* Ressourcen mit *denen* und zu welchen *Zeitpunkten*informieren können. 
  
Es gibt eine andere Schemaeigenschaft, die die Freigabe Story wichtig ist. Die **EventData** -Eigenschaft speichert zusätzliche Informationen über die Freigabe von Ereignissen. Beispielsweise wenn ein Benutzer eine Website mit einem anderen Benutzer gemeinsam, dies erfolgt durch den Target-Benutzer einer SharePoint-Gruppe hinzugefügt. Die **EventData** -Eigenschaft erfasst diese zusätzlichen Informationen um Kontext für Administratoren bereitzustellen. 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a>Die SharePoint-Objektmodell Freigabe und Freigeben von Ereignissen

Freigabe wird durch drei separate Ereignisse tatsächlich definiert: **SharingSet**, **SharingInvitationCreated**und **SharingInvitaitonAccepted**. Hier ist der Workflow für Ereignisse wie Freigabe im Überwachungsprotokoll Office 365 angemeldet sind. 
  
![Flussdiagramm der Funktionsweise der Freigabe der Überwachung](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
Wenn ein Benutzer (handelnden Benutzer) Freigeben einer Ressource mit einem anderen Benutzer (Zielbenutzer) möchte, überprüft SharePoint (oder OneDrive für Unternehmen) zuerst, wenn die e-Mail-Adresse des Zielbenutzers bereits ein Benutzerkonto im Verzeichnis der Organisation zugeordnet ist. Wenn die Zielbenutzer im Verzeichnis der Organisation ist, führt SharePoint Folgendes aus:
  
-  Sofort weist die Ziel von Benutzerberechtigungen für die Ressource zugreifen. 
    
- Sendet eine Freigabe Benachrichtigung an die e-Mail-Adresse des Zielbenutzers.
    
- Ein Ereignis **SharingSet** protokolliert. 
    
 Wenn ein Benutzerkonto für die Zielbenutzer im Verzeichnis der Organisation nicht ist, führt SharePoint Folgendes aus: 
  
- Erstellt eine Einladung zur Freigabe, und sendet ihn an die e-Mail-Adresse des Zielbenutzers.
    
- Ein Ereignis **SharingInvitationCreated** protokolliert. 
    
    > [!NOTE]
    > Das Ereignis **SharingInvitationCreated** ist am besten immer zugeordnet, mit externen oder Gast freigeben, wenn der Zielbenutzer Zugriff auf die Ressource hat, die gemeinsam genutzt wurde. 
  
Wenn der Zielbenutzer die Einladung zur Freigabe annimmt, die an sie gesendet wurde (durch Klicken auf den Link in der Einladung), SharePoint meldet ein **SharingInvitationAccepted** -Ereignis und weist die Ziel von Benutzerberechtigungen für die Ressource zugreifen. Weitere Informationen zu den Zielbenutzer wird auch protokolliert, wie die Identität des Benutzers, der die Einladung gesendet wurde und der Benutzer, der tatsächlich die Einladung annehmen. In einigen Fällen können diese Benutzer (oder die e-Mail-Adressen) abweichen. 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a>So identifizieren Sie Ressourcen mit externen Benutzern

Eine allgemeine Anforderung für Administratoren wird eine Liste aller Ressourcen erstellen, die mit Benutzern außerhalb der Organisation freigegeben wurden. Mithilfe der Freigabe in Office 365 Überwachung können Administratoren diese Liste jetzt generieren. Hier ist wie.
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>Schritt 1: Freigeben von Ereignissen suchen und die Ergebnisse in einer CSV-Datei exportieren

Im erste Schritt wird das Überwachungsprotokoll Office 365 für die Freigabe von Ereignissen gesucht. Weitere Informationen (einschließlich der erforderlichen Berechtigungen) zur Suche im Überwachungsprotokolls finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.
    
3. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung**, und klicken Sie auf **Audit Log suchen**.
    
    **Audit Log** Suchseite wird angezeigt. 
    
4. Klicken Sie auf **Freigabe Aktivitäten** aus, die nur für die Freigabe von Ereignissen suchen, klicken Sie unter **Aktivitäten**. 
    
    ![Wählen Sie unter Aktivitäten Freigabe Aktivitäten](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  Wählen Sie einen Bereich für Datum und Uhrzeit, die Freigabe Ereignisse zu erhalten, die innerhalb dieses Zeitraums aufgetreten sind. 
    
6. Klicken Sie auf **Suchen** , um die Suche auszuführen. 
    
7. Wenn die Suche abgeschlossen ist ausgeführt werden und die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse exportieren** \> **alle Ergebnisse herunterladen**.
    
    Nachdem Sie die Export-Option auswählen, wird eine Meldung am unteren Rand des Fensters angezeigt, die Sie zum Öffnen oder speichern die CSV-Datei auffordert.
    
8. Klicken Sie auf **Speichern** \> **Speichern unter** , und speichern Sie die CSV-Datei in einen Ordner auf Ihrem lokalen Computer. 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a>Schritt 2: Filtern der CSV-Datei für Ressourcen mit externen Benutzern

Der nächste Schritt besteht im CSV-Format für die Ereignisse **SharingSet** und **SharingInvitationCreated** filtern und Anzeigen dieser Ereignisse wobei **Gast**ist die **TargetUserOrGroupType** -Eigenschaft. Verwenden Sie die Abfrage Power-Funktion in Excel dazu. Das folgende Verfahren wird in Excel 2016 ausgeführt. 
  
1. Öffnen Sie in Excel 2016 eine leere Arbeitsmappe.
    
2. Klicken Sie auf die Registerkarte **Daten**. 
    
3. Klicken Sie auf **Neue Abfrage** \> **aus Datei** \> **CSV aus**.
    
    ![Wählen Sie auf der Registerkarte Daten neue Abfrage, wählen Sie aus der Datei, und wählen Sie dann aus der CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. Öffnen Sie die CSV-Datei, die Sie heruntergeladen haben, in Schritt 1.
    
    Die CSV-Datei wird im Abfrage-Editor geöffnet. Beachten Sie, dass es vier Spalten: **Zeit**, **Benutzer**, **Aktion**und **Details**. Die **Detail** -Spalte ist ein Feld mit mehreren Eigenschaften. Im nächste Schritt wird eine neue Spalte für die einzelnen Eigenschaften in der Spalte **Details** zu erstellen. 
    
5. Wählen Sie die Spalte **Details** , und klicken Sie dann auf der Registerkarte **Start** auf **Geteilte Spalte** \> **Durch Trennzeichen**.
    
    ![Klicken Sie auf der Registerkarte Start auf geteilte Spalte, und klicken Sie dann auf durch Trennzeichen](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. Klicken Sie im Fenster **Geteilte Spalte durch Trennzeichen** folgendermaßen Sie vor: 
    
      - Wählen Sie unter **Wählen Sie aus, oder geben Sie als Trennzeichen** **Komma**ein.
    
      - Wählen Sie unter **Teilen** **bei jedem Vorkommen von Trennzeichen**.
    
7. Klicken Sie auf **OK**.
    
    Die **Detail** -Spalte wird in mehreren Spalten aufgeteilt. Jede neue Spalte heißt **Detail.1**, **Detail.2**, **Detail.3**und So weiter. Sie sehen, dass die Werte in jeder Zelle in den Spalten **Detail.n** mit dem Namen der Eigenschaft als Präfix vorangestellt ist; Angenommen, **Vorgang: SharingSet**, **Vorgang: SharingInvitationAccepted**und **Vorgang: SharingInvitationCreated**.
    
    ![Die Detail-Spalte wird in mehreren Spalten für jede Eigenschaft aufgeteilt.](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. Klicken Sie auf der Registerkarte **Datei** auf **Schließen &amp; Load** schließen Sie den Abfrage-Editor, und öffnen Sie die Datei in einer Excel-Arbeitsmappe. 
    
    Im nächste Schritt ist zum Filtern der Datei, um nur die Ereignisse **SharingSet** und **SharingInvitationCreated** anzeigen. 
    
9. Wechseln Sie auf der Registerkarte **Start** , und wählen Sie dann aus der Spalte **Aktion** . 
    
10. In der **sortieren &amp; Filter** Dropdown-Listenfeld, löschen Sie alle ausgewählten Optionen, klicken Sie dann wählen **SharingSet** und **SharingInvitationCreated**, und klicken Sie auf **OK**.
    
    Excel zeigt die Zeilen für die Ereignisse **SharingSet** und **SharingInvitationCreated** . 
    
11. Besuchen Sie die Spalte mit dem Namen **Detail.17** (oder Spalte die **TargetUserOrGroupType** -Eigenschaft enthält), und wählen Sie sie aus. 
    
12. In der **sortieren &amp; Filter** Dropdown-Listenfeld, löschen Sie alle ausgewählten Optionen, wählen Sie **TargetUserOrGroupType:Guest**, und klicken Sie auf **OK**.
    
    Excel zeigt jetzt die Zeilen für **SharingInvitationCreated** und **SharingSet** -Ereignisse und den Zielbenutzer außerhalb Ihrer Organisation, da externe Benutzer den Wert **TargetUserOrGroupType:Guest**identifiziert werden. 
    
Die folgende Tabelle zeigt alle Benutzer in der Organisation, die freigegebenen Ressourcen mit einem Gäste Benutzer innerhalb eines angegebenen Zeitraums.
  
![Überwachungsprotokoll Sharing Ereignisse in Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
Obwohl es nicht in der vorherigen Tabelle enthalten ist, identifiziert der Spalte **Detail.10** (oder Spalte die **ObjectId** -Eigenschaft enthält) Ressource, die für die Zielbenutzer freigegeben wurde; beispielsweise `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
  
> [!TIP]
> Wenn Sie bestimmen möchten wenn Gast wurde tatsächlich zugewiesen Berechtigungen zum Zugriff auf eine Ressource (also nicht nur die Ressourcen, wo sie freigegeben), wiederholen Sie die Schritte 10, 11 und 12 und filter für die **SharingInvitationAccepted** und **SharingSet **Ereignisse in Schritt 10. 
