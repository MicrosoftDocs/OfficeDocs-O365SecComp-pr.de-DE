---
title: Häufig gestellte Fragen zur Dienstverschlüsselung mit Kundenschlüssel für Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 41ae293a-bd5c-4083-acd8-e1a2b4329da6
description: Zusätzlich zu der Basisrichtlinie, die durch BitLocker und Distributed Key Manager (DKM) aktiviert ist, bietet Office 365 eine zusätzliche Verschlüsselungsschicht auf Anwendungsebene für Kunden Inhalte in Office 365, einschließlich Daten aus Exchange Online, Skype for Business, SharePoint Online und OneDrive for Business. Dies wird als Dienst Verschlüsselung bezeichnet.
ms.openlocfilehash: 5e1acca69ccdd8acb986acb4d7a302d4ca3fbe8a
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2019
ms.locfileid: "30936765"
---
# <a name="service-encryption-with-customer-key-for-office-365-faq"></a>Häufig gestellte Fragen zur Dienstverschlüsselung mit Kundenschlüssel für Office 365

Zusätzlich zu der Basisrichtlinie, die durch BitLocker und Distributed Key Manager (DKM) aktiviert ist, bietet Office 365 eine zusätzliche Verschlüsselungsschicht auf Anwendungsebene für Kunden Inhalte in Office 365, einschließlich Daten aus Exchange Online, Skype for Business, SharePoint Online und OneDrive for Business. Dies wird als Dienst Verschlüsselung bezeichnet.
  
Der Kundenschlüssel basiert auf der Dienst Verschlüsselung und ermöglicht Ihnen das Bereitstellen und Steuern von Schlüsseln, die zum Verschlüsseln von Daten in Rest in Office 365 verwendet werden, wie im Abschnitt [Online Services Terms (Ost)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)beschrieben. Mit dem Kundenschlüssel können Sie Auflagen erfüllen, da Sie die Verschlüsselungsschlüssel steuern, mit denen Office 365 die Daten entschlüsselt.
  
Um Feedback zum Kundenschlüssel, einschließlich der Dokumentation, zu geben, senden Sie Ihre Ideen, Vorschläge und Perspektiven an customerkeyfeedback@microsoft.com.
  
## <a name="what-is-service-encryption-with-customer-key"></a>Was ist Dienst Verschlüsselung mit Kundenschlüssel?

Kundenschlüssel verbessert die Fähigkeit Ihrer Organisation, die Anforderungen der Compliance-Anforderungen zu erfüllen, die wichtige Vorkehrungen mit dem Cloud-Dienstanbieter festlegen. Mit dem Kundenschlüssel können Sie die Verschlüsselungsschlüssel für Ihre Office 365-Daten auf Anwendungsebene bereitstellen und steuern. Daher können Sie die Steuerelemente ausüben und die Schlüssel Ihrer Organisation widerrufen, wenn Sie den Dienst beenden möchten. Durch das Widerrufen der Schlüssel sind die Daten für den Dienst unlesbar. Die Schlüssel Sperrung ist der erste Schritt auf dem Weg zum Löschen von Daten.

## <a name="what-office-365-data-at-rest-is-covered-by-customer-key"></a>Welche Office 365-Daten im Ruhezustand werden vom Kundenschlüssel abgedeckt?
<a name="WhatDataIsCoveredbyCustomerKey"> </a>

Der SharePoint Online-Websiteinhalt und die auf dieser Website gespeicherten Dateien und Dateien, die in OneDrive for Business hochgeladen werden, werden behandelt. Exchange Online-Postfachinhalte (e-Mail-Text, Kalendereinträge und Inhalt von e-Mail-Anlagen) werden behandelt. Text Unterhaltungen von Skype for Business werden behandelt, aber Skype-Besprechungs Übertragungs Aufzeichnungen und Skype-Besprechungsinhalte werden nicht behandelt. Skype Meeting-Broadcast-und Skype-Besprechungsinhalte werden zusammen mit allen anderen Inhalten in Office 365 verschlüsselt, aber wir bieten derzeit keine Kunden Steuerung der Verschlüsselungsschlüssel.
  
