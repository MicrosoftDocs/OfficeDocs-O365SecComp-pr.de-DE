---
title: Inhaltssuche in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 53390468-eec6-45cb-b6cd-7511f9c909e4
description: Verwenden Sie die Inhaltssuche im Office 365 &amp; Security Compliance Center, um nach Inhalten in Postfächern, SharePoint Online-Websites, OneDrive-Konten, Microsoft Teams, Office 365-Gruppen und Skype for Business-Unterhaltungen zu suchen. Sie können Keyword-Suchabfragen und Suchbedingungen verwenden, um die Suchergebnisse einzuschränken. Dann können Sie die Suchergebnisse in der Vorschau anzeigen und exportieren. Die Inhaltssuche ist auch ein effektives Tool, um nach Inhalten zu suchen, die möglicherweise mit einer DSGVO-Anforderung verbunden sind.
ms.openlocfilehash: b7ecfc68c143225f097508e2cca0e87b7ce250d6
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296358"
---
# <a name="content-search-in-office-365"></a>Inhaltssuche in Office 365

Sie können das eDiscovery-Tool für die Inhaltssuche im Office 365 &amp; Security Compliance Center verwenden, um in ihrer Office 365-Organisation nach in-Place-Elementen wie e-Mails, Dokumenten und Chatnachrichten zu suchen. Verwenden Sie dieses Tool, um nach Elementen in diesen Office 365-Diensten zu suchen:
  
- Exchange Online-Postfächer und öffentliche Ordner
    
- SharePoint Online-Websites und OneDrive for Business-Konten
    
- Skype for Business-Unterhaltungen
    
- Microsoft Teams 
    
- Office 365-Gruppen
    
Nachdem Sie eine Inhaltssuche ausgeführt haben, wird die Anzahl der inhaltsspeicherorte und eine geschätzte Anzahl von Suchergebnissen im Suchprofil angezeigt. Sie können auch schnell Statistiken anzeigen, beispielsweise die inhaltsspeicherorte mit den meisten Elementen, die mit der Suchabfrage übereinstimmen. Nachdem Sie eine Suche ausgeführt haben, können Sie eine Vorschau der Ergebnisse anzeigen oder Sie auf einen lokalen Computer exportieren.


## <a name="create-a-new-search"></a>Erstellen einer neuen Suche

Um Zugriff auf die Seite " **Inhaltssuche** " zum Ausführen von Suchvorgängen und Vorschau-und Exportergebnisse zu haben, muss ein Administrator, ein Compliance Officer oder ein eDiscovery-Manager Mitglied der rollenGruppe " &amp; eDiscovery Manager" im Security Compliance Center sein. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office 365 &amp; Security Compliance Center](assign-ediscovery-permissions.md).
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrer Office 365-e-Mail-Adresse und Ihrem Kennwort an. 
    
3. Klicken Sie im &amp; Security Compliance Center auf **Search &amp; Investigation** \> **Content Search**.
    
