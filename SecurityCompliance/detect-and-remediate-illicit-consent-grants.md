---
title: Erkennen und Korrigieren von unerlaubter Zustimmung in Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/23/2018
audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Hier erfahren Sie, wie Sie den Angriff auf unerlaubte Zustimmung in Office 365 erkennen und korrigieren.
ms.openlocfilehash: 5e89e6cb39c04b708ffe0a49a2cd41d6a775e4a4
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150277"
---
# <a name="detect-and-remediate-illicit-consent-grants-in-office-365"></a>Erkennen und Korrigieren von unerlaubter Zustimmung in Office 365

**Zusammenfassung**  Hier erfahren Sie, wie Sie den Angriff auf unerlaubte Zustimmung in Office 365 erkennen und korrigieren.

## <a name="what-is-the-illicit-consent-grant-attack-in-office-365"></a>Was ist der rechtswidrige Genehmigungs Zuschuss Angriff in Office 365?
Bei einem Angriff mit unerlaubter Zustimmung erstellt der Angreifer eine Azure-registrierte Anwendung, die den Zugriff auf Daten wie Kontaktinformationen, e-Mail oder Dokumente anfordert. Der Angreifer täuscht dann einen Endbenutzer vor, dass er der Anwendung zustimmt, dass er über einen Phishing-Angriff auf seine Daten zugreift oder unerlaubten Code in eine vertrauenswürdige Website einfügt. Nachdem der illegalen Anwendung eine Zustimmung erteilt wurde, verfügt sie über einen Zugriff auf Kontoebene auf Daten, ohne dass ein organisationskonto erforderlich ist. Normale korrekturschritte wie das Zurücksetzen von Kennwörtern für Benutzerkonten, die mehrstufige Authentifizierung (Multi-Factor Authentication, MFA) für Konten erfordern, sind für diese Art von Angriff nicht wirksam, da es sich um Drittanbieteranwendungen handelt, die sich außerhalb der Organisation befinden. Diese Angriffe nutzen ein Interaktionsmodell, das davon ausgeht, dass die Entität, die die Informationen anfordert, Automatisierung und kein Mensch ist.

## <a name="what-does-an-illicit-consent-grant-attack-look-like-in-office-365"></a>Wie sieht ein Angriff der illegalen Zustimmungs Erteilung in Office 365 aus?
Sie müssen das Office 365 **Überwachungsprotokoll** durchsuchen, um nach Zeichen zu suchen, die auch als Indikatoren für Kompromisse (IOC) dieses Angriffs bezeichnet werden. Für Organisationen mit vielen Azure-registrierten Anwendungen und einer großen Benutzerbasis besteht die bewährte Methode darin, die Genehmigungs Stipendien für Organisationen auf wöchentlicher Basis zu überprüfen.
### <a name="steps-for-finding-signs-of-this-attack"></a>Schritte zum Auffinden von Anzeichen für diesen Angriff
1. Öffnen Sie das **Security and Compliance Center** in Ihrem Office 365 Mandanten.
2. Navigieren Sie zum Knoten **Suche & unter** suchung, und wählen Sie **Überwachungsprotokoll** Suche aus.
3. Erstellen Sie eine Suche (alle Aktivitäten und alle Benutzer), und Filtern Sie die Ergebnisse zur Zustimmung zur Anwendung, und fügen Sie OAuth2PermissionGrant hinzu.
4. Untersuchen Sie die erweiterten Eigenschaften, und überprüfen Sie, ob IsAdminContent auf true festgelegt ist.

> [!NOTE]
>  
   - Es kann bis zu 30 Minuten oder bis zu 24 Stunden dauern, bis ein Ereignis eintritt, damit der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt wird.
   - Der Zeitraum, in dem ein Überwachungsdatensatz aufbewahrt und im Überwachungsprotokoll durchsucht werden kann, hängt von Ihrem Office 365-Abonnement und insbesondere vom Typ der Lizenz ab, die einem bestimmten Benutzer zugewiesen ist. Weitere Informationen finden Sie unter [Überwachungsprotokoll](search-the-audit-log-in-security-and-compliance.md).
      
