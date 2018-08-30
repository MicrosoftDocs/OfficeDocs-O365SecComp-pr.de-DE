---
title: Kontrolle über Ihre Daten in Office 365 mit Kunden-Taste
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: Erfahren Sie, wie Kundenschlüssel für Office 365 für Exchange Online, Skype für Unternehmen, SharePoint Online und OneDrive für Unternehmen einzurichten. Mit Kundenschlüssel Verschlüsselungsschlüssel Ihrer Organisation steuern und konfigurieren Sie anschließend Office 365, um diese verwenden, um die Daten im Ruhezustand in Microsoft Rechenzentren zu verschlüsseln.
ms.openlocfilehash: f8d7c12c32ca74b842f676f4a2ccde4d1c758361
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559230"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a>Kontrolle über Ihre Daten in Office 365 mit Kunden-Taste

Mit Kundenschlüssel Verschlüsselungsschlüssel Ihrer Organisation steuern und konfigurieren Sie anschließend Office 365, um diese verwenden, um die Daten im Ruhezustand in Microsoft Rechenzentren zu verschlüsseln. Daten im Ruhezustand enthält Daten aus Exchange Online und Skype für Unternehmen, die in Dateien, die in SharePoint Online gespeichert sind und Postfächer gespeichert sind und OneDrive für Unternehmen.
  
Sie müssen die Azure einrichten, bevor Sie Kundenschlüssel für Office 365 verwenden können. In diesem Thema werden die Schritte zum Erstellen und konfigurieren die erforderlichen Ressourcen Azure benötigten Schritte beschrieben und dann werden die Schritte zum Einrichten von Kundenschlüssel in Office 365. Nachdem Sie Azure Setup abgeschlossen haben, bestimmen Sie, welche Richtlinie und daher, welche Schlüssel, um Postfächer und Dateien in Ihrer Organisation zuweisen. Postfächer und die Dateien für die Sie eine Richtlinie zuweisen nicht verwendet Verschlüsselungsrichtlinien, die von Microsoft verwaltet und gesteuert. Weitere Informationen zu Kunden-Taste oder eine allgemeine Übersicht finden Sie unter den [Kunden Product Key für die Office 365 – häufig gestellte Fragen](service-encryption-with-customer-key-faq.md).
  
> [!IMPORTANT]
> Es wird dringend empfohlen, dass Sie den empfohlenen Vorgehensweisen in diesem Thema beschrieben. Diese werden als **Tipp** und **Wichtig**heraus aufgerufen. Kunden-Taste können Sie über Root Verschlüsselungsschlüssel, deren Bereich so groß wie die gesamte Organisation sein kann. Dies bedeutet, dass gemachte mit hierüber eine umfassende auswirken und können im Dienst unterbrechen oder unwiderruflich Verlust der Daten. 
  
## <a name="before-you-begin-setting-up-customer-key"></a>Vor dem Einrichten von Kunden-Taste
<a name="Beforeyoustart"> </a>

Bevor Sie beginnen, müssen Sie unbedingt, dass Sie die entsprechenden Lizenzierung für Ihre Organisation verfügen. Kundenschlüssel in Office 365 wird in Office 365 E5 oder die erweiterte Compliance-SKU angeboten.
  
Klicken Sie dann, sollten Sie zum Verständnis der Konzepte und die Verfahren in diesem Thema die [Azure Schlüssel Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) Dokumentation überprüfen. Darüber hinaus sind mit den in Azure, beispielsweise [Mandanten](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant)verwendeten Begriffen vertraut sein.
  
Senden Sie Ideen, Vorschläge und Perspektiven an customerkeyfeedback@microsoft.com, um Feedback auf Kundenschlüssel, einschließlich der Dokumentation zu ermöglichen.
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a>Übersicht über das Einrichten von Kundenschlüssel für Office 365
<a name="Overview"> </a>

Zum Einrichten der Customer-Schlüssel werden diese Aufgaben ausgeführt werden: Der Rest dieses Themas finden Sie ausführliche Anweisungen für jeden Vorgang oder Links, um weitere Informationen für jeden Schritt im Prozess.
  
**In Azure und Microsoft schnelle:**
  
Führen Sie die meisten dieser Aufgaben von Azure PowerShell eine Remoteverbindung herstellen. Die besten Ergebnisse erzielen, verwenden Sie Version 4.4.0 oder höher von Azure PowerShell.
  
