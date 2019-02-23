---
title: Konfigurieren von Aufsichtsrichtlinien für Ihre Organisation
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Einrichten einer Aufsichts Übersichts Richtlinie zur Erfassung der Mitarbeiterkommunikation zur Überprüfungen.
ms.openlocfilehash: af317194fcf551acde8c53cdf6aa38bfb040dc84
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216735"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Konfigurieren von Aufsichtsrichtlinien für Ihre Organisation

Verwenden Sie Aufsichtsrichtlinien, um die Mitarbeiterkommunikation zur Prüfung durch interne oder externe Prüfer zu erfassen. Weitere Informationen dazu, wie Sie mit Aufsichtsrichtlinien die Kommunikation in Ihrer Organisation überwachen können, finden Sie unter [Aufsichtsrichtlinien in Office 365](supervision-policies.md).

> [!NOTE]
> Benutzer, die von Aufsichtsrichtlinien überwacht werden, müssen entweder über eine Office 365 Enterprise E3-Lizenz mit dem Advanced Compliance-Add-on verfügen oder in einem Office 365 Enterprise E5-Abonnement enthalten sein. Wenn Sie keinen Enterprise E5-Plan haben und die Überwachung testen möchten, können Sie [sich für eine Testversion von Office 365 Enterprise E5 registrieren](https://go.microsoft.com/fwlink/p/?LinkID=698279).
  
Führen Sie die folgenden Schritte aus, um die Überwachung in Ihrer Office 365-Organisation einzurichten und zu verwenden:
  
- **Schritt 1 (optional)** - [Einrichten von Gruppen für die Überwachung](configure-supervision-policies.md#exampledist)

    Bevor Sie mit der Überwachung beginnen, bestimmen Sie, wer Ihre Kommunikation überprüft hat und wer diese Bewertungen durchführen wird. Wenn Sie mit wenigen Benutzern beginnen möchten, um zu sehen, wie die Überwachung funktioniert, können Sie die Einrichtung von Gruppen für jetzt überspringen.

- **Schritt 2 (erforderlich)** - [Beaufsichtigung in Ihrer Organisation verfügbar machen](configure-supervision-policies.md#MakeAvailable)

    Fügen Sie sich selbst zur Rollengruppe Supervisory Review hinzu, damit Sie Richtlinien einrichten können. Jeder, der diese Rolle zugewiesen hat, kann auf die Seite " **Aufsicht** " unter " **Datensteuerung** " im Security & Compliance Center zugreifen. Wenn die zu überprüfende e-Mail in Exchange Online gehostet wird, muss jeder Prüfer auch über [Remote-PowerShell-Zugriff auf Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)verfügen.

- **Schritt 3 (optional)** - [Konfigurieren von benutzerdefinierten vertraulichen Informationstypen oder benutzerdefinierten Keyword-Wörterbüchern/Lexika](configure-supervision-policies.md#sensitiveinfo)

    Wenn Sie einen benutzerdefinierten vertraulichen Infotyp oder ein benutzerdefiniertes Stichwort Wörterbuch für Ihre Aufsichtsrichtlinie verwenden müssen, müssen Sie es erstellen, bevor Sie den Überwachungs-Assistenten starten.

- **Schritt 4 (erforderlich)** - [Einrichten einer Aufsichtsrichtlinie](configure-supervision-policies.md#setupsuper)

    Sie erstellen Aufsichtsrichtlinien im Security & Compliance Center. Diese Richtlinien legen fest, welche Kommunikation in Ihrer Organisation überprüft werden soll, und gibt an, wer Bewertungen durchführen soll. Zu den Kommunikationen Gehören e-Mails und Microsoft Teams-Kommunikation sowie Platt Form Kommunikation von Drittanbietern (wie Facebook, Twitter usw.).

- **Schritt 5-(optional)** [Testen der neuen Aufsichtsrichtlinie](configure-supervision-policies.md#TestPolicy)

    Das Testen Ihrer Aufsichtsrichtlinie, um sicherzustellen, dass Sie wie gewünscht funktioniert, ist ein wichtiger Teil, um sicherzustellen, dass Ihre Compliance-Strategie Ihren Standards entspricht.

- **Schritt 6 – (optional)** [Einrichten von Outlook-Add-Ins für Prüfer, die das Office 365-überwachungsdashboard oder Outlook im Web (früher als Outlook Web App bezeichnet) nicht verwenden möchten, um die überwachte Kommunikation zu überarbeiten](configure-supervision-policies.md#UseOutlook)

    Das Überwachungs-Add-in für Outlook erteilt den Prüfern Zugriff auf die Überwachungsfunktionen direkt im Outlook-Client, damit Sie jedes Element bewerten und kategorisieren können.

<a name="exampledist"> </a>

## <a name="step-1---set-up-groups-for-supervision-optional"></a>Schritt 1: Einrichten von Gruppen für die Überwachung (optional)

 Wenn Sie eine Aufsichtsrichtlinie erstellen, legen Sie fest, wer Ihre Kommunikation überprüft hat und wer diese Bewertungen durchführen wird. In der Richtlinie verwenden Sie e-Mail-Adressen, um Personen oder Personengruppen zu identifizieren. Um das Setup zu vereinfachen, erstellen Sie Gruppen für Personen, die Ihre Kommunikation überprüft haben, und Gruppen für Personen, die diese Kommunikationen überprüfen. Wenn Sie Gruppen verwenden, benötigen Sie möglicherweise mehrere-beispielsweise, wenn Sie die Kommunikation zwischen zwei verschiedenen Personengruppen überwachen möchten, oder wenn Sie eine Gruppe angeben möchten, die nicht überwacht werden soll. Details zur Funktionsweise finden Sie unter [example Distribution Groups](configure-supervision-policies.md#GroupExample) .
  
Um die Kommunikation zwischen oder innerhalb von Gruppen in Ihrer Organisation zu überwachen, richten Sie Verteilergruppen in der Exchange-Verwaltungskonsole ein (wechseln Sie zu **Empfänger** \> **Gruppen**). Weitere Informationen zum Einrichten von Verteilergruppen finden Sie unter [Manage Distribution Groups](http://go.microsoft.com/fwlink/?LinkId=613635) .
  
> [!NOTE]
> Sie können auch dynamische Verteilergruppen oder Sicherheitsgruppen für die Überwachung verwenden, wenn Sie es vorziehen. Informationen dazu, wie Sie entscheiden können, ob diese für Ihre Organisation besser geeignet sind, finden Sie unter [Verwalten von e-Mail-aktivierten Sicherheitsgruppen](http://go.microsoft.com/fwlink/?LinkId=627033)und [Verwalten dynamischer Verteilergruppen](http://go.microsoft.com/fwlink/?LinkId=627058).
  
<a name="GroupExample"> </a>

### <a name="example-distribution-groups"></a>Beispielverteilergruppen

Dieses Beispiel enthält eine Verteilergruppe, die für eine Finanzorganisation namens Contoso Financial International eingerichtet wurde.
  
Im Unternehmen Contoso Financial International muss eine Stichprobe der Kommunikationen zwischen Brokern in den Vereinigten Staaten beaufsichtigt werden. Für die Compliance Officer in dieser Gruppe ist jedoch keine Aufsicht erforderlich. Für dieses Beispiel können wir die folgenden Gruppen erstellen:
  
|**Einrichten dieser Verteilergruppe**|**Gruppenadresse (Alias)**|**Beschreibung**|
|:-----|:-----|:-----|
|Alle US-Broker | US_Brokers@Contoso.com | Diese Gruppe umfasst E-Mail-Adressen für alle US-basierten Broker, die für Contoso arbeiten. |
| Alle Compliance Officer für die Vereinigten Staaten | US_Compliance@Contoso.com  | Diese Gruppe enthält e-Mail-Adressen für alle US-basierten Compliance Officer, die für Contoso arbeiten. Da diese Gruppe eine Teilmenge aller in der USA ansässigen Broker ist, können Sie diesen Alias verwenden, um die Compliance-Verantwortlichen von einer Aufsichtsrichtlinie zu befreien. |
  
<a name="MakeAvailable"> </a>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a>Schritt 2: Bereitstellen der Überwachung in Ihrer Organisation (erforderlich)

Um die **Überwachung** als Menüoption im Security _AMP_ Compliance Center zur Verfügung zu stellen, muss Ihnen die Rolle "Supervisory Review Administrator" zugewiesen sein.
  
Zu diesem Zweck können Sie sich selbst als Mitglied der Rollengruppe "Supervisory Review" hinzufügen oder eine neue Rollengruppe erstellen.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Hinzufügen von Mitgliedern zur Rollengruppe "Supervisory Review"

1. Melden Sie [https://protection.office.com](https://protection.office.com) sich mit Anmeldeinformationen für ein Administratorkonto in ihrer Office 365-Organisation an.

2. Wechseln Sie im Security & Compliance Center zu **Berechtigungen**.

3. Wählen Sie die Rollengruppe **Aufsichtsüberprüfung** aus, und klicken Sie dann auf das Symbol bearbeiten.

4. Fügen Sie im Abschnitt **Mitglieder** die Personen hinzu, die die Überwachung für Ihre Organisation verwalten sollen.

### <a name="create-a-new-role-group"></a>Erstellen einer neuen Rollengruppe

1. Melden Sie [https://protection.office.com](https://protection.office.com) sich mit Anmeldeinformationen für ein Administratorkonto in ihrer Office 365-Organisation an.

2. Wechseln Sie im Security & Compliance Center zu **Berechtigungen** , und klicken Sie dann auf**+** hinzufügen ().

3. Klicken Sie im Abschnitt **Rollen** auf Hinzufügen**+**(), und Scrollen Sie nach unten zum **Supervisory Review-Administrator**. Diese Rolle der Rollengruppe hinzufügen.

4. Fügen Sie im Abschnitt **Mitglieder** die Personen hinzu, die die Überwachung für Ihre Organisation verwalten sollen.

Weitere Informationen zu Rollengruppen und Berechtigungen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a>Aktivieren des Remote-PowerShell-Zugriffs für Prüfer (wenn e-Mails in Exchange Online gehostet werden)

1. BeFolgen Sie die Anweisungen unter [Aktivieren oder Deaktivieren des Zugriffs auf Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).

<a name="sensitiveinfo"> </a>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a>Schritt 3-Erstellen benutzerdefinierter vertraulicher Informationstypen oder benutzerdefinierter Stichwort Wörterbücher (optional)

Um aus vorhandenen benutzerdefinierten vertraulichen Informationstypen oder benutzerdefinierten Keyword-Wörterbüchern im Assistenten für Aufsichtsrichtlinien auszuwählen, müssen Sie diese Elemente bei Bedarf zunächst erstellen.

### <a name="create-custom-sensitive-information-types"></a>Erstellen von benutzerdefinierten Typen für vertrauliche Informationen

1. Erstellen Sie einen neuen vertraulichen Informationstyp im Office 365 Security & Compliance Center. Navigieren Sie zu **vertraulichen Info-Typen** für **Klassifikationen** \> , und führen Sie die Schritte im Assistenten für **neue vertrauliche Informationen**aus. Hier finden Sie die folgenden Schritte:

    - Definieren Sie einen Namen und eine Beschreibung für den vertraulichen Infotyp.
    - Definieren der Näherungs-, Konfidenz Grad-und primären Musterelemente
    - Überarbeiten Ihrer Auswahl und Erstellen des Typs für vertrauliche Informationen

    Ausführlichere Informationen finden Sie unter [Erstellen eines benutzerdefinierten Typs für vertrauliche Informationen](create-a-custom-sensitive-information-type.md).

### <a name="create-custom-keyword-dictionarylexicon"></a>Erstellen benutzerdefinierter Stichwort Wörterbuch/Lexikon

1. Erstellen Sie mithilfe eines Text-Editors (wie Notepad) eine neue Datei mit den Stichwortbegriffen, die Sie in einer Aufsichtsrichtlinie überwachen möchten. Stellen Sie sicher, dass sich jeder Ausdruck in einer separaten Leitung befindet, und speichern Sie die Datei im **Unicode/UTF-16 (Little Endian)-** Format.
2. Importieren Sie die Schlüsselwortdatei mithilfe von PowerShell in Ihren Office 365-Mandanten. Informationen zum Herstellen einer Verbindung mit Office 365 mit PowerShell finden Sie unter [Connect to office 365 Security _AMP_ Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

    Nachdem Sie mit PowerShell eine Verbindung mit Office 365 hergestellt haben, führen Sie die folgenden Befehle aus, um Ihr Stichwort Wörterbuch zu importieren:

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    Ausführlichere Informationen finden Sie unter [Create a Keyword Dictionary](create-a-keyword-dictionary.md).

3. Erstellen Sie einen neuen vertraulichen Informationstyp im Office 365 Security & Compliance Center. Navigieren Sie zu **vertraulichen Info-Typen** für **Klassifikationen** \> , und führen Sie die Schritte im Assistenten für **neue vertrauliche Informationen**aus. Hier finden Sie die folgenden Schritte:

    - Definieren Sie einen Namen und eine Beschreibung für den vertraulichen Infotyp.
    - Hinzufügen des Benutzerwörterbuchs als Anforderung für das übereinstimmende Element
    - Überarbeiten Ihrer Auswahl und Erstellen des Typs für vertrauliche Informationen

    Nachdem das Benutzerwörterbuch/Lexikon erstellt wurde, können Sie die konfigurierten Schlüsselwörter mithilfe des Cmdlets [Get-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) oder durch Hinzufügen und Entfernen von Ausdrücken mithilfe des Cmdlets [Set-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) anzeigen.

    Ausführlichere Informationen finden Sie unter [Erstellen eines benutzerdefinierten Typs für vertrauliche Informationen](create-a-custom-sensitive-information-type.md).

<a name="setupsuper"> </a>

## <a name="step-4---set-up-a-supervision-policy-required"></a>Schritt 4: Einrichten einer Aufsichtsrichtlinie (erforderlich)
  
1. Melden Sie [https://protection.office.com](https://protection.office.com) sich mit Anmeldeinformationen für ein Administratorkonto in ihrer Office 365-Organisation an.

2. Wählen Sie im Security & Compliance Center die Option **Überwachung**aus.
  
3. Wählen Sie **Erstellen** aus, und folgen Sie dann dem Assistenten, um die folgenden Seiten der Richtlinie einzurichten. Mithilfe des Assistenten können Sie Folgendes tun:

    - Geben Sie der Richtlinie einen Namen und eine Beschreibung.
    - Wählen Sie die zu überwachenden Benutzer oder Gruppen aus, einschließlich der Auswahl von Benutzern oder Gruppen, die Sie ausschließen möchten.
    - Definieren Sie die Aufsichtsrichtlinien Bedingungen.
    - Wählen Sie aus, ob Sie vertrauliche Informationstypen einbeziehen möchten. Hier können Sie Standard-und benutzerdefinierte vertrauliche Infotypen auswählen.
    - Definieren Sie den Prozentsatz der zu überprüfenden Kommunikation.
    - Wählen Sie die Bearbeiter für die Richtlinie aus. Prüfer können einzelne Benutzer oder [e-Mail-aktivierte Sicherheitsgruppen](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group)sein.
    - Überdenken Sie Ihre Richtlinienauswahl und erstellen Sie die Richtlinie.

<a name="TestPolicy"> </a>

## <a name="step-5---test-your-supervision-policy-optional"></a>Schritt 5 – Testen der Aufsichtsrichtlinie (optional)

Nachdem Sie eine Aufsichtsrichtlinie erstellt haben, empfiehlt es sich zu testen, um sicherzustellen, dass die von Ihnen definierten Bedingungen ordnungsgemäß durch die Richtlinie erzwungen werden. Sie können auch [Ihre Data Loss Prevention (DLP)-Richtlinien testen](create-test-tune-dlp-policy.md) , wenn Ihre Aufsichtsrichtlinien vertrauliche Informationstypen aufweisen. Führen Sie die folgenden Schritte aus, um Ihre Aufsichtsrichtlinie zu testen:

1. Öffnen Sie einen e-Mail-Client oder Microsoft Teams, die als überwachten Benutzer angemeldet sind, der in der Richtlinie definiert ist, die Sie testen möchten.
2. Senden Sie eine e-Mail oder einen Microsoft Teams-Chat, der den Kriterien entspricht, die Sie in der Aufsichtsrichtlinie definiert haben. Dabei kann es sich um ein Stichwort, eine Anlagegröße, eine Domäne usw. handeln. Stellen Sie sicher, dass Sie feststellen, ob die konfigurierten bedingten Einstellungen in der Richtlinie zu restriktiv oder zu nachsichtig sind.

    > [!Note]
    > E-Mails, die bestimmten Richtlinien unterliegen, werden nahezu in Echtzeit verarbeitet und können sofort nach der Konfiguration der Richtlinie getestet werden. Chats in Microsoft Teams können bis zu 24 Stunden dauern, bis Sie in einer Richtlinie vollständig verarbeitet werden. 

3. Melden Sie sich bei Ihrem Office 365-Mandanten als Prüfer an, der in der Aufsichtsrichtlinie festgelegt ist. Navigieren Sie zu **Aufsicht** > *Ihre benutzerdefinierte Richtlinie* > **** , um den Bericht für die Richtlinie anzuzeigen.

<a name="UseOutlook"> </a>

## <a name="step-6---set-up-outlook-add-in-for-reviewers-optional"></a>Schritt 6: Einrichten des Outlook-Add-Ins für Prüfer (optional)

Prüfer, die Outlook verwenden möchten, anstatt das Aufsichts Dashboard in Office 365 oder Outlook im Web zum Überwachen der Kommunikation zu überwachen, müssen das Aufsichts-Add-in für Ihren Outlook-Client installieren.

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a>Schritt 1: Kopieren der Adresse für das überwachungspostfach

Um das Add-in für Outlook-Desktop zu installieren, benötigen Sie die Adresse für das überwachungspostfach, das im Rahmen der Einrichtung der Aufsichtsrichtlinie erstellt wurde.
  
> [!NOTE]
> Wenn eine andere Person die Richtlinie erstellt hat, müssen Sie diese Adresse abrufen, um das Add-in zu installieren.

 **So finden Sie die Überwachungs Postfachadresse**
  
1. Melden Sie sich [beim &amp; Security Compliance Center](https://protection.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Office 365-Organisation an.

2. Gehen Sie zur **Überwachung**.

3. Klicken Sie auf die Aufsichtsrichtlinie, die die zu überprüfende Kommunikation erfasst.

4. Kopieren Sie im Flyout Richtliniendetails unter **überwachungspostfach**die Adresse.<br/>![Der Abschnitt "Überwachungspostfach" im Detail Flyout der Aufsichtsrichtlinie mit der hervorgehobenen Überwachungs-Postfachadresse](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a>Schritt 2: Konfigurieren des Überwachungs Postfachs für Outlook-Desktop Zugriff

Als nächstes müssen die Bearbeiter einige Exchange Online PowerShell-Befehle ausführen, damit Sie Outlook mit dem überwachungspostfach verbinden können.
  
1. Stellen Sie eine Verbindung mit Exchange Online PowerShell her. [Wie mache ich das?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. Führen Sie die folgenden Befehle aus, wobei *SupervisoryReview {GUID} @domain. onmicrosoft.com* die Adresse ist, die Sie in Schritt 1 oben kopiert haben, und *Benutzer* ist der Name des Rezensenten, der eine Verbindung mit dem überwachungspostfach in Schritt 3 herstellt.

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. Warten Sie mindestens eine Stunde, bevor Sie mit Schritt 3 fortfahren.

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a>Schritt 3: Erstellen eines Outlook-Profils zum Herstellen einer Verbindung mit dem überwachungspostfach

Für den letzten Schritt müssen die Bearbeiter ein Outlook-Profil erstellen, um eine Verbindung mit dem überwachungspostfach herzustellen.

> [!NOTE]
> Zum Erstellen eines neuen Outlook-Profils verwenden Sie die e-Mail-Einstellungen in der Windows-Systemsteuerung. Der Pfad, den Sie zum Abrufen dieser Einstellungen ergreifen, hängt möglicherweise davon ab, welches Windows-Betriebssystem (Windows 7, Windows 8 oder Windows 10) Sie verwenden und welche Version von Outlook installiert ist.
  
1. Öffnen Sie die Systemsteuerung, und geben Sie im **Suchfeld** oben im Fenster **e-Mail**ein.<br/>(Sind Sie nicht sicher, wie Sie zur Systemsteuerung gelangen? Weitere Informationen finden Sie unter [wo ist die Systemsteuerung?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))
  
2. Öffnen Sie die **Mail-** app.

3. Klicken Sie in **Mail Setup-Outlook**auf **Profile anzeigen**.<br/>![Das Dialogfeld ' e-Mail-Setup-Outlook ' mit hervorgehobener Schaltfläche ' Profile anzeigen '](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. Klicken Sie in **e-Mail**auf **Hinzufügen**. Geben Sie dann unter **Neues Profil**einen Namen für das überwachungspostfach ein (beispielsweise **Aufsicht**).<br/>![Das Dialogfeld ' neues Profil ', in dem der Name ' Aufsicht ' in der Box ' Profilname ' angezeigt wird](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. Klicken Sie in **Outlook mit Office 365 verbinden**auf mit **einem anderen Konto verbinden**.<br/>![Die Meldung "Verbindung zwischen Outlook und Office 365" mit hervorgehobenem Link "mit einem anderen Konto verbinden"](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. Wählen Sie unter **Automatische Kontoeinrichtung** **manuell einrichten oder zusätzliche Servertypen**aus, und klicken Sie dann auf **weiter**.

7. Wählen Sie unter **Wählen Sie Ihren Kontotyp aus die**option **Office 365**. Geben Sie dann im Feld **e-Mail-Adresse** die Adresse des Überwachungs Postfachs ein, das Sie zuvor kopiert haben.<br/>![Die Seite "wählen Sie Ihren Kontotyp" des Dialogfelds ' Konto hinzufügen ' in Outlook, in dem das Feld ' e-Mail-Adresse ' hervorgehoben angezeigt wird.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. Geben Sie Ihre Office 365-Anmeldeinformationen ein, wenn Sie dazu aufgefordert werden.

9. Wenn die Einstellung erfolgreich ist, wird der Ordner " ** \<Aufsicht\> -Richtlinienname** " in der Ansicht "Ordnerliste" in Outlook angezeigt.

## <a name="powershell-reference"></a>PowerShell-Referenz

Bei Bedarf können Sie Aufsichtsrichtlinien mithilfe der folgenden PowerShell-Cmdlets erstellen und verwalten:

- [New-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [Set-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [Remove-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [Get-SupervisoryReviewOverallProgressReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [Get-SupervisoryReviewTopCasesReport](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)