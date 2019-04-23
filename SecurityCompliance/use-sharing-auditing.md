---
title: Überwachen der Freigabe für die Suche nach Ressourcen, die für externe Benutzer freigegeben wurden
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Die Freigabe ist eine wichtige Aktivität in SharePoint Online und OneDrive for Business. Administratoren können jetzt die Freigabe Überwachung im Office 365-Überwachungsprotokoll verwenden, um zu bestimmen, wie die Freigabe in Ihrer Organisation verwendet wird. '
ms.openlocfilehash: 08b511acdf74edac5b2d595d1b60bdd84d630918
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958246"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Überwachen der Freigabe für die Suche nach Ressourcen, die für externe Benutzer freigegeben wurden

Die Freigabe ist eine wichtige Aktivität in SharePoint Online und OneDrive for Business und wird in Office 365-Organisationen am häufigsten verwendet. Administratoren können jetzt die Freigabe Überwachung im Office 365-Überwachungsprotokoll verwenden, um zu bestimmen, wie die Freigabe in Ihrer Organisation verwendet wird. 
  
## <a name="the-sharepoint-sharing-schema"></a>Das SharePoint-Freigabe Schema

Freigabe Ereignisse (ohne Freigaberichtlinien und Freigabe verknüpfungsereignisse) unterscheiden sich von Datei-und ordnerbezogenen Ereignissen auf eine primäre Art und Weise: ein Benutzer führt eine Aktion aus, die für einen anderen Benutzer etwas bewirkt. Benutzer A gibt beispielsweise dem Benutzer B Zugriff auf eine Datei. In diesem Beispiel ist Benutzer A der *amtierende Benutzer* und Benutzer B der *Zielbenutzer*. Im SharePoint-Datei Schema wirkt sich die Aktion des handelnden Benutzers nur auf die Datei selbst aus. Wenn Benutzer A eine Datei öffnet, ist der handelnde Benutzer nur **** für das fileaccessed-Ereignis erforderlich. Um diesen Unterschied zu beheben, gibt es ein separates Schema, das als *SharePoint-Freigabe Schema*bezeichnet wird und weitere Informationen zu Freigabe Ereignissen erfasst. Auf diese Weise wird sichergestellt, dass Administratoren mehr über die Freigabe einer Ressource und den Benutzer verfügen, für den die Ressource freigegeben wurde. 
  
Das Freigabe Schema enthält zwei zusätzliche Felder im Überwachungsprotokoll im Zusammenhang mit Freigabe Ereignissen: 
  
- **TargetUserOrGroupName** -speichert den UPN oder den Namen des Zielbenutzers oder der Gruppe, für die eine Ressource freigegeben wurde (Benutzer B im vorherigen Beispiel). 
    
- **TargetUserOrGroupType** – gibt an, ob der Zielbenutzer oder die Gruppe Mitglied, Gast, Gruppe oder Partner ist. 
    
Diese beiden Felder, zusätzlich zu anderen Eigenschaften aus dem Office 365-Überwachungsprotokoll Schema wie Benutzer, Vorgang und Datum, können den vollständigen Bericht darüber mitteilen, *welche* Benutzer *welche* Ressource für *wen* und *wann*freigegeben haben. 
  
Es gibt eine andere Schemaeigenschaft, die für die Freigabe Story wichtig ist. Die **EventData** -Eigenschaft speichert zusätzliche Informationen zu Freigabe Ereignissen. Wenn ein Benutzer beispielsweise eine Website für einen anderen Benutzer freigibt, wird dies erreicht, indem der Zielbenutzer einer SharePoint-Gruppe hinzugefügt wird. Die **EventData** -Eigenschaft erfasst diese zusätzlichen Informationen, um den Kontext für Administratoren bereitzustellen. 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a>Das SharePoint-Freigabemodell und Freigabe Ereignisse

Die Freigabe wird tatsächlich durch drei separate Ereignisse definiert ****: sharingset, **SharingInvitationCreated**und **SharingInvitaitonAccepted**. Hier ist der Arbeitsablauf für die Protokollierung von Freigabe Ereignissen im Office 365-Überwachungsprotokoll. 
  
