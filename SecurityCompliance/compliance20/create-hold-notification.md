---
title: Erstellen einer gesetzlichen Aufbewahrungspflicht
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 7d2746699a427fa3c7ad3afd7cf791c61cd55249
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213095"
---
# <a name="create-a-legal-hold-notice"></a><span data-ttu-id="bec13-102">Erstellen einer gesetzlichen Aufbewahrungspflicht</span><span class="sxs-lookup"><span data-stu-id="bec13-102">Create a legal hold notice</span></span>

<span data-ttu-id="bec13-p101">Mithilfe der Advanced eDiscovery (Preview)-Depot Kommunikation können Organisationen ihren Workflow für die Kommunikation mit Depotbank verwalten. Mithilfe des Kommunikationstools können juristische Teams die Benachrichtigungen über zugelassene Warteschleife systematisch senden, sammeln und nachverfolgen. Der Prozess der flexiblen Erstellung ermöglicht es Teams auch, den Workflow für die Aufbewahrungs Benachrichtigung und den Inhalt der an die Verwalter gesendeten Benachrichtigungen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="bec13-p101">Using Advanced eDiscovery (Preview) custodian communications, organizations can manage their workflow around communicating with custodians. Through the Communications tool, legal teams can systematically send, collect, and track legal hold notifications. The flexible creation process also allows teams to customize the hold notification workflow and the content in the notices sent to custodians.</span></span> 

<span data-ttu-id="bec13-106">In diesem Artikel werden die Schritte im Workflow zum Anhalten von Benachrichtigungen erläutert.</span><span class="sxs-lookup"><span data-stu-id="bec13-106">The article outlines the steps in the hold notification workflow.</span></span>

## <a name="step-1-specify-communication-details"></a><span data-ttu-id="bec13-107">Schritt 1: Angeben von Kommunikationsdetails</span><span class="sxs-lookup"><span data-stu-id="bec13-107">Step 1: Specify communication details</span></span>

<span data-ttu-id="bec13-108">Der erste Schritt besteht darin, die entsprechenden Details für rechtliche Aufbewahrungs Hinweise oder andere Depot Kommunikationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bec13-108">The first step is to specify the appropriate details for legal hold notices or other custodian communications.</span></span> 

1. <span data-ttu-id="bec13-109">Wechseln Sie im Security & Compliance Center zu **eDiscovery _GT_ Advanced eDiscovery (Preview)** , um die Liste der Fälle in Ihrer Organisation anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bec13-109">In the Security & Compliance Center, go to **eDiscovery > Advanced eDiscovery (Preview)** to display the list of cases in your organization.</span></span>
   
2. <span data-ttu-id="bec13-110">Klicken Sie auf die Registerkarte **Kommunikation** , und klicken Sie dann auf **neue Kommunikation**.</span><span class="sxs-lookup"><span data-stu-id="bec13-110">Click the **Communications** tab, and then click **New communication**.</span></span>
   
3. <span data-ttu-id="bec13-111">Geben Sie auf der Seite **Name Communication** die folgenden (erforderlichen) Kommunikationsdetails an.</span><span class="sxs-lookup"><span data-stu-id="bec13-111">On the **Name communication** page, specify the following (required) communication details.</span></span>

    - <span data-ttu-id="bec13-112">**Name**: Dies ist der Name für die Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="bec13-112">**Name**: This is the name for the communication.</span></span>
    
    - <span data-ttu-id="bec13-p102">AusStell ender **Offizier**: in der Dropdownliste wird eine Liste mit den Fall Mitgliedern angezeigt. Jeder Hinweis, der an Verwalter gesendet wird, wird im Auftrag des angegebenen ausstellenden beauftragten gesendet.</span><span class="sxs-lookup"><span data-stu-id="bec13-p102">**Issuing officer**: The dropdown list displays a list of a case members. Each notice sent to custodians will be sent on behalf of the specified issuing officer.</span></span>

4. <span data-ttu-id="bec13-115">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bec13-115">Click **Next**.</span></span>

## <a name="step-2-define-the-portal-content"></a><span data-ttu-id="bec13-116">Schritt 2: Definieren des Portalinhalts</span><span class="sxs-lookup"><span data-stu-id="bec13-116">Step 2: Define the portal content</span></span>

