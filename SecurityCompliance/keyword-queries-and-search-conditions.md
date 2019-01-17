---
title: Stichwortabfragen und Suchbedingungen für die Inhaltssuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.SearchQueryLearnMore
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: c4639c2e-7223-4302-8e0d-b6e10f1c3be3
description: 'Erfahren Sie mehr über die Eigenschaften für e-Mail- und -Datei, die in Exchange Online-Postfächern und SharePoint oder OneDrive for Business-Websites mit dem Tool für die Inhaltssuche in die Office 365-Sicherheit suchen können &amp; Compliance Center.  '
ms.openlocfilehash: c1b5c3721a892929535a7e699201d0bcfc39937b
ms.sourcegitcommit: a2afa4c06e9b762cf689b0d2a0653076f9b00c49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28328161"
---
# <a name="keyword-queries-and-search-conditions-for-content-search"></a>Stichwortabfragen und Suchbedingungen für die Inhaltssuche

In diesem Thema werden die e-Mails und Dokument-Eigenschaften, die Sie in der e-Mail-Elemente in Exchange Online und in SharePoint gespeicherten Dokumenten suchen können und OneDrive for Business-Websites mithilfe der Suchfunktion von Inhalt in die Office 365-Sicherheit &amp; Compliance Zentriert. Sie können auch die ** \*- ComplianceSearch** -Cmdlets in Security &amp; Compliance Center PowerShell zu suchenden diese Eigenschaften. Das Thema wird außerdem beschrieben:   
  
- Verwenden Sie boolesche Suche Operatoren, suchbedingungen und anderen Techniken der Search-Abfrage, um Ihre Suchergebnisse zu verbessern.
    
- Suchen nach vertraulichen Datentypen und benutzerdefinierte vertrauliche Daten Inhaltstypen in SharePoint und OneDrive für Unternehmen.
    
- Websiteinhalt gesucht, die mit Benutzern außerhalb Ihres Unternehmens gemeinsam genutzt wird
    
