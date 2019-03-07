---
title: Erstellen einer gesetzlichen Aufbewahrungspflicht
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: acfa0c635b361426542e91a55c8d75c315bfb831
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455197"
---
# <a name="create-a-legal-hold-notice"></a>Erstellen einer gesetzlichen Aufbewahrungspflicht

Mithilfe der Advanced eDiscovery (Preview)-Depot Kommunikation können Organisationen ihren Workflow für die Kommunikation mit Depotbank verwalten. Mithilfe des Kommunikationstools können juristische Teams die Benachrichtigungen über zugelassene Warteschleife systematisch senden, sammeln und nachverfolgen. Der Prozess der flexiblen Erstellung ermöglicht es Teams auch, den Workflow für die Aufbewahrungs Benachrichtigung und den Inhalt der an die Verwalter gesendeten Benachrichtigungen anzupassen. 

![Seite "Kommunikation"](../media/CommunicationPage.PNG)

In diesem Artikel werden die Schritte im Workflow zum Anhalten von Benachrichtigungen erläutert.

## <a name="step-1-specify-communication-details"></a>Schritt 1: Angeben von Kommunikationsdetails

Der erste Schritt besteht darin, die entsprechenden Details für rechtliche Aufbewahrungs Hinweise oder andere Depot Kommunikationen anzugeben. 

![Name Communication page](../media/NameCommunication.PNG)

1. Wechseln Sie im Security & Compliance Center zu **eDiscovery _GT_ Advanced eDiscovery (Preview)** , um die Liste der Fälle in Ihrer Organisation anzuzeigen.
   
2. Klicken Sie auf die Registerkarte **Kommunikation** , und klicken Sie dann auf **neue Kommunikation**.
   
3. Geben Sie auf der Seite **Name Communication** die folgenden (erforderlichen) Kommunikationsdetails an.

    - **Name**: Dies ist der Name für die Kommunikation.
    
    - AusStell ender **Offizier**: in der Dropdownliste wird eine Liste mit den Fall Mitgliedern angezeigt. Jeder Hinweis, der an Verwalter gesendet wird, wird im Auftrag des angegebenen ausstellenden beauftragten gesendet.

4. Klicken Sie zum Senden von Kopien der Migrationsberichte an andere Benutzer unten auf der Seite auf **Durchsuchen**.

## <a name="step-2-define-the-portal-content"></a>Schritt 2: Definieren des Portalinhalts

Als nächstes können Sie den Inhalt des Notiz Speichers erstellen und hinzufügen. Geben Sie auf der Seite **Portalinhalt definieren** im Assistenten zum **Erstellen** von Kommunikationen den Inhalt des Notiz Speichers an. Dieser Inhalt wird automatisch den Benachrichtigungen zu Ausstellung, erneuter Ausstellung, Erinnerung und Eskalation angefügt. Darüber hinaus werden diese Inhalte im Compliance-Portal des Depotbank angezeigt. 

![Portal Inhaltsseite](../media/PortalContent.PNG)

So erstellen Sie den Portalinhalt:

1. Geben Sie (oder Ausschneiden und Einfügen aus einem anderen Dokument) ihren Haltestatus im TextBox-Element für den Portalinhalt ein. 

2. Fügen Sie Merge-Variablen in Ihre Nachricht ein, um den Hinweis anzupassen und das Depotschutz-Portal zu teilen.

3. Klicken Sie zum Senden von Kopien der Migrationsberichte an andere Benutzer unten auf der Seite auf **Durchsuchen**.

  >[!Tip]
  >Weitere Informationen dazu, wie Sie den Inhalt und das Format des Portalinhalts anpassen können, finden Sie unter [use the Communications Editor](using-communications-editor.md).

## <a name="step-3-set-the-required-notifications"></a>Schritt 3: Festlegen der erforderlichen Benachrichtigungen

Nachdem Sie den Inhalt des Haltestatus festgelegt haben, können Sie die Workflows zum Senden und Verwalten des Benachrichtigungsprozesses einrichten. Benachrichtigungen sind e-Mail-Nachrichten, die zur Benachrichtigung und Nachverfolgung mit Depotbank gesendet werden. Jeder Verwalter, der der Kommunikation hinzugefügt wird, erhält dieselbe Benachrichtigung. 

Zum Einrichten und Senden einer Aufbewahrungs Benachrichtigung müssen Sie Veröffentlichungs-, erneute Veröffentlichungs-und Versions Benachrichtigungen enthalten.

### <a name="issuance-notification"></a>Veröffentlichungs Benachrichtigung 

Nachdem die Kommunikation erstellt wurde, wird die **Veröffentlichungs Benachrichtigung** vom angegebenen ausstellenden Offizier initiiert. Die Veröffentlichungs Benachrichtigung ist die erste Nachricht, die an die Depotbank gesendet wurde, um Sie über Ihre Aufbewahrungspflichten zu informieren. 

