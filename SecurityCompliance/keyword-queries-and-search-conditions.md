---
title: Stichwortabfragen und Suchbedingungen für die Inhaltssuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.SearchQueryLearnMore
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: c4639c2e-7223-4302-8e0d-b6e10f1c3be3
description: 'Erfahren Sie mehr über e-Mail-und Dateieigenschaften, die Sie in Exchange Online-Postfächern und in SharePoint oder OneDrive for Business-Websites mithilfe &amp; des Tools für die Inhaltssuche im Office 365 Security Compliance Center durchsuchen können.  '
ms.openlocfilehash: b3d0e7bb18513765c48bfc5ca324f13e5abc4c27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214075"
---
# <a name="keyword-queries-and-search-conditions-for-content-search"></a>Stichwortabfragen und Suchbedingungen für die Inhaltssuche

In diesem Thema werden die e-Mail-und Dokumenteigenschaften beschrieben, die Sie in e-Mail-Elementen in Exchange Online und in SharePoint-und OneDrive für Business-Websites gespeicherte Dokumente mithilfe der &amp; Inhaltssuche im Office 365 Security Compliance suchen können. Center. Sie können auch die ** \*-ComplianceSearch-** Cmdlets in Security &amp; Compliance Center PowerShell verwenden, um nach diesen Eigenschaften zu suchen. Das Thema beschreibt auch:   
  
- Verwenden von booleschen Suchoperatoren, Suchbedingungen und anderen Suchabfrage Techniken, um Ihre Suchergebnisse zu verfeinern.
    
- Suchen nach vertraulichen Datentypen und benutzerdefinierten vertraulichen Datentypen in SharePoint und OneDrive for Business.
    
- Suchen nach Websiteinhalten, die für Benutzer außerhalb Ihrer Organisation freigegeben sind
    
