---
title: Dokumentfingerabdrücke
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: exchange-online
localization_priority: Normal
ms.assetid: 1e0c579c-26e0-462a-a1b0-d7506dfe05fa
description: Information Worker in Ihrer Organisation behandeln viele Arten von vertraulichen Daten in einem normalen Tag. Der Dokumentfingerabdruck vereinfacht die schützen diese Informationen durch das Identifizieren von Standardformulare, die in der gesamten Organisation verwendet werden. In diesem Thema werden die Konzepte von Dokumentfingerabdrücken und wie Sie mithilfe von PowerShell erstellt.
ms.openlocfilehash: d73b769e7a014f2642a0fcd66cc6a500c68c46c3
ms.sourcegitcommit: 4be502d1fc6cbaef4c72d599758d51efe3a173c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/06/2018
ms.locfileid: "23867495"
---
# <a name="document-fingerprinting"></a>Dokumentfingerabdrücke

Information Worker in Ihrer Organisation behandeln viele Arten von vertraulichen Daten in einem normalen Tag. In das Wertpapier &amp; Compliance Center, Dokumentfingerabdrücke erleichtert Sie schützen diese Informationen durch das Identifizieren von Standardformulare, die in der gesamten Organisation verwendet werden. In diesem Thema werden die Konzepte von Dokumentfingerabdrücken und wie Sie mithilfe von PowerShell erstellt.
  
## <a name="basic-scenario-for-document-fingerprinting"></a>Grundlegendes Szenario für Dokumentfingerabdrücke

Der Dokumentfingerabdruck ist ein Data Loss Prevention (DLP)-Feature, das einem Standardformular simulieren in einen Typ vertrauliche Informationen umgewandelt wird, das Sie in den Regeln der DLP-Richtlinien verwenden können. Beispielsweise können Sie basierend auf einer leeren patentvorlage dokumentfingerabdruck erstellt und dann Erstellen einer DLP-Richtlinie, die erkannt und blockiert alle ausgehende Patente Vorlagen mit vertrauliche Inhalte ausgefüllt. Optional können Sie [richtlinientipps](use-notifications-and-policy-tips.md) einrichten, um Absender benachrichtigen, dass sie vertraulichen Informationen senden und der Absender sicherstellen sollte, dass die Empfänger der Patente empfangen qualifiziert sind. Dieser Prozess kann mit textbasierte Formulare in Ihrer Organisation verwendeten. Weitere Beispiele für Formulare, die Sie hochladen können sind: 
  
- Regierungsformulare
    
- HIPAA (Health Insurance Portability and Accountability Act)-kompatible Formulare
    
- Formulare mit Mitarbeiterinformationen für die Personalabteilung
    
- Speziell für Ihre Organisation erstellte benutzerdefinierte Formulare
    
Idealerweise hat Ihre Organisation bereits eine eingerichteten Geschäftsmethoden der Verwendung bestimmter Formulare zum Übertragen von vertraulichen Informationen. Nach dem Hochladen eines leeren Formulars ein, um zu einem dokumentfingerabdruck konvertiert und richten Sie eine entsprechende Richtlinie, erkennt der DLP alle Dokumente in ausgehenden Nachrichten, die mit diesem Fingerabdruck übereinstimmen.
  
## <a name="how-document-fingerprinting-works"></a>Funktionsweise von Dokumentfingerabdrücken

Sie haben möglicherweise bereits erraten, dass Dokumente keinen tatsächlichen Fingerabdrücke, aber der Namen unterstützt das Feature zu erläutern. Auf die gleiche Weise, dass eine Person Fingerabdrücke eindeutige Muster verfügen müssen Dokumente Wort unique Muster. Wenn Sie eine Datei hochladen, DLP bezeichnet das Wort unique Muster im Dokument basierend auf das Muster dokumentfingerabdruck erstellt und dieser dokumentfingerabdruck verwendet, um ausgehende Dokumente, die mit dem gleichen Muster zu erkennen. Aus diesem Grund Hochladen ein Formulars wird oder Vorlage erstellt den effektivste dokumentfingerabdruck. Jeder Benutzer, der ein Formular ausfüllt verwendet die ursprünglichen Wörter und anschließend ein eigenes Wörter mit dem Dokument hinzugefügt. Solange das ausgehende Dokument nicht kennwortgeschützt und enthält den gesamten Text aus dem ursprünglichen Formular, kann DLP bestimmen, ob das Dokument den dokumentfingerabdruck übereinstimmt.
  