So erstellen Sie eine Veröffentlichungs Benachrichtigung

1. Klicken Sie in der **Ausstellungs** Kachel auf **Bearbeiten**.
   
2. Fügen Sie gegebenenfalls zusätzliche Fall Mitglieder oder Mitarbeiter zu den Feldern **CC** und **Bcc** hinzu. Wenn Sie diesen Feldern mehrere Benutzer hinzufügen möchten, trennen Sie die e-Mail-Adressen durch ein Semikolon.
   
3. Geben Sie den **Betreff** für den Hinweis an (erforderlich).
   
4. Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich). Beachten Sie, dass der in Schritt 2 definierte Portalinhalt am Ende der Veröffentlichungs Benachrichtigung hinzugefügt wird. 
   
5. Klicken Sie auf **Speichern**. 

### <a name="re-issuance-notification"></a>Erneute Veröffentlichungs Benachrichtigung 

Bei Fortschreiten des Falls sind möglicherweise depotbanks erforderlich, um zusätzliche oder geringere Daten beizubehalten, als Sie zuvor angewiesen wurden. Nach dem Aktualisieren des Inhalts des Notiz Speichers wird die Benachrichtigung der Verwalter zu den Änderungen an den Aufbewahrungspflichten von der erneuten Ausstellung benachrichtigt.

So erstellen Sie eine erneute Veröffentlichungs Benachrichtigung: 

1. Klicken Sie in der Kachel erneut **herausstellen** auf **Bearbeiten**.
   
2. Fügen Sie gegebenenfalls zusätzliche Fall Mitglieder oder Mitarbeiter zu den Feldern **CC** und **Bcc** hinzu. Wenn Sie diesen Feldern mehrere Benutzer hinzufügen möchten, trennen Sie die e-Mail-Adressen durch ein Semikolon.
   
3. Geben Sie den **Betreff** für den Hinweis an (erforderlich).
   
4. Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich). Beachten Sie, dass der in Schritt 2 definierte Portalinhalt am Ende der erneuten Veröffentlichungs Benachrichtigung hinzugefügt wird.
   
5. Klicken Sie auf **Speichern**.

>[!Note]
>Wenn eine Hold-Benachrichtigung geändert wird, wird die erneute Veröffentlichungs Benachrichtigung automatisch an alle Verwalter gesendet, die der Nachricht zugewiesen sind. Nachdem die Benachrichtigung gesendet wurde, werden die Verwalter aufgefordert, ihren Haltestatus erneut anzuerkennen. Wenn Sie Mahn-oder Eskalations Workflows eingerichtet haben, werden diese ebenfalls neu gestartet. 

### <a name="release-notification"></a>Versions Benachrichtigung

Nachdem eine Angelegenheit aufgelöst wurde oder ein depotverwalter nicht mehr Inhalte aufbewahrt, können Sie die Depotbank aus einem Fall freigeben. Wenn der Depotbank zuvor eine Hold-Benachrichtigung ausgegeben wurde, kann die Freigabemeldung verwendet werden, um Verwalter zu warnen, dass Sie von ihrer Verpflichtung befreit wurden.

So erstellen Sie eine Versions Benachrichtigung 

1. Klicken Sie auf der **Freigabe** Kachel auf **Bearbeiten**.
   
2. Fügen Sie gegebenenfalls zusätzliche Fall Mitglieder oder Mitarbeiter zu den Feldern **CC** und **Bcc** hinzu. Wenn Sie diesen Feldern mehrere Benutzer hinzufügen möchten, trennen Sie die e-Mail-Adressen durch ein Semikolon.
   
3. Geben Sie den **Betreff** für den Hinweis an (erforderlich).
   
4. Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich).
   
5. Klicken Sie auf **Speichern** , und fahren Sie mit dem nächsten Schritt fort. 

## <a name="optional-step-4-set-the-optional-notifications"></a>Optional Schritt 4: Festlegen der optionalen Benachrichtigungen

Optional können Sie den Workflow für die Weiterleitung mit nicht reagierenden Verwalter vereinfachen, indem Sie automatisierte Mahn-und Eskalations Benachrichtigungen erstellen und planen.

![Seite zur Erinnerung/Eskalation](../media/ReminderEscalations.PNG)

### <a name="reminders"></a>Reminders

Nachdem Sie eine Aufbewahrungs Benachrichtigung gesendet haben, können Sie nicht reagierende Verwalter durch Definieren eines Erinnerungs Workflows nachverfolgen. 

So planen Sie Erinnerungen:

1. Klicken Sie in der Kachel **Erinnerung** auf **Bearbeiten**.
   
