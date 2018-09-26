---
title: Filtern von Daten beim Importieren von PST-Dateien in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Verwenden Sie das neue Feature für intelligente Import in den Import von Office 365-Dienst zum Filtern der Elemente, die tatsächlich an die Ziel-Postfächer importiert. Intelligente importieren können Sie die proaktiv entscheiden, welche Daten zu importieren und zu bleiben. Intelligente Import außerdem Insights auf die Daten, die Sie zu Office 365 importieren. '
ms.openlocfilehash: c90d9df62c7d8c411196b283acec37959fc95e57
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038198"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a>Filtern von Daten beim Importieren von PST-Dateien in Office 365

Verwenden Sie das neue Feature für intelligente Import in den Import von Office 365-Dienst zum Filtern der Elemente in PST-Dateien, die tatsächlich an die Ziel-Postfächer importiert. Hier wird die Funktionsweise:
  
- Nachdem Sie erstellen und senden einen Auftrag für Import von PST-Datei, werden PST-Dateien in einen Bereich Azure-Speicher in der Microsoft-Cloud hochgeladen.
    
- Office 365 analysiert die Daten in die PST-Dateien auf sichere Weise durch das Identifizieren von des Alters der Postfachelemente und die verschiedenen Nachrichtentypen in PST-Dateien enthalten.
    
- Wenn die Analyse abgeschlossen ist, und die Daten zum Importieren bereit sind, müssen Sie die Option zum Importieren alle Daten in die PST-Dateien oder erhöhen, die Daten, die durch Festlegen von Filtern, die steuern, welche Daten importierten ruft importiert wird. Sie können beispielsweise an:
    
  - Importieren Sie nur die Elemente mit einem bestimmten Alter.
    
  - Importieren von ausgewählten Nachrichtentypen.
    
  - Ausschließen von Nachrichten von bestimmten Personen gesendet oder empfangen.
    
- Nach der Konfiguration der filtereinstellungen importiert Office 365 nur die Daten, die an die Ziel-Postfächer in den Importauftrag angegebenen Filterkriterien erfüllt.
    
In der folgenden Grafik veranschaulicht den intelligenten importieren, und die Aufgaben, die ausgeführt werden und die Aufgaben, die von Office 365 durchgeführt werden.
  
