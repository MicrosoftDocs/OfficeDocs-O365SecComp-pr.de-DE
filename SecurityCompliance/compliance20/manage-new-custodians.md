---
title: Verwalten von Verwalter in einem erweiterten eDiscovery (Preview)-Fall
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 742f6bc35b67071fba528e6a0ce543ecc6915762
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607831"
---
# <a name="managing-custodians-in-an-advanced-ediscovery-preview-case"></a>Verwalten von Verwalter in einem erweiterten eDiscovery (Preview)-Fall

Die Verwalter Registerkarte enthält eine Liste aller Verwalter im Fall sortierbare. Nachdem Sie eine Anfrage Verwalter hinzugefügt haben, werden Details zu einzelnen Verwaltungsberechtigter automatisch von Azure Active Directory gesammelt.

## <a name="viewing-custodian-details"></a>Anzeigen von Details zu Verwaltungsberechtigter

Die Dropdown-Seite, die Verwaltungsberechtigter Details enthält, wird angezeigt, nachdem Sie eine Anfrage ein Verwaltungsberechtigter hinzu, und sie aus der Liste auf der Registerkarte **Verwalter wählen** . Von hier aus können Sie alle im Zusammenhang mit diesem Verwaltungsberechtigter Details anzeigen. Die Dropdown-Seite enthält die folgenden Felder:

- Kontaktinformationen

  - **Anzeigename**: der Name der Verwaltungsberechtigte im Adressbuch angezeigt. Dies ist in der Regel die Kombination aus der Verwaltungsberechtigte Vorname, mittlere ersten und letzten Namen.
  - **/ SMTP Mail**: die SMTP-Adresse für der Verwaltungsberechtigte, beispielsweise jeff@contoso.onmicrosoft.com.  
  - **Titel**: der Verwaltungsberechtigte Position.
  - **Abteilung**: der Name für die Abteilung, in dem der Verwaltungsberechtigte funktioniert.
  - **Manager**: der Verwaltungsberechtigte-Manager. Der festgelegte-Manager erhalten alle Ausweitung Kommunikation für diese Verwaltungsberechtigter.
  
- Standortinformationen

  - **Ort**: der Ort, in dem der Verwaltungsberechtigte befindet.
  - **Status**: das Bundesland oder Kanton in der Verwaltungsberechtigte Adresse.
  - **Land/Region**: das Land/Region, in dem sich der Verwaltungsberechtigte befindet; "USA" oder "UK".
  - **Office**: der Standort des Büros der Verwaltungsberechtigte direkten Unternehmens.

- Case-Informationen

  - **Sperrstatus**: Gibt an, ob der Verwaltungsberechtigte in der Warteschleife versetzt wurde. 
  - **Kommunikationsstatus**: Gibt an, ob der Verwaltungsberechtigte eine Warteschleife Bekanntmachung ausgestellt wurde. Wenn der Verwaltungsberechtigte eine Benachrichtigung ausgegeben wurde, wird dies als *veröffentlichte*markiert werden. Wenn der Verwaltungsberechtigte keinen entsprechender Hinweis erteilt wurde noch, dann ist dieser Status wird *nicht veröffentlicht*. 
  - **Status**: der Status der Verwaltungsberechtigte innerhalb der Groß-/Kleinschreibung. Dies wird *aktiv* sein, wenn der Verwaltungsberechtigte weiterhin in der Warteschleife für die Groß-/Kleinschreibung ist. Wenn ein Verwaltungsberechtigter aus einem Fall entfernt wird, ändert sich ihr Status in *freigegeben*. 

- Verarbeitungsstatus

  - **Indizierungsstatus**: Gibt den Status des Auftrags Tiefe indizieren.  
  - **Zeitpunkt der letzten Aktualisierung Indizierung**: Gibt an, die Datumsstempel der bei der intensive Indizierung Auftrag zuletzt ausgelöst wurde.
  - **Datenquellen**: Zeigt die Anzahl der Postfächer, Websites und Teams, die für die Verwaltungsberechtigter ausgewählt wurden.

## <a name="updating-a-custodian"></a>Ein Verwaltungsberechtigter aktualisieren

Im Verlauf Ihrer Groß-/Kleinschreibung können Sie feststellen, dass möglicherweise zusätzliche Datenquellen für eine bestimmte Verwaltungsberechtigter & Bedeutung der Fall. In anderen Szenarien sollten Sie bestimmte Datenquellen zu entfernen, die überprüft und als nicht relevant angesehen wurden.

Ein Verwaltungsberechtigter und die ausgewählten Datenquellen zu aktualisieren:

1. Wählen Sie eine vorhandene Anfrage aus der **eDiscovery > erweiterte eDiscovery (Preview)**.
  
2. Klicken Sie auf der Registerkarte **Verwalter** , im Fall.
  
3. Wählen Sie die Custodian(s) aus der Liste aus, und klicken Sie auf **Bearbeiten von Quellen**.
  
4. Aktualisieren Sie Auswahl für Exchange und OneDrive Standorte durch **Auswählen von Datenquellen**auf.
  
5. Hinzufügen oder Entfernen von Teams, SharePoint oder Exchange Postfächer den Benutzer durch Klicken auf **zusätzliche Datenquellen**aus zugeordnet. Weitere Informationen dazu, wie Sie zum Zuordnen von Daten an ein Verwaltungsberechtigter Quellen, finden Sie unter [Verwalter hinzufügen, um eine erweiterte eDiscovery (Preview) Fall](add-custodians-to-case.md).
  
