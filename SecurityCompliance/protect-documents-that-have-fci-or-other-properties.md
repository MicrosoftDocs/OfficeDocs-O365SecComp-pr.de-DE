---
title: Erstellen einer DLP-Richtlinie zum Schützen von Dokumenten mit FCI oder anderen Eigenschaften
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContentPropertyContainsWords
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: 1b9e3c6c-4308-4a20-b11e-c37b8013e177
description: Viele Organisationen haben bereits einen Prozess zum Erkennen und Klassifizieren von vertraulichen Informationen mithilfe der Klassifizierungseigenschaften in Windows Server-Datei Klassifizierung-Infrastruktur (FCI), die Dokumenteigenschaften in SharePoint oder die Dokumenteigenschaften von einem Drittanbieter System angewendet. Wenn dies Ihrer Organisation beschrieben, können Sie eine DLP-Richtlinie in Office 365 erstellen, die erkennt die Eigenschaften, die von Windows Server FCI oder einem anderen System auf Dokumente angewendet wurden, damit die DLP-Richtlinie für Office-Dokumente mit bestimmten FCI oder andere erzwungen werden kann Eigenschaftswerte.
ms.openlocfilehash: 057cdad981249e39d6f39f231d8d60ab977e717a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013689"
---
# <a name="create-a-dlp-policy-to-protect-documents-with-fci-or-other-properties"></a>Erstellen einer DLP-Richtlinie zum Schützen von Dokumenten mit FCI oder anderen Eigenschaften

In Office 365 können Sie eine DLP-Richtlinie (Data Loss Prevention, Verhinderung von Datenverlust) verwenden, um vertrauliche Informationen zu ermitteln, zu überwachen und zu schützen. Viele Organisationen verfügen mithilfe der Klassifikationseigenschaften in Windows Dateiklassifizierungsinfrastruktur (FCI, File Classification Infrastructure), der Dokumenteigenschaften in SharePoint oder Dokumenteigenschaften, die von einem Drittanbietersystem angewendet werden, bereits über einen Prozess zum Identifizieren und Klassifizieren vertraulicher Informationen. Wenn dies auf Ihre Organisation zutrifft, können Sie eine DLP-Richtlinie in Office 365 erstellen, welche die Eigenschaften erkennt, die von Windows Server FCI oder einem anderen System auf Dokumente angewendet wurden, damit die DLP-Richtlinie bei Office-Dokumenten mit bestimmten FCI- oder anderen Eigenschaftswerten erzwungen werden kann.
  
![Diagramm, das Office 365 und ein externes Klassifizierungssystem zeigt](media/59ad0ac1-4146-4919-abd1-c74d8508d25e.png)
  
Beispielsweise Ihrer Organisation mithilfe von Windows Server FCI Identifizieren von Dokumenten mit personenbezogene Informationen (PII) wie Sozialversicherungsnummern möglicherweise, und klicken Sie dann das Dokument durch Festlegen der **Personally Identifiable Information** klassifizieren -Eigenschaft auf **Hoch**, **Mittel**, **Niedrig**, **öffentlichen**oder **Nicht PII** basierend auf dem Typ und Anzahl der Vorkommen eines PII im Dokument gefunden. In Office 365 können Sie eine DLP-Richtlinie erstellen, die identifiziert Dokumente, die diese Eigenschaft auf bestimmte Werte, wie **Hoch** und **Mittel**, festgelegt haben und nimmt dann eine Aktion wie etwa Blockieren des Zugriffs auf diese Dateien. Die gleiche Richtlinie kann eine weitere Regel haben, eine andere Aktion akzeptiert, wenn die Eigenschaft auf **Niedrig**festgelegt ist, beispielsweise das Senden einer e-Mail-benachrichtigungs. Auf diese Weise DLP in Office 365 mit Windows Server FCI integriert und kann schützen Office-Dokumente hochgeladen oder von Windows Server-basierte Dateiserver zu Office 365 freigegeben.
  
Eine DLP-Richtlinie sucht einfach nach einem bestimmten Eigenschafts-Name-Wert-Paar. Eine beliebige Dokumenteigenschaft kann verwendet werden, solange die Eigenschaft über eine entsprechende verwaltete Eigenschaft für die SharePoint-Suche verfügt. Eine SharePoint-Websitesammlung verwendet z. B. möglicherweise einen Inhaltstyp namens **Reisebericht** mit einem erforderlichen Feld namens **Kunde**. Wenn eine Person einen Reisebericht erstellt, muss sie den Namen des Kunden eingeben. Dieses Eigenschafts-Name-Wert-Paar kann auch in einer DLP-Richtlinie verwendet werden – z. B. wenn Sie eine Regel möchten, die den Zugriff auf das Dokument für externe Benutzer sperrt, wenn das Feld **Kunde****Contoso** enthält.
  