## <a name="what-is-the-difference-between-customer-key-and-bring-your-own-key-byok-with-azure-information-protection-for-exchange-online"></a>Was ist der Unterschied zwischen dem Kundenschlüssel und dem eigenen Schlüssel (BYOK) mit Azure Information Protection für Exchange Online?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Beide Optionen ermöglichen es Ihnen, eigene Verschlüsselungsschlüssel bereitzustellen und zu steuern. Dienst Verschlüsselung mit Kundenschlüssel verschlüsselt jedoch Ihre Daten im Ruhezustand, der sich in Office 365-Servern befindet, während BYOK mit Azure Information Protection für Exchange Online Ihre Daten in Transit verschlüsselt und persistente Online-und Offlinedienste bereitstellt. Schutz für e-Mail-Nachrichten und Anlagen für Office 365. Kundenschlüssel und BYOK mit Azure Information Protection für Exchange Online sind komplementär, und unabhängig davon, ob Sie Microsoft-Dienst verwaltete Schlüssel oder eigene Schlüssel verwenden, die Verschlüsselung Ihrer Daten-at-Rest-und in-Transit können zusätzlichen Schutz von böswillige Angriffe.
  
BYOK mit Azure Information Protection für Exchange Online finden Sie in den Nachrichten Verschlüsselungsfunktionen von Office 365.
  
## <a name="does-office-365-message-encryption-and-bring-your-own-key-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Ist Office 365-Nachrichtenverschlüsselung und bringen Sie Ihren eigenen Schlüssel mit Azure Information Protection Ändern des Ansatzes von Microsoft an Drittanbieter-Datenanforderungen wie Vorladungen?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. Office 365 Nachrichtenverschlüsselung und die Option zum Bereitstellen und Steuern ihrer eigenen Verschlüsselungsschlüssel mit bringen Sie Ihren eigenen Schlüssel (BYOK) für Azure Information Protection (AIP) wurde nicht entwickelt, um auf Strafverfolgungsbehörden Vorladungen zu reagieren. Die Nachrichtenverschlüsselung von Office 365 mit BYOK für AIP wurde für Kunden mit Compliance-Orientierung entwickelt, die ihre internen oder externen Compliance-Verpflichtungen erfüllen müssen. Microsoft übernimmt Drittanbieter Anforderungen für Kundendaten sehr ernst. Als Cloud-Dienstanbieter befürworten wir stets den Schutz von Kundendaten. Für den Fall, dass eine Vorladung vorliegt, versuchen wir immer, den dritten an den Kunden zu leiten, um die Informationen zu erhalten. (Lesen Sie den Blog zu Brad Smith: [Schützen von Kundendaten vor der Regierung Snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Wir veröffentlichen in regelmäßigen Abständen detaillierte Informationen zu der Anforderung, die wir [hier](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data)erhalten.
  
