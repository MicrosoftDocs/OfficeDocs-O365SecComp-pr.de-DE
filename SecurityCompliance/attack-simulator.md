---
title: Angriffssimulator in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/02/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Als globaler Office 365-Administrator können Sie Angriff Simulator realistische Angriff Szenarien in Ihrer Organisation ausführen. Dies hilft Ihnen zu identifizieren und anfällig Benutzer vor ein tatsächlichen Angriff Ihres Unternehmens Treffer zu finden.
ms.openlocfilehash: 3449e29197aa5a7a0b63a805ad8cc429f8f8f81b
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2019
ms.locfileid: "28015037"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="b04f1-104">Angriffssimulator in Office 365</span><span class="sxs-lookup"><span data-stu-id="b04f1-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="b04f1-p102">**Zusammenfassung** Wenn Sie ein Office 365 globaler Administrator sind und Ihre Organisation [Office 365 Bedrohungsanalyse verfügt](office-365-ti.md), können Angriff Simulator Sie realistisch Angriff Szenarien in Ihrer Organisation auszuführen. Dies hilft Ihnen zu identifizieren und anfällig Benutzer vor ein tatsächlichen Angriff wirkt sich auf die Ihre bedeutsam zu finden. Lesen Sie diesen Artikel, um mehr zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="b04f1-108">Die Angriffe</span><span class="sxs-lookup"><span data-stu-id="b04f1-108">The Attacks</span></span>

<span data-ttu-id="b04f1-109">Drei Arten von Angriff Simulationen sind derzeit verfügbar:</span><span class="sxs-lookup"><span data-stu-id="b04f1-109">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="b04f1-110">Anzeigen von Namen Spear-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="b04f1-110">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="b04f1-111">Kennwort Sprühende-Angriff</span><span class="sxs-lookup"><span data-stu-id="b04f1-111">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="b04f1-112">Brute-Force-Angriff auf das Kennwort</span><span class="sxs-lookup"><span data-stu-id="b04f1-112">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="b04f1-p103">Für ein Angriff erfolgreich gestartet werden verwenden Sie mehrstufige Authentifizierung auf das Konto, das Sie mithilfe von simulierten Angriffe ausführen. Darüber hinaus müssen Sie ein globaler Office 365-Administrator sein.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p103">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b04f1-115">Unterstützung für bedingten Zugriff wird in Kürze bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b04f1-115">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="b04f1-116">Angriff Simulator, in das Wertpapier Zugriff auf &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.</span><span class="sxs-lookup"><span data-stu-id="b04f1-116">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="b04f1-117">Bevor Sie beginnen...</span><span class="sxs-lookup"><span data-stu-id="b04f1-117">Before you begin...</span></span>

<span data-ttu-id="b04f1-118">Stellen Sie sicher, dass Sie und Ihre Organisation die folgenden Anforderungen für Angriff Simulator erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b04f1-118">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="b04f1-p104">E-Mail von Ihrer Organisation wird in Exchange Online gehostet. (Angriff Simulator ist nicht für lokale e-Mail-Server verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="b04f1-p104">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="b04f1-121">Sie sind Administrator globaler Office 365</span><span class="sxs-lookup"><span data-stu-id="b04f1-121">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="b04f1-122">Ihr Unternehmen verwendet [Multi-Factor Authentication für Office 365-Benutzer](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="b04f1-122">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="b04f1-123">Ihre Organisation verfügt [Office 365 Bedrohungsanalyse](office-365-ti.md)mit Angriff Simulator sichtbar in das Wertpapier &amp; Compliance Center (Wechseln Sie zu **Threat Management** \> **Angriff Simulator**)</span><span class="sxs-lookup"><span data-stu-id="b04f1-123">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="b04f1-124">![Threat Management - Angriff Simulator](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="b04f1-124">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="b04f1-125">Anzeigen von Namen Spear-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="b04f1-125">Display name spear-phishing attack</span></span>

<span data-ttu-id="b04f1-p105">Phishing ist ein allgemeiner Begriff für eine Breite Palette von Angriffen als eine Formatvorlage Social Engineering-Angriff. Dieser Angriff konzentriert sich auf einen mehr gezielten Angriff Spear Phishing, die auf eine bestimmte Gruppe von Personen oder einer Organisation gerichtet ist. In der Regel ein angepasster Angriff mit einigen Eindringung durchgeführt, und verwenden einen Anzeigenamen ein, der die Vertrauenswürdigkeit in der Empfänger generiert wird, wie eine e-Mail-Nachricht, die es aussieht stammt Führungskraft innerhalb Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p105">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="b04f1-p106">Dieser Angriff konzentriert sich auf Navigate Bearbeitung, die die Meldung angezeigt wird, durch ändern den Anzeigenamen und die Quelle der Adresse stammt haben. Wenn Spear Phishing-Angriffe erfolgreich ausgeführt werden, Zugriff Internetkriminelle auf Anmeldeinformationen von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p106">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="b04f1-131">Simuliert einen Spear-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="b04f1-131">To simulate a spear-phishing attack</span></span>