Schrittweise Anleitung zum Erstellen einer Inhaltssuche finden Sie unter [Content-Suche in Office 365](content-search.md). |

  
> [!NOTE]
> Content-Suche in das Wertpapier &amp; Compliance Center und die entsprechenden ** \*- ComplianceSearch** -Cmdlets in Security &amp; Compliance Center PowerShell Keyword Query Language (KQL) verwenden. Ausführlichere Informationen finden Sie unter [Keyword Query Language-Syntax-Referenz](https://go.microsoft.com/fwlink/?LinkId=269603). 
  
## <a name="searchable-email-properties"></a>Durchsuchbare E-Mail-Eigenschaften

Die folgende Tabelle enthält die e-Mail-Nachricht-Eigenschaften, die durchsucht werden können, mithilfe der Suchfunktion von Inhalt in das Wertpapier &amp; Compliance Center oder mithilfe der **New-ComplianceSearch** oder das Cmdlet **Set-ComplianceSearch** . Die Tabelle enthält ein Beispiel für die Syntax der _Eigenschaftswert:_ für jede Eigenschaft und eine Beschreibung der Suchergebnisse von den Beispielen zurückgegeben. Geben Sie diese `property:value` -Paare in die Schlüsselwörter für ein Inhaltssuche Feld. 
  
|**Eigenschaft**|**Beschreibung der Eigenschaft**|**Beispiele**|**Von den Beispielen zurückgegebene Suchergebnisse**|
|:-----|:-----|:-----|:-----|
|AttachmentNames  <br/> |Die Namen der an eine E-Mail angefügten Dateien.  <br/> |`attachmentnames:annualreport.ppt`  <br/> `attachmentnames:annual*`  <br/> |Nachrichten, die in der Anlage eine Datei mit dem Namen „Jahresbericht.ppt“ haben. Im zweiten Beispiel werden, wenn Sie das Platzhalterzeichen verwenden, Nachrichten mit dem Wort „Jahresbericht“ im Dateinamen einer Anlage zurückgegeben.  <br/> |
|Bcc  <br/> |Das Feld „BCC" einer E-Mail-Nachricht.<sup>1</sup> <br/> |`bcc:pilarp@contoso.com`  <br/> `bcc:pilarp`  <br/> `bcc:"Pilar Pinilla"`  <br/> |In allen Beispielen werden Nachrichten mit dem Namen "Pilar Pinilla" im Bcc-Feld zurückgegeben.  <br/> |
|Kategorie  <br/> | Die Kategorien, nach denen gesucht wird. Kategorien können durch Benutzer mithilfe von Outlook oder Outlook Web App definiert werden. Die folgenden Werte sind möglich:  <br/><br/>  blau  <br/>  grün  <br/>  orange  <br/>  violett  <br/>  rot  <br/>  gelb  <br/> |`category:"Red Category"`  <br/> |Nachrichten, denen in den Quellpostfächern die rote Kategorie zugewiesen wurde.  <br/> |
|Cc  <br/> |Das Feld „CC" einer E-Mail-Nachricht.<sup>1</sup> <br/> |`cc:pilarp@contoso.com`  <br/> `cc:"Pilar Pinilla"`  <br/> |In beiden Fällen Nachrichten mit dem Namen "Pilar Pinilla" im CC-Feld.  <br/> |
|Folderid  <br/> |Der Ordner-ID (GUID) eines bestimmten Postfachordners. Wenn Sie diese Eigenschaft verwenden, müssen Sie unbedingt das Postfach zu suchen, dem in der angegebene Ordner gespeichert ist. Beachten Sie, dass nur die angegebene Ordner durchsucht werden. Alle Unterordner im Ordner wird nicht durchsucht werden. Um Unterordner zu suchen, müssen Sie die Folderid-Eigenschaft für den Unterordner verwenden, den Sie suchen möchten.<br/> Weitere Informationen zum Suchen nach die Folderid-Eigenschaft und mithilfe eines Skripts, um den Ordner IDs für ein bestimmtes Postfach zu erhalten finden Sie unter [Inhaltssuche in Office 365 für zielgerichtete Websitesammlungen verwenden](use-content-search-for-targeted-collections.md).  <br/> |`folderid:4D6DD7F943C29041A65787E30F02AD1F00000000013A0000`  <br/> `folderid:2370FB455F82FC44BE31397F47B632A70000000001160000 AND participants:garthf@contoso.com`  <br/> |Im erste Beispiel gibt alle Elemente in der angegebenen Postfachordner zurück. Im zweite Beispiel werden alle Elemente in der angegebenen Postfachordner, die gesendet oder Empfangen von garthf@contoso.com wurden zurück.  <br/> |
|Von  <br/> |Der Absender einer E-Mail-Nachricht.<sup>1</sup> <br/> |`from:pilarp@contoso.com`  <br/> `from:contoso.com`  <br/> |Nachrichten, die vom angegebenen Benutzer oder einer bestimmten Domäne gesendet wurden.  <br/> |
|HasAttachment  <br/> |Gibt an, ob eine Nachricht eine Anlage enthält. Verwenden Sie die Werte **true** oder **false**.<br/> |`from:pilar@contoso.com AND hasattachment:true`  <br/> |Der angegebene Benutzer gesendeten Nachrichten, die Anlagen enthalten.  <br/> |
|Wichtigkeit  <br/> |Die Wichtigkeit einer E-Mail-Nachricht, die ein Absender festlegen kann, wenn er eine Nachricht sendet. Standardmäßig werden Nachrichten mit normaler Wichtigkeit gesendet, außer wenn der Absender die Wichtigkeit auf **Hoch** oder **Niedrig** setzt.  <br/> |`importance:high`  <br/> `importance:medium`  <br/> `importance:low`  <br/> |Nachrichten, deren Wichtigkeit auf "Hoch", "Mittel" bzw. "Niedrig" eingestellt ist.  <br/> |
|IsRead  <br/> |Gibt an, ob Nachrichten gelesen wurden. Verwenden Sie die Werte **true** oder **false**.<br/> |`isread:true`  <br/> `isread:false`  <br/> |Im erste Beispiel gibt Nachrichten zurück, mit der IsRead-Eigenschaft auf **True**festgelegt. Im zweite Beispiel gibt Nachrichten zurück, mit der IsRead-Eigenschaft auf **False**festgelegt.<br/> |
|ItemClass  <br/> |Verwenden Sie diese Eigenschaft, um bestimmte Drittanbieter-Datentypen zu suchen, die Ihre Organisation in Office 365 importiert. Verwenden Sie für diese Eigenschaft die folgende Syntax:`itemclass:ipm.externaldata.<third-party data type>*` <br/> |`itemclass:ipm.externaldata.Facebook* AND subject:contoso`  <br/> `itemclass:ipm.externaldata.Twitter* AND from:"Ann Beebe" AND "Northwind Traders"`  <br/> |Im erste Beispiel gibt Facebook Elementen, die das Wort "Contoso" in die Subject-Eigenschaft zurück. Im zweite Beispiel gibt Twitter-Elemente, die von Ann Beebe bereitgestellt wurden und der Stichwortausdruck "Northwind Traders" enthalten.<br/> Eine vollständige Liste der Werte für Drittanbieter-Datentypen für die Eigenschaft "itemclass" verwenden finden Sie unter [Inhaltssuche verwenden, um Daten von Dritten zu suchen, die in Office 365 importiert wurde](use-content-search-to-search-third-party-data-that-was-imported.md).  <br/> |
|Art  <br/> | Der Typ des zu suchenden e-Mail-Nachricht. Mögliche Werte:  <br/>  contacts  <br/>  docs  <br/>  email  <br/>  externaldata  <br/>  faxes  <br/>  im  <br/>  journals  <br/>  meetings  <br/>  Microsoftteams (gibt Elemente von Chats, Besprechungen und Anrufe in Microsoft-Teams)  <br/>  notes  <br/>  posts  <br/>  rssfeeds  <br/>  tasks  <br/>  voicemail  <br/> |`kind:email`  <br/> `kind:email OR kind:im OR kind:voicemail`  <br/> `kind:externaldata`  <br/> |Im erste Beispiel gibt die e-Mail-Nachrichten, die den Suchkriterien entsprechen. Die zweiten Beispiel gibt e-Mail-Nachrichten, instant messaging-Unterhaltungen (einschließlich Skype für Business Unterhaltungen und Chats in Microsoft-Teams) und VoIP-Nachrichten, die den Suchkriterien entsprechen. Im dritte Beispiel gibt die Elemente, die auf Postfächer in Office 365 von Drittanbieter-Datenquellen wie Twitter, Facebook und Cisco Jabber, importiert wurden, die den Suchkriterien entsprechen. Weitere Informationen finden Sie unter [Archivierung Drittanbieter - Daten in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).<br/> |
|Teilnehmer  <br/> |Alle Felder mit Personen in einer E-Mail-Nachricht. Diese Felder sind „Von", „An", „CC" und „BCC".<sup>1</sup> <br/> |`participants:garthf@contoso.com`  <br/> `participants:contoso.com`  <br/> |Nachrichten, die von oder an garthf@contoso.com gesendet wurden. Im zweiten Beispiel werden alle Nachrichten zurückgegeben, die von oder an einen Benutzer in der Domäne contoso.com gesendet wurden.  <br/> |
|Empfangen  <br/> |Das Datum, an dem eine E-Mail-Nachricht von einem Empfänger empfangen wurde.  <br/> |`received:04/15/2016`  <br/> `received>=01/01/2016 AND received<=03/31/2016`  <br/> |Nachrichten, die auf 15 April 2016 empfangen wurden. Im zweite Beispiel gibt alle Nachrichten, die zwischen 1 Januar 2016 und 31 März 2016 zurück.  <br/> |
|Empfänger  <br/> |Alle Felder mit Empfängern in einer E-Mail-Nachricht. Diese Felder sind „An", „CC" und „BCC".<sup>1</sup> <br/> |`recipients:garthf@contoso.com`  <br/> `recipients:contoso.com`  <br/> |Nachrichten, die an garthf@contoso.com gesendet wurden. Im zweiten Beispiel werden Nachrichten zurückgegeben, die an einen Empfänger in der Domäne contoso.com gesendet wurden.  <br/> |
|Gesendet  <br/> |Das Datum, an dem eine E-Mail vom Absender gesendet wurde.  <br/> |`sent:07/01/2016`  <br/> `sent>=06/01/2016 AND sent<=07/01/2016`  <br/> |Nachrichten, die am angegebenen Tag oder im angegebenen Datumsbereich gesendet wurden.  <br/> |
|Größe  <br/> |Die Größe eines Elements in Byte.  <br/> |`size>26214400`  <br/> `size:1..1048567`  <br/> |Nachrichten, die größer als 25?? sein. MB. Im zweite Beispiel werden Nachrichten von 1 bis 1,048,567 Bytes (1 MB) zurückgegeben.  <br/> |
|Betreff  <br/> |Der Text in der Betreffzeile einer E-Mail.  <br/> **Hinweis:** Wenn Sie die Subject-Eigenschaft in einer Abfrage verwenden, gibt ???the Suche alle Nachrichten, die in denen die Betreffzeile den Text enthält, den, dem Sie suchen. Anders ausgedrückt, zurück nicht die Abfrage nur Nachrichten, die eine genaue Übereinstimmung aufweisen. Suchen Sie beispielsweise `subject:"Quarterly Financials"`, Ihre Ergebnisse Nachrichten mit dem Betreff "Quartal Finanzen 2018" enthalten.<br/> |`subject:"Quarterly Financials"`  <br/> `subject:northwind`  <br/> |Nachrichten, die den Begriff "Quartal Finanzen" an einer beliebigen Stelle in der Text der Betreffzeile enthalten. Im zweite Beispiel gibt alle Nachrichten, die Word Northwind in der Betreffzeile enthalten.  <br/> |
|An  <br/> |Das Feld „An" einer E-Mail-Nachricht.<sup>1</sup> <br/> |`to:annb@contoso.com`  <br/> `to:annb ` <br/> `to:"Ann Beebe"`  <br/> |In allen Beispielen wegen Nachrichten zurückgegeben, in deren Zeile "An" der Name "Ann Beebe" angegeben ist.  <br/> |
   
> [!NOTE]
> <sup>1</sup> für den Wert einer Eigenschaft Empfänger, Sie können e-Mail-Adresse (auch gewählte *Benutzerprinzipalnamen* oder UPN) verwenden, der Anzeigename oder Alias eines Benutzers an. Beispielsweise können Sie annb@contoso.com, Annb oder "Ann Beebe" verwenden, um den Benutzer Ann Beebe anzugeben.<br/><br/>Bei der Suche eine von den Empfängereigenschaften (From, To, Cc, Bcc, Teilnehmer und Empfänger), Office 365 versucht, um die Identität der einzelnen Benutzer Schlüsseltokens erweitern diese aus Azure Active Directory.  Wenn der Benutzer in Azure Active Directory gefunden wird, wird die Abfrage zum einschließen oder des Benutzers e-Mail-Adresse (UPN), alias, Anzeigename und LegacyExchangeDN erweitert.<br/><br/>Beispielsweise eine Abfrage wie `participants:ronnie@contoso.com` erweitert zu `participants:ronnie@contoso.com OR participants:ronnie OR participants:"Ronald Nelson" OR participants:"<LegacyExchangeDN>"`.

## <a name="searchable-site-properties"></a>Durchsuchbare Websiteeigenschaften

Die folgende Tabelle enthält einige der SharePoint und OneDrive für Unternehmen-Eigenschaften, die durchsucht werden können, mithilfe der Suchfunktion von Inhalt in das Wertpapier &amp; Compliance Center oder mithilfe der **New-ComplianceSearch** oder die ** Set-ComplianceSearch** Cmdlet. Die Tabelle enthält ein Beispiel für die Syntax der _Eigenschaftswert:_ für jede Eigenschaft und eine Beschreibung der Suchergebnisse von den Beispielen zurückgegeben. 
  
Eine vollständige Liste der SharePoint-Eigenschaften, die durchsucht werden können, finden Sie unter [Übersicht über durchforstete und verwaltete Eigenschaften in SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Eigenschaften mit **Ja** in der Spalte **Einstellung "Queryable"** markiert sind, können gesucht werden soll. 
  
|**Eigenschaft**|**Beschreibung der Eigenschaft**|**Beispiel**|**Von den Beispielen zurückgegebene Suchergebnisse**|
|:-----|:-----|:-----|:-----|
|Autor  <br/> |Autor Felds aus Office-Dokumenten, die weiterhin auf, wenn ein Dokument kopiert wird. Beispielsweise wenn ein Benutzer ein Dokument und die e-Mails erstellt wird, um eine andere Person, die er klicken Sie dann auf SharePoint, das Dokument hochgeladen weiterhin den ursprünglichen Autor beibehalten. Achten Sie darauf, dass der Benutzer Anzeigenamen für diese Eigenschaft verwenden.  <br/> |`author:"Garth Fort"`  <br/> |Alle Dokumente, die von Garth Fort erstellt wurden.  <br/> |
|ContentType  <br/> |Die SharePoint-Inhaltstyps eines Elements, wie etwa Element oder Dokument oder Video.  <br/> |`contenttype:document`  <br/> |Alle Dokumente würden zurückgegeben.  <br/> |
|Created  <br/> |Das Datum, an dem ein Element erstellt wird.  <br/> |`created\>=06/01/2016`  <br/> |Alle Elemente, die am oder nach 1 Juni 2016 erstellt wurden.  <br/> |
|CreatedBy  <br/> |Die Person, die erstellt oder hochgeladen ein Elements. Achten Sie darauf, dass der Benutzer Anzeigenamen für diese Eigenschaft verwenden.  <br/> |`createdby:"Garth Fort"`  <br/> |Alle Elemente, die von Garth Fort erstellt oder hochgeladen wurden.  <br/> |
|DetectedLanguage  <br/> |Die Sprache eines Elements.  <br/> |`detectedlanguage:english`  <br/> |Alle Elemente in Englisch.  <br/> |
|FileExtension  <br/> |Die Erweiterung einer Datei; beispielsweise Docx, einem, Pptx oder Xlsx.  <br/> |`fileextension:xlsx`  <br/> |Alle Excel-Dateien (Excel 2007 und später)  <br/> |
|Dateiname  <br/> |Der Name einer Datei.  <br/> |`filename:"marketing plan"`  <br/> `filename:estimate`  <br/> |Im ersten Beispiel werden Dateien mit den exakten Ausdruck "Marketingplan" im Titel zurückgegeben. Das zweite Beispiel gibt Dateien mit dem Wort "schätzen" im Dateinamen zurück.  <br/> |
|ZuletztGeändertUm  <br/> |Das Datum, an dem ein Element zuletzt geändert wurde.  <br/> |`lastmodifiedtime>=05/01/2016`  <br/> `lastmodifiedtime>=05/10/2016 AND lastmodifiedtime<=06/1/2016`  <br/> |Im erste Beispiel werden die Elemente, die an oder nach 1 Mai 2016 geändert wurden zurückgegeben. Im zweite Beispiel werden die Elemente, die zwischen 1 Mai 2016 und 1 Juni 2016 geändert zurückgegeben.  <br/> |
|ModifiedBy  <br/> |Die Person, die ein Element zuletzt geändert wurde. Achten Sie darauf, dass der Benutzer Anzeigenamen für diese Eigenschaft verwenden.  <br/> |`modifiedby:"Garth Fort"`  <br/> |Alle Elemente, die zuletzt von Garth Fort geändert wurden.  <br/> |
|Path  <br/> |Der Pfad (URL) eines bestimmten Ordners in einem SharePoint oder OneDrive for Business-Site. Wenn Sie diese Eigenschaft verwenden, müssen Sie die Website zu suchen, der in der angegebene Ordner gespeichert ist.<br/> Zum Zurückgeben von Elementen, die in Unterordnern im Ordner, den Sie für die Path-Eigenschaft angeben, müssen Sie hinzufügen /\* an die URL des angegebenen Ordners; Zum Beispiel`path: "https://contoso.sharepoint.com/Shared Documents/*"`  <br/> <br/> **Hinweis:** Mithilfe der `Path` -Eigenschaft auf OneDrive Speicherorte durchsuchen wird nicht Mediendateien wie PNG, TIFF oder WAV-Dateien in den Suchergebnissen zurück. Verwenden Sie eine andere Website-Eigenschaft in Ihrer Suchabfrage um zu suchenden Mediendateien in OneDrive-Ordner.<br/> <br/> Weitere Informationen zum Suchen nach die Path-Eigenschaft und Verwendung eines Skripts zum Pfad URLs für Ordner auf eine bestimmte Website zu erhalten finden Sie unter [Inhaltssuche in Office 365 für zielgerichtete Websitesammlungen verwenden](use-content-search-for-targeted-collections.md).  <br/> |`path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Private"`  <br/> `path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Shared with Everyone/*" AND filename:confidential`  <br/> |Im erste Beispiel gibt alle Elemente in der angegebenen OneDrive for Business-Ordner zurück. Im zweite Beispiel gibt Dokumente in der angegebenen Website-Ordner (und alle Unterordner), die das Wort "confidential" im Dateinamen enthalten.  <br/> |
|SharedWithUsersOWSUser  <br/> |Dokumente, die den angegebenen Benutzer freigegeben wurden und auf der Seite **freigegeben für mich** in OneDrive for Business-Standort des Benutzers angezeigt. Dies sind die Dokumente, die explizit mit dem angegebenen Benutzer von anderen Personen in Ihrer Organisation freigegeben wurden. Beim Exportieren von Dokumenten, die eine Suchabfrage entsprechen, die die SharedWithUsersOWSUser-Eigenschaft verwendet, werden die Dokumente aus der ursprünglichen Inhaltsspeicherort der Person, die das Dokument mit dem angegebenen Benutzer freigegeben, exportiert. Weitere Informationen finden Sie unter [Suchen für Websiteinhalte freigegebene innerhalb Ihrer Organisation](keyword-queries-and-search-conditions.md#internal).<br/> |`sharedwithusersowsuser:garthf`  <br/> `sharedwithusersowsuser:"garthf@contoso.com"`  <br/> |Beispiele für alle internen explizit mit Gert freigegeben wurden haben und Dokumente, die auf der Seite **freigegeben für mich** des Gert angezeigt werden zurückzugeben OneDrive for Business-Konto.  <br/> |
|Website  <br/> |Die URL einer Website oder einer Gruppe von Websites in Ihrer Organisation.  <br/> |`site:"https://contoso-my.sharepoint.com"`  <br/> `site:"https://contoso.sharepoint.com/sites/teams"`  <br/> |Im erste Beispiel gibt Elemente zurück, aus der OneDrive for Business-Websites für alle Benutzer in der Organisation. Im zweite Beispiel gibt Elemente aus allen Teamwebsites zurück.  <br/> |
|Größe  <br/> |Die Größe eines Elements in Byte.  <br/> |`size>=1`  <br/> `size:1..10000`  <br/> |Im ersten Beispiel werden Elemente zurückgegeben, die größer als 1 Byte sind. Im zweiten Beispiel werden Elemente mit einer Größe von 1 bis 10.000 Byte zurückgegeben.  <br/> |
|Title  <br/> |Der Titel des Dokuments. Die Title-Eigenschaft sind Metadaten, die in Microsoft Office-Dokumente angegeben ist. Es unterscheidet sich von der Dateiname des Dokuments.  <br/> |`title:"communication plan"`  <br/> |Jedes Dokument, das den Ausdruck "Kommunikationsplan" in der Title-Metadateneigenschaft eines Office-Dokuments enthält.  <br/> |
   
## <a name="searchable-contact-properties"></a>Durchsuchbare Kontaktinformationen

Die folgende Tabelle enthält die Kontakten-Eigenschaften, die indiziert sind und, dass Sie bei der Verwendung von Inhaltssuche suchen können. Dies sind die Eigenschaften, die für Benutzer so konfigurieren Sie für die Kontakte (auch als persönliche Kontakte bezeichnet), die in das persönliche Adressbuch des Postfachs eines Benutzers befinden verfügbar sind. Zum Suchen von Kontakten können Sie die Postfächer suchen, und klicken Sie dann in der Stichwortabfrage Verwenden einer oder mehrerer Kontakt Eigenschaften auswählen.
  
> [!TIP]
> Um Werte suchen, Leerzeichen und Sonderzeichen enthalten, verwenden Sie doppelte Anführungszeichen ("") auf den Ausdruck; enthalten beispielsweise `businessaddress:"123 Main Street"`. 
  
|**Eigenschaft**|**Beschreibung der Eigenschaft**|
|:-----|:-----|
|BusinessAddress  <br/> |Die Adresse in der **Geschäftsadresse** -Eigenschaft. Die Eigenschaft wird auch **die Geschäftsadresse** auf der Seite Kontakt Eigenschaften bezeichnet.<br/> |
|BusinessPhone  <br/> |Die Telefonnummer in das **Telefon (geschäftlich)** eines Zahlenformatvorlage Eigenschaften.  <br/> |
|Firma  <br/> |Der Name in der **Company** -Eigenschaft.  <br/> |
|Abteilung  <br/> |Der Name in der **Abteilung** -Eigenschaft.  <br/> |
|DisplayName  <br/> |Der Anzeigename des Kontakts. Dies ist der Name in der **Vollständige Name** -Eigenschaft des Kontakts.<br/> |
|EmailAddress  <br/> |Die Adresse für eine beliebige e-Mail-Adresse-Eigenschaft für den Kontakt. Beachten Sie, dass Benutzer mehrere e-Mail-Adressen für einen Kontakt hinzufügen können. Die Verwendung dieser Eigenschaft würde Kontakte zurückgeben, die einer e-Mail-Adressen des Kontakts entsprechen.  <br/> |
|FileAs  <br/> |Die **Datei als** -Eigenschaft. Diese Eigenschaft wird verwendet, um anzugeben, wie der Kontakt in der Kontaktliste des Benutzers aufgeführt ist. Beispielsweise könnten ein Kontakt als *Vorname, Nachname* oder *LastName, FirstName* aufgelistet werden.<br/> |
|Vorname  <br/> |Der Name in der **erste Name** -Eigenschaft.  <br/> |
|HomeAddress  <br/> |Die Adresse im **Home** Eigenschaften.  <br/> |
|HomePhone  <br/> |Die Telefonnummer in das Telefon ( **Privat** ) eines Zahlenformatvorlage Eigenschaften.  <br/> |
|IMAddress  <br/> |Die Instant Messaging-Adresse-Eigenschaft, die in der Regel eine e-Mail-Adresse für Sofortnachrichten verwendet wird.  <br/> |
|MiddleName  <br/> |Der Name in der **mittleren** Name-Eigenschaft.  <br/> |
|MobilePhone  <br/> |Die Telefonnummer in **das Mobiltelefon** number-Eigenschaft.  <br/> |
|Nickname  <br/> |Der Name in der **Nickname** -Eigenschaft.  <br/> |
|OfficeLocation  <br/> |Der Wert in **Office** oder **Bürostandort** -Eigenschaft.  <br/> |
|OtherAddress  <br/> |Der Wert für **die Address-Eigenschaft** .  <br/> |
|Surname  <br/> |Der Name in der **letzten** Name-Eigenschaft.  <br/> |
|Position  <br/> |Der Titel in der **Position** -Eigenschaft.  <br/> |
   

## <a name="searchable-sensitive-data-types"></a>Durchsuchbare vertrauliche Datentypen

Sie können das Feature für die Inhaltssuche in das Wertpapier &amp; Compliance Center für die Suche nach vertrauliche Daten wie Kreditkarte Zahlen oder Sozialversicherungsnummern, die in Dokumenten auf SharePoint und OneDrive for Business-Websites gespeichert ist. Hierzu können Sie mithilfe der `SensitiveType` -Eigenschaft und der Name einer vertrauliche Informationen in einer schlüsselwortabfrage geben. Beispiel: die Abfrage `SensitiveType:"Credit Card Number"` Dokumente, die eine Kreditkartennummer enthalten. Die Abfrage `SensitiveType:"U.S. Social Security Number (SSN)"` Dokumente, die eine US-Sozialversicherungsnummer enthält. Um eine Liste der Typen vertrauliche Daten anzuzeigen, die Sie ermitteln können, wechseln Sie zu **Klassifikationen** \> **Typen vertraulicher Informationen** in das Wertpapier &amp; Compliance Center. Sie können auch das Cmdlet **Get-DlpSensitiveInformationType** in das Wertpapier &amp; Compliance Center PowerShell, um eine Liste der Typen vertraulicher Informationen anzuzeigen. 
  
Sie können auch die `SensitiveType` -Eigenschaft auf die Suche nach dem Namen eines Typs benutzerdefinierte vertrauliche Informationen, die Sie (oder ein anderer Administrator) für Ihre Organisation erstellt. Beachten Sie, dass Sie die **Publisher** -Spalte auf der Seite **Typen vertraulicher Informationen** in das Wertpapier &amp; Compliance Center (oder die **Publisher** -Eigenschaft in PowerShell) zur Unterscheidung zwischen integrierten und benutzerdefinierten Sensitive Typen von Informationen. Weitere Informationen finden Sie unter [Erstellen einer benutzerdefinierten vertrauliche Informationen-Typ](create-a-custom-sensitive-information-type.md).
  
Weitere Informationen zum Erstellen von Abfragen mithilfe der `SensitiveType` -Eigenschaft, finden Sie unter [Form einer Abfrage, vertrauliche Daten auf Websites zu erhalten](form-a-query-to-find-sensitive-data-stored-on-sites.md).
  
## <a name="search-operators"></a>Suchoperatoren

Boolesche Suche Operatoren wie **AND**, **OR**und **nicht**, können Sie die mehr präzise Suchvorgänge definieren, indem Sie ein- oder Ausschließen von bestimmten Wörtern in der Suchabfrage. Andere Techniken, wie mit eigenschaftsoperatoren (z. B. \>= oder...), Anführungszeichen, Klammern und Platzhalter helfen Ihnen bei der Optimierung einer Suchabfrage. Die folgende Tabelle enthält die Operatoren, die Sie zum Eingrenzen oder Erweitern der Suchergebnisse verwenden können. 
  
|**Operator**|**Verwendung**|**Beschreibung**|
|:-----|:-----|:-----|
|AND  <br/> |Wort1 AND Wort2  <br/> |Gibt die Elemente, die alle angegebenen Schlüsselwörter enthalten oder `property:value` Ausdrücke. Beispielsweise `from:"Ann Beebe" AND subject:northwind` alle Nachrichten von Ann Beebe, der die Northwind Wort in der Betreffzeile enthalten zurück. <sup>2</sup> <br/> |
|+  <br/> |Schlüsselwort1 Schlüsselwort2 + Schlüsselwort3  <br/> |Gibt die Elemente zurück, die  *entweder*  `keyword2` oder  `keyword3` *enthalten und*  , die ebenfalls  `keyword1` enthalten. Damit entspricht dieses Beispiel der Abfrage  `(keyword2 OR keyword3) AND keyword1`.  <br/> Beachten Sie, dass die Abfrage  `keyword1 + keyword2` (mit einem Leerzeichen nach dem **+** -Symbol) nicht der Verwendung des ** UND ** -Operators entspricht. Diese Abfrage wäre gleichbedeutend mit  `"keyword1 + keyword2"` und gibt Elemente mit dem exakten Ausdruck  `"keyword1 + keyword2"` zurück.  <br/> |
|ODER  <br/> |Wort1 OR Wort2  <br/> |Gibt die Elemente, die eine oder mehrere der angegebenen Schlüsselwörter enthalten oder `property:value` Ausdrücke. <sup>2</sup> <br/> |
|NOT  <br/> |Wort1 NOT Wort2  <br/> NOT Von:"Ann Beebe"  <br/> NICHT Art: Instant Messaging  <br/> |Schließt ein Schlüsselwort angegeben oder eine `property:value` Ausdruck. In der zweiten schließt Beispiel von Ann Beebe gesendete Nachrichten. Im dritte Beispiel schließt alle Sofortnachrichtenunterhaltungen wie Skype für Business Unterhaltungen, die die Postfach-Ordner Unterhaltungsverlauf gespeichert sind. <sup>2</sup> <br/> |
|-  <br/> |Wort1 - Wort2  <br/> |Identisch mit der **nicht** -Operator. Damit diese Abfrage gibt Elemente zurück, die enthalten `keyword1` und Ausschließen von Elementen, die enthalten würde `keyword2`.<br/> |
|NEAR  <br/> |Wort1 NEAR(n) Wort2  <br/> |Gibt Elemente mit Wörter, die nahe beieinander, sind zurück, wobei n die Anzahl der Wörter auseinander entspricht. Beispielsweise `best NEAR(5) worst` zurückgegeben, für jedes Element ist das Wort "schlechtesten" innerhalb von fünf Wörtern von "beste". Wenn keine Zahl angegeben wird, ist der Standardabstand acht Wörter. <sup>2</sup> <br/> |
|ONEAR  <br/> |Wort1 NEAR(n) Wort2  <br/> |Vergleichbar mit der **in der Nähe**, aber Elemente mit Wörter, die nahe beieinander, in der angegebenen Reihenfolge sind zurückgegeben. Beispielsweise `best ONEAR(5) worst` jedes Element, in denen das Wort "am besten" tritt auf, bevor Sie das Wort "schlechtesten" und die beiden Wörter eingeladenen fünf Wörter voneinander, zurückgegeben. Wenn keine Zahl angegeben wird, ist der Standardabstand acht Wörter. <sup>2</sup> <br/> > [!NOTE]> **ONEAR** -Operator wird nicht unterstützt, bei der Suche Postfächer; Es funktioniert nur bei der Suche von SharePoint und OneDrive for Business-Websites. Wenn Sie Postfächer und Websites in derselben Suche gesucht und die Abfrage den **ONEAR** -Operator enthält, wird die Suche Postfachelemente zurück, als ob Sie den **NEAR** -Operator verwendet haben. Anders ausgedrückt, gibt die Suche Elemente in denen angegebenen Wörter nahe beieinander sind, in denen die Wörter auftreten, unabhängig von der Reihenfolge zurück.           |
|:  <br/> |Eigenschaftswert  <br/> |Der Doppelpunkt (:)) in der `property:value` Syntax gibt an, dass der Wert der Eigenschaft gesucht wird den angegebenen Wert enthält. Beispielsweise `recipients:garthf@contoso.com` gibt alle an garthf@contoso.com gesendeten Nachrichten.<br/> |
|=  <br/> |Eigenschaft=Wert  <br/> |Identisch mit der **:** -Operator.  <br/> |
|\<  <br/> |Eigenschaft\<Wert  <br/> |Zeigt an, dass die Eigenschaft, nach der gesucht wird, kleiner ist als der angegebene Wert.<sup>1</sup> <br/> |
|\>  <br/> |Eigenschaft\>Wert  <br/> |Zeigt an, dass die Eigenschaft, nach der gesucht wird, größer ist als der angegebene Wert.<sup>1</sup> <br/> |
|\<=  <br/> |Eigenschaft\<=Wert  <br/> |Zeigt an, dass die Eigenschaft, nach der gesucht wird, kleiner gleich dem angegebenen Wert ist.<sup>1</sup> <br/> |
|\>=  <br/> |Eigenschaft\>=Wert  <br/> |Zeigt an, dass die Eigenschaft, nach der gesucht wird, größer gleich dem angegebenen Wert ist.<sup>1</sup> <br/> |
|..  <br/> |Eigenschaft: Wert1... Wert2  <br/> |Zeigt an, dass die Eigenschaft, nach der gesucht wird, größer gleich Wert1 und kleiner gleich Wert2 ist.<sup>1</sup> <br/> |
|"  "  <br/> |"fair Value"  <br/> Betreff:"Vierteljährliche Finanzdaten"  <br/> |Verwenden Sie doppelte Anführungszeichen ("") für einen exakten Ausdruck oder Begriff in Schlüsselwort suchen und `property:value` Suchabfragen.  <br/> |
|\*  <br/> |cat\*  <br/> Betreff:set\*  <br/> |Präfix Platzhaltersuche (, in dem das Sternchen wird am Ende eines Worts platziert) für NULL oder mehr Zeichen in Schlüsselwörtern übereinstimmen oder `property:value` Abfragen. Beispielsweise `title:set*` Dokumente, die den Satz von Word, Setup, Einstellung (sowie andere Wörter, die mit "Set" beginnen) enthalten in den Titel des Dokuments zurückgegeben.<br/><br/> **Hinweis:** Sie können nur die Platzhaltersuche Präfix verwenden. beispielsweise **Katze\* ** oder **festgelegt\***. Suffix Suchvorgänge ( ** \*Katze** ), infix-Suchvorgänge ( **c\*t** ), und Suchvorgänge Teilzeichenfolgen ( ** \*Katze\* ** ) werden nicht unterstützt.           |
|(  )  <br/> | (fair OR frei) AND (Von:contoso.com)  <br/> (IPO OR Initiale) AND (Aktien OR Anteile)  <br/> (Vierteljährliche Finanzdaten)  <br/> |Mit Klammern werden Boolesche Ausdrücke,  `property:value`-Elemente und Schlüsselwörter gruppiert.  `(quarterly financials)` gibt z. B. Elemente zurück, die die Wörter "Vierteljährliche" und "Finanzdaten" enthalten.  <br/> |
   
> [!NOTE]
> Verwenden Sie <sup>1</sup> diesen Operator für Eigenschaften, die Datum oder numerischen Werte besitzen.<br/> <sup>2</sup> boolesche Suchoperatoren müssen in Großbuchstaben sein. beispielsweise **und**. Wenn Sie einen Kleinbuchstaben Operator, wie **und**, wird diese als ein Schlüsselwort in der Suchabfrage behandelt. 
  
## <a name="search-conditions"></a>Suchbedingungen

Sie können Bedingungen hinzufügen, um eine Suchabfrage aus, um eine Suche einzugrenzen und eine genauere Ergebnisse zurückgeben. Jede Bedingung hinzugefügt der KQL Search-Abfrage, die erstellt und ausgeführt werden, wenn Sie die Suche starten eine-Klausel.
  
[Bedingungen für allgemeine Eigenschaften ](#conditions-for-common-properties)

[Bedingungen für E-Mail-Eigenschaften](#conditions-for-mail-properties)

[Bedingungen für Dokumenteigenschaften ](#conditions-for-document-properties)

[Mit Bedingungen verwendete Operatoren](#operators-used-with-conditions)

[Richtlinien für die Verwendung von Bedingungen](#guidelines-for-using-conditions)

[Beispiele](#examples-of-using-conditions-in-search-queries)
  
### <a name="conditions-for-common-properties"></a>Bedingungen für allgemeine Eigenschaften 

Erstellen Sie eine Bedingung mit allgemeinen Eigenschaften, Postfächer und Websites in derselben Suche zu suchen. Die folgende Tabelle enthält die verfügbaren Eigenschaften zu verwenden, wenn eine Bedingung hinzufügen.
  
|**Bedingung**|**Beschreibung**|
|:-----|:-----|
|Datum  <br/> |Für e-Mails die, wurde das Datum, an dem Nachricht eines Empfängers oder vom Absender gesendet. Für Dokumente, das Datum, an das einem Dokument zuletzt geändert wurde.  <br/> |
|Absender/Autor  <br/> |Für e-Mails, die die Person, die eine Nachricht gesendet. Für Dokumente, die Person, die im Autorenfeld von Office-Dokumente genannt. Sie können mehrere Namen, durch Kommas getrennt eingeben. Zwei oder mehr Werte werden durch den Operator **oder** logisch verbunden.<br/> |
|Größe (in Bytes)  <br/> |Sowohl bei E-Mails als auch bei Dokumenten die Größe des Elements (in Byte).  <br/> |
|Betreff/Titel  <br/> |Für e-Mails, die den Text in der Betreffzeile einer Nachricht. Für Dokumente, die den Titel des Dokuments. Wie bereits erklärt ist die Title-Eigenschaft angegebenen in Microsoft Office-Dokumenten Metadaten. Sie können den Namen der mehr als eine Betreff/Titel, durch Kommas getrennt eingeben. Zwei oder mehr Werte werden durch den Operator **oder** logisch verbunden.<br/> |
|Compliancetag  <br/> |Für e-Mails und Dokumente haben Beschriftungen, die zugewiesen wurden, Nachrichten und Dokumente automatisch Bezeichnung Richtlinien oder Etiketten, die vom Benutzer manuell zugewiesen wurden. Etiketten dienen zum Klassifizieren von e-Mails und Dokumente für Daten Governance und Erzwingen von Aufbewahrungsregeln basierend auf der Klassifikation durch die Bezeichnung definiert. Geben Sie den Namen der Bezeichnung Teil und einen Platzhalter verwenden, oder geben Sie den Namen der Bezeichnung abgeschlossen. Weitere Informationen finden Sie unter [Übersicht über die Beschriftungen in Office 365](labels.md).<br/> |
  
### <a name="conditions-for-mail-properties"></a>Bedingungen für E-Mail-Eigenschaften

Erstellen Sie eine Bedingung unter Verwendung von E-Mail-Eigenschaften beim Durchsuchen von Postfächern oder öffentlichen Ordnern. Die folgende Tabelle enthält die E-Mail-Eigenschaften, die Sie für eine Bedingung verwenden können. Beachten Sie, dass diese Eigenschaften eine Teilmenge der bereits beschriebenen E-Mail-Eigenschaften darstellen. Diese Beschreibungen werden der Einfachheit halber wiederholt.
  
|**Bedingung**|**Beschreibung**|
|:-----|:-----|
|Art der Nachricht  <br/> | Der Nachrichtentyp zu suchen. Dies ist die gleiche Eigenschaft wie die Kind-e-Mail-Eigenschaft. Mögliche Werte:  <br/><br/>  contacts  <br/>  docs  <br/>  email  <br/>  externaldata  <br/>  faxes  <br/>  im  <br/>  journals  <br/>  meetings  <br/>  microsoftteams  <br/>  notes  <br/>  posts  <br/>  rssfeeds  <br/>  tasks  <br/>  voicemail  <br/> |
|Teilnehmer  <br/> |Alle Felder mit Personen in einer E-Mail-Nachricht. Diese Felder sind "Von", "An", "CC" und "BCC".  <br/> |
|Typ  <br/> |Die Klasse Message-Eigenschaft für ein e-Mail-Element. Dies ist die gleiche Eigenschaft als ItemClass e-Mail-Eigenschaft. Es ist außerdem eine Bedingung mit mehreren Werten. Damit mehrere Nachrichtenklassen ausgewählt haben, halten Sie die **STRG** -Taste, und klicken Sie dann auf zwei oder mehr Nachrichtenklassen in der Dropdown-Liste, die Sie die Bedingung hinzufügen möchten. Jede Nachrichtenklasse, die Sie in der Liste auswählen wird durch den Operator **oder** in der entsprechenden Suchabfrage logisch verbunden.<br/> Eine Liste mit den Nachrichtenklassen (und ihre entsprechenden ID der Nachrichtenklasse), die von Exchange verwendet werden und, die Sie in der Liste der **Nachrichtenklasse** auswählen können finden Sie unter [Item Types and Message Classes](https://go.microsoft.com/fwlink/?linkid=848143).  <br/> |
|Received  <br/> |Das Datum, an dem eine E-Mail-Nachricht von einem Empfänger empfangen wurde. Dies ist die gleiche Eigenschaft wie die E-Mail-Eigenschaft „Empfangen“.  <br/> |
|Empfänger  <br/> |An wurde die Person, die eine e-Mail-Nachricht gesendet. Dies ist die gleiche Eigenschaft als der To-e-Mail-Eigenschaft.  <br/> |
|Absender  <br/> |Der Absender einer E-Mail-Nachricht.  <br/> |
|Sent  <br/> |Das Datum, das vom Absender eine e-Mail-Nachricht gesendet wurde. Dies ist die gleiche Eigenschaft als gesendete e-Mail-Eigenschaft.  <br/> |
|Betreff  <br/> |Der Text in der Betreffzeile einer E-Mail.  <br/> |
|An  <br/> |Der Empfänger einer e-Mail-Nachricht.  <br/> |
  
### <a name="conditions-for-document-properties"></a>Bedingungen für Dokumenteigenschaften 

Erstellen Sie eine Bedingung mit Dokumenteigenschaften, bei der Suche nach Dokumenten auf SharePoint und OneDrive for Business-Websites. Die folgende Tabelle enthält die Eigenschaften, die Sie für eine Bedingung verwenden können. Beachten Sie, dass diese Eigenschaften eine Teilmenge der Eigenschaften des Standorts, die weiter oben beschrieben wurden. Diese Beschreibungen sind zu diesem Zweck wiederholt.
  
|**Bedingung**|**Beschreibung**|
|:-----|:-----|
|Autor  <br/> |Autor Felds aus Office-Dokumenten, die weiterhin auf, wenn ein Dokument kopiert wird. Beispielsweise wenn ein Benutzer ein Dokument und die e-Mails erstellt wird, um eine andere Person, die er klicken Sie dann auf SharePoint, das Dokument hochgeladen weiterhin den ursprünglichen Autor beibehalten.  <br/> |
|Position  <br/> |Der Titel des Dokuments. Die Title-Eigenschaft sind Metadaten, die in Office-Dokumenten angegeben ist. Es ist anders als der Dateiname des Dokuments.  <br/> |
|Created  <br/> |Das Datum, an dem ein Dokument erstellt wird.  <br/> |
|Zuletzt geändert  <br/> |Das Datum, an dem ein Dokument zuletzt geändert wurde.  <br/> |
|Dateityp  <br/> |Die Erweiterung einer Datei; beispielsweise Docx, einem, Pptx oder Xlsx. Dies ist die gleiche Eigenschaft als FileExtension Website-Eigenschaft.  <br/> |
  
### <a name="operators-used-with-conditions"></a>Mit Bedingungen verwendete Operatoren

Beim Hinzufügen einer Bedingung können Sie einen Operator auswählen, der für den Typ der Eigenschaft für die Bedingung relevant ist. Die folgende Tabelle enthält die mit Bedingungen verwendeten Operatoren und die dazugehörigen Entsprechungen, die in der Suchabfrage verwendet werden.
  
|**Operator**|**Entsprechung in der Abfrage**|**Beschreibung**|
|:-----|:-----|:-----|
|After  <br/> |`property>date`  <br/> |Wird mit Datumsbedingungen verwendet. Gibt die Elemente zurück, die nach dem angegebenen Datum gesendet, empfangen oder geändert wurden.   <br/> |
|Before  <br/> |`property<date`  <br/> |Wird mit Datumsbedingungen verwendet. Gibt die Elemente zurück, die vor dem angegebenen Datum gesendet, empfangen oder geändert wurden.  <br/> |
|Between  <br/> |`date..date`  <br/> |Verwenden Sie mit Datum und die Größe Bedingungen. Bei Verwendung mit einer Bedingung Datum wurden es gibt Elemente gesendet, empfangen oder innerhalb des angegebenen Datumsbereichs geändert. Bei Verwendung mit einer Größe Bedingung gibt Elemente, deren Größe innerhalb des angegebenen Bereichs liegt.  <br/> |
|Contains any of  <br/> |`(property:value) OR (property:value)`  <br/> |Verwendet mit Bedingungen für Eigenschaften, die einen String-Wert angeben. Gibt Elemente zurück, die einem beliebigen Teil des Werte für eine oder mehrere angegebene Zeichenfolge enthalten.  <br/> |
|Doesn't contain any of  <br/> |`-property:value`  <br/> `NOT property:value`  <br/> |Wird mit Bedingungen für Eigenschaften verwendet, die einen Zeichenfolgenwert angeben. Gibt Elemente zurück, die keinen Teil des angegebenen Zeichenfolgenwerts enthalten.  <br/> |
|Doesn't equal any of
  <br/> |`-property=value`  <br/> `NOT property=value`  <br/> |Wird mit Bedingungen für Eigenschaften verwendet, die einen Zeichenfolgenwert angeben. Gibt Elemente zurück, die die angegebene Zeichenfolge nicht enthalten.  <br/> |
|Equals  <br/> |`size=value`  <br/> |Gibt Elemente zurück, die der angegebenen Größe entsprechen.<sup>1</sup> <br/> |
|Equals any of  <br/> |`(property=value) OR (property=value)`  <br/> |Wird mit Bedingungen für Eigenschaften verwendet, die einen Zeichenfolgenwert angeben. Gibt Elemente zurück, die genau den angegebenen Zeichenfolgenwerten entsprechen.  <br/> |
|Greater  <br/> |`size>value`  <br/> |Gibt Elemente zurück, in denen die angegebene Eigenschaft größer als der angegebene Wert ist.<sup>1</sup> <br/> |
|Greater or equal  <br/> |`size>=value`  <br/> |Gibt Elemente zurück, in denen die angegebene Eigenschaft größer als oder gleich dem angegebenen Wert ist.<sup>1</sup> <br/> |
|Less  <br/> |`size<value`  <br/> |Gibt Elemente zurück, die größer als oder gleich dem angegebenen Wert sind.<sup>1</sup> <br/> |
|Less or equal  <br/> |`size<=value`  <br/> |Gibt Elemente zurück, die größer als oder gleich dem angegebenen Wert sind.<sup>1</sup> <br/> |
|Not equal  <br/> |`size<>value`  <br/> | Gibt Elemente zurück, die nicht der angegebenen Größe entsprechen.<sup>1</sup> <br/> |
   
> [!NOTE]
> <sup>1</sup> dieser Operator steht nur für Situationen, in denen die Size-Eigenschaft verwendet. 
  
### <a name="guidelines-for-using-conditions"></a>Richtlinien für die Verwendung von Bedingungen

Beachten Sie Folgendes bei der Verwendung von Suchbedingungen:
  
- Eine Bedingung ist logisch mit der Stichwortabfrage (im Schlüsselwort angegeben) durch den **AND** -Operator verbunden. Dies bedeutet, dass Elemente erfüllen der Stichwortabfrage und die Bedingung, die in den Ergebnissen enthalten sein müssen. Dies ist die Bedingungen wie helfen, um Ihre Suchergebnisse einzuschränken. 
    
- Wenn Sie zwei oder mehr eindeutige Bedingungen auf eine Suchabfrage (Conditions, die verschiedene Eigenschaften angeben) hinzufügen, werden diese Probleme logisch durch **AND** -Operator verbunden. Dies bedeutet, dass nur die Elemente, die alle Bedingungen (zusätzlich zum alle Stichwortabfrage) erfüllen zurückgegeben werden. 
    
- Wenn Sie mehr als eine Bedingung für die gleiche Eigenschaft hinzufügen, werden die Suchkriterien logisch durch **oder** -Operator verbunden. Dies bedeutet, dass Elemente, die die Stichwortabfrage und eine Bedingung erfüllen zurückgegeben werden. Also Gruppen der gleichen Bedingungen miteinander verbunden sind, mithilfe des Operators **OR** und legt der eindeutige Bedingungen durch den **AND** -Operator verbunden sind. 
    
- Wenn Sie mehrere Werte (durch Kommas oder Semikolons voneinander getrennt) zu einer einzelnen Bedingung hinzufügen, werden diese Werte durch den **oder** -Operator verbunden. Dies bedeutet, dass Elemente zurückgegeben werden, wenn sie eines der angegebenen Werte für die Eigenschaft in der Bedingung enthalten. 
    
- Search-Abfrage, die mithilfe der im Feld Stichwörter und Bedingungen erstellt wird, wird auf der Seite **Suche** im Detailbereich für die ausgewählte Suche angezeigt. In einer Abfrage, alles rechts neben der Notation `(c:c)` gibt Bedingungen, die die Abfrage hinzugefügt werden. 
    
- Bedingungen werden die Suchabfrage nur Eigenschaften hinzugefügt. die Operatoren nicht hinzufügen. Daher wird die Abfrage im Detailbereich angezeigt Operatoren rechts neben der nicht angezeigt wird die `(c:c)` Notation. KQL fügt die logischen Operatoren (gemäß den Regeln bereits erklärt) beim Ausführen der Abfrage. 
    
- Sie können das Ziehen und Ablegen verwenden-Steuerelement, um die Reihenfolge der Bedingungen neu geordnet. Klicken Sie auf das Steuerelement für eine Bedingung und nach oben oder nach unten.
    
- Wie bereits erklärt können einige Bedingungseigenschaften Sie mehrere Werte geben. Jeder Wert ist logisch durch den **oder** -Operator verbunden. Dies führt die gleiche Logik, da durch mehrere Instanzen der gleichen Bedingung, hat jeder einen single-Wert. Die folgende Abbildung zeigt ein Beispiel für eine einzelne Bedingung mit mehreren Werten und ein Beispiel für mehrere Bedingungen (für die gleiche Eigenschaft) mit einem einzelnen Wert. Beispiele für Laufzeitfehler in der gleichen Abfrage:`(filetype="docx") OR (filetype="pptx") OR (filetype="xlsx")`
    
    ![Eine Bedingung mit mehreren Werten](media/9880aa29-d117-4531-be20-6d53f1d21341.gif)
  
    ![Mehrere Suchkriterien für die gleiche Eigenschaft](media/1e63d37d-6d8d-4c9b-a509-a7e1c3a05193.gif)
  
> [!TIP]
> Wenn für eine Bedingung mehrere Werte zulässig sind, wird empfohlen, eine einzelne Bedingung mit mehreren Werten (durch Kommas oder Semikolons getrennt) zu verwenden. Auf diese Weise können Sie leichter sicherstellen, dass Sie die gewünschte Abfragelogik erhalten. 
  
### <a name="examples-of-using-conditions-in-search-queries"></a>Beispiele

Die folgenden Beispiele zeigen die GUI-basierte Version einer Suchabfrage mit Bedingungen, die Search-Abfragesyntax, die angezeigt wird, klicken Sie im Detailbereich der ausgewählten Suche (das auch durch das Cmdlet **Get-ComplianceSearch** zurückgegeben wird), und die Logik der entsprechende KQL-Abfrage. 
  
#### <a name="example-1"></a>Beispiel 1

Dieses Beispiel gibt Dokumente in SharePoint, und OneDrive for Business-Websites, die eine Kreditkartennummer enthalten und vor dem 1 Januar 2016 zuletzt geändert wurden.
  
 **GUI**
  
![Erstes Beispiel für Suchbedingungen](media/099515ba-d4ee-474e-af25-3aa48816b87b.gif)
  
 **Suchabfragesyntax**
  
 `SensitiveType:"Credit Card Number(c:c)(lastmodifiedtime<2016-01-01)`
  
 **Suchabfragelogik**
  
 `SensitiveType:"Credit Card Number" AND (lastmodifiedtime<2016-01-01)`
  
#### <a name="example-2"></a>Beispiel 2

In diesem Beispiel werden E-Mail-Elemente oder Dokumente zurückgegeben, die das Schlüsselwort "report" enthalten, die vor dem 1. April 2105 erstellt wurden und die das Wort "Northwind" in der Betreffzeile von E-Mail-Nachrichten oder in der Title-Eigenschaft von Dokumenten enthalten. Die Abfrage schließt Webseiten aus, die den anderen Suchkriterien entsprechen. 
  
 **GUI**
  
![Zweites Beispiel für Suchbedingungen](media/fe07d495-df81-42da-8106-3cdb409c6e7f.gif)
  
 **Suchabfragesyntax**
  
 `report(c:c)(date<2016-04-01)(subjecttitle:"northwind")(-filetype="aspx")`
  
 **Suchabfragelogik**
  
 `report AND (date<2016-04-01) AND (subjecttitle:"northwind") NOT (filetype="aspx")`
  
#### <a name="example-3"></a>Beispiel 3
<a name="conditionexamples"> </a>

Dieses Beispiel gibt die e-Mail-Nachrichten oder Kalender Besprechungen, die zwischen 12/1/2016 und 11/30/2016 gesendet wurden, und enthält Wörter, die mit "Tel:" oder "Smartphone" beginnen.
  
 **GUI**
  
![Drittes Beispiel für Suchbedingungen](media/973d45fc-0923-43d6-9d0a-25e4a625f057.gif)
  
 **Suchabfragesyntax**
  
 `phone* OR smartphone*(c:c)(sent=2016-12-01..2016-11-30)(kind="email")(kind="meetings")`
  
 **Suchabfragelogik**
  
 `phone* OR smartphone* AND (sent=2016-12-01..2016-11-30) AND ((kind="email") OR (kind="meetings"))`
  
## <a name="searching-for-site-content-shared-with-external-users"></a>Suchen nach Websiteinhalten, die für externe Benutzer freigegeben sind

Sie können auch das Inhaltssuche-Feature in das Wertpapier &amp; Compliance Center für die Suche nach Dokumenten auf SharePoint und OneDrive for Business-Websites, die mit Personen außerhalb Ihrer Organisation freigegeben wurden. Dadurch können Sie vertrauliche oder proprietäre Informationen zu identifizieren, die sich außerhalb Ihrer Organisation gemeinsam genutzt wird. Hierzu können Sie mithilfe der `ViewableByExternalUsers` -Eigenschaft in einem Stichwortabfrage. Diese Eigenschaft gibt zurück, Dokumenten oder Websites, die mit einer der folgenden Methoden sharing mit externen Benutzern freigegeben wurden: 
  
- Eine Einladung zur Freigabe, die Benutzer zur Anmeldung bei Ihrer Organisation als authentifizierter Benutzer erforderlich sind.
    
- Eine anonyme gastlink, dem jede Person mit diesen Link, um die Ressource zuzugreifen, ohne authentifiziert werden kann.
    
Hier sind einige Beispiele:
  
- Die Abfrage `ViewableByExternalUsers:true AND SensitiveType:"Credit Card Number"` werden alle Elemente, die mit Personen außerhalb Ihrer Organisation freigegeben und enthalten eine Kreditkartennummer zurückgegeben. 
    
- Die Abfrage `ViewableByExternalUsers:true AND ContentType:document AND site:"https://contoso.sharepoint.com/Sites/Teams"` gibt eine Liste der Dokumente zurück, auf alle Teamwebsites in der Organisation, die mit externen Benutzern freigegeben wurden. 
    
> [!TIP]
> Eine Suchabfrage wie `ViewableByExternalUsers:true AND ContentType:document` möglicherweise viele ASPX-Dateien in den Suchergebnissen zurück. Um diese (oder andere Typen von Dateien), zu beseitigen können die `FileExtension` -Eigenschaft auf Ausschließen bestimmter Dateitypen; beispielsweise `ViewableByExternalUsers:true AND ContentType:document NOT FileExtension:aspx`. 
  
Was gilt als Inhalte, die mit Personen außerhalb Ihrer Organisation freigegeben werden? Dokumente in Ihrer Organisation SharePoint und OneDrive for Business-Websites, die durch Senden einer Einladungen zur Freigabe feinere oder, der im öffentlichen Speicherorte gemeinsam genutzt werden. Beispielsweise führen die folgenden Benutzeraktivitäten Inhalte, die von externen Benutzern angezeigt werden:
  
- Ein Benutzer gibt eine Datei oder einen Ordner für eine Person außerhalb Ihrer Organisation frei.

    
- Ein Benutzer erstellt und einen Link zu einer freigegebenen Datei an eine Person außerhalb Ihrer Organisation sendet. Dieser Link ermöglicht es dem externen Benutzer die Datei anzeigen (oder bearbeiten).
    
- Ein Benutzer sendet eine Freigabeeinladung oder einen Gastlink an eine Person außerhalb Ihrer Organisation, um eine freigegebene Datei anzuzeigen (oder zu bearbeiten).
    
### <a name="issues-using-the-viewablebyexternalusers-property"></a>Probleme mit der ViewableByExternalUsers-Eigenschaft

Während der `ViewableByExternalUsers` Eigenschaft stellt den Status, ob ein Dokument oder einer Website mit externen Benutzern freigegeben ist, gibt es einige Warnhinweise, was diese Eigenschaft ist und nicht widerspiegeln. In den folgenden Szenarien, die den Wert der `ViewableByExternalUsers` -Eigenschaft wird nicht aktualisiert werden, und die Ergebnisse einer Inhaltssuche-Abfrage, die diese Eigenschaft verwendet werden. 
  
- Änderungen an der Freigaberichtlinie, wie externe Freigabe für eine Website oder für die Organisation deaktivieren. Die Eigenschaft wird weiterhin zuvor freigegebene Dokumente als extern zugänglichen, obwohl Sie externer Zugriff widerrufen haben möglicherweise angezeigt.
    
- Änderungen an der Gruppenmitgliedschaft wie hinzufügen oder Entfernen von externen Benutzern zu Office 365 Gruppen oder Office 365-Sicherheitsgruppen. Die Eigenschaft wird nicht automatisch für Elemente aktualisiert werden, die die Gruppe hat Zugriff auf.
    
- Sendende Einladungen zur Freigabe an externe Benutzer, in dem der Empfänger die Einladung noch nicht akzeptiert, und daher nicht noch, haben Zugriff auf die Inhalte.
    
In diesen Szenarien der `ViewableByExternalUsers` Eigenschaft wird nicht den aktuellen Status Freigabe widerzuspiegeln, bis die Website oder Dokumentbibliothek erneut durchforstet und erneut indiziert ist. 

## <a name="searching-for-site-content-shared-within-your-organization"></a>Suchen nach Websiteinhalt innerhalb Ihrer Organisation

Wie bereits erklärt, können Sie die `SharedWithUsersOWSUser` Eigenschaft so suchen Sie nach Dokumenten, die zwischen Personen in Ihrer Organisation freigegeben wurden. Wenn eine Person eine Datei (oder einen Ordner) mit einem anderen Benutzer innerhalb Ihres Unternehmens gemeinsam verwendet wird, wird auf der Seite **freigegeben für mich** in die OneDrive for Business-Konto der Person ein, die für die Datei freigegeben wurde ein Link zu der freigegebenen Datei angezeigt. Beispielsweise um für die Dokumente zu suchen, die mit Sara Davis freigegeben wurden, können die Abfrage `SharedWithUsersOWSUser:"sarad@contoso.com"`. Wenn Sie die Ergebnisse dieser Suche exportieren, werden die ursprüngliche Dokumente (befindet sich in der Speicherort des Inhalts der Person ein, die die Dokumente mit Sara gemeinsam genutzt) heruntergeladen werden.
  
Beachten Sie, dass Dokumente mit einem bestimmten Benutzer in den Suchergebnissen zurückgegeben werden soll, wenn mit explizit freigegeben werden müssen die `SharedWithUsersOWSUser` Eigenschaft. Wenn eine Person gemeinsam ein Dokument in ihrer OneDrive-Konto verwendet wird, haben sie die Option zum Weitergeben (innerhalb oder außerhalb der Organisation), nur für Personen innerhalb der Organisation freigeben oder einer bestimmten Person freigeben. Hier ist ein Screenshot des Fensters **Freigeben** in OneDrive, die die drei Freigabeoptionen anzeigt. 
  
![Nur für bestimmte Personen gemeinsam genutzte Dateien werden durch eine Suchabfrage zurückgegeben, die die SharedWithUsersOWSUser-Eigenschaft verwendet](media/469a4b61-68bd-4ab0-b612-ab6302973886.png)
  
Nur Dokumente, die gemeinsam genutzt werden, mithilfe der dritten Option (freigegebene für **bestimmte Benutzer**) zurückgegeben durch eine Search-Abfrage, verwendet die `SharedWithUsersOWSUser` Eigenschaft. 

## <a name="searching-for-skype-for-business-conversations"></a>Suchen nach Skype für Business Unterhaltungen

Die folgenden Stichwortabfrage können Sie speziell für Inhalte in Skype für Business Unterhaltungen suchen:

```
kind:im
```

Beachten Sie, dass die vorherige Suchabfrage aus Microsoft-Teams, auch Chats zurückgegeben wird. Um dies zu verhindern, können Sie die Suchergebnisse zum Einschließen von nur Skype für Business Unterhaltungen mithilfe der folgenden Stichwortabfrage einzuschränken:

```
kind:im AND subject:conversation
```

Der vorherigen Stichwortabfrage schließt Chats in Microsoft-Teams, da Skype für Business Unterhaltungen werden als e-Mail-Nachrichten mit einer Betreffzeile, die beginnt mit dem Wort "Unterhaltung" gespeichert.

Zum Skype für Business Unterhaltungen suchen, die innerhalb eines bestimmten Zeitraums aufgetreten sind, verwenden Sie die folgenden Stichwortabfrage:

```
kind:im AND subject:conversation AND (received=startdate..enddate)
```

## <a name="search-tips-and-tricks"></a>Tipps und Tricks für die Suche

- Schlüsselwortsuchen unterscheiden nicht zwischen Groß- und Kleinschreibung. Beispielsweise geben **katze** und **KATZE** dieselben Ergebnisse zurück. 
    
- Die booleschen Operatoren **AND**, **OR**, **nicht**, **NEAR**und **ONEAR** müssen in Großbuchstaben umgewandelt werden. 
    
- Ein Leerzeichen zwischen zwei Schlüsselwörter oder zwei `property:value` Ausdrücke ist identisch mit **AND**. Beispielsweise `from:"Sara Davis" subject:reorganization` gibt alle Sara Davis gesendete Nachrichten, die die Neuorganisation Wort in der Betreffzeile enthalten. 
    
- Verwenden Sie Syntax, die entspricht der `property:value` Format. Werte Groß-/Kleinschreibung nicht beachtet, und sie dürfen nicht nach dem Operator ein Leerzeichen besitzen. Ist ein Leerzeichen, werden Ihre beabsichtigte Wert nur eine Volltextsuche. Beispielsweise `to: pilarp` Suchvorgänge für "Pilarp" als Schlüsselwort, statt die Daten für Nachrichten, die an Pilarp gesendet wurden. 
    
- Wenn Sie nach einer Empfängereigenschaft wie An, Von, Cc oder Empfänger suchen, können Sie eine SMTP-Adresse, einen Alias oder einen Anzeigenamen verwenden, um einen Empfänger anzugeben. Sie können z. B. pilarp@contoso.com, pilarp oder "Pilar Pinilla" verwenden.
    
- Sie können nur die Platzhaltersuche Präfix verwenden. beispielsweise **Katze\* ** oder **festgelegt\***. Suffix Suchvorgänge ( ** \*Katze** ), infix-Suchvorgänge ( **c\*t** ), und Suchvorgänge Teilzeichenfolgen ( ** \*Katze\* ** ) werden nicht unterstützt. 
    
- Verwenden Sie bei der Suche einer Eigenschaft doppelte Anführungszeichen (""), wenn der gesuchte Wert aus mehreren Wörtern besteht. Beispielsweise `subject:budget Q1` gibt Nachrichten mit **Budget** in der in der Betreffzeile und, enthalten **Q1** an einer beliebigen Stelle in der Nachricht oder in einem der Nachrichteneigenschaften. Mit `subject:"budget Q1"` gibt alle Nachrichten, die **Q1 Budget** an einer beliebigen Stelle in der Betreffzeile enthalten. 
    
- Um bestimmte-Eigenschaft den Wert aus den Suchergebnissen markiert Inhalte auszuschließen, setzen Sie ein Minuszeichen (-) vor den Namen der Eigenschaft. Beispielsweise `-from:"Sara Davis"` schließt Sara Davis gesendeten Nachrichten.
- Sie können Elemente basierend auf den Elementtyp exportieren. Beispielsweise um Skype IM Nachrichten Recived von einem Benutzer zu exportieren, verwenden Sie die Syntax "Art: Sofortnachrichten" an. Diese Suche Abfragen Returen alle im-Nachricht. 
