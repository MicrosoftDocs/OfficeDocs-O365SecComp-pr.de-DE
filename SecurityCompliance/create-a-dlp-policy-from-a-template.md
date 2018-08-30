---
title: Erstellen einer DLP-Richtlinie aus einer Vorlage
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'Die einfachste und am häufigsten verwendete Methode zum Einstieg in DLP-Richtlinien ist die Verwendung der Vorlagen in Office 365 enthalten. '
ms.openlocfilehash: 4e3a5d731538e4998858b5f9f7a296c43e6774ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529505"
---
# <a name="create-a-dlp-policy-from-a-template"></a>Erstellen einer DLP-Richtlinie aus einer Vorlage

Die einfachste und am häufigsten verwendete Methode zum Einstieg in DLP-Richtlinien ist die Verwendung der Vorlagen in Office 365 enthalten. Sie können eine dieser Vorlagen unverändert verwenden oder zur Anpassung der Regeln für Ihre Organisation bestimmte gesetzliche Vorschriften zu erfüllen.
  
Office 365 umfasst mehr als 40 verwendungsbereite Vorlagen, mit denen Sie eine Vielzahl von allgemeinen behördlichen und geschäftlichen Richtlinienanforderungen erfüllen können. Es gibt z. B. DLP-Richtlinienvorlagen für:
  
- Gramm-Leach-Bliley Act (GLBA)
    
- Payment Card Industry Data Security Standard (PCI-DSS)
    
- United States Personally Identifiable Information (U.S. PII)
    
- United States Health Insurance Act (HIPAA)
    
Sie können eine Vorlage anpassen, indem Sie eine vorhandene Regel ändern oder neue hinzufügen. Beispielsweise können Sie neue Arten von vertraulichen Informationen zu einer Regel hinzufügen oder die Anzahl in einer Regel ändern, damit sie leichter oder schwerer ausgelöst wird. Sie können es auch Benutzern ermöglichen, die Aktionen in einer Regel anhand einer geschäftlichen Begründung außer Kraft zu setzen oder ändern, an wen Benachrichtigungen und Schadensberichte gesendet werden. Eine DLP-Richtlinienvorlage ist ein flexibler Ausgangspunkt für viele gängige Compliance-Szenarien.
  
Sie können auch die benutzerdefinierte Vorlage auswählen, die über keine Standardregeln verfügt, und die DLP-Richtlinie von Grund auf neu konfigurieren, um die spezifischen Vorschriften für Ihre Organisation einzuhalten.
  
## <a name="example-identify-sensitive-information-across-all-onedrive-for-business-sites-and-restrict-access-for-people-outside-your-organization"></a>Beispiel: Identifizieren Sie vertraulichen Informationen über alle OneDrive for Business-Websites und schränken Sie des Zugriffs für Personen außerhalb Ihrer Organisation ein

OneDrive for Business-Konten erleichtern für Personen innerhalb Ihrer Organisation zur Zusammenarbeit und Freigabe von Dokumenten. Eine allgemeine hinsichtlich der Compliance-beauftragte ist jedoch, dass vertraulicher Informationen gespeichert in OneDrive for Business-Konten versehentlich mit Personen außerhalb Ihrer Organisation gemeinsam genutzt werden kann. Eine DLP-Richtlinie kann diese Risiken helfen.
  
In diesem Beispiel erstellen Sie eine DLP-Richtlinie, die US PII-Daten identifiziert die einzelnen Steuernummer Identification Zahlen (ITIN), Sozialversicherungsnummern und US Ausweisnummern enthält. Sie benötigen steigen mithilfe einer Vorlage, und ändern Sie die Vorlage, um Ihrer Organisation Auflagen – insbesondere benötigen Sie:
  
- Fügen Sie eine Reihe von Typen von vertraulichen information—U.S. Bankkonto Zahlen und US Führerscheinnummer –, damit die DLP-Richtlinie noch mehr Ihre sensiblen Daten geschützt.
    
- Stellen Sie die Richtlinie mehr vertrauliche, damit ein einzelnes Vorkommen des vertrauliche Informationen zum Einschränken des Zugriffs für externe Benutzer ausreicht.
    
