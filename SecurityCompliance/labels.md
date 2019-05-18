---
title: Übersicht über Aufbewahrungsbezeichnungen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Aufbewahrungsbezeichnungen in Office 365 können Ihnen dabei helfen, die richtigen Maßnahmen für die entsprechenden Inhalte zu treffen. Mit Aufbewahrungsbezeichnungen können Sie Daten organisationsweit für Governance klassifizieren und Aufbewahrungsregeln basierend auf dieser Klassifizierung durchsetzen. Sie können Aufbewahrungsbezeichnungen auch verwenden, um die Datensatzverwaltung in Office 365 zu implementieren.
ms.openlocfilehash: b6e0263b02c6395d7f8d9ccb68d04b82aa84fe29
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154347"
---
# <a name="overview-of-retention-labels"></a>Übersicht über Aufbewahrungsbezeichnungen

In Ihrer Organisation verwenden Sie wahrscheinlich verschiedene Arten von Inhalten, für die unterschiedliche Aktionen ausgeführt werden müssen, um branchenspezifische Vorschriften und interne Richtlinien einzuhalten. Dies kann zum Beispiel die folgenden Inhalte umfassen:
  
- Steuerformulare, die für einen bestimmten Zeitraum **aufbewahrt** werden müssen. 
    
- Pressematerialien, die nach dem Erreichen eines bestimmten Alters **dauerhaft gelöscht** werden müssen. 
    
- Im Wettbewerb stehende Forschungen, die sowohl **aufbewahrt** als auch anschließend **dauerhaft gelöscht** werden müssen. 
    
- Arbeitsvisa, die **als Datensatz gekennzeichnet** werden müssen, damit sie nicht bearbeitet oder gelöscht werden. 
    
In all diesen Fällen können Aufbewahrungsbezeichnungen in Office 365 Ihnen dabei helfen, die richtigen Maßnahmen für die entsprechenden Inhalte zu treffen. Mit Aufbewahrungsbezeichnungen können Sie Daten organisationsweit für Governance klassifizieren und Aufbewahrungsregeln basierend auf dieser Klassifizierung durchsetzen.
  
Mit Aufbewahrungsbezeichnungen können Sie Folgendes:
  
- **Sie können Personen in Ihrer Organisation ermöglichen, eine Aufbewahrungsbezeichnungen manuell** auf einen Inhalt in Outlook im Web, Outlook 2010 und höher, OneDrive, SharePoint und Office 365-Gruppen anzuwenden. Benutzer wissen häufig am besten, mit welcher Art von Inhalt sie arbeiten. Sie können den Inhalt somit klassifizieren und die entsprechende Richtlinie anwenden lassen. 
    
- **Sie können Aufbewahrungsbezeichnungen automatisch** auf Inhalt anwenden, wenn er bestimmten Bedingungen entspricht: 
    
  - Der Inhalt enthält bestimmte vertrauliche Informationen.
    
  - Der Inhalt enthält bestimmte Stichwörter, die einer von Ihnen erstellten Abfrage entsprechen.
    
    Die Möglichkeit, Aufbewahrungsbezeichnungen automatisch auf Inhalte anzuwenden, ist aus den folgenden Gründen wichtig:
    
  - Sie müssen die Benutzer nicht schulen, damit sie alle Ihre Klassifizierungen kennen.
    
  - Sie müssen sich nicht darauf verlassen, dass die Benutzer alle Inhalte richtig klassifizieren.
    
  - Benutzer müssen nicht mehr über Governance-Richtlinien Bescheid wissen, sondern können sich stattdessen auf ihre Arbeit konzentrieren.

  > [!NOTE]
  > Die Möglichkeit, Bezeichnungen automatisch anzuwenden, erfordert eine Office 365 Enterprise E5-Lizenz für jeden Benutzer, der die Berechtigung zum Bearbeiten von Inhalten hat, die auf einer Website oder in einem Postfach automatisch mit Bezeichnungen versehen wurden. Benutzer, die nur Schreibzugriff haben, benötigen keine Lizenz.
      
- **Wenden Sie eine Standardaufbewahrungsbezeichnung auf eine Dokumentbibliothek** in SharePoint- und Office 365-Gruppenwebsites an, sodass alle Dokumente in dieser Bibliothek mit der Standardaufbewahrungsbezeichnung versehen werden. 
    
- **Implementieren Sie die Datensatzverwaltung im gesamten Office 365**, darunter E-Mails und Dokumente. Sie können eine Aufbewahrungsbezeichnung verwenden, um Inhalt als Datensatz zu klassifizieren. In diesem Fall kann die Bezeichnung nicht geändert oder entfernt werden, und der Inhalt kann nicht bearbeitet oder gelöscht werden. 
    
Sie erstellen und verwalten Aufbewahrungsbezeichnungen auf der Seite **Bezeichungen** > Registerkarte **Aufbewahrung** im Microsoft 365 Compliance Center, Microsoft 365 Security Center oder Office 365 Security &amp; Compliance Center.  
  

## <a name="how-retention-labels-work-with-label-policies"></a>Funktionsweise von Aufbewahrungsbezeichnungen bei Bezeichnungsrichtlinien

Das Bereitstellen von Aufbewahrungsbezeichnungen für Personen in Ihrer Organisation, damit sie Inhalte klassifizieren können, ist ein zweistufiger Vorgang: Zuerst erstellen Sie die Bezeichnungen, und dann veröffentlichen Sie die Bezeichnungen an den von Ihnen ausgewählten Speicherorten. Wenn Sie Aufbewahrungsbezeichnungen veröffentlichen, wird eine Bezeichnungsrichtlinie erstellt.
  
![Diagramm der Rollen und Aufgaben für Bezeichnungen](media/4082bc7d-c04c-4b9a-8a26-7f12565d3311.png)
  
Aufbewahrungsbezeichnungen sind unabhängige, wiederverwendbare Bausteine, die in einer Bezeichnungsrichtlinie enthalten sind und an verschiedenen Orten veröffentlicht werden. Aufbewahrungsbezeichnungen können in vielen Richtlinien wiederverwendet werden. Der Hauptzweck der Bezeichnungsrichtlinie ist es, eine Reihe von Aufbewahrungsbezeichnungen zu gruppieren und die Speicherorte anzugeben, an denen die Bezeichnungen verfügbar sein sollen.
  
![Diagramm der Bezeichnungen, Bezeichnungsrichtlinien und Speicherorte](media/eee42516-adf0-4664-b5ab-76727a9a3511.png)
  
