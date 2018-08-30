---
title: Installieren der Aufsicht-add-Ins für Outlook desktop
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- ZOL160
ms.assetid: 6c5620e6-aba3-4910-8f3a-b55451656ff7
description: Installieren der Office 365-Überwachung-add-Ins für die Desktopversion von Outlook
ms.openlocfilehash: 0bddf305087bf0d9552c7671da5306db8352143f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528963"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a><span data-ttu-id="597bf-103">Installieren der Aufsicht-add-Ins für Outlook desktop</span><span class="sxs-lookup"><span data-stu-id="597bf-103">Install the Supervision add-in for Outlook desktop</span></span>

<span data-ttu-id="597bf-p101">Communications identifiziert durch eine Richtlinie für Überwachung um zu überprüfen, der Bearbeiter Verwendung der Aufsicht-add-in für Outlook und Outlook web app. Das Add-In wird automatisch in Outlook Web app für alle Bearbeiter installiert, die Sie in der Richtlinie angegeben. Bearbeiter müssen jedoch über einige Schritte zur Installation in der Desktopversion von Outlook ausführen.</span><span class="sxs-lookup"><span data-stu-id="597bf-p101">To review communications identified by a supervision policy, reviewers use the Supervision add-in for Outlook and Outlook web app. The add-in is installed automatically in Outlook web app for all reviewers you specified in the policy. However, reviewers must run through some steps to install it in the desktop version of Outlook.</span></span>
  
