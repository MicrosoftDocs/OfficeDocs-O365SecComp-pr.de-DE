---
title: Bewährte Methoden für die Sicherheit in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: Minimieren Sie das Potenzial der Verletzung Daten oder einem kompromittierten Konto, indem Sie diese empfohlenen bewährten Methoden befolgen.
ms.openlocfilehash: 0d3dc30a9975f2ed8fe6d524b4fc67918b34e51d
ms.sourcegitcommit: 49b565f6a57febe53f331b2605d6a06d11e2d0be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2018
ms.locfileid: "25637999"
---
# <a name="security-best-practices-for-office-365"></a>Bewährte Methoden für die Sicherheit in Office 365

Minimieren Sie das Potenzial der Verletzung Daten oder einem kompromittierten Konto, indem Sie diese empfohlenen bewährten Methoden befolgen.
  
Dieser Artikel enthält eine Liste der bewährten Methoden. Weitere eingehenderen Analysen und Informationen zum Einrichten von Sicherheit finden Sie unter [Wegweiser für Office 365-Sicherheit: Top-Prioritäten für den ersten 30 Tagen 90 Tage und darüber hinaus](security-roadmap.md). In diesem Artikel finden Sie Informationen basierend auf Untersuchungen Praxis-Angriffe, in denen unsere oberen Sicherheit im Internet Experten für Microsoft Office 365 coaching zum Bewerten der Risiken und Implementieren der wichtigsten Sicherheit, Kompatibilität und Informationen bereitstellen Dokumentschutz-Steuerelemente zum Schutz Ihres Office 365-Mandanten. Sie erfahren, wie Sie priorisieren Bedrohungen, Bedrohungen in technischen Strategie übersetzen, und schalten einen systematischen Ansatz zur Implementierung von Features und Steuerelemente.
  
## <a name="use-office-365-secure-score"></a>Verwenden Sie sichere Bewertung der Office 365

Sichere Score ist ein Analytics Sicherheitstool, die empfiehlt, was Sie tun können, um Risiko zu reduzieren. Sichere Faktor befasst sich mit Ihren Office 365-Einstellungen und Aktivitäten und miteinander verglichen, an einer Grundlinie von Microsoft hergestellt. Erhalten Sie eine Bewertung basierend auf wie ausgerichtete Sie mit bewährten Methoden für die Sicherheit sind. Weitere Informationen dazu, wie Sie Secure Score abrufen und verwenden, um die Sicherheit von Office 365-Organisation zu erhöhen finden Sie unter [Einführung in die Office 365 Secure Bewertung](office-365-secure-score.md).
  
Secure Score ausprobieren möchten?
  