4. Klicken Sie auf der Seite **Suchen** auf den Pfeil neben ![Symbol](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **neue Suche**hinzufügen. 
    
    ![Die neue Dropdownliste für die Suche](media/76b25861-55c5-4f50-9d48-9e2be2d0d078.png)
  
    Sie können eine der folgenden Optionen auswählen:
    
  - **Guided search** -mit dieser Option wird ein Assistent gestartet, der Sie durch die Erstellung der Suche führt. Die Benutzeroberfläche, um inhaltsspeicherorte auszuwählen und die Suchabfrage zu erstellen, ist identisch mit der **neuen Such** Option. 
    
  - **Neue Suche** : mit dieser Option wird eine aktualisierte Benutzeroberfläche zum Erstellen einer neuen Suche angezeigt. Dies ist die Standardoption, wenn Sie auf **neue Suche**klicken.
    
  - **Suche nach ID-Liste** – mit dieser Option können Sie mit einer Liste von Exchange-IDs nach bestimmten e-Mail-Nachrichten und anderen Postfachelementen suchen. Um eine ID-Listensuche (formell als gezielte Suche bezeichnet) zu erstellen, übermitteln Sie eine CSV-Datei (Comma Separated Value), die die zu suchenden Postfachelemente identifiziert. Weitere Informationen finden Sie unter [Vorbereiten einer CSV-Datei für die Inhaltssuche einer ID-Liste in Office 365](csv-file-for-an-id-list-content-search.md).
    
    Die restlichen Schritte in diesem Verfahren folgen dem standardmäßigen neuen Such Workflow.
    
5. Klicken Sie in der Dropdownliste auf **neue Suche** . 
    
6. Geben Sie unter **Suchabfrage**die folgenden Punkte an.
    
    ![Angeben von Stichwörtern, Bedingungen und Speicherorten für die Suche](media/1e6de9dd-eac9-4e2a-819d-9740cf6c9106.png)
  
- **Zu suchende Schlüsselwörter** -geben Sie im Feld **Stichwörter** eine Suchabfrage ein. Sie können Schlüsselwörter, Nachrichteneigenschaften wie gesendete und empfangene Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, an dem ein Dokument zuletzt geändert wurde, angeben. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**. Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Schlüsselwortfeld leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in die Suchergebnisse eingeschlossen.
    
    Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** klicken und in jeder Zeile ein Stichwort eingeben. Wenn Sie dies tun, werden die Schlüsselwörter in jeder Zeile durch einen logischen Operator ( **c:s**) verbunden, der in der Funktionalität mit dem **or** -Operator in der erstellten Suchabfrage vergleichbar ist. 
    
    Gründe für die Verwendung der Keyword-Liste Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit jedem Stichwort übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Schlüsselwörter am meisten (und am wenigsten) wirksam sind. Sie können auch eine Schlüsselwortphrase (umgeben von Klammern) in einer Zeile verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [View Keyword Statistics for Content Search results](view-keyword-statistics-for-content-search.md).

    [!NOTE] Um Probleme zu vermeiden, die durch umfangreiche Stichwortlisten verursacht werden, sind Sie jetzt auf maximal 20 Zeilen in der Keyword-Liste beschränkt.
    
- **Bedingungen** : Sie können Suchbedingungen hinzufügen, um eine Suche einzuschränken und eine genauere Ergebnismenge zurückzugeben. Jede Bedingung fügt eine Klausel zu der Suchabfrage hinzu, die erstellt und beim Starten der Suche ausgeführt wird. Eine Bedingung ist logisch mit der Stichwortabfrage (angegeben im Stichwortfeld) durch einen logischen Operator ( **c:c**) verbunden, der in der Funktionalität mit dem **and-** Operator vergleichbar ist. Dies führt dazu, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in die Ergebnisse eingeschlossen werden sollen. Auf diese Weise können Sie Ihre Ergebnisse einschränken. Eine Liste und Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" in [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md#search-conditions).
    
- **Standorte** – wählen Sie die zu durchsuchenden inhaltsspeicherorte aus.
    
  - **Alle Standorte** -verwenden Sie diese Option, um alle inhaltsspeicherorte in Ihrer Organisation zu durchsuchen. Dazu gehören e-Mails in allen Exchange-Postfächern (einschließlich aller inaktiven Postfächer, Postfächer für alle Office 365-Gruppen, Postfächer für alle Microsoft Teams), alle Skype for Business-Unterhaltungen, alle SharePoint-und OneDrive für Business-Websites (einschließlich der Websites für alle Office 365-Gruppen und Microsoft Teams) und Elemente in allen öffentlichen Exchange-Ordnern.
    
  - **Bestimmte Standorte** -verwenden Sie diese Option, um bestimmte inhaltsspeicherorte zu durchsuchen. Sie können alle inhaltsspeicherorte für einen bestimmten Office 365-Dienst durchsuchen (beispielsweisedurch Suchen aller Exchange-Postfächer oder Durchsuchen aller SharePoint-Websites), oder Sie können bestimmte Standorte in einem der Office 365-Dienste durchsuchen, die angezeigt werden. 
    
    ![Benutzeroberfläche zur Auswahl der zu durchsuchenden inhaltsspeicherorte](media/9a09708b-f8a2-4382-8c4e-2c610ec33c72.png)
  
    Beachten Sie, dass Sie der Liste der zu durchsuchenden Exchange-Postfächer auch Verteilergruppen hinzufügen können. Für Verteilergruppen werden die Postfächer der Gruppenmitglieder durchsucht. Beachten Sie, dass dynamische Verteilergruppen nicht unterstützt werden.
    
    **Wichtig:** Wenn Sie alle Postfachspeicher Orte oder nur bestimmte Postfächer durchsuchen, werden Daten aus myAnalytics und anderen Office 365-Anwendungen, die in Benutzerpostfächern gespeichert sind, beim Exportieren der Ergebnisse einer Inhaltssuche eingeschlossen. Diese Daten werden nicht in die geschätzten Suchergebnisse eingeschlossen und stehen nicht für die Vorschau zur Verfügung. Sie wird nur beim Exportieren und Herunterladen der Suchergebnisse eingeschlossen. Weitere Informationen finden Sie unter [Exportieren von Daten aus myAnalytics und anderen Office 365-Anwendungen](#exporting-data-from-myanalytics-and-other-office-365-applications) im Abschnitt "Weitere Information über Inhaltssuche". 
    
7. Nachdem Sie Ihre Suchabfrage eingerichtet haben, klicken Sie **auf &amp; Run speichern**.
    
8. Geben Sie auf der Seite **Suche speichern** einen Namen für die Suche und eine optionale Beschreibung ein, die die Suche erleichtert. Beachten Sie, dass der Name der Suche in Ihrer Organisation eindeutig sein muss. 
    
9. Klicken Sie auf **Speichern** , um die Suche zu starten. 
    
    Nachdem Sie die Suche gespeichert und ausgeführt haben, werden alle von der Suche zurückgegebenen Ergebnisse im Ergebnisbereich angezeigt. Je nachdem, wie Sie die Vorschau Einstellung konfiguriert haben, werden die Suchergebnisse angezeigt, oder Sie müssen auf **Vorschau Ergebnisse** klicken, um Sie anzuzeigen. Weitere Informationen finden Sie im nächsten Abschnitt. 
    
Um erneut auf diese Inhaltssuche zuzugreifen oder auf andere auf der Seite **Inhaltssuche** aufgeführte Inhalts Suchvorgänge zuzugreifen, wählen Sie die Suche aus, und klicken Sie dann auf **Öffnen**. 
  
Klicken Sie ![auf Symbol](media/O365-MDM-CreatePolicy-AddIcon.gif) **** hinzufügen, um die Ergebnisse zu löschen oder eine neue Suche zu erstellen. 

  
## <a name="preview-search-results"></a>Suchergebnisse in der Vorschau anzeigen

Es gibt zwei Konfigurationseinstellungen für die Vorschau der Suchergebnisse. Nachdem Sie eine neue Suche ausgeführt oder eine vorhandene Suche geöffnet haben, klicken Sie auf * * Einzelergebnisse * *, um die folgenden Vorschaueinstellungen anzuzeigen: 
  
![Vorschau der Suchergebnis Einstellungen](media/83519477-1c85-4442-8886-481f186fd758.png)
  
1. **Automatische Vorschau der Ergebnisse** – mit dieser Einstellung werden die Suchergebnisse angezeigt, nachdem Sie eine Suche ausgeführt haben.
    
2. **Ergebnisse manuell** anzeigen – mit dieser Einstellung werden Platzhalter im Suchergebnisbereich angezeigt und die Schaltfläche **Vorschau Ergebnisse** angezeigt, auf die Sie klicken müssen, um die Suchergebnisse anzuzeigen. Dies ist die Standardeinstellung; Dadurch wird die Suchleistung verbessert, da beim Öffnen einer vorhandenen Suche nicht automatisch die Suchergebnisse angezeigt werden. 
    
Es gibt Beschränkungen im Zusammenhang mit der Anzahl der verfügbaren Elemente für die Vorschau. Weitere Informationen finden Sie unter [Grenzwerte für die Suche im Office 365 &amp; Security Compliance Center](limits-for-content-search.md). 
  
Eine Liste der unterstützten Dateitypen, die in der Vorschau angezeigt werden können, finden Sie unter [Vorschau der Suchergebnisse](#previewing-search-results) im Abschnitt "Weitere Informationen zur Inhaltssuche". Wenn ein Dateityp für die Vorschau nicht unterstützt wird oder eine Kopie eines Dokuments heruntergeladen wird, können Sie auf **Originaldatei herunter** laden klicken, um Sie auf Ihren lokalen Computer herunterzuladen. Für aspx-Webseiten ist die URL für die Seite enthalten, obwohl Sie möglicherweise nicht über die Berechtigungen für den Zugriff auf die Seite verfügen. 
  
Beachten Sie, dass nicht indizierte Elemente für die Vorschau nicht verfügbar sind.
  
## <a name="view-information-and-statistics-about-a-search"></a>Anzeigen von Informationen und Statistiken zu einer Suche

Nach dem Erstellen und Ausführen einer Inhaltssuche können Sie Statistiken zu den geschätzten Suchergebnissen anzeigen. Hierzu gehören eine Zusammenfassung der Suchergebnisse, die Abfragestatistiken wie die Anzahl der inhaltsspeicherorte mit Elementen, die mit der Suchabfrage übereinstimmen, und der Name der inhaltsspeicherorte, die die meisten übereinstimmenden Elemente aufweisen. Sie können Statistiken für eine oder mehrere Inhalts Suchvorgänge anzeigen. Auf diese Weise können Sie die Ergebnisse für mehrere Suchvorgänge schnell vergleichen und Entscheidungen zur Effektivität ihrer Suchabfragen treffen.
  
Sie können die Suchstatistiken und Keyword-Statistiken auch in eine CSV-Datei herunterladen. Auf diese Weise können Sie die Filter-und Sortierfunktionen in Excel verwenden, um Ergebnisse zu vergleichen und Berichte für Ihre Suchergebnisse vorzubereiten.
  
So zeigen Sie Suchstatistiken an
  
1. Klicken Sie auf der Seite **Inhaltssuche** im &amp; Security Compliance Center auf **Öffnen** , und klicken Sie dann auf die Suche, für die Sie die Statistik anzeigen möchten. 
    
2. Klicken Sie auf der Seite Fly Out auf **Abfrage öffnen**. 
    
3. Klicken Sie in der Dropdownliste **Einzelergebnisse** auf **Suchprofil**.
    
4. Klicken Sie in der Dropdownliste **Typ** auf eine der folgenden Optionen, je nachdem, welche Suchstatistiken angezeigt werden sollen. 
    
  - **Zusammenfassung** : zeigt Statistiken für jeden Typ von durchsuchten Inhaltsspeicherorten an. Dieser Inhalt gibt die Anzahl der inhaltsspeicherorte an, die Elemente enthalten, die mit der Suchabfrage übereinstimmen, sowie die Gesamtanzahl und Größe der Suchergebnis Elemente. Dies ist die Standardeinstellung.
    
  - **Queries** – zeigt Statistiken zur Suchabfrage an. Dies umfasst die Art des Inhaltsspeicherorts, auf den die Abfragestatistik angewendet werden soll, ein Teil der Suchabfrage, auf die die **** Statistik angewendet werden soll (Beachten Sie, dass Primary die gesamte Suchabfrage angibt), die Anzahl der inhaltsspeicherorte, die Elemente enthalten, die Übereinstimmung mit der Suchabfrage und der Gesamtanzahl und-Größe und den gefundenen Elementen (am angegebenen Inhaltsspeicherort), die mit der Suchabfrage übereinstimmen. Beachten Sie, dass Statistiken für nicht indizierte Elemente (auch als teilweise indizierte Elemente bezeichnet) ebenfalls angezeigt werden. Die Statistik enthält jedoch nur teilweise indizierte Elemente aus Postfächern. Teilweise indizierte Elemente aus SharePoint und OneDrive sind nicht in der Statistik enthalten.
    
  - **Top Locations** – zeigt Statistiken zur Anzahl der Elemente an, die mit der Suchabfrage an jedem gesuchten Inhaltsspeicherort übereinstimmen. Die Top 1.000-Speicherorte werden angezeigt.
    
Ausführlichere Informationen zu Suchstatistiken finden Sie unter [View Keyword Statistics for Content Search results](view-keyword-statistics-for-content-search.md).
  
  
## <a name="export-search-results"></a>Exportieren der Suchergebnisse

Nachdem eine Suche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse auf einen lokalen Computer exportieren. Wenn Sie e-Mail-Ergebnisse exportieren, können diese als PST-Dateien oder als einzelne Nachrichten (msg-Dateien) auf Ihren Computer heruntergeladen werden. Beim Exportieren von Inhalten aus SharePoint-und OneDrive-Websites werden Kopien von systemeigenen Office-Dokumenten exportiert. Es gibt auch zusätzliche Dokumente und Berichte, die in den exportierten Suchergebnissen enthalten sind. Sie können den Suchergebnisbericht auch nur exportieren und nicht die tatsächlichen Elemente.
  
So exportieren Sie Suchergebnisse:
  
1. Klicken Sie auf der Seite **Inhaltssuche** im &amp; Security Compliance Center auf **Öffnen** , und klicken Sie dann auf die Suche, für die Sie die Suchergebnisse exportieren möchten. 
    
2. Klicken Sie ![auf der Seite Fly Out auf Suchergebnis Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) exportieren **mehr**, und klicken Sie dann auf **Ergebnisse exportieren**. Beachten Sie, dass Sie einen Suchergebnisbericht auch exportieren können.
    
3. Füllen Sie die Abschnitte auf der Fly-Out-Navigation der **Exportergebnisse** aus. Stellen Sie sicher, dass Sie Bildlaufleiste verwenden, um alle Exportoptionen anzuzeigen. 
    
Ausführlichere Anweisungen und Tipps zur Problembehandlung finden Sie unter:
  
- [Exportieren von Suchergebnissen aus dem Office 365 &amp; Security Compliance Center](export-search-results.md)
    
- [Exportieren eines Inhaltssuchberichts](export-a-content-search-report.md)
    

  
## <a name="more-information-about-content-search"></a>Weitere Informationen zur Inhaltssuche

Weitere Informationen zu Inhalts suchen finden Sie in den folgenden Abschnitten.
  
[Grenzwerte für die Inhaltssuche](#content-search-limits)
  
[Erstellen einer Suchabfrage](#building-a-search-query)
  
[DurchSuchen von OneDrive-Konten](#searching-onedrive-accounts)
  
[DurchSuchen von Microsoft Teams und Office 365-Gruppen](#searching-microsoft-teams-and-office-365-groups)
  
[DurchSuchen inaktiver Postfächer](#searching-inactive-mailboxes)
  
[Anzeigen einer Vorschau der Suchergebnisse](#previewing-search-results)
  
[Teilweise indizierte Elemente](#partially-indexed-items)
  
[Exportieren von Daten aus myAnalytics und anderen Office 365-Anwendungen](#exporting-data-from-myanalytics-and-other-office-365-applications)
  
### <a name="content-search-limits"></a>Grenzwerte für die Inhaltssuche

- Eine Beschreibung der Grenzwerte für die Inhaltssuche finden Sie unter [Grenzwerte für die Suche im Office 365 Security &amp; Compliance Center](limits-for-content-search.md).
    
- Microsoft sammelt Leistungsinformationen für Inhaltssuche, die von allen Office 365-Organisationen ausgeführt werden. Während sich die Komplexität der Suchabfrage auf die Suchzeiten auswirken kann, ist der größte Faktor für die Dauer der Suche die Anzahl der durchsuchten Postfächer. Obwohl Microsoft keine Vereinbarung zum Service Level für Suchzeiten bereitstellt, werden in der folgenden Tabelle die durchschnittlichen Suchzeiten für eine Inhaltssuche basierend auf der Anzahl der Postfächer aufgeführt, die in der Suche enthalten sind.
    
|**Anzahl der Postfächer**|**Durchschnittliche Suchzeit**|
|:-----|:-----|
|100  <br/> |30 Sekunden  <br/> |
|1,000  <br/> |45 Sekunden  <br/> |
|10,000  <br/> |4 Minuten  <br/> |
|25.000  <br/> |10 Minuten  <br/> |
|50.000  <br/> |20 Minuten  <br/> |
|100,000  <br/> |25 Minuten  <br/> |
  
### <a name="building-a-search-query"></a>Erstellen einer Suchabfrage

Ausführliche Informationen zum Erstellen einer Suchabfrage, verwenden von booleschen Suchoperatoren und Suchbedingungen sowie zum Suchen nach vertraulichen Informationstypen und Inhalten, die für Benutzer außerhalb Ihrer Organisation freigegeben sind, finden Sie unter [Stichwortabfragen und Suchbedingungen. für die Inhaltssuche ](keyword-queries-and-search-conditions.md).
  
Beachten Sie bei der Verwendung der Stichwortliste zum Erstellen einer Suchabfrage die folgenden Aspekte.
  
- Sie müssen das Kontrollkästchen **Keyword-Liste anzeigen** aktivieren und dann jedes Schlüsselwort in eine separate Zeile eingeben, um eine Suchabfrage zu erstellen, in der die Schlüsselwörter (oder Stichwort Ausdrücke) in jeder Zeile durch den **or** -Operator verbunden werden. Wenn Sie nur eine Liste mit Stichwörtern in das Stichwortfeld einfügen oder die **Eingabe** Taste drücken, nachdem Sie ein Schlüsselwort eingegeben haben, werden Sie nicht durch den **or** -Operator verbunden. Hier sind falsch und richtig Beispiel für das Hinzufügen einer Liste von Schlüsselwörtern. 
    
    **Falsche**
    
    ![Die falsche Methode zum Formatieren einer Schlüsselwortliste (durch Einfügen der Liste in das Stichwortfeld)](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Richtig**
    
    ![Die richtige Methode zum Formatieren einer Stichwortliste (durch Auswahl von CheckBox und dann Einfügen einer Liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
- Sie können auch eine Liste von Schlüsselwörtern oder Keyword-Phrasen in einer Excel-Datei oder in einer nur-Text-Datei vorbereiten und dann Ihre Liste in die Stichwortliste kopieren und einfügen. Hierzu müssen Sie das Kontrollkästchen **Keyword-Liste anzeigen** aktivieren. Klicken Sie dann auf die erste Zeile in der Stichwortliste, und fügen Sie Ihre Liste ein. Jede Zeile aus der Excel-oder Textdatei wird in eine separate Zeile in der Stichwortliste eingefügt. 
    
- Nachdem Sie eine Abfrage mithilfe der Stichwortliste erstellt haben, empfiehlt es sich, die Suchabfrage Syntax zu überprüfen, um die beabsichtigte Suchabfrage zu aktivieren. In der Suchabfrage, die im Detailbereich unter **Query** angezeigt wird, werden die Schlüsselwörter durch den Text **(c:s)** getrennt. Dies gibt an, dass die Schlüsselwörter durch einen logischen Operator ähnlich der Funktionalität mit dem **or** -Operator verbunden sind. Wenn Ihre Suchabfrage Bedingungen enthält, werden die Schlüsselwörter und die Bedingungen entsprechend durch den Text **(c:c)** getrennt. Dies weist darauf hin, dass die Schlüsselwörter mit den Bedingungen mit einem logischen Operator verbunden sind, der in der Funktionalität mit dem **und** Operator. Nachfolgend finden Sie ein Beispiel für die Suchabfrage (wird im Detailbereich angezeigt), die bei Verwendung der Stichwortliste und einer Bedingung resultiert. 
    
    ![Beispiel für die Abfrage, die erstellt wird, wenn die Stichwortliste und eine Bedingung verwendet wird](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
- Wenn Sie eine Inhaltssuche ausführen, prüft Office 365 automatisch Ihre Suchabfrage nach nicht unterstützten Zeichen und für boolesche Operatoren, die möglicherweise nicht groß geschrieben werden. Nicht unterstützte Zeichen werden oft ausgeblendet und verursachen in der Regel einen Suchfehler oder geben unbeabsichtigte Ergebnisse zurück. Weitere Informationen zu den nicht unterstützten Zeichen, die überprüft werden, finden Sie unter [Überprüfen der Inhalts Suchabfrage auf Fehler](check-your-content-search-query-for-errors.md).
    
- Wenn Sie über eine Suchabfrage mit Schlüsselwörtern für nicht englische Zeichen (beispielsweise chinesische Zeichen) verfügen, können Sie in der Inhaltssuche](media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) auf **Sprache-Land/Region**![-Abfragesprache-Land/Region (Symbol) und dann auf eine Language-Country-Kultur Codewert für die Suche. Beachten Sie, dass die Standardsprache/Region neutral ist. Wie können Sie feststellen, ob die Spracheinstellung für eine Inhaltssuche geändert werden muss? Wenn Sie bestimmte inhaltsspeicherorte die nicht-englischen Zeichen enthalten, die Sie suchen, aber die Suche keine Ergebnisse zurückgibt, kann die Spracheinstellung die Ursache sein. 
  
### <a name="searching-onedrive-accounts"></a>DurchSuchen von OneDrive-Konten

- Informationen zum Erfassen einer Liste der URLs für die OneDrive-Websites in Ihrer Organisation finden Sie unter [Erstellen einer Liste aller OneDrive-Standorte in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Dieses Skript in diesem Artikel erstellt eine Textdatei, die eine Liste aller OneDrive-Websites enthält. Um dieses Skript ausführen zu können, müssen Sie die SharePoint Online-Verwaltungsshell installieren und verwenden. Fügen Sie die URL der mysite-Domäne Ihrer Organisation jeder OneDrive-Website, die Sie durchsuchen möchten, hinzu. Dies ist die Domäne, die alle Ihre OneDrive enthält. Beispiel: `https://contoso-my.sharepoint.com`. Nachfolgend finden Sie ein Beispiel für eine URL für die OneDrive-Website `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`eines Benutzers:.
    
    In dem seltenen Fall, dass der Benutzerprinzipalname (UPN) einer Person geändert wird, wird auch die URL für Ihren OneDrive-Speicherort geändert, um den neuen UPN zu integrieren. In diesem Fall müssen Sie eine Inhaltssuche ändern, indem Sie die neue OneDrive-URL des Benutzers hinzufügen und den alten entfernen.
  
### <a name="searching-microsoft-teams-and-office-365-groups"></a>DurchSuchen von Microsoft Teams und Office 365-Gruppen

Sie können das Postfach durchsuchen, das einer Office 365-Gruppe oder einem Microsoft-Team zugeordnet ist. Da Microsoft Teams in Office 365-Gruppen erstellt werden, sind Sie sehr ähnlich. In beiden Fällen wird nur das Postfach der Gruppe oder des Teams durchsucht; die Postfächer der Gruppe oder Teammitglieder wurden nicht durchsucht. Um Sie durchsuchen zu können, müssen Sie Sie der Suche ausdrücklich hinzufügen.
  
Beachten Sie bei der Suche nach Inhalten in Microsoft Teams-und Office 365-Gruppen die folgenden Aspekte.
  
- Zum Suchen nach Inhalten in Microsoft Teams-und Office 365-Gruppen müssen Sie das Postfach und die SharePoint-Website angeben, die einem Team oder einer Gruppe zugeordnet sind.
    
- Führen Sie das Cmdlet **Get-Unifiedgroup** in Exchange Online aus, um die Eigenschaften für ein Microsoft-Team oder eine Office 365-Gruppe anzuzeigen. Dies ist eine gute Möglichkeit, die URL für die Website abzurufen, die einem Team oder einer Gruppe zugeordnet ist. Mit dem folgenden Befehl werden beispielsweise ausgewählte Eigenschaften für eine Office 365-Gruppe mit dem Namen "Senior Leadership Team" angezeigt: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Damit Sie das Cmdlet **Get-Unifiedgroup** ausführen können, müssen Sie die Rolle "nur anzeigen" in Exchange Online oder Mitglied einer Rollengruppe haben, der die Rolle "nur anzeigen" zugewiesen ist. 
  
- Wenn das Postfach eines Benutzers durchsucht wird, wird jede Microsoft-Team-oder Office 365-Gruppe, der der Benutzer angehört, nicht durchsucht. Auf ähnliche Weise wird beim Durchsuchen eines Microsoft-Teams oder einer Office 365-Gruppe nur das Gruppenpostfach und die von Ihnen angegebene Gruppen Website durchsucht; die Postfächer und OneDrive für Geschäftskonten von Gruppenmitgliedern werden nicht durchsucht, es sei denn, Sie fügen Sie der Suche explizit hinzu.
    
- Wenn Sie eine Liste der Mitglieder eines Microsoft-Teams oder einer Office 365-Gruppe abrufen möchten, können Sie die Eigenschaften auf der Seite **Start \> gruppen** im Office 365 Admin Center anzeigen. Alternativ können Sie den folgenden Befehl in Exchange Online PowerShell ausführen: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Damit Sie das Cmdlet **Get-UnifiedGroupLinks** ausführen können, müssen Sie die Rolle "nur anzeigen" in Exchange Online oder Mitglied einer Rollengruppe haben, der die Rolle "nur anzeigen" zugewiesen ist. 
  
- Unterhaltungen, die Teil eines Microsoft Teams-Kanals sind, werden in dem Postfach gespeichert, das dem Microsoft-Team zugeordnet ist. Entsprechend werden Dateien, die Teammitglieder in einem Kanal freigeben, auf der SharePoint-Website des Teams gespeichert. Daher müssen Sie das Microsoft Team-Postfach und die SharePoint-Website als Inhaltsspeicherort hinzufügen, um Unterhaltungen und Dateien in einem Kanal zu durchsuchen.
    
- Alternativ werden Unterhaltungen, die Teil der Chat Liste in Microsoft Teams sind, im Exchange Online-Postfach der Benutzer gespeichert, die am Chat teilnehmen. Und Dateien, die ein Benutzer in Chat Unterhaltungen freigibt, werden im OneDrive for Business-Konto des Benutzers gespeichert, der die Datei freigibt. Daher müssen Sie die einzelnen Benutzerpostfächer und OneDrive für Geschäftskonten als inhaltsspeicherorte hinzufügen, um Unterhaltungen und Dateien in der Chat Liste zu durchsuchen.
    
    > [!NOTE]
    > In einer Exchange-hybridbereitstellung können Benutzer mit einem lokalen Postfach an Unterhaltungen teilnehmen, die in der Chat Liste in Microsoft Teams enthalten sind. In diesem Fall ist der Inhalt dieser Unterhaltungen auch durchsuchbar, da er in einem cloudbasierten Speicherbereich (als *Cloud-basiertes Postfach für lokale Benutzer*bezeichnet) für Benutzer gespeichert wird, die über ein lokales Postfach verfügen. Weitere Informationen finden Sie unter [Durchsuchen von cloudbasierten Postfächern für lokale Benutzer in Office 365](search-cloud-based-mailboxes-for-on-premises-users.md).
  
- Jeder Microsoft-Team-oder Team Kanal enthält ein wiki für Notizen und Zusammenarbeit. Der wiki-Inhalt wird automatisch in einer Datei mit dem MHT-Format gespeichert. Diese Datei wird in der Microsoft Teams-wiki-Datendokument Bibliothek auf der SharePoint-Website des Teams gespeichert. Sie können das Inhaltssuche-Tool verwenden, um das Wiki zu durchsuchen, indem Sie die SharePoint-Website des Teams als den zu durchsuchenden Inhaltsspeicherort angeben. 
    
    > [!NOTE]
    > Die Möglichkeit zum Durchsuchen des Wikis nach einem Microsoft-Team oder-Kanal (beim Durchsuchen der SharePoint-Website des Teams) wurde am 2017 veröffentlicht. Wiki-Seiten, die an diesem oder nach dem Datum gespeichert oder aktualisiert wurden, können durchsucht werden. Wiki-Seiten, die zuletzt gespeichert oder vor diesem Datum aktualisiert wurden, sind nicht für die Suche verfügbar. 
 
- Zusammenfassende Informationen für Besprechungen und Anrufe in einem Microsoft Teams-Kanal werden auch in den Postfächern der Benutzer gespeichert, die sich in die Besprechung oder den Anruf eingewählt haben. Dies führt dazu, dass Sie die Inhaltssuche zum Durchsuchen dieser zusammenfassenden Datensätze verwenden können. Zu den zusammenfassenden Informationen gehören: 
  - Datum, Startzeit, Endzeit und Dauer einer Besprechung oder eines Anrufs

  - Das Datum und die Uhrzeit, zu denen jeder Teilnehmer der Besprechung oder dem Anruf beigetreten ist.

  - An Voicemail gesendete Anrufe

  - VerPasste oder nicht entgegengenommene Anrufe

  - Anruf Übertragungen, die als zwei getrennte Anrufe dargestellt werden

  Beachten Sie, dass es bis zu 8 Stunden dauern kann, bis Besprechungs-und Anruf Zusammenfassungs Einträge durchsucht werden können.

  In den Suchergebnissen werden Besprechungs Zusammenfassungen im **Feld Typ**als **Besprechung** identifiziert. Anruf Zusammenfassungen werden als **Anruf**identifiziert. Darüber hinaus werden Unterhaltungen, die Teil eines Teams-Kanals und 1xN-Chats sind, als **Sofortnachrichten** im Feld **Typ** identifiziert.
  
  ![Teams-Besprechungen, Anrufe und 1xN-Chats werden im Feld Typ identifiziert.](media/O365-ContentSearch-Teams-MessageKind.png)

- Sie können die **Art** -e-Mail-Eigenschaft oder die **Nachrichtentyp** -Suchbedingung verwenden, um in Microsoft Teams gezielt nach Inhalten zu suchen. 
  - Wenn Sie die **Kind** -Eigenschaft als Teil der Keyword-Suchabfrage verwenden möchten, geben `kind:microsoftteams`Sie im Feld **Stichwörter** einer Suchabfrage ein.

    ![Verwenden Sie die Art: verläuft im Feld Schlüsselwörter.](media/O365-ContentSearch-Teams-Keywords.png)
  
  - Wenn Sie eine Suchbedingung verwenden möchten, fügen Sie die Bedingung für die **Nachrichten Freundlichkeit** hinzu, und verwenden Sie den Wert `microsoftteams`. 

    ![Verwenden Sie die Message Kind-Bedingung mit dem Wert verläuft.](media/O365-ContentSearch-Teams-MessageKindCondition.png)

Beachten Sie, dass Bedingungen logisch mit der Schlüsselwortabfrage vom **and-** Operator verbunden sind. Das muss bedeuten, dass ein Element sowohl der Stichwortabfrage als auch der Suchbedingung entspricht, die in den Suchergebnissen zurückgegeben werden soll. Weitere Informationen finden Sie im Abschnitt "Richtlinien für die Verwendung von Bedingungen" in [Stichwortabfragen und Suchbedingungen für die Inhaltssuche.](keyword-queries-and-search-conditions.md#guidelines-for-using-conditions)

  
### <a name="searching-inactive-mailboxes"></a>DurchSuchen inaktiver Postfächer

Sie können inaktive Postfächer in einer Inhaltssuche durchsuchen. Führen Sie den Befehl `Get-Mailbox -InactiveMailboxOnly` in Exchange Online PowerShell aus, um eine Liste der inaktiven Postfächer in Ihrer Organisation zu erhalten. Alternativ können Sie im](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> Security &amp; Compliance Center zu **Data Governance** \> **Retention** wechseln und dann auf **Weitere**![Navigationsleisten Ellipsen inaktive **Postfächer**klicken.
  
Im folgenden finden Sie einige Punkte, die Sie beachten sollten, wenn Sie inaktive Postfächer durchsuchen.
  
- Wenn eine Inhaltssuche ein Benutzerpostfach enthält und das Postfach dann inaktiv ist, wird die Inhaltssuche weiterhin das inaktive Postfach durchsuchen, wenn Sie die Suche erneut ausführen, nachdem Sie inaktiv wurde.
    
- In einigen Fällen kann ein Benutzer über ein aktives Postfach und ein inaktives Postfach mit derselben SMTP-Adresse verfügen. In diesem Fall wird nur das bestimmte Postfach, das Sie als Speicherort für eine Inhaltssuche auswählen, durchsucht. Anders ausgedrückt: Wenn Sie ein Benutzerpostfach zu einer Suche hinzufügen, können Sie nicht davon ausgehen, dass sowohl Ihre aktiven als auch die inaktiven Postfächer durchsucht werden. nur das Postfach, das Sie der Suche explizit hinzufügen, wird durchsucht.
    
- Es wird dringend empfohlen, ein aktives Postfach und ein inaktives Postfach mit derselben SMTP-Adresse zu vermeiden. Wenn Sie die SMTP-Adresse, die derzeit einem inaktiven Postfach zugewiesen ist, wieder verwenden müssen, sollten Sie das inaktive Postfach wiederherstellen oder den Inhalt eines inaktiven Postfachs in einem aktiven Postfach (oder im Archiv eines aktiven Postfachs) wiederherstellen und dann den inaktives Postfach. Weitere Informationen finden Sie in einem der folgenden Themen:
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md)
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md)
    
  - [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)

  
### <a name="previewing-search-results"></a>Anzeigen einer Vorschau der Suchergebnisse

Im Vorschaubereich können Sie eine Vorschau der unterstützten Dateitypen anzeigen. Wenn ein Dateityp nicht unterstützt wird, müssen Sie eine Kopie der Datei auf den lokalen Computer herunterladen, um Sie anzuzeigen. Die folgenden Dateitypen werden unterstützt und können im Suchergebnisbereich angezeigt werden.
  
- . txt,. html,. MHTML
    
- . eml
    
- . doc,. docx,. docm
    
- . pptm, PPTX
    
- PDF
    
Darüber hinaus werden die folgenden Dateicontainer Typen unterstützt. Sie können die Liste der Dateien im Container im Vorschaubereich anzeigen.
  
- ZIP
    
- . gzip
    
### <a name="partially-indexed-items"></a>Teilweise indizierte Elemente

- Wie bereits erläutert, sind teilweise indizierte Elemente in Postfächern in die geschätzten Suchergebnisse eingeschlossen. teilweise indizierte Elemente aus SharePoint und OneDrive sind nicht in den geschätzten Suchergebnissen enthalten. 
    
- Wenn ein Teilelement mit der Suchabfrage übereinstimmt (da andere Nachrichten-oder Dokumenteigenschaften den Suchkriterien entsprechen), wird es nicht in der geschätzten Anzahl von nicht indizierten Elementen eingeschlossen. Wenn ein Teilelement durch die Suchkriterien ausgeschlossen wird, wird es auch nicht in die geschätzte Anzahl von teilweise indizierten Elementen eingeschlossen. Weitere Informationen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md).
    
### <a name="exporting-data-from-myanalytics-and-other-office-365-applications"></a>Exportieren von Daten aus myAnalytics und anderen Office 365-Anwendungen

- Daten aus myAnalytics (beispielsweise Einblicke darüber, wie Benutzer ihre Zeit auf der Grundlage von e-Mails und Kalenderdaten in Ihrem Postfach verbringen) und Daten aus anderen Office 365-Anwendungen werden in einem cloudbasierten Postfach des Benutzers in einem verborgenen Speicherort (in einer nicht-IPM-Unterstruktur) gespeichert. Nachdem Sie eine Inhaltssuche ausgeführt haben, werden diese Daten nicht in die geschätzten Suchergebnisse, die Abfragestatistik eingeschlossen und sind nicht für die Vorschau verfügbar. Diese Daten werden jedoch exportiert, wenn Sie die Ergebnisse einer Suche exportieren.
    
- Die myAnalytics-Daten und die Daten aus anderen Office 365-Anwendungen werden in einen Ordner mit dem Namen "andere Office 365-Daten" exportiert. Dieser Ordner enthält Unterordner für jeden Benutzer.
  
