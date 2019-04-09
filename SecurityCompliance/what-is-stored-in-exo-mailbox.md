---
title: In Exchange Online-Postfächern gespeicherte Inhalte
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
description: Daten, die von cloudbasierten apps in Office 365 erstellt werden, werden in der Microsoft-Cloud in das Exchange Online-Postfach eines Benutzers gespeichert.
ms.openlocfilehash: 6f7a81842df5972a03648a2f93d4bd6fbd738fec
ms.sourcegitcommit: 7a6c742a81bc8ebd55b5a437e835bcb85485cf99
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2019
ms.locfileid: "31520248"
---
# <a name="content-stored-in-exchange-online-mailboxes"></a>In Exchange Online-Postfächern gespeicherte Inhalte

Ein Postfach in Exchange Online wird hauptsächlich zum Speichern von e-Mail-bezogenen Elementen wie Nachrichten, Kalenderelementen, Aufgaben und Notizen verwendet. Dies ändert sich jedoch, da mehr Cloud-basierte Office 365-apps Ihre Daten auch im Postfach eines Benutzers speichern. Ein Vorteil beim Speichern von Daten in einem Postfach besteht darin, dass Sie die Such Tools in der Inhaltssuche, eDiscovery, Advanced eDiscovery und Daten Untersuchungen verwenden können, um die Daten aus diesen cloudbasierten apps zu suchen, anzuzeigen und zu exportieren. Beachten Sie, dass die Daten aus einigen dieser apps in ausgeblendeten Ordnern gespeichert sind, die sich in einer nicht-zwischenmenschlichen Nachricht (nicht-IPM) im Postfach befinden. Das bedeutet, dass die Daten aus der Benutzeransicht ausgeblendet werden, wenn Sie Outlook oder andere e-Mail-Clients verwenden, um auf Ihr Postfach zuzugreifen.

In der folgenden Tabelle sind die Office 365-apps aufgelistet, in denen Daten in einem cloudbasierten Postfach gespeichert werden. Die Tabelle beschreibt auch die Art der Inhalte, die in jeder APP gespeichert werden.

|Office 365-App  |Beschreibung  |
|:---------|:---------|
|Formulare     <br/> |Formulare (als PDF-Datei gespeichert) und Antworten auf ein Formular (in einer CSV-Datei gespeichert) werden an e-Mail-Nachrichten angefügt und in einem ausgeblendeten Ordner im Postfach des Benutzers gespeichert, der das Formular erstellt hat. Wenn Sie Inhalte aus Formularen in einer PST-Datei exportieren, befinden sich diese Daten im Ordner **ApplicationDataRoot** in einem Unterordner, der mit der folgenden Globally Unique identified (GUID) benannt ist: **c9a559d2-7aab-4f13-a6ed-e7e9c52aec87**.        <br/> |
|MyAnalytics    <br/> |   MyAnalytics bietet Benutzern Einblicke darüber, wie Sie Ihre Zeit basierend auf den e-Mails und Kalenderdaten in Ihrem Postfach verbringen. Diese Daten werden im Postfach des Benutzers in einem ausgeblendeten Ordner gespeichert. Weitere Informationen zu myAnalytics-Daten und deren Export finden Sie unter [Exportieren von Daten aus myAnalytics](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#exporting-data-from-myanalytics-and-the-office-roaming-service).      <br/> |
|Office 365-Gruppen    <br/>|  E-Mail-Nachrichten, Kalenderelemente, Kontakte (Personen), Notizen und Aufgaben werden in dem Postfach gespeichert, das einer Office 365-Gruppe zugeordnet ist.       <br/> |
|Outlook/Exchange Online<br/>|  E-Mail-Nachrichten, Kalenderelemente, Kontakte (Personen), Notizen und Aufgaben werden im Postfach eines Benutzers gespeichert.       <br/> |
|Kontakte    <br/> |  Kontakte in der Personen-App (bei denen es sich um die gleichen Kontakte wie in Outlook handelt) werden im Postfach eines Benutzers gespeichert.      <br/> |
|Planner     <br/> |   Pläne, die in Planner erstellt werden, werden im Postfach der entsprechenden Office 365-Gruppe gespeichert, die beim Erstellen eines neuen Plans bereitgestellt wird. Der Alias für das Gruppenpostfach ist der Name des Plans.      <br/> |
|Skype for Business    <br/>  | UnterHaltungen in Skype for Business werden im Ordner "Unterhaltungsverlauf" im Postfach eines Benutzers gespeichert. Wenn das Postfach eines Teilnehmers einer Skype-Besprechung in einem sperrVerfahren gespeichert oder einer Aufbewahrungsrichtlinie zugewiesen ist, werden an eine Besprechung angefügte Dateien im Teilnehmer-Postfach aufbewahrt.         <br/> |
|Sway     <br/> |  Sways werden als HTML-Datei gespeichert, die an eine e-Mail-Nachricht angefügt und in einem versteckten Ordner im Postfach des Benutzers gespeichert ist, der die Sway erstellt hat. Wenn Sie Inhalte aus Sway in eine PST-Datei exportieren, befinden sich diese Daten im Ordner **ApplicationDataRoot** in einem Unterordner, der mit der folgenden GUID benannt ist) **905fcf26-4eb7-48A0-9ff0-8dcc7194b5ba**.       <br/> |
|Aufgaben    <br/> |  Aufgaben in der Aufgaben-app (bei denen es sich um die gleichen Aufgaben wie in Outlook handelt) werden im Postfach eines Benutzers gespeichert.       <br/> |
|Teams    <br/>  |Unterhaltungen, die Teil eines Teams-Kanals sind, werden in dem Postfach gespeichert, das dem Team zugeordnet ist. UnterHaltungen, die Teil der Chat-Liste in Teams (auch als *1 X N*-Chats bezeichnet) sind, werden im Postfach der Benutzer gespeichert, die am Chat teilnehmen. Darüber hinaus werden zusammenfassende Informationen für Besprechungen und Anrufe in einem Teams-Kanal in den Postfächern der Benutzer gespeichert, die sich in die Besprechung oder den Anruf eingewählt haben. <br/> | 
|To-Do  <br/> | Tasks (als ** Aufgaben bezeichnet, die in Vorgangslisten gespeichert werden) in der to-do-App werden im Postfach eines Benutzers gespeichert.        <br/> |
||||

> [!NOTE]
> Wenn in Advanced eDiscovery (Preview) ein Depot in einem Depotbank-Postfach gespeichert wird, werden die Inhalte von Formularen und Sway nicht durch den Haltestatus beibehalten. 