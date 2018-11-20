---
title: Erstellen, Testen und Optimieren einer DLP-Richtlinie
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
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
ms.openlocfilehash: 1d4697811a5d8dd426fed80d3d60bcd2fbea6335
ms.sourcegitcommit: 42c7ad69f95fc4d2de13293b39cc44931b9f82e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2018
ms.locfileid: "26522787"
---
# <a name="create-test-and-tune-a-dlp-policy"></a>Erstellen, Testen und Optimieren einer DLP-Richtlinie

**Principal Autor** </br>
Blog von Paul Cunningham, Microsoft MVP </br>
[Praktische 365](https://practical365.com/) </br>
[@Practical365](https://twitter.com/practical365)</br>
__________________________________________________

Verhinderung von Datenverlust ist ein Compliance-Feature von Office 365, die für Ihre Organisation zu verhindern, dass vertrauliche Informationen unerwünschten Parteien verfügbar gemacht beabsichtigt oder vor unbeabsichtigten entwickelt wurde. DLP hat ihren Ursprung in Exchange Server und Exchange Online und kann zudem in SharePoint Online und OneDrive für Unternehmen verwendet werden.

DLP verwendet eine Analysemodul Inhalt, um den Inhalt der e-Mail-Nachrichten und Dateien, untersuchen Sie vertrauliche Informationen wie Kreditkarte Zahlen und personenbezogene Informationen (PII) gesucht. Vertraulicher Informationen in der Regel nicht per e-Mail versenden, oder in Dokumenten, ohne dass zusätzliche Schritte erforderlich, wie die Verschlüsselung der e-Mail-Nachricht oder Dateien enthalten. Mit DLP können Sie erkennen Sie vertrauliche Informationen und Ausführen einer Aktion wie etwa:

- Protokollierung des Ereignisses für Überprüfungszwecken
- Anzeige einer Warnung für den Endbenutzer, die die e-Mail-Nachricht sendet oder die Freigabe der Datei
- Blockieren Sie die e-Mail- oder Dateifreigabe aus stattfinden aktiv

In einigen Fällen schließen Kunden DLP, da sie sollten Sie nicht selbst haben den Typ der Daten, die benötigt schützen. Davon ausgegangen wird, dass vertrauliche Daten wie medizinische Daten oder Finanzdaten, nur besteht für Branchen wie Gesundheitswesen oder für Unternehmen, die online-Stores ausgeführt. Aber Business vertraulichen Informationen in regelmäßigen Abständen, behandeln kann, selbst wenn sie es nicht erkennen. Eine Arbeitsmappe mit dem Namen der Mitarbeiter und Geburtsdaten ist nur als vertraulich als Kundennamen und Kreditkarteninformationen-Tabelle. Und dieser Art von Informationen, um mehr als erwartet, float-Mitarbeiter im stillen Modus zu ihrer täglichen Aufgaben benötigen, denken nothing der Export einer CSV-Datei von einem System und an eine Person per. Möglicherweise werden auch überraschen wie oft Mitarbeiter senden von e-Mails mit Kreditkarte oder Bankgeschäfte Details ohne Berücksichtigung der folgen.

## <a name="how-sensitive-information-is-detected-by-dlp"></a>Wie vertraulicher Informationen vom DLP erkannt wird.

Vertraulicher Informationen wird durch den regulären Ausdruck (RegEx) Mustervergleich in Kombination mit mit anderen Indikatoren wie der Nähe von bestimmten Schlüsselwörtern zu übereinstimmenden Muster identifiziert. Ein Beispiel hierfür ist Kreditkarte Zahlen. Eine Kreditkartennummer hat 16 Ziffern. Jedoch diesen Ziffern geschrieben werden können auf unterschiedliche Weise, wie etwa 1111-1111-1111-1111 1111 1111 1111 1111 oder 1111111111111111.

Eine beliebige 16-stellige Zeichenfolge ist nicht unbedingt eine Kreditkartennummer, kann dies eine Ticket-Nummer aus einem Desk-Hilfesystem oder eine fortlaufende Zahl von einem Hardwaregerät. Um die Differenz zwischen eine Kreditkartennummer und eine unschädlichen 16-stellige Zeichenfolge zu sagen, ist eine Berechnung ausgeführt (Prüfsumme) zu bestätigen, dass die Zahlen der verschiedenen Kreditkarte Marken einem bekannten Muster übereinstimmen.

Darüber hinaus gilt der Nähe von Schlüsselwörtern wie "VISA" oder "AMEX" zusammen mit der Nähe zu Datumswerte, die das Ablaufdatum Kreditkarte möglicherweise auch Treffen einer Entscheidung darüber, ob die Daten eine Kreditkartennummer ist.

Anders gesagt ist DLP in der Regel intelligent genug ist, den Unterschied zwischen diesen beiden Texte in einer e-Mail erkennt:

- "Können Sie mir einen neuen Laptop bestellen. Meine VISA Anzahl verwenden Sie 1111-1111-1111-1111, Ablauf 11/22, und senden Sie mir das voraussichtliche Lieferung Datum, wenn Sie es haben."
- "Mein Laptop Seriennummer 2222-2222-2222-2222 ist und es auf 11/2010 erworben wurde. Sagen, ist Meine Reisen Visa noch genehmigt?"

Ein guter Verweis auf die mit einer Textmarke versehenen beibehalten wird in diesem [Thema auf Typen vertraulicher Informationen](what-the-sensitive-information-types-look-for.md) , die erklärt, wie jeden Informationstyp erkannt wird.

## <a name="where-to-start-with-data-loss-prevention"></a>Wo Sie beginnen mit Verhinderung von Datenverlust

Wenn die Risiken von Datenlecks nicht vollständig offensichtlich sind, ist es schwierig, um zu bestimmen, wo genau Sie gestartet werden soll mit DLP implementieren. Zum Glück können DLP-Richtlinien ausgeführt werden, im "Testmodus", sodass Sie ihre Effizienz und Genauigkeit zu ermitteln, bevor Sie diese aktivieren.

DLP-Richtlinien für Exchange Online können über die Exchange-Verwaltungskonsole verwaltet werden. Aber Sie können DLP-Richtlinien für alle Arbeitslasten über die Sicherheit und Compliance Center, konfigurieren, damit das ist, was für Präsentationen in diesem Artikel verwendet wird. Im Compliance Center & Sicherheit finden Sie unter **Verhinderung von Datenverlust**die DLP-Richtlinien > **Richtlinie**. Klicken Sie auf **Erstellen einer Richtlinie** zu starten.

Office 365 bietet eine Reihe von [DLP-Richtlinienvorlagen](what-the-dlp-policy-templates-include.md) , die Sie verwenden können, um DLP-Richtlinien zu erstellen. Angenommen, Sie ein Australien Business sind. Sie können die Vorlagen, um nur die anzuzeigen, die für Australien, relevant sind Filtern die fallen in die allgemeinen Kategorien der Financial, medizinische und Integrität und den Datenschutz.

![Land oder Region auswählen](media/DLP-create-test-tune-choose-country.png)

Für diese Demo werde ich Australien persönlich identifizierbare Informationen (PII)-Daten auswählen, welche die Informationstypen Australien Tax Datei Anzahl (TFN) und des Treibers Lizenz Zahl enthält.

![Auswählen eine Vorlage](media/DLP-create-test-tune-choose-policy-template.png)

Benennen Sie Ihre neuen DLP-Richtlinie. Der Standardnamen entspricht der DLP-Richtlinienvorlage sollten, aber Sie einen aussagekräftigeren Namen eigenes, da mehrere Richtlinien aus der gleichen Vorlage erstellt werden können.

![Option, um Ihre Richtlinie nennen](media/DLP-create-test-tune-name-policy.png)

Wählen Sie die Speicherorte, denen die Richtlinie angewendet wird. Exchange Online, SharePoint Online und OneDrive für Unternehmen können DLP-Richtlinien zuweisen. Ich werde lassen Sie diese Richtlinie so konfiguriert, dass für alle Speicherorte gelten.

![Auswählen von allen Speicherorten](media/DLP-create-test-tune-choose-locations.png)

Übernehmen Sie die Standardwerte bei **Richtlinieneinstellungen** zunächst nur für jetzt. Es ist viel Anpassung, die Sie in DLP-Richtlinien ausführen können, aber die Standardwerte sind eine präzise Anlaufstelle für.

![Optionen zum Anpassen des Inhaltstyps zu schützenden Komponenten](media/DLP-create-test-tune-default-customization-settings.png)

Nachdem Sie auf **Weiter** wird eine zusätzliche Seite **Einstellungen für die Informationsverwaltungsrichtlinie** mit mehr Anpassungsoptionen angezeigt werden. Für eine Richtlinie, die Sie gerade testen, wird hier, in dem Sie einige anpassen beginnen können.

- Ich habe Tipps zu Richtlinien für die ist nun eine angemessene Schritt ausgeführt werden, wenn nur Dinge testen und nicht alles noch für Benutzer anzeigen möchten, dass deaktiviert. Tipps zu Richtlinien anzeigen Warnungen für Benutzer, dass sie gerade eine DLP-Richtlinie verletzen. Angenommen, ein Outlook-Benutzer wird eine Warnung ausgegeben, dass die Datei, die sie angefügt haben Kreditkarte Zahlen enthält angezeigt und bewirkt, dass ihre e-Mails abgelehnt werden soll. Das Ziel des richtlinientipps ist, nicht kompatible Verhalten zu beenden, bevor er eintritt.
- Ich habe auch die Anzahl der Instanzen von 10 auf 1 fest, verringert, sodass diese Richtlinie erkennt alle Freigabe von Australien PII-Daten, nicht nur Massen Freigabe der Daten.
- Ich habe die schadensbericht e-Mail auch einen anderen Empfänger hinzugefügt.

![Zusätzliche Richtlinieneinstellungen](media/DLP-create-test-tune-more-policy-settings.png)

Schließlich habe ich diese Richtlinie anfänglich im Testmodus ausführen konfiguriert. Beachten Sie, dass auch eine Option deaktivieren richtlinientipps im Testmodus vorhanden ist. Dadurch werden die Flexibilität, richtlinieninfos in die Richtlinie aktiviert haben, aber entscheiden, ob anzeigen oder unterdrücken sie während der Tests.

![Option, um zuerst Richtlinie testen](media/DLP-create-test-tune-test-mode.png)

Klicken Sie auf dem Bildschirm endgültige Überprüfung auf **Erstellen** , um die Erstellung der Richtlinie abzuschließen.

## <a name="test-a-dlp-policy"></a>Testen einer DLP-Richtlinie

Die neue DLP-Richtlinie beginnt innerhalb von ungefähr einer Stunde wirksam wird. Sie können sit und warten, bis es vom normalen Benutzeraktivität ausgelöst werden, oder können Sie versuchen, es selbst ausgelöst. Zuvor verknüpfte ich dieses [Thema auf Typen vertraulicher Informationen](what-the-sensitive-information-types-look-for.md), die Sie mit Informationen zur Verwendung von Übereinstimmungen mit DLP auslösen bietet.

Beispielsweise wird die DLP-Richtlinie für diesen Artikel erstellten Australien Tax Datei Zahlen (TFN) erkennen. Entsprechend der Dokumentation basiert die Übereinstimmung auf die folgenden Kriterien.

![Dokumentationen zum australische Steuernummer](media/DLP-create-test-tune-Australia-Tax-File-Number-doc.png)
 
Um eine vielmehr stumpfen Weise TFN Erkennung demonstrieren, werden eine e-Mail mit den Wörtern "Steuernummer" und eine Zeichenfolge 9 Ziffer in der Nähe über ohne Probleme führen. Der Grund dafür, dass es die DLP-Richtlinie nicht ausgelöst werden besteht die Zeichenfolge 9 Ziffern muss die Prüfsumme übergeben, die angibt, dass es sich um eine gültige TFN und nicht nur eine unschädlichen Zeichenfolge aus Zahlen handelt.

![Australische Steuernummer, die Prüfsumme nicht erfolgreich ausgeführt wird](media/DLP-create-test-tune-email-test1.png)

Im Vergleich wird eine e-Mail mit den Wörtern "Steuernummer" und eine gültige TFN, die die Prüfsumme übergibt die Richtlinie ausgelöst. Für den Datensatz der TFN ich verwende stammt von einer Website, die generiert gültig, aber kein Original TFNs. Es gibt ähnliche Websites, die [gültige jedoch gefälschten Kreditkarte Zahlen](http://www.fakecreditcardgenerator.net/)zu generieren. Solche Websites sind sehr nützlich, da eine der häufigsten Fehler beim Testen einer DLP-Richtlinie eine falsche Anzahl, die ist nicht gültig verwendet wird und wird nicht die Prüfsumme übergeben (und aus diesem Grund wird nicht die Richtlinie auslösen).

![Australische Steuernummer, die die Prüfsumme übergibt.](media/DLP-create-test-tune-email-test2.png)

Die schadensbericht e-Mail enthält den Typ der vertraulichen Informationen, der gefunden wurde, wie viele Instanzen erkannt wurden und die Vertrauensstufe der Entdeckung.

![Schadensbericht mit Steuernummer erkannt](media/DLP-create-test-tune-email-incident-report.png)

Wenn Sie die DLP-Richtlinie im Testmodus lassen und der schadensbericht-e-Mails analysieren, können Sie beginnen, erhalten Sie einen Eindruck davon für die Genauigkeit der DLP-Richtlinien und wie effektiv es werden kann, wenn es erzwungen wird. Neben der Vorfall Berichte können Sie an, um einer aggregierten Ansicht Richtlinie Treffer über Ihre Mandanten finden Sie unter [Verwenden der DLP-Berichte](view-the-dlp-reports.md) .

## <a name="tune-a-dlp-policy"></a>Optimieren einer DLP-Richtlinie

Wie Sie Ihre Richtlinie Treffer, die Sie möglicherweise einige ändern analysieren Sie das Verhalten der Richtlinien. Ein einfaches Beispiel können Sie feststellen, dass eine TFN in e-Mail kein Problem ist (Ich könnte es noch ist, aber wir wählen sie aus Gründen der Demo), aber zwei oder mehr Instanzen ist ein Problem. Mehrere Instanzen könnte ein riskant Szenario wie ein Mitarbeiter per e-Mail senden einen CSV Export aus der HR-Datenbank für Dritte, beispielsweise einen externen Accounting-Dienst sein. Auf jeden Fall etwas bevorzugen Sie erkennen und blockieren.

Im Compliance Center & Sicherheit können Sie eine vorhandene Richtlinie zum Anpassen des Verhaltens bearbeiten.

![Option zum Bearbeiten von Gruppenrichtlinien](media/DLP-create-test-tune-edit-policy.png)
 
Sie können die standorteinstellungen anpassen, so, dass die Richtlinie nur für bestimmte Arbeitslasten oder auf bestimmte Websites und Konten angewendet wird.

![Optionen, um bestimmte Orte auswählen](media/DLP-create-test-tune-edit-locations.png)

Sie können auch Anpassen der Einstellungen für die Informationsverwaltungsrichtlinie und bearbeiten den Regeln, die Ihre Arbeitsweise Ihren Anforderungen.

![Option zum Bearbeiten der Regel](media/DLP-create-test-tune-edit-rule.png)

Wenn Sie eine Regel in einer DLP-Richtlinie bearbeiten können Sie Folgendes ändern:

- Die Bedingungen, einschließlich Typ und Anzahl der Instanzen von vertrauliche Daten, die die Regel ausgelöst werden.
- Die Aktionen, die ausgeführt werden, wie etwa Einschränken des Zugriffs auf den Inhalt.
- Benutzer-Benachrichtigungen, die richtlinientipps sind, die der Benutzer in ihrem e-Mail-Client oder Web-Browser angezeigt werden.
- Benutzer überschreibt, um zu bestimmen, ob Benutzer auswählen können, ihre e-Mail oder eine Dateifreigabe trotzdem fortsetzen.
- Vorfall Berichte, um Administratoren zu benachrichtigen.

![Optionen, um Teile einer Regel bearbeiten](media/DLP-create-test-tune-editing-options.png)

Für diese Demo ich die Richtlinie (Achten Sie auf diese Weise ohne angemessene zur Förderung des Bekanntheitsgrads benutzerschulungen), Benutzer Benachrichtigungen hinzugefügt haben, und Benutzer können Sie die Richtlinie mit als Rechtfertigung oder als falsch positiv kennzeichnen überschreiben zulässig. Beachten Sie, dass Sie auch e-Mails und Richtlinie QuickInfo-Text anpassen können, wenn Sie zusätzliche Informationen zu Ihrer Organisation Richtlinien enthalten ist, oder fordern Benutzer an den Support wenden, wenn sie Fragen haben möchten.

![Optionen für die Benutzer Benachrichtigungen und Außerkraftsetzungen](media/DLP-create-test-tune-user-notifications.png)

Die Richtlinie enthält zwei Regeln für die Behandlung von hohen und niedrigen Volume sein, weshalb beide mit den Aktionen, die Sie möchten bearbeiten. Dies ist eine Gelegenheit, Fällen unterschiedlich je nach ihren Eigenschaften zu behandeln. Sie können beispielsweise Außerkraftsetzungen für leise Verstöße zulassen, jedoch nicht zulassen Außerkraftsetzungen für große Menge Verstöße.

![Eine Regel für große Menge und eine Regel für leise](media/DLP-create-test-tune-two-rules.png)

Wenn Sie tatsächlich blockieren oder Einschränken des Zugriffs auf Inhalte, die in Verletzung der Richtlinie möchten, müssen Sie auch, eine Aktion für die Regel dazu zu konfigurieren.

![Option zum Einschränken des Zugriffs auf Inhalt](media/DLP-create-test-tune-restrict-access-action.png)

Nach dem speichern diese Änderungen an den Richtlinieneinstellungen, muss auch das Hauptfenster Einstellungsseite für die Richtlinie zurück, und aktivieren die Option zum Anzeigen von Tipps zu Richtlinien für Benutzer, während die Richtlinie im Testmodus ist. Dies ist eine effektive Möglichkeit Einführung von DLP-Richtlinien für die Endbenutzer, und führen Sie Benutzer zur Förderung des Bekanntheitsgrads Training, ohne zu riskieren zu viele falsch positive Ergebnisse, die ihre Produktivität auswirkt.

![Option zum Anzeigen von Tipps zu Richtlinien im Testmodus](media/DLP-create-test-tune-show-policy-tips.png)

Auf dem Server-Seite (oder Cloud-Seite, wenn Sie lieber) kann die Änderung nicht sofort, aufgrund von verschiedenen Verarbeitung Intervalle wirksam. Wenn Sie eine Änderung der DLP-Richtlinie tätigen, die neue Tipps zu Richtlinien, die einem Benutzer angezeigt wird, kann der Benutzer nicht finden Sie die Änderungen wirksam in ihrem Outlook-Client werden die Richtlinien alle 24 Stunden überprüft. Wenn Sie zu beschleunigen bei testen möchten, können Sie dieses Registrierungsupdate [Zeitstempel der letzten Download aus dem Schlüssel PolicyNudges](https://support.microsoft.com/en-au/help/2823261/changes-to-a-data-loss-prevention-policy-don-t-take-effect-in-outlook?__hstc=18650278.46377037dc0a82baa8a30f0ef07a7b2f.1538687978676.1538693509953.1540315763430.3&__hssc=18650278.1.1540315763430&__hsfp=3446956451)deaktivieren. Die neuesten Richtlinieninformationen das nächste Mal neu, und beginnen Verfassen einer e-Mail-Nachricht wird von Outlook heruntergeladen werden.

Wenn Sie richtlinientipps aktiviert haben, wird der Benutzer beginnt mit dem die Tipps in Outlook finden Sie unter und falsch positive Ergebnisse können Sie melden werden, sobald diese auftreten.

![Mit der Option zum falsch positives richtlinientipp](media/DLP-create-test-tune-policy-tip-in-outlook.png)

## <a name="investigate-false-positives"></a>Falsch positive Ergebnisse untersuchen

DLP-Richtlinienvorlagen sind nicht perfekte gerade aus dem Feld. Es ist wahrscheinlich, dass Sie einige falsch positive Ergebnisse, die Sie in der Umgebung aus diesem finden Grund es so wichtig ist ist, die Sie sich in einer DLP-Bereitstellung zu erleichtern, auftreten Dank angemessen testen und Optimieren Ihrer Richtlinien.

Hier ist ein Beispiel für ein falsch positives Ergebnis. Diese e-Mail ist ziemlich unschädlichen. Der Benutzer ist ihre Mobiltelefonnummer an eine Person bereitstellen und einschließlich deren e-Mail-Signatur.

![E-Mail mit falsch positive](media/DLP-create-test-tune-false-positive-email.png)
 
Aber der Benutzer erhält einen richtlinientipp Warnung sie, dass die e-Mail vertraulichen Informationen enthält, insbesondere einer australische Führerscheinnummer.

![Option zum falsch positives in richtlinientipp](media/DLP-create-test-tune-policy-tip-closeup.png)

Der Benutzer kann das false positive Ergebnis melden, und der Administrator kann untersuchen Sie, warum es aufgetreten ist. In der e-Mail schadensbericht wird die e-Mail-Nachricht als falsch positiv gekennzeichnet.

![Schadensbericht mit falsch positives Ergebnis](media/DLP-create-test-tune-false-positive-incident-report.png)

Groß-/Kleinschreibung des Treibers-Lizenz ist ein gutes Beispiel, in einsteigen. Der Grund dafür, diese falsch positives Ergebnis ist innerhalb von 300 Zeichen der Nähe der Schlüsselwörter "australische Nsw" aufgetreten ist, die die "Australien Personalausweis" Typ von einer beliebigen 9 Ziffern-Zeichenfolge (sogar eine, die Teil einer Zeichenfolge 10 Ziffern ist), ausgelöst werden soll (ohne Beachtung von Groß-/Kleinschreibung). Damit durch das Telefon und e-Mail-Signatur ausgelöst wird, da der Benutzer werden in australische geschieht.

Interessant, wenn "Australische, NSW" ein Komma aufweist, wird die DLP-Richtlinie nicht ausgelöst. Ich habe keine Ahnung, warum ein Komma spielt Rolle hier noch warum andere Orte und Zustände in Australien sind nicht in der Schlüsselwörter für die australische Treiber Lizenztyp Informationen enthalten, aber es Sie wechseln. So, wie können wir genauer darüber? Es gibt einige Optionen.

Eine Option besteht darin, den Australien Treiber Lizenztyp Informationen aus der Richtlinie zu entfernen. Es ist vorhanden, da es die DLP-Richtlinienvorlage gehört, aber es sind nicht gezwungen, es zu verwenden. Wenn Sie nur Tax Dateinummern und nicht des Treibers Lizenzen interessiert sind, können Sie nur entfernen. Sie können beispielsweise die leise Regel in der Richtlinie zu entfernen, jedoch in der Regel große Menge lassen, sodass Listen mit mehrere Treiber Lizenzen weiterhin erkannt werden.

![Option zum Löschen von vertraulichen Informationen Typ Regel](media/DLP-create-test-tune-delete-low-volume-rule.png)
 
Eine weitere Option ist die Anzahl der Instanzen, einfach zu erhöhen, damit nur eine geringe Anzahl von Lizenzen des Treibers erkannt wird, wenn mehrere Instanzen vorhanden sind.

![Option zum Bearbeiten der Anzahl der Instanzen](media/DLP-create-test-tune-edit-instance-count.png)

Zusätzlich zum Ändern der Anzahl der Instanzen, können Sie auch die Übereinstimmung Genauigkeit (oder Confidence Level) anpassen. Wenn Ihre vertrauliche Informationen mehrere Muster verfügt, können Sie die Genauigkeit Übereinstimmung in der Regel anpassen, damit die Regel nur bestimmte Muster entspricht. Falsch positive Ergebnisse reduzieren Sie können Sie beispielsweise die Übereinstimmung Genauigkeit von der Regel festlegen, sodass sie nur das Muster, die höchste Vertrauensstufe übereinstimmt. Grundlegendes zur Berechnung Vertrauensstufe ist etwas komplizierter (und Gegenstand dieses Post), aber hier ist eine gute Erläuterung der [Vorgehensweise zum Vertrauensstufe zur Optimierung Ihrer Regeln verwenden](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#match-accuracy).

Wenn Sie noch etwas abrufen möchten erweitert, schließlich können Sie alle Arten von vertraulichen Informationen anpassen – Sie können beispielsweise "Australische NSW" entfernen, aus der Liste der Schlüsselwörter für [Australien Personalausweis](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for#australia-drivers-license-number), um das falsch positive Ergebnis ausgelöst oben zu vermeiden. Für diese Vorgehensweise mithilfe von XML und PowerShell finden Sie unter in diesem Thema zum [Anpassen eines integrierten vertrauliche Informationen-Typs](customize-a-built-in-sensitive-information-type.md).

## <a name="turn-off-a-dlp-policy"></a>Deaktivieren einer DLP-Richtlinie

Wenn Sie die DLP-Richtlinie ist genau und effektiv zu erkennen, Typen vertraulicher Informationen, und Ihre Endbenutzer bereit für den Umgang mit der Richtlinien vorhanden sind, dann können Sie die Richtlinie zufrieden sind.

![Option, um die Richtlinie zu aktivieren](media/DLP-create-test-tune-turn-on-policy.png)
 
Wenn Sie warten zu sehen, wenn die Richtlinie wirksam werden, [Verbindung mit Office 365-Sicherheit und Compliance Center PowerShell herstellen](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps) und führen Sie das [Cmdlet Get-DlpCompliancePolicy](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/get-dlpcompliancepolicy?view=exchange-ps) um die DistributionStatus anzuzeigen.

![Ausführen von Cmdlets in PowerShell](media/DLP-create-test-tune-PowerShell.png)

Nach dem Einschalten der DLP-Richtlinie, sollten Sie einige abschließende Tests eigene, stellen Sie sicher, dass ausführen, dass die erwartete Richtlinienaktionen auftreten können. Wenn Sie Elemente wie Kreditkartendaten testen möchten, sind Websites online mit Informationen dazu, wie zum Beispiel Kreditkarte generieren oder andere persönliche Informationen, die Prüfsumme übergeben und Ihrer Richtlinien auszulösen.

Richtlinien, mit die Benutzer Außerkraftsetzungen können, werden die Option für dem Benutzer als Teil der richtlinientipp angezeigt.

![Richtlinientipp, mit dem Benutzer außer Kraft setzen kann.](media/DLP-create-test-tune-override-option.png)

Richtlinien, die Inhalte einschränken werden die Warnung dem Benutzer als Teil der richtlinientipp angezeigt, und verhindern, dass sie die e-Mail-Nachricht senden.

![Richtlinientipp Inhalt ist beschränkt.](media/DLP-create-test-tune-restrict-warning.png)

## <a name="summary"></a>Zusammenfassung

Richtlinien zur Verhinderung von Datenverlust eignen sich für Organisationen aller Arten. Testen einige DLP-Richtlinien ist eine niedriges Risiko Übung aufgrund das Steuerelement über Dinge wie richtlinientipps, Endbenutzer Außerkraftsetzungen und Vorfall-Berichte. Sie können im stillen Modus einige DLP-Richtlinien, um herauszufinden, welche Art von Verletzungen sind bereits in Ihrer Organisation auftritt testen und klicken Sie dann erstellen Richtlinien mit falsch positive Sätze niedrig, informieren Sie die Benutzer auf zulässig, und was nicht zulässig ist und klicken Sie dann Ihre DLP-Richtlinien, um einführen der Organisation.
