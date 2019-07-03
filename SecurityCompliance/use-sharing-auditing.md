---
title: Überwachen der Freigabe für die Suche nach Ressourcen, die für externe Benutzer freigegeben wurden
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Die Freigabe ist eine wichtige Aktivität in SharePoint Online und OneDrive für Unternehmen. Administratoren können jetzt die Freigabe Überwachung im Office 365 Überwachungsprotokoll verwenden, um zu bestimmen, wie die Freigabe in Ihrer Organisation verwendet wird. '
ms.openlocfilehash: e2865d35e988d8c0e42a6c51f78507db8b170d4c
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435239"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Überwachen der Freigabe für die Suche nach Ressourcen, die für externe Benutzer freigegeben wurden

Die Freigabe ist eine wichtige Aktivität in SharePoint Online und OneDrive für Unternehmen und wird in Office 365 Organisationen häufig verwendet. Administratoren können jetzt die Freigabe Überwachung im Office 365 Überwachungsprotokoll verwenden, um zu bestimmen, wie die Freigabe in Ihrer Organisation verwendet wird. 
  
## <a name="the-sharepoint-sharing-schema"></a>Das SharePoint-Freigabe Schema

Freigabe Ereignisse (ohne Freigaberichtlinie und Freigabe Link Ereignisse) unterscheiden sich in erster Linie von Datei-und ordnerbezogenen Ereignissen: ein Benutzer führt eine Aktion aus, die sich auf einen anderen Benutzer auswirkt. Benutzer a gibt beispielsweise Benutzer B Zugriff auf eine Datei. In diesem Beispiel ist Benutzer A der *stellvertretende Benutzer* , und Benutzer B ist der *Zielbenutzer*. Im SharePoint-Datei Schema wirkt sich die Aktion des handelnden Benutzers nur auf die Datei selbst aus. Wenn Benutzer a eine Datei öffnet, sind die einzigen Informationen, die **** im fileaccessed-Ereignis erforderlich sind, der Benutzer, der fungiert. Um diesen Unterschied zu beheben, gibt es ein separates Schema, das als *SharePoint-Freigabe Schema*bezeichnet wird und in dem weitere Informationen zur Freigabe von Ereignissen erfasst werden. Dadurch wird sichergestellt, dass Administratoren mehr Einblick in die Person haben, die eine Ressource gemeinsam genutzt hat, und den Benutzer, für den die Ressource freigegeben wurde. 
  
Das Freigabe Schema stellt zwei zusätzliche Felder im Überwachungsprotokoll im Zusammenhang mit Freigabe Ereignissen bereit: 
  
- **TargetUserOrGroupName** – speichert den UPN oder den Namen des Zielbenutzers oder der Zielgruppe, für die eine Ressource freigegeben wurde (Benutzer B im vorherigen Beispiel). 
    
- **TargetUserOrGroupType** – gibt an, ob der Zielbenutzer oder die Zielgruppe ein Mitglied, Gast, eine Gruppe oder ein Partner ist. 
    
Diese beiden Felder können zusätzlich zu anderen Eigenschaften aus dem Office 365 Überwachungsprotokoll Schema wie "Benutzer", "Vorgang" und "Datum" die vollständige Übersicht darüber geben, *welcher* Benutzer *welche* Ressource mit *wem* und *wann*freigegeben hat. 
  
Es gibt eine andere Schemaeigenschaft, die für den Freigabe Text wichtig ist. Die **EventData** -Eigenschaft speichert zusätzliche Informationen zu Freigabe Ereignissen. Wenn ein Benutzer beispielsweise eine Website für einen anderen Benutzer freigibt, wird dies erreicht, indem der Zielbenutzer einer SharePoint-Gruppe hinzugefügt wird. Die **EventData** -Eigenschaft erfasst diese zusätzlichen Informationen, um Administratoren Kontext bereitzustellen. 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a>Das SharePoint-Freigabemodell und Freigabe Ereignisse

