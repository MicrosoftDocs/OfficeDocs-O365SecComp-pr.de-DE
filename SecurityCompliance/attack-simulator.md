---
title: Angriffssimulator in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/05/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: Als globaler Office 365-Administrator können Sie anGriffs Simulator verwenden, um realistische Angriffsszenarien in Ihrer Organisation auszuführen. Auf diese Weise können Sie anfällige Benutzer identifizieren und finden, bevor ein echter Angriff Ihr Unternehmen trifft.
ms.openlocfilehash: 25686ce194deca8d1ca07fca40f8142492951574
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410830"
---
# <a name="attack-simulator-in-office-365"></a>Angriffssimulator in Office 365

**Zusammenfassung** Wenn Sie ein globaler Office 365-Administrator sind und Ihre Organisation über [office 365 Threat Intelligence](office-365-ti.md)verfügt, können Sie Angriffs Simulator verwenden, um realistische Angriffsszenarien in Ihrer Organisation auszuführen. Dies kann Ihnen dabei helfen, anfällige Benutzer zu identifizieren und zu suchen, bevor sich ein echter Angriff auf Ihr Endergebnis auswirkt. Lesen Sie diesen Artikel, um mehr zu erfahren.

> [!IMPORTANT]
> Beginnend im Februar 2019 und über die nächsten Monate hinaus wird Office 365 Threat Intelligence zu Office 365 Advanced Threat Protection Plan 2 mit zusätzlichen Funktionen zum Schutz vor Bedrohungen. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
  
## <a name="the-attacks"></a>Die Angriffe

Derzeit stehen drei Arten von Angriffssimulationen zur Verfügung:
  
