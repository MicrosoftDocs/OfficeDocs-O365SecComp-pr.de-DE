---
title: Dokumentfingerabdrücke
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
search.appverid: MET150
ms.service: exchange-online
ms.collection: M365-security-compliance
localization_priority: Normal
description: Information-Worker in Ihrer Organisation verarbeiten im Lauf eines Arbeitstags viele Arten von vertraulichen Informationen. Dokumentfingerabdrücke erleichtern Ihnen den Schutz dieser Informationen durch Identifikation von Standardformularen, die in Ihrer gesamten Organisation verwendet werden. In diesem Thema werden die Konzepte für Dokument-Fingerabdrücke und die Erstellung eines mithilfe von PowerShell beschrieben.
ms.openlocfilehash: 2b8e4fd6b286f2c1a5c67863957f2b04fbef31b9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256898"
---
# <a name="document-fingerprinting"></a>Dokumentfingerabdrücke

Information-Worker in Ihrer Organisation verarbeiten im Lauf eines Arbeitstags viele Arten von vertraulichen Informationen. Im Security &amp; Compliance Center ist es einfacher für Sie, diese Informationen zu schützen, indem Sie die Standardformulare identifizieren, die in Ihrer Organisation verwendet werden. In diesem Thema werden die Konzepte für Dokument-Fingerabdrücke und die Erstellung eines mithilfe von PowerShell beschrieben.
  
## <a name="basic-scenario-for-document-fingerprinting"></a>Grundlegendes Szenario für Dokumentfingerabdrücke

Dokument-Fingerabdruck ist ein DLP-Feature (Data Loss Prevention), das ein Standardformular in einen vertraulichen Informationstyp konvertiert, den Sie in den Regeln ihrer DLP-Richtlinien verwenden können. Sie können beispielsweise einen Dokument Fingerabdruck erstellen, der auf einer leeren Patent Vorlage basiert, und dann eine DLP-Richtlinie erstellen, die alle ausgehenden Patent Vorlagen mit ausgefüllten vertraulichen Inhalten erkennt und blockiert. Optional können Sie [Richtlinien Tipps](use-notifications-and-policy-tips.md) einrichten, um Absender zu benachrichtigen, dass Sie möglicherweise vertrauliche Informationen senden, und der Absender sollte überprüfen, ob die Empfänger für den Empfang der Patente qualifiziert sind. Dieser Prozess funktioniert mit allen textbasierten Formularen, die in Ihrer Organisation verwendet werden. Weitere Beispiele für Formulare, die Sie hochladen können, sind: 
  
- Regierungsformulare
    
- HIPAA (Health Insurance Portability and Accountability Act)-kompatible Formulare
    
- Formulare mit Mitarbeiterinformationen für die Personalabteilung
    
- Speziell für Ihre Organisation erstellte benutzerdefinierte Formulare
    
Ideal wäre es, wenn es in Ihrer Organisation bereits eine etablierte Routine beim Umgang mit der Versendung vertraulicher Informationen gäbe. Nachdem Sie ein leeres Formular zum Konvertieren in einen Dokument Fingerabdruck hochgeladen und eine entsprechende Richtlinie eingerichtet haben, erkennt der DLP alle Dokumente in ausgehenden e-Mails, die mit diesem Fingerabdruck übereinstimmen.
  
## <a name="how-document-fingerprinting-works"></a>Funktionsweise von Dokumentfingerabdrücken

Wahrscheinlich haben Sie schon erraten, dass sich auf den Dokumenten keine echten Fingerabdrücke befinden - aber der Name erklärt sehr gut die Funktion. Genauso, wie der Fingerabdruck eines Menschen einzigartige Muster hat, haben Dokumente eine einzigartige Wortstruktur. Wenn Sie eine Datei hochladen, identifiziert DLP das eindeutige Wortmuster im Dokument, erstellt einen auf diesem Muster basierenden Dokument Fingerabdruck und verwendet diesen Dokument Fingerabdruck, um ausgehende Dokumente mit demselben Muster zu erkennen. Aus diesem Grund werden die effektivsten Dokumentfingerabdrücke durch Hochladen von Formularen oder Vorlagen erstellt. Jede Person, die ein Formular ausfüllt, verwendet denselben Originalsatz von Wörtern und fügt dann ihre eigenen Wörter in das Dokument ein. Solange das ausgehende Dokument nicht kennwortgeschützt ist und den gesamten Text aus dem ursprünglichen Formular enthält, kann DLP ermitteln, ob das Dokument mit dem Fingerabdruck des Dokuments übereinstimmt.
  
