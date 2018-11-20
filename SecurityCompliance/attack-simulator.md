---
title: Angriffssimulator in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/09/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Als globaler Office 365-Administrator können Sie Angriff Simulator realistische Angriff Szenarien in Ihrer Organisation ausführen. Dies hilft Ihnen zu identifizieren und anfällig Benutzer vor ein tatsächlichen Angriff Ihres Unternehmens Treffer zu finden.
ms.openlocfilehash: ccef127c4ce4d806ef9af04673b8c68d82ce9ec6
ms.sourcegitcommit: 7c55721b51b2f321537a0cdad6644abf91996710
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2018
ms.locfileid: "26256440"
---
# <a name="attack-simulator-in-office-365"></a>Angriffssimulator in Office 365

**Zusammenfassung** Wenn Sie ein Office 365 globaler Administrator sind und Ihre Organisation [Office 365 Bedrohungsanalyse verfügt](office-365-ti.md), können Angriff Simulator Sie realistisch Angriff Szenarien in Ihrer Organisation auszuführen. Dies hilft Ihnen zu identifizieren und anfällig Benutzer vor ein tatsächlichen Angriff wirkt sich auf die Ihre bedeutsam zu finden. Lesen Sie diesen Artikel, um mehr zu erfahren.
  
## <a name="the-attacks"></a>Die Angriffe

Derzeit sind drei Arten von Angriff Simulationen verfügbar:
  