Im folgenden Beispiel wird gezeigt, was passiert, wenn Sie einen Dokumentfingerabdruck auf Grundlage einer Patentvorlage erstellen. Sie können aber auch jedes andere Formular dafür verwenden.
  
**Beispiel für ein Patentdokument, das zum Fingerabdruck einer Patentvorlage passt**

![Document_Fingerprinting_diagram.PNG](media/Document_Fingerprinting_diagram.png)
  
Die patentvorlage enthält die leeren Felder "Patente Title", "Erfinder," und "Beschreibung" und Beschreibungen für jedes dieser Felder –, ist das Word-Muster. Wenn Sie die ursprünglichen patentvorlage hochladen, ist es in einer der unterstützten Dateitypen und in nur-Text. Dieses Muster Word in dokumentfingerabdruck, eine kleine Unicode XML wird Datei, die einen eindeutigen Hashwert zur Darstellung der ursprüngliche Text und der Fingerabdruck enthält DLP konvertiert wird als Datenklassifikation in Active Directory gespeichert. (Als Sicherheitsmaßnahme, das ursprüngliche Dokument selbst wird nicht auf den Dienst gespeichert; nur der Hashwert gespeichert ist und das ursprüngliche Dokument kann nicht aus dem Hashwert wiederhergestellt werden.) Die Patente Fingerabdruck wird dann einen Typ von vertraulichen Informationen, den mit einer DLP-Richtlinie zugeordnet werden kann. Nachdem Sie den Fingerabdruck einer DLP-Richtlinie zuzuordnen DLP erkennt keine ausgehenden e-Mails mit Dokumenten, die mit dem Fingerabdruck Patente übereinstimmen und befasst sich mit diesen entsprechend Ihrer Organisation geltenden Richtlinien. 

Sie möchten beispielsweise einer DLP-Richtlinie einrichten, die verhindert, regulären Mitarbeiter am Senden von ausgehender Nachrichten dass, Patente enthält. DLP verwenden die Patente Fingerabdruck zum Erkennen von Patenten und diese-e-Mails blockieren. Sie möchten Alternativ können die rechtsabteilung um Patente an andere Unternehmen senden, da es ein Unternehmen müssen wurde dafür. Sie können bestimmte Abteilungen zum Senden von vertraulichen Informationen durch Erstellen von Ausnahmen für die Abteilungen in DLP-Richtlinie, oder Sie können sie einen richtlinientipp mit als Rechtfertigung außer Kraft gesetzt.
  
### <a name="supported-file-types"></a>Unterstützte Dateitypen

Der Dokumentfingerabdruck unterstützt die gleichen Dateitypen, die in Transportregeln unterstützt werden. Eine Liste der unterstützten Dateitypen finden Sie unter [unterstützte Dateitypen für inhaltsüberprüfung mit e-Mail-Fluss Transportregeln](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection). Eine kurze Notiz zu Dateitypen: Transportregeln weder Dokumentfingerabdrücke unterstützt den Dateityp dotx verwirrend erfolgen kann, da das ist eine Vorlagendatei in Word. Wenn das Wort "Vorlage" in diesem und anderen Themen Dokumentfingerabdrücke angezeigt wird, verweist er auf ein Dokument, das Sie als einem Standardformular simulieren, nicht den Dateityp Vorlage eingerichtet haben.
  
#### <a name="limitations-of-document-fingerprinting"></a>Einschränkungen der Funktion "Dokumentfingerabdruck"

Der Dokumentfingerabdruck Erkennung keine vertraulichen Informationen in den folgenden Fällen:
  
- Kennwortgeschützte Dateien
    
- Dateien, die nur Bilder enthalten
    
- Dokumente, die nicht den gesamten Text aus dem Originalformular enthalten, aus dem der Dokumentfingerabdruck erstellt wurde
    
