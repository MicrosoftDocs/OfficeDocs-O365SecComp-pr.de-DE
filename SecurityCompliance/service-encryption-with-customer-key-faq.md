---
title: Häufig gestellte Fragen zur Dienstverschlüsselung mit Kundenschlüssel für Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 41ae293a-bd5c-4083-acd8-e1a2b4329da6
description: Zusätzlich zu den Baseline Lautstärkepegel Verschlüsselung, die über BitLocker und verteilten Schlüssel-Manager (DKM), aktiviert ist bietet Office 365 Sicherheitsebene mit einer Verschlüsselung auf Anwendungsebene für Kunden Inhalte in Office 365, einschließlich der Daten aus Exchange Online, Skype für Unternehmen, SharePoint Online und OneDrive für Unternehmen. Dies ist die Verschlüsselung der Service bezeichnet.
ms.openlocfilehash: ceba35233872bb65b7706ed4e11a263057adc6c1
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575329"
---
# <a name="service-encryption-with-customer-key-for-office-365-faq"></a>Häufig gestellte Fragen zur Dienstverschlüsselung mit Kundenschlüssel für Office 365

Zusätzlich zu den Baseline Lautstärkepegel Verschlüsselung, die über BitLocker und verteilten Schlüssel-Manager (DKM), aktiviert ist bietet Office 365 Sicherheitsebene mit einer Verschlüsselung auf Anwendungsebene für Kunden Inhalte in Office 365, einschließlich der Daten aus Exchange Online, Skype für Unternehmen, SharePoint Online und OneDrive für Unternehmen. Dies ist die Verschlüsselung der Service bezeichnet.
  
