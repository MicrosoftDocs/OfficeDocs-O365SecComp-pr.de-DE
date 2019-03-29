---
title: Erstellen und Anwenden von Informationsverwaltungsrichtlinien
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/16/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 8ccac9e4-3a50-49fa-a95b-d186032a6ee3
ms.collection:
- M365-security-compliance
description: Informationsverwaltungsrichtlinien ermöglichen es Ihrer Organisation, zu steuern, wie lange Inhalte aufbewahrt werden, wie Sie die Inhalte der Benutzer überwachen und ob Sie Dokumenten Barcodes oder Beschriftungen hinzufügen können. Eine Richtlinie kann dazu beitragen, die Einhaltung rechtlicher und behördlicher Vorschriften oder interner Geschäftsprozesse zu erzwingen. Als Administrator können Sie eine Richtlinie einrichten, mit der gesteuert wird, wie Dokumente verfolgt werden und wie lange Dokumente aufbewahrt werden sollen.
ms.openlocfilehash: 1d17dd8cadb721478831ab8fe77413c08f959f29
ms.sourcegitcommit: 1658be51e2c21ed23bc4467a98af74300a45b975
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2019
ms.locfileid: "30862567"
---
# <a name="create-and-apply-information-management-policies"></a>Erstellen und Anwenden von Informationsverwaltungsrichtlinien

Informationsverwaltungsrichtlinien ermöglichen es Ihrer Organisation, zu steuern, wie lange Inhalte aufbewahrt werden, wie Sie die Inhalte der Benutzer überwachen und ob Sie Dokumenten Barcodes oder Beschriftungen hinzufügen können. Eine Richtlinie kann dazu beitragen, die Einhaltung rechtlicher und behördlicher Vorschriften oder interner Geschäftsprozesse zu erzwingen. Als Administrator können Sie eine Richtlinie einrichten, mit der gesteuert wird, wie Dokumente verfolgt werden und wie lange Dokumente aufbewahrt werden sollen.
  
Sie können eine Informationsverwaltungsrichtlinie an drei verschiedenen Standorten in der Websitehierarchie von den am weitesten geringsten erstellen:
  
- Erstellen Sie eine Richtlinie für mehrere Inhaltstypen innerhalb einer Websitesammlung.
    
- Erstellen Sie eine Richtlinie für einen Websiteinhaltstyp.
    
- Erstellen Sie eine Richtlinie für eine Liste oder Bibliothek.
    
Weitere Informationen finden Sie unter [Einführung in Informationsverwaltungsrichtlinien](intro-to-info-mgmt-policies.md).
  
## <a name="create-a-policy-for-multiple-content-types-within-a-site-collection"></a>Erstellen einer Richtlinie für mehrere Inhaltstypen in einer Websitesammlung
<a name="__toc261001590"> </a>

Wenn Sie sicherstellen möchten, dass eine Informationsrichtlinie auf alle Dokumente eines bestimmten Typs innerhalb einer Websitesammlung angewendet wird, sollten Sie die Richtlinie auf Websitesammlungsebene erstellen und dann die Richtlinie später auf Inhaltstypen anwenden. Diese werden als Websitesammlungsrichtlinien bezeichnet. 
  