1. Wenn Sie Aufbewahrungsbezeichnungen veröffentlichen, sind sie in einer Bezeichnungsrichtlinie enthalten. Eine einzelne Aufbewahrungsbezeichnung kann in vielen Richtlinien enthalten sein.
    
2. Bezeichnungsrichtlinien geben die Speicherorte zum Veröffentlichen der Aufbewahrungsbezeichnungen an.
    
## <a name="only-one-retention-label-at-a-time"></a>Jeweils nur eine Aufbewahrungsbezeichnung

Es ist wichtig zu wissen, dass ein Inhalt wie eine E-Mail-Nachricht oder ein Dokument jeweils nur über eine Aufbewahrungsbezeichnung verfügen kann:
  
- Aufbewahrungsbezeichnungen, die von den Endbenutzern manuell zugewiesen wurden, können entfernt oder geändert werden.
    
- Wenn eine Bezeichnung einem Inhalt automatisch zugewiesen wurde, kann diese automatisch zugewiesene Aufbewahrungsbezeichnung durch eine vom Endbenutzer manuell zugewiesene Bezeichnung ersetzt werden.
    
- Wenn einem Inhalt eine Aufbewahrungsbezeichnung manuell von einem Endbenutzer zugewiesen wurde, kann diese manuell zugewiesene Aufbewahrungsbezeichnung nicht durch eine automatisch zugewiesene Bezeichnung ersetzt werden.
    
- Wenn es mehrere Regeln gibt, durch die eine Bezeichnung automatisch zugewiesen wird, und ein Inhalt die Bedingungen verschiedener Regeln erfüllt, wird die Aufbewahrungsbezeichnung für die älteste Regel angewendet.
    
