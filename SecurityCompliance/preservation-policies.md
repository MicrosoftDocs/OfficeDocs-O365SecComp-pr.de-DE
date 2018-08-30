---
title: Übersicht über Aufbewahrungsrichtlinien
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 4/3/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 9c3b1d52-40ce-4ba3-a520-9ae0be15538a
description: Organisationen möchten, um aus dem Gesundheitswesen rechts- oder interne Richtlinien entsprechen, Inhalte für einen bestimmten Zeitraum aufbewahren. Mit einer Beibehaltung der Richtlinie in Office 365 können Sie Inhalte in Websites, Postfächer und Öffentliche Ordner auf unbestimmte Zeit oder für einen bestimmten Zeitraum beibehalten. Sie können auch den Inhalt filtern, der durch die Angabe Schlüsselwörter oder einen Datumsbereich aus, um die Suchergebnisse einzuschränken beibehalten wird.
ms.openlocfilehash: a26b85a563dd0e6f9ed8a70bfe9a310fc89a50f2
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272460"
---
# <a name="overview-of-preservation-policies"></a>Übersicht über Aufbewahrungsrichtlinien

> [!IMPORTANT]
> Wenn Sie eine Beibehaltung der Richtlinie verwendet haben, wurde die Richtlinie automatisch konvertiert auf einer Aufbewahrungsrichtlinie, also ein neues Feature, das bietet alle Funktionen, die eine Beibehaltung der Richtlinie wird und mehr. Die Beibehaltung der Richtlinie wird weiterhin arbeiten und Ihrer Inhalte ohne Anpassungen von Ihnen beibehalten. Sie finden diese Richtlinien auf der Seite **Aufbewahrung** in das Wertpapier &amp; Compliance Center. Weitere Informationen finden Sie unter [Änderungen bei der Beibehaltung der Richtlinien?](retention-policies.md#what-happened-to-preservation-policies)
  
Organisationen möchten, um aus dem Gesundheitswesen rechts- oder interne Richtlinien entsprechen, Inhalte für einen bestimmten Zeitraum aufbewahren. Mit einer Beibehaltung der Richtlinie in Office 365 können Sie Inhalte in Websites, Postfächer und Öffentliche Ordner auf unbestimmte Zeit oder für einen bestimmten Zeitraum beibehalten. Sie können auch den Inhalt filtern, der durch die Angabe Schlüsselwörter oder einen Datumsbereich aus, um die Suchergebnisse einzuschränken beibehalten wird.
  
Beispielsweise die Inhalte in bestimmte Postfächer und zugehörigen the Sales Department sieben Jahren Websites beibehalten werden kann, und um den Bereich der Richtlinie darauf hin, dass Sie nur Inhalte aus den letzten zwei Jahren beibehalten, die eine bestimmte möchten einzugrenzen Name des Clients.
  
Wenn Inhalt zu einer Beibehaltung der Richtlinie ist, können Benutzer weiterhin bearbeiten und Arbeiten mit dem Inhalt wie Nothing zurück, da der Inhalts am ursprünglichen Speicherort direktes beibehalten geändert wird. Aber wenn jemand bearbeitet oder löscht Inhalte, die die Richtlinie gilt, wird eine Kopie an einem sicheren Speicherort, in dem es beibehalten wird, während die Richtlinie aktiviert ist.
  
Schließlich müssen einige Organisationen möglicherweise Einhaltung der behördlichen Texte wie die Sicherheit And Exchange Commission (s) Richtlinie 17a-4, die erforderlich sind, nachdem eine Beibehaltung der Richtlinie aktiviert ist, nicht deaktiviert oder weniger restriktiv vorgenommen definierten Regeln. Um diese Anforderung erfüllt, können Sie die Beibehaltung der Sperre verwenden. Nachdem eine Richtlinie des gesperrt wurde, niemand – einschließlich des Administrators – deaktivieren Sie die Richtlinie oder machen es weniger restriktiv können.
  
Sie erstellen und Verwalten von Beibehaltung der Richtlinien auf der Seite Aufbewahrung in die Office 365-Sicherheit &amp; Compliance Center.
  
![Aufbewahrung Seite in Office 365-Sicherheit &amp; Compliance Center](media/edb2e228-efff-4619-89d1-8665b5f38639.png)
  
> [!NOTE]
> Exchange Online-Postfachs in eine Beibehaltung der Richtlinie aufnehmen möchten, muss das Postfach eine Lizenz für Exchange Online – Plan 2 zugewiesen werden. Wenn ein Postfach eine Exchange Online – Plan 1-Lizenz zugewiesen ist, müssten Sie ihm eine separate Lizenz der Exchange Online-Archivierung für die Einbeziehung in eine Beibehaltung der Richtlinie zuweisen. 
  
## <a name="how-a-preservation-policy-works-with-content-in-place"></a>Funktionsweise einer Aufbewahrungsrichtlinie mit Inhalten

Wenn Sie eine Website, Postfach oder Öffentliche Ordner in einer Richtlinie permanentes einschließen, bleibt die Inhalte am ursprünglichen Speicherort. Benutzer können ihre Dokumente oder e-Mail entwickelt weiterhin, aber eine Kopie des Inhalts, wie es vorhanden war, als Sie die Richtlinie initiiert wird beibehalten. Für Websites, Inhalte des in der Bibliothek permanentes halten werden beibehalten. für Öffentliche Ordner und Postfächer beibehalten im Ordner "wiederherstellbare Elemente" des Inhalts. Diese sicheren Orten und beibehaltenem Inhalt sind nicht für die meisten Benutzer sichtbar. Mit einer Richtlinie permanentes müssen Personen sogar nicht bekannt ist, dass ihre Inhalte die Richtlinie gilt.
  
![Diagramm, das die Funktionsweise von Aufbewahrungsrichtlinien zeigt](media/2c1dd82b-84e0-49e0-ab46-d017df297040.png)
  
### <a name="site-content"></a>Websiteinhalt

Eine Beibehaltung der Richtlinie wird auf der Ebene einer Website angewendet. Wenn Sie eine Website in eine Beibehaltung der Richtlinie einschließen, wird eine Bibliothek permanentes halten erstellt, falls nicht bereits vorhanden. Die meisten Benutzer können die Bibliothek permanentes halten nicht anzeigen, da sie nur für den Besitzer der Websitesammlung angezeigt wird.
  
Wenn ein Benutzer versucht, ändern oder Löschen von Inhalt in einer Website, die eine Beibehaltung der Richtlinie fällt, überprüft zuerst die Richtlinie, ob der Inhalt des geändert wurden, seit die Richtlinie angewendet wurde. Ist dies der erste ändern, da die Beibehaltung der Richtlinie angewendet wurde, wird die Richtlinie kopiert den Inhalt in der Bibliothek permanentes halten und klicken Sie dann die Person ändern oder Löschen der ursprünglichen Inhalts ermöglicht. Beachten Sie, dass alle Inhalte der Website auf die Bibliothek permanentes halten, kopiert werden kann, selbst wenn der Inhalt den Filter der Abfrage, durch die Beibehaltung der Richtlinie nicht überein.
  
In diesem Fall bereinigt ein Zeitgeberauftrag die Aufbewahrungsbibliothek. Der Zeitgeberauftrag wird regelmäßig ausgeführt und vergleicht den gesamten Inhalt der Aufbewahrungsbibliothek mit den Filtern, die von den Aufbewahrungsrichtlinien der Website verwendet werden. Fall der Inhalt nicht mindestens einem der Filter entspricht, löscht der Zeitgeberauftrag den Inhalt dauerhaft aus der Aufbewahrungsbibliothek.
  
Die vorherigen gilt für Inhalte, die vorhanden ist, wenn die Beibehaltung der Richtlinie angewendet wird. Darüber hinaus werden alle neuen Inhalte, die erstellt oder auf der Website hinzugefügt werden, nachdem es in die Richtlinie aufgenommen wurde nach dem Löschen beibehalten. Jedoch ist nicht neuer Inhalt in der Beibehaltung halten Bibliothek die erste kopiert bearbeitet nur, wenn es gelöscht wird. Um Versionen für alle Dateien zu erhalten, müssen Sie Versionskontrolle aktivieren – finden Sie im Abschnitt höheren auf Versioning.
  
### <a name="mailbox-and-public-folder-content"></a>Inhalte von Postfächern und öffentlichen Ordnern

Für die E-Mails und andere Elemente eines Benutzers wird eine Aufbewahrungsrichtlinie auf Postfachebene angewendet. Für einen öffentlichen Ordner wird eine Aufbewahrungsrichtlinie auf Ordnerebene angewendet, nicht auf Postfachebene. Ein Postfach und ein öffentlicher Ordner verwenden beide den Order „Wiederherstellbare Elemente“, um Elemente beizubehalten. Nur Personen, denen eDiscovery-Berechtigungen zugewiesen wurden, können den Ordner „Wiederherstellbare Elemente“ eines anderen Benutzers anzeigen.  
  
Wenn eine Person eine Nachricht von einem anderen Ordner als dem Ordner Gelöschte Elemente löscht, wird standardmäßig die Nachricht in den Ordner Gelöschte Objekte verschoben. Wenn eine Person ein Element aus dem Ordner Gelöschte Elemente löscht, wird die Nachricht wird in den Ordner wiederherstellbare Elemente verschoben und wird nicht mehr des Benutzers angezeigt. Darüber hinaus kann eine Person weiche ein Elements (UMSCHALT + ENTF) in einen Ordner löschen die umgeht des Ordners Gelöschte Objekte und platziert das Element direkt im Ordner "wiederherstellbare Elemente".
  
Wenn ein Postfach in die Aufbewahrungsrichtlinie aufgenommen wird, werden gelöschte Elemente in den Ordner "DiscoveryHold" innerhalb des Ordners "Wiederherstellbare Elemente" verschoben. Beim regelmäßigen Verarbeiten des Postfachs wertet der Postfach-Assistent Nachrichten in diesem Ordner aus. Sofern der Inhalt nicht mindestens einem von einer Aufbewahrungsrichtlinie verwendeten Filter entspricht, löscht der Postfach-Assistent den Inhalt des Ordners "Wiederherstellbare Elemente" dauerhaft.
  
Ordner "wiederherstellbare Elemente" enthält auch einen Versionsordner. Wenn eine Person versucht, bestimmte Eigenschaften eines postfachelements ändern – beispielsweise den Betreff, body, Anlagen, Absender und Empfänger oder Datum gesendet oder empfangen wurden für eine Nachricht – eine Kopie des ursprünglichen Elements wird im Versionsordner gespeichert, bevor der Commit für die Änderung erfolgt ist. In diesem Fall für jede nachfolgende Änderung. Nachdem die Beibehaltung der Richtlinie entfernt wurde, werden durch die Postfach-Assistent Kopien im Ordner "Versionen" entfernt.
  
### <a name="where-a-preservation-policy-is-stored"></a>Speicherort der Aufbewahrungsrichtlinie

Wenn Sie eine Beibehaltung der Richtlinie erstellen, wird es zentral gespeichert werden, in das Wertpapier &amp; Compliance Center, und klicken Sie dann auf die verschiedenen Inhaltsquellen, die die Richtlinie, wie Websites, Postfächer und Öffentliche Ordner enthält bereitgestellt.
  
Nachdem eine Aufbewahrungsrichtlinie für diese Inhaltsquellen bereitgestellt wird, funktioniert die Richtlinie genau wie ein eDiscovery-In-Place-Archiv. Weitere Informationen zu In-Place-Aufbewahrungen finden Sie unter:
  
- [Übersicht über eDiscovery und Compliance - Archive](https://go.microsoft.com/fwlink/p/?LinkID=404352) (SharePoint Online) 
    
- [Compliance - Archiv und Aufbewahrung für eventuelle Rechtsstreitigkeiten](https://go.microsoft.com/fwlink/p/?LinkID=404353) (Exchange Online) 
    
- [Ordner "wiederherstellbare Elemente"](https://go.microsoft.com/fwlink/p/?LinkID=404354) (Exchange Online) 
    
### <a name="preservation-policy-vs-ediscovery-hold"></a>Beibehaltung der Richtlinie im Vergleich zu eDiscovery Haltestatus

Während es true ist, dass beide Features Inhalte enthalten, sollten diese Features nicht verwechselt werden, da sie verschiedene Zwecke dienen:
  
- **Wenn Sie Inhalte im Rahmen einer Aufbewahrungsrichtlinie Anforderung beibehalten müssen, verwenden Sie eine Richtlinie permanentes.** Wenn Sie Inhalte für sieben Jahre als Teil des Projektplans Aufbewahrung beibehalten werden müssen, verwenden Sie beispielsweise eine Beibehaltung der Richtlinie. Eine Beibehaltung der Richtlinie kann Inhalte für einen bestimmten Zeitraum aufbewahren, und am Ende der angegebenen Periode des Inhalts automatisch freigegeben aus der Richtlinie. Die Richtlinie kann auch gesperrt werden, damit niemand der Richtlinie deaktivieren oder weniger restriktiv erleichtern können. Eine eDiscovery-Archiv kann nicht gesperrt werden, oder geben Sie einen Zeitraum. Darüber hinaus hat eine Beibehaltung der Richtlinie im Allgemeinen eine Dauer von Jahre, während einer eDiscovery-Archiv vorübergehend ist und häufig nur die Dauer der rechtlichen Fall dauert. 
    
    Darüber hinaus können Sie eine Beibehaltung der Richtlinie ohne die zusätzlichen Schritte, dass eDiscovery möglicherweise, erfordern wie das Erstellen von Fällen Hinzufügen von Mitgliedern, oder wie folgt Inhalte durchsucht erstellen.
    
- **Wenn Sie Inhalte im Rahmen einer Anforderung von der rechts- oder eDiscovery halten müssen, verwenden Sie eine eDiscovery-Haltestatus.** Wenn Sie Inhalte an bestimmten Speicherorten im Rahmen einer rechtlichen Anforderung halten müssen, verwenden Sie beispielsweise eine eDiscovery-halten. Der Inhalt für eine Anfrage relevant ist in der Regel vertrauliche eDiscovery oder privilegierte, sodass andere Fällen können verschiedene Member beschränkt werden. Darüber hinaus Unterstützung von eDiscovery durch Content-Suche, die gespeichert, in der Seitenansicht angezeigt, mit erweiterten eDiscovery analysiert werden können, oder die Ergebnisse exportiert haben. 
    
    Im Gegensatz zu einer Richtlinie Beibehaltung einer eDiscovery-Archiv kann nicht Definieren eines Zeitraums - einer eDiscovery-Archiv ist gültig, bis Sie ihn deaktivieren oder zu löschen. Darüber hinaus kann ein eDiscovery Haltestatus gesperrt werden.
    
## <a name="how-a-preservation-policy-works-with-document-versions-in-a-site"></a>Funktionsweise einer Aufbewahrungsrichtlinie mit Dokumentversion in einer Website

Eine Beibehaltung der Richtlinie beibehalten nicht automatisch alle Versionen eines Dokuments in einer Website. Hierzu müssen Sie versionsverwaltung für die Dokumentbibliotheken auf der Website zu aktivieren. Weitere Informationen finden Sie unter [Aktivieren und Konfigurieren der versionsverwaltung für eine Liste oder Bibliothek](https://go.microsoft.com/fwlink/p/?LinkID=404350).
  
Wenn ein Dokument wird gelöscht aus einer Website, die gespeichert wird und die dokumentversionierung für die Bibliothek aktiviert ist, werden alle Versionen des gelöschten Dokuments beibehalten. 
  
Wenn dokumentversionierung ist nicht aktiviert, und ein Element mehrere permanentes Richtlinien unterliegt, wird die Version, die beibehalten wird, die aktuell ist, wenn jeder Beibehaltung der Richtlinie in Kraft treten kann. Beispielsweise wenn Version 27 eines Elements handelt es sich um das aktuellste Ergebnis die Website beibehalten wird die erste Uhrzeit und Version 51 das aktuellste Ergebnis wird bei die Website der zweites Mal Versionen 27 und 51 beibehalten wird werden beibehalten.
  
## <a name="filtering-a-preservation-policy"></a>Filtern einer Aufbewahrungsrichtlinie

Sie können die von einer Aufbewahrungsrichtlinie erfassten Inhalte eingrenzen, indem Sie der Richtlinie Schlüsselwörter oder einen Datumsbereich hinzufügen. 
  
![Die Verwendung von Schlüsselwörtern und Datumsbereichen als Filter beim Erstellen einer Aufbewahrungsrichtlinie](media/603cef40-8f7c-4140-956f-28c092273582.png)
  
### <a name="filter-by-using-keywords"></a>Filtern mithilfe von Schlüsselwörtern

Eine Beibehaltung der Richtlinie unterstützt Keyword Query Language (KQL). Beispielsweise können Sie grundlegende Operatoren wie und und oder, und Sie können eine Suche, wobei "Wingtip NEAR(30) Marketing" Ergebnisse bezeichnet wird, in dem "Wingtip" 30 Zeichen "Marketing". Eine schlüsselwortabfrage unterstützt Sie beim Identifizieren und Beibehalten von nur der relevante Inhalte.
  
### <a name="filter-by-using-a-date-range"></a>Filtern mithilfe eines Datumsbereichs

Sie können die Aufbewahrung auch filtern, sodass nur Inhalte innerhalb eines bestimmten Datumsbereichs beibehalten werden. Für Nachrichten ist das Datum relativ zum Empfangsdatum und für Dokumente und Websites ist das Datum relativ zum Änderungsdatum. Das bedeutet, dass Sie Inhalte beibehalten können, die empfangene E-Mails und geänderte Dokumente innerhalb eines bestimmten Datumsbereichs oder vor oder nach einem Start- oder Enddatum umfassen.
  
## <a name="preserving-content-for-a-specific-period-of-time"></a>Aufbewahren von Inhalten für einen bestimmten Zeitraum

Mit einer Aufbewahrungsrichtlinie können Sie Inhalte für unbegrenzte Zeit oder für eine bestimmte Anzahl von Tagen, Monaten oder Jahren aufbewahren. Beachten Sie, dass die Dauer der Inhaltsaufbewahrung anhand des Alters des Inhalts berechnet wird, nicht anhand des Erstellungsdatums der Richtlinie. 
  
Beispielsweise wenn Inhalte in einer Website sieben Jahren und in einem Dokument erhalten bleiben soll dieser Website noch nicht in sechs Jahren geändert wurde, wird das Dokument nur einen anderen Jahr beibehalten, wenn es nicht geändert wird. Wenn das Dokument erneut bearbeitet wird, wird das Alter des Dokuments aus der neuen Datum der letzten Änderung berechnet und beibehalten wird, ein anderes sieben Jahre.
  
Wenn Sie also Inhalte eines Postfachs sieben Jahre lang aufbewahren möchten und eine Nachricht vor sechs Jahren gesendet wurde, wird die Nachricht nur noch ein Jahr aufbewahrt, falls das Empfangsdatum nicht geändert wird. In diesem Falls wird eine neue Version der Nachricht, wie sie vor der Bearbeitung vorhanden war, im Ordner "Wiederherstellbare Elemente" aufbewahrt, und das Alter der Nachricht wird anhand des neuen Empfangsdatums berechnet. Danach wird sie für weitere sieben Jahre aufbewahrt.
  
![Dauereinstellung für eine neue Aufbewahrungsrichtlinie](media/455aac78-4c29-4dbb-93a2-b431b99002d9.png)
  
## <a name="locking-a-preservation-policy"></a>Sperren einer Aufbewahrungsrichtlinie

In einigen Unternehmen müssen möglicherweise Einhaltung der behördlichen Texte wie die Sicherheit And Exchange Commission (s) Richtlinie 17a-4, die erforderlich sind, nachdem eine Beibehaltung der Richtlinie aktiviert ist, nicht deaktiviert oder weniger restriktiv vorgenommen definierten Regeln. Mit Sperre ein permanentes, können Sie also die Richtlinie sperren, dass kein anderer – einschließlich des Administrators – deaktivieren Sie die Richtlinie oder machen es weniger restriktiv können.
  
Nachdem eine Richtlinie des gesperrt wurde, kann niemand deaktivieren oder Entfernen von Inhalt aus der Richtlinie. Und es ist nicht möglich, ändern oder Löschen von Inhalt, das die Richtlinie während des Berichtszeitraums permanentes fällt. Nachdem die Richtlinie des gesperrt wurde, sind die einzigen Möglichkeiten, die Sie die Beibehaltung der Richtlinie bearbeiten können durch Hinzufügen von Inhalt oder seine Dauer erweitern. Eine Richtlinie gesperrte erhöht oder erweitert werden kann, jedoch nicht verringert oder deaktiviert.
  
Aus diesem Grund, bevor Sie eine Beibehaltung der Richtlinie sperren, ist es wichtig, dass Sie Compliance-Bestimmungen Ihrer Organisation verstehen und keine Richtlinie zu sperren, bis Sie sicher sind, dass er ist, was Sie benötigen.
  
![Option zum Aktivieren der Aufbewahrungssperre](media/cf9cc070-ddfb-469c-a47e-f88005a82fe4.png)
  
## <a name="turning-off-a-preservation-policy"></a>Eine Beibehaltung der Richtlinie deaktivieren

Wenn Sie nicht die Beibehaltung der Richtlinie zu sperren, können Sie sie jederzeit, auch vor Ablauf des Zeitraums, durch die Richtlinie festgelegten freigeben. Hierzu müssen Sie nur die Richtlinie deaktivieren.
  
![Option für eine Beibehaltung der Richtlinie auf der Seite Beibehaltung der Sicherheit deaktivieren &amp; Compliance Center](media/fdb44455-da01-4480-8fa6-0e3b29b1f535.png)
  
Jedoch können Sie eine Beibehaltung der Richtlinie nicht löschen, während die Richtlinie noch aktiv's. Um eine Beibehaltung der Richtlinie zu löschen, deaktivieren Sie zuerst, und löschen Sie die Richtlinie.
  
Nachdem Sie eine Beibehaltung der Richtlinie deaktiviert haben, sind alle Elemente dieser Richtlinie in der Bibliothek permanentes halten oder Ordner "wiederherstellbare Elemente" für das zuvor beschriebene Verfahren standard Cleanup. Beachten Sie, dass dies bedeutet, dass Objekte freigegeben von einer Richtlinie nicht sofort gelöscht werden. Stattdessen bleiben sie in der Bibliothek permanentes halten oder Ordner "wiederherstellbare Elemente", bis der Prozess in regelmäßigen Abständen die Bibliothek oder einen Ordner bereinigt.
  
## <a name="using-preservation-policies-with-retention-policies-and-document-deletion-policies"></a>Verwenden von Aufbewahrungsrichtlinien mit Dokumentlöschrichtlinien

Eine Aufbewahrungsrichtlinie stellt sicher, dass Inhalte auf unbegrenzte Zeit oder für einen bestimmten Zeitraum beibehalten werden, während eine Aufbewahrungsrichtlinie für ein Postfach und eine Dokumentlöschrichtlinie für eine Website sicherstellt, dass Inhalte nach einer bestimmten Zeit gelöscht werden.  Wenn Sie Inhalte für einen festen Zeitraum beibehalten müssen, können Sie eine Aufbewahrungsrichtlinie zusammen mit einer Löschrichtlinie verwenden. 
  
### <a name="site-content"></a>Websiteinhalt

Für eine Website können Sie eine Aufbewahrungsrichtlinie zusammen mit einer Dokumentlöschrichtlinie verwenden. Sie können beispielsweise Dokumente nach einer Änderung fünf Jahre lang aufbewahren und dann eine Löschrichtlinie einrichten, um sie fünf Jahre nach der letzten Änderung zu löschen.
  
Eine dokumentlöschrichtlinie Inhalt löscht, das eine Beibehaltung der Richtlinie fällt, wird der Inhalt noch in der Bibliothek permanentes halten beibehalten. Beispielsweise werden, wenn eine Beibehaltung der Richtlinie Inhalt für zwei Jahre behält, aber eine dokumentlöschrichtlinie löscht den Inhalt nach einem Jahr, alle Inhalte, die gelöscht wird weiterhin beibehalten. Weitere Informationen finden Sie unter [Übersicht über dokumentlöschrichtlinien](https://support.office.com/article/55e8d858-f278-482b-a198-2e62d6a2e6e5).
  
### <a name="mailbox-content"></a>Inhalt von Postfächern

Sie können für ein Postfach eine Beibehaltung der Richtlinie mit einer Aufbewahrungsrichtlinie kombinieren, die eine einzelne Richtlinie Standardtag verfügt. Beispielsweise konnten Sie beibehalten von postfachelementen sieben Jahren, und klicken Sie dann richten Sie eine Aufbewahrungsrichtlinie zu löschen sieben Jahre nach (für Nachrichten empfangen) oder (für Elemente, die gesendet werden nicht, wie Notes) erstellt wurden. Die Beibehaltung der Richtlinie wird sichergestellt, dass Elemente, die gelöscht für mindestens die angegebene Dauer, erhalten bleiben, während die Aufbewahrungsrichtlinie wird sichergestellt, dass am Ende dieses Zeitraums Postfachelemente gelöscht werden. Weitere Informationen finden Sie unter [aufbewahrungstags und Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/p/?LinkID=404351).
  
## <a name="permissions"></a>Berechtigungen

Mitglieder Ihres Teams Compliance, die die Sicherheit zu nutzen, werden &amp; Compliance Center permanentes Richtlinien erstellen benötigen Berechtigungen, um die:
  
-  Office 365 Security &amp; Compliance Center 
    
- Websites mit Inhalten, die beibehalten werden sollen
    
- Postfächer mit Inhalten, die beibehalten werden sollen
    
### <a name="office-365-security-amp-compliance-center"></a>Office 365 Security &amp; Compliance Center

Als ein Administrator, Compliance Officer und anderen Personen Zugriff auf die Sicherheit gewähren können sollen &amp; Compliance Center, ohne dass sie alle erforderlichen Berechtigungen von einem Mandanten Admin. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
  
### <a name="sites"></a>Websites

Mitglieder Ihres Kompatibilitätsteams, die Aufbewahrungsrichtlinien erstellen, benötigen Berechtigungen für die Websitesammlungen, auf die die Richtlinien angewendet werden: Wenn auch Compliance Officers Dokumentlöschrichtlinien erstellen, benötigen sie darüber hinaus Berechtigungen für die Compliance Policy Center-Websitesammlung, in der Dokumentlöschrichtlinien erstellt und gespeichert werden. Wir empfehlen, dass Sie wie folgt vorgehen:
  
1. Erstellen Sie eine Sicherheitsgruppe, die alle Benutzer der Richtlinie Compliance Center enthält – wahrscheinlich Compliance richtlinienverwaltung Team. Weitere Informationen finden Sie unter [Manage Mail-Enabled-Sicherheitsgruppen](https://go.microsoft.com/fwlink/p/?LinkID=404345) . 
    
2. Fügen Sie die Sicherheitsgruppe im Compliance Center Richtlinie um der Gruppe der Besitzer. Weitere Informationen finden Sie unter [Berechtigungen für Administratoren von Websitesammlungen](https://go.microsoft.com/fwlink/p/?LinkID=404346) . 
    
3. Fügen Sie in jeder Websitesammlung, der Sie Aufbewahrungsrichtlinien zuweisen möchten, die Sicherheitsgruppe zur Gruppe der Websitesammlungs-Besucher (mit Leseberechtigungen) hinzu.
    
### <a name="mailboxes-and-public-folders"></a>Postfächer und öffentliche Ordner

Um eine Aufbewahrungsrichtlinie auf ein Postfach anzuwenden, muss der Compliance Officer zumindest die Leseberechtigung für dieses Postfach haben. 
  
Um eine Aufbewahrungsrichtlinie auf einen öffentlichen Ordner anzuwenden, muss der Compliance Officer zumindest die Leseberechtigung für alle öffentlichen Ordner haben.
  