- [Anzeigename Spear-Phishing-Angriff](attack-simulator.md#spearphish)
    
- [Kenn Wort Sprüh Angriff](attack-simulator.md#passwordspray)
    
- [Brute-Force-Kennwortangriff](attack-simulator.md#bruteforce)
    
Damit ein Angriff erfolgreich gestartet werden kann, verwenden Sie die mehrstufige Authentifizierung für das Konto, mit dem Sie simulierte Angriffe ausführen. Darüber hinaus müssen Sie ein globaler Office 365-Administrator sein.
  
> [!NOTE]
> Die Unterstützung für bedingten Zugriff wird in Kürze verfügbar sein. 
  
Für den Zugriff auf Angriffs Simulator &amp; wählen Sie im Security Compliance Center **Threat Management** \> **Attack Simulator**aus.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen...

Stellen Sie sicher, dass Sie und Ihre Organisation die folgenden Anforderungen für anGriffs Simulator erfüllen:
      
- **Die E-Mails Ihrer Organisation werden in Exchange Online gehostet**. (AnGriffs Simulator ist für lokale e-Mail-Server nicht verfügbar.)
    
- **Sie sind ein Office 365-globaler Administrator**
    
- **Die mehrstufige [Authentifizierung (Multi-Factor Authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide) , MFA) ist mindestens für das globale Administratorkonto von Office 365 aktiviert**. (Im Idealfall ist MFA für alle Benutzer in Ihrer Organisation aktiviert.)
 
- **ihre organisation verfügt [über Office 365 Threat Intelligence](office-365-ti.md)**, mit angriffs simulator im &amp; Security Compliance Center (zum **Threat management** \> -angriffs **simulator**)<br/>![Threat Management-anGriffs Simulator](media/ThreatMgmt-AttackSimulator.png)

    
## <a name="display-name-spear-phishing-attack"></a>Anzeigename Spear-Phishing-Angriff

Phishing ist ein allgemeiner Ausdruck für eine breite Palette von Angriffen, die als Social Engineering-Angriff eingestuft werden. Dieser Angriff konzentriert sich auf Spear-Phishing, einen gezielteren Angriff, der auf eine bestimmte Gruppe von Individuen oder eine Organisation abzielt. In der Regel wird eine angepasste Angriffs Funktion mit einer gewissen Aufklärung durchgeführt und ein Anzeigename verwendet, der eine Vertrauensstellung im Empfänger generiert, beispielsweise eine e-Mail-Nachricht, die so aussieht, als ob Sie von einem Führungskräfte in Ihrer Organisation stammt.
  
Dieser Angriff hat den Schwerpunkt darauf, dass Sie ändern, von wem die Nachricht scheinbar stammt, indem Sie den Anzeigenamen und die Quelladresse geändert haben. Wenn Speer-Phishing-Angriffe erfolgreich sind, erhalten Internetkriminelle Zugriff auf die Anmeldeinformationen der Benutzer.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>So simulieren Sie einen Speer-Phishing-Angriff

![E-Mail-Textkörper verFassen](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
Sie können den Rich-HTML-Editor direkt im Feld **e-Mail-Textkörper** selbst oder mit HTML-Quelle arbeiten.
  
1. Wählen Sie [im &amp; Security Compliance Center](https://protection.office.com) **Threat Management** \> **Attack Simulator**aus.
    
2. Geben Sie einen aussagekräftigen Namen für die Kampagne an, oder wählen Sie eine Vorlage aus. <br/>![Phishing-Start Seite](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. Geben Sie die Zielempfänger an. Dabei kann es sich um Einzelpersonen oder Gruppen in Ihrer Organisation handeln. Jeder Zielempfänger muss über ein Exchange Online-Postfach verfügen, damit der Angriff erfolgreich ist. <br/>![Empfängerauswahl](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. Konfigurieren Sie die Details für Phishing-e-Mails. <br/>![Konfigurieren von e-Mail-Details](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/>Die HTML-Formatierung kann so komplex oder einfach sein, wie es Ihre Kampagne benötigt. Da das e-Mail-Format HTML ist, können Sie Bilder und Text einfügen, um Glaubwürdigkeit erhöhen zu verbessern. Sie haben die Kontrolle darüber, wie die empfangene Nachricht im empfangenden e-Mail-Client aussieht.
    
5. Geben Sie Text für das Feld **from (Name)** an. Dies ist das Feld, das im **Anzeigenamen** im empfangenden e-Mail-Client angezeigt wird. 
    
6. Geben Sie Text oder das Feld **von** ein. Dies ist das Feld, das als e-Mail-Adresse des Absenders im empfangenden e-Mail-Client angezeigt wird. <br/>Sie können einen vorhandenen e-Mail-Namespace in Ihrer Organisation eingeben (Dadurch wird die e-Mail-Adresse tatsächlich im empfangenden Client aufgelöst, wodurch ein sehr hohes vertrauenswürdiges Modell erleichtert wird), oder Sie können eine externe e-Mail-Adresse eingeben. Die angegebene e-Mail-Adresse muss nicht tatsächlich vorhanden sein, Sie muss jedoch das Format einer gültigen SMTP-Adresse wie Benutzer @ Domänenname. Extension befolgen. 
  
7. Wählen Sie mithilfe der Dropdownauswahl eine Phishing-Anmeldeserver-URL aus, die die Art der Inhalte widerspiegelt, die Sie in ihrem Angriff haben werden. Es werden mehrere Thema-URLs bereitgestellt, aus denen Sie auswählen können, beispielsweise Dokument Zustellungen, Technik, Abrechnung usw. Dies ist die URL, auf die gezielt Benutzer klicken müssen.
    
8. Geben Sie eine benutzerdefinierte Zielseiten-URL an. Bei Verwendung dieser Methode werden Benutzer zu einer URL umgeleitet, die Sie am Ende eines erfolgreichen Angriffs angeben. Wenn Sie beispielsweise über interne Schulungen verfügen, können Sie dies hier angeben.
    
9. Geben Sie Text für das Feld **Betreff** an. Dies ist das Feld, das als **antragSteller Name** im empfangenden e-Mail-Client angezeigt wird. 
    
10. VerFassen Sie den **e-Mail-Text** , der vom Ziel empfangen wird. <br/>`${username}`Fügt den Namen der Ziele in den e-Mail-Text ein. <br/>`${loginserverurl}`Fügt die URL ein, auf die Zielbenutzer klicken sollen. 
    
11. Klicken Sie auf **weiter und** dann auf **Fertig stellen** , um den Angriff zu starten. Die Spear-Phishing-e-Mail wird an die Postfächer ihrer Zielempfänger gesendet. 
    
## <a name="password-spray-attack"></a>Kenn Wort Sprüh Angriff

Ein Kenn Wort Sprüh Angriff gegen eine Organisation wird in der Regel verwendet, nachdem ein fehlerhafter Akteur erfolgreich eine Liste gültiger Benutzer aus dem Mandanten abgerufen hat. Der ungültige Akteur weiß um allgemeine Kennwörter, die von Benutzern verwendet werden. Hierbei handelt es sich um eine weit verbreitete Attacke, da es sich um einen billigen Angriff handelt, der nicht mehr erkannt werden kann als Brute-Force-Ansätze.
  
Dieser Angriff konzentriert sich darauf, dass Sie ein allgemeines Kennwort für eine umfangreiche Zielbasis von Benutzern angeben können.
  
### <a name="to-simulate-a-password-spray-attack"></a>So simulieren Sie einen Kenn Wort Sprüh Angriff

1. Wählen Sie [im &amp; Security Compliance Center](https://protection.office.com) **Threat Management** \> **Attack Simulator**aus.
    
2. Geben Sie einen aussagekräftigen Kampagnennamen für den Angriff an.
    
3. Geben Sie die Zielempfänger an. Dabei kann es sich um Einzelpersonen oder Gruppen in Ihrer Organisation handeln. Ein Zielempfänger muss über ein Exchange Online-Postfach verfügen, damit der Angriff erfolgreich ist.
    
4. Geben Sie ein Kennwort für den Angriff an. Beispiel: ein gemeinsames, relevantes Kennwort, das Sie ausprobieren können, ist `Fall2017`. Eine andere kann `Spring2018`sein, `Password1`oder.
    
5. Wählen Sie **Fertig stellen** , um den Angriff zu starten. 
    
## <a name="brute-force-password-attack"></a>Brute-Force-Kennwortangriff

Ein Brute-Force-Kennwortangriff gegen eine Organisation wird in der Regel verwendet, nachdem ein fehlerhafter Akteur erfolgreich eine Liste der Hauptbenutzer aus dem Mandanten abgerufen hat. Dieser Angriff zielt darauf ab, eine Reihe von Kennwörtern für das Konto eines einzelnen Benutzers zu testen.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>So simulieren Sie einen Brute-Force-Kennwortangriff

1. Wählen Sie [im &amp; Security Compliance Center](https://protection.office.com) **Threat Management** \> **Attack Simulator**aus.
    
2. Geben Sie einen aussagekräftigen Kampagnennamen für den Angriff an.
    
3. Geben Sie den Zielempfänger an. Ein Zielempfänger muss über ein Exchange Online-Postfach verfügen, damit der Angriff erfolgreich ist.
    
4. Geben Sie einen Satz von Kennwörtern an, die für den Angriff verwendet werden sollen. Zu diesem Zweck können Sie eine Textdatei (. txt) für die Liste der Kennwörter verwenden. Die Textdatei darf nicht größer als 10 MB sein. Verwenden Sie ein Kennwort pro Leitung, und stellen Sie sicher, dass Sie nach dem letzten Kennwort in der Liste eine harte Rückgabe angeben.
    
5. Wählen Sie **Fertig stellen** , um den Angriff zu starten. 
    
## <a name="new-features-in-attack-simulator"></a>Neue Features im anGriffs Simulator

Dem anGriffs Simulator werden neue Features hinzugefügt. Zu diesen zählen:

- **Erweiterte Berichterstellungsfunktionen**. Sie können beispielsweise die schnellste (oder langsamste) Zeit zum Öffnen einer e-Mail-Angriffssimulation sehen, die schnellste (oder langsamste) Zeit, um auf einen Link in der Nachricht zu klicken, und vieles mehr.

- **E-Mail-Vorlageneditor**. Sie können eine benutzerdefinierte, wieder verwendbare e-Mail-Vorlage erstellen, die Sie für zukünftige Angriffssimulationen verwenden können.

Besuchen Sie die [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap) , um zu sehen, was sich in der Entwicklung befindet, was ausrollt und was bereits gestartet wurde.

## <a name="see-also"></a>Siehe auch

[Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)

[Office 365 Advanced Threat Protection](office-365-atp.md)