Im folgenden Beispiel wird gezeigt, was passiert, wenn Sie einen Dokumentfingerabdruck auf Grundlage einer Patentvorlage erstellen. Sie können aber auch jedes andere Formular dafür verwenden.
  
**Beispiel für ein Patentdokument, das zum Fingerabdruck einer Patentvorlage passt**

![Document_Fingerprinting_diagram. png](media/Document_Fingerprinting_diagram.png)
  
Die Patent Vorlage enthält die leeren Felder "Patent Titel", "Erfinder" und "Beschreibung" sowie Beschreibungen für jedes dieser Felder – das ist das Wortmuster. Wenn Sie die ursprüngliche Patent Vorlage hochladen, befinden Sie sich in einem der unterstützten Dateitypen und im nur-Text-Format. DLP konvertiert dieses Word-Muster in einen Fingerabdruck des Dokuments, bei dem es sich um eine kleine Unicode-XML-Datei handelt, die einen eindeutigen Hashwert enthält, der den Originaltext darstellt, und der Fingerabdruck als Datenklassifizierung in Active Directory gespeichert wird. (Als Sicherheitsmaßnahme wird das ursprüngliche Dokument selbst nicht im Dienst gespeichert; es wird nur der Hashwert gespeichert, und das ursprüngliche Dokument kann nicht aus dem Hashwert rekonstruiert werden.) Der Patent Fingerabdruck wird dann zu einem vertraulichen Informationstyp, den Sie einer DLP-Richtlinie zuordnen können. Nachdem Sie den Fingerabdruck einer DLP-Richtlinie zugeordnet haben, erkennt DLP alle ausgehenden e-Mails, die Dokumente enthalten, die mit dem Patent Fingerabdruck übereinstimmen, und behandelt Sie entsprechend der Richtlinie Ihrer Organisation. 

Sie können beispielsweise eine DLP-Richtlinie einrichten, die verhindert, dass reguläre Mitarbeiter ausgehende Nachrichten mit Patenten senden. DLP verwendet den Patent Fingerabdruck, um Patente zu finden und diese e-Mails zu blockieren. Alternativ können Sie Ihre Rechtsabteilung in der Lage sein, Patente an andere Organisationen zu senden, da Sie eine geschäftliche Notwendigkeit dazu hat. Sie können bestimmten Abteilungen gestatten, vertrauliche Informationen zu senden, indem Sie in der DLP-Richtlinie Ausnahmen für diese Abteilungen erstellen, oder Sie können es Ihnen gestatten, einen richtlinientipp mit einer geschäftlichen Berechtigung außer Kraft zu setzen.
  
### <a name="supported-file-types"></a>Unterstützte Dateitypen

Dokument-Fingerabdruckunterstützung unterstützt die gleichen Dateitypen, die in Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) unterstützt werden. Eine Liste unterstützter Dateitypen finden Sie unter [Supported file types for Mail Flow Rule Content Inspection](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection). Ein kurzer Hinweis zu Dateitypen: weder Nachrichtenfluss Regeln noch Dokument Fingerabdrücke unterstützen den DOTX-Dateityp, was verwirrend sein kann, da es sich um eine Vorlagendatei in Word handelt. Der Begriff "Vorlage" in diesem und anderen Themen zum Dokumentfingerabdruck bezieht sich auf ein Dokument, das Sie als Standardformular eingerichtet haben, nicht auf den Dateityp "Vorlage".
  
#### <a name="limitations-of-document-fingerprinting"></a>Einschränkungen der Funktion "Dokumentfingerabdruck"

In den folgenden Fällen werden vertrauliche Informationen in Dokument-Fingerabdruck nicht ermittelt:
  
- Kennwortgeschützte Dateien
    
- Dateien, die nur Bilder enthalten
    
- Dokumente, die nicht den gesamten Text aus dem Originalformular enthalten, aus dem der Dokumentfingerabdruck erstellt wurde
    
## <a name="use-powershell-to-create-a-classification-rule-package-based-on-document-fingerprinting"></a>Verwenden von PowerShell zum Erstellen eines Klassifizierungsregel Pakets basierend auf Dokument-Fingerabdruck

