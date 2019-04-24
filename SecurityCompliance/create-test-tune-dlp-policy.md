---
title: Erstellen, Testen und Optimieren einer DLP-Richtlinie
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'Die einfachste und gängigste Methode für den Einstieg in DLP-Richtlinien ist die Verwendung der in Office 365 enthaltenen Vorlagen. '
ms.openlocfilehash: 0c6b3bce7b336b08595a432c29601ecb63155589
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259338"
---
# <a name="create-test-and-tune-a-dlp-policy"></a>Erstellen, Testen und Optimieren einer DLP-Richtlinie

**Prinzipal Autor** <br/>
Paul Cunningham, Microsoft MVP <br/>
[Praktische 365](https://practical365.com/) <br/>
[@Practical365](https://twitter.com/practical365)<br/>
__________________________________________________

"Verhinderung von Datenverlust" ist ein Compliance-Feature von Office 365, mit dessen Hilfe Ihr Unternehmen verhindern kann, dass vertrauliche Informationen vorsätzlich oder versehentlich an unerwünschte Personen gerichtet werden. DLP hat seine Wurzeln in Exchange Server und Exchange Online und ist auch in SharePoint Online und OneDrive for Business anwendbar.

DLP verwendet ein Inhaltsanalyse Modul, um den Inhalt von e-Mail-Nachrichten und Dateien zu untersuchen und nach vertraulichen Informationen wie Kreditkartennummern und personenbezogenen Informationen (PII) zu suchen. Vertrauliche Informationen sollten in der Regel nicht per e-Mail oder in Dokumente gesendet werden, ohne zusätzliche Schritte wie das Verschlüsseln der e-Mail-Nachricht oder Dateien zu Unternehmen. Mit DLP können Sie vertrauliche Informationen aufspüren und Maßnahmen ergreifen, wie beispielsweise:

- Protokollieren des Ereignisses zu Überwachungszwecken
- Anzeigen einer Warnung an den Endbenutzer, der die e-Mail sendet oder die Datei freigibt
- Aktives Blockieren der e-Mail-oder Dateifreigabe

Manchmal lehnen Kunden DLP ab, da Sie sich nicht für die Art von Daten halten, die geschützt werden müssen. Es wird davon ausgegangen, dass vertrauliche Daten wie medizinische Datensätze oder finanzielle Informationen nur für Branchen wie das Gesundheitswesen oder für Unternehmen mit Online Shops vorhanden sind. Aber jedes Unternehmen kann vertrauliche Informationen regelmäßig behandeln, auch wenn Sie es nicht erkennen. Eine Tabelle mit Mitarbeiternamen und Geburtsdaten ist ebenso vertraulich wie eine Tabelle mit Kundennamen und Kreditkartendetails. Und diese Art von Informationen neigt dazu, mehr zu bewegen, als Sie vielleicht erwarten, da Mitarbeiter ruhig über Ihre täglichen Aufgaben zu gehen, denken nichts der Export eine CSV-Datei aus einem System und per e-Mail an einen anderen. Sie können auch überrascht sein, wie oft Mitarbeiter e-Mails mit Kreditkarten-oder Bank Details senden, ohne die Konsequenzen zu berücksichtigen.

## <a name="how-sensitive-information-is-detected-by-dlp"></a>Erkennung vertraulicher Informationen durch DLP

Vertrauliche Informationen werden durch RegEx-Musterübereinstimmung (Regular Expression) in Kombination mit anderen Indikatoren wie der Nähe bestimmter Schlüsselwörter zu den übereinstimmenden Mustern identifiziert. Ein Beispiel hierfür sind Kreditkartennummern. Eine VISA-Kreditkartennummer hat 16 Ziffern. Diese Ziffern können jedoch auf unterschiedliche Weise geschrieben werden, beispielsweise 1111-1111-1111-1111, 1111 1111 1111 1111 oder 1111111111111111.

Jede 16-stellige Zeichenfolge ist nicht unbedingt eine Kreditkartennummer, es könnte eine Ticketnummer von einem Helpdesk-System oder eine Seriennummer eines Hardware Stücks sein. Um den Unterschied zwischen einer Kreditkartennummer und einer harmlosen 16-stelligen Zeichenfolge zu erkennen, wird eine Berechnung durchgeführt (checksum), um zu bestätigen, dass die Zahlen mit einem bekannten Muster der verschiedenen Kreditkarten Marken übereinstimmen.

Darüber hinaus wird auch die Nähe von Stichwörtern wie "VISA" oder "AMEX" sowie die Nähe zu Datumswerten, die das Gültigkeitsdatum der Kreditkarte sein können, als Entscheidung getroffen, ob es sich bei den Daten um eine Kreditkartennummer handelt oder nicht.

Mit anderen Worten ist DLP in der Regel intelligent genug, um den Unterschied zwischen diesen beiden Texten in einer e-Mail zu erkennen:

- "Können Sie mir einen neuen Laptop bestellen. Verwenden Sie meine VISA Nummer 1111-1111-1111-1111, Ablauf 11/22, und senden Sie mir das voraussichtliche Lieferdatum, wenn Sie es haben. "
- "Meine Laptop-Seriennummer ist 2222-2222-2222-2222 und wurde am 11/2010 erworben. Ist mein Reisevisum noch nicht genehmigt? "

In diesem [Thema zu vertraulichen Informationstypen](what-the-sensitive-information-types-look-for.md) wird erläutert, wie jeder Informationstyp erkannt wird.

## <a name="where-to-start-with-data-loss-prevention"></a>Wo beginnen Sie mit der Verhinderung von Datenverlust

Wenn die Risiken von Datenlecks nicht ganz offensichtlich sind, ist es schwierig zu erarbeiten, wo genau Sie mit der Implementierung von DLP beginnen sollten. Zum Glück können DLP-Richtlinien im Testmodus ausgeführt werden, sodass Sie ihre Effektivität und Genauigkeit vor dem Aktivieren der Funktion messen.

DLP-Richtlinien für Exchange Online können über das Exchange-Verwaltungskonsole verwaltet werden. Sie können jedoch DLP-Richtlinien für alle Arbeitsauslastungen über das Security & Compliance Center konfigurieren. Im Security & Compliance Center finden Sie die DLP-Richtlinien unter **Data Loss Prevention** > **Policy**. Klicken Sie auf **Richtlinie erstellen** , um zu starten.

Office 365 bietet eine Reihe von [DLP-Richtlinienvorlagen](what-the-dlp-policy-templates-include.md) , die Sie zum Erstellen von DLP-Richtlinien verwenden können. Angenommen, Sie sind ein australisches Unternehmen. Sie können die Richtlinienvorlagen filtern, um nur diejenigen anzuzeigen, die für Australien relevant sind, die in die allgemeinen Kategorien finanzieller, medizinischer und gesundheitlicher Datenschutz fallen.

![Option zum Auswählen von Land oder Region](media/DLP-create-test-tune-choose-country.png)

Für diese Demonstration wähle ich australische personenbezogene Informationen (PII) aus, die die Informationstypen der australischen Steuer Dateinummer (TFN) und die Treiber Lizenznummer enthalten.

![Option zum Auswählen einer Richtlinienvorlage](media/DLP-create-test-tune-choose-policy-template.png)

Geben Sie Ihrer neuen DLP-Richtlinie einen Namen. Der Standardname stimmt mit der DLP-Richtlinienvorlage überein, Sie sollten jedoch einen aussagekräftigeren Namen für Ihre eigenen auswählen, da mehrere Richtlinien aus derselben Vorlage erstellt werden können.

![Option zum Benennen Ihrer Richtlinie](media/DLP-create-test-tune-name-policy.png)

Wählen Sie die Speicherorte aus, auf die die Richtlinie angewendet werden soll. DLP-Richtlinien können für Exchange Online, SharePoint Online und OneDrive for Business gelten. Ich möchte diese Richtlinie so konfigurieren, dass Sie auf alle Standorte angewendet wird.

![Option zum Auswählen aller Standorte](media/DLP-create-test-tune-choose-locations.png)

Akzeptieren Sie beim ersten Schritt der **Richtlinieneinstellungen** nur die Standardwerte für jetzt. Es gibt eine Vielzahl von Anpassungen, die Sie in DLP-Richtlinien ausführen können, aber die Standardwerte sind ein guter Ausgangspunkt.

![Optionen zum Anpassen des zu schützenden Inhaltstyps](media/DLP-create-test-tune-default-customization-settings.png)

Nachdem Sie auf **weiter** geklickt haben, wird eine Seite mit zusätzlichen **Richtlinieneinstellungen** mit weiteren Anpassungsoptionen angezeigt. Für eine Richtlinie, die Sie gerade testen, können Sie hier beginnen, einige Anpassungen vorzunehmen.

- Ich habe die Richtlinien Tipps für jetzt deaktiviert, was ein angemessener Schritt ist, wenn Sie nur die Dinge testen und noch nichts für die Benutzer anzeigen möchten. Richtlinien Tipps zeigen Warnungen für Benutzer an, die gegen eine DLP-Richtlinie verstoßen. Ein Outlook-Benutzer sieht beispielsweise eine Warnung, dass die angefügte Datei Kreditkartennummern enthält und Ihre e-Mails zurückgewiesen wird. Das Ziel von Richtlinien Tipps besteht darin, das nicht kompatible Verhalten zu beenden, bevor es geschieht.
- Ich habe auch die Anzahl der Instanzen von 10 auf 1 verringert, sodass diese Richtlinie eine Freigabe von australischen PII-Daten ermittelt, nicht nur die Massenfreigabe der Daten.
- Ich habe auch einen weiteren Empfänger zu der Vorfall Bericht-e-Mail hinzugefügt.

![Zusätzliche Richtlinieneinstellungen](media/DLP-create-test-tune-more-policy-settings.png)

Schließlich habe ich diese Richtlinie so konfiguriert, dass Sie zunächst im Testmodus ausgeführt wird. Beachten Sie, dass es hier auch eine Option gibt, um Richtlinien Tipps im Testmodus zu deaktivieren. Auf diese Weise haben Sie die Flexibilität, Richtlinien Tipps in der Richtlinie aktiviert zu haben, aber dann entscheiden, ob Sie während der Tests angezeigt oder unterdrückt werden sollen.

![Option zum Testen der Richtlinie zuerst](media/DLP-create-test-tune-test-mode.png)

Klicken Sie auf dem Bildschirm abschließende Überprüfung auf **Erstellen** , um die Erstellung der Richtlinie abzuschließen.

## <a name="test-a-dlp-policy"></a>Testen einer DLP-Richtlinie

Ihre neue DLP-Richtlinie wird innerhalb einer Stunde wirksam. Sie können sitzen und warten, bis es von normaler Benutzeraktivität ausgelöst wird, oder Sie können versuchen, es selbst auszulösen. Zuvor habe ich mich mit diesem [Thema zu vertraulichen Informationstypen](what-the-sensitive-information-types-look-for.md)verknüpft, in dem Sie Informationen dazu erhalten, wie Sie DLP-Übereinstimmungen auslösen.

Die für diesen Artikel erstellte DLP-Richtlinie ermittelt beispielsweise australische Steuerdatei Nummern (TFN). Gemäß der Dokumentation basiert die Übereinstimmung auf den folgenden Kriterien.

![Dokumentation zur australischen Steuer Dateinummer](media/DLP-create-test-tune-Australia-Tax-File-Number-doc.png)
 
Um die TFN-Erkennung auf eine eher stumpfe Weise zu demonstrieren, wird eine e-Mail mit den Worten "Tax File Number" und eine 9-stellige Zeichenfolge in unmittelbarer Nähe ohne Probleme durchlaufen. Der Grund dafür, dass die DLP-Richtlinie nicht ausgelöst wird, besteht darin, dass die 9-stellige Zeichenfolge die Prüfsumme passieren muss, die angibt, dass es sich um eine gültige TFN und nicht nur um eine harmlose Zahlenfolge handelt.

![Australische Steuerdatei Nummer, die keine Prüfsumme übergibt](media/DLP-create-test-tune-email-test1.png)

Im Vergleich dazu löst eine e-Mail mit dem Wort "Tax File Number" und einem gültigen TFN, das die Prüfsumme übergibt, die Richtlinie aus. Für den Eintrag hier wurde die TFN, die ich verwende, von einer Website entnommen, die gültige, aber nicht echte TFNs generiert. Es gibt ähnliche Websites, die [gültige, aber gefälschte Kreditkartennummern](http://www.fakecreditcardgenerator.net/)generieren. Solche Websites sind sehr nützlich, da eine der häufigsten Fehler beim Testen einer DLP-Richtlinie eine gefälschte Nummer verwendet wird, die ungültig ist und die Prüfsumme nicht weiter gibt (und daher die Richtlinie nicht auslöst).

![Australische Steuerdatei Nummer, die die Prüfsumme übergibt](media/DLP-create-test-tune-email-test2.png)

Die Vorfall Bericht-e-Mail enthält den Typ der vertraulichen Informationen, die erkannt wurden, wie viele Instanzen erkannt wurden, und die Zuverlässigkeitsstufe der Erkennung.

![Vorfall Bericht mit gefundener Steuerdatei Nummer](media/DLP-create-test-tune-email-incident-report.png)

Wenn Sie Ihre DLP-Richtlinie im Testmodus belassen und die Vorfall Berichts-e-Mails analysieren, können Sie sich über die Genauigkeit der DLP-Richtlinie und ihre Wirksamkeit bei der Erzwingung informieren. Zusätzlich zu den Vorfall Berichten können Sie [die DLP-Berichte verwenden](view-the-dlp-reports.md) , um eine aggregierte Ansicht der Richtlinien Übereinstimmungen in Ihrem Mandanten anzuzeigen.

## <a name="tune-a-dlp-policy"></a>Optimieren einer DLP-Richtlinie

Wenn Sie Ihre Richtlinien Treffer analysieren, können Sie einige Anpassungen an den Richtlinien vornehmen. Als einfaches Beispiel können Sie feststellen, dass ein TFN in einer e-Mail kein Problem darstellt (ich glaube, es ist immer noch, aber lassen Sie uns es um der Demonstration Willen gehen), aber zwei oder mehr Instanzen ist ein Problem. Bei mehreren Instanzen kann es sich um ein riskantes Szenario handeln, beispielsweise einen Mitarbeiter, der einen CSV-Export aus der HR-Datenbank an eine externe Person per e-Mail abgibt, beispielsweise einen externen Buchhaltungsdienst. Definitiv etwas, das Sie lieber aufspüren und blockieren möchten.

Im Security & Compliance Center können Sie eine vorhandene Richtlinie bearbeiten, um das Verhalten anzupassen.

![Option zum Bearbeiten der Richtlinie](media/DLP-create-test-tune-edit-policy.png)
 
Sie können die Standorteinstellungen so anpassen, dass die Richtlinie nur auf bestimmte Arbeitslasten oder auf bestimmte Websites und Konten angewendet wird.

![Optionen zum Auswählen bestimmter Standorte](media/DLP-create-test-tune-edit-locations.png)

Sie können auch die Richtlinieneinstellungen anpassen und die Regeln entsprechend Ihren Anforderungen bearbeiten.

![Option zum Bearbeiten der Regel](media/DLP-create-test-tune-edit-rule.png)

Beim Bearbeiten einer Regel in einer DLP-Richtlinie können Sie Folgendes ändern:

- Die Bedingungen, einschließlich des Typs und der Anzahl der Instanzen von vertraulichen Daten, die die Regel auslösen.
- Die Aktionen, die ausgeführt werden, beispielsweise das Einschränken des Zugriffs auf den Inhalt.
- Benutzer Benachrichtigungen, die dem Benutzer in seinem e-Mail-Client oder Webbrowser angezeigt werden.
- Benutzerüberschreibungen, die festlegen, ob Benutzer Ihre e-Mail-oder Dateifreigabe trotzdem fortsetzen können.
- Vorfallberichte, um Administratoren zu benachrichtigen.

![Optionen zum Bearbeiten von Teilen einer Regel](media/DLP-create-test-tune-editing-options.png)

Für diese Demo habe ich Benutzer Benachrichtigungen zu der Richtlinie hinzugefügt (seien Sie vorsichtig, dies ohne angemessene Benutzerschulung zu tun), und Benutzer können die Richtlinie mit einer geschäftlichen Begründung überschreiben oder als falsch positives Ergebnis kennzeichnen. Beachten Sie, dass Sie den e-Mail-und richtlinientipp Text auch anpassen können, wenn Sie zusätzliche Informationen zu den Richtlinien Ihrer Organisation hinzufügen möchten, oder Benutzer auffordern, den Support zu kontaktieren, wenn Sie Fragen haben.

![Optionen für Benutzer Benachrichtigungen und Außerkraftsetzungen](media/DLP-create-test-tune-user-notifications.png)

Die Richtlinie enthält zwei Regeln für die Behandlung von hohem Volumen und geringem Volumen, achten Sie daher darauf, beide mit den gewünschten Aktionen zu bearbeiten. Dies ist eine Möglichkeit, die Fälle abhängig von ihren Merkmalen unterschiedlich zu behandeln. Sie können beispielsweise Außerkraftsetzungen für geringste Verstöße zulassen, jedoch keine Außerkraftsetzungen für große Verstöße.

![Eine Regel für hohes Volumen und eine Regel für geringes Volumen](media/DLP-create-test-tune-two-rules.png)

Außerdem müssen Sie eine Aktion für die Regel konfigurieren, um den Zugriff auf Inhalte, die die Richtlinie verletzen, tatsächlich zu blockieren oder einzuschränken.

![Option zum Einschränken des Zugriffs auf Inhalte](media/DLP-create-test-tune-restrict-access-action.png)

Nachdem Sie diese Änderungen an den Richtlinieneinstellungen gespeichert haben, muss ich auch zur Seite mit den Haupteinstellungen für die Richtlinie zurückkehren und die Option zum Anzeigen von Richtlinien Tipps für Benutzer aktivieren, während sich die Richtlinie im Testmodus befindet. Dies ist ein effektives Verfahren, um Ihren Endbenutzern DLP-Richtlinien einzuführen und Benutzerschulungen durchzuführen, ohne zu viele falsch positive Ergebnisse zu riskieren, die sich auf Ihre Produktivität auswirken.

![Option zum Anzeigen von Richtlinien Tipps im Testmodus](media/DLP-create-test-tune-show-policy-tips.png)

Auf der Serverseite (oder auf der Cloud-Seite) wird die Änderung aufgrund verschiedener Verarbeitungsintervalle möglicherweise nicht sofort wirksam. Wenn Sie eine DLP-Richtlinienänderung vornehmen, die einem Benutzer neue Richtlinien Tipps anzeigt, werden die Änderungen möglicherweise nicht sofort in Ihrem Outlook-Client angezeigt, der alle 24 Stunden auf Richtlinienänderungen überprüft. Wenn Sie die Dinge zu Testzwecken beschleunigen möchten, können Sie diesen Registrierungs Fix verwenden, um [den Zeitstempel des letzten Downloads aus dem PolicyNudges-Schlüssel zu löschen](https://support.microsoft.com/en-au/help/2823261/changes-to-a-data-loss-prevention-policy-don-t-take-effect-in-outlook?__hstc=18650278.46377037dc0a82baa8a30f0ef07a7b2f.1538687978676.1538693509953.1540315763430.3&__hssc=18650278.1.1540315763430&__hsfp=3446956451). In Outlook werden die neuesten Richtlinieninformationen heruntergeladen, wenn Sie das nächste Mal neu gestartet werden, und mit dem Erstellen einer e-Mail-Nachricht beginnen.

Wenn Sie Richtlinien Tipps aktiviert haben, beginnt der Benutzer mit der Anzeige der Tipps in Outlook und kann Ihnen beim Auftreten falsch positive Ergebnisse melden.

![Richtlinientipp mit Option zum Melden von falsch positivem Ergebnis](media/DLP-create-test-tune-policy-tip-in-outlook.png)

## <a name="investigate-false-positives"></a>Untersuchen falsch positiver Ergebnisse

DLP-Richtlinienvorlagen sind direkt aus dem Feld nicht perfekt. Es ist wahrscheinlich, dass Sie einige falsch positive Ergebnisse in Ihrer Umgebung finden, weshalb es so wichtig ist, ihren Weg in eine DLP-Bereitstellung zu erleichtern, sich die Zeit nehmen, Ihre Richtlinien adäquat zu testen und zu optimieren.

Hier ist ein Beispiel für ein falsch positives Ergebnis. Diese e-Mail ist ziemlich harmlos. Der Benutzer stellt seine Mobiltelefonnummer einer Person zur Verfügung, einschließlich der e-Mail-Signatur.

![E-Mail-Nachricht mit falsch positiver Information](media/DLP-create-test-tune-false-positive-email.png)
 
Der Benutzer sieht jedoch einen richtlinientipp, der Sie warnt, dass die e-Mail vertrauliche Informationen enthält, insbesondere die Lizenznummer eines australischen Treibers.

![Option zum Melden von falsch positivem in richtlinientipp](media/DLP-create-test-tune-policy-tip-closeup.png)

Der Benutzer kann das falsch positive melden, und der Administrator kann sich ansehen, warum er aufgetreten ist. In der Vorfall Bericht-e-Mail wird die e-Mail als falsch positiv gekennzeichnet.

![Fehlerbericht mit falsch positivem Ergebnis](media/DLP-create-test-tune-false-positive-incident-report.png)

Dieser Führerschein Fall ist ein gutes Beispiel dafür. Der Grund für dieses falsch positive Ergebnis ist, dass der Typ "Australian Driver es License" von einer beliebigen 9-stelligen Zeichenfolge (sogar eine, die Teil einer 10-stelligen Zeichenfolge ist) ausgelöst wird, innerhalb von 300 Zeichen in der Nähe der Schlüsselwörter "Sydney NSW" (Groß-/Kleinschreibung nicht beachtet). Es wird also durch die Telefonnummer und die e-Mail-Signatur ausgelöst, nur weil der Benutzer zufällig in Sydney ist.

Interessant ist, dass die DLP-Richtlinie nicht ausgelöst wird, wenn "Sydney, NSW" ein Komma hat. Ich habe keine Ahnung, warum ein Komma hier einen Unterschied macht, noch warum andere Städte und Staaten in Australien nicht in die Schlüsselwörter für den australischen Treiber Lizenz-Informationstyp eingeschlossen sind, aber es geht los. Was können wir dagegen tun? Es gibt eine Reihe von Optionen.

Eine Option besteht darin, den Lizenz Informationstyp des australischen Treibers aus der Richtlinie zu entfernen. Er ist da, weil er Teil der DLP-Richtlinienvorlage ist, aber nicht dazu gezwungen ist. Wenn Sie nur an Steuerdatei Nummern und nicht an Treiber Lizenzen interessiert sind, können Sie Sie einfach entfernen. Sie können Sie beispielsweise aus der Regel für niedrige Volumes in der Richtlinie entfernen, aber in der Regel für hohe Volumes belassen, sodass Listen mit mehreren Treiber Lizenzen weiterhin erkannt werden.

![Option zum Löschen des Typs für vertrauliche Informationen aus der Regel](media/DLP-create-test-tune-delete-low-volume-rule.png)
 
Eine weitere Möglichkeit besteht darin, die Anzahl der Instanzen einfach zu erweitern, sodass ein niedriger Umfang an Treiber Lizenzen nur erkannt wird, wenn mehrere Instanzen vorhanden sind.

![Option zum Bearbeiten der instanzenanzahl](media/DLP-create-test-tune-edit-instance-count.png)

Sie können nicht nur die Anzahl der Instanzen ändern, sondern auch die Übereinstimmungs Genauigkeit (oder Zuverlässigkeitsstufe) anpassen. Wenn der Typ vertraulicher Informationen mehrere Muster aufweist, können Sie die Übereinstimmungs Genauigkeit in der Regel anpassen, sodass die Regel nur bestimmten Mustern entspricht. Um beispielsweise falsch positive Ergebnisse zu vermeiden, können Sie die Übereinstimmungs Genauigkeit der Regel so festlegen, dass nur das Muster mit der höchsten Zuverlässigkeitsstufe übereinstimmt. Zu verstehen, wie die Zuverlässigkeitsstufe berechnet wird, ist ein wenig heikel (und jenseits des Bereichs dieses Beitrags), aber hier ist eine gute Erklärung dafür, wie Sie die [Vertraulichkeitsstufe verwenden, um ihre Regeln zu optimieren](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#match-accuracy).

Schließlich können Sie einen beliebigen vertraulichen Informationstyp anpassen – beispielsweise "Sydney NSW" aus der Liste der Schlüsselwörter für [Australian Driver es License](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for#australia-drivers-license-number)entfernen, um das oben ausgelöste falsch positive Ergebnis zu vermeiden. Informationen dazu, wie Sie dies mithilfe von XML und PowerShell tun können, finden Sie in diesem Thema unter [Anpassen eines integrierten vertraulichen Informationstyps](customize-a-built-in-sensitive-information-type.md).

## <a name="turn-off-a-dlp-policy"></a>Deaktivieren einer DLP-Richtlinie

Wenn Sie sich darüber freuen, dass ihre DLP-Richtlinie vertrauliche Informationstypen genau und effektiv ermittelt und die Endbenutzer bereit sind, die Richtlinien zu behandeln, die vorhanden sind, können Sie die Richtlinie aktivieren.

![Option zum Aktivieren der Richtlinie](media/DLP-create-test-tune-turn-on-policy.png)
 
Wenn Sie warten, bis die Richtlinie wirksam wird, stellen Sie [eine Verbindung zur Security _AMP_ Compliance Center-PowerShell her](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps) , und führen Sie das [Cmdlet Get-DlpCompliancePolicy](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/get-dlpcompliancepolicy?view=exchange-ps) aus, um die Eigenschaften distributionstatus anzuzeigen.

![Ausführen des Cmdlets in PowerShell](media/DLP-create-test-tune-PowerShell.png)

Nach dem Aktivieren der DLP-Richtlinie sollten Sie einige abschließende Tests durchführen, um sicherzustellen, dass die erwarteten Richtlinienaktionen ausgeführt werden. Wenn Sie versuchen, Dinge wie Kreditkartendaten zu testen, gibt es Websites online mit Informationen zum Generieren von Beispiel Kreditkarten oder anderen persönlichen Informationen, die Prüfsummen überschreiten und ihre Richtlinien auslösen.

Durch Richtlinien, die Benutzerüberschreibungen zulassen, wird diese Option dem Benutzer als Teil des Richtlinien Tipps angezeigt.

![Richtlinientipp, der eine Benutzer Überschreibung ermöglicht](media/DLP-create-test-tune-override-option.png)

Durch Richtlinien, die Inhalte einschränken, wird dem Benutzer die Warnung als Teil des Richtlinien Tipps angezeigt und verhindert, dass diese e-Mails gesendet werden.

![Richtlinientipp, dass Inhalte eingeschränkt sind](media/DLP-create-test-tune-restrict-warning.png)

## <a name="summary"></a>Zusammenfassung

Richtlinien zur Verhinderung von Datenverlust sind für Organisationen aller Typen nützlich. Das Testen einiger DLP-Richtlinien ist aufgrund der Kontrolle, die Sie über die Richtlinien Tipps, Endbenutzer Überschreibungen und vorfallberichte haben, mit einem geringen Risiko verbunden. Sie können einige DLP-Richtlinien ruhig testen, um zu sehen, welche Art von Verstößen bereits in Ihrer Organisation vorkommt, und dann Richtlinien mit niedrigen falsch positiven Raten durchführen, Ihre Benutzer über das erlaubte und nicht zugelassene informieren und dann ihre DLP-Richtlinien auf die Organisation.