- [Erstellen Sie zwei neue Azure-Abonnements](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [Registrieren der Azure-Abonnements, um eine obligatorische Aufbewahrungsdauer verwenden](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    Registrierung kann bis zu fünf Business Tage dauern.
    
- [Übermitteln einer Anforderung an Kundenschlüssel für Office 365 aktivieren](controlling-your-data-using-customer-key.md#FastTrack)
    
    Nachdem Sie die zwei neue Azure Abonnements erstellt haben, müssen Sie senden Sie die entsprechende Kundenschlüssel Angebot Anforderung anhand von einem Webformular, die im Microsoft FastTrack Portal gehostet wird. Das Team der schnelle bieten nicht mit Kundenschlüssel Unterstützung. Office einfach verwendet das schnelle Portal, die Sie zum Senden des Formulars und helfen, die relevante Angebote für Kundenschlüssel verfolgen können.
  
Nachdem Sie ein Kundenschlüssel Angebot gesendet haben, wird Microsoft prüft Ihre Anforderung und benachrichtigt, wenn Sie mit dem Rest der Setup-Aufgaben fortfahren können. Dieser Vorgang kann bis zu fünf Business Tage dauern.
    
- [Erstellen Sie eine Premium Azure Schlüssel Vault in jedes Abonnement](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [Zuweisen von Berechtigungen zu jeder wichtige vault](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [Aktivieren, und klicken Sie dann auf Ihre wichtigsten Depots vorläufiges Löschen bestätigen](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [Hinzufügen eines Schlüssels zur jeder wichtige Vault entweder durch Erstellen oder Importieren eines Schlüssels](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [Überprüfen der Wiederherstellung Ihren Schlüsseln](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [Backup Azure wichtige Vault](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [Überprüfen der Azure-Taste Vault-Konfigurationseinstellungen](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [Den URI für jeden Schlüssel Azure Schlüssel Vault zu erhalten](controlling-your-data-using-customer-key.md#GetKeyURI)
    
**In Office 365:**
  
Exchange Online und Skype für Unternehmen:
  
- [Erstellen einer Daten-Verschlüsselung-Richtlinie (DEP) für die Verwendung mit Exchange Online und Skype für Unternehmen](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [Zuweisen einer Datenausführungsverhinderung an ein Postfach](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [Überprüfen der Postfach-Verschlüsselung](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
SharePoint Online und OneDrive für Unternehmen:
  
- [Erstellen Sie eine Daten-Verschlüsselung-Richtlinie (DEP) für jeden SharePoint Online und OneDrive for Business geo](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [Überprüfen Sie die Verschlüsselung der Gruppe Websites, Teamwebsites und OneDrive für Unternehmen](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a>Ausführen von Aufgaben in Azure Schlüssel Vault und Microsoft FastTrack für Kunden-Taste
<a name="AzureSteps"> </a>

Führen Sie diese Aufgaben in Azure Schlüssel Vault, um Kundenschlüssel für Office 365 einzurichten. Sie müssen diese Schritte unabhängig davon, ob Sie Kundenschlüssel für Exchange Online und Skype für Unternehmen oder SharePoint Online und OneDrive für Unternehmen oder für alle unterstützten Dienste in Office 365 einrichten möchten.
  
### <a name="create-two-new-azure-subscriptions"></a>Erstellen Sie zwei neue Azure-Abonnements
<a name="Create2newsubs"> </a>

Zwei Azure-Abonnements sind erforderlich für Kunden-Taste. Als bewährte Methode empfiehlt es sich, dass Sie neue Azure Abonnements für die Verwendung mit Kundenschlüssel erstellen. Azure-Taste Vault Schlüssel können nur für Applikationen in derselben mandantenorganisation Azure Active Directory (AAD) autorisiert werden, müssen Sie die neue Abonnements mit den gleichen Azure AD-Mandanten mit Office 365-Organisation verwendet werden, in dem die Einzahlgn zugewiesen werden erstellen. Beispielsweise verwenden Ihr Konto arbeiten oder Schule, die globalen in Office 365-Organisation Administratorrechten. Ausführliche Schritte finden Sie unter [Registrieren für Azure als einer Organisation](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).
  
> [!IMPORTANT]
> Kundenschlüssel erfordert zwei Schlüssel für jede Richtlinie für Daten-Verschlüsselung (DEP). Um dies zu erreichen, müssen Sie zwei Azure Abonnements erstellen. Als bewährte Methode empfiehlt es sich, dass Sie separate Mitglieder Ihrer Organisation konfigurieren Sie einen Schlüssel in jedem Abonnement verfügen. Darüber hinaus sollte nur diese Azure Abonnements verwendet werden, Verschlüsselungsschlüssel für Office 365 verwalten. Dies schützt Ihre Organisation Fall, dass eine Ihrer Operatoren versehentlich, absichtlich oder böswilligen Benutzern löscht oder andernfalls mismanages die Schlüssel für die sie verantwortlich sind.<br/> Es wird empfohlen, dass Sie neue Azure Abonnements einrichten, die ausschließlich für die Verwaltung von Azure Schlüssel Vault Ressourcen für die Verwendung mit Kundenschlüssel verwendet werden. Es gibt keine praktische Obergrenze für die Anzahl der Azure-Abonnements, die Sie für Ihre Organisation erstellen können. Diese bewährten Methoden befolgen minimieren die Auswirkungen der Benutzerfehler und gleichzeitig die von Kundenschlüssel verwendeten Ressourcen verwalten. 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a>Übermitteln einer Anforderung an Kundenschlüssel für Office 365 aktivieren
<a name="FastTrack"> </a>

Nachdem Sie die Azure Schritte abgeschlossen haben, müssen Sie eine Anforderung Angebot in [Microsoft schnelle Portal](https://fasttrack.microsoft.com/)übermitteln. Nachdem Sie eine Anforderung über die schnelle Webportal gesendet haben, überprüft Microsoft die Azure-Taste Vault Konfiguration Daten und von Ihnen eingegebenen Informationen. Die Optionen, die in der Form Angebot bezüglich der autorisierten Finanzabteilung Ihrer Organisation ist erforderlich für den Abschluss der Registrierung Customer-Taste. Der Finanzabteilung Ihrer Organisation, die Sie im Formular auswählen werden zum Sicherstellen der Authentizität jeder Anforderung von widerrufen, und löschen Sie alle Schlüssel mit einer Kunden-Schlüssel datenverschlüsselung Richtlinie verwendet werden. Sie müssen diesen Schritt einmal führen Sie zum Aktivieren von Kundenschlüssel für Exchange Online und Skype für Business Abdeckung und ein zweites Mal Kundenschlüssel für SharePoint Online und OneDrive für Unternehmen zu aktivieren.
  
Führen Sie diese Schritte, um ein Angebot Kunden-Schlüssels zu übermitteln:
  
1. Melden Sie sich mit einem arbeiten oder Schule Konto mit globalen Administratorberechtigungen in Office 365-Organisation, [Microsoft schnelle Portal](https://fasttrack.microsoft.com/).
    
2. Sobald Sie angemeldet sind, navigieren Sie zu dem **Dashboard**.
    
3. Wählen Sie **bietet**, und überprüfen Sie die Liste der aktuellen Angebote.
    
4. Wählen Sie **Hier erfahren Sie mehr** , für das Angebot, das für Sie gilt: 
    
  - **Exchange Online und Skype für Unternehmen:** **Hier erfahren Sie mehr** wählen Sie auf das Angebot **Customer Product Key für Exchange aus** . 
    
  - **SharePoint Online und OneDrive für Unternehmen:** **Hier erfahren Sie mehr** auf das Angebot **Customer Product Key für die SharePoint- und OneDrive für Unternehmen** gewählten. 
    
5. Wählen Sie auf der Seite **Details bieten** **Anfordern erstellen**.
    
6. Füllen Sie alle anwendbaren Details und angeforderten Informationen auf dem Angebot Formular. Beachten Sie insbesondere, Ihre Auswahl für die Führungskräfte Ihrer Organisation genehmigen dauerhaft entfernt und nicht rückgängig gemacht werden beim Löschen des Verschlüsselungsschlüssel und Daten autorisiert werden soll. Wenn Sie das Formular abgeschlossen haben, wählen Sie **Submit**.
    
    Dieser Vorgang kann bis zu fünf Arbeitstagen sobald Microsoft Ihrer Anfrage benachrichtigt wurde dauern.
    
7. Gehen Sie obligatorische Aufbewahrung Period weiter unten im Abschnitt.
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a>Registrieren der Azure-Abonnements, um eine obligatorische Aufbewahrungsdauer verwenden
<a name="RegisterSubsforMRP"> </a>

Die Daten vorübergehende oder endgültig zum Verlust von Verschlüsselungsschlüsseln Stamm kann sehr störende oder sogar katastrophale, des Diensts und Datenverlust führen kann. Aus diesem Grund erfordern die mit Kundenschlüssel verwendeten Ressourcen verstärkte Sicherheit. Die Azure Ressourcen, die mit Kundenschlüssel verwendet werden, bieten Schutzmechanismen über die Standardkonfiguration. Azure-Abonnements können markiert oder in eine Möglichkeit, die sofortige und unwiderruflich Abbruch verhindern registriert werden. Dies wird als registrieren für eine obligatorische Aufbewahrungsdauer bezeichnet. Die erforderlichen Schritte zum Registrieren von Azure-Abonnements für eine obligatorische Aufbewahrungsdauer erfordern für die Zusammenarbeit mit dem Office 365-Team. Dieser Vorgang kann bis zu fünf Business Tage dauern. Bisher war dies manchmal als "Nicht Abbrechen" bezeichnet.
  
Vor der Kontaktaufnahme mit Office 365-Team, müssen Sie die folgenden Schritte für jede Azure-Abonnement ausführen, die Sie mit Kundenschlüssel verwenden:
  
1. Melden Sie sich bei Ihrer Azure-Abonnement mit Azure PowerShell. Anweisungen finden Sie unter [Melden Sie sich mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
2. Führen Sie das Cmdlet Register-AzureRmProviderFeature zum Registrieren Ihrer Abonnements, um eine obligatorische Aufbewahrungsdauer verwenden.
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. Wenden Sie sich an Microsoft, um den Vorgang abgeschlossen haben. Wenden Sie sich an [spock@microsoft.com](mailto:spock@microsoft.com)für SharePoint und OneDrive for Business-Team. Wenden Sie sich an [exock@microsoft.com](mailto:exock@microsoft.com)für Exchange Online und Skype für Unternehmen. Service Level Agreement (SLA) für Abschluss dieses Vorgangs fünf Arbeitstagen ist nach Microsoft benachrichtigt (überprüft, und) Sie haben eine obligatorische Aufbewahrungsdauer verwenden, um Ihre Abonnements registriert. Fügen Sie die folgenden Ihre e-Mail-Adresse:
    
    **Betreff**: Customer Product Key für die \< *vollqualifizierten Domänennamen Ihres Mandanten*\> 
    
    **Body**: Abonnement-IDs für die die obligatorische Aufbewahrung Periode beendet werden soll. 
    
4. Nachdem Sie von Microsoft benachrichtigt, dass die Registrierung abgeschlossen ist, überprüfen Sie den Status Ihrer Registrierung durch Ausführen von mit dem Cmdlet Get-AzureRmProviderFeature wie folgt:
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. Führen Sie nachdem Sie sichergestellt haben, dass die **Registrierung State** -Eigenschaft aus dem Cmdlet Get-AzureRmProviderFeature **Registered**Wert zurückgegeben den folgenden Befehl aus, um den Vorgang abzuschließen:
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a>Erstellen Sie eine Premium Azure Schlüssel Vault in jedes Abonnement
<a name="CreateKeyVault"> </a>

Die Schritte zum Erstellen einer wichtige Vault sind in die [Erste Schritte mit Azure Schlüssel Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), dokumentiert, die führt Sie durch das Installieren und Starten von Azure PowerShell, eine Verbindung mit Ihrem Azure-Abonnement, erstellen eine Ressourcengruppe und erstellen eine wichtige Vault, in dem Ressourcengruppe.
  
Wenn Sie einen Schlüssel Vault erstellen, müssen Sie eine SKU auswählen: Standard oder Premium. Der Standard-SKU kann Azure Schlüssel Vault Schlüssel mit Software geschützt werden - ist kein Schutz (Hardware Security Module, HSM) Schlüssel - und der Premium-SKU ermöglicht die Verwendung von HSMs für den Schutz der Schlüssel Vault Schlüssel. Kundenschlüssel akzeptiert wichtige Depots, die entweder SKU verwenden, obwohl Microsoft empfiehlt, dass Sie nur die Premium-SKU verwenden. Die Kosten der Vorgänge mit Schlüsseln des Typs entspricht, damit der einzige Unterschied Kosten die Kosten pro Monat für jeden Schlüssel HSM geschützt ist. Einzelheiten finden Sie in der [Schlüssel Vault Preise](https://azure.microsoft.com/pricing/details/key-vault/) . 
  
> [!IMPORTANT]
> Verwenden Sie die wichtigsten Depots Premium SKU und Schlüssel HSM-geschützten für Produktionsdaten und nur verwenden Sie wichtige Depots Standard SKU und Schlüssel für Test- und Validierung. 
  
Erstellen Sie für jeden Office 365-Dienst mit dem Sie Kundenschlüssel verwenden möchten eine wichtige Vault in jeder der beiden Azure Abonnements aufgelistet, die Sie erstellt haben. Für Exchange Online und Skype für Geschäftskunden nur und SharePoint Online und OneDrive für Unternehmen nur, beispielsweise erstellen Sie nur ein paar Depots. Um Kundenschlüssel für Exchange Online und SharePoint Online zu aktivieren, erstellen Sie zwei wichtige Depots-Paare.
  
Verwenden Sie eine Namenskonvention für wichtige Depots, die die beabsichtigte Verwendung von der Datenausführungsverhinderung widerspiegelt, die Sie den Depots zuordnen möchten. Finden Sie im Abschnitt Best Practices unter naming Convention Recommendations.
  
Erstellen einer separaten, kombinierte Depots für jede Data Encryption-Richtlinie. Für Exchange Online wird der Bereich einer Daten-Verschlüsselung Richtlinie von Ihnen ausgewählt, wenn Sie die Richtlinie Postfach zuweisen. Ein Postfach kann nur eine Richtlinie zugewiesen haben, und Sie können bis zu 50 Richtlinien erstellen. Für SharePoint Online ist der Bereich einer Richtlinie alle Daten in einer Organisation in einem geografischen Standort oder Geo.
  
Die Erstellung von wichtigen Depots erfordert auch die Erstellung von Azure Ressourcengruppen, da wichtige Depots benötigen die Speicherkapazität (obwohl sehr kleine) und Schlüssel Vault Protokollierung ist aktiviert, auch gespeicherte Daten generiert. Als bewährte Methode empfiehlt Microsoft die Verwendung von separater Administratoren zum Verwalten von einzelnen Ressourcengruppen mit der Verwaltung mit dem Satz von Administratoren, die alle zugehörige Kundenschlüssel Ressourcen verwalten werden ausgerichtet.
  
> [!IMPORTANT]
> Um die Verfügbarkeit zu maximieren, sollte Ihre wichtigsten Depots Regionen ungefähr in Office 365-Dienst sein. Wenn Ihre Exchange Online-Organisation in Nordamerika ist, platzieren Sie Ihre wichtigsten Depots in Nordamerika fest. Ist Ihre Exchange Online-Organisation in Europa, setzen Sie Ihre wichtigsten Depots in Europa.<br/>Verwenden Sie ein gemeinsames Präfix für wichtige Depots und umfassen eine Abkürzung für die Verwendung und Bereich der wichtigsten Vault und Schlüssel (z. B., für der Contoso-SharePoint-Dienst, in dem die Depots sich in Nordamerika, eine mögliche Paar von Namen befinden, Contoso-O365SP-NA-VaultA1 ist und Contoso-O365SP-NA-VaultA2. Vault Namen sind global eindeutigen Zeichenfolgen in Azure, müssen Sie möglicherweise die Namen der gewünschten Varianten versuchen, für den Fall, dass die Namen die gewünschten bereits durch andere Azure Kunden beansprucht werden. Ab Juli 2017 können Vault Namen geändert werden, damit eine bewährte Methode besteht darin einen schriftlichen Plan für die Installation und verwenden Sie eine weitere Person um zu überprüfen, ob der Plan ordnungsgemäß ausgeführt wird.<br/>Erstellen Sie wenn möglich, Ihre Depots Regionen nicht kombiniert. Kombinierte Azure Regionen stellen hohen Verfügbarkeit über Fehlerdomänen Service bereit. Regionale-Paare können daher als Sicherung des jeweils anderen Region betrachtet werden. Dies bedeutet, dass eine Azure-Ressource, die in einer Region platziert wird automatisch Fehlertoleranz durch die kombinierte Region Zustand wechselt. Aus diesem Grund auswählen von Regionen für zwei Depots verwendet in einer Datenausführungsverhinderung, in dem der Bereiche gekoppelten bedeutet, dass nur zwei Regionen aus der Verfügbarkeit insgesamt verwendet wird. Die meisten Regionen müssen nur zwei Regionen aus, damit diese noch nicht möglich, nicht gepaart Regionen ausgewählt ist. Wenn möglich, wählen Sie zwei nicht gepaart Regionen für die zwei Depots mit einer Datenausführungsverhinderung verwendet Profitieren von insgesamt vier Regionen der Verfügbarkeit. Weitere Informationen finden Sie unter [Business Continuity und Disaster Recovery (BCDR): Azure gepaart Regionen](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) für eine aktuelle Liste der regionalen-Paare. 
  
### <a name="assign-permissions-to-each-key-vault"></a>Zuweisen von Berechtigungen zu jeder wichtige vault
<a name="KeyVaultPerms"> </a>

Für jeden Schlüssel Vault müssen Sie drei separaten Satz von Berechtigungen für Kundenschlüssel, je nach der Implementierung definieren. Beispielsweise müssen Sie eine Reihe von Berechtigungen für jede der folgenden definieren:
  
- **Taste Vault Administratoren** , die über die alltägliche Verwaltung von Ihrer wichtigsten Vault für Ihre Organisation ausführen. Diese Aufgaben umfassen Backup, erstellen, abrufen, importieren, auflisten und wiederherstellen. 
    
    > [!IMPORTANT]
    > Der Satz von Berechtigungen, die wichtige Vault Administratoren zugewiesen umfasst nicht die Berechtigung, um den Schlüssel zu löschen. Dies ist beabsichtigt und eine wichtige Praxis. Löschen von Verschlüsselungsschlüssel in der Regel erfolgt nicht seit wie folgt so dauerhaft Daten verloren gehen. Es empfiehlt sich gewähren Sie keine diese Berechtigung wichtige Vault Administratoren standardmäßig. Stattdessen reservieren Sie dies für wichtige Vault Mitwirkende und nur an einen Administrator für eine einzelne kurzfristig weisen Sie zu, nachdem eine umfassende Kenntnis der folgen verstanden wird. 
  
    Wenn diese Berechtigungen zu einem Benutzer in Office 365-Organisation zuweisen möchten, melden Sie sich bei Ihrer Azure-Abonnement mit Azure PowerShell. Anweisungen finden Sie unter [Melden Sie sich mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
- Führen Sie das Set-AzureRmKeyVaultAccessPolicy-Cmdlet, um die erforderlichen Berechtigungen zuzuweisen.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  Beispiel:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- **Taste Vault Autoren** , die Berechtigungen für die Azure Schlüssel Vault selbst ändern können. Sie müssen diese Berechtigungen ändern, wie Mitarbeiter lassen oder teilnehmen an Ihr Team oder in der sehr seltene Fall, dass der Schlüssel vault Administratoren bewusst benötigen die Berechtigung zum Löschen oder Wiederherstellen eines Schlüssels. Diese Reihe von wichtigen Vault Mitwirkende muss die Rolle **Mitwirkender** auf Ihre wichtigsten Vault erteilt werden. Sie können diese Rolle zuweisen, mithilfe von Azure Ressourcen-Manager. Ausführliche Schritte finden Sie unter [Use Role-Based Access Control zum Verwalten des Zugriffs auf Ihre Ressourcen Azure-Abonnement](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). Der Administrator, der ein Abonnement erstellt hat dieses Zugriff implizit, sowie die Möglichkeit, anderen Administratoren zur Rolle Mitwirkender zuzuweisen.
    
- Wenn Sie beabsichtigen, Kundenschlüssel mit Exchange Online und Skype für Unternehmen verwenden, müssen Sie zu Office 365, verwenden Sie die wichtigsten Vault im Auftrag von Exchange Online und Skype für Business Berechtigung erteilen. Wenn Sie beabsichtigen, Kundenschlüssel mit SharePoint Online und OneDrive für Unternehmen verwenden, müssen Sie ebenso Berechtigung für die Office 365, verwenden Sie die wichtigsten Vault für SharePoint Online und OneDrive für Unternehmen hinzugefügt. Um zu Office 365 die Berechtigung erteilen, führen Sie das Cmdlet " **Set-AzureRmKeyVaultAccessPolicy** " mithilfe der folgenden Syntax aus: 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    Wobei Folgendes gilt:
    
  - *Vaultname* ist der Name der der wichtigsten Vault, den Sie erstellt haben. 
    
  - Ersetzen Sie für Exchange Online und Skype für Unternehmen, *Office 365 AppID* mit`00000002-0000-0ff1-ce00-000000000000`
    
  - Ersetzen Sie *Office 365 AppID* mit für SharePoint Online und OneDrive für Unternehmen`00000003-0000-0ff1-ce00-000000000000`
    
  Beispiel: Festlegen von Berechtigungen für Exchange Online und Skype für Unternehmen:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  Beispiel: Festlegen von Berechtigungen für SharePoint Online und OneDrive für Unternehmen
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a>Aktivieren, und klicken Sie dann auf Ihre wichtigsten Depots vorläufiges Löschen bestätigen
<a name="SoftDelete"> </a>

Wenn Sie Ihren Schlüsseln schnell wiederherstellen können, sind Sie mit weitaus geringerer Wahrscheinlichkeit einer längeren Dienstausfall aufgrund von böswilligen Benutzern oder versehentlich gelöschte Schlüssel-Umgebung zu bieten. Sie müssen aktivieren diese Konfiguration, bezeichnet als Soft löschen, bevor Sie Ihren Schlüsseln mit Kundenschlüssel verwenden können. Weiche löschen aktivieren, können Sie innerhalb des Löschens 90 Tage Schlüsseln oder Depots wiederherstellen, ohne sie aus Sicherung wiederherstellen.
  
Um weiche löschen auf Ihre wichtigsten Depots zu aktivieren, führen Sie diese Schritte aus:
  
1. Melden Sie sich bei Ihrer Azure-Abonnement mit Windows Powershell. Anweisungen finden Sie unter [Melden Sie sich mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).
    
2. Führen Sie das Cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . In diesem Beispiel ist *Vaultname* der Name der dem Schlüssel Vault für das Sie vorläufiges löschen aktivieren: 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. Vergewissern Sie sich, dass vorläufiges löschen für die wichtigsten Vault durch Ausführen des Cmdlets **Get-AzureRmKeyVault** konfiguriert ist. Wenn vorläufiges löschen für die wichtigsten Vault ordnungsgemäß konfiguriert ist, löschen Sie dann die vorläufig aktiviert? -Eigenschaft gibt den Wert **True**zurück: 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a>Hinzufügen eines Schlüssels zur jeder wichtige Vault entweder durch Erstellen oder Importieren eines Schlüssels
<a name="AddKeystoKeyVault"> </a>

Es gibt zwei Methoden, um ein Azure Schlüssel Vault Schlüssel hinzugefügt. Erstellen Sie einen Schlüssel direkt im Schlüssel Vault, oder Sie können einen Schlüssel importieren. Erstellen einen Schlüssel direkt im Schlüssel Vault ist die weniger kompliziert-Methode Importieren eines Schlüssels bietet eine vollständige Kontrolle über wie der Schlüssel generiert wird.
  
Um einen Schlüssel direkt in Ihre wichtigsten Vault erstellen möchten, führen Sie das Cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) wie folgt aus: 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

Wobei Folgendes gilt:
  
-  *Vaultname* ist der Name der der wichtigsten Vault, in dem Sie den Schlüssel erstellen möchten. 
    
-  *Schlüsselname* ist der Name des neuen Schlüssels erhalten soll. 
    
    > [!TIP]
    > Nennen Sie die Tasten mit einer ähnlichen Benennungskonvention für wichtige Depots wie oben beschrieben. Auf diese Weise wird in den Tools, mit die nur der Name des Schlüssels angezeigt, die Zeichenfolge Self beschreiben. 
  
- Wenn Sie beabsichtigen, den Schlüssel mit einer HSM zu schützen, stellen Sie sicher, dass Sie geben Sie als Wert des Parameters _Ziel_ **HSM** anderenfalls **Software**angeben.
    
Beispiel:
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

Um einen Schlüssel direkt in Ihre wichtigsten Vault importieren, müssen Sie eine Thales nShield Hardware Security Module haben.
  
Manche Organisationen bevorzugen diese Vorgehensweise zum Einrichten der Herkunft der ihre Schlüssel, und diese Methode bietet außerdem die folgenden:
  
- Verwendet für den Import Toolset umfasst Bescheinigung Thales, dass der Schlüssel Exchange Schlüssel (KEK), die zum Verschlüsseln, die Sie generieren des Schlüssels verwendet wird nicht exportierbar ist und innerhalb einer echten HSM, die von Thales hergestellt wurde generiert.
    
- Das Toolset enthält Bescheinigung Thales, dass die Azure Schlüssel Vault Security World auch auf einer echten HSM von Thales hergestellt generiert wurde. Diese Bescheinigung erweist sich als für Sie, dass Microsoft genuine Thales Hardware auch verwendet.
    
Wenden Sie sich die Sicherheitsgruppe zu ermitteln, ob die oben genannten Datenschutzpolitik erforderlich sind. Ausführliche Schritte zum Erstellen einer wichtige lokalen und in Ihrer wichtigsten Vault importieren finden Sie unter [generieren und HSM-geschützten Schlüssel für Azure Schlüssel Vault übertragen](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Verwenden Sie die Azure Anweisungen, um einen Schlüssel in jeder wichtige Vault zu erstellen.
  
### <a name="check-the-recovery-level-of-your-keys"></a>Überprüfen der Wiederherstellung Ihren Schlüsseln
<a name="CheckKeyRecoveryLevel"> </a>

Office 365 erfordert, dass das Abonnement Azure Schlüssel Vault auf kein Abbrechen festgelegt ist und dass der Schlüssel von Kundenschlüssel verwendet vorläufiges Löschen aktiviert ist. Sie können dies überprüfen, anhand der Ebene der Wiederherstellung auf Ihren Schlüsseln.
  
Führen Sie das Cmdlet Get-AzureKeyVaultKey wie folgt aus, um die Wiederherstellung Ebene eines Schlüssels, in Azure PowerShell zu überprüfen:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

Wenn die _Wiederherstellung Level_ -Eigenschaft einen anderen Wert als Wert **Wiederherstellbaren + ProtectedSubscription**zurückgibt, müssen Sie überprüfen Sie in diesem Thema und stellen Sie sicher, dass Sie alle Schritte, um das Abonnement in der Liste kein Abbrechen platzieren befolgt haben und dass Sie vorläufiges löschen auf jedem Ihrer wichtigsten Depots aktiviert haben.
  
### <a name="backup-azure-key-vault"></a>Backup Azure wichtige Vault
<a name="BackupAzureKeyVaultkeys"> </a>

Unmittelbar nach Erstellung oder jede Änderung an einem Schlüssel eine Sicherung durchführen und Speichern von Kopien der Sicherung, online und offline. Offline-Kopien sollte nicht mit einem Netzwerk wie in einer physischen Speicher für sichere oder kommerziellen Einrichtung verbunden werden. Mindestens eine Kopie der Sicherung sollten an einem Speicherort gespeichert werden, die in einem Notfall zugegriffen werden. Die Sicherung Blobs werden ausschließlich Schlüsselmaterial sollte ein Schlüssel Vault-Schlüssel werden dauerhaft oder wiederherzustellen gerendert andernfalls nicht funktioniert. Schlüssel, die außerhalb der Azure-Taste Vault sind und in Azure Schlüssel Vault importiert wurden führen Sie als Sicherungskopie nicht geeignet ist, da die Metadaten für Kunden-Taste, um den Schlüssel verwenden, mit dem externen Schlüssel nicht vorhanden ist. Nur eine Sicherung von Azure Schlüssel Vault kann für Wiederherstellungsvorgänge mit Kundenschlüssel verwendet werden. Aus diesem Grund ist es wichtig, dass eine Sicherung der Azure-Taste Vault vorgenommen werden, sobald eine Taste hochgeladen oder erstellt wird.
  
Führen Sie das Cmdlet [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) zum Erstellen einer Sicherung eines Schlüssels Azure Schlüssel Vault wie folgt aus:
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

Stellen Sie sicher, dass die Ausgabedatei das Suffix verwendet `.backup`.
  
Dieses Cmdlet entsteht Ausgabedatei ist verschlüsselt und kann nicht außerhalb von Azure Schlüssel Vault verwendet werden. Die Sicherung kann nur mit dem Azure-Abonnement wiederhergestellt werden, von dem die Sicherung durchgeführt wurde.
  
> [!TIP]
> Wählen Sie eine Kombination von Ihren Vault Namen und Schlüsselname für die Ausgabedatei. Dadurch wird der Name selbst beschreiben. Es stellt auch sicher, dass backup Dateinamen nicht kollidieren. 
  
Beispiel:
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a>Überprüfen der Azure-Taste Vault-Konfigurationseinstellungen
<a name="Validateconfiguration"> </a>

Ausführen der Überprüfung vor dem Verwenden der Schlüssel in einem Prevention, DEP ist optional, wird jedoch dringend empfohlen. Insbesondere, wenn Sie die Schritte zum Einrichten Ihrer Schlüssel und Depots andere als die in diesem Thema beschriebenen verwenden, sollten Sie überprüfen die Integrität Ihrer Azure Schlüssel Vault Ressourcen vor dem Konfigurieren der Customer-Taste.
  
So überprüfen, dass der Schlüssel Get, WrapKey und UnwrapKey Vorgänge aktiviert haben:
  
Führen Sie das Cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) wie folgt aus: 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

Suchen Sie in die Ausgabe für die Richtlinie für den Zugriff und die Exchange Online-ID (GUID) oder die SharePoint Online-ID (GUID) nach Bedarf. Alle drei oben aufgeführten Berechtigungen muss unter Berechtigungen Schlüssel angezeigt.
  
Wenn Sie Konfiguration der Richtlinie falsch ist, führen Sie das Cmdlet Set-AzureRmKeyVaultAccessPolicy wie folgt aus:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

Beispiel für Exchange Online und Skype für Unternehmen:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

Beispiel für SharePoint Online und OneDrive für Unternehmen:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

So überprüfen, dass ein Ablaufdatum für die Schlüssel wie folgt führen Sie das Cmdlet [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) nicht festgelegt ist: 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

Abgelaufener Schlüssel kann nicht durch Kunden Key verwendet werden und Vorgänge mit einem Schlüssel abgelaufene versucht fehl, und der Benutzer möglicherweise in einem Dienstausfall führen. Es wird dringend empfohlen, dass mit Kundenschlüssel verwendeten Schlüssel nicht über ein Ablaufdatum verfügen. Ein Ablaufdatum, sobald festgelegt ist, kann nicht entfernt werden, jedoch können auf ein anderes Datum geändert werden. Wenn Sie ein Schlüssel verwendet werden muss, die ein Ablaufdatum festgelegt hat, ändern Sie den Ablaufwert auf 12/31/9999 fest. Schlüssel mit einem Ablaufdatum festgelegt zu einem Datum werden andere als 12/31/9999 nicht Office 365-Validierung erfolgreich ist.
  
Um ein Ablaufdatum zu ändern, die auf einen anderen Wert als 12/31/9999 festgelegt wurde, führen Sie das Cmdlet [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) wie folgt aus: 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> Festlegen Sie nicht ein Ablaufdatum auf Verschlüsselungsschlüssel für die Verwendung mit Kundenschlüssel. 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a>Den URI für jeden Schlüssel Azure Schlüssel Vault zu erhalten
<a name="GetKeyURI"> </a>

Sobald Sie alle Schritte in Azure Einrichten Ihrer wichtigsten Depots abgeschlossen und Ihren Schlüsseln hinzugefügt haben, führen Sie den folgenden Befehl aus, um den URI für den Schlüssel in jeder wichtige Vault abzurufen. Sie müssen diese verwenden URIs beim Erstellen und weisen jedem DEP später, so speichern Sie diese Informationen an einem sicheren Ort. Denken Sie daran, diesen Befehl für jeden Schlüssel Vault einmal ausführen.
  
In Azure PowerShell:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a>Office 365: Einrichten von Kundenschlüssel für Exchange Online und Skype für Unternehmen
<a name="AzureSteps"> </a>

Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Aufgaben zum Einrichten der Azure-Taste Vault abgeschlossen haben. Informationen finden Sie unter [Ausführen von Aufgaben in Azure Schlüssel Vault und Microsoft schnelle für Kunden-Taste](controlling-your-data-using-customer-key.md#AzureSteps) . 
  
Um Kundenschlüssel für Exchange Online und Skype für Unternehmen einzurichten, müssen Sie diese Schritte ausführen, indem zu Exchange Online mit Windows PowerShell eine Remoteverbindung herstellen.
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a>Erstellen einer Daten-Verschlüsselung-Richtlinie (DEP) für die Verwendung mit Exchange Online und Skype für Unternehmen
<a name="CreateDEP4EXOSkype"> </a>

Eine Datenausführungsverhinderung ist einen Satz von Schlüsseln in Azure Schlüssel Vault gespeicherten zugeordnet. Sie weisen eine DEP eines Postfachs in Office 365. Office 365 wird die in der Richtlinie identifiziert Schlüssel verwenden, um das Postfach zu verschlüsseln. Wenn die Datenausführungsverhinderung erstellen möchten, benötigen Sie die Taste Vault-URIs, die Sie zuvor abgerufen. Weitere Informationen finden Sie in [den URI für jeden Schlüssel Azure Schlüssel Vault beziehen](controlling-your-data-using-customer-key.md#GetKeyURI) . 
  
Denken Sie daran! Beim Erstellen einer Datenausführungsverhinderung Geben Sie zwei Tasten, die sich in zwei verschiedenen Azure Schlüssel Depots befinden. Stellen Sie sicher, dass diese Schlüssel in zwei separate Azure Regionen für die Geo-Redundanz befinden.
  
Gehen Sie folgendermaßen vor, um die Datenausführungsverhinderung zu erstellen:
  
1. Auf dem lokalen Computer mithilfe eines arbeiten oder Schule Kontos, das in Office 365-Organisation, [eine Verbindung mit Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , indem Sie Windows PowerShell öffnen und Ausführen des folgenden Befehls globaler Administrator-Berechtigungen verfügt. 
    
   ```
   $UserCredential = Get-Credential
   ```

2. Klicken Sie im Dialogfeld Windows PowerShell anmelden Geben Sie Ihre Arbeit oder Schule Kontoinformationen, klicken Sie auf **OK**, und geben Sie den folgenden Befehl. 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. Führen Sie den folgenden Befehl aus.
    
   ```
   Import-PSSession $Session
   ```

4. Um eine DEP zu erstellen, verwenden Sie das Cmdlet "New-DataEncryptionPolicy" durch den folgenden Befehl eingeben.
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   Wobei Folgendes gilt:
    
   -  *PolicyName* ist der Name, den Sie für die Richtlinie verwenden möchten. Dürfen enthalten keine Leerzeichen. Beispielsweise USA_mailboxes. 
    
   -  *PolicyDescription* ist eine Beschreibung der Richtlinie, mit die Hilfe Sie nicht vergessen, was für die Richtlinie ist. Sie können in der Beschreibung Leerzeichen enthalten. Beispielsweise Root-Schlüssel für Postfächer in den USA und seine Gebieten. 
    
   -  *KeyVaultURI1* ist der URI für den ersten Schlüssel in der Richtlinie. Beispielsweise https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01. 
    
   -  *KeyVaultURI2* ist der URI für den zweiten Schlüssel in der Richtlinie. Beispielsweise https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Trennen Sie die beiden URIs durch ein Komma und ein Leerzeichen. 
    
   Beispiel:
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a>Zuweisen einer Datenausführungsverhinderung an ein Postfach
<a name="assignDEPtomailbox"> </a>

Weisen Sie die Datenausführungsverhinderung an ein Postfach mithilfe des Cmdlets Set-Mailbox. Nachdem Sie die Richtlinie zuweisen, können Office 365 das Postfach mit dem Schlüssel in der Datenausführungsverhinderung festgelegte verschlüsseln.
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

Hierbei gibt *MailboxIdParameter* ein Postfachs an. Weitere Informationen zum Set-Mailbox-Cmdlet finden Sie unter [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).
  
### <a name="validate-mailbox-encryption"></a>Überprüfen der Postfach-Verschlüsselung
<a name="validatemailboxencryption"> </a>

Verschlüsseln eines Postfachs kann einige Zeit dauern. Erste Mal Richtlinie zugewiesen das Postfach darüber hinaus müssen die Verschiebung aus einer Datenbank in eine andere, bevor das Postfach des Diensts verschlüsselt werden kann. Es wird empfohlen, dass Sie warten, bevor Sie versuchen, Verschlüsselung zu überprüfen, nachdem Sie eine DEP ändern oder beim ersten Sie eine DEP an ein Postfach zuweisen 72 Stunden.
  
Verwenden Sie das Cmdlet Get-MailboxStatistics zu ermitteln, ob ein Postfach verschlüsselt werden.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

Die IsEncrypted-Eigenschaft gibt einen Wert **true,** Wenn das Postfach verschlüsselt sind und den Wert **false** , wenn das Postfach nicht verschlüsselt sind. 

Die Zeit für das Verschieben von Postfächern, hängt von der Anzahl der Postfächer, die Sie eine DEP zum ersten Mal zuweisen, als auch die Größe der Postfächer ab. Wenn die Postfächer nach einer Woche ab dem Zeitpunkt nicht verschlüsselt wurden Sie die Datenausführungsverhinderung zugewiesen, Verschieben eines Postfachs für die unverschlüsselte Postfächer mit dem Cmdlet New-MoveRequest initiiert.

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a>Office 365: Einrichten von Kundenschlüssel für SharePoint Online und OneDrive für Unternehmen
<a name="AzureSteps"> </a>

Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Aufgaben zum Einrichten der Azure-Taste Vault abgeschlossen haben. Informationen finden Sie unter [Ausführen von Aufgaben in Azure Schlüssel Vault und Microsoft schnelle für Kunden-Taste](controlling-your-data-using-customer-key.md#AzureSteps) . 
  
Um Kundenschlüssel für SharePoint Online und OneDrive für Unternehmen einzurichten, müssen Sie diese Schritte ausführen, indem mit SharePoint Online mit Windows PowerShell eine Remoteverbindung herstellen.
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a>Erstellen Sie eine Daten-Verschlüsselung-Richtlinie (DEP) für jeden SharePoint Online und OneDrive for Business geo
<a name="CreateDEP4SPOODfB"> </a>

Eine Datenausführungsverhinderung ist einen Satz von Schlüsseln in Azure Schlüssel Vault gespeicherten zugeordnet. Eine Datenausführungsverhinderung auf alle Ihre Daten in einem geografischen Standort, auch als bezeichnet eine Geo angewendet. Wenn Sie das Multi-Geo-Feature von Office 365 (derzeit in der Vorschau) verwenden, können Sie eine DEP pro Geo erstellen. Wenn Sie nicht mit mehreren geografisch verwenden, können Sie eine Datenausführungsverhinderung für die Verwendung mit SharePoint Online und OneDrive for Business in Office 365 erstellen. Office 365 wird die Schlüssel in der Datenausführungsverhinderung identifiziert verwenden, um Ihre Daten in dieser Geo verschlüsseln. Wenn die Datenausführungsverhinderung erstellen möchten, benötigen Sie die Taste Vault-URIs, die Sie zuvor abgerufen. Weitere Informationen finden Sie in [den URI für jeden Schlüssel Azure Schlüssel Vault beziehen](controlling-your-data-using-customer-key.md#GetKeyURI) . 
  
Denken Sie daran! Beim Erstellen einer Datenausführungsverhinderung Geben Sie zwei Tasten, die sich in zwei verschiedenen Azure Schlüssel Depots befinden. Stellen Sie sicher, dass diese Schlüssel in zwei separate Azure Regionen für die Geo-Redundanz befinden.
  
Um eine DEP zu erstellen, müssen Sie eine Remoteverbindung herstellen mit SharePoint Online mithilfe von Windows PowerShell.
  
1. Auf dem lokalen Computer mithilfe eines Kontos arbeiten oder Schule, die in Office 365-Organisation, [eine Verbindung mit SharePoint Online-Powershell](https://technet.microsoft.com/library/fp161372.aspx)globaler Administrator-Berechtigungen verfügt.
    
2. Führen Sie in der Microsoft SharePoint Online-Verwaltungsshell das Cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) wie folgt aus: 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   Wenn Sie die Datenausführungsverhinderung registrieren, beginnt die Verschlüsselung auf die Daten in die Geo. Dies kann eine Weile dauern.
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a>Überprüfen Sie die Verschlüsselung der Gruppe Websites, Teamwebsites und OneDrive für Unternehmen
<a name="validateencryptionSPO"> </a>

Sie können den Status der Verschlüsselung suchen, indem Sie mit dem Cmdlet Get-SPODataEncryptionPolicy wie folgt ausgeführt:
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

Die Ausgabe dieses Cmdlets enthält:
  
- Der URI der Primärschlüssel.
    
- Der URI des sekundären Schlüssel.
    
- Der Verschlüsselungsstatus für die Geo. Mögliche Zuständen zählen:
    
  - **Nicht aufgehoben:** Verschlüsselung mit Schlüssel wurde noch nicht angewendet. 
    
  - **Registrieren:** Verschlüsselung mit Schlüssel angewendet wurde, und die Dateien, die gerade verschlüsselt sind. Wenn Ihre Geo in diesem Status ist, benötigen Sie auch angezeigt werden Informationen auf wie viel Prozent der Websites in der Geo abgeschlossen sind, sodass Sie Verschlüsselung Fortschritt überwachen können. 
    
  - **Registriert:** Verschlüsselung mit Schlüssel angewendet wurde, und alle Dateien in allen Websites verschlüsselt wurden. 
    
  - **Parallelen:** Eine wichtige Rolle ist in Bearbeitung. Wenn Ihre Geo in diesem Status ist, können Sie auch angezeigt werden Informationen wie viel Prozent der Websites haben die wichtigsten Roll-Operation abgeschlossen sein, damit Sie den Fortschritt überwachen können. 
    
## <a name="managing-customer-key-for-office-365"></a>Verwalten von Kunden Product Key für die Office 365
<a name="ManageCustomerKey"> </a>

Nachdem Sie Kundenschlüssel für Office 365 eingerichtet haben, können Sie diese zusätzliche Verwaltungsaufgaben ausführen.
  
- [Azure-Taste Vault Schlüssel wiederherstellen](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [Zurücksetzen oder gedreht einen Schlüssel in Azure Schlüssel Vault, die Sie mit Kundenschlüssel verwenden](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [Verwalten von Berechtigungen für wichtige vault](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [Bestimmen der Datenausführungsverhinderung zugewiesen an ein Postfach](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a>Azure-Taste Vault Schlüssel wiederherstellen
<a name="RestoreAzureKeyVaultKeys"> </a>

Verwenden Sie bevor Sie eine Wiederherstellung ausführen die Wiederherstellungsfunktionen von vorläufiges löschen. Alle Schlüssel, die mit Kundenschlüssel verwendet werden, werden benötigt, um vorläufiges Löschen aktiviert haben. Vorläufiges löschen verhält sich wie ein Papierkorb und ermöglicht die Wiederherstellung bis zu 90 Tage ohne wiederherstellen müssen. Wiederherstellung sollten nur unter Umständen extreme oder ungewöhnliche beispielsweise die Taste oder wichtige Vault verloren gegangen ist erforderlich sein. Wenn Sie einen Schlüssel für die Verwendung mit Kunden-Schlüssel wiederherstellen müssen in Azure PowerShell führen Sie das Cmdlet Restore-AzureKeyVaultKey wie folgt:
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

Beispiel:
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

Wenn eine Taste mit dem gleichen Namen in der wichtigsten Vault bereits vorhanden ist, schlägt der Restore-Vorgang fehl. Wiederherstellung AzureKeyVaultKey wiederherstellen alle wichtigen Versionen und alle Metadaten für den Schlüssel, einschließlich der Name des Schlüssels.
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a>Zurücksetzen oder gedreht einen Schlüssel in Azure Schlüssel Vault, die Sie mit Kundenschlüssel verwenden
<a name="RollCKkey"> </a>

Paralleles Schlüssel ist nicht erforderlich, durch entweder Azure Schlüssel Vault oder Kundenschlüssel. Darüber hinaus sind Schlüssel, die mit einer HSM geschützt sind praktisch unmöglich zu gefährden. Auch wenn ein Stammschlüssel im Besitz des einen böswilligen Akteur wäre gibt es keine machbare Möglichkeit der Nutzung zum Entschlüsseln von Daten, da nur Office 365 Code Verwendungsweise weiß. Paralleles eines Schlüssels ist jedoch durch Kunden Key unterstützt.
  
> [!CAUTION]
> Führen Sie nur einen Verschlüsselungsschlüssel, den Sie mit Kundenschlüssel verwenden, wenn kein deaktivieren technischer Grund vorhanden ist oder eine Compliance-Anforderung so festgelegt ist, müssen Sie den Schlüssel ein Rollback. Darüber hinaus alle Schlüssel, die Richtlinien zugeordnet wurden oder werden nicht gelöscht. Wenn Sie ein der Schlüssel, wird es Rollback werden mit den vorherigen Schlüsseln Inhalte nicht verschlüsselt. Beispielsweise während aktive Postfächer häufig inaktive erneut verschlüsselt werden werden, möglicherweise getrennt und deaktivierten Postfächer weiterhin mit den vorherigen Schlüsseln verschlüsselt werden. SharePoint Online führt, sodass es möglicherweise archivierten Inhalte mithilfe von ältere Schlüssel Sicherung von Inhalten aus Gründen der Wiederherstellung und Recovery.<br/> Um die Sicherheit Ihrer Daten zu gewährleisten, SharePoint Online nicht mehr als einen Schlüssel ein Rollback-Operation zu einem Zeitpunkt durchgeführt werden können. Wenn beide der Schlüssel in einem wichtigen Vault begonnen werden soll, müssen Sie warten, bis der erste wichtige Roll Vorgang vollständig abgeschlossen. Unsere Empfehlung ist, Ihre wichtigsten Roll Vorgänge in verschiedenen Intervallen staffeln, damit dies kein Belang ist. 
  
Wenn Sie einen Schlüssel wiederherstellen, werden Sie eine neue Version eines vorhandenen Schlüssels anfordern. Um eine neue Version eines vorhandenen Schlüssels anfordern möchten, verwenden Sie das gleiche-Cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), mit derselben Syntax, die Sie zum Erstellen des Schlüssels an erster Stelle verwendet.
  
Beispiel:
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

In diesem Beispiel, da ein Schlüssel mit dem Namen **Contoso-O365EX-NA-VaultA1-Key001** bereits in der **Contoso-O365EX-NA-VaultA1** Vault vorhanden ist wird eine neue Version Schlüssel erstellt werden. Der Vorgang fügt eine neue Version des Schlüssels. Dieser Vorgang behält die wichtigsten früheren Versionen im Versionsverlauf der Schlüssel, sodass zuvor mit diesem Schlüssel verschlüsselte Daten weiterhin entschlüsselt werden können. Sobald Sie parallelen eine beliebige Taste, die ein DEP zugeordnet ist abgeschlossen haben, müssen Sie dann eine zusätzliche-Cmdlet, um sicherzustellen, dass Kundenschlüssel beginnt mit dem neuen Schlüssel ausführen. 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Aktivieren Sie einen neuen Schlüssel verwenden, nachdem Sie ein Rollback oder Schlüssel in Azure Schlüssel Vault drehen Exchange Online und Skype für Unternehmen

Wenn Sie eine der ein Rollback der Azure-Taste Vault eine DEP zugeordnete TAB-mit Exchange Online und Skype für Business, müssen Sie den folgenden Befehl zum Aktualisieren der Datenausführungsverhinderung und Aktivieren von Office 365 zu starten, mit dem neuen Schlüssel ausführen.
  
Angewiesen, Kunden-Taste, um den neuen Schlüssel zum Verschlüsseln von Postfächern in Office 365 führen Sie das Set-DataEncryptionPolicy-Cmdlet wie folgt verwenden:
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

Innerhalb von 48 Stunden werden die aktive Postfächer mit dieser Richtlinie verschlüsselt mit dem aktualisierten Schlüssel verknüpft. Führen Sie die Schritte in [Determine die Datenausführungsverhinderung an ein Postfach zugewiesen](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) , um den Wert für die DataEncryptionPolicyID-Eigenschaft für das Postfach einzuchecken. Der Wert für diese Eigenschaft wird geändert, sobald der aktualisierte Schlüssel angewendet wurde. 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Aktivieren Sie einen neuen Schlüssel verwenden, nachdem Sie ein Rollback oder Schlüssel in Azure Schlüssel Vault drehen SharePoint Online und OneDrive für Unternehmen

Wenn Sie eine der ein Rollback müssen die Azure Schlüssel Vault Schlüssel ein DEP mit SharePoint Online und OneDrive für Unternehmen verwendet, Sie das [Update-SPODataEncryptionPolicy-](https://technet.microsoft.com/library/mt843948.aspx) Cmdlet, um die Datenausführungsverhinderung aktualisieren und Aktivieren von Office 365, um mit dem neuen Schlüssel zu starten. 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

Dadurch wird die Schlüssel Roll-Operation für SharePoint Online und OneDrive für Unternehmen gestartet. Diese Aktion ist nicht direkt. Um den Fortschritt des Schlüssels Vorgang ein Rollback angezeigt wird, führen Sie das Cmdlet Get-SPODataEncryptionPolicy wie folgt aus:
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a>Verwalten von Berechtigungen für wichtige vault
<a name="Managekeyvaultperms"> </a>

Mehrere Cmdlets sind verfügbar, mit denen Sie anzeigen und, falls erforderlich, entfernen wichtige Vault Berechtigungen. Sie müssen möglicherweise Berechtigungen, beispielsweise zu entfernen, wenn ein Mitarbeiter das Team verlässt.
  
Um wichtige Vault Berechtigungen anzuzeigen, führen Sie das Cmdlet Get-AzureRmKeyVault aus:
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

Beispiel:
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

Wenn ein Administrator Berechtigungen entfernen möchten, führen Sie das Cmdlet Remove-AzureRmKeyVaultAccessPolicy aus:
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

Beispiel:
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a>Bestimmen der Datenausführungsverhinderung zugewiesen an ein Postfach
<a name="DeterminemailboxDEP"> </a>

Um die Datenausführungsverhinderung zugewiesen an ein Postfach zu bestimmen, verwenden Sie das Cmdlet Get-MailboxStatistics aus. Das Cmdlet gibt einen eindeutigen Bezeichner (GUID) zurück.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

Hierbei gibt *GeneralMailboxOrMailUserIdParameter* ein Postfachs an. Weitere Informationen über das Cmdlet Get-MailboxStatistics finden Sie unter [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).
  
Verwenden Sie die GUID, um den Anzeigenamen der die Datenausführungsverhinderung zu erhalten, der das Postfach zugewiesen ist, indem Sie das folgende Cmdlet ausführen.
  
```
Get-DataEncryptionPolicy <GUID>
```

Dabei ist die *GUID* der GUID, die vom Cmdlet Get-MailboxStatistics im vorherigen Schritt zurückgegeben. 
  