Unter Verwendung eines Kontos arbeiten oder Schule, die die Office 365- [Administratorrollen zu Office 365](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) -Rolle [bei Office 365 anmelden](https://www.office.com/signin)zugewiesen wurde.
  
Sicheren Zugriff Score unter [https://SecureScore.office.com](https://SecureScore.office.com).
  
## <a name="use-multi-factor-authentication-mfa"></a>Mehrstufige Authentifizierung (mehrstufiger Authentifizierung das) verwenden

Mehrstufiger Authentifizierung das hinzugefügt einer Strategie für die sichere Kennwörter durch Benutzer auffordern, bestätigen einen Telefonanruf, Textnachricht oder eine app-Benachrichtigung über ein Telefon smart nach ordnungsgemäß Sie ihr Kennwort eingeben eine zusätzliche Schutzebene. Mit mehrstufiger Authentifizierung das direkte sind die Office 365-Benutzerkonten weiterhin vor nicht autorisiertem Zugriff geschützt, auch wenn das Kennwort des Benutzers gefährdet ist. Konten sind geschützt, da ein Konto erst nach die zusätzliche Herausforderung erfüllt wurden nicht Zugriff gewährt wird. Ein Kennwort kompromittierten oder gestohlenen ist nicht ausreichend.
  
- [Planen der mehrstufigen Authentifizierung für Office 365-Bereitstellungen](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Einrichten der mehrstufigen Authentifizierung für Office 365-Benutzer](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a>Verwenden Sie Office 365-Cloud-App-Sicherheit

Einrichten von Richtlinien basierend auf Ihrer geschäftlichen Anforderungen abweichenden Aktivitäten verfolgen und handeln. Einrichten von Benachrichtigungen mit Office 365-Cloud-App-Sicherheit, damit Administratoren ungewöhnliche oder riskant Benutzeraktivität, wie große Datenmengen herunterladen überprüfen können fehlgeschlagen mehreren Anmeldeversuche oder Anmeldungen von unbekannten oder gefährlicher IP-Adresse. Für Organisationen mit einer Office 365 Enterprise E5 planen können Sie die mit Office 365-Cloud-App-Sicherheit sofort starten. Wenn Sie einen anderen Enterprise-Plan haben, können Sie Office 365-Cloud-App-Sicherheit als Add-on erwerben.
  
- [Übersicht über Office 365-Cloud-App-Sicherheit](office-365-cas-overview.md)
    
- [Aktivieren von Office 365 Cloud App Security](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a>Sichere e-Mail-Fluss

Implementieren Sie die Rich-Text Featuregruppe in Exchange Online Protection und größerer Sicherheit über die Identität des Absenders der jeder e-Mail-Nachricht erhalten und Schutz vor Schadsoftware unbekannt, Viren und schädliche URLs über-e-Mails übertragen.
  
- Konfigurieren von Richtlinien für [Office 365 E-Mail Anti-Spam-Schutz](anti-spam-protection.md) für Ihre Organisation. 
    
- Erfahren Sie, und klicken Sie dann verwenden Sie [Erweiterter Schutz für sichere Anlagen und sichere Links](https://technet.microsoft.com/library/mt148491.aspx).
    
- [Hinzufügen von Anti-Malware Protection für Ihre Organisation](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).
    
- Erfahren Sie mehr über und [Sicherheit in e-Mail-Nachrichten in Office 365 Tipps](safety-tips-in-office-365.md) für Ihre Benutzer zu aktivieren. 
    
- Wenn Sie eine benutzerdefinierte Domäne für Ihre Organisation in Office 365 verwenden, richten Sie SPF, DKIM, und klicken Sie dann DMARC, zum Überprüfen von e-Mails, die von Ihrer Organisation gesendet und als Hilfe spoofing zu verhindern:
    
  - [Einrichten von SPF in Office 365, um spoofing zu verhindern](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Verwendung mit DKIM überprüfen Sie ausgehende e-Mail-Nachrichten, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [DMARC verwenden, um e-Mail in Office 365 zu überprüfen](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
## <a name="enable-mailbox-audit-logging"></a>Aktivieren der Postfachüberwachungsprotokollierung

Einige überwachungsprotokollierung wird automatisch in Office 365 für Sie aktiviert. Allerdings postfachüberwachungsprotokollierung ist standardmäßig nicht aktiviert. Überwachungsprotokollierung für alle Benutzerpostfächer in Office 365 einschalten mithilfe von Exchange Online PowerShell. Informationen finden Sie unter [Überwachung in Office 365 Postfach zu aktivieren](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
Nachdem Sie aktiviert haben überwachungsprotokollierung Sie können [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md) um herauszufinden, wer an Ihrer Benutzerpostfächer gesendete Nachrichten und andere Aktivitäten, die von der Postfachbesitzer delegierte Benutzer angemeldet hat oder ein Administrator. Überwachungsprotokoll standardmäßig eine Liste der Postfach-Aktivitäten, die in der Office 365 enthalten sind, finden Sie unter [Exchange-Postfach-Aktivitäten](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).
  
Informationen zu anderen Aktionen, die Sie das Überwachungsprotokoll ausführen können wie etwa ändern die Zeitspanne zum Speichern der Einträge in das Überwachungsprotokoll finden Sie unter [postfachüberwachungsprotokollierung Protokollierung in Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).
  
## <a name="configure-data-loss-prevention-dlp"></a>Konfigurieren von Data Loss Prevention (DLP)

DLP können Sie vertrauliche Daten zu identifizieren und Richtlinien erstellen, die verhindern, dass Ihre Benutzer versehentlich oder absichtlich Datenfreigabe. DLP eignet sich für Office 365, einschließlich Exchange Online, SharePoint Online und OneDrive, damit die Benutzer kompatible bleiben können, ohne ihren Workflow zu unterbrechen. Weitere Informationen finden Sie unter [Übersicht über Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md).
  
## <a name="use-customer-lockbox"></a>Verwenden Sie Kunden Lockbox

Ein Office 365-Administrator können Kunden Lockbox Sie steuern, wie ein Microsoft-Supportmitarbeiter während einer Sitzung auf Ihre Daten zugreift. In Fällen, in denen der Engineer Zugriff auf Ihre Daten erfordert zu behandeln und ein Problem beheben, können Kunden Lockbox Sie genehmigen oder Ablehnen der Access-Anforderung. Wenn Sie es genehmigen, kann der Mitarbeiter die Daten zugreifen. Jeder Anforderung Ablaufzeit hat und nachdem das Problem behoben ist, die Anforderung wird geschlossen und Access gesperrt ist. Kunden Lockbox ist im Office 365 Enterprise E5 Plan enthalten, oder Sie können ein separates Abonnement mit anderen Office 365 Enterprise Plan erwerben. Informationen finden Sie unter [Office 365 Lockbox Kundenanfragen](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).
  
## <a name="try-it-yourself"></a>Probieren Sie es selbst
<a name="SecureScore"> </a>

Finden Sie unter Sicherheitsfeatures in einem trial Office 365-Abonnement vor ihrer Annahme in der Produktion arbeiten.
  
- [Erstellen Sie eine Testversion Office 365-Abonnements](https://technet.microsoft.com/library/mt736406.aspx)
    
- [Konfigurieren Sie und Testen Sie der mehrstufiger Authentifizierung das für ein Benutzerkonto](https://technet.microsoft.com/library/mt492459.aspx)
    
- [Konfigurieren und Testen von Office 365 Cloud App-Sicherheit, um Sie der Aktivität globaler Administrator benachrichtigen](https://technet.microsoft.com/library/mt757250.aspx)
    
- [Konfigurieren und Testen von ATP für verdächtigen e-Mails](https://technet.microsoft.com/library/mt490479.aspx)
    
- Überprüfen der [Office 365 Secure Score](https://securescore.office.com/) Test-Abonnement für jede der oben genannten Schritte 
    