<span data-ttu-id="bec13-p103">Als nächstes können Sie den Inhalt des Notiz Speichers erstellen und hinzufügen. Geben Sie auf der Seite **Portalinhalt definieren** im Assistenten zum **Erstellen** von Kommunikationen den Inhalt des Notiz Speichers an. Dieser Inhalt wird automatisch den Benachrichtigungen zu Ausstellung, erneuter Ausstellung, Erinnerung und Eskalation angefügt. Darüber hinaus werden diese Inhalte im Compliance-Portal des Depotbank angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bec13-p103">Next, you can create and add the content of the hold notice. On the **Define portal content** page in the **Create communication** wizard, specify the contents of the hold notice. This content will be automatically appended to the Issuance, Re-Issue, Reminder, and Escalation notices. Additionally, this content will appear in the custodian's Compliance Portal.</span></span> 

<span data-ttu-id="bec13-121">So erstellen Sie den Portalinhalt:</span><span class="sxs-lookup"><span data-stu-id="bec13-121">To create the portal content:</span></span>

1. <span data-ttu-id="bec13-122">Geben Sie (oder Ausschneiden und Einfügen aus einem anderen Dokument) Ihre Notiz im Textfeld für den Portalinhalt ein.</span><span class="sxs-lookup"><span data-stu-id="bec13-122">Type (or cut and paster from another document) your hold notice in the textbox for the portal content.</span></span> 

2. <span data-ttu-id="bec13-123">Fügen Sie Merge-Variablen in Ihre Nachricht ein, um den Hinweis anzupassen und das Depotschutz-Portal zu teilen.</span><span class="sxs-lookup"><span data-stu-id="bec13-123">Insert merge variables into your notice to customize the notice and share the Custodian Compliance Portal.</span></span>

3. <span data-ttu-id="bec13-124">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bec13-124">Click **Next**.</span></span>

  >[!Tip]
  ><span data-ttu-id="bec13-125">Weitere Informationen dazu, wie Sie den Inhalt und das Format des Portalinhalts anpassen können, finden Sie unter [use the Communications Editor](using-communications-editor.md).</span><span class="sxs-lookup"><span data-stu-id="bec13-125">To learn more about how to can customize the content and format of the portal content, see [Use the Communications Editor](using-communications-editor.md).</span></span>

## <a name="step-3-set-the-required-notifications"></a><span data-ttu-id="bec13-126">Schritt 3: Festlegen der erforderlichen Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bec13-126">Step 3: Set the required notifications</span></span>

<span data-ttu-id="bec13-p104">Nachdem Sie den Inhalt des Haltestatus festgelegt haben, können Sie die Workflows zum Senden und Verwalten des Benachrichtigungsprozesses einrichten. Benachrichtigungen sind e-Mail-Nachrichten, die zur Benachrichtigung und Nachverfolgung mit Depotbank gesendet werden. Jeder Verwalter, der der Kommunikation hinzugefügt wird, erhält dieselbe Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="bec13-p104">After you've defined the contents of the hold notice, you can set up the workflows around sending and managing the notification process. Notifications are email messages that are sent to notify and follow-up with custodians. Every custodian added to the communication will receive the same notification.</span></span> 

<span data-ttu-id="bec13-130">Zum Einrichten und Senden einer Aufbewahrungs Benachrichtigung müssen Sie Veröffentlichungs-, erneute Veröffentlichungs-und Versions Benachrichtigungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="bec13-130">To set up and send a hold notice, you must include Issuance, Re-Issuance, and Release notifications.</span></span>

### <a name="issuance-notification"></a><span data-ttu-id="bec13-131">Veröffentlichungs Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="bec13-131">Issuance notification</span></span> 

<span data-ttu-id="bec13-p105">Nachdem die Kommunikation erstellt wurde, wird die **Veröffentlichungs Benachrichtigung** vom angegebenen ausstellenden Offizier initiiert. Die Veröffentlichungs Benachrichtigung ist die erste Nachricht, die an die Depotbank gesendet wurde, um Sie über Ihre Aufbewahrungspflichten zu informieren.</span><span class="sxs-lookup"><span data-stu-id="bec13-p105">After the communication is created, the **Issuance Notification** is initiated by the specified Issuing Officer. The Issuance notification is the first communication sent to the custodian to inform them about their preservation obligations.</span></span> 

