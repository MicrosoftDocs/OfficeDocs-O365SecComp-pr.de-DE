---
title: Erstellen benutzerdefinierter vertraulicher Informationstypen mit genauer Datenübereinstimmung
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Erstellen Sie benutzerdefinierte vertrauliche Informationstypen mit genauer Datenübereinstimmungsklassifizierung.
ms.openlocfilehash: 3c2b7cbabc77328f7d907927008e93606d40eded
ms.sourcegitcommit: a5a7e43822336ed18d8f5879167766686cf6b2a3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2019
ms.locfileid: "36478194"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification"></a><span data-ttu-id="d3ec9-103">Erstellen von benutzerdefinierten vertraulichen Informationstypen mit genauer Datenübereinstimmungsklassifizierung</span><span class="sxs-lookup"><span data-stu-id="d3ec9-103">See Create a custom sensitive information type with Exact Data Match based classification (Preview).</span></span>

## <a name="overview"></a><span data-ttu-id="d3ec9-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d3ec9-104">Overview</span></span>

<span data-ttu-id="d3ec9-105">[Benutzerdefinierte vertrauliche Informationstypen](https://docs.microsoft.com/de-DE/office365/securitycompliance/custom-sensitive-info-types) werden verwendet, um zu verhindern, dass vertrauliche Informationen versehentlich oder in unangemessener Weise freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-105">[Custom sensitive information types](https://docs.microsoft.com/de-DE/office365/securitycompliance/custom-sensitive-info-types) are used to help prevent inadvertent or inappropriate sharing of sensitive information.</span></span> <span data-ttu-id="d3ec9-106">Als Administrator können Sie das [Security & Compliance Center](https://docs.microsoft.com/de-DE/office365/securitycompliance/create-a-custom-sensitive-information-type) oder [PowerShell](https://docs.microsoft.com/de-DE/office365/securitycompliance/create-a-custom-sensitive-information-type-in-scc-powershell) verwenden, um einen benutzerdefinierten vertraulichen Informationstyp basierend auf Mustern, Nachweisen (Stichwörtern wie  *Mitarbeiter*, *Abzeichen*, *ID* usw.), Zeichenabstand (wie nahe Nachweise sich an Zeichen in einem bestimmten Muster befinden) und Vertrauensstufen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-106">As an administrator, you can use the [Security & Compliance Center](https://docs.microsoft.com/de-DE/office365/securitycompliance/create-a-custom-sensitive-information-type) or [PowerShell](https://docs.microsoft.com/de-DE/office365/securitycompliance/create-a-custom-sensitive-information-type-in-scc-powershell) to define a custom sensitive information type based on patterns, evidence (keywords such as *employee*, *badge*, *ID*, and so on), character proximity (how close evidence is to characters in a particular pattern), and confidence levels.</span></span> <span data-ttu-id="d3ec9-107">Solche benutzerdefinierten vertraulichen Informationstypen erfüllen die geschäftlichen Anforderungen vieler Organisationen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-107">Such custom sensitive information types meet business needs for many organizations.</span></span>

<span data-ttu-id="d3ec9-108">Was aber, wenn Sie einen benutzerdefinierten vertraulichen Informationstyp nutzen möchten, der genaue Datenwerte verwendet, anstatt nur mit generischen Mustern übereinzustimmen?</span><span class="sxs-lookup"><span data-stu-id="d3ec9-108">But what if you wanted a custom sensitive information type that uses exact data values, instead of matching only with generic patterns?</span></span> <span data-ttu-id="d3ec9-109">Mit einer EDM-basierten Klassifizierung (genaue Datenübereinstimmung) können Sie einen benutzerdefinierten Informationstyp mit den folgenden Merkmalen erstellen:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-109">With Exact Data Match (EDM)-based classification, you can create a custom sensitive information type that is designed to:</span></span>

- <span data-ttu-id="d3ec9-110">dynamisch und aktualisierbar;</span><span class="sxs-lookup"><span data-stu-id="d3ec9-110">be dynamic and refreshable;</span></span>
- <span data-ttu-id="d3ec9-111">höhere Skalierbarkeit;</span><span class="sxs-lookup"><span data-stu-id="d3ec9-111">be more scalable;</span></span>
- <span data-ttu-id="d3ec9-112">weniger falsch positive Ergebnisse;</span><span class="sxs-lookup"><span data-stu-id="d3ec9-112">result in fewer false-positives;</span></span>
- <span data-ttu-id="d3ec9-113">Arbeiten mit strukturierten vertraulichen Daten;</span><span class="sxs-lookup"><span data-stu-id="d3ec9-113">work with structured sensitive data;</span></span>
- <span data-ttu-id="d3ec9-114">vertrauliche Informationen sicherer behandeln; </span><span class="sxs-lookup"><span data-stu-id="d3ec9-114">handle sensitive information more securely; and</span></span>
- <span data-ttu-id="d3ec9-115">Verwendbarkeit mit mehreren Microsoft Cloud Services.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-115">be used with several Microsoft cloud services.</span></span>

![EDM-basierte Klassifikation](media/EDMClassification.png)

<span data-ttu-id="d3ec9-117">Die EDM-basierte Klassifikation ermöglicht es Ihnen, benutzerdefinierte vertrauliche Informationstypen zu erstellen, die sich auf genaue Werte in einer Datenbank mit vertraulichen Informationen beziehen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-117">EDM-based classification enables you to create custom sensitive information types that refer to exact values in a database of sensitive information.</span></span> <span data-ttu-id="d3ec9-118">Die Datenbank kann täglich oder wöchentlich aktualisiert werden und bis zu 10 Millionen Datenzeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-118">The database can be refreshed daily or weekly, and it can contain up to 10 million rows of data.</span></span> <span data-ttu-id="d3ec9-119">Mitarbeiter, Patienten oder Kunden kommen und gehen und Datensätze ändern sich, aber Ihre benutzerdefinierten vertraulichen Informationstypen bleiben aktuell und anwendbar.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-119">So as employees, patients, or clients come and go, and records change, your custom sensitive information types remain current and applicable.</span></span> <span data-ttu-id="d3ec9-120">Darüber hinaus können Sie EDM-basierte Klassifikation mit Richtlinien verwenden, z. B. [Richtlinien zur Verhinderung von Datenverlust](https://docs.microsoft.com/de-DE/office365/securitycompliance/data-loss-prevention-policies) (Data Loss Prevention, DLP) oder [Microsoft Cloud App Security-Dateirichtlinien](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-120">And, you can use EDM-based classification with policies, such as [data loss prevention policies](https://docs.microsoft.com/de-DE/office365/securitycompliance/data-loss-prevention-policies) (DLP) or [Microsoft Cloud App Security file policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="d3ec9-121">Erforderliche Lizenzen und Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-121">Required licenses and permissions</span></span>

<span data-ttu-id="d3ec9-122">Sie müssen ein globaler, Compliance- oder Exchange Online-Administrator sein, um die in diesem Artikel beschriebenen Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-122">You must be a global admin, compliance administrator, or Exchange Online administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="d3ec9-123">Weitere Informationen über DLP-Berechtigungen finden Sie unter [Berechtigungen](https://docs.microsoft.com/de-DE/office365/securitycompliance/data-loss-prevention-policies#permissions).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-123">To learn more about DLP permissions, see [Permissions](https://docs.microsoft.com/de-DE/office365/securitycompliance/data-loss-prevention-policies#permissions).</span></span>

<span data-ttu-id="d3ec9-124">Nach allgemeiner Verfügbarkeit wird die EDM-basierte Klassifikation in folgenden Abonnements berücksichtigt:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-124">When generally available, EDM-based classification will be included in these subscriptions</span></span>

- <span data-ttu-id="d3ec9-125">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="d3ec9-125">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="d3ec9-126">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="d3ec9-126">Microsoft 365 E5</span></span>
- <span data-ttu-id="d3ec9-127">Microsoft 365 Informationsschutz und Compliance</span><span class="sxs-lookup"><span data-stu-id="d3ec9-127">Microsoft 365 Information Protection and Compliance</span></span>
- <span data-ttu-id="d3ec9-128">Office 365 Advanced Compliance</span><span class="sxs-lookup"><span data-stu-id="d3ec9-128">Office 365 Advanced Compliance</span></span>

## <a name="the-work-flow-at-a-glance"></a><span data-ttu-id="d3ec9-129">Der Workflow auf einen Blick</span><span class="sxs-lookup"><span data-stu-id="d3ec9-129">The work flow at a glance</span></span>

|<span data-ttu-id="d3ec9-130">Phase</span><span class="sxs-lookup"><span data-stu-id="d3ec9-130">Phase</span></span>  |<span data-ttu-id="d3ec9-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-131">What's needed</span></span>  |
|---------|---------|
|[<span data-ttu-id="d3ec9-132">Teil 1: Einrichten der EDM-basierten Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="d3ec9-132">Part 1: Set up EDM-based classification</span></span>](#part-1-set-up-edm-based-classification)<br/><br/><span data-ttu-id="d3ec9-133">(je nach Bedarf)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-133">(As needed)</span></span><br/><span data-ttu-id="d3ec9-134">- [Bearbeiten des Datenbankschemas](#editing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-134">- [Edit the database schema](#editing-the-schema-for-edm-based-classification)</span></span> <br/><span data-ttu-id="d3ec9-135">- [Entfernen des Schemas](#removing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-135">- [Remove the schema](#removing-the-schema-for-edm-based-classification)</span></span> |<span data-ttu-id="d3ec9-136">– Lesezugriff auf vertrauliche Daten</span><span class="sxs-lookup"><span data-stu-id="d3ec9-136">- Read access to the sensitive data</span></span><br/><span data-ttu-id="d3ec9-137">– Datenbankschema im XML-Format (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-137">- Database schema in .xml format (example provided)</span></span><br/><span data-ttu-id="d3ec9-138">– Regelpaket im XML-Format (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-138">- Rule package in .xml format (example provided)</span></span><br/><span data-ttu-id="d3ec9-139">– Administratorberechtigungen für das Security & Compliance Center (mithilfe von PowerShell)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-139">- Admin permissions to the Security & Compliance Center (using PowerShell)</span></span> |
|[<span data-ttu-id="d3ec9-140">Teil 2: Indizieren und Hochladen vertraulicher Daten</span><span class="sxs-lookup"><span data-stu-id="d3ec9-140">Part 2: Index and upload the sensitive data</span></span>](#part-2-index-and-upload-the-sensitive-data)<br/><br/><span data-ttu-id="d3ec9-141">(je nach Bedarf)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-141">(As needed)</span></span><br/>[<span data-ttu-id="d3ec9-142">Aktualisieren der Daten</span><span class="sxs-lookup"><span data-stu-id="d3ec9-142">Refresh the data</span></span>](#refreshing-your-sensitive-information-database) |<span data-ttu-id="d3ec9-143">– Benutzerdefinierte Sicherheitsgruppe und Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="d3ec9-143">- Custom security group and user account</span></span><br/><span data-ttu-id="d3ec9-144">– Lokaler Administratorzugriff auf den Computer mit dem EDM-Upload-Agent</span><span class="sxs-lookup"><span data-stu-id="d3ec9-144">- Local admin access to machine with EDM Upload Agent</span></span><br/><span data-ttu-id="d3ec9-145">– Lesezugriff auf vertrauliche Daten</span><span class="sxs-lookup"><span data-stu-id="d3ec9-145">- Read access to the sensitive data</span></span><br/><span data-ttu-id="d3ec9-146">– Prozess und Zeitplan für die Datenaktualisierung</span><span class="sxs-lookup"><span data-stu-id="d3ec9-146">- Process and schedule for refreshing the data</span></span>|
|[<span data-ttu-id="d3ec9-147">Teil 3: Verwenden der EDM-basierten Klassifizierung mit Ihren Microsoft Cloud Services</span><span class="sxs-lookup"><span data-stu-id="d3ec9-147">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |<span data-ttu-id="d3ec9-148">– Office 365-Abonnement mit DLP</span><span class="sxs-lookup"><span data-stu-id="d3ec9-148">- Office 365 subscription with DLP</span></span><br/><span data-ttu-id="d3ec9-149">– EDM-basiertes Klassifizierungsfeature aktiviert</span><span class="sxs-lookup"><span data-stu-id="d3ec9-149">- EDM-based classification feature enabled</span></span> |

### <a name="part-1-set-up-edm-based-classification"></a><span data-ttu-id="d3ec9-150">Teil 1: Einrichten der EDM-basierten Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="d3ec9-150">Part 1: Set up EDM-based classification</span></span>

<span data-ttu-id="d3ec9-151">Beim Einrichten und Konfigurieren der EDM-basierten Klassifizierung werden vertrauliche Daten im CSV-Format gespeichert, ein Schema für Ihre Datenbank mit vertraulichen Informationen definiert und ein Regelpaket erstellt. Anschließend werden das Schema und das Regelpaket hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-151">Setting up and configuring EDM-based classification involves saving sensitive data in .csv format, defining a schema for your database of sensitive information, creating a rule package, and then uploading the schema and rule package.</span></span>

#### <a name="define-the-schema-for-your-database-of-sensitive-information"></a><span data-ttu-id="d3ec9-152">Definieren des Schemas für Ihre Datenbank mit vertraulichen Informationen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-152">Define the schema for your database of sensitive information</span></span>

1. <span data-ttu-id="d3ec9-153">Identifizieren Sie die vertraulichen Informationen, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-153">Identify the KPIs that you want to use.</span></span> <span data-ttu-id="d3ec9-154">Exportieren Sie die Daten in eine App, wie z. B. Microsoft Excel, und speichern Sie die Datei im CSV-Format.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-154">Export the data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="d3ec9-155">Die Datendatei kann maximal Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-155">The data file can include a maximum of:</span></span>
      - <span data-ttu-id="d3ec9-156">bis zu 10 Millionen Zeilen vertraulicher Daten</span><span class="sxs-lookup"><span data-stu-id="d3ec9-156">Up to 10 million rows of sensitive data</span></span>
      - <span data-ttu-id="d3ec9-157">bis zu 32 Spalten (Felder) pro Datenquelle</span><span class="sxs-lookup"><span data-stu-id="d3ec9-157">Up to 32 columns (fields) per data source</span></span>
      - <span data-ttu-id="d3ec9-158">bis zu 5 als durchsuchbar markierte Spalten (Felder)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-158">Up to 5 columns (fields) marked as searchable</span></span>

2. <span data-ttu-id="d3ec9-159">Strukturieren Sie die vertraulichen Daten in der CSV-Datei so, dass die erste Zeile die Namen der für die EDM-basierte Klassifizierung verwendeten Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-159">Structure the sensitive data in the .csv file such that the first row includes the names of the fields used for EDM-based classification.</span></span> <span data-ttu-id="d3ec9-160">Möglicherweise gibt es in Ihrer CSV-Datei Feldnamen, wie z. B. "SSN", "Geburtsdatum", "Vorname", "Nachname" usw.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-160">In your .csv file, you might have field names, such as "ssn", "birthdate", "firstname", "lastname", and so on.</span></span> <span data-ttu-id="d3ec9-161">Im Beispiel nennen wir unsere CSV-Datei *PatientRecords.csv*, und die Spalten beinhalten *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN* und mehr.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-161">As an example, our .csv file is called *PatientRecords.csv*, and its columns include *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN* and more.</span></span>

3. <span data-ttu-id="d3ec9-162">Definieren Sie das Schema für die Datenbank mit vertraulichen Informationen im XML-Format (ähnlich wie in unserem Beispiel unten).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-162">Define the schema for the database of sensitive information in .xml format (similar to our example below).</span></span> <span data-ttu-id="d3ec9-163">Nennen Sie diese Schemadatei „edm.xml“ und konfigurieren Sie sie so, dass für jede Spalte in der Datenbank eine Zeile mit der Syntax \<Field name="" searchable=""/\> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-163">Name this schema file edm.xml, and configure it such that for each column in the database, there is a line that uses the syntax \<Field name="" searchable=""/\>.</span></span>

      - <span data-ttu-id="d3ec9-164">Verwenden Sie Spaltennamen für *Field name*-Werte.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-164">Use column names for *Field name* values.</span></span>
      - <span data-ttu-id="d3ec9-165">Verwenden Sie *searchable="true* für maximal 5 Felder, die durchsuchbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-165">Use *searchable="true"* for the fields that you want to be searchable up to a maximum of 5 fields.</span></span> <span data-ttu-id="d3ec9-166">Sie müssen mindestens ein Feld als durchsuchbar festlegen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-166">You must designate a minimum of one field as searchable.</span></span>

<span data-ttu-id="d3ec9-167">Im folgenden Beispiel definiert die XML-Datei das Schema für eine Datenbank mit Patientendatensätzen, wobei fünf Felder als durchsuchbar angegeben werden: *PatientID*, *MRN*, *SSN*, *Phone* und *DOB*.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-167">As an example, the following .xml file defines the schema for a patient records database, with five fields specified as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span>

<span data-ttu-id="d3ec9-168">(Sie können das Beispiel kopieren, ändern und verwenden.)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-168">(You can copy, modify, and use our example.)</span></span>

 ```xml
<EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
      <DataStore name="PatientRecords" description="Schema for patient records" version="1">
            <Field name="PatientID" searchable="true" />
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</EdmSchema>
```

4. <span data-ttu-id="d3ec9-169">[Stellen Sie eine Verbindung mit Office 365 Security & Compliance Center PowerShell her](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-169">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)</span></span>

5. <span data-ttu-id="d3ec9-170">Führen Sie die folgenden Cmdlets nacheinander aus, um das Datenbankschema hochzuladen:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-170">To upload the database schema, run the following cmdlets, one at a time:</span></span>

```powershell
$edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
```

<span data-ttu-id="d3ec9-171">Sie werden zu folgenden Bestätigungen aufgefordert:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-171">You will be prompted to confirm, as follows:</span></span>

> <span data-ttu-id="d3ec9-172">Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-172">Confirm</span></span>
>
> <span data-ttu-id="d3ec9-173">Möchten Sie diese Aktion wirklich ausführen?</span><span class="sxs-lookup"><span data-stu-id="d3ec9-173">ConfirmAre you sure you want to perform this action?</span></span>
>
> <span data-ttu-id="d3ec9-174">Das neue EDM-Schema für den Datenspeicher „patientrecords“ wird importiert.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-174">New EDM Schema for the data store 'patientrecords' will be imported.</span></span>
>
> <span data-ttu-id="d3ec9-175">\[J\] Ja \[A\] Ja für alle \[N\] Nein \[L\] Nein für alle \[?\] Hilfe (Standard ist "J"):</span><span class="sxs-lookup"><span data-stu-id="d3ec9-175">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
> <span data-ttu-id="d3ec9-176">Wenn Sie möchten, dass Ihre Änderungen ohne Bestätigung durchgeführt werden, verwenden Sie in Schritt 5 stattdessen das folgende Cmdlet: New-DlpEdmSchema -FileData $edmSchemaXml</span><span class="sxs-lookup"><span data-stu-id="d3ec9-176">If you want your changes to occur without confirmation, in Step 5, use this cmdlet instead: New-DlpEdmSchema -FileData $edmSchemaXml</span></span>

> [!NOTE]
> <span data-ttu-id="d3ec9-177">Es kann zwischen 10–60 Minuten dauern, bis das EDMSchema durch Ergänzungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-177">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="d3ec9-178">Das Update muss abgeschlossen sein, bevor Sie Schritte ausführen, die die Zusätze verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-178">The update must complete before you execute steps that use the additions.</span></span>

<span data-ttu-id="d3ec9-179">Nachdem das Schema für Ihre Datenbank mit vertraulichen Informationen definiert wurde, besteht der nächste Schritt darin, ein Regelpaket einzurichten.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-179">Now that the schema for your database of sensitive information is defined, the next step is to set up a rule package.</span></span> <span data-ttu-id="d3ec9-180">Fahren Sie mit dem Abschnitt [Einrichten eines Regelpakets](#set-up-a-rule-package) fort.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-180">Proceed to the section [Set up a rule package](#set-up-a-rule-package).</span></span>

#### <a name="editing-the-schema-for-edm-based-classification"></a><span data-ttu-id="d3ec9-181">Bearbeiten des Schemas für die EDM-basierte Klassifikation</span><span class="sxs-lookup"><span data-stu-id="d3ec9-181">Editing the schema for EDM-based classification</span></span>

<span data-ttu-id="d3ec9-182">Wenn Sie Änderungen an Ihrer edm.xml-Datei vornehmen und z. B. ändern möchten, welche Felder für die EDM-basierte Klassifikation verwendet werden, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-182">If you want to make changes to your edm.xml file, such as changing which fields are used for EDM-based classification, follow these steps:</span></span>

1. <span data-ttu-id="d3ec9-183">Bearbeiten Sie Ihre edm.mxl-Datei (die Datei, die im Abschnitt [Definieren des Schemas](#define-the-schema-for-your-database-of-sensitive-information) in diesem Artikel behandelt wird).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-183">Edit your edm.xml file (this is the file discussed in the [Define the schema](#define-the-schema-for-your-database-of-sensitive-information) section of this article).</span></span>

2. <span data-ttu-id="d3ec9-184">[Stellen Sie eine Verbindung mit Office 365 Security & Compliance Center PowerShell her](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-184">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)</span></span>

3. <span data-ttu-id="d3ec9-185">Führen Sie die folgenden Cmdlets nacheinander aus, um Ihr Datenbankschema zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-185">To update your database schema, run the following cmdlets, one at a time:</span></span>

```powershell
$edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
```

<span data-ttu-id="d3ec9-186">Sie werden zu folgenden Bestätigungen aufgefordert:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-186">You will be prompted to confirm, as follows:</span></span>

> <span data-ttu-id="d3ec9-187">Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-187">Confirm</span></span>
>
> <span data-ttu-id="d3ec9-188">Möchten Sie diese Aktion wirklich ausführen?</span><span class="sxs-lookup"><span data-stu-id="d3ec9-188">ConfirmAre you sure you want to perform this action?</span></span>
>
> <span data-ttu-id="d3ec9-189">Das EDM-Schema für den Datenspeicher „patientrecords“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-189">EDM Schema for the data store 'patientrecords' will be updated.</span></span>
>
> <span data-ttu-id="d3ec9-190">\[J\] Ja \[A\] Ja für alle \[N\] Nein \[L\] Nein für alle \[?\] Hilfe (Standard ist "J"):</span><span class="sxs-lookup"><span data-stu-id="d3ec9-190">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
> <span data-ttu-id="d3ec9-191">Wenn Sie möchten, dass Ihre Änderungen ohne Bestätigung durchgeführt werden, verwenden Sie in Schritt 3 stattdessen das folgende Cmdlet: Set-DlpEdmSchema -FileData $edmSchemaXml</span><span class="sxs-lookup"><span data-stu-id="d3ec9-191">If you want your changes to occur without confirmation, in Step 3, use this cmdlet instead: Set-DlpEdmSchema -FileData $edmSchemaXml</span></span>

> [!NOTE]
> <span data-ttu-id="d3ec9-192">Es kann zwischen 10–60 Minuten dauern, bis das EDMSchema durch Ergänzungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-192">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="d3ec9-193">Das Update muss abgeschlossen sein, bevor Sie Schritte ausführen, die die Zusätze verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-193">The update must complete before you execute steps that use the additions.</span></span>

## <a name="removing-the-schema-for-edm-based-classification"></a><span data-ttu-id="d3ec9-194">Entfernen des Schemas für die EDM-basierte Klassifikation</span><span class="sxs-lookup"><span data-stu-id="d3ec9-194">Removing the schema for EDM-based classification</span></span>

<span data-ttu-id="d3ec9-195">(Nach Bedarf) Wenn Sie das Schema entfernen möchten, das Sie für die EDM-basierte Klassifizierung verwenden, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-195">(As needed) If you want to remove the schema you're using for EDM-based classification, follow these steps:</span></span>

1. <span data-ttu-id="d3ec9-196">[Stellen Sie eine Verbindung mit Office 365 Security & Compliance Center PowerShell her](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-196">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)</span></span>

2. <span data-ttu-id="d3ec9-197">Führen Sie die folgenden PowerShell-Cmdlets aus, und ersetzen Sie dabei den Datenspeichernamen "patientrecords" durch den Namen, den Sie entfernen möchten:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-197">Run the following PowerShell cmdlets, substituting the data store name of "patientrecords" with the one you want to remove:</span></span>

```powershell
Remove-DlpEdmSchema -Identity patientrecords
```

<span data-ttu-id="d3ec9-198">Sie werden zu folgenden Bestätigungen aufgefordert:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-198">You will be prompted to confirm, as follows:</span></span>

> <span data-ttu-id="d3ec9-199">Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-199">Confirm</span></span>
>
> <span data-ttu-id="d3ec9-200">Möchten Sie diese Aktion wirklich ausführen?</span><span class="sxs-lookup"><span data-stu-id="d3ec9-200">ConfirmAre you sure you want to perform this action?</span></span>
>
> <span data-ttu-id="d3ec9-201">Das EDM-Schema für den Datenspeicher „patientrecords“ wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-201">EDM Schema for the data store 'patientrecords' will be removed.</span></span>
>
> <span data-ttu-id="d3ec9-202">\[J\] Ja \[A\] Ja für alle \[N\] Nein \[L\] Nein für alle \[?\] Hilfe (Standard ist "J"):</span><span class="sxs-lookup"><span data-stu-id="d3ec9-202">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
>  <span data-ttu-id="d3ec9-203">Wenn Sie möchten, dass Ihre Änderungen ohne Bestätigung durchgeführt werden, verwenden Sie in Schritt 2 stattdessen das folgende Cmdlet: Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span><span class="sxs-lookup"><span data-stu-id="d3ec9-203">If you want your changes to occur without confirmation, in Step 2, use this cmdlet instead: Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span></span>

### <a name="set-up-a-rule-package"></a><span data-ttu-id="d3ec9-204">Einrichten eines Regelpakets</span><span class="sxs-lookup"><span data-stu-id="d3ec9-204">Set up a rule package</span></span>

1. <span data-ttu-id="d3ec9-205">Erstellen Sie ein Regelpaket im XML-Format (mit Unicode-Codierung), ähnlich wie im folgenden Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-205">Create a rule package in .xml format (with Unicode encoding), similar to the following example.</span></span> <span data-ttu-id="d3ec9-206">(Sie können das Beispiel kopieren, ändern und verwenden.)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-206">(You can copy, modify, and use our example.)</span></span>

<span data-ttu-id="d3ec9-207">Vergewissern Sie sich beim Einrichten des Regelpakets, dass Sie die CSV-Datei und die edm.xml-Datei korrekt referenzieren.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-207">When you set up your rule package, make sure to correctly reference your .csv file and edm.xml file.</span></span> <span data-ttu-id="d3ec9-208">Sie können das Beispiel kopieren, ändern und verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-208">You can copy, modify, and use our example.</span></span> <span data-ttu-id="d3ec9-209">In dieser XML-Beispieldatei müssen die folgenden Felder so angepasst werden, dass Sie Ihren vertraulichen EDM-Typ erstellen:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-209">In this sample xml the following fields needs to be customized to create your EDM sensitive type:</span></span>

- <span data-ttu-id="d3ec9-210">**RulePack id und ExactMatch id**: Verwenden Sie [New-GUID](https://docs.microsoft.com/de-DE/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6), um eine GUID zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-210">**RulePack id & ExactMatch id**: Use [New-GUID](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) to generate a GUID.</span></span>

- <span data-ttu-id="d3ec9-211">**Datenspeicher**: Dieses Feld gibt den zu verwendenden EDM-Nachschlage-Datenspeicher an.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-211">**Datastore**: This field specifies EDM lookup data store to be used.</span></span> <span data-ttu-id="d3ec9-212">Sie geben einen Datenquellennamen eines konfigurierten EDM-Schemas an.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-212">You provide a data source name of a configured EDM Schema.</span></span>

- <span data-ttu-id="d3ec9-213">**idMatch**: Dieses Feld verweist auf das primäre Element für EDM.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-213">**idMatch**: This field points to the primary element for EDM.</span></span>
  - <span data-ttu-id="d3ec9-214">Stimmt überein mit: gibt das Feld an, das in der exakten Suche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-214">Matches: Specifies the field to be used in exact lookup.</span></span> <span data-ttu-id="d3ec9-215">Sie geben den Namen eines durchsuchbaren Felds im EDM-Schema für den Datenspeicher an.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-215">You provide a searchable field name in EDM Schema for the DataStore.</span></span>
  - <span data-ttu-id="d3ec9-216">Klassifizierung: Dieses Feld gibt die Übereinstimmung für den vertraulichen Typ an, der EDM-Nachschlagevorgänge auslöst.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-216">Classification: This field specifies the sensitive type match that triggers EDM lookup.</span></span> <span data-ttu-id="d3ec9-217">Sie können den Namen oder die GUID einer vorhandenen integrierten oder benutzerdefinierten Klassifizierung angeben.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-217">You can provide Name or GUID of an existing built-in or custom classification.</span></span>

- <span data-ttu-id="d3ec9-218">**Übereinstimmung:** Dieses Feld verweist auf zusätzliche Nachweise, die sich in der Nähe von "idMatch" befinden.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-218">**Match:** This field points to additional evidence found in proximity of idMatch.</span></span>
  - <span data-ttu-id="d3ec9-219">Stimmt überein mit: Sie geben einen Feldnamen im EDM-Schema für den Datenspeicher an.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-219">Matches: You provide any field name in EDM Schema for DataStore.</span></span>
- <span data-ttu-id="d3ec9-220">**Ressource:** In diesem Abschnitt werden der Name und die Beschreibung für den vertraulichen Typ in mehreren Sprachversionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-220">**Resource:** This section specifies the name and description for sensitive type in multiple locales.</span></span>
  - <span data-ttu-id="d3ec9-221">idRef: Sie geben die GUID für „ExactMatch id“ an.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-221">idRef: You provide GUID for ExactMatch id.</span></span>
  - <span data-ttu-id="d3ec9-222">Beschreibungen „Name“ und „Bearbeiten des Schemas“: Passen Sie nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-222">Name & des Editing the schema criptions: customize as required.</span></span>

```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2018/edm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b11">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care EDM Rulepack</Name>
        <Description>This rule package contains the EDM sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="100">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </ExactMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB371">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">EDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
```

1. <span data-ttu-id="d3ec9-223">Laden Sie das Regelpaket hoch, indem Sie nacheinander die folgenden PowerShell-Cmdlets ausführen:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-223">Upload the rule package by running the following PowerShell cmdlets, one at a time:</span></span>

```powershell
$rulepack=Get-Content .\\rulepack.xml -Encoding Byte -ReadCount 0
New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack
```

<span data-ttu-id="d3ec9-224">Sie haben die EDM-basierte Klassifizierung nun eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-224">At this point, you have set up EDM-based classification.</span></span> <span data-ttu-id="d3ec9-225">Im nächsten Schritt werden die vertraulichen Daten indiziert und dann hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-225">The next step is to index the sensitive data, and then upload the indexed data.</span></span>

<span data-ttu-id="d3ec9-226">Wie Sie im vorherigen Verfahren erfahren haben, wurden im PatientRecords-Schema fünf Felder als durchsuchbar definiert: *PatientID*, *MRN*, *SSN*, *Phone* und *DOB*.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-226">Recall from the previous procedure that our PatientRecords schema defines five fields as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span> <span data-ttu-id="d3ec9-227">Unser Beispiel für ein Regelpaket enthält diese Felder und verweist auf die Datenbankschemadatei (edm.xml), mit einem *ExactMatch*-Element pro durchsuchbarem Feld.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-227">Our example rule package includes those fields and references the database schema file (edm.xml), with one *ExactMatch* items per searchable field.</span></span> <span data-ttu-id="d3ec9-228">Sehen Sie sich das folgende ExactMatch-Element an:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-228">Consider the following ExactMatch item:</span></span>

```xml
<ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="100">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </ExactMatch>
```

<span data-ttu-id="d3ec9-229">Beachten Sie in diesem Beispiel Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-229">In connection with this point, note the following:</span></span>

- <span data-ttu-id="d3ec9-230">Der dataStore-Name verweist auf die zuvor erstellte CSV-Datei: **dataStore = "PatientRecords"**.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-230">The dataStore name references the .csv file we created earlier: **dataStore = "PatientRecords"**.</span></span>

- <span data-ttu-id="d3ec9-231">Der idMatch-Wert verweist auf ein durchsuchbares Feld, das in der Datenbankschema-Datei aufgelistet ist: **idMatch matches = "SSN"**.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-231">The idMatch value references a searchable field that is listed in the database schema file: **idMatch matches = "SSN"**.</span></span>

- <span data-ttu-id="d3ec9-232">Der classification-Wert verweist auf einen vorhandenen oder benutzerdefinierten vertraulichen Informationstyp: **classification = "US-Sozialversicherungsnummer (SSN)"**.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-232">The classification value references an existing or custom sensitive information type: **classification = "U.S. Social Security Number (SSN)"**.</span></span> <span data-ttu-id="d3ec9-233">(In diesem Fall wird der vorhandene vertrauliche Informationstyp "US-Sozialversicherungsnummer" verwendet.)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-233">(In this case, we use the existing sensitive information type of U.S. Social Security Number.)</span></span>

> [!NOTE]
> <span data-ttu-id="d3ec9-234">Es kann zwischen 10–60 Minuten dauern, bis das EDMSchema durch Ergänzungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-234">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="d3ec9-235">Das Update muss abgeschlossen sein, bevor Sie Schritte ausführen, die die Zusätze verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-235">The update must complete before you execute steps that use the additions.</span></span>

### <a name="part-2-index-and-upload-the-sensitive-data"></a><span data-ttu-id="d3ec9-236">Teil 2: Indizieren und Hochladen der vertraulichen Daten</span><span class="sxs-lookup"><span data-stu-id="d3ec9-236">Part 2: Index and upload the sensitive data</span></span>

<span data-ttu-id="d3ec9-237">In dieser Phase richten Sie eine benutzerdefinierte Sicherheitsgruppe, ein Benutzerkonto und das Tool EDM-Upload-Agent ein.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-237">During this phase, you set up a custom security group and user account, and set up the EDM Upload Agent tool.</span></span> <span data-ttu-id="d3ec9-238">Dann verwenden Sie das Tool, um die vertraulichen Daten zu indizieren und die indizierten Daten hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-238">Then, you use the tool to index the sensitive data, and upload the indexed data.</span></span>

#### <a name="set-up-the-security-group-and-user-account"></a><span data-ttu-id="d3ec9-239">Einrichten der Sicherheitsgruppe und des Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="d3ec9-239">Set up the security group and user account</span></span>

1. <span data-ttu-id="d3ec9-240">Wechseln Sie als globaler Administrator zum Admin Center ([https://admin.microsoft.com](https://admin.microsoft.com/)) und [erstellen Sie eine Sicherheitsgruppe](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) mit dem Namen „EDM\_DataUploaders“.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-240">As a global administrator, go to the admin center ([https://admin.microsoft.com](https://admin.microsoft.com/)) and [create a security group](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) called EDM\_DataUploaders.</span></span>

2. <span data-ttu-id="d3ec9-241">Fügen Sie einen oder mehrere Benutzer zur *EDM\_DataUploaders*-Sicherheitsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-241">Add one or more users to the *EDM\_DataUploaders* security group.</span></span> <span data-ttu-id="d3ec9-242">(Diese Benutzer verwalten die Datenbank mit vertraulichen Informationen.)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-242">(These users will manage the database of sensitive information.)</span></span>

3. <span data-ttu-id="d3ec9-243">Stellen Sie sicher, dass jeder Benutzer, der die vertraulichen Daten verwaltet, ein lokaler Administrator auf dem Computer ist, der für den EDM-Upload-Agent verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-243">Make sure each user who is managing the sensitive data is a local admin on the machine used for the EDM Upload Agent.</span></span>

#### <a name="set-up-the-edm-upload-agent"></a><span data-ttu-id="d3ec9-244">Einrichten des EDM-Upload-Agenten</span><span class="sxs-lookup"><span data-stu-id="d3ec9-244">Set up the EDM Upload Agent</span></span>

>[!NOTE]
> <span data-ttu-id="d3ec9-245">Bevor Sie mit diesem Verfahren beginnen, stellen Sie sicher, dass Sie Mitglied der Sicherheitsgruppe *EDM\_DataUploaders* und lokaler Administrator auf Ihrem Computer sind.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-245">Before you begin this procedure, make sure that you are a member of the *EDM\_DataUploaders* security group and a local admin on your machine.</span></span>

1. <span data-ttu-id="d3ec9-246">Laden Sie den [EDM-Upload-Agenten](https://go.microsoft.com/fwlink/?linkid=2088639) herunter und installieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-246">Download and install the [EDM Upload Agent](https://go.microsoft.com/fwlink/?linkid=2088639).</span></span> <span data-ttu-id="d3ec9-247">Standardmäßig sollte der Installationsspeicherort C:\\Programme\\Microsoft\\EdmUploadAgent sein.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-247">By default, the installation location should be C:\\Program Files\\Microsoft\\EdmUploadAgent.</span></span>

2. <span data-ttu-id="d3ec9-248">Wenn Sie den EDM-Upload-Agenten autorisieren möchten, öffnen Sie die Windows-Eingabeaufforderung (als Administrator), und führen Sie dann den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-248">To authorize the EDM Upload Agent, open Windows Command Prompt (as an administrator), and then run the following command:</span></span>

    `EdmUploadAgent.exe /Authorize`

3. <span data-ttu-id="d3ec9-249">Melden Sie sich mit Ihrem Office 365-Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-249">Sign in with your Office 365 work or school account.</span></span>

<span data-ttu-id="d3ec9-250">Im nächsten Schritt verwenden Sie den EDM-Upload-Agent, um die vertraulichen Daten zu indizieren und dann die indizierten Daten hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-250">The next step is to use the EDM Upload Agent to index the sensitive data, and then upload the indexed data.</span></span>

#### <a name="index-and-upload-the-sensitive-data"></a><span data-ttu-id="d3ec9-251">Indizieren und Hochladen der vertraulichen Daten</span><span class="sxs-lookup"><span data-stu-id="d3ec9-251">Index and upload the sensitive data</span></span>

<span data-ttu-id="d3ec9-252">Speichern Sie die Datei mit den vertraulichen Daten (unser Beispiel ist wie erwähnt *PatientRecords.csv*) auf dem lokalen Laufwerk Ihres Computers.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-252">Save the sensitive data file (recall our example is *PatientRecords.csv*) to the local drive on the machine.</span></span> <span data-ttu-id="d3ec9-253">(Die Beispieldatei *PatientRecords.csv* wurde in C:\\Edm\\Data gespeichert.)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-253">(We saved our example *PatientRecords.csv* file to C:\\Edm\\Data.)</span></span>

<span data-ttu-id="d3ec9-254">Um die vertraulichen Daten zu indizieren und hochzuladen, führen Sie den folgenden Befehl in der Windows-Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-254">To index and upload the sensitive data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /UploadData /DataStoreName \<DataStoreName\> /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

<span data-ttu-id="d3ec9-255">Beispiel: **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\\Edm\\Hash\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span><span class="sxs-lookup"><span data-stu-id="d3ec9-255">Example: **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\\Edm\\Hash\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span></span>

<span data-ttu-id="d3ec9-256">Wenn Sie das Indizieren vertraulicher Daten in einer isolierten Umgebung trennen und ausführen möchten, führen Sie die Schritte „Indizieren“ und „Hochladen“ separat aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-256">To separate and execute index of sensitive data in an isolated environment, execute index and upload steps separately.</span></span>

<span data-ttu-id="d3ec9-257">Um die vertraulichen Daten zu indizieren, führen Sie den folgenden Befehl in der Windows-Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-257">To index the sensitive data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /CreateHash /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

<span data-ttu-id="d3ec9-258">Beispiel: **EdmUploadAgent.exe /CreateHash /DataFile C:\\Edm\\Data\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span><span class="sxs-lookup"><span data-stu-id="d3ec9-258">Example: **EdmUploadAgent.exe /CreateHash /DataFile C:\\Edm\\Data\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span></span>

<span data-ttu-id="d3ec9-259">Um die vertraulichen Daten hochzuladen, führen Sie den folgenden Befehl in der Windows-Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-259">To upload the indexed data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /UploadHash /DataStoreName \<DataStoreName\> /HashFile \<HashedSourceFilePath\>`

<span data-ttu-id="d3ec9-260">Beispiel: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span><span class="sxs-lookup"><span data-stu-id="d3ec9-260">Example: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span></span>

<span data-ttu-id="d3ec9-261">Um zu überprüfen, ob Ihre vertraulichen Daten hochgeladen wurden, führen Sie den folgenden Befehl in der Windows-Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-261">To verify your sensitive data has been uploaded, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /GetDataStore`

<span data-ttu-id="d3ec9-262">Sie sehen eine Liste der Datenspeicher mit dem Zeitpunkt der letzten Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-262">You'll see a list of data stores and when they were last updated.</span></span>

<span data-ttu-id="d3ec9-263">Fahren Sie mit dem Einrichten des Prozesses und des Zeitplans für das [Aktualisieren der Datenbank für vertrauliche Informationen](#refreshing-your-sensitive-information-database) fort.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-263">Proceed to set up your process and schedule for [Refreshing your sensitive information database](#refreshing-your-sensitive-information-database).</span></span>

<span data-ttu-id="d3ec9-264">Sie können nun die EDM-basierte Klassifikation mit Ihren Microsoft Cloud Services verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-264">At this point, you are ready to use EDM-based classification with your Microsoft cloud services.</span></span> <span data-ttu-id="d3ec9-265">Sie können beispielsweise [eine DLP-Richtlinie mithilfe der EDM-basierten Klassifizierung einrichten](#to-create-a-dlp-policy-with-edm).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-265">For example, you can [set up a DLP policy using EDM-based classification](#to-create-a-dlp-policy-with-edm).</span></span>

#### <a name="refreshing-your-sensitive-information-database"></a><span data-ttu-id="d3ec9-266">Aktualisieren der Datenbank für vertrauliche Informationen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-266">Refreshing your sensitive information database</span></span>

<span data-ttu-id="d3ec9-267">Sie können Ihre Datenbank für vertrauliche Informationen täglich oder wöchentlich aktualisieren, und das EDM-Upload-Tool kann die vertraulichen Daten neu indizieren und dann die indizierten Daten erneut hochladen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-267">You can refresh your sensitive information database daily or weekly, and the EDM Upload Tool can reindex the sensitive data and then reupload the indexed data.</span></span>

1. <span data-ttu-id="d3ec9-268">Ermitteln Sie den Vorgang und die Häufigkeit (täglich oder wöchentlich) zum Aktualisieren der Datenbank mit vertraulichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-268">Determine your process and frequency (daily or weekly) for refreshing the database of sensitive information.</span></span>

2. <span data-ttu-id="d3ec9-269">Exportieren Sie die vertraulichen Daten erneut in eine App, wie z. B. Microsoft Excel, und speichern Sie die Datei im CSV-Format.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-269">Re-export the sensitive data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="d3ec9-270">Behalten Sie den Dateinamen und den Speicherort bei, den Sie beim Ausführen der unter [Indizieren und Hochladen vertraulicher Daten](#index-and-upload-the-sensitive-data) beschriebenen Schritte verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-270">Keep the same file name and location you used when you followed the steps described in [Index and upload the sensitive data](#index-and-upload-the-sensitive-data).</span></span>

> [!NOTE]
> <span data-ttu-id="d3ec9-271">Wenn es keine Änderungen an der Struktur (Feldnamen) der CSV-Datei gibt, müssen Sie auch keine an der Datenbankschemadatei vornehmen, wenn Sie die Daten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-271">If there are no changes to the structure (field names) of the .csv file, you won't need to make any changes to your database schema file when you refresh the data.</span></span> <span data-ttu-id="d3ec9-272">Wenn Sie jedoch Änderungen vornehmen müssen, stellen Sie sicher, dass Sie das Datenbankschema und Ihr Regelpaket entsprechend bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-272">But if you must make changes, make sure to edit the database schema and your rule package accordingly.</span></span>

3. <span data-ttu-id="d3ec9-273">Verwenden Sie die [Aufgabenplanung](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page), um die Schritte 2 und 3 im Verfahren [Indizieren und Hochladen vertraulicher Daten](#index-and-upload-the-sensitive-data) zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-273">Use [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) to automate steps 2 and 3 in the [Index and upload the sensitive data](#index-and-upload-the-sensitive-data) procedure.</span></span> <span data-ttu-id="d3ec9-274">Sie können Aufgaben mithilfe verschiedener Methoden planen:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-274">You can schedule tasks using several methods:</span></span>

| <span data-ttu-id="d3ec9-275">**Methode**</span><span class="sxs-lookup"><span data-stu-id="d3ec9-275">**Method**</span></span>             | <span data-ttu-id="d3ec9-276">**Nächste Schritte**</span><span class="sxs-lookup"><span data-stu-id="d3ec9-276">**What to do**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="d3ec9-277">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d3ec9-277">Windows PowerShell</span></span>     | <span data-ttu-id="d3ec9-278">Siehe die Dokumentation [Aufgabenplanung](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) und das [PowerShell-Beispielskript](#example-powershell-script-for-task-scheduler) in diesem Artikel</span><span class="sxs-lookup"><span data-stu-id="d3ec9-278">See the [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) documentation and the [example PowerShell script](#example-powershell-script-for-task-scheduler) in this article</span></span> |
| <span data-ttu-id="d3ec9-279">Aufgabenplaner-API</span><span class="sxs-lookup"><span data-stu-id="d3ec9-279">Task Scheduler API</span></span>     | <span data-ttu-id="d3ec9-280">Lesen Sie die Dokumentation [Aufgabenplanung](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-280">See the [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) documentation</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d3ec9-281">Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d3ec9-281">Windows user interface</span></span> | <span data-ttu-id="d3ec9-282">Klicken Sie in Windows auf **Start**, und geben Sie „Aufgabenplanung“ ein.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-282">In Windows, click **Start**, and type Task Scheduler.</span></span> <span data-ttu-id="d3ec9-283">Klicken Sie dann in der Ergebnisliste mit der rechten Maustaste auf **Aufgabenplanung** und wählen Sie **Als Administrator ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-283">Then, in the list of results, right-click **Task Scheduler**, and choose **Run as administrator**.</span></span>                                                                                                                                                                                                                                                                           |

#### <a name="example-powershell-script-for-task-scheduler"></a><span data-ttu-id="d3ec9-284">„PowerShell-Beispielskript“ für „Aufgabenplanung“</span><span class="sxs-lookup"><span data-stu-id="d3ec9-284">Example PowerShell script for Task Scheduler</span></span>

<span data-ttu-id="d3ec9-285">Dieser Abschnitt enthält ein Beispiel für ein PowerShell-Skript, das Sie verwenden können, um Ihre Aufgaben zum Indizieren von Daten und Hochladen der indizierten Daten zu planen:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-285">This section includes an example PowerShell script you can use to schedule your tasks for indexing data and uploading the indexed data:</span></span>

##### <a name="to-schedule-index-and-upload-in-a-combined-step"></a><span data-ttu-id="d3ec9-286">So planen Sie das Indizieren und Hochladen in einem kombinierten Schritt</span><span class="sxs-lookup"><span data-stu-id="d3ec9-286">To schedule index and upload in a combined step</span></span>

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
\# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\\$dataStoreName$csvext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$uploadDataArgs = '/UploadData /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ‘ /HashLocation’ + $hashLocation
\# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadDataArgs -WorkingDirectory $edminstallpath
\# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
\# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
\# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
\# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=\[Runtime.InteropServices.Marshal\]::PtrToStringAuto(\[Runtime.InteropServices.Marshal\]::SecureStringToBSTR($creds.Password))
\# Register the scheduled task
$taskName = 'EDMUpload\_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```

#### <a name="to-schedule-index-and-upload-as-separate-steps"></a><span data-ttu-id="d3ec9-287">So planen Sie das Indizieren und Hochladen als separate Schritte</span><span class="sxs-lookup"><span data-stu-id="d3ec9-287">To schedule index and upload as separate steps</span></span>

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
\# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\\$dataStoreName$csvext"
$hashFile = "$fileLocation\\$dataStoreName$edmext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash' + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation
$uploadHashArgs = '/UploadHash /DataStoreName ' + $dataStoreName + ' /HashFile ' + $hashFile
\# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $createHashArgs -WorkingDirectory $edminstallpath
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadHashArgs -WorkingDirectory $edminstallpath
\# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
\# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
\# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
\# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=\[Runtime.InteropServices.Marshal\]::PtrToStringAuto(\[Runtime.InteropServices.Marshal\]::SecureStringToBSTR($creds.Password))
\# Register the scheduled task
$taskName = 'EDMUpload\_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```

### <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a><span data-ttu-id="d3ec9-288">Teil 3: Verwenden der EDM-basierten Klassifizierung mit Ihren Microsoft Cloud Services</span><span class="sxs-lookup"><span data-stu-id="d3ec9-288">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>

<span data-ttu-id="d3ec9-289">Office 365 DLP für Exchange Online (E-Mail-Adresse), OneDrive for Business (Dateien), Microsoft Teams (Unterhaltungen) und Microsoft Cloud App Security DLP-Richtlinien unterstützen vertrauliche EDM-Informationstypen.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-289">Office 365 DLP for Exchange Online (email), OneDrive for Business (files), Microsoft Teams (conversations) and Microsoft Cloud App Security DLP policies will support EDM sensitive information types.</span></span>

<span data-ttu-id="d3ec9-290">Vertrauliche EDM-Informationstypen für die folgenden Szenarien sind derzeit in der Entwicklung, aber noch nicht verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d3ec9-290">EDM sensitive information types for following scenarios are currently in development, but not yet available:</span></span>

- <span data-ttu-id="d3ec9-291">Office 365 DLP für SharePoint (Dateien)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-291">Office 365 DLP for SharePoint (files)</span></span>
- <span data-ttu-id="d3ec9-292">automatische Klassifizierung von Vertraulichkeits- und Aufbewahrungsbezeichnungen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-292">Auto-classification of sensitivity labels and retention labels</span></span>

#### <a name="to-create-a-dlp-policy-with-edm"></a><span data-ttu-id="d3ec9-293">Erstellen einer DLP-Richtlinie mit EDM</span><span class="sxs-lookup"><span data-stu-id="d3ec9-293">To create a DLP policy with EDM</span></span>

1. <span data-ttu-id="d3ec9-294">Wechseln Sie zum Security & Compliance Center ([https://protection.office.com](https://protection.office.com/)).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-294">Go to the Security & Compliance Center</span></span>

2. <span data-ttu-id="d3ec9-295">Klicken Sie auf die **Richtlinie** \> **zur Verhinderung von Datenverlust**.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-295">Choose **Data loss prevention** \> **Policy**.</span></span>

3. <span data-ttu-id="d3ec9-296">Wählen Sie **Richtlinie erstellen** \> **Benutzerdefiniert** \> **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-296">Choose **Create a policy** \> **Custom** \> **Next**.</span></span>

4. <span data-ttu-id="d3ec9-297">Geben Sie auf der Registerkarte **Richtlinie benennen** einen Namen und eine Beschreibung ein, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-297">On the **Name your policy** tab, specify a name and description, and then choose **Next**.</span></span>

5. <span data-ttu-id="d3ec9-298">Wählen Sie auf der Registerkarte **Speicherorte auswählen**  **Bestimmte Speicherorte auswählen** und dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-298">On the **Choose locations** tab, select **Let me choose specific locations**, and then choose **Next**.</span></span>

6. <span data-ttu-id="d3ec9-299">Wählen Sie in der Spalte **Status**  **Exchange-E-Mail, OneDrive-Konten, Teams-Chat und Kanalnachricht** und dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-299">In the **Status** column, select **Exchange email, OneDrive accounts, Teams chat and channel message** , and then choose **Next**.</span></span> <span data-ttu-id="d3ec9-300">(Hinweis: EDM wird von SharePoint-Websites derzeit nicht unterstützt, und DLP-Richtlinien erkennen keine Dateien in SharePoint durch EDM).</span><span class="sxs-lookup"><span data-stu-id="d3ec9-300">(Note: EDM is currently not supported in SharePoint sites and DLP policy will not detect files in Sharepoint for EDM)</span></span>

7. <span data-ttu-id="d3ec9-301">Wählen Sie auf der Registerkarte **Richtlinieneinstellungen**  **Erweiterte Einstellungen verwenden** und dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-301">On the **Policy settings** tab, choose **Use advanced settings**, and then choose **Next**.</span></span>

8. <span data-ttu-id="d3ec9-302">Wählen Sie **+ Neue Regel** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-302">Choose **+ New rule**.</span></span>

9. <span data-ttu-id="d3ec9-303">Geben Sie im Abschnitt **Name** einen Namen und eine Beschreibung für die Regel ein.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-303">In the **Name** section, specify a name and description for the rule.</span></span>

10. <span data-ttu-id="d3ec9-304">Wählen Sie im Abschnitt **Bedingungen** in der Liste **+ Bedingung hinzufügen**  **Inhalt enthält vertraulichen Typ** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-304">In the **Conditions** section, in the **+ Add a condition** list, choose **Content contains sensitive type**.</span></span><br/><span data-ttu-id="d3ec9-305">![Inhalt enthält vertrauliche Informationstypen](media/edm-dlp-newrule-conditions.png)</span><span class="sxs-lookup"><span data-stu-id="d3ec9-305">![Content contains sensitive info types](media/edm-dlp-newrule-conditions.png)</span></span><br/>

11. <span data-ttu-id="d3ec9-306">Suchen Sie den vertraulichen Informationstyp, den Sie beim Einrichten Ihres Regelpakets erstellt haben, und wählen Sie dann **+ Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-306">Search for the sensitive information type you created when you set up your rule package, and then choose **+ Add**.</span></span>  
    <span data-ttu-id="d3ec9-307">Wählen Sie dann **Fertig** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-307">Then choose **Done**.</span></span>

12. <span data-ttu-id="d3ec9-308">Wählen Sie Optionen für die Regel aus, wie z. B. **Benutzerbenachrichtigungen**, **Außerkraftsetzungen durch Benutzer**, **Schadensberichte** usw., und dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-308">Finish selecting options for your rule, such as **User notifications**, **User overrides**, **Incident reports**, and so on, and then choose **Save**.</span></span>

13. <span data-ttu-id="d3ec9-309">Überprüfen Sie auf der Registerkarte **Richtlinieneinstellungen** Ihre Regeln und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-309">On the **Policy settings** tab, review your rules, and then choose **Next**.</span></span>

14. <span data-ttu-id="d3ec9-310">Geben Sie an, ob Sie die Richtlinie sofort aktivieren, testen oder deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-310">Specify whether to turn on the policy right away, test it out, or keep it turned off.</span></span> <span data-ttu-id="d3ec9-311">Wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-311">Then choose **Next**.</span></span>

15. <span data-ttu-id="d3ec9-312">Überprüfen Sie auf der Registerkarte **Überprüfen Sie Ihre Einstellungen** Ihre Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-312">On the **Review your settings** tab, review your policy.</span></span> <span data-ttu-id="d3ec9-313">Nehmen Sie alle nötigen Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-313">Make any needed changes.</span></span> <span data-ttu-id="d3ec9-314">Wenn Sie fertig sind, wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-314">When you're ready, choose **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="d3ec9-315">Es kann ungefähr eine Stunde dauern, bis Ihre neue DLP-Richtlinie im Rechenzentrum erscheint.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-315">Allow approximately one hour for your new DLP policy to work its way through your data center.</span></span>

## <a name="related-articles"></a><span data-ttu-id="d3ec9-316">Verwandte Artikel</span><span class="sxs-lookup"><span data-stu-id="d3ec9-316">Related articles</span></span>

[<span data-ttu-id="d3ec9-317">Integrierte vertrauliche Informationstypen und wonach diese suchen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-317">Built-in sensitive information types and what they look for</span></span>](https://docs.microsoft.com/de-DE/office365/securitycompliance/what-the-sensitive-information-types-look-for)

[<span data-ttu-id="d3ec9-318">Benutzerdefinierte vertrauliche Informationstypen</span><span class="sxs-lookup"><span data-stu-id="d3ec9-318">Custom sensitive information types</span></span>](https://docs.microsoft.com/de-DE/office365/securitycompliance/custom-sensitive-info-types)

[<span data-ttu-id="d3ec9-319">Überblick über DLP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d3ec9-319">Overview of DLP policies</span></span>](https://docs.microsoft.com/de-DE/office365/securitycompliance/data-loss-prevention-policies)

[<span data-ttu-id="d3ec9-320">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d3ec9-320">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)

[<span data-ttu-id="d3ec9-321">New-DlpEdmSchema</span><span class="sxs-lookup"><span data-stu-id="d3ec9-321">New-DlpEdmSchema</span></span>](https://docs.microsoft.com/de-DE/powershell/module/exchange/policy-and-compliance-dlp/new-dlpedmschema?view=exchange-ps)

## <a name="feedback"></a><span data-ttu-id="d3ec9-322">Feedback</span><span class="sxs-lookup"><span data-stu-id="d3ec9-322">Feedback</span></span>
<span data-ttu-id="d3ec9-323">GitHub-Feedback ist aktiviert, aber das Hinzufügen von Problemen ist nur auf der öffentlichen Website verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3ec9-323">GitHub feedback is enabled, but adding issues is only available on the public site.</span></span>
