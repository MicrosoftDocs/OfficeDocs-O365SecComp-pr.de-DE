---
title: Einführung in Informationsverwaltungsrichtlinien
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/16/2014
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- WSU150
- SPO160
- OSU150
- MET150
ms.assetid: 63a0b501-ba59-44b7-a35c-999f3be057b2
ms.collection:
- M365-security-compliance
description: Eine Informationsverwaltungsrichtlinie ist ein Satz von Regeln für einen Inhaltstyp. Mithilfe von Informationsverwaltungsrichtlinien können Organisationen Dinge wie lange Inhalte beibehalten oder welche Aktionen Benutzer mit diesen Inhalten ausführen können. Informationsverwaltungsrichtlinien können Organisationen dabei helfen, gesetzliche oder behördliche Bestimmungen einzuhalten, oder Sie können nur interne Geschäftsprozesse erzwingen.
ms.openlocfilehash: 23662c555dfc19b2fc83b0364d93724e922c7c97
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275755"
---
# <a name="introduction-to-information-management-policies"></a>Einführung in Informationsverwaltungsrichtlinien

Eine Informationsverwaltungsrichtlinie ist ein Satz von Regeln für einen Inhaltstyp. Mithilfe von Informationsverwaltungsrichtlinien können Organisationen Dinge wie lange Inhalte beibehalten oder welche Aktionen Benutzer mit diesen Inhalten ausführen können. Informationsverwaltungsrichtlinien können Organisationen dabei helfen, gesetzliche oder behördliche Bestimmungen einzuhalten, oder Sie können nur interne Geschäftsprozesse erzwingen. 
  
Beispielsweise kann eine Organisation, die den behördlichen Vorschriften folgen muss, dass Sie "angemessene Kontrollen" ihrer Abschlüsse demonstrieren, eine oder mehrere Informationsverwaltungsrichtlinien erstellen, die bestimmte Aktionen in der Erstellungs-und Genehmigungsprozess für alle Dokumente im Zusammenhang mit finanziellen Anmeldungen.
  
Informationen zu Vorgehensweisen finden Sie unter [Erstellen und Anwenden von Informationsverwaltungsrichtlinien](create-info-mgmt-policies.md).
  
## <a name="features-of-information-management-policies"></a>Features von Informationsverwaltungsrichtlinien
<a name="__top"> </a>

Es gibt vier grundlegende Kategorien von vordefinierten Richtlinienfeatures, die Organisationen einzeln oder in Kombination zum Verwalten von Inhalten und Prozessen verwenden können. 
  
