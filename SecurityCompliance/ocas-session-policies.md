---
title: Sitzungsrichtlinien in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Office 365 Cloud App Security-Sitzungs Richtlinien ermöglichen die Überwachung auf Sitzungsebene in Echtzeit und bieten eine detaillierte Sichtbarkeit auf Office 365-apps und die Möglichkeit, verschiedene Aktionen abhängig von der für eine Benutzersitzung festgelegten Richtlinie durchführen zu können. Anstatt den Zugriff vollständig zuzulassen oder zu blockieren, können Sie mit der Sitzungssteuerung Zugriff gewähren, während Sie die Sitzung überwachen und/oder bestimmte Sitzungsaktivitäten mithilfe der Reverse-Proxy-Funktionen der APP-Steuerung für den bedingten Zugriff einschränken.
ms.openlocfilehash: e0e4b04ee8cc0f7a14adbc26b074a5f2947e44c2
ms.sourcegitcommit: 866d8cab6bcfdd124516a8369e47ec797bc7cf8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2019
ms.locfileid: "30312092"
---
# <a name="session-policies-in-office-365-cloud-app-security"></a>Sitzungsrichtlinien in Office 365 Cloud App Security

|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](ocas-access-policies.md) <br/> |[Verwendung beginnen](utilization-activities-for-ocas.md) <br/> |

Office 365 Cloud App Security-Sitzungs Richtlinien ermöglichen die Überwachung auf Sitzungsebene in Echtzeit und bieten eine detaillierte Sichtbarkeit auf Office 365-apps und die Möglichkeit, verschiedene Aktionen abhängig von der für eine Benutzersitzung festgelegten Richtlinie durchführen zu können. Anstatt den Zugriff vollständig zuzulassen oder zu blockieren, können Sie mit der Sitzungssteuerung Zugriff gewähren, während Sie die Sitzung überwachen und/oder bestimmte Sitzungsaktivitäten mithilfe der Reverse-Proxy-Funktionen der APP-Steuerung für den bedingten Zugriff einschränken.

Sie können beispielsweise entscheiden, dass Sie auf nicht verwalteten Geräten oder für Sitzungen, die von bestimmten Orten kommen, dem Benutzer den Zugriff auf die APP erlauben, aber auch den Download vertraulicher Dateien einschränken oder festlegen müssen, dass bestimmte Dokumente beim Download geschützt werden müssen. Mithilfe von Sitzungs Richtlinien können Sie diese Benutzer Sitzungs Steuerelemente festlegen und den Zugriff gewähren und Folgendes ermöglichen:

