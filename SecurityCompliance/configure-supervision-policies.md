---
title: Konfigurieren von Richtlinien für Ihre Organisation Überwachung
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
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
ms.openlocfilehash: a919d65f5c0967a44ac12b7e02d477dac2113704
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530128"
---
# <a name="configure-supervision-policies-for-your-organization"></a>Konfigurieren von Richtlinien für Ihre Organisation Überwachung

Verwenden Sie aufsichtsrichtlinien Kommunikation der Mitarbeiter zur Prüfung durch interne oder externe Prüfer erfasst.
  
> [!NOTE]
> Verwenden aufsichtsrichtlinien erfordert ein Abonnement von Office 365 E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und Überwachung ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Führen Sie diese Schritte zum Einrichten und Verwenden der Überwachung in Office 365-Organisation aus: 
  
- [Einrichten von Gruppen für die Überwachung](configure-supervision-policies.md#exampledist)
    
    Bevor Sie mit der Überwachung beginnen, bestimmen Sie, wer werden haben ihre Kommunikation überprüft und führt, die diese Bewertungen. Wenn Sie mit nur wenigen Benutzern finden Sie unter Funktionsweise der Überwachung beginnen möchten, können Sie Gruppen für jetzt einrichten überspringen.
    
- [Überwachung in Ihrer Organisation zur Verfügung zu stellen](configure-supervision-policies.md#SRavailable)
    
    Fügen Sie sich selbst der Rollengruppe generelle überprüfen, damit Sie Richtlinien einrichten können. Jeder Benutzer, der diese Rolle zugewiesen wurde kann auf die Seite **Überwachung** unter **Steuerung der Daten** in das Wertpapier zugreifen &amp; Compliance Center. 
    
- [Richten Sie eine Richtlinie für Überwachung](configure-supervision-policies.md#setupsuper)
    
    Erstellen Sie in das Wertpapier aufsichtsrichtlinien &amp; Compliance Center. Diese Richtlinien definieren, welche Communications Review in Ihrer Organisation unterliegen, und gibt an, die überprüft werden soll. Kommunikationskomponenten umfassen e-Mail als auch 3rd Party Plattform Communications (z. B. Facebook, Twitter.)
    
- [Verwenden Sie Outlook Web app, um Communications identifiziert durch eine Richtlinie für die Überwachung zu prüfen](configure-supervision-policies.md#UseOutlook)
    
    Die Add-in-Überwachung ermöglicht Bearbeiter den Zugriff auf die Überwachung Funktionalität in Outlook Web app rechten bewerten und kategorisieren jedes Element. Unterstützung für die desktop-Version von Outlook wird in Kürze bereitgestellt.
    
- **Führen Sie den Bericht für die Überwachung**
    
    Verwenden Sie die Überwachung Berichte, um die Überprüfung Aktivität Ebene der Richtlinie und Bearbeiter finden Sie unter. Für jede Richtlinie können Sie auch live Statistiken auf den aktuellen Status der Überprüfung Aktivität anzeigen. Weitere Informationen hierzu finden Sie unter [Überwachung Berichte](supervision-reports.md).
    
## <a name="set-up-groups-for-supervision"></a>Einrichten von Gruppen für die Überwachung
<a name="exampledist"> </a>

 Wenn Sie eine Richtlinie für Überwachung erstellen, ermitteln Sie, ihre Kommunikation überprüft besitzen und wem diese Bewertungen ausgeführt werden soll. E-Mail-Adressen verwenden Sie in der Richtlinie um Personen oder Gruppen von Personen zu identifizieren. Um das Setup zu vereinfachen, Erstellen von Gruppen für Personen, die ihre Kommunikation überprüft haben, werden und Gruppen für Personen, die diese Kommunikation überprüft werden. Wenn Sie Gruppen verwenden, können Sie mehrere benötigen – beispielsweise, wenn Sie die Kommunikation zwischen zwei unterschiedlichen Gruppen von Personen überwachen möchten, oder wenn Sie möchten, um eine Gruppe anzugeben, die überwacht werden und sollte nicht zur Verfügung. Einzelheiten zur Funktionsweise finden Sie unter [Beispiel Verteilergruppen](configure-supervision-policies.md#GroupExample) . 
  
Um die Kommunikation zwischen oder in Gruppen in Ihrer Organisation zu überwachen, Einrichten von Verteilergruppen in der Exchange-Verwaltungskonsole (Wechseln Sie zu **Empfänger** \> **Gruppen**). Weitere Informationen zum Einrichten von Verteilergruppen finden Sie unter [Verwalten von Verteilergruppen](http://go.microsoft.com/fwlink/?LinkId=613635)
  
> [!NOTE]
> Sie können auch dynamische Verteilergruppen oder Sicherheitsgruppen für Überwachung Falls gewünscht. Um besser entscheiden, ob diese besser Ihrer Organisation passen müssen, finden Sie in [Verwalten von e-Mail-aktivierten Sicherheitsgruppen](http://go.microsoft.com/fwlink/?LinkId=627033)und [dynamische Verteilergruppen verwalten](http://go.microsoft.com/fwlink/?LinkId=627058). 
  
### <a name="example-distribution-groups"></a>Beispielverteilergruppen
<a name="GroupExample"> </a>

Dieses Beispiel enthält eine Verteilergruppe, die für eine finanzielle Organisation mit dem Namen "Contoso" finanzielle International eingerichtet wurde. 
  
Im Unternehmen Contoso Financial International muss eine Stichprobe der Kommunikationen zwischen Brokern in den Vereinigten Staaten beaufsichtigt werden. Für die Compliance Officer in dieser Gruppe ist jedoch keine Aufsicht erforderlich. Für dieses Beispiel können wir die folgenden Gruppen erstellen:
  
|**Einrichten dieser Verteilergruppe**|**Gruppenadresse (Alias)**|**Beschreibung**|
|:-----|:-----|:-----|
|Alle US-Broker  <br/> |US_Brokers@contoso.com  <br/> |Diese Gruppe umfasst E-Mail-Adressen für alle US-basierten Broker, die für Contoso arbeiten.  <br/> |
|Alle Compliance Officer für die Vereinigten Staaten  <br/> |US_Compliance@contoso.com  <br/> |Diese Gruppe werden e-Mail-Adressen für alle US-basierte Compliance Officer, die für Contoso arbeiten enthält. Da dieser Gruppe eine Teilmenge der alle US-basierte Broker ist, können Sie diesen Alias, ausgenommen Compliance Officer von einer Richtlinie für Überwachung verwenden.  <br/> |
   
Im Abschnitt [Richten Sie eine Richtlinie für Überwachung](configure-supervision-policies.md#setupsuper) wird beschrieben, wie Sie diese Gruppen verwenden können, wenn Sie die Richtlinie zu konfigurieren. 
  
## <a name="make-supervision-available-in-your-organization"></a>Überwachung in Ihrer Organisation zur Verfügung zu stellen
<a name="SRavailable"> </a>

**Überwachung** in das Wertpapier als Menüoption verfügbar machen &amp; Compliance Center, Sie müssen zugewiesen werden die generelle Administratorrolle überprüfen. 
  
Zu diesem Zweck können sich selbst als Mitglied der Rollengruppe generelle Überprüfung entweder hinzufügen oder Sie können eine neue Rollengruppe erstellen.
  
### <a name="add-members-to-the-supervisory-review-role-group"></a>Hinzufügen von Mitgliedern der Rollengruppe generelle überprüfen

1. Melden Sie sich bei [https://protection.office.com](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. In das Wertpapier &amp; Compliance Center, **Berechtigungen**zu wechseln.
    
3. Wählen Sie aus der Rollengruppe **Generelle Überprüfung** , und klicken Sie dann auf das Symbol bearbeiten. 
    
4. Fügen Sie im Abschnitt **Mitglieder** die Personen, die Überwachung für Ihre Organisation verwalten soll. 
    
### <a name="create-a-new-role-group"></a>Erstellen einer neuen Rollengruppe

1. Melden Sie sich bei [https://protection.office.com](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. In das Wertpapier &amp; Compliance Center, gehen Sie zu **Berechtigungen** , und klicken Sie dann auf Hinzufügen ( **+**).
    
3. Klicken Sie auf Hinzufügen, klicken Sie im Abschnitt **Rollen** ( **+**) und führen Sie einen Bildlauf nach unten zu **Generelle Überprüfung-Administrator**. Fügen Sie diese Rolle der Rollengruppe.
    
4. Fügen Sie im Abschnitt **Mitglieder** die Personen, die Überwachung für Ihre Organisation verwalten soll. 
    
Weitere Informationen zu Rollengruppen und Berechtigungen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center ](permissions-in-the-security-and-compliance-center.md).
  
## <a name="set-up-a-supervision-policy"></a>Richten Sie eine Richtlinie für Überwachung
<a name="setupsuper"> </a>

> [!IMPORTANT]
> Vor dem Erstellen einer Richtlinie für Überwachung, müssen Sie zuerst alle vorhandenen generelle Überprüfung Richtlinien entfernen. 
  
1. Melden Sie sich bei [https://protection.office.com](https://protection.office.com) Verwendung von Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Steuerung der Daten** klicken Sie auf \> **Überwachung**.
    
    > [!NOTE]
    > Die vorherige Version des Features möglicherweise in der linken Navigationsleiste als **generelle überprüfen (Abschließen bald)** angezeigt. Diese Version wird bald veraltet und entfernt werden. Die neue Version **Aufsicht** aufgerufen wird seine stattfinden. 
  
3. Klicken Sie auf **Erstellen** , und führen Sie dann den Assistenten zum Einrichten von der folgenden Seiten der Richtlinie. 
    
### <a name="policy-name-and-description"></a>Name und Beschreibung der Richtlinie

Geben Sie einen Namen und eine Beschreibung für die Richtlinie ein. Zu Beispielzwecken werden wir die Richtlinie "Contoso" uns Broker benennen.
  
### <a name="choose-users-to-supervise"></a>Wählen Sie Benutzer zur Überwachung

- Wählen Sie im Feld **Supervise diese Benutzer oder Gruppen** die Benutzer oder Gruppen, deren Kommunikation überwachen möchten. Das Festhalten mit unserem Beispiel für Contoso uns Broker, später wir die Gruppe US_Brokers@Contoso.com hier auswählen. 
    
- Wenn Sie eine Gruppe zur Überwachung ausgewählt haben, können Sie das **diese Benutzer ausschließen** , Mitglieder der Gruppe auswählen, die von der Überwachung ausgenommen sind. Im Beispiel werden wir die Gruppe US_Compliance@Contoso.com hier ausschließen. 
    
### <a name="choose-communications-to-review"></a>Wählen Sie Communications überprüfen
<a name="CommsToReview"> </a>

Standardmäßig wird die Bedingung **Richtung ist** wird angezeigt und kann nicht entfernt werden. Wenn Sie die Überprüfung (wie die Überprüfung von Inhalten, die bestimmte Wörter oder Ausdrücke enthält nur) Bereich möchten, klicken Sie auf **Bedingung hinzufügen**. Sie können mehrere Bedingungen angeben, falls erforderlich.
  
Die gewählte Bedingungen werden für die Kommunikation von e-Mails und 3rd Party Quellen in Ihrer Organisation (wie von Facebook oder Ablage) gelten. Ausführliche Informationen zum Importieren von Drittanbietern 3rd Communications in Office 365-Organisation finden Sie unter [Archivierung Drittanbieter - Daten in Office 365](https://technet.microsoft.com/EN-US/library/mt621583.aspx).
  
Die folgende Tabelle erläutert mehr zu jeder Bedingung.
  
|Zum Auswählen einer Option drücken Sie die EINGABETASTE.|**Verwendung**|
|:-----|:-----|
|Richtung ist  <br/> |Wählen Sie **eingehende** Kommunikation zu überprüfen, die **an** gesendet werden die Personen, die Sie ausgewählt, zur Überwachung **von** Personen haben in der Richtlinie nicht enthalten.  <br/> Wählen Sie **ausgehend** aus, wenn die zu überprüfenden Communications, die die Personen, die Sie ausgewählt, zur Überwachung haben **von** gesendete ** auf ** Personen, die nicht in der Richtlinie enthalten.  <br/> Wählen Sie **intern** , um zu prüfen, die gesendet werden, **zwischen** Personen, die Sie angegeben haben, in der Richtlinie.  <br/> |
|Nachricht enthält eines dieser Wörter  <br/> Nachricht enthält keine der folgenden Wörter  <br/> |Geben Sie zum Anwenden der Richtlinie, wenn bestimmte Wörter oder Ausdrücke ein- oder ausgeschlossen werden in einer Nachricht, einzelnen Wörter oder Ausdrücke in einer separaten Zeile ein. Jede Zeile der eingegebenen Wörter separat angewendet werden (nur eine der folgenden Zeilen muss für die Richtlinie angewendet, die der Nachricht angewendet). Weitere Informationen zum Eingeben von Wörtern oder Begriffen finden Sie im nächsten Abschnitt [übereinstimmende Wörter und Ausdrücke zum-e-Mails oder Anhänge](configure-supervision-policies.md#Matchwords).<br/> |
|Anlage enthält eines dieser Wörter  <br/> Anlage enthält keine der folgenden Wörter  <br/> |Um die Richtlinie anwenden, wenn bestimmte Wörter oder Ausdrücke ein- oder ausgeschlossen werden in e-Mail-Anlagen (beispielsweise ein Word-Dokument), geben Sie jedes Wort oder Ausdruck in einer separaten Zeile ein. Jede Zeile der eingegebenen Wörter separat angewendet werden (nur eine Zeile gilt für die Richtlinie auf die Anlage angewendet). Weitere Informationen zum Eingeben von Wörtern oder Begriffen finden Sie im nächsten Abschnitt [übereinstimmende Wörter und Ausdrücke zum-e-Mails oder Anhänge](configure-supervision-policies.md#Matchwords).<br/> |
|Anlage ist eine der folgenden Dateitypen  <br/> Anlage ist keiner dieser Dateitypen  <br/> |Um eine Kommunikation überwachen, die ein- oder ausschließen bestimmte Typen von Anlagen an, geben Sie die Dateierweiterungen (wie .exe oder PDF). Wenn Sie ein- oder Ausschließen von mehreren Dateierweiterungen möchten, geben Sie diese in separaten Zeilen. Nur eine Anlage-Erweiterung muss für die Richtlinie angewendet übereinstimmen.  <br/> |
|Nachricht ist größer als  <br/> Nachrichtengröße ist nicht größer als  <br/> |Verwenden Sie diese Bedingungen-Mails basierend auf eine bestimmte Größe um zu überprüfen, um die maximale oder minimale Größe anzugeben, die eine Nachricht werden kann, bevor es überprüft wird. Beispielsweise, wenn Sie die **Nachrichtengröße ist größer als** angeben \> **1.0 MB**, alle Nachrichten, die 1.01 MB und größere wird sind hin überprüft werden. Sie können Bytes, KB, MB oder GB für diese Bedingung auswählen.<br/> |
|Anlage ist größer als  <br/> Anlage ist nicht größer als  <br/> |Um Nachrichten basierend auf deren Anlagengröße zu überprüfen, geben Sie die maximale oder minimale Größe einer Anlage kann sein, bevor Sie die Nachricht und ihre Anhänge unterliegen überprüfen. Wenn Sie die **Anlage ist größer als** angeben beispielsweise \> **2.0 MB**, alle Nachrichten mit Anlagen 2.01 MB und Failover wird überprüft. Sie können Bytes, KB, MB oder GB für diese Bedingung auswählen.<br/> |
   
#### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Übereinstimmende Wörter und Ausdrücke in E-Mails oder Anlagen
<a name="Matchwords"> </a>

Jede Zeile der eingegebenen Wörter separat angewendet werden (nur eine Zeile muss für die Richtlinie Bedingung auf das e-Mail- oder Anlage anwenden anwenden). Verwenden Sie die Bedingung, die **Nachricht enthält eines dieser Wörter**, mit den Schlüsselwörtern "Banker" und "Insider-Geschäften" beispielsweise fangen wir an in separaten Zeilen. Die Richtlinie gilt für alle Nachrichten, die das Wort "Banker" oder der Ausdruck "Insider-Geschäften" enthält. Nur eine der folgenden Wörter oder Ausdrücke muss für diese Richtlinie Bedingung anwenden auftreten. Wörter in die Nachricht oder Anlage müssen exakt übereinstimmen, was Sie eingeben.
  
#### <a name="entering-multiple-conditions"></a>Eingeben mehrerer Bedingungen
<a name="Matchwords"> </a>

Wenn Sie mehrere Bedingungen eingeben, verwendet Office 365 aller Bedingungen um zu bestimmen, wann die Richtlinie auf Kommunikationselemente anwenden zusammen. Wenn Sie mehrere Bedingungen eingerichtet haben, müssen sie alle für die Richtlinie angewendet wurde, erfüllt sein, wenn Sie eine Ausnahme eingeben. Nehmen wir beispielsweise an, dass Sie eine Richtlinie erstellen, die angewendet werden soll, wenn eine Nachricht das Wort "Handel enthält" und größer als 2 MB ist müssen. Wenn die Nachricht auch die Wörter "Von Contoso finanzielle genehmigt enthält" sollten jedoch die Richtlinie nicht angewendet. In diesem Fall würde die drei Bedingungen folglich wie folgt lauten: 
  
- **Nachricht enthält eines dieser Wörter**, mit den Schlüsselwörtern "Handel"
    
- **Nachrichtengröße ist größer als**, mit dem Wert von 2 MB
    
- **Nachricht enthält keine der folgenden Wörter**, mit den Schlüsselwörtern "Contoso finanzielle Teams genehmigt".
    
### <a name="specify-percentage-to-review"></a>Geben Sie Prozentsatz überprüfen
<a name="CommsToReview"> </a>

Wenn Sie die Menge des Inhalts, um zu prüfen reduzieren möchten, geben Sie einen Prozentsatz. Wir werden nach dem Zufallsprinzip, Umfang des Inhalts von der Summe auswählen, die die Bedingungen entspricht, den, die Sie ausgewählt haben. Wenn Sie Bearbeiter alle Elemente überprüfen möchten, geben Sie **100 %**.
  
### <a name="choose-reviewers"></a>Wählen Sie Bearbeiter
<a name="CommsToReview"> </a>

Die Benutzer und Gruppen gewählte verwenden die Überwachung app in Outlook Web app die Kommunikation untersuchen, die durch diese Richtlinie zurückgegeben werden. Sie können e-Mail-Adressen für interne oder externe Bearbeiter einschließen. 
  
### <a name="review-your-settings"></a>Überprüfen Sie die Einstellungen
<a name="CommsToReview"> </a>

Nachdem Sie alle Abschnitte der aufsichtsrichtlinie abgeschlossen haben, überprüfen Sie die Einstellungen, und klicken Sie dann auf **Fertig stellen** , um die Richtlinie zu speichern. Es kann einige Stunden für die Richtlinie so startet das Sammeln von Communications dauern. Überwachung bietet die gesamte Kommunikation zur Überprüfung in einen freigegebenen Ordner, den Bearbeiter in Outlook Web app zugreifen können. 
  
## <a name="use-outlook-web-app-to-review-communications-identified-by-a-supervision-policy"></a>Verwenden Sie Outlook Web app, um Communications identifiziert durch eine Richtlinie für die Überwachung zu prüfen
<a name="UseOutlook"> </a>

Bearbeiter werden das Aufsicht-add-in für Outlook Web app verwenden, um Communications prüfen. Das Add-In wird automatisch in Outlook Web app für alle Bearbeiter installiert, die Sie in der Richtlinie angegeben. Unterstützung für die desktop-Version von Outlook wird in Kürze bereitgestellt.
  
 **Überprüfen der Kommunikation in Outlook Web app**
  
1. Erweitern Sie in Outlook Web app, die **Aufsicht - \<Richtlinienname\> ** Ordner. 
    
2. In der ** \<Richtlinienname\> ** Unterordner, siehe Bearbeiter die gesamte Kommunikation, die durch diese aufsichtsrichtlinie identifiziert. 
    
    ![Überwachung-add-Ins in Outlook Web app mit der Überwachung Richtlinie Unterordner ausgewählt](media/eef329bf-2bd0-477e-a715-76ca19b3347f.jpg)
  
3. Öffnen Sie ein Element aus, um zu überprüfen, und klicken Sie auf die Add-in- **Überwachung** . 
    
4. Verwenden Sie das Add-in, um das Element als **konform**, **Nicht konform**, **Questionable,** oder **gelöst**klassifizieren. Nachdem Sie ein Element klassifiziert haben, wird es auf den entsprechenden Unterordner verschoben werden die ** \<Richtlinienname\> ** Ordner. 
    

