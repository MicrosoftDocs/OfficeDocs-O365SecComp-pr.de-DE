---
title: Erstellen und Anwenden von Informationsverwaltungsrichtlinien
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/16/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 8ccac9e4-3a50-49fa-a95b-d186032a6ee3
description: Informationsverwaltungsrichtlinien können Ihrer Organisation beibehalten werden Inhalte, überwachen, was Personen mit Inhalten werden, und Hinzufügen von Barcodes, wie lange Steuerelement oder Etiketten auf Dokumente. Eine Richtlinie kann mit rechtlichen und behördlichen Regelungen oder interner Geschäftsprozesse Durchsetzung helfen. Als Administrator können Sie eine Richtlinie festlegen, steuern, wie die Dokumente überwachen und wie lange Dokumente aufbewahrt.
ms.openlocfilehash: cc15b7d830e6c13e00045f7e4b672ac4a755a70e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529137"
---
# <a name="create-and-apply-information-management-policies"></a>Erstellen und Anwenden von Informationsverwaltungsrichtlinien

Informationsverwaltungsrichtlinien können Ihrer Organisation beibehalten werden Inhalte, überwachen, was Personen mit Inhalten werden, und Hinzufügen von Barcodes, wie lange Steuerelement oder Etiketten auf Dokumente. Eine Richtlinie kann mit rechtlichen und behördlichen Regelungen oder interner Geschäftsprozesse Durchsetzung helfen. Als Administrator können Sie eine Richtlinie festlegen, steuern, wie die Dokumente überwachen und wie lange Dokumente aufbewahrt.
  
Sie können eine Informationen Management Policy können an drei unterschiedlichen Standorten in der Websitehierarchie aus der größte erstellen, der schmalste:
  
- Erstellen Sie eine Richtlinie auf mehrere Inhaltstypen innerhalb einer Websitesammlung verwenden.
    
- Erstellen Sie eine Richtlinie für einen Inhaltstyp für die Website.
    
- Erstellen Sie eine Richtlinie für eine Liste oder Bibliothek.
    
Weitere Informationen finden Sie unter [Einführung in Informationsverwaltungsrichtlinien](intro-to-info-mgmt-policies.md).
  
## <a name="create-a-policy-for-multiple-content-types-within-a-site-collection"></a>Erstellen Sie eine Richtlinie für mehrere Inhaltstypen innerhalb einer Websitesammlung
<a name="__toc261001590"> </a>

Um sicherzustellen, dass eine Informationsrichtlinie für alle Dokumente eines bestimmten Typs innerhalb einer Websitesammlung angewendet wird, sollten Sie die Richtlinie auf der Ebene der Websitesammlung zu erstellen und dann später wenden Sie die Richtlinie auf Inhaltstypen an. Diese werden als Auflistung von Standortrichtlinien bezeichnet. 
  
