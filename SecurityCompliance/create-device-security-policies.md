---
title: Erstellen und Bereitstellen von Gerätesicherheitsrichtlinien
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/9/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewDevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: d310f556-8bfb-497b-9bd7-fe3c36ea2fd6
description: 'Schritte zum Erstellen und Bereitstellen von Sicherheitsrichtlinien für die Verwaltung mobiler Geräte in Office 365, in denen werden Schützen Ihrer Organisation Informationen zu Office 365 vor nicht autorisiertem Zugriff. '
ms.openlocfilehash: ab1fc1960a3e55eb3080dde7df0ec742c58b2cc7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272070"
---
# <a name="create-and-deploy-device-security-policies"></a>Erstellen und Bereitstellen von Gerätesicherheitsrichtlinien

Mobile Device Management für Office 365 können Sie Sicherheitsrichtlinien erstellen, mit denen Ihre Organisation Informationen zu Office 365 vor nicht autorisiertem Zugriff geschützt. Sie können Richtlinien auf einem beliebigen mobilen Gerät in Ihrer Organisation anwenden, der Benutzer des Geräts verfügt über eine entsprechende Office 365-Lizenz und das Gerät im MDM für Office 365 registriert hat.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Informationen Sie zu den Geräten, Mobilgerät apps und Sicherheitseinstellungen, die für Office 365 MDM unterstützt. Finden Sie unter [Funktionen der Verwaltung von mobilen Geräten für Office 365](capabilities-of-mobile-device-management.md).
    
- Erstellen von Sicherheitsgruppen, die Office 365-Benutzer enthalten, denen Sie Richtlinien zum bereitstellen möchten, und für Benutzer, dass verhindern ausschließen soll Zugriff auf Office 365 gesperrt. Es wird empfohlen, bevor Sie eine neue Richtlinie für Ihre Organisation bereitstellen, die Richtlinie zu testen, indem es eine kleine Anzahl von Benutzern bereitgestellt. Sie können erstellen und verwenden eine Sicherheitsgruppe, die enthält nur sich selbst oder eine kleine Zahl Office 365-Benutzer, die die Richtlinie für Sie testen können. Weitere Informationen zu Sicherheitsgruppen finden Sie unter [erstellen, bearbeiten oder Löschen einer Sicherheitsgruppe](https://go.microsoft.com/fwlink/p/?LinkId=518555).
    
- **Wichtig:** Bevor Sie eine Richtlinie für mobile Geräte erstellen können, müssen Sie aktivieren und MDM für Office 365 einrichten. Finden Sie unter [Übersicht über die Verwaltung von mobilen Geräten für Office 365](overview-of-mdm.md).
    
- Zum Erstellen und Bereitstellen von Richtlinien für mobile Geräte Management in Office 365, müssen Sie ein Office 365 Admin global. Finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/d10608af-7934-490a-818e-e68f17d0e9c1).
    
- Vor der Bereitstellung von Richtlinien können Sie Ihre Organisation die potenziellen Auswirkungen Registrieren eines Geräts in MDM für Office 365 kennen. Je nachdem, wie Sie die Richtlinien einrichten nicht konformer Geräte können aus den Zugriff auf Office 365 blockiert werden, und Daten, einschließlich der installierten Programme, Fotos und persönlichen Informationen auf einem Gerät registrierten, gelöscht werden.
    
> [!NOTE]
> Richtlinien und Zugriffsregeln für Office 365 in MDM erstellt werden Exchange ActiveSync-Postfachrichtlinien für mobile Geräte und in der Exchange-Verwaltungskonsole erstellt gerätezugriffsregeln außer Kraft setzen. Nachdem ein Gerät für Office 365, alle Exchange ActiveSync-Postfachrichtlinie Mobilgerät MDM registriert ist oder gerätezugriffsregel angewendet auf das Gerät wird ignoriert. Weitere Informationen zu Exchange ActiveSync finden Sie unter [Exchange ActiveSync in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=524380). 
  
## <a name="step-1-create-a-security-policy-and-deploy-to-a-test-group"></a>Schritt 1: Erstellen einer Sicherheitsrichtlinie und Bereitstellen einer Testgruppe

