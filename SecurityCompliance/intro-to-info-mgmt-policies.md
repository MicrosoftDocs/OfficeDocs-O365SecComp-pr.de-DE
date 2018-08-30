---
title: Einführung in Informationsverwaltungsrichtlinien
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/16/2014
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- WSU150
- SPO160
- OSU150
- MET150
ms.assetid: 63a0b501-ba59-44b7-a35c-999f3be057b2
description: Eine Informationsverwaltungsrichtlinie ist eine Reihe von Regeln für einen Inhaltstyp. Informationen Informationsverwaltungsrichtlinien können Organisationen und nachzuverfolgen wie lange Inhalte beibehalten werden oder welche Aktionen die Benutzer kann mit dieser Inhalte nutzen. Informationsverwaltungsrichtlinien können Organisationen rechtlichen oder behördlichen Regelungen Vorschriften helfen, oder können sie interne Geschäftsprozesse einfach erzwingen.
ms.openlocfilehash: 9ec64cd7e015acc6a7d8da324ba18cf74405cc71
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529347"
---
# <a name="introduction-to-information-management-policies"></a>Einführung in Informationsverwaltungsrichtlinien

Eine Informationsverwaltungsrichtlinie ist eine Reihe von Regeln für einen Inhaltstyp. Informationen Informationsverwaltungsrichtlinien können Organisationen und nachzuverfolgen wie lange Inhalte beibehalten werden oder welche Aktionen die Benutzer kann mit dieser Inhalte nutzen. Informationsverwaltungsrichtlinien können Organisationen rechtlichen oder behördlichen Regelungen Vorschriften helfen, oder können sie interne Geschäftsprozesse einfach erzwingen. 
  
Beispielsweise eine Organisation, die erfordern, dass sie "angemessene Steuerelemente" deren Abschluss veranschaulichen behördlichen Vorschriften einhalten muss möglicherweise Erstellen von mindestens Informationsverwaltungsrichtlinien, die überwacht werden bestimmte Aktionen in der Erstellung und Genehmigungsprozess für alle Dokumente im Zusammenhang mit Finanzdaten.
  
Gewusst wie-Informationen finden Sie unter [Erstellen und Anwenden von Informationsverwaltungsrichtlinien](create-info-mgmt-policies.md).
  
## <a name="features-of-information-management-policies"></a>Features von Informationsverwaltungsrichtlinien
<a name="__top"> </a>

Es gibt vier Hauptkategorien vordefinierte Richtlinienfeatures, die Organisationen einzeln oder in Kombination Inhalte und Prozesse verwaltet. 
  