<span data-ttu-id="bec13-134">So erstellen Sie eine Veröffentlichungs Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="bec13-134">To create an issuance notification:</span></span>

1. <span data-ttu-id="bec13-135">Klicken Sie in der **Ausstellungs** Kachel auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="bec13-135">In the **Issuance** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bec13-p106">Fügen Sie gegebenenfalls zusätzliche Fall Mitglieder oder Mitarbeiter zu den Feldern **CC** und **Bcc** hinzu. Wenn Sie diesen Feldern mehrere Benutzer hinzufügen möchten, trennen Sie die e-Mail-Adressen durch ein Semikolon.</span><span class="sxs-lookup"><span data-stu-id="bec13-p106">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields. To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="bec13-138">Geben Sie den **Betreff** für den Hinweis an (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="bec13-138">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="bec13-p107">Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich). Beachten Sie, dass der in Schritt 2 definierte Portalinhalt am Ende der Veröffentlichungs Benachrichtigung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bec13-p107">Specify the contents or additional instructions that you would like to provide to the custodian (required). Note that the portal content you defined in Step 2 is added to the end of the issuance notice.</span></span> 
   
5. <span data-ttu-id="bec13-141">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bec13-141">Click **Save**</span></span> 

### <a name="re-issuance-notification"></a><span data-ttu-id="bec13-142">Erneute Veröffentlichungs Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="bec13-142">Re-Issuance notification</span></span> 

<span data-ttu-id="bec13-p108">Bei Fortschreiten des Falls sind möglicherweise depotbanks erforderlich, um zusätzliche oder geringere Daten beizubehalten, als Sie zuvor angewiesen wurden. Nach dem Aktualisieren des Inhalts des Notiz Speichers wird die Benachrichtigung der Verwalter zu den Änderungen an den Aufbewahrungspflichten von der erneuten Ausstellung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="bec13-p108">As the case progresses, custodians may be required to preserve additional or less data than was previously instructed. After you update the contents of the hold notice, the re-issuance notification alerts the  custodians about the changes to their preservation obligations.</span></span>

<span data-ttu-id="bec13-145">So erstellen Sie eine erneute Veröffentlichungs Benachrichtigung:</span><span class="sxs-lookup"><span data-stu-id="bec13-145">To create a re-issuance notification:</span></span> 

1. <span data-ttu-id="bec13-146">Klicken Sie in der Kachel erneut **herausstellen** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="bec13-146">In the **Reissue** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bec13-p109">Fügen Sie gegebenenfalls zusätzliche Fall Mitglieder oder Mitarbeiter zu den Feldern **CC** und **Bcc** hinzu. Wenn Sie diesen Feldern mehrere Benutzer hinzufügen möchten, trennen Sie die e-Mail-Adressen durch ein Semikolon.</span><span class="sxs-lookup"><span data-stu-id="bec13-p109">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields. To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="bec13-149">Geben Sie den **Betreff** für den Hinweis an (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="bec13-149">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="bec13-p110">Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich). Beachten Sie, dass der in Schritt 2 definierte Portalinhalt am Ende der erneuten Veröffentlichungs Benachrichtigung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bec13-p110">Specify the contents or additional instructions that you would like to provide to the custodian (required). Note that the portal content you defined in Step 2 is added to the end of the re-issuance notice.</span></span>
   
5. <span data-ttu-id="bec13-152">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bec13-152">Click **Save**.</span></span>

>[!Note]
><span data-ttu-id="bec13-p111">Wenn eine Hold-Benachrichtigung geändert wird, wird die erneute Veröffentlichungs Benachrichtigung automatisch an alle Verwalter gesendet, die der Nachricht zugewiesen sind. Nachdem die Benachrichtigung gesendet wurde, werden die Verwalter aufgefordert, ihren Haltestatus erneut anzuerkennen. Wenn Sie Mahn-oder Eskalations Workflows eingerichtet haben, werden diese ebenfalls neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="bec13-p111">If a hold notification is modified, the re-issuance notification will be automatically sent to all custodians assigned to the notice. After the notification is sent, custodians will be asked to re-acknowledge their hold notice. If you have set up any reminder or escalation workflows, these will also re-start.</span></span> 

