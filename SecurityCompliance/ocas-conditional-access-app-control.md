---
title: Schützen von apps mit Office 365 Cloud App Security Conditional Access-App-Steuerelement
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Stop Verstöße und Lecks in Echtzeit mit Office 365 Cloud App Security Conditional Access app Control.
ms.openlocfilehash: 8656bf9d3e028bf6b44731c397b74d9c883db707
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103360"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a>Schützen von apps mit Office 365 Cloud App Security Conditional Access-App-Steuerelement

|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](ocas-deploy-conditional-access-app-control.md) <br/> |[Verwendung beginnen](utilization-activities-for-ocas.md) <br/> |

Am heutigen Arbeitsplatz ist es oft nicht genug, nach der Tatsache zu wissen, was in ihrer Cloud-Umgebung passiert. Sie möchten Verstöße und Lecks in Echtzeit beenden, bevor Mitarbeiter absichtlich oder versehentlich Ihre Daten und Ihre Organisation gefährden. Es ist wichtig, Benutzern in Ihrer Organisation zu ermöglichen, die Dienste und Tools, die Ihnen in Cloud-Apps zur Verfügung stehen, optimal zu nutzen und ihre eigenen Geräte zum laufen zu bringen. Gleichzeitig benötigen Sie Tools, mit denen Sie Ihre Organisation vor Datenlecks und Datendiebstahl in Echtzeit schützen können. Zusammen mit Azure Active Directory bietet Office 365 Cloud App Security diese Funktionen in einer ganzheitlichen und integrierten Erfahrung mit Conditional Access app Control.

