---
title: Verwalten von OAuth-Apps mit Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: OAuth apps in Office 365 Cloud-App-Sicherheit helfen Ihnen, die apps zu verwalten, die Ihre Benutzer für die Verwendung mit Office 365-Daten herunterladen
ms.openlocfilehash: 510cb64f2267c99b783f86a69f7b7a84db8d84dd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219825"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a>Verwalten von OAuth-Apps mit Office 365 Cloud App Security

|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |[Starten der Bereitstellung](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
People Love apps und Sie laden Sie oft, insbesondere apps, die Leute denken, wird Zeit sparen, indem Sie es einfacher, ihre Arbeit oder Schulinformationen zu erhalten. Einige apps können jedoch möglicherweise ein Sicherheitsrisiko für Ihre Organisation darstellen, je nachdem, auf welche Informationen Sie zugreifen und wie diese Informationen verarbeitet werden. Mit [Office 365 Cloud App Security](office-365-cas-overview.md), wenn Sie ein globaler oder Sicherheitsadministrator sind, können Sie OAuth-Apps für Ihre Organisation verwalten. Sie können sehen, welche apps Benutzer mit Office 365-Daten verwenden, welche Berechtigungen diese apps haben und vieles mehr. 
  
In diesem Artikel wird beschrieben, wo Sie OAuth-apps verwalten, wie Sie eine APP genehmigen, verbieten oder melden und wie Sie eine APP-Abfrage erstellen.
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a>So finden Sie die Seite "Verwalten von OAuth-Apps"

> [!NOTE]
> OAuth-apps werden im Sicherheitsportal der Office 365 Cloud App verwaltet. Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die folgende Aufgabe ausführen zu können. Weitere Informationen finden Sie unter [Permissions in the Office &amp; 365 Security Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
1. Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.
  
2. Wählen Sie **OAuth-apps** **untersuchen** \> aus.<br/>![Wählen Sie im O365-CAS-Portal untersuchen aus.](media/OCAS-OAuthApps.png)<br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a>Was Sie auf der Seite "Verwalten von OAuth-Apps" sehen

In der folgenden Tabelle werden die Steuerelemente und Optionen beschrieben, die auf der Seite OAuth-apps verwalten zur Verfügung stehen.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|Basis Symbol in der APP-Abfrage Leiste  <br/> ![Symbol für einfache Abfrageansicht für Abfragen](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Wählen Sie diese Option aus, um zur erweiterten Ansicht zu wechseln.  <br/> (Wenn Sie " **Basic**" sehen, verwenden Sie die erweiterte Ansicht)  <br/> |
|Symbol "Erweitert" in der APP-Abfrage Leiste  <br/> ![Symbol, das die erweiterte Abfrageansicht für Abfragen angibt](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Wählen Sie diese Option aus, um zur Standardansicht zu wechseln.  <br/> (Wenn Sie " **erweitert**" sehen, verwenden Sie die Standardansicht.)  <br/> |
|Öffnen oder Schließen aller Details-Symbol in der APP-Liste  <br/> ![Klicken Sie auf dieses Symbol, um alle Details für alle apps zu öffnen oder zu schließen.](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Wählen Sie dieses Symbol aus, um mehr oder weniger Details zu den einzelnen apps anzuzeigen.  <br/> |
|Export Symbol in der APP-Liste  <br/> ![Klicken Sie auf dieses Symbol, um eine CSV-Datei aller apps zu exportieren.](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Wählen Sie dieses Symbol aus, um eine CSV-Datei zu exportieren, die eine Liste der apps, die Anzahl der Benutzer für jede APP, Berechtigungen für die APP, Berechtigungsstufe, App-Status und Community-Nutzungs Ebene enthält.  <br/> |
|Name  <br/> |Verwenden Sie diese Option, um den Namen einer APP anzuzeigen. Wählen Sie den Namen aus, um weitere Informationen anzuzeigen, beispielsweise die Beschreibung, den Herausgeber, die APP-Website und die APP-ID.  <br/> |
|Autorisiert von  <br/> |Verwenden Sie diese Informationen, um zu sehen, wie viele Benutzer eine APP autorisiert haben, auf Ihr Office 365-Konto zuzugreifen. Wählen Sie die Nummer aus, um weitere Informationen anzuzeigen, beispielsweise eine Liste von Benutzerkonten.  <br/> |
|Berechtigungsstufe  <br/> ![Symbol, das die permisiions-Ebene für eine APP angibt](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Verwenden Sie diese, um zu sehen, wie viel Zugriff eine APP auf Office 365-Daten hat. Berechtigungsstufen deuten auf **niedrig**, **Mittel**oder **hoch**hin, wobei **Low** darauf hindeuten kann, dass die app nur auf das Profil und den Namen eines Benutzers zugreift. Wählen Sie die Ebene aus, um weitere Informationen anzuzeigen, beispielsweise Berechtigungen, die der APP erteilt wurden, die Community-Nutzung und die zugehörigen Aktivitäten im [Steuerungsprotokoll](suspend-or-restore-an-account-in-ocas.md).<br/> |
|Zuletzt autorisiert <br/> |Verwenden Sie diese, um das Datum und die Uhrzeit anzuzeigen, zu der eine OAuth-App zuletzt autorisiert wurde, um auf die Office 365-Daten Ihrer Organisation zuzugreifen. <br/>  |
|Aktionen<br/>![OAuth-apps](media/OCAS-OAuthAppApproveBanReport.png)<br/> |Verwenden Sie diese Funktion, um eine App als genehmigt oder gesperrt zu markieren, eine OAuth-APP an Microsoft zu melden oder Sie als unbestimmt zu belassen.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Kennzeichnen einer App als genehmigt

Suchen Sie auf der Seite **OAuth-apps verwalten** die APP, die Sie genehmigen möchten, und klicken Sie auf das Symbol **App als genehmigt markieren** . 
  
![Auswählen des Symbols "App als genehmigt"](media/OCAS-MarkOAuthApproved.png)
  
Das Symbol wird grün, und die APP wird für alle Office 365-Benutzer genehmigt.
  
> [!NOTE]
> Wenn Sie eine App als genehmigt markieren, hat dies keinen Einfluss auf den Endbenutzer. Wenn Sie die genehmigten apps visuell markieren, können Sie diese von apps trennen, die noch nicht überprüft wurden. 
  
## <a name="ban-an-app"></a>Sperren einer APP

1. Suchen Sie auf der Seite **OAuth-apps verwalten** die APP, die Sie verbieten möchten, und klicken Sie auf das Symbol **App als gesperrt markieren** .<br/>![Auswählen des Symbols app AS Banned](media/OCAS-MarkOAuthBanned.png)
  
2. Behalten Sie im Feld Benachrichtigungsmeldung den vorhandenen Text bei, oder passen Sie den Text an. Legen Sie fest, ob die Benutzer wissen möchten, dass Ihre APP gesperrt wurde. <br/>![Die e-Mail-Vorlage für eine gesperrte App](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. Wählen Sie **Ban-App**aus.

## <a name="report-an-oauth-app-to-microsoft"></a>Melden einer OAuth-APP an Microsoft

Wenn Sie eine OAuth-App zur Analyse an Microsoft übermitteln möchten, können Sie diese APP melden.

1. Suchen Sie auf der Seite **OAuth-apps verwalten** die APP, die Sie zur Analyse übermitteln möchten.

2. Wählen Sie die vertikalen Auslassungspunkte aus, und wählen Sie dann **Bericht-app...**.<br/>![Melden einer OAuth-App](media/OCAS-MarkOAuthReported.png)<br/>

3. Geben Sie im Dialogfeld **diese APP melden** in der Dropdownliste ihre Bedenken an. Standardmäßig ist **diese APP bösartig** ausgewählt. Sie können jedoch eine der anderen verfügbaren Optionen auswählen.<br/>![Melden einer OAuth-App](media/OCAS-ReportOAuthApp.png)<br/>

4. Empfohlen Halten Sie die Option, Kontakt mit Ihnen ausgewählt, und bestätigen (oder bearbeiten) Sie die e-Mail-Adresse aufgeführt.

5. Wählen Sie **Übermitteln** aus. 
    
## <a name="create-an-app-query"></a>Erstellen einer APP-Abfrage

Es wird empfohlen, die erweiterte Ansicht zu verwenden, die wie folgt aussieht: 

![Erweiterte Ansicht](media/OCAS-OAuthAppsAdvQueryView.png)

Wenn Sie in der APP-Abfrage Leiste auf **erweitert**sehen, verwenden Sie die Standardansicht. Klicken (oder tippen) Sie auf **erweitert** , um zur erweiterten Ansicht zu wechseln. 

![Einfache Ansicht](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. Verwenden Sie in der Abfrage Leiste die Liste **Filter auswählen** , um eine Option auszuwählen. 
    - **App** Apps mit bestimmten Namen
    - **App-Status** Apps basierend auf Ihrem Status (genehmigt, gesperrt oder nicht festgelegt)
    - **Community-Verwendung** Apps, die auf Community-Nutzungs Ebenen basieren (seltene, ungewöhnliche oder häufige)
    - **Berechtigungsstufe** Apps basierend auf bestimmten Berechtigungsstufen 
    - **Berechtigungen** Apps, die bestimmte Berechtigungen erfordern
    - **Herausgeber**  Apps von bestimmten Herausgebern
    - **Benutzer** Apps, die ein bestimmter Benutzer autorisiert hat
   
2. Wählen Sie **gleich** oder **nicht gleich**aus, und geben Sie dann einen Wert für Ihren Filter an.
    
3. Um weitere Filter hinzuzufügen, wählen Sie das Pluszeichen (![Hinzufügen eines Filter Symbols für die Abfrage von apps](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)), und wiederholen Sie die Schritte 2 und 3.
    
4. Wenn Sie einen Filter entfernen möchten, wählen Sie das x (![Entfernen eines Filter Symbols für die Abfrage von apps](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) neben einem Filternamen.
    
Die Filter werden automatisch angewendet, und die apps-Liste wird entsprechend aktualisiert.
  
## <a name="next-steps"></a>Nächste Schritte

- [Überarbeiten und Aktionen für Warnungen](review-office-365-cas-alerts.md)
    
- Über [Wachen von Webprotokollen und Datenquellen für Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    

