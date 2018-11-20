---
title: Erstellen eines benutzerdefinierten Typs für vertrauliche Informationen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Erfahren Sie, wie Sie benutzerdefinierten Typen für vertrauliche Informationen für DLP in der grafischen Benutzeroberfläche in Office 365 Security & Compliance Center erstellen, ändern, entfernen und testen.
ms.openlocfilehash: a9234b160d720a04ff6bfeac62899246500ec9b4
ms.sourcegitcommit: e4291f751d6870d965dba191b4c8f10c5c4ce0b5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2018
ms.locfileid: "26534026"
---
# <a name="create-a-custom-sensitive-information-type"></a>Erstellen eines benutzerdefinierten Typs für vertrauliche Informationen

Die Verhinderung von Datenverlust (Data Loss Prevention, DLP) in Office 365 umfasst zahlreiche integrierte [Typen vertraulicher Informationen](what-the-sensitive-information-types-look-for.md), die Sie in DLP-Richtlinien verwenden können. Diese integrierten Typen unterstützen Sie beim Erkennen und Schützen von Kreditkartennummern, Bankkontonummern, Reisepassnummern und mehr. 

Wenn Sie jedoch verschiedene Typen vertraulicher Informationen identifizieren und schützen müssen, zum Beispiel Mitarbeiter-IDs oder Projektnummern, die ein für Ihre Organisation spezifisches Format verwenden, können Sie einen benutzerdefinierten Typ für vertrauliche Informationen erstellen.

Die grundlegenden Bestandteile eines benutzerdefinierten Typs für vertrauliche Informationen sind wie folgt:

- **Primäres Muster**: Mitarbeiter-ID-Nummer, Projektnummern usw. Dieses wird in der Regel durch einen regulären Ausdruck (RegEx) gekennzeichnet, kann aber auch eine Liste von Schlüsselwörtern sein.

- **Zusätzliche Nachweise**: Angenommen, Sie suchen nach einer neunstelligen Mitarbeiter-ID-Nummer. Nicht alle neunstelligen ID-Nummern sind Mitarbeiter-ID-Nummern, Sie können daher nach zusätzlichem Text suchen: Schlüsselwörter wie „Mitarbeiter“, „Ausweis“, „ID“ oder andere Textmuster basierend auf zusätzlichen regulären Ausdrücken. Diese Nachweise (auch bezeichnet als _unterstützende_ oder _bestätigende_ Nachweise) erhöhen die Wahrscheinlichkeit, dass die neunstellige Nummer, die in Inhalten gefunden wird, auch wirklich eine Mitarbeiter-ID-Nummer ist.

