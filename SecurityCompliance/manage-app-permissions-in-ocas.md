---
title: Verwalten von app-Berechtigungen, die mit Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: App-Berechtigungen in Office 365-Cloud-App-Sicherheit können Sie apps verwalten, die Ihre Benutzer für die Verwendung mit Office 365 Daten herunterladen
ms.openlocfilehash: 7bda35bbbf3a16cd1d386adcb03b1c7c4176913a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529842"
---
# <a name="manage-app-permissions-using-office-365-cloud-app-security"></a>Verwalten von app-Berechtigungen, die mit Office 365-Cloud-App-Sicherheit

Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
Erfolgreicher apps und sie diese häufig herunterladen, insbesondere apps, die für die Personensuche Reaktionszeiten werden sparen Sie Zeit, die an die geschäftliche abzurufen oder Schule Informationen zu erleichtern. Jedoch einige apps können ein Sicherheitsrisiko für Ihre Organisation potenziell handeln, je nachdem, welche Informationen sie zugreifen und wie diese Informationen verarbeiten. Mit [Office 365-Cloud-App-Sicherheit](office-365-cas-overview.md)Wenn Sie einen Administrator global oder Sicherheit sind können Sie app-Berechtigungen für Ihre Organisation verwalten. Sie können sehen, die apps Personen verwenden welche Berechtigungen mit Office 365-Daten, die apps haben, und vieles mehr. 
  
In diesem Artikel wird beschrieben, wo Sie zum Verwalten von app-Berechtigungen, zum Genehmigen oder Sperren einer app und wie Sie eine app-Abfrage zu erstellen.
  
## <a name="how-to-find-the-manage-app-permissions-page"></a>So finden Sie die Seite Berechtigungen app verwalten
<a name="findappperms"> </a>

> [!NOTE]
> App-Berechtigungen werden in der Cloud App Sicherheit in Office 365-Portal verwaltet. Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der folgenden Aufgabe sein. Um weitere finden Sie unter informieren [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.) 
    
2. Wechseln Sie zu **Benachrichtigungen** \> **Verwalten erweiterte Warnungen**.
    