1. auf der homepage \> der websitesammlung **einstellungen**![sharepoint 2016 einstellungen in der titelleiste.](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Websiteeinstellungen**.
    
    Klicken Sie in einer mit einer SharePoint-Gruppe verknüpften Website auf **Einstellungen**, **Websiteinhalte**und dann auf **Websiteeinstellungen**. 
    
2. Klicken Sie auf der Seite Websiteeinstellungen unter **Inhaltstyp Richtlinienvorlagen**für **Websitesammlungsverwaltung** \> . 
  
![Link zur Inhaltstyp-Richtlinienvorlage auf der Seite Websiteeinstellungen](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. \> **Erstellen**Sie auf der Seite Richtlinien. 
    
4. Geben Sie einen Namen und eine Beschreibung für die Richtlinie ein, und schreiben Sie dann eine kurze Richtlinienanweisung, die den Benutzern erläutert, wofür die Richtlinie gilt.
    
5. Im nächsten Abschnitt Erstellen von Richtlinien für einen Websiteinhaltstyp erfahren Sie, wie Sie die Features einrichten, die Sie der Richtlinie zuordnen möchten. 
    
6. Wählen Sie **OK** aus.
    
## <a name="create-a-policy-for-a-site-content-type"></a>Erstellen einer Richtlinie für einen Websiteinhaltstyp
<a name="__create_a_policy"> </a>

Das Hinzufügen einer Informationsverwaltungsrichtlinie zu einem Inhaltstyp erleichtert das Zuordnen von Richtlinienfeatures zu mehreren Listen oder Bibliotheken. Sie können eine vorhandene Informationsverwaltungsrichtlinie zu einem Inhaltstyp hinzufügen oder eine eindeutige Richtlinie für einen einzelnen Inhaltstyp erstellen.
  
 Sie können auch eine Informationsverwaltungsrichtlinie zu einem Inhaltstyp hinzufügen, der für Listen spezifisch ist. Dadurch wird die Richtlinie nur auf Elemente in dieser Liste angewendet, die den Inhaltstyp verwenden. 
  
1. auf der homepage \> der websitesammlung **einstellungen**![sharepoint 2016 einstellungen in der titelleiste.](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Websiteeinstellungen**.
    
    Klicken Sie in einer mit einer SharePoint-Gruppe verknüpften Website auf **Einstellungen**, **Websiteinhalte**und dann auf **Websiteeinstellungen**. 
    
2. Klicken Sie auf der Seite Websiteeinstellungen unter **Web-Designer-Kataloge** \> **Websiteinhaltstypen**.
  
![Link "Websiteinhaltstypen" auf der Seite "Websiteeinstellungen"](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
3. Wählen Sie auf der Seite Einstellungen für Websiteinhaltstyp den Inhaltstyp aus, dem Sie eine Richtlinie hinzufügen möchten.
    
4. Klicken Sie auf der Seite Websiteinhaltstyp unter **Einstellungen** \> für die **Informationsverwaltungsrichtlinie**.
    
5. Geben Sie auf der Seite Richtlinie bearbeiten einen Namen und eine Beschreibung für die Richtlinie ein, und schreiben Sie dann eine kurze Beschreibung, die den Benutzern erläutert, wofür die Richtlinie gilt.
    
6. Wählen Sie in den nächsten Abschnitten die einzelnen Richtlinienfeatures aus, die Sie zur Informationsverwaltungsrichtlinie hinzufügen möchten. 
  
![Arten von Inhaltsrichtlinien](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
7. Um einen Aufbewahrungszeitraum für Dokumente und Elemente anzugeben, die dieser Richtlinie unterliegen, wählen Sie **Aufbewahrung aktivieren**aus, und geben Sie dann den Aufbewahrungszeitraum und die Aktionen an, die beim Ablauf der Elemente auftreten sollen.
    
    So geben Sie einen Aufbewahrungszeitraum an
    
||||||**1.**|* * Wählen Sie * * eine Aufbewahrungs Stufe für Datensätze hinzufügen... * * * *|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> | Wählen Sie eine Beibehaltungsdauer aus, um anzugeben, wann Dokumente oder Elemente ablaufen sollen. Führen Sie einen der folgenden Schritte aus:  <br/>  Zum Festlegen des Ablaufdatums auf der Grundlage einer Date-Eigenschaft, unter **Ereignis** \> **Diese Stufe basiert auf einer Date-Eigenschaft für das Element**, und wählen Sie dann die Aktion Dokument oder Element (beispielsweise erstellt oder geändert) und die Zeitintervall nach dieser Aktion ( beispielsweise die Anzahl von Tagen, Monaten oder Jahren), wenn das Element ablaufen soll.  <br/>  Wenn Sie eine benutzerdefinierte Aufbewahrungs Formel zum Bestimmen des Ablaufs verwenden möchten, wählen Sie **festlegen nach einer benutzerdefinierten Aufbewahrungs Formel, die auf diesem Server installiert**ist.  <br/> > [!NOTE]> diese Option ist nur verfügbar, wenn Ihr Administrator eine benutzerdefinierte Formel eingerichtet hat.           |
||||||3.  <br/> |Die Option **Workflow starten** ist nur verfügbar, wenn Sie eine Richtlinie für eine Liste, eine Bibliothek oder einen Inhaltstyp definieren, denen bereits ein Workflow zugeordnet ist. Sie erhalten dann eine Auswahl von Workflows zur Auswahl.  <br/> |
||||||4.  <br/> |Wählen Sie im Abschnitt **Serie** die **Aktion diese Stufe wiederholen** aus... , und geben Sie ein, wie oft die Aktion erneut erfolgen soll.  <br/> > [!NOTE]> diese Option ist nur verfügbar, wenn die ausgewählte Aktion wiederholt werden kann. Sie können beispielsweise keine Serie für die Aktion **dauerhaft löschen**festlegen.           |
||||||5.  <br/> |Wählen Sie **OK**aus.  <br/> |
   
1. Zum Aktivieren der Überwachung für die Dokumente und Elemente, die dieser Richtlinie unterliegen, wählen Sie **Überwachung aktivieren**aus, und geben Sie dann die zu überwachenden Ereignisse an.
    
    So aktivieren Sie die Überwachung
    
||||||1. * * * *|Klicken Sie auf der Seite Richtlinie bearbeiten auf * * **unter** **Überwachung** **\>** **aktivieren** der Überwachung * *, und aktivieren Sie dann die Kontrollkästchen neben den Ereignissen, für die Sie einen Überwachungspfad beibehalten möchten. * * * *|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |**Um Benutzer aufzufordern, diese Barcodes in Dokumente einzufügen,** **Wählen Sie** **Benutzer auffordern, vor dem Speichern oder Drucken einen Barcode einzufügen** **.** <br/> |
||||||**3.** <br/> |**Wählen Sie** **OK** * * zum Anwenden des Überwachungsfeatures auf die Richtlinie. ** <br/> |
|||||||Das Überwachungsrichtlinienfeature ermöglicht Organisationen das Erstellen und Analysieren von Überwachungspfaden für Dokumente und das Auflisten von Elementen wie Aufgabenlisten, Problemlisten, Diskussionsgruppen und Kalendern. Mit diesem Richtlinienfeature wird ein Überwachungsprotokoll bereitgestellt, das Ereignisse wie beispielsweise, wenn Inhalt angezeigt, bearbeitet oder gelöscht wird, aufzeichnet.  <br/> |
|||||||Wenn die Überwachung im Rahmen einer Informationsverwaltungsrichtlinie aktiviert ist, können Administratoren die Überwachungsdaten in Richtlinien Verwendungsberichten anzeigen, die in Microsoft Excel basieren und die aktuelle Nutzung zusammenfassen. Administratoren können mithilfe dieser Berichte feststellen, wie Informationen innerhalb der Organisation verwendet werden. Diese Berichte können Organisationen auch dabei helfen, Ihre Compliance zu überprüfen und zu dokumentieren oder potenzielle Probleme zu untersuchen.  <br/> |
|||||||Im Überwachungsprotokoll werden folgende Informationen aufgezeichnet: Ereignisname, Datum und Uhrzeit des Ereignisses sowie der Systemname des Benutzers, der die Aktion ausgeführt hat.  <br/> |
   
1. Wenn Barcodes als Teil einer Richtlinie aktiviert werden, werden Sie den Dokumenteigenschaften hinzugefügt und im Kopfbereich des Dokuments angezeigt, auf das der Barcode angewendet wird. Wie Beschriftungen können auch Barcodes manuell aus einem Dokument entfernt werden. Sie können angeben, ob Benutzer beim Drucken oder Speichern eines Elements zum Einfügen des Barcodes aufgefordert werden sollen oder ob der Barcode mithilfe der Registerkarte **Einfügen** in 2010 Office Release-Programmen manuell eingefügt werden soll. 
    
    So aktivieren Sie Barcodes
    
||||||1. * * * *|**Aktivieren Sie auf der Seite Richtlinie **** \> bearbeiten unter Barcodes Barcodes. ******|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |Um Benutzer aufzufordern, diese Barcodes in Dokumente einzufügen, wählen Sie **Benutzer auffordern, vor dem Speichern oder Drucken einen Barcode einzufügen**.  <br/> |
||||||**3.** <br/> |Klicken Sie auf **OK** , um das Barcode-Feature auf die Richtlinie anzuwenden.  <br/> |
|||||||
 Die Barcode-Richtlinie generiert Code 39-Standard Barcodes. Jedes Barcode Bild enthält Text unter dem barcodesymbol, das den Barcode Wert darstellt. Dadurch können die Barcodedaten auch dann verwendet werden, wenn die Hardware nicht verfügbar ist. Benutzer können die Barcodenummer manuell in das Suchfeld eingeben, um das Element auf einer Website zu suchen.  <br/> |
   
1. Um festzulegen, dass Dokumente, die dieser Richtlinie unterliegen, Bezeichnungen aufweisen sollen, wählen Sie **Bezeichnungen aktivieren**aus, und geben Sie dann die gewünschten Einstellungen für die Bezeichnungen an.
    
    So aktivieren Sie Beschriftungen
    
||||||**1.**|* * Damit Benutzer eine Bezeichnung zu einem Dokument hinzufügen müssen, wählen Sie Benutzer aufFordern, eine Bezeichnung einzufügen, **bevor Sie speichern oder Drucken**.  <br/> > [!NOTE]> wenn Bezeichnungen optional sein sollen, aktivieren Sie dieses Kontrollkästchen nicht.        **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> |Wenn Sie eine Bezeichnung so sperren möchten, dass Sie nach dem Einfügen nicht mehr geändert werden kann, wählen Sie **Änderungen an Bezeichnungen nach dem Hinzufügen verhindern**aus.  <br/>  Diese Einstellung verhindert, dass der Bezeichnungstext aktualisiert wird, nachdem die Bezeichnung in ein Element in einer Clientanwendung wie Word, Excel oder PowerPoint eingefügt wurde. Aktivieren Sie dieses Kontrollkästchen nicht, falls die Bezeichnung aktualisiert werden soll, wenn die Eigenschaften für dieses Dokument oder Element aktualisiert werden.  <br/> |
||||||3.  <br/> |Geben Sie im Feld beZeichnungsformat den Text für die Beschriftung so ein, wie er angezeigt werden soll. Beschriftungen können bis zu 10 Spaltenbezüge enthalten, von denen jede bis zu 255 Zeichen lang sein kann. Gehen Sie folgendermaßen vor, um das Format für ihre Bezeichnung zu erstellen:  <br/> Geben Sie die Namen der Spalten ein, die in der Bezeichnung enthalten sein sollen, in der Reihenfolge, in der Sie angezeigt werden sollen. Legen Sie die Spaltennamen in geschweifte Klammern ({}), wie im Beispiel auf der Seite Richtlinie bearbeiten dargestellt.  <br/> Geben Sie Wörter ein, um die Spalten außerhalb der Klammern zu identifizieren, wie im Beispiel auf der Seite Richtlinie bearbeiten dargestellt.  <br/> |
||||||4.  <br/> |Wenn Sie einen Linien Umbruch hinzufügen möchten, geben Sie **\n** ein, wo der Linien Umbruch angezeigt werden soll.  <br/> |
||||||5.  <br/> |Wählen Sie den gewünschten Schriftgrad und die gewünschte Formatvorlage aus, und geben Sie an, ob die Beschriftung links, zentriert oder rechts im Dokument positioniert werden soll.  <br/>  Wählen Sie eine Schriftart und ein Format aus, die auf den Benutzercomputern verfügbar sind. Es hängt vom Schriftgrad ab, wie viel Text auf der Bezeichnung angezeigt werden kann.  <br/> |
||||||6.  <br/> |Geben Sie die Höhe und Breite der Beschriftung ein. Die Beschriftungs Höhe kann zwischen .25 Zoll und 20 Zoll liegen, und die Beschriftungs Breite kann zwischen .25 Zoll und 20 Zoll liegen. Beschriftungstext wird immer vertikal innerhalb des Beschriftungs Bilds zentriert.  <br/> |
||||||7.  <br/> |Klicken Sie auf **Aktualisieren** , um eine Vorschau des Beschriftungs Inhalts anzuzeigen.  <br/> |
   
1. Wählen Sie **OK** aus.
    
## <a name="create-a-policy-for-a-list-library-or-folder-location-based-retention-policy"></a>Erstellen einer Richtlinie für eine Liste, Bibliothek oder einen Ordner (standortbasierte Aufbewahrungsrichtlinie)
<a name="__create_a_policy"> </a>

Sie können eine Aufbewahrungsrichtlinie definieren, die nur für eine bestimmte Liste, Bibliothek oder einen bestimmten Ordner gilt. Wenn Sie jedoch eine Aufbewahrungsrichtlinie auf diese Weise erstellen, können Sie diese Richtlinie nicht für andere Listen, Bibliotheken, Ordner oder Websites wieder verwenden, und Sie können eine Websitesammlungsrichtlinie nicht auf eine standortbasierte Richtlinie anwenden.
  
Wenn Sie eine einzelne Aufbewahrungsrichtlinie auf alle Arten von Inhalten an einem einzigen Standort anwenden möchten, möchten Sie wahrscheinlich die standortbasierte Aufbewahrung verwenden. In den meisten Fällen möchten Sie sicherstellen, dass für alle Inhaltstypen eine Aufbewahrungsrichtlinie angegeben wird.
  
 Jeder Unterordner erbt die Aufbewahrungsrichtlinie seines übergeordneten Elements, es sei denn, Sie unterbrechen die Vererbung, und definieren eine neue Aufbewahrungsrichtlinie auf Child-Ebene. 
  
Wenn Sie eine andere Informationsverwaltungsrichtlinie als die Aufbewahrung für eine Liste oder Bibliothek definieren möchten, müssen Sie für jeden einzelnen Listeninhaltstyp, der dieser Liste oder Bibliothek zugeordnet ist, eine Informationsverwaltungsrichtlinie definieren.
  
 Wenn Sie sich für eine Liste oder Bibliothek zu einem beliebigen Zeitpunkt entscheiden, vom Inhaltstyp zu standortbasierten Richtlinien zu wechseln, wird nur die Aufbewahrungsrichtlinie als standortbasierte Richtlinie verwendet. Alle anderen Verwaltungsrichtlinien (Audits, Barcodes und Barcodes) werden von den zugeordneten Inhaltstypen geerbt. 
  
 Standortbasierte Richtlinien können für eine Websitesammlung deaktiviert werden, indem die Bibliotheks-und ordnerbasierte Aufbewahrungsfunktion deaktiviert wird. Dadurch können Websitesammlungsadministratoren sicherstellen, dass Ihre Inhaltstyp Richtlinien nicht durch standortbasierte Richtlinien eines Listenadministrators außer Kraft gesetzt werden. 
  
Sie benötigen mindestens die Berechtigung Listen verwalten, um die Einstellungen für die Informationsverwaltungsrichtlinie für eine Liste oder Bibliothek zu ändern.
  
1. Navigieren Sie zu der Liste oder Bibliothek, für die Sie eine Informationsverwaltungsrichtlinie angeben möchten. 
    
2. Klicken Sie auf dem Menüband auf **** die Registerkarte \> **** Bibliotheks-oder **Listen** Bibliothekseinstellungen oder **Listeneinstellungen**.
    
    Klicken Sie in SharePoint Online auf **Einstellungen** und dann auf **Listeneinstellungen** oder **Bibliothekseinstellungen**. 
    
3. Unter **Berechtigungen und Verwaltungs** \> **Informationsverwaltungsrichtlinien Einstellungen**.
  
![Informationsverwaltungsrichtlinien-Link auf der Seite "Einstellungen" für die Dokumentbibliothek](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Stellen Sie auf der Seite Einstellungen für die Informationsverwaltungsrichtlinie sicher, dass die Aufbewahrungs Quelle für die Liste oder Bibliothek auf Bibliothek und Ordner festgelegt ist. 
  
Wenn der **Inhaltstyp** als Quelle angezeigt wird, klicken Sie auf **Quelle ändern**, und klicken Sie dann auf **Bibliothek und Ordner**. Sie werden benachrichtigt, dass die Aufbewahrungsrichtlinien für Inhaltstypen ignoriert werden. Wählen Sie **OK** aus. 
    
5. Geben Sie auf der Seite Richtlinie bearbeiten unter **Bibliotheks basiertEr aufbewahrungszeitplan**eine kurze Beschreibung für die Richtlinie ein, die Sie erstellen. 
    
6. Wählen Sie **Add a Retention Staging** ...
    
     Beachten Sie, dass Sie Unterdatensätze verschiedene Aufbewahrungsrichtlinien für Datensätze definieren können, indem Sie die Option verschiedene Aufbewahrungs Phasen für Datensätze definieren auswählen. 
    
7. Wählen Sie im Dialogfeld Stufen Eigenschaften eine Beibehaltungsdauer aus, um anzugeben, wann Dokumente oder Elemente ablaufen sollen. Führen Sie einen der folgenden Schritte aus:
    
  - Zum Festlegen des Ablaufdatums auf der Grundlage einer Date-Eigenschaft, unter **Ereignis** \> **Diese Stufe basiert auf einer Date-Eigenschaft für das Element**, und wählen Sie dann die Aktion Dokument oder Element (beispielsweise erstellt oder geändert) und die Zeitintervall nach dieser Aktion ( beispielsweise die Anzahl von Tagen, Monaten oder Jahren), wenn das Element ablaufen soll. 
    
  - Wenn Sie eine benutzerdefinierte Aufbewahrungs Formel zum Bestimmen des Ablaufs verwenden möchten, wählen Sie **festlegen nach einer benutzerdefinierten Aufbewahrungs Formel, die auf diesem Server installiert**ist. 
    
    > [!NOTE]
    >  Diese Option ist nur verfügbar, wenn Ihr Administrator eine benutzerdefinierte Formel eingerichtet hat. 
  
  - Geben Sie unter **Aktion**an, was geschehen soll, wenn das Dokument oder Element abläuft. Wenn Sie eine bestimmte Aktion mit dem Dokument oder Element (beispielsweise Löschen) ausführen möchten, wählen Sie in der Liste eine Aktion aus. 
    
8. Die Option **Workflow starten** ist nur verfügbar, wenn Sie eine Richtlinie für eine Liste, eine Bibliothek oder einen Inhaltstyp definieren, denen bereits ein Workflow zugeordnet ist. Sie erhalten dann eine Auswahl von Workflows zur Auswahl. 
    
9. Wählen **** Sie unter Serie **die Aktion diese Stufe wiederholen...** , und geben Sie ein, wie oft die Aktion erneut erfolgen soll. 
    
    > [!NOTE]
    >  Diese Option ist nur verfügbar, wenn die ausgewählte Aktion wiederholt werden kann. Sie können beispielsweise keine Serie für die Aktion **dauerhaft löschen**festlegen. 
  
10. Wählen Sie **OK** aus.
    
## <a name="apply-a-site-collection-policy-to-a-content-type"></a>Anwenden einer Websitesammlungsrichtlinie auf einen Inhaltstyp
<a name="__apply_a_site"> </a>

Wenn für Ihre Website bereits Informationsverwaltungsrichtlinien als Websitesammlungsrichtlinien erstellt wurden, können Sie eine der Richtlinien auf einen Inhaltstyp anwenden. Auf diese Weise können Sie dieselbe Richtlinie auf mehrere Inhaltstypen in einer Websitesammlung anwenden, die nicht denselben übergeordneten Inhaltstyp aufweisen.
  
 Wenn Sie Richtlinien auf mehrere Inhaltstypen in einer Websitesammlung anwenden möchten und Sie einen verwalteten metaDatendienst konfiguriert haben, können Sie die InhaltstypVeröffentlichung verwenden, um die Informationsverwaltungsrichtlinien für mehrere Websitesammlungen zu veröffentlichen. Weitere Informationen finden Sie im Abschnitt [Anwenden einer Richtlinie für Websitesammlungen](#apply-a-policy-across-site-collections) . 
  
1. Navigieren Sie zu der Liste oder Bibliothek, die den Inhaltstyp enthält, auf den Sie eine Richtlinie anwenden möchten.
    
2. Klicken Sie auf dem Menüband auf **** die Registerkarte \> **** Bibliotheks-oder **Listen** Bibliothekseinstellungen oder **Listeneinstellungen**.
    
    Klicken Sie in SharePoint Online auf **Einstellungen** und dann auf **Listeneinstellungen** oder **Bibliothekseinstellungen**. 
    
3. Unter **Berechtigungen und Verwaltungs** \> **Informationsverwaltungsrichtlinien Einstellungen**.
  
![Informationsverwaltungsrichtlinien-Link auf der Seite "Einstellungen" für die Dokumentbibliothek](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Stellen Sie sicher, dass die Richtlinienquelle auf **Inhaltstypen**festgelegt ist, und wählen Sie unter **Inhaltstyp Richtlinien** den Inhaltstyp aus, auf den die Richtlinie angewendet werden soll. 
    
5. Wählen Sie unter **Richtlinie** \> **verwenden Sie eine Websitesammlungsrichtlinie**aus die Richtlinie aus, die Sie in der Liste anwenden möchten. 
    
    > [!NOTE]
    >  Wenn die Option **Websitesammlungsrichtlinie verwenden** nicht verfügbar ist, wurden für die Websitesammlung keine Websitesammlungsrichtlinien definiert. 
  
6. Wählen Sie **OK** aus.
    
     Wenn die Liste oder Bibliothek, mit der Sie arbeiten, die Verwaltung mehrerer Inhaltstypen unterstützt, können Sie unter **Inhaltstypen** den Inhaltstyp auswählen, für den Sie eine Informationsverwaltungsrichtlinie angeben möchten. Dadurch gelangen Sie direkt zu Schritt 5 oben. 
    
## <a name="apply-a-policy-across-site-collections"></a>Anwenden einer Richtlinie für Websitesammlungen
<a name="__toc260646789"> </a>

Freigeben von Inhaltstypen über Websitesammlungen hinweg mithilfe einer Dienstanwendung für verwaltete Metadaten zum Einrichten der inhaltstypveröffentlichung. Die inhaltstypveröffentlichung hilft Ihnen bei der konsistenten Verwaltung von Inhalten und Metadaten, da Inhaltstypen zentral erstellt und aktualisiert werden können und Updates in mehreren abonnierten Websitesammlungen oder Webanwendungen veröffentlicht werden können.
  
## <a name="create-a-template-from-an-existing-policy-to-use-across-site-collections"></a>Erstellen einer Vorlage aus einer vorhandenen Richtlinie für die Verwendung in Websitesammlungen
<a name="__toc262125409"> </a>

Sie können eine Informationsverwaltungsrichtlinie definieren und dann eine Vorlage erstellen, um Sie bei Bedarf über mehrere Websitesammlungen hinweg zu verwenden. Diese Methode kann verwendet werden, wenn Sie eine Sicherung ihrer Informationsrichtlinien verwenden möchten, oder Sie kann auch als alternative Methode zur Verwendung der inhaltstypveröffentlichung zum Anwenden einer Richtlinie für Websitesammlungen verwendet werden. Sie erstellen eine Vorlage oder Sicherung der Richtlinie, indem Sie die Richtlinie aus einer Websitesammlung exportieren und Sie dann an einen gespeicherten Speicherort oder in eine andere Websitesammlung importieren.
  
> [!IMPORTANT]
>  Wenn Sie das Feature exportieren/importieren als Möglichkeit zum Erstellen einer Gruppe von Richtlinienvorlagen verwenden, sollten Sie Bedenken, dass in der Datei Policy. XML ein eindeutiger Bezeichner vorhanden ist. Aus diesem Grund können Sie diese Richtlinie nicht mehr als einmal in eine Website importieren, ohne diesen eindeutigen Bezeichner zu ändern. 
  
### <a name="export-a-policy"></a>Exportieren einer Richtlinie
<a name="__toc260646790"> </a>

1. Klicken Sie auf der Homepage der Websitesammlung auf **Einstellungen**![für kleine Einstellungen, die den Ort der Websiteeinstellungen übernommen haben. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) **** Website \> Einstellungen.
    
    Klicken Sie in einer mit einer SharePoint-Gruppe verknüpften Website auf **Einstellungen**, **Websiteinhalte**und dann auf **Websiteeinstellungen**. 
    
2. Klicken Sie auf der Seite Websiteeinstellungen unter **Inhaltstyp Richtlinienvorlagen**für **Websitesammlungsverwaltung** \> . 
  
![Link zur Inhaltstyp-Richtlinienvorlage auf der Seite Websiteeinstellungen](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Wählen Sie die Richtlinie aus, \> die Sie exportieren möchten \> , Scrollen Sie zum unteren **Export**.
    
4. Klicken Sie bei der Meldung zum Speichern oder Öffnen der Datei auf **Speichern**, und wählen Sie dann einen Speicherort für die Datei aus. Wählen Sie unbedingt einen Speicherort aus, der den Websitesammlungen zur Verfügung steht, die die Richtlinie importieren.
    
5. Wenn das Dialogfeld zum Herunterladen angezeigt wird, klicken Sie auf **Schließen**.
    
### <a name="import-a-policy-to-a-different-site-collection"></a>Importieren einer Richtlinie in eine andere Websitesammlung
<a name="__toc260646791"> </a>

Durch das Importieren einer Informationsverwaltungsrichtlinie können Sie Sie auf mehrere Inhaltstypen auf der Website-oder Listenebene innerhalb einer bestimmten Websitesammlung anwenden. Die Vorteile sind zweierlei: Sie müssen die Richtlinie für jeden Inhaltstyp nicht neu definieren und anwenden, und Sie können Richtlinienänderungen leichter verwalten, indem Sie an nur einer Stelle Änderungen an der Richtlinie vornehmen.
  
1. Wählen Sie auf der Startseite der Websitesammlung, auf die Sie die Richtlinie anwenden möchten, **Einstellungen**![kleine Einstellungen Gear aus, die die Websiteeinstellungen übernommen haben. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) **** Website \> Einstellungen.
    
    Klicken Sie in einer mit einer SharePoint-Gruppe verknüpften Website auf **Einstellungen**, **Websiteinhalte**und dann auf **Websiteeinstellungen**. 
    
2. Klicken Sie auf der Seite Websiteeinstellungen unter **Inhaltstyp Richtlinienvorlagen**für **Websitesammlungsverwaltung** \> .
    
3. Klicken Sie auf der \> Seite Richtlinien- **Import** \> auf **Suchen** , um die XML-Datei für die Richtlinie zu suchen. 
    
4. Wählen Sie die XML-Datei aus, in der die \> Richtlinie **geöffnet**wurde. 
    
5. Fügen Sie auf der Seite \> **** Importieren einer Websitesammlungsrichtlinie die Richtlinie der Websitesammlung hinzu. 
    
Die importierte Richtlinie kann jetzt auf einen oder mehrere Inhaltstypen auf Website-oder Listenebene angewendet werden. 
  
Informationsverwaltungsrichtlinien ermöglichen es Ihrer Organisation, zu steuern, wie lange Inhalte aufbewahrt werden, wie Sie die Inhalte der Benutzer überwachen und ob Sie Dokumenten Barcodes oder Beschriftungen hinzufügen können. Eine Richtlinie kann dazu beitragen, die Einhaltung rechtlicher und behördlicher Vorschriften oder interner Geschäftsprozesse zu erzwingen. Als Administrator können Sie eine Richtlinie einrichten, mit der gesteuert wird, wie Dokumente verfolgt werden und wie lange Dokumente aufbewahrt werden sollen.

Sie können eine Informationsverwaltungsrichtlinie an drei verschiedenen Standorten in der Websitehierarchie von den am weitesten geringsten erstellen:
- Erstellen Sie eine Richtlinie für mehrere Inhaltstypen innerhalb einer Websitesammlung.
- Erstellen Sie eine Richtlinie für einen Websiteinhaltstyp.
- Erstellen Sie eine Richtlinie für eine Liste oder Bibliothek.

Weitere Informationen finden Sie unter [Einführung in Informationsverwaltungsrichtlinien](intro-to-info-mgmt-policies.md).
  

