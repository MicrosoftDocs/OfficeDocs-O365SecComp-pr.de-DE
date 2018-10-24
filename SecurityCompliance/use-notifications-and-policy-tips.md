---
title: Senden von e-Mail-Benachrichtigungen und Anzeigen von Tipps zu Richtlinien für DLP-Richtlinien
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleNotifyUser
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 87496bc5-9601-4473-8021-cb05c71369c1
description: 'Ein richtlinientipp ist eine Benachrichtigung oder Warnung, die angezeigt wird, wenn eine Person mit Inhalt, steht in Konflikt mit einer DLP-Richtlinie funktionsfähig ist. Sie können e-Mail-Benachrichtigungen und Tipps zu Richtlinien zu informieren und Hilfe Personen zu Ihrer Organisation Richtlinien zu informieren. Sie können auch vorführen benötigten Personen die Option aus, um die Richtlinie außer Kraft setzen, damit sie nicht blockiert sind, wenn sie einen gültigen Business verfügen oder wenn die Richtlinie falsch positives Ergebnis erkennt. '
ms.openlocfilehash: f95e392cc6cced6da29d34abfcab0fa0c3add069
ms.sourcegitcommit: 3ac6452ab77a761d06122c35c5f4a76da4472990
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2018
ms.locfileid: "25769914"
---
# <a name="send-email-notifications-and-show-policy-tips-for-dlp-policies"></a>Senden von e-Mail-Benachrichtigungen und Anzeigen von Tipps zu Richtlinien für DLP-Richtlinien

Sie können eine Data Loss Prevention (DLP) Richtlinie zu identifizieren, überwachen und schützen Sie sensible Informationen über Office 365 verwenden. Personen in Ihrer Organisation, die mit Ihrer DLP-Richtlinien kompatibel bleiben diese vertraulichen Informationen entwickelt werden soll, jedoch nicht diese unnötig erste Erledigung ihrer Arbeit verhindern möchten. Dies ist, auf dem e-Mail-Benachrichtigungen und richtlinientipps helfen kann.
  
