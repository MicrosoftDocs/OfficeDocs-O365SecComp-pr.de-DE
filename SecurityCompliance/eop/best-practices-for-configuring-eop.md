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
ms.openlocfilehash: ef58e2cd5a3ffdbbeb02124442c355974d174073
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027272"
---
# <a name="best-practices-for-configuring-eop"></a>Bewährte Methoden für das Konfigurieren von EOP
  
Beachten Sie die folgenden Empfehlungen für Exchange Online Protection (EOP), um allgemeine Konfigurationsfehler zu vermeiden und eine erfolgreiche Funktion zu gewährleisten. Es ist grundsätzlich empfehlenswert, die Standardkonfigurationseinstellungen zu verwenden. In diesem Thema wird vorausgesetzt, dass Sie den Setup-Prozess bereits abgeschlossen haben. Wenn Sie das EOP-Setup nicht abgeschlossen haben, finden Sie weitere Informationen unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md).
  
## <a name="use-a-test-domain"></a>Verwenden einer Testdomäne

Es wird empfohlen, eine Testdomäne, eine Unterdomäne oder eine Domäne von geringem Volumen zu verwenden, um Dienstfunktionen zu prüfen, bevor Sie sie auf Ihren Produktionsdomänen mit höherem Volumen implementieren.
  
## <a name="synchronize-recipients"></a>Synchronisieren von Empfängern

Wenn Ihre Organisation über vorhandene Benutzerkonten in einer lokalen Active Directory-Umgebung verfügt, können Sie diese Konten mit Azure Active Directory in der Cloud synchronisieren. Es wird empfohlen, Verzeichnissynchronisierung zu verwenden. Weitere Informationen über die Vorteile der Verzeichnissynchronisierung und über die Schritte zu ihrer Einrichtung finden Sie unter [Verwalten von E-Mail-Benutzern in EOP](manage-mail-users-in-eop.md).
  
## <a name="spf-record-customization-to-help-prevent-spoofing"></a>SPF-Eintrags-Anpassung zur Verhinderung von Spoofing

Wenn Sie EOP eingerichtet haben, werden einen SPF (Sender Policy Framework)-Eintrag für EOP Ihren DNS-Einträgen hinzugefügt. Der SPF-Datensatz hilft spoofing zu verhindern. Weitere Informationen wie ein SPF-Datensatzes verhindert spoofing und wie Sie Ihre lokale IP-Adressen der SPF-Datensatz hinzufügen können finden Sie unter [Einrichten von SPF in Office 365, um spoofing zu verhindern](../set-up-spf-in-office-365-to-help-prevent-spoofing.md). 
  
## <a name="set-anti-spam-options"></a>Festlegen von Antispamoptionen

