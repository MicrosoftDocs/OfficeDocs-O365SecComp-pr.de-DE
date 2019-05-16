---
title: Senden von E-Mail-Benachrichtigungen und Anzeigen von Richtlinientipps für DLP-Richtlinien
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleNotifyUser
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 'Ein richtlinientipp ist eine Benachrichtigung oder Warnung, die angezeigt wird, wenn ein Benutzer mit Inhalten arbeitet, die mit einer DLP-Richtlinie in Konflikt stehen. Sie können e-Mail-Benachrichtigungen und Richtlinien Tipps verwenden, um die Aufmerksamkeit zu verbessern und Personen über die Richtlinien Ihrer Organisation zu informieren. Sie können den Benutzern auch die Möglichkeit geben, die Richtlinie außer Kraft zu setzen, damit Sie nicht blockiert werden, wenn Sie über eine gültige geschäftliche Anforderung verfügen oder wenn die Richtlinie ein falsch positives Ergebnis ermittelt. '
ms.openlocfilehash: 487d3704b471b10ec876b0df3022d33d13583763
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077361"
---
# <a name="send-email-notifications-and-show-policy-tips-for-dlp-policies"></a>Senden von E-Mail-Benachrichtigungen und Anzeigen von Richtlinientipps für DLP-Richtlinien

Sie können eine DLP-Richtlinie (Data Loss Prevention, Datenverlust Verhütung) verwenden, um vertrauliche Informationen in Office 365 zu identifizieren, zu überwachen und zu schützen. Sie möchten, dass Personen in Ihrer Organisation, die mit diesen vertraulichen Informationen arbeiten, mit ihren DLP-Richtlinien kompatibel bleiben, Sie möchten Sie jedoch nicht unnötigerweise daran hindern, ihre Arbeit zu erledigen. Hier können e-Mail-Benachrichtigungen und Richtlinien Tipps helfen.
  