2. Aktivieren Sie den **Erinnerungs** Workflow, indem Sie die **Status** Umschalttaste (erforderlich) einschalten.
   
3. Angeben des **Intervalls für die Erinnerung (in Tagen)** (erforderlich). Dies ist die Anzahl der Tage, die gewartet werden muss, bevor die ersten und nach Verfolgungs Benachrichtigungen gesendet werden. Wenn Sie beispielsweise das Erinnerungsintervall auf 7 Tage festlegen, wird die erste Erinnerung 7 Tage nach der anfänglichen Benachrichtigung der Warteschlange gesendet. Alle nachfolgenden Erinnerungen würden auch alle 7 Tage gesendet.
   
4. Geben Sie die **Anzahl der Erinnerungen** an (erforderlich). Dieses Feld gibt an, wie viele Erinnerungen an nicht reagierende Verwalter gesendet werden. Wenn Sie beispielsweise die Anzahl der Erinnerungen auf 3 festlegen, erhält ein Verwalter maximal 3 Erinnerungen. Nachdem ein depotverwalter die Hold-Benachrichtigung bestätigt hat, werden Erinnerungen an diesen Benutzer nicht mehr gesendet.
   
5. Geben Sie den **Betreff** für den Hinweis an (erforderlich). 
   
6. Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich). Beachten Sie, dass der in Schritt 2 definierte Portalinhalt am Ende der Mahnungsbenachrichtigung hinzugefügt wird.
   
7. Klicken Sie auf **Speichern** , und fahren Sie mit dem nächsten Schritt fort.

### <a name="escalations"></a>Eskalationen 

In einigen Situationen benötigen Sie möglicherweise zusätzliche Möglichkeiten zum Nachverfolgen mit nicht reagierenden Verwalter. Wenn ein depotverwalter eine Hold-Benachrichtigung nach Erhalt der angegebenen Anzahl von Erinnerungen nicht anerkennt, kann das juristische Team einen Workflow angeben, um automatisch eine Eskalations Nachricht an die Depotbank und deren Vorgesetzten zu senden.

So planen Sie Eskalationen:

1. Klicken Sie **** in der Eskalations Kachel auf **Bearbeiten**.
   
2. Aktivieren Sie **** den Eskalations Workflow, indem Sie die **Status** -Umschaltfläche einschalten.
   
3. Geben Sie das **Eskalations Intervall (in Tagen)** (erforderlich) an. 
   
4. Geben Sie die **Anzahl der Eskalationen** an (erforderlich). Dieses Feld gibt an, wie viele Eskalationen an nicht reagierende Verwalter gesendet werden. Wenn Sie beispielsweise die Anzahl der Eskalationen auf 3 festlegen, wird eine Eskalations Benachrichtigung an die Depotbank und deren Vorgesetzten maximal 3 Mal gesendet. Nachdem ein depotverwalter die Hold-Benachrichtigung bestätigt hat, werden Eskalationen nicht mehr gesendet. 
   
5. Geben Sie den **Betreff** für den Hinweis an (erforderlich). 
   
6. Geben Sie die Inhalte oder zusätzlichen Anweisungen an, die Sie der Depotbank zur Verfügung stellen möchten (erforderlich). Beachten Sie, dass der in Schritt 2 definierte Portalinhalt am Ende der Eskalations Benachrichtigung hinzugefügt wird.
   
7. Klicken Sie auf **Speichern** , und fahren Sie mit dem nächsten Schritt fort.
   
## <a name="step-5-assign-custodians"></a>Schritt 5: Zuweisen von Verwaltern 

Nachdem Sie den Inhalt für Benachrichtigungen abgeschlossen haben, wählen Sie die Verwalter aus, an die Sie die Benachrichtigungen senden möchten. 

![Seite "Depotverwalter auswählen"](../media/SelectCustodians.PNG)

So fügen Sie Verwalter hinzu:

1. Weisen Sie der Kommunikation Verwalter zu, indem Sie auf das Kontrollkästchen neben Ihrem Namen klicken.

    Nachdem die Kommunikation erstellt wurde, wird der Benachrichtigungs Workflow automatisch auf die ausgewählten Verwalter angewendet.
   
2. Klicken Sie auf **weiter** , um die Kommunikationseinstellungen und Details zu überarbeiten.
 
>[!NOTE]
>Sie können nur Verwalter hinzufügen, die dem Fall hinzugefügt wurden und keine weitere Benachrichtigung innerhalb des Falls gesendet wurden.

## <a name="step-6-review-settings"></a>Schritt 6: Überarbeiten der Einstellungen

Nachdem Sie die Einstellungen überprüft und auf **senden** klicken, um die Kommunikation abzuschließen, wird der Kommunikations Workflow vom System automatisch gestartet, indem der Veröffentlichungshinweis gesendet wird.
