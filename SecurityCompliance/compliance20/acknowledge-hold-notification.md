---
title: Bestätigen einer Aufbewahrungs Benachrichtigung
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 048c85c7b8d77b9c7d3b9527640648b9ebe463d0
ms.sourcegitcommit: 5d6be2b208dbe28d5d5da057c60cf97729799c1b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/07/2019
ms.locfileid: "30465452"
---
# <a name="acknowledge-a-hold-notification"></a><span data-ttu-id="f39d7-102">Bestätigen einer Aufbewahrungsbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="f39d7-102">Acknowledge a hold notification</span></span> 
<span data-ttu-id="f39d7-103">Wenn Sie auf eine behördliche Anfrage oder Untersuchung reagieren, müssen Sie möglicherweise die Depotbank über ihre Verpflichtung zur Aufbewahrung elektronisch gespeicherter Informationen (ESI) sowie alle Materialien informieren, die für eine aktive oder drohende Rechtsmaterie relevant sein können.</span><span class="sxs-lookup"><span data-stu-id="f39d7-103">When responding to a regulatory request or investigation, you may be required to  inform custodians of their obligation to preserve electronically stored information (ESI) as well as any material that may be relevant to an active or imminent legal matter.</span></span> <span data-ttu-id="f39d7-104">Nach der Übermittlung müssen die rechtlichen Teams wissen, dass jeder Verwalter die angegebenen Anweisungen erhalten, gelesen und verstanden hat.</span><span class="sxs-lookup"><span data-stu-id="f39d7-104">Once sent, legal teams must know that each custodian has received, read, and understood, and agreed to comply with the given instructions.</span></span>

<span data-ttu-id="f39d7-105">Um die Zeit, Kosten und Anstrengungen beim Follow-up mit ihren Verwaltern zu reduzieren, ermöglicht Ihnen Advanced eDiscovery (Preview) das Senden und Nachverfolgen von Benachrichtigungen über zugelassene Aufbewahrung per e-Mail.</span><span class="sxs-lookup"><span data-stu-id="f39d7-105">To help reduce the time, cost, and effort of following up with your custodians,  Advanced eDiscovery (Preview) allows you to send and follow-up on legal hold notifications through email.</span></span> <span data-ttu-id="f39d7-106">Zusätzlich zu den e-Mail-Benachrichtigungen hat jeder Verwalter Zugriff auf ein individualisiertes Compliance-Portal, sodass Verwalter über Änderungen Ihres Verpflichtungs Status informiert werden können.</span><span class="sxs-lookup"><span data-stu-id="f39d7-106">In addition to email notices, each custodian will also have access to an individualized Compliance Portal, allowing custodians to be kept informed of changes to their obligation status.</span></span>

## <a name="email-notifications"></a><span data-ttu-id="f39d7-107">E-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="f39d7-107">Email notifications</span></span>
<span data-ttu-id="f39d7-108">Sobald eine Benachrichtigung über eine gesetzliche Aufbewahrungspflicht erteilt wurde, erhält jeder Depotbank eine eindeutige und personalisierte e-Mail mit dem definierten gesetzlichen Aufbewahrungs Vermerk und zusätzlichen Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="f39d7-108">Once a Legal Hold Notification has been issued, each custodian will receive a unique and personalized email containing your defined legal hold notice and added instructions.</span></span> 

> [!Tip] 
> <span data-ttu-id="f39d7-109">Sehen Sie sich an, wie Sie den integrierten [Kommunikations-Editor](using-communications-editor.md) verwenden können, damit Ihre Depotbank ihre Benachrichtigung anerkennen oder auf Ihr Compliance-Portal direkt über Ihre e-Mails zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="f39d7-109">See how you can use the built-in  [Communication Editor](using-communications-editor.md) to allow your custodians to acknowledge their notice or access their Compliance Portal directly from their email.</span></span>

<span data-ttu-id="f39d7-110">Basierend auf der Konfiguration Ihrer Legal Hold-Benachrichtigung erhalten Ihre depotbanks möglicherweise die folgenden Hinweise:</span><span class="sxs-lookup"><span data-stu-id="f39d7-110">Based on the configuration of your legal hold notification, your custodians may receive the following notices:</span></span> 

