---
title: Verwenden Sie Inhaltssuche, um Daten von Dritten zu suchen, die in Office 365 importiert wurde
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Verwenden Sie das Inhaltssuche eDiscovery-Tool nach Elementen gesucht, die auf Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Sie können eine Abfrage aus, um alle importierten Elemente suchen oder erstellen Sie eine Abfrage zum Suchen nach bestimmten von Drittanbieter-Datentypen erstellen. In diesem Artikel werden die Werte, die Sie in einer schlüsselwortabfrage verwenden können, um die Datentypen von Drittanbietern suchen, die auf Office 365 importiert werden kann.
ms.openlocfilehash: 6829e894ba687fb09184c32201f76394e37bbbf8
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037968"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a>Verwenden Sie Inhaltssuche, um Daten von Dritten zu suchen, die in Office 365 importiert wurde

Sie können das [Inhaltssuche eDiscovery-Tool](content-search.md) verwenden, in die Office 365-Sicherheit &amp; Compliance Center, um die Suche nach Elementen, die auf Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Sie können eine Abfrage aus, um alle importierten von Drittanbieter-Datenelementen gesucht werden soll erstellen, oder Sie können eine Abfrage an die Suche nur bestimmte Drittanbieter-Datenelemente erstellen. Darüber hinaus können Sie auch eine abfragebasierte Aufbewahrung Richtlinie erstellen oder einer eDiscovery-Abfrage-basierte halten Drittanbieter-Daten in Office 365 erhalten. 
  
Weitere Informationen zum Importieren von Drittanbieter-Daten und eine Liste der Drittanbieter-Datentypen, die in Office 365 importiert werden können, finden Sie unter [Archivierung Drittanbieter - Daten in Office 365](archiving-third-party-data.md). 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>Erstellen einer Abfrage zum Suchen von Daten für alle von Drittanbietern

Suche (oder direkt in der Warteschleife) jede Art von Drittanbieter-Daten, die Sie in Office 365 importiert haben, können Sie Sie können die `kind:externaldata` Meldung Eigenschaft-Wert-Paar in das Feld Stichwort für ein Inhaltssuche oder beim Erstellen einer abfragebasierte Aufbewahrung. Um die Suche nach Elementen, die aus einer beliebigen Drittanbieter-Datenquelle importiert wurden, und das Wort "Contoso" in die Subject-Eigenschaft des importierten Elements enthalten sein, verwenden Sie beispielsweise die folgende Abfrage: 
  
```
kind:externaldata AND subject:contoso
```

Im vorherigen Beispiel der Schlüsselwort-Abfrage enthält die Subject-Eigenschaft. Eine Liste mit anderen Eigenschaften für Drittanbieter-Datenelemente, die in einer schlüsselwortabfrage enthalten, finden Sie im Abschnitt "Weitere Informationen" in der [Drittanbieter - Archivierungsdaten in Office 365](archiving-third-party-data.md#more-information).
  
Beim Erstellen von Abfragen zum Durchsuchen und halten von Drittanbieter-Daten, können Sie auch Bedingungen verwenden, um die Suchergebnisse einzuschränken. Weitere Informationen zum Erstellen von Suchabfragen finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md).
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>Erstellen einer Abfrage, um bestimmte Arten von Drittanbieter-Daten zu suchen.

Nicht alle Arten von Drittanbieter-Daten durchsuchen, sondern können Sie Abfragen für ein Drittanbieter-Datentyp angeben, dass nur die Suche erstellen, mithilfe der folgenden Nachricht Eigenschaft-Wert-Paar in das Feld Stichwort für ein Inhaltssuche:
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

Um nur Facebook Daten zu suchen, die das Wort "Contoso" in die Subject-Eigenschaft enthält, würden Sie beispielsweise die folgende Abfrage verwenden:
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

Die folgende Tabelle enthält die Drittanbieter-Datentypen, die durchsucht werden, und der Wert für die `itemclass:` message-Eigenschaft, wie nach speziell für diese Art von Drittanbieter-Daten. Beachten Sie, dass die Abfragesyntax Groß-/Kleinschreibung nicht. 
  
