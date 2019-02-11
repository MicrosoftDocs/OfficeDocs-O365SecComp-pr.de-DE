---
title: Ansicht Verwaltungsberechtigter Audit-Aktivität
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 34e3fe207cf440c5992cdba7186e919a3968db22
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706146"
---
# <a name="view-custodian-audit-activity"></a>Ansicht Verwaltungsberechtigter Audit-Aktivität

Erforderlich, um zu ermitteln, ob ein Benutzer ein bestimmtes Dokument angezeigt oder ein Element aus dem Postfach gelöscht? Erweiterte eDiscovery (Preview) ist jetzt in der vorhandenen Audit Log Suchfunktion in die & Security Compliance Center integriert. Verwenden diese eingebetteten Erfahrung, können des erweiterten eDiscovery (Preview) Verwaltungsberechtigter-Verwaltungstools Sie um Ihre Untersuchung zu vereinfachen, indem auf einfache Weise den Zugriff auf und suchen die Aktivität für Verwalter innerhalb der Fall.

## <a name="before-you-begin"></a>Bevor Sie beginnen:

Sie müssen die Rolle des Kontaktobjekts überwachen Protokolle oder Protokolle überwachen im Exchange Online um das Office 365-Überwachungsprotokoll durchsuchen zugewiesen werden. Standardmäßig werden diese Rollen Organization Management Rollengruppen auf der Seite Berechtigungen in der Exchange-Verwaltungskonsole und der Verwaltung der Richtlinientreue zugewiesen. Wenn einem Benutzer die Möglichkeit, die das Überwachungsprotokoll erweiterte eDiscovery (Preview) mit der Mindestmaß an Privilegien durchsuchen übergeben möchten, erstellen eine benutzerdefinierte Rollengruppe in Exchange Online, die Kontaktobjekts überwachen Protokolle oder Protokolle überwachen Rolle hinzufügen und fügen Sie dann den Benutzer als Mitglied der neuen Rolle g Wiederherstellen. Weitere Informationen finden Sie unter Verwalten von Rollengruppen in Exchange Online.

> [!IMPORTANT]
> Wenn Sie einem Benutzer die Rolle Kontaktobjekts überwachen Protokolle oder Protokolle überwachen auf der Seite Berechtigungen in der & Security Compliance Center zuweisen, werden sie kann nicht auf das Office 365-Überwachungsprotokoll durchsuchen. Sie müssen die Berechtigungen in Exchange Online zuzuweisen. Dies ist, da das zugrunde liegende-Cmdlet verwendet, um das Überwachungsprotokoll durchsuchen Exchange Online-Cmdlet ist.

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a>Schritt 1: Erstellen einer erweiterten eDiscovery (Preview) Audit Log-Suche

   1. Wählen Sie eine vorhandene Anfrage aus der **Sicherheit & Compliance Center > erweiterte eDiscovery (Preview)**.
   
   2. Navigieren Sie zur Registerkarte **Verwalter** , und wählen Sie ein Verwaltungsberechtigter.
   
   3. Wenn Sie ein Verwaltungsberechtigter ausgewählt haben, klicken Sie auf **Ansicht Verwaltungsberechtigter Aktivität** aus dem Detailbereich.
   
   4. Konfigurieren Sie die folgenden Suchkriterien:
      
      a. **Aktivitäten** - klicken Sie auf die Dropdown-Liste die Aktivitäten angezeigt werden sollen, denen Sie für suchen können. Nachdem die Suche ausgeführt wurde, werden nur die Audit-Datensätze für die ausgewählten Aktivitäten angezeigt. Auswählen der **Ergebnisse für alle Aktivitäten anzeigen** zeigt Ergebnisse für alle Aktivitäten, die die anderen Suchkriterien erfüllen.
      
      b. **Startdatum und Enddatum** – wählen Sie einen Bereich Datum und Uhrzeit, um die Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten. Die letzten sieben Tagen sind standardmäßig aktiviert. Datum und Uhrzeit werden in koordinierter Weltzeit (UTC) Format angezeigt. Der maximale Zeitraum, den Sie angeben können, ist ein Jahr.
      
      c. **Verwalter** - klicken Sie in diesem Feld und wählen Sie ein bestimmtes Verwaltungsberechtigter anzuzeigenden Suche Ergebnisse für die. Audit-Einträge für die ausgewählten Aktivitäten, die von den Benutzern, die Sie in dieses Feld auswählen, werden in der Liste der Ergebnisse angezeigt.
    
    1. Klicken Sie auf **Suche** zum Ausführen der Suche mit den Suchkriterien. Die Suchergebnisse werden geladen, und werden sie nach einigen Augenblicken unter Ergebnisse angezeigt, auf der Seite Verwaltungsberechtigter Aktivitäten. 

