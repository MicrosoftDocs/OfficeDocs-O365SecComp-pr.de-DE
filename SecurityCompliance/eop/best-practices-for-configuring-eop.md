---
title: Bewährte Methoden für das Konfigurieren von EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: faf1efd1-3b0c-411a-804d-17f37292eac0
description: Beachten Sie die folgenden Empfehlungen für Exchange Online Protection (EOP), um allgemeine Konfigurationsfehler zu vermeiden und eine erfolgreiche Funktion zu gewährleisten.
ms.openlocfilehash: d58b03d4ac3e11c863cec32430236ca9f0cea13e
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670710"
---
# <a name="best-practices-for-configuring-eop"></a>Bewährte Methoden für das Konfigurieren von EOP
  
Beachten Sie die folgenden Empfehlungen für Exchange Online Protection (EOP), um allgemeine Konfigurationsfehler zu vermeiden und eine erfolgreiche Funktion zu gewährleisten. Es ist grundsätzlich empfehlenswert, die Standardkonfigurationseinstellungen zu verwenden. In diesem Thema wird vorausgesetzt, dass Sie den Setup-Prozess bereits abgeschlossen haben. Wenn Sie das EOP-Setup nicht abgeschlossen haben, finden Sie weitere Informationen unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md).
  
## <a name="use-a-test-domain"></a>Verwenden einer Testdomäne

Es wird empfohlen, eine Testdomäne, eine Unterdomäne oder eine Domäne von geringem Volumen zu verwenden, um Dienstfunktionen zu prüfen, bevor Sie sie auf Ihren Produktionsdomänen mit höherem Volumen implementieren.
  
## <a name="synchronize-recipients"></a>Synchronisieren von Empfängern

Wenn Ihre Organisation über vorhandene Benutzerkonten in einer lokalen Active Directory-Umgebung verfügt, können Sie diese Konten mit Azure Active Directory in der Cloud synchronisieren. Es wird empfohlen, Verzeichnissynchronisierung zu verwenden. Weitere Informationen über die Vorteile der Verzeichnissynchronisierung und über die Schritte zu ihrer Einrichtung finden Sie unter [Verwalten von E-Mail-Benutzern in EOP](manage-mail-users-in-eop.md).
  
## <a name="spf-record-customization-to-help-prevent-spoofing"></a>SPF-Eintrags-Anpassung zur Verhinderung von Spoofing

Bei der Einrichtung von EOP haben Sie zu Ihren DNS-Datensätzen einen SPF-Datensatz (Sender Policy Framework) für EOP hinzugefügt. Der SPF-Datensatz erleichtert die Vermeidung von Spoofing. Weitere Informationen dazu, wie ein SPF-Eintrag Spoofing verhindert und wie Sie Ihre lokalen IP-Adressen dem SPF-Eintrag hinzufügen können, finden Sie unter [Einrichten von SPF in Office 365, um Spoofing zu verhindern](../set-up-spf-in-office-365-to-help-prevent-spoofing.md). 
  
## <a name="set-anti-spam-options"></a>Festlegen von Antispamoptionen

