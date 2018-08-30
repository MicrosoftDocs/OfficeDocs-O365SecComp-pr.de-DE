---
title: Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung in Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Um IP-Adressen auf einfache Weise zu ermitteln, die Sie in Office 365 Cloud App-Sicherheit, wie Ihre physischen Büroraums IP-Adressen verwenden, können Sie Gruppen von IP-Adressbereiche einrichten.
ms.openlocfilehash: 76cb9625a46d1f5eceaab696de5dcbb72f4d2b47
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528872"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a>Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung in Office 365-Cloud-App-Sicherheit
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |[Starten Sie die Nutzung](utilization-activities-for-ocas.md) <br/> |
   
Um IP-Adressen auf einfache Weise zu ermitteln, die Sie in Office 365 Cloud App-Sicherheit, wie Ihre physischen Büroraums IP-Adressen verwenden, können Sie Gruppen von IP-Adressbereiche einrichten. Definieren diese Bereiche können markieren und kategorisiert werden können, und klicken Sie dann können Sie Tags und Kategorien auf anpassen, wie Ihre Aktivität Protokolle und Warnungen angezeigt und untersucht werden.
  
Jede Gruppe von IP-Adressbereichen kann markiert werden mit Tag-Namen, die Sie auswählen, und klicken Sie dann die Tags können kategorisiert werden basierend auf eine Standardliste von IP-Kategorien (beispielsweise Corporate, Administrative, Risky und VPN). Sowohl IPv4 als auch IPv6-Adressen werden unterstützt.
  
> [!NOTE]
> Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der Verfahren in diesem Artikel werden. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a>Einrichten eines IP-Adressbereichs in Office 365-Cloud-App-Sicherheit

1. Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.) 
    
2. In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.
    
    ![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Klicken Sie auf der rechten oberen Ecke der Seite, auf **Einstellungen** \> **IP-Adressbereiche**.
    
    ![Wählen Sie in Office 365-Cloud-App-Sicherheit Einstellungen für den Einstellungen für Ihr System und Zugriff auf](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)
  
5. Klicken Sie auf die Schaltfläche neu, die ein Pluszeichen (+) ähnelt ( **+**).
    
6. Geben Sie im Fenster **neuen IP-Adressbereich** die folgenden Werte ein: 
    
|**Webfeld- oder**|**Nächste Schritte**|
|:-----|:-----|
|**Name** <br/> |Verwenden Sie dieses Feld zum Verwalten von IP-Adressbereich und Einstellungen. (Dieser Wert in Aktivitäten Protokolle werden nicht angezeigt werden.)  <br/> |
|**IP-Adressbereiche** <br/> |Geben Sie einen Bereich, mithilfe der Netzwerk-Präfix-Notation (auch bekannt als CIDR-Notation). 192.168.1.0/27 umfasst beispielsweise den Wertebereich 192.168.1.0 bis 192.168.1.31 (einschließlich).  <br/> |
|**Speicherort** und den **Internetdienstanbieter registriert** <br/> |Geben Sie den Speicherort und den Internetdienstanbieter (ISP) für den IP-Adressbereich ein. Dies überschreibt für die Adressen definierten öffentlichen Felder die kann bei Fällen hilfreich sein, wie eine IP-Adresse ist, gilt als öffentlich in Irland, jedoch ist tatsächlich in den USA  <br/> |
|**Tags** <br/> |Verwenden Sie Tags zum Benennen von Ihren Gruppen von IP-Adressen. (Im Gegensatz zu Sie im Feld Name wird Tags in Aktivitätsprotokolle angezeigt.) Geben Sie ein Wort oder Ausdruck, die Sie für ein Tag verwenden möchten. Sie können beliebig viele Tags, wie Sie für jede IP-Adressbereich hinzufügen. Und wenn Sie bereits ein Tag eingerichtet haben, und Sie diese IP-Adressbereich hinzufügen möchten, wählen Sie ihn aus der Liste der aktuellen Tags, die angezeigt werden, wie Sie mit der Eingabe beginnen.  <br/> |
|**Kategorie** <br/> | Zuweisen von Kategorien zu Ihrer Kategorien zu erleichtern, Aktivitäten zu erkennen, die von bestimmten IP-Adressen stammen. Wählen Sie die folgenden Optionen aus:<br/> **Administrative** Alle IP-Adressen Ihrer Admins.  <br/> **Cloud-Anbieter** Die IP-Adresse Ihres Proxys in der Cloud.  <br/> **Im Unternehmen** Alle IP-Adressen in Ihrem internen Netzwerk, Ihren Zweigstellen und Ihre wechselnden Arbeitsplätzen Wi-Fi-Adressen.  <br/> **Riskant.** IP-Adressen, die Sie berücksichtigen riskant sein wie verdächtigen IP-Adressen in der Vergangenheit IP-Adressen in Ihrer Mitbewerber Netzwerken gesehen haben und so weiter. Standardmäßig enthält die Kategorien riskant zwei IP-Tags: **anonyme Proxy** und **Tor** <br/> **VPN** IP-Adressen, die Ihre Mitarbeiter remote verwenden.  <br/> |
   
7. Wählen Sie **Speichern**.
    
Lassen Sie nach dem Einrichten Ihrer IP-Adressbereiche, beachten Sie, dass diese Änderungen nur zukünftige Ereignisse betroffen sind.
  
## <a name="next-steps"></a>Nächste Schritte

- [Aktivität Richtlinien und Warnungen](activity-policies-and-alerts.md)
    
- [Anomalie Erkennungsrichtlinien](anomaly-detection-policies-in-ocas.md)
    
- [Integrieren von Ihrem Server SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Lesen Sie und führen Sie einer Aktion Warnungen in Office 365-Cloud-App-Sicherheit aus](review-office-365-cas-alerts.md)
    

