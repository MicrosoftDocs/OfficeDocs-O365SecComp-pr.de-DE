---
title: Einrichten von Lasten zum Hinzufügen von importierten Dateien in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Lesen Sie die Schritte zum Hinzufügen von importierten Dateien zur zuletzt definierten Last oder zum letzten Batch von Dateien, bevor Sie die Relevanz-Schulung in Office 365 Advanced eDiscovery ausführen.  '
ms.openlocfilehash: 8c5101628b468719f8aa4f81a4c73cbbb226105f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215985"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a>Einrichten von Lasten zum Hinzufügen von importierten Dateien in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In Advanced eDiscovery ist eine Auslastung ein neuer Batch von Dateien, die zu einem Fall hinzugefügt werden. Standardmäßig wird eine Auslastung definiert, und alle importierten Dateien werden ihr hinzugefügt. Vor der Durchführung der Relevanz-Schulung müssen importierte Dateien der Belastung hinzugefügt werden. 
  
Berücksichtigen Sie die folgenden Szenarien:
  
- Neue Dateien sind bekanntermaßen vergleichbar mit den vorherigen Dateien, die in die Case-Datenbank geladen wurden, oder die frühere Datei Last war ein Zufalls Satz aus der file-Auflistung. Fügen Sie in dieser Instanz die importierten Dateien der aktuellen Datei Auslastung hinzu.
    
- Neue Dateien unterscheiden sich von den vorherigen (beispielsweise aus einer anderen Quelle), oder Sie haben keine Vorkenntnisse, dass Sie ähnlich oder unterschiedlich zu den vorherigen Lasten sind. Fügen Sie in diesem Szenario die importierten Dateien einem neuen Datei Ladevorgang hinzu. Advanced eDiscovery erkennt dies als Roll laden Szenario, Ruft einen Aufholprozess ab, sperrt Relevanz Schulungen und Batch Berechnungen, bis das Catch-up abgeschlossen ist, und die neue Last ist integriert und geschult. 
    
## <a name="adding-imported-files-to-the-current-load"></a>Hinzufügen von importierten Dateien zur aktuellen Auslastung

Alle importierten Dateien müssen zu einer zu verarbeitenden Ladung in Advanced eDiscovery hinzugefügt werden. Importierte Dateien werden der zuletzt definierten Last hinzugefügt. Wenn Sie später weitere Dateien importieren, müssen Sie auch der Lade hinzugefügt werden.
  
