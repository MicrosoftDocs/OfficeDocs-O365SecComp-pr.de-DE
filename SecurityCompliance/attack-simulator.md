---
title: Angriff Simulator in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/19/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Hier erfahren Sie, etwa drei verschiedene Arten von Internet-Angriffen, die mit Angriff Simulator ausgeführt werden können.
ms.openlocfilehash: 364144c0b2f8109c67fb262ce879414088380ebe
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529186"
---
# <a name="attack-simulator-in-office-365"></a>Angriff Simulator in Office 365

Mit Angriff Simulator (enthalten in [Office 365 Bedrohungsanalyse](office-365-ti.md)) Wenn Sie Mitglied der Security-Team Ihrer Organisation sind, können Sie realistisch Angriff Szenarien in Ihrer Organisation ausführen. Dies hilft Ihnen zu identifizieren und anfällig Benutzer vor ein tatsächlichen Angriff wirkt sich auf die Ihre bedeutsam zu finden.
  
## <a name="the-attacks"></a>Die Angriffe

Unter Preview-Version bietet drei Arten von Angriff Simulationen, die Sie ausführen können:
  
- [Anzeigen von Namen Spear-Phishing-Angriff](attack-simulator.md#spearphish)
    
- [Kennwort Sprühende-Angriff](attack-simulator.md#passwordspray)
    
- [Brute-Force-Angriff auf das Kennwort](attack-simulator.md#bruteforce)
    
Für ein Angriff erfolgreich gestartet werden muss das Konto, das den Angriff ausgeführt wird und angemeldet mehrstufige Authentifizierung verwenden.
  
> [!NOTE]
> Unterstützung für bedingten Zugriff wird in Kürze bereitgestellt. 
  
Angriff Simulator, in das Wertpapier Zugriff auf &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen...

Stellen Sie sicher, dass Sie und Ihre Organisation die folgenden Anforderungen für Angriff Simulator erfüllen:
  
- Ihre Organisation verfügt [Office 365 Bedrohungsanalyse](office-365-ti.md)mit Angriff Simulator sichtbar in das Wertpapier &amp; Compliance Center (Wechseln Sie zu **Threat Management** \> **Angriff Simulator**)
    
- E-Mail von Ihrer Organisation wird in Exchange Online gehostet. (Angriff Simulator ist nicht für lokale e-Mail-Server verfügbar.)
    
- Sie sind Administrator globaler Office 365
    
- Ihr Unternehmen verwendet [Multi-Factor Authentication für Office 365-Benutzer](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="display-name-spear-phishing-attack"></a>Anzeigen von Namen Spear-Phishing-Angriff

Phishing ist ein allgemeiner Begriff für eine Breite Palette von Angriffen als eine Formatvorlage Social Engineering-Angriff. Dieser Angriff konzentriert sich auf einen mehr gezielten Angriff Spear Phishing, die auf eine bestimmte Gruppe von Personen oder einer Organisation gerichtet ist. In der Regel ein angepasster Angriff mit einigen Eindringung durchgeführt, und verwenden einen Anzeigenamen ein, der die Vertrauenswürdigkeit in der Empfänger generiert wird, wie eine e-Mail-Nachricht, die es aussieht stammt Führungskraft innerhalb Ihrer Organisation.
  
Dieser Angriff konzentriert sich auf Navigate Bearbeitung, die die Meldung angezeigt wird, durch ändern den Anzeigenamen und die Quelle der Adresse stammt haben. Wenn Spear Phishing-Angriffe erfolgreich ausgeführt werden, Zugriff Internetkriminelle auf Anmeldeinformationen von Benutzern.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>Simuliert einen Spear-Phishing-Angriff

![Verfassen Sie e-Mail-Text](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
Sie können den rich-HTML-Editor direkt in das Feld **e-Mail-Text** selbst erstellen oder Arbeiten mit HTML-Quelle. Es gibt zwei wichtige Felder für die Einbeziehung in der HTML-Code ein: 
  
1. In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.
    
2. Geben Sie einen sinnvollen Kampagnennamen für den Angriff, oder wählen Sie eine Vorlage aus.
    
    ![Phishing-Startseite](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. Geben Sie die Ziel-Empfänger. Dies kann Personen oder Gruppen in Ihrer Organisation sein. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.
    
    ![Empfänger Auswahl](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. Konfigurieren Sie die Details der Phishing-e-Mail.
    
    ![Konfigurieren von e-Mail-details](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
  
    Die HTML-Formatierung möglicherweise als komplexe oder grundlegende wie Ihre Kampagne benötigen. Es sich um HTML handelt, können Sie Bilder und Text Believability optimiert einfügen. Sie können bestimmen, auf die empfangene Meldung in der empfangenden e-Mail-Client aussehen.
    
1. Geben Sie Text für das Feld **von (Name)** . Dies ist das Feld, das den **Anzeigenamen** in den Empfang von e-Mail-Client anzeigt. 
    
2. Geben Sie Text oder auf das Feld **aus** . Dies ist das Feld, das zeigt, wie die e-Mail-Adresse des Absenders in der Empfang von e-Mail-Client. 
    
    > [!IMPORTANT]
    > Sie können einen vorhandenen e-Mail-Namespace innerhalb Ihrer Organisation eingeben (auf diese Weise wird stellen die e-Mail-Adresse, die tatsächlich in der empfangenden Client einen sehr hohen Vertrauensmodell Erleichterung beheben), oder Sie können eine externe e-Mail-Adresse eingeben. Die e-Mail-Adresse, die Sie noch nicht existieren tatsächlich angeben, aber es muss das Format der eine gültige SMTP-Adresse, wie beispielsweise user@domainname.extension folgen. 
  
3. Wählen Sie die Dropdown-Auswahl mit einen Phishing Anmelde-Server-URL, die den Typ des Inhalts widerspiegelt innerhalb Ihrer Angriff haben. Mehrere entsprechendes mit Design versehenes URLs werden für Sie auswählen, wie etwa Dokument Übermittlung, technische, Lohn und Gehalt usw. bereitgestellt. Dies ist effektiv die URL, die vorgesehenen Benutzer aufgefordert werden, klicken Sie auf.
    
4. Geben Sie einen benutzerdefinierten Zielseite Seiten-URL ein. Mit diesem werden Benutzer auf eine URL weitergeleitet, die Sie am Ende einer erfolgreichen Angriff angeben. Wenn Sie interne zur Förderung des Bekanntheitsgrads Schulung verfügen, z. B. soll, die hier.
    
5. Geben Sie Text für das Feld **Betreff** ein. Dies ist das Feld, das zeigt, wie der **Antragstellername** in der Empfang von e-Mail-Client. 
    
5. Erstellen Sie den **e-Mail-Text** , der das Ziel des Vorgangs erhalten soll. 
  
 **${Benutzername}** fügt den Zielen Namen in der e-Mail-Text 
  
 **${Loginserverurl}** fügt die URL, die wir Zielbenutzer klicken Sie auf sollen 
    
6. Wählen Sie **Weiter,** und klicken Sie dann **Fertig stellen,** um den Angriff zu starten. Die Spear Phishing-e-Mail-Nachricht wird an die Postfächer Ihrer Ziel Empfänger übermittelt. 
    
## <a name="password-spray-attack"></a>Kennwort Sprühende-Angriff

Ein Aerosol Angriff das Kennwort einer Organisation wird normalerweise verwendet, nachdem ein Akteur Bad erfolgreich eine Liste der gültigen Benutzer von den Mandanten mit Kenntnisse von häufig verwendeten Kennwörter aufgelistet ist. Es ist Auslastung weit unverändert einen billig Angriff ausführen und schwerer als brute-Force-Ansätze erkannt.
  
Dieser Angriff konzentriert sich auf lassen Sie ein allgemeine Kennwort anhand einer großen Ziel Basis von Benutzern angeben.
  
### <a name="to-simulate-a-password-spray-attack"></a>Können Sie das Kennwort Sprühende-Angriff

1. In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.
    
2. Geben Sie einen sinnvollen Kampagnennamen für den Angriff.
    
3. Geben Sie die Ziel-Empfänger. Dies kann Personen oder Gruppen in Ihrer Organisation sein. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.
    
4. Geben Sie ein Kennwort für den Angriff verwenden. Beispielsweise ist eine gängige und relevante Kennwort könnten Sie versuchen `Fall2017`. Eine andere möglicherweise `Spring2018`, oder `Password1`.
    
5. Wählen Sie auf **Fertig stellen** , um den Angriff zu starten. 
    
## <a name="brute-force-password-attack"></a>Brute-Force-Angriff auf das Kennwort

Ein Password Brute-Force-Angriff auf einer Organisation wird normalerweise verwendet, nachdem ein Akteur Bad erfolgreich eine Liste der wichtigsten Benutzer aus den Mandanten aufgelistet ist. Dieser Angriff konzentriert sich auf lassen Sie eine Gruppe von Kennwörtern für einen einzelnen Benutzer angeben.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>Simuliert einen Password Brute-Force-Angriff

1. In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.
    
2. Geben Sie einen sinnvollen Kampagnennamen für den Angriff.
    
3. Geben Sie den Empfänger weiter. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.
    
4. Geben Sie eine Gruppe von Kennwörtern für den Angriff verwenden. Beispielsweise ist eine gängige und relevante Kennwort könnten Sie versuchen `Fall2017`. Eine andere möglicherweise `Spring2018`, oder `Password1`.
    
5. Wählen Sie auf **Fertig stellen** , um den Angriff zu starten. 
    
## <a name="related-topics"></a>Verwandte Themen

[Informationen zu Bedrohungen in Office 365](office-365-ti.md)
  

