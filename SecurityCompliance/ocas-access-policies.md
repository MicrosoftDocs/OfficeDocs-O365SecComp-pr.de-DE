---
title: Zugriffsrichtlinien in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Office 365 Cloud App-Sicherheitszugriffs Richtlinien ermöglichen die Echtzeitüberwachung und Steuerung des Zugriffs auf Cloud-apps basierend auf Benutzer, Standort, Gerät und App. Sie können Zugriffsrichtlinien für ein beliebiges Gerät erstellen, einschließlich der Geräte, für die keine Domäne verbunden ist, und die nicht von Windows InTune verwaltet werden, indem Sie Clientzertifikate auf verwalteten Geräten oder mithilfe vorhandener Zertifikate wie Drittanbieter-MDM-Zertifikate bereitstellen. Sie können beispielsweise Clientzertifikate auf verwalteten Geräten bereitstellen und dann den Zugriff von Geräten ohne Zertifikat blockieren.
ms.openlocfilehash: a8651cb51419c93998f2ce6e176fab7c1651b6ea
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219775"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a>Zugriffsrichtlinien in Office 365 Cloud App Security

|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](group-your-ip-addresses-in-ocas.md) <br/> |[Verwendung beginnen](utilization-activities-for-ocas.md) <br/> |

Office 365 Cloud App-Sicherheitszugriffs Richtlinien ermöglichen die Echtzeitüberwachung und Steuerung des Zugriffs auf Cloud-apps basierend auf Benutzer, Standort, Gerät und App. Sie können Zugriffsrichtlinien für ein beliebiges Gerät erstellen, einschließlich der Geräte, für die keine Domäne verbunden ist, und die nicht von Windows InTune verwaltet werden, indem Sie Clientzertifikate auf verwalteten Geräten oder mithilfe vorhandener Zertifikate wie Drittanbieter-MDM-Zertifikate bereitstellen. Sie können beispielsweise Clientzertifikate auf verwalteten Geräten bereitstellen und dann den Zugriff von Geräten ohne Zertifikat blockieren.

Anstatt den Zugriff vollständig zuzulassen oder zu blockieren, können Sie mit [Sitzungs Richtlinien](ocas-session-policies.md) Zugriff gewähren, während Sie die Sitzung überwachen und/oder bestimmte Sitzungsaktivitäten einschränken.

## <a name="prerequisites-to-using-access-policies"></a>VoraussetZungen für die Verwendung von Zugriffsrichtlinien

- Azure AD Premium P1-Lizenz

- Die relevanten apps sollten [mit Conditional Access-App-Steuerelement bereitgestellt](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad) werden.

- eine [richtlinie](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) für den Azure AD-bedingten zugriff sollte vorhanden sein, die benutzer wie unten beschrieben zu Office 365 Cloud App Security umleitet.

## <a name="create-an-azure-ad-conditional-access-policy"></a>Erstellen einer Richtlinie für den Azure AD-bedingten Zugriff

Azure Active Directory-Richtlinien für den bedingten Zugriff und Cloud-App-Sicherheits Sitzungs Richtlinien arbeiten zusammen, um jede Benutzersitzung zu überprüfen und Richtlinien Entscheidungen für jede APP zu treffen. Gehen Sie folgendermaßen vor, um eine Richtlinie für den bedingten Zugriff in Azure AD einzurichten:

1. Konfigurieren Sie eine [Azure AD-Richtlinie](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) für den bedingten Zugriff mit Zuweisungen für Benutzer oder Gruppen von Benutzern und die APP, die Sie mit der APP-Steuerelement Steuerung für bedingte Zugriffssteuerung steuern möchten.<br>Hinweis: nur apps, die [mit Conditional Access-App-Steuerelement bereitgestellt](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad)wurden, sind von dieser Richtlinie betroffen.

2. leiten sie benutzer an Office 365 Cloud app Security weiter, indem sie unter **sitzung**die option **Conditional Access-app-steuerelement mit bedingtem zugriff verwenden**aktivieren.

## <a name="create-a-cloud-app-security-access-policy"></a>Erstellen einer Cloud-App-Sicherheitszugriffs Richtlinie

Gehen Sie folgendermaßen vor, um eine neue Zugriffsrichtlinie zu erstellen:

1. Wählen Sie im Portal **Steuerelement** gefolgt von **Richtlinien**aus.

2. Klicken Sie auf der Seite **Richtlinien** auf **Richtlinie** erstellen, und wählen Sie **Zugriffsrichtlinie**aus.

3. Weisen Sie im Fenster **Zugriffsrichtlinie** einen Namen für die Richtlinie zu, beispielsweise den *Zugriff auf nicht verwalteten Geräten blockieren*.

4. Wählen Sie in den Aktivitäten, die mit dem **folgenden** Abschnitt übereinstimmen, unter **Aktivitäts Quelle**die Option Weitere Aktivitäts Filter aus, die auf die Richtlinie angewendet werden sollen. Zu den Filtern gehört Folgendes:
    
    - **Geräte Tags**: Verwenden Sie diesen Filter, um nicht verwaltete Geräte zu identifizieren.
    
    - **Speicherort**: Verwenden Sie diesen Filter, um unbekannte (und daher riskante) Speicherorte zu identifizieren.
    
    - **IP-Adresse**: Verwenden Sie diesen Filter, um nach IP-Adressen zu filtern oder zuvor zugewiesene IP-Adress Tags zu verwenden.
    
    - **Benutzer-Agent-Tag**: Verwenden Sie diesen Filter, um die Heuristik zur Identifizierung mobiler und Desktop-Apps zu aktivieren. Dieser Filter kann auf Equals oder ungleich festgelegt werden. Die Werte sollten für jede Cloud-App mit ihren mobilen und Desktop-Apps getestet werden.

5. Wählen Sie unter **Aktionen**eine der folgenden Optionen aus:
    
    - **Zulassen**: Legen Sie diese Aktion so fest, dass der Zugriff entsprechend den von Ihnen festgelegten Richtlinien Filtern explizit zugelassen wird.
    
    - **Blockieren**: Legen Sie diese Aktion so fest, dass der Zugriff entsprechend den festgelegten Richtlinien Filtern explizit blockiert wird.

6. Sie können **eine Warnung für jedes übereinstimmende Ereignis mit dem Schweregrad der Richtlinie erstellen**und einen Warnungsgrenzwert festlegen und auswählen, ob die Warnung als e-Mail, als Textnachricht oder als beides angezeigt werden soll.

## <a name="next-steps"></a>Nächste Schritte

- [Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung in Office 365 Cloud App Security](group-your-ip-addresses-in-ocas.md)