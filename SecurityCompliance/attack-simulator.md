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
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="80409-103">Angriff Simulator in Office 365</span><span class="sxs-lookup"><span data-stu-id="80409-103">Attack Simulator in Office 365</span></span>

<span data-ttu-id="80409-p101">Mit Angriff Simulator (enthalten in [Office 365 Bedrohungsanalyse](office-365-ti.md)) Wenn Sie Mitglied der Security-Team Ihrer Organisation sind, können Sie realistisch Angriff Szenarien in Ihrer Organisation ausführen. Dies hilft Ihnen zu identifizieren und anfällig Benutzer vor ein tatsächlichen Angriff wirkt sich auf die Ihre bedeutsam zu finden.</span><span class="sxs-lookup"><span data-stu-id="80409-p101">With Attack Simulator (included in [Office 365 Threat Intelligence](office-365-ti.md)), if you are a member of your organization's security team, you can run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="80409-106">Die Angriffe</span><span class="sxs-lookup"><span data-stu-id="80409-106">The Attacks</span></span>

<span data-ttu-id="80409-107">Unter Preview-Version bietet drei Arten von Angriff Simulationen, die Sie ausführen können:</span><span class="sxs-lookup"><span data-stu-id="80409-107">At preview release we offer three kinds of attack simulations that you can run:</span></span>
  
