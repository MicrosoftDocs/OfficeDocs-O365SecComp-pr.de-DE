---
title: Bewährte Methoden für die Sicherheit in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: Minimieren Sie das Potenzial einer Datenverletzung oder eines kompromittierten Kontos, indem Sie diese empfohlenen bewährten Methoden befolgen.
ms.openlocfilehash: d40fa5e4534bef1bb8389989022c44967a162aee
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212815"
---
# <a name="security-best-practices-for-office-365"></a>Bewährte Methoden für die Sicherheit in Office 365

Minimieren Sie das Potenzial einer Datenverletzung oder eines kompromittierten Kontos, indem Sie diese empfohlenen bewährten Methoden befolgen.
  
Dieser Artikel enthält eine kurze Liste der bewährten Methoden. Ausführlichere Analysen und Informationen zum Einrichten der Sicherheit finden Sie unter [Office 365 Security Roadmap: Top-Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus](security-roadmap.md). In diesem Artikel finden Sie Informationen basierend auf Untersuchungen von realen Angriffen, bei denen unsere Top-Experten von Microsoft Office 365 Cyber Coachings zur Bewertung von Risiken und zur Implementierung der wichtigsten Sicherheits-, Compliance-und Informationsdaten bieten. Schutz Steuerelemente zum Schutz Ihres Office 365-Mandanten. Hier erfahren Sie, wie Sie Bedrohungen priorisieren, Bedrohungen in die technische Strategie umsetzen und dann einen systematischen Ansatz für die Implementierung von Features und Steuerelementen einleiten.
  
## <a name="use-office-365-secure-score"></a>Verwenden von Office 365 Secure Score

Secure Score ist ein Sicherheitsanalysetool, das empfiehlt, was Sie tun können, um das Risiko weiter zu reduzieren. Secure Score betrachtet Ihre Office 365-Einstellungen und-Aktivitäten und vergleicht sie mit einer von Microsoft festgelegten Baseline. Sie erhalten eine Bewertung basierend darauf, wie Sie mit den besten Sicherheitsmethoden ausgerichtet sind. Weitere Informationen dazu, wie Sie die Sicherheit Ihrer Office 365-Organisation sicherstellen und verwenden können, finden Sie unter [Einführung in die office 365 Secure Score](office-365-secure-score.md).
  
Möchten Sie die sichere Bewertung testen?
  