![Ablaufdiagramm zur Funktionsweise der Freigabe Überwachung](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
Wenn ein Benutzer (der amtierende Benutzer) eine Ressource für einen anderen Benutzer (den Zielbenutzer) freigeben möchte, überprüft SharePoint (oder OneDrive for Business) zunächst, ob die e-Mail-Adresse des Zielbenutzers bereits einem Benutzerkonto im Verzeichnis der Organisation zugeordnet ist. Wenn sich der Zielbenutzer im Verzeichnis der Organisation befindet, führt SharePoint Folgendes aus:
  
-  Weist den Zielbenutzer sofort Berechtigungen für den Zugriff auf die Ressource zu. 
    
- Sendet eine Freigabe Benachrichtigung an die e-Mail-Adresse des Zielbenutzers.
    
- Protokolliert ein **sharingset** -Ereignis. 
    
 Wenn sich ein Benutzerkonto für den Zielbenutzer nicht im Verzeichnis der Organisation befindet, führt SharePoint Folgendes aus: 
  
- Erstellt eine Freigabeeinladung und sendet Sie an die e-Mail-Adresse des Zielbenutzers.
    
- Protokolliert ein **SharingInvitationCreated** -Ereignis. 
    
    > [!NOTE]
    > Das **SharingInvitationCreated** -Ereignis wird immer mit externer oder Gast Freigabe verknüpft, wenn der Zielbenutzer keinen Zugriff auf die freigegebene Ressource hat. 
  
Wenn der Zielbenutzer die Freigabeeinladung akzeptiert, die Ihnen gesendet wird (durch Klicken auf den Link in der Einladung), protokolliert SharePoint ein **SharingInvitationAccepted** -Ereignis und weist die Zielbenutzer Berechtigungen für den Zugriff auf die Ressource zu. Außerdem werden zusätzliche Informationen zum Zielbenutzer protokolliert, beispielsweise die Identität des Benutzers, an den die Einladung gesendet wurde, und der Benutzer, der die Einladung tatsächlich akzeptiert hat. In einigen Fällen können diese Benutzer (oder e-Mail-Adressen) unterschiedlich sein. 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a>Identifizieren von Ressourcen, die für externe Benutzer freigegeben sind

Eine allgemeine Anforderung für Administratoren ist das Erstellen einer Liste aller Ressourcen, die für Benutzer außerhalb der Organisation freigegeben wurden. Mithilfe der Freigabe Überwachung in Office 365 können Administratoren diese Liste generieren. Die gehen so:
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>Schritt 1: Suchen nach Freigabe Ereignissen und Exportieren der Ergebnisse in eine CSV-Datei

Der erste Schritt besteht darin, im Office 365-Überwachungsprotokoll nach Freigabe Ereignissen zu suchen. Weitere Informationen (einschließlich der erforderlichen Berechtigungen) zum Durchsuchen des Überwachungsprotokolls finden Sie unter [Durchsuchen des Überwachungsprotokolls im Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md).
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security & Compliance Centers auf **Such**  > **Überwachungsprotokoll Suche**.
    
    Die Seite **Überwachungsprotokoll Suche** wird angezeigt. 
    
4. Klicken Sie unter **Aktivitäten**auf **freigabeaktivitäten** , um nur nach Freigabe Ereignissen zu suchen. 
    
    ![Wählen Sie unter Aktivitäten die Option freigabeaktivitäten aus.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  Wählen Sie einen Datums-und Uhrzeitbereich aus, um nach den Freigabe Ereignissen zu suchen, die in diesem Zeitraum aufgetreten sind. 
    
6. Klicken Sie auf **Suchen** , um die Suche auszuführen. 
    
7. Wenn die Suche abgeschlossen ist und die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse** \> exportieren, um **alle Ergebnisse herunterzuladen**.
    
    Nachdem Sie die Option Exportieren ausgewählt haben, wird unten im Fenster eine Meldung angezeigt, in der Sie aufgefordert werden, die CSV-Datei zu öffnen oder zu speichern.
    
8. Klicken Sie auf Speichern unter, und speichern Sie die CSV-Datei in einem Ordner auf dem lokalen Computer. **** **** \> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a>Schritt 2: Filtern der CSV-Datei für Ressourcen, die für externe Benutzer freigegeben sind

Der nächste Schritt besteht darin, die CSV-Datei **** für die freigabeset-und **SharingInvitationCreated** -Ereignisse zu filtern und die Ereignisse anzuzeigen, bei denen die **TargetUserOrGroupType** -Eigenschaft **Gast**ist. Hierzu verwenden Sie die Power Query-Funktion in Excel. Das folgende Verfahren wird in Excel 2016 ausgeführt. 
  
1. Öffnen Sie in Excel 2016 eine leere Arbeitsmappe.
    
2. Klicken Sie auf die Registerkarte **Daten** . 
    
3. Klicken Sie auf **neue Abfrage** \> **aus Datei** \> **aus CSV**.
    
    ![Wählen Sie auf der Registerkarte Daten die Option Neue Abfrage aus, wählen Sie aus Datei aus, und wählen Sie dann aus CSV aus.](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. Öffnen Sie die CSV-Datei, die Sie in Schritt 1 heruntergeladen haben.
    
    Die CSV-Datei wird im Abfrage-Editor geöffnet. Beachten Sie, dass es vier Spalten gibt: **Zeit**, **Benutzer**, **Aktion**und **Detail**. Die **Detail** -Spalte ist ein Multi-Property-Feld. Im nächsten Schritt erstellen Sie eine neue Spalte für jede der Eigenschaften in der **Detail** Spalte. 
    
5. Wählen Sie die Spalte **Detail** aus, und klicken Sie dann auf der Registerkarte **Start** auf **Spalte** \> **nach Trennzeichen**teilen.
    
    ![Klicken Sie auf der Registerkarte Start auf Spalte teilen, und klicken Sie dann auf nach Trennzeichen](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. Gehen Sie in der **Spalte geteilt durch Trennzeichen** wie folgt vor: 
    
      - Wählen Sie unter Trenn **Zeichen auswählen oder eingeben**die Option **Komma**aus.
    
      - Wählen **** Sie unter Split **bei jedem Vorkommen des Trennzeichens**.
    
7. Klicken Sie auf **OK**.
    
    Die **Detail** Spalte wird in mehrere Spalten aufgeteilt. Jede neue Spalte heißt **Detail. 1**, **Detail. 2**, **Detail. 3**usw. Sie werden feststellen, dass die Werte in jeder Zelle in den Spalten **Details. n** dem Namen der Eigenschaft vorangestellt werden. beispielsweise **Operation: sharingset**, **Operation: SharingInvitationAccepted**und **Operation: SharingInvitationCreated**.
    
    ![Die Detail Spalte wird in mehrere Spalten aufgeteilt, eine für jede Eigenschaft.](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. Klicken Sie auf der Registerkarte **Datei** auf **Laden schließen &amp; ** , um den Abfrage-Editor zu schließen und die Datei in einer Excel-Arbeitsmappe zu öffnen. 
    
    Im nächsten Schritt wird die Datei so gefiltert, dass nur die **freigabeset** -und **SharingInvitationCreated** -Ereignisse angezeigt werden. 
    
9. Wechseln Sie zur Registerkarte **Start** , und wählen Sie dann die Spalte **Aktion** aus. 
    
10. Deaktivieren Sie in der Dropdownliste **Sortier &amp; Filter** alle Optionen, und wählen Sie dann **freigabeset** und **SharingInvitationCreated**aus, und klicken Sie auf **OK**.
    
    Excel zeigt die Zeilen für die **freigabeset** -und **SharingInvitationCreated** -Ereignisse an. 
    
11. Wechseln Sie zu der Spalte mit dem Namen **Detail. 17** (oder einer Spalte, die die **TargetUserOrGroupType** -Eigenschaft enthält), und wählen Sie Sie aus. 
    
12. Deaktivieren Sie in der Dropdownliste **Sortier &amp; Filter** alle Optionen, und wählen Sie dann **TargetUserOrGroupType: Gast**aus, und klicken Sie auf **OK**.
    
    Excel zeigt nun die Zeilen für **SharingInvitationCreated** -und **Sharing** -Ereignisse an, wobei sich der Zielbenutzer außerhalb Ihrer Organisation befindet, da externe Benutzer durch den Wert **TargetUserOrGroupType: Guest**identifiziert werden. 
    
In der folgenden Tabelle sind alle Benutzer in der Organisation aufgeführt, die in einem bestimmten Zeitraum Ressourcen für einen Gastbenutzer freigegeben haben.
  
![Freigabe Ereignisse in Office 365-Überwachungsprotokoll](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
Obwohl es nicht in der vorherigen Tabelle enthalten ist, gibt die **Detail. 10** -Spalte (oder die Spalte mit der **objectID** -Eigenschaft) die Ressource an, die für den Zielbenutzer freigegeben wurde; Beispiel `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
  
> [!TIP]
> Wenn Sie ermitteln möchten, wann ein Gastbenutzer tatsächlich Berechtigungen für den Zugriff auf eine Ressource zugewiesen hat (im Gegensatz zu den Ressourcen, die für diesen freigegeben wurden), wiederholen Sie die Schritte 10, 11 und 12, und Filtern Sie nach dem **SharingInvitationAccepted** und dem freigabeset. ** **Ereignisse in Schritt 10. 