![Statusleiste zeigt Richtlinientipp in Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Ein richtlinientipp wird eine Benachrichtigung oder Warnung, die angezeigt wird, wenn eine Person mit Inhalten funktionsfähig ist, der mit einer DLP-Richtlinie verstößt – beispielsweise wie eine Excel-Arbeitsmappe auf einer OneDrive for Business-Website, die personenbezogene Informationen (PII) enthält und Inhalte ein externer Benutzer freigegeben.
  
Sie können e-Mail-Benachrichtigungen und Tipps zu Richtlinien zu informieren und Hilfe Personen zu Ihrer Organisation Richtlinien zu informieren. Sie können auch vorführen benötigten Personen die Option aus, um die Richtlinie außer Kraft setzen, damit sie nicht blockiert sind, wenn sie einen gültigen Business verfügen oder wenn die Richtlinie falsch positives Ergebnis erkennt.
  
In der Office 365-Sicherheit &amp; Compliance Center, bei der Erstellung einer DLP-Richtlinie, Sie können die Benutzer Benachrichtigungen zu konfigurieren:
  
- Senden eine e-Mail-Benachrichtigung an die Personen Sie auswählen, der das Problem beschreibt.
    
- Zeigen Sie einen richtlinientipp für Inhalte, die mit der DLP-Richtlinie in Konflikt steht:
    
  - Für e-Mail in Outlook im Web und Outlook 2013 und höher wird der richtlinientipp im oberen Bereich des über die Empfänger einer Nachricht angezeigt, während die Nachricht erstellt wurde.
    
  - Für Dokumente in einer OneDrive for Business-Konto oder SharePoint Online-Website wird die richtlinientipp durch das Warnungssymbol angezeigt, die für das Element angezeigt wird. Um weitere Informationen anzuzeigen, können Sie wählen ein Element aus, und wählen Sie dann **Informationen**![Bereich Informationssymbol](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) in der oberen rechten Ecke der Seite, öffnen Sie im Detailbereich. 
    
  - Für Excel 2016, 2016 PowerPoint und Word 2016 Dokumente, die auf einer OneDrive for Business-Website oder in die DLP-Richtlinie enthalten ist SharePoint Online-Website gespeichert sind, die Richtlinie-Info wird angezeigt, auf der Meldungsleiste und der Backstage-Ansicht (Menü " **Datei** " \> ** Info**).
    
## <a name="add-user-notifications-to-a-dlp-policy"></a>Hinzufügen von Benachrichtigungen für Benutzer zu einer DLP-Richtlinie

Bei der Erstellung einer DLP-Richtlinie gehören e-Mail-Benachrichtigungen sowie Tipps zu Richtlinien im Abschnitt **Benutzer Benachrichtigungen** . 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365. Sie sind jetzt in die Office 365-Sicherheit &amp; Compliance Center.
    
3. In das Wertpapier &amp; Compliance Center \> linke Navigationsleiste \> **Verhinderung von Datenverlust** \> **Richtlinie** \> **+ Richtlinie erstellen**.
    
    ![Erstellen einer Richtlinie-Schaltfläche](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Wählen Sie die DLP-Richtlinienvorlage, die die Arten von vertraulichen Informationen, die Sie benötigen, schützt \> **Weiter**.
    
    Um eine leere Vorlage zu starten, wählen Sie **Benutzerdefiniert** \> **benutzerdefinierte Richtlinie** \> **Weiter**.
    
5. Benennen Sie die Richtlinie \> **Weiter**.
    
6. Die Speicherorte auswählen die gewünschte die DLP-Richtlinie zu schützen, eine der folgenden Aktionen aus:
    
  - Wählen Sie **Alle Speicherorte in Office 365** \> **Weiter**.
    
  - Wählen Sie **selbst bestimmte Orte auswählen** \> **Weiter**.
    
    Wechseln Sie zum einbeziehen oder ausschließen einen gesamten Standort wie alle Exchange-e-Mail oder alle OneDrive-Konten, den **Status** von diesem Speicherort aktiviert oder deaktiviert. 
    
    Nur bestimmte SharePoint-Websites oder OneDrive Konten aufnehmen möchten, wechseln Sie auf den **Status** auf, und klicken Sie dann auf die Links unter **einschließen** , um bestimmte Standorte oder Konten auszuwählen. 
    
7. **Verwenden Sie den erweiterten Einstellungen** auswählen \> **Weiter**.
    
8. Wählen Sie **+ neue Regel**.
    
9. Wechseln Sie in der Regeleditor unter **Benutzer Benachrichtigungen**den Status auf.
    
    ![Regel-Editor im Abschnitt Benutzer Benachrichtigungen](media/47705927-c60b-4054-a072-ab914f33d15d.png)
  
## <a name="options-for-configuring-email-notifications"></a>Optionen zum Konfigurieren von E-Mail-Benachrichtigungen

Bei jeder Regel in einer DLP-Richtlinie haben Sie folgende Möglichkeiten:
  
- Senden der Benachrichtigung an die gewählten Personen. Diese Personen können den Besitzer des Inhalts, die Person, die den Inhalt zuletzt geändert hat, den Besitzer der Website, in welcher der Inhalt gespeichert ist, oder einen bestimmten Benutzer umfassen.
    
- Passen Sie den Text, der in der Benachrichtigung mithilfe von HTML oder Token enthalten ist. Finden Sie weitere Informationen im Abschnitt unten.
    
> [!NOTE]
>  E-Mail-Benachrichtigungen können nur für einzelne Empfänger gesendet werden – nicht Gruppen oder Verteilerlisten. > Nur neuer Inhalt wird eine e-Mail-Benachrichtigung ausgelöst. Bearbeiten von vorhandenen Inhalt wird richtlinientipps, aber nicht in einer e-Mail-Benachrichtigung ausgelöst. 
  
![E-Mail-Benachrichtigung-Optionen](media/4e7b9500-2a78-44e6-9067-09f4bfd50301.png)
  
### <a name="default-email-notification"></a>Standardmäßige E-Mail-Benachrichtigung

Benachrichtigungen haben eine Betreffzeile, die mit der Aktion, wie z. B. "Benachrichtigung", "Nachricht blockiert" beginnt für e-Mail- oder "Zugriff blockiert" für Dokumente. Wenn die Benachrichtigung über ein Dokument ist, enthält der Nachrichtentext für die Benachrichtigung eine Verknüpfung, die Sie zur Website, in dem das Dokument des gespeichert und öffnet die richtlinientipp für das Dokument, akzeptiert, in denen Sie Probleme beheben können (siehe unten im Abschnitt zu richtlinientipps). Wenn die Benachrichtigung über eine Nachricht ist, enthält die Benachrichtigung als Anlage die Nachricht, die mit eine DLP-Richtlinie übereinstimmt.
  
![Benachrichtigung](media/35813d40-5fd8-425f-9624-55655e74fa6b.png)
  
In der Standardeinstellung zeigen Benachrichtigungen für ein Element in einer Website Text wie den folgenden an. Der Benachrichtigungstext wird für jede Regel separat konfiguriert, damit sich der angezeigte Text abhängig von der angewendeten Regel unterscheidet.
  
| |
|**Wenn die DLP-Richtlinienregel dies tut...**|**Klicken Sie dann heißt die Standard-Benachrichtigung für SharePoint oder OneDrive für Geschäftsdokumente das...**|**Klicken Sie dann heißt die Standard-Benachrichtigung für Outlook-Nachrichten das...**|
|:-----|:-----|:-----|
|Sendet eine Benachrichtigung, ermöglicht aber kein außer Kraft setzen  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |Ihre e-Mail-Nachricht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |
|Sperrt Zugriff, sendet eine Benachrichtigung und erlaubt eine Außerkraftsetzung  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wenn Sie dieses Problem nicht lösen können, kann Zugriff auf diese Datei blockiert wird.  <br/> |Ihre e-Mail-Nachricht in Konflikt mit einer Richtlinie in Ihrer Organisation. Die Nachricht wurde nicht an alle Empfänger übermittelt.  <br/> |
|Sperrt Zugriff und sendet eine Benachrichtigung  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Der Zugriff auf dieses Element wird für alle Benutzer mit Ausnahme des Besitzers, des Benutzers, der es zuletzt geändert hat und des primären Websitesammlungsadministrators gesperrt.  <br/> |Ihre e-Mail-Nachricht in Konflikt mit einer Richtlinie in Ihrer Organisation. Die Nachricht wurde nicht an alle Empfänger übermittelt.  <br/> |
   
### <a name="custom-email-notification"></a>Benutzerdefinierte e-Mail-Benachrichtigung

Sie können eine benutzerdefinierte e-Mail-Benachrichtigung anstelle die standardmäßige e-Mail-Benachrichtigung an den Endbenutzer oder Administratoren senden erstellen. Die benutzerdefinierte e-Mail-Benachrichtigung HTML unterstützt und hat maximal 5.000 Zeichen. Sie können HTML verwenden, um Bilder, Formatierung und anderen branding in der Benachrichtigung einzubeziehen.
  
Sie können die folgenden Token auch verwenden, helfen, die e-Mail-Benachrichtigung anzupassen. Diese Token sind Variablen, die nach bestimmten Informationen in der Benachrichtigung ersetzt werden, die gesendet wird.
  
| |
|**Token**|**Beschreibung**|
|:-----|:-----|
|% AppliedActions %  <br/> |Die Aktionen, die auf den Inhalt angewendet.  <br/> |
|% ContentURL %  <br/> |Die URL des Dokuments auf dem SharePoint Online-Website oder OneDrive for Business-Site.  <br/> |
|% MatchedConditions %  <br/> |Die Bedingungen, die durch den Inhalt gefunden wurden. Verwenden Sie dieses Token, um Personen von möglichen Problemen mit dem Inhalt zu informieren.  <br/> |
   
![Benachrichtigung angezeigt, in dem Token angezeigt werden](media/cd3f36b3-40db-4f30-99e4-190750bd1955.png)
  
## <a name="options-for-configuring-policy-tips"></a>Optionen zum Konfigurieren von Richtlinientipps

Für jede Regel in einer DLP-Richtlinie können Sie zu folgenden Zwecken Richtlinientipps konfigurieren:
  
- Einfach benachrichtigen Sie, dass der Inhalt mit einer DLP-Richtlinie in Konflikt steht, damit sie die Aktion, die den Konflikt zu lösen nutzen können. Sie können den Standardtext verwenden (siehe die folgenden Tabellen) oder geben Sie einen benutzerdefinierten Text Ihrer Organisation spezielle Richtlinien.
    
- Der Person erlauben, die DLP-Richtlinie außer Kraft zu setzen. Optional können Sie Folgendes tun:
    
  - Erfordern Sie die Person, die als Rechtfertigung für das Außerkraftsetzen der Richtlinie. Diese Informationen protokolliert, und Sie können in die DLP-Berichten über die Sicherheit im Abschnitt **Berichte** anzeigen &amp; Compliance Center. 
    
  - Der Person erlauben, ein falsch positives Ergebnis zu melden und die DLP-Richtlinie außer Kraft zu setzen. Diese Informationen werden auch für Berichte erfasst, sodass Sie Ihre Regeln mithilfe von falsch positiven Ergebnissen optimieren können.
    
![Optionen für Richtlinie](media/0d2f2c68-028a-4900-afe6-1d9fce5303ef.png)
  
Angenommen, Sie möglicherweise einer DLP-Richtlinie zu OneDrive for Business-Websites angewendet, die personenbezogene Informationen (PII) erkennt, und diese Richtlinie hat drei Regeln:
  
1. Erste Regel: Wenn weniger als fünf Vorkommen dieser vertraulichen Informationen in einem Dokument erkannt werden und das Dokument für Personen innerhalb der Organisation freigegeben ist, wird bei der Aktion **Benachrichtigung senden** ein Richtlinientipp angezeigt. Für Richtlinientipps sind keine Optionen zum Außerkraftsetzen erforderlich, da diese Regel einfach Personen benachrichtigt und keinen Zugriff sperrt. 
    
2. Zweitens Regel: Wenn größer als fünf Instanzen dieser vertrauliche Informationen werden in einem Dokument erkannt, und das Dokument mit Personen innerhalb der Organisation freigeben, schränkt die Aktion **Blockieren des Zugriffs auf Inhalte** die Berechtigungen für die Datei, und die ** Senden Sie eine Benachrichtigung** Aktion können Personen, die Aktionen in dieser Regel außer Kraft gesetzt, durch die Bereitstellung als Rechtfertigung. Organisation erfordert manchmal interne Mitarbeiter PII Daten gemeinsam verwenden, und Sie nicht möchten, dass Ihre DLP-Richtlinie zu blockieren, diesen Vorgang. 
    
3. Dritte Regel: Wenn mehr als fünf Vorkommen dieser vertraulichen Informationen in einem Dokument erkannt werden und das Dokument für Personen außerhalb der Organisation freigegeben ist, schränkt die Aktion **Zugriff auf Inhalt sperren** die Berechtigungen für die Datei ein, und die Aktion **Benachrichtigung senden** erlaubt Personen nicht, die Aktionen in dieser Regel außer Kraft zu setzen, da die Informationen extern freigegeben werden. Mitarbeiter in Ihrer Organisation sollten unter keinen Umständen personenbezogene Daten außerhalb der Organisation freigeben dürfen. 
    
Hier sind einige wichtige Punkte zur Verwendung eines Richtlinientipps, um eine Regel außer Kraft zu setzen:
  
- Die Option außer Kraft gesetzt wird pro Regel, und sie überschrieben wird, alle Aktionen in der Regel (mit Ausnahme von Senden einer Benachrichtigung, die nicht überschrieben werden kann).
    
- Es ist möglich, dass Inhalte für mehrere Regeln in einer DLP-Richtlinie übereinstimmen, jedoch nur die richtlinientipp aus der Regel restriktivsten, höchste Priorität angezeigt werden soll. Beispielsweise einen richtlinientipp aus einer Regel, die blockiert den Zugriff auf Inhalt über einen richtlinientipp aus einer Regel angezeigt werden, die einfach eine Benachrichtigung sendet. Dadurch wird verhindert, dass Personen eine Hierarchie von richtlinientipps anzeigen.
    
- Wenn die Richtlinientipps in der restriktivsten Regel Benutzern erlauben, die Regel außer Kraft zu setzen, dann werden durch das Außerkraftsetzen dieser Regel auch alle weiteren Regeln außer Kraft gesetzt, welche mit dem Inhalt übereinstimmten.
    
## <a name="policy-tips-on-onedrive-for-business-sites-and-sharepoint-online-sites"></a>Richtlinientipps auf OneDrive für Business-Websites und SharePoint Online-Websites

Wenn ein Dokument in eine OneDrive for Business-Website oder SharePoint Online-Website eine Regel in einer DLP-Richtlinie entspricht, und diese Regel verwendet den Tipps zu Richtlinien, Anzeigen der richtlinientipps speziellen Symbole im Dokument:
  
1. Wenn die Regel eine Benachrichtigung über die Datei sendet, wird das Warnsymbol angezeigt.
    
2. Wenn die Regel den Zugriff auf das Dokument sperrt, wird das Sperrsymbol angezeigt.
    
![Richtlinie Tipp Symbole für Dokumente in einem OneDrive-Konto](media/d3e9f772-03f9-4d28-82f8-3064784332a2.png)
  
Um die Aktion in einem Dokument können Sie ein Element auswählen \> wählen Sie **Informationen**![Bereich Informationssymbol](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) in der oberen rechten Ecke der Seite, öffnen Sie im Detailbereich \> **richtlinientipp anzeigen**.
  
Der Richtlinientipp listet die Probleme mit dem Inhalt auf, und wenn die Richtlinientipps mit diesen Optionen konfiguriert sind, können Sie **Beheben** auswählen und dann den Richtlinientipp **außer Kraft setzen** oder ein falsch positives Ergebnis **melden** . 
  
![Informationen im Bereich mit richtlinientipp](media/0a191e70-80f0-4702-90f4-7a5b7aabcaab.png)
  
![Richtlinientipp mit Option zum Außerkraftsetzen](media/e250bff9-41d5-4ce4-82ea-1dc2d043fab1.png)
  
DLP-Richtlinien werden mit Websites synchronisiert, und Inhalte werden regelmäßig und asynchron anhand der Richtlinien ausgewertet, sodass es zwischen dem Zeitpunkt der Erstellung der DLP-Richtlinie und dem Beginn der Anzeige von Richtlinientipps zu einer Verzögerung kommen kann. Eine ähnliche Verzögerung kann auftreten, bis nach dem Beheben oder Außerkraftsetzen eines Richtlinientipps das Symbol im Dokument auf der Website nicht mehr angezeigt wird.
  
### <a name="default-text-for-policy-tips-on-sites"></a>Standardtext für Richtlinientipps auf Websites

In der Standardeinstellung zeigen Richtlinientipps für ein Element in einer Website Text wie den folgenden an. Der Benachrichtigungstext wird für jede Regel separat konfiguriert, damit sich der angezeigte Text abhängig von der angewendeten Regel unterscheidet.
  
| |
|**Wenn die DLP-Richtlinienregel dies tut...**|**Dann lautet der Standardtext eines Richtlinientipps folgendermaßen...**|
|:-----|:-----|
|Sendet eine Benachrichtigung, ermöglicht aber kein außer Kraft setzen  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |
|Sperrt Zugriff, sendet eine Benachrichtigung und erlaubt eine Außerkraftsetzung  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wenn Sie dieses Problem nicht lösen können, kann Zugriff auf diese Datei blockiert wird.  <br/> |
|Sperrt Zugriff und sendet eine Benachrichtigung  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Der Zugriff auf dieses Element wird für alle Benutzer mit Ausnahme des Besitzers, des Benutzers, der es zuletzt geändert hat und des primären Websitesammlungsadministrators gesperrt.  <br/> |
   
### <a name="custom-text-for-policy-tips-on-sites"></a>Standardtext für richtlinientipps auf Websites

Sie können den Text für richtlinientipps unabhängig von der e-Mail-Benachrichtigung anpassen. Im Gegensatz zu benutzerdefinierten Text für e-Mail-Benachrichtigungen (siehe oben im Abschnitt) akzeptiert benutzerdefinierter Text für richtlinientipps HTML oder Token keine. Standardtext für richtlinientipps ist nur-Text nur mit maximal 256 Zeichen.
  
## <a name="policy-tips-in-outlook-on-the-web-and-outlook-2013-and-later"></a>Richtlinie Tipps in Outlook im Web und Outlook 2013 und höher

Wenn beim Verfassen einer neuen e-Mails in Outlook im Web und Outlook 2013 und später einen richtlinientipp sehen, wenn Sie Inhalte hinzufügen, das eine Regel in einer DLP-Richtlinie entspricht, und diese Regel verwendet den Tipps zu Richtlinien. Die Richtlinie-Info wird am oberen Rand der Nachricht, über die Empfänger angezeigt, während die Nachricht erstellt wurde.
  
![Richtlinientipp am oberen Rand eine Nachricht verfasst wird](media/9b3b6b74-17c5-4562-82d5-d17ecaaa8d95.png)
  
Richtlinie Tipps Arbeit, ob die vertrauliche Informationen im Textkörper der Nachricht, die Betreffzeile oder sogar e-Mail-Anlagen angezeigt wird, wie hier gezeigt.
  
![Richtlinientipp, die darauf hinweist, dass eine Anlage zu mit einer DLP-Richtlinie Konflikten](media/59ae6655-215f-47d9-ad1d-39c0d1e61740.png)
  
Wenn die richtlinientipps für die Außerkraftsetzung zulassen konfiguriert sind, können Sie **Details anzeigen** auswählen \> **außer Kraft setzen** \> als Rechtfertigung eingeben oder falsch positives Ergebnis melden \> **außer Kraft setzen**.
  
![Richtlinientipp in Nachricht erweitert, um die Option für die Außerkraftsetzung anzeigen](media/28bfb997-48a6-41f0-8682-d5e62488458a.png)
  
![Richtlinie Tipp Dialogfeld, in dem die richtlinientipp überschrieben werden kann](media/f97e836c-04bd-44b4-aec6-ed9526ea31f8.png)
  
Beachten Sie, dass Sie eine e-Mail-Nachricht vertraulichen Informationen hinzugefügt, liegt möglicherweise Wartezeit zwischen Wenn vertrauliche Informationen hinzugefügt wird und wenn der richtlinientipp angezeigt wird.

### <a name="outlook-2013-and-later-supports-showing-policy-tips-for-only-some-conditions"></a>Outlook 2013 und höher mit Tipps zu Richtlinien für nur einige Bedingungen unterstützt

Derzeit unterstützt Outlook 2013 und höher mit richtlinientipps nur für diese Bedingungen:

- Inhalt enthält
- Inhalte werden freigegeben.

Wir arbeiten derzeit Unterstützung für das Anzeigen von Tipps zu Richtlinien für zusätzliche Bedingungen. Dazu zählen folgende:

- Inhalt einer e-Mail-Anlage konnte nicht überprüft werden
- Inhalt einer e-Mail-Anlage nicht vollständig überprüft
- Erweiterung für die Anlage ist
- Anlage ist kennwortgeschützt
- Ist der Document-Eigenschaft
- Domäne des Empfängers ist
- IP-Adresse des Absenders

Beachten Sie, dass alle diese Aktionen in Outlook arbeiten, in dem sie entspricht Inhalte und erzwingen Schutzvorrichtungen Aktionen auf Inhalt. Aber mit Tipps zu Richtlinien für Benutzer wird noch nicht unterstützt.
  
### <a name="policy-tips-in-the-exchange-admin-center-vs-the-office-365-security-amp-compliance-center"></a>Tipps zu Richtlinien in der Exchange-Verwaltungskonsole im Vergleich zu den Office 365-Sicherheit &amp; Compliance Center

Tipps zu Richtlinien können arbeiten entweder mit DLP-Richtlinien und e-Mail Flussregeln erstellt, in der Exchange-Verwaltungskonsole oder mit DLP-Richtlinien in der Office 365-Sicherheit erstellten &amp; Compliance Center, jedoch nicht beide. Dies ist, da diese Richtlinien werden an unterschiedlichen Standorten gespeichert, aber richtlinientipps können nur von einem einzigen Standort zeichnen.
  
Wenn Sie in der Exchange-Verwaltungskonsole eine beliebige richtlinientipps richtlinientipps konfiguriert haben, die Sie in der Office 365-Sicherheit konfigurieren &amp; Compliance Center wird nicht angezeigt, für die Benutzer in Outlook im Web und Outlook 2013 und höher, bis Sie die Tipps in den Austausch deaktivieren Admin Center. Dadurch wird sichergestellt, dass Ihre aktuellen Exchange-Transportregeln funktionsfähig weiterhin, bis Sie entscheiden, ob die Office 365-Sicherheit zu wechseln &amp; Compliance Center.
  
Notiz, die während der richtlinientipps nur von einem einzigen Standort, zeichnen können e-Mail-Benachrichtigungen sind immer gesendet, selbst wenn Sie die Office 365 Sicherheit DLP-Richtlinien verwenden, &amp; Compliance Center und der Exchange-Verwaltungskonsole.
  
### <a name="default-text-for-policy-tips-in-email"></a>Standardtext für richtlinientipps in e-Mail

In der Standardeinstellung Anzeigetext richtlinientipps ähnlich dem folgenden für e-Mail.

|**Wenn die DLP-Richtlinienregel dies tut...**|**Dann lautet der Standardtext eines Richtlinientipps folgendermaßen...**|
|:-----|:-----|
|Sendet eine Benachrichtigung, ermöglicht aber kein außer Kraft setzen  <br/> |Ihre e-Mail-steht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |
|Sperrt Zugriff, sendet eine Benachrichtigung und erlaubt eine Außerkraftsetzung  <br/> |Ihre e-Mail-steht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |
|Sperrt Zugriff und sendet eine Benachrichtigung  <br/> |Ihre e-Mail-steht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |
   
## <a name="policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Tipps zu Richtlinien in Excel 2016, PowerPoint 2016 und Word 2016

Wenn Benutzer mit vertraulichen Inhalten in den Desktopversionen von Excel 2016, PowerPoint 2016 und Word 2016 arbeiten, können Richtlinientipps sie in Echtzeit benachrichtigen, dass der Inhalt mit einer DLP-Richtlinie in Konflikt steht. Folgende Voraussetzungen müssen erfüllt sein:
  
- Das Office-Dokument ist auf einer OneDrive for Business-Website oder SharePoint Online-Website gespeichert.
    
- Die Website ist in einer DLP-Richtlinie enthalten, die richtlinientipps konfiguriert ist.
    
Diese desktop 2016 Office-Programme automatisch DLP-Richtlinien direkt vom Office 365 synchronisieren und überprüfen Sie Ihre Dokumente, um sicherzustellen, dass sie nicht in mit Ihrer DLP-Richtlinien Konflikt und Tipps zu Richtlinien in Echtzeit anzuzeigen.
  
Je nachdem, wie Sie die Richtlinientipps in der DLP-Richtlinie konfigurieren, können Benutzer wählen, den Richtlinientipp einfach zu ignorieren, die Richtlinie mit oder ohne geschäftliche Begründung außer Kraft zu setzen oder ein falsch positives Ergebnis zu melden.
  
Richtlinientipps werden auf der Statusleiste angezeigt.
  
![Statusleiste zeigt Richtlinientipp in Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Und Richtlinientipps werden auch in der Backstage-Ansicht angezeigt (auf der Registerkarte **Datei**). 
  
![Backstage zeigt Richtlinientipp in Excel 2016](media/44c561f6-8f3f-4878-b1b0-b7543f8a4120.png)
  
Wenn die Richtlinie Tipps in die DLP-Richtlinie mit diesen Optionen konfiguriert sind, können Sie entscheiden **zu beheben** , **außer Kraft gesetzt** ein richtlinientipp oder einen **Bericht** falsch positives Ergebnis. 
  
![Optionen für Richtlinientipp in Backstage in Excel 2016](media/5b3857ba-907e-456e-ae43-888b594c049c.png)
  
In jedem dieser Office 2016-Desktopprogramme können Personen Richtlinientipps deaktivieren. Wenn Richtlinientipps deaktiviert sind, werden Richtlinientipps, die einfache Benachrichtigungen sind, nicht in der Statusleiste oder der Backstage-Ansicht (auf der Registerkarte **Datei**) angezeigt. Richtlinientipps zum Sperren oder Außerkraftsetzen werden jedoch weiterhin angezeigt, und sie erhalten weiterhin die E-Mail-Benachrichtigung. Darüber hinaus wird durch das Deaktivieren von Richtlinientipps das Dokument nicht von DLP-Richtlinien ausgenommen, die darauf angewendet wurden. 
  
### <a name="default-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Standardtext für Richtlinientipps in Excel 2016, PowerPoint 2016 und Word 2016

Richtlinientipps zeigen in der Statusleiste und Backstage-Ansicht eines geöffneten Dokuments standardmäßig Text wie den folgenden an. Der Benachrichtigungstext wird für jede Regel separat konfiguriert, damit sich der angezeigte Text abhängig von der angewendeten Regel unterscheidet.

|**Wenn die DLP-Richtlinienregel dies tut...**|**Dann lautet der Standardtext eines Richtlinientipps folgendermaßen...**|
|:-----|:-----|
|Sendet eine Benachrichtigung, ermöglicht aber kein außer Kraft setzen  <br/> |Diese Datei steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wechseln Sie zur Weitere Informationen im Menü **Datei** .<br/> |
|Sperrt Zugriff, sendet eine Benachrichtigung und erlaubt eine Außerkraftsetzung  <br/> |Diese Datei steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wenn Sie dieses Problem nicht lösen können, kann Zugriff auf diese Datei blockiert wird. Wechseln Sie zur Weitere Informationen im Menü **Datei** .<br/> |
|Sperrt Zugriff und sendet eine Benachrichtigung  <br/> |Diese Datei steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wenn Sie dieses Problem nicht lösen können, kann Zugriff auf diese Datei blockiert wird. Wechseln Sie zur Weitere Informationen im Menü **Datei** .<br/> |
   
### <a name="custom-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Tipps zu benutzerdefinierter Text für die Richtlinie in Excel 2016, 2016 PowerPoint und Word 2016

Sie können den Text für richtlinientipps unabhängig von der e-Mail-Benachrichtigung anpassen. Im Gegensatz zu benutzerdefinierten Text für e-Mail-Benachrichtigungen (siehe oben im Abschnitt) akzeptiert benutzerdefinierter Text für richtlinientipps HTML oder Token keine. Standardtext für richtlinientipps ist nur-Text nur mit maximal 256 Zeichen.
  
## <a name="more-information"></a>Weitere Informationen

- [Übersicht über die Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md)
    
- [Erstellen einer DLP-Richtlinie aus einer Vorlage](create-a-dlp-policy-from-a-template.md)
    
- [Erstellen einer DLP-Richtlinie zum Schützen von Dokumenten mit FCI oder anderen Eigenschaften](protect-documents-that-have-fci-or-other-properties.md)
    
- [Inhalt der DLP-Richtlinienvorlagen](what-the-dlp-policy-templates-include.md)
    
- [Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)
    