Melden Sie sich bei einem Arbeits-oder Schulkonto, dem die Rolle Office 365 [zu office 365-Administratorrollen](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) zugewiesen wurde, [bei Office 365 an](https://www.office.com/signin).
  
Access Secure Score bei [https://SecureScore.office.com](https://SecureScore.office.com).
  
## <a name="use-multi-factor-authentication-mfa"></a>Mehrstufige Authentifizierung (MFA)

MFA fügt eine zusätzliche Schutzebene für eine starke Kenn Wort Strategie hinzu, indem Benutzer aufgefordert werden, einen Telefonanruf, eine Textnachricht oder eine APP-Benachrichtigung auf Ihrem Smartphone zu bestätigen, nachdem Sie das Kennwort richtig eingegeben haben. Bei Verwendung von MFA werden Office 365-Benutzerkonten auch dann noch vor unbefugtem Zugriff geschützt, wenn das Kennwort eines Benutzers kompromittiert wurde. Konten werden geschützt, da der Zugriff erst dann einem Konto gewährt wird, nachdem die zusätzliche Herausforderung erfüllt wurde. Ein kompromittiertes oder gestohlenes Kennwort genügt nicht.
  
- [Planen der mehrstufigen Authentifizierung für Office 365-Bereitstellungen](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Einrichten der mehrstufigen Authentifizierung für Office 365-Benutzer](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a>Verwenden von Office 365 Cloud App Security

Einrichten von Richtlinien basierend auf Ihren geschäftlichen Anforderungen, um anomale Aktivitäten nachzuverfolgen und darauf zu reagieren. Richten Sie Warnungen mit Office 365 Cloud App Security ein, damit Administratoren ungewöhnliche oder riskante Benutzeraktivitäten wie das Herunterladen umfangreicher Datenmengen, mehrere fehlgeschlagene Anmeldeversuche oder Anmeldungen von einer unbekannten oder gefährlichen IP-Adresse überarbeiten können. Für Organisationen mit einem Office 365 Enterprise E5-Plan können Sie sofort mit der Verwendung von Office 365 Cloud App Security beginnen. Wenn Sie über einen anderen Enterprise-Plan verfügen, können Sie Office 365 Cloud App Security als Add-on erwerben.
  
- [Übersicht über die O365-Cloud-App-Sicherheit](office-365-cas-overview.md)
    
- [Aktivieren von Office 365 Cloud App Security](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a>Sicherer Nachrichtenfluss

Implementieren Sie die umfangreichen Features, die in Exchange Online Protection festgelegt sind, und erhalten Sie mehr Sicherheit über die Identität des Absenders der einzelnen e-Mail-Nachrichten, und schützen Sie vor unbekannten Schadsoftware, Viren und bösartigen URLs, die über e-Mails übertragen
  
- Konfigurieren von Richtlinien für [e-Mail-Antispamschutz für Office 365](anti-spam-protection.md) für Ihre Organisation. 
    
- Erfahren Sie mehr über und verwenden Sie dann [Advanced Threat Protection für sichere Anlagen und sichere Links](https://technet.microsoft.com/library/mt148491.aspx).
    
- [Fügen Sie der Organisation den Schutz vor schadSoftware hinzu](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).
    
- Informieren Sie sich über und aktivieren Sie [Sicherheitstipps in e-Mail-Nachrichten in Office 365](safety-tips-in-office-365.md) für Ihre Benutzer. 
    
- Wenn Sie in Office 365 eine benutzerdefinierte Domäne für Ihre Organisation verwenden, richten Sie SPF, DKIM und dann DMARC ein, um von Ihrer Organisation gesendete e-Mails zu überprüfen und Spoofing zu verhindern:
    
  - [Richten Sie SPF in Office 365 ein, um Spoofing zu verhindern](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Verwenden Sie DKIM zum Überprüfen ausgehender e-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet werden](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Verwenden Sie DMARC, um e-Mails in Office 365 zu überprüfen](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
## <a name="enable-mailbox-audit-logging"></a>Aktivieren der Postfachüberwachungsprotokollierung

Einige Überwachungsprotokollierung wird automatisch für Sie in Office 365 aktiviert; die postfachüberwachungsprotokollierung ist jedoch nicht standardmäßig aktiviert. Sie aktivieren die Überwachungsprotokollierung für alle Benutzerpostfächer in Office 365 mithilfe von Exchange Online PowerShell. Weitere Informationen finden Sie unter [Aktivieren der postfachüberwachung in Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
Nachdem Sie die Überwachungsprotokollierung aktiviert haben, können Sie [das Überwachungsprotokoll im Office 365 Security &amp; Compliance Center durchsuchen](search-the-audit-log-in-security-and-compliance.md) , um herauszufinden, wer sich an Ihren Benutzerpostfächern, gesendeten Nachrichten und anderen Aktivitäten angemeldet hat, die vom Postfachbesitzer, einem Delegierten Benutzer, ausgeführt wurden. oder ein Administrator. Eine Liste der Postfachaktivitäten, die im Office 365-Überwachungsprotokoll standardmäßig enthalten sind, finden Sie unter [Exchange Mailbox Activities](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).
  
Informationen zu anderen Aktionen, die Sie mit dem Überwachungsprotokoll ausführen können, wie beispielsweise Ändern der Zeitdauer zum Speichern von Einträgen im Überwachungsprotokoll, finden Sie unter [Mailbox Audit Logging in Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).
  
## <a name="configure-data-loss-prevention-dlp"></a>Konfigurieren von Data Loss Prevention (DLP)

Mit DLP können Sie vertrauliche Daten identifizieren und Richtlinien erstellen, die verhindern, dass Ihre Benutzer versehentlich oder absichtlich die Daten freigeben. DLP funktioniert in Office 365, einschließlich Exchange Online, SharePoint Online und OneDrive, sodass Ihre Benutzer kompatibel bleiben können, ohne Ihren Workflow zu unterbrechen. Weitere Informationen finden Sie unter [Übersicht über Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md).
  
## <a name="use-customer-lockbox"></a>Kunden-Lockbox verwenden

Als Office 365-Administrator können Sie mit der Customer Lockbox steuern, wie ein Microsoft-Supporttechniker während einer Hilfesitzung auf Ihre Daten zugreift. In Fällen, in denen der Techniker Zugriff auf Ihre Daten benötigt, um ein Problem zu behandeln und zu beheben, können Sie mit der Kunden-Lockbox die Zugriffsanforderung genehmigen oder ablehnen. Wenn Sie es genehmigen, kann der Techniker auf die Daten zugreifen. Jede Anforderung hat eine Ablaufzeit, und nachdem das Problem behoben wurde, wird die Anforderung geschlossen, und der Zugriff wird widerrufen. Kunden-Lockbox ist im Office 365 Enterprise E5-Plan enthalten, oder Sie können ein separates Abonnement mit einem beliebigen anderen Office 365 Enterprise-Plan erwerben. Weitere Informationen finden Sie unter [Office 365-Kunden](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2)-lockBox-Anfragen.
  
## <a name="try-it-yourself"></a>Testen Sie es selbst
<a name="SecureScore"> </a>

Lesen Sie diese Sicherheitsfeatures, die in einem Office 365-Testabonnement ausgeführt werden, bevor Sie Sie in der Produktion übernehmen.
  
- [Erstellen eines Office 365-Testabonnements](https://technet.microsoft.com/library/mt736406.aspx)
    
- [Konfigurieren und Testen von MFA für ein Benutzerkonto](https://technet.microsoft.com/library/mt492459.aspx)
    
- [Konfigurieren und testen Sie Office 365 Cloud App Security, um Sie über globale Administratoraktivitäten zu informieren.](https://technet.microsoft.com/library/mt757250.aspx)
    
- [Konfigurieren und Testen von ATP für verdächtige e-Mails](https://technet.microsoft.com/library/mt490479.aspx)
    
- Überprüfen Sie die [Office 365 Secure Score](https://securescore.office.com/) für Ihr Testabonnement für jeden der obigen Schritte. 
    

