---
title: Verwenden der Inhaltssuche zum Durchsuchen von drittanbieterdaten, die in Office 365 importiert wurden
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Verwenden Sie das eDiscovery-Tool für die Inhaltssuche, um nach Elementen zu suchen, die in Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Sie können eine Abfrage erstellen, um nach allen importierten Elementen zu suchen, oder eine Abfrage erstellen, um nach bestimmten Drittanbieter Datentypen zu suchen. In diesem Artikel werden die Werte aufgelistet, die Sie in einer Stichwortabfrage verwenden können, um die Drittanbieter-Datentypen zu durchsuchen, die in Office 365 importiert werden können.
ms.openlocfilehash: f1ab3cfc8dd866aa0d70014b22a301de2a65f3c5
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296038"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a>Verwenden der Inhaltssuche zum Durchsuchen von drittanbieterdaten, die in Office 365 importiert wurden

Sie können das eDiscovery-Tool für die [Inhaltssuche](content-search.md) im Office 365 &amp; Security Compliance Center verwenden, um nach Elementen zu suchen, die in Postfächern in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Sie können eine Abfrage zum Durchsuchen aller importierten drittanbieterdaten Elemente erstellen, oder Sie können eine Abfrage erstellen, um nur bestimmte Drittanbieter-Datenelemente zu durchsuchen. Darüber hinaus können Sie auch eine abfragebasierte AufbewahrungsRichtlinie oder einen abfragebasierten eDiscovery-Speicher erstellen, um drittanbieterdaten in Office 365 zu erhalten. 
  
Weitere Informationen zum Importieren von drittanbieterdaten und eine Liste der Drittanbieter Datentypen, die in Office 365 importiert werden können, finden Sie unter [Archivierung von drittanbieterdaten in office 365](archiving-third-party-data.md). 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>Erstellen einer Abfrage zum Durchsuchen aller drittanbieterdaten

Wenn Sie alle Typen von drittanbieterdaten, die Sie in Office 365 importiert haben, Durchsuchen (oder im Wartebereich platzieren) möchten, können `kind:externaldata` Sie das Nachrichteneigenschaft-Wert-Paar im Stichwortfeld für eine Inhaltssuche oder beim Erstellen eines abfragebasierten haltebereichs verwenden. Wenn Sie beispielsweise nach Elementen suchen möchten, die aus einer Drittanbieter-Datenquelle importiert wurden und das Wort "Contoso" in der Subject-Eigenschaft des importierten Elements enthalten, würden Sie die folgende Abfrage verwenden: 
  
```
kind:externaldata AND subject:contoso
```

Das vorherige Keyword Query-Beispiel enthält die Subject-Eigenschaft. Eine Liste anderer Eigenschaften von drittanbieterdaten Elementen, die in eine Stichwortabfrage aufgenommen werden können, finden Sie im Abschnitt "Weitere Informationen" unter [Archivieren von drittanbieterdaten in Office 365](archiving-third-party-data.md#more-information).
  
Beim Erstellen von Abfragen zum Durchsuchen und Speichern von drittanbieterdaten können Sie auch Bedingungen verwenden, um die Suchergebnisse einzuschränken. Weitere Informationen zum Erstellen von Inhalts Suchabfragen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>Erstellen einer Abfrage zum Durchsuchen bestimmter Typen von drittanbieterdaten

Anstatt alle Typen von drittanbieterdaten zu durchsuchen, können Sie Abfragen erstellen, die nur nach einem angegebenen Typ von drittanbieterdaten suchen, indem Sie im Stichwortfeld für eine Inhaltssuche das folgende Nachrichten Eigenschaftswert-paar verwenden:
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

Wenn Sie beispielsweise nur Facebook-Daten durchsuchen möchten, die das Wort "Contoso" in der Subject-Eigenschaft enthalten, würden Sie die folgende Abfrage verwenden:
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

In der folgenden Tabelle sind die Drittanbieter-Datentypen aufgeführt, die Sie durchsuchen können, und der Wert `itemclass:` , der für die Message-Eigenschaft verwendet werden soll, um gezielt nach diesem Typ von drittanbieterdaten zu suchen. Beachten Sie, dass bei der Abfragesyntax die Groß-/Kleinschreibung nicht beachtet wird. 
  
|**Drittanbieter-Datentyp**|**Wert für `itemclass:` Eigenschaft**|
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
|AXS-Platzhalter  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Bazaarvoice  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|BearShare  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|BitTorrent  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|BlackBerry  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|BlackBerry-Anrufprotokolle  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|BlackBerry-Messenger  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|BlackBerry-PIN  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|BlackBerry-SMS  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|Bloomberg Mail
  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|Bloomberg-Messaging  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Box  <br/> | `ipm.externaldata.Box*` <br/> |
|Cisco- &amp; Sofortnachrichten-Anwesenheits Server  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
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
|ICE-Chat  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
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
|Ausrichtung  <br/> | `ipm.externaldata.MindAlign*` <br/> |
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
|YouTube  <br/> | `ipm.externaldata.YouTube*` <br/> |
