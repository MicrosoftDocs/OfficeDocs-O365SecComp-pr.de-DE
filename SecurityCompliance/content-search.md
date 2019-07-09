---
title: Inhaltssuche in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
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
description: Verwenden Sie das Tool für die Inhaltssuche im Compliance Center in Office 365 oder Microsoft 365, um nach Inhalten in Postfächern, SharePoint Online Websites, OneDrive-Konten, Microsoft Teams, Office 365 Gruppen und Skype for Business-Unterhaltungen zu suchen. Sie können Keyword-Suchabfragen und Suchbedingungen verwenden, um die Suchergebnisse einzuschränken. Anschließend können Sie die Suchergebnisse anzeigen und exportieren. Die Inhaltssuche ist auch ein effektives Tool zum Suchen nach Inhalten im Zusammenhang mit einer dsgvo-Datensubjekt Anforderung.
ms.openlocfilehash: 76c3ddbbd6cd7432a06506be62c63fbfa0291b46
ms.sourcegitcommit: 6b2ca6bd153d24a717d6c537efd2d41d35c20a0b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35587817"
---
# <a name="content-search-in-office-365"></a>Inhaltssuche in Office 365

Sie können das eDiscovery-Tool für die Inhaltssuche im Compliance Center in Office 365 oder Microsoft 365 verwenden, um nach in-Place-Elementen wie e-Mails, Dokumenten und Chat Unterhaltungen in Ihrer Office 365 Organisation zu suchen. Verwenden Sie dieses Tool, um nach Elementen in diesen Office 365 Diensten zu suchen:
  
- Exchange Online von Postfächern und öffentlichen Ordnern
    
- SharePoint Online von Websites und OneDrive für Unternehmen Konten
    
- Skype for Business Unterhaltungen
    
- Microsoft Teams 
    
- Office 365-Gruppen
    
Nachdem Sie eine Inhaltssuche ausgeführt haben, werden die Anzahl der inhaltsspeicherorte und eine geschätzte Anzahl von Suchergebnissen im Suchprofil angezeigt. Sie können auch schnell Statistiken anzeigen, beispielsweise die inhaltsspeicherorte mit den meisten Elementen, die mit der Suchabfrage übereinstimmen. Nachdem Sie eine Suche ausgeführt haben, können Sie eine Vorschau der Ergebnisse anzeigen oder Sie auf einen lokalen Computer exportieren.

## <a name="create-a-search"></a>Create a search

Um Zugriff auf die Seite für die **Inhaltssuche** zu haben, um Suchergebnisse auszuführen und in der Vorschau anzuzeigen und zu exportieren, müssen ein Administrator, ein Compliance Officer oder ein eDiscovery-Manager Mitglied der Rollengruppe "eDiscovery-Manager" im Security #a0 Compliance Center sein. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen](assign-ediscovery-permissions.md).
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrer Office 365-e-Mail-Adresse und Ihrem Kennwort an.
    
2. Klicken Sie auf **Such** \> **Inhaltssuche**.
    