1. Klicken Sie auf der Homepage der Websitesammlung \> **Einstellungen**![SharePoint 2016 Einstellungen-Schaltfläche auf der Titelleiste angezeigt. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Websiteeinstellungen**.
    
    Klicken Sie in einer SharePoint-Gruppe verbundenen Website auf **Einstellungen**, klicken Sie auf **Websiteinhalte**, und klicken Sie dann auf **Websiteeinstellungen**. 
    
2. Klicken Sie auf der Seite Websiteeinstellungen unter **Websitesammlungsverwaltung** \> **Content Type Richtlinienvorlagen**. 
  
![Verknüpfung mit Inhalt Typ Richtlinienvorlage auf der Seite Websiteeinstellungen](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Auf der Seite Richtlinien \> **Erstellen**. 
    
4. Geben Sie einen Namen und eine Beschreibung für die Richtlinie ein, und Schreiben Sie eine kurze richtlinienanweisung, die Benutzern erklärt, was für die Richtlinie ist.
    
5. Finden Sie im nächsten Abschnitt zum Erstellen von Richtlinien zu einem Websiteinhaltstyp zu erfahren, wie die Features einzurichten, den Sie der Richtlinie zuordnen möchten. 
    
6. Wählen Sie **OK** aus.
    
## <a name="create-a-policy-for-a-site-content-type"></a>Erstellen Sie eine Richtlinie für einen Websiteinhaltstyp
<a name="__create_a_policy"> </a>

Hinzufügen einer Informationsverwaltungsrichtlinie zu einem Inhaltstyp erleichtert Richtlinienfeatures mit mehreren Listen oder Bibliotheken zuordnen. Sie können auch eine vorhandene Informationsverwaltungsrichtlinie zu einem Inhaltstyp hinzufügen, oder erstellen Sie eine eigene Richtlinie speziell für einen einzelnen Inhaltstyp.
  
 Sie können auch eine Informationsverwaltungsrichtlinie zu einem Inhaltstyp hinzufügen, die spezifisch für Listen ist. Dies ist die Anwendung der Richtlinie nur für Elemente in dieser Liste, die den Inhaltstyp verwenden. 
  
1. Klicken Sie auf der Homepage der Websitesammlung \> **Einstellungen**![SharePoint 2016 Einstellungen-Schaltfläche auf der Titelleiste angezeigt. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Websiteeinstellungen**.
    
    Klicken Sie in einer SharePoint-Gruppe verbundenen Website auf **Einstellungen**, klicken Sie auf **Websiteinhalte**, und klicken Sie dann auf **Websiteeinstellungen**. 
    
2. Klicken Sie auf der Seite Websiteeinstellungen unter **Web-Designer-Kataloge** \> **Websiteinhaltstypen**.
  
![Website-Inhaltstypen Link auf der Seite Websiteeinstellungen](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
3. Wählen Sie auf der Seite Website Einstellungen für den Inhaltstyp, dem Sie eine Richtlinie hinzufügen möchten.
    
4. Klicken Sie auf der Seite Websiteinhaltstyp unter **Einstellungen** \> **Information Management Policy Settings**.
    
5. Geben Sie einen Namen und eine Beschreibung für die Richtlinie, und Schreiben Sie eine kurze Beschreibung, die Benutzern erklärt, was für die Richtlinie ist, klicken Sie auf der Seite Richtlinie bearbeiten.
    
6. Wählen Sie in den nächsten Abschnitten die einzelnen Richtlinienfeatures, die Sie zu Ihrer Informationsverwaltungsrichtlinie hinzufügen möchten. 
  
![Typen von Inhaltsrichtlinien](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
7. Klicken Sie zum Angeben eines Beibehaltungszeitraums für Dokumente und Elemente, für die diese Richtlinie gilt, wählen Sie die **Archivierung aktivieren**, und geben Sie den Beibehaltungszeitraum und die Aktionen, die auftreten, wenn die Elemente ablaufen soll.
    
    Um eine Aufbewahrungsdauer anzugeben
    
||||||**1.**|** Wählen Sie ** fügen Sie eine Aufbewahrungsphase für Datensätze... ***|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> | Wählen Sie eine Retention Period Option an, wann Dokumente oder Elemente an, die ablaufen festgelegt sind. Führen Sie eine der folgenden Aktionen aus:<br/>  So legen Sie das Ablaufdatum basierend auf ein Date-Eigenschaft unter **Ereignis** fest \> **Diese Stufe basiert auf ein Date-Eigenschaft für das Element**, und wählen Sie dann das Dokument oder Element Aktion (beispielsweise erstellt oder geändert) und Schrittweite für die Zeit nach dieser Aktion () beispielsweise die Anzahl der Tage, Monate oder Jahre) Wenn das Element an, die ablaufen soll.  <br/>  Um eine benutzerdefinierte Beibehaltungsformel verwenden den um Ablauf zu ermitteln, wählen Sie **nach einer benutzerdefinierten Aufbewahrung Formel auf diesem Server installiert**.  <br/> > [!NOTE]> Diese Option ist nur verfügbar, wenn eine benutzerdefinierte Formel von Ihrem Administrator eingerichtet wurde.           |
||||||3.  <br/> |Die Option **Starten eines Workflows** ist nur verfügbar, wenn Sie eine Richtlinie für eine Liste, Bibliothek oder einem Inhaltstyp einen, die bereits von einem Workflow zugeordnet definieren. Sie werden dann Wahl des Workflows zur Auswahl zugewiesen.<br/> |
||||||4.  <br/> |Wählen Sie im Abschnitt **Serie** **Wiederholen Sie diese Stufe Aktion...** und geben Sie, wie oft die Aktion, die wiederholt werden soll.  <br/> > [!NOTE]> Diese Option ist nur verfügbar, wenn die Aktion gewählte wiederholt werden kann. Beispielsweise können nicht Sie Serie für die Aktion **Endgültig löschen**festgelegt.           |
||||||5.  <br/> |Wählen Sie **OK**.  <br/> |
   
1. Zum Aktivieren der Überwachung für die Dokumente und Elemente, für die diese Richtlinie gilt, wählen Sie **Überwachung aktivieren**aus, und geben Sie die Ereignisse, den, die Sie überwachen möchten.
    
    Aktivieren der Überwachung
    
||||||1. * ist **|Klicken Sie auf der Seite Richtlinie bearbeiten ** **unter** **Überwachung** **\>** **Aktivieren der Überwachung** **, und wählen Sie dann die Kontrollkästchen neben den Ereignissen, die eine Überwachung bleiben sollen nachfolgende for.* **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |**Um Benutzern das Einfügen dieser Barcodes in Dokumente aufzufordern** **Wählen Sie aus** **Benutzer auffordern, vor dem Speichern oder Drucken einen Barcode hinzuzufügen** **.** <br/> |
||||||**3.** <br/> |**Wählen Sie aus** **OK** ** das Überwachungsfeature auf die Richtlinie anwenden. ** <br/> |
|||||||Das Überwachung Richtlinienfeature kann Organisationen zum Erstellen und Analysieren von Prüflisten für Dokumente und Listenelemente wie Aufgabenlisten, Problemlisten, Diskussionsgruppen und Kalender. Dieses Richtlinienfeature bietet ein Überwachungsprotokoll, die Ereignisse aufzeichnet, beispielsweise wenn Inhalte angezeigt, bearbeitet oder gelöscht wird.  <br/> |
|||||||Wenn die Überwachung als Teil einer Informationsverwaltungsrichtlinie aktiviert ist, können Administratoren die Überwachungsdaten in Berichte zur Richtlinienverwendung anzeigen, die in Microsoft Excel basieren und die derzeitige Verwendung zusammenfassen. Administratoren können diese Berichte verwenden, um zu bestimmen, wie Informationen innerhalb der Organisation verwendet wird. Diese Berichte können Organisationen überprüfen und deren Einhaltung von Vorschriften zu dokumentieren oder potenzielle Probleme zu untersuchen auch helfen.  <br/> |
|||||||Im Überwachungsprotokoll werden folgende Informationen aufgezeichnet: Ereignisname, Datum und Uhrzeit des Ereignisses sowie der Systemname des Benutzers, der die Aktion ausgeführt hat.  <br/> |
   
1. Wenn Barcodes als Teil einer Richtlinie aktiviert sind, werden sie Dokumenteigenschaften hinzugefügt und im Kopfbereich des Dokuments auf den Barcode angewendet wird angezeigt. Wie Etiketten kann Barcodes auch manuell aus einem Dokument entfernt werden. Sie können angeben, ob Benutzer aufgefordert sollten, den Barcode beim Drucken oder Speichern eines Elements enthalten oder wenn der Barcode manuell eingefügt werden soll mit der Registerkarte **Einfügen** in 2010 Office release Programme. 
    
    Barcodes aktivieren
    
||||||1. * ist **|**Klicken Sie auf der Seite Richtlinie bearbeiten unter **Barcodes** \> **Barcodes aktivieren**.**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |Um Benutzern das Einfügen dieser Barcodes in Dokumente aufzufordern, wählen Sie **Benutzer auffordern, vor dem Speichern oder Drucken einen Barcode hinzuzufügen**.  <br/> |
||||||**3.** <br/> |Wählen Sie **OK** , um die Barcode-Funktion auf die Richtlinie angewendet werden soll.  <br/> |
|||||||
 Die Barcoderichtlinie generiert Code 39 standard Barcodes. Jedes Barcode-Abbild enthält Text unterhalb der Barcode-Symbol, das den Barcodewert darstellt. Auf diese Weise können die Barcodedaten verwendet werden, auch wenn die Überprüfung der Hardware nicht verfügbar ist. Benutzer können die Anzahl der Barcode manuell in das Suchfeld auf das Element auf einer Website suchen eingeben.  <br/> |
   
1. Wenn Dokumente, für die diese Richtlinie gilt, Bezeichnungen sein muss, wählen Sie **Bezeichnungen aktivieren**, und geben Sie die Einstellungen, die Sie für die Beschriftungen verwenden möchten.
    
    So aktivieren Sie Etiketten
    
||||||**1.**|** Erforderlich, um Benutzer zu einem Dokument eine Bezeichnung hinzufügen wählen Sie **Benutzer auffordern, vor dem Speichern oder Drucken eine Bezeichnung einzufügen**.  <br/> > [!NOTE]> Wenn Bezeichnungen optional sein soll, aktivieren Sie dieses Kontrollkästchen nicht.        **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> |Um eine Bezeichnung zu sperren, damit sie nach dem Einfügen nicht geändert werden kann, wählen Sie **verhindert, dass Änderungen an Bezeichnungen nach dem aufgenommen werden**.  <br/>  Diese Einstellung wird verhindert, dass das Text im Bezeichnungsfeld aktualisieren, sobald die Bezeichnung in ein Element innerhalb einer Clientanwendung wie Word, Excel oder PowerPoint eingefügt wurde. Wenn die Bezeichnung aktualisiert werden, wenn die Eigenschaften für dieses Dokument oder Element aktualisiert werden soll, aktivieren Sie dieses Kontrollkästchen nicht.<br/> |
||||||3.  <br/> |Geben Sie im Feld Bezeichnungsformat den Text für die Bezeichnung angezeigt werden soll. Etiketten können bis zu 10 Spaltenverweise, enthalten, von die jedes bis zu 255 Zeichen lang sein kann. Führen Sie folgende Schritte aus, um das Format für die Bezeichnung zu erstellen:  <br/> Geben Sie die Namen der Spalten, die Sie zum Einschließen in die Bezeichnung in der Reihenfolge, in dem Sie angezeigt werden sollen. Setzen Sie die Spaltennamen in geschweiften Klammern ({}), wie im Beispiel auf der Seite Richtlinie bearbeiten.  <br/> Geben Sie Wörter, um die Spalten außerhalb der Klammern zu identifizieren, wie im Beispiel auf der Seite Richtlinie bearbeiten.  <br/> |
||||||4.  <br/> |Geben Sie zum Hinzufügen eines Zeilenumbruchs **\n** , wo den Zeilenumbruch angezeigt werden soll.  <br/> |
||||||5.  <br/> |Wählen Sie den Schriftgrad und die Formatvorlage, die Sie möchten, und geben an, ob Sie möchten, dass die Bezeichnung links, zentriert oder rechts innerhalb des Dokuments positioniert.  <br/>  Wählen Sie eine Schriftart und Formatvorlage, die auf den Computern der Benutzer verfügbar sind. Der Schriftgrad wirkt sich auf wie viel Text auf dem Etikett angezeigt werden kann.  <br/> |
||||||6.  <br/> |Geben Sie die Höhe und Breite der Beschriftung. Die Bezeichnungsgröße kann im Bereich von.25 Zoll bis 20 Zoll und die Breite der Beschriftung kann im Bereich von.25 Zoll bis 20 Zoll. Text im Bezeichnungsfeld wird die Beschriftung Image immer vertikal zentriert.  <br/> |
||||||7.  <br/> |Wählen Sie für die Vorschau des Inhalts für die Bezeichnung **zu aktualisieren** .  <br/> |
   
1. Wählen Sie **OK** aus.
    
## <a name="create-a-policy-for-a-list-library-or-folder-location-based-retention-policy"></a>Erstellen einer Richtlinie für eine Liste, Bibliothek oder einen Ordner (standortbasierte Aufbewahrungsrichtlinie)
<a name="__create_a_policy"> </a>

Sie können eine Aufbewahrungsrichtlinie zu definieren, die nur für eine bestimmte Liste, Bibliothek oder einen Ordner gilt. Wenn Sie eine Aufbewahrungsrichtlinie auf diese Weise erstellen, jedoch können nicht Sie diese Richtlinie auf einer anderen Listen, Bibliotheken, Ordner oder Websites wiederverwenden, und Websitesammlungsrichtlinie nicht möglich Zuweisen einer ortungsrichtlinie basierend.
  
Wenn Sie eine einzelne Aufbewahrungsrichtlinie auf alle Arten von Inhalten an einer zentralen Stelle anwenden möchten, möchten Sie wahrscheinlich standortbasierte Aufbewahrungsrichtlinie zu verwenden. In den meisten Fällen sollten Sie sicherstellen, dass eine Aufbewahrungsrichtlinie für alle Inhaltstypen angegeben ist.
  
 Jeder Unterordner erbt die Aufbewahrungsrichtlinie des übergeordneten, es sei denn, Sie Unterbrechen der Vererbung und definieren Sie eine neue Aufbewahrungsrichtlinie auf der untergeordneten Ebene. 
  
Wenn Sie eine Informationsverwaltungsrichtlinie als Aufbewahrungsrichtlinie auf eine Liste oder Bibliothek definieren möchten, müssen Sie eine Informationsverwaltungsrichtlinie für jeden einzelnen Listeninhaltstyp, das dieser Liste oder Bibliothek zugeordnet zu definieren.
  
 Wenn an einer beliebigen Stelle Sie beschließen, von der Inhaltstyp speicherortbasierte Richtlinien für eine Liste oder Bibliothek wechseln, werden nur die Aufbewahrungsrichtlinie als Richtlinie speicherortbasierte verwendet werden. Alle anderen Informationsverwaltungsrichtlinien (Überwachungen, Barcodes und Barcodes) werden von der zugeordneten Inhaltstypen geerbt werden. 
  
 Grundlage Standortrichtlinien können durch Deaktivieren des Features Bibliothek und Ordner basierte Aufbewahrung für eine Websitesammlung deaktiviert werden. Dies ermöglicht Websitesammlungsadministratoren, um sicherzustellen, dass ihre Inhaltstyprichtlinien durch basierend Standortrichtlinien ein Liste-Administrator nicht überschrieben werden. 
  
Sie benötigen mindestens die Berechtigung Listen verwalten, um die Informationen Einstellungen für die Informationsverwaltungsrichtlinie für eine Liste oder Bibliothek ändern.
  
1. Navigieren Sie zu der Liste oder Bibliothek, für die Sie eine Informationsverwaltungsrichtlinie angeben möchten. 
    
2. Wählen Sie auf dem Menüband die Registerkarte **Bibliothek** oder **Liste** \> **Bibliothekeinstellungen** oder **Listeneinstellungen**.
    
    Klicken Sie in SharePoint Online auf **Einstellungen** , und klicken Sie dann auf **listeneinstellungen** oder **bibliothekeinstellungen**. 
    
3. Klicken Sie unter **Berechtigungen und Verwaltung** \> **Information Management Policy Settings**.
  
![Informationslink Management Richtlinien auf der Einstellungsseite für die Dokumentbibliothek](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Klicken Sie auf der Seite Einstellungen für die Informationsverwaltungsrichtlinie Informationen stellen Sie sicher, dass die Quelle der Aufbewahrung für die Liste oder Bibliothek auf Bibliothek und Ordner festgelegt wird. 
  
Wenn als Quelle **Inhaltstyp** angezeigt wird, klicken Sie auf **Quelle ändern**, und klicken Sie dann auf **Bibliothek und Ordner**. Sie werden benachrichtigt, dass die Inhaltstyp-Aufbewahrungsrichtlinien ignoriert werden. Wählen Sie **OK**. 
    
5. Klicken Sie auf der Seite Richtlinie bearbeiten unter **Bibliothek basierend Aufbewahrungszeitplan**Geben Sie eine kurze Beschreibung für die Richtlinie, die Sie erstellen. 
    
6. Wählen Sie **Hinzufügen einer Aufbewahrungsrichtlinie Phase...**
    
     Beachten Sie, dass unter Datensätze Sie auswählen können, um unterschiedliche Aufbewahrungsrichtlinien für Datensätze zu definieren, indem Sie die Phasen definieren unterschiedliche Aufbewahrungsrichtlinien für Datensätze Option auswählen. 
    
7. Wählen Sie im Dialogfeld Eigenschaften Stufe eine Period Retention-Option, um anzugeben, wann Dokumente oder Elemente an, die ablaufen festgelegt sind. Führen Sie eine der folgenden Aktionen aus:
    
  - So legen Sie das Ablaufdatum basierend auf ein Date-Eigenschaft unter **Ereignis** fest \> **Diese Stufe basiert auf ein Date-Eigenschaft für das Element**, und wählen Sie dann das Dokument oder Element Aktion (beispielsweise erstellt oder geändert) und Schrittweite für die Zeit nach dieser Aktion () beispielsweise die Anzahl der Tage, Monate oder Jahre) Wenn das Element an, die ablaufen soll. 
    
  - Um eine benutzerdefinierte Beibehaltungsformel verwenden den um Ablauf zu ermitteln, wählen Sie **nach einer benutzerdefinierten Aufbewahrung Formel auf diesem Server installiert**. 
    
    > [!NOTE]
    >  Diese Option ist nur verfügbar, wenn eine benutzerdefinierte Formel von Ihrem Administrator eingerichtet wurde. 
  
  - Geben Sie unter **Aktion**an, was geschieht, wenn das Dokument oder Element läuft ab. Um eine bestimmte Aktion geschieht mit dem Dokument oder Element (z. B. löschen) aktivieren möchten, wählen Sie eine Aktion aus der Liste aus. 
    
8. Die Option **Starten eines Workflows** ist nur verfügbar, wenn Sie eine Richtlinie für eine Liste, Bibliothek oder einem Inhaltstyp einen, die bereits von einem Workflow zugeordnet definieren. Sie werden dann Wahl des Workflows zur Auswahl zugewiesen. 
    
9. Wählen Sie unter **Serie** **Wiederholen Sie diese Stufe Aktion...** und geben Sie, wie oft die Aktion, die wiederholt werden soll. 
    
    > [!NOTE]
    >  Diese Option ist nur verfügbar, wenn die Aktion gewählte wiederholt werden kann. Beispielsweise können nicht Sie Serie für die Aktion **Endgültig löschen**festgelegt. 
  
10. Wählen Sie **OK** aus.
    
## <a name="apply-a-site-collection-policy-to-a-content-type"></a>Anwenden einer Websitesammlungsrichtlinie zu einem Inhaltstyp
<a name="__apply_a_site"> </a>

Wenn Informationsverwaltungsrichtlinien bereits für Ihre Website als Auflistung von Standortrichtlinien erstellt wurden, können Sie eine der Richtlinien zu einem Inhaltstyp anwenden. Auf diese Weise können Sie die gleiche Richtlinie auf mehrere Inhaltstypen in einer Websitesammlung anwenden, die nicht den gleichen übergeordneten Inhaltstyp gemeinsam verwenden.
  
 Wenn Sie mehrere Inhaltstypen in einer Websitesammlung Richtlinien zuweisen möchten und Sie einen verwalteten Metadatendienst konfiguriert haben, können Sie Sie veröffentlichen Inhalt Typ Publishing Richtlinien Informationsmanagement zu mehreren Websitesammlungen. Siehe Abschnitt [Anwenden einer Richtlinie Inhaltstypen in allen Websitesammlungen](create-info-mgmt-policies.md#__apply_a_policy) für Weitere Informationen. 
  
1. Navigieren Sie zu der Liste oder Bibliothek, die den Inhaltstyp enthält eine Richtlinie angewendet werden soll.
    
2. Wählen Sie auf dem Menüband die Registerkarte **Bibliothek** oder **Liste** \> **Bibliothekeinstellungen** oder **Listeneinstellungen**.
    
    Klicken Sie in SharePoint Online auf **Einstellungen** , und klicken Sie dann auf **listeneinstellungen** oder **bibliothekeinstellungen**. 
    
3. Klicken Sie unter **Berechtigungen und Verwaltung** \> **Information Management Policy Settings**.
  
![Informationslink Management Richtlinien auf der Einstellungsseite für die Dokumentbibliothek](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Stellen Sie sicher, dass die Richtlinienquelle auf **Inhaltstypen**, und klicken Sie unter **Content Type Richtlinien** auswählen festgelegt ist den Inhaltstyp, der die Richtlinie angewendet werden soll. 
    
5. Klicken Sie unter **Richtlinie angeben** \> **Websitesammlungsrichtlinie verwenden**, und wählen Sie die Richtlinie, die Sie aus der Liste anwenden möchten. 
    
    > [!NOTE]
    >  Wenn die Option **Websitesammlungsrichtlinie verwenden** nicht verfügbar ist, wurden keine Site Collection Richtlinien für die Websitesammlung definiert. 
  
6. Wählen Sie **OK** aus.
    
     Wenn die Liste oder Bibliothek aus, die Sie mit arbeiten die Verwaltung mehrerer Inhaltstypen unterstützt, klicken Sie unter **Inhaltstypen** können Sie den Inhaltstyp für den Sie eine Informationsverwaltungsrichtlinie angeben möchten. Dadurch gelangen Sie direkt zu Schritt 5. 
    
## <a name="apply-a-policy-across-site-collections"></a>Anwenden einer Richtlinie über Websitesammlungen hinweg
<a name="__toc260646789"> </a>

Freigeben von Inhaltstypen in allen Websitesammlungen mit einer verwalteten Metadatendienstanwendung Inhaltstyp-Veröffentlichung einrichten. Inhaltstyp-Veröffentlichung können Sie Inhalt und Metadaten konsistent an Ihren Standorten verwalten, da Inhaltstypen können erstellt und aktualisiert werden zentral und Updates mehrere abonnierenden Websitesammlungen oder Web Applications veröffentlicht werden können.
  
## <a name="create-a-template-from-an-existing-policy-to-use-across-site-collections"></a>Erstellen Sie eine Vorlage aus einer vorhandenen Richtlinie in allen Websitesammlungen verwenden.
<a name="__toc262125409"> </a>

Sie können eine Informationsverwaltungsrichtlinie definieren und erstellen Sie dann eine Vorlage aus, um bei Bedarf über mehrere Websitesammlungen verwenden. Diese Methode kann verwendet werden, wenn Sie eine Sicherung Ihrer Richtlinien Informationen verfügen möchten oder kann auch als alternative Methode Verwendung von Inhaltstyp-Veröffentlichung für eine Richtlinie anwenden, in allen Websitesammlungen verwendet werden. Sie erstellen eine Vorlage oder eine Sicherung der Richtlinie, die Richtlinie aus einer Websitesammlung exportieren und anschließend importieren, um auf einen Speicherort oder in einer anderen Websitesammlung.
  
> [!IMPORTANT]
>  Wenn Sie über den Export/Import So stellen Sie eine Reihe von Vorlagen für Benutzerrechterichtlinien feature, lassen Sie berücksichtigen, die ein eindeutiger Bezeichner in der XML-Datei vorhanden ist. Sie aus diesem Grund können nicht die Richtlinie in einer Website nur einmal importiert ohne Änderung dieser eindeutigen Bezeichner. 
  
### <a name="export-a-policy"></a>Exportieren einer Richtlinie
<a name="__toc260646790"> </a>

1. Wählen Sie auf die Homepage der Websitesammlung, die **Einstellungen**![Zahnradsymbol für kleine Einstellungen, die stattgefunden der Site Settings. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **Websiteeinstellungen**.
    
    Klicken Sie in einer SharePoint-Gruppe verbundenen Website auf **Einstellungen**, klicken Sie auf **Websiteinhalte**, und klicken Sie dann auf **Websiteeinstellungen**. 
    
2. Klicken Sie auf der Seite Websiteeinstellungen unter **Websitesammlungsverwaltung** \> **Content Type Richtlinienvorlagen**. 
  
![Verknüpfung mit Inhalt Typ Richtlinienvorlage auf der Seite Websiteeinstellungen](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Wählen Sie die zu exportierende Richtlinie \> Bildlauf nach unten \> **Exportieren**.
    
4. Wählen Sie an der Eingabeaufforderung zum Speichern oder öffnen Sie die Datei **Speichern**, und wählen Sie dann einen Speicherort für die Datei zu speichern. Achten Sie darauf, dass Sie einen Speicherort auswählen, der für die Websitesammlungen verfügbar ist, die die Richtlinie importieren.
    
5. Wenn das Dialogfeld Download abgeschlossen angezeigt wird, wählen Sie auf **Schließen**.
    
### <a name="import-a-policy-to-a-different-site-collection"></a>Importieren einer Richtlinie in einer anderen Websitesammlung
<a name="__toc260646791"> </a>

Importieren einer Informationsverwaltungsrichtlinie können Sie es auf mehrere Inhaltstypen auf der Website oder Liste Ebene innerhalb einer bestimmten Websitesammlung anwenden. Auf diese Weise Vorteile aus zwei Schritten: Sie brauchen sich erneut definieren, und wenden die Richtlinie für jeden Inhaltstyp, und Sie können die Richtlinie Änderungen leichter verwalten, durch Ändern der Richtlinie an einer Stelle.
  
1. Wählen Sie auf der Homepage der Websitesammlung auf die Richtlinie angewendet werden soll, die **Einstellungen**![Zahnradsymbol für kleine Einstellungen, die stattgefunden der Site Settings. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **Websiteeinstellungen**.
    
    Klicken Sie in einer SharePoint-Gruppe verbundenen Website auf **Einstellungen**, klicken Sie auf **Websiteinhalte**, und klicken Sie dann auf **Websiteeinstellungen**. 
    
2. Klicken Sie auf der Seite Websiteeinstellungen unter **Websitesammlungsverwaltung** \> **Content Type Richtlinienvorlagen**.
    
3. Auf der Seite Richtlinien \> **Import** \> beim Suchen der XML-Datei für die Richtlinie **Durchsuchen** . 
    
4. Wählen Sie aus der XML-Datei, in dem die Richtlinie gespeichert wurden \> **Öffnen**. 
    
5. Der Import Websitesammlungsrichtlinie auf der Seite \> **Importieren** , um die Richtlinie für die Websitesammlung hinzufügen. 
    
Die importierten Richtlinien kann jetzt auf einen oder mehrere Inhaltstypen Ebene der Website oder Liste angewendet werden. 
  
[Informationsverwaltungsrichtlinien können Ihrer Organisation beibehalten werden Inhalte, überwachen, was Personen mit Inhalten werden, und Hinzufügen von Barcodes, wie lange Steuerelement oder Etiketten auf Dokumente. Eine Richtlinie kann mit rechtlichen und behördlichen Regelungen oder interner Geschäftsprozesse Durchsetzung helfen. Als Administrator können Sie eine Richtlinie festlegen, steuern, wie die Dokumente überwachen und wie lange Dokumente aufbewahrt. Sie können eine Informationen Management Policy können an drei unterschiedlichen Standorten in der Websitehierarchie aus der größte erstellen, der schmalste: Erstellen Sie eine Richtlinie auf mehrere Inhaltstypen innerhalb einer Websitesammlung verwenden. Erstellen Sie eine Richtlinie für einen Inhaltstyp für die Website. Erstellen Sie eine Richtlinie für eine Liste oder Bibliothek. Weitere Informationen finden Sie unter Einführung in Informationsverwaltungsrichtlinien.](create-info-mgmt-policies.md#__top)
  

