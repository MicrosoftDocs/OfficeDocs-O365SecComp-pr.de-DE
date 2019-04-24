---
title: Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Um Gruppen von IP-Adressen, die Sie in Office 365 Cloud App Security verwenden, wie etwa ihre physischen Office-IP-Adressen, leicht zu identifizieren, können Sie IP-Adressbereiche einrichten.
ms.openlocfilehash: b8f5c1dd46b2e3990d53a65881d12ca8f3961b16
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254858"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a>Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung in Office 365 Cloud App Security
  
|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |[Verwendung beginnen](utilization-activities-for-ocas.md) <br/> |
   
Um Gruppen von IP-Adressen, die Sie in Office 365 Cloud App Security verwenden, wie etwa ihre physischen Office-IP-Adressen, leicht zu identifizieren, können Sie IP-Adressbereiche einrichten. Wenn Sie diese Bereiche definieren, können Sie Sie markieren und kategorisieren und dann mithilfe von Tags und Kategorien anpassen, wie Ihre Aktivitätsprotokolle und Warnungen angezeigt und untersucht werden.
  
Jede Gruppe von IP-Bereichen kann mit Tagnamen gekennzeichnet werden, die Sie auswählen, und dann können die Tags basierend auf einer Standardliste mit IP-Kategorien kategorisiert werden (beispielsweise unterNehmens-, Verwaltungs-, Risikoy-und VPN-Verbindungen). Sowohl IPv4-als auch IPv6-Adressen werden unterstützt.
  
> [!NOTE]
> Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die Verfahren in diesem Artikel ausführen zu können. Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a>So richten Sie einen IP-Adressraum in Office 365 Cloud App Security ein

1. Wechseln Sie als globaler Administrator oder Sicherheitsadministrator zum Sicherheitsportal der Cloud-app ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.
    
2. Klicken Sie oben rechts auf der Seite auf **Einstellungen** \> für **IP-Adressbereiche**.<br>![Wählen Sie in O365 Cloud App Security die Option Einstellungen für den Zugriff auf Ihre System-und Daten Einstellungen aus.](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)<br>
  
3. Klicken Sie auf die Schaltfläche neu, die einem Pluszeichen **+** ähnelt ().
    
4. Geben Sie im Fenster **neuer IP-Adressbereiche** die folgenden Werte an: 
    
|**Feld oder Liste**|**Nächste Schritte**|
|:-----|:-----|
|**Name** <br/> |Verwenden Sie dieses Feld, um den IP-Adressbereich und die Einstellungen zu verwalten. (Dieser Wert wird in Aktivitätsprotokollen nicht angezeigt.)  <br/> |
|**IP-Adressbereiche** <br/> |Geben Sie einen Range mit der Netzwerkpräfix Notation (auch bekannt als CIDR-Notation) an. Beispielsweise enthält 192.168.1.0/27 den Werte 192.168.1.0 bis 192.168.1.31 (einschließlich).  <br/> |
|**Speicherort** und **registrierter ISP** <br/> |Angeben des Standorts und des InternetdienstAnbieters für den IP-Adressbereich. Dadurch werden die für die Adressen definierten öffentlichen Felder außer Kraft gesetzt, was für Fälle hilfreich ist, beispielsweise für eine IP-Adresse, die als öffentlich in Irland angesehen wird, aber tatsächlich in den USA ist.  <br/> |
|**Tags** <br/> |Verwenden Sie Tags, um Ihre Gruppen von IP-Adressen zu benennen. (Im Gegensatz zum Feld Name werden Tags in Aktivitätsprotokollen angezeigt.) Geben Sie ein Wort oder einen Ausdruck ein, der für ein Tag verwendet werden soll. Sie können für jeden IP-Adress Kreis beliebig viele Tags hinzufügen. Wenn Sie bereits ein Tag eingerichtet haben und diesen IP-Adress Kreis hinzufügen möchten, wählen Sie ihn aus der Liste der aktuellen Tags aus, die angezeigt werden, wenn Sie mit der Eingabe beginnen.  <br/> |
|**Kategorie** <br/> | Zuweisen von Kategorien zu ihren Tags, um die Erkennung von Aktivitäten, die aus bestimmten IP-Adressen stammen, zu erleichtern. Wählen Sie aus den folgenden Optionen aus:  <br/> **Administrative** Alle IP-Adressen Ihrer Administratoren.  <br/> **Cloud-Anbieter** Die IP-Adresse des Proxys in der Cloud.  <br/> Unter **nehmen** Alle IP-Adressen in Ihrem internen Netzwerk, ihren Zweigstellen und Ihre WLAN-Roaming-Adressen.  <br/> **Riskant** Alle IP-Adressen, die Sie als riskant betrachten, wie etwa verdächtige IP-Adressen, die Sie in der Vergangenheit gesehen haben, IP-Adressen in den Netzwerken Ihrer Mitbewerber usw. Standardmäßig enthält die Risikokategorien zwei IP-Tags: **Anonymer Proxy** und **Tor** <br/> **VPN** Alle IP-Adressen, die von den Remote Arbeitskräften verwendet werden.  <br/> |
   
7. Wählen Sie **Speichern** aus.
    
Beachten Sie nach der Einrichtung Ihrer IP-Adressbereiche, dass nur zukünftige Ereignisse von diesen Änderungen betroffen sind.
  
## <a name="next-steps"></a>Nächste Schritte

- [Aktivitätsrichtlinien und Warnungen](activity-policies-and-alerts.md)
    
- [Erkennungsrichtlinien für Anomalien](anomaly-detection-policies-in-ocas.md)
    
- [Integrieren Ihres SIEM-Servers](integrate-your-siem-server-with-office-365-cas.md)
    
- [Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security](review-office-365-cas-alerts.md)
    

