---
title: Installieren des Supervision-Add-Ins für Outlook-Desktop
ms.author: robmazz
author: robmazz
manager: laurawi
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
ms.openlocfilehash: b0cb0d78ab5f8887628528dd53b49fb15de44126
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180865"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a>Installieren des Supervision-Add-Ins für Outlook-Desktop

Communications identifiziert durch eine Richtlinie für Überwachung um zu überprüfen, der Bearbeiter Verwendung der Aufsicht-add-in für Outlook und Outlook web app. Das Add-In wird automatisch in Outlook Web app für alle Bearbeiter installiert, die Sie in der Richtlinie angegeben. Bearbeiter müssen jedoch über einige Schritte zur Installation in der Desktopversion von Outlook ausführen.
  
> [!NOTE]
> Benutzer von aufsichtsrichtlinien überwacht werden, müssen eine Office 365 Enterprise E3 Lizenz mit dem Add-on erweiterte Compliance oder in einem Office 365 Enterprise E5-Abonnement enthalten sein. Wenn Sie keinen vorhandenen Enterprise-E5 Plan haben und Überwachung ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Schritt 1: Kopieren Sie die Adresse für das Postfach für die Überwachung

Um das Add-in für Outlook Desktop zu installieren, benötigen Sie die Adresse für das Postfach Überwachung, die im Rahmen des Setups Richtlinie Aufsicht erstellt wurde.
  
> [!NOTE]
> Wenn eine Person bereits erstellte Richtlinie, müssen Sie diese Adresse von ihnen das Add-in installieren möchten.
 
 **Um die Überwachung Postfachadresse ermitteln**
  
1. Melden Sie sich bei der [Sicherheit &amp; Compliance Center](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation.
    
2. Wechseln Sie zu **Daten Governance** \> **Überwachung**.
    
3. Klicken Sie auf der aufsichtsrichtlinie, das die Kommunikation erfasst, den, die Sie überprüfen möchten.
    
4. In der Richtlinie details flyoutmenü, klicken Sie unter ** Aufsicht Postfach **, kopieren Sie die Adresse.<br/>![Im Abschnitt 'Postfach Überwachung' ein aufsichtsrichtlinie Details flyoutmenü mit der Überwachung Postfachadresse hervorgehoben](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>Schritt 2: Konfigurieren Sie Aufsicht Postfach für Outlook desktop Zugriff

Im nächsten Schritt müssen Bearbeiter einige Exchange Online PowerShell-Befehle ausgeführt werden, sodass sie Outlook mit dem Postfach Aufsicht verbinden können.
  
1. Herstellen einer Verbindung mit Exchange Online PowerShell. [Wie kann ich tun, dies?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)
    
2. Führen Sie die folgenden Befehle ein, wobei *SupervisoryReview{GUID}@domain.onmicrosoft.com* die Adresse an, die Sie in Schritt 1 kopiert haben, und *Benutzer* ist der Name des Bearbeiters, die an das Postfach Überwachung in Schritt 3 eine Verbindung hergestellt werden soll.
    - ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```<br/>
    - ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```
    
3. Warten Sie mindestens eine Stunde, bevor Sie mit Schritt 3 fortfahren.
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Schritt 3: Erstellen eines Outlook-Profils für die Verbindung mit dem Postfach Überwachung

Für die letzten Schritt müssen Bearbeiter ein Outlook-Profil für das Postfach Überwachung die Verbindung zu erstellen.
 
> [!NOTE]
> Um ein neues Outlook-Profil zu erstellen, verwenden Sie die E-Mail-Einstellungen in der Windows-Systemsteuerung. Der Pfad, den Sie durchführen, um diese Einstellungen erhalten abhängen, welches Windows-Betriebssystem (Windows 7, Windows 8 oder Windows 10) nutzen und welche Version von Outlook installiert ist.
  
1. Öffnen Sie die Systemsteuerung, und geben Sie in **das Suchfeld im oberen Bereich des Fensters,** **e-Mail-Nachrichten**.<br/>(Nicht sicher, wie Sie mit der Systemsteuerungsoption abrufen? Finden Sie unter [, in der Systemsteuerung ist?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))
  
2. Öffnen Sie die **Mail** -app.
    
3. Klicken Sie in **Mail-Setup – Outlook**auf **Profile anzeigen**.<br/>![Das "Mail-Setup - Outlook" im Dialogfeld mit der Schaltfläche 'Profile anzeigen' hervorgehoben](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. **E-Mail**klicken Sie auf **Hinzufügen**. Geben Sie dann im **Neuen Profil**, einen Namen für das Postfach Überwachung (beispielsweise **Aufsicht**).<br/>![Im Dialogfeld der 'Neues Profil' mit dem Namen "Überwachung" im Feld 'Profilname'](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. Klicken Sie in **Outlook zu Office 365 verbinden**auf **Verbindung mit einem anderen Konto herstellen**.<br/>![Die Nachricht Outlook nach Office 365 Verbinden mit den Link 'Verbindung in ein anderes Konto' hervorgehoben](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Klicken Sie im **Konto automatisch einrichten**wählen Sie **manuelle Installation oder zusätzliche Servertypen**, und klicken Sie dann auf **Weiter**.
    
7. Wählen Sie **Kontotyp wählen**Sie in **Office 365**. Geben Sie dann im Feld **E-Mail-Adresse** die Adresse des Postfachs Überwachung, die Sie zuvor kopiert.<br/>![Die Seite 'Your Kontotyp auswählen' des Dialogfelds 'Konto hinzufügen' in Outlook mit Feld 'E-Mail-Adresse' hervorgehoben.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Geben Sie bei Aufforderung Ihre Office 365-Anmeldeinformationen.
    
9. Wenn der Vorgang erfolgreich war, sehen Sie die **Aufsicht - \<Richtlinienname\> ** Ordner aufgeführt, in der Ansicht "Ordnerliste" in Outlook.