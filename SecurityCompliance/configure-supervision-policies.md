---
title: Konfigurieren von Aufsichtsrichtlinien für Ihre Organisation
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Richten Sie eine generelle Überprüfung Richtlinien mit Kommunikation zur Überprüfung der Mitarbeiter zu erfassen.
ms.openlocfilehash: 898ef9951ea20dec1e0cc6c28ad1ed6f9a0ded6e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29768036"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Konfigurieren von Aufsichtsrichtlinien für Ihre Organisation

Verwenden Sie aufsichtsrichtlinien Kommunikation der Mitarbeiter zur Prüfung durch interne oder externe Prüfer erfasst. Weitere Informationen dazu, wie aufsichtsrichtlinien Communications in Ihrer Organisation zu überwachen können finden Sie unter [aufsichtsrichtlinien in Office 365](supervision-policies.md).

> [!NOTE]
> Benutzer von aufsichtsrichtlinien überwacht werden, müssen eine Office 365 Enterprise E3 Lizenz mit dem Add-on erweiterte Compliance oder in einem Office 365 Enterprise E5-Abonnement enthalten sein. Wenn Sie keinen vorhandenen Enterprise-E5 Plan haben und Überwachung ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).
  
Führen Sie diese Schritte zum Einrichten und Verwenden der Überwachung in Office 365-Organisation aus:
  