### <a name="release-notification"></a><span data-ttu-id="bec13-156">Versions Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="bec13-156">Release notification</span></span>

<span data-ttu-id="bec13-p112">Nachdem eine Angelegenheit aufgelöst wurde oder ein depotverwalter nicht mehr Inhalte aufbewahrt, können Sie die Depotbank aus einem Fall freigeben. Wenn der Depotbank zuvor eine Hold-Benachrichtigung ausgegeben wurde, kann die Freigabemeldung verwendet werden, um Verwalter zu warnen, dass Sie von ihrer Verpflichtung befreit wurden.</span><span class="sxs-lookup"><span data-stu-id="bec13-p112">After a matter is resolved or if a custodian is no longer subject to preserve content, you can release the custodian from a case. If the custodian was previously issued a hold notice, the release notification can be used to alert custodians that they have been released from their obligation.</span></span>

<span data-ttu-id="bec13-159">So erstellen Sie eine Versions Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="bec13-159">To create a release notification:</span></span> 

1. <span data-ttu-id="bec13-160">Klicken Sie auf der **Freigabe** Kachel auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="bec13-160">In the **Release** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bec13-p113">Fügen Sie gegebenenfalls zusätzliche Fall Mitglieder oder Mitarbeiter zu den Feldern **CC** und **Bcc** hinzu. Wenn Sie diesen Feldern mehrere Benutzer hinzufügen möchten, trennen Sie die e-Mail-Adressen durch ein Semikolon.</span><span class="sxs-lookup"><span data-stu-id="bec13-p113">If necessary, add additional case members or staff to the **Cc** and **Bcc** fields. To add multiple users to these fields, separate email addresses with a semi-colon.</span></span>
   