- <span data-ttu-id="f39d7-111">**Veröffentlichungshinweis** -Dies ist der erste Hinweis, der an Ihren Depotbank gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f39d7-111">**Issuance notice** - This is the first notice sent to your custodian.</span></span> <span data-ttu-id="f39d7-112">Dies enthält Ihre Ausstellungs Anweisungen sowie den Haltestatus, der am Ende der Nachricht angehängt ist.</span><span class="sxs-lookup"><span data-stu-id="f39d7-112">This will contain your issuance instructions as well as the hold notice appended to the end of your message.</span></span>

- <span data-ttu-id="f39d7-113">**Erinnerungshinweis** -wenn diese Option aktiviert ist, wird eine Erinnerungsnachricht an Ihre Verwalter gesendet, die auf der angegebenen Häufigkeit und dem Intervall basiert.</span><span class="sxs-lookup"><span data-stu-id="f39d7-113">**Reminder notice** - If enabled, a reminder notice will be sent to your custodians based on the specified frequency and interval.</span></span> <span data-ttu-id="f39d7-114">Die Erinnerungen werden weiterhin gesendet, bis die Depotbank ihre Benachrichtigung bestätigt hat oder die Anzahl der Erinnerungen erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="f39d7-114">The reminders will continue to be sent either until the custodian has acknowledged their notice or until the number of reminders have been exhausted.</span></span>

- <span data-ttu-id="f39d7-115">**Eskalations Hinweis** – wenn diese Option aktiviert ist, wird ein Eskalations Hinweis an Ihren Verwalter und dessen Vorgesetzten gesendet, nachdem die Mahnungs Hinweise erschöpft sind.</span><span class="sxs-lookup"><span data-stu-id="f39d7-115">**Escalation notice** - If enabled, an escalation notice will be sent to your custodian and their manager after the reminder notices have been exhausted.</span></span> <span data-ttu-id="f39d7-116">Das System sendet automatisch Eskalations Hinweise, bis die zuzuteilenden Eskalationen abgeschlossen sind oder bis der Verwalter seine Hold-Benachrichtigung bestätigt hat.</span><span class="sxs-lookup"><span data-stu-id="f39d7-116">The system will automatically send escalation notices until the alloted escalations have been completed or until the custodian acknowledges their hold notification.</span></span>

- <span data-ttu-id="f39d7-117">**Hinweis erneut ausstellen** – wenn der Inhalt der Hold-Benachrichtigung aktualisiert wird, wird die aktualisierte Nachricht automatisch an die Depotbank gesendet.</span><span class="sxs-lookup"><span data-stu-id="f39d7-117">**Re-issue notice** - During the course of an investigation, if the contents of the hold notice are updated, then the updated notice will automatically be sent to the custodian.</span></span>

- <span data-ttu-id="f39d7-118">**Release Notice** -wenn eine Depotbank aus dem Fall entlassen wird, erhalten Sie den Veröffentlichungshinweis.</span><span class="sxs-lookup"><span data-stu-id="f39d7-118">**Release notice** - When a custodian is released from the case, they will be sent the release notice.</span></span> 

## <a name="compliance-portal"></a><span data-ttu-id="f39d7-119">Compliance-Portal</span><span class="sxs-lookup"><span data-stu-id="f39d7-119">Compliance Portal</span></span>
<span data-ttu-id="f39d7-120">Zusätzlich zu den e-Mail-Benachrichtigungen hat jeder Verwalter Zugriff auf ein eindeutiges Compliance-Portal.</span><span class="sxs-lookup"><span data-stu-id="f39d7-120">In addition to the email notifications, each custodian will also have access to a unique Compliance Portal.</span></span> <span data-ttu-id="f39d7-121">Über das Portal kann jeder Verwalter seine Active Hold-Benachrichtigungen anzeigen, darauf zugreifen und diese quittieren.</span><span class="sxs-lookup"><span data-stu-id="f39d7-121">Through the portal, each custodian will be able to view, access, and acknowledge their active hold notifications.</span></span>

![Compliance-Portal für eine Depotbank](../media/CustodianPortal.jpg)
