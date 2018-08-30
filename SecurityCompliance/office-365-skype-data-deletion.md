---
title: Office 365 Skype für Business Daten löschen
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Eine Erläuterung der Daten löschen in Skype für Unternehmen.
ms.openlocfilehash: f3ddd0ad0797c465857919e8f7b28341492769ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529704"
---
# <a name="skype-for-business-data-deletion-in-office-365"></a>Skype für Business Daten löschen in Office 365

Skype for Business ermöglicht das Archivieren von Peer-zu-Peer-Chatnachrichten, Chatnachrichten mit mehreren Teilnehmern und das Hochladen von Inhalt in Besprechungen. Zum Archivieren ist Exchange erforderlich, und die Funktion wird vom Compliance-Archiv-Attribut für das Exchange-Postfach des Benutzers gesteuert, mit dem sowohl E-Mails als auch Skype for Business-Inhalte archiviert werden.

Die gesamte Archivierung in Skype for Business wird als "Archivierung auf Benutzerebene" bezeichnet, da sie für bestimmte Benutzer oder Benutzergruppen aktiviert bzw. deaktiviert wird, indem eine Richtlinie für die Archivierung auf Benutzerebene für diese Benutzer erstellt, konfiguriert und angewendet wird. Das Skype for Business Admin Center bietet keine Möglichkeit zum direkten Steuern von Archivierungseinstellungen.

Die folgenden Arten von Inhalt werden in Skype für Unternehmen nicht archiviert: 
- Peer-zu-Peer-Dateiübertragungen
- Audio/Video für Peer-zu-Peer-Chatnachrichten und -Konferenzen
- Anwendungsfreigaben für Peer-zu-Peer-Chatnachrichten und -Konferenzen
- Anmerkungen zu Konferenzen 

## <a name="meeting-content-retention"></a>Erfüllen der Inhaltsaufbewahrung
Kunden mit Skype für Unternehmen können Inhalte auf einer Skype für Business Besprechung als Anlagen, von PowerPoint-Präsentationen, OneNote-Dateien und andere Dateien hochladen. Der Aufbewahrungszeitraum für Inhalte, die für eine Besprechung hochgeladen wurde lautet wie folgt:
- **Einmalige Besprechung** - Inhalt wird beibehalten, beginnend bei die letzte Person die Besprechung verlässt, 15 Tage.
- **Periodisch Besprechung** - Inhalt wird beibehalten, nachdem die letzte Person die letzte Sitzung der Besprechung verlässt, 15 Tage. Der Aufbewahrung Timer zurückgesetzt, wenn jemand die gleichen Meeting-Sitzung innerhalb von 15 Tagen teilnimmt. Nehmen wir beispielsweise an, dass eine Skype für Business Besprechung geplant ist wöchentlich ein Jahr, und eine Datei mit der Besprechung während der ersten Instanz hochgeladen wird. Wenn mindestens einer Person jede Woche die Meeting-Sitzung beigetreten ist, wird die Datei beibehalten in Skype für Business Onlineserver für das gesamte Jahr plus 15 Tage nach dem letzte Person der Datenreihe die letzte Besprechung verlässt.
- **"Jetzt besprechen" meeting** - Inhalt wird beibehalten, 8 Stunden nach Ende der Besprechung.

> [!NOTE]
> Wenn ein Benutzer nicht lizenzierten ist deaktiviert (z. B., wenn **MsRTCSIP-Userenabled** auf *False*festgelegt ist), und klicken Sie dann erneut lizenziert oder wieder aktiviert, der Inhalt der Besprechung wird nicht beibehalten.

## <a name="meeting-expiration"></a>Ablauf der Besprechung
Benutzer können nach Ende einer bestimmten Besprechung auf diese zugreifen. Dafür gelten die folgenden Ablaufzeiträume:
- **Einmalige Besprechung** - Besprechung läuft 14 Tage nach Ende der geplante Besprechung ab.
- **Periodisch Besprechung mit Enddatum** - Besprechung läuft 14 Tage nach dem geplanten Ende der letzten Besprechungsinstanz ab.
- **"Jetzt besprechen" meeting** - Besprechung läuft nach 8 Stunden ab.

## <a name="whiteboard-collaboration"></a>Zusammenarbeit an Whiteboards
Anmerkungen auf Whiteboards werden von allen Teilnehmern angezeigt. Beim Speichern eines Whiteboards am Whiteboard und aller Anmerkungen werden gespeichert werden auf einen Skype für Business Server, und es wird auf dem Server entsprechend Ablaufrichtlinien für Besprechungsinhalte vom Administrator festgelegten aufbewahrt werden.

## <a name="audio-test-service"></a>Dienst zum Testen der Audioqualität
Ein Beispiel Short (etwa 5 Sekunden) für Ihre Stimme aufgezeichnet wird während des Anrufs Audiodienst zum Testen. Die sprachprobe wird von Ihnen überprüfen und/oder die Audioqualität von Ihrer Skype für Business Anruf basierend auf die Qualität der Aufzeichnung zu überprüfen. Wenn der Dienst zum Testen der Audio-Anruf wird beendet, wird die sprachprobe gelöscht.

## <a name="persistent-group-chat"></a>Permanenter Gruppenchat
Persistent Gruppenchat werden die Inhalte der Group Chat Unterhaltungen gespeichert. Wenn aktiviert, kann der Administrator steuern die Aufbewahrungszeit der Server, auf denen diese Informationen gespeichert werden, wenn für die Einhaltung von Bestimmungen oder sonstige Zwecke Gruppe Chatverlauf archiviert wird und alle Eigenschaften für einen Chatroom verwalten/ändern. Benutzer mit verschiedenen Rollen haben andere Zugriff auf die permanenten Daten wie folgt:
- Administratoren können ältere Inhalte (z. B. Inhalte, die vor einem bestimmten Datum veröffentlicht wurden) aus allen Chatrooms, um zu verhindern, dass die Größe der Datenbank erheblich wachsende löschen. Oder sie können entfernen oder Ersetzen von Nachrichten für einen bestimmten Chatroom ungeeignetes berücksichtigt (oder als nicht geeignet).
- Endbenutzer, einschließlich Autoren von Nachrichten, können keine Inhalte aus Chatrooms gelöscht.
- Chatroommanager können Chatrooms deaktivieren, aber Chatrooms können nicht gelöscht werden. Nur Administratoren können einen Chatroom löschen, nachdem er erstellt wurde.