![Typen von Inhaltsrichtlinien](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
Die überwachungsrichtlinienfeatures kann Organisationen analysieren, wie ihre Content Management-Systemen verwendet werden, indem Protokollieren von Ereignissen und Vorgänge, die in Dokumenten und Listenelementen ausgeführt werden. Sie können die überwachungsrichtlinienfeatures zum Protokollieren von Ereignissen, beispielsweise wenn ein Dokument oder Element bearbeitet wird, angezeigt, eingecheckt, ausgecheckt gelöscht, oder verfügt über die Berechtigungen geändert wurden. Alle Überwachungsinformationen in einer einzelnen Überwachungsprotokoll auf dem Server gespeichert ist, und Websiteadministratoren können Berichte auf ausführen. 
  
Das ablaufrichtlinienfeature kann Organisationen löschen oder Entfernen von veralteten Inhalt von ihren Websites in eine einheitliche und nachvollziehbare Weise. Dadurch können Sie die Kosten und Risiken im Zusammenhang mit der Beibehaltung von veralteten Inhalt verwalten. Sie können konfigurieren eine Ablaufrichtlinie, um anzugeben, dass bestimmte Inhaltstypen ablaufen, an einem bestimmten Datum oder innerhalb eines Zeitraums, nach dem das Dokument erstellt oder zuletzt geändert wurde.
  
Organisationen können auch erstellen und Bereitstellen von benutzerdefinierten Richtlinienfeatures, um bestimmte Anforderungen erfüllen. Beispiel möchten eine Organisation Fertigung eine Informationsverwaltungsrichtlinie für alle Entwurf Produkt-Design-Spezifikationsdokumente definieren, die Benutzer von drucken Kopien dieser Dokumente auf nicht sicheren Druckern verbietet. Um dieser Art von Informationsverwaltungsrichtlinie zu definieren, können Sie erstellen und Bereitstellen einer Einschränkung drucken Richtlinienfeature, die die relevanten Informationsverwaltungsrichtlinie für den Inhaltstyp Product Design Spezifikation hinzugefügt werden kann.
  
## <a name="locations-to-use-an-information-management-policy"></a>Speicherorte mithilfe eine Informationsverwaltungsrichtlinie
<a name="__toc340213528"> </a>

Um eine Informationsverwaltungsrichtlinie zu implementieren, müssen Sie es mit einer Liste, einer Bibliothek oder einer Inhaltstyp in einer Website hinzufügen. Der Speicherort, an dem Sie erstellen oder hinzufügen eine Informationsverwaltungsrichtlinie, wirkt sich auf wie weit verbreitet die Richtlinie angewendet wird, oder wie weit verbreitet dieser verwendet werden kann. Sie können:
  
 **Erstellen Sie eine Websitesammlungsrichtlinie und fügen Sie diese Richtlinie zu einem Inhaltstyp, Liste oder Bibliothek** Sie können eine Websitesammlungsrichtlinie in der Liste der Richtlinien in der Website auf oberster Ebene einer Websitesammlung erstellen. Nachdem Sie eine Websitesammlungsrichtlinie erstellt haben, können Sie sie exportieren, damit Administratoren von anderen Websitesammlungen in ihrer Liste der Richtlinien importieren können. Erstellen eine "Exportierbar" markieren Websitesammlungsrichtlinie können Sie die Informationsverwaltungsrichtlinien in die Websites in Ihrer Organisation zu standardisieren. 
  
Wenn Sie eine Websitesammlungsrichtlinie zu einem Websiteinhaltstyp hinzufügen und eine Instanz dieses Websiteinhaltstyps zu einer Liste oder Bibliothek hinzugefügt wird, kann nicht der Besitzer dieser Liste oder Bibliothek die Websitesammlungsrichtlinie für die Liste oder Bibliothek ändern. Hinzufügen, dass eine Websitesammlungsrichtlinie zu einem Websiteinhaltstyp ein geeignetes Verfahren, um diese Website Auflistung Richtlinien sicherzustellen ist auf jeder Ebene der Websitehierarchie erzwungen werden.
  
![Verknüpfung mit Inhalt Typ Richtlinienvorlage auf der Seite Websiteeinstellungen](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
 **Erstellen eine Informationsverwaltungsrichtlinie für einen Websiteinhaltstyp im Websiteinhaltstyp-Katalog der Website auf oberster Ebene, und fügen Sie diesen Inhaltstyp auf eine oder mehrere Listen oder Bibliotheken** Sie können auch eine Informationsverwaltungsrichtlinie direkt für einen Websiteinhaltstyp erstellen, und ordnen Sie anschließend eine Instanz dieses Websiteinhaltstyps mit mehreren Listen oder Bibliotheken. Wenn Sie eine Informationsverwaltungsrichtlinie auf diese Weise erstellen, verfügt jedes Element in der Websitesammlung des Inhaltstyps oder eines Inhaltstyps, das von diesem Inhaltstyp erbt die Richtlinie an. Wenn Sie eine Informationsverwaltungsrichtlinie direkt für einen Websiteinhaltstyp erstellen, es ist jedoch schwieriger zu dieser Informationsverwaltungsrichtlinie in anderen Websitesammlungen wiederzuverwenden, da Richtlinien, die auf diese Weise erstellt werden nicht exportiert werden können. 
  
![Website-Inhaltstypen Link auf der Seite Websiteeinstellungen](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
![Link auf der Einstellungsseite für einem Websiteinhaltstyp Informationsverwaltungsrichtlinie](media/15d83a34-6c8f-4b6e-b6ee-e9b0a70cbb4b.png)
  
Hinweis zu steuern, welche Richtlinien in einer Websitesammlung verwendet werden, Websitesammlungs-Administratoren können die Möglichkeit zum Festlegen von Richtlinienfeatures direkt auf einem Inhaltstyp deaktivieren. Diese Einschränkung aktiviert ist, können Benutzer, die Inhaltstypen erstellen, beschränkt die Richtlinien websitesammlungsliste Richtlinien auswählen.
  
 **Erstellen einer Informationsverwaltungsrichtlinie für eine Liste oder Bibliothek** Wenn Ihre Organisation eine sehr begrenzte Auswahl von Inhalt eine bestimmte Informationsverwaltungsrichtlinie gilt muss, können Sie eine Informationsverwaltungsrichtlinie erstellen, die nur für eine einzelne Liste oder Bibliothek gilt. Diese Methode zum Erstellen einer Informationsverwaltungsrichtlinie ist die am wenigsten flexible, da die Richtlinie nur für einen Speicherort gilt und nicht exportiert oder für andere Speicherorte wiederverwendet. Jedoch müssen in einigen Fällen Sie eindeutigen Informationen erstellen Informationsverwaltungsrichtlinien mit begrenzten Anwendungsmöglichkeiten bestimmte Situationen zu behandeln. 
  
![Informationslink Management Richtlinien auf der Einstellungsseite für die Dokumentbibliothek](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
Notes 
  
Sie können eine Informationsverwaltungsrichtlinie für eine Liste oder Bibliothek erstellen, nur, wenn dieser Liste oder Bibliothek nicht mehrere Inhaltstypen unterstützt. Wenn eine Liste oder Bibliothek mehrere Inhaltstypen unterstützt, müssen Sie eine Informationsverwaltungsrichtlinie für jeden einzelnen Listeninhaltstyp definieren, die dieser Liste oder Bibliothek zugeordnet ist. (Instanzen von einem Websiteinhaltstyp, die eine bestimmte Liste oder Bibliothek zugeordnet sind, werden als Listeninhaltstypen bezeichnet.)
  
Um zu steuern, welche Richtlinien in einer Websitesammlung verwendet werden, können die Websitesammlungs-Administratoren die Möglichkeit zum Festlegen von Richtlinienfeatures direkt auf einer Liste oder Bibliothek deaktivieren. Diese Einschränkung aktiviert ist, können Benutzer, die Listen oder Bibliotheken verwalten beschränkt die Richtlinien websitesammlungsliste Richtlinien auswählen.
  
[Eine Informationsverwaltungsrichtlinie ist eine Reihe von Regeln für einen Inhaltstyp. Informationen Informationsverwaltungsrichtlinien können Organisationen und nachzuverfolgen wie lange Inhalte beibehalten werden oder welche Aktionen die Benutzer kann mit dieser Inhalte nutzen. Informationsverwaltungsrichtlinien können Organisationen rechtlichen oder behördlichen Regelungen Vorschriften helfen, oder können sie interne Geschäftsprozesse einfach erzwingen. Beispielsweise eine Organisation, die erfordern, dass sie "angemessene Steuerelemente" deren Abschluss veranschaulichen behördlichen Vorschriften einhalten muss möglicherweise Erstellen von mindestens Informationsverwaltungsrichtlinien, die überwacht werden bestimmte Aktionen in der Erstellung und Genehmigungsprozess für alle Dokumente im Zusammenhang mit Finanzdaten. Weitere Informationen finden Sie unter Erstellen und Anwenden von Informationsverwaltungsrichtlinien.](intro-to-info-mgmt-policies.md#__top)
  