![Der intelligente Importvorgang in Office 365](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Die Schritte in diesem Thema wird vorausgesetzt, dass Sie einen Auftrag für Import von PST-Datei im Office 365 importieren-Dienst mithilfe von Netzwerk hochladen oder Laufwerk des Protokollversands erstellt haben. Eine schrittweise Anleitung finden Sie in den folgenden Themen:
    
  - [Verwenden des Netzwerkuploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md)
    
  - [Verwenden des Laufwerkversands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- Nach dem Erstellen einer Importauftrag mithilfe von Netzwerk-Upload Seite des Status für den Importauftrag für den Import in Office 365-Sicherheit &amp; Compliance Center auf festgelegt ist **Analysis ausgeführt**, was bedeutet, dass Office 365 die Daten in die PST-Dateien analysiert, die Sie hochgeladen. Klicken Sie auf **Aktualisieren**![aktualisieren](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) zum Aktualisieren des Status für den Importauftrag. 
    
- Für Laufwerk ausgeliefert Importaufträge werden die Daten von Office 365 analysiert nach Microsoft Mitarbeiter im Rechenzentrum Ihrer Festplatte empfangen und Hochladen von PST-Dateien in den Bereich der Azure-Speicher für Ihre Organisation.
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a>Filtern von Daten, die auf Postfächer importiert Ruft

Nach dem Erstellen eine PST-Datei importieren Auftrag, befolgen Sie diese Schritte, um die Daten zu filtern, bevor Sie es in Office 365 importieren.
  
1. Wechseln Sie zu [https://protection.office.com/](https://protection.office.com/) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Im linken Bereich der Office 365-Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> **Importieren**.
    
    Der Importaufträge für Ihre Organisation werden auf der Seite **Importieren** aufgelistet. Beachten Sie, dass der **Analyse abgeschlossen** Wert in der Spalte **Status** der Importaufträge angibt, die haben von Office 365 analysiert wurde und für die Sie importieren bereit sind. 
    
    ![Analyse abgeschlossen Status gibt an, dass es sich bei Office 365 die Daten in PST-Dateien analysiert hat](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. Klicken Sie auf **importieren zu Office 365** für den Importauftrag aus, dem Sie ausführen möchten. 
    
    Ausfliegen Seite wird mit Informationen zu den PST-Dateien und andere Informationen zu den Importauftrag angezeigt.
    
4. Klicken Sie auf **Import zu Office 365**.
    
    Die Seite **Filtern die Daten** wird angezeigt. Einblicke in die Daten zu den Daten in die PST-Dateien für den Importauftrag, einschließlich Informationen über das Alter der Daten enthält. 
    
    ![Der Filter der Datenseite zeigt Einblicke in die Daten der PST-Dateien für den Importauftrag](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. Basierend auf unabhängig davon, ob Sie gekürzt werden die Daten, die in Office 365,, klicken Sie unter importiert wird möchten **möchten Sie Ihre Daten filtern?**, eine der folgenden Aktionen aus:
    
    a. Klicken Sie auf **Ja, ich möchte vor dem Importieren von Filtern** , um die Daten zu kürzen, die Sie importieren, und klicken Sie dann auf **Weiter**.
    
    Das **Importieren von Daten in Office 365-Seite** mit Detaildaten Insights aus der Analyse angezeigt wird, das Office 365 ausgeführt. 
    
    ![Office 365 zeigt detaillierte Daten Einblicke in der Analyse der PST-Dateien](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    Das Diagramm auf dieser Seite zeigt die Menge der Daten, die importiert werden. Informationen zu jedem Nachrichtentyp in PST-Dateien gefunden werden im Diagramm angezeigt. Sie können den Cursor über jeder Balken anzuzeigenden spezifische Informationen zu diesem Nachrichtentyp bewegen. Es ist auch ein Dropdown-Listenfeld mit verschiedenen Alter Werte basierend auf der Analyse der PST-Dateien. Wenn Sie ein Alter in der Dropdown-Liste auswählen, wird im Diagramm aktualisiert, um anzuzeigen, wie viele Daten für das ausgewählte Alter importiert werden sollen. 
    
    b. zum Konfigurieren der Addition Filter an, um die Datenmenge zu reduzieren, die importiert wird, klicken Sie auf **Weitere Filteroptionen**.
    
    ![Konfigurieren Sie die Filter auf der Seite für weitere Optionen zu erhöhen, die Daten, die importiert werden](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    Sie können diese Filter konfigurieren:
    
      - **Alter** - wählen Sie ein Alter, sodass nur Elemente vorhanden und neuer ist als der angegebene Alter sind importiert werden sollen. Finden Sie im Abschnitt [Weitere Informationen](filter-data-when-importing-pst-files.md#moreinfo) darüber, wie Office 365 mit der ALTER-Buckets für den Filter **Alter** bestimmt eine Beschreibung ein. 
    
      - **Typ** – in diesem Abschnitt zeigt alle Nachrichtentypen, die in die PST-Dateien für den Importauftrag gefunden wurden. Deaktivieren Sie ein Kontrollkästchen neben einem Nachrichtentyp, die Sie ausschließen möchten. Beachten Sie, dass Sie den anderen Nachrichtentyp ausschließen ist nicht möglich. Finden Sie im Abschnitt [Weitere Informationen](filter-data-when-importing-pst-files.md#moreinfo) erhalten Sie eine Liste der Postfachelemente, die in der anderen Kategorie enthalten sind. 
    
      - **Benutzer** : Sie können Nachrichten, die gesendet oder Empfangen von bestimmten Personen werden ausschließen. Ausschließen von Personen, die in der From stehen: Feld, um: Field- oder Cc: Feld von Nachrichten, klicken Sie neben diesem Empfängertyp auf **Ausschließen von Benutzern** . Geben Sie die e-Mail-Adresse (SMTP-Adresse) der Person ein, klicken Sie auf **Hinzufügen**![New Icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) diese zur Liste der ausgeschlossenen Benutzer für diesen Empfänger hinzufügen, und klicken Sie dann auf **Speichern** , um die Liste der ausgeschlossenen Benutzer speichern. 
    
        > [!NOTE]
        > Office 365 wird Einblicke in die Daten aus dem Festlegen des Filters **Personen** nicht angezeigt. Wenn Sie diesen Filter, Nachrichten von bestimmten Personen gesendet oder empfangen auszuschließen festlegen, werden diese Nachrichten während des tatsächlichen Importvorgangs ausgeschlossen werden. 
  
    c. Klicken Sie auf **Übernehmen** in die Seite zum Speichern Ihrer filtereinstellungen für Ausfliegen **Weitere Filteroptionen** . 
    
    Die Daten, die auf der Seite **Daten importieren auf Office 365** Insights basierend auf Ihrer filtereinstellungen für aktualisiert werden, einschließlich der Gesamtmenge der Daten, die importiert werden auf der Basis Filter. Beachten Sie, dass auch eine Zusammenfassung der filtereinstellungen für angezeigt wird. Sie können **Bearbeiten** neben einen Filter zum Ändern der Einstellung bei Bedarf klicken. 
    
    ![Einblicke in die die Daten werden basierend auf Ihrer filtereinstellungen für aktualisiert.](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    d. Klicken Sie auf **Weiter**.
    
    Anzeigen Ihrer filtereinstellungen für eine Statusseite angezeigt. In diesem Fall können Sie Filter Einstellungen bearbeiten.
    
    e. Klicken Sie auf **Daten importieren** , um den Import starten. Beachten Sie, dass die Gesamtmenge der Daten, die importiert werden angezeigt wird. 
    
    Oder
    
    a. Klicken Sie auf **Nein, ich möchte alles importieren** , um alle Daten in die PST-Dateien in Office 365 zu importieren, und klicken Sie dann auf **Weiter**.
    
    b. Klicken Sie auf der Seite **Importieren von Daten zu Office 365** klicken Sie auf **Daten importieren** , um den Import starten. Beachten Sie, dass die Gesamtmenge der Daten, die importiert werden angezeigt wird. 
    
6. Klicken Sie auf der Seite **Importieren** auf **Refresh** ![aktualisieren](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). Der Status für den Importauftrag wird in der Spalte **Status** angezeigt. 
    
7. Klicken Sie auf dem Import der Auftrag zum Anzeigen von Ausführlichere Informationen, wie der Status für jede PST-Datei und der filtereinstellungen, die Sie konfiguriert haben.

  
## <a name="more-information"></a>Weitere Informationen

- Bestimmt Office 365 wie die Schritten für den Filter ALTER? Office 365 eine PST-Datei analysiert, sucht unter der gesendete oder empfangene Zeitstempel der einzelnen Elemente (wenn ein Element einen Zeitstempel gesendeten und empfangenen wurde, wird das älteste Datum ausgewählt). Klicken Sie dann Office 365 befasst sich mit den Wert des Jahres für diese Zeitstempel und vergleicht ihn mit dem aktuellen Datum das Alter des Elements bestimmt. Diese Jahren werden dann als die Werte in der Dropdown-Liste für den **Age** -Filter verwendet. Wenn eine PST-Datei Nachrichten von 2015, 2016 und 2014 aufweist, Werte in der **Age** -Filter würde beispielsweise **1 Jahr**, **2 Jahre**und **3 Jahren**sein.
    
- Die folgende Tabelle enthält die Nachrichtentypen, die in der **anderen** Kategorie im **Typ** Filter auf der Seite Ausfliegen **Weitere Optionen** enthalten sind (siehe Schritt 5 b in der vorherigen Prozedur). Sie können nicht aktuell, Elemente in der Kategorie "Andere" ausgeschlossen werden beim Importieren von PST-Dateien in Office 365. 
    
    |**ID der Nachrichtenklasse**|**Postfachelemente, die diese Nachrichtenklasse verwenden**|
    |:-----|:-----|
    |IPM. Aktivität  <br/> |Journaleinträge  <br/> |
    |IPM. Dokument  <br/> |Dokumente und Dateien (nicht an eine e-Mail-Nachricht angefügt)  <br/> |
    |IPM. Datei  <br/> |(identisch mit IPM. Dokument)  <br/> |
    |IPM. Note.IMC.Notification  <br/> |Berichte vom Internet Mail eine Verbindung herzustellen, ist das Exchange Server-Gateway zum Internet gesendet  <br/> |
    |IPM. Note.Microsoft.Fax  <br/> |Faxnachrichten  <br/> |
    |IPM. Note.Rules.Oof.Template.Microsoft  <br/> |Abwesenheits automatische Antwortnachrichten  <br/> |
    |IPM. Note.Rules.ReplyTemplate.Microsoft  <br/> |Eine Posteingangsregel gesendeten Antworten  <br/> |
    |IPM. OLE. Klasse  <br/> |Ausnahmen für eine Besprechungsserie  <br/> |
    |IPM. Recall.Report  <br/> |Berichte zum Nachrichtenrückruf  <br/> |
    |IPM. Remote  <br/> |Remote-Mail-Nachrichten  <br/> |
    |IPM. Bericht  <br/> |Element Statusberichte  <br/> |