> [!NOTE]
> <span data-ttu-id="597bf-p102">Verwenden aufsichtsrichtlinien erfordert ein Abonnement von Office 365 E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und Überwachung ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="597bf-p102">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="597bf-109">Schritt 1: Kopieren Sie die Adresse für das Postfach für die Überwachung</span><span class="sxs-lookup"><span data-stu-id="597bf-109">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="597bf-110">Um das Add-in für Outlook Desktop zu installieren, benötigen Sie die Adresse für das Postfach Überwachung, die im Rahmen des Setups Richtlinie Aufsicht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="597bf-110">To install the add-in for Outlook desktop, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="597bf-111">Wenn eine Person bereits erstellte Richtlinie, müssen Sie diese Adresse von ihnen das Add-in installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="597bf-111">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span> 
  
 <span data-ttu-id="597bf-112">**Um die Überwachung Postfachadresse ermitteln**</span><span class="sxs-lookup"><span data-stu-id="597bf-112">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="597bf-113">Melden Sie sich bei der [Sicherheit &amp; Compliance Center](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation.</span><span class="sxs-lookup"><span data-stu-id="597bf-113">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="597bf-114">Wechseln Sie zu **Daten Governance** \> **Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="597bf-114">Go to **Data governance** \> **Supervision**.</span></span>
    
3. <span data-ttu-id="597bf-115">Klicken Sie auf der aufsichtsrichtlinie, das die Kommunikation erfasst, den, die Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="597bf-115">Click the supervision policy that's gathering the communications you want to review.</span></span>
    
4. <span data-ttu-id="597bf-116">In der Richtlinie details flyoutmenü, klicken Sie unter ** Aufsicht Postfach **, kopieren Sie die Adresse.</span><span class="sxs-lookup"><span data-stu-id="597bf-116">In the policy details flyout, under ** Supervision mailbox **, copy the address.</span></span> 
    
    ![Im Abschnitt 'Postfach Überwachung' ein aufsichtsrichtlinie Details flyoutmenü mit der Überwachung Postfachadresse hervorgehoben](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a><span data-ttu-id="597bf-118">Schritt 2: Konfigurieren Sie Aufsicht Postfach für Outlook desktop Zugriff</span><span class="sxs-lookup"><span data-stu-id="597bf-118">Step 2: Configure the supervision mailbox for Outlook desktop access</span></span>

<span data-ttu-id="597bf-119">Im nächsten Schritt müssen Bearbeiter einige Exchange Online PowerShell-Befehle ausgeführt werden, sodass sie Outlook mit dem Postfach Aufsicht verbinden können.</span><span class="sxs-lookup"><span data-stu-id="597bf-119">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="597bf-p103">Herstellen einer Verbindung mit Exchange Online PowerShell. [Wie kann ich tun, dies?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="597bf-p103">Connect to Exchange Online PowerShell. [How do I do this?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span></span>
    
2. <span data-ttu-id="597bf-122">Führen Sie die folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="597bf-122">Run the following commands.</span></span>
    
  ```
  Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccessSet-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false
  ```

    <span data-ttu-id="597bf-123">Wobei *SupervisoryReview{GUID}@domain.onmicrosoft.com* ist die Adresse, die Sie in Schritt 1 kopiert haben, und *Benutzer* ist der Name des Bearbeiters, die an das Postfach "Überwachung" im nächsten Schritt eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="597bf-123">Where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in the next step.</span></span> 
    
3. <span data-ttu-id="597bf-124">Warten Sie mindestens eine Stunde, bevor Sie mit Schritt 3 fortfahren.</span><span class="sxs-lookup"><span data-stu-id="597bf-124">Wait at least an hour before moving on to Step 3 below.</span></span>
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="597bf-125">Schritt 3: Erstellen eines Outlook-Profils für die Verbindung mit dem Postfach Überwachung</span><span class="sxs-lookup"><span data-stu-id="597bf-125">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="597bf-126">Für die letzten Schritt müssen Bearbeiter ein Outlook-Profil für das Postfach Überwachung die Verbindung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="597bf-126">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="597bf-p104">Um ein neues Outlook-Profil zu erstellen, verwenden Sie die E-Mail-Einstellungen in der Windows-Systemsteuerung. Der Pfad, den Sie durchführen, um diese Einstellungen erhalten abhängen, welches Windows-Betriebssystem (Windows 7, Windows 8 oder Windows 10) nutzen und welche Version von Outlook installiert ist.</span><span class="sxs-lookup"><span data-stu-id="597bf-p104">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel. The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using and which version of Outlook is installed.</span></span> 
  
1. <span data-ttu-id="597bf-129">Öffnen Sie die Systemsteuerung, und geben Sie in **das Suchfeld im oberen Bereich des Fensters,** **e-Mail-Nachrichten**.</span><span class="sxs-lookup"><span data-stu-id="597bf-129">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="597bf-p105">Nicht sicher, wie Sie mit der Systemsteuerungsoption abrufen? Finden Sie unter [, in der Systemsteuerung ist?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)</span><span class="sxs-lookup"><span data-stu-id="597bf-p105">Not sure how to get to the Control Panel? See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)</span></span>
  
2. <span data-ttu-id="597bf-132">Öffnen Sie die **Mail** -app.</span><span class="sxs-lookup"><span data-stu-id="597bf-132">Open the **Mail** app.</span></span> 
    
3. <span data-ttu-id="597bf-133">Klicken Sie in **Mail-Setup – Outlook**auf **Profile anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="597bf-133">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span>
    
    ![Das "Mail-Setup - Outlook" im Dialogfeld mit der Schaltfläche 'Profile anzeigen' hervorgehoben](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. <span data-ttu-id="597bf-p106">**E-Mail**klicken Sie auf **Hinzufügen**. Geben Sie dann im **Neuen Profil**, einen Namen für das Postfach Überwachung (beispielsweise **Aufsicht**).</span><span class="sxs-lookup"><span data-stu-id="597bf-p106">In **Mail**, click **Add**. Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span>
    
    ![Im Dialogfeld der 'Neues Profil' mit dem Namen "Überwachung" im Feld 'Profilname'](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. <span data-ttu-id="597bf-138">Klicken Sie in **Outlook zu Office 365 verbinden**auf **Verbindung mit einem anderen Konto herstellen**.</span><span class="sxs-lookup"><span data-stu-id="597bf-138">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span>
    
    ![Die Nachricht Outlook nach Office 365 Verbinden mit den Link 'Verbindung in ein anderes Konto' hervorgehoben](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. <span data-ttu-id="597bf-140">Klicken Sie im **Konto automatisch einrichten**wählen Sie **manuelle Installation oder zusätzliche Servertypen**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="597bf-140">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="597bf-p107">Wählen Sie **Kontotyp wählen**Sie in **Office 365**. Geben Sie dann im Feld **E-Mail-Adresse** die Adresse des Postfachs Überwachung, die Sie zuvor kopiert.</span><span class="sxs-lookup"><span data-stu-id="597bf-p107">In **Choose Your Account Type**, choose **Office 365**. Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span> 
    
    ![Die Seite 'Your Kontotyp auswählen' des Dialogfelds 'Konto hinzufügen' in Outlook mit Feld 'E-Mail-Adresse' hervorgehoben.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. <span data-ttu-id="597bf-144">Geben Sie bei Aufforderung Ihre Office 365-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="597bf-144">When prompted, enter your Office 365 credentials.</span></span>
    
9. <span data-ttu-id="597bf-145">Wenn der Vorgang erfolgreich war, sehen Sie die **Aufsicht - \<Richtlinienname\> ** Ordner aufgeführt, in der Ansicht "Ordnerliste" in Outlook.</span><span class="sxs-lookup"><span data-stu-id="597bf-145">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span> 
    