## <a name="step-2-view-the-audit-log-search-results"></a>Schritt 2: Anzeigen der Audit Log der Suchergebnisse

Die Ergebnisse einer Audit Log Suche werden auf der Seite Verwaltungsberechtigter überwachen Protokoll unter Ergebnisse angezeigt. Maximal 5.000 (neu) Ereignisse werden in Schritten von 150 Ereignisse angezeigt. Zum Anzeigen von mehr Ereignisse können Sie im Ergebnisbereich die Bildlaufleiste oder drücken Sie UMSCHALT + Ende, um die nächsten 150 Ereignisse anzuzeigen.

Die Ergebnisse enthalten die folgende Informationen zu jedem Ereignis, das von der Suche zurückgegebenen.
- **Datum**: Datum und Uhrzeit (in UTC-Format), die das Ereignis auftrat.

- **IP-Adresse**: die IP-Adresse des Geräts, das verwendet wurde, wenn die Aktivität protokolliert wurde. Die IP-Adresse wird in ein IPv4 oder IPv6-Adressformat angezeigt.

- **Benutzer**: die Benutzer (oder ein Dienstkonto), die die Aktion, die das Ereignis ausgelöst hat ausgeführt.

- **Aktivität**: die Aktivitäten des Benutzers. Dieser Wert entspricht der Aktivitäten, die Sie in der Dropdownliste Aktivitäten ausgewählt haben. Für ein Ereignis aus dem Exchange Admin-Überwachungsprotokoll ist der Wert in dieser Spalte ein Exchange-Cmdlet.

- **Artikel**: das Objekt, das erstellt oder als Ergebnis der entsprechenden Aktivität geändert wurde. Die Datei, die angezeigt oder geändert wurde oder das Benutzerkonto, das aktualisiert wurde. Nicht alle Aktivitäten haben einen Wert in dieser Spalte.

- **Detail**: Weitere Informationen zur Aktivität. In diesem Fall müssen nicht alle Aktivitäten einen Wert.

## <a name="step-3-filter-the-search-results"></a>Schritt 3: Filtern von Suchergebnissen

Zusätzlich zum Sortieren, können Sie auch die Ergebnisse einer Audit Log Suche filtern. Dies hilft schnell Filtern der Ergebnisse für einen bestimmten Benutzer oder eine Aktivität. 

Um die Ergebnisse zu filtern:

 1. Erstellen und Ausführen einer Audit Log-Suche.
  
2. Wenn die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse filtern**.
 
3. Schlüsselwort-Felder werden unter jeder Spaltenüberschrift angezeigt.
  
4. Klicken Sie auf eines der Felder unter eine Spaltenüberschrift, und geben Sie ein Wort oder Ausdruck, je nach der Spalte, der Sie filtern möchten. Die Ergebnisse werden dynamisch textlichen, um die Ereignisse anzuzeigen, die den Filter entsprechen.
  
5. Um einen Filter zu löschen, klicken Sie auf das **X** im Filterfeld, oder klicken Sie einfach auf **Filtern ausblenden**.

