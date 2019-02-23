---
title: Angriffssimulator in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
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
ms.openlocfilehash: ba5658dfa9075b5779f8ca09ccad3547dbddcbb5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216275"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="71c2b-104">Angriffssimulator in Office 365</span><span class="sxs-lookup"><span data-stu-id="71c2b-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="71c2b-p102">**Zusammenfassung** Wenn Sie ein globaler Office 365-Administrator sind und Ihre Organisation über [office 365 Threat Intelligence](office-365-ti.md)verfügt, können Sie Angriffs Simulator verwenden, um realistische Angriffsszenarien in Ihrer Organisation auszuführen. Dies kann Ihnen dabei helfen, anfällige Benutzer zu identifizieren und zu suchen, bevor sich ein echter Angriff auf Ihr Endergebnis auswirkt. Lesen Sie diesen Artikel, um mehr zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71c2b-p103">Beginnend im Februar 2019 und über die nächsten Monate hinaus wird Office 365 Threat Intelligence zu Office 365 Advanced Threat Protection Plan 2 mit zusätzlichen Funktionen zum Schutz vor Bedrohungen. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="71c2b-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="71c2b-110">Die Angriffe</span><span class="sxs-lookup"><span data-stu-id="71c2b-110">The Attacks</span></span>

<span data-ttu-id="71c2b-111">Derzeit stehen drei Arten von Angriffssimulationen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="71c2b-111">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="71c2b-112">Anzeigename Spear-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-112">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="71c2b-113">Kenn Wort Sprüh Angriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-113">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="71c2b-114">Brute-Force-Kennwortangriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-114">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="71c2b-p104">Damit ein Angriff erfolgreich gestartet werden kann, verwenden Sie die mehrstufige Authentifizierung für das Konto, mit dem Sie simulierte Angriffe ausführen. Darüber hinaus müssen Sie ein globaler Office 365-Administrator sein.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p104">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="71c2b-117">Die Unterstützung für bedingten Zugriff wird in Kürze verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="71c2b-117">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="71c2b-118">Für den Zugriff auf Angriffs Simulator &amp; wählen Sie im Security Compliance Center **Threat Management** \> **Attack Simulator**aus.</span><span class="sxs-lookup"><span data-stu-id="71c2b-118">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="71c2b-119">Bevor Sie beginnen...</span><span class="sxs-lookup"><span data-stu-id="71c2b-119">Before you begin...</span></span>