![Nachrichtenleiste zeigt richtlinientipp in Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Ein richtlinientipp ist eine Benachrichtigung oder Warnung, die angezeigt wird, wenn jemand mit Inhalten arbeitet, die mit einer DLP-Richtlinie in Konflikt stehen, beispielsweise Inhalte wie eine Excel-Arbeitsmappe auf einer OneDrive for Business-Website, die personenbezogene Informationen (PII) enthält und für einen externen Benutzer freigegeben.
  
Sie können e-Mail-Benachrichtigungen und Richtlinien Tipps verwenden, um die Aufmerksamkeit zu verbessern und Personen über die Richtlinien Ihrer Organisation zu informieren. Sie können den Benutzern auch die Möglichkeit geben, die Richtlinie außer Kraft zu setzen, damit Sie nicht blockiert werden, wenn Sie über eine gültige geschäftliche Anforderung verfügen oder wenn die Richtlinie ein falsch positives Ergebnis ermittelt.
  
Wenn Sie eine DLP- &amp; Richtlinie erstellen, können Sie im Office 365 Security Compliance Center folgende Benutzer Benachrichtigungen konfigurieren:
  
- Senden Sie eine e-Mail-Benachrichtigung an die von Ihnen ausgewählten Personen, die das Problem beschreiben.
    
- Anzeigen eines Richtlinien Tipps für Inhalte, die mit der DLP-Richtlinie in Konflikt stehen:
    
  - Bei e-Mails in Outlook im Web und Outlook 2013 und höher wird der richtlinientipp oben in einer Nachricht oberhalb der Empfänger angezeigt, während die Nachricht erstellt wird.
    
  - Für Dokumente in einem OneDrive-Konto oder einer SharePoint Online-Website wird der richtlinientipp durch ein Warnsymbol angezeigt, das auf dem Element angezeigt wird. Um weitere Informationen anzuzeigen, können Sie ein Element auswählen und dann in ****![der oberen rechten Ecke](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) der Seite auf das Symbol Informations Informationsbereich klicken, um den Detailbereich zu öffnen. 
    
  - Für Excel 2016, PowerPoint 2016 und Word 2016-Dokumente, die auf einer OneDrive for Business-Website oder SharePoint Online-Website gespeichert sind, die in der DLP-Richtlinie enthalten ist, wird der richtlinientipp in der Statusleiste und der backstaging-Ansicht angezeigt (Menü " **Datei** " \> ** Info**).
    
## <a name="add-user-notifications-to-a-dlp-policy"></a>Hinzufügen von Benutzer Benachrichtigungen zu einer DLP-Richtlinie

Wenn Sie eine DLP-Richtlinie erstellen, sind sowohl e-Mail-Benachrichtigungen als auch Richtlinien Tipps Teil des Abschnitts " **Benutzer Benachrichtigungen** ". 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an. Sie befinden sich jetzt im Office 365 Security &amp; Compliance Center.
    
3. Im Security &amp; Compliance \> Center Left Navigation \> **Data Loss Prevention** \> **Policy** \> **+ Create a Policy**.
    
    ![Erstellen einer Richtlinien Schaltfläche](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Wählen Sie die DLP-Richtlinienvorlage aus, die die Arten von vertraulichen \> Informationen schützt, die Sie **als nächstes**benötigen.
    
    Wenn Sie mit einer leeren Vorlage beginnen möchten, wählen Sie **als nächstes**die Option **Benutzer** \> **definierte Richtlinie** \> aus.
    
5. Benennen Sie die \> Richtlinie **als nächstes**.
    
6. Führen Sie einen der folgenden Schritte aus, um die Speicherorte auszuwählen, die von der DLP-Richtlinie geschützt werden sollen:
    
  - Wählen Sie **alle Standorte in Office 365** \> **Next**aus.
    
  - Wählen Sie die Option **Ich möchte bestimmte Standorte** \> **** auswählen.
    
    Wenn Sie einen gesamten Speicherort wie alle Exchange-e-Mails oder alle OneDrive-Konten einschließen oder ausschließen möchten, schalten Sie den **Status** dieses Standorts ein oder aus. 
    
    Um nur bestimmte SharePoint-Websites oder OneDrive-Konten einzuschließen, schalten Sie den **Status** auf ein, und klicken Sie dann auf die Links unter **include** , um bestimmte Websites oder Konten auszuwählen. 
    
7. Wählen Sie \> **weiter** **Erweiterte Einstellungen verwenden** aus.
    
8. Wählen Sie **+ neue Regel**aus.
    
9. Schalten Sie im Regel-Editor unter **Benutzer Benachrichtigungen**den Status ein.
    
    ![Abschnitt "Benutzer Benachrichtigungen" des Regel-Editors](media/47705927-c60b-4054-a072-ab914f33d15d.png)
  
## <a name="options-for-configuring-email-notifications"></a>Optionen zum Konfigurieren von e-Mail-Benachrichtigungen

Für jede Regel in einer DLP-Richtlinie können Sie Folgendes tun:
  
- Senden Sie die Benachrichtigung an die Personen, die Sie auswählen. Zu diesen Personen gehört der Besitzer des Inhalts, die Person, die den Inhalt zuletzt geändert hat, der Besitzer der Website, auf der der Inhalt gespeichert ist, oder ein bestimmter Benutzer.
    
- Passen Sie den in der Benachrichtigung enthaltenen Text mithilfe von HTML oder Token an. Weitere Informationen finden Sie im folgenden Abschnitt.
    
> [!NOTE]
>  E-Mail-Benachrichtigungen können nur an einzelne Empfänger gesendet werden – nicht an Gruppen oder Verteilerlisten. Nur neuer Inhalt löst eine e-Mail-Benachrichtigung aus. Das Bearbeiten vorhandener Inhalte löst Richtlinien Tipps aus, jedoch keine e-Mail-Benachrichtigung. 
  
![E-Mail-Benachrichtigungsoptionen](media/4e7b9500-2a78-44e6-9067-09f4bfd50301.png)
  
### <a name="default-email-notification"></a>Standard-e-Mail-Benachrichtigung

Benachrichtigungen haben eine Betreffzeile, die mit der durchgeführten Aktion beginnt, beispielsweise "Benachrichtigung", "blockierte Nachricht" für e-Mails oder "Zugriff blockiert" für Dokumente. Wenn es sich bei der Benachrichtigung um ein Dokument handelt, enthält der Benachrichtigungstext einen Link zu der Website, auf der das Dokument gespeichert ist, und öffnet den richtlinientipp für das Dokument, in dem Sie Probleme beheben können (siehe Abschnitt weiter unten zu Richtlinien Tipps). Wenn es sich bei der Benachrichtigung um eine Nachricht handelt, enthält die Benachrichtigung als Anlage die Nachricht, die einer DLP-Richtlinie entspricht.
  
![Benachrichtigung](media/35813d40-5fd8-425f-9624-55655e74fa6b.png)
  
Standardmäßig zeigen Benachrichtigungen für ein Element auf einer Website Text ähnlich der folgenden an. Der Benachrichtigungstext wird für jede Regel separat konfiguriert, sodass der angezeigte Text unterschiedlich ist, je nachdem, welcher Regel entsprochen wird.

|**Wenn die DLP-Richtlinienregel dies tut...**|**Dann lautet die Standardbenachrichtigung für SharePoint-oder OneDrive for Business-Dokumente...**|**Dann lautet die Standardbenachrichtigung für Outlook-Nachrichten...**|
|:-----|:-----|:-----|
|Sendet eine Benachrichtigung, aber keine Außerkraftsetzung  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |Ihre e-Mail-Nachricht steht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |
|Blockiert den Zugriff, sendet eine Benachrichtigung und lässt die Überschreibung zu  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wenn Sie diesen Konflikt nicht beheben, wird der Zugriff auf diese Datei möglicherweise blockiert.  <br/> |Ihre e-Mail-Nachricht steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Die Nachricht wurde nicht an alle Empfänger übermittelt.  <br/> |
|Blockiert den Zugriff und sendet eine Benachrichtigung  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Der Zugriff auf dieses Element ist für alle Benutzer mit Ausnahme des Besitzers, des letzten Modifizierers und des primären Websitesammlungsadministrators blockiert.  <br/> |Ihre e-Mail-Nachricht steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Die Nachricht wurde nicht an alle Empfänger übermittelt.  <br/> |
   
### <a name="custom-email-notification"></a>Benutzerdefinierte e-Mail-Benachrichtigung

Sie können eine benutzerdefinierte e-Mail-Benachrichtigung erstellen, anstatt die Standard-e-Mail-Benachrichtigung an Ihre Endbenutzer oder Administratoren zu senden. Die benutzerdefinierte e-Mail-Benachrichtigung unterstützt HTML und hat einen Grenzwert von 5.000 Zeichen. Sie können HTML verwenden, um Bilder, Formatierungen und andere Brandingfunktionen in die Benachrichtigung einzuschließen.
  
Sie können auch die folgenden Token verwenden, um die e-Mail-Benachrichtigung anzupassen. Diese Token sind Variablen, die durch bestimmte Informationen in der gesendeten Benachrichtigung ersetzt werden.

|**Token**|**Beschreibung**|
|:-----|:-----|
|%% AppliedActions%%  <br/> |Die Aktionen, die auf den Inhalt angewendet werden.  <br/> |
|%% ContentURL%%  <br/> |Die URL des Dokuments auf der SharePoint Online-Website oder OneDrive for Business-Website.  <br/> |
|%%MatchedConditions%%  <br/> |Die Bedingungen, die mit dem Inhalt verglichen wurden. Verwenden Sie dieses Token, um Personen über mögliche Probleme mit dem Inhalt zu informieren.  <br/> |
   
![Benachrichtigungsmeldung mit angezeigtem Token](media/cd3f36b3-40db-4f30-99e4-190750bd1955.png)
  
## <a name="options-for-configuring-policy-tips"></a>Optionen zum Konfigurieren von Richtlinien Tipps

Für jede Regel in einer DLP-Richtlinie können Sie Richtlinien Tipps für Folgendes konfigurieren:
  
- Teilen Sie der Person einfach mit, dass der Inhalt mit einer DLP-Richtlinie in Konflikt steht, damit Sie Maßnahmen ergreifen können, um den Konflikt zu beheben. Sie können den Standardtext (siehe die folgenden Tabellen) verwenden oder benutzerdefinierten Text zu den spezifischen Richtlinien Ihrer Organisation eingeben.
    
- Die Person kann die DLP-Richtlinie außer Kraft setzen. Optional können Sie Folgendes tun:
    
  - Die Person muss eine geschäftliche Begründung für das Überschreiben der Richtlinie eingeben. Diese Informationen werden protokolliert und können in den DLP-Berichten im Abschnitt " **Berichte** " des Security &amp; Compliance Centers angezeigt werden. 
    
  - Die Person kann ein falsch positives Ergebnis melden und die DLP-Richtlinie außer Kraft setzen. Diese Informationen werden auch für die Berichterstellung protokolliert, sodass Sie falsch positive Ergebnisse verwenden können, um ihre Regeln zu optimieren.
    
![Richtlinientipp Optionen](media/0d2f2c68-028a-4900-afe6-1d9fce5303ef.png)
  
Möglicherweise haben Sie eine DLP-Richtlinie auf OneDrive für Business-Websites angewendet, die personenbezogene Informationen (PII) erkennt, und diese Richtlinie hat drei Regeln:
  
1. Erste Regel: Wenn in einem Dokument weniger als fünf Instanzen dieser vertraulichen Informationen erkannt werden und das Dokument für Personen innerhalb der Organisation freigegeben wird, wird mit der Aktion **Benachrichtigung senden** ein richtlinientipp angezeigt. Für Richtlinien Tipps sind keine Außerkraftsetzungsoptionen erforderlich, da diese Regel lediglich Personen benachrichtigt und keinen Zugriff blockiert. 
    
2. Zweite Regel: Wenn in einem Dokument mehr als fünf Instanzen dieser vertraulichen Informationen erkannt werden und das Dokument für Personen innerhalb der Organisation freigegeben wird, schränkt die Aktion **Zugriff auf Inhalt blockieren** die Berechtigungen für die Datei ein und ** Benachrichtigungsaktion senden** ermöglicht es Benutzern, die Aktionen in dieser Regel zu überschreiben, indem eine geschäftliche Begründung bereitgestellt wird. Das Geschäft Ihrer Organisation erfordert manchmal interne Personen, die PII-Daten freigeben, und Sie möchten nicht, dass ihre DLP-Richtlinie diese Arbeit blockiert. 
    
3. Dritte Regel: Wenn in einem Dokument mehr als fünf Instanzen dieser vertraulichen Informationen erkannt werden und das Dokument für Personen außerhalb der Organisation freigegeben wird, schränkt die Aktion **Zugriff auf Inhalt blockieren** die Berechtigungen für die Datei ein und ** Benachrichtigungsaktion senden** ermöglicht es Benutzern nicht, die Aktionen in dieser Regel außer Kraft zu setzen, da die Informationen extern freigegeben werden. Unter keinen Umständen sollten Personen in Ihrer Organisation berechtigt sein, PII-Daten außerhalb der Organisation freizugeben. 
    
Hier sind einige feine Punkte, die Sie über die Verwendung eines Richtlinien Tipps zum Überschreiben einer Regel verstehen:
  
- Die Option zum Überschreiben ist pro Regel, und Sie überschreibt alle Aktionen in der Regel (außer dem Senden einer Benachrichtigung, die nicht außer Kraft gesetzt werden kann).
    
- Inhalte können in einer DLP-Richtlinie mit mehreren Regeln übereinstimmen, aber nur der richtlinientipp von der restriktivsten Regel mit der höchsten Priorität wird angezeigt. Beispielsweise wird ein richtlinientipp aus einer Regel, die den Zugriff auf Inhalte blockiert, über einen richtlinientipp aus einer Regel angezeigt, die einfach eine Benachrichtigung sendet. Dadurch wird verhindert, dass Personen eine Kaskade von Richtlinien Tipps sehen.
    
- Wenn die Richtlinien Tipps in der restriktivsten Regel es Benutzern ermöglichen, die Regel außer Kraft zu setzen, überschreibt diese Regel auch alle anderen Regeln, die mit dem Inhalt übereinstimmten.
    
## <a name="policy-tips-on-onedrive-for-business-sites-and-sharepoint-online-sites"></a>Richtlinien Tipps auf OneDrive for Business-Websites und SharePoint Online-Websites

Wenn ein Dokument auf einer OneDrive for Business-Website oder einer SharePoint Online-Website einer Regel in einer DLP-Richtlinie entspricht und diese Regelrichtlinien Tipps verwendet, werden in den Richtlinien Tipps spezielle Symbole im Dokument angezeigt:
  
1. Wenn die Regel eine Benachrichtigung über die Datei sendet, wird das Warnsymbol angezeigt.
    
2. Wenn die Regel den Zugriff auf das Dokument blockiert, wird das Symbol blockiert angezeigt.
    
![Richtlinientipp Symbole für Dokumente in einem OneDrive-Konto](media/d3e9f772-03f9-4d28-82f8-3064784332a2.png)
  
Wenn Sie eine Aktion für ein Dokument ausführen möchten, können Sie \> ](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) in ****![der rechten oberen Ecke der Seite ein Element auswählen, um den Detailbereich \> **Ansichts Richtlinien**Info zu öffnen.
  
Der richtlinientipp listet die Probleme mit dem Inhalt auf, und wenn die Richtlinien Tipps mit diesen Optionen konfiguriert sind, können Sie **Auflösen**auswählen und dann den richtlinientipp **außer Kraft setzen** oder ein falsch positives Ergebnis **melden** . 
  
![Informationsbereich mit richtlinientipp](media/0a191e70-80f0-4702-90f4-7a5b7aabcaab.png)
  
![Richtlinientipp mit Option zum außer Kraft setzen](media/e250bff9-41d5-4ce4-82ea-1dc2d043fab1.png)
  
DLP-Richtlinien werden mit Websites synchronisiert, und die Inhalte werden regelmäßig und asynchron gegen Sie ausgewertet, sodass zwischen dem Zeitpunkt, zu dem Sie die DLP-Richtlinie erstellen, und dem Zeitpunkt, zu dem Sie mit Richtlinien Tipps beginnen, eine kurze Verzögerung auftreten kann. Es kann eine ähnliche Verzögerung geben, wenn Sie einen richtlinientipp auflösen oder außer Kraft setzen, wenn das Symbol im Dokument auf der Website verschwindet.
  
### <a name="default-text-for-policy-tips-on-sites"></a>Standardtext für Richtlinien Tipps auf Websites

Standardmäßig werden in den Richtlinien Tipps für ein Element auf einer Website Text ähnlich der folgenden angezeigt. Der Benachrichtigungstext wird für jede Regel separat konfiguriert, sodass der angezeigte Text unterschiedlich ist, je nachdem, welcher Regel entsprochen wird.

|**Wenn die DLP-Richtlinienregel dies tut...**|**Dann lautet der Standardrichtlinien Tipp this...**|
|:-----|:-----|
|Sendet eine Benachrichtigung, aber keine Außerkraftsetzung  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation.  <br/> |
|Blockiert den Zugriff, sendet eine Benachrichtigung und lässt die Überschreibung zu  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wenn Sie diesen Konflikt nicht beheben, wird der Zugriff auf diese Datei möglicherweise blockiert.  <br/> |
|Blockiert den Zugriff und sendet eine Benachrichtigung  <br/> |Dieses Element steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Der Zugriff auf dieses Element ist für alle Benutzer mit Ausnahme des Besitzers, des letzten Modifizierers und des primären Websitesammlungsadministrators blockiert.  <br/> |
   
### <a name="custom-text-for-policy-tips-on-sites"></a>Benutzerdefinierter Text für Richtlinien Tipps auf Websites

Sie können den Text für Richtlinien Tipps separat von der e-Mail-Benachrichtigung anpassen. Anders als benutzerdefinierter Text für e-Mail-Benachrichtigungen (siehe Abschnitt oben) akzeptiert der benutzerdefinierte Text für Richtlinien Tipps weder HTML noch Token. Benutzerdefinierter Text für Richtlinien Tipps ist stattdessen nur-Text mit einem Grenzwert von 256 Zeichen.
  
## <a name="policy-tips-in-outlook-on-the-web-and-outlook-2013-and-later"></a>Richtlinien Tipps in Outlook im Web und Outlook 2013 und höher

Wenn Sie eine neue e-Mail in Outlook im Web und Outlook 2013 und höher verfassen, wird ein richtlinientipp angezeigt, wenn Sie Inhalte hinzufügen, die einer Regel in einer DLP-Richtlinie entsprechen, und diese Regel verwendet Richtlinien Tipps. Der richtlinientipp wird oben in der Nachricht oberhalb der Empfänger angezeigt, während die Nachricht erstellt wird.
  
![Richtlinientipp am Anfang einer zusammengesetzten Nachricht](media/9b3b6b74-17c5-4562-82d5-d17ecaaa8d95.png)
  
Richtlinien Tipps funktionieren, ob die vertraulichen Informationen im Nachrichtentext, in der Betreffzeile oder sogar in einer Nachrichtenanlage angezeigt werden (siehe hier).
  
![Richtlinientipp, der zeigt, dass eine Anlage mit einer DLP-Richtlinie in Konflikt steht](media/59ae6655-215f-47d9-ad1d-39c0d1e61740.png)
  
Wenn die Richtlinien Tipps so konfiguriert sind, dass eine Außerkraftsetzung zulässig ist, können Sie die Überschreibung **anzeigen Details** \> **** \> eingeben wählen \> Sie eine geschäftliche Begründung oder eine falsch positive **Überschreibung**.
  
![Richtlinientipp in Nachricht erweitert zum Anzeigen der Außerkraftsetzungsoption](media/28bfb997-48a6-41f0-8682-d5e62488458a.png)
  
![Richtlinientipp Dialogfeld, in dem Sie den richtlinientipp außer Kraft setzen können](media/f97e836c-04bd-44b4-aec6-ed9526ea31f8.png)
  
Beachten Sie, dass beim Hinzufügen vertraulicher Informationen zu einer e-Mail-Nachricht möglicherweise Latenzzeiten auftreten, wenn die vertraulichen Informationen hinzugefügt werden und der richtlinientipp angezeigt wird.

### <a name="outlook-2013-and-later-supports-showing-policy-tips-for-only-some-conditions"></a>Outlook 2013 und höher unterstützt das Anzeigen von Richtlinien Tipps nur für bestimmte Bedingungen

Outlook 2013 und höher unterstützt derzeit nur für die folgenden Bedingungen Richtlinien Tipps:

- Inhalt enthält
- Inhalte werden freigegeben

Wir arbeiten derzeit an Unterstützung für das Anzeigen von Richtlinien Tipps für zusätzliche Bedingungen. Zu diesen zählen:

- Der Inhalt einer e-Mail-Anlage konnte nicht gescannt werden.
- Der Inhalt der e-Mail-Anlage wurde nicht vollständig überprüft
- Anlagendatei Erweiterung ist
- Anlage ist kennwortgeschützt
- Document-Eigenschaft ist
- Empfängerdomäne ist
- Absender-IP-Adresse ist

Beachten Sie, dass alle diese Bedingungen in Outlook funktionieren, wo Sie mit Inhalten übereinstimmen und Schutzmaßnahmen für Inhalte erzwingen. Das Anzeigen von Richtlinien Tipps für Benutzer wird jedoch noch nicht unterstützt.
  
### <a name="policy-tips-in-the-exchange-admin-center-vs-the-office-365-security-amp-compliance-center"></a>Richtlinien Tipps im Exchange Admin Center im Vergleich zum Office 365 Security &amp; Compliance Center

Richtlinien Tipps können entweder mit DLP-Richtlinien und Nachrichtenfluss Regeln im Exchange Admin Center oder mit im Office 365 Security &amp; Compliance Center erstellten DLP-Richtlinien funktionieren, jedoch nicht mit beiden. Der Grund hierfür liegt darin, dass diese Richtlinien an unterschiedlichen Speicherorten gespeichert werden, Richtlinien Tipps können jedoch nur von einem Speicherort aus erstellt werden.
  
Wenn Sie im Exchange Admin Center Richtlinien Tipps konfiguriert haben, werden alle Richtlinien Tipps, die Sie im Office 365 Security &amp; Compliance Center konfigurieren, nicht für Benutzer in Outlook im Web und Outlook 2013 und höher angezeigt, bis Sie die Tipps im Exchange Admin Center. Dadurch wird sichergestellt, dass Ihre aktuellen Exchange-Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) weiterhin funktionieren, bis Sie sich für das Office 365 Security &amp; Compliance Center entscheiden.
  
Beachten Sie, dass während Richtlinien Tipps nur von einem einzigen Ort aus gezeichnet werden können, e-Mail-Benachrichtigungen auch dann immer gesendet werden, wenn Sie DLP- &amp; Richtlinien sowohl im Office 365 Security Compliance Center als auch im Exchange Admin Center verwenden.
  
### <a name="default-text-for-policy-tips-in-email"></a>Standardtext für Richtlinien Tipps in e-Mail

Standardmäßig werden in den Richtlinien Tipps Text ähnlich der folgenden für e-Mails angezeigt.

|**Wenn die DLP-Richtlinienregel dies tut...**|**Dann lautet der Standardrichtlinien Tipp this...**|
|:-----|:-----|
|Sendet eine Benachrichtigung, aber keine Außerkraftsetzung  <br/> |Ihre e-Mail steht mit einer Richtlinie in Ihrer Organisation in Konflikt.  <br/> |
|Blockiert den Zugriff, sendet eine Benachrichtigung und lässt die Überschreibung zu  <br/> |Ihre e-Mail steht mit einer Richtlinie in Ihrer Organisation in Konflikt.  <br/> |
|Blockiert den Zugriff und sendet eine Benachrichtigung  <br/> |Ihre e-Mail steht mit einer Richtlinie in Ihrer Organisation in Konflikt.  <br/> |
   
## <a name="policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Richtlinien Tipps in Excel 2016, PowerPoint 2016 und Word 2016

Wenn Benutzer mit vertraulichen Inhalten in den Desktop Versionen von Excel 2016, PowerPoint 2016 und Word 2016 arbeiten, können Sie diese in Echtzeit darüber informieren, dass der Inhalt mit einer DLP-Richtlinie in Konflikt steht. Dies erfordert Folgendes:
  
- Das Office-Dokument wird auf einer OneDrive for Business-Website oder einer SharePoint Online-Website gespeichert.
    
- Die Website ist in einer DLP-Richtlinie enthalten, die für die Verwendung von Richtlinien Tipps konfiguriert ist.
    
Diese Office 2016-Desktop Programme synchronisieren DLP-Richtlinien automatisch von Office 365 und überprüfen dann Ihre Dokumente, um sicherzustellen, dass Sie nicht mit ihren DLP-Richtlinien in Konflikt stehen und Richtlinien Tipps in Echtzeit anzeigen.
  
Je nachdem, wie Sie die Richtlinien Tipps in der DLP-Richtlinie konfigurieren, können Benutzer den richtlinientipp einfach ignorieren, die Richtlinie mit oder ohne geschäftliche Begründung außer Kraft setzen oder ein falsch positives Ergebnis melden.
  
Richtlinien Tipps werden in der Statusleiste angezeigt.
  
![Nachrichtenleiste zeigt richtlinientipp in Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Und Richtlinien Tipps werden auch in der backstaging-Ansicht (auf der Registerkarte **Datei** ) angezeigt. 
  
![Backstaging zeigt richtlinientipp in Excel 2016](media/44c561f6-8f3f-4878-b1b0-b7543f8a4120.png)
  
Wenn Richtlinien Tipps in der DLP-Richtlinie mit diesen Optionen konfiguriert sind, können Sie **Resolve** wählen, um einen richtlinientipp **außer Kraft zu setzen** oder ein falsch positives Ergebnis zu **melden** . 
  
![Optionen für richtlinientipp in backstaging in Excel 2016](media/5b3857ba-907e-456e-ae43-888b594c049c.png)
  
In jedem dieser Office 2016-Desktop Programme können Personen Richtlinien Tipps deaktivieren. Wenn diese Option deaktiviert ist, werden Richtlinien Tipps, die einfache Benachrichtigungen sind, nicht auf der Statusleiste oder der backstagingansicht (auf der Registerkarte **Datei** ) angezeigt. Richtlinien Tipps zum Blockieren und überschreiben werden jedoch weiterhin angezeigt, und Sie erhalten weiterhin die e-Mail-Benachrichtigung. Außerdem wird durch das Deaktivieren von Richtlinien Tipps das Dokument nicht von DLP-Richtlinien ausgenommen, die darauf angewendet wurden. 
  
### <a name="default-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Standardtext für Richtlinien Tipps in Excel 2016, PowerPoint 2016 und Word 2016

Standardmäßig werden in den Richtlinien Tipps in der Statusleiste und der backstagingansicht eines geöffneten Dokuments Text ähnlich der folgenden angezeigt. Der Benachrichtigungstext wird für jede Regel separat konfiguriert, sodass der angezeigte Text unterschiedlich ist, je nachdem, welcher Regel entsprochen wird.

|**Wenn die DLP-Richtlinienregel dies tut...**|**Dann lautet der Standardrichtlinien Tipp this...**|
|:-----|:-----|
|Sendet eine Benachrichtigung, aber keine Außerkraftsetzung  <br/> |Diese Datei steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Weitere Informationen finden Sie im Menü **Datei** .  <br/> |
|Blockiert den Zugriff, sendet eine Benachrichtigung und lässt die Überschreibung zu  <br/> |Diese Datei steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wenn Sie diesen Konflikt nicht beheben, wird der Zugriff auf diese Datei möglicherweise blockiert. Weitere Informationen finden Sie im Menü **Datei** .  <br/> |
|Blockiert den Zugriff und sendet eine Benachrichtigung  <br/> |Diese Datei steht in Konflikt mit einer Richtlinie in Ihrer Organisation. Wenn Sie diesen Konflikt nicht beheben, wird der Zugriff auf diese Datei möglicherweise blockiert. Weitere Informationen finden Sie im Menü **Datei** .  <br/> |
   
### <a name="custom-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Benutzerdefinierter Text für Richtlinien Tipps in Excel 2016, PowerPoint 2016 und Word 2016

Sie können den Text für Richtlinien Tipps separat von der e-Mail-Benachrichtigung anpassen. Anders als benutzerdefinierter Text für e-Mail-Benachrichtigungen (siehe Abschnitt oben) akzeptiert der benutzerdefinierte Text für Richtlinien Tipps weder HTML noch Token. Benutzerdefinierter Text für Richtlinien Tipps ist stattdessen nur-Text mit einem Grenzwert von 256 Zeichen.
  
## <a name="more-information"></a>Weitere Informationen

- [Übersicht über die Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md)
    
- [Erstellen einer DLP-Richtlinie aus einer Vorlage](create-a-dlp-policy-from-a-template.md)
    
- [Erstellen einer DLP-Richtlinie zum Schützen von Dokumenten mit FCI oder anderen Eigenschaften](protect-documents-that-have-fci-or-other-properties.md)
    
- [Inhalt der DLP-Richtlinienvorlagen](what-the-dlp-policy-templates-include.md)
    
- [Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)
    