![Verfassen Sie e-Mail-Text](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="b04f1-133">Sie können den rich-HTML-Editor direkt in das Feld **e-Mail-Text** selbst erstellen oder Arbeiten mit HTML-Quelle.</span><span class="sxs-lookup"><span data-stu-id="b04f1-133">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="b04f1-134">In der [Sicherheit &amp; Compliance Center](https://protection.office.com), wählen Sie **Threat Management** \> **Angriff Simulator**.</span><span class="sxs-lookup"><span data-stu-id="b04f1-134">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="b04f1-135">Geben Sie einen sinnvollen Kampagnennamen für den Angriff, oder wählen Sie eine Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="b04f1-135">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![Phishing-Startseite](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="b04f1-p107">Geben Sie die Ziel-Empfänger. Dies kann Personen oder Gruppen in Ihrer Organisation sein. Jeden vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p107">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![Empfänger Auswahl](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="b04f1-141">Konfigurieren Sie die Details der Phishing-e-Mail.</span><span class="sxs-lookup"><span data-stu-id="b04f1-141">Configure the Phishing email details.</span></span> <br/>![Konfigurieren von e-Mail-details](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="b04f1-p108">Die HTML-Formatierung möglicherweise als komplexe oder grundlegende wie Ihre Kampagne benötigen. Das e-Mail-Format um HTML handelt, können Sie Bilder und Text Believability optimiert einfügen. Sie können bestimmen, auf die empfangene Meldung in der empfangenden e-Mail-Client aussehen.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p108">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="b04f1-p109">Geben Sie Text für das Feld **von (Name)** . Dies ist das Feld, das den **Anzeigenamen** in den Empfang von e-Mail-Client anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p109">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="b04f1-p110">Geben Sie Text oder auf das Feld **aus** . Dies ist das Feld, das zeigt, wie die e-Mail-Adresse des Absenders in der Empfang von e-Mail-Client.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p110">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="b04f1-p111">Sie können einen vorhandenen e-Mail-Namespace innerhalb Ihrer Organisation eingeben (auf diese Weise wird stellen die e-Mail-Adresse, die tatsächlich in der empfangenden Client einen sehr hohen Vertrauensmodell Erleichterung beheben), oder Sie können eine externe e-Mail-Adresse eingeben. Die e-Mail-Adresse, die Sie noch nicht existieren tatsächlich angeben, aber es muss das Format der eine gültige SMTP-Adresse, wie beispielsweise user@domainname.extension folgen.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p111">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="b04f1-p112">Wählen Sie die Dropdown-Auswahl mit einen Phishing Anmelde-Server-URL, die den Typ des Inhalts widerspiegelt innerhalb Ihrer Angriff haben. Mehrere entsprechendes mit Design versehenes URLs werden für Sie auswählen, wie etwa Dokument Übermittlung, technische, Lohn und Gehalt usw. bereitgestellt. Dies ist effektiv die URL, die vorgesehenen Benutzer aufgefordert werden, klicken Sie auf.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p112">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="b04f1-p113">Geben Sie einen benutzerdefinierten Zielseite Seiten-URL. Mit diesem werden Benutzer auf eine URL weitergeleitet, die Sie am Ende einer erfolgreichen Angriff angeben. Wenn Sie interne zur Förderung des Bekanntheitsgrads Schulung verfügen, z. B. soll, die hier.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p113">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="b04f1-p114">Geben Sie Text für das Feld **Betreff** . Dies ist das Feld, das zeigt, wie der **Antragstellername** in der Empfang von e-Mail-Client.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p114">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="b04f1-159">Erstellen Sie den **e-Mail-Text** , der das Ziel des Vorgangs erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="b04f1-159">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="b04f1-160">`${username}`der Name der Ziele in den e-Mail-Text eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b04f1-160">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="b04f1-161">`${loginserverurl}`Fügt die URL, die wir Zielbenutzer klicken Sie auf sollen</span><span class="sxs-lookup"><span data-stu-id="b04f1-161">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="b04f1-p115">Wählen Sie **Weiter,** und klicken Sie dann **Fertig stellen,** um den Angriff zu starten. Die Spear Phishing-e-Mail-Nachricht wird an die Postfächer Ihrer Ziel Empfänger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p115">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="b04f1-164">Kennwort Sprühende-Angriff</span><span class="sxs-lookup"><span data-stu-id="b04f1-164">Password-spray attack</span></span>

<span data-ttu-id="b04f1-p116">Ein Aerosol Angriff das Kennwort einer Organisation wird normalerweise verwendet, nachdem ein Akteur Bad erfolgreich eine Liste der gültigen Benutzer aus den Mandanten erworben hat. Der Akteur "Bad" weiß über allgemeine Kennwörter, die für die Personensuche verwenden. Dies ist eine weit verbreitete Angriff unverändert einen billig Angriff ausführen und schwerer als brute-Force-Ansätze erkannt.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p116">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="b04f1-168">Dieser Angriff konzentriert sich auf lassen Sie ein allgemeine Kennwort anhand einer großen Ziel Basis von Benutzern angeben.</span><span class="sxs-lookup"><span data-stu-id="b04f1-168">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="b04f1-169">Können Sie das Kennwort Sprühende-Angriff</span><span class="sxs-lookup"><span data-stu-id="b04f1-169">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="b04f1-170">In der [Sicherheit &amp; Compliance Center](https://protection.office.com), wählen Sie **Threat Management** \> **Angriff Simulator**.</span><span class="sxs-lookup"><span data-stu-id="b04f1-170">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="b04f1-171">Geben Sie einen sinnvollen Kampagnennamen für den Angriff.</span><span class="sxs-lookup"><span data-stu-id="b04f1-171">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="b04f1-p117">Geben Sie die Ziel-Empfänger. Dies kann Personen oder Gruppen in Ihrer Organisation sein. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p117">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="b04f1-p118">Geben Sie ein Kennwort für den Angriff verwenden. Beispielsweise ist eine gängige und relevante Kennwort könnten Sie versuchen `Fall2017`. Eine andere möglicherweise `Spring2018`, oder `Password1`.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p118">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="b04f1-178">Wählen Sie auf **Fertig stellen** , um den Angriff zu starten.</span><span class="sxs-lookup"><span data-stu-id="b04f1-178">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="b04f1-179">Brute-Force-Angriff auf das Kennwort</span><span class="sxs-lookup"><span data-stu-id="b04f1-179">Brute-force password attack</span></span>

<span data-ttu-id="b04f1-p119">Ein Password Brute-Force-Angriff auf einer Organisation wird normalerweise verwendet, nachdem ein Akteur Bad erfolgreich eine Liste der wichtigsten Benutzer aus den Mandanten erworben hat. Dieser Angriff konzentriert sich auf versucht, eine Gruppe von Kennwörtern für einen Einzelbenutzer-Konto.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p119">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="b04f1-182">Simuliert einen Password Brute-Force-Angriff</span><span class="sxs-lookup"><span data-stu-id="b04f1-182">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="b04f1-183">In der [Sicherheit &amp; Compliance Center](https://protection.office.com), wählen Sie **Threat Management** \> **Angriff Simulator**.</span><span class="sxs-lookup"><span data-stu-id="b04f1-183">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="b04f1-184">Geben Sie einen sinnvollen Kampagnennamen für den Angriff.</span><span class="sxs-lookup"><span data-stu-id="b04f1-184">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="b04f1-p120">Geben Sie den Empfänger weiter. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p120">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="b04f1-p121">Geben Sie eine Gruppe von Kennwörtern für den Angriff verwenden. Zu diesem Zweck können Sie eine Textdatei (txt) für die Liste der Kennwörter verwenden. Die Datei darf 10 MB Dateigröße nicht überschreiten. Verwenden Sie ein Kennwort pro Zeile, und stellen Sie sicher, dass Sie eine Absatzmarke hinter das letzte Kennwort in der Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p121">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="b04f1-191">Wählen Sie auf **Fertig stellen** , um den Angriff zu starten.</span><span class="sxs-lookup"><span data-stu-id="b04f1-191">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="b04f1-192">Neue Features in Angriff Simulator</span><span class="sxs-lookup"><span data-stu-id="b04f1-192">New features in Attack Simulator</span></span>

<span data-ttu-id="b04f1-p122">Angriff Simulator werden neue Features hinzugefügt wird. Dazu zählen folgende:</span><span class="sxs-lookup"><span data-stu-id="b04f1-p122">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="b04f1-p123">**Reporting-Funktionen erweitert**. Sie können Daten wie die schnellste (oder langsamste) Uhrzeit, eine e-Mail-Nachricht Angriff Simulation, die schnellste (oder langsamste) zu öffnen, auf einen Link in der Nachricht sehen sein.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p123">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="b04f1-p124">**E-Mail-Vorlagen-Editor**. Sie können eine benutzerdefinierte, wieder verwendbare e-Mail-Vorlage erstellen, die Sie für zukünftige Angriff Simulationen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b04f1-p124">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="b04f1-199">Besuchen Sie die [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) , um herauszufinden, was bei der Entwicklung ist, was Rollout wird und was bereits gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b04f1-199">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>