Manuelle Bezeichnungen werden explizit zugewiesen, automatische Bezeichnungen hingegen implizit. Eine explizite Aufbewahrungsbezeichnung hat Vorrang vor einer impliziten Bezeichnung. Weitere Informationen finden Sie weiter unten im Abschnitt [Die Grundsätze der Aufbewahrung, oder was hat Vorrang?](#the-principles-of-retention-or-what-takes-precedence).

Alle Informationen in diesem Abschnitt gelten nur für Aufbewahrungsbezeichnungen. Beachten Sie, dass zusätzlich zu einer Aufbewahrungsbezeichnung auf ein Inhaltselement auch eine Vertraulichkeitsbezeichnung angewendet werden kann.
  
## <a name="how-long-it-takes-for-retention-labels-to-take-effect"></a>Wie lange es dauert, bis Aufbewahrungsbezeichnungen wirksam werden

Wenn Sie Aufbewahrungsbezeichnungen veröffentlichen oder automatisch anwenden, werden sie nicht sofort wirksam:
  
1. Zuerst muss die Bezeichnungsrichtlinie aus dem Admin Center mit den Standorten der Richtlinie synchronisiert werden.
    
2. Anschließend benötigt der Speicherort möglicherweise etwas Zeit, um den Endbenutzern die manuellen Bezeichnungen bereitzustellen oder die Bezeichnungen automatisch auf den Inhalt anzuwenden. Wie lange dies dauert, hängt vom Speicherort der Art der Bezeichnung ab.
    
### <a name="manual-retention-labels"></a>Manuelle Aufbewahrungsbezeichnungen

Wenn Sie Aufbewahrungsbezeichnungen auf SharePoint oder OneDrive veröffentlichen, kann es bis zu einem Tag dauern, bevor diese Aufbewahrungsbezeichnungen den Endbenutzern angezeigt werden. Darüber hinaus kann es, wenn Sie Aufbewahrungsbezeichnungen auf Exchange veröffentlichen, bis zu sieben Tage dauern, bevor sie den Endbenutzern zur Verfügung stehen. Außerdem muss das Postfach mindestens 10 MB Daten enthalten.
  
![Diagramm, wann manuelle Bezeichnungen wirksam werden](media/b19f3a10-f625-45bf-9a53-dd14df02ae7c.png)
  
### <a name="auto-apply-retention-labels"></a>Automatisch angewendete Aufbewahrungsbezeichnungen

Wenn Sie Aufbewahrungsbezeichnungen automatisch auf Inhalte anwenden, die bestimmte Bedingungen erfüllen, kann es bis zu sieben Tage dauern, bevor die Aufbewahrungsbezeichnungen auf alle vorhandenen Inhalte angewendet werden, die diesen Kriterien entsprechen. Beachten Sie jedoch, dass Ihre Aufbewahrungsbezeichnungen nach der Bereitstellung schnell auf neue Inhalte angewendet werden, in der Regel innerhalb von 15 Minuten oder weniger.
  
![Diagramm, wann automatisch angewendete Bezeichnungen wirksam werden](media/b8c00657-477a-4ade-b914-e643ef97a10d.png)
  
### <a name="how-to-check-on-the-status-of-exchange-labels"></a>So prüfen Sie den Status von Exchange-Bezeichnungen

In Exchange Online werden Aufbewahrungsbezeichnungen Endbenutzern anhand eines Prozesses bereitgestellt, die alle sieben Tage ausgeführt wird. Mit PowerShell können Sie sehen, wann dieser Prozess zuletzt ausgeführt wurde, und so ermitteln, wann er erneut ausgeführt wird.
  
1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://go.microsoft.com/fwlink/?linkid=799773).
    
2. Führen Sie die folgenden Befehle aus:
    
  ```
  $logProps = Export-MailboxDiagnosticLogs <user> -ExtendedProperties
  ```

  ```
  $xmlprops = [xml]($logProps.MailboxLog)
  ```

  ```
  $xmlprops.Properties.MailboxTable.Property | ? {$_.Name -like "ELC*"}
  ```

In den Ergebnissen zeigt die Eigenschaft `ELCLastSuccessTimeStamp` (UTC) an, wann das System Ihr Postfach das letzte Mal verarbeitet hat. Wenn dies nicht mehr geschehen ist, seit Sie die Richtlinie erstellt haben, werden die Bezeichnungen nicht angezeigt. Um die Verarbeitung zu erzwingen, führen Sie `Start-ManagedFolderAssistant -Identity <user>` aus.
    
Wenn die Bezeichnungen nicht in Outlook im Web angezeigt werden und Sie denken, dass sie angezeigt werden sollten, müssen Sie den Cache des Browsers leeren (STRG + F5).
    
## <a name="label-policies-and-locations"></a>Bezeichnungsrichtlinien und Speicherorte

Verschiedene Arten von Aufbewahrungsbezeichnungen können an verschiedenen Speicherorten veröffentlicht werden, je nach Funktion der Aufbewahrungsbezeichnung.
  
|**Wenn für die Aufbewahrungsbezeichnung Folgendes gilt:**|**So kann die Bezeichnungsrichtlinie angewendet werden auf...**|
|:-----|:-----|
|für Endbenutzer veröffentlicht  <br/> |Gruppen in Exchange, SharePoint, OneDrive, Office 365  <br/> |
|basierend auf Typen vertraulicher Informationen automatisch angewendet  <br/> |Exchange (nur alle Postfächer), SharePoint, OneDrive  <br/> |
|basieren auf einer Abfrage automatisch angewendet  <br/> |Gruppen in Exchange, SharePoint, OneDrive, Office 365  <br/> |
   
Beachten Sie, dass automatisch angewendete Aufbewahrungsbezeichnungen in Exchange (für Abfragen und Arten vertraulicher Informationen) nur auf neu gesendete Nachrichten angewendet werden (Daten bei der Übertragung), und nicht auf alle Elemente, die sich derzeit im Postfach befinden (ruhende Daten). Außerdem werden automatisch angewendete Aufbewahrungsbezeichnungen für Arten von vertraulichen Informationen immer auf alle Postfächer angewendet. Es können keine bestimmten Postfächer ausgewählt werden.
  
Beachten Sie, dass öffentliche Ordner in Exchange und Skype Bezeichnungen nicht unterstützen.
  
## <a name="how-retention-labels-enforce-retention"></a>So erzwingen Aufbewahrungsbezeichnungen die Aufbewahrung

Aufbewahrungsbezeichnungen können genau die gleichen Aufbewahrungsaktionen erzwingen wie eine Aufbewahrungsrichtlinie. Sie können Aufbewahrungsbezeichnungen verwenden, um einen komplexen Inhaltsplan (oder Dateiplan) zu implementieren. Weitere Informationen zur Funktionsweise der Aufbewahrung finden Sie unter [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md).
  
Darüber hinaus hat eine Aufbewahrungsbezeichnung zwei Aufbewahrungsoptionen, die nur für eine Aufbewahrungsbezeichnung und nicht in einer Aufbewahrungsrichtlinie verfügbar sind. Aufbewahrungsbezeichnungen bieten Ihnen die folgenden Möglichkeiten:
  
- Auslösen einer Dispositionsprüfung am Ende des Aufbewahrungszeitraums, damit SharePoint- und OneDrive-Dokumente überprüft werden müssen, bevor sie gelöscht werden können. Weitere Informationen finden Sie unter [Übersicht über Dispositionsprüfungen](disposition-reviews.md).
    
- Beginnen des Aufbewahrungszeitraums zu dem Zeitpunkt, an dem der Inhalt mit der Bezeichnung versehen wurde, und nicht ausgehend vom Alter des Inhalts oder dem Zeitpunkt, zu dem er zuletzt geändert wurde.
    
![Aufbewahrungseinstellungen mit Optionen speziell für Bezeichnungen](media/c49118c9-6279-4661-94db-deffa76e27ac.png)
  
## <a name="where-published-retention-labels-can-appear-to-end-users"></a>Wo veröffentlichte Aufbewahrungsbezeichnungen Endbenutzern verfügbar gemacht werden können

Wenn Endbenutzer Aufbewahrungsbezeichnungen auf Inhalte anwenden, können Sie die Bezeichnungen an den folgenden Speicherorten veröffentlichen:
  
- Outlook im Web
    
- Outlook 2010 und höher
    
- OneDrive
    
- SharePoint
    
- Office 365-Gruppen (sowohl die Gruppenwebsite als auch das Gruppenpostfach in Outlook im Web)
    
Die folgenden Abschnitte zeigen, wie Bezeichnungen den Endbenutzern in Ihrer Organisation in verschiedenen Apps angezeigt werden.
  
### <a name="outlook-on-the-web"></a>Outlook im Web

Um ein Element in Outlook im Web mit einer Bezeichnung zu versehen: Mit der rechten Maustaste auf das Element klicken \> **Richtlinie zuweisen** \> Aufbewahrungsbezeichnung auswählen. 
  
![Menü „Richtlinie zuweisen“ in Outlook im Web](media/146a23cf-e478-4595-b2e8-f707fc4e6ea3.png)
  
Nachdem die Aufbewahrungsbezeichnung zugewiesen wurde, können Sie oben im Element diese Aufbewahrungsbezeichnung anzeigen und sehen, welche Aktion sie durchführt. Wenn eine E-Mail klassifiziert ist, der ein Aufbewahrungszeitraum zugeordnet wurde, sehen Sie auf einen Blick, wann die E-Mail abläuft.
  
![Bezeichnung, die einer E-Mail in Outlook im Web zugewiesen wurde](media/16f6c91b-5eab-4574-9d13-6d12be00a783.png)
  
Sie können Aufbewahrungsbezeichnungen auch auf Ordner anwenden. Hierbei gilt Folgendes:
  
- Allen Elementen im Ordner wird automatisch dieselbe Aufbewahrungsbezeichnung zugewiesen, **mit Ausnahme von** Elementen, denen eine Aufbewahrungsbezeichnung explizit zugewiesen wurde. Explizit bezeichnete Elemente behalten diese Aufbewahrungsbezeichnung. Weitere Informationen finden Sie weiter unter im Abschnitt zu den Grundsätzen der Aufbewahrung. 
    
- Wenn Sie die Standardaufbewahrungsbezeichnung eines Ordners ändern oder entfernen, wird die Aufbewahrungsbezeichnung ebenfalls für alle Elemente in dem Ordner geändert oder entfernt, **mit Ausnahme von** Elementen, die über explizit zugewiesene Aufbewahrungsbezeichnungen verfügen. 
    
- Wenn Sie ein Element mit einer Standardaufbewahrungsbezeichnung von einem Ordner in einen anderen Ordner mit einer anderen Standardaufbewahrungsbezeichnung verschieben, erhält das Element die neue Standardaufbewahrungsbezeichnung.
    
- Wenn Sie ein Element mit einer Standardaufbewahrungsbezeichnung von einem Ordner in einen anderen Ordner ohne Standardaufbewahrungsbezeichnung verschieben, wird die alte Standardaufbewahrungsbezeichnung entfernt.
    
### <a name="outlook-2010-and-later"></a>Outlook 2010 und höher

Um ein Element in Outlook im Web mit einer Bezeichnung zu versehen: Mit der rechten Maustaste auf das Element klicken \> auf dem **Menüband** \> **Richtlinie zuweisen** \> Aufbewahrungsbezeichnung auswählen. 
  
![Schaltfläche „Richtlinie zuweisen“](media/30684dea-dd73-4e4a-9185-8e29f403b6ca.png)
  
Nachdem die Aufbewahrungsbezeichnung zugewiesen wurde, können Sie oben im Element diese Aufbewahrungsbezeichnung anzeigen und sehen, welche Aktion sie durchführt. Wenn eine E-Mail klassifiziert ist, der ein Aufbewahrungszeitraum zugeordnet wurde, sehen Sie auf einen Blick, wann die E-Mail abläuft.
  
Sie können Aufbewahrungsbezeichnungen auch auf Ordner anwenden. Dies funktioniert in Outlook 2010 und höher genauso wie in Outlook im Web – weitere Informationen finden Sie im vorherigen Abschnitt.
  
### <a name="onedrive-and-sharepoint"></a>OneDrive und SharePoint

Um ein Dokument mit einer Bezeichnung zu versehen (einschließlich OneNote-Dateien), wählen Sie in OneDrive oder SharePoint das Element \> in der oberen rechten Ecke aus, wählen Sie **Detailfenster öffnen**![Symbol des Informationsbereichs](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) \> **Bezeichnung anwenden** \> Aufbewahrungsbezeichnung auswählen. 
  
Beachten Sie, dass Sie eine Aufbewahrungsbezeichnung auch auf einen Ordner- oder Dokumentensatz anwenden können. Sie können auch eine Standardaufbewahrungsbezeichnung für eine Dokumentbibliothek festlegen. Weitere Informationen finden Sie in Abschnitt weiter unten.
  
![Bezeichnungsliste auf ein Element in SharePoint anwenden](media/151cc83c-da57-45b0-9cd1-fd2f28a31083.png)
  
Nachdem eine Aufbewahrungsbezeichnung auf ein Element angewendet wurde, wird sie im Detailbereich angezeigt, wenn das Element ausgewählt wird.
  
![Angewendete Bezeichnung im Detailbereich](media/d06e585e-29f7-4c8c-afef-629c97268b8e.png)
  
Sie können auch eine Ansicht der Bibliothek erstellen, die die Spalte **Bezeichnungen** oder die Spalte **Element ist ein Datensatz** enthält. Auf diese Weise können Sie auf einen Blick alle Aufbewahrungsbezeichnungen sehen, die Elementen zugewiesen sind, und Sie können sehen, welche Elemente Datensätze sind. Beachten Sie jedoch, dass Sie die Ansicht nicht anhand der Spalte **Element ist ein Datensatz** filtern können. 
  
![Spalte „Bibliothek“ für Bezeichnungen in benutzerdefinierter Ansicht](media/e3392627-c0a3-405e-bb57-55f27c34cfdd.png)
  
### <a name="office-365-groups"></a>Office 365-Gruppen

Wenn Sie Aufbewahrungsbezeichnungen in einer Office 365-Gruppe veröffentlichen, werden sie sowohl auf der Gruppenwebsite als auch im Gruppenpostfach in Outlook im Web angezeigt. Das Vorgehen zum Zuweisen einer Aufbewahrungsbezeichnung zu Inhalten ist mit dem weiter oben für E-Mails und Dokumente aufgeführten Vorgang identisch.

Um Inhalte für eine Office 365-Gruppe zu speichern, müssen Sie den Speicherort der Office 365-Gruppen verwenden. Obwohl eine Office 365-Gruppe über ein Exchange-Postfach verfügt, schließt eine Aufbewahrungsrichtlinie, die den gesamten Exchange-Speicherort umfasst, keine Inhalte in Office 365-Gruppenpostfächern ein.

Darüber hinaus ist es nicht möglich, den Exchange-Speicherort zu verwenden, um ein bestimmtes Gruppenpostfach ein- oder auszuschließen. Obwohl der Exchange-Speicherort zunächst die Auswahl eines Gruppenpostfachs zulässt, erhalten Sie beim Versuch, die Aufbewahrungsrichtlinie zu speichern, die Fehlermeldung, dass "RemoteGroupMailbox" keine gültige Auswahl für den Exchange-Speicherort ist.
  
## <a name="applying-a-retention-label-automatically-based-on-conditions"></a>Automatisches Zuweisen einer Aufbewahrungsbezeichnung basierend auf Bedingungen

Eines der leistungsstärksten Features von Aufbewahrungsbezeichnungen ist die Möglichkeit, sie automatisch auf Inhalte anzuwenden, die bestimmte Kriterien erfüllen. In diesem Fall müssen Personen in Ihrer Organisation die Aufbewahrungsbezeichnungen nicht selbst anwenden – Office 365 erledigt dies für sie.
  
![Diagramm der Rollen und Aufgaben für automatisch angewendete Bezeichnungen](media/32f2f2fd-18a8-43fd-839d-72ad7a43e069.png)
  
Das automatische Anwenden von Aufbewahrungsbezeichnungen ist aus den folgenden Gründen besonders leistungsstark:
  
- Sie müssen die Benutzer nicht schulen, damit sie alle Ihre Klassifizierungen kennen.
    
- Sie müssen sich nicht darauf verlassen, dass die Benutzer alle Inhalte richtig klassifizieren.
    
- Benutzer müssen nicht mehr über Governance-Richtlinien Bescheid wissen, sondern können sich stattdessen auf ihre Arbeit konzentrieren.
    
Sie können Aufbewahrungsbezeichnungen automatisch auf Inhalte anwenden, wenn diese folgende Bedingungen erfüllen:
  
- Der Inhalt enthält bestimmte vertrauliche Informationen.
    
- Der Inhalt enthält bestimmte Stichwörter, die einer von Ihnen erstellten Abfrage entsprechen.
    
![Seite „Bedingung auswählen“ für automatisch angewendete Bezeichnungen](media/c0b7a3ef-bda0-494c-941d-f1f93753ecdd.png)
  
Beachten Sie, dass für automatisch angewendete Aufbewahrungsbezeichnungen ein Office 365 Enterprise E5-Abonnement erforderlich ist. Es kann bis zu sieben Tage dauern, bevor automatisch angewendete Aufbewahrungsbezeichnungen auf alle Inhalte angewendet werden, die die Bedingungen erfüllen, wie oben beschrieben.
  
### <a name="auto-apply-retention-labels-to-content-with-specific-types-of-sensitive-information"></a>Automatisches Anwenden von Aufbewahrungsbezeichnungen auf Inhalte mit bestimmten Typen von vertraulichen Informationen

Beim Erstellen von automatisch angewendeten Aufbewahrungsbezeichnungen für vertrauliche Informationen wird dieselbe Liste von Richtlinienvorlagen wie beim Erstellen einer Richtlinie zur Verhinderung von Datenverlust (Data Loss Prevention, DLP) angezeigt. Jede Richtlinienvorlage ist so vorkonfiguriert, dass sie nach bestimmten Arten von vertraulichen Informationen sucht. So sucht die hier dargestellte Vorlage zum Beispiel nach US-ITIN, SSN und Passnummern. Weitere Informationen zu DLP finden Sie unter [Überblick über DLP-Richtlinien](data-loss-prevention-policies.md).
  
![Richtlinienvorlagen für Arten von vertraulichen Informationen](media/dafd87d4-c7bb-439a-ac7b-193c018f98a5.png)
  
Nach der Auswahl einer Richtlinienvorlage können Sie alle Arten von vertraulichen Informationen hinzufügen oder entfernen, und Sie können die Instanzenanzahl ändern und die Genauigkeit abgleichen. Im hier gezeigten Beispiel wird eine Aufbewahrungsbezeichnung nur dann automatisch angewendet, wenn Folgendes zutrifft:
  
- Der Inhalt besteht aus 1 bis 9 Instanzen einer der drei folgenden Typen von vertraulichen Informationen. Sie können den **max**-Wert löschen, sodass er sich in **any** ändert.
    
- Der Typ der vertraulichen Informationen, der erkannt wird, hat eine Übereinstimmungsgenauigkeit (oder Vertrauensstufe) von mindestens 75. Viele Typen vertraulicher Informationen werden mit mehreren Mustern definiert, wobei ein Muster mit einer höheren Übereinstimmungsgenauigkeit mehr Nachweise (z. B. Stichwörter, Datumsangaben oder Adressen) erfordert, während ein Muster mit einer niedrigeren Übereinstimmungsgenauigkeit weniger Nachweise erfordert. Einfach ausgedrückt: Je niedriger die **min**-Übereinstimmungsgenauigkeit, desto einfacher ist es für den Inhalt, die Bedingung zu erfüllen. 
    
Weitere Informationen zu diesen Optionen finden Sie unter [Optimieren von Regeln, um die Übereinstimmung zu vereinfachen oder zu erschweren](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).
    
![Optionen zum Identifizieren von Typen vertraulicher Informationen](media/de255881-f596-4c8d-8359-e974e3a0819a.png)
  
### <a name="auto-apply-labels-to-content-with-keywords-or-searchable-properties"></a>Automatisches Anwenden von Bezeichnungen auf Inhalte mit Stichwörtern oder durchsuchbare Eigenschaften

Sie können automatische Bezeichnungen auf Inhalte anwenden, die bestimmte Kriterien erfüllen. Die derzeit verfügbaren Bedingungen unterstützen das Anwenden einer Bezeichnung auf Inhalte, die bestimmte Wörter, Ausdrücke oder durchsuchbare Eigenschaften enthalten. Sie können Ihre Abfrage mithilfe von Suchoperatoren wie UND, ODER und NICHT verfeinern.

Weitere Informationen zur Abfragesyntax finden Sie unter:

- 
  [Syntaxreferenz für die Keyword Query Language (KQL)](https://docs.microsoft.com/de-DE/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

Abfragebasierte Bezeichnungen verwenden den Suchindex zum Identifizieren von Inhalten. Weitere Informationen zu gültigen durchsuchbaren Eigenschaften finden Sie unter:

- [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
- 
  [Übersicht über durchforstete und verwaltete Eigenschaften in SharePoint Server](https://docs.microsoft.com/de-DE/SharePoint/technical-reference/crawled-and-managed-properties-overview)

Beispiele für Abfragen:

- Exchange
    - Betreff: „Vierteljährliche Finanzdaten“
    - recipients:garthf<!--nolink-->@contoso.com
- SharePoint und OneDrive for Business
    - contenttype:contract
    - site:https<!--nolink-->://contoso.sharepoint.com/sites/teams/procurement AND contenttype:contract

![Abfrage-Editor](media/ac5b8e5e-7453-4ec7-905c-160df57298d3.png)

## <a name="applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set"></a>Anwenden einer Standardaufbewahrungsbezeichnung auf alle Inhalte in einer SharePoint-Bibliothek, einem Ordner oder einer Dokumentenmappe

Sie können es Personen nicht nur ermöglichen, eine Aufbewahrungsbezeichnung auf einzelne Dokumente anzuwenden, sondern Sie können eine Standardaufbewahrungsbezeichnung auf eine SharePoint-Bibliothek, einen Ordner oder eine Dokumentenmappe anwenden, sodass alle Dokumente in diesem Speicherort diese Standardaufbewahrungsbezeichnung erhalten.
  
Bei einer Dokumentenbibliothek erfolgt dies auf der Seite **Bibliothekseinstellungen**. Wenn Sie die Standardaufbewahrungsbezeichnung auswählen, können Sie auch auswählen, dass sie auf alle vorhandenen Elemente in der Bibliothek angewendet wird. 
  
Wenn Sie zum Beispiel über ein Tag für Marketingmaterial verfügen und wissen, dass eine bestimmte Dokumentenbibliothek nur diese Art von Inhalt enthält, können Sie das Marketingmaterial-Tag als Standard für alle Dokumente in dieser Bibliothek festlegen.
  
![Option „Bezeichnung anwenden“ auf der Seite mit den Bibliothekeinstellungen](media/0787d651-63dc-43b4-8768-716a5ecc64ec.png)
  
Wenn Sie eine Standardaufbewahrungsbezeichnung auf vorhandene Elemente in der Bibliothek, im Ordner oder in der Dokumentenmappe anwenden:
  
- Allen Elementen in der Bibliothek, im Ordner oder in der Dokumentenmappe wird automatisch dieselbe Aufbewahrungsbezeichnung zugewiesen, **mit Ausnahme von** Elementen, denen eine Aufbewahrungsbezeichnung explizit zugewiesen wurde. Explizit bezeichnete Elemente behalten diese Bezeichnung. Weitere Informationen finden Sie weiter unter im Abschnitt zu den [Grundsätzen der Aufbewahrung, oder was hat Vorrang?](#the-principles-of-retention-or-what-takes-precedence)
    
- Wenn Sie die Standardaufbewahrungsbezeichnung einer Bibliothek, eines Ordners oder einer Dokumentenmappe ändern oder entfernen, wird die Aufbewahrungsbezeichnung ebenfalls für alle Elemente in der Bibliothek, im Ordner oder in der Dokumentenmappe geändert oder entfernt, **mit Ausnahme von** Elementen, die über explizit zugewiesene Aufbewahrungsbezeichnungen verfügen. 
    
- Wenn Sie ein Element mit einer Standardaufbewahrungsbezeichnung aus einer Bibliothek, einem Ordner oder einer Dokumentenmappe in eine andere Bibliothek, einen Ordner oder eine Dokumentenmappe verschieben, behält das Element die vorhandene Standardaufbewahrungsbezeichnung auch dann, wenn der neue Speicherort eine andere Standardaufbewahrungsbezeichnung hat.
    
## <a name="applying-a-retention-label-to-email-by-using-rules"></a>Anwenden einer Aufbewahrungsbezeichnung auf E-Mails mithilfe von Regeln

In Outlook 2010 oder höher können Sie Regeln zum Anwenden einer Aufbewahrungsbezeichnung oder Aufbewahrungsrichtlinie erstellen.
  
Sie können zum Beispiel eine Regel erstellen, die eine bestimmte Aufbewahrungsbezeichnung auf alle Nachrichten anwendet, die an eine oder von einer bestimmten Verteilergruppe gesendet werden.
  
So erstellen Sie eine Regel: Rechtsklick auf ein Element \> **Regeln** \> **Regel erstellen** \> **Erweiterte Optionen** \> **Regel-Assistent** \> **Aufbewahrungsrichtlinie anwenden**.
  
![Regel-Assistent mit Option zum Anwenden von Aufbewahrungsrichtlinien](media/eeb2407c-15b6-4224-99cf-e0a00034d8ea.png)
  
## <a name="classifying-content-without-applying-any-actions"></a>Klassifizieren von Inhalten ohne Anwendung von Aktionen

Wenn Sie eine Aufbewahrungsbezeichnung erstellen, müssen Sie keine Aufbewahrungsaktion oder anderen Aktionen aktivieren, wie unten dargestellt. In diesem Fall können Sie eine Aufbewahrungsbezeichnung einfach als Textbeschriftung verwenden, ohne Aktionen zu erzwingen.
  
Sie können beispielsweise die Aufbewahrungsbezeichnung „Später überprüfen“ ohne Aktionen erstellen und diese Aufbewahrungsbezeichnung dann automatisch auf Inhalte mit vertraulichen Informationen oder auf abgefragte Inhalte anwenden.
  
![Seite „Bezeichnungseinstellungen“ mit deaktivierter Aufbewahrung](media/17ce863b-a823-426e-aaad-83718465f762.png)
  
## <a name="using-retention-labels-for-records-management"></a>Verwenden von Aufbewahrungsbezeichnungen für die Datensatzverwaltung

Im Allgemeinen bedeutet die Datensatzverwaltung Folgendes:
  
- Wichtiger Inhalt wird von Benutzern als Datensatz klassifiziert.
    
- Ein Datensatz kann nicht geändert oder gelöscht werden.
    
- Datensätze werden gelöscht, wenn die festgelegte Lebensdauer endet.
    
Sie können Aufbewahrungsbezeichnungen verwenden, um eine einheitliche Datensatzverwaltungsstrategie in Office 365 zu implementieren, während andere Funktionen für die Verwaltung von Datensätzen, z. B. das Datenarchiv, nur für SharePoint-Inhalte gelten. Darüber hinaus können Sie auch Aufbewahrungsaktionen für Datensätze erzwingen, damit sie am Ende ihres Lebenszyklus automatisch gelöscht werden.
  
Wenn Sie eine Aufbewahrungsbezeichnung erstellen, haben Sie die Möglichkeit, die Aufbewahrungsbezeichnung zum Klassifizieren des Inhalts als Datensatz zu verwenden.
  
![Kontrollkästchen zum Klassifizieren von Inhalt als Datensatz](media/9c300739-d5d0-41d2-88dd-137f1cfc9cb6.png)
  
Wenn ein Element als Datensatz bezeichnet wird, geschehen vier Dinge:
  
- Das Element kann nicht endgültig gelöscht werden.
    
- Das Element kann nicht bearbeitet werden.
    
- Die Bezeichnung kann nicht geändert werden.
    
- Die Bezeichnung kann nicht entfernt werden.
    
### <a name="who-can-classify-content-as-a-record"></a>Wer Inhalt als Datensatz klassifizieren kann

Bei SharePoint-Inhalten kann jeder Benutzer in der Standardgruppe „Mitglieder“ (Berechtigungsstufe „Mitwirken“) eine Datensatzbezeichnung auf Inhalte anwenden. Nur der Administrator der Websitesammlung kann diese Aufbewahrungsbezeichnung entfernen oder ändern, nachdem sie angewendet wurde. Darüber hinaus kann eine Aufbewahrungsbezeichnung, die Inhalt als Datensatz klassifiziert, [automatisch auf Inhalte angewendet werden](#auto-apply-retention-labels).
  
### <a name="records-and-folders"></a>Datensätze und Ordner

Sie können eine Aufbewahrungsbezeichnung auf einen Ordner in Exchange, SharePoint oder OneDrive anwenden. Wenn Sie einen Ordner als Datensatz bezeichnen und Sie ein Element in den Ordner verschieben, wird das Element als Datensatz gekennzeichnet. Wenn Sie das Element aus dem Ordner verschieben, bleibt es weiterhin als Datensatz gekennzeichnet.
  
### <a name="records-cant-be-deleted"></a>Datensätze können nicht gelöscht werden

Wenn Sie versuchen, einen Datensatz in Exchange zu löschen, wird das Element in den Ordner „Wiederherstellbare Elemente“ verschoben, entsprechend der Beschreibung in [Funktionsweise einer Aufbewahrungsrichtlinie mit Inhalten am Speicherort](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Wenn Sie versuchen, einen Datensatz in SharePoint zu löschen, wird eine Fehlermeldung angezeigt, dass das Element nicht gelöscht wurde, und das Element verbleibt in der Bibliothek.
  
![Nachricht, dass das Element nicht aus SharePoint gelöscht wurde](media/d0020726-1593-4a96-b07c-89b275e75c49.png)
  
Wenn Sie versuchen, einen Datensatz in OneDrive zu löschen, wird das Element in das permanentes Dokumentarchiv verschoben, entsprechend der Beschreibung in [Funktionsweise einer Aufbewahrungsrichtlinie mit Inhalten am Speicherort](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
## <a name="using-a-retention-label-as-a-condition-in-a-dlp-policy"></a>Verwenden einer Aufbewahrungsbezeichnung als Bedingung in einer DLP-Richtlinie

Eine Aufbewahrungsbezeichnung kann Aufbewahrungsaktionen für Inhalte erzwingen. Darüber hinaus können Sie eine Aufbewahrungsbezeichnung als Bedingung in einer Richtlinie zur Verhinderung von Datenverlust (Data Loss Prevention, DLP) verwenden. Dies bedeutet, dass die DLP-Richtlinie weitere Aktionen für Inhalte, die eine bestimmte Bezeichnung haben, erzwingen kann, wie zum Beispiel das Einschränken des Zugriffs. 
  
Weitere Informationen finden Sie unter [Verwenden einer Bezeichnung als Bedingung in einer DLP-Richtlinie](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy)
  
## <a name="monitor-retention-labels"></a>Aufbewahrungsbezeichnungen überwachen

Wenn Sie Aufbewahrungsbezeichnungen veröffentlicht oder automatisch angewendet haben, sollten Sie überprüfen, ob sie wie gewünscht auf Inhalte angewendet werden. Zum Überwachen der Aufbewahrungsbezeichnungen können Sie den
  
- **Bezeichnungsaktivitäten-Explorer** verwenden. Mit dem Explorer (siehe unten) können Sie schnell die Aufbewahrungsbezeichnungsaktivität für alle Inhalte in SharePoint und OneDrive for Business während der letzten 30 Tage durchsuchen und sie anzeigen. Weitere Informationen finden Sie unter [Anzeigen der Bezeichnungsaktivität für Dokumente](view-label-activity-for-documents.md).

- Seite **Analyse der Bezeichnungen**. Im Microsoft 365 Compliance Center und Microsoft 365 Security Center können Sie schnell sehen, welche Bezeichnungen am häufigsten verwendet werden und wo sie angewendet werden. Außerdem können Sie alle Inhalte mit einer bestimmten Bezeichnung anzeigen. Weitere Informationen finden Sie unter [Anhzeigen der Bezeichnungsnutzung mit der Analyse der Bezeichnungen](label-analytics.md).
    
- **Berichte zur Data Governance**. Mit diesen Berichten können Sie schnell die Trends bei Aufbewahrungsbezeichnungen und die Aktivitäten für alle Inhalte in Exchange, SharePoint und OneDrive for Business während der letzten 90 Tage anzeigen. Weitere Informationen finden Sie unter [Anzeigen der Berichte zur Data Governance](view-the-data-governance-reports.md).
    
![Bezeichnungsaktivitäten-Explorer](media/671ca0cd-1457-40b4-9917-b663360afd95.png)
  
## <a name="using-content-search-to-find-all-content-with-a-specific-retention-label-applied-to-it"></a>Verwenden der Inhaltssuche zum Suchen des gesamten Inhalts, auf den eine bestimmte Aufbewahrungsbezeichnung angewendet wurde

Nachdem die Aufbewahrungsbezeichnungen den Inhalten entweder von Benutzern oder automatisch zugewiesen wurden, können Sie mit der Inhaltssuche alle Inhalte finden, die mit einer bestimmten Aufbewahrungsbezeichnung klassifiziert sind.
  
Wenn Sie eine Inhaltssuche erstellen, wählen Sie die **Compliancetag**-Bedingung, und geben Sie dann den gesamten Bezeichnungsnamen oder einen Teil davon ein, und verwenden Sie ein Platzhalterzeichen. Weitere Informationen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).
  
![Compliancetag-Bedingung](media/82d6af16-59f8-462f-babb-c894b2917018.png)
  
## <a name="the-principles-of-retention-or-what-takes-precedence"></a>Die Grundsätze der Aufbewahrung, oder was hat Vorrang?

Es ist möglich oder sogar wahrscheinlich, dass auf Inhalte mehrere Aufbewahrungsrichtlinien angewendet werden, die jeweils mit einer anderen Aktion (aufbewahren, löschen oder beides) und einem anderen Aufbewahrungszeitraum verbunden sind. Was hat Vorrang? Ganz allgemein sei gesagt, dass Sie sich sicher sein können, dass Inhalte, die aufgrund einer Richtlinie aufbewahrt werden müssen, nicht von einer anderen Richtlinie dauerhaft gelöscht werden können.
  
![Diagramm der Grundsätze der Aufbewahrung](media/1693d6ec-b340-4805-9da3-89aa41bc6afb.png)
  
Um zu verstehen, wie verschiedene Bezeichnungen mit Aufbewahrungsrichtlinien auf Inhalte angewendet werden, sollten Sie diese Grundsätze der Aufbewahrung beachten:
  
1. **Aufbewahrung hat Vorrang vor Löschung. ** Angenommen, eine Aufbewahrungsrichtlinie gibt vor, dass Exchange-E-Mails nach drei Jahren gelöscht werden sollen, eine andere Aufbewahrungsrichtlinie jedoch besagt, dass Exchange-E-Mails fünf Jahre lang aufbewahrt und dann gelöscht werden müssen. Alle Inhalte, die drei Jahre alt sind, werden gelöscht und aus der Ansicht der Benutzer ausgeblendet, aber immer noch im Ordner "Wiederherstellbare Elemente" aufbewahrt, bis sie fünf Jahre alt sind und endgültig gelöscht werden. 
    
2. **Der längste Aufbewahrungszeitraum hat Vorrang. ** Wenn Inhalte mehreren Aufbewahrungsrichtlinien, nach denen Inhalte aufbewahrt werden, unterliegen, werden sie bis zum Ende des längsten Aufbewahrungszeitraums aufbewahrt. 
    
3. **Explizite Einbindung hat Vorrang vor impliziter Einbindung.** Dies bedeutet: 
    
    1. Wenn eine Aufbewahrungsbezeichnung mit Aufbewahrungseinstellungen von einem Benutzer manuell einem Element zugewiesen wird, z. B. einem Exchange-E-Mail- oder OneDrive-Dokument, hat diese Aufbewahrungsbezeichnung Vorrang sowohl vor einer Richtlinie, die auf Website- oder Postfachebene zugewiesen ist, als auch vor einer Standardaufbewahrungsbezeichnung, die von der Dokumentbibliothek zugewiesen wurde. Wenn z. B. die explizite Aufbewahrungsbezeichnung eine Aufbewahrung über zehn Jahr vorgibt, aber die der Website zugewiesene Richtlinie besagt, dass nur fünf Jahre aufbewahrt werden soll, hat die Aufbewahrungsbezeichnung Vorrang. Beachten Sie, dass automatisch angewendete Aufbewahrungsbezeichnungen als implizit und nicht als explizit angesehen werden, da sie von Office 365 automatisch angewendet werden.
    
    2. Wenn eine Aufbewahrungsrichtlinie einen bestimmten Speicherort wie das Postfach oder OneDrive for Business-Konto eines bestimmten Benutzers umfasst, hat diese Richtlinie Vorrang vor einer anderen Aufbewahrungsrichtlinie, die für alle Postfächer oder OneDrive for Business-Konten von Benutzern gilt, aber nicht das Postfach dieses Benutzers speziell einschließt.
    
4. **Der kürzeste Löschzeitraum hat Vorrang. ** Ebenso gilt, dass wenn Inhalte mehreren Aufbewahrungsrichtlinien zur Löschung (ohne Aufbewahrung) unterliegen, sie am Ende des kürzesten Aufbewahrungszeitraums gelöscht werden. 
    
Beachten Sie: Wenn die Regeln, die von allen Richtlinien oder Kennzeichnungen angewendet werden, auf einer Ebene identisch sind, bewegt sich der Fluss nach unten zur nächsten Ebene, wo entschieden wird, welche Regel Vorrang hat.
  
Schließlich kann keine Aufbewahrungsrichtlinie oder Kennzeichnung einen Inhalt dauerhaft löschen, der für eDiscovery gesperrt ist. Wenn die Sperre aufgehoben wird, kommt der Inhalt wieder für den oben beschriebenen Bereinigungsprozess infrage.
  
## <a name="use-retention-labels-instead-of-these-features"></a>Verwenden von Aufbewahrungsbezeichnungen statt dieser Features

Aufbewahrungsbezeichnungen können ganz einfach der gesamten Organisation und deren Inhalten in Office 365 bereitgestellt werden, einschließlich Exchange, SharePoint, OneDrive und Office 365-Gruppen. Wenn Sie Inhalte klassifizieren oder Datensätze in Office 365 verwalten müssen, empfehlen wir, dass Sie Aufbewahrungsbezeichnungen verwenden.
  
Es gibt mehrere andere Features, die zuvor zum Klassifizieren von Inhalten oder Verwalten von Datensätzen in Office 365 verwendet wurden. Diese sind nachfolgend aufgeführt. Diese Features arbeiten weiterhin Seite an Seite mit Aufbewahrungsbezeichnungen. Beachten Sie, dass es zwar Fälle gibt, in denen sich die Implementierung von Bezeichnungen von früheren Features unterscheidet, die Entwicklung von Aufbewahrungsbezeichnungen jedoch die Zukunft der Datensatzverwaltung in Office 365 bestimmen wird. Daher wird im Hinblick auf Datengovernance auf lange Sicht empfohlen, Aufbewahrungsbezeichnungen anstelle dieser Features zu verwenden.
  
### <a name="exchange-online"></a>Exchange Online

- [Aufbewahrungstags und Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/?linkid=846125), auch bekannt als [Messaging-Datensatzverwaltung](https://go.microsoft.com/fwlink/?linkid=846126) (Nur Löschen) 
    
### <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online und OneDrive for Business

- [Konfiguration von Datensatzverwaltung in situ](https://support.office.com/article/7707a878-780c-4be6-9cb0-9718ecde050a) (Aufbewahrung) 
    
- [Einführung in das Datenarchiv](https://support.office.com/article/bae6ca5a-7b19-40e0-b433-e3613a747c2c) (Aufbewahrung) 
    
- [Informationsverwaltungsrichtlinien](intro-to-info-mgmt-policies.md) (Nur Löschen) 
    
## <a name="permissions"></a>Berechtigungen

Mitglieder Ihres Compliance-Teams, die Aufbewahrungsbezeichnungen erstellen sollen, benötigen Berechtigungen für das Security &amp; Compliance Center. Standardmäßig hat Ihr Mandantenadministrator Zugriff auf diesen Speicherort und kann anderen Personen den Zugriff auf das Security &amp; Compliance Center gewähren, ohne ihnen alle Berechtigungen eines Mandantenadministrators zu geben. Zu diesem Zweck wird empfohlen, dass Sie zur Seite **Berechtigungen** des Security &amp; Compliance Center gehen, die Rollengruppe **Compliance-Administrator** bearbeiten und dieser Rollengruppe Mitglieder hinzufügen. 
  
Weitere Informationen finden Sie unter [Freigeben des Benutzerzugriffs auf das Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md).
  
Diese Berechtigungen sind nur erforderlich, um Aufbewahrungsbezeichnungen und eine Aufbewahrungsrichtlinie zu erstellen und anzuwenden. Für die Durchsetzung von Richtlinien ist kein Zugriff auf Inhalte erforderlich.
  
## <a name="find-the-powershell-cmdlets-for-labels"></a>Suchen der PowerShell-Cmdlets für Bezeichnungen

Um die Bezeichnungs-Cmdlets verwenden zu können, müssen Sie wie folgt vorgehen:
  
1. [Herstellen einer Verbindung mit Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)
    
2. Verwenden Sie die folgenden Office 365 Security & Compliance Center-Cmdlets:

  - [Get-ComplianceTag](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/get-compliancetag)

  - [New-ComplianceTag](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-compliancetag)

  - [Remove-ComplianceTag](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/remove-compliancetag)

  - [Set-ComplianceTag](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/set-compliancetag)

  - [Enable-ComplianceTagStorage](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/enable-compliancetagstorage)

  - [Get-ComplianceTagStorage](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/get-compliancetagstorage)

  - [Get-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/get-retentioncompliancepolicy)

  - [New-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-retentioncompliancepolicy)

  - [Remove-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/remove-retentioncompliancepolicy)

  - [Set-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/set-retentioncompliancepolicy)

  - [Get-RetentionComplianceRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/get-retentioncompliancerule)

  - [New-RetentionComplianceRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-retentioncompliancerule)

  - [Remove-RetentionComplianceRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/remove-retentioncompliancerule)

  - [Set-RetentionComplianceRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/set-retentioncompliancerule)

## <a name="more-information"></a>Weitere Informationen

[Übersicht über Aufbewahrungsrichtlinien](retention-policies.md)