1. Wählen Sie auf der Registerkarte **Relevanz \> Relevanz Setup** die Option **Lasten**aus.
    
    ![Relevanzeinrichtungslasten (Registerkarte)](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. **Include Files**: Wählen Sie eine Option für die einzuschließenden Dateien aus. Das Hinzufügen von Dateien zur aktuellen Auslastung basiert standardmäßig auf der Auffüllung "alle Dateien".
    
    > [!TIP]
    > Laden Sie alle verfügbaren gekeulten Dateien in Relevanz. Wenn Sie nur eine Teilmenge der verfügbaren Dateien laden möchten, konsultieren Sie zunächst den Support, da das Laden von Teilmengen sich negativ auf die Relevanz-Schulung auswirken kann. 
  
3. Wählen Sie unter **Lasten Verwaltung**eine Last aus.
    
4. Klicken Sie auf **Dateien hinzufügen**. Die Dateien werden dem Ladevorgang hinzugefügt, und eine Bestätigungsmeldung wird angezeigt. 
    
5. Klicken Sie auf **OK**.
    
Die Dateien können nun in Advanced eDiscovery-Relevanz für das Training der Dateien verarbeitet werden.
  
## <a name="editing-a-load-name-within-a-case"></a>Bearbeiten eines Lade namens in einem Fall

Wenn Sie den ladenamen ändern, empfiehlt es sich, einen für den Fall bedeutsamen Namen zu verwenden.
  
1. Wählen Sie auf der Registerkarte **Relevanz \> Relevanz Setup** die Option **Lasten**aus.
    
2. Wählen Sie in der Liste **Lasten Verwaltung** eine Lade aus, und klicken Sie auf das Symbol **Bearbeiten** . Das fensterladen bearbeiten wird angezeigt. 
    
3. Geben Sie die Änderungen ein, und klicken Sie dann auf **OK**.
    
## <a name="adding-imported-files-to-a-new-load"></a>Hinzufügen von importierten Dateien zu einer neuen Ladung

Nachdem Sie das Relevanz-Training gestartet oder die Batch Berechnung ausgeführt haben, können Sie einen zusätzlichen Satz von Dateien importieren und verarbeiten. 
  
Während des catch-up können Sie den catch-up-Satz erstellen, taggen und analysieren. Advanced eDiscovery vergleicht die Bewertung relevanter und nicht relevanter Dateien in der neuen Last mit denen in früheren Lasten. Basierend auf den Ergebnissen werden Sie aufgefordert, ggf. Nachhol Entscheidungen vorzunehmen, und erweiterte eDiscovery bietet Empfehlungen basierend auf den gesammelten Relevanzinformationen. 
  
Die Roll laden und die Catch-up-Funktionalität unterscheiden sich wie folgt: 
  
- Wenn Sie eine neue Datei Auslastung nach der Batch Berechnung importieren, bestimmt Advanced eDiscovery, in welchem Umfang die Dateien in eine der folgenden Kategorien fallen:
    
  - Ähnlich (homogen): eine neue, benutzerdefinierte Round-of-Relevance-Schulung ist nicht erforderlich, und das von der vorherigen Auslastung erworbene Wissen kann auf die neue Belastung angewendet werden. 
    
  - Distinct (heterogenes): eine neue, benutzerdefinierte Round-of-Relevance-Schulung ist erforderlich, und das vom vorherigen Laden erworbene Wissen kann nicht angewendet werden. 
    
    Diese Begriffe beziehen sich auf den Grad der Ähnlichkeit von Dateien zwischen Lasten und nicht innerhalb der Lasten. 
    
- Beim Importieren eines neuen Datei Ladevorgangs während des Relevanz-Trainings (vor der Batch Berechnung) können Sie die Relevanz-Schulung im United-Dateisatz fortsetzen. Erweiterte eDiscovery schätzt nicht, ob die neue Auslastung der vorherigen Belastung ähnelt oder nicht. Sie sammelt lediglich Informationen über die neue Auslastung und ermöglicht die Fortsetzung der Relevanz-Schulung für die neuen und früheren Dateigruppen. 
    
- Wenn mehrere Probleme in Relevanz und Probleme nach der Batch Berechnung auftreten, wird der Aufholprozess für alle Probleme einmal ausgeführt, und die Ergebnisse werden für jedes Problem berechnet und angezeigt.
    
> [!NOTE]
> Die Größe des catch-up-Beispiels kann variieren. Es hängt von der Größe der neuen Last im Verhältnis zu den vorherigen Lasten und der Anzahl der vor dem Hinzufügen der neuen Last abgeschlossenen Beispiele ab. Das Catch-up-Beispiel ist in der Regel eine Reihe von 200 bis 2.000-Dateien aus der neuen Lade. 
  
> [!TIP]
> Catch-up beendet alle anderen Aufgaben und erfordert einzelne Dateikennzeichnung und-Überprüfungen. Daher können Sie den Aufwand reduzieren, wenn Sie neue Dateien in größeren Batches hinzufügen. 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a>Hinzufügen einer neuen Datei Last mit catch-up und Rolling Loads

1. Wählen Sie auf der Registerkarte **Relevanz \> Relevanz Setup** die Option **Lasten**aus.
    
2. Klicken Sie unter **Lasten Verwaltung**auf **+** das Symbol, um eine Last hinzuzufügen. Eine Bestätigungsmeldung wird angezeigt. 
    
3. Klicken Sie auf **Ja** , um fortzufahren. Das Dialogfeld **neuen Ladevorgang hinzufügen** wird angezeigt. 
    
    > [!NOTE]
    > Sie können nur dann eine neue Ladung hinzufügen, wenn Aktionen zur vorherigen Belastung ausgeführt wurden. 
  
4. Geben Sie im Dialogfeld **neuen Ladevorgang hinzufügen** Informationen in **Laden Name** und **Beschreibung** ein, und klicken Sie dann auf **OK**. Advanced eDiscovery fügt eine neue Auslastung hinzu.
    
5. Klicken Sie auf **Dateien hinzufügen**, um die neue Ladedatei zu importieren. Alle neuen Dateien werden dieser Belastung hinzugefügt. Nachdem die Dateien von Advanced eDiscovery importiert wurden, erkennt es das Szenario "Rolling Loads" und zeigt als nächster Schritt catch-up an.
    
6. Klicken Sie unten im Dialogfeld auf **catch-up** , um das Szenario auszuführen. 
    
    Ein einzelner catch-up-Satz, der normalerweise 200 bis 2.000-Dateien aus der neuen Lade enthält, wird für alle Probleme erstellt, um die gleichzeitige Dateikennzeichnung zu ermöglichen.
    
    Details dazu, ob Lasten ähnlich oder unterschiedlich sind, ob Advanced eDiscovery die Lasten automatisch zusammengeführt oder geteilt hat, sowie Informationen zur Verarbeitung im nächsten Schritt.
    
    Anschließend können Sie Dateien markieren und einen Berechnungsvorgang ausführen. Das Tagging ermöglicht die Relevanz, um zu bestimmen, ob Lasten ähnlich oder unterschiedlich sind, und ermöglicht es Ihnen, weiterhin an den neuen Dateien zu arbeiten.
    
7. Nach der Überprüfung des catch-up-Satzes zeigen Sie die **Relevanz \> -Spur** für die Catch-up-Ergebnisse an. 
    
1. Wenn die neue Datei Auslastung während des Relevance-Trainings hinzugefügt wurde (was bedeutet, dass das Problem noch nicht durch die Batch Berechnung durchgeführt wurde), ist die **Weiterbildung** der nächste Schritt, unabhängig von den catch-up-Ergebnissen. 
    
    Die neue und frühere Lasten werden verarbeitet, während eine Last-und Relevanz-Schulung auf dem United-Set fortgesetzt wird. Sie sind jetzt fertig mit diesem Verfahren und können die Relevanz-Schulung fortsetzen. 
    
2. Wenn die neue Ladung nach der Batch Berechnung hinzugefügt wurde, führen Sie die folgenden Schritte aus.
    
8. Für neue Lasten, die nach der Batch Berechnung hinzugefügt werden, bestimmt Advanced eDiscovery, ob die neue Last ähnlich oder unterscheidet sich von früheren Lasten wie folgt:
    
1. Wenn Lasten ähnlich sind, ist keine zusätzliche Relevanz erforderlich. Im Dashboard wird der Empfohlene nächste Schritt angezeigt: * * Batch Berechnung * * erneut ausführen, um die Relevanz für die neue Auslastung zu berechnen. Es wurde festgestellt, dass Lasten ähnlich sind, sodass die frühere Klassifizierungsanalyse für die neuen Dateien ausgeführt werden kann. 
    
2. Wenn Lasten unterschiedlich festgestellt wurden: mehr Relevanz Training ist erforderlich, und der nächste Schritt ist catch-up Entscheidung. Wählen Sie eine Aufhol Entscheidung wie folgt aus:
    
    Wenn Sie **Lasten zusammenführen**auswählen, werden von Advanced eDiscovery frühere und neue Lasten für den Trainingssatz zusammengeführt. Obwohl der erste Ladevorgang die Batch Berechnung durchführte, ist mehr Schulung erforderlich. Trainieren Sie neue und frühere Lasten zusammen. Die Batch Berechnung wird dann erneut ausgeführt, und die vorherigen Batch Berechnungsergebnisse sollten ignoriert werden. Wählen Sie diese Option aus, wenn die Relevanz für vorhandene Lasten neu berechnet werden kann, beispielsweise wenn die Überprüfungen vorhandener Datei Lasten nicht gestartet wurden.
    
    Wenn Sie geTeilte **Lasten**auswählen, wird die Relevanz-Schulung nur für die neue Last fortgesetzt. In dieser Instanz bleiben frühere Batch Berechnungsergebnisse unverändert. Wählen Sie diese Option aus, wenn vorhandene Relevanzwerte für vorhandene Lasten nicht neu berechnet werden können, beispielsweise wenn die Überprüfungen vorhandener Lasten bereits begonnen haben. Relevanz-Ergebnisse werden ab diesem Zeitpunkt separat verwaltet und können nicht zusammengeführt werden.
    
3. Klicken Sie auf **Training fortfahren**.
    
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Definieren von Problemen und Zuweisen von Benutzern](define-issues-and-assign-users.md)
  
[Definieren hervorgehobener Schlüsselwörter und erweiterte Optionen](define-highlighted-keywords-and-advanced-options.md)

