---
title: Überwachung Berichte
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2a762db5-e1c9-4c09-aa8e-bef49ce97209
description: Verwenden Sie Überwachung finden Sie unter welche-e-Mails Compliance überprüfen muss Berichte und, die durchgeführt werden soll.
ms.openlocfilehash: e18d083c0aad8be945c628516e593462da8e3898
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529049"
---
# <a name="supervision-reports"></a>Überwachung Berichte

Aufsichtsrichtlinien definieren, die Kommunikation in Ihrer Organisation benötigen Überprüfung für die Kompatibilität, und führt, die diese Reviews (engl.). Verwenden Sie die Überwachung Berichte, um die Überprüfung Aktivität Ebene der Richtlinie und Bearbeiter finden Sie unter. Für jede Richtlinie können Sie auch live Statistiken auf den aktuellen Status der Überprüfung Aktivität anzeigen. [Erfahren Sie mehr über aufsichtsrichtlinien](configure-supervision-policies.md) . 
  
> [!NOTE]
> Verwenden aufsichtsrichtlinien erfordert ein Abonnement von Office 365 E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und Überwachung ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Sie können die Überwachung Berichte verwenden:
  
- Stellen Sie sicher, dass Ihre Richtlinien wie gewünscht funktionieren. 
    
- Erfahren Sie, wie viele e-Mails zur Überprüfung identifiziert werden können.
    
- Erfahren Sie, wie viele e-Mail-Nachrichten nicht kompatibel sind, und welche überprüfen übergeben werden. Diese Informationen helfen Ihnen die Entscheidung für Optimieren Ihrer Richtlinien oder Ändern der Anzahl der Bearbeiter.
    
## <a name="view-the-supervision-report"></a>Anzeigen des Berichts zu Überwachung

1. Melden Sie sich bei der [Sicherheit &amp; Compliance Center](https://protection.office.com/) mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation, die über Berechtigungen zum Anzeigen von Berichten Aufsicht verfügt. 
    
2. Wechseln Sie zu **Berichte** \> **Dashboard**. Sehen Sie ein reporting-Widget für Überwachung und anderen Berichten haben Sie Zugriff auf.
    
3. Klicken Sie auf das Widget **Überwachung** , um die Seite detaillierter Bericht zu öffnen. 
    
> [!NOTE]
> Wenn Sie auf die Seite **Berichte** zugreifen nicht, überprüfen Sie, ob Sie ein Mitglied der Rollengruppe generelle Überprüfung sind wie unter [Überwachung in Ihrer Organisation zur Verfügung stellen](configure-supervision-policies.md#SRavailable). In dieser Rolle Gruppe können Sie erstellen und Verwalten der Überwachung eingeschlossen werden Richtlinien, und führen Sie den Bericht. 
  
## <a name="how-to-use-the-report"></a>So verwenden Sie den Bericht

Wenn eine Richtlinie für Überwachung eine e-Mail zur Überprüfung erkannt wird, wird die e-Mail in der Prüfer Aufsicht Ordner in Outlook und Outlook übermittelt Web app. Dieser Bericht listet die Namen der einzelnen Richtlinien und die Anzahl der Kommunikation in den einzelnen Phasen des Prozesses überprüfen.
  
Verwenden Sie den Bericht an:
  
- Anzeigen von Daten für alle oder bestimmte Richtlinien.
    
- Anzeigen von Daten, die gruppiert nach Tag Typs (beispielsweise konform, Questionable usw.), Bearbeiter oder Nachrichtentyp.
    
- Exportieren von Daten in eine CSV-Datei.
    
- Filtern von Daten basierend auf Aktivität Nachbereitung, Tagtyp, Reviewer, Nachrichtentyp.
    
Es folgt eine Aufschlüsselung der Werte, die möglicherweise in der Spalte **Typ Tag** angezeigt. 
  
|**Tagtyp**|**Was bedeutet, dass**|
|:-----|:-----|
|Nicht überprüft.  <br/> |Die Anzahl der e-Mails, die noch nicht überprüft. Diese e-Mails werden zur Überprüfung im Outlook-Ordner Überwachung der Prüfer erwartet.  <br/> |
|Kompatible  <br/> |Die Anzahl der e-Mails überprüft und als kompatibel markiert. Es ist keine weitere Aktion erforderlich.  <br/> |
|Fragwürdige  <br/> |Die Anzahl der e-Mails überprüft und fragwürdige gekennzeichnet. Dies fungiert als Flag. andere Bearbeiter helfen überprüfen, ob eine e-Mail-Nachricht für die Einhaltung der Untersuchung benötigt.  <br/> |
|Nicht kompatible (aktiv)  <br/> |Die Anzahl der nicht konforme e-Mails, die derzeit Bearbeiter untersuchen.  <br/> |
|Nicht-kompatible (aufgelöst)  <br/> |Die Anzahl der nicht konforme e-Mails, die Bearbeiter untersucht und aufgelöst.  <br/> |
   
## <a name="more-details"></a>Weitere details

- Aufsichtsrichtlinien müssen zuerst bereitgestellt werden, bevor sie in diesem Bericht angezeigt werden.
    
- Wenn Richtlinien gelöscht werden, werden die Verlaufsdaten weiterhin angezeigt. Allerdings sie "nicht vorhandene Richtlinie" gekennzeichnet sind, und die **Export** -Funktion ist nicht verfügbar. 
    
- Wenn der Bericht keine Daten standardmäßig angezeigt wird, möglicherweise, weil der aktuellen Datumsbereich anzuzeigenden Daten besitzt. Verwenden Sie in diesen Fällen das **Filter** -Steuerelement, um den Datumsbereich zu ändern. 
    