Bevor Sie beginnen können, stellen Sie sicher, dass Sie aktiviert und Einrichten von MDM für Office 365. Weitere Informationen finden Sie in der [Übersicht der Verwaltung mobiler Geräte für Office 365](overview-of-mdm.md) . 
  
1. In Office 365 in das Wertpapier &amp; Compliance Center, navigieren Sie zur **Verhinderung von Datenverlust** \> **Sicherheitsrichtlinien für Geräte**.
    
    > [!NOTE]
    > Die **Sicherheitsrichtlinien für Geräte** wird im Menü angezeigt, nachdem Sie die Verwaltung von mobilen Geräten aktiviert haben. 
  
2. Wählen Sie **+ Richtlinie erstellen**.
    
    ![Erstellen eine Richtlinie für MDN Geräte unter Sicherheitsrichtlinien für Geräte](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
3. Geben Sie einen **Namen** und eine **Beschreibung** für die neue Richtlinie, und wählen Sie dann auf **Weiter**.
    
    ![Einen Namen für das Gerät Codezugriffssicherheits-Richtlinie festlegen](media/d382e845-4a7f-4f72-8a09-813ea4cbd0c4.png)
  
4. Klicken Sie auf die **welche Anforderungen möchten Sie, dass auf Geräten?** Seite, geben Sie die Anforderungen angewendet auf mobilen Geräten in Ihrer Organisation soll, und wählen Sie dann auf **Weiter**.
    
    ![Der Seite Einstellungen für Sicherheitsrichtlinien des Geräts](media/186b3bd5-5e3d-4059-978f-94113111a8ca.png)
  
5. Klicken Sie auf die **Was möchten Sie konfigurieren?** Seite, geben Sie zusätzlichen Anforderungen angewendet auf mobilen Geräten in Ihrer Organisation soll, und wählen Sie dann auf **Weiter**.
    
6. Klicken Sie auf die **möchten Sie diese Richtlinie jetzt anwenden?** Seite, wählen Sie **Ja**aus, und wählen Sie dann **+ Hinzufügen**. 
    
    ![Die Richtlinie hinzufügen](media/89ab7cab-1b7a-4c78-9aa6-3db7d7667f8e.png)
  
7. Wählen Sie die Gruppe, die die Richtlinie testen wird, bevor Sie in Ihrer Organisation bereitzustellen, und wählen Sie dann auf **Hinzufügen**.
    
8. Klicken Sie auf **Weiter**.
    
9. Überprüfen Sie und bestätigen Sie die Details der neuen Geräterichtlinie ein, und wählen Sie dann **diese Richtlinie erstellen**.
    
    ![Wählen Sie diese Richtlinie zum Erstellen einer Geräterichtlinie Finsih erstellen](media/e410bcf3-8a36-44ed-9fea-00e742db06fb.png)
  
10. Klicken Sie auf **Schließen**.
    
Jeder Benutzer, die die Richtlinie gilt, muss die Richtlinie auf ihrem Gerät das nächste Mal Anmeldung bei Office 365 mit ihrem mobilen Gerät abgelegt. Wenn Benutzer eine Richtlinie auf ihrem mobilen Gerät vor angewendet wurde noch nicht, klicken Sie dann erhalten nach der Bereitstellung von Richtlinien für des sie eine Benachrichtigung auf ihrem Gerät, die die [Schritte zum Registrieren und Aktivieren des MDM für Office 365](https://go.microsoft.com/fwlink/?LinkId=615272)umfasst. Bis sie Registrierung abgeschlossen haben, werden Zugriff auf e-Mail, OneDrive und andere Dienste beschränkt werden. Nach Abschluss Registrierung mit Intune Unternehmensportal app werden die Dienste verwenden können, und auf ihrem Gerät die Richtlinie angewendet werden.
  
## <a name="step-2-verify-your-policy-works"></a>Schritt 2: Überprüfen Sie Ihre Funktionsweise der Gruppenrichtlinien

Nachdem Sie eine Sicherheitsrichtlinie erstellt haben, sollten Sie überprüfen, dass die Richtlinie funktioniert wie erwartet, bevor Sie ihn für Ihre Organisation bereitstellen.
  
1. In Office 365, wechseln Sie zur **Sicherheit &amp; Compliance Center** \> **Verhinderung von Datenverlust** \> **Gerätemanagement**.
    
2. Überprüfen Sie den Status des Benutzers Geräte, die die Richtlinie angewendet haben, auf der Seite **Verwaltung der mobiler Geräte für Office 365** . Sie können filtern oder Sortieren von **Alle** Anzeigen aller Geräte oder **blockiert** , blockierte Geräte anzeigen. 
    
    ![Anzeigen von Geräten, die von MDM verwaltet werden](media/5c9fd069-b716-40d8-9b36-f9cfeae2139f.png)
  
3. Sie können auch eine vollständige oder eine selektive Remotegerätzurücksetzung auf dem Gerät ausführen. Anweisungen finden Sie unter [Löschen ein mobiles Geräts in Office 365](wipe-a-mobile-device.md).
    
## <a name="step-3-deploy-a-policy-to-your-organization"></a>Schritt 3: Bereitstellen einer Richtlinie für Ihre Organisation

Nachdem Sie eine Richtlinie für mobile Geräte erstellt und sichergestellt, dass diese wie erwartet funktioniert haben, stellen sie für Ihre Organisation bereit.
  
1. In Office 365, wechseln Sie zur **Sicherheit &amp; Compliance Center** \> **Verhinderung von Datenverlust** \> **Sicherheitsrichtlinien für Geräte**.
    
2. Wählen Sie die Richtlinie, die Sie bereitstellen möchten, und wählen Sie **Richtlinie bearbeiten** in der \< _Richtlinienname_ \> Systemsteuerung.  
    
3. Wählen Sie die Registerkarte **Bereitstellung** aus. 
    
4. Wählen Sie auf der Registerkarte **Bereitstellung** **Ja** oben **Wählen Sie eine oder mehrere Sicherheitsgruppen enthalten, die die Personen, die diese Richtlinie angewendet werden soll** , und klicken Sie dann **Hinzufügen**aus.
    
  - Klicken Sie im Bereich **Wählen Sie Gruppe** die Suche nach einer Gruppe hinzufügen können, können Sie durch Alias oder nach dem Anzeigenamen filtern. Sie können auch eine vorhandene Gruppe aus der Liste **Gruppen** hinzufügen. 
    
    Sie können mehrere Gruppen zum Anwenden der Richtlinie auf Hinzufügen.
    
    Wählen Sie **Add** am unteren Rand der Systemsteuerung. 
    
5. Wählen Sie auf der Registerkarte **Bereitstellung** **Speichern** . 
    
    ![Bereitstellen von MDM Richtlinien in Ihrer Organisation.](media/dc3e7fe5-201a-4e45-abe3-fc93e0b59028.png)
  
Jeder Benutzer, die die Richtlinie gilt, muss die Richtlinie auf ihrem Gerät das nächste Mal zu Office 365 auf ihrem mobilen Gerät Anmeldung abgelegt. Wenn Benutzer eine Richtlinie auf ihrem mobilen Gerät angewendet wurde noch nicht, benötigen sie [erhalten eine Benachrichtigung auf ihrem Gerät](https://go.microsoft.com/fwlink/?LinkId=615272) mit Schritte zum Registrieren und für Office 365 für MDM zu aktivieren. Nachdem sie die Registrierung abgeschlossen haben, wird die Richtlinie auf ihrem Gerät angewendet werden. 
  
## <a name="step-4-block-email-access-for-unsupported-devices"></a>Schritt 4: E-Mail-Zugriff für nicht unterstützter Geräte blockieren

Zum Sichern sollten Informationen Ihres Unternehmens, Sie app-Zugriff auf Office 365-e-Mail für mobile Geräte blockieren, die von MDM für Office 365 nicht unterstützt werden. Eine Liste der unterstützten Geräte finden Sie unter [Funktionen der integrierten Verwaltung mobiler Geräte für Office 365](capabilities-of-mobile-device-management.md) . Dazu: 
  
1. Wechseln Sie zu Sicherheit &amp; Compliance Center\> **Verhinderung von Datenverlust** \> **Sicherheitsrichtlinien für Geräte**.
    
2. Wählen Sie **organisationsweiten Gerät Access-Einstellungen verwalten**.
    
    ![Wechseln Sie zu Compliance Center \> Geräte und klicken Sie auf die Einstellungen verwalten Gerät Access verknüpfen.](media/b9f4da3c-dfa5-4913-8482-42a077cb4f56.png)
  
3. Um nicht unterstützter Geräte zu blockieren, wählen Sie im **Block** unter **Wenn ein Gerät nicht, durch MDM für Office 365 unterstützt wird, Sie möchten zulassen oder Blockieren von mit einem Exchange-Konto Zugriff auf Ihre Organisation e-Mail** \> **Speichern**.
  
## <a name="step-5-choose-security-groups-to-be-excluded-from-conditional-access-checks"></a>Schritt 5: Auswählen von aus Überprüfungen für den bedingten Zugriff auszuschließenden Sicherheitsgruppen

Wenn Sie einige Personen aus den Überprüfungen für den bedingten Zugriff auf ihren Mobilgeräten ausschließen möchten und Sie mindestens eine Sicherheitsgruppe für diese Personen erstellt haben, fügen Sie die Sicherheitsgruppen hier hinzu. Bei den Personen in diesen Gruppen werden keine Richtlinien für ihre unterstützten Mobilgeräte erzwungen.
  
1. Wechseln Sie zu Sicherheit &amp; Compliance Center\> **Verhinderung von Datenverlust** \> **Sicherheitsrichtlinien für Geräte**.
    
2. Wählen Sie **organisationsweiten Gerät Access-Einstellungen verwalten**.
    
    ![Wechseln Sie zu Compliance Center \> Geräte und klicken Sie auf die Einstellungen verwalten Gerät Access verknüpfen.](media/b9f4da3c-dfa5-4913-8482-42a077cb4f56.png)
  
3. Wählen Sie **Hinzufügen** auf Hinzufügen, dass die Sicherheitsgruppe, die Benutzer, die verfügt ausgeschlossen werden sollen, Zugriff auf Office 365 blockiert. Wenn ein Benutzer zu dieser Liste hinzugefügt wurde, werden sie Office 365-e-Mail zuzugreifen, wenn Sie ein nicht unterstütztes Gerät verwenden werden. 
    
4. Wählen Sie die Sicherheitsgruppe, den, die Sie im Bereich **Wählen Sie Gruppe** verwenden möchten. 
    
5. Wählen Sie Namen ein, und klicken Sie dann **Hinzufügen** \> **Speichern**.
    
6. Wählen Sie im Bereich **Einstellungen für die Organisation geltende Gerät** **Speichern**aus.
  
## <a name="what-is-the-impact-of-security-policies-on-different-device-types"></a>Wie wirken sich Sicherheitsrichtlinien auf verschiedene Gerätetypen aus?

Wenn Sie eine Richtlinie für Benutzergeräte anwenden, ist die Auswirkung je nach Gerätetyp leicht unterschiedlich. In der folgenden Tabelle finden Sie Beispiele für die Auswirkung von Richtlinien auf verschiedene Geräte.
  


|**Sicherheitsrichtlinie**|**Windows Phone 8.1 +**|**Android 4 und höher**|**Samsung Knox**|**IOS 6 +**|**Hinweise**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|Verschlüsselte Sicherung anfordern  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |IOS-verschlüsselte Sicherung erforderlich.  <br/> |
|Cloud-Sicherung blockieren  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |Google-Sicherung auf Android blockieren (abgeblendet), Cloud-Sicherung auf iOS.  <br/> |
|Dokumentsynchronisierung blockieren  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS: Dokumente in der Cloud blockieren.  <br/> |
|Fotosynchronisierung blockieren  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS (systemeigen): Fotodatenstrom blockieren.  <br/> |
|Screenshots blockieren  <br/> |✔  <br/> |X  <br/> |✔  <br/> |✔  <br/> |Bei Versuch blockiert.  <br/> |
|Videokonferenz blockieren  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |FaceTime unter iOS blockiert, nicht Skype oder andere.  <br/> |
|Senden von Diagnosedaten blockieren  <br/> |✖  <br/> |X  <br/> |✔  <br/> |✔  <br/> |Senden von Google-Absturzbericht unter Android blockieren  <br/> |
|Zugriff auf den App-Store blockieren  <br/> |✔  <br/> |X  <br/> |✔  <br/> |✔  <br/> |App-Store-Symbol fehlt auf Android-Startseite, ist deaktiviert unter Windows, fehlt unter iOS.  <br/> |
|Kennwort für den App-Store anfordern  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS: Kennwort für iTunes-Käufe erforderlich.  <br/> |
|Verbindung mit Wechselmedien blockieren  <br/> |✔  <br/> |X  <br/> |✔  <br/> |N/V  <br/> |Android: SD-Karte in Einstellungen abgeblendet, Windows benachrichtigt Benutzer, dort installierte Apps sind nicht verfügbar  <br/> |
|Bluetooth-Verbindung blockieren  <br/> |✔  <br/> |\*\*\*  <br/> |\*\*\*  <br/> |✖  <br/> |\*\*\*Es kann nicht als eine Einstellung für Android BlueTooth deaktivieren. Wir deaktivieren Sie stattdessen die Transaktionen, die BlueTooth erfordern: Advanced Audio Distribution, Audio/Video-Remotesteuerung, Geräte Headset, Kopfhörer, Telefonbuch Zugriff und seriellen Anschlusses. Eine kleine Toast-Meldung wird am unteren Rand der Seite angezeigt, wenn diese verwendet werden.  <br/> |
   
## <a name="what-happens-when-you-delete-a-policy-or-remove-a-user-from-the-policy"></a>Was geschieht beim Löschen einer Richtlinie oder beim Entfernen eines Benutzers aus der Richtlinie?

Wenn Sie eine Richtlinie löschen oder Entfernen eines Benutzers aus einer Gruppe, der die Richtlinie zu bereitgestellt wurde, können die Einstellungen für die Informationsverwaltungsrichtlinie, Office 365-e-Mail-Profil und Cache-e-Mails aus dem Gerät des Benutzers entfernt werden. Finden Sie in der folgenden Tabelle zu sehen, was für die verschiedenen Gerätetypen entfernt wird:
  
|**Was entfernt wird**|**Windows Phone 8.1 +**|**iOS 6 +**|**Android 4 + (einschließlich Samsung Knox)**|
|:-----|:-----|:-----|:-----|
|Verwaltete e-Mail-Profile\*  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|Richtlinieneinstellungen  <br/> |✔  <br/>           Mit Ausnahme von **Senden von Diagnosedaten vom Gerät aus blockieren**. <br/> |✔  <br/> |✖  <br/> |
   
> [!NOTE]
> \*Wenn die Richtlinie mit der Option bereitgestellt wurde **e-Mail-Profil wird verwaltet** ausgewählt haben, klicken Sie dann das verwaltete e-Mail-Profil und Cache-e-Mails, Profil aus dem Gerät des Benutzers gelöscht werden. 
  
Jeder Benutzer, die auf die entfernte Richtlinie angewendet wird die Richtlinie auf ihrem Gerät das nächste Mal, das Ihr mobile Gerät mit MDM für Office 365 überprüft, entfernt haben. Wenn Sie eine neue Richtlinie, die auf diese Benutzercomputern angewendet wird bereitstellen, werden sie aufgefordert, in MDM für Office 365 neu zu registrieren.
  
Sie können auch [ein Gerät](wipe-a-mobile-device.md), entweder vollständig, oder wählen Sie einzelne löschen Sie organisatorische Informationen aus dem Gerät.
  
## <a name="related-topics"></a>Verwandte Themen

[Übersicht der mobilen Geräteverwaltung für Office 365](overview-of-mdm.md)
  
[Funktionen der mobilen Geräteverwaltung für Office 365](capabilities-of-mobile-device-management.md)
  

