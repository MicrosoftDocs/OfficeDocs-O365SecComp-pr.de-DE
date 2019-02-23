---
Title: "Protection Features in Azure Information Protection Rolling to existing Office 365 Mandanten" MS. Author: krowley Author: kccross Manager: laurawi ms. Date: 6/29/2018 ms. Audience: ITPro ms. Topic: article ms. Service: O365-seccomp localization_ Priority: normal Search. appverid:
- MET150 ms. Asset-Nr.: 7ad6f58e-65d7-4c82-8e65-0b773666634d ms. Collection:
    - M365-Security-Compliance Description: "um mit dem ersten Schritt beim Schutz Ihrer Informationen zu helfen, werden ab Juli 2018 alle für den Azure Information Protection berechtigten Mandanten die Schutzfunktionen in Azure Information Protection standardmäßig aktiviert haben. Die Schutzfunktionen in Azure Information Protection waren früher in Office 365 als Rechteverwaltung oder Azure RMS bekannt. Wenn Ihre Organisation über einen Office E3-Service Plan oder einen höheren Service Plan verfügt, erhalten Sie jetzt einen Vorsprung beim Schutz von Informationen über Azure Information Protection, wenn wir diese Features bereitstellen. "
---

# <a name="protection-features-in-azure-information-protection-rolling-out-to-existing-office-365-tenants"></a>Schutzfunktionen in Azure Information Protection, die für vorhandene Office 365-Mandanten bereitstellen

Um den ersten Schritt zum Schutz Ihrer Informationen zu unterstützen, werden ab Juli 2018 alle für den Azure Information Protection berechtigten Mandanten die Schutzfunktionen in Azure Information Protection standardmäßig aktiviert haben. Die Schutzfunktionen in Azure Information Protection waren früher in Office 365 als Rechteverwaltung oder Azure RMS bekannt. Wenn Ihre Organisation über einen Office E3-Service Plan oder einen höheren Service Plan verfügt, erhalten Sie jetzt einen Vorsprung beim Schutz von Informationen über Azure Information Protection, wenn wir diese Features bereitstellen.
  
## <a name="changes-beginning-july-1-2018"></a>Änderungen ab 1. Juli 2018

Ab dem 1. Juli 2018 aktiviert Microsoft die Schutzfunktion in Azure Information Protection für alle Office 365-Mandanten, die über einen der folgenden Abonnement Pläne verfügen:
  
- Office 365 Nachrichtenverschlüsselung wird als Teil von Office 365 E3 und E5, Microsoft E3 und E5, Office 365 a1, a3 und A5 sowie Office 365 G3 und G5 angeboten. Sie benötigen keine zusätzlichen Lizenzen, um die neuen Schutzfunktionen von Azure Information Protection zu erhalten. 
    
- Sie können auch Azure Information Protection-Plan 1 zu den folgenden Plänen hinzufügen, um die neuen Office 365-Nachrichten Verschlüsselungsfunktionen zu erhalten: Exchange Online-Plan 1, Exchange Online Plan 2, Office 365 F1, Office 365 Business Essentials, Office 365 Business Premium oder Office 365 Enterprise E1.
    
- Jeder Benutzer, der von der Office 365-Nachrichtenverschlüsselung profitiert, muss lizenziert sein, damit er von der Funktion abgedeckt wird.
    
