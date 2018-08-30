---
title: Verwalten von GDPR Daten Betreff Anfragen mit der Groß-/Kleinschreibung DSR-Tool in der Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/25/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
description: Die GDPR bietet EU-Bürger (Data Themen genannt) bestimmte Rechte auf ihre persönlichen Daten; Diese Rechte umfassen Kopien davon erhalten, Änderungen an ihn anfordern, durch die Beschränkung auf die Verarbeitung von es, löschen oder empfängt, in einem elektronischen Format. Eine formelle Anforderung von einem Daten-unterliegen Take ist eine Aktion auf ihre persönlichen Daten als Betreff der Anforderung von Daten oder die DSR bezeichnet. Sie können die DSR Fällen verwenden, in die Office 365-Sicherheit &amp; Compliance Center zum Verwalten von Ihrer Organisation DSR Untersuchungen.
ms.openlocfilehash: c8edee8d377865d46662ebbd7f18a5a6f3015192
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529549"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-office-365-security-amp-compliance-center"></a>Verwalten von GDPR Daten Betreff Anfragen mit der Groß-/Kleinschreibung DSR-Tool in der Office 365-Sicherheit &amp; Compliance Center

Der EU-allgemeine Data Protection Regulierung (GDPR) wird zum Schutz und zur Aktivierung der einzelnen Personen Privacy Rights innerhalb der Europäischen Union (EU). Die GDPR bietet Personen in der Europäischen Union bekannt (als Daten Betreffzeilen) das Recht, Zugriff, abrufen, korrigieren, löschen und Verarbeitung ihrer persönlichen Daten zu beschränken. Unter den GDPR bedeutet persönliche Daten alle Informationen über eine identifizierte oder identifizierbare natürliche Person. Eine formelle Anforderung von einer Person in ihrer Organisation eine Aktion auf ihre persönlichen Daten wird eine Anforderung zum Betreff Daten oder DSR aufgerufen. Ausführliche Informationen zu reagieren auf DSRs für Daten in Office 365 finden Sie unter [Office 365 Data Betreff anfordern Guide](https://go.microsoft.com/fwlink/?linkid=871169 ).
  
Sie können das Groß-/Kleinschreibung DSR-Tool zum Verwalten von Ermittlungen als Antwort auf eine von einer Person in Ihrer Organisation übermittelt DSR verwenden, in die Office 365-Sicherheit &amp; Compliance Center in gespeicherte Inhalte zu suchen:
  
- Kein Benutzerpostfach in Ihrer Organisation. Dazu gehören Skype für Business Unterhaltungen und 1: 1-Chats in Microsoft-Teams
    
- Alle Postfächer, die ein Office 365-Gruppe und alle Team Postfächer in Microsoft-Teams, zugeordnet
    
- Alle SharePoint Online-Websites und OneDrive for Business-Konten in Ihrer Organisation
    
- Alle Teams Websites und Office 365-Gruppe Websites in Ihrer Organisation
    
- Alle öffentlichen Ordner in Exchange Online
    
Mit der Groß-/Kleinschreibung DSR-Tool können Sie die folgenden Schritte ausführen:
  
- Erstellen Sie eine separate Anfrage für jede Untersuchung einer Anforderung einer betroffenen Person.
    
- Steuern, wer Zugriff auf die DSR Groß-/Kleinschreibung wurde durch Hinzufügen von Personen als Mitglieder der Groß-/Kleinschreibung; nur Mitglieder können zugreifen, die Groß-/Kleinschreibung und können nur auf der Seite **DSR Fällen** in das Wertpapier sehen, deren Fällen in der Liste der Fälle &amp; Compliance Center. Darüber hinaus können Sie verschiedene Member der die gleiche Groß-/Kleinschreibung unterschiedliche Berechtigungen zuweisen. Beispielsweise können Sie einige Elemente nur die Groß-/Kleinschreibung und die Suchergebnisse anzeigen und Mitgliedern erstellen gesucht und Exportieren von Suchergebnissen gestatten. 
    
- Verwenden Sie die integrierte zum Durchsuchen für alle Inhalte erstellt oder nach einem bestimmten Daten Betreff hochgeladen.
    
- Optional überarbeiten Sie die integrierten Suchabfrage, und führen Sie die Suche, um die Suchergebnisse einzuschränken erneut aus.
    
- Fügen Sie zusätzliche Content-Suche die DSR Groß-/Kleinschreibung zugeordnet. Dazu gehören erstellen suchen, die teilweise indizierte Elemente und Protokollen vom System generierte aus Meine Analytics und den Dienst für die Office-Roaming zurückgeben.
    
- Exportieren von Daten als Antwort auf eine DSR Access oder Exportieren der Anforderung.
    
- Löschen Sie Fälle, wenn die DSR Untersuchung abgeschlossen ist; Entfernt alle suchen und Exportieren Aufträge im Zusammenhang mit der Groß-/Kleinschreibung.
    
Nachfolgend finden Sie die folgenden allgemeinen Schritte für die Verwendung der Groß-/Kleinschreibung DSR-Tools zum Verwalten von DSR Untersuchungen:
  
[Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Schritt 2: Erstellen Sie einen DSR-Fall und Hinzufügen von Mitgliedern](#step-2-create-a-dsr-case-and-add-members)

[Schritt 3: Ausführen die Suchabfrage](#step-3-run-the-search-query)

[Schritt 4: Exportieren der Daten](#step-4-export-the-data)

[(Optional) Schritt 5: Überprüfen Sie die integrierten Search-Abfrage](#optional-step-5-revise-the-built-in-search-query)

[Weitere Informationen zur Verwendung der Groß-/Kleinschreibung DSR-Tools](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Unsere Tools hilft Administratoren DSR Access ausführen oder Exportieren von Anforderungen durch ermöglicht es ihnen, die integrierte Suche nutzen und exportieren die Groß-/Kleinschreibung DSR-Tool-Funktionalität. Das Tool erleichtert vereinfachen eine Best-Effort-Methode zum Exportieren von Daten, die auf eine DSR-Anforderung nach einem Betreff Daten übermittelt relevant sind. Jedoch ist es wichtig, beachten Sie, dass die Suchergebnisse variieren können auf der Grundlage der betroffenen Person oder die Admin-Aktionen, können die beeinträchtigen, unabhängig davon, ob ein Element als "Persönliche Daten" für den Export auszugehen würde. Wenn die betroffenen Person die letzte Person so ändern Sie eine Datei wurde sie nicht selbst erstellt, die Datei kann nicht in den Suchergebnissen zurückgegeben werden. In ähnlicher Weise kann ein Administrator Daten ohne einschließlich teilweise indizierte Elemente oder alle Versionen von SharePoint-Dokumente exportieren. Aus diesem Grund können die bereitgestellten Tools erleichtern den Zugriff auf und Exportieren von Daten Anforderungen; bestimmte Admin und Daten Betreff Verwendungsszenarien jedoch unterliegen die Ergebnisse. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern

Standardmäßig kann ein globaler Office 365-Administrator das Groß-/Kleinschreibung DSR-Tool in das Wertpapier zugreifen &amp; Compliance Center. Durch entwerfen, anderer Benutzer wie Daten Privacy Officer, ein Personalwesen-Manager oder andere Personen beteiligt DSR Untersuchungen keinen Zugriff auf die Groß-/Kleinschreibung DSR-Tool und weist das Tool Zugriff auf die entsprechenden Berechtigungen zugewiesen werden soll. Die einfachste Möglichkeit hierzu ist, fahren Sie mit der Seite **Berechtigungen** in das Wertpapier &amp; Compliance Center und Hinzufügen von Benutzern zur Rollengruppe eDiscovery-Manager. Beachten Sie, dass Sie auch diese Berechtigungen zuweisen, damit Sie sie als Mitglieder der Anfrage DSR hinzufügen können, die in Schritt2 erstellt haben. 
  
Schrittweise Anweisungen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
  
> [!NOTE]
> Standardmäßig ist ein globaler Office 365-Administrator (oder andere Mitglieder der Rollengruppe "Organisationsverwaltung" in das Wertpapier &amp; Compliance Center haben nicht die erforderlichen Berechtigungen zum Exportieren von Suchergebnissen (siehe Schritt 4 in diesem Artikel). Dieses Problem umgehen, kann ein Administrator sich selbst als Mitglied der Gruppe der eDiscovery-Manager-Rolle hinzufügen. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Schritt 2: Erstellen Sie einen DSR-Fall und Hinzufügen von Mitgliedern

Im nächste Schritt wird eine DSR-Anfrage zu erstellen. Wenn Sie einen Fall erstellen, Sie können auch die integrierte Suche zu starten, oder können Sie die Groß-/Kleinschreibung erstellen, ohne die Suche beginnen. Das folgende Verfahren wird weisen Sie die Groß-/Kleinschreibung zu erstellen, ohne die Suche beginnen und wird gezeigt, wie die Groß-/Kleinschreibung Mitglieder hinzugefügt.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365. 
    
2. In das Wertpapier &amp; Compliance Center, klicken Sie auf **den Datenschutz** \> **Daten Subject-Anforderungen**, und klicken Sie dann auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **neue DSR Groß-/Kleinschreibung**.
    
3. Benennen Sie auf der Seite **neue DSR Groß-/Kleinschreibung** flyoutmenü der Groß-/Kleinschreibung, geben Sie eine optionale Beschreibung ein, und klicken Sie dann auf **Weiter**. Beachten Sie, dass der Name der Anfrage in Ihrer Organisation eindeutig sein muss.
    
    > [!TIP]
    > Sollten Sie den Namen der Person ein, die die DSR-Anforderung gesendet, die Sie in den Namen untersuchen sind und/oder Beschreibung der neuen Anfrage hinzufügen. Beachten Sie, dass nur Mitglieder der in diesem Fall (und eDiscovery-Administratoren) die Groß-/Kleinschreibung in der Liste der Anfragen auf der Seite **Daten Betreff Anfragen** angezeigt werden. 
  
4. Wählen Sie auf der Seite **Details der Anforderung** unter **Daten Betreff (die Person, die diese Anforderung eingereicht)** die Person, die Sie verwenden möchten, suchen und Exportieren von Daten für, und klicken Sie dann auf **Weiter**.
    
5. Auf der Seite **bestätigen Sie die Groß-/Kleinschreibung Einstellungen** Sie ändern der Groß-/Kleinschreibung Namen und eine Beschreibung, und wählen Sie einen Betreff für andere Daten. Andernfalls, klicken Sie einfach auf **Speichern**.
    
    Eine Seite angezeigt, das bestätigt, dass die neue DSR Groß-/Kleinschreibung erstellt wurde.
    
    ![Starten Sie die Suche oder schließen Sie die Groß-/Kleinschreibung neue DSR-Seite](media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    Zu diesem Zeitpunkt können Sie einen der folgenden Schritte ausführen:
    
    a. **mich Suchergebnisse anzeigen** klicken, beginnt die Suche. Dies ist die Standardauswahl. Die integrierte Suche, die ausgeführt wird, wenn Sie diese Option auswählen und die Ergebnisse, die zurückgegeben werden, sind in Schritt 3 beschrieben.
    
    b auf **Fertig stellen** klicken schließt die neue DSR Groß-/Kleinschreibung, ohne die integrierte Suche beginnen. Wenn Sie diese Option auswählen, wird die Groß-/Kleinschreibung neue DSR auf der Seite **Daten Subject-Anfragen** angezeigt.
    
6. Klicken Sie auf **Fertig stellen** , sodass Sie Sie die neue DSR Groß-/Kleinschreibung rufen und Mitglieder hinzufügen können. 
    
7. Klicken Sie auf der Seite **Daten Subject-Anforderungen** auf den Namen der DSR-Anfrage, die Sie gerade erstellt haben. 
    
8. Klicken Sie auf der Seite flyoutmenü **Verwalten in diesem Fall** klicken Sie unter **Manage Mitglieder**auf **Hinzufügen**. 
    
    Klicken Sie unter **Benutzer**wird eine Liste der Personen, die die entsprechenden eDiscovery-Berechtigungen zugewiesen wurden, angezeigt. Beachten Sie, dass die Personen, denen, die Sie eDiscovery-Berechtigungen zum in Schritt 1 zugewiesen, in dieser Liste angezeigt werden. 
    
9. Wählen Sie die Personen als Mitglieder der Anfrage DSR hinzufügen, klicken Sie auf **Hinzufügen**, und speichern Sie Ihre Änderungen.
    
    Beachten Sie, dass Sie Rollengruppen auch als Mitglieder von DSR Groß-/Kleinschreibung hinzufügen können, indem Sie auf **Hinzufügen** , klicken Sie unter **Rollengruppen verwalten**. 
    
## <a name="step-3-run-the-search-query"></a>Schritt 3: Ausführen die Suchabfrage

Nachdem Sie eine Anfrage DSR erstellen und Hinzufügen von Mitgliedern, besteht der nächste Schritt die integrierte Suche auszuführen, die die Groß-/Kleinschreibung zugeordnet ist. Dieses Standard-Suchabfrage bewirkt Folgendes:
  
- Sucht alle Postfächer in Ihrer Organisation für alle e-Mail-Elemente, die gesendet oder Empfangen von der betroffenen wurden. Dies erfolgt mithilfe der *Teilnehmer* Email-Eigenschaft, die für den Betreff der Daten in allen Feldern, die Personen in einer e-Mail-Nachricht sucht. Diese Eigenschaft gibt die Elemente in der **aus**, **an**, **CC**und **BCC** -Felder, in denen die betroffenen Person ist. Öffentliche Ordner in Exchange Online werden auch für Nachrichten, die von der betroffenen Person gesendet oder empfangen durchsucht. 
    
- Sucht alle Websites in Ihrer Organisation für Dokumente und Elemente, die erstellt oder von der betroffenen hochgeladen wurden. Dies erfolgt mithilfe der folgenden Eigenschaften:
    
  - *Author* -Eigenschaft gibt Elemente zurück, in dem die betroffenen Person in das Autorenfeld in Office-Dokumenten aufgeführt. Dieser Wert weiterhin auftritt, auch wenn das Dokument kopiert und von einer anderen Person hochgeladen. 
    
  - Die *Eigenschaften CreatedBy* -Eigenschaft gibt die Elemente, die erstellt oder von der betroffenen hochgeladen wurden zurück. 
    
Hier ist wie der Stichwortabfrage für die integrierte Suche aussieht, die automatisch erstellt wird, wenn Sie eine Anfrage DSR erstellen.
  
```
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Der Name der betroffenen Ina Leonte ist, könnte beispielsweise die Schlüsselwort-Abfrage wie folgt aussehen:
  
```
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **So führen die integrierte Suche für eine DSR-Anfrage:**
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **den Datenschutz** \> **Daten Subject-Anforderungen**, und klicken Sie dann auf **Öffnen** , neben die DSR-Anfrage, die Sie in Schritt2 erstellt haben. 
    
    Klicken Sie auf der Registerkarte " **Suchen** " am oberen Rand der Seite, und klicken Sie dann auf das Kontrollkästchen neben der integrierten suchen, die bei der Erstellung der neuen DSR-Anfrage erstellt wurde. Hinweis für die Suche hat den gleichen Namen wie die DSR Groß-/Kleinschreibung. 
    
2. Klicken Sie auf **Abfrage öffnen**, in der Dropdown-Suchseite.
    
    Wenn Sie die Abfrage öffnen, wird die Suche wird gestartet und abgeschlossen in einen Moment. 
    
3. Wenn die Suche abgeschlossen ist, klicken Sie auf **Vorschau Ergebnisse** , um eine Vorschau der Suchergebnisse anzuzeigen. Weitere Informationen finden Sie unter [Vorschau der Suchergebnisse](content-search.md#preview-search-results).
    
    > [!TIP]
    > Sie können auch die Suchstatistik Abfrage, um die Anzahl der Postfach- und Website-Elemente, die von der Suche zurückgegeben werden und die Speicherorte für oberen Inhalte, die Elemente enthält, die die Suchabfrage entsprechen, anzeigen. Weitere Informationen finden Sie unter [Anzeigen von Informationen und Statistiken zu einer Suche](content-search.md#view-information-and-statistics-about-a-search). 
  
Sie können die integrierten Suchabfrage bearbeiten, ändern die Speicherorte für Inhalte, die durchsucht werden und führen Sie die Suche erneut. Weitere Informationen finden Sie unter [Schritt 5](#optional-step-5-revise-the-built-in-search-query) . 
  
## <a name="step-4-export-the-data"></a>Schritt 4: Exportieren der Daten

Nachdem Sie die integrierte Suche ausführen können Sie die Suchergebnisse exportieren. Bevor Sie die Daten exportiert werden, sollten Sie alternativ die Abfrage aus, um die Anzahl der Suchergebnisse reduzieren zu ändern. Weitere Informationen zum Eingrenzen der Suchergebnisse finden Sie unter Schritt 5.
  
Beim Exportieren von Suchergebnissen können Postfachelemente in PST-Dateien oder als einzelne Nachrichten heruntergeladen werden. Beim Exportieren von Inhalt aus SharePoint und OneDrive-Konten werden Kopien der systemeigenen Office-Dokumente und andere Dokumente exportiert. Eine Datei mit den Suchergebnissen, die Informationen über jedes Element enthält, die exportiert wird, ist auch mit den Suchergebnissen enthalten. Ausführlichere Informationen zum Exportieren von finden Sie unter [Exportieren der Suchergebnisse aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md).
  
> [!NOTE]
> Standardmäßig ist ein globaler Office 365-Administrator (oder andere Mitglieder der Rollengruppe "Organisationsverwaltung" in das Wertpapier &amp; Compliance Center) nicht über die erforderlichen Berechtigungen zum Exportieren von Suchergebnissen verfügen. Dieses Problem umgehen, kann ein Administrator sich selbst als Mitglied der Gruppe der eDiscovery-Manager-Rolle hinzufügen. 
  
Der Computer, den Sie zum Exportieren von Daten verwenden, muss die folgenden Voraussetzungen erfüllen:
  
- 32- oder 64-Bit-Versionen von Windows 7 und höher
    
- Microsoft .NET Framework 4.7
    
- Einen unterstützten Browser:
    
  - Microsoft Edge
    
    oder -
    
  - Microsoft Internet Explorer 10 und höhere Versionen
    
    > [!NOTE]
    > Microsoft herstellen nicht Drittanbieter-Erweiterungen oder Add-ons für ClickOnce-Anwendungen. Exportieren von Daten mit einem nicht unterstützten Browser mit Drittanbieter-Erweiterungen oder Add-ons wird nicht unterstützt. 
  
 **So exportieren Sie Daten aus der integrierte Suche in dem Fall DSR:**
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **den Datenschutz** \> **Daten Subject-Anforderungen**, und klicken Sie dann auf **Öffnen** , neben die DSR-Anfrage, die Daten exportiert werden soll. 
    
2. Klicken Sie auf der Registerkarte " **Suchen** " am oberen Rand der Seite, und klicken Sie dann auf das Kontrollkästchen neben der integrierten Suche, die erstellt wurde, wenn Sie die DSR Groß-/Kleinschreibung erstellt haben. Oder klicken Sie auf eine andere Suche, um Daten aus, dass die Suche zu exportieren. 
    
3. Klicken Sie auf der Seite Suche flyoutmenü auf ![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Weitere**, und wählen Sie dann **Exportergebnisse** aus der Dropdown Liste. 
    
4. Wählen Sie auf der Seite **Ergebnisse exportieren** die folgenden empfohlenen Optionen für DSR exportanforderungen. 
    
    ![Konfigurieren Sie die exporteinstellungen](media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. unter **Ausgabeoptionen**wählen Sie die erste Option ( **alle Elemente mit Ausnahme der Schriftarten, die Schriftarten, die ein unbekanntes Format haben, verschlüsselt werden, oder aus anderen Gründen indiziert wurden nicht, haben**) zum Exportieren von indizierter Elementen nur. Der Grund dafür, dass Sie nicht teilweise indizierte Elemente aus der integrierten Suche exportieren möchten besteht, da teilweise indizierte Elemente von anderen Benutzern exportiert werden sollen. Um nur die teilweise indizierte Elemente für den Betreff der Daten zu exportieren, wird empfohlen, eine separate Suche zu erstellen. Weitere Informationen finden Sie unter [Exportieren teilweise indizierte Elemente](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#exportunindexeditems) im Abschnitt "Weitere Informationen zur Verwendung der Groß-/Kleinschreibung DSR-Tools".
    
    b Wählen Sie unter **Exportieren von Exchange-Inhalte als**die dritte Option, **eine PST-Datei, die alle Nachrichten in einem gemeinsamen Ordner enthält**. Da einige der Ergebnisse für Elemente, die im Postfach eines anderen Benutzers stammt sein kann, diese Option nur Listet das Element in einem gemeinsamen Ordner ohne, der angibt, des tatsächlichen Postfachs und ist die beste Option zu verwenden, wenn Sie die Ergebnisse entsprechend den Empfehlungen in das nächste Element Entfernung von Duplikaten . Mit dieser Option können auch die betroffenen Elemente in chronologischer Reihenfolge (Absendedatum werden Elemente sortiert) überprüfen, ohne die ursprünglichen Postfachordnerstruktur für jedes Element zu navigieren.
    
    c Option **Deduplizierung aktivieren** können schließt doppelte e-Mail-Nachrichten. Diese Option wird empfohlen, da die integrierte Suche alle Postfächer in Ihrer Organisation durchsucht. Damit mehrere Kopien der gleichen Nachricht in die Postfächer gefunden, die durchsucht wurden, diese Option ist wird nur eine Kopie einer Nachricht exportiert werden. Diese Option werden zusammen ausführende Nachrichten in eine PST-Datei in einem gemeinsamen Ordner die beste benutzerumgebung für DSR führt Anforderungen exportieren. Beachten Sie, dass der Bericht Results.csv Export alle Speicherorte aufgelistet werden, in dem doppelte Nachrichten gefunden wurden.
    
    Optional können Sie **Include-Versionen für SharePoint-Dokumente** Option zum Exportieren von allen Versionen von SharePoint und OneDrive Dokumente auswählen. Dies erfordert, dass diese Versioning für Dokumentbibliotheken aktiviert ist. Diese Option wird sichergestellt, dass alle relevante Daten werden exportiert.
    
5. Nachdem Sie die exporteinstellungen ausgewählt haben, klicken Sie auf **Exportieren**.
    
    Die Suchergebnisse werden vorbereitet für das Herunterladen, was bedeutet, dass Upload zu dem Bereich der Azure-Speicher für Ihre Organisation in der Microsoft-Cloud. Die nächsten Schritte zeigen, wie diese Daten auf den lokalen Computer herunterladen.
    
6. Klicken Sie auf die Registerkarte **Exportieren** , um den Exportauftrag anzuzeigen, die, den Sie gerade erstellt haben. Beachten Sie, dass Exportaufträge denselben Namen wie das entsprechende suchen mit **_Export** bis zum Ende des Suchbegriff angefügt haben. 
    
7. Klicken Sie auf den Exportauftrag, den Sie gerade erstellt haben, um die Export-Dropdown-Seite anzuzeigen. Diese Seite zeigt Informationen über die Suche, wie die Größe und die Gesamtanzahl der Elemente exportiert werden sollen, und den Prozentsatz der Elemente, die in einen Bereich Azure-Speicher übertragen wurden. Klicken Sie auf **Aktualisieren** , um die Statusinformationen Upload zu aktualisieren. 
    
8. Klicken Sie unter **Schlüssel exportieren**auf **in die Zwischenablage kopieren**. Sie werden dieser Schlüssel in Schritt 11 verwenden, um die Suchergebnisse herunterzuladen.
    
9. Klicken Sie auf ![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) am oberen Rand der Seite exportieren flyoutmenü **Ergebnisse herunterladen** . 
    
10. Klicken Sie im Popupfenster am unteren Rand der Seite auf **Öffnen** , um die **Microsoft Office 365-eDiscovery-Exporttool**öffnen. Die **eDiscovery-Exporttool** wird der ersten Verwendung installiert werden Sie Suchergebnisse herunterladen. 
    
11. Fügen Sie in der **eDiscovery-Exporttool**den Schlüssel exportieren, den Sie in Schritt 8 im entsprechenden Feld kopiert.
    
12. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der großen Menge von Datenträgeraktivität (Lese- und Schreibvorgänge) sollten Sie Suchergebnisse auf einem lokalen Laufwerk herunterladen. nicht auf ein Netzlaufwerk oder anderen Speicherort im Netzwerk herunterladen. 
  
13. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Die **eDiscovery-Exporttool** zeigt Statusinformationen über den Exportvorgang, einschließlich eine Schätzung der Anzahl (und Größe) der verbleibenden Elemente heruntergeladen werden. Wenn der Exportvorgang abgeschlossen ist, können Sie die Dateien in den Speicherort zugreifen, in dem sie heruntergeladen wurden. Weitere Informationen zu den Berichten, die beim Herunterladen von Suchergebnissen enthalten, finden Sie im Abschnitt [Weitere Informationen](export-search-results.md#more-information) in "Export Content Suchergebnisse aus der Office 365-Sicherheit &amp; Compliance Center". 
    
Nachdem die Daten exportiert werden, werden die Suchergebnisse und Exportieren von Berichten in einem Ordner gespeichert, die hat den gleichen Namen wie die DSR Groß-/Kleinschreibung. Die PST-Dateien, die Postfachelemente enthalten befinden sich in einem Unterordner mit dem Namen **Exchange**. Dokumente und andere Elemente von Websites befinden sich in einem Unterordner mit dem Namen **SharePoint**. 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>(Optional) Schritt 5: Überprüfen Sie die integrierten Search-Abfrage

Nachdem Sie die integrierte Suche ausführen können Sie es zum Einschränken des Bereichs zum Zurückgeben von Suchergebnissen weniger überarbeiten. Hierzu können Sie Bedingung der Abfrage hinzufügen. Eine Bedingung ist mit der Stichwortabfrage logisch mithilfe der **AND** -Operator verbunden. Das bedeutet zurückgegeben in den Suchergebnissen Elemente erfüllen müssen, die Stichwortabfrage und etwaige Auflagen, die Sie hinzufügen. Dies ist die Bedingungen wie helfen, um die Suchergebnisse einzuschränken. Wenn Sie zwei oder mehr eindeutige Bedingungen auf eine Suchabfrage (Conditions, die verschiedene Eigenschaften angeben) hinzufügen, werden diese Probleme logisch durch **AND** -Operator verbunden. Dies bedeutet, dass nur die Elemente, die alle Bedingungen (zusätzlich zu der Stichwortabfrage) erfüllen zurückgegeben werden. Wenn Sie mehrere Werte (durch Kommas oder Semikolons voneinander getrennt) zu einer einzelnen Bedingung hinzufügen, werden diese Werte durch den **oder** -Operator verbunden. Dies bedeutet, dass Elemente zurückgegeben werden, wenn sie eines der angegebenen Werte für die Eigenschaft in der Bedingung enthalten. 
  
Es folgen einige Beispiele der Bedingungen, die die integrierten Suchabfrage ein DSR-Fall hinzugefügt werden können. Der Name der tatsächlichen-Eigenschaft bei einer Suchabfrage verwendet wird in Klammern angezeigt.
  
- **Dateityp ( `filetype`)** -gibt die Erweiterung eines Dokuments oder einer Datei. Verwenden Sie diese Bedingung, um für Dokumente und bestimmte Office-Programme wie Word, Excel und OneNote erstellten Dateien zu suchen. 
    
- **Art der Nachricht ( `kind`)** -gibt den Typ des zu suchenden e-Mail-Elements. Sie können beispielsweise die Syntax `kind:email OR kind:im` nur e-Mail-Nachrichten und Skype für Business Unterhaltungen oder 1: 1-Chats in Microsoft-Teams, zurückgegeben. 
    
- **Compliance-Tag (`compliancetag`)** -gibt eine Bezeichnung zu einer e-Mail-Nachricht oder einem Dokument zugewiesen. Diese Bedingung gibt Elemente zurück, die mit einem bestimmten Etikett klassifiziert werden. Etiketten dienen zum Klassifizieren von e-Mails und Dokumente für Daten Governance und Erzwingen von Aufbewahrungsregeln basierend auf der Klassifikation durch die Bezeichnung definiert. Dies ist eine nützliche Bedingung für DSR Untersuchungen, da Ihre Organisation Etiketten verwenden kann, um Inhalt im Zusammenhang mit Datenschutz klassifizieren oder das persönliche Daten oder vertrauliche Informationen enthält. Verwenden Sie für den Wert des diese Bedingung die vollständige Beschriftungsnamen oder den ersten Teil des Namens Label mit einem Platzhalter. Weitere Informationen finden Sie unter [Übersicht über die Beschriftungen in Office 365](labels.md).
    
Eine Liste und Beschreibung aller Bedingungen in der Groß-/Kleinschreibung DSR-Tool finden Sie unter [suchbedingungen](keyword-queries-and-search-conditions.md#search-conditions) im Artikel "Stichwortabfragen und Suchkriterien für die Inhaltssuche". 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Ändern die Speicherorte für Inhalte, die durchsucht werden

Zusätzlich zu überarbeiten die integrierte Suche für eine DSR-Anfrage, können Sie auch die Speicherorte für Inhalte ändern, die durchsucht werden. Wie bereits erklärt sucht die integrierte Suche jedem Postfach und die Website in der Organisation und Exchange Online Öffentliche Ordner an. Beispielsweise könnte die Suche, um nur des Daten des Antragstellers Postfach- und OneDrive Konto suchen einschränken und SharePoint-Websites ausgewählt. Wenn Sie auswählen, um bestimmte Websites zu suchen, müssen Sie jeden Standort hinzufügen, die Sie suchen möchten.
  
So ändern Sie die Speicherorte für Inhalte zu suchen:
  
1. Öffnen Sie die integrierte Suche, der Sie für die Speicherorte für Inhalte ändern möchten.
    
2. Klicken Sie in der Suchabfrage klicken Sie unter **Speicherorte** **Bearbeiten** neben die Option **bestimmte Orte** aus. 
    
    ![Klicken Sie auf ändern, um die Speicherorte für Inhalte der integrierten Suchabfrage ändern](media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    Die **Adressen ändern** Dropdown-Seite wird angezeigt. Es folgt eine Beschreibung für die Speicherorte für Inhalte in die integrierte Suche und einige Informationen zum Ändern der Speicherorte, die durchsucht werden. 
    
    ![Dropdown-Seite Speicherorte ändern](media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a. die Umschaltfläche klicken Sie unter **Wählen Sie alle** im Postfach Abschnitt am oberen Rand der Seite flyoutmenü ist ausgewählt, gibt an, dass alle Postfächer durchsucht werden. Um die Suche einzugrenzen, klicken Sie auf die Umschaltfläche zum deaktivieren, und klicken Sie dann auf **Wählen Sie Benutzer, Gruppen oder Teams** und wählen bestimmte Postfächer zu suchen.
    
    b. das Umschalten unter **Alles markieren** Sie im Abschnitt Websites in der Mitte der Seite flyoutmenü ist ausgewählt, gibt an, dass alle Websites durchsucht werden. Um die Suche auf ausgewählte Websites zu beschränken, würden Sie die Umschaltfläche deaktivieren und dann auf **auswählen Sites**. Sie müssen jeden speziellen Standort hinzufügen, die Sie suchen möchten, einschließlich der betroffenen Person OneDrive Konto.
    
    c. der Umschaltfläche im Abschnitt Exchange Öffentliche Ordner ist aktiviert, was bedeutet, dass alle öffentlichen Exchange-Ordner durchsucht werden. Beachten Sie, dass Sie alle öffentlichen Exchange-Ordner oder keines der Projekte nur suchen können. Sie können nicht das Domänenkennwort suchen auswählen.
    
3. Wenn Sie die Speicherorte für Inhalte in die integrierte Suche ändern, klicken Sie auf **Speichern &amp; ausführen** für die Suche erneut zu starten. 
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Weitere Informationen zur Verwendung der Groß-/Kleinschreibung DSR-Tools

Die folgenden Abschnitte enthalten weitere Informationen zur Verwendung des Groß-/Kleinschreibung DSR-Tools auf DSR exportanforderungen reagieren.
  
[Exportieren von Daten aus MyAnalytics und den Dienst für die Office-Roaming](#exporting-data-from-myanalytics-and-the-office-roaming-service)

[Exportieren von teilweise indizierte Elemente](#exporting-partially-indexed-items)

[Suchen und Exportieren von Daten aus Microsoft-Teams und Office 365-Gruppen](#searching-and-exporting-data-from-microsoft-teams-and-office-365-groups)

[Suchen nach öffentlichen Ordnern von Exchange](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-myanalytics-and-the-office-roaming-service"></a>Exportieren von Daten aus MyAnalytics und den Dienst für die Office-Roaming

Das Groß-/Kleinschreibung DSR-Tool können Sie suchen und Exportieren von Verwendungsdaten, die von MyAnalytics und den Dienst für die Office-Roaming generiert werden. Hier ist eine Beschreibung des vorgehen, diese Dienste:
  
- **MyAnalytics** - ermöglicht es Benutzern Rückschlüsse wie ihre Zeit basierend auf den Daten e-Mail und Kalender in ihrem Postfach verbringen. Besprechung und e-Mail-Kopfzeilen in das Postfach des Benutzers sind alle MyAnalytics Insights abgeleitet. Benutzer, die eine MyAnalytics Lizenz zugewiesen sind können zu Office 365 anmelden und wechseln Sie zum Anzeigen der Rückschlüsse auf wie ihre Zeit verbringen MyAnalytics-Dashboard. (Benutzer können Screenshots, die diese Einblicke als Antwort auf die Anforderung einer DSR Access Bildschirm). Die integrierte Suche in DSR Fall werden die Daten exportiert werden, die zum Generieren von MyAnalytics Insights verwendet wird. 
    
- **Office-Roaming Service** - Roaming ist ein Dienst, der Office-bezogene Einstellungen, wie Office-Design, Benutzerwörterbuch, spracheinstellungen, Entwicklermodus und AutoKorrektur speichert. 
    
Die Daten aus MyAnalytics und den Dienst Office Roaming ist im Postfach in verborgenen Ordnern befindet sich in einer Nachricht nicht personenbezogenen (nicht-IPM) Exchange Online-Postfächern des Antragstellers Daten gespeichert. Dies bedeutet, dass die Daten aus der Ansicht des Benutzers ausgeblendet ist, wenn sie Outlook oder anderen e-Mail-Clients verwenden, um ihre Postfächer zugreifen. Weitere Informationen zu ausgeblendeten Ordnern finden Sie unter [MAPI verborgene Ordner](https://go.microsoft.com/fwlink/?linkid=872758).
  
Sie können erstellt eine separate Inhaltssuche (und ordnen Sie ihm eine Anfrage DSR), gibt die MyAnalytics und die Office-Roaming Service Nutzungsdaten in die Daten Betreffzeilen Postfach. Diese Daten nicht in die Suchstatistik einbezogen, und er nicht für die Vorschau werden. Sie können jedoch zu exportieren und weisen Sie ihr den betroffenen als Antwort auf eine DSR-Export-Anforderung.
  
Beim Exportieren von Daten aus MyAnalytics und den Office Roaming Service werden die Daten in einen gesonderten Ordner für jede Anwendung gespeichert, die sich im Ordner **ApplicationDataRoot** befindet befindet sich unter einem Ordner, der Name mit der betroffenen Person e-Mail-Adresse ist. Diese Daten werden als JSON-Dateien exportiert lesbare Textdateien ähnlich wie XML oder TXT-Dateien darstellen, die e-Mail-Nachrichten angefügt sind. Derzeit werden diese Ordner mit einen global eindeutigen Bezeichner (GUID) benannt, die zum MyAnalytics und der Office Roaming-Dienst, die in der folgenden Tabelle aufgeführt sind zugewiesen ist. Die GUID wird in zukünftigen Versionen des DSR Groß-/Kleinschreibung Tools mit dem Namen der eigentlichen Anwendung ersetzt. 
  
|**Anwendung**|**GUID/Ordnername**|
|:-----|:-----|
|MyAnalytics  <br/> |3c896ded-22c5-450f-91f6-3d1ef0848f6e  <br/> |
|Office-Roamingdienst  <br/> |1caee58f-eb14-4a6b-9339-1fe2ddf6692b  <br/> |
   
 **Suchen und Exportieren von Daten MyAnalytics und Office Roaming Service:**
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **den Datenschutz** \> **Daten Subject-Anforderungen**, und klicken Sie dann auf **Open** neben der DSR Groß-/Kleinschreibung für den Betreff von Daten, die Sie Verwendungsdaten für exportieren möchten. 
    
2. Klicken Sie auf der Registerkarte " **Suchen** " am oberen Rand der Seite, und klicken Sie dann auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Guided suchen**.
    
3. Klicken Sie auf der Seite **Name der Suche** auf **Abbrechen** . 
    
4. Wählen Sie unter **Search-Abfrage**in der Bedingung **Typ** die Kontrollkästchen neben **MyAnalytics** und **Office Roaming-Dienst**aus. 
    
    ![Aktivieren Sie die Kontrollkästchen MyAnalytics und Office Roaming-Dienst zum Exportieren von Verwendungsdaten](media/3dacbc7a-c314-492c-828c-6757fda84963.png)
  
    Beachten Sie, dass die Bedingung **Type** (die e-Mail-Nachrichtenklassen sind) in der Suchabfrage einziges Element werden soll. Sie können das Feld **Schlüsselwörter** gelöscht oder leer lassen. 
    
5. Klicken Sie unter **Speicherorte**stellen Sie sicher, dass **bestimmte Orte** ausgewählt ist, und klicken Sie dann auf **Ändern**.
    
6. Klicken Sie auf der oberen Teil der Seite flyoutmenü **Adressen ändern** (der Postfach-Bereich) **Wählen Sie Benutzer, Gruppen oder Teams**ein.
    
7. Klicken Sie auf der Seite **"Bearbeiten"** klicken Sie auf **Wählen Sie Benutzer, Gruppen oder Teams**, wählen Sie die Daten des Antragstellers Postfach, und speichern Sie Ihre Auswahl. 
    
8. Klicken Sie auf **Speichern &amp; ausführen**, und nennen Sie die Suche, und speichern Sie es.
    
    Die Suche wird gestartet.
    
 **So exportieren Sie Daten MyAnalytics und Office Roaming Service:**
  
1. Nach Abschluss die Suche, die Sie im vorherigen Schritt erstellt haben, klicken Sie auf der Registerkarte " **Suchen** " am oberen Rand der Seite, und klicken Sie dann auf das Kontrollkästchen neben der Suche. Möglicherweise müssen Sie klicken Sie auf ![aktualisieren](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **Aktualisieren** , um die Suche angezeigt werden. 
    
2. Klicken Sie auf der Seite Suche flyoutmenü auf ![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Weitere**, und wählen Sie dann **Exportergebnisse** aus der Dropdown Liste. 
    
3. Wählen Sie auf der Seite **Ergebnisse exportieren** die folgenden empfohlenen Optionen zum Exportieren von Verwendungsdaten. 
    
    ![Exportoptionen beim Exportieren von Verwendungsdaten MyAnalytics und Office Roaming-Dienst](media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. unter **Ausgabeoptionen**wählen Sie die erste Option ( **alle Elemente mit Ausnahme der Schriftarten, die Schriftarten, die ein unbekanntes Format haben, verschlüsselt werden, oder aus anderen Gründen indiziert wurden nicht, haben**) zum Exportieren von indizierter Elementen nur.
    
    b Wählen Sie unter **Exportieren von Exchange-Inhalte als**die zweite Möglichkeit, **eine PST-Datei, die alle Nachrichten**.
    
    c. lassen Sie c. die restlichen Exportoptionen deaktiviert.
    
4. Nachdem Sie die exporteinstellungen ausgewählt haben, klicken Sie auf **Exportieren**.
    
    Die Suchergebnisse werden vorbereitet für das Herunterladen, was bedeutet, dass Upload zu dem Bereich der Azure-Speicher für Ihre Organisation in der Microsoft-Cloud. Die nächsten Schritte zeigen, wie diese Daten auf den lokalen Computer herunterladen.
    
5. Klicken Sie auf die Registerkarte **Exportieren** , um den Exportauftrag anzuzeigen, die, den Sie gerade erstellt haben. Beachten Sie, dass Exportaufträge denselben Namen wie das entsprechende suchen mit **_Export** bis zum Ende des Suchbegriff angefügt haben. 
    
6. Klicken Sie auf den Exportauftrag, den Sie gerade erstellt haben, um die Export-Dropdown-Seite anzuzeigen. 
    
7. Klicken Sie unter **Schlüssel exportieren**auf **in die Zwischenablage kopieren**. Sie werden dieser Schlüssel in Schritt 10 verwenden, um die Suchergebnisse herunterzuladen.
    
8. Klicken Sie auf ![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) am oberen Rand der Seite exportieren flyoutmenü **Ergebnisse herunterladen** . 
    
9. Klicken Sie im Popupfenster am unteren Rand der Seite auf **Öffnen** , um die **Microsoft Office 365-eDiscovery-Exporttool**öffnen. Die **eDiscovery-Exporttool** wird der ersten Verwendung installiert werden Sie Suchergebnisse herunterladen. 
    
10. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 7 kopiert haben, in das entsprechende Feld ein.
    
11. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der großen Menge von Datenträgeraktivität (Lese- und Schreibvorgänge) sollten Sie Suchergebnisse auf einem lokalen Laufwerk herunterladen. nicht auf ein Netzlaufwerk oder anderen Speicherort im Netzwerk herunterladen. 
  
12. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Die **eDiscovery-Exporttool** zeigt Statusinformationen über den Exportvorgang, einschließlich eine Schätzung der Anzahl (und Größe) der verbleibenden Elemente heruntergeladen werden. Wenn der Exportvorgang abgeschlossen ist, können Sie öffnen Sie die Exchange-PST-Datei in Outlook und wechseln Sie zu dem Ordner **ApplicationDataRoot** auf die Unterordnern MyAnalytics und Roaming-Dienst zugreifen. 
    
    Wie bereits erklärt werden die JSON-Dateien, die Nutzungsdaten enthält an Nachrichten angehängt. Um ein JSON-Datei anzuzeigen, klicken Sie auf eine Nachricht aus, und öffnen Sie die angefügte JSON-Datei. 
  
### <a name="exporting-partially-indexed-items"></a>Exportieren von teilweise indizierte Elemente

Es wird empfohlen, dass Sie über die integrierte Suche teilweise indizierte Elemente (auch als nicht-indizierten Elementen bezeichnet) exportieren nicht, die beim Erstellen einer neuen DSR-Anfrage erstellt wird. Dies liegt daran die Suche, die Ergebnisse werden höchstwahrscheinlich teilweise enthalten indizierte Elemente für andere Benutzer in Ihrer Organisation und nicht nur teilweise indizierte Elemente für den Betreff Daten). Stattdessen wird empfohlen, dass Sie einen separaten Inhaltssuche, die die DSR Groß-/Kleinschreibung zugeordnet ist, die entwickelt wurde erstellen, um nur die teilweise indizierte Elemente im Zusammenhang mit der betroffenen Person zu exportieren. 
  
Hier ist der allgemeiner Prozess zum Exportieren von teilweise indizierter Elementen. Nachdem sie Export sind, können Sie prüfen, um festzustellen, ob ein Elemente zu einem DSR Zugriffspunkt reagiert oder Anforderung exportieren.
  
1. Öffnen Sie die DSR-Anfrage und erstellen Sie eine neue Suche auf **der Suchseite** . 
    
2. Verwenden Sie die folgenden Kriterien zum Konfigurieren von Search-Abfrage und die Speicherorte für Inhalte um zu suchen:
    
    - Verwenden Sie eine leere/leer Stichwortabfrage. Dadurch werden alle Elemente in die Speicherorte für Inhalte zurückgegeben, die durchsucht werden.
    
    - Suchen Sie nur die Daten des Antragstellers Exchange Online-Postfach und ihre OneDrive-Konto.
    
3. Nachdem Sie führen Sie die Suche, und er abgeschlossen ist, können Sie exportieren und Laden Sie die Suchergebnisse (wie in [Schritt 4](#step-4-export-the-data)beschrieben). Verwenden Sie die folgenden Einstellungen, um teilweise indizierte Elemente zu exportieren. 
    
    - Wählen Sie unter **Ausgabeoptionen**die dritte Option zum Exportieren von nur teilweise indizierter Elementen ( **nur Elemente mit ein unbekanntes Format, verschlüsselt werden, oder aus anderen Gründen indiziert wurden nicht**).
    
    - Unter **Exportieren von Exchange-Inhalte als**können Sie eine beliebige Option für die jeweiligen testanforderungen auswählen. 
    
    - Auswählen der Option **Include-Versionen für SharePoint-Dokumente** exportiert Versionen von Dokumenten eine Version teilweise indiziert ist. 
    
Weitere Informationen zu teilweise indizierte Elemente finden Sie unter: 
  
- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md)

- [Exportieren von teilweise indizierte Elemente](export-search-results.md#exporting-partially-indexed-items)
    
### <a name="searching-and-exporting-data-from-microsoft-teams-and-office-365-groups"></a>Suchen und Exportieren von Daten aus Microsoft-Teams und Office 365-Gruppen

Unterhaltungen, die Teil der Liste der Chat in Microsoft-Teams (Team Chats oder 1: 1-Chats bezeichnet) sind befinden sich in der Exchange Online-Postfach der Benutzer, die in den Chats teilnehmen. Darüber hinaus werden die Dateien, die eine Person in einer 1: 1-Chat teilt im OneDrive Konto der Person gespeichert, die die Dateifreigaben. Da die integrierte Suche in der Organisation alle Postfächer und OneDrive Konten sucht, werden Team Chats und Dokumente in einer chatsitzung (die betroffenen erstellt oder hochgeladen) freigegebenen durch integrierte Suche in dem Fall DSR zurückgegeben.
  
Alternativ werden Unterhaltungen, die Teil eines Teams Kanals (auch als Channel Nachrichten bezeichnet) sind im Postfach gespeichert, die ein Team zugeordnet ist. Diese Arten von Unterhaltungen, denen betroffenen teilgenommen werden auch durch die integrierte Suche zurückgegeben, da alle Postfächer zugeordneten Microsoft-Teams, durchsucht werden. Darüber hinaus werden die Kacheln, die ein Betreff für die Daten in einem Kanal Teams freigegeben haben möglicherweise auf SharePoint-Teamwebsite gespeichert. Dateien erstellt oder Uploadedby betroffenen zurückgegeben durch die integrierte Suche in dem Fall DSR, da Websites zugeordneten Microsoft-Teams bei der Suche enthalten sind.
  
In ähnlicher Weise sind Postfächern und SharePoint-Websites, die ein Office 365-Gruppe entsprechen, in die integrierte Suche ebenfalls enthalten. Dies bedeutet, dass e-Mail-Nachrichten, sofern von der betroffenen Person gesendet oder empfangen und Dateien erstellt oder hochgeladen haben, nach dem Betreff Daten zurückgegeben werden. 
  
Weitere Informationen zur Verwendung von Inhaltssuche Suche nach Elementen in Microsoft-Teams und Office 365 Gruppen oder dazu, wie Sie eine Liste der Elemente abrufen finden Sie im Abschnitt "Suchen von Microsoft-Teams und Office 365 Groups" im [Content-Suche in Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups). 
  
### <a name="searching-exchange-public-folders"></a>Suchen nach öffentlichen Ordnern von Exchange

Die integrierte Suche in dem Fall DSR wird nur return e-Mail-Nachrichten, dass die betroffenen Person gesendet, um einen e-Mail-aktivierten Öffentlichen Ordner oder Nachrichten, die eine andere Person zu einem öffentlichen Ordner gesendet und die betroffenen Person ebenfalls kopiert. Es gibt keine Nachricht, die der Betreff Daten veröffentlicht haben möglicherweise zurück, mit einem öffentlichen Ordner. Um die Suche nach Elementen, die der Betreff der Daten in einem öffentlichen Ordner veröffentlicht können Sie eine Separate erstellen Erstellen Sie eine separate Inhaltssuche, das für jedes Element in einem öffentlichen Ordner von der betroffenen gebucht durchsucht.
  
Hier ist der allgemeiner Prozess nach Elementen gesucht, die betroffenen möglicherweise mit einem öffentlichen Ordner veröffentlicht haben. 
  
1. Öffnen Sie die DSR-Anfrage und erstellen Sie eine neue Suche auf **der Suchseite** . 
    
2. Verwenden Sie die folgenden Kriterien zum Konfigurieren von Search-Abfrage und die Speicherorte für Inhalte um zu suchen:
    
  - Verwenden Sie die folgenden Suchabfrage in das Feld **Schlüsselwörter** : 
    
    ```
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Suchen Sie alle öffentlichen Exchange-Ordner
    
  - Nachdem Sie führen Sie die Suche, und er abgeschlossen ist, können Sie exportieren und Laden Sie die Suchergebnisse (wie in [Schritt 4](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#step4)beschrieben). Verwenden Sie die folgenden Einstellungen, um teilweise indizierte Elemente zu exportieren. 