Eine schrittweise Anleitung zum Erstellen einer Inhaltssuche finden Sie unter [Inhaltssuche in Office 365](content-search.md).

  
> [!NOTE]
> Inhaltssuche im Security &amp; Compliance Center und den entsprechenden ** \*-ComplianceSearch-** Cmdlets in Security &amp; Compliance Center PowerShell verwenden Sie die Keyword Query Language (KQL). Ausführlichere Informationen finden Sie unter [Stichwort Query Language Syntax Reference](https://go.microsoft.com/fwlink/?LinkId=269603). 
  
## <a name="searchable-email-properties"></a>Durchsuchbare E-Mail-Eigenschaften

In der folgenden Tabelle sind die Eigenschaften von e-Mail-Nachrichten aufgeführt, die mithilfe der Inhalts &amp; Suche im Security Compliance Center oder mithilfe des Cmdlets **New-ComplianceSearch** oder **Set-ComplianceSearch** durchsucht werden können. Die Tabelle enthält ein Beispiel für die _Eigenschaft: Value-_ Syntax für jede Eigenschaft und eine Beschreibung der Suchergebnisse, die von den Beispielen zurückgegeben werden. Sie können diese `property:value` Paare in das Feld Schlüsselwörter für eine Inhaltssuche eingeben. 
  
|**Eigenschaft**|**Beschreibung der Eigenschaft**|**Beispiele**|**Von den Beispielen zurückgegebene Suchergebnisse**|
|:-----|:-----|:-----|:-----|
|AttachmentNames|Die Namen der an eine E-Mail angefügten Dateien.|`attachmentnames:annualreport.ppt`  <br/> `attachmentnames:annual*`|Nachrichten, die in der Anlage eine Datei mit dem Namen „Jahresbericht.ppt“ haben. Im zweiten Beispiel werden, wenn Sie das Platzhalterzeichen verwenden, Nachrichten mit dem Wort „Jahresbericht“ im Dateinamen einer Anlage zurückgegeben.|
|Bcc|Das Feld „BCC" einer E-Mail-Nachricht.<sup>1</sup>|`bcc:pilarp@contoso.com`  <br/> `bcc:pilarp`  <br/> `bcc:"Pilar Pinilla"`|In allen Beispielen werden Nachrichten mit dem Namen "Pilar Pinilla" im Bcc-Feld zurückgegeben.|
|Kategorie| Die Kategorien, die durchsucht werden sollen. Kategorien können von Benutzern mithilfe von Outlook oder Outlook im Web (früher als Outlook Web App bezeichnet) definiert werden. Folgende Werte sind möglich:  <br/><br/>  blau  <br/>  grün  <br/>  orange  <br/>  violett  <br/>  rot  <br/>  gelb|`category:"Red Category"`|Nachrichten, denen in den Quellpostfächern die rote Kategorie zugewiesen wurde.|
|Cc|Das Feld „CC" einer E-Mail-Nachricht.<sup>1</sup>|`cc:pilarp@contoso.com`  <br/> `cc:"Pilar Pinilla"`|In beiden Fällen Nachrichten mit dem Namen "Pilar Pinilla" im CC-Feld.|
|Folderid|Die Ordner-ID (GUID) eines bestimmten Postfachordners. Wenn Sie diese Eigenschaft verwenden, müssen Sie das Postfach durchsuchen, in dem sich der angegebene Ordner befindet. Beachten Sie, dass nur der angegebene Ordner durchsucht wird. Alle Unterordner im Ordner werden nicht durchsucht. Zum Durchsuchen von Unterordnern müssen Sie die Folder-Eigenschaft für den Unterordner verwenden, den Sie durchsuchen möchten.<br/> Weitere Informationen zum Suchen nach der Folder-Eigenschaft und zum Verwenden eines Skripts zum Abrufen der Ordner-IDs für ein bestimmtes Postfach finden Sie unter [use Content Search in Office 365 for Targeted Collections](use-content-search-for-targeted-collections.md).|`folderid:4D6DD7F943C29041A65787E30F02AD1F00000000013A0000`  <br/> `folderid:2370FB455F82FC44BE31397F47B632A70000000001160000 AND participants:garthf@contoso.com`|Im ersten Beispiel werden alle Elemente im angegebenen Postfachordner zurückgegeben. Im zweiten Beispiel werden alle Elemente im angegebenen Postfachordner zurückgegeben, die von garthf@contoso.com gesendet oder empfangen wurden.|
|Von|Der Absender einer E-Mail-Nachricht.<sup>1</sup>|`from:pilarp@contoso.com`  <br/> `from:contoso.com`|Nachrichten, die vom angegebenen Benutzer oder einer bestimmten Domäne gesendet wurden.|
|HasAttachment|Gibt an, ob eine Nachricht eine Anlage enthält. Verwenden Sie die Werte **true** oder **false**.|`from:pilar@contoso.com AND hasattachment:true`|Vom angegebenen Benutzer gesendete Nachrichten mit Anlagen.|
|Wichtigkeit|Die Wichtigkeit einer E-Mail-Nachricht, die ein Absender festlegen kann, wenn er eine Nachricht sendet. Standardmäßig werden Nachrichten mit normaler Wichtigkeit gesendet, außer wenn der Absender die Wichtigkeit auf **Hoch** oder **Niedrig** setzt.  |`importance:high`  <br/> `importance:medium`  <br/> `importance:low`|Nachrichten, deren Wichtigkeit auf "Hoch", "Mittel" bzw. "Niedrig" eingestellt ist.|
|IsRead|Gibt an, ob Nachrichten gelesen wurden. Verwenden Sie die Werte **true** oder **false**.|`isread:true`  <br/> `isread:false`|Im ersten Beispiel werden Nachrichten zurückgegeben, wobei die isRead-Eigenschaft auf **true**festgelegt ist. Im zweiten Beispiel werden Nachrichten zurückgegeben, wobei die isRead-Eigenschaft auf **false**festgelegt ist.|
|ItemClass|Verwenden Sie diese Eigenschaft, um bestimmte Drittanbieter-Datentypen zu durchsuchen, die Ihre Organisation in Office 365 importiert hat. Verwenden Sie für diese Eigenschaft die folgende Syntax:`itemclass:ipm.externaldata.<third-party data type>*`|`itemclass:ipm.externaldata.Facebook* AND subject:contoso`  <br/> `itemclass:ipm.externaldata.Twitter* AND from:"Ann Beebe" AND "Northwind Traders"`|Im ersten Beispiel werden Facebook-Elemente zurückgegeben, die das Wort "Contoso" in der Subject-Eigenschaft enthalten. Im zweiten Beispiel werden von Ann Beebe veröffentlichte Twitter-Elemente zurückgegeben, die die Schlüsselwortphrase "Northwind Traders" enthalten.<br/> Eine vollständige Liste der Werte für Drittanbieter-Datentypen für die ItemClass-Eigenschaft finden Sie unter [Verwenden der Inhaltssuche zum Durchsuchen von drittanbieterdaten, die in Office 365 importiert wurden](use-content-search-to-search-third-party-data-that-was-imported.md).|
|Art| Der Typ der zu suchenden e-Mail-Nachricht. Mögliche Werte:  <br/>  contacts  <br/>  docs  <br/>  email  <br/>  externaldata  <br/>  faxes  <br/>  im  <br/>  journals  <br/>  meetings  <br/>  verläuft (gibt Elemente aus Chats, Besprechungen und anrufen in Microsoft Teams zurück)  <br/>  notes  <br/>  posts  <br/>  rssfeeds  <br/>  tasks  <br/>  voicemail|`kind:email`  <br/> `kind:email OR kind:im OR kind:voicemail`  <br/> `kind:externaldata`|Im ersten Beispiel werden e-Mail-Nachrichten zurückgegeben, die den Suchkriterien entsprechen. Im zweiten Beispiel werden e-Mail-Nachrichten, Sofortnachrichtenunterhaltungen (einschließlich Skype for Business-Unterhaltungen und-Chats in Microsoft Teams) und Sprachnachrichten zurückgegeben, die den Suchkriterien entsprechen. Das dritte Beispiel gibt Elemente zurück, die in Postfächer in Office 365 aus Datenquellen von Drittanbietern wie Twitter, Facebook und Cisco Jabber importiert wurden, die die Suchkriterien erfüllen. Weitere Informationen finden Sie unter [archivIeren von drittanbieterdaten in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).|
|Teilnehmer|Alle Felder mit Personen in einer E-Mail-Nachricht. Diese Felder sind „Von", „An", „CC" und „BCC".<sup>1</sup>|`participants:garthf@contoso.com`  <br/> `participants:contoso.com`|Nachrichten, die von oder an garthf@contoso.com gesendet wurden. Im zweiten Beispiel werden alle Nachrichten zurückgegeben, die von oder an einen Benutzer in der Domäne contoso.com gesendet wurden.|
|Empfangen|Das Datum, an dem eine E-Mail-Nachricht von einem Empfänger empfangen wurde.|`received:04/15/2016`  <br/> `received>=01/01/2016 AND received<=03/31/2016`|Nachrichten, die am 15. April 2016 empfangen wurden. Im zweiten Beispiel werden alle Nachrichten zurückgegeben, die zwischen dem 1. Januar 2016 und dem 2016.|
|Empfänger|Alle Felder mit Empfängern in einer E-Mail-Nachricht. Diese Felder sind „An", „CC" und „BCC".<sup>1</sup>|`recipients:garthf@contoso.com`  <br/> `recipients:contoso.com`|Nachrichten, die an garthf@contoso.com gesendet wurden. Im zweiten Beispiel werden Nachrichten zurückgegeben, die an einen Empfänger in der Domäne contoso.com gesendet wurden.|
|Gesendet|Das Datum, an dem eine E-Mail vom Absender gesendet wurde.|`sent:07/01/2016`  <br/> `sent>=06/01/2016 AND sent<=07/01/2016`|Nachrichten, die am angegebenen Tag oder im angegebenen Datumsbereich gesendet wurden.|
|Größe|Die Größe eines Elements in Byte.|`size>26214400`  <br/> `size:1..1048567`|Nachrichten, die größer als 25 sind? MB. Im zweiten Beispiel werden Nachrichten von 1 bis 1.048.567 Byte (1 MB) in der Größe zurückgegeben.|
|Betreff|Der Text in der Betreffzeile einer E-Mail.  <br/> **Hinweis:** Wenn Sie die Subject-Eigenschaft in einer Abfrage verwenden, gibt die ???the-Suche alle Nachrichten zurück, in denen die Betreffzeile den gesuchten Text enthält. Anders ausgedrückt, gibt die Abfrage nur die Nachrichten zurück, die eine exakte Übereinstimmung aufweisen. Wenn Sie beispielsweise nach suchen `subject:"Quarterly Financials"`, enthalten Ihre Ergebnisse Nachrichten mit dem Betreff "quarterly Financials 2018".|`subject:"Quarterly Financials"`  <br/> `subject:northwind`|Nachrichten, die den Ausdruck "vierteljährliche Finanzdaten" im Text der Betreffzeile enthalten. Im zweiten Beispiel werden alle Nachrichten zurückgegeben, die das Wort Northwind in der Betreffzeile enthalten.|
|An|Das Feld „An" einer E-Mail-Nachricht.<sup>1</sup>|`to:annb@contoso.com`  <br/> `to:annb ` <br/> `to:"Ann Beebe"`|In allen Beispielen wegen Nachrichten zurückgegeben, in deren Zeile "An" der Name "Ann Beebe" angegeben ist.|
   
> [!NOTE]
> <sup>1</sup> für den Wert einer Empfänger Eigenschaft können Sie die e-Mail-Adresse (auch als *Benutzerprinzipalname* oder UPN bezeichnet), Anzeigenamen oder Alias verwenden, um einen Benutzer anzugeben. Sie können beispielsweise annb@contoso.com, annb oder "Ann Beebe" verwenden, um den Benutzer Ann Beebe anzugeben.<br/><br/>Beim Durchsuchen einer der Empfänger Eigenschaften (from, to, CC, BCC, participants, and recipients) versucht Office 365, die Identität der einzelnen Benutzer zu erweitern, indem Sie Sie in Azure Active Directory nachschlagen.  Wenn der Benutzer in Azure Active Directory gefunden wird, wird die Abfrage erweitert, um die e-Mail-Adresse des Benutzers (oder UPN), Alias, Anzeigename und LegacyExchangeDN einzuschließen.<br/><br/>Beispielsweise wird eine Abfrage wie `participants:ronnie@contoso.com` erweitert zu. `participants:ronnie@contoso.com OR participants:ronnie OR participants:"Ronald Nelson" OR participants:"<LegacyExchangeDN>"`

## <a name="searchable-site-properties"></a>Durchsuchbare Websiteeigenschaften

In der folgenden Tabelle sind einige der SharePoint-und OneDrive für Business-Eigenschaften aufgeführt, die mithilfe der Inhaltssuche im Security &amp; Compliance Center oder mithilfe der **New-ComplianceSearch** oder der ** Set-ComplianceSearch-** Cmdlet. Die Tabelle enthält ein Beispiel für die _Eigenschaft: Value-_ Syntax für jede Eigenschaft und eine Beschreibung der Suchergebnisse, die von den Beispielen zurückgegeben werden. 
  
Eine vollständige Liste der SharePoint-Eigenschaften, die durchsucht werden können, finden Sie unter [Übersicht über durchforstete und verwaltete Eigenschaften in SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Eigenschaften, die mit einem **Ja** in der Spalte **Queryable** markiert sind, können durchsucht werden. 
  
|**Eigenschaft**|**Beschreibung der Eigenschaft**|**Beispiel**|**Von den Beispielen zurückgegebene Suchergebnisse**|
|:-----|:-----|:-----|:-----|
|Autor|Das Author-Feld aus Office-Dokumenten, das beibehalten wird, wenn ein Dokument kopiert wird. Wenn ein Benutzer beispielsweise ein Dokument erstellt und es an eine andere Person sendet, die es dann in SharePoint hochlädt, behält das Dokument weiterhin den ursprünglichen Autor bei. Achten Sie darauf, den Anzeigenamen des Benutzers für diese Eigenschaft zu verwenden.|`author:"Garth Fort"`|Alle Dokumente, die von Garth Fort erstellt wurden.|
|ContentType|Der SharePoint-Inhaltstyp eines Elements wie Element, Dokument oder Video.|`contenttype:document`|Alle Dokumente würden zurückgegeben.|
|Created|Das Datum, an dem ein Element erstellt wird.|`created\>=06/01/2016`|Alle Elemente, die am oder nach dem 1. Juni 2016 erstellt wurden.|
|CreatedBy|Die Person, die ein Element erstellt oder hochgeladen hat. Achten Sie darauf, den Anzeigenamen des Benutzers für diese Eigenschaft zu verwenden.|`createdby:"Garth Fort"`|Alle Elemente, die von Garth Fort erstellt oder hochgeladen wurden.|
|DetectedLanguage|Die Sprache eines Elements.|`detectedlanguage:english`|Alle Elemente in Englisch.|
|File extension|Die Erweiterung einer Datei; beispielsweise docx, eine, PPTX oder xlsx.|`fileextension:xlsx`|Alle Excel-Dateien (Excel 2007 und höher)|
|FileName|Der Name einer Datei.|`filename:"marketing plan"`  <br/> `filename:estimate`|Im ersten Beispiel werden Dateien mit den exakten Ausdruck "Marketingplan" im Titel zurückgegeben. Das zweite Beispiel gibt Dateien mit dem Wort "schätzen" im Dateinamen zurück.|
|LastModifiedTime|Das Datum, an dem ein Element zuletzt geändert wurde.|`lastmodifiedtime>=05/01/2016`  <br/> `lastmodifiedtime>=05/10/2016 AND lastmodifiedtime<=06/1/2016`|Im ersten Beispiel werden Elemente zurückgegeben, die am oder nach dem 1. Mai 2016 geändert wurden. Im zweiten Beispiel werden Elemente zurückgegeben, die zwischen 1. Mai 2016 und dem 1. Juni 2016 geändert wurden.|
|ModifiedBy|Die Person, die ein Element zuletzt geändert hat. Achten Sie darauf, den Anzeigenamen des Benutzers für diese Eigenschaft zu verwenden.|`modifiedby:"Garth Fort"`|Alle Elemente, die zuletzt von Garth Fort geändert wurden.|
|Path|Der Pfad (URL) eines bestimmten Ordners auf einer SharePoint-oder OneDrive for Business-Website. Wenn Sie diese Eigenschaft verwenden, müssen Sie unbedingt die Website durchsuchen, in der sich der angegebene Ordner befindet.<br/> Wenn Sie Elemente zurückgeben möchten, die sich in Unterordnern im Ordner befinden, den Sie für die Path-Eigenschaft angeben\* , müssen Sie/der URL des angegebenen Ordners hinzufügen. Zum Beispiel`path: "https://contoso.sharepoint.com/Shared Documents/*"`  <br/> <br/> **Hinweis:** Wenn Sie `Path` die Eigenschaft zum Durchsuchen von OneDrive-Speicherorten verwenden, werden keine Mediendateien wie PNG-, TIFF-oder WAV-Dateien in den Suchergebnissen zurückgegeben. Verwenden Sie eine andere Site-Eigenschaft in Ihrer Suchabfrage, um in OneDrive-Ordnern nach Mediendateien zu suchen.<br/> <br/> Weitere Informationen zum Suchen nach der Path-Eigenschaft und zum Verwenden eines Skripts zum Abrufen der Pfad-URLs für Ordner auf einer bestimmten Website finden Sie unter [Verwenden der Inhaltssuche in Office 365 für zielgerichtete Auflistungen](use-content-search-for-targeted-collections.md).|`path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Private"`  <br/> `path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Shared with Everyone/*" AND filename:confidential`|Im ersten Beispiel werden alle Elemente im angegebenen OneDrive for Business-Ordner zurückgegeben. Im zweiten Beispiel werden Dokumente im angegebenen Websiteordner (und allen Unterordnern) zurückgegeben, die das Wort "vertraulich" im Dateinamen enthalten.|
|SharedWithUsersOWSUser|Dokumente, die für den angegebenen Benutzer freigegeben wurden und auf der Seite für **mich freigegeben** auf der OneDrive für Business-Website des Benutzers angezeigt werden. Hierbei handelt es sich um Dokumente, die von anderen Personen in Ihrer Organisation explizit für den angegebenen Benutzer freigegeben wurden. Beim Exportieren von Dokumenten, die einer Suchabfrage entsprechen, die die SharedWithUsersOWSUser-Eigenschaft verwendet, werden die Dokumente aus dem ursprünglichen Inhaltsspeicherort der Person exportiert, die das Dokument für den angegebenen Benutzer freigegeben hat. Weitere Informationen finden Sie unter [Suchen nach Websiteinhalten, die in Ihrer Organisation freigegeben](keyword-queries-and-search-conditions.md#internal)sind.|`sharedwithusersowsuser:garthf`  <br/> `sharedwithusersowsuser:"garthf@contoso.com"`|In beiden Beispielen werden alle internen Dokumente zurückgegeben, die ausdrücklich für Garth fort freigegeben wurden und auf der Seite "für **mich freigegeben** " des OneDrive for Business-Kontos von Garth fort angezeigt werden.|
|Website|Die URL einer Website oder einer Gruppe von Websites in Ihrer Organisation.|`site:"https://contoso-my.sharepoint.com"`  <br/> `site:"https://contoso.sharepoint.com/sites/teams"`|Im ersten Beispiel werden Elemente aus der OneDrive for Business-Websites für alle Benutzer in der Organisation zurückgegeben. Im zweiten Beispiel werden Elemente von allen Teamwebsites zurückgegeben.|
|Größe|Die Größe eines Elements in Byte.|`size>=1`  <br/> `size:1..10000`|Im ersten Beispiel werden Elemente zurückgegeben, die größer als 1 Byte sind. Im zweiten Beispiel werden Elemente mit einer Größe von 1 bis 10.000 Byte zurückgegeben.|
|Title|Der Titel des Dokuments. Die Title-Eigenschaft sind Metadaten, die in Microsoft Office-Dokumenten angegeben sind. Sie unterscheidet sich vom Dateinamen des Dokuments.|`title:"communication plan"`|Jedes Dokument, das den Ausdruck "Kommunikationsplan" in der Title-Metadateneigenschaft eines Office-Dokuments enthält.|
   
## <a name="searchable-contact-properties"></a>Durchsuchbare Kontakteigenschaften

In der folgenden Tabelle sind die Kontakteigenschaften aufgelistet, die indiziert werden und die Sie mithilfe der Inhaltssuche suchen können. Dies sind die Eigenschaften, die Benutzer für die Kontakte konfigurieren können (auch als persönliche Kontakte bezeichnet), die sich im persönlichen Adressbuch des Postfachs eines Benutzers befinden. Zum Suchen nach Kontakten können Sie die zu durchsuchenden Postfächer auswählen und dann eine oder mehrere Kontakteigenschaften in der Stichwortabfrage verwenden.
  
> [!TIP]
> Wenn Sie nach Werten suchen möchten, die Leerzeichen oder Sonderzeichen enthalten, verwenden Sie doppelte Anführungszeichen (""), um den Ausdruck zu enthalten. Beispiel: `businessaddress:"123 Main Street"`. 
  
|**Eigenschaft**|**Beschreibung der Eigenschaft**|
|:-----|:-----|
|BusinessAddress|Die Adresse in der **Geschäfts Adress** Eigenschaft. Die Eigenschaft wird auch als **Arbeits** Adresse auf der Seite mit den Kontakteigenschaften bezeichnet.|
|BusinessPhone|Die Telefonnummer in den Eigenschaften der **Geschäftstelefonnummer** .|
|CompanyName|Der Name in der **Company** -Eigenschaft.|
|Abteilung|Der Name in der **Department** -Eigenschaft.|
|DisplayName|Der Anzeigename des Kontakts. Dies ist der Name in der **vollständigen Name** -Eigenschaft des Kontakts.|
|EmailAddress|Die Adresse für eine beliebige e-Mail-Adress Eigenschaft für den Kontakt. Beachten Sie, dass Benutzer mehrere e-Mail-Adressen für einen Kontakt hinzufügen können. Bei Verwendung dieser Eigenschaft werden Kontakte zurückgegeben, die mit den e-Mail-Adressen des Kontakts übereinstimmen.|
|FileAs|Die **Datei als** -Eigenschaft. Diese Eigenschaft wird verwendet, um anzugeben, wie der Kontakt in der Kontaktliste des Benutzers aufgeführt wird. Beispielsweise kann ein Kontakt als *FirstName, LastName* oder *LastName, FirstName* aufgeführt werden.|
|GivenName|Der Name in der **First Name** -Eigenschaft.|
|HomeAddress|Die Adresse in den Eigenschaften der **Home** -Adresse.|
|HomePhone|Die Telefonnummer in den Eigenschaften der **privaten** Telefonnummern.|
|IMAddress|Die Eigenschaft der IM-Adresse, bei der es sich in der Regel um eine e-Mail-Adresse handelt.|
|MiddleName|Der Name in der Eigenschaft **mittlerer** Name.|
|Handy|Die Telefonnummer in der **Mobil** Telefonnummer.|
|Nickname|Der Name in der **Nickname** -Eigenschaft.|
|OfficeLocation|Der Wert in der **Office** -oder **Office-Standort** Eigenschaft.|
|OtherAddress|Der Wert für die **andere** Address-Eigenschaft.|
|Surname|Der Name in der Eigenschaft **Nachname** .|
|Title|Der Titel in der Eigenschaft " **Job Title** ".|
   

## <a name="searchable-sensitive-data-types"></a>Durchsuchbare vertrauliche Datentypen

Mithilfe der Inhaltssuche im Security &amp; Compliance Center können Sie nach vertraulichen Daten wie Kreditkartennummern oder Sozialversicherungsnummern suchen, die in Dokumenten auf SharePoint-und OneDrive für Business-Websites gespeichert sind. Hierzu können Sie die `SensitiveType` -Eigenschaft und den Namen eines vertraulichen Informationstyps in einer Stichwortabfrage verwenden. Die Abfrage `SensitiveType:"Credit Card Number"` gibt beispielsweise Dokumente zurück, die eine Kreditkartennummer enthalten. Die Abfrage `SensitiveType:"U.S. Social Security Number (SSN)"` gibt Dokumente zurück, die eine US-Sozialversicherungsnummer enthalten. Eine Liste der vertraulichen Datentypen, nach denen Sie suchen können, finden Sie unter **Klassifizierungen** \> **vertrauliche Informationstypen** im Security &amp; Compliance Center. Sie können auch das Cmdlet **Get-DlpSensitiveInformationType** im Security &amp; Compliance Center PowerShell verwenden, um eine Liste der Typen vertraulicher Informationen anzuzeigen. 
  
Sie können die `SensitiveType` -Eigenschaft auch verwenden, um nach dem Namen eines benutzerdefinierten Typs für vertrauliche Informationen zu suchen, den Sie (oder ein anderer Administrator) für Ihre Organisation erstellt haben. Beachten Sie, dass Sie die Spalte **Herausgeber** auf der Seite **vertrauliche Informationstypen** im &amp; Security Compliance Center (oder in der **Publisher** -Eigenschaft in PowerShell) verwenden können, um zwischen integrierten und benutzerdefinierten vertraulichen unterschieden Informationstypen. Weitere Informationen finden Sie unter [Erstellen eines benutzerdefinierten Typs für vertrauliche Informationen](create-a-custom-sensitive-information-type.md).
  
Weitere Informationen zum Erstellen von Abfragen mithilfe der `SensitiveType` -Eigenschaft finden Sie unter [Form a Query to Find sensitive data stored on Sites](form-a-query-to-find-sensitive-data-stored-on-sites.md).
  
## <a name="search-operators"></a>Suchoperatoren

Boolesche Suchoperatoren wie **and**, **or**und **Not**helfen Ihnen bei der Definition präziser suchen, indem Sie bestimmte Wörter in die Suchabfrage einschließen oder ausschließen. Weitere Techniken wie die Verwendung von eigenschaftsoperatoren (Beispiels \>Weise = oder..), Anführungszeichen, Klammern und Platzhalter können eine Suchabfrage verfeinern. In der folgenden Tabelle sind die Operatoren aufgeführt, die Sie verwenden können, um Suchergebnisse einzuschränken oder zu erweitern. 
  
|**Operator**|**Verwendung**|**Beschreibung**|
|:-----|:-----|:-----|
|AND|Wort1 AND Wort2|Gibt Elemente zurück, die alle angegebenen Schlüsselwörter oder `property:value` Ausdrücke enthalten. So werden `from:"Ann Beebe" AND subject:northwind` beispielsweise alle von Ann Beebe gesendeten Nachrichten zurückgegeben, die das Wort Northwind in der Betreffzeile enthalten. <sup>2</sup>|
|+|Wort1 + Wort2 + Wort3|Gibt die Elemente zurück, die  *entweder*  `keyword2` oder  `keyword3` *enthalten und*  , die ebenfalls  `keyword1` enthalten. Damit entspricht dieses Beispiel der Abfrage  `(keyword2 OR keyword3) AND keyword1`.  <br/> Beachten Sie, dass die Abfrage  `keyword1 + keyword2` (mit einem Leerzeichen nach dem **+** -Symbol) nicht der Verwendung des ** UND ** -Operators entspricht. Diese Abfrage wäre gleichbedeutend mit  `"keyword1 + keyword2"` und gibt Elemente mit dem exakten Ausdruck  `"keyword1 + keyword2"` zurück.  |
|ODER|Wort1 OR Wort2|Gibt Elemente zurück, die eines oder mehrere der angegebenen Schlüsselwörter `property:value` oder Ausdrücke enthalten. <sup>2</sup>|
|NOT|Wort1 NOT Wort2  <br/> NOT Von:"Ann Beebe"  <br/> NOT Kind: im|Schließt Elemente aus, die durch ein Schlüsselwort `property:value` oder einen Ausdruck angegeben werden. Im zweiten Beispiel werden von Ann Beebe gesendete Nachrichten ausgeschlossen. Im dritten Beispiel werden alle Sofortnachrichtenunterhaltungen, wie etwa Skype for Business-Unterhaltungen, die im Ordner "Conversation History Mailbox" gespeichert sind, ausgeschlossen. <sup>2</sup>|
|-|Wort1 - Wort2|Identisch mit dem Operator **Not** . Diese Abfrage gibt also Elemente zurück, `keyword1` die Elemente enthalten, die enthalten `keyword2`.|
|NEAR|Wort1 NEAR(n) Wort2|Gibt Elemente mit Wörtern zurück, die sich nahe beieinander befinden, wobei n gleich der Anzahl von Wörtern auseinander ist. Gibt beispielsweise `best NEAR(5) worst` alle Elemente zurück, bei denen das Wort "Worst" innerhalb von fünf Wörtern vom "besten" liegt. Wenn keine Zahl angegeben wird, beträgt der Standardabstand acht Wörter. <sup>2</sup>|
|ONEAR|Wort1 NEAR(n) Wort2|Ähnelt **near**, gibt jedoch Elemente mit Wörtern zurück, die sich in der angegebenen Reihenfolge nahe beieinander befinden. Gibt beispielsweise `best ONEAR(5) worst` alle Elemente zurück, bei denen das Wort "am besten" vor dem Wort "Worst" auftritt und die beiden Wörter innerhalb von fünf Wörtern voneinander sind. Wenn keine Zahl angegeben wird, beträgt der Standardabstand acht Wörter. <sup>2</sup> <br/> > [!NOTE]> der **ONEAR** -Operator wird beim Durchsuchen von Postfächern nicht unterstützt. Sie funktioniert nur beim Durchsuchen von SharePoint-und OneDrive for Business-Websites. Wenn Sie Postfächer und Websites in derselben Suche durchsuchen und die Abfrage den **ONEAR** -Operator enthält, gibt die Suche Postfachelemente zurück, als würden Sie den **near** -Operator verwenden. Mit anderen Worten gibt die Suche Elemente zurück, in denen sich die angegebenen Wörter befinden, unabhängig von der Reihenfolge, in der die Wörter auftreten.|
|:|Eigenschaftswert|Der Doppelpunkt (:) in der `property:value` Syntax gibt an, dass der Wert der Eigenschaft, nach der gesucht wird, den angegebenen Wert enthält. Gibt beispielsweise `recipients:garthf@contoso.com` jede Nachricht zurück, die an garthf@contoso.com gesendet wurde.|
|=|Eigenschaft=Wert|Identisch mit dem Operator **:** .|
|\<|Eigenschaft\<Wert|Zeigt an, dass die Eigenschaft, nach der gesucht wird, kleiner ist als der angegebene Wert.<sup>1</sup>|
|\>|Eigenschaft\>Wert|Zeigt an, dass die Eigenschaft, nach der gesucht wird, größer ist als der angegebene Wert.<sup>1</sup>|
|\<=|Eigenschaft\<=Wert|Zeigt an, dass die Eigenschaft, nach der gesucht wird, kleiner gleich dem angegebenen Wert ist.<sup>1</sup>|
|\>=|Eigenschaft\>=Wert|Zeigt an, dass die Eigenschaft, nach der gesucht wird, größer gleich dem angegebenen Wert ist.<sup>1</sup>|
|..|Eigenschaft: Wert1.. Wert2|Zeigt an, dass die Eigenschaft, nach der gesucht wird, größer gleich Wert1 und kleiner gleich Wert2 ist.<sup>1</sup>|
|"  "|"fair Value"  <br/> Betreff:"Vierteljährliche Finanzdaten"|Verwenden Sie doppelte Anführungszeichen (""), um in Stichwort-und `property:value` Suchabfragen nach einem exakten Ausdruck oder Ausdruck zu suchen.|
|\*|cat\*  <br/> Betreff:set\*|Präfix Platzhaltersuche (wobei das Sternchen am Ende eines Wortes gesetzt wird) entsprechen NULL oder mehr Zeichen in Schlüsselwörtern oder `property:value` Abfragen. `title:set*` Gibt beispielsweise Dokumente zurück, die den wortsatz, das Setup und die Einstellung (und andere Wörter, die mit "Set" beginnen) im Dokumenttitel enthalten.<br/><br/> **Hinweis:** Sie können nur Präfix-Platzhaltersuche verwenden. beispielsweise **Cat\* ** oder **Set\***. Suffix-suchen ( ** \*Cat** ), Infix-Suchvorgänge ( **\*c t** ) und Teilzeichenfolgen-suchen ( ** \*Cat\* ** ) werden nicht unterstützt.|
|(  )| (fair OR frei) AND (Von:contoso.com)  <br/> (IPO OR Initiale) AND (Aktien OR Anteile)  <br/> (Vierteljährliche Finanzdaten)|Mit Klammern werden Boolesche Ausdrücke,  `property:value`-Elemente und Schlüsselwörter gruppiert.  `(quarterly financials)` gibt z. B. Elemente zurück, die die Wörter "Vierteljährliche" und "Finanzdaten" enthalten.  |
   
> [!NOTE]
> <sup>1</sup> verwenden Sie diesen Operator für Eigenschaften, die Datums-oder numerische Werte aufweisen.<br/> <sup>2</sup> boolesche Suchoperatoren müssen groß-und klein geschrieben sein. Beispiel: **und**. Wenn Sie einen Kleinbuchstaben-Operator wie **und**verwenden, wird er in der Suchabfrage als Schlüsselwort behandelt. 
  
## <a name="search-conditions"></a>Suchbedingungen

Sie können einer Suchabfrage Bedingungen hinzufügen, um eine Suche einzuschränken und eine genauere Ergebnismenge zurückzugeben. Jede Bedingung fügt der KQL-Suchabfrage, die beim Starten der Suche erstellt und ausgeführt wird, eine Klausel hinzu.
  
[Bedingungen für allgemeine Eigenschaften ](#conditions-for-common-properties)

[Bedingungen für E-Mail-Eigenschaften](#conditions-for-mail-properties)

[Bedingungen für Dokumenteigenschaften ](#conditions-for-document-properties)

[Mit Bedingungen verwendete Operatoren](#operators-used-with-conditions)

[Richtlinien für die Verwendung von Bedingungen](#guidelines-for-using-conditions)

[Beispiele](#examples-of-using-conditions-in-search-queries)
  
### <a name="conditions-for-common-properties"></a>Bedingungen für allgemeine Eigenschaften 

Erstellen Sie eine Bedingung mithilfe allgemeiner Eigenschaften beim Durchsuchen von Postfächern und Websites in derselben Suche. In der folgenden Tabelle sind die verfügbaren Eigenschaften aufgeführt, die beim Hinzufügen einer Bedingung verwendet werden können.
  
|**Bedingung**|**Beschreibung**|
|:-----|:-----|
|Datum|Für e-Mails das Datum, an dem eine Nachricht von einem Empfänger empfangen oder vom Absender gesendet wurde. Für Dokumente das Datum, an dem ein Dokument zuletzt geändert wurde.|
|Absender/Autor|Für e-Mails die Person, die eine Nachricht gesendet hat. Für Dokumente, die Person, die im Feld "Autor" aus Office-Dokumenten zitiert wird. Sie können mehrere Namen eingeben, die durch Kommata getrennt sind. Zwei oder mehr Werte werden logisch vom **or** -Operator miteinander verbunden.|
|Größe (in Byte)|Sowohl bei E-Mails als auch bei Dokumenten die Größe des Elements (in Byte).|
|Betreff/Titel|Für e-Mails den Text in der Betreffzeile einer Nachricht. Für Dokumente den Titel des Dokuments. Wie bereits erläutert, handelt es sich bei der Title-Eigenschaft um Metadaten, die in Microsoft Office-Dokumenten angegeben sind. Sie können den Namen mehrerer Betreff/Titel durch Kommata getrennt eingeben. Zwei oder mehr Werte werden logisch vom **or** -Operator miteinander verbunden.|
|Compliancetag|Sowohl für e-Mails als auch für Dokumente werden Bezeichnungen, die Nachrichten und Dokumenten automatisch nach Bezeichnungsrichtlinien oder Bezeichnungen zugewiesen wurden, die manuell von Benutzern zugewiesen wurden. Bezeichnungen werden zum Klassifizieren von e-Mails und Dokumenten für die Datensteuerung und zum Erzwingen von Aufbewahrungsregeln basierend auf der Klassifizierung verwendet, die von der Bezeichnung definiert wird. Sie können einen Teil des Bezeichnungsnamens eingeben und einen Platzhalter verwenden oder den vollständigen Bezeichnungsnamen eingeben. Weitere Informationen finden Sie unter [Overview of Labels in Office 365](labels.md).|
  
### <a name="conditions-for-mail-properties"></a>Bedingungen für E-Mail-Eigenschaften

Erstellen Sie eine Bedingung unter Verwendung von E-Mail-Eigenschaften beim Durchsuchen von Postfächern oder öffentlichen Ordnern. Die folgende Tabelle enthält die E-Mail-Eigenschaften, die Sie für eine Bedingung verwenden können. Beachten Sie, dass diese Eigenschaften eine Teilmenge der bereits beschriebenen E-Mail-Eigenschaften darstellen. Diese Beschreibungen werden der Einfachheit halber wiederholt.
  
|**Bedingung**|**Beschreibung**|
|:-----|:-----|
|Nachrichtentyp| Der zu durchsuchende Nachrichtentyp. Dies ist dieselbe Eigenschaft wie die Art-e-Mail-Eigenschaft. Mögliche Werte:  <br/><br/>  contacts  <br/>  docs  <br/>  email  <br/>  externaldata  <br/>  faxes  <br/>  im  <br/>  journals  <br/>  meetings  <br/>  verläuft  <br/>  notes  <br/>  posts  <br/>  rssfeeds  <br/>  tasks  <br/>  voicemail|
|Teilnehmer|Alle Felder mit Personen in einer E-Mail-Nachricht. Diese Felder sind "Von", "An", "CC" und "BCC".|
|Typ|Die Eigenschaft der Nachrichtenklasse für ein e-Mail-Element. Dies ist dieselbe Eigenschaft wie die ItemClass-e-Mail-Eigenschaft. Es ist auch eine mehrwertige Bedingung. Um mehrere Nachrichtenklassen auszuwählen, halten Sie die **STRG** -Taste gedrückt, und klicken Sie dann in der Dropdownliste auf zwei oder mehr Nachrichtenklassen, die Sie der Bedingung hinzufügen möchten. Jede Nachrichtenklasse, die Sie in der Liste auswählen, wird logisch durch den **or** -Operator in der entsprechenden Suchabfrage verbunden.<br/> Eine Liste der Nachrichtenklassen (und der zugehörigen Nachrichtenklassen-ID), die von Exchange verwendet werden und die Sie in der Liste **Nachrichtenklasse** auswählen können, finden Sie unter [Item Types and Message](https://go.microsoft.com/fwlink/?linkid=848143)Classes.|
|Received|Das Datum, an dem eine E-Mail-Nachricht von einem Empfänger empfangen wurde. Dies ist die gleiche Eigenschaft wie die E-Mail-Eigenschaft „Empfangen“.|
|Empfänger|Die Person, an die eine e-Mail-Nachricht gesendet wurde. Dies ist dieselbe Eigenschaft wie die to-e-Mail-Eigenschaft.|
|Absender|Der Absender einer E-Mail-Nachricht.|
|Sent|Das Datum, an dem eine e-Mail-Nachricht vom Absender gesendet wurde. Dies ist dieselbe Eigenschaft wie die Eigenschaft "gesendete e-Mail".|
|Betreff|Der Text in der Betreffzeile einer E-Mail.|
|An|Der Empfänger einer e-Mail-Nachricht.|
  
### <a name="conditions-for-document-properties"></a>Bedingungen für Dokumenteigenschaften 

Erstellen Sie eine Bedingung mithilfe von Dokumenteigenschaften beim Suchen nach Dokumenten auf SharePoint-und OneDrive für Business-Websites. In der folgenden Tabelle werden die Dokumenteigenschaften aufgelistet, die Sie für eine Bedingung verwenden können. Beachten Sie, dass diese Eigenschaften eine Teilmenge der zuvor beschriebenen Websiteeigenschaften sind. Diese Beschreibungen werden zu Ihrer Bequemlichkeit wiederholt.
  
|**Bedingung**|**Beschreibung**|
|:-----|:-----|
|Autor|Das Author-Feld aus Office-Dokumenten, das beibehalten wird, wenn ein Dokument kopiert wird. Wenn ein Benutzer beispielsweise ein Dokument erstellt und es an eine andere Person sendet, die es dann in SharePoint hochlädt, behält das Dokument weiterhin den ursprünglichen Autor bei.|
|Title|Der Titel des Dokuments. Die Title-Eigenschaft sind Metadaten, die in Office-Dokumenten angegeben sind. Sie unterscheidet sich vom Dateinamen des Dokuments.|
|Erstellt|Das Datum, an dem ein Dokument erstellt wird.|
|Zuletzt geändert|Das Datum, an dem ein Dokument zuletzt geändert wurde.|
|Dateityp|Die Erweiterung einer Datei; beispielsweise docx, eine, PPTX oder xlsx. Dies ist die gleiche Eigenschaft wie die Site-Eigenschaft FileExtension.|
  
### <a name="operators-used-with-conditions"></a>Mit Bedingungen verwendete Operatoren

Beim Hinzufügen einer Bedingung können Sie einen Operator auswählen, der für den Typ der Eigenschaft für die Bedingung relevant ist. Die folgende Tabelle enthält die mit Bedingungen verwendeten Operatoren und die dazugehörigen Entsprechungen, die in der Suchabfrage verwendet werden.
  
|**Operator**|**Entsprechung in der Abfrage**|**Beschreibung**|
|:-----|:-----|:-----|
|After|`property>date`|Wird mit Datumsbedingungen verwendet. Gibt die Elemente zurück, die nach dem angegebenen Datum gesendet, empfangen oder geändert wurden. |
|Before|`property<date`|Wird mit Datumsbedingungen verwendet. Gibt die Elemente zurück, die vor dem angegebenen Datum gesendet, empfangen oder geändert wurden.|
|Between|`date..date`|Verwendung mit Datums-und Größen Bedingungen. Bei Verwendung mit einer Date-Bedingung werden Elemente zurückgegeben, die im angegebenen Datumsbereich gesendet, empfangen oder geändert wurden. Bei Verwendung mit einer Größen Bedingung gibt Elemente zurück, deren Größe innerhalb des angegebenen Bereich liegt.|
|Contains any of|`(property:value) OR (property:value)`|Wird mit Bedingungen für Eigenschaften verwendet, die einen Zeichenfolgenwert angeben. Gibt Elemente zurück, die einen Teil der angegebenen Zeichenfolgenwerte enthalten.|
|Doesn't contain any of|`-property:value`  <br/> `NOT property:value`|Wird mit Bedingungen für Eigenschaften verwendet, die einen Zeichenfolgenwert angeben. Gibt Elemente zurück, die keinen Teil des angegebenen Zeichenfolgenwerts enthalten.|
|Doesn't equal any of
|`-property=value`  <br/> `NOT property=value`|Wird mit Bedingungen für Eigenschaften verwendet, die einen Zeichenfolgenwert angeben. Gibt Elemente zurück, die die angegebene Zeichenfolge nicht enthalten.|
|Equals|`size=value`|Gibt Elemente zurück, die der angegebenen Größe entsprechen.<sup>1</sup>|
|Equals any of|`(property=value) OR (property=value)`|Wird mit Bedingungen für Eigenschaften verwendet, die einen Zeichenfolgenwert angeben. Gibt Elemente zurück, die genau den angegebenen Zeichenfolgenwerten entsprechen.|
|Greater|`size>value`|Gibt Elemente zurück, in denen die angegebene Eigenschaft größer als der angegebene Wert ist.<sup>1</sup>|
|Greater or equal|`size>=value`|Gibt Elemente zurück, in denen die angegebene Eigenschaft größer als oder gleich dem angegebenen Wert ist.<sup>1</sup>|
|Less|`size<value`|Gibt Elemente zurück, die größer als oder gleich dem angegebenen Wert sind.<sup>1</sup>|
|Less or equal|`size<=value`|Gibt Elemente zurück, die größer als oder gleich dem angegebenen Wert sind.<sup>1</sup>|
|Not equal|`size<>value`| Gibt Elemente zurück, die nicht der angegebenen Größe entsprechen.<sup>1</sup>|
   
> [!NOTE]
> <sup>1</sup> dieser Operator steht nur für Bedingungen zur Verfügung, die die Size-Eigenschaft verwenden. 
  
### <a name="guidelines-for-using-conditions"></a>Richtlinien für die Verwendung von Bedingungen

Beachten Sie Folgendes bei der Verwendung von Suchbedingungen:
  
- Eine Bedingung ist logisch mit der Schlüsselwortabfrage (angegeben im Stichwortfeld) durch den **and-** Operator verbunden. Dies führt dazu, dass Elemente sowohl die Stichwortabfrage als auch die Bedingung erfüllen müssen, die in die Ergebnisse eingeschlossen werden soll. Auf diese Weise können Sie Ihre Ergebnisse einschränken. 
    
- Wenn Sie zwei oder mehr eindeutige Bedingungen zu einer Suchabfrage hinzufügen (Bedingungen, die verschiedene Eigenschaften angeben), werden diese Bedingungen logisch mit dem **and-** Operator verbunden. Dies führt dazu, dass nur Elemente zurückgegeben werden, die alle Bedingungen erfüllen (zusätzlich zu einer Stichwortabfrage). 
    
- Wenn Sie mehr als eine Bedingung für dieselbe Eigenschaft hinzufügen, werden diese Bedingungen vom **or** -Operator logisch miteinander verbunden. Dies sind Elemente, die die Schlüsselwortabfrage erfüllen, und eine der Bedingungen werden zurückgegeben. Daher werden Gruppen derselben Bedingungen vom **or** -Operator miteinander verbunden, und dann werden Sätze mit eindeutigen Bedingungen durch den **and-** Operator verbunden. 
    
- Wenn Sie mehrere Werte (durch Kommas oder Semikolons getrennt) einer einzelnen Bedingung hinzufügen, werden diese Werte durch den **or** -Operator verbunden. Das Ergebnis ist, dass Elemente zurückgegeben werden, wenn Sie einen der angegebenen Werte für die Eigenschaft in der Bedingung enthalten. 
    
- Die Suchabfrage, die mithilfe des Felds Schlüsselwörter und Bedingungen erstellt wird, wird auf **** der Suchseite im Detailbereich für die ausgewählte Suche angezeigt. In einer Abfrage gibt alles rechts neben der Notation `(c:c)` Bedingungen an, die der Abfrage hinzugefügt werden. 
    
- Bedingungen fügen der Suchabfrage nur Eigenschaften hinzu; die keine Operatoren hinzufügen. Aus diesem Grund zeigt die Abfrage, die im Detailbereich angezeigt wird, keine Operatoren rechts neben `(c:c)` der Notation. KQL fügt die logischen Operatoren (gemäß den zuvor erläuterten Regeln) beim Ausführen der Abfrage hinzu. 
    
- Sie können das Drag & Drop-Steuerelement verwenden, um die Reihenfolge der Bedingungen neu zu ordnen. Klicken Sie einfach auf das Steuerelement für eine Bedingung, und verschieben Sie Sie nach oben oder unten.
    
- Wie bereits erläutert, können Sie mit einigen Bedingungseigenschaften mehrere Werte eingeben. Jeder Wert wird logisch vom **or** -Operator miteinander verbunden. Dies führt zu derselben Logik wie mehrere Instanzen derselben Bedingung mit einem einzelnen Wert. Die folgenden Abbildungen zeigen ein Beispiel für eine einzelne Bedingung mit mehreren Werten und ein Beispiel für mehrere Bedingungen (für die gleiche Eigenschaft) mit einem einzelnen Wert. Beide Beispiele resultieren in derselben Abfrage:`(filetype="docx") OR (filetype="pptx") OR (filetype="xlsx")`
    
    ![Eine Bedingung mit mehreren Werten](media/9880aa29-d117-4531-be20-6d53f1d21341.gif)
  
    ![Mehrere Suchkriterien für die gleiche Eigenschaft](media/1e63d37d-6d8d-4c9b-a509-a7e1c3a05193.gif)
  
> [!TIP]
> Wenn für eine Bedingung mehrere Werte zulässig sind, wird empfohlen, eine einzelne Bedingung mit mehreren Werten (durch Kommas oder Semikolons getrennt) zu verwenden. Auf diese Weise können Sie leichter sicherstellen, dass Sie die gewünschte Abfragelogik erhalten. 
  
### <a name="examples-of-using-conditions-in-search-queries"></a>Beispiele

Die folgenden Beispiele zeigen die GUI-basierte Version einer Suchabfrage mit Bedingungen, die Suchabfrage Syntax, die im Detailbereich der ausgewählten Suche angezeigt wird (die auch vom **Get-ComplianceSearch-** Cmdlet zurückgegeben wird), und die Logik der entsprechende KQL-Abfrage. 
  
#### <a name="example-1"></a>Beispiel 1

In diesem Beispiel werden Dokumente auf SharePoint-und OneDrive für Business-Websites zurückgegeben, die eine Kreditkartennummer enthalten und zuletzt vor dem 1. Januar geändert wurden 2016.
  
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

In diesem Beispiel werden e-Mail-Nachrichten oder Kalender Besprechungen zurückgegeben, die zwischen 12/1/2016 und 11/30/2016 gesendet wurden und Wörter enthalten, die mit "Phone" oder "Smartphone" beginnen.
  
 **GUI**
  
![Drittes Beispiel für Suchbedingungen](media/973d45fc-0923-43d6-9d0a-25e4a625f057.gif)
  
 **Suchabfragesyntax**
  
 `phone* OR smartphone*(c:c)(sent=2016-12-01..2016-11-30)(kind="email")(kind="meetings")`
  
 **Suchabfragelogik**
  
 `phone* OR smartphone* AND (sent=2016-12-01..2016-11-30) AND ((kind="email") OR (kind="meetings"))`
  
## <a name="searching-for-site-content-shared-with-external-users"></a>Suchen nach Websiteinhalten, die für externe Benutzer freigegeben sind

Sie können auch die Inhaltssuche im Security &amp; Compliance Center verwenden, um nach Dokumenten zu suchen, die auf SharePoint-und OneDrive für Business-Websites gespeichert sind, die für Personen außerhalb Ihrer Organisation freigegeben wurden. Dies kann Ihnen dabei helfen, vertrauliche oder proprietäre Informationen zu identifizieren, die außerhalb Ihrer Organisation freigegeben werden. Verwenden Sie dazu die `ViewableByExternalUsers` -Eigenschaft in einer Stichwortabfrage. Diese Eigenschaft gibt Dokumente oder Websites zurück, die für externe Benutzer freigegeben wurden, indem Sie eine der folgenden Freigabemethoden verwenden: 
  
- Eine Freigabeeinladung, bei der sich Benutzer als authentifizierter Benutzer bei Ihrer Organisation anmelden müssen.
    
- Ein anonymer gastlink, der jedem, der über diesen Link verfügt, Zugriff auf die Ressource ermöglicht, ohne authentifiziert werden zu müssen.
    
Hier sind einige Beispiele:
  
- Die Abfrage `ViewableByExternalUsers:true AND SensitiveType:"Credit Card Number"` gibt alle Elemente zurück, die für Personen außerhalb Ihrer Organisation freigegeben wurden und eine Kreditkartennummer enthalten. 
    
- Die Abfrage `ViewableByExternalUsers:true AND ContentType:document AND site:"https://contoso.sharepoint.com/Sites/Teams"` gibt eine Liste von Dokumenten auf allen Teamwebsites in der Organisation zurück, die für externe Benutzer freigegeben wurden. 
    
> [!TIP]
> Eine Suchabfrage wie z `ViewableByExternalUsers:true AND ContentType:document` . b. kann viele ASPX-Dateien in den Suchergebnissen zurückgeben. Um diese (oder andere Dateitypen) zu vermeiden, können Sie die `FileExtension` -Eigenschaft verwenden, um bestimmte Typen von Dateien auszuschließen. Beispiel `ViewableByExternalUsers:true AND ContentType:document NOT FileExtension:aspx`. 
  
Was gilt als Inhalte, die für Personen außerhalb Ihrer Organisation freigegeben werden? Dokumente in SharePoint-und OneDrive für Business-Websites Ihrer Organisation, die freigegeben werden, indem Sie eine Freigabeeinladung senden oder die an öffentlichen Standorten freigegeben werden. Die folgenden Benutzeraktivitäten führen beispielsweise zu Inhalten, die von externen Benutzern angezeigt werden können:
  
- Ein Benutzer gibt eine Datei oder einen Ordner für eine Person außerhalb Ihrer Organisation frei.

    
- Ein Benutzer erstellt und sendet einen Link zu einer freigegebenen Datei an eine Person außerhalb Ihrer Organisation. Dieser Link ermöglicht es dem externen Benutzer, die Datei anzuzeigen (oder zu bearbeiten).
    
- Ein Benutzer sendet eine Freigabeeinladung oder einen Gastlink an eine Person außerhalb Ihrer Organisation, um eine freigegebene Datei anzuzeigen (oder zu bearbeiten).
    
### <a name="issues-using-the-viewablebyexternalusers-property"></a>Probleme bei der Verwendung der ViewableByExternalUsers-Eigenschaft

Während die `ViewableByExternalUsers` Eigenschaft den Status der Freigabe eines Dokuments oder einer Website für externe Benutzer darstellt, gibt es einige Vorsichtsmaßnahmen, die diese Eigenschaft erfüllt und nicht widerspiegelt. In den folgenden Szenarien wird der Wert der `ViewableByExternalUsers` Eigenschaft nicht aktualisiert, und die Ergebnisse einer Inhalts Suchabfrage, die diese Eigenschaft verwendet, sind möglicherweise ungenau. 
  
- Änderungen an der Freigaberichtlinie, wie das Deaktivieren der externen Freigabe für eine Website oder für die Organisation. Die Eigenschaft zeigt weiterhin freigegebene Dokumente als extern zugänglich an, auch wenn der externe Zugriff möglicherweise widerrufen wurde.
    
- Änderungen an der Gruppenmitgliedschaft, beispielsweise hinzufügen oder Entfernen externer Benutzer zu Office 365-Gruppen oder Office 365-Sicherheitsgruppen. Die Eigenschaft wird nicht automatisch für Elemente aktualisiert, auf die die Gruppe Zugriff hat.
    
- Senden von Freigabeeinladungen an externe Benutzer, bei denen der Empfänger die Einladung nicht akzeptiert hat und daher noch keinen Zugriff auf den Inhalt hat.
    
In diesen Szenarien reflektiert die `ViewableByExternalUsers` Eigenschaft nicht den aktuellen Freigabestatus, bis die Website oder Dokumentbibliothek erneut durchforstet und erneut indiziert wird. 

## <a name="searching-for-site-content-shared-within-your-organization"></a>Suchen nach innerhalb Ihrer Organisation freigegebenen Websiteinhalten

Wie bereits erläutert, können Sie die `SharedWithUsersOWSUser` -Eigenschaft verwenden, um nach Dokumenten zu suchen, die von Personen in Ihrer Organisation freigegeben wurden. Wenn eine Person eine Datei (oder einen Ordner) für einen anderen Benutzer in Ihrer Organisation freigibt, wird ein Link zur freigegebenen Datei auf der Seite für **mich freigegeben** im OneDrive for Business-Konto der Person angezeigt, mit der die Datei freigegeben wurde. Um beispielsweise nach Dokumenten zu suchen, die mit Sara Davis freigegeben wurden, können Sie die Abfrage `SharedWithUsersOWSUser:"sarad@contoso.com"`verwenden. Wenn Sie die Ergebnisse dieser Suche exportieren, werden die ursprünglichen Dokumente (am Inhaltsspeicherort der Person, die die Dokumente mit Sara freigegeben hat) heruntergeladen.
  
Beachten Sie, dass Dokumente explizit für einen bestimmten Benutzer freigegeben werden müssen, damit Sie in den Such `SharedWithUsersOWSUser` Ergebnissen zurückgegeben werden, wenn Sie die-Eigenschaft verwenden. Wenn ein Benutzer beispielsweise ein Dokument in seinem OneDrive-Konto freigibt, haben Sie die Möglichkeit, es für jeden Benutzer (innerhalb oder außerhalb der Organisation) freizugeben, es nur für Personen innerhalb der Organisation freizugeben oder für eine bestimmte Person freizugeben. Hier ist ein Screenshot des **Freigabe** Fensters in OneDrive, in dem die drei Freigabeoptionen angezeigt werden. 
  
![Nur Dateien, die für bestimmte Personen freigegeben werden, werden von einer Suchabfrage zurückgegeben, die die SharedWithUsersOWSUser-Eigenschaft verwendet.](media/469a4b61-68bd-4ab0-b612-ab6302973886.png)
  
Nur Dokumente, die mit der dritten Option (für **bestimmte Personen**freigegeben) freigegeben werden, werden von einer Suchabfrage zurückgegeben `SharedWithUsersOWSUser` , die die Eigenschaft verwendet. 

## <a name="searching-for-skype-for-business-conversations"></a>Suchen nach Skype for Business-Unterhaltungen

Mithilfe der folgenden Stichwortabfrage können Sie gezielt nach Inhalten in Skype for Business-Unterhaltungen suchen:

```
kind:im
```

Hinweis die vorherige Suchabfrage gibt auch Chats von Microsoft Teams zurück. Um dies zu verhindern, können Sie die Suchergebnisse so einschränken, dass nur Skype for Business-Unterhaltungen mit der folgenden Stichwortabfrage eingeschlossen werden:

```
kind:im AND subject:conversation
```

Die vorherige Keyword-Abfrage schließt Chats in Microsoft Teams aus, da Skype for Business-Unterhaltungen als e-Mail-Nachrichten mit einer Betreffzeile gespeichert werden, die mit dem Wort "Conversation" beginnt.

Verwenden Sie die folgende Stichwortabfrage, um in einem bestimmten Datumsbereich nach Skype für Business-Unterhaltungen zu suchen:

```
kind:im AND subject:conversation AND (received=startdate..enddate)
```

## <a name="search-tips-and-tricks"></a>Tipps und Tricks für die Suche

- Schlüsselwortsuchen unterscheiden nicht zwischen Groß- und Kleinschreibung. Beispielsweise geben **katze** und **KATZE** dieselben Ergebnisse zurück. 
    
- Die booleschen Operatoren **and**, **or**, **Not**, **near**und **ONEAR** müssen groß geschrieben sein. 
    
- Ein Leerzeichen zwischen zwei Schlüsselwörtern `property:value` oder zwei Ausdrücken ist identisch mit der Verwendung von **und**. `from:"Sara Davis" subject:reorganization` Gibt beispielsweise alle von Sara Davis gesendeten Nachrichten zurück, die das Wort Reorganisation in der Betreffzeile enthalten. 
    
- Verwenden Sie eine Syntax, `property:value` die mit dem Format übereinstimmt. Bei Werten wird die Groß-/Kleinschreibung nicht beachtet, und Sie können kein Leerzeichen nach dem Operator aufweisen. Wenn es ein Leerzeichen gibt, ist der vorgesehene Wert nur eine Volltextsuche. Sucht Beispiels `to: pilarp` Weise nach "pilarp" als Schlüsselwort, statt für Nachrichten, die an pilarp gesendet wurden. 
    
- Wenn Sie nach einer Empfängereigenschaft wie An, Von, Cc oder Empfänger suchen, können Sie eine SMTP-Adresse, einen Alias oder einen Anzeigenamen verwenden, um einen Empfänger anzugeben. Sie können z. B. pilarp@contoso.com, pilarp oder "Pilar Pinilla" verwenden.
    
- Sie können nur Präfix-Platzhaltersuche verwenden. beispielsweise **Cat\* ** oder **Set\***. Suffix-suchen ( ** \*Cat** ), Infix-Suchvorgänge ( **\*c t** ) und Teilzeichenfolgen-suchen ( ** \*Cat\* ** ) werden nicht unterstützt. 
    
- Verwenden Sie beim Durchsuchen einer Eigenschaft doppelte Anführungszeichen (""), wenn der Suchwert aus mehreren Wörtern besteht. Gibt Beispiels `subject:budget Q1` Weise Nachrichten zurück, die das **Budget** in der Betreffzeile enthalten und **Q1** an beliebiger Stelle in der Nachricht oder in einer der Nachrichteneigenschaften enthalten. Using `subject:"budget Q1"` gibt alle Nachrichten zurück, die das **Budget Q1** in der Betreffzeile enthalten. 
    
- Wenn Sie mit einem bestimmten Eigenschaftswert markierte Inhalte aus den Suchergebnissen ausschließen möchten, platzieren Sie ein Minuszeichen (-) vor dem Namen der Eigenschaft. Beispielsweise `-from:"Sara Davis"` werden alle von Sara Davis gesendeten Nachrichten ausgeschlossen.

- Sie können Elemente basierend auf dem Nachrichtentyp exportieren. Wenn Sie beispielsweise Skype-Unterhaltungen und-Chats in Microsoft Teams exportieren `kind:im`möchten, verwenden Sie die Syntax. Wenn Sie nur e-Mail-Nachrichten `kind:email`zurückgeben möchten, verwenden Sie. Wenn Sie Chats, Besprechungen und Anrufe in Microsoft Teams zurückgeben `kind:microsoftteams`möchten, verwenden Sie.