Beachten Sie, dass Sie einen Fingerabdruck nur mithilfe von PowerShell im Security &amp; Compliance Center erstellen können. Informationen zum Herstellen einer Verbindung finden Sie unter [Connect to Security _AMP_ Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).

DLP verwendet Klassifizierungsregel Pakete, um vertrauliche Inhalte zu identifizieren. Verwenden Sie die Cmdlets **New-DlpFingerprint** und **New-DlpSensitiveInformationType** , um ein Klassifizierungsregel Paket basierend auf einem Dokument Fingerabdruck zu erstellen. Da die Ergebnisse von **New-DlpFingerprint** nicht außerhalb der Daten Klassifizierungsregel gespeichert werden, führen Sie immer **New-DlpFingerprint** und **New-DlpSensitiveInformationType** oder **Set-DlpSensitiveInformationType** in der gleichen PowerShell-Sitzung. Im folgenden Beispiel wird ein neuer Dokumentfingerabdruck basierend auf der Datei "C:\Eigene Dateien\Contoso Employee Template.docx" erstellt. Sie speichern den neuen Fingerabdruck als Variable, damit Sie ihn mit dem Cmdlet **New-DlpSensitiveInformationType** in derselben PowerShell-Sitzung verwenden können. 
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Employee Template.docx" -Encoding byte -ReadCount 0
$Employee_Fingerprint = New-DlpFingerprint -FileData $Employee_Template -Description "Contoso Employee Template"
```

Lassen Sie uns nun eine neue Datenklassifizierungsregel namens "Contoso Employee Confidential" erstellen, die den Dokumentfingerabdruck auf der Datei "C:\Eigene Dateien\Contoso Customer Information Form.docx" verwendet.
  
```
$Customer_Form = Get-Content "C:\My Documents\Contoso Customer Information Form.docx" -Encoding byte -ReadCount 0
$Customer_Fingerprint = New-DlpFingerprint -FileData $Customer_Form -Description "Contoso Customer Information Form"
New-DlpSensitiveInformationType -Name "Contoso Customer Confidential" -Fingerprints $Customer_Fingerprint -Description "Message contains Contoso customer information." 
```

Sie können jetzt das Cmdlet **Get-DlpSensitiveInformationType** verwenden, um alle DLP-Daten Klassifizierungsregel Pakete zu finden, und in diesem Beispiel ist "Contoso Customer Confidential" Teil der Liste der Daten Klassifizierungsregel Pakete. 
  
Fügen Sie abschließend das Daten Klassifizierungsregel Paket "Contoso Customer Confidential" zu einer DLP-Richtlinie &amp; im Security Compliance Center hinzu. In diesem Beispiel wird eine Regel zu einer vorhandenen DLP-Richtlinie mit dem Namen "ConfidentialPolicy" hinzugefügt.

```
New-DlpComplianceRule -Name "ContosoConfidentialRule" -Policy "ConfidentialPolicy" -ContentContainsSensitiveInformation @{Name="Contoso Customer Confidential"} -BlockAccess $True
```

Sie können das Paket für die Daten Klassifizierungsregel auch in Nachrichtenfluss Regeln in Exchange Online verwenden, wie im folgenden Beispiel gezeigt. Zum Ausführen dieses Befehls müssen Sie zunächst [eine Verbindung mit Exchange Online PowerShell herstellen](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Beachten Sie, dass es Zeit braucht, bis das Regelpaket vom Security &amp; Compliance Center mit dem Exchange Admin Center synchronisiert wird.
  
```
New-TransportRule -Name "Notify :External Recipient Contoso confidential" -NotifySender NotifyOnly -Mode Enforce -SentToScope NotInOrganization -MessageContainsDataClassification @{Name=" Contoso Customer Confidential"}

```

DLP erkennt jetzt Dokumente, die mit dem Fingerabdruck "Contoso Customer Form. docx" übereinstimmen.
  
Informationen zu Syntax und Parametern finden Sie unter:

- [New-DlpFingerprint](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpFingerprint)
- [New-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpSensitiveInformationType)
- [Remove-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Remove-DlpSensitiveInformationType)
- [Set-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpSensitiveInformationType)
- [Get-DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpSensitiveInformationType)
