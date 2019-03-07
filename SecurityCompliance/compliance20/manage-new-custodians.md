---
title: Verwalten von Verwaltern in einem erweiterten eDiscovery-Fall (Preview)
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
ms.openlocfilehash: 6a21240f71c64f244ee42c3d3a2ed9d75381edaa
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454937"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a>Verwalten von Verwaltern in einem erweiterten eDiscovery-Fall (Preview)

Die Registerkarte Depotbanken enthält eine sortierbare Liste aller Verwalter in dem Fall. Nachdem Sie einem Fall Verwalter hinzugefügt haben, werden die Details zu den einzelnen Depotbanken automatisch aus Azure Active Directory gesammelt.

![Verwalten von verWaltern](../media/CustodianDetails.PNG)

## <a name="viewing-custodian-details"></a>Anzeigen von Depot Details

Die Flyout-Seite mit Depot Details wird angezeigt, nachdem Sie einen Verwalter zu einem Fall hinzugefügt haben, und wählen Sie ihn in der Liste auf der Registerkarte **Verwalter** aus. Von hier aus können Sie alle Details zu diesem Verwalter anzeigen. Die Flyout-Seite enthält die folgenden Felder:

- Kontaktinformationen

  - **Anzeigename**: der Name, der im Adressbuch für die Depotbank angezeigt wird. Dies ist normalerweise die Kombination aus Vornamen, mittlerem und Nachnamen.
  - **Mail/SMTP**: die SMTP-Adresse für die Depotbank, beispielsweise Jeff@contoso.onmicrosoft.com.  
  - **Title**: die Position des Depotbank-Titels.
  - **Abteilung**: der Name der Abteilung, in der die Depotbank arbeitet.
  - **Manager**: Manager der Depotbank. Der designierte Vorgesetzte erhält eine Eskalations Kommunikation für diesen Verwalter.
  
- Standortinformationen

  - **Ort**: die Stadt, in der sich die Depotbank befindet.
  - **Bundes**Land: Bundesland oder Kanton in der Depotbank-Adresse.
  - **Land/Region**: das Land/die Region, in der sich die Depotbank befindet; zum Beispiel "US" oder "UK".
  - **Office**: der Bürostandort im Geschäftssitz des Depotbank.

- Fall Informationen

  - **Status halten**: gibt an, ob die Depotbank in der Warteschleife gehalten wurde. 
  - **Kommunikationsstatus**: gibt an, ob der Depotbank eine Hold-Benachrichtigung ausgegeben wurde. Wenn der Depotbank eine Benachrichtigung ausgegeben wurde, wird diese als *veröffentlicht*gekennzeichnet. Wenn der Depotbank nicht eine Benachrichtigung ausgegeben wurde, wird dieser Status nicht *veröffentlicht*. 
  - **Status**: der Status der Depotbank innerhalb des Falls. Dies ist *aktiv* , wenn die Depotbank noch für den Fall in der Warteschleife ist. Wenn ein Depot aus einem Fall entfernt wird, wird der Status in *veröffentlicht*geändert. 

- Verarbeitungsstatus

  - **Indizierungsstatus**: gibt den Status des Deep Indexing-Auftrags an.  
  - **IndexIng Last updated Time**: gibt den DATESTAMP an, in dem der Deep Indexing-Auftrag zuletzt ausgelöst wurde.
  - **Datenquellen**: zeigt die Anzahl von Postfächern, Websites und Teams an, die für die Depotbank ausgewählt wurden.

## <a name="editing-a-custodian"></a>Bearbeiten einer Depotbank

Wenn Ihr Fall fortgeschritten ist, können Sie feststellen, dass möglicherweise zusätzliche Datenquellen relevant für eine bestimmte Depotbank & Ihrem Fall. In anderen Szenarien möchten Sie möglicherweise bestimmte Datenquellen entfernen, die überprüft und als nicht relevant eingestuft wurden.

So aktualisieren Sie einen Depotbank und die ausgewählten Datenquellen:

1. Wählen Sie einen vorhandenen Fall aus der **eDiscovery-_GT_ Advanced eDiscovery (Preview)** aus.
  
2. Klicken Sie in dem Fall auf die Registerkarte **depotverwalter** .
  
3. Wählen Sie die Verwalter aus der Liste aus, und klicken Sie auf **Quellen bearbeiten**.

    ![Bearbeiten von Datenquellen](../media/EditCustodianDataSource.PNG)
  
4. Aktualisieren Sie die Auswahl für Exchange-und OneDrive-Speicherorte, indem **Sie auf Datenquellen auswählen**klicken.
  
5. Hinzufügen oder Entfernen von Teams, SharePoint oder Exchange-Postfächern der Benutzer wird durch Klicken auf **zusätzliche Datenquellen**zugeordnet. Weitere Informationen dazu, wie Sie Datenquellen einem depotverwalter zuordnen, finden Sie unter Hinzufügen von Bewahrern [zu einem Fall](add-custodians-to-case.md).
  