- [<span data-ttu-id="80409-108">Anzeigen von Namen Spear-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="80409-108">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="80409-109">Kennwort Sprühende-Angriff</span><span class="sxs-lookup"><span data-stu-id="80409-109">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="80409-110">Brute-Force-Angriff auf das Kennwort</span><span class="sxs-lookup"><span data-stu-id="80409-110">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="80409-111">Für ein Angriff erfolgreich gestartet werden muss das Konto, das den Angriff ausgeführt wird und angemeldet mehrstufige Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="80409-111">For an attack to be successfully launched, the account that is running the attack and logged on must use multi-factor authentication.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80409-112">Unterstützung für bedingten Zugriff wird in Kürze bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="80409-112">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="80409-113">Angriff Simulator, in das Wertpapier Zugriff auf &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.</span><span class="sxs-lookup"><span data-stu-id="80409-113">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="80409-114">Bevor Sie beginnen...</span><span class="sxs-lookup"><span data-stu-id="80409-114">Before you begin...</span></span>

<span data-ttu-id="80409-115">Stellen Sie sicher, dass Sie und Ihre Organisation die folgenden Anforderungen für Angriff Simulator erfüllen:</span><span class="sxs-lookup"><span data-stu-id="80409-115">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
  
- <span data-ttu-id="80409-116">Ihre Organisation verfügt [Office 365 Bedrohungsanalyse](office-365-ti.md)mit Angriff Simulator sichtbar in das Wertpapier &amp; Compliance Center (Wechseln Sie zu **Threat Management** \> **Angriff Simulator**)</span><span class="sxs-lookup"><span data-stu-id="80409-116">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span>
    
- <span data-ttu-id="80409-p102">E-Mail von Ihrer Organisation wird in Exchange Online gehostet. (Angriff Simulator ist nicht für lokale e-Mail-Server verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="80409-p102">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="80409-119">Sie sind Administrator globaler Office 365</span><span class="sxs-lookup"><span data-stu-id="80409-119">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="80409-120">Ihr Unternehmen verwendet [Multi-Factor Authentication für Office 365-Benutzer](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span><span class="sxs-lookup"><span data-stu-id="80409-120">Your organization is using [Multi-factor authentication for Office 365 users](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span></span>
    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="80409-121">Anzeigen von Namen Spear-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="80409-121">Display name spear-phishing attack</span></span>

<span data-ttu-id="80409-p103">Phishing ist ein allgemeiner Begriff für eine Breite Palette von Angriffen als eine Formatvorlage Social Engineering-Angriff. Dieser Angriff konzentriert sich auf einen mehr gezielten Angriff Spear Phishing, die auf eine bestimmte Gruppe von Personen oder einer Organisation gerichtet ist. In der Regel ein angepasster Angriff mit einigen Eindringung durchgeführt, und verwenden einen Anzeigenamen ein, der die Vertrauenswürdigkeit in der Empfänger generiert wird, wie eine e-Mail-Nachricht, die es aussieht stammt Führungskraft innerhalb Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="80409-p103">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="80409-p104">Dieser Angriff konzentriert sich auf Navigate Bearbeitung, die die Meldung angezeigt wird, durch ändern den Anzeigenamen und die Quelle der Adresse stammt haben. Wenn Spear Phishing-Angriffe erfolgreich ausgeführt werden, Zugriff Internetkriminelle auf Anmeldeinformationen von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="80409-p104">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="80409-127">Simuliert einen Spear-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="80409-127">To simulate a spear-phishing attack</span></span>

![Verfassen Sie e-Mail-Text](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="80409-p105">Sie können den rich-HTML-Editor direkt in das Feld **e-Mail-Text** selbst erstellen oder Arbeiten mit HTML-Quelle. Es gibt zwei wichtige Felder für die Einbeziehung in der HTML-Code ein:</span><span class="sxs-lookup"><span data-stu-id="80409-p105">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source. There are two important fields for inclusion in the HTML:</span></span> 
  
1. <span data-ttu-id="80409-131">In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.</span><span class="sxs-lookup"><span data-stu-id="80409-131">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="80409-132">Geben Sie einen sinnvollen Kampagnennamen für den Angriff, oder wählen Sie eine Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="80409-132">Specify a meaningful campaign name for the attack or select a template.</span></span>
    
    ![Phishing-Startseite](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="80409-p106">Geben Sie die Ziel-Empfänger. Dies kann Personen oder Gruppen in Ihrer Organisation sein. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.</span><span class="sxs-lookup"><span data-stu-id="80409-p106">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
    ![Empfänger Auswahl](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="80409-138">Konfigurieren Sie die Details der Phishing-e-Mail.</span><span class="sxs-lookup"><span data-stu-id="80409-138">Configure the Phishing email details.</span></span>
    
    ![Konfigurieren von e-Mail-details](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
  
    <span data-ttu-id="80409-p107">Die HTML-Formatierung möglicherweise als komplexe oder grundlegende wie Ihre Kampagne benötigen. Es sich um HTML handelt, können Sie Bilder und Text Believability optimiert einfügen. Sie können bestimmen, auf die empfangene Meldung in der empfangenden e-Mail-Client aussehen.</span><span class="sxs-lookup"><span data-stu-id="80409-p107">The HTML formatting can be as complex or basic as your campaign needs. As it is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
1. <span data-ttu-id="80409-p108">Geben Sie Text für das Feld **von (Name)** . Dies ist das Feld, das den **Anzeigenamen** in den Empfang von e-Mail-Client anzeigt.</span><span class="sxs-lookup"><span data-stu-id="80409-p108">Enter text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
2. <span data-ttu-id="80409-p109">Geben Sie Text oder auf das Feld **aus** . Dies ist das Feld, das zeigt, wie die e-Mail-Adresse des Absenders in der Empfang von e-Mail-Client.</span><span class="sxs-lookup"><span data-stu-id="80409-p109">Enter text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="80409-p110">Sie können einen vorhandenen e-Mail-Namespace innerhalb Ihrer Organisation eingeben (auf diese Weise wird stellen die e-Mail-Adresse, die tatsächlich in der empfangenden Client einen sehr hohen Vertrauensmodell Erleichterung beheben), oder Sie können eine externe e-Mail-Adresse eingeben. Die e-Mail-Adresse, die Sie noch nicht existieren tatsächlich angeben, aber es muss das Format der eine gültige SMTP-Adresse, wie beispielsweise user@domainname.extension folgen.</span><span class="sxs-lookup"><span data-stu-id="80409-p110">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
3. <span data-ttu-id="80409-p111">Wählen Sie die Dropdown-Auswahl mit einen Phishing Anmelde-Server-URL, die den Typ des Inhalts widerspiegelt innerhalb Ihrer Angriff haben. Mehrere entsprechendes mit Design versehenes URLs werden für Sie auswählen, wie etwa Dokument Übermittlung, technische, Lohn und Gehalt usw. bereitgestellt. Dies ist effektiv die URL, die vorgesehenen Benutzer aufgefordert werden, klicken Sie auf.</span><span class="sxs-lookup"><span data-stu-id="80409-p111">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
4. <span data-ttu-id="80409-p112">Geben Sie einen benutzerdefinierten Zielseite Seiten-URL ein. Mit diesem werden Benutzer auf eine URL weitergeleitet, die Sie am Ende einer erfolgreichen Angriff angeben. Wenn Sie interne zur Förderung des Bekanntheitsgrads Schulung verfügen, z. B. soll, die hier.</span><span class="sxs-lookup"><span data-stu-id="80409-p112">Enter a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
5. <span data-ttu-id="80409-p113">Geben Sie Text für das Feld **Betreff** ein. Dies ist das Feld, das zeigt, wie der **Antragstellername** in der Empfang von e-Mail-Client.</span><span class="sxs-lookup"><span data-stu-id="80409-p113">Enter text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
5. <span data-ttu-id="80409-156">Erstellen Sie den **e-Mail-Text** , der das Ziel des Vorgangs erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="80409-156">Compose the **Email body** that the target will receive.</span></span> 
  
 <span data-ttu-id="80409-157">**${Benutzername}** fügt den Zielen Namen in der e-Mail-Text</span><span class="sxs-lookup"><span data-stu-id="80409-157">**${username}** inserts the targets name into the Email body</span></span> 
  
 <span data-ttu-id="80409-158">**${Loginserverurl}** fügt die URL, die wir Zielbenutzer klicken Sie auf sollen</span><span class="sxs-lookup"><span data-stu-id="80409-158">**${loginserverurl}** inserts the URL we want target users to click</span></span> 
    
6. <span data-ttu-id="80409-p114">Wählen Sie **Weiter,** und klicken Sie dann **Fertig stellen,** um den Angriff zu starten. Die Spear Phishing-e-Mail-Nachricht wird an die Postfächer Ihrer Ziel Empfänger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="80409-p114">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="80409-161">Kennwort Sprühende-Angriff</span><span class="sxs-lookup"><span data-stu-id="80409-161">Password-spray attack</span></span>

<span data-ttu-id="80409-p115">Ein Aerosol Angriff das Kennwort einer Organisation wird normalerweise verwendet, nachdem ein Akteur Bad erfolgreich eine Liste der gültigen Benutzer von den Mandanten mit Kenntnisse von häufig verwendeten Kennwörter aufgelistet ist. Es ist Auslastung weit unverändert einen billig Angriff ausführen und schwerer als brute-Force-Ansätze erkannt.</span><span class="sxs-lookup"><span data-stu-id="80409-p115">A password spray attack against an organization is typically used after a bad actor has successfully enumerated a list of valid users from the tenant, utilizing their knowledge of common passwords used. It is utilized widely as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="80409-164">Dieser Angriff konzentriert sich auf lassen Sie ein allgemeine Kennwort anhand einer großen Ziel Basis von Benutzern angeben.</span><span class="sxs-lookup"><span data-stu-id="80409-164">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="80409-165">Können Sie das Kennwort Sprühende-Angriff</span><span class="sxs-lookup"><span data-stu-id="80409-165">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="80409-166">In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.</span><span class="sxs-lookup"><span data-stu-id="80409-166">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="80409-167">Geben Sie einen sinnvollen Kampagnennamen für den Angriff.</span><span class="sxs-lookup"><span data-stu-id="80409-167">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="80409-p116">Geben Sie die Ziel-Empfänger. Dies kann Personen oder Gruppen in Ihrer Organisation sein. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.</span><span class="sxs-lookup"><span data-stu-id="80409-p116">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="80409-p117">Geben Sie ein Kennwort für den Angriff verwenden. Beispielsweise ist eine gängige und relevante Kennwort könnten Sie versuchen `Fall2017`. Eine andere möglicherweise `Spring2018`, oder `Password1`.</span><span class="sxs-lookup"><span data-stu-id="80409-p117">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="80409-174">Wählen Sie auf **Fertig stellen** , um den Angriff zu starten.</span><span class="sxs-lookup"><span data-stu-id="80409-174">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="80409-175">Brute-Force-Angriff auf das Kennwort</span><span class="sxs-lookup"><span data-stu-id="80409-175">Brute-force password attack</span></span>

<span data-ttu-id="80409-p118">Ein Password Brute-Force-Angriff auf einer Organisation wird normalerweise verwendet, nachdem ein Akteur Bad erfolgreich eine Liste der wichtigsten Benutzer aus den Mandanten aufgelistet ist. Dieser Angriff konzentriert sich auf lassen Sie eine Gruppe von Kennwörtern für einen einzelnen Benutzer angeben.</span><span class="sxs-lookup"><span data-stu-id="80409-p118">A brute-force password attack against an organization is typically used after a bad actor has successfully enumerated a list of key users from the tenant. This attack focuses on letting you specify a set of passwords against a single user.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="80409-178">Simuliert einen Password Brute-Force-Angriff</span><span class="sxs-lookup"><span data-stu-id="80409-178">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="80409-179">In das Wertpapier &amp; Compliance Center, wählen Sie **Threat Management** \> **Angriff Simulator**.</span><span class="sxs-lookup"><span data-stu-id="80409-179">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="80409-180">Geben Sie einen sinnvollen Kampagnennamen für den Angriff.</span><span class="sxs-lookup"><span data-stu-id="80409-180">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="80409-p119">Geben Sie den Empfänger weiter. Ein vorgesehenen Empfänger benötigen ein Exchange Online-Postfach damit der Angriff erfolgreich zu sein.</span><span class="sxs-lookup"><span data-stu-id="80409-p119">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="80409-p120">Geben Sie eine Gruppe von Kennwörtern für den Angriff verwenden. Beispielsweise ist eine gängige und relevante Kennwort könnten Sie versuchen `Fall2017`. Eine andere möglicherweise `Spring2018`, oder `Password1`.</span><span class="sxs-lookup"><span data-stu-id="80409-p120">Specify a set of passwords to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="80409-186">Wählen Sie auf **Fertig stellen** , um den Angriff zu starten.</span><span class="sxs-lookup"><span data-stu-id="80409-186">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="related-topics"></a><span data-ttu-id="80409-187">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="80409-187">Related topics</span></span>

[<span data-ttu-id="80409-188">Informationen zu Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="80409-188">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  