3. Klicken Sie auf der Seite **Suchen** auf den Pfeil neben ![Symbol](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **neue Suche**hinzufügen. 
    
    ![Die neue Suchdropdownliste](media/76b25861-55c5-4f50-9d48-9e2be2d0d078.png)
  
    Verwenden Sie die Registerkarte Interne DNS-Lookups, um festzulegen, ob die DNS-Server verwendet werden sollen, die für einen auf diesem Server installierten Netzadapter konfiguriert sind, oder ob beim Auflösen der Adressen von E-Mail-Servern für die interne Nachrichtenzustellung bestimmte DNS-Server verwendet werden sollen. Interne DNS-Server werden zum Auflösen von IP-Adressen für Server innerhalb der Organisation verwendet.
    
    - * * Geführte Suche – mit dieser Option wird ein Assistent gestartet, der Sie durch das Erstellen der Suche führt. Die Benutzeroberfläche zum Auswählen von Inhaltsspeicherorten und zum Erstellen der Suchabfrage ist identisch mit der **neuen Such** Option. 
    
    - **Neue Suche** – diese Option zeigt eine aktualisierte Benutzeroberfläche zum Erstellen einer Suche an. Dies ist die Standardoption, wenn Sie auf **neue Suche**klicken.
    
    - **Suche nach ID-Liste** – mit dieser Option können Sie mithilfe einer Liste von Exchange-IDs nach bestimmten e-Mail-Nachrichten und anderen Postfachelementen suchen. Zum Erstellen einer ID-Listensuche (formell als gezielte Suche bezeichnet) senden Sie eine CSV-Datei (Comma-Separated Value), die die zu suchenden Postfachelemente identifiziert. Anweisungen finden Sie unter [Vorbereiten einer CSV-Datei für eine ID-Listeninhalts Suche in Office 365](csv-file-for-an-id-list-content-search.md).
    
    Die restlichen Schritte in diesem Verfahren folgen dem standardmäßigen neuen Such Workflow.
    
4. Klicken Sie in der Dropdownliste auf **neue Suche** . 
    
5. Geben Sie unter **Suchabfrage**die folgenden Schritte an:
    
    ![Angeben von Stichwörtern, Bedingungen und Speicherorten für die Suche](media/1e6de9dd-eac9-4e2a-819d-9740cf6c9106.png)
  
   - **Schlüsselwörter für die Suche** – geben Sie eine Suchabfrage in das Feld **Schlüsselwörter** ein. Sie können Schlüsselwörter, Nachrichteneigenschaften , z. B. Sende- und Empfangsdatum, oder Dokumenteigenschaften angeben, z. B. Dateinamen oder das Datum der letzten Dokumentänderung. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**. Sie können auch nach vertraulichen Informationen (wie etwa Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Feld Schlüsselwort leer lassen, sind alle Inhalte, die sich an den angegebenen Inhaltsspeicherorten befinden, in den Suchergebnissen enthalten.
    
      Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** und in jede Zeile ein Schlüsselwort eingeben. Wenn Sie dies tun, werden die Schlüsselwörter für jede Zeile durch einen logischen Operator (**c:s**) verbunden, der in der Funktionalität des **or** -Operators in der erstellten Suchabfrage ähnelt. 
    
      Gründe für die Verwendung der Stichwortliste Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit den einzelnen Schlüsselwörtern übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Stichwörter am häufigsten (und am wenigsten) effektiv sind. Sie können auch eine Stichwort Phrase (umgeben von Klammern) in einer Zeile verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [Anzeigen von Keyword-Statistiken für Inhalts Suchergebnisse](view-keyword-statistics-for-content-search.md).

     > [!NOTE]
     > Um Probleme aufgrund großer Stichwortlisten zu verringern, sind Sie jetzt auf maximal 20 Zeilen in der Schlüsselwortliste eingeschränkt.
    
    - **Bedingungen** – Sie können Suchbedingungen hinzufügen, um eine Suche einzugrenzen und eine verfeinerte Ergebnismenge zurückzugeben. Jede Bedingung fügt der Suchabfrage, die erstellt und ausgeführt wird, eine Klausel hinzu, wenn Sie die Suche starten. Eine Bedingung ist logisch mit der Stichwortabfrage (im Feld Schlüsselwort angegeben) durch einen logischen Operator (**c:c**) verbunden, der in der Funktionalität des **and-** Operators ähnelt. Das bedeutet, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in den Ergebnissen enthalten sein sollen. Auf diese Weise können Sie Ihre Ergebnisse mit Bedingungen eingrenzen. Eine Liste und eine Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md#search-conditions).
    
       - **Standorte** – wählen Sie die zu durchsuchenden inhaltsspeicherorte aus.
    
      - **Alle Standorte** – verwenden Sie diese Option, um alle inhaltsspeicherorte in Ihrer Organisation zu durchsuchen. Dies umfasst e-Mails in allen Exchange-Postfächern (einschließlich aller inaktiven Postfächer, Postfächer für alle Office 365 Gruppen, Postfächer für alle Microsoft Teams), alle Skype for Business Unterhaltungen, alle SharePoint-und OneDrive für Unternehmen Websites (einschließlich der Websites für alle Office 365 Gruppen und Microsoft Teams) und Elemente in allen öffentlichen Exchange-Ordnern.
    
      - **Bestimmte Standorte** – verwenden Sie diese Option, um bestimmte inhaltsspeicherorte zu durchsuchen. Sie können alle inhaltsspeicherorte nach einem bestimmten Office 365 Dienst durchsuchen (beispielsweisedurch Suchen aller Exchange-Postfächer oder Durchsuchen aller SharePoint-Websites), oder Sie können bestimmte Orte in einem der angezeigten Office 365 Dienste durchsuchen. 
    
        ![Benutzeroberfläche zum Auswählen von Inhaltsspeicherorten für die Suche](media/9a09708b-f8a2-4382-8c4e-2c610ec33c72.png)
  
         Sie können auch Verteilergruppen zur Liste der zu durchsuchenden Exchange-Postfächer hinzufügen. Für Verteilergruppen werden die Postfächer von Gruppenmitgliedern durchsucht. Dynamische Verteilergruppen werden nicht unterstützt.
    
       > [!NOTE]
       > Wenn Sie alle Postfachspeicher Orte oder nur bestimmte Postfächer durchsuchen, werden Daten aus anderen Office 365-Anwendungen, die in Benutzerpostfächern gespeichert sind, beim Exportieren der Ergebnisse einer Inhaltssuche einbezogen. Diese Daten werden nicht in die geschätzten Suchergebnisse aufgenommen und stehen nicht für die Vorschau zur Verfügung. Es ist enthalten, wenn Sie die Suchergebnisse exportieren und herunterladen. Weitere Informationen finden Sie unter [in Exchange Online Postfächern gespeicherte Inhalte](what-is-stored-in-exo-mailbox.md).

    
6. Nachdem Sie Ihre Suchabfrage eingerichtet haben, klicken Sie auf **#a0 ausführen speichern**.
    
7. Geben Sie auf der Seite **Suche speichern** einen Namen für die Suche und eine optionale Beschreibung ein, mit der die Suche identifiziert werden kann. Der Name der Suche muss in Ihrer Organisation eindeutig sein. 
    
8. Klicken Sie auf **Speichern** , um die Suche zu starten. 
    
    Nachdem Sie die Suche gespeichert und ausgeführt haben, werden alle Ergebnisse, die von der Suche zurückgegeben werden, im Ergebnisbereich angezeigt. Je nachdem, wie Sie die Vorschau Einstellung konfiguriert haben, werden die Suchergebnisse angezeigt, oder Sie müssen auf **Ergebnisse der Vorschau** klicken, um Sie anzuzeigen. Weitere Informationen finden Sie im nächsten Abschnitt. 
    
Um erneut auf diese Inhaltssuche zuzugreifen oder auf andere auf der Seite **Inhaltssuche** aufgeführte Inhalts suchen zuzugreifen, wählen Sie die Suche aus, und klicken Sie dann auf **Öffnen**. 
  
Klicken Sie ![auf Symbol "](media/O365-MDM-CreatePolicy-AddIcon.gif) **neue Suche**hinzufügen", um die Ergebnisse zu löschen oder eine weitere Suche zu erstellen. 

  
## <a name="preview-search-results"></a>Suchergebnisse in der Vorschau anzeigen

Es gibt zwei Konfigurationseinstellungen für die Vorschau von Suchergebnissen. Nachdem Sie eine neue Suche durchgeführt oder eine vorhandene Suche geöffnet haben, klicken Sie auf * * einzelne Ergebnisse * *, um die folgenden Vorschaueinstellungen anzuzeigen: 
  
![Vorschau der Suchergebnis Einstellungen](media/83519477-1c85-4442-8886-481f186fd758.png)
  
1. **Automatische Vorschau der Ergebnisse** – diese Einstellung zeigt die Suchergebnisse nach dem Ausführen einer Suche an.
    
2. **Ergebnisse in der Vorschau manuell** anzeigen – mit dieser Einstellung werden Platzhalter im Suchergebnisbereich angezeigt, und die Schaltfläche **Vorschau Ergebnisse** wird angezeigt, auf die Sie klicken müssen, um die Suchergebnisse anzuzeigen. Dies ist die Standardeinstellung. Es hilft bei der Verbesserung der Suchleistung, indem nicht automatisch die Suchergebnisse angezeigt werden, wenn Sie eine vorhandene Suche öffnen. 
    
Es gibt Grenzen im Zusammenhang mit der Anzahl der verfügbaren Elemente für eine Vorschau. Weitere Informationen finden Sie unter [Grenzwerte für die Inhaltssuche](limits-for-content-search.md). 
  
Eine Liste der unterstützten Dateitypen, die in der Vorschau angezeigt werden können, finden Sie unter [Vorschau der Suchergebnisse](#previewing-search-results) im Abschnitt "Weitere Informationen zur Inhaltssuche". Wenn ein Dateityp nicht für die Vorschau oder zum Herunterladen einer Kopie eines Dokuments unterstützt wird, können Sie auf **ursprüngliche Datei herunterladen** klicken, um Sie auf den lokalen Computer herunterzuladen. Für aspx-Webseiten ist die URL für die Seite enthalten, obwohl Sie möglicherweise nicht über Berechtigungen für den Zugriff auf die Seite verfügen. 
  
Beachten Sie auch, dass nicht indizierte Elemente für die Vorschau nicht verfügbar sind.
  
## <a name="view-information-and-statistics-about-a-search"></a>Anzeigen von Informationen und Statistiken zu einer Suche

Nachdem Sie eine Inhaltssuche erstellt und ausgeführt haben, können Sie Statistiken zu den geschätzten Suchergebnissen anzeigen. Dies umfasst eine Zusammenfassung der Suchergebnisse, die Abfragestatistiken wie die Anzahl der inhaltsspeicherorte mit Elementen, die mit der Suchabfrage übereinstimmen, und den Namen der inhaltsspeicherorte mit den am besten übereinstimmenden Elementen. Sie können Statistiken für eine oder mehrere Inhalts suchen anzeigen. Auf diese Weise können Sie die Ergebnisse für mehrere Suchvorgänge schnell vergleichen und Entscheidungen hinsichtlich der Effektivität ihrer Suchabfragen treffen.
  
Sie können auch die Suchstatistik und die Keyword-Statistik in eine CSV-Datei herunterladen. Auf diese Weise können Sie die Filter-und Sortierfunktionen in Excel verwenden, um Ergebnisse zu vergleichen und Berichte für Ihre Suchergebnisse vorzubereiten.
  
So zeigen Sie Suchstatistiken an:
  
1. Klicken Sie auf der Seite **Inhaltssuche** auf **Öffnen** , und klicken Sie dann auf die Suche, für die Sie die Statistik anzeigen möchten. 
    
2. Klicken Sie auf der Seite Flyout auf **Abfrage öffnen**. 
    
3. Klicken Sie in der Dropdownliste **einzelne Ergebnisse** auf **Suchprofil**.
    
4. Klicken Sie in der Dropdownliste **Typ** auf eine der folgenden Optionen, abhängig von den Suchstatistiken, die Sie anzeigen möchten. 
    
  - **Zusammenfassung** – zeigt Statistiken für jeden Typ von durchsuchten Inhaltsspeicherorten an. Dadurch wird die Anzahl der inhaltsspeicherorte, die Elemente enthalten, die mit der Suchabfrage übereinstimmen, sowie die Gesamtanzahl und Größe der Suchergebnis Elemente Inhalt. Dies ist die Standardeinstellung.
    
  - **Abfragen** – zeigt Statistiken zur Suchabfrage an. Dies umfasst den Typ des Inhaltsspeichers, auf den die Abfragestatistik angewendet wird, einen Teil der Suchabfrage, auf den die Statistik **** anwendbar ist (Beachten Sie, dass Primary die gesamte Suchabfrage angibt), die Anzahl der inhaltsspeicherorte, die Elemente enthalten, die entsprechen der Suchabfrage und der Gesamtzahl und-Größe und den Elementen, die gefunden wurden (am angegebenen Inhaltsspeicherort), die der Suchabfrage entsprechen. Statistiken für nicht indexierte Elemente (auch als *teilweise indizierte Elemente*bezeichnet) werden ebenfalls angezeigt. Die Statistik enthält jedoch nur teilweise indizierte Elemente aus Postfächern. Teilweise indizierte Elemente aus SharePoint und OneDrive sind nicht in den Statistiken enthalten.
    
  - **Top-Standorte** – zeigt Statistiken zur Anzahl der Elemente an, die mit der Suchabfrage in jedem Inhaltsspeicherort übereinstimmen. Die oberen 1.000-Speicherorte werden angezeigt.
    
Ausführlichere Informationen zu Suchstatistiken finden Sie unter [Anzeigen von Keyword-Statistiken für Inhalts Suchergebnisse](view-keyword-statistics-for-content-search.md).
  
  
## <a name="export-search-results"></a>Exportieren der Suchergebnisse

Nachdem eine Suche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse auf einen lokalen Computer exportieren. Wenn Sie e-Mail-Ergebnisse exportieren, können Sie Sie als PST-Dateien oder als einzelne Nachrichten (msg-Dateien) auf Ihren Computer herunterladen. Wenn Sie Inhalte aus SharePoint-und OneDrive-Websites exportieren, werden Kopien von systemeigenen Office-Dokumenten exportiert. Es gibt auch andere Dokumente und Berichte, die in den exportierten Suchergebnissen enthalten sind. Sie können auch den Suchergebnisbericht und nicht die tatsächlichen Elemente exportieren.
  
So exportieren Sie Suchergebnisse:
  
1. Klicken Sie auf der Seite **Inhaltssuche** auf die Suche, für die Sie die Suchergebnisse exportieren möchten. 
    
2. ![Klicken Sie auf der Seite Flyout auf Suchergebnisse](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **** exportieren, und klicken Sie dann auf **Ergebnisse exportieren**. Sie können auch einen Suchergebnisbericht exportieren.
    
3. Füllen Sie die Abschnitte auf der Seite **Export results** Fly Out aus. Stellen Sie sicher, dass Sie die Bildlaufleiste verwenden, um alle Exportoptionen anzuzeigen. 
    
Ausführlichere Anweisungen und Tipps zur Problembehandlung finden Sie unter:
  
- [Exportieren von Inhaltssuchergebnissen ](export-search-results.md)
    
- [Exportieren eines Inhaltssuchberichts](export-a-content-search-report.md)
    
  
## <a name="more-information-about-content-search"></a>Weitere Informationen zur Inhaltssuche

In den folgenden Abschnitten finden Sie weitere Informationen zu Inhalts suchen.
  
[Grenzwerte für die Inhaltssuche](#content-search-limits)
  
[Erstellen einer Suchabfrage](#building-a-search-query)
  
[Durchsuchen von OneDrive-Konten](#searching-onedrive-accounts)
  
[Durchsuchen von Microsoft Teams und Office 365 Gruppen](#searching-microsoft-teams-and-office-365-groups)
  
[Durchsuchen inaktiver Postfächer](#searching-inactive-mailboxes)
  
[Anzeigen einer Vorschau der Suchergebnisse](#previewing-search-results)
  
[Teilweise indizierte Elemente](#partially-indexed-items)
  
### <a name="content-search-limits"></a>Grenzwerte für die Inhaltssuche

- Eine Beschreibung der Grenzwerte, die auf das Feature für die Inhaltssuche angewendet werden, finden Sie unter [Grenzwerte für die Inhaltssuche](limits-for-content-search.md).
    
- Microsoft sammelt Leistungsinformationen für Inhalts suchen, die von allen Office 365 Organisationen ausgeführt werden. Während sich die Komplexität der Suchabfrage auf die Suchzeiten auswirken kann, ist der größte Faktor, der sich auf die Dauer der Suche auswirkt, die Anzahl der durchsuchten Postfächer. Obwohl Microsoft keine Vereinbarung zum Service Level für Suchzeiten bereitstellt, werden in der folgenden Tabelle die durchschnittlichen Suchzeiten für eine Inhaltssuche basierend auf der Anzahl der in der Suche enthaltenen Postfächer aufgeführt.
    
|**Anzahl der Postfächer**|**Durchschnittliche Such Dauer**|
|:-----|:-----|
|100  <br/> |30 Sekunden  <br/> |
|1,000  <br/> |45 Sekunden  <br/> |
|10,000  <br/> |4 Minuten  <br/> |
|25.000  <br/> |10 Minuten  <br/> |
|50.000  <br/> |20 Minuten  <br/> |
|100,000  <br/> |25 Minuten  <br/> |
  
### <a name="building-a-search-query"></a>Erstellen einer Suchabfrage

Ausführliche Informationen zum Erstellen einer Suchabfrage mithilfe von booleschen Suchoperatoren und Suchbedingungen sowie zum Suchen nach vertraulichen Informationstypen und Inhalten, die für Benutzer außerhalb Ihrer Organisation freigegeben wurden, finden Sie unter [Keyword-Abfragen und Suchbedingungen. für die Inhaltssuche ](keyword-queries-and-search-conditions.md).
  
Beachten Sie beim Erstellen einer Suchabfrage die folgenden Punkte, wenn Sie die Stichwortliste verwenden.
  
- Sie müssen das Kontrollkästchen **Keyword-Liste anzeigen** aktivieren und dann jedes Schlüsselwort in eine separate Zeile eingeben, um eine Suchabfrage zu erstellen, bei der die Schlüsselwörter (oder Keyword-Phrasen) in jeder Zeile durch den **or** -Operator miteinander verbunden sind. Wenn Sie eine Liste von Schlüsselwörtern in das Feld Stichwort einfügen oder die **Eingabe** Taste drücken, nachdem Sie ein Stichwort eingegeben haben, wird Sie nicht durch den Operator **oder** verbunden. Hier sind falsche und richtige Beispiele dafür, wie Sie eine Liste von Schlüsselwörtern hinzufügen. 
    
    **Falsche**
    
    ![Falsche Vorgehensweise zum Formatieren einer Keyword-Liste (durch Einfügen der Liste in das Feld "Stichwort")](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Richtig**
    
    ![Die richtige Möglichkeit zum Formatieren einer Keyword-Liste (durch Markieren von CheckBox und Einfügen der Liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
- Sie können auch eine Liste von Schlüsselwörtern oder Keyword-Phrasen in einer Excel-Datei oder einer nur-Text-Datei vorbereiten und dann die Liste kopieren und in die Stichwortliste einfügen. Dazu müssen Sie das Kontrollkästchen **Schlüsselwortliste anzeigen** aktivieren. Klicken Sie dann in der Liste Stichwort auf die erste Zeile, und fügen Sie Ihre Liste ein. Jede Zeile aus der Excel-oder Textdatei wird in eine separate Zeile in der Schlüsselwortliste eingefügt. 
    
- Nachdem Sie eine Abfrage mithilfe der Stichwortliste erstellt haben, empfiehlt es sich, die Suchabfrage Syntax zu überprüfen, um die beabsichtigte Suchabfrage zu erstellen. In der Suchabfrage, die unter **Query** im Detailbereich angezeigt wird, werden die Schlüsselwörter durch den Text **(c:s)** getrennt. Dies deutet darauf hin, dass die Schlüsselwörter durch einen logischen Operator mit ähnlicher Funktionalität wie der Operator **or** verbunden sind. Wenn Ihre Suchabfrage Bedingungen enthält, werden die Schlüsselwörter und Bedingungen entsprechend durch den Text **(c:c)** getrennt. Dies deutet darauf hin, dass die Schlüsselwörter mit den Bedingungen verbunden sind, die einen logischen Operator aufweisen, der in der Funktionalität des **and-** Operators ähnelt. Im folgenden finden Sie ein Beispiel für die Suchabfrage (die im Detailbereich angezeigt wird), die bei Verwendung der Stichwortliste und einer Bedingung resultiert. 
    
    ![Beispiel für die Abfrage, die erstellt wird, wenn die Stichwortliste verwendet wird und eine Bedingung](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
- Wenn Sie eine Inhaltssuche ausführen, überprüft Office 365 Ihre Suchabfrage automatisch auf nicht unterstützte Zeichen und auf boolesche Operatoren, die möglicherweise nicht groß geschrieben werden. Nicht unterstützte Zeichen werden häufig ausgeblendet und verursachen in der Regel einen Suchfehler oder geben unbeabsichtigte Ergebnisse zurück. Weitere Informationen zu den nicht unterstützten Zeichen, die überprüft werden, finden Sie unter [Überprüfen der Inhalts Suchabfrage auf Fehler](check-your-content-search-query-for-errors.md).
    
- Wenn Sie über eine Suchabfrage verfügen, die Stichwörter für nicht englische Zeichen enthält (beispielsweise chinesische Zeichen), können Sie in der Inhaltssuche](media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) auf **Abfragesprache – Land/Region**![-Abfragesprache – Land/Regions Symbol klicken und dann eine Language-Country-Kultur Codewert für die Suche. Die Standardsprache/Region ist neutral. Wie können Sie erkennen, ob Sie die Spracheinstellung für eine Inhaltssuche ändern müssen? Wenn Sie bestimmte inhaltsspeicherorte enthalten, die nicht englische Zeichen sind, die Sie suchen, aber die Suche keine Ergebnisse zurückgibt, ist die Spracheinstellung möglicherweise die Ursache. 
  
### <a name="searching-onedrive-accounts"></a>Durchsuchen von OneDrive-Konten

- Informationen zum Erfassen einer Liste der URLs für die OneDrive-Websites in Ihrer Organisation finden Sie unter [Erstellen einer Liste aller OneDrive-Standorte in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Dieses Skript in diesem Artikel erstellt eine Textdatei, die eine Liste aller OneDrive-Websites enthält. Um dieses Skript auszuführen, müssen Sie die SharePoint Online-Verwaltungsshell installieren und verwenden. Stellen Sie sicher, dass Sie die URL für die mysite-Domäne Ihrer Organisation an jede OneDrive-Website anfügen, die Sie durchsuchen möchten. Dies ist die Domäne, die alle OneDrive enthält. Beispiel: `https://contoso-my.sharepoint.com`. Hier ist ein Beispiel für eine URL für die OneDrive-Website eines Benutzers `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`:.
    
    Im seltenen Fall, dass der Benutzerprinzipalname (UPN) einer Person geändert wird, wird die URL für den OneDrive-Speicherort geändert, sodass der neue UPN integriert wird. In diesem Fall müssen Sie eine Inhaltssuche ändern, indem Sie die neue OneDrive-URL des Benutzers hinzufügen und die alte entfernen.
  
### <a name="searching-microsoft-teams-and-office-365-groups"></a>Durchsuchen von Microsoft Teams und Office 365 Gruppen

Sie können das Postfach durchsuchen, das einer Office 365 Gruppe oder einem Microsoft-Team zugeordnet ist. Da Microsoft Teams auf Office 365 Gruppen aufbaut, ist die Suche ähnlich. In beiden Fällen wird nur das Gruppen-oder Team Postfach durchsucht. Die Postfächer der Gruppe oder der Teammitglieder werden nicht durchsucht. Um Sie durchsuchen zu können, müssen Sie Sie explizit der Suche hinzufügen.
  
Beachten Sie bei der Suche nach Inhalten in Microsoft Teams und Office 365 Gruppen die folgenden Punkte.
  
- Um nach Inhalten zu suchen, die sich in Teams und Office 365 Gruppen befinden, müssen Sie das Postfach und die SharePoint-Website angeben, die einem Team oder einer Gruppe zugeordnet sind.
    
- Führen Sie das Cmdlet **Get-Unifiedgroup** in Exchange Online aus, um Eigenschaften für ein Team oder eine Office 365 Gruppe anzuzeigen. Dies ist eine gute Möglichkeit, die URL für die Website abzurufen, die einem Team oder einer Gruppe zugeordnet ist. Mit dem folgenden Befehl werden beispielsweise ausgewählte Eigenschaften für eine Office 365 Gruppe mit dem Namen "Senior Leadership Team" angezeigt: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Damit Sie das Cmdlet **Get-Unifiedgroup** ausführen können, müssen Sie in Exchange Online die Rolle "nur-Ansicht-Empfänger" besitzen oder Mitglied einer Rollengruppe sein, der die Rolle "nur-Empfänger" zugewiesen ist. 
  
- Wenn das Postfach eines Benutzers durchsucht wird, werden alle Teams oder Office 365 Gruppen, in denen der Benutzer Mitglied ist, nicht durchsucht. Wenn Sie ein Team oder eine Office 365 Gruppe durchsuchen, wird auf ähnliche Weise nur das Gruppenpostfach und die von Ihnen angegebene Gruppen Website durchsucht. Die Postfächer und OneDrive für Unternehmen Konten von Gruppenmitgliedern werden nur durchsucht, wenn Sie Sie explizit der Suche hinzugefügt haben.
    
- Wenn Sie eine Liste der Mitglieder eines Teams oder einer Office 365 Gruppe erhalten möchten, können Sie die Eigenschaften auf der Seite **" \> Startgruppen** " im Microsoft 365 Admin Center anzeigen. Alternativ können Sie den folgenden Befehl in Exchange Online PowerShell ausführen: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Damit Sie das Cmdlet **Get-UnifiedGroupLinks** ausführen können, müssen Sie in Exchange Online die Rolle "nur-Ansicht-Empfänger" besitzen oder Mitglied einer Rollengruppe sein, der die Rolle "nur-Ansicht-Empfänger" zugewiesen ist. 
  
- Unterhaltungen, die Teil eines Teams-Kanals sind, werden in dem Postfach gespeichert, das dem Team zugeordnet ist. Auf ähnliche Weise werden Dateien, die Teammitglieder in einem Kanal freigeben, auf der SharePoint-Website des Teams gespeichert. Daher müssen Sie das Team Postfach und die SharePoint-Website als Inhaltsspeicherort hinzufügen, um Unterhaltungen und Dateien in einem Kanal zu durchsuchen.
    
- Alternativ werden Unterhaltungen, die Teil der Chat Liste in Microsoft Teams sind, im Exchange Online Postfach der Benutzer gespeichert, die an dem Chat teilnehmen. Und Dateien, die ein Benutzer in Chat Unterhaltungen freigibt, werden im OneDrive für Unternehmen Konto des Benutzers gespeichert, der die Datei freigibt. Daher müssen Sie die einzelnen Benutzerpostfächer und OneDrive für Unternehmen Konten als inhaltsspeicherorte hinzufügen, um Unterhaltungen und Dateien in der Chat Liste zu durchsuchen.
    
    > [!NOTE]
    > In einer Exchange-hybridbereitstellung können Benutzer mit einem lokalen Postfach an Unterhaltungen teilnehmen, die Teil der Chat Liste in Microsoft Teams sind. In diesem Fall können Inhalte aus diesen Unterhaltungen auch durchsuchbar sein, da Sie in einem cloudbasierten Speicherbereich (als *Cloud-basiertes Postfach für lokale Benutzer*) für Benutzer mit einem lokalen Postfach gespeichert werden. Weitere Informationen finden Sie unter [searching Cloud-based Mailboxes for on-premises users in Office 365](search-cloud-based-mailboxes-for-on-premises-users.md).
  
- Jeder Kanal für Teams oder Teams enthält ein wiki für die Notizen und die Zusammenarbeit. Der Inhalt des Wikis wird automatisch in einer Datei mit dem MHT-Format gespeichert. Diese Datei wird in der Microsoft Teams-wiki-Datendokument Bibliothek auf der SharePoint-Website des Teams gespeichert. Sie können das Inhaltssuche-Tool zum Durchsuchen des Wikis verwenden, indem Sie die SharePoint-Website des Teams als den zu durchsuchenden Inhaltsspeicherort angeben. 
    
    > [!NOTE]
    > Die Funktion zum Durchsuchen des Wikis für ein Team oder einen Kanal (wenn Sie die SharePoint-Website des Teams durchsuchen) wurde am 22. Juni 2017 veröffentlicht. Wiki-Seiten, die an diesem Datum oder später gespeichert oder aktualisiert wurden, stehen für die Durchsuchung zur Verfügung. Wiki-Seiten, die zuletzt gespeichert oder vor diesem Datum aktualisiert wurden, stehen nicht für die Suche zur Verfügung. 
 
- Zusammenfassende Informationen für Besprechungen und Anrufe in einem Teams-Kanal werden auch in den Postfächern von Benutzern gespeichert, die sich in die Besprechung oder den Anruf eingewählt haben. Dies bedeutet, dass Sie die Inhaltssuche zum Durchsuchen dieser zusammenfassungsdatensätze verwenden können. Zu den zusammenfassenden Informationen gehören: 
  
  - Datum, Anfangszeit, Endzeit und Dauer einer Besprechung oder eines Anrufs

  - Das Datum und die Uhrzeit, zu denen jeder Teilnehmer der Besprechung oder dem Anruf beigetreten ist oder ihn verlassen hat

  - An Voice Mail gesendete Anrufe

  - Verpasste oder nicht beantwortete Anrufe

  - Anruf Übertragungen, die als zwei getrennte Anrufe dargestellt werden

  Es kann bis zu 8 Stunden dauern, bis Besprechungs-und Anruf Zusammenfassungen zur Verfügung stehen, um durchsucht zu werden.

  In den Suchergebnissen werden Besprechungs Zusammenfassungen als **Besprechung** im **Feld Typ**identifiziert, und Anruf Zusammenfassungen werden als **Anruf**identifiziert. Außerdem werden Unterhaltungen, die Teil eines Teams-Kanals und 1xN-Chats sind, als im Feld **Typ** als **im** angegeben.
  
  ![Microsoft Teams-Besprechungen, Anrufe und 1xN-Chats werden im Feld Typ identifiziert.](media/O365-ContentSearch-Teams-MessageKind.png)

- Sie können die **Art** -e-Mail-Eigenschaft oder die **Nachrichtenart** -Suchbedingung verwenden, um gezielt nach Inhalten in Microsoft Teams zu suchen. 
  
  - Um die **Kind** -Eigenschaft als Teil der Stichwort Suchabfrage zu verwenden, geben `kind:microsoftteams`Sie im Feld **Schlüsselwörter** einer Suchabfrage ein.

    ![Verwenden Sie die Art: verläuft im Feld Schlüsselwörter](media/O365-ContentSearch-Teams-Keywords.png)
  
  - Um eine Suchbedingung zu verwenden, fügen **** Sie die Nachrichtenart Bedingung hinzu und `microsoftteams`verwenden Sie den Wert. 

    ![Verwenden Sie die Meldung Kind Condition mit dem Wert verläuft.](media/O365-ContentSearch-Teams-MessageKindCondition.png)

Beachten Sie, dass Bedingungen durch den **and-** Operator logisch mit der Stichwortabfrage verbunden sind. Das bedeutet, dass ein Element sowohl mit der Stichwortabfrage als auch mit der Suchbedingung übereinstimmen muss, die in den Suchergebnissen zurückgegeben werden soll. Weitere Informationen finden Sie im Abschnitt "Richtlinien für die Verwendung von Bedingungen" unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche.](keyword-queries-and-search-conditions.md#guidelines-for-using-conditions)

  
### <a name="searching-inactive-mailboxes"></a>Durchsuchen inaktiver Postfächer

Sie können inaktive Postfächer in einer Inhaltssuche durchsuchen. Um eine Liste der inaktiven Postfächer in Ihrer Organisation abzurufen, führen `Get-Mailbox -InactiveMailboxOnly` Sie den Befehl in Exchange Online PowerShell aus. Alternativ können Sie im Security #a0 Compliance Center zur **Aufbewahrung** von **Datenverwaltung** \> wechseln und dann auf **Weitere**![Navigationsleiste Ellipsen](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **inaktive Postfächer**klicken.
  
Im folgenden finden Sie einige Punkte, die Sie bei der Suche inaktiver Postfächer beachten sollten.
  
- Wenn eine Inhaltssuche ein Benutzerpostfach enthält und dieses Postfach dann inaktiv ist, wird die Inhaltssuche weiterhin das inaktive Postfach durchsuchen, wenn Sie die Suche erneut ausführen, nachdem Sie inaktiv geworden ist.
    
- Manchmal verfügt ein Benutzer möglicherweise über ein aktives Postfach und ein inaktives Postfach mit der gleichen SMTP-Adresse. In diesem Fall wird nur das bestimmte Postfach durchsucht, das Sie als Speicherort für eine Inhaltssuche ausgewählt haben. Wenn Sie also das Postfach eines Benutzers zu einer Suche hinzufügen, können Sie nicht davon ausgehen, dass sowohl die aktiven als auch die inaktiven Postfächer durchsucht werden. Es wird nur das Postfach durchsucht, das Sie explizit der Suche hinzugefügt haben.
    
- Es wird dringend empfohlen, ein aktives Postfach und ein inaktives Postfach mit derselben SMTP-Adresse zu vermeiden. Wenn Sie die SMTP-Adresse wieder verwenden möchten, die einem inaktiven Postfach zugewiesen ist, wird empfohlen, das inaktive Postfach wiederherzustellen oder den Inhalt eines inaktiven Postfachs in einem aktiven Postfach (oder im Archiv eines aktiven Postfachs) wiederherzustellen und dann die inaktiven Postfächer zu löschen. Postfach. Weitere Informationen finden Sie unter einem der folgenden Themen:
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md)
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md)
    
  - [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)

  
### <a name="previewing-search-results"></a>Anzeigen einer Vorschau der Suchergebnisse

Unterstützte Dateitypen können im Vorschaufenster angezeigt werden. Wenn ein Dateityp nicht unterstützt wird, müssen Sie eine Kopie der Datei auf den lokalen Computer herunterladen, um Sie anzuzeigen. Die folgenden Dateitypen werden unterstützt und können im Suchergebnisbereich als Vorschau angezeigt werden.
  
- txt, HTML, MHTML
    
- EML
    
- doc-, docx-, DOCM-
    
- . pptm,. pptx
    
- .pdf
    
Außerdem werden die folgenden Dateicontainer Typen unterstützt. Sie können die Liste der Dateien im Container im Bereich Vorschau anzeigen.
  
- . zip
    
- gzip
    
### <a name="partially-indexed-items"></a>Teilweise indizierte Elemente

- Wie bereits erläutert, sind teilweise indizierte Elemente in Postfächern in den geschätzten Suchergebnissen enthalten. Teilweise indizierte Elemente aus SharePoint und OneDrive sind nicht in den geschätzten Suchergebnissen enthalten. 
    
- Wenn ein teilweise indiziertes Element mit der Suchabfrage übereinstimmt (da andere Nachrichten-oder Dokumenteigenschaften die Suchkriterien erfüllen), ist es nicht in der geschätzten Anzahl von nicht indizierten Elementen enthalten. Wenn ein teilweise indiziertes Element durch die Suchkriterien ausgeschlossen wird, ist es nicht in der geschätzten Anzahl nicht indexierter Elemente enthalten. Weitere Informationen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md).