Kundenschlüssel basiert auf Service-Verschlüsselung und können Sie bereitstellen und Steuerelement-Schlüssel, die zum Verschlüsseln von Ihrer Daten im Ruhezustand in Office 365 gemäß der [Online Services-Begriffe (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)verwendet werden. Kunden-Taste können Sie die Auflagen erfüllen, da Sie die Verschlüsselungsschlüssel, die Office 365 wird verwendet steuern, um Daten zu entschlüsseln.
  
Senden Sie Ihrer Ideen, Vorschläge und Perspektiven an customerkeyfeedback@microsoft.com, um Feedback auf Kundenschlüssel, einschließlich der Dokumentation zu ermöglichen.
  
## <a name="what-is-service-encryption-with-customer-key"></a>Was ist die Verschlüsselung der Service mit Kundenschlüssel?

Kundenschlüssel verbessert die Fähigkeit Ihrer Organisation, die Notwendigkeit, Compliance-Bestimmungen zu erfüllen, die wichtigsten Modalitäten mit dem Cloud-Dienstanbieter angeben. Mit Kundenschlüssel bereitstellen und steuern den Verschlüsselungsschlüssel für Ihre Office 365 Daten am-Rest auf Anwendungsebene. Daher können Sie Übung Kontrolle und Widerrufen von Ihrer Organisation Schlüsseln, sollten Sie entscheiden, um den Dienst zu beenden. Durch das Aufheben der Schlüssel, befinden sich die Daten mit dem Dienst nicht gelesen werden. Die Sperrung ist der erste Schritt auf dem Weg zur Daten löschen.

## <a name="what-office-365-data-at-rest-is-covered-by-customer-key"></a>Welche Office 365-Daten im Ruhezustand von Kundenschlüssel abgedeckt werden?
<a name="WhatDataIsCoveredbyCustomerKey"> </a>

SharePoint Online-Website-Inhalte und die Dateien, die auf dieser Website und Dateien zu OneDrive for Business hochgeladen werden behandelt. Exchange Online Inhalt von Postfächern (e-Mail-Body, Kalendereinträge und Inhalte von e-Mail-Anlagen) wird behandelt. Text Unterhaltungen von Skype für Unternehmen behandelt werden, aber Aufzeichnungen Skype Besprechung übertragen und Skype-Meeting Content Uploads werden nicht behandelt. Skype Besprechung übertragen und Skype Besprechungsinhalt Uploads zusammen mit allen anderen Inhalten in Office 365 verschlüsselt werden, aber es derzeit nicht bieten Kunden Kontrolle der Verschlüsselungsschlüssel.
  
## <a name="what-is-the-difference-between-customer-key-and-bring-your-own-key-byok-with-azure-information-protection-for-exchange-online"></a>Was ist der Unterschied zwischen Kundenschlüssel und schalten Sie Ihren eigenen Schlüssel (BYOK) mit Azure Information Protection für Exchange Online?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Beide Optionen können Sie bereitstellen und steuern Ihre eigene Verschlüsselungsschlüssel erstellen. jedoch verschlüsselt Service-Verschlüsselung mit Schlüssel Kunden Ihre Daten im Ruhezustand, die in Office 365-Servern am-Rest, während BYOK mit Azure Information Protection für Exchange Online Ihre Daten-Übertragung verschlüsselt und persistent online und offline bietet Schutz für e-Mail-Nachrichten und Anlagen für Office 365. Kundenschlüssel und BYOK mit Azure Information Protection für Exchange Online sind ergänzende und, ob Sie entscheiden, Microsoft Dienst verwaltet oder Ihre eigene Schlüssel verwenden, Ihre Daten am Rest und in während der Übertragung verschlüsselt kann hinzugefügten Schutz vor vor böswilligen Angriffen.
  
BYOK mit Azure Information Protection für Exchange Online wird in die Office 365 Message Encryption Funktionen angeboten.
  
## <a name="does-office-365-message-encryption-and-bring-your-own-key-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Ändert Office 365 Message Encryption und schalten Sie Ihren eigenen Schlüssel mit Azure Information Protection Microsofts Ansatz zur Drittanbieter-Daten von Anforderungen wie Anträge sich?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. Office 365 Message Encryption und die Option bereitgestellt und steuern Ihre eigene Verschlüsselungsschlüsseln mit schalten Sie Ihren eigenen Schlüssel (BYOK) für Azure Informationen Schutz (per) wurde nicht zur Beantwortung Recht Erzwingung Anträge entwickelt. Office 365 Message Encryption mit BYOK für per wurde für praxisorientierte Compliance-Kunden entwickelt, um ihre internen oder externen Auflagen erfüllen müssen. Microsoft nimmt sehr stark Drittanbieter-Anforderungen für die Kundendaten. Als Cloud-Dienstanbieter Vertreter wir immer für die Vertraulichkeit der Kundendaten. In der Ereignisprozedur wir eine Vorladung erhalten möchten, versuchen wir immer zur Umleitung von Drittanbieter an den Kunden, die Informationen zu erhalten. (Brad Smith Blog lesen: [Protecting Kundendaten von Behörden snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Wir veröffentlichen regelmäßig detaillierte Informationen der Anforderung wir erhalten [hier](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data).
  
Finden Sie im [Microsoft Trust Center](https://www.microsoft.com/en-us/trustcenter/default.aspx) zu im Zusammenhang mit Daten von Drittanbieter-Anforderungen und "Offenlegung von Kundendaten" in der [Online Services-Begriffe (OST) ](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)für Weitere Informationen.
  
## <a name="does-service-encryption-with-customer-key-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Ändert Service-Verschlüsselung mit Kundenschlüssel Microsofts Ansatz zur Drittanbieter-Daten von Anforderungen wie Anträge?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. Kunden-Taste wurde nicht zur Beantwortung Recht Erzwingung Anträge entwickelt. Es wurde regulierten Kunden auf ihren internen oder externen Auflagen erfüllen entwickelt. Microsoft nimmt sehr stark Drittanbieter-Anforderungen für die Kundendaten. Als Cloud-Dienstanbieter Vertreter wir immer für die Vertraulichkeit der Kundendaten. In der Ereignisprozedur wir eine Vorladung erhalten möchten, versuchen wir immer zur Umleitung von Drittanbieter an den Kunden, die Informationen zu erhalten. (Brad Smith Blog lesen: [Protecting Kundendaten von Behörden snooping](http://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Wir veröffentlichen regelmäßig detaillierte Informationen der Anforderung wir erhalten [hier](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data).
  
Finden Sie im [Microsoft Trust Center](https://www.microsoft.com/en-us/trustcenter/Privacy/govt-requests-for-data) zu im Zusammenhang mit Daten von Drittanbieter-Anforderungen und "Offenlegung von Kundendaten" in der [Online Services-Begriffe (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx) für Weitere Informationen. 
  
## <a name="is-fasttrack-support-available-for-implementing-customer-key"></a>Ist der schnelle Unterstützung für die Implementierung von Kundenschlüssel verfügbar?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. Schnelle wird nur verwendet, um Mandanten und Dienst Konfigurationsdaten gesammelt, die für Kundenschlüssel registriert erforderlich ist. Der Schlüssel bietet Kunden werden, damit es erscheint sinnvoll für Kunden und Partnern, diese erforderlichen Informationen mit demselben Verfahren und zur Erleichterung der Archivierung der Daten, die Kunden in dem Angebot über schnelle veröffentlicht.
  
Wenn Sie weitere Unterstützung von mehr als die Dokumentation benötigen, wenden Sie sich an einen Microsoft Consulting Services (MCS), Premier Field Engineering (PFE) oder einem Microsoft-Partner.
  
## <a name="if-my-keys-are-destroyed-how-can-i-recover"></a>Wenn mein Schlüssel gelöscht werden, können wie ich werden wiederhergestellt?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Der Schlüssel Verfügbarkeit bietet Ihnen die Möglichkeit, die von der unvorhergesehene Verlust der Stammschlüssel wiederhergestellt werden, die Sie verwalten. Wenn Sie die Stammschlüssel verlieren, hilft Microsoft-Support zu kontaktieren und Microsoft durch den Prozess von der Verfügbarkeit Aktivierungsschlüssel Ihnen. Verwenden Sie die Taste Verfügbarkeit zum Migrieren zu einer neuen Richtlinie für die Verschlüsselung von Daten mit neuen Schlüssel, die von Ihnen bereitgestellt. 
  
## <a name="what-is-the-availability-key"></a>Was ist der Schlüssel Verfügbarkeit?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Der Schlüssel Verfügbarkeit ist ein Stamm, die beim Erstellen einer Daten-Verschlüsselungsrichtlinie bereitgestellt wird. Der Schlüssel Verfügbarkeit gespeichert und geschützt in Office 365 und ist funktional mit zwei Stammschlüssel, die von Ihnen für die Verwendung mit Verschlüsselung Service mit Kundenschlüssel bereitgestellt werden. Im Gegensatz zu den Schlüsseln, die Sie bereitstellen und Verwalten von Azure Schlüssel Vault können nicht direkt Schlüssels Verfügbarkeit zugreifen werden. Speicherung und Steuerung des Schlüssels Verfügbarkeit unterscheiden sich bewusst von Azure Schlüssel Vault-Schlüsseln für drei Gründe: zunächst der Verfügbarkeit Schlüssel ein Funktionen für hohe Verfügbarkeit bietet, die Office 365-Dienste nicht erreicht Schlüssel im Schlüssel Azure gehostet werden Vault; Zweitens verfügt über die Verfügbarkeit-Taste eine Funktion "break Glas" den Fall, dass beide Azure Schlüssel Vault Schlüssel verloren gegangen sind; und dritte die Trennung von logischen Steuerelemente bietet Verteidigung und schützt vor den Verlust aller Schlüssel aus einem einzigen Angriff oder Zeitpunkt des Fehlers. Freigabe verantwortlich für die Schlüssel schützen, während der Verwendung verschiedener Schutzebenen und Prozesse für Key Management reduziert letztendlich das Risiko, dass alle Schlüssel (und damit Ihre Daten) verloren gehen oder gelöscht werden soll. Microsoft bietet Ihnen dazu berechtigt über die Vernichtung der Verfügbarkeit-Taste. Konzipiert niemand bei Microsoft hat Zugriff auf die Taste Verfügbarkeit – nur von Office 365-Dienstcode zugegriffen werden.
  
## <a name="how-many-data-encryption-policies-deps-can-i-create"></a>Wie viele datenverschlüsselung Policies (Einzahlgn) kann ich erstellen?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype für Unternehmen:** Sie können bis zu 50 Einzahlgn erstellen. 
  
 **SharePoint Online und OneDrive für Unternehmen:** Eine Datenausführungsverhinderung gilt für Daten in einem geografischen Standort, auch als eine Geo bezeichnet. Wenn Sie das Multi-Geo-Feature von Office 365 verwenden, können Sie eine DEP pro Geo erstellen. Wenn Sie Multi-Geo nicht verwenden, können Sie eine Datenausführungsverhinderung erstellen.
  
## <a name="can-i-assign-a-data-encryption-policy-before-migrating-a-mailbox-to-the-cloud"></a>Kann ich eine datenverschlüsselung Richtlinie zuweisen, vor der Migration eines Postfachs in die Cloud?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Ja. Das Windows PowerShell-Cmdlet Set-MailUser können zuweisen eine Richtlinie für Daten-Verschlüsselung (DEP) für den Benutzer vor der Migration des Postfachs zu Office 365. Wenn Sie dies tun, werden der Inhalt des Postfachs mit der zugewiesenen Datenausführungsverhinderung, wie der Inhalt migriert wird verschlüsselt. Dies kann sein effizienter als eine DEP zuweisen, nachdem das Postfach bereits migriert wurde und darauf zu warten, für die Verschlüsselung erfolgen, die Stunden oder möglicherweise Tage dauern kann. 
  
## <a name="how-do-i-verify-that-encryption-with-customer-key-is-activated-and-office-365-has-finished-encrypting-with-customer-key"></a>Wie überprüfe ich, dass Verschlüsselung mit Kundenschlüssel aktiviert ist, und Office 365 mit Kundenschlüssel verschlüsseln beendet wurde?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype für Unternehmen:** Sie können [eine Verbindung mit Exchange Online mithilfe von remote-PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) und dann verwenden Sie das Cmdlet **[Get-MailboxStatistics]** für jedes Postfach, die Sie prüfen möchten. In der Ausgabe des Cmdlets Get-MailboxStatistics gibt die _IsEncrypted_ -Eigenschaft der Wert **true,** Wenn das Postfach verschlüsselt sind und der Wert **false** , falls noch nicht. Wenn das Postfach verschlüsselt ist, ist der für die _DataEncryptionPolicyID_ -Eigenschaft zurückgegebene Wert die GUID der die Datenausführungsverhinderung, mit dem das Postfach verschlüsselt ist. Weitere Informationen zum Ausführen dieses Cmdlets finden Sie unter [Get-MailboxStatistics](https://technet.microsoft.com/en-us/library/bb124612%28v=exchg.160%29.aspx) und Verwenden von PowerShell mit Exchange Online. 
  
Wenn die Postfächer verschlüsselt werden nicht nach 72 Stunden zu warten Sie die Datenausführungsverhinderung zugewiesen, Verschieben eines Postfachs zu initiieren. Dazu [zu Exchange Online mit remote-PowerShell eine Verbindung herstellen](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , und verwenden Sie das Cmdlet New-MoveRequest, und geben Sie den Alias des Postfachs wie folgt: 
  
```
New-MoveRequest <alias>
```

 **SharePoint Online und OneDrive für Unternehmen:** Sie können [eine Verbindung mit SharePoint Online-PowerShell](https://technet.microsoft.com/en-us/library/fp161372.aspx), und klicken Sie dann mit dem Cmdlet **[Get-SPODataEncryptionPolicy]** verwenden, um den Status Ihres Mandanten zu überprüfen. Die ** _Zustand_**-Eigenschaft gibt einen Wert von **registriert** , wenn Kundenschlüssel Verschlüsselung aktiviert ist, und alle Dateien in allen Websites verschlüsselt wurden. Wenn die Verschlüsselung noch ausgeführt wird, enthält dieses Cmdlet Informationen wie viel Prozent der Websites abgeschlossen ist. 
  
## <a name="if-i-want-to-switch-to-a-different-set-of-keys-how-long-does-it-take-for-the-new-set-of-keys-to-protect-my-data"></a>Wenn ich eine andere Menge von Schlüsseln wechseln möchten, wie lange für den neuen Satz von Schlüsseln dauert es, meine Daten zu schützen?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype für Unternehmen:** Es dauert bis zu 72 Stunden, um ein Postfach gemäß einer neuen Daten Verschlüsselung Richtlinie (DEP) die Zeit zu schützen, denen die neue DEP an das Postfach zugeordnet ist. 
  
 **SharePoint Online und OneDrive für Unternehmen:** Sie können Ihre gesamte Mandanten erneut zu verschlüsseln, sobald ein neuer Schlüssel zugewiesen wurde bis zu vier Stunden dauern. 
  
## <a name="is-my-existing-data-stored-without-encryption-at-any-time-while-it-is-decrypted-or-encrypted-with-customer-key"></a>Sind meine vorhandenen Daten gespeichert ohne Verschlüsselung können Sie jederzeit während mit Kundenschlüssel verschlüsselt oder entschlüsselt wird?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. Die Daten werden immer im Ruhezustand in Office 365-Dienst mit BitLocker und DKM verschlüsselt. Weitere Informationen finden Sie unter "Sicherheit, Datenschutz, und Kompatibilitätsdaten für Office 365", und [wie Exchange Online schützt Ihre e-Mail-vertraulichen Daten](https://support.office.com/article/989BA10C-F73F-4EFB-AD1B-AF3322E5F376).
  
## <a name="if-i-no-longer-want-to-use-customer-managed-encryption-keys-can-i-switch-to-microsoft-managed-keys"></a>Wenn ich nicht mehr Kunden verwalteten Verschlüsselungsschlüssel verwenden möchten, kann ich Microsoft-Mitarbeiter Tasten wechseln?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype für Unternehmen:** Noch nicht. Dies wird unterstützt werden, sobald Service Verschlüsselung in Office 365 mit Schlüsseln Microsoft-Mitarbeiter im Allgemeinen gibt es eingeführt. Wir erwarten einführen dies im Dienst nach dem veröffentlichen wir Service-Verschlüsselung mit Kundenschlüssel. 
  
 **SharePoint Online und OneDrive für Unternehmen:** Ja. Sie können auch mit Microsoft-Mitarbeiter Schlüssel separat für jedes Geo (Wenn Sie das Multi-Geo-Feature verwenden) oder für alle Ihre Daten ist in einer einzelnen Geo wiederherstellen. 
  
## <a name="if-i-lose-my-keys-how-long-does-it-take-to-recover-service-availability-using-the-recovery-key"></a>Wenn ich mein Schlüssel verlieren, wie lange dauert es zum Wiederherstellen der Verfügbarkeit von Diensten mithilfe des Wiederherstellungsschlüssels?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

 **Exchange Online und Skype für Unternehmen:** Nachdem Sie Aufrufen der Verfügbarkeit Schlüssel verwenden, können innerhalb von Minuten Postfächer zugegriffen werden. 
  
 **SharePoint Online und OneDrive für Unternehmen:** Dieser Vorgang ist proportional zur Anzahl der Standorte vorhanden sind. Nachdem Sie den Schlüssel Verfügbarkeit verwenden, um Microsoft aufrufen, werden Sie innerhalb von ungefähr vier Stunden vollständig online sein. 
  
## <a name="how-is-the-availability-key-used-with-exchange-online"></a>Wie wird der Verfügbarkeit Schlüssel mit Exchange Online verwendet?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Es gibt drei Möglichkeiten, der Verfügbarkeit Schlüssel verwendet wird mit Exchange Online:
  
- Service-Verfügbarkeit – die Azure Schlüssel Vault-Schlüssel nicht erreichbar sind.
    
- Aktionen, die von Office 365-Dienstcode – beispielsweise Search-indexerstellung initiiert oder Verschieben von Postfächern.
    
- Wiederherstellen von Verlust des Schlüssels - wie den Verlust von Azure Schlüssel Vault Tasten mit einer einzelnen Datenausführungsverhinderung verknüpft ist
    
 **Verwenden den Schlüssel Verfügbarkeit Verfügbarkeit in der Ereignisprozedur Azure Schlüssel Vault-Schlüssel nicht erreichbar sind.**
  
Office 365 verwendet den Verfügbarkeit-Schlüssel sowohl für Verfügbarkeit und Recovery aus einen fehlerhaften Zustand Kundenschlüssel für Exchange Online. Es ist eine Hierarchie von Schlüsseln von Kundenschlüssel verwendet. Diese Hierarchie ist in der folgenden Abbildung dargestellt.
  
![](media/a760156b-737f-469a-80ab-c28b7a8b9160.png)
  
Wenn beide Azure Schlüssel Vault Schlüssel von einem einzelnen Daten Verschlüsselung Richtlinie (DEP) nicht verfügbar sind, können die Verfügbarkeit von Office 365 verwenden-Taste, um zu einem neuen Datenausführungsverhinderung Office 365 ändern bestimmt, ob die Taste Verfügbarkeit Verfügbarkeit unterschiedlich je nachdem, ob verwendet eine vom Benutzer initiierte Aktivität, wenn ein Benutzer an der Outlook-Client oder eine System initiiert Aktivität, wie die Indizierung Postfachinhalte oder für eDiscovery-suchen e-Mail herunterlädt beispielsweise ausgelöst des Prozesses.
  
Office 365 folgt dieser Prozess als Antwort auf vom Benutzer initiierte Aktionen zu bestimmen, ob die Taste Verfügbarkeit für Benutzerpostfächer verwenden:
  
1. Office 365 liest die Datenausführungsverhinderung an, der das Postfach zugewiesen ist, um den Speicherort der zwei-Customer Schlüssel in Azure Schlüssel Vault zu bestimmen.
    
2. Office 365 nach dem Zufallsprinzip wählt eine der zwei-Customer-Tasten aus der Datenausführungsverhinderung und sendet eine Anforderung an Azure Schlüssel Vault aufgelöst werden mit dem Kundenschlüssel DEP-Taste.
    
3. Wenn die Anforderung an die Datenausführungsverhinderung Entpacken wichtige mit Office 365 sendet eine zweite Anforderung an Azure Schlüssel Vault, diesmal anweist, verwenden Sie die alternative Schlüssels Kunden schlägt fehl und gibt einen Fehler zurück, (zweite) Kunden-Taste.
    
4. Wenn die zweite Anforderung an den DEP-Schlüssel, die mit der wichtigsten Kunden ist fehlerhaft entpacken und gibt einen Fehler zurück, untersucht Office 365 die Ergebnisse der beiden Anforderungen:
    
  - Die Prüfung fest, dass der Fehler nicht durch eine Identität Kunden einen expliziten Vorgang widerzuspiegeln, verwendet Office 365 Schlüssels Verfügbarkeit den Datenausführungsverhinderung Schlüssel entschlüsselt. Die Datenausführungsverhinderung-Taste wird zum Entschlüsseln des Postfach-Schlüssels, und schließen Sie die benutzeranforderung verwendet.
    
    In diesem Fall ist Azure Schlüssel Vault entweder reagiert oder nicht erreichbar aus irgendeinem Grund. Office 365 verfügt über keine Möglichkeit, feststellen, ob der Kunden Zugriff auf die Schlüssel absichtlich gesperrt wurde.
    
  - Wenn gibt an, die Prüfung der Kunde Schlüssel nicht verfügbar ist, gerendert wurde, absichtliche Aktion übernommen und klicken Sie dann Schlüssels Verfügbarkeit nicht verwendet werden, die benutzeranforderung ein Fehler auftritt und der Benutzer erhält eine Fehlermeldung angezeigt, wie beispielsweise Fehler bei der Anmeldung.
    
    In diesem Fall wird der Kunden darauf aufmerksam gemacht, dass der Dienst beeinträchtigt wird, und die Bedingung des Kunden Schlüssels ist fehlerhaft. Wenn ein Kunde einen einzelnen Datenausführungsverhinderung für alle Postfächer in der Organisation verwendet wird, kann Kunden beispielsweise einen weit verbreitete Fehler auftreten, in dem Benutzer nicht auf ihre Postfächer zugreifen können. Dadurch wird sichergestellt, dass wenn beide Kundenschlüssel fehlerhaft sind, der Kunden, sollten Sie die Notwendigkeit vorliegt, die über diese Situation zu beheben und den Dienst in einem fehlerfreien Zustand wiederherzustellen.
    
 **Verwenden die Verfügbarkeit-Taste für Aktionen, die von Office 365-Dienstcode initiiert.**
  
Office 365-Dienstcode immer verfügt über ein gültiger Anmeldename Token und nicht blockiert werden. Aus diesem Grund, bis der Verfügbarkeit Schlüssel gelöscht wurde, kann er für Aktionen von initiiert wurde, oder für Office 365-Dienst Code, wie etwa Search-indexerstellung intern oder Verschieben von Postfächern verwendet werden.
  
 **Mithilfe des Availability-Schlüssels zur Wiederherstellung Verlust des Schlüssels.**
  
Den Schlüssel Verfügbarkeit können Sie von den Verlust von beide Azure Schlüssel Vault Schlüssel wiederhergestellt werden, die die gleichen DEP zugeordnet sind wie beschrieben in der Antwort auf den Eintrag häufig gestellte Fragen "Wenn mein Schlüssel gelöscht werden, wie ich wiederhergestellt werden können?".
  
## <a name="how-is-the-availability-key-used-with-sharepoint-online-and-onedrive-for-business"></a>Wie wird der Verfügbarkeit Schlüssel mit SharePoint Online und OneDrive für Unternehmen verwendet?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Die SharePoint Online und OneDrive for Business-Architektur und Implementierung für Kundenschlüssel und Verfügbarkeit Schlüssel unterscheiden sich von Exchange Online und Skype für Unternehmen.
  
Wenn ein Kunde zu Kunden verwalteten Schlüssel wechselt, erstellt Office 365 einen Mandanten-spezifischen intermediate Schlüssel (TIK). Office 365 verschlüsselt die TIK zweimal einmal mit aller Kundenschlüssel, und speichert die verschlüsselten zwei Versionen der TIK. Nur die verschlüsselten Versionen der die TIK gespeichert sind, und eine TIK nur mit den Kunden Schlüsseln entschlüsselt werden kann. Die TIK wird dann zum Verschlüsseln von Website-Schlüssel, die anschließend zum Verschlüsseln von BLOB-Schlüssel verwendet werden. Die Blobs selbst sind verschlüsselt und in den Dienst Microsoft Azure BLOB-Speicher gespeichert.
  
Office 365 folgt diesen Vorgang, um ein Blob zugreifen, der Kundendaten Datei hat:
  
1. Die TIK mit dem Kunden-Schlüssel zu entschlüsseln.
    
2. Verwenden Sie die entschlüsselten TIK, um einen Website-Schlüssel zu entschlüsseln.
    
3. Verwenden Sie den Schlüssel entschlüsselten Website, um ein Blob-Schlüssel zu entschlüsseln.
    
4. Verwenden Sie die entschlüsselten Blob-Taste, um den Blob zu entschlüsseln.
    
Wenn ein TIK entschlüsseln, stellt Office 365 zwei Entschlüsselung Anforderungen für Azure Schlüssel Vault mit einer leichten Offset aus. So schließen Sie der ersten stellt das Ergebnis, die andere Anforderung stornieren bereit.
  
Für den Fall, dass der Kunden Zugriff auf ihre Kundenschlüssel verliert, wird in Office 365 auch verschlüsselt die TIK mit einem Schlüssel Verfügbarkeit und speichert diese zusammen mit der TIKs mit jedem Kundenschlüssel verschlüsselt. Die TIK verschlüsselt mit dem Schlüssel Verfügbarkeit wird nur, wenn der Kunde Microsoft den Wiederherstellungspfad eintragen anruft, wenn sie den Zugriff auf ihre Schlüssel oder versehentlich verloren.
  
Verfügbarkeit und Skalierung Gründe werden in einem Arbeitsspeichercache zeitlich begrenzte entschlüsselten TIKs zwischengespeichert. Zwei Stunden, bis ein TIK Cache festgelegt wird, abläuft, versucht Office 365, jede TIK entschlüsseln. Entschlüsseln der TIKs erstreckt sich die Lebensdauer des Caches. Wenn ein signifikanter zeitlicher TIK Entschlüsselung fehlschlägt, generiert Office 365 eine Warnung um Engineering vor der Ablaufzeit für den Cache zu benachrichtigen. Nur, wenn der Kunde Microsoft bezeichnet werden Office 365 des Wiederherstellungsvorgangs gestartet umfasst Entschlüsseln der TIK mit dem Schlüssel Verfügbarkeit in Microsofts geheimen Store und den Mandanten erneut mit der entschlüsselte Onboarding TIK und ein neuer Satz von gespeichert Kunden bereitgestellten Azure Schlüssel Vault Schlüssel.
  
Ab heute ist Kundenschlüssel der Kette Ver- und Entschlüsselung von SharePoint Online Dateidaten im Azure Blob-Speicher, aber nicht SharePoint Online Listenelemente oder in der SQL-Datenbank gespeicherten Metadaten gespeichert beteiligt. Office 365 wird nicht als die oben beschriebene Groß-/Kleinschreibung Schlüssels Verfügbarkeit für SharePoint Online oder OneDrive für Unternehmen verwendet die Kunden initiiert wird. Human Zugriff auf Kundendaten ist durch Kunden Lockbox geschützt.
  
## <a name="how-is-customer-key-licensed"></a>Wie wird Kundenschlüssel lizenziert?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Kundenschlüssel wird in der Office 365 Enterprise-Suite, "E5" und die erweiterte Compliance-SKU angeboten. Darüber hinaus müssen Kunden auch die entsprechende Lizenz für die Verwendung von Azure Schlüssel Vault erwerben.
  
Jeder Benutzer profitieren von Kundenschlüssel muss lizenziert werden, die von Kundenschlüssel abgedeckt werden sollen.
  
Für SharePoint Online muss der Office 365-Administrator, die Kundenschlüssel konfiguriert auch zum Ausführen der Setupschritte lizenziert werden. Darüber hinaus müssen die Benutzer, die von der Funktion profitieren lizenziert werden – dazu gehören der Websitebesitzer und Benutzer den Zugriff auf Dateien auf einem oder mehreren Standorten, die mit Kundenschlüssel verschlüsselt werden. Externe Benutzer müssen nicht lizenziert werden, um die Dateien auf eine oder mehrere Websites zugreifen, die mit Kundenschlüssel verschlüsselt werden.
  
Für Exchange Online müssen "User" und "e-Mail-Benutzer" Postfächer lizenziert werden. Alle anderen, wie etwa freigegebene Postfächer müssen nicht über eine Lizenz für Kundenschlüssel verfügen. Um zu überprüfen, dass Ihre Exchange Online-Postfach ordnungsgemäß lizenziert ist, führen Sie das folgende Cmdlet aus:
  
```
(Get-Mailbox <alias >).PersistedCapabilities
```

Wenn die Zeichenfolge BPOS_S_EquivioAnalytics vorhanden ist, wird das Postfach ordnungsgemäß lizenziert. Wenn dies nicht der Fall ist, müssen Sie die entsprechende Lizenz zum Verwenden der Customer-Schlüssel für dieses Postfach anwenden.
  
## <a name="can-i-enable-customer-key-for-a-trial-subscription"></a>Kann ich Kundenschlüssel für einen Test-Abonnement aktivieren?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Nein. Per Definition haben Testabonnements eine beschränkte Lebensdauer. Verschlüsselungsschlüssel, die in Testabonnements gehostet werden können am Ende der Lebensdauer Studien verloren gehen. Da Microsoft nicht und verhindert nicht, dass Kunden wichtige Kundendaten Testabonnements Websitemigration, ist die Verwendung des Schlüssels Kunden mit Testabonnements nicht erlaubt.
  
## <a name="how-much-will-using-customer-key-cost"></a>Wie viel wird Kundenschlüssel Kosten verwenden?
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Zusätzlich zu der Lizenzierung für Kundenschlüssel erforderlich, werden Kunden Kosten für die Verwendung der Schlüssel Vault zu übernehmen. [Azure Schlüssel Vault Preise](https://azure.microsoft.com/en-us/pricing/details/key-vault/) beschreibt das Kostenmodell und hilft bei der Schätzung. Es ist nicht möglich, die genaue Kosten vorhergesagt, die kundenspezifischen entstehen, da Verwendungsmuster variieren. Die Erfahrung hat gezeigt, dass die Kosten sehr gering ist und in der Regel innerhalb des Bereichs der $0,002 zu $0,005 pro Benutzer pro Monat, zuzüglich der Kosten von Schlüsseln HSM-Backup liegt. Die Kosten variiert entsprechend der Protokollierungskonfiguration für die von Kunden und der Menge der Azure-Speicher für Azure Schlüssel Vault Protokolle ausgewählt wird. 
  
## <a name="for-more-information"></a>Weitere Informationen
<a name="DiffCustomerKeyandBYOKAzureIP"> </a>

Mit Kundenschlüssel Einstieg finden Sie unter [Kontrolle über Ihre Daten in Office 365 mit Kunden-Taste](controlling-your-data-using-customer-key.md).
  

