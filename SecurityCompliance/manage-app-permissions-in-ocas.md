---
title: Verwalten von OAuth-Apps mit Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: OAuth-apps in Office 365-Cloud-App-Sicherheit können Sie apps verwalten, die Ihre Benutzer für die Verwendung mit Office 365 Daten herunterladen
ms.openlocfilehash: ae32e3c6b15f4ad4794a3dd08c3992adaeba655c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603686"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a>Verwalten von OAuth-Apps mit Office 365 Cloud App Security

|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
Erfolgreicher apps und sie diese häufig herunterladen, insbesondere apps, die für die Personensuche Reaktionszeiten werden sparen Sie Zeit, die an die geschäftliche abzurufen oder Schule Informationen zu erleichtern. Jedoch einige apps können ein Sicherheitsrisiko für Ihre Organisation potenziell handeln, je nachdem, welche Informationen sie zugreifen und wie diese Informationen verarbeiten. Mit [Office 365-Cloud-App-Sicherheit](office-365-cas-overview.md)Wenn Sie einen Administrator global oder Sicherheit sind können Sie OAuth-apps für Ihre Organisation verwalten. Sie können sehen, die apps Personen verwenden welche Berechtigungen mit Office 365-Daten, die apps haben, und vieles mehr. 
  
In diesem Artikel wird beschrieben, wo Sie OAuth apps verwalten, wie genehmigen, Sperren oder melden einer app und wie Sie eine app-Abfrage zu erstellen.
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a>So finden Sie die OAuth verwalten apps-Seite