6. Um den Status der Depotbank zu aktualisieren, **** klicken Sie auf Depot Aufbewahrung und aktivieren oder deaktivieren Sie die Aufbewahrung für Verwalter.

> [!TIP]
> Sie können mehrere Verwalter auswählen, um Massenaktionen durchzuführen, wie beispielsweise die erneute Indizierung, Freigabe oder Bearbeitung einer Reihe von Verwalter.

## <a name="resolving-custodian-processing-errors"></a>Beheben von Fehlern bei der Depot Verarbeitung

In den meisten legalen Workflows wird eine Teilmenge der Benutzerdaten durchsucht, nachdem Verwalter für eine bestimmte Untersuchung hinzugefügt wurden. Aufgrund von großen Dateigrößen oder möglicher Beschädigung können einige Elemente innerhalb der Datenquellen der Depotbank teilweise indiziert werden. Mithilfe der erweiterten eDiscovery (Preview) Deep Indexing-Funktion können diese teilweise indizierten Elemente durch erneutes Crawlen und Erneutes Indizieren dieser Elemente bei Bedarf automatisch wiederhergestellt werden. 

Wenn einem Fall eine Depotbank hinzugefügt wird, werden Ihre Daten automatisch "tief indiziert", sodass Benutzer diese teilweise indizierten Elemente beibehalten können, anstatt Suchvorgänge außerhalb von Office 365 herunterzuladen, zu beheben und erneut auszuführen. Während des Lebenszyklus eines Falls kann ein Benutzer Elemente korrigieren oder neue Datenquellen für eine bestimmte Depotbank hinzufügen. Möglicherweise muss der Depotbank-Index aktualisiert werden. 

So lösen Sie einen erneuten Indizierungsprozess für teilweise indizierte Elemente aus:

1. Wechseln Sie zu **eDiscovery _GT_ Advanced eDiscovery (Preview)** , und wählen Sie einen vorhandenen Fall aus.

2. Klicken Sie in diesem Fall auf die **Registerkarte depotverwalter**. 

3. Wählen Sie die Depotbanken aus, die erneut indiziert werden müssen, und klicken Sie dann auf ![Index aktualisieren](../media/UpdateIndex.PNG) auf der Flyout-Seite.

4. Überprüfen Sie den Status des Depot Indexes, indem Sie auf der Registerkarte **Depotbanken** auf den Link in der Spalte **Status des Indizierungs Auftrags** klicken.  

5. Der Status für den erneuten Indizierungsprozess kann auch auf der Registerkarte **Aufträge** nachverfolgt werden.

Weitere Informationen zum erneuten indizieren und korrigieren von teilweise indizierten Elementen finden Sie unter [Beheben von Verarbeitungsfehlern](processing-data-for-case.md).

## <a name="releasing-a-custodian-from-a-case"></a>Freigeben eines Depotbank aus einem Fall

Eine Depotbank wird in Situationen freigegeben, in denen ein Fall geschlossen ist, eine Depotbank nicht mehr zur Aufbewahrung von Inhalten für einen Fall verpflichtet ist oder wenn eine Depotbank als nicht mehr relevant für einen bestimmten Fall erachtet wird. 

Wenn Sie einen Verwalter freigeben, nachdem ein Aufbewahrungs Hinweis veröffentlicht wurde, wird eine Veröffentlichungs Benachrichtigung an die Depotbank gesendet. Darüber hinaus werden alle Depotinhaber, die den freigegebenen depotbanks zugeordnet sind, ebenfalls entfernt.

Wenn die Depotbank in einem Stillstand gehalten wurde, in dem Sie keine zugelassenen Haltestatus Benachrichtigungen ausgegeben haben, werden alle Freiheitsentzug, die den freigegebenen Verwaltern zugeordnet sind, entfernt.  

So geben Sie eine Depotbank frei 

1.  Wechseln Sie zur Registerkarte **depotverwalter** .

2.  Wählen Sie den Verwalter aus der Liste aus, und klicken Sie auf ![Versionsverwalter](../media/ReleaseCustodian.PNG) auf der Flyout-Seite.

    Der Status der Depotbank auf der Register **** Karte depotbanks ist auf **Released** festgelegt, und der **Haltestatus** auf der Flyout-Seite wird in **inaktiv**geändert. 

> [!TIP]
> Eine Depotbank kann an mehreren rechtlichen Aufbewahrungs Fragen beteiligt sein. Wenn ein Depot aus einem Fall entlassen wird, werden die Aufbewahrungs-und Benachrichtigungen in anderen Angelegenheiten nicht beeinträchtigt.

## <a name="related-information"></a>Weitere Informationen

 - [Beheben von Fehlern beim Verarbeiten von Daten](error-remediation.md) 
- [Arbeiten mit Kommunikation](managing-custodian-communications.md)