Die Freigabe wird durch drei separate Ereignisse definiert ****: "sharingset", " **SharingInvitationCreated**" und " **SharingInvitaitonAccepted**". Hier ist der Workflow für die Protokollierung von Freigabe Ereignissen im Office 365 Überwachungsprotokoll. 
  
![Flussdiagramm zur Funktionsweise der Freigabe Überwachung](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
Wenn ein Benutzer (der stellvertretender Benutzer) eine Ressource für einen anderen Benutzer (den Zielbenutzer) freigeben möchte, überprüft SharePoint (oder OneDrive für Unternehmen) zunächst, ob die e-Mail-Adresse des Zielbenutzers bereits einem Benutzerkonto im Verzeichnis der Organisation zugeordnet ist. Wenn sich der Zielbenutzer im Verzeichnis der Organisation befindet, führt SharePoint Folgendes aus:
  
-  Weist sofort die Zielbenutzer Berechtigungen für den Zugriff auf die Ressource zu. 
    
- Sendet eine Freigabe Benachrichtigung an die e-Mail-Adresse des Zielbenutzers.
    
- Protokolliert ein **sharingset** -Ereignis. 
    
 Wenn sich ein Benutzerkonto für den Zielbenutzer nicht im Verzeichnis der Organisation befindet, führt SharePoint Folgendes aus: 
  
- Erstellt eine Freigabeeinladung und sendet Sie an die e-Mail-Adresse des Zielbenutzers.
    
- Protokolliert ein **SharingInvitationCreated** -Ereignis. 
    
    > [!NOTE]
    > Das **SharingInvitationCreated** -Ereignis ist meistens immer mit externer oder Gast Freigabe verbunden, wenn der Zielbenutzer keinen Zugriff auf die freigegebene Ressource hat. 
  
Wenn der Zielbenutzer die an Sie gesendete Freigabeeinladung annimmt (durch Klicken auf den Link in der Einladung), protokolliert SharePoint ein **SharingInvitationAccepted** -Ereignis und weist den Zielbenutzer Berechtigungen für den Zugriff auf die Ressource zu. Weitere Informationen zum Zielbenutzer werden ebenfalls protokolliert, beispielsweise die Identität des Benutzers, an den die Einladung gesendet wurde, und der Benutzer, der die Einladung tatsächlich angenommen hat. In einigen Fällen können diese Benutzer (oder e-Mail-Adressen) unterschiedlich sein. 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a>Vorgehensweise identifizieren von Ressourcen, die für externe Benutzer freigegeben sind

Eine häufige Anforderung an Administratoren ist das Erstellen einer Liste aller Ressourcen, die für Benutzer außerhalb der Organisation freigegeben wurden. Wenn Sie die Freigabe Überwachung in Office 365 verwenden, können Administratoren diese Liste jetzt generieren. Die gehen so:
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>Schritt 1: Suchen nach Freigabe Ereignissen und Exportieren der Ergebnisse in eine CSV-Datei

Der erste Schritt besteht darin, das Office 365 Überwachungsprotokoll nach Freigabe Ereignissen zu durchsuchen. Weitere Informationen (einschließlich der erforderlichen Berechtigungen) zum Durchsuchen des Überwachungsprotokolls finden Sie unter [Durchsuchen des Überwachungsprotokolls im Security #a0 Compliance Center](search-the-audit-log-in-security-and-compliance.md).
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security #a0 Compliance Centers auf **Such**  > **Überwachungsprotokoll Suche**.
    
    Die Seite **Überwachungsprotokoll Suche** wird angezeigt. 
    
4. Klicken Sie unter **Aktivitäten**auf **Freigabe-und Zugriffs Anforderungs Aktivitäten** , um nach Freigabe bezogenen Ereignissen zu suchen. 
    
    ![Wählen Sie unter Aktivitäten die Option Freigabe-und Zugriffs Anforderungs Aktivitäten aus.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  Wählen Sie einen Datums-und Zeitbereich aus, um die Freigabe Ereignisse zu finden, die innerhalb dieses Zeitraums aufgetreten sind. 
    
6. Klicken Sie auf **Suchen** , um die Suche auszuführen. 
    
7. Wenn die Suche abgeschlossen ist und die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse** \> exportieren **alle Ergebnisse herunterladen**.
    
    Nachdem Sie die Option Exportieren ausgewählt haben, wird am unteren Rand des Fensters eine Meldung angezeigt, in der Sie aufgefordert werden, die CSV-Datei zu öffnen oder zu speichern.
    
8. Klicken Sie auf Save **As** **Speichern** \> und speichern Sie die CSV-Datei in einem Ordner auf Ihrem lokalen Computer. 

### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a>Schritt 2: Filtern der CSV-Datei nach Ressourcen, die für externe Benutzer freigegeben sind

Der nächste Schritt besteht darin, die CSV-Datei **** für das sharingset-und das **SharingInvitationCreated** -Ereignis zu filtern und die Ereignisse anzuzeigen, bei denen die **TargetUserOrGroupType** -Eigenschaft **Gast**ist. Verwenden Sie dazu das Tool Power Query Editor in Excel. Eine Schritt-für-Schritt-Anleitung finden Sie unter [exportieren, konfigurieren und Anzeigen von Überwachungsprotokolldaten Sätzen](export-view-audit-log-records.md). 

Nachdem Sie die Anweisungen im vorherigen Thema zum Vorbereiten der CSV-Datei befolgt haben, gehen Sie wie folgt vor:
    
1. Öffnen Sie die CSV-Datei, die Sie mit dem Power Query-Editor vorbereitet haben. 

2. Klicken Sie auf der Registerkarte **Start** auf **#a0 Filter sortieren**, und klicken Sie dann auf **Filter**.
    
3. Deaktivieren Sie in der Dropdownliste **Sortier #a0 Filter** in der Spalte **Vorgänge** alle Optionen, und wählen **** Sie dann freigabeset und **SharingInvitationCreated**aus, und klicken Sie dann auf **OK**.
    
    Excel zeigt die Zeilen für das **sharingset** -und das **SharingInvitationCreated** -Ereignis an. 
    
4. Wechseln Sie zur Spalte mit dem Namen **TargetUserOrGroupType** , und wählen Sie Sie aus. 
    
5. Deaktivieren Sie in der Dropdownliste **Sortier #a0 Filter** die Option alle Auswahlen, wählen Sie **TargetUserOrGroupType: Gast**aus, und klicken Sie dann auf **OK**.
    
    In Excel werden nun die Zeilen für **SharingInvitationCreated** -und **sharingset** -Ereignisse sowie die Position des Zielbenutzers außerhalb Ihrer Organisation angezeigt, da externe Benutzer durch den Wert **TargetUserOrGroupType: Guest**identifiziert werden. 
    
In der folgenden Tabelle sind alle Benutzer in der Organisation aufgeführt, die Ressourcen mit einem Gastbenutzer innerhalb eines angegebenen Datumsbereichs freigegeben haben.
  
![Freigeben von Ereignissen in Office 365 Überwachungsprotokoll](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
Obwohl es nicht in der vorherigen Tabelle enthalten ist, gibt die **objectID** -Eigenschaft die Ressource an, die für den Zielbenutzer freigegeben wurde; zum Beispiel `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
  
> [!TIP]
> Wenn Sie ermitteln möchten, ob einem Gastbenutzer tatsächlich Berechtigungen für den Zugriff auf eine Ressource zugewiesen wurden (im Gegensatz zu den Ressourcen, die für Sie freigegeben wurden), wiederholen Sie die Schritte 2, 3 und 4, und Filtern Sie nach dem **SharingInvitationAccepted** und dem **freigabeset** . Ereignisse in Schritt 5. 