## <a name="export-the-search-results-to-a-file"></a>Die Suchergebnisse in eine Datei exportieren

Sie können die Ergebnisse einer Audit Log-Suche in einer durch Trennzeichen getrennten Werten (CSV)-Datei auf Ihrem lokalen Computer exportieren. Sie können diese Datei in Microsoft Excel öffnen und verwenden Features wie beispielsweise die Suche, sortieren, Filtern und Aufteilen einer einzelnen Spalteninhalts (die Zellen mit mehreren Werte enthält) in mehreren Spalten.

1. Führen Sie eine Audit Log-Suche, und Überarbeiten Sie die Suchkriterien, bis Sie die gewünschten Ergebnisse haben.
  
2. Klicken Sie auf Exportergebnisse, und wählen Sie eine der folgenden Optionen aus:

    - **Speichern geladen Ergebnisse:** Wählen Sie diese Option, um nur die Einträge zu exportieren, die auf der Seite **Verwaltungsberechtigter Audit Log Suche** unter **Ergebnisse** angezeigt werden. Die CSV-Datei, die heruntergeladen wird enthält dieselben Spalten (und Daten) angezeigt, auf der Seite (Datum, Benutzer, Aktivität, Artikel und Details). Eine weitere Spalte (mit dem Titel **Weitere**) ist in der CSV-Datei enthalten, die Informationen aus dem Überwachungseintrag Protokoll enthält. Da Sie die gleichen Ergebnisse exportieren, die geladen (und angezeigt werden können) sind auf der Seite Audit Log Suche maximal 5.000 Einträge werden exportiert.
        
    - **Alle Ergebnisse herunterladen:** Wählen Sie diese Option, um alle Einträge aus dem Office 365-Überwachungsprotokoll, die die Suchkriterien erfüllen exportieren. Wählen Sie für eine große Gruppe von Suchergebnissen diese Option, um alle Einträge aus dem Überwachungsprotokoll zusätzlich zu den 5000 Ergebnisse herunterladen, die auf der Seite **Verwaltungsberechtigter Audit Log** angezeigt werden kann. Diese Option wird die Rohdaten in eine CSV-Datei aus dem Überwachungsprotokoll herunterladen und enthält zusätzliche Informationen aus dem Überwachungseintrag melden Sie sich in einer Spalte mit dem Namen AuditData. Länger kann dauern, die Datei herunterzuladen, wenn Sie diese Exportoption auswählen, da die Datei wesentlich größer als der sein kann, die heruntergeladen wird, wenn Sie die Option andere ausgewählt.
    
      > [!IMPORTANT]
      > Sie können maximal 50.000 Einträge aus einer einzigen Audit Log-Suche in einer CSV-Datei herunterladen. Wenn 50.000 Einträge in der CSV-Datei heruntergeladen werden, können Sie wahrscheinlich davon ausgehen, dass es sind mehr als 50.000 Ereignisse, die die Suchkriterien erfüllen. Wenn mehr als diese Grenze exportieren möchten, verwenden Sie einen Datumsbereich zur Reduzierung der Anzahl von Überwachungsprotokolleinträgen. Möglicherweise müssen Sie mehrere Suchvorgänge mit kleineren Datumsbereiche für mehr als 50.000 Einträge exportieren durchgeführt werden.
        

3. Nach der Auswahl einer Exportoption von wird eine Meldung am unteren Rand des Fensters angezeigt, die aufgefordert, öffnen Sie die CSV-Datei, speichern Sie die Downloads-Ordner oder in einen bestimmten Ordner zu speichern

Weitere Informationen zum Anzeigen filtern oder Exportieren von Suchergebnissen aus Audit Log, finden Sie unter [Suchen der Überwachungsprotokolle melden Sie sich bei der Sicherheit in Office 365 & Compliance Center](../search-the-audit-log-in-security-and-compliance.md).