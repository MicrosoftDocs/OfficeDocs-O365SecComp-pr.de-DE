---
title: Versionshinweise zu Advanced eDiscovery (Preview)
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
description: Dieser Artikel enthält die Versionshinweise zu Advanced eDiscovery (Preview).
ms.openlocfilehash: 32a02c16fd30e740fcc6e1c99b46775b97590a28
ms.sourcegitcommit: 15202bba32313534da2478b0cd215f32a10c9ef4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "30684354"
---
# <a name="release-notes-for-advanced-ediscovery-preview"></a>Versionshinweise zu Advanced eDiscovery (Preview)

Das öffentliche Vorschauprogramm für Advanced eDiscovery ist die Möglichkeit, frühzeitig Zugriff auf die bevorstehenden Funktionen und Updates zu erhalten. Wenn Sie frühzeitig auf die neuesten Funktionen zugreifen möchten, erstellen Sie einfach einen Advanced eDiscovery (Preview)-Fall im Office 365 Security & Compliance Center. Weitere Informationen finden Sie unter [Create a New Case](create-new-ediscovery-case.md).

## <a name="known-issues"></a>Bekannte Probleme

**Microsoft Forms**

- Die Daten, die einem Formular entsprechen, das vor dem 31. Januar 2019 erstellt wurde, können nicht durchsucht werden, wenn das Such Tool in Advanced eDiscovery (Preview) zum Durchsuchen von Depot Postfächern verwendet wird. Nach diesem Datum erstellte Formulare stehen für die Suche zur Verfügung.

- Ein von einem Benutzer erstelltes Formular kann weiterhin Antworten erhalten, auch wenn der Benutzer, der das Formular erstellt hat, gelöscht wird. Die entsprechenden Daten für diese Antworten (die nach dem Löschen des Depotbank-Postfachs aufgetreten sind) können jedoch nicht durchsucht werden, wenn das Such Tool in Advanced eDiscovery (Preview) zum Durchsuchen von Depot Postfächern verwendet wird.
 
**Microsoft Sway**

- Wenn ein Benutzer eine Sway unmittelbar vor dem Löschen des Benutzerkontos für den Besitzer dieser Sway bearbeitet, sind diese Änderungen möglicherweise nicht durchsuchbar, wenn Sie das Such Tool in Advanced eDiscovery (Preview) zum Durchsuchen von Depot Postfächern verwenden. Sway blockiert Änderungen zu einem Sway, sobald es ein Signal empfängt, dass das Konto gelöscht wurde. Es gibt jedoch eine geringe Wahrscheinlichkeit, dass ein Sway bearbeitet werden kann, bevor dieses Signal empfangen wird.

## <a name="issues-fixed-in-this-release"></a>In dieser Ausgabe behobene Probleme

- DCR: Ausnahmebehandlung für nicht indizierte Elemente und verwaiste Elemente
- DCR: Benachrichtigungen halten
- DCR: Verwalter in eDiscovery

## <a name="whats-new"></a>Neuigkeiten

- **Die neu gestaltete Navigation im Security _AMP_ Compliance Center** – Advanced EDiscovery (Preview) hat ein neues Aussehen und Verhalten. Verwenden Sie Advanced eDiscovery (Preview), um einen größeren Fall Workflow zu verwalten.

- **Case Management** – zusätzliche Unterstützung für neue Falltypen. Sie können auch Ihre letzten und bevorzugten Fälle auswählen und speichern. Verfolgen und Überwachen von Aktivitäten innerhalb und über die Fälle mithilfe neuer Dashboards.

- **Depotverwaltung** – hinzufügen und Entfernen von Benutzern als Datenverwalter innerhalb eines Falls.

- **Exchange-, OneDrive-und Teams-Integration** – fügen Sie automatisch die aktuellen Postfach-, OneDrive for Business-und Microsoft Teams-Websites eines Benutzers zu einem Fall hinzu. 

- **Depot Kommunikation** – senden und Verwalten von Benachrichtigungen für zugelassene Aufbewahrungsdaten im Namen Ihrer Organisation.

- **Depot Portal** – neues Portal für Verwalter für den Zugriff auf Ihre Active Hold-Benachrichtigungen.

- **Deep Indexing** – beim erneuten durchforsten teilweise indizierter Elemente bei Bedarf.

- **Fehler** Korrektur – beheben oder Herunterladen von Verarbeitungsfehlern; Hierzu gehört die Korrektur Unterstützung für umfangreiche Dateitypen, kennwortgeschützte Dateien und vieles mehr. 

- **Verbesserungen bei der Suche** – erstellen Sie eine Suche, indem Sie Verwalter und/oder Standorte identifizieren.

- **Arbeitsmappen** – verwalten, nachverfolgen und Überwachen von statischen Dokumentsätzen.

- **Review** – verwenden Sie eine native, Text-und systemeigene Ansicht, um Dokumente zu überprüfen, die Ihrem Workingset hinzugefügt wurden.

- **Redact, Tags und Anmerkungen** – Redact Text, wendet Tags an und macht Anmerkungen, wenn Sie Dokumente überprüfen.
  
- **Analytics-powered Review**– Nutzung von eDiscovery-Analysen zum Suchen, suchen und Ausschlachten von Ergebnissen in einem Arbeitssatz.

- **Jobs** – verfolgen Sie den Status lang andauernder Prozesse.

- **Neue Überwachungsaktivitäten** – verfolgen und Anzeigen neuer Überwachungsaktivitäten für erweiterte eDiscovery.