Beachten Sie, wenn Sie Inhalte mit bestimmten Office 365 Etiketten DLP-Richtlinie zuweisen möchten, nicht der folgenden Schritte befolgen sollten. In diesem Fall Hier erfahren Sie, wie Sie [eine Beschriftung als Bedingung in einer DLP-Richtlinie verwenden](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy).
  
## <a name="before-you-create-the-dlp-policy"></a>Bevor Sie die DLP-Richtlinie erstellen

Bevor Sie eine Windows Server FCI-Eigenschaft oder anderen-Eigenschaft in einer DLP-Richtlinie verwenden können, müssen Sie eine verwaltete Eigenschaft im SharePoint Administrationscenter zu erstellen. Hier ist die Antwort.
  
Beispiele
  
Dies ist wichtig, da DLP in Office 365 den Suchcrawler zum Identifizieren und Klassifizieren vertraulicher Informationen auf Ihren Websites verwendet und dann diese vertraulichen Informationen in einem sicheren Bereich des Suchindex speichert. Wenn Sie ein Dokument in Office 365 hochladen, erstellt SharePoint automatisch durchforstete Eigenschaften auf Grundlage der Dokumenteigenschaften. Um aber eine FCI- oder eine andere Eigenschaft in einer DLP-Richtlinie zu verwenden, muss die durchforstete Eigenschaft einer verwalteten Eigenschaft zugeordnet werden, damit Inhalt mit dieser Eigenschaft im Index gespeichert wird.
  