- **Schritt 1 (optional)** - [-Gruppen für die Überwachung einrichten](configure-supervision-policies.md#exampledist)

    Bevor Sie mit der Überwachung beginnen, bestimmen Sie, wer werden haben ihre Kommunikation überprüft und führt, die diese Bewertungen. Wenn Sie mit nur wenigen Benutzern finden Sie unter Funktionsweise der Überwachung beginnen möchten, können Sie Gruppen für jetzt einrichten überspringen.

- **Schritt 2 (erforderlich)** - [Überwachung in Ihrer Organisation zur Verfügung stellen](configure-supervision-policies.md#MakeAvailable)

    Fügen Sie sich selbst der Rollengruppe generelle überprüfen, damit Sie Richtlinien einrichten können. Jeder Benutzer, der diese Rolle zugewiesen wurde kann auf die Seite **Überwachung** unter **Steuerung der Daten** in der & Security Compliance Center zugreifen. Wenn e-Mail überprüft werden in Exchange Online gehostet wird, benötigen Bearbeiter auch [remote PowerShell Access zu Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

- **Schritt 3 (optional)** - [Konfigurieren benutzerdefinierter vertraulichen Informationstypen oder benutzerdefinierte Schlüsselwortsuche Wörterbücher/Lexika](configure-supervision-policies.md#sensitiveinfo)

    Wenn Sie einen benutzerdefinierten vertrauliche Info-Typ oder ein benutzerdefiniertes Schlüsselwort Wörterbuch für Ihre aufsichtsrichtlinie verwenden müssen, müssen Sie sie vor dem Starten des Assistenten für die Überwachung zu erstellen.

- **Schritt 4 (erforderlich)** - [Richten Sie eine Richtlinie für Überwachung](configure-supervision-policies.md#setupsuper)

    Aufsichtsrichtlinien erstellen Sie in der & Security Compliance Center. Diese Richtlinien definieren, welche Communications Review in Ihrer Organisation unterliegen und gibt an, die überprüft werden soll. Kommunikationskomponenten umfassen e-Mail- und Microsoft-Teams Communications sowie 3rd Party Plattform Communications (z. B. Facebook, Twitter.)

- **Schritt 5: (optional)** [Testen Sie die neue Richtlinie für die Überwachung](configure-supervision-policies.md#TestPolicy)

    Testen Ihrer aufsichtsrichtlinie sicherstellen, dass es wie gewünscht funktionsfähig ist, ist ein wichtiger Teil der sicherstellen, dass Ihre Compliance-Strategie Ihrer Standards erfüllt.

- **Schritt 6: (optional)** [Einrichten von Outlook-add-in für Prüfer, die nicht Office 365 Aufsicht Dashboard oder OWA überwachten Communications überprüfen verwenden möchten](configure-supervision-policies.md#UseOutlook)

    Aufsicht-add-in für Outlook ermöglicht Bearbeiter Zugriff auf Überwachung Funktionalität rechts im Outlook-Client, damit diese bewerten und jedes Element kategorisieren.

<a name="exampledist"> </a>

## <a name="step-1---set-up-groups-for-supervision-optional"></a>Schritt 1: Einrichten von Gruppen für die Überwachung (optional)

 Wenn Sie eine Richtlinie für Überwachung erstellen, ermitteln Sie, ihre Kommunikation überprüft besitzen und wem diese Bewertungen ausgeführt werden soll. E-Mail-Adressen verwenden Sie in der Richtlinie um Personen oder Gruppen von Personen zu identifizieren. Um das Setup zu vereinfachen, Erstellen von Gruppen für Personen, die ihre Kommunikation überprüft haben, werden und Gruppen für Personen, die diese Kommunikation überprüft werden. Wenn Sie Gruppen verwenden, können Sie mehrere benötigen – beispielsweise, wenn Sie die Kommunikation zwischen zwei unterschiedlichen Gruppen von Personen überwachen möchten, oder wenn Sie möchten, um eine Gruppe anzugeben, die überwacht werden und sollte nicht zur Verfügung. Einzelheiten zur Funktionsweise finden Sie unter [Beispiel Verteilergruppen](configure-supervision-policies.md#GroupExample) .
  
Um die Kommunikation zwischen oder in Gruppen in Ihrer Organisation zu überwachen, Einrichten von Verteilergruppen in der Exchange-Verwaltungskonsole (Wechseln Sie zu **Empfänger** \> **Gruppen**). Weitere Informationen zum Einrichten von Verteilergruppen finden Sie unter [Verwalten von Verteilergruppen](http://go.microsoft.com/fwlink/?LinkId=613635)
  
> [!NOTE]
> Sie können auch dynamische Verteilergruppen oder Sicherheitsgruppen für Überwachung Falls gewünscht. Um besser entscheiden, ob diese besser Ihrer Organisation passen müssen, finden Sie in [Verwalten von e-Mail-aktivierten Sicherheitsgruppen](http://go.microsoft.com/fwlink/?LinkId=627033)und [dynamische Verteilergruppen verwalten](http://go.microsoft.com/fwlink/?LinkId=627058).
  
<a name="GroupExample"> </a>

### <a name="example-distribution-groups"></a>Beispielverteilergruppen

Dieses Beispiel enthält eine Verteilergruppe, die für eine finanzielle Organisation mit dem Namen "Contoso" finanzielle International eingerichtet wurde.
  
Im Unternehmen Contoso Financial International muss eine Stichprobe der Kommunikationen zwischen Brokern in den Vereinigten Staaten beaufsichtigt werden. Für die Compliance Officer in dieser Gruppe ist jedoch keine Aufsicht erforderlich. Für dieses Beispiel können wir die folgenden Gruppen erstellen:
  
|**Einrichten dieser Verteilergruppe**|**Gruppenadresse (Alias)**|**Beschreibung**|
|:-----|:-----|:-----|
|Alle US-Broker | US_Brokers@contoso.com | Diese Gruppe umfasst E-Mail-Adressen für alle US-basierten Broker, die für Contoso arbeiten. |
| Alle Compliance Officer für die Vereinigten Staaten | US_Compliance@contoso.com  | Diese Gruppe werden e-Mail-Adressen für alle US-basierte Compliance Officer, die für Contoso arbeiten enthält. Da dieser Gruppe eine Teilmenge der alle US-basierte Broker ist, können Sie diesen Alias, ausgenommen Compliance Officer von einer Richtlinie für Überwachung verwenden. |
  
<a name="MakeAvailable"> </a>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a>Schritt 2: Stellen Sie Überwachung in Ihrer Organisation (erforderlich)

Um die **Überwachung** in der & Security Compliance Center als Menüoption verfügbar zu machen, müssen Sie generelle Überprüfung Administratorrolle zugewiesen werden.
  
Zu diesem Zweck können sich selbst als Mitglied der Rollengruppe generelle Überprüfung entweder hinzufügen oder Sie können eine neue Rollengruppe erstellen.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Hinzufügen von Mitgliedern der Rollengruppe generelle überprüfen

1. Melden Sie sich bei [https://protection.office.com](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation.

2. Navigieren Sie in der & Security Compliance Center zu **Berechtigungen**.

3. Wählen Sie aus der Rollengruppe **Generelle Überprüfung** , und klicken Sie dann auf das Symbol bearbeiten.

4. Fügen Sie im Abschnitt **Mitglieder** die Personen, die Überwachung für Ihre Organisation verwalten soll.

### <a name="create-a-new-role-group"></a>Erstellen einer neuen Rollengruppe

1. Melden Sie sich bei [https://protection.office.com](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation.

2. In der & Security Compliance Center gehen Sie zu **Berechtigungen** , und klicken Sie dann auf Hinzufügen (**+**).

3. Klicken Sie auf Hinzufügen, klicken Sie im Abschnitt **Rollen** (**+**) und führen Sie einen Bildlauf nach unten zu **Generelle Überprüfung-Administrator**. Fügen Sie diese Rolle der Rollengruppe.

4. Fügen Sie im Abschnitt **Mitglieder** die Personen, die Überwachung für Ihre Organisation verwalten soll.

Weitere Informationen zu Rollengruppen und Berechtigungen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a>Aktivieren von PowerShell-Remotezugriff für Bearbeiter (Wenn e-Mail auf Exchange Online gehostet wird)

1. Führen Sie die Anweisungen in [Aktivieren oder Deaktivieren des Zugriffs auf Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)aus.

<a name="sensitiveinfo"> </a>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a>Schritt 3: Erstellen von benutzerdefinierten vertraulichen Informationstypen oder benutzerdefinierte Schlüsselwortsuche Wörterbücher (optional)

Um vorhandene benutzerdefinierte vertraulichen Informationstypen oder benutzerdefinierte Schlüsselwortsuche Wörterbücher im Assistenten Aufsicht auszuwählen, müssen Sie zuerst diese Elemente zu erstellen, falls erforderlich.

### <a name="create-custom-sensitive-information-types"></a>Erstellen von benutzerdefinierten vertraulichen Informationstypen

1. Erstellen eines neuen vertrauliche Informationen in der Office 365-Sicherheit & Compliance Center. Navigieren Sie zu **Klassifikationen** \> **Arten von vertraulichen Informationen** , und befolgen Sie die Schritte im **Assistenten für neue vertrauliche Informationen Typ**. Hier lernen Sie Folgendes:

    - Definieren Sie einen Namen und eine Beschreibung für den ein vertrauliche Informationen
    - Definieren der Nähe, Vertrauensstufe und primäre Muster Elemente
    - Überprüfen Sie die Auswahl, und erstellen Sie den Typ von vertraulichen Informationen

    Ausführlichere Informationen finden Sie unter [Erstellen einer benutzerdefinierten vertrauliche Informationen-Typ](create-a-custom-sensitive-information-type.md).

### <a name="create-custom-keyword-dictionarylexicon"></a>Erstellen Sie benutzerdefinierte Schlüsselwortsuche Wörterbuch/Wörterbuch

1. Erstellen Sie eine neue Datei, die die Stichwörtern enthält, den, die Sie in einer Richtlinie für Überwachung überwachen möchten, Sie mit einem Texteditor (wie beispielsweise Editor). Vergewissern Sie sich, jeden Ausdruck in einer separaten Zeile ein, und speichern Sie die Datei im **Unicode/UTF-16 (Little-Endian)** Format.
2. Importieren Sie die Schlüsselwort-Datei in Ihrem Office 365-Mandanten mit PowerShell. Zum Verbinden mit Office 365 mit PowerShell finden Sie unter [Connect to Office 365-Sicherheit & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

    Nachdem Sie mit PowerShell zu Office 365 hergestellt haben, führen Sie die folgenden Befehle zum Importieren des Schlüsselwort-Wörterbuchs:

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    Ausführlichere Informationen finden Sie unter [Erstellen eines Wörterbuchs Schlüsselwort](create-a-keyword-dictionary.md).

3. Erstellen eines neuen vertrauliche Informationen in der Office 365-Sicherheit & Compliance Center. Navigieren Sie zu **Klassifikationen** \> **Arten von vertraulichen Informationen** , und befolgen Sie die Schritte im **Assistenten für neue vertrauliche Informationen Typ**. Hier lernen Sie Folgendes:

    - Definieren Sie einen Namen und eine Beschreibung für den ein vertrauliche Informationen
    - Fügen Sie Ihrem benutzerdefinierten Wörterbuch als Voraussetzung für das übereinstimmende Element hinzu
    - Überprüfen Sie die Auswahl, und erstellen Sie den Typ von vertraulichen Informationen

    Nach dem Erstellen der benutzerdefinierten Wörterbuch-Wörterbuch können Sie die konfigurierten Schlüsselwörter mit dem Cmdlet [Get-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) anzeigen oder hinzufügen und Entfernen von Ausdrücken mithilfe des Cmdlets [Set-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) .

    Ausführlichere Informationen finden Sie unter [Erstellen einer benutzerdefinierten vertrauliche Informationen-Typ](create-a-custom-sensitive-information-type.md).

<a name="setupsuper"> </a>

## <a name="step-4---set-up-a-supervision-policy-required"></a>Schritt 4: Einrichten einer aufsichtsrichtlinie (erforderlich)
  
1. Melden Sie sich bei [https://protection.office.com](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation.

2. Wählen Sie in der & Security Compliance Center **Überwachung**.
  
3. Wählen Sie **Erstellen** aus, und führen Sie dann den Assistenten zum Einrichten von der folgenden Seiten der Richtlinie. Mithilfe des Assistenten können Sie die folgenden Schritte ausführen:

    - Geben Sie einen Namen und eine Beschreibung der Richtlinie.
    - Wählen Sie die Benutzer oder Gruppen zu überwachen, einschließlich der Auswahl von Benutzern oder Gruppen, den, die Sie ausschließen möchten.
    - Definieren Sie den Drahtloszugriff Überwachung.
    - Wählen Sie, wenn Sie mit vertraulichen Informationstypen aufnehmen möchten. Dies ist, in dem Sie Standard und benutzerdefinierten vertrauliche Informationen Typen auswählen können.
    - Definieren Sie den Prozentsatz der Kommunikation zu überprüfen.
    - Wählen Sie die Bearbeiter für die Richtlinie ein. Bearbeiter können einzelnen Benutzern oder [Gruppen e-Mail-aktivierte Sicherheitsgruppe](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group)sein.
    - Überprüfen Sie die Richtlinienauswahl und erstellen Sie die Richtlinie zu.

<a name="TestPolicy"> </a>

## <a name="step-5---test-your-supervision-policy-optional"></a>Schritt 5: Testen Sie Ihre aufsichtsrichtlinie (optional)

Nach der Erstellung einer aufsichtsrichtlinie ist es ratsam, testen Sie, um sicherzustellen, dass die Bedingungen, die Sie definiert durch die Richtlinie ordnungsgemäß umgesetzt werden. Sie sollten auch zum [Testen Ihrer Richtlinien zur Verhinderung von Datenverlust (DLP)](create-test-tune-dlp-policy.md) Wenn Ihre aufsichtsrichtlinien Typen vertraulicher Informationen enthalten. Befolgen Sie diese Schritte zum Testen der Richtlinie für Überwachung:

1. Open angemeldet ein e-Mail-Client oder Microsoft-Teams als überwachten Benutzer gemäß der Richtlinie ein, die Sie testen möchten.
2. Senden Sie eine e-Mail oder chatten Microsoft-Teams, die die Kriterien erfüllt, die Sie in der aufsichtsrichtlinie definiert haben. Dies kann ein Schlüsselwort, Anlagengröße, Domäne usw. sein. Stellen Sie sicher, dass Sie feststellen, ob Ihre bedingten konfigurierten Einstellungen in der Richtlinie zu restriktiv oder zu flexibel ist.

    > [!Note]
    > Unterliegen definierte Richtlinien-e-Mails werden nahezu in Echtzeit verarbeitet und können getestet werden, unmittelbar nachdem die Richtlinie konfiguriert ist. Chats in Microsoft-Teams können vollständig in einer Richtlinie verarbeitet bis zu 24 Stunden dauern. 

3. Melden Sie sich bei Ihrem Office 365-Mandanten als einem Bearbeiter in der aufsichtsrichtlinie festgelegt. Navigieren Sie zur **Überwachung** > *Your benutzerdefinierte Richtlinie* > **Open** um den Bericht für die Richtlinie anzuzeigen.

<a name="UseOutlook"> </a>

## <a name="step-6---set-up-outlook-add-in-for-reviewers-optional"></a>Schritt 6: Einrichten von Outlook-add-in für Bearbeiter (optional)

Prüfer, die Outlook verwenden, anstatt das Dashboard Überwachung in Office 365 oder in Outlook im Web Communications überprüfen möchten, müssen die Aufsicht-add-in für ihren Outlook-Client installieren.

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Schritt 1: Kopieren Sie die Adresse für das Postfach für die Überwachung

Um das Add-in für Outlook Desktop zu installieren, benötigen Sie die Adresse für das Postfach Überwachung, die im Rahmen des Setups Richtlinie Aufsicht erstellt wurde.
  
> [!NOTE]
> Wenn eine Person bereits erstellte Richtlinie, müssen Sie diese Adresse von ihnen das Add-in installieren möchten.

 **Um die Überwachung Postfachadresse ermitteln**
  
1. Melden Sie sich bei der [Sicherheit &amp; Compliance Center](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation.

2. Wechseln Sie zur **Überwachung**.

3. Klicken Sie auf der aufsichtsrichtlinie, das die Kommunikation erfasst, den, die Sie überprüfen möchten.

4. Kopieren Sie in der Richtlinie Details flyoutmenü unter **Aufsicht Postfach**die Adresse.<br/>![Im Abschnitt 'Postfach Überwachung' ein aufsichtsrichtlinie Details flyoutmenü mit der Überwachung Postfachadresse hervorgehoben](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>Schritt 2: Konfigurieren Sie Aufsicht Postfach für Outlook desktop Zugriff

Im nächsten Schritt müssen Bearbeiter einige Exchange Online PowerShell-Befehle ausgeführt werden, sodass sie Outlook mit dem Postfach Aufsicht verbinden können.
  
1. Herstellen einer Verbindung mit Exchange Online PowerShell. [Wie kann ich tun, dies?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. Führen Sie die folgenden Befehle ein, wobei *SupervisoryReview{GUID}@domain.onmicrosoft.com* die Adresse an, die Sie in Schritt 1 kopiert haben, und *Benutzer* ist der Name des Bearbeiters, die an das Postfach Überwachung in Schritt 3 eine Verbindung hergestellt werden soll.

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. Warten Sie mindestens eine Stunde, bevor Sie mit Schritt 3 fortfahren.

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Schritt 3: Erstellen eines Outlook-Profils für die Verbindung mit dem Postfach Überwachung

Für die letzten Schritt müssen Bearbeiter ein Outlook-Profil für das Postfach Überwachung die Verbindung zu erstellen.

> [!NOTE]
> Um ein neues Outlook-Profil zu erstellen, verwenden Sie die E-Mail-Einstellungen in der Windows-Systemsteuerung. Der Pfad, den Sie durchführen, um diese Einstellungen erhalten abhängen, welches Windows-Betriebssystem (Windows 7, Windows 8 oder Windows 10) nutzen, und welche Version von Outlook installiert ist.
  
1. Öffnen Sie die Systemsteuerung, und geben Sie in **das Suchfeld im oberen Bereich des Fensters,** **e-Mail-Nachrichten**.<br/>(Nicht sicher, wie Sie mit der Systemsteuerungsoption abrufen? Finden Sie unter [, in der Systemsteuerung ist?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))
  
2. Öffnen Sie die **Mail** -app.

3. Klicken Sie in **Mail-Setup – Outlook**auf **Profile anzeigen**.<br/>![Das "Mail-Setup - Outlook" im Dialogfeld mit der Schaltfläche 'Profile anzeigen' hervorgehoben](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. **E-Mail**klicken Sie auf **Hinzufügen**. Geben Sie dann im **Neuen Profil**, einen Namen für das Postfach Überwachung (beispielsweise **Aufsicht**).<br/>![Im Dialogfeld der 'Neues Profil' mit dem Namen "Überwachung" im Feld 'Profilname'](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. Klicken Sie in **Outlook zu Office 365 verbinden**auf **Verbindung mit einem anderen Konto herstellen**.<br/>![Die Nachricht Outlook nach Office 365 Verbinden mit den Link 'Verbindung in ein anderes Konto' hervorgehoben](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Klicken Sie im **Konto automatisch einrichten**wählen Sie **manuelle Installation oder zusätzliche Servertypen**, und klicken Sie dann auf **Weiter**.

7. Wählen Sie **Kontotyp wählen**Sie in **Office 365**. Geben Sie dann im Feld **E-Mail-Adresse** die Adresse des Postfachs Überwachung, die Sie zuvor kopiert.<br/>![Die Seite 'Your Kontotyp auswählen' des Dialogfelds 'Konto hinzufügen' in Outlook mit Feld 'E-Mail-Adresse' hervorgehoben.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Geben Sie bei Aufforderung Ihre Office 365-Anmeldeinformationen.

9. Wenn der Vorgang erfolgreich war, sehen Sie die **Aufsicht - \<Richtlinienname\> ** Ordner aufgeführt, in der Ansicht "Ordnerliste" in Outlook.

## <a name="powershell-reference"></a>PowerShell-Verweis

Bei Bedarf können Sie erstellen und Verwalten von aufsichtsrichtlinien mit den folgenden PowerShell-Cmdlets:

- [Neue SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [Set-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [Remove-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [Neue SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [Get-SupervisoryReviewOverallProgressReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [Get-SupervisoryReviewTopCasesReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)