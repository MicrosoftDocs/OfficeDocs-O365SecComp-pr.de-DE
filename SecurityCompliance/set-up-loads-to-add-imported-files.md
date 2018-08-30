---
title: Einrichten von Lasten importierte Dateien in Office 365 erweiterte eDiscovery hinzu
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Überprüfen Sie die Schritte aus, um die letzten definierten laden oder einen Batch von Dateien mit früherer ausführen Relevanz Schulung in Office 365 erweiterte eDiscovery importierte Dateien hinzugefügt.  '
ms.openlocfilehash: 2c986578b969b671351930fd6939a90e3a821dc2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529974"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a>Einrichten von Lasten importierte Dateien in Office 365 erweiterte eDiscovery hinzu

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Im erweiterten eDiscovery ist eine Last einen neuen Batch von Dateien in eine Anfrage hinzugefügt. Standardmäßig wird ein Hardwaregerät definiert und alle importierte Dateien hinzugefügt. Bevor Sie Relevanz Schulungen durchführen, müssen die Last importierte Dateien hinzugefügt werden. 
  
Berücksichtigen Sie die folgenden Szenarien:
  
- Neue Dateien bekanntermaßen ähnlich wie bei der vorherigen Dateien auf die Groß-/Kleinschreibung Datenbank geladen werden, oder der vorherigen Laden der Dateien einer zufällig ausgewählten Satz aus der Auflistung der Datei wurde. Fügen Sie in diesem Fall die importierten Dateien das Laden der aktuellen Datei hinzu.
    
- Neue Dateien unterscheiden sich von vorherigen Unterhaltungen (beispielsweise aus einer anderen Quelle), oder Sie haben keine Vorkenntnisse, dass sie ähnliche oder auf den vorherigen Lasten unterschiedliche sind. Fügen Sie in diesem Szenario die importierten Dateien zu einer neuen Datei laden. Erweiterte eDiscovery dies als einen parallelen Lasten Szenario erkennt, ruft einen Ausgleich Prozess, sperrt Relevanz Schulung und Batch Berechnungen, bis die Ermittlung abgeschlossen ist, und die neue Last integriert und geschult ist. 
    
## <a name="adding-imported-files-to-the-current-load"></a>Importierte Dateien hinzufügen, um die aktuelle Auslastung

Eine Auslastung im erweiterten eDiscovery verarbeitet werden müssen alle importierte Dateien hinzugefügt werden. Importierte Dateien werden die letzten definierten Last hinzugefügt. Wenn Sie später weitere Dateien importieren, müssen sie auch die Last hinzugefügt.
  
