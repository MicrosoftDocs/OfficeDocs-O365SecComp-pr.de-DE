---
title: Nachrichtenflussregeln (Transportregeln) in Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/29/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9c2cf227-eff7-48ef-87fb-487186e47363
description: Mithilfe von Nachrichtenfluss Regeln (Transportregeln) können Sie Nachrichten identifizieren und Aktionen ausführen, die in Ihrer Office 365-Organisation durchlaufen werden.
ms.openlocfilehash: 379886788a4fa411d70830c702dd8850e8118b32
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256629"
---
# <a name="mail-flow-rules-transport-rules-in-exchange-online-protection"></a>Nachrichtenflussregeln (Transportregeln) in Exchange Online Protection

Mithilfe von Nachrichtenflussregeln (auch bekannt als Transportregeln) können Sie Nachrichten, die über Ihre Office 365-Organisation fließen, identifizieren und Maßnahmen dafür ergreifen. Nachrichtenflussregeln sind mit den Posteingangsregeln vergleichbar, die in Outlook und Outlook im Web zur Verfügung stehen. Der Hauptunterschied besteht darin, dass Nachrichtenflussregeln Nachrichten während der Übertragung behandeln und nicht nach der Übermittlung der Nachricht an das Postfach. Nachrichtenflussregeln enthalten einen reichhaltigeren Satz an Bedingungen, Ausnahmen und Aktionen, sodass Sie über die Flexibilität verfügen, viele Arten von Nachrichtenrichtlinien zu implementieren.
  
In diesem Artikel werden die Komponenten von Nachrichtenflussregeln und deren Funktionsweise erläutert.
  
Schritte zum Erstellen, Kopieren und Verwalten von Nachrichtenflussregeln finden Sie unter **Manage Transport Rules**. Bei jeder Regel haben Sie die Möglichkeit, sie zu erzwingen, sie zu testen oder sie zu testen und den Absender zu benachrichtigen. Weitere Informationen zum Testen von Optionen finden Sie unter **Test a transport rule** und **Policy Tips**.
  
Eine Zusammenfassung und ausführliche Berichte zu Nachrichten, die Nachrichtenflussregeln entsprechen, finden Sie unter **Verwenden von Berichten zum E-Mail-Schutz in Office 365, um Daten über Schadsoftware, Spam und Regelerkennung anzuzeigen**.
  
Informationen zur Implementierung bestimmter Nachrichtenrichtlinien mithilfe von Nachrichtenflussregeln finden Sie in den folgenden Themen:
  
- [Überprüfen von Nachrichtenanlagen mithilfe von Nachrichtenflussregeln in Office 365](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)
    