Weitere Informationen zum Suchen und verwalteten Eigenschaften finden Sie unter [Verwalten des suchschemas in SharePoint Online](http://go.microsoft.com/fwlink/p/?LinkID=627454).
  
### <a name="step-1-upload-a-document-with-the-needed-property-to-office-365"></a>Schritt 1: Hochladen eines Dokuments mit der erforderlichen Eigenschaft in Office 365

Sie müssen zuerst zum Hochladen eines Dokuments mit der-Eigenschaft, die Sie in Ihrer DLP-Richtlinie verweisen möchten. Office 365 erkennt die-Eigenschaft und eine durchforstete Eigenschaft automatisch daraus erstellen. Sie werden im nächsten Schritt erstellen Sie eine verwaltete Eigenschaft und ordnen Sie die verwaltete Eigenschaft dieser durchforsteten Eigenschaft.
  
### <a name="step-2-create-a-managed-property"></a>Schritt 2: Erstellen einer verwalteten Eigenschaft

1. Melden Sie sich beim Office 365 Admin Center an.
    
2. Wählen Sie im linken Navigationsbereich **Admin zentriert** \> **SharePoint**. Sie sind jetzt in der SharePoint-Verwaltungskonsole.
    
3. Wählen Sie im linken Navigationsbereich **Suche** \> auf der Seite **suchverwaltung** \> **Suchschema verwalten**.
    
    ![Seite „Suchverwaltung“ im SharePoint Admin Center](media/6bcd3aec-d11a-4f8c-9987-8f35da14d80b.png)
  
4. Klicken Sie auf der Seite **Verwaltete Eigenschaften** \> **Neue verwaltete Eigenschaft**.
    
    ![Seite „Verwaltete Eigenschaften“ mit hervorgehobener Schaltfläche „Neue verwaltete Eigenschaft“](media/b161c764-414c-4037-83ed-503a49fb4410.png)
  
5. Geben Sie einen Namen und eine Beschreibung für die Eigenschaft ein. Dieser Name wird in den DLP-Richtlinien angezeigt.
    
6. Wählen Sie für **Typ****Text**. 
    
7. Wählen Sie unter **Haupteigenschaften****Abfragbar** und **Abrufbar**.
    
8. Klicken Sie unter **Zuordnungen zu durchforsteten Eigenschaften** \> **Zuordnung hinzufügen**.
    
9. Klicken Sie im Dialogfeld **durchforstete Eigenschaft Auswahl** \> suchen, und wählen Sie die durchforstete Eigenschaft, die die Windows Server FCI-Eigenschaft oder anderen-Eigenschaft, die Sie in Ihrer DLP-Richtlinie verwenden entspricht \> **OK**.
    
    ![Dialogfeld für Auswahl für durchforstete Eigenschaft](media/aeda1dce-1342-48bf-9594-a8e4f230e8aa.png)
  
10. Am unteren Rand der Seite \> **OK**.
    
## <a name="create-a-dlp-policy-that-uses-an-fci-property-or-other-property"></a>Erstellen einer DLP-Richtlinie, die eine FCI-Eigenschaft oder eine andere Eigenschaft verwendet

In diesem Beispiel wird eine Organisation FCI auf die Windows Server-basierten Dateiserver verwenden; Verwenden sie insbesondere die FCI Klassifizierung-Eigenschaft mit dem Namen möglicher Werten der **Hoch**, **Mittel**, **Niedrig**, **Öffentliche**und **Nicht PII** **Persönlich identifizierbare Informationen** . Jetzt möchten sie ihre vorhandenen FCI Einstufung in ihrer DLP-Richtlinien in Office 365 zu nutzen.
  
Zunächst führen sie die oben beschriebenen Schritte zum Erstellen einer verwalteten Eigenschaft in SharePoint Online aus, die der durchforsteten Eigenschaft zugeordnet wird, die automatisch aus der FCI-Eigenschaft erstellt wurde.
  
Im nächsten Schritt erstellen sie eine DLP-Richtlinie mit zwei Regeln, die beide die Bedingung **Dokumenteigenschaften enthalten die folgenden Werte**verwenden:
  
- **Inhalte für FCI PII - hoch, Mittel** Die erste Regel beschränkt Zugriff auf das Dokument, wenn der FCI Klassifizierung-Eigenschaft **Personally Identifiable Information** **Hoch** oder **Mittel entspricht** und das Dokument mit Personen außerhalb der Organisation freigeben. 
    
- **Inhalte für FCI PII - niedrig** Die zweite Regel sendet eine Benachrichtigung an den Besitzer des Dokuments, wenn die FCI Klassifizierung-Eigenschaft **Personally Identifiable Information** **Niedrig** und das Dokument ist mit Personen außerhalb der Organisation gemeinsam genutzt wird. 
    
### <a name="create-the-dlp-policy-by-using-powershell"></a>Erstellen Sie die DLP-Richtlinie mithilfe von PowerShell

Beachten Sie, dass die Bedingung **Dokumenteigenschaften enthalten die folgenden Werte** vorübergehend nicht verfügbar in der Benutzeroberfläche des Wertpapiers ist &amp; Compliance Center, aber Sie können weiterhin diese Bedingung mithilfe von PowerShell. Können die `New\Set\Get-DlpCompliancePolicy` -Cmdlets zum Arbeiten mit einer DLP-Richtlinie, und verwenden Sie die `New\Set\Get-DlpComplianceRule` Cmdlets, mit der `ContentPropertyContainsWords` Parameter So fügen Sie die Bedingung **Dokumenteigenschaften enthalten die folgenden Werte**hinzu.
  
Weitere Informationen zu diesen Cmdlets, finden Sie unter [Sicherheit in Office 365 &amp; Compliance Center Cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409).
  
1. [Verbinden mit der Office 365-Sicherheit &amp; Compliance Center mit remote-PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Erstellen Sie die Richtlinie mithilfe von `New-DlpCompliancePolicy`.
    
    Hier ist ein PowerShell-Beispiel, mit dem eine DLP-Richtlinie erstellt, die für alle Standorte gilt.
    
      ```
      New-DlpCompliancePolicy -Name FCI_PII_policy -ExchangeLocation All -SharePointLocation All -OneDriveLocation All -Mode Enable
      ```

3. Erstellen Sie die beiden Regeln mithilfe der oben beschriebenen `New-DlpComplianceRule`, wobei eine Regel für den Wert **niedriger** ist, und eine weitere Regel für die **hohe** und **mittlere** Werte. 
    
    Hier ist ein PowerShell-Beispiel, mit dem dieser beiden Regeln erstellt. Beachten Sie, dass die Eigenschaft Name/Wert-Paare in Anführungszeichen eingeschlossen sind, und ein Eigenschaftennamen kann durch Kommata ohne Leerzeichen getrennt werden, wie mehrere Werte angeben`"<Property1>:<Value1>,<Value2>","<Property2>:<Value3>,<Value4>"....`
    
      ```
      New-DlpComplianceRule -Name FCI_PII_content-High,Moderate -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $true -ContentPropertyContainsWords "Personally Identifiable Information:High,Moderate" -Disabled $falseNew-DlpComplianceRule -Name FCI_PII_content-Low -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $false -ContentPropertyContainsWords "Personally Identifiable Information:Low" -Disabled $false -NotifyUser Owner
      ```

    Beachten Sie, dass Windows Server FCI zahlreiche integrierte Eigenschaften, einschließlich **Persönlich identifizierbare Informationen** in diesem Beispiel verwendete enthält. Die möglichen Werte für jede Eigenschaft können für jede Organisation unterschiedlich sein. **Die **hohe**, Mäßiges hier verwendeten **Niedrig** Werte**sind nur ein Beispiel. Für Ihre Organisation können Sie die Windows Server FCI Klassifizierungseigenschaften mit den möglichen Werten in der Datei Ressourcen-Manager auf dem Windows Server-basierten Dateiserver anzeigen. Weitere Informationen finden Sie unter [Erstellen einer Klassifikation-Eigenschaft](http://go.microsoft.com/fwlink/p/?LinkID=627456).
    
Wenn Sie fertig sind, sollte Ihre Richtlinie zwei neue Regeln, die beide die Bedingung **Dokumenteigenschaften enthalten die folgenden Werte** verwenden. Beachten Sie, dass diese Bedingung in der Benutzeroberfläche, obwohl die Bedingungen, Aktionen und Einstellungen nicht angezeigt wird, wird angezeigt. 
  
Eine Regel Blöcke zugreifen, um die Inhalte, auf dem der **Personally Identifiable Information** -Eigenschaft **Hoch** oder **Moderater**entspricht. Eine zweite Regel sendet eine Benachrichtigung über Inhalte, wobei die **Persönlich identifizierbare Informationen** -Eigenschaft **Niedrig**entspricht.
  
![Neues DLP-Richtliniendialogfeld mit zwei soeben erstellten Regeln](media/5c56c13b-62a5-4f25-8eb7-ce83a844bb12.png)
  
## <a name="after-you-create-the-dlp-policy"></a>Nachdem Sie die DLP-Richtlinie erstellt haben

Die Schritte in den vorherigen Abschnitten Erstellen einer DLP-Richtlinie, die schnell erkannt wird, mit dieser Eigenschaft Inhalt, jedoch nur, wenn dieser Inhalte (so, dass des Inhalts indiziert) neu hochgeladen wird, oder wenn Inhalten ist alte jedoch gerade bearbeitet (so, dass des Inhalts erneut indiziert) .
  
Um überall Inhalte mit dieser Eigenschaft zu ermitteln, sollten Sie manuell anfordern, dass die Bibliothek, Website oder Websitesammlung neu indiziert werden, damit die DLP-Richtlinie alle Inhalte mit dieser Eigenschaft kennt. In SharePoint Online werden Inhalte basierend auf einem definierten Durchforstungszeitplan automatisch durchforstet. Der Crawler ruft Inhalte ab, die seit der letzten Durchforstung geändert wurden, und aktualisiert den Index. Wenn Ihre DLP-Richtlinie Inhalte vor der nächsten geplanten Durchforstung schützen soll, können Sie diese Schritte ausführen.
  
> [!CAUTION]
> Erneute Indizierung einer Website kann eine große Auslastung auf das Suchsystem führen. Indizieren Sie nicht Ihrer Website erneut, es sei denn, das Szenario unbedingt erforderlich. 
  
Weitere Informationen finden Sie unter [manuell anfordern crawlen und einer Website, eine Bibliothek oder einer Liste neu indizieren](http://go.microsoft.com/fwlink/p/?LinkID=627457).
  
### <a name="re-index-a-site-optional"></a>Erneute Indizierung einer Website (optional)

1. Wählen Sie auf der Website die **Einstellungen** (Zahnradsymbol in der oberen rechten Ecke) \> **Websiteeinstellungen**.
    
2. Wählen Sie unter **Suchen**, **Suche und offlineverfügbarkeit** \> **Website indizieren**.
    
## <a name="more-information"></a>Weitere Informationen

- [Übersicht über Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md)
    
- [Erstellen einer DLP-Richtlinie aus einer Vorlage](create-a-dlp-policy-from-a-template.md)
    
- [Senden von Benachrichtigungen und Anzeigen von Richtlinientipps für DLP-Richtlinien](use-notifications-and-policy-tips.md)
    
- [Inhalt der DLP-Richtlinienvorlagen](what-the-dlp-policy-templates-include.md)
    
- [Verfügbare Arten von vertraulichen Informationen](what-the-sensitive-information-types-look-for.md)
    