- Ermöglicht es Benutzern, die Aktionen außer Kraft gesetzt, durch das als Rechtfertigung oder falsch positives Ergebnis melden. Auf diese Weise wird nicht die DLP-Richtlinie Personen in Ihrer Organisation arbeiten, abrufen, vorausgesetzt, sie verfügen über einen gültigen Business Grund für die Freigabe von vertraulichen Informationen verhindern.
    
### <a name="create-a-dlp-policy-from-a-template"></a>Erstellen einer DLP-Richtlinie aus einer Vorlage

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365. Sie sind jetzt in die Office 365-Sicherheit &amp; Compliance Center.
    
3. In das Wertpapier &amp; Compliance Center \> linke Navigationsleiste \> **Verhinderung von Datenverlust** \> **Richtlinie** \> **+ Richtlinie erstellen**.
    
    ![Erstellen einer Richtlinie-Schaltfläche](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Wählen Sie die DLP-Richtlinienvorlage, die die Arten von vertraulichen Informationen, die Sie benötigen, schützt \> **Weiter**.
    
    In diesem Beispiel wählen Sie **private** \> **US persönlich identifizierbare Informationen (PII) Daten** , da es bereits die meisten der Arten von vertraulichen Informationen enthält, die Sie schützen möchten – Sie müssen ein paar später hinzufügen. 
    
    Wenn Sie eine Vorlage auswählen, können Sie die Beschreibung für das Recht, erfahren, welche Arten von vertraulichen Informationen der Vorlage schützt lesen.
    
    ![Seite zur Auswahl einer DLP-Richtlinienvorlage](media/775266f6-ad87-4080-8d7c-97f2e7403b30.png)
  
5. Benennen Sie die Richtlinie \> **Weiter**.
    
6. Die Speicherorte auswählen die gewünschte die DLP-Richtlinie zu schützen, eine der folgenden Aktionen aus:
    
  - Wählen Sie **Alle Speicherorte in Office 365** \> **Weiter**.
    
  - Wählen Sie **selbst bestimmte Orte auswählen** \> **Weiter**. Wählen Sie diese Option aus, in diesem Beispiel.
    
    Wechseln Sie zum einbeziehen oder ausschließen einen gesamten Standort wie alle Exchange-e-Mail oder alle OneDrive-Konten, den **Status** von diesem Speicherort aktiviert oder deaktiviert. 
    
    Nur bestimmte SharePoint-Websites oder OneDrive for Business-Konten aufnehmen möchten, wechseln Sie auf den **Status** auf, und klicken Sie dann auf die Links unter **einschließen** , um bestimmte Standorte oder Konten auszuwählen. Wenn Sie Anwenden einer Richtlinie auf einer Website, die Regeln, die so konfiguriert, dass Richtlinie automatisch auf alle Unterwebsites dieser Website angewendet werden. 
    
    ![Optionen für Speicherorte, an denen eine DLP-Richtlinie angewendet werden kann](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
    In diesem Beispiel wird um vertrauliche Informationen gespeichert, die in allen OneDrive for Business-Konten zu schützen, deaktivieren Sie den **Status** für **Exchange-e-Mail-** und **SharePoint-Websites**, und lassen Sie den **Status** auf für **OneDrive-Konten**.
    
7. **Verwenden Sie den erweiterten Einstellungen** auswählen \> **Weiter**.
    
8. Eine DLP-Richtlinienvorlage enthält vordefinierte Regeln mit Bedingungen und Aktionen, die erkennen und bestimmte Arten von vertraulichen Informationen zu bearbeiten. Sie können bearbeiten, löschen, oder eine vorhandene Regel deaktivieren oder neue hinzufügen. Klicken Sie dann auf **Weiter**.
    
    ![Regeln in uns PII Richtlinienvorlage erweitert](media/3bc9f1b6-f8ad-4334-863a-24448bb87687.png)
  
    In diesem Beispiel enthält die US PII Datenvorlage zwei vordefinierte Regeln:
    
  - **Geringe Anzahl von Inhalten US PII erkannt** Diese Regel sucht nach Dateien, die zwischen 1 und 10 Vorkommen jedes der drei Arten von vertraulichen Informationen (ITIN, SSN und US Passport Numbers), in dem die Dateien mit Personen außerhalb der Organisation gemeinsam genutzt werden. Wenn gefunden, die Regel eine e-Mail-Benachrichtigung an den primären Websitesammlungsadministrators Besitzer des Dokuments sendet, und die Person, die zuletzt, das Dokument geändert. 
    
  - **Große Menge von Inhalten US PII erkannt** Diese Regel sucht nach Dateien mit 10 oder mehr Vorkommen eines einzelnen gleichen drei Arten der vertraulichen Informationen, wobei die Dateien mit Personen außerhalb der Organisation gemeinsam genutzt werden. Wenn gefunden, wird diese Aktion auch eine e-Mail-Benachrichtigung sendet, plus es schränkt den Zugriff auf die Datei. Nach Inhalten in einer OneDrive for Business-Konto bedeutet dies, dass die Berechtigungen für das Dokument sind für alle Benutzer mit Ausnahme der primärer Administrator der Websitesammlung, der Besitzer des Dokuments und der Person, die das Dokument zuletzt geändert. 
    
    Um bestimmte Anforderungen Ihrer Organisation zu erfüllen, sollten Sie die Regeln Trigger vereinfachen, damit ein einzelnes Vorkommen des vertrauliche Informationen ausreichen Blockieren des Zugriffs für externe Benutzer ist. Betrachten Sie diese Regeln, Sie verstehen, dass Sie nicht die Höchst- und Count Regeln benötigen – benötigen Sie nur eine Regel, die den Zugriff blockiert, wenn jedes Vorkommen von vertraulichen Informationen gefunden werden kann.
    
    So erweitern Sie die Regel mit dem Namen **geringem Umfang des Inhalts erkannt US PII** \> **Regel zu löschen**.
    
    ![Regel-Schaltfläche "löschen"](media/bc36f7d2-0fae-4af1-92e8-95ba51077b12.png)
  
9. Jetzt in diesem Beispiel müssen Sie zwei Typen vertraulicher Informationen (US-Bank Account Zahlen und US Führerscheinnummer) hinzufügen zulassen von Personen zu eine Regel außer Kraft setzen und ändern die Anzahl die für jedes auftreten. Sie können all diese Aufgaben durch eine Regel bearbeiten müssen, wählen Sie **große Menge von Inhalten US PII erkannt** \> **Regel bearbeiten**.
    
    ![Schaltfläche Regel bearbeiten](media/eaf54067-4945-4c98-8dd6-fb2c5d6de075.png)
  
10. Einen Typ vertrauliche Informationen im Abschnitt **Bedingungen** hinzufügen \> **Typen hinzufügen oder ändern**. Klicken Sie dann unter **Hinzufügen oder Ändern von Typen** \> wählen Sie **Hinzufügen** \> wählen **US Bankkontonummer** und **US Führerscheinnummer** \> **Hinzufügen** \> **durchgeführt**.
    
    ![Option zum Hinzufügen oder Ändern von Typen](media/c6c3ae86-f7db-40a8-a6e4-db11692024be.png)
  
    ![Hinzufügen oder Ändern von Bereich Projekttypen an](media/fdbb96af-b914-4a6c-a97b-bbd014689965.png)
  
11. Zum Ändern der Anzahl (die Anzahl der Instanzen von vertraulichen Informationen, die erforderlich sind, um die Regel), klicken Sie unter **Anzahl der Instanzen** \> wählen Sie den Wert **min** , für die einzelnen \> Geben Sie 1 ein. Die minimale Anzahl darf nicht leer sein. Die maximale Anzahl kann leer sein. ein leeres **max** -Wert in **eine beliebige**konvertieren.
    
    Nach Abschluss der min Count für alle Arten der vertraulichen Informationen sollte **1** und der maximalen Anzahl sollten **Alle**. Jedes Vorkommen von dieser Art von vertraulichen Informationen, mit anderen Worten, diese Bedingung erfüllen.
    
    ![Anzahl der Instanz Typen vertraulicher Informationen](media/5c6e08cb-59a9-4558-b54b-d899836d4737.png)
  
12. Für die endgültige Anpassung möchten Sie nicht Ihrer DLP-Richtlinien zum Blockieren von Personen aus ihrer Arbeit ausführen, wenn sie als Rechtfertigung ungültig haben oder falsch positives Ergebnis auftreten, damit die Benutzer Benachrichtigung Optionen, um die durchzuführende Aktion außer Kraft setzen eingeschlossen werden soll.
    
    Klicken Sie im Abschnitt **Benutzer Benachrichtigungen** sehen Sie sich, dass e-Mail-Benachrichtigungen und richtlinientipps für diese Regel in der Vorlage in der Standardeinstellung aktiviert sind. 
    
    Klicken Sie im Abschnitt **Benutzer überschreibt** sehen Sie sich, dass Außerkraftsetzungen für als Rechtfertigung sind eingeschaltet, Außerkraftsetzungen falsch positive Ergebnisse gemeldet sind jedoch nicht. Wählen Sie **die Regel überschreiben, automatisch, wenn sie es als falsch positives Ergebnis melden**.
    
    ![Im Abschnitt Benutzer Benachrichtigungen und Benutzer überschreibt Abschnitt](media/62720e7a-a939-4c03-b414-67748f3d64a0.png)
  
13. Am oberen Rand der Regeleditor ändern Sie den Namen dieser Regel aus der Standard- **große Menge von Inhalten erkannt US PII** auf **alle Inhalte mit US PII erkannt** , da nun durch jedes Vorkommen von dessen vertraulichen Informationstypen ausgelöst wird. 
    
14. Am unteren Rand des Editors Regel \> **Speichern**.
    
15. Überprüfen Sie die Bedingungen und Aktionen für diese Regel \> **Weiter**.
    
    Beachten Sie auf der rechten Seite den **Status** für die Regel zu wechseln. Wenn Sie eine ganze Richtlinie deaktivieren, werden auch alle in der Richtlinie enthaltenen Regeln deaktiviert. Jedoch können hier finden Sie eine bestimmte Regel deaktivieren ohne die gesamte Richtlinie auszuschalten. Dies kann hilfreich sein, wenn Sie benötigen, um eine Regel zu untersuchen, die eine große Anzahl von falsch positive Ergebnisse generiert. 
    
16. Auf der nächsten Seite lesen und verstehen, die folgenden, und wählen Sie dann, ob die Regel zu aktivieren oder testen sie auszuchecken \> **Weiter**.
    
     Bevor Sie Ihre DLP-Richtlinien erstellen, sollten Sie erwägen, Bereitstellung der Schulungsunterlagen schrittweise deren Einfluss bewerten und Effektivität zu testen, bevor Sie vollständig erzwingen. Sie möchten beispielsweise keine neue DLP-Richtlinie zum versehentlich Blockieren des Zugriffs auf Tausenden von Dokumenten, die Personen für ihre Arbeit vermitteln erfordern. 
    
    Wenn Sie möglicherweise eine große Auswirkung DLP-Richtlinien erstellen, sollten in den folgenden Schritten folgen:
    
17. Beginnen Sie im Testmodus ohne Richtlinientipps, und werten Sie die Auswirkungen dann anhand der DLP-Berichte aus. In den DLP-Berichten werden die Anzahl von Richtlinienübereinstimmungen, der Ort des Vorkommens, der Typ und der Schweregrad aufgeführt. Auf Grundlage der Ergebnisse können Sie die Regeln nach Bedarf genauer anpassen. Im Testmodus haben DLP-Richtlinien keinen Einfluss auf die Produktivität der Mitarbeiter in Ihrer Organisation. 
    
18. Fahren Sie im Testmodus mit Benachrichtigungen und Richtlinientipps fort, sodass Sie die Benutzer über die Einhaltungsrichtlinien in Kenntnis setzen und auf die Anwendung der Regeln vorbereiten können. In dieser Phase können Sie die Benutzer auch bitte, Sie über falsche Positivmeldungen zu benachrichtigen, damit Sie die Regeln noch besser abstimmen können.
    
19. Aktivieren Sie die Richtlinien, damit die Regeln erzwungen werden, und der Inhalt der geschützte. Überwachen der DLP-Berichte und Vorfall Berichte oder Benachrichtigungen, um sicherzustellen, dass die Ergebnisse sind, was Sie beabsichtigen weiterhin. 
    
    ![Optionen für die Verwendung des Testmodus und das Einschalten der Richtlinie](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
20. Überprüfen Sie die Einstellungen für diese Richtlinie \> wählen Sie **Erstellen**aus.
    
Nach dem Erstellen und einer DLP-Richtlinie zu aktivieren, wird es auf alle Inhaltsquellen, die er, wie SharePoint Online-Websites oder OneDrive for Business-Konten enthält, bereitgestellt, an dem die Richtlinie beginnt automatisch die Regeln auf diesen Inhalt durchsetzen.
  
## <a name="view-the-status-of-a-dlp-policy"></a>Anzeigen des Status einer DLP-Richtlinie

Sie können den Status Ihrer DLP-Richtlinien zu einem beliebigen Zeitpunkt anzeigen, auf der Seite **Richtlinie** im Abschnitt **Verhinderung von Datenverlust** der Sicherheit &amp; Compliance Center. Hier finden Sie wichtigen Informationen, wie z. B., ob eine Richtlinie erfolgreich aktiviert oder deaktiviert wurde, oder gibt an, ob die Richtlinie im Testmodus ist. 
  
Nachfolgend werden die verschiedenen Statuswerte und deren Bedeutung beschrieben.
  
|**Status**|**Erläuterung**|
|:-----|:-----|
|**Aktivieren von...** <br/> |Die Richtlinie wird gerade für die Inhaltsquellen, die sie umfasst, bereitgestellt. Die Richtlinie wird noch nicht bei allen Quellen erzwungen.  <br/> |
|**Testen, mit Benachrichtigungen** <br/> |Die Richtlinie ist im Testmodus. Die Aktionen in einer Regel werden nicht angewendet, aber Richtlinienübereinstimmungen werden mithilfe der DLP-Berichte zusammengestellt und angezeigt. Benachrichtigungen über Richtlinienübereinstimmungen werden an die angegebenen Empfänger gesendet.  <br/> |
|**Testen, ohne Benachrichtigungen** <br/> |Die Richtlinie ist im Testmodus. Die Aktionen in einer Regel werden nicht angewendet, aber Richtlinienübereinstimmungen werden mithilfe der DLP-Berichte zusammengestellt und angezeigt. Benachrichtigungen über Richtlinienübereinstimmungen werden nicht an die angegebenen Empfänger gesendet.  <br/> |
|**Ein** <br/> |Die Richtlinie ist aktiv und wird erzwungen. Die Richtlinie wurde erfolgreich für alle zugehörigen Inhaltsquellen bereitgestellt.  <br/> |
|**Wird deaktiviert...** <br/> |Die Richtlinie wird gerade aus den Inhaltsquellen, die sie umfasst, entfernt. Die Richtlinie kann noch bei einigen Quellen aktiv sein und erzwungen werden. Das Deaktivieren einer Richtlinie kann bis zu 45 Minuten dauern.  <br/> |
|**Aus** <br/> |Die Richtlinie ist nicht aktiv und wird nicht erzwungen. Die Einstellungen für die Richtlinie (Quellen, Schlüsselwörter, Dauer usw.) werden gespeichert.  <br/> |
|**Wird gelöscht...** <br/> |Die Richtlinie wird gerade gelöscht. Die Richtlinie ist nicht aktiv und wird nicht erzwungen.  <br/> |
   
## <a name="turn-off-a-dlp-policy"></a>Deaktivieren einer DLP-Richtlinie

Sie können bearbeiten oder Deaktivieren einer DLP-Richtlinie zu einem beliebigen Zeitpunkt. Deaktivieren eine Richtlinie deaktiviert alle Regeln in der Richtlinie.
  
Zum Bearbeiten oder Deaktivieren einer DLP-Richtlinie auf der Seite **Richtlinie** \> wählen Sie die Richtlinie \> **Richtlinie bearbeiten**.
  
![Richtlinie Schaltfläche "Bearbeiten"](media/ce319e92-0519-44fe-9507-45a409eaefe4.png)
  
Darüber hinaus können Sie jede Regel einzeln deaktivieren, indem die Richtlinie bearbeiten, und klicken Sie dann das Umschalten deaktiviert den **Status** dieser Regel, wie oben beschrieben. 
  
## <a name="more-information"></a>Weitere Informationen

- [Übersicht über Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md)
    
- [Senden von Benachrichtigungen und Anzeigen von Richtlinientipps für DLP-Richtlinien](use-notifications-and-policy-tips.md)
    
- [Erstellen einer DLP-Richtlinie zum Schützen von Dokumenten mit FCI oder anderen Eigenschaften](protect-documents-that-have-fci-or-other-properties.md)
    
- [Inhalt der DLP-Richtlinienvorlagen](what-the-dlp-policy-templates-include.md)
    
- [Verfügbare Arten von vertraulichen Informationen](what-the-sensitive-information-types-look-for.md)
    