3. <span data-ttu-id="bec13-163">Geben Sie den **Betreff** für den Hinweis an (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="bec13-163">Specify the **Subject** for the notice (required).</span></span>
   
4. <span data-ttu-id="bec13-164">Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="bec13-164">Specify the contents or additional instructions that you would like to provide to the custodian (required).</span></span>
   
5. <span data-ttu-id="bec13-165">Klicken Sie auf **Speichern** , und fahren Sie mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="bec13-165">Click **Save** and go to the next step.</span></span> 

## <a name="optional-step-4-set-the-optional-notifications"></a><span data-ttu-id="bec13-166">Optional Schritt 4: Festlegen der optionalen Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bec13-166">(Optional) Step 4: Set the optional notifications</span></span>

<span data-ttu-id="bec13-167">Optional können Sie den Workflow für die Weiterleitung mit nicht reagierenden Verwalter vereinfachen, indem Sie automatisierte Mahn-und Eskalations Benachrichtigungen erstellen und planen.</span><span class="sxs-lookup"><span data-stu-id="bec13-167">Optionally, you can simplify the workflow for following up with unresponsive custodians by creating and scheduling automated reminder and escalation notifications.</span></span>

### <a name="reminders"></a><span data-ttu-id="bec13-168">Erinnerungen</span><span class="sxs-lookup"><span data-stu-id="bec13-168">Reminders</span></span>

<span data-ttu-id="bec13-169">Nachdem Sie eine Aufbewahrungs Benachrichtigung gesendet haben, können Sie nicht reagierende Verwalter durch Definieren eines Erinnerungs Workflows nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="bec13-169">After you have sent a hold notification, you can follow-up with unresponsive custodians by defining a reminder workflow.</span></span> 

<span data-ttu-id="bec13-170">So planen Sie Erinnerungen:</span><span class="sxs-lookup"><span data-stu-id="bec13-170">To schedule reminders:</span></span>

1. <span data-ttu-id="bec13-171">Klicken Sie in der Kachel **Erinnerung** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="bec13-171">In the **Reminder** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bec13-172">Aktivieren Sie den **Erinnerungs** Workflow, indem Sie die **Status** Umschalttaste (erforderlich) einschalten.</span><span class="sxs-lookup"><span data-stu-id="bec13-172">Enable the **Reminder** workflow by turning on the **Status** toggle (required).</span></span>
   
3. <span data-ttu-id="bec13-p114">Angeben des **Intervalls für die Erinnerung (in Tagen)** (erforderlich). Dies ist die Anzahl der Tage, die gewartet werden muss, bevor die ersten und nach Verfolgungs Benachrichtigungen gesendet werden. Wenn Sie beispielsweise das Erinnerungsintervall auf 7 Tage festlegen, wird die erste Erinnerung 7 Tage nach der anfänglichen Benachrichtigung der Warteschlange gesendet. Alle nachfolgenden Erinnerungen würden auch alle 7 Tage gesendet.</span><span class="sxs-lookup"><span data-stu-id="bec13-p114">Specify the **Reminder interval (in days)** (required). This is the number of days to wait before sending the first and follow-up reminder notifications. For example, if you set the reminder interval to 7 days, then the first reminder would be sent 7 days after the hold notification was initially issued. All subsequent reminders would also be sent every 7 days.</span></span>
   
4. <span data-ttu-id="bec13-p115">Geben Sie die **Anzahl der Erinnerungen** an (erforderlich). Dieses Feld gibt an, wie viele Erinnerungen an nicht reagierende Verwalter gesendet werden. Wenn Sie beispielsweise die Anzahl der Erinnerungen auf 3 festlegen, erhält ein Verwalter maximal 3 Erinnerungen. Nachdem ein depotverwalter die Hold-Benachrichtigung bestätigt hat, werden Erinnerungen an diesen Benutzer nicht mehr gesendet.</span><span class="sxs-lookup"><span data-stu-id="bec13-p115">Specify the **Number of reminders** (required). This field specifies how many reminders to send to un-responsive custodians. For example, if you set the number of reminders to 3, then a custodian would receive a maximum of 3 reminders. After a custodian acknowledges the hold notification, reminders will no longer be sent to that user.</span></span>
   
5. <span data-ttu-id="bec13-181">Geben Sie den **Betreff** für den Hinweis an (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="bec13-181">Specify the **Subject** for the notice (required).</span></span> 
   
6. <span data-ttu-id="bec13-p116">Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich). Beachten Sie, dass der in Schritt 2 definierte Portalinhalt am Ende der Mahnungsbenachrichtigung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bec13-p116">Specify the contents or additional instructions that you would like to provide to the custodian (required). Note that the portal content you defined in Step 2 is added to the end of the reminder notice.</span></span>
   
7. <span data-ttu-id="bec13-184">Klicken Sie auf **Speichern** , und fahren Sie mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="bec13-184">Click **Save** and go the the next step.</span></span>

### <a name="escalations"></a><span data-ttu-id="bec13-185">Eskalationen</span><span class="sxs-lookup"><span data-stu-id="bec13-185">Escalations</span></span> 

<span data-ttu-id="bec13-p117">In einigen Situationen benötigen Sie möglicherweise zusätzliche Möglichkeiten zum Nachverfolgen mit nicht reagierenden Verwalter. Wenn ein depotverwalter eine Hold-Benachrichtigung nach Erhalt der angegebenen Anzahl von Erinnerungen nicht anerkennt, kann das juristische Team einen Workflow angeben, um automatisch eine Eskalations Nachricht an die Depotbank und deren Vorgesetzten zu senden.</span><span class="sxs-lookup"><span data-stu-id="bec13-p117">In some situations, you may need additional ways to follow-up with unresponsive custodians. If a custodian doesn't acknowledge a hold notification after receiving the specified number of reminders, the legal team can specify a workflow to automatically send an escalation notice to the custodian and their manager.</span></span>

<span data-ttu-id="bec13-188">So planen Sie Eskalationen:</span><span class="sxs-lookup"><span data-stu-id="bec13-188">To schedule escalations:</span></span>

1. <span data-ttu-id="bec13-189">Klicken Sie \*\*\*\* in der Eskalations Kachel auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="bec13-189">In the **Escalation** tile, click **Edit**.</span></span>
   
2. <span data-ttu-id="bec13-190">Aktivieren Sie \*\*\*\* den Eskalations Workflow, indem Sie die **Status** -Umschaltfläche einschalten.</span><span class="sxs-lookup"><span data-stu-id="bec13-190">Enable the **Escalation** workflow by turning on the **Status** toggle.</span></span>
   
3. <span data-ttu-id="bec13-191">Geben Sie das **Eskalations Intervall (in Tagen)** (erforderlich) an.</span><span class="sxs-lookup"><span data-stu-id="bec13-191">Specify the **Escalation interval (in days)** (required).</span></span> 
   
4. <span data-ttu-id="bec13-p118">Geben Sie die **Anzahl der Eskalationen** an (erforderlich). Dieses Feld gibt an, wie viele Eskalationen an nicht reagierende Verwalter gesendet werden. Wenn Sie beispielsweise die Anzahl der Eskalationen auf 3 festlegen, wird eine Eskalations Benachrichtigung an die Depotbank und deren Vorgesetzten maximal 3 Mal gesendet. Nachdem ein depotverwalter die Hold-Benachrichtigung bestätigt hat, werden Eskalationen nicht mehr gesendet.</span><span class="sxs-lookup"><span data-stu-id="bec13-p118">Specify the **Number of escalations** (required). This field specifies how many escalations to send to un-responsive custodians. For example, if you set the number of escalations to 3, then an escalation notice would be sent to the custodian and their manager a maximum of 3 times. After a custodian acknowledges the hold notification, escalations will no longer be sent.</span></span> 
   
5. <span data-ttu-id="bec13-196">Geben Sie den **Betreff** für den Hinweis an (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="bec13-196">Specify the **Subject** for the notice (required).</span></span> 
   
6. <span data-ttu-id="bec13-p119">Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich). Beachten Sie, dass der in Schritt 2 definierte Portalinhalt am Ende der Eskalations Benachrichtigung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bec13-p119">Specify the contents or additional instructions that you would like to provide to the custodian (required). Note that the portal content you defined in Step 2 is added to the end of the escalation notice.</span></span>
   
7. <span data-ttu-id="bec13-199">Klicken Sie auf **Speichern** , und fahren Sie mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="bec13-199">Click **Save** and go the the next step.</span></span>
   
## <a name="step-5-assign-custodians"></a><span data-ttu-id="bec13-200">Schritt 5: Zuweisen von Verwaltern</span><span class="sxs-lookup"><span data-stu-id="bec13-200">Step 5: Assign custodians</span></span> 

<span data-ttu-id="bec13-201">Nachdem Sie den Inhalt für Benachrichtigungen abgeschlossen haben, wählen Sie die Verwalter aus, an die die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bec13-201">After you have finalized the content for notifications, select the custodians to send the notifications to.</span></span> 

<span data-ttu-id="bec13-202">So fügen Sie Verwalter hinzu:</span><span class="sxs-lookup"><span data-stu-id="bec13-202">To add custodians:</span></span>

1. <span data-ttu-id="bec13-203">Weisen Sie der Kommunikation Verwalter zu, indem Sie auf das Kontrollkästchen neben Ihrem Namen klicken.</span><span class="sxs-lookup"><span data-stu-id="bec13-203">Assign custodians to the communication by clicking the checkbox next to their name.</span></span>

    <span data-ttu-id="bec13-204">Nachdem die Kommunikation erstellt wurde, wird der Benachrichtigungs Workflow automatisch auf die ausgewählten Verwalter angewendet.</span><span class="sxs-lookup"><span data-stu-id="bec13-204">After the communication is created, the notification workflow will automatically apply to the selected custodians.</span></span>
   
2. <span data-ttu-id="bec13-205">Klicken Sie auf **weiter** , um die Kommunikationseinstellungen und Details zu überarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bec13-205">Click **Next** to review the communication settings and details.</span></span>
 
>[!NOTE]
><span data-ttu-id="bec13-206">Sie können nur Verwalter hinzufügen, die dem Fall hinzugefügt wurden und keine weitere Benachrichtigung innerhalb des Falls gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="bec13-206">You can only add custodians who have been added to the case and haven't been sent another notification within the case.</span></span>

## <a name="step-6-review-settings"></a><span data-ttu-id="bec13-207">Schritt 6: Überarbeiten der Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bec13-207">Step 6: Review settings</span></span>

<span data-ttu-id="bec13-208">Nachdem Sie die Einstellungen überprüft und auf **senden** klicken, um die Kommunikation abzuschließen, wird der Kommunikations Workflow vom System automatisch gestartet, indem der Veröffentlichungshinweis gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="bec13-208">After you review the settings and click **Send** to complete the communication, the system will automatically start the communication workflow by sending the issuance notice.</span></span>