3. Klicken (oder tippen) **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.
    
    ![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    > [!NOTE]
    > Wenn Office 365-Cloud-App-Sicherheit noch nicht aktiviert ist, können Sie das auf dieser Seite tun. Finden Sie unter [machen Sie sich bereit für Office 365-Cloud-App-Sicherheit](get-ready-for-office-365-cas.md). 
  
4. Wählen Sie **untersuchen** \> **App-Berechtigungen**.
    
    ![Wählen Sie im Portal O365 CAS überprüfen.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
## <a name="what-youll-see-on-the-manage-app-permissions-page"></a>Was sehen Sie auf der Seite verwalten app-Berechtigungen
<a name="whatsonpage"> </a>

In der folgenden Tabelle werden die Steuerelemente und die verfügbaren Optionen auf der Seite Manage app Berechtigungen beschrieben.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|Grundlegende Symbol in der app-Leiste Abfrage  <br/> ![Symbol, der angibt, grundlegende Abfrageansicht für das Abfragen von app-Berechtigungen](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Wählen Sie diese Option, um die erweiterte Ansicht wechseln.  <br/> (Wenn Sie **grundlegende**angezeigt wird, die erweiterte Ansicht verwenden Sie)  <br/> |
|Erweiterte Symbol in der app-Leiste Abfrage  <br/> ![Symbol, das angibt, Abfrageansicht für das Abfragen von app-Berechtigungen für die erweiterte](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Wählen Sie diese Option, um die grundlegende Ansicht wechseln.  <br/> (Wenn Sie **Erweitert**angezeigt wird, werden Sie die grundlegende Ansicht verwenden.)  <br/> |
|Öffnen Sie oder schließen Sie alle Detailsymbol in der app-Liste  <br/> ![Klicken Sie auf dieses Symbol, um das Öffnen oder schließen Sie alle Details für alle apps](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Wählen Sie dieses Symbol, um mehr oder weniger Details zu einzelnen app anzeigen.  <br/> |
|Exportsymbol in der app-Liste  <br/> ![Klicken Sie auf dieses Symbol, um alle Apps eine Csv-Datei exportieren](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Wählen Sie dieses Symbol, um eine CSV-Datei zu exportieren, die eine Liste von apps, die Anzahl von Benutzern für die jeweilige app die app, Berechtigungsstufe, app-Status und Community Verwendung Ebene zugeordneten Berechtigungen enthält.  <br/> |
|Name  <br/> |Verwenden Sie diese auf den Namen der eine App auswählen finden Sie unter dem Namen zum Anzeigen von Informationen, Beschreibung, Publisher, app-Website und app-ID.  <br/> |
|Autorisiert durch  <br/> |Verwenden Sie diese Option, um anzuzeigen, wie viele Benutzer Zugriff auf ihre Office 365-Konto eine app autorisiert haben. Wählen Sie die Nummer, um weitere Informationen, wie eine Liste der Benutzerkonten anzuzeigen.  <br/> |
|Berechtigungsstufe  <br/> ![Symbol, das die Permisiions Ebene für eine app angibt](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Verwenden Sie diese Option, um anzuzeigen, wie viel eine app auf Office 365-Daten zugreifen können. Berechtigungsstufen angeben, **Niedrig**, **Mittel**oder **Hoch**, wobei **Niedrig** hinweisen können, dass die app nur Profile und den Namen des Benutzers zugreift. Wählen Sie die Ebene, um weitere Informationen, wie Berechtigungen erteilt der app, Community-Verwendung und verwandte Aktivität im [Governance Protokoll](suspend-or-restore-an-account-in-ocas.md)anzeigen.<br/> |
|App-Status ( **gesperrten**, **genehmigt**oder **unbestimmt**)  <br/> ![App-Berechtigungen Symbole, nachdem die wird zugelassen, blockiert oder keine Aktion durch den ein Administrator ausgeführt wurde](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)|Hiermit können Sie um eine app als genehmigt oder gesperrten zu markieren, oder lassen sie als unbestimmten.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Markieren Sie eine app genehmigt hat
<a name="approveapp"> </a>

Klicken Sie auf der Seite **app-Berechtigungen verwalten** suchen Sie die app aus, den, die Sie genehmigen möchten,, und wählen Sie das Symbol **Mark app als genehmigt** . 
  
![Wählen Sie die app Mark als genehmigte Symbol](media/dd1b7690-441a-48c9-9c3a-58466513c63d.png)
  
Das Symbol wird grün und die app für alle Ihre Office 365-Benutzer freigegeben wird.
  
> [!NOTE]
> Wenn Sie eine app genehmigt markieren, ist es keine Auswirkung auf die Endbenutzer. Visuell Markieren von apps, die genehmigt wurden hilft bei der um sie von apps zu trennen, die noch überarbeitet wurden noch nicht bei. 
  
## <a name="ban-an-app"></a>Sperren einer app
<a name="banapp"> </a>

1. Suchen Sie die app aus, die Sie sperren möchten, und wählen Sie das Symbol **Mark app als gesperrte** , auf der Seite **app-Berechtigungen verwalten** . 
    
    ![Wählen Sie die app Mark als gesperrte Symbol](media/b9b1c5f6-fde7-46d5-8589-1564d05702b3.png)
  
2. Wählen Sie, ob, damit Benutzer wissen, dass ihre app gesperrt wurde.
    
    (Empfohlen) Um Benutzer wissen zu lassen, wählen Sie **Notify-Benutzer, die Zugriff auf diese gesperrten app gewährt**, fügen Sie hinzu oder bearbeiten Sie eine benutzerdefinierte Benachrichtigung.
    
    Damit können Benutzer wissen nicht, deaktivieren Sie **Notify-Benutzer, die Zugriff auf diese gesperrten app gewährt**.
    
    ![Die e-Mail-Vorlage für eine gesperrte-app](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)
  
3. Wählen Sie **app Sperren**.
    
## <a name="create-an-app-query"></a>Erstellen Sie eine app-Abfrage
<a name="createapp"> </a>

1. In der Abfrage app-Leiste Wenn Sie **Erweitert**angezeigt wird, klicken Sie auf (oder tippen Sie auf) es so wechseln zur erweiterten Ansicht. (Wenn Sie Basic angezeigt wird, verwenden Sie die erweiterte Ansicht, nicht die Ansicht geändert werden.)
    
2. Verwenden Sie der Liste **Wählen Sie einen Filter** , um eine Option zu wählen. In der folgenden Tabelle sind die verfügbaren Filteroptionen zusammengefasst. 
    
|**Verwenden Sie diesen filter**|**Um Folgendes anzuzeigen**|
|:-----|:-----|
|**App** <br/> |Apps mit bestimmten Namen  <br/> |
|**App-Status** <br/> |Apps basierend auf deren Status (genehmigt, gesperrten oder unbestimmt)  <br/> |
|**Community-Verwendung** <br/> |Verwenden Sie Apps basierend auf Community Ebenen (seltene, Uncommon oder gemeinsamen)  <br/> |
|**Berechtigungsstufe** <br/> |Apps basierend auf bestimmte Berechtigungsstufen  <br/> |
|**Berechtigungen** <br/> |Apps, die bestimmte Berechtigungen erfordern  <br/> |
|**Herausgeber** <br/> |Apps, die von bestimmten Herausgebern  <br/> |
|**Benutzer** <br/> |Apps, die ein bestimmter Benutzer autorisiert  <br/> |
   
3. Wählen Sie **gleich** oder **ungleich**aus, und geben Sie einen Wert für den Filter.
    
4. Um weitere Filter hinzuzufügen, wählen Sie das Pluszeichen (+) (![Fügen Sie ein Filter-Symbol für das Abfragen von apps](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)), und wiederholen Sie die Schritte 2 und 3.
    
5. Wählen Sie zum Entfernen eines Filters aus der x (![Entfernen Sie ein Filter-Symbol für das Abfragen von apps](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) neben dem Namen eines Filters.
    
Die Filter werden automatisch angewendet, und die Liste apps wird entsprechend aktualisiert.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="nextsteps"> </a>

- [Lesen und Ausführen einer Aktion Warnungen](review-office-365-cas-alerts.md)
    
- Überprüfen Sie Ihre [Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)
    

