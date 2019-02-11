---
title: Content-Suche in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 53390468-eec6-45cb-b6cd-7511f9c909e4
description: Verwenden der Suche von Inhalt in die Office 365-Sicherheit &amp; Compliance Center zum Suchen nach Inhalt in Postfächern, SharePoint Online-Websites, OneDrive-Konten, Microsoft-Teams, Gruppen von Office 365 und Skype für Business Unterhaltungen. Sie können Schlüsselwort von Suchabfragen verwenden, und suchen Bedingungen, um die Suchergebnisse einzuschränken. Anschließend können Sie eine Vorschau anzeigen und Exportieren von Suchergebnissen. Inhaltssuche ist auch ein effektives Tool zum Suchen nach Inhalt, die eine Anforderung zum GDPR Daten Betreff zugeordnet werden kann.
ms.openlocfilehash: befd2060e65cea73d3c8432b77727e27dd91b82a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686116"
---
# <a name="content-search-in-office-365"></a>Content-Suche in Office 365

Sie können das Inhaltssuche eDiscovery-Tool verwenden, in die Office 365-Sicherheit &amp; Compliance Center für Compliance-Elemente wie e-Mails, Dokumente und Sofortnachrichtenunterhaltungen führen in Office 365-Organisation zu suchen. Verwenden Sie dieses Tool, um die Suche nach Elementen in diese Office 365-Dienste:
  
- Öffentliche Ordner und Exchange Online-Postfächern
    
- SharePoint Online-Websites und OneDrive for Business-Konten
    
- Skype für Business Unterhaltungen
    
- Microsoft Teams 
    
- Office 365-Gruppen
    
Nachdem Sie eine Suche Inhalte, die Anzahl der Speicherorte für Inhalte ausführen und eine geschätzte Anzahl der Suchergebnisse im Search Profil angezeigt werden. Sie können auch schnell Statistiken, wie die Speicherorte für Inhalte anzeigen, die die meisten Elemente verfügen, die die Suchabfrage entsprechen. Nachdem Sie eine Suche ausführen können Sie eine Vorschau der Ergebnisse oder in einem lokalen Computer zu exportieren.


## <a name="create-a-new-search"></a>Erstellen Sie eine neue Suche

Um den Zugriff auf die Seite **Inhaltssuche** zum Ausführen von Suchanfragen und Vorschau und Exportieren von Suchergebnissen haben, ein Administrator, Compliance-beauftragte oder eDiscovery-Manager muss ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier &amp; Compliance Center. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihren Office 365-e-Mail-Adresse und Ihr Kennwort. 
    
3. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
4. Auf **der Seite,** klicken Sie auf den Pfeil neben ![Symbol hinzufügen](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **neue Suche**. 
    
    ![Der neue Suche Dropdown-Liste](media/76b25861-55c5-4f50-9d48-9e2be2d0d078.png)
  
    Sie können eine der folgenden Optionen auswählen:
    
  - **Guided Suche** – diese Option wird ein Assistent, der hilft Ihnen beim Erstellen der Suche gestartet. Die Benutzeroberfläche auswählen Speicherorte für Inhalte und erstellen die Suchabfrage sind die gleichen wie die Option **neue Suche** . 
    
  - **Neue Suche** – diese Option zeigt eine aktualisierte Benutzeroberfläche, um eine neue Suche zu erstellen. Dies ist die Standardoption, wenn Sie auf **neu zu suchen**.
    
  - **Suchen nach ID-Liste** – diese Option können Sie die Suche nach bestimmten e-Mail-Nachrichten und andere Postfachelemente mithilfe einer Liste der Exchange-IDs. Um eine ID-Liste-Suche (formell als eine gezielte Suche bezeichnet) zu erstellen, senden Sie eine durch Trennzeichen getrennten Werten (CSV)-Datei, die bestimmte Postfachelemente zu suchenden identifiziert. Anweisungen finden Sie unter [Vorbereiten einer CSV-Datei für ein Inhaltssuche in Office 365-ID-Liste](csv-file-for-an-id-list-content-search.md).
    
    Der Rest der Schritte in diesem Verfahren wird den neue Suche Standardworkflow folgen.
    
5. Klicken Sie auf **neue Suche** in der Dropdown-Liste. 
    
6. Geben Sie unter **Search-Abfrage**die folgenden Schritte aus.
    
    ![Geben Sie Schlüsselwörter, Bedingungen und Speicherorte zum Durchsuchen](media/1e6de9dd-eac9-4e2a-819d-9740cf6c9106.png)
  
- **Schlüsselwörter für die Suche** - Typ eine Suche im Feld **Stichwörter** Abfragen. Sie können angeben, Schlüsselwörter, Nachricht Eigenschaften wie gesendet und empfangen, Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, das ein Dokument zuletzt geändert wurde. Sie können eine komplexere Abfragen verwenden, die einen booleschen Operators, wie **AND**, **OR**, **nicht**und **NEAR**verwenden. Sie können auch suchen für vertrauliche Informationen (wie Sozialversicherungsnummern) in Dokumenten, oder suchen Sie nach Dokumenten, die extern freigegeben haben. Wenn Sie das Schlüsselwort Feld leer lassen, werden alle Inhalte, die in der angegebenen Speicherorte für Inhalte befindet sich in den Suchergebnissen enthalten sein.
    
    Alternativ können Sie das Kontrollkästchen **Schlüsselwortliste anzeigen** und den Typ ein Schlüsselworts in jede Zeile klicken. Wenn Sie dies tun, sind die Schlüsselwörter für jede Zeile ein logischer Operator ( **C:s**) vorhanden, die Funktionalität der **OR** -Operator in der Suchabfrage ähnlich ist, die erstellt wird. 
    
    Gründe für die Verwendung der Schlüsselwortliste Sie können Statistiken abrufen, die zeigen, wie viele Elemente jedes Schlüsselwort überein. Dadurch können Sie schnell erkennen, welche Schlüsselwörter der am häufigsten (und mindestens) wirksam werden. Sie können auch eine Stichwortbegriff (in Klammern eingeschlossen sind) in einer Zeile. Weitere Informationen zu Suchstatistik finden Sie unter [schlüsselwortstatistiken für die Inhaltssuche Ergebnisse anzeigen](view-keyword-statistics-for-content-search.md).

    [!NOTE] Zur Verringerung der Probleme aufgrund von großen Listen Sie nun auf ein Maximum von 20 Zeilen in der Schlüsselwortliste begrenzt.
    
- **Conditions** - können Sie Suchkriterien, um eine Suche einzugrenzen und eine genauere Ergebnisse zurückgeben hinzufügen. Jede Bedingung hinzugefügt Search-Abfrage, die erstellt und ausgeführt werden, wenn Sie die Suche starten eine-Klausel. Eine Bedingung ist logisch mit der Stichwortabfrage (im Schlüsselwort angegeben) durch einen logischen Operator ( **c: c**) verbunden, die an den **und** -Operator vergleichbar ist. Dies bedeutet, dass Elemente erfüllen der Stichwortabfrage und einen oder mehrere Bedingungen, die in den Ergebnissen berücksichtigt werden müssen. Dies ist die Bedingungen wie helfen, um Ihre Suchergebnisse einzuschränken. Eine Liste und eine Beschreibung der Bedingungen, die Sie bei einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchen Conditions" in [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md#search-conditions).
    
- **Speicherorte** - wählen Sie die Speicherorte für Inhalte zu suchen.
    
  - **Alle Speicherorte** - mit dieser Option werden alle Speicherorte für Inhalte in Ihrer Organisation zu suchen. Dazu gehören e-Mail in alle Exchange-Postfächer (einschließlich aller inaktiver Postfächer, Postfächer für alle Office 365-Gruppen, Postfächer für alle Microsoft-Teams), alle Skype für Business Unterhaltungen, alle SharePoint und OneDrive for Business-Websites (einschließlich der Websites für alle Office 365-Gruppen und Microsoft-Teams) und Elemente in alle öffentlichen Exchange-Ordner.
    
  - **Bestimmte Orte** - mit dieser Option werden bestimmte Speicherorte für Inhalte zu suchen. Sie können alle Speicherorte für Inhalte für einen bestimmten Office 365-Dienst suchen (z. B. Suche alle Exchange-Postfächer oder suchen Sie alle SharePoint-Websites), oder Sie können bestimmte Orte suchen, in der Office 365-Dienste, die angezeigt werden. 
    
    ![Benutzeroberfläche zum Suchen Speicherorte für Inhalte auswählen](media/9a09708b-f8a2-4382-8c4e-2c610ec33c72.png)
  
    Beachten Sie, dass Sie der Liste der Exchange-Postfächer suchen auch Verteilergruppen hinzufügen können. Für Verteilergruppen werden die Postfächer von Gruppenmitgliedern durchsucht. Beachten Sie, dass die dynamische Verteilergruppen nicht unterstützt werden.
    
    **Wichtig:** Wenn Sie alle Speicherorte Postfach oder nur für bestimmte Postfächer suchen, werden Daten aus MyAnalytics und anderen Office 365-Clientanwendungen, die auf die Benutzerpostfächer gespeichert hat eingeschlossen, wenn Sie die Ergebnisse einer Inhaltssuche exportieren. Diese Daten werden nicht in der geschätzten Suchergebnisse enthalten sein, und er nicht für die Vorschau werden. Es wird nur eingeschlossen werden, wenn Sie exportieren, und Laden Sie die Suchergebnisse; finden Sie unter [Exportieren von Daten aus MyAnalytics und anderen Office 365-Clientanwendungen](#exporting-data-from-myanalytics-and-other-office-365-applications) im Abschnitt "Weitere Informationen zur Inhaltssuche". 
    
7. Nachdem Sie die Suchabfrage eingerichtet haben, klicken Sie auf **Speichern &amp; ausführen**.
    
8. Geben Sie auf der Seite **Suche speichern** einen Namen für die Suche und eine optionale Beschreibung, die hilft bei die Suche zu identifizieren. Beachten Sie, dass der Name der Suche in Ihrer Organisation eindeutig sein muss. 
    
9. Klicken Sie auf **Speichern** , um die Suche zu starten. 
    
    Nachdem Sie speichern und die Suche ausführen, werden alle von der Suche zurückgegebenen Ergebnisse im Ergebnisbereich angezeigt. Je nachdem, wie Sie die Preview-Einstellung konfiguriert haben die Suchergebnisse angezeigt werden, oder Sie haben auf **Vorschau Ergebnisse** zum Anzeigen klicken. Finden Sie im nächsten Abschnitt Details. 
    
Greifen Sie erneut auf diese Inhaltssuche oder Zugriff auf andere Content-Suche auf der Seite **Durchsuchen von Inhalten** aufgeführt, wählen die Suche, und klicken Sie dann auf **Öffnen**. 
  
Um die Ergebnisse löschen, oder erstellen eine neue Suche, klicken Sie auf ![Symbol hinzufügen](media/O365-MDM-CreatePolicy-AddIcon.gif) **neue Suche**. 

  
## <a name="preview-search-results"></a>Suchergebnisse in der Vorschau anzeigen

Es gibt zwei Konfigurationseinstellungen für die Vorschau der Suchergebnisse. Nachdem Sie einen neuen eine neue Suche ausführen oder eine vorhandene Suche öffnen, klicken Sie auf ** einzelne Ergebnisse ** um die folgenden Einstellungen Vorschau anzuzeigen: 
  
![Vorschau Ergebnisse für die Suche](media/83519477-1c85-4442-8886-481f186fd758.png)
  
1. **Ergebnisse automatisch eine Vorschau anzeigen** : Diese Einstellung zeigt die Suchergebnisse nach dem Sie einen durchführen eine Suche.
    
2. **Ergebnisse manuell eine Vorschau anzeigen** : Diese Einstellung Platzhalter im Suchergebnisbereich angezeigt und zeigt die Schaltfläche **Vorschau Ergebnisse** , die Sie klicken, um die Suchergebnisse anzuzeigen. Dies ist die Standardeinstellung. auf diese Weise suchleistung verbessern, indem Sie die Suchergebnisse nicht automatisch angezeigt, wenn Sie eine vorhandene Suche öffnen. 
    
Es gibt Grenzwerte, die im Zusammenhang mit der Anzahl der Elemente für die Seitenansicht verfügbar sind. Weitere Informationen finden Sie unter [Grenzwerte für die Suche in der Office 365-Sicherheit &amp; Compliance Center](limits-for-content-search.md). 
  
Eine Liste der unterstützten Dateitypen aufgeführt, die eine Vorschau angezeigt werden kann, finden Sie unter [Anzeigen einer Vorschau der Suchergebnisse](#previewing-search-results) im Abschnitt "Weitere Informationen zur Inhaltssuche". Wenn Sie ein Dateityp für die Vorschau oder Herunterladen eine Kopie eines Dokuments nicht unterstützt wird, können Sie die **ursprüngliche Datei herunterladen** , um sie auf dem lokalen Computer herunterladen klicken. Für .aspx Webseiten ist die URL für die Seite enthalten, obwohl Sie keinen Zugriff auf die Seite Berechtigungen können. 
  
Beachten Sie außerdem, dass nicht indizierter Elemente nicht für die Vorschau von verfügbar sind.
  
## <a name="view-information-and-statistics-about-a-search"></a>Anzeigen von Informationen und Statistiken zu einer Suche

Nachdem Sie erstellen und einer Inhaltssuche ausführen, können Sie Statistiken zu der geschätzten Suchergebnisse anzeigen. Dies umfasst eine Zusammenfassung der Suchergebnisse, die Abfragestatistiken wie die Anzahl der Speicherorte für Inhalte mit Elementen, die die Suchabfrage erfüllen und den Namen der Speicherorte für Inhalte, die die meisten übereinstimmenden Elemente aufweisen. Sie können Statistiken für einen oder mehrere Content-Suche anzeigen. Auf diese Weise können Sie schnell vergleichen Sie die Ergebnisse für mehrere Suchen und bestimmen, welche Informationen die Effektivität von Suchabfragen.
  
Sie können auch die Suchstatistik und schlüsselwortstatistiken in eine CSV-Datei herunterladen. Auf diese Weise können Sie die Filter- und Funktionen in Excel verwenden, um Ergebnisse zu vergleichen, und bereiten Berichte für die Suchergebnisse.
  
So zeigen Sie Suchstatistik an:
  
1. Auf der Seite **Inhaltssuche** in das Wertpapier &amp; Compliance Center, klicken Sie auf **Öffnen** , und klicken Sie dann auf die Suche, die Sie für die zu berechnende anzeigen möchten. 
    
2. Klicken Sie auf der Seite Ausfliegen auf **Abfrage öffnen**. 
    
3. Klicken Sie in der Dropdownliste **einzelne Ergebnisse** auf **Suche Profil**.
    
4. Klicken Sie in der Dropdownliste **Typ** auf eine der folgenden Optionen je nach den Suchstatistik, den, die Sie anzeigen möchten. 
    
  - **Zusammenfassung** : Zeigt Statistiken für jede Art von Speicherorte für Inhalte durchsucht. Dies die Anzahl der Speicherorte für Inhalte, die Elemente enthalten, die die Suchabfrage übereinstimmenden Inhalt und die gesamte Anzahl und Größe der Ergebniselemente durchsuchen. Dies ist die Standardeinstellung.
    
  - **Abfragen** - Statistiken zur Suchabfrage angezeigt. Dies umfasst den Typ der Inhaltsspeicherort gelten auch für die Abfrage Statistiken, die Teil der Suchabfrage die Statistiken gelten (mit dem Hinweis, dass der **primäre** gibt an, die gesamte Suchabfrage), Elemente, die Anzahl der Speicherorte für Inhalte, die enthalten Übereinstimmung mit der Suchabfrage und der Gesamtzahl und Größe und Elemente, (in der angegebenen Inhaltsspeicherort) gefunden wurden, die die Suchabfrage erfüllen. Beachten Sie, dass auch Statistiken für nicht indizierte Elemente (auch als teilweise indizierte Elemente bezeichnet) angezeigt werden. Jedoch sind nur teilweise indizierte Elemente von Postfächern in die Statistiken enthalten. Teilweise indizierte Elemente aus SharePoint und OneDrive sind nicht in der Statistik enthalten.
    
  - **Obere Speicherorte** - Zeigt Statistiken zur Anzahl der Elemente, die die Suchabfrage in jedem Inhaltsspeicherort entsprechen, die durchsucht wurde. Die Speicherorte der oberen 1.000 werden angezeigt.
    
Ausführlichere Informationen zum Suchstatistik finden Sie unter [schlüsselwortstatistiken für die Inhaltssuche Ergebnisse anzeigen](view-keyword-statistics-for-content-search.md).
  
  
## <a name="export-search-results"></a>Exportieren der Suchergebnisse

Nachdem eine Suche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse auf einen lokalen Computer exportieren. Wenn Sie e-Mail-Ergebnisse exportieren, können sie auf Ihrem Computer als PST-Dateien oder als einzelne Nachrichten (MSG-Dateien) heruntergeladen werden. Wenn Sie Inhalte aus SharePoint und OneDrive Websites exportieren, werden Kopien der systemeigenen Office-Dokumenten exportiert. Es gibt auch zusätzliche Dokumente und Berichte, die mit der exportierten Suchergebnisse enthalten sind. Sie können auch nur den Bericht der Suchergebnisse und nicht die tatsächlichen Elemente exportieren.
  
So exportieren Sie Suchergebnisse:
  
1. Auf der Seite **Inhaltssuche** in das Wertpapier &amp; Compliance Center, klicken Sie auf **Öffnen** , und klicken Sie dann auf die Suche, die Sie für die Suchergebnisse exportieren möchten. 
    
2. Klicken Sie auf der Seite Ausfliegen auf ![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Weitere**, und klicken Sie dann auf **Ergebnisse exportieren**. Beachten Sie, dass Sie auch einen Bericht der Suchergebnisse exportieren können.
    
3. Füllen Sie die Abschnitte auf der Fly-Out-Navigation der **Exportergebnisse** aus. Stellen Sie sicher, dass Sie Bildlaufleiste verwenden, um alle Exportoptionen anzuzeigen. 
    
Detailliertere Anweisungen und Tipps zur Problembehandlung finden Sie unter:
  
- [Exportieren von Suchergebnissen aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md)
    
- [Exportieren eines Inhaltssuchberichts](export-a-content-search-report.md)
    

  
## <a name="more-information-about-content-search"></a>Weitere Informationen zu Inhaltssuche

Finden Sie weitere Informationen zum Content-Suche in den folgenden Abschnitten.
  
[Grenzwerte für die Inhaltssuche](#content-search-limits)
  
[Erstellen einer Suchabfrage](#building-a-search-query)
  
[Suchen von OneDrive-Konten](#searching-onedrive-accounts)
  
[Microsoft-Teams und Office 365 Gruppen suchen](#searching-microsoft-teams-and-office-365-groups)
  
[Suchen inaktive Postfächer](#searching-inactive-mailboxes)
  
[Vorschau der Suchergebnisse](#previewing-search-results)
  
[Teilweise indizierte Elemente](#partially-indexed-items)
  
[Exportieren von Daten aus MyAnalytics und anderen Office 365-Clientanwendungen](#exporting-data-from-myanalytics-and-other-office-365-applications)
  
### <a name="content-search-limits"></a>Grenzwerte für die Inhaltssuche

- Eine Beschreibung der die Grenzwerte, die zu dem Feature für die Inhaltssuche angewendet werden, finden Sie unter [Grenzwerte für die Suche in der Office 365-Sicherheit &amp; Compliance Center](limits-for-content-search.md).
    
- Microsoft sammelt Leistungsinformationen für Content-Suche ausführen, indem Sie alle Office 365-Organisationen. Während die Komplexität der Suchabfrage Suche Zeiten beeinflussen kann, durchsucht der größte Faktor, der bestimmt, wie lange Suchvorgänge nehmen die Anzahl von Postfächern. Zwar Microsoft ein Service Level Agreement für Suche Zeiten keine, wie oft die durchschnittliche Suche für ein Inhaltssuche basierend auf der Anzahl der Postfächer, die die Suche von der folgenden Tabelle aufgeführt.
    
|**Anzahl der Postfächer**|**Durchschnittliche Suche Zeit**|
|:-----|:-----|
|100  <br/> |30 Sekunden  <br/> |
|1,000  <br/> |45 Sekunden  <br/> |
|10,000  <br/> |4 Minuten  <br/> |
|25.000  <br/> |10 Minuten  <br/> |
|50.000  <br/> |20 Minuten  <br/> |
|100,000  <br/> |25 Minuten  <br/> |
  
### <a name="building-a-search-query"></a>Erstellen einer Suchabfrage

Ausführliche Informationen zum Erstellen einer Suchabfrage, mithilfe von boolesche Suchoperatoren und Suchkriterien und Typen vertraulicher Informationen und Inhalte für Benutzer außerhalb Ihrer Organisation freigegeben werden gesucht finden Sie unter [Stichwortabfragen und suchen Bedingungen für die Inhaltssuche ](keyword-queries-and-search-conditions.md).
  
Halten die folgenden Punkte berücksichtigen, wenn die diese Schlüsselwortliste verwenden, um eine Suchabfrage zu erstellen.
  
- Sie haben, aktivieren Sie das Kontrollkästchen **Schlüsselwortliste anzeigen** , und geben Sie dann jedes Schlüsselwort in einer separaten Zeile um eine Suchabfrage zu erstellen, in dem die Keywords (oder Schlüsselwort Ausdrücke) in jeder Zeile über der **OR** -Operator verbunden. Wenn Sie nur eine Liste von Schlüsselwörtern in das Feld Stichwort einfügen oder drücken Sie **die EINGABETASTE** nach Eingabe eines Stichworts, werden nicht sie durch den **oder** -Operator verbunden werden. Hier sind falsch und richtig Beispiel für eine Liste der Schlüsselwörter hinzufügen. 
    
    **Falsche**
    
    ![Die falsche Möglichkeit, um ein Schlüsselwort Listenformat (von der Liste in das Feld Schlüsselwort einfügen)](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Richtig**
    
    ![Die ordnungsgemäße ein Schlüsselwort Listenformat (durch auswählen das Kontrollkästchen und klicken Sie dann auf einfügen Liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
- Sie können auch eine Liste der Schlüsselwörter oder Ausdrücke in einer Excel-Datei oder eine Klartextdatei Schlüsselwort vorbereiten und klicken Sie dann kopieren und fügen Sie Ihrer Liste in der Liste Schlüsselwort. Zu diesem Zweck müssen Sie das Kontrollkästchen **Schlüsselwortliste anzeigen** . Klicken Sie auf der ersten Zeile in der Schlüsselwortliste, und fügen Sie Ihrer Liste. Jede Zeile aus der Datei Excel- oder Text wird in Zeile in der Schlüsselwortliste trennen eingefügt werden soll. 
    
- Nach der Erstellung einer Abfrage mithilfe der Schlüsselwortliste ist es ratsam, überprüfen, ob die Abfrage Suchsyntax, stellen Sie die Suchabfrage ist wie gewünscht. Die Schlüsselwörter werden in der Suchabfrage, die im Detailbereich unter **Abfrage** angezeigt wird, durch den Text **(C:s)** getrennt. darauf hin, dass die Schlüsselwörter durch einen logischen Operator ähnliche Funktionalität wie der **OR** -Operator verbunden sind. In ähnlicher Weise enthält die Suchabfrage Bedingungen, die Schlüsselwörter und die Bedingungen sind getrennt durch den Text **(c: c)**. Dies weist darauf hin, dass die Bedingungen mit einem logischen Operator ähnliche Funktionalität **und** die Schlüsselwörter verbunden sind Operator. Hier ist ein Beispiel für die Suchabfrage (im Bereich Details angezeigt), die bei der Verwendung der Schlüsselwortliste und eine Bedingung ergibt. 
    
    ![Beispiel für die Abfrage, die bei der Verwendung der Schlüsselwortliste und eine Bedingung erstellt wird](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
- Beim Ausführen einer Inhaltssuche überprüft Office 365 automatisch die Suchabfrage für nicht unterstützte Zeichen und boolesche Operatoren, die möglicherweise nicht groß geschrieben werden. Nicht unterstützte Zeichen werden häufig ausgeblendet und in der Regel verursacht einen Fehler beim Suchen oder unbeabsichtigte Ergebnisse zurückzugeben. Weitere Informationen zu nicht unterstützten Zeichen, die überprüft werden, finden Sie unter [Content Suchabfrage Fehler überprüfen](check-your-content-search-query-for-errors.md).
    
- Wenn Sie eine Suchabfrage verfügen, Schlüsselwörter für nicht englische Zeichen (beispielsweise chinesischen Schriftzeichen) enthält, klicken Sie auf **Abfrage Sprache-Land/Region**![Sprache nationale/regionale das Symbol Abfrage in Inhaltssuche](media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) und wählen Sie eine Sprach-/Landes-Kultur Codewert für die Suche. Beachten Sie, dass die standardmäßige Sprache/Region neutral ist. Wie können Sie feststellen, wenn Sie die Einstellung für die Sprache für ein Inhaltssuche ändern müssen? Wenn Sie auf bestimmte Speicherorte für Inhalte enthalten, die nicht englische Zeichen an, denen Sie suchen, aber die Suche gibt keine Ergebnisse zurück sind, kann die Language-Einstellung die Ursache sein. 
  
### <a name="searching-onedrive-accounts"></a>Suchen von OneDrive-Konten

- Um eine Liste der URLs für die OneDrive-Websites in Ihrer Organisation zu sammeln, finden Sie unter [Erstellen einer Liste der OneDrive Positionen in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Dieses Skript in diesem Artikel erstellt eine Textdatei, die eine Liste aller OneDrive-Websites enthält. Wenn Sie dieses Skript ausführen, müssen Sie zum Installieren und Verwenden von SharePoint Online-Verwaltungsshell. Achten Sie darauf, dass Sie die URL für die MySite Domäne Ihrer Organisation an jedem Standort OneDrive angefügt werden soll, die Sie suchen möchten. Dies ist die Domäne, die alle Ihre OneDrive enthält. beispielsweise `https://contoso-my.sharepoint.com`. Es folgt ein Beispiel für die URL der Website eines Benutzers OneDrive: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
    
    In seltenen Fällen einer Person für Benutzerprinzipalnamen (UPN) geändert wird wird auch die URL für ihre OneDrive-Speicherort, um den neuen UPN integrieren geändert werden. In diesem Fall müssen Sie eine Inhaltssuche ändern, indem Sie neue OneDrive-URL des Benutzers hinzufügen und Entfernen von der alte Datenbankserver.
  
### <a name="searching-microsoft-teams-and-office-365-groups"></a>Microsoft-Teams und Office 365 Gruppen suchen

Sie können das Postfach suchen, das ein Office 365-Gruppe oder ein Microsoft-Team zugeordnet ist. Da Microsoft-Teams, auf Office 365-Gruppen erstellt werden, ist das Suchen sie sehr ähnlich. In beiden Fällen ist nur das Gruppe oder ein Team Postfach gesucht. die Postfächer der Gruppe oder ein Team Elemente werden nicht durchsucht. Wenn sie suchen möchten, müssen Sie speziell für die Suche hinzufügen.
  
Behalten Sie die folgenden Punkte berücksichtigen, bei der Suche nach Inhalten in Office 365-Gruppen und Microsoft-Teams.
  
- Zum Suchen nach Inhalt befindet sich im Microsoft-Teams und Office 365 Gruppen müssen Sie angeben, das Postfach und die SharePoint-Website, die ein Team oder eine Gruppe zugeordnet sind.
    
- Führen Sie das Cmdlet **Get-UnifiedGroup** in Exchange Online zum Anzeigen von Eigenschaften für ein Microsoft-Team oder eine Office 365-Gruppe. Dies ist eine empfehlenswerte Methode zum Abrufen der URL für die Website, die ein Team oder eine Gruppe zugeordnet ist. Beispielsweise wird mit der folgende Befehl ausgewählte Eigenschaften für ein Office 365-Gruppe mit dem Namen Senior führende Team angezeigt: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Um das Cmdlet **Get-UnifiedGroup** ausführen, müssen Sie die Rolle des Kontaktobjekts Empfänger in Exchange Online zugewiesen werden, oder ein Mitglied einer Rollengruppe sein hat, die die Rolle des Kontaktobjekts Empfänger zugewiesen. 
  
- Wenn dem Postfach eines Benutzers durchsucht wird, werden keine Microsoft-Teams oder Office 365-Gruppe, die der Benutzer Mitglied ist gesucht werden soll. Auf ähnliche Weise, wenn Sie ein Microsoft-Team oder eine Office 365-Gruppe, nur auf die Gruppenpostfach und Gruppe Website, die Sie angeben suchen werden durchsucht; Postfächer und OneDrive for Business-Konten Gruppenmitglieder werden nicht durchsucht, wenn Sie explizit auf die Suche hinzufügen.
    
- Wenn Sie eine Liste der Elemente von einem Microsoft-Team oder eine Office 365-Gruppe erhalten möchten, können Sie die Eigenschaften anzeigen, auf die **Home \> Gruppen** Seite im Office 365 Administrationscenter. Alternativ können Sie in Exchange Online PowerShell den folgenden Befehl ausführen: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Um das Cmdlet **Get-UnifiedGroupLinks** ausführen, müssen Sie die Rolle des Kontaktobjekts Empfänger in Exchange Online zugewiesen werden, oder ein Mitglied einer Rollengruppe sein hat, die die Rolle des Kontaktobjekts Empfänger zugewiesen. 
  
- Unterhaltungen, die Teil eines Microsoft-Teams Kanals sind werden im Postfach gespeichert, die mit dem Microsoft-Team zugeordnet ist. In ähnlicher Weise werden Dateien, die in einem Kanal Teammitglieder freigeben auf das Team SharePoint-Website gespeichert. Daher müssen Sie das Microsoft-Teams Postfach und die SharePoint-Website als einen Inhaltsspeicherort, Gespräche und Dateien in einem Kanal durchsuchen hinzuzufügen.
    
- Alternativ werden Unterhaltungen, die Teil der Liste der Chat in Microsoft-Teams, sind in der Exchange Online-Postfach der Benutzer gespeichert, die im Chat teilnehmen. Und Dateien, die ein Benutzer in Chat Unterhaltungen gemeinsam in die OneDrive for Business-Konto des Benutzers, der die Dateifreigaben gespeichert werden. Aus diesem Grund müssen Sie die einzelnen Benutzerpostfächer und OneDrive for Business-Konten als Speicherorte für Inhalte, Gespräche und Dateien in der Liste Chat zu durchsuchen hinzufügen.
    
    > [!NOTE]
    > In einer Exchange-hybridbereitstellung können Benutzer mit einem lokalen Postfach Unterhaltungen teilnehmen, die Teil der Liste der Chat in Microsoft-Teams sind. Inhalte aus dieser Unterhaltungen kann in diesem Fall auch durchsucht werden, da es eine Cloud-basierten Speicherbereich (einem *cloudbasierten Postfach für lokale Benutzer*genannt) für Benutzer gespeichert wird, die über ein lokales Postfach verfügen. Weitere Informationen finden Sie unter [Suchen cloudbasierten Postfächer für lokale Benutzer in Office 365](search-cloud-based-mailboxes-for-on-premises-users.md).
  
- Jede Microsoft-Teams oder ein Team Kanal enthält ein Wiki für Notizen und die Zusammenarbeit. Der Wiki-Inhalt wird automatisch in eine Datei mit einem MHT-Format gespeichert. Diese Datei ist in der Dokumentbibliothek Teams Wiki-Daten auf SharePoint-Teamwebsite gespeichert. Inhalt Such-Tool können Sie das Wiki suchen, indem Sie SharePoint-Teamwebsite als Content Speicherort zu suchen. 
    
    > [!NOTE]
    > Die Möglichkeit zum Suchen von Wiki für ein Microsoft-Team oder DDE-Kanal (bei der SharePoint-Teamwebsite Suche) wurde am 22 Juni 2017 veröffentlicht. Wiki-Seiten, die gespeichert oder auf aktualisiert wurden, die Datum oder nachdem verfügbar sind, gesucht werden soll. Zuletzt gespeichert oder vor diesem Datum aktualisiert Wiki-Seiten sind nicht verfügbar für die Suche. 
 
- Zusammenfassende Informationen für Besprechungen und Anrufe in einem Microsoft-Teams Kanal werden auch in den Postfächern der Benutzer, die in die Besprechung oder den Anruf gewählte gespeichert. Dies bedeutet, dass Sie Inhaltssuche verwenden können, um diese Zusammenfassung Datensätze zu suchen. Zusammenfassende Informationen enthält: 
  - Datum, Startzeit, Endzeit und Dauer einer Besprechung oder eines Anrufs

  - Datum und Uhrzeit, wann die einzelnen Teilnehmer sind oder diese verlassen der Besprechung oder einen Anruf

  - Anrufe an die Voicemail gesendet

  - Verpasste oder nicht beantwortete Anrufe

  - Rufen Sie Übertragungen, die als zwei separate Anrufe dargestellt werden

  Beachten Sie, dass es bis zu 8 Stunden für Besprechung, und rufen Zusammenfassung Datensätze zu durchsuchenden verfügbar sein kann.

  Zusammenfassung der Besprechung werden in den Suchergebnissen als **Besprechung** in das **Feld**gekennzeichnet; Anruf Zusammenfassungen werden als **aufrufen**gekennzeichnet. Darüber hinaus werden Unterhaltungen, die Teil einer Teams Kanal- und 1xN Chats sind als **Instant Messaging** , im Feld **Typ** gekennzeichnet.
  
  ![Teams Besprechungen, Anrufe und 1xN Chats werden im Feld identifiziert.](media/O365-ContentSearch-Teams-MessageKind.png)

- Die **Art** -e-Mail-Eigenschaft oder die Suchbedingung **Nachricht Art** können zum Suchen nach Inhalten in Microsoft-Teams, insbesondere. 
  - Geben Sie mit der **Art** -Eigenschaft als Teil der Suchabfrage Schlüsselwort im Feld **Stichwörter** einer Suchabfrage `kind:microsoftteams`.

    ![Verwenden Sie die Art: Microsoftteams in das Feld Schlüsselwörter](media/O365-ContentSearch-Teams-Keywords.png)
  
  - Um eine Bedingung für die Suche zu verwenden, fügen Sie die **Art der Nachricht** Bedingung, und verwenden Sie den Wert `microsoftteams`. 

    ![Verwenden Sie die Nachricht Kind Bedingung mit dem Wert Microsoftteams.](media/O365-ContentSearch-Teams-MessageKindCondition.png)

Beachten Sie, dass Bedingungen logisch mit der Stichwortabfrage durch den **AND** -Operator verbunden sind. Dies bedeutet, dass ein Element übereinstimmen muss, damit der Stichwortabfrage und die Suchbedingung in den Suchergebnissen zurückgegeben werden soll. Weitere Informationen finden Sie im Abschnitt "Richtlinien für die Verwendung von Bedingungen" in [Stichwortabfragen und Suchkriterien für die Inhaltssuche.](keyword-queries-and-search-conditions.md#guidelines-for-using-conditions)

  
### <a name="searching-inactive-mailboxes"></a>Suchen inaktive Postfächer

Sie können inaktiver Postfächer in einer Inhaltssuche suchen. Wenn Sie eine Liste mit den inaktiver Postfächer in Ihrer Organisation erhalten möchten, führen Sie den Befehl `Get-Mailbox -InactiveMailboxOnly` in Exchange Online PowerShell. Alternativ können Sie zu **Daten Governance** wechseln \> **Aufbewahrung** in das Wertpapier &amp; Compliance Center, und klicken Sie dann auf **Weitere**![Navigationsleiste Ellipsen](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **inaktiver Postfächer**.
  
Hier sind einige Dinge im Hinterkopf behalten, inaktiver Postfächer zu suchen.
  
- Wenn eine Inhaltssuche ein Benutzerpostfach enthält und das Postfach dann inaktiv erfolgt, wird die Inhaltssuche weiterhin inaktive Postfach suchen, wenn die Suche erneut ausführen, nachdem es deaktiviert wurde.
    
- In einigen Fällen kann ein Benutzer einer aktiven Postfach- und eines inaktiven Postfachs, die der gleichen SMTP-Adresse verfügen. In diesem Fall wird nur das spezifische Postfach, das Sie als Speicherort für ein Inhaltssuche auswählen gesucht werden soll. Anders ausgedrückt, wenn Sie dem Postfach eines Benutzers zu einer Suche hinzufügen, nicht davon ausgehen, dass ihre aktive und inaktive Postfächer durchsucht werden; Es wird nur das Postfach, das Sie für die Suche explizit hinzu gesucht werden soll.
    
- Es wird dringend empfohlen, dass Sie vermeiden, dass eine aktive Postfach- und inaktiven Postfachs mit der gleichen SMTP-Adresse. Wenn Sie müssen die SMTP-Adresse wiederverwenden, die aktuell eines inaktiven Postfachs zugewiesen ist, wird empfohlen, das inaktive Postfach wiederherstellen oder des Inhalts eines inaktiven Postfachs zu einem aktiven Postfach (oder das Archiv eines aktiven Postfachs wiederherstellen), und Sie löschen die Inaktives Postfach. Weitere Informationen finden Sie in den folgenden Themen:
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md)
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md)
    
  - [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)

  
### <a name="previewing-search-results"></a>Vorschau der Suchergebnisse

Sie können unterstützte Dateitypen in der Vorschau anzeigen. Wenn Sie ein Dateityp nicht unterstützt wird, müssen Sie herunterladen eine Kopie der Datei auf Ihrem lokalen Computer an. Die folgenden Dateitypen werden unterstützt und können im Suchergebnisbereich angezeigt werden.
  
- TXT, HTML, MHTML
    
- EML
    
- doc, DOCX, DOCM
    
- pptm, PPTX-Format
    
- PDF
    
Darüber hinaus werden die folgenden Dateitypen Container unterstützt. Sie können die Liste der Dateien im Container in der Vorschau anzeigen.
  
- ZIP
    
- .gzip
    
### <a name="partially-indexed-items"></a>Teilweise indizierte Elemente

- Wie bereits erklärt, teilweise indizierte Elemente in Postfächern in der geschätzten Suchergebnisse aufgeführt. teilweise indizierte Elemente aus SharePoint und OneDrive werden nicht in der geschätzten Suchergebnisse eingeschlossen. 
    
- Wenn eine teilweise Element entspricht die Suche Abfragen (da es sich um eine andere Nachricht oder ein Dokument Eigenschaften den Suchkriterien entsprechen), werden nicht es in die geschätzte Anzahl der nicht-indizierten Elementen enthalten sein. Wenn ein teilweise Element wird durch die Suchkriterien ausgeschlossen, auch werden nicht aufgenommen in die geschätzte Anzahl der teilweise indizierte Elemente. Weitere Informationen finden Sie unter [teilweise indizierte Elemente in Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md).
    
### <a name="exporting-data-from-myanalytics-and-other-office-365-applications"></a>Exportieren von Daten aus MyAnalytics und anderen Office 365-Clientanwendungen

- Daten aus MyAnalytics (beispielsweise Insights auf wie Benutzer ihre basierend auf Daten von e-Mail und Kalender in ihrem Postfach Zeit) und Daten aus anderen Office 365-Anwendungen ist eine auf einer ausgeblendeten Position (in einer nicht-IPM-Unterstruktur) in cloudbasierten Postfach des Benutzers gespeichert. Nach der Ausführung einer Inhaltssuche diese Daten ist nicht in der geschätzten Suchergebnisse, die Abfragestatistiken enthalten, und es ist nicht verfügbar für die Vorschau. Diese Daten werden jedoch exportiert werden, wenn Sie die Ergebnisse einer Suche exportieren.
    
- Die MyAnalytics-Daten und die Daten aus anderen Office 365-Anwendungen wird in einen Ordner namens "Andere Office 365-Daten" exportiert. Dieser Ordner enthält Unterordner für jeden Benutzer.
  