Weitere Informationen finden Sie im [Microsoft Trust Center](https://www.microsoft.com/en-us/trustcenter/default.aspx) in Bezug auf Datenanforderungen von Drittanbietern und "Offenlegung von Kundendaten" in den [Online-Dienstbedingungen (Ost) ](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).
  
## <a name="does-service-encryption-with-customer-key-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Ändert die Dienst Verschlüsselung mit Kundenschlüssel den Ansatz von Microsoft zu Drittanbieter-Datenanforderungen wie Vorladungen?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. Kundenschlüssel wurde nicht entwickelt, um auf Strafverfolgungsbehörden Vorladungen zu reagieren. Sie wurde für regulierte Kunden entwickelt, um Ihre internen oder externen Compliance-Verpflichtungen zu erfüllen. Microsoft übernimmt Drittanbieter Anforderungen für Kundendaten sehr ernst. Als Cloud-Dienstanbieter befürworten wir stets den Schutz von Kundendaten. Für den Fall, dass eine Vorladung vorliegt, versuchen wir immer, den dritten an den Kunden zu leiten, um die Informationen zu erhalten. (Lesen Sie den Blog zu Brad Smith: [Schützen von Kundendaten vor der Regierung Snooping](http://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Wir veröffentlichen in regelmäßigen Abständen detaillierte Informationen zu der Anforderung, die wir [hier](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data)erhalten.
  
Weitere Informationen finden Sie im [Microsoft Trust Center](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data) in Bezug auf Datenanforderungen von Drittanbietern und "Offenlegung von Kundendaten" in den [Online-Dienstbedingungen (Ost)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx) . 
  
## <a name="is-fasttrack-support-available-for-implementing-customer-key"></a>Ist die Unterstützung für die Implementierung des Kunden Schlüssels verfügbar?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. "Nur" wird zum Erfassen von Mandanten-und Dienstkonfigurationsinformationen verwendet, die für die Registrierung für den Kundenschlüssel erforderlich sind. Die Kundenschlüssel Angebote werden über die Kurzinfo-Veröffentlichung veröffentlicht, sodass Kunden und Partner diese erforderlichen Informationen bequem mit derselben Methode übermitteln können, um die von Kunden im Angebot bereitgestellten Daten zu vereinfachen.
  
Wenn Sie über die Dokumentation hinaus weitere Unterstützung benötigen, wenden Sie sich an Microsoft Consulting Services (MCS), Premier Field Engineering (PFE) oder einen Microsoft-Partner zur Unterstützung.
  
## <a name="if-my-keys-are-destroyed-how-can-i-recover"></a>Wie kann ich wiederhergestellt werden, wenn meine Schlüssel zerstört werden?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Der Verfügbarkeits Schlüssel bietet Ihnen die Möglichkeit, nach dem unerwarteten Verlust von Stamm Schlüsseln, die Sie verwalten, wiederherzustellen. Wenn Sie Ihre Stammschlüssel verlieren, wenden Sie sich an den Microsoft-Support, und Microsoft unterstützt Sie bei der Aktivierung des Verfügbarkeits Schlüssels. Sie verwenden den Verfügbarkeits Schlüssel, um zu einer neuen Daten VerschlüsselungsRichtlinie mit neuen Schlüsseln zu migrieren, die von Ihnen bereitgestellt werden. 
  
## <a name="what-is-the-availability-key"></a>Was ist der Verfügbarkeits Schlüssel?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Der Verfügbarkeits Schlüssel ist ein Stammschlüssel, der beim Erstellen einer Daten Verschlüsselungsrichtlinie bereitgestellt wird. Der Verfügbarkeits Schlüssel wird in Office 365 gespeichert und geschützt und ähnelt funktionell den zwei Stamm Schlüsseln, die von Ihnen zur Verwendung mit der Dienst Verschlüsselung mit dem Kundenschlüssel bereitgestellt werden. Im Gegensatz zu den Schlüsseln, die Sie in Azure Key Vault bereitstellen und verwalten, können Sie nicht direkt auf den Verfügbarkeits Schlüssel zugreifen. Der Speicher und die Steuerung des Verfügbarkeits Schlüssels unterscheiden sich bewusst von den Azure Key Vault-Schlüsseln aus drei Gründen: Erstens bietet der Verfügbarkeits Schlüssel eine hohe Verfügbarkeit für den Fall, dass Office 365-Dienste nicht in der Lage sind, die Schlüssel zu erreichen, die in Azure Key gehostet werden. Tresor Zweitens stellt der Verfügbarkeits Schlüssel für den Fall, dass beide Azure Key Vault-Schlüssel verloren gehen, eine "Glasbruch-Funktion" bereit. und drittens bietet die Trennung von logischen Steuerelementen eine Tiefenverteidigung und schützt vor dem Verlust aller Schlüssel aus einem einzelnen Angriff oder einem Ausfall. Wenn Sie die Verantwortung für den Schutz der Schlüssel Teilen und gleichzeitig eine Vielzahl von Schutz-und Prozessverfahren für die Schlüsselverwaltung verwenden, wird das Risiko, dass alle Schlüssel (und damit Ihre Daten) verloren gehen oder zerstört werden, verringert. Microsoft bietet Ihnen alleinige Autorität über die Zerstörung des Verfügbarkeits Schlüssels. Im Entwurf hat niemand bei Microsoft Zugriff auf den Verfügbarkeits Schlüssel, auf den nur über den Office 365-Dienstcode zugegriffen werden kann.
  
## <a name="how-many-data-encryption-policies-deps-can-i-create"></a>Wie viele Daten Verschlüsselungsrichtlinien (DEPs) kann ich erstellen?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype for Business:** Sie können bis zu 50 DEPs erstellen. 
  
 **SharePoint Online und OneDrive for Business:** Eine DEP betrifft Daten an einem geografischen Standort. Wenn Sie das Multi-Geo-Feature von Office 365 verwenden, können Sie eine DEP pro Geo erstellen. Wenn Sie nicht Multi-Geo verwenden, können Sie eine datenAUSFÜHRUNGSverHINDERung erstellen.
  
## <a name="can-i-assign-a-data-encryption-policy-before-migrating-a-mailbox-to-the-cloud"></a>Kann ich eine Daten Verschlüsselungsrichtlinie zuweisen, bevor ein Postfach zur Cloud migriert wird?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Ja. Sie können das Windows PowerShell-Cmdlet Set-MailUser verwenden, um dem Benutzer eine Daten Verschlüsselungsrichtlinie zuzuweisen, bevor das Postfach zu Office 365 migriert wird. Wenn Sie dies tun, wird der Inhalt des Postfachs mithilfe der zugewiesenen DEP verschlüsselt, wenn der Inhalt migriert wird. Dies kann effizienter sein, als das Zuweisen einer datenAUSFÜHRUNGSverHINDERung nach der Migration des Postfachs und das anschließende warten auf die Verschlüsselung, die Stunden oder sogar Tage dauern kann. 
  
## <a name="how-do-i-verify-that-encryption-with-customer-key-is-activated-and-office-365-has-finished-encrypting-with-customer-key"></a>Wie kann ich überprüfen, ob die Verschlüsselung mit dem Kundenschlüssel aktiviert ist und dass Office 365 die Verschlüsselung mit dem Kundenschlüssel abgeschlossen hat?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype for Business:** Sie können [mithilfe der Remote-PowerShell eine Verbindung mit Exchange Online herstellen](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) und dann das Cmdlet **[Get-MailboxStatistics]** für jedes Postfach verwenden, das Sie überprüfen möchten. In der Ausgabe des Cmdlets Get-MailboxStatistics gibt die __ IsEncrypted-Eigenschaft den Wert **true** zurück, wenn das Postfach verschlüsselt ist, und den Wert **false** , falls dies nicht der Fall ist. Wenn das Postfach verschlüsselt ist, ist der für die _DataEncryptionPolicyID_ -Eigenschaft zurückgegebene Wert die GUID der DEP, mit der das Postfach verschlüsselt wird. Weitere Informationen zum Ausführen dieses Cmdlets finden Sie unter [Get-MailboxStatistics](https://technet.microsoft.com/en-us/library/bb124612%28v=exchg.160%29.aspx) und Verwenden von PowerShell mit Exchange Online. 
  
Wenn die Postfächer nach dem Warten von 72 Stunden nach dem Zuweisen der DEP nicht verschlüsselt sind, initiieren Sie eine Postfachverschiebung. Stellen Sie hierzu [mithilfe der Remote-PowerShell eine Verbindung mit Exchange Online her](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , und verwenden Sie dann das Cmdlet New-MoveRequest, und geben Sie den Alias des Postfachs wie folgt an: 
  
```
New-MoveRequest <alias>
```

 **SharePoint Online und OneDrive for Business:** Sie können [eine Verbindung mit SharePoint Online PowerShell herstellen](https://technet.microsoft.com/en-us/library/fp161372.aspx)und dann mit dem Cmdlet **[get-SPODataEncryptionPolicy]** den Status Ihres Mandanten überprüfen. Die * * _State_* *-Eigenschaft gibt den Wert **registriert** zurück, wenn die Kundenschlüssel Verschlüsselung aktiviert ist und alle Dateien in allen Websites verschlüsselt wurden. Wenn die Verschlüsselung noch läuft, stellt dieses Cmdlet Informationen dazu bereit, wie viel Prozent der Websites abgeschlossen ist. 
  
## <a name="if-i-want-to-switch-to-a-different-set-of-keys-how-long-does-it-take-for-the-new-set-of-keys-to-protect-my-data"></a>Wie lange dauert es, bis der neue Schlüsselsatz meine Daten schützt, wenn ich zu einem anderen Schlüsselsatz wechseln möchte?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype for Business:** Es kann bis zu 72 Stunden dauern, bis ein Postfach gemäß einer neuen Daten VerschlüsselungsRichtlinie (Data Encryption Policy, DEP) aus der Zeit geschützt wird, in der die neue DEP dem Postfach zugewiesen wurde. 
  
 **SharePoint Online und OneDrive for Business:** Es kann bis zu vier Stunden dauern, bis der gesamte Mandant neu verschlüsselt wurde, nachdem ein neuer Schlüssel zugewiesen wurde. 
  
## <a name="is-my-existing-data-stored-without-encryption-at-any-time-while-it-is-decrypted-or-encrypted-with-customer-key"></a>Werden meine vorhandenen Daten jederzeit ohne Verschlüsselung gespeichert, während Sie mit dem Kundenschlüssel entschlüsselt oder verschlüsselt werden?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. Ihre Daten werden stets im Office 365-Dienst mit BitLocker und DKM verschlüsselt. Weitere Informationen finden Sie unter "Informationen zu Sicherheit, Datenschutz und Kompatibilität für Office 365" und zur [Sicherung Ihrer e-Mail-Geheimnisse durch Exchange Online](https://support.office.com/article/989BA10C-F73F-4EFB-AD1B-AF3322E5F376).
  
## <a name="if-i-no-longer-want-to-use-customer-managed-encryption-keys-can-i-switch-to-microsoft-managed-keys"></a>Kann ich zu Microsoft-Managed Keys wechseln, wenn ich nicht mehr Kunden verwaltete Verschlüsselungsschlüssel verwenden möchte?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype for Business:** Noch nicht. Dies wird unterstützt, sobald die Dienst Verschlüsselung in Office 365 mit von Microsoft verwalteten Schlüsseln allgemein ausgeführt wird. Wir gehen davon aus, dass dies im Dienst ausgeführt wird, nachdem wir die Dienst Verschlüsselung mit dem Kundenschlüssel veröffentlicht haben. 
  
 **SharePoint Online und OneDrive for Business:** Ja. Sie können festlegen, dass die Verwendung von Microsoft-verwalteten Schlüsseln für jede Geo (bei Verwendung des Multi-Geo-Features) oder für alle Daten, die sich in einem einzelnen Geo befinden, separat wiederhergestellt werden soll. 
  
## <a name="if-i-lose-my-keys-how-long-does-it-take-to-recover-service-availability-using-the-recovery-key"></a>Wenn ich meine Schlüssel verliere, wie lange dauert es, bis die Dienstverfügbarkeit mithilfe des Wiederherstellungsschlüssels wiederhergestellt wird?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype for Business:** Sobald Sie den Verfügbarkeits Schlüssel verwendet haben, können Sie innerhalb von Minuten auf die Postfächer zugreifen. 
  
 **SharePoint Online und OneDrive for Business:** Dieser Vorgang ist proportional zur Anzahl der Websites, die Sie haben. Sobald Sie Microsoft zur Verwendung des Verfügbarkeits Schlüssels aufgerufen haben, sind Sie innerhalb von etwa vier Stunden vollständig online. 
  
## <a name="how-is-the-availability-key-used-with-exchange-online"></a>Wie wird der Verfügbarkeits Schlüssel mit Exchange Online verwendet?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Es gibt drei Möglichkeiten, den Verfügbarkeits Schlüssel mit Exchange Online zu verwenden:
  
- Dienstverfügbarkeit-für den Fall, dass Azure Key Vault-Schlüssel nicht erreichbar sind.
    
- Vom Office 365-Dienstcode initiierte Aktionen wie Such Indexerstellung oder Postfachverschiebungen.
    
- Wiederherstellen von Schlüssel Verlusten, beispielsweise dem Verlust von beiden Azure Key Vault-Schlüsseln, die einer einzelnen DEP zugeordnet sind.
    
 **Verwenden des Verfügbarkeits Schlüssels für die Dienstverfügbarkeit im Ereignis Azure Key Vault-Schlüssel sind nicht erreichbar.**
  
Office 365 verwendet den Verfügbarkeits Schlüssel für die Dienstverfügbarkeit und die Wiederherstellung von einem fehlerhaften Kundenschlüssel Status für Exchange Online. Es gibt eine Hierarchie von Schlüsseln, die vom Kundenschlüssel verwendet werden. Diese Hierarchie wird in der folgenden Abbildung dargestellt.
  
![](media/a760156b-737f-469a-80ab-c28b7a8b9160.png)
  
Wenn beide Azure Key Vault-Schlüssel einer einzelnen Daten VerschlüsselungsRichtlinie nicht verfügbar sind, kann Office 365 den Verfügbarkeits Schlüssel verwenden, um zu einer neuen DEP zu wechseln. Office 365 bestimmt, ob der Verfügbarkeits Schlüssel für die Dienstverfügbarkeit unterschiedlich ist, je nachdem, ob eine vom Benutzer initiierte Aktivität, wenn beispielsweise ein Benutzer e-Mails an den Outlook-Client herunterlädt, oder eine vom System initiierte Aktivität wie die Indizierung Postfachinhalte oder für eDiscovery-suchen lösten den Prozess aus.
  
Office 365 folgt diesem Prozess als Reaktion auf vom Benutzer initiierte Aktionen, um zu bestimmen, ob der Verfügbarkeits Schlüssel für Benutzerpostfächer verwendet werden soll:
  
1. Office 365 liest die DEP, der das Postfach zugewiesen ist, um den Speicherort der beiden Kundenschlüssel in Azure Key Vault zu bestimmen.
    
2. Office 365 wählt nach dem Zufallsprinzip einen der beiden Kundenschlüssel aus der DEP aus und sendet eine Anforderung an Azure Key Vault, um den DEP-Schlüssel mithilfe des Kunden Schlüssels zu entpacken.
    
3. Wenn die Anforderung zum Auspacken des DEP-Schlüssels mithilfe des Customer-Schlüssels fehlschlägt und einen Fehler zurückgibt, sendet Office 365 eine zweite Anforderung an Azure Key Vault und weist dieses Mal an, dass der Alternative (zweite) Kundenschlüssel verwendet werden soll.
    
4. Wenn die zweite Anforderung zum Aufziehen des DEP-Schlüssels mithilfe des Kunden Schlüssels fehlschlägt und einen Fehler zurückgibt, untersucht Office 365 die Ergebnisse beider Anforderungen:
    
  - Wenn die Prüfung feststellt, dass die Fehler keine explizite Aktion durch eine Kundenidentität widerspiegeln, verwendet Office 365 den Verfügbarkeits Schlüssel, um den DEP-Schlüssel zu entschlüsseln. Der DEP-Schlüssel wird dann verwendet, um den postfachschlüssel zu entschlüsseln und die Benutzeranforderung abzuschließen.
    
    In diesem Fall kann Azure Key Vault aus irgendeinem Grund entweder nicht Antworten oder nicht erreichbar sein. Office 365 kann nicht feststellen, ob der Kunde den Zugriff auf die Schlüssel absichtlich aufgehoben hat.
    
  - Wenn die Prüfung darauf hinweist, dass eine absichtliche Aktion ausgeführt wurde, damit die Kundenschlüssel nicht verfügbar sind, wird der Verfügbarkeits Schlüssel nicht verwendet, die Benutzeranforderung schlägt fehl, und der Benutzer erhält eine Fehlermeldung, wie beispielsweise einen Anmeldefehler.
    
    In diesem Fall wird der Kunde darauf hingewiesen, dass der Dienst betroffen ist und dass der Zustand des Kunden Schlüssels fehlerhaft ist. Wenn ein Kunde beispielsweise eine einzelne DEP für alle Postfächer in der Organisation verwendet, kann der Kunde einen weit verbreiteten Misserfolg haben, wenn Benutzer nicht auf ihre Postfächer zugreifen können. Dadurch wird sichergestellt, dass bei fehlerhaften Kunden Schlüsseln der Kunde darauf aufmerksam gemacht wird, dass die Situation korrigiert und der Dienst in einem einwandfreien Zustand wiederhergestellt werden muss.
    
 **Verwenden des Verfügbarkeits Schlüssels für Aktionen, die von Office 365-Dienstcode initiiert wurden.**
  
Der Office 365-Dienstcode hat immer ein gültiges Anmeldetoken und kann nicht blockiert werden. Daher kann es, bis der Verfügbarkeits Schlüssel gelöscht wurde, für Aktionen verwendet werden, die von einem Office 365-Dienstcode oder von einem internen an, wie beispielsweise Such Indexerstellung oder Postfächern, initiiert werden.
  
 **Verwenden des Verfügbarkeits Schlüssels zur Wiederherstellung nach Schlüsselverlust.**
  
Sie können den Verfügbarkeits Schlüssel verwenden, um nach dem Verlust der beiden Azure Key Vault-Schlüssel zu erholen, die derselben DEP zugeordnet sind, wie in der Antwort auf den FAQ-Eintrag beschrieben, "wenn meine Schlüssel zerstört werden, wie kann ich wiederherstellen?".
  
## <a name="how-is-the-availability-key-used-with-sharepoint-online-and-onedrive-for-business"></a>Wie wird der Verfügbarkeits Schlüssel mit SharePoint Online und OneDrive for Business verwendet?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Die SharePoint Online-und OneDrive for Business-Architektur und-Implementierung für Kundenschlüssel-und Verfügbarkeits Schlüssel unterscheiden sich von Exchange Online und Skype for Business.
  
Wenn ein Kunde zu vom Kunden verwalteten Schlüssel wechselt, erstellt Office 365 einen mandantenspezifischen zwischen Schlüssel (TIK). Office 365 verschlüsselt das TIK zweimal, einmal mit jedem Kundenschlüssel, und speichert die beiden verschlüsselten Versionen von TIK. Nur die verschlüsselten Versionen des TIK werden gespeichert, und ein TIK kann nur mit den Kunden Schlüsseln entschlüsselt werden. Der TIK wird dann zum Verschlüsseln von Website Schlüsseln verwendet, die dann zum Verschlüsseln von BLOB-Schlüsseln verwendet werden. Die BLOBs selbst werden verschlüsselt und im Microsoft Azure BLOB Storage-Dienst gespeichert.
  
Office 365 folgt diesem Prozess für den Zugriff auf ein BLOB mit Kundendatei Daten:
  
1. EntSchlüsseln Sie die TIK mithilfe des Kunden Schlüssels.
    
2. Verwenden Sie die entschlüsselte TIK, um einen Website Schlüssel zu entschlüsseln.
    
3. Verwenden Sie den Schlüssel entschlüsselter Website, um einen BLOB-Schlüssel zu entschlüsseln.
    
4. Verwenden Sie den entschlüsselten BLOB-Schlüssel, um das BLOB zu entschlüsseln.
    
Beim Entschlüsseln eines TIK gibt Office 365 zwei Entschlüsselungs Anforderungen an Azure Key Vault mit einem leichten Offset aus. Der erste, der fertig gestellt wird, liefert das Ergebnis, wobei die andere Anforderung abgebrochen wird.
  
Wenn der Kunde den Zugriff auf seine Kundenschlüssel verliert, verschlüsselt Office 365 auch den TIK mit einem Verfügbarkeits Schlüssel und speichert diesen zusammen mit dem TIKs, der mit jedem Kundenschlüssel verschlüsselt ist. Der mit dem Verfügbarkeits Schlüssel verschlüsselte TIK wird nur verwendet, wenn der Kunde Microsoft auffordert, den Wiederherstellungspfad einzutragen, wenn er den Zugriff auf seine Schlüssel verloren hat, oder versehentlich.
  
Aus Gründen der Verfügbarkeit und der Skalierung werden entschlüsselte TIKs in einem zeitbegrenzten Arbeitsspeichercache zwischengespeichert. Zwei Stunden vor dem Ablauf eines TIK-Caches wird versucht, jede TIK zu entschlüsseln. Das entSchlüsseln des TIKs verlängert die Lebensdauer des Caches. Wenn die TIK-Entschlüsselung für eine erhebliche Zeitspanne fehlschlägt, generiert Office 365 eine Warnung, um die Planung vor dem Ablauf des Caches zu benachrichtigen. Nur, wenn der Kunde Microsoft Office 365 anruft, wird der Wiederherstellungsvorgang initiiert, der das Entschlüsseln des TIK mit dem im geheimen Speicher von Microsoft gespeicherten Verfügbarkeits Schlüssel und das erneute Onboarding des Mandanten mithilfe des entschlüsselten TIK und eines neuen Satzes von vom Kunden bereitgestellte Azure Key Vault-Schlüssel.
  
Ab heute ist der Kundenschlüssel an der Verschlüsselungs-und Entschlüsselungs Kette von im Azure-BLOB-Speicher gespeicherten SharePoint Online-Dateidaten beteiligt, nicht jedoch an SharePoint Online-Listenelementen oder-Metadaten, die in der SQL-Datenbank gespeichert sind. Office 365 verwendet nicht den Verfügbarkeits Schlüssel für SharePoint Online oder OneDrive für Unternehmen, außer dem oben beschriebenen Fall, der von Kunden initiiert wird. Der menschliche Zugriff auf Kundendaten wird durch die Lockbox des Kunden geschützt.
  
## <a name="how-is-customer-key-licensed"></a>Wie wird der Kundenschlüssel lizenziert?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Der Kundenschlüssel wird in der Office 365 Enterprise Suite, "E5" und der Advanced Compliance-SKU angeboten. Darüber hinaus müssen Kunden auch die entsprechende Lizenz für die Verwendung von Azure Key Vault erwerben.
  
Jeder Benutzer, der vom Kundenschlüssel profitiert, muss lizenziert werden, wenn er vom Kundenschlüssel abgedeckt werden soll.
  
Für SharePoint Online muss der Office 365-Administrator, der den Kundenschlüssel konfiguriert, ebenfalls lizenziert sein, um die Setupschritte ausführen zu können. Darüber hinaus müssen die Benutzer, die von dem Feature profitieren, lizenziert werden – dazu gehören der Websitebesitzer und alle Benutzer, die auf Dateien auf einem oder mehreren Websites zugreifen, die mit dem Kundenschlüssel verschlüsselt werden. Externe Benutzer müssen nicht lizenziert werden, um auf Dateien auf einem oder mehreren Websites zuzugreifen, die mit dem Kundenschlüssel verschlüsselt wurden.
  
Für Exchange Online müssen "Benutzerpostfächer" und "e-Mail-Benutzer"-Postfächer lizenziert sein. Alle anderen, wie etwa freigegebene Postfächer, müssen keine Lizenz für den Kundenschlüssel besitzen. Führen Sie das folgende Cmdlet aus, um zu überprüfen, ob Ihr Exchange Online-Postfach ordnungsgemäß lizenziert ist:
  
```
(Get-Mailbox <alias >).PersistedCapabilities
```

Wenn die Zeichenfolge BPOS_S_EquivioAnalytics vorhanden ist, wird das Postfach ordnungsgemäß lizenziert. Wenn dies nicht der Fall ist, müssen Sie die richtige Lizenz anwenden, um die Kundenschlüssel Funktion für dieses Postfach zu verwenden.
  
## <a name="can-i-enable-customer-key-for-a-trial-subscription"></a>Kann ich den Kundenschlüssel für ein Testabonnement aktivieren?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. DefinitionsGemäß haben Testabonnements eine begrenzte Lebensdauer. Verschlüsselungsschlüssel, die in Testabonnements gehostet werden, können am Ende der Test Lebensdauer verloren gehen. Da Microsoft Kunden nicht in der Lage ist, wichtige Kundendaten in Testabonnements einzusetzen, ist die Verwendung von Kunden Schlüsseln mit Testabonnements unzulässig.
  
## <a name="how-much-will-using-customer-key-cost"></a>Wie viel kostet der Einsatz von Kunden Schlüsseln?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Zusätzlich zu der für den Kundenschlüssel erforderlichen Lizenzierung entstehen für Kunden Kosten für die Verwendung von Schlüssel Tresoren. Die [Preisdetails in Azure Key Vault](https://azure.microsoft.com/en-us/pricing/details/key-vault/) beschreiben das Kostenmodell und helfen bei der Schätzung. Es gibt keine Möglichkeit, die genauen Kosten vorherzusagen, die jedem Kunden entstehen, da die Nutzungsmuster unterschiedlich sind. Die Erfahrung hat gezeigt, dass die Kosten sehr niedrig sind und in der Regel in den Bereich von $0,002 bis $0,005 pro Benutzer und Monat zuzüglich der Kosten von HSM-Backed Keys fallen. Die Kosten variieren auch entsprechend der vom Kunden ausgewählten Protokollierungskonfiguration und der Größe des Azure-Speichers, der für Azure-Schlüsseltresor-Protokolle verwendet wird. 
  
## <a name="for-more-information"></a>Weitere Informationen
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Erste Schritte mit dem Kundenschlüssel finden Sie unter [Controlling Your Data in Office 365 using Customer Key](controlling-your-data-using-customer-key.md).
  