- [Anzeigen von Namen Spear-Phishing-Angriff](attack-simulator.md#spearphish)
    
- [Kennwort Sprühende-Angriff](attack-simulator.md#passwordspray)
    
- [Brute-Force-Angriff auf das Kennwort](attack-simulator.md#bruteforce)
    
Für ein Angriff erfolgreich gestartet werden verwenden Sie mehrstufige Authentifizierung auf das Konto, das Sie mithilfe von simulierten Angriffe ausführen. Darüber hinaus müssen Sie ein globaler Office 365-Administrator sein.
  
> [!NOTE]
> Unterstützung für bedingten Zugriff wird in Kürze bereitgestellt. 
  
Angriff Simulator, in das Wertpapier Zugriff auf &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen...

Stellen Sie sicher, dass Sie und Ihre Organisation die folgenden Anforderungen für Angriff Simulator erfüllen:
      
- E-Mail von Ihrer Organisation wird in Exchange Online gehostet. (Angriff Simulator ist nicht für lokale e-Mail-Server verfügbar.)
    
- Sie sind Administrator globaler Office 365
    
- Ihr Unternehmen verwendet [Multi-Factor Authentication für Office 365-Benutzer](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication&view=o365-worldwide)
 
- Ihre Organisation verfügt [Office 365 Bedrohungsanalyse](office-365-ti.md)mit Angriff Simulator sichtbar in das Wertpapier &amp; Compliance Center (Wechseln Sie zu **Threat Management** \> **Angriff Simulator**)<br/>![Threat Management - Angriff Simulator](media/ThreatMgmt-AttackSimulator.png)

    
## <a name="display-name-spear-phishing-attack"></a>Anzeigen von Namen Spear-Phishing-Angriff

Phishing ist ein allgemeiner Begriff für eine Breite Palette von Angriffen als eine Formatvorlage Social Engineering-Angriff. Dieser Angriff konzentriert sich auf einen mehr gezielten Angriff Spear Phishing, die auf eine bestimmte Gruppe von Personen oder einer Organisation gerichtet ist. In der Regel ein angepasster Angriff mit einigen Eindringung durchgeführt, und verwenden einen Anzeigenamen ein, der die Vertrauenswürdigkeit in der Empfänger generiert wird, wie eine e-Mail-Nachricht, die es aussieht stammt Führungskraft innerhalb Ihrer Organisation.
  
Dieser Angriff konzentriert sich auf Navigate Bearbeitung, die die Meldung angezeigt wird, durch ändern den Anzeigenamen und die Quelle der Adresse stammt haben. Wenn Spear Phishing-Angriffe erfolgreich ausgeführt werden, Zugriff Internetkriminelle auf Anmeldeinformationen von Benutzern.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>Simuliert einen Spear-Phishing-Angriff

![Verfassen Sie e-Mail-Text](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
Sie können den rich-HTML-Editor direkt in das Feld **e-Mail-Text** selbst erstellen oder Arbeiten mit HTML-Quelle. Es gibt zwei wichtige Felder für die Einbeziehung in der HTML-Code ein: 
  
1. In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.
    
2. Geben Sie einen sinnvollen Kampagnennamen für den Angriff, oder wählen Sie eine Vorlage aus. <br/>![Phishing-Startseite](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. Geben Sie die Ziel-Empfänger. Dies kann Personen oder Gruppen in Ihrer Organisation sein. Jeden vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein. <br/>![Empfänger Auswahl](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. Konfigurieren Sie die Details der Phishing-e-Mail. <br/>![Konfigurieren von e-Mail-details](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/>Die HTML-Formatierung möglicherweise als komplexe oder grundlegende wie Ihre Kampagne benötigen. Das e-Mail-Format um HTML handelt, können Sie Bilder und Text Believability optimiert einfügen. Sie können bestimmen, auf die empfangene Meldung in der empfangenden e-Mail-Client aussehen.
    
5. Geben Sie Text für das Feld **von (Name)** . Dies ist das Feld, das den **Anzeigenamen** in den Empfang von e-Mail-Client anzeigt. 
    
6. Geben Sie Text oder auf das Feld **aus** . Dies ist das Feld, das zeigt, wie die e-Mail-Adresse des Absenders in der Empfang von e-Mail-Client.<br/>Sie können einen vorhandenen e-Mail-Namespace innerhalb Ihrer Organisation eingeben (auf diese Weise wird stellen die e-Mail-Adresse, die tatsächlich in der empfangenden Client einen sehr hohen Vertrauensmodell Erleichterung beheben), oder Sie können eine externe e-Mail-Adresse eingeben. Die e-Mail-Adresse, die Sie noch nicht existieren tatsächlich angeben, aber es muss das Format der eine gültige SMTP-Adresse, wie beispielsweise user@domainname.extension folgen. 
  
7. Wählen Sie die Dropdown-Auswahl mit einen Phishing Anmelde-Server-URL, die den Typ des Inhalts widerspiegelt innerhalb Ihrer Angriff haben. Mehrere entsprechendes mit Design versehenes URLs werden für Sie auswählen, wie etwa Dokument Übermittlung, technische, Lohn und Gehalt usw. bereitgestellt. Dies ist effektiv die URL, die vorgesehenen Benutzer aufgefordert werden, klicken Sie auf.
    
8. Geben Sie einen benutzerdefinierten Zielseite Seiten-URL. Mit diesem werden Benutzer auf eine URL weitergeleitet, die Sie am Ende einer erfolgreichen Angriff angeben. Wenn Sie interne zur Förderung des Bekanntheitsgrads Schulung verfügen, z. B. soll, die hier.
    
9. Geben Sie Text für das Feld **Betreff** . Dies ist das Feld, das zeigt, wie der **Antragstellername** in der Empfang von e-Mail-Client. 
    
10. Erstellen Sie den **e-Mail-Text** , der das Ziel des Vorgangs erhalten soll. <br/>`${username}`der Name der Ziele in den e-Mail-Text eingefügt. <br/>`${loginserverurl}`Fügt die URL, die wir Zielbenutzer klicken Sie auf sollen 
    
11. Wählen Sie **Weiter,** und klicken Sie dann **Fertig stellen,** um den Angriff zu starten. Die Spear Phishing-e-Mail-Nachricht wird an die Postfächer Ihrer Ziel Empfänger übermittelt. 
    
## <a name="password-spray-attack"></a>Kennwort Sprühende-Angriff

Ein Aerosol Angriff das Kennwort einer Organisation wird normalerweise verwendet, nachdem ein Akteur Bad erfolgreich eine Liste der gültigen Benutzer aus den Mandanten erworben hat. Der Akteur "Bad" weiß über allgemeine Kennwörter, die für die Personensuche verwenden. Dies ist eine weit verbreitete Angriff unverändert einen billig Angriff ausführen und schwerer als brute-Force-Ansätze erkannt.
  
Dieser Angriff konzentriert sich auf lassen Sie ein allgemeine Kennwort anhand einer großen Ziel Basis von Benutzern angeben.
  
### <a name="to-simulate-a-password-spray-attack"></a>Können Sie das Kennwort Sprühende-Angriff

1. In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.
    
2. Geben Sie einen sinnvollen Kampagnennamen für den Angriff.
    
3. Geben Sie die Ziel-Empfänger. Dies kann Personen oder Gruppen in Ihrer Organisation sein. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.
    
4. Geben Sie ein Kennwort für den Angriff verwenden. Beispielsweise ist eine gängige und relevante Kennwort könnten Sie versuchen `Fall2017`. Eine andere möglicherweise `Spring2018`, oder `Password1`.
    
5. Wählen Sie auf **Fertig stellen** , um den Angriff zu starten. 
    
## <a name="brute-force-password-attack"></a>Brute-Force-Angriff auf das Kennwort

Ein Password Brute-Force-Angriff auf einer Organisation wird normalerweise verwendet, nachdem ein Akteur Bad erfolgreich eine Liste der wichtigsten Benutzer aus den Mandanten erworben hat. Dieser Angriff konzentriert sich auf versucht, eine Gruppe von Kennwörtern für einen Einzelbenutzer-Konto.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>Simuliert einen Password Brute-Force-Angriff

1. In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.
    
2. Geben Sie einen sinnvollen Kampagnennamen für den Angriff.
    
3. Geben Sie den Empfänger weiter. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.
    
4. Geben Sie eine Gruppe von Kennwörtern für den Angriff verwenden. Sie können eine Textdatei (txt) für die Liste der Kennwörter. Die Datei darf 10 MB Dateigröße nicht überschreiten. Verwenden Sie ein Kennwort pro Zeile, und stellen Sie sicher, dass Sie eine Absatzmarke hinter das letzte Kennwort in der Liste enthalten.
    
5. Wählen Sie auf **Fertig stellen** , um den Angriff zu starten. 
    
## <a name="new-features-in-attack-simulator"></a>Neue Features in Angriff Simulator

Angriff Simulator werden neue Features hinzugefügt wird. Dazu zählen folgende:
- **Reporting-Funktionen erweitert**. Sie können Daten wie die schnellste (oder langsamste) Uhrzeit, eine e-Mail-Nachricht Angriff Simulation, die schnellste (oder langsamste) zu öffnen, auf einen Link in der Nachricht sehen sein.
- **E-Mail-Vorlagen-Editor**. Sie können eine benutzerdefinierte, wieder verwendbare e-Mail-Vorlage erstellen, die Sie für zukünftige Angriff Simulationen verwenden können.

Besuchen Sie die [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) , um herauszufinden, was bei der Entwicklung ist, was Rollout wird und was bereits gestartet wird.