- **Zeichenabstand**: Je näher sich das primäre Muster an den unterstützenden Nachweisen befindet, desto größer ist die Wahrscheinlichkeit, dass die gefundenen Inhalte den von Ihnen gesuchten Inhalten entsprechen. Sie können den Zeichenabstand zwischen dem primären Muster und den unterstützenden Nachweisen angeben (auch als _Näherungsfenster_ bezeichnet), wie in der folgenden Abbildung dargestellt:

    ![Diagramm von bestätigenden Nachweisen und Näherungsfenster](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- **Zuverlässigkeitsgrad**: Je mehr unterstützende Nachweise Sie haben, desto höher die Wahrscheinlichkeit, dass eine Übereinstimmung die vertraulichen Informationen enthält, die Sie suchen. Sie können höhere Zuverlässigkeitsstufen für Übereinstimmungen zuweisen, die gefunden werden, indem Sie mehr Nachweise verwenden.

  Wenn eine Übereinstimmung gefunden wurde, gibt ein Muster eine Anzahl und einen Zuverlässigkeitsgrad zurück, die bzw. den Sie in den Bedingungen Ihrer DLP-Richtlinien verwenden können. Wenn Sie eine Bedingung zum Erkennen eines Typs vertraulicher Informationen zu einer DLP-Richtlinie hinzufügen, können Sie die Anzahl und den Zuverlässigkeitsgrad wie in der folgenden Abbildung dargestellt bearbeiten:

    ![Instanzenanzahl und Optionen für die Übereinstimmungsgenauigkeit](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

Zum Erstellen von benutzerdefinierten Typen für vertrauliche Informationen im Office 365 Security & Compliance Center stehen Ihnen die folgenden Optionen zur Verfügung:

- **Verwenden der Benutzeroberfläche**: Diese Methode ist schneller und einfacher, aber Sie haben weniger Konfigurationsoptionen als bei PowerShell. Im restlichen Thema werden diese Verfahren beschrieben.

- **Verwenden von PowerShell**: Diese Methode setzt voraus, dass Sie zuerst eine XML-Datei erstellen (bezeichnet als _Regelpaket_), die einen oder mehrere Typen von vertraulichen Informationen enthält. Sie verwenden dann PowerShell, um das Regelpaket zu importieren (das Importieren des Regelpakets ist einfach im Vergleich zum Erstellen des Regelpakets). Diese Methode ist wesentlich komplexer als die Verwendung der Benutzeroberfläche, aber Sie haben mehr Konfigurationsoptionen. Anweisungen finden Sie unter [Erstellen eines benutzerdefinierten Typs für vertrauliche Informationen in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).

Die wichtigsten Unterschiede werden in der folgenden Tabelle näher erläutert:

|**Benutzerdefinierte Typen für vertrauliche Informationen in der Benutzeroberfläche**|**Benutzerdefinierte Typen für vertrauliche Informationen in PowerShell**|
|:-----|:-----|
|Name und Beschreibung sind in einer Sprache.|Unterstützt mehrere Sprachen für Name und Beschreibung.|
|Unterstützt ein Muster.|Unterstützt mehrere Muster.|
|Unterstützende Nachweise können Folgendes sein: <br/>• Reguläre Ausdrücke <br/>• Schlüsselwörter <br/>• Schlüsselwörterbücher|Unterstützende Nachweise können Folgendes sein: <br/>• Reguläre Ausdrücke <br/>• Schlüsselwörter <br/>• Schlüsselwörterbücher <br/>• [Integrierte DLP-Funktionen](what-the-dlp-functions-look-for.md)|
|Benutzerdefinierte Typen vertraulicher Informationen werden zum Regelpaket namens Microsoft.SCCManaged.CustomRulePack hinzugefügt.|Sie können bis zu 10 Regelpakete erstellen, die benutzerdefinierten Typen vertraulicher Informationen enthalten.|
|Die Musterübereinstimmung erfordert die Erkennung des primären Musters und aller unterstützenden Nachweise (der implizite UND-Operator wird verwendet).|Die Musterübereinstimmung erfordert die Erkennung des primären Musters und einer konfigurierbaren Menge unterstützender Nachweise (implizite UND- und ODER-Operatoren können verwendet werden).|

## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

- Informationen zum Öffnen des Security & Compliance Center finden Sie unter [Wechseln zum Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).

- Benutzerdefinierte Typen für vertrauliche Informationen erfordern Kenntnisse über reguläre Ausdrücke (RegEx). Weitere Informationen über das Modul Boost.RegEx (vormals als RegEx++ bezeichnet), das für die Textverarbeitung verwendet wird, finden Sie unter [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).

  Der Kundendienst und Support von Microsoft kann beim Bereitstellen von benutzerdefinierten Definitionen für die Inhaltsübereinstimmung (Erstellen benutzerdefinierter Klassifizierungen oder Muster für reguläre Ausdrücke) keine Unterstützung anbieten. Die Supportmitarbeiter können eingeschränkten Support für das Feature bereitstellen (z. B. Bereitstellen von Mustern für reguläre Ausdrücke zu Testzwecken oder Hilfestellung bei der Problembehandlung eines bestehenden Musters für reguläre Ausdrücke, das nicht wie erwartet ausgelöst wird), es können jedoch keine Zusicherungen dahingehend gegeben werden, dass benutzerdefinierte Entwicklungen für die Inhaltsübereinstimmung Ihre Anforderungen oder Verpflichtungen erfüllen.

- DLP verwendet den Suchcrawler zum Erkennen und Klassifizieren vertraulicher Informationen in SharePoint Online- und OneDrive for Business-Websites. Um Ihren neuen benutzerdefinierten Typ vertraulicher Informationen in vorhandenen Inhalten zu identifizieren, muss der Inhalt erneut durchforstet werden. Inhalte werden basierend auf einem Zeitplan erneut durchforstet, Sie können aber Inhalte für eine Websitesammlung, eine Liste oder eine Bibliothek manuell erneut durchforsten. Weitere Informationen finden Sie unter [Manuelles Anfordern einer Durchforstung und erneutes Indizieren einer Website, einer Bibliothek oder einer Liste](https://docs.microsoft.com/sharepoint/crawl-site-content).

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a>Erstellen von benutzerdefinierten Typen für vertrauliche Informationen im Security & Compliance Center

Wechseln Sie im Security & Compliance Center zu **Klassifizierungen** \> **Typen vertraulicher Informationen**, und klicken Sie auf **Erstellen**.

Die Einstellungen sind selbsterklärend und werden auf der entsprechenden Seite des Assistenten erläutert:

- **Name**

- **Beschreibung**

- **Näherung**

- **Zuverlässigkeitsstufe**

- **Primäres Muster-Element** (Schlüsselwörter, reguläre Ausdrücke oder Wörterbuch)

- Optionale Elemente für **unterstützende Muster** (Schlüsselwörter, reguläre Ausdrücke oder Wörterbuch) und einen entsprechenden Wert für **Mindestkosten**.

Sehen Sie sich das folgende Szenario an: Sie möchten einen benutzerdefinierten Typ für vertrauliche Informationen, der neunstellige Mitarbeiternummern in Inhalten erkennt, zusammen mit den Schlüsselwörtern „Mitarbeiter“, „ID“ und „Ausweis“. Um diesen benutzerdefinierten Typ für vertrauliche Information zu erstellen, führen Sie die folgenden Schritte aus:

1. Wechseln Sie im Security & Compliance Center zu **Klassifizierungen** \> **Typen vertraulicher Informationen**, und klicken Sie auf **Erstellen**.

    ![Speicherort der Typen für vertrauliche Informationen und Schaltfläche „Erstellen“](media/scc-cust-sens-info-type-new.png)

2. Geben Sie auf der Seite **Namen und Beschreibung auswählen**, die geöffnet wird, die folgenden Werte ein:

  - **Name**: Mitarbeiter-ID.

  - **Beschreibung**: Neunstellige Contoso-Mitarbeiter-ID-Nummern erkennen.

    ![Seite „Name und Beschreibung“](media/scc-cust-sens-info-type-new-name-desc.png)

    Klicken Sie nach Abschluss des Vorgangs auf **Weiter**.

3. Klicken Sie auf der Seite **Anforderungen für Übereinstimmung** auf **Element hinzufügen**, um die folgenden Einstellungen zu konfigurieren:

    - **Inhalt erkennen, der Folgendes enthält**:
 
      a. Klicken Sie auf die Option, dass **eines der folgenden Elemente enthalten sein muss**, und wählen Sie **Regulärer Ausdruck** aus.

      b. Geben Sie in dem Feld für den regulären Ausdruck `(\s)(\d{9})(\s)` ein (neunstellige Zahlen umgeben von einem Leerzeichen).
  
    - **Unterstützende Elemente**: Klicken Sie auf **Unterstützende Elemente hinzufügen**, und wählen Sie **Enthält die folgende Schlüsselwortliste** aus.

    - Konfigurieren Sie in dem Bereich **Enthält die folgende Schlüsselwortliste**, der angezeigt wird, die folgenden Einstellungen:

      - **Schlüsselwortliste**: Geben Sie den folgenden Wert ein: Mitarbeiter,ID,Ausweis.

      - **Mindestanzahl**: Behalten Sie den Standardwert 1 bei.

    - Behalten Sie den Standardwert 60 für den **Zuverlässigkeitsgrad** bei. 

    - Behalten Sie den Standardwert 300 für den **Zeichenabstand** bei.

    ![Seite „Anforderungen für Übereinstimmung“](media/scc-cust-sens-info-type-new-reqs.png)

    Klicken Sie nach Abschluss des Vorgangs auf **Weiter**.

4. Überprüfen Sie auf der Seite **Überprüfen und Abschließen** die Einstellungen, und klicken Sie auf **Fertig stellen**.

    ![Seite „Überprüfen und Abschließen“](media/scc-cust-sens-info-type-new-review.png)

5. Auf der nächsten Seite werden Sie aufgefordert, den neuen benutzerdefinierten Typ für vertrauliche Informationen zu testen. Klicken Sie dazu auf **Ja**. Weitere Informationen finden Sie unter [Testen von benutzerdefinierten Typen für vertrauliche Information im Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center). Um die Regel später zu testen, klicken Sie auf **Nein**.

    ![Testempfehlungsseite](media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Um sicherzustellen, dass Sie einen neuen Typ für vertrauliche Informationen erstellt haben, führen Sie einen der folgenden Schritte aus:

  - Wechseln Sie zu **Klassifizierungen** \> **Typen vertraulicher Informationen**, und bestätigen Sie, dass der neue benutzerdefinierte Typ für vertrauliche Informationen aufgeführt ist.

  - Testen Sie den neuen benutzerdefinierten Typ für vertrauliche Informationen. Weitere Informationen finden Sie unter [Testen von benutzerdefinierten Typen für vertrauliche Informationen im Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a>Ändern von benutzerdefinierten Typen für vertrauliche Information im Security & Compliance Center

**Hinweise**:

- Sie können nur benutzerdefinierte Typen für vertrauliche Informationen ändern; integrierte Typen vertraulicher Informationen können nicht geändert werden. Sie können aber PowerShell verwenden, um integrierte Typen vertraulicher Informationen zu exportieren, diese anzupassen und sie als benutzerdefinierte Typen vertraulicher Informationen zu importieren. Weitere Informationen finden Sie unter [Anpassen eines integrierten benutzerdefinierten Typs für vertrauliche Informationen](customize-a-built-in-sensitive-information-type.md).

- Sie können nur benutzerdefinierte Typen für vertrauliche Informationen ändern, die Sie in der Benutzeroberfläche erstellt haben. Wenn Sie das [PowerShell-Verfahren](create-a-custom-sensitive-information-type-in-scc-powershell.md) zum Importieren eines Regelpakets für benutzerdefinierte Typen für vertrauliche Informationen verwendet haben, erhalten Sie eine Fehlermeldung.

Wechseln Sie im Security & Compliance Center zu **Klassifizierungen** \> **Typen vertraulicher Informationen**, und wählen Sie den benutzerdefinierten Typ vertraulicher Informationen aus, den Sie ändern möchten. Klicken Sie anschließend auf **Bearbeiten**.

  ![Speicherort der Typen für vertrauliche Informationen und Schaltfläche „Bearbeiten“](media/scc-cust-sens-info-type-edit.png)

Hier stehen die gleichen Optionen wie beim Erstellen des benutzerdefinierten Typs für vertrauliche Informationen im Security & Compliance Center zur Verfügung. Weitere Informationen finden Sie unter [Erstellen von benutzerdefinierten Typen für vertrauliche Informationen im Security & Compliance Center](#create-custom-sensitive-information-types-in-the-security--compliance-center).

### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Um sicherzustellen, dass Sie einen neuen Typ für vertrauliche Informationen erfolgreich geändert haben, führen Sie einen der folgenden Schritte aus:

  - Wechseln Sie zu **Klassifizierungen** \> **Typen vertraulicher Informationen**, um die Eigenschaften des geänderten benutzerdefinierten Typs vertraulicher Informationen zu überprüfen. 

  - Testen Sie den geänderten benutzerdefinierten Typ für vertrauliche Informationen. Weitere Informationen finden Sie unter [Testen von benutzerdefinierten Typen für vertrauliche Informationen im Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a>Entfernen von benutzerdefinierten Typen für vertrauliche Informationen im Security & Compliance Center 

**Hinweise**:

- Sie können nur benutzerdefinierte Typen für vertrauliche Informationen entfernen; Sie können keine integrierten Typen vertraulicher Informationen entfernen.

- Bevor Sie einen benutzerdefinierten Typ für vertrauliche Informationen entfernen, überprüfen Sie, dass keine DLP-Richtlinien oder Exchange-Nachrichtenflussregeln (auch bezeichnet als Transportregeln) mehr auf den Typ vertraulicher Informationen verweisen.

1. Wechseln Sie im Security & Compliance Center zu **Klassifizierungen** \> **Typen vertraulicher Informationen**, und wählen Sie einen oder mehrere benutzerdefinierte Typen vertraulicher Informationen aus, die Sie entfernen möchten.

2. Klicken Sie in dem Fenster, das geöffnet wird, auf **Löschen** (oder auf **Typen vertraulicher Informationen löschen**, wenn Sie mehrere ausgewählt haben).

    ![Speicherort der Typen für vertrauliche Informationen und Schaltfläche „Löschen“](media/scc-cust-sens-info-type-delete.png)

3. Klicken Sie in der angezeigten Warnmeldung auf **Ja**.

### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Um sicherzustellen, dass Sie einen benutzerdefinierten Typ vertraulicher Informationen erfolgreich entfernt haben, wechseln Sie zu **Klassifizierungen** \> **Typen vertraulicher Informationen**, und bestätigen Sie, dass der benutzerdefinierte Typ vertraulicher Informationen nicht mehr aufgeführt ist.

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a>Testen von benutzerdefinierten Typen für vertrauliche Informationen im Security & Compliance Center

1. Wechseln Sie im Security & Compliance Center zu **Klassifizierungen** \> **Typen vertraulicher Informationen**.

2. Wählen Sie einen oder mehrere benutzerdefinierte Typen vertraulicher Informationen aus, die Sie testen möchten. Klicken Sie in dem Fenster, das geöffnet wird, auf **Typ testen** (oder auf **Typen vertraulicher Informationen testen**, wenn Sie mehrere ausgewählt haben).

    ![Speicherort der Typen für vertrauliche Informationen und Schaltfläche „Typ testen“](media/scc-cust-sens-info-type-test.png)

3. Laden Sie auf der Seite **Zu testende Datei hochladen**, die geöffnet wird, per Drag & Drop ein zu testendes Dokument hoch, oder klicken Sie auf **Durchsuchen**, und wählen Sie eine Datei aus.

    ![Seite „Zu testende Datei hochladen“](media/scc-cust-sens-info-type-test-upload.png)

4. Klicken Sie auf die Schaltfläche **Testen**, um das Dokument auf Musterübereinstimmungen in der Datei zu testen.

5. Klicken Sie auf der Seite **Übereinstimmungsergebnisse** auf **Fertig stellen**.

    ![Übereinstimmungsergebnisse](media/scc-cust-sens-info-type-test-results.png)