> [!NOTE]
> OAuth-apps werden in der Cloud App Sicherheit in Office 365-Portal verwaltet. Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der folgenden Aufgabe sein. Um weitere finden Sie unter informieren [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
1. Klicken Sie auf das Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung.
  
2. Wählen Sie **untersuchen** \> **OAuth-apps**.<br/>![Wählen Sie im Portal O365 CAS überprüfen.](media/OCAS-OAuthApps.png)<br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a>Was sehen Sie auf der Seite verwalten OAuth-apps

In der folgenden Tabelle werden die Steuerelemente und die verfügbaren Optionen auf der Seite verwalten OAuth apps beschrieben.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|Grundlegende Symbol in der app-Leiste Abfrage  <br/> ![Symbol, grundlegende Abfrageansicht für die Abfrage angibt.](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Wählen Sie diese Option, um die erweiterte Ansicht wechseln.  <br/> (Wenn Sie **grundlegende**angezeigt wird, die erweiterte Ansicht verwenden Sie)  <br/> |
|Erweiterte Symbol in der app-Leiste Abfrage  <br/> ![Symbol, erweiterte Abfrageansicht für die Abfrage angibt.](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Wählen Sie diese Option, um die grundlegende Ansicht wechseln.  <br/> (Wenn Sie **Erweitert**angezeigt wird, werden Sie die grundlegende Ansicht verwenden.)  <br/> |
|Öffnen Sie oder schließen Sie alle Detailsymbol in der app-Liste  <br/> ![Klicken Sie auf dieses Symbol, um das Öffnen oder schließen Sie alle Details für alle apps](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Wählen Sie dieses Symbol, um mehr oder weniger Details zu einzelnen app anzeigen.  <br/> |
|Exportsymbol in der app-Liste  <br/> ![Klicken Sie auf dieses Symbol, um alle Apps eine Csv-Datei exportieren](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Wählen Sie dieses Symbol, um eine CSV-Datei zu exportieren, die eine Liste von apps, die Anzahl von Benutzern für die jeweilige app die app, Berechtigungsstufe, app-Status und Community Verwendung Ebene zugeordneten Berechtigungen enthält.  <br/> |
|Name  <br/> |Verwenden Sie diese auf den Namen der eine App auswählen finden Sie unter dem Namen zum Anzeigen von Informationen, Beschreibung, Publisher, app-Website und app-ID.  <br/> |
|Autorisiert durch  <br/> |Verwenden Sie diese Option, um anzuzeigen, wie viele Benutzer Zugriff auf ihre Office 365-Konto eine app autorisiert haben. Wählen Sie die Nummer, um weitere Informationen, wie eine Liste der Benutzerkonten anzuzeigen.  <br/> |
|Berechtigungsstufe  <br/> ![Symbol, das die Permisiions Ebene für eine app angibt](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Verwenden Sie diese Option, um anzuzeigen, wie viel eine app auf Office 365-Daten zugreifen können. Berechtigungsstufen angeben, **Niedrig**, **Mittel**oder **Hoch**, wobei **Niedrig** hinweisen können, dass die app nur Profile und den Namen des Benutzers zugreift. Wählen Sie die Ebene, um weitere Informationen, wie Berechtigungen erteilt der app, Community-Verwendung und verwandte Aktivität im [Governance Protokoll](suspend-or-restore-an-account-in-ocas.md)anzeigen.<br/> |
|Zuletzt autorisiert <br/> |Verwenden Sie diese Option, um finden Sie unter Datum und Uhrzeit, eine app OAuth letzten Zugriff auf Ihre Organisation Office 365-Daten autorisiert wurde. <br/>  |
|Aktionen<br/>![OAuth-apps](media/OCAS-OAuthAppApproveBanReport.png)<br/> |Verwenden Sie diese finden Sie unter oder um eine app als genehmigt oder gesperrten, markieren eine OAuth-app an Microsoft melden, oder lassen sie als unbestimmten.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Markieren Sie eine app genehmigt hat

Klicken Sie auf der Seite **Verwalten OAuth-apps** suchen Sie die app aus, den, die Sie genehmigen möchten, und wählen Sie das Symbol **Mark app als genehmigt** . 
  
![Wählen Sie die app Mark als genehmigte Symbol](media/OCAS-MarkOAuthApproved.png)
  
Das Symbol wird grün und die app für alle Ihre Office 365-Benutzer freigegeben wird.
  
> [!NOTE]
> Wenn Sie eine app genehmigt markieren, ist es keine Auswirkung auf die Endbenutzer. Visuell Markieren von apps, die genehmigt wurden hilft bei der um sie von apps zu trennen, die noch überarbeitet wurden noch nicht bei. 
  
## <a name="ban-an-app"></a>Sperren einer app

1. Suchen Sie auf der Seite **Verwalten OAuth-apps** die app aus, die Sie sperren möchten, und wählen Sie das Symbol **Mark app als gesperrte** .<br/>![Wählen Sie die app Mark als gesperrte Symbol](media/OCAS-MarkOAuthBanned.png)
  
2. Klicken Sie im Meldungsfeld Benachrichtigung nicht vorhandenen Text geändert werden, oder passen Sie den Text. Wählen Sie, ob, damit Benutzer wissen, dass ihre app gesperrt wurde. <br/>![Die e-Mail-Vorlage für eine gesperrte-app](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. Wählen Sie **app Sperren**.

## <a name="report-an-oauth-app-to-microsoft"></a>Eine app OAuth an Microsoft melden

Wenn Sie eine OAuth-app für die Analyse an Microsoft übermitteln möchten, können Sie diese app melden.

1. Suchen Sie auf der Seite **apps OAuth verwalten** die app aus, die Sie zur Analyse senden möchten.

2. Wählen Sie die vertikale Ellipse und dann auf **Bericht App..**.<br/>![Melden einer OAuth-app](media/OCAS-MarkOAuthReported.png)<br/>

3. Klicken Sie im Dialogfeld **Bericht diese app** verwenden Sie die Dropdown-Liste an, dass Ihr Problem. **Diese app wird böswilliger** ist standardmäßig ausgewählt. Sie können jedoch auf eine der verfügbaren Optionen.<br/>![Melden einer OAuth-app](media/OCAS-ReportOAuthApp.png)<br/>

4. (Empfohlen) Lassen Sie die Option zum ausgewählten Kontakt, und bestätigen (oder bearbeiten) die e-Mail-Adresse aufgeführt.

5. Wählen Sie **Übermitteln** aus. 
    
## <a name="create-an-app-query"></a>Erstellen Sie eine app-Abfrage

Es wird empfohlen, mit der erweiterten Ansicht, der wie folgt aussieht: 

![Erweiterte Ansicht](media/OCAS-OAuthAppsAdvQueryView.png)

In der app-Leiste Abfrage, wenn Sie **Erweitert**, sehen verwenden Sie die Basisansicht. **Erweitert** aus, um die erweiterte Ansicht wechseln klicken (oder tippen). 

![Basisansicht](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. Verwenden Sie in der Adressleiste die Abfrage der Liste **Wählen Sie einen Filter** auf eine Option. 
    - **App** Apps mit bestimmten Namen
    - **App-Status** Apps basierend auf deren Status (genehmigt, gesperrten oder unbestimmt)
    - **Verwenden der Community** Verwenden Sie Apps basierend auf Community Ebenen (seltene, Uncommon oder gemeinsamen)
    - **Berechtigungsstufe** Apps basierend auf bestimmte Berechtigungsstufen 
    - **Berechtigungen** Apps, die bestimmte Berechtigungen erfordern
    - **Publisher**  Apps, die von bestimmten Herausgebern
    - **Benutzer** Apps, die ein bestimmter Benutzer autorisiert
   
2. Wählen Sie **gleich** oder **ungleich**aus, und geben Sie einen Wert für den Filter.
    
3. Um weitere Filter hinzuzufügen, wählen Sie das Pluszeichen (+) (![Fügen Sie ein Filter-Symbol für das Abfragen von apps](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)), und wiederholen Sie die Schritte 2 und 3.
    
4. Wählen Sie zum Entfernen eines Filters aus der x (![Entfernen Sie ein Filter-Symbol für das Abfragen von apps](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) neben dem Namen eines Filters.
    
Die Filter werden automatisch angewendet, und die Liste apps wird entsprechend aktualisiert.
  
## <a name="next-steps"></a>Nächste Schritte

- [Lesen und Ausführen einer Aktion Warnungen](review-office-365-cas-alerts.md)
    
- Überprüfen Sie Ihre [Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)
    