6. Um den Sperrstatus Verwaltungsberechtigter zu aktualisieren, **freiheitsentziehenden Place-Haltebereiche**, klicken Sie auf, und aktivieren Sie oder deaktivieren Sie den Haltestatus für Verwalter.

> [!TIP]
> Sie können mehrere Verwalter Massenaktionen wie erneute Indizierung, freigeben oder Bearbeiten einer Reihe von Verwalter ausführen auswählen.

## <a name="resolving-custodian-processing-errors"></a>Beheben von Verwaltungsberechtigten Verarbeitungsfehler

In den meisten rechtlichen Workflows nach dem Hinzufügen der Verwalter für eine bestimmte Untersuchung wird eine Teilmenge der Daten der Benutzer gesucht werden soll. Aufgrund der großen Dateien oder möglicherweise beschädigt können einige Elemente innerhalb der Verwalter Datenquellen teilweise indiziert werden. Die erweiterte eDiscovery (Preview) Tiefe Indizierung-Funktion verwenden, können diese teilweise indizierte Elemente automatisch behoben werden durch erneutes durchforsten und erneute Indizierung dieser Elemente nach Bedarf. 

Wenn ein Verwaltungsberechtigter eine Anfrage hinzugefügt wird, ihre Daten automatisch "intensive indiziert werden", können Benutzer die teilweise lassen Sie diese indizierte Elemente direkt anstelle der herunterladen, warten und Suchvorgänge außerhalb von Office 365 erneut ausführen. Während des Lebenszyklus einer Anfrage kann ein Benutzer warten von Elementen oder neue Datenquellen für ein bestimmtes Verwaltungsberechtigter hinzufügen. Dies erfordert möglicherweise den Index Verwaltungsberechtigter aktualisiert werden. 

Um eine erneute Indizierung Prozess an-Adresse teilweise auszulösen indizierte Elemente:

1. Wechseln Sie zur **eDiscovery > erweiterte eDiscovery (Preview)** , und wählen Sie eine vorhandene Anfrage aus.

2. Klicken Sie im Fall nacheinander auf **Verwalter**. 

3. Wählen Sie die Custodian(s), die erneut indiziert werden soll, und klicken Sie dann auf der Seite flyoutmenü **Index aktualisieren** .

4. Überprüfen Sie den Status des Indexes Verwaltungsberechtigter durch Klicken auf den Link in der Spalte **Indizierung Job Status** auf der Registerkarte **Verwalter** .  

5. Der Status für die erneute Indizierung kann auch auf der Registerkarte **Aufträge** nachverfolgt werden.

Weitere Informationen zur erneuten Indizierung und Korrigieren von teilweise indizierte Elemente finden Sie unter [behoben Verarbeitungsfehler in erweiterten eDiscovery (Preview)](processing-data-for-case.md).

## <a name="releasing-a-custodian-from-a-case"></a>Ein Verwaltungsberechtigter aus einem Fall freigeben

Ein Verwaltungsberechtigter freigegeben ist, in Situationen, in dem eine Anfrage abgeschlossen ist, ein Verwaltungsberechtigter ist nicht mehr verpflichtet, um die Inhalte für eine Anfrage beizubehalten oder wenn ein Verwaltungsberechtigter keine mehr als erachtet wird für ein bestimmtes relevant sein case. 

Wenn Sie ein Verwaltungsberechtigter freigeben, nachdem eine Warteschleife Bekanntmachung veröffentlicht wurde, wird eine Version Bekanntmachung an der Verwaltungsberechtigte gesendet. Darüber hinaus werden Haltebereiche freiheitsentziehenden Ergebnisarray als Attribut zugewiesen, die endgültige Verwalter entfernt werden.

Der Verwaltungsberechtigte automatische gehalten getätigt wurde, wurden sie keine Benachrichtigungen rechtliche Aufbewahrungspflicht ausgestellt, werden freiheitsentziehenden Haltebereiche Ergebnisarray als Attribut zugewiesen, die endgültige Verwalter entfernt.  

Um ein Verwaltungsberechtigter freizugeben: 

1.  Wechseln Sie zur Registerkarte **Verwalter** .

2.  Wählen Sie aus der Liste der Verwaltungsberechtigte aus, und klicken Sie auf der Seite flyoutmenü auf **Version Verwalter** .

    Der Status der Verwaltungsberechtigte auf der Registerkarte **Verwalter** auf **freigegeben** festgelegt ist und der **Sperrstatus** auf der Seite flyoutmenü in **inaktiv**geändert wird. 

> [!TIP]
> Ein Verwaltungsberechtigter werden gleichzeitig möglicherweise mehrere rechtliche Aufbewahrungspflicht Angelegenheiten beteiligt. Wenn ein Verwaltungsberechtigter aus einem Fall veröffentlicht wird, werden der Haltestatus und Benachrichtigungen über andere Angelegenheiten nicht beeinträchtigt werden.

## <a name="related-information"></a>Weitere Informationen

 - Benutzerattribute in Active Directory 
 - [Error Remediation beim Verarbeiten von Daten](error-remediation.md) 
 - [Arbeiten mit communications](managing-custodian-communications.md)