- [Einrichten der Verschlüsselung in Office 365 Enterprise](https://support.office.com/article/e86fc991-0161-4f01-9c1c-d25e87733d06)
    
- [Organisationsweite Haftungsausschlüsse, Signaturen, Fußzeilen oder Kopfzeilen für E-Mail-Nachrichten in Office 365](http://technet.microsoft.com/library/29ac61c2-77f1-4071-b14e-8cc64e3e76ba.aspx)
    
- [Verwenden von Nachrichtenflussregeln zum Festlegen der SCL-Bewertung (Spam Confidence Level) in Nachrichten ](../use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)
    
- [Erstellen von organisationsweiten Listen sicherer Absender oder blockierter Absender in Office 365](../create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365.md)
    
- [Reduzieren von Schadsoftwarebedrohungen durch das Blockieren von Dateianlagen in Exchange Online Protection](reducing-malware-threats-through-file-attachment-blocking-in-exchange-online-pro.md)
    
- [Definieren von Regeln zum Verschlüsseln oder Entschlüsseln von E-Mail-Nachrichten](https://go.microsoft.com/fwlink/p/?Linkid=402846)
    
Das folgende Video bietet eine Demonstration der Einrichtung von Nachrichtenfluss Regeln in Exchange Online Protection.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/7cdcd2cb-9382-4065-98e1-81257b32a189?autoplay=false]
  
## <a name="mail-flow-rule-components"></a>Komponenten von Nachrichtenflussregeln

Eine Nachrichtenflussregel besteht aus Bedingungen, Ausnahmen, Aktionen und Eigenschaften:
  
- Anhand von **Bedingungen** werden die Nachrichten ermittelt, auf die Sie die Regel anwenden möchten. Mit einigen Bedingungen werden Nachrichtenkopfzeilenfelder geprüft (z. B. die Felder "An", "Von" oder "Cc"). Andere Bedingungen dienen zum Untersuchen von Nachrichteneigenschaften (z. B. Betreff, Text, Anlagen, Größe oder Klassifizierung der Nachricht). Bei den meisten Bedingungen müssen Sie einen Vergleichsoperator (z. B. Gleich, Ungleich oder Enthält) sowie einen abzugleichenden Wert angeben. Wenn keine Bedingungen oder Ausnahmen angegeben werden, wird die Regel auf alle Nachrichten angewendet. 
    
    Weitere Informationen zu Bedingungen für Nachrichtenfluss Regeln in Exchange Online Protection finden Sie unter [Mail Flow rule conditions and Exceptions (predicates) in Exchange Online.](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions).
    
- **Ausnahmen** kennzeichnen optional die Nachrichten, auf die die Aktionen nicht angewendet werden sollen. In Ausnahmen sind die gleichen Nachrichten-IDs verfügbar wie in Bedingungen. Mit Ausnahmen werden Bedingungen außer Kraft gesetzt, und es wird verhindert, dass die Regelaktionen auf eine Nachricht angewendet werden, und zwar auch dann, wenn die Nachricht allen konfigurierten Bedingungen entspricht. 
    
- **Aktionen** geben an, was mit Nachrichten geschehen soll, die den Bedingungen in der Regel und keiner der Ausnahmen entsprechen. Es stehen zahlreiche Aktionen zur Verfügung, wie Ablehnen, Löschen oder Umleiten von Nachrichten, Hinzufügen weiterer Empfänger, Hinzufügen von Präfixen zum Nachrichtenbetreff oder Einfügen von Haftungsausschlüssen in den Nachrichtentext. 
    
    Weitere Informationen zu Aktionen für Nachrichtenfluss Regeln, die in Exchange Online Protection verfügbar sind, finden Sie unter [Mail Flow rule actions in Exchange Online Protection](http://technet.microsoft.com/library/f8621ecb-a177-4025-9011-a6569999746a.aspx).
    
- **Eigenschaften** geben weitere Regeleinstellungen an, die keine Bedingungen, Ausnahmen oder Aktionen sind. Zum Beispiel, wann die Regel angewendet werden soll, ob die Regel erzwungen oder getestet werden soll und in welchem Zeitraum die Regel aktiv ist. 
    
     Weitere Informationen finden Sie im Abschnitt [Eigenschaften von Nachrichtenflussregeln](mail-flow-rules-transport-rules-0.md#Properties) in diesem Thema. 
    
### <a name="multiple-conditions-exceptions-and-actions"></a>Mehrere Bedingungen, Ausnahmen und Aktionen

Die folgende Tabelle zeigt, wie mehrere Bedingungen, Bedingungswerte, Ausnahmen und Aktionen in einer Regel verarbeitet werden.
  
|**Komponente**|**Logik**|**Kommentare**|
|:-----|:-----|:-----|
|Kommentare  <br/> |UND  <br/> |Eine Nachricht muss allen Bedingungen in der Regel entsprechen. Wenn eine von zwei Bedingungen erfüllt werden muss, verwenden Sie für die Bedingungen separate Regeln. Wenn Sie z. B. Nachrichten mit Anlagen und Nachrichten, die einen bestimmten Text enthalten, die gleiche Haftungsausschlusserklärung hinzufügen möchten, erstellen Sie für jede Bedingung eine Regel. In der Exchange-Verwaltungskonsole können Sie eine Regel ganz einfach kopieren.  <br/> |
|Eine Nachricht muss allen Bedingungen in der Regel entsprechen. Wenn eine bestimmte Bedingung erfüllt werden muss, verwenden Sie für jede Bedingung separate Regeln. Wenn Sie Nachrichten mit Anlagen und Nachrichten mit Inhalt, der einem Muster entspricht, z. B. die gleichen Haftungsausschlusserklärung hinzufügen möchten, erstellen Sie für jede Bedingung eine Regel. Sie können eine Regel problemlos kopieren.  <br/> |ODER  <br/> |Bei einigen Bedingungen können Sie mehr als einen Wert angeben. Die Nachricht muss einem der angegebenen Werte (nicht allen) entsprechen. Beispiel: Wenn eine E-Mail den Betreff Informationen zum Börsenkurs hat und die Bedingung **Betreff enthält eines der folgenden Wörter** für die Übereinstimmung mit den Wörtern Contoso oder Börsenkurs konfiguriert ist, gilt die Bedingung als erfüllt, da der Betreff mindestens einen der angegebenen Werte enthält.  <br/> |
|Bei einigen Bedingungen können Sie mehr als einen Wert angeben. Wenn eine Bedingung die Eingabe mehrerer Werte zulässt, muss die Nachricht einem der Werte entsprechen, der für diese Bedingung angegeben wurde. Beispiel: Wenn eine E-Mail den Betreff Informationen zum Börsenkurs hat und die Bedingung Betreff enthält eines der folgenden Wörter für die Übereinstimmung mit den Wörtern Contoso oder Börsenkurs konfiguriert ist, gilt die Bedingung als erfüllt, da der Betreff mindestens einen der Bedingungswerte enthält.  <br/> |ODER  <br/> |Wenn eine Nachricht einer der Ausnahmen entspricht, werden die Aktionen nicht angewendet. Die Nachricht muss nicht allen Ausnahmen entsprechen.  <br/> |
|Wenn eine Nachricht einer der Ausnahmen entspricht, werden die Aktionen nicht durchgeführt. Die Nachricht muss nicht allen Ausnahmen entsprechen.  <br/> |UND  <br/> |Für Nachrichten, die die Bedingungen einer Regel erfüllen, werden alle in der Regel angegebenen Aktionen ausgeführt. Wenn beispielsweise die Aktionen **Dem Betreff der Nachricht Folgendes voranstellen** und **Empfänger zum Feld "Bcc" hinzufügen** ausgewählt wurden, werden beide Aktionen auf die Nachricht angewendet.  <br/> Bei Nachrichten, die den Bedingungen einer Regel entsprechen, werden alle in der Regel angegebenen Aktionen durchgeführt. Wenn beispielsweise die Aktionen "Dem Betreff der Nachricht Folgendes voranstellen" und "Empfänger zum Feld "Bcc" hinzufügen" ausgewählt wurden, werden beide Aktionen auf die Nachricht angewendet. In der Nachricht wird die angegebene Zeichenfolge dem Nachrichtenbetreff vorangestellt, und die angegebenen Empfänger werden als Bcc-Empfänger hinzugefügt.<br/> Sie können für eine Regel auch eine Aktion festlegen, sodass bei Anwendung dieser Regel nachfolgende Regeln nicht auf die Nachricht angewendet werden.  <br/> |
   
### <a name="mail-flow-rule-properties"></a>Eigenschaften von Nachrichtenflussregeln
<a name="Properties"> </a>

Die folgende Tabelle beschreibt die Regeleigenschaften, die in Nachrichtenflussregeln zur Verfügung stehen.
  
|**Eigenschaftenname in der Exchange-Verwaltungskonsole**|**Parametername in PowerShell**|**Beschreibung**|
|:-----|:-----|:-----|
|**Priority** <br/> | _Priority_ <br/> |Gibt die Reihenfolge an, in der die Regeln auf Nachrichten angewendet werden. Die Standardpriorität basiert auf dem Erstellungsdatum der Regel (ältere Regeln haben eine höhere Priorität als neuere Regeln, und Regeln mit höherer Priorität werden vor Regeln mit niedrigerer Priorität verarbeitet).    <br/> Sie ändern die Regelpriorität in der Exchange-Verwaltungskonsole, indem Sie die Regel in der Liste der Regeln nach oben oder unten verschieben. In der PowerShell legen Sie die Prioritätsnummer fest (0 ist die höchste Priorität).    <br/> Wenn Sie z. B. eine Regel verwenden, um Nachrichten abzulehnen, die eine Kreditkartennummer enthalten, und eine andere Regel, die eine Genehmigung erfordert, sollte die Ablehnungsregel zuerst angewendet werden, und es sollten keine anderen Regeln mehr angewendet werden.      |
|**Mode** <br/> | _Mode_ <br/> |Sie können angeben, ob die Regel sofort mit der Verarbeitung von Nachrichten beginnen soll oder ob Sie Regeln ohne Auswirkungen auf die Übermittlung der Nachricht (mit oder ohne Verhinderung von Datenverlust oder DLP-Richtlinientipps) testen möchten.  <br/> Richtlinientipps zeigen dem Ersteller einer Nachricht in Outlook oder Outlook im Web einen Hinweis mit Informationen über mögliche Richtlinienverletzungen an. Weitere Informationen finden Sie unter **Policy Tips**.  <br/> Weitere Informationen zu den Modi finden Sie unter **Test a mail flow rule**.  <br/> |
|**Diese Regel an folgendem Datum aktivieren** <br/> **Diese Regel an folgendem Datum deaktivieren** <br/> | _ActivationDate_ <br/>  _Ablaufdatum_ <br/> |Gibt den Datumsbereich an, in dem die Regel aktiv ist.  <br/> |
|Kontrollkästchen **Ein** aktiviert oder nicht aktiviert  <br/> |Neue Regeln: Parameter  _Enabled_ im Cmdlet **New-TransportRule**.  <br/> Vorhandene Regeln: Verwenden Sie die Cmdlets **Enable-TransportRule** oder **Disable-TransportRule**.  <br/> Der Wert wird in der **State** -Eigenschaft der Regel angezeigt.  <br/> |Sie können eine deaktivierte Regel erstellen und diese aktivieren, wenn Sie sie testen möchten. Alternativ können Sie eine Regel deaktivieren, ohne sie zu löschen, um die Einstellungen beizubehalten.  <br/> |
|**Nachricht zurückstellen, wenn die Regelverarbeitung nicht abgeschlossen wird** <br/> | _RuleErrorAction_ <br/> |Sie können angeben, wie die Nachricht behandelt werden soll, wenn die Regelverarbeitung nicht abgeschlossen werden kann. Standardmäßig wird die Regel ignoriert, aber Sie können angeben, dass die Nachricht erneut zur Verarbeitung übermittelt werden soll.  <br/> |
|**Absenderadresse in Nachricht vergleichen** <br/> | _SenderAddressLocation_ <br/> |Wenn die Regel Bedingungen oder Ausnahmen verwendet, die die E-Mail-Adresse des Absenders überprüfen, finden Sie den Wert in der Nachrichtenkopfzeile und/oder im Nachrichtenumschlag.  <br/> |
|**Verarbeiten weiterer Regeln beenden** <br/> | _SenderAddressLocation_ <br/> |Dies ist eine Aktion für die Regel, aber sie sieht in der Exchange-Verwaltungskonsole wie eine Eigenschaft aus. Sie können auswählen, dass keine weiteren Regeln auf eine Nachricht angewendet werden, nachdem eine Nachricht durch eine Regel verarbeitet wurde.  <br/> |
|**Comments** <br/> | _Comments_ <br/> |Sie können beschreibende Kommentare zur Regel eingeben.  <br/> |
   
## <a name="how-mail-flow-rules-are-applied-to-messages"></a>Wie Nachrichtenflussregeln auf Nachrichten angewendet werden

Alle Nachrichten, die Ihre Organisation durchlaufen, werden anhand der aktivierten Nachrichtenflussregeln in Ihrer Organisation ausgewertet. Regeln werden in der im EAC auf der Seite **Nachrichtenfluss** \> **Regeln** angegebenen Reihenfolge oder basierend auf dem entsprechenden Wert des Parameters  _Priority_ in PowerShell verarbeitet. 
  
Jede Regel bietet außerdem die Möglichkeit, die Verarbeitung weiterer Regeln anzuhalten, wenn die Regel erfüllt wird. Diese Einstellung ist für Nachrichten wichtig, die die Bedingungen in mehreren E-Mail-Flussregeln erfüllen. (Welche Regel soll auf die die Nachricht angewendet werden? Alle? Nur eine?)
  
### <a name="differences-in-processing-based-on-message-type"></a>Unterschiede in der Verarbeitung basierend auf dem Nachrichtentyp

Es gibt verschiedene Nachrichtentypen, die eine Organisation durchlaufen. Die folgende Tabelle zeigt, welche Nachrichtentypen von Nachrichtenflussregeln verarbeitet werden können.
  
****

|**Nachrichtentyp**|**Kann eine Regel angewendet werden?**|
|:-----|:-----|
|**Gewöhnliche Nachrichten** Nachrichten, die einen einteiligen RTF-, HTML- oder unformatierten Nachrichtentext bzw. einen mehrteiligen Nachrichtentext oder einen alternativen Satz von Nachrichtentexten enthalten.      <br/> |Ja  <br/> |
|**Office 365-Nachrichtenverschlüsselung ** Nachrichten, die von Office 365-Nachrichtenverschlüsselung in Office 365 verschlüsselt werden. Weitere Informationen finden Sie unter [Verschlüsselung in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=392525).  <br/> |Regeln können immer auf Umschlagkopfzeilen zugreifen und Nachrichten auf Grundlage von Bedingungen verarbeiten, mit denen diese Kopfzeilen untersucht werden.  <br/> Damit eine Regel den Inhalt einer verschlüsselten Nachricht überprüft oder ändert, müssen Sie überprüfen, ob die Transportentschlüsselung aktiviert ist („Obligatorisch" oder „Optional"; der Standardwert ist „Optional"). Weitere Informationen finden Sie unter [Aktivieren oder Deaktivieren der Transportentschlüsselung](https://go.microsoft.com/fwlink/p/?linkid=848060).  <br/> Sie können auch eine Regel erstellen, die verschlüsselte Nachrichten automatisch entschlüsselt. Weitere Informationen finden Sie unter [Definieren von Regeln zum Ver- oder Entschlüsseln von E-Mail-Nachrichten](https://go.microsoft.com/fwlink/p/?Linkid=402846).  <br/> |
|**S/MIME-Verschlüsselte Nachrichten** <br/> |Regeln können nur auf Umschlagkopfzeilen zugreifen und Nachrichten auf Grundlage von Bedingungen verarbeiten, mit denen diese Kopfzeilen untersucht werden.  <br/> Regeln mit Bedingungen, die eine Untersuchung des Nachrichteninhalts erfordern, oder Aktionen, die den Inhalt der Nachricht ändern, können nicht verarbeitet werden.  <br/> |
|**RMS-geschützte Nachrichten** Nachrichten, auf die eine Active Directory-Rechteverwaltungsdienste (Active Directory Rights Management Services, AD RMS) (AD RMS)- oder Azure-Rechteverwaltung (RMS)-Richtlinie angewendet wurde.  <br/> |Regeln können immer auf Umschlagkopfzeilen zugreifen und Nachrichten auf Grundlage von Bedingungen verarbeiten, mit denen diese Kopfzeilen untersucht werden.  <br/> Damit eine Regel den Inhalt einer RMS-geschützten Nachricht überprüft oder ändert, müssen Sie überprüfen, ob die Transportentschlüsselung aktiviert ist („Obligatorisch" oder „Optional"; der Standardwert ist „Optional"). Weitere Informationen finden Sie unter [Aktivieren oder Deaktivieren der Transportentschlüsselung](https://go.microsoft.com/fwlink/p/?linkid=848060).  <br/> |
|**Transparent signierte Nachrichten** Nachrichten, die signiert, aber nicht verschlüsselt wurden.  <br/> |Ja  <br/> |
|**UM-Nachrichten** Nachrichten, die vom Unified Messaging-Dienst erstellt oder verarbeitet wurden, z. B. Voicemail, Fax, Benachrichtigungen über verpasste Anrufe und mit Microsoft Outlook Voice Access erstellte oder weitergeleitete Nachrichten.      <br/> |Ja  <br/> |
|**Anonyme Nachrichten** Nachrichten, die von anonymen Absendern gesendet wurden.  <br/> |Ja  <br/> |
|**Lesebestätigungsberichte** Berichte, die als Reaktion auf Lesebestätigungsanforderungen von Absendern generiert werden. Lesebestätigungsberichte weisen die Nachrichtenklasse  `IPM.Note*.MdnRead` oder  `IPM.Note*.MdnNotRead` auf.  <br/> |Ja  <br/> |
   
## <a name="what-else-should-i-know"></a>Was muss ich sonst noch wissen?

- Der **Version** -oder **RuleVersion** -Eigenschaftswert für eine Regel ist in Exchange Online Protection nicht wichtig. 
    
- Nach dem Erstellen oder Ändern einer E-Mail-Flussregel kann es bis zu 30 Minuten dauern, bis die neue oder aktualisierte Regel auf Nachrichten angewendet wird.
    
## <a name="for-more-information"></a>Weitere Informationen
  
[Überprüfen von Nachrichtenanlagen in Exchange Online mithilfe von Nachrichtenfluss Regeln](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)
  
[E-Mail-Verschlüsselung in Office 365](https://support.office.com/article/c0d87cbe-6d65-4c03-88ad-5216ea5564e8)
  
[Journal-, Transport- und Posteingangsregelgrenzen](https://go.microsoft.com/fwlink/p/?LinkId=324584)