Des Umgangs mit Filtern die Verbindung Einstellungen durch zugelassene IP-Adressen und IP-Sperrlisten IP-Adressen hinzugefügt und durch Auswählen der Option **Liste sicheren aktivieren** , die sollte die Anzahl der falsch positive Ergebnisse (unbedenkliche e-Mails, die als Spam klassifiziert ist) reduzieren Sie erhalten. Weitere Informationen finden Sie unter [Konfigurieren der verbindungsfilterrichtlinie](../configure-the-connection-filter-policy.md). Sehen Sie für weitere Spameinstellungen, die für die gesamte Organisation gelten sich die [Vorgehensweise dazu beitragen, dass eine Nachricht als Spam gekennzeichnet ist nicht](https://go.microsoft.com/fwlink/p/?LinkId=534224) oder [e-Mail-Nachrichten mit dem Office 365-Spam-Filter auf false negative Probleme zu verhindern, dass spam blockieren](https://go.microsoft.com/fwlink/p/?LinkId=534225). Dies sind hilfreich, wenn Sie falsch positive Ergebnisse oder falsch negative verhindern möchten, und Sie auf Administratorebene-Steuerelement haben.
  
Verwalten von Inhaltsfilter überprüfen und optional ändern die Standardeinstellungen. Beispielsweise können Sie die Aktion für was, als Spam erkannten Nachrichten passiert ändern. Wenn Sie einen aggressiven Ansatz zum Filtern von Spam-verfolgen möchten, können Sie erweiterte spamfilterungsoptionen konfigurieren. Es wird empfohlen, dass Sie diese Optionen zuerst vor deren Implementierung in Ihrer produktionsumgebung (durch Klicken auf aktivieren) Es wird empfohlen, dass Organisationen, die betreffenden Informationen zu Phishing sind aktivieren Testen der **SPF-Datensatz: Schwerer Fehler** Option. Weitere Informationen finden Sie unter [Konfigurieren Ihrer Spam-Filter-Richtlinien](../configure-your-spam-filter-policies.md) und [Erweiterte Optionen für Spamfilterung](../advanced-spam-filtering-asf-options.md).
  
> [!IMPORTANT]
> Wenn Sie, um sicherzustellen, dass diese Aktion mit lokalen Postfächern die Inhaltsfilter Standardaktion **Nachricht in Junk-e-Mail-Ordner verschieben**möchten, verwenden, müssen Sie auch als Transportregeln, bezeichnet, auf dem lokalen Exchange Mail Flow Regeln konfigurieren. Server zum Erkennen von Spam-Headern von EOP gefiltert werden hinzugefügt. Weitere Informationen hierzu finden Sie unter [sicherstellen, dass Spam an die Junk-e-Mail-Ordner des Benutzers weitergeleitet wird](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
Es wird empfohlen, dass Sie überprüfen des [Anti-Spam Protection FAQ](../anti-spam-protection-faq.md), einschließlich des ausgehenden Adressetiketts besten Practices Abschnitts, der hilft sicherzustellen, dass Ihre ausgehende Nachrichten übermittelt werden.
  
Sie können falsch negative (Spam) und falsch positive Ergebnisse (nicht-Spam) an Microsoft zur Analyse auf verschiedene Weise übermitteln. Weitere Informationen hierzu finden Sie unter [Submit Spam, nicht-Spam und Phishing-Betrug Nachrichten an Microsoft zur Analyse](../submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).
  
## <a name="set-anti-malware-options"></a>Festlegen von Antimalwareoptionen

Überprüfen und Feinabstimmung Ihrer filtereinstellungen für Schadsoftware in der Exchange-Admin-center(EAC). Weitere Informationen finden Sie unter [Configure Anti-Malware Policies](../configure-anti-malware-policies.md). Es wird empfohlen, Informationen zu anderen häufig gestellte Fragen und Antworten zur Anti-Malware Protection unserer [Anti-Malware Protection FAQ ](../anti-malware-protection-faq-eop.md)gelesen wird.
  
Wenn Sie befürchten, dass ausführbare Dateien Schadsoftware enthalten könnten, können Sie eine Exchange-Nachrichtenflussregel erstellen, durch die alle E-Mail-Anhänge mit ausführbaren Inhalten blockiert werden. Führen Sie die Schritte in [Reduzieren von Malware-Bedrohungen durch Dateianhangblockierung in Exchange Online Protection](https://support.microsoft.com/kb/2959596) aus, um die unter "Unterstützte ausführbare Dateitypen für die Überprüfung mit Transportregeln" in [Use mail flow rules to inspect message attachments](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx) aufgelisteten Dateitypen zu blockieren.
  
Sie können den Filter für gängige Anlagetypen in der Exchange-Verwaltungskonsole verwenden. Wählen Sie **Schutz** \> **Schadsoftwarefilter**. Sie können eine Exchange-Nachrichtenflussregel, auch als Transportregel bezeichnet, erstellen, durch die alle E-Mail-Anhänge mit ausführbarem Inhalt blockiert werden. 
  
Für einen höheren Schutz empfehlen wir, auch einige oder alle der folgenden Erweiterungen mithilfe von Nachrichtenflussregeln zu blockieren: ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh. Dies kann mithilfe der Bedingung **Mindestens eine Anlage... eine Dateierweiterung hat, die diese Wörter enthält** erfolgen. 
  
Administratoren und Endbenutzer können Malware, die an den Filtern vorbei gelangt ist, oder Dateien, die fälschlicherweise als Malware erkannt wurden, zur Analyse an Microsoft übermitteln. Weitere Informationen finden Sie unter [Submitting malware and non-malware to Microsoft for analysis](../submitting-malware-and-non-malware-to-microsoft-for-analysis.md).
  
## <a name="create-mail-flow-rules"></a>Erstellen von Nachrichtenflussregeln

Erstellen Sie Nachrichtenflussregeln, die auch als Transportregeln oder benutzerdefinierte Filter bezeichnet werden, um den Anforderungen Ihres Unternehmens gerecht zu werden.
  
Wenn Sie eine neue Regel in die Produktion übernehmen, wählen Sie zunächst einen der Testmodi aus, um die Wirkung der Regeln zu überprüfen. Wenn Sie sicher sind, dass die Regel so funktioniert wie beabsichtigt, ändern Sie den Regelmodus in **Erzwingen**.
  
Beim Bereitstellen neuer Regeln sollten Sie in Erwägung ziehen, als zusätzliche Aktion **Schadensbericht generieren** hinzuzufügen, um die betreffende Regel zu überwachen. 
  
Bei der Konfiguration einer Hybridbereitstellung, bei der ein Teil der Organisation lokal und ein Teil in Office 365 verwaltet wird, können Sie Regeln erstellen, die sich auf die gesamte Organisation anwenden lassen. Dies ist nur möglich, wenn Sie Bedingungen verwenden, die sowohl lokal als auch in Office 365 verfügbar sind. Die meisten Bedingungen stehen zwar in beiden Bereitstellungen zur Verfügung, doch sind einige davon nur für bestimmte Bereitstellungsszenarien geeignet. Weitere Informationen finden Sie unter [Mail flow or Transport rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
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

Wenn Sie ausführbare Dateien mit Malware besorgt sind, können Sie Antischadsoftware-Richtlinien, um mindestens eine e-Mail-Anlage zu blockieren, die hat ausführbaren Inhalt konfigurieren. Führen Sie die Schritte unter [Configure Anti-Malware Policies](../configure-anti-malware-policies.md).
  
Für einen höheren Schutz empfehlen wir, auch einige oder alle der folgenden Erweiterungen zu blockieren: ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh.
  
## <a name="reporting-and-troubleshooting"></a>Berichterstellung und Problembehandlung

Mithilfe der Berichte im Office 365 Admin Center können Sie allgemeine Probleme und Trends beheben. Mithilfe des Nachrichtenablaufverfolgungs-Tools können Sie nach einzelnen quellenspezifischen Daten zu einer Nachricht suchen. Weitere Informationen zu Berichten finden Sie unter [Berichterstellung und Nachrichtenablaufverfolgung in Exchange Online Protection](reporting-and-message-trace-in-exchange-online-protection.md). Weitere Informationen zum Nachrichtenablaufverfolgungs-Tool finden Sie unter [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx).
  
## <a name="for-more-information"></a>Weitere Informationen

[EOP - Allgemeine häufig gestellte Fragen](eop-general-faq.md)
  
[Hilfe und Support für EOP](help-and-support-for-eop.md)
  
[Videos für erste Schritte mit EOP](videos-for-getting-started-with-eop.md)
  
[So können Sie dazu beitragen, dass eine Nachricht nicht als Spam gekennzeichnet wird](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