1. In der **Relevanz \> Relevanz Setup** **Lasten**wählen Sie Registerkarte.
    
    ![Relevanzeinrichtungslasten (Registerkarte)](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. **Include-Dateien**: Wählen Sie eine Option für Dateien hinzu. In der Standardeinstellung Dateien hinzufügen, um die aktuelle Auslastung der Auffüllung "Alle Dateien" basiert.
    
    > [!TIP]
    > Laden Sie alle verfügbare culled Dateien in Relevanz. Wenn Sie nur eine Teilmenge der verfügbaren Dateien laden möchten, zuerst finden Sie mit der Unterstützung von wie Laden Teilmengen Relevanz Schulung beeinträchtigen kann. 
  
3. Wählen Sie in **Management wird geladen**eine Auslastung.
    
4. Klicken Sie auf **Dateien hinzufügen**. Die Dateien werden an die Last hinzugefügt und ein Bestätigungsdialogfeld wird angezeigt. 
    
5. Klicken Sie auf **OK**.
    
Die Dateien können nun im erweiterten eDiscovery Relevanz für die Dateien Schulung bearbeitet werden.
  
## <a name="editing-a-load-name-within-a-case"></a>Bearbeiten einer Last Name innerhalb einer Anfrage

Wenn die Last Name ändern, wird empfohlen, einen Namen zu verwenden, der an die Groß-/Kleinschreibung relevant ist.
  
1. In der **Relevanz \> Relevanz Setup** **Lasten**wählen Sie Registerkarte.
    
2. Wählen Sie einen, und klicken Sie auf das Symbol **Bearbeiten** , aus der Liste **Lasten Management** . Das Load-Fenster bearbeiten wird angezeigt. 
    
3. Geben Sie die Änderungen, und klicken Sie dann auf **OK**.
    
## <a name="adding-imported-files-to-a-new-load"></a>Importierte Dateien hinzufügen, um ein neues laden

Nach dem Starten Relevanz Schulungen oder Batch Berechnung ausführen, sollten Sie zum Importieren und einen weiteren Satz von Dateien zu verarbeiten. 
  
Bei der Ermittlung können Sie erstellen, markieren und analysieren den Ermittlung Satz. Erweiterte eDiscovery vergleicht seine Bewertung Relevant und nicht Relevant Dateien in die neue Last auf diejenigen in vorherigen wird geladen. Basierend auf den Ergebnissen, werden Sie aufgefordert, Synchronisieren beim treffen Falls erforderlich, und erweiterten eDiscovery Empfehlungen basierend auf den aufgelaufenen Relevanz Informationen bereitstellt. 
  
Paralleles wird geladen, und dieser Funktionalität hängt wie folgt: 
  
- Wenn Sie eine neue Dateilast nach Batch Berechnung importieren, bestimmt erweiterte eDiscovery, inwieweit die Dateien in eine der folgenden Kategorien fallen:
    
  - Ähnlich wie (homogene): ein neues, benutzerdefiniertes Round Relevanz Schulungen ist nicht erforderlich, und die Kenntnisse aus der vorherigen Last aufgelaufene kann angewendet werden "wie gesehen" auf die neue Load. 
    
  - DISTINCT (heterogenen): ein neues, benutzerdefiniertes Round Relevanz Schulungen erforderlich ist und die Kenntnisse aus der vorherigen Last aufgelaufene kann nicht angewendet werden. 
    
    Diese Begriffe beziehen sich auf die Ebene der Ähnlichkeit von Dateien zwischen Lasten und nicht innerhalb der wird geladen. 
    
- Beim Importieren eines neuen Datei laden während der Relevanz Schulung (vor dem Batch Berechnung) kann synchronisieren Sie Relevanz Schulungen auf den Dateisatz united weiter. Erweiterte eDiscovery wird nicht schätzen Sie, ob die neue Last ähnelt oder die vorherige Ladung voneinander ist. Es einfach sammelt Informationen über die neuen Last und ermöglicht die Relevanz Schulungen auf den neuen und vorherigen fortgesetzt von Dateien festgelegt. 
    
- Wenn vorhanden mehrere Probleme in Relevanz Schulung sowie Probleme nach Batch Berechnung sind, wird der Prozess der Ermittlung einmal für alle Probleme ausgeführt, und die Ergebnisse werden berechnet und für jedes Problem angezeigt.
    
> [!NOTE]
> Der Umfang der Stichprobe synchronisieren kann variieren. Es hängt von der Größe der neuen Last relativ zum Laden vorherigen und für die Anzahl der Beispiele, die vor dem Hinzufügen des neuen Laden abgeschlossen. Im Beispiel synchronisieren ist in der Regel eine Reihe von 200 bis 2.000 Dateien aus der neuen laden. 
  
> [!TIP]
> Ermittlung andere Aufgaben beendet und erfordert einzelne Datei markieren und überprüfen. Daher können Sie führt zu mehr Verarbeitungsaufwand reduzieren, wenn Sie neue Dateien in großen Batches hinzufügen. 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a>Lädt ein neue Datei Laden von hervorgehobene und paralleles hinzufügen

1. In der **Relevanz \> Relevanz Setup** **Lasten**wählen Sie Registerkarte.
    
2. Klicken Sie unter **Lasten Management**, klicken Sie auf die **+** Symbol, um eine Auslastung hinzuzufügen. Ein Bestätigungsdialogfeld wird angezeigt. 
    
3. Klicken Sie auf **Ja,** um den Vorgang fortzusetzen. Klicken Sie im Dialogfeld **neue hinzufügen laden** wird angezeigt. 
    
    > [!NOTE]
    > Sie können ein neues Laden nur hinzufügen, wenn Aktionen auf die vorherige Load durchgeführt wurden. 
  
4. Klicken Sie im Dialogfeld **neue hinzufügen laden** Typinformationen in **Laden Name** und **Beschreibung** , und klicken Sie dann auf **OK**. Erweiterte eDiscovery Fügt ein neues laden.
    
5. Klicken Sie auf **Dateien hinzufügen**, um die neue Load-Datei zu importieren. Diese Auslastung werden alle neue Dateien hinzugefügt. Nach dem Import der Dateien erweiterte eDiscovery erkennt das Szenario der parallelen Lasten und synchronisieren im nächsten Schritt angibt.
    
6. Klicken Sie auf **Synchronisieren** Sie unten im Dialogfeld, um das Szenario ausgeführt. 
    
    Ein einzelner Satz zu synchronisieren, in der Regel mit 200 bis 2.000 Dateien aus der neuen Load wird für alle Probleme zum gleichzeitigen Datei tagging zulassen erstellt.
    
    Details dienen, ob Lasten ähnliche oder unterschiedliche sind, gibt an, ob erweiterte eDiscovery zusammenführen oder teilen die Lasten automatisch und Informationen im Hinblick auf Verarbeitung im nächsten Schritt.
    
    Sie können Dateien markieren und führen Sie einen Vorgang berechnen. Die Kategorien Relevanz zu ermitteln, ob Lasten ähnliche oder unterschiedliche sind aktiviert und ermöglicht das Fortsetzen des neuen Satz von Dateien.
    
7. Nach der Ermittlung Satz überprüft werden, anzeigen **Relevanz \> nachverfolgen** für die Ermittlung Ergebnisse. 
    
1. Wenn das Laden der neuen Datei während der Relevanz Schulung hinzugefügt wurde ist eine (d. h., das Problem nicht noch Batch Berechnung durchlaufen hat), **Weiter Schulung** im nächsten Schritt, unabhängig von den Ergebnissen synchronisieren. 
    
    Die neuen und vorherigen geladen werden als ein Hardwaregerät verarbeitet, und Relevanz Schulung in der united Satz fortgesetzt. Sie sind jetzt mit diesem Verfahren abgeschlossen und Relevanz Schulung fortgesetzt. 
    
2. Wenn die neue Auslastung nach Batch Berechnung hinzugefügt wurde, fahren Sie mit den folgenden Schritten.
    
8. Für neue Lasten nach Batch Berechnung hinzugefügt bestimmt die erweiterte eDiscovery ist die neue Last ähnelt oder vom vorherigen geladen wird, wie folgt:
    
1. Lädt ähneln gefunden: keine weiteren Relevanz Schulung erforderlich ist. Das Dashboard zeigt die empfohlenen nächsten Schritt wird ausgeführt ** Berechnung Batch ** erneut aus, um die Relevanz der Ergebnisse für die neue Auslastung berechnen. Lädt gefunden ähnlich, sein, damit die vorherigen Analyse Klassifizierung auf die neuen Dateien ausgeführt werden kann. 
    
2. Wenn Lasten gefunden wurden, eindeutig sein: mehr Relevanz Schulungen erforderlich ist und im nächsten Schritt wird die Entscheidung synchronisieren. Wählen Sie eine Entscheidung Ermittlung wie folgt aus:
    
    Wenn Sie **Zusammenführen Lasten**auswählen, werden erweiterte eDiscovery vorherige und neue Lasten für die Schulung ein miteinander verbunden. Obwohl die erstmalige laden durchlaufen Batch Berechnung haben, ist Weitere Schulungen erforderlich. Schulung von neuen und vorherigen Lasten zusammen fortgesetzt werden. Batch Berechnung wird dann erneut ausführen und die Ergebnisse der vorherigen Batch Berechnung ignoriert werden soll. Wählen Sie die Auswahl dieser Option, wenn Relevanz Bewertungen für vorhandenen Lasten, beispielsweise neu berechnet werden können bei der Überprüfung der vorhandenen Datei Lasten nicht gestartet wurde.
    
    Wenn Sie **geteilte lädt**auswählen, Relevanz Schulung nur auf die neue Last weiter aus. In diesem Fall werden vorherige Batch Berechnung Bewertungen bleiben unverändert. Wählen Sie diese Option bei vorhandene Relevanz Bewertungen für vorhandenen Lasten, beispielsweise nicht neu berechnet wird, wenn die Überprüfung der vorhandenen Lasten bereits gestartet wurde. Relevanz Bewertungen von diesem Punkt an separat verwaltet werden und können nicht zusammengeführt werden.
    
3. Klicken Sie auf **Weiter Schulung**.
    
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Definieren von Problemen und Zuweisen von Benutzern](define-issues-and-assign-users.md)
  
[Schlüsselwörter hervorgehoben definieren und erweiterte Optionen](define-highlighted-keywords-and-advanced-options.md)

