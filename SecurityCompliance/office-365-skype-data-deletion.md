---
title: Office 365 Skype for Business-Datenlöschung
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Erklärung zum Löschen von Daten in Skype for Business.
ms.openlocfilehash: ca48a4bc57cdba7301a51cc6404a7d402166ffb0
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261303"
---
# <a name="skype-for-business-data-deletion-in-office-365"></a>Löschen von Skype for Business-Daten in Office 365

Skype for Business ermöglicht das Archivieren von Peer-zu-Peer-Chatnachrichten, Chatnachrichten mit mehreren Teilnehmern und das Hochladen von Inhalt in Besprechungen. Zum Archivieren ist Exchange erforderlich, und die Funktion wird vom Compliance-Archiv-Attribut für das Exchange-Postfach des Benutzers gesteuert, mit dem sowohl E-Mails als auch Skype for Business-Inhalte archiviert werden.

Die gesamte Archivierung in Skype for Business wird als "Archivierung auf Benutzerebene" bezeichnet, da sie für bestimmte Benutzer oder Benutzergruppen aktiviert bzw. deaktiviert wird, indem eine Richtlinie für die Archivierung auf Benutzerebene für diese Benutzer erstellt, konfiguriert und angewendet wird. Das Skype for Business Admin Center bietet keine Möglichkeit zum direkten Steuern von Archivierungseinstellungen.

Die folgenden Inhaltstypen werden in Skype for Business nicht archiviert: 
- Peer-zu-Peer-Dateiübertragungen
- Audio/Video für Peer-zu-Peer-Chatnachrichten und -Konferenzen
- Anwendungsfreigaben für Peer-zu-Peer-Chatnachrichten und -Konferenzen
- Anmerkungen zu Konferenzen 

## <a name="meeting-content-retention"></a>Erfüllen der Inhaltsaufbewahrung
Kunden, die Skype for Business verwenden, können Inhalte als Anlagen wie PowerPoint-Präsentationen, OneNote-Dateien und andere Dateien in eine Skype for Business-Besprechung hochladen. Für Inhalte, die in eine Besprechung hochgeladen werden, gilt folgende Aufbewahrungsdauer:
- **Einmalige Besprechung** -Inhalte werden 15 Tage lang aufbewahrt, beginnend mit dem Zeitpunkt, zu dem die letzte Person die Besprechung verlässt.
- Besprechungs **Serien** -Inhalt wird 15 Tage lang aufbewahrt, nachdem die letzte Person die letzte Sitzung der Besprechung verlassen hat. Der Aufbewahrungstimer wird zurückgesetzt, wenn jemand innerhalb von 15 Tagen an dieser Besprechungssitzung teilnimmt. Nehmen wir beispielsweise an, dass eine Skype for Business-Besprechung wöchentlich für ein Jahr stattfindet und eine Datei während der ersten Instanz in die Besprechung hochgeladen wird. Wenn mindestens eine Person wöchentlich an der Besprechungs Sitzung teilnimmt, wird die Datei in Skype for Business Online-Servern für das gesamte Jahr und 15 Tage nach der letzten Person, die die letzte Besprechung der Reihe verlässt, aufbewahrt.
- **Besprechung jetzt** Treffen – der Inhalt wird 8 Stunden nach der Besprechungs Endzeit aufbewahrt.

> [!NOTE]
> Wenn ein Benutzer nicht lizenziert oder deaktiviert ist (beispielsweise wenn **msRTCSIP-UserEnabled** auf *false*festgelegt ist) und dann erneut lizenziert oder erneut aktiviert wird, wird der Besprechungsinhalt nicht beibehalten.

## <a name="meeting-expiration"></a>Ablauf der Besprechung
Benutzer können nach Ende einer bestimmten Besprechung auf diese zugreifen. Dafür gelten die folgenden Ablaufzeiträume:
- **Eine einmalige Besprechungs** Besprechung läuft 14 Tage nach der geplanten Besprechungs Endzeit ab.
- Besprechungs **Serie mit Enddatum** – die Besprechung läuft 14 Tage nach der geplanten Endzeit des letzten Besprechungstermins ab.
- **Besprechung jetzt** treffen-Besprechung läuft nach 8 Stunden ab.

## <a name="whiteboard-collaboration"></a>Whiteboard-Zusammenarbeit
Anmerkungen auf Whiteboards sind für alle Teilnehmer sichtbar. Beim Speichern eines Whiteboards werden das Whiteboard und alle Anmerkungen auf einem Skype for Business-Server gespeichert, und es wird auf dem Server gemäß den vom Administrator festgelegten Ablaufrichtlinien für Besprechungsinhalte aufbewahrt.

## <a name="audio-test-service"></a>AudioTestdienst
Während des audioTest-Dienst Anrufs wird eine kurze (ungefähr 5 Sekunden) Probe ihrer Stimme aufgezeichnet. Das VoIP-Beispiel wird verwendet, um die Tonqualität Ihres Skype for Business-Anrufs anhand der Qualität der Aufzeichnung zu überprüfen und/oder zu überprüfen. Wenn der audioTest-Dienst beendet wird, wird das VoIP-Beispiel gelöscht.

## <a name="persistent-group-chat"></a>BeStändiger Gruppen Chat
Persistent Group Chat speichert den Inhalt von Gruppenchat Unterhaltungen. Wenn diese Option aktiviert ist, kann der Administrator den Aufbewahrungszeitraum, den Server, auf dem diese Informationen gespeichert sind, Steuern, wenn der Gruppen Chat Verlauf zu Compliance-oder anderen Zwecken archiviert wird, und Eigenschaften in einem Raum verwalten/ändern. Benutzer mit unterschiedlichen Rollen haben unterschiedlichen Zugriff auf die beibehaltenen Daten wie folgt:
- Administratoren können ältere Inhalte (beispielsweise Inhalte, die vor einem bestimmten Datum veröffentlicht wurden) aus einem beliebigen Chatroom löschen, um die Größe der Datenbank zu erhalten. Sie können auch Nachrichten entfernen oder ersetzen, die für einen bestimmten Chatroom als unangemessen angesehen wurden (oder als unpassend angesehen werden).
- Endbenutzer, einschließlich Nachrichten Autoren, können Inhalte aus keinem Chatroom löschen.
- Chatroommanager können Räume deaktivieren, aber keine Räume löschen. Nur Administratoren können einen Chatroom löschen, nachdem er erstellt wurde.