Verwalten Sie die Filter der Verbindungseinstellungen durch das Hinzufügen von IP-Adressen zur IP-Zulassungs- und IP-Sperrliste, indem Sie die Option **Liste sicherer Adressen** aktivieren, wodurch die Anzahl der falsch positiven Nachrichten (Nachrichten, die fälschlicherweise als Spam eingestuft werden) reduziert werden sollte. Weitere Informationen finden Sie unter [configure the Connection Filter Policy](../configure-the-connection-filter-policy.md). Weitere Antispameinstellungen, die für die gesamte Organisation gelten, finden Sie unter [Sicherstellen, dass eine Nachricht nicht als Spam gekennzeichnet wird](https://go.microsoft.com/fwlink/p/?LinkId=534224) oder [Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zum Verhindern von falsch negativen Ergebnissen](https://go.microsoft.com/fwlink/p/?LinkId=534225). Diese sind hilfreich, wenn Sie Administratorebenen-Kontrolle haben und falsch positive oder falsch negative Ergebnisse vermeiden möchten.
  
Verwalten Sie Ihre Inhaltsfilter, indem Sie die Standardeinstellungen überprüfen und optional ändern. Sie können beispielsweise die Aktion für das geschehen mit Spam erkannten Nachrichten ändern. Wenn Sie einen aggressiven Ansatz für die Spamfilterung verfolgen möchten, können Sie Erweiterte Spam Filterungsoptionen konfigurieren. Es wird empfohlen, diese Optionen zuerst zu testen, bevor Sie Sie in Ihrer Produktionsumgebung implementieren (indem Sie Sie aktivieren), es wird empfohlen, dass Organisationen, die sich um Phishing kümmern, die Option **SPF-Eintrag: harter Fehler** aktivieren. Weitere Informationen finden Sie unter [configure your Spamfilter Policies](../configure-your-spam-filter-policies.md) and [Advanced Spam Filtering Options](../advanced-spam-filtering-asf-options.md).
  
> [!IMPORTANT]
> Wenn Sie die standardmäßige Inhaltsfilteraktion, **Nachricht in Junk-e-Mail-Ordner verschieben**, um sicherzustellen, dass diese Aktion mit lokalen Postfächern funktioniert, müssen Sie Exchange-Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) in Ihrer lokalen Konfiguration konfigurieren. Server zum Aufspüren von Spam Kopfzeilen, die von EOP hinzugefügt wurden. Weitere Informationen finden Sie unter [Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
Wir empfehlen, die Antispamschutz [-FAQ](../anti-spam-protection-faq.md)zu lesen, einschließlich des Abschnitts "Best Practices für ausgehende Nachrichten", um sicherzustellen, dass Ihre ausgehenden e-Mails zugestellt werden.
  
Sie können falsche negative Meldungen (Spam) und falsche positive Meldungen (kein Spam) auf verschiedene Weise an Microsoft zur Analyse schicken. Weitere Informationen finden Sie unter [Submit Spam, Non-Spam, and Phishing Scam messages to Microsoft for Analysis](../submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).
  
## <a name="set-anti-malware-options"></a>Festlegen von Antimalwareoptionen

Sie können Ihre Malwarefiltereinstellungen in der Exchange-Verwaltungskonsole (EAC) überprüfen und anpassen. Weitere Informationen finden Sie unter [configure Anti-Malware Policies](../configure-anti-malware-policies.md). Wir empfehlen auch, sich über andere häufig gestellte Fragen und Antworten im Zusammenhang mit dem Schutz vor Schadsoftware zu verständigen. [ ](../anti-malware-protection-faq-eop.md)
  
Wenn Sie befürchten, dass ausführbare Dateien Schadsoftware enthalten könnten, können Sie eine Exchange-Nachrichtenflussregel erstellen, durch die alle E-Mail-Anhänge mit ausführbaren Inhalten blockiert werden. Führen Sie die Schritte in [How to Reduce Malware Threats through File Attachment Blocking in Exchange Online Protection](https://support.microsoft.com/kb/2959596) aus, um die in [use Mail Flow Rules aufgeführten Dateitypen zum Überprüfen von Nachrichtenanlagen in Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection)zu blockieren.
  
Sie können den Filter für gängige Anlagetypen in der Exchange-Verwaltungskonsole verwenden. Wählen Sie **Schutz** \> **Schadsoftwarefilter**. Sie können eine e-Mail-Fluss Regel erstellen, die alle e-Mail-Anlagen blockiert, die ausführbare Inhalte aufweisen. 
  
Für einen höheren Schutz empfehlen wir, auch einige oder alle der folgenden Erweiterungen mithilfe von Nachrichtenflussregeln zu blockieren: ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh. Dies kann mithilfe der Bedingung **Mindestens eine Anlage... eine Dateierweiterung hat, die diese Wörter enthält** erfolgen. 
  
Administratoren und Endbenutzer können Malware, die an den Filtern vorbei gelangt ist, oder Dateien, die fälschlicherweise als Malware erkannt wurden, zur Analyse an Microsoft übermitteln. Weitere Informationen finden Sie unter [Submitting malware and non-malware to Microsoft for analysis](../submitting-malware-and-non-malware-to-microsoft-for-analysis.md).
  
## <a name="create-mail-flow-rules"></a>Erstellen von Nachrichtenflussregeln

Erstellen Sie Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) oder benutzerdefinierte Filter, um Ihre geschäftlichen Anforderungen zu erfüllen.
  
Wenn Sie eine neue Regel in die Produktion übernehmen, wählen Sie zunächst einen der Testmodi aus, um die Wirkung der Regeln zu überprüfen. Wenn Sie sicher sind, dass die Regel so funktioniert wie beabsichtigt, ändern Sie den Regelmodus in **Erzwingen**.
  
Beim Bereitstellen neuer Regeln sollten Sie in Erwägung ziehen, als zusätzliche Aktion **Schadensbericht generieren** hinzuzufügen, um die betreffende Regel zu überwachen. 
  
Bei der Konfiguration einer Hybridbereitstellung, bei der ein Teil der Organisation lokal und ein Teil in Office 365 verwaltet wird, können Sie Regeln erstellen, die sich auf die gesamte Organisation anwenden lassen. Dies ist nur möglich, wenn Sie Bedingungen verwenden, die sowohl lokal als auch in Office 365 verfügbar sind. Die meisten Bedingungen stehen zwar in beiden Bereitstellungen zur Verfügung, doch sind einige davon nur für bestimmte Bereitstellungsszenarien geeignet. Weitere Informationen finden Sie unter [Nachrichtenfluss Regeln (Transportregeln) in Exchange Online](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
Wenn Sie in Ihrer Organisation E-Mail-Anlagen von Nachrichten während der Übermittlung überprüfen möchten, können Sie dazu Nachrichtenflussregeln einrichten. Führen Sie dann Aktionen für die überprüften Nachrichten basierend auf deren Inhalten oder Merkmalen dieser Anlagen durch. Weitere Informationen finden Sie unter [Use mail flow rules to inspect message attachments](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx).
  
### <a name="phishing-and-spoofing-prevention"></a>Schutz vor Phishing und Spoofing

Sie können den Antiphishingschutz verbessern, indem Sie ermitteln, wann persönliche Informationen die Organisation in einer E-Mail verlassen. Beispielsweise können Sie die folgenden normalen Ausdrücke in Nachrichtenflussregeln verwenden, um die Übertragung persönlicher Finanzdaten oder Informationen, die urheberrechtlich geschützte Daten enthalten, zu erkennen:
  
- \d\d\d\d\s\d\d\d\d\s\d\d\d\d\s\d\d\d\d (MasterCard Visa)
    
- \d\d\d\d\s\d\d\d\d\d\d\s\d\d\d\d\d (American Express)
    
- \d\d\d\d\d\d\d\d\d\d\d\d\d\d\d\d (eine beliebige 16-stellige Zahl)
    
- \d\d\d\-\d\d\-\d\d\d\d (Sozialversicherungsnummern)
    
Spam und Phishing können ebenfalls durch Blockieren eingehender bösartiger E-Mails erfolgreich verhindert werden, die scheinbar von Ihrer eigenen Domäne gesendet wurden. Sie können zum Beispiel eine Nachrichtenflussregel erstellen, die Nachrichten von Ihrer Firmendomäne an dieselbe Firmendomäne ablehnt, um diese Art von Absenderfilterung zu blockieren.
  
> [!CAUTION]
> Wir empfehlen Ihnen, diese Regel nur in solchen Fällen zu erstellen, in denen Sie sicher sind, dass keine legitime E-Mail von Ihrer Domäne über das Internet an Ihrem Mailserver gesendet wird. Dies kann in Fällen passieren, in denen eine Nachricht von einem Benutzer in Ihrer Organisation an einen externen Empfänger gesendet und anschließend an einen anderen Empfänger in Ihrer Organisation weitergeleitet wird. 
  
### <a name="extension-blocking"></a>Erweiterungsblockierung

Wenn Sie befürchten, dass ausführbare Dateien Schadsoftware enthalten könnten, können Sie Antischadsoftwarerichtlinien erstellen, durch die alle E-Mail-Anhänge mit ausführbaren Inhalten blockiert werden. Führen Sie die Schritte unter [configure Anti-Malware Policies](../configure-anti-malware-policies.md)aus.
  
Für einen höheren Schutz empfehlen wir, auch einige oder alle der folgenden Erweiterungen zu blockieren: ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh.
  
## <a name="reporting-and-troubleshooting"></a>Berichterstellung und Problembehandlung

Behandeln allgemeiner Probleme und Trends mithilfe der Berichte im Admin Center. Mithilfe des Nachrichtenablaufverfolgungs-Tools können Sie nach einzelnen quellenspezifischen Daten zu einer Nachricht suchen. Weitere Informationen zu Berichten finden Sie unter [Berichterstellung und Nachrichtenablaufverfolgung in Exchange Online Protection](reporting-and-message-trace-in-exchange-online-protection.md). Weitere Informationen zum Nachrichtenablaufverfolgungs-Tool finden Sie unter [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx).
  
## <a name="for-more-information"></a>Weitere Informationen

[EOP - Allgemeine häufig gestellte Fragen](eop-general-faq.md)
  
[Hilfe und Support für EOP](help-and-support-for-eop.md)
  
[Videos für erste Schritte mit EOP](videos-for-getting-started-with-eop.md)
  
[So können Sie dazu beitragen, dass eine Nachricht nicht als Spam gekennzeichnet wird](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