|**Drittanbieter-Datentyp**|**Wert für `itemclass:` -Eigenschaft**|
|:-----|:-----|
|AIM  <br/> | `ipm.externaldata.AIM*` <br/> |
|American Idol  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|AOL mit Pivot-Client
  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|Apple Juice  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|Ares  <br/> | `ipm.externaldata.Ares*` <br/> |
|Axs Encrypted  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|Axs Exchange  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|Axs Local Archive  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|Platzhalter für AX  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Bazaarvoice  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|Bearshare  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|BitTorrent  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|BlackBerry  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|BlackBerry mithilfe von Anruflisten  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|BlackBerry Messenger  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|BlackBerry-PIN  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|BlackBerry SMS  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|Bloomberg Mail
  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|Bloomberg Messaging  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Box
  <br/> | `ipm.externaldata.Box*` <br/> |
|Cisco Sofortnachrichten &amp; Anwesenheitsserver  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|Cisco Jabber  <br/> | `ipm.externaldata.Jabber*` <br/> |
|CipherCloud for Salesforce Chatter  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|Direct Connect  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|Facebook  <br/> | `ipm.externaldata.Facebook*` <br/> |
|FastTrack  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|FXConnect  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|Flickr
  <br/> | `ipm.externaldata.Flickr*` <br/> |
|Gnutella  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|Google+
  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|Google Talk  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|GoToMyPC  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|HipChat  <br/> | `ipm.externaldata.HipChat*` <br/> |
|Hopster  <br/> | `ipm.externaldata.Hopster*` <br/> |
|HubConnex  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|IBM-Verbindungen  <br/> | `ipm.externaldata.Connections*` <br/> |
|IBM SameTime  <br/> | `ipm.externaldata.Sametime*` <br/> |
|ICE Chat  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|Indii Messenger
  <br/> | `ipm.externaldata.Indii*` <br/> |
|Instagram
  <br/> | `ipm.externaldata.Instagram*` <br/> |
|Instant Bloomberg
  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|InvestEdge  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|IRC  <br/> | `ipm.externaldata.IRC*` <br/> |
|Jive
  <br/> | `ipm.externaldata.Jive*` <br/> |
|JiveApiRetention  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|JXTA  <br/> | `ipm.externaldata.JXTA*` <br/> |
|LinkedIn  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|MFTP  <br/> | `ipm.externaldata.MFTP*` <br/> |
|Microsoft UC  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|Beachten Sie ausrichten  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|Mobile Guard  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|MSN  <br/> | `ipm.externaldata.MSN*` <br/> |
|MySpace  <br/> | `ipm.externaldata.MySpace*` <br/> |
|NEONetwork  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|OpenNap  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|Pinterest  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|Pivot  <br/> | `ipm.externaldata.Pivot*` <br/> |
|QQ  <br/> | `ipm.externaldata.QQ*` <br/> |
|Microsoft SharePoint  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|Salesforce Chatter  <br/> | `ipm.externaldata.Chatter*` <br/> |
|Skype for Business  <br/> | `ipm.externaldata.Skype*` <br/> |
|Slack Enterprise Grid  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|SoftEther  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|
Squawker
  <br/> | `ipm.externaldata.Squawker*` <br/> |
|Symphony
  <br/> | `ipm.externaldata.Symphony*` <br/> |
|Thomson Reuters  <br/> | `ipm.externaldata.Reuters*` <br/> |
| Thomson Reuters Eikon Messenger
  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|Tor  <br/> | `ipm.externaldata.Tor*` <br/> |
|TTT  <br/> | `ipm.externaldata.TTT*` <br/> |
|Twitter  <br/> | `ipm.externaldata.Twitter*` <br/> |
|UBS Chat
  <br/> | `ipm.externaldata.UBS*` <br/> |
|Vimeo  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|WinMX  <br/> | `ipm.externaldata.WinMX*` <br/> |
|Winny  <br/> | `ipm.externaldata.Winny*` <br/> |
|Yahoo!  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|Yammer  <br/> | `ipm.externaldata.Yammer*` <br/> |
|YellowJacket  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|YouTube (engl.)  <br/> | `ipm.externaldata.YouTube*` <br/> |