<span data-ttu-id="71c2b-120">Stellen Sie sicher, dass Sie und Ihre Organisation die folgenden Anforderungen für anGriffs Simulator erfüllen:</span><span class="sxs-lookup"><span data-stu-id="71c2b-120">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="71c2b-p105">Die e-Mails Ihrer Organisation werden in Exchange Online gehostet. (AnGriffs Simulator ist für lokale e-Mail-Server nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="71c2b-p105">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="71c2b-123">Sie sind ein Office 365-globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="71c2b-123">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="71c2b-124">Ihre Organisation verwendet mehrstufige [Authentifizierung für Office 365-Benutzer](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="71c2b-124">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="71c2b-125">ihre organisation verfügt über [Office 365 Threat Intelligence](office-365-ti.md), mit angriffs simulator im &amp; Security Compliance Center (zum **Threat management** \> -angriffs **simulator**)</span><span class="sxs-lookup"><span data-stu-id="71c2b-125">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="71c2b-126">![Threat Management-anGriffs Simulator](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="71c2b-126">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="71c2b-127">Anzeigename Spear-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-127">Display name spear-phishing attack</span></span>

<span data-ttu-id="71c2b-p106">Phishing ist ein allgemeiner Ausdruck für eine breite Palette von Angriffen, die als Social Engineering-Angriff eingestuft werden. Dieser Angriff konzentriert sich auf Spear-Phishing, einen gezielteren Angriff, der auf eine bestimmte Gruppe von Individuen oder eine Organisation abzielt. In der Regel wird eine angepasste Angriffs Funktion mit einer gewissen Aufklärung durchgeführt und ein Anzeigename verwendet, der eine Vertrauensstellung im Empfänger generiert, beispielsweise eine e-Mail-Nachricht, die so aussieht, als ob Sie von einem Führungskräfte in Ihrer Organisation stammt.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p106">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="71c2b-p107">Dieser Angriff hat den Schwerpunkt darauf, dass Sie ändern, von wem die Nachricht scheinbar stammt, indem Sie den Anzeigenamen und die Quelladresse geändert haben. Wenn Speer-Phishing-Angriffe erfolgreich sind, erhalten Internetkriminelle Zugriff auf die Anmeldeinformationen der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p107">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="71c2b-133">So simulieren Sie einen Speer-Phishing-Angriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-133">To simulate a spear-phishing attack</span></span>

![E-Mail-Textkörper verFassen](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="71c2b-135">Sie können den Rich-HTML-Editor direkt im Feld **e-Mail-Textkörper** selbst oder mit HTML-Quelle arbeiten.</span><span class="sxs-lookup"><span data-stu-id="71c2b-135">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="71c2b-136">Wählen Sie [im &amp; Security Compliance Center](https://protection.office.com) **Threat Management** \> **Attack Simulator**aus.</span><span class="sxs-lookup"><span data-stu-id="71c2b-136">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="71c2b-137">Geben Sie einen aussagekräftigen Namen für die Kampagne an, oder wählen Sie eine Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="71c2b-137">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![Phishing-Start Seite](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="71c2b-p108">Geben Sie die Zielempfänger an. Dabei kann es sich um Einzelpersonen oder Gruppen in Ihrer Organisation handeln. Jeder Zielempfänger muss über ein Exchange Online-Postfach verfügen, damit der Angriff erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p108">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![Empfängerauswahl](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="71c2b-143">Konfigurieren Sie die Details für Phishing-e-Mails.</span><span class="sxs-lookup"><span data-stu-id="71c2b-143">Configure the Phishing email details.</span></span> <br/>![Konfigurieren von e-Mail-Details](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="71c2b-p109">Die HTML-Formatierung kann so komplex oder einfach sein, wie es Ihre Kampagne benötigt. Da das e-Mail-Format HTML ist, können Sie Bilder und Text einfügen, um Glaubwürdigkeit erhöhen zu verbessern. Sie haben die Kontrolle darüber, wie die empfangene Nachricht im empfangenden e-Mail-Client aussieht.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p109">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="71c2b-p110">Geben Sie Text für das Feld **from (Name)** an. Dies ist das Feld, das im **Anzeigenamen** im empfangenden e-Mail-Client angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p110">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="71c2b-p111">Geben Sie Text oder das Feld **von** ein. Dies ist das Feld, das als e-Mail-Adresse des Absenders im empfangenden e-Mail-Client angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p111">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="71c2b-p112">Sie können einen vorhandenen e-Mail-Namespace in Ihrer Organisation eingeben (Dadurch wird die e-Mail-Adresse tatsächlich im empfangenden Client aufgelöst, wodurch ein sehr hohes vertrauenswürdiges Modell erleichtert wird), oder Sie können eine externe e-Mail-Adresse eingeben. Die angegebene e-Mail-Adresse muss nicht tatsächlich vorhanden sein, Sie muss jedoch das Format einer gültigen SMTP-Adresse wie Benutzer @ Domänenname. Extension befolgen.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p112">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="71c2b-p113">Wählen Sie mithilfe der Dropdownauswahl eine Phishing-Anmeldeserver-URL aus, die die Art der Inhalte widerspiegelt, die Sie in ihrem Angriff haben werden. Es werden mehrere Thema-URLs bereitgestellt, aus denen Sie auswählen können, beispielsweise Dokument Zustellungen, Technik, Abrechnung usw. Dies ist die URL, auf die gezielt Benutzer klicken müssen.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p113">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="71c2b-p114">Geben Sie eine benutzerdefinierte Zielseiten-URL an. Bei Verwendung dieser Methode werden Benutzer zu einer URL umgeleitet, die Sie am Ende eines erfolgreichen Angriffs angeben. Wenn Sie beispielsweise über interne Schulungen verfügen, können Sie dies hier angeben.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p114">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="71c2b-p115">Geben Sie Text für das Feld **Betreff** an. Dies ist das Feld, das als **antragSteller Name** im empfangenden e-Mail-Client angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p115">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="71c2b-161">VerFassen Sie den **e-Mail-Text** , der vom Ziel empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="71c2b-161">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="71c2b-162">`${username}`Fügt den Namen der Ziele in den e-Mail-Text ein.</span><span class="sxs-lookup"><span data-stu-id="71c2b-162">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="71c2b-163">`${loginserverurl}`Fügt die URL ein, auf die Zielbenutzer klicken sollen.</span><span class="sxs-lookup"><span data-stu-id="71c2b-163">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="71c2b-p116">Klicken Sie auf **weiter und** dann auf **Fertig stellen** , um den Angriff zu starten. Die Spear-Phishing-e-Mail wird an die Postfächer ihrer Zielempfänger gesendet.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p116">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="71c2b-166">Kenn Wort Sprüh Angriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-166">Password-spray attack</span></span>

<span data-ttu-id="71c2b-p117">Ein Kenn Wort Sprüh Angriff gegen eine Organisation wird in der Regel verwendet, nachdem ein fehlerhafter Akteur erfolgreich eine Liste gültiger Benutzer aus dem Mandanten abgerufen hat. Der ungültige Akteur weiß um allgemeine Kennwörter, die von Benutzern verwendet werden. Hierbei handelt es sich um eine weit verbreitete Attacke, da es sich um einen billigen Angriff handelt, der nicht mehr erkannt werden kann als Brute-Force-Ansätze.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p117">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="71c2b-170">Dieser Angriff konzentriert sich darauf, dass Sie ein allgemeines Kennwort für eine umfangreiche Zielbasis von Benutzern angeben können.</span><span class="sxs-lookup"><span data-stu-id="71c2b-170">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="71c2b-171">So simulieren Sie einen Kenn Wort Sprüh Angriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-171">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="71c2b-172">Wählen Sie [im &amp; Security Compliance Center](https://protection.office.com) **Threat Management** \> **Attack Simulator**aus.</span><span class="sxs-lookup"><span data-stu-id="71c2b-172">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="71c2b-173">Geben Sie einen aussagekräftigen Kampagnennamen für den Angriff an.</span><span class="sxs-lookup"><span data-stu-id="71c2b-173">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="71c2b-p118">Geben Sie die Zielempfänger an. Dabei kann es sich um Einzelpersonen oder Gruppen in Ihrer Organisation handeln. Ein Zielempfänger muss über ein Exchange Online-Postfach verfügen, damit der Angriff erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p118">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="71c2b-p119">Geben Sie ein Kennwort für den Angriff an. Beispiel: ein gemeinsames, relevantes Kennwort, das Sie ausprobieren können, ist `Fall2017`. Eine andere kann `Spring2018`sein, `Password1`oder.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p119">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="71c2b-180">Wählen Sie **Fertig stellen** , um den Angriff zu starten.</span><span class="sxs-lookup"><span data-stu-id="71c2b-180">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="71c2b-181">Brute-Force-Kennwortangriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-181">Brute-force password attack</span></span>

<span data-ttu-id="71c2b-p120">Ein Brute-Force-Kennwortangriff gegen eine Organisation wird in der Regel verwendet, nachdem ein fehlerhafter Akteur erfolgreich eine Liste der Hauptbenutzer aus dem Mandanten abgerufen hat. Dieser Angriff zielt darauf ab, eine Reihe von Kennwörtern für das Konto eines einzelnen Benutzers zu testen.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p120">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="71c2b-184">So simulieren Sie einen Brute-Force-Kennwortangriff</span><span class="sxs-lookup"><span data-stu-id="71c2b-184">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="71c2b-185">Wählen Sie [im &amp; Security Compliance Center](https://protection.office.com) **Threat Management** \> **Attack Simulator**aus.</span><span class="sxs-lookup"><span data-stu-id="71c2b-185">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="71c2b-186">Geben Sie einen aussagekräftigen Kampagnennamen für den Angriff an.</span><span class="sxs-lookup"><span data-stu-id="71c2b-186">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="71c2b-p121">Geben Sie den Zielempfänger an. Ein Zielempfänger muss über ein Exchange Online-Postfach verfügen, damit der Angriff erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p121">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="71c2b-p122">Geben Sie einen Satz von Kennwörtern an, die für den Angriff verwendet werden sollen. Zu diesem Zweck können Sie eine Textdatei (. txt) für die Liste der Kennwörter verwenden. Die Textdatei darf nicht größer als 10 MB sein. Verwenden Sie ein Kennwort pro Leitung, und stellen Sie sicher, dass Sie nach dem letzten Kennwort in der Liste eine harte Rückgabe angeben.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p122">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="71c2b-193">Wählen Sie **Fertig stellen** , um den Angriff zu starten.</span><span class="sxs-lookup"><span data-stu-id="71c2b-193">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="71c2b-194">Neue Features im anGriffs Simulator</span><span class="sxs-lookup"><span data-stu-id="71c2b-194">New features in Attack Simulator</span></span>

<span data-ttu-id="71c2b-p123">Dem anGriffs Simulator werden neue Features hinzugefügt. Hierzu gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="71c2b-p123">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="71c2b-p124">**Erweiterte Berichterstellungsfunktionen**. Sie können beispielsweise die schnellste (oder langsamste) Zeit zum Öffnen einer e-Mail-Angriffssimulation sehen, die schnellste (oder langsamste) Zeit, um auf einen Link in der Nachricht zu klicken, und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p124">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="71c2b-p125">**E-Mail-Vorlageneditor**. Sie können eine benutzerdefinierte, wieder verwendbare e-Mail-Vorlage erstellen, die Sie für zukünftige Angriffssimulationen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="71c2b-p125">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="71c2b-201">Besuchen Sie die [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap) , um zu sehen, was sich in der Entwicklung befindet, was ausrollt und was bereits gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="71c2b-201">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>