> [!IMPORTANT]
> zur verwendung der cloud app security Conditional Access-app-steuerung benötigen sie eine [Azure active Directory P1-lizenz](https://azure.microsoft.com/pricing/details/active-directory/) und ein active [Office 365 cloud app security](office-365-cas-overview.md) -abonnement.

## <a name="how-it-works"></a>Funktionsweise

Die APP-Steuerelement für die Conditional Access-Anwendung verwendet eine Reverse-Proxy-Architektur und ist in Azure AD Conditional Access integriert. Mit dem bedingten Zugriff von Azure AD können Sie Zugriffssteuerungen für die Apps ihrer Organisation basierend auf bestimmten Bedingungen erzwingen. Die Bedingungen definieren *, wer* (Benutzer oder Gruppe von Benutzern) und *was* (welche Cloud-Apps) und *wo* (an welchen Standorten und Netzwerken) eine Richtlinie für den bedingten Zugriff angewendet wird. Nachdem Sie die Bedingungen festgelegt haben, können Sie Benutzer an Office 365 Cloud App Security weiterleiten, in dem Sie Daten mit der APP-Steuerelement für die bedingte Zugriffssteuerung schützen können, indem Sie Zugriffs-und Sitzungs Steuerelemente anwenden.

Mit der APP-Steuerelement für die bedingte Zugriffssteuerung können Benutzer-App-Zugriff und-Sitzungen basierend auf Zugriffs-und Sitzungs Richtlinien in Echtzeit überwacht und gesteuert werden. Zugriffs-und Sitzungs Richtlinien werden innerhalb des Cloud-App-Sicherheits Portals verwendet, um Filter weiter zu verfeinern und Aktionen für einen Benutzer festzulegen. Mit den Zugriffs-und Sitzungs Richtlinien können Sie Folgendes tun:

- **Blockieren beim Herunterladen**: Sie können den Download vertraulicher Dokumente blockieren. Beispielsweise auf nicht verwalteten Geräten.

- **Protect on Download**: anstatt den Download vertraulicher Dokumente zu blockieren, können Sie festlegen, dass Dokumente per Verschlüsselung beim Download geschützt werden müssen. Diese Verschlüsselung stellt sicher, dass das Dokument geschützt ist und der Benutzer Zugriff authentifiziert wird, wenn die Daten auf ein nicht vertrauenswürdiges Gerät heruntergeladen werden.

- **Überwachen von Benutzersitzungen mit niedriger Vertrauens**Ebene: riskante Benutzer werden überwachen, wenn Sie sich bei Apps anmelden und ihre Aktionen innerhalb der Sitzung protokolliert werden. Sie können das Benutzerverhalten untersuchen und analysieren, um zu verstehen, wo und unter welchen Bedingungen die Sitzungs Richtlinien zukünftig angewendet werden sollen.

- **Zugriff blockieren**: Sie können den Zugriff auf bestimmte Apps für Benutzer, die von nicht verwalteten Geräten oder von nicht-Unternehmensnetzwerken kommen, vollständig blockieren.

- **Schreibgeschützten Modus erstellen**: durch überwachen und blockieren benutzerdefinierter in-App-Aktivitäten können Sie einen schreibgeschützten Modus für bestimmte Apps für bestimmte Benutzer erstellen.

- **Einschränken von Benutzersitzungen von nicht-Unternehmensnetzwerken**: Benutzer, die über einen Standort, der nicht Teil Ihres Unternehmensnetzwerks ist, auf eine geschützte App zugreifen, haben Zugriff auf eingeschränkte Berechtigungen. Der Download von vertraulichen Materialien wird blockiert oder geschützt.

### <a name="how-session-control-works"></a>FunktionsWeise der Sitzungssteuerung

Durch das Erstellen einer Sitzungsrichtlinie mit der APP-Steuerelement für den bedingten Zugriff können Sie Benutzersitzungen steuern, indem Sie den Benutzer über einen Reverseproxy statt direkt an die APP umleiten. Von nun an gehen Benutzeranfragen und-Antworten durch Office 365 Cloud App Security anstatt direkt an die app.

Um den Benutzer innerhalb der Sitzung beizubehalten, werden alle relevanten URLs, Java-Skripts und Cookies innerhalb der App-Sitzung durch Office 365 Cloud App Security-URLs ersetzt. Wenn die APP beispielsweise eine Seite mit Links zurückgibt, deren Domänen mit myapp.com enden, wird die Verknüpfung durch Domänen beendet, die mit ungefähr folgendem enden: myapp.com.us.cas.ms

Bei dieser Methode müssen Sie nichts auf dem Gerät installieren. Diese Methode eignet sich ideal zum Überwachen von Sitzungen von nicht verwalteten Geräten.

Nachdem eine Sitzung durch Office 365 Cloud App Security geleitet wurde, können die folgenden Aktionen ausgeführt werden:

1. Überprüfen des Datenverkehrs für Benutzeraktivitäten

2. Anzeigen der identifizierten Aktivitäten im Sicherheits Aktivitätsprotokoll der Office 365 Cloud-App

3. Speichern der Datenverkehrs Protokolle und analysieren

4. Aktivieren des Administrators zum Exportieren der Datenverkehrs Protokolle

5. Erzwingen von Richtlinien für die Sitzung

## <a name="managed-device-identification"></a>Erkennung verwalteter Geräte

Mit der APP-Steuerelement für die bedingte Zugriffssteuerung können Sie Richtlinien erstellen, die berücksichtigen, ob ein Gerät verwaltet wird. Um zu ermitteln, ob ein Gerät verwaltet wird, verwendet die Funktion Folgendes:

- Kompatible Geräte

- Domänen verbundene Geräte

- Bereitstellung von Client Zertifikaten

### <a name="compliant-and-domain-joined-devices"></a>Kompatible und Domänen verbundene Geräte

Mit dem bedingten Zugriff von Azure AD können kompatible und Domänen verbundene Geräteinformationen direkt an Office 365 Cloud App Security übergeben werden. Von dort kann eine Zugriffsrichtlinie oder eine Sitzungsrichtlinie entwickelt werden, die den Gerätestatus als Filter verwendet. Weitere Informationen finden Sie in der [Einführung in die Geräteverwaltung in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).

### <a name="client-certificate-authenticated-devices"></a>Authentifizierte Geräte mit Client Zertifikat

Der Mechanismus zur Geräteidentifizierung kann die Authentifizierung von relevanten Geräten mithilfe von Clientzertifikaten anfordern. Sie können entweder vorhandene Clientzertifikate, die bereits in Ihrer Organisation bereitgestellt werden, oder neue Clientzertifikate auf verwalteten Geräten verwenden. Anschließend verwenden Sie das vorhanden sein dieser Zertifikate, um Zugriffs-und Sitzungs Richtlinien festzulegen. Informationen zur Bereitstellung von Clientzertifikaten finden Sie unter [Deploy Conditional Access app Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).

## <a name="supported-apps-and-clients"></a>Unterstützte apps und Clients

Die APP-Steuerelement für die bedingte Zugriffssteuerung für Office 365 unterstützt die folgenden vorgestellten Apps:

- Exchange Online (Vorschau)

- OneDrive for Business (Vorschau)

- Power BI (Vorschau)

- SharePoint Online (Vorschau)

- Microsoft Teams (Vorschau)

- Jammern (Vorschau)

Weitere apps werden kontinuierlich an die Sitzungssteuerung weitergegeben.

## <a name="next-steps"></a>Nächste Schritte

- [Bereitstellen von App-Steuerelement für den bedingten Zugriff für Office 365-apps](ocas-deploy-conditional-access-app-control.md)

- [Informationen zu Sitzungs Richtlinien in Office 365 Cloud App Security](ocas-session-policies.md)

- [Informationen zu Zugriffsrichtlinien in Office 365 Cloud App Security](ocas-access-policies.md) 