- [Überwachen aller Aktivitäten](#monitor-all-activities)

- [Alle Downloads blockieren](#block-all-downloads)

- [Blockieren bestimmter Aktivitäten](#block-specific-activities)

- [Schützen von Dateien beim Download](#protect-files-on-download)

## <a name="prerequisites-to-using-session-policies"></a>VoraussetZungen für die Verwendung von Sitzungs Richtlinien

- Azure AD Premium P1-Lizenz

- Die relevanten Office 365-apps sollten [mit Conditional Access-App-Steuerelement bereitgestellt](ocas-deploy-conditional-access-app-control.md) werden.

- eine [richtlinie](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) für den Azure AD-bedingten zugriff sollte vorhanden sein, die benutzer zu Office 365 Cloud App Security umleitet

## <a name="create-an-azure-ad-conditional-access-policy"></a>Erstellen einer Richtlinie für den Azure AD-bedingten Zugriff

Azure Active Directory-Richtlinien für den bedingten Zugriff und Cloud-App-Sicherheits Sitzungs Richtlinien arbeiten zusammen, um jede Benutzersitzung zu überprüfen und Richtlinien Entscheidungen für jede APP zu treffen. Gehen Sie folgendermaßen vor, um eine Richtlinie für den bedingten Zugriff in Azure AD einzurichten:

1. Konfigurieren Sie eine [Azure AD-Richtlinie](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) für den bedingten Zugriff mit Zuweisungen für einen Benutzer oder eine Gruppe von Benutzern und die APP, die Sie mit der APP-Steuerelement für die bedingte Zugriffssteuerung steuern möchten. Hinweis: nur apps, die [mit Conditional Access-App-Steuerelement bereitgestellt](ocas-deploy-conditional-access-app-control.md)wurden, sind von dieser Richtlinie betroffen.

2. leiten sie benutzer an Office 365 Cloud app Security weiter, indem sie auf der seite **sitzung** die  **einschränkungen für bedingte zugriffs-app-steuerung erzwingen verwenden**auswählen.

## <a name="create-a-cloud-app-security-session-policy"></a>Erstellen einer Cloud-App-Sicherheits Sitzungsrichtlinie

Gehen Sie folgendermaßen vor, um eine neue Sitzungsrichtlinie zu erstellen:

1. Wählen Sie im Portal **Steuerelement** gefolgt von **Richtlinien**aus.

2. Klicken Sie auf der Seite **Richtlinien** auf **Richtlinie** erstellen, und wählen Sie **Sitzungsrichtlinie**aus.

3. Weisen Sie im Fenster **Sitzungsrichtlinie** einen Namen für die Richtlinie zu.

4. Im Feld **Sitzungs Steuerelementtyp**:
    
    - Wählen Sie **Monitor nur** aus, wenn Sie nur Aktivitäten von Benutzern überwachen möchten. Bei Auswahl dieser Option wird eine nur-Monitor-Richtlinie für die ausgewählten Apps erstellt, in denen alle Anmelde-, heuristischen und Aktivitätstypen heruntergeladen werden.
    
    - Wählen Sie **Dateidownload Steuern (mit DLP)** aus, wenn Sie Benutzeraktivitäten überwachen möchten. Sie können zusätzliche Aktionen wie blockieren oder schützen von Downloads für Benutzer ausführen.
    
    - Wählen Sie **Aktivitäten** blockieren aus, um bestimmte Aktivitäten zu blockieren, die Sie mithilfe des **Aktivitätstyp** Filters auswählen können. Alle Aktivitäten aus ausgewählten apps werden überwacht (und im Aktivitätsprotokoll angezeigt). Die ausgewählten Aktivitäten werden blockiert, wenn Sie die Aktion **blockieren** auswählen. Die ausgewählten Aktivitäten lösen Warnungen aus, wenn Sie die **Test** Aktion auswählen und Warnungen aktiviert haben.

5. Wählen Sie unter **Aktivitäts Quelle** in den Aktivitäten, die mit dem **folgenden** Abschnitt übereinstimmen, zusätzliche Aktivitäts Filter aus, die auf die Richtlinie angewendet werden sollen. Diese Filter können die folgenden Optionen aufweisen:
    
    - **Geräte Tags**: Verwenden Sie diesen Filter, um nicht verwaltete Geräte zu identifizieren.
    
    - **Speicherort**: Verwenden Sie diesen Filter, um unbekannte (und daher riskante) Speicherorte zu identifizieren.
    
    - **IP-Adresse**: Verwenden Sie diesen Filter, um nach IP-Adressen zu filtern oder zuvor zugewiesene IP-Adress Tags zu verwenden.
    
    - **Benutzer-Agent-Tag**: Verwenden Sie diesen Filter, um die Heuristik zur Identifizierung mobiler und Desktop-Apps zu aktivieren. Dieser Filter kann auf Equals oder nicht auf **Native Client**festgelegt werden. Dieser Filter sollte für jede Cloud-App mit ihren mobilen und Desktop-Apps getestet werden.<br>Hinweis: Sitzungs Richtlinien unterstützen keine mobilen und Desktop-Apps. Mobile Apps und Desktop-Apps können auch blockiert oder zugelassen werden, indem eine Zugriffsrichtlinie erstellt wird.

6. Wenn Sie die Option zum **Steuern des Dateidownloads (mit DLP)** ausgewählt haben, wählen Sie unter **Aktivitäts Quelle** in den Dateien, die mit **dem folgenden** Abschnitt übereinstimmen, zusätzliche Dateifilter aus, die auf die Richtlinie angewendet werden sollen. Diese Filter können die folgenden Optionen aufweisen:
        
    - **Klassifizierungs Bezeichnung** : Verwenden Sie diesen Filter, wenn Ihre Organisation Azure Information Protection verwendet und Ihre Daten durch die Klassifizierungs Bezeichnungen geschützt wurden. Sie können Dateien basierend auf der Klassifizierungs Bezeichnung filtern, die Sie auf Sie angewendet haben. Weitere Informationen zur Integration mit Azure Information Protection finden Sie unter [Azure Information Protection Integration](https://docs.microsoft.com/cloud-app-security/azip-integration).
        
    - **Dateiname** – verwenden Sie diesen Filter, um die Richtlinie auf bestimmte Dateien anzuwenden.
        
    - **Dateityp** – verwenden Sie diesen Filter, um die Richtlinie auf bestimmte Dateitypen anzuwenden, beispielsweise den Download für alle XLS-Dateien zu blockieren.
    
    - Legen Sie im Abschnitt **Inhaltsprüfung** fest, ob das DLP-Modul zum Überprüfen von Dokumenten und Dateiinhalten aktiviert werden soll.
    
    - Wählen Sie unter **Aktionen**eines der folgenden Elemente aus:
        
        - **Test (alle Aktivitäten überwachen)**: Legen Sie diese Aktion fest, um den Download entsprechend den festgelegten Richtlinien Filtern explizit zuzulassen.
        
        - **Blockieren (Dateidownload blockieren und alle Aktivitäten überwachen)**: Legen Sie diese Aktion fest, um den Download explizit gemäß den festgelegten Richtlinien Filtern zu blockieren. Weitere Informationen finden Sie unter [Funktionsweise des Block Downloads](https://docs.microsoft.com/en-us/cloud-app-security/session-policy-aad#block-download).
        
        - **Protect (Klassifikations Bezeichnung anwenden zum herunterladen und Überwachen aller Aktivitäten)**: diese Option ist nur verfügbar, wenn Sie unter **Sitzungsrichtlinie**den **Kontrolldatei Download (mit DLP)** ausgewählt haben. Wenn in Ihrer Organisation Azure Information Protection verwendet wird, können Sie eine **Aktion** festlegen, um einen Klassifikations Bezeichnungs Satz in Azure Information Protection auf die Datei anzuwenden. Weitere Informationen finden Sie unter [How Protect Download Works](https://docs.microsoft.com/en-us/cloud-app-security/session-policy-aad#protect-download).

7. Sie können **eine Warnung für jedes übereinstimmende Ereignis mit dem Schweregrad der Richtlinie erstellen**und einen Warnungsgrenzwert festlegen. Wählen Sie aus, ob die Warnung als e-Mail, als Textnachricht oder als beides angezeigt werden soll.

## <a name="monitor-all-activities"></a>Überwachen aller Aktivitäten

Wenn Sie eine Sitzungsrichtlinie erstellen, wird jede Benutzersitzung, die mit der Richtlinie übereinstimmt, an das Sitzungs Steuerelement umgeleitet und nicht direkt an die app. Dem Benutzer wird ein Überwachungs Hinweis angezeigt, damit er weiß, dass seine Sitzungen überwacht werden.

Wenn Sie den Benutzer nicht benachrichtigen möchten, dass er überwacht wird, können Sie die Benachrichtigung deaktivieren.

1. Wählen Sie unter den Einstellungen Cog die Option **Allgemeine Einstellungen**aus.

2. Wählen Sie dann unter **Conditional Access-App-Steuerelement**  **Benutzerüberwachung** aus, und deaktivieren Sie das Kontrollkästchen **Benutzer** benachrichtigen.

Um den Benutzer innerhalb der Sitzung beizubehalten, ersetzt die APP-Steuerelement für die bedingte Zugriffssteuerung alle relevanten URLs, Java-Skripts und Cookies innerhalb der App-Sitzung mit Sicherheits-URLs von Office 365 Cloud app. Wenn die APP beispielsweise eine Seite mit Links zurückgibt, deren Domänen mit `myapp.com`endet, ersetzt die APP-Steuerelement für die Conditional Access-Anwendung `myapp.com.us.cas.ms`die Links durch Domänen, die mit so etwas enden. Auf diese Weise wird die gesamte Sitzung von Office 365 Cloud App Security überwacht.

App-Steuerelement für die bedingte Zugriffssteuerung zeichnet die Datenverkehrs Protokolle jeder Benutzersitzung auf, die weitergeleitet wird. Die Datenverkehrs Protokolle schließen die Uhrzeit, die IP-Adresse, den Benutzer-Agent, die besuchten URLs und die Anzahl der hochgeladenen und heruntergeladenen Bytes ein. Diese Protokolle werden analysiert, und der Liste der Cloud-Discovery-Berichte im Dashboard für die Cloud-Suche wird die Cloud **App Security Conditional Access-App-Steuerung**hinzugefügt.

### <a name="to-export-these-logs"></a>So exportieren Sie diese Protokolle:

1. Wechseln Sie zum COG Einstellungen, und klicken Sie auf **App-Steuerelement für bedingte Zugriffsrechte**.

2. Klicken Sie auf der rechten Seite der Tabelle auf die Schaltfläche Exportieren.<br>![Schaltfläche "Exportieren"](media/image3.png)<br>

3. Wählen Sie den Bereich des Berichts aus, und klicken Sie auf **exportieren**. Dieser Vorgang kann einige Zeit in Anspruch nehmen.

### <a name="to-download-the-exported-log"></a>So laden Sie das exportierte Protokoll herunter:

1. Nachdem der Bericht fertig ist, wechseln Sie zu **Einstellungen** , und exportieren Sie dann **Berichte**.

2. Wählen Sie in der Tabelle den relevanten Bericht aus der Liste der **Datenverkehrs Protokolle** für die bedingte Zugriffssteuerung aus, und klicken Sie auf herunterladen.<br>![Schaltfläche "herunterladen"](media/image4.png)<br>

## <a name="block-all-downloads"></a>Alle Downloads blockieren

Wenn **Block** als die **Aktion** festgelegt wird, die Sie in der Cloud-App-Sicherheits Sitzungsrichtlinie ausführen möchten, wird durch die APP-Steuerelement Steuerung verhindert, dass ein Benutzer eine Datei gemäß den Dateifiltern der Richtlinie herunterlädt. Ein Download-Ereignis wird von Office 365 Cloud App Security für jede APP erkannt, wenn ein Benutzer einen Download startet. App-Steuerelement für bedingten Zugriff greift in Echtzeit ein, um die Ausführung zu verhindern. Wenn das Signal empfangen wurde, dass ein Benutzer einen Download initiiert hat, gibt die Conditional Access-App-Steuerelement eine **herunter** geladene eingeschränkte Nachricht an den Benutzer zurück und ersetzt die heruntergeladene Datei durch eine Textdatei. Die Nachricht der Textdatei an den Benutzer kann aus der Sitzungsrichtlinie konfiguriert und angepasst werden.

## <a name="block-specific-activities"></a>Blockieren bestimmter Aktivitäten

Wenn **Block Aktivitäten** als Aktivitätstyp fest **** gelegt ist, können Sie bestimmte Aktivitäten zum Blockieren in bestimmten apps auswählen. Alle Aktivitäten aus ausgewählten apps werden im Aktivitätsprotokoll überwacht und angezeigt. Die ausgewählten Aktivitäten werden blockiert, wenn Sie die Aktion **blockieren** auswählen. Die ausgewählten Aktivitäten lösen Warnungen aus, wenn Sie die **Test** Aktion auswählen und Warnungen aktiviert haben.

**Blockieren Sie bestimmte Aktivitäten** , und wenden Sie Sie auf bestimmte Gruppen an, um einen umfassenden schreibgeschützten Modus für Ihre Organisation zu erstellen.

## <a name="protect-files-on-download"></a>Schützen von Dateien beim Download

Wählen Sie **Aktivitäten** blockieren aus, um bestimmte Aktivitäten zu blockieren, die Sie mithilfe des **Aktivitätstyp** Filters finden können. Alle Aktivitäten aus ausgewählten apps werden überwacht (und im Aktivitätsprotokoll angezeigt). Die ausgewählten Aktivitäten werden blockiert, wenn Sie die Aktion **blockieren** auswählen. Die ausgewählten Aktivitäten lösen Warnungen aus, wenn Sie die **Test** Aktion auswählen und Warnungen aktiviert haben.

Wenn **Protect** als die **Aktion** festgelegt wird, die in der Sicherheits Sitzungsrichtlinie für Cloud-apps ausgeführt werden soll, erzwingt die Steuerelement-App-Steuerung die Kennzeichnung und den nachfolgenden Schutz einer Datei gemäß den Dateifiltern der Richtlinie. Bezeichnungen werden in der Azure Information Protection-Konsole konfiguriert, und **Protect** muss innerhalb der Bezeichnung ausgewählt werden, damit Sie als Option in der Sicherheitsrichtlinie für die Cloud-App angezeigt wird. Wenn eine Bezeichnung ausgewählt ist und eine Datei heruntergeladen wird, die den Kriterien der Cloud-App-Sicherheitsrichtlinie entspricht, wird die Bezeichnung und der entsprechende Schutz (mit Berechtigungen) beim Herunterladen auf die Datei angewendet. Die ursprüngliche Datei bleibt unverändert in der Cloud-APP, während die heruntergeladene Datei nun geschützt ist. Benutzer, die versuchen, auf die Datei zuzugreifen, müssen die durch den Schutz angewendeten Berechtigungsanforderungen erfüllen.

## <a name="next-steps"></a>Nächste Schritte

- [Informationen zu Zugriffsrichtlinien in Office 365 Cloud App Security](ocas-access-policies.md)

- [Blockieren von Downloads auf nicht verwalteten Geräten mithilfe von Azure AD Conditional Access-App-Steuerelementen](https://docs.microsoft.com/en-us/cloud-app-security/use-case-proxy-block-session-aad)