- Die vollständige Liste finden Sie in den [Exchange Online-Dienstbeschreibungen](https://technet.microsoft.com/library/exchange-online-service-description.aspx) für die Office 365-Nachrichtenverschlüsselung. 
    
Mandantenadministratoren können den Schutzstatus im Office 365-Administratorportal überprüfen. 
  
![Screenshot, der zeigt, dass die Rechteverwaltung in Office 365 aktiviert ist.](media/303453c8-e4a5-4875-b49f-e80c3eb7b91e.png)
  
## <a name="why-are-we-making-this-change"></a>Warum machen wir diese Änderung?

Office 365-Nachrichtenverschlüsselung nutzt die Schutzfunktionen in Azure Information Protection. Im Kern der letzten Verbesserungen an der Office 365-Nachrichtenverschlüsselung und unseren umfassenderen Investitionen in den Informationsschutz in Microsoft 365 machen wir es für Organisationen einfacher, unsere Schutzfunktionen zu aktivieren und zu verwenden, wie historisch die Verschlüsselung Technologien waren schwierig einzurichten. Wenn Sie die Schutzfunktionen in Azure Information Protection standardmäßig aktivieren, können Sie schnell beginnen, Ihre vertraulichen Daten zu schützen.
  
## <a name="does-this-impact-me"></a>Wirkt sich dies auf mich aus?

Wenn Ihre Office 365-Organisation eine berechtigte Office 365-Lizenz erworben hat, wird Ihr Mandant von dieser Änderung betroffen sein.
  
 **Wichtig!** Wenn Sie Active Directory-RechteverwaltungsDienste (AD RMS) in Ihrer lokalen Umgebung verwenden, müssen Sie diese Änderung sofort beenden oder zu Azure Information Protection migrieren, bevor wir diese Änderung innerhalb der nächsten 30 Tage ausführen. Weitere Informationen zum Abmelden finden Sie unter "Ich verwende AD RMS, wie aktiviere ich out?" weiter unten in diesem Artikel. Wenn Sie lieber migrieren möchten, lesen Sie [Migrieren von AD RMS zu Azure Information Protection.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="can-i-use-azure-information-protection-with-active-directory-rights-management-services-ad-rms"></a>Kann ich Azure Information Protection mit Active Directory Rights Management Services (AD RMS) verwenden?

Nein. Hierbei handelt es sich nicht um ein unterstütztes Bereitstellungsszenario. Ohne die zusätzlichen Opt-out-Schritte können einige Computer automatisch den Azure-Rechteverwaltungsdienst verwenden und eine Verbindung mit Ihrem AD RMS-Cluster herstellen. Dieses Szenario wird nicht unterstützt und hat unzuverlässige Ergebnisse, daher ist es wichtig, dass Sie diese Änderung innerhalb der nächsten 30 Tage abwählen, bevor wir diese neuen Features bereitstellen. Weitere Informationen zum Abmelden finden Sie unter "Ich verwende AD RMS, wie aktiviere ich out?" weiter unten in diesem Artikel. Wenn Sie lieber migrieren möchten, lesen Sie [Migrieren von AD RMS zu Azure Information Protection.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="how-do-i-know-if-im-using-ad-rms"></a>Wie erkenne ich, ob ich AD RMS verwende?

Verwenden Sie diese Anweisungen, um [die Umgebung für die Azure-Rechteverwaltung vorzubereiten, wenn Sie auch über Active Directory-rechteVerwaltungsdienste (AD RMS) verfügen](https://docs.microsoft.com/azure/information-protection/deploy-use/prepare-environment-adrms) , um zu überprüfen, ob Sie AD RMS bereitgestellt haben: 
  
1. Obwohl die meisten AD RMS-Bereitstellungen optional den Dienstverbindungspunkt (Service Connection Point, SCP) in Active Directory veröffentlichen, können Domänencomputer den AD RMS-Cluster erkennen. 
  
Verwenden Sie die ADSI-Bearbeitung, um festzustellen, ob Sie einen SCP in Active Directory veröffentlicht haben: CN = Configuration [Servername], CN = Services, CN = RightsManagementServices, CN = SCP
    
2. Wenn Sie keinen SCP verwenden, müssen Windows-Computer, die eine Verbindung mit einem AD RMS-Cluster herstellen, für die clientseitige Dienstermittlung oder Lizenzierungs Umleitung mithilfe der Windows-Registrierung konfiguriert werden: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation oder HKEY_ LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSIPC\ServiceLocation 
  
Weitere Informationen zu diesen Registrierungs Konfigurationen finden Sie unter [Aktivieren der clientseitigen Diensterkennung mithilfe der Windows-Registrierung](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#enabling-client-side-service-discovery-by-using-the-windows-registry) und Umleiten des [Lizenzierungsserver](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#redirecting-licensing-server-traffic)Datenverkehrs.
    
## <a name="i-use-ad-rms-how-do-i-opt-out"></a>Ich verwende AD RMS, wie kann ich mich entscheiden?

Führen Sie die folgenden Schritte aus, um die bevorstehende Änderung abzulehnen:
  
1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Führen Sie das Cmdlet Set-IRMConfiguration mit der folgenden Syntax aus:
    
  ```
  Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false 
  ```

## <a name="what-can-i-expect-after-this-change-has-been-made"></a>Was kann ich erwarten, nachdem diese Änderung vorgenommen wurde?

Nachdem Sie diese Option aktiviert haben, können Sie die neue Version der Office 365-Nachrichtenverschlüsselung verwenden, die bei [Microsoft ignite 2017](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Email-Encryption-and-Rights-Protection/ba-p/110801) angekündigt wurde und die Verschlüsselungs-und Schutzfunktionen von Azure-Informationen nutzt. Schutz. 
  
![Screenshot, der eine geschützte Nachricht in Outlook im Web anzeigt.](media/599ca9e7-c05a-429e-ae8d-359f1291a3d8.png)
  
Weitere Informationen zu den neuen Erweiterungen finden Sie unter [Office 365-Nachrichtenverschlüsselung](ome.md).
  