Wenn dieser Wert auf true festgelegt ist, weist dies darauf hin, dass ein Benutzer mit globalem Administrator Zugriff möglicherweise umfassenden Zugriff auf Daten erhalten hat. Wenn dies unerwartet ist, nehmen Sie die erforderlichen Schritte zum [bestätigen eines](detect-and-remediate-illicit-consent-grants.md#confirmattack)Angriffs vor.

<a name="confirmattack"> </a>
## <a name="how-to-confirm-an-attack"></a>Vorgehensweise zum Bestätigen eines Angriffs
Wenn Sie über eine oder mehrere Instanzen der IOCs verfügen, müssen Sie weitere Untersuchungen durchführen, um positiv zu bestätigen, dass der Angriff aufgetreten ist. Sie können eine dieser drei Methoden zum Bestätigen des Angriffs verwenden.
- Inventory-Anwendungen und deren Berechtigungen mithilfe des Azure Active Directory-Portals. Diese Methode ist gründlich, aber Sie können nur einen Benutzer zu einem Zeitpunkt überprüfen, der sehr zeitaufwendig sein kann, wenn Sie viele Benutzer überprüfen müssen.
- Inventur Anwendungen und deren Berechtigungen mithilfe von PowerShell. Dies ist die schnellste und gründlichste Methode mit der geringsten Aufwandmenge.
- Lassen Sie Ihre Benutzer ihre apps und Berechtigungen einzeln überprüfen und die Ergebnisse den Administratoren zur Behebung zurückmelden.

## <a name="inventory-apps-with-access-in-your-organization"></a>Inventarisieren von apps mit Zugriff in Ihrer Organisation
Sie können dies für Ihre Benutzer entweder mit dem Azure Active Directory-Portal oder mit PowerShell tun, oder Ihre Benutzer müssen ihren Anwendungszugriff einzeln auflisten.

### <a name="steps-for-using-the-azure-active-directory-portal"></a>Schritte für die Verwendung des Azure Active Directory-Portals
Sie können die Anwendungen, für die ein einzelner Benutzerberechtigungen erteilt hat, über das [Azure Active Directory-Portal](https://portal.azure.com/)nachschlagen. 
1. Melden Sie sich beim Azure-Portal mit Administratorrechten an.
2. Wählen Sie das Azure Active Directory Blade aus.
3. Wählen Sie **Benutzer** aus.
4. Wählen Sie den Benutzer aus, den Sie überprüfen möchten.
5. Wählen Sie **Anwendungen**aus.

Dadurch werden die apps angezeigt, die dem Benutzer zugewiesen sind und welche Berechtigungen die applcations haben.

### <a name="steps-for-having-your-users-enumerate-their-application-access"></a>Schritte zum Auflisten des Anwendungszugriffs durch Ihre Benutzer
Lassen Sie Ihre Benutzer dorthin https://myapps.microsoft.com wechseln und ihren eigenen Anwendungszugriff überprüfen. Sie sollten in der Lage sein, alle apps mit Zugriff anzuzeigen, Details dazu anzuzeigen (einschließlich des Umfangs des Zugriffs) und in der Lage zu sein, Berechtigungen für verdächtige oder illegale apps zu widerrufen.

### <a name="steps-for-doing-this-with-powershell"></a>Schritte dafür mit PowerShell
Die einfachste Möglichkeit zum Überprüfen des Angriffs auf unerlaubte Zustimmung ist die Ausführung von [Get-AzureADPSPermissions. ps1](https://gist.github.com/psignoret/41793f8c6211d2df5051d77ca3728c09), wodurch alle OAuth-Zustimmungs-und OAuth-Apps für alle Benutzer in Ihrem Mandanten in einer CSV-Datei abgeworfen werden. 

#### <a name="pre-requisites"></a>Voraussetzungen
- Die Azure AD PowerShell-Bibliothek installiert.
- Globale Administratorrechte für den Mandanten, für die das Skript ausgeführt wird.
- Lokaler Administrator auf dem Computer, von dem die Skripts ausgeführt werden.

> [!IMPORTANT]
> Es wird dringend empfohlen, dass Sie mehrstufige Authentifizierung für Ihr Administratorkonto benötigen.  Dieses Skript unterstützt die MFA-Authentifizierung.

1. Melden Sie sich mit lokalen Administratorrechten bei dem Computer an, auf dem das Skript ausgeführt wird.
2. Laden Sie das [Get-AzureADPSPermissions. ps1-](https://gist.github.com/psignoret/41793f8c6211d2df5051d77ca3728c09) Skript aus GitHub in einen Ordner herunter, von dem aus Sie das scruipt ausführen werden.  Dabei handelt es sich um denselben Ordner, in den die Ausgabedatei "Permissions. csv" geschrieben wird.
3. Öffnen Sie eine PowerShell-Instanz als Administrator, und öffnen Sie den Ordner, in dem Sie das Skript gespeichert haben.
4. Stellen Sie mithilfe des [Connect-AzureAD-](https://docs.microsoft.com/powershell/module/azuread/connect-azuread?view=azureadps-2.0) Cmdlets eine Verbindung zu Ihrem Verzeichnis her.
5. Führen Sie diese PowerShell-Befehlszeile wie folgt aus:`Get-AzureADPSPermissions.ps1 | Export-csv -path "Permissions.csv" -NoTypeInformation`

Das Skript erstellt eine Datei namens "Permissions. csv". Führen Sie die folgenden Schritte aus, um nach illegalen Anwendungs Berechtigungs Zuschüssen zu suchen: 
1. Suchen Sie in der Spalte "zusenttype" (Spalte G) nach dem Wert "allprinciples". Die allprincipals-Berechtigung ermöglicht der Clientanwendung den Zugriff auf alle Inhalte im Mandanten. Systemeigene Office 365 Anwendungen benötigen diese Berechtigung, um ordnungsgemäß zu funktionieren. Jede nicht-Microsoft-Anwendung mit dieser Berechtigung sollte sorgfältig geprüft werden.
2.  Überprüfen Sie in der Spalte Permission (Spalte F) die Berechtigungen, die jede Delegierte Anwendung auf Inhalte hat. Suchen Sie nach der Berechtigung "lesen" und "schreiben" oder "*. "Alle"-Berechtigungen und überprüfen diese sorgfältig, da Sie möglicherweise nicht geeignet sind.
3.  Überprüfen Sie die spezifischen Benutzer, denen Zustimmung erteilt wurde. Wenn Benutzer mit hohem Profil oder hoher Auswirkung unangemessene Zustimmungen erteilt haben, sollten Sie weiter untersuchen.
4.  Suchen Sie in der Spalte ClientDisplayName (Spalte C) nach apps, die verdächtig erscheinen. Apps mit falsch geschriebenen Namen, Super langweiligen Namen oder Hacker-klingenden Namen sollten sorgfältig geprüft werden.

## <a name="determine-the-scope-of-the-attack"></a>Bestimmen des Umfangs des Angriffs
Nachdem Sie die Inventarisierung des Anwendungszugriffs abgeschlossen haben, überprüfen Sie das Office 365 **Überwachungsprotokoll** , um den vollständigen Umfang der Verletzung zu ermitteln.  Suchen Sie die betroffenen Benutzer, die Zeiträume, für die die unerlaubte Anwendung Zugriff auf Ihre Organisation hatte, sowie die Berechtigungen, die die APP besaß. Sie können das **Überwachungsprotokoll** im [Microsoft 365 Security and Compliance Center](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)durchsuchen. 

> [!IMPORTANT]
> Die [postfachüberwachung](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918) und [Aktivitätsüberwachung für Administratoren und Benutzer](https://support.office.com/article/turn-office-365-audit-log-search-on-or-off-e893b19a-660c-41f2-9074-d3631c95a014) müssen vor dem Angriff aktiviert worden sein, damit Sie diese Informationen erhalten.

## <a name="how-to-stop-and-remediate-an-illicit-consent-grant--attack"></a>Vorgehensweise beenden und Korrigieren eines Grant-Angriffs für unerlaubte Zustimmung
Nachdem Sie eine Anwendung mit unzulässigen Berechtigungen identifiziert haben, haben Sie mehrere Möglichkeiten, diesen Zugriff zu entfernen.
- Sie können die Berechtigung der Anwendung im Azure Active Directory-Portal durch folgende Anweisung widerrufen:
    - Navigieren Sie zum betroffenen Benutzer im **Azure Active Directory-Benutzer** Blatt.
    - Wählen Sie **Anwendungen**aus.
    - Wählen Sie die unzulässige Anwendung aus.
    - Klicken Sie im Drilldown auf **Entfernen** .
- Sie können die OAuth-Zustimmungs Erteilung mit PowerShell widerrufen, indem Sie die Schritte unter [Remove-AzureADOAuth2PermissionGrant](https://docs.microsoft.com/powershell/module/azuread/Remove-AzureADOAuth2PermissionGrant?view=azureadps-2.0)ausführen.
- Sie können die Rollenzuweisung für die Dienstanwendung mithilfe von PowerShell widerrufen, indem Sie die Schritte unter [Remove-AzureADServiceAppRoleAssignment](https://docs.microsoft.com/powershell/module/azuread/Remove-AzureADServiceAppRoleAssignment?view=azureadps-2.0)ausführen.
- Sie können die Anmeldung für das betroffene Konto auch ganz deaktivieren, wodurch wiederum der APP-Zugriff auf die Daten in diesem Konto deaktiviert wird. Dies ist natürlich nicht ideal für die Produktivität des Endbenutzers, aber wenn Sie die Auswirkungen schnell begrenzen möchten, kann es sich um eine praktikable kurzfristige Behebung handeln.
- Sie können integrierte Anwendungen für Ihr Mandanten deaktivieren. Dies ist ein drastischer Schritt, bei dem die Möglichkeit für Endbenutzer, die Zustimmung auf Mandantenebene zu erteilen, deaktiviert wird. Dadurch wird verhindert, dass Benutzer versehentlich Zugriff auf eine böswillige Anwendung gewähren. Dies wird nicht dringend empfohlen, da es die Fähigkeit Ihrer Benutzer, mit Anwendungen von Drittanbietern produktiv zu sein, stark beeinträchtigt.  Befolgen Sie dazu die Schritte unter [Aktivieren oder deaktivieren integrierter apps](https://support.office.com/article/Turning-Integrated-Apps-on-or-off-7e453a40-66df-44ab-92a1-96786cb7fb34).

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sichern von Office 365 wie ein Profi für Internetsicherheit
Ihr Office 365-Abonnement bietet eine Reihe von leistungsfähigen Funktionen für Sicherheit, die Sie zum Schutz Ihrer Daten und Ihrer Benutzer verwenden können.  Verwenden Sie die [Office 365-Sicherheits-Roadmap: Top-Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus](https://support.office.com/article/office-365-security-roadmap-top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) zum Implementieren von empfohlenen Microsoft-Best-Practices für den Schutz Ihres Office 365-Mandanten.
- Aufgaben, die in den ersten 30 Tagen ausgeführt werden sollten.  Diese sind unmittelbar gültig und haben nur geringe Auswirkungen für die Benutzer.
- Aufgaben, die innerhalb von 90 Tagen ausgeführt werden sollten. Diese erfordern etwas mehr Zeit für Planung und Implementierung, stärken die Sicherheit Ihres Unternehmens jedoch erheblich.
- Über 90 Tage hinaus. Diese Verbesserungen werden in den ersten 90 Tagen Ihrer Arbeit umgesetzt.

## <a name="see-also"></a>Siehe auch:
- [Unerwartete Anwendung in der Liste "meine Anwendungen](https://docs.microsoft.com/azure/active-directory/application-access-unexpected-application) " führt Administratoren durch verschiedene Aktionen, die Sie nach der Realisierung unerwarteter Anwendungen mit Zugriff auf Daten möglicherweise ausführen möchten.
- [Integrieren von Anwendungen in Azure Active Directory]  (https://docs.microsoft.com/azure/active-directory/active-directory-apps-permissions-consent) ist eine allgemeine Übersicht über die Zustimmung und die Berechtigungen.  Achten Sie besonders auf die [Übersicht über den Abschnitt Zustimmungs Framework](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#overview-of-the-consent-framework) .
- [Probleme beim entwickeln meiner Anwendung](https://docs.microsoft.com/azure/active-directory/active-directory-application-dev-development-content-map) bieten Links zu verschiedenen Zustimmungs bezogenen Artikeln.
- [Application-und Service Principal-Objekte in Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/develop/active-directory-application-objects) bietet eine Übersicht über die Anwendungs-und Dienstprinzipal Objekte, die Kern des Anwendungsmodells sind.
- [Verwalten des Zugriffs auf apps](https://docs.microsoft.com/azure/active-directory/active-directory-managing-access-to-apps) ist eine Übersicht über die Funktionen, die Administratoren zum Verwalten des Benutzerzugriffs auf apps haben.
