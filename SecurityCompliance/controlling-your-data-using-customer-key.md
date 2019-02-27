---
title: Kontrolle über Daten in Office 365 mithilfe von Kundenschlüsseln
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie den Kundenschlüssel für Office 365 für Exchange Online, Skype for Business, SharePoint Online und OneDrive for Business einrichten. Mit dem Kundenschlüssel können Sie die Verschlüsselungsschlüssel Ihrer Organisation steuern und dann Office 365 so konfigurieren, dass Sie zum Verschlüsseln Ihrer Daten im Rest in Microsoft-Rechenzentren verwendet werden.
ms.openlocfilehash: 219ddb94727cd2b708f734a77a8397b3bc3f1064
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296668"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a>Kontrolle über Daten in Office 365 mithilfe von Kundenschlüsseln

Mit dem Kundenschlüssel können Sie die Verschlüsselungsschlüssel Ihrer Organisation steuern und dann Office 365 so konfigurieren, dass Sie zum Verschlüsseln Ihrer Daten im Rest in Microsoft-Rechenzentren verwendet werden. Mit anderen Worten: der Kundenschlüssel ermöglicht es Kunden, mit ihren Schlüsseln eine Verschlüsselungsschicht hinzuzufügen, die Ihnen gehört. Zu den restlichen Daten gehören Daten aus Exchange Online und Skype for Business, die in Postfächern und Dateien gespeichert sind, die in SharePoint Online und OneDrive for Business gespeichert sind.
  
Sie müssen Azure einrichten, bevor Sie den Kundenschlüssel für Office 365 verwenden können. In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um die erforderlichen Azure-Ressourcen zu erstellen und zu konfigurieren und dann die Schritte zum Einrichten des Kunden Schlüssels in Office 365. Nachdem Sie das Azure-Setup abgeschlossen haben, legen Sie fest, welche Richtlinie und daher welche Schlüssel den Postfächern und Dateien in Ihrer Organisation zugewiesen werden sollen. Postfächer und Dateien, für die Sie keine Richtlinie zuweisen, verwenden Verschlüsselungsrichtlinien, die von Microsoft gesteuert und verwaltet werden. Weitere Informationen zum Kundenschlüssel oder eine allgemeine Übersicht finden Sie unter [Kundenschlüssel für Office 365 FAQ](service-encryption-with-customer-key-faq.md).
  
> [!IMPORTANT]
> Es wird dringend empfohlen, dass Sie die bewährten Methoden in diesem Thema befolgen. Diese werden als **Trinkgeld** und **wichtig**bezeichnet. Mit dem Kundenschlüssel können Sie die Stamm Verschlüsselungsschlüssel steuern, deren Bereich so breit wie die gesamte Organisation sein kann. Dies bedeutet, dass Fehler, die mit diesen Schlüsseln vorgenommen werden, eine große Auswirkung haben und zu Dienstunterbrechungen oder unwiderruflichem Verlust Ihrer Daten führen können. 
  
## <a name="before-you-begin-setting-up-customer-key"></a>Bevor Sie mit dem Einrichten des Kunden Schlüssels beginnen
<a name="Beforeyoustart"> </a>

Bevor Sie beginnen, sollten Sie sicherstellen, dass Sie über die entsprechenden Lizenzen für Ihre Organisation verfügen. Der Kundenschlüssel in Office 365 wird in Office 365 E5 oder der Advanced Compliance-SKU angeboten.
  
Um die Konzepte und Verfahren in diesem Thema zu verstehen, sollten Sie sich die [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) -Dokumentation ansehen. Sie können sich auch mit den in Azure verwendeten Ausdrücken vertraut machen, Beispiels [](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant)Weise mit dem Mandanten.
  
Um Feedback zum Kundenschlüssel, einschließlich der Dokumentation, zu geben, senden Sie Ihre Ideen, Vorschläge und Perspektiven an customerkeyfeedback@microsoft.com.
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a>Übersicht über das Einrichten des Kunden Schlüssels für Office 365
<a name="Overview"> </a>

Zum Einrichten des Kunden Schlüssels führen Sie diese Aufgaben aus. Im restlichen Teil dieses Themas finden Sie detaillierte Anweisungen für jede Aufgabe oder Links zu weiteren Informationen für jeden Schritt im Prozess.
  
**In Azure und Microsoft:**
  
Die meisten dieser Aufgaben werden durch Remoteverbindung mit Azure PowerShell ausgeführt. Verwenden Sie Version 4.4.0 oder höher von Azure PowerShell, um optimale Ergebnisse zu erzielen.
  