![Arten von Inhaltsrichtlinien](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
Mit dem Überwachungsrichtlinienfeature können Organisationen analysieren, wie Ihre Inhaltsverwaltungssysteme verwendet werden, indem Ereignisse und Vorgänge protokolliert werden, die für Dokumente und Listenelemente ausgeführt werden. Sie können das Überwachungsrichtlinienfeature so konfigurieren, dass Ereignisse wie beim Bearbeiten, anzeigen, Einchecken, Auschecken, löschen oder Ändern der Berechtigungen protokolliert werden. Alle Überwachungsinformationen werden in einem einzelnen Überwachungsprotokoll auf dem Server gespeichert, und Websiteadministratoren können Berichte darauf ausführen. 
  
Mit dem Ablaufrichtlinienfeature können Organisationen veraltete Inhalte von ihren Websites auf konsistente, nach verfolgbare Weise löschen oder entfernen. Auf diese Weise können Sie sowohl die Kosten als auch das Risiko verwalten, die mit der Beibehaltung von veralteten Inhalten verbunden sind. Sie können eine Ablaufrichtlinie konfigurieren, um anzugeben, dass bestimmte Inhaltstypen an einem bestimmten Datum oder innerhalb eines Zeitraums ablaufen, nachdem das Dokument erstellt oder zuletzt geändert wurde.
  
Organisationen können auch benutzerdefinierte Richtlinienfeatures erstellen und bereitstellen, um bestimmte Anforderungen zu erfüllen. Eine Produktionsorganisation kann beispielsweise eine Informationsverwaltungsrichtlinie für alle Entwurfs Spezifikationsdokumente definieren, die es Benutzern untersagt, Kopien dieser Dokumente auf nicht sicheren Druckern zu drucken. Um diese Art von Informationsverwaltungsrichtlinie zu definieren, können Sie ein Feature für die Druck Einschränkungsrichtlinie erstellen und bereitstellen, das der relevanten Informationsverwaltungsrichtlinie für den Inhaltstyp Product Design Specification hinzugefügt werden kann.
  
## <a name="locations-to-use-an-information-management-policy"></a>Standorte für die Verwendung einer Informationsverwaltungsrichtlinie
<a name="__toc340213528"> </a>

Um eine Informationsverwaltungsrichtlinie zu implementieren, müssen Sie Sie einer Liste, einer Bibliothek oder einem Inhaltstyp in einer Website hinzufügen. Der Speicherort, an dem Sie eine Informationsverwaltungsrichtlinie erstellen oder hinzufügen, wirkt sich auf die Breite der Richtlinie oder ihre Breite aus. Sie können:
  
 **Erstellen Sie eine Websitesammlungsrichtlinie, und fügen Sie diese Richtlinie dann einem Inhaltstyp, einer Liste oder einer Bibliothek hinzu** . Sie können eine Websitesammlungsrichtlinie in der Liste Richtlinien auf der Website auf oberster Ebene einer Websitesammlung erstellen. Nachdem Sie eine Websitesammlungsrichtlinie erstellt haben, können Sie Sie exportieren, sodass Administratoren anderer Websitesammlungen Sie in Ihre Richtlinienliste importieren können. Durch das Erstellen einer exportierbaren Websitesammlungsrichtlinie können Sie die Informationsverwaltungsrichtlinien für die Standorte in Ihrer Organisation standardisieren. 
  
Wenn Sie eine Websitesammlungsrichtlinie einem Websiteinhaltstyp hinzufügen und eine Instanz dieses Websiteinhaltstyps einer Liste oder Bibliothek hinzugefügt wird, kann der Besitzer dieser Liste oder Bibliothek die Websitesammlungsrichtlinie für die Liste oder Bibliothek nicht ändern. Das Hinzufügen einer Websitesammlungsrichtlinie zu einem Websiteinhaltstyp ist eine gute Möglichkeit, um sicherzustellen, dass Websitesammlungsrichtlinien auf jeder Ebene ihrer Websitehierarchie erzwungen werden.
  
![Link zur Inhaltstyp-Richtlinienvorlage auf der Seite Websiteeinstellungen](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
 **Erstellen Sie eine Informationsverwaltungsrichtlinie für einen Websiteinhaltstyp im Websiteinhaltstyp Katalog der Website auf oberster Ebene, und fügen Sie diesen Inhaltstyp einer oder mehreren Listen oder Bibliotheken hinzu.** Sie können auch eine Informationsverwaltungsrichtlinie direkt für einen Websiteinhaltstyp erstellen und dann eine Instanz dieses Websiteinhaltstyps mehreren Listen oder Bibliotheken zuordnen. Wenn Sie eine Informationsverwaltungsrichtlinie auf diese Weise erstellen, weist jedes Element in der Websitesammlung dieses Inhaltstyps oder eines Inhaltstyps, der von diesem Inhaltstyp erbt, die Richtlinie auf. Wenn Sie jedoch eine Informationsverwaltungsrichtlinie direkt für einen Websiteinhaltstyp erstellen, ist es schwieriger, diese Informationsverwaltungsrichtlinie in anderen Websitesammlungen wiederzuverwenden, da Richtlinien, die auf diese Weise erstellt werden, nicht exportiert werden können. 
  
![Link "Websiteinhaltstypen" auf der Seite "Websiteeinstellungen"](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
![Link zur Informationsverwaltungsrichtlinie auf der Seite "Einstellungen" für einen Websiteinhaltstyp](media/15d83a34-6c8f-4b6e-b6ee-e9b0a70cbb4b.png)
  
Hinweis um zu steuern, welche Richtlinien in einer Websitesammlung verwendet werden, können Websitesammlungsadministratoren die Möglichkeit zum Festlegen von Richtlinienfeatures für einen Inhaltstyp deaktivieren. Wenn diese Einschränkung aktiviert ist, sind Benutzer, die Inhaltstypen erstellen, auf die Auswahl von Richtlinien in der Liste websitesammlungsRichtlinien beschränkt.
  
 **Erstellen einer Informationsverwaltungsrichtlinie für eine Liste oder Bibliothek** Wenn Ihre Organisation eine bestimmte Informationsverwaltungsrichtlinie auf einen sehr begrenzten Satz von Inhalten anwenden muss, können Sie eine Informationsverwaltungsrichtlinie erstellen, die nur für eine einzelne Liste oder Bibliothek gilt. Diese Methode zum Erstellen einer Informationsverwaltungsrichtlinie ist am wenigsten flexibel, da die Richtlinie nur für einen Standort gilt und nicht für andere Speicherorte exportiert oder wieder verwendet werden kann. Manchmal müssen Sie jedoch möglicherweise eindeutige Informationsverwaltungsrichtlinien mit eingeschränkter Anwendbarkeit erstellen, um bestimmte Situationen zu beheben. 
  
![Informationsverwaltungsrichtlinien-Link auf der Seite "Einstellungen" für die Dokumentbibliothek](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
Notes 
  
Sie können eine Informationsverwaltungsrichtlinie nur für eine Liste oder Bibliothek erstellen, wenn diese Liste oder Bibliothek nicht mehrere Inhaltstypen unterstützt. Wenn eine Liste oder Bibliothek mehrere Inhaltstypen unterstützt, müssen Sie für jeden einzelnen Listeninhaltstyp, der dieser Liste oder Bibliothek zugeordnet ist, eine Informationsverwaltungsrichtlinie definieren. (Instanzen eines Websiteinhaltstyps, die einer bestimmten Liste oder Bibliothek zugeordnet sind, werden als Listeninhaltstypen bezeichnet.)
  
Um zu steuern, welche Richtlinien in einer Websitesammlung verwendet werden, können Websitesammlungsadministratoren die Möglichkeit zum Festlegen von Richtlinienfeatures für eine Liste oder Bibliothek deaktivieren. Wenn diese Einschränkung aktiviert ist, sind Benutzer, die Listen oder Bibliotheken verwalten, auf die Auswahl von Richtlinien in der Liste websitesammlungsRichtlinien beschränkt.
  
[Eine Informationsverwaltungsrichtlinie ist ein Satz von Regeln für einen Inhaltstyp. Mithilfe von Informationsverwaltungsrichtlinien können Organisationen Dinge wie lange Inhalte beibehalten oder welche Aktionen Benutzer mit diesen Inhalten ausführen können. Informationsverwaltungsrichtlinien können Organisationen dabei helfen, gesetzliche oder behördliche Bestimmungen einzuhalten, oder Sie können nur interne Geschäftsprozesse erzwingen. Beispielsweise kann eine Organisation, die den behördlichen Vorschriften folgen muss, dass Sie "angemessene Kontrollen" ihrer Abschlüsse demonstrieren, eine oder mehrere Informationsverwaltungsrichtlinien erstellen, die bestimmte Aktionen in der Erstellungs-und Genehmigungsprozess für alle Dokumente im Zusammenhang mit finanziellen Anmeldungen. Informationen zu Vorgehensweisen finden Sie unter Erstellen und Anwenden von Informationsverwaltungsrichtlinien.](intro-to-info-mgmt-policies.md#__top)
  

