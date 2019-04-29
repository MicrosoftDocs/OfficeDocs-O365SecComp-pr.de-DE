---
title: Erkennen und Korrigieren von unerlaubter Zustimmung in Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/23/2018
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Erfahren Sie, wie Sie die unerlaubte Einwilligung in Office 365 erkennen und beheben können.
ms.openlocfilehash: 658183b3e5a3089425312ee14c6663485e0543ce
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402953"
---
# <a name="detect-and-remediate-illicit-consent-grants-in-office-365"></a>Erkennen und Korrigieren von unerlaubter Zustimmung in Office 365

**Zusammenfassung**  Erfahren Sie, wie Sie die unerlaubte Einwilligung in Office 365 erkennen und beheben können.

## <a name="what-is-the-illicit-consent-grant-attack-in-office-365"></a>Was ist der illegale Genehmigungs Angriff in Office 365?
Bei einem unerlaubten Genehmigungs Angriff erstellt der Angreifer eine Azure-registrierte Anwendung, die den Zugriff auf Daten wie Kontaktinformationen, e-Mails oder Dokumente anfordert. Der Angreifer betrügt dann einen Endbenutzer bei der Erteilung der Einwilligung für den Zugriff auf seine Daten entweder über einen Phishing-Angriff oder durch Einschleusen von illegalem Code in eine vertrauenswürdige Website. Nachdem der unzulässigen Anwendung eine Einwilligung erteilt wurde, hat Sie Zugriff auf die Daten auf Kontoebene, ohne dass ein organisationskonto erforderlich ist. Normale korrekturschritte, wie das Zurücksetzen von Kennwörtern für Benutzerkonten oder das Erzwingen einer mehrstufigen Authentifizierung (Multi-Factor Authentication, MFA) für Konten, sind für diese Art von Angriffen nicht wirksam, da es sich um Drittanbieteranwendungen handelt, die sich außerhalb der Organisation befinden. Diese Angriffe nutzen ein Interaktionsmodell, das davon ausgeht, dass die Entität, die die Informationen aufruft, automatisiert und kein Mensch ist.

## <a name="what-does-an-illicit-consent-grant-attack-look-like-in-office-365"></a>Wie sieht eine illegale Einwilligung in Office 365 aus?
Sie müssen das Office 365- **Überwachungsprotokoll** durchsuchen, um Zeichen zu finden, die auch als Indikatoren für den KOMPROMISS (IOC) dieses Angriffs bezeichnet werden. Für Organisationen mit vielen Azure-registrierten Anwendungen und einer großen Benutzerbasis empfiehlt es sich, die Zuwendungen für die Zustimmung Ihrer Organisation wöchentlich zu überarbeiten.
### <a name="steps-for-finding-signs-of-this-attack"></a>Schritte zum Auffinden von Anzeichen für diesen Angriff
1. Öffnen Sie das **Security and Compliance Center** in ihrem Office 365-Mandanten.
2. Navigieren Sie zum Knoten **Such & unter** suchung, und wählen Sie **Überwachungsprotokoll** Suche aus.
3. Erstellen Sie eine Suche (alle Aktivitäten und alle Benutzer), und Filtern Sie die Ergebnisse für die Zustimmung zur Anwendung, und fügen Sie OAuth2PermissionGrant hinzu.
4. Untersuchen Sie die erweiterten Eigenschaften, und überprüfen Sie, ob IsAdminContent auf true festgelegt ist.

> [!NOTE]
>  
   - Es kann bis zu 30 Minuten oder bis zu 24 Stunden dauern, bis ein Ereignis eintritt, damit der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt wird.
   - Die Dauer, die ein Überwachungsdatensatz aufbewahrt und im Überwachungsprotokoll durchsuchbar ist, hängt von Ihrem Office 365-Abonnement und insbesondere vom Typ der Lizenz ab, die einem bestimmten Benutzer zugewiesen ist. Weitere Informationen finden Sie unter [Überwachungsprotokoll](search-the-audit-log-in-security-and-compliance.md).
      