## <a name="use-powershell-to-create-a-classification-rule-package-based-on-document-fingerprinting"></a>Erstellen ein klassifizierungsregelpakets auf Grundlage des dokumentfingerabdrucks mithilfe von PowerShell

Beachten Sie, dass Sie derzeit Fingerabdruck erstellen können nur mithilfe von PowerShell in das Wertpapier &amp; Compliance Center. Um eine Verbindung herzustellen, finden Sie unter [Connect to Office 365-Sicherheit und Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

DLP verwendet klassifizierungsregelpakete, um vertrauliche Inhalte zu erkennen. Verwenden Sie zum Erstellen eines klassifizierungsregelpakets basierend auf einer dokumentfingerabdruck die Cmdlets **New-DlpFingerprint** und **New-DlpSensitiveInformationType** . Da die Ergebnisse der **New-DlpFingerprint** außerhalb der datenklassifizierungsregel gespeichert sind, führen Sie immer **Neu DlpFingerprint** und **New-DlpSensitiveInformationType** oder **Set-DlpSensitiveInformationType** in der gleichen PowerShell-Sitzung. Das folgende Beispiel erstellt einen neuen dokumentfingerabdruck basierend auf der Datei C:\My Documents\Contoso Employee Template.docx. Sie Speichern der neuen Fingerabdruck als Variable, damit Sie sie in der gleichen PowerShell-Sitzung mit dem Cmdlet **New-DlpSensitiveInformationType** verwenden können. 
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Employee Template.docx" -Encoding byte -ReadCount 0
$Employee_Fingerprint = New-DlpFingerprint -FileData $Employee_Template -Description "Contoso Employee Template"
```

Lassen Sie uns nun eine neue Datenklassifizierungsregel namens "Contoso Employee Confidential" erstellen, die den Dokumentfingerabdruck auf der Datei "C:\Eigene Dateien\Contoso Customer Information Form.docx" verwendet.
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Customer Information Form.docx" -Encoding byte -ReadCount 0
$Customer_Fingerprint = New-DlpFingerprint -FileData $Customer_Form -Description "Contoso Customer Information Form"
New-DlpSensitiveInformationType -Name "Contoso Customer Confidential" -Fingerprints $Customer_Fingerprint -Description "Message contains Contoso customer information." 
```

Nun können Sie das Cmdlet **Get-DlpSensitiveInformationType** , um alle Daten DLP-klassifizierungsregelpakete zu erhalten, und in diesem Beispiel wird "Contoso Customer Confidential" Teil der Liste der Daten Classification Rule-Pakete. 
  
Schließlich hinzufügen "Contoso Customer Confidential" datenklassifizierungsregelpaket zu einer DLP-Richtlinie in das Wertpapier &amp; Compliance Center. In diesem Beispiel wird eine vorhandene DLP-Richtlinie mit dem Namen "ConfidentialPolicy" eine Regel hinzugefügt.

```
New-DlpComplianceRule -Name "ContosoConfidentialRule" -Policy "ConfidentialPolicy" -ContentContainsSensitiveInformation @{Name="Contoso Customer Confidential"} -BlockAccess $True
```

Sie können auch die datenklassifizierungsregelpaket in Transportregeln in Exchange Online verwenden, wie im folgenden Beispiel dargestellt. Um diesen Befehl auszuführen, müssen Sie zunächst Herstellen einer Verbindung [mit Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Beachten Sie, dass es für das Paket Regel Zeit für die Synchronisierung von der Sicherheit &amp; Compliance Center, um die Exchange-Verwaltungskonsole.
  
```
New-TransportRule -Name "Notify :External Recipient Contoso confidential" -NotifySender NotifyOnly -Mode Enforce -SentToScope NotInOrganization -MessageContainsDataClassification @{Name=" Contoso Customer Confidential"}

```

DLP erkennt nun Dokumente, die den dokumentfingerabdruck Contoso Customer Form.docx entsprechen.
  
Informationen zu Syntax und Parametern finden Sie unter:

- [Neue DlpFingerprint](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpFingerprint)
- [Neue DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpSensitiveInformationType)
- [Remove-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Remove-DlpSensitiveInformationType)
- [Set-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpSensitiveInformationType)
- [Get-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpSensitiveInformationType)