- [Erstellen zweier neuer Azure-Abonnements](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [Registrieren von Azure-Abonnements für die Verwendung eines obligatorischen Aufbewahrungszeitraums](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    Die Registrierung kann zwischen einem und fünf Werktagen dauern.
    
- [Senden einer Anforderung zum Aktivieren des Kunden Schlüssels für Office 365](controlling-your-data-using-customer-key.md#FastTrack)
    
    Nachdem Sie die beiden neuen Azure-Abonnements erstellt haben, müssen Sie die entsprechende Anforderung für das Kunden-Key-Angebot übermitteln, indem Sie ein Webformular ausfüllen, das im Microsoft-Portal für den Zugriff gehostet wird. **Das Team für die Zusammenarbeit bietet keine Unterstützung für den Kundenschlüssel. Office verwendet einfach das Portal für den Überblick, mit dem Sie das Formular übermitteln und uns dabei helfen können, die relevanten Angebote für den Kundenschlüssel nachzuverfolgen**.
  
Nachdem Sie ein Kundenschlüssel Angebot eingereicht haben, prüft Microsoft Ihre Anfrage und benachrichtigt Sie, wenn Sie mit den restlichen Setupaufgaben fortfahren können. Dieser Vorgang kann bis zu fünf Arbeitstage dauern.
    
- [Erstellen eines Premium-Azure-Schlüsseldepots in jedem Abonnement](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [Zuweisen von Berechtigungen zu jedem schlüsseltresor](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [Aktivieren und bestätigen des weichen Löschvorganges in ihren Schlüsseldepots](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [Hinzufügen eines Schlüssels zu jedem Schlüsseldepot durch Erstellen oder Importieren eines Schlüssels](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [Überprüfen der Wiederherstellungsebene der Schlüssel](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [Azure-Schlüsseltresor sichern](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [Validieren von Azure Key Vault-Konfigurationseinstellungen](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [Abrufen des URIs für jeden Azure Key Vault-Schlüssel](controlling-your-data-using-customer-key.md#GetKeyURI)
    
**In Office 365:**
  
Exchange Online und Skype for Business:
  
- [Erstellen einer Daten Verschlüsselungsrichtlinie für die Verwendung mit Exchange Online und Skype for Business](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [Zuweisen einer DEP zu einem Postfach](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [ÜberPrüfen der Postfachverschlüsselung](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
SharePoint Online und OneDrive for Business:
  
- [Erstellen Sie eine Daten Verschlüsselungsrichtlinie (DEP) für jede SharePoint Online-und OneDrive for Business-Geo](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [Überprüfen der Verschlüsselung von Gruppen Websites, Team Websites und OneDrive für Unternehmen](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a>Ausführen von Aufgaben in Azure Key Vault und Microsoft für den Kundenschlüssel
<a name="AzureSteps"> </a>

Führen Sie diese Aufgaben in Azure Key Vault aus, um den Kundenschlüssel für Office 365 einzurichten. Sie müssen diese Schritte unabhängig davon ausführen, ob Sie den Kundenschlüssel für Exchange Online und Skype for Business oder SharePoint Online und OneDrive for Business oder für alle unterstützten Dienste in Office 365 einrichten möchten.
  
### <a name="create-two-new-azure-subscriptions"></a>Erstellen zweier neuer Azure-Abonnements
<a name="Create2newsubs"> </a>

Für den Kundenschlüssel sind zwei Azure-Abonnements erforderlich. Als bewährte vorgehensWeise empfiehlt Microsoft, dass Sie neue Azure-Abonnements für die Verwendung mit dem Kundenschlüssel erstellen. Azure Key Vault-Schlüssel können nur für Anwendungen im selben Azure Active Directory-Mandanten (AAD) autorisiert werden, Sie müssen die neuen Abonnements mit demselben Azure AD-Mandanten erstellen, der mit Ihrer Office 365-Organisation verwendet wird, in der die DEPs zugewiesen werden. Verwenden Sie beispielsweise Ihr Arbeits-oder Schulkonto mit globalen Administratorrechten in Ihrer Office 365-Organisation. Weitere Informationen finden Sie unter [registrieren für Azure als Organisation](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).
  
> [!IMPORTANT]
> Der Kundenschlüssel erfordert zwei Schlüssel für jede Daten Verschlüsselungsrichtlinie. Um dies zu erreichen, müssen Sie zwei Azure-Abonnements erstellen. Als bewährte Vorgehensweise empfiehlt Microsoft, dass separate Mitglieder Ihrer Organisation einen Schlüssel in jedem Abonnement konfigurieren. Darüber hinaus sollten diese Azure-Abonnements nur für die Verwaltung von Verschlüsselungsschlüsseln für Office 365 verwendet werden. Dies schützt Ihre Organisation, falls eine ihrer Operatoren versehentlich, absichtlich oder in böswilliger Absicht die Schlüssel löscht, für die Sie verantwortlich sind.<br/> Es wird empfohlen, neue Azure-Abonnements einzurichten, die ausschließlich für die Verwaltung von Azure Key Vault-Ressourcen zur Verwendung mit dem Kundenschlüssel verwendet werden. Es gibt keine praktische Grenze für die Anzahl von Azure-Abonnements, die Sie für Ihre Organisation erstellen können. Durch diese bewährte Vorgehensweise werden die Auswirkungen menschlicher Fehler minimiert und gleichzeitig die Ressourcen der Kundenschlüssel verwaltet. 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a>Senden einer Anforderung zum Aktivieren des Kunden Schlüssels für Office 365
<a name="FastTrack"> </a>

Nachdem Sie die Azure-Schritte abgeschlossen haben, müssen Sie eine Angebotsanforderung im [Microsoft-Portal](https://fasttrack.microsoft.com/)für die Übersendung einreichen. Nachdem Sie eine Anforderung über das Web-Portal für die Verbindung gesendet haben, überprüft Microsoft die von Ihnen bereitgestellten Konfigurationsdaten und Kontaktinformationen von Azure Key Vault. Die Auswahl, die Sie im Angebotsformular bezüglich der autorisierten Mitarbeiter Ihrer Organisation treffen, ist kritisch und für die Fertigstellung der Kundenschlüssel Registrierung erforderlich. Die Offiziere Ihrer Organisation, die Sie im Formular auswählen, werden verwendet, um sicherzustellen, dass alle Anforderungen zum widerrufen und zerstören aller Schlüssel, die mit einer Kundenschlüssel-Daten Verschlüsselungsrichtlinie verwendet werden, verschlüsselt werden. Sie müssen diesen Schritt einmal ausführen, um den Kundenschlüssel für Exchange Online und Skype for Business-Abdeckung zu aktivieren, und ein zweites Mal, um den Kundenschlüssel für SharePoint Online und OneDrive for Business zu aktivieren.
  
Führen Sie die folgenden Schritte aus, um ein Angebot zum Aktivieren des Kunden Schlüssels zu übermitteln:
  
1. Melden Sie sich unter Verwendung eines Geschäfts-oder Schul Kontos mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation beim [Microsoft-Portal](https://fasttrack.microsoft.com/)an.
    
2. Nachdem Sie sich angemeldet haben, navigieren Sie zum **Dashboard**.
    
3. Wählen Sie **Angebote**aus, und sehen Sie sich die Liste der aktuellen Angebote an.
    
4. Wählen Sie **Weitere Informationen** für das Angebot aus, das für Sie gilt: 
    
  - **Exchange Online und Skype for Business:** Wählen Sie **Weitere Informationen** zum **Kundenschlüssel für das Exchange** -Angebot aus. 
    
  - **SharePoint Online und OneDrive for Business:** **Weitere Informationen finden Sie** unter **Kundenschlüssel für SharePoint und OneDrive for Business-** Angebot. 
    
5. Klicken Sie auf der Seite **Angebotsdetails** auf **Anforderung erstellen**.
    
6. Füllen Sie alle relevanten Details und erforderlichen Informationen im Angebotsformular aus. Achten Sie besonders auf Ihre Auswahl für die Mitarbeiter Ihrer Organisation, die die dauerhafte und irreversible Zerstörung von Verschlüsselungsschlüsseln und Daten genehmigen möchten. Nachdem Sie das Formular ausgefüllt haben, **** klicken Sie auf Absenden.
    
    Dieser Vorgang kann bis zu fünf Werktage dauern, nachdem Microsoft Ihre Anforderung benachrichtigt hat.
    
7. Weiter unten im Abschnitt obligatorische Aufbewahrungsdauer.
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a>Registrieren von Azure-Abonnements für die Verwendung eines obligatorischen Aufbewahrungszeitraums
<a name="RegisterSubsforMRP"> </a>

Der vorübergehende oder dauerhafte Verlust von Verschlüsselungsschlüsseln kann sehr störend oder sogar katastrophal für den Dienstvorgang sein und zu Datenverlusten führen. Aus diesem Grund erfordern die mit dem Kundenschlüssel verwendeten Ressourcen einen starken Schutz. Alle Azure-Ressourcen, die mit dem Kundenschlüssel verwendet werden, bieten Schutzmechanismen jenseits der Standardkonfiguration. Azure-Abonnements können auf eine Weise gekennzeichnet oder registriert werden, die eine sofortige und unwiderrufliche Stornierung verhindert. Dies wird als Registrierung für eine obligatorische Aufbewahrungsdauer bezeichnet. Die erforderlichen Schritte zum Registrieren von Azure-Abonnements für einen obligatorischen Aufbewahrungszeitraum erfordern eine Zusammenarbeit mit dem Office 365-Team. Dieser Prozess kann zwischen einem und fünf Werktagen dauern. Zuvor wurde dies auch als "nicht abbrechen" bezeichnet.
  
Bevor Sie sich mit dem Office 365-Team in Verbindung setzen, müssen Sie für jedes Azure-Abonnement, das Sie mit dem Kundenschlüssel verwenden, die folgenden Schritte ausführen:
  
1. Melden Sie sich bei Ihrem Azure-Abonnement mit Azure PowerShell an. Weitere Informationen finden Sie unter [Anmelden mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
2. Führen Sie das Cmdlet Register-AzureRmProviderFeature aus, um Ihre Abonnements für die Verwendung eines obligatorischen Aufbewahrungszeitraums zu registrieren.
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. Wenden Sie sich an Microsoft, um den Prozess abzuschließen. Wenden Sie sich für das SharePoint-und OneDrive for Business-Team an [Spock@microsoft.com](mailto:spock@microsoft.com). Für Exchange Online und Skype for Business wenden Sie sich an [exock@microsoft.com](mailto:exock@microsoft.com). Die Vereinbarung zum Service Level (SLA) für den Abschluss dieses Vorgangs beträgt fünf Werktage, nachdem Microsoft benachrichtigt (und überprüft) wurde, dass Sie Ihre Abonnements für die Verwendung eines obligatorischen Aufbewahrungszeitraums registriert haben. Fügen Sie Folgendes in Ihre e-Mail ein:
    
    **Betreff**: Kundenschlüssel für \< *den vollqualifizierten Domänennamen Ihres Mandanten*\> 
    
    **Body**: Abonnement-IDs, für die Sie den obligatorischen Aufbewahrungszeitraum abschließen möchten. 
    
4. Sobald Sie von Microsoft eine Benachrichtigung erhalten haben, dass die Registrierung abgeschlossen ist, überprüfen Sie den Status Ihrer Registrierung, indem Sie das Cmdlet Get-AzureRmProviderFeature wie folgt ausführen:
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. Führen Sie den folgenden Befehl aus, um den Vorgang abzuschließen, nachdem Sie sichergestellt haben, dass die Eigenschaft **Registrierungsstatus** des Cmdlets Get-AzureRmProviderFeature den Wert **registered**zurückgibt:
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a>Erstellen eines Premium-Azure-Schlüsseldepots in jedem Abonnement
<a name="CreateKeyVault"> </a>

Die Schritte zum Erstellen eines Schlüssel Tresors sind unter [Erste Schritte mit Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/)dokumentiert, in dem Sie die Installation und Einführung von Azure PowerShell, das Herstellen einer Verbindung mit Ihrem Azure-Abonnement, das Erstellen einer Ressourcengruppe und das Erstellen eines Schlüsseldepots in diesem Ressourcengruppe.
  
Wenn Sie einen schlüsseltresor erstellen, müssen Sie eine SKU wählen: entweder Standard oder Premium. Die Standard-SKU ermöglicht das Schützen von Azure Key Vault-Schlüsseln mit Software – es gibt keinen Sicherheitsmodul-Schlüsselschutz (HSM) – und die Premium-SKU ermöglicht die Verwendung von HSMs für den Schutz von Schlüsseltresor Schlüsseln. Der Kundenschlüssel akzeptiert Schlüsseldepots, die entweder SKU verwenden, obwohl Microsoft dringend empfiehlt, nur die Premium-SKU zu verwenden. Die Kosten für Vorgänge mit Schlüsseln beider Typen sind identisch, daher ist der einzige Kostenunterschied die Kosten pro Monat für jeden HSM-geschützten Schlüssel. Details finden Sie unter [Key Vault Pricing](https://azure.microsoft.com/pricing/details/key-vault/) . 
  
> [!IMPORTANT]
> Verwenden Sie die Premium-SKU-Schlüsseldepots und HSM-Protected-Schlüssel für Produktionsdaten, und verwenden Sie nur Standard-SKU-Schlüsseldepots und-Schlüssel zu Test-und Validierungszwecken. 
  
Erstellen Sie für jeden Office 365-Dienst, mit dem Sie den Kundenschlüssel verwenden, in jedem der beiden Azure-Abonnements, die Sie erstellt haben, einen schlüsseltresor. Wenn Sie beispielsweise nur für Exchange Online und Skype for Business oder SharePoint Online und OneDrive for Business tätig sind, erstellen Sie nur ein paar von Vaults. Zum Aktivieren des Kunden Schlüssels für Exchange Online und SharePoint Online erstellen Sie zwei schlüsseltresor Paare.
  
Verwenden Sie eine Benennungskonvention für Schlüssel Tresore, die die vorgesehene Verwendung der DEP widerspiegelt, mit der Sie die Tresore verknüpfen möchten. Weitere Informationen finden Sie im Abschnitt bewährte Methoden unter Empfehlungen zur Benennungskonvention.
  
Erstellen Sie eine separate, paarweise Reihe von Vaults für jede Daten Verschlüsselungsrichtlinie. Für Exchange Online wird der Bereich einer Daten Verschlüsselungsrichtlinie von Ihnen ausgewählt, wenn Sie die Richtlinie dem Postfach zuweisen. Einem Postfach kann nur eine Richtlinie zugewiesen werden, und Sie können bis zu 50 Richtlinien erstellen. Für SharePoint Online ist der Bereich einer Richtlinie alle Daten innerhalb einer Organisation an einem geografischen Standort oder Geo.
  
Für die Erstellung von Schlüsseldepots ist außerdem die Erstellung von Azure-Ressourcengruppen erforderlich, da für Schlüsseldepots Speicherkapazität (obwohl sehr klein) erforderlich ist und die Schlüsseldepot Protokollierung, falls aktiviert, auch gespeicherte Daten generiert. Als bewährte Methode empfiehlt Microsoft die Verwendung separater Administratoren zum Verwalten der einzelnen Ressourcengruppen, wobei die Verwaltung mit den Administratoren ausgerichtet ist, die alle zugehörigen Kundenschlüssel Ressourcen verwalten.
  
> [!IMPORTANT]
> Um die Verfügbarkeit zu maximieren, sollten sich Ihre Schlüsseldepots in Regionen in der Umgebung Ihres Office 365-Diensts befinden. Wenn sich Ihre Exchange Online-Organisation beispielsweise in Nordamerika befindet, platzieren Sie Ihre Schlüsseldepots in Nordamerika. Wenn sich Ihre Exchange Online-Organisation in Europa befindet, legen Sie Ihre Schlüsseldepots in Europa ab.<br/>Verwenden Sie ein gemeinsames Präfix für Schlüssel Tresore, und schließen Sie eine Abkürzung für die Verwendung und den Umfang des Schlüssel Tresors und der Schlüssel ein (beispielsweise für den Contoso SharePoint-Dienst, in dem sich die Tresore in Nordamerika befinden werden, ein mögliches paar von Namen ist contoso-O365SP-NA-VaultA1 und Contoso-O365SP-NA-VaultA2. Vault-Namen sind global eindeutige Zeichenfolgen innerhalb von Azure, daher müssen Sie möglicherweise Variationen Ihrer gewünschten Namen ausprobieren, falls die gewünschten Namen bereits von anderen Azure-Kunden beansprucht werden. 2017 Vault-Namen können nicht geändert werden, daher empfiehlt es sich, einen schriftlichen Plan für das Setup zu haben und eine zweite Person zu verwenden, um zu überprüfen, ob der Plan ordnungsgemäß ausgeführt wird.<br/>Erstellen Sie nach Möglichkeit Ihre Tresore in nicht gepaarten Regionen. Paarweise gePaarte Azure-Regionen bieten eine hohe Verfügbarkeit für Dienst fehlerdomänen. Daher können regionale Paare als Sicherungs Region des jeweils anderen betrachtet werden. Dies bedeutet, dass eine Azure-Ressource, die in einem Bereich eingefügt wird, automatisch eine Fehlertoleranz durch den gepaarten Bereich erlangt. Aus diesem Grund wird durch das Auswählen von Regionen für zwei Tresore, die in einem DEP verwendet werden, in dem die Regionen gekoppelt sind, nur eine Gesamtanzahl von zwei Verfügbarkeits Regionen verwendet. Die meisten Geographen haben nur zwei Regionen, daher ist es noch nicht möglich, nicht gepaarte Regionen auszuwählen. Wählen Sie nach Möglichkeit zwei nicht gepaarte Regionen für die beiden Tresore aus, die mit einem DEP verwendet werden. Dies profitiert von insgesamt vier Verfügbarkeits Regionen. Weitere Informationen finden Sie unter [Business Continuity and Disaster Recovery (BCDR): Azure pairEd Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current List of Regional Pairs. 
  
### <a name="assign-permissions-to-each-key-vault"></a>Zuweisen von Berechtigungen zu jedem schlüsseltresor
<a name="KeyVaultPerms"> </a>

Für jeden schlüsseltresor müssen Sie je nach Implementierung drei separate Berechtigungssätze für den Kundenschlüssel definieren. Sie müssen beispielsweise einen Satz von Berechtigungen für jede der folgenden definieren:
  
- **Wichtige Vault-Administratoren** , die die tägliche Verwaltung Ihres Schlüsseldepots für Ihre Organisation ausführen. Zu diesen Aufgaben gehört das sichern, erstellen, abrufen, importieren, auflisten und wiederherstellen. 
    
    > [!IMPORTANT]
    > Der Satz von Berechtigungen, die schlüsseltresor-Administratoren zugewiesen sind, enthält nicht die Berechtigung zum Löschen von Schlüsseln. Dies ist beabsichtigt und eine wichtige Vorgehensweise. Das Löschen von Verschlüsselungsschlüsseln erfolgt in der Regel nicht, da Daten dauerhaft gelöscht werden. Als bewährte Methode sollten Sie diese Berechtigung nicht standardmäßig den schlüsseltresor-Administratoren erteilen. Behalten Sie stattdessen diese für wichtige Vault-Mitwirkende bei, und weisen Sie Sie nur kurzfristig einem Administrator zu, wenn ein klares Verständnis der Konsequenzen verstanden wird. 
  
    Wenn Sie diesen Berechtigungen einem Benutzer in Ihrer Office 365-Organisation zuweisen möchten, melden Sie sich bei Ihrem Azure-Abonnement mit Azure PowerShell an. Weitere Informationen finden Sie unter [Anmelden mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
- Führen Sie das Cmdlet Set-AzureRmKeyVaultAccessPolicy aus, um die erforderlichen Berechtigungen zuzuweisen.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  Beispiel:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- **Wichtige Vault** -Mitwirkende, die Berechtigungen für den Azure-schlüsseltresor selbst ändern können. Sie müssen diese Berechtigungen ändern, wenn Mitarbeiter verlassen oder Ihrem Team beitreten, oder in der äußerst seltenen Situation, dass die schlüsseltresor-Administratoren berechtigterweise die Berechtigung zum Löschen oder Wiederherstellen eines Schlüssels benötigen. Dieser Gruppe von wichtigen Vault-Mitwirkenden muss die Rolle **** "Mitwirkende" in Ihrem schlüsseltresor erteilt werden. Sie können diese Rolle mithilfe des Azure-Ressourcen-Managers zuweisen. Weitere Informationen finden Sie unter [Verwenden der rollenbasierten Zugriffssteuerung zum Verwalten des Zugriffs auf Ihre Azure-Abonnement Ressourcen](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). Der Administrator, der ein Abonnement erstellt, hat diesen Zugriff implizit sowie die Möglichkeit, andere Administratoren der Rolle mitWirkender zuzuweisen.
    
- Wenn Sie den Kundenschlüssel mit Exchange Online und Skype for Business verwenden möchten, müssen Sie Office 365 die Berechtigung erteilen, das Schlüsseldepot im Namen von Exchange Online und Skype for Business zu verwenden. Wenn Sie den Kundenschlüssel mit SharePoint Online und OneDrive for Business verwenden möchten, müssen Sie entsprechend die Berechtigung für das Office 365 hinzufügen, um das Schlüsseldepot im Namen von SharePoint Online und OneDrive for Business zu verwenden. Führen Sie das Cmdlet **Set-AzureRmKeyVaultAccessPolicy** mit der folgenden Syntax aus, um die Berechtigung für Office 365 zu erteilen: 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    Wobei Folgendes gilt:
    
  - *vaultname* ist der Name des Schlüsseldepots, den Sie erstellt haben. 
    
  - Ersetzen Sie *Office 365* -ID für Exchange Online und Skype for Business durch`00000002-0000-0ff1-ce00-000000000000`
    
  - Ersetzen Sie *Office 365* -ID für SharePoint Online und OneDrive for Business durch`00000003-0000-0ff1-ce00-000000000000`
    
  Beispiel: Festlegen von Berechtigungen für Exchange Online und Skype for Business:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  Beispiel: Festlegen von Berechtigungen für SharePoint Online und OneDrive for Business
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a>Aktivieren und bestätigen des weichen Löschvorganges in ihren Schlüsseldepots
<a name="SoftDelete"> </a>

Wenn Sie Ihre Schlüssel schnell wiederherstellen können, ist die Wahrscheinlichkeit eines erweiterten Dienstausfalls aufgrund versehentlich oder in böswilliger Absicht gelöschter Schlüssel geringer. Sie müssen diese Konfiguration, die als weiche Löschung bezeichnet wird, aktivieren, bevor Sie Ihre Schlüssel mit dem Kundenschlüssel verwenden können. Durch Aktivieren von Soft Delete können Sie Schlüssel oder Depots innerhalb von 90 Tagen nach dem Löschen wiederherstellen, ohne Sie aus der Sicherung wiederherstellen zu müssen.
  
Führen Sie die folgenden Schritte aus, um die weiche Löschung in ihren Schlüsseldepots zu aktivieren:
  
1. Melden Sie sich bei Ihrem Azure-Abonnement mit Windows PowerShell an. Weitere Informationen finden Sie unter [Anmelden mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).
    
2. Führen Sie das Cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) aus. In diesem Beispiel ist *vaultname* der Name des Schlüssel Tresors, für den Sie das weiche löschen aktivieren: 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. Bestätigen Sie, dass die weiche Löschung für das Schlüsseldepot konfiguriert ist, indem Sie das Cmdlet **Get-AzureRmKeyVault** ausführen. Wenn Soft Delete für den schlüsseltresor ordnungsgemäß konfiguriert ist, ist der weiche Löschvorgang aktiviert? -Eigenschaft gibt den Wert **true**zurück: 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a>Hinzufügen eines Schlüssels zu jedem Schlüsseldepot durch Erstellen oder Importieren eines Schlüssels
<a name="AddKeystoKeyVault"> </a>

Es gibt zwei Möglichkeiten, einem Azure-Schlüsseltresor Schlüssel hinzuzufügen. Sie können einen Schlüssel direkt im Key Vault erstellen, oder Sie können einen Schlüssel importieren. Das Erstellen eines Schlüssels direkt im Schlüsseltresor ist die unkompliziertere Methode, während der Import eines Schlüssels die vollständige Kontrolle über die Generierung des Schlüssels bietet.
  
Führen Sie das [Add-AzureKeyVaultKey-](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) Cmdlet wie folgt aus, um einen Schlüssel direkt in Ihrem schlüsseltresor zu erstellen: 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

Wobei Folgendes gilt:
  
-  *vaultname* ist der Name des Schlüssel Tresors, in dem Sie den Schlüssel erstellen möchten. 
    
-  *keyName* ist der Name, den Sie dem neuen Schlüssel geben möchten. 
    
    > [!TIP]
    > Benennen Sie Schlüssel unter Verwendung einer ähnlichen Benennungskonvention wie oben beschrieben für Schlüsseldepots. Auf diese Weise wird in Tools, die nur den Schlüsselnamen anzeigen, die Zeichenfolge selbsterklärend. 
  
- Wenn Sie den Schlüssel mit einem HSM schützen möchten, stellen Sie sicher, dass Sie **HSM** als Wert des Parameters _Destination_ angeben, andernfalls geben Sie **Software**an.
    
Beispiel:
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

Um einen Schlüssel direkt in Ihr Schlüsseldepot zu importieren, benötigen Sie ein Thales nShield-Hardware Sicherheitsmodul.
  
Einige Organisationen bevorzugen diesen Ansatz, um die Herkunft Ihrer Schlüssel zu bestimmen, und die diese Methode stellt auch Folgendes bereit:
  
- Das für den Import verwendete Toolset umfasst die Bescheinigung von Thales, dass der Schlüsselaustauschschlüssel (KEK), der zum Verschlüsseln des von Ihnen generierten Schlüssels verwendet wird, nicht exportierbar ist und innerhalb eines echten HSM generiert wird, das von Thales hergestellt wurde.
    
- Das Toolset enthält die Bescheinigung von Thales, dass die Azure Key Vault-Sicherheitswelt auch auf einem echten HSM von Thales hergestellt wurde. Diese Bescheinigung weist darauf hin, dass Microsoft auch echte Thales-Hardware verwendet.
    
Erkundigen Sie sich bei ihrer Sicherheitsgruppe, ob die obigen Bescheinigungen erforderlich sind. Ausführliche Schritte zum Erstellen eines lokalen Schlüssels und zum Importieren dieser Schlüssel in ihren schlüsseltresor finden Sie unter [Vorgehensweise: generieren und übertragen von HSM-geschützten Schlüsseln für Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Verwenden Sie die Azure-Anweisungen, um einen Schlüssel in jedem schlüsseltresor zu erstellen.
  
### <a name="check-the-recovery-level-of-your-keys"></a>Überprüfen der Wiederherstellungsebene der Schlüssel
<a name="CheckKeyRecoveryLevel"> </a>

Office 365 erfordert, dass das Azure Key Vault-Abonnement auf nicht abbrechen festgelegt ist und dass die vom Kundenschlüssel verwendeten Schlüssel weiche Löschfunktion aktiviert haben. Sie können dies überprüfen, indem Sie sich die Wiederherstellungs Stufe für Ihre Schlüssel ansehen.
  
Führen Sie zum Überprüfen der Wiederherstellungsebene eines Schlüssels in Azure PowerShell das Cmdlet Get-AzureKeyVaultKey wie folgt aus:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

Wenn die Eigenschaft wiederHerstellungsEbene einen anderen Wert als " _wieder_ **herstellbare + ProtectedSubscription**" zurückgibt, müssen Sie dieses Thema überprüfen und sicherstellen, dass Sie alle Schritte ausgeführt haben, um das Abonnement auf die Liste nicht abbrechen zu setzen und , dass für jedes Schlüsseldepot der Soft Delete aktiviert ist.
  
### <a name="backup-azure-key-vault"></a>Azure-Schlüsseltresor sichern
<a name="BackupAzureKeyVaultkeys"> </a>

Führen Sie sofort nach dem Erstellen oder Ändern eines Schlüssels eine Sicherung aus, und speichern Sie Kopien der Sicherung, sowohl online als auch offline. Offline Kopien sollten nicht mit einem Netzwerk verbunden sein, beispielsweise in einer physischen oder kommerziellen Speicheranlage. Mindestens eine Kopie der Sicherung sollte an einem Speicherort gespeichert werden, auf den bei einem Notfall zugegriffen werden kann. Die Sicherungs BLOBs sind das einzige Mittel zur Wiederherstellung von Schlüsselmaterial, wenn ein Schlüsseltresor dauerhaft zerstört oder anderweitig nicht mehr funktionsfähig ist. Schlüssel, die sich außerhalb von Azure Key Vault befinden und in Azure Key Vault importiert wurden, können nicht als Sicherung verwendet werden, da die Metadaten, die für den Kundenschlüssel erforderlich sind, nicht mit dem externen Schlüssel vorhanden sind. Nur eine Sicherung aus Azure Key Vault kann für Wiederherstellungsvorgänge mit Kundenschlüssel verwendet werden. Daher ist es wichtig, dass eine Sicherung von Azure Key Vault durchgeführt wird, nachdem ein Schlüssel hochgeladen oder erstellt wurde.
  
Führen Sie das Cmdlet [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) wie folgt aus, um eine Sicherung eines Azure Key Vault-Schlüssels zu erstellen:
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

Stellen Sie sicher, dass die Ausgabedatei `.backup`das Suffix verwendet.
  
Die aus diesem Cmdlet resultierende Ausgabedatei ist verschlüsselt und kann nicht außerhalb von Azure Key Vault verwendet werden. Die Sicherung kann nur für das Azure-Abonnement wiederhergestellt werden, von dem die Sicherung ausgeführt wurde.
  
> [!TIP]
> Wählen Sie für die Ausgabedatei eine Kombination aus Vault-und Schlüsselnamen aus. Dadurch wird der Dateiname selbsterklärend. Außerdem wird sichergestellt, dass die Namen der Sicherungsdateien nicht kollidieren. 
  
Beispiel:
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a>Validieren von Azure Key Vault-Konfigurationseinstellungen
<a name="Validateconfiguration"> </a>

Das Durchführen einer Validierung vor dem Verwenden von Schlüsseln in einer DEP ist optional, wird jedoch dringend empfohlen. Wenn Sie beispielsweise die in diesem Thema beschriebenen Schritte zum Einrichten Ihrer Schlüssel und Tresore verwenden, sollten Sie die Integrität ihrer Azure Key Vault-Ressourcen überprüfen, bevor Sie den Kundenschlüssel konfigurieren.
  
So überprüfen Sie, ob für die Schlüssel Get-, wrapKey-und unwrapKey-Vorgänge aktiviert sind:
  
Führen [Sie das Get-AzureRmKeyVault-](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) Cmdlet wie folgt aus: 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

Suchen Sie in der Ausgabe nach den entsprechenden Zugriffsrichtlinien und der Exchange Online-Identität (GUID) oder der SharePoint Online-Identität (GUID). Alle drei obigen Berechtigungen müssen unter Berechtigungen für Schlüssel angezeigt werden.
  
Wenn die Konfiguration der Zugriffsrichtlinie falsch ist, führen Sie das Cmdlet Set-AzureRmKeyVaultAccessPolicy wie folgt aus:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

Beispielsweise für Exchange Online und Skype for Business:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

Beispielsweise für SharePoint Online und OneDrive for Business:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

Führen Sie das [Get-AzureKeyVaultKey-](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) Cmdlet wie folgt aus, um zu überprüfen, ob ein Ablaufdatum für die Schlüssel festgelegt ist: 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

Ein abgelaufener Schlüssel kann nicht vom Kundenschlüssel verwendet werden, und Vorgänge, die mit einem abgelaufenen Schlüssel versucht wurden, können fehlschlagen und zu einem Dienstausfall führen. Es wird dringend empfohlen, dass Schlüssel, die mit dem Kundenschlüssel verwendet werden, kein Ablaufdatum aufweisen. Ein Ablaufdatum, einmal festgelegt, kann nicht entfernt werden, kann aber in ein anderes Datum geändert werden. Wenn ein Schlüssel verwendet werden muss, der ein Ablaufdatum festgelegt hat, ändern Sie den Ablaufwert in 12/31/9999. Schlüssel mit einem Ablaufdatum, das auf ein anderes Datum als 12/31/9999 festgelegt ist, führen keine Office 365-Validierung aus.
  
Wenn Sie ein Ablaufdatum ändern möchten, das auf einen anderen Wert als 12/31/9999 festgelegt wurde, führen Sie das Cmdlet [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) wie folgt aus: 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> Legen Sie keine Ablaufdaten für Verschlüsselungsschlüssel fest, die Sie mit dem Kundenschlüssel verwenden. 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a>Abrufen des URIs für jeden Azure Key Vault-Schlüssel
<a name="GetKeyURI"> </a>

Nachdem Sie alle Schritte in Azure ausgeführt haben, um Ihre Schlüsseldepots einzurichten und Ihre Schlüssel hinzugefügt haben, führen Sie den folgenden Befehl aus, um den URI für den Schlüssel in jedem schlüsseltresor abzurufen. Sie müssen diese URIs verwenden, wenn Sie jede DEP später erstellen und zuweisen, diese Informationen also an einem sicheren Ort speichern. Denken Sie daran, diesen Befehl einmal für jeden schlüsseltresor auszuführen.
  
In Azure PowerShell:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a>Office 365: Einrichten des Kunden Schlüssels für Exchange Online und Skype for Business
<a name="AzureSteps"> </a>

Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Aufgaben zum Einrichten von Azure Key Vault abgeschlossen haben. Weitere Informationen finden Sie unter [Complete Tasks in Azure Key Vault und Microsoft für den Kundenschlüssel](controlling-your-data-using-customer-key.md#AzureSteps) . 
  
Um den Kundenschlüssel für Exchange Online und Skype for Business einzurichten, müssen Sie diese Schritte ausführen, indem Sie Remote eine Verbindung zu Exchange Online mit Windows PowerShell herstellen.
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a>Erstellen einer Daten Verschlüsselungsrichtlinie für die Verwendung mit Exchange Online und Skype for Business
<a name="CreateDEP4EXOSkype"> </a>

Eine DEP ist mit einem Schlüsselsatz verknüpft, der in Azure Key Vault gespeichert ist. Sie weisen einem Postfach in Office 365 eine DEP zu. Office 365 verwendet dann die in der Richtlinie angegebenen Schlüssel, um das Postfach zu verschlüsseln. Zum Erstellen der datenAUSFÜHRUNGSverHINDERung benötigen Sie die wichtigsten Vault-URIs, die Sie zuvor abgerufen haben. Anweisungen dazu finden Sie unter [Abrufen des URIs für jeden Azure Key Vault-Schlüssel](controlling-your-data-using-customer-key.md#GetKeyURI) . 
  
Denken Sie daran! Wenn Sie eine DEP erstellen, geben Sie zwei Schlüssel an, die sich in zwei verschiedenen Azure-Schlüsseldepots befinden. Stellen Sie sicher, dass sich diese Schlüssel in zwei getrennten Azure-Regionen befinden, um die Geo-Redundanz sicherzustellen.
  
Führen Sie die folgenden Schritte aus, um die DEP zu erstellen:
  
1. Stellen Sie auf Ihrem lokalen Computer über ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation eine [Verbindung zu Exchange Online PowerShell her](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , indem Sie Windows PowerShell öffnen und den folgenden Befehl ausführen. 
    
   ```
   $UserCredential = Get-Credential
   ```

2. Geben Sie im Dialogfeld für die Windows PowerShell-Anmelde informationsAnforderung Ihre geschäftlichen oder Schulkonto Informationen ein, klicken Sie auf **OK**, und geben Sie den folgenden Befehl ein. 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. Führen Sie den folgenden Befehl aus.
    
   ```
   Import-PSSession $Session
   ```

4. Verwenden Sie zum Erstellen einer datenAUSFÜHRUNGSverHINDERung das Cmdlet New-DataEncryptionPolicy, indem Sie den folgenden Befehl eingeben.
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   Wobei Folgendes gilt:
    
   -  *PolicyName* ist der Name, den Sie für die Richtlinie verwenden möchten. Namen dürfen keine Leerzeichen enthalten. Beispiel: USA_mailboxes. 
    
   -  *PolicyDescription* ist eine benutzerfreundliche Beschreibung der Richtlinie, mit der Sie sich an die Richtlinie erinnern können. Sie können Leerzeichen in die Beschreibung aufnehmen. Beispiel: Stammschlüssel für Postfächer in den USA und dessen Territorien. 
    
   -  *KeyVaultURI1* ist der URI für den ersten Schlüssel in der Richtlinie. Beispiel: https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01. 
    
   -  *KeyVaultURI2* ist der URI für den zweiten Schlüssel in der Richtlinie. Beispiel: https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Trennen Sie die beiden URIs durch ein Komma und ein Leerzeichen. 
    
   Beispiel:
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a>Zuweisen einer DEP zu einem Postfach
<a name="assignDEPtomailbox"> </a>

Weisen Sie die DEP mithilfe des Cmdlets Set-Mailbox einem Postfach zu. Nachdem Sie die Richtlinie zugewiesen haben, kann Office 365 das Postfach mit dem in der DEP angegebenen Schlüssel verschlüsseln.
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

Wobei *MailboxIdParameter* ein Postfach angibt. Weitere Informationen zum Cmdlet Set-Mailbox finden Sie unter [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).
  
### <a name="validate-mailbox-encryption"></a>ÜberPrüfen der Postfachverschlüsselung
<a name="validatemailboxencryption"> </a>

Das verSchlüsseln eines Postfachs kann einige Zeit in Anspruch nehmen. Bei der erstmaligen Richtlinienzuweisung muss das Postfach die Verschiebung von einer Datenbank in eine andere abschließen, bevor der Dienst das Postfach verschlüsseln kann. Es wird empfohlen, dass Sie 72 Stunden warten, bevor Sie versuchen, die Verschlüsselung zu überprüfen, nachdem Sie eine DEP geändert haben oder wenn Sie eine DEP zum ersten Mal einem Postfach zuweisen.
  
Verwenden Sie das Cmdlet Get-MailboxStatistics, um zu ermitteln, ob ein Postfach verschlüsselt ist.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

Die isEncrypted-Eigenschaft gibt den Wert **true** zurück, wenn das Postfach verschlüsselt ist, und der Wert **false** , wenn das Postfach nicht verschlüsselt ist. 

Die Zeit zum Abschließen der Postfachverschiebungen hängt von der Anzahl der Postfächer ab, denen Sie eine datenAUSFÜHRUNGSverHINDERung zum ersten Mal zuweisen, sowie der Größe der Postfächer. Wenn die Postfächer nach einer Woche ab dem Zeitpunkt, zu dem Sie die DEP zugewiesen haben, nicht verschlüsselt wurden, initiieren Sie mithilfe des Cmdlets New-MoveRequest eine Postfachverschiebung für die unverschlüsselten Postfächer.

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a>Office 365: Einrichten des Kunden Schlüssels für SharePoint Online und OneDrive for Business
<a name="AzureSteps"> </a>

Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Aufgaben zum Einrichten von Azure Key Vault abgeschlossen haben. Weitere Informationen finden Sie unter [Complete Tasks in Azure Key Vault und Microsoft für den Kundenschlüssel](controlling-your-data-using-customer-key.md#AzureSteps) . 
  
Zum Einrichten des Kunden Schlüssels für SharePoint Online und OneDrive for Business müssen Sie diese Schritte ausführen, indem Sie Remote eine Verbindung mit SharePoint Online mit Windows PowerShell herstellen.
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a>Erstellen Sie eine Daten Verschlüsselungsrichtlinie (DEP) für jede SharePoint Online-und OneDrive for Business-Geo
<a name="CreateDEP4SPOODfB"> </a>

Eine DEP ist mit einem Schlüsselsatz verknüpft, der in Azure Key Vault gespeichert ist. Sie wenden eine DEP auf alle Daten an einem geografischen Standort an. Wenn Sie das Multi-Geo-Feature von Office 365 (derzeit in der Vorschau) verwenden, können Sie eine DEP pro Geo erstellen. Wenn Sie nicht Multi-Geo verwenden, können Sie eine datenAUSFÜHRUNGSverHINDERung in Office 365 für die Verwendung mit SharePoint Online und OneDrive for Business erstellen. Office 365 verwendet dann die Schlüssel, die in der DEP identifiziert wurden, um Ihre Daten in dieser Geo zu verschlüsseln. Zum Erstellen der datenAUSFÜHRUNGSverHINDERung benötigen Sie die wichtigsten Vault-URIs, die Sie zuvor abgerufen haben. Anweisungen dazu finden Sie unter [Abrufen des URIs für jeden Azure Key Vault-Schlüssel](controlling-your-data-using-customer-key.md#GetKeyURI) . 
  
Denken Sie daran! Wenn Sie eine DEP erstellen, geben Sie zwei Schlüssel an, die sich in zwei verschiedenen Azure-Schlüsseldepots befinden. Stellen Sie sicher, dass sich diese Schlüssel in zwei getrennten Azure-Regionen befinden, um die Geo-Redundanz sicherzustellen.
  
Zum Erstellen einer datenAUSFÜHRUNGSverHINDERung müssen Sie mithilfe von Windows PowerShell eine Remoteverbindung mit SharePoint Online herstellen.
  
1. Stellen Sie auf Ihrem lokalen Computer über ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation eine [Verbindung mit SharePoint Online PowerShell her](https://technet.microsoft.com/library/fp161372.aspx).
    
2. Führen Sie in der Microsoft SharePoint Online-Verwaltungsshell das Cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) wie folgt aus: 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   Wenn Sie die DEP registrieren, beginnt die Verschlüsselung mit den Daten im Geo. Dies kann einige Zeit in Anspruch nehmen.
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a>Überprüfen der Verschlüsselung von Gruppen Websites, Team Websites und OneDrive für Unternehmen
<a name="validateencryptionSPO"> </a>

Sie können den Status der Verschlüsselung überprüfen, indem Sie das Cmdlet Get-SPODataEncryptionPolicy wie folgt ausführen:
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

Die Ausgabe dieses Cmdlets umfasst Folgendes:
  
- Der URI des Primärschlüssels.
    
- Der URI des sekundären Schlüssels.
    
- Der Verschlüsselungsstatus für den Geo. Mögliche Status:
    
  - Nicht **registriert:** Die Kundenschlüssel Verschlüsselung wurde noch nicht angewendet. 
    
  - **Registrierung:** Die Kundenschlüssel Verschlüsselung wurde angewendet, und Ihre Dateien werden verschlüsselt. Wenn sich Ihr Geo in diesem Zustand befindet, werden Ihnen auch Informationen darüber angezeigt, wie viel Prozent der Websites in der Geo abgeschlossen sind, damit Sie den Verschlüsselungs Fortschritt überwachen können. 
    
  - **Registriert:** Die Kundenschlüssel Verschlüsselung wurde angewendet, und alle Dateien in allen Websites wurden verschlüsselt. 
    
  - **Rolling:** Ein Schlüssel Roll wird ausgeführt. Wenn sich Ihr Geo in diesem Zustand befindet, werden Ihnen auch Informationen darüber angezeigt, wie viel Prozent der Websites den Schlüssel Rollvorgang abgeschlossen haben, damit Sie den Fortschritt überwachen können. 
    
## <a name="managing-customer-key-for-office-365"></a>Verwalten des Kunden Schlüssels für Office 365
<a name="ManageCustomerKey"> </a>

Nachdem Sie den Kundenschlüssel für Office 365 eingerichtet haben, können Sie diese zusätzlichen Verwaltungsaufgaben ausführen.
  
- [Wiederherstellen von Azure Key Vault-Schlüsseln](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [Rollen oder Drehen eines Schlüssels im Azure Key Vault, den Sie mit dem Kundenschlüssel verwenden](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [Verwalten von schlüsseltresor-Berechtigungen](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [Bestimmen der einem Postfach zugewiesenen DEP](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a>Wiederherstellen von Azure Key Vault-Schlüsseln
<a name="RestoreAzureKeyVaultKeys"> </a>

Verwenden Sie vor dem Ausführen einer Wiederherstellung die von Soft Delete bereitgestellten Wiederherstellungsfunktionen. Für alle Schlüssel, die mit dem Kundenschlüssel verwendet werden, muss das weiche löschen aktiviert sein. Soft Delete fungiert wie ein Papierkorb und ermöglicht die Wiederherstellung bis zu 90 Tage ohne Wiederherstellung. Die Wiederherstellung sollte nur unter extremen oder ungewöhnlichen Umständen erforderlich sein, beispielsweise wenn der Schlüssel-oder schlüsseltresor verloren geht. Wenn Sie einen Schlüssel zur Verwendung mit dem Kundenschlüssel wiederherstellen müssen, führen Sie in Azure PowerShell das Cmdlet Restore-AzureKeyVaultKey wie folgt aus:
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

Beispiel:
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

Wenn bereits ein Schlüssel mit demselben Namen im schlüsseltresor vorhanden ist, schlägt der Wiederherstellungsvorgang fehl. Restore-AzureKeyVaultKey stellt alle Schlüssel Versionen und alle Metadaten für den Schlüssel einschließlich des Schlüssel namens wieder her.
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a>Rollen oder Drehen eines Schlüssels im Azure Key Vault, den Sie mit dem Kundenschlüssel verwenden
<a name="RollCKkey"> </a>

Rollende Schlüssel sind weder für Azure Key Vault noch für einen Kundenschlüssel erforderlich. Außerdem sind Schlüssel, die mit einem HSM geschützt sind, nahezu unmöglich zu kompromittieren. Selbst wenn ein Stammschlüssel im Besitz eines böswilligen Akteurs war, gibt es keine Möglichkeit, diese zum Entschlüsseln von Daten zu verwenden, da nur Office 365 Code die Verwendung dieses Schlüssels weiß. Das Rollen eines Schlüssels wird jedoch vom Kundenschlüssel unterstützt.
  
> [!CAUTION]
> Rollen Sie nur einen Verschlüsselungsschlüssel, den Sie mit dem Kundenschlüssel verwenden, wenn ein klarer technischer Grund vorliegt oder eine Compliance-Anforderung vorschreibt, dass Sie den Schlüsselrollen müssen. Löschen Sie außerdem keine Schlüssel, die Richtlinien zugeordnet sind oder waren. Wenn Sie Ihre Schlüsselrollen, werden Inhalte mit den vorherigen Schlüsseln verschlüsselt. Wenn beispielsweise aktive Postfächer häufig erneut verschlüsselt werden, können inaktive, getrennte und deaktivierte Postfächer weiterhin mit den vorherigen Schlüsseln verschlüsselt werden. SharePoint Online führt eine Sicherung von Inhalten zu Wiederherstellungs-und Wiederherstellungszwecken aus, sodass archivierte Inhalte möglicherweise weiterhin mithilfe älterer Schlüssel gespeichert werden.<br/> Um die Sicherheit Ihrer Daten sicherzustellen, kann SharePoint Online nicht mehr als einen Schlüssel Roll Vorgang ausführen. Wenn Sie beide Schlüssel in einem schlüsseltresor Rollen möchten, müssen Sie warten, bis der erste Schlüssel Rollvorgang abgeschlossen ist. Unsere Empfehlung besteht darin, Ihre Key-Roll-Vorgänge in unterschiedlichen Intervallen zu staffeln, sodass dies kein Problem darstellt. 
  
Wenn Sie einen Schlüsselrollen, fordern Sie eine neue Version eines vorhandenen Schlüssels an. Um eine neue Version eines vorhandenen Schlüssels anzufordern, verwenden Sie dasselbe Cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), mit derselben Syntax, die Sie zum Erstellen des Schlüssels verwendet haben.
  
Beispiel:
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

In diesem Beispiel wird eine neue Schlüssel Version erstellt, da bereits ein Schlüssel mit dem Namen " **contoso-O365EX-na-VaultA1-Key001** " im **contoso-O365EX-VaultA1** -Tresor vorhanden ist. Der Vorgang fügt eine neue Schlüssel Version hinzu. Bei diesem Vorgang werden die vorherigen Schlüssel Versionen im Versionsverlauf des Schlüssels beibehalten, sodass Daten, die zuvor mit diesem Schlüssel verschlüsselt wurden, weiterhin entschlüsselt werden können. Nachdem Sie einen beliebigen Schlüssel für eine datenAUSFÜHRUNGSverHINDERung abgeschlossen haben, müssen Sie ein zusätzliches Cmdlet ausführen, um sicherzustellen, dass der Kundenschlüssel mit dem neuen Schlüssel beginnt. 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Aktivieren von Exchange Online und Skype for Business zum Verwenden eines neuen Schlüssels nach dem Rollen oder Drehen von Schlüsseln in Azure Key Vault

Wenn Sie einen der Azure Key Vault-Schlüssel für eine datenAUSFÜHRUNGSverHINDERung mit Exchange Online und Skype for Business verwenden, müssen Sie den folgenden Befehl ausführen, um die DEP zu aktualisieren und Office 365 zu aktivieren, um mit dem neuen Schlüssel zu beginnen.
  
So weisen Sie den Kundenschlüssel an, den neuen Schlüssel zum Verschlüsseln von Postfächern in Office 365 zu verwenden führen Sie das Cmdlet Set-DataEncryptionPolicy wie folgt aus:
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

Innerhalb von 48 Stunden werden die mit dieser Richtlinie verschlüsselten aktiven Postfächer dem aktualisierten Schlüssel zugeordnet. Gehen Sie folgendermaßen vor, um den Wert für die DataEncryptionPolicyID-Eigenschaft für das Postfach zu überprüfen. [](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) Der Wert für diese Eigenschaft ändert sich, nachdem der aktualisierte Schlüssel angewendet wurde. 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Aktivieren von SharePoint Online und OneDrive for Business zum Verwenden eines neuen Schlüssels nach dem Rollen oder Drehen von Schlüsseln in Azure Key Vault

Wenn Sie einen der Azure Key Vault-Schlüssel für eine datenAUSFÜHRUNGSverHINDERung in SharePoint Online und OneDrive for Business verwenden, müssen Sie das [Update-SPODataEncryptionPolicy-](https://technet.microsoft.com/library/mt843948.aspx) Cmdlet ausführen, um die DEP zu aktualisieren und Office 365 zu aktivieren, um mit dem neuen Schlüssel zu beginnen. 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

Dadurch wird der Schlüssel Roll-Vorgang für SharePoint Online und OneDrive for Business gestartet. Diese Aktion ist nicht sofort. Führen Sie zum Anzeigen des Fortschritts des Schlüssels Roll-Vorgangs das Cmdlet Get-SPODataEncryptionPolicy wie folgt aus:
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a>Verwalten von schlüsseltresor-Berechtigungen
<a name="Managekeyvaultperms"> </a>

Es stehen mehrere Cmdlets zur Verfügung, mit denen Sie wichtige Vault-Berechtigungen anzeigen und gegebenenfalls entfernen können. Möglicherweise müssen Sie Berechtigungen entfernen, beispielsweise wenn ein Mitarbeiter das Team verlässt.
  
Führen Sie das Cmdlet Get-AzureRmKeyVault aus, um die schlüsseltresor-Berechtigungen anzuzeigen:
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

Beispiel:
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

Führen Sie das Cmdlet Remove-AzureRmKeyVaultAccessPolicy aus, um die Berechtigungen eines Administrators zu entfernen:
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

Beispiel:
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a>Bestimmen der einem Postfach zugewiesenen DEP
<a name="DeterminemailboxDEP"> </a>

Verwenden Sie das Cmdlet Get-MailboxStatistics, um die einem Postfach zugewiesene DEP zu bestimmen. Das Cmdlet gibt einen eindeutigen Bezeichner (GUID) zurück.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

Wobei *GeneralMailboxOrMailUserIdParameter* ein Postfach angibt. Weitere Informationen zum Cmdlet Get-MailboxStatistics finden Sie unter [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).
  
Verwenden Sie die GUID, um den Anzeigenamen der DEP zu ermitteln, dem das Postfach zugewiesen wird, indem Sie das folgende Cmdlet ausführen.
  
```
Get-DataEncryptionPolicy <GUID>
```

Dabei ist *GUID* die GUID, die vom Get-MailboxStatistics-Cmdlet im vorherigen Schritt zurückgegeben wird. 
  