Wenn dieser Wert auf true festgelegt ist, bedeutet dies, dass eine Person mit globalem Administrator Zugriff möglicherweise umfassenden Zugriff auf Daten gewährt hat. Wenn dies nicht der Fall ist, müssen Sie Schritte zur [Bestätigung eines](detect-and-remediate-illicit-consent-grants.md#confirmattack)Angriffs ergreifen.

<a name="confirmattack"> </a>
## <a name="how-to-confirm-an-attack"></a>VorGehensWeise zum Bestätigen eines Angriffs
Wenn Sie über eine oder mehrere Instanzen des oben aufgeführten IOCs verfügen, müssen Sie weitere Untersuchungen durchführen, um positiv zu bestätigen, dass der Angriff aufgetreten ist. Sie können eine dieser drei Methoden zum Bestätigen des Angriffs verwenden.
- Inventarisieren von Anwendungen und deren Berechtigungen mithilfe des Azure Active Directory-Portals. Diese Methode ist gründlich, aber Sie können nur einen Benutzer gleichzeitig überprüfen, was sehr zeitaufwändig sein kann, wenn viele Benutzer überprüfen müssen.
- Inventarisieren von Anwendungen und deren Berechtigungen mithilfe von PowerShell. Dies ist die schnellste und gründlichste Methode mit dem geringsten Aufwand.
- Lassen Sie Ihre Benutzer ihre apps und Berechtigungen einzeln überprüfen und die Ergebnisse an die Administratoren zur Behebung zurückmelden.

## <a name="inventory-apps-with-access-in-your-organization"></a>Inventarisieren von apps mit Zugriff in Ihrer Organisation
Sie können dies für Ihre Benutzer entweder mit dem Azure Active Directory-Portal oder mit PowerShell tun, oder Ihre Benutzer müssen ihren Anwendungszugriff einzeln auflisten.

### <a name="steps-for-using-the-azure-active-directory-portal"></a>Schritte zur Verwendung des Azure Active Directory-Portals
Mithilfe des [Azure Active Directory](https://portal.azure.com/)-Portals können Sie die Anwendungen nachschlagen, denen ein einzelner Benutzerberechtigungen erteilt hat. 
1. Melden Sie sich mit Administratorrechten beim Azure-Portal an.
2. Wählen Sie das Azure Active Directory-Blade aus.
3. Wählen Sie **Benutzer** aus.
4. Wählen Sie den zu überprüfenden Benutzer aus.
5. Wählen Sie **Anwendungen**aus.

Dadurch werden die apps angezeigt, die dem Benutzer zugewiesen sind und welche Berechtigungen die applcations besitzen.

### <a name="steps-for-having-your-users-enumerate-their-application-access"></a>Schritte für die Aufzählung des Anwendungszugriffs durch Ihre Benutzer
Lassen Sie Ihre Benutzer zu https://myapps.microsoft.com Ihrem eigenen Anwendungszugriff dorthin wechseln. Sie sollten in der Lage sein, alle apps mit Zugriff anzuzeigen, Details zu diesen zu sehen (einschließlich des Zugriffs), und in der Lage sein, Rechte für verdächtige oder illegale apps zu widerrufen.

### <a name="steps-for-doing-this-with-powershell"></a>Schritte dafür mit PowerShell
Die einfachste Möglichkeit zum Überprüfen des Zugriffs auf eine illegale Einwilligung ist die Ausführung von [Get-AzureADPSPermissions. ps1](https://gist.github.com/psignoret/41793f8c6211d2df5051d77ca3728c09), die alle OAuth-Genehmigungs-und OAuth-Apps für alle Benutzer in ihrer Mandantschaft in einer CSV-Datei abgibt. 

#### <a name="pre-requisites"></a>Voraussetzungen
- Die Azure AD PowerShell-Bibliothek ist installiert.
- Globale Administratorrechte für den Mandanten, für die das Skript ausgeführt wird.
- Lokaler Administrator auf dem Computer, von dem die Skripts ausgeführt werden.

> [!IMPORTANT]
> Es wird dringend empfohlen, dass Sie mehrstufige Authentifizierung für Ihr Administratorkonto benötigen.  Dieses Skript unterstützt die MFA-Authentifizierung.

1. Melden Sie sich bei dem Computer an, von dem Sie das Skript mit lokalen Administratorrechten ausführen.
2. Laden Sie das [Get-AzureADPSPermissions. ps1-](https://gist.github.com/psignoret/41793f8c6211d2df5051d77ca3728c09) Skript aus GitHub herunter, und kopieren Sie es in einen Ordner, in dem Sie die scruipt ausführen werden.  Dabei handelt es sich um den gleichen Ordner, in den die Ausgabedatei "Permissions. csv" geschrieben wird.
3. Öffnen Sie eine PowerShell-Instanz als Administrator, und öffnen Sie den Ordner, in dem Sie das Skript gespeichert haben.
4. Stellen Sie mithilfe des [Connect-AzureAD-](https://docs.microsoft.com/powershell/module/azuread/connect-azuread?view=azureadps-2.0) Cmdlets eine Verbindung zu Ihrem Verzeichnis her.
5. Führen Sie diese PowerShell-Befehlszeile wie folgt aus:`Get-AzureADPSPermissions.ps1 | Export-csv -path "Permissions.csv" -NoTypeInformation`

Das Skript erzeugt eine Datei mit dem Namen Permissions. CSV. Führen Sie die folgenden Schritte aus, um nach unzulässigen Anwendungsberechtigungen zu suchen: 
1. Suchen Sie in der Spalte "subsenttype" (Spalte G) nach dem Wert "allPrinciples". Die allPrincipals-Berechtigung ermöglicht es der Clientanwendung, auf die Inhalte aller Benutzer in der Mandantschaft zuzugreifen. Native Office 365-Anwendungen benötigen diese Berechtigung, um ordnungsgemäß zu funktionieren. Jede nicht-Microsoft-Anwendung mit dieser Berechtigung sollte sorgfältig überprüft werden.
2.  Überarbeiten Sie in der Spalte Berechtigung (Spalte F) die Berechtigungen, die jede Delegierte Anwendung auf Inhalte hat. Suchen Sie nach Lese-und Schreibberechtigung oder "*. Alle "Berechtigung, und überprüfen Sie diese sorgfältig, da Sie möglicherweise nicht geeignet sind.
3.  Überarbeiten Sie die Benutzer, denen die Zustimmung erteilt wurde. Wenn die Benutzer mit hohem Profil oder mit hoher Auswirkung unangemessene Zustimmungen haben, sollten Sie weiter untersuchen.
4.  Suchen Sie in der Spalte ClientDisplayName nach apps, die verdächtig erscheinen. Apps mit falsch geschriebenen Namen, Super Bland-Namen oder Hacker-klingenden Namen sollten sorgfältig überprüft werden.

## <a name="determine-the-scope-of-the-attack"></a>Bestimmen des Umfangs des Angriffs
Nachdem Sie den Anwendungszugriff inventarisiert haben, überprüfen Sie das Office 365- **Überwachungsprotokoll** , um den vollständigen Umfang der Verletzung zu ermitteln.  Suchen Sie nach den betroffenen Benutzern, den Zeitrahmen, die die illegale Anwendung Zugriff auf Ihre Organisation hatte, und die Berechtigungen, die die APP hatte. Sie können das **Überwachungsprotokoll** im [Microsoft 365 Security and Compliance Center](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)durchsuchen. 

> [!IMPORTANT]
> Die [postfachüberwachung](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918) und [Aktivitätsüberwachung für Administratoren und Benutzer](https://support.office.com/article/turn-office-365-audit-log-search-on-or-off-e893b19a-660c-41f2-9074-d3631c95a014) müssen vor dem Angriff aktiviert worden sein, damit Sie diese Informationen erhalten.

## <a name="how-to-stop-and-remediate-an-illicit-consent-grant--attack"></a>Beenden und Beheben einer illegalen Einwilligung
Nachdem Sie eine Anwendung mit illegalen Berechtigungen identifiziert haben, haben Sie mehrere Möglichkeiten, diesen Zugriff zu entfernen.
- Sie können die Berechtigung der Anwendung im Azure Active Directory-Portal durch Folgendes widerrufen:
    - Navigieren Sie im **Azure Active Directory-Benutzer** Blatt zu dem betreffenden Benutzer.
    - Wählen Sie **Anwendungen**aus.
    - Wählen Sie die illegale Anwendung aus.
    - Klicken Sie im Drilldown auf **Entfernen** .
- Sie können den OAuth-Genehmigungs Zuschuss mit PowerShell widerrufen, indem Sie die Schritte in [Remove-AzureADOAuth2PermissionGrant](https://docs.microsoft.com/powershell/module/azuread/Remove-AzureADOAuth2PermissionGrant?view=azureadps-2.0)ausführen.
- Sie können die Rollenzuweisung für die Dienstanwendung mit PowerShell widerrufen, indem Sie die Schritte in [Remove-AzureADServiceAppRoleAssignment](https://docs.microsoft.com/powershell/module/azuread/Remove-AzureADServiceAppRoleAssignment?view=azureadps-2.0)ausführen.
- Sie können die Anmeldung für das betroffene Konto auch deaktivieren, wodurch der APP-Zugriff auf Daten in diesem Konto deaktiviert wird. Dies ist natürlich nicht ideal für die Produktivität des Endbenutzers, aber wenn Sie arbeiten, um die Auswirkungen schnell zu begrenzen, kann es sich um eine praktikable kurzfristige Korrektur handeln.
- Sie können integrierte Anwendungen für Ihren Mandanten deaktivieren. Dies ist ein drastischer Schritt, der die Möglichkeit für Endbenutzer deaktiviert, die Zustimmung mandantenweit zu gewähren. Dadurch wird verhindert, dass Benutzer versehentlich Zugriff auf eine bösartige Anwendung gewähren. Dies wird nicht unbedingt empfohlen, da dadurch die Produktivität der Benutzer in Drittanbieteranwendungen erheblich beeinträchtigt wird.  Führen Sie dazu die Schritte unter [Aktivieren oder Deaktivieren von integrierten Apps](https://support.office.com/article/Turning-Integrated-Apps-on-or-off-7e453a40-66df-44ab-92a1-96786cb7fb34)aus.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sichern von Office 365 wie ein Profi für Internetsicherheit
Ihr Office 365-Abonnement bietet eine Reihe von leistungsfähigen Funktionen für Sicherheit, die Sie zum Schutz Ihrer Daten und Ihrer Benutzer verwenden können.  Verwenden Sie die [Office 365-Sicherheits-Roadmap: Top-Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus](https://support.office.com/article/office-365-security-roadmap-top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) zum Implementieren von empfohlenen Microsoft-Best-Practices für den Schutz Ihres Office 365-Mandanten.
- Aufgaben, die in den ersten 30 Tagen ausgeführt werden sollten.  Diese sind unmittelbar gültig und haben nur geringe Auswirkungen für die Benutzer.
- Aufgaben, die innerhalb von 90 Tagen ausgeführt werden sollten. Diese erfordern etwas mehr Zeit für Planung und Implementierung, stärken die Sicherheit Ihres Unternehmens jedoch erheblich.
- Über 90 Tage hinaus. Diese Verbesserungen werden in den ersten 90 Tagen Ihrer Arbeit umgesetzt.

## <a name="see-also"></a>Siehe auch:
- [Unerwartete Anwendung in der Liste meine Anwendungen](https://docs.microsoft.com/azure/active-directory/application-access-unexpected-application) führt Administratoren durch verschiedene Aktionen, die Sie möglicherweise ausführen möchten, wenn Sie feststellen, dass es unerwartete Anwendungen mit Zugriff auf Daten gibt.
- [Integrieren von Anwendungen in Azure Active Directory]  (https://docs.microsoft.com/azure/active-directory/active-directory-apps-permissions-consent) eine allgemeine Übersicht über Einwilligung und Berechtigungen.  Achten Sie besonders auf die [Übersicht über den Abschnitt Zustimmungs Framework](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#overview-of-the-consent-framework) .
- [Probleme beim entwickeln meiner Anwendung](https://docs.microsoft.com/azure/active-directory/active-directory-application-dev-development-content-map) finden Sie Links zu verschiedenen Artikeln zur Einwilligung.
- [Application-und Service Principal-Objekte in Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/develop/active-directory-application-objects) bietet eine Übersicht über die Anwendungs-und Dienstprinzipal Objekte, die Kern für das Anwendungsmodell sind.
- [Verwalten des Zugriffs auf apps](https://docs.microsoft.com/azure/active-directory/active-directory-managing-access-to-apps) ist eine Übersicht über die Funktionen, die Administratoren zum Verwalten des Benutzerzugriffs auf apps haben.
